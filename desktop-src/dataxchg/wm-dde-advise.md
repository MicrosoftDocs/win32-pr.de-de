---
title: WM_DDE_ADVISE Meldung (DDE. h)
description: Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet die "WM DDE"- \_ \_ Empfehlung an eine DDE-Serveranwendung, um den Server aufzufordern, ein Update für ein Datenelement anzufordern, wenn das Element geändert wird.
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- WM_DDE_ADVISE Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DDE_ADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832c6991169b71955c0ab21b59d2b55b0b54fc9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103518"
---
# <a name="wm_dde_advise-message"></a><span data-ttu-id="55bd9-104">WM-DDE-Benachrichtigungs \_ \_ Meldung</span><span class="sxs-lookup"><span data-stu-id="55bd9-104">WM\_DDE\_ADVISE message</span></span>

<span data-ttu-id="55bd9-105">Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet die " **WM DDE"- \_ \_ Empfehlung** an eine DDE-Serveranwendung, um den Server aufzufordern, ein Update für ein Datenelement anzufordern, wenn das Element geändert wird.</span><span class="sxs-lookup"><span data-stu-id="55bd9-105">A Dynamic Data Exchange (DDE) client application posts the **WM\_DDE\_ADVISE** message to a DDE server application to request the server to supply an update for a data item whenever the item changes.</span></span>

<span data-ttu-id="55bd9-106">Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="55bd9-106">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a><span data-ttu-id="55bd9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="55bd9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55bd9-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55bd9-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55bd9-109">Ein Handle für das Client Fenster, das die Meldung bereitstellen soll.</span><span class="sxs-lookup"><span data-stu-id="55bd9-109">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="55bd9-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55bd9-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55bd9-111">Das nieder wertige Wort ist ein Handle für ein globales Speicher Objekt, das eine [**DDE-Empfehlung**](/windows/desktop/api/Dde/ns-dde-ddeadvise) -Struktur enthält, die angibt, wie die Daten gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="55bd9-111">The low-order word is a handle to a global memory object containing a [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) structure that specifies how the data is to be sent.</span></span>

<span data-ttu-id="55bd9-112">Das hochwertige Wort enthält ein Atom, das das angeforderte Datenelement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="55bd9-112">The high-order word contains an atom that identifies the requested data item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55bd9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55bd9-113">Remarks</span></span>

<span data-ttu-id="55bd9-114">Wenn eine Client Anwendung mehr als ein Zwischenablage Format für ein einzelnes Thema und Element unterstützt, kann Sie mehrere **WM-DDE-Anmeldungs \_ \_** Nachrichten für das Thema und das Element bereitstellen und für jede Nachricht ein anderes Zwischenablage Format angeben.</span><span class="sxs-lookup"><span data-stu-id="55bd9-114">If a client application supports more than one clipboard format for a single topic and item, it can post multiple **WM\_DDE\_ADVISE** messages for the topic and item, specifying a different clipboard format with each message.</span></span> <span data-ttu-id="55bd9-115">Beachten Sie, dass ein Server mehrere Formate nur für heiße Daten Verknüpfungen unterstützen kann, nicht für warm Daten Links.</span><span class="sxs-lookup"><span data-stu-id="55bd9-115">Note that a server can support multiple formats only for hot data links, not warm data links.</span></span>

### <a name="posting"></a><span data-ttu-id="55bd9-116">Veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="55bd9-116">Posting</span></span>

