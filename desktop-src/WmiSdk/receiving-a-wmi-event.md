---
description: WMI enthält eine Ereignis Infrastruktur, die Benachrichtigungen zu Änderungen in WMI-Daten und-Diensten erzeugt. WMI-Ereignis Klassen stellen Benachrichtigungen bereit, wenn bestimmte Ereignisse auftreten.
ms.assetid: 347808a7-0f7b-4687-93f4-bea55c96795a
ms.tgt_platform: multiple
title: Empfangen eines WMI-Ereignisses
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 255f54f78bb64659d1cd07eddb72eae55b0263c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131016"
---
# <a name="receiving-a-wmi-event"></a><span data-ttu-id="6556e-104">Empfangen eines WMI-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="6556e-104">Receiving a WMI Event</span></span>

<span data-ttu-id="6556e-105">WMI enthält eine Ereignis Infrastruktur, die Benachrichtigungen zu Änderungen in WMI-Daten und-Diensten erzeugt.</span><span class="sxs-lookup"><span data-stu-id="6556e-105">WMI contains an event infrastructure that produces notifications about changes in WMI data and services.</span></span> <span data-ttu-id="6556e-106">WMI- [*Ereignis Klassen*](gloss-e.md) stellen Benachrichtigungen bereit, wenn bestimmte Ereignisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="6556e-106">WMI [*event classes*](gloss-e.md) provide notification when specific events occur.</span></span>

