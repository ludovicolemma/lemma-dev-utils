# Development Kit

Here there are some useful functions I developed and use to speed up some of my coding sessions.

# Installation

With Python and Pip installed, do:

``` sh

   pip install lemma-dev-utils
   
```

# Functionalities

Currently the main functions are the "download" and "unzip" functions, for which I implemented a progress bar (useful when dealing with large files).

The function can be easily used as it follows:

``` sh

   download(url, file_name)
   unzip(path, file_name)

```

With file_name as the name of the file to download in a case and to unzip in the other, while path is the destination path (default is the current working directory)

I also implemented an object called ImageExtractor so that I could extract and see all images from websites in a few lines.

This is how it works:

First an instance of the object is created, it will extract direct links to images from the webpage:

``` sh

   ie = ImageExtractor(url)
   
```

Then it is possible to see which are the urls stored by using the attribute ".urls".

Then the following method can be called:

``` sh

   image_list = ie.display_list()
   
```

Which will download and store the images into a list for which I created a modified list object so that the images are shown when the object an image item is called upon.

Finally it is also possible to store all images present in the list by using:

``` sh

   image_list.save_all()
   
```

or considering that a copy of the images is stored in the ImageExtractor object (as attribute in ie.image_list), also the following method can be used if it isn't necessary to manipulate the list first.


``` sh

   ie.save_content()
   
```
