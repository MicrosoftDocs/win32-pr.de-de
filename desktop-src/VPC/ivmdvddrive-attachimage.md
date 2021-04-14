---
title: Ivmdvddrive attachimage-Methode (vpccominterfaces. h)
description: Fügt ein ISO-Abbild an das DVD-Laufwerk innerhalb des virtuellen Computers an.
ms.assetid: 08947898-ca3f-41b6-97a3-52dc6977fc6d
keywords:
- Attachimage-Methode Virtual PC
- Attachimage-Methode Virtual PC, ivmdvddrive-Schnittstelle
- Ivmdvddrive Interface Virtual PC, attachimage-Methode
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58204545e21bd7dbf48d21acbc232b9fc5d1e3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392158"
---
# <a name="ivmdvddriveattachimage-method"></a><span data-ttu-id="035d1-106">Ivmdvddrive:: attachimage-Methode</span><span class="sxs-lookup"><span data-stu-id="035d1-106">IVMDVDDrive::AttachImage method</span></span>

<span data-ttu-id="035d1-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="035d1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="035d1-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="035d1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="035d1-109">Fügt ein ISO-Abbild an das DVD-Laufwerk innerhalb des virtuellen Computers (VM) an.</span><span class="sxs-lookup"><span data-stu-id="035d1-109">Attaches an ISO image to the DVD drive within the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="035d1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="035d1-110">Syntax</span></span>


```C++
HRESULT AttachImage(
  [in] BSTR imagePath
);
```



## <a name="parameters"></a><span data-ttu-id="035d1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="035d1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="035d1-112">*ImagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="035d1-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="035d1-113">Der vollständige Pfad zu dem ISO-Abbild, das angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="035d1-113">The full path to the ISO image that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="035d1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="035d1-114">Return value</span></span>

<span data-ttu-id="035d1-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="035d1-115">This method can return one of these values.</span></span>



| <span data-ttu-id="035d1-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="035d1-116">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="035d1-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="035d1-117">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="035d1-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="035d1-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="035d1-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="035d1-119">The operation was successful.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="035d1-120"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="035d1-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>         | <span data-ttu-id="035d1-121">Der *ImagePath* -Parameter ist ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="035d1-121">The *imagePath* parameter is a directory.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="035d1-122"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="035d1-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="035d1-123">Der *ImagePath* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="035d1-123">The *imagePath* parameter is **NULL**.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="035d1-124"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="035d1-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="035d1-125">Die VM wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="035d1-125">The VM could not be found.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="035d1-126"><dt>**VM \_ E- \_ Laufwerk \_ in \_ Verwendung**</dt> von <dt>0xa0040727</dt></span><span class="sxs-lookup"><span data-stu-id="035d1-126"><dt>**VM\_E\_DRIVE\_IN\_USE**</dt> <dt>0xA0040727</dt></span></span> </dl> | <span data-ttu-id="035d1-127">Ein Host-DVD-Laufwerk oder ein ISO-Abbild ist bereits an dieses Laufwerk angefügt.</span><span class="sxs-lookup"><span data-stu-id="035d1-127">A host DVD drive or ISO image is already attached to this drive.</span></span><br/>                                  |
| <dl> <span data-ttu-id="035d1-128"><dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="035d1-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="035d1-129">Der Busort dieses Laufwerks ist ungültig, oder das Laufwerk scheint kein gültiges DVD-Laufwerk zu sein.</span><span class="sxs-lookup"><span data-stu-id="035d1-129">The bus location for this drive is invalid, or the drive does not appear to be a valid DVD drive.</span></span><br/> |
| <dl> <span data-ttu-id="035d1-130"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="035d1-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="035d1-131">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="035d1-131">An unexpected error has occurred.</span></span><br/>                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="035d1-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="035d1-132">Requirements</span></span>



| <span data-ttu-id="035d1-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="035d1-133">Requirement</span></span> | <span data-ttu-id="035d1-134">Wert</span><span class="sxs-lookup"><span data-stu-id="035d1-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="035d1-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="035d1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="035d1-136">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="035d1-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="035d1-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="035d1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="035d1-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="035d1-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="035d1-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="035d1-139">End of client support</span></span><br/>    | <span data-ttu-id="035d1-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="035d1-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="035d1-141">Produkt</span><span class="sxs-lookup"><span data-stu-id="035d1-141">Product</span></span><br/>                  | <span data-ttu-id="035d1-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="035d1-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="035d1-143">Header</span><span class="sxs-lookup"><span data-stu-id="035d1-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="035d1-144"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="035d1-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="035d1-145">IID</span><span class="sxs-lookup"><span data-stu-id="035d1-145">IID</span></span><br/>                      | <span data-ttu-id="035d1-146">IID \_ ivmdvddrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.</span><span class="sxs-lookup"><span data-stu-id="035d1-146">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="035d1-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="035d1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="035d1-148">**Ivmdvddrive**</span><span class="sxs-lookup"><span data-stu-id="035d1-148">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

