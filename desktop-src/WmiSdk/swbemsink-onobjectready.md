---
description: Das onobjectready-Ereignis eines slibemsink-Objekts wird ausgelöst, wenn ein asynchroner Vorgang ein Objekt zurückgibt.
ms.assetid: 14110ee7-a808-4786-b695-2ce54189d826
ms.tgt_platform: multiple
title: 'Iswbemsinkevents:: onobjectready-Ereignis (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectReady
- ISWbemSinkEvents.OnObjectReady
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1fa803339e7007a030881c3d5b47d67f354b5661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130961"
---
# <a name="iswbemsinkeventsonobjectready-event"></a><span data-ttu-id="b47ac-103">Iswbemsinkevents:: onobjectready-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b47ac-103">ISWbemSinkEvents::OnObjectReady event</span></span>

<span data-ttu-id="b47ac-104">Das **onobjectready** -Ereignis eines [**slibemsink**](swbemsink.md) -Objekts wird ausgelöst, wenn ein asynchroner Vorgang ein Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b47ac-104">The **OnObjectReady** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous operation returns an object.</span></span> <span data-ttu-id="b47ac-105">Verwenden Sie dieses Ereignis, um Objekte aus asynchronen Aufrufen wie z. [**b. "slibemubject \_ . instancesasync**](swbemobject-instancesasync-.md) " oder " [**SWbemServices.Execqueryasync**](swbemservices-execqueryasync.md)" zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="b47ac-105">Use this event to process objects from asynchronous calls such as [**SWbemObject.InstancesAsync\_**](swbemobject-instancesasync-.md) or [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md).</span></span> <span data-ttu-id="b47ac-106">**Onobjectready** gibt jedes Mal ein [**Austausch Objekt**](swbemobject.md) zurück, bis die Enumeration beendet ist.</span><span class="sxs-lookup"><span data-stu-id="b47ac-106">**OnObjectReady** returns one [**SWbemObject**](swbemobject.md) each time until the enumeration is complete.</span></span>

<span data-ttu-id="b47ac-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b47ac-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b47ac-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b47ac-108">Syntax</span></span>


```VB
SWbemSink.OnObjectReady( _
  ByVal objWbemObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="b47ac-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b47ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b47ac-110">*objwbemujekt*</span><span class="sxs-lookup"><span data-stu-id="b47ac-110">*objWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="b47ac-111">Ein-Objekt mit einem [**Swap**](swbemobject.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b47ac-111">An [**SWbemObject**](swbemobject.md) object.</span></span> <span data-ttu-id="b47ac-112">Dies ähnelt dem, was vom synchronen Äquivalent des asynchronen Aufrufes zurückgegeben wird, der dieses Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="b47ac-112">This is similar to what is returned by the synchronous equivalent of the asynchronous call that triggers this event.</span></span> <span data-ttu-id="b47ac-113">Beispielsweise gibt ein Aufrufen der Methode " [**errbemservices. getasync**](swbemservices-getasync.md) " ein " **errbewbject** " *im objwbefubject* -Parameter des " **onobjectready** "-Ereignisses des " [**slibemsink**](swbemsink.md) "-Objekts zurück, das als *objwbefubject* -Parameter des ursprünglichen Aufrufes-Objekts übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b47ac-113">For example, a call to the [**SWbemServices.GetAsync**](swbemservices-getasync.md) method returns an **SWbemObject** in the *objWbemObject* parameter of the **OnObjectReady** event of the [**SWbemSink**](swbemsink.md) object, which is passed as the *objWbemObject* parameter of the original call.</span></span> <span data-ttu-id="b47ac-114">Das gleiche " **errbejebject** "-Objekt kann mithilfe eines äquivalenten synchronen Aufrufes für " [**errbemservices. Get**](swbemservices-get.md)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b47ac-114">The same **SWbemObject** object can be obtained by using an equivalent synchronous call to [**SWbemServices.Get**](swbemservices-get.md).</span></span>

</dd> <dt>

<span data-ttu-id="b47ac-115">*objwbemasynccontext*</span><span class="sxs-lookup"><span data-stu-id="b47ac-115">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="b47ac-116">Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das an den ursprünglichen asynchronen-Befehl übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b47ac-116">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="b47ac-117">Verwenden Sie diesen Parameter, um den Ursprung des asynchronen Aufrufs zu identifizieren, der dieses Ereignis auslöst, wenn mehrere asynchrone Aufrufe mithilfe dieser Objekt Senke durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b47ac-117">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b47ac-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b47ac-118">Return value</span></span>

<span data-ttu-id="b47ac-119">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b47ac-119">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b47ac-120">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b47ac-120">Error codes</span></span>

<span data-ttu-id="b47ac-121">Nach Abschluss des **onobjectready** -Ereignisses kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der folgenden Fehlercodes enthalten.</span><span class="sxs-lookup"><span data-stu-id="b47ac-121">After the completion of the **OnObjectReady** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="b47ac-122">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b47ac-122">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b47ac-123">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="b47ac-123">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b47ac-124">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b47ac-124">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b47ac-125">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b47ac-125">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b47ac-126">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="b47ac-126">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="b47ac-127">Netzwerkfehler. der normale Betrieb wird verhindert.</span><span class="sxs-lookup"><span data-stu-id="b47ac-127">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b47ac-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b47ac-128">Remarks</span></span>

<span data-ttu-id="b47ac-129">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="b47ac-129">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="b47ac-130">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="b47ac-130">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="b47ac-131">Um die Risiken auszuschließen, verwenden Sie entweder semisynchrone Kommunikation oder synchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="b47ac-131">To eliminate the risks, use either semi-synchronous communication or synchronous communication.</span></span> <span data-ttu-id="b47ac-132">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b47ac-132">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b47ac-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b47ac-133">Requirements</span></span>



| <span data-ttu-id="b47ac-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b47ac-134">Requirement</span></span> | <span data-ttu-id="b47ac-135">Wert</span><span class="sxs-lookup"><span data-stu-id="b47ac-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b47ac-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b47ac-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b47ac-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b47ac-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b47ac-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b47ac-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b47ac-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b47ac-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b47ac-140">Header</span><span class="sxs-lookup"><span data-stu-id="b47ac-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b47ac-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b47ac-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b47ac-142">IDL</span><span class="sxs-lookup"><span data-stu-id="b47ac-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b47ac-143"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b47ac-143"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b47ac-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b47ac-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b47ac-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b47ac-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b47ac-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="b47ac-146">CLSID</span></span><br/>                    | <span data-ttu-id="b47ac-147">CLSID- \_ Swap-senbemsink</span><span class="sxs-lookup"><span data-stu-id="b47ac-147">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="b47ac-148">IID</span><span class="sxs-lookup"><span data-stu-id="b47ac-148">IID</span></span><br/>                      | <span data-ttu-id="b47ac-149">IID \_ iswbemsinkevents</span><span class="sxs-lookup"><span data-stu-id="b47ac-149">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="b47ac-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b47ac-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b47ac-151">**Swap-Senke**</span><span class="sxs-lookup"><span data-stu-id="b47ac-151">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

