---
title: Ivmvirtualmachine Startup2-Methode (vpccominterfaces. h)
description: Startet die virtuelle Maschine entweder über den nicht initialisierten oder gespeicherten Zustand mit erweiterten Optionen.
ms.assetid: c2679ea1-bbd5-42dc-9326-2019ad99554c
keywords:
- Startup2-Methode Virtual PC
- Startup2-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Startup2-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b40149b0b21abc126261d8b1ddec34b9948371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391953"
---
# <a name="ivmvirtualmachinestartup2-method"></a><span data-ttu-id="d841f-106">Ivmvirtualmachine:: Startup2-Methode</span><span class="sxs-lookup"><span data-stu-id="d841f-106">IVMVirtualMachine::Startup2 method</span></span>

<span data-ttu-id="d841f-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d841f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d841f-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d841f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d841f-109">Startet den virtuellen Computer (VM) entweder aus dem nicht initialisierten oder gespeicherten Zustand mit erweiterten Optionen.</span><span class="sxs-lookup"><span data-stu-id="d841f-109">Starts the virtual machine (VM) from either the uninitialized or saved state, with advanced options.</span></span>

<span data-ttu-id="d841f-110">Diese Methode bietet einen Mechanismus zum Starten eines virtuellen Computers mit einem differenzierenden Datenträger, auch wenn der Zeitstempel des übergeordneten Datenträgers geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d841f-110">This method provides a mechanism to start a VM with a differencing disk even if the parent disk's timestamp has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d841f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d841f-111">Syntax</span></span>


```C++
HRESULT Startup2(
  [in]          VMStartupOption startupOption,
  [out, retval] IVMTask         **startupTask
);
```



## <a name="parameters"></a><span data-ttu-id="d841f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d841f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d841f-113">*startuption* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d841f-113">*startupOption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d841f-114">Die erweiterte Startoption.</span><span class="sxs-lookup"><span data-stu-id="d841f-114">The advanced startup option.</span></span> <span data-ttu-id="d841f-115">Die möglichen Werte stammen aus der [**vmstartupoption**](vmstartupoption.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="d841f-115">The possible values are from the [**VMStartupOption**](vmstartupoption.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="d841f-116">*startuptask* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d841f-116">*startupTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d841f-117">Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss Fortschritt der Startsequenz zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="d841f-117">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the start sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d841f-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d841f-118">Return value</span></span>

<span data-ttu-id="d841f-119">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d841f-119">This method can return one of these values.</span></span>



| <span data-ttu-id="d841f-120">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="d841f-120">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="d841f-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d841f-121">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d841f-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d841f-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="d841f-123">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d841f-123">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d841f-124"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="d841f-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                               | <span data-ttu-id="d841f-125">Der *startupoption* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d841f-125">The *startupOption* parameter is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="d841f-126"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d841f-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="d841f-127">Der *startuptask* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="d841f-127">The *startupTask* parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="d841f-128"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Zugriff \_ verweigert)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="d841f-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="d841f-129">Der Aufrufer muss über Berechtigungen zum Ausführen des Zugriffs verfügen, um diese VM zu starten</span><span class="sxs-lookup"><span data-stu-id="d841f-129">The caller must have execute access permissions to start this VM.</span></span><br/> |
| <dl> <span data-ttu-id="d841f-130"><dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt></span><span class="sxs-lookup"><span data-stu-id="d841f-130"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="d841f-131">Der Vorgang wurde nicht rechtzeitig beendet.</span><span class="sxs-lookup"><span data-stu-id="d841f-131">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="d841f-132"><dt>**VM \_ E \_ aus \_ \_ Ressource**</dt> <dt>0xa0040203</dt></span><span class="sxs-lookup"><span data-stu-id="d841f-132"><dt>**VM\_E\_OUT\_OF\_RESOURCE**</dt> <dt>0xA0040203</dt></span></span> </dl>                    | <span data-ttu-id="d841f-133">Es sind nicht genügend Host Ressourcen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d841f-133">There are not enough host resources.</span></span><br/>                              |
| <dl> <span data-ttu-id="d841f-134"><dt>**VM \_ E \_ zu \_ viele \_ VMS**</dt> <dt>0xa0040204</dt></span><span class="sxs-lookup"><span data-stu-id="d841f-134"><dt>**VM\_E\_TOO\_MANY\_VMS**</dt> <dt>0xA0040204</dt></span></span> </dl>                       | <span data-ttu-id="d841f-135">Es sind zu viele aktive VMS vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d841f-135">There are too many active VMs.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d841f-136"><dt>**VM \_ E \_ VM \_**</dt> mit <dt>0xa0040500</dt></span><span class="sxs-lookup"><span data-stu-id="d841f-136"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                          | <span data-ttu-id="d841f-137">Der virtuelle Computer wird bereits ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d841f-137">The VM is already running.</span></span><br/>                                        |
| <dl> <span data-ttu-id="d841f-138"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d841f-138"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="d841f-139">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d841f-139">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="d841f-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d841f-140">Remarks</span></span>

