---
title: Registeredtask. NextRunTime (Eigenschaft)
description: Ruft bei der Skripterstellung die Uhrzeit ab, zu der der registrierte Task die nächste geplante Ausführung ist.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- NextRunTime-Eigenschaft Taskplaner
- NextRunTime-Eigenschaft Taskplaner, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, NextRunTime-Eigenschaft
topic_type:
- apiref
api_name:
- RegisteredTask.NextRunTime
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94db26c023ddd2c146586fbc433548517a84f234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742777"
---
# <a name="registeredtasknextruntime-property"></a><span data-ttu-id="91bf8-106">Registeredtask. NextRunTime (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="91bf8-106">RegisteredTask.NextRunTime property</span></span>

<span data-ttu-id="91bf8-107">Ruft bei der Skripterstellung die Uhrzeit ab, zu der der registrierte Task die nächste geplante Ausführung ist.</span><span class="sxs-lookup"><span data-stu-id="91bf8-107">For scripting, gets the time when the registered task is next scheduled to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="91bf8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="91bf8-108">Syntax</span></span>


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a><span data-ttu-id="91bf8-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="91bf8-109">Property value</span></span>

<span data-ttu-id="91bf8-110">Der Zeitpunkt der nächsten geplanten Ausführung der registrierten Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="91bf8-110">The time when the registered task is next scheduled to run.</span></span>

## <a name="remarks"></a><span data-ttu-id="91bf8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91bf8-111">Remarks</span></span>

<span data-ttu-id="91bf8-112">Wenn die registrierte Aufgabe einzeln deaktivierte Trigger enthält, wirken sich diese Trigger weiterhin auf die nächste geplante Laufzeit aus, die zurückgegeben wird, auch wenn Sie deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="91bf8-112">If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="91bf8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91bf8-113">Requirements</span></span>



| <span data-ttu-id="91bf8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91bf8-114">Requirement</span></span> | <span data-ttu-id="91bf8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="91bf8-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91bf8-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91bf8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="91bf8-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91bf8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="91bf8-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91bf8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="91bf8-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91bf8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="91bf8-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="91bf8-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="91bf8-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="91bf8-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="91bf8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="91bf8-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91bf8-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91bf8-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91bf8-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91bf8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91bf8-125">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="91bf8-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="91bf8-126">**Registeredtask**</span><span class="sxs-lookup"><span data-stu-id="91bf8-126">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





