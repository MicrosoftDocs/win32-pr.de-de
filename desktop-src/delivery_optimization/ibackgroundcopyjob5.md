---
title: IBackgroundCopyJob5-Schnittstelle (deliveryoptimization. h)
description: Verwenden Sie diese Schnittstelle, um mehrere optionale Verhalten eines Auftrags abzufragen oder festzulegen.
ms.assetid: C4706E10-40E6-489B-9772-59D581781038
keywords:
- IBackgroundCopyJob5-Schnittstelle
- IBackgroundCopyJob5-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e76898f7bbfe4d4dc34aec035b842e6671091630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105326"
---
# <a name="ibackgroundcopyjob5-interface"></a><span data-ttu-id="924d5-105">IBackgroundCopyJob5-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="924d5-105">IBackgroundCopyJob5 interface</span></span>

<span data-ttu-id="924d5-106">Verwenden Sie diese Schnittstelle, um mehrere optionale Verhalten eines Auftrags abzufragen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="924d5-106">Use this interface to query or set several optional behaviors of a job.</span></span>

<span data-ttu-id="924d5-107">Um diese Schnittstelle abzurufen, nennen Sie die **ibackgroundcopyjob:: QueryInterface** -Methode mithilfe von `__uuidof(IBackgroundCopyJob5)` als Schnittstellen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="924d5-107">To get this interface, call the **IBackgroundCopyJob::QueryInterface** method using `__uuidof(IBackgroundCopyJob5)` as the interface identifier.</span></span>

## <a name="members"></a><span data-ttu-id="924d5-108">Member</span><span class="sxs-lookup"><span data-stu-id="924d5-108">Members</span></span>

<span data-ttu-id="924d5-109">Die **IBackgroundCopyJob5** -Schnittstelle erbt von [**ibackgroundcopyjob**](ibackgroundcopyjob-.md).</span><span class="sxs-lookup"><span data-stu-id="924d5-109">The **IBackgroundCopyJob5** interface inherits from [**IBackgroundCopyJob**](ibackgroundcopyjob-.md).</span></span> <span data-ttu-id="924d5-110">**IBackgroundCopyJob5** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="924d5-110">**IBackgroundCopyJob5** also has these types of members:</span></span>

-   [<span data-ttu-id="924d5-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="924d5-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="924d5-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="924d5-112">Methods</span></span>

<span data-ttu-id="924d5-113">Die **IBackgroundCopyJob5** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="924d5-113">The **IBackgroundCopyJob5** interface has these methods.</span></span>



| <span data-ttu-id="924d5-114">Methode</span><span class="sxs-lookup"><span data-stu-id="924d5-114">Method</span></span>                                                 | <span data-ttu-id="924d5-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="924d5-115">Description</span></span>                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="924d5-116">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="924d5-116">**GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md) | <span data-ttu-id="924d5-117">Eine generische Methode zum erhalten von Aufgaben Auftrags Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="924d5-117">A generic method for getting DO job properties.</span></span><br/> |
| [<span data-ttu-id="924d5-118">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="924d5-118">**SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md) | <span data-ttu-id="924d5-119">Eine generische Methode zum Festlegen von Auftrags Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="924d5-119">A generic method for setting DO job properties.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="924d5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="924d5-120">Requirements</span></span>



| <span data-ttu-id="924d5-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="924d5-121">Requirement</span></span> | <span data-ttu-id="924d5-122">Wert</span><span class="sxs-lookup"><span data-stu-id="924d5-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="924d5-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="924d5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="924d5-124">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="924d5-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="924d5-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="924d5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="924d5-126">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="924d5-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="924d5-127">Header</span><span class="sxs-lookup"><span data-stu-id="924d5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="924d5-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="924d5-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="924d5-129">IDL</span><span class="sxs-lookup"><span data-stu-id="924d5-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="924d5-130"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="924d5-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="924d5-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="924d5-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="924d5-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="924d5-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="924d5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="924d5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="924d5-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="924d5-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="924d5-135">IID</span><span class="sxs-lookup"><span data-stu-id="924d5-135">IID</span></span><br/>                      | <span data-ttu-id="924d5-136">IID_IBackgroundCopyJob5 ist als E847030C-bbba-4657-AF6D-484aa42bf1fe definiert.</span><span class="sxs-lookup"><span data-stu-id="924d5-136">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="924d5-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="924d5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="924d5-138">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="924d5-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





