---
title: Trigger.ID-Eigenschaft
description: Ruft bei der Skripterstellung den Bezeichner für den-Typ ab oder legt ihn fest.
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- ID-Eigenschaft Taskplaner
- ID-Eigenschaften Taskplaner, Auslöserobjekt
- Auslöse Objekt Taskplaner, ID-Eigenschaft
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a3868f76368b19e6a316b222b8ddaf4cbbff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517558"
---
# <a name="triggerid-property"></a><span data-ttu-id="08492-106">Trigger.ID-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="08492-106">Trigger.Id property</span></span>

<span data-ttu-id="08492-107">Ruft bei der Skripterstellung den Bezeichner für den-Typ ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="08492-107">For scripting, gets or sets the identifier for the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="08492-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="08492-108">Syntax</span></span>


```VB
Trigger.Id As String
```



## <a name="property-value"></a><span data-ttu-id="08492-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="08492-109">Property value</span></span>

<span data-ttu-id="08492-110">Der Bezeichner für den-Auslösers.</span><span class="sxs-lookup"><span data-stu-id="08492-110">The identifier for the trigger.</span></span> <span data-ttu-id="08492-111">Dieser Bezeichner wird von der-Taskplaner zu Protokollierungs Zwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="08492-111">This identifier is used by the Task Scheduler for logging purposes.</span></span>

## <a name="remarks"></a><span data-ttu-id="08492-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08492-112">Remarks</span></span>

<span data-ttu-id="08492-113">Beim Lesen oder Schreiben von XML für eine Aufgabe wird der auslöserbezeichner im ID-Attribut der einzelnen auslöserelemente (z. b. des ID-Attributs des [**boottrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) -Elements) des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="08492-113">When reading or writing XML for a task, the trigger identifier is specified in the Id attribute of the individual trigger elements (for example, the Id attribute of the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element) of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="08492-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08492-114">Requirements</span></span>



| <span data-ttu-id="08492-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08492-115">Requirement</span></span> | <span data-ttu-id="08492-116">Wert</span><span class="sxs-lookup"><span data-stu-id="08492-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08492-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08492-117">Minimum supported client</span></span><br/> | <span data-ttu-id="08492-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08492-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="08492-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08492-119">Minimum supported server</span></span><br/> | <span data-ttu-id="08492-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08492-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08492-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="08492-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="08492-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="08492-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="08492-123">DLL</span><span class="sxs-lookup"><span data-stu-id="08492-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08492-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08492-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08492-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08492-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08492-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="08492-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





