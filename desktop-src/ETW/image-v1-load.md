---
description: 'Image_V1_Load-Klasse: Diese Klasse ist die Ereignistypklasse für Bildladeereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
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
ms.openlocfilehash: 2e8a8c31cee7e45311887c16a1d10545e6a38e41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106498"
---
# <a name="image_v1_load-class"></a>Image \_ V1 \_ Load-Klasse

Diese Klasse ist die Ereignistypklasse für Bildladeereignisse.

Die folgende Syntax wird aus MOF-Code vereinfacht.

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

Die **Image \_ V1 \_ Load-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Image \_ V1 \_ Load-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Dateiname und Erweiterung der zu ladende DLL oder des ausführbaren Images.

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

Größe des geladenen Images.

Beim Verwenden dieser Eigenschaft ist der Datentyp für diese Eigenschaft tatsächlich die Größe \_ t. Der Zeigerqualifizierer wird verwendet, um zu bestimmen, ob die Größe \_ t 4 Byte oder 8 Bytes beträgt.

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



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Image \_ V1**](image-v1.md)
</dt> </dl>

 

 




