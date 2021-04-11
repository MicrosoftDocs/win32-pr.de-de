---
description: Die ExecMethod- \_ Methode des errbemubject-Objekts führt eine Methode aus, die von einem Methoden Anbieter exportiert wird.
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.tgt_platform: multiple
title: SWbemObject.ExecMethod_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6b71d88a113e515d50ac01a23f070714fa467615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130984"
---
# <a name="swbemobjectexecmethod_-method"></a><span data-ttu-id="dc9aa-103">SWbemObject.Execmethod- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="dc9aa-103">SWbemObject.ExecMethod\_ method</span></span>

<span data-ttu-id="dc9aa-104">Die **ExecMethod \_** -Methode des [**errbemubject**](swbemobject.md) -Objekts führt eine Methode aus, die von einem Methoden Anbieter exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-104">The **ExecMethod\_** method of the [**SWbemObject**](swbemobject.md) object executes a method exported by a method provider.</span></span>

<span data-ttu-id="dc9aa-105">Diese Methode wird angehalten, während die an den entsprechenden Anbieter weitergeleitete Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-105">This method pauses while the method that is forwarded to the appropriate provider executes.</span></span> <span data-ttu-id="dc9aa-106">Die Informationen und der Status werden dann zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-106">The information and status are then returned.</span></span> <span data-ttu-id="dc9aa-107">Der Anbieter implementiert die-Methode anstelle von WMI.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-107">The provider rather than WMI implements the method.</span></span>

<span data-ttu-id="dc9aa-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="dc9aa-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc9aa-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc9aa-109">Syntax</span></span>


```VB
objOutParams = .ExecMethod_( _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="dc9aa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc9aa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc9aa-111">" *Name* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="dc9aa-111">*strMethodName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc9aa-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-112">Required.</span></span> <span data-ttu-id="dc9aa-113">Der Name der Methode für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-113">Name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="dc9aa-114">*objwbeminparameams* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="dc9aa-114">*objwbemInParams* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dc9aa-115">Hierbei handelt es sich um ein Objekt vom [**typaustausch**](swbemobject.md) , das die Eingabeparameter für die Methode enthält, die ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-115">This is an [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="dc9aa-116">Standardmäßig ist dieser Parameter nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-116">By default, this parameter is undefined.</span></span> <span data-ttu-id="dc9aa-117">Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="dc9aa-117">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc9aa-118">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="dc9aa-118">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dc9aa-119">Reserviert und muss auf 0 (null) festgelegt werden, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-119">Reserved and must be set to 0 (zero) if specified.</span></span>

</dd> <dt>

<span data-ttu-id="dc9aa-120">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="dc9aa-120">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dc9aa-121">In der Regel ist Sie nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-121">Typically, it is undefined.</span></span> <span data-ttu-id="dc9aa-122">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="dc9aa-123">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc9aa-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc9aa-124">Return value</span></span>

<span data-ttu-id="dc9aa-125">Wenn diese Methode erfolgreich ist, gibt ein [**Swap**](swbemobject.md) -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-125">If this method is successful, an [**SWbemObject**](swbemobject.md) object returns.</span></span> <span data-ttu-id="dc9aa-126">Das zurückgegebene-Objekt enthält die Out-Parameter und den Rückgabewert für die Methode, die ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-126">The returned object contains the out parameters and return value for the method being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dc9aa-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="dc9aa-127">Error codes</span></span>

<span data-ttu-id="dc9aa-128">Nach dem Abschluss der **ExecMethod \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-128">After the completion of the **ExecMethod\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="dc9aa-129">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="dc9aa-129">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="dc9aa-130">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-130">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="dc9aa-131">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="dc9aa-131">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="dc9aa-132">Die angegebene Klasse war ungültig.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-132">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="dc9aa-133">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="dc9aa-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="dc9aa-134">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-134">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="dc9aa-135">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="dc9aa-135">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="dc9aa-136">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-136">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="dc9aa-137">**wbemErrInvalidMethod** -2147749934 (0x8004102e)</span><span class="sxs-lookup"><span data-stu-id="dc9aa-137">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="dc9aa-138">Die angeforderte Methode war nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-138">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="dc9aa-139">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="dc9aa-139">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="dc9aa-140">Der aktuelle Benutzer war nicht autorisiert, die Methode auszuführen.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-140">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc9aa-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc9aa-141">Remarks</span></span>

<span data-ttu-id="dc9aa-142">Diese Methode ähnelt [**SWbemServices.Execmethod**](swbemservices-execmethod.md), funktioniert jedoch direkt mit dem Objekt, dessen-Methode ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-142">This method is similar to [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), but it operates directly on the object whose method is to be executed.</span></span> <span data-ttu-id="dc9aa-143">Im folgenden Codebeispiel wird die [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) -Anbieter Methode im Win32- [**\_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) aufgerufen und der [direkte Zugriff](manipulating-class-and-instance-information.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-143">For example, the following code example calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider method in [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) and uses [direct access](manipulating-class-and-instance-information.md).</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



<span data-ttu-id="dc9aa-144">Diese Version ruft **SWbemObject.Execmethod \_** auf, um die [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) -Methode auszuführen.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-144">This version calls **SWbemObject.ExecMethod\_** to execute the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")
```



