---
description: Wie bei allen Anwendungen empfängt WMI Fehlercodes vom Windows-Betriebssystem.
ms.assetid: f54b8e7c-c531-47d5-bab8-780652b94555
ms.tgt_platform: multiple
title: Abrufen eines Fehlercodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c42dbd160ef6412c332e2da2c01f6590e10966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345244"
---
# <a name="retrieving-an-error-code"></a><span data-ttu-id="cfd61-103">Abrufen eines Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="cfd61-103">Retrieving an Error Code</span></span>

<span data-ttu-id="cfd61-104">Wie bei allen Anwendungen empfängt WMI Fehlercodes vom Windows-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="cfd61-104">As with all applications, WMI receives error codes from the Windows operating system.</span></span>

<span data-ttu-id="cfd61-105">Wenn Sie einen Fehlercode erhalten, haben Sie die folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="cfd61-105">When you receive an error code, you have the following options:</span></span>

-   <span data-ttu-id="cfd61-106">Sehen Sie sich das Ereignisprotokoll an.</span><span class="sxs-lookup"><span data-stu-id="cfd61-106">Look at the event log.</span></span>

    <span data-ttu-id="cfd61-107">WMI sendet Fehlermeldungen an den Ereignisprotokoll Dienst, der die Ereignisprotokolle prüft, um die Ursache eines Fehlers zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="cfd61-107">WMI sends error messages to the Event Log service that checks the event logs to help determine the cause of an error.</span></span> <span data-ttu-id="cfd61-108">Sie können die Klassen, die vom [Ereignisprotokoll](/previous-versions/windows/desktop/eventlogprov/event-log-provider) Anbieter unterstützt werden, für den programmgesteuerten Zugriff auf Ereignisprotokolle verwenden.</span><span class="sxs-lookup"><span data-stu-id="cfd61-108">You can use the classes that the [Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider) provider supports to access event logs programmatically.</span></span>

-   <span data-ttu-id="cfd61-109">Rufen Sie den Fehlercode in der Regel ab.</span><span class="sxs-lookup"><span data-stu-id="cfd61-109">Retrieve the error code normally.</span></span>

    <span data-ttu-id="cfd61-110">WMI unterstützt die Standardverfahren zum Abrufen von Fehlercodes, die com-Fehlercodes für C++ sind, und systemeigene Fehler Objekte wie [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85))oder [**Swap-LastError**](swbemlasterror.md) , wenn der Anbieter Fehlerinformationen liefert.</span><span class="sxs-lookup"><span data-stu-id="cfd61-110">WMI supports the standard techniques to retrieve error codes, which are COM error codes for C++, and native error objects, such as [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)), or [**SWbemLastError**](swbemlasterror.md) if the provider supplies error information.</span></span>

