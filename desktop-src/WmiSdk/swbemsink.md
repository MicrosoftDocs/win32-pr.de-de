---
description: Das slibemsink-Objekt wird von Client Anwendungen implementiert, um die Ergebnisse von asynchronen Vorgängen und Ereignis Benachrichtigungen zu empfangen.
ms.assetid: a90777ef-fa26-4bfb-b196-c083a0c92a29
ms.tgt_platform: multiple
title: Taubemsink-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink
- ISWbemSinkEvents
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b8007b7387a09e31f49dbc833f657bc959ee11e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353204"
---
# <a name="swbemsink-object"></a><span data-ttu-id="ef4cf-103">Swap-Objekt</span><span class="sxs-lookup"><span data-stu-id="ef4cf-103">SWbemSink object</span></span>

<span data-ttu-id="ef4cf-104">Das **slibemsink** -Objekt wird von Client Anwendungen implementiert, um die Ergebnisse von asynchronen Vorgängen und Ereignis Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-104">The **SWbemSink** object is implemented by client applications to receive the results of asynchronous operations and event notifications.</span></span> <span data-ttu-id="ef4cf-105">Um einen asynchronen-aufzurufen, müssen Sie eine Instanz eines " **taubemsink** "-Objekts erstellen und als *objwbemsink* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-105">To make an asynchronous call, you must create an instance of an **SWbemSink** object and pass it as the *ObjWbemSink* parameter.</span></span> <span data-ttu-id="ef4cf-106">Die Ereignisse in der Implementierung von " **taubemsink** " werden ausgelöst, wenn Status oder Ergebnisse zurückgegeben werden oder wenn der-Vorgang beendet ist.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-106">The events in your implementation of **SWbemSink** are triggered when status or results are returned, or when the call is complete.</span></span> <span data-ttu-id="ef4cf-107">Der VBScript-Befehl zum Erstellen von **Objekten** erstellt dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-107">The VBScript **CreateObject** call creates this object.</span></span>

## <a name="members"></a><span data-ttu-id="ef4cf-108">Member</span><span class="sxs-lookup"><span data-stu-id="ef4cf-108">Members</span></span>

<span data-ttu-id="ef4cf-109">Das **taubemsink** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ef4cf-109">The **SWbemSink** object has these types of members:</span></span>

-   [<span data-ttu-id="ef4cf-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="ef4cf-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ef4cf-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="ef4cf-111">Methods</span></span>

<span data-ttu-id="ef4cf-112">Das **taubemsink** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-112">The **SWbemSink** object has these methods.</span></span>



| <span data-ttu-id="ef4cf-113">Methode</span><span class="sxs-lookup"><span data-stu-id="ef4cf-113">Method</span></span>                             | <span data-ttu-id="ef4cf-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef4cf-114">Description</span></span>                                                                        |
|:-----------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="ef4cf-115">**Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="ef4cf-115">**Cancel**</span></span>](swbemsink-cancel.md) | <span data-ttu-id="ef4cf-116">Bricht alle asynchronen Vorgänge ab, die dieser Senke zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-116">Cancels all asynchronous operations that are associated with this sink.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef4cf-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef4cf-117">Remarks</span></span>

<span data-ttu-id="ef4cf-118">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-118">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="ef4cf-119">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-119">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="ef4cf-120">Um die Risiken auszuschließen, verwenden Sie entweder die semisynchrone Kommunikation oder die synchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-120">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="ef4cf-121">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ef4cf-121">For more information, see [Calling a Method](calling-a-method.md).</span></span>

### <a name="events"></a><span data-ttu-id="ef4cf-122">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ef4cf-122">Events</span></span>

