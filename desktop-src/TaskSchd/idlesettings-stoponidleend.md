---
title: Idlesettings. stoponidleend (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe beendet, wenn die Leerlauf Bedingung endet, bevor die Aufgabe abgeschlossen wird, oder legt diesen fest.
ms.assetid: 5908bf6b-227a-4234-a741-82cf38163171
keywords:
- Stoponidleend-Eigenschaft Taskplaner
- Stoponidleend-Eigenschaft Taskplaner, idlesettings-Objekt
- Idlesettings-Objekt Taskplaner, stoponidleend-Eigenschaft
topic_type:
- apiref
api_name:
- IdleSettings.StopOnIdleEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f475c0a05d43cf0fbdd7097c1ee083f9040b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858740"
---
# <a name="idlesettingsstoponidleend-property"></a><span data-ttu-id="e50ee-106">Idlesettings. stoponidleend (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e50ee-106">IdleSettings.StopOnIdleEnd property</span></span>

<span data-ttu-id="e50ee-107">Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe beendet, wenn die Leerlauf Bedingung endet, bevor die Aufgabe abgeschlossen wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="e50ee-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e50ee-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e50ee-108">Syntax</span></span>


```VB
IdleSettings.StopOnIdleEnd As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e50ee-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e50ee-109">Property value</span></span>

<span data-ttu-id="e50ee-110">Ein boolescher Wert, der angibt, dass die Taskplaner die Aufgabe beendet, wenn die Leerlauf Bedingung endet, bevor die Aufgabe abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="e50ee-110">A Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e50ee-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e50ee-111">Remarks</span></span>

<span data-ttu-id="e50ee-112">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**stoponidleend**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="e50ee-112">When reading or writing XML for a task, this setting is specified in the [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="e50ee-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e50ee-113">Requirements</span></span>



| <span data-ttu-id="e50ee-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e50ee-114">Requirement</span></span> | <span data-ttu-id="e50ee-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e50ee-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e50ee-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e50ee-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e50ee-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e50ee-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e50ee-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e50ee-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e50ee-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e50ee-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e50ee-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e50ee-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="e50ee-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e50ee-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e50ee-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e50ee-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e50ee-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e50ee-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e50ee-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e50ee-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e50ee-125">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="e50ee-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e50ee-126">**Idlesettings**</span><span class="sxs-lookup"><span data-stu-id="e50ee-126">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





