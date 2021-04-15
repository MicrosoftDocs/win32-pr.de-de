---
title: Comhandleraction. Data (Eigenschaft)
description: Ruft bei der Skripterstellung zusätzliche Daten ab, die dem Handler zugeordnet sind, oder legt diese fest.
ms.assetid: bf4d3e77-4b2b-4622-b26b-a8f7e9aa687b
keywords:
- Daten Eigenschafts Taskplaner
- Dateneigenschaft Taskplaner, comhandleraction-Objekt
- Comhandleraction-Objekt Taskplaner, Dateneigenschaft
topic_type:
- apiref
api_name:
- ComHandlerAction.Data
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15743c3f787a591a4644081fdd63189829d2eab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392148"
---
# <a name="comhandleractiondata-property"></a><span data-ttu-id="170c1-106">Comhandleraction. Data (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="170c1-106">ComHandlerAction.Data property</span></span>

<span data-ttu-id="170c1-107">Ruft bei der Skripterstellung zusätzliche Daten ab, die dem Handler zugeordnet sind, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="170c1-107">For scripting, gets or sets additional data that is associated with the handler.</span></span>

## <a name="syntax"></a><span data-ttu-id="170c1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="170c1-108">Syntax</span></span>


```VB
ComHandlerAction.Data As String
```



## <a name="property-value"></a><span data-ttu-id="170c1-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="170c1-109">Property value</span></span>

<span data-ttu-id="170c1-110">Die Argumente, die vom Handler benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="170c1-110">The arguments that are needed by the handler.</span></span>

## <a name="remarks"></a><span data-ttu-id="170c1-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="170c1-111">Remarks</span></span>

<span data-ttu-id="170c1-112">Beim Lesen oder Schreiben von XML werden die Daten eines com-Handlers im [**Data**](taskschedulerschema-data-comhandlertype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="170c1-112">When reading or writing XML, the data of a COM handler is specified in the [**Data**](taskschedulerschema-data-comhandlertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="170c1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="170c1-113">Requirements</span></span>



| <span data-ttu-id="170c1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="170c1-114">Requirement</span></span> | <span data-ttu-id="170c1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="170c1-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="170c1-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="170c1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="170c1-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="170c1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="170c1-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="170c1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="170c1-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="170c1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="170c1-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="170c1-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="170c1-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="170c1-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="170c1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="170c1-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="170c1-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="170c1-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="170c1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="170c1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="170c1-125">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="170c1-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="170c1-126">**Comhandleraction**</span><span class="sxs-lookup"><span data-stu-id="170c1-126">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





