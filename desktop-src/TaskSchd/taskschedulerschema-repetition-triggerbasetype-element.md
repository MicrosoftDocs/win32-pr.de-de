---
title: Wiederholungs Element (triggerbasetype)
description: Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- Wiederholungs Element Taskplaner
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ebd6f9f77998e5e975e24ff752a475e3880c0aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477778"
---
# <a name="repetition-triggerbasetype-element"></a><span data-ttu-id="beb94-104">Wiederholungs Element (triggerbasetype)</span><span class="sxs-lookup"><span data-stu-id="beb94-104">Repetition (triggerBaseType) Element</span></span>

<span data-ttu-id="beb94-105">Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="beb94-105">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

<span data-ttu-id="beb94-106">Das **Wiederholungs** Element wird durch den komplexen Typ [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="beb94-106">The **Repetition** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="beb94-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="beb94-107">Parent element</span></span>



| <span data-ttu-id="beb94-108">Element</span><span class="sxs-lookup"><span data-stu-id="beb94-108">Element</span></span>                                                                                     | <span data-ttu-id="beb94-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="beb94-109">Derived from</span></span>                                                                               | <span data-ttu-id="beb94-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="beb94-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="beb94-111">**Boottrigger**</span><span class="sxs-lookup"><span data-stu-id="beb94-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="beb94-112">**boottriggertype**</span><span class="sxs-lookup"><span data-stu-id="beb94-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="beb94-113">Gibt einen-Fehler an, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="beb94-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="beb94-114">**Calendarausgelöst**</span><span class="sxs-lookup"><span data-stu-id="beb94-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="beb94-115">**calendartriggertype**</span><span class="sxs-lookup"><span data-stu-id="beb94-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="beb94-116">Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.</span><span class="sxs-lookup"><span data-stu-id="beb94-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="beb94-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="beb94-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="beb94-118">**eventtriggertype**</span><span class="sxs-lookup"><span data-stu-id="beb94-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="beb94-119">Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="beb94-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="beb94-120">**Idle-Auslösung**</span><span class="sxs-lookup"><span data-stu-id="beb94-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="beb94-121">**idletriggertype**</span><span class="sxs-lookup"><span data-stu-id="beb94-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="beb94-122">Gibt einen-Auslösers an, der einen Task startet, wenn der Computer in den Leerlauf wechselt.</span><span class="sxs-lookup"><span data-stu-id="beb94-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="beb94-123">**Logonauslöst**</span><span class="sxs-lookup"><span data-stu-id="beb94-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="beb94-124">**logontriggertype**</span><span class="sxs-lookup"><span data-stu-id="beb94-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="beb94-125">Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="beb94-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="beb94-126">**Registration-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="beb94-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="beb94-127">**registrationtriggertype**</span><span class="sxs-lookup"><span data-stu-id="beb94-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="beb94-128">Gibt einen-Typ an, der einen Task startet, wenn der Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="beb94-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="beb94-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="beb94-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="beb94-130">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="beb94-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="beb94-131">Gibt einen-Auslösers an, der einen Task startet, wenn der--ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="beb94-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="child-elements"></a><span data-ttu-id="beb94-132">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="beb94-132">Child elements</span></span>



| <span data-ttu-id="beb94-133">Element</span><span class="sxs-lookup"><span data-stu-id="beb94-133">Element</span></span>                                                                                   | <span data-ttu-id="beb94-134">type</span><span class="sxs-lookup"><span data-stu-id="beb94-134">Type</span></span>     | <span data-ttu-id="beb94-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="beb94-135">Description</span></span>                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="beb94-136">**Duration**</span><span class="sxs-lookup"><span data-stu-id="beb94-136">**Duration**</span></span>](taskschedulerschema-duration-repetitiontype-element.md)                   | <span data-ttu-id="beb94-137">duration</span><span class="sxs-lookup"><span data-stu-id="beb94-137">duration</span></span> | <span data-ttu-id="beb94-138">Gibt an, wie lange das Muster wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="beb94-138">Specifies how long the pattern is repeated.</span></span><br/>                                                              |
| [<span data-ttu-id="beb94-139">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="beb94-139">**Interval**</span></span>](taskschedulerschema-interval-repetitiontype-element.md)                   | <span data-ttu-id="beb94-140">duration</span><span class="sxs-lookup"><span data-stu-id="beb94-140">duration</span></span> | <span data-ttu-id="beb94-141">Gibt die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="beb94-141">Specifies the amount of time between each restart of the task.</span></span><br/>                                           |
| [<span data-ttu-id="beb94-142">**Stopatdurationend**</span><span class="sxs-lookup"><span data-stu-id="beb94-142">**StopAtDurationEnd**</span></span>](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | <span data-ttu-id="beb94-143">boolean</span><span class="sxs-lookup"><span data-stu-id="beb94-143">boolean</span></span>  | <span data-ttu-id="beb94-144">Gibt an, dass eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer beendet wird.</span><span class="sxs-lookup"><span data-stu-id="beb94-144">Specifies that a running instances of the task is stopped at the end of the repetition pattern duration.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="beb94-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="beb94-145">Remarks</span></span>

<span data-ttu-id="beb94-146">Wenn Sie eine Wiederholungs Dauer für eine Aufgabe angeben, müssen Sie auch das Wiederholungsintervall angeben.</span><span class="sxs-lookup"><span data-stu-id="beb94-146">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="beb94-147">Wenn Sie eine Aufgabe registrieren, die einen-Auslösers mit einem Wiederholungsintervall von einer Minute und einer Wiederholungs Dauer von vier Minuten enthält, wird die Aufgabe fünfmal gestartet.</span><span class="sxs-lookup"><span data-stu-id="beb94-147">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched five times.</span></span> <span data-ttu-id="beb94-148">Die fünf Wiederholungen können mithilfe des folgenden Musters definiert werden.</span><span class="sxs-lookup"><span data-stu-id="beb94-148">The five repetitions can be defined by the following pattern.</span></span>

1.  <span data-ttu-id="beb94-149">Eine Aufgabe beginnt am Anfang der ersten Minute.</span><span class="sxs-lookup"><span data-stu-id="beb94-149">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="beb94-150">Die nächste Aufgabe beginnt am Ende der ersten Minute.</span><span class="sxs-lookup"><span data-stu-id="beb94-150">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="beb94-151">Die nächste Aufgabe beginnt am Ende der zweiten Minute.</span><span class="sxs-lookup"><span data-stu-id="beb94-151">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="beb94-152">Die nächste Aufgabe beginnt am Ende der dritten Minute.</span><span class="sxs-lookup"><span data-stu-id="beb94-152">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="beb94-153">Die nächste Aufgabe beginnt am Ende der vierten Minute.</span><span class="sxs-lookup"><span data-stu-id="beb94-153">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="beb94-154">**Windows Server 2003, Windows XP und Windows 2000:** Wenn Sie eine Aufgabe registrieren, die einen-Auslösers mit einem Wiederholungsintervall von einer Minute und einer Wiederholungs Dauer von vier Minuten enthält, wird die Aufgabe viermal gestartet.</span><span class="sxs-lookup"><span data-stu-id="beb94-154">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched four times.</span></span>

<span data-ttu-id="beb94-155">**Windows Vista, Windows 7, Windows Server 2008, Windows 8 und Windows Server 2012:** Wenn die Wiederholungs Dauer auf das genaue Vielfache des Intervalls festgelegt wird, ergibt sich in der Regel die oben beschriebene Anzahl.</span><span class="sxs-lookup"><span data-stu-id="beb94-155">**Windows Vista, Windows 7, Windows Server 2008, Windows 8 and Windows Server 2012:** Usually, setting the repetition duration to an exact multiple of the interval yields the numbers described above.</span></span> <span data-ttu-id="beb94-156">Unter bestimmten starken Ladebedingungen ist es jedoch möglich, dass die Dauer Zeitüberschreitung liegt, bevor TaskScheduler das abschließende Aufgaben Intervall starten kann.</span><span class="sxs-lookup"><span data-stu-id="beb94-156">However, under certain heavy load conditions, it is possible for the duration to timeout before TaskScheduler can launch the final task interval.</span></span>

<span data-ttu-id="beb94-157">Bei der Skripterstellung wird das Wiederholungsmuster mithilfe [**der Eigenschaft "" des "**](trigger-repetition.md) "</span><span class="sxs-lookup"><span data-stu-id="beb94-157">For scripting development, the repetition pattern is specified using the [**Trigger.Repetition**](trigger-repetition.md) property that is inherited by all the trigger objects.</span></span>

<span data-ttu-id="beb94-158">Bei der C++-Entwicklung wird das Wiederholungsmuster mithilfe der [**i-Funktion:: Wiederholungs**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) Eigenschaft angegeben, die von allen-auslöserschnittstellen geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="beb94-158">For C++ development, the repetition pattern is specified using the [**ITRigger::Repetition**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) property that is inherited by all the trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="beb94-159">Beispiele</span><span class="sxs-lookup"><span data-stu-id="beb94-159">Examples</span></span>

<span data-ttu-id="beb94-160">Der folgende XML-Code definiert ein startauslöserelement, das ein Wiederholungsmuster für einen-Auslösers angibt</span><span class="sxs-lookup"><span data-stu-id="beb94-160">The following XML defines a boot trigger element that specifies a repetition pattern for a trigger.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition>
        <Interval></Interval>
        <Duration></Duration>
        <StopAtDurationEnd>true</StopAtDirationEnd>
    </Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="beb94-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="beb94-161">Requirements</span></span>



| <span data-ttu-id="beb94-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="beb94-162">Requirement</span></span> | <span data-ttu-id="beb94-163">Wert</span><span class="sxs-lookup"><span data-stu-id="beb94-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="beb94-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="beb94-164">Minimum supported client</span></span><br/> | <span data-ttu-id="beb94-165">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="beb94-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="beb94-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="beb94-166">Minimum supported server</span></span><br/> | <span data-ttu-id="beb94-167">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="beb94-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="beb94-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="beb94-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb94-169">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="beb94-169">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="beb94-170">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="beb94-170">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





