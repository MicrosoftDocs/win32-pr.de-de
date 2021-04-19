---
description: Asynchrone Ereignis Benachrichtigung ist eine Technik, mit der eine Anwendung Ereignisse ständig überwachen kann, ohne die Systemressourcen zu überwachen.
ms.assetid: 69ec8ead-9073-4689-bc66-5134728ab147
ms.tgt_platform: multiple
title: Empfangen von asynchronen Ereignis Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d883908475c796a6bcf31895f2928345541c940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364055"
---
# <a name="receiving-asynchronous-event-notifications"></a><span data-ttu-id="c2f03-103">Empfangen von asynchronen Ereignis Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="c2f03-103">Receiving Asynchronous Event Notifications</span></span>

<span data-ttu-id="c2f03-104">Asynchrone Ereignis Benachrichtigung ist eine Technik, mit der eine Anwendung Ereignisse ständig überwachen kann, ohne die Systemressourcen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="c2f03-104">Asynchronous event notification is a technique that allows an application to constantly monitor events without monopolizing system resources.</span></span> <span data-ttu-id="c2f03-105">Für asynchrone Ereignis Benachrichtigungen gelten die gleichen Sicherheitseinschränkungen wie für andere asynchrone Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="c2f03-105">Asynchronous event notifications have the same security limitations that other asynchronous calls have.</span></span> <span data-ttu-id="c2f03-106">Sie können stattdessen semisynchrone Aufrufe durchführen.</span><span class="sxs-lookup"><span data-stu-id="c2f03-106">You can make semisynchronous calls instead.</span></span> <span data-ttu-id="c2f03-107">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c2f03-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="c2f03-108">Die Warteschlange für asynchrone Ereignisse, die an einen Client weitergeleitet werden, ist möglicherweise sehr groß.</span><span class="sxs-lookup"><span data-stu-id="c2f03-108">The queue of asynchronous events routed to a client has the potential to grow exceptionally large.</span></span> <span data-ttu-id="c2f03-109">Daher implementiert WMI eine systemweite Richtlinie, um zu vermeiden, dass nicht genügend Arbeitsspeicher verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c2f03-109">Therefore, WMI implements a system-wide policy to avoid running out of memory.</span></span> <span data-ttu-id="c2f03-110">WMI verlangsamt Ereignisse oder löscht Ereignisse aus der Warteschlange, wenn die Warteschlange eine bestimmte Größe überschreitet.</span><span class="sxs-lookup"><span data-stu-id="c2f03-110">WMI either slows down events, or starts dropping events from the queue when the queue grows past a certain size.</span></span>

<span data-ttu-id="c2f03-111">WMI verwendet die Eigenschaften [**lowgrenzoldonevents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) und [**highgrenzoldonevents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) der [**Win32 \_ wmisetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) -Klasse, um Grenzwerte für die Vermeidung von nicht genügend Arbeitsspeicher festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c2f03-111">WMI uses the [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) and [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) properties of the [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) class to set limits on out-of-memory avoidance.</span></span> <span data-ttu-id="c2f03-112">Der Minimalwert gibt an, wann WMI mit der Verlangsamung der Ereignis Benachrichtigung beginnen soll, und der Höchstwert gibt an, wann Ereignisse gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c2f03-112">The minimum value indicates when WMI should start slowing event notification, and the maximum value indicates when to start dropping events.</span></span> <span data-ttu-id="c2f03-113">Die Standardwerte für die niedrigen und hohen Schwellenwerte sind 1 Million (10 MB) und 2 Millionen (20 MB).</span><span class="sxs-lookup"><span data-stu-id="c2f03-113">The default values for the low and high thresholds are 1000000 (10 MB) and 2000000 (20 MB).</span></span> <span data-ttu-id="c2f03-114">Außerdem können Sie die [**maxwaitonevents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) -Eigenschaft so festlegen, dass Sie die Zeitspanne beschreibt, die WMI warten soll, bevor Ereignisse gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="c2f03-114">In addition, you can set the [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) property to describe the amount of time WMI should wait before dropping events.</span></span> <span data-ttu-id="c2f03-115">Der Standardwert für **maxwaitonevents** ist 2000 oder 2 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="c2f03-115">The default value for **MaxWaitOnEvents** is 2000, or 2 seconds.</span></span>

