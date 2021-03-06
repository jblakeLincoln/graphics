#What Is GLSL?

##What Is GLSL?

- a high-level shading language
- based on the syntax of the C programming language
    - importantly **different** from C
- https://www.opengl.org/documentation/glsl/

##GLSL and the OpenGL pipeline

- GLSL is how you **program** the OpenGL pipeline
    - for the DirectX pipeline you use HLSL
    - there are other tools also
- GLSL programs are compiled at **run-time**
    - by **your** program
    - you've already been **unknowingly** doing this ...
- GLSL programs are also called **shaders**

##GLSL and the OpenGL pipeline 2

- GLSL programs run in very **specific** points in the OpenGL pipeline
- Each point in the pipeline takes a different **type** of GLSL program
    - what **types** of GLSL programs are there
    - **where** (in the pipeline) does each run?
    - what are the **inputs** and **outputs** of each?

##The inescapable GLSL

- Modern OpenGL (i.e. 3.0 upwards) **REQUIRES** you to use **GLSL programs**
- You **must** provide at least one **vertex program** and one **fragment program**

#Version fun ;-)

##Version fun ;-)

- Just like OpenGL there are many versions of GLSL
- You have to match your GLSL version to your OpenGL version
    - i.e. if you create an OpenGL 3.3 context then you **must** use GLSL 3.3
        - for *limited* values of *must*. Some drivers are quite tolerant

##GL vs GLSL version numbering

> GLSL versions have evolved alongside specific versions of the OpenGL API.
> It is only with OpenGL versions 3.3 and above that the GLSL and OpenGL major and minor version numbers match.
> These versions for GLSL and OpenGL are related in the following table.

    - http://en.wikipedia.org/wiki/OpenGL_Shading_Language#Versions

##

| GLSL Version | OpenGL Version | Date           | Shader Preprocessor |
|--------------|----------------|----------------|---------------------|
| 1.10.59      | 2.0            | April 2004     | #version 110        |
| 1.20.8       | 2.1            | September 2006 | #version 120        |
| 1.30.10      | 3.0            | August 2008    | #version 130        |
| **1.40.08**  | **3.1**        | March 2009     | **#version 140**    |
| 1.50.11      | 3.2            | August 2009    | #version 150        |
| 3.30.6       | 3.3            | February 2010  | #version 330        |
| 4.00.9       | 4.0            | March 2010     | #version 400        |
| 4.10.6       | 4.1            | July 2010      | #version 410        |
| 4.20.11      | 4.2            | August 2011    | #version 420        |
| 4.30.8       | 4.3            | August 2012    | #version 430        |
| 4.40         | 4.4            | July 2013      | #version 440        |
| 4.50         | 4.5            | August 2014    | #version 450        |

http://en.wikipedia.org/wiki/OpenGL_Shading_Language#Versions
