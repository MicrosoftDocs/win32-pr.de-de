---
description: WMI stellt Methoden in der com-API und der Skript-API bereit, um Informationen zu erhalten oder Objekte in einem Unternehmenssystem zu bearbeiten.
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: Aufrufen einer WMI-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c327bbf0c4c90ad05d1c5026e3308e5fd8447aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353997"
---
# <a name="calling-a-wmi-method"></a><span data-ttu-id="06552-103">Aufrufen einer WMI-Methode</span><span class="sxs-lookup"><span data-stu-id="06552-103">Calling a WMI Method</span></span>

<span data-ttu-id="06552-104">WMI stellt Methoden in der [com-API](com-api-for-wmi.md) und der [Skript-API](scripting-api-for-wmi.md) bereit, um Informationen zu erhalten oder Objekte in einem Unternehmenssystem zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="06552-104">WMI supplies methods in the [COM API](com-api-for-wmi.md) and the [scripting API](scripting-api-for-wmi.md) to obtain information or manipulate objects in an enterprise system.</span></span> <span data-ttu-id="06552-105">Die WMI-Skript MethodeSWbemServices.Exez. b. [**cquery**](swbemservices-execquery.md) -Abfragen für-Daten.</span><span class="sxs-lookup"><span data-stu-id="06552-105">For example, the WMI scripting method [**SWbemServices.ExecQuery**](swbemservices-execquery.md) queries for data.</span></span> <span data-ttu-id="06552-106">Außerdem verfügen Anbieter über Methoden, die in den von Ihnen registrierten Klassen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="06552-106">Providers also have methods defined in the classes they register.</span></span> <span data-ttu-id="06552-107">Beispiele hierfür sind [**die Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Methoden [**chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) und [**scheduleautochk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) , die vom [Win32-Anbieter](/windows/desktop/CIMWin32Prov/win32-provider)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="06552-107">Examples are the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) methods [**Chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) and [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) supplied by the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider).</span></span>

