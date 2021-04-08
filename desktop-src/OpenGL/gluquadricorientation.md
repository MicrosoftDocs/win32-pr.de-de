---
title: gluquadricorientation-Funktion (glu. h)
description: Die Funktion "gluquadricorientation" gibt die Ausrichtung innerhalb oder außerhalb von viercs an.
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- gluquadricorientation-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluQuadricOrientation
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05ffb1eeff199297943e678783731a26a38092a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739792"
---
# <a name="gluquadricorientation-function"></a><span data-ttu-id="07996-104">gluquadricorientation-Funktion</span><span class="sxs-lookup"><span data-stu-id="07996-104">gluQuadricOrientation function</span></span>

<span data-ttu-id="07996-105">Die Funktion " **gluquadricorientation** " gibt die Ausrichtung innerhalb oder außerhalb von viercs an.</span><span class="sxs-lookup"><span data-stu-id="07996-105">The **gluQuadricOrientation** function specifies inside or outside orientation for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="07996-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="07996-106">Syntax</span></span>


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a><span data-ttu-id="07996-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="07996-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07996-108">*quadobject*</span><span class="sxs-lookup"><span data-stu-id="07996-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="07996-109">Das Quadric-Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="07996-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="07996-110">*orientation*</span><span class="sxs-lookup"><span data-stu-id="07996-110">*orientation*</span></span> 
</dt> <dd>

<span data-ttu-id="07996-111">Die gewünschte Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="07996-111">The desired orientation.</span></span> <span data-ttu-id="07996-112">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="07996-112">The following values are valid.</span></span>



| <span data-ttu-id="07996-113">Wert</span><span class="sxs-lookup"><span data-stu-id="07996-113">Value</span></span>                                                                                                                                                   | <span data-ttu-id="07996-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="07996-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <span data-ttu-id="07996-115"><dt>**Glu \_ außerhalb**</dt></span><span class="sxs-lookup"><span data-stu-id="07996-115"><dt>**GLU\_OUTSIDE**</dt></span></span> </dl> | <span data-ttu-id="07996-116">Zeichnen von viercs mit normalen, die nach außen zeigen.</span><span class="sxs-lookup"><span data-stu-id="07996-116">Draw quadrics with normals pointing outward.</span></span> <span data-ttu-id="07996-117">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="07996-117">This is the default value.</span></span><br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <span data-ttu-id="07996-118"><dt>**Glu \_ in**</dt></span><span class="sxs-lookup"><span data-stu-id="07996-118"><dt>**GLU\_INSIDE**</dt></span></span> </dl>    | <span data-ttu-id="07996-119">Zeichnen von viercs mit normalen, die nach innen zeigen.</span><span class="sxs-lookup"><span data-stu-id="07996-119">Draw quadrics with normals pointing inward.</span></span><br/>                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07996-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07996-120">Return value</span></span>

<span data-ttu-id="07996-121">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="07996-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07996-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07996-122">Remarks</span></span>

<span data-ttu-id="07996-123">Die Funktion " **gluquadricorientation** " gibt an, welche Art von Ausrichtung für mit **quadobject** gerenderten viercs gewünscht ist.</span><span class="sxs-lookup"><span data-stu-id="07996-123">The **gluQuadricOrientation** function specifies what kind of orientation is desired for quadrics rendered with **quadObject**.</span></span> <span data-ttu-id="07996-124">Die Interpretation von außen und innen hängt von der Quadric ab, die gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="07996-124">The interpretation of outward and inward depends on the quadric being drawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="07996-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07996-125">Requirements</span></span>



| <span data-ttu-id="07996-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07996-126">Requirement</span></span> | <span data-ttu-id="07996-127">Wert</span><span class="sxs-lookup"><span data-stu-id="07996-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="07996-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07996-128">Minimum supported client</span></span><br/> | <span data-ttu-id="07996-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07996-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="07996-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07996-130">Minimum supported server</span></span><br/> | <span data-ttu-id="07996-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07996-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="07996-132">Header</span><span class="sxs-lookup"><span data-stu-id="07996-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="07996-133"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="07996-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="07996-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="07996-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="07996-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07996-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="07996-136">DLL</span><span class="sxs-lookup"><span data-stu-id="07996-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07996-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07996-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07996-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07996-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07996-139">**glunewquadric**</span><span class="sxs-lookup"><span data-stu-id="07996-139">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="07996-140">**gluquadricdrawstyle**</span><span class="sxs-lookup"><span data-stu-id="07996-140">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="07996-141">**gluquadricnormals**</span><span class="sxs-lookup"><span data-stu-id="07996-141">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="07996-142">**gluquadrictexture**</span><span class="sxs-lookup"><span data-stu-id="07996-142">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