## <a name="receiving-asynchronous-event-notifications-in-vbscript"></a><span data-ttu-id="c2f03-116">Empfangen von asynchronen Ereignis Benachrichtigungen in VBScript</span><span class="sxs-lookup"><span data-stu-id="c2f03-116">Receiving Asynchronous Event Notifications in VBScript</span></span>

<span data-ttu-id="c2f03-117">Die Skript Aufrufe für den Empfang von Ereignis Benachrichtigungen sind im Wesentlichen identisch mit allen asynchronen Aufrufen mit denselben Sicherheitsproblemen.</span><span class="sxs-lookup"><span data-stu-id="c2f03-117">The scripting calls to receive event notifications are essentially the same as all asynchronous calls with the same security issues.</span></span> <span data-ttu-id="c2f03-118">Weitere Informationen finden Sie unter [Erstellen eines asynchronen Aufrufes mit VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="c2f03-118">For more information, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="c2f03-119">**So empfangen Sie asynchrone Ereignis Benachrichtigungen in VBScript**</span><span class="sxs-lookup"><span data-stu-id="c2f03-119">**To receive asynchronous event notifications in VBScript**</span></span>

1.  <span data-ttu-id="c2f03-120">Erstellen Sie ein Sink-Objekt, indem Sie [WScript. CreateObject](/previous-versions//xzysf6hc(v=vs.85)) aufrufen und die ProgID von "WbemScripting" und den Objekttyp von " [**Swap-Sink**](swbemsink.md)" angeben.</span><span class="sxs-lookup"><span data-stu-id="c2f03-120">Create a sink object by calling [WScript.CreateObject](/previous-versions//xzysf6hc(v=vs.85)) and specifying the progid of "WbemScripting" and the object type of [**SWbemSink**](swbemsink.md).</span></span> <span data-ttu-id="c2f03-121">Das sink-Objekt empfängt die Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="c2f03-121">The sink object receives the notifications.</span></span>
2.  <span data-ttu-id="c2f03-122">Schreiben Sie eine Unterroutine für jedes Ereignis, das Sie verarbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="c2f03-122">Write a subroutine for each event you want to handle.</span></span> <span data-ttu-id="c2f03-123">In der folgenden Tabelle sind die [**slibemsink**](swbemsink.md) -Ereignisse aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2f03-123">The following table lists the [**SWbemSink**](swbemsink.md) events.</span></span>

    

    | <span data-ttu-id="c2f03-124">Ereignis</span><span class="sxs-lookup"><span data-stu-id="c2f03-124">Event</span></span>                                            | <span data-ttu-id="c2f03-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c2f03-125">Meaning</span></span>                                                                                                                         |
    |--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="c2f03-126">**Onobjectready**</span><span class="sxs-lookup"><span data-stu-id="c2f03-126">**OnObjectReady**</span></span>](swbemsink-onobjectready.md) | <span data-ttu-id="c2f03-127">Meldet die Rückgabe eines Objekts an die Senke.</span><span class="sxs-lookup"><span data-stu-id="c2f03-127">Reports the returns of an object to the sink.</span></span> <span data-ttu-id="c2f03-128">Bei Verwendung dieses Aufrufes wird jedes Mal ein Objekt zurückgegeben, bis der Vorgang beendet ist.</span><span class="sxs-lookup"><span data-stu-id="c2f03-128">Using this call returns one object each time until the operation is complete.</span></span>     |
    | [<span data-ttu-id="c2f03-129">**OnCompleted**</span><span class="sxs-lookup"><span data-stu-id="c2f03-129">**OnCompleted**</span></span>](swbemsink-oncompleted.md)     | <span data-ttu-id="c2f03-130">Meldet den Abschluss eines asynchronen Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="c2f03-130">Reports when an asynchronous call is complete.</span></span> <span data-ttu-id="c2f03-131">Dieses Ereignis tritt nie auf, wenn der Vorgang unbegrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="c2f03-131">This event never occurs if the operation is indefinite.</span></span>                          |
    | [<span data-ttu-id="c2f03-132">**Onobjectput**</span><span class="sxs-lookup"><span data-stu-id="c2f03-132">**OnObjectPut**</span></span>](swbemsink-onobjectput.md)     | <span data-ttu-id="c2f03-133">Meldet den Abschluss eines asynchronen Put-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c2f03-133">Reports the completion of an asynchronous put operation.</span></span> <span data-ttu-id="c2f03-134">Dieses Ereignis gibt den Objekt Pfad der-Instanz oder der gespeicherten-Klasse zurück.</span><span class="sxs-lookup"><span data-stu-id="c2f03-134">This event returns the object path of the instance or the saved class.</span></span> |
    | [<span data-ttu-id="c2f03-135">**OnProgress**</span><span class="sxs-lookup"><span data-stu-id="c2f03-135">**OnProgress**</span></span>](swbemsink-onprogress.md)       | <span data-ttu-id="c2f03-136">Meldet den Status eines asynchronen aufrulaufs, der gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2f03-136">Reports the status of an asynchronous call that is in progress.</span></span> <span data-ttu-id="c2f03-137">Nicht alle Anbieter unterstützen zwischenfortschritts Berichte.</span><span class="sxs-lookup"><span data-stu-id="c2f03-137">Not all providers support interim progress reports.</span></span>             |
    | [<span data-ttu-id="c2f03-138">**Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="c2f03-138">**Cancel**</span></span>](swbemsink-cancel.md)               | <span data-ttu-id="c2f03-139">Bricht alle ausstehenden asynchronen Vorgänge ab, die dieser Objekt Senke zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c2f03-139">Cancels all of the outstanding asynchronous operations associated with this object sink.</span></span>                                        |

    

     

<span data-ttu-id="c2f03-140">Im folgenden VBScript-Codebeispiel wird das Löschen von Prozessen mit einem 10 Sekunden-Abruf Intervall benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="c2f03-140">The following VBScript code example notifies the deletion of processes with a 10 second polling interval.</span></span> <span data-ttu-id="c2f03-141">In diesem Skript behandelt die Unterroutine-Senke \_ onobjectready das Ereignis vorkommen.</span><span class="sxs-lookup"><span data-stu-id="c2f03-141">In this script, the subroutine SINK\_OnObjectReady handles the event occurrence.</span></span> <span data-ttu-id="c2f03-142">Im Beispiel hat das sink-Objekt den Namen "Sink", aber Sie können dieses Objekt bei der Auswahl benennen.</span><span class="sxs-lookup"><span data-stu-id="c2f03-142">In the example, the sink object is named "Sink", however you can name this object as you choose.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, _
    "SELECT * FROM __InstanceDeletionEvent" _
    & " WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'"


WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "__InstanceDeletionEvent event has occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="receiving-asynchronous-event-notifications-in-c"></a><span data-ttu-id="c2f03-143">Empfangen von asynchronen Ereignis Benachrichtigungen in C++</span><span class="sxs-lookup"><span data-stu-id="c2f03-143">Receiving Asynchronous Event Notifications in C++</span></span>

<span data-ttu-id="c2f03-144">Um eine asynchrone Benachrichtigung auszuführen, erstellen Sie nur einen separaten Thread, um Ereignisse von Windows-Verwaltungsinstrumentation (WMI) zu überwachen und zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c2f03-144">To perform asynchronous notification, you create a separate thread solely to monitor and receive events from Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="c2f03-145">Wenn dieser Thread eine Nachricht empfängt, benachrichtigt der Thread Ihre Hauptanwendung.</span><span class="sxs-lookup"><span data-stu-id="c2f03-145">When that thread receives a message, the thread notifies your main application.</span></span>

<span data-ttu-id="c2f03-146">Indem Sie einen separaten Thread zuweisen, gestatten Sie Ihrem Hauptprozess das Ausführen anderer Aktivitäten, während Sie auf das Eintreffen eines Ereignisses warten.</span><span class="sxs-lookup"><span data-stu-id="c2f03-146">By dedicating a separate thread, you permit your main process to perform other activities while waiting for an event to arrive.</span></span> <span data-ttu-id="c2f03-147">Die asynchrone Übermittlung von Benachrichtigungen verbessert die Leistung, bietet jedoch möglicherweise weniger Sicherheit als Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="c2f03-147">Asynchronous delivery of notifications improves performance but may provide less security than you want.</span></span> <span data-ttu-id="c2f03-148">In C++ haben Sie die Möglichkeit, die [**iwbemunsecuagentpartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) -Schnittstelle zu verwenden oder Zugriffs Überprüfungen für Sicherheits Deskriptoren auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c2f03-148">In C++, you have the option of using the [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) interface or performing access checks on security descriptors.</span></span> <span data-ttu-id="c2f03-149">Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="c2f03-149">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="c2f03-150">**So richten Sie asynchrone Ereignis Benachrichtigungen ein**</span><span class="sxs-lookup"><span data-stu-id="c2f03-150">**To set up asynchronous event notifications**</span></span>

1.  <span data-ttu-id="c2f03-151">Bevor Sie asynchrone Benachrichtigungen initialisieren, stellen Sie sicher, dass die Parameter zur Vermeidung von nicht genügend Arbeitsspeicher in [**Win32- \_ wmisetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting)korrekt festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="c2f03-151">Before initializing any asynchronous notifications, ensure your out-of-memory avoidance parameters are set correctly in [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting).</span></span>

2.  <span data-ttu-id="c2f03-152">Bestimmen Sie, welche Art von Ereignissen Sie empfangen möchten.</span><span class="sxs-lookup"><span data-stu-id="c2f03-152">Determine what kind of events you want to receive.</span></span>

    <span data-ttu-id="c2f03-153">WMI unterstützt systeminterne und extrinsische Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="c2f03-153">WMI supports intrinsic and extrinsic events.</span></span> <span data-ttu-id="c2f03-154">Ein System internes Ereignis ist ein von WMI vordefiniertes Ereignis, wohingegen ein extrinsisches Ereignis ein Ereignis ist, das von einem Drittanbieter definiert wird.</span><span class="sxs-lookup"><span data-stu-id="c2f03-154">An intrinsic event is an event predefined by WMI, whereas an extrinsic event is an event defined by a third party provider.</span></span> <span data-ttu-id="c2f03-155">Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="c2f03-155">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="c2f03-156">Im folgenden Verfahren wird beschrieben, wie asynchrone Ereignis Benachrichtigungen in C++ empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="c2f03-156">The following procedure describes how to receive asynchronous event notifications in C++.</span></span>

<span data-ttu-id="c2f03-157">**So empfangen Sie asynchrone Ereignis Benachrichtigungen in C++**</span><span class="sxs-lookup"><span data-stu-id="c2f03-157">**To receive asynchronous event notifications in C++**</span></span>

1.  <span data-ttu-id="c2f03-158">Richten Sie Ihre Anwendung mit Aufrufen der Funktionen [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ein.</span><span class="sxs-lookup"><span data-stu-id="c2f03-158">Set up your application with calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions.</span></span>

    <span data-ttu-id="c2f03-159">Durch den Aufruf von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) wird com initialisiert, während [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) WMI die Berechtigung zum Aufrufen in den consumerprozess erteilt.</span><span class="sxs-lookup"><span data-stu-id="c2f03-159">Calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) initializes COM, while [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) grants WMI the permission to call into the process of the consumer.</span></span> <span data-ttu-id="c2f03-160">Die **CoInitializeEx** -Funktion erteilt Ihnen außerdem die Möglichkeit, eine Multithread-Anwendung zu programmieren, die für die asynchrone Benachrichtigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c2f03-160">The **CoInitializeEx** function also grants you the ability to program a multithreaded application, which is necessary for asynchronous notification.</span></span> <span data-ttu-id="c2f03-161">Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="c2f03-161">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

    <span data-ttu-id="c2f03-162">Der Code in diesem Thema erfordert die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="c2f03-162">The code in this topic requires the following references and \#include statements to compile correctly.</span></span>

    ```C++
    #define _WIN32_DCOM
    #include <iostream>
    using namespace std;
    #include <wbemidl.h>
    ```

    

    <span data-ttu-id="c2f03-163">Im folgenden Codebeispiel wird beschrieben, wie der temporäre Ereignisconsumer mit Aufrufen von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="c2f03-163">The following code example describes how to set up the temporary event consumer with calls to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    ```C++
    void main(int argc, char **argv)
    {
        HRESULT hr = 0;
        hr = CoInitializeEx (0, COINIT_MULTITHREADED);
        hr = CoInitializeSecurity (NULL, 
           -1, 
           NULL, 
           NULL,   
           RPC_C_AUTHN_LEVEL_NONE, 
           RPC_C_IMP_LEVEL_IMPERSONATE, 
           NULL,
           EOAC_NONE,
           NULL); 

        if (FAILED(hr))
        {
           CoUninitialize();
           cout << "Failed to initialize security. Error code = 0x"
               << hex << hr << endl;
           return;
        }

    // ...
    }
    ```

    

