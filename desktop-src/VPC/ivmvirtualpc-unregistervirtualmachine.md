---
title: Ivmvirtualpc unregistervirtualmachine-Methode (vpccominterfaces. h)
description: Hebt die Registrierung einer VM-Konfiguration auf, ohne die Konfigurationsdatei zu löschen.
ms.assetid: 82ca6ef3-e9e5-471e-b2dc-0ff689a618d9
keywords:
- Unregistervirtualmachine-Methode Virtual PC
- Unregistervirtualmachine-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, unregistervirtualmachine-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnregisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d74380a822253918791b78bc34ac1c796f595ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478993"
---
# <a name="ivmvirtualpcunregistervirtualmachine-method"></a><span data-ttu-id="82ce4-106">Ivmvirtualpc:: unregistervirtualmachine-Methode</span><span class="sxs-lookup"><span data-stu-id="82ce4-106">IVMVirtualPC::UnregisterVirtualMachine method</span></span>

<span data-ttu-id="82ce4-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="82ce4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="82ce4-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="82ce4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="82ce4-109">Hebt die Registrierung einer Konfiguration eines virtuellen Computers (VM) auf, ohne die Konfigurationsdatei zu löschen.</span><span class="sxs-lookup"><span data-stu-id="82ce4-109">Unregisters a virtual machine (VM) configuration without deleting the configuration file.</span></span>

## <a name="syntax"></a><span data-ttu-id="82ce4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="82ce4-110">Syntax</span></span>


```C++
HRESULT UnregisterVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="82ce4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="82ce4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82ce4-112">*virtualmachine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82ce4-112">*virtualMachine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82ce4-113">Ein Zeiger auf ein [**ivmvirtualmachine**](ivmvirtualmachine.md) -Objekt, das die VM-Konfiguration darstellt, deren Registrierung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="82ce4-113">A pointer to an [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents the VM configuration to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82ce4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82ce4-114">Return value</span></span>

<span data-ttu-id="82ce4-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="82ce4-115">This method can return one of these values.</span></span>



| <span data-ttu-id="82ce4-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="82ce4-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="82ce4-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82ce4-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="82ce4-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="82ce4-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="82ce4-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="82ce4-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="82ce4-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="82ce4-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="82ce4-121">Der Parameter " *virtualmachine* " war **null**.</span><span class="sxs-lookup"><span data-stu-id="82ce4-121">The *virtualMachine* parameter was **NULL**.</span></span><br/>                                         |
| <dl> <span data-ttu-id="82ce4-122"><dt>**VM \_ E \_ VM \_**</dt> mit <dt>0xa0040500</dt></span><span class="sxs-lookup"><span data-stu-id="82ce4-122"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                        | <span data-ttu-id="82ce4-123">Die VM wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82ce4-123">The VM is running.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="82ce4-124"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="82ce4-124"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="82ce4-125">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="82ce4-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="82ce4-126"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="82ce4-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="82ce4-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="82ce4-127">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="82ce4-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82ce4-128">Remarks</span></span>

<span data-ttu-id="82ce4-129">Die Registrierung von nur beendeten VMS kann aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="82ce4-129">Only stopped VMs can be unregistered.</span></span> <span data-ttu-id="82ce4-130">Vorhandene gespeicherte Zustands-oder rückgängig-Laufwerks Daten für diese Konfiguration bleiben erhalten, wenn die Registrierung eines virtuellen Computers aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="82ce4-130">Existing saved state or undo drive data for this configuration will be retained when a VM is unregistered.</span></span>

## <a name="requirements"></a><span data-ttu-id="82ce4-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82ce4-131">Requirements</span></span>



| <span data-ttu-id="82ce4-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82ce4-132">Requirement</span></span> | <span data-ttu-id="82ce4-133">Wert</span><span class="sxs-lookup"><span data-stu-id="82ce4-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="82ce4-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82ce4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="82ce4-135">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82ce4-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82ce4-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82ce4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="82ce4-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="82ce4-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="82ce4-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="82ce4-138">End of client support</span></span><br/>    | <span data-ttu-id="82ce4-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="82ce4-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="82ce4-140">Produkt</span><span class="sxs-lookup"><span data-stu-id="82ce4-140">Product</span></span><br/>                  | <span data-ttu-id="82ce4-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="82ce4-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="82ce4-142">Header</span><span class="sxs-lookup"><span data-stu-id="82ce4-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="82ce4-143"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="82ce4-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="82ce4-144">IID</span><span class="sxs-lookup"><span data-stu-id="82ce4-144">IID</span></span><br/>                      | <span data-ttu-id="82ce4-145">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="82ce4-145">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="82ce4-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82ce4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82ce4-147">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="82ce4-147">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

