Note: `rename.ul` is for Debian, Fedora uses `rename` instead

# Export PNGs

for f in *.svg ; do rsvg-convert -f png -x 2 -y 2  $f -o $f.png ; done && rename.ul .svg.png .png * && mv *.png ../png

# Export PDFs

for f in *.svg ; do rsvg-convert -f pdf -x 2 -y 2  $f -o $f.pdf ; done && rename.ul .svg.pdf .pdf * && mv *.pdf ../pdf

