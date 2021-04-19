---
description: Durch das Ausführen eines asynchronen Aufrufens an eine WMI-Methode oder eine Anbieter Methode kann ein Skript weiter ausgeführt werden, während Objekte zu einem "Swap"-Objekt zurückkehren und von Methoden wie z. b. "Swap. onobjectready" behandelt werden.
ms.assetid: 61f401d9-c874-472d-8dd3-7cf9d7f20a12
ms.tgt_platform: multiple
title: Erstellen eines asynchronen Aufrufes mit VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c2b3ec0c1bd771f59a4e456cb8e57c3bb3e9e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362256"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a><span data-ttu-id="6fc5b-103">Erstellen eines asynchronen Aufrufes mit VBScript</span><span class="sxs-lookup"><span data-stu-id="6fc5b-103">Making an Asynchronous Call with VBScript</span></span>

<span data-ttu-id="6fc5b-104">Durch das Ausführen eines asynchronen Aufrufens an eine [*WMI-Methode*](gloss-w.md) oder eine [*Anbieter Methode*](gloss-p.md) kann ein Skript weiter ausgeführt werden, während Objekte zu einem " [**Swap**](swbemsink.md) "-Objekt zurückkehren und von Methoden wie z. b. " [**Swap. onobjectready**](swbemsink-onobjectready.md)" behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-104">Making an asynchronous call to a [*WMI method*](gloss-w.md) or a [*provider method*](gloss-p.md) allows a script to continue executing while objects return to an [**SWbemSink**](swbemsink.md) object, and are handled by methods such as [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md).</span></span> <span data-ttu-id="6fc5b-105">Asynchrone Aufrufe werden jedoch nicht empfohlen, da die Daten möglicherweise nicht mit derselben Sicherheitsstufe wie der Aufruf zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-105">However, asynchronous calls are not recommended because the data may not be returned at the same level of security as the call is made.</span></span>

<span data-ttu-id="6fc5b-106">Wenn Sie asynchrone Sink-Aufrufe wie z. b. " [**taubemsink. onobjectready**](swbemsink-onobjectready.md) " verwenden, um zurückgegebene Daten abzurufen, können Sie den folgenden Registrierungs Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-106">When using asynchronous sink calls like [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) to get returned data, you can set the following registry value.</span></span>

<span data-ttu-id="6fc5b-107">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **unsecappaccesscontroldefault**</span><span class="sxs-lookup"><span data-stu-id="6fc5b-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault**</span></span>

