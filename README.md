



```
npm init 
npm install materialize-css
sudo npm install grunt-cli -g
npm install grunt --save-dev
npm install grunt-contrib-copy --save-dev
npm install grunt-contrib-clean --save-dev

npm install grunt-contrib-concat --save-dev
npm install grunt-contrib-uglify --save-dev
npm install grunt-contrib-cssmin --save-dev
npm install grunt-usemin --save-dev
npm install grunt-contrib-imagemin --save-dev

```


Gruntfile.js init

```javascript
module.exports = function(grunt) {
   grunt.initConfig({
        copy: {
              public: {
                   cwd: 'public', 
                   src: ['**'], 
                   dest: 'dist', 
                   expand: true
              }
         }, 
         clean: {
              dist: {
                  src: ['dist']
              }
         }
  });

  grunt.registerTask('default', ['dist']);
  grunt.registerTask('dist', ['clean', 'copy']);

  grunt.loadNpmTasks('grunt-contrib-copy');
  grunt.loadNpmTasks('grunt-contrib-clean');
};
```