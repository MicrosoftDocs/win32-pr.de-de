---
description: User-Mode Audiokomponenten
ms.assetid: b240b629-5bb6-4b07-95be-8ca5a14a3567
title: User-Mode Audiokomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8768cb6ece5825ae48803f30d8c1631a2e593f40815565b5dc879d23afd961aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166030"
---
# <a name="user-mode-audio-components"></a>User-Mode Audiokomponenten

In Windows Vista dienen die Kernaudio-APIs als Grundlage für das Audiosubsystem im Benutzermodus. Die Kernaudio-APIs werden als schlanke Schicht von Systemkomponenten im Benutzermodus implementiert, die Benutzermodusclients von Kernelmodus-Audiotreibern und Audiohardware trennen. Audio-APIs auf höherer Ebene, z. B. DirectSound und die Windows Multimediafunktionen, greifen über die Kernaudio-APIs auf Audiogeräte zu. Darüber hinaus kommunizieren einige Audioanwendungen direkt mit den Kernaudio-APIs.

Die Kernaudio-APIs unterstützen das benutzerfreundliche Konzept eines Audioendpunktgeräts. Ein Audioendpunktgerät ist eine Softwareabstraktion, die ein physisches Gerät darstellt, das der Benutzer direkt bearbeitet. Beispiele für Audioendpunktgeräte sind Lautsprecher, Lautsprecher und Mikrofone. Weitere Informationen finden Sie unter [Audioendpunktgeräte](audio-endpoint-devices.md).

Das folgende Diagramm zeigt die Kernaudio-APIs und ihre Beziehung zu den anderen Audiokomponenten im Benutzermodus in Windows Vista.

![Diagramm der Audiorenderingkomponenten im Benutzermodus](images/fig1.jpg)

Der Einfachheit halber zeigt das obige Diagramm nur einen Audiorenderingdatenpfad zum Endpunktgerät– das Diagramm zeigt keinen Audioaufnahmedatenpfad an. Zu den Kernaudio-APIs gehören die [MMDevice-API,](mmdevice-api.md) [WASAPI,](wasapi.md)die [DeviceTopology-API](devicetopology-api.md)und die [EndpointVolume-API,](endpointvolume-api.md)die in den Systemmodulen Audioses.dll und Mmdevapi.dll Benutzermodus implementiert werden.

Wie im obigen Diagramm dargestellt, bilden die Kernaudio-APIs eine Grundlage für die folgenden APIs auf höherer Ebene:

-   Media Foundation
-   Windows **Multimediafunktionen waveXxx** und **mixerXxx**
-   Directsound
-   Directmusic

DirectSound, die Windows Multimedia-Audiofunktionen und Media Foundation (über den Streamingaudiorenderer oder die SAR-Komponente) kommunizieren direkt mit den Kernaudio-APIs. DirectCast kommuniziert indirekt über DirectSound mit den Kernaudio-APIs.

Ein Client von WASAPI übergibt Daten über einen *Endpunktpuffer* an ein Endpunktgerät. Systemsoftware- und Hardwarekomponenten verwalten das Verschieben von Daten aus dem Endpunktpuffer zum Endpunktgerät auf eine Weise, die für den Client weitgehend transparent ist. Darüber hinaus kann der Client für ein Endpunktgerät, das an einen Audioadapter mit Jack-Presence-Erkennung angeschlossen ist, einen Endpunktpuffer nur für ein physisch vorhandenes Endpunktgerät erstellen. Weitere Informationen zur Erkennung von Jack-Presence finden Sie unter [Audioendpunktgeräte.](audio-endpoint-devices.md)

Das obige Diagramm zeigt zwei Typen von Endpunktpuffern. Wenn ein Client von WASAPI einen Stream im *freigegebenen Modus* öffnet, schreibt der Client Audiodaten in den Endpunktpuffer, und die Windows Audio-Engine liest die Daten aus dem Puffer. In diesem Modus verwendet der Client die Audiohardware gemeinsam mit anderen Anwendungen, die in anderen Prozessen ausgeführt werden. Die Audio-Engine kombiniert die Streams aus diesen Anwendungen und gibt die resultierende Mischung über die Hardware wieder. Die Audio-Engine ist eine Systemkomponente im Benutzermodus (Audiodg.dll), die alle Datenstromverarbeitungsvorgänge in Software ausführt. Wenn ein Client dagegen einen Stream im *exklusiven Modus* öffnet, hat der Client exklusiven Zugriff auf die Audiohardware. In der Regel erfordert nur eine kleine Anzahl von "Pro-Audio"- oder RTC-Anwendungen den exklusiven Modus. Obwohl das Diagramm die Datenströme im freigegebenen Modus und im exklusiven Modus zeigt, ist nur einer dieser beiden Datenströme (und der entsprechende Endpunktpuffer) vorhanden, je nachdem, ob der Client den Datenstrom im freigegebenen Modus oder im exklusiven Modus öffnet.

Im exklusiven Modus kann der Client den Stream in einem beliebigen Audioformat öffnen, das das Endpunktgerät unterstützt. Im freigegebenen Modus muss der Client den Stream im Mischungsformat öffnen, das derzeit von der Audio-Engine verwendet wird (oder in einem Format, das dem Mischungsformat ähnelt). Die Eingabestreams der Audio-Engine und die Ausgabemischung der Engine haben alle dieses Format.

