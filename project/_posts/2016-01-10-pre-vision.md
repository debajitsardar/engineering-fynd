---
layout: externalpost3
title:  "PRE VISION"
name: pre-vision
date:   2015-01-30 12:00:00
categories: project
description: Build e-commerce apps faster with visual recognition technology 
img: witivision_logo.png
redirect_url: "http://vision-open-api.gofynd.com"


---

<p>

Fynd Pre Vision is a service that makes it easy to automatically tags all your e-commerce specific catalogue images, so you can quickly organize, manage, and search through your content. With pre-vsion, you can detect ecommerce specific product attributes like sleeve length, pattern, neck type, product category and more.

</p>

<p>

Fynd Pre-Vision API enables you to quickly add sophisticated deep learning-based visual search and image classification to your applications. Currently its in beta version so we are allowing free api access to limited number of model's, In comming month we will be sharing full free api access to find content by visual similarity, keyword tag, or a combination of both so you can serve powerful image-based recommendations.

</p>

 

<p>

You can call the Pri-Vision API with the specific model. Simply pass in an image input with a publicly accessible URL or by directly sending image bytes as form data.
</p>
<p>sample cURL request to list all models and their url
</p>

<pre>
curl -X GET http://vision-open-api.gofynd.com/api/open/v1/models-meta/
</pre>

<p>sample cURL request to classify image
</p>

<pre>
curl -X POST

    -H "Content-Type: application/json"

    -d '
    {
    "image_url": "https://goo.gl/RD8BoC",

        "model_name": "sleeve_length_men"

    }'

    http://vision-open-api.gofynd.com/api/open/v1/prediction/

</pre>

