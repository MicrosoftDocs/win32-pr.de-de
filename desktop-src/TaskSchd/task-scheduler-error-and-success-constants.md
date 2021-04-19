---
title: Taskplaner Fehler-und Erfolgs Konstanten (Winerror. h)
description: Wenn ein Fehler auftritt, können die Taskplaner-APIs einen der folgenden Fehlercodes als HRESULT-Wert zurückgeben.
ms.assetid: 54278bbd-7dca-438e-a771-5fcb08c4aa68
keywords:
- Taskplaner Taskplaner-, Verweis-, Fehler-und Erfolgs Konstanten
topic_type:
- apiref
api_name:
- SCHED_S_TASK_READY
- SCHED_S_TASK_RUNNING
- SCHED_S_TASK_DISABLED
- SCHED_S_TASK_HAS_NOT_RUN
- SCHED_S_TASK_NO_MORE_RUNS
- SCHED_S_TASK_NOT_SCHEDULED
- SCHED_S_TASK_TERMINATED
- SCHED_S_TASK_NO_VALID_TRIGGERS
- SCHED_S_EVENT_TRIGGER
- SCHED_E_TRIGGER_NOT_FOUND
- SCHED_E_TASK_NOT_READY
- SCHED_E_TASK_NOT_RUNNING
- SCHED_E_SERVICE_NOT_INSTALLED
- SCHED_E_CANNOT_OPEN_TASK
- SCHED_E_INVALID_TASK
- SCHED_E_ACCOUNT_INFORMATION_NOT_SET
- SCHED_E_ACCOUNT_NAME_NOT_FOUND
- SCHED_E_ACCOUNT_DBASE_CORRUPT
- SCHED_E_NO_SECURITY_SERVICES
- SCHED_E_UNKNOWN_OBJECT_VERSION
- SCHED_E_UNSUPPORTED_ACCOUNT_OPTION
- SCHED_E_SERVICE_NOT_RUNNING
- SCHED_E_UNEXPECTEDNODE
- SCHED_E_NAMESPACE
- SCHED_E_INVALIDVALUE
- SCHED_E_MISSINGNODE
- SCHED_E_MALFORMEDXML
- SCHED_S_SOME_TRIGGERS_FAILED
- SCHED_S_BATCH_LOGON_PROBLEM
- SCHED_E_TOO_MANY_NODES
- SCHED_E_PAST_END_BOUNDARY
- SCHED_E_ALREADY_RUNNING
- SCHED_E_USER_NOT_LOGGED_ON
- SCHED_E_INVALID_TASK_HASH
- SCHED_E_SERVICE_NOT_AVAILABLE
- SCHED_E_SERVICE_TOO_BUSY
- SCHED_E_TASK_ATTEMPTED
- SCHED_S_TASK_QUEUED
- SCHED_E_TASK_DISABLED
- SCHED_E_TASK_NOT_V1_COMPAT
- SCHED_E_START_ON_DEMAND
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: a1d0347938020ca8937f2764e3b2c62a38fc9273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369571"
---
# <a name="task-scheduler-error-and-success-constants"></a><span data-ttu-id="6c829-104">Taskplaner Fehler-und Erfolgs Konstanten</span><span class="sxs-lookup"><span data-stu-id="6c829-104">Task Scheduler Error and Success Constants</span></span>

<span data-ttu-id="6c829-105">Wenn ein Fehler auftritt, können die Taskplaner-APIs einen der folgenden Fehlercodes als **HRESULT** -Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6c829-105">If an error occurs, the Task Scheduler APIs can return one of the following error codes as an **HRESULT** value.</span></span>

<span data-ttu-id="6c829-106">Die Konstanten, die mit "sched S" beginnen \_ \_ , sind Erfolgs Konstanten, und die Konstanten, die mit "sched E" beginnen, \_ \_ sind Fehler Konstanten.</span><span class="sxs-lookup"><span data-stu-id="6c829-106">The constants that begin with SCHED\_S\_ are success constants, and the constants that begin with SCHED\_E\_ are error constants.</span></span>

