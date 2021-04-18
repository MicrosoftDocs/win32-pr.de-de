---
title: Übersetzen von TEXGEN
description: Die Iris GL-Funktion TEXGEN wird in gltexgen für OpenGL übersetzt.
ms.assetid: ddf398ed-37d4-4fb6-97be-20fe0564cb77
keywords:
- IRIS GL portieren, Textur
- Portieren von IRIS GL, Textur
- Portieren auf OpenGL von IRIS GL, Texture
- OpenGL-Portierung von IRIS GL, Textur
- Struktur
- IRIS GL portieren, TEXGEN
- Portieren von IRIS GL, TEXGEN
- Portieren auf OpenGL von IRIS GL, TEXGEN
- OpenGL-Portierung von IRIS GL, TEXGEN
- TEXGEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07654fc35e20096ed71c3fe74ff9279214eb45c8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337612"
---
# <a name="translating-texgen"></a><span data-ttu-id="5c979-113">Übersetzen von TEXGEN</span><span class="sxs-lookup"><span data-stu-id="5c979-113">Translating texgen</span></span>

<span data-ttu-id="5c979-114">Die Iris GL-Funktion **TEXGEN** wird in [gltexgen](gltexgen-functions.md) für OpenGL übersetzt.</span><span class="sxs-lookup"><span data-stu-id="5c979-114">The IRIS GL function **texgen** is translated to [glTexGen](gltexgen-functions.md) for OpenGL.</span></span>

<span data-ttu-id="5c979-115">Bei Iris GL wird **TEXGEN** zweimal aufgerufen: einmal, um den Modus und die ebenengleichung gleichzeitig festzulegen, und einmal, um die Generierung der Textur Koordinate zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5c979-115">With IRIS GL, you call **texgen** twice: once to set the mode and plane equation simultaneously, and once to enable texture-coordinate generation.</span></span> <span data-ttu-id="5c979-116">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5c979-116">For example:</span></span>


```C++
texgen(TX_S, TG_LINEAR, planeParams); 
texgen(TX_S, TG_ON, NULL);
```



<span data-ttu-id="5c979-117">Mit OpenGL führen Sie drei Aufrufe aus: zwei bis zu **gltexgen** (einmal, um den Modus festzulegen, und einmal, um die Ebene der Ebene festzulegen) und einen zu [**glEnable**](glenable.md).</span><span class="sxs-lookup"><span data-stu-id="5c979-117">With OpenGL, you make three calls: two to **glTexGen** (once to set the mode and once to set the plane equation), and one to [**glEnable**](glenable.md).</span></span> <span data-ttu-id="5c979-118">Beispielsweise ist der OpenGL-Code, der dem obigen IRIS GL-Code entspricht,:</span><span class="sxs-lookup"><span data-stu-id="5c979-118">For example, the OpenGL equivalent to the IRIS GL code above is:</span></span>


```C++
glTexGen(GL_S, GLTEXTURE_GEN_MODE, modeName); 
glTextGen(GL_S, GL_OBJECT_PLANE, planeParameters); 
glEnable(GL_TEXTURE_GEN_S);
```



<span data-ttu-id="5c979-119">In der folgenden Tabelle werden die Namen der Iris GL-Texturkoordinaten und deren OpenGL-Entsprechungen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5c979-119">The following table lists the IRIS GL texture-coordinate names and their OpenGL equivalents.</span></span>



