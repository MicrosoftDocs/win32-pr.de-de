---
description: Eine der offensichtlichsten Änderungen von IPv4 zu IPv6 ist die Größe der IP-Adresse. Viele Benutzeroberflächen stellen Dialogfelder bereit, mit denen ein Benutzer eine IP-Adresse eingeben kann, wie in der folgenden Abbildung dargestellt.
ms.assetid: e2d7fd41-297a-400b-ae59-5d67db2be6f6
title: Benutzeroberfläche für IPv6-Winsock-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae982504798789c928691bbf4932d5e6abdfabf1ba12077122bb6dab28eb47de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121185"
---
# <a name="user-interface-issues-for-ipv6-winsock-applications"></a>Benutzeroberfläche für IPv6-Winsock-Anwendungen

Eine der offensichtlichsten Änderungen von IPv4 zu IPv6 ist die Größe der IP-Adresse. Viele Benutzeroberflächen stellen Dialogfelder bereit, mit denen ein Benutzer eine IP-Adresse eingeben kann, wie in der folgenden Abbildung dargestellt.

![Allgemeines Ipv4-Adressfeld in einer Benutzeroberfläche](images/portingguide001.jpg)

Die Adressierung in IPv6 ist aufgrund vieler Faktoren wie Länge, Komplexität und Bedeutung von Abschnitten innerhalb des IPv6-Adressraums nicht von Änderungen oder Spezifikationen durch Benutzer abhängig. Daher ist es weniger notwendig, Benutzern die Möglichkeit zu bieten, ihre eigene Adresse anzugeben. Darüber hinaus ist es aufgrund der Komplexität im Zusammenhang mit der IPv6-Adressierung wahrscheinlich nicht möglich, Administratoren die Möglichkeit zu bieten, IPv6-Adressinformationen pro Knoten anzugeben.

Das Anzeigen einer IPv6-Adresse auf der Benutzeroberfläche ist nicht unvorstellbar, daher sollten Entwickler die Variabilität bei der Größe einer IPv6-Adresse berücksichtigen, wenn sie eine Anwendung so ändern, dass sie IPv6 unterstützt.

Im restlichen Teil dieses Abschnitts wird der Unterschied zwischen der Vorhersagbarkeit der IPv4-Adresslänge und überlegungen zur IPv6-Adresslänge erläutert. In diesem Abschnitt wird davon ausgehen, dass IPv6-Adressen in ihrer hexadezimalen Darstellung angezeigt werden.

IPv4-Adressen sind in ihrer Größe vorhersagbar, da sie fest auf punktierte Dezimalschreibzeichen folgen, wie im folgenden Adressbeispiel veranschaulicht:

``` syntax
10.10.256.1
```

IPv6-Adressen sind aufgrund der IPv6-Adresskonvention, die die Verwendung eines Doppelpunkts (::) , um eine Reihe von Nullen zu darstellen. Daher entspricht die folgende IPv6-Adressdarstellung der gleichen IPv6-Adresse:

``` syntax
1040:0:0:0:0:0:0:1
1040::1
```

Die Funktion, eine Reihe von Nullen mit einem Doppelpunkt zu darstellen, führt zu einer unvorhersehbaren Länge für jede bestimmte IPv6-Adresse. Daher müssen Programmierer diese Funktion beim Erstellen von Benutzeroberflächenanzeigen von IPv6-Adressen berücksichtigen. Natürlich sollten Entwickler sicherstellen, dass die Benutzeroberfläche IP-Adressen anzeigen kann, die keinen Doppelpunkt verwenden, um eine Reihe von Nullen (erste Adresse unten) darstellen zu können, und dass sie beim Erstellen ihrer IPv6-fähigen Benutzeroberfläche die längste mögliche IPv6-Adresse (zweite Adresse unten mit der eingebetteten IPv4-Adresse) anzeigen kann. Beachten Sie auch, dass das Hinzufügen des Bereichsbezeichners (ID) zur folgenden Adresse die Länge um weitere elf Zeichen erhöhen würde:

``` syntax
21DA:00D3:0010:2F3B:02AA:00FF:FE28:9C5A
0000:0000:0000:0000:0000:ffff:123.123.123.123
```

Ein weiterer wichtiger Aspekt ist, ob namensbasierte Adressen besser geeignet sind als zahlenbasierte IPv6-Adressen. Wenn namensbasierte Adressen besser geeignet sind, sollten Benennungskonventionen in die Benutzeroberfläche integriert werden, einschließlich aller Eingabefehlerüberprüfungen, die für die Aufgabe geeignet sind.

Es gibt weitere Komplexitäten im Zusammenhang mit der Anzeige von IPv6-Adressen, die Entwickler beim Ändern ihrer Anwendung und beim Entwerfen von Benutzeroberflächendarstellungen von IPv6-Adressen berücksichtigen müssen. Einige dieser Überlegungen sind die folgenden:

-   Sollte die Adresse alle Sequenzen von Nullen enthalten oder die Doppelpunkt-Notation verwenden?
-   Ist es besser, eine zahlenbasierte Adressdarstellung oder eine namensbasierte Darstellung zu verwenden?
-   Ist der Benutzer daran interessiert, einen bestimmten Aspekt des Adressierungsschemas zu erkennen, z. B. das Subnetzpräfix, den Bereichsbezeichner oder andere Unterfelder?
-   Ist der Benutzer daran interessiert, andere Aspekte der Adresse zu bestimmen, z. B. den TLA-Bezeichner, den NLA-Bezeichner oder den SLA-Bezeichner?
-   Kann Ihre Benutzeroberfläche eingebettete IPv6-Adressen erkennen, und wenn ja, wie werden diese behandelt und angezeigt? Erkennen Sie beim Anzeigen von Adressinformationen für den Benutzer zwischen IPv4-kompatiblen Adressen und IPv4-zugeordneten IPv6-Adressen?

Es gibt auch andere Überlegungen, und Entwickler sollten ihre Zielgruppe bei der Entwicklung von BENUTZEROBERFLÄCHEN für IP-Adressen sorgfältig berücksichtigen.

Empfehlungen

-   Entwickler müssen den geeigneten Ansatz für jede Benutzeroberfläche in Betracht ziehen, wenn sie ihre Anwendung so ändern, dass sie IPv6 unterstützt. Es ist zwingend erforderlich, sicherzustellen, dass die Benutzeroberfläche eine ausreichende Länge zum Anzeigen von IPv6-Adressen enthält, ebenso wie die Bestimmung, ob diese Adresse zahlen- oder namensbasierte Adressen ist.
-   Verwenden Sie nach Möglichkeit vorhandene Winsock- und IP-Hilfsfunktionen, wenn Sie IPv6-Adressen verwenden, anstatt diese Logik erneut zu implementieren. Beispielsweise können die [**Funktionen RtlIpv6AddressToString,**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa) [**RtlIpv6AddressToStringEx,**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw) [**RtlIpv6StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)und [**RtlIpv6StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw) zum Konvertieren zwischen IPv6-Adressen und Zeichenfolgendarstellungen dieser IPv6-Adressen verwendet werden.

Code, der vermieden werden soll

-   Benutzeroberflächenelemente, die von einer IPv4-Adresse abhängen, müssen überprüft werden, und ein Teil dieser Überprüfung sollte beinhalten, ob die von Ihnen (unter IPv4) angegebene Informationen für IPv6 geeignet sind.
-   Die Funktion zum Angeben einer IP-Adresse sollte auch davon abhängen, ob IPv4 verwendet wird oder IPv6 verfügbar ist. Wenn IPv6 verfügbar ist, ist es sinnvoll, zahlenbasierte (hexadezimale) Adressen oder namensbasierte Adressen anzugeben?

Programmieraufgaben

**So überarbeiten Sie Ihre vorhandene Codebasis von IPv4 zu IPv4- und IPv6-Interoperabilität**

1.  Führen Sie eine visuelle Überprüfung der Benutzeroberfläche durch, und suchen Sie nach jedem Element, das von einer bestimmten Länge für die IP-Adresszeichenfolge abhängig ist. Steuerelemente mit der leicht zu erkennenden punktierten Dezimalschreibschreibung mit vier Abschnitten sind leicht zu erkennen, andere jedoch nicht. Es gibt möglicherweise Stellen, an denen IP-Adressen angezeigt werden können, z. B. in Dialogfeldern, an denen eine IPv6-Adresse nicht mehr verfügbar ist.
2.  Überprüfen Sie beim Auffinden eines dieser Steuerelemente, ob es sinnvoll ist, die Adresse bei Verwendung von IPv6 anzuzeigen. Wenn es möglich ist, dass entweder IPv4 oder IPv6 verwendet wird, stellen Sie sicher, dass die Benutzeroberfläche beides aufnehmen kann. Ersetzen oder vergrößeren Sie steuerelemente durch Steuerelemente der Benutzeroberfläche, die eine gesamte IPv6-Adresse anzeigen können.
3.  Führen Sie die Tests der Benutzeroberfläche durch, um sicherzustellen, dass die Änderungen, die die IPv6-Adressanzeige ermöglichen, die beabsichtigte Nutzbarkeit bei Verwendung von IPv4-Adressen erhalten. Testen Sie außerdem auf Protokolladressenanzeigeorte, z. B. Informationsdialogfelder, um sicherzustellen, dass sie IPv6-Adressen ordnungsgemäß verarbeiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPv6-Leitfaden für Windows Sockets-Anwendungen](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Ändern von Datenstrukturen für IPv6 Winsock-Appications](changing-data-structures-2.md)
</dt> <dt>

[Dual-Stack-Sockets für IPv6-Winsock-Anwendungen](dual-stack-sockets.md)
</dt> <dt>

[Funktionsaufrufe für IPv6 Winsock-Anwendungen](function-calls-2.md)
</dt> <dt>

[Verwenden von hartcodierten IPv4-Adressen](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Zugrunde liegende Protokolle für IPv6 Winsock-Anwendungen](underlying-protocols-2.md)
</dt> </dl>

 

 