```cpp
  HRESULT phrStatus;
  hr = pITask->GetStatus(&phrStatus);
  
  // Release the ITask interface.
  pITask->Release();
    
  switch(phrStatus)
  {
  case SCHED_S_TASK_READY:
       wprintf(L"  SCHED_S_TASK_READY\n");
       break;
  case SCHED_S_TASK_RUNNING:
       wprintf(L"  SCHED_S_TASK_RUNNING\n");
       break;

  //...
  }
```

<span data-ttu-id="6c829-107">Beispiel aus [C/C++-Code Beispiel: Abrufen des Aufgaben Status](c-c-code-example-retrieving-task-status.md).</span><span class="sxs-lookup"><span data-stu-id="6c829-107">Example from [C/C++ Code Example: Retrieving Task Status](c-c-code-example-retrieving-task-status.md).</span></span>

> [!Note]  
> <span data-ttu-id="6c829-108">Einige Taskplaner APIs können System-und Netzwerkfehler Codes zurückgeben (z. b. 64).</span><span class="sxs-lookup"><span data-stu-id="6c829-108">Some Task Scheduler APIs can return system and network error codes (64 for example).</span></span> <span data-ttu-id="6c829-109">Sie können die Definition dieser Arten von Fehlercodes überprüfen, indem Sie den Befehl **net helpmsg** im Eingabe Aufforderungs Fenster verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c829-109">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="6c829-110">Der Befehl **net helpmsg 64** gibt beispielsweise die folgende Meldung zurück: der angegebene Netzwerkname ist nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c829-110">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

 

<span data-ttu-id="6c829-111">Weitere Informationen zu Ereignissen und Fehlermeldungen finden Sie unter [Events And Errors Message Center](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).</span><span class="sxs-lookup"><span data-stu-id="6c829-111">For more information about events and error messages, see [Events and Errors Message Center](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).</span></span>

<dl> <dt>

<span data-ttu-id="6c829-112"><span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**Aufgabe ist \_ \_ \_ abgeschlossen.**</span><span class="sxs-lookup"><span data-stu-id="6c829-112"><span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**SCHED\_S\_TASK\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-113">0x00041300</span><span class="sxs-lookup"><span data-stu-id="6c829-113">0x00041300</span></span>
</dt> <dt>



<span data-ttu-id="6c829-114">Der Task kann zum nächsten geplanten Zeitpunkt ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c829-114">The task is ready to run at its next scheduled time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-115"><span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**sched \_ S- \_ Aufgabe wird \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="6c829-115"><span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**SCHED\_S\_TASK\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-116">0x00041301</span><span class="sxs-lookup"><span data-stu-id="6c829-116">0x00041301</span></span>
</dt> <dt>



<span data-ttu-id="6c829-117">Die Aufgabe wird gerade ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c829-117">The task is currently running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-118"><span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**sched \_ S \_ Aufgabe \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="6c829-118"><span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**SCHED\_S\_TASK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-119">0x00041302</span><span class="sxs-lookup"><span data-stu-id="6c829-119">0x00041302</span></span>
</dt> <dt>



<span data-ttu-id="6c829-120">Der Task wird nicht zu den geplanten Zeiten ausgeführt, weil er deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="6c829-120">The task will not run at the scheduled times because it has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-121"><span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**der Task "sched \_ S" \_ \_ wurde \_ nicht \_ ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="6c829-121"><span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**SCHED\_S\_TASK\_HAS\_NOT\_RUN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-122">0x00041303</span><span class="sxs-lookup"><span data-stu-id="6c829-122">0x00041303</span></span>
</dt> <dt>



<span data-ttu-id="6c829-123">Der Task wurde noch nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c829-123">The task has not yet run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-124"><span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**der Task "sched S" wird \_ \_ \_ nicht \_ mehr \_ ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="6c829-124"><span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**SCHED\_S\_TASK\_NO\_MORE\_RUNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-125">0x00041304</span><span class="sxs-lookup"><span data-stu-id="6c829-125">0x00041304</span></span>
</dt> <dt>



