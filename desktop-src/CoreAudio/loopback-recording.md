---
description: Loopbackaufzeichnung
ms.assetid: 71c567f7-fffa-4b75-897a-63ed30c4c9b0
title: Loopbackaufzeichnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa5ffe48bf11ad57b02085ab00dfd1ca09be0f72a56935cbd8d1bb40543033f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118005273"
---
# <a name="loopback-recording"></a>Loopbackaufzeichnung

Im Loopbackmodus kann ein Client von WASAPI den Audiostream erfassen, der von einem Renderingendpunktgerät wiedergegeben wird. Um einen Stream im Loopbackmodus zu öffnen, muss der Client:

-   Rufen Sie eine [**IMMDevice-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) für das Renderingendpunktgerät ab.
-   Initialisieren Sie einen Erfassungsstream im Loopbackmodus auf dem Renderingendpunktgerät.

Nach dem Ausführen dieser Schritte kann der Client die [**IAudioClient::GetService-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) aufrufen, um eine [**IAudioCaptureClient-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) auf dem Renderingendpunktgerät abzurufen.

WASAPI stellt den Loopbackmodus in erster Linie zur Unterstützung des Akustik-Echoabbruchs (Acoustic Echo Cancellation, AEC) bereit. Für andere Arten von Audioanwendungen kann der Loopbackmodus jedoch nützlich sein, um die Systemmischung zu erfassen, die von der Audio-Engine wiedergegeben wird.

Im Codebeispiel unter [Erfassen eines Streams](capturing-a-stream.md)kann die RecordAudioStream-Funktion leicht geändert werden, um einen Loopbackmodus-Erfassungsdatenstrom zu konfigurieren. Die erforderlichen Änderungen sind:

-   Ändern Sie im Aufruf der [**IMMDeviceEnumerator::GetDefaultAudioEndpoint-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) den ersten Parameter (*dataFlow*) von eCapture in eRender.
-   Ändern Sie im Aufruf der [**IAudioClient::Initialize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) den Wert des zweiten Parameters (*StreamFlags*) von 0 in AUDCLNT \_ STREAMFLAGS \_ LOOPBACK.

In Versionen von Windows vor Windows 10 1703 empfängt der Erfassungsclient im Pullmodus keine Ereignisse, wenn ein Stream mit ereignisgesteuerter Pufferung initialisiert und loopbackfähig ist. Um dies zu umgehen, initialisieren Sie einen Renderstream im ereignisgesteuerten Modus. Jedes Mal, wenn der Client ein Ereignis für den Renderstream empfängt, muss er dem Erfassungsclient signalisieren, dass der Erfassungsthread ausgeführt wird, der die nächsten Stichproben aus dem Erfassungsendpunktpuffer liest. In Windows 10 Versionen 1703 und höher werden ereignisgesteuerte Loopbackclients unterstützt, und die Problemumgehung im Zusammenhang mit dem Renderstream ist nicht mehr erforderlich.  

Ein Client kann den Loopbackmodus nur für einen Stream im freigegebenen Modus (AUDCLNT \_ SHAREMODE \_ SHARED) aktivieren. Streams im exklusiven Modus können nicht im Loopbackmodus ausgeführt werden.

Die Implementierung des Loopbacks durch WASAPI hängt von den Funktionen der Hardware ab. Wenn die Hardware einen Loopbackanschluss am Renderendpunkt unterstützt, verwendet WASAPI die auf diesem Pin bereitgestellten Audiodaten für den Loopbackstream. Wenn die Hardware keinen Loopbackpin unterstützt, kopiert WASAPI den Ausgabestream von der Audio-Engine in den Erfassungspuffer der Loopbackanwendung und kopiert die Audiodaten auf den Renderpin der Hardware.

Einige Hardwareanbieter implementieren Loopbackgeräte (im Gegensatz zu Pin-Instanzen auf Rendergeräten) in ihren Audioadaptern. Obwohl Hardware-Loopbackgeräte im Betrieb mit dem WASAPI-Loopbackmodus vergleichbar sind, können sie schwieriger zu verwenden sein.

Hardware-Loopbackgeräte haben die folgenden Nachteile für Audioanwendungen:

-   Nicht alle Audioadapter verfügen über Loopbackgeräte. Daher funktionieren Anwendungen, die von ihnen abhängen, nicht auf allen Systemen.
-   Bevor eine Anwendung von einem Loopbackgerät aufzeichnen kann, muss der Benutzer das Loopbackgerät identifizieren und für die Verwendung aktivieren.

