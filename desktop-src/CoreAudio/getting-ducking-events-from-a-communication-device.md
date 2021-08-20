---
description: Eine Medienanwendung, die eine benutzerdefinierte Beschneidung bereitstellen möchte, muss auf die Ereignisbenachrichtigungen lauschen, wenn ein Kommunikationsstream im System geöffnet oder geschlossen wird.
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: Getting GettingIng Events (Getting GettingIng Events) (Abrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5869aa02a64ef3b7d035743b9bee3c91d295448c4d89d659862c5efc81d89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828261"
---
# <a name="getting-ducking-events"></a>Getting GettingIng Events (Getting GettingIng Events) (Abrufen

Eine Medienanwendung, die eine benutzerdefinierte Beschneidung bereitstellen möchte, muss auf die Ereignisbenachrichtigungen lauschen, wenn ein Kommunikationsstream im System geöffnet oder geschlossen wird. Die benutzerdefinierte Implementierung kann mit MediaFoundation, DirectShow oder DirectSound bereitgestellt werden, die die Core Audio-APIs verwenden. Ein direkter WASAPI-Client kann auch die Standardbehandlung überschreiben, wenn er weiß, wann die Kommunikationssitzung gestartet und beendet wird.

Um eine benutzerdefinierte Implementierung bereitstellen zu können, muss eine Medienanwendung Benachrichtigungen vom System erhalten, wenn eine Kommunikationsanwendung einen Kommunikationsstream startet oder beendet. Die Medienanwendung muss die [**IAudioVolumeDuckNotification-Schnittstelle**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) implementieren und die Implementierung beim Audiosystem registrieren. Nach erfolgreicher Registrierung empfängt die Medienanwendung Ereignisbenachrichtigungen in Form von Rückrufen über die Methoden in der Schnittstelle. Weitere Informationen finden Sie unter [Überlegungen zur Implementierung von Benachrichtigungen.](handling-audio-ducking-events-from-communication-devices.md)

Um Benachrichtigungen zu senden, muss das Audiosystem wissen, welche Audiositzung auf die abhörenden Ereignisse lausst. Jede Audiositzung wird eindeutig mit einer GUID identifiziert– sitzungsinstanzbezeichner. Mit dem Sitzungs-Manager kann eine Anwendung Informationen über die Sitzung wie den Titel der Audiositzung, den Renderingzustand und den Sitzungsinstanzbezeichner erhalten. Der Bezeichner kann mithilfe der Richtliniensteuerungsschnittstelle [**IAudioSessionControl2 abgerufen werden.**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)

Die folgenden Schritte fassen den Prozess zum Abrufen des Sitzungsinstanzbezeichners der Medienanwendung zusammen:

1.  Instanziieren Sie den Geräteenumerator, und verwenden Sie ihn, um einen Verweis auf den Endpunkt des Geräts zu erhalten, den die Medienanwendung zum Rendern des Nichtkommunikationsstreams verwendet.
2.  Aktivieren Sie den Sitzungs-Manager über den Geräteendpunkt, und erhalten Sie einen Verweis auf die [**IAudioSessionManager2-Schnittstelle**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) des Sitzungs-Managers.
3.  Mithilfe des [**IAudioSessionManager2-Zeigers**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) erhalten Sie einen Verweis auf die [**IAudioSessionControl-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) des Sitzungs-Managers.
4.  Fragen Sie [**IAudioSessionControl2 über**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) die [**IAudioSessionControl-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) ab.
5.  Rufen [**Sie IAudioSessionControl2::GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) auf, und rufen Sie eine Zeichenfolge ab, die den Sitzungsbezeichner für die aktuelle Audiositzung enthält.

Um Benachrichtigungen über Kommunikationsstreams zu erhalten, ruft die Medienanwendung [**IAudioSessionManager2::RegisterDuckNotification auf.**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification) Die Medienanwendung stellt den Sitzungsinstanzbezeichner für das Audiosystem und einen Zeiger auf die [**IAudioVolumeDuckNotification-Implementierung**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) zur Anwendung. Die Anwendung kann jetzt Ereignisbenachrichtigungen empfangen, wenn ein Stream auf dem Kommunikationsgerät geöffnet wird. Um die Benachrichtigung zu beenden, muss die Medienanwendung [**IAudioSessionManager2::UnregisterDuckNotification aufrufen.**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification)

Der folgende Code zeigt, wie sich eine Anwendung registrieren kann, um Benachrichtigungen zu erhalten. Die CMediaPlayer-Klasse ist in [Implementierungsüberlegungen für Benachrichtigungen definiert.](handling-audio-ducking-events-from-communication-devices.md) Diese Funktionalität wird im Beispiel ["IngMediaPlayer"](duckingmediaplayer.md) implementiert.


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

[Standardeinstellung für die Beeinschnung](stream-attenuation.md)
</dt> <dt>

[Deaktivieren der Standardmäßigen Begeherfahrung](disabling-the-ducking-experience.md)
</dt> <dt>

[Bereitstellen eines benutzerdefinierten Verhaltens bei der Abschüssung](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Überlegungen zur Implementierung von Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



