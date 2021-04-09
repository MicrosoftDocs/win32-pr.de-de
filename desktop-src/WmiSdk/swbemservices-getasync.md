---
description: Ruft ein Objekt ab, das eine Klassendefinition oder eine-Instanz ist, basierend auf dem Objekt Pfad.
ms.assetid: 8da46851-52b8-4b5a-8c9d-1d492f57f4b6
ms.tgt_platform: multiple
title: Swap Services. getasync-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.GetAsync
- ISWbemServices.GetAsync
- ISWbemServices.GetAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 451f13bde9458e7d57ec393f42b92a4092c99924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863760"
---
# <a name="swbemservicesgetasync-method"></a><span data-ttu-id="a7fb4-103">Swap Services. getasync-Methode</span><span class="sxs-lookup"><span data-stu-id="a7fb4-103">SWbemServices.GetAsync method</span></span>

<span data-ttu-id="a7fb4-104">Die **getasync** -Methode des [**Swap Services**](swbemservices.md) -Objekts Ruft ein Objekt ab, das eine Klassendefinition oder eine-Instanz ist, die auf dem Objekt Pfad basiert.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-104">The **GetAsync** method of the [**SWbemServices**](swbemservices.md) object retrieves an object, that is a class definition or an instance, based on the object path.</span></span>

<span data-ttu-id="a7fb4-105">Diese Methode ruft nur Objekte aus dem Namespace ab, der dem aktuellen ' [**Swap Services**](swbemservices.md) '-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-105">This method retrieves only objects from the namespace that is associated with the current [**SWbemServices**](swbemservices.md) object.</span></span>

<span data-ttu-id="a7fb4-106">Diese Methode wird im asynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-106">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="a7fb4-107">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="a7fb4-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="a7fb4-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a7fb4-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7fb4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7fb4-109">Syntax</span></span>


