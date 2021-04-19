---
title: Ivmvirtualpc maximumparallelportspervm-Eigenschaft (vpccominterfaces. h)
description: Hiermit wird die maximale Anzahl paralleler Ports pro virtuellem Computer abgerufen.
ms.assetid: c5baac59-386c-4373-a560-460750178894
keywords:
- Maximumparallelportspervm-Eigenschaft virtueller PC
- Maximumparallelportspervm-Eigenschaft Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, maximumparallelportspervm (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumParallelPortsPerVM
- IVMVirtualPC.get_MaximumParallelPortsPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57c5bed446a421190eb47630bde0d05f0cbcee7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342441"
---
# <a name="ivmvirtualpcmaximumparallelportspervm-property"></a><span data-ttu-id="7ac90-106">Ivmvirtualpc:: maximumparallelportspervm (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7ac90-106">IVMVirtualPC::MaximumParallelPortsPerVM property</span></span>

<span data-ttu-id="7ac90-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7ac90-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7ac90-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7ac90-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7ac90-109">Hiermit wird die maximale Anzahl paralleler Ports pro virtuellem Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7ac90-109">Retrieves the maximum number of parallel ports per virtual machine.</span></span>

<span data-ttu-id="7ac90-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7ac90-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ac90-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ac90-111">Syntax</span></span>


```C++
HRESULT get_MaximumParallelPortsPerVM(
  [out, retval] long *maxPorts
);
```



## <a name="property-value"></a><span data-ttu-id="7ac90-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7ac90-112">Property value</span></span>

<span data-ttu-id="7ac90-113">Die maximale Anzahl paralleler Ports pro virtuellem Computer.</span><span class="sxs-lookup"><span data-stu-id="7ac90-113">The maximum number of parallel ports per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7ac90-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7ac90-114">Error codes</span></span>



| <span data-ttu-id="7ac90-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="7ac90-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="7ac90-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7ac90-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7ac90-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7ac90-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="7ac90-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ac90-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="7ac90-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7ac90-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="7ac90-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="7ac90-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="7ac90-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7ac90-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="7ac90-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7ac90-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="7ac90-123"><dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="7ac90-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="7ac90-124">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="7ac90-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7ac90-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ac90-125">Requirements</span></span>



| <span data-ttu-id="7ac90-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ac90-126">Requirement</span></span> | <span data-ttu-id="7ac90-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7ac90-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac90-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ac90-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7ac90-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ac90-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ac90-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ac90-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7ac90-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7ac90-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7ac90-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7ac90-132">End of client support</span></span><br/>    | <span data-ttu-id="7ac90-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7ac90-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7ac90-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="7ac90-134">Product</span></span><br/>                  | <span data-ttu-id="7ac90-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7ac90-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7ac90-136">Header</span><span class="sxs-lookup"><span data-stu-id="7ac90-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ac90-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ac90-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7ac90-138">IID</span><span class="sxs-lookup"><span data-stu-id="7ac90-138">IID</span></span><br/>                      | <span data-ttu-id="7ac90-139">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="7ac90-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7ac90-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ac90-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ac90-141">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="7ac90-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

