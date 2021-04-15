---
title: Tasksettings. runonlyimedle (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe nur dann ausführen soll, wenn sich der Computer im Leerlauf befindet, oder legt diesen fest.
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- Runonlyimedle-Eigenschaft Taskplaner
- Runonlyifdle-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, runonlyimedle-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8256b2a3d1dd96db9a8f29b49ce10f6c2fdb266d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391754"
---
# <a name="tasksettingsrunonlyifidle-property"></a><span data-ttu-id="e0cfb-106">Tasksettings. runonlyimedle (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e0cfb-106">TaskSettings.RunOnlyIfIdle property</span></span>

<span data-ttu-id="e0cfb-107">Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe nur dann ausführen soll, wenn sich der Computer im Leerlauf befindet, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="e0cfb-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will run the task only if the computer is in an idle condition.</span></span>

<span data-ttu-id="e0cfb-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e0cfb-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0cfb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0cfb-109">Syntax</span></span>


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e0cfb-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e0cfb-110">Property value</span></span>

<span data-ttu-id="e0cfb-111">Wenn true, gibt die-Eigenschaft an, dass die Taskplaner die Aufgabe nur dann ausführen soll, wenn sich der Computer im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="e0cfb-111">If True, the property indicates that the Task Scheduler will run the task only if the computer is in an idle condition.</span></span> <span data-ttu-id="e0cfb-112">Die Standardeinstellung lautet „false“.</span><span class="sxs-lookup"><span data-stu-id="e0cfb-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0cfb-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0cfb-113">Remarks</span></span>

<span data-ttu-id="e0cfb-114">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**runonlyimedle**](taskschedulerschema-runonlyifidle-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="e0cfb-114">When reading or writing XML for a task, this setting is specified in the [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0cfb-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0cfb-115">Requirements</span></span>



| <span data-ttu-id="e0cfb-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0cfb-116">Requirement</span></span> | <span data-ttu-id="e0cfb-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e0cfb-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0cfb-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0cfb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e0cfb-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0cfb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e0cfb-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0cfb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e0cfb-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0cfb-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e0cfb-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e0cfb-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="e0cfb-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e0cfb-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e0cfb-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e0cfb-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0cfb-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0cfb-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0cfb-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0cfb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0cfb-127">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="e0cfb-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





