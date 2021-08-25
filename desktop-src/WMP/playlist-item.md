---
title: Playlist.item-Methode
description: Die Item-Methode ruft das Medienelement am angegebenen Index ab.
ms.assetid: a564f6db-ede4-4c85-87ca-0e2539d914c2
keywords:
- item-Methode Windows Media Player
- item-Methode Windows Media Player , Playlist-Klasse
- Playlist-Klasse Windows Media Player , Item-Methode
topic_type:
- apiref
api_name:
- Playlist.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72987feb8438edc50c28bb6349b44c4f43736549c92a293794a6bc728ed7853a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862230"
---
# <a name="playlistitem-method"></a>Playlist.item-Methode

Die **Item-Methode** ruft das Medienelement am angegebenen Index ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = Playlist.item(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

**Number** (**long**), die den Index des abzurufenden Elements enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Media-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *Playlist* verwendet. **Element** zum Abrufen eines Medienelements aus der aktuellen Wiedergabeliste basierend auf einer Benutzerauswahl. Ein SELECT-HTML-Element wurde mit dem Namen "weblist" erstellt und mit den Titeln aus der aktuellen Wiedergabeliste gefüllt. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
// Store the value of the selected item in the list box
// using the selectedIndex property.
var index = weblist.selectedIndex;

// Store the corresponding digital media object from the current playlist.
var listItem = Player.currentPlaylist.item(index);

// Set the URL using the listItem variable.
Player.URL = listItem.sourceURL;

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

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> <dt>

[**Playlist.insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Playlist.removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





