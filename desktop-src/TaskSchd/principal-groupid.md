---
title: Principal. GroupID (Eigenschaft)
description: Dient zum Abrufen oder Festlegen des Bezeichners der Benutzergruppe, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.
ms.assetid: be0b7cd1-0e17-4aa5-af8e-880c95b3e7dc
keywords:
- GroupID-Eigenschaft Taskplaner
- GroupID-Eigenschaft Taskplaner, Prinzipal Objekt
- Principal-Objekt Taskplaner, GroupID-Eigenschaft
topic_type:
- apiref
api_name:
- Principal.GroupId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5acd17d32b0123723fe53f91e390c37f42d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339995"
---
# <a name="principalgroupid-property"></a><span data-ttu-id="b8ca1-106">Principal. GroupID (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b8ca1-106">Principal.GroupId property</span></span>

<span data-ttu-id="b8ca1-107">Dient zum Abrufen oder Festlegen des Bezeichners der Benutzergruppe, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b8ca1-107">For scripting, gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8ca1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8ca1-108">Syntax</span></span>


```VB
Principal.GroupId As String
```



## <a name="property-value"></a><span data-ttu-id="b8ca1-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b8ca1-109">Property value</span></span>

<span data-ttu-id="b8ca1-110">Der Bezeichner der Benutzergruppe, die diesem Prinzipal zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b8ca1-110">The identifier of the user group that is associated with this principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8ca1-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8ca1-111">Remarks</span></span>

<span data-ttu-id="b8ca1-112">Legen Sie diese Eigenschaft nicht fest, wenn ein Benutzer Bezeichner in der [**UserID**](principal-userid.md) -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b8ca1-112">Do not set this property if a user identifier is specified in the [**UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="b8ca1-113">Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Gruppen Bezeichner für einen Prinzipal im [**GroupID**](taskschedulerschema-groupid-principaltype-element.md) -Element des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="b8ca1-113">When reading or writing XML for a task, the group identifier for a principal is specified in the [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8ca1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8ca1-114">Requirements</span></span>



| <span data-ttu-id="b8ca1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8ca1-115">Requirement</span></span> | <span data-ttu-id="b8ca1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b8ca1-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ca1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8ca1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b8ca1-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8ca1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b8ca1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8ca1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b8ca1-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8ca1-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b8ca1-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b8ca1-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="b8ca1-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b8ca1-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b8ca1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b8ca1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8ca1-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8ca1-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8ca1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8ca1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8ca1-126">**UserID**</span><span class="sxs-lookup"><span data-stu-id="b8ca1-126">**UserId**</span></span>](principal-userid.md)
</dt> <dt>

[<span data-ttu-id="b8ca1-127">**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="b8ca1-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="b8ca1-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="b8ca1-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





