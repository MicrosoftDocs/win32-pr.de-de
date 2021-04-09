---
title: "\"Ivmfloppydrive\"-ImageFile-Eigenschaft (\"vpccominterfaces. h\")"
description: Ruft den vollständigen Pfad der Bilddatei ab, an die das Diskettenlaufwerk angefügt ist.
ms.assetid: fc87e438-e5d4-494d-8ac2-27a4312ee81d
keywords:
- ImageFile-Eigenschaft virtueller PC
- ImageFile-Eigenschaft Virtual PC, ivmfloppydrive-Schnittstelle
- Ivmfloppydrive Interface Virtual PC, ImageFile-Eigenschaft
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ImageFile
- IVMFloppyDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa18c4a1da3137613e0106f828f59805e5615384
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040820"
---
# <a name="ivmfloppydriveimagefile-property"></a><span data-ttu-id="776f6-106">Ivmfloppydrive:: ImageFile (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="776f6-106">IVMFloppyDrive::ImageFile property</span></span>

<span data-ttu-id="776f6-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="776f6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="776f6-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="776f6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="776f6-109">Ruft den vollständigen Pfad der Bilddatei ab, an die das Diskettenlaufwerk angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="776f6-109">Retrieves the full path of the image file to which the floppy drive is attached.</span></span>

<span data-ttu-id="776f6-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="776f6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="776f6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="776f6-111">Syntax</span></span>


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imageFile
);
```



## <a name="property-value"></a><span data-ttu-id="776f6-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="776f6-112">Property value</span></span>

<span data-ttu-id="776f6-113">Der vollständige Pfad der Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="776f6-113">The full path of the image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="776f6-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="776f6-114">Error codes</span></span>



| <span data-ttu-id="776f6-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="776f6-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="776f6-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="776f6-116">Meaning</span></span>                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="776f6-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="776f6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="776f6-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="776f6-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="776f6-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="776f6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="776f6-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="776f6-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="776f6-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="776f6-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="776f6-122">Die Konfiguration für diesen virtuellen Computer ist ungültig oder wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="776f6-122">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="776f6-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="776f6-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="776f6-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="776f6-124">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="requirements"></a><span data-ttu-id="776f6-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="776f6-125">Requirements</span></span>



| <span data-ttu-id="776f6-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="776f6-126">Requirement</span></span> | <span data-ttu-id="776f6-127">Wert</span><span class="sxs-lookup"><span data-stu-id="776f6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="776f6-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="776f6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="776f6-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="776f6-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="776f6-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="776f6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="776f6-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="776f6-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="776f6-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="776f6-132">End of client support</span></span><br/>    | <span data-ttu-id="776f6-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="776f6-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="776f6-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="776f6-134">Product</span></span><br/>                  | <span data-ttu-id="776f6-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="776f6-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="776f6-136">Header</span><span class="sxs-lookup"><span data-stu-id="776f6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="776f6-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="776f6-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="776f6-138">IID</span><span class="sxs-lookup"><span data-stu-id="776f6-138">IID</span></span><br/>                      | <span data-ttu-id="776f6-139">IID \_ ivmfloppydrive ist als 661abee6-112a-4ed9-BABF -3c874969s10e definiert.</span><span class="sxs-lookup"><span data-stu-id="776f6-139">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="776f6-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="776f6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="776f6-141">**Ivmfloppydrive**</span><span class="sxs-lookup"><span data-stu-id="776f6-141">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

