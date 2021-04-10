---
title: Ivmvirtualmachine-Start Methode (vpccominterfaces. h)
description: Startet die virtuelle Maschine entweder aus dem nicht initialisierten oder gespeicherten Zustand.
ms.assetid: 82f9b6f1-99b1-4402-93f5-b4aa3520a505
keywords:
- Startup-Methode Virtual PC
- Startup-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Start Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a45e0952fc1a17fc6ba2ea639f2ee87f7b9ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956955"
---
# <a name="ivmvirtualmachinestartup-method"></a><span data-ttu-id="c5895-106">Ivmvirtualmachine:: Startup-Methode</span><span class="sxs-lookup"><span data-stu-id="c5895-106">IVMVirtualMachine::Startup method</span></span>

<span data-ttu-id="c5895-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c5895-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c5895-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c5895-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c5895-109">Startet die virtuelle Maschine entweder aus dem nicht initialisierten oder gespeicherten Zustand.</span><span class="sxs-lookup"><span data-stu-id="c5895-109">Starts the virtual machine from either the uninitialized or saved state.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5895-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5895-110">Syntax</span></span>


```C++
HRESULT Startup(
  [out, retval] IVMTask **startupTask
);
```



## <a name="parameters"></a><span data-ttu-id="c5895-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5895-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5895-112">*startuptask* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c5895-112">*startupTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c5895-113">Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss Status der Startsequenz der virtuellen Maschine zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="c5895-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the virtual machine's startup sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5895-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5895-114">Return value</span></span>

<span data-ttu-id="c5895-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c5895-115">This method can return one of these values.</span></span>



| <span data-ttu-id="c5895-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="c5895-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="c5895-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5895-117">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5895-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c5895-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="c5895-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5895-119">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="c5895-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c5895-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="c5895-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c5895-121">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="c5895-122"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Zugriff \_ verweigert)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="c5895-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="c5895-123">Der Aufrufer muss über Execute-Zugriffsberechtigungen verfügen, um diesen virtuellen Computer zu starten.</span><span class="sxs-lookup"><span data-stu-id="c5895-123">The caller must have execute access permissions to start this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="c5895-124"><dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt></span><span class="sxs-lookup"><span data-stu-id="c5895-124"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="c5895-125">Der Vorgang wurde nicht rechtzeitig beendet.</span><span class="sxs-lookup"><span data-stu-id="c5895-125">The operation did not complete in a timely manner.</span></span><br/>                             |
| <dl> <span data-ttu-id="c5895-126"><dt>**VM \_ E \_ aus \_ \_ Ressource**</dt> <dt>0xa0040203</dt></span><span class="sxs-lookup"><span data-stu-id="c5895-126"><dt>**VM\_E\_OUT\_OF\_RESOURCE**</dt> <dt>0xA0040203</dt></span></span> </dl>                    | <span data-ttu-id="c5895-127">Es sind nicht genügend Host Ressourcen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c5895-127">There are not enough host resources.</span></span><br/>                                           |
| <dl> <span data-ttu-id="c5895-128"><dt>**VM \_ E \_ zu \_ viele \_ VMS**</dt> <dt>0xa0040204</dt></span><span class="sxs-lookup"><span data-stu-id="c5895-128"><dt>**VM\_E\_TOO\_MANY\_VMS**</dt> <dt>0xA0040204</dt></span></span> </dl>                       | <span data-ttu-id="c5895-129">Es sind zu viele aktive virtuelle Computer vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c5895-129">There are too many active virtual machines.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c5895-130"><dt>**VM \_ E \_ VM \_**</dt> mit <dt>0xa0040500</dt></span><span class="sxs-lookup"><span data-stu-id="c5895-130"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                          | <span data-ttu-id="c5895-131">Der virtuelle Computer wird bereits ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5895-131">The virtual machine is already running.</span></span><br/>                                        |
| <dl> <span data-ttu-id="c5895-132"><dt>**VM \_ E \_ Parent- \_ Änderung**</dt> <dt>0xa00400687</dt></span><span class="sxs-lookup"><span data-stu-id="c5895-132"><dt>**VM\_E\_PARENT\_MODIFIED**</dt> <dt>0xA00400687</dt></span></span> </dl>                    | <span data-ttu-id="c5895-133">Der virtuelle Computer kann nicht gestartet werden, da die übergeordnete VHD geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c5895-133">The virtual machine cannot be started as the parent VHD has been modified.</span></span><br/>     |
| <dl> <span data-ttu-id="c5895-134"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c5895-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="c5895-135">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c5895-135">An unexpected error has occurred.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="c5895-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5895-136">Remarks</span></span>

