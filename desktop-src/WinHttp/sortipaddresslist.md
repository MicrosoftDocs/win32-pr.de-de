---
description: Sortiert eine Liste von IP-Adressen.
ms.assetid: 1266d6f3-e9f5-4e6b-9431-7329df156f0a
title: sortIpAddressList-Funktion
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
ms.openlocfilehash: 3144ecf044f832a49dd6aa4d9fabf76ce8e81c79c195ec101d294c432a8081e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562447"
---
# <a name="sortipaddresslist-function"></a>sortIpAddressList-Funktion

Sortiert eine Liste von IP-Adressen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*IpAddressList* 
</dt> <dd>

Eine durch Semikolons getrennte Zeichenfolge, die IP-Adressen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Liste sortierter durch Semikolons getrennter IP-Adressen oder eine leere Zeichenfolge, wenn die IP-Adressliste nicht sortiert werden kann.

## <a name="remarks"></a>Hinweise

FindProxyforURLEx-Implementierer sollten Code hinzufügen, der die Zeichenfolge von durch Semikolons getrennten IP-Adressen in separate Adressen unterbricht.

## <a name="examples"></a>Beispiele

``` syntax
sortIpAddressList(2001:4898:28:3:201:2ff:feea:fc14; 
                  157.59.139.22; 
                  fe80::5efe:157.59.139.22");
    returns "fe80::5efe:157.59.139.22;2001:4898:28:3:201:2ff:feea:fc14;157.59.139.22" 
    A list of sorted IP addresses. If there both IPv6 and IPv4 IP addresses are passed as input to this function, then the sorted IPv6 addresses are followed by sorted IPv4 addresses
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IPv6-fähige Proxyhilfs-API-Definitionen](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[IPv6-Erweiterungen für das Navigator-Dateiformat für die automatische Konfiguration](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



