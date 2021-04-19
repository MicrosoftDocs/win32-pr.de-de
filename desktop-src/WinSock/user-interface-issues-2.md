---
description: Eine der offensichtlichsten Änderungen von IPv4 zu IPv6 ist die Größe der IP-Adresse. Viele Benutzeroberflächen stellen Dialogfelder bereit, die es einem Benutzer ermöglichen, eine IP-Adresse einzugeben, wie in der folgenden Abbildung dargestellt.
ms.assetid: e2d7fd41-297a-400b-ae59-5d67db2be6f6
title: Probleme mit der Benutzeroberfläche für IPv6-Winsock-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03305073687cdd77e17c529d70ffe5959df40960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368968"
---
# <a name="user-interface-issues-for-ipv6-winsock-applications"></a>Probleme mit der Benutzeroberfläche für IPv6-Winsock-Anwendungen

Eine der offensichtlichsten Änderungen von IPv4 zu IPv6 ist die Größe der IP-Adresse. Viele Benutzeroberflächen stellen Dialogfelder bereit, die es einem Benutzer ermöglichen, eine IP-Adresse einzugeben, wie in der folgenden Abbildung dargestellt.

![Feld "allgemeine IPv4-Adresse" auf einer Benutzeroberfläche](images/portingguide001.jpg)

Adressierung in IPv6 ist aufgrund vieler Faktoren wie z. b. Länge, Komplexität und der Bedeutung von Abschnitten innerhalb des IPv6-Adressraums nicht für Änderungen oder Spezifikationen durch Benutzer geeignet. Daher ist die Notwendigkeit, Benutzern die Möglichkeit zu geben, ihre eigene Adresse anzugeben, reduziert. Aufgrund der Komplexität, die mit der IPv6-Adressierung verbunden ist, ist die Bereitstellung von IPv6-Adressinformationen in der Regel auf Knoten Basis nicht wahrscheinlich.

Eine IPv6-Adresse in der Benutzeroberfläche anzuzeigen, ist nicht denkbar, und Entwickler sollten daher die Variabilität der Größe einer IPv6-Adresse berücksichtigen, wenn Sie eine Anwendung zur Unterstützung von IPv6 ändern.

Im restlichen Teil dieses Abschnitts wird der Unterschied zwischen der Vorhersagbarkeit der IPv4-Adressen und der IPv6-Adress Länge erörtert. In diesem Abschnitt wird davon ausgegangen, dass IPv6-Adressen in ihrer hexadezimalen Darstellung angezeigt werden.

Die Größe von IPv4-Adressen ist vorhersagbar, da Sie eine dezimale dezimale Notation befolgen, wie im folgenden Beispiel für eine Adresse veranschaulicht:

``` syntax
10.10.256.1
```

IPv6-Adressen sind aufgrund der IPv6-Adress Konvention, die die Verwendung eines doppelten Doppelpunkts (::) stellt eine Reihe von Nullen dar. Daher entsprechen die folgenden IPv6-Adress Darstellungen derselben IPv6-Adresse:

``` syntax
1040:0:0:0:0:0:0:1
1040::1
```

Die Funktion, eine Reihe von Nullen mit einem Doppelpunkt darzustellen, führt zu einer unvorhersehbaren Länge für einen beliebigen IPv6-Wert, der Programmierer beim Erstellen von Benutzeroberflächen Anzeigen von IPv6-Adressen berücksichtigen muss. Sicherlich sollten Entwickler sicherstellen, dass die Benutzeroberfläche IP-Adressen anzeigen kann, von denen kein Doppelpunkt für eine Reihe von Nullen (erste Adresse unten) verwendet wird. Außerdem sollten Sie sicherstellen können, dass die längste mögliche IPv6-Adresse (zweite Adresse unten, mit der eingebetteten IPv4-Adresse) angezeigt wird, wenn Sie Ihre IPv6-fähige Benutzeroberfläche erstellen. Beachten Sie, dass durch das Hinzufügen des Bereichs Bezeichners (ID) zur folgenden Adresse die Länge um bis zu elf Zeichen vergrößert werden kann:

``` syntax
21DA:00D3:0010:2F3B:02AA:00FF:FE28:9C5A
0000:0000:0000:0000:0000:ffff:123.123.123.123
```

Ein weiterer wichtiger Aspekt ist, ob namensbasierte Adressen besser geeignet sind als Zahlen basierte IPv6-Adressen. Wenn Namen basierte Adressen besser geeignet sind, sollten Sie in der Benutzeroberfläche auf Benennungs Konventionen achten, einschließlich der entsprechenden Eingabe Fehlerüberprüfung für den Task.

Die Anzeige von IPv6-Adressen, die Entwickler bei der Änderung Ihrer Anwendung berücksichtigen müssen, und beim Entwerfen von Benutzeroberflächen Darstellungen von IPv6-Adressen ist mit anderen Komplexitäten verbunden. Folgende Aspekte sind zu beachten:

