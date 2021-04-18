---
title: Sessionstatechange-Objekt
description: Skript Objekt, das Aufgaben für die Konsolen Verbindung oder die Verbindung, die Remote Verbindung oder die Verbindung oder die Sperre von Arbeitsstations sperren oder entsperren auslöst.
ms.assetid: ea450b8a-81cc-4d24-b850-78c967dcc5b8
keywords:
- Sessionstatechange-Objekt Taskplaner
- Sessionstatechangeauslöserobjekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55d41f495c714fe2e1798c79cc4f24b99987a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337723"
---
# <a name="sessionstatechangetrigger-object"></a><span data-ttu-id="12ed6-105">Sessionstatechange-Objekt</span><span class="sxs-lookup"><span data-stu-id="12ed6-105">SessionStateChangeTrigger object</span></span>

<span data-ttu-id="12ed6-106">Skript Objekt, das Aufgaben für die Konsolen Verbindung oder die Verbindung, die Remote Verbindung oder die Verbindung oder die Sperre von Arbeitsstations sperren oder entsperren auslöst.</span><span class="sxs-lookup"><span data-stu-id="12ed6-106">Scripting object that triggers tasks for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.</span></span>

## <a name="members"></a><span data-ttu-id="12ed6-107">Member</span><span class="sxs-lookup"><span data-stu-id="12ed6-107">Members</span></span>

<span data-ttu-id="12ed6-108">Das **sessionstatechange-** Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="12ed6-108">The **SessionStateChangeTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="12ed6-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12ed6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="12ed6-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12ed6-110">Properties</span></span>

<span data-ttu-id="12ed6-111">Das **sessionstatechange-** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="12ed6-111">The **SessionStateChangeTrigger** object has these properties.</span></span>



