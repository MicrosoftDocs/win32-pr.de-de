---
title: Network.setProxyName-Methode
description: Die setProxyName-Methode gibt den Namen des zu verwendenden Proxyservers an. | Network.setProxyName-Methode
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- setProxyName-Windows Media Player
- setProxyName-Methode Windows Media Player , Network-Klasse
- Netzwerkklasse Windows Media Player , setProxyName-Methode
topic_type:
- apiref
api_name:
- Network.setProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9831b25e37fd6e19b70c1ee2589736394560c97f841b5d18c3a128a82997cc6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134923"
---
# <a name="networksetproxyname-method"></a>Network.setProxyName-Methode

Die **setProxyName-Methode** gibt den Namen des zu verwendenden Proxyservers an.

## <a name="syntax"></a>Syntax


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Protocol* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Protokollnamen angibt. Eine Liste der unterstützten Protokolle finden Sie unter [Unterstützte Protokolle und Dateitypen.](supported-protocols-and-file-types.md)

</dd> <dt>

*Name* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Namen des zu verwendenden Proxyservers angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode hat keine Auswirkungen, es **sei denn, getProxySettings** gibt den Wert 2 zurück (verwenden Sie manuelle Einstellungen).

Diese Methode schlägt fehl, es sei denn, die aufrufende Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Netzwerk *verwendet.* **setProxyName,** um den Namen des Windows Media Player Proxyservers für das MMS-Protokoll anzugeben. Der neue Name wird aus einem HTML-TEXT-Element mit der ID = "NAME" abgerufen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the new proxy server name specified by the user.
   var proxyname = NAME.value;

   // Set the proxy server name.
   Player.network.setProxyName("MMS", proxyname);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

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

 

 