-   Soll die Adresse alle Sequenzen von Nullen enthalten, oder verwenden Sie die Double-Doppelpunkt-Notation?
-   Empfiehlt es sich, eine Zahlen basierte Adress Darstellung oder eine namensbasierte Darstellung zu verwenden?
-   Möchte der Benutzer einen bestimmten Aspekt des Adressierungs Schemas, z. b. Subnetzpräfix, Bereichs Bezeichner oder andere Unterfelder, unterscheiden?
-   Möchte der Benutzer andere Aspekte der Adresse bestimmen, wie z. b. den TLA-Bezeichner, den NLA-Bezeichner oder den SLA-Bezeichner?
-   Kann Ihre Benutzeroberfläche eingebettete IPv6-Adressen unterstützen. wenn dies der Fall ist, wie werden diese behandelt und angezeigt? Unterscheiden Sie sich zwischen IPv4-kompatiblen Adressen und IPv4-zugeordneten IPv6-Adressen, wenn Sie dem Benutzer Adressinformationen anzeigen?

Es gibt auch weitere Überlegungen, und Entwickler sollten Ihre Kunden Zielgruppe sorgfältig berücksichtigen, wenn Sie IP-Adress Benutzeroberflächen entwickeln.

Bewährte Methoden

-   Entwickler müssen bei der Änderung Ihrer Anwendung zur Unterstützung von IPv6 den entsprechenden Ansatz für jede Benutzeroberfläche in Erwägung gezogen. Das sicherstellen, dass die Benutzeroberfläche ausreichend Länge zum Anzeigen von IPv6-Adressen enthält, ist zwingend erforderlich, da festgelegt wird, ob diese Adresse eine Zahl oder ein Name ist
-   Verwenden Sie nach Möglichkeit vorhandene Winsock-und IP-Hilfsfunktionen, wenn Sie IPv6-Adressen verwenden, anstatt diese Logik erneut zu implementieren. Beispielsweise können die [**RtlIpv6AddressToString**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)-, [**RtlIpv6AddressToStringEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)-, [**RtlIpv6StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)-und [**RtlIpv6StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw) -Funktionen verwendet werden, um zwischen IPv6-Adressen und Zeichen folgen Darstellungen dieser IPv6-Adressen zu konvertieren.

Zu Vermeider Code

-   Benutzeroberflächen Elemente, die von einer Adresse mit IPv4-Adresse abhängen, müssen überprüft werden, und bei dieser Überprüfung sollte berücksichtigt werden, ob die von Ihnen bereitgestellten Informationen (unter IPv4) für IPv6 geeignet sind.
-   Die Möglichkeit, eine IP-Adresse anzugeben, hängt auch davon ab, ob IPv4 verwendet wird oder ob IPv6 verfügbar ist. Wenn IPv6 verfügbar ist, ist es sinnvoll, Zahlen basierte (hexadezimale) Adressen oder namensbasierte Adressen anzugeben?

Codierungs Aufgaben

**So überarbeiten Sie Ihre vorhandene Codebasis von IPv4 zu IPv4-und IPv6-Interoperabilität**

1.  Führen Sie eine visuelle Überprüfung der Benutzeroberfläche aus, und suchen Sie nach einem Element, das von einer bestimmten Länge für die IP-Adress Zeichenfolge abhängt. Steuerelemente mit der leicht identifizierten Dezimal Schreibweise mit vier Abschnitts Trennzeichen sind leicht zu erkennen, andere hingegen nicht. Es gibt möglicherweise Orte, an denen IP-Adressen angezeigt werden können, z. b. in Dialogfeldern, in denen eine IPv6-Adresse außerhalb des Anzeige Raums liegen könnte.
2.  Wenn Sie eines dieser Steuerelemente finden, überprüfen Sie, ob es angemessen ist, die Adresse bei Verwendung von IPv6 anzuzeigen. Wenn es möglich ist, dass entweder IPv4 oder IPv6 verwendet wird, stellen Sie sicher, dass die Benutzeroberfläche beide unterstützen kann. Ersetzen oder erweitern Sie alle Steuerelemente durch Benutzeroberflächen-Steuerelemente, die eine ganze IPv6-Adresse anzeigen können.
3.  Befolgen Sie das Testen der Benutzeroberfläche, um sicherzustellen, dass die Änderungen, die die IPv6-Adress Anzeige ermöglichen, die gewünschte Nutzbarkeit bei Verwendung von IPv4-Adressen beibehalten Testen Sie außerdem die Anzeige Pfade für Protokolladressen, z. b. Informations Dialogfelder, um sicherzustellen, dass Sie IPv6-Adressen ordnungsgemäß verarbeiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPv6-Handbuch für Windows Sockets-Anwendungen](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Ändern von Datenstrukturen für IPv6-Winsock-Appications](changing-data-structures-2.md)
</dt> <dt>

[Dual-Stack-Sockets für IPv6-Winsock-Anwendungen](dual-stack-sockets.md)
</dt> <dt>

[Funktionsaufrufe für IPv6-Winsock-Anwendungen](function-calls-2.md)
</dt> <dt>

[Verwendung von hart codierten IPv4-Adressen](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Zugrunde liegende Protokolle für IPv6-Winsock-Anwendungen](underlying-protocols-2.md)
</dt> </dl>

 

 
