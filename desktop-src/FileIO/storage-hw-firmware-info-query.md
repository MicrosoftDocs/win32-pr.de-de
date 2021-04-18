---
description: Diese Struktur enthält Informationen zur Gerätefirmware.
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: STORAGE_HW_FIRMWARE_INFO_QUERY Struktur (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO_QUERY
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: c5c4294a733a57a6735691a134f997189736def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358907"
---
# <a name="storage_hw_firmware_info_query-structure"></a><span data-ttu-id="40eda-103">\_ \_ \_ \_ Abfrage Struktur der Speicher-HW-Firmware</span><span class="sxs-lookup"><span data-stu-id="40eda-103">STORAGE\_HW\_FIRMWARE\_INFO\_QUERY structure</span></span>

<span data-ttu-id="40eda-104">Diese Struktur enthält Informationen zur Gerätefirmware.</span><span class="sxs-lookup"><span data-stu-id="40eda-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="40eda-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="40eda-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a><span data-ttu-id="40eda-106">Member</span><span class="sxs-lookup"><span data-stu-id="40eda-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="40eda-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="40eda-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="40eda-108">Die Version dieser-Struktur.</span><span class="sxs-lookup"><span data-stu-id="40eda-108">The version of this structure.</span></span> <span data-ttu-id="40eda-109">Dieser Wert sollte auf sizeof (Speicher \_ HW \_ Firmware \_ Info \_ Query) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="40eda-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO\_QUERY)</span></span>

</dd> <dt>

<span data-ttu-id="40eda-110">**Größe**</span><span class="sxs-lookup"><span data-stu-id="40eda-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="40eda-111">Die Größe dieser-Struktur als Puffer.</span><span class="sxs-lookup"><span data-stu-id="40eda-111">The size of this structure as a buffer.</span></span>

</dd> <dt>

<span data-ttu-id="40eda-112">**Flags**</span><span class="sxs-lookup"><span data-stu-id="40eda-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="40eda-113">Die der Abfrage zugeordneten Flags.</span><span class="sxs-lookup"><span data-stu-id="40eda-113">The flags associated with the query.</span></span> <span data-ttu-id="40eda-114">Im folgenden finden Sie Flags, die in diesem Member festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="40eda-114">The following are flags that can be set in this member.</span></span>



| <span data-ttu-id="40eda-115">Flag</span><span class="sxs-lookup"><span data-stu-id="40eda-115">Flag</span></span>                                             | <span data-ttu-id="40eda-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40eda-116">Description</span></span>                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40eda-117">speicherhw-firmwareanforderungs- \_ \_ \_ \_ Flag \_ Controller</span><span class="sxs-lookup"><span data-stu-id="40eda-117">STORAGE\_HW\_FIRMWARE\_REQUEST\_FLAG\_CONTROLLER</span></span> | <span data-ttu-id="40eda-118">Gibt an, dass das Ziel der Anforderung nicht das Hand-Objekt selbst ist.</span><span class="sxs-lookup"><span data-stu-id="40eda-118">Indicates that the target of the request other than the device hand/object itself.</span></span> |



 

</dd> <dt>

<span data-ttu-id="40eda-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="40eda-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="40eda-120">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="40eda-120">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40eda-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40eda-121">Requirements</span></span>



| <span data-ttu-id="40eda-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40eda-122">Requirement</span></span> | <span data-ttu-id="40eda-123">Wert</span><span class="sxs-lookup"><span data-stu-id="40eda-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40eda-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40eda-124">Minimum supported client</span></span><br/> | <span data-ttu-id="40eda-125">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40eda-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="40eda-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40eda-126">Minimum supported server</span></span><br/> | <span data-ttu-id="40eda-127">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40eda-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="40eda-128">Header</span><span class="sxs-lookup"><span data-stu-id="40eda-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="40eda-129"><dt>Winioctl. h. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40eda-129"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40eda-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40eda-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40eda-131">**IOCTL- \_ Speicher \_ Firmware \_ aktivieren**</span><span class="sxs-lookup"><span data-stu-id="40eda-131">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="40eda-132">**Aktivieren der Speicher- \_ HW- \_ Firmware \_**</span><span class="sxs-lookup"><span data-stu-id="40eda-132">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="40eda-133">**Download der IOCTL- \_ Speicher \_ Firmware \_**</span><span class="sxs-lookup"><span data-stu-id="40eda-133">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="40eda-134">**speicherhw- \_ \_ Firmwaredownload \_**</span><span class="sxs-lookup"><span data-stu-id="40eda-134">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="40eda-135">**IOCTL- \_ Speicher \_ Firmware \_ get \_ Info**</span><span class="sxs-lookup"><span data-stu-id="40eda-135">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="40eda-136">**Firmware-Informationen zur Speicher- \_ HW \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40eda-136">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="40eda-137">**\_Informationen zum \_ Firmware- \_ Slot \_ für Speicher HW**</span><span class="sxs-lookup"><span data-stu-id="40eda-137">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




