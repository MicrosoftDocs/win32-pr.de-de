---
title: Ivmvirtualmachine Reset-Methode (vpccominterfaces. h)
description: Setzt den virtuellen Computer zurück.
ms.assetid: 44daf6be-66ce-4291-a535-c30369eed60f
keywords:
- Methode für virtuellen PC zurücksetzen
- Methode "Virtual PC zurücksetzen", ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Methode zurücksetzen
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Reset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45314eef6d837ac00647d477f3652b63221d977c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478345"
---
# <a name="ivmvirtualmachinereset-method"></a><span data-ttu-id="0f3cc-106">Ivmvirtualmachine:: Reset-Methode</span><span class="sxs-lookup"><span data-stu-id="0f3cc-106">IVMVirtualMachine::Reset method</span></span>

<span data-ttu-id="0f3cc-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0f3cc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0f3cc-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0f3cc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0f3cc-109">Setzt den virtuellen Computer (VM) zurück.</span><span class="sxs-lookup"><span data-stu-id="0f3cc-109">Resets the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f3cc-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f3cc-110">Syntax</span></span>


```C++
HRESULT Reset(
  [out, retval] IVMTask **resetTask
);
```



## <a name="parameters"></a><span data-ttu-id="0f3cc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f3cc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f3cc-112">*resettask* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0f3cc-112">*resetTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0f3cc-113">Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss Status der zurückgesetzten Sequenz der VM zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="0f3cc-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the VM's reset sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f3cc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f3cc-114">Return value</span></span>

<span data-ttu-id="0f3cc-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0f3cc-115">This method can return one of these values.</span></span>



| <span data-ttu-id="0f3cc-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="0f3cc-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="0f3cc-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f3cc-117">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f3cc-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0f3cc-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="0f3cc-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f3cc-119">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="0f3cc-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0f3cc-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="0f3cc-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="0f3cc-121">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="0f3cc-122"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Zugriff \_ verweigert)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="0f3cc-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="0f3cc-123">Der Aufrufer muss über Execute Access-Berechtigungen verfügen, um diesen virtuellen Computer zurückzusetzen</span><span class="sxs-lookup"><span data-stu-id="0f3cc-123">The caller must have execute access permissions to reset this VM.</span></span><br/> |
| <dl> <span data-ttu-id="0f3cc-124"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="0f3cc-124"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="0f3cc-125">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f3cc-125">The VM is not running.</span></span><br/>                                            |
| <dl> <span data-ttu-id="0f3cc-126"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="0f3cc-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="0f3cc-127">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="0f3cc-127">The configuration is unknown.</span></span><br/>                                     |
| <dl> <span data-ttu-id="0f3cc-128"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0f3cc-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="0f3cc-129">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0f3cc-129">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="0f3cc-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f3cc-130">Requirements</span></span>



| <span data-ttu-id="0f3cc-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f3cc-131">Requirement</span></span> | <span data-ttu-id="0f3cc-132">Wert</span><span class="sxs-lookup"><span data-stu-id="0f3cc-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3cc-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f3cc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3cc-134">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f3cc-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f3cc-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f3cc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3cc-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0f3cc-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0f3cc-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0f3cc-137">End of client support</span></span><br/>    | <span data-ttu-id="0f3cc-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0f3cc-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0f3cc-139">Produkt</span><span class="sxs-lookup"><span data-stu-id="0f3cc-139">Product</span></span><br/>                  | <span data-ttu-id="0f3cc-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0f3cc-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0f3cc-141">Header</span><span class="sxs-lookup"><span data-stu-id="0f3cc-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f3cc-142"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f3cc-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0f3cc-143">IID</span><span class="sxs-lookup"><span data-stu-id="0f3cc-143">IID</span></span><br/>                      | <span data-ttu-id="0f3cc-144">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="0f3cc-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="0f3cc-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f3cc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3cc-146">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="0f3cc-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

