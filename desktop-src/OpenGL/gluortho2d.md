---
title: gluOrtho2D-Funktion (glu. h)
description: Die gluOrtho2D-Funktion definiert eine 2D-Projektions Matrix (orthografische).
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
ms.openlocfilehash: a36b321f312a074a5dd78340968f1c9b2b844c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391500"
---
# <a name="gluortho2d-function"></a><span data-ttu-id="1dc7d-104">gluOrtho2D-Funktion</span><span class="sxs-lookup"><span data-stu-id="1dc7d-104">gluOrtho2D function</span></span>

<span data-ttu-id="1dc7d-105">Die **gluOrtho2D** -Funktion definiert eine 2D-Projektions Matrix (orthografische).</span><span class="sxs-lookup"><span data-stu-id="1dc7d-105">The **gluOrtho2D** function defines a 2-D orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc7d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dc7d-106">Syntax</span></span>


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a><span data-ttu-id="1dc7d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1dc7d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dc7d-108">*linken*</span><span class="sxs-lookup"><span data-stu-id="1dc7d-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="1dc7d-109">Die Koordinate für die linke vertikale Clippingebene.</span><span class="sxs-lookup"><span data-stu-id="1dc7d-109">The coordinate for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="1dc7d-110">*Richting*</span><span class="sxs-lookup"><span data-stu-id="1dc7d-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="1dc7d-111">Die Koordinate für die Rechte vertikale Clippingebene.</span><span class="sxs-lookup"><span data-stu-id="1dc7d-111">The coordinate for the right vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="1dc7d-112">*top*</span><span class="sxs-lookup"><span data-stu-id="1dc7d-112">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="1dc7d-113">Die Koordinate für die obere horizontale Clippingebene.</span><span class="sxs-lookup"><span data-stu-id="1dc7d-113">The coordinate for the top horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="1dc7d-114">*unten*</span><span class="sxs-lookup"><span data-stu-id="1dc7d-114">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="1dc7d-115">Die Koordinate für die untere horizontale Clippingebene.</span><span class="sxs-lookup"><span data-stu-id="1dc7d-115">The coordinate for the bottom horizontal clipping plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dc7d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1dc7d-116">Return value</span></span>

<span data-ttu-id="1dc7d-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1dc7d-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dc7d-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1dc7d-118">Remarks</span></span>

<span data-ttu-id="1dc7d-119">Die **gluOrtho2D** -Funktion richtet einen zweidimensionalen orthografischen Anzeigebereich ein.</span><span class="sxs-lookup"><span data-stu-id="1dc7d-119">The **gluOrtho2D** function sets up a two-dimensional orthographic viewing region.</span></span> <span data-ttu-id="1dc7d-120">Dies entspricht dem Aufrufen von [**glortho**](glortho.md) mit Near = 1 und far = 1.</span><span class="sxs-lookup"><span data-stu-id="1dc7d-120">This is equivalent to calling [**glOrtho**](glortho.md) with near =  1 and far = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dc7d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1dc7d-121">Requirements</span></span>



| <span data-ttu-id="1dc7d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1dc7d-122">Requirement</span></span> | <span data-ttu-id="1dc7d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1dc7d-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc7d-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1dc7d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1dc7d-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1dc7d-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1dc7d-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1dc7d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1dc7d-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1dc7d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1dc7d-128">Header</span><span class="sxs-lookup"><span data-stu-id="1dc7d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dc7d-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dc7d-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="1dc7d-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1dc7d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="1dc7d-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1dc7d-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1dc7d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1dc7d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dc7d-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dc7d-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dc7d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dc7d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc7d-135">**glortho**</span><span class="sxs-lookup"><span data-stu-id="1dc7d-135">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="1dc7d-136">**gluperspective**</span><span class="sxs-lookup"><span data-stu-id="1dc7d-136">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





