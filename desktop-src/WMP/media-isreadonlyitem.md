---
title: Media.isReadOnlyItem-Methode
description: Die isReadOnlyItem-Methode gibt einen Wert zurück, der angibt, ob das angegebene Attribut des Medienelements bearbeitet werden kann.
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- isReadOnlyItem-Windows Media Player
- isReadOnlyItem-Methode Windows Media Player , Media-Klasse
- Medienklasse Windows Media Player , isReadOnlyItem-Methode
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
ms.openlocfilehash: 501aacb7b9a56fd9780aba75a15aa9f717640ebff7619df020bad432cdffd459
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123390"
---
# <a name="mediaisreadonlyitem-method"></a>Media.isReadOnlyItem-Methode

Die **isReadOnlyItem-Methode** gibt einen Wert zurück, der angibt, ob das angegebene Attribut des Medienelements bearbeitet werden kann.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Attribut* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Namen des zu testenden Attributs angibt. Informationen zu den attributes, die von Windows Media Player unterstützt werden, finden Sie in der Windows Media Player [Attribute Reference](attribute-reference.md)..

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen zurück.**

## <a name="remarks"></a>Hinweise

Wenn ein Attribut schreibgeschützt ist, kann es nicht mit der **setItemInfo-Methode festgelegt** werden. Beachten Sie, dass diese Methode unterschiedliche Werte für ein bestimmtes Attribut zurückgeben kann, wenn sie mit verschiedenen Versionen von Windows Media Player.

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer **true zurück.**

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Media *verwendet.* **isReadOnlyItem,** um ein HTML-TEXTAREA-Element namens rwText mit Informationen zum aktuellen Medienelement zu füllen. Der Code gibt jedes Attribut des aktuellen Medienelements zusammen mit Text aus, der angibt, ob das Attribut schreibgeschützt ist oder gelesen/geschrieben wird. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media.setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





