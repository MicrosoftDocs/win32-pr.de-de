---
description: Informationen zu WASAPI
ms.assetid: 452b9725-b0b9-4888-bbb5-a23e0067e840
title: Informationen zu WASAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f869319f3100b797e58c7b43597869c9767ac037
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958422"
---
# <a name="about-wasapi"></a>Informationen zu WASAPI

Mithilfe der Windows-audiositzungs-API (WASAPI) können Client Anwendungen den Fluss von Audiodaten zwischen der Anwendung und einem [audioendpunkt-Gerät](audio-endpoint-devices.md)verwalten.

Header Dateien AudioClient. h und audiopolicy. h definieren die WASAPI-Schnittstellen.

Jeder Audiostream ist ein Member einer [Audiositzung](audio-sessions.md). Mithilfe der Sitzungs Abstraktion kann ein WASAPI-Client einen Audiostream als Member einer Gruppe verwandter Audiostreams identifizieren. Das System kann alle Streams in der Sitzung als eine Einheit verwalten.

Die Audioengine ist die [Audiokomponente im Benutzermodus](user-mode-audio-components.md) , über die Anwendungen den Zugriff auf ein audioendpunktgerät freigeben. Die Audioengine transportiert Audiodaten zwischen einem Endpunkt Puffer und einem Endpunkt Gerät. Um einen Audiostream über ein renderingendpunktgerät wiederzugeben, schreibt eine Anwendung regelmäßig Audiodaten in einen renderingendpunktpuffer. Die Audioengine mischt die Streams aus den verschiedenen Anwendungen. Um einen Audiostream von einem Aufzeichnungs Endpunkt-Gerät aufzuzeichnen, liest eine Anwendung regelmäßig Audiodaten aus einem Erfassungs Endpunkt Puffer.

WASAPI besteht aus mehreren Schnittstellen. Der erste ist die [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Schnittstelle. Für den Zugriff auf die WASAPI-Schnittstellen Ruft ein Client zuerst einen Verweis auf die **iaudioclient** -Schnittstelle eines audioendpunktgeräts ab, indem er die Methode " [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) " mit dem Parameter " *IID* " auf **REFIID** IID \_ iaudioclient ansetzt. Der Client ruft die [**iaudioclient:: Initialisieren**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode auf, um einen Stream auf einem Endpunkt Gerät zu initialisieren. Nachdem ein Stream initialisiert wurde, kann der Client Verweise auf die anderen WASAPI-Schnittstellen abrufen, indem er die [**iaudioclient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) -Methode aufrufen.

Viele der Methoden in der WASAPI geben Fehlercode "audclnt \_ E \_ Device" ungültig aus \_ , wenn das audioendpunktgerät, das von einer Client Anwendung verwendet wird, ungültig wird. Häufig kann die Anwendung nach diesem Fehler wieder hergestellt werden. Weitere Informationen finden Sie unter wieder [herstellen nach einem Invalid-Device Fehler](recovering-from-an-invalid-device-error.md).

WASAPI implementiert die folgenden Schnittstellen.



| Schnittstelle                                            | BESCHREIBUNG                                                                                                                                                     |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iaudiocaptureclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)   | Ermöglicht einem Client das Lesen von Eingabedaten aus einem Erfassungs Endpunkt Puffer.                                                                                             |
| [**Iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                 | Ermöglicht es einem Client, einen Audiostream zwischen einer Audioanwendung und der Audioengine oder dem Hardware Puffer eines audioendpunktgeräts zu erstellen und zu initialisieren. |
| [**Iaudioclock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                   | Ermöglicht einem Client, die Datenrate eines Streams und die aktuelle Position im Stream zu überwachen.                                                                        |
| [**Iaudiorenderclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)     | Ermöglicht einem Client das Schreiben von Ausgabedaten in einen Rendering-Endpunkt Puffer.                                                                                           |
| [**Iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) | Ermöglicht einem Client, die Steuerelement Parameter für eine Audiositzung zu konfigurieren und Ereignisse in der Sitzung zu überwachen.                                                 |
| [**Iaudiosessionmanager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) | Ermöglicht einem Client den Zugriff auf die Sitzungs Steuerelemente und volumesteuerelemente für prozessübergreifende und prozessspezifische audiositzungen.                                 |
| [**Iaudiostreamvolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)     | Ermöglicht einem Client, die volumeebenen für alle Kanäle in einem Audiostream zu steuern und zu überwachen.                                                           |
| [**Ichannelaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)   | Ermöglicht einem Client das Steuern der volumeebenen für alle Kanäle in der Audiositzung, zu der der Stream gehört.                                          |
| [**Isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)     | Ermöglicht einem Client, die Master Volume-Ebene einer Audiositzung zu steuern.                                                                                        |



 

Bei WASAPI-Clients, die Benachrichtigungen zu Sitzungs bezogenen Ereignissen erfordern, sollte die folgende Schnittstelle implementiert werden.



| Schnittstelle                                          | BESCHREIBUNG                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**Iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) | Bietet Benachrichtigungen zu Sitzungs bezogenen Ereignissen, wie z. b. Änderungen der Volumeebene, des anzeigen Amens und des Sitzungs Zustands. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenstrom Verwaltung](stream-management.md)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 



