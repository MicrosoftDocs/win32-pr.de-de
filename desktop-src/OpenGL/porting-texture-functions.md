---
title: Portieren von Textur Funktionen
description: Portieren von Textur Funktionen
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- IRIS GL portieren, Textur
- Portieren von IRIS GL, Textur
- Portieren auf OpenGL von IRIS GL, Texture
- OpenGL-Portierung von IRIS GL, Textur
- Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cba8b105089553084a93f997517d19cf371e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037188"
---
# <a name="porting-texture-functions"></a><span data-ttu-id="f680a-108">Portieren von Textur Funktionen</span><span class="sxs-lookup"><span data-stu-id="f680a-108">Porting Texture Functions</span></span>

<span data-ttu-id="f680a-109">Beachten Sie beim Portieren von IRIS GL-Textur Funktionen in OpenGL die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="f680a-109">When porting IRIS GL texture functions to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="f680a-110">OpenGL verwaltet keine Tabellen mit Texturen. Sie verwendet entweder eine 1-d-Textur und eine 2D-Textur.</span><span class="sxs-lookup"><span data-stu-id="f680a-110">OpenGL doesn't maintain tables of textures; it uses either 1-D texture and 2-D texture only.</span></span> <span data-ttu-id="f680a-111">Um die Texturen aus dem IRIS GL-Code wiederzuverwenden, platzieren Sie Sie in einer Anzeigeliste.</span><span class="sxs-lookup"><span data-stu-id="f680a-111">To reuse the textures from your IRIS GL code, put them in a display list.</span></span>
-   <span data-ttu-id="f680a-112">OpenGL generiert nicht automatisch Mipmaps.</span><span class="sxs-lookup"><span data-stu-id="f680a-112">OpenGL doesn't automatically generate mipmaps.</span></span> <span data-ttu-id="f680a-113">Wenn Sie Mipmaps verwenden, müssen Sie zuerst die [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) -Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f680a-113">If you're using mipmaps, you must first call the [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) function.</span></span>
-   <span data-ttu-id="f680a-114">In OpenGL verwenden Sie [**glEnable**](glenable.md) und [**gldeaktiviert**](gldisable.md) , um die Funktionen für die Texturierung zu aktivieren und zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="f680a-114">In OpenGL, you use [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) to turn texturing capabilities on and off.</span></span>
-   <span data-ttu-id="f680a-115">In OpenGL ist die Textur Größe strenger geregelt als in IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="f680a-115">In OpenGL, texture size is more strictly regulated than in IRIS GL.</span></span> <span data-ttu-id="f680a-116">Die Größe einer OpenGL-Textur muss wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="f680a-116">The size of an OpenGL texture must be:</span></span>

    <span data-ttu-id="f680a-117">2 *n* + 2 *b*</span><span class="sxs-lookup"><span data-stu-id="f680a-117">2 *n* + 2 *b*</span></span>

    <span data-ttu-id="f680a-118">Dabei ist *n* eine ganze Zahl, und *b* ist:</span><span class="sxs-lookup"><span data-stu-id="f680a-118">where *n* is an integer and *b* is:</span></span>

    -   <span data-ttu-id="f680a-119">0, wenn die Textur keinen Rahmen hat.</span><span class="sxs-lookup"><span data-stu-id="f680a-119">0, if the texture has no border</span></span>
    -   <span data-ttu-id="f680a-120">1, wenn die Textur einen Rahmen Pixel aufweist (OpenGL-Texturen können 1-Pixel-Rahmen aufweisen).</span><span class="sxs-lookup"><span data-stu-id="f680a-120">1, if the texture has a border pixel (OpenGL textures can have 1-pixel borders.)</span></span>

<span data-ttu-id="f680a-121">In der folgenden Tabelle werden die Textur Funktionen von IRIS GL und ihre allgemeinen OpenGL-Entsprechungen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f680a-121">The following table lists IRIS GL texture functions and their general OpenGL equivalents.</span></span>



