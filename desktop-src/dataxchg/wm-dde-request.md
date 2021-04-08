---
title: WM_DDE_REQUEST Meldung (DDE. h)
description: Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine WM- \_ DDE- \_ Anforderungs Nachricht an eine DDE-Serveranwendung, um den Wert eines Datenelements anzufordern. Um diese Nachricht zu veröffentlichen, wenden Sie die PostMessage-Funktion mit den folgenden Parametern an.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- WM_DDE_REQUEST Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DDE_REQUEST
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7d5eab75d3b7298d78547b17fccfb164a47ae4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741088"
---
# <a name="wm_dde_request-message"></a><span data-ttu-id="c3b4e-105">WM- \_ DDE- \_ Anforderungs Nachricht</span><span class="sxs-lookup"><span data-stu-id="c3b4e-105">WM\_DDE\_REQUEST message</span></span>

<span data-ttu-id="c3b4e-106">Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine **WM- \_ DDE- \_ Anforderungs** Nachricht an eine DDE-Serveranwendung, um den Wert eines Datenelements anzufordern.</span><span class="sxs-lookup"><span data-stu-id="c3b4e-106">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_REQUEST** message to a DDE server application to request the value of a data item.</span></span>

<span data-ttu-id="c3b4e-107">Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="c3b4e-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a><span data-ttu-id="c3b4e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3b4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3b4e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3b4e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3b4e-110">Ein Handle für das Client Fenster, das die Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="c3b4e-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="c3b4e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3b4e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3b4e-112">Das nieder wertige Wort gibt ein Standardmäßiges oder registriertes Zwischenablage Format an.</span><span class="sxs-lookup"><span data-stu-id="c3b4e-112">The low-order word specifies a standard or registered clipboard format.</span></span>

<span data-ttu-id="c3b4e-113">Das höchst wertige Wort enthält ein Atom, das das vom Server angeforderte Datenelement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c3b4e-113">The high-order word contains an atom that identifies the data item requested from the server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3b4e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3b4e-114">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="c3b4e-115">Veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="c3b4e-115">Posting</span></span>

<span data-ttu-id="c3b4e-116">Die Client Anwendung ordnet das Atom durch Aufrufen der [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) -Funktion zu.</span><span class="sxs-lookup"><span data-stu-id="c3b4e-116">The client application allocates the atom by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

### <a name="receiving"></a><span data-ttu-id="c3b4e-117">Empfangen</span><span class="sxs-lookup"><span data-stu-id="c3b4e-117">Receiving</span></span>

<span data-ttu-id="c3b4e-118">Wenn die empfangende Anwendung (Server) die Anforderung erfüllen kann, antwortet sie mit einer [**WM- \_ DDE- \_ Daten**](wm-dde-data.md) Nachricht, die die angeforderten Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="c3b4e-118">If the receiving (server) application can satisfy the request, it responds with a [**WM\_DDE\_DATA**](wm-dde-data.md) message containing the requested data.</span></span> <span data-ttu-id="c3b4e-119">Andernfalls antwortet er mit einer negativen [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung.</span><span class="sxs-lookup"><span data-stu-id="c3b4e-119">Otherwise, it responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="c3b4e-120">Bei der Reaktion entweder der [**WM- \_ DDE- \_ Daten**](wm-dde-data.md) oder der [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung kann die Serveranwendung entweder das Atom wieder verwenden oder das Atom löschen und ein neues erstellen.</span><span class="sxs-lookup"><span data-stu-id="c3b4e-120">When responding with either a [**WM\_DDE\_DATA**](wm-dde-data.md) or [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the server application can either reuse the atom or it can delete the atom and create a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3b4e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3b4e-121">Requirements</span></span>



| <span data-ttu-id="c3b4e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3b4e-122">Requirement</span></span> | <span data-ttu-id="c3b4e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c3b4e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3b4e-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3b4e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c3b4e-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3b4e-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c3b4e-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3b4e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c3b4e-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3b4e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c3b4e-128">Header</span><span class="sxs-lookup"><span data-stu-id="c3b4e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3b4e-129"><dt>DDE. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3b4e-129"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3b4e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3b4e-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="c3b4e-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c3b4e-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c3b4e-132">**Globaladdatom**</span><span class="sxs-lookup"><span data-stu-id="c3b4e-132">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="c3b4e-133">**Packddelta param**</span><span class="sxs-lookup"><span data-stu-id="c3b4e-133">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="c3b4e-134">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="c3b4e-134">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="c3b4e-135">**Reuseddelta param**</span><span class="sxs-lookup"><span data-stu-id="c3b4e-135">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="c3b4e-136">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="c3b4e-136">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="c3b4e-137">**Unpackddelta param**</span><span class="sxs-lookup"><span data-stu-id="c3b4e-137">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="c3b4e-138">**WM-DDE-Bestätigung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c3b4e-138">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="c3b4e-139">**WM- \_ DDE- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="c3b4e-139">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

<span data-ttu-id="c3b4e-140">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c3b4e-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c3b4e-141">Informationen zu dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="c3b4e-141">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

