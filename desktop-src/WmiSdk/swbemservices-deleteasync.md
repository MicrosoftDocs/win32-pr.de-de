---
description: Löscht die im Objekt Pfad angegebene Klasse oder Instanz.
ms.assetid: f5ed170e-d002-4dd9-b8b6-b764a7a41a27
ms.tgt_platform: multiple
title: Swap Services. deleteasync-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: adc8811c11f67b9fc92628740bd15df2086948d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348522"
---
# <a name="swbemservicesdeleteasync-method"></a><span data-ttu-id="72967-103">Swap Services. deleteasync-Methode</span><span class="sxs-lookup"><span data-stu-id="72967-103">SWbemServices.DeleteAsync method</span></span>

<span data-ttu-id="72967-104">Die **deleteasync** -Methode des [**Swap Services**](swbemservices.md) -Objekts löscht die im Objekt Pfad angegebene Klasse oder Instanz.</span><span class="sxs-lookup"><span data-stu-id="72967-104">The **DeleteAsync** method of the [**SWbemServices**](swbemservices.md) object deletes the class or instance specified in the object path.</span></span> <span data-ttu-id="72967-105">Der Aufruf von **deleteasync** wird sofort zurückgegeben, und die Ergebnisse und der Status werden an den Aufrufer über Ereignisse zurückgegeben, die an die in *objwbemsink* angegebene Senke gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="72967-105">The call to **DeleteAsync** returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="72967-106">Weitere Informationen zum Erstellen einer Senke finden Sie unter [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="72967-106">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span> <span data-ttu-id="72967-107">Sie können nur Objekte im Namespace löschen, mit dem Sie verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="72967-107">You can only delete objects in the namespace to which you are connected.</span></span>

<span data-ttu-id="72967-108">Wenn ein dynamischer Anbieter die Klasse oder Instanz bereitstellt, ist es manchmal nicht möglich, dieses Objekt zu löschen, es sei denn, der Anbieter unterstützt das Löschen von Klassen oder Instanzen.</span><span class="sxs-lookup"><span data-stu-id="72967-108">If a dynamic provider supplies the class or instance, sometimes it is not possible to delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="72967-109">Die-Methode wird im asynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="72967-109">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="72967-110">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="72967-110">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="72967-111">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="72967-111">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="72967-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="72967-112">Syntax</span></span>


```VB
SWbemServices.DeleteAsync( _
  [ ByVal ObjWbemSink ], _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="72967-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="72967-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72967-114">*Objwbemsink* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="72967-114">*ObjWbemSink* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="72967-115">Objekt Senke, die die Ergebnisse der Löschung empfängt.</span><span class="sxs-lookup"><span data-stu-id="72967-115">Object sink that receives the results of the deletion.</span></span> <span data-ttu-id="72967-116">Erstellen Sie ein " [**taubemsink**](swbemsink.md) "-Objekt zum Empfangen der Objekte.</span><span class="sxs-lookup"><span data-stu-id="72967-116">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="72967-117">*strobjectpath*</span><span class="sxs-lookup"><span data-stu-id="72967-117">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="72967-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="72967-118">Required.</span></span> <span data-ttu-id="72967-119">Eine Zeichenfolge, die den Objekt Pfad zu dem Objekt enthält, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="72967-119">String that contains the object path to the object that you want to delete.</span></span> <span data-ttu-id="72967-120">Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="72967-120">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="72967-121">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="72967-121">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="72967-122">Bestimmt, ob Statusaktualisierungen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="72967-122">Determines if status updates are returned.</span></span> <span data-ttu-id="72967-123">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="72967-123">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="72967-124"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="72967-124"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="72967-125">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="72967-125">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="72967-126"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="72967-126"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="72967-127">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="72967-127">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="72967-128">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="72967-128">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="72967-129">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="72967-129">Typically, this is undefined.</span></span> <span data-ttu-id="72967-130">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="72967-130">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="72967-131">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="72967-131">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="72967-132">*objwbemasynccontext* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="72967-132">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="72967-133">Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das zur Objekt Senke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufes aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="72967-133">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="72967-134">Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen.</span><span class="sxs-lookup"><span data-stu-id="72967-134">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="72967-135">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="72967-135">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="72967-136">Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="72967-136">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="72967-137">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="72967-137">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72967-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72967-138">Return value</span></span>

<span data-ttu-id="72967-139">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="72967-139">This method does not return a value.</span></span> <span data-ttu-id="72967-140">Wenn der-Vorgang erfolgreich ist, empfängt die Objekt Senke eine Benachrichtigung über den Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="72967-140">If the call is successful, the object sink receives notification of the deletion.</span></span>

## <a name="error-codes"></a><span data-ttu-id="72967-141">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="72967-141">Error codes</span></span>

<span data-ttu-id="72967-142">Nach dem Abschluss der **deleteasync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="72967-142">After the completion of the **DeleteAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="72967-143">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="72967-143">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="72967-144">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="72967-144">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="72967-145">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="72967-145">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="72967-146">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="72967-146">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="72967-147">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="72967-147">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="72967-148">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="72967-148">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="72967-149">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="72967-149">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="72967-150">Netzwerkfehler. der normale Betrieb wird verhindert.</span><span class="sxs-lookup"><span data-stu-id="72967-150">Networking error occurred, preventing normal operation.</span></span>

</dd> <dt>

<span data-ttu-id="72967-151">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="72967-151">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="72967-152">Der aktuelle oder der angegebene Benutzername und das Kennwort sind ungültig oder sind zum Herstellen der Verbindung autorisiert.</span><span class="sxs-lookup"><span data-stu-id="72967-152">Current or specified user name and password are not valid or authorized to make the connection.</span></span>

</dd> <dt>

<span data-ttu-id="72967-153">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="72967-153">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="72967-154">Das angeforderte Element wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="72967-154">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72967-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72967-155">Remarks</span></span>

<span data-ttu-id="72967-156">Dieser Rückruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="72967-156">This call returns immediately.</span></span> <span data-ttu-id="72967-157">Der Status des Löschvorgangs wird an den Aufrufer zurückgegeben, indem ein Rückruf an die Senke gesendet wird, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="72967-157">The status of the delete operation is returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="72967-158">Sie können die endgültige Verarbeitung in ihrer Implementierung von *objwbemsink* ausführen. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="72967-158">You can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="72967-159">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="72967-159">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="72967-160">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="72967-160">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="72967-161">Um die Risiken auszuschließen, finden Sie weitere Informationen unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="72967-161">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72967-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72967-162">Requirements</span></span>



| <span data-ttu-id="72967-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72967-163">Requirement</span></span> | <span data-ttu-id="72967-164">Wert</span><span class="sxs-lookup"><span data-stu-id="72967-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72967-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72967-165">Minimum supported client</span></span><br/> | <span data-ttu-id="72967-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72967-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="72967-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72967-167">Minimum supported server</span></span><br/> | <span data-ttu-id="72967-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72967-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72967-169">Header</span><span class="sxs-lookup"><span data-stu-id="72967-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="72967-170"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="72967-170"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="72967-171">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="72967-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="72967-172"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="72967-172"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="72967-173">DLL</span><span class="sxs-lookup"><span data-stu-id="72967-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72967-174"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72967-174"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="72967-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="72967-175">CLSID</span></span><br/>                    | <span data-ttu-id="72967-176">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="72967-176">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="72967-177">IID</span><span class="sxs-lookup"><span data-stu-id="72967-177">IID</span></span><br/>                      | <span data-ttu-id="72967-178">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="72967-178">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="72967-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72967-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72967-180">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="72967-180">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="72967-181">**Errbemubjectpath**</span><span class="sxs-lookup"><span data-stu-id="72967-181">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> </dl>

 