<span data-ttu-id="55bd9-117">Die Client Anwendung sendet die **Empfehlung "WM \_ DDE- \_ Empfehlung** " durch Aufrufen der [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion und nicht der [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="55bd9-117">The client application posts the **WM\_DDE\_ADVISE** message by calling the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function, not the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span>

<span data-ttu-id="55bd9-118">Die Client Anwendung ordnet das globale Speicher Objekt mithilfe der [**globalbelegungsfunktion**](/windows/desktop/api/winbase/nf-winbase-globalalloc) zu.</span><span class="sxs-lookup"><span data-stu-id="55bd9-118">The client application allocates the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="55bd9-119">Das Atom wird mithilfe der [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) -Funktion zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="55bd9-119">It allocates the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="55bd9-120">Die Client Anwendung muss den *LPARAM* -Parameter " **WM \_ DDE- \_ Empfehlung** " durch Aufrufen der Funktion " [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) " oder der Funktion " [**reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) " erstellen oder wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="55bd9-120">The client application must create or reuse the **WM\_DDE\_ADVISE** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="55bd9-121">Wenn die empfangende Anwendung (Server) mit einer negativen [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung antwortet, muss das Objekt von der Posting-Anwendung gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="55bd9-121">If the receiving (server) application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the posting application must delete the object.</span></span>

<span data-ttu-id="55bd9-122">Das **frelease** -Flag wird nicht in **WM- \_ DDE \_** -Anmeldungs Nachrichten verwendet, aber das Datenfreigabe Verhalten ähnelt dem der [**WM- \_ DDE- \_ Daten**](wm-dde-data.md) und [**WM \_ DDE \_ Poke**](wm-dde-poke.md) -Nachrichten, bei denen **frelease** **true** ist.</span><span class="sxs-lookup"><span data-stu-id="55bd9-122">The **fRelease** flag is not used in **WM\_DDE\_ADVISE** messages, but their data-freeing behavior is similar to that of [**WM\_DDE\_DATA**](wm-dde-data.md) and [**WM\_DDE\_POKE**](wm-dde-poke.md) messages where **fRelease** is **TRUE**.</span></span>

### <a name="receiving"></a><span data-ttu-id="55bd9-123">Empfangen</span><span class="sxs-lookup"><span data-stu-id="55bd9-123">Receiving</span></span>

<span data-ttu-id="55bd9-124">Die Serveranwendung sendet die " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) "-Nachricht, um positiv oder negativ zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="55bd9-124">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="55bd9-125">Beim Veröffentlichen der **WM- \_ DDE \_**-Bestätigung kann die Anwendung das Atom wieder verwenden oder löschen und ein neues erstellen.</span><span class="sxs-lookup"><span data-stu-id="55bd9-125">When posting **WM\_DDE\_ACK**, the application can reuse the atom or delete it and create a new one.</span></span> <span data-ttu-id="55bd9-126">Wenn die **WM- \_ DDE \_** -Bestätigungsnachricht positiv ist, sollte die Anwendung das globale Speicher Objekt löschen, andernfalls sollte die Anwendung das Objekt nicht löschen.</span><span class="sxs-lookup"><span data-stu-id="55bd9-126">If the **WM\_DDE\_ACK** message is positive, the application should delete the global memory object; otherwise, the application should not delete the object.</span></span>

<span data-ttu-id="55bd9-127">Der Server muss den " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *LPARAM* "-Parameter durch Aufrufen der [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) -Funktion oder der [**reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) -Funktion erstellen oder wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="55bd9-127">The server must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="55bd9-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55bd9-128">Requirements</span></span>



| <span data-ttu-id="55bd9-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55bd9-129">Requirement</span></span> | <span data-ttu-id="55bd9-130">Wert</span><span class="sxs-lookup"><span data-stu-id="55bd9-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55bd9-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55bd9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="55bd9-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55bd9-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="55bd9-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55bd9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="55bd9-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55bd9-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="55bd9-135">Header</span><span class="sxs-lookup"><span data-stu-id="55bd9-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="55bd9-136"><dt>DDE. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55bd9-136"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55bd9-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55bd9-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="55bd9-138">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="55bd9-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="55bd9-139">**DDE-Empfehlung**</span><span class="sxs-lookup"><span data-stu-id="55bd9-139">**DDEADVISE**</span></span>](/windows/desktop/api/Dde/ns-dde-ddeadvise)
</dt> <dt>

[<span data-ttu-id="55bd9-140">**Freeddelta param**</span><span class="sxs-lookup"><span data-stu-id="55bd9-140">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="55bd9-141">**Globaladdatom**</span><span class="sxs-lookup"><span data-stu-id="55bd9-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="55bd9-142">**Packddelta param**</span><span class="sxs-lookup"><span data-stu-id="55bd9-142">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="55bd9-143">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="55bd9-143">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="55bd9-144">**Reuseddelta param**</span><span class="sxs-lookup"><span data-stu-id="55bd9-144">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="55bd9-145">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="55bd9-145">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="55bd9-146">**Unpackddelta param**</span><span class="sxs-lookup"><span data-stu-id="55bd9-146">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="55bd9-147">**WM-DDE-Bestätigung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="55bd9-147">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="55bd9-148">**WM- \_ DDE- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="55bd9-148">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="55bd9-149">**WM \_ DDE \_ Poke**</span><span class="sxs-lookup"><span data-stu-id="55bd9-149">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="55bd9-150">**WM- \_ DDE- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="55bd9-150">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

<span data-ttu-id="55bd9-151">**Licher**</span><span class="sxs-lookup"><span data-stu-id="55bd9-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="55bd9-152">Informationen zu dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="55bd9-152">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

