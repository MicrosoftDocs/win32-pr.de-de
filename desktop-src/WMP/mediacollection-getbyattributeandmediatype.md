---
title: Mediacollection. getbyattributeandmediatype-Methode
description: Die getbyattributeandmediatype-Methode ruft ein Wiedergabelisten Objekt ab, das Medienobjekte mit dem angegebenen Attribut und Medientyp enthält.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- getbyattributeandmediatype-Methode, Windows Media Player
- getbyattributeandmediatype-Methode Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getbyattributeandmediatype-Methode
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
ms.openlocfilehash: 7e26abbf2f19d50ec6a10ebbafe12afae8576f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361592"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a>Mediacollection. getbyattributeandmediatype-Methode

Die **getbyattributeandmediatype** -Methode ruft ein **Wiedergabe** Listen Objekt ab, das **Medien** Objekte mit dem angegebenen Attribut und Medientyp enthält.

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

*Attribut* \[ in\]
</dt> <dd>

**Zeichenfolge** , die das Attribut enthält.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Wert enthält.

</dd> <dt>

*mediaType* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Medientyp enthält. Muss einen der folgenden Werte enthalten: "Audiodatei", "Video", "Photo", "Wiedergabeliste" oder "Other".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> <dt>

[**Mediacollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> </dl>

 

 





