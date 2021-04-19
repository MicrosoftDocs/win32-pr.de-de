---
title: glunewtess-Funktion (glu. h)
description: Die glunewtess-Funktion erstellt ein Mosaik Objekt.
ms.assetid: dfc9fce8-ecab-493b-85ee-6d7487814186
keywords:
- glunewtess-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluNewTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0573ead0cf9b81568c4bf2101e317bef7faf148
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338141"
---
# <a name="glunewtess-function"></a><span data-ttu-id="1437c-104">glunewtess-Funktion</span><span class="sxs-lookup"><span data-stu-id="1437c-104">gluNewTess function</span></span>

<span data-ttu-id="1437c-105">Die **glunewtess** -Funktion erstellt ein Mosaik Objekt.</span><span class="sxs-lookup"><span data-stu-id="1437c-105">The **gluNewTess** function creates a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1437c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1437c-106">Syntax</span></span>


```C++
GLUtesselator* WINAPI gluNewTess(void);
```



## <a name="parameters"></a><span data-ttu-id="1437c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1437c-107">Parameters</span></span>

<span data-ttu-id="1437c-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1437c-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1437c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1437c-109">Remarks</span></span>

<span data-ttu-id="1437c-110">Die Funktion " **glunewtess** " erstellt einen Zeiger auf ein neues Mosaik Objekt und gibt diesen zurück.</span><span class="sxs-lookup"><span data-stu-id="1437c-110">The **gluNewTess** function creates and returns a pointer to a new tessellation object.</span></span> <span data-ttu-id="1437c-111">Verweisen Sie auf dieses Objekt, wenn Sie Mosaik Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1437c-111">Refer to this object when calling tessellation functions.</span></span> <span data-ttu-id="1437c-112">Der Rückgabewert 0 (null) bedeutet, dass nicht genügend Arbeitsspeicher vorhanden ist, um dem-Objekt zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="1437c-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1437c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1437c-113">Requirements</span></span>



| <span data-ttu-id="1437c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1437c-114">Requirement</span></span> | <span data-ttu-id="1437c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1437c-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1437c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1437c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1437c-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1437c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1437c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1437c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1437c-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1437c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1437c-120">Header</span><span class="sxs-lookup"><span data-stu-id="1437c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1437c-121"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="1437c-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="1437c-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1437c-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="1437c-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1437c-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1437c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1437c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1437c-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1437c-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1437c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1437c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1437c-127">**gludeletetess**</span><span class="sxs-lookup"><span data-stu-id="1437c-127">**gluDeleteTess**</span></span>](gludeletetess.md)
</dt> <dt>

[<span data-ttu-id="1437c-128">**glutess beginpolygon**</span><span class="sxs-lookup"><span data-stu-id="1437c-128">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="1437c-129">*glutesscallback*</span><span class="sxs-lookup"><span data-stu-id="1437c-129">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





