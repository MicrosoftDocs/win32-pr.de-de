---
title: TriggerCollection. Create-Methode
description: Erstellt bei der Skripterstellung einen neuen---------
ms.assetid: 3d7dc811-0d83-475f-8a6e-87e59dae0113
keywords:
- Trigger Taskplaner, erstellen
- Create-Methode Taskplaner
- Create Method-Taskplaner, TriggerCollection-Objekt
- TriggerCollection-Objekt Taskplaner, Create-Methode
topic_type:
- apiref
api_name:
- TriggerCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0f1c5dd8bef3d81a8e9b5859bc2bbd8c969bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339138"
---
# <a name="triggercollectioncreate-method"></a><span data-ttu-id="30757-107">TriggerCollection. Create-Methode</span><span class="sxs-lookup"><span data-stu-id="30757-107">TriggerCollection.Create method</span></span>

<span data-ttu-id="30757-108">Erstellt bei der Skripterstellung einen neuen---------</span><span class="sxs-lookup"><span data-stu-id="30757-108">For scripting, creates a new trigger for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="30757-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="30757-109">Syntax</span></span>


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a><span data-ttu-id="30757-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="30757-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30757-111">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30757-111">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30757-112">Dieser Parameter ist auf einen der folgenden [**Aufgaben \_ Auslösers \_**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) festgelegt Typ2 Enumerationskonstanten.</span><span class="sxs-lookup"><span data-stu-id="30757-112">This parameter is set to one of the following [**TASK\_TRIGGER\_TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) enumeration constants.</span></span>



