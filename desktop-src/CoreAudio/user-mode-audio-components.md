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

In Windows Vista dienen die Kernaudio-APIs als Grundlage für das Audiosubsystem im Benutzermodus. Die Kernaudio-APIs werden als schlanke Schicht von Systemkomponenten im Benutzermodus implementiert, die Clients im Benutzermodus von Kernelmodus-Audiotreibern und Audiohardware trennen. Audio-APIs auf höherer Ebene, z. B. DirectSound und Windows Multimediafunktionen, greifen über die Kernaudio-APIs auf Audiogeräte zu. Darüber hinaus kommunizieren einige Audioanwendungen direkt mit den Kernaudio-APIs.

Die Kernaudio-APIs unterstützen das benutzerfreundliche Konzept eines Audioendpunktgeräts. Ein Audioendpunktgerät ist eine Softwareabstraktion, die ein physisches Gerät darstellt, das der Benutzer direkt bearbeitet. Beispiele für Audioendpunktgeräte sind Lautsprecher, Mikrofone und Mikrofone. Weitere Informationen finden Sie unter [AudioEndpunktgeräte](audio-endpoint-devices.md).

Das folgende Diagramm zeigt die wichtigsten Audio-APIs und ihre Beziehung zu den anderen Audiokomponenten im Benutzermodus in Windows Vista.

![Diagramm der Audiorenderingkomponenten im Benutzermodus](images/fig1.jpg)

Der Einfachheit halber zeigt das obige Diagramm nur einen Audiorendering-Datenpfad zum Endpunktgerät. Das Diagramm zeigt keinen Audioerfassungsdatenpfad. Zu den Kernaudio-APIs gehören die [MMDevice-API,](mmdevice-api.md) [WASAPI,](wasapi.md)die [DeviceTopology-API](devicetopology-api.md)und die [EndpointVolume-API,](endpointvolume-api.md)die in den Audioses.dll- und Mmdevapi.dll-Systemmodulen im Benutzermodus implementiert sind.

Wie im obigen Diagramm gezeigt, bilden die Kernaudio-APIs eine Grundlage für die folgenden APIs auf höherer Ebene:

-   Media Foundation
-   Windows multimedia **waveXxx- und** **mixerXxx-Funktionen**
-   Directsound
-   Directmusic

DirectSound, das Windows Multimedia-Audiofunktionen, und Media Foundation (über den Streamingaudiorenderer oder sar-Komponente) kommunizieren direkt mit den Kernaudio-APIs. DirectGuide kommuniziert indirekt über DirectSound mit den Kernaudio-APIs.

Ein WASAPI-Client übergibt Daten über einen Endpunktpuffer an *ein Endpunktgerät.* Systemsoftware- und Hardwarekomponenten verwalten das Übertragen von Daten aus dem Endpunktpuffer auf das Endpunktgerät auf eine Weise, die für den Client größtenteils transparent ist. Darüber hinaus kann der Client für ein Endpunktgerät, das sich an einen Audioadapter mit Erkennung des Vorhandenseins von Klinken angeschlossen hat, einen Endpunktpuffer nur für ein endpunktbasiertes Gerät erstellen, das physisch vorhanden ist. Weitere Informationen zur Erkennung des Vorhandenseins von Jacken finden Sie unter [AudioEndpunktgeräte](audio-endpoint-devices.md).

Das obige Diagramm zeigt zwei Arten von Endpunktpuffern. Wenn ein WASAPI-Client einen Stream im freigegebenen Modus *öffnet,* schreibt der Client Audiodaten in den Endpunktpuffer, und die Windows-Audio-Engine liest die Daten aus dem Puffer. In diesem Modus teilt der Client die Audiohardware mit anderen Anwendungen, die in anderen Prozessen ausgeführt werden. Die Audio-Engine gemischt die Datenströme aus diesen Anwendungen und gibt die resultierende Mischung über die Hardware wieder. Die Audio-Engine ist eine Systemkomponente im Benutzermodus (Audiodg.dll), die alle Datenstromverarbeitungsvorgänge in Software ausführt. Wenn ein Client dagegen einen Stream im exklusiven Modus *öffnet,* hat der Client exklusiven Zugriff auf die Audiohardware. In der Regel erfordert nur eine kleine Anzahl von Pro-Audio- oder RTC-Anwendungen den exklusiven Modus. Obwohl das Diagramm sowohl die Streams im freigegebenen modus als auch im exklusiven Modus zeigt, ist nur einer dieser beiden Streams (und der entsprechende Endpunktpuffer) vorhanden, je nachdem, ob der Client den Stream im modus shared oder im exklusiven Modus öffnet.

Im exklusiven Modus kann der Client den Stream in einem beliebigen Audioformat öffnen, das vom Endpunktgerät unterstützt wird. Im modus shared muss der Client den Stream im Mischungsformat öffnen, das derzeit von der Audio-Engine verwendet wird (oder ein Format, das dem Mischungsformat ähnelt). Die Eingabestreams der Audio-Engine und die Ausgabemischung der Engine liegen alle in diesem Format vor.

In Windows 7 wurde ein neues  Feature namens Modus mit geringer Latenz für Streams im Freigabemodus hinzugefügt. In diesem Modus wird die Audio-Engine im Pullmodus ausgeführt, in dem die Latenz deutlich reduziert wird. Dies ist sehr nützlich für Kommunikationsanwendungen, die eine niedrige Audiostreamlatenz für schnelleres Streaming erfordern.

