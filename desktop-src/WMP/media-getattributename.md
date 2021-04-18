---
title: Media. GetAttributeName-Methode
description: Die GetAttributeName-Methode ruft den Namen des Attributs ab, das dem angegebenen Index entspricht.
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- GetAttributeName-Methode, Windows-Media Player
- GetAttributeName-Methode, Windows Media Player, Medienklasse
- Medienklasse Windows Media Player, GetAttributeName-Methode
topic_type:
- apiref
api_name:
- Media.getAttributeName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7134b68837a7a5d1b765c64320ae68c56c6fc56
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357591"
---
# <a name="mediagetattributename-method"></a>Media. GetAttributeName-Methode

Die **GetAttributeName** -Methode ruft den Namen des Attributs ab, das dem angegebenen Index entspricht.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Die **Zahl** (**Long**), die den Index des Attributs enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück, die den Namen des Attributs angibt.

## <a name="remarks"></a>Bemerkungen

Der zurückgegebene Attribut Name kann in Verbindung mit **getiteminfo** verwendet werden, um den Wert für ein bestimmtes benanntes Attribut abzurufen.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

**Windows Media Player 10 Mobile:** Attribute für ein Medien Element sind nur während der Wiedergabe verfügbar, es sei denn, Sie werden über die Medien Auflistung aus dem Element abgerufen.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel werden *Medien* verwendet. **GetAttributeName** zum Ausfüllen eines HTML-Text Bereichs namens MyText mit dem Index und dem Namen der einzelnen Attribute für das aktuelle Medien Element. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Get the number of attributes for the current media. 
var atCount = cm.attributeCount;

// Loop through the attribute list.
for(var i=0; i < atCount; i++){
   
   // Print each attribute index and name.   
   myText.value += "Attribute " + i +": ";
   myText.value += cm.getAttributeName(i);
   myText.value += "\n";
}

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media. AttributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getiteminfo**](media-getiteminfo.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





