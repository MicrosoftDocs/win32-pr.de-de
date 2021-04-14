---
title: glCopyTexSubImage2D-Funktion (GL. h)
description: Die glCopyTexSubImage2D-Funktion kopiert ein untergeordnetes Bild eines zweidimensionalen Textur Bilds aus dem Framebuffer.
ms.assetid: cbb644d4-6a23-4d66-8599-5f8b48e9b91f
keywords:
- glCopyTexSubImage2D-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c966d031bb154b59cc54ae2e5d254347aa88d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391992"
---
# <a name="glcopytexsubimage2d-function"></a><span data-ttu-id="a67bb-104">glCopyTexSubImage2D-Funktion</span><span class="sxs-lookup"><span data-stu-id="a67bb-104">glCopyTexSubImage2D function</span></span>

<span data-ttu-id="a67bb-105">Die **glCopyTexSubImage2D** -Funktion kopiert ein untergeordnetes Bild eines zweidimensionalen Textur Bilds aus dem Framebuffer.</span><span class="sxs-lookup"><span data-stu-id="a67bb-105">The **glCopyTexSubImage2D** function copies a sub-image of a two-dimensional texture image from the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a67bb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a67bb-106">Syntax</span></span>


```C++
void WINAPI glCopyTexSubImage2D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   yoffset,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="a67bb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a67bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a67bb-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="a67bb-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="a67bb-109">Das Ziel, in das die Bilddaten geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a67bb-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="a67bb-110">Muss den Wert "GL \_ Texture \_ 2D" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a67bb-110">Must have the value GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="a67bb-111">*level*</span><span class="sxs-lookup"><span data-stu-id="a67bb-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="a67bb-112">Die Detailebene.</span><span class="sxs-lookup"><span data-stu-id="a67bb-112">The level-of-detail number.</span></span> <span data-ttu-id="a67bb-113">Ebene 0 ist das Basis Image.</span><span class="sxs-lookup"><span data-stu-id="a67bb-113">Level 0 is the base image.</span></span> <span data-ttu-id="a67bb-114">Ebene *n* ist das *n*-te MipMap-Reduzierungs Bild.</span><span class="sxs-lookup"><span data-stu-id="a67bb-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="a67bb-115">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="a67bb-115">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="a67bb-116">Der textOffset in der *x* -Richtung innerhalb des Textur Arrays.</span><span class="sxs-lookup"><span data-stu-id="a67bb-116">The texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="a67bb-117">*yoffset*</span><span class="sxs-lookup"><span data-stu-id="a67bb-117">*yoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="a67bb-118">Der texveroffset in der *y* -Richtung innerhalb des Textur Arrays.</span><span class="sxs-lookup"><span data-stu-id="a67bb-118">The texel offset in the *y* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="a67bb-119">*x*</span><span class="sxs-lookup"><span data-stu-id="a67bb-119">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="a67bb-120">Die x-Ebenen-Koordinaten des Fensters der unteren linken Ecke der Zeile der zu kopierenden Pixel.</span><span class="sxs-lookup"><span data-stu-id="a67bb-120">The window x-plane coordinates of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="a67bb-121">*y*</span><span class="sxs-lookup"><span data-stu-id="a67bb-121">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="a67bb-122">Die y-Ebenen-Koordinaten des Fensters der unteren linken Ecke der Zeile der zu kopierenden Pixel.</span><span class="sxs-lookup"><span data-stu-id="a67bb-122">The window y-plane coordinates of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="a67bb-123">*width*</span><span class="sxs-lookup"><span data-stu-id="a67bb-123">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="a67bb-124">Die Breite des unter Bilds des Textur Bilds.</span><span class="sxs-lookup"><span data-stu-id="a67bb-124">The width of the sub-image of the texture image.</span></span> <span data-ttu-id="a67bb-125">Das Angeben eines Textur unter Bilds mit einer Breite von NULL hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="a67bb-125">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="a67bb-126">*height*</span><span class="sxs-lookup"><span data-stu-id="a67bb-126">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="a67bb-127">Die Höhe des unter Bilds des Textur Bilds.</span><span class="sxs-lookup"><span data-stu-id="a67bb-127">The height of the sub-image of the texture image.</span></span> <span data-ttu-id="a67bb-128">Das Angeben eines Textur unter Bilds mit einer Breite von NULL hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="a67bb-128">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a67bb-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a67bb-129">Return value</span></span>

<span data-ttu-id="a67bb-130">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a67bb-130">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a67bb-131">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a67bb-131">Error codes</span></span>

<span data-ttu-id="a67bb-132">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a67bb-132">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a67bb-133">Name</span><span class="sxs-lookup"><span data-stu-id="a67bb-133">Name</span></span>                                                                                                  | <span data-ttu-id="a67bb-134">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a67bb-134">Meaning</span></span>                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a67bb-135"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a67bb-135"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="a67bb-136">Das *Ziel* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="a67bb-136">*target* was not an accepted value.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="a67bb-137"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="a67bb-137"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a67bb-138">die *Ebene* war kleiner als 0 (null) oder größer als *Log* 2 (*Max*), wobei *Max* der zurückgegebene Wert von GL \_ Max \_ Texture \_ size ist.</span><span class="sxs-lookup"><span data-stu-id="a67bb-138">*level* was less than zero or greater than *log* 2 (*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="a67bb-139"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="a67bb-139"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a67bb-140">*xoffset* war kleiner als der *Rahmen oder (* *xoffset*  +  *Width*) war größer als (*w*  +  *Border*), *yoffset* war kleiner als *Border*, oder (*yoffset*  +  *height*) war größer als (*h*  +  -Rahmen), wobei *w* für die Breite von GL und der Rahmen der \_ \_ GL-Textur Rahmen ist  \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a67bb-140">*xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), *yoffset* was less than *border*, or (*yoffset* + *height*) was greater than (*h* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER.</span></span> <span data-ttu-id="a67bb-141">Beachten Sie, dass *w* die doppelte *Rahmenbreite umfasst* .</span><span class="sxs-lookup"><span data-stu-id="a67bb-141">Note that *w* includes twice the *border* width.</span></span><br/> |
| <dl> <span data-ttu-id="a67bb-142"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="a67bb-142"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a67bb-143">" *Width* " war kleiner als " *Border* " oder " *y* " ist kleiner als " *Border*", wobei " *Border* " die Rahmenbreite des Textur Arrays ist.</span><span class="sxs-lookup"><span data-stu-id="a67bb-143">*width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.</span></span><br/>                                                                                                                                                                                           |
| <dl> <span data-ttu-id="a67bb-144"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="a67bb-144"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a67bb-145">Das Textur Array wurde nicht durch einen vorherigen [**glTexImage1D**](glteximage1d.md) -Vorgang definiert.</span><span class="sxs-lookup"><span data-stu-id="a67bb-145">The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.</span></span><br/>                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="a67bb-146"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="a67bb-146"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a67bb-147">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a67bb-147">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="a67bb-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a67bb-148">Remarks</span></span>

<span data-ttu-id="a67bb-149">Die **glCopyTexSubImage2D** -Funktion ersetzt einen rechteckigen Teil eines zweidimensionalen Textur Bilds durch Pixel aus dem aktuellen Framebuffer, nicht aus dem Hauptspeicher, wie es bei [**glTexSubImage2D**](gltexsubimage2d.md)der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="a67bb-149">The **glCopyTexSubImage2D** function replaces a rectangular portion of a two-dimensional texture image with pixels from the current framebuffer, rather than from main memory as is the case for [**glTexSubImage2D**](gltexsubimage2d.md).</span></span>

<span data-ttu-id="a67bb-150">Ein Rechteck aus Pixeln, beginnend mit *den x* -und *y* -Fenster Koordinaten und mit den Abmessungen *Width* und *height* , ersetzt den Teil des Textur Arrays durch *xoffset* + (*Width* -1), wobei die Indizes *yoffset* *durch* *yoffset* + (*Width* -1) auf der durch *Ebene* angegebenen MipMap-Ebene liegen.</span><span class="sxs-lookup"><span data-stu-id="a67bb-150">A rectangle of pixels beginning with the *x* and *y* window coordinates and with the dimensions *width* and *height* replaces the portion of the texture array with the indexes *xoffset* through *xoffset* + (*width* - 1), with the indexes *yoffset* through *yoffset* + (*width* - 1) at the mipmap level specified by *level*.</span></span> <span data-ttu-id="a67bb-151">Das Ziel Rechteck im Textur Array darf keine texeln außerhalb des ursprünglich angegebenen Textur Arrays enthalten.</span><span class="sxs-lookup"><span data-stu-id="a67bb-151">The destination rectangle in the texture array cannot include any texels outside the originally specified texture array.</span></span>

<span data-ttu-id="a67bb-152">Die **glCopyTexSubImage2D** -Funktion verarbeitet die Pixel in einer Zeile auf die gleiche Weise wie [**glcopypixels**](glcopypixels.md), mit dem Unterschied, dass vor der abschließenden Konvertierung der Pixel alle Pixel Komponenten Werte an den Bereich \[ 0, 1 gebunden und in das \] interne Format der Textur für die Speicherung im Textur Array konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="a67bb-152">The **glCopyTexSubImage2D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md), except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="a67bb-153">Die Pixel Reihenfolge wird mit niedrigeren *x* -Koordinaten bestimmt, die den unteren Texturkoordinaten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a67bb-153">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="a67bb-154">Wenn eine der Pixel innerhalb einer angegebenen Zeile des aktuellen Frame Puffer außerhalb des Fensters liegt, das dem aktuellen renderingkontext zugeordnet ist, sind ihre Werte nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a67bb-154">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="a67bb-155">Wenn einer der Pixel innerhalb des angegebenen Rechtecks des aktuellen Frame Puffer außerhalb des dem aktuellen renderingkontext zugeordneten Lese Fensters liegt, sind die für diese Pixel erhaltenen Werte nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a67bb-155">If any of the pixels within the specified rectangle of the current framebuffer are outside the read window associated with the current rendering context, then the values obtained for those pixels are undefined.</span></span> <span data-ttu-id="a67bb-156">An der *internalformat*-, *Width*-, *height*-oder *Border* -Parameter des angegebenen Textur Arrays oder an Texttyp außerhalb des angegebenen Textur unter Bilds wird keine Änderung vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="a67bb-156">No change is made to the *internalFormat*, *width*, *height*, or *border* parameter of the specified texture array or to texel values outside the specified texture sub-image.</span></span>

<span data-ttu-id="a67bb-157">Sie können **glCopyTexSubImage2D** -Aufrufe nicht in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="a67bb-157">You cannot include calls to **glCopyTexSubImage2D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="a67bb-158">Die **glCopyTexSubImage2D** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a67bb-158">The **glCopyTexSubImage2D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="a67bb-159">Die Texturierung hat keine Auswirkung auf den Farb Index Modus.</span><span class="sxs-lookup"><span data-stu-id="a67bb-159">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="a67bb-160">Die Funktionen " [**glpixelstore**](glpixelstore-functions.md) " und " [**glpixeltransfer**](glpixeltransfer.md) " beeinflussen die Textur Bilder genau so, wie Sie sich auf die Art und Weise auswirken, wie Pixel mithilfe von " [**gldrawpixels**](gldrawpixels.md)</span><span class="sxs-lookup"><span data-stu-id="a67bb-160">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect the way pixels are drawn using [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="a67bb-161">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glCopyTexSubImage2D** ab:</span><span class="sxs-lookup"><span data-stu-id="a67bb-161">The following functions retrieve information related to **glCopyTexSubImage2D**:</span></span>

[<span data-ttu-id="a67bb-162">**glgetteximage**</span><span class="sxs-lookup"><span data-stu-id="a67bb-162">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="a67bb-163">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Textur \_ 2D</span><span class="sxs-lookup"><span data-stu-id="a67bb-163">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="a67bb-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a67bb-164">Requirements</span></span>



| <span data-ttu-id="a67bb-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a67bb-165">Requirement</span></span> | <span data-ttu-id="a67bb-166">Wert</span><span class="sxs-lookup"><span data-stu-id="a67bb-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a67bb-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a67bb-167">Minimum supported client</span></span><br/> | <span data-ttu-id="a67bb-168">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a67bb-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a67bb-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a67bb-169">Minimum supported server</span></span><br/> | <span data-ttu-id="a67bb-170">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a67bb-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a67bb-171">Header</span><span class="sxs-lookup"><span data-stu-id="a67bb-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="a67bb-172"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a67bb-172"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a67bb-173">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a67bb-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="a67bb-174"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a67bb-174"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a67bb-175">DLL</span><span class="sxs-lookup"><span data-stu-id="a67bb-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a67bb-176"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a67bb-176"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a67bb-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a67bb-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a67bb-178">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a67bb-178">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a67bb-179">**glcopypixels**</span><span class="sxs-lookup"><span data-stu-id="a67bb-179">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="a67bb-180">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="a67bb-180">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="a67bb-181">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="a67bb-181">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="a67bb-182">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a67bb-182">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a67bb-183">**glnebel**</span><span class="sxs-lookup"><span data-stu-id="a67bb-183">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="a67bb-184">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="a67bb-184">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="a67bb-185">**glpixeltransfer**</span><span class="sxs-lookup"><span data-stu-id="a67bb-185">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="a67bb-186">**gltexd**</span><span class="sxs-lookup"><span data-stu-id="a67bb-186">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="a67bb-187">**gltexgen**</span><span class="sxs-lookup"><span data-stu-id="a67bb-187">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="a67bb-188">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="a67bb-188">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="a67bb-189">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="a67bb-189">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="a67bb-190">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="a67bb-190">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





