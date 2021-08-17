---
title: Player.Error-Ereignis
description: Das Fehlerereignis tritt auf, wenn eine Fehlerbedingung vorliegt.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Fehlerereignis Windows Media Player
- Error-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , Error-Ereignis
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
ms.openlocfilehash: 6a7e4642eef19b4edc4b1aa5bc75022a307d279d0d60482af0c7e2f0a9368c06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134813"
---
# <a name="playererror-event"></a>Player.Error-Ereignis

Das **Fehlerereignis** tritt auf, wenn eine Fehlerbedingung vorliegt.

## <a name="syntax"></a>Syntax


```JScript
Player.Error()
```



## <a name="parameters"></a>Parameter

Dieses Ereignis verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird ein Ereignishandler erstellt, um den Beschreibungstext für den ersten Fehler in der Fehlerwarteschlange anzuzeigen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ErrorItem.errorDescription**](erroritem-errordescription.md)
</dt> <dt>

[**Error.item**](error-item.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





