---
title: Tasksettings. stopifgoingonakkus (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab oder legt diesen fest, der angibt, dass der Task angehalten wird, wenn der Computer auf dem Gerät ausgeführt wird.
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- Stopifgoingonakkus-Eigenschaft Taskplaner
- Stopifgoingonakkus-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, stopifgoingonakkus (Eigenschaft)
topic_type:
- apiref
api_name:
- TaskSettings.StopIfGoingOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aced436d653b6bbc02b4b36edea9046e3ac62392
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478354"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a><span data-ttu-id="9efbc-106">Tasksettings. stopifgoingonakkus (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9efbc-106">TaskSettings.StopIfGoingOnBatteries property</span></span>

<span data-ttu-id="9efbc-107">Ruft bei der Skripterstellung einen booleschen Wert ab oder legt diesen fest, der angibt, dass der Task angehalten wird, wenn der Computer auf dem Gerät ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9efbc-107">For scripting, gets or sets a Boolean value that indicates that the task will be stopped if the computer is going onto batteries.</span></span>

<span data-ttu-id="9efbc-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9efbc-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9efbc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9efbc-109">Syntax</span></span>


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a><span data-ttu-id="9efbc-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9efbc-110">Property value</span></span>

<span data-ttu-id="9efbc-111">Ein boolescher Wert, der angibt, dass der Task angehalten wird, wenn der Computer in den Akku Betrieb geht.</span><span class="sxs-lookup"><span data-stu-id="9efbc-111">A Boolean value that indicates that the task will be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="9efbc-112">Wenn der Wert true ist, gibt die Eigenschaft an, dass der Task beendet wird, wenn der Computer auf die Batterie geht.</span><span class="sxs-lookup"><span data-stu-id="9efbc-112">If True, the property indicates that the task will be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="9efbc-113">Wenn der Wert false ist, gibt die Eigenschaft an, dass die Aufgabe nicht angehalten wird, wenn der Computer auf die Batterie geht.</span><span class="sxs-lookup"><span data-stu-id="9efbc-113">If False, the property indicates that the task will not be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="9efbc-114">Der Standardwert ist True.</span><span class="sxs-lookup"><span data-stu-id="9efbc-114">The default is True.</span></span> <span data-ttu-id="9efbc-115">Weitere Informationen finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="9efbc-115">See Remarks for more details.</span></span>

## <a name="remarks"></a><span data-ttu-id="9efbc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9efbc-116">Remarks</span></span>

<span data-ttu-id="9efbc-117">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**stopifgoingonakkus**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="9efbc-117">When reading or writing XML for a task, this setting is specified in the [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="9efbc-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9efbc-118">Requirements</span></span>



| <span data-ttu-id="9efbc-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9efbc-119">Requirement</span></span> | <span data-ttu-id="9efbc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9efbc-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9efbc-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9efbc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9efbc-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9efbc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9efbc-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9efbc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9efbc-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9efbc-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9efbc-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9efbc-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="9efbc-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9efbc-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9efbc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9efbc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9efbc-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9efbc-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9efbc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9efbc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9efbc-130">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="9efbc-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





