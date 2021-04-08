---
title: Struktur "netwheader"
description: Enthält die Anzahl der Symbol-oder Cursor Komponenten in einer Ressourcengruppe. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 1549579a-b558-42a9-9b3b-5b382334221c
keywords:
- Menüs für die netwheader-Struktur und weitere Ressourcen
topic_type:
- apiref
api_name:
- NEWHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d215bc00ef414d4e626d3da657dcecfd7a8a6c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949554"
---
# <a name="newheader-structure"></a><span data-ttu-id="ac762-105">Struktur "netwheader"</span><span class="sxs-lookup"><span data-stu-id="ac762-105">NEWHEADER structure</span></span>

<span data-ttu-id="ac762-106">Enthält die Anzahl der Symbol-oder Cursor Komponenten in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ac762-106">Contains the number of icon or cursor components in a resource group.</span></span> <span data-ttu-id="ac762-107">Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ac762-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac762-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac762-108">Syntax</span></span>


```C++
typedef struct {
  WORD Reserved;
  WORD ResType;
  WORD ResCount;
} NEWHEADER, *NEWHEADER;
```



## <a name="members"></a><span data-ttu-id="ac762-109">Member</span><span class="sxs-lookup"><span data-stu-id="ac762-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="ac762-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="ac762-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="ac762-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="ac762-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ac762-112">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="ac762-112">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ac762-113">**RESTYPE**</span><span class="sxs-lookup"><span data-stu-id="ac762-113">**ResType**</span></span>
</dt> <dd>

<span data-ttu-id="ac762-114">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="ac762-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ac762-115">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="ac762-115">The resource type.</span></span> <span data-ttu-id="ac762-116">Dieser Member muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ac762-116">This member must have one of the following values.</span></span>



| <span data-ttu-id="ac762-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ac762-117">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="ac762-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ac762-118">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="RES_CURSOR"></span><span id="res_cursor"></span><dl> <span data-ttu-id="ac762-119"><dt>**Res \_ Cursor**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ac762-119"><dt>**RES\_CURSOR**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="ac762-120">Der Cursor Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="ac762-120">Cursor resource type.</span></span><br/> |
| <span id="RES_ICON"></span><span id="res_icon"></span><dl> <span data-ttu-id="ac762-121"><dt>**Res \_ Symbol**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ac762-121"><dt>**RES\_ICON**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="ac762-122">Symbol Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="ac762-122">Icon resource type.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="ac762-123">**Rescount**</span><span class="sxs-lookup"><span data-stu-id="ac762-123">**ResCount**</span></span>
</dt> <dd>

<span data-ttu-id="ac762-124">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="ac762-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ac762-125">Die Anzahl der Symbol-oder Cursor Komponenten in der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ac762-125">The number of icon or cursor components in the resource group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac762-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac762-126">Remarks</span></span>

<span data-ttu-id="ac762-127">Eine oder mehrere [**resdir**](resdir.md) -Strukturen folgen direkt der Struktur " **netwheader** " in der RES-Datei.</span><span class="sxs-lookup"><span data-stu-id="ac762-127">One or more [**RESDIR**](resdir.md) structures immediately follow the **NEWHEADER** structure in the .res file.</span></span> <span data-ttu-id="ac762-128">Der **rescount** -Member gibt die Anzahl der **resdir** -Strukturen an.</span><span class="sxs-lookup"><span data-stu-id="ac762-128">The **ResCount** member specifies the number of **RESDIR** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac762-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac762-129">Requirements</span></span>



| <span data-ttu-id="ac762-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac762-130">Requirement</span></span> | <span data-ttu-id="ac762-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ac762-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ac762-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac762-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ac762-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac762-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ac762-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac762-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ac762-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac762-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ac762-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac762-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="ac762-137">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="ac762-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ac762-138">**Resdir**</span><span class="sxs-lookup"><span data-stu-id="ac762-138">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="ac762-139">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ac762-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ac762-140">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ac762-140">Resources</span></span>](resources.md)
</dt> </dl>

 

 





