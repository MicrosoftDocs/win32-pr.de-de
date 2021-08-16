---
description: Eine Medienanwendung, die eine abgesperrte Benutzeroberfläche bereitstellen möchte, muss auf die Ereignisbenachrichtigungen lauschen, wenn ein Kommunikationsstream im System geöffnet oder geschlossen wird.
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: Abrufen von Entzungsereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5869aa02a64ef3b7d035743b9bee3c91d295448c4d89d659862c5efc81d89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828261"
---
# <a name="getting-ducking-events"></a>Abrufen von Entzungsereignissen

Eine Medienanwendung, die eine abgesperrte Benutzeroberfläche bereitstellen möchte, muss auf die Ereignisbenachrichtigungen lauschen, wenn ein Kommunikationsstream im System geöffnet oder geschlossen wird. Die benutzerdefinierte Implementierung kann mit MediaFoundation, DirectShow oder DirectSound bereitgestellt werden, die die Core Audio-APIs verwenden. Ein direkter WASAPI-Client kann auch die Standardbehandlung überschreiben, wenn er weiß, wann die Kommunikationssitzung gestartet und beendet wird.

Um eine benutzerdefinierte Implementierung bereitzustellen, muss eine Medienanwendung Benachrichtigungen vom System erhalten, wenn eine Kommunikationsanwendung einen Kommunikationsstream startet oder beendet. Die Medienanwendung muss die [**IAudioVolumeDuckNotification-Schnittstelle**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) implementieren und die Implementierung beim Audiosystem registrieren. Nach erfolgreicher Registrierung empfängt die Medienanwendung Ereignisbenachrichtigungen in Form von Rückrufen über die Methoden in der -Schnittstelle. Weitere Informationen finden Sie unter [Implementierungsüberlegungen für Entenbenachrichtigungen.](handling-audio-ducking-events-from-communication-devices.md)

Zum Senden von Entzungsbenachrichtigungen muss das Audiosystem wissen, welche Audiositzung auf die Abhörereignisse lauscht. Jede Audiositzung wird eindeutig mit einer GUID identifiziert– dem Sitzungsinstanzbezeichner. Mit dem Sitzungs-Manager kann eine Anwendung Informationen zur Sitzung abrufen, z. B. den Titel der Audiositzung, den Renderingzustand und den Sitzungsinstanzbezeichner. Der Bezeichner kann mithilfe der Richtliniensteuerungsschnittstelle [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)abgerufen werden.

In den folgenden Schritten wird der Prozess zum Abrufen des Sitzungsinstanzbezeichners der Medienanwendung zusammengefasst:

1.  Instanziieren Sie den Geräteenumerator, und verwenden Sie ihn, um einen Verweis auf den Endpunkt des Geräts abzurufen, den die Medienanwendung zum Rendern des Nichtkommunikationsdatenstroms verwendet.
2.  Aktivieren Sie den Sitzungs-Manager über den Geräteendpunkt, und erhalten Sie einen Verweis auf die [**IAudioSessionManager2-Schnittstelle**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) des Sitzungs-Managers.
3.  Mithilfe des [**IAudioSessionManager2-Zeigers**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) können Sie einen Verweis auf die [**IAudioSessionControl-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) des Sitzungs-Managers abrufen.
4.  Fragen Sie [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) über die [**IAudioSessionControl-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) ab.
5.  Rufen Sie [**IAudioSessionControl2::GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) auf, und rufen Sie eine Zeichenfolge ab, die den Sitzungsbezeichner für die aktuelle Audiositzung enthält.

Die Medienanwendung ruft [**IAudioSessionManager2::RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification)auf, um Benachrichtigungen zu Kommunikationsdatenströmen zu erhalten. Die Medienanwendung stellt ihren Sitzungsinstanzbezeichner für das Audiosystem und einen Zeiger auf die [**IAudioVolumeDuckNotification-Implementierung**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) bereit. Die Anwendung kann jetzt ereignisbenachrichtigungen empfangen, wenn ein Stream auf dem Kommunikationsgerät geöffnet wird. Um das Abrufen von Benachrichtigungen zu beenden, muss die Medienanwendung [**IAudioSessionManager2::UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification)aufrufen.

Der folgende Code zeigt, wie sich eine Anwendung registrieren kann, um Entzungsbenachrichtigungen zu erhalten. Die CMediaPlayer-Klasse ist unter [Implementierungsüberlegungen für Entzungsbenachrichtigungen](handling-audio-ducking-events-from-communication-devices.md)definiert. Im [Beispiel "MultiplayeringMediaPlayer"](duckingmediaplayer.md) wird diese Funktionalität implementiert.


```C++
////////////////////////////////////////////////////////////////////
//Description: Registers for duck notifications depending on the 
//             the ducking options specified by the caller.
//Parameters: 
//    If DuckingOptOutChecked is TRUE, the client is registered for
//    to receive ducking notifications; 
//    FALSE, the client's registration is deleted.
////////////////////////////////////////////////////////////////////

HRESULT CMediaPlayer::DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;

    LPWSTR sessionId = NULL;

    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(
              eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate the session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>
                                 (&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(
                                  NULL, 0, &pSessionControl);
        
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                               IID_PPV_ARGS(&pSessionControl2));
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    // Get the session instance identifier.
    
    if (SUCCEEDED(hr))
    {
        hr = pSessionControl2->GetSessionInstanceIdentifier(
                                 sessionId);
                
        pSessionControl2->Release();
        pSessionControl2 = NULL;
    }

    //  Register for ducking events depending on 
    //  the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionManager2->RegisterDuckNotification(
                                    sessionId, this);
        }
        else
        {
            hr = pSessionManager2->UnregisterDuckNotification
                                      (FALSE);
        }
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden eines Kommunikationsgeräts](using-the-communication-device.md)
</dt> <dt>

[Standardmäßige Benutzeroberfläche](stream-attenuation.md)
</dt> <dt>

[Deaktivieren der Standardbenutzeroberfläche für die Entzung](disabling-the-ducking-experience.md)
</dt> <dt>

[Bereitstellen eines benutzerdefinierten Entzungsverhaltens](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Überlegungen zur Implementierung von Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



