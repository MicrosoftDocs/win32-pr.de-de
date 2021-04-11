---
description: Führt eine Methode aus, die von einem Methoden Anbieter exportiert wird.
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: SWbemServices.Execmethod-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethod
- ISWbemServices.ExecMethod
- ISWbemServices.ExecMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c95bc3b0fa85d7c682f9ffd2436439da9a05763f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042364"
---
# <a name="swbemservicesexecmethod-method"></a><span data-ttu-id="eb1e8-103">SWbemServices.Execmethod-Methode</span><span class="sxs-lookup"><span data-stu-id="eb1e8-103">SWbemServices.ExecMethod method</span></span>

<span data-ttu-id="eb1e8-104">Die **ExecMethod** -Methode des [**Swap Services**](swbemservices.md) -Objekts führt eine Methode aus, die von einem Methoden Anbieter exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-104">The **ExecMethod** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="eb1e8-105">Diese Methode wird blockiert, während die Methode, die an den entsprechenden Anbieter weitergeleitet wird, ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-105">This method blocks while the method that is forwarded to the appropriate provider executes.</span></span> <span data-ttu-id="eb1e8-106">Die Informationen und der Status werden dann zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-106">The information and status are then returned.</span></span> <span data-ttu-id="eb1e8-107">Der Anbieter implementiert die-Methode anstelle von WMI.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-107">The provider, rather than WMI, implements the method.</span></span>

<span data-ttu-id="eb1e8-108">Diese Methode wird im synchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-108">This method is called in the synchronous mode.</span></span> <span data-ttu-id="eb1e8-109">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e8-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="eb1e8-110">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e8-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb1e8-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb1e8-111">Syntax</span></span>


```VB
objOutParams = .ExecMethod( _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="eb1e8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb1e8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb1e8-113">*strobjectpath*</span><span class="sxs-lookup"><span data-stu-id="eb1e8-113">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="eb1e8-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-114">Required.</span></span> <span data-ttu-id="eb1e8-115">Eine Zeichenfolge, die den Objekt Pfad des Objekts enthält, für das die Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-115">String that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="eb1e8-116">Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e8-116">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb1e8-117">*"Name"*</span><span class="sxs-lookup"><span data-stu-id="eb1e8-117">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="eb1e8-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-118">Required.</span></span> <span data-ttu-id="eb1e8-119">Der Name der Methode für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-119">Name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="eb1e8-120">*objwbeminparameams* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="eb1e8-120">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1e8-121">Ein [**-**](swbemobject.md) Objekt, das die Eingabeparameter für die ausgeführte Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-121">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="eb1e8-122">Standardmäßig ist dieser Parameter nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-122">By default, this parameter is undefined.</span></span> <span data-ttu-id="eb1e8-123">Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e8-123">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb1e8-124">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="eb1e8-124">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1e8-125">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-125">Reserved.</span></span> <span data-ttu-id="eb1e8-126">Dieser Wert muss null (0) sein.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-126">This value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="eb1e8-127">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="eb1e8-127">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1e8-128">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-128">Typically, this is undefined.</span></span> <span data-ttu-id="eb1e8-129">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-129">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="eb1e8-130">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-130">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb1e8-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb1e8-131">Return value</span></span>

<span data-ttu-id="eb1e8-132">Wenn die Methode erfolgreich ist, wird ein " [**errbemujeject**](swbemobject.md) "-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-132">If the method is successful, an [**SWbemObject**](swbemobject.md) object is returned.</span></span> <span data-ttu-id="eb1e8-133">Das zurückgegebene-Objekt enthält die Out-Parameter und den Rückgabewert für die Methode, die ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-133">The returned object contains the out parameters and return value for the method that is being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eb1e8-134">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="eb1e8-134">Error codes</span></span>

<span data-ttu-id="eb1e8-135">Nach dem Abschluss der **ExecMethod** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-135">After the completion of the **ExecMethod** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="eb1e8-136">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="eb1e8-136">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="eb1e8-137">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-137">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="eb1e8-138">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="eb1e8-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="eb1e8-139">Die angegebene Klasse war ungültig.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-139">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="eb1e8-140">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="eb1e8-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="eb1e8-141">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-141">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="eb1e8-142">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="eb1e8-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="eb1e8-143">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-143">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="eb1e8-144">**wbemErrInvalidMethod** -2147749934 (0x8004102e)</span><span class="sxs-lookup"><span data-stu-id="eb1e8-144">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="eb1e8-145">Die angeforderte Methode war nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-145">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="eb1e8-146">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="eb1e8-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="eb1e8-147">Der aktuelle Benutzer war nicht autorisiert, die Methode auszuführen.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-147">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb1e8-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb1e8-148">Remarks</span></span>

<span data-ttu-id="eb1e8-149">Verwenden Sie **SWbemServices.Execmethod** als Alternative zum direkten Zugriff auf die Ausführung einer [*Anbieter Methode*](gloss-p.md) , wenn es nicht möglich ist, eine Methode direkt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-149">Use **SWbemServices.ExecMethod** as an alternative to direct access for executing a [*provider method*](gloss-p.md) in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="eb1e8-150">Die **ExecMethod** -Methode ermöglicht Ihnen das Abrufen von Ausgabeparametern, wenn der Anbieter Sie mit einer Skriptsprache bereitstellt, die keine Ausgabeparameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-150">The **ExecMethod** method allows you to obtain output parameters, if the provider supplies them, with a scripting language that does not support output parameters.</span></span> <span data-ttu-id="eb1e8-151">Andernfalls besteht die empfohlene Methode zum Aufrufen einer Methode darin, den direkten Zugriff zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-151">Otherwise, the recommended means of invoking a method is to use direct access.</span></span> <span data-ttu-id="eb1e8-152">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e8-152">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="eb1e8-153">Beispielsweise verwendet das folgende Codebeispiel, das die [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) -Anbieter Methode im [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) aufruft, den direkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-153">For example, the following code example that calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider method in [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) uses direct access.</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



<span data-ttu-id="eb1e8-154">In diesem Beispiel wird **SWbemServices.Execmethod** aufgerufen, um die [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) -Methode auszuführen.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-154">This example calls **SWbemServices.ExecMethod** to execute the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span> <span data-ttu-id="eb1e8-155">Beachten Sie, dass ein Objekt Pfad erforderlich ist, weil **SWbemServices.Execmethod** im Gegensatz zu [**SWbemObject.Execmethod**](swbemobject-execmethod-.md)nicht bereits auf dem Objekt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-155">Note that an object path is required because **SWbemServices.ExecMethod** is not operating on the object already, unlike [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



<span data-ttu-id="eb1e8-156">Die **SWbemServices.Execmethod** -Methode erfordert einen Objekt Pfad.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-156">The **SWbemServices.ExecMethod** method requires an object path.</span></span> <span data-ttu-id="eb1e8-157">Wenn das Skript bereits ein " [**errbemubject**](swbemobject.md) "-Objekt enthält, verwenden Sie die [**SWbemObject.Execmethod**](swbemobject-execmethod-.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-157">If the script already holds an [**SWbemObject**](swbemobject.md) object, use the [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="eb1e8-158">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb1e8-158">Examples</span></span>

<span data-ttu-id="eb1e8-159">Das folgende Beispiel zeigt die **ExecMethod** -Methode.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-159">The following example shows the **ExecMethod** method.</span></span> <span data-ttu-id="eb1e8-160">Das Skript erstellt ein [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Objekt, das einen Prozess darstellt, der Notepad ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-160">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="eb1e8-161">Es zeigt das Einrichten eines [**InParameters**](swbemmethod-inparameters.md) -Objekts und das Abrufen von Ergebnissen von einem [**OutParameters**](swbemmethod-outparameters.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="eb1e8-161">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="eb1e8-162">Ein Skript, das die asynchron durchgeführten Vorgänge anzeigt, finden Sie unter [**SWbemServices.Execmethodasync**](swbemservices-execmethodasync.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e8-162">For a script that shows the same operations performed asynchronously, see [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span></span> <span data-ttu-id="eb1e8-163">Ein Beispiel für die Verwendung des direkten Zugriffs finden Sie unter [Create Method in \_ der Win32-Klasse](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="eb1e8-163">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="eb1e8-164">Ein Beispiel für den gleichen Vorgang, der ein [**Swap-Objekt**](swbemobject.md)verwendet, finden Sie unter [**SWbemObject.Execmethod**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e8-164">For an example of the same operation using an [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


```VB
' Connect to WMI
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains obtains a class object that
' defines the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_ 
'can be called to create it.

