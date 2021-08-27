---
title: Informationen zu DNS
description: Domain Name System (DNS) ist ein branchenübliches Protokoll zum Suchen von Computern in einem IP-basierten Netzwerk. Benutzer können sich Anzeigenamen merken, z. B. www.microsoft.com einfacher als nummerbasierte Adressen, z.B. 207.46.131.137.
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- Informationen Domain Name System DNS
- Domain Name System DNS
- Domain Name System DNS beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc286c18aa60a930a243c1500cf4707d0d42874fc9556fcb090df582334f077
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084790"
---
# <a name="about-dns"></a>Informationen zu DNS

Domain Name System (DNS) ist ein branchenübliches Protokoll zum Suchen von Computern in einem IP-basierten Netzwerk. Benutzer können sich Anzeigenamen merken, z. B. `www.microsoft.com` einfacher als zahlenbasierte Adressen, z.B. 207.46.131.137.

IP-Netzwerke, z. B. das Internet und Windows Netzwerke, benötigen zahlenbasierte Adressen, um Daten im gesamten Netzwerk zu übertragen. Daher ist es erforderlich, Anzeigenamen (z.B. ) in numerische Adressen zu `www.microsoft.com` übersetzen, die das Netzwerk erkennen kann (z.B. 207.46.131.137). DNS ist der Dienst ihrer Wahl in Windows, um solche Ressourcen zu finden und in IP-Adressen zu übersetzen.

DNS ist der primäre Locatordienst für Active Directory. Daher kann DNS sowohl für Windows als auch für Active Directory als Basisdienst betrachtet werden. Windows stellt Funktionen bereit, mit denen Anwendungsprogrammierer DNS-Funktionen verwenden können, z. B. programmgesteuertes Erstellen von DNS-Abfragen, Vergleichen von Datensätzen und Suchen von Namen.

Viele DNS-Funktionen sind eigentlich Funktionstypen, da es einen Basisnamen für die Funktion gibt, deren Verwendung jedoch von der Zeichencodierung abhängt. Beispielsweise wird die [**DnsQuery-Funktion**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) in der Funktionsreferenz der DNS-API (Application Programming Interface) als **DnsQuery** aufgeführt. Ihre Verwendung in Anwendungen hängt jedoch davon ab, ob die Zeichencodierung ANSI (durch Anfügen von \_ A an den Funktionstypnamen), Unicode (durch Anfügen von \_ W an den Funktionstypnamen) oder UTF-8 (angegeben durch Anfügen von \_ UTF an den Funktionstypnamen) ist. Daher wäre der Funktionsaufruf für die **DnsQuery-Funktion** tatsächlich einer der folgenden:

DnsQuery \_ A ( A für \_ ANSI-Codierung)

DnsQuery \_ W ( W für \_ Unicode-Codierung)

DnsQuery \_ UTF8 ( \_ UTF8 für UTF-8-Codierung)

Alle Funktionen, die diese Konvention erfordern, geben diese Anforderung innerhalb der ersten Sätze ihrer Funktionsdefinition eindeutig an. Verwenden Sie den richtigen Funktionsnamen. Beispielsweise können Sie [**dnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) nicht einfach anstelle von DnsQuery \_ A aufrufen.

 

 




