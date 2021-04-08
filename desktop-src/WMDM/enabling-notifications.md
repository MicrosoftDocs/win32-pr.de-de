---
title: Aktivieren von Benachrichtigungen
description: Aktivieren von Benachrichtigungen
ms.assetid: b4fc7714-a7d0-409f-a47c-4903bab883cc
keywords:
- Windows Media-Device Manager, Benachrichtigungen
- Device Manager, Benachrichtigungen
- Programmier Handbuch, Benachrichtigungen
- Desktop Anwendungen, Benachrichtigungen
- Erstellen von Windows Media Device Manager-Anwendungen, Benachrichtigungen
- Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618356c9d63d20a8b6b14e6c99072074cfc75073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709696"
---
# <a name="enabling-notifications"></a>Aktivieren von Benachrichtigungen

Windows Media Device Manager deklariert vier Schnittstellen, die von einer Anwendung in einer com-Klasse implementiert werden können, um Ereignis Benachrichtigungen zu empfangen. Diese Schnittstellen sind in zwei Gruppen unterteilt, wie in der folgenden Tabelle dargestellt.



| Schnittstellen                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmdmnotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | Benachrichtigt die Anwendung, wenn Geräte oder Speichermedien verbunden oder getrennt sind.                                                                                         |
| [**Iwmdmprogress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | Ein sehr einfaches Benachrichtigungssystem, um eine Anwendung über den Fortschritt eines beliebigen Ereignisses zu informieren. Die Anwendung muss keine Aktionen als Reaktion auf diese Nachrichten durchführen. |



 

**Iwmdmnotification**

**Iwmdmnotification** benachrichtigt die Anwendung, wenn Plug & Play Geräte mit dem Computer verbunden oder getrennt werden, und wenn Plug & Play Speichermedien (z. b. Flash Karten) vom Gerät eingefügt oder entfernt werden. Diese Benachrichtigungen können dazu beitragen, dass die Anwendung die Benutzeroberfläche aktualisiert, um Änderungen widerzuspiegeln.

Um diese Benachrichtigungen zu erhalten, muss Ihre Anwendung sich registrieren, um Sie über das Platform SDK **IConnectionPointContainer** -und **IConnectionPoint** -Schnittstellen zu empfangen. Die Anwendung sollte sich registrieren, um beim Starten Ereignisse zu empfangen und die Registrierung beim Schließen aufzuheben. Führen Sie diese Schritte aus, um sich für den Empfang dieser Benachrichtigungen zu registrieren

1.  Fragen Sie die Hauptschnittstelle von **iwmtovicemanager** ab, die Sie beim Authentifizieren Ihrer Anwendung für **IConnectionPointContainer** erhalten haben.
2.  Rufen Sie **IConnectionPointContainer:: FindConnectionPoint** auf, um einen Container Verbindungspunkt für die **iwmdmnotification** -Schnittstellen abzurufen.
3.  Registrieren Sie sich, um Ereignisse durch Aufrufen von **IConnectionPoint:: Rat** zu empfangen. Übergeben Sie die Klasse, die **iwmdmnotification** implementiert, und rufen Sie ein Cookie ab, eine eindeutige ID, die den Verbindungspunkt identifiziert. Diese muss gespeichert und später verwendet werden, um die Registrierung für Ereignis Benachrichtigungen aufzuheben.

Der folgende C++-Code veranschaulicht, wie Sie sich für den Empfang von Benachrichtigungen von **iwmdmnotification** registrieren können.


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



Wenn die Anwendung geschlossen wird, müssen Sie die Registrierung bei **IConnectionPoint** aufheben, um anzugeben, dass Benachrichtigungen nicht mehr gesendet werden sollen. Führen Sie die folgenden Schritte aus, um die Registrierung für Benachrichtigungen aufzuheben:

1.  Fragen Sie die Hauptschnittstelle der **iwmdebug** Manager-Schnittstelle für **IConnectionPointContainer** ab.
2.  Sie erhalten einen Verbindungspunkt für die **iwmdmnotification** -Schnittstellen.
3.  Heben Sie die Registrierung Ihrer Anwendung für Ereignis Benachrichtigungen auf, indem Sie **IConnectionPoint:: Unrat** aufrufen und dabei die eindeutige ID übergeben, die bei der Registrierung für den Empfang von Ereignissen empfangen wurde.

Der folgende C++-Code zeigt, wie die Registrierung für **iwmdmnotification** -Ereignisse aufgehoben wird, wenn die Anwendung geschlossen wird.


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



**Verwenden von iwmdmprogress**

Windows Media Device Manager kann Ihre Anwendungs Statusmeldungen senden, wenn bestimmte Aktionen (z. b. Inhalts Übertragung, sichere Uhr-Erfassung und Informationen zu DRM-Dateien) auftreten. Die Anwendung kann diese Nachrichten verwenden, um den Status des Ereignisses zu überwachen oder ein Ereignis abzubrechen. Um diese Schnittstelle zu verwenden, implementieren Sie [**iwmdmprogress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)oder [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3), und übergeben Sie Sie als Parameter an eine Methode, die eine Fortschrittsmeldung akzeptiert. Beachten Sie, dass **IWMDMProgress3** die überlegene Schnittstelle ist, da Sie eine Identifikations-GUID bereitstellt, die angibt, welche Aktion nachverfolgt wird. Die folgenden Anwendungsmethoden akzeptieren eine Fortschritts Schnittstelle (die entsprechenden Dienstanbieter Methoden sollten Benachrichtigungen an eine übermittelte Schnittstelle senden können):

[**Iwmdmstoragecontrol::D Elete**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[**Iwmdmstoragecontrol:: INSERT**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[**Iwmdmstoragecontrol:: Move**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[**Iwmdmstoragecontrol:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[**Iwmdmstoragecontrol:: Rename**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[**Iwmdmstorageglobals:: Initialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[**Iwmdrmdeviceapp:: acquiredevicedata**](iwmdrmdeviceapp-acquiredevicedata.md)

Beispiele für die Übergabe einer Schnittstelle an eine Methode finden Sie in der Dokumentation für diese Methoden. Beispiele für die Implementierung der Rückruf Schnittstellen finden Sie in der Dokumentation zu den Methoden von **iwmdmprogress**, **IWMDMProgress2** oder **IWMDMProgress3**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen einer Windows Media Device Manager-Anwendung**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





