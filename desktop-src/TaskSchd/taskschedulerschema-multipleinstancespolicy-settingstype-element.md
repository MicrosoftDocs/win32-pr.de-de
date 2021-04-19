---
title: Multipleinstancespolicy-Element (settingstype)
description: Gibt die Richtlinie an, mit der definiert wird, wie die Taskplaner mehrere Instanzen der Aufgabe behandelt.
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- Multipleinstancespolicy-Element Taskplaner
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5bcbbd26880f1ccced3e71b44dc93993d20f4a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339165"
---
# <a name="multipleinstancespolicy-settingstype-element"></a><span data-ttu-id="1a393-104">Multipleinstancespolicy-Element (settingstype)</span><span class="sxs-lookup"><span data-stu-id="1a393-104">MultipleInstancesPolicy (settingsType) Element</span></span>

<span data-ttu-id="1a393-105">Gibt die Richtlinie an, mit der definiert wird, wie die Taskplaner mehrere Instanzen der Aufgabe behandelt.</span><span class="sxs-lookup"><span data-stu-id="1a393-105">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span>

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

<span data-ttu-id="1a393-106">Das **multipleinstancespolicy** -Element wird vom einfachen Typ " [**multipleinstancespolicytype**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="1a393-106">The **MultipleInstancesPolicy** element is defined by the [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) simple type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1a393-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1a393-107">Parent element</span></span>



| <span data-ttu-id="1a393-108">Element</span><span class="sxs-lookup"><span data-stu-id="1a393-108">Element</span></span>                                                           | <span data-ttu-id="1a393-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="1a393-109">Derived from</span></span>                                                         | <span data-ttu-id="1a393-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a393-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a393-111">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="1a393-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="1a393-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="1a393-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="1a393-113">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1a393-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1a393-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a393-114">Remarks</span></span>

<span data-ttu-id="1a393-115">Informationen zur C++-Entwicklung finden Sie unter [**multipleinhaltungen-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).</span><span class="sxs-lookup"><span data-stu-id="1a393-115">For C++ development, see [**MultipleInstances Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).</span></span>

<span data-ttu-id="1a393-116">Informationen zur Skript Entwicklung finden Sie unter [**Task Settings. multipleinhaltungen**](tasksettings-multipleinstances.md).</span><span class="sxs-lookup"><span data-stu-id="1a393-116">For script development, see [**TaskSettings.MultipleInstances**](tasksettings-multipleinstances.md).</span></span>

### <a name="restricted-values"></a><span data-ttu-id="1a393-117">Eingeschränkte Werte</span><span class="sxs-lookup"><span data-stu-id="1a393-117">Restricted Values</span></span>

<span data-ttu-id="1a393-118">Dieses Element ist auf die folgenden Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="1a393-118">This element is restricted to the following values.</span></span>

-   <span data-ttu-id="1a393-119">Parallel: startet eine neue-Instanz, während eine vorhandene-Instanz ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a393-119">Parallel: Starts a new instance while an existing instance is running.</span></span>
-   <span data-ttu-id="1a393-120">Queue: startet eine neue Instanz der Aufgabe, nachdem alle anderen Instanzen der Aufgabe vollständig sind.</span><span class="sxs-lookup"><span data-stu-id="1a393-120">Queue: Starts a new instance of task after all other instances of the task are complete.</span></span>
-   <span data-ttu-id="1a393-121">Ignorumew: Standardwert.</span><span class="sxs-lookup"><span data-stu-id="1a393-121">IgnoreNew: Default.</span></span> <span data-ttu-id="1a393-122">Startet keine neue Instanz, wenn eine vorhandene Instanz der Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a393-122">Does not start a new instance if an existing instance of the task is running.</span></span>
-   <span data-ttu-id="1a393-123">StopAll: beendet eine vorhandene Instanz der Aufgabe, bevor eine neue Instanz gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1a393-123">StopExisting: Stops an existing instance of the task before it starts a new instance.</span></span>

## <a name="examples"></a><span data-ttu-id="1a393-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a393-124">Examples</span></span>

<span data-ttu-id="1a393-125">Der folgende XML-Code definiert ein settings-Element, das es ermöglicht, mehrere Instanzen der Aufgabe parallel auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1a393-125">The following XML defines a settings element that allows multiple instances of the task to run in parallel.</span></span>


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="1a393-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a393-126">Requirements</span></span>



| <span data-ttu-id="1a393-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a393-127">Requirement</span></span> | <span data-ttu-id="1a393-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1a393-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1a393-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1a393-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1a393-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a393-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1a393-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1a393-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1a393-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a393-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a393-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a393-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a393-134">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="1a393-134">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





