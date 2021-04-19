---
title: Mediacollection. getAttributeStringCollection-Methode
description: Die getAttributeStringCollection-Methode ruft ein StringCollection-Objekt ab, das den Satz aller Werte für ein angegebenes Attribut innerhalb eines angegebenen Medientyps darstellt.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- getAttributeStringCollection-Methode, Windows Media Player
- getAttributeStringCollection-Methode Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getAttributeStringCollection-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getAttributeStringCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d50d25488a05e6076c99802ce738edf02298ade
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352024"
---
# <a name="mediacollectiongetattributestringcollection-method"></a>Mediacollection. getAttributeStringCollection-Methode

Die **getAttributeStringCollection** -Methode ruft ein **StringCollection** -Objekt ab, das den Satz aller Werte für ein angegebenes Attribut innerhalb eines angegebenen Medientyps darstellt.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Attribut* \[ in\]
</dt> <dd>

**Zeichenfolge** , die das Attribut angibt.

</dd> <dt>

*mediaType* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Medientyp darstellt. Enthält einen der folgenden Werte: "Audiodatei", "Video", "Wiedergabeliste" oder "andere".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **StringCollection** -Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie im Abschnitt [Attribut Verweis](attribute-reference.md) .

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *mediacollection* verwendet. **getAttributeStringCollection** zum Anzeigen einer Liste von Werten, die einem bestimmten Attribut für Audioelemente in der Mediensammlung entsprechen. Ein HTML SELECT-Element, das mit ID = "Attribute" erstellt wurde, ermöglicht dem Benutzer die Auswahl eines Attributs, z. b. eines Künstlers, Genres oder Albums. Mit einem HTML-TEXTAREA-Element, das mit ID = "attributevals" erstellt wurde, wird das Ergebnis angezeigt. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Clear the text in the display area.
AttributeVals.value = "";

// Store the mediaCollection object.
var library = Player.mediaCollection;

// Get the string collection for the attribute type the user selects.
var all = library.getAttributeStringCollection(Attribute.value, "Audio");

// Loop through the string collection.
for (i = 0; i < all.count; i++){

    // Display the items one line at a time.
    AttributeVals.value += all.item(i);
    AttributeVals.value += "\n";
}

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mediacollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**StringCollection-Objekt**](stringcollection-object.md)
</dt> </dl>

 

 





