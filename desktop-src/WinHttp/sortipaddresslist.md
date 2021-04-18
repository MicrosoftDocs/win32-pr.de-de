---
description: Sortiert eine Liste von IP-Adressen.
ms.assetid: 1266d6f3-e9f5-4e6b-9431-7329df156f0a
title: menpaddresslist-Funktion
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
ms.openlocfilehash: 600d87a58248aafdef5b0a8a7f284f4094c95780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343632"
---
# <a name="sortipaddresslist-function"></a>menpaddresslist-Funktion

Sortiert eine Liste von IP-Adressen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*Ipaddresslist* 
</dt> <dd>

Eine durch Semikolons getrennte Zeichenfolge, die IP-Adressen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Liste von durch Trennzeichen getrennten, durch Semikola getrennten IP-Adressen oder eine leere Zeichenfolge, wenn die IP-Adressliste nicht sortiert werden kann.

## <a name="remarks"></a>Bemerkungen

Findproxyforurlex-Implementierer sollten Code hinzufügen, der die Zeichenfolge von durch Semikola getrennten IP-Adressen in separate Adressen unterbricht.

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

[IPv6-abhängige proxyhilfsobjekts-Definitionen](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[IPv6-Erweiterungen für das Auto-config-Datei Format des Navigators](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



