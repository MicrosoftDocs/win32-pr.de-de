---
description: Erfahren Sie mehr über Benachrichtigungen für das Streamrouting. APIs implementieren das Streamrouting, indem sie den Streamwechsel zu einem neuen Standardaudioendpunkt verarbeiten.
ms.assetid: caf831bb-b8de-467f-bdb4-f9f8991dc7a8
title: Relevante Benachrichtigungen für das Streamrouting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0660735590853161395b1cf771ba17bbb72e48e072b2f9daa11a0841c9a5c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109460"
---
# <a name="relevant-notifications-for-stream-routing"></a>Relevante Benachrichtigungen für das Streamrouting

In Windows 7 implementieren high-level-Plattform-APIs, die Core Audio-APIs wie Media Foundation, DirectSound und Wave-APIs verwenden, das Streamroutingfeature, indem sie den Streamwechsel von einem vorhandenen Gerät zu einem neuen Standardaudioendpunkt verarbeiten. Medienanwendungen, die diese APIs verwenden, verwenden das Streamroutingverhalten ohne Änderungen an der Quelle. Direkte WASAPI-Clients können die von Core Audio-Komponenten gesendeten Benachrichtigungen verwenden und das Streamroutingfeature implementieren.

Um das Streamroutingfeature zu implementieren, muss ein Client auf zwei Arten von Ereignissen lauschen: Geräteänderungsbenachrichtigungen und Sitzungstrennungsbenachrichtigungen. In der von den übergeordneten APIs bereitgestellten Implementierung werden diese Ereignisse für Standardgeräteendpunkte gesendet, die durch Aufrufen von [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)erstellt werden. Weitere Informationen finden Sie unter [Abrufen des Geräteendpunkts für das Streamrouting.](getting-the-default-device-endpoint-for-stream-routing.md)

Die Core Audio-Komponente MMDeviceAPI übermittelt Benachrichtigungsrückrufe, wenn Audiogeräte hinzugefügt, entfernt oder geändert werden. Format- und Audiositzungsänderungen werden über WASAPI als Ereignisse gemeldet.

## <a name="device-change-notifications"></a>Geräteänderungsbenachrichtigungen

MMDeviceAPI löst Ereignisse aus, wenn Audiogeräte hinzugefügt, entfernt oder geändert werden. Wenn der Client Streamroutingfunktionen bereitstellen soll, muss er die [**IMMNotificationClient-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) implementieren und seine Implementierung bei MMDeviceAPI registrieren.

Um Geräteänderungsbenachrichtigungen zu erhalten, muss der Client die folgenden Aufgaben ausführen:

-   Implementieren Sie die [**IMMNotificationClient-Schnittstelle,**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) um geräteänderungsbenachrichtigungen zu verarbeiten, die von MMDeviceAPI gesendet werden.
-   Registrieren Sie die [**IMMNotificationClient-Implementierung**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) bei MMDeviceAPI, indem Sie die [**IMMDeviceEnumerator::RegisterEndpointNotificationCallback-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) aufrufen.

Nachdem die Implementierung dieser Schnittstellen durch den Client registriert wurde, empfängt der Client Benachrichtigungen in Form von Rückrufen über die Methoden dieser Schnittstellen. [**IMMNotificationClient-Methoden**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) werden von MMDeviceAPI aufgerufen, wenn sie Ereignisse auf Endpunktebene auslöst (Endpunktstatusänderungen, neue Endpunkteingänge, Endpunktlöschungen, Standardendpunktänderungen und Änderungen an Endpunkteigenschaften).

Wenn der Client das Streamrouting für das Standardgerät bereitstellen möchte, muss der Client das Geräteänderungsverhalten implementieren, wenn er die Benachrichtigung über den [**IMMNotificationClient::OnDefaultDeviceChanged-Rückruf empfängt.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged)

## <a name="audio-session-change-notifications"></a>Änderungsbenachrichtigungen für Audiositzung

Änderungen an Audiositzungen und Formatänderungen werden als Audiositzungsereignisse über WASAPI gemeldet. Ein WASAPI-Client implementiert die [**IAudioSessionEvents-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) und registriert die Implementierung bei WASAPI.

Um Änderungsbenachrichtigungen für Audiositzungen zu erhalten, muss der Client die folgenden Aufgaben ausführen:

-   Implementieren Sie die [**IAudioSessionEvents-Schnittstelle,**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) um formatänderungsbenachrichtigungen zu verarbeiten, die von WASAPI gesendet werden.
-   Registrieren Sie die [**IAudioSessionEvents-Implementierung**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) bei WASAPI, indem Sie die [**IAudioSessionControl::RegisterAudioSessionNotification-Methode**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) aufrufen.

[**IAudioSessionEvents-Methoden**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) werden von WASAPI aufgerufen, wenn Audiositzungsänderungen auftreten. Diese Ereignisse werden ausgelöst, wenn sich der Anzeigename, der Symbolpfad, das Volume, der Gruppierungsparameter oder der Status der Sitzung ändern.

Um das Streamroutingfeature zu implementieren, muss der Client auf die Sitzungstrennungsbenachrichtigung warten. Wenn eine Audiositzung getrennt wird oder das Format eines Geräts geändert wird, sendet WASAPI die Clientbenachrichtigungen in Form von Rückrufen über [**IAudioSessionEvents::OnSessionDisconnected.**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) Mit der Benachrichtigung zum Trennen der Verbindung sendet WASAPI auch einen Wert, der angibt, warum die Sitzung getrennt wurde. Dies kann aus verschiedenen Gründen auftreten, z. B. weil das Gerät entfernt wurde, der Server beendet wurde usw. Eine vollständige Liste der Gründe finden Sie in der in AudioPolicy.h definierten **AudioSessionDisconnectReason-Enumeration.** Wenn sich das Standardgerät ändert, muss der Client auf die Benachrichtigungen warten (sofern sie noch nicht empfangen wurden), die mit einem **DisconnectReasonDeviceRemoval-Wert** begleitet werden. Als Reaktion auf solche Benachrichtigungen kann der Client den Stream auf dem neuen Standardgerät erneut öffnen.

Da alle diese Vorgänge asychron sind, kann die Reihenfolge, in der die Anwendung Benachrichtigungen empfängt, nicht vorhergesagt werden. In der Regel empfängt die Anwendung jedoch den Wert **AudioSessionDisconnect** vor der Standardbenachrichtigung über Geräteänderungen.

### <a name="format-change-notifications"></a>Formatieren von Änderungsbenachrichtigungen

Audioformatänderungen treten auf, wenn sich das Format des Streams ändert. Dies kann auftreten, wenn der Benutzer  in der Sound-Systemsteuerung ein neues Format auswählt oder das neue Standardgerät ein neues Format unterstützt (z. B. EINEN ODERE oder bestimmte professionelle Audioschnittstellen mit einer manuellen Anpassung der Abtastrate). Um den Client über diese Formatänderungen zu benachrichtigen, sendet WASAPI eine Sitzungsbenachrichtigung von der registrierten Implementierung von [**IAudioSessionEvents::OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) mit dem Grund **disconnectReasonFormatChanged.** Der Client kann die Benachrichtigung verarbeiten, indem er den Stream im neuen Format erneut öffnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur MMDevice-API](mmdevice-api.md)
</dt> <dt>

[Informationen zu WASAPI](wasapi.md)
</dt> <dt>

[Streamrouting](stream-routing.md)
</dt> </dl>

 

 



