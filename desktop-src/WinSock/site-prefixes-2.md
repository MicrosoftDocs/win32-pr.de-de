---
description: Gibt ein Präfix an, das mit Schnittstelle \# 4 verknüpft ist.
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: IPv6-Site Präfixe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed8a21c59f9b6727c98ccb7fdacf4e9ec6ea5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345102"
---
# <a name="ipv6-site-prefixes"></a>IPv6-Site Präfixe

Der IPv6-RTU-Befehl ermöglicht die Konfiguration veröffentlichter on-Link-Präfixe mit der Präfix Länge eines Standorts. Wenn angegeben, wird die Site Präfix Länge in Routerankündigungen in eine Präfix Informations Option eingefügt. Beispiel:

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

Gibt ein Präfix an, das mit Schnittstelle \# 4 verknüpft ist. Das Präfix wird veröffentlicht. Dies bedeutet, dass es in Routerankündigungen enthalten ist, wenn Schnittstelle \# 4 eine Werbe Schnittstelle ist. Die Gültigkeitsdauer in der Option für die Präfix Informationen beträgt 1800 Sekunden (30 Minuten). Die Präfix Länge der Site in der Option für Präfix Informationen ist 48.

Der Empfang einer Präfix Informations Option, die ein Site Präfix angibt, bewirkt, dass ein Eintrag in der Site Prefix-Tabelle erstellt wird, der mit dem IPv6-SPT-Befehl angezeigt werden kann. Die Site-Präfix Tabelle wird verwendet, um ungeeignete Site lokale Adressen von den von [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) und verwandten Funktionen zurückgegebenen Adressen zu entfernen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPv6-Verbindungs lokale und Standort lokale Adressen](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> </dl>

 

 



