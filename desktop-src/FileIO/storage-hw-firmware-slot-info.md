---
description: Diese Struktur enthält Informationen zu einem Slot auf einem Gerät.
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
title: STORAGE_HW_FIRMWARE_SLOT_INFO Struktur (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_SLOT_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: afb38e3dc866f31b6ada6797dcb611bce1ac81a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348815"
---
# <a name="storage_hw_firmware_slot_info-structure"></a><span data-ttu-id="4a510-103">Informationsstruktur des Speicher-HW- \_ \_ Firmware- \_ Slots \_</span><span class="sxs-lookup"><span data-stu-id="4a510-103">STORAGE\_HW\_FIRMWARE\_SLOT\_INFO structure</span></span>

<span data-ttu-id="4a510-104">Diese Struktur enthält Informationen zu einem Slot auf einem Gerät.</span><span class="sxs-lookup"><span data-stu-id="4a510-104">This structure contains information about a slot on a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a510-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a510-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_SLOT_INFO {
  DWORD Version;
  DWORD Size;
  BYTE  SlotNumber;
  BYTE  ReadOnly  :1;
  BYTE  Reserved0  :7;
  BYTE  Reserved1[6];
  BYTE  Revision[STORAGE_HW_FIRMWARE_REVISION_LENGTH];
} STORAGE_HW_FIRMWARE_SLOT_INFO, *PSTORAGE_HW_FIRMWARE_SLOT_INFO;
```



## <a name="members"></a><span data-ttu-id="4a510-106">Member</span><span class="sxs-lookup"><span data-stu-id="4a510-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4a510-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="4a510-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="4a510-108">Die Version dieser-Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a510-108">The version of this structure.</span></span> <span data-ttu-id="4a510-109">Dieser Wert sollte auf sizeof festgelegt werden ( \_ Informationen zum firmwareinsloterinfo für Speicher \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4a510-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_SLOT\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="4a510-110">**Größe**</span><span class="sxs-lookup"><span data-stu-id="4a510-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="4a510-111">Die Größe dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a510-111">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="4a510-112">**SlotNumber**</span><span class="sxs-lookup"><span data-stu-id="4a510-112">**SlotNumber**</span></span>
</dt> <dd>

<span data-ttu-id="4a510-113">Die Slotnummer dieses Slots.</span><span class="sxs-lookup"><span data-stu-id="4a510-113">The slot number of this slot.</span></span>

</dd> <dt>

<span data-ttu-id="4a510-114">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="4a510-114">**ReadOnly**</span></span>
</dt> <dd>

<span data-ttu-id="4a510-115">Gibt an, ob dieser Slot schreibgeschützt ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="4a510-115">Indicates whether this slot is read-only or not.</span></span>

</dd> <dt>

<span data-ttu-id="4a510-116">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="4a510-116">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="4a510-117">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="4a510-117">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="4a510-118">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="4a510-118">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="4a510-119">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="4a510-119">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="4a510-120">**Novel**</span><span class="sxs-lookup"><span data-stu-id="4a510-120">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="4a510-121">Die Revision der Firmware in diesem Slot.</span><span class="sxs-lookup"><span data-stu-id="4a510-121">The revision of the firmware on this slot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a510-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a510-122">Requirements</span></span>



| <span data-ttu-id="4a510-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a510-123">Requirement</span></span> | <span data-ttu-id="4a510-124">Wert</span><span class="sxs-lookup"><span data-stu-id="4a510-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a510-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a510-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4a510-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a510-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="4a510-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a510-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4a510-128">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a510-128">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="4a510-129">Header</span><span class="sxs-lookup"><span data-stu-id="4a510-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a510-130"><dt>Winioctl. h. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a510-130"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a510-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a510-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a510-132">**IOCTL- \_ Speicher \_ Firmware \_ aktivieren**</span><span class="sxs-lookup"><span data-stu-id="4a510-132">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="4a510-133">**Aktivieren der Speicher- \_ HW- \_ Firmware \_**</span><span class="sxs-lookup"><span data-stu-id="4a510-133">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="4a510-134">**Download der IOCTL- \_ Speicher \_ Firmware \_**</span><span class="sxs-lookup"><span data-stu-id="4a510-134">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="4a510-135">**speicherhw- \_ \_ Firmwaredownload \_**</span><span class="sxs-lookup"><span data-stu-id="4a510-135">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="4a510-136">**IOCTL- \_ Speicher \_ Firmware \_ get \_ Info**</span><span class="sxs-lookup"><span data-stu-id="4a510-136">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="4a510-137">**Firmware-Informationen zur Speicher- \_ HW \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4a510-137">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="4a510-138">**\_Firmware- \_ \_ Informations \_ Abfrage für Speicher HW**</span><span class="sxs-lookup"><span data-stu-id="4a510-138">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




