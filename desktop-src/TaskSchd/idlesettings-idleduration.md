---
title: Idlesettings. idleduration-Eigenschaft
description: Ruft bei der Skripterstellung einen Wert ab, der angibt, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird, oder legt ihn fest.
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- Idleduration-Eigenschaft Taskplaner
- Idleduration-Eigenschaft Taskplaner, idlesettings-Objekt
- Idlesettings-Objekt Taskplaner, idleduration-Eigenschaft
topic_type:
- apiref
api_name:
- IdleSettings.IdleDuration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6eeed4fef540b3a9e13d0f52e3ce1934cb9e220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742456"
---
# <a name="idlesettingsidleduration-property"></a><span data-ttu-id="026cb-106">Idlesettings. idleduration-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="026cb-106">IdleSettings.IdleDuration property</span></span>

<span data-ttu-id="026cb-107">Ruft bei der Skripterstellung einen Wert ab, der angibt, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="026cb-107">For scripting, gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.</span></span>

## <a name="syntax"></a><span data-ttu-id="026cb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="026cb-108">Syntax</span></span>


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a><span data-ttu-id="026cb-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="026cb-109">Property value</span></span>

<span data-ttu-id="026cb-110">Ein-Wert, der die Zeitspanne angibt, in der sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="026cb-110">A value that indicates the amount of time that the computer must be in an idle state before the task is run).</span></span> <span data-ttu-id="026cb-111">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="026cb-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="026cb-112">Der Mindestwert ist eine Minute.</span><span class="sxs-lookup"><span data-stu-id="026cb-112">The minimum value is one minute.</span></span> <span data-ttu-id="026cb-113">Wenn dieser Wert **null** ist, wird die Verzögerung auf den Standardwert von 10 Minuten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="026cb-113">If this value is **NULL**, then the delay will be set to the default of 10 minutes.</span></span>

## <a name="remarks"></a><span data-ttu-id="026cb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="026cb-114">Remarks</span></span>

<span data-ttu-id="026cb-115">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="026cb-115">When reading or writing XML for a task, this setting is specified in the [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="026cb-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="026cb-116">Requirements</span></span>



| <span data-ttu-id="026cb-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="026cb-117">Requirement</span></span> | <span data-ttu-id="026cb-118">Wert</span><span class="sxs-lookup"><span data-stu-id="026cb-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="026cb-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="026cb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="026cb-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="026cb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="026cb-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="026cb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="026cb-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="026cb-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="026cb-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="026cb-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="026cb-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="026cb-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="026cb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="026cb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="026cb-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="026cb-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="026cb-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="026cb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="026cb-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="026cb-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="026cb-129">**Idlesettings**</span><span class="sxs-lookup"><span data-stu-id="026cb-129">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





