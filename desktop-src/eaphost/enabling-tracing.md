---
title: Aktivieren der EAPHost-Ablauf Verfolgung
description: Kann Benutzer bei der Suche nach den Hauptursachen von Problemen unterstützen, die während des EAP-Authentifizierungs Vorgangs auftreten. Zu den Debuginformationen können API-Aufrufe ausgeführt werden, interne Funktionsaufrufe durchgeführt und Zustandsübergänge ausgeführt werden.
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdee8a5516b218e51f0151e1964885789560d82
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104039882"
---
# <a name="enabling-eaphost-tracing"></a><span data-ttu-id="344ae-104">Aktivieren der EAPHost-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="344ae-104">Enabling EAPHost Tracing</span></span>

<span data-ttu-id="344ae-105">Ablauf Verfolgungs Protokolle mit Debuginformationen können Benutzer bei der Suche nach den Hauptursachen von Problemen unterstützen, die während des EAP-Authentifizierungs Vorgangs auftreten.</span><span class="sxs-lookup"><span data-stu-id="344ae-105">Trace logs containing debugging information can assist users in finding the root causes of issues that occur during the EAP authentication process.</span></span> <span data-ttu-id="344ae-106">Zu den Debuginformationen können API-Aufrufe ausgeführt werden, interne Funktionsaufrufe durchgeführt und Zustandsübergänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="344ae-106">The debugging information can include API calls performed, internal function calls performed, and state transitions performed.</span></span>

