---
description: Audioendpunktgeräte
ms.assetid: 773714fb-3b00-4f03-988f-05c5835f87cf
title: Audioendpunktgeräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11145227ff4f6cf4eb7dd11342e28b3a8260aac95c41b32faed6b2d6bd414dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407330"
---
# <a name="audio-endpoint-devices"></a>Audioendpunktgeräte

Der Begriff *Endpunktgerät* bezieht sich auf ein Hardwaregerät, das sich an einem Ende eines Datenpfads befindet, der aus einem Anwendungsprogramm stammt oder beendet wird. Beispiele für Audioendpunktgeräte sind Lautsprecher, Lautsprecher, Mikrofone und CD-Player. Die Audiodaten, die sich entlang des Datenpfads bewegen, können während der Reise zwischen der Anwendung und dem Endpunktgerät eine Reihe von Software- und Hardwarekomponenten durchlaufen. Obwohl diese Komponenten für den Betrieb des Endpunktgeräts wichtig sind, sind sie in der Regel für Benutzer unsichtbar. Benutzer denken eher an Endpunktgeräte, die sie direkt bearbeiten, als an die Geräte auf Audioadaptern, an die die Endpunktgeräte angeschlossen sind, oder an die Softwarekomponenten, die die Audiostreams verarbeiten, die zu und von diesen Adaptern fließen.

Um Verwirrung mit Endpunktgeräten zu vermeiden, bezieht sich diese Dokumentation auf ein Gerät auf einem Audioadapter als *Adaptergerät.*

Das folgende Diagramm zeigt, wie sich Audioendpunktgeräte von Adaptergeräten unterscheiden.

![Beispiele für Audioendpunktgeräte und Adaptergeräte](images/devices.jpg)

Im obigen Diagramm sind die folgenden Beispiele für Endpunktgeräte aufgeführt:

-   Speakers
-   Mikrofon
-   Hilfseingabegerät

Im Folgenden sind Beispiele für Adaptergeräte aufgeführt:

-   Wellenausgabegerät (enthält digital-zu-analog-Konverter)
-   Ausgabesteuerelement (enthält Lautstärke- und Stummschaltungssteuerelemente)
-   Welleneingabegerät (enthält Analog-digital-Konverter)
-   Eingabesteuerelement (enthält Volumesteuerung und Multiplexer)

In der Regel beziehen sich die Benutzeroberflächen von Audioanwendungen auf Audioendpunktgeräte, nicht auf Adaptergeräte. Windows Vista vereinfacht den Entwurf benutzerfreundlicher Anwendungen, indem die Endpunktgeräteabstraktion direkt unterstützt wird.

Einige Endpunktgeräte stellen möglicherweise dauerhaft eine Verbindung mit einem Adaptergerät her. Beispielsweise kann ein Computer interne Geräte wie einen CD-Player, ein Mikrofon oder Lautsprecher enthalten, die in das Systemgehäuse integriert sind. In der Regel entfernt der Benutzer diese Endpunktgeräte nicht physisch.

Andere Endpunktgeräte stellen möglicherweise über Audiobuchsen eine Verbindung mit einem Audioadapter her. Der Benutzer schließt diese externen Geräte ein und entpackt sie. Beispielsweise befindet sich ein Audioendpunktgerät wie ein externes Mikrofon oder ein Kabel an einem Ende eines Kabels, dessen anderes Ende an eine Buchse auf einem Adaptergerät angeschlossen ist.

Der Adapter kommuniziert mit dem Systemprozessor über einen Systembus (in der Regel PCI oder PCI Express) oder einen externen Bus (USB oder IEEE 1394), der Plug & Play (PnP) unterstützt. Während der Geräteenumeration identifiziert der Plug & Play-Manager die Geräte im Audioadapter und registriert diese Geräte, um sie für die Verwendung durch das Betriebssystem und anwendungen verfügbar zu machen.

Im Gegensatz zur Verbindung zwischen einem Adapter und einem externen Bus wie USB oder dem IEEE 1394 Bus unterstützt die Verbindung zwischen einem Endpunktgerät und einem Adaptergerät keine PnP-Geräteerkennung. Einige Audioadapter unterstützen jedoch die Erkennung des Vorhandenseins von *Klinken:* Wenn ein Stecker in eine Buchse eingefügt oder aus einer Buchse entfernt wird, generiert die Hardware einen Interrupt, um den Adaptertreiber über die Änderung der Hardwarekonfiguration zu informieren. Der Endpunkt-Manager in Windows Vista kann diese Hardwarefunktion nutzen, um Anwendungen zu benachrichtigen, welche Endpunktgeräte jederzeit vorhanden sind. Auf diese Weise entspricht der Vorgang des Endpunkt-Managers dem des Plug & Play-Managers, der die im System vorhandenen Adaptergeräte nachverfolgt.

