---
title: Ivmhostinfo processorspeed-Eigenschaft (vpccominterfaces. h)
description: Geschwindigkeit des Host Prozessors in Megahertz (MHz) oder Gigahertz (GHz).
ms.assetid: 2d5e3f2e-8e81-4527-bd7f-52bf5b1f56ef
keywords:
- Processorspeed-Eigenschaft virtueller PC
- Processorspeed-Eigenschaft Virtual PC, ivmhostinfo-Schnittstelle
- Ivmhostinfo Interface Virtual PC, processorspeed (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorSpeed
- IVMHostInfo.get_ProcessorSpeed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28fc890392db5f61a7819fa1d4b4a11d2b3de312
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040053"
---
# <a name="ivmhostinfoprocessorspeed-property"></a><span data-ttu-id="e26df-106">Ivmhostinfo::P rocess orspeed-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e26df-106">IVMHostInfo::ProcessorSpeed property</span></span>

<span data-ttu-id="e26df-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e26df-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e26df-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e26df-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e26df-109">Ruft die Geschwindigkeit des Host Prozessors in Megahertz (MHz) oder Gigahertz (GHz) ab.</span><span class="sxs-lookup"><span data-stu-id="e26df-109">Retrieves the speed of the host processor, in megahertz (MHz) or gigahertz (GHz).</span></span>

<span data-ttu-id="e26df-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e26df-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e26df-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e26df-111">Syntax</span></span>


```C++
HRESULT get_ProcessorSpeed(
  [out, retval] long *processorSpeed
);
```



## <a name="property-value"></a><span data-ttu-id="e26df-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e26df-112">Property value</span></span>

<span data-ttu-id="e26df-113">Die Prozessorgeschwindigkeit in Megahertz oder Gigahertz.</span><span class="sxs-lookup"><span data-stu-id="e26df-113">The processor speed, in megahertz or gigahertz.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e26df-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e26df-114">Error codes</span></span>



| <span data-ttu-id="e26df-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="e26df-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="e26df-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e26df-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e26df-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e26df-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e26df-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e26df-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="e26df-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e26df-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="e26df-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="e26df-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="e26df-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e26df-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e26df-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e26df-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e26df-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e26df-123">Requirements</span></span>



| <span data-ttu-id="e26df-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e26df-124">Requirement</span></span> | <span data-ttu-id="e26df-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e26df-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e26df-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e26df-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e26df-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e26df-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e26df-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e26df-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e26df-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e26df-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e26df-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e26df-130">End of client support</span></span><br/>    | <span data-ttu-id="e26df-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e26df-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e26df-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="e26df-132">Product</span></span><br/>                  | <span data-ttu-id="e26df-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e26df-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e26df-134">Header</span><span class="sxs-lookup"><span data-stu-id="e26df-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e26df-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e26df-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e26df-136">IID</span><span class="sxs-lookup"><span data-stu-id="e26df-136">IID</span></span><br/>                      | <span data-ttu-id="e26df-137">IID \_ ivmhostinfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.</span><span class="sxs-lookup"><span data-stu-id="e26df-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="e26df-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e26df-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e26df-139">**Ivmhostinfo**</span><span class="sxs-lookup"><span data-stu-id="e26df-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

