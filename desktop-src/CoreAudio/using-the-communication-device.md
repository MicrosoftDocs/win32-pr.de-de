---
description: In Windows 7 bietet die Windows Multimedia-Systemsteuerung Mmsys.cpl eine neue Registerkarte Kommunikation.
ms.assetid: bec2127d-fb82-436d-beee-d43e8fef5c35
title: Verwenden eines Kommunikationsgeräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25dccba320e7b7adbe7804b1cd98bea72e0f1f0de5904ee6b41df08934940ff3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834075"
---
# <a name="using-a-communication-device"></a>Verwenden eines Kommunikationsgeräts

In Windows 7 bietet die Windows Multimedia-Systemsteuerung Mmsys.cpl eine neue Registerkarte **Kommunikation.** Diese Registerkarte enthält Optionen, mit denen ein Benutzer Optionen festlegen kann, die definieren, wie das System ein *Kommunikationsgerät* verwaltet. Ein Kommunikationsgerät wird hauptsächlich zum Tätigen oder Empfangen von Telefonanrufen auf dem Computer verwendet. Für einen Computer, der nur über ein Renderinggerät (Lautsprecher) und ein Erfassungsgerät (Mikrofon) verfügt, fungieren diese Audiogeräte auch als Standardkommunikationsgeräte. Wenn ein Benutzer ein neues Gerät , z. B. ein USB-Headset, verbindet, führt das System eine automatische Geräterollenerkennung durch, indem es die Konfigurationseinstellungen nachverweiset, die vom OEM aufgefüllt werden. Wenn das System bestimmt, dass ein Gerät für Kommunikationszwecke am besten geeignet ist, weist das System dem Gerät die **eCommunications-Rolle** zu. Für diese Geräte bietet der Windows 7 Mmsys.cpl die Option **Standardkommunikationsgerät,** mit der ein Benutzer ein Kommunikationsgerät für das Audiorendering (Registerkarte **Wiedergabe)** und die Audioaufzeichnung (Registerkarte **Aufzeichnung)** auswählen kann. Das System führt die automatische Rollenerkennung durch, legt aber kein bestimmtes Gerät für die Kommunikation fest. Dies muss vom Benutzer erfolgen. Mit der neuen **eCommunications-Rolle** kann eine Anwendung zwischen einem Gerät, das vom Benutzer für die Verarbeitung von Telefonanrufen ausgewählt wird, und einem Gerät unterscheiden, das als Multimediagerät verwendet werden soll (Musikwiedergabe). Wenn der Benutzer beispielsweise über ein Headset und einen Lautsprecher verfügt, der mit dem Computer verbunden ist, weist das System dem Lautsprecher die **eConsole-Rolle** und dem Headset die **eCommunications-Rolle** zu. Nachdem der Benutzer das Headset ausgewählt hat, das als Kommunikationsgerät verwendet werden soll, können Sie zum Entwickeln einer Kommunikationsanwendung das Headset speziell zum Rendern eines Audiodatenstroms verwenden. Eine Anwendung, die der Benutzer nicht ändern kann, die vom System zugewiesene Geräterolle. Weitere Informationen zu Geräterollen finden Sie unter [Geräterollen.](device-roles.md)

Kommunikationsanwendungen, z. B. VoIP- und Unified Communication-Anwendungen, platzieren und empfangen Telefonanrufe über einen Computer. Beispielsweise kann eine VoIP-Anwendung dem Endpunkt eines Kommunikationsgeräts, das audiostreams rendern soll, einen Stream zuweisen, der die Ringbenachrichtigung enthält. Darüber hinaus kann die Anwendung die Spracheingabe- und Ausgabedatenströme auf den Erfassungs- und Renderingendpunktgeräten öffnen, die als Kommunikationsgeräte festgelegt sind.

Um Kommunikationsfunktionen in Ihre Anwendungen zu integrieren, können Sie:

-   [MMDevice-API](mmdevice-api.md): Abrufen eines Verweises auf den Endpunkt des Kommunikationsgeräts.
-   [WASAPI](wasapi.md): Zum Rendern und Erfassen von Audiostreams über das Kommunikationsgerät. Das Betriebssystem betrachtet den auf einem Kommunikationsgerät geöffneten Stream als *Kommunikationsdatenstrom.*

