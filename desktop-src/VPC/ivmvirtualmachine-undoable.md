---
title: Nicht doable-Eigenschaft für ivmvirtualmachine (vpccominterfaces. h)
description: Bestimmt, ob rückgängig-Laufwerke für Festplatten aktiviert sind, die mit der VM verbunden sind.
ms.assetid: 4f591360-1229-46ae-9925-3a3d02ab3202
keywords:
- Nicht doable Property Virtual PC
- Nicht doable Property Virtual PC, ivmvirtualmachine Interface
- Ivmvirtualmachine Interface Virtual PC, undoable-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Undoable
- IVMVirtualMachine.get_Undoable
- IVMVirtualMachine.put_Undoable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2cbc77f4d68fbdbfcc8d3998e3c207b8f4245c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517855"
---
# <a name="ivmvirtualmachineundoable-property"></a><span data-ttu-id="c9f45-106">Ivmvirtualmachine:: undoable-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c9f45-106">IVMVirtualMachine::Undoable property</span></span>

<span data-ttu-id="c9f45-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c9f45-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c9f45-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c9f45-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c9f45-109">Bestimmt, ob rückgängig-Laufwerke für Festplatten aktiviert sind, die mit dem virtuellen Computer (VM) verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="c9f45-109">Determines whether undo drives are enabled for hard disks connected to the virtual machine (VM).</span></span>

<span data-ttu-id="c9f45-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c9f45-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9f45-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9f45-111">Syntax</span></span>


```C++
HRESULT put_Undoable(
  [in]          VARIANT_BOOL enableUndo
);

HRESULT get_Undoable(
  [out, retval] VARIANT_BOOL *isUndoable
);
```



## <a name="property-value"></a><span data-ttu-id="c9f45-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c9f45-112">Property value</span></span>

<span data-ttu-id="c9f45-113">Gibt **Variant \_ true** an, wenn rückgängig-Laufwerke für Festplatten aktiviert sind, die mit dem virtuellen Computer verbunden sind, und andernfalls **\_ false** .</span><span class="sxs-lookup"><span data-stu-id="c9f45-113">Specifies **VARIANT\_TRUE** if undo drives are enabled for hard disks connected to the VM and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c9f45-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c9f45-114">Error codes</span></span>



| <span data-ttu-id="c9f45-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="c9f45-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="c9f45-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c9f45-116">Meaning</span></span>                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c9f45-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c9f45-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="c9f45-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9f45-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c9f45-119"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c9f45-119"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="c9f45-120">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c9f45-120">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="c9f45-121"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c9f45-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="c9f45-122">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c9f45-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="c9f45-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="c9f45-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="c9f45-124">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c9f45-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="c9f45-125"><dt>VM \_ E \_ Pref- \_ VM \_ aktiv</dt> <dt>0xa0040302</dt></span><span class="sxs-lookup"><span data-stu-id="c9f45-125"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl> | <span data-ttu-id="c9f45-126">Die VM wird ausgeführt oder gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c9f45-126">The VM is running or saved.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="c9f45-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9f45-127">Remarks</span></span>

<span data-ttu-id="c9f45-128">Wenn rückgängig-Laufwerke deaktiviert sind, werden alle vorhandenen rückgängig-Laufwerks Dateien gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c9f45-128">If undo drives are disabled, any existing undo drive files will be deleted.</span></span>

<span data-ttu-id="c9f45-129">Diese Eigenschaft kann nicht festgelegt werden, wenn die VM ausgeführt wird oder gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="c9f45-129">You cannot set this property if the VM is running or saved.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9f45-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9f45-130">Requirements</span></span>



| <span data-ttu-id="c9f45-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9f45-131">Requirement</span></span> | <span data-ttu-id="c9f45-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c9f45-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f45-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9f45-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c9f45-134">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9f45-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9f45-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9f45-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c9f45-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c9f45-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c9f45-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c9f45-137">End of client support</span></span><br/>    | <span data-ttu-id="c9f45-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c9f45-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c9f45-139">Produkt</span><span class="sxs-lookup"><span data-stu-id="c9f45-139">Product</span></span><br/>                  | <span data-ttu-id="c9f45-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c9f45-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c9f45-141">Header</span><span class="sxs-lookup"><span data-stu-id="c9f45-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9f45-142"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9f45-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c9f45-143">IID</span><span class="sxs-lookup"><span data-stu-id="c9f45-143">IID</span></span><br/>                      | <span data-ttu-id="c9f45-144">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="c9f45-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c9f45-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9f45-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f45-146">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="c9f45-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

