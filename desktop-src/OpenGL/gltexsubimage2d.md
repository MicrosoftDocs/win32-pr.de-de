---
title: glTexSubImage2D-Funktion (GL. h)
description: Die glTexSubImage2D-Funktion gibt einen Teil eines vorhandenen eindimensionalen Textur Bilds an. Sie können keine neue Textur mit glTexSubImage2D definieren.
ms.assetid: 2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7
keywords:
- glTexSubImage2D-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a0a59ae9e6724386cb2f7891a14e4bf9d4c1a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342180"
---
# <a name="gltexsubimage2d-function"></a><span data-ttu-id="c87df-105">glTexSubImage2D-Funktion</span><span class="sxs-lookup"><span data-stu-id="c87df-105">glTexSubImage2D function</span></span>

<span data-ttu-id="c87df-106">Die **glTexSubImage2D** -Funktion gibt einen Teil eines vorhandenen eindimensionalen Textur Bilds an.</span><span class="sxs-lookup"><span data-stu-id="c87df-106">The **glTexSubImage2D** function specifies a portion of an existing one-dimensional texture image.</span></span> <span data-ttu-id="c87df-107">Sie können keine neue Textur mit **glTexSubImage2D** definieren.</span><span class="sxs-lookup"><span data-stu-id="c87df-107">You cannot define a new texture with **glTexSubImage2D**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c87df-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c87df-108">Syntax</span></span>


