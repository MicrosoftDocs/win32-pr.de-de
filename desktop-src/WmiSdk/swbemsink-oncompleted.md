---
description: Das OnComplete-Ereignis eines slibemsink-Objekts wird ausgelöst, wenn ein asynchroner-Befehl abgeschlossen ist. Dieses Ereignis gibt für die Client Anwendung das Ergebnis eines asynchronen Vorgangs an und stellt Fehlerinformationen bereit, wenn der asynchrone-Befehl fehlschlägt.
ms.assetid: 2723185d-5b8b-4cc7-ada3-51c3275272a9
ms.tgt_platform: multiple
title: 'Iswbemsinkevents:: onabgeschlossene-Ereignis (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnCompleted
- ISWbemSinkEvents.OnCompleted
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 16cb0362b5c1b1d432d72bb959103adbb7315069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130965"
---
# <a name="iswbemsinkeventsoncompleted-event"></a><span data-ttu-id="d636e-104">Iswbemsinkevents:: onabgeschlossene-Ereignis</span><span class="sxs-lookup"><span data-stu-id="d636e-104">ISWbemSinkEvents::OnCompleted event</span></span>

<span data-ttu-id="d636e-105">Das **OnComplete** -Ereignis eines [**slibemsink**](swbemsink.md) -Objekts wird ausgelöst, wenn ein asynchroner-Befehl abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d636e-105">The **OnCompleted** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous call is complete.</span></span> <span data-ttu-id="d636e-106">Dieses Ereignis gibt für die Client Anwendung das Ergebnis eines asynchronen Vorgangs an und stellt Fehlerinformationen bereit, wenn der asynchrone-Befehl fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="d636e-106">This event indicates to the client application, the result of an asynchronous operation, and provides error information when the asynchronous call fails.</span></span>

<span data-ttu-id="d636e-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d636e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d636e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d636e-108">Syntax</span></span>


```VB
SWbemSink.OnCompleted( _
  ByVal iHResult, _
  ByVal objWbemErrorObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="d636e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d636e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d636e-110">*ihresult*</span><span class="sxs-lookup"><span data-stu-id="d636e-110">*iHResult*</span></span> 
</dt> <dd>

<span data-ttu-id="d636e-111">Das HRESULT der abgeschlossenen asynchronen Methode.</span><span class="sxs-lookup"><span data-stu-id="d636e-111">The HRESULT of the completed asynchronous method.</span></span> <span data-ttu-id="d636e-112">Das HRESULT ist mit dem Wert identisch, der von einem entsprechenden com- [API für WMI](com-api-for-wmi.md) -Methodenaufrufe zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d636e-112">The HRESULT is the same as the value that is returned from an equivalent [COM API for WMI](com-api-for-wmi.md) method call.</span></span> <span data-ttu-id="d636e-113">Überprüfen Sie diesen Wert, um zu bestimmen, ob der asynchrone-Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="d636e-113">Check this value to determine whether or not the asynchronous call is successful.</span></span> <span data-ttu-id="d636e-114">Wenn der asynchrone-Aufrufvorgang erfolgreich ist, enthält dieser Parameter WBEM \_ S \_ No \_ Error (0).</span><span class="sxs-lookup"><span data-stu-id="d636e-114">If the asynchronous call is successful, this parameter contains WBEM\_S\_NO\_ERROR (0).</span></span> <span data-ttu-id="d636e-115">Wenn der asynchrone-Rückruf fehlschlägt, enthält dieser Parameter einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d636e-115">If the asynchronous call fails, this parameter contains an error code.</span></span>

</dd> <dt>

<span data-ttu-id="d636e-116">*objWbemErrorObject*</span><span class="sxs-lookup"><span data-stu-id="d636e-116">*objWbemErrorObject*</span></span> 
</dt> <dd>

<span data-ttu-id="d636e-117">Enthält ein " [**taubemlasterror**](swbemlasterror.md) "-Objekt, wenn die asynchrone Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="d636e-117">Contains an [**SWbemLastError**](swbemlasterror.md) object when the asynchronous method fails.</span></span>

</dd> <dt>

<span data-ttu-id="d636e-118">*objwbemasynccontext*</span><span class="sxs-lookup"><span data-stu-id="d636e-118">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="d636e-119">Dabei handelt es sich um ein-Objekt, das an den ursprünglichen asynchronen- [**Befehl**](swbemnamedvalueset.md) übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d636e-119">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="d636e-120">Verwenden Sie diesen Parameter, um den Ursprung des asynchronen Aufrufs zu identifizieren, der dieses Ereignis auslöst, wenn mehrere asynchrone Aufrufe mithilfe dieser Objekt Senke durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d636e-120">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d636e-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d636e-121">Return value</span></span>

<span data-ttu-id="d636e-122">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d636e-122">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d636e-123">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d636e-123">Error codes</span></span>

<span data-ttu-id="d636e-124">Nach Abschluss des **oncompletion** -Ereignisses kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der folgenden Fehlercodes enthalten.</span><span class="sxs-lookup"><span data-stu-id="d636e-124">After completion of the **OnCompleted** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="d636e-125">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d636e-125">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d636e-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="d636e-126">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d636e-127">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d636e-127">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d636e-128">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d636e-128">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d636e-129">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="d636e-129">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="d636e-130">Netzwerkfehler. der normale Betrieb wird verhindert.</span><span class="sxs-lookup"><span data-stu-id="d636e-130">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d636e-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d636e-131">Remarks</span></span>

<span data-ttu-id="d636e-132">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="d636e-132">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="d636e-133">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="d636e-133">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="d636e-134">Um die Risiken auszuschließen, verwenden Sie die semisynchrone oder synchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="d636e-134">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="d636e-135">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d636e-135">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d636e-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d636e-136">Requirements</span></span>



| <span data-ttu-id="d636e-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d636e-137">Requirement</span></span> | <span data-ttu-id="d636e-138">Wert</span><span class="sxs-lookup"><span data-stu-id="d636e-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d636e-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d636e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d636e-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d636e-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d636e-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d636e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d636e-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d636e-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d636e-143">Header</span><span class="sxs-lookup"><span data-stu-id="d636e-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="d636e-144"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d636e-144"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d636e-145">IDL</span><span class="sxs-lookup"><span data-stu-id="d636e-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d636e-146"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d636e-146"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="d636e-147">DLL</span><span class="sxs-lookup"><span data-stu-id="d636e-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d636e-148"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d636e-148"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d636e-149">CLSID</span><span class="sxs-lookup"><span data-stu-id="d636e-149">CLSID</span></span><br/>                    | <span data-ttu-id="d636e-150">CLSID- \_ Swap-senbemsink</span><span class="sxs-lookup"><span data-stu-id="d636e-150">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="d636e-151">IID</span><span class="sxs-lookup"><span data-stu-id="d636e-151">IID</span></span><br/>                      | <span data-ttu-id="d636e-152">IID \_ iswbemsinkevents</span><span class="sxs-lookup"><span data-stu-id="d636e-152">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



 

