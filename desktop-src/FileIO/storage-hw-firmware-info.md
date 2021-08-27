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
ms.openlocfilehash: 1b9aa008e108f1282f8f61aaeacdce11eba7016632fa9643ae3db5550efb1e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047910"
---
# <a name="storage_hw_firmware_info-structure"></a>\_SPEICHER HW \_ FIRMWARE \_ INFO-Struktur

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

Die Version dieser Struktur. Dieser sollte auf sizeof(STORAGE \_ HW FIRMWARE INFO) festgelegt \_ \_ werden.

</dd> <dt>

**Größe**
</dt> <dd>

Die Größe dieser Struktur als Puffer einschließlich Slot.

</dd> <dt>

**SupportUpgrade**
</dt> <dd>

Gibt an, dass diese Firmware ein Upgrade unterstützt.

</dd> <dt>

**Reserviert 0**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

**SlotCount**
</dt> <dd>

Die Anzahl der Firmwareslots auf dem Gerät. Dies ist die Dimension des Slotarrays.

> [!Note]  
> Einige Geräte können mehr als ein Firmwareimage speichern, wenn sie über mehr als einen Firmwareslot verfügen.

 

</dd> <dt>

**ActiveSlot**
</dt> <dd>

Der Firmwareslot, der das aktuell aktive/ausgeführte Firmwareimage enthält.

</dd> <dt>

**PendingActivateSlot**
</dt> <dd>

Der Firmwareslot, für den die Aktivierung aussteht.

</dd> <dt>

**FirmwareShared**
</dt> <dd>

Gibt an, dass die Firmware sowohl für das Gerät als auch für den Controller/Adapter gilt, z. B. NVMe SSD.

</dd> <dt>

**Reserved**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

**ImagePayloadAlignment**
</dt> <dd>

Die Ausrichtung der Bildnutzlast in Anzahl von Bytes. Der Höchstwert ist PAGE \_ SIZE. Die Übertragungsgröße ist ein Mutliple dieser Größe. Einige Protokolle erfordern mindestens die Sektorgröße. Wenn dieser Wert auf 0 festgelegt ist, bedeutet dies, dass dieser Wert ungültig ist.

</dd> <dt>

**ImagePayloadMaxSize**
</dt> <dd>

Die maximale Größe der Imagenutzlast, die für einen einzelnen Befehl verwendet wird.

</dd> <dt>

**Slot**
</dt> <dd>

Enthält die Slotinformationen für jeden Slot auf dem Gerät vom Typ [**STORAGE \_ HW \_ FIRMWARE SLOT \_ \_ INFO**](storage-hw-firmware-slot-info.md).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                        |
| Header<br/>                   | <dl> <dt>Winioctl.h.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AKTIVIEREN DER \_ IOCTL-SPEICHERFIRMWARE \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[**AKTIVIEREN DER \_ SPEICHER-HW-FIRMWARE \_ \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[**HERUNTERLADEN DER \_ IOCTL-SPEICHERFIRMWARE \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[**DOWNLOAD DER \_ SPEICHER-HW-FIRMWARE \_ \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[**\_IOCTL-SPEICHERFIRMWARE \_ \_ – ABRUFEN VON \_ INFORMATIONEN**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[**\_SPEICHER HW FIRMWARE INFO QUERY (ABFRAGE DER \_ SPEICHER-HW-FIRMWAREINFORMATIONEN) \_ \_**](storage-hw-firmware-info-query.md)
</dt> <dt>

[**INFORMATIONEN ZUM \_ SPEICHER-HW-FIRMWARESLOT \_ \_ \_**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




