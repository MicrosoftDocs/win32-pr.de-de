---
description: Ruft Instanzen einer angegebenen Klasse entsprechend den vom Benutzer angegebenen Kriterien ab.
ms.assetid: 631cd749-9a39-4606-9a38-0b4bb5b4b2cd
ms.tgt_platform: multiple
title: Swap Services. instancesofasync-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c518cb38a0ecb221f4fcb0d0e7f9ce6dfc226ba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863759"
---
# <a name="swbemservicesinstancesofasync-method"></a><span data-ttu-id="7366e-103">Methode "Swap Services. instancesofasync"</span><span class="sxs-lookup"><span data-stu-id="7366e-103">SWbemServices.InstancesOfAsync method</span></span>

<span data-ttu-id="7366e-104">Die **instancesofasync** -Methode des [**Swap Services**](swbemservices.md) -Objekts Ruft die Instanzen einer angegebenen Klasse entsprechend den vom Benutzer angegebenen Kriterien ab.</span><span class="sxs-lookup"><span data-stu-id="7366e-104">The **InstancesOfAsync** method of the [**SWbemServices**](swbemservices.md) object retrieves instances of a specified class according to user-specified criteria.</span></span>

<span data-ttu-id="7366e-105">Die-Methode wird im asynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7366e-105">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="7366e-106">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7366e-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="7366e-107">Die Syntax Erklärung finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7366e-107">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7366e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7366e-108">Syntax</span></span>


