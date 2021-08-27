---
title: Player.CurrentPlaylistChange-Ereignis
description: Das CurrentPlaylistChange-Ereignis tritt auf, wenn sich etwas innerhalb der aktuellen Wiedergabeliste ändert. | Player.CurrentPlaylistChange-Ereignis
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- CurrentPlaylistChange-Ereignis Windows Media Player
- CurrentPlaylistChange-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , CurrentPlaylistChange-Ereignis
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672ff739e60efe73e1d30670dec5bc956f9fdd56506464b036add6f52cc6fc34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338146"
---
# <a name="playercurrentplaylistchange-event"></a>Player.CurrentPlaylistChange-Ereignis

Das **CurrentPlaylistChange-Ereignis** tritt auf, wenn sich etwas innerhalb der aktuellen Wiedergabeliste ändert.

## <a name="syntax"></a>Syntax


```JScript
Player.CurrentPlaylistChange(
  change
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*change* 
</dt> <dd>

**Number** (**long**), die angibt, welcher Änderungstyp an der Wiedergabeliste aufgetreten ist. Weitere Informationen finden Sie unter *Player*. **PlaylistChange-Ereignis** für eine Tabelle möglicher Werte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieses Ereignis tritt nicht auf, wenn eine andere Wiedergabeliste zur aktuellen Wiedergabeliste wird. Sie tritt nur auf, wenn eine Änderung innerhalb der aktuellen Wiedergabeliste erfolgt, z. B. wenn ein Medienelement an die Wiedergabeliste angefügt wird.

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens in einer importierten JScript-Datei auf eine Methode zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt eingegeben werden, einschließlich Der Groß-/Großschreibung.

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird der Text in einem HTML-DIV-Element namens PlItems aktualisiert, um die Namen der Medienelemente in der aktuellen Wiedergabeliste anzuzeigen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<!-- Create an event handler for current playlist change. -->
<SCRIPT FOR = "Player" EVENT = "currentPlaylistChange(change)">
   switch (change){
      // Only update for move, delete, insert, and append events.
      case 3, 4, 5, 6:

         // Clear the contents of the DIV.
         PlItems.innerHTML = "";

         // Loop through the playlist and display each item name.
         for (var i = 0; i < Player.currentPlaylist.count; i++){
            PlItems.innerHTML += Player.currentPlaylist.item(i).name;
            PlItems.innerHTML += "<br>";
         }
         break;
      
      default:
   } 
</SCRIPT>

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

[**Player.currentPlaylist**](player-currentplaylist.md)
</dt> <dt>

[**Player.PlaylistChange**](player-player-playlistchange.md)
</dt> </dl>

 

 





