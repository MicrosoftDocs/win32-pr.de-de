---
title: Player. currentwiedergabe
description: Die currentwiedergabe-Eigenschaft gibt das aktuelle Wiedergabelisten Objekt an oder ruft es ab.
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- Player. currentwiedergabe-Fenster Media Player
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
ms.openlocfilehash: ceae33a201086d268942e47496874678ec13f459
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367742"
---
# <a name="playercurrentplaylist"></a>Player. currentwiedergabe

Die currentwiedergabe-Eigenschaft gibt das aktuelle **Wiedergabe** Listen Objekt an oder ruft es ab.

## <a name="syntax"></a>Syntax

*Player* . **currentwiedergabe**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein Lese-/Schreib-Wiedergabe Listen Objekt. 

## <a name="remarks"></a>Bemerkungen

Wenn die *Einstellungen*. die **Autostart** -Eigenschaft ist "true". die Wiedergabe beginnt automatisch, wenn Sie **currentwiedergabe** festlegen.

Diese Eigenschaft nimmt ein Wiedergabelisten Objekt an, das auf verschiedene Weise abgerufen werden kann, z. b. durch Aufrufen von *playlistarray*. **Item** oder *playlistcollection*. **newwiedergabe**. Wenn Sie ein **Wiedergabe** Listenelement mithilfe eines Datei namens laden möchten, legen Sie die URL-Eigenschaft fest oder verwenden *Player*. **newwiedergabe**.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird die erste Wiedergabeliste in der-Bibliothek abgerufen. Anschließend wird **currentwiedergabe** verwendet, um die abgerufene Wiedergabeliste zur aktuellen Wiedergabeliste zu machen, und dann, um den Namen der aktuellen Wiedergabeliste anzuzeigen. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player. newwiedergabe**](player-newplaylist.md)
</dt> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> <dt>

[**Playlistarray. Item**](playlistarray-item.md)
</dt> <dt>

[**Playlistcollection. newwiedergabe**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Einstellungen. Autostart**](settings-autostart.md)
</dt> </dl>

 

 