<span data-ttu-id="ef4cf-123">Sie können Unterroutinen implementieren, die aufgerufen werden, wenn Ereignisse ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-123">You can implement subroutines to be called when events are triggered.</span></span> <span data-ttu-id="ef4cf-124">Wenn Sie z. b. jedes Objekt verarbeiten möchten, das von einem asynchronen Abfrage Vorgang zurückgegeben wird, z. b. [**SWbemServices.Execqueryasync**](swbemservices-execqueryasync.md), erstellen Sie eine Unterroutine mithilfe der Senke, die im asynchronen-Befehl angegeben wird, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-124">For example, if you want to process each object that is returned by an asynchronous query call such as [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), create a subroutine using the sink that is specified in the asynchronous call, as shown in the following example.</span></span>


```VB
Sub SinkName_OnObjectReady(objObject, objAsyncContext)
```



<span data-ttu-id="ef4cf-125">Verwenden Sie die folgende Tabelle als Referenz, um Ereignisse und triggerbeschreibungen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-125">Use the following table as a reference to identify events and trigger descriptions.</span></span>



| <span data-ttu-id="ef4cf-126">Ereignis</span><span class="sxs-lookup"><span data-stu-id="ef4cf-126">Event</span></span>                                            | <span data-ttu-id="ef4cf-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef4cf-127">Description</span></span>                                                             |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="ef4cf-128">**OnCompleted**</span><span class="sxs-lookup"><span data-stu-id="ef4cf-128">**OnCompleted**</span></span>](swbemsink-oncompleted.md)     | <span data-ttu-id="ef4cf-129">Wird ausgelöst, wenn ein asynchroner Vorgang beendet ist.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-129">Triggered when an asynchronous operation is complete.</span></span>                   |
| [<span data-ttu-id="ef4cf-130">**Onobjectput**</span><span class="sxs-lookup"><span data-stu-id="ef4cf-130">**OnObjectPut**</span></span>](swbemsink-onobjectput.md)     | <span data-ttu-id="ef4cf-131">Wird ausgelöst, wenn ein asynchroner Put-Vorgang beendet ist.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-131">Triggered when an asynchronous Put operation is complete.</span></span>               |
| [<span data-ttu-id="ef4cf-132">**Onobjectready**</span><span class="sxs-lookup"><span data-stu-id="ef4cf-132">**OnObjectReady**</span></span>](swbemsink-onobjectready.md) | <span data-ttu-id="ef4cf-133">Wird ausgelöst, wenn ein von einem asynchronen-Befehl bereitgestelltes Objekt verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-133">Triggered when an object provided by an asynchronous call is available.</span></span> |
| [<span data-ttu-id="ef4cf-134">**OnProgress**</span><span class="sxs-lookup"><span data-stu-id="ef4cf-134">**OnProgress**</span></span>](swbemsink-onprogress.md)       | <span data-ttu-id="ef4cf-135">Wird ausgelöst, um den Status eines asynchronen Vorgangs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-135">Triggered to provide the status of a asynchronous operation.</span></span>            |



 

<span data-ttu-id="ef4cf-136">**Asynchrones Abrufen von Ereignisprotokoll Statistiken**</span><span class="sxs-lookup"><span data-stu-id="ef4cf-136">**Asynchronously Retrieving Event Log Statistics**</span></span>

<span data-ttu-id="ef4cf-137">WMI unterstützt sowohl asynchrone als auch semisynchrone Skripts.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-137">WMI supports both asynchronous and semi-synchronous scripts.</span></span> <span data-ttu-id="ef4cf-138">Beim Abrufen von Ereignissen aus den Ereignisprotokollen werden diese Daten von asynchronen Skripts häufig viel schneller abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-138">When retrieving events from the event logs, asynchronous scripts often retrieve this data much faster.</span></span>

