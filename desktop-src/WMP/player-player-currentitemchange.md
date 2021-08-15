---
title: Player.CurrentItemChange-Ereignis
description: Das CurrentItemChange-Ereignis tritt auf, wenn controls.currentItem geändert wird.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- CurrentItemChange-Ereignis Windows Media Player
- CurrentItemChange-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , CurrentItemChange-Ereignis
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
ms.openlocfilehash: 5ed0ca3c8333c7261c8332bcc124c905c5540f5cdf0dbefe3f34f121eb901cc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338125"
---
# <a name="playercurrentitemchange-event"></a>Player.CurrentItemChange-Ereignis

Das **CurrentItemChange-Ereignis** tritt auf, wenn *Steuert*. **currentItem-Änderungen.**

## <a name="syntax"></a>Syntax


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a>Parameter

Dieses Ereignis verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird ein Ereignishandler für den *Player* veranschaulicht. **currentItemChange-Ereignis.** Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Controls.currentItem**](controls-currentitem.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





