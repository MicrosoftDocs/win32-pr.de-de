---
title: glunewquadric-Funktion (glu. h)
description: Die Funktion "glunewquadric" erstellt ein Quadric-Objekt.
ms.assetid: 5a4289bf-b57a-4c74-b0e3-b7536671e4df
keywords:
- glunewquadric-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluNewQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: affedc7dcebd2b7925449e22cc1b902e88d936f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956696"
---
# <a name="glunewquadric-function"></a><span data-ttu-id="9798b-104">glunewquadric-Funktion</span><span class="sxs-lookup"><span data-stu-id="9798b-104">gluNewQuadric function</span></span>

<span data-ttu-id="9798b-105">Die Funktion " **glunewquadric** " erstellt ein Quadric-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9798b-105">The **gluNewQuadric** function creates a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9798b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9798b-106">Syntax</span></span>


```C++
GLUquadric* WINAPI gluNewQuadric(void);
```



## <a name="parameters"></a><span data-ttu-id="9798b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9798b-107">Parameters</span></span>

<span data-ttu-id="9798b-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9798b-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9798b-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9798b-109">Remarks</span></span>

<span data-ttu-id="9798b-110">Die Funktion " **glunewquadric** " erstellt einen Zeiger auf ein neues Quadric-Objekt und gibt diesen zurück.</span><span class="sxs-lookup"><span data-stu-id="9798b-110">The **gluNewQuadric** function creates and returns a pointer to a new quadric object.</span></span> <span data-ttu-id="9798b-111">Verweisen Sie auf dieses Objekt, wenn Sie Quadric-Rendering-und-Steuerungsfunktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9798b-111">Refer to this object when calling quadric rendering and control functions.</span></span> <span data-ttu-id="9798b-112">Der Rückgabewert 0 (null) bedeutet, dass nicht genügend Arbeitsspeicher vorhanden ist, um dem-Objekt zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="9798b-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="9798b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9798b-113">Requirements</span></span>



| <span data-ttu-id="9798b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9798b-114">Requirement</span></span> | <span data-ttu-id="9798b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9798b-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9798b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9798b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9798b-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9798b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9798b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9798b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9798b-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9798b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9798b-120">Header</span><span class="sxs-lookup"><span data-stu-id="9798b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9798b-121"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9798b-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9798b-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="9798b-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9798b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9798b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9798b-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9798b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9798b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9798b-127">**gluzylinder**</span><span class="sxs-lookup"><span data-stu-id="9798b-127">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="9798b-128">**gludeletequadric**</span><span class="sxs-lookup"><span data-stu-id="9798b-128">**gluDeleteQuadric**</span></span>](gludeletequadric.md)
</dt> <dt>

[<span data-ttu-id="9798b-129">**gludisk**</span><span class="sxs-lookup"><span data-stu-id="9798b-129">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="9798b-130">**glupartialdisk**</span><span class="sxs-lookup"><span data-stu-id="9798b-130">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="9798b-131">*gluvierccallback*</span><span class="sxs-lookup"><span data-stu-id="9798b-131">*gluQuadricCallback*</span></span>](gluquadric.md)
</dt> <dt>

[<span data-ttu-id="9798b-132">**gluquadricdrawstyle**</span><span class="sxs-lookup"><span data-stu-id="9798b-132">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="9798b-133">**gluquadricnormals**</span><span class="sxs-lookup"><span data-stu-id="9798b-133">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="9798b-134">**gluquadricorientation**</span><span class="sxs-lookup"><span data-stu-id="9798b-134">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="9798b-135">**gluquadrictexture**</span><span class="sxs-lookup"><span data-stu-id="9798b-135">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="9798b-136">**glusphere**</span><span class="sxs-lookup"><span data-stu-id="9798b-136">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