<span data-ttu-id="06552-108">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="06552-108">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="06552-109">WMI-Methoden im Vergleich zu Anbieter Methoden</span><span class="sxs-lookup"><span data-stu-id="06552-109">WMI Methods Compared to Provider Methods</span></span>](#wmi-methods-compared-to-provider-methods)
-   [<span data-ttu-id="06552-110">Methodenaufruf Modi in WMI</span><span class="sxs-lookup"><span data-stu-id="06552-110">Method-Calling Modes in WMI</span></span>](#method-calling-modes-in-wmi)
    -   [<span data-ttu-id="06552-111">Synchroner Modus</span><span class="sxs-lookup"><span data-stu-id="06552-111">Synchronous Mode</span></span>](#synchronous-mode)
    -   [<span data-ttu-id="06552-112">Asynchroner Modus</span><span class="sxs-lookup"><span data-stu-id="06552-112">Asynchronous Mode</span></span>](#asynchronous-mode)
    -   [<span data-ttu-id="06552-113">Semisynchroner Modus</span><span class="sxs-lookup"><span data-stu-id="06552-113">Semisynchronous Mode</span></span>](#semisynchronous-mode)
-   [<span data-ttu-id="06552-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06552-114">Related topics</span></span>](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a><span data-ttu-id="06552-115">WMI-Methoden im Vergleich zu Anbieter Methoden</span><span class="sxs-lookup"><span data-stu-id="06552-115">WMI Methods Compared to Provider Methods</span></span>

<span data-ttu-id="06552-116">Durch die Verwendung von [*WMI-Methoden*](gloss-w.md) aufrufen in Kombination mit [*Anbieter Methoden*](gloss-p.md) aufrufen können Sie Informationen zu Ihrem Unternehmen abrufen und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="06552-116">By using [*WMI method*](gloss-w.md) calls combined with [*provider method*](gloss-p.md) calls, you can retrieve and manipulate information about your enterprise.</span></span> <span data-ttu-id="06552-117">Weitere Informationen finden Sie unter [Aufrufen einer WMI-Methode](calling-a-wmi-method.md) und [Aufrufen einer Anbieter Methode](calling-a-provider-method.md).</span><span class="sxs-lookup"><span data-stu-id="06552-117">For more information, see [Calling a WMI Method](calling-a-wmi-method.md) and [Calling a Provider Method](calling-a-provider-method.md).</span></span>

<span data-ttu-id="06552-118">Die Methoden des WMI-Skript Objekts " [**errbewbject**](swbemobject.md) " haben einen besonderen Status, da Sie auf jede beliebige WMI-Datenklasse angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="06552-118">The methods of the WMI scripting object [**SWbemObject**](swbemobject.md) have a special status because they can apply to any WMI data class.</span></span> <span data-ttu-id="06552-119">Weitere Informationen finden Sie unter [Skripterstellung mit "Swap](scripting-with-swbemobject.md)".</span><span class="sxs-lookup"><span data-stu-id="06552-119">For more information, see [Scripting with SWbemObject](scripting-with-swbemobject.md).</span></span>

<span data-ttu-id="06552-120">Im folgenden Codebeispiel werden sowohl WMI-als auch Provider-Methoden aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="06552-120">The following code example calls both WMI and provider methods.</span></span>

<span data-ttu-id="06552-121">Die folgenden WMI-und Anbieter Methoden befinden sich in der [Skript-API für WMI](scripting-api-for-wmi.md):</span><span class="sxs-lookup"><span data-stu-id="06552-121">The following WMI and provider methods are located in the [Scripting API for WMI](scripting-api-for-wmi.md):</span></span>

-   <span data-ttu-id="06552-122">**objWMIService.Execquery** Ruft die WMI-Skript Methode [ **SWbemServices.Execquery** auf.](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)</span><span class="sxs-lookup"><span data-stu-id="06552-122">**objWMIService.ExecQuery** calls the WMI scripting method [**SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)</span></span>
-   <span data-ttu-id="06552-123">**objservice. StopService ()** Ruft die Anbieter Methode [ **Win32 \_ Service. Stop Service auf.**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)</span><span class="sxs-lookup"><span data-stu-id="06552-123">**objService.StopService()** calls the provider method [**Win32\_Service.StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)</span></span>

<span data-ttu-id="06552-124">Sie können den Code suchen, der im Abschnitt "Rückgabe Codes" für den [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service)möglicherweise im Abschnitt "Return" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="06552-124">You can look up the code that may appear in "Return" in the Return Codes section for [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```


```PowerShell

$colServices= Get-WmiObject -Class Win32_Service -Filter 'Name = &quot;Alerter&quot;'
foreach ($objService in $colServices)
{
    $objService.StopService()
}
```





## <a name="method-calling-modes-in-wmi"></a><span data-ttu-id="06552-125">Method-Calling Modi in WMI</span><span class="sxs-lookup"><span data-stu-id="06552-125">Method-Calling Modes in WMI</span></span>

<span data-ttu-id="06552-126">Der semisynchrone Aufruf Modus bietet in der Regel das beste Gleichgewicht zwischen Sicherheit und Leistung.</span><span class="sxs-lookup"><span data-stu-id="06552-126">The semisynchronous calling mode usually provides the best balance between security and performance.</span></span>

<span data-ttu-id="06552-127">Weitere Informationen zu den einzelnen möglichen Modi finden Sie in den folgenden Bereichen:</span><span class="sxs-lookup"><span data-stu-id="06552-127">For more information about each of the possible modes, see the following:</span></span>

-   [<span data-ttu-id="06552-128">Synchron</span><span class="sxs-lookup"><span data-stu-id="06552-128">Synchronous</span></span>](#synchronous-mode)
-   [<span data-ttu-id="06552-129">Asynchron</span><span class="sxs-lookup"><span data-stu-id="06552-129">Asynchronous</span></span>](#asynchronous-mode)
-   [<span data-ttu-id="06552-130">Halb synchron</span><span class="sxs-lookup"><span data-stu-id="06552-130">Semisynchronous</span></span>](#semisynchronous-mode)

### <a name="synchronous-mode"></a><span data-ttu-id="06552-131">Synchroner Modus</span><span class="sxs-lookup"><span data-stu-id="06552-131">Synchronous Mode</span></span>

<span data-ttu-id="06552-132">Der synchrone Modus tritt auf, wenn das Programm oder die Skripts angehalten werden, bis der Methoden aufzurufende das Objekt " [**errbewbjectset**](swbemobjectset.md)</span><span class="sxs-lookup"><span data-stu-id="06552-132">Synchronous mode occurs when the program or scripts pauses until the method call returns a [**SWbemObjectSet**](swbemobjectset.md) collection object.</span></span> <span data-ttu-id="06552-133">WMI erstellt diese Auflistung im Arbeitsspeicher, bevor das Auflistungs Objekt an das aufrufende Programm oder Skript zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="06552-133">WMI builds this collection in memory before returning the collection object to the calling program or script.</span></span>

<span data-ttu-id="06552-134">Der synchrone Modus kann sich auf den Computer, auf dem das Programm oder das Skript ausgeführt wird, negativ auf die Programm-oder Skript Leistung auswirken</span><span class="sxs-lookup"><span data-stu-id="06552-134">Synchronous mode can have an adverse effect of program or script performance on the computer running the program or script.</span></span> <span data-ttu-id="06552-135">Beispielsweise kann das synchrone abrufen Tausender Ereignisse aus dem Ereignisprotokoll sehr lange dauern und viel Arbeitsspeicher beanspruchen, da WMI ein Objekt aus jedem Ereignis erstellt und diese Objekte dann in eine Auflistung einfügt, bevor die Auflistung an die-Methode übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="06552-135">For example, synchronously retrieving thousands of events from the event log can take a long time and use a lot of memory because WMI creates an object from each event and then puts those objects into a collection before passing the collection to the method.</span></span>

<span data-ttu-id="06552-136">Sie sollten nur Methoden aufzurufen, die keine großen Datasets im synchronen Modus zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="06552-136">You should only call methods that do not return large data sets in synchronous mode.</span></span> <span data-ttu-id="06552-137">Die folgenden " [**Swap Services**](swbemservices.md) "-Methoden können im synchronen Modus sicher aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="06552-137">The following [**SWbemServices**](swbemservices.md) methods can be safely called in synchronous mode:</span></span>

-   [<span data-ttu-id="06552-138">**Swap Services. Delete**</span><span class="sxs-lookup"><span data-stu-id="06552-138">**SWbemServices.Delete**</span></span>](swbemservices-delete.md)
-   [<span data-ttu-id="06552-139">**SWbemServices.Execmethod**</span><span class="sxs-lookup"><span data-stu-id="06552-139">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
-   [<span data-ttu-id="06552-140">**Austauschdienste. Get**</span><span class="sxs-lookup"><span data-stu-id="06552-140">**SWbemServices.Get**</span></span>](swbemservices-get.md)

<span data-ttu-id="06552-141">Alle "Async"- [**Methoden ohne das**](swbemservices.md) Wort "Async" im Namen können im synchronen Modus aufgerufen werden, indem der Wert " **wbemflagreturneincomplete** " im *IFlags* -Parameter festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="06552-141">Any [**SWbemServices**](swbemservices.md) methods without the word, "Async" in the name can be called in synchronous mode by setting the **wbemFlagReturnWhenComplete** value in the *iFlags* parameter.</span></span>

### <a name="asynchronous-mode"></a><span data-ttu-id="06552-142">Asynchroner Modus</span><span class="sxs-lookup"><span data-stu-id="06552-142">Asynchronous Mode</span></span>

<span data-ttu-id="06552-143">Der asynchrone Modus tritt auf, wenn das Programm oder Skript nach dem Aufrufen der-Methode weiter ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06552-143">Asynchronous mode occurs when the program or script continues to run after calling the method.</span></span> <span data-ttu-id="06552-144">WMI gibt bei der Erstellung jedes Objekts alle Objekte aus der-Methode in ein " [**taubemsink**](swbemsink.md) "-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="06552-144">WMI returns all objects from the method to a [**SWbemSink**](swbemsink.md) object as each object is created.</span></span> <span data-ttu-id="06552-145">Das aufrufende Programm oder Skript muss ein " **slibemsink** "-Objekt und einen " [**slibemsink. onobjectready**](swbemsink-onobjectready.md) "-Ereignishandler aufweisen, um die zurückgegebenen Objekte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="06552-145">The calling program or script must have an **SWbemSink** object and an [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event handler to process the returned objects.</span></span> <span data-ttu-id="06552-146">Weitere Informationen zum Erstellen eines Ereignis Handlers für den asynchronen Modus finden Sie unter [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="06552-146">For more information about creating an event handler for asynchronous mode, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="06552-147">In diesem Modus gibt es nicht die Leistungs-und Ressourcen Einbuße des synchronen Modus, aber der asynchrone Modus kann zu ernsthaften Sicherheitsrisiken führen, da die im " [**Swap**](swbemsink.md) "-Objekt gespeicherten Ergebnisse möglicherweise nicht aus dem aufrufenden Programm oder Skript stammen.</span><span class="sxs-lookup"><span data-stu-id="06552-147">While this mode does not have the performance and resource penalty of synchronous mode, asynchronous mode can create serious security risks because the results stored in the [**SWbemSink**](swbemsink.md) object may not come from the calling program or script.</span></span> <span data-ttu-id="06552-148">WMI senkt die Authentifizierungs Ebene für das Objekt " **taubemsink** ", bis die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="06552-148">WMI lowers the authentication level on the **SWbemSink** object until the method succeeds.</span></span> <span data-ttu-id="06552-149">Weitere Informationen zum mindern dieser Sicherheitsrisiken finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="06552-149">For more information about how to mitigate these security risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="06552-150">Mit dem Wort "Async" angefügte Methoden sind Methoden für den asynchronen Modus.</span><span class="sxs-lookup"><span data-stu-id="06552-150">Methods appended with the word Async are methods for asynchronous mode.</span></span> <span data-ttu-id="06552-151">Die folgenden Methoden sind asynchrone Aufrufe:</span><span class="sxs-lookup"><span data-stu-id="06552-151">The following methods are asynchronous calls:</span></span>

-   [<span data-ttu-id="06552-152">**Swap Services. associatorsofasync**</span><span class="sxs-lookup"><span data-stu-id="06552-152">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
-   [<span data-ttu-id="06552-153">**"Swap Services. deleteasync"**</span><span class="sxs-lookup"><span data-stu-id="06552-153">**SWbemServices.DeleteAsync**</span></span>](swbemservices-deleteasync.md)
-   [<span data-ttu-id="06552-154">**SWbemServices.Execmethodasync**</span><span class="sxs-lookup"><span data-stu-id="06552-154">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
-   [<span data-ttu-id="06552-155">**SWbemServices.Execnotificationqueryasync**</span><span class="sxs-lookup"><span data-stu-id="06552-155">**SWbemServices.ExecNotificationQueryAsync**</span></span>](swbemservices-execnotificationqueryasync.md)
-   [<span data-ttu-id="06552-156">**CqueryasyncSWbemServices.Exe**</span><span class="sxs-lookup"><span data-stu-id="06552-156">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)
-   [<span data-ttu-id="06552-157">**Swap Services. instancesofasync**</span><span class="sxs-lookup"><span data-stu-id="06552-157">**SWbemServices.InstancesOfAsync**</span></span>](swbemservices-instancesofasync.md)
-   [<span data-ttu-id="06552-158">**"Swap Services. referencestoasync"**</span><span class="sxs-lookup"><span data-stu-id="06552-158">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="06552-159">**Austausch Services. subclassesofasync**</span><span class="sxs-lookup"><span data-stu-id="06552-159">**SWbemServices.SubclassesOfAsync**</span></span>](swbemservices-subclassesofasync.md)

<span data-ttu-id="06552-160">Weitere Informationen zum asynchronen Modus finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="06552-160">For more information about asynchronous mode, see:</span></span>

-   [<span data-ttu-id="06552-161">Erstellen eines asynchronen Aufrufes mit C++</span><span class="sxs-lookup"><span data-stu-id="06552-161">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
-   [<span data-ttu-id="06552-162">Erstellen eines asynchronen Aufrufes mit VBScript</span><span class="sxs-lookup"><span data-stu-id="06552-162">Making an Asynchronous Call with VBScript</span></span>](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a><span data-ttu-id="06552-163">Semisynchroner Modus</span><span class="sxs-lookup"><span data-stu-id="06552-163">Semisynchronous Mode</span></span>

<span data-ttu-id="06552-164">Der semisynchrone Modus ähnelt dem asynchronen Modus, da das Programm oder Skript nach dem Aufrufen der-Methode weiterhin ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06552-164">Semisynchronous mode is similar to asynchronous mode in that the program or script continues to run after calling the method.</span></span> <span data-ttu-id="06552-165">Im semisynchronen Modus ruft WMI die Objekte im Hintergrund ab, während das Skript oder Programm weiterhin ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06552-165">In semisynchronous mode, WMI retrieves the objects in the background as your script or program continues to run.</span></span> <span data-ttu-id="06552-166">WMI gibt jedes Objekt zurück, das direkt nach dem Erstellen des-Objekts an die Aufruf Methode zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="06552-166">WMI returns each object returned to the calling method right after the object is created.</span></span>

<span data-ttu-id="06552-167">Da das Objekt von WMI verwaltet wird, ist der semisynchrone Modus sicherer als der asynchrone Modus.</span><span class="sxs-lookup"><span data-stu-id="06552-167">Because WMI manages the object, semisynchronous mode is more secure than asynchronous mode.</span></span> <span data-ttu-id="06552-168">Wenn Sie jedoch den semisynchronen Modus mit mehr als 1.000 Instanzen verwenden, kann der Instanzabruf die verfügbaren Ressourcen monopolisieren, wodurch die Leistung des Programms oder Skripts und des Computers mithilfe des Programms oder Skripts beeinträchtigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="06552-168">However, if you use semisynchronous mode with more than 1,000 instances, instance retrieval can monopolize the available resources, which can degrade the performance of the program or script and the computer using the program or script.</span></span> <span data-ttu-id="06552-169">Jedes-Objekt benötigt die erforderlichen Ressourcen, bis der Arbeitsspeicher freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="06552-169">Each object takes up the necessary resources until the memory is released.</span></span>

<span data-ttu-id="06552-170">Um diese Bedingung zu umgehen, können Sie die-Methode mit dem *IFlags* -Parameter festlegen, der mit den **wbemFlagForwardOnly** -und **wbemFlagReturnImmediately** -Flags festgelegt ist, um WMI anzuweisen, ein vorwärts geschütztes-Objekt vom Typ " [**Swap**](swbemobjectset.md)-only" zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="06552-170">To work around this condition, you can call the method with the *iFlags* parameter set with the **wbemFlagForwardOnly** and **wbemFlagReturnImmediately** flags to instruct WMI to return a forward-only [**SWbemObjectSet**](swbemobjectset.md).</span></span> <span data-ttu-id="06552-171">Ein vorwärts gesteuerter " **errbewbjectset** " entfernt das von einem großen Dataset verursachte Leistungsproblem, indem der Arbeitsspeicher freigegeben wird, nachdem das Objekt aufgezählt wurde.</span><span class="sxs-lookup"><span data-stu-id="06552-171">A forward-only **SWbemObjectSet** eliminates the performance problem caused by a large data set by releasing the memory after the object is enumerated.</span></span>

<span data-ttu-id="06552-172">Jede [**Methode, die nicht im**](swbemservices.md) synchronen oder asynchronen Modus aufgerufen werden kann, wird im semisynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="06552-172">Any [**SWbemServices**](swbemservices.md) method that cannot be called in either synchronous or asynchronous mode is called in semisynchronous mode.</span></span>

<span data-ttu-id="06552-173">Die folgenden Methoden werden im semisynchronen Modus aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="06552-173">The following methods are called in semisynchronous mode:</span></span>

-   [<span data-ttu-id="06552-174">**"Taubemservices. associatorsof"**</span><span class="sxs-lookup"><span data-stu-id="06552-174">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
-   [<span data-ttu-id="06552-175">**Swap Services. Delete**</span><span class="sxs-lookup"><span data-stu-id="06552-175">**SWbemServices.Delete**</span></span>](swbemservices-delete.md)
-   [<span data-ttu-id="06552-176">**SWbemServices.Execmethod**</span><span class="sxs-lookup"><span data-stu-id="06552-176">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
-   [<span data-ttu-id="06552-177">**CnotificationquerySWbemServices.Exe**</span><span class="sxs-lookup"><span data-stu-id="06552-177">**SWbemServices.ExecNotificationQuery**</span></span>](swbemservices-execnotificationquery.md)
-   [<span data-ttu-id="06552-178">**CquerySWbemServices.Exe**</span><span class="sxs-lookup"><span data-stu-id="06552-178">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
-   [<span data-ttu-id="06552-179">**Austauschdienste. Get**</span><span class="sxs-lookup"><span data-stu-id="06552-179">**SWbemServices.Get**</span></span>](swbemservices-get.md)
-   [<span data-ttu-id="06552-180">**Swap Services. InstancesOf**</span><span class="sxs-lookup"><span data-stu-id="06552-180">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)
-   [<span data-ttu-id="06552-181">**"Swap Services. referencesto"**</span><span class="sxs-lookup"><span data-stu-id="06552-181">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="06552-182">**Swap Services. SubclassesOf**</span><span class="sxs-lookup"><span data-stu-id="06552-182">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)
-   [<span data-ttu-id="06552-183">**Swap Services. Put**</span><span class="sxs-lookup"><span data-stu-id="06552-183">**SWbemServices.Put**</span></span>](swbemservicesex-put.md)

<span data-ttu-id="06552-184">Weitere Informationen zum semisynchronen Modus finden Sie unter [Erstellen eines semisynchronen Aufrufes mit C++](making-a-semisynchronous-call-with-c--.md) und [Erstellen eines semisynchronen Aufrufes mit VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="06552-184">For more information about semisynchronous mode, see [Making a Semisynchronous Call with C++](making-a-semisynchronous-call-with-c--.md) and [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06552-185">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06552-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06552-186">Verbessern der enumerationsleistung</span><span class="sxs-lookup"><span data-stu-id="06552-186">Improving Enumeration Performance</span></span>](improving-enumeration-performance.md)
</dt> <dt>

[<span data-ttu-id="06552-187">Skripterstellung mit "errbemuject"</span><span class="sxs-lookup"><span data-stu-id="06552-187">Scripting with SWbemObject</span></span>](scripting-with-swbemobject.md)
</dt> <dt>

[<span data-ttu-id="06552-188">**Wbemflagenum**</span><span class="sxs-lookup"><span data-stu-id="06552-188">**WbemFlagEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 
