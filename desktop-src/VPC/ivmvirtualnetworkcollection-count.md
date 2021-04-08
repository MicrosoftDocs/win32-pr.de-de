---
title: Ivmvirtualnetworkcollection Count-Eigenschaft (vpccominterfaces. h)
description: Ruft die Anzahl der virtuellen Netzwerke in dieser Auflistung ab.
ms.assetid: a9a3ab48-74a0-498e-936e-a99c7b027a85
keywords:
- Count-Eigenschaft virtueller PC
- Count-Eigenschaft Virtual PC, ivmvirtualnetworkcollection-Schnittstelle
- Ivmvirtualnetworkcollection-Schnittstelle Virtual PC, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Count
- IVMVirtualNetworkCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82e3244327d5840c8f7cce8ed498f90cd406d573
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742736"
---
# <a name="ivmvirtualnetworkcollectioncount-property"></a><span data-ttu-id="8e2b2-106">Ivmvirtualnetworkcollection:: count (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8e2b2-106">IVMVirtualNetworkCollection::Count property</span></span>

<span data-ttu-id="8e2b2-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8e2b2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8e2b2-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8e2b2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8e2b2-109">Ruft die Anzahl der virtuellen Netzwerke in dieser Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="8e2b2-109">Retrieves the number of virtual networks in this collection.</span></span>

<span data-ttu-id="8e2b2-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8e2b2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e2b2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e2b2-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="8e2b2-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8e2b2-112">Property value</span></span>

<span data-ttu-id="8e2b2-113">Die Anzahl der virtuellen Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="8e2b2-113">The number of virtual networks.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8e2b2-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="8e2b2-114">Error codes</span></span>



| <span data-ttu-id="8e2b2-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="8e2b2-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="8e2b2-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8e2b2-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8e2b2-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8e2b2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="8e2b2-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e2b2-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="8e2b2-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8e2b2-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="8e2b2-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="8e2b2-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="8e2b2-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8e2b2-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="8e2b2-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8e2b2-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8e2b2-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e2b2-123">Requirements</span></span>



| <span data-ttu-id="8e2b2-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e2b2-124">Requirement</span></span> | <span data-ttu-id="8e2b2-125">Wert</span><span class="sxs-lookup"><span data-stu-id="8e2b2-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e2b2-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e2b2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8e2b2-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e2b2-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8e2b2-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e2b2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8e2b2-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8e2b2-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8e2b2-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="8e2b2-130">End of client support</span></span><br/>    | <span data-ttu-id="8e2b2-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8e2b2-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="8e2b2-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="8e2b2-132">Product</span></span><br/>                  | <span data-ttu-id="8e2b2-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8e2b2-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="8e2b2-134">Header</span><span class="sxs-lookup"><span data-stu-id="8e2b2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e2b2-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e2b2-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="8e2b2-136">IID</span><span class="sxs-lookup"><span data-stu-id="8e2b2-136">IID</span></span><br/>                      | <span data-ttu-id="8e2b2-137">IID \_ ivmvirtualnetworkcollection ist als 8ed680be-4242-4b2a-A21C-1982d8b0f. definiert.</span><span class="sxs-lookup"><span data-stu-id="8e2b2-137">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e2b2-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e2b2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e2b2-139">**Ivmvirtualnetworkcollection**</span><span class="sxs-lookup"><span data-stu-id="8e2b2-139">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

