---
description: 'STORAGE_HW_FIRMWARE_INFO Struktur: Diese Struktur enthält Informationen zur Gerätefirmware.'
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: STORAGE_HW_FIRMWARE_INFO-Struktur (Winioctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: e7aa3d33f744b00fc742a2862add83149cb265b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090958"
---
# <a name="storage_hw_firmware_info-structure"></a><span data-ttu-id="774ba-103">\_SPEICHER HW \_ FIRMWARE \_ INFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="774ba-103">STORAGE\_HW\_FIRMWARE\_INFO structure</span></span>

<span data-ttu-id="774ba-104">Diese Struktur enthält Informationen zur Gerätefirmware.</span><span class="sxs-lookup"><span data-stu-id="774ba-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="774ba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="774ba-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO {
  DWORD                         Version;
  DWORD                         Size;
  BYTE                          SupportUpgrade  :1;
  BYTE                          Reserved0  :7;
  BYTE                          SlotCount;
  BYTE                          ActiveSlot;
  BYTE                          PendingActivateSlot;
  BOOLEAN                       FirmwareShared;
  BYTE                          Reserved[3];
  DWORD                         ImagePayloadAlignment;
  DWORD                         ImagePayloadMaxSize;
  STORAGE_HW_FIRMWARE_SLOT_INFO Slot[ANYSIZE_ARRAY];
} STORAGE_HW_FIRMWARE_INFO, *PSTORAGE_HW_FIRMWARE_INFO;
```



## <a name="members"></a><span data-ttu-id="774ba-106">Member</span><span class="sxs-lookup"><span data-stu-id="774ba-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="774ba-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="774ba-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="774ba-108">Die Version dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="774ba-108">The version of this structure.</span></span> <span data-ttu-id="774ba-109">Dieser sollte auf sizeof(STORAGE \_ HW FIRMWARE INFO) festgelegt \_ \_ werden.</span><span class="sxs-lookup"><span data-stu-id="774ba-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="774ba-110">**Größe**</span><span class="sxs-lookup"><span data-stu-id="774ba-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="774ba-111">Die Größe dieser Struktur als Puffer einschließlich Slot.</span><span class="sxs-lookup"><span data-stu-id="774ba-111">The size of this structure as a buffer including slot.</span></span>

</dd> <dt>

<span data-ttu-id="774ba-112">**SupportUpgrade**</span><span class="sxs-lookup"><span data-stu-id="774ba-112">**SupportUpgrade**</span></span>
</dt> <dd>

<span data-ttu-id="774ba-113">Gibt an, dass diese Firmware ein Upgrade unterstützt.</span><span class="sxs-lookup"><span data-stu-id="774ba-113">Indicates that this firmware supports an upgrade.</span></span>

</dd> <dt>

<span data-ttu-id="774ba-114">**Reserviert 0**</span><span class="sxs-lookup"><span data-stu-id="774ba-114">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="774ba-115">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="774ba-115">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="774ba-116">**SlotCount**</span><span class="sxs-lookup"><span data-stu-id="774ba-116">**SlotCount**</span></span>
</dt> <dd>

<span data-ttu-id="774ba-117">Die Anzahl der Firmwareslots auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="774ba-117">The number of firmware slots on the device.</span></span> <span data-ttu-id="774ba-118">Dies ist die Dimension des Slot-Arrays.</span><span class="sxs-lookup"><span data-stu-id="774ba-118">This is the dimension of the Slot array.</span></span>

> [!Note]  
> <span data-ttu-id="774ba-119">Einige Geräte können mehr als ein Firmwareimage speichern, wenn sie über mehr als einen Firmwareslot verfügen.</span><span class="sxs-lookup"><span data-stu-id="774ba-119">Some devices can store more than 1 firmware image, if they have more than 1 firmware slot.</span></span>

 

</dd> <dt>

<span data-ttu-id="774ba-120">**ActiveSlot**</span><span class="sxs-lookup"><span data-stu-id="774ba-120">**ActiveSlot**</span></span>
</dt> <dd>

<span data-ttu-id="774ba-121">Der Firmwareslot, der das aktuell aktive/ausgeführte Firmwareimage enthält.</span><span class="sxs-lookup"><span data-stu-id="774ba-121">The firmware slot containing the currently active/running firmware image.</span></span>

</dd> <dt>

<span data-ttu-id="774ba-122">**PendingActivateSlot**</span><span class="sxs-lookup"><span data-stu-id="774ba-122">**PendingActivateSlot**</span></span>
</dt> <dd>

<span data-ttu-id="774ba-123">Der Firmwareslot, für den die Aktivierung aussteht.</span><span class="sxs-lookup"><span data-stu-id="774ba-123">The firmware slot that is pending activation.</span></span>

</dd> <dt>

<span data-ttu-id="774ba-124">**FirmwareShared**</span><span class="sxs-lookup"><span data-stu-id="774ba-124">**FirmwareShared**</span></span>
</dt> <dd>

<span data-ttu-id="774ba-125">Gibt an, dass die Firmware sowohl für das Gerät als auch für den Controller/Adapter gilt, z. B. NVMe SSD.</span><span class="sxs-lookup"><span data-stu-id="774ba-125">Indicates that the firmware applies to both the device and controller/adapter, e.g. NVMe SSD.</span></span>

</dd> <dt>

<span data-ttu-id="774ba-126">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="774ba-126">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="774ba-127">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="774ba-127">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="774ba-128">**ImagePayloadAlignment**</span><span class="sxs-lookup"><span data-stu-id="774ba-128">**ImagePayloadAlignment**</span></span>
</dt> <dd>

<span data-ttu-id="774ba-129">Die Ausrichtung der Bildnutzlast in Byteanzahl.</span><span class="sxs-lookup"><span data-stu-id="774ba-129">The alignment of the image payload, in number of bytes.</span></span> <span data-ttu-id="774ba-130">Der Höchstwert ist PAGE \_ SIZE.</span><span class="sxs-lookup"><span data-stu-id="774ba-130">The maximum is PAGE\_SIZE.</span></span> <span data-ttu-id="774ba-131">Die Übertragungsgröße ist ein Mutliple dieser Größe.</span><span class="sxs-lookup"><span data-stu-id="774ba-131">The transfer size is a mutliple of this size.</span></span> <span data-ttu-id="774ba-132">Einige Protokolle erfordern mindestens die Sektorgröße.</span><span class="sxs-lookup"><span data-stu-id="774ba-132">Some protocols require at least sector size.</span></span> <span data-ttu-id="774ba-133">Wenn dieser Wert auf 0 festgelegt ist, bedeutet dies, dass dieser Wert ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="774ba-133">When this value is set to 0, this means that this value is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="774ba-134">**ImagePayloadMaxSize**</span><span class="sxs-lookup"><span data-stu-id="774ba-134">**ImagePayloadMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="774ba-135">Die maximale Größe der Bildnutzlast, die für einen einzelnen Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="774ba-135">The image payload maximum size, this is used for a single command.</span></span>

</dd> <dt>

<span data-ttu-id="774ba-136">**Slot**</span><span class="sxs-lookup"><span data-stu-id="774ba-136">**Slot**</span></span>
</dt> <dd>

<span data-ttu-id="774ba-137">Enthält die Slotinformationen für jeden Slot auf dem Gerät vom Typ [**STORAGE \_ HW \_ FIRMWARE SLOT \_ \_ INFO**](storage-hw-firmware-slot-info.md).</span><span class="sxs-lookup"><span data-stu-id="774ba-137">Contains the slot information for each slot on the device, of type [**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**](storage-hw-firmware-slot-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="774ba-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="774ba-138">Requirements</span></span>



| <span data-ttu-id="774ba-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="774ba-139">Requirement</span></span> | <span data-ttu-id="774ba-140">Wert</span><span class="sxs-lookup"><span data-stu-id="774ba-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="774ba-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="774ba-141">Minimum supported client</span></span><br/> | <span data-ttu-id="774ba-142">Windows 10 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="774ba-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="774ba-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="774ba-143">Minimum supported server</span></span><br/> | <span data-ttu-id="774ba-144">Nur Windows Server \[ 2016-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="774ba-144">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="774ba-145">Header</span><span class="sxs-lookup"><span data-stu-id="774ba-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="774ba-146"><dt>Winioctl.h.h (einschließlich Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="774ba-146"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="774ba-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="774ba-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="774ba-148">**IOCTL \_ STORAGE \_ FIRMWARE \_ ACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="774ba-148">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="774ba-149">**STORAGE \_ HW \_ FIRMWARE \_ ACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="774ba-149">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="774ba-150">**HERUNTERLADEN DER \_ \_ IOCTL-SPEICHERFIRMWARE \_**</span><span class="sxs-lookup"><span data-stu-id="774ba-150">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="774ba-151">**DOWNLOAD DER \_ SPEICHER-HW-FIRMWARE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="774ba-151">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="774ba-152">**\_IOCTL-SPEICHERFIRMWARE \_ \_ – \_ GET-INFORMATIONEN**</span><span class="sxs-lookup"><span data-stu-id="774ba-152">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="774ba-153">**ABFRAGE \_ DER SPEICHER-HW-FIRMWAREINFORMATIONEN \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="774ba-153">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> <dt>

[<span data-ttu-id="774ba-154">**INFORMATIONEN ZUM \_ SPEICHER-HW-FIRMWARESLOT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="774ba-154">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




