---
title: Media. isread onlyitem-Methode
description: Die isread onlyitem-Methode gibt einen Wert zurück, der angibt, ob das angegebene Attribut des Medien Elements bearbeitet werden kann.
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- isread onlyitem-Methode, Windows Media Player
- isleseronlyitem-Methode, Windows Media Player, Medienklasse
- Media Class Windows Media Player, isumonlyitem-Methode
topic_type:
- apiref
api_name:
- Media.isReadOnlyItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ac5bb8d445c3ba6418be4ee5c0c5e7a96f507d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106363199"
---
# <a name="mediaisreadonlyitem-method"></a>Media. isread onlyitem-Methode

Die **isread onlyitem** -Methode gibt einen Wert zurück, der angibt, ob das angegebene Attribut des Medien Elements bearbeitet werden kann.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Attribut* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen des zu testenden Attributs angibt. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen** Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn ein Attribut schreibgeschützt ist, kann es nicht mit der **setiteminfo** -Methode festgelegt werden. Beachten Sie, dass diese Methode möglicherweise unterschiedliche Werte für ein bestimmtes Attribut zurückgibt, wenn Sie mit verschiedenen Versionen von Windows Media Player verwendet wird.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer **true** zurück.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel werden *Medien* verwendet. " **isinfoonlyitem** ", um ein HTML-TEXTAREA-Element mit dem Namen "rwtext" mit Informationen zum aktuellen Medien Element auszufüllen. Der Code gibt jedes Attribut des aktuellen Medien Elements zusammen mit Text aus, der angibt, ob das Attribut schreibgeschützt ist oder Lese-/Schreibzugriff hat. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Store the current media item object.
var cm = Player.currentMedia;

// Create a variable to hold each attribute name.
var atName;

// Loop through the attribute list.
for(var i = 0; i < cm.attributeCount; i++){

   // Get the attribute name.
   atName = cm.getAttributeName(i);

   // Test whether the attribute is read-only.
   var test = ((cm.isReadOnlyItem(atName))?"Read-Only":"Read/Write");

// Print the attribute information to the text area.
   rwText.value += atName + " is " + test;
   rwText.value += "\n";
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

[**"Media. mentiteminfo"**](media-setiteminfo.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





