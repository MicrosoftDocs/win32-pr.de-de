---
description: Diese Klasse ist die Ereignistyp Klasse für Bild Lade Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: e2836153-8e4f-4c7f-9542-9402ed9e4356
title: Image_V0_Load-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V0_Load
- Image_V0_Load.BaseAddress
- Image_V0_Load.ModuleSize
- Image_V0_Load.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: b2486e6918884e51a57f077dc9c569f926dc902e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977121"
---
# <a name="image_v0_load-class"></a>Image \_ v0- \_ Lade Klasse

Diese Klasse ist die Ereignistyp Klasse für Bild Lade Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a>Member

Die **\_ \_ Load** -Klasse von Image v0 verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ Load** -Klasse von Image v0 verfügt über diese Eigenschaften.

<dl> <dt>

BaseAddress
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Zeiger
</dt> </dl>

Die Basisadresse der Anwendung, in der das Image geladen wird.

</dd> <dt>

Imagefilename
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3), stringbeendigung ("nullterminiert"), Format ("w")
</dt> </dl>

Dateiname und Erweiterung der zu ladenden DLL oder des zu ladenden ausführbaren Images.

</dd> <dt>

Modulesize
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2)
</dt> </dl>

Größe des Bilds.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Bild \_ v0**](image-v0.md)
</dt> </dl>

 

 




