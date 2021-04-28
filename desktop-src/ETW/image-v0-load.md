---
description: 'Image_V0_Load Klasse: Diese Klasse ist die Ereignistypklasse für Bildladeereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
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
ms.openlocfilehash: ed15254ac509334c802ba4c6165c73e681a2c7b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106512"
---
# <a name="image_v0_load-class"></a>Image \_ V0 \_ Load-Klasse

Diese Klasse ist die Ereignistypklasse für Bildladeereignisse.

Die folgende Syntax wird durch MOF-Code vereinfacht.

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

Die **Image \_ V0 \_ Load-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Image \_ V0 \_ Load-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

BaseAddress
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

Basisadresse der Anwendung, in die das Image geladen wird.

</dd> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Dateiname und Erweiterung der zu ladenden DLL oder des ausführbaren Images.

</dd> <dt>

ModuleSize
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2)
</dt> </dl>

Größe des Bilds.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Image \_ V0**](image-v0.md)
</dt> </dl>

 

 




