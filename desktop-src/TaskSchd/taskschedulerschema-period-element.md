---
title: Period-Element
description: Gibt an, wie oft der Task während der automatischen Wartung gestartet werden muss.
ms.assetid: E4BE2466-3119-41F8-8238-4627C28B26E5
keywords:
- Period-Element Taskplaner
topic_type:
- apiref
api_name:
- Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a507a9b0a8f97d1ae4e6c8df654a45d67b77767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479230"
---
# <a name="period-element"></a><span data-ttu-id="cf0be-104">Period-Element</span><span class="sxs-lookup"><span data-stu-id="cf0be-104">Period Element</span></span>

<span data-ttu-id="cf0be-105">Gibt an, wie oft der Task während der automatischen Wartung gestartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="cf0be-105">Specifies how often the task needs to be started during Automatic maintenance.</span></span>

<span data-ttu-id="cf0be-106">Das Format dieser Zeichenfolge ist " *pnynmndtnhnmns*", wobei " *NY* " die Anzahl von Jahren ist. "nm" ist die Anzahl von Monaten, " *ND* " die Anzahl von Tagen, " *T* " das Trennzeichen für Datum/Uhrzeit, " *NH* " die Anzahl von Stunden, " *nm* " die Anzahl der Minuten und " *NS* " die Anzahl von Sekunden (z. b. "PT5M" gibt 5 Minuten an und "P1M4DT2H5M" einen Monat, vier Tage, zwei Stunden und fünf Minuten)</span><span class="sxs-lookup"><span data-stu-id="cf0be-106">The format for this string is *PnYnMnDTnHnMnS*, where *nY* is the number of years, nM is the number of months, *nD* is the number of days, *T* is the date/time separator, *nH* is the number of hours, *nM* is the number of minutes, and *nS* is the number of seconds (for example, "PT5M" specifies 5 minutes and "P1M4DT2H5M" specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="cf0be-107">Der Mindestwert ist eine Minute.</span><span class="sxs-lookup"><span data-stu-id="cf0be-107">The minimum value is one minute.</span></span> <span data-ttu-id="cf0be-108">Weitere Informationen zum Duration-Typ finden Sie unter [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span><span class="sxs-lookup"><span data-stu-id="cf0be-108">For more information about the duration type, see [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span></span>

``` syntax
<xs:element name="Period"
    maxOccurs="1"
    minOccurs="1"
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

<span data-ttu-id="cf0be-109">Das **Period** -Element wird durch den komplexen Typ [**maintenancesettingstype**](taskschedulerschema-maintenancesettingstype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="cf0be-109">The **Period** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cf0be-110">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="cf0be-110">Parent element</span></span>



| <span data-ttu-id="cf0be-111">Element</span><span class="sxs-lookup"><span data-stu-id="cf0be-111">Element</span></span>                                                                                                                          | <span data-ttu-id="cf0be-112">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="cf0be-112">Derived from</span></span>                                                                               | <span data-ttu-id="cf0be-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf0be-113">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf0be-114">**Maintenancesettings (maintenancesettingstype)**</span><span class="sxs-lookup"><span data-stu-id="cf0be-114">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="cf0be-115">**maintenancesettingstype**</span><span class="sxs-lookup"><span data-stu-id="cf0be-115">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="cf0be-116">Gibt die Task Einstellungen an, mit denen der Taskplaner während der automatischen Wartung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="cf0be-116">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cf0be-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf0be-117">Remarks</span></span>

<span data-ttu-id="cf0be-118">Bei der C++-Programmierung wird diese Einstellung für den Leerlauf mithilfe der [**imaintenancesettings::P eriod**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="cf0be-118">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Period**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) property.</span></span>

## <a name="examples"></a><span data-ttu-id="cf0be-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf0be-119">Examples</span></span>

<span data-ttu-id="cf0be-120">Der folgende XML-Code definiert einen Wartungs Task, bei dem periodizitäts Anforderungen auf 5 Tage festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="cf0be-120">The following XML defines maintenance task with periodicity requirement set to 5 days.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="cf0be-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf0be-121">Requirements</span></span>



| <span data-ttu-id="cf0be-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf0be-122">Requirement</span></span> | <span data-ttu-id="cf0be-123">Wert</span><span class="sxs-lookup"><span data-stu-id="cf0be-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cf0be-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf0be-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cf0be-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf0be-125">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="cf0be-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf0be-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cf0be-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf0be-127">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf0be-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf0be-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf0be-129">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="cf0be-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="cf0be-130">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="cf0be-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





