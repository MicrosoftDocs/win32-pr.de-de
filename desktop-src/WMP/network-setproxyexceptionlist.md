---
title: Network.setProxyExceptionList-Methode
description: Die setProxyExceptionList-Methode gibt die Proxyausnahmeliste an. | Network.setProxyExceptionList-Methode
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- setProxyExceptionList-Windows Media Player
- setProxyExceptionList-Methode Windows Media Player , Network-Klasse
- Netzwerkklasse Windows Media Player , setProxyExceptionList-Methode
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
ms.openlocfilehash: cf72d9c35778e965021ec31671e4e345ec2d8e281d18f9fcb16c8f2ff04d4722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647300"
---
# <a name="networksetproxyexceptionlist-method"></a>Network.setProxyExceptionList-Methode

Die **setProxyExceptionList-Methode** gibt die Proxyausnahmeliste an.

## <a name="syntax"></a>Syntax


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Protocol* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Protokollnamen angibt. Eine Liste der unterstützten Protokolle finden Sie unter [Unterstützte Protokolle und Dateitypen.](supported-protocols-and-file-types.md)

</dd> <dt>

*list* \[ In\]
</dt> <dd>

**Eine** Zeichenfolge, die eine durch Semikolons getrennte Liste von Hosts angibt, für die der Proxyserver umgangen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dies ist eine Liste von Computern, Domänen und/oder Adressen, die den Proxyserver umgehen, wenn der Hostteil der Ziel-URL einem Eintrag in der Liste entspricht.

Das \* Zeichen kann als Platzhalter für das Auflisten von Einträgen verwendet werden. Beispielsweise würde .com mit allen Hosts in der Com-Domäne übereinstimmen, während 67. mit allen Hosts \* \* im Subnetz der 67-Klasse A übereinstimmen würde.

Diese Methode hat keine Auswirkungen, es **sei denn, getProxySettings** gibt den Wert 2 zurück (verwenden Sie manuelle Einstellungen).

Diese Methode schlägt fehl, es sei denn, die aufrufende Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Netzwerk *verwendet.* **setProxyExceptionList,** um eine Liste von Hosts anzugeben, für die der Proxyserver umgangen wird, wenn das MMS-Protokoll verwendet wird. Die neue Liste wird aus einem HTML-TEXT-Element mit der ID = "XLIST" abgerufen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerkobjekt**](network-object.md)
</dt> </dl>

 

 





