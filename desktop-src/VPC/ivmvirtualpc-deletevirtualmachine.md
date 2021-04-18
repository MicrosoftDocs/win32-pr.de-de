---
title: Ivmvirtualpc deletevirtualmachine-Methode (vpccominterfaces. h)
description: Löscht die Konfiguration einer virtuellen Maschine.
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- Deletevirtualmachine-Methode Virtual PC
- Deletevirtualmachine-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, deletevirtualmachine-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.DeleteVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee9c1591ccd736099fab04cce31c8a8b77b5fb06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343460"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a><span data-ttu-id="9996a-106">Ivmvirtualpc::D eletevirtualmachine-Methode</span><span class="sxs-lookup"><span data-stu-id="9996a-106">IVMVirtualPC::DeleteVirtualMachine method</span></span>

<span data-ttu-id="9996a-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9996a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9996a-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9996a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9996a-109">Löscht die Konfiguration einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="9996a-109">Deletes a virtual machine configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="9996a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9996a-110">Syntax</span></span>


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="9996a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9996a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9996a-112">*virtualmachine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9996a-112">*virtualMachine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9996a-113">Ein Zeiger auf ein [**ivmvirtualmachine**](ivmvirtualmachine.md) -Objekt, das die zu löschende Konfiguration der virtuellen Maschine darstellt.</span><span class="sxs-lookup"><span data-stu-id="9996a-113">A pointer to an [**IVMVirtualMachine**](ivmvirtualmachine.md) object representing the virtual machine configuration to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9996a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9996a-114">Return value</span></span>

<span data-ttu-id="9996a-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9996a-115">This method can return one of these values.</span></span>



| <span data-ttu-id="9996a-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="9996a-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="9996a-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9996a-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9996a-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9996a-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="9996a-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9996a-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="9996a-120"><dt>**S \_ Falsch**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9996a-120"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                           | <span data-ttu-id="9996a-121">Die angegebene Konfiguration wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="9996a-121">The specified configuration could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="9996a-122"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9996a-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="9996a-123">Der Parameter " *virtualmachine* " war **null**.</span><span class="sxs-lookup"><span data-stu-id="9996a-123">The *virtualMachine* parameter was **NULL**.</span></span><br/>                                         |
| <dl> <span data-ttu-id="9996a-124"><dt>**VM \_ E \_ VM \_**</dt> mit <dt>0xa0040500</dt></span><span class="sxs-lookup"><span data-stu-id="9996a-124"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                        | <span data-ttu-id="9996a-125">Der virtuelle Computer wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9996a-125">The virtual machine is running.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="9996a-126"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="9996a-126"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="9996a-127">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="9996a-127">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="9996a-128"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9996a-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="9996a-129">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="9996a-129">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="9996a-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9996a-130">Remarks</span></span>

<span data-ttu-id="9996a-131">Es können nur beendete virtuelle Computer gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="9996a-131">Only stopped virtual machines can be deleted.</span></span> <span data-ttu-id="9996a-132">Beachten Sie, dass alle vorhandenen gespeicherten Zustands-oder rückgängig-Laufwerks Daten für diese Konfiguration zusätzlich zur Konfigurationsdatei gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="9996a-132">Note that any existing saved state or undo drive data for this configuration will be deleted in addition to the configuration file.</span></span>

## <a name="requirements"></a><span data-ttu-id="9996a-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9996a-133">Requirements</span></span>



| <span data-ttu-id="9996a-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9996a-134">Requirement</span></span> | <span data-ttu-id="9996a-135">Wert</span><span class="sxs-lookup"><span data-stu-id="9996a-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9996a-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9996a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9996a-137">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9996a-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9996a-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9996a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9996a-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9996a-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9996a-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9996a-140">End of client support</span></span><br/>    | <span data-ttu-id="9996a-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9996a-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9996a-142">Produkt</span><span class="sxs-lookup"><span data-stu-id="9996a-142">Product</span></span><br/>                  | <span data-ttu-id="9996a-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9996a-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9996a-144">Header</span><span class="sxs-lookup"><span data-stu-id="9996a-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="9996a-145"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9996a-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9996a-146">IID</span><span class="sxs-lookup"><span data-stu-id="9996a-146">IID</span></span><br/>                      | <span data-ttu-id="9996a-147">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="9996a-147">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9996a-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9996a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9996a-149">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="9996a-149">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

