---
title: StringCollection. getattributezähltbytype-Methode
description: Die getattributezähltbytype-Methode ruft die Anzahl der Attribute ab, die dem angegebenen StringCollection-Element Index, dem angegebenen Attributnamen und der angegebenen Sprache zugeordnet sind.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- getattributezähltbytype-Methode, Windows Media Player
- getattributecountrytbytype-Methode, Windows Media Player, StringCollection-Klasse
- StringCollection-Klasse, Windows Media Player, getattributezähltbytype-Methode
topic_type:
- apiref
api_name:
- StringCollection.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acf2d7a1f8849f9bd0e83ead3880ca90d2d6149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361944"
---
# <a name="stringcollectiongetattributecountbytype-method"></a>StringCollection. getattributezähltbytype-Methode

Die **getattributezähltbytype** -Methode ruft die Anzahl der Attribute ab, die dem angegebenen **StringCollection** -Element Index, dem angegebenen Attributnamen und der angegebenen Sprache zugeordnet sind.

## <a name="syntax"></a>Syntax


```JScript
retVal = StringCollection.getAttributeCountByType(
  index,
  name,
  language
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

**Number** (**Long**) gibt den NULL basierten Index des **StringCollection** -Elements an, aus dem das Attribut bezogen werden soll.

</dd> <dt>

*Name* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen des Attributs enthält.

</dd> <dt>

*Sprache* \[ in\]
</dt> <dd>

**Zeichenfolge** , die die Sprache enthält. Wenn der Wert auf NULL oder eine leere Zeichenfolge ("") festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet. Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**Long**) zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird verwendet, um die Anzahl der Attribute zu bestimmen, die einem bestimmten Attributnamen für ein bestimmtes **StringCollection** -Element entsprechen. Index Nummern können dann an den vierten Parameter der **StringCollection. getItemInfoByType** -Methode übergeben werden.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**StringCollection-Objekt**](stringcollection-object.md)
</dt> </dl>

 

 





