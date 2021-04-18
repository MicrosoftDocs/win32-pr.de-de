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
# <a name="storage_hw_firmware_info_query-structure"></a>\_ \_ \_ \_ Abfrage Struktur der Speicher-HW-Firmware

Diese Struktur enthält Informationen zur Gerätefirmware.

## <a name="syntax"></a>Syntax


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a>Member

<dl> <dt>

**Version**
</dt> <dd>

Die Version dieser-Struktur. Dieser Wert sollte auf sizeof (Speicher \_ HW \_ Firmware \_ Info \_ Query) festgelegt werden.

</dd> <dt>

**Größe**
</dt> <dd>

Die Größe dieser-Struktur als Puffer.

</dd> <dt>

**Flags**
</dt> <dd>

Die der Abfrage zugeordneten Flags. Im folgenden finden Sie Flags, die in diesem Member festgelegt werden können.



| Flag                                             | Beschreibung                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| speicherhw-firmwareanforderungs- \_ \_ \_ \_ Flag \_ Controller | Gibt an, dass das Ziel der Anforderung nicht das Hand-Objekt selbst ist. |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

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

[**\_Informationen zum \_ Firmware- \_ Slot \_ für Speicher HW**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




