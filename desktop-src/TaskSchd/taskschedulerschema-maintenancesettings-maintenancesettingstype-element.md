---
title: Maintenancesettings-Element (maintenancesettingstype)
description: Gibt an, wie das Taskplaner während der automatischen Wartung Tasks ausführt.
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- Maintenancesettings-Element Taskplaner
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca68876d8742ea04faa972d2ea7fd5f4b2071ffc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105218"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a><span data-ttu-id="41a8a-104">Maintenancesettings-Element (maintenancesettingstype)</span><span class="sxs-lookup"><span data-stu-id="41a8a-104">MaintenanceSettings (maintenanceSettingsType) Element</span></span>

<span data-ttu-id="41a8a-105">Gibt an, wie das Taskplaner während der automatischen Wartung Tasks ausführt.</span><span class="sxs-lookup"><span data-stu-id="41a8a-105">Specifies how the Task Scheduler performs tasks during Automatic maintenance.</span></span>

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="41a8a-106">Das **maintenancesettings** -Element wird durch den komplexen Typ [**maintenancesettingstype**](taskschedulerschema-maintenancesettingstype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="41a8a-106">The **MaintenanceSettings** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="41a8a-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="41a8a-107">Parent element</span></span>



| <span data-ttu-id="41a8a-108">Element</span><span class="sxs-lookup"><span data-stu-id="41a8a-108">Element</span></span>                                                           | <span data-ttu-id="41a8a-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="41a8a-109">Derived from</span></span>                                                         | <span data-ttu-id="41a8a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41a8a-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="41a8a-111">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="41a8a-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="41a8a-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="41a8a-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="41a8a-113">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="41a8a-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="41a8a-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="41a8a-114">Child elements</span></span>



| <span data-ttu-id="41a8a-115">Element</span><span class="sxs-lookup"><span data-stu-id="41a8a-115">Element</span></span>                                                    | <span data-ttu-id="41a8a-116">type</span><span class="sxs-lookup"><span data-stu-id="41a8a-116">Type</span></span>    | <span data-ttu-id="41a8a-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41a8a-117">Description</span></span>                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41a8a-118">**Stichtag**</span><span class="sxs-lookup"><span data-stu-id="41a8a-118">**Deadline**</span></span>](taskschedulerschema-deadline-element.md)   |         | <span data-ttu-id="41a8a-119">Gibt die Zeitspanne an, nach der der Taskplaner versucht, die Aufgabe während der automatischen Notfallwartung zu starten, wenn dieser während der regulären Wartung nicht fertiggestellt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="41a8a-119">Specifies the amount of time after which the Task scheduler will attempt to start task during emergency Automatic maintenance, if it failed to complete during regular maintenance.</span></span> <br/> |
| [<span data-ttu-id="41a8a-120">**Exklusiv**</span><span class="sxs-lookup"><span data-stu-id="41a8a-120">**Exclusive**</span></span>](taskschedulerschema-exclusive-element.md) | <span data-ttu-id="41a8a-121">boolean</span><span class="sxs-lookup"><span data-stu-id="41a8a-121">boolean</span></span> | <span data-ttu-id="41a8a-122">Wenn diese Einstellung auf "true" festgelegt ist, wird die Aufgabe ausschließlich unter anderen Wartungs Tasks gestartet.</span><span class="sxs-lookup"><span data-stu-id="41a8a-122">If set to true, the task will be started exclusively among other maintenance tasks.</span></span> <br/>                                                                                                 |
| [<span data-ttu-id="41a8a-123">**Zeitraum**</span><span class="sxs-lookup"><span data-stu-id="41a8a-123">**Period**</span></span>](taskschedulerschema-period-element.md)       |         | <span data-ttu-id="41a8a-124">Gibt an, wie oft der Task während der automatischen Wartung gestartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="41a8a-124">Specifies how often the task needs to be started during Automatic maintenance.</span></span> <br/>                                                                                                      |



## <a name="remarks"></a><span data-ttu-id="41a8a-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41a8a-125">Remarks</span></span>

<span data-ttu-id="41a8a-126">Bei der C++-Programmierung wird diese Einstellung für den Leerlauf mithilfe der [**ITaskSettings3:: maintenancesettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="41a8a-126">For C++ programming, this idle setting is specified using the [**ITaskSettings3::MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) property.</span></span>

## <a name="examples"></a><span data-ttu-id="41a8a-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41a8a-127">Examples</span></span>

<span data-ttu-id="41a8a-128">Der folgende XML-Code definiert ein Einstellungs Element, das Taskplaner anweist, die Aufgabe einmal in 5 Tagen während der regulären automatischen Wartung auszuführen. wenn 15 Tage lang ein Fehler aufgetreten ist, sollte der Task während der automatischen Notfallwartung gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="41a8a-128">The following XML defines a settings element that instructs Task Scheduler to execute task once in 5 days during regular Automatic maintenance and if failed for 15 days, start attempting the task during the emergency Automatic maintenance.</span></span>


```XML
<Settings>
    <MaintenanceSettings>
        <Period>P5D</Period>
        <Deadline>P15D</Deadline>
    </MaintenanceSettings>       
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="41a8a-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41a8a-129">Requirements</span></span>



| <span data-ttu-id="41a8a-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41a8a-130">Requirement</span></span> | <span data-ttu-id="41a8a-131">Wert</span><span class="sxs-lookup"><span data-stu-id="41a8a-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="41a8a-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41a8a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="41a8a-133">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41a8a-133">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="41a8a-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41a8a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="41a8a-135">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41a8a-135">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41a8a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41a8a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41a8a-137">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="41a8a-137">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="41a8a-138">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="41a8a-138">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





