---
description: In Windows 7 bietet die Windows-Multimedia-Systemsteuerung Mmsys.cpl eine neue Registerkarte für die Kommunikation.
ms.assetid: bec2127d-fb82-436d-beee-d43e8fef5c35
title: Verwenden eines kommunikationsgeräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f677245e650cf11c71c879b2c26d3183ff4a0b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861291"
---
# <a name="using-a-communication-device"></a>Verwenden eines kommunikationsgeräts

In Windows 7 bietet die Windows-Multimedia-Systemsteuerung Mmsys.cpl eine neue Registerkarte für die **Kommunikation** . Diese Registerkarte enthält Optionen, mit denen Benutzeroptionen festlegen können, die definieren, wie das System ein *Kommunikationsgerät* verwaltet. Ein Kommunikationsgerät wird hauptsächlich zum platzieren oder empfangen von Telefon anrufen auf dem Computer verwendet. Bei einem Computer, der nur über ein renderinggerät (Sprecher) und ein Erfassungsgerät (Mikrofon) verfügt, fungieren diese Audiogeräte auch als Standard Kommunikationsgeräte. Wenn ein Benutzer ein neues Gerät (z. b. ein USB-Headset) verbindet, führt das System eine automatische Geräte Rollen Erkennung durch, indem er die vom OEM aufgefüllten Konfigurationseinstellungen prüft. Wenn das System festlegt, dass ein Gerät für die Kommunikation am besten geeignet ist, weist das System dem Gerät die **eCommunications** -Rolle zu. Für diese Geräte bietet das Windows 7-Mmsys.cpl die Option **Standard Kommunikationsgerät** , mit dem Benutzer ein Kommunikationsgerät für audiorendering (**Wiedergabe** Registerkarte) und Audioerfassung **(Register** Karte) auswählen können. Das System führt die automatische Rollen Erkennung aus, legt jedoch kein bestimmtes Gerät für die Kommunikation fest. Dies muss vom Benutzer vorgenommen werden. Mit der neuen **eCommunications** -Rolle kann eine Anwendung zwischen einem Gerät, das vom Benutzer für die Verarbeitung von Telefon anrufen ausgewählt wird, und einem Gerät unterscheiden, das als multimediategerät (Musikwiedergabe) verwendet werden soll. Wenn der Benutzer z. b. über ein Headset und einen Redner verfügt, der mit dem Computer verbunden ist, weist das System die Rolle " **econsole** " dem Redner und der **eCommunications** -Rolle dem Headset zu. Nachdem der Benutzer das als Kommunikationsgerät zu verwendende Headset ausgewählt hat, können Sie zum Entwickeln einer Kommunikationsanwendung speziell auf das Headset abzielen, um einen Audiostream zu rendern. Eine Anwendung, mit der der Benutzer die vom System zugewiesene Geräte Rolle nicht ändern kann. Weitere Informationen zu Geräte Rollen finden Sie unter [Geräte Rollen](device-roles.md).

Kommunikationsanwendungen, wie z. b. VoIP-und Unified Communication-Anwendungen, platzieren und empfangen Telefonanrufe über einen Computer. Beispielsweise kann eine VoIP-Anwendung einen Stream, der die Benachrichtigung über den Ring enthält, an den Endpunkt eines kommunikationsgeräts zuweisen, das zum Rendern von Audiodatenströmen festgelegt ist. Außerdem öffnet die Anwendung möglicherweise die Spracheingabe-und-Ausgabedaten Ströme auf den Geräten zum Erfassen und Rendern von Endpunkten, die als Kommunikationsgeräte festgelegt sind.

Wenn Sie Kommunikationsfunktionen in Ihre Anwendungen integrieren möchten, können Sie Folgendes verwenden:

-   [Mmdevice-API](mmdevice-api.md)–, um einen Verweis auf den Endpunkt des kommunikationsgeräts zu erhalten.
-   [WASAPI](wasapi.md)– zum Rendering und Erfassen von Audiodatenströmen über das Kommunikationsgerät. Das Betriebssystem betrachtet den in einem Kommunikationsgerät geöffneten Stream als einen *Kommunikationsstream*.

