#Apitrace - Initial state

##Initialisation

- Frame 0 contained all the stuff the SDL2 and GLEW did for us
    - e.g. setting of the framebuffer details, asking GL for function pointers
    - there's nothing interesting for us here
- We'll start look at Frame 1, which as the first call to **GL** that we've made (that we're interested in)
- At this point the context (the OpenGL state) is almost brand new

##Initial state

- Initially, every variable in the OpenGL state (of **our** context) is set to a default
- There are many variables in the OpenGL state.
- We are interested in only a small subset

##ApiTrace initially, with whole state

- note the thumbnails on the left are from the **end** of each frame

![01_initial_wholeState.png](assets/apitrace/01_initial/01_initial_wholeState.png)

##ApiTrace initially, only showing non-default state

- debug is enabled
- we've set the viewport, so viewport and scissor box are set
- our window is 600x600, so the viewport covers the whole window
    - we've set the viewport explicitly, to allow apiTrace to replay properly

![02_initial_nonDefaultState.png](assets/apitrace/01_initial/02_initial_nonDefaultState.png)


##Apitrace initially, with an unfilled back buffer (GL_BACK)

- at this point the back buffer hasn't been filled
    - it is just whatever happens to be whatever the GPU has in RAM already in the allocated area
![03_unfilledBackBuffer.png](assets/apitrace/01_initial/03_unfilledBackBuffer.png)


##Apitrace initially, with a unfilled back buffer (GL_BACK) - ZOOM

- large view of the back buffer
   - filled with random stuff that's being rendered previously
   - **fun days**

![04_unfilledBackBufferZoom.png](assets/apitrace/01_initial/04_unfilledBackBufferZoom.png)


##Apitrace initially, with no *uniform* variables set

- initially no *uniform* variables are set

![05_noUniformsSet.png](assets/apitrace/01_initial/05_noUniformsSet.png)
