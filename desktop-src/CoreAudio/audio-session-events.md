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
# <a name="audio-session-events"></a>Audiositzungsereignisse

Eine Anwendung, die Audiodatenströme im freigegebenen Modus verwaltet, kann beim Auftreten von Sitzungs Ereignissen registriert werden, um Benachrichtigungen zu empfangen. Wie bereits erläutert, gehört jeder Stream zu einer [Audiositzung](audio-sessions.md). Ein Sitzungs Ereignis wird durch eine Änderung des Status einer Audiositzung initiiert.

Eine Client Anwendung kann sich registrieren, um Benachrichtigungen über die folgenden Sitzungs Ereignis Typen zu erhalten:

-   Die Master Volume-Ebene oder der stumm Schaltung-Status der Sitzungs teilmischung hat sich geändert.
-   Die Volumeebene eines oder mehrerer Kanäle der Sitzungs teilmischung hat sich geändert.
-   Die Sitzung wurde getrennt.
-   Der Aktivitätsstatus der Sitzung wurde in "aktiv", "inaktiv" oder "abgelaufen" geändert.
-   Der Sitzung wurde ein neuer Gruppierungs Parameter zugewiesen.
-   Eine Benutzeroberflächen Eigenschaft der Sitzung (Symbol oder Anzeige Name) wurde geändert.

Der Client empfängt Benachrichtigungen über diese Ereignisse über die Methoden in der Implementierung der [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle. Im Gegensatz zu den anderen Schnittstellen in WASAPI, die vom WASAPI-Systemmodul implementiert werden, implementiert der Client **iaudiosessionevents**. Die Methoden in dieser Schnittstelle empfangen Rückrufe vom WASAPI-Systemmodul, wenn Sitzungs Ereignisse auftreten.

Um mit dem Empfang von Benachrichtigungen zu beginnen, ruft der Client die [**iaudiosessioncontrol:: registeraudiosessionnotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) -Methode auf, um die [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle zu registrieren. Wenn der Client keine Benachrichtigungen mehr erfordert, ruft er die [**iaudiosessioncontrol:: unregisteraudiosessionnotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) -Methode auf, um die Registrierung zu löschen.

Im folgenden Codebeispiel wird eine mögliche Implementierung der [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle veranschaulicht:


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



Die caudiosessionevents-Klasse im vorangehenden Codebeispiel ist eine Implementierung der [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle. Diese spezielle Implementierung ist möglicherweise Teil einer Konsolenanwendung, die Informationen zu Sitzungs Ereignissen in einem Eingabe Aufforderungs Fenster ausgibt. Da **iaudiosessionevents** von [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)erbt, enthält die Klassendefinition Implementierungen der **IUnknown** -Methoden [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)und [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Die übrigen öffentlichen Methoden in der Klassendefinition sind spezifisch für die **iaudiosessionevents** -Schnittstelle.

Einige Clients sind möglicherweise nicht für die Überwachung aller Typen von Sitzungs Ereignissen interessiert. Im vorangehenden Codebeispiel führen verschiedene Benachrichtigungs Methoden in der caudiosessionevents-Klasse keine Aktion aus. Beispielsweise führt die [**onchannelvolumechaning**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) -Methode keine Ausnahme aus, wenn der Statuscode "OK" zurückgegeben wird \_ . Von dieser Anwendung werden keine kanalvolumes überwacht, da die kanalvolumes nicht geändert werden (durch Aufrufen der Methoden in der Schnittstelle [**ichannelaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) ) und die Sitzung nicht mit anderen Anwendungen gemeinsam genutzt wird, die möglicherweise die kanalvolumes ändern.

Die einzigen drei Methoden in der caudiosessionevents-Klasse, die den Benutzer über Sitzungs Ereignisse benachrichtigen, sind [**onsimplevolumechaning**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged)und [**onsessiongetrennte**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected). Wenn der Benutzer z. b. das System Volume-Control-Programm, sndvol, ausführt und das Volume-Steuerelement in sndvol verwendet, um die Volumeebene der Anwendung zu ändern, `OnSimpleVolumeChanged` druckt sofort die neue Volumeebene.

Ein Codebeispiel, in dem die [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle eines Clients registriert und die Registrierung aufgehoben wird, finden Sie unter [Audioereignisse für Legacy-Audioanwendungen](audio-events-for-legacy-audio-applications.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiositzungen](audio-sessions.md)
</dt> </dl>

 

 
