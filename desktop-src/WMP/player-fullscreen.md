---
title: Player.fullScreen
description: Die fullScreen-Eigenschaft gibt einen Wert an oder ruft einen Wert ab, der angibt, ob Der Videoinhalt im Vollbildmodus wiedergibt.
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Player.fullScreen-Windows Media Player
topic_type:
- apiref
api_name:
- Player.fullScreen
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f380dcbcaeedddd23c5e6ff42f9750ea8bcd2f552942e19ba7b847e725edc3b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054378"
---
# <a name="playerfullscreen"></a>Player.fullScreen

Die **fullScreen-Eigenschaft** gibt einen Wert an oder ruft einen Wert ab, der angibt, ob Der Videoinhalt im Vollbildmodus wiedergibt.

## <a name="syntax"></a>Syntax

*Player* . **fullScreen**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein boolescher Wert mit **Lese-/Schreibzugriff.**



| Wert | BESCHREIBUNG                                                    |
|-------|----------------------------------------------------------------|
| true  | Videoinhalte werden im Vollbildmodus wiedergerufen.              |
| false | Standard. Videoinhalte werden nicht im Vollbildmodus abgespielt. |



 

## <a name="remarks"></a>Hinweise

Damit der Vollbildmodus beim Einbetten des Windows Media Player-Steuerelements ordnungsgemäß funktioniert, muss der Videoanzeigebereich eine Höhe und Breite von mindestens einem Pixel haben. Wenn **uiMode** auf "mini" oder "full" festgelegt ist, muss die Höhe des Steuerelements selbst 65 oder höher sein, um den Videoanzeigebereich zusätzlich zur Benutzeroberfläche aufnehmen zu können.

Wenn **uiMode** auf "invisible" festgelegt ist, löst das Festlegen dieser Eigenschaft auf TRUE einen Fehler aus und wirkt sich nicht auf das Verhalten des Steuerelements aus.

Während der Vollbildwiedergabe blendet Windows Media Player Mauscursor aus, wenn **enableContextMenu** gleich false und **uiMode** gleich "none" ist.

Wenn **uiMode** auf "full" oder "mini" festgelegt ist, zeigt Windows Media Player Transportsteuerelemente im Vollbildmodus an, wenn sich der Mauszeiger bewegt. Nach einem kurzen Intervall ohne Mausbewegung werden die Transportsteuerelemente ausgeblendet. Wenn **uiMode** auf "none" festgelegt ist, werden keine Steuerelemente im Vollbildmodus angezeigt.

**Hinweis**

Das Anzeigen von Transportsteuerelementen im Vollbildmodus erfordert das Windows XP-Betriebssystem.

Wenn Transportsteuerelemente nicht im Vollbildmodus angezeigt werden, beendet Windows Media Player automatisch den Vollbildmodus, wenn die Wiedergabe beendet wird.

**Hinweis**

Informieren Sie den Benutzer immer darüber, wie er aus dem Vollbildmodus zurückkehren soll.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine HTML-Eingabeschaltfläche erstellt, die *Player verwendet.* **FullScreen** zum Wechseln eines eingebetteten Playerobjekts in den Vollbildmodus. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```
<INPUT type = button 
       value = "Full Screen" 
       name = FSBUTTON
       onclick = "
               /* Check to be sure the player is playing. */
               if (Player.playState == 3) 
                  Player.fullScreen = 'true';
               ">
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





