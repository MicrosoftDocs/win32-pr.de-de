---
title: Useunimeschedulingengine (settingstype)-Element
description: Gibt an, dass die vereinheitlichte Planungs-Engine verwendet wird, um diese Aufgabe auszuführen.
ms.assetid: 93436f14-1caf-4ec8-bf74-a198b7dcb27c
keywords:
- Useunifedschedulingengine-Element Taskplaner
topic_type:
- apiref
api_name:
- UseUnifiedSchedulingEngine
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a00798a46df3dfbb351dd8705b264192c38daff6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040392"
---
# <a name="useunifiedschedulingengine-settingstype-element"></a><span data-ttu-id="f8a9f-104">Useunimeschedulingengine (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="f8a9f-104">UseUnifiedSchedulingEngine (settingsType) Element</span></span>

<span data-ttu-id="f8a9f-105">Gibt an, dass die vereinheitlichte Planungs-Engine verwendet wird, um diese Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f8a9f-105">Specifies that the Unified Scheduling Engine will be used to run this task.</span></span>

``` syntax
<xs:element name="UseUnifiedSchedulingEngine"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="f8a9f-106">Das **useunifedschedulingengine** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="f8a9f-106">The **UseUnifiedSchedulingEngine** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f8a9f-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f8a9f-107">Parent element</span></span>



| <span data-ttu-id="f8a9f-108">Element</span><span class="sxs-lookup"><span data-stu-id="f8a9f-108">Element</span></span>                                                           | <span data-ttu-id="f8a9f-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="f8a9f-109">Derived from</span></span>                                                         | <span data-ttu-id="f8a9f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8a9f-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8a9f-111">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="f8a9f-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="f8a9f-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="f8a9f-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="f8a9f-113">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f8a9f-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f8a9f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8a9f-114">Remarks</span></span>

<span data-ttu-id="f8a9f-115">Die Standardeinstellung für dieses Element ist false.</span><span class="sxs-lookup"><span data-stu-id="f8a9f-115">The default setting for this element is False.</span></span>

<span data-ttu-id="f8a9f-116">Bei der C++-Entwicklung erfolgt der Zugriff auf diese Informationen über die [**ITaskSettings2:: useunifedschedulingengine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f8a9f-116">For C++ development, this information is accessed through the [**ITaskSettings2::UseUnifiedSchedulingEngine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) property.</span></span>

## <a name="examples"></a><span data-ttu-id="f8a9f-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8a9f-117">Examples</span></span>

<span data-ttu-id="f8a9f-118">Der folgende XML-Code definiert ein settings-Element, das angibt, dass das vereinheitlichte Planungs Modul zum Ausführen dieser Aufgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f8a9f-118">The following XML defines a settings element that specifies that the Unified Scheduling Engine will be used to run this task.</span></span>


```XML
<Settings>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="f8a9f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8a9f-119">Requirements</span></span>



| <span data-ttu-id="f8a9f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8a9f-120">Requirement</span></span> | <span data-ttu-id="f8a9f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f8a9f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f8a9f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8a9f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a9f-123">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8a9f-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f8a9f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8a9f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a9f-125">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8a9f-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f8a9f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8a9f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a9f-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="f8a9f-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





