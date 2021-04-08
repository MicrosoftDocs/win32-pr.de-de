---
title: Disallowstartifonakkus (settingstype)-Element
description: Gibt an, dass der Task nicht gestartet wird, wenn der Computer unter "Akkus" ausgeführt wird.
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- Disallowstartifonakkus-Element Taskplaner
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a8d93bcabd0e121c44f4a7212d11491624a08d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743776"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a><span data-ttu-id="43d44-104">Disallowstartifonakkus (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="43d44-104">DisallowStartIfOnBatteries (settingsType) Element</span></span>

<span data-ttu-id="43d44-105">Gibt an, dass der Task nicht gestartet wird, wenn der Computer unter "Akkus" ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43d44-105">Specifies that the task will not be started if the computer is running on batteries.</span></span>

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

<span data-ttu-id="43d44-106">Das **disallowstartifonakkus** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="43d44-106">The **DisallowStartIfOnBatteries** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="43d44-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="43d44-107">Parent element</span></span>



| <span data-ttu-id="43d44-108">Element</span><span class="sxs-lookup"><span data-stu-id="43d44-108">Element</span></span>                                                           | <span data-ttu-id="43d44-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="43d44-109">Derived from</span></span>                                                         | <span data-ttu-id="43d44-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43d44-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="43d44-111">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="43d44-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="43d44-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="43d44-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="43d44-113">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="43d44-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="43d44-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43d44-114">Remarks</span></span>

<span data-ttu-id="43d44-115">Die Standardeinstellung für dieses Element ist "true".</span><span class="sxs-lookup"><span data-stu-id="43d44-115">The default setting for this element is True.</span></span>

<span data-ttu-id="43d44-116">Bei der Skripterstellung erfolgt der Zugriff auf diese Informationen über die [**tasksettings. disallowstartifonakkus**](tasksettings-disallowstartifonbatteries.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="43d44-116">For scripting development, this information is accessed through the [**TaskSettings.DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) property.</span></span>

<span data-ttu-id="43d44-117">Bei der C++-Entwicklung erfolgt der Zugriff auf diese Informationen über die Eigenschaft [**itasksettings::D isallowstartifonakkus**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) .</span><span class="sxs-lookup"><span data-stu-id="43d44-117">For C++ development, this information is accessed through the [**ITaskSettings::DisallowStartIfOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) property.</span></span>

## <a name="examples"></a><span data-ttu-id="43d44-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43d44-118">Examples</span></span>

<span data-ttu-id="43d44-119">Der folgende XML-Code definiert ein settings-Element, das nicht zulässt, dass der Task ausgeführt wird, wenn der Computer unter Akkus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43d44-119">The following XML defines a settings element that does not allow the task to run if the computer is running on batteries.</span></span>


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="43d44-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43d44-120">Requirements</span></span>



| <span data-ttu-id="43d44-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43d44-121">Requirement</span></span> | <span data-ttu-id="43d44-122">Wert</span><span class="sxs-lookup"><span data-stu-id="43d44-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="43d44-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43d44-123">Minimum supported client</span></span><br/> | <span data-ttu-id="43d44-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43d44-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="43d44-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43d44-125">Minimum supported server</span></span><br/> | <span data-ttu-id="43d44-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43d44-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43d44-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43d44-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d44-128">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="43d44-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





