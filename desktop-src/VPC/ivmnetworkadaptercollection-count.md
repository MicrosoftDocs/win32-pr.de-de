---
title: Ivmnetworkadaptercollection Count-Eigenschaft (vpccominterfaces. h)
description: Ruft die Anzahl der Netzwerkschnittstellen in dieser Auflistung ab.
ms.assetid: 0b6391fa-62fe-4db1-b0a2-565ab17157ab
keywords:
- Count-Eigenschaft virtueller PC
- Count-Eigenschaft Virtual PC, ivmnetworkadaptercollection-Schnittstelle
- Ivmnetworkadaptercollection-Schnittstelle Virtual PC, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Count
- IVMNetworkAdapterCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a287122d9829cd98f355d44e6bd408f6ca0d67a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102806"
---
# <a name="ivmnetworkadaptercollectioncount-property"></a><span data-ttu-id="52fd4-106">Ivmnetworkadaptercollection:: count (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="52fd4-106">IVMNetworkAdapterCollection::Count property</span></span>

<span data-ttu-id="52fd4-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="52fd4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="52fd4-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="52fd4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="52fd4-109">Ruft die Anzahl der Netzwerkschnittstellen in dieser Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="52fd4-109">Retrieves the number of network interfaces in this collection.</span></span>

<span data-ttu-id="52fd4-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="52fd4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="52fd4-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="52fd4-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="52fd4-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="52fd4-112">Property value</span></span>

<span data-ttu-id="52fd4-113">Die Anzahl der Netzwerkschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="52fd4-113">The number of network interfaces.</span></span>

## <a name="error-codes"></a><span data-ttu-id="52fd4-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="52fd4-114">Error codes</span></span>



| <span data-ttu-id="52fd4-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="52fd4-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="52fd4-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="52fd4-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="52fd4-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="52fd4-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="52fd4-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="52fd4-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="52fd4-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="52fd4-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="52fd4-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="52fd4-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="52fd4-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="52fd4-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="52fd4-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="52fd4-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="52fd4-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52fd4-123">Requirements</span></span>



| <span data-ttu-id="52fd4-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52fd4-124">Requirement</span></span> | <span data-ttu-id="52fd4-125">Wert</span><span class="sxs-lookup"><span data-stu-id="52fd4-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52fd4-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52fd4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="52fd4-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52fd4-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="52fd4-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52fd4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="52fd4-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="52fd4-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="52fd4-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="52fd4-130">End of client support</span></span><br/>    | <span data-ttu-id="52fd4-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52fd4-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="52fd4-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="52fd4-132">Product</span></span><br/>                  | <span data-ttu-id="52fd4-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="52fd4-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="52fd4-134">Header</span><span class="sxs-lookup"><span data-stu-id="52fd4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="52fd4-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="52fd4-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="52fd4-136">IID</span><span class="sxs-lookup"><span data-stu-id="52fd4-136">IID</span></span><br/>                      | <span data-ttu-id="52fd4-137">IID \_ ivmnetworkadaptercollection ist als ebaeafe9-EBCD-47cf-866e-ad87d735e479 definiert.</span><span class="sxs-lookup"><span data-stu-id="52fd4-137">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52fd4-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52fd4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52fd4-139">**Ivmnetworkadaptercollection**</span><span class="sxs-lookup"><span data-stu-id="52fd4-139">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

