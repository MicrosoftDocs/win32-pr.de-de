---
title: gludeletenurbsrenderer-Funktion (glu. h)
description: Die Funktion "gludeletenurbsrenderer" zerstört ein nicht einheitliches Rational B-Spline-Objekt (NURBS).
ms.assetid: 77063dcb-90b8-47e4-8b00-e1c46cf4f712
keywords:
- gludeletenurbsrenderer-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluDeleteNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fb6ecf0bbb7076d4d6292676d3d358586d0986c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741417"
---
# <a name="gludeletenurbsrenderer-function"></a><span data-ttu-id="79535-104">gludeletenurbsrenderer-Funktion</span><span class="sxs-lookup"><span data-stu-id="79535-104">gluDeleteNurbsRenderer function</span></span>

<span data-ttu-id="79535-105">Die Funktion " **gludeletenurbsrenderer** " zerstört ein nicht einheitliches Rational B-Spline-Objekt ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="79535-105">The **gluDeleteNurbsRenderer** function destroys a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="79535-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="79535-106">Syntax</span></span>


```C++
void WINAPI gluDeleteNurbsRenderer(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="79535-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="79535-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79535-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="79535-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="79535-109">Das NURBS-Objekt, das zerstört werden soll (mit **glunewnurbsrenderer** erstellt).</span><span class="sxs-lookup"><span data-stu-id="79535-109">The NURBS object to be destroyed (created with **gluNewNurbsRenderer**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79535-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79535-110">Return value</span></span>

<span data-ttu-id="79535-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="79535-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79535-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79535-112">Remarks</span></span>

<span data-ttu-id="79535-113">Die Funktion " **gludeletenurbsrenderer** " zerstört das NURBS-Objekt und gibt den verwendeten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="79535-113">The **gluDeleteNurbsRenderer** function destroys the NURBS object and frees any memory that it used.</span></span> <span data-ttu-id="79535-114">Nachdem Sie " **gludeletenurbsrenderer**" aufgerufen haben, können Sie *nobj* nicht mehr verwenden.</span><span class="sxs-lookup"><span data-stu-id="79535-114">After you have called **gluDeleteNurbsRenderer**, you cannot use *nobj* again.</span></span>

## <a name="requirements"></a><span data-ttu-id="79535-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79535-115">Requirements</span></span>



| <span data-ttu-id="79535-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79535-116">Requirement</span></span> | <span data-ttu-id="79535-117">Wert</span><span class="sxs-lookup"><span data-stu-id="79535-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="79535-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79535-118">Minimum supported client</span></span><br/> | <span data-ttu-id="79535-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79535-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="79535-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79535-120">Minimum supported server</span></span><br/> | <span data-ttu-id="79535-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79535-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="79535-122">Header</span><span class="sxs-lookup"><span data-stu-id="79535-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="79535-123"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="79535-123"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="79535-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="79535-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="79535-125"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79535-125"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="79535-126">DLL</span><span class="sxs-lookup"><span data-stu-id="79535-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79535-127"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79535-127"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79535-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79535-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79535-129">**glunewnurbsrenderer**</span><span class="sxs-lookup"><span data-stu-id="79535-129">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





