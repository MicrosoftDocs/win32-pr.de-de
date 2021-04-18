---
title: glgetcolortableext-Funktion (GL. h)
description: Die glgetcolortableext-Funktion Ruft die Farbtabellen Daten der aktuellen Ziel Texturpalette ab.
ms.assetid: 9169c4e1-a22e-48fe-bd45-4549c1a10ff0
keywords:
- glgetcolortableext-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811dc53b32c937970fbef8d87fa9a2ef4eb8b978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343894"
---
# <a name="glgetcolortableext-function"></a><span data-ttu-id="f9fd7-104">glgetcolortableext-Funktion</span><span class="sxs-lookup"><span data-stu-id="f9fd7-104">glGetColorTableEXT function</span></span>

<span data-ttu-id="f9fd7-105">Die **glgetcolortableext** -Funktion Ruft die Farbtabellen Daten der aktuellen Ziel Texturpalette ab.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-105">The **glGetColorTableEXT** function gets the color table data of the current targeted texture palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9fd7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9fd7-106">Syntax</span></span>


```C++
void WINAPI glGetColorTableEXT(
         GLenum target,
         GLenum format,
         GLenum type,
   const GLvoid *data
);
```



## <a name="parameters"></a><span data-ttu-id="f9fd7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9fd7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9fd7-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="f9fd7-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fd7-109">Die Ziel Textur, deren Palette geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-109">The target texture that is to have its palette changed.</span></span> <span data-ttu-id="f9fd7-110">Muss Textur \_ 1D oder Textur \_ 2D sein.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-110">Must be TEXTURE\_1D or TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="f9fd7-111">*format*</span><span class="sxs-lookup"><span data-stu-id="f9fd7-111">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fd7-112">Das Format der Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-112">The format of the pixel data.</span></span> <span data-ttu-id="f9fd7-113">Die folgenden symbolischen Konstanten werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-113">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9fd7-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f9fd7-114">Value</span></span></th>
<th><span data-ttu-id="f9fd7-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f9fd7-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="f9fd7-116"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9fd7-116"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f9fd7-117">Jedes Pixel ist eine Gruppe von vier Komponenten in der folgenden Reihenfolge: rot, grün, blau, alpha.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-117">Each pixel is a group of four components in the following order: red, green, blue, alpha.</span></span> <span data-ttu-id="f9fd7-118">Das RGBA-Format wird auf diese Weise bestimmt:</span><span class="sxs-lookup"><span data-stu-id="f9fd7-118">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="f9fd7-119">Die Funktion " <strong>glgetcolortableext</strong> " konvertiert Gleit Komma Werte direkt in ein internes Format mit einer nicht spezifizierten Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-119">The <strong>glGetColorTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="f9fd7-120">Ganzzahlige Werte mit Vorzeichen werden linear dem internen Format zugeordnet, sodass der positivste darstellbare ganzzahlige Wert 1,0 und der negativste darstellbare ganzzahlige Wert-1,0 zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-120">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable integer value maps to -1.0.</span></span> <span data-ttu-id="f9fd7-121">Ganzzahlige Daten ohne Vorzeichen werden ähnlich zugeordnet: der größte ganzzahlige Wert ist 1,0, und NULL wird 0,0 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-121">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="f9fd7-122">Die Funktion " <strong>glgetcolortableext</strong> " multipliziert die resultierenden Farbwerte GL_c_SCALE und fügt Sie GL_c_BIAS hinzu, wobei <em>c</em> rot, grün, blau und Alpha für die jeweiligen Farbkomponenten ist.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-122">The <strong>glGetColorTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="f9fd7-123">Die Ergebnisse werden an den Bereich [0, 1] gebunden.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-123">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="f9fd7-124">Wenn GL_MAP_COLOR auf <strong>true</strong>festgelegt ist, skaliert <strong>glgetcolortableext</strong> jede Farbkomponente anhand der Größe der Nachschlage Tabelle GL_PIXEL_MAP_c_TO_c und ersetzt dann die Komponente durch den Wert, auf den Sie in dieser Tabelle verweist. <em>c</em> ist R, G, B bzw..</span><span class="sxs-lookup"><span data-stu-id="f9fd7-124">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glGetColorTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="f9fd7-125">Die Funktion " <strong>glgetcolortableext</strong> " konvertiert die resultierenden RGBA-Farben in Fragmente, indem die aktuelle Raster Position z-Koordinate und die Texturkoordinaten an jedes Pixel angefügt werden und dann dem <em>n</em>-ten Fragment, z. b. <em>x</em>, <em>x</em> -und <em>y</em> -Fenster Koordinaten zugewiesen werden?</span><span class="sxs-lookup"><span data-stu-id="f9fd7-125">The <strong>glGetColorTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position z-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment, such that <em>x</em>?</span></span><span data-ttu-id="f9fd7-126"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>Breite</em></span><span class="sxs-lookup"><span data-stu-id="f9fd7-126"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="f9fd7-127"><em>j</em>?</span><span class="sxs-lookup"><span data-stu-id="f9fd7-127"><em>y</em>?</span></span><span data-ttu-id="f9fd7-128"> = <em>y</em><sub>r</sub> + <em>n/Breite</em></span><span class="sxs-lookup"><span data-stu-id="f9fd7-128"> = <em>y</em><sub>r</sub> + <em>n/width</em></span></span><br/> <span data-ttu-id="f9fd7-129">Where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) ist die aktuelle Raster Position.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-129">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="f9fd7-130">Diese Pixel Fragmente werden dann wie die Fragmente behandelt, die durch rasterisierungspunkte, Linien oder Polygone generiert werden.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-130">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="f9fd7-131">Die <strong>glgetcolortableext</strong> -Funktion wendet Textur Zuordnung, Nebel und alle fragmentvorgänge an, bevor die Fragmente in den Framebuffer geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-131">The <strong>glGetColorTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="f9fd7-132"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9fd7-132"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f9fd7-133">Jedes Pixel ist eine einzelne rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-133">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="f9fd7-134">Die Funktion " <strong>glgetcolortableext</strong> " konvertiert diese Komponente auf die gleiche Weise in das interne Format wie die rote Komponente eines RGBA-Pixels, konvertiert Sie dann in ein RGBA-Pixel, wobei Grün und blau auf 0,0 und Alpha auf 1,0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-134">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="f9fd7-135">Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-135">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="f9fd7-136"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9fd7-136"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f9fd7-137">Jedes Pixel ist eine einzelne grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-137">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="f9fd7-138">Die Funktion " <strong>glgetcolortableext</strong> " konvertiert diese Komponente auf die gleiche Weise wie die grüne Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, bei dem "Red" und "Blue" auf "0,0" und "Alpha" auf 1,0 festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-138">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="f9fd7-139">Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-139">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="f9fd7-140"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9fd7-140"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f9fd7-141">Jedes Pixel ist eine einzelne blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-141">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="f9fd7-142">Die Funktion " <strong>glgetcolortableext</strong> " konvertiert diese Komponente auf die gleiche Weise in das interne Format wie die blaue Komponente eines RGBA-Pixels und konvertiert Sie dann in ein RGBA-Pixel, wobei "rot" und "grün" auf "0,0" und "Alpha" auf 1,0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-142">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="f9fd7-143">Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-143">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="f9fd7-144"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9fd7-144"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f9fd7-145">Jedes Pixel ist eine einzelne Alpha Komponente.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-145">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="f9fd7-146">Die Funktion " <strong>glgetcolortableext</strong> " konvertiert diese Komponente auf die gleiche Weise wie die Alpha Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, wobei rot, grün und blau auf 0,0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-146">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="f9fd7-147">Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-147">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="f9fd7-148"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9fd7-148"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f9fd7-149">Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: rot, grün, blau.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-149">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="f9fd7-150">Die Funktion " <strong>glgetcolortableext</strong> " konvertiert jede Komponente auf die gleiche Weise in das interne Format wie die roten, grünen und blauen Komponenten eines RGBA-Pixels.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-150">The <strong>glGetColorTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="f9fd7-151">Die Farbe Triple wird in ein RGBA-Pixel konvertiert, bei dem Alpha auf 1,0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-151">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="f9fd7-152">Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-152">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="f9fd7-153"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9fd7-153"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f9fd7-154">Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: blau, grün, rot.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-154">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="f9fd7-155">GL_BGR_EXT bietet ein Format, das dem Arbeitsspeicher Layout von Microsoft Windows-geräteunabhängigen Bitmaps (Disb) entspricht.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-155">GL_BGR_EXT provides a format that matches the memory layout of Microsoft Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="f9fd7-156">Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-156">Thus, your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="f9fd7-157"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9fd7-157"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f9fd7-158">Jedes Pixel ist eine Gruppe von vier Komponenten in dieser Reihenfolge: blau, grün, rot, alpha.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-158">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="f9fd7-159">GL_BGRA_EXT bietet ein Format, das dem Arbeitsspeicher Layout von Windows-geräteunabhängigen Bitmaps (Disb) entspricht.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-159">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="f9fd7-160">Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-160">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="f9fd7-161">*type*</span><span class="sxs-lookup"><span data-stu-id="f9fd7-161">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fd7-162">Der Datentyp für *Daten*.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-162">The data type for *data*.</span></span> <span data-ttu-id="f9fd7-163">Im folgenden finden Sie die akzeptierten symbolischen Konstanten und ihre Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-163">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="f9fd7-164">Wert</span><span class="sxs-lookup"><span data-stu-id="f9fd7-164">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="f9fd7-165">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f9fd7-165">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="f9fd7-166"><dt>**GL- \_ Byte ohne Vorzeichen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9fd7-166"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="f9fd7-167">8-Bit-Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="f9fd7-167">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="f9fd7-168"><dt>**GL \_ Byte**</dt></span><span class="sxs-lookup"><span data-stu-id="f9fd7-168"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="f9fd7-169">Ganze 8-Bit-Zahl mit Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="f9fd7-169">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="f9fd7-170"><dt>**GL \_ unsigned \_ Short**</dt></span><span class="sxs-lookup"><span data-stu-id="f9fd7-170"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="f9fd7-171">16-Bit-Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="f9fd7-171">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="f9fd7-172"><dt>**GL \_ Short**</dt></span><span class="sxs-lookup"><span data-stu-id="f9fd7-172"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="f9fd7-173">Ganze 16-Bit-Zahl mit Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="f9fd7-173">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="f9fd7-174"><dt>**GL \_ unsigned \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="f9fd7-174"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="f9fd7-175">32-Bit Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="f9fd7-175">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="f9fd7-176"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="f9fd7-176"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="f9fd7-177">32-bit integer</span><span class="sxs-lookup"><span data-stu-id="f9fd7-177">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="f9fd7-178"><dt>**GL \_ float**</dt></span><span class="sxs-lookup"><span data-stu-id="f9fd7-178"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="f9fd7-179">Gleitkommawert mit einfacher Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="f9fd7-179">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f9fd7-180">*data*</span><span class="sxs-lookup"><span data-stu-id="f9fd7-180">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fd7-181">Zeigt auf den Speicherort, an dem die zurückgegebenen Farbtabellen Informationen gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-181">Points to the location where returned color table information is to be stored.</span></span> <span data-ttu-id="f9fd7-182">Jeder Farbtabellen Eintrag wird so gespeichert, als ob es sich um ein einzelnes Pixel einer 1-D-Textur handelt.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-182">Each color table entry is stored as if it was a single pixel of a 1-D texture.</span></span> <span data-ttu-id="f9fd7-183">Da alle Texturen über eine Standardpalette verfügen, gibt **glgetcolortableext** immer Paletteninformationen zurück, auch wenn die Textur Daten nicht in einem Palettenformat vorliegen.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-183">Because all textures have a default palette, **glGetColorTableEXT** always returns palette information even if the texture data is not in a paletted format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9fd7-184">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9fd7-184">Return value</span></span>

