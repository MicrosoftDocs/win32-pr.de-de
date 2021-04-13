---
title: Tasksettings. deleteexpiredtaskafter-Eigenschaft
description: Ruft bei der Skripterstellung die Zeitspanne ab, die der Taskplaner wartet, bevor der Task nach Ablauf gelöscht wird, oder legt ihn fest.
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- Deleteexpiredtaskafter-Eigenschaft Taskplaner
- Deleteexpiredtaskafter-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, deleteexpiredtaskafter-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.DeleteExpiredTaskAfter
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9005ff7988353daa902b1bc3151c539713bb94ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475957"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a><span data-ttu-id="d139c-106">Tasksettings. deleteexpiredtaskafter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d139c-106">TaskSettings.DeleteExpiredTaskAfter property</span></span>

<span data-ttu-id="d139c-107">Ruft bei der Skripterstellung die Zeitspanne ab, die der Taskplaner wartet, bevor der Task nach Ablauf gelöscht wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="d139c-107">For scripting, gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="d139c-108">Wenn für diese Eigenschaft kein Wert angegeben wird, wird die Aufgabe vom Taskplaner-Dienst nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d139c-108">If no value is specified for this property, then the Task Scheduler service will not delete the task.</span></span>

<span data-ttu-id="d139c-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d139c-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d139c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d139c-110">Syntax</span></span>


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a><span data-ttu-id="d139c-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d139c-111">Property value</span></span>

<span data-ttu-id="d139c-112">Eine Zeichenfolge, mit der die Zeitspanne abgerufen oder festgelegt wird, die der Taskplaner wartet, bevor die Aufgabe nach Ablauf gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="d139c-112">A string that gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="d139c-113">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="d139c-113">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="d139c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d139c-114">Remarks</span></span>

<span data-ttu-id="d139c-115">Ein Task läuft ab, nachdem die Endgrenze für alle der Aufgabe zugeordneten Trigger überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="d139c-115">A task expires after the end boundary has been exceeded for all triggers associated with the task.</span></span> <span data-ttu-id="d139c-116">Die Endgrenze für einen-Endpunkt wird durch die [endboundary](trigger-endboundary.md) -Eigenschaft angegeben, die von allen auslöserobjekten geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="d139c-116">The end boundary for a trigger is specified by the [EndBoundary](trigger-endboundary.md) property inherited by all trigger objects.</span></span>

<span data-ttu-id="d139c-117">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**deleteexpiredtaskafter-Element (settingstype)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="d139c-117">When reading or writing XML for a task, this setting is specified in the [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d139c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d139c-118">Requirements</span></span>



| <span data-ttu-id="d139c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d139c-119">Requirement</span></span> | <span data-ttu-id="d139c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d139c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d139c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d139c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d139c-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d139c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d139c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d139c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d139c-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d139c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d139c-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d139c-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="d139c-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d139c-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d139c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d139c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d139c-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d139c-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d139c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d139c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d139c-130">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="d139c-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





