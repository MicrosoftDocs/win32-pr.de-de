---
title: Mediacollection. SetDeleted-Methode
description: Die SetDeleted-Methode verschiebt das angegebene Medien Element in den Ordner "Gelöschte Elemente". | Mediacollection. SetDeleted-Methode
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- SetDeleted-Methoden Fenster Media Player
- SetDeleted-Methode, Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, SetDeleted-Methode
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
ms.openlocfilehash: f545953899883933286f3c38def62d9f254dfdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358360"
---
# <a name="mediacollectionsetdeleted-method"></a>Mediacollection. SetDeleted-Methode

Die **SetDeleted** -Methode verschiebt das angegebene Medien Element in den Ordner "Gelöschte Elemente".

## <a name="syntax"></a>Syntax


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Element* \[ in\]
</dt> <dd>

Das **Medien** Objekt, das verschoben wird.

</dd> <dt>

*true* \[ in\]
</dt> <dd>

Geben Sie diesen Wert immer an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode werden Dateien nicht auf dem Computer des Benutzers entfernt.

Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *mediacollection* verwendet. **SetDeleted** zum Verschieben eines bestimmten Medien Elements, das in der Variablen mit dem Namen "mediaobject" gespeichert ist, in den Ordner "Gelöschte Elemente". Die *mediacollection*. die **isDeleted** -Methode testet zunächst, ob das Element bereits gelöscht wurde. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0, Windows Media Player Version 7,1 oder Windows Media Player für Windows XP. Diese Methode wird für Windows Media Player 9-Serie oder höher nicht unterstützt.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Mediacollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Mediacollection. IsDeleted**](mediacollection-isdeleted.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