<span data-ttu-id="f9fd7-185">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-185">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f9fd7-186">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f9fd7-186">Error codes</span></span>

<span data-ttu-id="f9fd7-187">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-187">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f9fd7-188">Name</span><span class="sxs-lookup"><span data-stu-id="f9fd7-188">Name</span></span>                                                                                                  | <span data-ttu-id="f9fd7-189">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f9fd7-189">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9fd7-190"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9fd7-190"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="f9fd7-191">*Ziel*, *Format* oder *Typ* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-191">*target*, *format*, or *type* was not an accepted value.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="f9fd7-192"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="f9fd7-192"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f9fd7-193">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-193">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f9fd7-194">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9fd7-194">Remarks</span></span>

<span data-ttu-id="f9fd7-195">Die Funktion " **glgetcolortableext** " Ruft die tatsächlichen Farbtabellen Daten ab, die von [**glcolortableext**](glcolortableext.md) und [**glcolorsubtableext**](glcolorsubtableext.md)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-195">The **glGetColorTableEXT** function gets the actual color table data specified by [**glColorTableEXT**](glcolortableext.md) and [**glColorSubTableEXT**](glcolorsubtableext.md).</span></span>

<span data-ttu-id="f9fd7-196">Bei der **glgetcolortableext** -Funktion handelt es sich um eine Erweiterungs Funktion, die nicht Teil der OpenGL-Standardbibliothek ist, aber Bestandteil der \_ \_ Struktur Erweiterung von GL ext ist \_ .</span><span class="sxs-lookup"><span data-stu-id="f9fd7-196">The **glGetColorTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="f9fd7-197">Um zu überprüfen, ob die Implementierung von OpenGL **glgetcolortableext** unterstützt, nennen Sie [**glgetstring**](glgetstring.md)(GL \_ Extensions).</span><span class="sxs-lookup"><span data-stu-id="f9fd7-197">To check whether your implementation of OpenGL supports **glGetColorTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="f9fd7-198">Wenn Sie die Struktur von GL ext in der Struktur zurückgibt \_ \_ \_ , wird **glgetcolortableext** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-198">If it returns GL\_EXT\_paletted\_texture, **glGetColorTableEXT** is supported.</span></span> <span data-ttu-id="f9fd7-199">Rufen Sie zum Abrufen der Funktions Adresse einer Erweiterungs Funktion [**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)auf.</span><span class="sxs-lookup"><span data-stu-id="f9fd7-199">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9fd7-200">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9fd7-200">Requirements</span></span>



