---
description: 'SWbemServices.ExecQueryAsync-Methode: Führt eine Abfrage aus, um Objekte abzurufen.'
ms.assetid: 50c7f62b-dd83-4117-b10e-acee1690ce8c
ms.tgt_platform: multiple
title: SWbemServices.ExecQueryAsync-Methode (Wbemdisp.h)
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
ms.openlocfilehash: 5cd3fe778ca7338df6b2674a4930458ef9113a1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118378"
---
# <a name="swbemservicesexecqueryasync-method"></a><span data-ttu-id="b0b35-103">SWbemServices.ExecQueryAsync-Methode</span><span class="sxs-lookup"><span data-stu-id="b0b35-103">SWbemServices.ExecQueryAsync method</span></span>

<span data-ttu-id="b0b35-104">Die **ExecQueryAsync-Methode** des [**SWbemServices-Objekts**](swbemservices.md) führt eine Abfrage aus, um Objekte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b0b35-104">The **ExecQueryAsync** method of the [**SWbemServices**](swbemservices.md) object executes a query to retrieve objects.</span></span> <span data-ttu-id="b0b35-105">Der Aufruf dieser Methode wird sofort zurückgegeben, und die Ergebnisse und der Status werden dem Aufrufer über Ereignisse zurückgegeben, die an die Senke übermittelt werden, die in *objWbemSink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b0b35-105">The call to this method returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="b0b35-106">Um jedes zurückgegebene Objekt zu verarbeiten, erstellen Sie einen *objWbemSink*. [**OnObjectReady-Ereignisunterroutine.**](swbemsink-onobjectready.md)</span><span class="sxs-lookup"><span data-stu-id="b0b35-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span>

