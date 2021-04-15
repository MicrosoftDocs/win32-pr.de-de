---
title: glpolygonstippel-Funktion (GL. h)
description: Die glpolygonstippel-Funktion legt das Polygon-stippling-Muster fest.
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- glpolygonstippel-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a2eb0b2e4319f7e3e37191fb197cd7ff86a2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477235"
---
# <a name="glpolygonstipple-function"></a><span data-ttu-id="9dda9-104">glpolygonstippel-Funktion</span><span class="sxs-lookup"><span data-stu-id="9dda9-104">glPolygonStipple function</span></span>

<span data-ttu-id="9dda9-105">Die **glpolygonstippel** -Funktion legt das Polygon-stippling-Muster fest.</span><span class="sxs-lookup"><span data-stu-id="9dda9-105">The **glPolygonStipple** function sets the polygon stippling pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dda9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dda9-106">Syntax</span></span>


```C++
void WINAPI glPolygonStipple(
   const GLubyte *mask
);
```



## <a name="parameters"></a><span data-ttu-id="9dda9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9dda9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dda9-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="9dda9-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="9dda9-109">Ein Zeiger auf ein 32x32-stippingmuster, das aus dem Arbeitsspeicher auf die gleiche Weise entpackt wird, wie " [**gldrawpixels**](gldrawpixels.md) " Pixel entpackt.</span><span class="sxs-lookup"><span data-stu-id="9dda9-109">A pointer to a 32x32 stipple pattern that will be unpacked from memory in the same way that [**glDrawPixels**](gldrawpixels.md) unpacks pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dda9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9dda9-110">Return value</span></span>

<span data-ttu-id="9dda9-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9dda9-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9dda9-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="9dda9-112">Error codes</span></span>

<span data-ttu-id="9dda9-113">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9dda9-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9dda9-114">Name</span><span class="sxs-lookup"><span data-stu-id="9dda9-114">Name</span></span>                                                                                                  | <span data-ttu-id="9dda9-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9dda9-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9dda9-116"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="9dda9-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9dda9-117">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9dda9-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9dda9-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9dda9-118">Remarks</span></span>

<span data-ttu-id="9dda9-119">Die **glpolygonstippel** -Funktion legt das Polygon-stippling-Muster fest.</span><span class="sxs-lookup"><span data-stu-id="9dda9-119">The **glPolygonStipple** function sets the polygon stippling pattern.</span></span> <span data-ttu-id="9dda9-120">Beim Polygon-stippling, wie z. b. Zeilen stippling (siehe [**glLineStipple**](gllinestipple.md)), werden bestimmte Fragmente maskiert, die von rasterization erzeugt werden, und ein Muster erstellt.</span><span class="sxs-lookup"><span data-stu-id="9dda9-120">Polygon stippling, like line stippling (see [**glLineStipple**](gllinestipple.md)), masks out certain fragments produced by rasterization, creating a pattern.</span></span> <span data-ttu-id="9dda9-121">Stippling ist unabhängig vom Polygon-Antialiasing.</span><span class="sxs-lookup"><span data-stu-id="9dda9-121">Stippling is independent of polygon antialiasing.</span></span>

<span data-ttu-id="9dda9-122">Der *Mask* -Parameter ist ein Zeiger auf ein 32 x 32-stippingmuster, das im Arbeitsspeicher gespeichert ist, genau wie die Pixeldaten, die für **gldrawpixels** bereitgestellt werden, wobei *Höhe* und *Breite* gleich 32, ein Pixel *Format* des GL \_ \_ -Farb Indexes und der *Datentyp* von GL \_ Bitmap sind.</span><span class="sxs-lookup"><span data-stu-id="9dda9-122">The *mask* parameter is a pointer to a 32x32 stipple pattern that is stored in memory just like the pixel data supplied to **glDrawPixels** with *height* and *width* both equal to 32, a pixel *format* of GL\_COLOR\_INDEX, and data *type* of GL\_BITMAP.</span></span> <span data-ttu-id="9dda9-123">Das Stippel Muster wird also als 32 x 32-Array von 1-Bit-Farbindizes dargestellt, die in nicht signierten Bytes verpackt sind.</span><span class="sxs-lookup"><span data-stu-id="9dda9-123">That is, the stipple pattern is represented as a 32x32 array of 1-bit color indexes packed in unsigned bytes.</span></span> <span data-ttu-id="9dda9-124">Die Parameter der [**glpixelstore**](glpixelstore-functions.md) -Funktion, wie z. b. gl \_ unpack \_ Swap \_ Bytes und GL \_ unpack \_ lsb \_ First, wirken sich auf die Zusammenstellung der Bits in ein Stippel Muster aus.</span><span class="sxs-lookup"><span data-stu-id="9dda9-124">The [**glPixelStore**](glpixelstore-functions.md) function parameters, such as GL\_UNPACK\_SWAP\_BYTES and GL\_UNPACK\_LSB\_FIRST, affect the assembling of the bits into a stipple pattern.</span></span> <span data-ttu-id="9dda9-125">Pixel Übertragungs Vorgänge (Shift, Offset und Pixel Map) werden jedoch nicht auf das Stippel Bild angewendet.</span><span class="sxs-lookup"><span data-stu-id="9dda9-125">Pixel transfer operations (shift, offset, and pixel map) are not applied to the stipple image, however.</span></span>

