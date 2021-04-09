---
title: gludeletetess-Funktion (glu. h)
description: Die Funktion "gludeletetess" zerstört ein Mosaik Objekt.
ms.assetid: 7e1540f7-5e7d-4a3b-8c94-5a6800b17411
keywords:
- gludeletetess-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluDeleteTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4625f0a9c2f51e9d7147c9564fcd4fb1fa7117
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740632"
---
# <a name="gludeletetess-function"></a><span data-ttu-id="95e88-104">gludeletetess-Funktion</span><span class="sxs-lookup"><span data-stu-id="95e88-104">gluDeleteTess function</span></span>

<span data-ttu-id="95e88-105">Die Funktion " **gludeletetess** " zerstört ein Mosaik Objekt.</span><span class="sxs-lookup"><span data-stu-id="95e88-105">The **gluDeleteTess** function destroys a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e88-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="95e88-106">Syntax</span></span>


```C++
void WINAPI gluDeleteTess(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="95e88-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="95e88-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95e88-108">*ATI*</span><span class="sxs-lookup"><span data-stu-id="95e88-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="95e88-109">Das Mosaik Objekt, das zerstört werden soll (mit [**glunewtess**](glunewtess.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="95e88-109">The tessellation object to destroy (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95e88-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95e88-110">Return value</span></span>

<span data-ttu-id="95e88-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="95e88-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95e88-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95e88-112">Remarks</span></span>

<span data-ttu-id="95e88-113">Die Funktion " **gludeletetess** " zerstört das festgestellte Mosaik Objekt und gibt den verwendeten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="95e88-113">The **gluDeleteTess** function destroys the indicated tessellation object and frees any memory that it used.</span></span>

## <a name="requirements"></a><span data-ttu-id="95e88-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95e88-114">Requirements</span></span>



| <span data-ttu-id="95e88-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95e88-115">Requirement</span></span> | <span data-ttu-id="95e88-116">Wert</span><span class="sxs-lookup"><span data-stu-id="95e88-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="95e88-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95e88-117">Minimum supported client</span></span><br/> | <span data-ttu-id="95e88-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95e88-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="95e88-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95e88-119">Minimum supported server</span></span><br/> | <span data-ttu-id="95e88-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95e88-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="95e88-121">Header</span><span class="sxs-lookup"><span data-stu-id="95e88-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="95e88-122"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="95e88-122"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="95e88-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95e88-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="95e88-124"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95e88-124"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="95e88-125">DLL</span><span class="sxs-lookup"><span data-stu-id="95e88-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95e88-126"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95e88-126"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95e88-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95e88-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95e88-128">**glunewtess**</span><span class="sxs-lookup"><span data-stu-id="95e88-128">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="95e88-129">**glutess beginpolygon**</span><span class="sxs-lookup"><span data-stu-id="95e88-129">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="95e88-130">*glutesscallback*</span><span class="sxs-lookup"><span data-stu-id="95e88-130">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





