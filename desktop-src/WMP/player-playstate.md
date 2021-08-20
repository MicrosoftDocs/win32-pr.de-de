---
title: Player.playState
description: Die playState-Eigenschaft ruft einen Wert ab, der den Zustand des Windows Media Player angibt.
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- Player.playState-Windows Media Player
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
ms.openlocfilehash: 0241f8ab538e985a64835065e1eb6bca0a831164cd66fbb7d9166724a72680e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118835119"
---
# <a name="playerplaystate"></a>Player.playState

Die **playState-Eigenschaft** ruft einen Wert ab, der den Zustand des Windows Media Player angibt.

## <a name="syntax"></a>Syntax

*Player* . **playState**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**). Die Enumerationskonst constant im C-Stil kann abgeleitet werden, indem dem Zustandswert "wmpps" vorangestellt wird. Die Konstante für den Wiedergabezustand ist z. B. **wmppsPlaying.**



| Wert | State         | Beschreibung                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| 0     | Nicht definiert     | Windows Media Player befindet sich in einem nicht definierten Zustand.                                                                              |
| 1     | Beendet       | Die Wiedergabe des aktuellen Medienelements wird beendet.                                                                              |
| 2     | Angehalten        | Die Wiedergabe des aktuellen Medienelements wird angehalten. Wenn ein Medienelement angehalten wird, beginnt das Fortsetzen der Wiedergabe an derselben Position. |
| 3     | Wiedergabe       | Das aktuelle Medienelement wird abspielt.                                                                                          |
| 4     | ScanForward   | Das aktuelle Medienelement ist die schnelle Weiterleitung.                                                                                  |
| 5     | ScanReverse   | Das aktuelle Medienelement wird schnell zurücklädt.                                                                                   |
| 6     | Pufferung     | Das aktuelle Medienelement bekommt zusätzliche Daten vom Server.                                                          |
| 7     | Wartend       | Die Verbindung wird hergestellt, aber der Server sendet keine Daten. Warten auf den Beginn der Sitzung.                                |
| 8     | MediaEnded    | Die Wiedergabe des Medienelements wurde abgeschlossen.                                                                                          |
| 9     | Im Übergang | Vorbereiten eines neuen Medienelements.                                                                                                   |
| 10    | Bereit         | Bereit, mit der Wiedergabe zu beginnen.                                                                                                     |
| 11    | Wiederherstellen  | Erneutes Herstellen einer Verbindung mit dem Stream.                                                                                                     |



 

## <a name="remarks"></a>Hinweise

Windows Media Player, dass Zustände nicht in einer bestimmten Reihenfolge auftreten. Darüber hinaus tritt nicht jeder Zustand notwendigerweise während einer Abfolge von Ereignissen auf. Sie sollten keinen Code schreiben, der von der Zustandsordnung abhängig ist.

## <a name="examples"></a>Beispiele

Der folgende JScript zeigt die Verwendung des *Players*. **playState-Eigenschaft.** Ein HTML-Textelement mit dem Namen "myText" zeigt den aktuellen Status an. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player.PlayStateChange-Ereignis**](player-player-playstatechange.md)
</dt> </dl>

 

 





