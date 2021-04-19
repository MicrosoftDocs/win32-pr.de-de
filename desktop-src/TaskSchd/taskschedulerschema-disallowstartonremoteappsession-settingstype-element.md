---
title: Disallowstartonremoteappsession (settingstype)-Element
description: Gibt an, dass der Task nicht gestartet wird, wenn er für die Durchführung in einer lokal (Schiene) lokalen Anwendung ausgelöst wird.
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- Disallowstartonremoteappsession-Element Taskplaner
topic_type:
- apiref
api_name:
- DisallowStartOnRemoteAppSession
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11e3d0a367f2385e78cf1ec56231bbf7632fe05b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342416"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a><span data-ttu-id="41681-104">Disallowstartonremoteappsession (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="41681-104">DisallowStartOnRemoteAppSession (settingsType) Element</span></span>

<span data-ttu-id="41681-105">Gibt an, dass der Task nicht gestartet wird, wenn er für die Durchführung in einer lokal (Schiene) lokalen Anwendung ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="41681-105">Specifies that the task will not be started if triggered to run in a Remote Applications Integrated Locally (RAIL) session.</span></span>

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="41681-106">Das **disallowstartonremoteappsession** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="41681-106">The **DisallowStartOnRemoteAppSession** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="41681-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="41681-107">Parent element</span></span>



| <span data-ttu-id="41681-108">Element</span><span class="sxs-lookup"><span data-stu-id="41681-108">Element</span></span>                                                           | <span data-ttu-id="41681-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="41681-109">Derived from</span></span>                                                         | <span data-ttu-id="41681-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41681-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="41681-111">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="41681-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="41681-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="41681-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="41681-113">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="41681-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="41681-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41681-114">Remarks</span></span>

<span data-ttu-id="41681-115">Die Standardeinstellung für dieses Element ist false.</span><span class="sxs-lookup"><span data-stu-id="41681-115">The default setting for this element is False.</span></span>

<span data-ttu-id="41681-116">Bei der C++-Entwicklung erfolgt der Zugriff auf diese Informationen über die [**ITaskSettings2::D isallowstartonremoteappsession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="41681-116">For C++ development, this information is accessed through the [**ITaskSettings2::DisallowStartOnRemoteAppSession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) property.</span></span>

## <a name="examples"></a><span data-ttu-id="41681-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41681-117">Examples</span></span>

<span data-ttu-id="41681-118">Der folgende XML-Code definiert ein settings-Element, das nicht zulässt, dass der Task gestartet wird, wenn die Aufgabe für die Durchführung in einer Eisenbahn Sitzung ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="41681-118">The following XML defines a settings element that does not allow the task to start if the task is triggered to run in a RAIL session.</span></span>


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="41681-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41681-119">Requirements</span></span>



| <span data-ttu-id="41681-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41681-120">Requirement</span></span> | <span data-ttu-id="41681-121">Wert</span><span class="sxs-lookup"><span data-stu-id="41681-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="41681-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41681-122">Minimum supported client</span></span><br/> | <span data-ttu-id="41681-123">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41681-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="41681-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41681-124">Minimum supported server</span></span><br/> | <span data-ttu-id="41681-125">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41681-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41681-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41681-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41681-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="41681-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





