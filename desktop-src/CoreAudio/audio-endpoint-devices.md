---
description: Audioendpunktgeräte
ms.assetid: 773714fb-3b00-4f03-988f-05c5835f87cf
title: Audioendpunktgeräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c14d21aa174e34f8cb4ddab520819446a0e0ec89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958588"
---
# <a name="audio-endpoint-devices"></a>Audioendpunktgeräte

Der Begriff *Endpunkt-Gerät* bezieht sich auf ein Hardware Gerät, das sich an einem Ende eines Daten Pfads befindet, der bei einem Anwendungsprogramm stammt oder beendet wird. Beispiele für audioendpunktgeräte sind Sprecher, Kopfhörer, Mikrofone und CD-Player. Die Audiodaten, die sich entlang des Daten Pfads bewegen, können während der Migration zwischen dem Anwendungs-und dem Endpunkt Gerät eine Reihe von Software-und Hardwarekomponenten durchlaufen. Obwohl diese Komponenten für den Betrieb des Endpunkt Geräts von entscheidender Bedeutung sind, sind Sie für Benutzer tendenziell unsichtbar. Benutzer sind eher für Endpunkt Geräte gedacht, die Sie direkt bearbeiten, anstatt in Bezug auf die Geräte auf audioadaptern, die von den Endpunkt Geräten eingebunden werden, oder in Bezug auf die Softwarekomponenten, die die Audiodatenströme verarbeiten, die zu und von diesen Adaptern fließen.

Um Verwechslungen mit Endpunkt Geräten zu vermeiden, bezieht sich diese Dokumentation auf ein Gerät auf einem Audioadapter als *Adapter Gerät*.

Das folgende Diagramm zeigt, wie sich audioendpunktgeräte von Adapter Geräten unterscheiden.

![Beispiele für audioendpunktgeräte und Adapter Geräte](images/devices.jpg)

Im vorangehenden Diagramm sind die folgenden Beispiele für Endpunkt Geräte aufgeführt:

-   Speakers
-   Mikrofon
-   Zusätzliches Eingabegerät

Im folgenden finden Sie Beispiele für Adapter Geräte:

-   Wave-Ausgabegerät (enthält Digital-zu-Analog-Konverter)
-   Gerät für Ausgabe Steuerelemente (enthält Volume-und stumm Steuerelemente)
-   Wave Input-Gerät (enthält einen Analog-zu-Digital-Konverter)
-   Eingabe Steuerelemente-Gerät (enthält volumesteuerung und Multiplexer)

In der Regel beziehen sich die Benutzeroberflächen von Audioanwendungen auf audioendpunktgeräte, nicht auf Adapter Geräte. Windows Vista vereinfacht das Design benutzerfreundlicher Anwendungen, indem die Endpunkt-Geräte Abstraktion direkt unterstützt wird.

Einige Endpunkt Geräte stellen möglicherweise eine permanente Verbindung mit einem Adapter Gerät her. Ein Computer kann z. b. interne Geräte, z. b. CD-Player, Mikrofon oder Referenten enthalten, die in das System Chassis integriert sind. Normalerweise entfernt der Benutzer diese Endpunkt Geräte nicht physisch.

Andere Endpunkt Geräte können über audiobuben eine Verbindung mit einem Audioadapter herstellen. Der Benutzer schließt diese externen Geräte ein und entschließt diese. Beispielsweise befindet sich ein audioendpunktgerät, z. b. ein externes Mikrofon oder Kopfhörer, an einem Ende eines Kabels, dessen anderer Ende an einem Wagen Halter Gerät angeschlossen ist.

Der Adapter kommuniziert mit dem System Prozessor über einen Systembus (in der Regel PCI oder PCI Express) oder über einen externen Bus (USB oder IEEE 1394), der Plug & Play (PNP) unterstützt. Während der Geräte Enumeration identifiziert der Plug & Play-Manager die Geräte im Audioadapter und registriert diese Geräte, damit Sie vom Betriebssystem und von Anwendungen zur Verfügung gestellt werden können.

Anders als bei der Verbindung zwischen einem Adapter und einem externen Bus wie z. b. USB oder dem IEEE 1394-Bus unterstützt die Verbindung zwischen einem Endpunkt Gerät und einem Adapter Gerät keine PNP-Geräteerkennung. Einige Audioadapter unterstützen jedoch die *Erkennung von Jack-Presence*: Wenn ein Plug-in in einen Jack eingefügt oder daraus entfernt wird, generiert die Hardware einen Interrupt, um den Adapter Treiber über die Änderung der Hardwarekonfiguration zu benachrichtigen. Der Endpunkt-Manager in Windows Vista kann diese Hardware Funktion ausnutzen, um Anwendungen zu benachrichtigen, welche Endpunkt Geräte zu einem beliebigen Zeitpunkt vorhanden sind. Auf diese Weise entspricht der-Vorgang des Endpunkt-Managers dem des Plug & Play-Managers, der die Adapter Geräte nachverfolgt, die im System vorhanden sind.

