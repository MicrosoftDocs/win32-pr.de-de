---
title: Ivmkeyboard hasexclusiveaccess-Eigenschaft (vpccominterfaces. h)
description: Gibt an, ob dieses-Objekt über eine exklusive Kontrolle über das Tastatur Gerät der VM verfügt.
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- Hasexclusiveaccess-Eigenschaft virtueller PC
- Hasexclusiveaccess-Eigenschaft virtueller PC, ivmkeyboard-Schnittstelle
- Ivmkeyboard Interface Virtual PC, hasexclusiveaccess (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMKeyboard.HasExclusiveAccess
- IVMKeyboard.get_HasExclusiveAccess
- IVMKeyboard.put_HasExclusiveAccess
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62c235f3b4325a70a939239ac1e44360b3b5d9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105680"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a><span data-ttu-id="2acf8-106">Ivmkeyboard:: hasexclusiveaccess (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2acf8-106">IVMKeyboard::HasExclusiveAccess property</span></span>

<span data-ttu-id="2acf8-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2acf8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2acf8-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2acf8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2acf8-109">Gibt an, ob dieses Objekt über eine exklusive Kontrolle über das Tastatur Gerät (VM) des virtuellen Computers verfügt.</span><span class="sxs-lookup"><span data-stu-id="2acf8-109">Indicates whether this object has exclusive control over the virtual machine's (VM) keyboard device.</span></span>

<span data-ttu-id="2acf8-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2acf8-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2acf8-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2acf8-111">Syntax</span></span>


```C++
HRESULT put_HasExclusiveAccess(
  [in]          VARIANT_BOOL makeExclusive
);

HRESULT get_HasExclusiveAccess(
  [out, retval] VARIANT_BOOL *isExclusive
);
```



## <a name="property-value"></a><span data-ttu-id="2acf8-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2acf8-112">Property value</span></span>

<span data-ttu-id="2acf8-113">**True** , wenn exklusiver Zugriff auf das Tastatur Gerät der VM abgerufen wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="2acf8-113">**TRUE** if exclusive access to the VM's keyboard device has been acquired, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2acf8-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2acf8-114">Error codes</span></span>



| <span data-ttu-id="2acf8-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="2acf8-115">Name/value</span></span>                                                                                                                                                                   | <span data-ttu-id="2acf8-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2acf8-116">Meaning</span></span>                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2acf8-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2acf8-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                      | <span data-ttu-id="2acf8-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="2acf8-118">The operation was successful.</span></span><br/>                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="2acf8-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2acf8-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                        | <span data-ttu-id="2acf8-120">Der *isexclusive* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="2acf8-120">The *isExclusive* parameter is **NULL**.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="2acf8-121"><dt>S \_ Falsch</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2acf8-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                   | <span data-ttu-id="2acf8-122">Der angeforderte exklusive Modus ist für dieses Gerät bereits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2acf8-122">The requested exclusive mode is already set for this device.</span></span> <span data-ttu-id="2acf8-123">Dies kann der Fall sein, wenn Sie versuchen, den exklusiven Modus festzulegen, wenn er bereits abgerufen wurde, oder wenn Sie den exklusiven Modus freigeben möchten, wenn er zuvor noch nicht abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="2acf8-123">This can happen when trying to set exclusive mode when it has already been acquired, or when trying to release exclusive mode when it had not been previously acquired.</span></span><br/> |
| <dl> <span data-ttu-id="2acf8-124"><dt>VM \_ E \_ Set \_ Exclusive \_ Mode \_ Fail</dt> <dt>0xa0040825</dt></span><span class="sxs-lookup"><span data-stu-id="2acf8-124"><dt>VM\_E\_SET\_EXCLUSIVE\_MODE\_FAIL</dt> <dt>0xA0040825</dt></span></span> </dl> | <span data-ttu-id="2acf8-125">Der exklusive Modus konnte nicht wie angefordert festgelegt oder freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2acf8-125">Failed to set or release exclusive mode as requested.</span></span> <span data-ttu-id="2acf8-126">Dies kann daran liegen, dass der virtuelle Computer nicht mehr ausgeführt wird oder dass ein anderer Prozess bereits exklusiven Modus auf dem Tastatur Gerät der VM erworben hat.</span><span class="sxs-lookup"><span data-stu-id="2acf8-126">This could be because the VM is no longer running, or because another process has already acquired exclusive mode on the VM's keyboard device.</span></span><br/>                                 |
| <dl> <span data-ttu-id="2acf8-127"><dt>E \_ InvalidArg</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="2acf8-127"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                     | <span data-ttu-id="2acf8-128">Die angegebene Zeichenfolge ist leer oder enthält einen ungültigen Schlüsselcode.</span><span class="sxs-lookup"><span data-stu-id="2acf8-128">The specified string is empty, or contains an invalid key code.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="2acf8-129"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2acf8-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                | <span data-ttu-id="2acf8-130">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2acf8-130">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                    |



## <a name="requirements"></a><span data-ttu-id="2acf8-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2acf8-131">Requirements</span></span>



| <span data-ttu-id="2acf8-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2acf8-132">Requirement</span></span> | <span data-ttu-id="2acf8-133">Wert</span><span class="sxs-lookup"><span data-stu-id="2acf8-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2acf8-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2acf8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2acf8-135">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2acf8-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2acf8-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2acf8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2acf8-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2acf8-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2acf8-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2acf8-138">End of client support</span></span><br/>    | <span data-ttu-id="2acf8-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2acf8-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2acf8-140">Produkt</span><span class="sxs-lookup"><span data-stu-id="2acf8-140">Product</span></span><br/>                  | <span data-ttu-id="2acf8-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2acf8-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2acf8-142">Header</span><span class="sxs-lookup"><span data-stu-id="2acf8-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="2acf8-143"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2acf8-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2acf8-144">IID</span><span class="sxs-lookup"><span data-stu-id="2acf8-144">IID</span></span><br/>                      | <span data-ttu-id="2acf8-145">IID \_ ivmkeyboard ist als 00695b2e-c5ad-4d6e-B1ab-336ed121f 8c4 definiert.</span><span class="sxs-lookup"><span data-stu-id="2acf8-145">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="2acf8-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2acf8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2acf8-147">**Ivmkeyboard**</span><span class="sxs-lookup"><span data-stu-id="2acf8-147">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

