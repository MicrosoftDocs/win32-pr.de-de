---
title: Network. setproxysettings-Methode
description: Die setproxysettings-Methode gibt die Proxy Einstellung für ein bestimmtes Protokoll an.
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- setproxysettings-Methode, Windows-Media Player
- setproxysettings-Methode, Windows Media Player, Network-Klasse
- Netzwerk Klassen-Windows-Media Player, setproxysettings-Methode
topic_type:
- apiref
api_name:
- Network.setProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f3da665b07f717449721c9fb43a8733cdb6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352871"
---
# <a name="networksetproxysettings-method"></a>Network. setproxysettings-Methode

Die **setproxysettings** -Methode gibt die Proxy Einstellung für ein bestimmtes Protokoll an.

## <a name="syntax"></a>Syntax


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Protokoll* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen des Protokolls angibt. Eine Liste der unterstützten Protokolle finden Sie [unter Unterstützte Protokolle und Dateitypen](supported-protocols-and-file-types.md).

</dd> <dt>

*Einstellung* \[ in\]
</dt> <dd>

**Number** (**Long**), der einen der folgenden Werte enthält.



| Wert | BESCHREIBUNG                                                          |
|-------|----------------------------------------------------------------------|
| 0     | Verwenden Sie keinen Proxy Server.                                           |
| 1     | Verwenden Sie die Proxy Einstellungen des aktuellen Browsers (nur gültig für http). |
| 2     | Verwenden Sie die manuell angegebenen Proxy Einstellungen.                           |
| 3     | Erkennen Sie die Proxy Einstellungen automatisch.                                      |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode schlägt fehl, es sei denn, die aufrufenden Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird JScript mit einem HTML SELECT- **Element verwendet, um dem Benutzer die Angabe der Windows Media Player-Proxy Einstellung für das HTTP-Protokoll zu ermöglichen. Das Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<SELECT ID = HTTPsetproxy  NAME = "HTTPsetproxy"  LANGUAGE="JScript"
        onChange = "
                      /* Store the current selection.*/
                      var setting = this.value;

                      /* Change the proxy setting. */
                      Player.network.setProxySettings('HTTP', setting);
">

<OPTION VALUE=0>Do not use a proxy server
<OPTION VALUE=1>Use the browser settings
<OPTION VALUE=2>Use manual settings
<OPTION VALUE=3>Auto-detect settings

</SELECT>

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

 

 





