---
title: 'DailyWildfireCAN: A Dataset and Benchmark for Next-Day Wildfire Spread Prediction in Canada'
layout: default
---

<p class="teaser">
<video width="85%" autoplay loop muted playsinline controls poster="assets/dailywildfirecan_explainer.gif">
  <source src="assets/dailywildfirecan_explainer.mp4" type="video/mp4">
  <img src="assets/dailywildfirecan_explainer.gif" width="100%" alt="DailyWildfireCAN explainer animation"/>
</video>
</p>

<p class="caption" style="width:85%; margin:0 auto 10px; text-align:justify;">
<b>DailyWildfireCAN Dataset and Benchmark.</b><br>
<b>(a) Geographic coverage.</b> Locations of the 2,440 wildfires (2017–2024), with marker size indicating total burned area. Bars show the number of fires per year. The inset shows one data sample with its burned area within a 23.04 × 23.04 km tile at 90-m resolution.<br>
<b>(b) Input features.</b> The 33 input features for the example tile, grouped by data source. Each group indicates the number of features, source dataset, native spatial resolution and temporal frequency.<br>
<b>(c) Daily Fire Progression.</b> Evolution of an example fire from 16 to 18 July 2024. Dark grey indicates previously burned areas, while orange indicates newly burned areas on each day. The newly burned area on day <i>T</i>+1 constitutes the prediction target.<br>
<b>(d) Benchmark.</b> Input features available up to day <i>T</i> are used to predict the newly burned area on day <i>T</i>+1. Predictions are evaluated against the observed target using precision, recall and area under the precision–recall curve (AUC-PR).
</p>

<p class="teaser"> <img src="assets/DailyWildfireCAN_overview.png" width="85%" alt="Overview of the CanadaWildFireDaily dataset"/>
</p>

## Abstract

<p class="abstract">
<b>DailyWildfireCAN</b> is a comprehensive dataset and benchmark for next-day wildfire spread prediction across Canada. It combines high-resolution fire progression data with environmental and satellite observations to support the development and evaluation of AI models for wildfire forecasting.
</p>

<p><b>Key Highlights:</b></p>

<ul>
<li><b>Nationwide coverage:</b> 2,440 wildfire events across eight fire seasons (2017–2024).</li>
<li><b>High resolution:</b> Daily fire progression at 90 m spatial and 24-hour temporal resolution.</li>
<li><b>Multi-modal data:</b> 33 features covering weather, terrain, vegetation, forest structure, human influence, and satellite imagery.</li>
<li><b>Two dataset formats:</b> Mono-temporal and multi-temporal inputs for predicting next-day wildfire spread as a pixel-wise segmentation task.</li>
<li><b>Comprehensive benchmark:</b> Diverse AI models evaluated using standardized data splits, baselines, and protocols.</li>
<li><b>Robustness analysis:</b> Evaluation across fire characteristics, geographic regions, temporal conditions, spatial tolerances, and label uncertainty.</li>
<li><b>Open research resources:</b> Publicly available raw and processed datasets, benchmark implementations, trained checkpoints, and evaluation code.</li>
</ul>

## Dataset and Benchmark

- **Dataset:** raw per-fire data and prepared mono-temporal and multi-temporal ML datasets on [Hugging Face](https://huggingface.co/datasets/DailyWildfireCAN/DailyWildfireCAN).
- **Benchmark:** benchmark models and trained checkpoints on [Hugging Face](https://huggingface.co/DailyWildfireCAN/DailyWildfireCAN-Benchmark).
- **Code:** code for building the dataset, training the benchmark models, and evaluation on [GitHub](https://github.com/milatechtransfer/DailyWildfireCAN).

## Authors

<div class="authors" id="authors">
{%- for person in site.data.authors limit: 2 -%}
<div class="person">
  {%- if person.image and person.image != "" -%}
  <span class="avatar avatar--{{ person.name | slugify }}"><img src="{{ person.image }}" alt="{{ person.name }}"/></span>
  {%- else -%}
  <span class="avatar-fallback">{{ person.name | slice: 0 }}</span>
  {%- endif -%}
  {%- if person.url and person.url != "" -%}
  <a href="{{ person.url | relative_url }}">{{ person.name }}</a>
  {%- else -%}
  <span>{{ person.name }}</span>
  {%- endif -%}
  <span>{{ person.title | replace: '&', '<br>' }}</span>
</div>
{%- endfor -%}
</div>

<div class="authors" id="authors-more">
{%- for person in site.data.authors offset: 2 -%}
<div class="person">
  {%- if person.image and person.image != "" -%}
  <span class="avatar avatar--{{ person.name | slugify }}"><img src="{{ person.image }}" alt="{{ person.name }}"/></span>
  {%- else -%}
  <span class="avatar-fallback">{{ person.name | slice: 0 }}</span>
  {%- endif -%}
  {%- if person.url and person.url != "" -%}
  <a href="{{ person.url | relative_url }}">{{ person.name }}</a>
  {%- else -%}
  <span>{{ person.name }}</span>
  {%- endif -%}
  <span>{{ person.title | replace: '&', '<br>' }}</span>
</div>
{%- endfor -%}
</div>

<p>
For inquiries, please contact us at:
<a href="mailto:mahacine.ettahri@etud.polymtl.ca">mahacine.ettahri@etud.polymtl.ca</a> (Mahacine Ettahri) or
<a href="mailto:hager.radi@mila.quebec">hager.radi@mila.quebec</a> (Hager Radi)
</p>

## Citation

Please cite our preprint:

<div class="citation-block">
@article{dailywildfirecan,
  title={DailyWildfireCAN: A Dataset and Benchmark for Next-Day Wildfire Spread Prediction in Canada},
  author={Ettahri, Mahacine and Abdelwahed, Hager Radi and Olutayo, Toluwaleke and Aloise, Daniel and Caron, Ga{\'e}tan Marceau},
  journal={arXiv preprint arXiv:2611.14207},
  year={2026}
}
</div>


<p style="text-align:center; margin-top:2rem;"><i>Developed at Mila: Quebec AI Institute, The Applied Research Team</i></p>

<p style="text-align:center; margin-top:1rem;">
  <a href="https://mila.quebec"><img src="{{ '/assets/mila_logo.svg' | relative_url }}" alt="Mila - Quebec AI Institute" style="height:50px;"></a>
</p>
