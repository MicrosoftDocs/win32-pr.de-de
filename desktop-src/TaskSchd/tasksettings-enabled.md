---
title: Tasksettings. aktivierte Eigenschaft
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task aktiviert ist, oder legt ihn fest. Der Task kann nur ausgeführt werden, wenn diese Einstellung auf "true" festgelegt ist.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Aktivierte Eigenschaften Taskplaner
- Aktivierte Eigenschaften Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, aktivierte Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6805d7b754ac2c3553d5fde91826ffa192b91d97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392036"
---
# <a name="tasksettingsenabled-property"></a><span data-ttu-id="6aa8f-107">Tasksettings. aktivierte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6aa8f-107">TaskSettings.Enabled property</span></span>

<span data-ttu-id="6aa8f-108">Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="6aa8f-108">For scripting, gets or sets a Boolean value that indicates that the task is enabled.</span></span> <span data-ttu-id="6aa8f-109">Der Task kann nur ausgeführt werden, wenn diese Einstellung auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6aa8f-109">The task can be performed only when this setting is True.</span></span>

<span data-ttu-id="6aa8f-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6aa8f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aa8f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6aa8f-111">Syntax</span></span>


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="6aa8f-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6aa8f-112">Property value</span></span>

<span data-ttu-id="6aa8f-113">True gibt an, dass die Aufgabe aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6aa8f-113">If True, the task is enabled.</span></span> <span data-ttu-id="6aa8f-114">Der Wert false gibt an, dass der Task nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6aa8f-114">If False, the task is not enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="6aa8f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6aa8f-115">Remarks</span></span>

<span data-ttu-id="6aa8f-116">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**aktivierten (settingstype)**](taskschedulerschema-enabled-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="6aa8f-116">When reading or writing XML for a task, this setting is specified in the [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="6aa8f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6aa8f-117">Requirements</span></span>



| <span data-ttu-id="6aa8f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6aa8f-118">Requirement</span></span> | <span data-ttu-id="6aa8f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6aa8f-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6aa8f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6aa8f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6aa8f-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6aa8f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6aa8f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6aa8f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6aa8f-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6aa8f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6aa8f-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6aa8f-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="6aa8f-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6aa8f-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6aa8f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6aa8f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6aa8f-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6aa8f-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6aa8f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6aa8f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aa8f-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="6aa8f-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





