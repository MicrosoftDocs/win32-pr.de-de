---
title: WM_DDE_TERMINATE Meldung (DDE. h)
description: Eine dynamischer Datenaustausch (DDE)-Anwendung (Client oder Server) sendet eine WM-DDE-Beendigungs \_ \_ Nachricht, um eine Konversation zu beenden. Um diese Nachricht zu veröffentlichen, wenden Sie die PostMessage-Funktion mit den folgenden Parametern an.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- WM_DDE_TERMINATE Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DDE_TERMINATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 105b4a7daab87b1311a58a7b5e5805bbd81e73ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103414"
---
# <a name="wm_dde_terminate-message"></a><span data-ttu-id="f9687-105">WM- \_ DDE- \_ Nachricht beenden</span><span class="sxs-lookup"><span data-stu-id="f9687-105">WM\_DDE\_TERMINATE message</span></span>

<span data-ttu-id="f9687-106">Eine dynamischer Datenaustausch (DDE)-Anwendung (Client oder Server) sendet eine **WM-DDE-Beendigungs \_ \_** Nachricht, um eine Konversation zu beenden.</span><span class="sxs-lookup"><span data-stu-id="f9687-106">A Dynamic Data Exchange (DDE) application (client or server) posts a **WM\_DDE\_TERMINATE** message to terminate a conversation.</span></span>

<span data-ttu-id="f9687-107">Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="f9687-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a><span data-ttu-id="f9687-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9687-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9687-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9687-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9687-110">Ein Handle für das Client-oder Server Fenster, das die Meldung bereitstellen soll.</span><span class="sxs-lookup"><span data-stu-id="f9687-110">A handle to the client or server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="f9687-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9687-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9687-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9687-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9687-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9687-113">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="f9687-114">Veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="f9687-114">Posting</span></span>

<span data-ttu-id="f9687-115">Beim Warten auf die Bestätigung der Beendigung sollte die Posting-Anwendung keine weiteren Nachrichten an die empfangende Anwendung senden.</span><span class="sxs-lookup"><span data-stu-id="f9687-115">While waiting for confirmation of the termination, the posting application should not post any other messages to the receiving application.</span></span> <span data-ttu-id="f9687-116">Wenn die sendende Anwendung Nachrichten (mit Ausnahme von **WM \_ DDE \_ Beenden**) von der empfangenden Anwendung empfängt, sollten alle Atome oder gemeinsam genutzten Speicher Objekte, die den Nachrichten angehören, gelöscht werden, mit Ausnahme der globalen Speicher Objekte, die mit [**WM \_ DDE \_ Poke**](wm-dde-poke.md) -oder [**WM \_ DDE- \_ Daten**](wm-dde-data.md) Nachrichten verknüpft sind, für die das **frelease** -Element</span><span class="sxs-lookup"><span data-stu-id="f9687-116">If the sending application receives messages (other than **WM\_DDE\_TERMINATE**) from the receiving application, it should delete any atoms or shared memory objects accompanying the messages, except global memory objects associated with [**WM\_DDE\_POKE**](wm-dde-poke.md) or [**WM\_DDE\_DATA**](wm-dde-data.md) messages that do not have the **fRelease** member set.</span></span>

### <a name="receiving"></a><span data-ttu-id="f9687-117">Empfangen</span><span class="sxs-lookup"><span data-stu-id="f9687-117">Receiving</span></span>

<span data-ttu-id="f9687-118">Die Client-oder Serveranwendung sollte Antworten, indem Sie eine Abbruch Meldung vom Typ " **WM \_ DDE \_** " veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="f9687-118">The client or server application should respond by posting a **WM\_DDE\_TERMINATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9687-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9687-119">Requirements</span></span>



| <span data-ttu-id="f9687-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9687-120">Requirement</span></span> | <span data-ttu-id="f9687-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f9687-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9687-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9687-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f9687-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9687-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f9687-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9687-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f9687-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9687-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f9687-126">Header</span><span class="sxs-lookup"><span data-stu-id="f9687-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9687-127"><dt>DDE. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9687-127"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9687-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9687-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="f9687-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f9687-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f9687-130">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="f9687-130">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="f9687-131">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="f9687-131">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="f9687-132">**WM- \_ DDE- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="f9687-132">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="f9687-133">**WM \_ DDE \_ Poke**</span><span class="sxs-lookup"><span data-stu-id="f9687-133">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

<span data-ttu-id="f9687-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="f9687-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f9687-135">Informationen zu dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="f9687-135">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

