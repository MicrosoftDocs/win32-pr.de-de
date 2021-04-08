---
title: gluquadricdrawstyle-Funktion (glu. h)
description: Die Funktion "gluquadricdrawstyle" gibt die gewünschte Zeichnungs Art für viercs an.
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- gluquadricdrawstyle-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluQuadricDrawStyle
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a1b44b7894ea9762b450c5a5d6c2b022c5e02f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956849"
---
# <a name="gluquadricdrawstyle-function"></a><span data-ttu-id="f6804-104">gluquadricdrawstyle-Funktion</span><span class="sxs-lookup"><span data-stu-id="f6804-104">gluQuadricDrawStyle function</span></span>

<span data-ttu-id="f6804-105">Die Funktion " **gluquadricdrawstyle** " gibt die gewünschte Zeichnungs Art für viercs an.</span><span class="sxs-lookup"><span data-stu-id="f6804-105">The **gluQuadricDrawStyle** function specifies the draw style desired for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6804-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6804-106">Syntax</span></span>


```C++
void WINAPI gluQuadricDrawStyle(
   GLUquadric *quadObject,
   GLenum     drawStyle
);
```



## <a name="parameters"></a><span data-ttu-id="f6804-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6804-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6804-108">*quadobject*</span><span class="sxs-lookup"><span data-stu-id="f6804-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="f6804-109">Das Quadric-Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="f6804-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="f6804-110">*DrawStyle*</span><span class="sxs-lookup"><span data-stu-id="f6804-110">*drawStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="f6804-111">Der gewünschte Zeichnungs Stil.</span><span class="sxs-lookup"><span data-stu-id="f6804-111">The desired draw style.</span></span> <span data-ttu-id="f6804-112">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="f6804-112">The following values are valid.</span></span>



| <span data-ttu-id="f6804-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f6804-113">Value</span></span>                                                                                                                                                            | <span data-ttu-id="f6804-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f6804-114">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <span data-ttu-id="f6804-115"><dt>**Glu \_ ausfüllen**</dt></span><span class="sxs-lookup"><span data-stu-id="f6804-115"><dt>**GLU\_FILL**</dt></span></span> </dl>                   | <span data-ttu-id="f6804-116">Viercs werden mit Polygon primitiven gerendert.</span><span class="sxs-lookup"><span data-stu-id="f6804-116">Quadrics are rendered with polygon primitives.</span></span> <span data-ttu-id="f6804-117">Die Polygone werden gegen den Uhrzeigersinn in Bezug auf ihre normale (wie mit " [**gluquadricorientation**](gluquadricorientation.md)" definiert) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f6804-117">The polygons are drawn in a counterclockwise fashion with respect to their normals (as defined with [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span><br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <span data-ttu-id="f6804-118"><dt>**Glu- \_ Linie**</dt></span><span class="sxs-lookup"><span data-stu-id="f6804-118"><dt>**GLU\_LINE**</dt></span></span> </dl>                   | <span data-ttu-id="f6804-119">Viercs werden als Zeilen Satz gerendert.</span><span class="sxs-lookup"><span data-stu-id="f6804-119">Quadrics are rendered as a set of lines.</span></span><br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <span data-ttu-id="f6804-120"><dt>**Glu- \_ Silhouette**</dt></span><span class="sxs-lookup"><span data-stu-id="f6804-120"><dt>**GLU\_SILHOUETTE**</dt></span></span> </dl> | <span data-ttu-id="f6804-121">Viercs werden als Zeilen Satz gerendert, mit dem Unterschied, dass Kanten, die Coplanar trennen, nicht gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="f6804-121">Quadrics are rendered as a set of lines, except that edges separating coplanar faces will not be drawn.</span></span><br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <span data-ttu-id="f6804-122"><dt>**Glu- \_ Punkt**</dt></span><span class="sxs-lookup"><span data-stu-id="f6804-122"><dt>**GLU\_POINT**</dt></span></span> </dl>                | <span data-ttu-id="f6804-123">Viercs werden als eine Gruppe von Punkten gerendert.</span><span class="sxs-lookup"><span data-stu-id="f6804-123">Quadrics are rendered as a set of points.</span></span><br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6804-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6804-124">Return value</span></span>

<span data-ttu-id="f6804-125">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f6804-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6804-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6804-126">Remarks</span></span>

<span data-ttu-id="f6804-127">Die Funktion " **gluquadricdrawstyle** " gibt den Zeichnungs Stil für viercs an, die mit **quadobject** gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="f6804-127">The **gluQuadricDrawStyle** function specifies the draw style for quadrics rendered with **quadObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6804-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6804-128">Requirements</span></span>



| <span data-ttu-id="f6804-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6804-129">Requirement</span></span> | <span data-ttu-id="f6804-130">Wert</span><span class="sxs-lookup"><span data-stu-id="f6804-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f6804-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6804-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f6804-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6804-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f6804-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6804-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f6804-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6804-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f6804-135">Header</span><span class="sxs-lookup"><span data-stu-id="f6804-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6804-136"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6804-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f6804-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f6804-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="f6804-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6804-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f6804-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f6804-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6804-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6804-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6804-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6804-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6804-142">**glunewquadric**</span><span class="sxs-lookup"><span data-stu-id="f6804-142">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="f6804-143">**gluquadricnormals**</span><span class="sxs-lookup"><span data-stu-id="f6804-143">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="f6804-144">**gluquadricorientation**</span><span class="sxs-lookup"><span data-stu-id="f6804-144">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="f6804-145">**gluquadrictexture**</span><span class="sxs-lookup"><span data-stu-id="f6804-145">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





