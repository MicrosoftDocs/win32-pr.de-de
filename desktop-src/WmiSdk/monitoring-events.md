---
description: System Administratoren können WMI zum Überwachen von Ereignissen in einem Netzwerk verwenden.
ms.assetid: 871d4add-a7b1-4ec9-a202-3821fdf09e9f
ms.tgt_platform: multiple
title: Überwachen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea5d9fc6f9a12f4aa1fb7bc0ff6f66fc4dd4a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130393"
---
# <a name="monitoring-events"></a><span data-ttu-id="5c92d-103">Überwachen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="5c92d-103">Monitoring Events</span></span>

<span data-ttu-id="5c92d-104">System Administratoren können WMI zum Überwachen von Ereignissen in einem Netzwerk verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c92d-104">System administrators can use WMI to monitor events on a network.</span></span> <span data-ttu-id="5c92d-105">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5c92d-105">For example:</span></span>

-   <span data-ttu-id="5c92d-106">Ein Dienst wird unerwartet beendet.</span><span class="sxs-lookup"><span data-stu-id="5c92d-106">A service stops unexpectedly.</span></span>
-   <span data-ttu-id="5c92d-107">Ein Server steht nicht mehr zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5c92d-107">A server becomes unavailable.</span></span>
-   <span data-ttu-id="5c92d-108">Ein Laufwerk füllt die Kapazität von 80% aus.</span><span class="sxs-lookup"><span data-stu-id="5c92d-108">A disk drive fills to 80% capacity.</span></span>
-   <span data-ttu-id="5c92d-109">Sicherheitsereignisse werden einem NT-Ereignisprotokoll gemeldet.</span><span class="sxs-lookup"><span data-stu-id="5c92d-109">Security events are reported to an NT Event Log.</span></span>

