---
description: Bestimmt, ob sich eine IP-Adresse in einem bestimmten Subnetz befindet.
ms.assetid: 2fbfad9c-86b1-44c3-860b-a5c98ac6c2e9
title: isinnettex-Funktion
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
ms.openlocfilehash: d738fbf5788fbe56d8c801b6c5256e96e8d4a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351034"
---
# <a name="isinnetex-function"></a>isinnettex-Funktion

Bestimmt, ob sich eine IP-Adresse in einem bestimmten Subnetz befindet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*IPAddress* 
</dt> <dd>

Eine Zeichenfolge, die IPv6/IPv4-Adressen enthält.

</dd> <dt>

*Ipprefix* 
</dt> <dd>

Eine Zeichenfolge mit einem durch Trennzeichen getrennten IP-Präfix mit oberen n Bits, die im Bitfeld angegeben sind (z. b. 3FFE: 8311: FFFF::/48 oder 123.112.0.0/16).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

TRUE, wenn sich der Host im gleichen Subnetz befindet. andernfalls false.

Gibt auch false zurück, wenn das Präfix nicht im richtigen Format vorliegt oder wenn Adressen und Präfixe verschiedener Typen im Vergleich verwendet werden (d.h. IPv4-Präfix und eine IPv6-Adresse).

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

[IPv6-abhängige proxyhilfsobjekts-Definitionen](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[IPv6-Erweiterungen für das Auto-config-Datei Format des Navigators](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



