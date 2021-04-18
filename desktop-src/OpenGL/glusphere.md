---
title: glusphere-Funktion (glu. h)
description: Die Funktion "glusphere" zeichnet eine Kugel.
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- glusphere-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluSphere
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899ff4833c705aae34fdb7830c264fee91414116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478015"
---
# <a name="glusphere-function"></a><span data-ttu-id="a3c79-104">glusphere-Funktion</span><span class="sxs-lookup"><span data-stu-id="a3c79-104">gluSphere function</span></span>

<span data-ttu-id="a3c79-105">Die Funktion " **glusphere** " zeichnet eine Kugel.</span><span class="sxs-lookup"><span data-stu-id="a3c79-105">The **gluSphere** function draws a sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3c79-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3c79-106">Syntax</span></span>


```C++
void WINAPI gluSphere(
   GLUquadric *qobj,
   GLdouble   radius,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a><span data-ttu-id="a3c79-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3c79-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3c79-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="a3c79-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="a3c79-109">Das Quadric-Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="a3c79-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a3c79-110">*Kreises*</span><span class="sxs-lookup"><span data-stu-id="a3c79-110">*radius*</span></span> 
</dt> <dd>

<span data-ttu-id="a3c79-111">Der Radius der Kugel.</span><span class="sxs-lookup"><span data-stu-id="a3c79-111">The radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="a3c79-112">*aufs*</span><span class="sxs-lookup"><span data-stu-id="a3c79-112">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="a3c79-113">Die Anzahl der Unterteilungen um die z-Achse (ähnlich wie Längengrad).</span><span class="sxs-lookup"><span data-stu-id="a3c79-113">The number of subdivisions around the z-axis (similar to lines of longitude).</span></span>

</dd> <dt>

<span data-ttu-id="a3c79-114">*Stöcke*</span><span class="sxs-lookup"><span data-stu-id="a3c79-114">*stacks*</span></span> 
</dt> <dd>

<span data-ttu-id="a3c79-115">Die Anzahl der untergeordneten Bereiche entlang der z-Achse (ähnlich wie bei breiten Linien).</span><span class="sxs-lookup"><span data-stu-id="a3c79-115">The number of subdivisions along the z-axis (similar to lines of latitude).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3c79-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3c79-116">Return value</span></span>

<span data-ttu-id="a3c79-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a3c79-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3c79-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3c79-118">Remarks</span></span>

<span data-ttu-id="a3c79-119">Die **glusphere** -Funktion zeichnet eine Kugel des angegebenen Radius, zentriert um den Ursprung.</span><span class="sxs-lookup"><span data-stu-id="a3c79-119">The **gluSphere** function draws a sphere of the given radius centered around the origin.</span></span> <span data-ttu-id="a3c79-120">Die Kugel wird um die z-Achse in Slices und entlang der z-Achse in Stapel aufgeteilt (ähnlich wie Längen-und Breitengrad).</span><span class="sxs-lookup"><span data-stu-id="a3c79-120">The sphere is subdivided around the z-axis into slices and along the z-axis into stacks (similar to lines of longitude and latitude).</span></span>

<span data-ttu-id="a3c79-121">Wenn die Ausrichtung auf "glu \_ outside" (mit " **gluquadricorientation**") festgelegt ist, werden alle normalisierten Punkte vom Mittelpunkt der Kugel entfernt.</span><span class="sxs-lookup"><span data-stu-id="a3c79-121">If the orientation is set to GLU\_OUTSIDE (with **gluQuadricOrientation**), any normals generated point away from the center of the sphere.</span></span> <span data-ttu-id="a3c79-122">Andernfalls zeigen Sie auf den Mittelpunkt der Kugel.</span><span class="sxs-lookup"><span data-stu-id="a3c79-122">Otherwise, they point toward the center of the sphere.</span></span>

<span data-ttu-id="a3c79-123">Wenn die Texturierung aktiviert ist (mit " **gluquadrictexture**"), werden Texturkoordinaten generiert, sodass *t* von 0,0 bei *z* =-*RADIUS* bis 1,0 am *z*-  =  *RADIUS* reicht (*t* vergrößert sich linear entlang der Längenlinien); und *s* liegen zwischen 0,0 und der positiven y-Achse, bis 0,25 auf der positiven x-Achse, bis 0,5 auf der negativen y-Achse, bis 0,75 auf der negativen x-Achse und zurück zu 1,0 auf der positiven y-Achse.</span><span class="sxs-lookup"><span data-stu-id="a3c79-123">If texturing is turned on (with **gluQuadricTexture**): texture coordinates are generated so that *t* ranges from 0.0 at *z* = -*radius* to 1.0 at *z* = *radius* (*t* increases linearly along longitudinal lines); and *s* ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3c79-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3c79-124">Requirements</span></span>



| <span data-ttu-id="a3c79-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3c79-125">Requirement</span></span> | <span data-ttu-id="a3c79-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a3c79-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c79-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3c79-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a3c79-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3c79-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a3c79-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3c79-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a3c79-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3c79-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a3c79-131">Header</span><span class="sxs-lookup"><span data-stu-id="a3c79-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3c79-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3c79-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="a3c79-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a3c79-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3c79-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3c79-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a3c79-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a3c79-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3c79-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3c79-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3c79-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3c79-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3c79-138">**gluzylinder**</span><span class="sxs-lookup"><span data-stu-id="a3c79-138">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="a3c79-139">**gludisk**</span><span class="sxs-lookup"><span data-stu-id="a3c79-139">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="a3c79-140">**glunewquadric**</span><span class="sxs-lookup"><span data-stu-id="a3c79-140">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="a3c79-141">**glupartialdisk**</span><span class="sxs-lookup"><span data-stu-id="a3c79-141">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="a3c79-142">**gluquadricorientation**</span><span class="sxs-lookup"><span data-stu-id="a3c79-142">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="a3c79-143">**gluquadrictexture**</span><span class="sxs-lookup"><span data-stu-id="a3c79-143">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





