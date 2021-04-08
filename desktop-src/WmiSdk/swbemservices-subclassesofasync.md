---
description: Gibt eine Auflistung von Unterklassen für eine angegebene Klasse zurück.
ms.assetid: a9d16ee9-992e-4ce5-9c03-0a2c9958588c
ms.tgt_platform: multiple
title: Swap Services. subclassesofasync-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d8d325c96ea1a292d8ac3afc76bfea619fe5a143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960097"
---
# <a name="swbemservicessubclassesofasync-method"></a><span data-ttu-id="b7add-103">Methode "Swap Services. subclassesofasync"</span><span class="sxs-lookup"><span data-stu-id="b7add-103">SWbemServices.SubclassesOfAsync method</span></span>

<span data-ttu-id="b7add-104">Die **subclassesofasync** -Methode des [**Swap Services**](swbemservices.md) -Objekts gibt eine Auflistung von Unterklassen für eine angegebene Klasse zurück.</span><span class="sxs-lookup"><span data-stu-id="b7add-104">The **SubclassesOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of subclasses for a specified class.</span></span> <span data-ttu-id="b7add-105">Verwenden Sie diese Methode nur für Klassen Objekte.</span><span class="sxs-lookup"><span data-stu-id="b7add-105">Only use this method for class objects.</span></span>

<span data-ttu-id="b7add-106">Diese Methode wird im asynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b7add-106">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="b7add-107">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b7add-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="b7add-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b7add-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7add-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7add-109">Syntax</span></span>


