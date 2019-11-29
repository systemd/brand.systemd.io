![Systemd Logo](assets/page-logo.png)

# brand.systemd.io

Website with systemd brand assets

## Update assets

If you change the SVG assets, you need to re-render the assets in the PNG and PDF folders to keep them in sync.

*Note: The commands below work on Fedora, but on Debian-based systems you have to replace `rename` with `rename.ul`.*

Navigate to the SVG folder:
```
cd assets/svg
```

Render the PNGs:
```
for f in *.svg ; do rsvg-convert -f png -x 2 -y 2  $f -o $f.png ; done && rename .svg.png .png * && mv *.png ../png
```

Render the PDFs:
```
for f in *.svg ; do rsvg-convert -f pdf -x 2 -y 2  $f -o $f.pdf ; done && rename .svg.pdf .pdf * && mv *.pdf ../pdf
```
