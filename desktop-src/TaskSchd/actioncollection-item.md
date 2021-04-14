---
title: Aktions Collection. Item-Eigenschaft
description: Ruft bei der Skripterstellung eine angegebene Aktion aus der Auflistung ab.
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- Element Eigenschaft Taskplaner
- Item-Eigenschaft Taskplaner, Aktions Sammlungsobjekt
- Aktions Sammlungsobjekt Taskplaner, Element Eigenschaft
topic_type:
- apiref
api_name:
- ActionCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4853009c547f3bdfbb269e512ce5d39273726095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392089"
---
# <a name="actioncollectionitem-property"></a><span data-ttu-id="489cd-106">Aktions Collection. Item-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="489cd-106">ActionCollection.Item property</span></span>

<span data-ttu-id="489cd-107">Ruft bei der Skripterstellung eine angegebene Aktion aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="489cd-107">For scripting, gets a specified action from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="489cd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="489cd-108">Syntax</span></span>


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a><span data-ttu-id="489cd-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="489cd-109">Property value</span></span>

<span data-ttu-id="489cd-110">Ein [**Aktions**](action.md) Objekt, das die angeforderte Aktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="489cd-110">An [**Action**](action.md) object that represents the requested action.</span></span>

## <a name="remarks"></a><span data-ttu-id="489cd-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="489cd-111">Remarks</span></span>

<span data-ttu-id="489cd-112">Sammlungen sind 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="489cd-112">Collections are 1-based.</span></span> <span data-ttu-id="489cd-113">Anders ausgedrückt: der Index für das erste Element in der Auflistung ist 1.</span><span class="sxs-lookup"><span data-stu-id="489cd-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="489cd-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="489cd-114">Requirements</span></span>



| <span data-ttu-id="489cd-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="489cd-115">Requirement</span></span> | <span data-ttu-id="489cd-116">Wert</span><span class="sxs-lookup"><span data-stu-id="489cd-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="489cd-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="489cd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="489cd-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="489cd-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="489cd-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="489cd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="489cd-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="489cd-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="489cd-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="489cd-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="489cd-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="489cd-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="489cd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="489cd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="489cd-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="489cd-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="489cd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="489cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="489cd-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="489cd-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="489cd-127">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="489cd-127">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





