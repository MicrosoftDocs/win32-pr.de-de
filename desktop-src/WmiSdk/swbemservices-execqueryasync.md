---
description: Führt eine Abfrage zum Abrufen von Objekten aus.
ms.assetid: 50c7f62b-dd83-4117-b10e-acee1690ce8c
ms.tgt_platform: multiple
title: SWbemServices.Execqueryasync-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5564e53ef3ea185235e93bbbeb8e2a5fa001d67b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344699"
---
# <a name="swbemservicesexecqueryasync-method"></a><span data-ttu-id="56bee-103">SWbemServices.Execqueryasync-Methode</span><span class="sxs-lookup"><span data-stu-id="56bee-103">SWbemServices.ExecQueryAsync method</span></span>

<span data-ttu-id="56bee-104">Die **ExecQueryAsync** -Methode des-Objekts " [**Swap-Dienste**](swbemservices.md) " führt eine Abfrage zum Abrufen von-Objekten aus.</span><span class="sxs-lookup"><span data-stu-id="56bee-104">The **ExecQueryAsync** method of the [**SWbemServices**](swbemservices.md) object executes a query to retrieve objects.</span></span> <span data-ttu-id="56bee-105">Der Aufruf dieser Methode wird sofort zurückgegeben, und die Ergebnisse und der Status werden mithilfe von Ereignissen, die an die in *objwbemsink* angegebene Senke gesendet werden, an den Aufrufer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="56bee-105">The call to this method returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="56bee-106">Um jedes zurückgegebene Objekt zu verarbeiten, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="56bee-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span>

<span data-ttu-id="56bee-107">Die-Methode wird im asynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="56bee-107">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="56bee-108">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="56bee-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="56bee-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="56bee-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="56bee-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="56bee-110">Syntax</span></span>


