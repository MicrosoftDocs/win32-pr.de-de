---
title: Registrationauslöst. Delay (Eigenschaft)
description: Ruft bei der Skripterstellung die Zeitspanne zwischen dem Registrieren der Aufgabe und dem Start der Aufgabe ab oder legt diese fest.
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- Verzögerte Eigenschaften Taskplaner
- Delay-Eigenschaft Taskplaner, Registration-Auslöserobjekt
- Registration-Auslöserobjekt Taskplaner, Delay-Eigenschaft
topic_type:
- apiref
api_name:
- RegistrationTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad86017547ac4476f430e13e2566ddd6d3494226
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518602"
---
# <a name="registrationtriggerdelay-property"></a><span data-ttu-id="e0ee6-106">Registrationauslöst. Delay (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e0ee6-106">RegistrationTrigger.Delay property</span></span>

<span data-ttu-id="e0ee6-107">Ruft bei der Skripterstellung die Zeitspanne zwischen dem Registrieren der Aufgabe und dem Start der Aufgabe ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e0ee6-107">For scripting, gets or sets the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="e0ee6-108">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="e0ee6-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0ee6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0ee6-109">Syntax</span></span>


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="e0ee6-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e0ee6-110">Property value</span></span>

<span data-ttu-id="e0ee6-111">Die Zeitspanne zwischen dem Registrieren des Systems und dem Start des Tasks.</span><span class="sxs-lookup"><span data-stu-id="e0ee6-111">The amount of time between when the system is registered and when the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0ee6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0ee6-112">Remarks</span></span>

<span data-ttu-id="e0ee6-113">Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Startverzögerung mit dem [**Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="e0ee6-113">When reading or writing XML for a task, the boot delay is specified using the [**Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="e0ee6-114">Wenn eine Aufgabe mit einem verzögerten Registrierungs Ausfall registriert ist und der Computer, auf dem der Task registriert ist, während der Verzögerung heruntergefahren oder neu gestartet wird, bevor der Task ausgeführt wird, wird der Task nicht ausgeführt, und die Verzögerung geht verloren.</span><span class="sxs-lookup"><span data-stu-id="e0ee6-114">If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during the delay, before the task runs, then the task will not run and the delay will be lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0ee6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0ee6-115">Requirements</span></span>



| <span data-ttu-id="e0ee6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0ee6-116">Requirement</span></span> | <span data-ttu-id="e0ee6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e0ee6-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ee6-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0ee6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e0ee6-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0ee6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e0ee6-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0ee6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e0ee6-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0ee6-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e0ee6-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e0ee6-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="e0ee6-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e0ee6-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e0ee6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e0ee6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0ee6-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0ee6-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0ee6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0ee6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0ee6-127">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="e0ee6-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





