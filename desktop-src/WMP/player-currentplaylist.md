---
title: Player.currentPlaylist
description: Die currentPlaylist-Eigenschaft gibt das aktuelle Playlist-Objekt an oder ruft es ab.
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- Player.currentPlaylist-Windows Media Player
topic_type:
- apiref
api_name:
- Player.currentPlaylist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7139c567eab5fbb3c324916dec260d34f57429cb50bb99d199f35be8aee7a1c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573215"
---
# <a name="playercurrentplaylist"></a>Player.currentPlaylist

Die currentPlaylist-Eigenschaft gibt das aktuelle Playlist-Objekt an oder **ruft es** ab.

## <a name="syntax"></a>Syntax

*Player* . **currentPlaylist**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein  Wiedergabelistenobjekt mit Lese-/Schreibzugriff.

## <a name="remarks"></a>Hinweise

Wenn der *Einstellungen.* **Die autoStart-Eigenschaft** ist true. Die Wiedergabe beginnt automatisch, wenn Sie **currentPlaylist festlegen.**

Diese Eigenschaft verwendet ein Playlist-Objekt, das auf verschiedene Weise erworben werden kann, z. B. durch Aufrufen von *PlaylistArray*. **item** oder *PlaylistCollection*. **newPlaylist**. Um ein **Wiedergabelistenelement** mithilfe eines Dateinamens zu laden, legen Sie die URL-Eigenschaft fest, oder verwenden Sie *Player*. **newPlaylist**.

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird die erste Wiedergabeliste in der Bibliothek abgerufen. Anschließend wird **currentPlaylist verwendet,** um die abgerufene Wiedergabeliste zur aktuellen Wiedergabeliste zu machen und dann den Namen der aktuellen Wiedergabeliste anzuzeigen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
// Retrieve the first playlist from the library.
var firstPL = Player.playlistCollection.getAll().item(0);

// Make the retrieved playlist the current playlist.
Player.currentPlaylist = firstPL;

// Display the name of the current playlist.
document.write("Found first playlist. Name: " + Player.currentPlaylist.name);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player.newPlaylist**](player-newplaylist.md)
</dt> <dt>

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> <dt>

[**PlaylistArray.item**](playlistarray-item.md)
</dt> <dt>

[**PlaylistCollection.newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Einstellungen.autoStart**](settings-autostart.md)
</dt> </dl>

 

 





