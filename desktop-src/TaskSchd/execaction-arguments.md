---
title: Execaction. Arguments (Eigenschaft)
description: Ruft bei der Skripterstellung die Argumente ab, die dem Befehlszeilen Vorgang zugeordnet sind, oder legt diese fest.
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Arguments-Eigenschaft Taskplaner
- Arguments-Eigenschaft Taskplaner, execaction-Objekt
- Execaction-Objekt Taskplaner, Arguments-Eigenschaft
topic_type:
- apiref
api_name:
- ExecAction.Arguments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4207a9fbfb60d9e45c15e174a33e7d6ab66e5fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949647"
---
# <a name="execactionarguments-property"></a><span data-ttu-id="ffbbf-106">Execaction. Arguments (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ffbbf-106">ExecAction.Arguments property</span></span>

<span data-ttu-id="ffbbf-107">Ruft bei der Skripterstellung die Argumente ab, die dem Befehlszeilen Vorgang zugeordnet sind, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="ffbbf-107">For scripting, gets or sets the arguments associated with the command-line operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffbbf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffbbf-108">Syntax</span></span>


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a><span data-ttu-id="ffbbf-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ffbbf-109">Property value</span></span>

<span data-ttu-id="ffbbf-110">Die Argumente, die für den Befehlszeilen Vorgang erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ffbbf-110">The arguments that are needed by the command-line operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffbbf-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffbbf-111">Remarks</span></span>

<span data-ttu-id="ffbbf-112">Beim Lesen oder Schreiben von XML werden die Befehlszeilen-Vorgangs Argumente im [**Arguments**](taskschedulerschema-arguments-exectype-element.md) -Element des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="ffbbf-112">When reading or writing XML, the command-line operation arguments are specified in the [**Arguments**](taskschedulerschema-arguments-exectype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffbbf-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffbbf-113">Requirements</span></span>



| <span data-ttu-id="ffbbf-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffbbf-114">Requirement</span></span> | <span data-ttu-id="ffbbf-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ffbbf-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffbbf-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ffbbf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ffbbf-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffbbf-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ffbbf-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ffbbf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ffbbf-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffbbf-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ffbbf-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ffbbf-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="ffbbf-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ffbbf-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ffbbf-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ffbbf-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffbbf-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffbbf-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffbbf-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffbbf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffbbf-125">**Execaction**</span><span class="sxs-lookup"><span data-stu-id="ffbbf-125">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="ffbbf-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="ffbbf-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





