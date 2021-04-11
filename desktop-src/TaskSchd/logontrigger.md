---
title: Logon-Auslöserobjekt
description: Skript Objekt, das einen-Auslösers darstellt, der einen Task startet, wenn sich ein Benutzer anmeldet.
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- Logon-auslöserTaskplaner, Objekt
- Logon-Auslöserobjekt Taskplaner
- Logon-Auslöserobjekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- LogonTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9c4b2031b39a6dfd483b039023ad9114271b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956766"
---
# <a name="logontrigger-object"></a><span data-ttu-id="dc43a-106">Logon-Auslöserobjekt</span><span class="sxs-lookup"><span data-stu-id="dc43a-106">LogonTrigger object</span></span>

<span data-ttu-id="dc43a-107">Skript Objekt, das einen-Auslösers darstellt, der einen Task startet, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="dc43a-107">Scripting object that represents a trigger that starts a task when a user logs on.</span></span> <span data-ttu-id="dc43a-108">Wenn der Taskplaner-Dienst gestartet wird, werden alle angemeldeten Benutzer aufgezählt, und alle mit LOGON-Triggern registrierten Tasks, die dem angemeldeten Benutzer entsprechen, werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc43a-108">When the Task Scheduler service starts, all logged-on users are enumerated and any tasks registered with logon triggers that match the logged on user are run.</span></span>

## <a name="members"></a><span data-ttu-id="dc43a-109">Member</span><span class="sxs-lookup"><span data-stu-id="dc43a-109">Members</span></span>

<span data-ttu-id="dc43a-110">Das **Logon-Auslöserobjekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dc43a-110">The **LogonTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="dc43a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc43a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc43a-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc43a-112">Properties</span></span>

<span data-ttu-id="dc43a-113">Das **Logon-Auslöserobjekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc43a-113">The **LogonTrigger** object has these properties.</span></span>



