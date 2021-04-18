---
description: Mit der associatorsasync- \_ Methode von "errbemubject" werden Objekte (Klassen oder Instanzen) abgerufen, die dem aktuellen Objekt zugeordnet sind. Diese Objekte werden als Endpunkte bezeichnet. Diese Methode führt die gleiche Funktion aus, die die assoziatoren der WQL-Abfrage ausführen.
ms.assetid: c71e11cd-39a5-40d8-b279-f5ee9ff3ae04
ms.tgt_platform: multiple
title: SWbemObject.AssociatorsAsync_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fe7a592327b6952308e44ac054fb94e21aa6d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347892"
---
# <a name="swbemobjectassociatorsasync_-method"></a><span data-ttu-id="c3baa-105">Errbemubject. associatorsasync- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="c3baa-105">SWbemObject.AssociatorsAsync\_ method</span></span>

<span data-ttu-id="c3baa-106">Mit der **associatorsasync \_** -Methode von " [**errbemubject**](swbemobject.md) " werden Objekte (Klassen oder Instanzen) abgerufen, die dem aktuellen Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c3baa-106">The **AssociatorsAsync\_** method of [**SWbemObject**](swbemobject.md) obtains objects (classes or instances) that are associated with the current object.</span></span> <span data-ttu-id="c3baa-107">Diese Objekte werden als Endpunkte bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c3baa-107">These objects are called endpoints.</span></span> <span data-ttu-id="c3baa-108">Diese Methode führt die gleiche Funktion aus, die die assoziatoren der WQL-Abfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3baa-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="c3baa-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c3baa-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c3baa-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3baa-110">Syntax</span></span>