| <span data-ttu-id="5c979-120">IRIS GL-Textur Koordinate</span><span class="sxs-lookup"><span data-stu-id="5c979-120">IRIS GL texture coordinate</span></span> | <span data-ttu-id="5c979-121">OpenGL-Textur Koordinate</span><span class="sxs-lookup"><span data-stu-id="5c979-121">OpenGL texture coordinate</span></span> | <span data-ttu-id="5c979-122">glEnable-Argument</span><span class="sxs-lookup"><span data-stu-id="5c979-122">glEnable argument</span></span>   |
|----------------------------|---------------------------|---------------------|
| <span data-ttu-id="5c979-123">TX \_ S</span><span class="sxs-lookup"><span data-stu-id="5c979-123">TX\_S</span></span>                      | <span data-ttu-id="5c979-124">GL \_ S</span><span class="sxs-lookup"><span data-stu-id="5c979-124">GL\_S</span></span>                     | <span data-ttu-id="5c979-125">GL- \_ Textur \_ gen \_ S</span><span class="sxs-lookup"><span data-stu-id="5c979-125">GL\_TEXTURE\_GEN\_S</span></span> |
| <span data-ttu-id="5c979-126">TX \_ T</span><span class="sxs-lookup"><span data-stu-id="5c979-126">TX\_T</span></span>                      | <span data-ttu-id="5c979-127">GL \_ T</span><span class="sxs-lookup"><span data-stu-id="5c979-127">GL\_T</span></span>                     | <span data-ttu-id="5c979-128">GL \_ Textur \_ gen \_ T</span><span class="sxs-lookup"><span data-stu-id="5c979-128">GL\_TEXTURE\_GEN\_T</span></span> |
| <span data-ttu-id="5c979-129">TX \_ R</span><span class="sxs-lookup"><span data-stu-id="5c979-129">TX\_R</span></span>                      | <span data-ttu-id="5c979-130">GL \_ .</span><span class="sxs-lookup"><span data-stu-id="5c979-130">GL\_R</span></span>                     | <span data-ttu-id="5c979-131">GL \_ Textur \_ gen \_ R</span><span class="sxs-lookup"><span data-stu-id="5c979-131">GL\_TEXTURE\_GEN\_R</span></span> |
| <span data-ttu-id="5c979-132">TX \_ Q</span><span class="sxs-lookup"><span data-stu-id="5c979-132">TX\_Q</span></span>                      | <span data-ttu-id="5c979-133">GL. \_ f</span><span class="sxs-lookup"><span data-stu-id="5c979-133">GL\_Q</span></span>                     | <span data-ttu-id="5c979-134">GL \_ Textur \_ gen, \_ Q</span><span class="sxs-lookup"><span data-stu-id="5c979-134">GL\_TEXTURE\_GEN\_Q</span></span> |



 

<span data-ttu-id="5c979-135">In der folgenden Tabelle sind die Formen der Iris GL-Textur Generierung und ihre entsprechenden OpenGL-Textur Modi und-Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5c979-135">The following table lists the IRIS GL texture-generation modes and their equivalent OpenGL texture modes and plane names.</span></span>



| <span data-ttu-id="5c979-136">IRIS GL-Textur Modus</span><span class="sxs-lookup"><span data-stu-id="5c979-136">IRIS GL texture mode</span></span> | <span data-ttu-id="5c979-137">OpenGL-Textur Modus</span><span class="sxs-lookup"><span data-stu-id="5c979-137">OpenGL texture mode</span></span> | <span data-ttu-id="5c979-138">OpenGL-Ebenenname</span><span class="sxs-lookup"><span data-stu-id="5c979-138">OpenGL plane name</span></span> |
|----------------------|---------------------|-------------------|
| <span data-ttu-id="5c979-139">TG \_ linear</span><span class="sxs-lookup"><span data-stu-id="5c979-139">TG\_LINEAR</span></span>           | <span data-ttu-id="5c979-140">GL- \_ Objekt \_ linear</span><span class="sxs-lookup"><span data-stu-id="5c979-140">GL\_OBJECT\_LINEAR</span></span>  | <span data-ttu-id="5c979-141">GL- \_ Objekt \_ Ebene</span><span class="sxs-lookup"><span data-stu-id="5c979-141">GL\_OBJECT\_PLANE</span></span> |
| <span data-ttu-id="5c979-142">TG- \_ Kontur</span><span class="sxs-lookup"><span data-stu-id="5c979-142">TG\_CONTOUR</span></span>          | <span data-ttu-id="5c979-143">GL- \_ Eye \_ linear</span><span class="sxs-lookup"><span data-stu-id="5c979-143">GL\_EYE\_LINEAR</span></span>     | <span data-ttu-id="5c979-144">GL- \_ Augen \_ Ebene</span><span class="sxs-lookup"><span data-stu-id="5c979-144">GL\_EYE\_PLANE</span></span>    |
| <span data-ttu-id="5c979-145">\_spheremap von TG</span><span class="sxs-lookup"><span data-stu-id="5c979-145">TG\_SPHEREMAP</span></span>        | <span data-ttu-id="5c979-146">GL- \_ Kugel \_ Karte</span><span class="sxs-lookup"><span data-stu-id="5c979-146">GL\_SPHERE\_MAP</span></span>     |                   |



 

 

 




