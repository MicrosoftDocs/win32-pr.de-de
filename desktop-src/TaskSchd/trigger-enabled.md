---
title: Eigenschaft "Auslösung"
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.
ms.assetid: 8fb5a0cc-ddd4-430d-9593-95a4cb311f18
keywords:
- Aktivierte Eigenschaften Taskplaner
- Aktivierte Eigenschaften Taskplaner, Auslöserobjekt
- Auslöse Objekt Taskplaner, aktivierte Eigenschaft
topic_type:
- apiref
api_name:
- Trigger.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411bc36dcf03933e2b4cee2f575aaec3b8133846
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949638"
---
# <a name="triggerenabled-property"></a><span data-ttu-id="6147e-106">Eigenschaft "Auslösung"</span><span class="sxs-lookup"><span data-stu-id="6147e-106">Trigger.Enabled property</span></span>

<span data-ttu-id="6147e-107">Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="6147e-107">For scripting, gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="6147e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6147e-108">Syntax</span></span>


```VB
Trigger.Enabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="6147e-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6147e-109">Property value</span></span>

<span data-ttu-id="6147e-110">True, wenn der-Wert aktiviert ist. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="6147e-110">True if the trigger is enabled; otherwise, false.</span></span> <span data-ttu-id="6147e-111">Der Standardwert ist "True".</span><span class="sxs-lookup"><span data-stu-id="6147e-111">The default is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="6147e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6147e-112">Remarks</span></span>

<span data-ttu-id="6147e-113">Beim Lesen oder Schreiben von XML für eine Aufgabe wird die aktivierte Eigenschaft mit dem [**aktivierten**](taskschedulerschema-enabled-triggerbasetype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="6147e-113">When reading or writing XML for a task, the enabled property is specified using the [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="6147e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6147e-114">Requirements</span></span>



| <span data-ttu-id="6147e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6147e-115">Requirement</span></span> | <span data-ttu-id="6147e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6147e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6147e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6147e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6147e-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6147e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6147e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6147e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6147e-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6147e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6147e-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6147e-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="6147e-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6147e-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6147e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6147e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6147e-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6147e-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6147e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6147e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6147e-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="6147e-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





