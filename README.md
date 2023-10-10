# Irodori-Comics-ripper

## Ripping doujinshi from Irodori Comics

If you have purchased a doujinshi from the Irodori Comics store, you need to extract the images from the PDF. This can be done by using pdfimages, which is available in the poppler-utils package. Unfortunately, this package is only available on Linux.

<u> Windows users can just install Ubuntu by using the Windows Subsystem for Linux (WSL). </u>

To keep the guide concise, a bash script is available to help streamline the process (written by none other than myself, with the assistance of several anonymous contributors): rip.sh. The script will automatically extract, optimize, and package the images for you.

To use the script, place the PDFs and pingo alongside the script, and install the prerequisites:
``` sudo apt-get install poppler-utils zip ```

Then, simply execute the command ```bash rip.sh```.

## Extra: Restoring modTime attribute

    1. Retrieve the most recent value of the Last-Modified header.
    2. Apply it using the command ```touch -a -m -d "Wed, 03 May 2023 00:00:00 +0000" target_file```.

*Replace ```Wed, 03 May 2023``` with the date obtained from the DevTools.
Do this on the PDF before executing the script.

[mtime.webm](https://github.com/WebForks/Irodori-Comics-ripper/assets/35718739/d388c1c4-95fe-4235-929a-818b03b1d48b)
