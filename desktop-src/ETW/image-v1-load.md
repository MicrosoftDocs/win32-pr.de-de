---
description: Diese Klasse ist die Ereignistyp Klasse für Bild Lade Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: bd0a2a61b263ce78c2cf28cdf1cd5df4b702140d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977120"
---
# <a name="image_v1_load-class"></a>Image \_ v1- \_ Lade Klasse

Diese Klasse ist die Ereignistyp Klasse für Bild Lade Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **\_ \_ Load** -Klasse von Image v1 verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ Load** -Klasse von Image v1 verfügt über diese Eigenschaften.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4), stringbeendigung ("nullterminiert"), Format ("w")
</dt> </dl>

Dateiname und Erweiterung der zu ladenden DLL oder des zu ladenden ausführbaren Images.

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

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Bild \_ v1**](image-v1.md)
</dt> </dl>

 

 




