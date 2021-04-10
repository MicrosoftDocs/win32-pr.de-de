---
title: Ivmhostinfo SSE2-Eigenschaft (vpccominterfaces. h)
description: Bestimmt, ob der Prozessor den SSE2-Anweisungs Satz unterstützt. | Ivmhostinfo SSE2-Eigenschaft (vpccominterfaces. h)
ms.assetid: 1db5583c-fb8e-400e-87d3-3c4309696307
keywords:
- SSE2 Property Virtual PC
- SSE2 Property Virtual PC, ivmhostinfo-Schnittstelle
- Ivmhostinfo Interface Virtual PC, SSE2-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHostInfo.SSE2
- IVMHostInfo.get_SSE2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28286262d02512f58df8c3a00e4ba07a67c2916f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869951"
---
# <a name="ivmhostinfosse2-property"></a><span data-ttu-id="bbe81-107">Ivmhostinfo:: SSE2-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bbe81-107">IVMHostInfo::SSE2 property</span></span>

<span data-ttu-id="bbe81-108">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bbe81-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bbe81-109">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bbe81-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bbe81-110">Bestimmt, ob der Prozessor den SSE2-Anweisungs Satz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bbe81-110">Determines whether the processor supports the SSE2 instruction set.</span></span>

<span data-ttu-id="bbe81-111">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bbe81-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe81-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbe81-112">Syntax</span></span>


```C++
HRESULT get_SSE2(
  [out, retval] VARIANT_BOOL *sse2Enabled
);
```



## <a name="property-value"></a><span data-ttu-id="bbe81-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="bbe81-113">Property value</span></span>

<span data-ttu-id="bbe81-114">**True** , wenn SSE2-Anweisungen vom Host Prozessor unterstützt werden, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="bbe81-114">**TRUE** if SSE2 instructions are supported by the host processor, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bbe81-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="bbe81-115">Error codes</span></span>



| <span data-ttu-id="bbe81-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="bbe81-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="bbe81-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bbe81-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="bbe81-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bbe81-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="bbe81-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="bbe81-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="bbe81-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bbe81-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="bbe81-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="bbe81-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="bbe81-122"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bbe81-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="bbe81-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="bbe81-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bbe81-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbe81-124">Requirements</span></span>



| <span data-ttu-id="bbe81-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbe81-125">Requirement</span></span> | <span data-ttu-id="bbe81-126">Wert</span><span class="sxs-lookup"><span data-stu-id="bbe81-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe81-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bbe81-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bbe81-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbe81-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bbe81-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bbe81-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bbe81-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bbe81-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bbe81-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="bbe81-131">End of client support</span></span><br/>    | <span data-ttu-id="bbe81-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbe81-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bbe81-133">Produkt</span><span class="sxs-lookup"><span data-stu-id="bbe81-133">Product</span></span><br/>                  | <span data-ttu-id="bbe81-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bbe81-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bbe81-135">Header</span><span class="sxs-lookup"><span data-stu-id="bbe81-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbe81-136"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbe81-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bbe81-137">IID</span><span class="sxs-lookup"><span data-stu-id="bbe81-137">IID</span></span><br/>                      | <span data-ttu-id="bbe81-138">IID \_ ivmhostinfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.</span><span class="sxs-lookup"><span data-stu-id="bbe81-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="bbe81-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbe81-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbe81-140">**Ivmhostinfo**</span><span class="sxs-lookup"><span data-stu-id="bbe81-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

