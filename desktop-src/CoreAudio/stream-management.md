---
description: Streamverwaltung
ms.assetid: 936d8d69-e86c-418b-b5b0-c4fbbfa1dd49
title: Streamverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669e3be8af4532f9045c08f07400d47c423d507d4e11da4ada0b1a279c52772d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077434"
---
# <a name="stream-management"></a>Streamverwaltung

Nach dem Aufzählen der [Audioendpunktgeräte](audio-endpoint-devices.md) im System und dem Identifizieren eines geeigneten Rendering- oder Erfassungsgeräts besteht die nächste Aufgabe für eine Audioclientanwendung darin, eine Verbindung mit dem Endpunktgerät zu öffnen und den Datenfluss von Audiodaten über diese Verbindung zu verwalten. [WASAPI](wasapi.md) ermöglicht Clients das Erstellen und Verwalten von Audiostreams.

WASAPI implementiert mehrere Schnittstellen, um Datenstromverwaltungsdienste für Audioclients bereitzustellen. Die primäre Schnittstelle ist [**IAudioClient.**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) Ein Client ruft die **IAudioClient-Schnittstelle** für ein Audioendpunktgerät ab, indem er die [**IMMDevice::Activate-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (wobei der Parameter *iid* auf **REFIID** IID \_ IAudioClient festgelegt ist) für das Endpunktobjekt aufruft.

Der Client ruft die Methoden in der [**IAudioClient-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) auf, um Folgendes zu tun:

-   Ermitteln Sie, welche Audioformate das Endpunktgerät unterstützt.
-   Abrufen der Größe des Endpunktpuffers.
-   Abrufen des Streamformats und der Latenz.
-   Starten, Beenden und Zurücksetzen des Streams, der das Endpunktgerät durchläuft.
-   Zugreifen auf zusätzliche Audiodienste.

Zum Erstellen eines Streams ruft ein Client die [**IAudioClient::Initialize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) auf. Mit dieser Methode gibt der Client das Datenformat für den Stream, die Größe des Endpunktpuffers und ob der Stream im freigegebenen oder exklusiven Modus ausgeführt wird.

Die verbleibenden Methoden in der [**IAudioClient-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) lassen sich in zwei Gruppen unterteilen:

-   Methoden, die erst aufgerufen werden können, nachdem der Stream von [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)geöffnet wurde.
-   Methoden, die vor oder nach dem [**Initialize-Aufruf**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) jederzeit aufgerufen werden können.

Die folgenden Methoden können nur nach dem Aufruf von [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)aufgerufen werden:

-   [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)
-   [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)
-   [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
-   [**IAudioClient::GetStreamLatency**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getstreamlatency)
-   [**IAudioClient::Reset**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-reset)
-   [**IAudioClient::Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start)
-   [**IAudioClient::Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop)

Die folgenden Methoden können vor oder nach dem Aufruf von [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) aufgerufen werden:

-   [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)
-   [**IAudioClient::GetMixFormat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)

Um auf die zusätzlichen Audioclientdienste zuzugreifen, ruft der Client die [**IAudioClient::GetService-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) auf. Mit dieser Methode kann der Client Verweise auf die folgenden Schnittstellen abrufen:

-   [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)

    Schreibt Renderingdaten in einen Audiorendering-Endpunktpuffer.

-   [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)

    Liest erfasste Daten aus einem Audioerfassungsendpunktpuffer.

-   [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)

    Kommuniziert mit dem Audiositzungs-Manager, um die Audiositzung zu konfigurieren und zu verwalten, die dem Stream zugeordnet ist.

-   [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)

    Steuert die Lautstärke der Audiositzung, die dem Stream zugeordnet ist.

-   [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)

    Steuert die Lautstärkeebenen der einzelnen Kanäle in der Audiositzung, die dem Stream zugeordnet ist.

-   [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)

    Überwacht die Datenstromrate und die Streamposition.

Darüber hinaus sollten WASAPI-Clients, die eine Benachrichtigung über sitzungsbezogene Ereignisse erfordern, die folgende Schnittstelle implementieren:

-   [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

    Um Ereignisbenachrichtigungen zu empfangen, übergibt der Client einen Zeiger auf seine [**IAudioSessionEvents-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) als Aufrufparameter an die [**IAudioSessionControl::RegisterAudioSessionNotification-Methode.**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification)

Schließlich kann ein Client eine API auf höherer Ebene verwenden, um einen Audiostream zu erstellen, erfordert aber auch Zugriff auf die Sitzungssteuerelemente und Volumesteuerelemente für die Sitzung, die den Stream enthält. Eine API auf höherer Ebene bietet diesen Zugriff in der Regel nicht. Der Client kann die Steuerelemente für eine bestimmte Sitzung über die [**IAudioSessionManager-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) abrufen. Mit dieser Schnittstelle kann der Client die Schnittstellen [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) und [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) für eine Sitzung abrufen, ohne dass der Client die [**IAudioClient-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) verwenden muss, um einen Stream zu erstellen und den Stream der Sitzung zuzuweisen. Ein Client ruft die **IAudioSessionManager-Schnittstelle** für ein Audioendpunktgerät ab, indem er die [**IMMDevice::Activate-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (wobei der Parameter *iid* auf **REFIID** IID \_ IAudioSessionManager festgelegt ist) für das Endpunktobjekt aufruft.

Die Schnittstellen [**IAudioSessionControl,**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)und [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) werden in der Headerdatei Audiopolicy.h definiert. Alle anderen WASAPI-Schnittstellen werden in der Headerdatei Audioclient.h definiert.

In den folgenden Abschnitten wird beschrieben, wie Sie MIT WASAPI Audiostreams verwalten:

-   [Informationen zu WASAPI](wasapi.md)
-   [Rendern eines Streams](rendering-a-stream.md)
-   [Erfassen eines Streams](capturing-a-stream.md)
-   [Loopbackaufzeichnung](loopback-recording.md)
-   [Streams im exklusiven Modus](exclusive-mode-streams.md)
-   [Wiederherstellen nach einem Invalid-Device-Fehler](recovering-from-an-invalid-device-error.md)
-   [Verwenden eines Kommunikationsgeräts](using-the-communication-device.md)
-   [Streamrouting](stream-routing.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 



