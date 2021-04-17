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
# <a name="getting-ducking-events"></a><span data-ttu-id="2e1ff-103">Erhalten von Ducking-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="2e1ff-103">Getting Ducking Events</span></span>

<span data-ttu-id="2e1ff-104">Eine Medien Anwendung, die eine angepasste Ducking-Funktion bereitstellen möchte, muss auf die Ereignis Benachrichtigungen lauschen, wenn ein Kommunikationsstream im System geöffnet oder geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-104">A media application that wants to provide a customised ducking experience must listen for the event notifications when a communication stream is opened or closed in the system.</span></span> <span data-ttu-id="2e1ff-105">Die benutzerdefinierte Implementierung kann mithilfe von mediafoundations, DirectShow oder DirectSound bereitgestellt werden, die die kernaudio-APIs verwenden.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-105">The custom implementation can be provided by using MediaFoundation, DirectShow, or DirectSound, which use the Core Audio APIs.</span></span> <span data-ttu-id="2e1ff-106">Ein direkter WASAPI-Client kann die Standardbehandlung auch überschreiben, wenn er weiß, wann die Kommunikationssitzung gestartet und beendet wird.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-106">A direct WASAPI client can also override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="2e1ff-107">Zum Bereitstellen einer benutzerdefinierten Implementierung muss eine Medien Anwendung Benachrichtigungen vom System erhalten, wenn eine Kommunikationsanwendung einen Kommunikationsstream startet oder beendet.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-107">To provide a custom implementation, a media application needs to get notifications from the system when a communication application starts or ends a communication stream.</span></span> <span data-ttu-id="2e1ff-108">Die Medien Anwendung muss die [**iaudiovolumeducknotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) -Schnittstelle implementieren und die Implementierung beim Audiosystem registrieren.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-108">The media application must implement the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface and register the implementation with the audio system.</span></span> <span data-ttu-id="2e1ff-109">Bei erfolgreicher Registrierung empfängt die Medien Anwendung Ereignis Benachrichtigungen in Form von Rückrufen durch die Methoden in der-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-109">Upon successful registration, the media application receives event notifications in the form of callbacks through the methods in the interface.</span></span> <span data-ttu-id="2e1ff-110">Weitere Informationen finden Sie unter [Implementierungs Überlegungen für Ducking-Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="2e1ff-110">For more information, see [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span>

<span data-ttu-id="2e1ff-111">Zum Senden von Ducking-Benachrichtigungen muss das Audiosystem wissen, welche Audiositzung auf die Ducking-Ereignisse lauscht.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-111">To send ducking notifications, the audio system must know which audio session is listening for the ducking events.</span></span> <span data-ttu-id="2e1ff-112">Jede Audiositzung wird eindeutig durch eine GUID – sitzungsinstanzbezeichner identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-112">Each audio session is uniquely identified with a GUID—session instance identifier.</span></span> <span data-ttu-id="2e1ff-113">Der Sitzungs-Manager ermöglicht es einer Anwendung, Informationen zur Sitzung zu erhalten, z. b. den Titel der Audiositzung, den renderingstatus und den sitzungsinstanzbezeichner.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-113">The session manager allows an application to get information about the session such as title of audio session, the rendering state, and the session instance identifier.</span></span> <span data-ttu-id="2e1ff-114">Der Bezeichner kann mithilfe der Richtlinien Steuerungs Schnittstelle [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-114">The identifier can be retrieved by using the policy control interface, [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).</span></span>

<span data-ttu-id="2e1ff-115">In den folgenden Schritten wird der Prozess zum erhalten des sitzungsinstanzbezeichners der Medien Anwendung zusammengefasst:</span><span class="sxs-lookup"><span data-stu-id="2e1ff-115">The following steps summarize the process of getting the session instance identifier of the media application:</span></span>

1.  <span data-ttu-id="2e1ff-116">Instanziieren Sie den Geräte Enumerator, und verwenden Sie ihn, um einen Verweis auf den Endpunkt des Geräts zu erhalten, das die Medien Anwendung zum Rendering des nicht-Kommunikationsstreams verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-116">Instantiate the device enumerator and use it to get a reference to the endpoint of the device that the media application is using to render the non-communication stream.</span></span>
2.  <span data-ttu-id="2e1ff-117">Aktivieren Sie den Sitzungs-Manager über den Geräte Endpunkt, und erhalten Sie einen Verweis auf die [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) -Schnittstelle des Sitzungs-Managers.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-117">Activate the session manager from the device endpoint and get a reference to the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) interface of the session manager.</span></span>
3.  <span data-ttu-id="2e1ff-118">Wenn Sie den [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) -Zeiger verwenden, erhalten Sie einen Verweis auf die [**iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) -Schnittstelle des Sitzungs-Managers.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-118">By using the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) pointer, get a reference to the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface of the session manager.</span></span>
4.  <span data-ttu-id="2e1ff-119">Fragen Sie die [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) von der [**iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-119">Query for the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) from the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface.</span></span>
5.  <span data-ttu-id="2e1ff-120">Rufen Sie [**IAudioSessionControl2:: getessioninstanceidentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) auf, und rufen Sie eine Zeichenfolge ab, die den Sitzungs Bezeichner für die aktuelle Audiositzung enthält.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-120">Call [**IAudioSessionControl2::GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) and retrieve a string that contains the session identifier for the current audio session.</span></span>

<span data-ttu-id="2e1ff-121">Um duckbenachrichtigungen zu Kommunikationsstreams zu erhalten, ruft die Medien Anwendung [**IAudioSessionManager2:: registerducknotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification)auf.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-121">To get ducking notifications about communication streams, the media application calls [**IAudioSessionManager2::RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification).</span></span> <span data-ttu-id="2e1ff-122">Die Medien Anwendung stellt ihren sitzungsinstanzbezeichner für das Audiosystem und einen Zeiger auf die [**iaudiovolumeducknotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) -Implementierung bereit.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-122">The media application supplies its session instance identifier to the audio system and a pointer to the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) implementation.</span></span> <span data-ttu-id="2e1ff-123">Die Anwendung kann jetzt eine Ereignis Benachrichtigung erhalten, wenn ein Datenstrom auf dem Kommunikationsgerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-123">The application can now receive event notification when a stream opened on the communication device.</span></span> <span data-ttu-id="2e1ff-124">Um die Benachrichtigung zu erhalten, muss die Medien Anwendung [**IAudioSessionManager2:: unregisterducknotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-124">To stop getting notification, the media application must call [**IAudioSessionManager2::UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).</span></span>

<span data-ttu-id="2e1ff-125">Der folgende Code zeigt, wie eine Anwendung registriert werden kann, um Ducking-Benachrichtigungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-125">The following code shows how an application can register to get ducking notifications.</span></span> <span data-ttu-id="2e1ff-126">Die cmediaplayer-Klasse wird in [Implementierungs Überlegungen für das ducken von Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-126">The CMediaPlayer class is defined in [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span> <span data-ttu-id="2e1ff-127">Das Beispiel " [duckingmediaplayer](duckingmediaplayer.md) " implementiert diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="2e1ff-127">The [DuckingMediaPlayer](duckingmediaplayer.md) sample implements this functionality.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2e1ff-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2e1ff-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e1ff-129">Verwenden eines kommunikationsgeräts</span><span class="sxs-lookup"><span data-stu-id="2e1ff-129">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="2e1ff-130">Standardmäßiges ducken</span><span class="sxs-lookup"><span data-stu-id="2e1ff-130">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="2e1ff-131">Deaktivieren der Standardeinstellung für das ducken</span><span class="sxs-lookup"><span data-stu-id="2e1ff-131">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="2e1ff-132">Bereitstellen eines benutzerdefinierten Ducking-Verhaltens</span><span class="sxs-lookup"><span data-stu-id="2e1ff-132">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="2e1ff-133">Implementierungs Überlegungen für Ducking-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="2e1ff-133">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