<span data-ttu-id="6c829-126">Es sind keine weiteren Ausführungen für diese Aufgabe geplant.</span><span class="sxs-lookup"><span data-stu-id="6c829-126">There are no more runs scheduled for this task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-127"><span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**sched \_ S \_ Aufgabe \_ nicht \_ geplant**</span><span class="sxs-lookup"><span data-stu-id="6c829-127"><span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**SCHED\_S\_TASK\_NOT\_SCHEDULED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-128">0x00041305</span><span class="sxs-lookup"><span data-stu-id="6c829-128">0x00041305</span></span>
</dt> <dt>



<span data-ttu-id="6c829-129">Mindestens eine der Eigenschaften, die zum Ausführen dieser Aufgabe nach einem Zeitplan benötigt werden, wurde nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6c829-129">One or more of the properties that are needed to run this task on a schedule have not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-130"><span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**sched \_ S \_ Aufgabe wurde \_ beendet.**</span><span class="sxs-lookup"><span data-stu-id="6c829-130"><span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**SCHED\_S\_TASK\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-131">0x00041306</span><span class="sxs-lookup"><span data-stu-id="6c829-131">0x00041306</span></span>
</dt> <dt>



<span data-ttu-id="6c829-132">Die letzte Ausführungsdauer der Aufgabe wurde vom Benutzer beendet.</span><span class="sxs-lookup"><span data-stu-id="6c829-132">The last run of the task was terminated by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-133"><span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**sched \_ S- \_ Aufgabe \_ keine \_ gültigen \_ Trigger**</span><span class="sxs-lookup"><span data-stu-id="6c829-133"><span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**SCHED\_S\_TASK\_NO\_VALID\_TRIGGERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-134">0x00041307</span><span class="sxs-lookup"><span data-stu-id="6c829-134">0x00041307</span></span>
</dt> <dt>



<span data-ttu-id="6c829-135">Entweder hat der Task keine Trigger, oder die vorhandenen Trigger sind deaktiviert oder nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6c829-135">Either the task has no triggers or the existing triggers are disabled or not set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-136"><span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**sched \_ S- \_ Ereignis \_ auslöst**</span><span class="sxs-lookup"><span data-stu-id="6c829-136"><span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**SCHED\_S\_EVENT\_TRIGGER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-137">0x00041308</span><span class="sxs-lookup"><span data-stu-id="6c829-137">0x00041308</span></span>
</dt> <dt>



<span data-ttu-id="6c829-138">Ereignis Trigger haben keine festgelegten Laufzeiten.</span><span class="sxs-lookup"><span data-stu-id="6c829-138">Event triggers do not have set run times.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-139"><span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**sched E-Auslösung \_ \_ \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="6c829-139"><span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**SCHED\_E\_TRIGGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-140">0x80041309</span><span class="sxs-lookup"><span data-stu-id="6c829-140">0x80041309</span></span>
</dt> <dt>



<span data-ttu-id="6c829-141">Der auslösertyp einer Aufgabe wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6c829-141">A task's trigger is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-142"><span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**sched \_ E- \_ Aufgabe \_ nicht \_ bereit**</span><span class="sxs-lookup"><span data-stu-id="6c829-142"><span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**SCHED\_E\_TASK\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-143">0x8004130a</span><span class="sxs-lookup"><span data-stu-id="6c829-143">0x8004130A</span></span>
</dt> <dt>



<span data-ttu-id="6c829-144">Mindestens eine der zum Ausführen dieser Aufgabe erforderlichen Eigenschaften wurde nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6c829-144">One or more of the properties required to run this task have not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-145"><span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**sched \_ E- \_ Aufgabe wird \_ nicht \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="6c829-145"><span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**SCHED\_E\_TASK\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-146">0x8004130b</span><span class="sxs-lookup"><span data-stu-id="6c829-146">0x8004130B</span></span>
</dt> <dt>



<span data-ttu-id="6c829-147">Es ist keine laufende Instanz der Aufgabe vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c829-147">There is no running instance of the task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-148"><span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**sched \_ E- \_ Dienst \_ nicht \_ installiert**</span><span class="sxs-lookup"><span data-stu-id="6c829-148"><span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**SCHED\_E\_SERVICE\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-149">0x8004130c</span><span class="sxs-lookup"><span data-stu-id="6c829-149">0x8004130C</span></span>
</dt> <dt>



