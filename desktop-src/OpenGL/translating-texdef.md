---
title: Übersetzen von texdef
description: Das folgende Codebeispiel ist eine IRIS GL-Textur Definition.
ms.assetid: bb2d257d-ee74-4a65-b364-c7a97bccaa78
keywords:
- IRIS GL portieren, Textur
- Portieren von IRIS GL, Textur
- Portieren auf OpenGL von IRIS GL, Texture
- OpenGL-Portierung von IRIS GL, Textur
- Struktur
- IRIS GL Porting, texdef
- Portieren von IRIS GL, texdef
- Portieren auf OpenGL von IRIS GL, texdef
- OpenGL-Portierung von IRIS GL, texdef
- texdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479af06bcfd3a50daf56fb0629e4c32f24750081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856811"
---
# <a name="translating-texdef"></a><span data-ttu-id="dd2a7-113">Übersetzen von texdef</span><span class="sxs-lookup"><span data-stu-id="dd2a7-113">Translating texdef</span></span>

<span data-ttu-id="dd2a7-114">Das folgende Codebeispiel ist eine IRIS GL-Textur Definition:</span><span class="sxs-lookup"><span data-stu-id="dd2a7-114">The following code example is an IRIS GL texture definition:</span></span>


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



<span data-ttu-id="dd2a7-115">Im vorherigen Beispiel gibt **texdef** den TX \_ -Punkt Filter sowohl als Vergrößerungs-als auch als Minimierungs Mechanismus an \_ .</span><span class="sxs-lookup"><span data-stu-id="dd2a7-115">In the preceding example, **texdef** specifies the TX\_POINT filter as both the magnification and the minimizing filter, and TX\_REPEAT as the wrapping mechanism.</span></span> <span data-ttu-id="dd2a7-116">Außerdem wird das Textur Bild angegeben: **Granit \_ Textur**.</span><span class="sxs-lookup"><span data-stu-id="dd2a7-116">It also specifies the texture image: **granite\_texture**.</span></span>

<span data-ttu-id="dd2a7-117">In OpenGL gibt [**glteximage**](glteximage1d.md) das Image an, und [gltexparameter](gltexparameter-functions.md) legt die-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="dd2a7-117">In OpenGL, [**glTexImage**](glteximage1d.md) specifies the image and [glTexParameter](gltexparameter-functions.md) sets the property.</span></span> <span data-ttu-id="dd2a7-118">Um IRIS GL-Textur Definitionen zu übersetzen, ersetzen Sie die **textdef** -Funktion durch **glteximage** und einen oder mehrere Aufrufe von **gltexparameter**.</span><span class="sxs-lookup"><span data-stu-id="dd2a7-118">To translate IRIS GL texture definitions, replace the **textdef** function with **glTexImage** and one or more calls to **glTexParameter**.</span></span>

<span data-ttu-id="dd2a7-119">Der obige IRIS GL-Code sieht wie folgt aus, wenn er in OpenGL übersetzt wird:</span><span class="sxs-lookup"><span data-stu-id="dd2a7-119">The preceding IRIS GL code looks like this when translated to OpenGL:</span></span>


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



<span data-ttu-id="dd2a7-120">In der folgenden Tabelle sind die Iris GL-Textur Parameter und ihre entsprechenden OpenGL-Parameter aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="dd2a7-120">The following table lists the IRIS GL texture parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="dd2a7-121">IRIS GL-Textur Parameter</span><span class="sxs-lookup"><span data-stu-id="dd2a7-121">IRIS GL texture parameter</span></span> | <span data-ttu-id="dd2a7-122">OpenGL-Textur Parameter</span><span class="sxs-lookup"><span data-stu-id="dd2a7-122">OpenGL texture parameter</span></span>                                  |
|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="dd2a7-123">TX \_ MinFilter</span><span class="sxs-lookup"><span data-stu-id="dd2a7-123">TX\_MINFILTER</span></span>             | <span data-ttu-id="dd2a7-124">GL- \_ Textur- \_ Min- \_ Filter</span><span class="sxs-lookup"><span data-stu-id="dd2a7-124">GL\_TEXTURE\_MIN\_FILTER</span></span>                                  |
| <span data-ttu-id="dd2a7-125">TX- \_ MagFilter</span><span class="sxs-lookup"><span data-stu-id="dd2a7-125">TX\_MAGFILTER</span></span>             | <span data-ttu-id="dd2a7-126">GL- \_ Textur- \_ mag- \_ Filter</span><span class="sxs-lookup"><span data-stu-id="dd2a7-126">GL\_TEXTURE\_MAG\_FILTER</span></span>                                  |
| <span data-ttu-id="dd2a7-127">TX \_ Wrap, TX \_ Wrap \_ S</span><span class="sxs-lookup"><span data-stu-id="dd2a7-127">TX\_WRAP, TX\_WRAP\_S</span></span>     | <span data-ttu-id="dd2a7-128">GL- \_ Textur Umbruch \_ \_ S</span><span class="sxs-lookup"><span data-stu-id="dd2a7-128">GL\_TEXTURE\_WRAP\_S</span></span>                                      |
| <span data-ttu-id="dd2a7-129">TX \_ Wrap, TX \_ Wrap \_ T</span><span class="sxs-lookup"><span data-stu-id="dd2a7-129">TX\_WRAP, TX\_WRAP\_T</span></span>     | <span data-ttu-id="dd2a7-130">Rahmenfarbe für GL- \_ Textur Umbruch \_ \_ TGL- \_ Textur \_ \_ Umbruch</span><span class="sxs-lookup"><span data-stu-id="dd2a7-130">GL\_TEXTURE\_WRAP\_TGL\_TEXTURE\_BORDER\_COLOR</span></span><br/> |



 

