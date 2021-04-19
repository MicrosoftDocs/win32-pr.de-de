---
title: Player. PlayStateChange-Ereignis
description: Das PlayStateChange-Ereignis tritt auf, wenn die playstate-Eigenschaft geändert wird.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- Media Player "PlayStateChange-Ereignisfenster"
- PlayStateChange-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, PlayStateChange-Ereignis
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
ms.openlocfilehash: e621d8698a5379b0d39a55db141fc0012f6ef969
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356377"
---
# <a name="playerplaystatechange-event"></a>Player. PlayStateChange-Ereignis

Das **PlayStateChange** -Ereignis tritt auf, wenn die **playstate** -Eigenschaft geändert wird.

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

Number (**Long**), der den neuen **playstate** angibt. Eine Tabelle mit möglichen Werten finden Sie unter [playstate](player-playstate.md) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

Es ist nicht garantiert, dass Windows-Media Player Zustände in einer bestimmten Reihenfolge auftreten. Außerdem treten nicht alle Zustände notwendigerweise während einer Sequenz von Ereignissen auf. Sie sollten keinen Code schreiben, der auf der Status Reihenfolge basiert.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Ereignishandler für den *Player* veranschaulicht. **PlayStateChange** -Ereignis. Ein HTML-Textelement mit dem Namen "MyText" zeigt den neuen Wiedergabe Zustand an. Das Player-Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player. playstate**](player-playstate.md)
</dt> </dl>

 

 





