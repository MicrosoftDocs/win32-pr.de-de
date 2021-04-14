---
title: Registeredtask. State (Eigenschaft)
description: Ruft bei der Skripterstellung den Betriebsstatus der registrierten Aufgabe ab.
ms.assetid: 1acd4946-322f-4f24-b317-92be80e19de5
keywords:
- State-Eigenschaft Taskplaner
- State-Eigenschaft Taskplaner, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, State-Eigenschaft
topic_type:
- apiref
api_name:
- RegisteredTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47af082174bc6927a16760e87566f311ec9f4a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478909"
---
# <a name="registeredtaskstate-property"></a><span data-ttu-id="799ea-106">Registeredtask. State (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="799ea-106">RegisteredTask.State property</span></span>

<span data-ttu-id="799ea-107">Ruft bei der Skripterstellung den Betriebsstatus der registrierten Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="799ea-107">For scripting, gets the operational state of the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="799ea-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="799ea-108">Syntax</span></span>


```VB
RegisteredTask.State As Integer
```



## <a name="property-value"></a><span data-ttu-id="799ea-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="799ea-109">Property value</span></span>

<span data-ttu-id="799ea-110">Eine [**Task \_ Zustands**](/windows/desktop/api/taskschd/ne-taskschd-task_state) Konstante, die den Betriebszustand der Aufgabe definiert.</span><span class="sxs-lookup"><span data-stu-id="799ea-110">A [**TASK\_STATE**](/windows/desktop/api/taskschd/ne-taskschd-task_state) constant that defines the operational state of the task.</span></span>



| <span data-ttu-id="799ea-111">Wert</span><span class="sxs-lookup"><span data-stu-id="799ea-111">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="799ea-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="799ea-112">Meaning</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <span data-ttu-id="799ea-113"><dt>**Aufgabe \_ \_Unbekannter Status**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="799ea-113"><dt>**TASK\_STATE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="799ea-114">Der Task Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="799ea-114">The state of the task is unknown.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <span data-ttu-id="799ea-115"><dt>**Aufgabe \_ Status \_ deaktiviert**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="799ea-115"><dt>**TASK\_STATE\_DISABLED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="799ea-116">Der Task ist registriert, aber deaktiviert, und es werden keine Instanzen der Aufgabe in die Warteschlange eingereiht oder ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="799ea-116">The task is registered but is disabled and no instances of the task are queued or running.</span></span> <span data-ttu-id="799ea-117">Der Task kann erst ausgeführt werden, wenn er aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="799ea-117">The task cannot be run until it is enabled.</span></span><br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <span data-ttu-id="799ea-118"><dt>**Aufgabe \_ Status in \_ Warteschlange**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="799ea-118"><dt>**TASK\_STATE\_QUEUED**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="799ea-119">Instanzen der Aufgabe werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="799ea-119">Instances of the task are queued.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <span data-ttu-id="799ea-120"><dt>**Aufgabe \_ Status \_ bereit**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="799ea-120"><dt>**TASK\_STATE\_READY**</dt> <dt>3</dt></span></span> </dl>          | <span data-ttu-id="799ea-121">Der Task ist für die Ausführung bereit, aber es werden keine Instanzen in die Warteschlange eingereiht oder ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="799ea-121">The task is ready to be executed, but no instances are queued or running.</span></span><br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <span data-ttu-id="799ea-122"><dt>**Aufgabe \_ Status \_**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="799ea-122"><dt>**TASK\_STATE\_RUNNING**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="799ea-123">Eine oder mehrere Instanzen der Aufgabe werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="799ea-123">One or more instances of the task are running.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="799ea-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="799ea-124">Requirements</span></span>



| <span data-ttu-id="799ea-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="799ea-125">Requirement</span></span> | <span data-ttu-id="799ea-126">Wert</span><span class="sxs-lookup"><span data-stu-id="799ea-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="799ea-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="799ea-127">Minimum supported client</span></span><br/> | <span data-ttu-id="799ea-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="799ea-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="799ea-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="799ea-129">Minimum supported server</span></span><br/> | <span data-ttu-id="799ea-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="799ea-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="799ea-131">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="799ea-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="799ea-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="799ea-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="799ea-133">DLL</span><span class="sxs-lookup"><span data-stu-id="799ea-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="799ea-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="799ea-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="799ea-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="799ea-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="799ea-136">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="799ea-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="799ea-137">**Registeredtask**</span><span class="sxs-lookup"><span data-stu-id="799ea-137">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





