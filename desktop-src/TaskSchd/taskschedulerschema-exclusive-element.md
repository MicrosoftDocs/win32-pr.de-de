---
title: Exklusives Element
description: Gibt an, ob der Taskplaner die Aufgabe während der automatischen Wartung im exklusiven Modus starten muss.
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- Exklusives Element Taskplaner
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e0cd7cf5b2a5ce3aa68f92834aa45563000945d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339941"
---
# <a name="exclusive-element"></a><span data-ttu-id="a5264-104">Exklusives Element</span><span class="sxs-lookup"><span data-stu-id="a5264-104">Exclusive Element</span></span>

<span data-ttu-id="a5264-105">Gibt an, ob der Taskplaner die Aufgabe während der automatischen Wartung im exklusiven Modus starten muss.</span><span class="sxs-lookup"><span data-stu-id="a5264-105">Indicates whether the Task scheduler must start the task during the Automatic maintenance in exclusive mode.</span></span>

<span data-ttu-id="a5264-106">Die Exklusivität wird nur zwischen anderen Wartungs Tasks garantiert und erteilt keine Reihenfolge Priorität der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="a5264-106">The exclusivity is guaranteed only between other maintenance tasks and doesn't grant any ordering priority of the task.</span></span> <span data-ttu-id="a5264-107">Wenn die Exklusivität nicht angegeben wird, wird die Aufgabe parallel mit anderen Wartungs Tasks gestartet.</span><span class="sxs-lookup"><span data-stu-id="a5264-107">If exclusivity is not specified, the task is started in parallel with other maintenance tasks.</span></span>

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="a5264-108">Das **exklusive** Element wird durch den komplexen Typ [**maintenancesettingstype**](taskschedulerschema-maintenancesettingstype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="a5264-108">The **Exclusive** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a5264-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="a5264-109">Parent element</span></span>



| <span data-ttu-id="a5264-110">Element</span><span class="sxs-lookup"><span data-stu-id="a5264-110">Element</span></span>                                                                                                                          | <span data-ttu-id="a5264-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="a5264-111">Derived from</span></span>                                                                               | <span data-ttu-id="a5264-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5264-112">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5264-113">**Maintenancesettings (maintenancesettingstype)**</span><span class="sxs-lookup"><span data-stu-id="a5264-113">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="a5264-114">**maintenancesettingstype**</span><span class="sxs-lookup"><span data-stu-id="a5264-114">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="a5264-115">Gibt die Task Einstellungen an, mit denen der Taskplaner während der automatischen Wartung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a5264-115">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a5264-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5264-116">Remarks</span></span>

<span data-ttu-id="a5264-117">Bei der C++-Programmierung wird diese Einstellung für den Leerlauf mithilfe der [**imaintenancesettings:: Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="a5264-117">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) property.</span></span>

## <a name="examples"></a><span data-ttu-id="a5264-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5264-118">Examples</span></span>

<span data-ttu-id="a5264-119">Der folgende XML-Code definiert den Wartungs Task mit der Stichtag Anforderung auf 15 Tage.</span><span class="sxs-lookup"><span data-stu-id="a5264-119">The following XML defines maintenance task with deadline requirement set to 15 days.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
    <Exclusive>true</Exclusive>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="a5264-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5264-120">Requirements</span></span>



| <span data-ttu-id="a5264-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5264-121">Requirement</span></span> | <span data-ttu-id="a5264-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a5264-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a5264-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5264-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a5264-124">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5264-124">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="a5264-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5264-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a5264-126">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5264-126">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5264-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5264-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5264-128">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="a5264-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a5264-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="a5264-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





