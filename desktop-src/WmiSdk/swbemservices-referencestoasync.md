---
description: Gibt alle Zuordnungs Klassen oder-Instanzen zurück, die auf eine bestimmte Quell Klasse oder-Instanz verweisen.
ms.assetid: 2ad66ea1-b8f0-4b6b-b68f-29496afbe4bf
ms.tgt_platform: multiple
title: "\"Swap Services. referencestoasync\"-Methode (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 64a8b9b336a1e7aa6007b17d2e878f1ace5e6163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350562"
---
# <a name="swbemservicesreferencestoasync-method"></a><span data-ttu-id="1cc89-103">Swap Services. referencestoasync-Methode</span><span class="sxs-lookup"><span data-stu-id="1cc89-103">SWbemServices.ReferencesToAsync method</span></span>

<span data-ttu-id="1cc89-104">Die **referencestoasync** -Methode des [**Swap Services**](swbemservices.md) -Objekts gibt alle Zuordnungs Klassen oder-Instanzen zurück, die auf eine bestimmte Quell Klasse oder Instanz verweisen.</span><span class="sxs-lookup"><span data-stu-id="1cc89-104">The **ReferencesToAsync** method of the [**SWbemServices**](swbemservices.md) object returns all association classes or instances that refer to a specific source class or instance.</span></span> <span data-ttu-id="1cc89-105">Diese Methode führt die gleiche Funktion aus, die die [Verweise der](references-of-statement.md) WQL-Abfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="1cc89-105">This method performs the same function that the [REFERENCES OF](references-of-statement.md) WQL query performs.</span></span>

<span data-ttu-id="1cc89-106">Weitere Informationen zum asynchronen Modus finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="1cc89-106">For more information about the asynchronous mode, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="1cc89-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1cc89-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc89-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cc89-108">Syntax</span></span>


