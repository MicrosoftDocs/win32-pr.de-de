---
title: Iremotedesktopclientevents-Schnittstelle
description: Stellt Methoden bereit, die Informationen vom Server empfangen, die mit Client Steuerungs Ereignissen verknüpft sind.
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7533ee7fea7c522b6129bda06891630c3e5ad15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040611"
---
# <a name="iremotedesktopclientevents-interface"></a><span data-ttu-id="98eb0-105">Iremotedesktopclientevents-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="98eb0-105">IRemoteDesktopClientEvents interface</span></span>

<span data-ttu-id="98eb0-106">Stellt Methoden bereit, die Informationen vom Server empfangen, die mit Client Steuerungs Ereignissen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="98eb0-106">Provides methods that receive information from the server that are related to client control events.</span></span> <span data-ttu-id="98eb0-107">Zu den Ereignissen gehören das Herstellen von Verbindungen und trennen von Anforderungen im Vollbildmodus, das erfolgreiche anmelden und Fehlerbedingungen.</span><span class="sxs-lookup"><span data-stu-id="98eb0-107">Events include connecting and disconnecting, full-screen mode requests, successful logon, and error conditions.</span></span>

## <a name="members"></a><span data-ttu-id="98eb0-108">Member</span><span class="sxs-lookup"><span data-stu-id="98eb0-108">Members</span></span>

<span data-ttu-id="98eb0-109">Die **iremotedesktopclientevents** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="98eb0-109">The **IRemoteDesktopClientEvents** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="98eb0-110">**Iremotedesktopclientevents** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="98eb0-110">**IRemoteDesktopClientEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="98eb0-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="98eb0-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="98eb0-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="98eb0-112">Methods</span></span>

<span data-ttu-id="98eb0-113">Die **iremotedesktopclientevents** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="98eb0-113">The **IRemoteDesktopClientEvents** interface has these methods.</span></span>