```VB
SWbemServices.GetAsync( _
  ByVal objWbemSink, _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a7fb4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7fb4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7fb4-111">*objwbemsink*</span><span class="sxs-lookup"><span data-stu-id="a7fb4-111">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="a7fb4-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-112">Required.</span></span> <span data-ttu-id="a7fb4-113">Objekt Senke, die Objekte asynchron abruft.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-113">Object sink that gets objects asynchronously.</span></span> <span data-ttu-id="a7fb4-114">Erstellen Sie ein " [**Swap**](swbemsink.md) "-Objekt, um die Objekte zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-114">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="a7fb4-115">*strobjectpath* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="a7fb4-115">*strObjectPath* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fb4-116">Der Pfad des Objekts, das Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-116">Path of the object that you want to retrieve.</span></span> <span data-ttu-id="a7fb4-117">Wenn dieser Wert leer ist, kann das leere Objekt, das zurückgegeben wird, eine neue Klasse werden.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-117">If this value is empty, the empty object that is returned can become a new class.</span></span> <span data-ttu-id="a7fb4-118">Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="a7fb4-118">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7fb4-119">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="a7fb4-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fb4-120">Eine ganze Zahl, die das Verhalten des Aufrufes bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-120">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="a7fb4-121">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-121">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="a7fb4-122"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="a7fb4-122"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="a7fb4-123">Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-123">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="a7fb4-124"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="a7fb4-124"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="a7fb4-125">Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-125">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="a7fb4-126"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="a7fb4-126"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="a7fb4-127">Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-127">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="a7fb4-128">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="a7fb4-128">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a7fb4-129">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="a7fb4-129">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fb4-130">In der Regel ist dieser Wert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-130">Typically, this value is undefined.</span></span> <span data-ttu-id="a7fb4-131">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-131">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="a7fb4-132">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-132">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="a7fb4-133">*objwbemasynccontext* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="a7fb4-133">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fb4-134">Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das zur Objekt Senke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufes aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-134">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="a7fb4-135">Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-135">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="a7fb4-136">Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-136">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="a7fb4-137">Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-137">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="a7fb4-138">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="a7fb4-138">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7fb4-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7fb4-139">Return value</span></span>

<span data-ttu-id="a7fb4-140">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-140">This method does not return a value.</span></span> <span data-ttu-id="a7fb4-141">Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis, wenn das Objekt verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-141">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event when the object is available.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a7fb4-142">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a7fb4-142">Error codes</span></span>

<span data-ttu-id="a7fb4-143">Nach dem Abschluss der **getasync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-143">After the completion of the **GetAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a7fb4-144">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="a7fb4-144">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="a7fb4-145">Der aktuelle Benutzer verfügt nicht über die Berechtigung für den Zugriff auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-145">Current user does not have the permission to access the object.</span></span>

</dd> <dt>

<span data-ttu-id="a7fb4-146">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a7fb4-146">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a7fb4-147">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-147">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="a7fb4-148">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="a7fb4-148">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="a7fb4-149">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-149">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a7fb4-150">**wbemErrInvalidObjectPath** -2147749946 (0x8004103a)</span><span class="sxs-lookup"><span data-stu-id="a7fb4-150">**wbemErrInvalidObjectPath** - 2147749946 (0x8004103A)</span></span>
</dt> <dd>

<span data-ttu-id="a7fb4-151">Der angegebene Pfad war ungültig.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-151">Specified path was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a7fb4-152">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="a7fb4-152">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="a7fb4-153">Das angeforderte Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-153">Requested object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="a7fb4-154">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="a7fb4-154">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="a7fb4-155">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-155">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7fb4-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7fb4-156">Remarks</span></span>

<span data-ttu-id="a7fb4-157">Dieser Rückruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-157">This call returns immediately.</span></span> <span data-ttu-id="a7fb4-158">Das angeforderte Objekt und der Status werden mithilfe eines Rückrufs an den Aufrufer zurückgegeben, der an die in *objwbemsink* angegebene Senke gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-158">The requested object and status are returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="a7fb4-159">Um das Objekt zu verarbeiten, wenn es zurückgegeben wird, erstellen Sie eine *objwbemsink*. " [**Onobjectready**](swbemsink-onobjectready.md)" oder " *objwbemsink*". [**Onabgeschlossene**](swbemsink-oncompleted.md) Ereignis Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-159">To process the object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md), or an *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event subroutine.</span></span>

<span data-ttu-id="a7fb4-160">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-160">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="a7fb4-161">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-161">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="a7fb4-162">Um die Risiken auszuschließen, verwenden Sie die semisynchrone oder synchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-162">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="a7fb4-163">Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="a7fb4-163">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7fb4-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7fb4-164">Requirements</span></span>



| <span data-ttu-id="a7fb4-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7fb4-165">Requirement</span></span> | <span data-ttu-id="a7fb4-166">Wert</span><span class="sxs-lookup"><span data-stu-id="a7fb4-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7fb4-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7fb4-167">Minimum supported client</span></span><br/> | <span data-ttu-id="a7fb4-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7fb4-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7fb4-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7fb4-169">Minimum supported server</span></span><br/> | <span data-ttu-id="a7fb4-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7fb4-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7fb4-171">Header</span><span class="sxs-lookup"><span data-stu-id="a7fb4-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7fb4-172"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7fb4-172"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7fb4-173">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a7fb4-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="a7fb4-174"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a7fb4-174"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a7fb4-175">DLL</span><span class="sxs-lookup"><span data-stu-id="a7fb4-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7fb4-176"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7fb4-176"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a7fb4-177">CLSID</span><span class="sxs-lookup"><span data-stu-id="a7fb4-177">CLSID</span></span><br/>                    | <span data-ttu-id="a7fb4-178">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="a7fb4-178">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="a7fb4-179">IID</span><span class="sxs-lookup"><span data-stu-id="a7fb4-179">IID</span></span><br/>                      | <span data-ttu-id="a7fb4-180">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="a7fb4-180">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="a7fb4-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7fb4-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7fb4-182">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="a7fb4-182">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="a7fb4-183">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="a7fb4-183">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

