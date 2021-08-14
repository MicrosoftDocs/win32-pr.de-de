---
description: Audiositzungsereignisse
ms.assetid: 6943b405-0807-412b-a149-fc3a8ece1b48
title: Audiositzungsereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf0c3441a7f6f6835070a530c4ebb8985354b2701f312f2f085c5e449f12cbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407224"
---
# <a name="audio-session-events"></a>Audiositzungsereignisse

Eine Anwendung, die Audiostreams im freigegebenen Modus verwaltet, kann sich registrieren, um Benachrichtigungen zu empfangen, wenn Sitzungsereignisse auftreten. Wie bereits erläutert, gehört jeder Stream zu einer [Audiositzung.](audio-sessions.md) Ein Sitzungsereignis wird durch eine Änderung des Status einer Audiositzung initiiert.

Eine Clientanwendung kann sich registrieren, um Benachrichtigungen über die folgenden Arten von Sitzungsereignissen zu empfangen:

-   Die Mastervolumeebene oder der Mutingzustand des Sitzungsuntermix wurde geändert.
-   Die Volumeebene eines oder mehrerer Kanäle des Sitzungsuntermix wurde geändert.
-   Die Sitzung wurde getrennt.
-   Der Aktivitätsstatus der Sitzung wurde in aktiv, inaktiv oder abgelaufen geändert.
-   Der Sitzung wurde ein neuer Gruppierungsparameter zugewiesen.
-   Eine Benutzeroberflächeneigenschaft der Sitzung (Symbol oder Anzeigename) wurde geändert.

Der Client empfängt Benachrichtigungen über diese Ereignisse über die Methoden in seiner Implementierung der [**IAudioSessionEvents-Schnittstelle.**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) Im Gegensatz zu den anderen Schnittstellen in WASAPI, die vom WASAPI-Systemmodul implementiert werden, implementiert der Client **IAudioSessionEvents.** Die Methoden in dieser Schnittstelle empfangen Rückrufe vom WASAPI-Systemmodul, wenn Sitzungsereignisse auftreten.

Um mit dem Empfangen von Benachrichtigungen zu beginnen, ruft der Client die [**IAudioSessionControl::RegisterAudioSessionNotification-Methode**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) auf, um die [**IAudioSessionEvents-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) zu registrieren. Wenn der Client keine Benachrichtigungen mehr benötigt, ruft er die [**IAudioSessionControl::UnregisterAudioSessionNotification-Methode**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) auf, um die Registrierung zu löschen.

Das folgende Codebeispiel zeigt eine mögliche Implementierung der [**IAudioSessionEvents-Schnittstelle:**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)


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



Die CAudioSessionEvents-Klasse im vorherigen Codebeispiel ist eine Implementierung der [**IAudioSessionEvents-Schnittstelle.**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) Diese spezielle Implementierung kann Teil einer Konsolenanwendung sein, die Informationen zu Sitzungsereignissen in einem Eingabeaufforderungsfenster ausgibt. Da **IAudioSessionEvents** von [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)erbt, enthält die Klassendefinition Implementierungen der **IUnknown-Methoden** [**AddRef,**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)und [**QueryInterface.**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) Die verbleibenden öffentlichen Methoden in der Klassendefinition sind spezifisch für die **IAudioSessionEvents-Schnittstelle.**

Einige Clients sind möglicherweise nicht an der Überwachung aller Arten von Sitzungsereignissen interessiert. Im vorherigen Codebeispiel haben mehrere Benachrichtigungsmethoden in der CAudioSessionEvents-Klasse nichts zu tun. Die [**OnChannelVolumeChanged-Methode**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) gibt beispielsweise nur den Statuscode S \_ OK zurück. Diese Anwendung überwacht keine Kanalvolumes, da sie die Kanalvolumes nicht ändert (durch Aufrufen der Methoden in der [**IChannelAudioVolume-Schnittstelle),**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) und sie gibt die Sitzung nicht für andere Anwendungen frei, die die Kanalvolumes ändern können.

Die einzigen drei Methoden in der CAudioSessionEvents-Klasse, die den Benutzer über Sitzungsereignisse benachrichtigen, sind [**OnSimpleVolumeChanged,**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged)und [**OnSessionDisconnected.**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) Wenn der Benutzer beispielsweise das Systemvolume-Steuerungsprogramm Sndvol ausführt und die Volumesteuerung in Sndvol verwendet, um die Volumeebene der Anwendung zu ändern, `OnSimpleVolumeChanged` gibt sofort die neue Volumeebene aus.

Ein Codebeispiel zum Registrieren und Aufheben der Registrierung der [**IAudioSessionEvents-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) eines Clients finden Sie unter [Audioereignisse für Legacyaudioanwendungen.](audio-events-for-legacy-audio-applications.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiositzungen](audio-sessions.md)
</dt> </dl>

 

 
