---
title: Ivmaccountant cpunutzungseigenschaft (vpccominterfaces. h)
description: Ruft den Prozentsatz der aktuellen CPU-Auslastung für diesen virtuellen Computer ab.
ms.assetid: 69bb61ec-af41-4bd0-95bd-4698a1d33098
keywords:
- Cpunutzungseigenschaft virtueller PC
- Cpunutzungseigenschaft Virtual PC, ivmaccountant-Schnittstelle
- Ivmaccountant Interface Virtual PC, cpunutzungseigenschaft
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilization
- IVMAccountant.get_CPUUtilization
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e38c223f47678cdb9c2d49e06452d014083c94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957127"
---
# <a name="ivmaccountantcpuutilization-property"></a><span data-ttu-id="8787c-106">Ivmaccountant:: cpunutzungseigenschaft</span><span class="sxs-lookup"><span data-stu-id="8787c-106">IVMAccountant::CPUUtilization property</span></span>

<span data-ttu-id="8787c-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8787c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8787c-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8787c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8787c-109">Ruft den Prozentsatz der aktuellen CPU-Auslastung für diesen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="8787c-109">Retrieves the percentage of current CPU utilization for this virtual machine.</span></span>

<span data-ttu-id="8787c-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8787c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8787c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8787c-111">Syntax</span></span>


```C++
HRESULT get_CPUUtilization(
  [out, retval] long *percentageUtilization
);
```



## <a name="property-value"></a><span data-ttu-id="8787c-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8787c-112">Property value</span></span>

<span data-ttu-id="8787c-113">Der Prozentsatz der aktuellen CPU-Auslastung.</span><span class="sxs-lookup"><span data-stu-id="8787c-113">The percentage of current CPU utilization.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8787c-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="8787c-114">Error codes</span></span>



| <span data-ttu-id="8787c-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="8787c-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="8787c-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8787c-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="8787c-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8787c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="8787c-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="8787c-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="8787c-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8787c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="8787c-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="8787c-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="8787c-121"><dt>S \_ Falsch</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8787c-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="8787c-122">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8787c-122">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="8787c-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8787c-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="8787c-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8787c-124">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="8787c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8787c-125">Requirements</span></span>



| <span data-ttu-id="8787c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8787c-126">Requirement</span></span> | <span data-ttu-id="8787c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="8787c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8787c-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8787c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8787c-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8787c-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8787c-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8787c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8787c-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8787c-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8787c-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="8787c-132">End of client support</span></span><br/>    | <span data-ttu-id="8787c-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8787c-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8787c-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="8787c-134">Product</span></span><br/>                  | <span data-ttu-id="8787c-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8787c-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8787c-136">Header</span><span class="sxs-lookup"><span data-stu-id="8787c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8787c-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8787c-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8787c-138">IID</span><span class="sxs-lookup"><span data-stu-id="8787c-138">IID</span></span><br/>                      | <span data-ttu-id="8787c-139">IID \_ ivmaccountant ist als 6376c067-7b57-4d63-B754-06e2e4f 51d73 definiert.</span><span class="sxs-lookup"><span data-stu-id="8787c-139">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="8787c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8787c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8787c-141">**Ivmaccountant**</span><span class="sxs-lookup"><span data-stu-id="8787c-141">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

