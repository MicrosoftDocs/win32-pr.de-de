---
title: Mediacollection. IsDeleted-Methode
description: Die IsDeleted-Methode ruft einen Wert ab, der angibt, ob sich das angegebene Medien Element im Ordner "Gelöschte Elemente" befindet.
ms.assetid: bb3ce9c9-9e43-45a5-8802-dc6783cf2ad7
keywords:
- IsDeleted-Methode (Windows Media Player)
- IsDeleted-Methode, Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, IsDeleted-Methode
topic_type:
- apiref
api_name:
- MediaCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3cdc27c84c88eb65df5b7635f34c79c1b4fe82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352946"
---
# <a name="mediacollectionisdeleted-method"></a>Mediacollection. IsDeleted-Methode

Die **isDeleted** -Methode ruft einen Wert ab, der angibt, ob sich das angegebene Medien Element im Ordner "Gelöschte Elemente" befindet.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = MediaCollection.isDeleted(
  item
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Element* \[ in\]
</dt> <dd>

**Medien** Objekt, das möglicherweise gelöscht wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen** Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

**Windows Media Player 10 Mobile:** Diese Methode gibt immer **false** zurück.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *mediacollection* verwendet. **isDeleted** zum Testen, ob ein bestimmtes Medien Element, das in der Variablen mit dem Namen mediaobject gespeichert ist, im Ordner Gelöschte Elemente ist. Wenn das Medien Element nicht bereits gelöscht wurde, wird es in den Ordner Gelöschte Elemente verschoben. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The media item is available to be deleted, move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Media item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0, Windows Media Player Version 7,1 oder Windows Media Player für Windows XP. Diese Methode wird für Windows Media Player 9-Serie oder höher nicht unterstützt.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Mediacollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Mediacollection. SetDeleted**](mediacollection-setdeleted.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





