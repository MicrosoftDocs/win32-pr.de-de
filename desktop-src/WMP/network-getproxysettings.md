---
title: Network. getproxysettings-Methode
description: Die getproxysettings-Methode ruft die Proxy Einstellung für ein bestimmtes Protokoll ab.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- getproxysettings-Methode, Windows-Media Player
- getproxysettings-Methode, Windows Media Player, Network-Klasse
- Netzwerk Klassen-Windows Media Player, getproxysettings-Methode
topic_type:
- apiref
api_name:
- Network.getProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44a306fca1e671e7e5b3a89c0da952e5c81ba20e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361928"
---
# <a name="networkgetproxysettings-method"></a>Network. getproxysettings-Methode

Die **getproxysettings** -Methode ruft die Proxy Einstellung für ein bestimmtes Protokoll ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = Network.getProxySettings(
  protocol
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Protokoll* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen des Protokolls angibt. Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**Long**) zurück, die einen der folgenden Werte enthält.



| Wert | BESCHREIBUNG                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | Ein Proxy Server wird nicht verwendet.                                                |
| 1     | Die Proxy Einstellungen für den aktuellen Browser werden verwendet (nur gültig für http). |
| 2     | Die manuell angegebenen Proxy Einstellungen werden verwendet.                            |
| 3     | Die Proxy Einstellungen werden automatisch erkannt.                                      |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **getproxysettings** zum Anzeigen einer Meldung, die Informationen zu den aktuellen Proxy Einstellungen des Players im Browserfenster enthält. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Retrieve a number representing the current proxy settings.
var proxySetting = Player.network.getProxySettings("MMS");

// Display the message the corresponds to the current settings.
switch(proxySetting){

   case 0:
     document.write("A proxy server is not being used");
     break;

   case 1: 
     document.write("The proxy settings for the current browser are being used.");
     break;

   case 2:
     document.write("The manually specified proxy settings are being used.");
     break;

case 3:
     document.write("The proxy settings are being auto-detected.");
     break;

   default:
     document.write("Unable to determine proxy setting, try again.");
}

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerk Objekt**](network-object.md)
</dt> </dl>

 

 





