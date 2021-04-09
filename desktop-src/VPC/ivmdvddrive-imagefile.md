---
title: Eigenschaften von ivmdvddrive ImageFile (vpccominterfaces. h)
description: Ruft den vollständigen Pfad der Bilddatei ab, die für dieses Gerät festgelegt ist.
ms.assetid: e7910d37-d3a5-4291-b374-aaa67db50f1b
keywords:
- ImageFile-Eigenschaft virtueller PC
- ImageFile-Eigenschaft Virtual PC, ivmdvddrive-Schnittstelle
- Ivmdvddrive Interface Virtual PC, ImageFile-Eigenschaft
topic_type:
- apiref
api_name:
- IVMDVDDrive.ImageFile
- IVMDVDDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c71ed5328e41a72c9896147c6dcd824b2bd2ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859210"
---
# <a name="ivmdvddriveimagefile-property"></a><span data-ttu-id="7b891-106">Ivmdvddrive:: ImageFile (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7b891-106">IVMDVDDrive::ImageFile property</span></span>

<span data-ttu-id="7b891-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7b891-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7b891-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7b891-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7b891-109">Ruft den vollständigen Pfad der Bilddatei ab, die für dieses Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7b891-109">Retrieves the full path of the image file set for this device.</span></span>

<span data-ttu-id="7b891-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7b891-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b891-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b891-111">Syntax</span></span>


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imagePath
);
```



## <a name="property-value"></a><span data-ttu-id="7b891-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7b891-112">Property value</span></span>

<span data-ttu-id="7b891-113">Der vollständige Pfad zur Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="7b891-113">The full path to the image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7b891-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7b891-114">Error codes</span></span>



| <span data-ttu-id="7b891-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="7b891-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="7b891-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7b891-116">Meaning</span></span>                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7b891-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7b891-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="7b891-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b891-118">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="7b891-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7b891-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="7b891-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="7b891-120">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="7b891-121"><dt>E \_ </dt> <dt>0x80004005</dt> fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="7b891-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="7b891-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7b891-122">An unexpected error has occurred.</span></span><br/>                              |
| <dl> <span data-ttu-id="7b891-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="7b891-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="7b891-124">Der virtuelle Computer wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="7b891-124">The virtual machine could not be found.</span></span><br/>                        |
| <dl> <span data-ttu-id="7b891-125"><dt>VM \_ E \_ Laufwerk \_ ungültige</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="7b891-125"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="7b891-126">Der Busstandort für dieses Laufwerk ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7b891-126">The bus location for this drive is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="7b891-127"><dt>VM \_ E \_ Medien \_ falscher \_ Typ</dt> <dt>0xa00400728</dt></span><span class="sxs-lookup"><span data-stu-id="7b891-127"><dt>VM\_E\_MEDIA\_WRONG\_TYPE</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="7b891-128">Das von diesem DVD-Laufwerk erfasste Medium ist keine ISO-Abbild Datei.</span><span class="sxs-lookup"><span data-stu-id="7b891-128">The media captured by this DVD drive is not an ISO image file.</span></span><br/> |
| <dl> <span data-ttu-id="7b891-129"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7b891-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="7b891-130">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7b891-130">An unexpected error has occurred.</span></span><br/>                              |



## <a name="requirements"></a><span data-ttu-id="7b891-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b891-131">Requirements</span></span>



| <span data-ttu-id="7b891-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b891-132">Requirement</span></span> | <span data-ttu-id="7b891-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7b891-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b891-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b891-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7b891-135">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b891-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7b891-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b891-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7b891-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7b891-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7b891-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7b891-138">End of client support</span></span><br/>    | <span data-ttu-id="7b891-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7b891-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7b891-140">Produkt</span><span class="sxs-lookup"><span data-stu-id="7b891-140">Product</span></span><br/>                  | <span data-ttu-id="7b891-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7b891-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7b891-142">Header</span><span class="sxs-lookup"><span data-stu-id="7b891-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b891-143"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b891-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7b891-144">IID</span><span class="sxs-lookup"><span data-stu-id="7b891-144">IID</span></span><br/>                      | <span data-ttu-id="7b891-145">IID \_ ivmdvddrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.</span><span class="sxs-lookup"><span data-stu-id="7b891-145">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="7b891-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b891-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b891-147">**Ivmdvddrive**</span><span class="sxs-lookup"><span data-stu-id="7b891-147">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

