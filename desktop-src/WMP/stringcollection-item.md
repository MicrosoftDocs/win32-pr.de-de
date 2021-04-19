---
title: StringCollection. Item-Methode
description: Die Item-Methode ruft die Zeichenfolge am angegebenen Index ab.
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, StringCollection-Klasse
- StringCollection-Klasse, Windows Media Player, Element-Methode
topic_type:
- apiref
api_name:
- StringCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4244ad194ff3426dab81baddc0b7188214e0360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359213"
---
# <a name="stringcollectionitem-method"></a>StringCollection. Item-Methode

Die **Item** -Methode ruft die Zeichenfolge am angegebenen Index ab.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Die **Zahl** (**Long**), die den Index enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück.

## <a name="remarks"></a>Bemerkungen

Das **StringCollection** -Objekt wird verwendet, um den Satz von Werten abzurufen, die für ein Attribut verfügbar sind. Beispielsweise *mediacollection*. die **getAttributeStringCollection** -Methode kann verwendet werden, um ein **StringCollection** -Objekt abzurufen, das alle Werte für das Genre-Attribut im audiomedientyp darstellt. Die **Item** -Eigenschaft kann dann zum Durchlaufen aller möglichen Werte für das Genre-Attribut verwendet werden.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mediacollection. getAttributeStringCollection**](mediacollection-getattributestringcollection.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**StringCollection-Objekt**](stringcollection-object.md)
</dt> </dl>

 

 





