---
title: gluOrtho2D-Funktion (Glu.h)
description: Die gluOrtho2D-Funktion definiert eine orthografische 2D-Projektionsmatrix.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- gluOrtho2D-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluOrtho2D
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf07fea583c5ae46680d888f6bf6c0a9c5aa9a0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153553"
---
# <a name="gluortho2d-function"></a><span data-ttu-id="e83d5-104">gluOrtho2D-Funktion</span><span class="sxs-lookup"><span data-stu-id="e83d5-104">gluOrtho2D function</span></span>

<span data-ttu-id="e83d5-105">Die **gluOrtho2D-Funktion** definiert eine orthografische 2D-Projektionsmatrix.</span><span class="sxs-lookup"><span data-stu-id="e83d5-105">The **gluOrtho2D** function defines a 2-D orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e83d5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e83d5-106">Syntax</span></span>


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a><span data-ttu-id="e83d5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e83d5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e83d5-108">*Links*</span><span class="sxs-lookup"><span data-stu-id="e83d5-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="e83d5-109">Die Koordinate für die linke vertikale Clippingebene.</span><span class="sxs-lookup"><span data-stu-id="e83d5-109">The coordinate for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="e83d5-110">*Richting*</span><span class="sxs-lookup"><span data-stu-id="e83d5-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="e83d5-111">Die Koordinate für die rechte vertikale Clippingebene.</span><span class="sxs-lookup"><span data-stu-id="e83d5-111">The coordinate for the right vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="e83d5-112">*top*</span><span class="sxs-lookup"><span data-stu-id="e83d5-112">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="e83d5-113">Die Koordinate für die obere horizontale Ausschneideebene.</span><span class="sxs-lookup"><span data-stu-id="e83d5-113">The coordinate for the top horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="e83d5-114">*Unteres*</span><span class="sxs-lookup"><span data-stu-id="e83d5-114">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="e83d5-115">Die Koordinate für die untere horizontale Ausschneideebene.</span><span class="sxs-lookup"><span data-stu-id="e83d5-115">The coordinate for the bottom horizontal clipping plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e83d5-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e83d5-116">Return value</span></span>

<span data-ttu-id="e83d5-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e83d5-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e83d5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e83d5-118">Remarks</span></span>

<span data-ttu-id="e83d5-119">Die **gluOrtho2D-Funktion** richtet einen zweidimensionalen orthografischen Anzeigebereich ein.</span><span class="sxs-lookup"><span data-stu-id="e83d5-119">The **gluOrtho2D** function sets up a two-dimensional orthographic viewing region.</span></span> <span data-ttu-id="e83d5-120">Dies entspricht dem Aufrufen von [**glOrtho**](glortho.md) mit zNear = -1 und zFar = 1.</span><span class="sxs-lookup"><span data-stu-id="e83d5-120">This is equivalent to calling [**glOrtho**](glortho.md) with zNear = -1 and zFar = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="e83d5-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e83d5-121">Requirements</span></span>



| <span data-ttu-id="e83d5-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e83d5-122">Requirement</span></span> | <span data-ttu-id="e83d5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e83d5-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e83d5-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e83d5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e83d5-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e83d5-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e83d5-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e83d5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e83d5-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e83d5-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e83d5-128">Header</span><span class="sxs-lookup"><span data-stu-id="e83d5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e83d5-129"><dt>Glu.h</dt></span><span class="sxs-lookup"><span data-stu-id="e83d5-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="e83d5-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e83d5-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="e83d5-131"><dt>Glu32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e83d5-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e83d5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e83d5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e83d5-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e83d5-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e83d5-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e83d5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e83d5-135">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="e83d5-135">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="e83d5-136">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="e83d5-136">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





