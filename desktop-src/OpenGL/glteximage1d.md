---
title: glTexImage1D-Funktion (GL. h)
description: Die glTexImage1D-Funktion gibt ein eindimensionales Textur Bild an.
ms.assetid: 4f537b89-2ea2-4e2e-8c57-c372bf53f12c
keywords:
- glTexImage1D-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1865d19c54b9c59654f07162d2480aa5b29c47f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040477"
---
# <a name="glteximage1d-function"></a><span data-ttu-id="735cd-104">glTexImage1D-Funktion</span><span class="sxs-lookup"><span data-stu-id="735cd-104">glTexImage1D function</span></span>

<span data-ttu-id="735cd-105">Die **glTexImage1D** -Funktion gibt ein eindimensionales Textur Bild an.</span><span class="sxs-lookup"><span data-stu-id="735cd-105">The **glTexImage1D** function specifies a one-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="735cd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="735cd-106">Syntax</span></span>


```C++
void WINAPI glTexImage1D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="735cd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="735cd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="735cd-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="735cd-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="735cd-109">Die Ziel Textur.</span><span class="sxs-lookup"><span data-stu-id="735cd-109">The target texture.</span></span> <span data-ttu-id="735cd-110">Muss "GL \_ Texture \_ 1D" lauten.</span><span class="sxs-lookup"><span data-stu-id="735cd-110">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="735cd-111">*level*</span><span class="sxs-lookup"><span data-stu-id="735cd-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="735cd-112">Die Detailebene.</span><span class="sxs-lookup"><span data-stu-id="735cd-112">The level-of-detail number.</span></span> <span data-ttu-id="735cd-113">Ebene 0 ist die Basis Image Ebene.</span><span class="sxs-lookup"><span data-stu-id="735cd-113">Level 0 is the base image level.</span></span> <span data-ttu-id="735cd-114">Ebene *n* ist das *n*-te MipMap-Reduzierungs Bild.</span><span class="sxs-lookup"><span data-stu-id="735cd-114">Level *n* is the *n* Th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="735cd-115">*internalformat*</span><span class="sxs-lookup"><span data-stu-id="735cd-115">*internalformat*</span></span> 
</dt> <dd>

<span data-ttu-id="735cd-116">Gibt die Anzahl der Farbkomponenten in der Textur an.</span><span class="sxs-lookup"><span data-stu-id="735cd-116">Specifies the number of color components in the texture.</span></span> <span data-ttu-id="735cd-117">Muss 1, 2, 3 oder 4 sein oder eine der folgenden symbolischen Konstanten sein: GL \_ Alpha, GL \_ ALPHA4, GL \_ ALPHA8, GL \_ ALPHA12, GL \_ ALPHA16, GL \_ Luminance, GL \_ LUMINANCE4, GL \_ LUMINANCE8, GL \_ LUMINANCE12, GL \_ LUMINANCE16, GL \_ Luminance \_ Alpha, GL \_ LUMINANCE4 \_ ALPHA4, GL \_ LUMINANCE6 \_ ALPHA2, GL \_ LUMINANCE8 \_ ALPHA8, GL \_ LUMINANCE12 \_ ALPHA4, GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 \_ ALPHA16, GL \_ Intensität, GL \_ INTENSITY4, GL \_ INTENSITY8, GL \_ INTENSITY12, GL \_ INTENSITY16, GL \_ RGB, GL \_ R3 \_ G3, GL RGB4 \_ \_ , GL \_ RGB5, GL \_ RGB8, GL \_ RGB10, GL \_ RGB12, GL \_ RGB16, GL \_ RGBA, GL \_ RGBA2, GL \_ RGBA4, GL \_ RGB5 \_ a1, GL \_ RGBA8, GL \_ RGB10 \_ a2, GL \_ RGBA12 oder GL \_ RGBA16.</span><span class="sxs-lookup"><span data-stu-id="735cd-117">Must be 1, 2, 3, or 4, or one of the following symbolic constants: GL\_ALPHA, GL\_ALPHA4, GL\_ALPHA8, GL\_ALPHA12, GL\_ALPHA16, GL\_LUMINANCE, GL\_LUMINANCE4, GL\_LUMINANCE8, GL\_LUMINANCE12, GL\_LUMINANCE16, GL\_LUMINANCE\_ALPHA, GL\_LUMINANCE4\_ALPHA4, GL\_LUMINANCE6\_ALPHA2, GL\_LUMINANCE8\_ALPHA8, GL\_LUMINANCE12\_ALPHA4, GL\_LUMINANCE12\_ALPHA12, GL\_LUMINANCE16\_ALPHA16, GL\_INTENSITY, GL\_INTENSITY4, GL\_INTENSITY8, GL\_INTENSITY12, GL\_INTENSITY16, GL\_RGB, GL\_R3\_G3\_B2, GL\_RGB4, GL\_RGB5, GL\_RGB8, GL\_RGB10, GL\_RGB12, GL\_RGB16, GL\_RGBA, GL\_RGBA2, GL\_RGBA4, GL\_RGB5\_A1, GL\_RGBA8, GL\_RGB10\_A2, GL\_RGBA12, or GL\_RGBA16.</span></span>

</dd> <dt>

<span data-ttu-id="735cd-118">*width*</span><span class="sxs-lookup"><span data-stu-id="735cd-118">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="735cd-119">Die Breite des Textur Bilds.</span><span class="sxs-lookup"><span data-stu-id="735cd-119">The width of the texture image.</span></span> <span data-ttu-id="735cd-120">Muss für eine Ganzzahl *n* 2 *n* + *2 (Rahmen* ) lauten.</span><span class="sxs-lookup"><span data-stu-id="735cd-120">Must be 2 *n* + 2( *border* ) for some integer *n*.</span></span> <span data-ttu-id="735cd-121">Die Höhe des Textur Bilds ist 1.</span><span class="sxs-lookup"><span data-stu-id="735cd-121">The height of the texture image is 1.</span></span>

</dd> <dt>

<span data-ttu-id="735cd-122">*Aun*</span><span class="sxs-lookup"><span data-stu-id="735cd-122">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="735cd-123">Die Breite des Rahmens.</span><span class="sxs-lookup"><span data-stu-id="735cd-123">The width of the border.</span></span> <span data-ttu-id="735cd-124">Muss entweder 0 oder 1 sein.</span><span class="sxs-lookup"><span data-stu-id="735cd-124">Must be either 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="735cd-125">*format*</span><span class="sxs-lookup"><span data-stu-id="735cd-125">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="735cd-126">Das Format der Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="735cd-126">The format of the pixel data.</span></span> <span data-ttu-id="735cd-127">Es kann einen von neun symbolischen Werten annehmen.</span><span class="sxs-lookup"><span data-stu-id="735cd-127">It can assume one of nine symbolic values.</span></span>



| <span data-ttu-id="735cd-128">Wert</span><span class="sxs-lookup"><span data-stu-id="735cd-128">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="735cd-129">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="735cd-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="735cd-130"><dt>**GL- \_ Farb \_ Index**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-130"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="735cd-131">Jedes Element ist ein einzelner Wert, ein Farbindex.</span><span class="sxs-lookup"><span data-stu-id="735cd-131">Each element is a single value, a color index.</span></span> <span data-ttu-id="735cd-132">Der Wert wird in einen festgelegten Punkt (mit einer nicht angegebenen Anzahl von 0 Bits rechts neben dem binären Punkt) konvertiert, je nach Wert und Vorzeichen der GL-Index Verschiebung nach links oder rechts verschoben \_ \_ und dem GL- \_ Index \_ Offset (siehe [**glpixeltransfer**](glpixeltransfer.md)) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="735cd-132">It is converted to fixed point (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="735cd-133">Der resultierende Index wird mithilfe von GL \_ Pixel \_ map \_ i to \_ \_ R, GL \_ Pixel \_ map \_ i \_ to \_ G, GL \_ Pixel \_ map \_ i \_ to \_ B und GL Pixel Map i to a Tables in eine Gruppe von Farbkomponenten konvertiert \_ \_ \_ \_ \_ und an den Bereich \[ 0, 1 gebunden \] .</span><span class="sxs-lookup"><span data-stu-id="735cd-133">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="735cd-134"><dt>**GL. \_ rot**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-134"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="735cd-135">Jedes Element ist eine einzelne rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="735cd-135">Each element is a single red component.</span></span> <span data-ttu-id="735cd-136">Sie wird in den Gleit Komma Wert konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für Grün und blau und 1,0 für Alpha angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="735cd-136">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="735cd-137">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.</span><span class="sxs-lookup"><span data-stu-id="735cd-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="735cd-138"><dt>**GL \_ grün**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-138"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="735cd-139">Jedes Element ist eine einzelne grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="735cd-139">Each element is a single green component.</span></span> <span data-ttu-id="735cd-140">Sie wird in den Gleit Komma Wert konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für "Red" und "Blue" und 1,0 für Alpha angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="735cd-140">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="735cd-141">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe [**glpixeltransfer**](glpixeltransfer.md)) gebunden.</span><span class="sxs-lookup"><span data-stu-id="735cd-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="735cd-142"><dt>**GL \_ blau**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-142"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="735cd-143">Jedes Element ist eine einzelne blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="735cd-143">Each element is a single blue component.</span></span> <span data-ttu-id="735cd-144">Sie wird in den Gleit Komma Wert konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für Rot und grün und 1,0 für Alpha angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="735cd-144">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="735cd-145">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.</span><span class="sxs-lookup"><span data-stu-id="735cd-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="735cd-146"><dt>**GL- \_ Alpha**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-146"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="735cd-147">Jedes Element ist eine einzelne rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="735cd-147">Each element is a single red component.</span></span> <span data-ttu-id="735cd-148">Sie wird in den Gleit Komma Wert konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für Rot, grün und blau angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="735cd-148">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="735cd-149">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe [**glpixeltransfer**](glpixeltransfer.md)) gebunden.</span><span class="sxs-lookup"><span data-stu-id="735cd-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                      |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="735cd-150"><dt>**GL. \_ RGB**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-150"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="735cd-151">Jedes Element ist ein RGB-Triple.</span><span class="sxs-lookup"><span data-stu-id="735cd-151">Each element is an RGB triple.</span></span> <span data-ttu-id="735cd-152">Sie wird in den Gleit Komma Wert konvertiert und in ein RGBA-Element zusammengefasst, indem 1,0 für Alpha angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="735cd-152">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="735cd-153">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.</span><span class="sxs-lookup"><span data-stu-id="735cd-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="735cd-154"><dt>**GL \_ RGBA**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-154"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="735cd-155">Jedes Element ist ein umfassendes RGBA-Element.</span><span class="sxs-lookup"><span data-stu-id="735cd-155">Each element is a complete RGBA element.</span></span> <span data-ttu-id="735cd-156">Der Wert wird in einen Gleit Komma Wert konvertiert.</span><span class="sxs-lookup"><span data-stu-id="735cd-156">It is converted to floating point.</span></span> <span data-ttu-id="735cd-157">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.</span><span class="sxs-lookup"><span data-stu-id="735cd-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="735cd-158"><dt>**GL \_ BGR \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-158"><dt>**GL\_BGR\_EXT**</dt></span></span> </dl>                         | <span data-ttu-id="735cd-159">Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: blau, grün, rot.</span><span class="sxs-lookup"><span data-stu-id="735cd-159">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="735cd-160">GL \_ BGR \_ ext bietet ein Format, das dem Arbeitsspeicher Layout von Windows-geräteunabhängigen Bitmaps (DIB) entspricht.</span><span class="sxs-lookup"><span data-stu-id="735cd-160">GL\_BGR\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="735cd-161">Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.</span><span class="sxs-lookup"><span data-stu-id="735cd-161">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="735cd-162"><dt>**GL \_ BGRA \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-162"><dt>**GL\_BGRA\_EXT**</dt></span></span> </dl>                      | <span data-ttu-id="735cd-163">Jedes Pixel ist eine Gruppe von vier Komponenten in dieser Reihenfolge: blau, grün, rot, alpha.</span><span class="sxs-lookup"><span data-stu-id="735cd-163">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="735cd-164">GL \_ BGRA \_ ext bietet ein Format, das dem Arbeitsspeicher Layout von Windows-geräteunabhängigen Bitmaps (DIB) entspricht.</span><span class="sxs-lookup"><span data-stu-id="735cd-164">GL\_BGRA\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="735cd-165">Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.</span><span class="sxs-lookup"><span data-stu-id="735cd-165">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="735cd-166"><dt>**GL- \_ Beleuchtung**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-166"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="735cd-167">Jedes Element ist ein einzelner Wert für die Leuchtkraft.</span><span class="sxs-lookup"><span data-stu-id="735cd-167">Each element is a single luminance value.</span></span> <span data-ttu-id="735cd-168">Sie wird in Gleit Komma Zahlen konvertiert und dann in einem RGBA-Element zusammengefasst, indem der Wert für die Leuchtkraft dreimal für Rot, grün und blau replizieren und 1,0 für Alpha angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="735cd-168">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="735cd-169">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe [**glpixeltransfer**](glpixeltransfer.md)) gebunden.</span><span class="sxs-lookup"><span data-stu-id="735cd-169">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="735cd-170"><dt>**GL- \_ Leuchtkraft \_ Alpha**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-170"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="735cd-171">Jedes Element ist ein leuchtendes/Alpha-Paar.</span><span class="sxs-lookup"><span data-stu-id="735cd-171">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="735cd-172">Sie wird in den Gleit Komma Wert konvertiert und dann in einem RGBA-Element zusammengefasst, indem der Wert für die Leuchtkraft drei Mal für Rot, grün und blau replizieren wird.</span><span class="sxs-lookup"><span data-stu-id="735cd-172">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="735cd-173">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.</span><span class="sxs-lookup"><span data-stu-id="735cd-173">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="735cd-174">*type*</span><span class="sxs-lookup"><span data-stu-id="735cd-174">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="735cd-175">Der Datentyp der Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="735cd-175">The data type of the pixel data.</span></span> <span data-ttu-id="735cd-176">Die folgenden symbolischen Werte werden akzeptiert: GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ Bitmap, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int und GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="735cd-176">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="735cd-177">*Pixel*</span><span class="sxs-lookup"><span data-stu-id="735cd-177">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="735cd-178">Ein Zeiger auf die Bilddaten im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="735cd-178">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="735cd-179">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="735cd-179">Return value</span></span>

<span data-ttu-id="735cd-180">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="735cd-180">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="735cd-181">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="735cd-181">Error codes</span></span>

<span data-ttu-id="735cd-182">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="735cd-182">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="735cd-183">Name</span><span class="sxs-lookup"><span data-stu-id="735cd-183">Name</span></span>                                                                                                  | <span data-ttu-id="735cd-184">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="735cd-184">Meaning</span></span>                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="735cd-185"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-185"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="735cd-186">Das *Ziel* war keine GL- \_ Textur.</span><span class="sxs-lookup"><span data-stu-id="735cd-186">*target* was not an GL\_TEXTURE.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="735cd-187"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-187"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="735cd-188">Das *Format* war keine akzeptierte *Format* Konstante.</span><span class="sxs-lookup"><span data-stu-id="735cd-188">*format* was not an accepted *format* constant.</span></span> <span data-ttu-id="735cd-189">Nur Format Konstanten außer dem GL \_ -Schablonen \_ Index und der GL- \_ tiefen \_ Komponente werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="735cd-189">Only format constants other than GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT are accepted.</span></span> <span data-ttu-id="735cd-190">Eine Liste möglicher Werte finden Sie in der Beschreibung des- *Formats* des-Parameters.</span><span class="sxs-lookup"><span data-stu-id="735cd-190">See the parameter description of *format* for a list of possible values.</span></span><br/> |
| <dl> <span data-ttu-id="735cd-191"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-191"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="735cd-192">der *Typ* war keine *typkonstante* .</span><span class="sxs-lookup"><span data-stu-id="735cd-192">*type* was not a *type* constant.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="735cd-193"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-193"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="735cd-194">*Typ* : GL \_ Bitmap und *Format* war kein GL \_ - \_ Farbindex.</span><span class="sxs-lookup"><span data-stu-id="735cd-194">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                        |
| <dl> <span data-ttu-id="735cd-195"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-195"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="735cd-196">die *Ebene* war kleiner als 0 (null) oder größer als log2 *Max*, wobei *Max* der zurückgegebene Wert von GL \_ Max \_ Texture \_ size war.</span><span class="sxs-lookup"><span data-stu-id="735cd-196">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="735cd-197"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-197"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="735cd-198">*internalformat* war nicht 1, 2, 3 oder 4.</span><span class="sxs-lookup"><span data-stu-id="735cd-198">*internalformat* was was not 1, 2, 3, or 4.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="735cd-199"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="735cd-200">die *Breite* war kleiner als 0 (null) oder größer als 2 + gl \_ . die maximale \_ Textur \_ Größe, oder Sie konnte nicht als 2 *n* + 2 (Rahmen) für einen ganzzahligen Wert von *n* dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="735cd-200">*width* was less than zero or greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or it could not be represented as 2 *n* + 2(border) for some integer value of *n*.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="735cd-201"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-201"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="735cd-202">der *Rahmen war nicht* 0 oder 1.</span><span class="sxs-lookup"><span data-stu-id="735cd-202">*border* was not 0 or 1.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="735cd-203"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-203"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="735cd-204">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="735cd-204">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                          |



## <a name="remarks"></a><span data-ttu-id="735cd-205">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="735cd-205">Remarks</span></span>

<span data-ttu-id="735cd-206">Die **glTexImage1D** -Funktion gibt ein eindimensionales Textur Bild an.</span><span class="sxs-lookup"><span data-stu-id="735cd-206">The **glTexImage1D** function specifies a one-dimensional texture image.</span></span> <span data-ttu-id="735cd-207">Bei der Texturierung wird ein Teil eines angegebenen *Textur Bilds* allen grafischen Primitiven zugeordnet, für die die Texturierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="735cd-207">Texturing maps a portion of a specified *texture image* onto each graphical primitive for which texturing is enabled.</span></span> <span data-ttu-id="735cd-208">Eindimensionale Texturierung wird mithilfe von " [**glEnable**](glenable.md) " und " **gldeaktivieren** " mit dem Argument "GL \_ Texture 1D" aktiviert und deaktiviert \_ .</span><span class="sxs-lookup"><span data-stu-id="735cd-208">One-dimensional texturing is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_TEXTURE\_1D.</span></span>

<span data-ttu-id="735cd-209">Textur Bilder werden mit **glTexImage1D** definiert.</span><span class="sxs-lookup"><span data-stu-id="735cd-209">Texture images are defined with **glTexImage1D**.</span></span> <span data-ttu-id="735cd-210">Die Argumente beschreiben die Parameter des Textur Bilds, z. b. Breite, Breite des Rahmens, Detailebene (siehe [**gltexparameter**](gltexparameter-functions.md)) und Anzahl der angegebenen Farbkomponenten.</span><span class="sxs-lookup"><span data-stu-id="735cd-210">The arguments describe the parameters of the texture image, such as width, width of the border, level-of-detail number (see [**glTexParameter**](gltexparameter-functions.md)), and number of color components provided.</span></span> <span data-ttu-id="735cd-211">Die letzten drei Argumente beschreiben die Darstellung des Bilds im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="735cd-211">The last three arguments describe the way the image is represented in memory.</span></span> <span data-ttu-id="735cd-212">Diese Argumente sind identisch mit den für [**gldrawpixels**](gldrawpixels.md)verwendeten Pixel Formaten.</span><span class="sxs-lookup"><span data-stu-id="735cd-212">These arguments are identical to the pixel formats used for [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="735cd-213">Daten werden je nach *Typ* aus *Pixel* als Sequenz von Bytes mit oder ohne Vorzeichen, Shorts oder Longs oder Gleit Komma Werten mit einfacher Genauigkeit gelesen.</span><span class="sxs-lookup"><span data-stu-id="735cd-213">Data is read from *pixels* as a sequence of signed or unsigned bytes, shorts or longs, or single-precision floating-point values, depending on *type*.</span></span> <span data-ttu-id="735cd-214">Diese Werte werden je nach *Format* in Mengen von einem, zwei, drei oder vier Werten gruppiert, um Elemente zu bilden.</span><span class="sxs-lookup"><span data-stu-id="735cd-214">These values are grouped into sets of one, two, three, or four values, depending on *format*, to form elements.</span></span> <span data-ttu-id="735cd-215">Wenn der *Typ* "GL \_ Bitmap" ist, werden die Daten als Zeichenfolge nicht signierter Bytes betrachtet (und das *Format* muss ein GL- \_ \_ Farbindex sein).</span><span class="sxs-lookup"><span data-stu-id="735cd-215">If *type* is GL\_BITMAP, the data is considered as a string of unsigned bytes (and *format* must be GL\_COLOR\_INDEX).</span></span> <span data-ttu-id="735cd-216">Jedes Daten Byte wird als 8 1-Bit-Elemente behandelt, wobei die bitanordnung zuerst von GL \_ Entpack- \_ lsb \_ (siehe [**glpixelstore**](glpixelstore-functions.md)) bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="735cd-216">Each data byte is treated as eight 1-bit elements, with bit ordering determined by GL\_UNPACK\_LSB\_FIRST (see [**glPixelStore**](glpixelstore-functions.md)).</span></span>

<span data-ttu-id="735cd-217">Ein Textur Bild kann je nach *Komponenten* bis zu vier Komponenten pro Textur Element aufweisen.</span><span class="sxs-lookup"><span data-stu-id="735cd-217">A texture image can have up to four components per texture element, depending on *components*.</span></span> <span data-ttu-id="735cd-218">Ein Textur Bild mit einer Komponente verwendet nur die rote Komponente der aus *Pixel* extrahierten RGBA-Farbe.</span><span class="sxs-lookup"><span data-stu-id="735cd-218">A one-component texture image uses only the red component of the RGBA color extracted from *pixels*.</span></span> <span data-ttu-id="735cd-219">Ein Image mit zwei Komponenten verwendet den R-Wert und einen-Wert.</span><span class="sxs-lookup"><span data-stu-id="735cd-219">A two-component image uses the R and A values.</span></span> <span data-ttu-id="735cd-220">Ein Image mit drei Komponenten verwendet die Werte R, G und B.</span><span class="sxs-lookup"><span data-stu-id="735cd-220">A three-component image uses the R, G, and B values.</span></span> <span data-ttu-id="735cd-221">Ein Image mit vier Komponenten verwendet alle RGBA-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="735cd-221">A four-component image uses all of the RGBA components.</span></span>

<span data-ttu-id="735cd-222">Die Texturierung hat keine Auswirkung auf den Farb Index Modus.</span><span class="sxs-lookup"><span data-stu-id="735cd-222">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="735cd-223">Das Textur Bild kann mit den gleichen Datenformaten dargestellt werden wie die Pixel in einem [**gldrawpixels**](gldrawpixels.md) -Befehl, mit dem Unterschied, dass der GL \_ \_ -Schablone-Index und die GL- \_ tiefen \_ Komponente nicht verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="735cd-223">The texture image can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="735cd-224">Die [**glpixelstore**](glpixelstore-functions.md) -und [**glpixeltransfer**](glpixeltransfer.md) -Modi wirken sich auf Textur Bilder genau so aus, wie Sie sich auf **gldrawpixels** auswirken.</span><span class="sxs-lookup"><span data-stu-id="735cd-224">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="735cd-225">Ein Textur Bild mit der Breite 0 (null) gibt die NULL Textur an.</span><span class="sxs-lookup"><span data-stu-id="735cd-225">A texture image with zero width indicates the null texture.</span></span> <span data-ttu-id="735cd-226">Wenn die NULL-Textur für die Detailebene 0 angegeben wird, ist dies so, als ob die Texturierung deaktiviert wäre.</span><span class="sxs-lookup"><span data-stu-id="735cd-226">If the null texture is specified for level-of-detail 0, it is as if texturing were disabled.</span></span>

<span data-ttu-id="735cd-227">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glteximageid** ab:</span><span class="sxs-lookup"><span data-stu-id="735cd-227">The following functions retrieve information related to **glTexImageID**:</span></span>

[<span data-ttu-id="735cd-228">**glgetteximage**</span><span class="sxs-lookup"><span data-stu-id="735cd-228">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="735cd-229">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Texture \_ 1D</span><span class="sxs-lookup"><span data-stu-id="735cd-229">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="735cd-230">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="735cd-230">Requirements</span></span>



| <span data-ttu-id="735cd-231">Anforderung</span><span class="sxs-lookup"><span data-stu-id="735cd-231">Requirement</span></span> | <span data-ttu-id="735cd-232">Wert</span><span class="sxs-lookup"><span data-stu-id="735cd-232">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="735cd-233">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="735cd-233">Minimum supported client</span></span><br/> | <span data-ttu-id="735cd-234">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="735cd-234">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="735cd-235">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="735cd-235">Minimum supported server</span></span><br/> | <span data-ttu-id="735cd-236">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="735cd-236">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="735cd-237">Header</span><span class="sxs-lookup"><span data-stu-id="735cd-237">Header</span></span><br/>                   | <dl> <span data-ttu-id="735cd-238"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-238"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="735cd-239">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="735cd-239">Library</span></span><br/>                  | <dl> <span data-ttu-id="735cd-240"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-240"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="735cd-241">DLL</span><span class="sxs-lookup"><span data-stu-id="735cd-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="735cd-242"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="735cd-242"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="735cd-243">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="735cd-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="735cd-244">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="735cd-244">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="735cd-245">**glcopypixels**</span><span class="sxs-lookup"><span data-stu-id="735cd-245">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="735cd-246">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="735cd-246">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="735cd-247">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="735cd-247">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="735cd-248">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="735cd-248">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="735cd-249">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="735cd-249">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="735cd-250">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="735cd-250">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="735cd-251">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="735cd-251">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="735cd-252">**glnebel**</span><span class="sxs-lookup"><span data-stu-id="735cd-252">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="735cd-253">**glgetteximage**</span><span class="sxs-lookup"><span data-stu-id="735cd-253">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="735cd-254">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="735cd-254">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="735cd-255">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="735cd-255">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="735cd-256">**glpixeltransfer**</span><span class="sxs-lookup"><span data-stu-id="735cd-256">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="735cd-257">**gltexd**</span><span class="sxs-lookup"><span data-stu-id="735cd-257">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="735cd-258">**gltexgen**</span><span class="sxs-lookup"><span data-stu-id="735cd-258">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="735cd-259">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="735cd-259">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="735cd-260">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="735cd-260">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="735cd-261">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="735cd-261">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="735cd-262">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="735cd-262">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





