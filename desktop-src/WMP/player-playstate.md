---
title: Player. playstate
description: Die playstate-Eigenschaft ruft einen Wert ab, der den Zustand des Windows-Media Player Vorgangs angibt.
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- Player. playstate-Fenster Media Player
topic_type:
- apiref
api_name:
- Player.playState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c442b1be9e1ea15b8a54c2dafc264edf8aeb479
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351306"
---
# <a name="playerplaystate"></a>Player. playstate

Die **playstate** -Eigenschaft ruft einen Wert ab, der den Zustand des Windows-Media Player Vorgangs angibt.

## <a name="syntax"></a>Syntax

*Player* . **playstate**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**). Die Enumerationskonstante im C-Stil kann durch Voranstellen des Zustands Werts mit "wmpps" abgeleitet werden. Beispielsweise ist die Konstante für den Wiedergabe Zustand **wmppsplay**.



| Wert | State         | BESCHREIBUNG                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| 0     | Nicht definiert     | Windows Media Player befindet sich in einem nicht definierten Zustand.                                                                              |
| 1     | Beendet       | Die Wiedergabe des aktuellen Medien Elements wurde beendet.                                                                              |
| 2     | Angehalten        | Die Wiedergabe des aktuellen Medien Elements wurde angehalten. Wenn ein Medien Element angehalten wird, beginnt das Fortsetzen der Wiedergabe am gleichen Speicherort. |
| 3     | Wiedergabe       | Das aktuelle Medien Element wird abgespielt.                                                                                          |
| 4     | Scanforward   | Das aktuelle Medien Element ist eine schnelle Weiterleitung.                                                                                  |
| 5     | Scanreverse   | Das aktuelle Medien Element ist schnelles reaktivieren.                                                                                   |
| 6     | Pufferung     | Das aktuelle Medien Element erhält zusätzliche Daten vom Server.                                                          |
| 7     | Warten       | Die Verbindung wird hergestellt, aber der Server sendet keine Daten. Warten auf das Starten der Sitzung.                                |
| 8     | MediaEnded    | Die Wiedergabe des Medien Elements wurde abgeschlossen.                                                                                          |
| 9     | Im Übergang | Neues Medien Element wird vorbereitet.                                                                                                   |
| 10    | Bereit         | Bereit für die Wiedergabe.                                                                                                     |
| 11    | Verbindung  | Verbindung mit Stream wird wieder hergestellt.                                                                                                     |



 

## <a name="remarks"></a>Bemerkungen

Es ist nicht garantiert, dass Windows-Media Player Zustände in einer bestimmten Reihenfolge auftreten. Außerdem treten nicht alle Zustände notwendigerweise während einer Sequenz von Ereignissen auf. Sie sollten keinen Code schreiben, der auf der Status Reihenfolge basiert.

## <a name="examples"></a>Beispiele

Der folgende JScript-Code zeigt die Verwendung des *Players*. **playstate** -Eigenschaft. Ein HTML-Textelement mit dem Namen "MyText" zeigt den aktuellen Status an. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Test whether Windows Media Player is in the playing state.
if (3 == Player.playState)
    myText.value = "Windows Media Player is playing!";
else
    myText.value = "Windows Media Player is NOT playing!";
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

[**Player. PlayStateChange-Ereignis**](player-player-playstatechange.md)
</dt> </dl>

 

 