<span data-ttu-id="6c829-150">Der Taskplaner-Dienst ist auf diesem Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="6c829-150">The Task Scheduler service is not installed on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-151"><span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**sched \_ E \_ kann \_ Aufgabe nicht öffnen \_**</span><span class="sxs-lookup"><span data-stu-id="6c829-151"><span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**SCHED\_E\_CANNOT\_OPEN\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-152">0x8004130d</span><span class="sxs-lookup"><span data-stu-id="6c829-152">0x8004130D</span></span>
</dt> <dt>



<span data-ttu-id="6c829-153">Das Task Objekt konnte nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="6c829-153">The task object could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-154"><span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**sched \_ E \_ ungültige \_ Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="6c829-154"><span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**SCHED\_E\_INVALID\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-155">0x8004130e</span><span class="sxs-lookup"><span data-stu-id="6c829-155">0x8004130E</span></span>
</dt> <dt>



<span data-ttu-id="6c829-156">Das-Objekt ist entweder ein ungültiges Task Objekt oder kein Task Objekt.</span><span class="sxs-lookup"><span data-stu-id="6c829-156">The object is either an invalid task object or is not a task object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-157"><span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**die sched \_ E- \_ Konto \_ Informationen \_ \_ wurden nicht festgelegt.**</span><span class="sxs-lookup"><span data-stu-id="6c829-157"><span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**SCHED\_E\_ACCOUNT\_INFORMATION\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-158">0x8004130f</span><span class="sxs-lookup"><span data-stu-id="6c829-158">0x8004130F</span></span>
</dt> <dt>



<span data-ttu-id="6c829-159">In der Taskplaner-Sicherheitsdatenbank wurden keine Kontoinformationen für die jeweilige Aufgabe gefunden.</span><span class="sxs-lookup"><span data-stu-id="6c829-159">No account information could be found in the Task Scheduler security database for the task indicated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-160"><span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**der sched \_ E- \_ \_ Kontoname wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6c829-160"><span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**SCHED\_E\_ACCOUNT\_NAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-161">0x80041310</span><span class="sxs-lookup"><span data-stu-id="6c829-161">0x80041310</span></span>
</dt> <dt>



<span data-ttu-id="6c829-162">Das vorhanden sein des angegebenen Kontos kann nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6c829-162">Unable to establish existence of the account specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-163"><span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**sched \_ E \_ Account \_ dBASE \_ beschädigt**</span><span class="sxs-lookup"><span data-stu-id="6c829-163"><span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**SCHED\_E\_ACCOUNT\_DBASE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-164">0x80041311</span><span class="sxs-lookup"><span data-stu-id="6c829-164">0x80041311</span></span>
</dt> <dt>



<span data-ttu-id="6c829-165">In der Taskplaner-Sicherheitsdatenbank wurde eine Beschädigung festgestellt. die Datenbank wurde zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="6c829-165">Corruption was detected in the Task Scheduler security database; the database has been reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-166"><span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**sched \_ E \_ No \_ Security \_ Services**</span><span class="sxs-lookup"><span data-stu-id="6c829-166"><span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHED\_E\_NO\_SECURITY\_SERVICES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-167">0x80041312</span><span class="sxs-lookup"><span data-stu-id="6c829-167">0x80041312</span></span>
</dt> <dt>



<span data-ttu-id="6c829-168">Taskplaner Sicherheitsdienste sind nur unter Windows NT verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c829-168">Task Scheduler security services are available only on Windows NT.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-169"><span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**sched \_ E \_ unbekannte \_ Objekt \_ Version**</span><span class="sxs-lookup"><span data-stu-id="6c829-169"><span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**SCHED\_E\_UNKNOWN\_OBJECT\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-170">0x80041313</span><span class="sxs-lookup"><span data-stu-id="6c829-170">0x80041313</span></span>
</dt> <dt>



