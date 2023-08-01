---
layout: page
title: Hydrologic Prediction in Ungauged Basins
description: How do we predict model parameters when there is lack of observed data for model calibration? I tried to tackle this question during my master's thesis.
img: assets/img/prev.png
importance: 1
category: work
related_publications: karki2023comparative
---
# Hydrologic Prediction in Ungauged Basins

We extracted different catchment properties for 23 basins across Nepal and used 4 different regionalization methods to predict the parameters for a hydrologic model.
<div class="row justify-content-sm-center">
    {% include figure.html path="assets/img/abstract.pdf" title="example image" class="img-fluid rounded z-depth-1" width=600%}
</div>

The model showed good performance when the observed data was made available for model calibration (on-site).
<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/onsite.png" title="example image" class="img-fluid rounded z-depth-1" width=600 %}
</div>

While there was no single regionalization method that could perform well in all the basins, the physical similarity based method was found to be the most robust among others in simulating daily hydrographs. The regression-based methods generally performed poorer than the donor-based methods.

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/reg_summary.png" title="example image" class="img-fluid rounded z-depth-1"%}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/heatmap.png" title="example image" class="img-fluid rounded z-depth-1"%}
    </div>
</div>
Boxplot showing performance of regionalization methods (left) and heatmap for model performance in all the selected basins (right).

Similar results were also found in reproducibility of flow duration curves. Notice the overprediction of low flows (exceedance>0.75) in panel a? This could be due to NSE metric used for model calibration whose squared-error formulation prioritizes the high-flows. 

<div class="row justify-content-sm-center">
    {% include figure.html path="assets/img/edc.png" title="example image" class="img-fluid rounded z-depth-1" width=600 %}
</div>

Next, we used multiple donors instead of a single donor and tested two different averaging methods: output-averaging and parameter-averaging. We found that output-averaging increases the overall efficiency of the donor-based methods while parameter-averaging showed a rather declining effect. 
<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/multiple.png" title="example image" class="img-fluid rounded z-depth-1" width=600 %}
</div>

Finally, we looked at whether there were actually other basins that could yield better results than that chosen by the donor-based methods, and looks like there were - many; leaving us with questions like: Why did they perfom better than other basins? In what ways, are they similar? Can we infer basin-similarity using model results instead and then trace back the attributes similarity?
<div class="row justify-content-sm-center">
{% include figure.html path="assets/img/best.png" title="example image" class="img-fluid rounded z-depth-1" width=600 %}
</div>
