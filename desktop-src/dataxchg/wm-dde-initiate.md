---
title: WM_DDE_INITIATE Meldung (DDE. h)
description: Eine dynamischer Datenaustausch (DDE)-Client Anwendung sendet eine \_ WM \_ -DDE-Initiierungs Nachricht, um eine Konversation mit einer Serveranwendung zu initiieren, die auf die angegebenen Anwendungs-und Themen Namen antwortet.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- WM_DDE_INITIATE Nachrichten Datenaustausch
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
ms.openlocfilehash: 36485db262c46d5364ee0ee26e7e6f39ccf0e677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391842"
---
# <a name="wm_dde_initiate-message"></a><span data-ttu-id="bc214-104">WM- \_ DDE- \_ Initiierungs Meldung</span><span class="sxs-lookup"><span data-stu-id="bc214-104">WM\_DDE\_INITIATE message</span></span>

<span data-ttu-id="bc214-105">Eine dynamischer Datenaustausch (DDE)-Client Anwendung sendet eine **WM- \_ DDE- \_ Initiierungs** Nachricht, um eine Konversation mit einer Serveranwendung zu initiieren, die auf die angegebenen Anwendungs-und Themen Namen antwortet.</span><span class="sxs-lookup"><span data-stu-id="bc214-105">A Dynamic Data Exchange (DDE) client application sends a **WM\_DDE\_INITIATE** message to initiate a conversation with a server application responding to the specified application and topic names.</span></span> <span data-ttu-id="bc214-106">Wenn diese Nachricht empfangen wird, wird Sie von allen Server Anwendungen mit Namen, die der angegebenen Anwendung entsprechen und die das angegebene Thema unterstützen, erwartet.</span><span class="sxs-lookup"><span data-stu-id="bc214-106">Upon receiving this message, all server applications with names that match the specified application and that support the specified topic are expected to acknowledge it.</span></span> <span data-ttu-id="bc214-107">(Weitere Informationen finden Sie in der " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) "-Meldung.)</span><span class="sxs-lookup"><span data-stu-id="bc214-107">(For more information, see the [**WM\_DDE\_ACK**](wm-dde-ack.md) message.)</span></span>


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a><span data-ttu-id="bc214-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc214-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc214-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc214-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc214-110">Ein Handle für das Client Fenster, das die Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="bc214-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="bc214-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc214-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc214-112">Das nieder wertige Wort enthält ein Atom, das die Anwendung identifiziert, mit der eine Konversation angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="bc214-112">The low-order word contains an atom that identifies the application with which a conversation is requested.</span></span> <span data-ttu-id="bc214-113">Der Anwendungsname darf keine Schrägstriche (/) oder umgekehrten Schrägstriche () enthalten \) .</span><span class="sxs-lookup"><span data-stu-id="bc214-113">The application name cannot contain slashes (/) or backslashes (\).</span></span> <span data-ttu-id="bc214-114">Diese Zeichen sind für Netzwerk Implementierungen reserviert.</span><span class="sxs-lookup"><span data-stu-id="bc214-114">These characters are reserved for network implementations.</span></span> <span data-ttu-id="bc214-115">Wenn dieser Parameter **null** ist, wird eine Konversation mit allen Anwendungen angefordert.</span><span class="sxs-lookup"><span data-stu-id="bc214-115">If this parameter is **NULL**, a conversation with all applications is requested.</span></span>

<span data-ttu-id="bc214-116">Das höchst wertige Wort enthält ein Atom, das das Thema identifiziert, für das eine Konversation angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="bc214-116">The high-order word contains an atom that identifies the topic for which a conversation is requested.</span></span> <span data-ttu-id="bc214-117">Wenn das Thema **null** ist, werden Konversationen für alle verfügbaren Themen angefordert.</span><span class="sxs-lookup"><span data-stu-id="bc214-117">If the topic is **NULL**, conversations for all available topics are requested.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc214-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc214-118">Remarks</span></span>

