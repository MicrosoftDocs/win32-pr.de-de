---
description: Führt eine Abfrage zum Empfangen von Ereignissen aus.
ms.assetid: 0b0e8313-4ffd-4d4a-8965-d2c6743e7573
ms.tgt_platform: multiple
title: SWbemServices.Execnotificationqueryasync-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8e2ecddf290d83583b3108620b8b4bb23be7c957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347309"
---
# <a name="swbemservicesexecnotificationqueryasync-method"></a><span data-ttu-id="30c6a-103">SWbemServices.Execnotificationqueryasync-Methode</span><span class="sxs-lookup"><span data-stu-id="30c6a-103">SWbemServices.ExecNotificationQueryAsync method</span></span>

<span data-ttu-id="30c6a-104">Die **ExecNotificationQueryAsync** -Methode des-Objekts " [**Swap-Dienste**](swbemservices.md) " führt eine Abfrage zum Empfangen von Ereignissen aus.</span><span class="sxs-lookup"><span data-stu-id="30c6a-104">The **ExecNotificationQueryAsync** method of the [**SWbemServices**](swbemservices.md) object executes a query to receive events.</span></span> <span data-ttu-id="30c6a-105">Dieser Aufruf wird sofort zurückgegeben, und die Ergebnisse und der Status werden über Ereignisse an die Senke, die in *objwbemsink* angegeben ist, an den Aufrufer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="30c6a-105">This call returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span>

