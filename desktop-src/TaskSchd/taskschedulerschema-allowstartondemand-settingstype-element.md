---
title: Allowstartondemand-Element (settingstype)
description: Gibt an, dass der Task entweder über den Befehl ausführen oder über das Kontextmenü gestartet werden kann.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- Allowstartondemand-Element Taskplaner
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec396bf10efbd11024fe39e57bdf05025db0e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949575"
---
# <a name="allowstartondemand-settingstype-element"></a><span data-ttu-id="bdf46-104">Allowstartondemand-Element (settingstype)</span><span class="sxs-lookup"><span data-stu-id="bdf46-104">AllowStartOnDemand (settingsType) Element</span></span>

<span data-ttu-id="bdf46-105">Gibt an, dass der Task entweder über den Befehl ausführen oder über das Kontextmenü gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bdf46-105">Specifies that the task can be started using either the Run command or the Context menu.</span></span>

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

<span data-ttu-id="bdf46-106">Das **allowstartondemand** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="bdf46-106">The **AllowStartOnDemand** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bdf46-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="bdf46-107">Parent element</span></span>



| <span data-ttu-id="bdf46-108">Element</span><span class="sxs-lookup"><span data-stu-id="bdf46-108">Element</span></span>                                                           | <span data-ttu-id="bdf46-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="bdf46-109">Derived from</span></span>                                                         | <span data-ttu-id="bdf46-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdf46-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="bdf46-111">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="bdf46-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="bdf46-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="bdf46-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="bdf46-113">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bdf46-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bdf46-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdf46-114">Remarks</span></span>

<span data-ttu-id="bdf46-115">Wenn dieses Element auf true festgelegt ist, kann der Task unabhängig von gestartet werden, wenn ein Trigger den Task startet.</span><span class="sxs-lookup"><span data-stu-id="bdf46-115">When this element is set to True, the task can be started independently of when any triggers start the task.</span></span>

<span data-ttu-id="bdf46-116">Informationen zur C++-Entwicklung finden Sie unter der [**allowdemandstart-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).</span><span class="sxs-lookup"><span data-stu-id="bdf46-116">For C++ development, see the [**AllowDemandStart property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).</span></span>

<span data-ttu-id="bdf46-117">Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. allowdemandstart**](tasksettings-allowdemandstart.md).</span><span class="sxs-lookup"><span data-stu-id="bdf46-117">For script development, see [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bdf46-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdf46-118">Examples</span></span>

<span data-ttu-id="bdf46-119">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die den Start von Anforderungen ermöglicht, finden Sie unter [time-auslöserbeispiel (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="bdf46-119">For a complete example of the XML for a task that allows demand start, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bdf46-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdf46-120">Requirements</span></span>



| <span data-ttu-id="bdf46-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdf46-121">Requirement</span></span> | <span data-ttu-id="bdf46-122">Wert</span><span class="sxs-lookup"><span data-stu-id="bdf46-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bdf46-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bdf46-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bdf46-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdf46-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bdf46-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bdf46-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bdf46-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdf46-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bdf46-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdf46-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdf46-128">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="bdf46-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





