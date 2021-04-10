---
title: Ivmharddisk-Typeigenschaft (vpccominterfaces. h)
description: Der Typ der virtuellen Festplatte.
ms.assetid: a855ed9b-a573-471c-ad98-521c80e9ab8c
keywords:
- Type-Eigenschaft Virtual PC
- Type-Eigenschaft Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, Type-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDisk.Type
- IVMHardDisk.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3757d74de5fc99972be3c7d267b15c56da6bee16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040566"
---
# <a name="ivmharddisktype-property"></a><span data-ttu-id="7b37d-106">Ivmharddisk:: Type (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7b37d-106">IVMHardDisk::Type property</span></span>

<span data-ttu-id="7b37d-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7b37d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7b37d-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7b37d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7b37d-109">Ruft den Typ der virtuellen Festplatte ab.</span><span class="sxs-lookup"><span data-stu-id="7b37d-109">Retrieves the type of the virtual hard disk.</span></span>

<span data-ttu-id="7b37d-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7b37d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b37d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b37d-111">Syntax</span></span>


```C++
HRESULT get_Type(
  [out, retval] VMHardDiskType *type
);
```



## <a name="property-value"></a><span data-ttu-id="7b37d-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7b37d-112">Property value</span></span>

<span data-ttu-id="7b37d-113">Der Typ des aktuellen Festplatten Bilds.</span><span class="sxs-lookup"><span data-stu-id="7b37d-113">The type of the current hard disk image.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7b37d-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7b37d-114">Error codes</span></span>



| <span data-ttu-id="7b37d-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="7b37d-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="7b37d-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7b37d-116">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7b37d-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7b37d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="7b37d-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b37d-118">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="7b37d-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7b37d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="7b37d-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="7b37d-120">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="7b37d-121"><dt>HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="7b37d-121"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="7b37d-122">Die aktuelle Festplatten Abbild Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="7b37d-122">The current hard disk image file could not be found.</span></span><br/>                           |
| <dl> <span data-ttu-id="7b37d-123"><dt>VM \_ E \_ Laufwerk \_ ungültige</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="7b37d-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="7b37d-124">Der Typ des aktuellen Festplatten Abbilds ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7b37d-124">The type of the current hard disk image is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="7b37d-125"><dt>VM \_ E \_ HD- \_ Abbild \_ Öffnen \_ fehlschlagen</dt> <dt>0xa004067c</dt></span><span class="sxs-lookup"><span data-stu-id="7b37d-125"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="7b37d-126">Fehler beim Öffnen der aktuellen Festplatten Abbild Datei.</span><span class="sxs-lookup"><span data-stu-id="7b37d-126">An error occurred while attempting to open the current hard disk image file.</span></span><br/>   |
| <dl> <span data-ttu-id="7b37d-127"><dt>VM \_ E \_ HD- \_ Abbild \_ Zugriff</dt> <dt>0xa0040681</dt></span><span class="sxs-lookup"><span data-stu-id="7b37d-127"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="7b37d-128">Fehler beim Zugriff auf die aktuelle Festplatten Abbild Datei.</span><span class="sxs-lookup"><span data-stu-id="7b37d-128">An error occurred while attempting to access the current hard disk image file.</span></span><br/> |
| <dl> <span data-ttu-id="7b37d-129"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7b37d-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="7b37d-130">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7b37d-130">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="7b37d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b37d-131">Requirements</span></span>



| <span data-ttu-id="7b37d-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b37d-132">Requirement</span></span> | <span data-ttu-id="7b37d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7b37d-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b37d-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b37d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7b37d-135">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b37d-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7b37d-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b37d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7b37d-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7b37d-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7b37d-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7b37d-138">End of client support</span></span><br/>    | <span data-ttu-id="7b37d-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7b37d-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7b37d-140">Produkt</span><span class="sxs-lookup"><span data-stu-id="7b37d-140">Product</span></span><br/>                  | <span data-ttu-id="7b37d-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7b37d-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7b37d-142">Header</span><span class="sxs-lookup"><span data-stu-id="7b37d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b37d-143"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b37d-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7b37d-144">IID</span><span class="sxs-lookup"><span data-stu-id="7b37d-144">IID</span></span><br/>                      | <span data-ttu-id="7b37d-145">IID \_ ivmharddisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.</span><span class="sxs-lookup"><span data-stu-id="7b37d-145">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="7b37d-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b37d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b37d-147">**Ivmharddisk**</span><span class="sxs-lookup"><span data-stu-id="7b37d-147">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

