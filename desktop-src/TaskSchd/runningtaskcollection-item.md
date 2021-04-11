---
title: Runningtaskcollection. Item-Eigenschaft
description: Ruft bei der Skripterstellung die angegebene Aufgabe aus der Auflistung ab.
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- Element Eigenschaft Taskplaner
- Item-Eigenschaft Taskplaner, runningtaskcollection-Objekt
- Runningtaskcollection-Objekt Taskplaner, Element Eigenschaft
topic_type:
- apiref
api_name:
- RunningTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d28da7a3f5348ff9f5d6171a1a698d95b646f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104649"
---
# <a name="runningtaskcollectionitem-property"></a><span data-ttu-id="ed441-106">Runningtaskcollection. Item-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ed441-106">RunningTaskCollection.Item property</span></span>

<span data-ttu-id="ed441-107">Ruft bei der Skripterstellung die angegebene Aufgabe aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="ed441-107">For scripting, gets the specified task from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed441-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed441-108">Syntax</span></span>


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a><span data-ttu-id="ed441-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ed441-109">Property value</span></span>

<span data-ttu-id="ed441-110">Ein [**runningtask**](runningtask.md) -Objekt, das den angeforderten Kontext enthält.</span><span class="sxs-lookup"><span data-stu-id="ed441-110">A [**RunningTask**](runningtask.md) object that contains the requested context.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed441-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed441-111">Remarks</span></span>

<span data-ttu-id="ed441-112">Sammlungen sind 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="ed441-112">Collections are 1-based.</span></span> <span data-ttu-id="ed441-113">Anders ausgedrückt: der Index für das erste Element in der Auflistung ist 1.</span><span class="sxs-lookup"><span data-stu-id="ed441-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed441-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed441-114">Requirements</span></span>



| <span data-ttu-id="ed441-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed441-115">Requirement</span></span> | <span data-ttu-id="ed441-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ed441-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed441-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed441-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ed441-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed441-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ed441-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed441-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ed441-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed441-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ed441-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ed441-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="ed441-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ed441-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ed441-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ed441-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed441-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed441-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed441-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed441-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed441-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="ed441-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





