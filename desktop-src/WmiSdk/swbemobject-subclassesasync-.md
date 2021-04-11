---
description: Die subclassesasync- \_ Methode von Swap-Objekten liefert asynchron die Unterklassen des aktuellen-Objekts, das eine-Klasse sein muss.
ms.assetid: 14d4a609-3aa4-49bd-bea4-6a71bc24d9dd
ms.tgt_platform: multiple
title: SWbemObject.SubclassesAsync_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6e922953e9f25aae2e47ea572678790b1228a581
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218299"
---
# <a name="swbemobjectsubclassesasync_-method"></a><span data-ttu-id="cbccc-103">Errbemubject. subclassesasync- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="cbccc-103">SWbemObject.SubclassesAsync\_ method</span></span>

<span data-ttu-id="cbccc-104">Die **subclassesasync \_** -Methode von [**Swap**](swbemobject.md) -Objekten liefert asynchron die Unterklassen des aktuellen-Objekts, das eine-Klasse sein muss.</span><span class="sxs-lookup"><span data-stu-id="cbccc-104">The **SubclassesAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously supplies the subclasses of the current object, which must be a class.</span></span>

<span data-ttu-id="cbccc-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="cbccc-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cbccc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbccc-106">Syntax</span></span>


```VB
SWbemObject.SubclassesAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="cbccc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cbccc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbccc-108">*objwbemsink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cbccc-108">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbccc-109">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cbccc-109">Required.</span></span> <span data-ttu-id="cbccc-110">Objekt Senke, die die-Objekte asynchron empfängt.</span><span class="sxs-lookup"><span data-stu-id="cbccc-110">Object sink that receives the objects asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="cbccc-111">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cbccc-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cbccc-112">Bestimmt, wie detailliert der aufzurufende Aufzählung ist.</span><span class="sxs-lookup"><span data-stu-id="cbccc-112">Determines how detailed the call enumerates.</span></span> <span data-ttu-id="cbccc-113">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="cbccc-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="cbccc-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemqueryflagdeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="cbccc-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="cbccc-115">Erzwingt eine rekursive Enumeration in alle Unterklassen, die von der angegebenen übergeordneten Klasse abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="cbccc-115">Forces recursive enumeration into all subclasses derived from the specified parent class.</span></span> <span data-ttu-id="cbccc-116">Die übergeordnete Klasse selbst wird nicht in der-Enumeration zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cbccc-116">The parent class itself is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="cbccc-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemqueryflagflache \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="cbccc-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="cbccc-118">Der Standardwert für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="cbccc-118">Default for this parameter.</span></span> <span data-ttu-id="cbccc-119">Es erzwingt, dass die Enumeration nur unmittelbare Unterklassen der angegebenen übergeordneten Klasse einschließt.</span><span class="sxs-lookup"><span data-stu-id="cbccc-119">It forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="cbccc-120"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="cbccc-120"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="cbccc-121">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den " [**slibemsink. OnProgress**](swbemsink-onprogress.md) "-Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="cbccc-121">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="cbccc-122"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="cbccc-122"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="cbccc-123">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="cbccc-123">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="cbccc-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="cbccc-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="cbccc-125">Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="cbccc-125">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="cbccc-126">Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="cbccc-126">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cbccc-127">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cbccc-127">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cbccc-128">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="cbccc-128">Typically, this is undefined.</span></span> <span data-ttu-id="cbccc-129">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="cbccc-129">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="cbccc-130">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="cbccc-130">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="cbccc-131">*objwbemasynccontext* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cbccc-131">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cbccc-132">Dabei handelt es sich um ein Objekt vom Typ " [**taubemnamedvalueset**](swbemnamedvalueset.md) ", das zur Objekt Senke zurückkehrt, um die Quelle für den ursprünglichen asynchronen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="cbccc-132">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="cbccc-133">Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen.</span><span class="sxs-lookup"><span data-stu-id="cbccc-133">Use this parameter when you make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="cbccc-134">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen-Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cbccc-134">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="cbccc-135">Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="cbccc-135">This **SWbemNamedValueSet** object is returned to the object sink, and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="cbccc-136">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="cbccc-136">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbccc-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cbccc-137">Return value</span></span>

<span data-ttu-id="cbccc-138">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cbccc-138">This method does not return a value.</span></span> <span data-ttu-id="cbccc-139">Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis für jede Instanz.</span><span class="sxs-lookup"><span data-stu-id="cbccc-139">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event for each instance.</span></span> <span data-ttu-id="cbccc-140">Nach der letzten Instanz empfängt die Objekt Senke ein [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="cbccc-140">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cbccc-141">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="cbccc-141">Error codes</span></span>

<span data-ttu-id="cbccc-142">Nach dem Abschluss der **\_ subclassesasync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="cbccc-142">After the completion of the **SubclassesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="cbccc-143">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="cbccc-143">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="cbccc-144">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen einer oder mehrerer Klassen, die durch den-Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cbccc-144">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="cbccc-145">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="cbccc-145">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="cbccc-146">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="cbccc-146">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="cbccc-147">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="cbccc-147">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="cbccc-148">Die angegebene Klasse ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cbccc-148">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="cbccc-149">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="cbccc-149">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="cbccc-150">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="cbccc-150">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="cbccc-151">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="cbccc-151">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="cbccc-152">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="cbccc-152">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbccc-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbccc-153">Remarks</span></span>

<span data-ttu-id="cbccc-154">Dieser Rückruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cbccc-154">This call returns immediately.</span></span> <span data-ttu-id="cbccc-155">Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, wenn Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cbccc-155">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="cbccc-156">Um jedes Objekt zu verarbeiten, sobald es eintrifft, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="cbccc-156">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="cbccc-157">Nachdem alle Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in ihrer Implementierung von *objwbemsink* durchführen. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="cbccc-157">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="cbccc-158">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="cbccc-158">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="cbccc-159">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="cbccc-159">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="cbccc-160">Um die Risiken auszuschließen, verwenden Sie entweder die semisynchrone Kommunikation oder die synchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="cbccc-160">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="cbccc-161">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="cbccc-161">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="cbccc-162">Es wird empfohlen, dass Skripts die Quelle des Aufrufes mithilfe eines *objwbemasynccontext* -Parameters überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cbccc-162">It is recommended that scripts verify the source of the call by using an *objWbemAsyncContext* parameter.</span></span>

<span data-ttu-id="cbccc-163">Es ist kein Fehler, wenn die zurückgegebene Auflistung keine Elemente enthält, wenn keine Unterklassen des aktuellen-Objekts vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="cbccc-163">It is not an error for the returned collection to have zero elements if there are no subclasses of the current object.</span></span> <span data-ttu-id="cbccc-164">Die **subclassesasync \_** -Methode funktioniert nur für Klassen Objekte.</span><span class="sxs-lookup"><span data-stu-id="cbccc-164">The **SubclassesAsync\_** method only works for class objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbccc-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cbccc-165">Requirements</span></span>



| <span data-ttu-id="cbccc-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbccc-166">Requirement</span></span> | <span data-ttu-id="cbccc-167">Wert</span><span class="sxs-lookup"><span data-stu-id="cbccc-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbccc-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cbccc-168">Minimum supported client</span></span><br/> | <span data-ttu-id="cbccc-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbccc-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cbccc-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cbccc-170">Minimum supported server</span></span><br/> | <span data-ttu-id="cbccc-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbccc-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cbccc-172">Header</span><span class="sxs-lookup"><span data-stu-id="cbccc-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbccc-173"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbccc-173"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cbccc-174">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="cbccc-174">Type library</span></span><br/>             | <dl> <span data-ttu-id="cbccc-175"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cbccc-175"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cbccc-176">DLL</span><span class="sxs-lookup"><span data-stu-id="cbccc-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbccc-177"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbccc-177"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cbccc-178">CLSID</span><span class="sxs-lookup"><span data-stu-id="cbccc-178">CLSID</span></span><br/>                    | <span data-ttu-id="cbccc-179">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="cbccc-179">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="cbccc-180">IID</span><span class="sxs-lookup"><span data-stu-id="cbccc-180">IID</span></span><br/>                      | <span data-ttu-id="cbccc-181">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="cbccc-181">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="cbccc-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbccc-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbccc-183">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="cbccc-183">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="cbccc-184">**Austauschen von "errbemubjectset"**</span><span class="sxs-lookup"><span data-stu-id="cbccc-184">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> <dt>

[<span data-ttu-id="cbccc-185">**Swap-aktuableitem**</span><span class="sxs-lookup"><span data-stu-id="cbccc-185">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> </dl>

 