<span data-ttu-id="dc9aa-145">Verwenden Sie **SWbemObject.Execmethod \_** als Alternative zum direkten Zugriff auf die Ausführung einer [*Anbieter Methode*](gloss-p.md) , wenn es nicht möglich ist, eine Methode direkt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-145">Use **SWbemObject.ExecMethod\_** as an alternative to direct access for executing a [*provider method*](gloss-p.md) in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="dc9aa-146">Beispielsweise können Sie **SWbemObject.Execmethod \_** mit einer Skriptsprache verwenden, die keine Ausgabeparameter unterstützt, wenn die Methode out-Parameter aufweist.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-146">For example, you would use **SWbemObject.ExecMethod\_** with a scripting language that does not support output parameters if your method has out parameters.</span></span> <span data-ttu-id="dc9aa-147">Andernfalls besteht die empfohlene Methode zum Aufrufen einer Methode darin, den direkten Zugriff zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-147">Otherwise, the recommended means of invoking a method is to use direct access.</span></span>

-   <span data-ttu-id="dc9aa-148">Die **SWbemObject.Execmethod \_** -Methode geht davon aus, dass [**das durch das**](swbemobject.md) -Objekt dargestellte Objekt die auszuführende Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-148">The **SWbemObject.ExecMethod\_** method assumes the object represented by [**SWbemObject**](swbemobject.md) contains the method to execute.</span></span> <span data-ttu-id="dc9aa-149">Im Gegensatz dazu erfordert [**SWbemServices.Execmethod**](swbemservices-execmethod.md) einen Objekt Pfad.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-149">By contrast, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) requires an object path.</span></span> <span data-ttu-id="dc9aa-150">Verwenden Sie **SWbemObject.Execmethod \_** , wenn Sie bereits das Objekt abgerufen haben, dessen Methode Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-150">Use **SWbemObject.ExecMethod\_** if you already have obtained the object whose method you want to execute.</span></span>

## <a name="examples"></a><span data-ttu-id="dc9aa-151">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc9aa-151">Examples</span></span>

<span data-ttu-id="dc9aa-152">Das folgende Beispiel zeigt die [**ExecMethod**](swbemservices-execmethod.md) -Methode. Das Skript erstellt ein [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Objekt, das einen Prozess darstellt, der Editor ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-152">The following example shows the [**ExecMethod**](swbemservices-execmethod.md) method.The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object representing a process running Notepad.</span></span> <span data-ttu-id="dc9aa-153">Weitere Informationen zu einem Skript, das die asynchron durchgeführten Vorgänge veranschaulicht, finden Sie unter [**SWbemObject.Execmethodasync \_**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="dc9aa-153">For more information about a script illustrating the same operations performed asynchronously, see [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md).</span></span> <span data-ttu-id="dc9aa-154">Ein Beispiel für die Verwendung des direkten Zugriffs finden Sie unter [**Create method \_ in der Win32-Klasse**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) .</span><span class="sxs-lookup"><span data-stu-id="dc9aa-154">For an example using direct access, see [**Create Method in Class Win32\_Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) .</span></span> <span data-ttu-id="dc9aa-155">Ein Beispiel für denselben Vorgang mit einem " [**Swap Services**](swbemservices.md) "-Objekt finden Sie unter **SWbemServices.Execmethod**.</span><span class="sxs-lookup"><span data-stu-id="dc9aa-155">For an example of the same operation using an [**SWbemServices**](swbemservices.md) object, see **SWbemServices.ExecMethod**.</span></span>


```VB
' Connect to WMI and obtain a Win32_Process object.
' This is also an SWbemObject object.
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters
' object to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"
Set oOutParams = oProcess.ExecMethod_("Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully"
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed but had error" _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a><span data-ttu-id="dc9aa-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc9aa-156">Requirements</span></span>



| <span data-ttu-id="dc9aa-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc9aa-157">Requirement</span></span> | <span data-ttu-id="dc9aa-158">Wert</span><span class="sxs-lookup"><span data-stu-id="dc9aa-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9aa-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc9aa-159">Minimum supported client</span></span><br/> | <span data-ttu-id="dc9aa-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc9aa-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc9aa-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc9aa-161">Minimum supported server</span></span><br/> | <span data-ttu-id="dc9aa-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc9aa-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc9aa-163">Header</span><span class="sxs-lookup"><span data-stu-id="dc9aa-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc9aa-164"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc9aa-164"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc9aa-165">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="dc9aa-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="dc9aa-166"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dc9aa-166"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dc9aa-167">DLL</span><span class="sxs-lookup"><span data-stu-id="dc9aa-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc9aa-168"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc9aa-168"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dc9aa-169">CLSID</span><span class="sxs-lookup"><span data-stu-id="dc9aa-169">CLSID</span></span><br/>                    | <span data-ttu-id="dc9aa-170">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="dc9aa-170">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="dc9aa-171">IID</span><span class="sxs-lookup"><span data-stu-id="dc9aa-171">IID</span></span><br/>                      | <span data-ttu-id="dc9aa-172">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="dc9aa-172">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="dc9aa-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc9aa-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc9aa-174">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="dc9aa-174">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="dc9aa-175">**SWbemObject.Execmethodasync\_**</span><span class="sxs-lookup"><span data-stu-id="dc9aa-175">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="dc9aa-176">**SWbemServices.Execmethod**</span><span class="sxs-lookup"><span data-stu-id="dc9aa-176">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> </dl>

 