| <span data-ttu-id="98eb0-114">Methode</span><span class="sxs-lookup"><span data-stu-id="98eb0-114">Method</span></span>                                                                                      | <span data-ttu-id="98eb0-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98eb0-115">Description</span></span>                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98eb0-116">**Onadminmessagereceived**</span><span class="sxs-lookup"><span data-stu-id="98eb0-116">**OnAdminMessageReceived**</span></span>](iremotedesktopclientevents-onadminmessagereceived.md)         | <span data-ttu-id="98eb0-117">Wird aufgerufen, wenn das Client Steuerelement eine administrative Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="98eb0-117">Called when the client control receives an administrative message.</span></span> <br/>                                                                                      |
| [<span data-ttu-id="98eb0-118">**Onautoreconnected**</span><span class="sxs-lookup"><span data-stu-id="98eb0-118">**OnAutoReconnected**</span></span>](iremotedesktopclientevents-onautoreconnected.md)                   | <span data-ttu-id="98eb0-119">Wird aufgerufen, wenn das Client Steuerelement automatisch eine Verbindung mit einer Remote Sitzung hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="98eb0-119">Called when the client control has automatically reconnected to a remote session.</span></span> <br/>                                                                       |
| [<span data-ttu-id="98eb0-120">**Onautoreconnecting**</span><span class="sxs-lookup"><span data-stu-id="98eb0-120">**OnAutoReconnecting**</span></span>](iremotedesktopclientevents-onautoreconnecting.md)                 | <span data-ttu-id="98eb0-121">Wird aufgerufen, wenn das Client Steuerelement versucht, eine Verbindung mit einer Remote Sitzung automatisch wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="98eb0-121">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span> <br/>                                                  |
| [<span data-ttu-id="98eb0-122">**Onconnected**</span><span class="sxs-lookup"><span data-stu-id="98eb0-122">**OnConnected**</span></span>](iremotedesktopclientevents-onconnected.md)                               | <span data-ttu-id="98eb0-123">Wird aufgerufen, wenn das Client Steuerelement eine Verbindung mit einer Remote Sitzung hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="98eb0-123">Called when the client control has connected to a remote session.</span></span><br/>                                                                                        |
| [<span data-ttu-id="98eb0-124">**Verbindung wird hergestellt**</span><span class="sxs-lookup"><span data-stu-id="98eb0-124">**OnConnecting**</span></span>](iremotedesktopclientevents-onconnecting.md)                             | <span data-ttu-id="98eb0-125">Wird aufgerufen, wenn das Client Steuerelement versucht, eine Verbindung mit einer Remote Sitzung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="98eb0-125">Called when the client control attempts to establish a connection to a remote session.</span></span> <br/>                                                                  |
| [<span data-ttu-id="98eb0-126">**Ondialogverworfen**</span><span class="sxs-lookup"><span data-stu-id="98eb0-126">**OnDialogDismissed**</span></span>](iremotedesktopclientevents-ondialogdismissed.md)                   | <span data-ttu-id="98eb0-127">Wird aufgerufen, nachdem ein vom Client Steuerelement angezeigtes Dialogfeld verworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="98eb0-127">Called after a dialog box displayed by the client control is dismissed.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="98eb0-128">**Ondialogdisplay**</span><span class="sxs-lookup"><span data-stu-id="98eb0-128">**OnDialogDisplaying**</span></span>](iremotedesktopclientevents-ondialogdisplaying.md)                 | <span data-ttu-id="98eb0-129">Wird aufgerufen, bevor das-Steuerelement ein Dialogfeld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="98eb0-129">Called before the control displays a dialog box.</span></span> <br/>                                                                                                        |
| [<span data-ttu-id="98eb0-130">**Nicht getrennt**</span><span class="sxs-lookup"><span data-stu-id="98eb0-130">**OnDisconnected**</span></span>](iremotedesktopclientevents-ondisconnected.md)                         | <span data-ttu-id="98eb0-131">Wird aufgerufen, wenn das Client Steuerelement von einer Remote Sitzung getrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="98eb0-131">Called when the client control has been disconnected from a remote session.</span></span> <br/>                                                                             |
| [<span data-ttu-id="98eb0-132">**Onkeycombinationpressed**</span><span class="sxs-lookup"><span data-stu-id="98eb0-132">**OnKeyCombinationPressed**</span></span>](iremotedesktopclientevents-onkeycombinationpressed.md)       | <span data-ttu-id="98eb0-133">Wird aufgerufen, wenn in der Remote Sitzung Sondertasten Kombinationen gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="98eb0-133">Called when special key combinations are pressed in the remote session.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="98eb0-134">**Onloginabgeschlossene**</span><span class="sxs-lookup"><span data-stu-id="98eb0-134">**OnLoginCompleted**</span></span>](iremotedesktopclientevents-onlogincompleted.md)                     | <span data-ttu-id="98eb0-135">Wird aufgerufen, wenn sich das Client Steuerelement erfolgreich bei einer Remote Sitzung angemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="98eb0-135">Called when the client control has successfully logged on to a remote session.</span></span> <br/>                                                                          |
| [<span data-ttu-id="98eb0-136">**Onnetworkstatuschge**</span><span class="sxs-lookup"><span data-stu-id="98eb0-136">**OnNetworkStatusChanged**</span></span>](iremotedesktopclientevents-onnetworkstatuschanged.md)         | <span data-ttu-id="98eb0-137">Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat.</span><span class="sxs-lookup"><span data-stu-id="98eb0-137">Called when the network status has changed.</span></span> <br/>                                                                                                             |
| [<span data-ttu-id="98eb0-138">**"Onremotedesktopsizechanged"**</span><span class="sxs-lookup"><span data-stu-id="98eb0-138">**OnRemoteDesktopSizeChanged**</span></span>](iremotedesktopclientevents-onremotedesktopsizechanged.md) | <span data-ttu-id="98eb0-139">Wird aufgerufen, wenn sich die Remote Desktop Größe geändert hat.</span><span class="sxs-lookup"><span data-stu-id="98eb0-139">Called when the remote desktop size has changed.</span></span> <br/>                                                                                                        |
| [<span data-ttu-id="98eb0-140">**Onstatuschge**</span><span class="sxs-lookup"><span data-stu-id="98eb0-140">**OnStatusChanged**</span></span>](iremotedesktopclientevents-onstatuschanged.md)                       | <span data-ttu-id="98eb0-141">Wird aufgerufen, wenn das Client Steuerelement seinen Status aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="98eb0-141">Called when the client control has updated its status.</span></span> <br/>                                                                                                  |
| [<span data-ttu-id="98eb0-142">**Ontouchpointercurrsorverschohe**</span><span class="sxs-lookup"><span data-stu-id="98eb0-142">**OnTouchPointerCursorMoved**</span></span>](iremotedesktopclientevents-ontouchpointercursormoved.md)   | <span data-ttu-id="98eb0-143">Wird aufgerufen, wenn der Fingerabdruck Cursor verschoben wurde und die [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) -Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="98eb0-143">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="98eb0-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98eb0-144">Requirements</span></span>



| <span data-ttu-id="98eb0-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98eb0-145">Requirement</span></span> | <span data-ttu-id="98eb0-146">Wert</span><span class="sxs-lookup"><span data-stu-id="98eb0-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98eb0-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98eb0-147">Minimum supported client</span></span><br/> | <span data-ttu-id="98eb0-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="98eb0-148">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="98eb0-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98eb0-149">Minimum supported server</span></span><br/> | <span data-ttu-id="98eb0-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="98eb0-150">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="98eb0-151">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="98eb0-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="98eb0-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98eb0-152"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="98eb0-153">DLL</span><span class="sxs-lookup"><span data-stu-id="98eb0-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98eb0-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98eb0-154"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="98eb0-155">CLSID</span><span class="sxs-lookup"><span data-stu-id="98eb0-155">CLSID</span></span><br/>                    | <span data-ttu-id="98eb0-156">CLSID \_ Remotedesktopclient ist als EAB16C5D-EED1-4E95-868B-0FBA1B42C092 definiert.</span><span class="sxs-lookup"><span data-stu-id="98eb0-156">CLSID\_RemoteDesktopClient is defined as EAB16C5D-EED1-4E95-868B-0FBA1B42C092</span></span><br/>       |
| <span data-ttu-id="98eb0-157">IID</span><span class="sxs-lookup"><span data-stu-id="98eb0-157">IID</span></span><br/>                      | <span data-ttu-id="98eb0-158">Diid \_ iremotedesktopclientevents ist als 079863b7-6d47-4105-8bfe-0cdcb360e67d definiert.</span><span class="sxs-lookup"><span data-stu-id="98eb0-158">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98eb0-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98eb0-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98eb0-160">Remotedesktop ActiveX-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="98eb0-160">Remote Desktop ActiveX control reference</span></span>](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

