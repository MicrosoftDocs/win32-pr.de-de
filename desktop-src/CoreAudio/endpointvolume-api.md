---
description: EndpointVolume-API
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: EndpointVolume-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22965e882a2f7d413ae58690fc9bc5f8134aba0e7b26838ca38c74d7f0093c98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018448"
---
# <a name="endpointvolume-api"></a>EndpointVolume-API

Mit der EndpointVolume-API können spezialisierte Clients die Lautstärkeebenen von [Audioendpunktgeräten steuern und überwachen.](audio-endpoint-devices.md) Ein Client ruft Verweise auf die Schnittstellen in der EndpointVolume-API ab, indem er die [**IMMDevice-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) eines Audioendpunktgeräts erhält und die [**IMMDevice::Activate-Methode aufruft.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)

Die Headerdatei Endpointvolume.h definiert die Schnittstellen in der EndpointVolume-API.

Audioanwendungen, die die [MMDevice-API](mmdevice-api.md) und [WASAPI](wasapi.md) verwenden, verwenden in der Regel die [**ISimpleAudioVolume-Schnittstelle,**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) um die Lautstärkeebenen pro Sitzung zu steuern. Nur zwei Arten von Audioanwendungen erfordern die Verwendung der EndpointVolume-API. Diese Anwendungstypen sind:

-   Anwendungen, die die Master-Volumeebenen von Audioendpunktgeräten verwalten, ähnlich wie Windows Volumesteuerungsprogramm, Sndvol.exe.
-   Professional Audioanwendungen ("Pro Audio"), die exklusiven Moduszugriff auf Audioendpunktgeräte erfordern.

Eine ungeeignete Verwendung der EndpointVolume-API kann Windows Audiorichtlinie beeinträchtigen und die Systemvolumeeinstellungen des Benutzers beeinträchtigen.

Wenn ein Audioendpunktgerät Hardwarevolume- und Stummschaltungssteuerelemente implementiert, verwendet die EndpointVolume-API diese Steuerelemente, um das Gerätevolume zu verwalten. Andernfalls implementiert die EndpointVolume-API die Steuerelemente in der Software transparent für den Client.

Wenn ein Gerät über Steuerelemente für Hardwarevolume und Stummschaltung verfügt, wirken sich Änderungen am Gerätevolume und stummgeschalteten Einstellungen über die EndpointVolume-API sowohl im modus shared als auch im exklusiven Modus auf die Volumeebene aus. Wenn ein Gerät kein Hardwarevolume und stummgeschaltete Steuerelemente hat, wirken sich Änderungen am Softwarevolume und stummgeschalteten Steuerelementen über die EndpointVolume-API im modus shared, aber nicht im exklusiven Modus auf die Volumeebene aus. Im exklusiven Modus tauschen Client und Gerät Audiodaten direkt aus und umgehen dabei die Softwaresteuerelemente.

Für Anwendungen, die Hardwarevolume und Stummschaltungssteuerelemente verwalten müssen, bietet die EndpointVolume-API zwei potenzielle Vorteile gegenüber der [DeviceTopology-API.](devicetopology-api.md)

Erstens fehlt bei einer Reihe von Audioadaptergeräten die Steuerung des Hardwarevolumens. Wenn auf einem Gerät kein Hardwarevolume-Steuerelement verfügbar ist, implementiert die [**IAudioEndpointVolume-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) in der EndpointVolume-API automatisch ein Softwarevolume-Steuerelement für den Datenstrom auf das bzw. von diesem Gerät. Für einen Client der EndpointVolume-API ist das Ergebnis dasselbe, unabhängig davon, ob die Volumesteuerung auf Hardware vom Gerät oder von der EndpointVolume-API-Schnittstelle in Software implementiert wird.

Zweitens kann eine Anwendung, die die DeviceTopology-API zum Implementieren eines Topologiedurchlaufalgorithmus verwendet, das gesuchte Steuerelement möglicherweise nicht finden, selbst wenn das Adaptergerät Hardware-Volumesteuerelemente implementiert. In der Regel ist eine solche Anwendung so konzipiert, dass sie die Hardwaretopologie eines bestimmten Geräts oder einer Gruppe verwandter Geräte durchläuft. Die Anwendung riskiert einen Fehler, wenn sie versucht, die Topologie eines Geräts zu durchlaufen, für das sie nicht speziell entwickelt oder getestet wurde.

Nur spezielle Anwendungen, die auf andere Hardwarefunktionen als Volume- und Stummschaltungssteuerelemente zugreifen müssen, erfordern die Verwendung der DeviceTopology-API. Für Anwendungen, die nur die Steuerung der Volumeebene eines Streams im exklusiven Modus erfordern, ist die EndpointVolume-API einfacher zu verwenden und funktioniert zuverlässig mit einer größeren Bandbreite von Audiohardwaregeräten.

Codebeispiele, die die Schnittstellen in der EndpointVolume-API verwenden, finden Sie in den folgenden Themen:

-   [Steuerelemente für Endpunktvolumen](endpoint-volume-controls.md)
-   [Spitzenzähler](peak-meters.md)

Ein Beispiel, in dem die EndpointVolume-API verwendet wird, finden Sie unter [EndpointVolume](endpointvolume.md) im Windows SDK.

Die EndpointVolume-API implementiert die folgenden Schnittstellen.



| Schnittstelle                                                | BESCHREIBUNG                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | Stellt die Volumesteuerelemente für den Audiodatenstrom zu oder von einem Audioendpunktgerät dar. |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | Stellt eine Spitzenmessung für den Audiodatenstrom zu oder von einem Audioendpunktgerät dar.        |



 

Darüber hinaus sollten Clients der EndpointVolume-API, die eine Benachrichtigung über Lautstärke und mutierende Änderungen auf Audioendpunktgeräten erfordern, die folgende Schnittstelle implementieren.



| Schnittstelle                                                            | BESCHREIBUNG                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Stellt Benachrichtigungen zur Auswahl, wenn sich die Lautstärke oder der Veränderungszustand eines Audioendpunktgeräts ändert. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lautstärkeregler](volume-controls.md)
</dt> <dt>

[**IMMDevice-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 



