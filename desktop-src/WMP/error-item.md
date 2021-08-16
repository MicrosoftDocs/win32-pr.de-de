---
title: Error.item-Methode
description: Die item-Methode ruft ein ErrorItem-Objekt aus der Fehlerwarteschlange ab.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- item-Methode Windows Media Player
- item-Methode Windows Media Player , Error-Klasse
- Error-Klasse Windows Media Player , Item-Methode
topic_type:
- apiref
api_name:
- Error.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fbd9f402a659af27db42c34cb0c58e2097270b73eb0eeff382544979dc0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339695"
---
# <a name="erroritem-method"></a>Error.item-Methode

Die **item-Methode** ruft ein **ErrorItem-Objekt** aus der Fehlerwarteschlange ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

**Number** (**long**), die den Index des abzurufenden **ErrorItem-Objekts** enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **ErrorItem-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Windows Media Player können eine Reihe von Fehlern als Reaktion auf eine Fehlerbedingung generieren. Diese Methode ermöglicht das Abrufen eines bestimmten Fehlers in der Warteschlange mithilfe einer Indexnummer. Die Indexnummern für die Fehlerwarteschlange beginnen mit 0 (null).

Sie sollten *Einstellungen* festlegen. **enableErrorDialogs** wird auf FALSE festgelegt, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird der *Fehler* verwendet. **Elementobjekt** in einem Ereignishandler, um den Benutzer vor dem letzten Fehler zu warnen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<SCRIPT LANGUAGE="JScript"  FOR=Player EVENT=error()>

// Store the most recent error item number.
var max = Player.error.errorCount - 1 

// Store the most recent error in an error item object.
var errItem = Player.error.item(max);

// Use the error item object to store the error info.
errDesc = errItem.errorDescription;
errNum = errItem.errorCode;

// Display the error info.
alert(errNum + "\n" + errDesc);

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
</dt> <dt>

[**ErrorItem-Objekt**](erroritem-object.md)
</dt> </dl>

 

 





