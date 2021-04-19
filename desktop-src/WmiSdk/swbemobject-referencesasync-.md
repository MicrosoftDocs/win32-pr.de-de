---
description: Die referencesasync-Methode von Swap-Objekten stellt eine Auflistung aller Zuordnungs \_ Klassen oder-Instanzen bereit, die auf das aktuelle-Objekt verweisen. Diese Methode führt die gleiche Funktion aus, die die WQL-Verweise der Abfrage ausführen.
ms.assetid: 44989726-3f68-453b-b9f5-e76fb0fbb152
ms.tgt_platform: multiple
title: SWbemObject.ReferencesAsync_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: aa4b85475a0dc9f736254c8f207469a52897b7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356617"
---
# <a name="swbemobjectreferencesasync_-method"></a><span data-ttu-id="c3a1e-104">Errbemubject. referencesasync- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="c3a1e-104">SWbemObject.ReferencesAsync\_ method</span></span>

<span data-ttu-id="c3a1e-105">Die **referencesasync \_** -Methode von [**Swap**](swbemobject.md) -Objekten stellt eine Auflistung aller Zuordnungs Klassen oder-Instanzen bereit, die auf das aktuelle-Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-105">The **ReferencesAsync\_** method of [**SWbemObject**](swbemobject.md) supplies a collection of all association classes or instances that refer to the current object.</span></span> <span data-ttu-id="c3a1e-106">Diese Methode führt die gleiche Funktion aus, die die WQL- [Verweise der](references-of-statement.md) Abfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-106">This method performs the same function that the WQL [REFERENCES OF](references-of-statement.md) query performs.</span></span>

<span data-ttu-id="c3a1e-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c3a1e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a1e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3a1e-108">Syntax</span></span>


