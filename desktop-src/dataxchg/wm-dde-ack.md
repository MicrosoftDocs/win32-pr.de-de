---
title: WM_DDE_ACK Meldung (DDE. h)
description: Die "WM \_ DDE \_ ACK"-Meldung benachrichtigt eine dynamischer Datenaustausch (DDE)-Anwendung über die Bestätigung und Verarbeitung der folgenden Nachrichten WM \_ DDE \_ Poke, WM \_ DDE \_ Execute, WM \_ DDE \_ Data, WM \_ DDE- \_ Empfehlung, WM \_ DDE \_ unempfehlung, WM \_ DDE \_ initiieren oder WM \_ DDE \_ Request (in einigen Fällen). Um diese Nachricht zu veröffentlichen, wenden Sie die PostMessage-Funktion mit den folgenden Parametern an.
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- WM_DDE_ACK Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DDE_ACK
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a407fc6cad7077586539f119dd65be59a507cacd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040528"
---
# <a name="wm_dde_ack-message"></a><span data-ttu-id="b450a-105">WM-DDE-Bestätigungs \_ \_ Meldung</span><span class="sxs-lookup"><span data-stu-id="b450a-105">WM\_DDE\_ACK message</span></span>

<span data-ttu-id="b450a-106">Die **"WM \_ DDE \_ ACK** "-Nachricht benachrichtigt eine dynamischer Datenaustausch (DDE)-Anwendung über die Bestätigung und Verarbeitung der folgenden Nachrichten: [**WM \_ DDE \_ Poke**](wm-dde-poke.md), [**WM \_ DDE \_ Execute**](wm-dde-execute.md), [**WM \_ DDE \_ Data**](wm-dde-data.md), [**WM DDE- \_ \_ Empfehlung**](wm-dde-advise.md), [**WM \_ DDE \_ unempfehlung**](wm-dde-unadvise.md), [**WM \_ DDE \_ initiieren**](wm-dde-initiate.md)oder [**WM DDE- \_ \_ Anforderung**](wm-dde-request.md) (in einigen Fällen).</span><span class="sxs-lookup"><span data-stu-id="b450a-106">The **WM\_DDE\_ACK** message notifies a Dynamic Data Exchange (DDE) application of the receipt and processing of the following messages: [**WM\_DDE\_POKE**](wm-dde-poke.md), [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), [**WM\_DDE\_DATA**](wm-dde-data.md), [**WM\_DDE\_ADVISE**](wm-dde-advise.md), [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md), [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), or [**WM\_DDE\_REQUEST**](wm-dde-request.md) (in some cases).</span></span>

<span data-ttu-id="b450a-107">Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="b450a-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a><span data-ttu-id="b450a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b450a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b450a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b450a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b450a-110">Bei der Reaktion auf " [**WM \_ DDE \_ initiieren**](wm-dde-initiate.md)" ist dieser Parameter ein Handle für das Server Fenster, das die Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="b450a-110">When responding to [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), this parameter is a handle to the server window sending the message.</span></span>

<span data-ttu-id="b450a-111">Bei der Reaktion auf " [**WM \_ DDE \_ Execute**](wm-dde-execute.md)" ist dieser Parameter ein Handle für das Server Fenster, das die Meldung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b450a-111">When responding to [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), this parameter is a handle to the server window posting the message.</span></span>

<span data-ttu-id="b450a-112">Beim Antworten auf alle anderen Nachrichten ist dieser Parameter ein Handle für das Client-oder Server Fenster, das die Meldung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b450a-112">When replying to all other messages, this parameter is a handle to the client or server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="b450a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b450a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b450a-114">Bei der Reaktion auf " [**WM \_ DDE \_ initiieren**](wm-dde-initiate.md)" enthält das nieder wertige Wort ein Atom, das die antwortende Anwendung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b450a-114">When responding to [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), the low-order word contains an atom that identifies the replying application.</span></span> <span data-ttu-id="b450a-115">Das Haupt Wort enthält ein Atom, das das Thema identifiziert, für das eine Konversation eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="b450a-115">The high-order word contains an atom that identifies the topic for which a conversation is being established.</span></span>