| <span data-ttu-id="12ed6-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="12ed6-112">Property</span></span>                                                                | <span data-ttu-id="12ed6-113">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="12ed6-113">Access type</span></span>           | <span data-ttu-id="12ed6-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12ed6-114">Description</span></span>                                                                                                                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12ed6-115">**Verzögern**</span><span class="sxs-lookup"><span data-stu-id="12ed6-115">**Delay**</span></span>](sessionstatechangetrigger-delay.md)<br/>             | <span data-ttu-id="12ed6-116">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12ed6-116">Read/write</span></span><br/> | <span data-ttu-id="12ed6-117">Ruft einen Wert ab oder legt einen Wert fest, der angibt, wie lange eine Verzögerung stattfindet, bevor eine Aufgabe gestartet wird, nachdem eine Terminal Server-Sitzungs Zustandsänderung erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="12ed6-117">Gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected.</span></span><br/>                                         |
| [<span data-ttu-id="12ed6-118">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="12ed6-118">**Enabled**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled)<br/>                          | <span data-ttu-id="12ed6-119">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12ed6-119">Read/write</span></span><br/> | <span data-ttu-id="12ed6-120">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="12ed6-120">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="12ed6-121">Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="12ed6-121">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="12ed6-122">**Endgrenze**</span><span class="sxs-lookup"><span data-stu-id="12ed6-122">**EndBoundary**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary)<br/>                  | <span data-ttu-id="12ed6-123">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12ed6-123">Read/write</span></span><br/> | <span data-ttu-id="12ed6-124">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="12ed6-124">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="12ed6-125">Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="12ed6-125">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="12ed6-126">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="12ed6-126">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="12ed6-127">**Executiontimelimit**</span><span class="sxs-lookup"><span data-stu-id="12ed6-127">**ExecutionTimeLimit**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit)<br/>    | <span data-ttu-id="12ed6-128">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12ed6-128">Read/write</span></span><br/> | <span data-ttu-id="12ed6-129">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="12ed6-129">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="12ed6-130">Ruft den maximalen Zeitraum ab, in dem der Task vom-Vorgang gestartet werden kann, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="12ed6-130">Gets or sets the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                                 |
| [<span data-ttu-id="12ed6-131">**Name**</span><span class="sxs-lookup"><span data-stu-id="12ed6-131">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                    | <span data-ttu-id="12ed6-132">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12ed6-132">Read/write</span></span><br/> | <span data-ttu-id="12ed6-133">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="12ed6-133">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="12ed6-134">Ruft den Bezeichner für den-Typ ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="12ed6-134">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="12ed6-135">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="12ed6-135">**Repetition**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition)<br/>                    | <span data-ttu-id="12ed6-136">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12ed6-136">Read/write</span></span><br/> | <span data-ttu-id="12ed6-137">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="12ed6-137">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="12ed6-138">Ruft einen Wert ab, der angibt, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird, oder legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="12ed6-138">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="12ed6-139">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="12ed6-139">**StartBoundary**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary)<br/>              | <span data-ttu-id="12ed6-140">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12ed6-140">Read/write</span></span><br/> | <span data-ttu-id="12ed6-141">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="12ed6-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="12ed6-142">Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="12ed6-142">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="12ed6-143">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="12ed6-143">**StateChange**</span></span>](sessionstatechangetrigger-statechange.md)<br/> | <span data-ttu-id="12ed6-144">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12ed6-144">Read/write</span></span><br/> | <span data-ttu-id="12ed6-145">Ruft die Art der Sitzungs Änderung für Terminal Server ab, die einen Task Start auslöst, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="12ed6-145">Gets or sets the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="12ed6-146">**type**</span><span class="sxs-lookup"><span data-stu-id="12ed6-146">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                | <span data-ttu-id="12ed6-147">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12ed6-147">Read-only</span></span><br/>  | <span data-ttu-id="12ed6-148">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="12ed6-148">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="12ed6-149">Ruft den Typ des Auslösers ab.</span><span class="sxs-lookup"><span data-stu-id="12ed6-149">Gets the type of the trigger.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="12ed6-150">**UserID**</span><span class="sxs-lookup"><span data-stu-id="12ed6-150">**UserId**</span></span>](sessionstatechangetrigger-userid.md)<br/>           | <span data-ttu-id="12ed6-151">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="12ed6-151">Read/write</span></span><br/> | <span data-ttu-id="12ed6-152">Ruft den Benutzer für die Terminal Server Sitzung ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="12ed6-152">Gets or sets the user for the Terminal Server session.</span></span> <span data-ttu-id="12ed6-153">Wenn eine Sitzungs Zustandsänderung für diesen Benutzer erkannt wird, wird eine Aufgabe gestartet.</span><span class="sxs-lookup"><span data-stu-id="12ed6-153">When a session state change is detected for this user, a task is started.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="12ed6-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12ed6-154">Remarks</span></span>

<span data-ttu-id="12ed6-155">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird ein Sitzungs Status Änderungs--Vorgang mit dem [**sessionstatechange-**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="12ed6-155">When reading or writing your own XML for a task, a session state change trigger is specified using the [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="12ed6-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12ed6-156">Requirements</span></span>



| <span data-ttu-id="12ed6-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12ed6-157">Requirement</span></span> | <span data-ttu-id="12ed6-158">Wert</span><span class="sxs-lookup"><span data-stu-id="12ed6-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12ed6-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12ed6-159">Minimum supported client</span></span><br/> | <span data-ttu-id="12ed6-160">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12ed6-160">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="12ed6-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12ed6-161">Minimum supported server</span></span><br/> | <span data-ttu-id="12ed6-162">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12ed6-162">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="12ed6-163">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="12ed6-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="12ed6-164"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="12ed6-164"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="12ed6-165">DLL</span><span class="sxs-lookup"><span data-stu-id="12ed6-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12ed6-166"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12ed6-166"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12ed6-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12ed6-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12ed6-168">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="12ed6-168">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="12ed6-169">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="12ed6-169">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