<span data-ttu-id="344ae-107">Die Ablauf Verfolgung kann sowohl auf der Clientseite als auch auf der Authenticator-Seite aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="344ae-107">Tracing can be enabled on both the client side and the authenticator side.</span></span> <span data-ttu-id="344ae-108">Die Ablauf Verfolgung kann auch für Aufrufe der APIs für den [Routing-und RAS-Dienst (RRAS)](/windows/desktop/RRAS/routing-start-page) aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="344ae-108">Tracing can also be enabled for calls to the [Routing and Remote Access Service (RRAS)](/windows/desktop/RRAS/routing-start-page) APIs.</span></span> <span data-ttu-id="344ae-109">Weitere Informationen finden Sie unter Ablauf [Verfolgung für den Routing-und RAS-Dienst](#tracing-on-the-routing-and-remote-access-service).</span><span class="sxs-lookup"><span data-stu-id="344ae-109">For more information, see [Tracing on the Routing and Remote Access Service](#tracing-on-the-routing-and-remote-access-service).</span></span>

> [!Note]  
> <span data-ttu-id="344ae-110">Ablauf Verfolgungs Protokolle sind nur in englischer Sprache verfügbar.</span><span class="sxs-lookup"><span data-stu-id="344ae-110">Trace logs are available in English only.</span></span>

 

<span data-ttu-id="344ae-111">Wenn die EAPHost-Ablauf Verfolgung aktiviert ist, werden die Protokollierungs Informationen in einer ETL-Datei an einem vom Benutzer angegebenen Speicherort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="344ae-111">When EAPHost tracing is enabled, logging information is stored in an .etl file in a user-specified location.</span></span> <span data-ttu-id="344ae-112">Wenn während der EAP-Authentifizierung Fehler auftreten, generiert die Ablauf Verfolgung eine ETL-Datei, die für die Fehlerursachen Analyse an Developer Support Microsoft gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="344ae-112">If errors occur during EAP authentication, tracing generates an .etl file that can be sent to Microsoft Developer Support for root cause analysis.</span></span> <span data-ttu-id="344ae-113">Partner, die Zugriff auf Microsoft Windows Build-Freigaben,-Symbole und traceformat-Dateien haben, können die ETL-Dateien mithilfe des **tracerpt** -Tools in eine einfache Textdatei konvertieren.</span><span class="sxs-lookup"><span data-stu-id="344ae-113">Partners that have access to Microsoft windows build shares, symbols, and traceformat files can convert the .etl files into a plain text file using the **tracerpt** tool.</span></span>

<span data-ttu-id="344ae-114">NPS-Fehler (Network Policy Server, Netzwerk Richtlinien Server) werden in den EAPHost-Protokollen nicht erfasst.</span><span class="sxs-lookup"><span data-stu-id="344ae-114">Network policy server (NPS) failures are not captured in the EAPHost logs.</span></span> <span data-ttu-id="344ae-115">Wenn Sie versuchen, einen NPS-Fehler zu beheben, sehen Sie sich den iassam an. Log und [iasnap. Protokoll](https://go.microsoft.com/fwlink/p/?linkid=84108) Dateien.</span><span class="sxs-lookup"><span data-stu-id="344ae-115">If you are trying to troubleshoot a NPS failure, view the IASSAM.LOG and [IASNAP.LOG](https://go.microsoft.com/fwlink/p/?linkid=84108) files.</span></span>

## <a name="tracing-on-the-client"></a><span data-ttu-id="344ae-116">Ablauf Verfolgung auf dem Client</span><span class="sxs-lookup"><span data-stu-id="344ae-116">Tracing on the Client</span></span>

<span data-ttu-id="344ae-117">So aktivieren Sie die Ablauf Verfolgung auf der Clientseite:</span><span class="sxs-lookup"><span data-stu-id="344ae-117">To enable tracing on the client side:</span></span>

1.  <span data-ttu-id="344ae-118">Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten.</span><span class="sxs-lookup"><span data-stu-id="344ae-118">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="344ae-119">Führen Sie den folgenden Befehl aus: **logman** **Start Trace** **eaphostpeer** **-o** **. \\ Eaphostpeer. ETL** **-p** **{5f31090b-d990-4e91-b16d-46121d0255aa} 0x4000ffff 0** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="344ae-119">Run the following command: **logman** **start trace** **EapHostPeer** **-o** **.\\EapHostPeer.etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ets**</span></span>
3.  <span data-ttu-id="344ae-120">Reproduzieren Sie das Szenario, das Sie nachverfolgen möchten.</span><span class="sxs-lookup"><span data-stu-id="344ae-120">Reproduce the scenario that you want to trace.</span></span>
4.  <span data-ttu-id="344ae-121">Führen Sie den folgenden Befehl aus: **logman** **stoppt** **eaphostpeer** **-ETS** .</span><span class="sxs-lookup"><span data-stu-id="344ae-121">Run the following command: **logman** **stop** **EapHostPeer** **-ets**</span></span>
5.  <span data-ttu-id="344ae-122">Konvertieren Sie die ETL-Datei mithilfe des folgenden Befehls in Text: **tracerpt eaphostpeer. ETL** **– PDB** **&lt; PDBPATH &gt;** **-tp** **&lt; tracemessagefilesdirector &gt; ypath** **-o** **EapHostPeer.txt**</span><span class="sxs-lookup"><span data-stu-id="344ae-122">Convert the etl file into text using the following command: **tracerpt EapHostPeer.etl** **–pdb** **&lt;pdbpath&gt;** **-tp** **&lt;tracemessagefilesdirectorypath&gt;** **-o** **EapHostPeer.txt**</span></span>
    > [!Note]  
    > <span data-ttu-id="344ae-123">Wenn Sie keinen Zugriff auf das tracerpt-Tool haben, vermeiden Sie den letzten Schritt, und senden Sie die ETL-Datei an Microsoft Developer Support.</span><span class="sxs-lookup"><span data-stu-id="344ae-123">If you do not have access to the tracerpt tool, avoid the last step and send the .etl file to Microsoft Developer Support.</span></span>

     

## <a name="tracing-on-the-authenticator"></a><span data-ttu-id="344ae-124">Ablauf Verfolgung für den Authentifikator</span><span class="sxs-lookup"><span data-stu-id="344ae-124">Tracing on the Authenticator</span></span>

<span data-ttu-id="344ae-125">So aktivieren Sie die Ablauf Verfolgung auf der Authentifikator-Seite:</span><span class="sxs-lookup"><span data-stu-id="344ae-125">To enable tracing on the authenticator side:</span></span>

1.  <span data-ttu-id="344ae-126">Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten.</span><span class="sxs-lookup"><span data-stu-id="344ae-126">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="344ae-127">Führen Sie den folgenden Befehl aus: **logman** **Start Trace** **eaphostauthr** **-o** **. \\ Eaphostauthr. ETL** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="344ae-127">Run the following command: **logman** **start trace** **EapHostAuthr** **-o** **.\\EapHostAuthr.etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ets**</span></span>
3.  <span data-ttu-id="344ae-128">Reproduzieren Sie das Szenario, das Sie nachverfolgen möchten.</span><span class="sxs-lookup"><span data-stu-id="344ae-128">Reproduce the scenario that you want to trace.</span></span>
4.  <span data-ttu-id="344ae-129">Führen Sie den folgenden Befehl aus: **logman** **stoppt** **eaphostauthr** **-ETS** .</span><span class="sxs-lookup"><span data-stu-id="344ae-129">Run the following command: **logman** **stop** **EapHostAuthr** **-ets**</span></span>
5.  <span data-ttu-id="344ae-130">Konvertieren Sie die ETL-Datei mithilfe des folgenden Befehls in Text: **tracerpt eaphostauthr. ETL** **– PDB** **&lt; PDBPATH &gt;** **-tp** **&lt; tracemessagefilesdirecterypath &gt;** **-o** **EapHostAuthr.txt**</span><span class="sxs-lookup"><span data-stu-id="344ae-130">Convert the etl file into text using the following command: **tracerpt EapHostAuthr.etl** **–pdb** **&lt;pdbpath&gt;** **-tp** **&lt;tracemessagefilesdirectorypath&gt;** **-o** **EapHostAuthr.txt**</span></span>
    > [!Note]  
    > <span data-ttu-id="344ae-131">Wenn Sie keinen Zugriff auf das tracerpt-Tool haben, vermeiden Sie den letzten Schritt, und senden Sie stattdessen die ETL-Datei an Microsoft Developer Support.</span><span class="sxs-lookup"><span data-stu-id="344ae-131">If you do not have access to the tracerpt tool, avoid the last step and instead send the .etl file to Microsoft Developer Support.</span></span>

     

## <a name="event-tracing"></a><span data-ttu-id="344ae-132">Ereignisablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="344ae-132">Event tracing</span></span>

<span data-ttu-id="344ae-133">In Windows 7 und höheren Versionen von Windows bietet EAPHost eine ereignisbasierte Ablauf Verfolgung für den Authentifikator und den Peer.</span><span class="sxs-lookup"><span data-stu-id="344ae-133">In Windows 7 and later versions of Windows, EapHost provides event based tracing on the authenticator and the peer.</span></span> <span data-ttu-id="344ae-134">Der Vorteil der ereignisbasierten Ablauf Verfolgung besteht darin, dass zum Anzeigen der Ablauf Verfolgungs Meldungen keine Symbol Dateien erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="344ae-134">The advantage of event based tracing is that no symbol files are needed to view the trace messages.</span></span> <span data-ttu-id="344ae-135">So aktivieren Sie die Ereignis Ablauf Verfolgung:</span><span class="sxs-lookup"><span data-stu-id="344ae-135">To enable event tracing:</span></span>

1.  <span data-ttu-id="344ae-136">Öffnen Sie **Event Viewer**.</span><span class="sxs-lookup"><span data-stu-id="344ae-136">Open **EventViewer**.</span></span>
2.  <span data-ttu-id="344ae-137">Wichtige EAPHost-Nachrichten werden unter "benutzerdefinierte Ansichten \\ Administrative Ereignisse" protokolliert.</span><span class="sxs-lookup"><span data-stu-id="344ae-137">Critical EapHost messages are logged under: “Custom Views\\Administrative Events”</span></span>
3.  <span data-ttu-id="344ae-138">Nicht kritische Nachrichten werden unter "Anwendungen und Dienste \\ Microsoft \\ Windows \\ EAPHost" protokolliert.</span><span class="sxs-lookup"><span data-stu-id="344ae-138">Non-critical messages are logged under: “Applications and Services\\Microsoft\\Windows\\EapHost</span></span>
4.  <span data-ttu-id="344ae-139">Ereignismeldungen vom Typ "Analyse" und "Debuggen" können unter demselben Pfad angezeigt werden, indem Sie in der Titelleiste im Menü **Ansicht** die Option **analytische und Debugprotokolle anzeigen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="344ae-139">"Analytic" and "Debug" type event messages can be seen under the same path by selecting **Show Analytic and Debug Logs** from the **view** menu in the title bar.</span></span>

## <a name="tracing-on-the-routing-and-remote-access-service"></a><span data-ttu-id="344ae-140">Ablauf Verfolgung für den Routing-und RAS-Dienst</span><span class="sxs-lookup"><span data-stu-id="344ae-140">Tracing on the Routing and Remote Access Service</span></span>

<span data-ttu-id="344ae-141">So aktivieren Sie die RRAS-Ablauf Verfolgung:</span><span class="sxs-lookup"><span data-stu-id="344ae-141">To enable RRAS tracing:</span></span>

1.  <span data-ttu-id="344ae-142">Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten.</span><span class="sxs-lookup"><span data-stu-id="344ae-142">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="344ae-143">Führen Sie den folgenden Befehl aus: **netsh** **RAS** **set** **TR** **\* *_ _* en**</span><span class="sxs-lookup"><span data-stu-id="344ae-143">Run the following command: **netsh** **ras** **set** **tr** **\**_ _\* en*\*</span></span>
3.  <span data-ttu-id="344ae-144">**% Systemroot%-Ablauf \\ Verfolgung** öffnen, um RAS-Ablauf Verfolgungen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="344ae-144">Open **%systemroot%\\tracing** to view RAS traces</span></span>

<span data-ttu-id="344ae-145">So deaktivieren Sie die RRAS-Ablauf Verfolgung:</span><span class="sxs-lookup"><span data-stu-id="344ae-145">To disable RRAS tracing:</span></span>

1.  <span data-ttu-id="344ae-146">Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten.</span><span class="sxs-lookup"><span data-stu-id="344ae-146">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="344ae-147">Führen Sie den folgenden Befehl aus: **netsh** **RAS** **set** **TR** **\* *_ _* DIS**</span><span class="sxs-lookup"><span data-stu-id="344ae-147">Run the following command: **netsh** **ras** **set** **tr** **\**_ _\* dis*\*</span></span>

<span data-ttu-id="344ae-148">Weitere Informationen finden Sie unter [Netsh Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="344ae-148">For more information, see [Netsh Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="344ae-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="344ae-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="344ae-150">Verwenden von EAPHost</span><span class="sxs-lookup"><span data-stu-id="344ae-150">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="344ae-151">Routing- und RAS-Dienst (RRAS)</span><span class="sxs-lookup"><span data-stu-id="344ae-151">Routing and Remote Access Service (RRAS)</span></span>](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 