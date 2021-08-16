---
description: Ein Benutzer kann die vom System bereitgestellte Standardbenutzeroberfläche deaktivieren, indem er die Optionen verwendet, die auf der Registerkarte Kommunikation der Windows Multimedia-Systemsteuerung Mmsys.cpl verfügbar sind.
ms.assetid: 5604b927-99f8-450f-a48c-b38d782584de
title: Deaktivieren der Standardbenutzeroberfläche für die Entzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473b0bab8c3575d416cc72b7e931b4c85160bdaacc6031611ad80394f44b9098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828551"
---
# <a name="disabling-the-default-ducking-experience"></a>Deaktivieren der Standardbenutzeroberfläche für die Entzung

Ein Benutzer kann die vom System [bereitgestellte Standardbenutzeroberfläche](stream-attenuation.md) deaktivieren, indem er die Optionen verwendet, die auf der Registerkarte **Kommunikation** der Windows Multimedia-Systemsteuerung verfügbar sind, Mmsys.cpl.

Beim Anwenden von Abblendungen wird eine Einblendungs- und Einblendungswirkung für einen Zeitraum von 1 Sekunde verwendet. Eine Spielanwendung möchte möglicherweise nicht, dass der Kommunikationsdatenstrom die Spielaudiodaten beeinträchtigt. Einige Medienanwendungen stellen möglicherweise fest, dass die Wiedergabe nicht mehr erfolgt, wenn die Musik wieder einblendet. Diese Arten von Anwendungen können auswählen, dass sie nicht an der Benutzeroberfläche teilnehmen.

Programmgesteuert kann ein direkter WASAPI-Client die Verwendung des Sitzungs-Managers für die Audiositzung deaktivieren, der die Volumesteuerung für die Nichtkommunikationsstreams bereitstellt. Beachten Sie, dass ein Client selbst dann, wenn er sich von der Abmeldung abmeldet, immer noch Entenbenachrichtigungen vom System empfängt.

Um das Veralten zu deaktivieren, muss der Client einen Verweis auf die [**IAudioSessionControl2-Schnittstelle**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) des Sitzungs-Managers abrufen. Um die Entzungserfahrung zu deaktivieren, verwenden Sie die folgenden Schritte:

1.  Instanziieren Sie den Geräteenumerator, und verwenden Sie ihn, um einen Verweis auf den Endpunkt des Geräts abzurufen, den die Medienanwendung zum Rendern des Nichtkommunikationsdatenstroms verwendet.
2.  Aktivieren Sie den Sitzungs-Manager über den Geräteendpunkt, und erhalten Sie einen Verweis auf die [**IAudioSessionManager2-Schnittstelle**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) des Sitzungs-Managers.
3.  Mithilfe des [**IAudioSessionManager2-Zeigers**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) können Sie einen Verweis auf die [**IAudioSessionControl-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) des Sitzungs-Managers abrufen.
4.  Fragen Sie [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) über die [**IAudioSessionControl-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) ab.
5.  Rufen Sie [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) auf, und übergeben Sie **TRUE** oder **FALSE,** um die Enthaltungseinstellung anzugeben. Die angegebene Einstellung kann während der Sitzung dynamisch geändert werden. Beachten Sie, dass die Deaktivierungsänderung erst wirksam wird, wenn der Stream beendet und erneut gestartet wird.

Der folgende Code zeigt, wie eine Anwendung ihre Entzungspräferenz angeben kann. Der Aufrufer der Funktion muss **TRUE** oder **FALSE** im Parameter "TigeringOptOutChecked" übergeben. Abhängig vom übergebenen Wert wird das Entschließen über [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference)aktiviert oder deaktiviert.


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

[Verwenden eines Kommunikationsgeräts](using-the-communication-device.md)
</dt> <dt>

[Standardmäßige Benutzeroberfläche](stream-attenuation.md)
</dt> <dt>

[Bereitstellen eines benutzerdefinierten Entzungsverhaltens](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Überlegungen zur Implementierung von Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Abrufen von Entzungsereignissen](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



