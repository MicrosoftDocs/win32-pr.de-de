---
description: Ein Benutzer kann die vom System bereitgestellte standardmäßige Ducking-Benutzerfreundlichkeit mithilfe der Optionen deaktivieren, die auf der Registerkarte "Kommunikation" der Windows-Multimedia-Systemsteuerung (Mmsys.cpl) verfügbar sind.
ms.assetid: 5604b927-99f8-450f-a48c-b38d782584de
title: Deaktivieren der Standardeinstellung für das ducken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed33fa7d9473cb5c68a018b98bff8a826612387e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127668"
---
# <a name="disabling-the-default-ducking-experience"></a>Deaktivieren der Standardeinstellung für das ducken

Ein Benutzer kann die vom System bereitgestellte [standardmäßige Ducking](stream-attenuation.md) -Benutzerfreundlichkeit mithilfe der Optionen deaktivieren, die auf der Registerkarte " **Kommunikation** " der Windows-Multimedia-Systemsteuerung (Mmsys.cpl) verfügbar sind.

Wenn das Einblenden angewendet wird, wird für einen Zeitraum von 1 Sekunde ein Ausblend-und einblenden Effekt verwendet. Eine Spiel Anwendung möchte möglicherweise nicht, dass der Kommunikationsstream die Spiel Audiodaten beeinträchtigt. Einige Medienanwendungen stellen möglicherweise fest, dass die Wiedergabe Darstellung jarringvorgänge ist, wenn Musik wieder in den Hintergrund kommt. Diese Arten von Anwendungen können auswählen, dass Sie nicht an der Ducking-Funktion teilnehmen möchten.

Programm gesteuert kann ein direkter WASAPI-Client den Sitzungs-Manager für die Audiositzung verwenden, die die volumesteuerung für die nicht-Kommunikationsstreams bereitstellt. Beachten Sie, dass auch dann, wenn ein Client nicht mit dem ducken beendet wird, trotzdem Benachrichtigungen vom System empfangen werden.

Um das einducken zu abonnieren, muss der Client einen Verweis auf die [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) -Schnittstelle des Sitzungs-Managers erhalten. Führen Sie die folgenden Schritte aus, um das ducken zu abonnieren:

1.  Instanziieren Sie den Geräte Enumerator, und verwenden Sie ihn, um einen Verweis auf den Endpunkt des Geräts zu erhalten, das die Medien Anwendung zum Rendering des nicht-Kommunikationsstreams verwendet.
2.  Aktivieren Sie den Sitzungs-Manager über den Geräte Endpunkt, und erhalten Sie einen Verweis auf die [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) -Schnittstelle des Sitzungs-Managers.
3.  Wenn Sie den [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) -Zeiger verwenden, erhalten Sie einen Verweis auf die [**iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) -Schnittstelle des Sitzungs-Managers.
4.  Fragen Sie die [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) von der [**iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) -Schnittstelle ab.
5.  Aufrufen von [**IAudioSessionControl2:: setduckingpreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) und übergeben von **true** oder **false** , um die Ducking-Einstellung anzugeben. Die angegebene Einstellung kann während der Sitzung dynamisch geändert werden. Beachten Sie, dass die Opt-out-Änderung erst wirksam wird, wenn der Stream beendet und erneut gestartet wurde.

Der folgende Code zeigt, wie eine Anwendung ihre Ducking-Einstellung angeben kann. Der Aufrufer der Funktion muss im Parameter "duckingoptoutcheck" den Wert " **true** " oder " **false** " übergeben. Abhängig vom übergebenen Wert wird das ducken mithilfe von [**IAudioSessionControl2:: setduckingpreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference)aktiviert oder deaktiviert.


```C++
////////////////////////////////////////////////////////////////////
//Description: Specifies the ducking options for the application.
//Parameters: 
//    If DuckingOptOutChecked is TRUE system ducking is disabled; 
//    FALSE, system ducking is enabled.
////////////////////////////////////////////////////////////////////

HRESULT DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;


    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>(&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(NULL, 0, &pSessionControl);
        
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                  __uuidof(IAudioSessionControl2),
                  (void**)&pSessionControl2);
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    //  Sync the ducking state with the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionControl2->SetDuckingPreference(TRUE);
        }
        else
        {
            hr = pSessionControl2->SetDuckingPreference(FALSE);
        }
        pSessionControl2->Release();
        pSessionControl2 = NULL;
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

[Bereitstellen eines benutzerdefinierten Ducking-Verhaltens](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Implementierungs Überlegungen für Ducking-Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Erhalten von Ducking-Ereignissen](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



