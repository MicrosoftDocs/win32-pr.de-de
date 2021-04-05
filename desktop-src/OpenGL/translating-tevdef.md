---
title: Übersetzen von tevdef
description: Das folgende Codebeispiel ist eine IRIS GL-Textur-Umgebungs Definition, die den \_ Parameter "TV Decal Texture-Environment" angibt.
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- IRIS GL portieren, Textur
- Portieren von IRIS GL, Textur
- Portieren auf OpenGL von IRIS GL, Texture
- OpenGL-Portierung von IRIS GL, Textur
- Struktur
- IRIS GL Porting, tevdef
- Portieren von IRIS GL, tevdef
- Portieren auf OpenGL von IRIS GL, tevdef
- OpenGL-Portierung von IRIS GL, tevdef
- tevdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac2610d1467adb6faa1ea105fc8e8734bfb9c4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948032"
---
# <a name="translating-tevdef"></a><span data-ttu-id="3b87a-113">Übersetzen von tevdef</span><span class="sxs-lookup"><span data-stu-id="3b87a-113">Translating tevdef</span></span>

<span data-ttu-id="3b87a-114">Das folgende Codebeispiel ist eine IRIS GL-Textur-Umgebungs Definition, die den \_ Parameter "TV-Decal Texture-Environment" angibt:</span><span class="sxs-lookup"><span data-stu-id="3b87a-114">The following code example is an IRIS GL texture-environment definition that specifies the TV\_DECAL texture-environment parameter:</span></span>


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



<span data-ttu-id="3b87a-115">und der gleiche Code, der in OpenGL übersetzt wurde:</span><span class="sxs-lookup"><span data-stu-id="3b87a-115">and the same code translated to OpenGL:</span></span>


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



<span data-ttu-id="3b87a-116">In der folgenden Tabelle werden die Parameter der Iris GL-Textur Umgebung und ihre entsprechenden OpenGL-Parameter aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3b87a-116">The following table lists the IRIS GL texture-environment parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="3b87a-117">IRIS GL-Parameter</span><span class="sxs-lookup"><span data-stu-id="3b87a-117">IRIS GL parameter</span></span>     | <span data-ttu-id="3b87a-118">OpenGL-Parameter</span><span class="sxs-lookup"><span data-stu-id="3b87a-118">OpenGL parameter</span></span>             |
|-----------------------|------------------------------|
| <span data-ttu-id="3b87a-119">TV- \_ modulate</span><span class="sxs-lookup"><span data-stu-id="3b87a-119">TV\_MODULATE</span></span>          | <span data-ttu-id="3b87a-120">GL \_ modulate</span><span class="sxs-lookup"><span data-stu-id="3b87a-120">GL\_MODULATE</span></span>                 |
| <span data-ttu-id="3b87a-121">TV \_ -Debug</span><span class="sxs-lookup"><span data-stu-id="3b87a-121">TV\_DECAL</span></span>             | <span data-ttu-id="3b87a-122">GL \_ -Debug</span><span class="sxs-lookup"><span data-stu-id="3b87a-122">GL\_DECAL</span></span>                    |
| <span data-ttu-id="3b87a-123">TV- \_ Blend</span><span class="sxs-lookup"><span data-stu-id="3b87a-123">TV\_BLEND</span></span>             | <span data-ttu-id="3b87a-124">GL \_ Blend</span><span class="sxs-lookup"><span data-stu-id="3b87a-124">GL\_BLEND</span></span>                    |
| <span data-ttu-id="3b87a-125">TV- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="3b87a-125">TV\_COLOR</span></span>             | <span data-ttu-id="3b87a-126">GL- \_ Textur Gesamt \_ \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="3b87a-126">GL\_TEXTURE\_ENV\_COLOR</span></span>      |
| <span data-ttu-id="3b87a-127">TV- \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="3b87a-127">TV\_ALPHA</span></span>             | <span data-ttu-id="3b87a-128">Keine direkte OpenGL-Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="3b87a-128">No direct OpenGL equivalent.</span></span> |
| <span data-ttu-id="3b87a-129">TV- \_ Komponente \_ auswählen</span><span class="sxs-lookup"><span data-stu-id="3b87a-129">TV\_COMPONENT\_SELECT</span></span> | <span data-ttu-id="3b87a-130">Keine direkte OpenGL-Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="3b87a-130">No direct OpenGL equivalent.</span></span> |



 

<span data-ttu-id="3b87a-131">Weitere Informationen zu Textur Umgebungs Parametern finden Sie unter [**gltextev**](gltexenv-functions.md).</span><span class="sxs-lookup"><span data-stu-id="3b87a-131">For more information about texture-environment parameters, see [**glTexEnv**](gltexenv-functions.md).</span></span>

 

 




