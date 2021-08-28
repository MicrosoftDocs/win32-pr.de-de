---
description: Bestimmt, ob eine bestimmte Hostzeichenfolge in eine IP-Adresse aufgelöst werden kann.
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: isResolvableEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isResolvableEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 580f5400b59a1142de90843e2be26790aef25a9311f7aa6f732aebeef606c701
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899170"
---
# <a name="isresolvableex-function"></a>isResolvableEx-Funktion

Bestimmt, ob eine bestimmte Hostzeichenfolge in eine IP-Adresse aufgelöst werden kann.

## <a name="parameters"></a>Parameter

<dl> <dt>

*host* 
</dt> <dd>

Eine Zeichenfolge, die den HTTP-Host enthält, der für FindProxyForUrl bereitgestellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

TRUE, wenn der Host in eine IPv4- oder IPv6-Adresse aufgelöst werden kann; andernfalls FALSE.

## <a name="examples"></a>Beispiele

``` syntax
isResolvableEx(host);
    true if the hostname can be resolved to and IP address 
```

``` syntax
isResolvableEx(host); 
    false if the hostname cannot be resolved to an IP address 
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IPv6-fähige Proxyhilfs-API-Definitionen](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[IPv6-Erweiterungen für das Navigator-Dateiformat für die automatische Konfiguration](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



