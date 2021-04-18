---
title: Deleteexpiredtaskafter (settingstype)-Element
description: Gibt die Zeitspanne an, die der Taskplaner wartet, bevor der Task nach Ablauf gelöscht wird.
ms.assetid: 947a2fec-ceda-4726-aa1a-26fd1b258c1f
keywords:
- Deleteexpiredtaskafter-Element Taskplaner
topic_type:
- apiref
api_name:
- DeleteExpiredTaskAfter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cee7cfc48f62b58caf63125404fb07209b399fc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340576"
---
# <a name="deleteexpiredtaskafter-settingstype-element"></a><span data-ttu-id="e5c87-104">Deleteexpiredtaskafter (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="e5c87-104">DeleteExpiredTaskAfter (settingsType) Element</span></span>

<span data-ttu-id="e5c87-105">Gibt die Zeitspanne an, die der Taskplaner wartet, bevor der Task nach Ablauf gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="e5c87-105">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="e5c87-106">Wenn für dieses Element kein Wert angegeben wird, wird der Task vom Taskplaner-Dienst nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e5c87-106">If no value is specified for this element, then the Task Scheduler service will not delete the task.</span></span> <span data-ttu-id="e5c87-107">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="e5c87-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="e5c87-108">Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="e5c87-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="DeleteExpiredTaskAfter"
    type="duration"
    minOccurs="0"
    default="PT0S"
 />
```

<span data-ttu-id="e5c87-109">Das **deleteexpiredtaskafter** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="e5c87-109">The **DeleteExpiredTaskAfter** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e5c87-110">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="e5c87-110">Parent element</span></span>



| <span data-ttu-id="e5c87-111">Element</span><span class="sxs-lookup"><span data-stu-id="e5c87-111">Element</span></span>                                                           | <span data-ttu-id="e5c87-112">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="e5c87-112">Derived from</span></span>                                                         | <span data-ttu-id="e5c87-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5c87-113">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5c87-114">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="e5c87-114">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="e5c87-115">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="e5c87-115">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="e5c87-116">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e5c87-116">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e5c87-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5c87-117">Remarks</span></span>

<span data-ttu-id="e5c87-118">Informationen zur C++-Entwicklung finden Sie unter [**deleteexpiredtaskafter-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter).</span><span class="sxs-lookup"><span data-stu-id="e5c87-118">For C++ development, see [**DeleteExpiredTaskAfter Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter).</span></span>

<span data-ttu-id="e5c87-119">Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. deleteexpiredtaskafter**](tasksettings-deleteexpiredtaskafter.md).</span><span class="sxs-lookup"><span data-stu-id="e5c87-119">For script development, see [**TaskSettings.DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e5c87-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5c87-120">Examples</span></span>

<span data-ttu-id="e5c87-121">Der folgende XML-Code definiert ein Einstellungs Element, das eine abgelaufene Aufgabe nach einer Woche löscht.</span><span class="sxs-lookup"><span data-stu-id="e5c87-121">The following XML defines a settings element that deletes an expired task after one week.</span></span>


```XML
<Settings>
    <DeleteExpiredTaskAfter>PT7D</DeleteExpiredTaskAfter>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="e5c87-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5c87-122">Requirements</span></span>



| <span data-ttu-id="e5c87-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5c87-123">Requirement</span></span> | <span data-ttu-id="e5c87-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e5c87-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e5c87-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5c87-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e5c87-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5c87-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e5c87-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5c87-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e5c87-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5c87-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e5c87-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5c87-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c87-130">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="e5c87-130">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