```VB
SWbemObject.ReferencesAsync_( _
  ByVal objWbemSink, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c3a1e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3a1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3a1e-110">*objwbemsink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3a1e-110">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a1e-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-111">Required.</span></span> <span data-ttu-id="c3a1e-112">Objekt Senke, die die-Objekte asynchron empfängt.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-112">Object sink that receives the objects asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="c3a1e-113">" *strautclass* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3a1e-113">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a1e-114">Eine Zeichenfolge, die einen Klassennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-114">String that contains a class name.</span></span> <span data-ttu-id="c3a1e-115">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte der in diesem Parameter angegebenen Klasse angehören oder von dieser abgeleitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-115">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c3a1e-116">*Rolle "Rolle* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3a1e-116">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a1e-117">Eine Zeichenfolge, die einen Eigenschaftsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-117">String that contains a property name.</span></span> <span data-ttu-id="c3a1e-118">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte auf diejenigen beschränkt werden müssen, in denen das Quell Objekt eine bestimmte Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-118">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="c3a1e-119">Der Name einer angegebenen Verweis Eigenschaft definiert die Rolle einer Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-119">The name of a specified reference property defines the role of an association.</span></span>

</dd> <dt>

<span data-ttu-id="c3a1e-120">*bclassesonly* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3a1e-120">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a1e-121">Boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle tatsächlicher Instanzen der Klassen zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-121">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="c3a1e-122">Dabei handelt es sich um die Klassen, zu denen die Zuordnungs Objekte gehören.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-122">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="c3a1e-123">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-123">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="c3a1e-124">*bschemaonly* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3a1e-124">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a1e-125">Boolescher Wert, der angibt, ob die Abfrage auf das Schema und nicht auf die Daten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-125">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="c3a1e-126">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-126">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="c3a1e-127">Sie kann nur auf " **true** " festgelegt werden, wenn das Objekt, für das diese Methode aufgerufen wird, eine Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-127">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="c3a1e-128">Wenn der Wert auf **true** festgelegt ist, stellt der Satz der zurückgegebenen Endpunkte Klassen dar, die der Quell Klasse im Schema entsprechend zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-128">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="c3a1e-129">" *stringdqualifier* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3a1e-129">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a1e-130">Eine Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-130">String that contains a qualifier name.</span></span> <span data-ttu-id="c3a1e-131">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte den angegebenen Qualifizierer einschließen müssen.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-131">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="c3a1e-132">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3a1e-132">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a1e-133">Eine ganze Zahl, die zusätzliche Flags für den Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-133">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="c3a1e-134">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-134">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="c3a1e-135"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="c3a1e-135"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="c3a1e-136">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den " [**slibemsink. OnProgress**](swbemsink-onprogress.md) "-Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-136">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="c3a1e-137"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="c3a1e-137"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c3a1e-138">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-138">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="c3a1e-139"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="c3a1e-139"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="c3a1e-140">Bewirkt, dass Windows-Verwaltungsinstrumentation (WMI) Klassen Zusatzdaten mit der Basisklassen Definition zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-140">Causes Windows Management Instrumentation (WMI) to return class amendment data with the base class definition.</span></span> <span data-ttu-id="c3a1e-141">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="c3a1e-141">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c3a1e-142">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3a1e-142">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a1e-143">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-143">Typically, this is undefined.</span></span> <span data-ttu-id="c3a1e-144">Andernfalls handelt es sich hierbei um ein-Objekt vom [typswap namedvalueset](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-144">Otherwise, this is an [SWbemNamedValueSet](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="c3a1e-145">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-145">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c3a1e-146">*objwbemasynccontext* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3a1e-146">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a1e-147">Dabei handelt es sich um ein Objekt vom Typ " [taubemnamedvalueset](swbemnamedvalueset.md) ", das zur Objekt Senke zurückkehrt, um die Quelle für den ursprünglichen asynchronen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-147">This is an [SWbemNamedValueSet](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="c3a1e-148">Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-148">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="c3a1e-149">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ "Swap namedvalueset", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen-Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-149">To use this parameter, create an SWbemNamedValueSet object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="c3a1e-150">Dieses Objekt vom Typ "Swap namedvalueset" wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-150">This SWbemNamedValueSet object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="c3a1e-151">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c3a1e-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3a1e-152">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3a1e-152">Return value</span></span>

<span data-ttu-id="c3a1e-153">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-153">This method does not return a value.</span></span> <span data-ttu-id="c3a1e-154">Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-154">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="c3a1e-155">Nach der letzten Instanz empfängt die Objekt Senke ein [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-155">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c3a1e-156">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c3a1e-156">Error codes</span></span>

<span data-ttu-id="c3a1e-157">Nach dem Abschluss der **referencesasync \_** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-157">After the completion of the **ReferencesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c3a1e-158">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="c3a1e-158">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="c3a1e-159">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen einer oder mehrerer Klassen, die durch den-Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-159">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="c3a1e-160">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c3a1e-160">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c3a1e-161">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-161">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="c3a1e-162">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="c3a1e-162">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c3a1e-163">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-163">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="c3a1e-164">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="c3a1e-164">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="c3a1e-165">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-165">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3a1e-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3a1e-166">Remarks</span></span>

<span data-ttu-id="c3a1e-167">Dieser Rückruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-167">This call returns immediately.</span></span> <span data-ttu-id="c3a1e-168">Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, wenn Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-168">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="c3a1e-169">Um jedes Objekt zu verarbeiten, sobald es eintrifft, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-169">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="c3a1e-170">Nachdem alle Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in ihrer Implementierung von *objwbemsink* durchführen. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-170">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="c3a1e-171">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-171">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="c3a1e-172">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-172">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="c3a1e-173">Um die Risiken auszuschließen, verwenden Sie entweder die semisynchrone Kommunikation oder die synchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="c3a1e-173">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="c3a1e-174">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c3a1e-174">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="c3a1e-175">Weitere Informationen zu den verweisen der zugeordneten WQL-Abfrage, Quell Instanzen und Zuordnungs Objekte finden Sie unter [ASSOCIATORS of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="c3a1e-175">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3a1e-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3a1e-176">Requirements</span></span>



| <span data-ttu-id="c3a1e-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3a1e-177">Requirement</span></span> | <span data-ttu-id="c3a1e-178">Wert</span><span class="sxs-lookup"><span data-stu-id="c3a1e-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a1e-179">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3a1e-179">Minimum supported client</span></span><br/> | <span data-ttu-id="c3a1e-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3a1e-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c3a1e-181">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3a1e-181">Minimum supported server</span></span><br/> | <span data-ttu-id="c3a1e-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3a1e-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c3a1e-183">Header</span><span class="sxs-lookup"><span data-stu-id="c3a1e-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3a1e-184"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3a1e-184"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c3a1e-185">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c3a1e-185">Type library</span></span><br/>             | <dl> <span data-ttu-id="c3a1e-186"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c3a1e-186"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c3a1e-187">DLL</span><span class="sxs-lookup"><span data-stu-id="c3a1e-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3a1e-188"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3a1e-188"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c3a1e-189">CLSID</span><span class="sxs-lookup"><span data-stu-id="c3a1e-189">CLSID</span></span><br/>                    | <span data-ttu-id="c3a1e-190">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="c3a1e-190">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="c3a1e-191">IID</span><span class="sxs-lookup"><span data-stu-id="c3a1e-191">IID</span></span><br/>                      | <span data-ttu-id="c3a1e-192">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="c3a1e-192">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="c3a1e-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3a1e-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a1e-194">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-194">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="c3a1e-195">**"Errbemujeject. ASSOCIATORS"\_**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-195">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="c3a1e-196">**"Taubemservices. associatorsof"**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-196">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="c3a1e-197">**"Swap Services. referencesto"**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-197">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="c3a1e-198">**"Swap Services. referencestoasync"**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-198">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

