---
description: 'SWbemServices.ExecMethodAsync-Methode: Führt eine Methode aus, die von einem Methodenanbieter exportiert wird.'
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: SWbemServices.ExecMethodAsync-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fcdcd70b567a737cb8686ac841dc1ce0b55d3996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105588"
---
# <a name="swbemservicesexecmethodasync-method"></a><span data-ttu-id="a3522-103">SWbemServices.ExecMethodAsync-Methode</span><span class="sxs-lookup"><span data-stu-id="a3522-103">SWbemServices.ExecMethodAsync method</span></span>

<span data-ttu-id="a3522-104">Die **ExecMethodAsync-Methode** des [**SWbemServices-Objekts**](swbemservices.md) führt eine Methode aus, die von einem Methodenanbieter exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="a3522-104">The **ExecMethodAsync** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="a3522-105">Der Aufruf wird sofort an den Client zurückgegeben, während die eingehenden Parameter an den entsprechenden Anbieter weitergeleitet werden, an dem die Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3522-105">The call immediately returns to the client while the inbound parameters are forwarded to the appropriate provider where the method executes.</span></span> <span data-ttu-id="a3522-106">Informationen und Status werden an den Aufrufer durch Ereignisse zurückgegeben, die an die in *objWbemSink* angegebene Senke übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="a3522-106">Information and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="a3522-107">Der Anbieter implementiert anstelle Windows-Verwaltungsinstrumentation (WMI) die -Methode.</span><span class="sxs-lookup"><span data-stu-id="a3522-107">The provider, rather than Windows Management Instrumentation (WMI), implements the method.</span></span>

<span data-ttu-id="a3522-108">Die -Methode wird im asynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a3522-108">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="a3522-109">Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)</span><span class="sxs-lookup"><span data-stu-id="a3522-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="a3522-110">Weitere Informationen und eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)</span><span class="sxs-lookup"><span data-stu-id="a3522-110">For more information and an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3522-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3522-111">Syntax</span></span>


