---
description: Führt eine Methode aus, die von einem Methoden Anbieter exportiert wird.
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: SWbemServices.Execmethodasync-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898912efae276fc0404576e162468e06e1b95a68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347888"
---
# <a name="swbemservicesexecmethodasync-method"></a><span data-ttu-id="2d132-103">SWbemServices.Execmethodasync-Methode</span><span class="sxs-lookup"><span data-stu-id="2d132-103">SWbemServices.ExecMethodAsync method</span></span>

<span data-ttu-id="2d132-104">Die **ExecMethodAsync** -Methode des [**Swap Services**](swbemservices.md) -Objekts führt eine Methode aus, die von einem Methoden Anbieter exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="2d132-104">The **ExecMethodAsync** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="2d132-105">Der-Befehl kehrt sofort an den Client zurück, während die eingehenden Parameter an den entsprechenden Anbieter weitergeleitet werden, in dem die Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d132-105">The call immediately returns to the client while the inbound parameters are forwarded to the appropriate provider where the method executes.</span></span> <span data-ttu-id="2d132-106">Informationen und Status werden an den Aufrufer zurückgegeben, indem Ereignisse an die Senke gesendet werden, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2d132-106">Information and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="2d132-107">Der Anbieter implementiert die-Methode anstelle von Windows-Verwaltungsinstrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="2d132-107">The provider, rather than Windows Management Instrumentation (WMI), implements the method.</span></span>

<span data-ttu-id="2d132-108">Die-Methode wird im asynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2d132-108">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="2d132-109">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="2d132-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="2d132-110">Weitere Informationen und eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2d132-110">For more information and an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d132-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d132-111">Syntax</span></span>


