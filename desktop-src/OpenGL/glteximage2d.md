---
title: glTexImage2D-Funktion (GL. h)
description: Die glTexImage2D-Funktion gibt ein zweidimensionales Textur Bild an.
ms.assetid: e8b9c692-5239-47de-86eb-80c247c60e1d
keywords:
- glTexImage2D-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba2d5bc6f966d9b10c0dadccb221086e64de827
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346771"
---
# <a name="glteximage2d-function"></a><span data-ttu-id="43156-104">glTexImage2D-Funktion</span><span class="sxs-lookup"><span data-stu-id="43156-104">glTexImage2D function</span></span>

<span data-ttu-id="43156-105">Die **glTexImage2D** -Funktion gibt ein zweidimensionales Textur Bild an.</span><span class="sxs-lookup"><span data-stu-id="43156-105">The **glTexImage2D** function specifies a two-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="43156-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="43156-106">Syntax</span></span>


```C++
void WINAPI glTexImage2D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLsizei height,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="43156-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="43156-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43156-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="43156-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="43156-109">Die Ziel Textur.</span><span class="sxs-lookup"><span data-stu-id="43156-109">The target texture.</span></span> <span data-ttu-id="43156-110">Muss "GL \_ Texture \_ 2D" lauten.</span><span class="sxs-lookup"><span data-stu-id="43156-110">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="43156-111">*level*</span><span class="sxs-lookup"><span data-stu-id="43156-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="43156-112">Die Detailebene.</span><span class="sxs-lookup"><span data-stu-id="43156-112">The level-of-detail number.</span></span> <span data-ttu-id="43156-113">Ebene 0 ist die Basis Image Ebene.</span><span class="sxs-lookup"><span data-stu-id="43156-113">Level 0 is the base image level.</span></span> <span data-ttu-id="43156-114">Ebene *n* ist das *n* -te MipMap-Reduzierungs Bild.</span><span class="sxs-lookup"><span data-stu-id="43156-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="43156-115">*internalformat*</span><span class="sxs-lookup"><span data-stu-id="43156-115">*internalformat*</span></span> 
</dt> <dd>

<span data-ttu-id="43156-116">Die Anzahl der Farbkomponenten in der Textur.</span><span class="sxs-lookup"><span data-stu-id="43156-116">The number of color components in the texture.</span></span> <span data-ttu-id="43156-117">Muss 1, 2, 3 oder 4 sein oder eine der folgenden symbolischen Konstanten sein: GL \_ Alpha, GL \_ ALPHA4, GL \_ ALPHA8, GL \_ ALPHA12, GL \_ ALPHA16, GL \_ Luminance, GL \_ LUMINANCE4, GL \_ LUMINANCE8, GL \_ LUMINANCE12, GL \_ LUMINANCE16, GL \_ Luminance \_ Alpha, GL \_ LUMINANCE4 \_ ALPHA4, GL \_ LUMINANCE6 \_ ALPHA2, GL \_ LUMINANCE8 \_ ALPHA8, GL \_ LUMINANCE12 \_ ALPHA4, GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 \_ ALPHA16, GL \_ Intensität, GL \_ INTENSITY4, GL \_ INTENSITY8, GL \_ INTENSITY12, GL \_ INTENSITY16, GL \_ R3 \_ G3 \_ B2, GL \_ RGB, GL \_ RGB4, GL \_ RGB5, GL \_ RGB8, GL \_ RGB10, GL \_ RGB12, GL \_ RGB16, GL \_ RGBA, GL \_ RGBA2, GL \_ RGBA4, GL \_ RGB5 \_ a1, GL \_ RGBA8, GL \_ RGB10 \_ a2, GL \_ RGBA12 oder GL \_ RGBA16.</span><span class="sxs-lookup"><span data-stu-id="43156-117">Must be 1, 2, 3, or 4, or one of the following symbolic constants: GL\_ALPHA, GL\_ALPHA4, GL\_ALPHA8, GL\_ALPHA12, GL\_ALPHA16, GL\_LUMINANCE, GL\_LUMINANCE4, GL\_LUMINANCE8, GL\_LUMINANCE12, GL\_LUMINANCE16, GL\_LUMINANCE\_ALPHA, GL\_LUMINANCE4\_ALPHA4, GL\_LUMINANCE6\_ALPHA2, GL\_LUMINANCE8\_ALPHA8, GL\_LUMINANCE12\_ALPHA4, GL\_LUMINANCE12\_ALPHA12, GL\_LUMINANCE16\_ALPHA16, GL\_INTENSITY, GL\_INTENSITY4, GL\_INTENSITY8, GL\_INTENSITY12, GL\_INTENSITY16, GL\_R3\_G3\_B2, GL\_RGB, GL\_RGB4, GL\_RGB5, GL\_RGB8, GL\_RGB10, GL\_RGB12, GL\_RGB16, GL\_RGBA, GL\_RGBA2, GL\_RGBA4, GL\_RGB5\_A1, GL\_RGBA8, GL\_RGB10\_A2, GL\_RGBA12, or GL\_RGBA16.</span></span>

</dd> <dt>

<span data-ttu-id="43156-118">*width*</span><span class="sxs-lookup"><span data-stu-id="43156-118">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="43156-119">Die Breite des Textur Bilds.</span><span class="sxs-lookup"><span data-stu-id="43156-119">The width of the texture image.</span></span> <span data-ttu-id="43156-120">Muss für eine Ganzzahl *n* 2 *n* +*2 (Rahmen*) lauten.</span><span class="sxs-lookup"><span data-stu-id="43156-120">Must be 2 *n* + 2(*border*) for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="43156-121">*height*</span><span class="sxs-lookup"><span data-stu-id="43156-121">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="43156-122">Die Höhe des Textur Bilds.</span><span class="sxs-lookup"><span data-stu-id="43156-122">The height of the texture image.</span></span> <span data-ttu-id="43156-123">Muss für ein ganzzahliges *m* 2 *<sup>m</sup>* +*2 (Rahmen*) sein.</span><span class="sxs-lookup"><span data-stu-id="43156-123">Must be 2 *<sup>m</sup>* + 2(*border*) for some integer *m*.</span></span>

</dd> <dt>

<span data-ttu-id="43156-124">*Aun*</span><span class="sxs-lookup"><span data-stu-id="43156-124">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="43156-125">Die Breite des Rahmens.</span><span class="sxs-lookup"><span data-stu-id="43156-125">The width of the border.</span></span> <span data-ttu-id="43156-126">Muss entweder 0 oder 1 sein.</span><span class="sxs-lookup"><span data-stu-id="43156-126">Must be either 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="43156-127">*format*</span><span class="sxs-lookup"><span data-stu-id="43156-127">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="43156-128">Das Format der Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="43156-128">The format of the pixel data.</span></span> <span data-ttu-id="43156-129">Es kann einen von neun symbolischen Werten annehmen.</span><span class="sxs-lookup"><span data-stu-id="43156-129">It can assume one of nine symbolic values.</span></span>



| <span data-ttu-id="43156-130">Wert</span><span class="sxs-lookup"><span data-stu-id="43156-130">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="43156-131">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="43156-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="43156-132"><dt>**GL- \_ Farb \_ Index**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-132"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="43156-133">Jedes Element ist ein einzelner Wert, ein Farbindex.</span><span class="sxs-lookup"><span data-stu-id="43156-133">Each element is a single value, a color index.</span></span> <span data-ttu-id="43156-134">Es wird in einen festgelegten Punkt (mit einer nicht angegebenen Anzahl von 0 Bits rechts neben dem binären Punkt) konvertiert, abhängig vom Wert und Vorzeichen der GL-Index Verschiebung nach links oder rechts verschoben \_ \_ und dem GL- \_ Index \_ Offset (siehe [**glpixeltransfer**](glpixeltransfer.md)) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="43156-134">It is converted to fixed point (with an unspecified number of 0 bits to the right of the binary point), shifted left or right depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="43156-135">Der resultierende Index wird mithilfe von GL \_ Pixel \_ map \_ i to \_ \_ R, GL \_ Pixel \_ map \_ i \_ to \_ G, GL \_ Pixel \_ map \_ i \_ to \_ B und GL Pixel Map i to a Tables in eine Gruppe von Farbkomponenten konvertiert \_ \_ \_ \_ \_ und an den Bereich \[ 0, 1 gebunden \] .</span><span class="sxs-lookup"><span data-stu-id="43156-135">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="43156-136"><dt>**GL. \_ rot**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-136"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="43156-137">Jedes Element ist eine einzelne rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="43156-137">Each element is a single red component.</span></span> <span data-ttu-id="43156-138">Sie wird in den Gleit Komma Wert konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für Grün und blau und 1,0 für Alpha angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="43156-138">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="43156-139">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.</span><span class="sxs-lookup"><span data-stu-id="43156-139">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                               |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="43156-140"><dt>**GL \_ grün**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-140"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="43156-141">Jedes Element ist eine einzelne grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="43156-141">Each element is a single green component.</span></span> <span data-ttu-id="43156-142">Sie wird in den Gleit Komma Wert konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für "Red" und "Blue" und 1,0 für Alpha angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="43156-142">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="43156-143">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe [**glpixeltransfer**](glpixeltransfer.md)) gebunden.</span><span class="sxs-lookup"><span data-stu-id="43156-143">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                        |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="43156-144"><dt>**GL \_ blau**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-144"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="43156-145">Jedes Element ist eine einzelne blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="43156-145">Each element is a single blue component.</span></span> <span data-ttu-id="43156-146">Sie wird in den Gleit Komma Wert konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für Rot und grün und 1,0 für Alpha angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="43156-146">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="43156-147">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.</span><span class="sxs-lookup"><span data-stu-id="43156-147">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                               |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="43156-148"><dt>**GL- \_ Alpha**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-148"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="43156-149">Jedes Element ist eine einzelne rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="43156-149">Each element is a single red component.</span></span> <span data-ttu-id="43156-150">Sie wird in den Gleit Komma Wert konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für Rot, grün und blau angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="43156-150">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="43156-151">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe [**glpixeltransfer**](glpixeltransfer.md)) gebunden.</span><span class="sxs-lookup"><span data-stu-id="43156-151">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                     |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="43156-152"><dt>**GL. \_ RGB**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-152"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="43156-153">Jedes Element ist ein RGB-Triple.</span><span class="sxs-lookup"><span data-stu-id="43156-153">Each element is an RGB triple.</span></span> <span data-ttu-id="43156-154">Sie wird in den Gleit Komma Wert konvertiert und in ein RGBA-Element zusammengefasst, indem 1,0 für Alpha angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="43156-154">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="43156-155">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.</span><span class="sxs-lookup"><span data-stu-id="43156-155">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="43156-156"><dt>**GL \_ RGBA**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-156"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="43156-157">Jedes Element ist ein umfassendes RGBA-Element.</span><span class="sxs-lookup"><span data-stu-id="43156-157">Each element is a complete RGBA element.</span></span> <span data-ttu-id="43156-158">Der Wert wird in einen Gleit Komma Wert konvertiert.</span><span class="sxs-lookup"><span data-stu-id="43156-158">It is converted to floating point.</span></span> <span data-ttu-id="43156-159">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe [**glpixeltransfer**](glpixeltransfer.md)) gebunden.</span><span class="sxs-lookup"><span data-stu-id="43156-159">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="43156-160"><dt>**GL \_ BGR \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-160"><dt>**GL\_BGR\_EXT**</dt></span></span> </dl>                         | <span data-ttu-id="43156-161">Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: blau, grün, rot.</span><span class="sxs-lookup"><span data-stu-id="43156-161">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="43156-162">GL \_ BGR \_ ext bietet ein Format, das dem Arbeitsspeicher Layout von Windows-geräteunabhängigen Bitmaps (DIB) entspricht.</span><span class="sxs-lookup"><span data-stu-id="43156-162">GL\_BGR\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="43156-163">Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.</span><span class="sxs-lookup"><span data-stu-id="43156-163">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="43156-164"><dt>**GL \_ BGRA \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-164"><dt>**GL\_BGRA\_EXT**</dt></span></span> </dl>                      | <span data-ttu-id="43156-165">Jedes Pixel ist eine Gruppe von vier Komponenten in dieser Reihenfolge: blau, grün, rot, alpha.</span><span class="sxs-lookup"><span data-stu-id="43156-165">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span> <span data-ttu-id="43156-166">GL \_ BGRA \_ ext bietet ein Format, das dem Arbeitsspeicher Layout von Windows-geräteunabhängigen Bitmaps (DIB) entspricht.</span><span class="sxs-lookup"><span data-stu-id="43156-166">GL\_BGRA\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="43156-167">Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.</span><span class="sxs-lookup"><span data-stu-id="43156-167">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="43156-168"><dt>**GL- \_ Beleuchtung**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-168"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="43156-169">Jedes Element ist ein einzelner Wert für die Leuchtkraft.</span><span class="sxs-lookup"><span data-stu-id="43156-169">Each element is a single luminance value.</span></span> <span data-ttu-id="43156-170">Sie wird in Gleit Komma Zahlen konvertiert und dann in einem RGBA-Element zusammengefasst, indem der Wert für die Leuchtkraft dreimal für Rot, grün und blau replizieren und 1,0 für Alpha angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="43156-170">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="43156-171">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.</span><span class="sxs-lookup"><span data-stu-id="43156-171">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                         |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="43156-172"><dt>**GL- \_ Leuchtkraft \_ Alpha**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-172"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="43156-173">Jedes Element ist ein leuchtendes/Alpha-Paar.</span><span class="sxs-lookup"><span data-stu-id="43156-173">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="43156-174">Sie wird in den Gleit Komma Wert konvertiert und dann in einem RGBA-Element zusammengefasst, indem der Wert für die Leuchtkraft drei Mal für Rot, grün und blau replizieren wird.</span><span class="sxs-lookup"><span data-stu-id="43156-174">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="43156-175">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe [**glpixeltransfer**](glpixeltransfer.md)) gebunden.</span><span class="sxs-lookup"><span data-stu-id="43156-175">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="43156-176">*type*</span><span class="sxs-lookup"><span data-stu-id="43156-176">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="43156-177">Der Datentyp der Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="43156-177">The data type of the pixel data.</span></span> <span data-ttu-id="43156-178">Die folgenden symbolischen Werte werden akzeptiert: GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ Bitmap, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int und GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="43156-178">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="43156-179">*Pixel*</span><span class="sxs-lookup"><span data-stu-id="43156-179">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="43156-180">Ein Zeiger auf die Bilddaten im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="43156-180">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43156-181">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43156-181">Return value</span></span>

<span data-ttu-id="43156-182">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="43156-182">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="43156-183">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="43156-183">Error codes</span></span>

<span data-ttu-id="43156-184">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="43156-184">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="43156-185">Name</span><span class="sxs-lookup"><span data-stu-id="43156-185">Name</span></span>                                                                                                  | <span data-ttu-id="43156-186">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="43156-186">Meaning</span></span>                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43156-187"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-187"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="43156-188">Das *Ziel* war keine GL \_ \_ -Textur 2D.</span><span class="sxs-lookup"><span data-stu-id="43156-188">*target* was not an GL\_TEXTURE\_2D.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="43156-189"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-189"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="43156-190">Das *Format* war keine akzeptierte *Format* Konstante.</span><span class="sxs-lookup"><span data-stu-id="43156-190">*format* was not an accepted *format* constant.</span></span> <span data-ttu-id="43156-191">Nur Format Konstanten außer dem GL \_ -Schablonen \_ Index und der GL- \_ tiefen \_ Komponente werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="43156-191">Only format constants other than GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT are accepted.</span></span> <span data-ttu-id="43156-192">Eine Liste möglicher Werte finden Sie in der Beschreibung des- *Formats* des-Parameters.</span><span class="sxs-lookup"><span data-stu-id="43156-192">See the parameter description of *format* for a list of possible values.</span></span><br/> |
| <dl> <span data-ttu-id="43156-193"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-193"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="43156-194">der *Typ* war keine *typkonstante* .</span><span class="sxs-lookup"><span data-stu-id="43156-194">*type* was not a *type* constant.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="43156-195"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-195"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="43156-196">*Typ* : GL \_ Bitmap und *Format* war kein GL \_ - \_ Farbindex.</span><span class="sxs-lookup"><span data-stu-id="43156-196">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                        |
| <dl> <span data-ttu-id="43156-197"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-197"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="43156-198">die *Ebene* war kleiner als 0 (null) oder größer als log2 *Max*, wobei *Max* der zurückgegebene Wert von GL \_ Max \_ Texture \_ size war.</span><span class="sxs-lookup"><span data-stu-id="43156-198">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="43156-199"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="43156-200">*internalformat* war nicht 1, 2, 3 oder 4.</span><span class="sxs-lookup"><span data-stu-id="43156-200">*internalformat* was was not 1, 2, 3, or 4.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="43156-201"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-201"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="43156-202">die *Breite* oder Höhe war kleiner als 0 (null) oder größer als 2 + gl \_ . die maximale \_ Textur \_ Größe, oder Sie konnte nicht als 2 *n* + 2 (Rahmen) für einen ganzzahligen Wert von *n* dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="43156-202">*width* or height was less than zero or greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or it could not be represented as 2 *n* + 2(border) for some integer value of *n*.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="43156-203"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-203"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="43156-204">der *Rahmen war nicht* 0 oder 1.</span><span class="sxs-lookup"><span data-stu-id="43156-204">*border* was not 0 or 1.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="43156-205"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="43156-205"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="43156-206">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="43156-206">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                          |



## <a name="remarks"></a><span data-ttu-id="43156-207">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43156-207">Remarks</span></span>

<span data-ttu-id="43156-208">Die **glTexImage2D** -Funktion gibt ein zweidimensionales Textur Bild an.</span><span class="sxs-lookup"><span data-stu-id="43156-208">The **glTexImage2D** function specifies a two-dimensional texture image.</span></span> <span data-ttu-id="43156-209">Bei der Texturierung wird ein Teil eines angegebenen *Textur Bilds* allen grafischen Primitiven zugeordnet, für die die Texturierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="43156-209">Texturing maps a portion of a specified *texture image* onto each graphical primitive for which texturing is enabled.</span></span> <span data-ttu-id="43156-210">Die zweidimensionale Texturierung wird mithilfe von [**glEnable**](glenable.md) und **glEnable** mit dem Argument GL \_ Texture \_ 2D aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="43156-210">Two-dimensional texturing is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_TEXTURE\_2D.</span></span>

<span data-ttu-id="43156-211">Textur Bilder werden mit **glTexImage2D** definiert.</span><span class="sxs-lookup"><span data-stu-id="43156-211">Texture images are defined with **glTexImage2D**.</span></span> <span data-ttu-id="43156-212">Die Argumente beschreiben die Parameter des Textur Bilds, z. b. Höhe, Breite, Breite des Rahmens, Detailebene (siehe [**gltexparameter**](gltexparameter-functions.md)) und Anzahl der angegebenen Farbkomponenten.</span><span class="sxs-lookup"><span data-stu-id="43156-212">The arguments describe the parameters of the texture image, such as height, width, width of the border, level-of-detail number (see [**glTexParameter**](gltexparameter-functions.md)), and number of color components provided.</span></span> <span data-ttu-id="43156-213">Die letzten drei Argumente beschreiben die Darstellung des Bilds im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="43156-213">The last three arguments describe the way the image is represented in memory.</span></span> <span data-ttu-id="43156-214">Diese Argumente sind identisch mit den für [**gldrawpixels**](gldrawpixels.md)verwendeten Pixel Formaten.</span><span class="sxs-lookup"><span data-stu-id="43156-214">These arguments are identical to the pixel formats used for [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="43156-215">Daten werden je nach *Typ* aus *Pixel* als Sequenz von Bytes mit oder ohne Vorzeichen, Shorts oder Longs oder Gleit Komma Werten mit einfacher Genauigkeit gelesen.</span><span class="sxs-lookup"><span data-stu-id="43156-215">Data is read from *pixels* as a sequence of signed or unsigned bytes, shorts or longs, or single-precision floating-point values, depending on *type*.</span></span> <span data-ttu-id="43156-216">Diese Werte werden je nach *Format* in Mengen von einem, zwei, drei oder vier Werten gruppiert, um Elemente zu bilden.</span><span class="sxs-lookup"><span data-stu-id="43156-216">These values are grouped into sets of one, two, three, or four values, depending on *format*, to form elements.</span></span> <span data-ttu-id="43156-217">Wenn der *Typ* "GL \_ Bitmap" ist, werden die Daten als Zeichenfolge nicht signierter Bytes betrachtet (und das *Format* muss ein GL- \_ \_ Farbindex sein).</span><span class="sxs-lookup"><span data-stu-id="43156-217">If *type* is GL\_BITMAP, the data is considered as a string of unsigned bytes (and *format* must be GL\_COLOR\_INDEX).</span></span> <span data-ttu-id="43156-218">Jedes Daten Byte wird als 8 1-Bit-Elemente behandelt, wobei die bitanordnung zuerst von GL \_ Entpack- \_ lsb \_ (siehe [**glpixelstore**](glpixelstore-functions.md)) bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="43156-218">Each data byte is treated as eight 1-bit elements, with bit ordering determined by GL\_UNPACK\_LSB\_FIRST (see [**glPixelStore**](glpixelstore-functions.md)).</span></span> <span data-ttu-id="43156-219">Eine Beschreibung der zulässigen Werte für den *Typparameter* finden Sie unter [**gldrawpixels**](gldrawpixels.md) .</span><span class="sxs-lookup"><span data-stu-id="43156-219">Please see [**glDrawPixels**](gldrawpixels.md) for a description of the acceptable values for the *type* parameter.</span></span>

<span data-ttu-id="43156-220">Ein Textur Bild kann je nach *Komponenten* bis zu vier Komponenten pro Textur Element aufweisen.</span><span class="sxs-lookup"><span data-stu-id="43156-220">A texture image can have up to four components per texture element, depending on *components*.</span></span> <span data-ttu-id="43156-221">Ein Textur Bild mit einer Komponente verwendet nur die rote Komponente der aus *Pixel* extrahierten RGBA-Farbe.</span><span class="sxs-lookup"><span data-stu-id="43156-221">A one-component texture image uses only the red component of the RGBA color extracted from *pixels*.</span></span> <span data-ttu-id="43156-222">Ein Image mit zwei Komponenten verwendet den R-Wert und einen-Wert.</span><span class="sxs-lookup"><span data-stu-id="43156-222">A two-component image uses the R and A values.</span></span> <span data-ttu-id="43156-223">Ein Image mit drei Komponenten verwendet die Werte R, G und B.</span><span class="sxs-lookup"><span data-stu-id="43156-223">A three-component image uses the R, G, and B values.</span></span> <span data-ttu-id="43156-224">Ein Image mit vier Komponenten verwendet alle RGBA-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="43156-224">A four-component image uses all of the RGBA components.</span></span>

<span data-ttu-id="43156-225">Die Texturierung hat keine Auswirkung auf den Farb Index Modus.</span><span class="sxs-lookup"><span data-stu-id="43156-225">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="43156-226">Das Textur Bild kann mit den gleichen Datenformaten dargestellt werden wie die Pixel in einem **gldrawpixels** -Befehl, mit dem Unterschied, dass der GL \_ \_ -Schablone-Index und die GL- \_ tiefen \_ Komponente nicht verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="43156-226">The texture image can be represented by the same data formats as the pixels in a **glDrawPixels** command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="43156-227">Die [**glpixelstore**](glpixelstore-functions.md) -und [**glpixeltransfer**](glpixeltransfer.md) -Modi wirken sich auf Textur Bilder genau so aus, wie Sie sich auf **gldrawpixels** auswirken.</span><span class="sxs-lookup"><span data-stu-id="43156-227">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="43156-228">Ein Textur Bild, bei dem die Höhe oder Breite null ist, gibt die NULL-Textur an</span><span class="sxs-lookup"><span data-stu-id="43156-228">A texture image with zero height or width indicates the null texture.</span></span> <span data-ttu-id="43156-229">Wenn die NULL-Textur für die Detailebene 0 angegeben wird, ist dies so, als ob die Texturierung deaktiviert wäre.</span><span class="sxs-lookup"><span data-stu-id="43156-229">If the null texture is specified for level-of-detail 0, it is as if texturing were disabled.</span></span>

<span data-ttu-id="43156-230">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glTexImage2D** ab:</span><span class="sxs-lookup"><span data-stu-id="43156-230">The following functions retrieve information related to **glTexImage2D**:</span></span>

[<span data-ttu-id="43156-231">**glgetteximage**</span><span class="sxs-lookup"><span data-stu-id="43156-231">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="43156-232">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Textur \_ 2D</span><span class="sxs-lookup"><span data-stu-id="43156-232">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="43156-233">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43156-233">Requirements</span></span>



| <span data-ttu-id="43156-234">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43156-234">Requirement</span></span> | <span data-ttu-id="43156-235">Wert</span><span class="sxs-lookup"><span data-stu-id="43156-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43156-236">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43156-236">Minimum supported client</span></span><br/> | <span data-ttu-id="43156-237">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43156-237">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="43156-238">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43156-238">Minimum supported server</span></span><br/> | <span data-ttu-id="43156-239">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43156-239">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="43156-240">Header</span><span class="sxs-lookup"><span data-stu-id="43156-240">Header</span></span><br/>                   | <dl> <span data-ttu-id="43156-241"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="43156-241"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="43156-242">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="43156-242">Library</span></span><br/>                  | <dl> <span data-ttu-id="43156-243"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43156-243"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="43156-244">DLL</span><span class="sxs-lookup"><span data-stu-id="43156-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43156-245"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43156-245"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43156-246">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43156-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43156-247">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="43156-247">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="43156-248">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="43156-248">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="43156-249">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="43156-249">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="43156-250">**glnebel**</span><span class="sxs-lookup"><span data-stu-id="43156-250">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="43156-251">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="43156-251">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="43156-252">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="43156-252">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="43156-253">**glpixeltransfer**</span><span class="sxs-lookup"><span data-stu-id="43156-253">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="43156-254">**gltexd**</span><span class="sxs-lookup"><span data-stu-id="43156-254">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="43156-255">**gltexgen**</span><span class="sxs-lookup"><span data-stu-id="43156-255">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="43156-256">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="43156-256">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="43156-257">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="43156-257">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





