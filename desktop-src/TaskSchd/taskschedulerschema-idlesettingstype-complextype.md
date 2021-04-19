---
title: komplexer idlesettingstype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das idlesettings (settingstype)-Element.
ms.assetid: 0f50c4d6-fda9-42cc-8dab-4c9439fbea4b
keywords:
- komplexer idlesettingstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- idleSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba5ffa3acb879aad095b5b136d882bb817eb0ab0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338133"
---
# <a name="idlesettingstype-complex-type"></a><span data-ttu-id="33477-104">komplexer idlesettingstype-Typ</span><span class="sxs-lookup"><span data-stu-id="33477-104">idleSettingsType Complex Type</span></span>

<span data-ttu-id="33477-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**idlesettings (settingstype)**](taskschedulerschema-idlesettings-settingstype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="33477-105">Defines the child elements and sequencing information for the [**IdleSettings (settingsType)**](taskschedulerschema-idlesettings-settingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="idleSettingsType">
    <xs:all>
        <xs:element name="Duration"
            default="PT10M"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="WaitTimeout"
            default="PT1H"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="StopOnIdleEnd"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="33477-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="33477-106">Child elements</span></span>



| <span data-ttu-id="33477-107">Element</span><span class="sxs-lookup"><span data-stu-id="33477-107">Element</span></span>                                                                                  | <span data-ttu-id="33477-108">type</span><span class="sxs-lookup"><span data-stu-id="33477-108">Type</span></span>    | <span data-ttu-id="33477-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33477-109">Description</span></span>                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33477-110">**Duration**</span><span class="sxs-lookup"><span data-stu-id="33477-110">**Duration**</span></span>](taskschedulerschema-duration-idlesettingstype-element.md)                |         | <span data-ttu-id="33477-111">Gibt die Zeitspanne an, die zum Starten der Aufgabe in einer Leerlauf Bedingung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="33477-111">Specifies the amount of time allowed to start the task while in an idle condition.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="33477-112">**Neustartondle**</span><span class="sxs-lookup"><span data-stu-id="33477-112">**RestartOnIdle**</span></span>](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | <span data-ttu-id="33477-113">boolean</span><span class="sxs-lookup"><span data-stu-id="33477-113">boolean</span></span> | <span data-ttu-id="33477-114">Der Task wird neu gestartet, sobald eine Leerlauf Bedingung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="33477-114">The task is restarted as soon as an idle condition starts.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="33477-115">**Stoponidleend**</span><span class="sxs-lookup"><span data-stu-id="33477-115">**StopOnIdleEnd**</span></span>](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | <span data-ttu-id="33477-116">boolean</span><span class="sxs-lookup"><span data-stu-id="33477-116">boolean</span></span> | <span data-ttu-id="33477-117">Gibt an, dass der Task beendet wird, wenn die Leerlauf Bedingung endet, bevor die Leerlauf Dauer überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="33477-117">Specifies that the task is terminated if the idle condition ends before the idle duration is exceeded.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="33477-118">**WaitTimeout**</span><span class="sxs-lookup"><span data-stu-id="33477-118">**WaitTimeout**</span></span>](taskschedulerschema-waittimeout-idlesettingstype-element.md)          |         | <span data-ttu-id="33477-119">Gibt die Zeitspanne an, die gewartet werden soll, bis eine Leerlauf Bedingung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="33477-119">Specifies the amount of time to wait for an idle condition to start.</span></span> <span data-ttu-id="33477-120">Wenn für dieses Element kein Wert angegeben wird, wartet der Taskplaner-Dienst unbegrenzt, bis eine Leerlauf Bedingung auftritt.</span><span class="sxs-lookup"><span data-stu-id="33477-120">If no value is specified for this element, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="33477-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33477-121">Requirements</span></span>



| <span data-ttu-id="33477-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33477-122">Requirement</span></span> | <span data-ttu-id="33477-123">Wert</span><span class="sxs-lookup"><span data-stu-id="33477-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="33477-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33477-124">Minimum supported client</span></span><br/> | <span data-ttu-id="33477-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33477-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="33477-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33477-126">Minimum supported server</span></span><br/> | <span data-ttu-id="33477-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33477-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="33477-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33477-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33477-129">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="33477-129">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="33477-130">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="33477-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





