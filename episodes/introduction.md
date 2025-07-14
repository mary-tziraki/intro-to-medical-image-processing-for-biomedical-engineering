---
title: "2d image basics"
teaching: 40
exercises: 20
---

:::::::::::::::::::::::::::::::::::::: questions 

- What is a 2D image?
- What parameters would describe a 2D image?
- How to view an image?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- describe different 2d image formats
- explain size, dimensions, and compressions and their significance
- opening and visualizing examples from the 2d imaging general dataset
- identify/extract the data type, size, dimensions, and compression type from an image

::::::::::::::::::::::::::::::::::::::::::::::::

## Introduction 

This is imported from Carpenries 

This is a lesson created via The Carpentries Workbench. It is written in
[Pandoc-flavored Markdown](https://pandoc.org/MANUAL.html) for static files and
[R Markdown][r-markdown] for dynamic files that can render code into output. 
Please refer to the [Introduction to The Carpentries 
Workbench](https://carpentries.github.io/sandpaper-docs/) for full documentation.

What you need to know is that there are three sections required for a valid
Carpentries lesson:

 1. `questions` are displayed at the beginning of the episode to prime the
    learner for the content.
 2. `objectives` are the learning objectives for an episode displayed with
    the questions.
 3. `keypoints` are displayed at the end of the episode to reinforce the
    objectives.

:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::: instructor

Inline instructor notes can help inform instructors of timing challenges
associated with the lessons. They appear in the "Instructor View"
::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

# Introduction of the episode 01

Digital images are part of modern life. With digital cameras and mobile phones, people generate and receive thousands of images every year in their pockets and computers. In addition, telescopes, medical imaging modalities and sophisticated cameras in research are designed to capture, store and digitally propagate copies of the original subject image indefinitely without losing image quality. High-quality images are crucial for medical diagnostics, imaging the universe and the microcosmos and solving numerous research problems.

 In all forms of digital imaging, information about the object are collected by sensors and then converted into numbers that represent a measurement of a specific property. This measurements could be based on many different properties, including visual light (digital photography), X-ray attenuation (digital radiography, fluoroscopy, and CT), gamma rays emission from injected radioactive materials (digital scintigraphy, SPECT, and PET), transmissions of sound (ultrasonography).
 
The term digital imaging also implies processing, compression storage, printing and display of such images. 
2-dimensional (2D) images are stored in computer memories in 2-dimensional rectangular arrays (like a matrix) of hundreds, thousands or millions of discrete 'picture elements' called pixels. Each pixel holds a number or multiple numbers representing the pixel's intensity or colour. The pixel arrays could be manipulated with mathematics and algorithms to give high-quality image outputs or valuable information for analysis, and this is called image processing. As computer systems have become faster and more powerful, Image processing is part of extensive image analysis and a growing area of research. Some well-known 2D digital imaging formats are BMP, PNG, TIFF and JPEG.


Image can also be described that represent measurements throughout a three-dimensional volume. These 3-D images are most often seen in medical imaging. Medical Images (MRI, CT, PET) are often stored at acquisition using a format described by an industry standard known as Digital Imaging in Communications and Medicine (DICOM). 


Considering the large volumes of data that can be involved and the time-consuming and error-prone nature of manual processing, it can be advantageous, or even necessary, to automate the image processing and analysis steps using a computer program. While there are a number of widely available free imaging packages available, there will be times when they may be limiting to what you are trying to achieve, and thus you may need to write some bespoke code to meet your research objectives. This series of episodes aims to give you an initial understanding of how to analyze and process imaging data using Python scripts. For the purpose of these lessons, we will focus on imaging analysis involving high-resolution structural MR images of the brain.

In this notebook, we will learn the basic information that a 2D image contains. It introduces an open-source toolkit for processing image data: the Python programming language and the scikit-image (skimage) library. With careful experimental design, Python code can be a powerful instrument in answering many different questions.

::::::::::::::::::::::::::::::::::::: challenge 

## Challenge 1: Can you do it?

What is the output of this command?

```r
paste("This", "new", "lesson", "looks", "good")
```

:::::::::::::::::::::::: solution 

## Output
 
```output
[1] "This new lesson looks good"
```

:::::::::::::::::::::::::::::::::


## Challenge 2: how do you nest solutions within challenge blocks?

:::::::::::::::::::::::: solution 

You can add a line with at least three colons and a `solution` tag.

:::::::::::::::::::::::::::::::::
::::::::::::::::::::::::::::::::::::::::::::::::

## Figures

You can use standard markdown for static figures with the following syntax:

`![optional caption that appears below the figure](figure url){alt='alt text for
accessibility purposes'}`

![You belong in The Carpentries!](https://raw.githubusercontent.com/carpentries/logo/master/Badge_Carpentries.svg){alt='Blue Carpentries hex person logo with no text.'}

::::::::::::::::::::::::::::::::::::: callout

Callout sections can highlight information.

They are sometimes used to emphasise particularly important points
but are also used in some lessons to present "asides": 
content that is not central to the narrative of the lesson,
e.g. by providing the answer to a commonly-asked question.

::::::::::::::::::::::::::::::::::::::::::::::::


## Math

One of our episodes contains $\LaTeX$ equations when describing how to create
dynamic reports with {knitr}, so we now use mathjax to describe this:

`$\alpha = \dfrac{1}{(1 - \beta)^2}$` becomes: $\alpha = \dfrac{1}{(1 - \beta)^2}$

Cool, right?

::::::::::::::::::::::::::::::::::::: keypoints 

- 2D images are matrices 

::::::::::::::::::::::::::::::::::::::::::::::::

[r-markdown]: https://rmarkdown.rstudio.com/
