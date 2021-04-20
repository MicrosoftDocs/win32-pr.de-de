---
title: Interval (restartType)-Element
description: Gibt an, wie lange der Taskplaner versucht, den Task neu zu starten.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
keywords:
- Interval-Taskplaner
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e731582364df23bdef800ab5d2cf15dd5c882ae
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734185"
---
# <a name="interval-restarttype-element"></a><span data-ttu-id="95ebc-104">Interval (restartType)-Element</span><span class="sxs-lookup"><span data-stu-id="95ebc-104">Interval (restartType) Element</span></span>

<span data-ttu-id="95ebc-105">Gibt an, wie lange der Taskplaner versucht, den Task neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="95ebc-105">Specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="95ebc-106">Das Format für diese Zeichenfolge ist (z. B. `P<days>DT<hours>H<minutes>M<seconds>S` ist "PT5M" 5 Minuten, "PT1H" ist 1 Stunde und "PT20M" beträgt 20 Minuten).</span><span class="sxs-lookup"><span data-stu-id="95ebc-106">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="95ebc-107">Die maximal zulässige Zeit beträgt 31 Tage, und die zulässige Mindestzeit beträgt 1 Minute.</span><span class="sxs-lookup"><span data-stu-id="95ebc-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="95ebc-108">Das -Element wird durch den komplexen [**restartType-Typ**](taskschedulerschema-restarttype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="95ebc-108">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="95ebc-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="95ebc-109">Parent element</span></span>



| <span data-ttu-id="95ebc-110">Element</span><span class="sxs-lookup"><span data-stu-id="95ebc-110">Element</span></span>                                                                               | <span data-ttu-id="95ebc-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="95ebc-111">Derived from</span></span>                                                       | <span data-ttu-id="95ebc-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95ebc-112">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95ebc-113">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="95ebc-113">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="95ebc-114">**restartType**</span><span class="sxs-lookup"><span data-stu-id="95ebc-114">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="95ebc-115">Gibt an, dass der Taskplaner versucht, den Task neu zu starten, wenn der Task aus irgendeinem Grund fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="95ebc-115">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="95ebc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95ebc-116">Remarks</span></span>

<span data-ttu-id="95ebc-117">Wenn dieses Element angegeben wird, muss auch [**das Count-Element**](taskschedulerschema-count-restarttype-element.md) angegeben werden, um dem Benutzer Taskplaner, wie oft versucht werden soll, den Task neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="95ebc-117">If this element is specified, the [**Count**](taskschedulerschema-count-restarttype-element.md) element must also be specified to tell the Task Scheduler how many times it should try to restart the task.</span></span>

<span data-ttu-id="95ebc-118">Informationen zur C++-Entwicklung finden Sie unter [**RestartInterval-Eigenschaft von ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval)</span><span class="sxs-lookup"><span data-stu-id="95ebc-118">For C++ development, see [**RestartInterval Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).</span></span>

<span data-ttu-id="95ebc-119">Informationen zur Skriptentwicklung finden Sie [**unter TaskSettings.RestartInterval**](tasksettings-restartinterval.md).</span><span class="sxs-lookup"><span data-stu-id="95ebc-119">For script development, see [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95ebc-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95ebc-120">Requirements</span></span>



| <span data-ttu-id="95ebc-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95ebc-121">Requirement</span></span> | <span data-ttu-id="95ebc-122">Wert</span><span class="sxs-lookup"><span data-stu-id="95ebc-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="95ebc-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95ebc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="95ebc-124">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95ebc-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="95ebc-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95ebc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="95ebc-126">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95ebc-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="95ebc-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="95ebc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95ebc-128">Taskplaner Schemaelemente</span><span class="sxs-lookup"><span data-stu-id="95ebc-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





