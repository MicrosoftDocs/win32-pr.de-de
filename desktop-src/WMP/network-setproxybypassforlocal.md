---
title: Network. setproxybypassforlocal-Methode
description: Die setproxybypassforlocal-Methode gibt einen Wert an, der angibt, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.
ms.assetid: 3023a561-f3b7-45c8-a432-baadd795aaa6
keywords:
- setproxybypassforlocal-Methode, Windows Media Player
- setproxybypassforlocal-Methode, Windows Media Player, Netzwerk Klasse
- Netzwerk Klasse Windows Media Player, setproxybypassforlocal-Methode
topic_type:
- apiref
api_name:
- Network.setProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9426c310c8977317cf5a8415fd19966b8dfc8fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361945"
---
# <a name="networksetproxybypassforlocal-method"></a>Network. setproxybypassforlocal-Methode

Die **setproxybypassforlocal** -Methode gibt einen Wert an, der angibt, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.

## <a name="syntax"></a>Syntax


```JScript
Network.setProxyBypassForLocal(
  protocol,
  bypass
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Protokoll* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen des Protokolls angibt. Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).

</dd> <dt>

*Umgehung* \[ in\]
</dt> <dd>

**Boolescher** Wert, der angibt, ob der Proxy Server umgangen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode hat keine Auswirkung, es sei denn, **getproxysettings** gibt den Wert 2 zurück (manuelle Einstellungen verwenden).

Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **setproxybypassforlocal** , um anzugeben, ob der Windows-Media Player Proxyserver bei Verwendung des MMS-Protokolls umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Test whether the proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Prompt the user for a setting. Store the response in a variable.
   var proxybypass = confirm("Bypass proxy server for local addresses? \n OK = Yes \n Cancel = No");

   // Set the proxy bypass value using the user input.
   Player.network.setProxyBypassForLocal("MMS", proxybypass);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

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

 

 





