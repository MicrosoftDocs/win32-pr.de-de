---
title: Ivmfloppydrive AttachHostDrive-Methode (vpccominterfaces. h)
description: Fügt ein physisches Laufwerk auf dem Host an das Diskettenlaufwerk auf dem virtuellen Computer an.
ms.assetid: 9be84e06-e38a-419a-be50-dddd0cc6d2dd
keywords:
- AttachHostDrive-Methode Virtual PC
- AttachHostDrive-Methode Virtual PC, ivmfloppydrive-Schnittstelle
- Ivmfloppydrive Interface Virtual PC, AttachHostDrive-Methode
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a21785e3e1e4ec77146f048ab4cce018de9d8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040743"
---
# <a name="ivmfloppydriveattachhostdrive-method"></a><span data-ttu-id="52dd4-106">Ivmfloppydrive:: AttachHostDrive-Methode</span><span class="sxs-lookup"><span data-stu-id="52dd4-106">IVMFloppyDrive::AttachHostDrive method</span></span>

<span data-ttu-id="52dd4-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="52dd4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="52dd4-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="52dd4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="52dd4-109">Fügt ein physisches Laufwerk auf dem Host an das Diskettenlaufwerk auf dem virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="52dd4-109">Attaches a physical drive on the host to the floppy drive in the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="52dd4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="52dd4-110">Syntax</span></span>


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="52dd4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="52dd4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52dd4-112">Laufwerk *Etter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52dd4-112">*driveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52dd4-113">Der Laufwerk Buchstabe des physischen Disketten Laufwerks auf dem Host Computer, an das angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="52dd4-113">The drive letter of the physical floppy drive on the host machine to is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52dd4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52dd4-114">Return value</span></span>

<span data-ttu-id="52dd4-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="52dd4-115">This method can return one of these values.</span></span>



| <span data-ttu-id="52dd4-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="52dd4-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="52dd4-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52dd4-117">Description</span></span>                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="52dd4-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="52dd4-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="52dd4-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="52dd4-119">The operation was successful.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="52dd4-120"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="52dd4-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="52dd4-121">Der *DriveLetter* -Parameter ist **null**, ist kein gültiges Diskettenlaufwerk, oder der angegebene Pfad ist leer.</span><span class="sxs-lookup"><span data-stu-id="52dd4-121">The *driveLetter* parameter is **NULL**, is not a valid floppy drive, or the given path is empty.</span></span><br/> |
| <dl> <span data-ttu-id="52dd4-122"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="52dd4-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="52dd4-123">Die Konfiguration für diesen virtuellen Computer ist ungültig oder wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="52dd4-123">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/>                       |
| <dl> <span data-ttu-id="52dd4-124"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="52dd4-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="52dd4-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="52dd4-125">An unexpected error has occurred.</span></span><br/>                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="52dd4-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52dd4-126">Requirements</span></span>



| <span data-ttu-id="52dd4-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52dd4-127">Requirement</span></span> | <span data-ttu-id="52dd4-128">Wert</span><span class="sxs-lookup"><span data-stu-id="52dd4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="52dd4-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52dd4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="52dd4-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52dd4-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52dd4-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52dd4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="52dd4-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="52dd4-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="52dd4-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="52dd4-133">End of client support</span></span><br/>    | <span data-ttu-id="52dd4-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52dd4-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="52dd4-135">Produkt</span><span class="sxs-lookup"><span data-stu-id="52dd4-135">Product</span></span><br/>                  | <span data-ttu-id="52dd4-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="52dd4-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="52dd4-137">Header</span><span class="sxs-lookup"><span data-stu-id="52dd4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="52dd4-138"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="52dd4-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="52dd4-139">IID</span><span class="sxs-lookup"><span data-stu-id="52dd4-139">IID</span></span><br/>                      | <span data-ttu-id="52dd4-140">IID \_ ivmfloppydrive ist als 661abee6-112a-4ed9-BABF -3c874969s10e definiert.</span><span class="sxs-lookup"><span data-stu-id="52dd4-140">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="52dd4-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52dd4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52dd4-142">**Ivmfloppydrive**</span><span class="sxs-lookup"><span data-stu-id="52dd4-142">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

