---
title: ErrorItem. ErrorCode
description: Die ErrorCode-Eigenschaft ruft den aktuellen Fehlercode ab.
ms.assetid: 1495ec34-0995-40c6-bfd0-f3695784e057
keywords:
- ErrorItem. ErrorCode-Media Player
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
ms.openlocfilehash: 8c934b83b28e510f29b84a45b48bde700968c97b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353820"
---
# <a name="erroritemerrorcode"></a>ErrorItem. ErrorCode

Die **errorCode** -Eigenschaft ruft den aktuellen Fehlercode ab.

``` syntax
player.error.item(
        index
        ).errorCode
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Sie sollten *Einstellungen* festlegen. **enableerrordialogs** auf false, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *ErrorItem* verwendet. **errorCode** in einem Ereignishandler, um dem Benutzer den Fehlercode anzuzeigen. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ErrorItem-Objekt**](erroritem-object.md)
</dt> <dt>

[**ErrorItem. ErrorDescription**](erroritem-errordescription.md)
</dt> </dl>

 

 





