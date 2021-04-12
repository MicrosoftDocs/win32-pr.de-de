---
title: glCopyTexSubImage1D-Funktion (GL. h)
description: Die glCopyTexSubImage1D-Funktion kopiert ein unter Bild eines eindimensionalen Textur Bilds aus dem Framebuffer.
ms.assetid: 718aee8a-6dce-49e1-a441-19beccd89f8d
keywords:
- glCopyTexSubImage1D-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64006f9cec7e5fd2f3ca6f860249e579b16dbf10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956700"
---
# <a name="glcopytexsubimage1d-function"></a><span data-ttu-id="48e9e-104">glCopyTexSubImage1D-Funktion</span><span class="sxs-lookup"><span data-stu-id="48e9e-104">glCopyTexSubImage1D function</span></span>

<span data-ttu-id="48e9e-105">Die **glCopyTexSubImage1D** -Funktion kopiert ein unter Bild eines eindimensionalen Textur Bilds aus dem Framebuffer.</span><span class="sxs-lookup"><span data-stu-id="48e9e-105">The **glCopyTexSubImage1D** function copies a sub-image of a one-dimensional texture image from the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="48e9e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="48e9e-106">Syntax</span></span>


```C++
void WINAPI glCopyTexSubImage1D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   x,
   GLint   y,
   GLsizei width
);
```



## <a name="parameters"></a><span data-ttu-id="48e9e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="48e9e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48e9e-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="48e9e-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="48e9e-109">Das Ziel, in das die Bilddaten geändert werden.</span><span class="sxs-lookup"><span data-stu-id="48e9e-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="48e9e-110">Muss den Wert "GL \_ Texture \_ 1D" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="48e9e-110">Must have the value GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="48e9e-111">*level*</span><span class="sxs-lookup"><span data-stu-id="48e9e-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="48e9e-112">Die Detailebene.</span><span class="sxs-lookup"><span data-stu-id="48e9e-112">The level-of-detail number.</span></span> <span data-ttu-id="48e9e-113">Ebene 0 ist das Basis Image.</span><span class="sxs-lookup"><span data-stu-id="48e9e-113">Level 0 is the base image.</span></span> <span data-ttu-id="48e9e-114">Ebene *n* ist das *n*-te MipMap-Reduzierungs Bild.</span><span class="sxs-lookup"><span data-stu-id="48e9e-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="48e9e-115">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="48e9e-115">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="48e9e-116">Der texveroffset innerhalb des Textur Arrays.</span><span class="sxs-lookup"><span data-stu-id="48e9e-116">The texel offset within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="48e9e-117">*x*</span><span class="sxs-lookup"><span data-stu-id="48e9e-117">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="48e9e-118">Die x-Ebenen-Koordinate der unteren linken Ecke der Zeile der zu kopierenden Pixel.</span><span class="sxs-lookup"><span data-stu-id="48e9e-118">The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="48e9e-119">*y*</span><span class="sxs-lookup"><span data-stu-id="48e9e-119">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="48e9e-120">Die y-ebenenkoordinate des Fensters der unteren linken Ecke der Zeile der zu kopierenden Pixel.</span><span class="sxs-lookup"><span data-stu-id="48e9e-120">The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="48e9e-121">*width*</span><span class="sxs-lookup"><span data-stu-id="48e9e-121">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="48e9e-122">Die Breite des unter Bilds des Textur Bilds.</span><span class="sxs-lookup"><span data-stu-id="48e9e-122">The width of the sub-image of the texture image.</span></span> <span data-ttu-id="48e9e-123">Das Angeben eines Textur unter Bilds mit einer Breite von NULL hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="48e9e-123">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48e9e-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48e9e-124">Return value</span></span>

<span data-ttu-id="48e9e-125">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="48e9e-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="48e9e-126">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="48e9e-126">Error codes</span></span>

