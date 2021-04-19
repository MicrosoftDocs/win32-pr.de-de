---
description: Die deleteasync- \_ Methode von "errbemubject" löscht asynchron entweder die aktuelle Klasse oder die aktuelle Instanz.
ms.assetid: b8d67fa5-5217-422b-acbe-5eea6028deeb
ms.tgt_platform: multiple
title: SWbemObject.DeleteAsync_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7951b84a2b5d9f06061f4cefb04c797ccfea3ecd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355609"
---
# <a name="swbemobjectdeleteasync_-method"></a><span data-ttu-id="2a11d-103">Errbemubject. deleteasync- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="2a11d-103">SWbemObject.DeleteAsync\_ method</span></span>

<span data-ttu-id="2a11d-104">Die **deleteasync \_** -Methode von " [**errbemubject**](swbemobject.md) " löscht asynchron entweder die aktuelle Klasse oder die aktuelle Instanz.</span><span class="sxs-lookup"><span data-stu-id="2a11d-104">The **DeleteAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously deletes either the current class or the current instance.</span></span> <span data-ttu-id="2a11d-105">Wenn ein dynamischer Anbieter die Klasse oder Instanz bereitstellt, ist es manchmal nicht möglich, dieses Objekt zu löschen, es sei denn, der Anbieter unterstützt das Löschen von Klassen oder Instanzen.</span><span class="sxs-lookup"><span data-stu-id="2a11d-105">If a dynamic provider supplies the class or instance, sometimes it is not possible to delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="2a11d-106">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2a11d-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2a11d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a11d-107">Syntax</span></span>


```VB
SWbemObject.DeleteAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2a11d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a11d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a11d-109">*objwbemsink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a11d-109">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a11d-110">Objekt Senke, die das Ergebnis des Löschvorgangs zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2a11d-110">Object sink that returns the outcome of the delete operation.</span></span>

</dd> <dt>

<span data-ttu-id="2a11d-111">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2a11d-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a11d-112">Eine ganze Zahl, die das Verhalten des Aufrufes bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2a11d-112">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="2a11d-113">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="2a11d-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="2a11d-114"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="2a11d-114"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="2a11d-115">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den " [**slibemsink. OnProgress**](swbemsink-onprogress.md) "-Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="2a11d-115">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="2a11d-116"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="2a11d-116"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* ( 0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2a11d-117">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="2a11d-117">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2a11d-118">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2a11d-118">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a11d-119">Dieser Parameter ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="2a11d-119">This parameter is typically undefined.</span></span> <span data-ttu-id="2a11d-120">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="2a11d-120">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="2a11d-121">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="2a11d-121">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="2a11d-122">*objwbemasynccontext* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2a11d-122">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a11d-123">Dabei handelt es sich um ein Objekt vom Typ " [**taubemnamedvalueset**](swbemnamedvalueset.md) ", das zur Objekt Senke zurückkehrt, um die Quelle für den ursprünglichen asynchronen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2a11d-123">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="2a11d-124">Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen.</span><span class="sxs-lookup"><span data-stu-id="2a11d-124">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="2a11d-125">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2a11d-125">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="2a11d-126">Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="2a11d-126">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="2a11d-127">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="2a11d-127">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a11d-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a11d-128">Return value</span></span>

<span data-ttu-id="2a11d-129">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2a11d-129">This method does not return a value.</span></span> <span data-ttu-id="2a11d-130">Wenn dieser Vorgang erfolgreich ist, wird das Ergebnis des Löschvorgangs durch die angegebene Objekt Senke bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2a11d-130">If this call is successful, the result of the delete operation is provided through the supplied object sink.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2a11d-131">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2a11d-131">Error codes</span></span>

<span data-ttu-id="2a11d-132">Nach dem Abschluss der **deleteasync \_** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="2a11d-132">After the completion of the **DeleteAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="2a11d-133">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="2a11d-133">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="2a11d-134">Der aktuelle Kontext verfügt nicht über die erforderlichen Sicherheitsrechte, um das Objekt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="2a11d-134">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="2a11d-135">**wbemErrFailed** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="2a11d-135">**wbemErrFailed** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="2a11d-136">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="2a11d-136">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="2a11d-137">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="2a11d-137">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="2a11d-138">Die angegebene Klasse ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2a11d-138">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="2a11d-139">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="2a11d-139">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="2a11d-140">Das Objekt kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="2a11d-140">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="2a11d-141">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="2a11d-141">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="2a11d-142">Das Objekt ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2a11d-142">Object did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="2a11d-143">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="2a11d-143">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="2a11d-144">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="2a11d-144">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a11d-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a11d-145">Remarks</span></span>

<span data-ttu-id="2a11d-146">Dieser Rückruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2a11d-146">This call returns immediately.</span></span> <span data-ttu-id="2a11d-147">Der Status wird an den Aufrufer zurückgegeben, indem ein Rückruf an die Senke gesendet wird, die in *objwbemsink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2a11d-147">The status is returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span>

<span data-ttu-id="2a11d-148">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="2a11d-148">An asynchronous callback allows a nonauthenticated user to provide data to the sink.</span></span> <span data-ttu-id="2a11d-149">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="2a11d-149">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="2a11d-150">Um die Risiken auszuschließen, verwenden Sie entweder die semisynchrone Kommunikation oder die synchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="2a11d-150">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="2a11d-151">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="2a11d-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a11d-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a11d-152">Requirements</span></span>



| <span data-ttu-id="2a11d-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a11d-153">Requirement</span></span> | <span data-ttu-id="2a11d-154">Wert</span><span class="sxs-lookup"><span data-stu-id="2a11d-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a11d-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a11d-155">Minimum supported client</span></span><br/> | <span data-ttu-id="2a11d-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a11d-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2a11d-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a11d-157">Minimum supported server</span></span><br/> | <span data-ttu-id="2a11d-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a11d-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2a11d-159">Header</span><span class="sxs-lookup"><span data-stu-id="2a11d-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a11d-160"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a11d-160"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a11d-161">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2a11d-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="2a11d-162"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2a11d-162"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2a11d-163">DLL</span><span class="sxs-lookup"><span data-stu-id="2a11d-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a11d-164"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a11d-164"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2a11d-165">CLSID</span><span class="sxs-lookup"><span data-stu-id="2a11d-165">CLSID</span></span><br/>                    | <span data-ttu-id="2a11d-166">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="2a11d-166">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="2a11d-167">IID</span><span class="sxs-lookup"><span data-stu-id="2a11d-167">IID</span></span><br/>                      | <span data-ttu-id="2a11d-168">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="2a11d-168">IID\_ISWbemObject</span></span><br/>                                                            |



 