```VB
SWbemServices.InstancesOfAsync( _
  ByVal ObjWbemSink, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7366e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7366e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7366e-110">*Objwbemsink*</span><span class="sxs-lookup"><span data-stu-id="7366e-110">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="7366e-111">Objekt Senke, die die Instanzen asynchron empfängt.</span><span class="sxs-lookup"><span data-stu-id="7366e-111">Object sink that receives the instances asynchronously.</span></span> <span data-ttu-id="7366e-112">Erstellen Sie ein " [**Swap**](swbemsink.md) "-Objekt, um die Objekte zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="7366e-112">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="7366e-113">*Klasse*</span><span class="sxs-lookup"><span data-stu-id="7366e-113">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="7366e-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7366e-114">Required.</span></span> <span data-ttu-id="7366e-115">Eine Zeichenfolge, die den Namen der Klasse für die gewünschten Instanzen enthält.</span><span class="sxs-lookup"><span data-stu-id="7366e-115">String that contains the name of the class for the instances that you want.</span></span> <span data-ttu-id="7366e-116">Dieser Parameter darf nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="7366e-116">This parameter cannot be blank.</span></span>

</dd> <dt>

<span data-ttu-id="7366e-117">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="7366e-117">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7366e-118">Bestimmt die Tiefe der aufrufenumeration und gibt an, ob der Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7366e-118">Determines the depth of the call enumeration, and whether or not the call returns immediately.</span></span> <span data-ttu-id="7366e-119">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="7366e-119">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="7366e-120"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemqueryflagflache \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="7366e-120"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="7366e-121">Erzwingt, dass die Enumeration nur unmittelbare Unterklassen der angegebenen übergeordneten Klasse einschließt.</span><span class="sxs-lookup"><span data-stu-id="7366e-121">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="7366e-122"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemqueryflagdeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="7366e-122"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="7366e-123">Der Standardwert für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="7366e-123">Default for this parameter.</span></span> <span data-ttu-id="7366e-124">Dieser Wert erzwingt, dass die Enumeration alle Klassen in der Hierarchie einschließt.</span><span class="sxs-lookup"><span data-stu-id="7366e-124">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="7366e-125"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="7366e-125"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="7366e-126">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="7366e-126">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="7366e-127"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="7366e-127"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="7366e-128">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="7366e-128">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="7366e-129"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="7366e-129"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="7366e-130">Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7366e-130">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="7366e-131">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="7366e-131">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7366e-132">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="7366e-132">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7366e-133">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="7366e-133">Typically, this is undefined.</span></span> <span data-ttu-id="7366e-134">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="7366e-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="7366e-135">Ein Anbieter, der Kontext Informations Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="7366e-135">A provider that supports or requires context information information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="7366e-136">*objwbemasynccontext* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="7366e-136">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7366e-137">Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das zur Objekt Senke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufes aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7366e-137">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="7366e-138">Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen.</span><span class="sxs-lookup"><span data-stu-id="7366e-138">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="7366e-139">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7366e-139">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="7366e-140">Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="7366e-140">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7366e-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7366e-141">Return value</span></span>

<span data-ttu-id="7366e-142">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7366e-142">This method does not return a value.</span></span> <span data-ttu-id="7366e-143">Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="7366e-143">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="7366e-144">Nach der letzten Instanz empfängt die Objekt Senke ein [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7366e-144">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7366e-145">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7366e-145">Error codes</span></span>

<span data-ttu-id="7366e-146">Nach Abschluss der **instancesofasync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="7366e-146">Upon the completion of the **InstancesOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="7366e-147">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="7366e-147">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="7366e-148">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen von Instanzen der angegebenen Klasse.</span><span class="sxs-lookup"><span data-stu-id="7366e-148">Current user does not have the permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="7366e-149">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7366e-149">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7366e-150">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="7366e-150">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="7366e-151">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="7366e-151">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="7366e-152">Die angegebene Klasse ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7366e-152">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7366e-153">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="7366e-153">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="7366e-154">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7366e-154">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7366e-155">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="7366e-155">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="7366e-156">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7366e-156">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7366e-157">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7366e-157">Remarks</span></span>

<span data-ttu-id="7366e-158">Dieser Rückruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7366e-158">This call returns immediately.</span></span> <span data-ttu-id="7366e-159">Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, wenn Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7366e-159">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="7366e-160">Um jedes Objekt zu verarbeiten, wenn es zurückgegeben wird, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="7366e-160">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="7366e-161">Nachdem alle Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in ihrer Implementierung von *objwbemsink* ausführen. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7366e-161">After all the objects are returned, you can perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="7366e-162">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="7366e-162">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="7366e-163">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="7366e-163">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="7366e-164">Informationen zur Vermeidung der Risiken finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="7366e-164">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md)</span></span>

<span data-ttu-id="7366e-165">Die **instancesofasync** -Methode funktioniert nur für Klassen Objekte.</span><span class="sxs-lookup"><span data-stu-id="7366e-165">The **InstancesOfAsync** method only works for class objects.</span></span> <span data-ttu-id="7366e-166">Es ist kein Fehler, wenn der zurückgegebene Enumerator NULL (0) Elemente aufweist.</span><span class="sxs-lookup"><span data-stu-id="7366e-166">It is not an error for the returned enumerator to have zero (0) elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="7366e-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7366e-167">Requirements</span></span>



| <span data-ttu-id="7366e-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7366e-168">Requirement</span></span> | <span data-ttu-id="7366e-169">Wert</span><span class="sxs-lookup"><span data-stu-id="7366e-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7366e-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7366e-170">Minimum supported client</span></span><br/> | <span data-ttu-id="7366e-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7366e-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7366e-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7366e-172">Minimum supported server</span></span><br/> | <span data-ttu-id="7366e-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7366e-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7366e-174">Header</span><span class="sxs-lookup"><span data-stu-id="7366e-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="7366e-175"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7366e-175"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7366e-176">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7366e-176">Type library</span></span><br/>             | <dl> <span data-ttu-id="7366e-177"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7366e-177"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7366e-178">DLL</span><span class="sxs-lookup"><span data-stu-id="7366e-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7366e-179"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7366e-179"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7366e-180">CLSID</span><span class="sxs-lookup"><span data-stu-id="7366e-180">CLSID</span></span><br/>                    | <span data-ttu-id="7366e-181">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="7366e-181">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="7366e-182">IID</span><span class="sxs-lookup"><span data-stu-id="7366e-182">IID</span></span><br/>                      | <span data-ttu-id="7366e-183">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="7366e-183">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="7366e-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7366e-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7366e-185">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="7366e-185">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="7366e-186">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="7366e-186">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

