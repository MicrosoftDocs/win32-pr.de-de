---
description: Die ExecMethodAsync- \_ Methode von "errbemubject" führt asynchron eine Methode aus, die von einem Methoden Anbieter exportiert wird.
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: SWbemObject.ExecMethodAsync_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8af1b7c10eed427423afea8b40a1df5bc237f99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218169"
---
# <a name="swbemobjectexecmethodasync_-method"></a><span data-ttu-id="ca0ce-103">SWbemObject.Execmethodasync- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="ca0ce-103">SWbemObject.ExecMethodAsync\_ method</span></span>

<span data-ttu-id="ca0ce-104">Die **ExecMethodAsync \_** -Methode von " [**errbemubject**](swbemobject.md) " führt asynchron eine Methode aus, die von einem Methoden Anbieter exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-104">The **ExecMethodAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously executes a method that a method provider exports.</span></span> <span data-ttu-id="ca0ce-105">Diese Methode ähnelt [**SWbemServices.Execmethodasync**](swbemservices-execmethodasync.md), funktioniert jedoch direkt mit dem-Objekt der auszuführenden Methode.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-105">This method is similar to [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), but operates directly on the object of the method to be executed.</span></span> <span data-ttu-id="ca0ce-106">Diese Methode wird von Windows-Verwaltungsinstrumentation (WMI) nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-106">Windows Management Instrumentation (WMI) does not implement this method.</span></span> <span data-ttu-id="ca0ce-107">Der Anbieter implementiert diese Methode.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-107">The provider implements this method.</span></span>

<span data-ttu-id="ca0ce-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ca0ce-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca0ce-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca0ce-109">Syntax</span></span>


