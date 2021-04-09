---
title: glbitmap-Funktion (GL. h)
description: Die glbitmap-Funktion zeichnet eine Bitmap.
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- glbitmap-Funktion OpenGL
topic_type:
- apiref
api_name:
- glBitmap
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb97bb16a1e3c4c29d1dfb1a5320c02f44404d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040714"
---
# <a name="glbitmap-function"></a><span data-ttu-id="77c6b-104">glbitmap-Funktion</span><span class="sxs-lookup"><span data-stu-id="77c6b-104">glBitmap function</span></span>

<span data-ttu-id="77c6b-105">Die **glbitmap** -Funktion zeichnet eine Bitmap.</span><span class="sxs-lookup"><span data-stu-id="77c6b-105">The **glBitmap** function draws a bitmap.</span></span>

## <a name="syntax"></a><span data-ttu-id="77c6b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="77c6b-106">Syntax</span></span>


```C++
void WINAPI glBitmap(
         GLSizei width,
         GLSizei height,
         GLfloat xorig,
         GLfloat yorig,
         GLfloat xmove,
         GLfloat ymove,
   const GLubyte *bitmap
);
```



## <a name="parameters"></a><span data-ttu-id="77c6b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="77c6b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77c6b-108">*width*</span><span class="sxs-lookup"><span data-stu-id="77c6b-108">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="77c6b-109">Die Pixel Breite des Bitmap-Bilds.</span><span class="sxs-lookup"><span data-stu-id="77c6b-109">The pixel width of the bitmap image.</span></span>

</dd> <dt>

<span data-ttu-id="77c6b-110">*height*</span><span class="sxs-lookup"><span data-stu-id="77c6b-110">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="77c6b-111">Die Pixelhöhe des Bitmapbilds.</span><span class="sxs-lookup"><span data-stu-id="77c6b-111">The pixel height of the bitmap image.</span></span>

</dd> <dt>

<span data-ttu-id="77c6b-112">*xorig*</span><span class="sxs-lookup"><span data-stu-id="77c6b-112">*xorig*</span></span> 
</dt> <dd>

<span data-ttu-id="77c6b-113">Der *x* -Speicherort des Ursprungs im Bitmap-Bild.</span><span class="sxs-lookup"><span data-stu-id="77c6b-113">The *x* location of the origin in the bitmap image.</span></span> <span data-ttu-id="77c6b-114">Der Ursprung wird von der unteren linken Ecke der Bitmap gemessen, wobei die Pfeil nach rechts und nach oben die positiven Achsen bilden.</span><span class="sxs-lookup"><span data-stu-id="77c6b-114">The origin is measured from the lower-left corner of the bitmap, with right and up directions being the positive axes.</span></span>

</dd> <dt>

<span data-ttu-id="77c6b-115">*yorig*</span><span class="sxs-lookup"><span data-stu-id="77c6b-115">*yorig*</span></span> 
</dt> <dd>

<span data-ttu-id="77c6b-116">Die *y* -Position des Ursprungs im Bitmap-Bild.</span><span class="sxs-lookup"><span data-stu-id="77c6b-116">The *y* location of the origin in the bitmap image.</span></span> <span data-ttu-id="77c6b-117">Der Ursprung wird von der unteren linken Ecke der Bitmap gemessen, wobei die Pfeil nach rechts und nach oben die positiven Achsen bilden.</span><span class="sxs-lookup"><span data-stu-id="77c6b-117">The origin is measured from the lower-left corner of the bitmap, with right and up directions being the positive axes.</span></span>

</dd> <dt>

<span data-ttu-id="77c6b-118">*xmove*</span><span class="sxs-lookup"><span data-stu-id="77c6b-118">*xmove*</span></span> 
</dt> <dd>

<span data-ttu-id="77c6b-119">Der *x* -Offset, der der aktuellen Raster Position nach dem Zeichnen der Bitmap hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="77c6b-119">The *x* offset to be added to the current raster position after the bitmap is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="77c6b-120">*ymove*</span><span class="sxs-lookup"><span data-stu-id="77c6b-120">*ymove*</span></span> 
</dt> <dd>

<span data-ttu-id="77c6b-121">Der *y* -Offset, der der aktuellen Raster Position hinzugefügt werden soll, nachdem die Bitmap gezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="77c6b-121">The *y* offset to be added to the current raster position after the bitmap is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="77c6b-122">*Bitmap*</span><span class="sxs-lookup"><span data-stu-id="77c6b-122">*bitmap*</span></span> 
</dt> <dd>

<span data-ttu-id="77c6b-123">Die Adresse des Bitmapbilds.</span><span class="sxs-lookup"><span data-stu-id="77c6b-123">The address of the bitmap image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77c6b-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77c6b-124">Return value</span></span>

<span data-ttu-id="77c6b-125">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="77c6b-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="77c6b-126">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="77c6b-126">Error codes</span></span>

