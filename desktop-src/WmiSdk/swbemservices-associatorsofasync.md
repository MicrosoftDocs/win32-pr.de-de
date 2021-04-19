---
description: Gibt eine Auflistung von-Objekten (Klassen oder Instanzen) zurück, die als Endpunkte bezeichnet werden, die einem angegebenen Objekt zugeordnet sind.
ms.assetid: 3969d90f-d39c-40f1-9328-fc1afbaa53b1
ms.tgt_platform: multiple
title: Swap Services. associatorsofasync-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d83f2eb33b7cd2d6ce6345d9b40a2367539dfec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356615"
---
# <a name="swbemservicesassociatorsofasync-method"></a><span data-ttu-id="9fe62-103">Methode "Swap Services. associatorsofasync"</span><span class="sxs-lookup"><span data-stu-id="9fe62-103">SWbemServices.AssociatorsOfAsync method</span></span>

<span data-ttu-id="9fe62-104">Die **associatorsofasync** -Methode des [**Swap Services**](swbemservices.md) -Objekts gibt eine Auflistung von Objekten (Klassen oder Instanzen) zurück, die als Endpunkte bezeichnet werden, die einem angegebenen Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9fe62-104">The **AssociatorsOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="9fe62-105">Der Aufruf von **associatorsofasync** wird sofort zurückgegeben, und die Ergebnisse und der Status werden an den Aufrufer über Ereignisse gesendet, die an die in *objwbemsink* angegebene Senke gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9fe62-105">The call to **AssociatorsOfAsync** returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="9fe62-106">Um jedes zurückgegebene Objekt zu verarbeiten, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="9fe62-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event handler.</span></span>

