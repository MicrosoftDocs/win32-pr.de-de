---
title: Stichtag-Element
description: Gibt an, wann der Taskplaner den Task während der automatischen Notfallwartung starten muss, wenn er während der regulären automatischen Wartung nicht fertiggestellt werden konnte.
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- Stichtag Element Taskplaner
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e12524971e8b713d4d17817a8a7c7602017bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740832"
---
# <a name="deadline-element"></a><span data-ttu-id="9235d-104">Stichtag-Element</span><span class="sxs-lookup"><span data-stu-id="9235d-104">Deadline Element</span></span>

<span data-ttu-id="9235d-105">Gibt an, wann der Taskplaner den Task während der automatischen Notfallwartung starten muss, wenn er während der regulären automatischen Wartung nicht fertiggestellt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="9235d-105">Specifies when the Task scheduler must to start the task during emergency Automatic maintenance, if it failed to complete during regular Automatic maintenance.</span></span>

<span data-ttu-id="9235d-106">Das Format dieser Zeichenfolge ist " *pnynmndtnhnmns*", wobei " *NY* " die Anzahl von Jahren ist. "nm" ist die Anzahl von Monaten, " *ND* " die Anzahl von Tagen, " *T* " das Trennzeichen für Datum/Uhrzeit, " *NH* " die Anzahl von Stunden, " *nm* " die Anzahl der Minuten und " *NS* " die Anzahl von Sekunden (z. b. "PT5M" gibt 5 Minuten an und "P1M4DT2H5M" einen Monat, vier Tage, zwei Stunden und fünf Minuten)</span><span class="sxs-lookup"><span data-stu-id="9235d-106">The format for this string is *PnYnMnDTnHnMnS*, where *nY* is the number of years, nM is the number of months, *nD* is the number of days, *T* is the date/time separator, *nH* is the number of hours, *nM* is the number of minutes, and *nS* is the number of seconds (for example, "PT5M" specifies 5 minutes and "P1M4DT2H5M" specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="9235d-107">Der Mindestwert ist eine Minute.</span><span class="sxs-lookup"><span data-stu-id="9235d-107">The minimum value is one minute.</span></span> <span data-ttu-id="9235d-108">Weitere Informationen zum Duration-Typ finden Sie unter [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span><span class="sxs-lookup"><span data-stu-id="9235d-108">For more information about the duration type, see [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span></span> <span data-ttu-id="9235d-109">Der minimale Stichtag, den ein Task verwenden kann, ist 1 Tag.</span><span class="sxs-lookup"><span data-stu-id="9235d-109">Minimum Deadline a task can use is 1 day.</span></span> <span data-ttu-id="9235d-110">Der Wert des stichtelementes muss größer als der Wert des [**Period**](taskschedulerschema-period-element.md) **-Elements sein** .</span><span class="sxs-lookup"><span data-stu-id="9235d-110">The value of the **Deadline** element should be greater than the value of the [**Period**](taskschedulerschema-period-element.md) element.</span></span> <span data-ttu-id="9235d-111">Wenn der Stichtag nicht angegeben wird, wird der Task während der automatischen Notfallwartung nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="9235d-111">If the deadline is not specified the task will not be started during emergency Automatic maintenance.</span></span>

``` syntax
<xs:element name="Deadline"
    maxOccurs="1"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="P1D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="9235d-112">Das **Stichtag** -Element wird durch den komplexen Typ [**maintenancesettingstype**](taskschedulerschema-maintenancesettingstype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="9235d-112">The **Deadline** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9235d-113">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="9235d-113">Parent element</span></span>



| <span data-ttu-id="9235d-114">Element</span><span class="sxs-lookup"><span data-stu-id="9235d-114">Element</span></span>                                                                                                                          | <span data-ttu-id="9235d-115">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="9235d-115">Derived from</span></span>                                                                               | <span data-ttu-id="9235d-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9235d-116">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9235d-117">**Maintenancesettings (maintenancesettingstype)**</span><span class="sxs-lookup"><span data-stu-id="9235d-117">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="9235d-118">**maintenancesettingstype**</span><span class="sxs-lookup"><span data-stu-id="9235d-118">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="9235d-119">Gibt die Task Einstellungen an, mit denen der Taskplaner während der automatischen Wartung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="9235d-119">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9235d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9235d-120">Remarks</span></span>

<span data-ttu-id="9235d-121">Bei der C++-Programmierung wird diese Einstellung für den Leerlauf mithilfe der [**imaintenancesettings::D eadline**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="9235d-121">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Deadline**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) property.</span></span>

## <a name="examples"></a><span data-ttu-id="9235d-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9235d-122">Examples</span></span>

<span data-ttu-id="9235d-123">Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im März ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9235d-123">The following XML defines a months calendar that runs the task in March.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="9235d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9235d-124">Requirements</span></span>



| <span data-ttu-id="9235d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9235d-125">Requirement</span></span> | <span data-ttu-id="9235d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="9235d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9235d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9235d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9235d-128">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9235d-128">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="9235d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9235d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9235d-130">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9235d-130">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9235d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9235d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9235d-132">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="9235d-132">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="9235d-133">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="9235d-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





