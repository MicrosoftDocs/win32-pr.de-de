---
title: Principal.ID-Eigenschaft
description: Ruft bei der Skripterstellung den Bezeichner des Prinzipals ab oder legt ihn fest.
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- ID-Eigenschaft Taskplaner
- ID-Eigenschaft Taskplaner, Prinzipal Objekt
- Prinzipal Objekt Taskplaner, ID-Eigenschaft
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392087"
---
# <a name="principalid-property"></a><span data-ttu-id="1f6ee-106">Principal.ID-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1f6ee-106">Principal.Id property</span></span>

<span data-ttu-id="1f6ee-107">Ruft bei der Skripterstellung den Bezeichner des Prinzipals ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="1f6ee-107">For scripting, gets or sets the identifier of the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f6ee-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f6ee-108">Syntax</span></span>


```VB
Principal.Id As String
```



## <a name="property-value"></a><span data-ttu-id="1f6ee-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1f6ee-109">Property value</span></span>

<span data-ttu-id="1f6ee-110">Der Bezeichner des Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="1f6ee-110">The identifier of the principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f6ee-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f6ee-111">Remarks</span></span>

<span data-ttu-id="1f6ee-112">Dieser Bezeichner wird auch verwendet, wenn die Eigenschaft " [**aktioncollection. Context**](actioncollection-context.md) " angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1f6ee-112">This identifier is also used when specifying the [**ActionCollection.Context**](actioncollection-context.md) property.</span></span>

<span data-ttu-id="1f6ee-113">Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Bezeichner des Prinzipals im ID-Attribut des [**Principal**](taskschedulerschema-principal-principaltype-element.md) -Elements des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="1f6ee-113">When reading or writing XML for a task, the identifier of the principal is specified in the Id attribute of the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f6ee-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f6ee-114">Requirements</span></span>



| <span data-ttu-id="1f6ee-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f6ee-115">Requirement</span></span> | <span data-ttu-id="1f6ee-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1f6ee-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f6ee-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f6ee-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1f6ee-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f6ee-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1f6ee-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f6ee-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1f6ee-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f6ee-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f6ee-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1f6ee-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f6ee-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1f6ee-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1f6ee-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1f6ee-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f6ee-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f6ee-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f6ee-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f6ee-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f6ee-126">**"Aktions Sammlung. Context"**</span><span class="sxs-lookup"><span data-stu-id="1f6ee-126">**ActionCollection.Context**</span></span>](actioncollection-context.md)
</dt> <dt>

[<span data-ttu-id="1f6ee-127">**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="1f6ee-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="1f6ee-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="1f6ee-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





