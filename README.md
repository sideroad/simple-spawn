Simplify spawn interface for across a multitude of platform
========================================
[spawn](http://nodejs.org/api/child_process.html#child_process_child_process_spawn_command_args_options) is very useful more than exec.
but command arguments is not instinctive and we should change arguments on windows OS.

This library wrapping this complexity and provide simple interface.


var spawn = require('simple-spawn').spawn,
    child = spawn('npm config ls');

child.stdout.on('data', function(data){
    process.stdout.write(''+data);
}
