---
description: Ruft die Version der WPAD-Verarbeitungs-Engine ab.
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: getClientVersion-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 33aeb4bd59730c48407220fede0cec0a606614f4a9692cd0e9852d56757a7f9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133213"
---
# <a name="getclientversion-function"></a>getClientVersion-Funktion

Ruft die Version der WPAD-Verarbeitungs-Engine ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*IpAddressList* 
</dt> <dd>

Eine durch Semikolons getrennte Zeichenfolge, die IP-Adressen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Liste sortierter durch Semikolons getrennter IP-Adressen oder eine leere Zeichenfolge, wenn die IP-Adressliste nicht sortiert werden kann.

## <a name="remarks"></a>Hinweise

Derzeit gibt diese Funktion Version 1.0 zurück.

Microsoft hat diese Funktion hinzugefügt, damit IT-Administratoren ihre WPAD-Skripts so aktualisieren können, dass sie unterschiedliche Versionen der WPAD-Verarbeitungs-Engine verwenden, ohne unterbrechungsfrei ihre vorhandene Bereitstellung zu verursachen. Wenn Microsoft beispielsweise der 2.0-Version der WPAD-Engine eine Funktion hinzugefügt hat, können Administratoren die Version überprüfen, bevor sie versuchen, diese Funktion aufzurufen. Dadurch kann das Skript mit dem Client verwendet werden, auf dem die Versionen 1.0 und 2.0 der WPAD-Engine ausgeführt werden.

## <a name="examples"></a>Beispiele

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IPv6-fähige Proxyhilfs-API-Definitionen](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[IPv6-Erweiterungen für das Navigator-Dateiformat für die automatische Konfiguration](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



