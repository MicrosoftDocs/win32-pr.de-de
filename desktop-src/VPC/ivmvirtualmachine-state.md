---
title: Ivmvirtualmachine State-Eigenschaft (vpccominterfaces. h)
description: Ruft den aktuellen Zustand des virtuellen Computers ab.
ms.assetid: a4214dfc-09d2-4d6b-a053-e75e99063411
keywords:
- Zustands Eigenschaft virtueller PC
- State-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, State-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.State
- IVMVirtualMachine.get_State
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11616f2a88b9238da11a4edec00c048e69885a07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956954"
---
# <a name="ivmvirtualmachinestate-property"></a><span data-ttu-id="417cf-106">Ivmvirtualmachine:: State (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="417cf-106">IVMVirtualMachine::State property</span></span>

<span data-ttu-id="417cf-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="417cf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="417cf-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="417cf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="417cf-109">Ruft den aktuellen Zustand des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="417cf-109">Retrieves the current state of the virtual machine.</span></span>

<span data-ttu-id="417cf-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="417cf-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="417cf-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="417cf-111">Syntax</span></span>


```C++
HRESULT get_State(
  [out, retval] VMVMState *virtualMachineState
);
```



## <a name="property-value"></a><span data-ttu-id="417cf-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="417cf-112">Property value</span></span>

<span data-ttu-id="417cf-113">Der aktuelle Zustand der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="417cf-113">The current state of the virtual machine.</span></span> <span data-ttu-id="417cf-114">Eine Liste der Werte finden Sie unter [**vmvmstate**](vmvmstate.md).</span><span class="sxs-lookup"><span data-stu-id="417cf-114">For a list of values, see [**VMVMState**](vmvmstate.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="417cf-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="417cf-115">Error codes</span></span>



| <span data-ttu-id="417cf-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="417cf-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="417cf-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="417cf-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="417cf-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="417cf-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="417cf-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="417cf-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="417cf-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="417cf-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="417cf-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="417cf-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="417cf-122"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="417cf-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="417cf-123">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="417cf-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="417cf-124"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="417cf-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="417cf-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="417cf-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="417cf-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="417cf-126">Requirements</span></span>



| <span data-ttu-id="417cf-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="417cf-127">Requirement</span></span> | <span data-ttu-id="417cf-128">Wert</span><span class="sxs-lookup"><span data-stu-id="417cf-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="417cf-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="417cf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="417cf-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="417cf-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="417cf-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="417cf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="417cf-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="417cf-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="417cf-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="417cf-133">End of client support</span></span><br/>    | <span data-ttu-id="417cf-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="417cf-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="417cf-135">Produkt</span><span class="sxs-lookup"><span data-stu-id="417cf-135">Product</span></span><br/>                  | <span data-ttu-id="417cf-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="417cf-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="417cf-137">Header</span><span class="sxs-lookup"><span data-stu-id="417cf-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="417cf-138"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="417cf-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="417cf-139">IID</span><span class="sxs-lookup"><span data-stu-id="417cf-139">IID</span></span><br/>                      | <span data-ttu-id="417cf-140">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="417cf-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="417cf-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="417cf-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="417cf-142">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="417cf-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

