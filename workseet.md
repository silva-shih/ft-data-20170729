# Slides

[Morning]()

[Afternoon]()

# Workshop 

## How to create gif? 

1. Download [the package](https://share.weiyun.com/4e6e4205774add9bdea33c0e4378d0e5) and save it to you desktop. 

2. Then install [homebrew](https://brew.sh/).

    You could paste the flowing line at a Terminal prompt.
    
        /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

3. Install [ImageMagick](https://www.imagemagick.org/script/index.php).

    You can use command line to install : `brew install ImageMagick`, or install the package directly from [this link](https://www.imagemagick.org/script/download.php).
    

4. Usage:
    
    
        convert *.png gif-layers.gif


## Coverter (without too much code)

1. Image to txt. 

    * **Tesseract OCR**
  
        brew install tesseract --all-languages

        Or install without `--all-languages` and [install them manually as needed](http://blog.philippklaus.de/2011/01/chinese-ocr/).

        It's better the input image is a grayscale `.tif` and fairly large. ~2000*500 works very well.

            convert ocr.png -resize 400% -type Grayscale ocr.tif

        OCR it. The default language is English. Language codes are 3 chars per `man tesseract`.

            tesseract -l eng input.tif output

        This creates `output.txt`.


    * **Or you can simply use [Tesseract's online converter](Tesseract)**.

2. Pdf to txt. 

    * google drive
    
    * [tabula](http://tabula.technology/)
    
    * [pdfconverter](https://pdftables.com/)

3. Other data converter: 

    * [Mr. data converter](http://shancarter.github.io/mr-data-converter/)