<span data-ttu-id="6c829-171">Die Task Objekt Version wird entweder nicht unterstützt oder ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c829-171">The task object version is either unsupported or invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-172"><span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**sched \_ E \_ nicht unterstützte \_ Konto \_ Option**</span><span class="sxs-lookup"><span data-stu-id="6c829-172"><span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**SCHED\_E\_UNSUPPORTED\_ACCOUNT\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-173">0x80041314</span><span class="sxs-lookup"><span data-stu-id="6c829-173">0x80041314</span></span>
</dt> <dt>



<span data-ttu-id="6c829-174">Der Task wurde mit einer nicht unterstützten Kombination aus Kontoeinstellungen und Laufzeitoptionen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6c829-174">The task has been configured with an unsupported combination of account settings and run time options.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-175"><span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**sched \_ E- \_ Dienst wird \_ nicht \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="6c829-175"><span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**SCHED\_E\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-176">0x80041315</span><span class="sxs-lookup"><span data-stu-id="6c829-176">0x80041315</span></span>
</dt> <dt>



<span data-ttu-id="6c829-177">Der Taskplaner-Dienst wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c829-177">The Task Scheduler Service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-178"><span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**sched \_ E \_ unexpectednode**</span><span class="sxs-lookup"><span data-stu-id="6c829-178"><span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**SCHED\_E\_UNEXPECTEDNODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-179">0x80041316</span><span class="sxs-lookup"><span data-stu-id="6c829-179">0x80041316</span></span>
</dt> <dt>



<span data-ttu-id="6c829-180">Die Task-XML-Datei enthält einen unerwarteten Knoten.</span><span class="sxs-lookup"><span data-stu-id="6c829-180">The task XML contains an unexpected node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-181"><span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**sched \_ E- \_ Namespace**</span><span class="sxs-lookup"><span data-stu-id="6c829-181"><span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**SCHED\_E\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-182">0x80041317</span><span class="sxs-lookup"><span data-stu-id="6c829-182">0x80041317</span></span>
</dt> <dt>



<span data-ttu-id="6c829-183">Die Task-XML-Datei enthält ein Element oder Attribut aus einem unerwarteten Namespace.</span><span class="sxs-lookup"><span data-stu-id="6c829-183">The task XML contains an element or attribute from an unexpected namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-184"><span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**sched \_ E \_ invalidvalue**</span><span class="sxs-lookup"><span data-stu-id="6c829-184"><span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**SCHED\_E\_INVALIDVALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-185">0x80041318</span><span class="sxs-lookup"><span data-stu-id="6c829-185">0x80041318</span></span>
</dt> <dt>



<span data-ttu-id="6c829-186">Die Task-XML-Datei enthält einen Wert, der falsch formatiert oder außerhalb des gültigen Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="6c829-186">The task XML contains a value which is incorrectly formatted or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-187"><span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**sched \_ E \_ missingnode**</span><span class="sxs-lookup"><span data-stu-id="6c829-187"><span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**SCHED\_E\_MISSINGNODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-188">0x80041319</span><span class="sxs-lookup"><span data-stu-id="6c829-188">0x80041319</span></span>
</dt> <dt>



<span data-ttu-id="6c829-189">In der XML-Aufgabe fehlt ein erforderliches Element oder Attribut.</span><span class="sxs-lookup"><span data-stu-id="6c829-189">The task XML is missing a required element or attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-190"><span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**sched \_ E \_ malformedxml**</span><span class="sxs-lookup"><span data-stu-id="6c829-190"><span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**SCHED\_E\_MALFORMEDXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-191">0x8004131a</span><span class="sxs-lookup"><span data-stu-id="6c829-191">0x8004131A</span></span>
</dt> <dt>



<span data-ttu-id="6c829-192">Die Task-XML-Datei ist falsch formatiert.</span><span class="sxs-lookup"><span data-stu-id="6c829-192">The task XML is malformed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-193"><span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**Fehler beim \_ \_ auslösen einiger \_ Trigger \_**</span><span class="sxs-lookup"><span data-stu-id="6c829-193"><span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**SCHED\_S\_SOME\_TRIGGERS\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-194">0x0004131b</span><span class="sxs-lookup"><span data-stu-id="6c829-194">0x0004131B</span></span>
</dt> <dt>