| <span data-ttu-id="f680a-122">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="f680a-122">IRIS GL function</span></span> | <span data-ttu-id="f680a-123">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="f680a-123">OpenGL function</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="f680a-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f680a-124">Meaning</span></span>                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f680a-125">**textdef2d**</span><span class="sxs-lookup"><span data-stu-id="f680a-125">**textdef2d**</span></span>    | <span data-ttu-id="f680a-126">[**glTexImage2D**](glteximage2d.md)[**gltexparameter**](gltexparameter-functions.md)</span><span class="sxs-lookup"><span data-stu-id="f680a-126">[**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)</span></span><br/> [<span data-ttu-id="f680a-127">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="f680a-127">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)<br/>                                                                                                           | <span data-ttu-id="f680a-128">Gibt ein 2D-Textur Bild an.</span><span class="sxs-lookup"><span data-stu-id="f680a-128">Specifies a 2-D texture image.</span></span>                                                              |
| <span data-ttu-id="f680a-129">**textbind**</span><span class="sxs-lookup"><span data-stu-id="f680a-129">**textbind**</span></span>     | <span data-ttu-id="f680a-130">**glTexImage2DglTexParameter**</span><span class="sxs-lookup"><span data-stu-id="f680a-130">**glTexImage2DglTexParameter**</span></span><br/> <span data-ttu-id="f680a-131">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="f680a-131">**gluBuild2DMipmaps**</span></span><br/>                                                                                                                                                                                            | <span data-ttu-id="f680a-132">Wählt eine Textur Funktion aus.</span><span class="sxs-lookup"><span data-stu-id="f680a-132">Selects a texture function.</span></span>                                                                 |
| <span data-ttu-id="f680a-133">**tevdef**</span><span class="sxs-lookup"><span data-stu-id="f680a-133">**tevdef**</span></span>       | [<span data-ttu-id="f680a-134">**gltexd**</span><span class="sxs-lookup"><span data-stu-id="f680a-134">**glTexEnv**</span></span>](gltexenv-functions.md)                                                                                                                                                                                                                                | <span data-ttu-id="f680a-135">Definiert eine Textur Mapping-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="f680a-135">Defines a texture-mapping environment.</span></span>                                                      |
| <span data-ttu-id="f680a-136">**tevbind**</span><span class="sxs-lookup"><span data-stu-id="f680a-136">**tevbind**</span></span>      | <span data-ttu-id="f680a-137">**gltexd**[**glTexImage1D**](glteximage1d.md)</span><span class="sxs-lookup"><span data-stu-id="f680a-137">**glTexEnv**[**glTexImage1D**](glteximage1d.md)</span></span><br/>                                                                                                                                                                                                           | <span data-ttu-id="f680a-138">Wählt eine Textur Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="f680a-138">Selects a texture environment.</span></span>                                                              |
| <span data-ttu-id="f680a-139">**T2**</span><span class="sxs-lookup"><span data-stu-id="f680a-139">**t2**</span></span>           | [<span data-ttu-id="f680a-140">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="f680a-140">**glTexCoord**</span></span>](gltexcoord-functions.md)                                                                                                                                                                                                                            | <span data-ttu-id="f680a-141">Legt die aktuellen Texturkoordinaten fest.</span><span class="sxs-lookup"><span data-stu-id="f680a-141">Sets the current texture coordinates.</span></span>                                                       |
| <span data-ttu-id="f680a-142">**TEXGEN**</span><span class="sxs-lookup"><span data-stu-id="f680a-142">**texgen**</span></span>       | <span data-ttu-id="f680a-143">[**gltexgen**](gltexgen-functions.md)[**glgettexparameter**](glgettexparameter.md)</span><span class="sxs-lookup"><span data-stu-id="f680a-143">[**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)</span></span><br/> [<span data-ttu-id="f680a-144">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="f680a-144">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)<br/> [<span data-ttu-id="f680a-145">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="f680a-145">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)<br/> [<span data-ttu-id="f680a-146">**gluscaleimage**</span><span class="sxs-lookup"><span data-stu-id="f680a-146">**gluScaleImage**</span></span>](gluscaleimage.md)<br/> | <span data-ttu-id="f680a-147">Steuert die Generierung von Texturkoordinaten. Skaliert ein Bild auf eine beliebige Größe.</span><span class="sxs-lookup"><span data-stu-id="f680a-147">Controls generation of texture coordinates.Scales an image to an arbitrary size.</span></span><br/> |



 

<span data-ttu-id="f680a-148">Weitere Informationen zum Texturierung finden Sie im *OpenGL-Programmier Handbuch*.</span><span class="sxs-lookup"><span data-stu-id="f680a-148">For more information on texturing, see the *OpenGL Programming Guide*.</span></span>

<span data-ttu-id="f680a-149">Dieses Thema enthält Informationen zu den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="f680a-149">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="f680a-150">Übersetzen von tevdef</span><span class="sxs-lookup"><span data-stu-id="f680a-150">Translating tevdef</span></span>](translating-tevdef.md)
-   [<span data-ttu-id="f680a-151">Übersetzen von texdef</span><span class="sxs-lookup"><span data-stu-id="f680a-151">Translating texdef</span></span>](translating-texdef.md)
-   [<span data-ttu-id="f680a-152">Übersetzen von TEXGEN</span><span class="sxs-lookup"><span data-stu-id="f680a-152">Translating texgen</span></span>](translating-texgen.md)

 

 





