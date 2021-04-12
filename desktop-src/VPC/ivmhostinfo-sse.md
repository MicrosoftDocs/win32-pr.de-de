---
title: Ivmhostinfo SSE-Eigenschaft (vpccominterfaces. h)
description: Bestimmt, ob der Prozessor den SSE-Anweisungs Satz unterstützt. | Ivmhostinfo SSE-Eigenschaft (vpccominterfaces. h)
ms.assetid: 135704db-757a-45b1-884a-5e26ef7d65c7
keywords:
- SSE-Eigenschaft virtueller PC
- SSE-Eigenschaft Virtual PC, ivmhostinfo-Schnittstelle
- Ivmhostinfo Interface Virtual PC, SSE-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHostInfo.SSE
- IVMHostInfo.get_SSE
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02bef292e7dbcae48b9e2a6a94e7f879212a0dfc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353479"
---
# <a name="ivmhostinfosse-property"></a><span data-ttu-id="6261e-107">Ivmhostinfo:: SSE (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6261e-107">IVMHostInfo::SSE property</span></span>

<span data-ttu-id="6261e-108">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6261e-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6261e-109">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6261e-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6261e-110">Bestimmt, ob der Prozessor den SSE-Anweisungs Satz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6261e-110">Determines whether the processor supports the SSE instruction set.</span></span>

<span data-ttu-id="6261e-111">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6261e-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6261e-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="6261e-112">Syntax</span></span>


```C++
HRESULT get_SSE(
  [out, retval] VARIANT_BOOL *sseEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="6261e-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6261e-113">Property value</span></span>

<span data-ttu-id="6261e-114">**True** , wenn SSE-Anweisungen vom Host Prozessor unterstützt werden, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="6261e-114">**TRUE** if SSE instructions are supported by the host processor, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6261e-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="6261e-115">Error codes</span></span>



| <span data-ttu-id="6261e-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="6261e-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6261e-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6261e-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6261e-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6261e-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6261e-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6261e-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="6261e-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6261e-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6261e-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="6261e-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="6261e-122"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6261e-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6261e-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6261e-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6261e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6261e-124">Requirements</span></span>



| <span data-ttu-id="6261e-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6261e-125">Requirement</span></span> | <span data-ttu-id="6261e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6261e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6261e-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6261e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6261e-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6261e-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6261e-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6261e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6261e-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6261e-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6261e-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6261e-131">End of client support</span></span><br/>    | <span data-ttu-id="6261e-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6261e-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6261e-133">Produkt</span><span class="sxs-lookup"><span data-stu-id="6261e-133">Product</span></span><br/>                  | <span data-ttu-id="6261e-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6261e-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6261e-135">Header</span><span class="sxs-lookup"><span data-stu-id="6261e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="6261e-136"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6261e-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6261e-137">IID</span><span class="sxs-lookup"><span data-stu-id="6261e-137">IID</span></span><br/>                      | <span data-ttu-id="6261e-138">IID \_ ivmhostinfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.</span><span class="sxs-lookup"><span data-stu-id="6261e-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="6261e-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6261e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6261e-140">**Ivmhostinfo**</span><span class="sxs-lookup"><span data-stu-id="6261e-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