<span data-ttu-id="dd2a7-131">In der folgenden Tabelle sind die möglichen Werte der Iris GL-Textur Parameter und ihre entsprechenden OpenGL-Parameter aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="dd2a7-131">The following table lists the possible values of the IRIS GL texture parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="dd2a7-132">IRIS GL-Textur Parameter</span><span class="sxs-lookup"><span data-stu-id="dd2a7-132">IRIS GL texture parameter</span></span> | <span data-ttu-id="dd2a7-133">OpenGL-Textur Parameter</span><span class="sxs-lookup"><span data-stu-id="dd2a7-133">OpenGL texture parameter</span></span>     |
|---------------------------|------------------------------|
| <span data-ttu-id="dd2a7-134">TX- \_ Punkt</span><span class="sxs-lookup"><span data-stu-id="dd2a7-134">TX\_POINT</span></span>                 | <span data-ttu-id="dd2a7-135">GL am \_ nächsten</span><span class="sxs-lookup"><span data-stu-id="dd2a7-135">GL\_NEAREST</span></span>                  |
| <span data-ttu-id="dd2a7-136">TX \_ Bilinear</span><span class="sxs-lookup"><span data-stu-id="dd2a7-136">TX\_BILINEAR</span></span>              | <span data-ttu-id="dd2a7-137">GL \_ linear</span><span class="sxs-lookup"><span data-stu-id="dd2a7-137">GL\_LINEAR</span></span>                   |
| <span data-ttu-id="dd2a7-138">TX- \_ MipMap- \_ Punkt</span><span class="sxs-lookup"><span data-stu-id="dd2a7-138">TX\_MIPMAP\_POINT</span></span>         | <span data-ttu-id="dd2a7-139">nächste \_ nächste \_ MipMap \_ am nächsten</span><span class="sxs-lookup"><span data-stu-id="dd2a7-139">GL\_NEAREST\_MIPMAP\_NEAREST</span></span> |
| <span data-ttu-id="dd2a7-140">TX \_ MipMap \_ Bilinear</span><span class="sxs-lookup"><span data-stu-id="dd2a7-140">TX\_MIPMAP\_BILINEAR</span></span>      | <span data-ttu-id="dd2a7-141">GL \_ lineare \_ MipMap am \_ nächsten</span><span class="sxs-lookup"><span data-stu-id="dd2a7-141">GL\_LINEAR\_MIPMAP\_NEAREST</span></span>  |
| <span data-ttu-id="dd2a7-142">TX \_ MipMap \_ linear</span><span class="sxs-lookup"><span data-stu-id="dd2a7-142">TX\_MIPMAP\_LINEAR</span></span>        | <span data-ttu-id="dd2a7-143">\_nächste nächste \_ MipMap ( \_ linear)</span><span class="sxs-lookup"><span data-stu-id="dd2a7-143">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>  |
| <span data-ttu-id="dd2a7-144">TX- \_ drei-linear</span><span class="sxs-lookup"><span data-stu-id="dd2a7-144">TX\_TRILINEAR</span></span>             | <span data-ttu-id="dd2a7-145">GL \_ lineare \_ MipMap \_ linear</span><span class="sxs-lookup"><span data-stu-id="dd2a7-145">GL\_LINEAR\_MIPMAP\_LINEAR</span></span>   |



 

 

 





