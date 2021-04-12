---
title: Restartonfailure (settingstype)-Element
description: Gibt an, dass der Taskplaner den Task neu starten soll, wenn die Aufgabe aus irgendeinem Grund fehlschlägt.
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- Restartonfailure-Element Taskplaner
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4239d21362d589cae84252c728387b2a2b6159e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213748"
---
# <a name="restartonfailure-settingstype-element"></a><span data-ttu-id="80adc-104">Restartonfailure (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="80adc-104">RestartOnFailure (settingsType) Element</span></span>

<span data-ttu-id="80adc-105">Gibt an, dass der Taskplaner den Task neu starten soll, wenn die Aufgabe aus irgendeinem Grund fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="80adc-105">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span>

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

<span data-ttu-id="80adc-106">Das **restartonfailure** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="80adc-106">The **RestartOnFailure** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="80adc-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="80adc-107">Parent element</span></span>



| <span data-ttu-id="80adc-108">Element</span><span class="sxs-lookup"><span data-stu-id="80adc-108">Element</span></span>                                                           | <span data-ttu-id="80adc-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="80adc-109">Derived from</span></span>                                                         | <span data-ttu-id="80adc-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80adc-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="80adc-111">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="80adc-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="80adc-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="80adc-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="80adc-113">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="80adc-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="80adc-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="80adc-114">Child elements</span></span>



| <span data-ttu-id="80adc-115">Element</span><span class="sxs-lookup"><span data-stu-id="80adc-115">Element</span></span>                                                              | <span data-ttu-id="80adc-116">type</span><span class="sxs-lookup"><span data-stu-id="80adc-116">Type</span></span>         | <span data-ttu-id="80adc-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80adc-117">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80adc-118">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="80adc-118">**Count**</span></span>](taskschedulerschema-count-restarttype-element.md)       | <span data-ttu-id="80adc-119">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="80adc-119">unsignedByte</span></span> | <span data-ttu-id="80adc-120">Gibt an, wie oft das Taskplaner versucht, den Task neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="80adc-120">Specifies the number of times that the Task Scheduler will attempt to restart the task.</span></span><br/> |
| [<span data-ttu-id="80adc-121">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="80adc-121">**Interval**</span></span>](taskschedulerschema-interval-restarttype-element.md) | <span data-ttu-id="80adc-122">duration</span><span class="sxs-lookup"><span data-stu-id="80adc-122">duration</span></span>     | <span data-ttu-id="80adc-123">Gibt an, wie lange der Taskplaner versucht, den Task neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="80adc-123">Specifies how long the Task Scheduler will attempt to restart the task.</span></span><br/>                 |



## <a name="remarks"></a><span data-ttu-id="80adc-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80adc-124">Remarks</span></span>

<span data-ttu-id="80adc-125">Wenn eine Anwendung Task Einstellungen angibt, erfolgt der Zugriff auf diese Informationen über die Eigenschaften [**restartcount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) und [**restartinterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) der [**itasksettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="80adc-125">When an application specifies task settings, this information is accessed through the [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) and [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) properties of the [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) interface.</span></span> <span data-ttu-id="80adc-126">Bei der Skripterstellung erfolgt der Zugriff auf diese Informationen über die Eigenschaften " [**tasksettings. restartcount**](tasksettings-restartcount.md) " und " [**tasksettings. restartinterval**](tasksettings-restartinterval.md) ".</span><span class="sxs-lookup"><span data-stu-id="80adc-126">For scripting, this information is accessed through the [**TaskSettings.RestartCount**](tasksettings-restartcount.md) and [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md) properties.</span></span>

<span data-ttu-id="80adc-127">Beide untergeordneten Elemente müssen festgelegt werden, um anzugeben, wie die Taskplaner den Task neu startet.</span><span class="sxs-lookup"><span data-stu-id="80adc-127">Both child elements must be set to specify how the Task Scheduler restarts the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="80adc-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80adc-128">Requirements</span></span>



| <span data-ttu-id="80adc-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80adc-129">Requirement</span></span> | <span data-ttu-id="80adc-130">Wert</span><span class="sxs-lookup"><span data-stu-id="80adc-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="80adc-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80adc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="80adc-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80adc-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="80adc-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80adc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="80adc-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80adc-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80adc-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80adc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80adc-136">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="80adc-136">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





