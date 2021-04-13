---
title: Ivmvirtualmachine Notes-Eigenschaft (vpccominterfaces. h)
description: Hinweise zum virtuellen Computer.
ms.assetid: 4be6842b-31b2-4619-a6ab-b728be1e2174
keywords:
- Notes-Eigenschaft Virtual PC
- Notes-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Notes (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Notes
- IVMVirtualMachine.get_Notes
- IVMVirtualMachine.put_Notes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca8fba8659a8f9546866129f21299e44006eb496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478681"
---
# <a name="ivmvirtualmachinenotes-property"></a><span data-ttu-id="bb946-106">Ivmvirtualmachine:: Notes (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bb946-106">IVMVirtualMachine::Notes property</span></span>

<span data-ttu-id="bb946-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bb946-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bb946-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bb946-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bb946-109">Ruft die Hinweise für den virtuellen Computer ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="bb946-109">Retrieves and sets the notes for the virtual machine.</span></span>

<span data-ttu-id="bb946-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="bb946-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb946-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb946-111">Syntax</span></span>


```C++
HRESULT put_Notes(
  [in]          BSTR virtualMachineNotes
);

HRESULT get_Notes(
  [out, retval] BSTR *virtualMachineNotes
);
```



## <a name="property-value"></a><span data-ttu-id="bb946-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="bb946-112">Property value</span></span>

<span data-ttu-id="bb946-113">Gibt die Anmerkungen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="bb946-113">Specifies the notes for the virtual machine.</span></span> <span data-ttu-id="bb946-114">Die maximale Länge der Zeichenfolge beträgt 65.536 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="bb946-114">The maximum length of the string is 65,536 characters.</span></span>

<span data-ttu-id="bb946-115">Um Notizen zu entfernen, übergeben Sie eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="bb946-115">To remove any notes, pass an empty string.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bb946-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="bb946-116">Error codes</span></span>



| <span data-ttu-id="bb946-117">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="bb946-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="bb946-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bb946-118">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb946-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bb946-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="bb946-120">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb946-120">The operation was successful.</span></span><br/>                                       |
| <dl> <span data-ttu-id="bb946-121"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bb946-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="bb946-122">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="bb946-122">The parameter is **NULL**.</span></span><br/>                                          |
| <dl> <span data-ttu-id="bb946-123"><dt>E \_ InvalidArg</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="bb946-123"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="bb946-124">Der-Parameter ist ungültig oder enthält mehr als 65.536 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="bb946-124">The parameter is not valid or contains more than 65,536 characters.</span></span><br/> |
| <dl> <span data-ttu-id="bb946-125"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="bb946-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="bb946-126">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="bb946-126">The configuration is unknown.</span></span><br/>                                       |
| <dl> <span data-ttu-id="bb946-127"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bb946-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="bb946-128">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="bb946-128">An unexpected error has occurred.</span></span><br/>                                   |



## <a name="requirements"></a><span data-ttu-id="bb946-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb946-129">Requirements</span></span>



| <span data-ttu-id="bb946-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb946-130">Requirement</span></span> | <span data-ttu-id="bb946-131">Wert</span><span class="sxs-lookup"><span data-stu-id="bb946-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb946-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb946-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bb946-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb946-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb946-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb946-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bb946-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bb946-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bb946-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="bb946-136">End of client support</span></span><br/>    | <span data-ttu-id="bb946-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb946-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bb946-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="bb946-138">Product</span></span><br/>                  | <span data-ttu-id="bb946-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bb946-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bb946-140">Header</span><span class="sxs-lookup"><span data-stu-id="bb946-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb946-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb946-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bb946-142">IID</span><span class="sxs-lookup"><span data-stu-id="bb946-142">IID</span></span><br/>                      | <span data-ttu-id="bb946-143">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="bb946-143">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="bb946-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb946-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb946-145">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="bb946-145">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