```VB
SWbemServices.ExecMethodAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a3522-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3522-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3522-113">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="a3522-113">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="a3522-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a3522-114">Required.</span></span> <span data-ttu-id="a3522-115">Erstellen Sie [**ein SWbemSink-Objekt,**](swbemsink.md) um die Objekte zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="a3522-115">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span> <span data-ttu-id="a3522-116">Objektsenke, die das Ergebnis des Methodenaufrufs empfängt.</span><span class="sxs-lookup"><span data-stu-id="a3522-116">Object sink that receives the result of the method call.</span></span> <span data-ttu-id="a3522-117">Die ausgehenden Parameter werden an das [**SWbemSink.OnObjectReady-Ereignis**](swbemsink-onobjectready.md) der angegebenen Objektsenke gesendet.</span><span class="sxs-lookup"><span data-stu-id="a3522-117">The outbound parameters are sent to the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event of the supplied object sink.</span></span> <span data-ttu-id="a3522-118">Die Ergebnisse des Aufrufmechanismus werden an das [**SWbemSink.OnCompleted-Ereignis**](swbemsink-oncompleted.md) der angegebenen Objektsenke gesendet.</span><span class="sxs-lookup"><span data-stu-id="a3522-118">The results of the call mechanism are sent to the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the supplied object sink.</span></span> <span data-ttu-id="a3522-119">Beachten Sie, **dass SWbemSink.OnCompleted** nicht den Rückgabecode der WMI-Methode erhält.</span><span class="sxs-lookup"><span data-stu-id="a3522-119">Be aware that **SWbemSink.OnCompleted** does not receive the return code of the WMI method.</span></span> <span data-ttu-id="a3522-120">Er empfängt jedoch den Rückgabecode des tatsächlichen Aufruf/Rückgabe-Mechanismus und ist nur nützlich, um zu überprüfen, ob der Aufruf aufgetreten ist oder dass er aus reinen Gründen fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="a3522-120">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons.</span></span> <span data-ttu-id="a3522-121">Der von der WMI-Methode zurückgegebene Ergebniscode wird im ausgehenden Parameterobjekt zurückgegeben, das für **SWbemSink.OnObjectReady bereitgestellt wird.**</span><span class="sxs-lookup"><span data-stu-id="a3522-121">The result code that is returned from the WMI method is returned in the outbound parameter object supplied to **SWbemSink.OnObjectReady**.</span></span> <span data-ttu-id="a3522-122">Wenn ein Fehlercode zurückgegeben wird, wird das angegebene [**IWbemObjectSink-Objekt**](iwbemobjectsink.md) nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3522-122">If any error code is returned, then the supplied [**IWbemObjectSink**](iwbemobjectsink.md) object is not used.</span></span> <span data-ttu-id="a3522-123">Wenn der Aufruf erfolgreich ist, wird die **IWbemObjectSink-Implementierung** des Benutzers aufgerufen, um das Ergebnis des Vorgangs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a3522-123">If the call is successful, then the user's **IWbemObjectSink** implementation is called to indicate the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a3522-124">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="a3522-124">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="a3522-125">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a3522-125">Required.</span></span> <span data-ttu-id="a3522-126">Eine Zeichenfolge, die den Objektpfad des Objekts enthält, für das die Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3522-126">A string that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="a3522-127">Weitere Informationen finden Sie unter [Beschreiben des Speicherorts eines WMI-Objekts.](describing-the-location-of-a-wmi-object.md)</span><span class="sxs-lookup"><span data-stu-id="a3522-127">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3522-128">*strMethodName*</span><span class="sxs-lookup"><span data-stu-id="a3522-128">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="a3522-129">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a3522-129">Required.</span></span> <span data-ttu-id="a3522-130">Der Name der zu auszuführenden Methode.</span><span class="sxs-lookup"><span data-stu-id="a3522-130">The name of the method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="a3522-131">*objWbemInParams* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="a3522-131">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a3522-132">Ein [**SWbemObject-Objekt,**](swbemobject.md) das die Eingabeparameter für die ausgeführte Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="a3522-132">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method that is executed.</span></span> <span data-ttu-id="a3522-133">Standardmäßig ist dieser Parameter nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a3522-133">By default, this parameter is undefined.</span></span> <span data-ttu-id="a3522-134">Weitere Informationen finden Sie unter [Constructing InParameters Objects (Erstellen von InParameters-Objekten) und Parsing OutParameters Objects (Analyse von OutParameters-Objekten).](constructing-inparameters-objects-and-parsing-outparameters-objects.md)</span><span class="sxs-lookup"><span data-stu-id="a3522-134">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3522-135">*iFlags* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="a3522-135">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a3522-136">Eine ganze Zahl, die das Verhalten des Aufrufs bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a3522-136">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="a3522-137">Dieser Parameter kann die folgenden Werte akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="a3522-137">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="a3522-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus\*\* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="a3522-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="a3522-139">Bewirkt, dass asynchrone Aufrufe Statusupdates an den [**OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.</span><span class="sxs-lookup"><span data-stu-id="a3522-139">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="a3522-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus\*\* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="a3522-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="a3522-141">Verhindert, dass asynchrone Aufrufe Statusupdates an den [**OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.</span><span class="sxs-lookup"><span data-stu-id="a3522-141">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a3522-142">*objWbemNamedValueSet* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="a3522-142">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a3522-143">In der Regel ist dies nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a3522-143">Typically, this is undefined.</span></span> <span data-ttu-id="a3522-144">Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung bedient.</span><span class="sxs-lookup"><span data-stu-id="a3522-144">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="a3522-145">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="a3522-145">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="a3522-146">*objWbemAsyncContext* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="a3522-146">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a3522-147">Ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das zur Objektsenke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufs zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a3522-147">A [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="a3522-148">Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mit derselben Objektsenke vornehmen.</span><span class="sxs-lookup"><span data-stu-id="a3522-148">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="a3522-149">Um diesen Parameter zu verwenden, erstellen Sie ein **SWbemNamedValueSet-Objekt,** und verwenden Sie die [**SWbemNamedValueSet.Add-Methode,**](swbemnamedvalueset-add.md) um einen Wert hinzuzufügen, der den asynchronen Aufruf identifiziert, den Sie vornehmen.</span><span class="sxs-lookup"><span data-stu-id="a3522-149">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="a3522-150">Dieses **SWbemNamedValueSet-Objekt** wird an die Objektsenke zurückgegeben, und die Quelle des Aufrufs kann mithilfe der [**SWbemNamedValueSet.Item-Methode**](swbemnamedvalueset-item.md) extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="a3522-150">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="a3522-151">Weitere Informationen finden Sie unter [Erstellen eines asynchronen Aufrufs mit VBScript.](making-an-asynchronous-call-with-vbscript.md)</span><span class="sxs-lookup"><span data-stu-id="a3522-151">For more information, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3522-152">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3522-152">Return value</span></span>

<span data-ttu-id="a3522-153">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a3522-153">This method does not return a value.</span></span> <span data-ttu-id="a3522-154">Wenn der Aufruf erfolgreich ist, wird ein [**OutParameters-Objekt,**](swbemmethod-outparameters.md) das auch ein [**SWbemObject**](swbemobject.md) ist, an die Senke bereitgestellt, die in *objWbemSink* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a3522-154">If the call is successful, an [**OutParameters**](swbemmethod-outparameters.md) object, which is also an [**SWbemObject**](swbemobject.md) is supplied to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="a3522-155">Das **zurückgegebene OutParameters-Objekt** enthält die Ausgabeparameter und den Rückgabewert für die ausgeführte Methode.</span><span class="sxs-lookup"><span data-stu-id="a3522-155">The returned **OutParameters** object contains the output parameters and return value for the method being executed.</span></span> <span data-ttu-id="a3522-156">Weitere Informationen finden Sie unter [Erstellen von InParameters-Objekten und Analysieren von OutParameters-Objekten.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)</span><span class="sxs-lookup"><span data-stu-id="a3522-156">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="a3522-157">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a3522-157">Error codes</span></span>

<span data-ttu-id="a3522-158">Nach Abschluss der **ExecMethodAsync-Methode** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der in der folgenden Liste aufgeführten Fehlercodes enthalten.</span><span class="sxs-lookup"><span data-stu-id="a3522-158">After the completion of the **ExecMethodAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes listed in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a3522-159">**wbemErrFailed** – 2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a3522-159">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a3522-160">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="a3522-160">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="a3522-161">**wbemErrInvalidClass** – 2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="a3522-161">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="a3522-162">Die angegebene Klasse war ungültig.</span><span class="sxs-lookup"><span data-stu-id="a3522-162">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a3522-163">**wbemErrInvalidParameter** – 2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="a3522-163">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="a3522-164">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a3522-164">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a3522-165">**wbemErrOutOfMemory** – 2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="a3522-165">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="a3522-166">Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a3522-166">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a3522-167">**wbemErrInvalidMethod** – 2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="a3522-167">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="a3522-168">Die angeforderte Methode war nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a3522-168">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="a3522-169">**wbemErrAccessDenied** – 2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="a3522-169">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="a3522-170">Der aktuelle Benutzer war nicht berechtigt, die -Methode auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a3522-170">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3522-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3522-171">Remarks</span></span>

<span data-ttu-id="a3522-172">Wenn die ausgeführte Methode Eingabeparameter enthält, muss das [**InParameters-Objekt**](swbemmethod-inparameters.md) im *objWbemInParam-Parameter* mit der Beschreibung in den Themen [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md) (Erstellen von InParameters-Objekten und Analyse von OutParameters-Objekten) identisch sein.</span><span class="sxs-lookup"><span data-stu-id="a3522-172">If the method executed has input parameters, the [**InParameters**](swbemmethod-inparameters.md) object in the *objWbemInParam* parameter must be the same as the description in the [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md) topics.</span></span>

<span data-ttu-id="a3522-173">Verwenden **SWbemServices.ExecMethodAsync** als Alternative zum direkten Zugriff [](gloss-p.md) zum Ausführen einer Anbietermethode, wenn es nicht möglich ist, eine Methode direkt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a3522-173">Use **SWbemServices.ExecMethodAsync** as an alternative to direct access for executing a [*provider method*](gloss-p.md) when it is not possible to execute a method directly.</span></span> <span data-ttu-id="a3522-174">Verwenden Sie sie z. B. mit einer Skriptsprache, die keine Ausgabeparameter unterstützt, das heißt, wenn Ihre Methode OUT-Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="a3522-174">For example, use it with a scripting language that does not support output parameters, that is, if your method has OUT parameters.</span></span> <span data-ttu-id="a3522-175">Andernfalls wird empfohlen, den direkten Zugriff zum Aufrufen einer Methode zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a3522-175">Otherwise, it is recommended that you use direct access to invoke a method.</span></span> <span data-ttu-id="a3522-176">Weitere Informationen finden Sie unter [Bearbeiten von Klassen- und Instanzinformationen.](manipulating-class-and-instance-information.md)</span><span class="sxs-lookup"><span data-stu-id="a3522-176">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="a3522-177">Die **SWbemServices.ExecMethodAsync-Methode** erfordert einen Objektpfad.</span><span class="sxs-lookup"><span data-stu-id="a3522-177">The **SWbemServices.ExecMethodAsync** method requires an object path.</span></span> <span data-ttu-id="a3522-178">Wenn das Skript bereits ein [**SWbemObject-Objekt**](swbemobject.md) enthält, können SieSWbemObject.Exe [**cMethodAsync aufrufen.**](swbemobject-execmethodasync-.md)</span><span class="sxs-lookup"><span data-stu-id="a3522-178">If the script already contains an [**SWbemObject**](swbemobject.md) object, you can call [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>

<span data-ttu-id="a3522-179">Dieser Aufruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a3522-179">This call returns immediately.</span></span> <span data-ttu-id="a3522-180">Die Statusinformationen werden über Rückrufe an die Senke zurückgegeben, die in *objWbemSink angegeben ist.*</span><span class="sxs-lookup"><span data-stu-id="a3522-180">The status information is returned to the caller through call-backs delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="a3522-181">Um die Verarbeitung nach Abschluss des Aufrufs fortzufahren, implementieren Sie eine Unterroutine für *objWbemSink*. [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)</span><span class="sxs-lookup"><span data-stu-id="a3522-181">To continue processing when the call is completed, implement a subroutine for the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="a3522-182">Ein asynchroner Rückruf ermöglicht es einem nicht authentifizierten Benutzer, Daten für die Senke zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="a3522-182">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="a3522-183">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="a3522-183">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="a3522-184">Weitere Informationen zum Beseitigen der Risiken finden Sie unter [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="a3522-184">For more information about how to eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="a3522-185">Verwenden Sie *den parameter objWbemAsyncContext,* um die Quelle eines Aufrufs zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a3522-185">Use the *objWbemAsyncContext* parameter to verify the source of a call.</span></span>

## <a name="examples"></a><span data-ttu-id="a3522-186">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3522-186">Examples</span></span>

<span data-ttu-id="a3522-187">Das folgende Codebeispiel zeigt die **ExecMethodAsync-Methode.**</span><span class="sxs-lookup"><span data-stu-id="a3522-187">The following code example shows the **ExecMethodAsync** method.</span></span> <span data-ttu-id="a3522-188">Das Skript erstellt ein [**Win32 \_ Process-Objekt,**](/windows/desktop/CIMWin32Prov/win32-process) das einen Prozess darstellt, in dem Editor ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3522-188">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="a3522-189">Es zeigt die Einrichtung eines [**InParameters-Objekts**](swbemmethod-inparameters.md) und das Abrufen von Ergebnissen aus einem [**OutParameters-Objekt.**](swbemmethod-outparameters.md)</span><span class="sxs-lookup"><span data-stu-id="a3522-189">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="a3522-190">Ein Skript, das dieselben synchron ausgeführten Vorgänge zeigt, finden Sie unterSWbemServices.Exe [**cMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="a3522-190">For a script that shows the same operations performed synchronously, see [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span> <span data-ttu-id="a3522-191">Ein Beispiel für die Verwendung des direkten Zugriffs finden Sie unter [Create Method in Class Win32 \_ Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="a3522-191">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="a3522-192">Ein Beispiel für den gleichen Vorgang mit [**SWbemObject**](swbemobject.md)finden Sie unter [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="a3522-192">For an example of the same operation using [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>


```VB
' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &VBCR & "ReturnValue = " _
        & oOutParams.ReturnValue &VBCR & _
        "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
        & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a><span data-ttu-id="a3522-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3522-193">Requirements</span></span>



