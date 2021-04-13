---
title: Counters. Item (Eigenschaft)
description: Ruft die angegebene-Instanz aus der Auflistung ab.
ms.assetid: bf503371-c8bd-4e0d-ab8d-58de3f8fac5f
keywords:
- Element Eigenschaften-sysmon
- Item-Eigenschaft (Sysmon), counters-Klasse
- Indikatorenklasse "sysmon", Element Eigenschaft
topic_type:
- apiref
api_name:
- Counters.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251a645f0a4ceacdbfb4e2ab7e650f41e44dd508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475825"
---
# <a name="countersitem-property"></a><span data-ttu-id="c5029-106">Counters. Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c5029-106">Counters.Item property</span></span>

<span data-ttu-id="c5029-107">Ruft [**die angegebene-**](counteritem.md) Instanz aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="c5029-107">Retrieves the specified [**CounterItem**](counteritem.md) instance from the collection.</span></span>

<span data-ttu-id="c5029-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c5029-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5029-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5029-109">Syntax</span></span>


```VB
Property Item( _
  ByVal index As Object _
) As CounterItem
```



## <a name="property-value"></a><span data-ttu-id="c5029-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c5029-110">Property value</span></span>

<span data-ttu-id="c5029-111">Die Instanz des [**rattritem**](counteritem.md) , die dem angegebenen Indexwert entspricht.</span><span class="sxs-lookup"><span data-stu-id="c5029-111">[**CounterItem**](counteritem.md) instance that corresponds to the specified index value.</span></span>

## <a name="exceptions"></a><span data-ttu-id="c5029-112">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="c5029-112">Exceptions</span></span>



| <span data-ttu-id="c5029-113">Ausnahmetyp</span><span class="sxs-lookup"><span data-stu-id="c5029-113">Exception type</span></span>                                  | <span data-ttu-id="c5029-114">Bedingung</span><span class="sxs-lookup"><span data-stu-id="c5029-114">Condition</span></span>                         |
|-------------------------------------------------|-----------------------------------|
| <span data-ttu-id="c5029-115">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="c5029-115">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="c5029-116">Der angegebene Index ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c5029-116">The specified index is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c5029-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5029-117">Remarks</span></span>

<span data-ttu-id="c5029-118">Dies ist die Standard Eigenschaft des [**Counters**](counters.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="c5029-118">This is the default property of the [**Counters**](counters.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5029-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5029-119">Requirements</span></span>



| <span data-ttu-id="c5029-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5029-120">Requirement</span></span> | <span data-ttu-id="c5029-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c5029-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5029-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5029-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c5029-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5029-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c5029-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5029-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c5029-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5029-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5029-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c5029-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5029-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="c5029-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5029-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5029-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5029-129">**Ratteritem**</span><span class="sxs-lookup"><span data-stu-id="c5029-129">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="c5029-130">**Counters**</span><span class="sxs-lookup"><span data-stu-id="c5029-130">**Counters**</span></span>](counters.md)
</dt> </dl>

 

 