<span data-ttu-id="48e9e-127">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="48e9e-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="48e9e-128">Name</span><span class="sxs-lookup"><span data-stu-id="48e9e-128">Name</span></span>                                                                                                  | <span data-ttu-id="48e9e-129">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="48e9e-129">Meaning</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48e9e-130"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="48e9e-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="48e9e-131">Das *Ziel* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="48e9e-131">*target* was not an accepted value.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="48e9e-132"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="48e9e-132"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="48e9e-133">die *Ebene* war kleiner als 0 (null), oder die *Ebene* ist größer als *Log* 2 (*Max*), wobei *Max* der zurückgegebene Wert von GL \_ Max \_ Texture \_ size ist.</span><span class="sxs-lookup"><span data-stu-id="48e9e-133">*level* was less than zero or *level* is greater than *log* 2(*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="48e9e-134"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="48e9e-134"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="48e9e-135">*xoffset* war kleiner als der *Rahmen oder (* *xoffset*  +  *Width*) war größer als (*w*-Rahmen  +  ), wobei *w* die Breite von GL und der Rahmen der \_ \_ GL-Textur Rahmen ist  \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="48e9e-135">*xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER.</span></span> <span data-ttu-id="48e9e-136">Beachten Sie, dass *w* die doppelte *Rahmenbreite umfasst* .</span><span class="sxs-lookup"><span data-stu-id="48e9e-136">Note that *w* includes twice the *border* width.</span></span><br/> |
| <dl> <span data-ttu-id="48e9e-137"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="48e9e-137"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="48e9e-138">" *Width* " war kleiner als " *Border* " oder " *y* " ist kleiner als " *Border*", wobei " *Border* " die Rahmenbreite des Textur Arrays ist.</span><span class="sxs-lookup"><span data-stu-id="48e9e-138">*width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="48e9e-139"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="48e9e-139"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="48e9e-140">Das Textur Array wurde nicht durch einen vorherigen [**glTexImage1D**](glteximage1d.md) -Vorgang definiert.</span><span class="sxs-lookup"><span data-stu-id="48e9e-140">The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="48e9e-141"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="48e9e-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="48e9e-142">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="48e9e-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                        |



## <a name="remarks"></a><span data-ttu-id="48e9e-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48e9e-143">Remarks</span></span>

<span data-ttu-id="48e9e-144">Die **glCopyTexSubImage1D** -Funktion ersetzt einen Teil eines eindimensionalen Textur Bilds mithilfe von Pixeln aus dem aktuellen Framebuffer, nicht aus dem Hauptspeicher, wie es bei [**glTexSubImage1D**](gltexsubimage1d.md)der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="48e9e-144">The **glCopyTexSubImage1D** function replaces a portion of a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexSubImage1D**](gltexsubimage1d.md).</span></span>

<span data-ttu-id="48e9e-145">Eine Zeile mit Pixeln, beginnend mit den durch *x* und *y* angegebenen Fenster Koordinaten und mit der Längen *Breite* , ersetzt den Teil des Textur *Arrays durch xoffset +* (  *Width* -1).</span><span class="sxs-lookup"><span data-stu-id="48e9e-145">A row of pixels beginning with the window coordinates specified by *x* and *y* and with the length *width* replaces the portion of the texture array with the indexes *xoffset* through *xoffset* + (*width* - 1).</span></span> <span data-ttu-id="48e9e-146">Das Ziel im Textur Array darf keine texeln außerhalb des ursprünglich angegebenen Textur Arrays enthalten.</span><span class="sxs-lookup"><span data-stu-id="48e9e-146">The destination in the texture array cannot include any texels outside the originally specified texture array.</span></span>

