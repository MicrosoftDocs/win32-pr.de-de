---
description: In Windows 7 implementieren allgemeine Plattform-APIs, die kernaudio-APIs verwenden, wie Media Foundation-, DirectSound-und Wave-APIs, das Streaming-Routing Feature, indem Sie den Datenstrom Wechsel von einem vorhandenen Gerät zu einem neuen standardaudioendpunkt verarbeiten.
ms.assetid: caf831bb-b8de-467f-bdb4-f9f8991dc7a8
title: Relevante Benachrichtigungen für das Datenstrom Routing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3d253ce2ec5d6e3bef025a33233a9d377ca44b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126893"
---
# <a name="relevant-notifications-for-stream-routing"></a>Relevante Benachrichtigungen für das Datenstrom Routing

In Windows 7 implementieren allgemeine Plattform-APIs, die kernaudio-APIs verwenden, wie Media Foundation-, DirectSound-und Wave-APIs, das Streaming-Routing Feature, indem Sie den Datenstrom Wechsel von einem vorhandenen Gerät zu einem neuen standardaudioendpunkt verarbeiten. Medienanwendungen, die diese APIs verwenden, verwenden das Datenstrom-Routing Verhalten ohne Änderungen an der Quelle. Direkte WASAPI-Clients können die Benachrichtigungen verwenden, die von den kernaudiokomponenten gesendet werden, und die streamweiterleitungs Funktion implementieren.

Zum Implementieren der streamweiterleitungs-Funktion muss ein Client auf zwei Arten von Ereignissen lauschen: Geräte Änderungs Benachrichtigungen und Sitzungs Trennungs Benachrichtigungen. In der Implementierung der APIs auf hoher Ebene werden diese Ereignisse für Standardgeräte Endpunkte gesendet, die durch den Aufruf von [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)erstellt wurden. Weitere Informationen finden Sie unter [Getting the Device Endpoint for Stream Routing](getting-the-default-device-endpoint-for-stream-routing.md).

Die mmdeviceapi der kernaudiokomponente übermittelt Benachrichtigungs Rückrufe, wenn Audiogeräte hinzugefügt, entfernt oder geändert werden. Die Änderungen an der Format-und Audiositzung werden über WASAPI als Ereignisse gemeldet.

## <a name="device-change-notifications"></a>Geräte Änderungs Benachrichtigungen

Mmdeviceapi löst Ereignisse aus, wenn Audiogeräte hinzugefügt, entfernt oder geändert werden. Wenn der Client Stream-Routing Funktionen bereitstellen soll, muss er die [**immnotificationclient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) -Schnittstelle implementieren und seine Implementierung bei mmdeviceapi registrieren.

Um Benachrichtigungen über Geräteänderungen zu erhalten, muss der Client die folgenden Aufgaben ausführen:

-   Implementieren Sie die [**immnotificationclient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) -Schnittstelle zum Verarbeiten von Benachrichtigungen über Geräteänderungen, die von mmdeviceapi gesendet werden.
-   Registrieren Sie die [**immnotificationclient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) -Implementierung mit mmdeviceapi, indem Sie die [**immdeviceenumerator:: registerendpointnotificationcallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) -Methode aufrufen.

Nachdem die Implementierung dieser Schnittstellen durch den Client registriert wurde, empfängt der Client Benachrichtigungen in Form von Rückrufe über die Methoden dieser Schnittstellen. [**Immnotificationclient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) -Methoden werden von mmdeviceapi aufgerufen, wenn Sie Ereignisse auf Endpunkt Ebene auslöst (Änderungen am Endpunkt Zustand, neue Endpunkt-Ankünfte, Endpunkt Löschungen, standardend Punkt Änderungen und Änderungen an Endpunkt Eigenschaften).

Wenn der Client Datenstrom Routing für das Standardgerät bereitstellen möchte, muss der Client das Verhalten der Geräte Änderung implementieren, wenn er die Benachrichtigung über den " [**immnotificationclient:: ondefaultdevicechanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) "-Rückruf empfängt.

## <a name="audio-session-change-notifications"></a>Benachrichtigungen zu Änderungen an audiositzungen

Änderungen an der Audiositzung und Formatänderungen werden als audiositzungsereignisse über WASAPI gemeldet. Ein WASAPI-Client implementiert die [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle und registriert die Implementierung bei WASAPI.

Der Client muss die folgenden Aufgaben ausführen, um Benachrichtigungen über Änderungen der Audiositzung zu erhalten:

-   Implementieren Sie die [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle zum Verarbeiten von Format Änderungs Benachrichtigungen, die von WASAPI gesendet werden.
-   Registrieren Sie die [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Implementierung mit WASAPI, indem Sie die [**iaudiosessioncontrol:: registeraudiosessionnotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) -Methode aufrufen.

[**Iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Methoden werden von WASAPI aufgerufen, wenn Änderungen an der Audiositzung auftreten. Diese Ereignisse werden ausgelöst, wenn sich der Anzeige Name, der Symbol Pfad, das Volume, der Gruppierungs Parameter oder der Status der Sitzung ändert.

Zum Implementieren der streamweiterleitungs-Funktion muss der Client auf die Benachrichtigung Sitzungs getrennt warten. Wenn eine Audiositzung getrennt oder das Format eines Geräts geändert wird, sendet WASAPI die Client Benachrichtigungen in Form von Rückrufen über [**iaudiosessionevents:: onsessiongetrennte**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected). Mit der disverbindungsbenachrichtigung sendet WASAPI außerdem einen Wert, der angibt, warum die Sitzung getrennt wurde. Dies kann verschiedene Ursachen haben, z. b. wenn das Gerät entfernt wurde, der Server angehalten wurde und so weiter. Eine umfassende Liste der Gründe finden Sie unter der in audiopolicy. h definierten Enumeration **audiosessiondisconnecverrat** . Wenn das Standardgerät geändert wird, muss der Client auf die Benachrichtigungen warten (sofern noch nicht geschehen), die mit einem **disconnecwerondeviceremoval** -Wert verknüpft sind. Als Reaktion auf solche Benachrichtigungen kann der Client den Datenstrom auf dem neuen Standardgerät erneut öffnen.

Da alle diese Vorgänge asynchron sind, kann die Reihenfolge, in der die Anwendung Benachrichtigungen empfängt, nicht vorhergesagt werden. In der Regel erhält die Anwendung jedoch den Wert **audiosessiondisconnect** vor der Standard Benachrichtigung für Geräteänderungen.

### <a name="format-change-notifications"></a>Formatieren von Änderungs Benachrichtigungen

Audioformatänderungen treten auf, wenn das Format des Streams geändert wird. Dies kann vorkommen, **Wenn der Benutzer in der System** Steuerung ein neues Format auswählt oder wenn das neue Standardgerät ein neues Format unterstützt (z. b. "HDMI" oder bestimmte professionelle Audioschnittstellen mit manueller Anpassung der Stichprobenrate). Um den Client über diese Art von Formatänderungen zu benachrichtigen, sendet WASAPI eine Sitzungs Benachrichtigung durch die registrierte Implementierung von [**iaudiosessionevents:: onsessiondisconnect**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) mit dem **Trennungsgrund von disconnecationonformatchanged**. Der Client kann die Benachrichtigung verarbeiten, indem er den Stream im neuen Format erneut öffnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über die mmdevice-API](mmdevice-api.md)
</dt> <dt>

[Informationen zu WASAPI](wasapi.md)
</dt> <dt>

[Streamrouting](stream-routing.md)
</dt> </dl>

 

 