| <span data-ttu-id="f9fd7-201">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9fd7-201">Requirement</span></span> | <span data-ttu-id="f9fd7-202">Wert</span><span class="sxs-lookup"><span data-stu-id="f9fd7-202">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="f9fd7-203">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9fd7-203">Minimum supported client</span></span><br/> | <span data-ttu-id="f9fd7-204">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9fd7-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="f9fd7-205">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9fd7-205">Minimum supported server</span></span><br/> | <span data-ttu-id="f9fd7-206">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9fd7-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f9fd7-207">Header</span><span class="sxs-lookup"><span data-stu-id="f9fd7-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9fd7-208"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9fd7-208"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9fd7-209">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9fd7-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9fd7-210">**glcolorsubtableext**</span><span class="sxs-lookup"><span data-stu-id="f9fd7-210">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="f9fd7-211">**glcolortableext**</span><span class="sxs-lookup"><span data-stu-id="f9fd7-211">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="f9fd7-212">**glgetcolortableparameterfvext**</span><span class="sxs-lookup"><span data-stu-id="f9fd7-212">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="f9fd7-213">**glgetcolortableparameterivext**</span><span class="sxs-lookup"><span data-stu-id="f9fd7-213">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="f9fd7-214">**wglgetprocaddress**</span><span class="sxs-lookup"><span data-stu-id="f9fd7-214">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





