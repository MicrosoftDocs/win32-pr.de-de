---
title: Error. clearerrorqueue-Methode
description: Mit der clearerrorqueue-Methode werden die Fehler in der Fehler Warteschlange gelöscht. | Error. clearerrorqueue-Methode
ms.assetid: 306f0700-88b1-4433-8abb-7d225e82060a
keywords:
- clearerrorqueue-Methode, Windows Media Player
- clearerrorqueue-Methode, Windows Media Player, Error-Klasse
- Error-Klasse, Windows Media Player, clearerrorqueue-Methode
topic_type:
- apiref
api_name:
- Error.clearErrorQueue
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b756708b8f0643f86489c26dd921e87c408be8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358054"
---
# <a name="errorclearerrorqueue-method"></a>Error. clearerrorqueue-Methode

Mit der **clearerrorqueue** -Methode werden die Fehler in der Fehler Warteschlange gelöscht.

## <a name="syntax"></a>Syntax


```JScript
Error.clearErrorQueue()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ist nützlich, um die Fehler Warteschlange zu löschen, nachdem eine Reihe von Fehlern verarbeitet wurde.

Sie sollten *Einstellungen* festlegen. **enableerrordialogs** auf false, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird ein *Fehler* verwendet. **clearerrorqueue** in einem Ereignishandler, um die Fehler Warteschlange zu leeren, nachdem alle Fehlerbeschreibungen angezeigt wurden. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount 

// Loop through the list of errors.
for (var i = 0; i < max; i++){
    // Get the error description for this item.
    var errDesc = Player.error.item(i).errorDescription;
    
    // Display the error message.
    alert(errDesc);
}

// Clear the error queue to prepare for the next group of errors.
Player.error.clearErrorQueue();

</SCRIPT>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Error-Objekt**](error-object.md)
</dt> </dl>

 

 





