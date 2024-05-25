---
layout: post
read_time: true
show_date: true
title: Audio Distortion Circuit
date: 2099-04-07 05:50:00 -0500
description: Design of a distortion pedal
img: posts/20240407/guitar-pedal1595862_1280.jpg
tags: [audio, pcb, kicad, opamp]
author: Rafael Reyes
github: rafa-2112/BH-distortion-pedal/
mathjax: yes
---

Audio effects are prevalent in music and range in purpose. While some are subtle and designed to clean-up signals, others add their own variations. One such effect is distortion.

## What is distortion?
Distortion is an alteration that produces a "gritty" tone. It is typically achieved by increasing the gain of the audio signal until the peaks surpass the point of saturation or by diode clipping. The video below demonstrates the how distortion affects a clean audio signal.

<center>
    <iframe width="75%" height="315" src="https://www.youtube.com/embed/7dLArMd-y64?si=eqY3fxMvaLuB1e9L" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</center>

## Design



<center><img src='./assets/img/posts/20240407/opamp-clipping-stage.png'  width="250"><font size="2">Op-Amp Clipping Stage</font></center>

<p style="text-align:center">\(<br>
\begin{align}
\ A_v = 1 + \frac{\text{R}_{17}}{\text{R}_{V1}} 
\Rightarrow 1 + \frac{510k}{500k + 1.2k} \approx 2
\end{align}
\)</p>

<p style="text-align:center">\(<br>
\begin{align}
\ A_v = 1 + \frac{\text{R}_{17}}{\text{R}_{V1}} 
\Rightarrow 1 + \frac{510k}{1.2k} = 426
\end{align}
\)</p>

<p style="text-align:center">\(<br>
\begin{align}
f_L = \frac{1}{2 \pi \text{RC}} \Rightarrow
\frac{1}{2 \pi (510k) (100p\text{F})} \approx 3120 \space \text{Hz} 
\end{align}
\)</p>

<p style="text-align:center">\(<br>
\begin{align}
f_H = \frac{1}{2 \pi \text{RC}} \Rightarrow
\frac{1}{2 \pi (500k + 1.2k) (47n\text{F})} \approx 7 \space \text{Hz} 
\end{align}
\)</p>

<p style="text-align:center">\(<br>
\begin{align}
f_H = \frac{1}{2 \pi \text{RC}} \Rightarrow
\frac{1}{2 \pi (1.2k) (47n\text{F})} \approx 2822 \space \text{Hz} 
\end{align}
\)</p>

<center><img src='./assets/img/posts/20240407/opamp-clipping-stage.png'  width="250"><font size="2">Op-Amp Clipping Stage</font></center>

## <center>UPDATES COMING SOON</center>