```VB
objWbemObjectSet = .ExecQueryAsync( _
  [ ByVal objWbemSink ], _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="56bee-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="56bee-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56bee-112">*objwbemsink* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="56bee-112">*objWbemSink* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="56bee-113">Objekt Senke, die die Abfrage asynchron ausführt.</span><span class="sxs-lookup"><span data-stu-id="56bee-113">Object sink that executes the query asynchronously.</span></span> <span data-ttu-id="56bee-114">Erstellen Sie ein " [**taubemsink**](swbemsink.md) "-Objekt zum Empfangen der Objekte.</span><span class="sxs-lookup"><span data-stu-id="56bee-114">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="56bee-115">*"-Abfrage"*</span><span class="sxs-lookup"><span data-stu-id="56bee-115">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="56bee-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="56bee-116">Required.</span></span> <span data-ttu-id="56bee-117">Eine Zeichenfolge, die den Text der Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="56bee-117">String that contains the text of the query.</span></span> <span data-ttu-id="56bee-118">Dieser Parameter darf nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="56bee-118">This parameter cannot be blank.</span></span> <span data-ttu-id="56bee-119">Weitere Informationen zum Aufbau von WMI-Abfrage Zeichenfolgen finden Sie unter [Abfragen mit WQL](querying-with-wql.md) und [WQL](wql-sql-for-wmi.md) -Referenz.</span><span class="sxs-lookup"><span data-stu-id="56bee-119">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="56bee-120">"in der *Sprache* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="56bee-120">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="56bee-121">Eine Zeichenfolge, die die zu verwendende Abfragesprache enthält.</span><span class="sxs-lookup"><span data-stu-id="56bee-121">String that contains the query language to be used.</span></span> <span data-ttu-id="56bee-122">Wenn angegeben, muss der Wert "WQL" lauten.</span><span class="sxs-lookup"><span data-stu-id="56bee-122">If specified, the value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="56bee-123">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="56bee-123">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="56bee-124">Eine ganze Zahl, die das Verhalten der Abfrage bestimmt.</span><span class="sxs-lookup"><span data-stu-id="56bee-124">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="56bee-125">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="56bee-125">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="56bee-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="56bee-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="56bee-127">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="56bee-127">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="56bee-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="56bee-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="56bee-129">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="56bee-129">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span data-ttu-id="56bee-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemqueryflagprototype \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="56bee-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>\*\*\*\*wbemQueryFlagPrototype\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="56bee-131">Wird für einen Prototyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="56bee-131">Used for a prototype.</span></span> <span data-ttu-id="56bee-132">Die Abfrage wird beendet, und stattdessen wird ein Objekt zurückgegeben, das wie ein typisches Ergebnis Objekt aussieht.</span><span class="sxs-lookup"><span data-stu-id="56bee-132">It stops the query from happening and instead, returns an object that looks like a typical result object.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="56bee-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="56bee-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="56bee-134">Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="56bee-134">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="56bee-135">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="56bee-135">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="56bee-136">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="56bee-136">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="56bee-137">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="56bee-137">Typically, this is undefined.</span></span> <span data-ttu-id="56bee-138">Andernfalls handelt es sich hierbei um ein Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="56bee-138">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="56bee-139">Ein Anbieter, der Kontextinformationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="56bee-139">A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="56bee-140">*objwbemasynccontext* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="56bee-140">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="56bee-141">Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das zur Objekt Senke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufes aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="56bee-141">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="56bee-142">Verwenden Sie diesen Parameter, um mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke auszuführen.</span><span class="sxs-lookup"><span data-stu-id="56bee-142">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="56bee-143">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen-Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="56bee-143">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="56bee-144">Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="56bee-144">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="56bee-145">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="56bee-145">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56bee-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56bee-146">Return value</span></span>

<span data-ttu-id="56bee-147">Diese Methode hat keine Rückgabewerte.</span><span class="sxs-lookup"><span data-stu-id="56bee-147">This method has no return values.</span></span> <span data-ttu-id="56bee-148">Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="56bee-148">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="56bee-149">Nach der letzten Instanz empfängt die Objekt Senke ein [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="56bee-149">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="56bee-150">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="56bee-150">Error codes</span></span>

<span data-ttu-id="56bee-151">Nach dem Abschluss der **ExecQueryAsync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="56bee-151">After the completion of the **ExecQueryAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object can contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="56bee-152">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="56bee-152">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="56bee-153">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen des Resultsets.</span><span class="sxs-lookup"><span data-stu-id="56bee-153">Current user does not have the permission to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="56bee-154">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="56bee-154">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="56bee-155">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="56bee-155">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="56bee-156">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="56bee-156">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="56bee-157">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="56bee-157">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="56bee-158">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="56bee-158">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="56bee-159">Die Abfrage Syntax ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="56bee-159">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="56bee-160">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="56bee-160">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="56bee-161">Die angeforderte Abfragesprache wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="56bee-161">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="56bee-162">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="56bee-162">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="56bee-163">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="56bee-163">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56bee-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56bee-164">Remarks</span></span>

<span data-ttu-id="56bee-165">Dieser Rückruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="56bee-165">This call returns immediately.</span></span> <span data-ttu-id="56bee-166">Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, wenn Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="56bee-166">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="56bee-167">Um jedes Objekt zu verarbeiten, wenn es zurückgegeben wird, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="56bee-167">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="56bee-168">Nachdem alle Objekte zurückgegeben wurden, führen Sie die endgültige Verarbeitung in ihrer Implementierung von *objwbemsink* aus. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="56bee-168">After all the objects are returned, perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="56bee-169">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="56bee-169">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="56bee-170">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="56bee-170">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="56bee-171">Informationen zur Vermeidung der Risiken finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="56bee-171">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md)</span></span>

<span data-ttu-id="56bee-172">Die **ExecQueryAsync** -Methode gibt ein leeres Resultset zurück, wenn keine Objekte vorhanden sind, die mit den Kriterien in der Abfrage übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="56bee-172">The **ExecQueryAsync** method returns an empty result set when there are no objects to match the criteria in the query.</span></span> <span data-ttu-id="56bee-173">Diese Methode gibt Schlüsseleigenschaften zurück, unabhängig davon, ob die [**Key**](standard-qualifiers.md) -Eigenschaft im " *strinquery* "-Parameter angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="56bee-173">This method returns key properties whether or not the [**Key**](standard-qualifiers.md) property is requested in the *strQuery* parameter.</span></span>

<span data-ttu-id="56bee-174">Es gibt Einschränkungen für die Anzahl von **-** und- **oder** -Schlüsselwörtern, die in WQL-Abfragen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="56bee-174">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="56bee-175">Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann bewirken, dass WMI den Fehlercode der WBEM \_ E- \_ Kontingent \_ Verletzung als **HRESULT** -Wert zurückgibt</span><span class="sxs-lookup"><span data-stu-id="56bee-175">Large numbers of WQL keywords used in a complex query can cause WMI to return the WBEM\_E\_QUOTA\_VIOLATION error code as an **HRESULT** value.</span></span> <span data-ttu-id="56bee-176">Das Limit von WQL-Schlüsselwörtern hängt von der Komplexität der Abfrage ab.</span><span class="sxs-lookup"><span data-stu-id="56bee-176">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="requirements"></a><span data-ttu-id="56bee-177">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56bee-177">Requirements</span></span>



| <span data-ttu-id="56bee-178">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56bee-178">Requirement</span></span> | <span data-ttu-id="56bee-179">Wert</span><span class="sxs-lookup"><span data-stu-id="56bee-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56bee-180">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56bee-180">Minimum supported client</span></span><br/> | <span data-ttu-id="56bee-181">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56bee-181">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="56bee-182">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56bee-182">Minimum supported server</span></span><br/> | <span data-ttu-id="56bee-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56bee-183">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="56bee-184">Header</span><span class="sxs-lookup"><span data-stu-id="56bee-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="56bee-185"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="56bee-185"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="56bee-186">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="56bee-186">Type library</span></span><br/>             | <dl> <span data-ttu-id="56bee-187"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="56bee-187"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="56bee-188">DLL</span><span class="sxs-lookup"><span data-stu-id="56bee-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56bee-189"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56bee-189"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="56bee-190">CLSID</span><span class="sxs-lookup"><span data-stu-id="56bee-190">CLSID</span></span><br/>                    | <span data-ttu-id="56bee-191">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="56bee-191">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="56bee-192">IID</span><span class="sxs-lookup"><span data-stu-id="56bee-192">IID</span></span><br/>                      | <span data-ttu-id="56bee-193">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="56bee-193">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="56bee-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56bee-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56bee-195">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="56bee-195">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="56bee-196">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="56bee-196">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="56bee-197">**Austauschdienste. Get**</span><span class="sxs-lookup"><span data-stu-id="56bee-197">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> </dl>

 

