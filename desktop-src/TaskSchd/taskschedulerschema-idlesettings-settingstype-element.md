---
title: Idlesettings (settingstype)-Element
description: Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- Idlesettings-Element Taskplaner
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae8b7953f31d7e9c6f01387d3136f01d8ab697a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105219"
---
# <a name="idlesettings-settingstype-element"></a><span data-ttu-id="ff314-104">Idlesettings (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="ff314-104">IdleSettings (settingsType) Element</span></span>

<span data-ttu-id="ff314-105">Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="ff314-105">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span> <span data-ttu-id="ff314-106">Informationen zu Bedingungen im Leerlauf finden Sie unter [Aufgaben im Leerlauf](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="ff314-106">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="ff314-107">Das **idlesettings** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="ff314-107">The **IdleSettings** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ff314-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="ff314-108">Parent element</span></span>

| <span data-ttu-id="ff314-109">Element</span><span class="sxs-lookup"><span data-stu-id="ff314-109">Element</span></span>                                                           | <span data-ttu-id="ff314-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="ff314-110">Derived from</span></span>                                                         | <span data-ttu-id="ff314-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff314-111">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff314-112">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="ff314-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="ff314-113">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="ff314-113">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="ff314-114">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ff314-114">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |

## <a name="child-elements"></a><span data-ttu-id="ff314-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff314-115">Child elements</span></span>

> [!NOTE]
> <span data-ttu-id="ff314-116">Die Einstellungen für *Dauer* und *WaitTimeout* sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="ff314-116">The *Duration* and *WaitTimeout* settings are deprecated.</span></span> <span data-ttu-id="ff314-117">Sie sind weiterhin in der Taskplaner-Benutzeroberfläche vorhanden, und ihre Schnittstellen Methoden geben möglicherweise weiterhin gültige Werte zurück, aber Sie werden nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff314-117">They're still present in the Task Scheduler user interface, and their interface methods may still return valid values, but they're no longer used.</span></span>

| <span data-ttu-id="ff314-118">Element</span><span class="sxs-lookup"><span data-stu-id="ff314-118">Element</span></span>                                                                                  | <span data-ttu-id="ff314-119">type</span><span class="sxs-lookup"><span data-stu-id="ff314-119">Type</span></span>     | <span data-ttu-id="ff314-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff314-120">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff314-121">**Neustartondle**</span><span class="sxs-lookup"><span data-stu-id="ff314-121">**RestartOnIdle**</span></span>](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | <span data-ttu-id="ff314-122">boolean</span><span class="sxs-lookup"><span data-stu-id="ff314-122">boolean</span></span>  | <span data-ttu-id="ff314-123">Gibt an, ob der Task neu gestartet wird, wenn der Computer mehrmals in eine Leerlauf Bedingung wechselt.</span><span class="sxs-lookup"><span data-stu-id="ff314-123">Specifies whether the task is restarted when the computer cycles into an idle condition more than once.</span></span><br/>       |
| [<span data-ttu-id="ff314-124">**Stoponidleend**</span><span class="sxs-lookup"><span data-stu-id="ff314-124">**StopOnIdleEnd**</span></span>](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | <span data-ttu-id="ff314-125">boolean</span><span class="sxs-lookup"><span data-stu-id="ff314-125">boolean</span></span>  | <span data-ttu-id="ff314-126">Gibt an, dass der Taskplaner den Task beendet, wenn die Leerlauf Bedingung vor dem Abschluss der Aufgabe endet.</span><span class="sxs-lookup"><span data-stu-id="ff314-126">Specifies that the Task Scheduler will stop the task if the idle condition ends before the task is completed.</span></span><br/> |
| <span data-ttu-id="ff314-127">**Veraltet**: [ **Dauer**](taskschedulerschema-duration-idlesettingstype-element.md)</span><span class="sxs-lookup"><span data-stu-id="ff314-127">**Deprecated**: [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md)</span></span>                | <span data-ttu-id="ff314-128">duration</span><span class="sxs-lookup"><span data-stu-id="ff314-128">duration</span></span> | <span data-ttu-id="ff314-129">Gibt an, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff314-129">Specifies how long the computer must be in an idle state before the task is run.</span></span><br/>                              |
| <span data-ttu-id="ff314-130">**Veraltet**: [ **WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)</span><span class="sxs-lookup"><span data-stu-id="ff314-130">**Deprecated**: [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)</span></span>          | <span data-ttu-id="ff314-131">duration</span><span class="sxs-lookup"><span data-stu-id="ff314-131">duration</span></span> | <span data-ttu-id="ff314-132">Gibt die Zeitspanne an, die der Taskplaner auf das Eintreten einer Leerlauf Bedingung wartet.</span><span class="sxs-lookup"><span data-stu-id="ff314-132">Specifies the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span><br/>                |

## <a name="remarks"></a><span data-ttu-id="ff314-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff314-133">Remarks</span></span>

<span data-ttu-id="ff314-134">Bei der Skript Entwicklung werden im Leerlauf Einstellungen mithilfe der [**tasksettings. idlesettings**](tasksettings-idlesettings.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="ff314-134">For script development, idle settings are specified using the [**TaskSettings.IdleSettings**](tasksettings-idlesettings.md) property.</span></span>

<span data-ttu-id="ff314-135">Bei der C++-Entwicklung werden Leerlauf Einstellungen mithilfe der [**itasksettings:: idlesettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="ff314-135">For C++ development, idle settings are specified using the [**ITaskSettings::IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) property.</span></span>

## <a name="examples"></a><span data-ttu-id="ff314-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff314-136">Examples</span></span>

<span data-ttu-id="ff314-137">Der folgende XML-Code definiert ein settings-Element, das es Taskplaner ermöglicht, 24 Stunden auf eine Leerlauf Bedingung zu warten, und dann nur 10 Minuten {idleduration) zum Initiieren der Aufgabe zulässt.</span><span class="sxs-lookup"><span data-stu-id="ff314-137">The following XML defines a settings element that allows Task Scheduler to wait 24 hours for an idle condition and then allows only 10 minutes {IdleDuration) to initiate the task.</span></span>

```XML
<Settings>
    <IdleSettings>
        <StopOnIdleEnd>false</StopOnIdleEnd>
        <RestartOnIdle>false</RestartOnIdle> 
        <!-- WaitTimeout and Duration have been deprecated -->
        <Duration>PT5M</Duration>
        <WaitTimeout>PT24H</WaitTimeout>
    </IdleSettings>       
</Settings>
```

## <a name="requirements"></a><span data-ttu-id="ff314-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff314-138">Requirements</span></span>

| <span data-ttu-id="ff314-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff314-139">Requirement</span></span> | <span data-ttu-id="ff314-140">Wert</span><span class="sxs-lookup"><span data-stu-id="ff314-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff314-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff314-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ff314-142">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff314-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ff314-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff314-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ff314-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff314-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |

## <a name="see-also"></a><span data-ttu-id="ff314-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff314-145">See also</span></span>

[<span data-ttu-id="ff314-146">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="ff314-146">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)

[<span data-ttu-id="ff314-147">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="ff314-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
