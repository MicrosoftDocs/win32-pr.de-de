---
title: MediaCollection.getByAttributeAndMediaType-Methode
description: Die getByAttributeAndMediaType-Methode ruft ein Playlist-Objekt ab, das Medienobjekte mit dem angegebenen Attribut und Medientyp enthält.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- getByAttributeAndMediaType-Methode Windows Media Player
- getByAttributeAndMediaType-Methode Windows Media Player , MediaCollection-Klasse
- MediaCollection-Klasse Windows Media Player , getByAttributeAndMediaType-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getByAttributeAndMediaType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46dab1bdcb511e4c96374b17bc6a98be95e48fd64d005eb856c9ec247af48f2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647880"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a>MediaCollection.getByAttributeAndMediaType-Methode

Die **getByAttributeAndMediaType-Methode** ruft ein **Playlist-Objekt** ab, das **Medienobjekte** mit dem angegebenen Attribut und Medientyp enthält.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.getByAttributeAndMediaType(
  attribute,
  value,
  mediaType
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*-Attribut* \[ In\]
</dt> <dd>

**Zeichenfolge,** die das Attribut enthält.

</dd> <dt>

*wert* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Wert enthält.

</dd> <dt>

*mediaType* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Medientyp enthält. Muss einen der folgenden Werte enthalten: "audio", "video", "photo", "playlist" oder "other".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Wiedergabelistenobjekt zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> </dl>

 

 





