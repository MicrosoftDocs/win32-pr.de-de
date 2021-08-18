---
title: MediaCollection.getAttributeStringCollection-Methode
description: Die getAttributeStringCollection-Methode ruft ein StringCollection-Objekt ab, das den Satz aller Werte für ein angegebenes Attribut innerhalb eines angegebenen Medientyps darstellt.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- getAttributeStringCollection-Methode Windows Media Player
- getAttributeStringCollection-Methode Windows Media Player , MediaCollection-Klasse
- MediaCollection-Klasse Windows Media Player , getAttributeStringCollection-Methode
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
ms.openlocfilehash: c27b7c6dbef585763ecfda1abdc7beadfa3d883476033424ff868a3d56c4bb96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996300"
---
# <a name="mediacollectiongetattributestringcollection-method"></a>MediaCollection.getAttributeStringCollection-Methode

Die **getAttributeStringCollection-Methode** ruft ein **StringCollection-Objekt** ab, das den Satz aller Werte für ein angegebenes Attribut innerhalb eines angegebenen Medientyps darstellt.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*-Attribut* \[ In\]
</dt> <dd>

**Zeichenfolge,** die das Attribut angibt.

</dd> <dt>

*mediaType* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Medientyp darstellt. Enthält einen der folgenden Werte: "Audio", "Video", "Playlist" oder "Other".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **StringCollection-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Informationen zu den attributen, die von Windows Media Player unterstützt werden, finden Sie im Abschnitt [Attributreferenz.](attribute-reference.md)

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *MediaCollection* verwendet. **getAttributeStringCollection,** um eine Liste von Werten anzuzeigen, die einem bestimmten Attribut für Audioelemente in der Medienauflistung entsprechen. Mit einem HTML SELECT-Element, das mit id = "Attribute" erstellt wurde, kann der Benutzer ein Attribut auswählen, z. B. Interpret, Genre oder Album. Ein HTML TEXTAREA-Element, das mit ID = "AttributeVals" erstellt wurde, zeigt das Ergebnis an. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**StringCollection-Objekt**](stringcollection-object.md)
</dt> </dl>

 

 





