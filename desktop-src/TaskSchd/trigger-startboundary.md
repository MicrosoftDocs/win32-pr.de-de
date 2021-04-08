---
title: Auslöse. StartBoundary (Eigenschaft)
description: Ruft bei der Skripterstellung das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- StartBoundary-Eigenschaft Taskplaner
- StartBoundary-Eigenschaft Taskplaner, Auslöserobjekt
- Auslöse Objekt Taskplaner, StartBoundary-Eigenschaft
topic_type:
- apiref
api_name:
- Trigger.StartBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141e7e4d80d090e92ecb951917f60f972587d4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740793"
---
# <a name="triggerstartboundary-property"></a><span data-ttu-id="464ad-106">Auslöse. StartBoundary (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="464ad-106">Trigger.StartBoundary property</span></span>

<span data-ttu-id="464ad-107">Ruft bei der Skripterstellung das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="464ad-107">For scripting, gets or sets the date and time when the trigger is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="464ad-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="464ad-108">Syntax</span></span>


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a><span data-ttu-id="464ad-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="464ad-109">Property value</span></span>

<span data-ttu-id="464ad-110">Das Datum und die Uhrzeit der Aktivierung des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="464ad-110">The date and time when the trigger is activated.</span></span> <span data-ttu-id="464ad-111">Das Datum und die Uhrzeit müssen im folgenden Format vorliegen: yyyy-mm-ddThh: mm: SS (+-) hh: mm.</span><span class="sxs-lookup"><span data-stu-id="464ad-111">The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM.</span></span> <span data-ttu-id="464ad-112">Beispielsweise würde das Datum am 11. Oktober 2005 um 1:21:17 in der Pacific Time Zone als "2005-10-11t13:21:17-08:00" geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="464ad-112">For example the date October 11th, 2005 at 1:21:17 in the Pacific Time zone would be written as 2005-10-11T13:21:17-08:00.</span></span> <span data-ttu-id="464ad-113">Der Abschnitt (+-) hh: mm des Formats beschreibt die Zeitzone als eine bestimmte Anzahl von Stunden vor oder hinter koordinierter Weltzeit (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="464ad-113">The (+-)HH:MM section of the format describes the time zone as a certain number of hours ahead or behind Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="remarks"></a><span data-ttu-id="464ad-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="464ad-114">Remarks</span></span>

<span data-ttu-id="464ad-115">Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Start Grenze des Auslösers im [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="464ad-115">When reading or writing XML for a task, the trigger start boundary is specified in the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="464ad-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="464ad-116">Requirements</span></span>



| <span data-ttu-id="464ad-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="464ad-117">Requirement</span></span> | <span data-ttu-id="464ad-118">Wert</span><span class="sxs-lookup"><span data-stu-id="464ad-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="464ad-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="464ad-119">Minimum supported client</span></span><br/> | <span data-ttu-id="464ad-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="464ad-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="464ad-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="464ad-121">Minimum supported server</span></span><br/> | <span data-ttu-id="464ad-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="464ad-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="464ad-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="464ad-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="464ad-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="464ad-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="464ad-125">DLL</span><span class="sxs-lookup"><span data-stu-id="464ad-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="464ad-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="464ad-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="464ad-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="464ad-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="464ad-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="464ad-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