<span data-ttu-id="9dda9-126">Der Polygon-stippling ist mit " [**glEnable**](glenable.md) " und " **gldeaktivieren**" aktiviert und deaktiviert \_ \_</span><span class="sxs-lookup"><span data-stu-id="9dda9-126">Polygon stippling is enabled and disabled with [**glEnable**](glenable.md) and **glDisable**, using argument GL\_POLYGON\_STIPPLE.</span></span> <span data-ttu-id="9dda9-127">Wenn diese Option aktiviert ist, wird ein rasterisiertes Polygon Fragment mit den Fenster Koordinaten *x*<sub>w</sub> und *y*<sub>w</sub> nur dann an die nächste Stufe von OpenGL gesendet, wenn das (*x*<sub>w</sub> mod 32) Th-Bit in der (*y*<sub>w</sub> mod 32) Th-Zeile des stippingmusters 1 ist.</span><span class="sxs-lookup"><span data-stu-id="9dda9-127">If enabled, a rasterized polygon fragment with window coordinates *x*<sub>w</sub> and *y*<sub>w</sub> is sent to the next stage of OpenGL if and only if the (*x*<sub>w</sub> mod 32)th bit in the (*y*<sub>w</sub> mod 32)th row of the stipple pattern is one.</span></span> <span data-ttu-id="9dda9-128">Wenn das Polygon-stippling deaktiviert ist, ist es so, als ob es sich um ein stippingmuster handelt.</span><span class="sxs-lookup"><span data-stu-id="9dda9-128">When polygon stippling is disabled, it is as if the stipple pattern were all ones.</span></span>

<span data-ttu-id="9dda9-129">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glpolygonstiple** ab:</span><span class="sxs-lookup"><span data-stu-id="9dda9-129">The following functions retrieve information related to **glPolygonStipple**:</span></span>

[<span data-ttu-id="9dda9-130">**glgetpolygonstippel**</span><span class="sxs-lookup"><span data-stu-id="9dda9-130">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)

<span data-ttu-id="9dda9-131">[**glisenabled**](glisenabled.md) mit Argument GL \_ Polygon \_ Stippel</span><span class="sxs-lookup"><span data-stu-id="9dda9-131">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_STIPPLE</span></span>

## <a name="requirements"></a><span data-ttu-id="9dda9-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9dda9-132">Requirements</span></span>



| <span data-ttu-id="9dda9-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9dda9-133">Requirement</span></span> | <span data-ttu-id="9dda9-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9dda9-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9dda9-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9dda9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9dda9-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dda9-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9dda9-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9dda9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9dda9-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dda9-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9dda9-139">Header</span><span class="sxs-lookup"><span data-stu-id="9dda9-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dda9-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dda9-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9dda9-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9dda9-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="9dda9-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9dda9-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9dda9-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9dda9-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dda9-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dda9-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dda9-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9dda9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dda9-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9dda9-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9dda9-147">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="9dda9-147">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="9dda9-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9dda9-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9dda9-149">**gllinestippel**</span><span class="sxs-lookup"><span data-stu-id="9dda9-149">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="9dda9-150">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="9dda9-150">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="9dda9-151">**glpixeltransfer**</span><span class="sxs-lookup"><span data-stu-id="9dda9-151">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> </dl>

 

 





