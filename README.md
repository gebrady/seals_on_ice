# Seals On Ice: Mapping ice habitat for harbor seals in tidewater glacier fjords
## Quantifying ice change in Kenai Fjords National Park through monthly acquisitions using fixed wing aircraft and aerial photos.

#### _National Park Service, Alaska Regional Office, Scientist in Parks Program_

This repository contains our Jupyter Notebook workflow for mapping harbor seal habitat from aerial imagery. By using a shareable, annotatable format like a Jupyter Notebook, the steps in our remote sensing/GIS processing can be better understood and modified for similar projects by other researchers.

![Seals on Ice](field_photos/DSC_0566-3.jpg)


Graham Brady
Chad Hults, Deb Kurtz

## Abstract

Glaciers in Alaska are melting rapidly, changing environmental conditions and necessitating
a higher frequency of monitoring to maintain an understanding of current conditions for
informed natural resource management. We developed an image classification workflow that
processes large amounts of monitoring data to map harbor seal habitat (icebergs) from imagery
using ArcGIS segmentation tools. Icebergs are used as habitat by seals in Alaska fjords.
Using normalized difference indices and pixel brightness characteristics, we implemented an
automated object-based segmentation method that allows scientists to efficiently process
large quantities of remotely collected image data to map changing seal habitat. In 2023,
we conducted aerial photo surveys in Kenai Fjords National Park using a belly-mounted
camera in a fixed-wing aircraft, producing thematic maps of ice cover via ArcGIS Pro and
Jupyter Notebook. This approach is adaptable for generating ice estimates across multiple
acquisitions, making it applicable to broader conservation projects. Results of our classification
show the effectiveness of using normalized band indices to accentuate differences in ice/
water and pixel brightness to refine preliminary outputs. The notebook demonstrates how
programmatic implementation can leverage geoprocessing tools, inline annotations, and
scripting to simplify data management, test classification methods, and strengthen science
communication. Furthermore, our seal habitat monitoring goal fits within the larger scope
of ice cover assessment in the Arctic, an important element of risk assessment and land
management for varying uses from competing stakeholders. With continued developments
of automated mapping methods for fixed-wing and UAV systems, traditional environmental
monitoring protocols can be replaced with robust, scalable techniques to support adaptive
natural resource management in the era of climate change.

## Thematic Mapping of Icebergs

Several methods of image classification and GIS processing were attempted before developing a finalized workflow. While individual images could be robustly mapped using a particular approach, few of these approaches were successful for multiple fjords or months of acquisitions. However, leveraging the positive aspects of prior attempts proved helpful for develping a solution that worked for many acquisitions. Because of changing lighting conditions, variability in ice density, and differences in surface water appearance, it was necessary to develop a workflow that produces accurate thematic maps to compare available ice area with minimal alteration or input from an analyst beyond project setup.

The Jupyter Notebook format incorporates blocks of codes and annotations to document processing, show results, and provide a way to share workflows wither others. While developing the image classification workflow for this project, stages were written in Python code format and the final version is included below.

Most of the geoprocessing for this workflow utilizes ESRI's ArcPy library of classes and methods, which blend standard python techniques and syntax with a simple set of tools that resemble the organization of ArcMap and ArcGIS Pro geoprocessing tools. With an understanding of the way these tools work and some creativity, the Jupyter Notebook is an optimal environment through which to develop and improve an analytical workflow, particularly in a repetitive way. With the ability to quickly cycle through parameters we were able to determine the optimal settings and combinations of variables with which to produce the best result across acquisitions

