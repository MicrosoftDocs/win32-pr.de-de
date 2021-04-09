---
title: Tasksettings. waketor UN-Eigenschaft
description: Ruft bei der Skripterstellung einen booleschen Wert ab oder legt diesen fest, der angibt, dass die Taskplaner den Computer reaktivieren wird, wenn die Aufgabe ausgeführt wird.
ms.assetid: 51f83637-5bae-48c6-b750-b4467e651cec
keywords:
- Eigenschaft "waketor UN" Taskplaner
- Waketorun-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, waketorun-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.WakeToRun
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b563fd1ecd27914e84043b85c44f0cf5262e9fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740801"
---
# <a name="tasksettingswaketorun-property"></a><span data-ttu-id="e8dc9-106">Tasksettings. waketor UN-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e8dc9-106">TaskSettings.WakeToRun property</span></span>

<span data-ttu-id="e8dc9-107">Ruft bei der Skripterstellung einen booleschen Wert ab oder legt diesen fest, der angibt, dass die Taskplaner den Computer reaktivieren wird, wenn die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will wake the computer when it is time to run the task.</span></span>

<span data-ttu-id="e8dc9-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8dc9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8dc9-109">Syntax</span></span>


```VB
TaskSettings.WakeToRun As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e8dc9-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e8dc9-110">Property value</span></span>

<span data-ttu-id="e8dc9-111">Wenn true, gibt die-Eigenschaft an, dass der Computer vom Taskplaner aktiviert wird, wenn die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-111">If True, the property indicates that the Task Scheduler will wake the computer when it is time to run the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8dc9-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8dc9-112">Remarks</span></span>

<span data-ttu-id="e8dc9-113">Wenn der Taskplaner-Dienst den Computer zum Ausführen einer Aufgabe aktiviert, bleibt der Bildschirm möglicherweise deaktiviert, auch wenn sich der Computer nicht mehr im Standbymodus oder Ruhezustand befindet.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-113">When the Task Scheduler service wakes the computer to run a task, the screen may remain off even though the computer is no longer in the sleep or hibernate mode.</span></span> <span data-ttu-id="e8dc9-114">Der Bildschirm wird eingeschaltet, wenn Windows Vista erkennt, dass ein Benutzer die Verwendung des Computers zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-114">The screen will turn on when Windows Vista detects that a user has returned to use the computer.</span></span>

<span data-ttu-id="e8dc9-115">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**waketorun-**](taskschedulerschema-waketorun-settingstype-element.md) Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-115">When reading or writing XML for a task, this setting is specified in the [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8dc9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8dc9-116">Requirements</span></span>



| <span data-ttu-id="e8dc9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8dc9-117">Requirement</span></span> | <span data-ttu-id="e8dc9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e8dc9-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8dc9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8dc9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e8dc9-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8dc9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e8dc9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8dc9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e8dc9-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8dc9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e8dc9-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e8dc9-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8dc9-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e8dc9-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e8dc9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e8dc9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8dc9-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8dc9-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8dc9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8dc9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8dc9-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="e8dc9-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





