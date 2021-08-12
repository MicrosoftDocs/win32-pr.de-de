---
title: Network.setProxySettings-Methode
description: Die setProxySettings-Methode gibt die Proxyeinstellung für ein bestimmtes Protokoll an.
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- setProxySettings-Windows Media Player
- setProxySettings-Methode Windows Media Player , Network-Klasse
- Netzwerkklasse Windows Media Player , setProxySettings-Methode
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
ms.openlocfilehash: 6501d097a4ec342c2831e4b72bf8f17edc4e4e1bec02b2b51cd7840325674b88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573858"
---
# <a name="networksetproxysettings-method"></a>Network.setProxySettings-Methode

Die **setProxySettings-Methode** gibt die Proxyeinstellung für ein bestimmtes Protokoll an.

## <a name="syntax"></a>Syntax


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Protocol* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Protokollnamen angibt. Eine Liste der unterstützten Protokolle finden Sie unter [Unterstützte Protokolle und Dateitypen.](supported-protocols-and-file-types.md)

</dd> <dt>

*Einstellung* \[ In\]
</dt> <dd>

**Number** (**long**), die einen der folgenden Werte enthält.



| Wert | Beschreibung                                                          |
|-------|----------------------------------------------------------------------|
| 0     | Verwenden Sie keinen Proxyserver.                                           |
| 1     | Verwenden Sie die Proxyeinstellungen des aktuellen Browsers (nur für HTTP gültig). |
| 2     | Verwenden Sie die manuell angegebenen Proxyeinstellungen.                           |
| 3     | Automatische Erkennung der Proxyeinstellungen.                                      |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode schlägt fehl, es sei denn, die aufrufende Anwendung wird auf dem lokalen Computer oder Intranet ausgeführt.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird JScript mit einem HTML SELECT-Element verwendet, damit der Benutzer die Windows Media Player **proxy-Einstellung für das HTTP-Protokoll angeben kann. Das Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerkobjekt**](network-object.md)
</dt> </dl>

 

 





