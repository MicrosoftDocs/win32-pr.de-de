---
title: Ressourcen Einträge
description: Ein Ressourcen Daten Satz, der häufig als RR bezeichnet wird, ist die Eintrags Einheit in DNS-Zonendateien. RRS sind die grundlegenden Bausteine von Hostnamen-und IP-Informationen und werden verwendet, um alle DNS-Abfragen aufzulösen.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05b667b95a8ede32018e1aad7de375e77a890487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712798"
---
# <a name="resource-records"></a>Ressourcen Einträge

Ein Ressourcen Daten Satz, der häufig als RR bezeichnet wird, ist die Eintrags Einheit in DNS-Zonendateien. RRS sind die grundlegenden Bausteine von Hostnamen-und IP-Informationen und werden verwendet, um alle DNS-Abfragen aufzulösen. Ressourcen Einträge sind so viele Typen vorhanden, dass erweiterte Namensauflösungsdienste bereitgestellt werden.

Verschiedene Arten von RRS haben unterschiedliche Formate, da Sie unterschiedliche Daten enthalten. Im allgemeinen weisen viele RRS jedoch ein allgemeines Format auf, wie im folgenden Beispiel für Adress Ressourcen Einträge veranschaulicht. Im folgenden fiktiven Beispiel werden die Felder in einem Ressourcen Daten Satz erläutert:

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   Das erste Feld (Microsoft.com) bezeichnet den Besitzer.
-   Das zweite Feld (600) ist der Gültigkeitsdauer Parameter (Time-to-Live, TTL) in Sekunden.
-   Das dritte Feld (in) ist das Klassenfeld, das die Protokollfamilie darstellt, die sich fast immer in für die Internet Klasse befindet.
-   Das vierte Feld (A) ist der Typ der Ressource, die der RR darstellt.
-   Das fünfte Feld (150.150.150.1) ist die Ressourcen Daten bzw. rdata. Dieses Feld ist ein Variablentyp, der Informationen bereitstellt, die für den Ressourcentyp geeignet sind. in diesem Fall handelt es sich um eine 32-Bit-IP-Adresse.

Die folgenden Ressourcen Daten Satz Typen werden häufig in DNS verwendet:

-   Autoritäts Anfang (SOA)
-   Namen Server (NS)
-   [*Zeiger Daten Satz*](p-gly.md) (PTR)
-   Adresse (A)
-   IPv6-Adresse (AAAA)
-   E-Mail-Austausch (MX)
-   [*Kanonischer Name*](c-gly.md) (CNAME)
-   Windows Internet Naming Service (WINS)
-   WINS-Reverse-Suche (WINSR)

Es gibt zahlreiche andere Ressourcen Daten Satz Typen in DNS. Weitere Informationen finden Sie unter [DNS-WMI-Anbieter Referenz](dns-wmi-provider-reference.md).

 

 