```VB
objOutParams = .ExecMethodAsync_( _
  ByVal objWbemSink, _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ca0ce-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca0ce-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca0ce-111">*objwbemsink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca0ce-111">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca0ce-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-112">Required.</span></span> <span data-ttu-id="ca0ce-113">Dies ist die Objekt Senke, die die Ergebnisse des Methoden Aufrufes empfängt.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-113">This is the object sink that receives the results of the method call.</span></span> <span data-ttu-id="ca0ce-114">Die ausgehenden Parameter werden an das Ereignis " [**slibemsink. onobjectready**](swbemsink-onobjectready.md) " der angegebenen Objekt Senke gesendet.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-114">The outbound parameters are sent to the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event of the supplied object sink.</span></span> <span data-ttu-id="ca0ce-115">Die Ergebnisse des-aufrufungsmechanismus werden an das Ereignis " [**slibemsink. onabgeschlossene**](swbemsink-oncompleted.md) " der angegebenen Objekt Senke gesendet.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-115">The results of the call mechanism are sent to the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the supplied object sink.</span></span> <span data-ttu-id="ca0ce-116">Beachten Sie, dass " **taubemsink. onabgeschlossene** " nicht den Rückgabecode der Methode empfängt.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-116">Notice that **SWbemSink.OnCompleted** does not receive the return code of the method.</span></span> <span data-ttu-id="ca0ce-117">Er empfängt jedoch den Rückgabecode des eigentlichen Rückrufmechanismus und ist nur nützlich, um zu überprüfen, ob der-Befehl aufgetreten ist, oder dass er aus mechanischen Gründen fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-117">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred, or that it failed for mechanical reasons.</span></span> <span data-ttu-id="ca0ce-118">Der von der-Methode zurückgegebene Ergebniscode wird im ausgehenden Parameter Objekt zurückgegeben, das für " **Swap. onobjectready**" bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-118">The result code returned from the method is returned in the outbound parameter object supplied to **SWbemSink.OnObjectReady**.</span></span> <span data-ttu-id="ca0ce-119">Wenn ein Fehlercode zurückgegeben wird, wird das angegebene [**iwbejebjectsink**](iwbemobjectsink.md) -Objekt nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-119">If any error code returns, then the supplied [**IWbemObjectSink**](iwbemobjectsink.md) object is not used.</span></span> <span data-ttu-id="ca0ce-120">Wenn der Aufruf erfolgreich ist, wird die **iwberobjectsink** -Implementierung des Benutzers aufgerufen, um das Ergebnis des Vorgangs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-120">If the call is successful, then the user's **IWbemObjectSink** implementation is called to indicate the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ca0ce-121">" *Name* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="ca0ce-121">*strMethodName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca0ce-122">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-122">Required.</span></span> <span data-ttu-id="ca0ce-123">Dies ist der Name der-Methode für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-123">This is the name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="ca0ce-124">*objwbeminparameams* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ca0ce-124">*objwbemInParams* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca0ce-125">Hierbei handelt es sich um ein Objekt vom [**typaustausch**](swbemobject.md) , das die Eingabeparameter für die Methode enthält, die ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-125">This is an [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="ca0ce-126">Standardmäßig ist dieser Parameter nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-126">By default, this parameter is undefined.</span></span> <span data-ttu-id="ca0ce-127">Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten](constructing-inparameters-objects.md) und Überprüfen von [outparameter-Objekten](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ca0ce-127">For more information, see [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca0ce-128">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ca0ce-128">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca0ce-129">Eine ganze Zahl, die das Verhalten des Aufrufes bestimmt.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-129">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="ca0ce-130">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-130">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="ca0ce-131"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="ca0ce-131"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="ca0ce-132">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den " [**slibemsink. OnProgress**](swbemsink-onprogress.md) "-Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-132">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="ca0ce-133"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="ca0ce-133"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="ca0ce-134">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-134">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ca0ce-135">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ca0ce-135">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca0ce-136">In der Regel ist Sie nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-136">Typically, it is undefined.</span></span> <span data-ttu-id="ca0ce-137">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-137">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="ca0ce-138">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-138">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="ca0ce-139">*objwbemasynccontext* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ca0ce-139">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca0ce-140">Dabei handelt es sich um ein Objekt vom Typ " [**taubemnamedvalueset**](swbemnamedvalueset.md) ", das zur Objekt Senke zurückkehrt, um die Quelle für den ursprünglichen asynchronen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-140">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="ca0ce-141">Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-141">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="ca0ce-142">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-142">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="ca0ce-143">Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-143">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="ca0ce-144">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ca0ce-144">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca0ce-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca0ce-145">Return value</span></span>

<span data-ttu-id="ca0ce-146">Diese Methode hat keine Rückgabewerte.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-146">This method has no return values.</span></span> <span data-ttu-id="ca0ce-147">Wenn der-Befehl erfolgreich ausgeführt wurde, wird ein [**OutParameters**](swbemmethod-outparameters.md) -Objekt, das auch ein " [**errbefubject**](swbemobject.md) "-Objekt ist, an die in *objwbemsink* angegebene Senke bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-147">If the call is successful, an [**OutParameters**](swbemmethod-outparameters.md) object, which is also an [**SWbemObject**](swbemobject.md) object, is supplied to the sink specified in *objWbemSink*.</span></span> <span data-ttu-id="ca0ce-148">Das zurückgegebene **OutParameters** -Objekt enthält die Ausgabeparameter und den Rückgabewert für die Methode, die ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-148">The returned **OutParameters** object contains the output parameters and return value for the method being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ca0ce-149">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ca0ce-149">Error codes</span></span>

<span data-ttu-id="ca0ce-150">Nach Abschluss der **ExecMethodAsync \_** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-150">After completion of the **ExecMethodAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ca0ce-151">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ca0ce-151">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ca0ce-152">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-152">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ca0ce-153">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="ca0ce-153">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="ca0ce-154">Die angegebene Klasse war ungültig.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-154">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ca0ce-155">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ca0ce-155">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ca0ce-156">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-156">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ca0ce-157">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="ca0ce-157">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="ca0ce-158">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-158">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ca0ce-159">**wbemErrInvalidMethod** -2147749934 (0x8004102e)</span><span class="sxs-lookup"><span data-stu-id="ca0ce-159">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="ca0ce-160">Die angeforderte Methode war nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-160">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="ca0ce-161">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="ca0ce-161">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="ca0ce-162">Der aktuelle Benutzer war nicht autorisiert, die Methode auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-162">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca0ce-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca0ce-163">Remarks</span></span>

<span data-ttu-id="ca0ce-164">Verwenden Sie die **SWbemObject.Exe\_ cmethodasync** -Methode als Alternative zum direkten Zugriff auf die Ausführung einer [*Anbieter Methode*](gloss-p.md) , wenn Sie eine Methode nicht direkt ausführen können.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-164">Use the **SWbemObject.ExecMethodAsync\_** method as an alternative to direct access for executing a [*provider method*](gloss-p.md) when you cannot execute a method directly.</span></span> <span data-ttu-id="ca0ce-165">Wenn Ihre Methode z. b. über out-Parameter verfügt, verwenden Sie die **SWbemObject.Exe\_ cmethodasync** -Methode mit einer Skriptsprache, die keine Ausgabeparameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-165">For example, if your method has out parameters, use the **SWbemObject.ExecMethodAsync\_** method with a scripting language that does not support output parameters.</span></span> <span data-ttu-id="ca0ce-166">Andernfalls wird empfohlen, eine Methode mithilfe des direkten Zugriffs aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-166">Otherwise, it is recommended that you invoke a method using direct access.</span></span> <span data-ttu-id="ca0ce-167">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="ca0ce-167">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="ca0ce-168">Dieser Rückruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-168">This call returns immediately.</span></span> <span data-ttu-id="ca0ce-169">Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, wenn Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-169">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="ca0ce-170">Um jedes Objekt zu verarbeiten, sobald es eintrifft, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-170">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="ca0ce-171">Nachdem alle Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in ihrer Implementierung von *objwbemsink* durchführen. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-171">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="ca0ce-172">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-172">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="ca0ce-173">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-173">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="ca0ce-174">Um die Risiken auszuschließen, verwenden Sie entweder die semisynchrone Kommunikation oder die synchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-174">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="ca0ce-175">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ca0ce-175">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="ca0ce-176">Wenn die ausgeführte Methode über Eingabeparameter verfügt, müssen das [**InParameters**](swbemmethod-inparameters.md) -Objekt und der *objwbeminparam* -Parameter erstellt werden, wie unter [Erstellen von inparameter-Objekten](constructing-inparameters-objects.md) und [Parsing outparameter-Objekten](parsing-outparameters-objects.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-176">If the method being executed has input parameters, the [**InParameters**](swbemmethod-inparameters.md) object and *objWbemInParam* parameter must be constructed as described in [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="ca0ce-177">Die **SWbemObject.Execmethodasync \_** -Methode geht davon aus, dass [**das durch das**](swbemobject.md) -Objekt dargestellte Objekt die auszuführende Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-177">The **SWbemObject.ExecMethodAsync\_** method assumes the object represented by [**SWbemObject**](swbemobject.md) contains the method to execute.</span></span> <span data-ttu-id="ca0ce-178">Die [**SWbemServices.Execmethodasync**](swbemservices-execmethodasync.md) -Methode erfordert einen Objekt Pfad.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-178">The [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) method requires an object path.</span></span>

## <a name="examples"></a><span data-ttu-id="ca0ce-179">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca0ce-179">Examples</span></span>

<span data-ttu-id="ca0ce-180">Das folgende Beispiel zeigt die [**ExecMethodAsync**](swbemservices-execmethodasync.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-180">The following example shows the [**ExecMethodAsync**](swbemservices-execmethodasync.md) method.</span></span> <span data-ttu-id="ca0ce-181">Das Skript erstellt ein [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Objekt, das einen Prozess darstellt, der Notepad ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-181">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="ca0ce-182">Es zeigt das Einrichten des [**InParameters**](swbemmethod-inparameters.md) -Objekts und das Abrufen von Ergebnissen von einem [**OutParameters**](swbemmethod-outparameters.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ca0ce-182">It shows setting up of [**InParameters**](swbemmethod-inparameters.md) object, and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span>

<span data-ttu-id="ca0ce-183">Informationen zu einem Skript, das die synchron ausgeführten Vorgänge anzeigt, finden Sie unter [**SWbemObject.Execmethod**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="ca0ce-183">For a script that shows the same operations performed synchronously, see [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span> <span data-ttu-id="ca0ce-184">Ein Beispiel für die Verwendung des direkten Zugriffs finden Sie unter [**Create method \_ in der Win32-Klasse**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="ca0ce-184">For an example using direct access, see [**Create Method in Class Win32\_Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="ca0ce-185">Ein Beispiel für denselben Vorgang mit einem " [**Swap Services**](swbemservices.md) "-Objekt finden Sie unter [**SWbemServices.Execmethodasync**](swbemservices-execmethodasync.md).</span><span class="sxs-lookup"><span data-stu-id="ca0ce-185">For an example of the same operation using an [**SWbemServices**](swbemservices.md) object, see [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span></span>


```VB
On Error Resume Next

