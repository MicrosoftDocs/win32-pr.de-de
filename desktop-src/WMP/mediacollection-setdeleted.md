---
title: MediaCollection.setDeleted-Methode
description: Die setDeleted-Methode verschiebt das angegebene Medienelement in den Ordner für gelöschte Elemente. | MediaCollection.setDeleted-Methode
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- setDeleted-Methode Windows Media Player
- setDeleted-Methode Windows Media Player , MediaCollection-Klasse
- MediaCollection-Klasse Windows Media Player , setDeleted-Methode
topic_type:
- apiref
api_name:
- MediaCollection.setDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63dcb4c0062acbd5f457cd09b9c1370ff9c4f7683fd8758a4a64ce5f510a6948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647840"
---
# <a name="mediacollectionsetdeleted-method"></a>MediaCollection.setDeleted-Methode

Die **setDeleted-Methode** verschiebt das angegebene Medienelement in den Ordner für gelöschte Elemente.

## <a name="syntax"></a>Syntax


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Element* \[ In\]
</dt> <dd>

**Medienobjekt,** das verschoben wird.

</dd> <dt>

*TRUE* \[ In\]
</dt> <dd>

Geben Sie diesen Wert immer an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode entfernt keine Dateien vom Computer des Benutzers.

Um diese Methode verwenden zu können, ist vollzugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *MediaCollection* verwendet. **setDeleted,** um ein bestimmtes Medienelement, das in der Variablen mit dem Namen mediaObject gespeichert ist, in den Ordner für gelöschte Elemente zu verschieben. Die *MediaCollection*. **die isDeleted-Methode** testet zunächst, ob das Element bereits gelöscht wurde. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The item is available to be deleted; move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0, Windows Media Player Version 7.1 oder Windows Media Player für Windows XP. Diese Methode wird für Windows Media Player 9er Serie oder höher nicht unterstützt.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.isDeleted**](mediacollection-isdeleted.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





