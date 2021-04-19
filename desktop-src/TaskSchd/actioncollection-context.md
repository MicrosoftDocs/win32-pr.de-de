---
title: Eigenschaft "Aktions Sammlung. Context"
description: Ruft bei der Skripterstellung den Bezeichner des Prinzipals für den Task ab oder legt ihn fest.
ms.assetid: 5d8ac31c-ce07-4801-a04e-e12e996b88c6
keywords:
- Kontext Eigenschaft Taskplaner
- Kontext Eigenschaft Taskplaner, Aktions Sammlungsobjekt
- Aktions Sammlungsobjekt Taskplaner, Kontext Eigenschaft
topic_type:
- apiref
api_name:
- ActionCollection.Context
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98318ba8332e4c3bb0e7fee6b702a7ed50533
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339349"
---
# <a name="actioncollectioncontext-property"></a><span data-ttu-id="70436-106">Eigenschaft "Aktions Sammlung. Context"</span><span class="sxs-lookup"><span data-stu-id="70436-106">ActionCollection.Context property</span></span>

<span data-ttu-id="70436-107">Ruft bei der Skripterstellung den Bezeichner des Prinzipals für den Task ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="70436-107">For scripting, gets or sets the identifier of the principal for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="70436-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="70436-108">Syntax</span></span>


```VB
ActionCollection.Context As String
```



## <a name="property-value"></a><span data-ttu-id="70436-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="70436-109">Property value</span></span>

<span data-ttu-id="70436-110">Der Bezeichner des Prinzipals für die Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="70436-110">The identifier of the principal for the task.</span></span> <span data-ttu-id="70436-111">Der hier angegebene Bezeichner muss mit dem Bezeichner identisch sein, der in der ID-Eigenschaft der IPrincipal-Schnittstelle angegeben ist, die den Prinzipal definiert.</span><span class="sxs-lookup"><span data-stu-id="70436-111">The identifier that is specified here must match the identifier that is specified in the Id property of the IPrincipal interface that defines the principal.</span></span>

## <a name="requirements"></a><span data-ttu-id="70436-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70436-112">Requirements</span></span>



| <span data-ttu-id="70436-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70436-113">Requirement</span></span> | <span data-ttu-id="70436-114">Wert</span><span class="sxs-lookup"><span data-stu-id="70436-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70436-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="70436-115">Minimum supported client</span></span><br/> | <span data-ttu-id="70436-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70436-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="70436-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="70436-117">Minimum supported server</span></span><br/> | <span data-ttu-id="70436-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70436-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="70436-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="70436-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="70436-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="70436-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="70436-121">DLL</span><span class="sxs-lookup"><span data-stu-id="70436-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70436-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70436-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70436-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70436-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70436-124">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="70436-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="70436-125">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="70436-125">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





