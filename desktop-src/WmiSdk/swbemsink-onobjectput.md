---
description: Das onobjectput-Ereignis eines slibemsink-Objekts wird ausgelöst, wenn ein asynchroner Put-Vorgang beendet ist. Dieses Ereignis gibt den Objekt Pfad der-Instanz oder der gespeicherten-Klasse zurück.
ms.assetid: 2046dd03-ac2c-49fa-b1ad-a458967709e5
ms.tgt_platform: multiple
title: 'Iswbemsinkevents:: onobjectput-Ereignis (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectPut
- ISWbemSinkEvents.OnObjectPut
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c6ed42105efe407558d80cd108e657e396e88763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218480"
---
# <a name="iswbemsinkeventsonobjectput-event"></a><span data-ttu-id="325d7-104">Iswbemsinkevents:: onobjectput-Ereignis</span><span class="sxs-lookup"><span data-stu-id="325d7-104">ISWbemSinkEvents::OnObjectPut event</span></span>

<span data-ttu-id="325d7-105">Das **onobjectput** -Ereignis eines [**slibemsink**](swbemsink.md) -Objekts wird ausgelöst, wenn ein asynchroner Put-Vorgang beendet ist.</span><span class="sxs-lookup"><span data-stu-id="325d7-105">The **OnObjectPut** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous Put operation is complete.</span></span> <span data-ttu-id="325d7-106">Dieses Ereignis gibt den Objekt Pfad der-Instanz oder der gespeicherten-Klasse zurück.</span><span class="sxs-lookup"><span data-stu-id="325d7-106">This event returns the object path of the instance or the saved class.</span></span>

<span data-ttu-id="325d7-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="325d7-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="325d7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="325d7-108">Syntax</span></span>


```VB
SWbemSink.OnObjectPut( _
  ByVal objWbemObjectPath, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="325d7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="325d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="325d7-110">*objwbefubjectpath*</span><span class="sxs-lookup"><span data-stu-id="325d7-110">*objWbemObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="325d7-111">Ein Objekt vom Typ " [**errbemubjectpath**](swbemobjectpath.md) ", das den Objekt Pfad der Instanz oder Klasse enthält, die der Put-Vorgang in WMI schreibt.</span><span class="sxs-lookup"><span data-stu-id="325d7-111">An [**SWbemObjectPath**](swbemobjectpath.md) object, that contains the object path of the instance or class that the put operation writes to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="325d7-112">*objwbemasynccontext*</span><span class="sxs-lookup"><span data-stu-id="325d7-112">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="325d7-113">Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das an den ursprünglichen asynchronen-Befehl übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="325d7-113">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="325d7-114">Verwenden Sie diesen Parameter, um den Ursprung des asynchronen Aufrufs zu identifizieren, der dieses Ereignis auslöst, wenn mehrere asynchrone Aufrufe mithilfe dieser Objekt Senke durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="325d7-114">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="325d7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="325d7-115">Return value</span></span>

<span data-ttu-id="325d7-116">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="325d7-116">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="325d7-117">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="325d7-117">Error codes</span></span>

<span data-ttu-id="325d7-118">Nach Abschluss des **onobjectput** -Ereignisses kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der folgenden Fehlercodes enthalten.</span><span class="sxs-lookup"><span data-stu-id="325d7-118">After the completion of the **OnObjectPut** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="325d7-119">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="325d7-119">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="325d7-120">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="325d7-120">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="325d7-121">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="325d7-121">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="325d7-122">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="325d7-122">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="325d7-123">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="325d7-123">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="325d7-124">Netzwerkfehler. der normale Betrieb wird verhindert.</span><span class="sxs-lookup"><span data-stu-id="325d7-124">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="325d7-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="325d7-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="325d7-126">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="325d7-126">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="325d7-127">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="325d7-127">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="325d7-128">Um die Risiken auszuschließen, verwenden Sie entweder semisynchrone Kommunikation oder synchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="325d7-128">To eliminate the risks, use either semi-synchronous communication or synchronous communication.</span></span> <span data-ttu-id="325d7-129">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="325d7-129">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="325d7-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="325d7-130">Requirements</span></span>



| <span data-ttu-id="325d7-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="325d7-131">Requirement</span></span> | <span data-ttu-id="325d7-132">Wert</span><span class="sxs-lookup"><span data-stu-id="325d7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="325d7-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="325d7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="325d7-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="325d7-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="325d7-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="325d7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="325d7-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="325d7-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="325d7-137">Header</span><span class="sxs-lookup"><span data-stu-id="325d7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="325d7-138"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="325d7-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="325d7-139">IDL</span><span class="sxs-lookup"><span data-stu-id="325d7-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="325d7-140"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="325d7-140"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="325d7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="325d7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="325d7-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="325d7-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="325d7-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="325d7-143">CLSID</span></span><br/>                    | <span data-ttu-id="325d7-144">CLSID- \_ Swap-senbemsink</span><span class="sxs-lookup"><span data-stu-id="325d7-144">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="325d7-145">IID</span><span class="sxs-lookup"><span data-stu-id="325d7-145">IID</span></span><br/>                      | <span data-ttu-id="325d7-146">IID \_ iswbemsinkevents</span><span class="sxs-lookup"><span data-stu-id="325d7-146">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="325d7-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="325d7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="325d7-148">**Swap-Senke**</span><span class="sxs-lookup"><span data-stu-id="325d7-148">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