<span data-ttu-id="b0b35-107">Die -Methode wird im asynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b0b35-107">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="b0b35-108">Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)</span><span class="sxs-lookup"><span data-stu-id="b0b35-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="b0b35-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)</span><span class="sxs-lookup"><span data-stu-id="b0b35-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0b35-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0b35-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="b0b35-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0b35-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0b35-112">*objWbemSink* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="b0b35-112">*objWbemSink* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0b35-113">Objektsenke, die die Abfrage asynchron ausführt.</span><span class="sxs-lookup"><span data-stu-id="b0b35-113">Object sink that executes the query asynchronously.</span></span> <span data-ttu-id="b0b35-114">Erstellen Sie ein [**SWbemSink-Objekt,**](swbemsink.md) um die Objekte zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="b0b35-114">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="b0b35-115">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="b0b35-115">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="b0b35-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b0b35-116">Required.</span></span> <span data-ttu-id="b0b35-117">Zeichenfolge, die den Text der Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="b0b35-117">String that contains the text of the query.</span></span> <span data-ttu-id="b0b35-118">Dieser Parameter darf nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="b0b35-118">This parameter cannot be blank.</span></span> <span data-ttu-id="b0b35-119">Weitere Informationen zum Erstellen von WMI-Abfragezeichenfolgen finden Sie unter [Abfragen mit WQL](querying-with-wql.md) und in der [WQL-Referenz.](wql-sql-for-wmi.md)</span><span class="sxs-lookup"><span data-stu-id="b0b35-119">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="b0b35-120">*strQueryLanguage* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="b0b35-120">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0b35-121">Zeichenfolge, die die zu verwendende Abfragesprache enthält.</span><span class="sxs-lookup"><span data-stu-id="b0b35-121">String that contains the query language to be used.</span></span> <span data-ttu-id="b0b35-122">Wenn angegeben, muss der Wert "WQL" sein.</span><span class="sxs-lookup"><span data-stu-id="b0b35-122">If specified, the value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="b0b35-123">*iFlags* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="b0b35-123">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0b35-124">Eine ganze Zahl, die das Verhalten der Abfrage bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b0b35-124">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="b0b35-125">Dieser Parameter kann die folgenden Werte akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="b0b35-125">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="b0b35-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus\*\* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="b0b35-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="b0b35-127">Bewirkt, dass asynchrone Aufrufe Statusupdates an den [**OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.</span><span class="sxs-lookup"><span data-stu-id="b0b35-127">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="b0b35-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus\*\* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b0b35-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b0b35-129">Verhindert, dass asynchrone Aufrufe Statusupdates an den [**OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.</span><span class="sxs-lookup"><span data-stu-id="b0b35-129">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span data-ttu-id="b0b35-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype\*\* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="b0b35-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>\*\*\*\*wbemQueryFlagPrototype\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="b0b35-131">Wird für einen Prototyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="b0b35-131">Used for a prototype.</span></span> <span data-ttu-id="b0b35-132">Sie verhindert die Abfrage und gibt stattdessen ein Objekt zurück, das wie ein typisches Ergebnisobjekt aussieht.</span><span class="sxs-lookup"><span data-stu-id="b0b35-132">It stops the query from happening and instead, returns an object that looks like a typical result object.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="b0b35-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers\*\* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="b0b35-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="b0b35-134">Bewirkt, dass WMI Klassenänderungsdaten mit der Basisklassendefinition zurück gibt.</span><span class="sxs-lookup"><span data-stu-id="b0b35-134">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="b0b35-135">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klasseninformationen.](localizing-wmi-class-information.md)</span><span class="sxs-lookup"><span data-stu-id="b0b35-135">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b0b35-136">*objwbemNamedValueSet* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="b0b35-136">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0b35-137">In der Regel ist dies nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="b0b35-137">Typically, this is undefined.</span></span> <span data-ttu-id="b0b35-138">Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung dienstanbietert.</span><span class="sxs-lookup"><span data-stu-id="b0b35-138">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="b0b35-139">Ein Anbieter, der Kontextinformationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="b0b35-139">A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="b0b35-140">*objWbemAsyncContext* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="b0b35-140">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0b35-141">Ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das zur Objektsenke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufs zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b0b35-141">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="b0b35-142">Verwenden Sie diesen Parameter, um mehrere asynchrone Aufrufe mit derselben Objektsenke zu tätigen.</span><span class="sxs-lookup"><span data-stu-id="b0b35-142">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="b0b35-143">Um diesen Parameter zu verwenden, erstellen Sie ein **SWbemNamedValueSet-Objekt,** und verwenden Sie die [**SWbemNamedValueSet.Add-Methode,**](swbemnamedvalueset-add.md) um einen Wert hinzuzufügen, der den asynchronen Aufruf identifiziert, den Sie ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0b35-143">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="b0b35-144">Dieses **SWbemNamedValueSet-Objekt** wird an die Objektsenke zurückgegeben, und die Quelle des Aufrufs kann mithilfe der [**SWbemNamedValueSet.Item-Methode**](swbemnamedvalueset-item.md) extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="b0b35-144">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="b0b35-145">Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)</span><span class="sxs-lookup"><span data-stu-id="b0b35-145">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0b35-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0b35-146">Return value</span></span>

<span data-ttu-id="b0b35-147">Diese Methode verfügt über keine Rückgabewerte.</span><span class="sxs-lookup"><span data-stu-id="b0b35-147">This method has no return values.</span></span> <span data-ttu-id="b0b35-148">Bei Erfolg empfängt die Senke ein [**OnObjectReady-Ereignis**](swbemsink-onobjectready.md) pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="b0b35-148">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="b0b35-149">Nach der letzten Instanz empfängt die Objektsenke ein [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)</span><span class="sxs-lookup"><span data-stu-id="b0b35-149">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b0b35-150">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b0b35-150">Error codes</span></span>

<span data-ttu-id="b0b35-151">Nach Abschluss der **ExecQueryAsync-Methode** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="b0b35-151">After the completion of the **ExecQueryAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object can contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b0b35-152">**wbemErrAccessDenied** – 2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="b0b35-152">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b0b35-153">Der aktuelle Benutzer verfügt nicht über die Berechtigung, das Resultset anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b0b35-153">Current user does not have the permission to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="b0b35-154">**wbemErrFailed** – 2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b0b35-154">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b0b35-155">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="b0b35-155">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b0b35-156">**wbemErrInvalidParameter** – 2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b0b35-156">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b0b35-157">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="b0b35-157">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="b0b35-158">**wbemErrInvalidQuery** – 2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="b0b35-158">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="b0b35-159">Die Abfragesyntax ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b0b35-159">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b0b35-160">**wbemErrInvalidQueryType** – 2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="b0b35-160">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="b0b35-161">Die angeforderte Abfragesprache wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b0b35-161">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b0b35-162">**wbemErrOutOfMemory** – 2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b0b35-162">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b0b35-163">Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b0b35-163">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0b35-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0b35-164">Remarks</span></span>

<span data-ttu-id="b0b35-165">Dieser Aufruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b0b35-165">This call returns immediately.</span></span> <span data-ttu-id="b0b35-166">Die angeforderten Objekte und der Status werden dem Aufrufer über Rückrufe zurückgegeben, die an die Senke übermittelt werden, die in *objWbemSink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b0b35-166">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="b0b35-167">Um jedes Objekt zu verarbeiten, wenn es zurückgegeben wird, erstellen Sie einen *objWbemSink*. [**OnObjectReady-Ereignisunterroutine.**](swbemsink-onobjectready.md)</span><span class="sxs-lookup"><span data-stu-id="b0b35-167">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="b0b35-168">Nachdem alle -Objekte zurückgegeben wurden, führen Sie die endgültige Verarbeitung in Ihrer Implementierung von *objWbemSink aus.* [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)</span><span class="sxs-lookup"><span data-stu-id="b0b35-168">After all the objects are returned, perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="b0b35-169">Ein asynchroner Rückruf ermöglicht es einem nicht authentifizierten Benutzer, Daten für die Senke zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="b0b35-169">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="b0b35-170">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="b0b35-170">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="b0b35-171">Informationen zum Beseitigen der Risiken finden Sie unter [Festlegen der Sicherheit für einen asynchronen Aufruf.](setting-security-on-an-asynchronous-call.md)</span><span class="sxs-lookup"><span data-stu-id="b0b35-171">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md)</span></span>

