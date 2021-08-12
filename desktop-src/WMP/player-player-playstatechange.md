---
title: Player.PlayStateChange-Ereignis
description: Das PlayStateChange-Ereignis tritt auf, wenn die playState-Eigenschaft geändert wird.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- PlayStateChange-Windows Media Player
- PlayStateChange-Ereignis Windows Media Player , Player-Klasse
- Playerklasse Windows Media Player , PlayStateChange-Ereignis
topic_type:
- apiref
api_name:
- Player.PlayStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3995f7373984ae9e3b0e24f9f41390154326cfd87bd8589970dc76520c6efd93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572526"
---
# <a name="playerplaystatechange-event"></a>Player.PlayStateChange-Ereignis

Das **PlayStateChange-Ereignis** tritt auf, wenn die **playState-Eigenschaft geändert** wird.

## <a name="syntax"></a>Syntax


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewState* 
</dt> <dd>

Number (**long**), die den neuen **playState angibt.** Eine Tabelle mit möglichen Werten finden Sie unter [playState.](player-playstate.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens auf eine Methode in einer importierten JScript-Datei zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt typisieren, einschließlich Groß-/Groß-/Schreibanforderungen.

Windows Media Player, dass die Zustände nicht in einer bestimmten Reihenfolge auftreten. Darüber hinaus tritt nicht jeder Zustand notwendigerweise während einer Abfolge von Ereignissen auf. Sie sollten keinen Code schreiben, der von der Zustandsordnung abhängig ist.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Ereignishandler für den *Player veranschaulicht.* **playStateChange-Ereignis.** Ein HTML-Textelement mit dem Namen "myText" zeigt den neuen Wiedergabezustand an. Das Player-Objekt wurde mit der ID = "Player" erstellt.


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = playStateChange(NewState)>

// Test for the player current state, display a message for each.
switch (NewState){
    case 1:
        myText.value = "Stopped";
        break;

    case 2:
        myText.value = "Paused";
        break;

    case 3:
        myText.value = "Playing";
        break;

    // Other cases go here.

    default:
        myText.value = "";
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

[**Player.playState**](player-playstate.md)
</dt> </dl>

 

 





