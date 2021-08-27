---
description: Informationen zu WASAPI
ms.assetid: 452b9725-b0b9-4888-bbb5-a23e0067e840
title: Informationen zu WASAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3effb34ec0cde0a53d0eb6f6e9718aa13fc308417b33427f168364afc32086ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088180"
---
# <a name="about-wasapi"></a>Informationen zu WASAPI

Mit Windows AUDIO Session API (WASAPI) können Clientanwendungen den Fluss von Audiodaten zwischen der Anwendung und einem [Audioendpunktgerät verwalten.](audio-endpoint-devices.md)

Die HEADERdateien Audioclient.h und Audiopolicy.h definieren die WASAPI-Schnittstellen.

Jeder Audiostream ist Ein Mitglied einer [Audiositzung.](audio-sessions.md) Durch die Sitzungsabstraktion kann ein WASAPI-Client einen Audiostream als Mitglied einer Gruppe verwandter Audiostreams identifizieren. Das System kann alle Streams in der Sitzung als einzelne Einheit verwalten.

Die Audio-Engine ist die [Audiokomponente im Benutzermodus,](user-mode-audio-components.md) über die Anwendungen den Zugriff auf ein Audioendpunktgerät gemeinsam nutzen. Die Audio-Engine transportiert Audiodaten zwischen einem Endpunktpuffer und einem Endpunktgerät. Um einen Audiodatenstrom über ein Renderingendpunktgerät wieder geben zu können, schreibt eine Anwendung in regelmäßigen Abständen Audiodaten in einen Renderingendpunktpuffer. Die Audio-Engine mischen die Datenströme aus den verschiedenen Anwendungen. Um einen Audiodatenstrom von einem Aufzeichnungsendpunktgerät aufzeichnen zu können, liest eine Anwendung regelmäßig Audiodaten aus einem Aufzeichnungsendpunktpuffer.

WASAPI besteht aus mehreren Schnittstellen. Die erste davon ist die [**IAudioClient-Schnittstelle.**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) Für den Zugriff auf die WASAPI-Schnittstellen ruft ein Client zunächst einen Verweis auf die **IAudioClient-Schnittstelle** eines Audioendpunktgeräts ab, indem er die [**IMMDevice::Activate-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) aufruft, deren *Parameter iid* auf **REFIID** IID \_ IAudioClient festgelegt ist. Der Client ruft die [**IAudioClient::Initialize-Methode auf,**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) um einen Stream auf einem Endpunktgerät zu initialisieren. Nach der Initialisierung eines Streams kann der Client Verweise auf die anderen WASAPI-Schnittstellen abrufen, indem er die [**IAudioClient::GetService-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) aufruft.

Viele der Methoden in WASAPI geben den Fehlercode AUDCLNT E DEVICE INVALIDATED zurück, wenn das Audioendpunktgerät, das von einer Clientanwendung \_ \_ verwendet \_ wird, ungültig wird. Häufig kann die Anwendung nach diesem Fehler wiederhergestellt werden. Weitere Informationen finden Sie unter [Recovering from an Invalid-Device Error](recovering-from-an-invalid-device-error.md).

WASAPI implementiert die folgenden Schnittstellen.



| Schnittstelle                                            | BESCHREIBUNG                                                                                                                                                     |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)   | Ermöglicht einem Client das Lesen von Eingabedaten aus einem Erfassungsendpunktpuffer.                                                                                             |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                 | Ermöglicht einem Client das Erstellen und Initialisieren eines Audiostreams zwischen einer Audioanwendung und der Audio-Engine oder dem Hardwarepuffer eines Audioendpunktgeräts. |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                   | Ermöglicht es einem Client, die Datenrate eines Streams und die aktuelle Position im Stream zu überwachen.                                                                        |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)     | Ermöglicht einem Client das Schreiben von Ausgabedaten in einen Renderingendpunktpuffer.                                                                                           |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) | Ermöglicht einem Client, die Steuerungsparameter für eine Audiositzung zu konfigurieren und Ereignisse in der Sitzung zu überwachen.                                                 |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) | Ermöglicht einem Client den Zugriff auf die Sitzungssteuerelemente und Volumesteuerelemente für prozessübergreifende und prozessspezifische Audiositzungen.                                 |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)     | Ermöglicht es einem Client, die Lautstärkeebenen für alle Kanäle in einem Audiostream zu steuern und zu überwachen.                                                           |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)   | Ermöglicht es einem Client, die Lautstärkeebenen für alle Kanäle in der Audiositzung zu steuern, zu der der Stream gehört.                                          |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)     | Ermöglicht es einem Client, die Master-Volumeebene einer Audiositzung zu steuern.                                                                                        |



 

WASAPI-Clients, die eine Benachrichtigung über sitzungsbezogene Ereignisse erfordern, sollten die folgende Schnittstelle implementieren.



| Schnittstelle                                          | BESCHREIBUNG                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) | Stellt Benachrichtigungen zu sitzungsbezogenen Ereignissen wie Änderungen auf Volumeebene, Anzeigename und Sitzungszustand zur Verfügung. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streamverwaltung](stream-management.md)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 



