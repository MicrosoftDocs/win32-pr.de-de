---
title: Network. getproxybypassforlocal-Methode
description: Die getproxybypassforlocal-Methode ruft einen Wert ab, der angibt, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- getproxybypassforlocal-Methode, Windows Media Player
- getproxybypassforlocal-Methode, Windows Media Player, Network-Klasse
- Netzwerk Klasse, Windows Media Player, getproxybypassforlocal-Methode
topic_type:
- apiref
api_name:
- Network.getProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60b9248cd5a893496c2de88c5a5370dfb7bf82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370062"
---
# <a name="networkgetproxybypassforlocal-method"></a>Network. getproxybypassforlocal-Methode

Die **getproxybypassforlocal** -Methode ruft einen Wert ab, der angibt, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = Network.getProxyBypassForLocal(
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

Diese Methode gibt einen **booleschen** Wert zurück, der angibt, ob der Proxy Server umgangen wird. Der zurückgegebene Wert ist nur dann von Bedeutung, wenn **getproxysettings** den Wert 2 zurückgibt (manuelle Einstellungen verwenden).

## <a name="remarks"></a>Bemerkungen

Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **getproxybypassforlocal** , um anzuzeigen, ob die Windows-Media Player so festgelegt ist, dass der Proxy Server für lokale Adressen umgangen wird. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy bypass for local value for HTTP.
   var proxyBypassForLocalHTTP = Player.network.getProxyBypassForLocal("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy bypass for local value for MMS.
   var proxyBypassForLocalMMS = Player.network.getProxyBypassForLocal("MMS");

// Display the proxy bypass for local values in the browser client area.
// Unavailable proxy bypass for local values will display as "undefined".
document.write("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP);
document.write("<BR>");
document.write("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS);

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerk Objekt**](network-object.md)
</dt> <dt>

[**Network. getproxysettings**](network-getproxysettings.md)
</dt> </dl>

 

 