Set oInParams = _
    oProcess.Methods_("Create").InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

'Call SWbemServices.ExecMethod with the WMI path Win32_Process
Set oOutParams = _
    Services.ExecMethod( "Win32_Process", "Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully."
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed" _
            & " but had error " _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a><span data-ttu-id="eb1e8-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb1e8-165">Requirements</span></span>



| <span data-ttu-id="eb1e8-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb1e8-166">Requirement</span></span> | <span data-ttu-id="eb1e8-167">Wert</span><span class="sxs-lookup"><span data-stu-id="eb1e8-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb1e8-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb1e8-168">Minimum supported client</span></span><br/> | <span data-ttu-id="eb1e8-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb1e8-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb1e8-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb1e8-170">Minimum supported server</span></span><br/> | <span data-ttu-id="eb1e8-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb1e8-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb1e8-172">Header</span><span class="sxs-lookup"><span data-stu-id="eb1e8-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb1e8-173"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb1e8-173"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb1e8-174">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="eb1e8-174">Type library</span></span><br/>             | <dl> <span data-ttu-id="eb1e8-175"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eb1e8-175"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eb1e8-176">DLL</span><span class="sxs-lookup"><span data-stu-id="eb1e8-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb1e8-177"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb1e8-177"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eb1e8-178">CLSID</span><span class="sxs-lookup"><span data-stu-id="eb1e8-178">CLSID</span></span><br/>                    | <span data-ttu-id="eb1e8-179">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="eb1e8-179">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="eb1e8-180">IID</span><span class="sxs-lookup"><span data-stu-id="eb1e8-180">IID</span></span><br/>                      | <span data-ttu-id="eb1e8-181">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="eb1e8-181">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="eb1e8-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb1e8-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb1e8-183">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="eb1e8-183">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="eb1e8-184">**SWbemObject.Execmethod\_**</span><span class="sxs-lookup"><span data-stu-id="eb1e8-184">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="eb1e8-185">Aufrufen einer Anbieter Methode</span><span class="sxs-lookup"><span data-stu-id="eb1e8-185">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="eb1e8-186">Manipulieren von Klassen-und Instanzinformationen</span><span class="sxs-lookup"><span data-stu-id="eb1e8-186">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

