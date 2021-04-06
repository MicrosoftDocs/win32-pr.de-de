---
title: glcolorsubtableext-Funktion (GL. h)
description: Die glcolorsubtableext-Funktion gibt einen Teil der zu ersetzenden Palette der Ziel Textur an.
ms.assetid: 21430245-f837-4c7a-944f-b44482254b12
keywords:
- glcolorsubtableext-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColorSubTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0386bda82bf08ae778d20b1be69858698ac7bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858981"
---
# <a name="glcolorsubtableext-function"></a><span data-ttu-id="e9e1a-104">glcolorsubtableext-Funktion</span><span class="sxs-lookup"><span data-stu-id="e9e1a-104">glColorSubTableEXT function</span></span>

<span data-ttu-id="e9e1a-105">Die **glcolorsubtableext** -Funktion gibt einen Teil der zu ersetzenden Palette der Ziel Textur an.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-105">The **glColorSubTableEXT** function specifies a portion of the targeted texture's palette to be replaced.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9e1a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9e1a-106">Syntax</span></span>


```C++
void WINAPI glColorSubTableEXT(
         GLenum  target,
         GLsizei start,
         GLsizei count,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a><span data-ttu-id="e9e1a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9e1a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9e1a-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="e9e1a-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="e9e1a-109">Die Zielstruktur, deren Palette geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-109">The target paletted texture that is to have its palette changed.</span></span> <span data-ttu-id="e9e1a-110">Muss Textur \_ 1D oder Textur \_ 2D sein.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-110">Must be TEXTURE\_1D or TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="e9e1a-111">*start*</span><span class="sxs-lookup"><span data-stu-id="e9e1a-111">*start*</span></span> 
</dt> <dd>

<span data-ttu-id="e9e1a-112">Der Eintrag für die Start Palette der Palette, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-112">The starting palette index entry of the palette to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="e9e1a-113">*count*</span><span class="sxs-lookup"><span data-stu-id="e9e1a-113">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="e9e1a-114">Die Anzahl der Palettenindex Einträge der Palette, die beginnend beim *Start* geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-114">The number of palette index entries of the palette to be changed beginning at *start*.</span></span> <span data-ttu-id="e9e1a-115">Der *count* -Parameter bestimmt den Bereich der Palettenindex Einträge, die geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-115">The *count* parameter determines the range of palette index entries that are changed.</span></span>

</dd> <dt>

<span data-ttu-id="e9e1a-116">*format*</span><span class="sxs-lookup"><span data-stu-id="e9e1a-116">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="e9e1a-117">Das Format der Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-117">The format of the pixel data.</span></span> <span data-ttu-id="e9e1a-118">Die folgenden symbolischen Konstanten werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-118">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9e1a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e9e1a-119">Value</span></span></th>
<th><span data-ttu-id="e9e1a-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e9e1a-120">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="e9e1a-121"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e9e1a-121"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e9e1a-122">Jedes Pixel ist eine Gruppe von vier Komponenten in der folgenden Reihenfolge: rot, grün, blau, alpha.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-122">Each pixel is a group of four components in the following order: red, green, blue, alpha.</span></span> <span data-ttu-id="e9e1a-123">Das RGBA-Format wird auf diese Weise bestimmt:</span><span class="sxs-lookup"><span data-stu-id="e9e1a-123">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="e9e1a-124">Mit der <strong>glcolorsubtableext</strong> -Funktion werden Gleit Komma Werte direkt in ein internes Format mit nicht spezifizierter Genauigkeit konvertiert.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-124">The <strong>glColorSubTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="e9e1a-125">Ganzzahlige Werte mit Vorzeichen werden linear dem internen Format zugeordnet, sodass der positivste darstellbare ganzzahlige Wert 1,0 zugeordnet wird und der negativere darstellbare Wert-1,0 zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-125">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="e9e1a-126">Ganzzahlige Daten ohne Vorzeichen werden ähnlich zugeordnet: der größte ganzzahlige Wert ist 1,0, und NULL wird 0,0 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-126">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="e9e1a-127">Die <strong>glcolorsubtableext</strong> -Funktion multipliziert die resultierenden Farbwerte GL_c_SCALE und fügt Sie GL_c_BIAS hinzu, wobei <em>c</em> rot, grün, blau und Alpha für die jeweiligen Farbkomponenten ist.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-127">The <strong>glColorSubTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="e9e1a-128">Die Ergebnisse werden an den Bereich [0, 1] gebunden.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-128">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="e9e1a-129">Wenn GL_MAP_COLOR auf <strong>true</strong>festgelegt ist, skaliert <strong>glcolorsubtableext</strong> jede Farbkomponente anhand der Größe der Such Tabelle GL_PIXEL_MAP_c_TO_c und ersetzt die Komponente dann durch den Wert, auf den Sie in dieser Tabelle verweist. <em>c</em> ist R, G, B bzw..</span><span class="sxs-lookup"><span data-stu-id="e9e1a-129">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glColorSubTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="e9e1a-130">Die <strong>glcolorsubtableext</strong> -Funktion konvertiert die resultierenden RGBA-Farben in Fragmente, indem die aktuelle Raster Position <em>z</em>-Koordinate und die Texturkoordinaten an jedes Pixel angefügt werden, und dann die <em>x</em> -und <em>y</em> -Fenster Koordinaten dem <em>n</em>-ten Fragment so<em>x</em>zugewiesen werden?</span><span class="sxs-lookup"><span data-stu-id="e9e1a-130">The <strong>glColorSubTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that<em>x</em>?</span></span><span data-ttu-id="e9e1a-131"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>Breite</em></span><span class="sxs-lookup"><span data-stu-id="e9e1a-131"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="e9e1a-132"><em>j</em>?</span><span class="sxs-lookup"><span data-stu-id="e9e1a-132"><em>y</em>?</span></span><span data-ttu-id="e9e1a-133"> = <em>y</em><sub>r</sub> +<em>n/Breite</em></span><span class="sxs-lookup"><span data-stu-id="e9e1a-133"> = <em>y</em><sub>r</sub> +<em>n / width</em></span></span><br/> <span data-ttu-id="e9e1a-134">Where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) ist die aktuelle Raster Position.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-134">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="e9e1a-135">Diese Pixel Fragmente werden dann wie die Fragmente behandelt, die durch rasterisierungspunkte, Linien oder Polygone generiert werden.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-135">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="e9e1a-136">Die <strong>glcolorsubtableext</strong> -Funktion wendet Textur Zuordnung, Nebel und alle fragmentvorgänge an, bevor die Fragmente in den Framebuffer geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-136">The <strong>glColorSubTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="e9e1a-137"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e9e1a-137"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e9e1a-138">Jedes Pixel ist eine einzelne rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-138">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="e9e1a-139">Die <strong>glcolorsubtableext</strong> -Funktion konvertiert diese Komponente auf die gleiche Weise wie die rote Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, bei dem Grün und blau auf 0,0 und Alpha auf 1,0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-139">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="e9e1a-140">Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-140">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="e9e1a-141"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e9e1a-141"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e9e1a-142">Jedes Pixel ist eine einzelne grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-142">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="e9e1a-143">Die Funktion " <strong>glcolorsubtableext</strong> " konvertiert diese Komponente auf die gleiche Weise wie die grüne Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, wobei "rot" und "blau" auf "0,0" und "Alpha" auf 1,0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-143">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="e9e1a-144">Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-144">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="e9e1a-145"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e9e1a-145"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e9e1a-146">Jedes Pixel ist eine einzelne blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-146">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="e9e1a-147">Die <strong>glcolorsubtableext</strong> -Funktion konvertiert diese Komponente auf die gleiche Weise wie die blaue Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, wobei rot und grün auf 0,0 und Alpha auf 1,0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-147">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="e9e1a-148">Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-148">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="e9e1a-149"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e9e1a-149"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e9e1a-150">Jedes Pixel ist eine einzelne Alpha Komponente.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-150">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="e9e1a-151">Die Funktion " <strong>glcolorsubtableext</strong> " konvertiert diese Komponente auf die gleiche Weise wie die Alpha Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, wobei rot, grün und blau auf 0,0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-151">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="e9e1a-152">Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-152">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="e9e1a-153"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e9e1a-153"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e9e1a-154">Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: rot, grün, blau.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-154">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="e9e1a-155">Die <strong>glcolorsubtableext</strong> -Funktion konvertiert jede Komponente auf die gleiche Weise in das interne Format wie die roten, grünen und blauen Komponenten eines RGBA-Pixels.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-155">The <strong>glColorSubTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="e9e1a-156">Die Farbe Triple wird in ein RGBA-Pixel konvertiert, bei dem Alpha auf 1,0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-156">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="e9e1a-157">Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-157">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="e9e1a-158"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e9e1a-158"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e9e1a-159">Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: blau, grün, rot.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-159">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="e9e1a-160">GL_BGR_EXT bietet ein Format, das dem Arbeitsspeicher Layout von Windows-geräteunabhängigen Bitmaps (Disb) entspricht.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-160">GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="e9e1a-161">Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-161">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="e9e1a-162"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e9e1a-162"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="e9e1a-163">Jedes Pixel ist eine Gruppe von vier Komponenten in dieser Reihenfolge: blau, grün, rot, alpha.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-163">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="e9e1a-164">GL_BGRA_EXT bietet ein Format, das dem Arbeitsspeicher Layout von Windows-geräteunabhängigen Bitmaps (Disb) entspricht.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-164">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="e9e1a-165">Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-165">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="e9e1a-166">*type*</span><span class="sxs-lookup"><span data-stu-id="e9e1a-166">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="e9e1a-167">Der Datentyp für *Daten*.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-167">The data type for *data*.</span></span> <span data-ttu-id="e9e1a-168">Die folgenden symbolischen Konstanten werden akzeptiert: GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int und GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-168">The following symbolic constants are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

<span data-ttu-id="e9e1a-169">In der folgenden Tabelle wird die Bedeutung der gültigen Konstanten für den *Typparameter* zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-169">The following table summarizes the meaning of the valid constants for the *type* parameter.</span></span>



| <span data-ttu-id="e9e1a-170">Wert</span><span class="sxs-lookup"><span data-stu-id="e9e1a-170">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="e9e1a-171">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e9e1a-171">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="e9e1a-172"><dt>**GL- \_ Byte ohne Vorzeichen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e9e1a-172"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="e9e1a-173">8-Bit-Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="e9e1a-173">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="e9e1a-174"><dt>**GL \_ Byte**</dt></span><span class="sxs-lookup"><span data-stu-id="e9e1a-174"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="e9e1a-175">Ganze 8-Bit-Zahl mit Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="e9e1a-175">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="e9e1a-176"><dt>**GL \_ unsigned \_ Short**</dt></span><span class="sxs-lookup"><span data-stu-id="e9e1a-176"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="e9e1a-177">16-Bit-Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="e9e1a-177">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="e9e1a-178"><dt>**GL \_ Short**</dt></span><span class="sxs-lookup"><span data-stu-id="e9e1a-178"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="e9e1a-179">Ganze 16-Bit-Zahl mit Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="e9e1a-179">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="e9e1a-180"><dt>**GL \_ unsigned \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="e9e1a-180"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="e9e1a-181">32-Bit Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="e9e1a-181">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="e9e1a-182"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="e9e1a-182"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="e9e1a-183">32-bit integer</span><span class="sxs-lookup"><span data-stu-id="e9e1a-183">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="e9e1a-184"><dt>**GL \_ float**</dt></span><span class="sxs-lookup"><span data-stu-id="e9e1a-184"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="e9e1a-185">Gleitkommawert mit einfacher Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="e9e1a-185">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e9e1a-186">*data*</span><span class="sxs-lookup"><span data-stu-id="e9e1a-186">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="e9e1a-187">Ein Zeiger auf die palettentextur Daten.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-187">A pointer to the paletted texture data.</span></span> <span data-ttu-id="e9e1a-188">Die Daten werden als einzelne Pixel eines 1-D-Textur paletteneintrags für einen Paletteneintrag behandelt.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-188">The data is treated as single pixels of a 1-D texture palette entry for a palette entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9e1a-189">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9e1a-189">Return value</span></span>

<span data-ttu-id="e9e1a-190">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-190">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e9e1a-191">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e9e1a-191">Error codes</span></span>

<span data-ttu-id="e9e1a-192">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-192">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e9e1a-193">Name</span><span class="sxs-lookup"><span data-stu-id="e9e1a-193">Name</span></span>                                                                                              | <span data-ttu-id="e9e1a-194">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e9e1a-194">Meaning</span></span>                                                                                                                               |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9e1a-195"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="e9e1a-195"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="e9e1a-196">*Start* oder *count* war eine ungültige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-196">*start* or *count* was an invalid integer.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="e9e1a-197"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e9e1a-197"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="e9e1a-198">*Ziel*, *Format* oder *Typ* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-198">*target*, *format*,or *type* was not an accepted value.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="e9e1a-199"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="e9e1a-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="e9e1a-200">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-200">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e9e1a-201">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9e1a-201">Remarks</span></span>

<span data-ttu-id="e9e1a-202">Die **glcolorsubtableext** -Funktion gibt Teile der zu ersetzenden Palette der aktuellen Zieltextur an.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-202">The **glColorSubTableEXT** function specifies portions of the current targeted texture's palette to be replaced.</span></span> <span data-ttu-id="e9e1a-203">Anders als bei [**glcolortableext**](glcolortableext.md)können Sie den *Ziel* Parameter nicht als Proxy Texturpalette angeben.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-203">Unlike [**glColorTableEXT**](glcolortableext.md), you cannot specify the *target* parameter to be a proxy texture palette.</span></span>

> [!Note]  
> <span data-ttu-id="e9e1a-204">Bei der **glcolorsubtableext** -Funktion handelt es sich um eine Erweiterungs Funktion, die nicht Teil der OpenGL-Standardbibliothek ist, aber Bestandteil der \_ \_ Struktur Erweiterung von GL ext ist \_ .</span><span class="sxs-lookup"><span data-stu-id="e9e1a-204">The **glColorSubTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="e9e1a-205">Um zu überprüfen, ob die Implementierung von OpenGL **glcolorsubtableext** unterstützt, nennen Sie [**glgetstring**](glgetstring.md)(GL \_ Extensions).</span><span class="sxs-lookup"><span data-stu-id="e9e1a-205">To check whether your implementation of OpenGL supports **glColorSubTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="e9e1a-206">Wenn Sie die Struktur "GL ext-Struktur" zurückgibt \_ \_ \_ , wird " **glcolorsubtableext** " unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-206">If it returns GL\_EXT\_paletted\_texture, **glColorSubTableEXT** is supported.</span></span> <span data-ttu-id="e9e1a-207">Rufen Sie zum Abrufen der Funktions Adresse einer Erweiterungs Funktion [**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)auf.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-207">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e9e1a-208">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9e1a-208">Requirements</span></span>



| <span data-ttu-id="e9e1a-209">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9e1a-209">Requirement</span></span> | <span data-ttu-id="e9e1a-210">Wert</span><span class="sxs-lookup"><span data-stu-id="e9e1a-210">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="e9e1a-211">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9e1a-211">Minimum supported client</span></span><br/> | <span data-ttu-id="e9e1a-212">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9e1a-212">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="e9e1a-213">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9e1a-213">Minimum supported server</span></span><br/> | <span data-ttu-id="e9e1a-214">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9e1a-214">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e9e1a-215">Header</span><span class="sxs-lookup"><span data-stu-id="e9e1a-215">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9e1a-216"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9e1a-216"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9e1a-217">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9e1a-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9e1a-218">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e9e1a-218">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e9e1a-219">**glcolortableext**</span><span class="sxs-lookup"><span data-stu-id="e9e1a-219">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="e9e1a-220">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e9e1a-220">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e9e1a-221">**glgetcolortableext**</span><span class="sxs-lookup"><span data-stu-id="e9e1a-221">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="e9e1a-222">**glgetcolortableparameterfvext**</span><span class="sxs-lookup"><span data-stu-id="e9e1a-222">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="e9e1a-223">**glgetcolortableparameterivext**</span><span class="sxs-lookup"><span data-stu-id="e9e1a-223">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="e9e1a-224">**glgetstring**</span><span class="sxs-lookup"><span data-stu-id="e9e1a-224">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="e9e1a-225">**wglgetprocaddress**</span><span class="sxs-lookup"><span data-stu-id="e9e1a-225">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





