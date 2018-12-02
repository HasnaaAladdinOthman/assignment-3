# assignment-3

drawing a multi colored triangle with glfw and shader

using GLFW to creating a window by using function {glfwCreateWindow}

if doesn't created output "Failed to create GLFW window" and terminate the window.

Using function {glCreateShader} to create shader.

create two types of shader:

1.vertex shader.
2.fregment shader

1) to create vertex shader:
"glCreateShader(GL_VERTEX_SHADER);".

using function "glGetShaderiv(vertexShader, GL_COMPILE_STATUS, &success) to Check for shader compile errors.

if(!success) call the function "glGetShaderInfoLog" and output message "error".

2) to create fregment shader :
 "glCreateShader(GL_FRAGMENT_SHADER);".
 
using function "glGetShaderiv(fragmentShader, GL_COMPILE_STATUS, &success);" to check for shader compile errors.

to link between shaders to use function "glCreateProgram();".

then attach shaders using glAttachShader(shaderProgram, vertexShader);
glAttachShader(shaderProgram, fragmentShader);

 use function "glGetProgramiv(shaderProgram, GL_LINK_STATUS, &success);" to check for linking errors.
 
 finally we should delete shader :
 
 glDeleteShader(vertexShader);
 glDeleteShader(fragmentShader);
 
