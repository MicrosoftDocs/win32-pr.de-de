---
title: Stopifgoingonakkus-Element (settingstype)
description: Gibt an, dass der Task angehalten wird, wenn der Computer auf die Batterie geht.
ms.assetid: 0d772dbb-a552-45ed-9dc0-7159f6ef12ed
keywords:
- Stopifgoingonakkus-Element Taskplaner
topic_type:
- apiref
api_name:
- StopIfGoingOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7de57cde928760c15dd671010880e824c8979f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340777"
---
# <a name="stopifgoingonbatteries-settingstype-element"></a><span data-ttu-id="f041f-104">Stopifgoingonakkus-Element (settingstype)</span><span class="sxs-lookup"><span data-stu-id="f041f-104">StopIfGoingOnBatteries (settingsType) Element</span></span>

<span data-ttu-id="f041f-105">Gibt an, dass der Task angehalten wird, wenn der Computer auf die Batterie geht.</span><span class="sxs-lookup"><span data-stu-id="f041f-105">Specifies that the task will be stopped if the computer is going onto batteries.</span></span>

``` syntax
<xs:element name="StopIfGoingOnBatteries"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

<span data-ttu-id="f041f-106">Das **stopifgoingonakkus** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="f041f-106">The **StopIfGoingOnBatteries** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f041f-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f041f-107">Parent element</span></span>



| <span data-ttu-id="f041f-108">Element</span><span class="sxs-lookup"><span data-stu-id="f041f-108">Element</span></span>                                                           | <span data-ttu-id="f041f-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="f041f-109">Derived from</span></span>                                                         | <span data-ttu-id="f041f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f041f-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="f041f-111">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="f041f-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="f041f-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="f041f-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="f041f-113">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f041f-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f041f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f041f-114">Remarks</span></span>

<span data-ttu-id="f041f-115">Die Standardeinstellung für dieses Element ist false.</span><span class="sxs-lookup"><span data-stu-id="f041f-115">The default setting for this element is False.</span></span> <span data-ttu-id="f041f-116">Beachten Sie, dass sich der Standardwert gegenüber früheren Versionen von Taskplaner geändert hat.</span><span class="sxs-lookup"><span data-stu-id="f041f-116">Note that the default value has changed from previous versions of Task Scheduler.</span></span>

<span data-ttu-id="f041f-117">Bei der Skripterstellung wird diese Einstellung mithilfe der [**Task Settings. stopifgoingonakkus**](tasksettings-stopifgoingonbatteries.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="f041f-117">For scripting development, this setting is specified using the [**TaskSettings.StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md) property.</span></span>

<span data-ttu-id="f041f-118">Bei der C++-Entwicklung wird diese Einstellung mithilfe der [**itasksettings:: stopifgoingonakkus**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="f041f-118">For C++ development, this setting is specified using the [**ITaskSettings::StopIfGoingOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) property.</span></span>

## <a name="examples"></a><span data-ttu-id="f041f-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f041f-119">Examples</span></span>

<span data-ttu-id="f041f-120">Der folgende XML-Code definiert ein settings-Element, das eine harte Beendigung der Aufgabe ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="f041f-120">The following XML defines a settings element that allows a hard termination of the task.</span></span>


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="f041f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f041f-121">Requirements</span></span>



| <span data-ttu-id="f041f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f041f-122">Requirement</span></span> | <span data-ttu-id="f041f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f041f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f041f-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f041f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f041f-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f041f-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f041f-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f041f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f041f-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f041f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f041f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f041f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f041f-129">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="f041f-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





