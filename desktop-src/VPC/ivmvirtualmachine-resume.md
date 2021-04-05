---
title: Ivmvirtualmachine Resume-Methode (vpccominterfaces. h)
description: Setzt den virtuellen Computer fort.
ms.assetid: 4a2d6b64-8dcf-484e-940d-b0180aba9f01
keywords:
- Virtual PC-Methode wieder aufnehmen
- Resume-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Resume-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Resume
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c24af1e1a00aa0fa29acc077faf48287c0307414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859136"
---
# <a name="ivmvirtualmachineresume-method"></a><span data-ttu-id="4f8ad-106">Ivmvirtualmachine:: Resume-Methode</span><span class="sxs-lookup"><span data-stu-id="4f8ad-106">IVMVirtualMachine::Resume method</span></span>

<span data-ttu-id="4f8ad-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4f8ad-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4f8ad-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4f8ad-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4f8ad-109">Setzt den virtuellen Computer (VM) fort.</span><span class="sxs-lookup"><span data-stu-id="4f8ad-109">Resumes the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f8ad-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f8ad-110">Syntax</span></span>


```C++
HRESULT Resume();
```



## <a name="parameters"></a><span data-ttu-id="4f8ad-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f8ad-111">Parameters</span></span>

<span data-ttu-id="4f8ad-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4f8ad-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f8ad-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f8ad-113">Return value</span></span>

<span data-ttu-id="4f8ad-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4f8ad-114">This method can return one of these values.</span></span>



| <span data-ttu-id="4f8ad-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="4f8ad-115">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="4f8ad-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f8ad-116">Description</span></span>                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f8ad-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4f8ad-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="4f8ad-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f8ad-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="4f8ad-119"><dt>**E \_**</dt> <dt>0x80004005</dt> fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="4f8ad-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="4f8ad-120">Der virtuelle Computer wurde nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="4f8ad-120">The VM is not paused.</span></span><br/>                                              |
| <dl> <span data-ttu-id="4f8ad-121"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Zugriff \_ verweigert)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="4f8ad-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="4f8ad-122">Der Aufrufer muss über Execute Access-Berechtigungen verfügen, um diesen virtuellen Computer fortsetzen</span><span class="sxs-lookup"><span data-stu-id="4f8ad-122">The caller must have execute access permissions to resume this VM.</span></span><br/> |
| <dl> <span data-ttu-id="4f8ad-123"><dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt></span><span class="sxs-lookup"><span data-stu-id="4f8ad-123"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="4f8ad-124">Der Vorgang wurde nicht rechtzeitig beendet.</span><span class="sxs-lookup"><span data-stu-id="4f8ad-124">The operation did not complete in a timely manner.</span></span><br/>                 |
| <dl> <span data-ttu-id="4f8ad-125"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="4f8ad-125"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="4f8ad-126">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f8ad-126">The VM is not running.</span></span><br/>                                             |
| <dl> <span data-ttu-id="4f8ad-127"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="4f8ad-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="4f8ad-128">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="4f8ad-128">The configuration is unknown.</span></span><br/>                                      |
| <dl> <span data-ttu-id="4f8ad-129"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4f8ad-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="4f8ad-130">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="4f8ad-130">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="4f8ad-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f8ad-131">Requirements</span></span>



| <span data-ttu-id="4f8ad-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f8ad-132">Requirement</span></span> | <span data-ttu-id="4f8ad-133">Wert</span><span class="sxs-lookup"><span data-stu-id="4f8ad-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f8ad-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f8ad-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4f8ad-135">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f8ad-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f8ad-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f8ad-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4f8ad-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4f8ad-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4f8ad-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4f8ad-138">End of client support</span></span><br/>    | <span data-ttu-id="4f8ad-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4f8ad-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4f8ad-140">Produkt</span><span class="sxs-lookup"><span data-stu-id="4f8ad-140">Product</span></span><br/>                  | <span data-ttu-id="4f8ad-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4f8ad-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4f8ad-142">Header</span><span class="sxs-lookup"><span data-stu-id="4f8ad-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f8ad-143"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f8ad-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4f8ad-144">IID</span><span class="sxs-lookup"><span data-stu-id="4f8ad-144">IID</span></span><br/>                      | <span data-ttu-id="4f8ad-145">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="4f8ad-145">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4f8ad-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f8ad-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f8ad-147">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="4f8ad-147">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