```C++
void WINAPI glTexSubImage2D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLint   yoffset,
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="c87df-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c87df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c87df-110">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="c87df-110">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="c87df-111">Die Ziel Textur.</span><span class="sxs-lookup"><span data-stu-id="c87df-111">The target texture.</span></span> <span data-ttu-id="c87df-112">Muss "GL \_ Texture \_ 2D" lauten.</span><span class="sxs-lookup"><span data-stu-id="c87df-112">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="c87df-113">*level*</span><span class="sxs-lookup"><span data-stu-id="c87df-113">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="c87df-114">Die Detailebene.</span><span class="sxs-lookup"><span data-stu-id="c87df-114">The level-of-detail number.</span></span> <span data-ttu-id="c87df-115">Ebene 0 ist das Basis Image.</span><span class="sxs-lookup"><span data-stu-id="c87df-115">Level 0 is the base image.</span></span> <span data-ttu-id="c87df-116">Ebene *n* ist das *n*-te MipMap-Reduzierungs Bild.</span><span class="sxs-lookup"><span data-stu-id="c87df-116">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="c87df-117">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="c87df-117">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="c87df-118">Ein textOffset in der *x* -Richtung innerhalb des Textur Arrays.</span><span class="sxs-lookup"><span data-stu-id="c87df-118">A texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="c87df-119">*yoffset*</span><span class="sxs-lookup"><span data-stu-id="c87df-119">*yoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="c87df-120">Ein texteoffset in der *y* -Richtung innerhalb des Textur Arrays.</span><span class="sxs-lookup"><span data-stu-id="c87df-120">A texel offset in the *y* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="c87df-121">*width*</span><span class="sxs-lookup"><span data-stu-id="c87df-121">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="c87df-122">Die Breite des Textur unter Bilds.</span><span class="sxs-lookup"><span data-stu-id="c87df-122">The width of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="c87df-123">*height*</span><span class="sxs-lookup"><span data-stu-id="c87df-123">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="c87df-124">Die Höhe des Textur unter Bilds.</span><span class="sxs-lookup"><span data-stu-id="c87df-124">The height of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="c87df-125">*format*</span><span class="sxs-lookup"><span data-stu-id="c87df-125">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="c87df-126">Das Format der Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="c87df-126">The format of the pixel data.</span></span> <span data-ttu-id="c87df-127">Es kann einen der folgenden symbolischen Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="c87df-127">It can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="c87df-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c87df-128">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="c87df-129">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c87df-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="c87df-130"><dt>**GL- \_ Farb \_ Index**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-130"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="c87df-131">Jedes Element ist ein einzelner Wert, ein Farbindex.</span><span class="sxs-lookup"><span data-stu-id="c87df-131">Each element is a single value, a color index.</span></span> <span data-ttu-id="c87df-132">Sie wird in ein festes Punkt Format (mit einer nicht angegebenen Anzahl von 0 Bits rechts neben dem binären Punkt) konvertiert, nach links oder rechts verschoben, abhängig vom Wert und Vorzeichen der GL \_ -Index \_ Verschiebung, und zum GL- \_ Index \_ Offset (siehe [**glpixeltransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="c87df-132">It is converted to fixed point format (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="c87df-133">Der resultierende Index wird mithilfe von GL \_ Pixel \_ map \_ i to \_ \_ R, GL \_ Pixel \_ map \_ i \_ to \_ G, GL \_ Pixel \_ map \_ i \_ to \_ B und GL Pixel Map i to a Tables in eine Gruppe von Farbkomponenten konvertiert \_ \_ \_ \_ \_ und an den Bereich \[ 0, 1 gebunden \] .</span><span class="sxs-lookup"><span data-stu-id="c87df-133">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="c87df-134"><dt>**GL. \_ rot**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-134"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="c87df-135">Jedes Element ist eine einzelne rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="c87df-135">Each element is a single red component.</span></span> <span data-ttu-id="c87df-136">Sie wird in ein Gleit Komma Format konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für Grün und blau und 1,0 für Alpha angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c87df-136">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="c87df-137">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.</span><span class="sxs-lookup"><span data-stu-id="c87df-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="c87df-138"><dt>**GL \_ grün**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-138"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="c87df-139">Jedes Element ist eine einzelne grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="c87df-139">Each element is a single green component.</span></span> <span data-ttu-id="c87df-140">Sie wird in ein Gleit Komma Format konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für "Red" und "Blue" und 1,0 für Alpha angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="c87df-140">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="c87df-141">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe [**glpixeltransfer**](glpixeltransfer.md)) gebunden.</span><span class="sxs-lookup"><span data-stu-id="c87df-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="c87df-142"><dt>**GL \_ blau**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-142"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="c87df-143">Jedes Element ist eine einzelne blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="c87df-143">Each element is a single blue component.</span></span> <span data-ttu-id="c87df-144">Sie wird in ein Gleit Komma Format konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für Rot und grün und 1,0 für Alpha angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c87df-144">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="c87df-145">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.</span><span class="sxs-lookup"><span data-stu-id="c87df-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="c87df-146"><dt>**GL- \_ Alpha**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-146"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="c87df-147">Jedes Element ist eine einzelne Alpha Komponente.</span><span class="sxs-lookup"><span data-stu-id="c87df-147">Each element is a single alpha component.</span></span> <span data-ttu-id="c87df-148">Sie wird in ein Gleit Komma Format konvertiert und in ein RGBA-Element zusammengefasst, indem 0,0 für Rot, grün und blau angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c87df-148">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="c87df-149">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe [**glpixeltransfer**](glpixeltransfer.md)) gebunden.</span><span class="sxs-lookup"><span data-stu-id="c87df-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="c87df-150"><dt>**GL. \_ RGB**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-150"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="c87df-151">Jedes Element ist ein RGB-Triple.</span><span class="sxs-lookup"><span data-stu-id="c87df-151">Each element is an RGB triple.</span></span> <span data-ttu-id="c87df-152">Sie wird in ein Gleit Komma Format konvertiert und in ein RGBA-Element zusammengefasst, indem 1,0 für Alpha angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c87df-152">It is converted to floating point format and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="c87df-153">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.</span><span class="sxs-lookup"><span data-stu-id="c87df-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="c87df-154"><dt>**GL \_ RGBA**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-154"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="c87df-155">Jedes Element ist ein umfassendes RGBA-Element.</span><span class="sxs-lookup"><span data-stu-id="c87df-155">Each element is a complete RGBA element.</span></span> <span data-ttu-id="c87df-156">Der Wert wird in einen Gleit Komma Wert konvertiert.</span><span class="sxs-lookup"><span data-stu-id="c87df-156">It is converted to floating point.</span></span> <span data-ttu-id="c87df-157">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.</span><span class="sxs-lookup"><span data-stu-id="c87df-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="c87df-158"><dt>**GL- \_ Beleuchtung**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-158"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="c87df-159">Jedes Element ist ein einzelner Wert für die Leuchtkraft.</span><span class="sxs-lookup"><span data-stu-id="c87df-159">Each element is a single luminance value.</span></span> <span data-ttu-id="c87df-160">Sie wird in das Gleit Komma Format konvertiert und dann in einem RGBA-Element zusammengefasst, indem der Wert für die Leuchtkraft dreimal für Rot, grün und blau replizieren und 1,0 für Alpha angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c87df-160">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="c87df-161">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe [**glpixeltransfer**](glpixeltransfer.md)) gebunden.</span><span class="sxs-lookup"><span data-stu-id="c87df-161">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="c87df-162"><dt>**GL- \_ Leuchtkraft \_ Alpha**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-162"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="c87df-163">Jedes Element ist ein leuchtendes/Alpha-Paar.</span><span class="sxs-lookup"><span data-stu-id="c87df-163">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="c87df-164">Sie wird in das Gleit Komma Format konvertiert und dann in einem RGBA-Element zusammengefasst, indem der Wert für die Leuchtkraft dreimal für Rot, grün und blau replizieren wird.</span><span class="sxs-lookup"><span data-stu-id="c87df-164">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="c87df-165">Jede Komponente wird dann mit der signierten Skalierungsfaktor-GL \_ c \_ -Skala multipliziert, dem signierten Bias \_ -GL \_ -c-Bias hinzugefügt und an den Bereich \[ 0, 1 \] (siehe **glpixeltransfer**) gebunden.</span><span class="sxs-lookup"><span data-stu-id="c87df-165">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="c87df-166">*type*</span><span class="sxs-lookup"><span data-stu-id="c87df-166">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="c87df-167">Der Datentyp der Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="c87df-167">The data type of the pixel data.</span></span> <span data-ttu-id="c87df-168">Die folgenden symbolischen Werte werden akzeptiert: GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ Bitmap, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int und GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="c87df-168">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="c87df-169">*Pixel*</span><span class="sxs-lookup"><span data-stu-id="c87df-169">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="c87df-170">Ein Zeiger auf die Bilddaten im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c87df-170">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c87df-171">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c87df-171">Return value</span></span>

<span data-ttu-id="c87df-172">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c87df-172">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c87df-173">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c87df-173">Error codes</span></span>

<span data-ttu-id="c87df-174">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c87df-174">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c87df-175">Name</span><span class="sxs-lookup"><span data-stu-id="c87df-175">Name</span></span>                                                                                                  | <span data-ttu-id="c87df-176">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c87df-176">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c87df-177"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-177"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c87df-178">*Ziel* war nicht gl \_ Texture \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="c87df-178">*target* was not GL\_TEXTURE\_2D.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="c87df-179"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-179"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c87df-180">Das *Format* war keine akzeptierte Konstante.</span><span class="sxs-lookup"><span data-stu-id="c87df-180">*format* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="c87df-181"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-181"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c87df-182">der *Typ* war keine akzeptierte Konstante.</span><span class="sxs-lookup"><span data-stu-id="c87df-182">*type* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="c87df-183"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-183"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c87df-184">*Typ* : GL \_ Bitmap und *Format* war kein GL \_ - \_ Farbindex.</span><span class="sxs-lookup"><span data-stu-id="c87df-184">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="c87df-185"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-185"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="c87df-186">die *Ebene* war kleiner als 0 (null) oder größer als log2 *Max*, wobei *Max* der zurückgegebene Wert von GL \_ Max \_ Texture \_ size war.</span><span class="sxs-lookup"><span data-stu-id="c87df-186">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="c87df-187"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-187"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="c87df-188">*xoffset* war kleiner als-*b*; oder *die xoffset*-  +  *Breite* war größer als *w*  -  *b*; oder *yoffset* war kleiner als-*b*; oder die *yoffset*-  +  *Höhe* war größer als *h*  -  *b*, wobei *w* für die GL- \_ Textur \_ Breite, *h* die Höhe von GL ist, \_ \_ und *b* die Breite des GL- \_ Textur Rahmens \_ des zu ändernden Textur Bilds.</span><span class="sxs-lookup"><span data-stu-id="c87df-188">*xoffset* was less than -*b*; or *xoffset* + *width* was greater than *w* - *b*; or *yoffset* was less than -*b*; or *yoffset* + *height* was greater than *h* - *b*, where *w* is the GL\_TEXTURE\_WIDTH, *h* is the GL\_TEXTURE\_HEIGHT, and *b* is the width of the GL\_TEXTURE\_BORDER of the texture image being modified.</span></span> <br/> <span data-ttu-id="c87df-189">Beachten Sie, dass *w* und *h* die doppelte Rahmenbreite enthalten.</span><span class="sxs-lookup"><span data-stu-id="c87df-189">Note that *w* and *h* include twice the border width.</span></span><br/> |
| <dl> <span data-ttu-id="c87df-190"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-190"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="c87df-191">die *Breite* war kleiner als *b*, wobei *b* die Rahmenbreite des Textur Arrays ist.</span><span class="sxs-lookup"><span data-stu-id="c87df-191">*width* was was less than *b*, where *b* is the border width of the texture array.</span></span><br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="c87df-192"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-192"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="c87df-193">der *Rahmen war nicht* 0 (null) oder 1.</span><span class="sxs-lookup"><span data-stu-id="c87df-193">*border* was not zero or 1.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="c87df-194"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-194"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c87df-195">Das Textur Array wurde nicht durch einen vorherigen **glTexImage2D** -Vorgang definiert.</span><span class="sxs-lookup"><span data-stu-id="c87df-195">The texture array was not defined by a previous **glTexImage2D** operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="c87df-196"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-196"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c87df-197">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c87df-197">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                                                                                                                                                        |



## <a name="remarks"></a><span data-ttu-id="c87df-198">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c87df-198">Remarks</span></span>

<span data-ttu-id="c87df-199">Zweidimensionale Texturierung für ein primitiv wird mithilfe von [**glEnable**](glenable.md) und **glEnable** mit dem Argument GL \_ Texture \_ 2D aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c87df-199">Two-dimensional texturing for a primitive is enabled using [**glEnable**](glenable.md) and **glDisable** with the argument GL\_TEXTURE\_2D.</span></span> <span data-ttu-id="c87df-200">Während der Texturierung wird ein Teil eines angegebenen Textur Bilds jedem aktivierten primitiven zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c87df-200">During texturing, part of a specified texture image is mapped into each enabled primitive.</span></span> <span data-ttu-id="c87df-201">Verwenden Sie die **glTexSubImage2D** -Funktion, um ein zusammenhängendes unter Bild eines vorhandenen zweidimensionalen Textur Bilds für die Texturierung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c87df-201">You use the **glTexSubImage2D** function to specify a contiguous sub-image of an existing two-dimensional texture image for texturing.</span></span>

<span data-ttu-id="c87df-202">Die texeln, auf die durch *Pixel* verwiesen wird, ersetzen einen Bereich des vorhandenen Textur Arrays durch *x* -Indizes von *xoffset* und *xoffset* + (*Width* 1) inklusive und *y* -Indizes von *yoffset* und *yoffset* + (*height* 1) einschließlich.</span><span class="sxs-lookup"><span data-stu-id="c87df-202">The texels referenced by *pixels* replace a region of the existing texture array with *x* indexes of *xoffset* and *xoffset* + (*width* 1) inclusive and *y* indexes of *yoffset* and *yoffset* + (*height* 1) inclusive.</span></span> <span data-ttu-id="c87df-203">Dieser Bereich darf keine texeln außerhalb des Bereichs des ursprünglich angegebenen Textur Arrays enthalten.</span><span class="sxs-lookup"><span data-stu-id="c87df-203">This region cannot include any texels outside the range of the originally specified texture array.</span></span>

<span data-ttu-id="c87df-204">Die Angabe eines unter Bilds mit einer *Breite* von 0 (null) hat keine Auswirkung und generiert keinen Fehler.</span><span class="sxs-lookup"><span data-stu-id="c87df-204">Specifying a sub-image with a *width* of zero has no effect and does not generate an error.</span></span>

<span data-ttu-id="c87df-205">Die Texturierung hat keine Auswirkung auf den Farb Index Modus.</span><span class="sxs-lookup"><span data-stu-id="c87df-205">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="c87df-206">Im Allgemeinen können Textur Bilder durch die gleichen Datenformate wie die Pixel in einem [**gldrawpixels**](gldrawpixels.md) -Befehl dargestellt werden, mit dem Unterschied, dass der GL \_ \_ -Schablone-Index und die GL- \_ tiefen \_ Komponente nicht verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c87df-206">In general, texture images can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="c87df-207">Die [**glpixelstore**](glpixelstore-functions.md) -und [**glpixeltransfer**](glpixeltransfer.md) -Modi wirken sich auf Textur Bilder genau so aus, wie Sie sich auf **gldrawpixels** auswirken.</span><span class="sxs-lookup"><span data-stu-id="c87df-207">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="c87df-208">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glTexSubImage2D** ab:</span><span class="sxs-lookup"><span data-stu-id="c87df-208">The following functions retrieve information related to **glTexSubImage2D**:</span></span>

[<span data-ttu-id="c87df-209">**glgetteximage**</span><span class="sxs-lookup"><span data-stu-id="c87df-209">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="c87df-210">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Textur \_ 2D</span><span class="sxs-lookup"><span data-stu-id="c87df-210">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="c87df-211">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c87df-211">Requirements</span></span>



| <span data-ttu-id="c87df-212">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c87df-212">Requirement</span></span> | <span data-ttu-id="c87df-213">Wert</span><span class="sxs-lookup"><span data-stu-id="c87df-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c87df-214">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c87df-214">Minimum supported client</span></span><br/> | <span data-ttu-id="c87df-215">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c87df-215">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c87df-216">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c87df-216">Minimum supported server</span></span><br/> | <span data-ttu-id="c87df-217">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c87df-217">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c87df-218">Header</span><span class="sxs-lookup"><span data-stu-id="c87df-218">Header</span></span><br/>                   | <dl> <span data-ttu-id="c87df-219"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-219"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c87df-220">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c87df-220">Library</span></span><br/>                  | <dl> <span data-ttu-id="c87df-221"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-221"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c87df-222">DLL</span><span class="sxs-lookup"><span data-stu-id="c87df-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c87df-223"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c87df-223"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c87df-224">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c87df-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c87df-225">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="c87df-225">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="c87df-226">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="c87df-226">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="c87df-227">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="c87df-227">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="c87df-228">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="c87df-228">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="c87df-229">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="c87df-229">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="c87df-230">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="c87df-230">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="c87df-231">**glnebel**</span><span class="sxs-lookup"><span data-stu-id="c87df-231">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="c87df-232">**glgetteximage**</span><span class="sxs-lookup"><span data-stu-id="c87df-232">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="c87df-233">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="c87df-233">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="c87df-234">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="c87df-234">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="c87df-235">**glpixeltransfer**</span><span class="sxs-lookup"><span data-stu-id="c87df-235">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="c87df-236">**gltexd**</span><span class="sxs-lookup"><span data-stu-id="c87df-236">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="c87df-237">**gltexgen**</span><span class="sxs-lookup"><span data-stu-id="c87df-237">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="c87df-238">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="c87df-238">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="c87df-239">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="c87df-239">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="c87df-240">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="c87df-240">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="c87df-241">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="c87df-241">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="c87df-242">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="c87df-242">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