```VB
SWbemServices.ExecMethodAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2d132-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d132-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d132-113">*objwbemsink*</span><span class="sxs-lookup"><span data-stu-id="2d132-113">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="2d132-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2d132-114">Required.</span></span> <span data-ttu-id="2d132-115">Erstellen Sie ein " [**taubemsink**](swbemsink.md) "-Objekt zum Empfangen der Objekte.</span><span class="sxs-lookup"><span data-stu-id="2d132-115">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span> <span data-ttu-id="2d132-116">Objekt Senke, die das Ergebnis des Methoden Aufrufes empfängt.</span><span class="sxs-lookup"><span data-stu-id="2d132-116">Object sink that receives the result of the method call.</span></span> <span data-ttu-id="2d132-117">Die ausgehenden Parameter werden an das Ereignis " [**slibemsink. onobjectready**](swbemsink-onobjectready.md) " der angegebenen Objekt Senke gesendet.</span><span class="sxs-lookup"><span data-stu-id="2d132-117">The outbound parameters are sent to the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event of the supplied object sink.</span></span> <span data-ttu-id="2d132-118">Die Ergebnisse des-aufrufungsmechanismus werden an das Ereignis " [**slibemsink. onabgeschlossene**](swbemsink-oncompleted.md) " der angegebenen Objekt Senke gesendet.</span><span class="sxs-lookup"><span data-stu-id="2d132-118">The results of the call mechanism are sent to the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the supplied object sink.</span></span> <span data-ttu-id="2d132-119">Beachten Sie, dass " **taubemsink. onabgeschlossene** " den Rückgabecode der WMI-Methode nicht empfängt.</span><span class="sxs-lookup"><span data-stu-id="2d132-119">Be aware that **SWbemSink.OnCompleted** does not receive the return code of the WMI method.</span></span> <span data-ttu-id="2d132-120">Er empfängt jedoch den Rückgabecode des eigentlichen Rückrufmechanismus und ist nur nützlich, um zu überprüfen, ob der-Befehl aufgetreten ist, oder dass er aus mechanischen Gründen fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="2d132-120">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons.</span></span> <span data-ttu-id="2d132-121">Der Ergebniscode, der von der WMI-Methode zurückgegeben wird, wird im ausgehenden Parameter Objekt zurückgegeben, das an " **taubemsink. onobjectready**" übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2d132-121">The result code that is returned from the WMI method is returned in the outbound parameter object supplied to **SWbemSink.OnObjectReady**.</span></span> <span data-ttu-id="2d132-122">Wenn ein Fehlercode zurückgegeben wird, wird das angegebene Objekt " [**iwbejebjectsink**](iwbemobjectsink.md) " nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d132-122">If any error code is returned, then the supplied [**IWbemObjectSink**](iwbemobjectsink.md) object is not used.</span></span> <span data-ttu-id="2d132-123">Wenn der Aufruf erfolgreich ist, wird die **iwberobjectsink** -Implementierung des Benutzers aufgerufen, um das Ergebnis des Vorgangs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2d132-123">If the call is successful, then the user's **IWbemObjectSink** implementation is called to indicate the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2d132-124">*strobjectpath*</span><span class="sxs-lookup"><span data-stu-id="2d132-124">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="2d132-125">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2d132-125">Required.</span></span> <span data-ttu-id="2d132-126">Eine Zeichenfolge, die den Objekt Pfad des-Objekts enthält, für das die-Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d132-126">A string that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="2d132-127">Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="2d132-127">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d132-128">*"Name"*</span><span class="sxs-lookup"><span data-stu-id="2d132-128">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="2d132-129">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2d132-129">Required.</span></span> <span data-ttu-id="2d132-130">Der Name der zu auszuführenden Methode.</span><span class="sxs-lookup"><span data-stu-id="2d132-130">The name of the method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="2d132-131">*objwbeminparameams* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="2d132-131">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2d132-132">Ein [**-**](swbemobject.md) Objekt, das die Eingabeparameter für die Methode enthält, die ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d132-132">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method that is executed.</span></span> <span data-ttu-id="2d132-133">Standardmäßig ist dieser Parameter nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="2d132-133">By default, this parameter is undefined.</span></span> <span data-ttu-id="2d132-134">Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2d132-134">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d132-135">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="2d132-135">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2d132-136">Eine ganze Zahl, die das Verhalten des Aufrufes bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2d132-136">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="2d132-137">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="2d132-137">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="2d132-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="2d132-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="2d132-139">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="2d132-139">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="2d132-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="2d132-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2d132-141">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="2d132-141">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2d132-142">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="2d132-142">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2d132-143">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="2d132-143">Typically, this is undefined.</span></span> <span data-ttu-id="2d132-144">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="2d132-144">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="2d132-145">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="2d132-145">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="2d132-146">*objwbemasynccontext* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="2d132-146">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2d132-147">Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das zur Objekt Senke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufes aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2d132-147">A [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="2d132-148">Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen.</span><span class="sxs-lookup"><span data-stu-id="2d132-148">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="2d132-149">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2d132-149">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="2d132-150">Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="2d132-150">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="2d132-151">Weitere Informationen finden Sie unter [Erstellen eines asynchronen Aufrufes mit VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="2d132-151">For more information, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d132-152">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d132-152">Return value</span></span>

<span data-ttu-id="2d132-153">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2d132-153">This method does not return a value.</span></span> <span data-ttu-id="2d132-154">Wenn der-Befehl erfolgreich ausgeführt wurde, wird ein [**OutParameters**](swbemmethod-outparameters.md) -Objekt, das ebenfalls ein " [**errbefubject**](swbemobject.md) "-Objekt ist, an die Senke bereitgestellt, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2d132-154">If the call is successful, an [**OutParameters**](swbemmethod-outparameters.md) object, which is also an [**SWbemObject**](swbemobject.md) is supplied to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="2d132-155">Das zurückgegebene **OutParameters** -Objekt enthält die Ausgabeparameter und den Rückgabewert für die Methode, die ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d132-155">The returned **OutParameters** object contains the output parameters and return value for the method being executed.</span></span> <span data-ttu-id="2d132-156">Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2d132-156">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="2d132-157">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2d132-157">Error codes</span></span>

<span data-ttu-id="2d132-158">Nach dem Abschluss der **ExecMethodAsync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der in der folgenden Liste aufgeführten Fehlercodes enthalten.</span><span class="sxs-lookup"><span data-stu-id="2d132-158">After the completion of the **ExecMethodAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes listed in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="2d132-159">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="2d132-159">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2d132-160">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="2d132-160">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="2d132-161">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="2d132-161">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="2d132-162">Die angegebene Klasse war ungültig.</span><span class="sxs-lookup"><span data-stu-id="2d132-162">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2d132-163">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="2d132-163">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="2d132-164">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="2d132-164">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2d132-165">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="2d132-165">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="2d132-166">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="2d132-166">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2d132-167">**wbemErrInvalidMethod** -2147749934 (0x8004102e)</span><span class="sxs-lookup"><span data-stu-id="2d132-167">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="2d132-168">Die angeforderte Methode war nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2d132-168">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="2d132-169">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="2d132-169">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="2d132-170">Der aktuelle Benutzer war nicht autorisiert, die Methode auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2d132-170">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d132-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d132-171">Remarks</span></span>

<span data-ttu-id="2d132-172">Wenn die ausgeführte Methode Eingabeparameter enthält, muss das [**InParameters**](swbemmethod-inparameters.md) -Objekt im *objwbeminparam* -Parameter mit der Beschreibung in den Themen [Erstellen von InParameters-Objekten und Parsing OutParameters-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md) identisch sein.</span><span class="sxs-lookup"><span data-stu-id="2d132-172">If the method executed has input parameters, the [**InParameters**](swbemmethod-inparameters.md) object in the *objWbemInParam* parameter must be the same as the description in the [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md) topics.</span></span>

<span data-ttu-id="2d132-173">Verwenden Sie **SWbemServices.Execmethodasync** als Alternative zum direkten Zugriff auf die Ausführung einer [*Anbieter Methode*](gloss-p.md) , wenn es nicht möglich ist, eine Methode direkt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2d132-173">Use **SWbemServices.ExecMethodAsync** as an alternative to direct access for executing a [*provider method*](gloss-p.md) when it is not possible to execute a method directly.</span></span> <span data-ttu-id="2d132-174">Verwenden Sie diese z. b. mit einer Skriptsprache, die keine Ausgabeparameter unterstützt, d. h., wenn die Methode out-Parameter aufweist.</span><span class="sxs-lookup"><span data-stu-id="2d132-174">For example, use it with a scripting language that does not support output parameters, that is, if your method has OUT parameters.</span></span> <span data-ttu-id="2d132-175">Andernfalls wird empfohlen, den direkten Zugriff zu verwenden, um eine Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2d132-175">Otherwise, it is recommended that you use direct access to invoke a method.</span></span> <span data-ttu-id="2d132-176">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="2d132-176">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="2d132-177">Die **SWbemServices.Execmethodasync** -Methode erfordert einen Objekt Pfad.</span><span class="sxs-lookup"><span data-stu-id="2d132-177">The **SWbemServices.ExecMethodAsync** method requires an object path.</span></span> <span data-ttu-id="2d132-178">Wenn das Skript bereits ein " [**errbemubject**](swbemobject.md) "-Objekt enthält, können Sie [**SWbemObject.Execmethodasync**](swbemobject-execmethodasync-.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2d132-178">If the script already contains an [**SWbemObject**](swbemobject.md) object, you can call [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>

<span data-ttu-id="2d132-179">Dieser Rückruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2d132-179">This call returns immediately.</span></span> <span data-ttu-id="2d132-180">Die Statusinformationen werden an den Aufrufer zurückgegeben, indem die Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2d132-180">The status information is returned to the caller through call-backs delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="2d132-181">Um die Verarbeitung fortzusetzen, wenn der-Befehl abgeschlossen ist, implementieren Sie eine Unterroutine für die *objwbemsink*. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="2d132-181">To continue processing when the call is completed, implement a subroutine for the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="2d132-182">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="2d132-182">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="2d132-183">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="2d132-183">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="2d132-184">Weitere Informationen zum Beseitigen der Risiken finden Sie unter Festlegen der [Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="2d132-184">For more information about how to eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="2d132-185">Verwenden Sie den *objwbemasynccontext* -Parameter, um die Quelle eines Aufrufes zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2d132-185">Use the *objWbemAsyncContext* parameter to verify the source of a call.</span></span>

## <a name="examples"></a><span data-ttu-id="2d132-186">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d132-186">Examples</span></span>

<span data-ttu-id="2d132-187">Das folgende Codebeispiel zeigt die **ExecMethodAsync** -Methode.</span><span class="sxs-lookup"><span data-stu-id="2d132-187">The following code example shows the **ExecMethodAsync** method.</span></span> <span data-ttu-id="2d132-188">Das Skript erstellt ein [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Objekt, das einen Prozess darstellt, der Notepad ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d132-188">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="2d132-189">Es zeigt das Einrichten eines [**InParameters**](swbemmethod-inparameters.md) -Objekts und das Abrufen von Ergebnissen von einem [**OutParameters**](swbemmethod-outparameters.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2d132-189">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="2d132-190">Informationen zu einem Skript, das die synchron ausgeführten Vorgänge anzeigt, finden Sie unter [**SWbemServices.Execmethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="2d132-190">For a script that shows the same operations performed synchronously, see [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span> <span data-ttu-id="2d132-191">Ein Beispiel für die Verwendung des direkten Zugriffs finden Sie unter [Create Method in \_ der Win32-Klasse](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="2d132-191">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="2d132-192">Ein Beispiel für denselben Vorgang mit " [**Swap**](swbemobject.md)" finden Sie unter [**SWbemObject.Execmethodasync**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="2d132-192">For an example of the same operation using [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>


```VB
' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &VBCR & "ReturnValue = " _
        & oOutParams.ReturnValue &VBCR & _
        "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
        & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a><span data-ttu-id="2d132-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d132-193">Requirements</span></span>



