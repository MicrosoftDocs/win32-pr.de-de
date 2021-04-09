---
description: Audiositzungsereignisse
ms.assetid: 6943b405-0807-412b-a149-fc3a8ece1b48
title: Audiositzungsereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ec5de18c883f817c2f650ccfc48ad0149ac84e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958390"
---
# <a name="audio-session-events"></a><span data-ttu-id="cca72-103">Audiositzungsereignisse</span><span class="sxs-lookup"><span data-stu-id="cca72-103">Audio Session Events</span></span>

<span data-ttu-id="cca72-104">Eine Anwendung, die Audiodatenströme im freigegebenen Modus verwaltet, kann beim Auftreten von Sitzungs Ereignissen registriert werden, um Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="cca72-104">An application that manages shared-mode audio streams can register to receive notifications when session events occur.</span></span> <span data-ttu-id="cca72-105">Wie bereits erläutert, gehört jeder Stream zu einer [Audiositzung](audio-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="cca72-105">As explained previously, each stream belongs to an [audio session](audio-sessions.md).</span></span> <span data-ttu-id="cca72-106">Ein Sitzungs Ereignis wird durch eine Änderung des Status einer Audiositzung initiiert.</span><span class="sxs-lookup"><span data-stu-id="cca72-106">A session event is initiated by a change in the status of an audio session.</span></span>

<span data-ttu-id="cca72-107">Eine Client Anwendung kann sich registrieren, um Benachrichtigungen über die folgenden Sitzungs Ereignis Typen zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="cca72-107">A client application can register to receive notifications of the following types of session events:</span></span>

-   <span data-ttu-id="cca72-108">Die Master Volume-Ebene oder der stumm Schaltung-Status der Sitzungs teilmischung hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="cca72-108">The master volume level or muting state of the session submix has changed.</span></span>
-   <span data-ttu-id="cca72-109">Die Volumeebene eines oder mehrerer Kanäle der Sitzungs teilmischung hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="cca72-109">The volume level of one or more channels of the session submix has changed.</span></span>
-   <span data-ttu-id="cca72-110">Die Sitzung wurde getrennt.</span><span class="sxs-lookup"><span data-stu-id="cca72-110">The session has been disconnected.</span></span>
-   <span data-ttu-id="cca72-111">Der Aktivitätsstatus der Sitzung wurde in "aktiv", "inaktiv" oder "abgelaufen" geändert.</span><span class="sxs-lookup"><span data-stu-id="cca72-111">The activity state of the session has changed to active, inactive, or expired.</span></span>
-   <span data-ttu-id="cca72-112">Der Sitzung wurde ein neuer Gruppierungs Parameter zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="cca72-112">The session has been assigned a new grouping parameter.</span></span>
-   <span data-ttu-id="cca72-113">Eine Benutzeroberflächen Eigenschaft der Sitzung (Symbol oder Anzeige Name) wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="cca72-113">A user-interface property of the session (icon or display name) has changed.</span></span>

<span data-ttu-id="cca72-114">Der Client empfängt Benachrichtigungen über diese Ereignisse über die Methoden in der Implementierung der [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cca72-114">The client receives notifications of these events through the methods in its implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="cca72-115">Im Gegensatz zu den anderen Schnittstellen in WASAPI, die vom WASAPI-Systemmodul implementiert werden, implementiert der Client **iaudiosessionevents**.</span><span class="sxs-lookup"><span data-stu-id="cca72-115">Unlike the other interfaces in WASAPI, which are implemented by the WASAPI system module, the client implements **IAudioSessionEvents**.</span></span> <span data-ttu-id="cca72-116">Die Methoden in dieser Schnittstelle empfangen Rückrufe vom WASAPI-Systemmodul, wenn Sitzungs Ereignisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="cca72-116">The methods in this interface receive callbacks from the WASAPI system module when session events occur.</span></span>

<span data-ttu-id="cca72-117">Um mit dem Empfang von Benachrichtigungen zu beginnen, ruft der Client die [**iaudiosessioncontrol:: registeraudiosessionnotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) -Methode auf, um die [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="cca72-117">To begin receiving notifications, the client calls the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method to register its [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="cca72-118">Wenn der Client keine Benachrichtigungen mehr erfordert, ruft er die [**iaudiosessioncontrol:: unregisteraudiosessionnotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) -Methode auf, um die Registrierung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="cca72-118">When the client no longer requires notifications, it calls the [**IAudioSessionControl::UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) method to delete the registration.</span></span>

<span data-ttu-id="cca72-119">Im folgenden Codebeispiel wird eine mögliche Implementierung der [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="cca72-119">The following code example shows a possible implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface:</span></span>


```C++
//-----------------------------------------------------------
// Client implementation of IAudioSessionEvents interface.
// WASAPI calls these methods to notify the application when
// a parameter or property of the audio session changes.
//-----------------------------------------------------------
class CAudioSessionEvents : public IAudioSessionEvents
{
    LONG _cRef;

public:
    CAudioSessionEvents() :
        _cRef(1)
    {
    }

    ~CAudioSessionEvents()
    {
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID  riid,
                                VOID  **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IAudioSessionEvents) == riid)
        {
            AddRef();
            *ppvInterface = (IAudioSessionEvents*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Notification methods for audio session events

    HRESULT STDMETHODCALLTYPE OnDisplayNameChanged(
                                LPCWSTR NewDisplayName,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnIconPathChanged(
                                LPCWSTR NewIconPath,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnSimpleVolumeChanged(
                                float NewVolume,
                                BOOL NewMute,
                                LPCGUID EventContext)
    {
        if (NewMute)
        {
            printf("MUTE\n");
        }
        else
        {
            printf("Volume = %d percent\n",
                   (UINT32)(100*NewVolume + 0.5));
        }

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnChannelVolumeChanged(
                                DWORD ChannelCount,
                                float NewChannelVolumeArray[],
                                DWORD ChangedChannel,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnGroupingParamChanged(
                                LPCGUID NewGroupingParam,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnStateChanged(
                                AudioSessionState NewState)
    {
        char *pszState = "?????";

        switch (NewState)
        {
        case AudioSessionStateActive:
            pszState = "active";
            break;
        case AudioSessionStateInactive:
            pszState = "inactive";
            break;
        }
        printf("New session state = %s\n", pszState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnSessionDisconnected(
              AudioSessionDisconnectReason DisconnectReason)
    {
        char *pszReason = "?????";

        switch (DisconnectReason)
        {
        case DisconnectReasonDeviceRemoval:
            pszReason = "device removed";
            break;
        case DisconnectReasonServerShutdown:
            pszReason = "server shut down";
            break;
        case DisconnectReasonFormatChanged:
            pszReason = "format changed";
            break;
        case DisconnectReasonSessionLogoff:
            pszReason = "user logged off";
            break;
        case DisconnectReasonSessionDisconnected:
            pszReason = "session disconnected";
            break;
        case DisconnectReasonExclusiveModeOverride:
            pszReason = "exclusive-mode override";
            break;
        }
        printf("Audio session disconnected (reason: %s)\n",
               pszReason);

        return S_OK;
    }
};
```



<span data-ttu-id="cca72-120">Die caudiosessionevents-Klasse im vorangehenden Codebeispiel ist eine Implementierung der [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cca72-120">The CAudioSessionEvents class in the preceding code example is an implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="cca72-121">Diese spezielle Implementierung ist möglicherweise Teil einer Konsolenanwendung, die Informationen zu Sitzungs Ereignissen in einem Eingabe Aufforderungs Fenster ausgibt.</span><span class="sxs-lookup"><span data-stu-id="cca72-121">This particular implementation might be part of a console application that prints information about session events to a Command Prompt window.</span></span> <span data-ttu-id="cca72-122">Da **iaudiosessionevents** von [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)erbt, enthält die Klassendefinition Implementierungen der **IUnknown** -Methoden [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)und [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="cca72-122">Because **IAudioSessionEvents** inherits from [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), the class definition contains implementations of the **IUnknown** methods [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="cca72-123">Die übrigen öffentlichen Methoden in der Klassendefinition sind spezifisch für die **iaudiosessionevents** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cca72-123">The remaining public methods in the class definition are specific to the **IAudioSessionEvents** interface.</span></span>

<span data-ttu-id="cca72-124">Einige Clients sind möglicherweise nicht für die Überwachung aller Typen von Sitzungs Ereignissen interessiert.</span><span class="sxs-lookup"><span data-stu-id="cca72-124">Some clients might not be interested in monitoring all types of session events.</span></span> <span data-ttu-id="cca72-125">Im vorangehenden Codebeispiel führen verschiedene Benachrichtigungs Methoden in der caudiosessionevents-Klasse keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="cca72-125">In the preceding code example, several notification methods in the CAudioSessionEvents class do nothing.</span></span> <span data-ttu-id="cca72-126">Beispielsweise führt die [**onchannelvolumechaning**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) -Methode keine Ausnahme aus, wenn der Statuscode "OK" zurückgegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="cca72-126">For example, the [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) method does nothing except to return status code S\_OK.</span></span> <span data-ttu-id="cca72-127">Von dieser Anwendung werden keine kanalvolumes überwacht, da die kanalvolumes nicht geändert werden (durch Aufrufen der Methoden in der Schnittstelle [**ichannelaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) ) und die Sitzung nicht mit anderen Anwendungen gemeinsam genutzt wird, die möglicherweise die kanalvolumes ändern.</span><span class="sxs-lookup"><span data-stu-id="cca72-127">This application does not monitor channel volumes because it does not change the channel volumes (by calling the methods in the [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) interface), and it does not share the session with other applications that might change the channel volumes.</span></span>

<span data-ttu-id="cca72-128">Die einzigen drei Methoden in der caudiosessionevents-Klasse, die den Benutzer über Sitzungs Ereignisse benachrichtigen, sind [**onsimplevolumechaning**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged)und [**onsessiongetrennte**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected).</span><span class="sxs-lookup"><span data-stu-id="cca72-128">The only three methods in the CAudioSessionEvents class that notify the user of session events are [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged), and [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected).</span></span> <span data-ttu-id="cca72-129">Wenn der Benutzer z. b. das System Volume-Control-Programm, sndvol, ausführt und das Volume-Steuerelement in sndvol verwendet, um die Volumeebene der Anwendung zu ändern, `OnSimpleVolumeChanged` druckt sofort die neue Volumeebene.</span><span class="sxs-lookup"><span data-stu-id="cca72-129">For example, if the user runs the system volume-control program, Sndvol, and uses the volume control in Sndvol to change the application's volume level, `OnSimpleVolumeChanged` immediately prints the new volume level.</span></span>

<span data-ttu-id="cca72-130">Ein Codebeispiel, in dem die [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle eines Clients registriert und die Registrierung aufgehoben wird, finden Sie unter [Audioereignisse für Legacy-Audioanwendungen](audio-events-for-legacy-audio-applications.md).</span><span class="sxs-lookup"><span data-stu-id="cca72-130">For a code example that registers and unregisters a client's [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface, see [Audio Events for Legacy Audio Applications](audio-events-for-legacy-audio-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cca72-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cca72-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cca72-132">Audiositzungen</span><span class="sxs-lookup"><span data-stu-id="cca72-132">Audio Sessions</span></span>](audio-sessions.md)
</dt> </dl>

 

 
