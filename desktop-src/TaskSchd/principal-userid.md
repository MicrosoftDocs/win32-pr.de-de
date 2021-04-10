---
title: Principal. UserId-Eigenschaft
description: Ruft bei der Skripterstellung die Benutzer-ID ab, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind, oder legt Sie fest.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- UserID-Eigenschaft Taskplaner
- UserID-Eigenschaft Taskplaner, Prinzipal Objekt
- Prinzipal Objekt Taskplaner, UserID-Eigenschaft
topic_type:
- apiref
api_name:
- Principal.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6fce7fcfdf235ba8a83f262161c2e0f2afc71c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104355"
---
# <a name="principaluserid-property"></a><span data-ttu-id="c272d-106">Principal. UserId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c272d-106">Principal.UserId property</span></span>

<span data-ttu-id="c272d-107">Ruft bei der Skripterstellung die Benutzer-ID ab, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="c272d-107">For scripting, gets or sets the user identifier that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="c272d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c272d-108">Syntax</span></span>


```VB
Principal.UserId As String
```



## <a name="property-value"></a><span data-ttu-id="c272d-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c272d-109">Property value</span></span>

<span data-ttu-id="c272d-110">Der Benutzer Bezeichner, der zum Ausführen der Aufgabe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c272d-110">The user identifier that is required to run the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="c272d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c272d-111">Remarks</span></span>

<span data-ttu-id="c272d-112">Legen Sie diese Eigenschaft nicht fest, wenn ein Gruppen Bezeichner in der [**GroupID**](principal-groupid.md) -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c272d-112">Do not set this property if a group identifier is specified in the [**GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="c272d-113">Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Benutzer-ID für den Prinzipal mit dem [**UserID**](taskschedulerschema-userid-principaltype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="c272d-113">When reading or writing XML for a task, the user identifier for the principal is specified using the [**UserId**](taskschedulerschema-userid-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="c272d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c272d-114">Requirements</span></span>



| <span data-ttu-id="c272d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c272d-115">Requirement</span></span> | <span data-ttu-id="c272d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c272d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c272d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c272d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c272d-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c272d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c272d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c272d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c272d-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c272d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c272d-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c272d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="c272d-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c272d-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c272d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c272d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c272d-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c272d-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c272d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c272d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c272d-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="c272d-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="c272d-127">**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="c272d-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="c272d-128">**Principal. groupID**</span><span class="sxs-lookup"><span data-stu-id="c272d-128">**Principal.GroupId**</span></span>](principal-groupid.md)
</dt> </dl>

 

 