<span data-ttu-id="6c829-195">Der Task wird registriert, aber nicht alle angegebenen Trigger starten den Task.</span><span class="sxs-lookup"><span data-stu-id="6c829-195">The task is registered, but not all specified triggers will start the task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-196"><span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**sched \_ S-Problem bei der \_ Batch \_ Anmeldung \_**</span><span class="sxs-lookup"><span data-stu-id="6c829-196"><span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**SCHED\_S\_BATCH\_LOGON\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-197">0x0004131c</span><span class="sxs-lookup"><span data-stu-id="6c829-197">0x0004131C</span></span>
</dt> <dt>



<span data-ttu-id="6c829-198">Der Task ist registriert, kann jedoch möglicherweise nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6c829-198">The task is registered, but may fail to start.</span></span> <span data-ttu-id="6c829-199">Die Batch Anmelde Berechtigung muss für den Task Prinzipal aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="6c829-199">Batch logon privilege needs to be enabled for the task principal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-200"><span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**sched \_ E \_ zu \_ viele \_ Knoten**</span><span class="sxs-lookup"><span data-stu-id="6c829-200"><span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**SCHED\_E\_TOO\_MANY\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-201">0x8004131d</span><span class="sxs-lookup"><span data-stu-id="6c829-201">0x8004131D</span></span>
</dt> <dt>



<span data-ttu-id="6c829-202">Die Task-XML-Datei enthält zu viele Knoten desselben Typs.</span><span class="sxs-lookup"><span data-stu-id="6c829-202">The task XML contains too many nodes of the same type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-203"><span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**sched \_ E \_ nach \_ Ende \_ Grenze**</span><span class="sxs-lookup"><span data-stu-id="6c829-203"><span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**SCHED\_E\_PAST\_END\_BOUNDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-204">0x8004131e</span><span class="sxs-lookup"><span data-stu-id="6c829-204">0x8004131E</span></span>
</dt> <dt>



<span data-ttu-id="6c829-205">Der Task kann nicht nach der Endpunkt Grenze des Auslösers gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6c829-205">The task cannot be started after the trigger end boundary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-206"><span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**sched \_ E wird \_ bereits \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="6c829-206"><span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHED\_E\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-207">0x8004131f</span><span class="sxs-lookup"><span data-stu-id="6c829-207">0x8004131F</span></span>
</dt> <dt>



<span data-ttu-id="6c829-208">Eine Instanz dieser Aufgabe wird bereits ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c829-208">An instance of this task is already running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-209"><span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**sched \_ E \_ Benutzer \_ nicht \_ angemeldet \_**</span><span class="sxs-lookup"><span data-stu-id="6c829-209"><span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**SCHED\_E\_USER\_NOT\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-210">0x80041320</span><span class="sxs-lookup"><span data-stu-id="6c829-210">0x80041320</span></span>
</dt> <dt>



<span data-ttu-id="6c829-211">Der Task wird nicht ausgeführt, da der Benutzer nicht angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="6c829-211">The task will not run because the user is not logged on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-212"><span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**sched \_ E \_ ungültiger \_ \_ taskhash**</span><span class="sxs-lookup"><span data-stu-id="6c829-212"><span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**SCHED\_E\_INVALID\_TASK\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-213">0x80041321</span><span class="sxs-lookup"><span data-stu-id="6c829-213">0x80041321</span></span>
</dt> <dt>



<span data-ttu-id="6c829-214">Das Aufgaben Image ist beschädigt oder wurde manipuliert.</span><span class="sxs-lookup"><span data-stu-id="6c829-214">The task image is corrupt or has been tampered with.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-215"><span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**sched \_ E- \_ Dienst \_ nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="6c829-215"><span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**SCHED\_E\_SERVICE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-216">0x80041322</span><span class="sxs-lookup"><span data-stu-id="6c829-216">0x80041322</span></span>
</dt> <dt>



