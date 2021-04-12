---
title: Informationen zu DNS
description: Domain Name System (DNS) ist ein Industriestandard Protokoll, das zum Auffinden von Computern in einem IP-basierten Netzwerk verwendet wird. Benutzer können anzeigen Amen wie z. b. www.Microsoft.com einfacher als Zahlen basierte Adressen, z. b. 207.46.131.137, merken.
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- Informationen zu Domain Name System DNS
- Domain Name System DNS, Informationen zu
- Domain Name System DNS, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98573e72db645d96c263efd479135807274c18a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104219406"
---
# <a name="about-dns"></a>Informationen zu DNS

Domain Name System (DNS) ist ein Industriestandard Protokoll, das zum Auffinden von Computern in einem IP-basierten Netzwerk verwendet wird. Benutzer können sich anzeigen Amen, wie z `www.microsoft.com` . b. einfacher als Zahlen basierte Adressen, wie z. b. 207.46.131.137, merken.

IP-Netzwerke, wie z. b. das Internet und Windows-Netzwerke, basieren auf Zahlen basierten Adressen, um Daten im gesamten Netzwerk zu übertragen. Daher ist es notwendig, anzeigen Amen (z `www.microsoft.com` . b.) in numerische Adressen zu übersetzen, die das Netzwerk erkennen kann (z. b. 207.46.131.137). DNS ist der bevorzugte Dienst in Windows, um solche Ressourcen zu suchen und in IP-Adressen zu übersetzen.

DNS ist der primäre Serverlocatorpunkt-Dienst für Active Directory. Daher kann DNS als Basis Dienst für Windows und Active Directory betrachtet werden. Windows stellt Funktionen bereit, mit denen Anwendungsprogrammierer DNS-Funktionen wie das programmgesteuerte Ausführen von DNS-Abfragen, das Vergleichen von Datensätzen und das Suchen von Namen verwenden können.

Viele DNS-Funktionen sind tatsächlich Funktionstypen, da es einen Basisnamen für die Funktion gibt, deren Verwendung jedoch von der Zeichencodierung abhängig ist. Beispielsweise ist die [**DNSQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) -Funktion in der Funktionsreferenz der DNS-API (Application Programming Interface) als **DNSQuery** aufgeführt. die Verwendung in Anwendungen hängt jedoch davon ab, ob die Zeichencodierung ANSI (durch Anhängen von \_ an den Funktionstyp Namen), Unicode (durch Anhängen von \_ W an den Funktionstyp Namen) oder UTF-8 (durch Anhängen von UTF an den Funktionstyp Namen) oder UTF-8 (festgelegt durch Anhängen von UTF an den Funktionstyp Namen) ist \_ . Daher würde der Funktions Aufrufder **DNSQuery** -Funktion eine der folgenden sein:

DNSQuery \_ A ( \_ a für ANSI-Codierung)

DNSQuery \_ w ( \_ w für Unicode-Codierung)

DNSQuery \_ utf8 ( \_ UTF8 für UTF-8-Codierung)

Alle Funktionen, die diese Konvention erfordern, geben diese Anforderung in den ersten Sätzen ihrer Funktionsdefinition eindeutig an. Verwenden Sie den richtigen Funktionsnamen; Beispielsweise können Sie nicht einfach [**DNSQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) anstelle von DNSQuery A aufzurufen \_ .

 

 




