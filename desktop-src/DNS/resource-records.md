---
title: Ressourcendatensätze
description: Erfahren Sie mehr über Ressourcendatensätze. Ein Ressourceneintrag ist die Informationseinheit in DNS-Zonendateien, die zum Auflösen aller DNS-Abfragen verwendet wird.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606d74f41e18fefa144ff21d3ed88d9683938304b0c8aa0bc7d94e2fbaa624cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825060"
---
# <a name="resource-records"></a>Ressourcendatensätze

Ein Ressourceneintrag, der häufig als RR bezeichnet wird, ist die Informationseinheit in DNS-Zonendateien. RRs sind die grundlegenden Bausteine von Hostnamen und IP-Informationen und werden verwendet, um alle DNS-Abfragen aufzulösen. Ressourcendatensätze sind so viele Typen vorhanden, dass erweiterte Namensauflösungsdienste zur Verfügung stehen.

Verschiedene Typen von RRs haben unterschiedliche Formate, da sie unterschiedliche Daten enthalten. Im Allgemeinen verwenden viele RRs jedoch ein gemeinsames Format, wie im folgenden Beispiel für Adressressourcendatensätze veranschaulicht. Im folgenden fiktiven Beispiel werden die Felder in einem A-Ressourcendatensatz erläutert:

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   Das erste Feld (microsoft.com) gibt den Besitzer an.
-   Das zweite Feld (600) ist der TTL-Parameter (Time-to-Live, Gültigkeitsdauer) in Sekunden.
-   Das dritte Feld (IN) ist das Klassenfeld, das die Protokollfamilie (fast immer IN) für die Internetklasse darstellt.
-   Das vierte Feld (A) ist der Typ der Ressource, die RR darstellt.
-   Das fünfte Feld (150.150.150.1) ist die Ressourcendaten oder RDATA. Dieses Feld ist ein Variablentyp, der Informationen bereitstellt, die für den Typ der Ressource geeignet sind. In diesem Fall handelt es sich um eine 32-Bit-IP-Adresse.

Die folgenden Ressourceneintragstypen werden häufig in DNS verwendet:

-   Autoritätsstart (SOA)
-   Namensserver (NS)
-   [*Zeigerdatensatz*](p-gly.md) (PTR)
-   Adresse (A)
-   IPv6-Adresse (AAAA)
-   E-Mail-Austausch (MX)
-   [*Kanonischer Name*](c-gly.md) (CNAME)
-   Windows Internet Naming Service (WINS)
-   WINS Reverse Look up (WINSR)

Es gibt viele andere Ressourceneintragstypen in DNS. Weitere Informationen finden Sie unter [DNS-WMI-Anbieterreferenz.](dns-wmi-provider-reference.md)

 

 




