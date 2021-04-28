---
description: 'SWbemServices.ExecMethod-Methode: Führt eine Methode aus, die von einem Methodenanbieter exportiert wird.'
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: SWbemServices.ExecMethod-Methode (Wbemdisp.h)
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
ms.openlocfilehash: 452c42c37e8dcb9f2b37b660b1f8899e587b5579
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103638"
---
# <a name="swbemservicesexecmethod-method"></a><span data-ttu-id="7ef0b-103">SWbemServices.ExecMethod-Methode</span><span class="sxs-lookup"><span data-stu-id="7ef0b-103">SWbemServices.ExecMethod method</span></span>

<span data-ttu-id="7ef0b-104">Die **ExecMethod-Methode** des [**SWbemServices-Objekts**](swbemservices.md) führt eine Methode aus, die von einem Methodenanbieter exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-104">The **ExecMethod** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="7ef0b-105">Diese Methode blockiert, während die Methode ausgeführt wird, die an den entsprechenden Anbieter weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-105">This method blocks while the method that is forwarded to the appropriate provider executes.</span></span> <span data-ttu-id="7ef0b-106">Die Informationen und der Status werden dann zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-106">The information and status are then returned.</span></span> <span data-ttu-id="7ef0b-107">Der Anbieter implementiert anstelle von WMI die -Methode.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-107">The provider, rather than WMI, implements the method.</span></span>

<span data-ttu-id="7ef0b-108">Diese Methode wird im synchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-108">This method is called in the synchronous mode.</span></span> <span data-ttu-id="7ef0b-109">Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)</span><span class="sxs-lookup"><span data-stu-id="7ef0b-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="7ef0b-110">Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)</span><span class="sxs-lookup"><span data-stu-id="7ef0b-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7ef0b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ef0b-111">Syntax</span></span>


