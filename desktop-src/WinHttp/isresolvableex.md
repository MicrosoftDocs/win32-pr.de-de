---
description: Bestimmt, ob eine angegebene Host Zeichenfolge in eine IP-Adresse aufgelöst werden kann.
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: isresolvableex-Funktion
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
ms.openlocfilehash: 1172aaed93a9fc6cede5ae5393c5dd430613a466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355342"
---
# <a name="isresolvableex-function"></a>isresolvableex-Funktion

Bestimmt, ob eine angegebene Host Zeichenfolge in eine IP-Adresse aufgelöst werden kann.

## <a name="parameters"></a>Parameter

<dl> <dt>

*host* 
</dt> <dd>

Eine Zeichenfolge, die den HTTP-Host enthält, der für FindProxyForURL bereitgestellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

TRUE, wenn der Host in eine IPv4-oder IPv6-Adresse aufgelöst werden kann. andernfalls false.

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

[IPv6-abhängige proxyhilfsobjekts-Definitionen](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[IPv6-Erweiterungen für das Auto-config-Datei Format des Navigators](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