<span data-ttu-id="ef4cf-139">In einem asynchronen Skript wird eine Abfrage ausgegeben, und die Steuerung wird sofort an das Skript zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-139">In an asynchronous script, a query is issued and control is immediately returned to the script.</span></span> <span data-ttu-id="ef4cf-140">Die Abfrage wird weiterhin in einem separaten Thread verarbeitet, während das Skript sofort die zurückgegebenen Informationen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-140">The query continues to process on a separate thread while the script begins to immediately act on the information that is returned.</span></span> <span data-ttu-id="ef4cf-141">Asynchrone Skripts sind ereignisgesteuert: jedes Mal, wenn ein Ereignisdaten Satz abgerufen wird, wird das onobjectready-Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-141">Asynchronous scripts are event driven: each time an event record is retrieved, the OnObjectReady event is fired.</span></span> <span data-ttu-id="ef4cf-142">Wenn die Abfrage abgeschlossen ist, wird das onabgeschlossene-Ereignis ausgelöst, und das Skript kann basierend auf der Tatsache fortgesetzt werden, dass alle verfügbaren Datensätze zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-142">When the query has completed, the OnCompleted event will fire, and the script can continue based on the fact that all the available records have been returned.</span></span>

<span data-ttu-id="ef4cf-143">In einem semisynchronen Skript wird im Gegensatz dazu eine Abfrage ausgegeben, und das Skript fügt dann eine große Menge an abgerufenen Informationen in die Warteschlange ein, bevor es darauf reagiert.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-143">In a semi-synchronous script, by contrast, a query is issued and the script then queues a large amount of retrieved information before acting upon it.</span></span> <span data-ttu-id="ef4cf-144">Bei vielen-Objekten ist die semisynchrone Verarbeitung angemessen. Wenn Sie z. b. ein Festplattenlaufwerk nach seinen Eigenschaften Abfragen, kann es zwischen dem Zeitpunkt, zu dem die Abfrage ausgegeben wird, und dem Zeitpunkt, zu dem die Informationen zurückgegeben und verarbeitet werden, nur eine Sekunde geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-144">For many objects, semi-synchronous processing is adequate; for example, when querying a disk drive for its properties, there might be only a split second between the time the query is issued and the time the information is returned and acted upon.</span></span> <span data-ttu-id="ef4cf-145">Der Grund dafür ist, dass die Menge der zurückgegebenen Informationen relativ klein ist.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-145">This is due in large part to the fact that the amount of information returned is relatively small.</span></span>

<span data-ttu-id="ef4cf-146">Beim Abfragen eines Ereignis Protokolls kann jedoch das Intervall zwischen dem Zeitpunkt, zu dem die Abfrage ausgegeben wird, und dem Zeitpunkt, zu dem ein semisynchrones Skript die Rückgabe der Informationen abschließen kann, Stunden dauern.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-146">When querying an event log, however, the interval between the time the query is issued and the time that a semi-synchronous script can finish returning and acting on the information can take hours.</span></span> <span data-ttu-id="ef4cf-147">Darüber hinaus ist für das Skript möglicherweise nicht genügend Arbeitsspeicher verfügbar, und ein Fehler tritt auf, bevor er abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-147">On top of that, the script might run out of memory and fail on its own before completing.</span></span>

<span data-ttu-id="ef4cf-148">Bei Ereignisprotokollen mit einer großen Anzahl von Datensätzen kann der Unterschied in der Verarbeitungszeit beträchtlich sein.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-148">For event logs with a large number of records, the difference in processing time can be considerable.</span></span> <span data-ttu-id="ef4cf-149">Auf einem Windows 2000-basierten Testcomputer mit 2.000 Datensätzen im Ereignisprotokoll hat eine semisynchrone Abfrage, bei der alle Ereignisse abgerufen und in einem Befehlsfenster angezeigt wurden, 10 Minuten 45 Sekunden gedauert.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-149">On a Windows 2000-based test computer with 2,000 records in the event log, a semi-synchronous query that retrieved all the events and displayed them in a command window took 10 minutes 45 seconds.</span></span> <span data-ttu-id="ef4cf-150">Eine asynchrone Abfrage, die denselben Vorgang ausgeführt hat, hat eine Minute 54 Sekunden gedauert.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-150">An asynchronous query that performed the same operation took one minute 54 seconds.</span></span>

