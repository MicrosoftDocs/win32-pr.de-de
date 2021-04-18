---
title: Ivmfloppydrive-Anlage Eigenschaft (vpccominterfaces. h)
description: Ruft den Medientyp ab, der mit dem Diskettenlaufwerk auf dem virtuellen Computer verbunden ist.
ms.assetid: 0b7e43ac-de56-4c4b-82e6-75877aea06f2
keywords:
- Anlage Eigenschaft virtueller PC
- Anlage Eigenschaft Virtual PC, ivmfloppydrive-Schnittstelle
- Ivmfloppydrive Interface Virtual PC, Anlage (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMFloppyDrive.Attachment
- IVMFloppyDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44814148baf27672f30b8e3c5015d841aaaba4b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340339"
---
# <a name="ivmfloppydriveattachment-property"></a><span data-ttu-id="f2c92-106">Ivmfloppydrive:: Attachment-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f2c92-106">IVMFloppyDrive::Attachment property</span></span>

<span data-ttu-id="f2c92-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f2c92-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f2c92-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f2c92-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f2c92-109">Ruft den Medientyp ab, der an das Diskettenlaufwerk im virtuellen Computer (VM) angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="f2c92-109">Retrieves the type of media attached to the floppy drive in the virtual machine (VM).</span></span>

<span data-ttu-id="f2c92-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f2c92-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2c92-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2c92-111">Syntax</span></span>


```C++
HRESULT get_Attachment(
  [out, retval] VMFloppyDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a><span data-ttu-id="f2c92-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f2c92-112">Property value</span></span>

<span data-ttu-id="f2c92-113">Der Medientyp.</span><span class="sxs-lookup"><span data-stu-id="f2c92-113">The type of media.</span></span> <span data-ttu-id="f2c92-114">Eine Liste der Werte finden Sie unter [**vmfloppydriveattachmenttype**](vmfloppydriveattachmenttype.md).</span><span class="sxs-lookup"><span data-stu-id="f2c92-114">For a list of values, see [**VMFloppyDriveAttachmentType**](vmfloppydriveattachmenttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="f2c92-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f2c92-115">Error codes</span></span>



| <span data-ttu-id="f2c92-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="f2c92-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f2c92-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f2c92-117">Meaning</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2c92-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f2c92-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f2c92-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2c92-119">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="f2c92-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f2c92-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f2c92-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="f2c92-121">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f2c92-122"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="f2c92-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="f2c92-123">Die Konfiguration für diese VM ist ungültig oder wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="f2c92-123">The configuration for this VM is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="f2c92-124"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f2c92-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f2c92-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f2c92-125">An unexpected error has occurred.</span></span><br/>                              |



## <a name="requirements"></a><span data-ttu-id="f2c92-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2c92-126">Requirements</span></span>



| <span data-ttu-id="f2c92-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2c92-127">Requirement</span></span> | <span data-ttu-id="f2c92-128">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c92-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c92-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2c92-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f2c92-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2c92-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2c92-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2c92-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f2c92-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f2c92-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f2c92-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f2c92-133">End of client support</span></span><br/>    | <span data-ttu-id="f2c92-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f2c92-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f2c92-135">Produkt</span><span class="sxs-lookup"><span data-stu-id="f2c92-135">Product</span></span><br/>                  | <span data-ttu-id="f2c92-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f2c92-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f2c92-137">Header</span><span class="sxs-lookup"><span data-stu-id="f2c92-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2c92-138"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2c92-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f2c92-139">IID</span><span class="sxs-lookup"><span data-stu-id="f2c92-139">IID</span></span><br/>                      | <span data-ttu-id="f2c92-140">IID \_ ivmfloppydrive ist als 661abee6-112a-4ed9-BABF -3c874969s10e definiert.</span><span class="sxs-lookup"><span data-stu-id="f2c92-140">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f2c92-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2c92-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2c92-142">**Ivmfloppydrive**</span><span class="sxs-lookup"><span data-stu-id="f2c92-142">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

