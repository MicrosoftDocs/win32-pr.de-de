---
description: Mit der instancesasync- \_ Methode von "errbemubject" werden die Instanzen des aktuellen Klassen Objekts asynchron bereitstellt. Diese Methode implementiert eine einfache Abfrage. Komplexere Abfragen erfordern möglicherweise die Verwendung von SWbemServices.Execquery.
ms.assetid: d10fcbbf-6110-4152-8201-db43dc7a3c14
ms.tgt_platform: multiple
title: SWbemObject.InstancesAsync_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.InstancesAsync_
- ISWbemObject.InstancesAsync_
- ISWbemObject.InstancesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 800e28184593e339f739fb52d488803666f552c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863780"
---
# <a name="swbemobjectinstancesasync_-method"></a><span data-ttu-id="62c53-105">Errbemubject. instancesasync- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="62c53-105">SWbemObject.InstancesAsync\_ method</span></span>

<span data-ttu-id="62c53-106">Mit der **instancesasync \_** -Methode von " [**errbemubject**](swbemobject.md) " werden die Instanzen des aktuellen Klassen Objekts asynchron bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="62c53-106">The **InstancesAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously supplies the instances of the current class object.</span></span> <span data-ttu-id="62c53-107">Diese Methode implementiert eine einfache Abfrage.</span><span class="sxs-lookup"><span data-stu-id="62c53-107">This method implements a simple query.</span></span> <span data-ttu-id="62c53-108">Komplexere Abfragen erfordern möglicherweise die Verwendung von [**SWbemServices.Execquery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="62c53-108">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="62c53-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="62c53-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="62c53-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="62c53-110">Syntax</span></span>


```VB
SWbemObject.InstancesAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="62c53-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="62c53-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c53-112">*objwbemsink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62c53-112">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c53-113">Objekt Senke, die die-Instanzen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="62c53-113">Object sink that returns the instances.</span></span>

</dd> <dt>

<span data-ttu-id="62c53-114">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="62c53-114">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="62c53-115">Eine ganze Zahl, die das Verhalten des Aufrufes bestimmt.</span><span class="sxs-lookup"><span data-stu-id="62c53-115">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="62c53-116">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="62c53-116">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="62c53-117"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="62c53-117"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="62c53-118">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den " [**slibemsink. OnProgress**](swbemsink-onprogress.md) "-Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="62c53-118">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="62c53-119"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="62c53-119"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="62c53-120">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="62c53-120">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="62c53-121"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="62c53-121"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="62c53-122">Bewirkt, dass WMI die lokalisierten Klassen-und Eigenschafts Beschreibungen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="62c53-122">Causes WMI to return the localized class and property descriptions.</span></span> <span data-ttu-id="62c53-123">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="62c53-123">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="62c53-124">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="62c53-124">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="62c53-125">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="62c53-125">Typically, this is undefined.</span></span> <span data-ttu-id="62c53-126">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="62c53-126">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="62c53-127">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="62c53-127">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="62c53-128">*objwbemasynccontext* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="62c53-128">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="62c53-129">Dabei handelt es sich um ein Objekt vom Typ " [**taubemnamedvalueset**](swbemnamedvalueset.md) ", das zur Objekt Senke zurückkehrt, um die Quelle für den ursprünglichen asynchronen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="62c53-129">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="62c53-130">Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen.</span><span class="sxs-lookup"><span data-stu-id="62c53-130">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="62c53-131">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="62c53-131">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="62c53-132">Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="62c53-132">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="62c53-133">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="62c53-133">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62c53-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62c53-134">Return value</span></span>

<span data-ttu-id="62c53-135">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="62c53-135">This method does not return a value.</span></span> <span data-ttu-id="62c53-136">Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="62c53-136">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="62c53-137">Nach der letzten Instanz empfängt die Objekt Senke ein [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="62c53-137">After the last instance, the object sink will receive an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="62c53-138">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="62c53-138">Error codes</span></span>

<span data-ttu-id="62c53-139">Nach dem Abschluss der **instancesasync \_** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="62c53-139">After the completion of the **InstancesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="62c53-140">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="62c53-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="62c53-141">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen von Instanzen der angegebenen Klasse.</span><span class="sxs-lookup"><span data-stu-id="62c53-141">Current user does not have permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="62c53-142">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="62c53-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="62c53-143">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="62c53-143">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="62c53-144">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="62c53-144">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="62c53-145">Die angegebene Klasse ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="62c53-145">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="62c53-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="62c53-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="62c53-147">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="62c53-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="62c53-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="62c53-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="62c53-149">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="62c53-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62c53-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62c53-150">Remarks</span></span>

<span data-ttu-id="62c53-151">Dieser Rückruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="62c53-151">This call returns immediately.</span></span> <span data-ttu-id="62c53-152">Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, wenn Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="62c53-152">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="62c53-153">Um jedes Objekt zu verarbeiten, sobald es eintrifft, erstellen Sie eine *objwbemsink*.</span><span class="sxs-lookup"><span data-stu-id="62c53-153">To process each object when it arrives, create an *objWbemSink*.</span></span> <span data-ttu-id="62c53-154">[**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="62c53-154">[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="62c53-155">Nachdem alle Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in ihrer Implementierung von *objwbemsink* durchführen.</span><span class="sxs-lookup"><span data-stu-id="62c53-155">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.</span></span> <span data-ttu-id="62c53-156">[**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="62c53-156">[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="62c53-157">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="62c53-157">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="62c53-158">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="62c53-158">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="62c53-159">Um die Risiken auszuschließen, verwenden Sie entweder die semisynchrone Kommunikation oder die synchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="62c53-159">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="62c53-160">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="62c53-160">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="62c53-161">Die **instancesasync \_** -Methode funktioniert nur für Klassen Objekte.</span><span class="sxs-lookup"><span data-stu-id="62c53-161">The **InstancesAsync\_** method only works for class objects.</span></span> <span data-ttu-id="62c53-162">Es ist kein Fehler, wenn die zurückgegebene Auflistung NULL (0) Elemente aufweist.</span><span class="sxs-lookup"><span data-stu-id="62c53-162">It is not an error for the returned collection to have zero (0) elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="62c53-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62c53-163">Requirements</span></span>



| <span data-ttu-id="62c53-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62c53-164">Requirement</span></span> | <span data-ttu-id="62c53-165">Wert</span><span class="sxs-lookup"><span data-stu-id="62c53-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62c53-166">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62c53-166">Minimum supported client</span></span><br/> | <span data-ttu-id="62c53-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62c53-167">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62c53-168">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62c53-168">Minimum supported server</span></span><br/> | <span data-ttu-id="62c53-169">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62c53-169">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62c53-170">Header</span><span class="sxs-lookup"><span data-stu-id="62c53-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="62c53-171"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="62c53-171"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="62c53-172">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="62c53-172">Type library</span></span><br/>             | <dl> <span data-ttu-id="62c53-173"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="62c53-173"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="62c53-174">DLL</span><span class="sxs-lookup"><span data-stu-id="62c53-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62c53-175"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62c53-175"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="62c53-176">CLSID</span><span class="sxs-lookup"><span data-stu-id="62c53-176">CLSID</span></span><br/>                    | <span data-ttu-id="62c53-177">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="62c53-177">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="62c53-178">IID</span><span class="sxs-lookup"><span data-stu-id="62c53-178">IID</span></span><br/>                      | <span data-ttu-id="62c53-179">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="62c53-179">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="62c53-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62c53-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c53-181">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="62c53-181">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="62c53-182">**Austauschen von "errbemubjectset"**</span><span class="sxs-lookup"><span data-stu-id="62c53-182">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

