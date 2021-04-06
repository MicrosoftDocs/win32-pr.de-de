---
title: Volatile-Element
description: Gibt an, ob der Task bei jedem Start von Windows automatisch deaktiviert wird.
ms.assetid: E0298876-2A96-401D-B857-69758AF980E5
keywords:
- Volatile-Element Taskplaner
topic_type:
- apiref
api_name:
- Volatile
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca697bd0dff3a1fffd0b92a29d2fc88f1d4ed433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743313"
---
# <a name="volatile-element"></a><span data-ttu-id="a2fcd-104">Volatile-Element</span><span class="sxs-lookup"><span data-stu-id="a2fcd-104">Volatile Element</span></span>

<span data-ttu-id="a2fcd-105">Gibt an, ob der Task bei jedem Start von Windows automatisch deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="a2fcd-105">Indicates whether the task is automatically disabled every time Windows starts.</span></span>

``` syntax
<xs:element name="Volatile"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
    default="false"
 />
```

<span data-ttu-id="a2fcd-106">Das **volatile** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="a2fcd-106">The **Volatile** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a2fcd-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="a2fcd-107">Parent element</span></span>



| <span data-ttu-id="a2fcd-108">Element</span><span class="sxs-lookup"><span data-stu-id="a2fcd-108">Element</span></span>                                                           | <span data-ttu-id="a2fcd-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="a2fcd-109">Derived from</span></span> | <span data-ttu-id="a2fcd-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2fcd-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2fcd-111">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="a2fcd-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) |              | <span data-ttu-id="a2fcd-112">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a2fcd-112">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a2fcd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2fcd-113">Remarks</span></span>

<span data-ttu-id="a2fcd-114">Bei der C++-Programmierung wird diese Einstellung für den Leerlauf mithilfe der [**ITaskSettings3:: volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="a2fcd-114">For C++ programming, this idle setting is specified using the [**ITaskSettings3::Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2fcd-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2fcd-115">Requirements</span></span>



| <span data-ttu-id="a2fcd-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2fcd-116">Requirement</span></span> | <span data-ttu-id="a2fcd-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a2fcd-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a2fcd-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2fcd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a2fcd-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2fcd-119">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="a2fcd-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2fcd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a2fcd-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2fcd-121">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2fcd-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2fcd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2fcd-123">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="a2fcd-123">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a2fcd-124">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="a2fcd-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





