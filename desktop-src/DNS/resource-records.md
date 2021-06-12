---
title: Ressourcendatensätze
description: Erfahren Sie mehr über Ressourcendatensätze. Ein Ressourceneintrag ist die Informationseinheit in DNS-Zonendateien, die zum Auflösen aller DNS-Abfragen verwendet wird.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84bd000e2d88884bbb387748eaced1d0d58a324
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010673"
---
# <a name="resource-records"></a>Ressourcendatensätze

Ein Ressourceneintrag, der häufig als RR bezeichnet wird, ist die Informationseinheit in DNS-Zonendateien. RRs sind die grundlegenden Bausteine von Hostnamen und IP-Informationen und werden verwendet, um alle DNS-Abfragen aufzulösen. Ressourcendatensätze sind so viele Typen vorhanden, dass erweiterte Namensauflösungsdienste zur Verfügung stehen.

Verschiedene Typen von RRs haben unterschiedliche Formate, da sie unterschiedliche Daten enthalten. Im Allgemeinen verwenden viele RRs jedoch ein gemeinsames Format, wie im folgenden Beispiel für Adressressourcendatensätze veranschaulicht. Im folgenden fiktiven Beispiel werden die Felder in einem A-Ressourcendatensatz erläutert:

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   Das erste Feld (microsoft.com) gibt den Besitzer an.
-   Das zweite Feld (600) ist der Parameter für die Gültigkeitsdauer (Time-to-Live, TTL) in Sekunden.
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

 

 




