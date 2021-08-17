---
description: Diese Klasse ist die Ereignistypklasse für Bildereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
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
ms.openlocfilehash: 44b957fbc1f8ffad78ec73d03a81fa45a8733a53e0e1d78fb31e48b9129a9e93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394650"
---
# <a name="image_load-class"></a>Image \_ Load-Klasse

Diese Klasse ist die Ereignistypklasse für Bildereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

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

Die **Image \_ Load-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Image \_ Load-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

DefaultBase
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(7), Zeiger
</dt> </dl>

Standardbasisadresse.

</dd> <dt>

FileName
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(12), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Dateiname und Erweiterung der DLL oder des ausführbaren Images.

</dd> <dt>

Imagebase
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

Basisadresse der Anwendung, in die das Image geladen wird.

</dd> <dt>

ImageCheckSum
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4)
</dt> </dl>

Summe der Bildüberprüfung.

</dd> <dt>

Imagesize
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Zeiger
</dt> </dl>

Größe des images, das geladen wird.

Bei der Verarbeitung dieser Eigenschaft ist der Datentyp für diese Eigenschaft tatsächlich die Größe \_ t. Der Zeigerqualifizierer wird verwendet, um zu bestimmen, ob die Größe \_ t 4 Byte oder 8 Bytes beträgt.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

Identifiziert den Prozess, in den das Image geladen wird.

</dd> <dt>

Reserved0
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6)
</dt> </dl>

Reserviert.

</dd> <dt>

Reserved1
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(8)
</dt> </dl>

Reserviert.

</dd> <dt>

Reserved2
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(9)
</dt> </dl>

Reserviert.

</dd> <dt>

Reserved3
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(10)
</dt> </dl>

Reserviert.

</dd> <dt>

Reserved4
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(11)
</dt> </dl>

Reserviert.

</dd> <dt>

TimeDateStamp
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5)
</dt> </dl>

Uhrzeit und Datum, zu denen das Image geladen oder entladen wurde.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die EREIGNISSE DCStart und DCEnd aufzählen alle geladenen Bilder am Anfang bzw. Ende der Ablaufverfolgung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Image**](image.md)
</dt> <dt>

[**Image \_ V0**](image-v0.md)
</dt> <dt>

[**Image \_ V1**](image-v1.md)
</dt> </dl>

 

 




