---
title: Idlesettings. WaitTimeout (Eigenschaft)
description: Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der die Zeitspanne angibt, die der Taskplaner auf das Eintreten einer Leerlauf Bedingung wartet.
ms.assetid: 1be1c62b-bab0-41f8-9f64-e778aba4891f
keywords:
- WaitTimeout-Eigenschaft Taskplaner
- WaitTimeout-Eigenschaft Taskplaner, idlesettings-Objekt
- Idlesettings-Objekt Taskplaner, WaitTimeout-Eigenschaft
topic_type:
- apiref
api_name:
- IdleSettings.WaitTimeout
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb8e2abbd200b2c10eaefeafe2082a00be636a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040710"
---
# <a name="idlesettingswaittimeout-property"></a><span data-ttu-id="77bd9-106">Idlesettings. WaitTimeout (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="77bd9-106">IdleSettings.WaitTimeout property</span></span>

<span data-ttu-id="77bd9-107">Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der die Zeitspanne angibt, die der Taskplaner auf das Eintreten einer Leerlauf Bedingung wartet.</span><span class="sxs-lookup"><span data-stu-id="77bd9-107">For scripting, gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="77bd9-108">Wenn für diese Eigenschaft kein Wert angegeben wird, wartet der Taskplaner-Dienst unbegrenzt, bis eine Leerlauf Bedingung auftritt.</span><span class="sxs-lookup"><span data-stu-id="77bd9-108">If no value is specified for this property, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span>

## <a name="syntax"></a><span data-ttu-id="77bd9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="77bd9-109">Syntax</span></span>


```VB
IdleSettings.WaitTimeout As String
```



## <a name="property-value"></a><span data-ttu-id="77bd9-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="77bd9-110">Property value</span></span>

<span data-ttu-id="77bd9-111">Ein-Wert, der die Zeitspanne angibt, die der Taskplaner auf das Eintreten einer Leerlauf Bedingung wartet.</span><span class="sxs-lookup"><span data-stu-id="77bd9-111">A value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="77bd9-112">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="77bd9-112">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="77bd9-113">Die zulässige minimal Zeit beträgt 1 Minute.</span><span class="sxs-lookup"><span data-stu-id="77bd9-113">The minimum time allowed is 1 minute.</span></span> <span data-ttu-id="77bd9-114">Wenn dieser Wert **null** ist, wird die Verzögerung auf den Standardwert von einer Stunde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="77bd9-114">If this value is **NULL**, then the delay will be set to the default of 1 hour.</span></span>

## <a name="remarks"></a><span data-ttu-id="77bd9-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77bd9-115">Remarks</span></span>

<span data-ttu-id="77bd9-116">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="77bd9-116">When reading or writing XML for a task, this setting is specified in the [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="77bd9-117">Wenn eine Aufgabe durch einen Leerlauf Trigger ausgelöst wird, wird die **idlesettings. WaitTimeout** -Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="77bd9-117">If a task is triggered by an idle trigger, then the **IdleSettings.WaitTimeout** property is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="77bd9-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77bd9-118">Requirements</span></span>



| <span data-ttu-id="77bd9-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77bd9-119">Requirement</span></span> | <span data-ttu-id="77bd9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="77bd9-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77bd9-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77bd9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="77bd9-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77bd9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="77bd9-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77bd9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="77bd9-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77bd9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77bd9-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="77bd9-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="77bd9-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="77bd9-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="77bd9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="77bd9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77bd9-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77bd9-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77bd9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77bd9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77bd9-130">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="77bd9-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="77bd9-131">**Idlesettings**</span><span class="sxs-lookup"><span data-stu-id="77bd9-131">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





