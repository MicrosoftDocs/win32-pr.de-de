---
title: Player. Currency Change-Ereignis
description: Das Ereignis "Ereignis Ereignisse" tritt auf, wenn sich "Controls. Events Item" ändert.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- Ereignisfenster für das Ereignis Ereignis Media Player
- Ereignis für den Ereignis Wechsel in Windows Media Player, Player-Klasse
- Windows Media Player der Player-Klasse, Ereignis für den Ereignis Wechsel
topic_type:
- apiref
api_name:
- Player.CurrentItemChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c425184bf4b338177ec892ed5362c085dd8cb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371319"
---
# <a name="playercurrentitemchange-event"></a>Player. Currency Change-Ereignis

Das **Ereignis** "Ereignis Ereignisse" tritt auf, wenn-Steuer *Elemente*. das Ereignis **wird geändert.**

## <a name="syntax"></a>Syntax


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a>Parameter

Dieses Ereignis weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird ein Ereignishandler für den *Player* veranschaulicht. Ereignis für die Ereignis Ereignis **Änderung** . Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<!-- Create an HTML text box to display the media item name. -->
<INPUT TYPE="TEXT" NAME="MEDIA">

<!-- Create an event handler. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = currentItemChange()>

   // Display the name of the new media item.
   MEDIA.value = Player.currentMedia.name;

</SCRIPT>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls. happtitem**](controls-currentitem.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





