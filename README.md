# Radio Shack TRS-80 FP-215 Flatbed Plotter Archive

## Introduction
I found an FP-215 plotter at a yard sale years ago, and I had many 
ideas about what I could do with it.  Like many ideas of my ideas, it never 
got further than a couple of "hello world" types of tests.  After moving a 
couple of times, I finally gave the plotter away for free to a random person on 
the internet.  I hope it got used for an interesting project.

This is all the information I found about the plotter, and it seems a lot 
of these resources are now gone.   Hopefully, these resources will be 
helpful to somebody else.   Do not hesitate to drop me a line to let 
me know what you're using the plotter for!  Who knows, maybe I'll even 
list your project here.

## Archived Information
The following information was mirrored from the following URL which no longer exists.  
`http://www.geocities.com/maboytim/fp215/ `

>  The native plotting language of the FP-215 is quite simple - I call it RSGL
(Radio Shack Graphics Language for lack of a better term). The best way to
control the FP-215 is to use a utility (filter) to convert from some well
supported graphics language, such as HPGL, to RSGL.
>
> As mentioned, RSGL is pretty simple - the only necessary commands are Move (move
with pen up) and Draw (move with pen down).
>
> I don't know much about HPGL but I'm sure it's more complicated and capable than
RSGL - but ultimately, the plotter's job is to draw on the paper so any plotter
command stream can in principle be converted to a sequence of Move and Draw
commands. In addition, there's nothing that says an application or driver has to
use the full capability of HPGL and if the application or driver uses only (the
equivalent of) moves and draws the conversion from HPGL to RSGL can be trivial.
In fact, the AutoCAD HP7550A plotter driver seems to use only Moves and Draws
(AutoCAD is essentially the only application I use with the FP-215 although
others are possible - Windows for example has an HP7550A print driver although I
don't know how restrictive a subset of HPGL it uses).
>
> HPGL uses PenUp (PU), PenDown (PD), and PenAt (PA) commands - a Move is a PenAt
with the pen up, a Draw is a PenAt with the pen down.

## Directories

### `rsplot/`

RSplot is a conversion utility written in C. It supports only the PU, PD. PA, and
SP (SelectPen) commands. Multiple pens are supported by generating an output
file per pen - this allows the FP-215's pen to be manually changed between
colors. RSplot can be easily extended to include additional HPGL commands as
needed but these four simple commands are sufficient to convert AutoCAD HPGL
plot files.

RSplot was written for DOS and compiled using PowerC. It should be easy to port
to other environments.

### `rsgl/`

drawRSGL is a small Gtk-Perl script for Linux derived from drawHPGL (an HPGL
previewer by Henry Palonen).

### `rsglsmpl/`

Sample RSGL plots.

### `hpglsmpl/`

Sample HPGL plots.

### `fp-215-manual-img/`

The original fp-215 manual, scanned to .gif and .jpg files.

### `info-from-radioshack/`

Mirrored information about the fp-215 from radioshack.com


