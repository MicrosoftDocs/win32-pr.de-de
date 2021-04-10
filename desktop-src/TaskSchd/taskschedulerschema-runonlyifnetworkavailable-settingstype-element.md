---
title: Runonlyifnetworkavailable (settingstype)-Element
description: Gibt an, dass der Taskplaner die Aufgabe nur dann ausgeführt wird, wenn ein Netzwerk verfügbar ist.
ms.assetid: b7b804d3-b31a-4d70-9ba5-805a285e278e
keywords:
- Runonlyifnetworkavailable-Element Taskplaner
topic_type:
- apiref
api_name:
- RunOnlyIfNetworkAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ff1e7c838c142e30b75eb4abb935c0de352d9f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956959"
---
# <a name="runonlyifnetworkavailable-settingstype-element"></a><span data-ttu-id="e1468-104">Runonlyifnetworkavailable (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="e1468-104">RunOnlyIfNetworkAvailable (settingsType) Element</span></span>

<span data-ttu-id="e1468-105">Gibt an, dass der Taskplaner die Aufgabe nur dann ausgeführt wird, wenn ein Netzwerk verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e1468-105">Specifies that the Task Scheduler will run the task only when a network is available.</span></span>

``` syntax
<xs:element name="RunOnlyIfNetworkAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="e1468-106">Das **runonlyifnetworkavailable** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="e1468-106">The **RunOnlyIfNetworkAvailable** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e1468-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="e1468-107">Parent element</span></span>



| <span data-ttu-id="e1468-108">Element</span><span class="sxs-lookup"><span data-stu-id="e1468-108">Element</span></span>                                                           | <span data-ttu-id="e1468-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="e1468-109">Derived from</span></span>                                                         | <span data-ttu-id="e1468-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1468-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1468-111">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="e1468-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="e1468-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="e1468-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="e1468-113">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e1468-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e1468-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1468-114">Remarks</span></span>

<span data-ttu-id="e1468-115">Informationen zur C++-Entwicklung finden Sie unter [**der runonlyifnetworkavailable-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).</span><span class="sxs-lookup"><span data-stu-id="e1468-115">For C++ development, see [**RunOnlyIfNetworkAvailable Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).</span></span>

<span data-ttu-id="e1468-116">Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. runonlyifnetworkavailable**](tasksettings-runonlyifnetworkavailable.md).</span><span class="sxs-lookup"><span data-stu-id="e1468-116">For script development, see [**TaskSettings.RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e1468-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1468-117">Examples</span></span>

<span data-ttu-id="e1468-118">Der folgende XML-Code definiert ein settings-Element, das es ermöglicht, dass der Task nur gestartet wird, wenn ein Netzwerk verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e1468-118">The following XML defines a settings element that allows the task to start only if a network is available.</span></span>


```XML
<Settings>
    <RunOnlyIfNetworkAvailable>true</RunOnlyIfNetworkAvailable>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="e1468-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1468-119">Requirements</span></span>



| <span data-ttu-id="e1468-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1468-120">Requirement</span></span> | <span data-ttu-id="e1468-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e1468-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e1468-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e1468-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e1468-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e1468-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e1468-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e1468-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e1468-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e1468-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e1468-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1468-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1468-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="e1468-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





