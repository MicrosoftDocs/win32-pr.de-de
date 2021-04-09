---
description: Loopback Aufzeichnung
ms.assetid: 71c567f7-fffa-4b75-897a-63ed30c4c9b0
title: Loopback Aufzeichnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374da7497096118905f5e4c79bbacda832a42a7b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958504"
---
# <a name="loopback-recording"></a>Loopback Aufzeichnung

Im Loopback Modus kann ein Client von WASAPI den Audiostream erfassen, der von einem renderingendpunktgerät abgespielt wird. Um einen Stream im Loopback Modus zu öffnen, muss der Client folgende Aktionen ausführen:

-   Abrufen einer [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle für das renderingendpunktgerät.
-   Initialisieren eines Aufzeichnungsdaten Stroms im Loopback Modus auf dem Rendering-Endpunkt Gerät.

Nachdem Sie diese Schritte ausgeführt haben, kann der Client die [**iaudioclient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) -Methode aufrufen, um eine [**iaudiocaptureclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) -Schnittstelle auf dem renderingendpunktgerät zu erhalten.

WASAPI bietet den Loopback Modus hauptsächlich zur Unterstützung von akustischem Echo Abbruch (AEC). Andere Arten von Audioanwendungen können jedoch den Loopback Modus für die Erfassung der System Mischung, die von der Audioengine abgespielt wird, nützlich finden.

Im Codebeispiel zum [Erfassen eines Streams](capturing-a-stream.md)kann die recordaudiostream-Funktion problemlos geändert werden, um einen Aufzeichnungsdaten Strom im Loopback Modus zu konfigurieren. Folgende Änderungen sind erforderlich:

-   Ändern Sie im Aufrufen der Methode [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) den ersten Parameter (*DataFlow*) von ecapture in.
-   Ändern Sie im Aufrufen der [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode den Wert des zweiten Parameters (*StreamFlags*) von 0 in das audclnt \_ StreamFlags- \_ Loopback.

In Windows-Versionen vor Windows 10 1703 empfängt der Pull-Modus-Erfassungs Client keine Ereignisse, wenn ein Stream mit Ereignis gesteuerter Pufferung initialisiert wird und Loopback aktiviert ist. Um dieses Problem zu umgehen, initialisieren Sie einen renderingstream im ereignisgesteuerten Modus. Jedes Mal, wenn der Client ein Ereignis für den RenderStream empfängt, muss er dem Erfassungs Client signalisieren, den Erfassungs Thread auszuführen, der den nächsten Satz von Beispielen aus dem Erfassungs Endpunkt Puffer liest. In Windows 10, Version 1703 und höher, werden ereignisgesteuerte Loopback Clients unterstützt und benötigen nicht mehr die Problem Umgehung, die den Rendering-Stream einschließt.  

Ein Client kann den Loopback Modus nur für einen Datenstrom im freigegebenen Modus aktivieren ("audclnt \_ sharemode \_ Shared"). Stream im exklusiven Modus kann nicht im Loopback Modus verwendet werden.

Die Implementierung von Loopback durch WASAPI hängt von den Funktionen der Hardware ab. Wenn die Hardware eine Loopback-PIN auf dem Rendering-Endpunkt unterstützt, verwendet WASAPI die Audiodaten, die in dieser PIN für den Loopback-Stream bereitgestellt werden. Wenn die Hardware keine Loopback-Pin unterstützt, kopiert WASAPI den Ausgabedatenstrom aus der Audioengine in den Erfassungs Puffer der Loopback Anwendung, zusätzlich zum Kopieren der Audiodaten in die renderpin der Hardware.

Einige Hardwarehersteller implementieren in ihren audioadaptern Loopback Geräte (im Gegensatz zur PIN-Instanzen auf rendergeräten). Obwohl sich Hardware-Loopback-Geräte im Betrieb des WASAPI-Loopback Modus ähneln, können Sie schwieriger zu verwenden sein.

Hardware-Loopback Geräte haben folgende Nachteile für Audioanwendungen:

-   Nicht alle Audioadapter haben Loopback-Geräte. Daher können Anwendungen, die von ihnen abhängen, nicht auf allen Systemen ausgeführt werden.
-   Bevor eine Anwendung von einem Loopback Gerät aufzeichnen kann, muss der Benutzer das Loopback Gerät identifizieren und für die Verwendung aktivieren.

Verschiedene Lieferanten weisen den Hardware-Loopback Geräten verschiedene Namen zu. Die folgenden Namen sind Beispiele:

-   Stereo Mischung
-   Waveout-Mischung
-   Gemischte Ausgabe
-   Was Sie hören

Der Mangel an standardisierten Namen kann dazu führen, dass Benutzer Schwierigkeiten haben, ein Loopback Gerät in einer Liste von Gerätenamen zu identifizieren.

Ein Hardware Loopback Gerät ist ein Erfassungsgerät. Wenn ein Adapter also ein Loopback Gerät unterstützt, kann eine Audioanwendung vom Gerät auf die gleiche Weise aufzeichnen, wie Sie von einem beliebigen anderen Erfassungsgerät aus erfasst wird.

Wenn Sie z. b. ein Hardware-Loopback Gerät als Standard Erfassungsgerät auswählen, können Sie die Funktion recordaudiostream (ohne Änderung) im Codebeispiel zum erfassen [eines Streams](capturing-a-stream.md) verwenden, um den Datenstrom vom Gerät zu erfassen. (Sie können auch eine Legacy-audioapi verwenden, wie z. b. die Windows Multimedia **waveinxxx** -Funktionen, um den Stream vom Gerät zu erfassen.)

Wenn Ihr Audioadapter ein Hardware Loopback-Gerät enthält, können Sie die Windows-Multimedia-Systemsteuerung (Mmsys.cpl) verwenden, um das Gerät als Standard Erfassungsgerät festzulegen. Die Schritte lauten wie folgt:

1.  Öffnen Sie zum Ausführen Mmsys.cpl ein Eingabe Aufforderungs Fenster, und geben Sie den folgenden Befehl ein:

    ```C++
    control mmsys.cpl,,1
    ```

    

    Alternativ dazu können Sie Mmsys.cpl ausführen, indem Sie mit der rechten Maustaste auf das Redner Symbol im Benachrichtigungsbereich klicken, der sich auf der rechten Seite der Taskleiste befindet, und **Geräte aufzeichnen** auswählen.

2.  Nachdem das Mmsys.cpl Fenster geöffnet wurde, klicken Sie mit der rechten Maustaste auf eine beliebige Stelle in der Liste der Aufzeichnungsgeräte, und vergewissern Sie sich, dass die Option **deaktivierte Geräte** (Andernfalls, wenn das Loopback Gerät deaktiviert ist, wird es nicht in der Liste angezeigt.)
3.  Durchsuchen Sie die Liste der Aufzeichnungsgeräte, um das Loopback Gerät zu finden (sofern vorhanden). Wenn das Loopback Gerät deaktiviert ist, aktivieren Sie es, indem Sie mit der rechten Maustaste auf das Gerät klicken und dann auf **aktivieren** klicken.
4.  Klicken Sie abschließend mit der rechten Maustaste auf das Gerät, und klicken Sie auf **als Standardgerät festlegen**, um das Loopback Gerät als Standard Erfassungsgerät auszuwählen.

WASAPI unterstützt Loopback Aufzeichnung, unabhängig davon, ob die Audiohardware ein Loopback Gerät enthält oder ob der Benutzer das Gerät aktiviert hat.

Windows Vista bietet Digital Rights Management (DRM). Inhaltsanbieter verwenden DRM, um proprietäre Musik oder andere Inhalte vor nicht autorisiertem kopieren und anderen unzulässigen Verwendungen zu schützen. Ebenso lässt ein vertrauenswürdiger Audiotreiber nicht zu, dass ein Loopback Gerät digitale Streams erfasst, die geschützte Inhalte enthalten. Mit Windows Vista können nur vertrauenswürdige Treiber geschützte Inhalte wiedergeben. Weitere Informationen zu vertrauenswürdigen Treibern und DRM finden Sie in der Windows-DDK-Dokumentation.

WASAPI-Loopback enthält die Mischung aus sämtlichen Audiofunktionen, die unabhängig von der Terminal Dienste-Sitzung, von der das Audiomaterial stammt, abgespielt werden. Sie können z. b. einen Loopback Client in einem Dienst ausführen, der in Sitzung 0 ausgeführt wird, und Audiodaten aus allen Benutzersitzungen erfassen, sowie Audiodaten, die in Sitzung 0 abgespielt werden.

Remotedesktop ermöglicht das Umleiten von Audiodaten an den Client. Dies wird durch das Erstellen neuer Audiogeräte implementiert, die nur für diese Sitzung angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenstrom Verwaltung](stream-management.md)
</dt> </dl>

 

 



