---
title: Aktivieren von Benachrichtigungen
description: Aktivieren von Benachrichtigungen
ms.assetid: b4fc7714-a7d0-409f-a47c-4903bab883cc
keywords:
- Windows Medien Geräte-Manager, Benachrichtigungen
- Geräte-Manager, Benachrichtigungen
- Programmierhandbuch,Benachrichtigungen
- Desktopanwendungen, Benachrichtigungen
- Erstellen von Windows Media Geräte-Manager-Anwendungen, Benachrichtigungen
- Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ab1b71482db78571f141b7042d8abc926b0d79ca2f487ee7dc961396993b9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585063"
---
# <a name="enabling-notifications"></a>Aktivieren von Benachrichtigungen

Windows Media Geräte-Manager deklariert vier Schnittstellen, die eine Anwendung in einer COM-Klasse implementieren kann, um Ereignisbenachrichtigungen zu empfangen. Diese Schnittstellen lassen sich in zwei Gruppen unterteilen, wie in der folgenden Tabelle dargestellt.



| Schnittstellen                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | Benachrichtigt die Anwendung, wenn Geräte oder Speichermedien verbunden oder getrennt sind.                                                                                         |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | Ein sehr einfaches Benachrichtigungssystem, um eine Anwendung über den Fortschritt eines Ereignisses zu informieren. Die Anwendung muss keine Aktionen als Reaktion auf diese Nachrichten ausführen. |



 

**IWMDMNotification**

**IWMDMNotification** alerts the application when Plug and Play devices are connected or disconnected from the computer, as well as when Plug and Play storage media (such as flash cards) are inserted or removed from the device. Diese Benachrichtigungen können der Anwendung helfen, ihre Benutzeroberfläche zu aktualisieren, um Änderungen widerzuspiegeln.

Um diese Benachrichtigungen zu erhalten, muss sich Ihre Anwendung registrieren, um sie mithilfe der Schnittstellen **IConnectionPointContainer** und **IConnectionPoint** des Plattform-SDK zu empfangen. Ihre Anwendung sollte sich registrieren, um Ereignisse zu empfangen, wenn sie gestartet wird, und die Registrierung beim Schließen aufheben. Führen Sie die folgenden Schritte aus, um sich zu registrieren, um diese Benachrichtigungen zu erhalten.

1.  Fragen Sie die **IWMDeviceManager-Hauptschnittstelle** ab, die Sie beim Authentifizieren Ihrer Anwendung für **IConnectionPointContainer** erhalten haben.
2.  Rufen Sie **IConnectionPointContainer::FindConnectionPoint** auf, um einen Containerverbindungspunkt für **IWMDMNotification-Schnittstellen** abzurufen.
3.  Registrieren Sie sich, um Ereignisse zu empfangen, indem **Sie IConnectionPoint::Advise** aufrufen. Übergeben Sie die Klasse, die **IWMDMNotification** implementiert, und rufen Sie ein Cookie ab, eine eindeutige ID, die Ihren Verbindungspunkt identifiziert. Dieser muss gespeichert und später zum Aufheben der Registrierung für Ereignisbenachrichtigungen verwendet werden.

Der folgende C++-Code veranschaulicht, wie Sie sich registrieren können, um Benachrichtigungen von **IWMDMNotification** zu empfangen.


```C++
HRESULT CWMDMController::RegisterForNotifications()
{
    HRESULT hr = S_OK;
    CComPtr<IConnectionPointContainer> pConxnPointCont;
    CComPtr<IConnectionPoint> pIConnPoint;

    // Get the IConnectionPointContainer interface from IWMDeviceManager.
    if (SUCCEEDED (hr = m_IWMDMDeviceMgr->QueryInterface(IID_IConnectionPointContainer, (void**) & pConxnPointCont)))
    {
        // Get a connection point from the container.
        if (SUCCEEDED (hr = pConxnPointCont->FindConnectionPoint(IID_IWMDMNotification, &pIConnPoint)))
        {
            // Add ourselves as a callback handler for the connection point.
            // If we succeeded, indicate that by storing the connection point ID.
            DWORD dwCookie;
            if (SUCCEEDED (hr = pIConnPoint->Advise((IUnknown*)((IWMDMNotification*)this), &dwCookie)))
            {
                m_dwNotificationCookie = dwCookie;
            }
        }
    }

    return hr;
}
```



