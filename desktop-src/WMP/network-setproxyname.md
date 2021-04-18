---
title: Network. setproxyname-Methode
description: Die setproxyname-Methode gibt den Namen des zu verwendenden Proxy Servers an. | Network. setproxyname-Methode
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- setproxyname-Methode, Windows Media Player
- setproxyname-Methode, Windows Media Player, Netzwerk Klasse
- Netzwerk Klasse, Windows Media Player, setproxyname-Methode
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
ms.openlocfilehash: 5a34546a395d48e939c71a806d8125150fca0ff4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371169"
---
# <a name="networksetproxyname-method"></a>Network. setproxyname-Methode

Die **setproxyname** -Methode gibt den Namen des zu verwendenden Proxy Servers an.

## <a name="syntax"></a>Syntax


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Protokoll* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen des Protokolls angibt. Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).

</dd> <dt>

*Name* \[ in\]
</dt> <dd>

Eine **Zeichenfolge** , die den Namen des zu verwendenden Proxy Servers angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode hat keine Auswirkung, es sei denn, **getproxysettings** gibt den Wert 2 zurück (manuelle Einstellungen verwenden).

Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **setproxyname** , um den Namen des Windows Media Player-Proxy Servers für das MMS-Protokoll anzugeben. Der neue Name wird von einem HTML-Text Element mit der ID "Name" abgerufen. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerk Objekt**](network-object.md)
</dt> </dl>

 

 





