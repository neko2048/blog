---
title: Documentation of Cloud Tracking Algorithm
date: 2022-09-30 00:00:00 +0800
categories: [Atmosphere]
tags: [atmosphere, crm, cloudtracking, algorithm]
# TAG names should always be lowercase
---
# Introduction
The cloud tracking algorithm presented here builds upon the Iterative Rain Cell Tracking (IRT) algorithm developed by Moseley and Haeter in 2020. We have expanded this approach from tracking 2-dimensional rain cells to capturing 3-dimensional cloud objects in the cloud resolving model.

This algorithm is designed to track the liquid water path instead of rain cells, projecting the identified entities onto the 3-dimensional cloud objects. For the sake of simplicity and ease of operation, when addressing the merging and splitting of cloud objects during their time evolution, we treat them as the same identity. (Refer to the detailed process outlined below.)
![Algorithm](/assets/img/2022-09-30-algorithmProcess.png)

## Quick View:
* Source Code: <https://github.com/neko2048/iterativeRainCellTracking>
* [Iterative rain cell tracking](#iterative-rain-cell-tracking)
    * Parameter Setup
    * Transfer 2D Track Variable
    * Main Program
    * Merge all parent & children track ID to same track ID
    * Project track ID to LWP regions
* [Cloud Water Object Recognition & Filtering](#cloud-water-object-recognition--filtering)
    * Cloud Object Recognition 
    * Cloud Object Filtering
    * Qc Object Recognition
    * Qc In Same Cloud Identification
* [Qc Co-location](#qc-co-location)
    * Collocate Qc Objects 
    * Merge Multiple LWP if they overlaps with one Qc 
* [Map Qc to Cloud](#map-qc-to-cloud)
    * Map Qc to Cloud 

## Iterative rain cell tracking

## Cloud Water Object Recognition & Filtering

## Qc Co-location

## Map Qc to Cloud