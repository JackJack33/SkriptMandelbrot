# SkriptMandelbrot
minecraft mandelbrot script for Skript

copy the text and put it in a .sk file under `plugins/skript/scripts`
save & reload

the set generates at y=3, so make sure to have an adequately sized clearing
or just a flat world

make sure you have effect commands enabled, else you will have
to link the function to a command or event

also make sure that you have increased decimal precision to at least
4 places in the skript config.yml. you can go over 4 but performance
decreases as you increase the decimal places

# How to use:

`genMandelbrot(i, s, zo=0, px=0, pz=0, of="")`

`i` - Iterations per block (21 is a good number if you're not editing anything)

`s` - Size (centered on the world's origin)

`zo` - Zoom

`px` - Offset x (real numbers)

`pz` - Offset z (complex numbers)

`of` - Offset Z (starting value in the function, leave this alone if you want the mandelbrot set)

# Examples

If you leave the zoom blank, you will end up with a very small visualization (~4x4 blocks)

`genMandelbrot(21, 10)`

With a semi-decent processor and 1GB RAM, it takes about a minute for a size 200, zoom 50 set to generate

`genMandelbrot(21, 200, 50)`

Heres my personal favorite area

`genMandelbrot(21, 100, 1600, -0.640, -0.480)`

Sunglasses

`genMandelbrot(21, 50, 10, 1, 0, "0+1i")`
