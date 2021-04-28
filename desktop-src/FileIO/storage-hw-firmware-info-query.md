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
# <a name="storage_hw_firmware_info_query-structure"></a>ABFRAGEstruktur \_ der SPEICHER-HW-FIRMWAREINFO \_ \_ \_

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

Die Version dieser -Struktur. Dies sollte auf sizeof (STORAGE \_ HW \_ FIRMWARE INFO \_ QUERY) festgelegt \_ werden.

</dd> <dt>

**Größe**
</dt> <dd>

Die Größe dieser Struktur als Puffer.

</dd> <dt>

**Flags**
</dt> <dd>

Die der Abfrage zugeordneten Flags. Im Folgenden finden Sie Flags, die in diesem Member festgelegt werden können.



| Flag                                             | Beschreibung                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| STORAGE \_ HW \_ FIRMWARE \_ REQUEST \_ FLAG \_ CONTROLLER | Gibt an, dass das Ziel der Anforderung nicht die Hand/das Objekt des Geräts selbst ist. |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 \[ Desktop-Apps\]<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2016-Desktop-Apps\]<br/>                                                        |
| Header<br/>                   | <dl> <dt>Winioctl.h.h (einschließlich Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IOCTL \_ STORAGE \_ FIRMWARE \_ ACTIVATE**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[**STORAGE \_ HW \_ FIRMWARE \_ ACTIVATE**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[**HERUNTERLADEN DER \_ \_ IOCTL-SPEICHERFIRMWARE \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[**DOWNLOAD DER \_ SPEICHER-HW-FIRMWARE \_ \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[**\_IOCTL-SPEICHERFIRMWARE \_ \_ – \_ GET-INFORMATIONEN**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[**\_ \_ SPEICHER-HW-FIRMWAREINFORMATIONEN \_**](storage-hw-firmware-info.md)
</dt> <dt>

[**INFORMATIONEN ZUM \_ SPEICHER-HW-FIRMWARESLOT \_ \_ \_**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




