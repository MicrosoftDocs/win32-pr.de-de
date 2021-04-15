---
title: Ivmaccountant cpuutilizationhistory-Eigenschaft (vpccominterfaces. h)
description: Ruft die aktuelle CPU-Auslastung dieses virtuellen Computers (als Array von Prozentwerten) ab.
ms.assetid: f6b92b25-9455-4061-8db0-3e42f9f7391d
keywords:
- Cpuutilizationhistory-Eigenschaft virtueller PC
- Cpuutilizationhistory-Eigenschaft Virtual PC, ivmaccountant-Schnittstelle
- Ivmaccountant Interface Virtual PC, cpuutilizationhistory (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilizationHistory
- IVMAccountant.get_CPUUtilizationHistory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa7e91a83be7ab4c09a0b779a729745e80e1e74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479020"
---
# <a name="ivmaccountantcpuutilizationhistory-property"></a><span data-ttu-id="d9904-106">Ivmaccountant:: cpuutilizationhistory-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d9904-106">IVMAccountant::CPUUtilizationHistory property</span></span>

<span data-ttu-id="d9904-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9904-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d9904-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d9904-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d9904-109">Ruft die aktuelle CPU-Auslastung dieses virtuellen Computers (als Array von Prozentwerten) ab.</span><span class="sxs-lookup"><span data-stu-id="d9904-109">Retrieves the recent CPU utilization of this virtual machine (as an array of percentage values).</span></span>

<span data-ttu-id="d9904-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d9904-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9904-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9904-111">Syntax</span></span>


```C++
HRESULT get_CPUUtilizationHistory(
  [out, retval] VARIANT *percentageUtilization
);
```



## <a name="property-value"></a><span data-ttu-id="d9904-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d9904-112">Property value</span></span>

<span data-ttu-id="d9904-113">Die aktuelle CPU-Nutzung dieses virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="d9904-113">The recent CPU use of this virtual machine.</span></span> <span data-ttu-id="d9904-114">Diese Daten werden als Array von 60 Elementen zurückgegeben, die den Prozentsatz der CPU-Nutzung in der letzten Minute in der letzten Minute darstellen.</span><span class="sxs-lookup"><span data-stu-id="d9904-114">This data is returned as an array of 60 elements that represent the percentage of CPU use at each second over the past minute.</span></span> <span data-ttu-id="d9904-115">Variant-Typ ist VT \_ array \| VT \_ UI1.</span><span class="sxs-lookup"><span data-stu-id="d9904-115">Variant type is VT\_ARRAY\|VT\_UI1.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d9904-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d9904-116">Error codes</span></span>



| <span data-ttu-id="d9904-117">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="d9904-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d9904-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d9904-118">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d9904-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d9904-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d9904-120">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9904-120">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="d9904-121"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d9904-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d9904-122">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="d9904-122">The parameter is **NULL**.</span></span><br/>                                              |
| <dl> <span data-ttu-id="d9904-123"><dt>S \_ Falsch</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d9904-123"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="d9904-124">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9904-124">The virtual machine is not running.</span></span> <span data-ttu-id="d9904-125">Alle 60 Array-Elemente werden auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d9904-125">All 60 array elements are set to 0.</span></span><br/> |
| <dl> <span data-ttu-id="d9904-126"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d9904-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d9904-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d9904-127">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="d9904-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9904-128">Requirements</span></span>



| <span data-ttu-id="d9904-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9904-129">Requirement</span></span> | <span data-ttu-id="d9904-130">Wert</span><span class="sxs-lookup"><span data-stu-id="d9904-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9904-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9904-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d9904-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9904-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d9904-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9904-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d9904-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d9904-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d9904-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d9904-135">End of client support</span></span><br/>    | <span data-ttu-id="d9904-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d9904-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d9904-137">Produkt</span><span class="sxs-lookup"><span data-stu-id="d9904-137">Product</span></span><br/>                  | <span data-ttu-id="d9904-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d9904-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d9904-139">Header</span><span class="sxs-lookup"><span data-stu-id="d9904-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9904-140"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9904-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d9904-141">IID</span><span class="sxs-lookup"><span data-stu-id="d9904-141">IID</span></span><br/>                      | <span data-ttu-id="d9904-142">IID \_ ivmaccountant ist als 6376c067-7b57-4d63-B754-06e2e4f 51d73 definiert.</span><span class="sxs-lookup"><span data-stu-id="d9904-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="d9904-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9904-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9904-144">**Ivmaccountant**</span><span class="sxs-lookup"><span data-stu-id="d9904-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

