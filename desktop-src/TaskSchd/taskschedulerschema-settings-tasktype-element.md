---
title: Settings (TaskType)-Element
description: Gibt die Einstellungen an, die vom Taskplaner zum Ausführen der Aufgabe verwendet werden.
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- Settings-Element Taskplaner
topic_type:
- apiref
api_name:
- Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9133d536aef692a5f9928e10963dff8c454f25fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391761"
---
# <a name="settings-tasktype-element"></a><span data-ttu-id="ddbc7-104">Settings (TaskType)-Element</span><span class="sxs-lookup"><span data-stu-id="ddbc7-104">Settings (taskType) Element</span></span>

<span data-ttu-id="ddbc7-105">Gibt die Einstellungen an, die vom Taskplaner zum Ausführen der Aufgabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-105">Specifies the settings that the Task Scheduler uses to perform the task.</span></span>

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="ddbc7-106">Das **Settings** -Element wird durch den komplexen [**TaskType**](taskschedulerschema-tasktype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-106">The **Settings** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ddbc7-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="ddbc7-107">Parent element</span></span>



| <span data-ttu-id="ddbc7-108">Element</span><span class="sxs-lookup"><span data-stu-id="ddbc7-108">Element</span></span>                                          | <span data-ttu-id="ddbc7-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="ddbc7-109">Derived from</span></span>                                                 | <span data-ttu-id="ddbc7-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddbc7-110">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="ddbc7-111">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="ddbc7-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="ddbc7-113">Gibt die Aufgabe an, die vom Taskplaner-Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-113">Specifies the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="ddbc7-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ddbc7-114">Child elements</span></span>



| <span data-ttu-id="ddbc7-115">Element</span><span class="sxs-lookup"><span data-stu-id="ddbc7-115">Element</span></span>                                                                                                          | <span data-ttu-id="ddbc7-116">type</span><span class="sxs-lookup"><span data-stu-id="ddbc7-116">Type</span></span>                                                                                              | <span data-ttu-id="ddbc7-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddbc7-117">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddbc7-118">**Zuweisung aufheben**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-118">**AllowHardTerminate**</span></span>](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | <span data-ttu-id="ddbc7-119">boolean</span><span class="sxs-lookup"><span data-stu-id="ddbc7-119">boolean</span></span>                                                                                           | <span data-ttu-id="ddbc7-120">Gibt an, dass die Aufgabe mithilfe von TerminateProcess beendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-120">Specifies that the task may be terminated using TerminateProcess.</span></span><br/>                                         |
| [<span data-ttu-id="ddbc7-121">**Allowstartondemand**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-121">**AllowStartOnDemand**</span></span>](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | <span data-ttu-id="ddbc7-122">boolean</span><span class="sxs-lookup"><span data-stu-id="ddbc7-122">boolean</span></span>                                                                                           | <span data-ttu-id="ddbc7-123">Gibt an, dass der Task entweder über den Befehl ausführen oder über das Kontextmenü gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-123">Specifies that the task can be started using either the Run command or the Context menu.</span></span><br/>                  |
| [<span data-ttu-id="ddbc7-124">**Deleteexpiredtaskafter**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-124">**DeleteExpiredTaskAfter**</span></span>](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | <span data-ttu-id="ddbc7-125">duration</span><span class="sxs-lookup"><span data-stu-id="ddbc7-125">duration</span></span>                                                                                          | <span data-ttu-id="ddbc7-126">Gibt die Zeitspanne an, die der Taskplaner wartet, bevor der Task nach Ablauf gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-126">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span><br/> |
| [<span data-ttu-id="ddbc7-127">**Disallowstartifonakkus**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-127">**DisallowStartIfOnBatteries**</span></span>](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | <span data-ttu-id="ddbc7-128">boolean</span><span class="sxs-lookup"><span data-stu-id="ddbc7-128">boolean</span></span>                                                                                           | <span data-ttu-id="ddbc7-129">Gibt an, dass der Task nicht gestartet wird, wenn der Computer unter "Akkus" ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-129">Specifies that the task will not be started if the computer is running on batteries.</span></span><br/>                      |
| [<span data-ttu-id="ddbc7-130">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-130">**Enabled**</span></span>](taskschedulerschema-enabled-settingstype-element.md)                                              | <span data-ttu-id="ddbc7-131">boolean</span><span class="sxs-lookup"><span data-stu-id="ddbc7-131">boolean</span></span>                                                                                           | <span data-ttu-id="ddbc7-132">Gibt an, dass der Task aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-132">Specifies that the task is enabled.</span></span> <span data-ttu-id="ddbc7-133">Der Task kann nur ausgeführt werden, wenn diese Einstellung auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-133">The task can be performed only when this setting is True.</span></span><br/>             |
| [<span data-ttu-id="ddbc7-134">**Executiontimelimit**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-134">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | <span data-ttu-id="ddbc7-135">duration</span><span class="sxs-lookup"><span data-stu-id="ddbc7-135">duration</span></span>                                                                                          | <span data-ttu-id="ddbc7-136">Die Zeitspanne, die zum Ausführen der Aufgabe zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-136">Amount of time allowed to complete the task.</span></span><br/>                                                              |
| [<span data-ttu-id="ddbc7-137">**Verbirgt**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-137">**Hidden**</span></span>](taskschedulerschema-hidden-settingstype-element.md)                                                | <span data-ttu-id="ddbc7-138">boolean</span><span class="sxs-lookup"><span data-stu-id="ddbc7-138">boolean</span></span>                                                                                           | <span data-ttu-id="ddbc7-139">Gibt an, dass die Aufgabe nicht standardmäßig in der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-139">Specifies that the task will not be visible in the UI by default.</span></span><br/>                                         |
| [<span data-ttu-id="ddbc7-140">**Idlesettings**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-140">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [<span data-ttu-id="ddbc7-141">**idlesettingstype**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-141">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)                      | <span data-ttu-id="ddbc7-142">Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-142">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/>                    |
| [<span data-ttu-id="ddbc7-143">**Maintenancesettings**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-143">**MaintenanceSettings**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [<span data-ttu-id="ddbc7-144">**maintenancesettingstype**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-144">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md)        | <span data-ttu-id="ddbc7-145">Gibt an, wie das Taskplaner während der automatischen Wartung Tasks ausführt.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-145">Specifies how the Task Scheduler performs tasks during Automatic maintenance.</span></span><br/>                             |
| [<span data-ttu-id="ddbc7-146">**Multipleinstancespolicy**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-146">**MultipleInstancesPolicy**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [<span data-ttu-id="ddbc7-147">**multipleinstancespolicytype**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-147">**multipleInstancesPolicyType**</span></span>](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | <span data-ttu-id="ddbc7-148">Gibt die Richtlinie an, mit der definiert wird, wie die Taskplaner mehrere Instanzen der Aufgabe behandelt.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-148">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span><br/>       |
| [<span data-ttu-id="ddbc7-149">**Priorität**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-149">**Priority**</span></span>](taskschedulerschema-priority-settingstype-element.md)                                            | [<span data-ttu-id="ddbc7-150">**prioritytype**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-150">**priorityType**</span></span>](taskschedulerschema-prioritytype-simpletype.md)                               | <span data-ttu-id="ddbc7-151">Gibt die Prioritätsstufe für den Task an.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-151">Specifies the priority level for the task.</span></span><br/>                                                                |
| [<span data-ttu-id="ddbc7-152">**Neustartonfailure**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-152">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [<span data-ttu-id="ddbc7-153">**neustarttype**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-153">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)                                | <span data-ttu-id="ddbc7-154">Gibt an, dass der Taskplaner den Task neu starten soll, wenn die Aufgabe aus irgendeinem Grund fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-154">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/>      |
| [<span data-ttu-id="ddbc7-155">**Runonlyifdle**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-155">**RunOnlyIfIdle**</span></span>](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | <span data-ttu-id="ddbc7-156">boolean</span><span class="sxs-lookup"><span data-stu-id="ddbc7-156">boolean</span></span>                                                                                           | <span data-ttu-id="ddbc7-157">Gibt an, dass der Task nur ausgeführt wird, wenn sich der Computer im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-157">Specifies that the task is run only when the computer is in an idle state.</span></span><br/>                                |
| [<span data-ttu-id="ddbc7-158">**Runonlyifnetworkavailable**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-158">**RunOnlyIfNetworkAvailable**</span></span>](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | <span data-ttu-id="ddbc7-159">boolean</span><span class="sxs-lookup"><span data-stu-id="ddbc7-159">boolean</span></span>                                                                                           | <span data-ttu-id="ddbc7-160">Gibt an, dass der Taskplaner die Aufgabe nur dann ausgeführt wird, wenn ein Netzwerk verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-160">Specifies that the Task Scheduler will run the task only when a network is available.</span></span><br/>                     |
| [<span data-ttu-id="ddbc7-161">**Startvor verfügbar**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-161">**StartWhenAvailable**</span></span>](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | <span data-ttu-id="ddbc7-162">boolean</span><span class="sxs-lookup"><span data-stu-id="ddbc7-162">boolean</span></span>                                                                                           | <span data-ttu-id="ddbc7-163">Gibt an, dass die Taskplaner die Aufgabe jederzeit starten kann, nachdem die geplante Zeit abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-163">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span><br/>     |
| [<span data-ttu-id="ddbc7-164">**Stopifgoingonakkus (settingstype)**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-164">**StopIfGoingOnBatteries (settingsType)**</span></span>](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | <span data-ttu-id="ddbc7-165">boolean</span><span class="sxs-lookup"><span data-stu-id="ddbc7-165">boolean</span></span>                                                                                           | <span data-ttu-id="ddbc7-166">Gibt an, dass der Task angehalten wird, wenn der Computer auf die Batterie geht.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-166">Specifies that the task will be stopped if the computer is going onto batteries.</span></span><br/>                          |
| [<span data-ttu-id="ddbc7-167">**Ständigem**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-167">**Volatile**</span></span>](taskschedulerschema-volatile-element.md)                                                         | <span data-ttu-id="ddbc7-168">boolean</span><span class="sxs-lookup"><span data-stu-id="ddbc7-168">boolean</span></span>                                                                                           | <span data-ttu-id="ddbc7-169">Gibt an, ob die Aufgabe beim Windows-Start automatisch durch Taskplaner deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-169">Specifies if the task is automatically disabled by Task Scheduler at Windows startup.</span></span><br/>                     |
| [<span data-ttu-id="ddbc7-170">**Waketor (settingstype)**</span><span class="sxs-lookup"><span data-stu-id="ddbc7-170">**WakeToRun (settingsType)**</span></span>](taskschedulerschema-waketorun-settingstype-element.md)                           | <span data-ttu-id="ddbc7-171">boolean</span><span class="sxs-lookup"><span data-stu-id="ddbc7-171">boolean</span></span>                                                                                           | <span data-ttu-id="ddbc7-172">Gibt an, dass der Computer von Taskplaner reaktiviert wird, wenn der Task ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-172">Specifies that Task Scheduler will wake the computer when it is time to run the task.</span></span><br/>                     |



## <a name="remarks"></a><span data-ttu-id="ddbc7-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ddbc7-173">Remarks</span></span>

<span data-ttu-id="ddbc7-174">Sie können mindestens ein untergeordnetes Element auswählen, auf das oben verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-174">You can select one or more of the child elements referenced above.</span></span>

<span data-ttu-id="ddbc7-175">Bei der C++-Entwicklung werden die Registrierungsinformationen einer Aufgabe mithilfe der [**Settings-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings)angegeben.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-175">For C++ development, the registration information of a task is specified using the [**Settings property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).</span></span>

<span data-ttu-id="ddbc7-176">Bei der Skripterstellung werden die Registrierungsinformationen einer Aufgabe mithilfe der [**Task Definition. Settings**](taskdefinition-settings.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-176">For scripting development, the registration information of a task is specified using the [**TaskDefinition.Settings**](taskdefinition-settings.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="ddbc7-177">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ddbc7-177">Examples</span></span>

<span data-ttu-id="ddbc7-178">Im folgenden XML-Codebeispiel wird ein Einstellungs Element definiert, das eine harte Beendigung der Aufgabe ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="ddbc7-178">The following XML code example defines a settings element that allows a hard termination of the task.</span></span>


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



<span data-ttu-id="ddbc7-179">Weitere Informationen und ein umfassendes Beispiel für den XML-Code zum Festlegen von Task Einstellungen finden Sie unter [time-auslöserbeispiel (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="ddbc7-179">For more information and a complete example of the XML for setting task settings, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ddbc7-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ddbc7-180">Requirements</span></span>



| <span data-ttu-id="ddbc7-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ddbc7-181">Requirement</span></span> | <span data-ttu-id="ddbc7-182">Wert</span><span class="sxs-lookup"><span data-stu-id="ddbc7-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ddbc7-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ddbc7-183">Minimum supported client</span></span><br/> | <span data-ttu-id="ddbc7-184">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddbc7-184">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ddbc7-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ddbc7-185">Minimum supported server</span></span><br/> | <span data-ttu-id="ddbc7-186">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddbc7-186">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ddbc7-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddbc7-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddbc7-188">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="ddbc7-188">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ddbc7-189">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="ddbc7-189">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





