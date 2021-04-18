---
title: komplexer settingstype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das Settings (TaskType)-Element.
ms.assetid: dba6b82d-aaa4-4f77-aeb1-c5a8f81aec25
keywords:
- komplexer settingstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- settingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3c2b3128a35ee0e46c56d19badd431400d4d862
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345308"
---
# <a name="settingstype-complex-type"></a><span data-ttu-id="a1782-104">komplexer settingstype-Typ</span><span class="sxs-lookup"><span data-stu-id="a1782-104">settingsType Complex Type</span></span>

<span data-ttu-id="a1782-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**Settings (TaskType)**](taskschedulerschema-settings-tasktype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="a1782-105">Defines the child elements and sequencing information for the [**Settings (taskType)**](taskschedulerschema-settings-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="settingsType">
    <xs:all>
        <xs:element name="AllowStartOnDemand"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnFailure"
            type="restartType"
            minOccurs="0"
         />
        <xs:element name="MultipleInstancesPolicy"
            type="multipleInstancesPolicyType"
            default="IgnoreNew"
            minOccurs="0"
         />
        <xs:element name="DisallowStartIfOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StopIfGoingOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="AllowHardTerminate"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartWhenAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="NetworkProfileName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfNetworkAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="WakeToRun"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="Hidden"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DeleteExpiredTaskAfter"
            type="duration"
            default="PT0S"
            minOccurs="0"
         />
        <xs:element name="IdleSettings"
            type="idleSettingsType"
            minOccurs="0"
         />
        <xs:element name="NetworkSettings"
            type="networkSettingsType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
        <xs:element name="Priority"
            type="priorityType"
            default="7"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="UseUnifiedSchedulingEngine"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DisallowStartOnRemoteAppSession"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a1782-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a1782-106">Child elements</span></span>



