---
title: gludeletequadric-Funktion (glu. h)
description: Die Funktion "gludeletequadric" zerstört ein Quadric-Objekt.
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- gludeletequadric-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluDeleteQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b5ee85e943cd958e394efb191932393d228d948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742232"
---
# <a name="gludeletequadric-function"></a><span data-ttu-id="7dd52-104">gludeletequadric-Funktion</span><span class="sxs-lookup"><span data-stu-id="7dd52-104">gluDeleteQuadric function</span></span>

<span data-ttu-id="7dd52-105">Die Funktion " **gludeletequadric** " zerstört ein Quadric-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7dd52-105">The **gluDeleteQuadric** function destroys a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dd52-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7dd52-106">Syntax</span></span>


```C++
void WINAPI gluDeleteQuadric(
   GLUquadricObj *state
);
```



## <a name="parameters"></a><span data-ttu-id="7dd52-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7dd52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dd52-108">*state*</span><span class="sxs-lookup"><span data-stu-id="7dd52-108">*state*</span></span> 
</dt> <dd>

<span data-ttu-id="7dd52-109">Das zu zerstörende quadrische Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="7dd52-109">The quadric object to be destroyed (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dd52-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7dd52-110">Return value</span></span>

<span data-ttu-id="7dd52-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7dd52-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dd52-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7dd52-112">Remarks</span></span>

<span data-ttu-id="7dd52-113">Die Funktion " **gludeletequadric** " zerstört das Quadric-Objekt und gibt den verwendeten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="7dd52-113">The **gluDeleteQuadric** function destroys the quadric object and frees any memory that it used.</span></span> <span data-ttu-id="7dd52-114">Nachdem Sie " **gludeletequadric**" aufgerufen haben, können Sie den *Zustand* nicht mehr verwenden.</span><span class="sxs-lookup"><span data-stu-id="7dd52-114">After you have called **gluDeleteQuadric**, you cannot use *state* again.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dd52-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7dd52-115">Requirements</span></span>



| <span data-ttu-id="7dd52-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7dd52-116">Requirement</span></span> | <span data-ttu-id="7dd52-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7dd52-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd52-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7dd52-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7dd52-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7dd52-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7dd52-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7dd52-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7dd52-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7dd52-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7dd52-122">Header</span><span class="sxs-lookup"><span data-stu-id="7dd52-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dd52-123"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dd52-123"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="7dd52-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7dd52-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="7dd52-125"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7dd52-125"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7dd52-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7dd52-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dd52-127"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dd52-127"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dd52-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7dd52-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dd52-129">**glunewquadric**</span><span class="sxs-lookup"><span data-stu-id="7dd52-129">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> </dl>

 

 





