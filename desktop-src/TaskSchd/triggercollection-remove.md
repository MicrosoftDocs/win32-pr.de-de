---
title: TriggerCollection. Remove-Methode
description: Bei der Skripterstellung wird der angegebene Trigger aus der Auflistung der vom Task verwendeten Trigger entfernt.
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- Trigger Taskplaner, entfernen
- Remove-Methode Taskplaner
- Remove-Methode Taskplaner, TriggerCollection-Objekt
- TriggerCollection-Objekt Taskplaner, Methode entfernen
topic_type:
- apiref
api_name:
- TriggerCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e84e57b28db9b08fd7e93e85fb7bc35f60647
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340608"
---
# <a name="triggercollectionremove-method"></a><span data-ttu-id="ce557-107">TriggerCollection. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="ce557-107">TriggerCollection.Remove method</span></span>

<span data-ttu-id="ce557-108">Bei der Skripterstellung wird der angegebene Trigger aus der Auflistung der vom Task verwendeten Trigger entfernt.</span><span class="sxs-lookup"><span data-stu-id="ce557-108">For scripting, removes the specified trigger from the collection of triggers used by the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce557-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce557-109">Syntax</span></span>


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a><span data-ttu-id="ce557-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce557-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce557-111">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce557-111">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce557-112">Der Index des zu entfernenden Auslösers.</span><span class="sxs-lookup"><span data-stu-id="ce557-112">The index of the trigger to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce557-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce557-113">Return value</span></span>

<span data-ttu-id="ce557-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ce557-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce557-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce557-115">Remarks</span></span>

<span data-ttu-id="ce557-116">Beachten Sie beim Entfernen von Elementen, dass der Index für das erste Element in der Auflistung 1 ist und der Index für das letzte Element der Wert der [**TriggerCollection. count**](triggercollection-count.md) -Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="ce557-116">When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the [**TriggerCollection.Count**](triggercollection-count.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce557-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce557-117">Requirements</span></span>



| <span data-ttu-id="ce557-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce557-118">Requirement</span></span> | <span data-ttu-id="ce557-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ce557-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce557-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce557-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ce557-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce557-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ce557-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce557-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ce557-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce557-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce557-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ce557-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="ce557-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ce557-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ce557-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ce557-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce557-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce557-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce557-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce557-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce557-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="ce557-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





