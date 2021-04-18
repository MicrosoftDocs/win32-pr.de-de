---
title: Player. Fullscreen
description: Mit der FullScreen-Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob Videoinhalte im Vollbildmodus wiedergegeben werden.
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Player. Fullscreen-Fenster Media Player
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
ms.openlocfilehash: c3f71b4100c359effd95f79c574a52b5a5bae28c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358243"
---
# <a name="playerfullscreen"></a>Player. Fullscreen

Mit der **Fullscreen** -Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob Videoinhalte im Vollbildmodus wiedergegeben werden.

## <a name="syntax"></a>Syntax

*Player* . **Vollbild**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                                                    |
|-------|----------------------------------------------------------------|
| true  | Video Inhalte werden im Vollbildmodus wiedergegeben.              |
| false | Standard. Video Inhalte werden im Vollbildmodus nicht wiedergegeben. |



 

## <a name="remarks"></a>Bemerkungen

Damit der Vollbildmodus beim Einbetten des Windows Media Player-Steuer Elements ordnungsgemäß funktioniert, muss der Videoanzeige Bereich eine Höhe und Breite von mindestens einem Pixel aufweisen. Wenn **uiMode** auf "Mini" oder "Full" festgelegt ist, muss die Höhe des Steuer Elements auf 65 oder höher festgelegt sein, um zusätzlich zur Benutzeroberfläche den Videoanzeige Bereich aufzunehmen.

Wenn **uiMode** auf "unsichtbar" festgelegt ist, löst das Festlegen dieser Eigenschaft auf true einen Fehler aus und wirkt sich nicht auf das Verhalten des Steuer Elements aus.

Während der Vollbildwiedergabe blendet Windows Media Player den Mauszeiger aus, wenn **enablecontextmenu** den Wert false hat und **uiMode** den Wert "None" hat.

Wenn **uiMode** auf "Full" oder "Mini" festgelegt ist, zeigt Windows Media Player Transport Steuerelemente im Vollbildmodus an, wenn der Mauszeiger bewegt wird. Nach einem kurzen Intervall ohne Mausbewegung werden die Transport Steuerelemente ausgeblendet. Wenn **uiMode** auf "None" festgelegt ist, werden keine Steuerelemente im Vollbildmodus angezeigt.

**Hinweis**

Zum Anzeigen von Transport Steuerelementen im Vollbildmodus ist das Betriebssystem Windows XP erforderlich.

Wenn Transport Steuerelemente nicht im Vollbildmodus angezeigt werden, beendet Windows Media Player den Vollbildmodus automatisch, wenn die Wiedergabe angehalten wird.

**Hinweis**

Stellen Sie sicher, dass Sie den Benutzer darüber informieren, wie Sie den Vollbildmodus zurückgeben.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine HTML-Eingabe Schaltfläche erstellt, die *Player* verwendet. **Vollbild** , um ein eingebettetes Player-Objekt in den Vollbildmodus zu wechseln. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