<span data-ttu-id="5c92d-110">WMI unterstützt Ereigniserkennung und-Übermittlung an Ereignisconsumer, da einige WMI-Anbieter Ereignis Anbieter sind.</span><span class="sxs-lookup"><span data-stu-id="5c92d-110">WMI supports event detection and delivery to event consumers because some WMI providers are event providers.</span></span> <span data-ttu-id="5c92d-111">Weitere Informationen finden Sie unter [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="5c92d-111">For more information, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="5c92d-112">[*Ereignisconsumer*](gloss-e.md) sind Anwendungen oder Skripts, die eine Benachrichtigung über Ereignisse anfordern und dann Aufgaben ausführen, wenn bestimmte Ereignisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="5c92d-112">[*Event consumers*](gloss-e.md) are applications or scripts that request notification of events, and then perform tasks when specific events occur.</span></span> <span data-ttu-id="5c92d-113">Sie können Ereignis Überwachungs Skripts oder-Anwendungen erstellen, die vorübergehend überwachen, wann Ereignisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="5c92d-113">You can create event monitoring scripts or applications that temporarily monitor when events occur.</span></span> <span data-ttu-id="5c92d-114">WMI stellt außerdem eine Reihe vorinstallierter dauerhafter Ereignis Anbieter und die permanenten Consumerklassen bereit, die es Ihnen ermöglichen, Ereignisse dauerhaft zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="5c92d-114">WMI also supplies a set of preinstalled permanent event providers and the permanent consumer classes that enable you to permanently monitor events.</span></span> <span data-ttu-id="5c92d-115">Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="5c92d-115">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="5c92d-116">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="5c92d-116">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="5c92d-117">Verwenden temporärer Ereignisconsumer</span><span class="sxs-lookup"><span data-stu-id="5c92d-117">Using Temporary Event Consumers</span></span>](#using-temporary-event-consumers)
-   [<span data-ttu-id="5c92d-118">Verwenden von permanenten Ereignisverbrauchern</span><span class="sxs-lookup"><span data-stu-id="5c92d-118">Using Permanent Event Consumers</span></span>](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a><span data-ttu-id="5c92d-119">Verwenden temporärer Ereignisconsumer</span><span class="sxs-lookup"><span data-stu-id="5c92d-119">Using Temporary Event Consumers</span></span>

<span data-ttu-id="5c92d-120">Temporäre Ereignisconsumer sind Skripts oder Anwendungen, die die Ereignisse zurückgeben, die einer Ereignis Abfrage oder einem Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5c92d-120">Temporary event consumers are scripts or applications that return the events that match an event query or filter.</span></span> <span data-ttu-id="5c92d-121">Temporäre Ereignis Abfragen verwenden in der Regel entweder [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++-Anwendungen oder [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) in Skripts und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5c92d-121">Temporary event queries usually use either [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ applications or [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) in scripts and Visual Basic.</span></span>

<span data-ttu-id="5c92d-122">Eine Ereignis Abfrage fordert Instanzen einer Ereignisklasse an, die einen bestimmten Ereignistyp angibt, z. b. [**Win32 \_ processtrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) oder [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="5c92d-122">An event query requests instances of an event class that specifies a certain type of event, such as [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) or [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span>

<span data-ttu-id="5c92d-123">Im folgenden VBScript-Codebeispiel wird eine Benachrichtigung angefordert, wenn eine Instanz von [**Win32 \_ processtrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5c92d-123">The following VBScript code example requests notification when an instance of [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) is created.</span></span> <span data-ttu-id="5c92d-124">Eine Instanz dieser Klasse wird generiert, wenn ein Prozess gestartet oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c92d-124">An instance of this class is generated when a process is started or stopped.</span></span>

<span data-ttu-id="5c92d-125">Um das Skript auszuführen, kopieren Sie es in eine Datei mit dem Namen event.vbs, und verwenden Sie die folgende Befehlszeile: **cscript event.vbs**.</span><span class="sxs-lookup"><span data-stu-id="5c92d-125">To execute the script, copy it to a file named event.vbs and use the following command line: **cscript event.vbs**.</span></span> <span data-ttu-id="5c92d-126">Sie können die Ausgabe des Skripts anzeigen, indem Sie Notepad.exe oder einen anderen Prozess starten.</span><span class="sxs-lookup"><span data-stu-id="5c92d-126">You can see output from the script by starting Notepad.exe or any other process.</span></span> <span data-ttu-id="5c92d-127">Das Skript wird beendet, nachdem fünf Prozesse gestartet oder beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="5c92d-127">The script stops after five processes have started or stopped.</span></span>

<span data-ttu-id="5c92d-128">Dieses Skript ruft [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md)auf, bei dem es sich um die [*semisynchrone*](gloss-s.md) Version der-Methode handelt.</span><span class="sxs-lookup"><span data-stu-id="5c92d-128">This script calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), which is the [*semisynchronous*](gloss-s.md) version of the method.</span></span> <span data-ttu-id="5c92d-129">Im nächsten Skript finden Sie ein Beispiel für das Einrichten eines asynchronen temporären Ereignis Abonnements durch Aufrufen von [**SWbemServices.Execnotificationqueryasync**](swbemservices-execnotificationqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="5c92d-129">See the next script for an example of setting up an asynchronous temporary event subscription by calling [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span></span> <span data-ttu-id="5c92d-130">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5c92d-130">For more information, see [Calling a Method](calling-a-method.md).</span></span> <span data-ttu-id="5c92d-131">Das Skript ruft die Datei " [**errbemeventsource. NextEvent**](swbemeventsource-nextevent.md) " auf, um jedes Ereignis beim Eintreffen abzurufen und zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="5c92d-131">The script calls [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) to obtain and process each event as it arrives.</span></span> <span data-ttu-id="5c92d-132">Speichern Sie das Skript in einer Datei mit der Erweiterung. VSB, und führen Sie das Skript mit cscript: **cscript file.vbs** in einer Befehlszeile aus.</span><span class="sxs-lookup"><span data-stu-id="5c92d-132">Save the script in a file with a .vbs extension and run the script on a command line using CScript: **cscript file.vbs**.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM Win32_ProcessTrace")

Wscript.Echo "Waiting for events ..."
i = 0
Do Until i=5
    Set objReceivedEvent = objEvents.NextEvent
    'report an event
    Wscript.Echo "Win32_ProcessTrace event occurred" & VBNewLine _
        & "Process Name = " _
            & objReceivedEvent.ProcessName & VBNewLine _
        & "Process ID = " _
            & objReceivedEvent.Processid & VBNewLine _
        & "Session ID = " & objReceivedEvent.SessionID 
i = i+ 1
Loop
```



Temporäre Ereignisconsumer müssen manuell gestartet werden und müssen nicht über WMI-Neustarts oder Betriebssystem Neustarts hinweg beibehalten werden. <span data-ttu-id="5c92d-134">Ein temporärer Ereignisconsumer kann Ereignisse nur verarbeiten, während er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c92d-134">A temporary event consumer can process events only while it is running.</span></span>

<span data-ttu-id="5c92d-135">Im folgenden Verfahren wird beschrieben, wie ein temporärer Ereignisconsumer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5c92d-135">The following procedure describes how to create a temporary event consumer.</span></span>

<span data-ttu-id="5c92d-136">**So erstellen Sie einen temporären Ereignisconsumer**</span><span class="sxs-lookup"><span data-stu-id="5c92d-136">**To create a temporary event consumer**</span></span>

1.  <span data-ttu-id="5c92d-137">Entscheiden Sie, welche Programmiersprache verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c92d-137">Decide which programming language to use.</span></span>

    <span data-ttu-id="5c92d-138">Die Programmiersprache bestimmt die zu verwendende API.</span><span class="sxs-lookup"><span data-stu-id="5c92d-138">The programming language determines the API to use.</span></span>

    -   <span data-ttu-id="5c92d-139">Verwenden Sie für die Programmiersprache C++ die [com-API für WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="5c92d-139">For the C++ programming language, use the [COM API for WMI](com-api-for-wmi.md).</span></span>
    -   <span data-ttu-id="5c92d-140">Verwenden Sie für Visual Basic-oder Skriptsprachen die [Skript-API für WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="5c92d-140">For Visual Basic or scripting languages, use the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

2.  <span data-ttu-id="5c92d-141">Beginnen Sie mit dem Programmieren einer temporären ereignisconsumeranwendung auf dieselbe Weise, wie Sie eine WMI-Anwendung starten.</span><span class="sxs-lookup"><span data-stu-id="5c92d-141">Start coding a temporary event consumer application the same way that you start a WMI application.</span></span>

    <span data-ttu-id="5c92d-142">Die ersten Schritte der Codierung hängen von der Programmiersprache ab.</span><span class="sxs-lookup"><span data-stu-id="5c92d-142">The first steps of coding depend on the programming language.</span></span> <span data-ttu-id="5c92d-143">In der Regel melden Sie sich bei WMI an und richten die Sicherheitseinstellungen ein.</span><span class="sxs-lookup"><span data-stu-id="5c92d-143">Typically, you log onto WMI and set up the security settings.</span></span> <span data-ttu-id="5c92d-144">Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="5c92d-144">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

3.  <span data-ttu-id="5c92d-145">Definieren Sie die Ereignis Abfrage, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="5c92d-145">Define the event query that you want to use.</span></span>

    <span data-ttu-id="5c92d-146">Um einige Arten von Leistungsdaten zu erhalten, müssen Sie möglicherweise Klassen verwenden, die von Hochleistungs Anbietern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5c92d-146">To obtain some types of performance data, you may need to use classes provided by high-performance providers.</span></span> <span data-ttu-id="5c92d-147">Weitere Informationen finden Sie unter über [Wachen von Leistungsdaten](monitoring-performance-data.md), [bestimmen der Art des](determining-the-type-of-event-to-receive.md)empfangenden Ereignisses und [Abfragen mit WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="5c92d-147">For more information, see [Monitoring Performance Data](monitoring-performance-data.md), [Determining the Type of Event To Receive](determining-the-type-of-event-to-receive.md), and [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="5c92d-148">Entscheiden Sie sich für einen asynchronen oder einen semisynchronen aufrufsbefehl, und wählen Sie die API-Methode aus.</span><span class="sxs-lookup"><span data-stu-id="5c92d-148">Decide to make either an asynchronous call or an semisynchronous call, and choose the API method.</span></span>

    <span data-ttu-id="5c92d-149">Mit asynchronen aufrufen können Sie den Aufwand für das Abrufen von Daten vermeiden.</span><span class="sxs-lookup"><span data-stu-id="5c92d-149">Asynchronous calls allow you to avoid the overhead of polling for data.</span></span> <span data-ttu-id="5c92d-150">Semisynchrone Aufrufe bieten jedoch eine ähnliche Leistung mit größerer Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="5c92d-150">However, semisynchronous calls provide similar performance with greater security.</span></span> <span data-ttu-id="5c92d-151">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5c92d-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

5.  <span data-ttu-id="5c92d-152">Führen Sie den asynchronen oder semisynchronen Methoden aufrufsbefehl aus, und schließen Sie eine Ereignis Abfrage *als den Parameter* "" "</span><span class="sxs-lookup"><span data-stu-id="5c92d-152">Make the asynchronous or semisynchronous method call and include an event query as the *strQuery* parameter.</span></span>

    <span data-ttu-id="5c92d-153">Für C++-Anwendungen werden die folgenden Methoden aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="5c92d-153">For C++ applications, call the following methods:</span></span>

    -   [<span data-ttu-id="5c92d-154">**IWbemServices:: ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="5c92d-154">**IWbemServices::ExecNotificationQuery**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [<span data-ttu-id="5c92d-155">**IWbemServices:: ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="5c92d-155">**IWbemServices::ExecNotificationQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    <span data-ttu-id="5c92d-156">Bei Skripts werden die folgenden Methoden aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="5c92d-156">For scripts, call the following methods:</span></span>

    -   [<span data-ttu-id="5c92d-157">**CnotificationquerySWbemServices.Exe**</span><span class="sxs-lookup"><span data-stu-id="5c92d-157">**SWbemServices.ExecNotificationQuery**</span></span>](swbemservices-execnotificationquery.md)
    -   [<span data-ttu-id="5c92d-158">**SWbemServices.Execnotificationqueryasync**</span><span class="sxs-lookup"><span data-stu-id="5c92d-158">**SWbemServices.ExecNotificationQueryAsync**</span></span>](swbemservices-execnotificationqueryasync.md)

6.  <span data-ttu-id="5c92d-159">Schreiben Sie den Code, um das zurückgegebene Ereignis Objekt zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="5c92d-159">Write the code to process the returned event object.</span></span>

    <span data-ttu-id="5c92d-160">Fügen Sie für asynchrone Ereignis Abfragen den Code in die verschiedenen Methoden oder Ereignisse der Objekt Senke ein.</span><span class="sxs-lookup"><span data-stu-id="5c92d-160">For asynchronous event queries, put the code in the various methods or events of the object sink.</span></span> <span data-ttu-id="5c92d-161">Bei semisynchronen Ereignis Abfragen wird jedes Objekt zurückgegeben, da es von WMI abgerufen wird, sodass sich der Code in der Schleife befinden muss, die jedes Objekt verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5c92d-161">For semisynchronous event queries, each object is returned as WMI obtains it, so the code should be in the loop that handles each object.</span></span>

<span data-ttu-id="5c92d-162">Das folgende Skriptcode Beispiel ist eine asynchrone Version des [**Win32 \_ processtrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) -Skripts.</span><span class="sxs-lookup"><span data-stu-id="5c92d-162">The following script code example is an asynchronous version of the [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) script.</span></span> <span data-ttu-id="5c92d-163">Da asynchrone Vorgänge sofort zurückgegeben werden, wird das Skript in einem Dialogfeld aktiv, während es auf Ereignisse wartet.</span><span class="sxs-lookup"><span data-stu-id="5c92d-163">Because asynchronous operations return immediately, a dialog box keeps the script active while it is waiting for events.</span></span>

<span data-ttu-id="5c92d-164">Anstatt " [**slibemeventsource. NextEvent**](swbemeventsource-nextevent.md) " aufzurufen, um die einzelnen Ereignisse zu empfangen, verfügt das Skript über einen Ereignishandler für das Ereignis " [**slibemsink onobjectready**](swbemsink-onobjectready.md) ".</span><span class="sxs-lookup"><span data-stu-id="5c92d-164">Rather than call [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) to receive each event, the script has an event handler for the [**SWbemSink OnObjectReady**](swbemsink-onobjectready.md) event.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\CIMV2") 
Set EventSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync EventSink, _
    "SELECT * FROM Win32_ProcessTrace WITHIN 10"
WScript.Echo "Waiting for events..."

i = 0
While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "Win32_ProcessTrace event has occurred."
    i = i+1
    If i = 3 Then WScript.Quit 0 
End Sub

```



> [!Note]
>
> <span data-ttu-id="5c92d-165">Ein asynchroner Rückruf (z. b. ein Rückruf, der von der `SINK_OnObjectReady` Unterroutine verarbeitet wird) ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="5c92d-165">An asynchronous callback such as a callback handled by the `SINK_OnObjectReady` subroutine, allows a nonauthenticated user to provide data to the sink.</span></span> <span data-ttu-id="5c92d-166">Verwenden Sie für eine bessere Sicherheit entweder die semisynchrone Kommunikation oder die synchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="5c92d-166">For better security, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="5c92d-167">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="5c92d-167">For more information, see the following topics:</span></span>
>
> -   [<span data-ttu-id="5c92d-168">Erstellen eines semisynchronen Aufrufes mit C++</span><span class="sxs-lookup"><span data-stu-id="5c92d-168">Making a Semisynchronous Call with C++</span></span>](making-a-semisynchronous-call-with-c--.md)
> -   [<span data-ttu-id="5c92d-169">Erstellen eines semisynchronen Aufrufes mit VBScript</span><span class="sxs-lookup"><span data-stu-id="5c92d-169">Making a Semisynchronous Call with VBScript</span></span>](making-a-semisynchronous-call-with-vbscript.md)
> -   [<span data-ttu-id="5c92d-170">Erstellen eines asynchronen Aufrufes mit C++</span><span class="sxs-lookup"><span data-stu-id="5c92d-170">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
> -   [<span data-ttu-id="5c92d-171">Erstellen eines asynchronen Aufrufes mit VBScript</span><span class="sxs-lookup"><span data-stu-id="5c92d-171">Making an Asynchronous Call with VBScript</span></span>](making-an-asynchronous-call-with-vbscript.md)
> -   [<span data-ttu-id="5c92d-172">Festlegen der Sicherheit für einen asynchronen-Befehl</span><span class="sxs-lookup"><span data-stu-id="5c92d-172">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
> -   [<span data-ttu-id="5c92d-173">Sichern von Skript Clients</span><span class="sxs-lookup"><span data-stu-id="5c92d-173">Securing Scripting Clients</span></span>](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a><span data-ttu-id="5c92d-174">Verwenden von permanenten Ereignisverbrauchern</span><span class="sxs-lookup"><span data-stu-id="5c92d-174">Using Permanent Event Consumers</span></span>

<span data-ttu-id="5c92d-175">Ein dauerhafter Ereignisconsumer wird ausgeführt, bis die Registrierung explizit abgebrochen wird, und startet dann, wenn WMI oder das System neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5c92d-175">A permanent event consumer runs until its registration is explicitly canceled, and then starts up when WMI or the system restarts.</span></span>

<span data-ttu-id="5c92d-176">Ein dauerhafter Ereignisconsumer ist eine Kombination aus WMI-Klassen,-Filtern und COM-Objekten in einem System.</span><span class="sxs-lookup"><span data-stu-id="5c92d-176">A permanent event consumer is a combination of WMI classes, filters, and COM objects on a system.</span></span>

<span data-ttu-id="5c92d-177">In der folgenden Liste sind die erforderlichen Komponenten zum Erstellen eines permanenten Ereignisconsumers aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="5c92d-177">The following list identifies the parts required to create a permanent event consumer:</span></span>

-   <span data-ttu-id="5c92d-178">Ein COM-Objekt, das den Code enthält, der den permanenten Consumer implementiert.</span><span class="sxs-lookup"><span data-stu-id="5c92d-178">A COM object containing the code that implements the permanent consumer.</span></span>
-   <span data-ttu-id="5c92d-179">Eine neue permanente Consumerklasse.</span><span class="sxs-lookup"><span data-stu-id="5c92d-179">A new permanent consumer class.</span></span>
-   <span data-ttu-id="5c92d-180">Eine Instanz der permanenten Consumer-Klasse.</span><span class="sxs-lookup"><span data-stu-id="5c92d-180">An instance of the permanent consumer class.</span></span>
-   <span data-ttu-id="5c92d-181">Ein Filter, der die Abfrage für Ereignisse enthält.</span><span class="sxs-lookup"><span data-stu-id="5c92d-181">A filter that contains the query for events.</span></span>
-   <span data-ttu-id="5c92d-182">Eine Verknüpfung zwischen dem Consumer und dem Filter.</span><span class="sxs-lookup"><span data-stu-id="5c92d-182">A link between the consumer and the filter.</span></span>

<span data-ttu-id="5c92d-183">Weitere Informationen finden Sie [unter empfangen von Ereignissen zu allen Zeit](--filtertoconsumerbinding.md)Punkten.</span><span class="sxs-lookup"><span data-stu-id="5c92d-183">For more information, see [Receiving Events At All Times](--filtertoconsumerbinding.md).</span></span>

<span data-ttu-id="5c92d-184">WMI bietet mehrere permanente Consumer.</span><span class="sxs-lookup"><span data-stu-id="5c92d-184">WMI supplies several permanent consumers.</span></span> <span data-ttu-id="5c92d-185">Die Consumerklassen und das COM-Objekt, das den Code enthält, sind vorinstalliert.</span><span class="sxs-lookup"><span data-stu-id="5c92d-185">The consumer classes and COM object containing the code are preinstalled.</span></span> <span data-ttu-id="5c92d-186">Beispielsweise können Sie eine Instanz der [**activescripteventconsumer**](activescripteventconsumer.md) -Klasse erstellen und konfigurieren, um ein Skript auszuführen, wenn ein Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="5c92d-186">For example, you can create and configure an instance of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class to run a script when an event occurs.</span></span> <span data-ttu-id="5c92d-187">Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="5c92d-187">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="5c92d-188">Ein Beispiel für die Verwendung von **activescripteventconsumer** finden Sie unter [Ausführen eines Skripts auf der Grundlage eines Ereignisses](running-a-script-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="5c92d-188">For an example of using **ActiveScriptEventConsumer**, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md).</span></span>

<span data-ttu-id="5c92d-189">Im folgenden Verfahren wird beschrieben, wie ein dauerhafter Ereignisconsumer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5c92d-189">The following procedure describes how to create a permanent event consumer.</span></span>

<span data-ttu-id="5c92d-190">**So erstellen Sie einen permanenten Ereignisconsumer**</span><span class="sxs-lookup"><span data-stu-id="5c92d-190">**To create a permanent event consumer**</span></span>

1.  <span data-ttu-id="5c92d-191">[Registrieren Sie den Ereignis Anbieter](registering-a-provider.md) bei dem Namespace, den Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c92d-191">[Register the event provider](registering-a-provider.md) with the namespace that you are using.</span></span>

    <span data-ttu-id="5c92d-192">Einige Ereignis Anbieter können nur einen bestimmten Namespace verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c92d-192">Some event providers can only use a specific namespace.</span></span> <span data-ttu-id="5c92d-193">[**\_ \_ Instancecreationevent**](--instancecreationevent.md) ist beispielsweise ein System internes Ereignis, das vom Win32- [Anbieter](/windows/desktop/CIMWin32Prov/win32-provider) unterstützt wird und standardmäßig mit dem \\ root \\ CIMV2-Namespace registriert wird.</span><span class="sxs-lookup"><span data-stu-id="5c92d-193">For example, [**\_\_InstanceCreationEvent**](--instancecreationevent.md) is an intrinsic event that is supported by the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider) and is registered by default with the \\root\\cimv2 namespace.</span></span>

    > [!Note]  
    > <span data-ttu-id="5c92d-194">Sie können die **eventnamespace** -Eigenschaft des [**\_ \_ eventfilters**](--eventfilter.md) verwenden, die in der Registrierung verwendet wird, um ein Cross-Namespace-Abonnement zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5c92d-194">You can use the **EventNamespace** property of the [**\_\_EventFilter**](--eventfilter.md) used in the registration to create a cross-namespace subscription.</span></span> <span data-ttu-id="5c92d-195">Weitere Informationen finden Sie unter [Implementieren von Abonnements für permanente Namespace-Ereignisse](implementing-cross-namespace-permanent-event-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="5c92d-195">For more information, see [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span></span>

     

2.  <span data-ttu-id="5c92d-196">[Registrieren Sie den ereignishandleranbieter](registering-an-event-consumer-provider.md) bei dem Namespace, in dem sich Ereignis Klassen befinden.</span><span class="sxs-lookup"><span data-stu-id="5c92d-196">[Register the event consumer provider](registering-an-event-consumer-provider.md) with the namespace where event classes are located.</span></span>

    <span data-ttu-id="5c92d-197">WMI verwendet einen Ereignisconsumeranbieter, um einen permanenten Ereignisconsumer zu finden.</span><span class="sxs-lookup"><span data-stu-id="5c92d-197">WMI uses an event consumer provider to find an event consumer that is permanent.</span></span> <span data-ttu-id="5c92d-198">Der permanente Ereignisconsumer ist die Anwendung, die von WMI beim Empfang eines Ereignisses gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5c92d-198">The permanent event consumer is the application that WMI starts when an event is received.</span></span> <span data-ttu-id="5c92d-199">Um Ereignisconsumer zu registrieren, erstellen Anbieter Instanzen von [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="5c92d-199">To register event consumer, providers create instances of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span></span>

3.  <span data-ttu-id="5c92d-200">Erstellen Sie eine Instanz der-Klasse, die den dauerhaften Ereignisconsumer darstellt, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="5c92d-200">Create an instance of the class that represents the permanent event consumer you want to use.</span></span>

    <span data-ttu-id="5c92d-201">Ereignisconsumerklassen werden von der [**\_ \_ eventconsumer**](--eventconsumer.md)-Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5c92d-201">Event consumer classes are derived from the class [**\_\_EventConsumer**](--eventconsumer.md).</span></span> <span data-ttu-id="5c92d-202">Legen Sie die Eigenschaften fest, die die ereignisconsumerinstanz benötigt.</span><span class="sxs-lookup"><span data-stu-id="5c92d-202">Set the properties that the event consumer instance requires.</span></span>

4.  <span data-ttu-id="5c92d-203">Registrieren Sie den Consumer mit com mithilfe des **regsvr32** -Hilfsprogramms.</span><span class="sxs-lookup"><span data-stu-id="5c92d-203">Register the consumer with COM by using the **regsvr32** utility.</span></span>
5.  <span data-ttu-id="5c92d-204">Erstellen Sie eine Instanz der Ereignis Filterklasse [**\_ \_ EventFilter**](--eventfilter.md).</span><span class="sxs-lookup"><span data-stu-id="5c92d-204">Create an instance of the event filter class [**\_\_EventFilter**](--eventfilter.md).</span></span>

    <span data-ttu-id="5c92d-205">Legen Sie die erforderlichen Felder für die Ereignis Filter Instanz fest.</span><span class="sxs-lookup"><span data-stu-id="5c92d-205">Set the required fields for the event filter instance.</span></span> <span data-ttu-id="5c92d-206">Die erforderlichen Felder für [**\_ \_ EventFilter**](--eventfilter.md) sind " **Name**", " **QueryLanguage**" und " **Query**".</span><span class="sxs-lookup"><span data-stu-id="5c92d-206">The required fields for [**\_\_EventFilter**](--eventfilter.md) are **Name**, **QueryLanguage**, and **Query**.</span></span> <span data-ttu-id="5c92d-207">Die **Name** -Eigenschaft kann ein beliebiger eindeutiger Name für eine Instanz dieser Klasse sein.</span><span class="sxs-lookup"><span data-stu-id="5c92d-207">The **Name** property can be any unique name for an instance of this class.</span></span> <span data-ttu-id="5c92d-208">Die **QueryLanguage** -Eigenschaft ist immer auf "WQL" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5c92d-208">The **QueryLanguage** property is always set to "WQL".</span></span> <span data-ttu-id="5c92d-209">Die **Query** -Eigenschaft ist eine Zeichenfolge, die eine Ereignis Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="5c92d-209">The **Query** property is a string that contains an event query.</span></span> <span data-ttu-id="5c92d-210">Ein Ereignis wird generiert, wenn die Abfrage eines permanenten Ereignisconsumers fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="5c92d-210">An event is generated when a permanent event consumer's query fails.</span></span> <span data-ttu-id="5c92d-211">Die Quelle des Ereignisses ist WinMgmt, die Ereignis-ID ist 10, und der Ereignistyp ist Fehler.</span><span class="sxs-lookup"><span data-stu-id="5c92d-211">The event's source is WinMgmt, the event ID is 10, and the event type is Error.</span></span>

6.  <span data-ttu-id="5c92d-212">Erstellen Sie eine Instanz der [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) -Klasse, um einen logischen Ereignisconsumer einem Ereignis Filter zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5c92d-212">Create an instance of the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class to associate a logical event consumer with an event filter.</span></span>

    <span data-ttu-id="5c92d-213">WMI verwendet eine Zuordnung, um den Ereignisconsumer zu finden, der dem Ereignis zugeordnet ist, das den im Ereignis Filter angegebenen Kriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="5c92d-213">WMI uses an association to find the event consumer associated with the event that matches the criteria specified in the event filter.</span></span> <span data-ttu-id="5c92d-214">WMI verwendet den Ereignisconsumeranbieter, um zu starten, um die Anwendung für die permanente Ereignisconsumer zu finden</span><span class="sxs-lookup"><span data-stu-id="5c92d-214">WMI uses the event consumer provider to find the permanent event consumer application to start.</span></span>

 

 
