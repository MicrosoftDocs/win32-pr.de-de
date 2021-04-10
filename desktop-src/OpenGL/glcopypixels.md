---
title: glcopypixels-Funktion (GL. h)
description: Die Funktion "glcopypixels" kopiert Pixel im Framebuffer.
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- glcopypixels-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCopyPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7ba0833534d21e48c251da6491fee2996c3ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956602"
---
# <a name="glcopypixels-function"></a><span data-ttu-id="81439-104">glcopypixels-Funktion</span><span class="sxs-lookup"><span data-stu-id="81439-104">glCopyPixels function</span></span>

<span data-ttu-id="81439-105">Die Funktion " **glcopypixels** " kopiert Pixel im Framebuffer.</span><span class="sxs-lookup"><span data-stu-id="81439-105">The **glCopyPixels** function copies pixels in the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="81439-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="81439-106">Syntax</span></span>


```C++
void WINAPI glCopyPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  type
);
```



## <a name="parameters"></a><span data-ttu-id="81439-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="81439-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81439-108">*x*</span><span class="sxs-lookup"><span data-stu-id="81439-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="81439-109">Die x-Ebenen-Koordinate der unteren linken Ecke des rechteckigen Bereichs, der kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="81439-109">The window x-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="81439-110">*y*</span><span class="sxs-lookup"><span data-stu-id="81439-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="81439-111">Die y-ebenenkoordinate des Fensters der unteren linken Ecke des rechteckigen Bereichs von Pixeln, die kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81439-111">The window y-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="81439-112">*width*</span><span class="sxs-lookup"><span data-stu-id="81439-112">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="81439-113">Die Width-Dimension des rechteckigen Bereichs von Pixeln, der kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="81439-113">The width dimension of the rectangular region of pixels to be copied.</span></span> <span data-ttu-id="81439-114">Darf nicht negativ sein.</span><span class="sxs-lookup"><span data-stu-id="81439-114">Must be nonnegative.</span></span>

</dd> <dt>

<span data-ttu-id="81439-115">*height*</span><span class="sxs-lookup"><span data-stu-id="81439-115">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="81439-116">Die Höhen Dimension des rechteckigen Bereichs von Pixeln, die kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="81439-116">The height dimension of the rectangular region of pixels to be copied.</span></span> <span data-ttu-id="81439-117">Darf nicht negativ sein.</span><span class="sxs-lookup"><span data-stu-id="81439-117">Must be nonnegative.</span></span>

</dd> <dt>

