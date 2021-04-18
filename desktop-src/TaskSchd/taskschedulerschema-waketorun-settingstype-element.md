---
title: Waketor (settingstype)-Element
description: Gibt an, dass der Computer von Taskplaner reaktiviert wird, wenn der Task ausgeführt werden soll.
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- Waketor-Element Taskplaner
topic_type:
- apiref
api_name:
- WakeToRun
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23eeaa06073fa9259c1a48137cf3676baa402d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341029"
---
# <a name="waketorun-settingstype-element"></a><span data-ttu-id="4f264-104">Waketor (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="4f264-104">WakeToRun (settingsType) Element</span></span>

<span data-ttu-id="4f264-105">Gibt an, dass der Computer von Taskplaner reaktiviert wird, wenn der Task ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f264-105">Specifies that Task Scheduler will wake the computer when it is time to run the task.</span></span>

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

<span data-ttu-id="4f264-106">Das **waketor-** Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="4f264-106">The **WakeToRun** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4f264-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="4f264-107">Parent element</span></span>



| <span data-ttu-id="4f264-108">Element</span><span class="sxs-lookup"><span data-stu-id="4f264-108">Element</span></span>                                                           | <span data-ttu-id="4f264-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="4f264-109">Derived from</span></span>                                                         | <span data-ttu-id="4f264-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f264-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f264-111">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="4f264-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="4f264-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="4f264-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="4f264-113">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4f264-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4f264-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f264-114">Remarks</span></span>

<span data-ttu-id="4f264-115">Wenn der Taskplaner-Dienst den Computer zum Ausführen einer Aufgabe aktiviert, bleibt der Bildschirm möglicherweise deaktiviert, auch wenn sich der Computer nicht mehr im Standbymodus oder Ruhezustand befindet.</span><span class="sxs-lookup"><span data-stu-id="4f264-115">When the Task Scheduler service wakes the computer to run a task, the screen may remain off even though the computer is no longer in the sleep or hibernate mode.</span></span> <span data-ttu-id="4f264-116">Der Bildschirm wird eingeschaltet, wenn Windows Vista erkennt, dass ein Benutzer die Verwendung des Computers zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="4f264-116">The screen will turn on when Windows Vista detects that a user has returned to use the computer.</span></span>

<span data-ttu-id="4f264-117">Informationen zur C++-Entwicklung finden Sie unter [**der Eigenschaft "waketor" von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).</span><span class="sxs-lookup"><span data-stu-id="4f264-117">For C++ development, see [**WakeToRun Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).</span></span>

<span data-ttu-id="4f264-118">Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. wakescripun**](tasksettings-waketorun.md).</span><span class="sxs-lookup"><span data-stu-id="4f264-118">For script development, see [**TaskSettings.WakeToRun**](tasksettings-waketorun.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f264-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f264-119">Requirements</span></span>



| <span data-ttu-id="4f264-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f264-120">Requirement</span></span> | <span data-ttu-id="4f264-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4f264-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4f264-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f264-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4f264-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f264-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4f264-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f264-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4f264-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f264-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f264-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f264-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f264-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="4f264-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="4f264-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="4f264-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





