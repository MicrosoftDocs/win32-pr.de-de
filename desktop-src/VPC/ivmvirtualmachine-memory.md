---
title: Ivmvirtualmachine-Speicher Eigenschaft (vpccominterfaces. h)
description: Menge an physischem Arbeitsspeicher auf dem virtuellen Computer in Megabyte.
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Arbeitsspeicher Eigenschaft (Virtual PC)
- Arbeitsspeicher Eigenschaft virtueller PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Arbeitsspeicher (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Memory
- IVMVirtualMachine.get_Memory
- IVMVirtualMachine.put_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b73251b58639e0311e33120cd4bb0e778a017b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338518"
---
# <a name="ivmvirtualmachinememory-property"></a><span data-ttu-id="7e722-106">Ivmvirtualmachine:: memory (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7e722-106">IVMVirtualMachine::Memory property</span></span>

<span data-ttu-id="7e722-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7e722-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7e722-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7e722-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7e722-109">Ruft die Menge des physischen Speichers auf dem virtuellen Computer in Megabyte ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="7e722-109">Retrieves and sets the amount of physical memory in the virtual machine, in megabytes.</span></span>

<span data-ttu-id="7e722-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7e722-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e722-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e722-111">Syntax</span></span>


```C++
HRESULT put_Memory(
  [in]          long megabytesOfMemory
);

HRESULT get_Memory(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="7e722-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7e722-112">Property value</span></span>

<span data-ttu-id="7e722-113">Gibt die Menge des physischen Speichers in Megabyte an.</span><span class="sxs-lookup"><span data-stu-id="7e722-113">Specifies the amount of physical memory, in megabytes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7e722-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7e722-114">Error codes</span></span>



| <span data-ttu-id="7e722-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="7e722-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="7e722-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7e722-116">Meaning</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="7e722-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7e722-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="7e722-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e722-118">The operation was successful.</span></span><br/>                  |
| <dl> <span data-ttu-id="7e722-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7e722-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="7e722-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="7e722-120">The parameter is **NULL**.</span></span><br/>                     |
| <dl> <span data-ttu-id="7e722-121"><dt>E \_ InvalidArg</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="7e722-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="7e722-122">Der-Parameter ist ungültig oder liegt außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="7e722-122">The parameter is not valid or is out of range.</span></span><br/> |
| <dl> <span data-ttu-id="7e722-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="7e722-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="7e722-124">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="7e722-124">The configuration is unknown.</span></span><br/>                  |
| <dl> <span data-ttu-id="7e722-125"><dt>VM \_ E \_ Pref \_ nicht \_ gefunden</dt> <dt>0xa0040300</dt></span><span class="sxs-lookup"><span data-stu-id="7e722-125"><dt>VM\_E\_PREF\_NOT\_FOUND</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="7e722-126">Die Einstellung wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="7e722-126">The preference was not found.</span></span><br/>                  |
| <dl> <span data-ttu-id="7e722-127"><dt>VM \_ E \_ Pref- \_ VM \_ aktiv</dt> <dt>0xa0040302</dt></span><span class="sxs-lookup"><span data-stu-id="7e722-127"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl> | <span data-ttu-id="7e722-128">Der virtuelle Computer wird ausgeführt oder gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7e722-128">The virtual machine is running or saved.</span></span><br/>       |
| <dl> <span data-ttu-id="7e722-129"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7e722-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="7e722-130">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7e722-130">An unexpected error has occurred.</span></span><br/>              |



## <a name="remarks"></a><span data-ttu-id="7e722-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e722-131">Remarks</span></span>

<span data-ttu-id="7e722-132">Der physische Arbeitsspeicher auf einem virtuellen Computer muss mindestens 4 MB betragen.</span><span class="sxs-lookup"><span data-stu-id="7e722-132">The amount of physical memory in a virtual machine must be at least 4 MB.</span></span> <span data-ttu-id="7e722-133">Die Obergrenze für den Arbeitsspeicher hängt von der Host Konfiguration ab, kann jedoch höchstens 3.712 MB betragen.</span><span class="sxs-lookup"><span data-stu-id="7e722-133">The upper limit on memory depends on the host configuration, but can be at most 3,712 MB.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e722-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e722-134">Requirements</span></span>



| <span data-ttu-id="7e722-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e722-135">Requirement</span></span> | <span data-ttu-id="7e722-136">Wert</span><span class="sxs-lookup"><span data-stu-id="7e722-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e722-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e722-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7e722-138">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e722-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e722-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e722-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7e722-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7e722-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7e722-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7e722-141">End of client support</span></span><br/>    | <span data-ttu-id="7e722-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7e722-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7e722-143">Produkt</span><span class="sxs-lookup"><span data-stu-id="7e722-143">Product</span></span><br/>                  | <span data-ttu-id="7e722-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7e722-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7e722-145">Header</span><span class="sxs-lookup"><span data-stu-id="7e722-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e722-146"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e722-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7e722-147">IID</span><span class="sxs-lookup"><span data-stu-id="7e722-147">IID</span></span><br/>                      | <span data-ttu-id="7e722-148">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="7e722-148">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="7e722-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e722-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e722-150">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="7e722-150">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

