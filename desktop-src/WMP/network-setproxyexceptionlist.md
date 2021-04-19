---
title: Network. setproxyexceptionlist-Methode
description: Die setproxyexceptionlist-Methode gibt die Proxy Ausnahmeliste an. | Network. setproxyexceptionlist-Methode
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- setproxyexceptionlist-Methode, Windows Media Player
- setproxyexceptionlist-Methode, Windows Media Player, Netzwerk Klasse
- Netzwerk Klassen-Windows-Media Player, setproxyexceptionlist-Methode
topic_type:
- apiref
api_name:
- Network.setProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1e48aa91ec4857181de5c607a586da42d6f2cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369932"
---
# <a name="networksetproxyexceptionlist-method"></a>Network. setproxyexceptionlist-Methode

Die **setproxyexceptionlist** -Methode gibt die Proxy Ausnahmeliste an.

## <a name="syntax"></a>Syntax


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Protokoll* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen des Protokolls angibt. Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).

</dd> <dt>

*Liste* \[ in\]
</dt> <dd>

Eine **Zeichenfolge** , die eine durch Semikolons getrennte Liste von Hosts angibt, für die der Proxy Server umgangen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dies ist eine Liste von Computern, Domänen und/oder Adressen, die den Proxy Server umgehen, wenn der Hostteil der Ziel-URL mit einem Eintrag in der Liste übereinstimmt.

Das \* Zeichen kann als Platzhalter für das Auflisten von Einträgen verwendet werden. Beispielsweise \* entspricht ". com" allen Hosts in der com-Domäne, und 67. \* entspricht allen Hosts in der 67-Klasse einem Subnetz.

Diese Methode hat keine Auswirkung, es sei denn, **getproxysettings** gibt den Wert 2 zurück (manuelle Einstellungen verwenden).

Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **setproxyexceptionlist** zum Angeben einer Liste von Hosts, für die der Proxy Server bei Verwendung des MMS-Protokolls umgangen wird. Die neue Liste wird aus einem HTML-Text Element mit ID = "xList" abgerufen. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the user's new exception list.
   var proxyxlist = XLIST.value;

   // Set the exception list.
   Player.network.setProxyExceptionList("MMS", proxyxlist);
}

else

// Warn that the proxy settings must be set to 2.
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

 

 





