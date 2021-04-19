---
title: Player. currentplaylistchange-Ereignis
description: Das currentplaylistchange-Ereignis tritt auf, wenn sich etwas innerhalb der aktuellen Wiedergabeliste ändert. | Player. currentplaylistchange-Ereignis
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- Currentplaylistchange-Ereignisfenster Media Player
- Currentplaylistchange-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, currentplaylistchange-Ereignis
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
ms.openlocfilehash: 4722db224285587198e3ddb021022ec5d8f2cea6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367615"
---
# <a name="playercurrentplaylistchange-event"></a>Player. currentplaylistchange-Ereignis

Das **currentplaylistchange** -Ereignis tritt auf, wenn sich etwas innerhalb der aktuellen Wiedergabeliste ändert.

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

**Zahl** (**Long**), die angibt, welche Art von Änderung in der Wiedergabeliste aufgetreten ist. Siehe den *Player*. **Playlistchange** -Ereignis für eine Tabelle mit möglichen Werten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis tritt nicht auf, wenn eine andere Wiedergabeliste zur aktuellen Wiedergabeliste wird. Sie tritt nur auf, wenn eine Änderung innerhalb der aktuellen Wiedergabeliste erfolgt, z. b. ein Medien Element, das an die Wiedergabeliste angefügt wird.

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird der Text in einem HTML div-Element mit dem Namen "plitems" aktualisiert, um die Namen der Medienelemente in der aktuellen Wiedergabeliste anzuzeigen. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player. currentwiedergabe**](player-currentplaylist.md)
</dt> <dt>

[**Player. playlistchange**](player-player-playlistchange.md)
</dt> </dl>

 

 





