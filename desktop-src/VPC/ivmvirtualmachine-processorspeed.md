---
title: Ivmvirtualmachine processorspeed-Eigenschaft (vpccominterfaces. h)
description: Geschwindigkeit des Prozessors in Megahertz (MHz) oder Gigahertz (GHz).
ms.assetid: 465157a9-08ad-4636-b7c6-a188ff21e131
keywords:
- Processorspeed-Eigenschaft virtueller PC
- Processorspeed-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, processorspeed (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ProcessorSpeed
- IVMVirtualMachine.get_ProcessorSpeed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaeb6f17e867d7618241b099b765ff450a2a4e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478675"
---
# <a name="ivmvirtualmachineprocessorspeed-property"></a><span data-ttu-id="a2774-106">Ivmvirtualmachine::P rocess orspeed-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a2774-106">IVMVirtualMachine::ProcessorSpeed property</span></span>

<span data-ttu-id="a2774-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a2774-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a2774-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a2774-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a2774-109">Ruft die Geschwindigkeit des Prozessors in Megahertz (MHz) oder Gigahertz (GHz) ab.</span><span class="sxs-lookup"><span data-stu-id="a2774-109">Retrieves the speed of the processor, in megahertz (MHz) or gigahertz (GHz).</span></span>

<span data-ttu-id="a2774-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a2774-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2774-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2774-111">Syntax</span></span>


```C++
HRESULT get_ProcessorSpeed(
  [out, retval] long *processorSpeed
);
```



## <a name="property-value"></a><span data-ttu-id="a2774-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a2774-112">Property value</span></span>

<span data-ttu-id="a2774-113">Die Geschwindigkeit in Megahertz oder Gigahertz.</span><span class="sxs-lookup"><span data-stu-id="a2774-113">The speed, in megahertz or gigahertz.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a2774-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a2774-114">Error codes</span></span>



| <span data-ttu-id="a2774-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="a2774-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a2774-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a2774-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a2774-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a2774-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a2774-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2774-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a2774-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a2774-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a2774-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="a2774-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="a2774-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="a2774-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="a2774-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="a2774-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="a2774-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a2774-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a2774-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a2774-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a2774-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2774-125">Requirements</span></span>



| <span data-ttu-id="a2774-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2774-126">Requirement</span></span> | <span data-ttu-id="a2774-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a2774-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2774-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2774-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a2774-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2774-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2774-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2774-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a2774-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a2774-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a2774-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a2774-132">End of client support</span></span><br/>    | <span data-ttu-id="a2774-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a2774-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a2774-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="a2774-134">Product</span></span><br/>                  | <span data-ttu-id="a2774-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a2774-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a2774-136">Header</span><span class="sxs-lookup"><span data-stu-id="a2774-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2774-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2774-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a2774-138">IID</span><span class="sxs-lookup"><span data-stu-id="a2774-138">IID</span></span><br/>                      | <span data-ttu-id="a2774-139">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="a2774-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a2774-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2774-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2774-141">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="a2774-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

