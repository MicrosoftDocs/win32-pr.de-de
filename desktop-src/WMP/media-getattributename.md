---
title: Media.getAttributeName-Methode
description: Die getAttributeName-Methode ruft den Namen des Attributs ab, das dem angegebenen Index entspricht.
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- getAttributeName-Windows Media Player
- getAttributeName-Methode Windows Media Player , Media-Klasse
- Medienklasse Windows Media Player , getAttributeName-Methode
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
ms.openlocfilehash: 9b6b9a288830283b3711c6e4eb652be968979628af48d2ce5b718150b9018568
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123430"
---
# <a name="mediagetattributename-method"></a>Media.getAttributeName-Methode

Die **getAttributeName-Methode** ruft den Namen des Attributs ab, das dem angegebenen Index entspricht.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

**Number** (**long**), die den Index des Attributs enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge zurück,** die den Namen des Attributs angibt.

## <a name="remarks"></a>Hinweise

Der zurückgegebene Attributname kann in Verbindung mit **getItemInfo** verwendet werden, um den Wert für ein bestimmtes benanntes Attribut abzurufen.

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Informationen zu den attributes, die von Windows Media Player unterstützt werden, finden Sie in Windows Media Player [Attribute Reference](attribute-reference.md)..

**Windows Media Player 10 Mobile:** Attribute für ein Medienelement sind nur während der Wiedergabe verfügbar, es sei denn, sie werden über die Mediensammlung aus dem Element abgerufen.

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Media *verwendet.* **getAttributeName,** um einen HTML-Textbereich namens myText mit dem Index und Namen jedes Attributs für das aktuelle Medienelement zu füllen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media.attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





