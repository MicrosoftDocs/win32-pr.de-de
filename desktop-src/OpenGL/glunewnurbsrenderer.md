---
title: glunewnurbsrenderer-Funktion (glu. h)
description: Die glunewnurbsrenderer-Funktion erstellt ein nicht einheitliches Rational B-Spline-Objekt (NURBS).
ms.assetid: f47badb0-6b75-4bfd-9771-516668d9e255
keywords:
- glunewnurbsrenderer-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluNewNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b6e35df5abd9fb9e7757dd79066fbbe7efe8680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956697"
---
# <a name="glunewnurbsrenderer-function"></a><span data-ttu-id="249ed-104">glunewnurbsrenderer-Funktion</span><span class="sxs-lookup"><span data-stu-id="249ed-104">gluNewNurbsRenderer function</span></span>

<span data-ttu-id="249ed-105">Die **glunewnurbsrenderer** -Funktion erstellt ein nicht einheitliches Rational B-Spline-Objekt ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="249ed-105">The **gluNewNurbsRenderer** function creates a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="249ed-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="249ed-106">Syntax</span></span>


```C++
GLUnurbs* WINAPI gluNewNurbsRenderer(void);
```



## <a name="parameters"></a><span data-ttu-id="249ed-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="249ed-107">Parameters</span></span>

<span data-ttu-id="249ed-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="249ed-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="249ed-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="249ed-109">Remarks</span></span>

<span data-ttu-id="249ed-110">Die Funktion " **glunewnurbsrenderer** " erstellt einen Zeiger auf ein neues NURBS-Objekt und gibt diesen zurück.</span><span class="sxs-lookup"><span data-stu-id="249ed-110">The **gluNewNurbsRenderer** function creates and returns a pointer to a new NURBS object.</span></span> <span data-ttu-id="249ed-111">Lesen Sie dieses Objekt, wenn Sie die Funktionen zum Rendern und Steuern von nursb aufrufen.</span><span class="sxs-lookup"><span data-stu-id="249ed-111">Refer to this object when calling NURBS rendering and control functions.</span></span> <span data-ttu-id="249ed-112">Der Rückgabewert 0 (null) bedeutet, dass nicht genügend Arbeitsspeicher vorhanden ist, um dem-Objekt zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="249ed-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="249ed-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="249ed-113">Requirements</span></span>



| <span data-ttu-id="249ed-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="249ed-114">Requirement</span></span> | <span data-ttu-id="249ed-115">Wert</span><span class="sxs-lookup"><span data-stu-id="249ed-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="249ed-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="249ed-116">Minimum supported client</span></span><br/> | <span data-ttu-id="249ed-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="249ed-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="249ed-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="249ed-118">Minimum supported server</span></span><br/> | <span data-ttu-id="249ed-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="249ed-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="249ed-120">Header</span><span class="sxs-lookup"><span data-stu-id="249ed-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="249ed-121"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="249ed-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="249ed-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="249ed-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="249ed-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="249ed-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="249ed-124">DLL</span><span class="sxs-lookup"><span data-stu-id="249ed-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="249ed-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="249ed-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="249ed-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="249ed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="249ed-127">**glubegincurve**</span><span class="sxs-lookup"><span data-stu-id="249ed-127">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="249ed-128">**glubeginsurface**</span><span class="sxs-lookup"><span data-stu-id="249ed-128">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="249ed-129">**glubegintrim**</span><span class="sxs-lookup"><span data-stu-id="249ed-129">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="249ed-130">**gludeletenurbsrenderer**</span><span class="sxs-lookup"><span data-stu-id="249ed-130">**gluDeleteNurbsRenderer**</span></span>](gludeletenurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="249ed-131">*glunurbscallback*</span><span class="sxs-lookup"><span data-stu-id="249ed-131">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="249ed-132">**glunurbsproperty**</span><span class="sxs-lookup"><span data-stu-id="249ed-132">**gluNurbsProperty**</span></span>](glunurbsproperty.md)
</dt> </dl>

 

 