<span data-ttu-id="c5895-137">Wenn die virtuelle Maschine gespeichert wird, wird Sie aus dem gespeicherten Zustand wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="c5895-137">If the virtual machine is saved, it will be restored from the saved state.</span></span>

<span data-ttu-id="c5895-138">Die folgenden Werte können durch die [**Error**](ivmtask-error.md) -Eigenschaft des zurückgegebenen [**ivmtask**](ivmtask.md) -Objekts zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c5895-138">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="c5895-139">[**Fehler**](ivmtask-error.md) Code/Wert</span><span class="sxs-lookup"><span data-stu-id="c5895-139">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="c5895-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5895-140">Description</span></span>                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c5895-141"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xa0040950)</span><span class="sxs-lookup"><span data-stu-id="c5895-141"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span></span><br/>                                                 | <span data-ttu-id="c5895-142">Die Hardware unterstützt keine Virtualisierung.</span><span class="sxs-lookup"><span data-stu-id="c5895-142">The hardware does not support virtualization.</span></span><br/>              |
| <span data-ttu-id="c5895-143"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xa0040951)</span><span class="sxs-lookup"><span data-stu-id="c5895-143"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span></span><br/> | <span data-ttu-id="c5895-144">Die Hardwarevirtualisierung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c5895-144">Hardware virtualization is disabled.</span></span><br/>                       |
| <span data-ttu-id="c5895-145"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xa0040952)</span><span class="sxs-lookup"><span data-stu-id="c5895-145"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span></span><br/>                             | <span data-ttu-id="c5895-146">Sowohl Virtual PC 2007 als auch Windows Virtual PC werden installiert.</span><span class="sxs-lookup"><span data-stu-id="c5895-146">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <span data-ttu-id="c5895-147"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xa0040953)</span><span class="sxs-lookup"><span data-stu-id="c5895-147"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span></span><br/>             | <span data-ttu-id="c5895-148">Andere Virtualisierungssoftware ist installiert.</span><span class="sxs-lookup"><span data-stu-id="c5895-148">Other virtualization software is installed.</span></span><br/>                |
| <span data-ttu-id="c5895-149"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span><span class="sxs-lookup"><span data-stu-id="c5895-149"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span></span><br/>                                                                 | <span data-ttu-id="c5895-150">Es sind nicht genügend Host Ressourcen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c5895-150">There are not enough host resources.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="c5895-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5895-151">Requirements</span></span>



| <span data-ttu-id="c5895-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5895-152">Requirement</span></span> | <span data-ttu-id="c5895-153">Wert</span><span class="sxs-lookup"><span data-stu-id="c5895-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5895-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5895-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c5895-155">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5895-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c5895-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5895-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c5895-157">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c5895-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c5895-158">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c5895-158">End of client support</span></span><br/>    | <span data-ttu-id="c5895-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c5895-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c5895-160">Produkt</span><span class="sxs-lookup"><span data-stu-id="c5895-160">Product</span></span><br/>                  | <span data-ttu-id="c5895-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c5895-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c5895-162">Header</span><span class="sxs-lookup"><span data-stu-id="c5895-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5895-163"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5895-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c5895-164">IID</span><span class="sxs-lookup"><span data-stu-id="c5895-164">IID</span></span><br/>                      | <span data-ttu-id="c5895-165">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="c5895-165">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c5895-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5895-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5895-167">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="c5895-167">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

