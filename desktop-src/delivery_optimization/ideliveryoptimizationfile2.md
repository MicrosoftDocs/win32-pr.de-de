---
title: IDeliveryOptimizationFile2-Schnittstelle
description: Der IDeliveryOptimizationFile2 unterstützt das Festlegen und das erhalten Optionaler Dateieigenschaften.
keywords:
- IDeliveryOptimizationFile2-Schnittstelle
- IDeliveryOptimizationFile2-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a45efd821116b24e883ec29d494a1d588559f57a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040377"
---
# <a name="ideliveryoptimizationfile2-interface"></a><span data-ttu-id="57438-105">IDeliveryOptimizationFile2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="57438-105">IDeliveryOptimizationFile2 interface</span></span>

<span data-ttu-id="57438-106">Der **IDeliveryOptimizationFile2** unterstützt das Festlegen und das erhalten Optionaler Dateieigenschaften.</span><span class="sxs-lookup"><span data-stu-id="57438-106">The **IDeliveryOptimizationFile2** supports setting and getting optional file properties.</span></span> 

## <a name="members"></a><span data-ttu-id="57438-107">Member</span><span class="sxs-lookup"><span data-stu-id="57438-107">Members</span></span>

<span data-ttu-id="57438-108">Die **IDeliveryOptimizationFile2** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="57438-108">The **IDeliveryOptimizationFile2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="57438-109">**IDeliveryOptimizationFile2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="57438-109">**IDeliveryOptimizationFile2** also has these types of members:</span></span>

- [<span data-ttu-id="57438-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="57438-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="57438-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="57438-111">Methods</span></span>

<span data-ttu-id="57438-112">Die **IDeliveryOptimizationFile2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="57438-112">The **IDeliveryOptimizationFile2** interface has these methods.</span></span>

| <span data-ttu-id="57438-113">Methode</span><span class="sxs-lookup"><span data-stu-id="57438-113">Method</span></span>                                                 | <span data-ttu-id="57438-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57438-114">Description</span></span>                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="57438-115">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="57438-115">**GetProperty**</span></span>](ideliveryoptimizationfile2-getproperty.md)  | <span data-ttu-id="57438-116">Diese Methode gibt eine einzelne Eigenschaft der do-Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="57438-116">This method returns a single property of the DO file.</span></span> |
| [<span data-ttu-id="57438-117">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="57438-117">**SetProperty**</span></span>](ideliveryoptimizationfile2-setproperty.md)  | <span data-ttu-id="57438-118">Diese Methode legt eine einzelne Eigenschaft der do-Datei fest.</span><span class="sxs-lookup"><span data-stu-id="57438-118">This method sets a single property of the DO file.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="57438-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57438-119">Requirements</span></span>

| <span data-ttu-id="57438-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57438-120">Requirement</span></span> | <span data-ttu-id="57438-121">Wert</span><span class="sxs-lookup"><span data-stu-id="57438-121">Value</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="57438-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57438-122">Minimum supported client</span></span>      | <span data-ttu-id="57438-123">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57438-123">Windows 10, version 1803 \[desktop apps only\]</span></span>                                    |
| <span data-ttu-id="57438-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57438-124">Minimum supported server</span></span>      | <span data-ttu-id="57438-125">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57438-125">Windows Server, version 1709 \[desktop apps only\]</span></span>                                |
| <span data-ttu-id="57438-126">Header</span><span class="sxs-lookup"><span data-stu-id="57438-126">Header</span></span>                        | <span data-ttu-id="57438-127">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="57438-127">Deliveryoptimization.h</span></span>                                                            |
| <span data-ttu-id="57438-128">IDL</span><span class="sxs-lookup"><span data-stu-id="57438-128">IDL</span></span>                           | <span data-ttu-id="57438-129">Deliveryoptimization. idl</span><span class="sxs-lookup"><span data-stu-id="57438-129">DeliveryOptimization.idl</span></span>                                                          |
| <span data-ttu-id="57438-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="57438-130">Library</span></span>                       | <span data-ttu-id="57438-131">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="57438-131">Dosvc.lib</span></span>                                                                         |
| <span data-ttu-id="57438-132">DLL</span><span class="sxs-lookup"><span data-stu-id="57438-132">DLL</span></span>                           | <span data-ttu-id="57438-133">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="57438-133">Dosvc.dll</span></span>                                                                         |
| <span data-ttu-id="57438-134">IID</span><span class="sxs-lookup"><span data-stu-id="57438-134">IID</span></span>                           | <span data-ttu-id="57438-135">IID_IDeliveryOptimizationFile2 ist als 3a87296f -6ec2-4126-ab29-E3F 8dc4cc390 definiert.</span><span class="sxs-lookup"><span data-stu-id="57438-135">IID_IDeliveryOptimizationFile2 is defined as 3A87296F-6EC2-4126-AB29-E3F8DC4CC390</span></span> |
