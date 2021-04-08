---
title: "\". Type\"-Eigenschaft"
description: Ruft bei der Skripterstellung den Typ des Auslösers ab.
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Type-Eigenschafts Taskplaner
- Type-Eigenschafts Taskplaner, Auslöserobjekt
- Auslöse Objekt Taskplaner, Typeigenschaft
topic_type:
- apiref
api_name:
- Trigger.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2cef2d6ae33ceeac028e10a0f545afbc0a0ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740792"
---
# <a name="triggertype-property"></a><span data-ttu-id="36523-106">". Type"-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="36523-106">Trigger.Type property</span></span>

<span data-ttu-id="36523-107">Ruft bei der Skripterstellung den Typ des Auslösers ab.</span><span class="sxs-lookup"><span data-stu-id="36523-107">For scripting, gets the type of the trigger.</span></span> <span data-ttu-id="36523-108">Der auslösertyp wird beim Erstellen des Auslösers definiert und kann später nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="36523-108">The trigger type is defined when the trigger is created and cannot be changed later.</span></span> <span data-ttu-id="36523-109">Weitere Informationen zum Erstellen eines Auslösers finden Sie unter [**TriggerCollection. Create**](triggercollection-create.md).</span><span class="sxs-lookup"><span data-stu-id="36523-109">For information on creating a trigger, see [**TriggerCollection.Create**](triggercollection-create.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="36523-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="36523-110">Syntax</span></span>


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a><span data-ttu-id="36523-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="36523-111">Property value</span></span>

<span data-ttu-id="36523-112">Einer der folgenden [**Aufgaben \_ löst \_ Typ2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) Enumerationswerte aus.</span><span class="sxs-lookup"><span data-stu-id="36523-112">One of the following [**TASK\_TRIGGER\_TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) enumeration values.</span></span>



| <span data-ttu-id="36523-113">Wert</span><span class="sxs-lookup"><span data-stu-id="36523-113">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="36523-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="36523-114">Meaning</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <span data-ttu-id="36523-115"><dt>**Aufgabe \_ Auslöse \_ Ereignis**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="36523-115"><dt>**TASK\_TRIGGER\_EVENT**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="36523-116">Startet die Aufgabe, wenn ein bestimmtes Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="36523-116">Starts the task when a specific event occurs.</span></span><br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <span data-ttu-id="36523-117"><dt>**Aufgabe \_ Auslöse \_ Zeit**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="36523-117"><dt>**TASK\_TRIGGER\_TIME**</dt> <dt>1</dt></span></span> </dl>                                                    | <span data-ttu-id="36523-118">Startet die Aufgabe zu einem bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="36523-118">Starts the task at a specific time of day.</span></span><br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <span data-ttu-id="36523-119"><dt>**Aufgabe \_ Auslösung \_ täglich**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="36523-119"><dt>**TASK\_TRIGGER\_DAILY**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="36523-120">Startet die Aufgabe täglich.</span><span class="sxs-lookup"><span data-stu-id="36523-120">Starts the task daily.</span></span><br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <span data-ttu-id="36523-121"><dt>**Aufgabe \_ Auslösung \_ wöchentlich**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="36523-121"><dt>**TASK\_TRIGGER\_WEEKLY**</dt> <dt>3</dt></span></span> </dl>                                              | <span data-ttu-id="36523-122">Startet die Aufgabe wöchentlich.</span><span class="sxs-lookup"><span data-stu-id="36523-122">Starts the task weekly.</span></span><br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <span data-ttu-id="36523-123"><dt>**Aufgabe \_ Auslösung \_ monatlich**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="36523-123"><dt>**TASK\_TRIGGER\_MONTHLY**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="36523-124">Startet die Aufgabe monatlich.</span><span class="sxs-lookup"><span data-stu-id="36523-124">Starts the task monthly.</span></span><br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <span data-ttu-id="36523-125"><dt>**Aufgabe \_ \_Monthlydow**</dt> <dt>5</dt> -Ereignis</span><span class="sxs-lookup"><span data-stu-id="36523-125"><dt>**TASK\_TRIGGER\_MONTHLYDOW**</dt> <dt>5</dt></span></span> </dl>                                  | <span data-ttu-id="36523-126">Startet die Aufgabe monatlich an einem bestimmten Tag der Woche.</span><span class="sxs-lookup"><span data-stu-id="36523-126">Starts the task every month on a specific day of the week.</span></span><br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <span data-ttu-id="36523-127"><dt>**Aufgabe \_ Auslöse \_ Leerlauf**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="36523-127"><dt>**TASK\_TRIGGER\_IDLE**</dt> <dt>6</dt></span></span> </dl>                                                    | <span data-ttu-id="36523-128">Startet den Task, wenn der Computer in den Leerlauf wechselt.</span><span class="sxs-lookup"><span data-stu-id="36523-128">Starts the task when the computer goes into an idle state.</span></span><br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <span data-ttu-id="36523-129"><dt>**Aufgabe \_ \_Registrierungs Registrierungs**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="36523-129"><dt>**TASK\_TRIGGER\_REGISTRATION**</dt> <dt>7</dt></span></span> </dl>                            | <span data-ttu-id="36523-130">Startet die Aufgabe, wenn die Aufgabe registriert wird.</span><span class="sxs-lookup"><span data-stu-id="36523-130">Starts the task when the task is registered.</span></span><br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <span data-ttu-id="36523-131"><dt>**Aufgabe \_ \_Starten von Start**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="36523-131"><dt>**TASK\_TRIGGER\_BOOT**</dt> <dt>8</dt></span></span> </dl>                                                    | <span data-ttu-id="36523-132">Startet die Aufgabe, wenn der Computer startet.</span><span class="sxs-lookup"><span data-stu-id="36523-132">Starts the task when the computer boots.</span></span><br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <span data-ttu-id="36523-133"><dt>**Aufgabe \_ \_Logon-Anmeldung**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="36523-133"><dt>**TASK\_TRIGGER\_LOGON**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="36523-134">Startet die Aufgabe, wenn sich ein bestimmter Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="36523-134">Starts the task when a specific user logs on.</span></span><br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <span data-ttu-id="36523-135"><dt>**Aufgabe \_ \_Änderung der Sitzungs \_ Status \_ Änderung**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="36523-135"><dt>**TASK\_TRIGGER\_SESSION\_STATE\_CHANGE**</dt> <dt>11</dt></span></span> </dl> | <span data-ttu-id="36523-136">Löst die Aufgabe aus, wenn sich ein bestimmter Sitzungszustand ändert.</span><span class="sxs-lookup"><span data-stu-id="36523-136">Triggers the task when a specific session state changes.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="36523-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36523-137">Requirements</span></span>



| <span data-ttu-id="36523-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36523-138">Requirement</span></span> | <span data-ttu-id="36523-139">Wert</span><span class="sxs-lookup"><span data-stu-id="36523-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36523-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36523-140">Minimum supported client</span></span><br/> | <span data-ttu-id="36523-141">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36523-141">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="36523-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36523-142">Minimum supported server</span></span><br/> | <span data-ttu-id="36523-143">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36523-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="36523-144">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="36523-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="36523-145"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="36523-145"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="36523-146">DLL</span><span class="sxs-lookup"><span data-stu-id="36523-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36523-147"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36523-147"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36523-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36523-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36523-149">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="36523-149">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> <dt>

[<span data-ttu-id="36523-150">**Task \_ - \_ Typ2**</span><span class="sxs-lookup"><span data-stu-id="36523-150">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[<span data-ttu-id="36523-151">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="36523-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