Verschiedene Anbieter weisen ihren Hardware-Loopbackgeräten unterschiedliche Namen zu. Die folgenden Namen sind Beispiele:

-   Stereomischung
-   Waveoutmischung
-   Gemischte Ausgabe
-   Was Sie hören

Das Fehlen standardisierter Namen kann dazu führen, dass Benutzer Schwierigkeiten haben, ein Loopbackgerät in einer Liste von Gerätenamen zu identifizieren.

Ein Hardware-Loopbackgerät ist ein Erfassungsgerät. Wenn ein Adapter also ein Loopbackgerät unterstützt, kann eine Audioanwendung vom Gerät auf die gleiche Weise aufzeichnen wie von jedem anderen Erfassungsgerät.

Wenn Sie beispielsweise ein Hardware-Loopbackgerät als Standarderfassungsgerät auswählen, können Sie die RecordAudioStream-Funktion (ohne Änderung) im Codebeispiel unter [Erfassen eines Streams](capturing-a-stream.md) verwenden, um den Datenstrom vom Gerät zu erfassen. (Sie können auch eine Legacy-Audio-API wie die Windows **Multimediafunktionen waveInXxx** verwenden, um den Datenstrom vom Gerät zu erfassen.)

Wenn Ihr Audioadapter ein Hardware-Loopbackgerät enthält, können Sie die Windows Multimediasteuerung Mmsys.cpl verwenden, um das Gerät als Standarderfassungsgerät festzulegen. Die Schritte lauten wie folgt:

1.  Um Mmsys.cpl auszuführen, öffnen Sie ein Eingabeaufforderungsfenster, und geben Sie den folgenden Befehl ein:

    ```C++
    control mmsys.cpl,,1
    ```

    

    Alternativ können Sie Mmsys.cpl ausführen, indem Sie mit der rechten Maustaste auf das Lautsprechersymbol im Infobereich rechts auf der Taskleiste klicken und **Recording Devices (Aufzeichnungsgeräte)** auswählen.

2.  Nachdem das fenster Mmsys.cpl geöffnet wurde, klicken Sie mit der rechten Maustaste auf eine beliebige Stelle in der Liste der Aufzeichnungsgeräte, und überprüfen Sie, ob die Option **Deaktivierte Geräte anzeigen** aktiviert ist. (Andernfalls wird das Loopbackgerät nicht in der Liste angezeigt,wenn es deaktiviert ist.)
3.  Durchsuchen Sie die Liste der Aufzeichnungsgeräte, um das Loopbackgerät zu suchen (sofern vorhanden). Wenn das Loopbackgerät deaktiviert ist, aktivieren Sie es, indem Sie mit der rechten Maustaste auf das Gerät klicken und auf **Aktivieren** klicken.
4.  Klicken Sie abschließend mit der rechten Maustaste auf das Gerät, und klicken Sie auf **Als Standardgerät festlegen,** um das Loopbackgerät als Standarderfassungsgerät auszuwählen.

WASAPI unterstützt die Loopbackaufzeichnung, unabhängig davon, ob die Audiohardware ein Loopbackgerät enthält oder ob der Benutzer das Gerät aktiviert hat.

Windows Vista bietet DRM (Digital Rights Management). Inhaltsanbieter verlassen sich auf DRM, um ihre proprietäre Musik oder andere Inhalte vor nicht autorisiertem Kopieren und anderen unzulässigen Verwendungen zu schützen. Ebenso lässt ein vertrauenswürdiger Audiotreiber nicht zu, dass ein Loopbackgerät digitale Datenströme erfasst, die geschützte Inhalte enthalten. Windows Vista ermöglicht es nur vertrauenswürdigen Treibern, geschützte Inhalte wiederzuspielen. Weitere Informationen zu vertrauenswürdigen Treibern und DRM finden Sie in der Windows DDK-Dokumentation.

WASAPI-Loopback enthält die Mischung aller wiedergegebenen Audiodaten, unabhängig von der Terminal services-Sitzung, aus der die Audiodaten stammen. Beispielsweise können Sie einen Loopbackclient in einem Dienst ausführen, der in Sitzung 0 ausgeführt wird, und Audiodaten aus allen Benutzersitzungen sowie Audiodaten erfassen, die von Sitzung 0 wiedergegeben werden.

Remotedesktop ermöglicht das Umleiten von Audiodaten an den Client. Dies wird implementiert, indem neue Audiogeräte erstellt werden, die nur für diese Sitzung angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streamverwaltung](stream-management.md)
</dt> </dl>

 

 