<span data-ttu-id="cfd61-111">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="cfd61-111">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="cfd61-112">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="cfd61-112">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="cfd61-113">Behandeln eines Fehlers mit VBScript</span><span class="sxs-lookup"><span data-stu-id="cfd61-113">Handling an Error with VBScript</span></span>](#handling-an-error-with-vbscript)
-   [<span data-ttu-id="cfd61-114">Behandeln eines Fehlers mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="cfd61-114">Handling an Error Using C++</span></span>](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a><span data-ttu-id="cfd61-115">Behandeln eines Fehlers mit VBScript</span><span class="sxs-lookup"><span data-stu-id="cfd61-115">Handling an Error with VBScript</span></span>

<span data-ttu-id="cfd61-116">Wenn ein WMI-Aufrufe über die Skript-API für WMI einen Fehler verursacht, haben Sie die folgenden Optionen für den Zugriff auf die Fehlerinformationen:</span><span class="sxs-lookup"><span data-stu-id="cfd61-116">If a call to WMI through the Scripting API for WMI causes an error, you have the following options to access the error information:</span></span>

-   <span data-ttu-id="cfd61-117">Verwenden Sie Native Fehler Mechanismen der Skriptsprache, z. b. Wenn Sie in VBScript das [Err-Objekt (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) verwenden, um die Fehlerbehandlung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cfd61-117">Use native error mechanisms of the scripting language, for example, in VBScript use [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) to support error handling.</span></span>
-   <span data-ttu-id="cfd61-118">Erstellen Sie ein " [**taubemlasterror**](swbemlasterror.md) "-Objekt, um einen Fehlerbericht zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cfd61-118">Create an [**SWbemLastError**](swbemlasterror.md) object to get an error report.</span></span>

<span data-ttu-id="cfd61-119">Das folgende Skript zeigt die Verwendung des nativen [Err-Objekts (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cfd61-119">The following script shows use of the native [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span></span> <span data-ttu-id="cfd61-120">Wenn ein falscher Wert für das Prozess handle angegeben ist, wird ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="cfd61-120">When an incorrect value for the process handle is given, an error is generated.</span></span>


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> <span data-ttu-id="cfd61-121">Die **Description** -Eigenschaft des [Err-Objekts (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) ist beim Herstellen einer Verbindung mit WMI über den Moniker "winmgmts:" leer.</span><span class="sxs-lookup"><span data-stu-id="cfd61-121">The **Description** property of [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) is empty when connecting to WMI through the "winmgmts:" moniker.</span></span> <span data-ttu-id="cfd61-122">Wenn Sie jedoch mithilfe von " [**Swap-Locator**](swbemlocator.md)" eine Verbindung herstellen, ist die Beschreibung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cfd61-122">However, if you connect using [**SWbemLocator**](swbemlocator.md), the description is available.</span></span>
>
> <span data-ttu-id="cfd61-123">In der folgenden Tabelle werden die Eigenschaften des [Err-Objekts (VBScript)](/previous-versions//sbf5ze0e(v=vs.85))aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cfd61-123">The following table lists the properties of [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span></span>
>
> 
>
> | <span data-ttu-id="cfd61-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cfd61-124">Property</span></span>                   | <span data-ttu-id="cfd61-125">Enthält</span><span class="sxs-lookup"><span data-stu-id="cfd61-125">Contains</span></span>                                                       |
> |----------------------------|----------------------------------------------------------------|
> | <span data-ttu-id="cfd61-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cfd61-126">**Description**</span></span><br/> | <span data-ttu-id="cfd61-127">Lokalisierte, lesbare Beschreibung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="cfd61-127">Localized, human-readable description of the error.</span></span><br/> |
> | <span data-ttu-id="cfd61-128">**Number**</span><span class="sxs-lookup"><span data-stu-id="cfd61-128">**Number**</span></span><br/>      | <span data-ttu-id="cfd61-129">**HRESULT** , das von der Skript-API für WMI zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="cfd61-129">**HRESULT** returned by the Scripting API for WMI.</span></span><br/>  |
> | <span data-ttu-id="cfd61-130">**Quelle**</span><span class="sxs-lookup"><span data-stu-id="cfd61-130">**Source**</span></span><br/>      | <span data-ttu-id="cfd61-131">Identifiziert das Objekt, das den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="cfd61-131">Identifies the object that raised the error.</span></span><br/>        |
>
> 
>
>  

 

<span data-ttu-id="cfd61-132">Das folgende Skript veranschaulicht die Verwendung eines " [**Swap**](swbemlasterror.md) "-Objekts, um ausführliche Fehlerinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cfd61-132">The following script shows use of an [**SWbemLastError**](swbemlasterror.md) object to obtain detailed error information.</span></span> <span data-ttu-id="cfd61-133">Beachten Sie, dass nicht alle Anbieter Informationen für " **taubemlasterror**" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cfd61-133">Note that not all providers supply information to **SWbemLastError**.</span></span> <span data-ttu-id="cfd61-134">Weitere Informationen zu Fehlercodes in Skripts finden Sie unter [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="cfd61-134">For more information about error codes in script, see [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a><span data-ttu-id="cfd61-135">Behandeln eines Fehlers mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="cfd61-135">Handling an Error Using C++</span></span>

<span data-ttu-id="cfd61-136">Eine WMI-Client Anwendung kann entweder com-oder WMI-spezifische Fehler empfangen.</span><span class="sxs-lookup"><span data-stu-id="cfd61-136">A WMI client application can receive either COM-specific or WMI-specific errors.</span></span> <span data-ttu-id="cfd61-137">Die com-Fehler entsprechen der Struktur von com-Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="cfd61-137">The COM errors conform to the structure of COM error codes.</span></span> <span data-ttu-id="cfd61-138">Alle WMI-Schnittstellen können einen com-spezifischen Fehler außer den Schnittstellen [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)und [**iwbemqualifierset**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cfd61-138">All WMI interfaces can return a COM-specific error except the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject), and [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interfaces.</span></span> <span data-ttu-id="cfd61-139">Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="cfd61-139">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span> <span data-ttu-id="cfd61-140">Auf den Referenzseiten der WMI-Schnittstellen werden die entsprechenden WMI-Fehlercodes im Abschnitt Fehlercodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cfd61-140">The reference pages of the WMI interfaces list the appropriate WMI error codes in the Error Codes section.</span></span>

<span data-ttu-id="cfd61-141">Eine Client Anwendung muss die com-Standards zum Überprüfen von Status-und Fehlerrückgabe Codes einhalten.</span><span class="sxs-lookup"><span data-stu-id="cfd61-141">A client application must follow the COM standards for checking status and error return codes.</span></span> <span data-ttu-id="cfd61-142">Der Hauptunterschied, den Sie auswählen müssen, ist, ob Sie den Fehlercode von einem synchronen, semisynchronen oder asynchronen aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="cfd61-142">The main difference you must choose is whether you wish to retrieve the error code from a synchronous, semisynchronous, or asynchronous call.</span></span>

<span data-ttu-id="cfd61-143">**So greifen Sie mit C++ auf synchrone und semisynchrone Fehlermeldungen zu**</span><span class="sxs-lookup"><span data-stu-id="cfd61-143">**To access synchronous and semisynchronous error messages using C++**</span></span>

1.  <span data-ttu-id="cfd61-144">Rufen Sie die Fehlerinformationen mit einem Aufrufen der com-Funktion [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) ab.</span><span class="sxs-lookup"><span data-stu-id="cfd61-144">Retrieve the error information with a call to the [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) COM function.</span></span>

    <span data-ttu-id="cfd61-145">Stellen Sie sicher, dass [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) unmittelbar nach einer Schnittstellen Methode aufgerufen wird, die auf einen Fehler hinweist.</span><span class="sxs-lookup"><span data-stu-id="cfd61-145">Make sure to call [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) immediately after an interface method indicates an error.</span></span> <span data-ttu-id="cfd61-146">Dies schließt alle [**iwbemcallresult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) -Methoden ein, die Sie bei der Verarbeitung eines semisynchronen Prozesses aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cfd61-146">This includes any of the [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) methods you call while processing a semisynchronous process.</span></span>

2.  <span data-ttu-id="cfd61-147">Überprüfen Sie das zurückgegebene com-Fehler Objekt mit einem Rückruf der [**IErrorInterface:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode.</span><span class="sxs-lookup"><span data-stu-id="cfd61-147">Examine the returned COM error object with a call to the [**IErrorInterface::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method.</span></span>

    <span data-ttu-id="cfd61-148">Stellen Sie sicher, dass IID \_ wbemclassobject für den *riid* -Parameter im [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Befehl angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cfd61-148">Make sure to specify IID\_WbemClassObject for the *riid* parameter in the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) call.</span></span> <span data-ttu-id="cfd61-149">Die **QueryInterface** -Methode gibt eine Instanz einer WMI-Klasse zurück, in der Regel [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="cfd61-149">The **QueryInterface** method returns an instance of a WMI class, typically [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

<span data-ttu-id="cfd61-150">WMI stellt das Fehler Objekt nicht über [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) für einen asynchronen-Befehl bereit, da es keine Möglichkeit gibt, zu wissen, wann oder in welchem Thread der asynchrone-Befehl aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cfd61-150">WMI does not deliver the error object through [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) for an asynchronous call because there is no way to know when, or on which thread the asynchronous call occurred.</span></span> <span data-ttu-id="cfd61-151">Daher kann Ihr Code nur bestimmte Fehler verarbeiten oder den Fehler des Aufrufes über com übergeben.</span><span class="sxs-lookup"><span data-stu-id="cfd61-151">Therefore, your code can only handle specific errors or pass the call failure through COM.</span></span>

> [!Note]  
> <span data-ttu-id="cfd61-152">Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cfd61-152">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="cfd61-153">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="cfd61-153">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="cfd61-154">**So greifen Sie mithilfe von C++ auf asynchrone Fehlermeldungen zu**</span><span class="sxs-lookup"><span data-stu-id="cfd61-154">**To access asynchronous error messages using C++**</span></span>

-   <span data-ttu-id="cfd61-155">Rufen Sie das com-Fehler Objekt aus der Implementierung von [**iwbemubjectsink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus)ab.</span><span class="sxs-lookup"><span data-stu-id="cfd61-155">Retrieve the COM error object from your implementation of [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span>

    <span data-ttu-id="cfd61-156">Der folgende Pseudo Code zeigt eine typische Implementierung der Fehlerbehandlung für eine Client Anwendung.</span><span class="sxs-lookup"><span data-stu-id="cfd61-156">The following pseudocode shows a typical error handling implementation for a client application.</span></span>

    ```C++
    HRESULT hRes = SomeMethod;

    // Check for specific error and status codes.
    if (hRes == WBEM_E_NOT_FOUND)
    {
    // Processing to handle specific error code
    }
    else if hRes == WBEM_S_DUPLICATE_OBJECTS
    {
    // All other cases, including errors specific to COM
    }
    else if (FAILED(hRes))
    {

    }
    ```

    

 

