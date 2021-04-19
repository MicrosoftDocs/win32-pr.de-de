---
description: Auflösen einer Host Zeichenfolge in Ihre IP-Adresse
ms.assetid: 32d70f10-803b-484d-a9e0-d4c61a8d897f
title: dnsresolveex-Funktion
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
ms.openlocfilehash: 1c63ba3e20653c41864394d9c563c851f2aab5e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356950"
---
# <a name="dnsresolveex-function"></a>dnsresolveex-Funktion

Auflösen einer Host Zeichenfolge in Ihre IP-Adresse

## <a name="parameters"></a>Parameter

<dl> <dt>

*host* 
</dt> <dd>

Eine Zeichenfolge, die den HTTP-Host enthält, der für FindProxyForURL bereitgestellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine durch Semikolons getrennte Zeichenfolge, die IPv6-und IPv4-Adressen enthält, oder eine leere Zeichenfolge, wenn der Host nicht aufgelöst werden kann.

## <a name="remarks"></a>Bemerkungen

Findproxyforurlex-Implementierer sollten Code hinzufügen, der die Zeichenfolge von durch Semikola getrennten IP-Adressen in separate Adressen unterbricht.

## <a name="examples"></a>Beispiele

``` syntax
dnsResolveEx("testmachine1");
    returns the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IPv6-abhängige proxyhilfsobjekts-Definitionen](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[IPv6-Erweiterungen für das Auto-config-Datei Format des Navigators](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



