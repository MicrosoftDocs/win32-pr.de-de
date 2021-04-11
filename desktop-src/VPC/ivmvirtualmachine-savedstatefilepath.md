---
title: Ivmvirtualmachine savedstatefilepath-Eigenschaft (vpccominterfaces. h)
description: Ruft den vollständigen Pfad zur gespeicherten Zustands Datei ab.
ms.assetid: 01bd5491-4d08-4558-ac33-01b096f057a2
keywords:
- Savedstatefilepath-Eigenschaft virtueller PC
- Savedstatefilepath-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, savedstatefilepath (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SavedStateFilePath
- IVMVirtualMachine.get_SavedStateFilePath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9baea53e3fce2455a2bdfa361e56b45b9b65d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105339"
---
# <a name="ivmvirtualmachinesavedstatefilepath-property"></a><span data-ttu-id="44167-106">Ivmvirtualmachine:: savedstatefilepath (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="44167-106">IVMVirtualMachine::SavedStateFilePath property</span></span>

<span data-ttu-id="44167-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44167-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="44167-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="44167-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="44167-109">Ruft den vollständigen Pfad zur gespeicherten Zustands Datei ab.</span><span class="sxs-lookup"><span data-stu-id="44167-109">Retrieves the full path to the saved state file.</span></span>

<span data-ttu-id="44167-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="44167-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="44167-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="44167-111">Syntax</span></span>


```C++
HRESULT get_SavedStateFilePath(
  [out, retval] BSTR *savedStateFilePath
);
```



## <a name="property-value"></a><span data-ttu-id="44167-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="44167-112">Property value</span></span>

<span data-ttu-id="44167-113">Der voll qualifizierte Pfad zur gespeicherten Zustands Datei der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="44167-113">The fully qualified path to the virtual machine's saved state file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="44167-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="44167-114">Error codes</span></span>



| <span data-ttu-id="44167-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="44167-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="44167-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="44167-116">Meaning</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="44167-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="44167-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="44167-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="44167-118">The operation was successful.</span></span><br/>                           |
| <dl> <span data-ttu-id="44167-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="44167-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="44167-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="44167-120">The parameter is **NULL**.</span></span><br/>                              |
| <dl> <span data-ttu-id="44167-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="44167-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="44167-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="44167-122">The configuration is unknown.</span></span><br/>                           |
| <dl> <span data-ttu-id="44167-123"><dt>VM \_ E \_ VM \_ nicht \_ gespeicherten \_ Status</dt> <dt>0xa00400501</dt></span><span class="sxs-lookup"><span data-stu-id="44167-123"><dt>VM\_E\_VM\_NO\_SAVED\_STATE</dt> <dt>0xA00400501</dt></span></span> </dl> | <span data-ttu-id="44167-124">Der virtuellen Maschine ist keine gespeicherte Zustands Datei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="44167-124">The virtual machine has no associated saved state file.</span></span><br/> |
| <dl> <span data-ttu-id="44167-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="44167-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="44167-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="44167-126">An unexpected error has occurred.</span></span><br/>                       |



## <a name="requirements"></a><span data-ttu-id="44167-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44167-127">Requirements</span></span>



| <span data-ttu-id="44167-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44167-128">Requirement</span></span> | <span data-ttu-id="44167-129">Wert</span><span class="sxs-lookup"><span data-stu-id="44167-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="44167-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44167-130">Minimum supported client</span></span><br/> | <span data-ttu-id="44167-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44167-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="44167-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44167-132">Minimum supported server</span></span><br/> | <span data-ttu-id="44167-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="44167-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="44167-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="44167-134">End of client support</span></span><br/>    | <span data-ttu-id="44167-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="44167-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="44167-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="44167-136">Product</span></span><br/>                  | <span data-ttu-id="44167-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="44167-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="44167-138">Header</span><span class="sxs-lookup"><span data-stu-id="44167-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="44167-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="44167-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="44167-140">IID</span><span class="sxs-lookup"><span data-stu-id="44167-140">IID</span></span><br/>                      | <span data-ttu-id="44167-141">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="44167-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="44167-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44167-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44167-143">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="44167-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

