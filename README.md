mklapse
=======

This script is a merger of two or three other scripts I built around making a timelapse from a series of still images. It performs three major functions; Timelapse (-L), Composite (-C), and Anim (-A). The Anim function is dependent on the Composite function.

TIMELAPSE

The basic function, -L, creates a timelapse video, frame by frame, in the order each image was taken regardless of file name. It can resize the video as needed based on vertical resolution (default is 768 - probably because that was an easy fit for Vimeo). It can also adjust bitrate, number of frames to use per second of video, and the codec to use (see ffmpeg/mencoder). You can change the temporary filename as well, if needed.


COMPOSITE

The secondary function (though at this point the one I use the most) is the composite function, -C, which merges each frame in a given series by lightest pixels. The two methods (-m) I recommend are either lighten or lighten_intensity. See the convert (part of ImageMagick) man page for more. 


ANIMATION

The anim function, -A, only makes sense when creating a composite since it is, in fact, a movie of the composite creation process.  It takes the same options as the timelapse function, though making a timelapse is not a requisite. 


The following tools are required:
Imagemagick   http://www.imagemagick.org/
mencoder (MPlayer)  http://en.wikipedia.org/wiki/MEncoder
exiftool  https://www.sno.phy.queensu.ca/~phil/exiftool/