Wenn Die Anwendung geschlossen wird, müssen Sie die Registrierung bei **IConnectionPoint** aufheben, um anzugeben, dass keine Benachrichtigungen mehr gesendet werden sollen. Führen Sie die folgenden Schritte aus, um die Registrierung für Benachrichtigungen zu aufheben:

1.  Fragen Sie die **IWMDeviceManager-Hauptschnittstelle** nach **IConnectionPointContainer** ab.
2.  Abrufen eines Verbindungspunkts für **IWMDMNotification-Schnittstellen.**
3.  Aufheben der Registrierung Ihrer Anwendung für Ereignisbenachrichtigungen durch Aufrufen von **IConnectionPoint::Unadvise.** Dabei wird die eindeutige ID übergeben, die beim Registrieren für den Empfang von Ereignissen empfangen wurde.

Der folgende C++-Code zeigt, wie die Registrierung für **IWMDMNotification-Ereignisse** aufgehoben wird, wenn Ihre Anwendung geschlossen wird.


```C++
HRESULT CWMDMController::UnregisterForNotifications()
{
    HRESULT hr = S_FALSE;

    // On class initialization, we initialized the handle to -1 as a flag 
    // to indicate we had not yet registered for notifications. If registration 
    // never happened, don't bother to unregister.
    if (-1 != m_dwNotificationCookie)
    {
        CComPtr<IConnectionPointContainer> pConxnPointCont;
        CComPtr<IConnectionPoint> pIConnPoint;

        // Get the connection point container from IWMDeviceManager. 
        if (SUCCEEDED (hr = 
           m_IWMDMDeviceMgr->QueryInterface(IID_IConnectionPointContainer,
           (void**) & pConxnPointCont)))
        {
            // Get a connection point from the container.
            if (SUCCEEDED (hr = pConxnPointCont->FindConnectionPoint(IID_IWMDMNotification, &pIConnPoint)))
            {
                // Remove ourselves as a callback from the connection point.
                // If successful, reset the ID to a flag value.
                if (SUCCEEDED (hr = 
                    pIConnPoint->Unadvise(m_dwNotificationCookie)))
                {
                    m_dwNotificationCookie = -1;
                    hr = S_OK;
                }
            }
        }
    }

    return hr;
}
```



**Verwenden von IWMDMProgress**

Windows Medien-Geräte-Manager können Ihre Anwendungsstatusmeldungen senden, wenn bestimmte Aktionen wie Inhaltsübertragung, sichere Uhrerfassung und das Auftreten von DRM-Dateiinformationen auftreten. Ihre Anwendung kann diese Meldungen verwenden, um den Status des Ereignisses zu überwachen oder ein Ereignis abzubrechen. Um diese Schnittstelle zu verwenden, implementieren [**Sie IWMDMProgress,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress) [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)oder [**IWMDMProgress3,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)und übergeben Sie sie als Parameter an eine Methode, die eine Statusmeldung akzeptiert. Beachten Sie, dass **IWMDMProgress3** die übergeordnete Schnittstelle ist, da sie eine ID-GUID bereitstellt, die angibt, welche Aktion nachverfolgt wird. Die folgenden Anwendungsmethoden akzeptieren eine Statusschnittstelle (die entsprechenden Dienstanbietermethoden sollten in der Lage sein, Benachrichtigungen an eine übermittelte Schnittstelle zu senden):

[**IWMDMStorageControl::D elete**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[**IWMDMStorageControl::Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[**IWMDMStorageControl::Move**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[**IWMDMStorageControl::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[**IWMDMStorageControl::Rename**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[**IWMDMStorageGlobals::Initialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)

Beispiele für die Übergabe einer Schnittstelle an eine Methode finden Sie in der Dokumentation für diese Methoden. Beispiele für die Implementierung der Rückrufschnittstellen finden Sie in der Dokumentation zu den Methoden von **IWMDMProgress,** **IWMDMProgress2** oder **IWMDMProgress3.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen einer Windows Media Geräte-Manager-Anwendung**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





