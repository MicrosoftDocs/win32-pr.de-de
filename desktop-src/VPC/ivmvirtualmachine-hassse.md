---
title: Ivmvirtualmachine-hassse-Eigenschaft (vpccominterfaces. h)
description: Bestimmt, ob der Prozessor den SSE-Anweisungs Satz unterstützt. | Ivmvirtualmachine-hassse-Eigenschaft (vpccominterfaces. h)
ms.assetid: 949dd93b-aa4e-4506-91ed-ed625a535d5f
keywords:
- "\"Hassse Property Virtual PC\""
- Hassse-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, hassse-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HasSSE
- IVMVirtualMachine.get_HasSSE
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a367ddc7b32ff4627976d2c5b63ec3565dbace53
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103870023"
---
# <a name="ivmvirtualmachinehassse-property"></a><span data-ttu-id="d10e4-107">Ivmvirtualmachine:: hassse-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d10e4-107">IVMVirtualMachine::HasSSE property</span></span>

<span data-ttu-id="d10e4-108">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d10e4-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d10e4-109">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d10e4-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d10e4-110">Bestimmt, ob der Prozessor den SSE-Anweisungs Satz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d10e4-110">Determines whether the processor supports the SSE instruction set.</span></span>

<span data-ttu-id="d10e4-111">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d10e4-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d10e4-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="d10e4-112">Syntax</span></span>


```C++
HRESULT get_HasSSE(
  [out, retval] VARIANT_BOOL *sseEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="d10e4-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d10e4-113">Property value</span></span>

<span data-ttu-id="d10e4-114">**True** , wenn der Prozessor den SSE-Anweisungs Satz unterstützt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="d10e4-114">**TRUE** if the processor supported the SSE instruction set, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d10e4-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d10e4-115">Error codes</span></span>



| <span data-ttu-id="d10e4-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="d10e4-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d10e4-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d10e4-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d10e4-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d10e4-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d10e4-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d10e4-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="d10e4-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d10e4-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d10e4-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="d10e4-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="d10e4-122"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="d10e4-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="d10e4-123">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="d10e4-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="d10e4-124"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d10e4-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d10e4-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d10e4-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d10e4-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d10e4-126">Requirements</span></span>



| <span data-ttu-id="d10e4-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d10e4-127">Requirement</span></span> | <span data-ttu-id="d10e4-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d10e4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d10e4-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d10e4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d10e4-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d10e4-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d10e4-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d10e4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d10e4-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d10e4-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d10e4-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d10e4-133">End of client support</span></span><br/>    | <span data-ttu-id="d10e4-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d10e4-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d10e4-135">Produkt</span><span class="sxs-lookup"><span data-stu-id="d10e4-135">Product</span></span><br/>                  | <span data-ttu-id="d10e4-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d10e4-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d10e4-137">Header</span><span class="sxs-lookup"><span data-stu-id="d10e4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d10e4-138"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d10e4-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d10e4-139">IID</span><span class="sxs-lookup"><span data-stu-id="d10e4-139">IID</span></span><br/>                      | <span data-ttu-id="d10e4-140">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="d10e4-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d10e4-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d10e4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d10e4-142">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="d10e4-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

