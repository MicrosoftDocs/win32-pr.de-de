---
description: gibt ein Präfix an, das über einen Link zur Schnittstelle \# 4 verbunden ist.
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: IPv6-Standortpräfixe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd37370aa14bd6883f83e93d661f10b96d804dc3b85cf47173da4b1f0ee0f90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111294"
---
# <a name="ipv6-site-prefixes"></a>IPv6-Standortpräfixe

Mit dem Befehl ipv6 rtu können veröffentlichte On-Link-Präfixe mit einer Länge des Standortpräfixes konfiguriert werden. Wenn angegeben, wird die Länge des Standortpräfixes in einer Präfixinformationsoption in Router-Ankündigungen angegeben. Beispiel:

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

gibt ein Präfix an, das über einen Link zur Schnittstelle \# 4 verbunden ist. Das Präfix wird veröffentlicht, was bedeutet, dass es in Router-Ankündigungen enthalten ist, wenn Schnittstelle \# 4 eine Werbeschnittstelle ist. Die Lebensdauer in der Präfixinformationsoption beträgt 1.800 Sekunden (30 Minuten). Die Länge des Standortpräfixes in der Präfixinformationsoption ist 48.

Der Empfang einer Präfixinformationsoption, die ein Standortpräfix angibt, bewirkt, dass ein Eintrag in der Standortpräfixtabelle erstellt wird, der mit dem Befehl ipv6 spt angezeigt werden kann. Die Standortpräfixtabelle wird verwendet, um ungeeignete lokale Adressen von den adressen zu entfernen, die von [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) und zugehörigen Funktionen zurückgegeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lokale und standortbasierte IPv6-Adressen](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> </dl>

 

 



