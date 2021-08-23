---
title: MediaCollection.getAll-Methode
description: Die getAll-Methode ruft eine Wiedergabeliste ab, die alle Medienelemente in der Bibliothek enthält.
ms.assetid: c22532ee-5714-4762-966f-7dc6543384f4
keywords:
- getAll-Windows Media Player
- getAll-Methode Windows Media Player , MediaCollection-Klasse
- MediaCollection-Klasse Windows Media Player , getAll-Methode
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
ms.openlocfilehash: c1d3bba961f9400470c16e3d773a5765d389ce05bc23c2e948f0b94c7ad22229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135064"
---
# <a name="mediacollectiongetall-method"></a>MediaCollection.getAll-Methode

Die **getAll-Methode** ruft eine Wiedergabeliste ab, die alle Medienelemente in der Bibliothek enthält.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.getAll()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Playlist-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript *MediaCollection verwendet.* **getAll zum** zufälligen Wiederstellen von Medienelementen aus der Mediensammlung. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