<span data-ttu-id="77c6b-127">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="77c6b-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="77c6b-128">Name</span><span class="sxs-lookup"><span data-stu-id="77c6b-128">Name</span></span>                                                                                                  | <span data-ttu-id="77c6b-129">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="77c6b-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="77c6b-130"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="77c6b-130"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="77c6b-131">*Breite* oder *Höhe* ist negativ.</span><span class="sxs-lookup"><span data-stu-id="77c6b-131">*width* or *height* is negative.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="77c6b-132"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="77c6b-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="77c6b-133">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="77c6b-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="77c6b-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77c6b-134">Remarks</span></span>

<span data-ttu-id="77c6b-135">Eine Bitmap ist ein binäres Bild.</span><span class="sxs-lookup"><span data-stu-id="77c6b-135">A bitmap is a binary image.</span></span> <span data-ttu-id="77c6b-136">Wenn Sie gezeichnet wird, wird die Bitmap relativ zur aktuellen Raster Position positioniert, und die in der Bitmap entsprechenden Frame Puffer Pixel werden mit der aktuellen Raster Farbe oder dem aktuellen Index geschrieben.</span><span class="sxs-lookup"><span data-stu-id="77c6b-136">When drawn, the bitmap is positioned relative to the current raster position, and framebuffer pixels corresponding to 1s in the bitmap are written using the current raster color or index.</span></span> <span data-ttu-id="77c6b-137">Frame-Puffer Pixel, die Nullen in der Bitmap entsprechen, werden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="77c6b-137">Frame-buffer pixels corresponding to zeros in the bitmap are not modified.</span></span>

<span data-ttu-id="77c6b-138">Das Bitmap-Bild wird wie Bilddaten für die Funktion " [**gldrawpixels**](gldrawpixels.md) " interpretiert, wobei " *Width* " und " *height* " den breiten-und Höhen Argumenten dieser Funktion entsprechen und der *Typ* auf die GL- \_ Bitmap und das *Format* auf "GL \_ Color Index" festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="77c6b-138">The bitmap image is interpreted like image data for the [**glDrawPixels**](gldrawpixels.md) function, with *width* and *height* corresponding to the width and height arguments of that function, and with *type* set to GL\_BITMAP and *format* set to GL\_COLOR\_INDEX.</span></span> <span data-ttu-id="77c6b-139">Modi, die Sie mithilfe von [**glpixelstore**](glpixelstore-functions.md) angeben, wirken sich auf die Interpretation von Bitmap-Bilddaten aus der Modus, den Sie mit [**glpixeltransfer**](glpixeltransfer.md) angeben, ist nicht.</span><span class="sxs-lookup"><span data-stu-id="77c6b-139">Modes you specify using [**glPixelStore**](glpixelstore-functions.md) affect the interpretation of bitmap image data; modes you specify using [**glPixelTransfer**](glpixeltransfer.md) do not.</span></span>

<span data-ttu-id="77c6b-140">Wenn die aktuelle Raster Position ungültig ist, wird **glbitmap** ignoriert.</span><span class="sxs-lookup"><span data-stu-id="77c6b-140">If the current raster position is invalid, **glBitmap** is ignored.</span></span> <span data-ttu-id="77c6b-141">Andernfalls wird die linke untere Ecke des Bitmap-Bilds an den folgenden Fenster Koordinaten positioniert:</span><span class="sxs-lookup"><span data-stu-id="77c6b-141">Otherwise, the lower-left corner of the bitmap image is positioned at the following window coordinates:</span></span>

<span data-ttu-id="77c6b-142">*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*?</span><span class="sxs-lookup"><span data-stu-id="77c6b-142">*x*<sub>w</sub> = *x*<sub>r</sub> *x*?</span></span>

<span data-ttu-id="77c6b-143">*y*<sub>w</sub>  =  *y*<sub>r</sub> *y*?</span><span class="sxs-lookup"><span data-stu-id="77c6b-143">*y*<sub>w</sub> = *y*<sub>r</sub> *y*?</span></span>

