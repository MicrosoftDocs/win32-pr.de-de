---
title: gluzylinder-Funktion (glu. h)
description: Die Funktion "gluzylinder" zeichnet einen Zylinder.
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- gluzylinder-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluCylinder
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fd201d1ddd720501715d1ead08d94bab72f7b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345305"
---
# <a name="glucylinder-function"></a><span data-ttu-id="5b7d7-104">gluzylinder-Funktion</span><span class="sxs-lookup"><span data-stu-id="5b7d7-104">gluCylinder function</span></span>

<span data-ttu-id="5b7d7-105">Die Funktion " **gluzylinder** " zeichnet einen Zylinder.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-105">The **gluCylinder** function draws a cylinder.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b7d7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b7d7-106">Syntax</span></span>


```C++
void WINAPI gluCylinder(
   GLUquadric *qobj,
   GLdouble   baseRadius,
   GLdouble   topRadius,
   GLdouble   height,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a><span data-ttu-id="5b7d7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b7d7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b7d7-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="5b7d7-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="5b7d7-109">Das Quadric-Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="5b7d7-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="5b7d7-110">*baseradius*</span><span class="sxs-lookup"><span data-stu-id="5b7d7-110">*baseRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="5b7d7-111">Der Radius des Zylinders bei *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-111">The radius of the cylinder at *z* = 0.</span></span>

</dd> <dt>

<span data-ttu-id="5b7d7-112">*topradius*</span><span class="sxs-lookup"><span data-stu-id="5b7d7-112">*topRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="5b7d7-113">Der Radius des Zylinders an der *z*-  =  *Höhe*.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-113">The radius of the cylinder at *z* = *height*.</span></span>

</dd> <dt>

<span data-ttu-id="5b7d7-114">*height*</span><span class="sxs-lookup"><span data-stu-id="5b7d7-114">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="5b7d7-115">Die Höhe des Zylinders.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-115">The height of the cylinder.</span></span>

</dd> <dt>

<span data-ttu-id="5b7d7-116">*aufs*</span><span class="sxs-lookup"><span data-stu-id="5b7d7-116">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="5b7d7-117">Die Anzahl der Unterteilungen um die z-Achse.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-117">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="5b7d7-118">*Stöcke*</span><span class="sxs-lookup"><span data-stu-id="5b7d7-118">*stacks*</span></span> 
</dt> <dd>

<span data-ttu-id="5b7d7-119">Die Anzahl der Unterteilungen entlang der z-Achse.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-119">The number of subdivisions along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b7d7-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b7d7-120">Return value</span></span>

<span data-ttu-id="5b7d7-121">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b7d7-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b7d7-122">Remarks</span></span>

<span data-ttu-id="5b7d7-123">Die Funktion " **gluzylinder** " zeichnet einen Zylinder, der entlang der z-Achse ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-123">The **gluCylinder** function draws a cylinder oriented along the z-axis.</span></span> <span data-ttu-id="5b7d7-124">Die Basis des Zylinders wird bei *z* = 0 und am oberen Rand bei der *z*-  =  *Höhe* platziert.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-124">The base of the cylinder is placed at *z* = 0, and the top at *z* = *height*.</span></span> <span data-ttu-id="5b7d7-125">Wie bei einer Kugel wird ein Zylinder um die z-Achse in Slices und entlang der z-Achse in Stapel aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-125">Like a sphere, a cylinder is subdivided around the z-axis into slices, and along the z-axis into stacks.</span></span>

<span data-ttu-id="5b7d7-126">Beachten Sie, dass diese Routine einen Kegel generiert, wenn *topradius* auf 0 (null) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-126">Note that if *topRadius* is set to zero, then this routine will generate a cone.</span></span>

<span data-ttu-id="5b7d7-127">Wenn die Ausrichtung auf "glu \_ outside" (mit " [**gluquadricorientation**](gluquadricorientation.md)") festgelegt ist, zeigen alle generierten normale von der z-Achse Weg.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-127">If the orientation is set to GLU\_OUTSIDE (with [**gluQuadricOrientation**](gluquadricorientation.md)), then any generated normals point away from the z-axis.</span></span> <span data-ttu-id="5b7d7-128">Andernfalls zeigen Sie auf die z-Achse.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-128">Otherwise, they point toward the z-axis.</span></span>

<span data-ttu-id="5b7d7-129">Wenn die Texturierung aktiviert ist (mit " [**gluquadrictexture**](gluquadrictexture.md)"): Es werden Texturkoordinaten generiert, sodass *t* von 0,0 bei *z* = 0 auf 1,0 bei *z*  =  *height* und *s* zwischen 0,0 an der positiven y-Achse, bis 0,25 an der positiven x-Achse, zu 0,5 auf der negativen y-Achse, zu 0,75 auf der negativen x-Achse und zurück zu 1,0 auf der positiven y-Achse reicht.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-129">If texturing is turned on (with [**gluQuadricTexture**](gluquadrictexture.md)): texture coordinates are generated so that *t* ranges linearly from 0.0 at *z* = 0 to 1.0 at *z* = *height*; and *s* ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b7d7-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b7d7-130">Requirements</span></span>



| <span data-ttu-id="5b7d7-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b7d7-131">Requirement</span></span> | <span data-ttu-id="5b7d7-132">Wert</span><span class="sxs-lookup"><span data-stu-id="5b7d7-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5b7d7-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b7d7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5b7d7-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b7d7-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5b7d7-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b7d7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5b7d7-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b7d7-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5b7d7-137">Header</span><span class="sxs-lookup"><span data-stu-id="5b7d7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b7d7-138"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b7d7-138"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="5b7d7-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5b7d7-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="5b7d7-140"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b7d7-140"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5b7d7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5b7d7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b7d7-142"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b7d7-142"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b7d7-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b7d7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b7d7-144">**gludisk**</span><span class="sxs-lookup"><span data-stu-id="5b7d7-144">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="5b7d7-145">**glunewquadric**</span><span class="sxs-lookup"><span data-stu-id="5b7d7-145">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="5b7d7-146">**glupartialdisk**</span><span class="sxs-lookup"><span data-stu-id="5b7d7-146">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="5b7d7-147">**gluquadricorientation**</span><span class="sxs-lookup"><span data-stu-id="5b7d7-147">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="5b7d7-148">**gluquadrictexture**</span><span class="sxs-lookup"><span data-stu-id="5b7d7-148">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="5b7d7-149">**glusphere**</span><span class="sxs-lookup"><span data-stu-id="5b7d7-149">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





