---
title: Network. setproxyport-Methode
description: Die setproxyport-Methode gibt den zu verwendenden ProxyPort an. | Network. setproxyport-Methode
ms.assetid: 09cfce4a-191c-4596-b678-15d9328d5c53
keywords:
- setproxyport-Methode, Windows Media Player
- setproxyport-Methode, Windows Media Player, Netzwerk Klasse
- Netzwerk Klassen-Windows-Media Player, setproxyport-Methode
topic_type:
- apiref
api_name:
- Network.setProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2438688535e4727688ddbd5d67fd65cbed15864d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370496"
---
# <a name="networksetproxyport-method"></a>Network. setproxyport-Methode

Die **setproxyport** -Methode gibt den zu verwendenden ProxyPort an.

## <a name="syntax"></a>Syntax


```JScript
Network.setProxyPort(
  protocol,
  port
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Protokoll* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen des Protokolls angibt. Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).

</dd> <dt>

*Port* \[ in\]
</dt> <dd>

**Zahl** (**Long**), die den zu verwendenden ProxyPort angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode hat keine Auswirkung, es sei denn, **getproxysettings** gibt den Wert 2 zurück (manuelle Einstellungen verwenden).

Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **setproxyport** , um die Portnummer des Windows-Media Player Proxys für das MMS-Protokoll anzugeben. Die Portnummer wird von einem HTML-Eingabe Element mit ID = "Port" abgerufen. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the port number specified by the user.
   var portnumber = PORT.value;

   // Set the port number for the MMS protocol.
   Player.network.setProxyPort("MMS", portnumber);
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

 

 