```VB
SWbemServices.ReferencesToAsync( _
  ByVal ObjWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="1cc89-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cc89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc89-110">*Objwbemsink*</span><span class="sxs-lookup"><span data-stu-id="1cc89-110">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="1cc89-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1cc89-111">Required.</span></span> <span data-ttu-id="1cc89-112">Objekt Senke, die die-Objekte asynchron empfängt.</span><span class="sxs-lookup"><span data-stu-id="1cc89-112">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="1cc89-113">Erstellen Sie ein " [**Swap**](swbemsink.md) "-Objekt, um die Objekte zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="1cc89-113">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="1cc89-114">*strobjectpath*</span><span class="sxs-lookup"><span data-stu-id="1cc89-114">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="1cc89-115">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1cc89-115">Required.</span></span> <span data-ttu-id="1cc89-116">Eine Zeichenfolge, die den Objekt Pfad der Quelle für diese Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="1cc89-116">String that contains the object path of the source for this method.</span></span> <span data-ttu-id="1cc89-117">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="1cc89-117">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cc89-118">" *strautclass* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="1cc89-118">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc89-119">Eine Zeichenfolge, die einen Klassennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="1cc89-119">String that contains a class name.</span></span> <span data-ttu-id="1cc89-120">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte der in diesem Parameter angegebenen Klasse angehören oder von dieser abgeleitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1cc89-120">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class that is specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1cc89-121">*Rolle "Rolle* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="1cc89-121">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc89-122">Eine Zeichenfolge, die einen Eigenschaftsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="1cc89-122">String that contains a property name.</span></span> <span data-ttu-id="1cc89-123">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte auf diejenigen beschränkt werden müssen, in denen das Quell Objekt eine bestimmte Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="1cc89-123">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="1cc89-124">Die Rolle wird durch den Namen einer angegebenen Verweis Eigenschaft einer Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="1cc89-124">The role is defined by the name of a specified reference property of an association.</span></span>

</dd> <dt>

<span data-ttu-id="1cc89-125">*bclassesonly* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="1cc89-125">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc89-126">Boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle tatsächlicher Instanzen der Klassen zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="1cc89-126">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="1cc89-127">Dabei handelt es sich um die Klassen, zu denen die Zuordnungs Objekte gehören.</span><span class="sxs-lookup"><span data-stu-id="1cc89-127">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="1cc89-128">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="1cc89-128">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cc89-129">*bschemaonly* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="1cc89-129">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc89-130">Boolescher Wert, der angibt, ob die Abfrage auf das Schema und nicht auf die Daten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1cc89-130">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="1cc89-131">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="1cc89-131">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="1cc89-132">Sie kann nur auf " **true** " festgelegt werden, wenn der *strobjectpath* -Parameter den Objekt Pfad einer Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="1cc89-132">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="1cc89-133">Wenn der Wert auf **true** festgelegt ist, stellt der Satz der zurückgegebenen Endpunkte Klassen dar, die der Quell Klasse im Schema zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1cc89-133">When set to **TRUE**, the set of returned endpoints represents classes that are associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="1cc89-134">" *stringdqualifier* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="1cc89-134">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc89-135">Eine Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="1cc89-135">String that contains a qualifier name.</span></span> <span data-ttu-id="1cc89-136">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte den angegebenen Qualifizierer einschließen müssen.</span><span class="sxs-lookup"><span data-stu-id="1cc89-136">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="1cc89-137">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="1cc89-137">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc89-138">Eine ganze Zahl, die zusätzliche Flags für den Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="1cc89-138">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="1cc89-139">Der Standardwert für diesen Parameter ist **wbemflagbidirektional**.</span><span class="sxs-lookup"><span data-stu-id="1cc89-139">The default for this parameter is **wbemFlagBidirectional**.</span></span> <span data-ttu-id="1cc89-140">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="1cc89-140">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="1cc89-141"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="1cc89-141"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="1cc89-142">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="1cc89-142">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="1cc89-143"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="1cc89-143"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="1cc89-144">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="1cc89-144">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="1cc89-145"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="1cc89-145"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="1cc89-146">Bewirkt, dass Windows-Verwaltungsinstrumentation (WMI) zusammen mit der Basisklassen Definition Klassen Änderungs Daten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1cc89-146">Causes Windows Management Instrumentation (WMI) to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="1cc89-147">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="1cc89-147">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1cc89-148">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="1cc89-148">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc89-149">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="1cc89-149">Typically, this is undefined.</span></span> <span data-ttu-id="1cc89-150">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="1cc89-150">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="1cc89-151">Ein Anbieter, der Kontextinformationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="1cc89-151">A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="1cc89-152">*objwbemasynccontext* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="1cc89-152">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc89-153">Dabei handelt es sich um ein Objekt vom Typ " [**taubemnamedvalueset**](swbemnamedvalueset.md) ", das zur Objekt Senke zurückkehrt, um die Quelle für den ursprünglichen asynchronen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1cc89-153">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="1cc89-154">Verwenden Sie diesen Parameter, um mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1cc89-154">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="1cc89-155">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen-Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1cc89-155">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="1cc89-156">Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="1cc89-156">This **SWbemNamedValueSet** object is returned to the object sink, and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="1cc89-157">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="1cc89-157">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc89-158">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1cc89-158">Return value</span></span>

<span data-ttu-id="1cc89-159">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1cc89-159">This method does not return a value.</span></span> <span data-ttu-id="1cc89-160">Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="1cc89-160">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="1cc89-161">Nach der letzten Instanz empfängt die Objekt Senke ein [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1cc89-161">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1cc89-162">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="1cc89-162">Error codes</span></span>

<span data-ttu-id="1cc89-163">Nach dem Abschluss der **referencestoasync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="1cc89-163">After the completion of the **ReferencesToAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="1cc89-164">Eine zurückgegebene Auflistung mit 0 (null) Elementen ist kein Fehler.</span><span class="sxs-lookup"><span data-stu-id="1cc89-164">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="1cc89-165">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="1cc89-165">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="1cc89-166">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen einer oder mehrerer Klassen, die durch den-Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1cc89-166">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="1cc89-167">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="1cc89-167">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="1cc89-168">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="1cc89-168">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="1cc89-169">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="1cc89-169">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="1cc89-170">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="1cc89-170">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="1cc89-171">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="1cc89-171">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="1cc89-172">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="1cc89-172">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1cc89-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cc89-173">Remarks</span></span>

<span data-ttu-id="1cc89-174">Dieser Rückruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1cc89-174">This call returns immediately.</span></span> <span data-ttu-id="1cc89-175">Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, wenn Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1cc89-175">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="1cc89-176">Um jedes Objekt zu verarbeiten, wenn es zurückgegeben wird, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="1cc89-176">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="1cc89-177">Nachdem alle Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in ihrer Implementierung von *objwbemsink* durchführen. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1cc89-177">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="1cc89-178">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="1cc89-178">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="1cc89-179">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="1cc89-179">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="1cc89-180">Um die Risiken auszuschließen, finden Sie weitere Informationen unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="1cc89-180">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc89-181">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1cc89-181">Requirements</span></span>



| <span data-ttu-id="1cc89-182">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1cc89-182">Requirement</span></span> | <span data-ttu-id="1cc89-183">Wert</span><span class="sxs-lookup"><span data-stu-id="1cc89-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc89-184">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1cc89-184">Minimum supported client</span></span><br/> | <span data-ttu-id="1cc89-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1cc89-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1cc89-186">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1cc89-186">Minimum supported server</span></span><br/> | <span data-ttu-id="1cc89-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1cc89-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1cc89-188">Header</span><span class="sxs-lookup"><span data-stu-id="1cc89-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cc89-189"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cc89-189"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1cc89-190">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1cc89-190">Type library</span></span><br/>             | <dl> <span data-ttu-id="1cc89-191"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1cc89-191"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1cc89-192">DLL</span><span class="sxs-lookup"><span data-stu-id="1cc89-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cc89-193"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cc89-193"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1cc89-194">CLSID</span><span class="sxs-lookup"><span data-stu-id="1cc89-194">CLSID</span></span><br/>                    | <span data-ttu-id="1cc89-195">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="1cc89-195">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="1cc89-196">IID</span><span class="sxs-lookup"><span data-stu-id="1cc89-196">IID</span></span><br/>                      | <span data-ttu-id="1cc89-197">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="1cc89-197">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="1cc89-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cc89-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc89-199">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="1cc89-199">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="1cc89-200">**"Errbemujeject. ASSOCIATORS"\_**</span><span class="sxs-lookup"><span data-stu-id="1cc89-200">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="1cc89-201">**"Errbemubject. References"\_**</span><span class="sxs-lookup"><span data-stu-id="1cc89-201">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="1cc89-202">**"Taubemservices. associatorsof"**</span><span class="sxs-lookup"><span data-stu-id="1cc89-202">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

