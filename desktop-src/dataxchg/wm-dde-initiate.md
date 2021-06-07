---
title: WM_DDE_INITIATE (Dde.h)
description: Eine dynamischer Datenaustausch-Clientanwendung (DDE) sendet eine WM DDE INITIATE-Nachricht, um eine Konversation mit einer Serveranwendung zu initiieren, die auf die angegebenen Anwendungs- \_ \_ und Themennamen antwortet.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- WM_DDE_INITIATE von Nachrichtendatenaustausch
topic_type:
- apiref
api_name:
- WM_DDE_INITIATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf65e222c7711d429db44e391d4f03c35997e219
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386728"
---
# <a name="wm_dde_initiate-message"></a><span data-ttu-id="20252-104">WM \_ DDE \_ INITIATE-Nachricht</span><span class="sxs-lookup"><span data-stu-id="20252-104">WM\_DDE\_INITIATE message</span></span>

<span data-ttu-id="20252-105">Eine dynamischer Datenaustausch-Clientanwendung (DDE) sendet eine **WM \_ DDE \_ INITIATE-Nachricht,** um eine Konversation mit einer Serveranwendung zu initiieren, die auf die angegebenen Anwendungs- und Themennamen antwortet.</span><span class="sxs-lookup"><span data-stu-id="20252-105">A Dynamic Data Exchange (DDE) client application sends a **WM\_DDE\_INITIATE** message to initiate a conversation with a server application responding to the specified application and topic names.</span></span> <span data-ttu-id="20252-106">Nach dem Empfang dieser Meldung wird von allen Serveranwendungen mit Namen, die der angegebenen Anwendung und dem angegebenen Thema unterstützen, erwartet, dass sie bestätigt werden.</span><span class="sxs-lookup"><span data-stu-id="20252-106">Upon receiving this message, all server applications with names that match the specified application and that support the specified topic are expected to acknowledge it.</span></span> <span data-ttu-id="20252-107">(Weitere Informationen finden Sie in der [**WM \_ DDE \_ ACK-Meldung.)**](wm-dde-ack.md)</span><span class="sxs-lookup"><span data-stu-id="20252-107">(For more information, see the [**WM\_DDE\_ACK**](wm-dde-ack.md) message.)</span></span>


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a><span data-ttu-id="20252-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="20252-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20252-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="20252-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20252-110">Ein Handle für das Clientfenster, das die Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="20252-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="20252-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="20252-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20252-112">Das Wort der niedrigen Ordnung enthält ein Atom, das die Anwendung identifiziert, mit der eine Konversation angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="20252-112">The low-order word contains an atom that identifies the application with which a conversation is requested.</span></span> <span data-ttu-id="20252-113">Der Anwendungsname darf keine Schrägstriche (/) oder schräge Schrägstriche () \\ enthalten.</span><span class="sxs-lookup"><span data-stu-id="20252-113">The application name cannot contain slashes (/) or backslashes (\\).</span></span> <span data-ttu-id="20252-114">Diese Zeichen sind für Netzwerkimplementierungen reserviert.</span><span class="sxs-lookup"><span data-stu-id="20252-114">These characters are reserved for network implementations.</span></span> <span data-ttu-id="20252-115">Wenn dieser Parameter **NULL ist,** wird eine Konversation mit allen Anwendungen angefordert.</span><span class="sxs-lookup"><span data-stu-id="20252-115">If this parameter is **NULL**, a conversation with all applications is requested.</span></span>

<span data-ttu-id="20252-116">Das obere Wort enthält ein Atom, das das Thema identifiziert, für das eine Konversation angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="20252-116">The high-order word contains an atom that identifies the topic for which a conversation is requested.</span></span> <span data-ttu-id="20252-117">Wenn das Thema NULL **ist,** werden Konversationen für alle verfügbaren Themen angefordert.</span><span class="sxs-lookup"><span data-stu-id="20252-117">If the topic is **NULL**, conversations for all available topics are requested.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20252-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20252-118">Remarks</span></span>

