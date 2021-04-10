---
title: Ibackgroundcopymanager-Schnittstelle (deliveryoptimization. h)
description: Erstellt Übertragungs Aufträge, Ruft ein Enumeratorobjekt ab, das die Aufträge in der Warteschlange enthält, und ruft einzelne Aufträge aus der Warteschlange ab.
ms.assetid: EA7CB5CE-5E95-4C6D-8026-4B8375EE216A
keywords:
- Ibackgroundcopymanager-Schnittstelle
- Ibackgroundcopymanager-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyManager
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fa752398c0849c987e2a28b804e65a8361e15b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956590"
---
# <a name="ibackgroundcopymanager-interface"></a><span data-ttu-id="8dae7-105">Ibackgroundcopymanager-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8dae7-105">IBackgroundCopyManager interface</span></span>

<span data-ttu-id="8dae7-106">Erstellt Übertragungs Aufträge, Ruft ein Enumeratorobjekt ab, das die Aufträge in der Warteschlange enthält, und ruft einzelne Aufträge aus der Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="8dae7-106">Creates transfer jobs, retrieves an enumerator object that contains the jobs in the queue, and retrieves individual jobs from the queue.</span></span>

## <a name="members"></a><span data-ttu-id="8dae7-107">Member</span><span class="sxs-lookup"><span data-stu-id="8dae7-107">Members</span></span>

<span data-ttu-id="8dae7-108">Die **ibackgroundcopymanager** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8dae7-108">The **IBackgroundCopyManager** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8dae7-109">**Ibackgroundcopymanager** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8dae7-109">**IBackgroundCopyManager** also has these types of members:</span></span>

-   [<span data-ttu-id="8dae7-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="8dae7-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8dae7-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="8dae7-111">Methods</span></span>

<span data-ttu-id="8dae7-112">Die **ibackgroundcopymanager** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8dae7-112">The **IBackgroundCopyManager** interface has these methods.</span></span>



| <span data-ttu-id="8dae7-113">Methode</span><span class="sxs-lookup"><span data-stu-id="8dae7-113">Method</span></span>                                                | <span data-ttu-id="8dae7-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8dae7-114">Description</span></span>                                          |
|:------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="8dae7-115">**CreateJob**</span><span class="sxs-lookup"><span data-stu-id="8dae7-115">**CreateJob**</span></span>](ibackgroundcopymanager-createjob.md) | <span data-ttu-id="8dae7-116">Erstellt einen Übertragungs Auftrag.</span><span class="sxs-lookup"><span data-stu-id="8dae7-116">Creates a transfer job.</span></span><br/>                   |
| [<span data-ttu-id="8dae7-117">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="8dae7-117">**GetJob**</span></span>](ibackgroundcopymanager-getjob.md)       | <span data-ttu-id="8dae7-118">Ruft einen angegebenen Auftrag aus der Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="8dae7-118">Retrieves a specified job from the queue.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8dae7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8dae7-119">Requirements</span></span>



| <span data-ttu-id="8dae7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8dae7-120">Requirement</span></span> | <span data-ttu-id="8dae7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8dae7-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dae7-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8dae7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8dae7-123">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8dae7-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8dae7-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8dae7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8dae7-125">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8dae7-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8dae7-126">Header</span><span class="sxs-lookup"><span data-stu-id="8dae7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dae7-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dae7-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="8dae7-128">IDL</span><span class="sxs-lookup"><span data-stu-id="8dae7-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8dae7-129"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8dae7-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="8dae7-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8dae7-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="8dae7-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8dae7-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="8dae7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8dae7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8dae7-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8dae7-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="8dae7-134">IID</span><span class="sxs-lookup"><span data-stu-id="8dae7-134">IID</span></span><br/>                      | <span data-ttu-id="8dae7-135">IID_IBackgroundCopyManager ist als 5ce34c0d-0dc9-4c1f -897c-daa1b78cee7c definiert.</span><span class="sxs-lookup"><span data-stu-id="8dae7-135">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="8dae7-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dae7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dae7-137">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="8dae7-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