<span data-ttu-id="b450a-116">Bei der Reaktion auf [**WM \_ DDE \_ Execute**](wm-dde-execute.md)gibt das nieder wertige Wort eine [**ddeack**](/windows/desktop/api/Dde/ns-dde-ddeack) -Struktur an, die eine Reihe von Flags enthält, die den Status der Antwort angeben.</span><span class="sxs-lookup"><span data-stu-id="b450a-116">When responding to [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), the low-order word specifies a [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) structure containing a series of flags that indicate the status of the response.</span></span> <span data-ttu-id="b450a-117">Das höchst wertige Wort ist ein Handle für ein globales Speicher Objekt, das die Befehls Zeichenfolge enthält, die in der **WM- \_ DDE- \_ Ausführungs** Nachricht empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="b450a-117">The high-order word is a handle to a global memory object that contains the command string that was received in the **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="b450a-118">Beim Antworten auf alle anderen Nachrichten gibt das nieder wertige Wort eine [**ddeack**](/windows/desktop/api/Dde/ns-dde-ddeack) -Struktur an, die eine Reihe von Flags enthält, die den Status der Antwort angeben.</span><span class="sxs-lookup"><span data-stu-id="b450a-118">When replying to all other messages, the low-order word specifies a [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) structure containing a series of flags that indicate the status of the response.</span></span> <span data-ttu-id="b450a-119">Das höchst wertige Wort enthält ein globales Atom, das den Namen des Datenelements identifiziert, für das die Antwort gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="b450a-119">The high-order word contains a global atom that identifies the name of the data item for which the response is sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b450a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b450a-120">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="b450a-121">Veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="b450a-121">Posting</span></span>

