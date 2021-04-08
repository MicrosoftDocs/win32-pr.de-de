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
# <a name="enabling-notifications"></a><span data-ttu-id="1ce13-109">Aktivieren von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="1ce13-109">Enabling Notifications</span></span>

<span data-ttu-id="1ce13-110">Windows Media Device Manager deklariert vier Schnittstellen, die von einer Anwendung in einer com-Klasse implementiert werden können, um Ereignis Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="1ce13-110">Windows Media Device Manager declares four interfaces that an application can implement in a COM class to receive event notifications.</span></span> <span data-ttu-id="1ce13-111">Diese Schnittstellen sind in zwei Gruppen unterteilt, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1ce13-111">These interfaces fall into two groups, as shown in the following table.</span></span>



| <span data-ttu-id="1ce13-112">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1ce13-112">Interfaces</span></span>                                                                                                                                                | <span data-ttu-id="1ce13-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ce13-113">Description</span></span>                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ce13-114">**Iwmdmnotification**</span><span class="sxs-lookup"><span data-stu-id="1ce13-114">**IWMDMNotification**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | <span data-ttu-id="1ce13-115">Benachrichtigt die Anwendung, wenn Geräte oder Speichermedien verbunden oder getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="1ce13-115">Notifies the application when devices or storage media are connected or disconnected.</span></span>                                                                                         |
| [<span data-ttu-id="1ce13-116">**Iwmdmprogress**</span><span class="sxs-lookup"><span data-stu-id="1ce13-116">**IWMDMProgress**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [<span data-ttu-id="1ce13-117">**IWMDMProgress2**</span><span class="sxs-lookup"><span data-stu-id="1ce13-117">**IWMDMProgress2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [<span data-ttu-id="1ce13-118">**IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="1ce13-118">**IWMDMProgress3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | <span data-ttu-id="1ce13-119">Ein sehr einfaches Benachrichtigungssystem, um eine Anwendung über den Fortschritt eines beliebigen Ereignisses zu informieren.</span><span class="sxs-lookup"><span data-stu-id="1ce13-119">A very simple notification system to alert an application about the progress of any event.</span></span> <span data-ttu-id="1ce13-120">Die Anwendung muss keine Aktionen als Reaktion auf diese Nachrichten durchführen.</span><span class="sxs-lookup"><span data-stu-id="1ce13-120">The application is not required to take any actions in response to these messages.</span></span> |



 

<span data-ttu-id="1ce13-121">**Iwmdmnotification**</span><span class="sxs-lookup"><span data-stu-id="1ce13-121">**IWMDMNotification**</span></span>

<span data-ttu-id="1ce13-122">**Iwmdmnotification** benachrichtigt die Anwendung, wenn Plug & Play Geräte mit dem Computer verbunden oder getrennt werden, und wenn Plug & Play Speichermedien (z. b. Flash Karten) vom Gerät eingefügt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1ce13-122">**IWMDMNotification** alerts the application when Plug and Play devices are connected or disconnected from the computer, as well as when Plug and Play storage media (such as flash cards) are inserted or removed from the device.</span></span> <span data-ttu-id="1ce13-123">Diese Benachrichtigungen können dazu beitragen, dass die Anwendung die Benutzeroberfläche aktualisiert, um Änderungen widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="1ce13-123">These notifications can help the application update its user interface to reflect changes.</span></span>

<span data-ttu-id="1ce13-124">Um diese Benachrichtigungen zu erhalten, muss Ihre Anwendung sich registrieren, um Sie über das Platform SDK **IConnectionPointContainer** -und **IConnectionPoint** -Schnittstellen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="1ce13-124">In order to receive these notifications, your application must register to receive them using the Platform SDK **IConnectionPointContainer** and **IConnectionPoint** interfaces.</span></span> <span data-ttu-id="1ce13-125">Die Anwendung sollte sich registrieren, um beim Starten Ereignisse zu empfangen und die Registrierung beim Schließen aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="1ce13-125">Your application should register to receive events when it starts up, and unregister when it closes.</span></span> <span data-ttu-id="1ce13-126">Führen Sie diese Schritte aus, um sich für den Empfang dieser Benachrichtigungen zu registrieren</span><span class="sxs-lookup"><span data-stu-id="1ce13-126">Follow these steps to register to receive these notifications.</span></span>

1.  <span data-ttu-id="1ce13-127">Fragen Sie die Hauptschnittstelle von **iwmtovicemanager** ab, die Sie beim Authentifizieren Ihrer Anwendung für **IConnectionPointContainer** erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="1ce13-127">Query the main **IWMDeviceManager** interface you received when you authenticated your application for **IConnectionPointContainer**.</span></span>
2.  <span data-ttu-id="1ce13-128">Rufen Sie **IConnectionPointContainer:: FindConnectionPoint** auf, um einen Container Verbindungspunkt für die **iwmdmnotification** -Schnittstellen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1ce13-128">Call **IConnectionPointContainer::FindConnectionPoint** to retrieve a container connection point for **IWMDMNotification** interfaces.</span></span>
3.  <span data-ttu-id="1ce13-129">Registrieren Sie sich, um Ereignisse durch Aufrufen von **IConnectionPoint:: Rat** zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="1ce13-129">Register to receive events by calling **IConnectionPoint::Advise**.</span></span> <span data-ttu-id="1ce13-130">Übergeben Sie die Klasse, die **iwmdmnotification** implementiert, und rufen Sie ein Cookie ab, eine eindeutige ID, die den Verbindungspunkt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1ce13-130">Pass in the class that implements **IWMDMNotification**, and retrieve a cookie, a unique ID that identifies your connection point.</span></span> <span data-ttu-id="1ce13-131">Diese muss gespeichert und später verwendet werden, um die Registrierung für Ereignis Benachrichtigungen aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="1ce13-131">This must be stored, and used later to unregister for event notifications.</span></span>

<span data-ttu-id="1ce13-132">Der folgende C++-Code veranschaulicht, wie Sie sich für den Empfang von Benachrichtigungen von **iwmdmnotification** registrieren können.</span><span class="sxs-lookup"><span data-stu-id="1ce13-132">The following C++ code demonstrates how you can register to receive notifications from **IWMDMNotification**.</span></span>


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



<span data-ttu-id="1ce13-133">Wenn die Anwendung geschlossen wird, müssen Sie die Registrierung bei **IConnectionPoint** aufheben, um anzugeben, dass Benachrichtigungen nicht mehr gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1ce13-133">When your application closes, you must unregister with **IConnectionPoint** to indicate that it should no longer send you notifications.</span></span> <span data-ttu-id="1ce13-134">Führen Sie die folgenden Schritte aus, um die Registrierung für Benachrichtigungen aufzuheben:</span><span class="sxs-lookup"><span data-stu-id="1ce13-134">Follow these steps to unregister for notifications:</span></span>

1.  <span data-ttu-id="1ce13-135">Fragen Sie die Hauptschnittstelle der **iwmdebug** Manager-Schnittstelle für **IConnectionPointContainer** ab.</span><span class="sxs-lookup"><span data-stu-id="1ce13-135">Query the main **IWMDeviceManager** interface for **IConnectionPointContainer**.</span></span>
2.  <span data-ttu-id="1ce13-136">Sie erhalten einen Verbindungspunkt für die **iwmdmnotification** -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="1ce13-136">Get a connection point for **IWMDMNotification** interfaces.</span></span>
3.  <span data-ttu-id="1ce13-137">Heben Sie die Registrierung Ihrer Anwendung für Ereignis Benachrichtigungen auf, indem Sie **IConnectionPoint:: Unrat** aufrufen und dabei die eindeutige ID übergeben, die bei der Registrierung für den Empfang von Ereignissen empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="1ce13-137">Unregister your application for event notifications by calling **IConnectionPoint::Unadvise**, passing in the unique ID received when you registered to receive events.</span></span>

<span data-ttu-id="1ce13-138">Der folgende C++-Code zeigt, wie die Registrierung für **iwmdmnotification** -Ereignisse aufgehoben wird, wenn die Anwendung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="1ce13-138">The following C++ code shows how to unregister for **IWMDMNotification** events when your application closes.</span></span>


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



<span data-ttu-id="1ce13-139">**Verwenden von iwmdmprogress**</span><span class="sxs-lookup"><span data-stu-id="1ce13-139">**Using IWMDMProgress**</span></span>

<span data-ttu-id="1ce13-140">Windows Media Device Manager kann Ihre Anwendungs Statusmeldungen senden, wenn bestimmte Aktionen (z. b. Inhalts Übertragung, sichere Uhr-Erfassung und Informationen zu DRM-Dateien) auftreten.</span><span class="sxs-lookup"><span data-stu-id="1ce13-140">Windows Media Device Manager can send your application status messages when specific actions, such as content transfer, secure clock acquisition, and encountering DRM file information, occur.</span></span> <span data-ttu-id="1ce13-141">Die Anwendung kann diese Nachrichten verwenden, um den Status des Ereignisses zu überwachen oder ein Ereignis abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="1ce13-141">Your application can use these messages to monitor the status of the event or cancel an event.</span></span> <span data-ttu-id="1ce13-142">Um diese Schnittstelle zu verwenden, implementieren Sie [**iwmdmprogress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)oder [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3), und übergeben Sie Sie als Parameter an eine Methode, die eine Fortschrittsmeldung akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="1ce13-142">To use this interface, implement [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2), or [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3), and pass it in as a parameter to a method that will accept a progress message.</span></span> <span data-ttu-id="1ce13-143">Beachten Sie, dass **IWMDMProgress3** die überlegene Schnittstelle ist, da Sie eine Identifikations-GUID bereitstellt, die angibt, welche Aktion nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="1ce13-143">Note that **IWMDMProgress3** is the superior interface because it provides an identification GUID that specifies what action is being tracked.</span></span> <span data-ttu-id="1ce13-144">Die folgenden Anwendungsmethoden akzeptieren eine Fortschritts Schnittstelle (die entsprechenden Dienstanbieter Methoden sollten Benachrichtigungen an eine übermittelte Schnittstelle senden können):</span><span class="sxs-lookup"><span data-stu-id="1ce13-144">The following application methods accept a progress interface (the corresponding service provider methods should be able to send notifications to a submitted interface):</span></span>

[<span data-ttu-id="1ce13-145">**Iwmdmstoragecontrol::D Elete**</span><span class="sxs-lookup"><span data-stu-id="1ce13-145">**IWMDMStorageControl::Delete**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[<span data-ttu-id="1ce13-146">**Iwmdmstoragecontrol:: INSERT**</span><span class="sxs-lookup"><span data-stu-id="1ce13-146">**IWMDMStorageControl::Insert**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[<span data-ttu-id="1ce13-147">**Iwmdmstoragecontrol:: Move**</span><span class="sxs-lookup"><span data-stu-id="1ce13-147">**IWMDMStorageControl::Move**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[<span data-ttu-id="1ce13-148">**Iwmdmstoragecontrol:: Read**</span><span class="sxs-lookup"><span data-stu-id="1ce13-148">**IWMDMStorageControl::Read**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[<span data-ttu-id="1ce13-149">**Iwmdmstoragecontrol:: Rename**</span><span class="sxs-lookup"><span data-stu-id="1ce13-149">**IWMDMStorageControl::Rename**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[<span data-ttu-id="1ce13-150">**IWMDMStorageControl2::Insert2**</span><span class="sxs-lookup"><span data-stu-id="1ce13-150">**IWMDMStorageControl2::Insert2**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[<span data-ttu-id="1ce13-151">**IWMDMStorageControl3::Insert3**</span><span class="sxs-lookup"><span data-stu-id="1ce13-151">**IWMDMStorageControl3::Insert3**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[<span data-ttu-id="1ce13-152">**Iwmdmstorageglobals:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="1ce13-152">**IWMDMStorageGlobals::Initialize**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[<span data-ttu-id="1ce13-153">**Iwmdrmdeviceapp:: acquiredevicedata**</span><span class="sxs-lookup"><span data-stu-id="1ce13-153">**IWMDRMDeviceApp::AcquireDeviceData**</span></span>](iwmdrmdeviceapp-acquiredevicedata.md)

<span data-ttu-id="1ce13-154">Beispiele für die Übergabe einer Schnittstelle an eine Methode finden Sie in der Dokumentation für diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1ce13-154">Examples of passing an interface into a method are given in the documentation for these methods.</span></span> <span data-ttu-id="1ce13-155">Beispiele für die Implementierung der Rückruf Schnittstellen finden Sie in der Dokumentation zu den Methoden von **iwmdmprogress**, **IWMDMProgress2** oder **IWMDMProgress3**.</span><span class="sxs-lookup"><span data-stu-id="1ce13-155">For examples of implementing the callback interfaces, see the documentation for the methods of **IWMDMProgress**, **IWMDMProgress2**, or **IWMDMProgress3**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ce13-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ce13-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ce13-157">**Erstellen einer Windows Media Device Manager-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="1ce13-157">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