<span data-ttu-id="bc214-119">Wenn das nieder wertige Wort von *LPARAM* **null** ist, kann jede Serveranwendung Antworten.</span><span class="sxs-lookup"><span data-stu-id="bc214-119">If the low-order word of *lParam* is **NULL**, any server application can respond.</span></span> <span data-ttu-id="bc214-120">Wenn das hochwertige Wort *LPARAM* **null** ist, ist jedes Thema gültig.</span><span class="sxs-lookup"><span data-stu-id="bc214-120">If the high-order word of *lParam* is **NULL**, any topic is valid.</span></span> <span data-ttu-id="bc214-121">Beim Empfang einer **WM- \_ DDE- \_ Initiierungs** Anforderung, bei der das hochwertige Wort des *LPARAM* -Parameters auf **null** festgelegt ist, muss ein Server eine [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht für jedes der unterstützten Themen senden.</span><span class="sxs-lookup"><span data-stu-id="bc214-121">Upon receiving a **WM\_DDE\_INITIATE** request with the high-order word of the *lParam* parameter set to **NULL**, a server must send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each of the topics it supports.</span></span>

### <a name="sending"></a><span data-ttu-id="bc214-122">Senden</span><span class="sxs-lookup"><span data-stu-id="bc214-122">Sending</span></span>

<span data-ttu-id="bc214-123">Der Client sendet die Nachricht an alle Fenster der obersten Ebene, indem der erste Parameter von [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) auf **HWND- \_ Broadcast** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bc214-123">The client broadcasts the message to all top-level windows by setting the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="bc214-124">Wenn die Client Anwendung bereits das Fenster Handle des gewünschten Servers abgerufen hat, kann Sie **WM \_ DDE \_ initiieren** direkt an das Server Fenster senden, indem Sie das Fenster Handle des Servers als ersten Parameter von [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)übergibt.</span><span class="sxs-lookup"><span data-stu-id="bc214-124">If the client application has already obtained the window handle of the desired server, it can send **WM\_DDE\_INITIATE** directly to the server window by passing the server's window handle as the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span>

<span data-ttu-id="bc214-125">Die Client Anwendung ordnet Atome durch Aufrufen der [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) -Funktion zu.</span><span class="sxs-lookup"><span data-stu-id="bc214-125">The client application allocates atoms by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="bc214-126">Wenn [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) zurückgibt, muss die Client Anwendung die Atome löschen.</span><span class="sxs-lookup"><span data-stu-id="bc214-126">When [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application must delete the atoms.</span></span>

### <a name="receiving"></a><span data-ttu-id="bc214-127">Empfangen</span><span class="sxs-lookup"><span data-stu-id="bc214-127">Receiving</span></span>

<span data-ttu-id="bc214-128">Um die Initiierung einer Konversation abzuschließen, muss die Serveranwendung mit einer oder mehreren [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachrichten Antworten, wobei jede Nachricht für ein separates Thema gilt.</span><span class="sxs-lookup"><span data-stu-id="bc214-128">To complete the initiation of a conversation, the server application must respond with one or more [**WM\_DDE\_ACK**](wm-dde-ack.md) messages, where each message is for a separate topic.</span></span> <span data-ttu-id="bc214-129">Beim Senden der " **WM \_ DDE \_ ACK** "-Nachricht sollte der Server neue Atome erstellen, und die mit **WM \_ DDE \_ initiieren** gesendeten Atome sollten nicht wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc214-129">When sending **WM\_DDE\_ACK** message, the server should create new atoms; it should not reuse the atoms sent with **WM\_DDE\_INITIATE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc214-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc214-130">Requirements</span></span>



| <span data-ttu-id="bc214-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc214-131">Requirement</span></span> | <span data-ttu-id="bc214-132">Wert</span><span class="sxs-lookup"><span data-stu-id="bc214-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc214-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc214-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bc214-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc214-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bc214-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc214-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bc214-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc214-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bc214-137">Header</span><span class="sxs-lookup"><span data-stu-id="bc214-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc214-138"><dt>DDE. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc214-138"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc214-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc214-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc214-140">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="bc214-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bc214-141">**Globaladdatom**</span><span class="sxs-lookup"><span data-stu-id="bc214-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="bc214-142">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="bc214-142">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="bc214-143">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="bc214-143">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="bc214-144">**WM-DDE-Bestätigung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bc214-144">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="bc214-145">**Licher**</span><span class="sxs-lookup"><span data-stu-id="bc214-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bc214-146">Informationen zu dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="bc214-146">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