<span data-ttu-id="48e9e-147">Die **glCopyTexSubImage1D** -Funktion verarbeitet die Pixel in einer Zeile auf die gleiche Weise wie [**glcopypixels**](glcopypixels.md) , mit dem Unterschied, dass vor der abschließenden Konvertierung der Pixel alle Pixel Komponenten Werte an den Bereich \[ 0, 1 gebunden \] und in das interne Format der Textur für die Speicherung im Textur Array konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="48e9e-147">The **glCopyTexSubImage1D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md) except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="48e9e-148">Die Pixel Reihenfolge wird mit niedrigeren *x* -Koordinaten bestimmt, die den unteren Texturkoordinaten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="48e9e-148">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="48e9e-149">Wenn eine der Pixel innerhalb einer angegebenen Zeile des aktuellen Frame Puffer außerhalb des Fensters liegt, das dem aktuellen renderingkontext zugeordnet ist, sind ihre Werte nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="48e9e-149">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="48e9e-150">Der *internalformat*-, *Width*-oder Border-Parameter des angegebenen Textur Arrays oder der *Border* -Wert außerhalb des angegebenen Textur unter Bilds wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="48e9e-150">No change is made to the *internalFormat*, *width*, or *border* parameter of the specified texture array or to texel values outside the specified texture sub-image.</span></span>

<span data-ttu-id="48e9e-151">Sie können **glCopyTexSubImage1D** -Aufrufe nicht in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="48e9e-151">You cannot include calls to **glCopyTexSubImage1D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="48e9e-152">Die **glCopyTexSubImage1D** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="48e9e-152">The **glCopyTexSubImage1D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="48e9e-153">Die Texturierung hat keine Auswirkung auf den Farb Index Modus.</span><span class="sxs-lookup"><span data-stu-id="48e9e-153">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="48e9e-154">Die Funktionen " [**glpixelstore**](glpixelstore-functions.md) " und " [**glpixeltransfer**](glpixeltransfer.md) " beeinflussen die Textur Bilder genau so, wie Sie sich auf die Art und Weise auswirken, wie Pixel mithilfe von " [**gldrawpixels**](gldrawpixels.md)</span><span class="sxs-lookup"><span data-stu-id="48e9e-154">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect the way pixels are drawn using [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="48e9e-155">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glCopyTexSubImage1D** ab:</span><span class="sxs-lookup"><span data-stu-id="48e9e-155">The following functions retrieve information related to **glCopyTexSubImage1D**:</span></span>

[<span data-ttu-id="48e9e-156">**glgetteximage**</span><span class="sxs-lookup"><span data-stu-id="48e9e-156">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="48e9e-157">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Texture \_ 1D</span><span class="sxs-lookup"><span data-stu-id="48e9e-157">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="48e9e-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48e9e-158">Requirements</span></span>



| <span data-ttu-id="48e9e-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48e9e-159">Requirement</span></span> | <span data-ttu-id="48e9e-160">Wert</span><span class="sxs-lookup"><span data-stu-id="48e9e-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48e9e-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48e9e-161">Minimum supported client</span></span><br/> | <span data-ttu-id="48e9e-162">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48e9e-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="48e9e-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48e9e-163">Minimum supported server</span></span><br/> | <span data-ttu-id="48e9e-164">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48e9e-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="48e9e-165">Header</span><span class="sxs-lookup"><span data-stu-id="48e9e-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="48e9e-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="48e9e-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="48e9e-167">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48e9e-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="48e9e-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48e9e-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="48e9e-169">DLL</span><span class="sxs-lookup"><span data-stu-id="48e9e-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48e9e-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48e9e-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48e9e-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48e9e-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48e9e-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="48e9e-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="48e9e-173">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="48e9e-173">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="48e9e-174">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="48e9e-174">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="48e9e-175">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="48e9e-175">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="48e9e-176">**glnebel**</span><span class="sxs-lookup"><span data-stu-id="48e9e-176">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="48e9e-177">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="48e9e-177">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="48e9e-178">**glpixeltransfer**</span><span class="sxs-lookup"><span data-stu-id="48e9e-178">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="48e9e-179">**gltexd**</span><span class="sxs-lookup"><span data-stu-id="48e9e-179">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="48e9e-180">**gltexgen**</span><span class="sxs-lookup"><span data-stu-id="48e9e-180">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="48e9e-181">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="48e9e-181">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="48e9e-182">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="48e9e-182">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="48e9e-183">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="48e9e-183">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="48e9e-184">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="48e9e-184">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="48e9e-185">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="48e9e-185">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





