---
description: Enthält die Seriennummer eines USB-Geräts. Sie wird vom IOCTL- \_ Speicher \_ Ablaufsteuerungs-Code für \_ Medien \_ Seriennummern verwendet \_ .
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: MEDIA_SERIAL_NUMBER_DATA Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SERIAL_NUMBER_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 843c445a29bcce9e6dc26b66b0c6738831e9b79c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355711"
---
# <a name="media_serial_number_data-structure"></a>\_Datenstruktur der Medien Serien \_ Nummer \_

Enthält die Seriennummer eines USB-Geräts. Sie wird vom ioctl-Speicher Ablaufsteuerungs-Code für [**\_ \_ \_ Medien \_ Serien \_ Nummern**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct _MEDIA_SERIAL_NUMBER_DATA {
  ULONG SerialNumberLength;
  ULONG Result;
  ULONG Reserved[2];
  UCHAR SerialNumberData[];
} MEDIA_SERIAL_NUMBER_DATA, *PMEDIA_SERIAL_NUMBER_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**Serialzahldauer**
</dt> <dd>

Die Größe der **serialnummeri-Daten** Zeichenfolge in Bytes.

</dd> <dt>

**Ergebnis**
</dt> <dd>

Der Status der Anforderung.

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**Serialzahldaten**
</dt> <dd>

Die Seriennummer des Geräts.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Für die Datenstruktur der **Medien \_ Serien \_ Nummer \_** ist keine Header Datei verfügbar. Fügen Sie die Struktur Definition am oberen Rand dieser Seite in den Quellcode ein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOCTL- \_ Speicher \_ Medien- \_ \_ Serien \_ Nummer**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




