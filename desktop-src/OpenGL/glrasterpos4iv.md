---
title: glRasterPos4iv-Funktion (GL. h)
description: Gibt die Raster Position für Pixel Vorgänge an. | glRasterPos4iv-Funktion (GL. h)
ms.assetid: d50cf8ea-6edb-474d-ace5-4e5ba454d498
keywords:
- glRasterPos4iv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRasterPos4iv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401ead1c9134b8a6c4465352f215a2a466caaf1c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352349"
---
# <a name="glrasterpos4iv-function"></a><span data-ttu-id="e63d6-105">glRasterPos4iv-Funktion</span><span class="sxs-lookup"><span data-stu-id="e63d6-105">glRasterPos4iv function</span></span>

<span data-ttu-id="e63d6-106">Gibt die Raster Position für Pixel Vorgänge an.</span><span class="sxs-lookup"><span data-stu-id="e63d6-106">Specifies the raster position for pixel operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="e63d6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e63d6-107">Syntax</span></span>


```C++
void WINAPI glRasterPos4iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="e63d6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e63d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e63d6-109">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="e63d6-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="e63d6-110">Ein Zeiger auf ein Array aus vier Elementen, der x-, y-, z-und w-Koordinaten für die aktuelle Raster Position angibt.</span><span class="sxs-lookup"><span data-stu-id="e63d6-110">A pointer to an array of four elements, specifying x, y, z, and w coordinates for the current raster position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e63d6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e63d6-111">Return value</span></span>

<span data-ttu-id="e63d6-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e63d6-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e63d6-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e63d6-113">Remarks</span></span>

<span data-ttu-id="e63d6-114">OpenGL verwaltet eine 3D-Position in Fenster Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="e63d6-114">OpenGL maintains a 3-D position in window coordinates.</span></span> <span data-ttu-id="e63d6-115">Diese Position, die als Raster Position bezeichnet wird, wird mit der unter Pixelgenauigkeit beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e63d6-115">This position, called the raster position, is maintained with subpixel accuracy.</span></span> <span data-ttu-id="e63d6-116">Sie wird verwendet, um Pixel-und Bitmap-Schreibvorgänge zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="e63d6-116">It is used to position pixel and bitmap write operations.</span></span> <span data-ttu-id="e63d6-117">Weitere Informationen finden Sie unter [**glbitmap**](glbitmap.md), [**gldrawpixels**](gldrawpixels.md)und [**glcopypixels**](glcopypixels.md).</span><span class="sxs-lookup"><span data-stu-id="e63d6-117">See [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md), and [**glCopyPixels**](glcopypixels.md).</span></span>

<span data-ttu-id="e63d6-118">Die aktuelle Raster Position besteht aus drei Fenster Koordinaten (*x, y, z*), einem Ausschneide *Koordinaten Wert, einer Augen Koordinaten Entfernung* , einem gültigen Bit und zugeordneten Farbdaten und Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="e63d6-118">The current raster position consists of three window coordinates (*x, y, z*), a clip coordinate *w* value, an eye coordinate distance, a valid bit, and associated color data and texture coordinates.</span></span> <span data-ttu-id="e63d6-119">Die *w* -Koordinate ist eine Clip Koordinate, da *w* nicht zu Fenster Koordinaten projiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e63d6-119">The *w* coordinate is a clip coordinate, because *w* is not projected to window coordinates.</span></span> <span data-ttu-id="e63d6-120">Die [glRasterPos4](glrasterpos-functions.md) -Funktion gibt die Objekt Koordinaten *x, y, z* und *w* explizit an.</span><span class="sxs-lookup"><span data-stu-id="e63d6-120">The [glRasterPos4](glrasterpos-functions.md) function specifies object coordinates *x, y, z*, and *w* explicitly.</span></span> <span data-ttu-id="e63d6-121">Die glRasterPos3-Funktion gibt die Objekt Koordinaten *x, y* und *z* explizit an, während *w* implizit auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e63d6-121">The glRasterPos3 function specifies object coordinates *x, y,* and *z* explicitly, while *w* is implicitly set to one.</span></span> <span data-ttu-id="e63d6-122">Die glRasterPos2-Funktion verwendet die Argument Werte für *x* und *y* , während *z* und *w* implizit auf NULL und 1 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e63d6-122">The glRasterPos2 function uses the argument values for *x* and *y* while implicitly setting *z* and *w* to zero and one.</span></span>

<span data-ttu-id="e63d6-123">Die von [glRasterPos](glrasterpos-functions.md) dargestellten Objekt Koordinaten werden genau wie die eines [glVertex](glvertex-functions.md) -Befehls behandelt.</span><span class="sxs-lookup"><span data-stu-id="e63d6-123">The object coordinates presented by [glRasterPos](glrasterpos-functions.md) are treated just like those of a [glVertex](glvertex-functions.md) command.</span></span> <span data-ttu-id="e63d6-124">Sie werden von der aktuellen Modelview-und Projektions Matrizen transformiert und an die clippingphase übergeben.</span><span class="sxs-lookup"><span data-stu-id="e63d6-124">They are transformed by the current modelview and projection matrices and passed to the clipping stage.</span></span> <span data-ttu-id="e63d6-125">Wenn der Scheitelpunkt nicht mit einem plotvorgang versehen ist, wird er projiziert und auf Fenster Koordinaten skaliert, die zur neuen aktuellen Raster Position werden, und das \_ gültige Flag für die aktuelle \_ Raster Position von GL \_ \_ wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e63d6-125">If the vertex is not culled, then it is projected and scaled to window coordinates, which become the new current raster position, and the GL\_CURRENT\_RASTER\_POSITION\_VALID flag is set.</span></span> <span data-ttu-id="e63d6-126">Wenn der Scheitelpunkt ein culled-Wert ist, wird das gültige Bit gelöscht, und die aktuelle Raster Position und die zugehörige Farbe und Texturkoordinaten sind nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="e63d6-126">If the vertex is culled, then the valid bit is cleared and the current raster position and associated color and texture coordinates are undefined.</span></span>

<span data-ttu-id="e63d6-127">Die aktuelle Raster Position enthält auch einige zugeordnete Farbdaten und Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="e63d6-127">The current raster position also includes some associated color data and texture coordinates.</span></span> <span data-ttu-id="e63d6-128">Wenn Beleuchtung aktiviert ist, wird die \_ aktuelle \_ Raster \_ Farbe (im RGBA-Modus) oder der \_ aktuelle "GL Current \_ Raster \_ Index" im Farb Index Modus auf die von der Beleuchtungs Berechnung erzeugte Farbe festgelegt (siehe [gllight](gllight-functions.md), [gllightmodel](gllightmodel-functions.md)und [**glshademodel**](glshademodel.md)).</span><span class="sxs-lookup"><span data-stu-id="e63d6-128">If lighting is enabled, then GL\_CURRENT\_RASTER\_COLOR, in RGBA mode, or the GL\_CURRENT\_RASTER\_INDEX, in color-index mode, is set to the color produced by the lighting calculation (see [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md), and [**glShadeModel**](glshademodel.md)).</span></span> <span data-ttu-id="e63d6-129">Wenn Beleuchtung deaktiviert ist, wird für die aktuelle Raster Farbe die aktuelle Farbe (im RGBA-Modus, die Status Variable "GL \_ Current \_ Color") oder der Farbindex (im Farb Index Modus, Zustands Variable "GL \_ Current \_ Index") verwendet.</span><span class="sxs-lookup"><span data-stu-id="e63d6-129">If lighting is disabled, current color (in RGBA mode, state variable GL\_CURRENT\_COLOR) or color index (in color-index mode, state variable GL\_CURRENT\_INDEX) is used to update the current raster color.</span></span>

<span data-ttu-id="e63d6-130">Entsprechend werden \_ die aktuellen \_ Raster \_ Textur \_ -CoOrds von GL als eine Funktion von GL \_ Current \_ Texture \_ CoOrds aktualisiert, basierend auf der Textur Matrix und den Funktionen der Textur Generierung (siehe [gltexgen](gltexgen-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="e63d6-130">Likewise, GL\_CURRENT\_RASTER\_TEXTURE\_COORDS is updated as a function of GL\_CURRENT\_TEXTURE\_COORDS, based on the texture matrix and the texture generation functions (see [glTexGen](gltexgen-functions.md)).</span></span> <span data-ttu-id="e63d6-131">Schließlich ersetzt der Abstand vom Ursprung des Augen Koordinatensystems zum Scheitelpunkt, der nur von der Modelview-Matrix transformiert wird, die aktuelle Version von GL \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e63d6-131">Finally, the distance from the origin of the eye coordinate system to the vertex, as transformed by only the modelview matrix, replaces GL\_CURRENT\_RASTER\_DISTANCE.</span></span>

<span data-ttu-id="e63d6-132">Anfänglich ist die aktuelle Raster Position (0, 0, 0, 1), die aktuelle Raster Entfernung ist 0, das gültige Bit ist festgelegt, die zugeordnete RGBA-Farbe (1, 1, 1, 1), der zugeordnete Farb Index ist 1, und die zugeordneten Texturkoordinaten lauten (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="e63d6-132">Initially, the current raster position is (0,0,0,1), the current raster distance is 0, the valid bit is set, the associated RGBA color is (1,1,1,1), the associated color index is 1, and the associated texture coordinates are (0, 0, 0, 1).</span></span> <span data-ttu-id="e63d6-133">Im RGBA-Modus ist "GL \_ Current \_ Raster \_ Index" immer 1. im Farb Index Modus behält die aktuelle Raster-RGBA-Farbe stets ihren Anfangswert bei.</span><span class="sxs-lookup"><span data-stu-id="e63d6-133">In RGBA mode, GL\_CURRENT\_RASTER\_INDEX is always 1; in color-index mode, the current raster RGBA color always maintains its initial value.</span></span>

> [!Note]  
> <span data-ttu-id="e63d6-134">Die Raster Position wird durch [glRasterPos](glrasterpos-functions.md) und durch [**glbitmap**](glbitmap.md)geändert.</span><span class="sxs-lookup"><span data-stu-id="e63d6-134">The raster position is modified both by [glRasterPos](glrasterpos-functions.md) and by [**glBitmap**](glbitmap.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="e63d6-135">Wenn die Raster Positionskoordinaten ungültig sind, werden Zeichenbefehle, die auf der Raster Position basieren, ignoriert (d. h., Sie führen nicht zu Änderungen am OpenGL-Zustand).</span><span class="sxs-lookup"><span data-stu-id="e63d6-135">When the raster position coordinates are invalid, drawing commands that are based on the raster position are ignored (that is, they do not result in changes to the OpenGL state).</span></span>

 

<span data-ttu-id="e63d6-136">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit [glRasterPos](glrasterpos-functions.md)abgerufen:</span><span class="sxs-lookup"><span data-stu-id="e63d6-136">The following functions retrieve information related to [glRasterPos](glrasterpos-functions.md):</span></span>

<dl>

<span data-ttu-id="e63d6-137">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ aktuelle \_ Raster \_ Position</span><span class="sxs-lookup"><span data-stu-id="e63d6-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>  
<span data-ttu-id="e63d6-138">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ aktuelle \_ Raster \_ Position \_ gültig</span><span class="sxs-lookup"><span data-stu-id="e63d6-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>  
<span data-ttu-id="e63d6-139">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ aktuelle \_ Raster \_ Entfernung</span><span class="sxs-lookup"><span data-stu-id="e63d6-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_DISTANCE</span></span>  
<span data-ttu-id="e63d6-140">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ aktuelle \_ Raster \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="e63d6-140">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_COLOR</span></span>  
<span data-ttu-id="e63d6-141">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Current \_ Raster \_ Index</span><span class="sxs-lookup"><span data-stu-id="e63d6-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_INDEX</span></span>  
<span data-ttu-id="e63d6-142">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Current \_ Raster \_ Textur \_ CoOrds</span><span class="sxs-lookup"><span data-stu-id="e63d6-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="e63d6-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e63d6-143">Requirements</span></span>



| <span data-ttu-id="e63d6-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e63d6-144">Requirement</span></span> | <span data-ttu-id="e63d6-145">Wert</span><span class="sxs-lookup"><span data-stu-id="e63d6-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e63d6-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e63d6-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e63d6-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e63d6-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e63d6-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e63d6-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e63d6-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e63d6-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e63d6-150">Header</span><span class="sxs-lookup"><span data-stu-id="e63d6-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="e63d6-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e63d6-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e63d6-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e63d6-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="e63d6-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e63d6-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e63d6-154">DLL</span><span class="sxs-lookup"><span data-stu-id="e63d6-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e63d6-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e63d6-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e63d6-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e63d6-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e63d6-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e63d6-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e63d6-158">**glbitmap**</span><span class="sxs-lookup"><span data-stu-id="e63d6-158">**glBitmap**</span></span>](glbitmap.md)
</dt> <dt>

[<span data-ttu-id="e63d6-159">**glcopypixels**</span><span class="sxs-lookup"><span data-stu-id="e63d6-159">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="e63d6-160">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="e63d6-160">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="e63d6-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e63d6-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e63d6-162">gllight</span><span class="sxs-lookup"><span data-stu-id="e63d6-162">glLight</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="e63d6-163">gllightmodel</span><span class="sxs-lookup"><span data-stu-id="e63d6-163">glLightModel</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="e63d6-164">**glshademodel**</span><span class="sxs-lookup"><span data-stu-id="e63d6-164">**glShadeModel**</span></span>](glshademodel.md)
</dt> <dt>

[<span data-ttu-id="e63d6-165">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="e63d6-165">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="e63d6-166">gltexgen</span><span class="sxs-lookup"><span data-stu-id="e63d6-166">glTexGen</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="e63d6-167">glVertex</span><span class="sxs-lookup"><span data-stu-id="e63d6-167">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





