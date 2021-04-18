---
description: Das OnProgress-Ereignis von "slibemsink" wird ausgelöst, wenn ein asynchroner-Befehl den Status eines aktuell ausgeführten-Aufrufes zurückgibt.
ms.assetid: abb43916-f952-41fe-a5ba-0428864c0685
ms.tgt_platform: multiple
title: 'Iswbemsinkevents:: OnProgress-Ereignis (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnProgress
- ISWbemSinkEvents.OnProgress
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d322309adcfad33b1c303d7efd6af28db1cac80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351117"
---
# <a name="iswbemsinkeventsonprogress-event"></a><span data-ttu-id="b7546-103">Iswbemsinkevents:: OnProgress-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b7546-103">ISWbemSinkEvents::OnProgress event</span></span>

<span data-ttu-id="b7546-104">Das **OnProgress** -Ereignis von " [**slibemsink**](swbemsink.md) " wird ausgelöst, wenn ein asynchroner-Befehl den Status eines aktuell ausgeführten-Aufrufes zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b7546-104">The **OnProgress** event of [**SWbemSink**](swbemsink.md) is triggered when an asynchronous call returns the status of a call that is in progress.</span></span> <span data-ttu-id="b7546-105">Wenn die Ereignisse, Instanzen oder Klassen von einem Anbieter erzeugt werden, der Statusaktualisierungen unterstützt, können Sie Code in diesem Ereignis platzieren, um Benutzern Feedback zum Status eines asynchronen Vorgangs zu geben.</span><span class="sxs-lookup"><span data-stu-id="b7546-105">If the events, instances, or classes are produced from a provider that supports status updates, you can place code in this event to provide users with feedback about the status of an asynchronous operation.</span></span> <span data-ttu-id="b7546-106">Wenn Sie Statusaktualisierungen empfangen möchten, müssen Sie den *IFlags* -Parameter des asynchronen Aufrufes **wbemflagsendstatus** (128/0x80) festlegen. andernfalls wird dieses Ereignis nicht ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b7546-106">You must set the *iFlags* parameter of the asynchronous call to **wbemFlagSendStatus** (128/0x80) if you want to receive status updates, otherwise this event is not triggered.</span></span>

<span data-ttu-id="b7546-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b7546-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7546-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7546-108">Syntax</span></span>


```VB
SWbemSink.OnProgress( _
  ByVal iUpperBound, _
  ByVal iCurrent, _
  ByVal strMessage, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="b7546-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7546-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7546-110">*iupperbound*</span><span class="sxs-lookup"><span data-stu-id="b7546-110">*iUpperBound*</span></span> 
</dt> <dd>

<span data-ttu-id="b7546-111">Ganze Zahl, die die Gesamtzahl der zu erledigenden Aufgaben beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b7546-111">Integer that describes the total number of tasks to complete.</span></span>

</dd> <dt>

<span data-ttu-id="b7546-112">*icurrent*</span><span class="sxs-lookup"><span data-stu-id="b7546-112">*iCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="b7546-113">Aktuelles Element, das gerade verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b7546-113">Current item that is being processed.</span></span>

</dd> <dt>

<span data-ttu-id="b7546-114">*strMessage*</span><span class="sxs-lookup"><span data-stu-id="b7546-114">*strMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="b7546-115">Meldung, in der der Status der aktuellen Aufgabe beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b7546-115">Message that describes the status of the current task.</span></span>

</dd> <dt>

<span data-ttu-id="b7546-116">*objwbemasynccontext*</span><span class="sxs-lookup"><span data-stu-id="b7546-116">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="b7546-117">Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das an den ursprünglichen asynchronen-Befehl übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b7546-117">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="b7546-118">Verwenden Sie diesen Parameter, um den Ursprung des asynchronen Aufrufs zu identifizieren, der dieses Ereignis auslöst, wenn mehrere asynchrone Aufrufe mithilfe dieser Objekt Senke durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b7546-118">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7546-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7546-119">Return value</span></span>

<span data-ttu-id="b7546-120">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b7546-120">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b7546-121">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b7546-121">Error codes</span></span>

<span data-ttu-id="b7546-122">Nach Abschluss des **OnProgress** -Ereignisses kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der folgenden Fehlercodes enthalten.</span><span class="sxs-lookup"><span data-stu-id="b7546-122">After the completion of the **OnProgress** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="b7546-123">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b7546-123">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b7546-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="b7546-124">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b7546-125">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b7546-125">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b7546-126">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b7546-126">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b7546-127">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="b7546-127">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="b7546-128">Netzwerkfehler. der normale Betrieb wird verhindert.</span><span class="sxs-lookup"><span data-stu-id="b7546-128">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7546-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7546-129">Remarks</span></span>

<span data-ttu-id="b7546-130">Das **OnProgress** -Ereignis wird ausgelöst, wenn ein asynchroner-Rückruf den Status eines aktuell ausgeführten Aufrufs zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b7546-130">The **OnProgress** event is triggered when an asynchronous call returns the status of a call that is in progress.</span></span> <span data-ttu-id="b7546-131">Wenn die Ereignisse, Instanzen oder Klassen von einem Anbieter erzeugt werden, der Statusaktualisierungen unterstützt, können Sie Code in diesem Ereignis platzieren, um Benutzern Feedback zum Status eines asynchronen Vorgangs zu geben.</span><span class="sxs-lookup"><span data-stu-id="b7546-131">If the events, instances, or classes are produced from a provider that supports status updates, you can place code in this event to give users feedback about the status of an asynchronous operation.</span></span>

> [!Note]  
> <span data-ttu-id="b7546-132">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="b7546-132">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="b7546-133">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="b7546-133">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="b7546-134">Um die Risiken auszuschließen, verwenden Sie die semisynchrone oder synchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="b7546-134">To eliminate the risks, use semi-synchronous or synchronous communication.</span></span> <span data-ttu-id="b7546-135">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b7546-135">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b7546-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7546-136">Requirements</span></span>



| <span data-ttu-id="b7546-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7546-137">Requirement</span></span> | <span data-ttu-id="b7546-138">Wert</span><span class="sxs-lookup"><span data-stu-id="b7546-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7546-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7546-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b7546-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7546-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7546-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7546-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b7546-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7546-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7546-143">Header</span><span class="sxs-lookup"><span data-stu-id="b7546-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7546-144"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7546-144"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7546-145">IDL</span><span class="sxs-lookup"><span data-stu-id="b7546-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7546-146"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7546-146"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b7546-147">DLL</span><span class="sxs-lookup"><span data-stu-id="b7546-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7546-148"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7546-148"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b7546-149">CLSID</span><span class="sxs-lookup"><span data-stu-id="b7546-149">CLSID</span></span><br/>                    | <span data-ttu-id="b7546-150">CLSID- \_ Swap-senbemsink</span><span class="sxs-lookup"><span data-stu-id="b7546-150">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="b7546-151">IID</span><span class="sxs-lookup"><span data-stu-id="b7546-151">IID</span></span><br/>                      | <span data-ttu-id="b7546-152">IID \_ iswbemsinkevents</span><span class="sxs-lookup"><span data-stu-id="b7546-152">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="b7546-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7546-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7546-154">**Swap-Senke**</span><span class="sxs-lookup"><span data-stu-id="b7546-154">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

