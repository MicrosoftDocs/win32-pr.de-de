---
title: Ivmvirtualmachine biosguid-Eigenschaft (vpccominterfaces. h)
description: Die BIOS-GUID.
ms.assetid: d866838d-31e9-41f1-be57-43e778b9db95
keywords:
- Biosguid-Eigenschaft virtueller PC
- Biosguid-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, biosguid-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSGUID
- IVMVirtualMachine.get_BIOSGUID
- IVMVirtualMachine.put_BIOSGUID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10263e32ab71c2a5b9533b3dde6547f774d6b302
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858863"
---
# <a name="ivmvirtualmachinebiosguid-property"></a><span data-ttu-id="8eac0-106">Ivmvirtualmachine:: biosguid-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8eac0-106">IVMVirtualMachine::BIOSGUID property</span></span>

<span data-ttu-id="8eac0-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8eac0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8eac0-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8eac0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8eac0-109">Ruft die BIOS-GUID ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="8eac0-109">Retrieves and sets the BIOS GUID.</span></span>

<span data-ttu-id="8eac0-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8eac0-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eac0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8eac0-111">Syntax</span></span>


```C++
HRESULT put_BIOSGUID(
  [in]          BSTR biosGUID
);

HRESULT get_BIOSGUID(
  [out, retval] BSTR *biosGUID
);
```



## <a name="property-value"></a><span data-ttu-id="8eac0-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8eac0-112">Property value</span></span>

<span data-ttu-id="8eac0-113">Gibt die BIOS-GUID an.</span><span class="sxs-lookup"><span data-stu-id="8eac0-113">Specifies the BIOS GUID.</span></span> <span data-ttu-id="8eac0-114">Schließen Sie die hexadezimal Ziffern um die linke und die Rechte Klammer</span><span class="sxs-lookup"><span data-stu-id="8eac0-114">Include left and right braces around the hex digits.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8eac0-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="8eac0-115">Error codes</span></span>



| <span data-ttu-id="8eac0-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="8eac0-116">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="8eac0-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8eac0-117">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="8eac0-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8eac0-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="8eac0-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="8eac0-119">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="8eac0-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8eac0-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="8eac0-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="8eac0-121">The parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="8eac0-122"><dt>E \_ InvalidArg</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="8eac0-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="8eac0-123">Der-Parameter ist ungültig oder eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8eac0-123">The parameter is not valid or is an empty string.</span></span><br/>   |
| <dl> <span data-ttu-id="8eac0-124"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="8eac0-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="8eac0-125">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="8eac0-125">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="8eac0-126"><dt>VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_ </dt> <dt>0xa004020b</dt> gespeichert</span><span class="sxs-lookup"><span data-stu-id="8eac0-126"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="8eac0-127">Der virtuelle Computer befindet sich im Zustand "wird ausgeführt" oder "gespeichert".</span><span class="sxs-lookup"><span data-stu-id="8eac0-127">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="8eac0-128"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8eac0-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="8eac0-129">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8eac0-129">An unexpected error has occurred.</span></span><br/>                   |



## <a name="remarks"></a><span data-ttu-id="8eac0-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8eac0-130">Remarks</span></span>

<span data-ttu-id="8eac0-131">Diese Eigenschaft enthält keine gültigen Informationen, bis der virtuelle Computer zum ersten Mal gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="8eac0-131">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="8eac0-132">Eine leere Zeichenfolge wird zurückgegeben, wenn Sie vor dem ersten Start gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="8eac0-132">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eac0-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8eac0-133">Requirements</span></span>



| <span data-ttu-id="8eac0-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8eac0-134">Requirement</span></span> | <span data-ttu-id="8eac0-135">Wert</span><span class="sxs-lookup"><span data-stu-id="8eac0-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eac0-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8eac0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8eac0-137">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8eac0-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8eac0-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8eac0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8eac0-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8eac0-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8eac0-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="8eac0-140">End of client support</span></span><br/>    | <span data-ttu-id="8eac0-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8eac0-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8eac0-142">Produkt</span><span class="sxs-lookup"><span data-stu-id="8eac0-142">Product</span></span><br/>                  | <span data-ttu-id="8eac0-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8eac0-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8eac0-144">Header</span><span class="sxs-lookup"><span data-stu-id="8eac0-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eac0-145"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eac0-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8eac0-146">IID</span><span class="sxs-lookup"><span data-stu-id="8eac0-146">IID</span></span><br/>                      | <span data-ttu-id="8eac0-147">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="8eac0-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="8eac0-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8eac0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eac0-149">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="8eac0-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

