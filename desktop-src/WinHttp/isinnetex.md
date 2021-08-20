---
description: Bestimmt, ob sich eine IP-Adresse in einem bestimmten Subnetz befindet.
ms.assetid: 2fbfad9c-86b1-44c3-860b-a5c98ac6c2e9
title: isInNetEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isInNetEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3a91555370bada5c4bb9257918d0920ac71ac5475c08201f30bf1fbbb4b95c1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114463"
---
# <a name="isinnetex-function"></a>isInNetEx-Funktion

Bestimmt, ob sich eine IP-Adresse in einem bestimmten Subnetz befindet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*Ipaddress* 
</dt> <dd>

Eine Zeichenfolge, die IPv6/IPv4-Adressen enthält.

</dd> <dt>

*IPprefix* 
</dt> <dd>

Eine Zeichenfolge, die das IP-Präfix mit Doppelpunkttrennzeichen mit den im Bitfeld angegebenen top n Bits enthält (d.h. 3ffe:8311:ffff::/48 oder 123.112.0.0/16).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

TRUE, wenn sich der Host im gleichen Subnetz befindet; andernfalls FALSE.

Gibt auch FALSE zurück, wenn das Präfix nicht im richtigen Format vorkommt oder wenn Adressen und Präfixe verschiedener Typen im Vergleich verwendet werden (d. h. IPv4-Präfix und eine IPv6-Adresse).

## <a name="examples"></a>Beispiele

``` syntax
isInNetEx(host, "198.95.249.79/32");
    true if the IP address of host matches exactly 198.95.249.79
```

``` syntax
isInNetEx(host, "198.95.0.0/16");
    true if the IP address of the host matches 198.95.*.*
```

``` syntax
isInNetEx(host, "3ffe:8311:ffff::/48");
    true if the IP address of the host matches 3ffe:8311:fff:*:*:*:*:*
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IPv6-orientierte Proxy-Hilfs-API-Definitionen](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[IPv6-Erweiterungen für das Navigator-Dateiformat für die automatische Konfiguration](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