Die Kommunikationsanwendung listet Geräte auf und stellt die streamverwaltung für einen Kommunikationsstream (Rendering-oder Aufzeichnungsdaten Strom) auf die gleiche Weise bereit wie einen nicht-Kommunikationsstream mithilfe der Kerndatei-APIs.

Eine der Features, die Sie in Ihre Kommunikationsanwendung integrieren können, ist das *ducken* oder die Daten *Strom Dämpfung*. Dieses Verhalten definiert, was mit anderen Sounds geschehen muss, wenn ein Kommunikationsstream geöffnet wird, z. b. Wenn ein Telefonanruf auf dem Kommunikationsgerät empfangen wird. Abhängig von der Auswahl des Benutzers kann das System das audiovolume des nicht-Kommunikationsstreams entweder stumm oder niedriger sein. Das Audiosystem generiert Ducking-Ereignisse, wenn ein Kommunikationsstream zum Rendern oder Erfassen von Streams geöffnet oder geschlossen wird. Standardmäßig bietet das Betriebssystem ein Standardmäßiges Ducking. Eine Medien Anwendung kann das Standardverhalten ersetzen und diese Ereignisse selbst behandeln, um eine angepasste Ducking-Darstellung bereitzustellen.

In den folgenden Abschnitten wird beschrieben, wie Sie mit den Kerncode-APIs eine benutzerdefinierte Ducking-Funktion bereitstellen.

-   [Standardmäßiges ducken](stream-attenuation.md)
-   [Deaktivieren der Standardeinstellung für das ducken](disabling-the-ducking-experience.md)
-   [Bereitstellen eines benutzerdefinierten Ducking-Verhaltens](providing-a-custom-ducking-experience.md)
-   [Implementierungs Überlegungen für Ducking-Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md)
-   [Erhalten von Ducking-Ereignissen](getting-ducking-events-from-a-communication-device.md)

### <a name="getting-a-reference-to-the-communication-device-endpoint"></a>Beziehen eines Verweises auf den Kommunikationsgeräte Endpunkt

Um das Kommunikationsgerät verwenden zu können, muss ein direkter WASAPI-Client die Geräte mit dem Geräte Enumerator auflisten. Rufen Sie einen Verweis auf den Endpunkt des Standard kommunikationsgeräts ab, indem Sie [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)aufrufen. In diesem-Befehl muss die Anwendung **eCommunications** im *Role* -Parameter angeben, um die Geräte Enumeration auf Kommunikationsgeräte zu beschränken. Nachdem Sie einen Verweis auf den Geräte Endpunkt für das Gerät erhalten haben, können Sie die Dienste, für die der Endpunkt festgelegt ist, durch Aufrufen von " [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)" aktivieren. Beispielsweise können Sie die **IID \_ iaudioclient** -Dienst-ID übergeben, um ein audioclientobjekt zu aktivieren und für die streamverwaltung zu verwenden, den **IID \_ iaudioendpointvolume** -Bezeichner, um Zugriff auf die volumesteuerelemente des Kommunikationsgeräte Endpunkts zu erhalten, oder den **IID \_ iaudiosessionmanager** -Bezeichner, um den Sitzungs-Manager zu aktivieren Informationen zu Streamvorgängen finden Sie unter [Stream Management](stream-management.md).

Mithilfe der [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Referenz können Sie auch auf den Eigenschaften Speicher für den Geräte Endpunkt zugreifen. Diese Eigenschaftswerte (z. b. Anzeige Name und Herstellername) werden vom OEM aufgefüllt und ermöglichen es einer Anwendung, die Merkmale eines kommunikationsgeräts zu bestimmen. Weitere Informationen finden Sie unter [Geräteeigenschaften](device-properties.md).

Der folgende Beispielcode ruft einen Verweis auf den Endpunkt des Standard kommunikationsgeräts zum Rendern eines Audiostreams ab.


```C++
IMMDevice *defaultDevice = NULL;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), NULL,
            CLSCTX_INPROC_SERVER, 
            __uuidof(IMMDeviceEnumerator), 
            (LPVOID *)&deviceEnumerator);

hr = deviceEnumerator->GetDefaultAudioEndpoint(eRender, 
            eCommunications, &defaultDevice);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenstrom Verwaltung](stream-management.md)
</dt> </dl>

 

 



