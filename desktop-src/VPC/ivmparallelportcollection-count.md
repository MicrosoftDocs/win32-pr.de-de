---
title: Ivmparallelportcollection-Anzahl (Eigenschaft) (vpccominterfaces. h)
description: Anzahl paralleler Ports in dieser Sammlung.
ms.assetid: f2f4cac4-bb63-4ac2-ba6e-321a8a29c6d4
keywords:
- Count-Eigenschaft virtueller PC
- Count-Eigenschaft Virtual PC, ivmparallelportcollection-Schnittstelle
- Ivmparallelportcollection-Schnittstelle Virtual PC, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Count
- IVMParallelPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0bb1af40f0e4d15b7eae65e18a8d9910deb769c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956560"
---
# <a name="ivmparallelportcollectioncount-property"></a><span data-ttu-id="3998f-106">Ivmparallelportcollection:: Count-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3998f-106">IVMParallelPortCollection::Count property</span></span>

<span data-ttu-id="3998f-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3998f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3998f-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3998f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3998f-109">Ruft die Anzahl paralleler Ports in dieser Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="3998f-109">Retrieves the number of parallel ports in this collection.</span></span>

<span data-ttu-id="3998f-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3998f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3998f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3998f-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="3998f-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3998f-112">Property value</span></span>

<span data-ttu-id="3998f-113">Die Anzahl paralleler Ports.</span><span class="sxs-lookup"><span data-stu-id="3998f-113">The number of parallel ports.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3998f-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3998f-114">Error codes</span></span>



| <span data-ttu-id="3998f-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="3998f-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="3998f-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3998f-116">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="3998f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3998f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="3998f-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="3998f-118">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="3998f-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3998f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="3998f-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="3998f-120">The parameter is **NULL**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="3998f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3998f-121">Requirements</span></span>



| <span data-ttu-id="3998f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3998f-122">Requirement</span></span> | <span data-ttu-id="3998f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3998f-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3998f-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3998f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3998f-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3998f-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3998f-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3998f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3998f-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3998f-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3998f-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3998f-128">End of client support</span></span><br/>    | <span data-ttu-id="3998f-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3998f-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3998f-130">Produkt</span><span class="sxs-lookup"><span data-stu-id="3998f-130">Product</span></span><br/>                  | <span data-ttu-id="3998f-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3998f-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3998f-132">Header</span><span class="sxs-lookup"><span data-stu-id="3998f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3998f-133"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3998f-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3998f-134">IID</span><span class="sxs-lookup"><span data-stu-id="3998f-134">IID</span></span><br/>                      | <span data-ttu-id="3998f-135">IID \_ ivmparallelportcollection ist als 27c3e036-198l-430c-8735-6e652f 7203fd definiert.</span><span class="sxs-lookup"><span data-stu-id="3998f-135">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="3998f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3998f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3998f-137">**Ivmparallelportcollection**</span><span class="sxs-lookup"><span data-stu-id="3998f-137">**IVMParallelPortCollection**</span></span>](ivmparallelportcollection.md)
</dt> </dl>

 

