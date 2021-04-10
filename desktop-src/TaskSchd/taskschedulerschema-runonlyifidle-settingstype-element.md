---
title: Runonlyifdle (settingstype)-Element
description: Gibt an, dass der Task nur ausgeführt wird, wenn sich der Computer im Leerlauf befindet.
ms.assetid: 2ef3dd19-4d5c-4399-89b8-d737be4ef85e
keywords:
- Runonlyimedle-Element Taskplaner
topic_type:
- apiref
api_name:
- RunOnlyIfIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c57663d763926d68e5a552ebaf66edff2172e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040869"
---
# <a name="runonlyifidle-settingstype-element"></a><span data-ttu-id="17cee-104">Runonlyifdle (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="17cee-104">RunOnlyIfIdle (settingsType) Element</span></span>

<span data-ttu-id="17cee-105">Gibt an, dass der Task nur ausgeführt wird, wenn sich der Computer im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="17cee-105">Specifies that the task is run only when the computer is in an idle state.</span></span>

``` syntax
<xs:element name="RunOnlyIfIdle"
    type="boolean"
 />
```

<span data-ttu-id="17cee-106">Das **runonlyimedle** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="17cee-106">The **RunOnlyIfIdle** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="17cee-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="17cee-107">Parent element</span></span>



| <span data-ttu-id="17cee-108">Element</span><span class="sxs-lookup"><span data-stu-id="17cee-108">Element</span></span>                                                           | <span data-ttu-id="17cee-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="17cee-109">Derived from</span></span>                                                         | <span data-ttu-id="17cee-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17cee-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="17cee-111">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="17cee-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="17cee-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="17cee-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="17cee-113">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="17cee-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="17cee-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17cee-114">Remarks</span></span>

<span data-ttu-id="17cee-115">Informationen zur C++-Entwicklung finden Sie unter [**runonlyimedle-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).</span><span class="sxs-lookup"><span data-stu-id="17cee-115">For C++ development, see [**RunOnlyIfIdle Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).</span></span>

<span data-ttu-id="17cee-116">Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. runonlyifdle**](tasksettings-runonlyifidle.md).</span><span class="sxs-lookup"><span data-stu-id="17cee-116">For script development, see [**TaskSettings.RunOnlyIfIdle**](tasksettings-runonlyifidle.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17cee-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17cee-117">Requirements</span></span>



| <span data-ttu-id="17cee-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17cee-118">Requirement</span></span> | <span data-ttu-id="17cee-119">Wert</span><span class="sxs-lookup"><span data-stu-id="17cee-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="17cee-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17cee-120">Minimum supported client</span></span><br/> | <span data-ttu-id="17cee-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17cee-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="17cee-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17cee-122">Minimum supported server</span></span><br/> | <span data-ttu-id="17cee-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17cee-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="17cee-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17cee-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17cee-125">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="17cee-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="17cee-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="17cee-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