| <span data-ttu-id="a3522-194">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3522-194">Requirement</span></span> | <span data-ttu-id="a3522-195">Wert</span><span class="sxs-lookup"><span data-stu-id="a3522-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3522-196">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3522-196">Minimum supported client</span></span><br/> | <span data-ttu-id="a3522-197">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3522-197">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3522-198">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3522-198">Minimum supported server</span></span><br/> | <span data-ttu-id="a3522-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3522-199">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3522-200">Header</span><span class="sxs-lookup"><span data-stu-id="a3522-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3522-201"><dt>Wbemdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="a3522-201"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3522-202">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a3522-202">Type library</span></span><br/>             | <dl> <span data-ttu-id="a3522-203"><dt>Wbemdisp.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a3522-203"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a3522-204">DLL</span><span class="sxs-lookup"><span data-stu-id="a3522-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3522-205"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3522-205"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a3522-206">CLSID</span><span class="sxs-lookup"><span data-stu-id="a3522-206">CLSID</span></span><br/>                    | <span data-ttu-id="a3522-207">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="a3522-207">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="a3522-208">IID</span><span class="sxs-lookup"><span data-stu-id="a3522-208">IID</span></span><br/>                      | <span data-ttu-id="a3522-209">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="a3522-209">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="a3522-210">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a3522-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3522-211">**Swbemservices**</span><span class="sxs-lookup"><span data-stu-id="a3522-211">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="a3522-212">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="a3522-212">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="a3522-213">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="a3522-213">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="a3522-214">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="a3522-214">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="a3522-215">Aufrufen einer Anbietermethode</span><span class="sxs-lookup"><span data-stu-id="a3522-215">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="a3522-216">Bearbeiten von Klassen- und Instanzinformationen</span><span class="sxs-lookup"><span data-stu-id="a3522-216">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

