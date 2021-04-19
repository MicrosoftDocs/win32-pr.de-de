---
title: Player. Error-Ereignis
description: Das Fehler Ereignis tritt auf, wenn eine Fehlerbedingung vorliegt.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Fehler Ereignis-Windows-Media Player
- Fehler Ereignis Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, Fehler Ereignis
topic_type:
- apiref
api_name:
- Player.Error
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99411773994ad012155eea5a203ed341d50b460
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355936"
---
# <a name="playererror-event"></a>Player. Error-Ereignis

Das **Fehler** Ereignis tritt auf, wenn eine Fehlerbedingung vorliegt.

## <a name="syntax"></a>Syntax


```JScript
Player.Error()
```



## <a name="parameters"></a>Parameter

Dieses Ereignis weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird ein Ereignishandler erstellt, um den Beschreibungstext für den ersten Fehler in der Fehler Warteschlange anzuzeigen. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the description of the first error. 
var errDesc = Player.error.item(0).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ErrorItem. ErrorDescription**](erroritem-errordescription.md)
</dt> <dt>

[**Error. Item**](error-item.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