| <span data-ttu-id="30757-113">Wert</span><span class="sxs-lookup"><span data-stu-id="30757-113">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="30757-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="30757-114">Meaning</span></span>                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <span data-ttu-id="30757-115"><dt>**Aufgabe \_ Auslöse \_ Ereignis**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="30757-115"><dt>**TASK\_TRIGGER\_EVENT**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="30757-116">Löst die Aufgabe aus, wenn ein bestimmtes Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="30757-116">Triggers the task when a specific event occurs.</span></span><br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <span data-ttu-id="30757-117"><dt>**Aufgabe \_ Auslöse \_ Zeit**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="30757-117"><dt>**TASK\_TRIGGER\_TIME**</dt> <dt>1</dt></span></span> </dl>                                                    | <span data-ttu-id="30757-118">Löst den Task zu einem bestimmten Zeitpunkt aus.</span><span class="sxs-lookup"><span data-stu-id="30757-118">Triggers the task at a specific time of day.</span></span><br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <span data-ttu-id="30757-119"><dt>**Aufgabe \_ Auslösung \_ täglich**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="30757-119"><dt>**TASK\_TRIGGER\_DAILY**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="30757-120">Löst die Aufgabe nach einem täglichen Zeitplan aus.</span><span class="sxs-lookup"><span data-stu-id="30757-120">Triggers the task on a daily schedule.</span></span> <span data-ttu-id="30757-121">Der Task wird z. b. jeden Tag, jeden Tag, jeden dritten Tag und so weiter zu einem bestimmten Zeitpunkt gestartet.</span><span class="sxs-lookup"><span data-stu-id="30757-121">For example, the task starts at a specific time every day, every-other day, every third day, and so on.</span></span><br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <span data-ttu-id="30757-122"><dt>**Aufgabe \_ Auslösung \_ wöchentlich**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="30757-122"><dt>**TASK\_TRIGGER\_WEEKLY**</dt> <dt>3</dt></span></span> </dl>                                              | <span data-ttu-id="30757-123">Löst die Aufgabe nach einem wöchentlichen Zeitplan aus.</span><span class="sxs-lookup"><span data-stu-id="30757-123">Triggers the task on a weekly schedule.</span></span> <span data-ttu-id="30757-124">Der Task wird z. b. wöchentlich um 8:00 Uhr an einem bestimmten Tag gestartet.</span><span class="sxs-lookup"><span data-stu-id="30757-124">For example, the task starts at 8:00 AM on a specific day every week or other week.</span></span><br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <span data-ttu-id="30757-125"><dt>**Aufgabe \_ Auslösung \_ monatlich**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="30757-125"><dt>**TASK\_TRIGGER\_MONTHLY**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="30757-126">Löst die Aufgabe nach einem monatlichen Zeitplan aus.</span><span class="sxs-lookup"><span data-stu-id="30757-126">Triggers the task on a monthly schedule.</span></span> <span data-ttu-id="30757-127">Beispielsweise wird die Aufgabe an bestimmten Tagen eines bestimmten Monats gestartet.</span><span class="sxs-lookup"><span data-stu-id="30757-127">For example, the task starts on specific days of specific months.</span></span><br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <span data-ttu-id="30757-128"><dt>**Aufgabe \_ \_Monthlydow**</dt> <dt>5</dt> -Ereignis</span><span class="sxs-lookup"><span data-stu-id="30757-128"><dt>**TASK\_TRIGGER\_MONTHLYDOW**</dt> <dt>5</dt></span></span> </dl>                                  | <span data-ttu-id="30757-129">Löst die Aufgabe an einem monatlichen Wochentag aus.</span><span class="sxs-lookup"><span data-stu-id="30757-129">Triggers the task on a monthly day-of-week schedule.</span></span> <span data-ttu-id="30757-130">Beispielsweise wird die Aufgabe an einem bestimmten Tag der Woche, Wochen des Monats und Monaten des Jahres gestartet.</span><span class="sxs-lookup"><span data-stu-id="30757-130">For example, the task starts on a specific days of the week, weeks of the month, and months of the year.</span></span><br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <span data-ttu-id="30757-131"><dt>**Aufgabe \_ Auslöse \_ Leerlauf**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="30757-131"><dt>**TASK\_TRIGGER\_IDLE**</dt> <dt>6</dt></span></span> </dl>                                                    | <span data-ttu-id="30757-132">Löst die Aufgabe aus, wenn der Computer in den Leerlauf wechselt.</span><span class="sxs-lookup"><span data-stu-id="30757-132">Triggers the task when the computer goes into an idle state.</span></span><br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <span data-ttu-id="30757-133"><dt>**Aufgabe \_ \_Registrierungs Registrierungs**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="30757-133"><dt>**TASK\_TRIGGER\_REGISTRATION**</dt> <dt>7</dt></span></span> </dl>                            | <span data-ttu-id="30757-134">Löst die Aufgabe aus, wenn die Aufgabe registriert wird.</span><span class="sxs-lookup"><span data-stu-id="30757-134">Triggers the task when the task is registered.</span></span><br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <span data-ttu-id="30757-135"><dt>**Aufgabe \_ \_Starten von Start**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="30757-135"><dt>**TASK\_TRIGGER\_BOOT**</dt> <dt>8</dt></span></span> </dl>                                                    | <span data-ttu-id="30757-136">Löst die Aufgabe aus, wenn der Computer gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="30757-136">Triggers the task when the computer boots.</span></span><br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <span data-ttu-id="30757-137"><dt>**Aufgabe \_ \_Logon-Anmeldung**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="30757-137"><dt>**TASK\_TRIGGER\_LOGON**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="30757-138">Löst die Aufgabe aus, wenn sich ein bestimmter Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="30757-138">Triggers the task when a specific user logs on.</span></span><br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <span data-ttu-id="30757-139"><dt>**Aufgabe \_ \_Änderung der Sitzungs \_ Status \_ Änderung**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="30757-139"><dt>**TASK\_TRIGGER\_SESSION\_STATE\_CHANGE**</dt> <dt>11</dt></span></span> </dl> | <span data-ttu-id="30757-140">Löst die Aufgabe aus, wenn sich ein bestimmter Sitzungszustand ändert.</span><span class="sxs-lookup"><span data-stu-id="30757-140">Triggers the task when a specific session state changes.</span></span><br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30757-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30757-141">Return value</span></span>

<span data-ttu-id="30757-142">Ein- [**Auslöserobjekt**](trigger.md) , das den neuen-Typ darstellt.</span><span class="sxs-lookup"><span data-stu-id="30757-142">A [**Trigger**](trigger.md) object that represents the new trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="30757-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30757-143">Remarks</span></span>

<span data-ttu-id="30757-144">Informationen zu den einzelnen Auslösertypen finden Sie unter [Auslösertypen](trigger-types.md)</span><span class="sxs-lookup"><span data-stu-id="30757-144">For information about each trigger type see [Trigger Types](trigger-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30757-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30757-145">Requirements</span></span>



| <span data-ttu-id="30757-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30757-146">Requirement</span></span> | <span data-ttu-id="30757-147">Wert</span><span class="sxs-lookup"><span data-stu-id="30757-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30757-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30757-148">Minimum supported client</span></span><br/> | <span data-ttu-id="30757-149">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30757-149">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="30757-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30757-150">Minimum supported server</span></span><br/> | <span data-ttu-id="30757-151">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30757-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30757-152">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="30757-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="30757-153"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="30757-153"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="30757-154">DLL</span><span class="sxs-lookup"><span data-stu-id="30757-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30757-155"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30757-155"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30757-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30757-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30757-157">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="30757-157">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="30757-158">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="30757-158">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





