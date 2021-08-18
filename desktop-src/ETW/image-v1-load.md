---
description: 'Image_V1_Load Klasse: Diese Klasse ist die Ereignistypklasse für Bildladeereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.'
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Image_V1_Load-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V1_Load
- Image_V1_Load.ImageBase
- Image_V1_Load.ImageSize
- Image_V1_Load.ProcessId
- Image_V1_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 35144317b67a8d24ec07d72633897366e83628d6cc66d9c4661980fc44c373b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070160"
---
# <a name="image_v1_load-class"></a>Image \_ V1 \_ Load-Klasse

Diese Klasse ist die Ereignistypklasse für Bildladeereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V1_Load : Image_V1
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  string FileName;
};
```

## <a name="members"></a>Member

Die **Image \_ V1 \_ Load-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Image \_ V1 \_ Load-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Dateiname und Erweiterung der zu ladenden DLL oder des ausführbaren Images.

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

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Image \_ V1**](image-v1.md)
</dt> </dl>

 

 




