---
title: gluquadricnormals-Funktion (glu. h)
description: Die Funktion "gluquadricnormals" gibt an, welche Art von normalen für viercs verwendet werden soll.
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
keywords:
- gluquadricnormals-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluQuadricNormals
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11f9d8cd1884d7a5d1bc4cd03797517ba484126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478018"
---
# <a name="gluquadricnormals-function"></a><span data-ttu-id="0ee7d-104">gluquadricnormals-Funktion</span><span class="sxs-lookup"><span data-stu-id="0ee7d-104">gluQuadricNormals function</span></span>

<span data-ttu-id="0ee7d-105">Die Funktion " **gluquadricnormals** " gibt an, welche Art von normalen für viercs verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ee7d-105">The **gluQuadricNormals** function specifies what kind of normals are to be used for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee7d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ee7d-106">Syntax</span></span>


```C++
void WINAPI gluQuadricNormals(
   GLUquadric *quadObject,
   GLenum     normals
);
```



## <a name="parameters"></a><span data-ttu-id="0ee7d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ee7d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ee7d-108">*quadobject*</span><span class="sxs-lookup"><span data-stu-id="0ee7d-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="0ee7d-109">Das Quadric-Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="0ee7d-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0ee7d-110">*normale*</span><span class="sxs-lookup"><span data-stu-id="0ee7d-110">*normals*</span></span> 
</dt> <dd>

<span data-ttu-id="0ee7d-111">Der gewünschte Typ von normalen.</span><span class="sxs-lookup"><span data-stu-id="0ee7d-111">The desired type of normals.</span></span> <span data-ttu-id="0ee7d-112">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="0ee7d-112">The following values are valid.</span></span>



| <span data-ttu-id="0ee7d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0ee7d-113">Value</span></span>                                                                                                                                                | <span data-ttu-id="0ee7d-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0ee7d-114">Meaning</span></span>                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="GLU_NONE"></span><span id="glu_none"></span><dl> <span data-ttu-id="0ee7d-115"><dt>**Glu \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="0ee7d-115"><dt>**GLU\_NONE**</dt></span></span> </dl>       | <span data-ttu-id="0ee7d-116">Es werden keine normale generiert.</span><span class="sxs-lookup"><span data-stu-id="0ee7d-116">No normals are generated.</span></span><br/>                                                         |
| <span id="GLU_FLAT"></span><span id="glu_flat"></span><dl> <span data-ttu-id="0ee7d-117"><dt>**Glu \_ flach**</dt></span><span class="sxs-lookup"><span data-stu-id="0ee7d-117"><dt>**GLU\_FLAT**</dt></span></span> </dl>       | <span data-ttu-id="0ee7d-118">Eine normale wird für jedes Facetten eines quadkts generiert.</span><span class="sxs-lookup"><span data-stu-id="0ee7d-118">One normal is generated for every facet of a quadric.</span></span><br/>                             |
| <span id="GLU_SMOOTH"></span><span id="glu_smooth"></span><dl> <span data-ttu-id="0ee7d-119"><dt>**Glu \_ glatt**</dt></span><span class="sxs-lookup"><span data-stu-id="0ee7d-119"><dt>**GLU\_SMOOTH**</dt></span></span> </dl> | <span data-ttu-id="0ee7d-120">Für jeden Scheitelpunkt einer Quadric wird eine normale generiert.</span><span class="sxs-lookup"><span data-stu-id="0ee7d-120">One normal is generated for every vertex of a quadric.</span></span> <span data-ttu-id="0ee7d-121">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="0ee7d-121">This is the default value.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ee7d-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ee7d-122">Return value</span></span>

<span data-ttu-id="0ee7d-123">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0ee7d-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ee7d-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ee7d-124">Remarks</span></span>

<span data-ttu-id="0ee7d-125">Die Funktion " **gluquadricnormals** " gibt an, welche Art von normalen für mit **quadobject** gerenderten viercs verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0ee7d-125">The **gluQuadricNormals** function specifies what kind of normals are to be used for quadrics rendered with **quadObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee7d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ee7d-126">Requirements</span></span>



| <span data-ttu-id="0ee7d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ee7d-127">Requirement</span></span> | <span data-ttu-id="0ee7d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0ee7d-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee7d-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ee7d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0ee7d-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ee7d-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0ee7d-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ee7d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0ee7d-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ee7d-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0ee7d-133">Header</span><span class="sxs-lookup"><span data-stu-id="0ee7d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ee7d-134"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ee7d-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="0ee7d-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0ee7d-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="0ee7d-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ee7d-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0ee7d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="0ee7d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ee7d-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ee7d-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ee7d-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ee7d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee7d-140">**glunewquadric**</span><span class="sxs-lookup"><span data-stu-id="0ee7d-140">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="0ee7d-141">**gluquadricdrawstyle**</span><span class="sxs-lookup"><span data-stu-id="0ee7d-141">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="0ee7d-142">**gluquadricorientation**</span><span class="sxs-lookup"><span data-stu-id="0ee7d-142">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="0ee7d-143">**gluquadrictexture**</span><span class="sxs-lookup"><span data-stu-id="0ee7d-143">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