2.  <span data-ttu-id="c2f03-164">Erstellen Sie ein Sink-Objekt über die [**iwbemubjectsink**](iwbemobjectsink.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c2f03-164">Create a sink object through the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="c2f03-165">WMI verwendet zum Senden von Ereignis Benachrichtigungen und zum Melden des Status für einen asynchronen Vorgang oder eine Ereignis Benachrichtigung " [**iwbemubjectsink**](iwbemobjectsink.md) ".</span><span class="sxs-lookup"><span data-stu-id="c2f03-165">WMI uses [**IWbemObjectSink**](iwbemobjectsink.md) to send event notifications and to report status on an asynchronous operation or event notification.</span></span>

3.  <span data-ttu-id="c2f03-166">Registrieren Sie Ihren Ereignisconsumer durch einen Aufruf der [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c2f03-166">Register your event consumer with a call to the [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method.</span></span>

    <span data-ttu-id="c2f03-167">Stellen Sie sicher, dass der *presponsehandler* -Parameter auf das sink-Objekt verweist, das im vorherigen Schritt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c2f03-167">Make sure that the *pResponseHandler* parameter points to the sink object created in the preceding step.</span></span>

    <span data-ttu-id="c2f03-168">Der Zweck der Registrierung besteht darin, nur die erforderlichen Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c2f03-168">The purpose of registration is to receive only the required notifications.</span></span> <span data-ttu-id="c2f03-169">Das empfangen überflüssiger Benachrichtigungen verschwendet Verarbeitungs-und Übermittlungs Zeit. und verwendet nicht die Filterungs Fähigkeit von WMI, um das volle Potenzial zu haben.</span><span class="sxs-lookup"><span data-stu-id="c2f03-169">Receiving superfluous notifications wastes processing and delivery time; and does not use the filtering ability of WMI to the fullest potential.</span></span>

    <span data-ttu-id="c2f03-170">Ein temporärer Consumer kann jedoch mehr als einen Ereignistyp empfangen.</span><span class="sxs-lookup"><span data-stu-id="c2f03-170">However, a temporary consumer can receive more than one type of event.</span></span> <span data-ttu-id="c2f03-171">In diesem Fall muss ein temporärer Consumer für jeden Ereignistyp separate Aufrufe von [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2f03-171">In this case, a temporary consumer must make separate calls to [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) for each event type.</span></span> <span data-ttu-id="c2f03-172">Ein Consumer benötigt z. b. möglicherweise eine Benachrichtigung, wenn neue Prozesse erstellt werden (ein instanzerstellungs Ereignis oder [**\_ \_ instancecreationevent**](--instancecreationevent.md)) und für Änderungen an bestimmten Registrierungs Schlüsseln (ein Registrierungs Ereignis wie " [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)").</span><span class="sxs-lookup"><span data-stu-id="c2f03-172">For example, a consumer might require notification when new processes are created (an instance creation event or [**\_\_InstanceCreationEvent**](--instancecreationevent.md)) and for changes to certain registry keys (a registry event such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)).</span></span> <span data-ttu-id="c2f03-173">Daher führt der Consumer einen Aufruf an [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) aus, um sich für instanzerstellungsereignisse und einen weiteren Aufruf von **ExecNotificationQueryAsync** zu registrieren, um Registrierungs Ereignisse zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="c2f03-173">Therefore, the consumer makes one call to [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) to register for instance creation events and another call to **ExecNotificationQueryAsync** to register for registry events.</span></span>

    <span data-ttu-id="c2f03-174">Wenn Sie einen Ereignisconsumer erstellen, der sich für mehrere Ereignisse registriert, sollten Sie das Registrieren mehrerer Klassen mit der gleichen Senke vermeiden.</span><span class="sxs-lookup"><span data-stu-id="c2f03-174">If you choose to create an event consumer that registers for multiple events, you should avoid registering multiple classes with the same sink.</span></span> <span data-ttu-id="c2f03-175">Verwenden Sie stattdessen eine separate Senke für jede Klasse des registrierten Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="c2f03-175">Instead, use a separate sink for each class of registered event.</span></span> <span data-ttu-id="c2f03-176">Eine dedizierte Senke vereinfacht die Verarbeitung und unterstützt die Wartung, sodass Sie eine Registrierung abbrechen können, ohne dass sich dies auf die anderen auswirkt.</span><span class="sxs-lookup"><span data-stu-id="c2f03-176">Having a dedicated sink simplifies processing and aids in maintenance, allowing you to cancel one registration without affecting the others.</span></span>

4.  <span data-ttu-id="c2f03-177">Führen Sie alle notwendigen Aktivitäten in Ihrem Ereignisconsumer aus.</span><span class="sxs-lookup"><span data-stu-id="c2f03-177">Perform any necessary activities in your event consumer.</span></span>

    <span data-ttu-id="c2f03-178">Dieser Schritt sollte den größten Teil Ihres Codes enthalten und solche Aktivitäten wie das Anzeigen von Ereignissen für eine Benutzeroberfläche einschließen.</span><span class="sxs-lookup"><span data-stu-id="c2f03-178">This step should contain most of your code and include such activities as displaying events to a user interface.</span></span>

5.  <span data-ttu-id="c2f03-179">Wenn Sie den Vorgang abgeschlossen haben, heben Sie die Registrierung für den temporären Ereignisconsumer mit einem Befehl des [**IWbemServices:: cancelasynccall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) -Ereignisses auf.</span><span class="sxs-lookup"><span data-stu-id="c2f03-179">When finished, unregister the temporary event consumer with a call to the [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) event.</span></span>

    <span data-ttu-id="c2f03-180">Löschen Sie das sink-Objekt nicht, bis der Verweis Zähler des Objekts Null erreicht wird, unabhängig davon, ob der Rückruf von [**cancelasynccall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) erfolgreich ist oder fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="c2f03-180">Regardless of whether the call to [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) succeeds or fails, do not delete the sink object until the object reference count reaches zero.</span></span> <span data-ttu-id="c2f03-181">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c2f03-181">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 
