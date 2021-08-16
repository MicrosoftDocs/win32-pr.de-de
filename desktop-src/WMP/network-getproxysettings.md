---
title: Network.getProxySettings-Methode
description: Die getProxySettings-Methode ruft die Proxyeinstellung für ein bestimmtes Protokoll ab.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- getProxySettings-Windows Media Player
- getProxySettings-Methode Windows Media Player , Network-Klasse
- Netzwerkklasse Windows Media Player , getProxySettings-Methode
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
ms.openlocfilehash: e142e7366c9e2b03e55dbd3768ee9c4fb41f30266d221a2ac5ac80019d5a7b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647440"
---
# <a name="networkgetproxysettings-method"></a>Network.getProxySettings-Methode

Die **getProxySettings-Methode** ruft die Proxyeinstellung für ein bestimmtes Protokoll ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = Network.getProxySettings(
  protocol
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Protocol* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Protokollnamen angibt. Eine Liste der unterstützten Protokolle finden Sie unter [Unterstützte Protokolle und Dateitypen.](supported-protocols-and-file-types.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**long**) zurück, die einen der folgenden Werte enthält.



| Wert | BESCHREIBUNG                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | Ein Proxyserver wird nicht verwendet.                                                |
| 1     | Die Proxyeinstellungen für den aktuellen Browser werden verwendet (nur für HTTP gültig). |
| 2     | Die manuell angegebenen Proxyeinstellungen werden verwendet.                            |
| 3     | Die Proxyeinstellungen werden automatisch erkannt.                                      |



 

## <a name="remarks"></a>Hinweise

Diese Methode schlägt fehl, es sei denn, die aufrufende Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Netzwerk *verwendet.* **getProxySettings** zum Anzeigen einer Meldung, die Informationen zu den aktuellen Proxyeinstellungen des Players enthält, im Browserfenster. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Netzwerkobjekt**](network-object.md)
</dt> </dl>

 

 





