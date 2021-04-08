---
title: Aktioncollection. Remove-Methode
description: Entfernt bei der Skripterstellung die angegebene Aktion aus der Auflistung.
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- Remove-Methode Taskplaner
- Remove-Methode Taskplaner, Aktions Sammlungsobjekt
- Aktions Sammlungsobjekt Taskplaner, Methode entfernen
topic_type:
- apiref
api_name:
- ActionCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e110f870f4f192051b47cb3b65f0ebb41a490708
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742464"
---
# <a name="actioncollectionremove-method"></a><span data-ttu-id="25ced-106">Aktioncollection. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="25ced-106">ActionCollection.Remove method</span></span>

<span data-ttu-id="25ced-107">Entfernt bei der Skripterstellung die angegebene Aktion aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="25ced-107">For scripting, removes the specified action from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="25ced-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="25ced-108">Syntax</span></span>


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a><span data-ttu-id="25ced-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="25ced-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25ced-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25ced-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ced-111">Der Index der zu entfernenden Aktion.</span><span class="sxs-lookup"><span data-stu-id="25ced-111">The index of the action to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25ced-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25ced-112">Return value</span></span>

<span data-ttu-id="25ced-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="25ced-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25ced-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25ced-114">Remarks</span></span>

<span data-ttu-id="25ced-115">Beachten Sie beim Entfernen von Elementen, dass der Index für das erste Element in der Auflistung 1 ist und der Index für das letzte Element der Wert der Eigenschaft " [**Aktions Auflistung. count**](actioncollection-count.md) " ist.</span><span class="sxs-lookup"><span data-stu-id="25ced-115">When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the [**ActionCollection.Count**](actioncollection-count.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="25ced-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25ced-116">Requirements</span></span>



| <span data-ttu-id="25ced-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25ced-117">Requirement</span></span> | <span data-ttu-id="25ced-118">Wert</span><span class="sxs-lookup"><span data-stu-id="25ced-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25ced-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25ced-119">Minimum supported client</span></span><br/> | <span data-ttu-id="25ced-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25ced-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="25ced-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25ced-121">Minimum supported server</span></span><br/> | <span data-ttu-id="25ced-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25ced-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="25ced-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="25ced-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="25ced-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="25ced-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="25ced-125">DLL</span><span class="sxs-lookup"><span data-stu-id="25ced-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25ced-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25ced-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25ced-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25ced-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25ced-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="25ced-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="25ced-129">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="25ced-129">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





