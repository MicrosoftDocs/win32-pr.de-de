---
title: Ivmvirtualpc maximumserialportspervm-Eigenschaft (vpccominterfaces. h)
description: Hiermit wird die maximale Anzahl von seriellen Anschlüssen pro virtuellem Computer abgerufen.
ms.assetid: e7b874df-105e-4ca8-90ec-2368071dafa0
keywords:
- Maximumserialportspervm-Eigenschaft virtueller PC
- Maximumserialportspervm-Eigenschaft Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, maximumserialportspervm (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumSerialPortsPerVM
- IVMVirtualPC.get_MaximumSerialPortsPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63aa00c56add6bc48f4c33626a84a854b025c81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102790"
---
# <a name="ivmvirtualpcmaximumserialportspervm-property"></a><span data-ttu-id="3b268-106">Ivmvirtualpc:: maximumserialportspervm (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3b268-106">IVMVirtualPC::MaximumSerialPortsPerVM property</span></span>

<span data-ttu-id="3b268-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3b268-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3b268-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3b268-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3b268-109">Hiermit wird die maximale Anzahl von seriellen Anschlüssen pro virtuellem Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3b268-109">Retrieves the maximum number of serial ports per virtual machine.</span></span>

<span data-ttu-id="3b268-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3b268-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b268-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b268-111">Syntax</span></span>


```C++
HRESULT get_MaximumSerialPortsPerVM(
  [out, retval] long *maxPorts
);
```



## <a name="property-value"></a><span data-ttu-id="3b268-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3b268-112">Property value</span></span>

<span data-ttu-id="3b268-113">Die maximale Anzahl von seriellen Anschlüssen pro virtuellem Computer.</span><span class="sxs-lookup"><span data-stu-id="3b268-113">The maximum number of serial ports per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3b268-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3b268-114">Error codes</span></span>



| <span data-ttu-id="3b268-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="3b268-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="3b268-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3b268-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3b268-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3b268-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="3b268-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b268-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3b268-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3b268-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="3b268-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="3b268-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="3b268-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3b268-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="3b268-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3b268-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="3b268-123"><dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="3b268-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="3b268-124">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="3b268-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3b268-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b268-125">Requirements</span></span>



| <span data-ttu-id="3b268-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b268-126">Requirement</span></span> | <span data-ttu-id="3b268-127">Wert</span><span class="sxs-lookup"><span data-stu-id="3b268-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b268-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3b268-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3b268-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b268-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3b268-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3b268-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3b268-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3b268-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3b268-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3b268-132">End of client support</span></span><br/>    | <span data-ttu-id="3b268-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3b268-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3b268-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="3b268-134">Product</span></span><br/>                  | <span data-ttu-id="3b268-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3b268-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3b268-136">Header</span><span class="sxs-lookup"><span data-stu-id="3b268-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b268-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b268-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3b268-138">IID</span><span class="sxs-lookup"><span data-stu-id="3b268-138">IID</span></span><br/>                      | <span data-ttu-id="3b268-139">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="3b268-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3b268-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b268-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b268-141">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="3b268-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

