---
description: 'STORAGE_HW_FIRMWARE_INFO_QUERY struktur: Diese Struktur enthält Informationen zur Gerätefirmware.'
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: STORAGE_HW_FIRMWARE_INFO_QUERY -Struktur (Winioctl.h)
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
ms.openlocfilehash: ffda37d918406a696a29a9bf2903424523c3b830
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119398"
---
# <a name="storage_hw_firmware_info_query-structure"></a><span data-ttu-id="a655e-103">ABFRAGEstruktur \_ der SPEICHER-HW-FIRMWAREINFO \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a655e-103">STORAGE\_HW\_FIRMWARE\_INFO\_QUERY structure</span></span>

<span data-ttu-id="a655e-104">Diese Struktur enthält Informationen zur Gerätefirmware.</span><span class="sxs-lookup"><span data-stu-id="a655e-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="a655e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a655e-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a><span data-ttu-id="a655e-106">Member</span><span class="sxs-lookup"><span data-stu-id="a655e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a655e-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="a655e-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="a655e-108">Die Version dieser -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a655e-108">The version of this structure.</span></span> <span data-ttu-id="a655e-109">Dies sollte auf sizeof (STORAGE \_ HW \_ FIRMWARE INFO \_ QUERY) festgelegt \_ werden.</span><span class="sxs-lookup"><span data-stu-id="a655e-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO\_QUERY)</span></span>

</dd> <dt>

<span data-ttu-id="a655e-110">**Größe**</span><span class="sxs-lookup"><span data-stu-id="a655e-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="a655e-111">Die Größe dieser Struktur als Puffer.</span><span class="sxs-lookup"><span data-stu-id="a655e-111">The size of this structure as a buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a655e-112">**Flags**</span><span class="sxs-lookup"><span data-stu-id="a655e-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="a655e-113">Die der Abfrage zugeordneten Flags.</span><span class="sxs-lookup"><span data-stu-id="a655e-113">The flags associated with the query.</span></span> <span data-ttu-id="a655e-114">Im Folgenden finden Sie Flags, die in diesem Member festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="a655e-114">The following are flags that can be set in this member.</span></span>



| <span data-ttu-id="a655e-115">Flag</span><span class="sxs-lookup"><span data-stu-id="a655e-115">Flag</span></span>                                             | <span data-ttu-id="a655e-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a655e-116">Description</span></span>                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a655e-117">STORAGE \_ HW \_ FIRMWARE \_ REQUEST \_ FLAG \_ CONTROLLER</span><span class="sxs-lookup"><span data-stu-id="a655e-117">STORAGE\_HW\_FIRMWARE\_REQUEST\_FLAG\_CONTROLLER</span></span> | <span data-ttu-id="a655e-118">Gibt an, dass das Ziel der Anforderung nicht die Hand/das Objekt des Geräts selbst ist.</span><span class="sxs-lookup"><span data-stu-id="a655e-118">Indicates that the target of the request other than the device hand/object itself.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a655e-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="a655e-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="a655e-120">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="a655e-120">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a655e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a655e-121">Requirements</span></span>



| <span data-ttu-id="a655e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a655e-122">Requirement</span></span> | <span data-ttu-id="a655e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a655e-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a655e-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a655e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a655e-125">Windows 10 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a655e-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="a655e-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a655e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a655e-127">Nur Windows Server \[ 2016-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a655e-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="a655e-128">Header</span><span class="sxs-lookup"><span data-stu-id="a655e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a655e-129"><dt>Winioctl.h.h (einschließlich Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a655e-129"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a655e-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a655e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a655e-131">**IOCTL \_ STORAGE \_ FIRMWARE \_ ACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="a655e-131">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="a655e-132">**STORAGE \_ HW \_ FIRMWARE \_ ACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="a655e-132">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="a655e-133">**HERUNTERLADEN DER \_ \_ IOCTL-SPEICHERFIRMWARE \_**</span><span class="sxs-lookup"><span data-stu-id="a655e-133">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="a655e-134">**DOWNLOAD DER \_ SPEICHER-HW-FIRMWARE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a655e-134">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="a655e-135">**\_IOCTL-SPEICHERFIRMWARE \_ \_ – \_ GET-INFORMATIONEN**</span><span class="sxs-lookup"><span data-stu-id="a655e-135">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="a655e-136">**\_ \_ SPEICHER-HW-FIRMWAREINFORMATIONEN \_**</span><span class="sxs-lookup"><span data-stu-id="a655e-136">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="a655e-137">**INFORMATIONEN ZUM \_ SPEICHER-HW-FIRMWARESLOT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a655e-137">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




