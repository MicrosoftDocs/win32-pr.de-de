---
title: Trigger (TaskType)-Element
description: Gibt die Trigger an, die den Task starten.
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- Trigger-Element Taskplaner
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06994c395fbfbc5b0c6244c9d17930bc4afac885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743753"
---
# <a name="triggers-tasktype-element"></a><span data-ttu-id="538db-104">Trigger (TaskType)-Element</span><span class="sxs-lookup"><span data-stu-id="538db-104">Triggers (taskType) Element</span></span>

<span data-ttu-id="538db-105">Gibt die Trigger an, die den Task starten.</span><span class="sxs-lookup"><span data-stu-id="538db-105">Specifies the triggers that start the task.</span></span>

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

<span data-ttu-id="538db-106">Das **Trigger** -Element wird durch den komplexen [**triggerstype**](taskschedulerschema-triggerstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="538db-106">The **Triggers** element is defined by the [**triggersType**](taskschedulerschema-triggerstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="538db-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="538db-107">Parent element</span></span>



| <span data-ttu-id="538db-108">Element</span><span class="sxs-lookup"><span data-stu-id="538db-108">Element</span></span>                                          | <span data-ttu-id="538db-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="538db-109">Derived from</span></span>                                                 | <span data-ttu-id="538db-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="538db-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="538db-111">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="538db-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="538db-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="538db-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="538db-113">Definiert den Task, der vom Taskplaner-Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="538db-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="538db-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="538db-114">Child elements</span></span>



| <span data-ttu-id="538db-115">Element</span><span class="sxs-lookup"><span data-stu-id="538db-115">Element</span></span>                                                                                     | <span data-ttu-id="538db-116">type</span><span class="sxs-lookup"><span data-stu-id="538db-116">Type</span></span>                                                                                       | <span data-ttu-id="538db-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="538db-117">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="538db-118">**Boottrigger**</span><span class="sxs-lookup"><span data-stu-id="538db-118">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="538db-119">**boottriggertype**</span><span class="sxs-lookup"><span data-stu-id="538db-119">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="538db-120">Gibt einen-Fehler an, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="538db-120">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="538db-121">**Calendarausgelöst**</span><span class="sxs-lookup"><span data-stu-id="538db-121">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="538db-122">**calendartriggertype**</span><span class="sxs-lookup"><span data-stu-id="538db-122">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="538db-123">Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.</span><span class="sxs-lookup"><span data-stu-id="538db-123">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="538db-124">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="538db-124">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="538db-125">**eventtriggertype**</span><span class="sxs-lookup"><span data-stu-id="538db-125">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="538db-126">Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="538db-126">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="538db-127">**Idle-Auslösung**</span><span class="sxs-lookup"><span data-stu-id="538db-127">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="538db-128">**idletriggertype**</span><span class="sxs-lookup"><span data-stu-id="538db-128">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="538db-129">Gibt einen-Auslösers an, der einen Task startet, wenn der Computer in den Leerlauf wechselt.</span><span class="sxs-lookup"><span data-stu-id="538db-129">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="538db-130">**Logonauslöst**</span><span class="sxs-lookup"><span data-stu-id="538db-130">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="538db-131">**logontriggertype**</span><span class="sxs-lookup"><span data-stu-id="538db-131">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="538db-132">Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="538db-132">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="538db-133">**Registration-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="538db-133">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="538db-134">**registrationtriggertype**</span><span class="sxs-lookup"><span data-stu-id="538db-134">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="538db-135">Gibt einen-Typ an, der einen Task startet, wenn der Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="538db-135">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="538db-136">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="538db-136">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="538db-137">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="538db-137">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="538db-138">Gibt einen-Auslösers an, der einen Task startet, wenn der--ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="538db-138">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="538db-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="538db-139">Remarks</span></span>

<span data-ttu-id="538db-140">Die oben aufgeführten untergeordneten Elemente können in beliebiger Reihenfolge hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="538db-140">The child elements listed above can be added in any order.</span></span>

<span data-ttu-id="538db-141">Bei der C++-Entwicklung werden die Trigger einer Aufgabe mithilfe der Triggers- [**Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers)angegeben.</span><span class="sxs-lookup"><span data-stu-id="538db-141">For C++ development, the triggers of a task are specified using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).</span></span>

<span data-ttu-id="538db-142">Bei der Skripterstellung werden die Trigger einer Aufgabe mithilfe der [**Taskdefinition.**](taskdefinition-triggers.md) Triggers-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="538db-142">For scripting development, the triggers of a task are specified using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="538db-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="538db-143">Examples</span></span>

<span data-ttu-id="538db-144">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen-Auslösers angibt, finden Sie unter [time-auslöserbeispiel (XML)](time-trigger-example--xml-.md)</span><span class="sxs-lookup"><span data-stu-id="538db-144">For a complete example of the XML for a task that specifies a trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="538db-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="538db-145">Requirements</span></span>



| <span data-ttu-id="538db-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="538db-146">Requirement</span></span> | <span data-ttu-id="538db-147">Wert</span><span class="sxs-lookup"><span data-stu-id="538db-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="538db-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="538db-148">Minimum supported client</span></span><br/> | <span data-ttu-id="538db-149">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="538db-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="538db-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="538db-150">Minimum supported server</span></span><br/> | <span data-ttu-id="538db-151">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="538db-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="538db-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="538db-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="538db-153">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="538db-153">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="538db-154">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="538db-154">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





