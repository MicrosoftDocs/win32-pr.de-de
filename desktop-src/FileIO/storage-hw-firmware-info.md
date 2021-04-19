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
# <a name="storage_hw_firmware_info-structure"></a>\_Firmware- \_ \_ Informationsstruktur für Speicher HW

Diese Struktur enthält Informationen zur Gerätefirmware.

## <a name="syntax"></a>Syntax


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



## <a name="members"></a>Member

<dl> <dt>

**Version**
</dt> <dd>

Die Version dieser-Struktur. Dieser Wert sollte auf sizeof festgelegt werden (Informationen zur Speicher \_ HW- \_ Firmware \_ ).

</dd> <dt>

**Größe**
</dt> <dd>

Die Größe dieser-Struktur als Puffer einschließlich Slot.

</dd> <dt>

**Supportupgrade**
</dt> <dd>

Gibt an, dass diese Firmware ein Upgrade unterstützt.

</dd> <dt>

**Reserved0**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

**Slotcount**
</dt> <dd>

Die Anzahl der Firmware-Slots auf dem Gerät. Dies ist die Dimension des Slot-Arrays.

> [!Note]  
> Einige Geräte können mehr als 1 Firmwareabbild speichern, wenn Sie über mehr als einen firmwareslot verfügen.

 

</dd> <dt>

**Activeslot**
</dt> <dd>

Der firmwareslot, der das derzeit aktive/laufende Firmwareabbild enthält

</dd> <dt>

**"Menge"**
</dt> <dd>

Der Firmware-Slot, für den die Aktivierung aussteht.

</dd> <dt>

**Firmwaresed**
</dt> <dd>

Gibt an, dass die Firmware sowohl für das Gerät als auch für den Controller/Adapter gilt, z. b. nvme-SSD.

</dd> <dt>

**Reserved**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

**Imagepayloadalignment**
</dt> <dd>

Die Ausrichtung der Bild Nutzlast (in Byte). Der Höchstwert ist die Seiten \_ Größe. Die Übertragungs Größe ist ein mutwert dieser Größe. Für einige Protokolle ist mindestens eine Sektorgröße erforderlich. Wenn dieser Wert auf 0 festgelegt ist, bedeutet dies, dass dieser Wert ungültig ist.

</dd> <dt>

**Imagepayloadmaxsize**
</dt> <dd>

Die maximale Größe der Bild Nutzlast, die für einen einzelnen Befehl verwendet wird.

</dd> <dt>

**Slot**
</dt> <dd>

Enthält die slotinformationen für jeden Slot auf dem Gerät, vom Typ [**Speicher-HW firmwareinstellerinformationen \_ \_ \_ \_**](storage-hw-firmware-slot-info.md).

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

[**\_Firmware- \_ \_ Informations \_ Abfrage für Speicher HW**](storage-hw-firmware-info-query.md)
</dt> <dt>

[**\_Informationen zum \_ Firmware- \_ Slot \_ für Speicher HW**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