<span data-ttu-id="20252-119">Wenn das niedrige Wort von *lParam* **NULL ist,** kann jede Serveranwendung antworten.</span><span class="sxs-lookup"><span data-stu-id="20252-119">If the low-order word of *lParam* is **NULL**, any server application can respond.</span></span> <span data-ttu-id="20252-120">Wenn das obere Wort *von lParam* **NULL ist,** ist jedes Thema gültig.</span><span class="sxs-lookup"><span data-stu-id="20252-120">If the high-order word of *lParam* is **NULL**, any topic is valid.</span></span> <span data-ttu-id="20252-121">Beim Empfang einer **WM \_ DDE \_ INITIATE-Anforderung,** bei der das obere Wort des *lParam-Parameters* auf **NULL** festgelegt ist, muss ein Server für jedes der unterstützten Themen eine [**WM \_ DDE \_ ACK-Nachricht**](wm-dde-ack.md) senden.</span><span class="sxs-lookup"><span data-stu-id="20252-121">Upon receiving a **WM\_DDE\_INITIATE** request with the high-order word of the *lParam* parameter set to **NULL**, a server must send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each of the topics it supports.</span></span>

### <a name="sending"></a><span data-ttu-id="20252-122">Senden</span><span class="sxs-lookup"><span data-stu-id="20252-122">Sending</span></span>

<span data-ttu-id="20252-123">Der Client überträgt die Nachricht an alle Fenster der obersten Ebene, indem der erste Parameter von [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) auf **HWND \_ BROADCAST festgelegt wird.**</span><span class="sxs-lookup"><span data-stu-id="20252-123">The client broadcasts the message to all top-level windows by setting the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="20252-124">Wenn die Clientanwendung bereits das Fensterhand handle des gewünschten Servers abgerufen hat, kann sie **WM \_ DDE \_ INITIATE** direkt an das Serverfenster senden, indem sie das Fensterhand handle des Servers als ersten Parameter von [**SendMessage übergibt.**](/windows/desktop/api/winuser/nf-winuser-sendmessage)</span><span class="sxs-lookup"><span data-stu-id="20252-124">If the client application has already obtained the window handle of the desired server, it can send **WM\_DDE\_INITIATE** directly to the server window by passing the server's window handle as the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span>

<span data-ttu-id="20252-125">Die Clientanwendung ordnet Atome zu, indem sie die [**GlobalAddAtom-Funktion**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) aufruft.</span><span class="sxs-lookup"><span data-stu-id="20252-125">The client application allocates atoms by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="20252-126">Wenn [**SendMessage zurückgegeben**](/windows/desktop/api/winuser/nf-winuser-sendmessage) wird, muss die Clientanwendung die Atome löschen.</span><span class="sxs-lookup"><span data-stu-id="20252-126">When [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application must delete the atoms.</span></span>

### <a name="receiving"></a><span data-ttu-id="20252-127">Empfangen</span><span class="sxs-lookup"><span data-stu-id="20252-127">Receiving</span></span>

<span data-ttu-id="20252-128">Um die Initiierung einer Konversation abschließen zu können, muss die Serveranwendung mit mindestens einer [**WM \_ DDE \_ ACK-Nachricht**](wm-dde-ack.md) antworten, wobei jede Nachricht für ein separates Thema gilt.</span><span class="sxs-lookup"><span data-stu-id="20252-128">To complete the initiation of a conversation, the server application must respond with one or more [**WM\_DDE\_ACK**](wm-dde-ack.md) messages, where each message is for a separate topic.</span></span> <span data-ttu-id="20252-129">Beim Senden **der WM \_ DDE \_ ACK-Nachricht** sollte der Server neue Atome erstellen. Die mit WM DDE INITIATE gesendeten Atome sollten **nicht wiederverwendet \_ \_ werden.**</span><span class="sxs-lookup"><span data-stu-id="20252-129">When sending **WM\_DDE\_ACK** message, the server should create new atoms; it should not reuse the atoms sent with **WM\_DDE\_INITIATE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="20252-130">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="20252-130">Requirements</span></span>



| <span data-ttu-id="20252-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20252-131">Requirement</span></span> | <span data-ttu-id="20252-132">Wert</span><span class="sxs-lookup"><span data-stu-id="20252-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20252-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20252-133">Minimum supported client</span></span><br/> | <span data-ttu-id="20252-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20252-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="20252-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20252-135">Minimum supported server</span></span><br/> | <span data-ttu-id="20252-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20252-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="20252-137">Header</span><span class="sxs-lookup"><span data-stu-id="20252-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="20252-138"><dt>Dde.h (einschließlich Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="20252-138"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20252-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20252-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="20252-140">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="20252-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="20252-141">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="20252-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="20252-142">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="20252-142">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="20252-143">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="20252-143">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="20252-144">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="20252-144">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="20252-145">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="20252-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="20252-146">Informationen dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="20252-146">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