<span data-ttu-id="b0b35-172">Die **ExecQueryAsync-Methode** gibt ein leeres Resultset zurück, wenn es keine Objekte gibt, die den Kriterien in der Abfrage entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b0b35-172">The **ExecQueryAsync** method returns an empty result set when there are no objects to match the criteria in the query.</span></span> <span data-ttu-id="b0b35-173">Diese Methode gibt Schlüsseleigenschaften zurück, unabhängig davon, ob die [**Key-Eigenschaft**](standard-qualifiers.md) im *strQuery-Parameter angefordert* wird.</span><span class="sxs-lookup"><span data-stu-id="b0b35-173">This method returns key properties whether or not the [**Key**](standard-qualifiers.md) property is requested in the *strQuery* parameter.</span></span>

<span data-ttu-id="b0b35-174">Die Anzahl der SCHLÜSSELWÖRTER **AND** und **OR,** die in WQL-Abfragen verwendet werden können, ist begrenzt.</span><span class="sxs-lookup"><span data-stu-id="b0b35-174">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="b0b35-175">Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann dazu führen, dass WMI den WBEM \_ E \_ QUOTA \_ VIOLATION-Fehlercode als **HRESULT-Wert** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b0b35-175">Large numbers of WQL keywords used in a complex query can cause WMI to return the WBEM\_E\_QUOTA\_VIOLATION error code as an **HRESULT** value.</span></span> <span data-ttu-id="b0b35-176">Der Grenzwert für WQL-Schlüsselwörter hängt davon ab, wie komplex die Abfrage ist.</span><span class="sxs-lookup"><span data-stu-id="b0b35-176">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b35-177">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0b35-177">Requirements</span></span>



| <span data-ttu-id="b0b35-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0b35-178">Requirement</span></span> | <span data-ttu-id="b0b35-179">Wert</span><span class="sxs-lookup"><span data-stu-id="b0b35-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b35-180">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0b35-180">Minimum supported client</span></span><br/> | <span data-ttu-id="b0b35-181">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0b35-181">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b0b35-182">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0b35-182">Minimum supported server</span></span><br/> | <span data-ttu-id="b0b35-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0b35-183">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0b35-184">Header</span><span class="sxs-lookup"><span data-stu-id="b0b35-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0b35-185"><dt>Wbemdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="b0b35-185"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0b35-186">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b0b35-186">Type library</span></span><br/>             | <dl> <span data-ttu-id="b0b35-187"><dt>Wbemdisp.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b0b35-187"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b0b35-188">DLL</span><span class="sxs-lookup"><span data-stu-id="b0b35-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0b35-189"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0b35-189"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b0b35-190">CLSID</span><span class="sxs-lookup"><span data-stu-id="b0b35-190">CLSID</span></span><br/>                    | <span data-ttu-id="b0b35-191">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="b0b35-191">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="b0b35-192">IID</span><span class="sxs-lookup"><span data-stu-id="b0b35-192">IID</span></span><br/>                      | <span data-ttu-id="b0b35-193">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="b0b35-193">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="b0b35-194">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b0b35-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0b35-195">**Swbemservices**</span><span class="sxs-lookup"><span data-stu-id="b0b35-195">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="b0b35-196">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="b0b35-196">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="b0b35-197">**SWbemServices.Get**</span><span class="sxs-lookup"><span data-stu-id="b0b35-197">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> </dl>

 

