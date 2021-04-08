---
title: Interval (restarttype)-Element
description: Gibt an, wie lange der Taskplaner versucht, den Task neu zu starten.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
keywords:
- Interval-Element Taskplaner
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c97e754e0b29a43d6ba419bd806404fe1b85b2b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949517"
---
# <a name="interval-restarttype-element"></a><span data-ttu-id="1acbc-104">Interval (restarttype)-Element</span><span class="sxs-lookup"><span data-stu-id="1acbc-104">Interval (restartType) Element</span></span>

<span data-ttu-id="1acbc-105">Gibt an, wie lange der Taskplaner versucht, den Task neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="1acbc-105">Specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="1acbc-106">Das Format für diese Zeichenfolge ist P <days> dt <hours> H <minutes> M <seconds> S ("PT5M" ist beispielsweise 5 Minuten, "PT1H" ist 1 Stunde, und "PT20M" beträgt 20 Minuten).</span><span class="sxs-lookup"><span data-stu-id="1acbc-106">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="1acbc-107">Die maximal zulässige Dauer beträgt 31 Tage, und die zulässige Mindestanzahl beträgt 1 Minute.</span><span class="sxs-lookup"><span data-stu-id="1acbc-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

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

<span data-ttu-id="1acbc-108">Das-Element wird durch den komplexen [**restarttype**](taskschedulerschema-restarttype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="1acbc-108">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1acbc-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1acbc-109">Parent element</span></span>



| <span data-ttu-id="1acbc-110">Element</span><span class="sxs-lookup"><span data-stu-id="1acbc-110">Element</span></span>                                                                               | <span data-ttu-id="1acbc-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="1acbc-111">Derived from</span></span>                                                       | <span data-ttu-id="1acbc-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1acbc-112">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1acbc-113">**Neustartonfailure**</span><span class="sxs-lookup"><span data-stu-id="1acbc-113">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="1acbc-114">**neustarttype**</span><span class="sxs-lookup"><span data-stu-id="1acbc-114">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="1acbc-115">Gibt an, dass der Taskplaner den Task neu starten soll, wenn die Aufgabe aus irgendeinem Grund fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="1acbc-115">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1acbc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1acbc-116">Remarks</span></span>

<span data-ttu-id="1acbc-117">Wenn dieses Element angegeben ist, muss auch das [**count**](taskschedulerschema-count-restarttype-element.md) -Element angegeben werden, um den Taskplaner anzugeben, wie oft versucht werden soll, den Task neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="1acbc-117">If this element is specified, the [**Count**](taskschedulerschema-count-restarttype-element.md) element must also be specified to tell the Task Scheduler how many times it should try to restart the task.</span></span>

<span data-ttu-id="1acbc-118">Informationen zur C++-Entwicklung finden Sie unter [**restartinterval-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).</span><span class="sxs-lookup"><span data-stu-id="1acbc-118">For C++ development, see [**RestartInterval Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).</span></span>

<span data-ttu-id="1acbc-119">Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. restartinterval**](tasksettings-restartinterval.md).</span><span class="sxs-lookup"><span data-stu-id="1acbc-119">For script development, see [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1acbc-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1acbc-120">Requirements</span></span>



| <span data-ttu-id="1acbc-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1acbc-121">Requirement</span></span> | <span data-ttu-id="1acbc-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1acbc-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1acbc-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1acbc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1acbc-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1acbc-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1acbc-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1acbc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1acbc-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1acbc-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1acbc-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1acbc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1acbc-128">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="1acbc-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





