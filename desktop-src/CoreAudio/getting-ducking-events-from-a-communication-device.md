---
description: Eine Medien Anwendung, die eine angepasste Ducking-Funktion bereitstellen möchte, muss auf die Ereignis Benachrichtigungen lauschen, wenn ein Kommunikationsstream im System geöffnet oder geschlossen wird.
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: Erhalten von Ducking-Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e45557c25570a89452a39683a0b6732b9632129
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523723"
---
# <a name="getting-ducking-events"></a>Erhalten von Ducking-Ereignissen

Eine Medien Anwendung, die eine angepasste Ducking-Funktion bereitstellen möchte, muss auf die Ereignis Benachrichtigungen lauschen, wenn ein Kommunikationsstream im System geöffnet oder geschlossen wird. Die benutzerdefinierte Implementierung kann mithilfe von mediafoundations, DirectShow oder DirectSound bereitgestellt werden, die die kernaudio-APIs verwenden. Ein direkter WASAPI-Client kann die Standardbehandlung auch überschreiben, wenn er weiß, wann die Kommunikationssitzung gestartet und beendet wird.

Zum Bereitstellen einer benutzerdefinierten Implementierung muss eine Medien Anwendung Benachrichtigungen vom System erhalten, wenn eine Kommunikationsanwendung einen Kommunikationsstream startet oder beendet. Die Medien Anwendung muss die [**iaudiovolumeducknotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) -Schnittstelle implementieren und die Implementierung beim Audiosystem registrieren. Bei erfolgreicher Registrierung empfängt die Medien Anwendung Ereignis Benachrichtigungen in Form von Rückrufen durch die Methoden in der-Schnittstelle. Weitere Informationen finden Sie unter [Implementierungs Überlegungen für Ducking-Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md).

Zum Senden von Ducking-Benachrichtigungen muss das Audiosystem wissen, welche Audiositzung auf die Ducking-Ereignisse lauscht. Jede Audiositzung wird eindeutig durch eine GUID – sitzungsinstanzbezeichner identifiziert. Der Sitzungs-Manager ermöglicht es einer Anwendung, Informationen zur Sitzung zu erhalten, z. b. den Titel der Audiositzung, den renderingstatus und den sitzungsinstanzbezeichner. Der Bezeichner kann mithilfe der Richtlinien Steuerungs Schnittstelle [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)abgerufen werden.

In den folgenden Schritten wird der Prozess zum erhalten des sitzungsinstanzbezeichners der Medien Anwendung zusammengefasst:

1.  Instanziieren Sie den Geräte Enumerator, und verwenden Sie ihn, um einen Verweis auf den Endpunkt des Geräts zu erhalten, das die Medien Anwendung zum Rendering des nicht-Kommunikationsstreams verwendet.
2.  Aktivieren Sie den Sitzungs-Manager über den Geräte Endpunkt, und erhalten Sie einen Verweis auf die [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) -Schnittstelle des Sitzungs-Managers.
3.  Wenn Sie den [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) -Zeiger verwenden, erhalten Sie einen Verweis auf die [**iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) -Schnittstelle des Sitzungs-Managers.
4.  Fragen Sie die [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) von der [**iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) -Schnittstelle ab.
5.  Rufen Sie [**IAudioSessionControl2:: getessioninstanceidentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) auf, und rufen Sie eine Zeichenfolge ab, die den Sitzungs Bezeichner für die aktuelle Audiositzung enthält.

Um duckbenachrichtigungen zu Kommunikationsstreams zu erhalten, ruft die Medien Anwendung [**IAudioSessionManager2:: registerducknotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification)auf. Die Medien Anwendung stellt ihren sitzungsinstanzbezeichner für das Audiosystem und einen Zeiger auf die [**iaudiovolumeducknotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) -Implementierung bereit. Die Anwendung kann jetzt eine Ereignis Benachrichtigung erhalten, wenn ein Datenstrom auf dem Kommunikationsgerät geöffnet wird. Um die Benachrichtigung zu erhalten, muss die Medien Anwendung [**IAudioSessionManager2:: unregisterducknotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification)aufrufen.

Der folgende Code zeigt, wie eine Anwendung registriert werden kann, um Ducking-Benachrichtigungen zu erhalten. Die cmediaplayer-Klasse wird in [Implementierungs Überlegungen für das ducken von Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md)definiert. Das Beispiel " [duckingmediaplayer](duckingmediaplayer.md) " implementiert diese Funktion.


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

[Verwenden eines kommunikationsgeräts](using-the-communication-device.md)
</dt> <dt>

[Standardmäßiges ducken](stream-attenuation.md)
</dt> <dt>

[Deaktivieren der Standardeinstellung für das ducken](disabling-the-ducking-experience.md)
</dt> <dt>

[Bereitstellen eines benutzerdefinierten Ducking-Verhaltens](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Implementierungs Überlegungen für Ducking-Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



