---
description: Sucht alle IP-Adressen für localhost.
ms.assetid: 47f7d03e-c1a1-4395-9889-01891208fe0f
title: myIPAddressEx-Funktion
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
ms.openlocfilehash: 5db6107c061c845113e91590dab405bdd84cb4741f766abfeef6a1344652f115
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744162"
---
# <a name="myipaddressex-function"></a>myIPAddressEx-Funktion

Sucht alle IP-Adressen für localhost.

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine durch Semikolons getrennte Zeichenfolge, die alle IP-Adressen für localhost (IPv6 und/oder IPv4) enthält, oder eine leere Zeichenfolge, wenn localhost nicht in eine IP-Adresse aufgelöst werden kann.

## <a name="remarks"></a>Hinweise

FindProxyforURLEx-Implementierer sollten Code hinzufügen, der die Zeichenfolge von durch Semikolons getrennten IP-Adressen in separate Adressen unterbricht.

## <a name="examples"></a>Beispiele

``` syntax
myIpAddressEx();
    would return the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71:f5b9:a3b5" 
    if you were running on that host.
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IPv6-fähige Proxyhilfs-API-Definitionen](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[IPv6-Erweiterungen für das Navigator-Dateiformat für die automatische Konfiguration](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



