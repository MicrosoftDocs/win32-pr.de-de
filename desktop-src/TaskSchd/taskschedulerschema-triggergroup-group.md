---
title: triggergroup-Gruppe
description: Definiert die auslösergruppe.
ms.assetid: e07e6999-d982-405b-adfd-2976707b999f
keywords:
- triggergroup-Taskplaner
topic_type:
- apiref
api_name:
- triggerGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce0203cd9515808891f93223dd7b3ebaf2642103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106341"
---
# <a name="triggergroup-group"></a><span data-ttu-id="f3a13-104">triggergroup-Gruppe</span><span class="sxs-lookup"><span data-stu-id="f3a13-104">triggerGroup Group</span></span>

<span data-ttu-id="f3a13-105">Definiert die auslösergruppe.</span><span class="sxs-lookup"><span data-stu-id="f3a13-105">Defines the trigger group.</span></span>

``` syntax
<xs:group name="triggerGroup">
    <xs:choice>
        <xs:element name="BootTrigger"
            type="bootTriggerType"
            minOccurs="0"
         />
        <xs:element name="RegistrationTrigger"
            type="registrationTriggerType"
            minOccurs="0"
         />
        <xs:element name="IdleTrigger"
            type="idleTriggerType"
            minOccurs="0"
         />
        <xs:element name="TimeTrigger"
            type="timeTriggerType"
            minOccurs="0"
         />
        <xs:element name="EventTrigger"
            type="eventTriggerType"
            minOccurs="0"
         />
        <xs:element name="LogonTrigger"
            type="logonTriggerType"
            minOccurs="0"
         />
        <xs:element name="SessionStateChangeTrigger"
            type="sessionStateChangeTriggerType"
            minOccurs="0"
         />
        <xs:element name="CalendarTrigger"
            type="calendarTriggerType"
            minOccurs="0"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="f3a13-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f3a13-106">Child elements</span></span>



| <span data-ttu-id="f3a13-107">Element</span><span class="sxs-lookup"><span data-stu-id="f3a13-107">Element</span></span>                                                                                                 | <span data-ttu-id="f3a13-108">type</span><span class="sxs-lookup"><span data-stu-id="f3a13-108">Type</span></span>                                                                                                   | <span data-ttu-id="f3a13-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3a13-109">Description</span></span>                                                                                                       |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3a13-110">**Boottrigger**</span><span class="sxs-lookup"><span data-stu-id="f3a13-110">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                             | [<span data-ttu-id="f3a13-111">**boottriggertype**</span><span class="sxs-lookup"><span data-stu-id="f3a13-111">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                             | <span data-ttu-id="f3a13-112">Ein-Fehler, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f3a13-112">A trigger that starts a task when the system is booted.</span></span><br/>                                                |
| [<span data-ttu-id="f3a13-113">**Calendarausgelöst**</span><span class="sxs-lookup"><span data-stu-id="f3a13-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)                     | [<span data-ttu-id="f3a13-114">**calendartriggertype**</span><span class="sxs-lookup"><span data-stu-id="f3a13-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)                     | <span data-ttu-id="f3a13-115">Ein-Vorgang, bei dem eine Aufgabe auf Grundlage eines täglichen, wöchentlichen, monatlichen oder monatlichen Zeitplans (Day-of-week, Dow) gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f3a13-115">A trigger that starts a task based on a daily, weekly, monthly, or monthly day-of-week (DOW) schedule.</span></span><br/> |
| [<span data-ttu-id="f3a13-116">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="f3a13-116">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)                           | [<span data-ttu-id="f3a13-117">**eventtriggertype**</span><span class="sxs-lookup"><span data-stu-id="f3a13-117">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)                           | <span data-ttu-id="f3a13-118">Ein-Fehler, der eine Aufgabe startet, wenn ein System Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="f3a13-118">A trigger that starts a task when a system event occurs.</span></span><br/>                                               |
| [<span data-ttu-id="f3a13-119">**Idle-Auslösung**</span><span class="sxs-lookup"><span data-stu-id="f3a13-119">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                             | [<span data-ttu-id="f3a13-120">**idletriggertype**</span><span class="sxs-lookup"><span data-stu-id="f3a13-120">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                             | <span data-ttu-id="f3a13-121">Ein-Vorgang, der einen Task startet, wenn der Computer in den Leerlauf wechselt.</span><span class="sxs-lookup"><span data-stu-id="f3a13-121">A trigger that starts a task when the computer goes into an idle state.</span></span><br/>                                |
| [<span data-ttu-id="f3a13-122">**Logonauslöst**</span><span class="sxs-lookup"><span data-stu-id="f3a13-122">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)                           | [<span data-ttu-id="f3a13-123">**logontriggertype**</span><span class="sxs-lookup"><span data-stu-id="f3a13-123">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)                           | <span data-ttu-id="f3a13-124">Ein-Vorgang, der einen Task startet, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="f3a13-124">A trigger that starts a task when a user logs on.</span></span><br/>                                                      |
| [<span data-ttu-id="f3a13-125">**Registration-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="f3a13-125">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md)             | [<span data-ttu-id="f3a13-126">**registrationtriggertype**</span><span class="sxs-lookup"><span data-stu-id="f3a13-126">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md)             | <span data-ttu-id="f3a13-127">Ein-Vorgang, der einen Task startet, wenn der Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="f3a13-127">A trigger that starts a task when the task is registered.</span></span><br/>                                              |
| [<span data-ttu-id="f3a13-128">**Sessionstatechange-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="f3a13-128">**SessionStateChangeTrigger**</span></span>](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) | [<span data-ttu-id="f3a13-129">**sessionstatechangetriggertype**</span><span class="sxs-lookup"><span data-stu-id="f3a13-129">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="f3a13-130">Ein-Vorgang, der einen Task startet, wenn sich der Status einer Terminal Server Sitzung ändert.</span><span class="sxs-lookup"><span data-stu-id="f3a13-130">A trigger that starts a task when a Terminal Server session changes state.</span></span><br/>                             |
| [<span data-ttu-id="f3a13-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="f3a13-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                             | [<span data-ttu-id="f3a13-132">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="f3a13-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                             | <span data-ttu-id="f3a13-133">Ein-Vorgang, der einen Task startet, wenn der-Auslösers aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f3a13-133">A trigger that starts a task when the trigger is activated.</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="f3a13-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3a13-134">Remarks</span></span>

<span data-ttu-id="f3a13-135">Beim Lesen oder Schreiben von XML sind die Elemente, die von dieser Gruppe definiert werden, die untergeordneten [**Elemente des Triggers-Elements.**](taskschedulerschema-triggers-tasktype-element.md)</span><span class="sxs-lookup"><span data-stu-id="f3a13-135">When reading or writing XML, the elements that are defined by this group are the child elements of the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a13-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3a13-136">Requirements</span></span>



| <span data-ttu-id="f3a13-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3a13-137">Requirement</span></span> | <span data-ttu-id="f3a13-138">Wert</span><span class="sxs-lookup"><span data-stu-id="f3a13-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3a13-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3a13-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f3a13-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3a13-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f3a13-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3a13-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f3a13-142">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3a13-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3a13-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3a13-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a13-144">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="f3a13-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





