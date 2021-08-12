---
title: ErrorItem.errorCode
description: Die errorCode-Eigenschaft ruft den aktuellen Fehlercode ab.
ms.assetid: 1495ec34-0995-40c6-bfd0-f3695784e057
keywords:
- ErrorItem.errorCode Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorCode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f426bbaf1092b64cdb3578cb681282c9b27d9d2e2e23a69d50f9c065353ad104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118577704"
---
# <a name="erroritemerrorcode"></a>ErrorItem.errorCode

Die **errorCode-Eigenschaft** ruft den aktuellen Fehlercode ab.

``` syntax
player.error.item(
        index
        ).errorCode
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**).

## <a name="remarks"></a>Hinweise

Legen Sie *Einstellungen* fest. **enableErrorDialogs** wird auf FALSE festgelegt, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *ErrorItem* verwendet. **errorCode** in einem Ereignishandler, um den Fehlercode für den Benutzer anzuzeigen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error code for the first error item.
errNum = Player.error.item(0).errorCode;

// Display the error information.
var message = "Error number: " + errNum);
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ErrorItem-Objekt**](erroritem-object.md)
</dt> <dt>

[**ErrorItem.errorDescription**](erroritem-errordescription.md)
</dt> </dl>

 

 





