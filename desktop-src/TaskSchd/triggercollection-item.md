---
title: TriggerCollection. Item-Eigenschaft
description: Ruft bei der Skripterstellung den angegebenen-Auslösers aus der Auflistung ab.
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- Element Eigenschaft Taskplaner
- Element Eigenschaft Taskplaner, TriggerCollection-Objekt
- TriggerCollection-Objekt Taskplaner, Element Eigenschaft
topic_type:
- apiref
api_name:
- TriggerCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d600418d43459d6c4cbfcb0746a378633d096c24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740776"
---
# <a name="triggercollectionitem-property"></a><span data-ttu-id="a35e1-106">TriggerCollection. Item-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a35e1-106">TriggerCollection.Item property</span></span>

<span data-ttu-id="a35e1-107">Ruft bei der Skripterstellung den angegebenen-Auslösers aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="a35e1-107">For scripting, gets the specified trigger from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a35e1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a35e1-108">Syntax</span></span>


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a><span data-ttu-id="a35e1-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a35e1-109">Property value</span></span>

<span data-ttu-id="a35e1-110">Ein [**Auslöserobjekt**](trigger.md) , das den angeforderten-Auslösers darstellt</span><span class="sxs-lookup"><span data-stu-id="a35e1-110">A [**Trigger**](trigger.md) object that represents the requested trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="a35e1-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a35e1-111">Remarks</span></span>

<span data-ttu-id="a35e1-112">Sammlungen sind 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="a35e1-112">Collections are 1-based.</span></span> <span data-ttu-id="a35e1-113">Anders ausgedrückt: der Index für das erste Element in der Auflistung ist 1.</span><span class="sxs-lookup"><span data-stu-id="a35e1-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="a35e1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a35e1-114">Requirements</span></span>



| <span data-ttu-id="a35e1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a35e1-115">Requirement</span></span> | <span data-ttu-id="a35e1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a35e1-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a35e1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a35e1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a35e1-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a35e1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a35e1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a35e1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a35e1-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a35e1-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a35e1-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a35e1-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="a35e1-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a35e1-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a35e1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a35e1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a35e1-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a35e1-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a35e1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a35e1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a35e1-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="a35e1-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





