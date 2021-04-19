---
title: glpixelzoom-Funktion (GL. h)
description: Die glpixelzoom-Funktion gibt die Pixel Zoomfaktoren an.
ms.assetid: 57ead7d8-0502-46b4-9f66-dbb3cb75b0f9
keywords:
- glpixelzoom-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPixelZoom
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 065e1735ca0228046cfb08e2fb441d3cdc02af74
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106369924"
---
# <a name="glpixelzoom-function"></a><span data-ttu-id="7147a-104">glpixelzoom-Funktion</span><span class="sxs-lookup"><span data-stu-id="7147a-104">glPixelZoom function</span></span>

<span data-ttu-id="7147a-105">Die **glpixelzoom** -Funktion gibt die Pixel Zoomfaktoren an.</span><span class="sxs-lookup"><span data-stu-id="7147a-105">The **glPixelZoom** function specifies the pixel zoom factors.</span></span>

## <a name="syntax"></a><span data-ttu-id="7147a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7147a-106">Syntax</span></span>


```C++
void WINAPI glPixelZoom(
   GLfloat xfactor,
   GLfloat yfactor
);
```



## <a name="parameters"></a><span data-ttu-id="7147a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7147a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7147a-108">*xfactor*</span><span class="sxs-lookup"><span data-stu-id="7147a-108">*xfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="7147a-109">Der *x* -Zoomfaktor für Pixel Schreibvorgänge.</span><span class="sxs-lookup"><span data-stu-id="7147a-109">The *x* zoom factor for pixel write operations.</span></span>

</dd> <dt>

<span data-ttu-id="7147a-110">*yfactor*</span><span class="sxs-lookup"><span data-stu-id="7147a-110">*yfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="7147a-111">Der *y* -Zoomfaktor für Pixel Schreibvorgänge.</span><span class="sxs-lookup"><span data-stu-id="7147a-111">The *y* zoom factor for pixel write operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7147a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7147a-112">Return value</span></span>

<span data-ttu-id="7147a-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7147a-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7147a-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7147a-114">Error codes</span></span>

<span data-ttu-id="7147a-115">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7147a-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7147a-116">Name</span><span class="sxs-lookup"><span data-stu-id="7147a-116">Name</span></span>                                                                                                  | <span data-ttu-id="7147a-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7147a-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7147a-118"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="7147a-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7147a-119">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7147a-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7147a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7147a-120">Remarks</span></span>

<span data-ttu-id="7147a-121">Die **glpixelzoom** -Funktion gibt Werte für die *x* -und *y* -Zoomfaktoren an.</span><span class="sxs-lookup"><span data-stu-id="7147a-121">The **glPixelZoom** function specifies values for the *x* and *y* zoom factors.</span></span> <span data-ttu-id="7147a-122">Bei der Ausführung von [**gldrawpixels**](gldrawpixels.md) oder [**glcopypixels**](glcopypixels.md), wenn (*x*<sub>r</sub> ,*y*<sub>r</sub> ) die aktuelle Raster Position ist, und ein angegebenes Element in der *n*-ten Zeile und *m*.-Spalte des Pixel Rechtecks liegt, dann Pixel, deren zentriert im Rechteck mit Ecken</span><span class="sxs-lookup"><span data-stu-id="7147a-122">During the execution of [**glDrawPixels**](gldrawpixels.md) or [**glCopyPixels**](glcopypixels.md), if (*x*<sub>r</sub> ,*y*<sub>r</sub> ) is the current raster position, and a given element is in the *n* th row and *m* th column of the pixel rectangle, then pixels whose centers are in the rectangle with corners at</span></span>

![Gleichung, die die Orte anzeigt, an denen Pixel Kandidaten für die Ersetzung sind.](images/pix05.png)

<span data-ttu-id="7147a-124">sind Kandidaten für die Ersetzung.</span><span class="sxs-lookup"><span data-stu-id="7147a-124">are candidates for replacement.</span></span> <span data-ttu-id="7147a-125">Alle Pixel, deren Mitte am unteren oder linken Rand dieses rechteckigen Bereichs liegt, werden ebenfalls geändert.</span><span class="sxs-lookup"><span data-stu-id="7147a-125">Any pixel whose center lies on the bottom or left edge of this rectangular region is also modified.</span></span>

<span data-ttu-id="7147a-126">Die Pixel Zoomfaktoren sind nicht auf positive Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="7147a-126">Pixel zoom factors are not limited to positive values.</span></span> <span data-ttu-id="7147a-127">Negative Zoomfaktoren spiegeln das resultierende Bild der aktuellen Raster Position wider.</span><span class="sxs-lookup"><span data-stu-id="7147a-127">Negative zoom factors reflect the resulting image about the current raster position.</span></span>

<span data-ttu-id="7147a-128">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glpixelzoom** ab:</span><span class="sxs-lookup"><span data-stu-id="7147a-128">The following functions retrieve information related to **glPixelZoom**:</span></span>

<span data-ttu-id="7147a-129">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Zoom \_ X</span><span class="sxs-lookup"><span data-stu-id="7147a-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ZOOM\_X</span></span>

<span data-ttu-id="7147a-130">**glget** mit dem Argument GL \_ Zoom \_ Y</span><span class="sxs-lookup"><span data-stu-id="7147a-130">**glGet** with argument GL\_ZOOM\_Y</span></span>

## <a name="requirements"></a><span data-ttu-id="7147a-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7147a-131">Requirements</span></span>



| <span data-ttu-id="7147a-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7147a-132">Requirement</span></span> | <span data-ttu-id="7147a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7147a-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7147a-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7147a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7147a-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7147a-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7147a-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7147a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7147a-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7147a-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7147a-138">Header</span><span class="sxs-lookup"><span data-stu-id="7147a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7147a-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7147a-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7147a-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7147a-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="7147a-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7147a-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7147a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7147a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7147a-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7147a-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7147a-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7147a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7147a-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7147a-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7147a-146">**glcopypixels**</span><span class="sxs-lookup"><span data-stu-id="7147a-146">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="7147a-147">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="7147a-147">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="7147a-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7147a-148">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





