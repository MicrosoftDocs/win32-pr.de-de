---
description: Leistungsanforderungen von Benutzern und Administratoren mit Windows Sockets-Anwendungen (Winsock).
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 'Leistungsanforderungen: Benutzer und Administratoren'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c74f4ec6f0a545a98a890f0bc8ff954fe43a3f79fc04fd2c2d92e68ea9f646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097670"
---
# <a name="performance-needs-users-and-administrators"></a>Leistungsanforderungen: Benutzer und Administratoren

Benutzer bewerten die Anwendungsleistung nach ihrer Erfahrung:

-   Reagiert die Anwendung schnell?
-   Wird ein Sanduhrsymbol angezeigt, während Hintergrundvorgänge ausgeführt werden?
-   Wird die Anwendung schnell gestartet und geschlossen?
-   Werden Fehler auf verständliche Weise behandelt?

Zusammengefasst möchten Benutzer, dass Anwendungen schnell und vorhersagbar sind.

Im Gegensatz dazu bewerten Administratoren häufig die Leistung einer Anwendung in Der effizienten Nutzung von Netzwerkressourcen. Administratoren können Folgendes fragen:

-   Verfügt die Anwendung über einen geringen Mehraufwand und eine effiziente Netzwerknutzung?
-   Wird die Mindestanzahl von Verbindungen verwendet, sodass mein Server so viele Benutzer gleichzeitig wie möglich nutzen kann?
-   Rufe ich ständig den Helpdesk an?

Kurz gesagt: Administratoren möchten, dass Anwendungen skaliert werden.

## <a name="best-practices-for-performance-needs"></a>Bewährte Methoden für Leistungsanforderungen

Beim Entwickeln einer Windows Sockets-Anwendung werden diese Leistungsanforderungen in nützliche Regeln übersetzt.

-   Lassen Sie Netzwerkanwendungen schnell initialisieren.

    Die Benutzeroberfläche sollte nicht auf Netzwerkantworten warten müssen. Einige Aufgaben können ausgeführt werden, bevor das Netzwerk verfügbar ist, oder ohne das Netzwerk. Wenn das Netzwerk nicht reagiert, benötigt der Benutzer möglicherweise die Benutzeroberfläche für einfache Vorgänge, z. B. das Schließen der Anwendung.

-   Warten Sie nicht, bis das Netzwerk heruntergefahren ist.

    Ordnungsgemäß geschriebene Client-Server-Anwendungen behandeln abortive Trennungen ordnungsgemäß. Initiieren Sie keinen potenziell langwierigen Vorgang, z. B. das Synchronisieren von Dateien oder Ordnern mit einem Server, die beim Herunterfahren nicht unterbrochen werden können. Netzwerke sind nicht konsistent reaktionsfähig, sodass selbst kleine Vorgänge sich als zeitaufwändig erweisen könnten. Geben Sie benutzern positives Feedback, einschließlich Der Fortschritt und der geschätzten Abschlusszeiten.

-   Stellen Sie eine reaktionsfähige Benutzeroberfläche sicher.

    Die Reaktionsfähigkeit der Anwendung hilft dabei, unnötige Helpdeskanrufe zu vermeiden. Eine gute Richtlinie für interaktive Antworten sind 500 Millisekunden. Benutzer betrachten Pausen, die länger als 500 Millisekunden sind, als Leistungsverzögerung. Anwendungen sollten reaktionsfähig genug sein, um dem Benutzer Vertrauen in die Anwendung zu geben.

-   Beheben von Netzwerkfehlern.

    Nicht alle Netzwerkfehler sind kritisch. Beispielsweise kann eine Anwendung, die alle Daten empfangen oder gepostet hat, wahrscheinlich Fehler ignorieren, wenn die Verbindung geschlossen wird. Gehen Sie nicht davon aus, dass das Netzwerk oder der Benutzer verfügbar ist. Behandeln Sie Fehler entweder ohne Benutzereingriff, oder ignorieren Sie sie, wenn Fehler unkritisch sind.

-   Eine Anwendung sollte eigene angemessene Time outs definieren.

    Beispielsweise kann eine Windows Sockets connect()-Anforderung unter bestimmten Bedingungen für bis zu 21 Sekunden blockiert werden. Anwendungen müssen möglicherweise ihre eigenen Time outs entsprechend ihren Benutzern einführen.

-   Minimieren Sie den Protokollaufwand.

    Beim Einsparen der Netzwerkbandbreite geht es teilweise um die Minimierung des Protokollaufwands, der durch Ihre Anwendung verursacht wird. Außerdem geht es darum, unnötigen Netzwerkdatenverkehr zu vermeiden. Protokolle mit einem geringeren Headeraufwand können zum Übertragen von Anwendungsdaten verwendet werden. Wenn Sie beispielsweise kleinere Mengen nichtkritischer oder wiederholbarer Daten senden, verwenden Sie UDP im Gegensatz zu TCP, um den Mehraufwand im Zusammenhang mit der Verbindungseinrichtung und -wartung zu reduzieren. Wenn dieselben Daten an mehrere Empfänger gesendet werden müssen, ziehen Sie Multicast in Betracht. Beachten Sie, dass UDP-Anwendungen nicht flussgesteuert sind. Das Pushen über die verfügbare Bandbreite hinaus kann zu schwerwiegenden Netzwerkfehlern führen. Das Netstat-Hilfsprogramm kann mit den Optionen **-e** und **-s verwendet** werden, um Statistiken für verschiedene Protokolle anzuzeigen.

-   Sparen Sie Systemressourcen.

    Systemressourcen können schnell genutzt werden, wenn keine ordnungsgemäße Behandlung verwendet wird. Sockets und TCP-Verbindungen verbrauchen beispielsweise Ressourcen. Verwenden Sie nicht mehrere TCP-Verbindungen pro Client, wobei eine für den Zweck der Anwendung verwendet wird.

Bei Transaktionsanwendungen sind eine gute Benutzererfahrung und eine geringe Netzwerkauslastung keine in Konflikt stehenden Ziele. Das Netzwerk ist ein Engpass. Netzwerkintensive Anwendungen verbringen mehr Zeit mit Wartezeiten, und gut geschriebene Netzwerkanwendungen sind so konzipiert, dass unnötige Wartezeiten sowohl für die Benutzeroberfläche als auch für Netzwerkübertragungen minimiert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hochleistungsanwendungen Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Leistungsdimensionen](performance-dimensions-2.md)
</dt> </dl>

 

 



