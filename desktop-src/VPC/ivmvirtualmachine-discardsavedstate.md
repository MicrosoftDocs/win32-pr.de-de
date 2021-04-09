---
title: Methode ' ivmvirtualmachine verwerdsavedstate ' (vpccominterfaces. h)
description: Verwirft alle gespeicherten Zustandsinformationen für eine gespeicherte virtuelle Maschine.
ms.assetid: 546d6ea9-bfa3-487d-a333-399986bdf9a1
keywords:
- Verwerdsavedstate-Methode, Virtual PC
- Verwerdsavedstate-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, verwerdsavedstate-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardSavedState
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce5c9cc0b07af2cc8c995d0c368d7747fa1475a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040737"
---
# <a name="ivmvirtualmachinediscardsavedstate-method"></a><span data-ttu-id="749be-106">Ivmvirtualmachine::D iscardsavedstate-Methode</span><span class="sxs-lookup"><span data-stu-id="749be-106">IVMVirtualMachine::DiscardSavedState method</span></span>

<span data-ttu-id="749be-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="749be-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="749be-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="749be-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="749be-109">Verwirft alle gespeicherten Zustandsinformationen für eine gespeicherte virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="749be-109">Discards any saved state information for a saved virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="749be-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="749be-110">Syntax</span></span>


```C++
HRESULT DiscardSavedState();
```



## <a name="parameters"></a><span data-ttu-id="749be-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="749be-111">Parameters</span></span>

<span data-ttu-id="749be-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="749be-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="749be-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="749be-113">Return value</span></span>

<span data-ttu-id="749be-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="749be-114">This method can return one of these values.</span></span>



| <span data-ttu-id="749be-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="749be-115">Return code/value</span></span>                                                                                                                                                           | <span data-ttu-id="749be-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="749be-116">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="749be-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="749be-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="749be-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="749be-118">The operation was successful.</span></span><br/>                               |
| <dl> <span data-ttu-id="749be-119"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="749be-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="749be-120">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="749be-120">The configuration is unknown.</span></span><br/>                               |
| <dl> <span data-ttu-id="749be-121"><dt>**VM \_ E \_ VM \_**</dt> mit <dt>0xa0040500</dt></span><span class="sxs-lookup"><span data-stu-id="749be-121"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>           | <span data-ttu-id="749be-122">Der virtuelle Computer wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="749be-122">The virtual machine is running.</span></span><br/>                             |
| <dl> <span data-ttu-id="749be-123"><dt>**VM \_ E \_ VM \_ nicht \_ gespeicherten \_ Status**</dt> <dt>0xa00400501</dt></span><span class="sxs-lookup"><span data-stu-id="749be-123"><dt>**VM\_E\_VM\_NO\_SAVED\_STATE**</dt> <dt>0xA00400501</dt></span></span> </dl> | <span data-ttu-id="749be-124">Der virtuelle Computer wird nicht ausgeführt, hat aber keinen gespeicherten Zustand.</span><span class="sxs-lookup"><span data-stu-id="749be-124">The virtual machine is not running, but has no saved state.</span></span><br/> |
| <dl> <span data-ttu-id="749be-125"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="749be-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="749be-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="749be-126">An unexpected error has occurred.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="749be-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="749be-127">Requirements</span></span>



| <span data-ttu-id="749be-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="749be-128">Requirement</span></span> | <span data-ttu-id="749be-129">Wert</span><span class="sxs-lookup"><span data-stu-id="749be-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="749be-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="749be-130">Minimum supported client</span></span><br/> | <span data-ttu-id="749be-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="749be-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="749be-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="749be-132">Minimum supported server</span></span><br/> | <span data-ttu-id="749be-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="749be-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="749be-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="749be-134">End of client support</span></span><br/>    | <span data-ttu-id="749be-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="749be-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="749be-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="749be-136">Product</span></span><br/>                  | <span data-ttu-id="749be-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="749be-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="749be-138">Header</span><span class="sxs-lookup"><span data-stu-id="749be-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="749be-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="749be-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="749be-140">IID</span><span class="sxs-lookup"><span data-stu-id="749be-140">IID</span></span><br/>                      | <span data-ttu-id="749be-141">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="749be-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="749be-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="749be-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="749be-143">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="749be-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