Anwendungen, die Audiostreams mit geringer Latenz verwalten, können den Multimedia Class Scheduler Service (MMCSS) in Windows Vista verwenden, um die Priorität von Anwendungsthreads zu erhöhen, die auf Endpunktpuffer zugreifen. MIT MMCSS können Audioanwendungen mit hoher Priorität ausgeführt werden, ohne DASS CPU-Ressourcen für Anwendungen mit niedrigerer Priorität verweigert werden. MMCSS weist einem Thread basierend auf seinem Aufgabennamen eine Priorität zu. Beispielsweise unterstützt Windows Vista die Aufgabennamen "Audio" und "Pro Audio" für Threads, die Audiostreams verwalten. Standardmäßig ist die Priorität eines "Pro Audio"-Threads höher als die eines Audiothreads. Weitere Informationen zu MMCSS finden Sie in der Dokumentation Windows SDK.

Die Kernaudio-APIs unterstützen sowohl PCM- als auch Nicht-PCM-Streamformate. Die Audio-Engine kann jedoch nur PCM-Streams mischen. Daher können nur Streams im exklusiven Modus Nicht-PCM-Formate haben. Weitere Informationen finden Sie unter [Geräteformate.](device-formats.md)

Die Audio-Engine wird in einem eigenen geschützten Prozess ausgeführt, der von dem Prozess getrennt ist, in dem die Anwendung ausgeführt wird. Zur Unterstützung eines Streams im freigegebenen Modus weist der Windows-Audiodienst (das Feld mit der Bezeichnung "Audiodienst" im obigen Diagramm) einen prozessübergreifenden Endpunktpuffer zu, auf den sowohl die Anwendung als auch die Audio-Engine zugreifen können. Im exklusiven Modus befindet sich der Endpunktpuffer im Arbeitsspeicher, auf den sowohl die Anwendung als auch die Audiohardware zugreifen können.

Der Windows Audiodienst ist das Modul, das die Windows implementiert. Bei der Audiorichtlinie handelt es sich um eine Reihe interner Regeln, die das System für die Interaktionen zwischen Audiostreams aus mehreren Anwendungen verwendet, die dieselbe Audiohardware gemeinsam nutzen und um diese konkurrieren. Der Windows-Audiodienst implementiert die Audiorichtlinie, indem die Steuerungsparameter für die Audio-Engine festgelegt werden. Zu den Aufgaben des Audiodiensts gehören:

-   Nachverfolgen der Audiogeräte, die der Benutzer dem System hinzufügt oder daraus entfernt.
-   Überwachen der Rollen, die den Audiogeräten im System zugewiesen sind.
-   Verwalten der Audiostreams aus Aufgabengruppen, die ähnliche Klassen von Audioinhalten erzeugen (Konsole, Multimedia und Kommunikation).
-   Steuern der Lautstärke des kombinierten Ausgabestreams ("Submix") für jeden der verschiedenen Arten von Audioinhalten.
-   Informieren der Audio-Engine über die Verarbeitungselemente in den Datenpfaden für die Audiostreams.

In einigen Versionen von Windows ist der Windows-Audiodienst standardmäßig deaktiviert und muss explizit aktiviert werden, bevor das System Audio wieder geben kann.

Im beispiel im obigen Diagramm ist das Endpunktgerät eine Reihe von Lautsprechern, die an den Audioadapter angeschlossen sind. Die Clientanwendung schreibt Audiodaten in den Endpunktpuffer, und die Audio-Engine verarbeitet die Details zum Transport der Daten vom Puffer zum Endpunktgerät.

Das Feld mit der Bezeichnung "Audio Driver" (Audiotreiber) im obigen Diagramm kann eine Kombination aus vom System bereitgestellten und vom Anbieter bereitgestellten Treiberkomponenten sein. Bei einem Audioadapter auf einem PCI- oder PCI Express-Bus stellt das System den Portklassen-Systemtreiber (Portcls.sys) zur Verfügung, der eine Reihe von Porttreibern für die verschiedenen Audiofunktionen im Adapter implementiert, und der Hardwareanbieter stellt einen Adaptertreiber zur Verfügung, der einen Satz von Miniporttreibern implementiert, um gerätespezifische Vorgänge für die Porttreiber zu verarbeiten. Bei einem High Definition Audio Controller und Codec auf einem PCI- oder PCI Express-Bus stellt das System den Adaptertreiber (Hdaudio.sys) zur Verfügung, und es ist kein vom Anbieter bereitgestellter Treiber erforderlich. Bei einem Audioadapter auf einem USB-Bus stellt das System den AVStream-Klassensystemtreiber (Ks.sys) sowie den USB-Audiotreiber (Usbaudio.sys) zur Usbaudio.sys). auch hier ist kein vom Anbieter bereitgestellter Treiber erforderlich.

Der Einfachheit halber zeigt das obige Diagramm nur Renderingstreams. Die Kernaudio-APIs unterstützen jedoch auch Erfassungsstreams. Im modus shared können mehrere Clients den erfassten Datenstrom von einem Audiohardwaregerät freigeben. Im exklusiven Modus hat ein Client exklusiven Zugriff auf den erfassten Datenstrom vom Gerät.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 



