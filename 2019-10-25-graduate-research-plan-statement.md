---
title: Graduate Research Plan Statement
subtitle: "Metadata for Images of Meteorological Logbooks circa 1860--1960"
author: Colton Grainger
nonumbering: true
xy: true
fontsize: 12pt
geometry: margin=1in
blockquote: true
links-as-notes: true
bibliography: /home/colton/coltongrainger.bib

---

I propose to continue work on the classification and reduction of meteorological data from binary image files (e.g., digital scans of US Naval documents) using methods in statistics, applied topology, and the digital humanities.

As a student visitor at the National Center for Atmospheric Research (NCAR), I am currently extending my project^[Source code: <https://github.com/NCAR/rda-image-archive>.] as a summer intern to design a metadata schema for a $100$ TB collection of scanned documents in order to reduce each $6$ MB image in a document to a $2$ KB time series of observed data for the International Comprehensive Ocean-Atmosphere Data Set (ICOADS).

My immediate goals are

- to gather images into one repository and associate each image to a persistent identifier,
- to establish a common description framework for the image metadata, and
- to provide bulk, programmatic access to image subsets

I am committed to accomplishing these three tasks in the next year, but would rely on a fellowship in order to extend this project for the duration of my graduate career.

My goals for an extended project would be

- to elicit increasingly refined classifications of subsets of images from a document,
- to exploit spatio-temporal metadata from documents to infer the position over time of platforms (e.g., ships and land stations) responsible for meteorological observations, and
- to develop a Bayesian framework for iteratively reducing the uncertainty associated to metadata of unclassified images that are known to be in sequence with classified images.

## Intellectual Merit

### Which images are to be collected and classified?

To fix ideas:

Ship logbooks and land station records circa 1860--1960. Roughly 50 TB of images have been produced by Kevin Wood (University of Washington) from logbooks US Naval and logbooks, while roughly another 50 TB of images have been produced by Philip Brohan (UK Met Office) from UK Royal Navy
and the Indian .

### What is the need for classifying meteorological documents?

### What methods in computational and data-enabled science will be extended?

\newpage

## Broader Impacts

This project aims to persistently link images of meteorological documents (out of which observational data is to be reduced) to specific entries in ICOADS. These persistent identifiers would support inquiry and investigation of the validity of observational data used for climate modelling.

The first portion of this project seeks immediately to establish an open-access repository and a RESTful API for the 100 TB image collection. The API would allow any researcher to *query* images based on geospatial metadata, *retrieve* a subset of images corresponding to their query, and to *post back* refined metadata from their own image classification efforts.

The proposed software is to be released with an MIT open source license. Researchers could build their own image database to begin reducing image metadata. Moreover, researchers could mint persistent identifiers for images compatible with NCAR's repository, in order to transfer images and image metadata between repositories.

The proposed software design is functional and agnostic to the initial choice of metadata schema. It could support collaborative image classification tasks, say, for the medical case management of individuals with limited english proficiency (LEP). In particular, during my 2016 internship at the YMCA International Services,^[A refugee resettlement and  social service agency of ~50 staff directed by the YMCA of Greater Houston.] medical case management was bottlenecked by the need for case managers to parse overwrought English language medical documents that contained only $\%10$ client specific information. The proposed software could aid case managers by enabling remote classification of relevant sections of documents that LEP clients should seek to *translate carefully*.
<!--
I propose to continue work on the classification and reduction of meteorological data from binary image files (e.g., ship log books) using methods in statistics/machine learning, applied topology, and the digital humanities.

As a student visitor at the National Center for Atmospheric Research (NCAR), I am extending my project as a summer intern to classify images of handwritten meteorological logbooks from ocean and land platforms (ships and weather stations) in order to harvest meteorological data from them for the International Comprehensive Ocean-Atmosphere Data Set (ICOADS). My immediate goals are 

1. to gather images into (at least) one repository and associate each image to a persistent identifier,
2. to establish a common description framework for the image metadata, and
3. to provide bulk, programmatic access to image subsets.

I am committed to accomplishing these three tasks in the next year, but would necessarily rely on a fellowship to extend this project for the duration of my graduate career. My goals for an extended project would be 

1. to develop a framework for eliciting most useful classifications of individual images in a time-series,
2. to generalize the current geospatial metadata schema in the language of applied category theory, and
3. to study and reduce the statistical uncertainty associated to each image's geospatial metadata.

## Intellectual Merit

### Which images will be classified?

The archetypical image of a meteorological logbook contains 24 hours of weather observations (barometric pressure, sea-surface temperature, etc.) from an ocean-faring platform circa 1860 to 1960. The mathematical problem is to reduce each 6Mb image to a 2Kb time series of weather observations. To this end, I have develop a sophisticated metadata schema for images consisting of 5 categories

1. (`arc`) the archive of origin, 
2. (`doc`) the source document, 
3. (`img`) the binary image file itself, 
4. (`obs`) the meteorological observations available from the image, 
5. (`plt`) the platform responsible for producing the observations,

with functional dependencies given by the following diagram

$$
\xymatrix{
\text{arc} \ar@{->>}[dr] &  & \ar@{->>}@/^5px/[dl] \text{plt} \\
& \text{doc} \ar@{.>}@/^5px/[ur]^{\exists!} \ar@{->>}[dl] & \\
\text{img} \ar@{->>}[rr] & & \text{obs} \ar@{_{(}->}[uu]_{\text{update}}}
$$

Roughly, an image in the category $\text{img}$ approximates a time-series $\sigma \colon [t_0, t_1] \to \mathscr{S}$, where $\mathscr{S}$ is the state space of meteorological variables. An observation is $\sigma(t)$ evaluated at a time $t$. A platform in the category $\text{plt}$ approximates a time-series $\lambda \colon [t_0, t_1] \to M$, where $M$ is the Earth's surface (as a manifold). An image is successfully classified if both $\sigma$ and $\lambda$ are determined up to some statistical uncertainty. 
-->