<span data-ttu-id="d841f-141">Die folgenden Werte können durch die [**Error**](ivmtask-error.md) -Eigenschaft des zurückgegebenen [**ivmtask**](ivmtask.md) -Objekts zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d841f-141">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="d841f-142">[**Fehler**](ivmtask-error.md) Code/Wert</span><span class="sxs-lookup"><span data-stu-id="d841f-142">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="d841f-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d841f-143">Description</span></span>                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="d841f-144"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xa0040950)</span><span class="sxs-lookup"><span data-stu-id="d841f-144"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span></span><br/>                                                 | <span data-ttu-id="d841f-145">Die Hardware unterstützt keine Virtualisierung.</span><span class="sxs-lookup"><span data-stu-id="d841f-145">The hardware does not support virtualization.</span></span><br/>              |
| <span data-ttu-id="d841f-146"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xa0040951)</span><span class="sxs-lookup"><span data-stu-id="d841f-146"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span></span><br/> | <span data-ttu-id="d841f-147">Die Hardwarevirtualisierung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d841f-147">Hardware virtualization is disabled.</span></span><br/>                       |
| <span data-ttu-id="d841f-148"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xa0040952)</span><span class="sxs-lookup"><span data-stu-id="d841f-148"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span></span><br/>                             | <span data-ttu-id="d841f-149">Sowohl Virtual PC 2007 als auch Windows Virtual PC werden installiert.</span><span class="sxs-lookup"><span data-stu-id="d841f-149">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <span data-ttu-id="d841f-150"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xa0040953)</span><span class="sxs-lookup"><span data-stu-id="d841f-150"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span></span><br/>             | <span data-ttu-id="d841f-151">Andere Virtualisierungssoftware ist installiert.</span><span class="sxs-lookup"><span data-stu-id="d841f-151">Other virtualization software is installed.</span></span><br/>                |
| <span data-ttu-id="d841f-152"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span><span class="sxs-lookup"><span data-stu-id="d841f-152"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span></span><br/>                                                                 | <span data-ttu-id="d841f-153">Es sind nicht genügend Host Ressourcen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d841f-153">There are not enough host resources.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="d841f-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d841f-154">Requirements</span></span>



| <span data-ttu-id="d841f-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d841f-155">Requirement</span></span> | <span data-ttu-id="d841f-156">Wert</span><span class="sxs-lookup"><span data-stu-id="d841f-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d841f-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d841f-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d841f-158">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d841f-158">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d841f-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d841f-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d841f-160">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d841f-160">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d841f-161">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d841f-161">End of client support</span></span><br/>    | <span data-ttu-id="d841f-162">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d841f-162">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d841f-163">Produkt</span><span class="sxs-lookup"><span data-stu-id="d841f-163">Product</span></span><br/>                  | <span data-ttu-id="d841f-164">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d841f-164">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d841f-165">Header</span><span class="sxs-lookup"><span data-stu-id="d841f-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="d841f-166"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d841f-166"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d841f-167">IID</span><span class="sxs-lookup"><span data-stu-id="d841f-167">IID</span></span><br/>                      | <span data-ttu-id="d841f-168">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="d841f-168">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d841f-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d841f-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d841f-170">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="d841f-170">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