In Windows Vista verfolgt das Audiosystem sowohl Endpunkt Geräte als auch Adapter Geräte. Der Endpunkt-Manager registriert Endpunkt Geräte, und der Plug & Play-Manager registriert Adapter Geräte. Durch das Registrieren von Endpunkt Geräten können benutzerfreundliche Anwendungen leichter auf die Endpunkt Geräte verweisen, die von Benutzern direkt bearbeitet werden, anstatt auf Adapter Geräte zu verweisen, die möglicherweise im Computer Chassis ausgeblendet sind. Die Endpunkt Geräte, die vom Betriebssystem gemeldet werden, verfolgen die dynamischen Änderungen an der Konfiguration von Audiohardware mit der Erkennung von Jack-Presence-Vorgängen. Während ein Endpunkt Gerät angeschlossen bleibt, listet das System dieses Gerät auf. Wenn der Benutzer die Plug-ins eines Endpunkt Geräts entbindet, beendet das System die Enumeration.

In früheren Versionen von Windows, einschließlich Windows 98, Windows Me, Windows 2000 und Windows XP, stellt das Systemanwendungen explizit nur PNP-Geräte zur Anwendung. Daher müssen Anwendungen das vorhanden sein von Endpunkt Geräten ableiten. Ein Betriebssystem, das keine explizite Unterstützung für Endpunkt Geräte hat, zwingt, dass Client Anwendungen mehr Arbeit selbst erledigen können. Beispielsweise muss eine audioerfassungs Anwendung die folgenden Schritte ausführen, um die Erfassung von einem externen Mikrofon zu ermöglichen:

1.  Zählen Sie alle audioerfassungs Geräte (diese sind Adapter Geräte), die zuvor vom PNP-Manager registriert wurden.
2.  Nachdem Sie ein Erfassungsgerät ausgewählt haben, öffnen Sie einen Erfassungsdaten Strom auf dem Gerät, indem Sie entweder die **waveinopen** -Funktion aufrufen oder die **DirectSound Capture** -oder DirectShow-API verwenden.
3.  Verwenden Sie die Funktion mixeropen, und verwenden Sie die anderen **mixerxxx** -Funktionen, um nach einer mixerline \_ componentType \_ src-Mikrofon Linie zu suchen, die \_ dem Erfassungsgerät entspricht, das in Schritt 2 geöffnet wurde. Dies ist eine fundierte Vermutung.
4.  Entsperren Sie den Dateipfad des Mikrofons. Wenn der Datenpfad einen stumm Knoten enthält, muss der Client die stumm Schaltung des Signals vom Mikrofon deaktivieren. Wenn das Erfassungsgerät einen Multiplexer zur Auswahl aus mehreren Eingaben enthält, muss der Client die Mikrofon Eingabe auswählen.

Dieser Prozess ist fehleranfällig, weil die Software, die diese Vorgänge ausführt, möglicherweise fehlschlägt, wenn eine Hardwarekonfiguration festgestellt wird, die von den Designern nicht erwartet wurde oder für die Sie nicht getestet wurde.

In Windows Vista, das Endpunkt Geräte unterstützt, ist das Herstellen einer Verbindung mit dem gleichen Endpunktgerät wesentlich einfacher:

1.  Wählen Sie ein Mikrofon aus einer Sammlung von Endpunkt Geräten aus.
2.  Aktiviert eine audioerfassungs-Schnittstelle auf dem Mikrofon.

Das Betriebssystem führt alle notwendigen Schritte aus, um das Endpunkt Gerät zu identifizieren und zu aktivieren. Wenn der Dateipfad des Mikrofons beispielsweise einen Multiplexer enthält, wählt das System automatisch die Mikrofon Eingabe für den Multiplexer aus.

Das Verhalten des Audiosubsystems ist zuverlässiger und deterministisch, wenn Anwendungen, anstatt eigene Endpunkt Identifizierungs Algorithmen zu implementieren, die Aufgabe der Identifizierung von Endpunkt Geräten auf das Betriebssystem verlagern können. Software Anbieter müssen nicht mehr überprüfen, ob Ihre Endpunkt Identifizierungs Algorithmen mit allen verfügbaren audiohardwaregeräten und-Konfigurationen ordnungsgemäß funktionieren – Sie können sich einfach auf das Betriebssystem für die Endpunkt Identifizierung stützen. Ebenso müssen Hardware Anbieter nicht mehr überprüfen, ob jede relevante Client Anwendung beliebige Endpunkt Geräte, die mit dem Audioadapter verbunden sind, leicht identifizieren kann – Sie müssen nur sicherstellen, dass das Betriebssystem ein Endpunkt Gerät identifizieren kann, das mit dem Audioadapter verbunden ist.

Die folgenden Themen enthalten zusätzliche Informationen zu audioendpunktgeräten:

-   [Informationen über die mmdevice-API](mmdevice-api.md)
-   [Auflisten von Audiogeräten](enumerating-audio-devices.md)
-   [Endpunkt-ID](endpoint-id-strings.md)
-   [Geräteeigenschaften](device-properties.md)
-   [Geräte Ereignisse](device-events.md)
-   [Geräte Rollen](device-roles.md)
-   [Geräte Formate](device-formats.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 