In Windows Vista verfolgt das Audiosystem sowohl Endpunktgeräte als auch Adaptergeräte nach. Der Endpunkt-Manager registriert Endpunktgeräte, und der Plug & Play-Manager registriert Adaptergeräte. Durch das Registrieren von Endpunktgeräten können Benutzer benutzerfreundliche Anwendungen einfacher auf die Endpunktgeräte verweisen, die Benutzer direkt bearbeiten, anstatt auf Adaptergeräte zu verweisen, die möglicherweise im Gehäuse des Computers verborgen sind. Die Endpunktgeräte, die vom Betriebssystem gemeldet werden, verfolgen dynamisch Änderungen an der Konfiguration der Audiohardware nach, die über eine Erkennung von Jack-Presence verfügt. Während ein Endpunktgerät angeschlossen bleibt, zählt das System dieses Gerät auf. Wenn der Benutzer ein Endpunktgerät entpackt, beendet das System die Aufzählung.

In früheren Versionen von Windows, einschließlich Windows 98, Windows Me, Windows 2000 und Windows XP, stellt das System anwendungen explizit nur PNP-Geräte zur Verfügung. Daher müssen Anwendungen das Vorhandensein von Endpunktgeräten ableiten. Ein Betriebssystem, das keine explizite Unterstützung für Endpunktgeräte hat, zwingt Clientanwendungen, mehr arbeite selbst zu erledigen. Beispielsweise muss eine Audioaufnahmeanwendung die folgenden Schritte ausführen, um die Erfassung über ein externes Mikrofon zu aktivieren:

1.  Aufzählen aller Audioaufnahmegeräte (hierbei handelt es sich um Adaptergeräte), die zuvor vom PnP-Manager registriert wurden.
2.  Nachdem Sie ein Erfassungsgerät ausgewählt haben, öffnen Sie einen Erfassungsstream auf dem Gerät, indem Sie entweder die **waveInOpen-Funktion** aufrufen oder die **DirectSoundCapture-** oder DirectShow-API verwenden.
3.  Rufen Sie die mixerOpen-Funktion auf, und verwenden Sie die anderen **mixerXxx-Funktionen,** um nach einer MIXERLINE \_ COMPONENTTYPE \_ SRC \_ MICROPHONE-Zeile zu suchen, die dem in Schritt 2 geöffneten Erfassungsgerät entspricht. Dies ist eine fundierte Schätzung.
4.  Entsperren Sie die Blockierung des Datenpfads über das Mikrofon. Wenn der Datenpfad einen stummgeschalteten Knoten enthält, muss der Client das Stummschalten des Signals über das Mikrofon deaktivieren. Wenn das Erfassungsgerät einen Multiplexer für die Auswahl aus mehreren Eingaben enthält, muss der Client die Mikrofoneingabe auswählen.

Dieser Prozess ist fehleranfällig, da die Software, die diese Vorgänge ausführt, fehlschlagen kann, wenn eine Hardwarekonfiguration gefunden wird, die die Designer nicht erwartet haben oder für die sie nicht getestet wurde.

In Windows Vista, das Endpunktgeräte unterstützt, ist der Verbindungsvorgang mit demselben Endpunktgerät viel einfacher:

1.  Wählen Sie ein Mikrofon aus einer Sammlung von Endpunktgeräten aus.
2.  Aktivieren Sie eine Audioaufnahmeschnittstelle für dieses Mikrofon.

Das Betriebssystem führt alle erforderlichen Maßnahmen aus, um das Endpunktgerät zu identifizieren und zu aktivieren. Wenn beispielsweise der Datenpfad vom Mikrofon einen Multiplexer enthält, wählt das System automatisch die Mikrofoneingabe für den Multiplexer aus.

Das Verhalten des Audiosubsystems ist zuverlässiger und deterministischer, wenn Anwendungen anstelle der Implementierung eigener Endpunktidentifikationsalgorithmen die Aufgabe der Identifizierung von Endpunktgeräten an das Betriebssystem verwerfen können. Softwarehersteller müssen nicht mehr überprüfen, ob ihre Endpunktidentifikationsalgorithmen mit allen verfügbaren Audiohardwaregeräten und -konfigurationen ordnungsgemäß funktionieren. Sie können sich bei der Endpunktidentifikation einfach auf das Betriebssystem verlassen. Ebenso müssen Hardwarehersteller nicht mehr überprüfen, ob jede relevante Clientanwendung alle Endpunktgeräte identifizieren kann, die mit ihrem Audioadapter verbunden sind. Sie müssen lediglich überprüfen, ob das Betriebssystem ein Endpunktgerät identifizieren kann, das mit dem Audioadapter verbunden ist.

Die folgenden Themen enthalten zusätzliche Informationen zu Audioendpunktgeräten:

-   [Informationen zur MMDevice-API](mmdevice-api.md)
-   [Aufzählen von Audiogeräten](enumerating-audio-devices.md)
-   [Endpunkt-ID-Zeichenfolgen](endpoint-id-strings.md)
-   [Geräteeigenschaften](device-properties.md)
-   [Geräteereignisse](device-events.md)
-   [Geräterollen](device-roles.md)
-   [Geräteformate](device-formats.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 



