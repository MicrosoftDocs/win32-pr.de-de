---
description: Die Cancel-Methode des Swap-Objekts bricht alle ausstehenden asynchronen Vorgänge ab, die dieser Objekt Senke zugeordnet sind.
ms.assetid: dbe1eb24-5d9d-407a-b7c6-c58ec6891d7a
ms.tgt_platform: multiple
title: 'Iswbemsink:: Cancel-Methode (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.Cancel
- ISWbemSink.Cancel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 37bb44e8c34aa3cd7f9d491656461097e5a2bb5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218481"
---
# <a name="iswbemsinkcancel-method"></a><span data-ttu-id="97876-103">Iswbemsink:: Cancel-Methode</span><span class="sxs-lookup"><span data-stu-id="97876-103">ISWbemSink::Cancel method</span></span>

<span data-ttu-id="97876-104">Die **Cancel** -Methode des [**Swap**](swbemsink.md) -Objekts bricht alle ausstehenden asynchronen Vorgänge ab, die dieser Objekt Senke zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="97876-104">The **Cancel** method of the [**SWbemSink**](swbemsink.md) object cancels all outstanding asynchronous operations that are associated with this object sink.</span></span>

<span data-ttu-id="97876-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="97876-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="97876-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="97876-106">Syntax</span></span>


```VB
SWbemSink.Cancel()
```



## <a name="parameters"></a><span data-ttu-id="97876-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="97876-107">Parameters</span></span>

<span data-ttu-id="97876-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="97876-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="97876-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97876-109">Return value</span></span>

<span data-ttu-id="97876-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="97876-110">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="97876-111">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="97876-111">Error codes</span></span>

<span data-ttu-id="97876-112">Nach dem Abschluss der **Cancel** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der folgenden Fehlercodes enthalten.</span><span class="sxs-lookup"><span data-stu-id="97876-112">After the completion of the **Cancel** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="97876-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="97876-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="97876-114">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="97876-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="97876-115">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="97876-115">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="97876-116">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="97876-116">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="97876-117">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="97876-117">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="97876-118">Netzwerkfehler. der normale Betrieb wird verhindert.</span><span class="sxs-lookup"><span data-stu-id="97876-118">Networking error occurred, preventing normal operation.</span></span>

</dd> <dt>

<span data-ttu-id="97876-119">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="97876-119">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="97876-120">Der aktuelle oder der angegebene Benutzername und das Kennwort sind ungültig oder sind zum Herstellen der Verbindung autorisiert.</span><span class="sxs-lookup"><span data-stu-id="97876-120">Current or specified user name and password are not valid or authorized to make the connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97876-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97876-121">Remarks</span></span>

<span data-ttu-id="97876-122">Es ist nicht möglich, nur einen asynchronen-Befehl abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="97876-122">You cannot cancel only one asynchronous call.</span></span> <span data-ttu-id="97876-123">Wenn mehrere asynchrone Aufrufe ausstehen, die diese Objekt Senke verwenden, bricht diese Methode alle asynchronen Aufrufe mithilfe dieser Objekt Senke ab.</span><span class="sxs-lookup"><span data-stu-id="97876-123">If multiple asynchronous calls are pending that use this object sink, then this method cancels all the asynchronous calls using this object sink.</span></span> <span data-ttu-id="97876-124">Asynchrone Aufrufe, die anderen Objekt senken zugeordnet sind, bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="97876-124">Asynchronous calls that are associated with other object sinks continue unaffected.</span></span>

<span data-ttu-id="97876-125">Diese Senke kann **nichts** zugewiesen werden, um einen asynchronen Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="97876-125">You cannot assign this sink to **Nothing** to cancel an asynchronous operation.</span></span> <span data-ttu-id="97876-126">Sie müssen die **Cancel** -Methode aufzurufen, damit WMI den Vorgang abbricht und die zugeordneten Ressourcen freigibt.</span><span class="sxs-lookup"><span data-stu-id="97876-126">You must call the **Cancel** method to make WMI discontinue the operation and free the associated resources.</span></span> <span data-ttu-id="97876-127">Dies ist sehr wichtig bei langwierigen asynchronen Vorgängen wie z. b. Abfragen oder Vorgängen, die nicht vollständig ausgeführt werden, wie z. b. [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="97876-127">This is very important with lengthy asynchronous operations, such as queries, or operations that never complete, such as [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span></span>

> [!Note]  
> <span data-ttu-id="97876-128">Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke.</span><span class="sxs-lookup"><span data-stu-id="97876-128">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="97876-129">Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="97876-129">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="97876-130">Um die Risiken auszuschließen, verwenden Sie die semisynchrone oder synchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="97876-130">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="97876-131">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="97876-131">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="97876-132">Im folgenden Beispiel wird gezeigt, wie ein asynchroner-Befehl abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="97876-132">The following example shows you how to cancel an asynchronous call.</span></span>


```VB
objwbemsink.Cancel()
set objwbemsink= Nothing
```



## <a name="requirements"></a><span data-ttu-id="97876-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97876-133">Requirements</span></span>



| <span data-ttu-id="97876-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97876-134">Requirement</span></span> | <span data-ttu-id="97876-135">Wert</span><span class="sxs-lookup"><span data-stu-id="97876-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97876-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97876-136">Minimum supported client</span></span><br/> | <span data-ttu-id="97876-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97876-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97876-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97876-138">Minimum supported server</span></span><br/> | <span data-ttu-id="97876-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97876-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97876-140">Header</span><span class="sxs-lookup"><span data-stu-id="97876-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="97876-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="97876-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="97876-142">IDL</span><span class="sxs-lookup"><span data-stu-id="97876-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97876-143"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97876-143"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="97876-144">DLL</span><span class="sxs-lookup"><span data-stu-id="97876-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97876-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97876-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="97876-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="97876-146">CLSID</span></span><br/>                    | <span data-ttu-id="97876-147">CLSID- \_ Swap-senbemsink</span><span class="sxs-lookup"><span data-stu-id="97876-147">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="97876-148">IID</span><span class="sxs-lookup"><span data-stu-id="97876-148">IID</span></span><br/>                      | <span data-ttu-id="97876-149">IID \_ iswbemsink</span><span class="sxs-lookup"><span data-stu-id="97876-149">IID\_ISWbemSink</span></span><br/>                                                              |



## <a name="see-also"></a><span data-ttu-id="97876-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97876-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97876-151">**Swap-Senke**</span><span class="sxs-lookup"><span data-stu-id="97876-151">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

