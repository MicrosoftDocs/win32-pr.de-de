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
ms.openlocfilehash: 88c205dbd5ce071a809cf87f4f97bb6d42120dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353571"
---
# <a name="myipaddressex-function"></a>myIPAddressEx-Funktion

Sucht alle IP-Adressen für localhost.

## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine durch Semikolons getrennte Zeichenfolge, die alle IP-Adressen für localhost (IPv6 und/oder IPv4) enthält, oder eine leere Zeichenfolge, wenn "localhost" nicht in eine IP-Adresse aufgelöst werden kann.

## <a name="remarks"></a>Bemerkungen

Findproxyforurlex-Implementierer sollten Code hinzufügen, der die Zeichenfolge von durch Semikola getrennten IP-Adressen in separate Adressen unterbricht.

## <a name="examples"></a>Beispiele

``` syntax
myIpAddressEx();
    would return the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71:f5b9:a3b5" 
    if you were running on that host.
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IPv6-abhängige proxyhilfsobjekts-Definitionen](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[IPv6-Erweiterungen für das Auto-config-Datei Format des Navigators](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