<span data-ttu-id="77c6b-144">In diesen Koordinaten ist (*x*<sub>r</sub> , *y*<sub>r</sub> ) die Raster Position, und (*x*?</span><span class="sxs-lookup"><span data-stu-id="77c6b-144">In these coordinates, (*x*<sub>r</sub> , *y*<sub>r</sub> ) is the raster position, and (*x*?</span></span> <span data-ttu-id="77c6b-145">, *y*?</span><span class="sxs-lookup"><span data-stu-id="77c6b-145">, *y*?</span></span> <span data-ttu-id="77c6b-146">) ist der bitmapursprung.</span><span class="sxs-lookup"><span data-stu-id="77c6b-146">) is the bitmap origin.</span></span> <span data-ttu-id="77c6b-147">Fragmente werden dann für jedes Pixel generiert, das einem 1 im Bitmap-Bild entspricht.</span><span class="sxs-lookup"><span data-stu-id="77c6b-147">Fragments are then generated for each pixel corresponding to a 1 in the bitmap image.</span></span> <span data-ttu-id="77c6b-148">Diese Fragmente werden mithilfe der aktuellen Raster- *z*-Koordinate, des Farb-oder Farb Index und der aktuellen Rastertextur Koordinaten generiert.</span><span class="sxs-lookup"><span data-stu-id="77c6b-148">These fragments are generated using the current raster *z*-coordinate, color or color index, and current raster texture coordinates.</span></span> <span data-ttu-id="77c6b-149">Sie werden dann genauso behandelt, als würden Sie von einem Punkt, einer Linie oder einem Polygon generiert werden, einschließlich Textur Zuordnung, Fogging und sämtlicher Vorgänge pro Fragment, z. b. Alpha-und tiefen Tests.</span><span class="sxs-lookup"><span data-stu-id="77c6b-149">They are then treated just as if they had been generated by a point, line, or polygon, including texture mapping, fogging, and all per-fragment operations such as alpha and depth testing.</span></span>

<span data-ttu-id="77c6b-150">Nachdem die Bitmap gezeichnet wurde, werden die *x* -und *y* -Koordinaten der aktuellen Raster Position durch *xmove* und *ymove* versetzt.</span><span class="sxs-lookup"><span data-stu-id="77c6b-150">After the bitmap has been drawn, the *x* and *y* coordinates of the current raster position are offset by *xmove* and *ymove*.</span></span> <span data-ttu-id="77c6b-151">An der *z*-Koordinate der aktuellen Raster Position oder an der aktuellen Raster Farbe, dem Index oder den Texturkoordinaten wird keine Änderung vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="77c6b-151">No change is made to the *z*-coordinate of the current raster position, or to the current raster color, index, or texture coordinates.</span></span>

<span data-ttu-id="77c6b-152">Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **glbitmap** " ab:</span><span class="sxs-lookup"><span data-stu-id="77c6b-152">The following functions retrieve information related to the **glBitmap** function:</span></span>

<span data-ttu-id="77c6b-153">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ aktuelle \_ Raster \_ Position</span><span class="sxs-lookup"><span data-stu-id="77c6b-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>

 

<span data-ttu-id="77c6b-154">**glget** mit dem Argument GL \_ aktuelle \_ Raster \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="77c6b-154">**glGet** with argument GL\_CURRENT\_RASTER\_COLOR</span></span>

 

<span data-ttu-id="77c6b-155">**glget** mit dem Argument GL \_ Current \_ Raster \_ Index</span><span class="sxs-lookup"><span data-stu-id="77c6b-155">**glGet** with argument GL\_CURRENT\_RASTER\_INDEX</span></span>

 

<span data-ttu-id="77c6b-156">**glget** mit dem Argument GL \_ Current \_ Raster \_ Textur \_ CoOrds</span><span class="sxs-lookup"><span data-stu-id="77c6b-156">**glGet** with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>

 

<span data-ttu-id="77c6b-157">**glget** mit dem Argument GL \_ aktuelle \_ Raster \_ Position \_ gültig</span><span class="sxs-lookup"><span data-stu-id="77c6b-157">**glGet** with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>

## <a name="requirements"></a><span data-ttu-id="77c6b-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77c6b-158">Requirements</span></span>



| <span data-ttu-id="77c6b-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77c6b-159">Requirement</span></span> | <span data-ttu-id="77c6b-160">Wert</span><span class="sxs-lookup"><span data-stu-id="77c6b-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77c6b-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77c6b-161">Minimum supported client</span></span><br/> | <span data-ttu-id="77c6b-162">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77c6b-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="77c6b-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77c6b-163">Minimum supported server</span></span><br/> | <span data-ttu-id="77c6b-164">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77c6b-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77c6b-165">Header</span><span class="sxs-lookup"><span data-stu-id="77c6b-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="77c6b-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="77c6b-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="77c6b-167">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="77c6b-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="77c6b-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77c6b-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="77c6b-169">DLL</span><span class="sxs-lookup"><span data-stu-id="77c6b-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77c6b-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77c6b-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77c6b-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77c6b-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77c6b-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="77c6b-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="77c6b-173">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="77c6b-173">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="77c6b-174">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="77c6b-174">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="77c6b-175">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="77c6b-175">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="77c6b-176">**glpixeltransfer**</span><span class="sxs-lookup"><span data-stu-id="77c6b-176">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="77c6b-177">**glRasterPos**</span><span class="sxs-lookup"><span data-stu-id="77c6b-177">**glRasterPos**</span></span>](glrasterpos-functions.md)
</dt> </dl>

 

 





