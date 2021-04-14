---
title: Count (restarttype)-Element
description: Gibt an, wie oft das Taskplaner versucht, den Task neu zu starten.
ms.assetid: 67466c14-c9dd-49c8-a6ed-df7531fc63b8
keywords:
- Count-Element Taskplaner
topic_type:
- apiref
api_name:
- Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 655f636b725e48749540d67710afa57b3c45c89c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475969"
---
# <a name="count-restarttype-element"></a><span data-ttu-id="46220-104">Count (restarttype)-Element</span><span class="sxs-lookup"><span data-stu-id="46220-104">Count (restartType) Element</span></span>

<span data-ttu-id="46220-105">Gibt an, wie oft das Taskplaner versucht, den Task neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="46220-105">Specifies the number of times that the Task Scheduler will attempt to restart the task.</span></span>

``` syntax
<xs:element name="Count">
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="46220-106">Das-Element wird durch den komplexen [**restarttype**](taskschedulerschema-restarttype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="46220-106">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="46220-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="46220-107">Parent element</span></span>



| <span data-ttu-id="46220-108">Element</span><span class="sxs-lookup"><span data-stu-id="46220-108">Element</span></span>                                                                               | <span data-ttu-id="46220-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="46220-109">Derived from</span></span>                                                       | <span data-ttu-id="46220-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46220-110">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46220-111">**Neustartonfailure**</span><span class="sxs-lookup"><span data-stu-id="46220-111">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="46220-112">**neustarttype**</span><span class="sxs-lookup"><span data-stu-id="46220-112">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="46220-113">Gibt an, dass der Taskplaner den Task neu starten soll, wenn die Aufgabe aus irgendeinem Grund fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="46220-113">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="46220-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46220-114">Remarks</span></span>

<span data-ttu-id="46220-115">Wenn dieses Element angegeben ist, muss auch das [**Interval**](taskschedulerschema-interval-restarttype-element.md) -Element angegeben werden, um dem Taskplaner zu zeigen, wie lange versucht werden soll, den Task neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="46220-115">If this element is specified, the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element must also be specified to tell the Task Scheduler how long to attempt to restart the task.</span></span>

<span data-ttu-id="46220-116">Informationen zur C++-Entwicklung finden Sie unter [**restartcount-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).</span><span class="sxs-lookup"><span data-stu-id="46220-116">For C++ development, see [**RestartCount Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).</span></span>

<span data-ttu-id="46220-117">Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. restartcount**](tasksettings-restartcount.md).</span><span class="sxs-lookup"><span data-stu-id="46220-117">For script development, see [**TaskSettings.RestartCount**](tasksettings-restartcount.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46220-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46220-118">Requirements</span></span>



| <span data-ttu-id="46220-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46220-119">Requirement</span></span> | <span data-ttu-id="46220-120">Wert</span><span class="sxs-lookup"><span data-stu-id="46220-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="46220-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46220-121">Minimum supported client</span></span><br/> | <span data-ttu-id="46220-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46220-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="46220-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46220-123">Minimum supported server</span></span><br/> | <span data-ttu-id="46220-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46220-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46220-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46220-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46220-126">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="46220-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





