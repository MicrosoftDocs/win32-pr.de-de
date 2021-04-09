---
title: Starteinavailable (settingstype)-Element
description: Gibt an, dass die Taskplaner die Aufgabe jederzeit starten kann, nachdem die geplante Zeit abgelaufen ist.
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- Startstartbare Element Taskplaner
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d86f6f6e75457d08e10ef40d728eaf3e3b00aa7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949572"
---
# <a name="startwhenavailable-settingstype-element"></a><span data-ttu-id="64ee7-104">Starteinavailable (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="64ee7-104">StartWhenAvailable (settingsType) Element</span></span>

<span data-ttu-id="64ee7-105">Gibt an, dass die Taskplaner die Aufgabe jederzeit starten kann, nachdem die geplante Zeit abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="64ee7-105">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span>

``` syntax
<xs:element name="StartWhenAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="64ee7-106">Das **starteinavailable** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="64ee7-106">The **StartWhenAvailable** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="64ee7-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="64ee7-107">Parent element</span></span>



| <span data-ttu-id="64ee7-108">Element</span><span class="sxs-lookup"><span data-stu-id="64ee7-108">Element</span></span>                                                           | <span data-ttu-id="64ee7-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="64ee7-109">Derived from</span></span>                                                         | <span data-ttu-id="64ee7-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64ee7-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="64ee7-111">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="64ee7-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="64ee7-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="64ee7-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="64ee7-113">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="64ee7-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="64ee7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64ee7-114">Remarks</span></span>

<span data-ttu-id="64ee7-115">Diese Eigenschaft gilt nur für zeitgesteuerte Tasks.</span><span class="sxs-lookup"><span data-stu-id="64ee7-115">This property applies only to timed tasks.</span></span>

<span data-ttu-id="64ee7-116">Informationen zur C++-Entwicklung finden Sie unter [**Start-verfügbare Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).</span><span class="sxs-lookup"><span data-stu-id="64ee7-116">For C++ development, see [**StartWhenAvailable Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).</span></span>

<span data-ttu-id="64ee7-117">Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. start\available**](tasksettings-startwhenavailable.md).</span><span class="sxs-lookup"><span data-stu-id="64ee7-117">For script development, see [**TaskSettings.StartWhenAvailable**](tasksettings-startwhenavailable.md).</span></span>

## <a name="examples"></a><span data-ttu-id="64ee7-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64ee7-118">Examples</span></span>

<span data-ttu-id="64ee7-119">Der folgende XML-Code definiert ein settings-Element, das dem Taskplaner ermöglicht, die Aufgabe zu starten, wenn Sie verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="64ee7-119">The following XML defines a settings element that allows the Task Scheduler to start the task when it is available.</span></span>


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="64ee7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64ee7-120">Requirements</span></span>



| <span data-ttu-id="64ee7-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64ee7-121">Requirement</span></span> | <span data-ttu-id="64ee7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="64ee7-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="64ee7-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64ee7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="64ee7-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64ee7-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="64ee7-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64ee7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="64ee7-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64ee7-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64ee7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64ee7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64ee7-128">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="64ee7-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





