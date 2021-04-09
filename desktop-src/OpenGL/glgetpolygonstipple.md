---
title: glgetpolygonstippel-Funktion (GL. h)
description: Die glgetpolygonstippel-Funktion gibt das Polygon Stippel Muster zurück.
ms.assetid: 95c1ebfa-8465-4bc1-b3f5-eed696a83816
keywords:
- glgetpolygonstippel-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643d0ea6b7583f26565ab7b9233f7df1dce9aead
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858724"
---
# <a name="glgetpolygonstipple-function"></a><span data-ttu-id="37c44-104">glgetpolygonstippel-Funktion</span><span class="sxs-lookup"><span data-stu-id="37c44-104">glGetPolygonStipple function</span></span>

<span data-ttu-id="37c44-105">Die **glgetpolygonstippel** -Funktion gibt das Polygon Stippel Muster zurück.</span><span class="sxs-lookup"><span data-stu-id="37c44-105">The **glGetPolygonStipple** function returns the polygon stipple pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="37c44-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="37c44-106">Syntax</span></span>


```C++
void WINAPI glGetPolygonStipple(
   GLubyte *mask
);
```



## <a name="parameters"></a><span data-ttu-id="37c44-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="37c44-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37c44-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="37c44-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="37c44-109">Gibt das Stippel Muster zurück.</span><span class="sxs-lookup"><span data-stu-id="37c44-109">Returns the stipple pattern.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37c44-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37c44-110">Return value</span></span>

<span data-ttu-id="37c44-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="37c44-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="37c44-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="37c44-112">Error codes</span></span>

<span data-ttu-id="37c44-113">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="37c44-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="37c44-114">Name</span><span class="sxs-lookup"><span data-stu-id="37c44-114">Name</span></span>                                                                                                  | <span data-ttu-id="37c44-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="37c44-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="37c44-116"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="37c44-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="37c44-117">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="37c44-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="37c44-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37c44-118">Remarks</span></span>

<span data-ttu-id="37c44-119">Die **glgetpolygonstippel** -Funktion gibt ein Polygon stippingmuster mit einem 32x32-Polygon durch den *Mask* -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="37c44-119">The **glGetPolygonStipple** function returns a 32x32 polygon stipple pattern through the *mask* parameter.</span></span> <span data-ttu-id="37c44-120">Das Muster wird in den Arbeitsspeicher verpackt, als ob [**glread Pixels**](glreadpixels.md) sowohl mit der *Höhe* als auch mit der *Breite* 32, dem *Typ* der GL \_ -Bitmap und dem *Format* des GL \_ \_ -Farbindexes aufgerufen und das stippingmuster in einem internen 32 x 32-Farb Index Puffer gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="37c44-120">The pattern is packed into memory as if [**glReadPixels**](glreadpixels.md) with both *height* and *width* of 32, *type* of GL\_BITMAP, and *format* of GL\_COLOR\_INDEX were called, and the stipple pattern were stored in an internal 32x32 color-index buffer.</span></span> <span data-ttu-id="37c44-121">Im Gegensatz zu **gllepixels** werden Pixel Übertragungs Vorgänge (Shift, Offset und Pixel Map) jedoch nicht auf das zurückgegebene Stippel Bild angewendet.</span><span class="sxs-lookup"><span data-stu-id="37c44-121">Unlike **glReadPixels**, however, pixel-transfer operations (shift, offset, and pixel map) are not applied to the returned stipple image.</span></span>

<span data-ttu-id="37c44-122">Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt der *Maske* vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="37c44-122">If an error is generated, no change is made to the contents of *mask*.</span></span>

## <a name="requirements"></a><span data-ttu-id="37c44-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37c44-123">Requirements</span></span>



| <span data-ttu-id="37c44-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37c44-124">Requirement</span></span> | <span data-ttu-id="37c44-125">Wert</span><span class="sxs-lookup"><span data-stu-id="37c44-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37c44-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37c44-126">Minimum supported client</span></span><br/> | <span data-ttu-id="37c44-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37c44-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="37c44-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37c44-128">Minimum supported server</span></span><br/> | <span data-ttu-id="37c44-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37c44-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="37c44-130">Header</span><span class="sxs-lookup"><span data-stu-id="37c44-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="37c44-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="37c44-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="37c44-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="37c44-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="37c44-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37c44-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="37c44-134">DLL</span><span class="sxs-lookup"><span data-stu-id="37c44-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37c44-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37c44-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37c44-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37c44-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37c44-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="37c44-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="37c44-138">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="37c44-138">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="37c44-139">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="37c44-139">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="37c44-140">**glpixeltransfer**</span><span class="sxs-lookup"><span data-stu-id="37c44-140">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="37c44-141">**glpolygonstippel**</span><span class="sxs-lookup"><span data-stu-id="37c44-141">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="37c44-142">**glread Pixels**</span><span class="sxs-lookup"><span data-stu-id="37c44-142">**glReadPixels**</span></span>](glreadpixels.md)
</dt> </dl>

 

 