| <span data-ttu-id="dc43a-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dc43a-114">Property</span></span>                                                            | <span data-ttu-id="dc43a-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="dc43a-115">Access type</span></span>           | <span data-ttu-id="dc43a-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc43a-116">Description</span></span>                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc43a-117">**Verzögern**</span><span class="sxs-lookup"><span data-stu-id="dc43a-117">**Delay**</span></span>](logontrigger-delay.md)<br/>                      | <span data-ttu-id="dc43a-118">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc43a-118">Read/write</span></span><br/> | <span data-ttu-id="dc43a-119">Ruft einen Wert ab oder legt einen Wert fest, der die Zeitspanne zwischen dem Zeitpunkt der Anmeldung des Benutzers und dem Start des Auftrags angibt.</span><span class="sxs-lookup"><span data-stu-id="dc43a-119">Gets or sets a value that indicates the amount of time between when the user logs on and when the job is started.</span></span><br/>                                                                              |
| [<span data-ttu-id="dc43a-120">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="dc43a-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="dc43a-121">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc43a-121">Read/write</span></span><br/> | <span data-ttu-id="dc43a-122">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="dc43a-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="dc43a-123">Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="dc43a-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="dc43a-124">**Endgrenze**</span><span class="sxs-lookup"><span data-stu-id="dc43a-124">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="dc43a-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc43a-125">Read/write</span></span><br/> | <span data-ttu-id="dc43a-126">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="dc43a-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="dc43a-127">Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="dc43a-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="dc43a-128">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="dc43a-128">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="dc43a-129">**Executiontimelimit**</span><span class="sxs-lookup"><span data-stu-id="dc43a-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="dc43a-130">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc43a-130">Read/write</span></span><br/> | <span data-ttu-id="dc43a-131">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="dc43a-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="dc43a-132">Ruft die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="dc43a-132">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                                         |
| [<span data-ttu-id="dc43a-133">**Name**</span><span class="sxs-lookup"><span data-stu-id="dc43a-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="dc43a-134">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc43a-134">Read/write</span></span><br/> | <span data-ttu-id="dc43a-135">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="dc43a-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="dc43a-136">Ruft den Bezeichner für den-Typ ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="dc43a-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="dc43a-137">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="dc43a-137">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="dc43a-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc43a-138">Read/write</span></span><br/> | <span data-ttu-id="dc43a-139">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="dc43a-139">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="dc43a-140">Ruft einen Wert ab, der angibt, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird, oder legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="dc43a-140">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="dc43a-141">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="dc43a-141">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="dc43a-142">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc43a-142">Read/write</span></span><br/> | <span data-ttu-id="dc43a-143">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="dc43a-143">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="dc43a-144">Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="dc43a-144">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="dc43a-145">**type**</span><span class="sxs-lookup"><span data-stu-id="dc43a-145">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="dc43a-146">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc43a-146">Read-only</span></span><br/>  | <span data-ttu-id="dc43a-147">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="dc43a-147">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="dc43a-148">Ruft den Typ des Auslösers ab.</span><span class="sxs-lookup"><span data-stu-id="dc43a-148">Gets the type of the trigger.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="dc43a-149">**UserID**</span><span class="sxs-lookup"><span data-stu-id="dc43a-149">**UserId**</span></span>](logontrigger-userid.md)<br/>                    | <span data-ttu-id="dc43a-150">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc43a-150">Read/write</span></span><br/> | <span data-ttu-id="dc43a-151">Ruft den Bezeichner des Benutzers ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="dc43a-151">Gets or sets the identifier of the user.</span></span><br/>                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="dc43a-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc43a-152">Remarks</span></span>

<span data-ttu-id="dc43a-153">Wenn ein Task ausgelöst werden soll, wenn sich ein Mitglied einer Gruppe beim Computer anmeldet, anstatt sich zu anmelden, wenn sich ein bestimmter Benutzer anmeldet, weisen Sie der [**logontrigger. UserID**](logontrigger-userid.md) -Eigenschaft keinen Wert zu.</span><span class="sxs-lookup"><span data-stu-id="dc43a-153">If you want a task to be triggered when any member of a group logs on to the computer rather than when a specific user logs on, then do not assign a value to the [**LogonTrigger.UserId**](logontrigger-userid.md) property.</span></span> <span data-ttu-id="dc43a-154">Erstellen Sie stattdessen einen LOGON-und eine leere **logonauslöst. UserID** -Eigenschaft, und weisen Sie dem Prinzipal für die Aufgabe mithilfe der [**Principal. GroupID**](principal-groupid.md) -Eigenschaft einen Wert zu.</span><span class="sxs-lookup"><span data-stu-id="dc43a-154">Instead, create a logon trigger with an empty **LogonTrigger.UserId** property and assign a value to the principal for the task using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="dc43a-155">Beim Lesen oder Schreiben von XML für eine Aufgabe wird ein LOGON-Vorgang mit dem [**Logon-Auslöserelement**](taskschedulerschema-logontrigger-triggergroup-element.md) des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="dc43a-155">When reading or writing XML for a task, a logon trigger is specified using the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="dc43a-156">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc43a-156">Examples</span></span>

<span data-ttu-id="dc43a-157">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [Logon-auslöserbeispiel (Skripterstellung)](logon-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="dc43a-157">For more information and example code for this scripting object, see [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc43a-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc43a-158">Requirements</span></span>



| <span data-ttu-id="dc43a-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc43a-159">Requirement</span></span> | <span data-ttu-id="dc43a-160">Wert</span><span class="sxs-lookup"><span data-stu-id="dc43a-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc43a-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc43a-161">Minimum supported client</span></span><br/> | <span data-ttu-id="dc43a-162">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc43a-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dc43a-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc43a-163">Minimum supported server</span></span><br/> | <span data-ttu-id="dc43a-164">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc43a-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dc43a-165">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="dc43a-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="dc43a-166"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dc43a-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dc43a-167">DLL</span><span class="sxs-lookup"><span data-stu-id="dc43a-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc43a-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc43a-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc43a-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc43a-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc43a-170">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="dc43a-170">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





