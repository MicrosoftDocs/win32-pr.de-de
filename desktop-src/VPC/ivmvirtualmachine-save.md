---
title: Ivmvirtualmachine-Methode zum Speichern (vpccominterfaces. h)
description: Speichert den Zustand der virtuellen Maschine (VM).
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- Virtual PC-Methode speichern
- Save Method Virtual PC, ivmvirtualmachine Interface
- Ivmvirtualmachine Interface Virtual PC, Save-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Save
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b4dbe18b89f107657d67fb7e7b90e024b01383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742881"
---
# <a name="ivmvirtualmachinesave-method"></a><span data-ttu-id="adcf1-106">Ivmvirtualmachine:: Save-Methode</span><span class="sxs-lookup"><span data-stu-id="adcf1-106">IVMVirtualMachine::Save method</span></span>

<span data-ttu-id="adcf1-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="adcf1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="adcf1-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="adcf1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="adcf1-109">Speichert den Zustand der virtuellen Maschine (VM).</span><span class="sxs-lookup"><span data-stu-id="adcf1-109">Saves the virtual machine (VM) state.</span></span>

## <a name="syntax"></a><span data-ttu-id="adcf1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="adcf1-110">Syntax</span></span>


```C++
HRESULT Save(
  [out, retval] IVMTask **saveTask
);
```



## <a name="parameters"></a><span data-ttu-id="adcf1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="adcf1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adcf1-112">*savetask* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="adcf1-112">*saveTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="adcf1-113">Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss Fortschritt der Zustands Speicher Sequenz der VM zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="adcf1-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the VM's state saving sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adcf1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="adcf1-114">Return value</span></span>

<span data-ttu-id="adcf1-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="adcf1-115">This method can return one of these values.</span></span>



| <span data-ttu-id="adcf1-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="adcf1-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="adcf1-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="adcf1-117">Description</span></span>                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="adcf1-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="adcf1-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="adcf1-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="adcf1-119">The operation was successful.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="adcf1-120"><dt>**E \_**</dt> <dt>0x80004005</dt> fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="adcf1-120"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="adcf1-121">Die VM konnte nicht gespeichert werden, da die Rückgängig-Datenträger zum Löschen markiert waren.</span><span class="sxs-lookup"><span data-stu-id="adcf1-121">The VM could not be saved because the undo disks were marked for deletion.</span></span><br/>    |
| <dl> <span data-ttu-id="adcf1-122"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="adcf1-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="adcf1-123">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="adcf1-123">The parameter is **NULL**.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="adcf1-124"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Zugriff \_ verweigert)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="adcf1-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="adcf1-125">Der Aufrufer muss über Berechtigungen zum Ausführen des Zugriffs verfügen, um den Status dieser VM zu speichern.</span><span class="sxs-lookup"><span data-stu-id="adcf1-125">The caller must have execute access permissions to save the state of this VM.</span></span><br/> |
| <dl> <span data-ttu-id="adcf1-126"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="adcf1-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="adcf1-127">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="adcf1-127">The VM is not running.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="adcf1-128"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="adcf1-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="adcf1-129">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="adcf1-129">An unexpected error has occurred.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="adcf1-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="adcf1-130">Remarks</span></span>

<span data-ttu-id="adcf1-131">Der virtuelle Computer wird ausgeschaltet, wenn der **Sicherungs Task den** Abschluss erreicht.</span><span class="sxs-lookup"><span data-stu-id="adcf1-131">The VM is turned off when the **Save** task reaches completion.</span></span> <span data-ttu-id="adcf1-132">Die [**ivmvirtualmachine:: State**](ivmvirtualmachine-state.md) -Eigenschaft enthält den Speicherort **vmvmstate \_** , während der Speichervorgang ausgeführt wird, gefolgt von **vmvmstate \_** , wenn der Speichervorgang abgeschlossen und der virtuelle Computer ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="adcf1-132">The [**IVMVirtualMachine::State**](ivmvirtualmachine-state.md) property will contain **vmVMState\_Saving** while the save is in progress, followed by **vmVMState\_Saved** when the save has completed and the VM is turned off.</span></span>

## <a name="requirements"></a><span data-ttu-id="adcf1-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="adcf1-133">Requirements</span></span>



| <span data-ttu-id="adcf1-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="adcf1-134">Requirement</span></span> | <span data-ttu-id="adcf1-135">Wert</span><span class="sxs-lookup"><span data-stu-id="adcf1-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="adcf1-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="adcf1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="adcf1-137">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="adcf1-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="adcf1-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="adcf1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="adcf1-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="adcf1-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="adcf1-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="adcf1-140">End of client support</span></span><br/>    | <span data-ttu-id="adcf1-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="adcf1-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="adcf1-142">Produkt</span><span class="sxs-lookup"><span data-stu-id="adcf1-142">Product</span></span><br/>                  | <span data-ttu-id="adcf1-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="adcf1-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="adcf1-144">Header</span><span class="sxs-lookup"><span data-stu-id="adcf1-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="adcf1-145"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="adcf1-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="adcf1-146">IID</span><span class="sxs-lookup"><span data-stu-id="adcf1-146">IID</span></span><br/>                      | <span data-ttu-id="adcf1-147">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="adcf1-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="adcf1-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adcf1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adcf1-149">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="adcf1-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

