---
title: Ivmvirtualmachine HasSSE2-Eigenschaft (vpccominterfaces. h)
description: Bestimmt, ob der Prozessor den SSE2-Anweisungs Satz unterstützt. | Ivmvirtualmachine HasSSE2-Eigenschaft (vpccominterfaces. h)
ms.assetid: da9860cf-d1e4-4dc4-8c4c-1b83104ffbc6
keywords:
- HasSSE2 Property Virtual PC
- HasSSE2-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, HasSSE2-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HasSSE2
- IVMVirtualMachine.get_HasSSE2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f18cd43919056a2a8563fc43b75d4c8fb8bd122a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350645"
---
# <a name="ivmvirtualmachinehassse2-property"></a><span data-ttu-id="10353-107">Ivmvirtualmachine:: HasSSE2-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="10353-107">IVMVirtualMachine::HasSSE2 property</span></span>

<span data-ttu-id="10353-108">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="10353-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="10353-109">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="10353-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="10353-110">Bestimmt, ob der Prozessor den SSE2-Anweisungs Satz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="10353-110">Determines whether the processor supports the SSE2 instruction set.</span></span>

<span data-ttu-id="10353-111">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="10353-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="10353-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="10353-112">Syntax</span></span>


```C++
HRESULT get_HasSSE2(
  [out, retval] VARIANT_BOOL *sse2Enabled
);
```



## <a name="property-value"></a><span data-ttu-id="10353-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="10353-113">Property value</span></span>

<span data-ttu-id="10353-114">**True** , wenn der Prozessor den SSE2-Anweisungs Satz unterstützt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="10353-114">**TRUE** if the processor supported the SSE2 instruction set, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="10353-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="10353-115">Error codes</span></span>



| <span data-ttu-id="10353-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="10353-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="10353-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="10353-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="10353-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="10353-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="10353-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="10353-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="10353-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="10353-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="10353-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="10353-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="10353-122"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="10353-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="10353-123">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="10353-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="10353-124"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="10353-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="10353-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="10353-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="10353-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10353-126">Requirements</span></span>



| <span data-ttu-id="10353-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10353-127">Requirement</span></span> | <span data-ttu-id="10353-128">Wert</span><span class="sxs-lookup"><span data-stu-id="10353-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="10353-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10353-129">Minimum supported client</span></span><br/> | <span data-ttu-id="10353-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10353-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="10353-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10353-131">Minimum supported server</span></span><br/> | <span data-ttu-id="10353-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="10353-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="10353-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="10353-133">End of client support</span></span><br/>    | <span data-ttu-id="10353-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="10353-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="10353-135">Produkt</span><span class="sxs-lookup"><span data-stu-id="10353-135">Product</span></span><br/>                  | <span data-ttu-id="10353-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="10353-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="10353-137">Header</span><span class="sxs-lookup"><span data-stu-id="10353-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="10353-138"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="10353-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="10353-139">IID</span><span class="sxs-lookup"><span data-stu-id="10353-139">IID</span></span><br/>                      | <span data-ttu-id="10353-140">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="10353-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="10353-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10353-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10353-142">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="10353-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

