# cuda_raytracing_in_one_weekend


The aim of the project is to implement a simple raytracer in Cuda, following the book [Ray Tracing in One Weekend](https://raytracing.github.io/books/RayTracingInOneWeekend.html). 
The guide [Accelerated Ray Tracing in One Weekend](https://developer.nvidia.com/blog/accelerated-ray-tracing-cuda/) was a useful starting point. 
[tde-nico](https://github.com/tde-nico) and I worked on this project for the course of "Multicore and Embedded Programming" at the University of Rome, La Sapienza. You can find the report in the folder of the same name and the video we used as demo.


<!-- add image from  data/samples-code -->
![Sample](./data/samples-codes/tramonto6.ppm)


## Requirements
Cuda compilation tools, release 11.5, V11.5.119


## Usage

Compile
```
> make
```

Run
```
> make run
```


## Attunement

In order to change the setting, you can modify the macros defined in includes/raytracer.cuh, such as the image resolution, the number of samples, the maximum depth of the recursion, etc.

You can also choose to use the managed memory or not, and to use the shared memory or not. 
The shared memory is used to store the samples of the pixels and let the neighbouring threads to access them. It is useful in combination with a lower number of samples per pixel.


## Data

Here there are some files we used to test the raytracer. In old-codes you can find alternative versions that allowed us to create the *demo_60.avi* video and some experiments to counter the warp divergence. 


### Scenery

In order to change the scenery, you can directly change the *create_world* where all the objects are defined. You can also find some examples in the data/samples-code folder.

