---
title: Ivmharddisk sizone Guest-Eigenschaft (vpccominterfaces. h)
description: Ruft die Größe der virtuellen Festplatte im Gast Betriebssystem ab.
ms.assetid: 895598db-cd54-414c-8783-13102cfbd453
keywords:
- Sizone Guest-Eigenschaft virtueller PC
- Sizeingeguest-Eigenschaft Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, sizone Guest (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeInGuest
- IVMHardDisk.get_SizeInGuest
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace142bf7c0dc612de47c8b2cb043ce24d6e9e9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104918"
---
# <a name="ivmharddisksizeinguest-property"></a><span data-ttu-id="c2c87-106">Ivmharddisk:: sizone Guest-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c2c87-106">IVMHardDisk::SizeInGuest property</span></span>

<span data-ttu-id="c2c87-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c2c87-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c2c87-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c2c87-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c2c87-109">Ruft die Größe der virtuellen Festplatte im Gast Betriebssystem ab.</span><span class="sxs-lookup"><span data-stu-id="c2c87-109">Retrieves the size of the virtual hard disk in the guest operating system.</span></span>

<span data-ttu-id="c2c87-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c2c87-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2c87-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2c87-111">Syntax</span></span>


```C++
HRESULT get_SizeInGuest(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a><span data-ttu-id="c2c87-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c2c87-112">Property value</span></span>

<span data-ttu-id="c2c87-113">Die Größe (in Bytes) des Festplatten Abbilds.</span><span class="sxs-lookup"><span data-stu-id="c2c87-113">The size, in bytes, of the hard disk image.</span></span> <span data-ttu-id="c2c87-114">Dieser Wert ist eine **Variante** vom Typ VT \_ Decimal.</span><span class="sxs-lookup"><span data-stu-id="c2c87-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c2c87-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c2c87-115">Error codes</span></span>



| <span data-ttu-id="c2c87-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="c2c87-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="c2c87-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c2c87-117">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2c87-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c2c87-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="c2c87-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2c87-119">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="c2c87-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c2c87-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="c2c87-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c2c87-121">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="c2c87-122"><dt>HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="c2c87-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="c2c87-123">Die aktuelle Datei der virtuellen Festplatte konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c2c87-123">The current virtual hard disk file could not be found.</span></span><br/>                         |
| <dl> <span data-ttu-id="c2c87-124"><dt>VM \_ E \_ HD- \_ Abbild \_ Öffnen \_ fehlschlagen</dt> <dt>0xa004067c</dt></span><span class="sxs-lookup"><span data-stu-id="c2c87-124"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="c2c87-125">Fehler beim Öffnen der aktuellen Festplatten Abbild Datei.</span><span class="sxs-lookup"><span data-stu-id="c2c87-125">An error occurred while attempting to open the current hard disk image file.</span></span><br/>   |
| <dl> <span data-ttu-id="c2c87-126"><dt>VM \_ E \_ HD- \_ Abbild \_ Zugriff</dt> <dt>0xa0040681</dt></span><span class="sxs-lookup"><span data-stu-id="c2c87-126"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="c2c87-127">Fehler beim Zugriff auf die aktuelle Festplatten Abbild Datei.</span><span class="sxs-lookup"><span data-stu-id="c2c87-127">An error occurred while attempting to access the current hard disk image file.</span></span><br/> |
| <dl> <span data-ttu-id="c2c87-128"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c2c87-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="c2c87-129">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c2c87-129">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="c2c87-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2c87-130">Requirements</span></span>



| <span data-ttu-id="c2c87-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2c87-131">Requirement</span></span> | <span data-ttu-id="c2c87-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c2c87-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c87-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2c87-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c2c87-134">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2c87-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c2c87-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2c87-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c2c87-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c2c87-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c2c87-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c2c87-137">End of client support</span></span><br/>    | <span data-ttu-id="c2c87-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c2c87-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c2c87-139">Produkt</span><span class="sxs-lookup"><span data-stu-id="c2c87-139">Product</span></span><br/>                  | <span data-ttu-id="c2c87-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c2c87-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c2c87-141">Header</span><span class="sxs-lookup"><span data-stu-id="c2c87-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2c87-142"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2c87-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c2c87-143">IID</span><span class="sxs-lookup"><span data-stu-id="c2c87-143">IID</span></span><br/>                      | <span data-ttu-id="c2c87-144">IID \_ ivmharddisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.</span><span class="sxs-lookup"><span data-stu-id="c2c87-144">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="c2c87-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2c87-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2c87-146">**Ivmharddisk**</span><span class="sxs-lookup"><span data-stu-id="c2c87-146">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

