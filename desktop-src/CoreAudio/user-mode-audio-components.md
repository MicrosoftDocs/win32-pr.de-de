---
description: User-Mode von Audiokomponenten
ms.assetid: b240b629-5bb6-4b07-95be-8ca5a14a3567
title: User-Mode von Audiokomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18715db2d32be3c4a70182571028acbfca411539
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861292"
---
# <a name="user-mode-audio-components"></a>User-Mode von Audiokomponenten

In Windows Vista dienen die Kern-audioapis als Grundlage für das Audiosubsystem im Benutzermodus. Die Kern-audioapis werden als schlanke Ebene von benutzermodussystemkomponenten implementiert, die Benutzermodusclients von Audiotreibern im Kernelmodus und Audiohardware trennen. Audio-APIs auf höherer Ebene, z. b. DirectSound und die Multimedia-Funktionen von Windows, greifen über die kernaudio-APIs auf Audiogeräte zu. Außerdem kommunizieren einige Audioanwendungen direkt mit den Kerncode-APIs.

Die wichtigsten audioapis unterstützen die benutzerfreundliche Darstellung eines audioendpunktgeräts. Bei einem audioendpunktgerät handelt es sich um eine Software Abstraktion, die ein physisches Gerät darstellt, das der Benutzer direkt bearbeitet. Beispiele für audioendpunktgeräte sind Sprecher, Kopfhörer und Mikrofon. Weitere Informationen finden Sie unter [audioendpunktgeräte](audio-endpoint-devices.md).

Im folgenden Diagramm werden die Kern-audioapis und deren Beziehung zu den anderen Audiokomponenten im Benutzermodus in Windows Vista veranschaulicht.

![Diagramm der benutzermodusaudiorenderingkomponenten](images/fig1.jpg)

Der Einfachheit halber zeigt das vorangehende Diagramm nur einen audiorenderingdatenpfad zum Endpunkt Gerät an – das Diagramm zeigt keinen Dateipfad für die Audioerfassung an. Zu den Kerncode-APIs zählen die [mmdevice-API](mmdevice-api.md), [WASAPI](wasapi.md), die [devicetopology-API](devicetopology-api.md)und die [endpointvolume-API](endpointvolume-api.md), die in den Audioses.dll-und Mmdevapi.dll benutzermodussystemmodulen implementiert werden.

Wie im obigen Diagramm gezeigt, stellen die Kerndatei-APIs eine Grundlage für die folgenden APIs auf höherer Ebene dar:

-   Media Foundation
-   Windows Multimedia **wavexxx** -und **mixerxxx** -Funktionen
-   DirectSound
-   DirectMusic

DirectSound, die Multimedia-Audiofunktionen von Windows und Media Foundation (über den Streaming-audiorenderer oder SAR, Component) kommunizieren direkt mit den kernaudio-APIs. DirectMusic kommuniziert indirekt über DirectSound mit den kernaudio-APIs.

Ein Client von WASAPI übergibt Daten über einen *Endpunkt Puffer* an ein Endpunkt Gerät. System Software und Hardwarekomponenten verwalten die Verschiebung der Daten vom Endpunkt Puffer auf das Endpunkt Gerät auf eine Weise, die für den Client weitgehend transparent ist. Außerdem kann der Client für ein Endpunkt Gerät, das in einen Audioadapter mit der Erkennung von Jack-Presence eingebunden ist, einen Endpunkt Puffer nur für ein physisch vorhandenes Endpunkt Gerät erstellen. Weitere Informationen zur Erkennung von Jack-Presence finden Sie unter [audioendpunktgeräte](audio-endpoint-devices.md).

Das vorangehende Diagramm zeigt zwei Typen von Endpunkt Puffern. Wenn ein Client von WASAPI einen Stream im frei *gegebenen Modus* öffnet, schreibt der Client Audiodaten in den Endpunkt Puffer, und die Windows-Audioengine liest die Daten aus dem Puffer. In diesem Modus gibt der Client die Audiohardware mit anderen Anwendungen frei, die in anderen Prozessen ausgeführt werden. Die Audioengine mischt die Streams aus diesen Anwendungen und gibt die resultierende Mischung über die Hardware wieder. Bei der Audioengine handelt es sich um eine Systemkomponente im Benutzermodus (Audiodg.dll), die alle Ihre streamverarbeitungs Vorgänge in der Software ausführt. Wenn ein Client dagegen einen Stream im *exklusiven Modus* öffnet, hat der Client exklusiven Zugriff auf die Audiohardware. In der Regel erfordert nur eine kleine Anzahl von "pro-Audiodaten" oder RTC-Anwendungen den exklusiven Modus. Obwohl im Diagramm sowohl der Datenstrom im freigegebenen als auch im exklusiven Modus angezeigt wird, ist nur einer der beiden Streams (und der zugehörige Endpunkt Puffer) vorhanden, abhängig davon, ob der Client den Datenstrom im freigegebenen Modus oder im exklusiven Modus öffnet.

Im exklusiven Modus kann der Client den Stream in jedem beliebigen Audioformat öffnen, das vom Endpunkt Gerät unterstützt wird. Im freigegebenen Modus muss der Client den Stream im Mischungs Format öffnen, das zurzeit von der Audioengine verwendet wird (oder ein Format, das dem Mischungs Format ähnelt). Die Eingabedaten Ströme der Audioengine und die Ausgabe Mischung aus der Engine befinden sich in diesem Format.

