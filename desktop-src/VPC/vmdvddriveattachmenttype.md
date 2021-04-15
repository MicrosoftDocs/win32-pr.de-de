---
title: Vmdvddriveattachmenttype-Enumeration (vpccominterfaces. h)
description: Gibt an, was an ein DVD-Laufwerk angefügt ist.
ms.assetid: 66f33974-8622-4fa3-b5ac-3fae5a637434
keywords:
- Vmdvddriveattachmenttype-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMDVDDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c5918fd414a5a83a114ebddf5752647e8db83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477394"
---
# <a name="vmdvddriveattachmenttype-enumeration"></a><span data-ttu-id="4fe54-104">Vmdvddriveattachmenttype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="4fe54-104">VMDVDDriveAttachmentType enumeration</span></span>

<span data-ttu-id="4fe54-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4fe54-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4fe54-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4fe54-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4fe54-107">Gibt an, was an ein DVD-Laufwerk angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="4fe54-107">Specifies what is attached to a DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fe54-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fe54-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDVDDrive_None       = 0,
  vmDVDDrive_Image      = 1,
  vmDVDDrive_HostDrive  = 2
} VMDVDDriveAttachmentType;
```



## <a name="constants"></a><span data-ttu-id="4fe54-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="4fe54-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4fe54-110"><span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**vmdvddrive \_ None**</span><span class="sxs-lookup"><span data-stu-id="4fe54-110"><span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**vmDVDDrive\_None**</span></span>
</dt> <dd>

<span data-ttu-id="4fe54-111">Es ist nichts angefügt.</span><span class="sxs-lookup"><span data-stu-id="4fe54-111">There is nothing attached.</span></span>

</dd> <dt>

<span data-ttu-id="4fe54-112"><span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**vmdvddrive- \_ Image**</span><span class="sxs-lookup"><span data-stu-id="4fe54-112"><span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**vmDVDDrive\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="4fe54-113">Eine ISO-Abbild Datei ist angefügt.</span><span class="sxs-lookup"><span data-stu-id="4fe54-113">There is an ISO image file attached.</span></span>

</dd> <dt>

<span data-ttu-id="4fe54-114"><span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**vmdvddrive- \_ Hostlaufwerk**</span><span class="sxs-lookup"><span data-stu-id="4fe54-114"><span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**vmDVDDrive\_HostDrive**</span></span>
</dt> <dd>

<span data-ttu-id="4fe54-115">Es ist ein Host-CD-oder DVD-Laufwerk angefügt.</span><span class="sxs-lookup"><span data-stu-id="4fe54-115">There is a host CD or DVD drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fe54-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fe54-116">Requirements</span></span>



| <span data-ttu-id="4fe54-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fe54-117">Requirement</span></span> | <span data-ttu-id="4fe54-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4fe54-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe54-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fe54-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4fe54-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fe54-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4fe54-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fe54-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4fe54-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4fe54-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4fe54-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4fe54-123">End of client support</span></span><br/>    | <span data-ttu-id="4fe54-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4fe54-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4fe54-125">Produkt</span><span class="sxs-lookup"><span data-stu-id="4fe54-125">Product</span></span><br/>                  | <span data-ttu-id="4fe54-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4fe54-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4fe54-127">Header</span><span class="sxs-lookup"><span data-stu-id="4fe54-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fe54-128"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fe54-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fe54-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fe54-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fe54-130">**Ivmdvddrive:: Attachment**</span><span class="sxs-lookup"><span data-stu-id="4fe54-130">**IVMDVDDrive::Attachment**</span></span>](ivmdvddrive-attachment.md)
</dt> </dl>

 

