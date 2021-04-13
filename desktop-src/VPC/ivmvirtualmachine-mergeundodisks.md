---
title: Ivmvirtualmachine mergeundodisks-Methode (vpccominterfaces. h)
description: Führt die virtuellen Rückgängig-Datenträger zusammen.
ms.assetid: 6445b097-220e-48c4-9a7b-1139ca7b3338
keywords:
- Mergeundodisks-Methode virtueller PC
- Mergeundodisks-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, mergeundodisks-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.MergeUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48863bf998ebc02bac93aa9e74d8cdbe07265477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341067"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a><span data-ttu-id="7fbf1-106">Ivmvirtualmachine:: mergeundodisks-Methode</span><span class="sxs-lookup"><span data-stu-id="7fbf1-106">IVMVirtualMachine::MergeUndoDisks method</span></span>

<span data-ttu-id="7fbf1-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7fbf1-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7fbf1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7fbf1-109">Führt die virtuellen Rückgängig-Datenträger zusammen.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-109">Merges the virtual undo disks.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fbf1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fbf1-110">Syntax</span></span>


```C++
HRESULT MergeUndoDisks(
  [out, retval] IVMTask **undoMergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="7fbf1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fbf1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fbf1-112">*rückgängig machen* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7fbf1-112">*undoMergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7fbf1-113">Ein [**ivmtask**](ivmtask.md) -Objekt, das zum Nachverfolgen der Image Erstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-113">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fbf1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7fbf1-114">Return value</span></span>

<span data-ttu-id="7fbf1-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-115">This method can return one of these values.</span></span>



| <span data-ttu-id="7fbf1-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="7fbf1-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="7fbf1-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7fbf1-117">Description</span></span>                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7fbf1-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf1-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="7fbf1-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-119">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="7fbf1-120"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf1-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="7fbf1-121">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-121">An unexpected error has occurred.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="7fbf1-122"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf1-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="7fbf1-123">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-123">The parameter is **NULL**.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="7fbf1-124"><dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf1-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="7fbf1-125">Das System kann den vom *converteddiskimagepath* -Parameter angegebenen Pfad nicht finden, oder einer der übergeordneten Datenträger ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-125">The system cannot find the path specified by the *convertedDiskImagePath* parameter or one of the parent disks is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="7fbf1-126"><dt>**E \_ AccessDenied**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf1-126"><dt>**E\_ACCESSDENIED**</dt> <dt>0x80070005</dt></span></span> </dl>                               | <span data-ttu-id="7fbf1-127">Der aktuelle Benutzer hat keinen ausreichenden Zugriff auf die übergeordnete Datei.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-127">The current user has insufficient access to the parent file.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="7fbf1-128"><dt>**E \_ Handle**</dt> <dt>0x80070006</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf1-128"><dt>**E\_HANDLE**</dt> <dt>0x80070006</dt></span></span> </dl>                                     | <span data-ttu-id="7fbf1-129">Einer der übergeordneten Datenträger wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-129">One of the parent disks is in use.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="7fbf1-130"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf1-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="7fbf1-131">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-131">The configuration is unknown.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="7fbf1-132"><dt>**VM \_ E \_ VM \_**</dt> mit <dt>0xa0040500</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf1-132"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                            | <span data-ttu-id="7fbf1-133">Der virtuelle Computer wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-133">The virtual machine is running.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="7fbf1-134"><dt>**VM \_ E \_ - \_ Datei \_**</dt> schreibgeschützt <dt>0xa004067a</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf1-134"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                       | <span data-ttu-id="7fbf1-135">Das übergeordnete Element von virtuellen Rückgängig-Datenträgern ist als schreibgeschützt gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-135">The parent of virtual undo disks is marked as read only.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="7fbf1-136"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf1-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="7fbf1-137">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-137">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="7fbf1-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fbf1-138">Remarks</span></span>

<span data-ttu-id="7fbf1-139">' **Mergeundodisks** ' kann nicht aufgerufen werden, während der virtuelle Computer weiterhin ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-139">**MergeUndoDisks** cannot be called while the virtual machine is still running.</span></span> <span data-ttu-id="7fbf1-140">Verwenden Sie [**ivmvirtualmachine:: Save**](ivmvirtualmachine-save.md) , um den Status des virtuellen Computers vor dem Aufrufen von **mergeundodisks** zu speichern, oder [**ivmvirtualmachine:: Turnoff**](ivmvirtualmachine-turnoff.md) , um den virtuellen Computer zu deaktivieren, ohne zuvor seinen aktuellen Zustand zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-140">Use [**IVMVirtualMachine::Save**](ivmvirtualmachine-save.md) to save the state of the virtual machine before calling **MergeUndoDisks**, or [**IVMVirtualMachine::TurnOff**](ivmvirtualmachine-turnoff.md) to turn off the virtual machine without saving its current state beforehand.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fbf1-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fbf1-141">Requirements</span></span>



| <span data-ttu-id="7fbf1-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7fbf1-142">Requirement</span></span> | <span data-ttu-id="7fbf1-143">Wert</span><span class="sxs-lookup"><span data-stu-id="7fbf1-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbf1-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7fbf1-144">Minimum supported client</span></span><br/> | <span data-ttu-id="7fbf1-145">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fbf1-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7fbf1-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7fbf1-146">Minimum supported server</span></span><br/> | <span data-ttu-id="7fbf1-147">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7fbf1-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7fbf1-148">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7fbf1-148">End of client support</span></span><br/>    | <span data-ttu-id="7fbf1-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7fbf1-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7fbf1-150">Produkt</span><span class="sxs-lookup"><span data-stu-id="7fbf1-150">Product</span></span><br/>                  | <span data-ttu-id="7fbf1-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7fbf1-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7fbf1-152">Header</span><span class="sxs-lookup"><span data-stu-id="7fbf1-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fbf1-153"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf1-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7fbf1-154">IID</span><span class="sxs-lookup"><span data-stu-id="7fbf1-154">IID</span></span><br/>                      | <span data-ttu-id="7fbf1-155">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="7fbf1-155">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="7fbf1-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fbf1-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fbf1-157">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="7fbf1-157">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

