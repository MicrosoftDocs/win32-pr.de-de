---
title: Mediacollection. GetAll-Methode
description: Die GetAll-Methode ruft eine Wiedergabeliste ab, die alle Medienelemente in der Bibliothek enthält.
ms.assetid: c22532ee-5714-4762-966f-7dc6543384f4
keywords:
- GetAll-Methoden Fenster Media Player
- GetAll-Methode, Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, GetAll-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getAll
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1681cd533be4084123cb80cdcc199ab5e1ce2981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373868"
---
# <a name="mediacollectiongetall-method"></a>Mediacollection. GetAll-Methode

Die **GetAll** -Methode ruft eine Wiedergabeliste ab, die alle Medienelemente in der Bibliothek enthält.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.getAll()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *mediacollection* verwendet. **GetAll** zum Zufalls Spiel der Medienelemente aus der Mediensammlung. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Store the count of all media items in the media collection.
var count = Player.mediaCollection.getAll().count;

// Generate a random number using the media count.
var rand = Math.random() * count;

// Round down the random number to the nearest integer.
rand = Math.floor(rand);

// Make the random media item the current media item.
Player.currentMedia = Player.mediaCollection.getAll().item(rand);

// Play the media item.
// Player.controls.play();

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

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