In Windows 7 wurde für Streams im Freigabe Modus ein neues Feature mit dem Namen " *niedriger Latenzmodus* " hinzugefügt. In diesem Modus wird das Audiomodul im Pullmodus ausgeführt, bei dem eine erhebliche Reduzierung der Latenz erfolgt. Dies ist sehr nützlich für Kommunikationsanwendungen, bei denen eine niedrige audiostreamwartezeit für schnelleres Streaming erforderlich ist.

Anwendungen, die Audiodatenströme mit geringer Latenz verwalten, können den Multimedia-Class Scheduler-Dienst (MMCSS) in Windows Vista verwenden, um die Priorität von Anwendungsthreads zu erhöhen, die auf Endpunkt Puffer zugreifen. Mit MMCSS können Audioanwendungen mit hoher Priorität ausgeführt werden, ohne dass CPU-Ressourcen für Anwendungen mit niedrigerer Priorität verweigert werden. MMCSS weist einem Thread eine Priorität auf der Grundlage seines Aufgaben namens zu. Windows Vista unterstützt z. b. die Aufgaben Namen "Audiodatei" und "pro-Audiodatei" für Threads, die Audiodatenströme verwalten. Standardmäßig ist die Priorität eines "pro-audiothreads" höher als der eines "audiothreads". Weitere Informationen zu MMCSS finden Sie in der Windows SDK-Dokumentation.

Die Core-audioapis unterstützen sowohl PCM-als auch nicht-PCM-Streamingformate. Die Audioengine kann jedoch nur PCM-Streams mischen. Folglich können nur exklusive streamingdatenströme nicht-PCM-Formate aufweisen. Weitere Informationen finden Sie unter [Geräte Formate](device-formats.md).

Die Audioengine wird in einem eigenen geschützten Prozess ausgeführt, der von dem Prozess getrennt ist, in dem die Anwendung ausgeführt wird. Um einen Stream im freigegebenen Modus zu unterstützen, ordnet der Windows-Audiodienst (das Feld mit der Bezeichnung "Audiodienst" im vorangehenden Diagramm) einen prozessübergreifenden Endpunkt Puffer zu, der sowohl für die Anwendung als auch für das Audiomodul zugänglich ist. Im exklusiven Modus befindet sich der Endpunkt Puffer im Arbeitsspeicher, der sowohl für die Anwendung als auch die Audiohardware zugänglich ist.

Der Windows-Audiodienst ist das Modul, das die Windows-audiorichtlinie implementiert. Bei der audiorichtlinie handelt es sich um einen Satz interner Regeln, die das System für die Interaktionen zwischen Audiodatenströmen aus mehreren Anwendungen anwendet, die gemeinsam mit derselben Audiohardware verwendet werden. Der Windows-Audiodienst implementiert eine audiorichtlinie durch Festlegen der Steuerelement Parameter für die Audioengine. Die Aufgaben des audiodienstanbieter umfassen Folgendes:

-   Nachverfolgen der Audiogeräte, die dem Benutzer hinzugefügt oder aus dem System entfernt werden.
-   Überwachen der Rollen, die den Audiogeräten im System zugewiesen sind.
-   Verwalten der Audiodatenströme aus Gruppen von Aufgaben, die ähnliche Klassen von Audioinhalten (Konsole, Multimedia und Kommunikation) entwickeln.
-   Steuern der Volumeebene des kombinierten Ausgabestreams ("Submix") für jeden der verschiedenen Arten von Audioinhalten.
-   Informieren der Audioengine über die Verarbeitungs Elemente in den Daten Pfaden für die Audiodatenströme.

In einigen Versionen von Windows ist der Windows-Audiodienst standardmäßig deaktiviert und muss explizit aktiviert werden, bevor das System Audioinhalte wiedergeben kann.

Im Beispiel im obigen Diagramm ist das Endpunkt Gerät ein Satz von Referenten, die an den Audioadapter angeschlossen sind. Die Client Anwendung schreibt Audiodaten in den Endpunkt Puffer, und die Audioengine verarbeitet die Details zum Transportieren der Daten aus dem Puffer auf das Endpunkt Gerät.

Das Feld mit der Bezeichnung "Audiotreiber" im vorangehenden Diagramm kann eine Kombination aus vom System bereitgestellten und vom Hersteller bereitgestellten Treiber Komponenten sein. Bei einem Audioadapter auf einem PCI-oder PCI-Express-Bus stellt das System den Port Klassensystem Treiber (Portcls.sys) bereit, der einen Satz von Port Treibern für die verschiedenen Audiofunktionen im Adapter implementiert, und der Hardwarehersteller stellt einen Adapter Treiber bereit, der einen Satz von Mini Port-Treibern implementiert, um gerätespezifische Vorgänge für die Port Treiber zu verarbeiten. Bei einem High Definition-Audiocontroller und-Codec auf einem PCI-oder PCI-Express-Bus liefert das System den Adapter Treiber (Hdaudio.sys), und es ist kein vom Hersteller bereitgestellter Treiber erforderlich. Bei einem Audioadapter auf einem USB-Bus liefert das System den System Treiber der AVStream-Klasse (Ks.sys) und den USB-Audiotreiber (Usbaudio.sys). auch hier ist kein vom Hersteller bereitgestellter Treiber erforderlich.

Der Einfachheit halber zeigt das vorangehende Diagramm nur renderingstreams an. Die wichtigsten audioapis unterstützen jedoch auch Erfassungsdaten Ströme. Im Modus "freigegeben" können mehrere Clients den erfassten Stream von einem audiohardwaregerät freigeben. Im exklusiven Modus hat ein Client exklusiven Zugriff auf den aufgezeichneten Stream vom Gerät aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 



