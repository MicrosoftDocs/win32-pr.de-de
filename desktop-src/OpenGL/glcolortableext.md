---
title: glcolortableext-Funktion (GL. h)
description: Die glcolortableext-Funktion gibt das Format und die Größe einer Palette für die Zielstrukturen an.
ms.assetid: f3d7b1a1-97a5-47ef-a0ca-5e58acb86bb4
keywords:
- glcolortableext-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0d5fd5c848e787f480e3e1893b9b25e4bbd3de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742209"
---
# <a name="glcolortableext-function"></a><span data-ttu-id="90d44-104">glcolortableext-Funktion</span><span class="sxs-lookup"><span data-stu-id="90d44-104">glColorTableEXT function</span></span>

<span data-ttu-id="90d44-105">Die **glcolortableext** -Funktion gibt das Format und die Größe einer Palette für die Zielstrukturen an.</span><span class="sxs-lookup"><span data-stu-id="90d44-105">The **glColorTableEXT** function specifies the format and size of a palette for targeted paletted textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="90d44-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="90d44-106">Syntax</span></span>


```C++
void WINAPI glColorTableEXT(
         GLenum  target,
         GLenum  internalFormat,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a><span data-ttu-id="90d44-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="90d44-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90d44-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="90d44-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="90d44-109">Die Ziel Textur, deren Palette geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="90d44-109">The target texture that is to have its palette changed.</span></span> <span data-ttu-id="90d44-110">Muss Textur \_ 1D, Textur \_ 2D, Proxy \_ Textur \_ 1D oder Proxy \_ Textur \_ 2D sein.</span><span class="sxs-lookup"><span data-stu-id="90d44-110">Must be TEXTURE\_1D, TEXTURE\_2D, PROXY\_TEXTURE\_1D, or PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="90d44-111">*internalformat*</span><span class="sxs-lookup"><span data-stu-id="90d44-111">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="90d44-112">Das interne Format und die Auflösung der Palette.</span><span class="sxs-lookup"><span data-stu-id="90d44-112">The internal format and resolution of the palette.</span></span> <span data-ttu-id="90d44-113">Dieser Parameter kann einen der folgenden symbolischen Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="90d44-113">This parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="90d44-114">Konstante</span><span class="sxs-lookup"><span data-stu-id="90d44-114">Constant</span></span>       | <span data-ttu-id="90d44-115">Basis Format</span><span class="sxs-lookup"><span data-stu-id="90d44-115">Base Format</span></span> | <span data-ttu-id="90d44-116">R-Bits</span><span class="sxs-lookup"><span data-stu-id="90d44-116">R Bits</span></span> | <span data-ttu-id="90d44-117">G Bits</span><span class="sxs-lookup"><span data-stu-id="90d44-117">G Bits</span></span> | <span data-ttu-id="90d44-118">B Bits</span><span class="sxs-lookup"><span data-stu-id="90d44-118">B Bits</span></span> | <span data-ttu-id="90d44-119">Eine Bits</span><span class="sxs-lookup"><span data-stu-id="90d44-119">A Bits</span></span> |
|----------------|-------------|--------|--------|--------|--------|
| <span data-ttu-id="90d44-120">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="90d44-120">GL\_R3\_G3\_B2</span></span> | <span data-ttu-id="90d44-121">GL. \_ RGB</span><span class="sxs-lookup"><span data-stu-id="90d44-121">GL\_RGB</span></span>     | <span data-ttu-id="90d44-122">3</span><span class="sxs-lookup"><span data-stu-id="90d44-122">3</span></span>      | <span data-ttu-id="90d44-123">3</span><span class="sxs-lookup"><span data-stu-id="90d44-123">3</span></span>      | <span data-ttu-id="90d44-124">2</span><span class="sxs-lookup"><span data-stu-id="90d44-124">2</span></span>      |        |
| <span data-ttu-id="90d44-125">GL \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="90d44-125">GL\_RGB4</span></span>       | <span data-ttu-id="90d44-126">GL. \_ RGB</span><span class="sxs-lookup"><span data-stu-id="90d44-126">GL\_RGB</span></span>     | <span data-ttu-id="90d44-127">4</span><span class="sxs-lookup"><span data-stu-id="90d44-127">4</span></span>      | <span data-ttu-id="90d44-128">4</span><span class="sxs-lookup"><span data-stu-id="90d44-128">4</span></span>      | <span data-ttu-id="90d44-129">4</span><span class="sxs-lookup"><span data-stu-id="90d44-129">4</span></span>      |        |
| <span data-ttu-id="90d44-130">GL \_ RGB5</span><span class="sxs-lookup"><span data-stu-id="90d44-130">GL\_RGB5</span></span>       | <span data-ttu-id="90d44-131">GL. \_ RGB</span><span class="sxs-lookup"><span data-stu-id="90d44-131">GL\_RGB</span></span>     | <span data-ttu-id="90d44-132">5</span><span class="sxs-lookup"><span data-stu-id="90d44-132">5</span></span>      | <span data-ttu-id="90d44-133">5</span><span class="sxs-lookup"><span data-stu-id="90d44-133">5</span></span>      | <span data-ttu-id="90d44-134">5</span><span class="sxs-lookup"><span data-stu-id="90d44-134">5</span></span>      |        |
| <span data-ttu-id="90d44-135">GL \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="90d44-135">GL\_RGB8</span></span>       | <span data-ttu-id="90d44-136">GL. \_ RGB</span><span class="sxs-lookup"><span data-stu-id="90d44-136">GL\_RGB</span></span>     | <span data-ttu-id="90d44-137">8</span><span class="sxs-lookup"><span data-stu-id="90d44-137">8</span></span>      | <span data-ttu-id="90d44-138">8</span><span class="sxs-lookup"><span data-stu-id="90d44-138">8</span></span>      | <span data-ttu-id="90d44-139">8</span><span class="sxs-lookup"><span data-stu-id="90d44-139">8</span></span>      |        |
| <span data-ttu-id="90d44-140">GL \_ RGB10</span><span class="sxs-lookup"><span data-stu-id="90d44-140">GL\_RGB10</span></span>      | <span data-ttu-id="90d44-141">GL. \_ RGB</span><span class="sxs-lookup"><span data-stu-id="90d44-141">GL\_RGB</span></span>     | <span data-ttu-id="90d44-142">10</span><span class="sxs-lookup"><span data-stu-id="90d44-142">10</span></span>     | <span data-ttu-id="90d44-143">10</span><span class="sxs-lookup"><span data-stu-id="90d44-143">10</span></span>     | <span data-ttu-id="90d44-144">10</span><span class="sxs-lookup"><span data-stu-id="90d44-144">10</span></span>     |        |
| <span data-ttu-id="90d44-145">GL \_ RGB12</span><span class="sxs-lookup"><span data-stu-id="90d44-145">GL\_RGB12</span></span>      | <span data-ttu-id="90d44-146">GL. \_ RGB</span><span class="sxs-lookup"><span data-stu-id="90d44-146">GL\_RGB</span></span>     | <span data-ttu-id="90d44-147">12</span><span class="sxs-lookup"><span data-stu-id="90d44-147">12</span></span>     | <span data-ttu-id="90d44-148">12</span><span class="sxs-lookup"><span data-stu-id="90d44-148">12</span></span>     | <span data-ttu-id="90d44-149">12</span><span class="sxs-lookup"><span data-stu-id="90d44-149">12</span></span>     |        |
| <span data-ttu-id="90d44-150">GL \_ RGB16</span><span class="sxs-lookup"><span data-stu-id="90d44-150">GL\_RGB16</span></span>      | <span data-ttu-id="90d44-151">GL. \_ RGB</span><span class="sxs-lookup"><span data-stu-id="90d44-151">GL\_RGB</span></span>     | <span data-ttu-id="90d44-152">16</span><span class="sxs-lookup"><span data-stu-id="90d44-152">16</span></span>     | <span data-ttu-id="90d44-153">16</span><span class="sxs-lookup"><span data-stu-id="90d44-153">16</span></span>     | <span data-ttu-id="90d44-154">16</span><span class="sxs-lookup"><span data-stu-id="90d44-154">16</span></span>     |        |
| <span data-ttu-id="90d44-155">GL \_ RGBA2</span><span class="sxs-lookup"><span data-stu-id="90d44-155">GL\_RGBA2</span></span>      | <span data-ttu-id="90d44-156">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="90d44-156">GL\_RGBA</span></span>    | <span data-ttu-id="90d44-157">2</span><span class="sxs-lookup"><span data-stu-id="90d44-157">2</span></span>      | <span data-ttu-id="90d44-158">2</span><span class="sxs-lookup"><span data-stu-id="90d44-158">2</span></span>      | <span data-ttu-id="90d44-159">2</span><span class="sxs-lookup"><span data-stu-id="90d44-159">2</span></span>      | <span data-ttu-id="90d44-160">2</span><span class="sxs-lookup"><span data-stu-id="90d44-160">2</span></span>      |
| <span data-ttu-id="90d44-161">GL \_ RGBA4</span><span class="sxs-lookup"><span data-stu-id="90d44-161">GL\_RGBA4</span></span>      | <span data-ttu-id="90d44-162">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="90d44-162">GL\_RGBA</span></span>    | <span data-ttu-id="90d44-163">4</span><span class="sxs-lookup"><span data-stu-id="90d44-163">4</span></span>      | <span data-ttu-id="90d44-164">4</span><span class="sxs-lookup"><span data-stu-id="90d44-164">4</span></span>      | <span data-ttu-id="90d44-165">4</span><span class="sxs-lookup"><span data-stu-id="90d44-165">4</span></span>      | <span data-ttu-id="90d44-166">4</span><span class="sxs-lookup"><span data-stu-id="90d44-166">4</span></span>      |
| <span data-ttu-id="90d44-167">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="90d44-167">GL\_RGB5\_A1</span></span>   | <span data-ttu-id="90d44-168">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="90d44-168">GL\_RGBA</span></span>    | <span data-ttu-id="90d44-169">5</span><span class="sxs-lookup"><span data-stu-id="90d44-169">5</span></span>      | <span data-ttu-id="90d44-170">5</span><span class="sxs-lookup"><span data-stu-id="90d44-170">5</span></span>      | <span data-ttu-id="90d44-171">5</span><span class="sxs-lookup"><span data-stu-id="90d44-171">5</span></span>      | <span data-ttu-id="90d44-172">1</span><span class="sxs-lookup"><span data-stu-id="90d44-172">1</span></span>      |
| <span data-ttu-id="90d44-173">GL \_ RGBA8</span><span class="sxs-lookup"><span data-stu-id="90d44-173">GL\_RGBA8</span></span>      | <span data-ttu-id="90d44-174">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="90d44-174">GL\_RGBA</span></span>    | <span data-ttu-id="90d44-175">8</span><span class="sxs-lookup"><span data-stu-id="90d44-175">8</span></span>      | <span data-ttu-id="90d44-176">8</span><span class="sxs-lookup"><span data-stu-id="90d44-176">8</span></span>      | <span data-ttu-id="90d44-177">8</span><span class="sxs-lookup"><span data-stu-id="90d44-177">8</span></span>      | <span data-ttu-id="90d44-178">8</span><span class="sxs-lookup"><span data-stu-id="90d44-178">8</span></span>      |
| <span data-ttu-id="90d44-179">GL \_ RG10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="90d44-179">GL\_RG10\_A2</span></span>   | <span data-ttu-id="90d44-180">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="90d44-180">GL\_RGBA</span></span>    | <span data-ttu-id="90d44-181">10</span><span class="sxs-lookup"><span data-stu-id="90d44-181">10</span></span>     | <span data-ttu-id="90d44-182">10</span><span class="sxs-lookup"><span data-stu-id="90d44-182">10</span></span>     | <span data-ttu-id="90d44-183">10</span><span class="sxs-lookup"><span data-stu-id="90d44-183">10</span></span>     | <span data-ttu-id="90d44-184">2</span><span class="sxs-lookup"><span data-stu-id="90d44-184">2</span></span>      |
| <span data-ttu-id="90d44-185">GL \_ RGB12</span><span class="sxs-lookup"><span data-stu-id="90d44-185">GL\_RGB12</span></span>      | <span data-ttu-id="90d44-186">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="90d44-186">GL\_RGBA</span></span>    | <span data-ttu-id="90d44-187">12</span><span class="sxs-lookup"><span data-stu-id="90d44-187">12</span></span>     | <span data-ttu-id="90d44-188">12</span><span class="sxs-lookup"><span data-stu-id="90d44-188">12</span></span>     | <span data-ttu-id="90d44-189">12</span><span class="sxs-lookup"><span data-stu-id="90d44-189">12</span></span>     | <span data-ttu-id="90d44-190">12</span><span class="sxs-lookup"><span data-stu-id="90d44-190">12</span></span>     |
| <span data-ttu-id="90d44-191">GL \_ RGBA16</span><span class="sxs-lookup"><span data-stu-id="90d44-191">GL\_RGBA16</span></span>     | <span data-ttu-id="90d44-192">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="90d44-192">GL\_RGBA</span></span>    | <span data-ttu-id="90d44-193">16</span><span class="sxs-lookup"><span data-stu-id="90d44-193">16</span></span>     | <span data-ttu-id="90d44-194">16</span><span class="sxs-lookup"><span data-stu-id="90d44-194">16</span></span>     | <span data-ttu-id="90d44-195">16</span><span class="sxs-lookup"><span data-stu-id="90d44-195">16</span></span>     | <span data-ttu-id="90d44-196">16</span><span class="sxs-lookup"><span data-stu-id="90d44-196">16</span></span>     |



 

</dd> <dt>

<span data-ttu-id="90d44-197">*width*</span><span class="sxs-lookup"><span data-stu-id="90d44-197">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="90d44-198">Die Größe der Palette.</span><span class="sxs-lookup"><span data-stu-id="90d44-198">The size of the palette.</span></span> <span data-ttu-id="90d44-199">Muss für eine Ganzzahl *n* 2 n = 1 sein.</span><span class="sxs-lookup"><span data-stu-id="90d44-199">Must be 2n = 1 for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="90d44-200">*format*</span><span class="sxs-lookup"><span data-stu-id="90d44-200">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="90d44-201">Das Format der Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="90d44-201">The format of the pixel data.</span></span> <span data-ttu-id="90d44-202">Die folgenden symbolischen Konstanten werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="90d44-202">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90d44-203">Wert</span><span class="sxs-lookup"><span data-stu-id="90d44-203">Value</span></span></th>
<th><span data-ttu-id="90d44-204">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="90d44-204">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="90d44-205"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="90d44-205"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="90d44-206">Jedes Pixel ist eine Gruppe von vier Komponenten in dieser Reihenfolge: rot, grün, blau, alpha.</span><span class="sxs-lookup"><span data-stu-id="90d44-206">Each pixel is a group of four components in this order: red, green, blue, alpha.</span></span> <span data-ttu-id="90d44-207">Das RGBA-Format wird auf diese Weise bestimmt:</span><span class="sxs-lookup"><span data-stu-id="90d44-207">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="90d44-208">Die <strong>glcolortableext</strong> -Funktion konvertiert Gleit Komma Werte direkt in ein internes Format mit einer nicht spezifizierten Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="90d44-208">The <strong>glColorTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="90d44-209">Ganzzahlige Werte mit Vorzeichen werden linear dem internen Format zugeordnet, sodass der positivste darstellbare ganzzahlige Wert 1,0 und der negativste darstellbare ganzzahlige Wert-1,0 zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="90d44-209">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable integer value maps to -1.0.</span></span> <span data-ttu-id="90d44-210">Ganzzahlige Daten ohne Vorzeichen werden ähnlich zugeordnet: der größte ganzzahlige Wert ist 1,0, und NULL wird 0,0 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="90d44-210">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="90d44-211">Die Funktion " <strong>glcolortableext</strong> " multipliziert die resultierenden Farbwerte GL_c_SCALE und fügt Sie GL_c_BIAS hinzu, wobei <em>c</em> rot, grün, blau und Alpha für die jeweiligen Farbkomponenten ist.</span><span class="sxs-lookup"><span data-stu-id="90d44-211">The <strong>glColorTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="90d44-212">Die Ergebnisse werden an den Bereich [0, 1] gebunden.</span><span class="sxs-lookup"><span data-stu-id="90d44-212">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="90d44-213">Wenn GL_MAP_COLOR auf <strong>true</strong>festgelegt ist, skaliert <strong>glcolortableext</strong> jede Farbkomponente anhand der Größe der Nachschlage Tabelle GL_PIXEL_MAP_c_TO_c und ersetzt dann die Komponente durch den Wert, auf den Sie in dieser Tabelle verweist. <em>c</em> ist R, G, B bzw..</span><span class="sxs-lookup"><span data-stu-id="90d44-213">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glColorTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="90d44-214">Mit der <strong>glcolortableext</strong> -Funktion werden die resultierenden RGBA-Farben in Fragmente konvertiert, indem die aktuelle Raster Position <em>z</em>-Koordinate und Texturkoordinaten an jedes Pixel angefügt werden. Anschließend werden <em>x</em> -und <em>y</em> -Fenster Koordinaten für das <em>n</em>-te Fragment so<em>x</em>zugewiesen?</span><span class="sxs-lookup"><span data-stu-id="90d44-214">The <strong>glColorTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that<em>x</em>?</span></span><span data-ttu-id="90d44-215"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>Breite</em></span><span class="sxs-lookup"><span data-stu-id="90d44-215"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="90d44-216"><em></em>Teenie?</span><span class="sxs-lookup"><span data-stu-id="90d44-216"><em></em>y?</span></span><span data-ttu-id="90d44-217"> = <em>y</em><sub>r</sub> +<em>n/Breite</em></span><span class="sxs-lookup"><span data-stu-id="90d44-217"> = <em>y</em><sub>r</sub> +<em>n / width</em></span></span><br/> <span data-ttu-id="90d44-218">Where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) ist die aktuelle Raster Position.</span><span class="sxs-lookup"><span data-stu-id="90d44-218">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="90d44-219">Diese Pixel Fragmente werden dann wie die Fragmente behandelt, die durch rasterisierungspunkte, Linien oder Polygone generiert werden.</span><span class="sxs-lookup"><span data-stu-id="90d44-219">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="90d44-220">Die <strong>glcolortableext</strong> -Funktion wendet Textur Zuordnung, Nebel und alle fragmentvorgänge an, bevor die Fragmente in den Framebuffer geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="90d44-220">The <strong>glColorTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="90d44-221"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="90d44-221"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="90d44-222">Jedes Pixel ist eine einzelne rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="90d44-222">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="90d44-223">Die Funktion " <strong>glcolortableext</strong> " konvertiert diese Komponente auf die gleiche Weise in das interne Format wie die rote Komponente eines RGBA-Pixels, konvertiert Sie dann in ein RGBA-Pixel, bei dem Grün und blau auf 0,0 und Alpha auf 1,0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="90d44-223">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="90d44-224">Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.</span><span class="sxs-lookup"><span data-stu-id="90d44-224">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="90d44-225"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="90d44-225"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="90d44-226">Jedes Pixel ist eine einzelne grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="90d44-226">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="90d44-227">Die Funktion " <strong>glcolortableext</strong> " konvertiert diese Komponente auf die gleiche Weise wie die grüne Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, bei dem "Red" und "Blue" auf "0,0" und "Alpha" auf 1,0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="90d44-227">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="90d44-228">Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.</span><span class="sxs-lookup"><span data-stu-id="90d44-228">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="90d44-229"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="90d44-229"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="90d44-230">Jedes Pixel ist eine einzelne blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="90d44-230">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="90d44-231">Die <strong>glcolortableext</strong> -Funktion konvertiert diese Komponente auf die gleiche Weise wie die blaue Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, wobei rot und grün auf 0,0 und Alpha auf 1,0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="90d44-231">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="90d44-232">Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.</span><span class="sxs-lookup"><span data-stu-id="90d44-232">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="90d44-233"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="90d44-233"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="90d44-234">Jedes Pixel ist eine einzelne Alpha Komponente.</span><span class="sxs-lookup"><span data-stu-id="90d44-234">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="90d44-235">Die Funktion " <strong>glcolortableext</strong> " konvertiert diese Komponente auf die gleiche Weise wie die Alpha Komponente eines RGBA-Pixels in das interne Format und konvertiert Sie dann in ein RGBA-Pixel, bei dem rot, grün und blau auf 0,0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="90d44-235">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="90d44-236">Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.</span><span class="sxs-lookup"><span data-stu-id="90d44-236">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="90d44-237"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="90d44-237"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="90d44-238">Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: rot, grün, blau.</span><span class="sxs-lookup"><span data-stu-id="90d44-238">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="90d44-239">Die <strong>glcolortableext</strong> -Funktion konvertiert jede Komponente auf die gleiche Weise in das interne Format wie die roten, grünen und blauen Komponenten eines RGBA-Pixels.</span><span class="sxs-lookup"><span data-stu-id="90d44-239">The <strong>glColorTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="90d44-240">Die Farbe Triple wird in ein RGBA-Pixel konvertiert, bei dem Alpha auf 1,0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="90d44-240">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="90d44-241">Nach dieser Konvertierung wird das Pixel so behandelt, als ob es als RGBA-Pixel gelesen worden wäre.</span><span class="sxs-lookup"><span data-stu-id="90d44-241">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="90d44-242"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="90d44-242"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="90d44-243">Jedes Pixel ist eine Gruppe von drei Komponenten in dieser Reihenfolge: blau, grün, rot.</span><span class="sxs-lookup"><span data-stu-id="90d44-243">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="90d44-244">GL_BGR_EXT bietet ein Format, das dem Arbeitsspeicher Layout von Windows-geräteunabhängigen Bitmaps (Disb) entspricht.</span><span class="sxs-lookup"><span data-stu-id="90d44-244">GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="90d44-245">Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.</span><span class="sxs-lookup"><span data-stu-id="90d44-245">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="90d44-246"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="90d44-246"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="90d44-247">Jedes Pixel ist eine Gruppe von vier Komponenten in dieser Reihenfolge: blau, grün, rot, alpha.</span><span class="sxs-lookup"><span data-stu-id="90d44-247">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="90d44-248">GL_BGRA_EXT bietet ein Format, das dem Arbeitsspeicher Layout von Windows-geräteunabhängigen Bitmaps (Disb) entspricht.</span><span class="sxs-lookup"><span data-stu-id="90d44-248">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="90d44-249">Daher können Ihre Anwendungen dieselben Daten mit Windows-Funktionsaufrufen und OpenGL-Pixel Funktionsaufrufen verwenden.</span><span class="sxs-lookup"><span data-stu-id="90d44-249">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="90d44-250">*type*</span><span class="sxs-lookup"><span data-stu-id="90d44-250">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="90d44-251">Der Datentyp für *Daten*.</span><span class="sxs-lookup"><span data-stu-id="90d44-251">The data type for *data*.</span></span> <span data-ttu-id="90d44-252">Die folgenden symbolischen Konstanten werden akzeptiert: GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int und GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="90d44-252">The following symbolic constants are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

<span data-ttu-id="90d44-253">In der folgenden Tabelle wird die Bedeutung der gültigen Konstanten für den *Typparameter* zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="90d44-253">The following table summarizes the meaning of the valid constants for the *type* parameter.</span></span>



| <span data-ttu-id="90d44-254">Wert</span><span class="sxs-lookup"><span data-stu-id="90d44-254">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="90d44-255">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="90d44-255">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="90d44-256"><dt>**GL- \_ Byte ohne Vorzeichen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="90d44-256"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="90d44-257">8-Bit-Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="90d44-257">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="90d44-258"><dt>**GL \_ Byte**</dt></span><span class="sxs-lookup"><span data-stu-id="90d44-258"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="90d44-259">Ganze 8-Bit-Zahl mit Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="90d44-259">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="90d44-260"><dt>**GL \_ unsigned \_ Short**</dt></span><span class="sxs-lookup"><span data-stu-id="90d44-260"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="90d44-261">16-Bit-Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="90d44-261">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="90d44-262"><dt>**GL \_ Short**</dt></span><span class="sxs-lookup"><span data-stu-id="90d44-262"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="90d44-263">Ganze 16-Bit-Zahl mit Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="90d44-263">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="90d44-264"><dt>**GL \_ unsigned \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="90d44-264"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="90d44-265">32-Bit Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="90d44-265">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="90d44-266"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="90d44-266"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="90d44-267">32-bit integer</span><span class="sxs-lookup"><span data-stu-id="90d44-267">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="90d44-268"><dt>**GL \_ float**</dt></span><span class="sxs-lookup"><span data-stu-id="90d44-268"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="90d44-269">Gleitkommawert mit einfacher Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="90d44-269">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="90d44-270">*data*</span><span class="sxs-lookup"><span data-stu-id="90d44-270">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="90d44-271">Ein Zeiger auf die palettentextur Daten.</span><span class="sxs-lookup"><span data-stu-id="90d44-271">A pointer to the paletted texture data.</span></span> <span data-ttu-id="90d44-272">Die Daten werden als einzelne Pixel eines 1-D-Textur paletteneintrags für einen Paletteneintrag behandelt.</span><span class="sxs-lookup"><span data-stu-id="90d44-272">The data is treated as single pixels of a 1-D texture palette entry for a palette entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90d44-273">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90d44-273">Return value</span></span>

<span data-ttu-id="90d44-274">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="90d44-274">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="90d44-275">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="90d44-275">Error codes</span></span>

<span data-ttu-id="90d44-276">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="90d44-276">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="90d44-277">Name</span><span class="sxs-lookup"><span data-stu-id="90d44-277">Name</span></span>                                                                                                  | <span data-ttu-id="90d44-278">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="90d44-278">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="90d44-279"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="90d44-279"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="90d44-280">*Breite* war eine ungültige ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="90d44-280">*width* was an invalid integer.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="90d44-281"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="90d44-281"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="90d44-282">" *target*", " *internalformat*", " *Format*" oder " *Type* " war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="90d44-282">*target*, *internalFormat*, *format*, or *type* was not an accepted value.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="90d44-283"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="90d44-283"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="90d44-284">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="90d44-284">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="90d44-285">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90d44-285">Remarks</span></span>

<span data-ttu-id="90d44-286">Palettentexturen werden mit einer Palette von Farben und einem Satz von Bilddaten definiert, die aus Indizes für Farbeinträge einer Palette (Farbtabelle) bestehen.</span><span class="sxs-lookup"><span data-stu-id="90d44-286">Paletted textures are defined with a palette of colors and a set of image data that is composed of indexes to color entries of a palette (a color table).</span></span>

<span data-ttu-id="90d44-287">Die **glcolortableext** -Funktion gibt die Texturpalette einer Ziel Textur an.</span><span class="sxs-lookup"><span data-stu-id="90d44-287">The **glColorTableEXT** function specifies the texture palette of a targeted texture.</span></span> <span data-ttu-id="90d44-288">Er nimmt die *Daten* aus dem Arbeitsspeicher und konvertiert die Daten so, als ob jeder Paletteneintrag ein einzelnes Pixel einer 1-D-Textur ist.</span><span class="sxs-lookup"><span data-stu-id="90d44-288">It takes the *data* from memory and converts the data as if each palette entry is a single pixel of a 1-D texture.</span></span> <span data-ttu-id="90d44-289">Die Funktion " **glcolortableext** " entpackt und konvertiert die Daten und übersetzt Sie in ein internes Format, das mit dem angegebenen *Format* so genau wie möglich übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="90d44-289">The **glColorTableEXT** function unpacks and converts the data and translates it into an internal format that matches the given *format* as closely as possible.</span></span>

<span data-ttu-id="90d44-290">Wenn die *Breite* einer Palette größer ist als der Bereich der Farbindizes in den Textur Daten, werden einige der Paletteneinträge nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="90d44-290">If a palette's *width* is greater than the range of the color indexes in the texture data, some of the palette entries are unused.</span></span> <span data-ttu-id="90d44-291">Wenn die *Breite* einer Palette kleiner ist als der Bereich der Farbindizes in den Textur Daten, werden die signifikantesten Bits der Textur Daten ignoriert, und nur die entsprechende Anzahl von Bits im Index wird beim Zugriff auf die Palette verwendet.</span><span class="sxs-lookup"><span data-stu-id="90d44-291">If a palette's *width* is less than the range of the color indexes in the texture data, the most significant bits of the texture data are ignored and only the appropriate number of bits in the index are used when accessing the palette.</span></span> <span data-ttu-id="90d44-292">Wenn Sie ein Proxy *Ziel* mithilfe der Proxy \_ Textur \_ 1D oder \_ der Proxy Textur \_ 2D angeben, wird die Größe der Palette der Proxy Textur geändert, und die Parameter werden festgelegt, aber es werden keine Daten übertragen oder darauf zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="90d44-292">When you specify a proxy *target* using PROXY\_TEXTURE\_1D or PROXY\_TEXTURE\_2D, the palette of the proxy texture is resized and its parameters are set but no data is transferred or accessed.</span></span>

<span data-ttu-id="90d44-293">Wenn der *Ziel* Parameter GL- \_ Proxy \_ Textur \_ 1D oder GL \_ \_ -Proxy Textur \_ 2D ist, und die-Implementierung die für *Format* oder *Width* angegebenen Werte nicht unter  stützt, kann bei der Erstellung der angeforderten Farbtabelle ein Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="90d44-293">When the *target* parameter is GL\_PROXY\_TEXTURE\_1D or GL\_PROXY\_TEXTURE\_2D, and the implementation does not support the values specified for either *format* or *width*, **glColorTableEXT** can fail to create the requested color table.</span></span> <span data-ttu-id="90d44-294">In diesem Fall ist die Farbtabelle leer, und alle abgerufenen Parameter haben den Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="90d44-294">In this case, the color table is empty and all parameters retrieved will be zero.</span></span> <span data-ttu-id="90d44-295">Sie können bestimmen, ob OpenGL ein bestimmtes Farbtabellen Format und eine bestimmte Größe unterstützt, indem Sie **glcolortableext** mit einem Proxy Ziel aufrufen und dann [**glgetcolortableparameterivext**](glgetcolortableparameterivext.md) oder [**glgetcolortableparameterfvext**](glgetcolortableparameterfvext.md) aufrufen, um zu bestimmen, ob der Width-Parameter mit dem von **glcolortableext** festgelegten width-Parameter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="90d44-295">You can determine whether OpenGL supports a particular color table format and size by calling **glColorTableEXT** with a proxy target, and then calling [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) or [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) to determine whether the width parameter matches that set by **glColorTableEXT**.</span></span> <span data-ttu-id="90d44-296">Wenn die abgerufene Breite 0 (null) ist, ist die Farbtabellen Anforderung von **glcolortable** fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="90d44-296">If the retrieved width is zero, the color table request by **glColorTable** failed.</span></span> <span data-ttu-id="90d44-297">Wenn die abgerufene Breite nicht NULL ist, können Sie **glcolortable** mit dem echten Ziel mit Textur \_ 1D oder Textur \_ 2D zum Festlegen der Farbtabelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="90d44-297">If the retrieved width is not zero, you can call **glColorTable** with the real target with TEXTURE\_1D or TEXTURE\_2D to set the color table.</span></span>

> [!Note]  
> <span data-ttu-id="90d44-298">Bei der **glcolortableext** -Funktion handelt es sich um eine Erweiterungs Funktion, die nicht Teil der OpenGL-Standardbibliothek ist, aber Bestandteil der \_ \_ Struktur Erweiterung von GL ext ist \_ .</span><span class="sxs-lookup"><span data-stu-id="90d44-298">The **glColorTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="90d44-299">Um zu überprüfen, ob die Implementierung von OpenGL **glcolortableext** unterstützt, nennen Sie [**glgetstring**](glgetstring.md)(GL \_ Extensions).</span><span class="sxs-lookup"><span data-stu-id="90d44-299">To check whether your implementation of OpenGL supports **glColorTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="90d44-300">Wenn Sie die Struktur von GL ext in der Struktur zurückgibt \_ \_ \_ , wird **glcolortableext** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="90d44-300">If it returns GL\_EXT\_paletted\_texture, **glColorTableEXT** is supported.</span></span> <span data-ttu-id="90d44-301">Rufen Sie zum Abrufen der Funktions Adresse einer Erweiterungs Funktion [**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)auf.</span><span class="sxs-lookup"><span data-stu-id="90d44-301">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

 

<span data-ttu-id="90d44-302">Rufen Sie zum Abrufen der tatsächlichen Farbtabellen Daten, die durch die **glcolortableext** -Funktion angegeben werden, [**glgetcolortableext**](glgetcolortableext.md)auf.</span><span class="sxs-lookup"><span data-stu-id="90d44-302">To retrieve the actual color table data specified by the **glColorTableEXT** function, call [**glGetColorTableEXT**](glgetcolortableext.md).</span></span> <span data-ttu-id="90d44-303">Um die Parameter (z. b. *Breite* und *Format*) der durch die Funktion " **glcolortableext** " angegebenen Farbtabelle abzurufen, rufen Sie die Funktion " **glgetcolortableparameterivext** " oder " **glgetcolortableparameterfvext** " auf.</span><span class="sxs-lookup"><span data-stu-id="90d44-303">To retrieve the parameters, such as *width* and *format*, of the color table specified by the **glColorTableEXT** function, call the **glGetColorTableParameterivEXT** or **glGetColorTableParameterfvEXT** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="90d44-304">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90d44-304">Requirements</span></span>



| <span data-ttu-id="90d44-305">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90d44-305">Requirement</span></span> | <span data-ttu-id="90d44-306">Wert</span><span class="sxs-lookup"><span data-stu-id="90d44-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="90d44-307">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90d44-307">Minimum supported client</span></span><br/> | <span data-ttu-id="90d44-308">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90d44-308">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="90d44-309">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90d44-309">Minimum supported server</span></span><br/> | <span data-ttu-id="90d44-310">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90d44-310">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="90d44-311">Header</span><span class="sxs-lookup"><span data-stu-id="90d44-311">Header</span></span><br/>                   | <dl> <span data-ttu-id="90d44-312"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="90d44-312"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90d44-313">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90d44-313">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90d44-314">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="90d44-314">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="90d44-315">**glcolorsubtableext**</span><span class="sxs-lookup"><span data-stu-id="90d44-315">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="90d44-316">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="90d44-316">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="90d44-317">**glgetcolortableext**</span><span class="sxs-lookup"><span data-stu-id="90d44-317">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="90d44-318">**glgetcolortableparameterfvext**</span><span class="sxs-lookup"><span data-stu-id="90d44-318">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="90d44-319">**glgetcolortableparameterivext**</span><span class="sxs-lookup"><span data-stu-id="90d44-319">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="90d44-320">**wglgetprocaddress**</span><span class="sxs-lookup"><span data-stu-id="90d44-320">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





