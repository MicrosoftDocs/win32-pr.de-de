---
title: Ivmhostinfo logicalprocessorcount-Eigenschaft (vpccominterfaces. h)
description: Ruft die Anzahl der logischen Prozessoren auf dem Host Computer ab.
ms.assetid: bf978a80-9a21-426a-ac18-109f20d38cbb
keywords:
- Logicalprocessorcount-Eigenschaft virtueller PC
- Logicalprocessorcount-Eigenschaft Virtual PC, ivmhostinfo-Schnittstelle
- Ivmhostinfo Interface Virtual PC, logicalprocessorcount (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMHostInfo.LogicalProcessorCount
- IVMHostInfo.get_LogicalProcessorCount
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7668bb4332a41b1cae809c6c2f29a8eac99bade
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337899"
---
# <a name="ivmhostinfologicalprocessorcount-property"></a><span data-ttu-id="769fa-106">Ivmhostinfo:: logicalprocessorcount (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="769fa-106">IVMHostInfo::LogicalProcessorCount property</span></span>

<span data-ttu-id="769fa-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="769fa-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="769fa-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="769fa-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="769fa-109">Ruft die Anzahl der logischen Prozessoren auf dem Host Computer ab.</span><span class="sxs-lookup"><span data-stu-id="769fa-109">Retrieves the number of logical processors in the host machine.</span></span>

<span data-ttu-id="769fa-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="769fa-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="769fa-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="769fa-111">Syntax</span></span>


```C++
HRESULT get_LogicalProcessorCount(
  [out, retval] long *processorCount
);
```



## <a name="property-value"></a><span data-ttu-id="769fa-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="769fa-112">Property value</span></span>

<span data-ttu-id="769fa-113">Die Anzahl der logischen Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="769fa-113">The number of logical processors.</span></span>

## <a name="error-codes"></a><span data-ttu-id="769fa-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="769fa-114">Error codes</span></span>



| <span data-ttu-id="769fa-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="769fa-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="769fa-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="769fa-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="769fa-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="769fa-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="769fa-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="769fa-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="769fa-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="769fa-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="769fa-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="769fa-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="769fa-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="769fa-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="769fa-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="769fa-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="769fa-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="769fa-123">Requirements</span></span>



| <span data-ttu-id="769fa-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="769fa-124">Requirement</span></span> | <span data-ttu-id="769fa-125">Wert</span><span class="sxs-lookup"><span data-stu-id="769fa-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="769fa-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="769fa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="769fa-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="769fa-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="769fa-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="769fa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="769fa-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="769fa-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="769fa-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="769fa-130">End of client support</span></span><br/>    | <span data-ttu-id="769fa-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="769fa-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="769fa-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="769fa-132">Product</span></span><br/>                  | <span data-ttu-id="769fa-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="769fa-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="769fa-134">Header</span><span class="sxs-lookup"><span data-stu-id="769fa-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="769fa-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="769fa-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="769fa-136">IID</span><span class="sxs-lookup"><span data-stu-id="769fa-136">IID</span></span><br/>                      | <span data-ttu-id="769fa-137">IID \_ ivmhostinfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.</span><span class="sxs-lookup"><span data-stu-id="769fa-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="769fa-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="769fa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="769fa-139">**Ivmhostinfo**</span><span class="sxs-lookup"><span data-stu-id="769fa-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

