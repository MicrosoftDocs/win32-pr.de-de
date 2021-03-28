---
description: Diese Klasse ist die Ereignistyp Klasse für Bild Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 70ec0542-16d3-4186-a346-7f3c44dedf67
title: Image_Load-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_Load
- Image_Load.ImageBase
- Image_Load.ImageSize
- Image_Load.ProcessId
- Image_Load.ImageCheckSum
- Image_Load.TimeDateStamp
- Image_Load.Reserved0
- Image_Load.DefaultBase
- Image_Load.Reserved1
- Image_Load.Reserved2
- Image_Load.Reserved3
- Image_Load.Reserved4
- Image_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 647879b972c7cff2c086f656f76fa8decedb49a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528652"
---
# <a name="image_load-class"></a>Image- \_ Lade Klasse

Diese Klasse ist die Ereignistyp Klasse für Bild Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(10, 2, 3, 4), EventTypeName("Load", "Unload", "DCStart", "DCEnd")]
class Image_Load : Image
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  uint32 ImageCheckSum;
  uint32 TimeDateStamp;
  uint32 Reserved0;
  uint32 DefaultBase;
  uint32 Reserved1;
  uint32 Reserved2;
  uint32 Reserved3;
  uint32 Reserved4;
  string FileName;
};
```

## <a name="members"></a>Member

Die **Bild \_ Lade** Klasse verfügt über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Bild \_ Lade** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

DEFAULTBASE
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (7), Zeiger
</dt> </dl>

Standardbasis Adresse.

</dd> <dt>

FileName
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (12), stringbeendigung ("nullterminiert"), Format ("w")
</dt> </dl>

Dateiname und Erweiterung der DLL oder des ausführbaren Images.

</dd> <dt>

ImageBase
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Zeiger
</dt> </dl>

Die Basisadresse der Anwendung, in der das Image geladen wird.

</dd> <dt>

Imagechecksum
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4)
</dt> </dl>

Abbild-Prüfsumme.

</dd> <dt>

ImageSize
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2), Zeiger
</dt> </dl>

Größe des geladenen Bilds.

Wenn diese Eigenschaft genutzt wird, ist die Größe des Datentyps für diese Eigenschaft tatsächlich " \_ t". Der Zeiger Qualifizierer wird verwendet, um zu bestimmen, ob die Größe \_ t 4 Bytes oder 8 Bytes beträgt.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3)
</dt> </dl>

Identifiziert den Prozess, in den das Bild geladen wird.

</dd> <dt>

Reserved0
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (6)
</dt> </dl>

Reserviert.

</dd> <dt>

Reserved1
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (8)
</dt> </dl>

Reserviert.

</dd> <dt>

Reserved2
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (9)
</dt> </dl>

Reserviert.

</dd> <dt>

"Reserved3"
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (10)
</dt> </dl>

Reserviert.

</dd> <dt>

"Reserved4"
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (11)
</dt> </dl>

Reserviert.

</dd> <dt>

TimeDateStamp
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (5)
</dt> </dl>

Uhrzeit und Datum, zu der das Bild geladen oder entladen wurde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mit den Ereignissen DCStart und DCEnd werden alle geladenen Bilder am Anfang bzw. Ende der Ablauf Verfolgung aufgelistet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Image**](image.md)
</dt> <dt>

[**Bild \_ v0**](image-v0.md)
</dt> <dt>

[**Bild \_ v1**](image-v1.md)
</dt> </dl>

 

 




