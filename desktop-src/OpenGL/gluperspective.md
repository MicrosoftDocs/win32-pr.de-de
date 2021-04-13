---
title: gluperspective-Funktion (glu. h)
description: Die Funktion "gluperspective" richtet eine perspektivische Projektions Matrix ein.
ms.assetid: 125e2828-a2d7-4c6c-9370-eb21a581ced8
keywords:
- gluperspective-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluPerspective
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf30fc7dc4c6ba5a56efd3def6a5a7178f81ed49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392109"
---
# <a name="gluperspective-function"></a><span data-ttu-id="7bb75-104">gluperspective-Funktion</span><span class="sxs-lookup"><span data-stu-id="7bb75-104">gluPerspective function</span></span>

<span data-ttu-id="7bb75-105">Die Funktion " **gluperspective** " richtet eine perspektivische Projektions Matrix ein.</span><span class="sxs-lookup"><span data-stu-id="7bb75-105">The **gluPerspective** function sets up a perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bb75-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bb75-106">Syntax</span></span>


```C++
void WINAPI gluPerspective(
   GLdouble fovy,
   GLdouble aspect,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="7bb75-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bb75-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bb75-108">*fovy*</span><span class="sxs-lookup"><span data-stu-id="7bb75-108">*fovy*</span></span> 
</dt> <dd>

<span data-ttu-id="7bb75-109">Das Feld des Ansichts Winkels in Grad in y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="7bb75-109">The field of view angle, in degrees, in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="7bb75-110">*aspect*</span><span class="sxs-lookup"><span data-stu-id="7bb75-110">*aspect*</span></span> 
</dt> <dd>

<span data-ttu-id="7bb75-111">Das Seitenverhältnis, das das Feld der Sicht in der x-Richtung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="7bb75-111">The aspect ratio that determines the field of view in the x-direction.</span></span> <span data-ttu-id="7bb75-112">Das Seitenverhältnis ist das Verhältnis von *x* (Width) zu *y* (Height).</span><span class="sxs-lookup"><span data-stu-id="7bb75-112">The aspect ratio is the ratio of *x* (width) to *y* (height).</span></span>

</dd> <dt>

<span data-ttu-id="7bb75-113">*znear*</span><span class="sxs-lookup"><span data-stu-id="7bb75-113">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="7bb75-114">Der Abstand zwischen dem Viewer und der Near Clipping-Ebene (immer positiv).</span><span class="sxs-lookup"><span data-stu-id="7bb75-114">The distance from the viewer to the near clipping plane (always positive).</span></span>

</dd> <dt>

<span data-ttu-id="7bb75-115">*zfar*</span><span class="sxs-lookup"><span data-stu-id="7bb75-115">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="7bb75-116">Der Abstand zwischen dem Viewer und der weit entfernten Clippingebene (immer positiv).</span><span class="sxs-lookup"><span data-stu-id="7bb75-116">The distance from the viewer to the far clipping plane (always positive).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bb75-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7bb75-117">Return value</span></span>

<span data-ttu-id="7bb75-118">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7bb75-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bb75-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bb75-119">Remarks</span></span>

<span data-ttu-id="7bb75-120">Die Funktion " **gluperspective** " gibt eine Anzeige von "Frustum" im Weltkoordinaten System an.</span><span class="sxs-lookup"><span data-stu-id="7bb75-120">The **gluPerspective** function specifies a viewing frustum into the world coordinate system.</span></span> <span data-ttu-id="7bb75-121">Im Allgemeinen sollte das Seitenverhältnis in " **gluperspective** " dem Seitenverhältnis des zugeordneten Viewports entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7bb75-121">In general, the aspect ratio in **gluPerspective** should match the aspect ratio of the associated viewport.</span></span> <span data-ttu-id="7bb75-122">*Aspekt* = 2,0 bedeutet beispielsweise, dass der Anzeige Winkel des Viewers *doppelt so breit wie in* *y* ist.</span><span class="sxs-lookup"><span data-stu-id="7bb75-122">For example, *aspect* = 2.0 means the viewer's angle of view is twice as wide in *x* as it is in *y*.</span></span> <span data-ttu-id="7bb75-123">Wenn der Viewport doppelt so breit ist, wie er hoch ist, wird das Bild ohne Verzerrung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7bb75-123">If the viewport is twice as wide as it is tall, it displays the image without distortion.</span></span>

<span data-ttu-id="7bb75-124">Die von " **gluperspective** " generierte Matrix wird mit der aktuellen Matrix multipliziert, so als ob " [**glmultmatrix**](glmultmatrix.md) " mit der generierten Matrix aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7bb75-124">The matrix generated by **gluPerspective** is multiplied by the current matrix, just as if [**glMultMatrix**](glmultmatrix.md) were called with the generated matrix.</span></span> <span data-ttu-id="7bb75-125">Wenn Sie stattdessen die Perspektiven Matrix auf den aktuellen Matrix Stapel laden möchten, stellen Sie dem aufzurufenden **gluperspective** -Befehl den Befehl " [**glLoadIdentity**](glloadidentity.md)" voran.</span><span class="sxs-lookup"><span data-stu-id="7bb75-125">To load the perspective matrix onto the current matrix stack instead, precede the call to **gluPerspective** with a call to [**glLoadIdentity**](glloadidentity.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7bb75-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bb75-126">Requirements</span></span>



| <span data-ttu-id="7bb75-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7bb75-127">Requirement</span></span> | <span data-ttu-id="7bb75-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7bb75-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb75-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7bb75-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7bb75-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7bb75-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7bb75-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7bb75-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7bb75-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7bb75-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7bb75-133">Header</span><span class="sxs-lookup"><span data-stu-id="7bb75-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bb75-134"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bb75-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="7bb75-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7bb75-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="7bb75-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7bb75-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7bb75-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7bb75-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bb75-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bb75-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bb75-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bb75-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bb75-140">**glfrustum**</span><span class="sxs-lookup"><span data-stu-id="7bb75-140">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="7bb75-141">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="7bb75-141">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="7bb75-142">**glmultmatrix**</span><span class="sxs-lookup"><span data-stu-id="7bb75-142">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="7bb75-143">**gluOrtho2D**</span><span class="sxs-lookup"><span data-stu-id="7bb75-143">**gluOrtho2D**</span></span>](gluortho2d.md)
</dt> </dl>

 

 