<span data-ttu-id="6fc5b-108">Durch Festlegen dieses Registrierungs Werts wird die Authentifizierung der an die Senke zurückgegebenen Datenobjekte sichergestellt.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-108">Setting this registry value ensures authentication of the data objects returned to the sink.</span></span> <span data-ttu-id="6fc5b-109">Wenn **unsecappaccesscontroldefault** auf eins (1) festgelegt ist, führt WMI die Zugriffs Überprüfung der Daten Rückgabe aus.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-109">If **UnsecAppAccessControlDefault** is set to one (1), then WMI performs access checking of the data return.</span></span> <span data-ttu-id="6fc5b-110">Mithilfe von Zugriffs Überprüfungen wird überprüft, ob die Daten aus der richtigen Quelle stammen.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-110">Access checks verify that the data comes from the correct source.</span></span> <span data-ttu-id="6fc5b-111">Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-111">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="6fc5b-112">Asynchrone Methoden, deren Namen mit "Async" enden, \_ werden immer nach dem Aufruf von zurückgegeben, damit ein Programm weiter ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-112">Asynchronous methods with names that end in "Async\_" always return immediately after being called so that a program can continue executing.</span></span> <span data-ttu-id="6fc5b-113">Beispielsweise [**SWbemServices.Execquery**](swbemservices-execquery.md) synchron ist und die Ausführung blockiert, bis alle-Objekte zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-113">For example, [**SWbemServices.ExecQuery**](swbemservices-execquery.md) is synchronous and blocks execution until all of the objects are returned.</span></span> <span data-ttu-id="6fc5b-114">Bei der [**SWbemServices.Execqueryasync**](swbemservices-execqueryasync.md) -Methode handelt es sich um die nicht blockierende asynchrone Version.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-114">The [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) method is the nonblocking asynchronous version.</span></span> <span data-ttu-id="6fc5b-115">Eine sicherere Möglichkeit, **SWbemServices.Execquery** -nicht Blockierung aufzurufen, besteht darin, den-Befehl [*halb synchron*](gloss-s.md)zu machen.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-115">A more secure way to make the call to **SWbemServices.ExecQuery** nonblocking is by making the call [*semisynchronously*](gloss-s.md).</span></span> <span data-ttu-id="6fc5b-116">Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md) -Befehl und [Erstellen eines semisynchronen Aufrufes mit VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="6fc5b-116">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md) and [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="6fc5b-117">Der *IFlags* -Parameter für asynchrone Aufrufe hat immer den Standardwert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6fc5b-117">The *iFlags* parameter for asynchronous calls always defaults to zero (0).</span></span> <span data-ttu-id="6fc5b-118">Asynchrone Methoden stellen keine [**errbewbjectset**](swbemobjectset.md) -Auflistung für die Sink-Unterroutine bereit.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-118">Asynchronous methods do not supply an [**SWbemObjectSet**](swbemobjectset.md) collection to the sink subroutine.</span></span> <span data-ttu-id="6fc5b-119">Stattdessen empfängt die [**slibemsink. onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine in Ihrem Skript oder in der Anwendung jedes Objekt, sobald es bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-119">Instead, the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event subroutine in your script or application receives each object as it is provided.</span></span>

<span data-ttu-id="6fc5b-120">Wenn der ursprüngliche asynchrone Aufruf abgeschlossen ist, ruft er das Ereignis " [**slibemsink. OnComplete**](swbemsink-oncompleted.md) " der Objekt Senke auf und führt den Code aus, den Sie dort platzieren, um das Ergebnis des Aufrufs zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-120">When the original asynchronous call is complete, it calls the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the object sink, and executes the code you place there to process the result of the call.</span></span>

> [!Note]  
> <span data-ttu-id="6fc5b-121">Eine Active Server Seite (ASP) als Skript Host unterstützt keinen asynchronen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-121">An Active Server Page (ASP) as a script host does not support an asynchronous call.</span></span>

 

<span data-ttu-id="6fc5b-122">Im folgenden Verfahren wird beschrieben, wie Sie mithilfe von VBScript einen asynchronen-Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-122">The following procedure describes how to make an asynchronous call by using VBScript.</span></span>

<span data-ttu-id="6fc5b-123">**So führen Sie einen asynchronen Befehl mithilfe von VBScript aus**</span><span class="sxs-lookup"><span data-stu-id="6fc5b-123">**To make an asynchronous call using VBScript**</span></span>

1.  <span data-ttu-id="6fc5b-124">Stellen Sie eine Verbindung mit WMI her, und erhalten Sie ein Objekt " [**Swap Services**](swbemservices.md) "</span><span class="sxs-lookup"><span data-stu-id="6fc5b-124">Connect to WMI and get an [**SWbemServices**](swbemservices.md) object.</span></span>

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  <span data-ttu-id="6fc5b-125">Erstellen Sie die Objekt Senke entweder mithilfe von " [kreateobject](/previous-versions//xzysf6hc(v=vs.85)) " oder (nur für Windows Script Host 2,0) dem Objekttag mit einem Ereignis Attribut, das auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-125">Create the object sink using either [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) or (for Windows Script Host 2.0 only) the OBJECT tag with an events attribute set to **TRUE**.</span></span>

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    <span data-ttu-id="6fc5b-126">Oder</span><span class="sxs-lookup"><span data-stu-id="6fc5b-126">-or-</span></span>

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  <span data-ttu-id="6fc5b-127">Erstellen Sie für jedes Ereignis, das von einem asynchronen Ereignis auslöst werden kann, eine Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-127">Create a subroutine for each event an asynchronous event can trigger.</span></span> <span data-ttu-id="6fc5b-128">Diese Ereignisse werden als Methoden für " [**errbemubject**](swbemobject.md)" definiert.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-128">These events are defined as methods on [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="6fc5b-129">Beispielsweise sendet WMI einen Rückruf an " [**taubemsink. onobjectready**](swbemsink-onobjectready.md) ", wenn jede Instanz zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-129">For example, WMI makes a callback to [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) as each instance returns.</span></span>

    <span data-ttu-id="6fc5b-130">Wenn Sie die Unterroutine erstellen, platzieren Sie Code in der Unterroutine, damit jedes Ereignis beim Empfang verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-130">When you create the subroutine, place code in the subroutine to handle each event when it is received.</span></span>

    ```VB
    Sub SINK_OnCompleted(
          iHResult, 
          objErrorObject, 
          objAsyncContext
          )
        WScript.Echo "Asynchronous operation is done."
    End Sub

    Sub SINK_OnObjectReady(objObject, objAsyncContext)
        WScript.Echo (objObject.Name)
    End Sub
    ```

    

    <span data-ttu-id="6fc5b-131">Überprüfen Sie den *ihresult* -Parameter, der vom [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis zurückgegeben wurde, um zu bestimmen, ob der asynchrone-Rückruf erfolgreich ist oder ob ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-131">Examine the *iHresult* parameter returned by the [**OnCompleted**](swbemsink-oncompleted.md) event to determine whether or not the asynchronous call is successful, or if an error occurred.</span></span> <span data-ttu-id="6fc5b-132">Bei erfolgreicher Ausführung ist der Wert, der im *ihresult* -Parameter übergeben wird, gleich NULL (0).</span><span class="sxs-lookup"><span data-stu-id="6fc5b-132">If successful, the value passed in the *iHresult* parameter is equal to zero (0).</span></span> <span data-ttu-id="6fc5b-133">Jeder andere Wert weist möglicherweise auf einen Fehler hin, und Sie sollten die Werte im Fehler Objekt überprüfen, das im *objerrorobject* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-133">Any other value may indicate an error, and you should check the values in the error object that is returned in the *objErrorObject* parameter.</span></span>

4.  <span data-ttu-id="6fc5b-134">Führen Sie einen asynchronen-Rückruf aus, und übergeben Sie den Namen der Senke im *objwbemsink* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-134">Make an asynchronous call and pass the name of your sink in the *objWbemSink* parameter.</span></span>

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  <span data-ttu-id="6fc5b-135">Führen Sie einen-Rückruf aus, der verhindert, dass das Skript beendet wird, bevor alle Ereignisse empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-135">Make a call that prevents the script from ending before all of the events are received.</span></span> <span data-ttu-id="6fc5b-136">Wenn das Skript mit einer Bildschirm Schnittstelle ausgeführt werden kann, können Sie dazu einen Windows Script Host (WSH)-Befehl verwenden, der `Echo` im folgenden Beispiel gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-136">If your script can run with a screen interface, a simple way to do this is to use a Windows Script Host (WSH) `Echo` command, which is shown in the following example.</span></span>

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    <span data-ttu-id="6fc5b-137">Wenn Sie dieses Skript ausführen, sehen Sie möglicherweise, dass die erste Instanz vor der Nachricht, die auf **Instanzen wartet** , zurückgegeben wird, oder Sie wird nach angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-137">When you execute this script you may see the first instance return before the **Waiting for instances** message or you may see it after.</span></span> <span data-ttu-id="6fc5b-138">Dabei handelt es sich um die Art der asynchronen Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-138">This is the nature of asynchronous processing.</span></span> <span data-ttu-id="6fc5b-139">Wenn Sie das Meldungs Feld **warten auf Instanzen** zu bald schließen, werden möglicherweise nicht alle Instanzen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-139">If you close the **Waiting for instances** message box too soon, you may not see all of the instances.</span></span>

6.  <span data-ttu-id="6fc5b-140">Wenn Sie Ergebnisse aus mehreren verschiedenen asynchronen Aufrufen haben, die zur gleichen Senke zurückkehren, speichern Sie alle notwendigen unterschiedlichen Daten im *objwbemasynccontext* -Kontext Parameter.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-140">If you have results from several different asynchronous calls returning to the same sink, store any necessary distinguishing data in the *objWbemAsyncContext* context parameter.</span></span>

7.  <span data-ttu-id="6fc5b-141">Wenn Sie mit der Senke fertig sind, brechen Sie den asynchronen-Befehl mit der [**Cancel**](swbemsink-cancel.md) -Methode ab.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-141">When finished with the sink, cancel your asynchronous call with the [**Cancel**](swbemsink-cancel.md) method.</span></span>

    ```VB
    objwbemsink.Cancel()
    ```

    

    <span data-ttu-id="6fc5b-142">Die [**Cancel**](swbemsink-cancel.md) -Methode weist WSH an, alle asynchronen Aufrufe abzubrechen, die einem angegebenen Sink-Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-142">The [**Cancel**](swbemsink-cancel.md) method instructs WSH to cancel all of the asynchronous calls associated with a given sink object.</span></span> <span data-ttu-id="6fc5b-143">Daher empfiehlt es sich, separate senken für asynchrone Vorgänge zu verwenden, die unabhängig sein müssen.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-143">Thus, you may want to use separate sinks for asynchronous operations that must be independent.</span></span>

8.  <span data-ttu-id="6fc5b-144">Geben Sie das sink-Objekt frei, indem Sie das sink-Objekt zuweisen `Nothing` .</span><span class="sxs-lookup"><span data-stu-id="6fc5b-144">Release the sink object by assigning the sink object to `Nothing`.</span></span>

    ```VB
    set objwbemsink= Nothing
    ```

    

<span data-ttu-id="6fc5b-145">Das folgende Codebeispiel zeigt eine asynchrone Abfrage für alle Instanzen des [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process) auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-145">The following code example shows an asynchronous query for all the instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) on the local machine.</span></span> <span data-ttu-id="6fc5b-146">Eine semisynchrone Version derselben Methode finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="6fc5b-146">For a semisynchronous version of the same method, see [Calling a Method](calling-a-method.md).</span></span>


```VB
' Create an object sink
set oSink = WScript.CreateObject("wbemscripting.swbemsink","sink_")
' Connect to WMI and the cimv2 namespace, and obtain
' an SWbemServices object
set oSvc = GetObject("winmgmts:root\cimv2")

bdone = false
' Query for all Win32_Process objects
osvc.ExecQueryAsync oSink, "SELECT Name FROM Win32_Process"
' Wait until all instances are returned. 
' The bdone flag prevents the script from exiting until
' the sink.OnCompleted subroutine is executed when
' all the objects are returned.
while not bdone    
    wscript.sleep 1000
wend

' The sink subroutine to handle the OnObjectReady 
' event. This is called as each object returns.
sub sink_OnObjectReady(oInst, octx)
    WScript.Echo "Got Instance: " & oInst.Name
end sub
' The sink subroutine to handle the OnCompleted event.
' This is called when all the objects are returned. 
' The oErr parameter obtains an SWbemLastError object,
' if available from the provider.
sub sink_OnCompleted(HResult, oErr, oCtx)
    WScript.Echo "ExecQueryAsync completed"
    bdone = true
end sub
```



## <a name="related-topics"></a><span data-ttu-id="6fc5b-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6fc5b-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fc5b-148">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="6fc5b-148">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="6fc5b-149">Verwalten der WMI-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="6fc5b-149">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

 
