---
title: Error. Item-Methode
description: Die Item-Methode ruft ein ErrorItem-Objekt aus der Fehler Warteschlange ab.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, Fehler Klasse
- Error-Klasse, Windows-Media Player, Element-Methode
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
ms.openlocfilehash: 5545df50fce05ff5a10a5f870d1ec07648434fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364787"
---
# <a name="erroritem-method"></a>Error. Item-Methode

Die **Item** -Methode ruft ein **ErrorItem** -Objekt aus der Fehler Warteschlange ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

**Zahl** (**Long**), die den Index des abzurufenden **ErrorItem** -Objekts enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **ErrorItem** -Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Windows Media Player kann als Reaktion auf eine Fehlerbedingung eine Reihe von Fehlern generieren. Diese Methode ermöglicht das Abrufen eines bestimmten Fehlers in der Warteschlange mithilfe einer Indexnummer. Die Indexnummern für die Fehler Warteschlange beginnen mit 0 (null).

Sie sollten *Einstellungen* festlegen. **enableerrordialogs** auf false, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.

## <a name="examples"></a>Beispiele

Der *Fehler* wird im folgenden JScript-Beispiel verwendet. **Item** -Objekt in einem Ereignishandler, um den Benutzer auf den letzten Fehler aufmerksam zu machen. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Error-Objekt**](error-object.md)
</dt> <dt>

[**ErrorItem-Objekt**](erroritem-object.md)
</dt> </dl>

 

 





