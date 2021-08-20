---
title: StringCollection.item-Methode
description: Die Item-Methode ruft die Zeichenfolge am angegebenen Index ab.
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- Item-Windows Media Player
- item-Windows Media Player , StringCollection-Klasse
- StringCollection-Klasse Windows Media Player , Item-Methode
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
ms.openlocfilehash: f1a7ab868a1b8814b3ea67d0c37988e492ed2576758d7e8e68a7dbfa997c16b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832313"
---
# <a name="stringcollectionitem-method"></a>StringCollection.item-Methode

Die **Item-Methode** ruft die Zeichenfolge am angegebenen Index ab.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

**Number** (**long**), die den Index enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge zurück.**

## <a name="remarks"></a>Hinweise

Das **StringCollection-Objekt** wird verwendet, um den Satz von Werten abzurufen, die für ein Attribut verfügbar sind. Beispiel: *MediaCollection*. **Die getAttributeStringCollection-Methode** kann verwendet werden, um ein **StringCollection-Objekt** abzurufen, das alle Werte für das Genre-Attribut innerhalb des Audio-Medientyps darstellt. Die **Item-Eigenschaft** kann dann verwendet werden, um alle möglichen Werte für das Genre-Attribut zu iterieren.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MediaCollection.getAttributeStringCollection**](mediacollection-getattributestringcollection.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**StringCollection-Objekt**](stringcollection-object.md)
</dt> </dl>

 

 





