---
title: Ivmvirtualpc maximumnumof-Bus-Eigenschaft (vpccominterfaces. h)
description: Ruft die maximal zulässige Anzahl von Bussen für IDE ab.
ms.assetid: 7b88eda4-0f66-4e26-96cb-1e9ebef9d0b8
keywords:
- Maximumnumostbus-Eigenschaft virtueller PC
- Maximumnumostbus-Eigenschaft virtueller PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, maximummaximiofdecobus (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumNumberOfIDEBuses
- IVMVirtualPC.get_MaximumNumberOfIDEBuses
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceabc071c0bf294eed3423d36c2c019586754101
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040040"
---
# <a name="ivmvirtualpcmaximumnumberofidebuses-property"></a><span data-ttu-id="79e2f-106">Ivmvirtualpc:: maximumnumomebus-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="79e2f-106">IVMVirtualPC::MaximumNumberOfIDEBuses property</span></span>

<span data-ttu-id="79e2f-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="79e2f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="79e2f-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="79e2f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="79e2f-109">Ruft die maximal zulässige Anzahl von Bussen für IDE ab.</span><span class="sxs-lookup"><span data-stu-id="79e2f-109">Retrieves the maximum number of buses allowed for IDE.</span></span>

<span data-ttu-id="79e2f-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="79e2f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e2f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="79e2f-111">Syntax</span></span>


```C++
HRESULT get_MaximumNumberOfIDEBuses(
  [out, retval] long *maxNumBuses
);
```



## <a name="property-value"></a><span data-ttu-id="79e2f-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="79e2f-112">Property value</span></span>

<span data-ttu-id="79e2f-113">Die maximal zulässige Anzahl von Bussen für IDE.</span><span class="sxs-lookup"><span data-stu-id="79e2f-113">The maximum number of buses allowed for IDE.</span></span>

## <a name="error-codes"></a><span data-ttu-id="79e2f-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="79e2f-114">Error codes</span></span>



| <span data-ttu-id="79e2f-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="79e2f-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="79e2f-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="79e2f-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="79e2f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="79e2f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="79e2f-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="79e2f-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="79e2f-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="79e2f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="79e2f-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="79e2f-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="79e2f-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="79e2f-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="79e2f-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="79e2f-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="79e2f-123"><dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="79e2f-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="79e2f-124">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="79e2f-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="79e2f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79e2f-125">Requirements</span></span>



| <span data-ttu-id="79e2f-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79e2f-126">Requirement</span></span> | <span data-ttu-id="79e2f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="79e2f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="79e2f-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79e2f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="79e2f-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79e2f-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79e2f-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79e2f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="79e2f-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="79e2f-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="79e2f-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="79e2f-132">End of client support</span></span><br/>    | <span data-ttu-id="79e2f-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="79e2f-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="79e2f-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="79e2f-134">Product</span></span><br/>                  | <span data-ttu-id="79e2f-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="79e2f-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="79e2f-136">Header</span><span class="sxs-lookup"><span data-stu-id="79e2f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="79e2f-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="79e2f-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="79e2f-138">IID</span><span class="sxs-lookup"><span data-stu-id="79e2f-138">IID</span></span><br/>                      | <span data-ttu-id="79e2f-139">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="79e2f-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="79e2f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79e2f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e2f-141">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="79e2f-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

