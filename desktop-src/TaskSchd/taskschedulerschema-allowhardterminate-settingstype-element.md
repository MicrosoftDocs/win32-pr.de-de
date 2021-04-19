---
title: "' Zubei '-Element (settingstype)-Element"
description: Gibt an, dass die Aufgabe mithilfe von TerminateProcess beendet werden kann.
ms.assetid: 093a3cc6-d3e1-48e3-bc9e-0b15df2a54de
keywords:
- "' Zuder '-Element (settingstype)-Element Taskplaner"
- "\"Zuweisung\"-Element Taskplaner"
topic_type:
- apiref
api_name:
- AllowHardTerminate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eba987b42206121b91b3c096f298eac32cf52b38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339132"
---
# <a name="allowhardterminate-settingstype-element"></a><span data-ttu-id="8fb30-105">' Zubei '-Element (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="8fb30-105">AllowHardTerminate (settingsType) Element</span></span>

<span data-ttu-id="8fb30-106">Gibt an, dass die Aufgabe mithilfe von TerminateProcess beendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8fb30-106">Specifies that the task may be terminated using TerminateProcess.</span></span>

``` syntax
<xs:element name="AllowHardTerminate"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

<span data-ttu-id="8fb30-107">Das Element "- **Zuweisung** " wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="8fb30-107">The **AllowHardTerminate** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8fb30-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="8fb30-108">Parent element</span></span>



| <span data-ttu-id="8fb30-109">Element</span><span class="sxs-lookup"><span data-stu-id="8fb30-109">Element</span></span>                                                           | <span data-ttu-id="8fb30-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="8fb30-110">Derived from</span></span>                                                 | <span data-ttu-id="8fb30-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8fb30-111">Description</span></span>                                                                        |
|-------------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="8fb30-112">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="8fb30-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="8fb30-113">**taskType**</span><span class="sxs-lookup"><span data-stu-id="8fb30-113">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="8fb30-114">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8fb30-114">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8fb30-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fb30-115">Remarks</span></span>

<span data-ttu-id="8fb30-116">Informationen zur C++-Entwicklung finden Sie unter der [**Eigenschaft "Zuweisung von Eigenschaften" von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).</span><span class="sxs-lookup"><span data-stu-id="8fb30-116">For C++ development, see the [**AllowHardTerminate property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).</span></span>

<span data-ttu-id="8fb30-117">Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. Zuweisung**](tasksettings-allowhardterminate.md).</span><span class="sxs-lookup"><span data-stu-id="8fb30-117">For script development, see [**TaskSettings.AllowHardTerminate**](tasksettings-allowhardterminate.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8fb30-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fb30-118">Examples</span></span>

<span data-ttu-id="8fb30-119">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die das harte Beenden zulässt, finden Sie unter [time-auslöserbeispiel (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="8fb30-119">For a complete example of the XML for a task that allows hard termination, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8fb30-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8fb30-120">Requirements</span></span>



| <span data-ttu-id="8fb30-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8fb30-121">Requirement</span></span> | <span data-ttu-id="8fb30-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8fb30-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8fb30-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8fb30-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8fb30-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fb30-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8fb30-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8fb30-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8fb30-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fb30-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8fb30-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fb30-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb30-128">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="8fb30-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





