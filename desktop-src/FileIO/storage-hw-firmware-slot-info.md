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
# <a name="storage_hw_firmware_slot_info-structure"></a>Informationsstruktur des Speicher-HW- \_ \_ Firmware- \_ Slots \_

Diese Struktur enthält Informationen zu einem Slot auf einem Gerät.

## <a name="syntax"></a>Syntax


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



## <a name="members"></a>Member

<dl> <dt>

**Version**
</dt> <dd>

Die Version dieser-Struktur. Dieser Wert sollte auf sizeof festgelegt werden ( \_ Informationen zum firmwareinsloterinfo für Speicher \_ \_ \_

</dd> <dt>

**Größe**
</dt> <dd>

Die Größe dieser Struktur.

</dd> <dt>

**SlotNumber**
</dt> <dd>

Die Slotnummer dieses Slots.

</dd> <dt>

**ReadOnly**
</dt> <dd>

Gibt an, ob dieser Slot schreibgeschützt ist oder nicht.

</dd> <dt>

**Reserved0**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

**Reserved1**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

**Novel**
</dt> <dd>

Die Revision der Firmware in diesem Slot.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                        |
| Header<br/>                   | <dl> <dt>Winioctl. h. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOCTL- \_ Speicher \_ Firmware \_ aktivieren**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[**Aktivieren der Speicher- \_ HW- \_ Firmware \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[**Download der IOCTL- \_ Speicher \_ Firmware \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[**speicherhw- \_ \_ Firmwaredownload \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[**IOCTL- \_ Speicher \_ Firmware \_ get \_ Info**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[**Firmware-Informationen zur Speicher- \_ HW \_ \_**](storage-hw-firmware-info.md)
</dt> <dt>

[**\_Firmware- \_ \_ Informations \_ Abfrage für Speicher HW**](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




