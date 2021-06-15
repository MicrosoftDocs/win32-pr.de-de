---
description: Erfahren Sie mehr über Benachrichtigungen für das Streamrouting. APIs implementieren Streamrouting, indem sie den Datenstromwechsel zu einem neuen Standardaudioendpunkt behandeln.
ms.assetid: caf831bb-b8de-467f-bdb4-f9f8991dc7a8
title: Relevante Benachrichtigungen für das Streamrouting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a843c1d8b5cfd740ada5049cb9428e7745072d
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068526"
---
# <a name="relevant-notifications-for-stream-routing"></a>Relevante Benachrichtigungen für das Streamrouting

In Windows 7 implementieren plattformübergreifende APIs, die Core Audio-APIs wie Media Foundation-, DirectSound- und Wave-APIs verwenden, das Streamroutingfeature, indem sie den Streamwechsel von einem vorhandenen Gerät zu einem neuen Standardaudioendpunkt behandeln. Medienanwendungen, die diese APIs verwenden, verwenden das Streamroutingverhalten ohne Änderungen an der Quelle. Direkte WASAPI-Clients können die von Core Audio-Komponenten gesendeten Benachrichtigungen verwenden und das Streamroutingfeature implementieren.

Um das Streamroutingfeature zu implementieren, muss ein Client auf zwei Arten von Ereignissen lauschen: Geräteänderungsbenachrichtigungen und Sitzungstrennungsbenachrichtigungen. In der von den apIs auf hoher Ebene bereitgestellten Implementierung werden diese Ereignisse für Standardgeräteendpunkte gesendet, die durch Aufrufen von [**IMMDeviceEnumerator::GetDefaultAudioEndpoint erstellt werden.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) Weitere Informationen finden Sie unter [Abrufen des Geräteendpunkts für das Streamrouting.](getting-the-default-device-endpoint-for-stream-routing.md)

Die Core Audio-Komponente MMDeviceAPI stellt Benachrichtigungsrückrufe zur Verfügung, wenn Audiogeräte hinzugefügt, entfernt oder geändert werden. Die Format- und Audiositzungsänderungen werden über WASAPI als Ereignisse gemeldet.

## <a name="device-change-notifications"></a>Geräteänderungsbenachrichtigungen

MMDeviceAPI löst Ereignisse aus, wenn Audiogeräte hinzugefügt, entfernt oder geändert werden. Wenn der Client Datenstromroutingfunktionen bereitstellen soll, muss er die [**IMMNotificationClient-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) implementieren und seine Implementierung bei MMDeviceAPI registrieren.

Um Geräteänderungsbenachrichtigungen zu erhalten, muss der Client die folgenden Aufgaben ausführen:

-   Implementieren Sie die [**IMMNotificationClient-Schnittstelle,**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) um von MMDeviceAPI gesendete Geräteänderungsbenachrichtigungen zu verarbeiten.
-   Registrieren Sie [**die IMMNotificationClient-Implementierung**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) bei MMDeviceAPI, indem Sie die [**IMMDeviceEnumerator::RegisterEndpointNotificationCallback-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) aufrufen.

Nachdem die Implementierung dieser Schnittstellen durch den Client registriert wurde, empfängt der Client Benachrichtigungen in Form von Rückrufen über die Methoden dieser Schnittstellen. [**IMMNotificationClient-Methoden**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) werden von MMDeviceAPI aufgerufen, wenn ereignisse auf Endpunktebene (Endpunktstatusänderungen, neue Endpunktankömmungen, Endpunktlöschungen, Standardendpunktänderungen und Änderungen der Endpunkteigenschaft) aufgerufen werden.

Wenn der Client Streamrouting für das Standardgerät bereitstellen möchte, muss der Client das Verhalten der Geräteänderung implementieren, wenn er die Benachrichtigung über den [**IMMNotificationClient::OnDefaultDeviceChanged-Rückruf**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) empfängt.

## <a name="audio-session-change-notifications"></a>Änderungsbenachrichtigungen für Audiositzung

Audiositzungsänderungen und Formatänderungen werden über WASAPI als Audiositzungsereignisse gemeldet. Ein WASAPI-Client implementiert die [**IAudioSessionEvents-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) und registriert die Implementierung bei WASAPI.

Um Änderungsbenachrichtigungen für Audiositzung zu erhalten, muss der Client die folgenden Aufgaben ausführen:

-   Implementieren Sie die [**IAudioSessionEvents-Schnittstelle,**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) um von WASAPI gesendete Formatänderungsbenachrichtigungen zu verarbeiten.
-   Registrieren Sie [**die IAudioSessionEvents-Implementierung**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) bei WASAPI, indem Sie die [**IAudioSessionControl::RegisterAudioSessionNotification-Methode**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) aufrufen.

[**IAudioSessionEvents-Methoden**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) werden von WASAPI aufgerufen, wenn Audiositzungsänderungen auftreten. Diese Ereignisse werden ausgelöst, wenn sich der Anzeigename, der Symbolpfad, das Volume, der Gruppierungsparameter oder der Zustand der Sitzung ändern.

Um das Streamroutingfeature zu implementieren, muss der Client auf die Benachrichtigung zur Trennung der Sitzungstrennung warten. Wenn eine Audiositzung getrennt wird oder das Format eines Geräts geändert wird, sendet WASAPI die Clientbenachrichtigungen in Form von Rückrufen über [**IAudioSessionEvents::OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected). Mit der Trennungsbenachrichtigung sendet WASAPI auch einen Wert, der angibt, warum die Sitzung getrennt wurde. Dies kann aus verschiedenen Gründen auftreten, z. B. weil das Gerät entfernt wurde, der Server beendet wurde und so weiter. Die vollständige Liste der Gründe finden Sie in der in AudioPolicy.h definierten **AudioSessionDisconnectReason-Enumeration.** Wenn sich das Standardgerät ändert, muss der Client auf die Benachrichtigungen warten (sofern sie noch nicht empfangen wurden), die mit einem **DisconnectReasonDeviceRemoval-Wert** begleitet werden. Als Reaktion auf solche Benachrichtigungen kann der Client den Stream auf dem neuen Standardgerät erneut öffnen.

Da alle diese Vorgänge achron sind, kann die Reihenfolge, in der die Anwendung Benachrichtigungen empfängt, nicht vorhergesagt werden. In der Regel empfängt die Anwendung jedoch den **Wert AudioSessionDisconnect,** bevor die Standardbenachrichtigung zur Geräteänderung angezeigt wird.

### <a name="format-change-notifications"></a>Formatänderungsbenachrichtigungen

Änderungen des Audioformats treten auf, wenn sich das Format des Streams ändert. Dies kann auftreten, wenn der Benutzer  ein neues Format in der Sound-Systemsteuerung auswählt oder das neue Standardgerät ein neues Format unterstützt (z. B. EINE oder bestimmte professionelle Audioschnittstellen mit einer manuellen Anpassung der Abtastrate). Um den Client über diese Arten von Formatänderungen zu benachrichtigen, sendet WASAPI eine Sitzungsbenachrichtigung durch die registrierte Implementierung von [**IAudioSessionEvents::OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) mit dem Trennungsgrund **DisconnectReasonFormatChanged**. Der Client kann die Benachrichtigung verarbeiten, indem er den Stream im neuen Format erneut öffnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur MMDevice-API](mmdevice-api.md)
</dt> <dt>

[Informationen zu WASAPI](wasapi.md)
</dt> <dt>

[Streamrouting](stream-routing.md)
</dt> </dl>

 

 



