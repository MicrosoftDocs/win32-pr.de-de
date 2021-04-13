---
title: Tasksettings. startaccessavailable (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe jederzeit nach dem geplanten Zeitpunkt starten kann, oder legt diesen fest.
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- Startin verfügbare Eigenschaft Taskplaner
- Starteinavailable-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, start\verfüg Bare Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63325fbf7aa9186e5748294c2ef57302efa0c79b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478363"
---
# <a name="tasksettingsstartwhenavailable-property"></a><span data-ttu-id="73daa-106">Tasksettings. startaccessavailable (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="73daa-106">TaskSettings.StartWhenAvailable property</span></span>

<span data-ttu-id="73daa-107">Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe jederzeit nach dem geplanten Zeitpunkt starten kann, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="73daa-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span>

<span data-ttu-id="73daa-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="73daa-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="73daa-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="73daa-109">Syntax</span></span>


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a><span data-ttu-id="73daa-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="73daa-110">Property value</span></span>

<span data-ttu-id="73daa-111">Wenn true, gibt die-Eigenschaft an, dass die Taskplaner die Aufgabe jederzeit nach Ablauf der geplanten Zeit starten kann.</span><span class="sxs-lookup"><span data-stu-id="73daa-111">If True, the property indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span> <span data-ttu-id="73daa-112">Die Standardeinstellung lautet „false“.</span><span class="sxs-lookup"><span data-stu-id="73daa-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="73daa-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73daa-113">Remarks</span></span>

<span data-ttu-id="73daa-114">Diese Eigenschaft gilt nur für zeitbasierte Aufgaben mit einer endbegrenzung oder zeitbasierten Aufgaben, die so festgelegt werden, dass Sie unendlich wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="73daa-114">This property applies only to time-based tasks with an end boundary or time-based tasks that are set to repeat infinitely.</span></span>

<span data-ttu-id="73daa-115">Tasks, die nach dem geplanten Zeitpunkt gestartet werden (da die [**start\available**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) -Eigenschaft auf true festgelegt ist), werden in die Warteschlange der Aufgaben des Taskplaner dienstangs eingereiht und nach einer Verzögerung gestartet.</span><span class="sxs-lookup"><span data-stu-id="73daa-115">Tasks that are started after the scheduled time has passed (because of the [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) property being set to True) are queued in the Task Scheduler service's queue of tasks and they are started after a delay.</span></span> <span data-ttu-id="73daa-116">Die Standard Verzögerung beträgt 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="73daa-116">The default delay is 10 minutes.</span></span>

<span data-ttu-id="73daa-117">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**starteinavailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="73daa-117">When reading or writing XML for a task, this setting is specified in the [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="73daa-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73daa-118">Requirements</span></span>



| <span data-ttu-id="73daa-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73daa-119">Requirement</span></span> | <span data-ttu-id="73daa-120">Wert</span><span class="sxs-lookup"><span data-stu-id="73daa-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73daa-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73daa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="73daa-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73daa-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="73daa-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73daa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="73daa-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73daa-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73daa-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="73daa-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="73daa-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="73daa-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="73daa-127">DLL</span><span class="sxs-lookup"><span data-stu-id="73daa-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73daa-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73daa-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73daa-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73daa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73daa-130">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="73daa-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





