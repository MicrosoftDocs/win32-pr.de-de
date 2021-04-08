---
title: Comhandleraction. ClassID (Eigenschaft)
description: Ruft bei der Skripterstellung den Bezeichner der Handlerklasse ab oder legt ihn fest.
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- ClassID-Eigenschaft Taskplaner
- ClassID-Eigenschaft Taskplaner, comhandleraction-Objekt
- Comhandleraction-Objekt Taskplaner, ClassID-Eigenschaft
topic_type:
- apiref
api_name:
- ComHandlerAction.ClassId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30409d5ea8067d1148bf42c88e2a3d1bb6f65ad1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740865"
---
# <a name="comhandleractionclassid-property"></a><span data-ttu-id="3053a-106">Comhandleraction. ClassID (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3053a-106">ComHandlerAction.ClassId property</span></span>

<span data-ttu-id="3053a-107">Ruft bei der Skripterstellung den Bezeichner der Handlerklasse ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="3053a-107">For scripting, gets or sets the identifier of the handler class.</span></span>

## <a name="syntax"></a><span data-ttu-id="3053a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3053a-108">Syntax</span></span>


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a><span data-ttu-id="3053a-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3053a-109">Property value</span></span>

<span data-ttu-id="3053a-110">Der Bezeichner der Klasse, die den auszulösende Handler definiert.</span><span class="sxs-lookup"><span data-stu-id="3053a-110">The identifier of the class that defines the handler to be fired.</span></span>

## <a name="remarks"></a><span data-ttu-id="3053a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3053a-111">Remarks</span></span>

<span data-ttu-id="3053a-112">Beim Lesen oder Schreiben von XML wird die Klasse eines com-Handlers im [**ClassID-**](taskschedulerschema-classid-comhandlertype-element.md) Element des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="3053a-112">When reading or writing XML, the class of a COM handler is specified in the [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="3053a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3053a-113">Requirements</span></span>



| <span data-ttu-id="3053a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3053a-114">Requirement</span></span> | <span data-ttu-id="3053a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3053a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3053a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3053a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3053a-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3053a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3053a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3053a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3053a-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3053a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3053a-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3053a-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="3053a-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3053a-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3053a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3053a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3053a-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3053a-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3053a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3053a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3053a-125">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="3053a-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="3053a-126">**Comhandleraction**</span><span class="sxs-lookup"><span data-stu-id="3053a-126">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





