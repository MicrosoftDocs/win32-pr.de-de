---
title: Ivmdvddrive AttachHostDrive-Methode (vpccominterfaces. h)
description: Fügt ein Host Laufwerk an das DVD-Laufwerk innerhalb der virtuellen Maschine an.
ms.assetid: 68e658ba-470c-452c-8124-5bb2ec81911b
keywords:
- AttachHostDrive-Methode Virtual PC
- AttachHostDrive-Methode Virtual PC, ivmdvddrive-Schnittstelle
- Ivmdvddrive Interface Virtual PC, AttachHostDrive-Methode
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012afcdc0b88aa5b77f1d85cc5becff1e70853f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342876"
---
# <a name="ivmdvddriveattachhostdrive-method"></a><span data-ttu-id="cae8f-106">Ivmdvddrive:: AttachHostDrive-Methode</span><span class="sxs-lookup"><span data-stu-id="cae8f-106">IVMDVDDrive::AttachHostDrive method</span></span>

<span data-ttu-id="cae8f-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cae8f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cae8f-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cae8f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cae8f-109">Fügt ein Host Laufwerk an das DVD-Laufwerk innerhalb der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="cae8f-109">Attaches a host drive to the DVD drive within the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae8f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="cae8f-110">Syntax</span></span>


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="cae8f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cae8f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cae8f-112">Laufwerk *Etter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cae8f-112">*driveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cae8f-113">Der Buchstabe des Host Laufwerks, das angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cae8f-113">The letter of the host drive that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cae8f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cae8f-114">Return value</span></span>

<span data-ttu-id="cae8f-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cae8f-115">This method can return one of these values.</span></span>



| <span data-ttu-id="cae8f-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="cae8f-116">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="cae8f-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cae8f-117">Description</span></span>                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cae8f-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cae8f-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="cae8f-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="cae8f-119">The operation was successful.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="cae8f-120"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="cae8f-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>         | <span data-ttu-id="cae8f-121">Es wurde kein Laufwerk Buchstabe angegeben, oder der angegebene Laufwerk Buchstabe ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="cae8f-121">No drive letter was specified, or the specified drive letter is invalid.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="cae8f-122"><dt>**E \_**</dt> <dt>0x80004005</dt> fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="cae8f-122"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>               | <span data-ttu-id="cae8f-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="cae8f-123">An unexpected error has occurred.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="cae8f-124"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="cae8f-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="cae8f-125">Der virtuelle Computer wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="cae8f-125">The virtual machine could not be found.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="cae8f-126"><dt>**VM \_ E- \_ Laufwerk \_ in \_ Verwendung**</dt> von <dt>0xa0040727</dt></span><span class="sxs-lookup"><span data-stu-id="cae8f-126"><dt>**VM\_E\_DRIVE\_IN\_USE**</dt> <dt>0xA0040727</dt></span></span> </dl> | <span data-ttu-id="cae8f-127">Ein Host-DVD-Laufwerk oder ISO-Abbild ist bereits an dieses Laufwerk innerhalb des virtuellen Computers angefügt, oder das angegebene Host Laufwerk wird bereits in einer anderen virtuellen Maschine verwendet.</span><span class="sxs-lookup"><span data-stu-id="cae8f-127">A host DVD drive or ISO image is already attached to this drive within the virtual machine, or the specified host drive is already in use within another virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="cae8f-128"><dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="cae8f-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="cae8f-129">Der Busort dieses Laufwerks ist ungültig, oder das Laufwerk scheint kein gültiges DVD-Laufwerk zu sein.</span><span class="sxs-lookup"><span data-stu-id="cae8f-129">The bus location for this drive is invalid, or the drive does not appear to be a valid DVD drive.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="cae8f-130"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cae8f-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="cae8f-131">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="cae8f-131">An unexpected error has occurred.</span></span><br/>                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="cae8f-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cae8f-132">Requirements</span></span>



| <span data-ttu-id="cae8f-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cae8f-133">Requirement</span></span> | <span data-ttu-id="cae8f-134">Wert</span><span class="sxs-lookup"><span data-stu-id="cae8f-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cae8f-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cae8f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cae8f-136">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cae8f-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cae8f-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cae8f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cae8f-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cae8f-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cae8f-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="cae8f-139">End of client support</span></span><br/>    | <span data-ttu-id="cae8f-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cae8f-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cae8f-141">Produkt</span><span class="sxs-lookup"><span data-stu-id="cae8f-141">Product</span></span><br/>                  | <span data-ttu-id="cae8f-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cae8f-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cae8f-143">Header</span><span class="sxs-lookup"><span data-stu-id="cae8f-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="cae8f-144"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cae8f-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cae8f-145">IID</span><span class="sxs-lookup"><span data-stu-id="cae8f-145">IID</span></span><br/>                      | <span data-ttu-id="cae8f-146">IID \_ ivmdvddrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.</span><span class="sxs-lookup"><span data-stu-id="cae8f-146">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="cae8f-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cae8f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae8f-148">**Ivmdvddrive**</span><span class="sxs-lookup"><span data-stu-id="cae8f-148">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