'Get a Win32_Process class description
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
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

' Create a sink to receive event resulting
' from the ExecMethodAsync call.
Set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink", "Sink_")

' Call the Win32_Process.Create method asynchronously. Set up a 
' wait so the results of the method execution can be returned to 
' the sink subroutines.
bDone = false

' Call SWbemObject.ExecMethodAsync on the oProcess object.
oProcess.ExecMethodAsync_ Sink, "Create", oInParams, 0 
' 
while not bDone
    wscript.sleep 1000
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _
    & VBNewLine & "ReturnValue = " _
    & oOutParams.ReturnValue & VBNewLine & _
    "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
    & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a><span data-ttu-id="ca0ce-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca0ce-186">Requirements</span></span>



| <span data-ttu-id="ca0ce-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca0ce-187">Requirement</span></span> | <span data-ttu-id="ca0ce-188">Wert</span><span class="sxs-lookup"><span data-stu-id="ca0ce-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca0ce-189">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca0ce-189">Minimum supported client</span></span><br/> | <span data-ttu-id="ca0ce-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca0ce-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca0ce-191">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca0ce-191">Minimum supported server</span></span><br/> | <span data-ttu-id="ca0ce-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca0ce-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca0ce-193">Header</span><span class="sxs-lookup"><span data-stu-id="ca0ce-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca0ce-194"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca0ce-194"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca0ce-195">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ca0ce-195">Type library</span></span><br/>             | <dl> <span data-ttu-id="ca0ce-196"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ca0ce-196"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ca0ce-197">DLL</span><span class="sxs-lookup"><span data-stu-id="ca0ce-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca0ce-198"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca0ce-198"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ca0ce-199">CLSID</span><span class="sxs-lookup"><span data-stu-id="ca0ce-199">CLSID</span></span><br/>                    | <span data-ttu-id="ca0ce-200">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="ca0ce-200">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="ca0ce-201">IID</span><span class="sxs-lookup"><span data-stu-id="ca0ce-201">IID</span></span><br/>                      | <span data-ttu-id="ca0ce-202">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="ca0ce-202">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="ca0ce-203">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca0ce-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca0ce-204">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="ca0ce-204">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="ca0ce-205">**SWbemServices.Execmethodasync**</span><span class="sxs-lookup"><span data-stu-id="ca0ce-205">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

