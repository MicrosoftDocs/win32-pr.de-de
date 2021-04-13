---
title: WM_DDE_UNADVISE Meldung (DDE. h)
description: Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine "WM \_ DDE \_ unempfehlung"-Meldung, um eine DDE Server-Anwendung zu informieren, dass das angegebene Element oder ein bestimmtes Zwischenablage Format für das Element nicht mehr aktualisiert werden soll.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- WM_DDE_UNADVISE Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba83badcb689789d2654d99780bcb8cc503511d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478306"
---
# <a name="wm_dde_unadvise-message"></a><span data-ttu-id="2ab33-104">WM \_ DDE- \_ Meldung "nicht Empfehlung"</span><span class="sxs-lookup"><span data-stu-id="2ab33-104">WM\_DDE\_UNADVISE message</span></span>

<span data-ttu-id="2ab33-105">Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine " **WM \_ DDE \_ unempfehlung** "-Meldung, um eine DDE Server-Anwendung zu informieren, dass das angegebene Element oder ein bestimmtes Zwischenablage Format für das Element nicht mehr aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ab33-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_UNADVISE** message to inform a DDE server application that the specified item or a particular clipboard format for the item should no longer be updated.</span></span> <span data-ttu-id="2ab33-106">Dadurch wird der Daten Link warm oder Hot für das angegebene Element beendet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-106">This terminates the warm or hot data link for the specified item.</span></span>

<span data-ttu-id="2ab33-107">Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="2ab33-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a><span data-ttu-id="2ab33-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ab33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ab33-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ab33-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ab33-110">Ein Handle für das Client Fenster, das die Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="2ab33-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ab33-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ab33-112">Das nieder wertige Wort gibt das Zwischenablage Format des Elements an, für das die Aktualisierungs Anforderung zurückgezogen wird.</span><span class="sxs-lookup"><span data-stu-id="2ab33-112">The low-order word specifies the clipboard format of the item for which the update request is being retracted.</span></span> <span data-ttu-id="2ab33-113">Wenn dieser Wert **null** ist, werden alle aktiven [**WM- \_ DDE \_**](wm-dde-advise.md) -Konversationen für das Element beendet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-113">If this is **NULL**, all active [**WM\_DDE\_ADVISE**](wm-dde-advise.md) conversations for the item are to be terminated.</span></span>

<span data-ttu-id="2ab33-114">Das höchst wertige Wort enthält ein globales Atom, das das Element identifiziert, für das die Aktualisierungs Anforderung zurückgezogen wird.</span><span class="sxs-lookup"><span data-stu-id="2ab33-114">The high-order word contains a global atom that identifies the item for which the update request is being retracted.</span></span> <span data-ttu-id="2ab33-115">Wenn dieser Wert **null** ist, werden alle aktiven [**WM- \_ DDE \_**](wm-dde-advise.md) -Links, die der Konversation zugeordnet sind, beendet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-115">If this is **NULL**, all active [**WM\_DDE\_ADVISE**](wm-dde-advise.md) links associated with the conversation are to be terminated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ab33-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ab33-116">Remarks</span></span>

<span data-ttu-id="2ab33-117">Die Client Anwendung ordnet das hochwertige Wort *LPARAM* zu, indem die [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2ab33-117">The client application allocates the high-order word of *lParam* by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="2ab33-118">Die Serveranwendung sendet die " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) "-Nachricht, um positiv oder negativ zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="2ab33-118">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="2ab33-119">Beim Veröffentlichen der **WM- \_ DDE \_**-Bestätigung kann der Server entweder das Atom wieder verwenden oder das Atom löschen und ein neues erstellen.</span><span class="sxs-lookup"><span data-stu-id="2ab33-119">When posting **WM\_DDE\_ACK**, the server can either reuse the atom, or it can delete the atom and create a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ab33-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ab33-120">Requirements</span></span>



| <span data-ttu-id="2ab33-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ab33-121">Requirement</span></span> | <span data-ttu-id="2ab33-122">Wert</span><span class="sxs-lookup"><span data-stu-id="2ab33-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab33-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ab33-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2ab33-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ab33-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2ab33-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ab33-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2ab33-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ab33-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2ab33-127">Header</span><span class="sxs-lookup"><span data-stu-id="2ab33-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ab33-128"><dt>DDE. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ab33-128"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ab33-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ab33-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="2ab33-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="2ab33-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2ab33-131">**Globaladdatom**</span><span class="sxs-lookup"><span data-stu-id="2ab33-131">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="2ab33-132">**Packddelta param**</span><span class="sxs-lookup"><span data-stu-id="2ab33-132">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="2ab33-133">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="2ab33-133">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="2ab33-134">**Reuseddelta param**</span><span class="sxs-lookup"><span data-stu-id="2ab33-134">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="2ab33-135">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="2ab33-135">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="2ab33-136">**Unpackddelta param**</span><span class="sxs-lookup"><span data-stu-id="2ab33-136">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="2ab33-137">**WM-DDE-Bestätigung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ab33-137">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="2ab33-138">**WM \_ DDE- \_ Empfehlung**</span><span class="sxs-lookup"><span data-stu-id="2ab33-138">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

<span data-ttu-id="2ab33-139">**Licher**</span><span class="sxs-lookup"><span data-stu-id="2ab33-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2ab33-140">Informationen zu dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="2ab33-140">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