```VB
SWbemServices.SubclassesOfAsync( _
  ByVal ObjWbemSink, _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b7add-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7add-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7add-111">*Objwbemsink*</span><span class="sxs-lookup"><span data-stu-id="b7add-111">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="b7add-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b7add-112">Required.</span></span> <span data-ttu-id="b7add-113">Objekt Senke, die die Unterklassen asynchron empfängt.</span><span class="sxs-lookup"><span data-stu-id="b7add-113">Object sink that receives the subclasses asynchronously.</span></span> <span data-ttu-id="b7add-114">Erstellen Sie ein " [**Swap**](swbemsink.md) "-Objekt, um die Objekte zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="b7add-114">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="b7add-115">" *Strauch Klasse* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="b7add-115">*strSuperclass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7add-116">Gibt einen übergeordneten Klassennamen an.</span><span class="sxs-lookup"><span data-stu-id="b7add-116">Specifies a parent class name.</span></span> <span data-ttu-id="b7add-117">Nur die Klassen, die Unterklassen dieser Klasse sind, werden im Enumerator zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b7add-117">Only the classes that are subclasses of this class are returned in the enumerator.</span></span> <span data-ttu-id="b7add-118">Wenn dieser Parameter leer ist, und wenn *IFlags* den Wert **wbemqueryflagparent** hat, werden nur die Klassen der obersten Ebene zurückgegeben (d. h. Klassen, die über keine übergeordnete Klasse verfügen).</span><span class="sxs-lookup"><span data-stu-id="b7add-118">If this parameter is blank, and if *iFlags* is **wbemQueryFlagShallow**, only the top-level classes are returned (that is, classes that have no parent class).</span></span> <span data-ttu-id="b7add-119">Wenn dieser Parameter leer ist, und *IFlags* den Wert **wbemqueryflagdeep** hat, werden alle Klassen im Namespace zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b7add-119">If this parameter is blank, and if *iFlags* is **wbemQueryFlagDeep**, all classes within the namespace are returned.</span></span>

</dd> <dt>

<span data-ttu-id="b7add-120">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="b7add-120">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7add-121">Bestimmt die Tiefe der aufrufenumeration.</span><span class="sxs-lookup"><span data-stu-id="b7add-121">Determines the depth of the call enumeration.</span></span> <span data-ttu-id="b7add-122">Der Standardwert für diesen Parameter ist **wbemqueryflagdeep**.</span><span class="sxs-lookup"><span data-stu-id="b7add-122">The default value for this parameter is **wbemQueryFlagDeep**.</span></span> <span data-ttu-id="b7add-123">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="b7add-123">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="b7add-124"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemqueryflagflache \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="b7add-124"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="b7add-125">Erzwingt, dass die Enumeration nur unmittelbare Unterklassen der angegebenen übergeordneten Klasse einschließt.</span><span class="sxs-lookup"><span data-stu-id="b7add-125">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="b7add-126"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemqueryflagdeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b7add-126"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b7add-127">Der Standardwert für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="b7add-127">Default for this parameter.</span></span> <span data-ttu-id="b7add-128">Dieser Wert erzwingt eine rekursive Enumeration in alle Unterklassen, die von der angegebenen übergeordneten Klasse abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="b7add-128">This value forces recursive enumeration into all subclasses that are derived from the specified parent class.</span></span> <span data-ttu-id="b7add-129">Die übergeordnete Klasse wird nicht in der-Enumeration zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b7add-129">The parent class is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="b7add-130"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="b7add-130"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="b7add-131">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="b7add-131">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="b7add-132"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b7add-132"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b7add-133">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="b7add-133">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="b7add-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="b7add-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="b7add-135">Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b7add-135">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="b7add-136">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="b7add-136">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b7add-137">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="b7add-137">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7add-138">In der Regel ist dieser Parameter nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="b7add-138">Typically, this parameter is undefined.</span></span> <span data-ttu-id="b7add-139">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b7add-139">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="b7add-140">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="b7add-140">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="b7add-141">*objwbemasynccontext* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="b7add-141">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7add-142">Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das zur Objekt Senke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufes aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b7add-142">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="b7add-143">Verwenden Sie diesen Parameter, um mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b7add-143">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="b7add-144">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b7add-144">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="b7add-145">Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="b7add-145">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="b7add-146">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b7add-146">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7add-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7add-147">Return value</span></span>

<span data-ttu-id="b7add-148">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b7add-148">This method does not return a value.</span></span> <span data-ttu-id="b7add-149">Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="b7add-149">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="b7add-150">Nach der letzten Instanz empfängt die Objekt Senke ein [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="b7add-150">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b7add-151">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b7add-151">Error codes</span></span>

<span data-ttu-id="b7add-152">Nach dem Abschluss der **subclassesofasync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="b7add-152">After the completion of the **SubclassesOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="b7add-153">Eine zurückgegebene Auflistung mit 0 (null) Elementen ist kein Fehler.</span><span class="sxs-lookup"><span data-stu-id="b7add-153">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="b7add-154">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="b7add-154">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b7add-155">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen einer oder mehrerer Klassen, die durch den-Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b7add-155">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="b7add-156">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b7add-156">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b7add-157">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="b7add-157">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b7add-158">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="b7add-158">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="b7add-159">Die angegebene Klasse ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b7add-159">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="b7add-160">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b7add-160">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b7add-161">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="b7add-161">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="b7add-162">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b7add-162">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b7add-163">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b7add-163">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7add-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7add-164">Remarks</span></span>

<span data-ttu-id="b7add-165">Dieser Rückruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b7add-165">This call returns immediately.</span></span> <span data-ttu-id="b7add-166">Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, wenn Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b7add-166">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="b7add-167">Um jedes Objekt zu verarbeiten, sobald es eintrifft, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="b7add-167">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="b7add-168">Nachdem alle Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in ihrer Implementierung von *objwbemsink* ausführen. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="b7add-168">After all the objects are returned, you can perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="b7add-169">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="b7add-169">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="b7add-170">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="b7add-170">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="b7add-171">Um die Risiken auszuschließen, finden Sie weitere Informationen unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="b7add-171">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7add-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7add-172">Requirements</span></span>



| <span data-ttu-id="b7add-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7add-173">Requirement</span></span> | <span data-ttu-id="b7add-174">Wert</span><span class="sxs-lookup"><span data-stu-id="b7add-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7add-175">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7add-175">Minimum supported client</span></span><br/> | <span data-ttu-id="b7add-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7add-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7add-177">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7add-177">Minimum supported server</span></span><br/> | <span data-ttu-id="b7add-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7add-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7add-179">Header</span><span class="sxs-lookup"><span data-stu-id="b7add-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7add-180"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7add-180"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7add-181">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b7add-181">Type library</span></span><br/>             | <dl> <span data-ttu-id="b7add-182"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b7add-182"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b7add-183">DLL</span><span class="sxs-lookup"><span data-stu-id="b7add-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7add-184"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7add-184"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b7add-185">CLSID</span><span class="sxs-lookup"><span data-stu-id="b7add-185">CLSID</span></span><br/>                    | <span data-ttu-id="b7add-186">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="b7add-186">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="b7add-187">IID</span><span class="sxs-lookup"><span data-stu-id="b7add-187">IID</span></span><br/>                      | <span data-ttu-id="b7add-188">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="b7add-188">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="b7add-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7add-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7add-190">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="b7add-190">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="b7add-191">**Austauschen von "errbemubjectset"**</span><span class="sxs-lookup"><span data-stu-id="b7add-191">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

