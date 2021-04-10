---
description: Leistungsanforderungen von Benutzern und Administratoren mit Windows Sockets (Winsock)-Anwendungen.
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 'Leistungsanforderungen: Benutzer und Administratoren'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a8178cf1d7516e9c16493916f8cf911752b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041722"
---
# <a name="performance-needs-users-and-administrators"></a>Leistungsanforderungen: Benutzer und Administratoren

Benutzer beurteilen die Anwendungsleistung nach ihren Möglichkeiten:

-   Reagiert die Anwendung schnell?
-   Wird ein Sanduhr Symbol angezeigt, während Hintergrund Vorgänge ausgeführt werden?
-   Wird die Anwendung schnell gestartet und geschlossen?
-   Werden Fehler verständlich behandelt?

Zusammenfassend möchten Benutzer, dass Anwendungen schnell und vorhersagbar sind.

Im Gegensatz dazu beurteilen Administratoren oft die Leistung einer Anwendung, um zu bestimmen, wie effizient Netzwerkressourcen verwendet werden. Administratoren können Folgendes anfordern:

-   Hat die Anwendung einen geringen Verwaltungsaufwand und eine effiziente Netzwerk Auslastung?
-   Wird die Mindestanzahl von Verbindungen verwendet, sodass der Server so viele Benutzer gleichzeitig wie möglich bedienen kann?
-   Rufe ich den Helpdesk ständig auf?

Kurz gesagt: Administratoren möchten, dass Anwendungen skaliert werden.

## <a name="best-practices-for-performance-needs"></a>Bewährte Methoden für Leistungsanforderungen

Wenn Sie eine Windows Sockets-Anwendung entwickeln, werden diese Leistungsanforderungen in nützliche Regeln übersetzt.

-   Schnelle Initialisierung von Netzwerkanwendungen.

    Die Benutzeroberfläche sollte nicht auf Netzwerk Antworten warten müssen. Einige Tasks können ausgeführt werden, bevor das Netzwerk verfügbar ist, oder ohne das Netzwerk. Wenn das Netzwerk nicht antwortet, benötigt der Benutzer möglicherweise die Benutzeroberfläche für einfache Vorgänge, z. b. das Schließen der Anwendung.

-   Warten Sie nicht, bis das Netzwerk heruntergefahren ist.

    Ordnungsgemäß geschriebene Client/Server-Anwendungen verarbeiten Abbruch Abbruch ordnungsgemäß. Initiieren Sie keinen möglicherweise langwierigen Vorgang, z. b. das Synchronisieren von Dateien oder Ordnern mit einem Server, der beim Herunterfahren nicht unterbrochen werden kann. Netzwerke sind nicht konsistent reaktionsfähig, sodass sogar kleine Vorgänge zeitaufwändig sein könnten. Bereitstellen von positivem Feedback für Benutzer, einschließlich Hinweise zum Fortschritt und zu geschätzten Abschlusszeiten.

-   Stellen Sie eine reaktionsfähige Benutzeroberfläche sicher.

    Die Reaktionsfähigkeit der Anwendung hilft, unnötige Helpdeskanrufe auszuschließen Eine gute Richtlinie für die interaktive Reaktion ist 500 Millisekunden. Benutzer sehen länger als 500 Millisekunden als Verzögerung der Leistung an. Anwendungen sollten ausreichend reaktionsfähig sein, um dem Benutzer die Gewissheit über die Anwendung zu geben.

-   Überprüfen Sie Netzwerkfehler.

    Nicht alle Netzwerkfehler sind von entscheidender Bedeutung. Beispielsweise kann eine Anwendung, die alle Daten empfangen oder gesendet hat, beim Schließen der Verbindung wahrscheinlich Fehler ignorieren. Gehen Sie nicht davon aus, dass das Netzwerk oder der Benutzer verfügbar ist. behandeln Sie Fehler ohne Benutzereingriff, oder ignorieren Sie diese, wenn Fehler nicht kritisch sind.

-   Eine Anwendung sollte Ihre eigenen angemessenen Timeouts definieren.

    Beispielsweise kann eine Windows Sockets Connect ()-Anforderung unter bestimmten Bedingungen für bis zu 21 Sekunden blockiert werden. Anwendungen müssen ggf. ihre eigenen Timeouts für Ihre Benutzer bereitstellen.

-   Minimieren Sie den Protokoll Aufwand.

    Die Erhaltung der Netzwerkbandbreite dient zum Minimieren des Protokoll Aufwands, der von Ihrer Anwendung verursacht wird. Es geht auch darum, unnötigen Netzwerk Datenverkehr zu vermeiden. Zum Übertragen von Anwendungsdaten können Protokolle mit einem niedrigeren Header Mehraufwand verwendet werden. Wenn Sie z. b. kleinere Mengen nicht kritischer oder wiederholbarer Daten senden, verwenden Sie UDP anstelle von TCP, um den mehr Aufwand im Zusammenhang mit der Verbindungs Einrichtung und-Wartung zu verringern. Wenn die gleichen Daten an mehrere Empfänger gesendet werden müssen, sollten Sie Multicast in Erwägung gezogen. Beachten Sie, dass UDP-Anwendungen nicht Fluss gesteuert werden – durch pushübertragung über die verfügbare Bandbreite kann schwerwiegender Netzwerkausfall verursacht werden. Das Hilfsprogramm netstat kann mit den Optionen **-e** und **-s** verwendet werden, um Statistiken für verschiedene Protokolle anzuzeigen.

-   Sparen Sie Systemressourcen.

    System Ressourcen können schnell verbraucht werden, wenn keine ordnungsgemäße Unterhaltung verwendet wird. Beispielsweise verbrauchen Sockets-und TCP-Verbindungen Ressourcen. Verwenden Sie zum Zweck der Anwendung nicht mehrere TCP-Verbindungen pro Client.

Bei transaktionalen Anwendungen sind gute Benutzer Funktionen und eine geringe Netzwerk Auslastung nicht in Konflikt stehende Ziele. Das Netzwerk stellt einen Engpass dar. Netzwerk intensive Anwendungen verbringen länger Zeit mit dem warten, und gut geschriebene Netzwerkanwendungen sind so konzipiert, dass unnötige Wartezeit sowohl für die Benutzeroberfläche als auch für Netzwerkübertragungen minimiert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hochleistungsfähige Windows Sockets-Anwendungen](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Leistungsdimensionen](performance-dimensions-2.md)
</dt> </dl>

 

 



