---
description: Diese Struktur enthält Informationen zur Gerätefirmware.
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: STORAGE_HW_FIRMWARE_INFO Struktur (winioctl. h)
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
ms.openlocfilehash: 5d611df1708059b0ee636a64f55026caf8801fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349625"
---
# <a name="storage_hw_firmware_info-structure"></a><span data-ttu-id="5f3ed-103">\_Firmware- \_ \_ Informationsstruktur für Speicher HW</span><span class="sxs-lookup"><span data-stu-id="5f3ed-103">STORAGE\_HW\_FIRMWARE\_INFO structure</span></span>

<span data-ttu-id="5f3ed-104">Diese Struktur enthält Informationen zur Gerätefirmware.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f3ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f3ed-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="5f3ed-106">Member</span><span class="sxs-lookup"><span data-stu-id="5f3ed-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5f3ed-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="5f3ed-108">Die Version dieser-Struktur.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-108">The version of this structure.</span></span> <span data-ttu-id="5f3ed-109">Dieser Wert sollte auf sizeof festgelegt werden (Informationen zur Speicher \_ HW- \_ Firmware \_ ).</span><span class="sxs-lookup"><span data-stu-id="5f3ed-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="5f3ed-110">**Größe**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="5f3ed-111">Die Größe dieser-Struktur als Puffer einschließlich Slot.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-111">The size of this structure as a buffer including slot.</span></span>

</dd> <dt>

<span data-ttu-id="5f3ed-112">**Supportupgrade**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-112">**SupportUpgrade**</span></span>
</dt> <dd>

<span data-ttu-id="5f3ed-113">Gibt an, dass diese Firmware ein Upgrade unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-113">Indicates that this firmware supports an upgrade.</span></span>

</dd> <dt>

<span data-ttu-id="5f3ed-114">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-114">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="5f3ed-115">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-115">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="5f3ed-116">**Slotcount**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-116">**SlotCount**</span></span>
</dt> <dd>

<span data-ttu-id="5f3ed-117">Die Anzahl der Firmware-Slots auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-117">The number of firmware slots on the device.</span></span> <span data-ttu-id="5f3ed-118">Dies ist die Dimension des Slot-Arrays.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-118">This is the dimension of the Slot array.</span></span>

> [!Note]  
> <span data-ttu-id="5f3ed-119">Einige Geräte können mehr als 1 Firmwareabbild speichern, wenn Sie über mehr als einen firmwareslot verfügen.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-119">Some devices can store more than 1 firmware image, if they have more than 1 firmware slot.</span></span>

 

</dd> <dt>

<span data-ttu-id="5f3ed-120">**Activeslot**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-120">**ActiveSlot**</span></span>
</dt> <dd>

<span data-ttu-id="5f3ed-121">Der firmwareslot, der das derzeit aktive/laufende Firmwareabbild enthält</span><span class="sxs-lookup"><span data-stu-id="5f3ed-121">The firmware slot containing the currently active/running firmware image.</span></span>

</dd> <dt>

<span data-ttu-id="5f3ed-122">**"Menge"**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-122">**PendingActivateSlot**</span></span>
</dt> <dd>

<span data-ttu-id="5f3ed-123">Der Firmware-Slot, für den die Aktivierung aussteht.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-123">The firmware slot that is pending activation.</span></span>

</dd> <dt>

<span data-ttu-id="5f3ed-124">**Firmwaresed**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-124">**FirmwareShared**</span></span>
</dt> <dd>

<span data-ttu-id="5f3ed-125">Gibt an, dass die Firmware sowohl für das Gerät als auch für den Controller/Adapter gilt, z. b. nvme-SSD.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-125">Indicates that the firmware applies to both the device and controller/adapter, e.g. NVMe SSD.</span></span>

</dd> <dt>

<span data-ttu-id="5f3ed-126">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-126">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="5f3ed-127">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-127">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="5f3ed-128">**Imagepayloadalignment**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-128">**ImagePayloadAlignment**</span></span>
</dt> <dd>

<span data-ttu-id="5f3ed-129">Die Ausrichtung der Bild Nutzlast (in Byte).</span><span class="sxs-lookup"><span data-stu-id="5f3ed-129">The alignment of the image payload, in number of bytes.</span></span> <span data-ttu-id="5f3ed-130">Der Höchstwert ist die Seiten \_ Größe.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-130">The maximum is PAGE\_SIZE.</span></span> <span data-ttu-id="5f3ed-131">Die Übertragungs Größe ist ein mutwert dieser Größe.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-131">The transfer size is a mutliple of this size.</span></span> <span data-ttu-id="5f3ed-132">Für einige Protokolle ist mindestens eine Sektorgröße erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-132">Some protocols require at least sector size.</span></span> <span data-ttu-id="5f3ed-133">Wenn dieser Wert auf 0 festgelegt ist, bedeutet dies, dass dieser Wert ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-133">When this value is set to 0, this means that this value is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="5f3ed-134">**Imagepayloadmaxsize**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-134">**ImagePayloadMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="5f3ed-135">Die maximale Größe der Bild Nutzlast, die für einen einzelnen Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-135">The image payload maximum size, this is used for a single command.</span></span>

</dd> <dt>

<span data-ttu-id="5f3ed-136">**Slot**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-136">**Slot**</span></span>
</dt> <dd>

<span data-ttu-id="5f3ed-137">Enthält die slotinformationen für jeden Slot auf dem Gerät, vom Typ [**Speicher-HW firmwareinstellerinformationen \_ \_ \_ \_**](storage-hw-firmware-slot-info.md).</span><span class="sxs-lookup"><span data-stu-id="5f3ed-137">Contains the slot information for each slot on the device, of type [**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**](storage-hw-firmware-slot-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f3ed-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f3ed-138">Requirements</span></span>



| <span data-ttu-id="5f3ed-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f3ed-139">Requirement</span></span> | <span data-ttu-id="5f3ed-140">Wert</span><span class="sxs-lookup"><span data-stu-id="5f3ed-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f3ed-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f3ed-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5f3ed-142">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f3ed-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="5f3ed-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f3ed-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5f3ed-144">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f3ed-144">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="5f3ed-145">Header</span><span class="sxs-lookup"><span data-stu-id="5f3ed-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f3ed-146"><dt>Winioctl. h. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f3ed-146"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f3ed-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f3ed-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f3ed-148">**IOCTL- \_ Speicher \_ Firmware \_ aktivieren**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-148">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="5f3ed-149">**Aktivieren der Speicher- \_ HW- \_ Firmware \_**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-149">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="5f3ed-150">**Download der IOCTL- \_ Speicher \_ Firmware \_**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-150">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="5f3ed-151">**speicherhw- \_ \_ Firmwaredownload \_**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-151">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="5f3ed-152">**IOCTL- \_ Speicher \_ Firmware \_ get \_ Info**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-152">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="5f3ed-153">**\_Firmware- \_ \_ Informations \_ Abfrage für Speicher HW**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-153">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> <dt>

[<span data-ttu-id="5f3ed-154">**\_Informationen zum \_ Firmware- \_ Slot \_ für Speicher HW**</span><span class="sxs-lookup"><span data-stu-id="5f3ed-154">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




