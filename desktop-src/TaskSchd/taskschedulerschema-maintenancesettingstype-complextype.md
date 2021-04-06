---
title: komplexer maintenancesettingstype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das maintenancesettings-Element.
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- komplexer maintenancesettingstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f261e84fe2af1239cce1bbd377e991ede6e8506
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742761"
---
# <a name="maintenancesettingstype-complex-type"></a><span data-ttu-id="edaf4-104">komplexer maintenancesettingstype-Typ</span><span class="sxs-lookup"><span data-stu-id="edaf4-104">maintenanceSettingsType Complex Type</span></span>

<span data-ttu-id="edaf4-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**maintenancesettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="edaf4-105">Defines the child elements and sequencing information for the [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="maintenanceSettingsType">
    <xs:all>
        <xs:element name="Period"
            minOccurs="1"
            maxOccurs="1"
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
        <xs:element name="Deadline"
            minOccurs="1"
            maxOccurs="1"
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
        <xs:element name="Exclusive"
            type="boolean"
            maxOccurs="1"
            minOccurs="1"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="edaf4-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="edaf4-106">Child elements</span></span>



| <span data-ttu-id="edaf4-107">Element</span><span class="sxs-lookup"><span data-stu-id="edaf4-107">Element</span></span>                                                                        | <span data-ttu-id="edaf4-108">type</span><span class="sxs-lookup"><span data-stu-id="edaf4-108">Type</span></span>    | <span data-ttu-id="edaf4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="edaf4-109">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="edaf4-110">**Stichtag**</span><span class="sxs-lookup"><span data-stu-id="edaf4-110">**Deadline**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | <span data-ttu-id="edaf4-111">Gibt die Zeitspanne an, nach der der Taskplaner versucht, die Aufgabe während der automatischen Notfallwartung zu starten, wenn dieser während der regulären Wartung nicht fertiggestellt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="edaf4-111">Specifies the amount of time after which the Task scheduler will attempt to start task during emergency Automatic maintenance, if it failed to complete during regular maintenance.</span></span><br/> |
| <span data-ttu-id="edaf4-112">**Exklusiv**</span><span class="sxs-lookup"><span data-stu-id="edaf4-112">**Exclusive**</span></span>                                                                  | <span data-ttu-id="edaf4-113">boolean</span><span class="sxs-lookup"><span data-stu-id="edaf4-113">boolean</span></span> | <span data-ttu-id="edaf4-114">Wenn diese Einstellung auf "true" festgelegt ist, wird die Aufgabe ausschließlich unter anderen Wartungs Tasks gestartet.</span><span class="sxs-lookup"><span data-stu-id="edaf4-114">If set to true, the task will be started exclusively among other maintenance tasks.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="edaf4-115">**Zeitraum**</span><span class="sxs-lookup"><span data-stu-id="edaf4-115">**Period**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | <span data-ttu-id="edaf4-116">Gibt an, wie oft der Task während der automatischen Wartung gestartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="edaf4-116">Specifies how often the task needs to be started during Automatic maintenance.</span></span><br/>                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="edaf4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="edaf4-117">Requirements</span></span>



| <span data-ttu-id="edaf4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="edaf4-118">Requirement</span></span> | <span data-ttu-id="edaf4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="edaf4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="edaf4-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="edaf4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="edaf4-121">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="edaf4-121">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="edaf4-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="edaf4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="edaf4-123">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="edaf4-123">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="edaf4-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edaf4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edaf4-125">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="edaf4-125">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="edaf4-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="edaf4-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





