---
title: Network.getProxyBypassForLocal-Methode
description: Die getProxyBypassForLocal-Methode ruft einen Wert ab, der angibt, ob der Proxyserver umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- getProxyBypassForLocal-Methode Windows Media Player
- getProxyBypassForLocal-Methode Windows Media Player , Network-Klasse
- Netzwerkklasse Windows Media Player , getProxyBypassForLocal-Methode
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
ms.openlocfilehash: 51f22eb6187938318d95b9dd7a473b58e216315210d4af41c29b352b2654cbf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054558"
---
# <a name="networkgetproxybypassforlocal-method"></a>Network.getProxyBypassForLocal-Methode

Die **getProxyBypassForLocal-Methode** ruft einen Wert ab, der angibt, ob der Proxyserver umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = Network.getProxyBypassForLocal(
  protocol
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Protokoll* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Protokollnamen angibt. Eine Liste der unterstützten Protokolle finden Sie unter [Unterstützte Protokolle und Dateitypen.](supported-protocols-and-file-types.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen Wert** zurück, der angibt, ob der Proxyserver umgangen wird. Der zurückgegebene Wert ist nur sinnvoll, wenn **getProxySettings** den Wert 2 zurückgibt (manuelle Einstellungen verwenden).

## <a name="remarks"></a>Hinweise

Diese Methode schlägt fehl, es sei denn, die aufrufende Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *Network* verwendet. **getProxyBypassForLocal,** um anzuzeigen, ob Windows Media Player so festgelegt ist, dass der Proxyserver für lokale Adressen umgangen wird. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerkobjekt**](network-object.md)
</dt> <dt>

[**Network.getProxySettings**](network-getproxysettings.md)
</dt> </dl>

 

 