<span data-ttu-id="6556e-107">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="6556e-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="6556e-108">Ereignis Abfragen</span><span class="sxs-lookup"><span data-stu-id="6556e-108">Event Queries</span></span>](#event-queries)
-   [<span data-ttu-id="6556e-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6556e-109">Example</span></span>](#example)
-   [<span data-ttu-id="6556e-110">Ereignisconsumer</span><span class="sxs-lookup"><span data-stu-id="6556e-110">Event Consumers</span></span>](#event-consumers)
-   [<span data-ttu-id="6556e-111">Bereitstellen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="6556e-111">Providing Events</span></span>](#providing-events)
-   [<span data-ttu-id="6556e-112">Abonnement Kontingente</span><span class="sxs-lookup"><span data-stu-id="6556e-112">Subscription Quotas</span></span>](#subscription-quotas)
-   [<span data-ttu-id="6556e-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6556e-113">Related topics</span></span>](#related-topics)

## <a name="event-queries"></a><span data-ttu-id="6556e-114">Ereignis Abfragen</span><span class="sxs-lookup"><span data-stu-id="6556e-114">Event Queries</span></span>

<span data-ttu-id="6556e-115">Sie können eine [semisynchrone](receiving-synchronous-and-semisynchronous-event-notifications.md) oder [**asynchrone**](receiving-asynchronous-event-notifications.md) Abfrage erstellen, um Änderungen an Ereignisprotokollen, Prozesserstellung, Dienststatus, Computer Verfügbarkeit oder freiem Speicherplatz auf dem Datenträger sowie andere Entitäten oder Ereignisse zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="6556e-115">You can create a [semisynchronous](receiving-synchronous-and-semisynchronous-event-notifications.md) or [**asynchronous**](receiving-asynchronous-event-notifications.md) query to monitor changes to event logs, process creation, service status, computer availability or disk drive free space, and other entities or events.</span></span> <span data-ttu-id="6556e-116">Bei der Skripterstellung wird die [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) -Methode verwendet, um Ereignisse zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="6556e-116">In scripting, the [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) method is used to subscribe to events.</span></span> <span data-ttu-id="6556e-117">In C++ wird [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) verwendet.</span><span class="sxs-lookup"><span data-stu-id="6556e-117">In C++, [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) is used.</span></span> <span data-ttu-id="6556e-118">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="6556e-118">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="6556e-119">Eine Benachrichtigung über eine Änderung im standardmäßigen WMI-Datenmodell wird als System internes [*Ereignis*](gloss-i.md)bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6556e-119">Notification of a change in the standard WMI data model is called an [*intrinsic event*](gloss-i.md).</span></span> <span data-ttu-id="6556e-120">[**\_ \_ Instancecreationevent**](--instancecreationevent.md) oder [**\_ \_ namespacedeletionevent**](--namespacedeletionevent.md) sind Beispiele für systeminterne Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="6556e-120">[**\_\_InstanceCreationEvent**](--instancecreationevent.md) or [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md) are examples of intrinsic events.</span></span> <span data-ttu-id="6556e-121">Eine Benachrichtigung über eine Änderung, die ein Anbieter zum Definieren eines Anbieter Ereignisses vornimmt, wird als [*System externe-Ereignis*](gloss-e.md)bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6556e-121">Notification of a change that a provider makes to define a provider event is called an [*extrinsic event*](gloss-e.md).</span></span> <span data-ttu-id="6556e-122">Beispielsweise definieren der [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider), der [Energie Verwaltungs Ereignis Anbieter](/windows/desktop/CIMWin32Prov/power-management-event-provider)und der [Win32-Anbieter](/windows/desktop/CIMWin32Prov/win32-provider) ihre eigenen Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="6556e-122">For example, the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider), [Power Management Event Provider](/windows/desktop/CIMWin32Prov/power-management-event-provider), and [Win32 Provider](/windows/desktop/CIMWin32Prov/win32-provider) define their own events.</span></span> <span data-ttu-id="6556e-123">Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="6556e-123">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

## <a name="example"></a><span data-ttu-id="6556e-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6556e-124">Example</span></span>

<span data-ttu-id="6556e-125">Das folgende Skriptcode Beispiel ist eine Abfrage für das intrinsische [**\_ \_ instancecreationevent**](--instancecreationevent.md) der Ereignisklasse [**Win32 \_ ntlogevent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="6556e-125">The following script code example is a query for the intrinsic [**\_\_InstanceCreationEvent**](--instancecreationevent.md) of the event class [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span> <span data-ttu-id="6556e-126">Sie können dieses Programm im Hintergrund ausführen, und wenn ein Ereignis vorliegt, wird eine Meldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6556e-126">You can run this program in the background and when there is an event, a message appears.</span></span> <span data-ttu-id="6556e-127">Wenn Sie das Dialogfeld **warten auf Ereignisse** schließen, hält das Programm nicht mehr auf Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="6556e-127">If you close the **Waiting for events** dialog box, the program stops waiting for events.</span></span> <span data-ttu-id="6556e-128">Beachten Sie, dass **SeSecurityPrivilege** aktiviert werden muss.</span><span class="sxs-lookup"><span data-stu-id="6556e-128">Be aware that the **SeSecurityPrivilege** must be enabled.</span></span>


```VB
Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo (objObject.TargetInstance.Message)
End Sub

Set objWMIServices = GetObject( _
    "WinMgmts:{impersonationLevel=impersonate, (security)}") 

' Create the event sink object that receives the events
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
 
' Set up the event selection. SINK_OnObjectReady is called when
' a Win32_NTLogEvent event occurs
objWMIServices.ExecNotificationQueryAsync sink,"SELECT * FROM __InstanceCreationEvent " & "WHERE TargetInstance ISA 'Win32_NTLogEvent' "

WScript.Echo "Waiting for events"
```


```PowerShell

# Define event Query
$query = "SELECT * FROM __InstanceCreationEvent 
          WHERE TargetInstance ISA 'Win32_NTLogEvent' "

<# Register for event - also specify an action that
displays the log event when the event fires.#>

Register-WmiEvent -Source Demo1 -Query $query -Action {
                Write-Host "Log Event occured"
                $global:myevent = $event
                Write-Host "EVENT MESSAGE"
                Write-Host $event.SourceEventArgs.NewEvent.TargetInstance.Message}
<# So wait #>
"Waiting for events"
```





<span data-ttu-id="6556e-129">Das folgende VBScript-Codebeispiel zeigt das System externe-Ereignis [ \_ \_ RegistryValueChangeEvent](registering-for-system-registry-events.md) , das der Registrierungs Anbieter definiert.</span><span class="sxs-lookup"><span data-stu-id="6556e-129">The following VBScript code example shows the extrinsic event [\_\_RegistryValueChangeEvent](registering-for-system-registry-events.md) that the registry provider defines.</span></span> <span data-ttu-id="6556e-130">Das Skript erstellt einen temporären Consumer mithilfe des Aufrufes [**SWbemServices.Execnotificationqueryasync**](swbemservices-execnotificationqueryasync.md)und empfängt nur Ereignisse, wenn das Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6556e-130">The script creates a temporary consumer by using the call to [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md), and only receives events when the script is running.</span></span> <span data-ttu-id="6556e-131">Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird.</span><span class="sxs-lookup"><span data-stu-id="6556e-131">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="6556e-132">Um das Skript manuell anzuhalten, verwenden Sie den Task-Manager, um den Prozess zu unterbinden.</span><span class="sxs-lookup"><span data-stu-id="6556e-132">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="6556e-133">Verwenden Sie zum programmgesteuerten beenden die Methode " [**Beenden**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) " in der Win32- \_ Prozess Klasse.</span><span class="sxs-lookup"><span data-stu-id="6556e-133">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span> <span data-ttu-id="6556e-134">Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="6556e-134">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>


```VB
strComputer = "."

Set objWMIServices=GetObject( _
    "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default")

set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")


objWMIServices.ExecNotificationQueryAsync objSink, _
    "Select * from RegistryValueChangeEvent Where Hive = 'HKEY_LOCAL_MACHINE' and KeyPath = 'SYSTEM\\ControlSet001\\Control' and ValueName = 'CurrentUser'"

WScript.Echo "Waiting for events..."

While (True) 
     WScript.Sleep (1000)
Wend

 
WScript.Echo "Listening for Registry Change Events..." & vbCrLf 

While(True) 
    WScript.Sleep 1000 
Wend 

Sub SINK_OnObjectReady(wmiObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Value Change Event" & vbCrLf & wmiObject.GetObjectText_() 
End Sub
```



## <a name="event-consumers"></a><span data-ttu-id="6556e-135">Ereignisconsumer</span><span class="sxs-lookup"><span data-stu-id="6556e-135">Event Consumers</span></span>

<span data-ttu-id="6556e-136">Beim Ausführen eines Skripts oder einer Anwendung können Ereignisse mithilfe der folgenden Verbraucher überwacht oder genutzt werden:</span><span class="sxs-lookup"><span data-stu-id="6556e-136">You can monitor or consume events using the following consumers while a script or application is running:</span></span>

-   <span data-ttu-id="6556e-137">Temporäre Ereignisconsumer</span><span class="sxs-lookup"><span data-stu-id="6556e-137">Temporary event consumers</span></span>

    <span data-ttu-id="6556e-138">Ein [*temporärer Consumer*](gloss-t.md) ist eine WMI-Client Anwendung, die ein WMI-Ereignis empfängt.</span><span class="sxs-lookup"><span data-stu-id="6556e-138">A [*temporary consumer*](gloss-t.md) is a WMI client application that receives a WMI event.</span></span> <span data-ttu-id="6556e-139">WMI enthält eine eindeutige Schnittstelle, die verwendet, um die Ereignisse anzugeben, die von WMI an eine Client Anwendung gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6556e-139">WMI includes a unique interface that use to specify the events for WMI to send to a client application.</span></span> <span data-ttu-id="6556e-140">Ein temporärer Ereignisconsumer gilt als temporär, da er nur funktioniert, wenn er von einem Benutzer explizit geladen wird.</span><span class="sxs-lookup"><span data-stu-id="6556e-140">A temporary event consumer is considered temporary because it only works when specifically loaded by a user.</span></span> <span data-ttu-id="6556e-141">Weitere Informationen finden Sie unter [empfangen von Ereignissen für die Dauer Ihrer Anwendung](receiving-events-for-the-duration-of-your-application.md).</span><span class="sxs-lookup"><span data-stu-id="6556e-141">For more information, see [Receiving Events for the Duration of Your Application](receiving-events-for-the-duration-of-your-application.md).</span></span>

-   <span data-ttu-id="6556e-142">Permanente Ereignisconsumer</span><span class="sxs-lookup"><span data-stu-id="6556e-142">Permanent event consumers</span></span>

    <span data-ttu-id="6556e-143">Ein [*dauerhafter Consumer*](gloss-p.md) ist ein COM-Objekt, das jederzeit ein WMI-Ereignis empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="6556e-143">A [*permanent consumer*](gloss-p.md) is a COM object that can receive a WMI event at all times.</span></span> <span data-ttu-id="6556e-144">Ein dauerhafter Ereignisconsumer verwendet einen Satz von persistenten Objekten und Filtern, um ein WMI-Ereignis zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="6556e-144">A permanent event consumer uses a set of persistent objects and filters to capture a WMI event.</span></span> <span data-ttu-id="6556e-145">Wie bei einem temporären Ereignisconsumer richten Sie eine Reihe von WMI-Objekten und filtern ein, die ein WMI-Ereignis erfassen.</span><span class="sxs-lookup"><span data-stu-id="6556e-145">Like a temporary event consumer, you set up a series of WMI objects and filters that capture a WMI event.</span></span> <span data-ttu-id="6556e-146">Wenn ein Ereignis auftritt, das einem Filter entspricht, lädt WMI den permanenten Ereignisconsumer und benachrichtigt ihn über das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6556e-146">When an event occurs that matches a filter, WMI loads the permanent event consumer and notifies it about the event.</span></span> <span data-ttu-id="6556e-147">Da ein dauerhafter Consumer im WMI-Repository implementiert ist und eine ausführbare Datei ist, die in WMI registriert ist, wird der permanente Ereignisconsumer nach der Erstellung und auch nach einem Neustart des Betriebssystems, solange WMI ausgeführt wird, nach einem Neustart des Betriebssystems ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6556e-147">Because a permanent consumer is implemented in the WMI repository and is an executable file that is registered in WMI, the permanent event consumer operates and receives events after it is created and even after a reboot of the operating system as long as WMI is running.</span></span> <span data-ttu-id="6556e-148">Weitere Informationen finden Sie [unter empfangen von Ereignissen zu allen Zeit](receiving-events-at-all-times.md)Punkten.</span><span class="sxs-lookup"><span data-stu-id="6556e-148">For more information, see [Receiving Events at All Times](receiving-events-at-all-times.md).</span></span>

<span data-ttu-id="6556e-149">Skripts oder Anwendungen, die Ereignisse empfangen, haben besondere Sicherheitsüberlegungen.</span><span class="sxs-lookup"><span data-stu-id="6556e-149">Scripts or applications that receive events have special security considerations.</span></span> <span data-ttu-id="6556e-150">Weitere Informationen finden Sie unter [Sichern von WMI-Ereignissen](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="6556e-150">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

<span data-ttu-id="6556e-151">Eine Anwendung oder ein Skript kann einen integrierten WMI-Ereignis Anbieter verwenden, der [Standard Consumerklassen](standard-consumer-classes.md)bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6556e-151">An application or script can use a built-in WMI event provider that supplies [standard consumer classes](standard-consumer-classes.md).</span></span> <span data-ttu-id="6556e-152">Jede Standard Consumerklasse antwortet auf ein Ereignis mit einer anderen Aktion, indem eine e-Mail-Nachricht gesendet oder ein Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6556e-152">Each standard consumer class responds to an event with a different action by sending an email message or executing a script.</span></span> <span data-ttu-id="6556e-153">Sie müssen keinen Anbieter Code schreiben, um eine Standard Consumerklasse zum Erstellen eines permanenten Ereignisconsumer zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6556e-153">You do not have to write provider code to use a standard consumer class to create a permanent event consumer.</span></span> <span data-ttu-id="6556e-154">Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="6556e-154">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="providing-events"></a><span data-ttu-id="6556e-155">Bereitstellen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="6556e-155">Providing Events</span></span>

<span data-ttu-id="6556e-156">Ein Ereignis Anbieter ist eine COM-Komponente, die ein Ereignis an WMI sendet.</span><span class="sxs-lookup"><span data-stu-id="6556e-156">An event provider is a COM component that sends an event to WMI.</span></span> <span data-ttu-id="6556e-157">Sie können einen Ereignis Anbieter erstellen, um ein Ereignis in einer C++-oder c#-Anwendung zu senden.</span><span class="sxs-lookup"><span data-stu-id="6556e-157">You can create an event provider to send an event in a C++ or C# application.</span></span> <span data-ttu-id="6556e-158">Die meisten Ereignis Anbieter verwalten ein Objekt für WMI, z. b. eine Anwendung oder ein Hardware Element.</span><span class="sxs-lookup"><span data-stu-id="6556e-158">Most event providers manage an object for WMI, for example, an application or hardware item.</span></span> <span data-ttu-id="6556e-159">Weitere Informationen finden Sie unter [Schreiben eines Ereignis Anbieters](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6556e-159">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

<span data-ttu-id="6556e-160">Ein zeitgesteuertes oder sich wiederholendes Ereignis ist ein Ereignis, das zu einem bestimmten Zeitpunkt auftritt.</span><span class="sxs-lookup"><span data-stu-id="6556e-160">A timed or repeating event is an event that occurs at a predetermined time.</span></span>

<span data-ttu-id="6556e-161">WMI bietet die folgenden Möglichkeiten, um zeitgesteuerte oder sich wiederholende Ereignisse für Ihre Anwendungen zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="6556e-161">WMI provides the following ways to create timed or repeating events for your applications:</span></span>

-   <span data-ttu-id="6556e-162">Die standardmäßige Microsoft-Ereignis Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="6556e-162">The standard Microsoft event infrastructure.</span></span>
-   <span data-ttu-id="6556e-163">Eine spezialisierte Timer-Klasse.</span><span class="sxs-lookup"><span data-stu-id="6556e-163">A specialized timer class.</span></span>

<span data-ttu-id="6556e-164">Weitere Informationen finden Sie unter [empfangen eines zeitgesteuerten oder wiederholten Ereignisses](receiving-a-timed-or-repeating-event.md).</span><span class="sxs-lookup"><span data-stu-id="6556e-164">For more information, see [Receiving a Timed or Repeating Event](receiving-a-timed-or-repeating-event.md).</span></span> <span data-ttu-id="6556e-165">Wenn Sie einen Ereignis Anbieter schreiben, sollten Sie die Sicherheitsinformationen beachten, die bei der [sicheren Bereitstellung von Ereignissen](providing-events-securely.md)identifiziert werden</span><span class="sxs-lookup"><span data-stu-id="6556e-165">When you write an event provider, consider the security information identified in [Providing Events Securely](providing-events-securely.md).</span></span>

<span data-ttu-id="6556e-166">Es wird empfohlen, dass permanente Ereignis Abonnements in den Namespace des Stamm Abonnements kompiliert werden \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="6556e-166">It is recommended that permanent event subscriptions be compiled into the \\root\\subscription namespace.</span></span> <span data-ttu-id="6556e-167">Weitere Informationen finden Sie unter [Implementieren von Abonnements für permanente Namespace-Ereignisse](implementing-cross-namespace-permanent-event-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="6556e-167">For more information, see [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span></span>

## <a name="subscription-quotas"></a><span data-ttu-id="6556e-168">Abonnement Kontingente</span><span class="sxs-lookup"><span data-stu-id="6556e-168">Subscription Quotas</span></span>

<span data-ttu-id="6556e-169">Durch das Abrufen von Ereignissen kann die Leistung für Anbieter beeinträchtigt werden, die Abfragen für große Datasets unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6556e-169">Polling for events can degrade performance for providers that support queries over huge data sets.</span></span> <span data-ttu-id="6556e-170">Außerdem kann jeder Benutzer, der über Lesezugriff auf einen Namespace mit dynamischen Anbietern verfügt, einen Denial-of-Service-Angriff (DOS) durchführen.</span><span class="sxs-lookup"><span data-stu-id="6556e-170">Additionally, any user that has read access to a namespace with dynamic providers can perform a denial of service (DoS) attack.</span></span> <span data-ttu-id="6556e-171">WMI verwaltet Kontingente für alle Benutzer zusammen und für jeden Ereignisconsumer in der einzelnen Instanz von " [**\_ \_ arbiatorconfiguration**](--arbitratorconfiguration.md) ", die sich im Stamm \\ Namespace befindet.</span><span class="sxs-lookup"><span data-stu-id="6556e-171">WMI maintains quotas for all of the users combined and for each event consumer in the single instance of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md) located in the \\root namespace.</span></span> <span data-ttu-id="6556e-172">Diese Kontingente sind global und nicht für jeden Namespace.</span><span class="sxs-lookup"><span data-stu-id="6556e-172">These quotas are global rather than for each namespace.</span></span> <span data-ttu-id="6556e-173">Die Kontingente können nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6556e-173">You cannot change the quotas.</span></span>

<span data-ttu-id="6556e-174">WMI erzwingt derzeit Kontingente mithilfe der Eigenschaften von " [**\_ \_ arbiatorconfiguration**](--arbitratorconfiguration.md)".</span><span class="sxs-lookup"><span data-stu-id="6556e-174">WMI currently enforces quotas using the properties of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md).</span></span> <span data-ttu-id="6556e-175">Jedes Kontingent verfügt über einen pro-Benutzer und eine Gesamt Version, die alle Benutzer kombiniert und nicht pro Namespace umfasst.</span><span class="sxs-lookup"><span data-stu-id="6556e-175">Each quota has a per user and a total version that includes all users combined, not per namespace.</span></span> <span data-ttu-id="6556e-176">In der folgenden Tabelle sind die Kontingente aufgelistet, die für die Eigenschaften von " **\_ \_ arbiatorconfiguration** " gelten.</span><span class="sxs-lookup"><span data-stu-id="6556e-176">The following table lists the quotas that apply to the **\_\_ArbitratorConfiguration** properties.</span></span>



| <span data-ttu-id="6556e-177">Gesamt/Benutzer</span><span class="sxs-lookup"><span data-stu-id="6556e-177">Total/PerUser</span></span>                                                                   | <span data-ttu-id="6556e-178">Kontingent</span><span class="sxs-lookup"><span data-stu-id="6556e-178">Quota</span></span>                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6556e-179">Temporaryabonnemenzstotal</span><span class="sxs-lookup"><span data-stu-id="6556e-179">TemporarySubscriptionsTotal</span></span><br/> <span data-ttu-id="6556e-180">Temporaryabonnemenamtionsperuser</span><span class="sxs-lookup"><span data-stu-id="6556e-180">TemporarySubscriptionsPerUser</span></span><br/> | <span data-ttu-id="6556e-181">10.000</span><span class="sxs-lookup"><span data-stu-id="6556e-181">10,000</span></span><br/> <span data-ttu-id="6556e-182">1\.000</span><span class="sxs-lookup"><span data-stu-id="6556e-182">1,000</span></span><br/>                                          |
| <span data-ttu-id="6556e-183">Permanent abonniert</span><span class="sxs-lookup"><span data-stu-id="6556e-183">PermanentSubscriptionsTotal</span></span><br/> <span data-ttu-id="6556e-184">Permanentabonneptionsperuser</span><span class="sxs-lookup"><span data-stu-id="6556e-184">PermanentSubscriptionsPerUser</span></span><br/> | <span data-ttu-id="6556e-185">10.000</span><span class="sxs-lookup"><span data-stu-id="6556e-185">10,000</span></span><br/> <span data-ttu-id="6556e-186">1\.000</span><span class="sxs-lookup"><span data-stu-id="6556e-186">1,000</span></span><br/>                                          |
| <span data-ttu-id="6556e-187">Pollinginstructionstotal</span><span class="sxs-lookup"><span data-stu-id="6556e-187">PollingInstructionsTotal</span></span><br/> <span data-ttu-id="6556e-188">Pollinginstructionsperuser</span><span class="sxs-lookup"><span data-stu-id="6556e-188">PollingInstructionsPerUser</span></span><br/>       | <span data-ttu-id="6556e-189">10.000</span><span class="sxs-lookup"><span data-stu-id="6556e-189">10,000</span></span><br/> <span data-ttu-id="6556e-190">1\.000</span><span class="sxs-lookup"><span data-stu-id="6556e-190">1,000</span></span><br/>                                          |
| <span data-ttu-id="6556e-191">Pollingmemorytotal</span><span class="sxs-lookup"><span data-stu-id="6556e-191">PollingMemoryTotal</span></span><br/> <span data-ttu-id="6556e-192">Pollingmemoryperuser</span><span class="sxs-lookup"><span data-stu-id="6556e-192">PollingMemoryPerUser</span></span><br/>                   | <span data-ttu-id="6556e-193">10 Millionen (0x989680) Bytes</span><span class="sxs-lookup"><span data-stu-id="6556e-193">10,000,000 (0x989680) bytes</span></span><br/> <span data-ttu-id="6556e-194">5 Millionen (0x4cb40) Bytes</span><span class="sxs-lookup"><span data-stu-id="6556e-194">5,000,000 (0x4CB40) bytes</span></span><br/> |



 

<span data-ttu-id="6556e-195">Ein Administrator oder Benutzer mit **Vollständiger \_ Schreib** Berechtigung im-Namespace kann die Singleton-Instanz von " [**\_ \_ arbiatorconfiguration**](--arbitratorconfiguration.md)" ändern.</span><span class="sxs-lookup"><span data-stu-id="6556e-195">An administrator or a user with **FULL\_WRITE** permission in the namespace can modify the singleton instance of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md).</span></span> <span data-ttu-id="6556e-196">WMI verfolgt das Kontingent pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="6556e-196">WMI tracks the per-user quota.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6556e-197">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6556e-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6556e-198">Verwenden von WMI</span><span class="sxs-lookup"><span data-stu-id="6556e-198">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