```VB
SWbemObject.AssociatorsAsync_( _
  ByVal objWbemSink, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c3baa-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3baa-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3baa-112">*objwbemsink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3baa-112">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-113">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c3baa-113">Required.</span></span> <span data-ttu-id="c3baa-114">Objekt Senke, die die Objekte asynchron als Rückruf empfängt.</span><span class="sxs-lookup"><span data-stu-id="c3baa-114">Object sink that receives the objects asynchronously as a callback.</span></span>

</dd> <dt>

<span data-ttu-id="c3baa-115">*strassocclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3baa-115">*strAssocClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-116">Eine Zeichenfolge, die eine Association-Klasse enthält.</span><span class="sxs-lookup"><span data-stu-id="c3baa-116">String that contains an association class.</span></span> <span data-ttu-id="c3baa-117">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte mit der Quelle über die angegebene Zuordnungs Klasse oder eine von dieser Zuordnungs Klasse abgeleitete Klasse verknüpft werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c3baa-117">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="c3baa-118">" *strautclass* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3baa-118">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-119">Eine Zeichenfolge, die einen Klassennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="c3baa-119">String that contains a class name.</span></span> <span data-ttu-id="c3baa-120">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte der in diesem Parameter angegebenen Klasse angehören oder von dieser abgeleitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c3baa-120">If specified, this parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c3baa-121">" *stringetrole* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3baa-121">*strResultRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-122">Eine Zeichenfolge, die einen Eigenschaftsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="c3baa-122">String that contains a property name.</span></span> <span data-ttu-id="c3baa-123">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte eine bestimmte Rolle in ihrer Zuordnung zum Quell Objekt spielen müssen.</span><span class="sxs-lookup"><span data-stu-id="c3baa-123">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="c3baa-124">Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweis Eigenschaft sein muss) einer Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="c3baa-124">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="c3baa-125">*Rolle "Rolle* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3baa-125">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-126">Eine Zeichenfolge, die einen Eigenschaftsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="c3baa-126">String that contains a property name.</span></span> <span data-ttu-id="c3baa-127">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte an einer Zuordnung mit dem Quell Objekt teilnehmen müssen, in dem das Quell Objekt eine bestimmte Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="c3baa-127">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="c3baa-128">Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweis Eigenschaft sein muss) einer Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="c3baa-128">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="c3baa-129">*bclassesonly* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3baa-129">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-130">Boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle tatsächlicher Instanzen der Klassen zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3baa-130">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="c3baa-131">Dabei handelt es sich um die Klassen, zu denen die Endpunkt Instanzen gehören.</span><span class="sxs-lookup"><span data-stu-id="c3baa-131">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="c3baa-132">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="c3baa-132">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="c3baa-133">*bschemaonly* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3baa-133">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-134">Boolescher Wert, der angibt, ob die Abfrage auf das Schema und nicht auf die Daten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3baa-134">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="c3baa-135">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="c3baa-135">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="c3baa-136">Sie kann nur auf " **true** " festgelegt werden, wenn das Objekt, für das diese Methode aufgerufen wird, eine Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="c3baa-136">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="c3baa-137">Wenn der Wert auf **true** festgelegt ist, stellen die Menge der zurückgegebenen Endpunkte Klassen dar, die entsprechend der Quell Klasse im Schema zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c3baa-137">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="c3baa-138">"otrequirements *dassocqualifizierer* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3baa-138">*strRequiredAssocQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-139">Eine Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="c3baa-139">String that contains a qualifier name.</span></span> <span data-ttu-id="c3baa-140">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte über eine Association-Klasse, die den angegebenen Qualifizierer enthält, dem Quell Objekt zugeordnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c3baa-140">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="c3baa-141">" *stringdqualifier* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3baa-141">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-142">Eine Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="c3baa-142">String that contains a qualifier name.</span></span> <span data-ttu-id="c3baa-143">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte den angegebenen Qualifizierer einschließen müssen.</span><span class="sxs-lookup"><span data-stu-id="c3baa-143">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="c3baa-144">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3baa-144">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-145">Eine ganze Zahl, die zusätzliche Flags für den Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="c3baa-145">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="c3baa-146">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="c3baa-146">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="c3baa-147"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="c3baa-147"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="c3baa-148">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den " [**slibemsink. OnProgress**](swbemsink-onprogress.md) "-Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="c3baa-148">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="c3baa-149"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="c3baa-149"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c3baa-150">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="c3baa-150">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="c3baa-151"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="c3baa-151"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="c3baa-152">Bewirkt, dass WMI die lokalisierten Klassen-und Eigenschafts Beschreibungen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c3baa-152">Causes WMI to return the localized class and property descriptions.</span></span> <span data-ttu-id="c3baa-153">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="c3baa-153">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c3baa-154">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3baa-154">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-155">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c3baa-155">Typically, this is undefined.</span></span> <span data-ttu-id="c3baa-156">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c3baa-156">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="c3baa-157">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="c3baa-157">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c3baa-158">*objwbemasynccontext* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c3baa-158">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-159">Dabei handelt es sich um ein Objekt vom Typ " [**taubemnamedvalueset**](swbemnamedvalueset.md) ", das zur Objekt Senke zurückkehrt, um die Quelle für den ursprünglichen asynchronen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c3baa-159">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="c3baa-160">Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen.</span><span class="sxs-lookup"><span data-stu-id="c3baa-160">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="c3baa-161">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c3baa-161">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="c3baa-162">Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="c3baa-162">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="c3baa-163">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c3baa-163">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3baa-164">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3baa-164">Return value</span></span>

<span data-ttu-id="c3baa-165">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c3baa-165">This method does not return a value.</span></span> <span data-ttu-id="c3baa-166">Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="c3baa-166">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="c3baa-167">Nach der letzten Instanz empfängt die Objekt Senke ein [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c3baa-167">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c3baa-168">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c3baa-168">Error codes</span></span>

<span data-ttu-id="c3baa-169">Nach Abschluss der **\_ associatorsasync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="c3baa-169">After completion of the **AssociatorsAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c3baa-170">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="c3baa-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-171">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen einer oder mehrerer Klassen, die vom-Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c3baa-171">The current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="c3baa-172">**wbemErrFailed** -2147449889 (0x7fff7c21)</span><span class="sxs-lookup"><span data-stu-id="c3baa-172">**wbemErrFailed** - 2147449889 (0x7FFF7C21)</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-173">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="c3baa-173">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="c3baa-174">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="c3baa-174">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-175">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c3baa-175">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c3baa-176">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="c3baa-176">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="c3baa-177">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c3baa-177">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3baa-178">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3baa-178">Remarks</span></span>

<span data-ttu-id="c3baa-179">Dieser Rückruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c3baa-179">This call returns immediately.</span></span> <span data-ttu-id="c3baa-180">Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, indem die Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c3baa-180">The requested objects and status are returned to the caller through call-backs delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="c3baa-181">Um jedes Objekt zu verarbeiten, sobald es eintrifft, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="c3baa-181">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="c3baa-182">Nachdem alle Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in ihrer Implementierung von *objwbemsink* durchführen. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c3baa-182">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="c3baa-183">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="c3baa-183">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="c3baa-184">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="c3baa-184">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="c3baa-185">Um die Risiken auszuschließen, verwenden Sie entweder die semisynchrone Kommunikation oder die synchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="c3baa-185">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="c3baa-186">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c3baa-186">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="c3baa-187">Weitere Informationen zu den assoziatoren von zugeordneten WQL-Abfragen, Quell Instanzen und Endpunkten finden Sie unter [ASSOCIATORS of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="c3baa-187">For more information about the ASSOCIATORS OF associated WQL queries, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3baa-188">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3baa-188">Requirements</span></span>



| <span data-ttu-id="c3baa-189">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3baa-189">Requirement</span></span> | <span data-ttu-id="c3baa-190">Wert</span><span class="sxs-lookup"><span data-stu-id="c3baa-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3baa-191">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3baa-191">Minimum supported client</span></span><br/> | <span data-ttu-id="c3baa-192">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3baa-192">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c3baa-193">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3baa-193">Minimum supported server</span></span><br/> | <span data-ttu-id="c3baa-194">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3baa-194">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c3baa-195">Header</span><span class="sxs-lookup"><span data-stu-id="c3baa-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3baa-196"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3baa-196"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c3baa-197">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c3baa-197">Type library</span></span><br/>             | <dl> <span data-ttu-id="c3baa-198"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c3baa-198"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c3baa-199">DLL</span><span class="sxs-lookup"><span data-stu-id="c3baa-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3baa-200"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3baa-200"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c3baa-201">CLSID</span><span class="sxs-lookup"><span data-stu-id="c3baa-201">CLSID</span></span><br/>                    | <span data-ttu-id="c3baa-202">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="c3baa-202">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="c3baa-203">IID</span><span class="sxs-lookup"><span data-stu-id="c3baa-203">IID</span></span><br/>                      | <span data-ttu-id="c3baa-204">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="c3baa-204">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="c3baa-205">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3baa-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3baa-206">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="c3baa-206">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="c3baa-207">**Swap Services. associatorsofasync**</span><span class="sxs-lookup"><span data-stu-id="c3baa-207">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
</dt> <dt>

[<span data-ttu-id="c3baa-208">**"Errbemubject. References"\_**</span><span class="sxs-lookup"><span data-stu-id="c3baa-208">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="c3baa-209">**"Swap Services. referencesto"**</span><span class="sxs-lookup"><span data-stu-id="c3baa-209">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