<span data-ttu-id="6c829-217">Der Taskplaner-Dienst ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c829-217">The Task Scheduler service is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-218"><span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**sched \_ E- \_ Dienst \_ zu \_ stark ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="6c829-218"><span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**SCHED\_E\_SERVICE\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-219">0x80041323</span><span class="sxs-lookup"><span data-stu-id="6c829-219">0x80041323</span></span>
</dt> <dt>



<span data-ttu-id="6c829-220">Der Taskplaner-Dienst ist zu stark ausgelastet, um Ihre Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6c829-220">The Task Scheduler service is too busy to handle your request.</span></span> <span data-ttu-id="6c829-221">Versuchen Sie es später noch mal.</span><span class="sxs-lookup"><span data-stu-id="6c829-221">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-222"><span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**sched \_ E- \_ Aufgabe \_ versucht**</span><span class="sxs-lookup"><span data-stu-id="6c829-222"><span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**SCHED\_E\_TASK\_ATTEMPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-223">0x80041324</span><span class="sxs-lookup"><span data-stu-id="6c829-223">0x80041324</span></span>
</dt> <dt>



<span data-ttu-id="6c829-224">Der Taskplaner Dienst hat versucht, die Aufgabe auszuführen, aber die Aufgabe wurde aufgrund einer der Einschränkungen in der Aufgabendefinition nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c829-224">The Task Scheduler service attempted to run the task, but the task did not run due to one of the constraints in the task definition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-225"><span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**sched \_ S \_ Task in \_ Warteschlange eingereiht**</span><span class="sxs-lookup"><span data-stu-id="6c829-225"><span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**SCHED\_S\_TASK\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-226">0x00041325</span><span class="sxs-lookup"><span data-stu-id="6c829-226">0x00041325</span></span>
</dt> <dt>



<span data-ttu-id="6c829-227">Der Taskplaner-Dienst hat die Aufgabe zur Durchführung der Aufgabe aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="6c829-227">The Task Scheduler service has asked the task to run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-228"><span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**sched \_ E- \_ Aufgabe \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="6c829-228"><span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**SCHED\_E\_TASK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-229">0x80041326</span><span class="sxs-lookup"><span data-stu-id="6c829-229">0x80041326</span></span>
</dt> <dt>



<span data-ttu-id="6c829-230">Der Task ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6c829-230">The task is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-231"><span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**Sched \_ E \_ Task \_ nicht \_ v1- \_ Kompatibilität**</span><span class="sxs-lookup"><span data-stu-id="6c829-231"><span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**SCHED\_E\_TASK\_NOT\_V1\_COMPAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-232">0x80041327</span><span class="sxs-lookup"><span data-stu-id="6c829-232">0x80041327</span></span>
</dt> <dt>



<span data-ttu-id="6c829-233">Der Task verfügt über Eigenschaften, die mit früheren Versionen von Windows nicht kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="6c829-233">The task has properties that are not compatible with earlier versions of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c829-234"><span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**sched \_ E \_ \_ bei \_ Bedarf starten**</span><span class="sxs-lookup"><span data-stu-id="6c829-234"><span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**SCHED\_E\_START\_ON\_DEMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c829-235">0x80041328</span><span class="sxs-lookup"><span data-stu-id="6c829-235">0x80041328</span></span>
</dt> <dt>



<span data-ttu-id="6c829-236">Mit den Task Einstellungen kann die Aufgabe nicht bei Bedarf gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6c829-236">The task settings do not allow the task to start on demand.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c829-237">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c829-237">Requirements</span></span>



| <span data-ttu-id="6c829-238">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c829-238">Requirement</span></span> | <span data-ttu-id="6c829-239">Wert</span><span class="sxs-lookup"><span data-stu-id="6c829-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c829-240">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c829-240">Minimum supported client</span></span><br/> | <span data-ttu-id="6c829-241">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c829-241">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c829-242">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c829-242">Minimum supported server</span></span><br/> | <span data-ttu-id="6c829-243">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c829-243">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c829-244">Header</span><span class="sxs-lookup"><span data-stu-id="6c829-244">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c829-245"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c829-245"><dt>WinError.h</dt></span></span> </dl> |



 

 