<span data-ttu-id="b450a-122">Außer als Antwort auf die " [**WM DDE"- \_ \_ Initiierungs**](wm-dde-initiate.md) Nachricht stellt die Anwendung die " **WM \_ DDE \_ ACK** "-Nachricht durch Aufrufen der [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion und nicht durch Aufrufen der [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion zur Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b450a-122">Except in response to the [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message, the application posts the **WM\_DDE\_ACK** message by calling the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function, not by calling the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span> <span data-ttu-id="b450a-123">Bei der Reaktion auf " **WM \_ DDE \_ initiieren**" sendet die Anwendung die " **WM \_ DDE \_ ACK** "-Nachricht, indem **SendMessage** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b450a-123">When responding to **WM\_DDE\_INITIATE**, the application sends the **WM\_DDE\_ACK** message by calling **SendMessage**.</span></span> <span data-ttu-id="b450a-124">In diesem Fall sollte weder der Anwendungsname Atom noch das Atom-Name-Atom den Wert **null** aufweisen (auch wenn die WM-DDE-Nachricht die Meldung **null** -Atome **\_ \_ initiiert** hat).</span><span class="sxs-lookup"><span data-stu-id="b450a-124">In this case, neither the application-name atom nor the topic-name atom should be **NULL** (even if the **WM\_DDE\_INITIATE** message specified **NULL** atoms).</span></span>

<span data-ttu-id="b450a-125">Beim Bestätigen einer Nachricht mit einem begleitenden Atom kann die Anwendung, die die WM-DDE-Bestätigung veröffentlicht, entweder das Atom wieder verwenden, das die ursprüngliche Nachricht begleitet hat, oder Sie kann Sie löschen und eine neue erstellen. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="b450a-125">When acknowledging any message with an accompanying atom, the application posting **WM\_DDE\_ACK** can either reuse the atom that accompanied the original message, or it can delete it and create a new one.</span></span>

<span data-ttu-id="b450a-126">Wenn Sie [**WM \_ DDE \_ Execute**](wm-dde-execute.md)bestätigen, sollte die Anwendung, die die " **WM \_ DDE \_ ACK** "-Bestätigung sendet, das in der ursprünglichen " **WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b450a-126">When acknowledging [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), the application that posts **WM\_DDE\_ACK** should reuse the global memory object identified in the original **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="b450a-127">Alle zurückgegebenen **WM- \_ DDE \_** -Bestätigungsnachrichten müssen den *LPARAM* -Parameter durch Aufrufen der [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) -Funktion oder der [**reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) -Funktion erstellen oder wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="b450a-127">All posted **WM\_DDE\_ACK** messages must create or reuse the *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="b450a-128">Wenn eine Anwendung die Beendigung einer Konversation initiiert hat, indem [**WM \_ DDE \_ beendet**](wm-dde-terminate.md) wird und eine Bestätigung erwartet wird, sollte die wartende Anwendung nachfolgende Nachrichten, die von der anderen Anwendung gesendet werden, nicht bestätigen (positiv oder negativ).</span><span class="sxs-lookup"><span data-stu-id="b450a-128">If an application has initiated the termination of a conversation by posting [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) and is awaiting confirmation, the waiting application should not acknowledge (positively or negatively) any subsequent messages sent by the other application.</span></span> <span data-ttu-id="b450a-129">Die wartende Anwendung sollte alle Atome oder gemeinsam genutzten Speicher Objekte löschen, die in diesen Beteiligten Nachrichten empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="b450a-129">The waiting application should delete any atoms or shared memory objects received in these intervening messages.</span></span> <span data-ttu-id="b450a-130">Arbeitsspeicher Objekte sollten nicht freigegeben werden, wenn das **frelease** -Flag in den Daten Meldungen [**WM \_ DDE \_ Poke**](wm-dde-poke.md) und [**WM \_ DDE \_**](wm-dde-data.md) auf **false** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b450a-130">Memory objects should not be freed if the **fRelease** flag is set to **FALSE** in [**WM\_DDE\_POKE**](wm-dde-poke.md) and [**WM\_DDE\_DATA**](wm-dde-data.md) messages.</span></span>

### <a name="receiving"></a><span data-ttu-id="b450a-131">Empfangen</span><span class="sxs-lookup"><span data-stu-id="b450a-131">Receiving</span></span>

<span data-ttu-id="b450a-132">Die Anwendung, die eine **WM- \_ DDE \_** -Bestätigungsnachricht empfängt, sollte alle der Nachricht begleitenden Atome löschen.</span><span class="sxs-lookup"><span data-stu-id="b450a-132">The application that receives a **WM\_DDE\_ACK** message should delete all atoms accompanying the message.</span></span> <span data-ttu-id="b450a-133">Wenn die Anwendung eine **WM- \_ DDE \_** -Bestätigung als Antwort auf eine Nachricht mit einem begleitenden globalen Speicher Objekt empfängt und das-Objekt mit der auf **false** festgelegten **freleaseflags** gesendet wurde, ist die Anwendung für das Löschen des Objekts verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="b450a-133">If the application receives a **WM\_DDE\_ACK** in response to a message with an accompanying global memory object, and the object was sent with the **fRelease** flags set to **FALSE**, the application is responsible for deleting the object.</span></span>

<span data-ttu-id="b450a-134">Wenn die Anwendung eine negative **WM- \_ DDE \_** -Bestätigungsnachricht empfängt, die als Antwort auf eine [**WM-DDE-Benachrichtigungs \_ \_**](wm-dde-advise.md) Meldung gepostet wurde, sollte die Anwendung das mit der ursprünglichen **WM \_ DDE \_** -Benachrichtigungs Meldung veröffentlichte globale Speicher Objekt löschen.</span><span class="sxs-lookup"><span data-stu-id="b450a-134">If the application receives a negative **WM\_DDE\_ACK** message posted in reply to a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, the application should delete the global memory object posted with the original **WM\_DDE\_ADVISE** message.</span></span> <span data-ttu-id="b450a-135">Wenn die Anwendung eine negative **WM- \_ DDE \_** -Bestätigungsnachricht empfängt, die als Antwort auf eine [**WM-DDE- \_ \_ Daten**](wm-dde-data.md), [**WM \_ DDE \_ Poke**](wm-dde-poke.md)oder [**WM \_ DDE \_ Execute**](wm-dde-execute.md) -Nachricht gepostet wurde, sollte die Anwendung das globale Speicher Objekt löschen, das mit der ursprünglichen **WM DDE- \_ \_ Daten**, **WM \_ DDE \_ Poke** oder **WM \_ DDE \_ Execute** ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b450a-135">If the application receives a negative **WM\_DDE\_ACK** message posted in reply to a [**WM\_DDE\_DATA**](wm-dde-data.md), [**WM\_DDE\_POKE**](wm-dde-poke.md), or [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message, the application should delete the global memory object posted with the original **WM\_DDE\_DATA**, **WM\_DDE\_POKE**, or **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="b450a-136">Die Anwendung, die eine gepostete **WM- \_ DDE \_** -Bestätigungsnachricht empfängt, muss den *LPARAM* -Parameter mithilfe der [**freeddelta param**](/windows/desktop/api/Dde/nf-dde-freeddelparam) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="b450a-136">The application that receives a posted **WM\_DDE\_ACK** message must free the *lParam* parameter by using the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b450a-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b450a-137">Requirements</span></span>



| <span data-ttu-id="b450a-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b450a-138">Requirement</span></span> | <span data-ttu-id="b450a-139">Wert</span><span class="sxs-lookup"><span data-stu-id="b450a-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b450a-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b450a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b450a-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b450a-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b450a-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b450a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b450a-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b450a-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b450a-144">Header</span><span class="sxs-lookup"><span data-stu-id="b450a-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="b450a-145"><dt>DDE. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b450a-145"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b450a-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b450a-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="b450a-147">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="b450a-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b450a-148">**DDE ACK**</span><span class="sxs-lookup"><span data-stu-id="b450a-148">**DDEACK**</span></span>](/windows/desktop/api/Dde/ns-dde-ddeack)
</dt> <dt>

[<span data-ttu-id="b450a-149">**Freeddelta param**</span><span class="sxs-lookup"><span data-stu-id="b450a-149">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="b450a-150">**Packddelta param**</span><span class="sxs-lookup"><span data-stu-id="b450a-150">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="b450a-151">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="b450a-151">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="b450a-152">**Reuseddelta param**</span><span class="sxs-lookup"><span data-stu-id="b450a-152">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="b450a-153">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="b450a-153">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="b450a-154">**Unpackddelta param**</span><span class="sxs-lookup"><span data-stu-id="b450a-154">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="b450a-155">**WM \_ DDE- \_ Empfehlung**</span><span class="sxs-lookup"><span data-stu-id="b450a-155">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

[<span data-ttu-id="b450a-156">**WM- \_ DDE- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="b450a-156">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="b450a-157">**WM \_ DDE \_ Ausführen**</span><span class="sxs-lookup"><span data-stu-id="b450a-157">**WM\_DDE\_EXECUTE**</span></span>](wm-dde-execute.md)
</dt> <dt>

[<span data-ttu-id="b450a-158">**WM \_ DDE \_ initiieren**</span><span class="sxs-lookup"><span data-stu-id="b450a-158">**WM\_DDE\_INITIATE**</span></span>](wm-dde-initiate.md)
</dt> <dt>

[<span data-ttu-id="b450a-159">**WM \_ DDE \_ Poke**</span><span class="sxs-lookup"><span data-stu-id="b450a-159">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="b450a-160">**WM- \_ DDE- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="b450a-160">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

[<span data-ttu-id="b450a-161">**WM- \_ DDE \_ Beenden**</span><span class="sxs-lookup"><span data-stu-id="b450a-161">**WM\_DDE\_TERMINATE**</span></span>](wm-dde-terminate.md)
</dt> <dt>

[<span data-ttu-id="b450a-162">**WM \_ DDE \_ nicht Empfehlung**</span><span class="sxs-lookup"><span data-stu-id="b450a-162">**WM\_DDE\_UNADVISE**</span></span>](wm-dde-unadvise.md)
</dt> <dt>

<span data-ttu-id="b450a-163">**Licher**</span><span class="sxs-lookup"><span data-stu-id="b450a-163">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b450a-164">Informationen zu dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="b450a-164">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

