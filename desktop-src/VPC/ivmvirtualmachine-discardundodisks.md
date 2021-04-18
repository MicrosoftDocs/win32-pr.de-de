---
title: Methode ' ivmvirtualmachine Verwerfen von dodisks ' (vpccominterfaces. h)
description: Verwirft die virtuellen Rückgängig-Datenträger.
ms.assetid: 5c3a4b3f-ea58-498c-b7cf-54f028fa061c
keywords:
- Verwerfen der Methode "Verwerfen von dodisks"
- Verwerfen von dodisks-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Methode Verwerfen von dodisks
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d548b69a6cfebc383a0233f01ef19ad14d051474
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477043"
---
# <a name="ivmvirtualmachinediscardundodisks-method"></a><span data-ttu-id="3002e-106">Ivmvirtualmachine::D iscardundodisks-Methode</span><span class="sxs-lookup"><span data-stu-id="3002e-106">IVMVirtualMachine::DiscardUndoDisks method</span></span>

<span data-ttu-id="3002e-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3002e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3002e-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3002e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3002e-109">Verwirft die virtuellen Rückgängig-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="3002e-109">Discards the virtual undo disks.</span></span>

## <a name="syntax"></a><span data-ttu-id="3002e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3002e-110">Syntax</span></span>


```C++
HRESULT DiscardUndoDisks();
```



## <a name="parameters"></a><span data-ttu-id="3002e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3002e-111">Parameters</span></span>

<span data-ttu-id="3002e-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3002e-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3002e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3002e-113">Return value</span></span>

<span data-ttu-id="3002e-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3002e-114">This method can return one of these values.</span></span>



| <span data-ttu-id="3002e-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="3002e-115">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="3002e-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3002e-116">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3002e-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3002e-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="3002e-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="3002e-118">The operation was successful.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="3002e-119"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="3002e-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="3002e-120">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="3002e-120">The configuration is unknown.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="3002e-121"><dt>**VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_**</dt> <dt>0xa004020b</dt> gespeichert</span><span class="sxs-lookup"><span data-stu-id="3002e-121"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="3002e-122">Die virtuellen Rückgängig-Datenträger können nicht verworfen werden, während der virtuelle Computer ausgeführt wird oder sich in einem gespeicherten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="3002e-122">The virtual undo disks cannot be discarded while the virtual machine is running or in a saved state.</span></span><br/> |
| <dl> <span data-ttu-id="3002e-123"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3002e-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="3002e-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3002e-124">An unexpected error has occurred.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="3002e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3002e-125">Requirements</span></span>



| <span data-ttu-id="3002e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3002e-126">Requirement</span></span> | <span data-ttu-id="3002e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="3002e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3002e-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3002e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3002e-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3002e-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3002e-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3002e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3002e-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3002e-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3002e-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3002e-132">End of client support</span></span><br/>    | <span data-ttu-id="3002e-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3002e-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3002e-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="3002e-134">Product</span></span><br/>                  | <span data-ttu-id="3002e-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3002e-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3002e-136">Header</span><span class="sxs-lookup"><span data-stu-id="3002e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3002e-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3002e-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3002e-138">IID</span><span class="sxs-lookup"><span data-stu-id="3002e-138">IID</span></span><br/>                      | <span data-ttu-id="3002e-139">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="3002e-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="3002e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3002e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3002e-141">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="3002e-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

