---
title: IBackgroundCopyFile5-Schnittstelle (deliveryoptimization. h)
description: Verwenden Sie diese Schnittstelle, um allgemeine Eigenschaften von Dateiübertragungen zur Übermittlungs Optimierung (Do) zu erhalten oder festzulegen.
ms.assetid: 2D729717-62D2-4C69-92FE-F4289EC48DF1
keywords:
- IBackgroundCopyFile5-Schnittstelle
- IBackgroundCopyFile5-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f23fdb99ba24b4faeca7a65930bf83d4634a979
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103506"
---
# <a name="ibackgroundcopyfile5-interface"></a><span data-ttu-id="fa850-105">IBackgroundCopyFile5-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fa850-105">IBackgroundCopyFile5 interface</span></span>

<span data-ttu-id="fa850-106">Verwenden Sie diese Schnittstelle, um allgemeine Eigenschaften von Dateiübertragungen zur Übermittlungs Optimierung (Do) zu erhalten oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="fa850-106">Use this interface to get or set generic properties of Delivery Optimization (DO) file transfers.</span></span>

<span data-ttu-id="fa850-107">Um einen **IBackgroundCopyFile5** -Schnittstellen Zeiger abzurufen, verwenden Sie die **ibackgroundcopyfile:: QueryInterface** -Methode mithilfe __uuidof (IBackgroundCopyFile5) für den Schnittstellen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="fa850-107">To get an **IBackgroundCopyFile5** interface pointer, call the **IBackgroundCopyFile::QueryInterface** method using __uuidof(IBackgroundCopyFile5) for the interface identifier.</span></span>

## <a name="members"></a><span data-ttu-id="fa850-108">Member</span><span class="sxs-lookup"><span data-stu-id="fa850-108">Members</span></span>

<span data-ttu-id="fa850-109">Die **IBackgroundCopyFile5** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fa850-109">The **IBackgroundCopyFile5** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fa850-110">**IBackgroundCopyFile5** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fa850-110">**IBackgroundCopyFile5** also has these types of members:</span></span>

-   [<span data-ttu-id="fa850-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="fa850-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fa850-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="fa850-112">Methods</span></span>

<span data-ttu-id="fa850-113">Die **IBackgroundCopyFile5** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="fa850-113">The **IBackgroundCopyFile5** interface has these methods.</span></span>



| <span data-ttu-id="fa850-114">Methode</span><span class="sxs-lookup"><span data-stu-id="fa850-114">Method</span></span>                                                  | <span data-ttu-id="fa850-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa850-115">Description</span></span>                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="fa850-116">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="fa850-116">**GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md) | <span data-ttu-id="fa850-117">Ruft den Wert einer generischen backgroundcopyfile-Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="fa850-117">Gets the value of a generic BackgroundCopyFile property.</span></span><br/> |
| [<span data-ttu-id="fa850-118">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="fa850-118">**SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md) | <span data-ttu-id="fa850-119">Legt den Wert einer generischen backgroundcopyfile-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="fa850-119">Sets the value of a generic BackgroundCopyFile property.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fa850-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa850-120">Requirements</span></span>



| <span data-ttu-id="fa850-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa850-121">Requirement</span></span> | <span data-ttu-id="fa850-122">Wert</span><span class="sxs-lookup"><span data-stu-id="fa850-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa850-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa850-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fa850-124">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa850-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fa850-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa850-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fa850-126">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa850-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fa850-127">Header</span><span class="sxs-lookup"><span data-stu-id="fa850-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa850-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa850-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa850-129">IDL</span><span class="sxs-lookup"><span data-stu-id="fa850-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa850-130"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa850-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="fa850-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fa850-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa850-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa850-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="fa850-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fa850-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa850-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa850-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="fa850-135">IID</span><span class="sxs-lookup"><span data-stu-id="fa850-135">IID</span></span><br/>                      | <span data-ttu-id="fa850-136">IID_IBackgroundCopyFile5 ist als "85c1657f-DAFC-40e8-8834-df18ea25717e" definiert.</span><span class="sxs-lookup"><span data-stu-id="fa850-136">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="fa850-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa850-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa850-138">**Ibackgroundcopyfile**</span><span class="sxs-lookup"><span data-stu-id="fa850-138">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="fa850-139">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="fa850-139">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

