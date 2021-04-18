---
title: Ivmhostinfo processorfeaturesstring-Eigenschaft (vpccominterfaces. h)
description: Ruft die Listen Features ab, die vom Host Prozessor unterstützt werden.
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- Processorfeaturesstring-Eigenschaft virtueller PC
- Processorfeaturesstring-Eigenschaft Virtual PC, ivmhostinfo-Schnittstelle
- Ivmhostinfo Interface Virtual PC, processorfeaturesstring (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorFeaturesString
- IVMHostInfo.get_ProcessorFeaturesString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118aaa2eabe7ddb2fd608892775a17eac6a77d16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337487"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a><span data-ttu-id="52fb4-106">Ivmhostinfo::P rocess orfeaturesstring-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="52fb4-106">IVMHostInfo::ProcessorFeaturesString property</span></span>

<span data-ttu-id="52fb4-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="52fb4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="52fb4-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="52fb4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="52fb4-109">Ruft die Listen Features ab, die vom Host Prozessor unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="52fb4-109">Retrieves the list features supported by the host processor.</span></span>

<span data-ttu-id="52fb4-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="52fb4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="52fb4-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="52fb4-111">Syntax</span></span>


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a><span data-ttu-id="52fb4-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="52fb4-112">Property value</span></span>

<span data-ttu-id="52fb4-113">Eine durch Trennzeichen getrennte Liste von Features.</span><span class="sxs-lookup"><span data-stu-id="52fb4-113">A comma-delimited list of features.</span></span> <span data-ttu-id="52fb4-114">Ein Beispiel wäre "MMX, SSE, SSE2, x86-64".</span><span class="sxs-lookup"><span data-stu-id="52fb4-114">An example would be "MMX,SSE,SSE2,x86-64".</span></span>



| <span data-ttu-id="52fb4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="52fb4-115">Value</span></span>                                                                                 | <span data-ttu-id="52fb4-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="52fb4-116">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="52fb4-117"><dt>"AMD-V"</dt></span><span class="sxs-lookup"><span data-stu-id="52fb4-117"><dt>"AMD-V"</dt></span></span> </dl>    | <span data-ttu-id="52fb4-118">Unterstützt die AMD-Virtualisierungserweiterungen.</span><span class="sxs-lookup"><span data-stu-id="52fb4-118">Supports the AMD Virtualization extensions.</span></span><br/>              |
| <dl> <span data-ttu-id="52fb4-119"><dt>"Intel VT"</dt></span><span class="sxs-lookup"><span data-stu-id="52fb4-119"><dt>"Intel VT"</dt></span></span> </dl> | <span data-ttu-id="52fb4-120">Unterstützt die Intel Virtualization Technology Extensions.</span><span class="sxs-lookup"><span data-stu-id="52fb4-120">Supports the Intel Virtualization Technology extensions.</span></span><br/> |
| <dl> <span data-ttu-id="52fb4-121"><dt>"Havd"</dt></span><span class="sxs-lookup"><span data-stu-id="52fb4-121"><dt>"HAVD"</dt></span></span> </dl>     | <span data-ttu-id="52fb4-122">Die Hardware gestützte Virtualisierung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="52fb4-122">Hardware Assisted Virtualization is disabled.</span></span><br/>            |
| <dl> <span data-ttu-id="52fb4-123"><dt>Hätten</dt></span><span class="sxs-lookup"><span data-stu-id="52fb4-123"><dt>"HAVE"</dt></span></span> </dl>     | <span data-ttu-id="52fb4-124">Die Hardware gestützte Virtualisierung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="52fb4-124">Hardware Assisted Virtualization is enabled.</span></span><br/>             |
| <dl> <span data-ttu-id="52fb4-125"><dt>MMX</dt></span><span class="sxs-lookup"><span data-stu-id="52fb4-125"><dt>"MMX"</dt></span></span> </dl>      | <span data-ttu-id="52fb4-126">Unterstützt die MMX-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="52fb4-126">Supports the MMX extensions.</span></span><br/>                             |
| <dl> <span data-ttu-id="52fb4-127"><dt>Preußen</dt></span><span class="sxs-lookup"><span data-stu-id="52fb4-127"><dt>"SSE"</dt></span></span> </dl>      | <span data-ttu-id="52fb4-128">Unterstützt die Streaming SIMD Extensions.</span><span class="sxs-lookup"><span data-stu-id="52fb4-128">Supports the Streaming SIMD Extensions.</span></span><br/>                  |
| <dl> <span data-ttu-id="52fb4-129"><dt>SSE2</dt></span><span class="sxs-lookup"><span data-stu-id="52fb4-129"><dt>"SSE2"</dt></span></span> </dl>     | <span data-ttu-id="52fb4-130">Unterstützt die Streaming SIMD Extensions 2.</span><span class="sxs-lookup"><span data-stu-id="52fb4-130">Supports the Streaming SIMD Extensions 2.</span></span><br/>                |
| <dl> <span data-ttu-id="52fb4-131"><dt>SSE3</dt></span><span class="sxs-lookup"><span data-stu-id="52fb4-131"><dt>"SSE3"</dt></span></span> </dl>     | <span data-ttu-id="52fb4-132">Unterstützt die Streaming SIMD Extensions 3.</span><span class="sxs-lookup"><span data-stu-id="52fb4-132">Supports the Streaming SIMD Extensions 3.</span></span><br/>                |
| <dl> <span data-ttu-id="52fb4-133"><dt>"Txte"</dt></span><span class="sxs-lookup"><span data-stu-id="52fb4-133"><dt>"TXTE"</dt></span></span> </dl>     | <span data-ttu-id="52fb4-134">Unterstützt die Erweiterungen der vertrauenswürdigen Ausführungs Technologie.</span><span class="sxs-lookup"><span data-stu-id="52fb4-134">Supports the Trusted Execution Technology extensions.</span></span><br/>    |
| <dl> <span data-ttu-id="52fb4-135"><dt>"x86-64"</dt></span><span class="sxs-lookup"><span data-stu-id="52fb4-135"><dt>"x86-64"</dt></span></span> </dl>   | <span data-ttu-id="52fb4-136">Unterstützt x86-64-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="52fb4-136">Supports x86-64 extensions.</span></span><br/>                              |



 

## <a name="error-codes"></a><span data-ttu-id="52fb4-137">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="52fb4-137">Error codes</span></span>



| <span data-ttu-id="52fb4-138">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="52fb4-138">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="52fb4-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="52fb4-139">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="52fb4-140"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="52fb4-140"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="52fb4-141">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="52fb4-141">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="52fb4-142"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="52fb4-142"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="52fb4-143">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="52fb4-143">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="52fb4-144"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="52fb4-144"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="52fb4-145">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="52fb4-145">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="52fb4-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52fb4-146">Requirements</span></span>



| <span data-ttu-id="52fb4-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52fb4-147">Requirement</span></span> | <span data-ttu-id="52fb4-148">Wert</span><span class="sxs-lookup"><span data-stu-id="52fb4-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="52fb4-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52fb4-149">Minimum supported client</span></span><br/> | <span data-ttu-id="52fb4-150">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52fb4-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52fb4-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52fb4-151">Minimum supported server</span></span><br/> | <span data-ttu-id="52fb4-152">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="52fb4-152">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="52fb4-153">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="52fb4-153">End of client support</span></span><br/>    | <span data-ttu-id="52fb4-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52fb4-154">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="52fb4-155">Produkt</span><span class="sxs-lookup"><span data-stu-id="52fb4-155">Product</span></span><br/>                  | <span data-ttu-id="52fb4-156">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="52fb4-156">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="52fb4-157">Header</span><span class="sxs-lookup"><span data-stu-id="52fb4-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="52fb4-158"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="52fb4-158"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="52fb4-159">IID</span><span class="sxs-lookup"><span data-stu-id="52fb4-159">IID</span></span><br/>                      | <span data-ttu-id="52fb4-160">IID \_ ivmhostinfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.</span><span class="sxs-lookup"><span data-stu-id="52fb4-160">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="52fb4-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52fb4-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52fb4-162">**Ivmhostinfo**</span><span class="sxs-lookup"><span data-stu-id="52fb4-162">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

