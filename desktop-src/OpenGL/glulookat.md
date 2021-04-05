---
title: glulookat-Funktion (glu. h)
description: Die Funktion "glulookat" definiert eine Anzeige Transformation.
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- glulookat-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluLookAt
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5866f3c06ef6969c95eeef4b23fff7a4e7852eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859301"
---
# <a name="glulookat-function"></a><span data-ttu-id="c9c43-104">glulookat-Funktion</span><span class="sxs-lookup"><span data-stu-id="c9c43-104">gluLookAt function</span></span>

<span data-ttu-id="c9c43-105">Die Funktion " **glulookat** " definiert eine Anzeige Transformation.</span><span class="sxs-lookup"><span data-stu-id="c9c43-105">The **gluLookAt** function defines a viewing transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9c43-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9c43-106">Syntax</span></span>


```C++
void WINAPI gluLookAt(
   GLdouble eyex,
   GLdouble eyey,
   GLdouble eyez,
   GLdouble centerx,
   GLdouble centery,
   GLdouble centerz,
   GLdouble upx,
   GLdouble upy,
   GLdouble upz
);
```



## <a name="parameters"></a><span data-ttu-id="c9c43-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9c43-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9c43-108">*eyex*</span><span class="sxs-lookup"><span data-stu-id="c9c43-108">*eyex*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c43-109">Die Position des Augen Punkts.</span><span class="sxs-lookup"><span data-stu-id="c9c43-109">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="c9c43-110">*pipey*</span><span class="sxs-lookup"><span data-stu-id="c9c43-110">*eyey*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c43-111">Die Position des Augen Punkts.</span><span class="sxs-lookup"><span data-stu-id="c9c43-111">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="c9c43-112">*pipez*</span><span class="sxs-lookup"><span data-stu-id="c9c43-112">*eyez*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c43-113">Die Position des Augen Punkts.</span><span class="sxs-lookup"><span data-stu-id="c9c43-113">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="c9c43-114">*CenterX*</span><span class="sxs-lookup"><span data-stu-id="c9c43-114">*centerx*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c43-115">Die Position des Bezugspunkts.</span><span class="sxs-lookup"><span data-stu-id="c9c43-115">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="c9c43-116">*CenterY*</span><span class="sxs-lookup"><span data-stu-id="c9c43-116">*centery*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c43-117">Die Position des Bezugspunkts.</span><span class="sxs-lookup"><span data-stu-id="c9c43-117">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="c9c43-118">*CenterZ*</span><span class="sxs-lookup"><span data-stu-id="c9c43-118">*centerz*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c43-119">Die Position des Bezugspunkts.</span><span class="sxs-lookup"><span data-stu-id="c9c43-119">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="c9c43-120">*UPX*</span><span class="sxs-lookup"><span data-stu-id="c9c43-120">*upx*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c43-121">Die Richtung des aufwärts Vektors.</span><span class="sxs-lookup"><span data-stu-id="c9c43-121">The direction of the up vector.</span></span>

</dd> <dt>

<span data-ttu-id="c9c43-122">*UPY*</span><span class="sxs-lookup"><span data-stu-id="c9c43-122">*upy*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c43-123">Die Richtung des aufwärts Vektors.</span><span class="sxs-lookup"><span data-stu-id="c9c43-123">The direction of the up vector.</span></span>

</dd> <dt>

<span data-ttu-id="c9c43-124">*UPZ*</span><span class="sxs-lookup"><span data-stu-id="c9c43-124">*upz*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c43-125">Die Richtung des aufwärts Vektors.</span><span class="sxs-lookup"><span data-stu-id="c9c43-125">The direction of the up vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9c43-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9c43-126">Return value</span></span>

<span data-ttu-id="c9c43-127">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c9c43-127">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9c43-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9c43-128">Remarks</span></span>

<span data-ttu-id="c9c43-129">Die Funktion " **glulookat** " erstellt eine von einem Augen Punkt abgeleitete Anzeige Matrix, einen Bezugspunkt, der den Mittelpunkt der Szene angibt, und einen aufwärts Vektor.</span><span class="sxs-lookup"><span data-stu-id="c9c43-129">The **gluLookAt** function creates a viewing matrix derived from an eye point, a reference point indicating the center of the scene, and an up vector.</span></span> <span data-ttu-id="c9c43-130">Die Matrix ordnet den Verweis Punkt der negativen z-Achse und dem Augenblick auf den Ursprung zu. Wenn Sie also eine typische Projektions Matrix verwenden, wird der Mittelpunkt der Szene der Mitte des Viewports zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c9c43-130">The matrix maps the reference point to the negative z-axis and the eye point to the origin, so that when you use a typical projection matrix, the center of the scene maps to the center of the viewport.</span></span> <span data-ttu-id="c9c43-131">Entsprechend wird die Richtung, die durch den auf die Anzeige Ebene projizierten aufwärts Vektor beschrieben wird, der positiven y-Achse zugeordnet, sodass Sie im Viewport nach oben zeigt.</span><span class="sxs-lookup"><span data-stu-id="c9c43-131">Similarly, the direction described by the up vector projected onto the viewing plane is mapped to the positive y-axis so that it points upward in the viewport.</span></span> <span data-ttu-id="c9c43-132">Der Up-Vektor darf nicht parallel zum Bezugspunkt für die Sichtlinie gleich sein.</span><span class="sxs-lookup"><span data-stu-id="c9c43-132">The up vector must not be parallel to the line of sight from the eye to the reference point.</span></span>

<span data-ttu-id="c9c43-133">Die von " **glulookat** " generierte Matrix stellt die aktuelle Matrix dar.</span><span class="sxs-lookup"><span data-stu-id="c9c43-133">The matrix generated by **gluLookAt** postmultiplies the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9c43-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9c43-134">Requirements</span></span>



| <span data-ttu-id="c9c43-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9c43-135">Requirement</span></span> | <span data-ttu-id="c9c43-136">Wert</span><span class="sxs-lookup"><span data-stu-id="c9c43-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c43-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9c43-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c9c43-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9c43-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c9c43-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9c43-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c9c43-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9c43-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c9c43-141">Header</span><span class="sxs-lookup"><span data-stu-id="c9c43-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9c43-142"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9c43-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="c9c43-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c9c43-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="c9c43-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9c43-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c9c43-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c9c43-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9c43-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9c43-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9c43-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9c43-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9c43-148">**glfrustum**</span><span class="sxs-lookup"><span data-stu-id="c9c43-148">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="c9c43-149">**gluperspective**</span><span class="sxs-lookup"><span data-stu-id="c9c43-149">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





