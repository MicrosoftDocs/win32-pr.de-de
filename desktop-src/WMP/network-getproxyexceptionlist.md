---
title: Network.getProxyExceptionList-Methode
description: Die getProxyExceptionList-Methode ruft die Proxyausnahmeliste ab.
ms.assetid: f81d8c0f-cc75-470c-9c24-ceaf8a4b6f97
keywords:
- getProxyExceptionList-Windows Media Player
- getProxyExceptionList-Methode Windows Media Player , Network-Klasse
- Netzwerkklasse Windows Media Player , getProxyExceptionList-Methode
topic_type:
- apiref
api_name:
- Network.getProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2becc6c74a5ada575f1bfa85473bd3204bf53a4a739640149cffdd57e3facf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054572"
---
# <a name="networkgetproxyexceptionlist-method"></a>Network.getProxyExceptionList-Methode

Die **getProxyExceptionList-Methode** ruft die Proxyausnahmeliste ab.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = Network.getProxyExceptionList(
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

Diese Methode gibt eine **Zeichenfolge** zurück, die eine durch Semikolons getrennte Liste von Hosts angibt, für die der Proxyserver umgangen wird. Der zurückgegebene Wert ist nur sinnvoll, **wenn getProxySettings** den Wert 2 zurückgibt (verwenden Sie manuelle Einstellungen).

## <a name="remarks"></a>Hinweise

Dies ist eine Liste von Computern, Domänen und/oder Adressen, die den Proxyserver umgehen, wenn der Hostteil der Ziel-URL einem Eintrag in der Liste entspricht.

Das \* Zeichen kann als Platzhalter für das Auflisten von Einträgen verwendet werden. .com würde z. B. mit allen Hosts in der Com-Domäne übereinstimmen, während 67. mit allen Hosts \* \* im Subnetz der 67-Klasse A übereinstimmen würde.

Diese Methode schlägt fehl, es sei denn, die aufrufende Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Netzwerk *verwendet.* **getProxyExceptionList,** um die Listen der umgangenen Proxys für die MMS- und HTTP-Protokolle anzuzeigen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy exception list for HTTP.
   var proxyExceptionListHTTP = Player.network.getProxyExceptionList("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy exception list for MMS.
   var proxyExceptionListMMS = Player.network.getProxyExceptionList("MMS");

// Display the proxy exception lists in the browser client area.
// Unavailable proxy exception lists will display as "undefined".
document.write("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
document.write("<BR>");
document.write("The current MMS proxy exception list: " + proxyExceptionListMMS);

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

 

 