```VB
objOutParams = .ExecMethod( _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7ef0b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ef0b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ef0b-113">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="7ef0b-113">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="7ef0b-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-114">Required.</span></span> <span data-ttu-id="7ef0b-115">Zeichenfolge, die den Objektpfad des Objekts enthält, für das die Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-115">String that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="7ef0b-116">Weitere Informationen finden Sie unter [Beschreiben des Speicherorts eines WMI-Objekts.](describing-the-location-of-a-wmi-object.md)</span><span class="sxs-lookup"><span data-stu-id="7ef0b-116">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ef0b-117">*strMethodName*</span><span class="sxs-lookup"><span data-stu-id="7ef0b-117">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="7ef0b-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-118">Required.</span></span> <span data-ttu-id="7ef0b-119">Name der Methode für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-119">Name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="7ef0b-120">*objWbemInParams* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="7ef0b-120">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ef0b-121">Ein [**SWbemObject-Objekt,**](swbemobject.md) das die Eingabeparameter für die ausgeführte Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-121">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="7ef0b-122">Dieser Parameter ist standardmäßig nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-122">By default, this parameter is undefined.</span></span> <span data-ttu-id="7ef0b-123">Weitere Informationen finden Sie unter [Erstellen von InParameters-Objekten und Analysieren von OutParameters-Objekten.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)</span><span class="sxs-lookup"><span data-stu-id="7ef0b-123">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ef0b-124">*iFlags* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="7ef0b-124">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ef0b-125">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-125">Reserved.</span></span> <span data-ttu-id="7ef0b-126">Dieser Wert muss null (0) sein.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-126">This value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7ef0b-127">*objWbemNamedValueSet* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="7ef0b-127">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ef0b-128">In der Regel ist dies nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-128">Typically, this is undefined.</span></span> <span data-ttu-id="7ef0b-129">Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung bedient.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-129">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="7ef0b-130">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-130">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ef0b-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ef0b-131">Return value</span></span>

<span data-ttu-id="7ef0b-132">Wenn die Methode erfolgreich ist, wird ein [**SWbemObject-Objekt**](swbemobject.md) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-132">If the method is successful, an [**SWbemObject**](swbemobject.md) object is returned.</span></span> <span data-ttu-id="7ef0b-133">Das zurückgegebene -Objekt enthält die out-Parameter und den Rückgabewert für die Methode, die ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-133">The returned object contains the out parameters and return value for the method that is being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7ef0b-134">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7ef0b-134">Error codes</span></span>

<span data-ttu-id="7ef0b-135">Nach Abschluss der **ExecMethod-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-135">After the completion of the **ExecMethod** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="7ef0b-136">**wbemErrFailed** – 2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7ef0b-136">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7ef0b-137">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-137">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="7ef0b-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="7ef0b-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="7ef0b-139">Die angegebene Klasse war ungültig.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-139">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7ef0b-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="7ef0b-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="7ef0b-141">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-141">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7ef0b-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="7ef0b-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="7ef0b-143">Nicht genügend Arbeitsspeicher zum Abschließen des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-143">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7ef0b-144">**wbemErrInvalidMethod** – 2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="7ef0b-144">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="7ef0b-145">Die angeforderte Methode war nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-145">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="7ef0b-146">**wbemErrAccessDenied** – 2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="7ef0b-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="7ef0b-147">Der aktuelle Benutzer war nicht berechtigt, die Methode auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-147">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ef0b-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ef0b-148">Remarks</span></span>

<span data-ttu-id="7ef0b-149">Verwenden **SWbemServices.ExecMethod** als Alternative zum direkten Zugriff zum Ausführen einer Anbietermethode [*in*](gloss-p.md) Fällen, in denen es nicht möglich ist, eine Methode direkt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-149">Use **SWbemServices.ExecMethod** as an alternative to direct access for executing a [*provider method*](gloss-p.md) in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="7ef0b-150">Mit **der ExecMethod-Methode** können Sie Ausgabeparameter mit einer Skriptsprache abrufen, die keine Ausgabeparameter unterstützt, wenn sie vom Anbieter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-150">The **ExecMethod** method allows you to obtain output parameters, if the provider supplies them, with a scripting language that does not support output parameters.</span></span> <span data-ttu-id="7ef0b-151">Andernfalls wird empfohlen, einen direkten Zugriff zu verwenden, um eine Methode auf den Weg zu bringen.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-151">Otherwise, the recommended means of invoking a method is to use direct access.</span></span> <span data-ttu-id="7ef0b-152">Weitere Informationen finden Sie unter [Bearbeiten von Klassen- und Instanzinformationen.](manipulating-class-and-instance-information.md)</span><span class="sxs-lookup"><span data-stu-id="7ef0b-152">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="7ef0b-153">Das folgende Codebeispiel, das die [**StartService-Anbietermethode**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) in [**Win32 \_ Service**](/windows/desktop/CIMWin32Prov/win32-service) aufruft, verwendet beispielsweise direkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-153">For example, the following code example that calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider method in [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) uses direct access.</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



<span data-ttu-id="7ef0b-154">In diesem Beispiel **wirdSWbemServices.ExecMethod** aufgerufen, um die [**StartService-Methode**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-154">This example calls **SWbemServices.ExecMethod** to execute the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span> <span data-ttu-id="7ef0b-155">Beachten Sie, dass ein Objektpfad erforderlich ist, da **SWbemServices.ExecMethod** im Gegensatz zu [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md)nicht bereits für das Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-155">Note that an object path is required because **SWbemServices.ExecMethod** is not operating on the object already, unlike [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



<span data-ttu-id="7ef0b-156">Die **SWbemServices.ExecMethod-Methode** erfordert einen Objektpfad.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-156">The **SWbemServices.ExecMethod** method requires an object path.</span></span> <span data-ttu-id="7ef0b-157">Wenn das Skript bereits ein [**SWbemObject-Objekt**](swbemobject.md) enthält, verwenden Sie die [**SWbemObject.ExecMethod-Methode.**](swbemobject-execmethod-.md)</span><span class="sxs-lookup"><span data-stu-id="7ef0b-157">If the script already holds an [**SWbemObject**](swbemobject.md) object, use the [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="7ef0b-158">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ef0b-158">Examples</span></span>

<span data-ttu-id="7ef0b-159">Das folgende Beispiel zeigt die **ExecMethod-Methode.**</span><span class="sxs-lookup"><span data-stu-id="7ef0b-159">The following example shows the **ExecMethod** method.</span></span> <span data-ttu-id="7ef0b-160">Das Skript erstellt ein [**\_ Win32-Prozessobjekt,**](/windows/desktop/CIMWin32Prov/win32-process) das einen Prozess darstellt, der Editor ausführt.</span><span class="sxs-lookup"><span data-stu-id="7ef0b-160">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="7ef0b-161">Es zeigt die Einrichtung eines [**InParameters-Objekts**](swbemmethod-inparameters.md) und das Abrufen von Ergebnissen aus einem [**OutParameters-Objekt.**](swbemmethod-outparameters.md)</span><span class="sxs-lookup"><span data-stu-id="7ef0b-161">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="7ef0b-162">Ein Skript, das die gleichen asynchron ausgeführten Vorgänge anzeigt, finden Sie unter [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span><span class="sxs-lookup"><span data-stu-id="7ef0b-162">For a script that shows the same operations performed asynchronously, see [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span></span> <span data-ttu-id="7ef0b-163">Ein Beispiel für die Verwendung des direkten Zugriffs finden Sie unter [Create Method in Class Win32 \_ Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="7ef0b-163">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="7ef0b-164">Ein Beispiel für den gleichen Vorgang mit einem [**SWbemObject**](swbemobject.md)finden Sie unter [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="7ef0b-164">For an example of the same operation using an [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7ef0b-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ef0b-165">Requirements</span></span>



| <span data-ttu-id="7ef0b-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ef0b-166">Requirement</span></span> | <span data-ttu-id="7ef0b-167">Wert</span><span class="sxs-lookup"><span data-stu-id="7ef0b-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ef0b-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ef0b-168">Minimum supported client</span></span><br/> | <span data-ttu-id="7ef0b-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ef0b-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7ef0b-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ef0b-170">Minimum supported server</span></span><br/> | <span data-ttu-id="7ef0b-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ef0b-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7ef0b-172">Header</span><span class="sxs-lookup"><span data-stu-id="7ef0b-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ef0b-173"><dt>Wbemdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="7ef0b-173"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ef0b-174">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7ef0b-174">Type library</span></span><br/>             | <dl> <span data-ttu-id="7ef0b-175"><dt>Wbemdisp.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7ef0b-175"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7ef0b-176">DLL</span><span class="sxs-lookup"><span data-stu-id="7ef0b-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ef0b-177"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ef0b-177"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7ef0b-178">CLSID</span><span class="sxs-lookup"><span data-stu-id="7ef0b-178">CLSID</span></span><br/>                    | <span data-ttu-id="7ef0b-179">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="7ef0b-179">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="7ef0b-180">IID</span><span class="sxs-lookup"><span data-stu-id="7ef0b-180">IID</span></span><br/>                      | <span data-ttu-id="7ef0b-181">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="7ef0b-181">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="7ef0b-182">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7ef0b-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ef0b-183">**Swbemservices**</span><span class="sxs-lookup"><span data-stu-id="7ef0b-183">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="7ef0b-184">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="7ef0b-184">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="7ef0b-185">Aufrufen einer Anbietermethode</span><span class="sxs-lookup"><span data-stu-id="7ef0b-185">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="7ef0b-186">Bearbeiten von Klassen- und Instanzinformationen</span><span class="sxs-lookup"><span data-stu-id="7ef0b-186">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