## <a name="examples"></a><span data-ttu-id="ef4cf-151">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef4cf-151">Examples</span></span>

<span data-ttu-id="ef4cf-152">Das folgende VBScript fragt die Ereignisprotokolle für alle Datensätze asynchron ab.</span><span class="sxs-lookup"><span data-stu-id="ef4cf-152">The following VBScript asynchronously queries the event logs for all records.</span></span>


```VB
Const POPUP_DURATION = 10
Const OK_BUTTON = 0
Set objWSHShell = Wscript.CreateObject("Wscript.Shell")
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
objWMIService.InstancesOfAsync objSink, "Win32_NTLogEvent"
errReturn = objWshShell.Popup("Retrieving events", POPUP_DURATION, _
"Event Retrieval", OK_BUTTON)
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
 WScript.Echo "Asynchronous operation is done."
End Sub
Sub SINK_OnObjectReady(objEvent, objAsyncContext)
 Wscript.Echo "Category: " & objEvent.Category
 Wscript.Echo "Computer Name: " & objEvent.ComputerName
 Wscript.Echo "Event Code: " & objEvent.EventCode
 Wscript.Echo "Message: " & objEvent.Message
 Wscript.Echo "Record Number: " & objEvent.RecordNumber
 Wscript.Echo "Source Name: " & objEvent.SourceName
 Wscript.Echo "Time Written: " & objEvent.TimeWritten
 Wscript.Echo "Event Type: " & objEvent.Type
 Wscript.Echo "User: " & objEvent.User
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ef4cf-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef4cf-153">Requirements</span></span>



| <span data-ttu-id="ef4cf-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef4cf-154">Requirement</span></span> | <span data-ttu-id="ef4cf-155">Wert</span><span class="sxs-lookup"><span data-stu-id="ef4cf-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef4cf-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef4cf-156">Minimum supported client</span></span><br/> | <span data-ttu-id="ef4cf-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef4cf-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef4cf-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef4cf-158">Minimum supported server</span></span><br/> | <span data-ttu-id="ef4cf-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef4cf-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef4cf-160">Header</span><span class="sxs-lookup"><span data-stu-id="ef4cf-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef4cf-161"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef4cf-161"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef4cf-162">IDL</span><span class="sxs-lookup"><span data-stu-id="ef4cf-162">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef4cf-163"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef4cf-163"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="ef4cf-164">DLL</span><span class="sxs-lookup"><span data-stu-id="ef4cf-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef4cf-165"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef4cf-165"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ef4cf-166">CLSID</span><span class="sxs-lookup"><span data-stu-id="ef4cf-166">CLSID</span></span><br/>                    | <span data-ttu-id="ef4cf-167">CLSID- \_ Swap-senbemsink</span><span class="sxs-lookup"><span data-stu-id="ef4cf-167">CLSID\_SWbemSink</span></span><br/> <span data-ttu-id="ef4cf-168">CLSID- \_ Austausch Vorgänge</span><span class="sxs-lookup"><span data-stu-id="ef4cf-168">CLSID\_SWbemSinkEvents</span></span><br/>                           |
| <span data-ttu-id="ef4cf-169">IID</span><span class="sxs-lookup"><span data-stu-id="ef4cf-169">IID</span></span><br/>                      | <span data-ttu-id="ef4cf-170">IID \_ iswbemsink</span><span class="sxs-lookup"><span data-stu-id="ef4cf-170">IID\_ISWbemSink</span></span><br/> <span data-ttu-id="ef4cf-171">IID \_ iswbemsinkevents</span><span class="sxs-lookup"><span data-stu-id="ef4cf-171">IID\_ISWbemSinkEvents</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="ef4cf-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef4cf-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef4cf-173">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="ef4cf-173">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




