---
title: Media. getattributezähltbytype-Methode
description: Die getattributezähltbytype-Methode ruft die Anzahl der Attribute ab, die dem angegebenen Attributnamen und der Sprache zugeordnet sind.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- getattributezähltbytype-Methode, Windows Media Player
- getattributezähltbytype-Methode, Windows Media Player, Medienklasse
- Media Class Windows Media Player, getattributezähltbytype-Methode
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613dca43c32322cd5e7de2b2b04605789009cbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361025"
---
# <a name="mediagetattributecountbytype-method"></a>Media. getattributezähltbytype-Methode

Die **getattributezähltbytype** -Methode ruft die Anzahl der Attribute ab, die dem angegebenen Attributnamen und der Sprache zugeordnet sind.

## <a name="syntax"></a>Syntax


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen des Attributs enthält. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

</dd> <dt>

*Sprache* \[ in\]
</dt> <dd>

**Zeichenfolge** , die die Sprache darstellt. Wenn der Wert auf NULL oder "" (leere Zeichenfolge) festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet. Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**Long**) zurück, die die Attribut Anzahl enthält.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird verwendet, um die Anzahl der Attribute zu bestimmen, die einem bestimmten Attributnamen für ein bestimmtes **Medien** Objekt entsprechen. Index Nummern können dann an die **getItemInfoByType** -Methode weitergegeben werden. Dies ist beispielsweise hilfreich, wenn ein Medien Element unter mehreren Genres kategorisiert wurde.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mediaobject**](media-object.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