In Windows 7 wurde ein neues Feature namens Modus mit *niedriger Latenz* für Streams im Freigabemodus hinzugefügt. In diesem Modus wird die Audio-Engine im Pullmodus ausgeführt, in dem die Latenz deutlich reduziert wird. Dies ist sehr nützlich für Kommunikationsanwendungen, die eine niedrige Audiostreamlatenz für schnelleres Streaming erfordern.

Anwendungen, die Audiostreams mit geringer Latenz verwalten, können den Multimedia Class Scheduler Service (MMCSS) in Windows Vista verwenden, um die Priorität von Anwendungsthreads zu erhöhen, die auf Endpunktpuffer zugreifen. MIT MMCSS können Audioanwendungen mit hoher Priorität ausgeführt werden, ohne CPU-Ressourcen für Anwendungen mit niedrigerer Priorität zu verweigern. MMCSS weist einem Thread basierend auf seinem Aufgabennamen eine Priorität zu. Beispielsweise unterstützt Windows Vista die Aufgabennamen "Audio" und "Pro Audio" für Threads, die Audiostreams verwalten. Standardmäßig ist die Priorität eines "Pro Audio"-Threads höher als die eines "Audio"-Threads. Weitere Informationen zu MMCSS finden Sie in der Windows SDK-Dokumentation.

Die Kernaudio-APIs unterstützen sowohl PCM- als auch Nicht-PCM-Streamformate. Die Audio-Engine kann jedoch nur PCM-Streams mischen. Daher können nur Streams im exklusiven Modus Nicht-PCM-Formate aufweisen. Weitere Informationen finden Sie unter [Geräteformate.](device-formats.md)

Die Audio-Engine wird in einem eigenen geschützten Prozess ausgeführt, der von dem Prozess getrennt ist, in dem die Anwendung ausgeführt wird. Um einen Datenstrom im freigegebenen Modus zu unterstützen, ordnet der Windows Audiodienst (im obigen Diagramm das Feld mit der Bezeichnung "Audiodienst") einen prozessübergreifenden Endpunktpuffer zu, auf den sowohl die Anwendung als auch die Audio-Engine zugreifen können. Für den exklusiven Modus befindet sich der Endpunktpuffer im Arbeitsspeicher, auf den sowohl die Anwendung als auch die Audiohardware zugreifen können.

Der Windows Audiodienst ist das Modul, das Windows Audiorichtlinie implementiert. Bei der Audiorichtlinie handelt es sich um eine Reihe interner Regeln, die das System auf die Interaktionen zwischen Audiostreams aus mehreren Anwendungen anwendet, die die gleiche Audiohardware gemeinsam nutzen und um die Verwendung derselben Audiohardware konkurrieren. Der Windows Audiodienst implementiert eine Audiorichtlinie, indem die Steuerungsparameter für die Audio-Engine festgelegt werden. Die Aufgaben des Audiodiensts umfassen Folgendes:

-   Nachverfolgen der Audiogeräte, die der Benutzer dem System hinzufügt oder daraus entfernt.
-   Überwachen der Rollen, die den Audiogeräten im System zugewiesen sind.
-   Verwalten der Audiodatenströme aus Aufgabengruppen, die ähnliche Klassen von Audioinhalten erzeugen (Konsole, Multimedia und Kommunikation).
-   Steuern der Volumeebene des kombinierten Ausgabestreams ("submix") für jeden der verschiedenen Arten von Audioinhalten.
-   Informieren der Audio-Engine über die Verarbeitungselemente in den Datenpfaden für die Audiostreams.

In einigen Versionen von Windows ist der Windows Audiodienst standardmäßig deaktiviert und muss explizit aktiviert werden, bevor das System Audio wiedergeben kann.

Im Beispiel im obigen Diagramm ist das Endpunktgerät eine Reihe von Lautsprechern, die an den Audioadapter angeschlossen sind. Die Clientanwendung schreibt Audiodaten in den Endpunktpuffer, und die Audio-Engine verarbeitet die Details des Transports der Daten aus dem Puffer an das Endpunktgerät.

Das Feld mit der Bezeichnung "Audiotreiber" im vorherigen Diagramm kann eine Kombination aus vom System bereitgestellten und vom Hersteller bereitgestellten Treiberkomponenten sein. Im Fall eines Audioadapters auf einem PCI- oder PCI-Express-Bus stellt das System den Portklassen-Systemtreiber (Portcls.sys) bereit, der eine Reihe von Porttreibern für die verschiedenen Audiofunktionen im Adapter implementiert, und der Hardwarehersteller stellt einen Adaptertreiber bereit, der eine Reihe von Miniporttreibern implementiert, um gerätespezifische Vorgänge für die Porttreiber zu verarbeiten. Bei einem High Definition Audio Controller und Codec auf einem PCI- oder PCI Express-Bus stellt das System den Adaptertreiber (Hdaudio.sys) zur Verfügung, und es ist kein vom Anbieter bereitgestellter Treiber erforderlich. Im Fall eines Audioadapters auf einem USB-Bus stellt das System den AVStream-Klassensystemtreiber (Ks.sys) sowie den USB-Audiotreiber (Usbaudio.sys) zur Verfügung. auch hier ist kein vom Anbieter bereitgestellter Treiber erforderlich.

Der Einfachheit halber zeigt das obige Diagramm nur das Rendern von Datenströmen. Die Kernaudio-APIs unterstützen jedoch auch Erfassungsstreams. Im freigegebenen Modus können mehrere Clients den erfassten Datenstrom von einem Audiohardwaregerät freigeben. Im exklusiven Modus hat ein Client exklusiven Zugriff auf den erfassten Stream vom Gerät.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 