| <span data-ttu-id="2d132-194">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d132-194">Requirement</span></span> | <span data-ttu-id="2d132-195">Wert</span><span class="sxs-lookup"><span data-stu-id="2d132-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d132-196">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d132-196">Minimum supported client</span></span><br/> | <span data-ttu-id="2d132-197">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d132-197">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2d132-198">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d132-198">Minimum supported server</span></span><br/> | <span data-ttu-id="2d132-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d132-199">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2d132-200">Header</span><span class="sxs-lookup"><span data-stu-id="2d132-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d132-201"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d132-201"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d132-202">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2d132-202">Type library</span></span><br/>             | <dl> <span data-ttu-id="2d132-203"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2d132-203"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2d132-204">DLL</span><span class="sxs-lookup"><span data-stu-id="2d132-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d132-205"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d132-205"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2d132-206">CLSID</span><span class="sxs-lookup"><span data-stu-id="2d132-206">CLSID</span></span><br/>                    | <span data-ttu-id="2d132-207">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="2d132-207">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="2d132-208">IID</span><span class="sxs-lookup"><span data-stu-id="2d132-208">IID</span></span><br/>                      | <span data-ttu-id="2d132-209">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="2d132-209">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="2d132-210">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d132-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d132-211">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="2d132-211">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="2d132-212">**SWbemObject.Execmethod\_**</span><span class="sxs-lookup"><span data-stu-id="2d132-212">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="2d132-213">**SWbemObject.Execmethodasync\_**</span><span class="sxs-lookup"><span data-stu-id="2d132-213">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="2d132-214">**SWbemServices.Execmethod**</span><span class="sxs-lookup"><span data-stu-id="2d132-214">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="2d132-215">Aufrufen einer Anbieter Methode</span><span class="sxs-lookup"><span data-stu-id="2d132-215">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="2d132-216">Manipulieren von Klassen-und Instanzinformationen</span><span class="sxs-lookup"><span data-stu-id="2d132-216">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

