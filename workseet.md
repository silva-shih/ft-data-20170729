# Slides

[Morning](https://silva-shih.github.io/201707-ft-data/)

[Afternoon](https://silva-shih.github.io/201707-ft-data-2)

# Workshop 

## How to create gif? (using Terminal) 

1. Download this [demo package](https://share.weiyun.com/245e19184240fec73d5b7f056359b4ab) and save it to you _desktop_. 

2. Then install [homebrew](https://brew.sh/). You could paste the flowing line at a Terminal prompt.
    
        /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

3. Install [ImageMagick](https://www.imagemagick.org/script/index.php). You can use command line to install : `brew install ImageMagick`, or install the package directly from [this link](https://www.imagemagick.org/script/download.php).
    
4. Usage:

    This combines every .png file and creates `gif-layers.gif`.

        convert *.png gif-layers.gif
    
    This slows down the gif.

        convert *.png -set delay 50 gif-layers-slow.gif
        
     This resizes the gif. (Usage of [`-resize`](http://www.imagemagick.org/Usage/resize/))

        convert *.png -resize 50x50 resize.gif
        
                
        

## Coverter (without too much code)

1. Image to txt. 

    * **Tesseract OCR**
  
        `brew install tesseract --all-languages`

        Or install without `--all-languages` and [install them manually as needed](http://blog.philippklaus.de/2011/01/chinese-ocr/).

        It's better the input image is a grayscale `.tif` and fairly large. ~2000*500 works very well.

            convert ocr.jpg -resize 400% -type Grayscale ocr.tif

        OCR it. The default language is English. Language codes are 3 chars per `man tesseract`.

            tesseract -l eng input.tif output

        This creates `output.txt`.


    * **Or you can simply use [Tesseract's online converter](http://tesseract.projectnaptha.com/)**.

2. Pdf to txt. 

    * [google drive](https://www.google.com/drive/)
    * [tabula](http://tabula.technology/)
    * [pdfconverter](https://pdftables.com/)

3. Other data converter: 

    * [Mr. data converter](http://shancarter.github.io/mr-data-converter/)


