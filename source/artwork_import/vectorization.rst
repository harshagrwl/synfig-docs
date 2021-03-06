Vectorization of Bitmaps
==============================================

Synfig Studio comes with a feature of Vectorization of Bitmaps. In this tutorial, we will learn what is Vectorization feature and how to use it. :)

What does Vectorization mean?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
There are two common ways to represent a two-dimensional image:

    * Raster Graphics or Bitmap Graphics
    * Vector Graphics

In Bitmap Graphics images are stored as a two-dimensional grid of pixels. This has some problems for example if a bitmap image is scaled it becomes blurry and pixelated.

We use Vector Graphics to solve this problem. For converting Bitmap image to Vector Image, Synfig uses vectorization algorithm from `OpenToonz <https://opentoonz.github.io/e/>`_

Usage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Upload the image and right-click on the Image Layer and select "Convert to Vector" command.

    .. image:: ../images/convert_to_vector.png

Clicking on this "Convert to Vector" will open a dialog box with the following settings:
    
    .. image:: ../images/vector_dialog_box.png
    

    * **Threshold** - sets the value of the darkest pixels to be taken into account to detect lines to be converted to vector
    * **Accuracy** - sets how much the vector stroke will follow the shape of the original drawing lines. High values create more precise strokes but makes them more complex.
    * **Despeckling** - ignores during the conversion small areas generated by the image noise; the higher the value, the larger the areas ignored.
    * **Max thickness** - sets the maximum vector stroke thickness; if this value is low very thick lines will be converted in two centerline strokes defining the line outline; if this value is high, they will be converted in a single centerline stroke.

As soon as the "Convert" button is clicked, the image is converted into a vector which contains all the outlines of the image.
    
    .. note::

     Synfig currently supports only centerline vectorization
        