<span data-ttu-id="30c6a-106">Die in der Abfrage angegebenen Ereignisse können systeminterne Windows-Verwaltungsinstrumentation (WMI)-Ereignisse (z. b. [**\_ \_ instancecreationevent**](--instancecreationevent.md)) oder extrinsische Ereignisse wie z. b. [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) oder [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)sein.</span><span class="sxs-lookup"><span data-stu-id="30c6a-106">The events that are specified in the query can be intrinsic Windows Management Instrumentation (WMI) events, such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md), or extrinsic events, such as [**Win32\_IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) or [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span> <span data-ttu-id="30c6a-107">Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="30c6a-107">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="30c6a-108">Die-Methode wird im asynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="30c6a-108">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="30c6a-109">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="30c6a-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="30c6a-110">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="30c6a-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="30c6a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="30c6a-111">Syntax</span></span>


```VB
SWbemServices.ExecNotificationQueryAsync( _
  ByVal objWbemSink, _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="30c6a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="30c6a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30c6a-113">*objwbemsink*</span><span class="sxs-lookup"><span data-stu-id="30c6a-113">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="30c6a-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="30c6a-114">Required.</span></span> <span data-ttu-id="30c6a-115">Objekt Senke, die die Benachrichtigung über Ereignisse asynchron empfängt.</span><span class="sxs-lookup"><span data-stu-id="30c6a-115">Object sink that receives the notification of events asynchronously.</span></span> <span data-ttu-id="30c6a-116">Erstellen Sie ein " [**Swap**](swbemsink.md) "-Objekt, um die Objekte zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="30c6a-116">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="30c6a-117">*"-Abfrage"*</span><span class="sxs-lookup"><span data-stu-id="30c6a-117">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="30c6a-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="30c6a-118">Required.</span></span> <span data-ttu-id="30c6a-119">Eine Zeichenfolge, die den Text der ereignisbezogenen Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="30c6a-119">String that contains the text of the event-related query.</span></span> <span data-ttu-id="30c6a-120">Dieser Parameter darf nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="30c6a-120">This parameter cannot be blank.</span></span> <span data-ttu-id="30c6a-121">Weitere Informationen zum Aufbau von WMI-Abfrage Zeichenfolgen finden Sie unter [Abfragen mit WQL](querying-with-wql.md) und [WQL](wql-sql-for-wmi.md) -Referenz.</span><span class="sxs-lookup"><span data-stu-id="30c6a-121">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="30c6a-122">"in der *Sprache* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="30c6a-122">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30c6a-123">Eine Zeichenfolge, die die zu verwendende Abfragesprache enthält.</span><span class="sxs-lookup"><span data-stu-id="30c6a-123">String that contains the query language to be used.</span></span> <span data-ttu-id="30c6a-124">Wenn angegeben, muss dieser Wert "WQL" lauten.</span><span class="sxs-lookup"><span data-stu-id="30c6a-124">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="30c6a-125">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="30c6a-125">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30c6a-126">Eine ganze Zahl, die das Verhalten der Abfrage bestimmt.</span><span class="sxs-lookup"><span data-stu-id="30c6a-126">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="30c6a-127">Dieser Parameter kann auf die folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="30c6a-127">This parameter can be set to the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="30c6a-128"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="30c6a-128"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="30c6a-129">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="30c6a-129">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="30c6a-130"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="30c6a-130"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="30c6a-131">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="30c6a-131">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="30c6a-132">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="30c6a-132">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30c6a-133">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="30c6a-133">Typically, this is undefined.</span></span> <span data-ttu-id="30c6a-134">Andernfalls handelt es sich hierbei um ein Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="30c6a-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="30c6a-135">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="30c6a-135">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="30c6a-136">*objwbemasynccontext* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="30c6a-136">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30c6a-137">Dabei handelt es sich um ein Objekt vom Typ " [**taubemnamedvalueset**](swbemnamedvalueset.md) ", das zur Objekt Senke zurückkehrt, um die Quelle für den ursprünglichen asynchronen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="30c6a-137">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="30c6a-138">Verwenden Sie diesen Parameter, um mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke auszuführen.</span><span class="sxs-lookup"><span data-stu-id="30c6a-138">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="30c6a-139">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="30c6a-139">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="30c6a-140">Das Objekt " **taubemnamedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="30c6a-140">The **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="30c6a-141">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="30c6a-141">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30c6a-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30c6a-142">Return value</span></span>

<span data-ttu-id="30c6a-143">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="30c6a-143">This method does not return a value.</span></span> <span data-ttu-id="30c6a-144">Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="30c6a-144">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="30c6a-145">Nach der letzten Instanz empfängt die Objekt Senke ein [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="30c6a-145">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="30c6a-146">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="30c6a-146">Error codes</span></span>

<span data-ttu-id="30c6a-147">Nach dem Abschluss der **ExecNotificationQueryAsync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der in der folgenden Liste identifizierten Fehlercodes enthalten.</span><span class="sxs-lookup"><span data-stu-id="30c6a-147">After the completion of the **ExecNotificationQueryAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes identified in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="30c6a-148">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="30c6a-148">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="30c6a-149">Der aktuelle Benutzer ist nicht autorisiert, das Resultset anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="30c6a-149">Current user is not authorized to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="30c6a-150">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="30c6a-150">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="30c6a-151">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="30c6a-151">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="30c6a-152">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="30c6a-152">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="30c6a-153">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="30c6a-153">Invalid parameter is specified.</span></span>

</dd> <dt>

<span data-ttu-id="30c6a-154">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="30c6a-154">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="30c6a-155">Die Abfrage Syntax ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="30c6a-155">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="30c6a-156">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="30c6a-156">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="30c6a-157">Die angeforderte Abfragesprache wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30c6a-157">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="30c6a-158">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="30c6a-158">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="30c6a-159">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="30c6a-159">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30c6a-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30c6a-160">Remarks</span></span>

<span data-ttu-id="30c6a-161">Die **ExecNotificationQueryAsync** -Methode gibt Ereignistyp Objekte zurück, die von zukünftigen Ereignissen generiert werden.</span><span class="sxs-lookup"><span data-stu-id="30c6a-161">The **ExecNotificationQueryAsync** method returns event type objects that future events generate.</span></span> <span data-ttu-id="30c6a-162">Die Ereignis Objekte, die **ExecNotificationQueryAsync** -Anforderungen haben, können System intern (z. b. [**\_ \_ instancecreationevent**](--instancecreationevent.md)) oder System externe (z. b. [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) -oder SNMP-Ereignisse) sein.</span><span class="sxs-lookup"><span data-stu-id="30c6a-162">The event objects that **ExecNotificationQueryAsync** requests can be intrinsic (for example, [**\_\_InstanceCreationEvent**](--instancecreationevent.md)), or extrinsic (for example, [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) or SNMP events).</span></span> <span data-ttu-id="30c6a-163">Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="30c6a-163">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="30c6a-164">Der Aufruf von **ExecNotificationQueryAsync** wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="30c6a-164">The call to **ExecNotificationQueryAsync** returns immediately.</span></span> <span data-ttu-id="30c6a-165">Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, wenn Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="30c6a-165">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="30c6a-166">Um jedes Objekt zu verarbeiten, wenn es zurückgegeben wird, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="30c6a-166">To process each object when it is returned, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="30c6a-167">Nachdem alle Objekte zurückgegeben wurden, führen Sie die endgültige Verarbeitung aus, um die *objwbemsink*-Komponente zu implementieren. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="30c6a-167">After all the objects are returned, perform the final processing to implement the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="30c6a-168">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="30c6a-168">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="30c6a-169">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="30c6a-169">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="30c6a-170">Um die Risiken auszuschließen, finden Sie weitere Informationen unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="30c6a-170">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="30c6a-171">Es gibt Einschränkungen für die Anzahl von **-** und- **oder** -Schlüsselwörtern, die in WQL-Abfragen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="30c6a-171">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="30c6a-172">Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann dazu führen, dass WMI den Wert für die **WBEM \_ E- \_ Kontingent \_ Verletzungs** Fehlercode- **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="30c6a-172">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code asan **HRESULT** value.</span></span> <span data-ttu-id="30c6a-173">Das Limit von WQL-Schlüsselwörtern hängt von der Komplexität der Abfrage ab.</span><span class="sxs-lookup"><span data-stu-id="30c6a-173">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="30c6a-174">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30c6a-174">Examples</span></span>

<span data-ttu-id="30c6a-175">Im folgenden VBScript-Codebeispiel wird ein Skript gezeigt, das auf eine WMI-Ereignis Benachrichtigung wartet, die angibt, dass ein Prozess beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="30c6a-175">The following VBScript code example shows a script that is waiting for a WMI event notification that indicates that a process has terminated.</span></span> <span data-ttu-id="30c6a-176">Er wartet auf ein System eigenes WMI-Ereignis, eine Instanz der Ereignisklasse [**\_ \_ instancedeletionevent**](--instancedeletionevent.md).</span><span class="sxs-lookup"><span data-stu-id="30c6a-176">It is waiting for a WMI intrinsic event, an instance of the event class [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md).</span></span> <span data-ttu-id="30c6a-177">Das **\_ \_ instancedeletionevent** muss das Löschen einer Instanz des Win32- [**\_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process)darstellen.</span><span class="sxs-lookup"><span data-stu-id="30c6a-177">The **\_\_InstanceDeletionEvent** must represent the deletion of an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span> <span data-ttu-id="30c6a-178">Weitere Informationen zu systeminternen WMI-Ereignissen finden [Sie unter Bestimmen des zu empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="30c6a-178">For more information about WMI intrinsic events, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="30c6a-179">Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird.</span><span class="sxs-lookup"><span data-stu-id="30c6a-179">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="30c6a-180">Um das Skript manuell anzuhalten, verwenden Sie den Task-Manager, um den Prozess zu unterbinden.</span><span class="sxs-lookup"><span data-stu-id="30c6a-180">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="30c6a-181">Verwenden Sie zum programmgesteuerten beenden die Methode " [**Beenden**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) " in der Win32- \_ Prozess Klasse.</span><span class="sxs-lookup"><span data-stu-id="30c6a-181">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, "SELECT * FROM __InstanceCreationEvent WITHIN 1 " _
                                               & "WHERE TargetInstance ISA 'Win32_Process'"

WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo "Event occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="requirements"></a><span data-ttu-id="30c6a-182">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30c6a-182">Requirements</span></span>



| <span data-ttu-id="30c6a-183">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30c6a-183">Requirement</span></span> | <span data-ttu-id="30c6a-184">Wert</span><span class="sxs-lookup"><span data-stu-id="30c6a-184">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30c6a-185">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30c6a-185">Minimum supported client</span></span><br/> | <span data-ttu-id="30c6a-186">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30c6a-186">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="30c6a-187">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30c6a-187">Minimum supported server</span></span><br/> | <span data-ttu-id="30c6a-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30c6a-188">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="30c6a-189">Header</span><span class="sxs-lookup"><span data-stu-id="30c6a-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="30c6a-190"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="30c6a-190"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="30c6a-191">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="30c6a-191">Type library</span></span><br/>             | <dl> <span data-ttu-id="30c6a-192"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="30c6a-192"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="30c6a-193">DLL</span><span class="sxs-lookup"><span data-stu-id="30c6a-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30c6a-194"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30c6a-194"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="30c6a-195">CLSID</span><span class="sxs-lookup"><span data-stu-id="30c6a-195">CLSID</span></span><br/>                    | <span data-ttu-id="30c6a-196">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="30c6a-196">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="30c6a-197">IID</span><span class="sxs-lookup"><span data-stu-id="30c6a-197">IID</span></span><br/>                      | <span data-ttu-id="30c6a-198">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="30c6a-198">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="30c6a-199">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30c6a-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30c6a-200">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="30c6a-200">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="30c6a-201">**CquerySWbemServices.Exe**</span><span class="sxs-lookup"><span data-stu-id="30c6a-201">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
</dt> <dt>

[<span data-ttu-id="30c6a-202">**CqueryasyncSWbemServices.Exe**</span><span class="sxs-lookup"><span data-stu-id="30c6a-202">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)
</dt> <dt>

[<span data-ttu-id="30c6a-203">Registrierung für System Registrierungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="30c6a-203">Registering for System Registry Events</span></span>](registering-for-system-registry-events.md)
</dt> <dt>

[<span data-ttu-id="30c6a-204">Bestimmen des zu empfangenden Ereignis Typs</span><span class="sxs-lookup"><span data-stu-id="30c6a-204">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="30c6a-205">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="30c6a-205">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="30c6a-206">Festlegen der Sicherheit für einen asynchronen-Befehl</span><span class="sxs-lookup"><span data-stu-id="30c6a-206">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
</dt> </dl>

 