<span data-ttu-id="81439-118">*type*</span><span class="sxs-lookup"><span data-stu-id="81439-118">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="81439-119">Gibt an, ob **glcopypixels** Farbwerte, tiefen Werte oder Schablonen Werte kopieren soll.</span><span class="sxs-lookup"><span data-stu-id="81439-119">Specifies whether **glCopyPixels** is to copy color values, depth values, or stencil values.</span></span> <span data-ttu-id="81439-120">Die zulässigen symbolischen Konstanten sind.</span><span class="sxs-lookup"><span data-stu-id="81439-120">The acceptable symbolic constants are.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="81439-121">Wert</span><span class="sxs-lookup"><span data-stu-id="81439-121">Value</span></span></th>
<th><span data-ttu-id="81439-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="81439-122">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR"></span><span id="gl_color"></span><dl> <span data-ttu-id="81439-123"><dt><strong>GL_COLOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="81439-123"><dt><strong>GL_COLOR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="81439-124">Die Funktion " <strong>glcopypixels</strong> " liest Indizes oder RGBA-Farben aus dem Puffer, der derzeit als Lese Quell Puffer angegeben ist (siehe <a href="glreadbuffer.md"><strong>gllesebuffer</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="81439-124">The <strong>glCopyPixels</strong> function reads indexes or RGBA colors from the buffer currently specified as the read source buffer (see <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>).</span></span> <br/> <span data-ttu-id="81439-125">Wenn sich OpenGL im Farb Index Modus befindet:</span><span class="sxs-lookup"><span data-stu-id="81439-125">If OpenGL is in color-index mode:</span></span><br/>
<ol>
<li><span data-ttu-id="81439-126">Jeder aus diesem Puffer gelesene Index wird in ein fest Komma Format mit einer nicht angegebenen Anzahl von Bits auf der rechten Seite des Binär Punkts konvertiert.</span><span class="sxs-lookup"><span data-stu-id="81439-126">Each index that is read from this buffer is converted to a fixed-point format with an unspecified number of bits to the right of the binary point.</span></span></li>
<li><span data-ttu-id="81439-127">Jeder Index wird von GL_INDEX_SHIFT Bits nach links verschoben und GL_INDEX_OFFSET hinzugefügt. Wenn GL_INDEX_SHIFT negativ ist, befindet sich die UMSCHALTTASTE auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="81439-127">Each index is shifted left by GL_INDEX_SHIFT bits, and added to GL_INDEX_OFFSET.If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="81439-128">In beiden Fällen füllen Null Bits andernfalls nicht angegebene Bitpositionen im Ergebnis aus.</span><span class="sxs-lookup"><span data-stu-id="81439-128">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span><br/></li>
<li><span data-ttu-id="81439-129">Wenn GL_MAP_COLOR true ist, wird der Index durch den Wert ersetzt, auf den in der Nachschlage Tabelle GL_PIXEL_MAP_I_TO_I verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="81439-129">If GL_MAP_COLOR is true, the index is replaced with the value that it references in lookup table GL_PIXEL_MAP_I_TO_I.</span></span></li>
<li><span data-ttu-id="81439-130">Unabhängig davon, ob die Such Ersetzung des Indexes abgeschlossen ist oder nicht, wird der ganzzahlige Teil des <strong></strong>Indexes dann mit 2<em><sup>b</sup></em> 1, wobei <em>b</em> die Anzahl der Bits in einem Farb Index Puffer ist.</span><span class="sxs-lookup"><span data-stu-id="81439-130">Whether the lookup replacement of the index is done or not, the integer part of the index is then <strong>AND</strong>ed with 2<em><sup>b</sup></em> 1, where <em>b</em> is the number of bits in a color-index buffer.</span></span></li>
</ol>
<span data-ttu-id="81439-131">Wenn sich OpenGL im RGBA-Modus befindet:</span><span class="sxs-lookup"><span data-stu-id="81439-131">If OpenGL is in RGBA mode:</span></span><br/>
<ol>
<li><span data-ttu-id="81439-132">Die roten, grünen, blauen und Alpha Komponenten jedes gelesenen Pixels werden in ein internes Gleit Komma Format mit einer nicht spezifizierten Genauigkeit konvertiert.</span><span class="sxs-lookup"><span data-stu-id="81439-132">The red, green, blue, and alpha components of each pixel that is read are converted to an internal floating-point format with unspecified precision.</span></span></li>
<li><span data-ttu-id="81439-133">Bei der Konvertierung wird der größte darstellbare Komponenten Wert 1,0 und der Komponenten Wert 0 bis 0,0 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="81439-133">The conversion maps the largest representable component value to 1.0, and component value zero to 0.0.</span></span></li>
<li><span data-ttu-id="81439-134">Die resultierenden Gleit Komma Farbwerte werden dann mit GL_c_SCALE multipliziert und GL_c_BIAS hinzugefügt, wobei <em>c</em> für die jeweiligen Farbkomponenten Rot, grün, blau und Alpha ist.</span><span class="sxs-lookup"><span data-stu-id="81439-134">The resulting floating-point color values are then multiplied by GL_c_SCALE and added to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span></li>
<li><span data-ttu-id="81439-135">Die Ergebnisse werden an den Bereich [0, 1] gebunden.</span><span class="sxs-lookup"><span data-stu-id="81439-135">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="81439-136">Wenn GL_MAP_COLOR true ist, wird jede Farbkomponente von der Größe der Nachschlage Tabelle GL_PIXEL_MAP_c_TO_c skaliert und dann durch den Wert ersetzt, auf den Sie in dieser Tabelle verweist. <em>c</em> ist R, G, B bzw..</span><span class="sxs-lookup"><span data-stu-id="81439-136">If GL_MAP_COLOR is true, each color component is scaled by the size of lookup table GL_PIXEL_MAP_c_TO_c, and then replaced by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span> <span data-ttu-id="81439-137">Die resultierenden Indizes oder RGBA-Farben werden dann in Fragmente konvertiert, indem die aktuelle Raster Position <em>z</em>-Koordinate und Texturkoordinaten an jedes Pixel angefügt werden. Anschließend werden Fenster Koordinaten (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>) zugewiesen, wobei (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) die aktuelle Raster Position ist, und das Pixel ist das Pixel an der Position <em>i</em> in der <em>j</em> -Zeile.</span><span class="sxs-lookup"><span data-stu-id="81439-137">The resulting indexes or RGBA colors are then converted to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, and then assigning window coordinates (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position, and the pixel was the pixel in the <em>i</em> position in the <em>j</em> row.</span></span> <span data-ttu-id="81439-138">Diese Pixel Fragmente werden dann wie die Fragmente behandelt, die durch rasterisierungspunkte, Linien oder Polygone generiert werden.</span><span class="sxs-lookup"><span data-stu-id="81439-138">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="81439-139">Textur Zuordnung, Nebel und alle fragmentvorgänge werden angewendet, bevor die Fragmente in den Framebuffer geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="81439-139">Texture mapping, fog, and all the fragment operations are applied before the fragments are written to the framebuffer.</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_DEPTH"></span><span id="gl_depth"></span><dl> <span data-ttu-id="81439-140"><dt><strong>GL_DEPTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="81439-140"><dt><strong>GL_DEPTH</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="81439-141">Tiefen Werte werden aus dem tiefen Puffer gelesen und direkt in ein internes Gleit Komma Format mit nicht spezifizierter Genauigkeit konvertiert.</span><span class="sxs-lookup"><span data-stu-id="81439-141">Depth values are read from the depth buffer and converted directly to an internal floating-point format with unspecified precision.</span></span> <span data-ttu-id="81439-142">Der resultierende Gleit Komma tiefen Wert wird dann mit GL_DEPTH_SCALE multipliziert und GL_DEPTH_BIAS hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="81439-142">The resulting floating-point depth value is then multiplied by GL_DEPTH_SCALE and added to GL_DEPTH_BIAS.</span></span> <span data-ttu-id="81439-143">Das Ergebnis wird an den Bereich [0, 1] gebunden.</span><span class="sxs-lookup"><span data-stu-id="81439-143">The result is clamped to the range [0,1].</span></span> <br/> <span data-ttu-id="81439-144">Die resultierenden tiefen Komponenten werden dann in Fragmente konvertiert, indem die aktuelle Raster Positions Farbe oder der aktuelle Farb Index und die Texturkoordinaten an jedes Pixel angefügt werden. Anschließend werden Fenster Koordinaten (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>) zugewiesen, wobei (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) die aktuelle Raster Position und das Pixel das Pixel an der Position <em>i</em> in der <em>j</em> -Zeile ist.</span><span class="sxs-lookup"><span data-stu-id="81439-144">The resulting depth components are then converted to fragments by attaching the current raster position color or color index and texture coordinates to each pixel, then assigning window coordinates (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position, and the pixel was the pixel in the <em>i</em> position in the <em>j</em> row.</span></span> <span data-ttu-id="81439-145">Diese Pixel Fragmente werden dann wie die Fragmente behandelt, die durch rasterisierungspunkte, Linien oder Polygone generiert werden.</span><span class="sxs-lookup"><span data-stu-id="81439-145">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="81439-146">Textur Zuordnung, Nebel und alle fragmentvorgänge werden angewendet, bevor die Fragmente in den Framebuffer geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="81439-146">Texture mapping, fog, and all the fragment operations are applied before the fragments are written to the framebuffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl> <span data-ttu-id="81439-147"><dt><strong>GL_STENCIL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="81439-147"><dt><strong>GL_STENCIL</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="81439-148">Schablone-Indizes werden aus dem Schablonen Puffer gelesen und in ein internes fest Komma Format mit einer nicht angegebenen Anzahl von Bits auf der rechten Seite des binären Punkts konvertiert.</span><span class="sxs-lookup"><span data-stu-id="81439-148">Stencil indexes are read from the stencil buffer and converted to an internal fixed-point format with an unspecified number of bits to the right of the binary point.</span></span> <span data-ttu-id="81439-149">Jeder Index des Index wird dann von GL_INDEX_SHIFT Bits nach links verschoben und GL_INDEX_OFFSET hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="81439-149">Each fixed-point index is then shifted left by GL_INDEX_SHIFT bits, and added to GL_INDEX_OFFSET.</span></span> <span data-ttu-id="81439-150">Wenn GL_INDEX_SHIFT negativ ist, befindet sich die UMSCHALTTASTE auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="81439-150">If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="81439-151">In beiden Fällen füllen Null Bits andernfalls nicht angegebene Bitpositionen im Ergebnis aus.</span><span class="sxs-lookup"><span data-stu-id="81439-151">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span> <span data-ttu-id="81439-152">Wenn GL_MAP_STENCIL true ist, wird der Index durch den Wert ersetzt, auf den in der Nachschlage Tabelle GL_PIXEL_MAP_S_TO_S verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="81439-152">If GL_MAP_STENCIL is true, the index is replaced with the value that it references in lookup table GL_PIXEL_MAP_S_TO_S.</span></span> <span data-ttu-id="81439-153">Unabhängig davon, ob die Such Ersetzung des Indexes abgeschlossen ist oder nicht, wird der ganzzahlige Teil des Indexes dann mit 2<sup>b</sup> 1 <strong>und</strong>mit 2 b - 1, wobei <em>b</em> die Anzahl der Bits im Schablonen Puffer ist.</span><span class="sxs-lookup"><span data-stu-id="81439-153">Whether the lookup replacement of the index is done or not, the integer part of the index is then <strong>AND</strong>ed with 2<sup>b</sup> - 1, where <em>b</em> is the number of bits in the stencil buffer.</span></span> <span data-ttu-id="81439-154">Die resultierenden Schablonen Indizes werden dann in den Schablonen Puffer geschrieben, sodass der aus dem <em>i</em> -Speicherort der <em>j</em> -Zeile gelesene Index in den Speicherort (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>) geschrieben wird, wobei (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) die aktuelle Raster Position ist.</span><span class="sxs-lookup"><span data-stu-id="81439-154">The resulting stencil indexes are then written to the stencil buffer such that the index read from the <em>i</em> location of the <em>j</em> row is written to location (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span> <span data-ttu-id="81439-155">Diese Schreibvorgänge wirken sich nur auf den Pixel Besitz Test, den Scheren Test und die Schablone-Schreibvorgängen aus.</span><span class="sxs-lookup"><span data-stu-id="81439-155">Only the pixel-ownership test, the scissor test, and the stencil writemask affect these writes.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81439-156">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81439-156">Return value</span></span>

<span data-ttu-id="81439-157">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="81439-157">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="81439-158">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="81439-158">Error codes</span></span>

<span data-ttu-id="81439-159">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="81439-159">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="81439-160">Name</span><span class="sxs-lookup"><span data-stu-id="81439-160">Name</span></span>                                                                                                  | <span data-ttu-id="81439-161">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="81439-161">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81439-162"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81439-162"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="81439-163">der *Typ* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="81439-163">*type* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="81439-164"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="81439-164"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="81439-165">Die *Breite* oder Höhe war negativ.</span><span class="sxs-lookup"><span data-stu-id="81439-165">Either *width* or height was negative.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="81439-166"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="81439-166"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="81439-167">*Type* war GL \_ -Tiefe, und es gab keinen tiefen Puffer.</span><span class="sxs-lookup"><span data-stu-id="81439-167">*type* was GL\_DEPTH and there was no depth buffer.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="81439-168"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="81439-168"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="81439-169">*Typ* : GL \_ -Schablone und kein Schablone-Puffer.</span><span class="sxs-lookup"><span data-stu-id="81439-169">*type* was GL\_STENCIL and there was no stencil buffer.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="81439-170"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="81439-170"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="81439-171">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="81439-171">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="81439-172">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81439-172">Remarks</span></span>

<span data-ttu-id="81439-173">Die Funktion " **glcopypixels** " kopiert ein Bildschirm gerichtetes Rechteck aus Pixeln vom angegebenen Frame Puffer-Speicherort in einen Bereich relativ zur aktuellen Raster Position.</span><span class="sxs-lookup"><span data-stu-id="81439-173">The **glCopyPixels** function copies a screen-aligned rectangle of pixels from the specified framebuffer location to a region relative to the current raster position.</span></span> <span data-ttu-id="81439-174">Der Vorgang ist nur dann klar definiert, wenn sich der gesamte Pixel Quellbereich innerhalb des verfügbar gemachten Teils des Fensters befindet.</span><span class="sxs-lookup"><span data-stu-id="81439-174">Its operation is well defined only if the entire pixel source region is within the exposed portion of the window.</span></span> <span data-ttu-id="81439-175">Die Ergebnisse von Kopien von außerhalb des Fensters oder aus den nicht verfügbar gemachten Fenstern sind Hardware abhängig und nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="81439-175">Results of copies from outside the window, or from regions of the window that are not exposed, are hardware dependent and undefined.</span></span>

<span data-ttu-id="81439-176">Der *x* -und der *y* -Parameter geben die Fenster Koordinaten der unteren linken Ecke des rechteckigen Bereichs an, der kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="81439-176">The *x* and *y* parameters specify the window coordinates of the lower-left corner of the rectangular region to be copied.</span></span> <span data-ttu-id="81439-177">Die *Width* -und *height* -Parameter geben die Dimensionen des rechteckigen Bereichs an, der kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="81439-177">The *width* and *height* parameters specify the dimensions of the rectangular region to be copied.</span></span> <span data-ttu-id="81439-178">Sowohl " *Width* " als auch " *height* " dürfen nicht negativ sein.</span><span class="sxs-lookup"><span data-stu-id="81439-178">Both *width* and *height* must be nonnegative.</span></span>

<span data-ttu-id="81439-179">Mehrere Parameter steuern die Verarbeitung der Pixeldaten, während diese kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="81439-179">Several parameters control the processing of the pixel data while it is being copied.</span></span> <span data-ttu-id="81439-180">Diese Parameter werden mit drei Funktionen festgelegt: [**glpixeltransfer**](glpixeltransfer.md), [**glpixelmap**](glpixelmap.md)und [**glpixelzoom**](glpixelzoom.md).</span><span class="sxs-lookup"><span data-stu-id="81439-180">These parameters are set with three functions: [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md), and [**glPixelZoom**](glpixelzoom.md).</span></span> <span data-ttu-id="81439-181">In diesem Thema werden die Auswirkungen auf **glcopypixels** der meisten, aber nicht alle Parameter beschrieben, die von diesen drei Funktionen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="81439-181">This topic describes the effects on **glCopyPixels** of most, but not all, of the parameters specified by these three functions.</span></span>

<span data-ttu-id="81439-182">Die Funktion " **glcopypixels** " kopiert Werte von jedem Pixel mit der unteren linken Ecke um (*x*  +  *i*, *y*  +  *j*) für 0 = *i*  <  *Width* und 0 = *j*  <  *height*.</span><span class="sxs-lookup"><span data-stu-id="81439-182">The **glCopyPixels** function copies values from each pixel with the lower-left corner at (*x* + *i*, *y* + *j*) for 0 = *i* < *width* and 0 = *j* < *height*.</span></span> <span data-ttu-id="81439-183">Dieses Pixel ist das *i* -Pixel in der *j* -Zeile.</span><span class="sxs-lookup"><span data-stu-id="81439-183">This pixel is said to be the *i* pixel in the *j* row.</span></span> <span data-ttu-id="81439-184">Pixel werden in Zeilen Reihenfolge von der niedrigsten zur höchsten Zeile (von links nach rechts) in jeder Zeile kopiert.</span><span class="sxs-lookup"><span data-stu-id="81439-184">Pixels are copied in row order from the lowest to the highest row, left to right in each row.</span></span>

<span data-ttu-id="81439-185">Der *Typparameter* gibt an, ob Farbe, Tiefe oder Schablonen Daten kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81439-185">The *type* parameter specifies whether color, depth, or stencil data is to be copied.</span></span>

<span data-ttu-id="81439-186">Die bisher beschriebene rasterisierung setzt die Pixel Zoomfaktoren von 1,0 voraus.</span><span class="sxs-lookup"><span data-stu-id="81439-186">The rasterization described thus far assumes pixel zoom factors of 1.0.</span></span> <span data-ttu-id="81439-187">Wenn Sie mit [**glpixelzoom**](glpixelzoom.md) die *x* -und *y* -Pixel Zoomfaktoren ändern, werden Pixel wie folgt in Fragmente konvertiert.</span><span class="sxs-lookup"><span data-stu-id="81439-187">If you use [**glPixelZoom**](glpixelzoom.md) to change the *x* and *y* pixel zoom factors, pixels are converted to fragments as follows.</span></span> <span data-ttu-id="81439-188">Wenn (*x*<sub>r</sub> , *y*<sub>r</sub> ) die aktuelle Raster Position ist und sich ein angegebenes Pixel an der *i* -Position in der *j* -Zeile des Quell Pixel Rechtecks befindet, werden Fragmente für Pixel generiert, deren Mittelpunkt in dem Rechteck mit Ecken liegt.</span><span class="sxs-lookup"><span data-stu-id="81439-188">If (*x*<sub>r</sub> , *y*<sub>r</sub> ) is the current raster position, and a given pixel is in the *i* location in the *j* row of the source pixel rectangle, then fragments are generated for pixels whose centers are in the rectangle with corners at</span></span>

<span data-ttu-id="81439-189">(*x*<sub>r</sub>  +  *Zoom*? i, y <sub>r</sub>  +  *Zoom*<sub>y</sub> *j*)</span><span class="sxs-lookup"><span data-stu-id="81439-189">(*x*<sub>r</sub> + *zoom*? i, y <sub>r</sub> + *zoom*<sub>y</sub> *j*)</span></span>

<span data-ttu-id="81439-190">und</span><span class="sxs-lookup"><span data-stu-id="81439-190">and</span></span>

<span data-ttu-id="81439-191">(*x*<sub>r</sub>  +  *Zoom*?</span><span class="sxs-lookup"><span data-stu-id="81439-191">(*x*<sub>r</sub> + *zoom*?</span></span> <span data-ttu-id="81439-192">(*i* + 1), *y*<sub>r</sub>  +  *Zoom*<sub>y</sub> (*j* + 1))</span><span class="sxs-lookup"><span data-stu-id="81439-192">(*i* + 1), *y*<sub>r</sub> + *zoom*<sub>y</sub> (*j* + 1))</span></span>

<span data-ttu-id="81439-193">Where *Zoom*? der Wert von GL \_ Zoom \_ X und *Zoom*<sub>y</sub> ist der Wert von GL \_ Zoom \_ y.</span><span class="sxs-lookup"><span data-stu-id="81439-193">where *zoom*? is the value of GL\_ZOOM\_X and *zoom*<sub>y</sub> is the value of GL\_ZOOM\_Y.</span></span>

<span data-ttu-id="81439-194">Von [**glpixelstore**](glpixelstore-functions.md) angegebene Modi haben keine Auswirkung auf den Vorgang von **glcopypixels**.</span><span class="sxs-lookup"><span data-stu-id="81439-194">Modes specified by [**glPixelStore**](glpixelstore-functions.md) have no effect on the operation of **glCopyPixels**.</span></span>

<span data-ttu-id="81439-195">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glcopypixel** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="81439-195">The following functions retrieve information related to **glCopyPixels**:</span></span>

<span data-ttu-id="81439-196">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ aktuelle \_ Raster \_ Position</span><span class="sxs-lookup"><span data-stu-id="81439-196">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>

<span data-ttu-id="81439-197">**glget** mit dem Argument GL \_ aktuelle \_ Raster \_ Position \_ gültig</span><span class="sxs-lookup"><span data-stu-id="81439-197">**glGet** with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>

<span data-ttu-id="81439-198">Um das Farb Pixel in der unteren linken Ecke des Fensters an die aktuelle Raster Position zu kopieren, verwenden Sie</span><span class="sxs-lookup"><span data-stu-id="81439-198">To copy the color pixel in the lower-left corner of the window to the current raster position, use</span></span>

<span data-ttu-id="81439-199">**glcopypixels**(0, 0, 1, 1, GL- \_ Farbe);</span><span class="sxs-lookup"><span data-stu-id="81439-199">**glCopyPixels**( 0, 0, 1, 1, GL\_COLOR );</span></span>

## <a name="requirements"></a><span data-ttu-id="81439-200">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81439-200">Requirements</span></span>



| <span data-ttu-id="81439-201">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81439-201">Requirement</span></span> | <span data-ttu-id="81439-202">Wert</span><span class="sxs-lookup"><span data-stu-id="81439-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81439-203">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81439-203">Minimum supported client</span></span><br/> | <span data-ttu-id="81439-204">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81439-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="81439-205">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81439-205">Minimum supported server</span></span><br/> | <span data-ttu-id="81439-206">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81439-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="81439-207">Header</span><span class="sxs-lookup"><span data-stu-id="81439-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="81439-208"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="81439-208"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="81439-209">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="81439-209">Library</span></span><br/>                  | <dl> <span data-ttu-id="81439-210"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81439-210"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="81439-211">DLL</span><span class="sxs-lookup"><span data-stu-id="81439-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81439-212"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81439-212"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81439-213">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81439-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81439-214">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="81439-214">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="81439-215">**gldepthfunc**</span><span class="sxs-lookup"><span data-stu-id="81439-215">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="81439-216">**gldrawbuffer**</span><span class="sxs-lookup"><span data-stu-id="81439-216">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="81439-217">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="81439-217">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="81439-218">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="81439-218">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="81439-219">**glget**</span><span class="sxs-lookup"><span data-stu-id="81439-219">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="81439-220">**glpixelmap**</span><span class="sxs-lookup"><span data-stu-id="81439-220">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="81439-221">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="81439-221">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="81439-222">**glpixeltransfer**</span><span class="sxs-lookup"><span data-stu-id="81439-222">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="81439-223">**glpixelzoom**</span><span class="sxs-lookup"><span data-stu-id="81439-223">**glPixelZoom**</span></span>](glpixelzoom.md)
</dt> <dt>

[<span data-ttu-id="81439-224">**glRasterPos**</span><span class="sxs-lookup"><span data-stu-id="81439-224">**glRasterPos**</span></span>](glrasterpos-functions.md)
</dt> <dt>

[<span data-ttu-id="81439-225">**glread Buffer**</span><span class="sxs-lookup"><span data-stu-id="81439-225">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> <dt>

[<span data-ttu-id="81439-226">**glread Pixels**</span><span class="sxs-lookup"><span data-stu-id="81439-226">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="81439-227">**glstencilfunc**</span><span class="sxs-lookup"><span data-stu-id="81439-227">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





