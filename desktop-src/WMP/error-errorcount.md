---
title: Error.errorCount
description: Die errorCount-Eigenschaft ruft die Anzahl der Fehler in der Fehlerwarteschlange ab.
ms.assetid: 64d9bb0a-fcc4-401b-a7bd-529e1a517f3b
keywords:
- Error.errorCount Windows Media Player
topic_type:
- apiref
api_name:
- Error.errorCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99275930155724f47b77de4f85905b92de9d7a7eb612ab713d725a16c1239d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339802"
---
# <a name="errorerrorcount"></a>Error.errorCount

Die **errorCount-Eigenschaft** ruft die Anzahl der Fehler in der Fehlerwarteschlange ab.

``` syntax
player.error.errorCount
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**).

## <a name="remarks"></a>Hinweise

Sie sollten *Einstellungen* festlegen. **enableErrorDialogs** wird auf FALSE festgelegt, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *Fehler verwendet.* **errorCount** in einem Ereignishandler, um den Benutzer über den letzten Fehler in der Fehlerwarteschlange zu informieren. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount;

// Get the description of the last error. Error items start at zero,
// so the item index will always be one less than the error count.
var errDesc = Player.error.item(max-1).errorDescription;

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

[**Error-Objekt**](error-object.md)
</dt> </dl>

 

 