<span data-ttu-id="9fe62-107">Nachdem alle Objekte eintreffen, erfolgt die Verarbeitung in der *objwbemsink*. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9fe62-107">After all the objects arrive, processing is done in the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span> <span data-ttu-id="9fe62-108">Diese Methode führt die gleiche Funktion aus, die die assoziatoren der WQL-Abfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="9fe62-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span> <span data-ttu-id="9fe62-109">Weitere Informationen zum Erstellen einer Senke finden Sie unter [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="9fe62-109">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="9fe62-110">Die-Methode wird im asynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9fe62-110">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="9fe62-111">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="9fe62-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="9fe62-112">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9fe62-112">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9fe62-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fe62-113">Syntax</span></span>


```VB
SWbemServices.AssociatorsOfAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9fe62-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fe62-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fe62-115">*objwbemsink*</span><span class="sxs-lookup"><span data-stu-id="9fe62-115">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="9fe62-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9fe62-116">Required.</span></span> <span data-ttu-id="9fe62-117">Objekt Senke, die die-Objekte asynchron empfängt.</span><span class="sxs-lookup"><span data-stu-id="9fe62-117">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="9fe62-118">Erstellen Sie ein " [**taubemsink**](swbemsink.md) "-Objekt zum Empfangen der Objekte.</span><span class="sxs-lookup"><span data-stu-id="9fe62-118">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="9fe62-119">*strobjectpath*</span><span class="sxs-lookup"><span data-stu-id="9fe62-119">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="9fe62-120">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9fe62-120">Required.</span></span> <span data-ttu-id="9fe62-121">Eine Zeichenfolge, die den Objekt Pfad der Quell Klasse oder-Instanz enthält.</span><span class="sxs-lookup"><span data-stu-id="9fe62-121">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="9fe62-122">Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="9fe62-122">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fe62-123">*strassocclass* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="9fe62-123">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-124">Eine Zeichenfolge, die eine Association-Klasse enthält.</span><span class="sxs-lookup"><span data-stu-id="9fe62-124">String that contains an association class.</span></span> <span data-ttu-id="9fe62-125">Wenn dieser Parameter angegeben wird, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte mit der Quelle über die angegebene Zuordnungs Klasse oder eine von dieser Zuordnungs Klasse abgeleitete Klasse verknüpft werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9fe62-125">When specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="9fe62-126">" *strautclass* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="9fe62-126">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-127">Eine Zeichenfolge, die einen Klassennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="9fe62-127">String that contains a class name.</span></span> <span data-ttu-id="9fe62-128">Wenn angegeben, gibt dieser optionale Parameter an, dass die zurückgegebenen Endpunkte zu der in diesem Parameter angegebenen Klasse gehören bzw. davon abgeleitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9fe62-128">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9fe62-129">" *stringetrole* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="9fe62-129">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-130">Eine Zeichenfolge, die einen Eigenschaftsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="9fe62-130">String that contains a property name.</span></span> <span data-ttu-id="9fe62-131">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte eine bestimmte Rolle in ihrer Zuordnung zum Quell Objekt spielen müssen.</span><span class="sxs-lookup"><span data-stu-id="9fe62-131">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="9fe62-132">Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweis Eigenschaft sein muss) einer Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="9fe62-132">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="9fe62-133">*Rolle "Rolle* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="9fe62-133">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-134">Eine Zeichenfolge, die einen Eigenschaftsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="9fe62-134">String that contains a property name.</span></span> <span data-ttu-id="9fe62-135">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte an einer Zuordnung mit dem Quell Objekt teilnehmen müssen, in dem das Quell Objekt eine bestimmte Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="9fe62-135">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="9fe62-136">Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweis Eigenschaft sein muss) einer Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="9fe62-136">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="9fe62-137">*bclassesonly* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="9fe62-137">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-138">Boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle tatsächlicher Instanzen der Klassen zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9fe62-138">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="9fe62-139">Dabei handelt es sich um die Klassen, zu denen die Endpunkt Instanzen gehören.</span><span class="sxs-lookup"><span data-stu-id="9fe62-139">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="9fe62-140">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="9fe62-140">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9fe62-141">*bschemaonly* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="9fe62-141">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-142">Boolescher Wert, der angibt, ob die Abfrage auf das Schema und nicht auf die Daten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9fe62-142">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="9fe62-143">Der Standardwert für diesen Parameter ist **false**.</span><span class="sxs-lookup"><span data-stu-id="9fe62-143">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="9fe62-144">Sie kann nur auf " **true** " festgelegt werden, wenn der *strobjectpath* -Parameter den Objekt Pfad einer Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="9fe62-144">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="9fe62-145">Wenn der Wert auf **true** festgelegt ist, stellen die zurückgegebenen Endpunkte Klassen dar, die entsprechend der Quell Klasse im Schema zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9fe62-145">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="9fe62-146">"otrequirements *dassocqualifizierer* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="9fe62-146">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-147">Eine Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="9fe62-147">String that contains a qualifier name.</span></span> <span data-ttu-id="9fe62-148">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte über eine Association-Klasse, die den angegebenen Qualifizierer enthält, dem Quell Objekt zugeordnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9fe62-148">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="9fe62-149">" *stringdqualifier* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="9fe62-149">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-150">Eine Zeichenfolge, die einen Qualifizierernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="9fe62-150">String that contains a qualifier name.</span></span> <span data-ttu-id="9fe62-151">Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte den angegebenen Qualifizierer einschließen müssen.</span><span class="sxs-lookup"><span data-stu-id="9fe62-151">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="9fe62-152">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="9fe62-152">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-153">Eine ganze Zahl, die die zusätzlichen Flags für den Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="9fe62-153">Integer that specifies the additional flags to the operation.</span></span> <span data-ttu-id="9fe62-154">Der Standardwert für diesen Parameter ist **wbemflagdontsendstatus**.</span><span class="sxs-lookup"><span data-stu-id="9fe62-154">The default for this parameter is **wbemFlagDontSendStatus**.</span></span> <span data-ttu-id="9fe62-155">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="9fe62-155">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="9fe62-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="9fe62-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="9fe62-157">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="9fe62-157">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="9fe62-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="9fe62-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="9fe62-159">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="9fe62-159">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="9fe62-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="9fe62-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="9fe62-161">Bewirkt, dass WMI zusammen mit der Basisklassen Definition Klassen Änderungs Daten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9fe62-161">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="9fe62-162">Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="9fe62-162">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9fe62-163">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="9fe62-163">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-164">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="9fe62-164">Typically, this is undefined.</span></span> <span data-ttu-id="9fe62-165">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9fe62-165">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="9fe62-166">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="9fe62-166">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="9fe62-167">*objwbemasynccontext* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="9fe62-167">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-168">Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das zur Objekt Senke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufes aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9fe62-168">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="9fe62-169">Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen.</span><span class="sxs-lookup"><span data-stu-id="9fe62-169">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="9fe62-170">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9fe62-170">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="9fe62-171">Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="9fe62-171">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="9fe62-172">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="9fe62-172">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fe62-173">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fe62-173">Return value</span></span>

<span data-ttu-id="9fe62-174">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9fe62-174">This method does not return a value.</span></span> <span data-ttu-id="9fe62-175">Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="9fe62-175">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="9fe62-176">Nach der letzten Instanz empfängt die Objekt Senke ein [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9fe62-176">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9fe62-177">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="9fe62-177">Error codes</span></span>

<span data-ttu-id="9fe62-178">Nach dem Abschluss der **associatorsofasync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="9fe62-178">After the completion of the **AssociatorsOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="9fe62-179">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="9fe62-179">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-180">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen einer oder mehrerer Klassen, die durch den-Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9fe62-180">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="9fe62-181">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="9fe62-181">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-182">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="9fe62-182">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="9fe62-183">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="9fe62-183">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-184">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="9fe62-184">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="9fe62-185">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="9fe62-185">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-186">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="9fe62-186">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9fe62-187">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="9fe62-187">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="9fe62-188">Das angeforderte Element wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="9fe62-188">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fe62-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fe62-189">Remarks</span></span>

<span data-ttu-id="9fe62-190">Dieser Rückruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9fe62-190">This call returns immediately.</span></span> <span data-ttu-id="9fe62-191">Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, wenn Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9fe62-191">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="9fe62-192">Um jedes Objekt zu verarbeiten, wenn es zurückgegeben wird, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="9fe62-192">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="9fe62-193">Nachdem alle Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in ihrer Implementierung von *objwbemsink* durchführen. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9fe62-193">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="9fe62-194">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="9fe62-194">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="9fe62-195">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="9fe62-195">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="9fe62-196">Um die Risiken auszuschließen, finden Sie weitere Informationen unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="9fe62-196">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="9fe62-197">Verwenden Sie den *objwbemasynccontext* -Parameter in Skripts, um die Quelle eines Aufrufes zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9fe62-197">Use the *objWbemAsyncContext* parameter in scripts to verify the source of a call.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fe62-198">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fe62-198">Requirements</span></span>



| <span data-ttu-id="9fe62-199">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fe62-199">Requirement</span></span> | <span data-ttu-id="9fe62-200">Wert</span><span class="sxs-lookup"><span data-stu-id="9fe62-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fe62-201">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9fe62-201">Minimum supported client</span></span><br/> | <span data-ttu-id="9fe62-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fe62-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9fe62-203">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9fe62-203">Minimum supported server</span></span><br/> | <span data-ttu-id="9fe62-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fe62-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9fe62-205">Header</span><span class="sxs-lookup"><span data-stu-id="9fe62-205">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fe62-206"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fe62-206"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9fe62-207">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9fe62-207">Type library</span></span><br/>             | <dl> <span data-ttu-id="9fe62-208"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9fe62-208"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9fe62-209">DLL</span><span class="sxs-lookup"><span data-stu-id="9fe62-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fe62-210"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fe62-210"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9fe62-211">CLSID</span><span class="sxs-lookup"><span data-stu-id="9fe62-211">CLSID</span></span><br/>                    | <span data-ttu-id="9fe62-212">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="9fe62-212">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="9fe62-213">IID</span><span class="sxs-lookup"><span data-stu-id="9fe62-213">IID</span></span><br/>                      | <span data-ttu-id="9fe62-214">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="9fe62-214">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="9fe62-215">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fe62-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe62-216">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="9fe62-216">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="9fe62-217">**"Errbemujeject. ASSOCIATORS"\_**</span><span class="sxs-lookup"><span data-stu-id="9fe62-217">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="9fe62-218">**"Errbemubject. associatorsasync"\_**</span><span class="sxs-lookup"><span data-stu-id="9fe62-218">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="9fe62-219">**"Errbemubject. References"\_**</span><span class="sxs-lookup"><span data-stu-id="9fe62-219">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="9fe62-220">**Austauschen von "errbemubject. referencesasync"\_**</span><span class="sxs-lookup"><span data-stu-id="9fe62-220">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)
</dt> <dt>

[<span data-ttu-id="9fe62-221">**"Swap Services. referencesto"**</span><span class="sxs-lookup"><span data-stu-id="9fe62-221">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="9fe62-222">**"Swap Services. referencestoasync"**</span><span class="sxs-lookup"><span data-stu-id="9fe62-222">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

