---
title: Tasksettings. disallowstartifonakkus (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task nicht gestartet wird, wenn der Computer unter Akkus ausgeführt wird, oder legt ihn fest.
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- Disallowstartifonakkus-Eigenschaft Taskplaner
- Disallowstartifonakkus-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, disallowstartifonakkus (Eigenschaft)
topic_type:
- apiref
api_name:
- TaskSettings.DisallowStartIfOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35a7fde3012b25dfeab65e6e6088bb1d950892d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105345"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a><span data-ttu-id="4c7d9-106">Tasksettings. disallowstartifonakkus (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4c7d9-106">TaskSettings.DisallowStartIfOnBatteries property</span></span>

<span data-ttu-id="4c7d9-107">Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task nicht gestartet wird, wenn der Computer unter Akkus ausgeführt wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="4c7d9-107">For scripting, gets or sets a Boolean value that indicates that the task will not be started if the computer is running on batteries.</span></span>

<span data-ttu-id="4c7d9-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4c7d9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c7d9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c7d9-109">Syntax</span></span>


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a><span data-ttu-id="4c7d9-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4c7d9-110">Property value</span></span>

<span data-ttu-id="4c7d9-111">Ein boolescher Wert, der angibt, dass der Task nicht gestartet wird, wenn der Computer unter Akkus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c7d9-111">A Boolean value that indicates that the task will not be started if the computer is running on batteries.</span></span> <span data-ttu-id="4c7d9-112">True gibt an, dass der Task nicht gestartet wird, wenn der Computer unter Akkus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c7d9-112">If True, the task will not be started if the computer is running on batteries.</span></span> <span data-ttu-id="4c7d9-113">Bei "false" wird der Task gestartet, wenn der Computer unter "Akkus" ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c7d9-113">If False, the task will be started if the computer is running on batteries.</span></span> <span data-ttu-id="4c7d9-114">Der Standardwert ist True.</span><span class="sxs-lookup"><span data-stu-id="4c7d9-114">The default is True.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c7d9-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c7d9-115">Remarks</span></span>

<span data-ttu-id="4c7d9-116">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**disallowstartifonakkus**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="4c7d9-116">When reading or writing XML for a task, this setting is specified in the [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c7d9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c7d9-117">Requirements</span></span>



| <span data-ttu-id="4c7d9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c7d9-118">Requirement</span></span> | <span data-ttu-id="4c7d9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4c7d9-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c7d9-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c7d9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4c7d9-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c7d9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4c7d9-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c7d9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4c7d9-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c7d9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4c7d9-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4c7d9-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="4c7d9-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4c7d9-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4c7d9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4c7d9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c7d9-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c7d9-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c7d9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c7d9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c7d9-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="4c7d9-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