Die Kommunikationsanwendung listet Geräte auf und stellt die Streamverwaltung für einen Kommunikationsdatenstrom (Rendering oder Erfassung) auf die gleiche Weise bereit wie die Verwaltung eines Nichtkommunikationsdatenstroms mithilfe der Core Audio-APIs.

Eines der Features, die Sie in Ihre Kommunikationsanwendung integrieren können, ist *die Entschlangen-* oder *Stream-Dämpfung.* Dieses Verhalten definiert, was mit anderen Sounds geschehen muss, wenn ein Kommunikationsstream geöffnet wird, z. B. wenn ein Telefonanruf auf dem Kommunikationsgerät empfangen wird. Je nach Wahl des Benutzers kann das System die Audiolautstärke des Nichtkommunikationsstreams stummschalten oder verringern. Das Audiosystem generiert Entzungsereignisse, wenn ein Kommunikationsstream zum Rendern oder Erfassen von Datenströmen geöffnet oder geschlossen wird. Standardmäßig bietet das Betriebssystem eine Standardmäßige Benutzeroberfläche. Eine Medienanwendung kann das Standardverhalten ersetzen und diese Ereignisse selbst behandeln, um eine angepasste Benutzeroberfläche bereitzustellen.

In den folgenden Abschnitten wird beschrieben, wie Sie Core Audio-APIs verwenden, um eine benutzerdefinierte Benutzeroberfläche bereitzustellen.

-   [Standardmäßige Benutzeroberfläche](stream-attenuation.md)
-   [Deaktivieren der Standardbenutzeroberfläche für die Entzung](disabling-the-ducking-experience.md)
-   [Bereitstellen eines benutzerdefinierten Entzungsverhaltens](providing-a-custom-ducking-experience.md)
-   [Überlegungen zur Implementierung von Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md)
-   [Abrufen von Entzungsereignissen](getting-ducking-events-from-a-communication-device.md)

### <a name="getting-a-reference-to-the-communication-device-endpoint"></a>Abrufen eines Verweises auf den Endpunkt des Kommunikationsgeräts

Um das Kommunikationsgerät zu verwenden, muss ein direkter WASAPI-Client die Geräte mithilfe des Geräteenumerators aufzählen. Rufen Sie durch Aufrufen von [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)einen Verweis auf den Endpunkt des Standardkommunikationsgeräts ab. In diesem Aufruf muss die Anwendung **eCommunications** im *Role-Parameter* angeben, um die Geräteenumeration auf Kommunikationsgeräte zu beschränken. Nachdem Sie einen Verweis auf den Geräteendpunkt für das Gerät erhalten haben, können Sie die Dienste aktivieren, die für den Endpunkt gelten, indem Sie [**IMMDevice::Activate aufrufen.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) Beispielsweise können Sie den **\_ IID-IAudioClient-Dienstbezeichner** übergeben, um ein Audioclientobjekt zu aktivieren und für die Streamverwaltung zu verwenden, den **\_ IID-IAudioEndpointVolume-Bezeichner,** um Zugriff auf die Volumesteuerelemente des Endpunkts des Kommunikationsgeräts zu erhalten, oder den **\_ IID-IAudioSessionManager-Bezeichner,** um den Sitzungs-Manager zu aktivieren, mit dem Sie mit der Richtlinien-Engine des Endpunkts interagieren können. Informationen zu Streamvorgängen finden Sie unter [Stream Management](stream-management.md).

Mithilfe des [**IMMDevice-Verweises**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) können Sie auch auf den Eigenschaftenspeicher für den Geräteendpunkt zugreifen. Diese Eigenschaftswerte, z. B. Anzeigename des Geräts und Herstellername, werden vom OEM aufgefüllt und ermöglichen es einer Anwendung, die Merkmale eines Kommunikationsgeräts zu bestimmen. Weitere Informationen finden Sie unter [Geräteeigenschaften.](device-properties.md)

Der folgende Beispielcode ruft einen Verweis auf den Endpunkt des Standardkommunikationsgeräts zum Rendern eines Audiodatenstroms ab.


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

[Streamverwaltung](stream-management.md)
</dt> </dl>

 

 



