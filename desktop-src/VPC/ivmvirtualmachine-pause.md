---
title: Ivmvirtualmachine Pause-Methode (vpccominterfaces. h)
description: Hält den virtuellen Computer an.
ms.assetid: 29ac40c4-7713-4782-8a31-42f2c32b8f7d
keywords:
- Anhaltemethode Virtual PC
- Pause-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Pause-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Pause
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c953da05d34c999066a6bc87cb1f51983defbd5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859080"
---
# <a name="ivmvirtualmachinepause-method"></a><span data-ttu-id="d1208-106">Ivmvirtualmachine::P ause-Methode</span><span class="sxs-lookup"><span data-stu-id="d1208-106">IVMVirtualMachine::Pause method</span></span>

<span data-ttu-id="d1208-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d1208-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d1208-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d1208-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d1208-109">Hält den virtuellen Computer (VM) an.</span><span class="sxs-lookup"><span data-stu-id="d1208-109">Pauses the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1208-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1208-110">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="d1208-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1208-111">Parameters</span></span>

<span data-ttu-id="d1208-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d1208-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1208-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1208-113">Return value</span></span>

<span data-ttu-id="d1208-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d1208-114">This method can return one of these values.</span></span>



| <span data-ttu-id="d1208-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="d1208-115">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="d1208-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1208-116">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1208-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d1208-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="d1208-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1208-118">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d1208-119"><dt>**E \_**</dt> <dt>0x80004005</dt> fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="d1208-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="d1208-120">Der virtuelle Computer wurde bereits angehalten.</span><span class="sxs-lookup"><span data-stu-id="d1208-120">The VM is already paused.</span></span><br/>                                         |
| <dl> <span data-ttu-id="d1208-121"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Zugriff \_ verweigert)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="d1208-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="d1208-122">Der Aufrufer muss über Berechtigungen zum Ausführen des Zugriffs verfügen, um diese VM anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="d1208-122">The caller must have execute access permissions to pause this VM.</span></span><br/> |
| <dl> <span data-ttu-id="d1208-123"><dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt></span><span class="sxs-lookup"><span data-stu-id="d1208-123"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="d1208-124">Der Vorgang wurde nicht rechtzeitig beendet.</span><span class="sxs-lookup"><span data-stu-id="d1208-124">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="d1208-125"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="d1208-125"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="d1208-126">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1208-126">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="d1208-127"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="d1208-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="d1208-128">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="d1208-128">The configuration is unknown.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d1208-129"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d1208-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="d1208-130">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d1208-130">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="d1208-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1208-131">Remarks</span></span>

<span data-ttu-id="d1208-132">Durch anhalten wird der aktuelle Zustand der **VM nicht gespeichert** .</span><span class="sxs-lookup"><span data-stu-id="d1208-132">**Pause** does not save the current state of the VM.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1208-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1208-133">Requirements</span></span>



| <span data-ttu-id="d1208-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1208-134">Requirement</span></span> | <span data-ttu-id="d1208-135">Wert</span><span class="sxs-lookup"><span data-stu-id="d1208-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1208-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1208-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d1208-137">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1208-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1208-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1208-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d1208-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d1208-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d1208-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d1208-140">End of client support</span></span><br/>    | <span data-ttu-id="d1208-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d1208-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d1208-142">Produkt</span><span class="sxs-lookup"><span data-stu-id="d1208-142">Product</span></span><br/>                  | <span data-ttu-id="d1208-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d1208-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d1208-144">Header</span><span class="sxs-lookup"><span data-stu-id="d1208-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1208-145"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1208-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d1208-146">IID</span><span class="sxs-lookup"><span data-stu-id="d1208-146">IID</span></span><br/>                      | <span data-ttu-id="d1208-147">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="d1208-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d1208-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1208-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1208-149">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="d1208-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

