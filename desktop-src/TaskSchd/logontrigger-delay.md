---
title: Logonauslöst. Delay (Eigenschaft)
description: Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der angibt, wie lange der Benutzer sich anmeldet und wann die Aufgabe gestartet wird.
ms.assetid: 42198357-18e9-4fff-a8bf-f2da36148dc8
keywords:
- Verzögerte Eigenschaften Taskplaner
- Delay-Eigenschaft Taskplaner, LOGON-Auslöserobjekt
- Logon-Auslöserobjekt Taskplaner, Delay-Eigenschaft
topic_type:
- apiref
api_name:
- LogonTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce709b5095ffaeb9fdb5a4532f496ffa34c24e5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391637"
---
# <a name="logontriggerdelay-property"></a><span data-ttu-id="4248f-106">Logonauslöst. Delay (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4248f-106">LogonTrigger.Delay property</span></span>

<span data-ttu-id="4248f-107">Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der angibt, wie lange der Benutzer sich anmeldet und wann die Aufgabe gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="4248f-107">For scripting, gets or sets a value that indicates the amount of time between when the user logs on and when the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="4248f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4248f-108">Syntax</span></span>


```VB
LogonTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="4248f-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4248f-109">Property value</span></span>

<span data-ttu-id="4248f-110">Ein-Wert, der die Zeitspanne zwischen dem Zeitpunkt, an dem der Benutzer sich anmeldet, und dem Start der Aufgabe angibt.</span><span class="sxs-lookup"><span data-stu-id="4248f-110">A value that indicates the amount of time between when the user logs on and when the task is started.</span></span> <span data-ttu-id="4248f-111">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="4248f-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="4248f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4248f-112">Remarks</span></span>

<span data-ttu-id="4248f-113">Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Verzögerung des LOGON-Auslösers mit dem [**Delay**](taskschedulerschema-delay-logontriggertype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="4248f-113">When reading or writing XML for a task, the logon trigger delay is specified using the [**Delay**](taskschedulerschema-delay-logontriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="4248f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4248f-114">Requirements</span></span>



| <span data-ttu-id="4248f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4248f-115">Requirement</span></span> | <span data-ttu-id="4248f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4248f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4248f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4248f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4248f-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4248f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4248f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4248f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4248f-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4248f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4248f-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4248f-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="4248f-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4248f-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4248f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4248f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4248f-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4248f-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4248f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4248f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4248f-126">**Logonauslöst**</span><span class="sxs-lookup"><span data-stu-id="4248f-126">**LogonTrigger**</span></span>](logontrigger.md)
</dt> <dt>

[<span data-ttu-id="4248f-127">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="4248f-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