| <span data-ttu-id="a1782-107">Element</span><span class="sxs-lookup"><span data-stu-id="a1782-107">Element</span></span>                                                                                                             | <span data-ttu-id="a1782-108">type</span><span class="sxs-lookup"><span data-stu-id="a1782-108">Type</span></span>                                                                                              | <span data-ttu-id="a1782-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1782-109">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1782-110">**Zuweisung aufheben**</span><span class="sxs-lookup"><span data-stu-id="a1782-110">**AllowHardTerminate**</span></span>](taskschedulerschema-allowhardterminate-settingstype-element.md)                           | <span data-ttu-id="a1782-111">boolean</span><span class="sxs-lookup"><span data-stu-id="a1782-111">boolean</span></span>                                                                                           | <span data-ttu-id="a1782-112">Gibt an, ob der Taskplaner Dienstanbieter das harte Beenden der Aufgabe zulässt.</span><span class="sxs-lookup"><span data-stu-id="a1782-112">Specifies if the Task Scheduler service allows hard termination of the task.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="a1782-113">**Allowstartondemand**</span><span class="sxs-lookup"><span data-stu-id="a1782-113">**AllowStartOnDemand**</span></span>](taskschedulerschema-allowstartondemand-settingstype-element.md)                           | <span data-ttu-id="a1782-114">boolean</span><span class="sxs-lookup"><span data-stu-id="a1782-114">boolean</span></span>                                                                                           | <span data-ttu-id="a1782-115">Gibt an, dass der Task entweder mithilfe des Befehls ausführen oder des Kontextmenüs gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a1782-115">Specifies that the task can be started by using either the Run command or the Context menu.</span></span> <br/>                                                                                                                                                                                                             |
| [<span data-ttu-id="a1782-116">**Deleteexpiredtaskafter**</span><span class="sxs-lookup"><span data-stu-id="a1782-116">**DeleteExpiredTaskAfter**</span></span>](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                   | <span data-ttu-id="a1782-117">duration</span><span class="sxs-lookup"><span data-stu-id="a1782-117">duration</span></span>                                                                                          | <span data-ttu-id="a1782-118">Gibt die Zeitspanne an, die der Taskplaner wartet, bevor der Task nach Ablauf gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a1782-118">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="a1782-119">Wenn für dieses Element kein Wert angegeben wird, wird der Task vom Taskplaner-Dienst nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a1782-119">If no value is specified for this element, then the Task Scheduler service will not delete the task.</span></span><br/>                                                                                           |
| [<span data-ttu-id="a1782-120">**Disallowstartifonakkus**</span><span class="sxs-lookup"><span data-stu-id="a1782-120">**DisallowStartIfOnBatteries**</span></span>](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)           | <span data-ttu-id="a1782-121">boolean</span><span class="sxs-lookup"><span data-stu-id="a1782-121">boolean</span></span>                                                                                           | <span data-ttu-id="a1782-122">Gibt an, dass der Task nicht gestartet wird, wenn der Computer im Akku Betrieb ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1782-122">Specifies that the task will not be started if the computer is running on battery power.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="a1782-123">**Disallowstartonremoteappsession**</span><span class="sxs-lookup"><span data-stu-id="a1782-123">**DisallowStartOnRemoteAppSession**</span></span>](taskschedulerschema-disallowstartonremoteappsession-settingstype-element.md) | <span data-ttu-id="a1782-124">boolean</span><span class="sxs-lookup"><span data-stu-id="a1782-124">boolean</span></span>                                                                                           | <span data-ttu-id="a1782-125">Gibt an, dass der Task nicht gestartet werden soll, wenn die Aufgabe für die Durchführung in einer lokalen (Schiene) Remote Anwendung ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="a1782-125">Specifies that the task should not start if the task is triggered to run in a Remote Applications Integrated Locally (RAIL) session.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="a1782-126">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="a1782-126">**Enabled**</span></span>](taskschedulerschema-enabled-settingstype-element.md)                                                 | <span data-ttu-id="a1782-127">boolean</span><span class="sxs-lookup"><span data-stu-id="a1782-127">boolean</span></span>                                                                                           | <span data-ttu-id="a1782-128">Gibt an, dass der Task aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a1782-128">Specifies that the task is enabled.</span></span> <span data-ttu-id="a1782-129">Der Task kann nur ausgeführt werden, wenn diese Einstellung auf " **true**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a1782-129">The task can be performed only when this setting is **True**.</span></span><br/>                                                                                                                                                                                                        |
| [<span data-ttu-id="a1782-130">**Executiontimelimit**</span><span class="sxs-lookup"><span data-stu-id="a1782-130">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-settingstype-element.md)                           | <span data-ttu-id="a1782-131">duration</span><span class="sxs-lookup"><span data-stu-id="a1782-131">duration</span></span>                                                                                          | <span data-ttu-id="a1782-132">Gibt die Zeitspanne an, die zum Ausführen der Aufgabe zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="a1782-132">Specifies the amount of time allowed to complete the task.</span></span><br/>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="a1782-133">**Verbirgt**</span><span class="sxs-lookup"><span data-stu-id="a1782-133">**Hidden**</span></span>](taskschedulerschema-hidden-settingstype-element.md)                                                   | <span data-ttu-id="a1782-134">boolean</span><span class="sxs-lookup"><span data-stu-id="a1782-134">boolean</span></span>                                                                                           | <span data-ttu-id="a1782-135">Gibt standardmäßig an, dass die Aufgabe in der Benutzeroberfläche (UI) nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a1782-135">Specifies, by default, that the task will not be visible in the user interface (UI).</span></span><br/>                                                                                                                                                                                                                     |
| [<span data-ttu-id="a1782-136">**Idlesettings**</span><span class="sxs-lookup"><span data-stu-id="a1782-136">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md)                                       | [<span data-ttu-id="a1782-137">**idlesettingstype**</span><span class="sxs-lookup"><span data-stu-id="a1782-137">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)                      | <span data-ttu-id="a1782-138">Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="a1782-138">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/>                                                                                                                                                                                                                   |
| [<span data-ttu-id="a1782-139">**Multipleinstancespolicy**</span><span class="sxs-lookup"><span data-stu-id="a1782-139">**MultipleInstancesPolicy**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)                 | [<span data-ttu-id="a1782-140">**multipleinstancespolicytype**</span><span class="sxs-lookup"><span data-stu-id="a1782-140">**multipleInstancesPolicyType**</span></span>](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | <span data-ttu-id="a1782-141">Gibt die Richtlinie an, mit der definiert wird, wie die Taskplaner mehrere Instanzen der Aufgabe behandelt.</span><span class="sxs-lookup"><span data-stu-id="a1782-141">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span> <br/>                                                                                                                                                                                                     |
| [<span data-ttu-id="a1782-142">**Network Profile Name**</span><span class="sxs-lookup"><span data-stu-id="a1782-142">**NetworkProfileName**</span></span>](taskschedulerschema-networkprofilename-settingstype-element.md)                           | <span data-ttu-id="a1782-143">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a1782-143">string</span></span>                                                                                            | <span data-ttu-id="a1782-144">Gibt den Namen eines Netzwerk Profils an.</span><span class="sxs-lookup"><span data-stu-id="a1782-144">Specifies the name of a network profile.</span></span> <span data-ttu-id="a1782-145">Der Taskplaner-Dienst überprüft die Verfügbarkeit dieses Netzwerks, wenn das [**runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) -Element auf " **true**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a1782-145">The Task Scheduler service verifies the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span> <span data-ttu-id="a1782-146">Der Name wird zu Anzeige Zwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1782-146">The name is used for display purposes.</span></span><br/>        |
| [<span data-ttu-id="a1782-147">**NetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="a1782-147">**NetworkSettings**</span></span>](taskschedulerschema-networksettings-settingstype-element.md)                                 | [<span data-ttu-id="a1782-148">**Network settingstype**</span><span class="sxs-lookup"><span data-stu-id="a1782-148">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md)                | <span data-ttu-id="a1782-149">Gibt die Einstellungen an, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1782-149">Specifies the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="a1782-150">Der Taskplaner Dienst prüft die Verfügbarkeit dieses Netzwerks, wenn das [**runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) -Element auf " **true**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a1782-150">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |
| [<span data-ttu-id="a1782-151">**Priorität**</span><span class="sxs-lookup"><span data-stu-id="a1782-151">**Priority**</span></span>](taskschedulerschema-priority-settingstype-element.md)                                               | [<span data-ttu-id="a1782-152">**prioritytype**</span><span class="sxs-lookup"><span data-stu-id="a1782-152">**priorityType**</span></span>](taskschedulerschema-prioritytype-simpletype.md)                               | <span data-ttu-id="a1782-153">Gibt die Prioritätsstufe für den Task an.</span><span class="sxs-lookup"><span data-stu-id="a1782-153">Specifies the priority level for the task.</span></span><br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="a1782-154">**Neustartonfailure**</span><span class="sxs-lookup"><span data-stu-id="a1782-154">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md)                               | [<span data-ttu-id="a1782-155">**neustarttype**</span><span class="sxs-lookup"><span data-stu-id="a1782-155">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)                                | <span data-ttu-id="a1782-156">Gibt an, dass der Taskplaner versucht, den Task neu zu starten, wenn er aus irgendeinem Grund fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a1782-156">Specifies that the Task Scheduler will attempt to restart the task if it fails for any reason.</span></span> <br/>                                                                                                                                                                                                          |
| [<span data-ttu-id="a1782-157">**Runonlyifdle**</span><span class="sxs-lookup"><span data-stu-id="a1782-157">**RunOnlyIfIdle**</span></span>](taskschedulerschema-runonlyifidle-settingstype-element.md)                                     | <span data-ttu-id="a1782-158">boolean</span><span class="sxs-lookup"><span data-stu-id="a1782-158">boolean</span></span>                                                                                           | <span data-ttu-id="a1782-159">Gibt an, dass der Task nur ausgeführt wird, wenn sich der Computer im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="a1782-159">Specifies that the task is run only when the computer is in an idle state.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="a1782-160">**Runonlyifnetworkavailable**</span><span class="sxs-lookup"><span data-stu-id="a1782-160">**RunOnlyIfNetworkAvailable**</span></span>](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)             | <span data-ttu-id="a1782-161">boolean</span><span class="sxs-lookup"><span data-stu-id="a1782-161">boolean</span></span>                                                                                           | <span data-ttu-id="a1782-162">Gibt an, dass der Taskplaner die Aufgabe nur dann ausgeführt wird, wenn ein Netzwerk verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a1782-162">Specifies that the Task Scheduler will run the task only when a network is available.</span></span><br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="a1782-163">**Startvor verfügbar**</span><span class="sxs-lookup"><span data-stu-id="a1782-163">**StartWhenAvailable**</span></span>](taskschedulerschema-startwhenavailable-settingstype-element.md)                           | <span data-ttu-id="a1782-164">boolean</span><span class="sxs-lookup"><span data-stu-id="a1782-164">boolean</span></span>                                                                                           | <span data-ttu-id="a1782-165">Gibt an, dass die Taskplaner die Aufgabe jederzeit starten kann, nachdem die geplante Zeit abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="a1782-165">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="a1782-166">**Stopifgoingonakkus**</span><span class="sxs-lookup"><span data-stu-id="a1782-166">**StopIfGoingOnBatteries**</span></span>](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md)                   | <span data-ttu-id="a1782-167">boolean</span><span class="sxs-lookup"><span data-stu-id="a1782-167">boolean</span></span>                                                                                           | <span data-ttu-id="a1782-168">Gibt an, dass der Task angehalten wird, wenn der Computer in den Akku Betrieb wechselt.</span><span class="sxs-lookup"><span data-stu-id="a1782-168">Specifies that the task will be stopped if the computer switches to battery power.</span></span> <br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="a1782-169">**Useunifedschedulingengine**</span><span class="sxs-lookup"><span data-stu-id="a1782-169">**UseUnifiedSchedulingEngine**</span></span>](taskschedulerschema-useunifiedschedulingengine-settingstype-element.md)           | <span data-ttu-id="a1782-170">boolean</span><span class="sxs-lookup"><span data-stu-id="a1782-170">boolean</span></span>                                                                                           | <span data-ttu-id="a1782-171">Gibt an, dass der Task mithilfe der Unified Scheduling-Engine ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1782-171">Specifies that the task is run by using the Unified Scheduling Engine.</span></span><br/>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="a1782-172">**WakeToRun**</span><span class="sxs-lookup"><span data-stu-id="a1782-172">**WakeToRun**</span></span>](taskschedulerschema-waketorun-settingstype-element.md)                                             | <span data-ttu-id="a1782-173">boolean</span><span class="sxs-lookup"><span data-stu-id="a1782-173">boolean</span></span>                                                                                           | <span data-ttu-id="a1782-174">Gibt an, dass Taskplaner den Computer vor dem Ausführen der Aufgabe reaktivieren wird.</span><span class="sxs-lookup"><span data-stu-id="a1782-174">Specifies that Task Scheduler will wake the computer before it runs the task.</span></span><br/>                                                                                                                                                                                                                            |



## <a name="requirements"></a><span data-ttu-id="a1782-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1782-175">Requirements</span></span>



| <span data-ttu-id="a1782-176">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1782-176">Requirement</span></span> | <span data-ttu-id="a1782-177">Wert</span><span class="sxs-lookup"><span data-stu-id="a1782-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a1782-178">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1782-178">Minimum supported client</span></span><br/> | <span data-ttu-id="a1782-179">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1782-179">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1782-180">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1782-180">Minimum supported server</span></span><br/> | <span data-ttu-id="a1782-181">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1782-181">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1782-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1782-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1782-183">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="a1782-183">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="a1782-184">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="a1782-184">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





