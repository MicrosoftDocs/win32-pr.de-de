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
# <a name="disabling-the-default-ducking-experience"></a><span data-ttu-id="9bcc9-103">Deaktivieren der Standardeinstellung für das ducken</span><span class="sxs-lookup"><span data-stu-id="9bcc9-103">Disabling the Default Ducking Experience</span></span>

<span data-ttu-id="9bcc9-104">Ein Benutzer kann die vom System bereitgestellte [standardmäßige Ducking](stream-attenuation.md) -Benutzerfreundlichkeit mithilfe der Optionen deaktivieren, die auf der Registerkarte " **Kommunikation** " der Windows-Multimedia-Systemsteuerung (Mmsys.cpl) verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-104">A user can disable the [Default Ducking Experience](stream-attenuation.md) provided by the system by using the options that are available on the **Communications** tab of the Windows multimedia control panel, Mmsys.cpl.</span></span>

<span data-ttu-id="9bcc9-105">Wenn das Einblenden angewendet wird, wird für einen Zeitraum von 1 Sekunde ein Ausblend-und einblenden Effekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-105">When ducking is applied, a fade-out and fade-in effect is used for a period of 1 second.</span></span> <span data-ttu-id="9bcc9-106">Eine Spiel Anwendung möchte möglicherweise nicht, dass der Kommunikationsstream die Spiel Audiodaten beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-106">A game application might not want the communication stream to interfere with the game audio.</span></span> <span data-ttu-id="9bcc9-107">Einige Medienanwendungen stellen möglicherweise fest, dass die Wiedergabe Darstellung jarringvorgänge ist, wenn Musik wieder in den Hintergrund kommt.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-107">Some media applications might find that the playback experience is jarring when music fades back in.</span></span> <span data-ttu-id="9bcc9-108">Diese Arten von Anwendungen können auswählen, dass Sie nicht an der Ducking-Funktion teilnehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-108">These types of applications can choose not to participate in the ducking experience.</span></span>

<span data-ttu-id="9bcc9-109">Programm gesteuert kann ein direkter WASAPI-Client den Sitzungs-Manager für die Audiositzung verwenden, die die volumesteuerung für die nicht-Kommunikationsstreams bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-109">Programmatically, a direct WASAPI client can opt out by using the session manager for the audio session that provides volume control for the non-communication streams.</span></span> <span data-ttu-id="9bcc9-110">Beachten Sie, dass auch dann, wenn ein Client nicht mit dem ducken beendet wird, trotzdem Benachrichtigungen vom System empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-110">Note that even if an client opts out of ducking, it still receives ducking notifications from the system.</span></span>

<span data-ttu-id="9bcc9-111">Um das einducken zu abonnieren, muss der Client einen Verweis auf die [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) -Schnittstelle des Sitzungs-Managers erhalten.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-111">To opt out of ducking, the client must get a reference to the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) interface of the session manager.</span></span> <span data-ttu-id="9bcc9-112">Führen Sie die folgenden Schritte aus, um das ducken zu abonnieren:</span><span class="sxs-lookup"><span data-stu-id="9bcc9-112">To opt out of the ducking experience, use the following steps:</span></span>

1.  <span data-ttu-id="9bcc9-113">Instanziieren Sie den Geräte Enumerator, und verwenden Sie ihn, um einen Verweis auf den Endpunkt des Geräts zu erhalten, das die Medien Anwendung zum Rendering des nicht-Kommunikationsstreams verwendet.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-113">Instantiate the device enumerator and use it to get a reference to the endpoint of the device that the media application is using to render the non-communication stream.</span></span>
2.  <span data-ttu-id="9bcc9-114">Aktivieren Sie den Sitzungs-Manager über den Geräte Endpunkt, und erhalten Sie einen Verweis auf die [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) -Schnittstelle des Sitzungs-Managers.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-114">Activate the session manager from the device endpoint and get a reference to the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) interface of the session manager.</span></span>
3.  <span data-ttu-id="9bcc9-115">Wenn Sie den [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) -Zeiger verwenden, erhalten Sie einen Verweis auf die [**iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) -Schnittstelle des Sitzungs-Managers.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-115">By using the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) pointer, get a reference to the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface of the session manager.</span></span>
4.  <span data-ttu-id="9bcc9-116">Fragen Sie die [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) von der [**iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-116">Query for the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) from the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface.</span></span>
5.  <span data-ttu-id="9bcc9-117">Aufrufen von [**IAudioSessionControl2:: setduckingpreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) und übergeben von **true** oder **false** , um die Ducking-Einstellung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-117">Call [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) and pass **TRUE** or **FALSE** to specify the ducking preference.</span></span> <span data-ttu-id="9bcc9-118">Die angegebene Einstellung kann während der Sitzung dynamisch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-118">The specified preference can be changed dynamically during the session.</span></span> <span data-ttu-id="9bcc9-119">Beachten Sie, dass die Opt-out-Änderung erst wirksam wird, wenn der Stream beendet und erneut gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-119">Note that the opt-out change does not take effect until the stream is stopped and started again.</span></span>

<span data-ttu-id="9bcc9-120">Der folgende Code zeigt, wie eine Anwendung ihre Ducking-Einstellung angeben kann.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-120">The following code shows how an application can specify its ducking preference.</span></span> <span data-ttu-id="9bcc9-121">Der Aufrufer der Funktion muss im Parameter "duckingoptoutcheck" den Wert " **true** " oder " **false** " übergeben.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-121">The caller of the function must pass **TRUE** or **FALSE** in the DuckingOptOutChecked parameter.</span></span> <span data-ttu-id="9bcc9-122">Abhängig vom übergebenen Wert wird das ducken mithilfe von [**IAudioSessionControl2:: setduckingpreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference)aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9bcc9-122">Depending on the value passed, ducking is enabled or disabled through the [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9bcc9-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9bcc9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bcc9-124">Verwenden eines kommunikationsgeräts</span><span class="sxs-lookup"><span data-stu-id="9bcc9-124">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="9bcc9-125">Standardmäßiges ducken</span><span class="sxs-lookup"><span data-stu-id="9bcc9-125">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="9bcc9-126">Bereitstellen eines benutzerdefinierten Ducking-Verhaltens</span><span class="sxs-lookup"><span data-stu-id="9bcc9-126">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="9bcc9-127">Implementierungs Überlegungen für Ducking-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="9bcc9-127">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="9bcc9-128">Erhalten von Ducking-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="9bcc9-128">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



