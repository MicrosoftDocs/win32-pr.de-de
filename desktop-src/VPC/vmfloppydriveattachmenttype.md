---
title: Vmfloppydriveattachmenttype-Enumeration (vpccominterfaces. h)
description: Gibt an, was an ein Diskettenlaufwerk angefügt ist.
ms.assetid: aba1be92-bd07-4edb-ad62-f8d76dbd19b9
keywords:
- Vmfloppydriveattachmenttype-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMFloppyDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4a291778b2fea8039bf41fc04799a03421342f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956658"
---
# <a name="vmfloppydriveattachmenttype-enumeration"></a><span data-ttu-id="430ec-104">Vmfloppydriveattachmenttype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="430ec-104">VMFloppyDriveAttachmentType enumeration</span></span>

<span data-ttu-id="430ec-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="430ec-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="430ec-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="430ec-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="430ec-107">Gibt an, was an ein Diskettenlaufwerk angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="430ec-107">Specifies what is attached to a floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="430ec-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="430ec-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDrive_None       = 0,
  vmFloppyDrive_Image      = 1,
  vmFloppyDrive_HostDrive  = 2
} VMFloppyDriveAttachmentType;
```



## <a name="constants"></a><span data-ttu-id="430ec-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="430ec-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="430ec-110"><span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**vmfloppydrive \_ None**</span><span class="sxs-lookup"><span data-stu-id="430ec-110"><span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**vmFloppyDrive\_None**</span></span>
</dt> <dd>

<span data-ttu-id="430ec-111">Es ist nichts angefügt.</span><span class="sxs-lookup"><span data-stu-id="430ec-111">There is nothing attached.</span></span>

</dd> <dt>

<span data-ttu-id="430ec-112"><span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**vmfloppydrive- \_ Image**</span><span class="sxs-lookup"><span data-stu-id="430ec-112"><span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**vmFloppyDrive\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="430ec-113">Es ist eine Disketten Bilddatei angefügt.</span><span class="sxs-lookup"><span data-stu-id="430ec-113">There is a floppy disk image file attached.</span></span>

</dd> <dt>

<span data-ttu-id="430ec-114"><span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**vmfloppydrive- \_ Hostlaufwerk**</span><span class="sxs-lookup"><span data-stu-id="430ec-114"><span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**vmFloppyDrive\_HostDrive**</span></span>
</dt> <dd>

<span data-ttu-id="430ec-115">Es ist ein Host Diskettenlaufwerk angefügt.</span><span class="sxs-lookup"><span data-stu-id="430ec-115">There is a host floppy drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="430ec-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="430ec-116">Requirements</span></span>



| <span data-ttu-id="430ec-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="430ec-117">Requirement</span></span> | <span data-ttu-id="430ec-118">Wert</span><span class="sxs-lookup"><span data-stu-id="430ec-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="430ec-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="430ec-119">Minimum supported client</span></span><br/> | <span data-ttu-id="430ec-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="430ec-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="430ec-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="430ec-121">Minimum supported server</span></span><br/> | <span data-ttu-id="430ec-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="430ec-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="430ec-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="430ec-123">End of client support</span></span><br/>    | <span data-ttu-id="430ec-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="430ec-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="430ec-125">Produkt</span><span class="sxs-lookup"><span data-stu-id="430ec-125">Product</span></span><br/>                  | <span data-ttu-id="430ec-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="430ec-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="430ec-127">Header</span><span class="sxs-lookup"><span data-stu-id="430ec-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="430ec-128"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="430ec-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="430ec-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="430ec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="430ec-130">**Ivmfloppydrive:: Attachment**</span><span class="sxs-lookup"><span data-stu-id="430ec-130">**IVMFloppyDrive::Attachment**</span></span>](ivmfloppydrive-attachment.md)
</dt> </dl>

 

