---
title: Ivmdvddrive-Anlage Eigenschaft (vpccominterfaces. h)
description: Ruft den Medientyp ab, der mit dem DVD-Laufwerk innerhalb des virtuellen Computers verbunden ist.
ms.assetid: 7ae1714d-e5e9-4f6a-85a6-c0b3c4d21820
keywords:
- Anlage Eigenschaft virtueller PC
- Anlage Eigenschaft Virtual PC, ivmdvddrive-Schnittstelle
- Ivmdvddrive Interface Virtual PC, Anlage (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMDVDDrive.Attachment
- IVMDVDDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5c7801e11534249da899797b73b632a7eda307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859084"
---
# <a name="ivmdvddriveattachment-property"></a><span data-ttu-id="30281-106">Ivmdvddrive:: Attachment-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="30281-106">IVMDVDDrive::Attachment property</span></span>

<span data-ttu-id="30281-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="30281-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="30281-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="30281-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="30281-109">Ruft den Medientyp ab, der mit dem DVD-Laufwerk innerhalb des virtuellen Computers verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="30281-109">Retrieves the type of media attached to the DVD drive within the virtual machine.</span></span>

<span data-ttu-id="30281-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="30281-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="30281-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="30281-111">Syntax</span></span>


```C++
HRESULT get_Attachment(
  [out, retval] VMDVDDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a><span data-ttu-id="30281-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="30281-112">Property value</span></span>

<span data-ttu-id="30281-113">Der angefügte Medientyp.</span><span class="sxs-lookup"><span data-stu-id="30281-113">The attached media type.</span></span> <span data-ttu-id="30281-114">Eine Liste der Werte finden Sie unter [**vmdvddriveattachmenttype**](vmdvddriveattachmenttype.md).</span><span class="sxs-lookup"><span data-stu-id="30281-114">For a list of values, see [**VMDVDDriveAttachmentType**](vmdvddriveattachmenttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="30281-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="30281-115">Error codes</span></span>



| <span data-ttu-id="30281-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="30281-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="30281-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="30281-117">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="30281-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="30281-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="30281-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="30281-119">The operation was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="30281-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="30281-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="30281-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="30281-121">The parameter is **NULL**.</span></span><br/>                  |
| <dl> <span data-ttu-id="30281-122"><dt>E \_ </dt> <dt>0x80004005</dt> fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="30281-122"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>               | <span data-ttu-id="30281-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="30281-123">An unexpected error has occurred.</span></span><br/>           |
| <dl> <span data-ttu-id="30281-124"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="30281-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="30281-125">Der virtuelle Computer wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="30281-125">The virtual machine could not be found.</span></span><br/>     |
| <dl> <span data-ttu-id="30281-126"><dt>VM \_ E \_ Laufwerk \_ ungültige</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="30281-126"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="30281-127">Der Busstandort für dieses Laufwerk ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="30281-127">The bus location for this drive is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="30281-128"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="30281-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="30281-129">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="30281-129">An unexpected error has occurred.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="30281-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30281-130">Requirements</span></span>



| <span data-ttu-id="30281-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30281-131">Requirement</span></span> | <span data-ttu-id="30281-132">Wert</span><span class="sxs-lookup"><span data-stu-id="30281-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="30281-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30281-133">Minimum supported client</span></span><br/> | <span data-ttu-id="30281-134">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30281-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="30281-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30281-135">Minimum supported server</span></span><br/> | <span data-ttu-id="30281-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="30281-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="30281-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="30281-137">End of client support</span></span><br/>    | <span data-ttu-id="30281-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="30281-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="30281-139">Produkt</span><span class="sxs-lookup"><span data-stu-id="30281-139">Product</span></span><br/>                  | <span data-ttu-id="30281-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="30281-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="30281-141">Header</span><span class="sxs-lookup"><span data-stu-id="30281-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="30281-142"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="30281-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="30281-143">IID</span><span class="sxs-lookup"><span data-stu-id="30281-143">IID</span></span><br/>                      | <span data-ttu-id="30281-144">IID \_ ivmdvddrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.</span><span class="sxs-lookup"><span data-stu-id="30281-144">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="30281-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30281-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30281-146">**Ivmdvddrive**</span><span class="sxs-lookup"><span data-stu-id="30281-146">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

