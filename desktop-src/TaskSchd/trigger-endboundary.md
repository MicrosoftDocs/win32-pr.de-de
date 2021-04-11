---
title: Auslöse. endborder-Eigenschaft
description: Ruft bei der Skripterstellung das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- Endboundary-Eigenschaft Taskplaner
- Endboundary-Eigenschaften Taskplaner, Auslöserobjekt
- Auslöse Objekt Taskplaner, endboundary-Eigenschaft
topic_type:
- apiref
api_name:
- Trigger.EndBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b385dddf186484bc17cff9f92d979cd64381335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040390"
---
# <a name="triggerendboundary-property"></a><span data-ttu-id="b1430-107">Auslöse. endborder-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b1430-107">Trigger.EndBoundary property</span></span>

<span data-ttu-id="b1430-108">Ruft bei der Skripterstellung das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="b1430-108">For scripting, gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="b1430-109">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="b1430-109">The trigger cannot start the task after it is deactivated.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1430-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1430-110">Syntax</span></span>


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a><span data-ttu-id="b1430-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b1430-111">Property value</span></span>

<span data-ttu-id="b1430-112">Das Datum und die Uhrzeit der Deaktivierung des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="b1430-112">The date and time when the trigger is deactivated.</span></span> <span data-ttu-id="b1430-113">Das Datum und die Uhrzeit müssen im folgenden Format vorliegen: yyyy-mm-ddThh: mm: SS (+-) hh: mm.</span><span class="sxs-lookup"><span data-stu-id="b1430-113">The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM.</span></span> <span data-ttu-id="b1430-114">Beispielsweise würde das Datum am 11. Oktober 2005 um 1:21:17 in der Pacific Time Zone als "2005-10-11t13:21:17-08:00" geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b1430-114">For example the date October 11th, 2005 at 1:21:17 in the Pacific time zone would be written as 2005-10-11T13:21:17-08:00.</span></span> <span data-ttu-id="b1430-115">Der Abschnitt (+-) hh: mm des Formats beschreibt die Zeitzone als eine bestimmte Anzahl von Stunden vor oder hinter koordinierter Weltzeit (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="b1430-115">The (+-)HH:MM section of the format describes the time zone as a certain number of hours ahead or behind Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1430-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1430-116">Remarks</span></span>

<span data-ttu-id="b1430-117">Beim Lesen oder Schreiben von XML für eine Aufgabe wird die aktivierte Eigenschaft mit dem [**endboundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) -Element des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="b1430-117">When reading or writing XML for a task, the enabled property is specified using the [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1430-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1430-118">Requirements</span></span>



| <span data-ttu-id="b1430-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1430-119">Requirement</span></span> | <span data-ttu-id="b1430-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b1430-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1430-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1430-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b1430-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1430-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b1430-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1430-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b1430-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1430-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b1430-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b1430-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="b1430-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b1430-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b1430-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b1430-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1430-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1430-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1430-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1430-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1430-130">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="b1430-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





