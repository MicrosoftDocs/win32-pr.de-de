---
title: WM_DDE_POKE Meldung (DDE. h)
description: Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine WM- \_ DDE- \_ Poke-Nachricht an eine DDE-Serveranwendung.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- WM_DDE_POKE Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DDE_POKE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 001697cbd5328b9c8d9eb72ebddff5f86ef6381c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743696"
---
# <a name="wm_dde_poke-message"></a><span data-ttu-id="98e0f-104">WM- \_ DDE- \_ Poke-Nachricht</span><span class="sxs-lookup"><span data-stu-id="98e0f-104">WM\_DDE\_POKE message</span></span>

<span data-ttu-id="98e0f-105">Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine **WM- \_ DDE- \_ Poke** -Nachricht an eine DDE-Serveranwendung.</span><span class="sxs-lookup"><span data-stu-id="98e0f-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_POKE** message to a DDE server application.</span></span> <span data-ttu-id="98e0f-106">Ein Client verwendet diese Nachricht, um den Server aufzufordern, ein nicht angefordertes Datenelement zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="98e0f-106">A client uses this message to request the server to accept an unsolicited data item.</span></span> <span data-ttu-id="98e0f-107">Der Server antwortet mit einer [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung, die angibt, ob das Datenelement akzeptiert wurde.</span><span class="sxs-lookup"><span data-stu-id="98e0f-107">The server is expected to reply with a [**WM\_DDE\_ACK**](wm-dde-ack.md) message indicating whether it accepted the data item.</span></span>

<span data-ttu-id="98e0f-108">Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="98e0f-108">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a><span data-ttu-id="98e0f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="98e0f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e0f-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98e0f-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98e0f-111">Ein Handle für das Client Fenster, das die Meldung bereitstellen soll.</span><span class="sxs-lookup"><span data-stu-id="98e0f-111">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="98e0f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98e0f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98e0f-113">Das nieder wertige Wort ist ein Handle für ein globales Speicher Objekt, das eine [**DDEPoke**](/windows/desktop/api/Dde/ns-dde-ddepoke) -Struktur mit den Daten und zusätzlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="98e0f-113">The low-order word is a handle to a global memory object containing a [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) structure with the data and additional information.</span></span>

<span data-ttu-id="98e0f-114">Das höchst wertige Wort enthält ein globales Atom, das das Datenelement identifiziert, für das die Daten oder Benachrichtigungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="98e0f-114">The high-order word contains a global atom that identifies the data item for which the data or notification is being sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98e0f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98e0f-115">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="98e0f-116">Veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="98e0f-116">Posting</span></span>

<span data-ttu-id="98e0f-117">Die Client Anwendung muss Speicher für das globale Speicher Objekt mithilfe der [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) -Funktion zuweisen.</span><span class="sxs-lookup"><span data-stu-id="98e0f-117">The client application must allocate memory for the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="98e0f-118">Die Client Anwendung muss das-Objekt löschen, wenn eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="98e0f-118">The client application must delete the object if either of the following conditions is true:</span></span>

-   <span data-ttu-id="98e0f-119">Die Serveranwendung antwortet mit einer negativen [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung.</span><span class="sxs-lookup"><span data-stu-id="98e0f-119">The server application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>
-   <span data-ttu-id="98e0f-120">Der **frelease** -Member ist **false**, aber die Serveranwendung antwortet entweder mit einer positiven oder negativen [**WM- \_ DDE \_**](wm-dde-ack.md)-Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="98e0f-120">The **fRelease** member is **FALSE**, but the server application responds with either a positive or negative [**WM\_DDE\_ACK**](wm-dde-ack.md).</span></span>

<span data-ttu-id="98e0f-121">Die Client Anwendung muss das Atom mithilfe der [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) -Funktion erstellen.</span><span class="sxs-lookup"><span data-stu-id="98e0f-121">The client application must create the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="98e0f-122">Die Client Anwendung muss den **WM- \_ DDE \_ Poke** - *LPARAM* -Parameter durch Aufrufen der [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) -Funktion oder der [**reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) -Funktion erstellen oder wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="98e0f-122">The client application must create or reuse the **WM\_DDE\_POKE** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

### <a name="receiving"></a><span data-ttu-id="98e0f-123">Empfangen</span><span class="sxs-lookup"><span data-stu-id="98e0f-123">Receiving</span></span>

<span data-ttu-id="98e0f-124">Die Serveranwendung sollte die " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) "-Nachricht senden, um positiv oder negativ zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="98e0f-124">The server application should post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="98e0f-125">Beim Veröffentlichen der **WM- \_ DDE \_**-Bestätigung kann der Server entweder das Atom wieder verwenden oder es löschen und ein neues erstellen.</span><span class="sxs-lookup"><span data-stu-id="98e0f-125">When posting **WM\_DDE\_ACK**, the server can either reuse the atom, or it can delete it and create a new one.</span></span>

<span data-ttu-id="98e0f-126">Der Server muss den " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *LPARAM* "-Parameter durch Aufrufen der [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) -Funktion oder der [**reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) -Funktion erstellen oder wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="98e0f-126">The server must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="98e0f-127">Um das globale Speicher Objekt freizugeben, sollte der Server die [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="98e0f-127">To free the global memory object, the server should call the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="98e0f-128">Wenn das Datenformat entweder [**CF \_ dspmetafilepict**](clipboard-formats.md) oder **CF \_ MetafilePict** ist, muss der Server außerdem [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) mit dem eingebetteten metadateihandle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="98e0f-128">Also, if the data format is either [**CF\_DSPMETAFILEPICT**](clipboard-formats.md) or **CF\_METAFILEPICT**, the server must also call [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) with the embedded metafile handle.</span></span> <span data-ttu-id="98e0f-129">Diese beiden Formate haben eine zusätzliche Dereferenzierungsebene. Das heißt, eine Anwendung muss das Objekt Sperren, um einen Zeiger auf ein Handle zu erhalten, und dann das Handle sperren, um einen Zeiger auf eine [**MetafilePict**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) -Struktur zu erhalten, und schließlich **DeleteMetaFile** mit dem Handle aus dem **HMF** -Member der **MetafilePict** -Struktur aufrufen.</span><span class="sxs-lookup"><span data-stu-id="98e0f-129">These two formats have an extra level of indirection; that is, an application must lock the object to get a pointer to a handle, then lock that handle to get a pointer to a [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) structure, and finally call **DeleteMetaFile** with the handle from the **hMF** member of the **METAFILEPICT** structure.</span></span>

<span data-ttu-id="98e0f-130">Um das Objekt freizugeben, sollte der Server die Funktion " [**freeddelta param**](/windows/desktop/api/Dde/nf-dde-freeddelparam) " anrufen.</span><span class="sxs-lookup"><span data-stu-id="98e0f-130">To free the object, the server should call the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="98e0f-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98e0f-131">Requirements</span></span>



| <span data-ttu-id="98e0f-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98e0f-132">Requirement</span></span> | <span data-ttu-id="98e0f-133">Wert</span><span class="sxs-lookup"><span data-stu-id="98e0f-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98e0f-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98e0f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="98e0f-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98e0f-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="98e0f-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98e0f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="98e0f-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98e0f-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="98e0f-138">Header</span><span class="sxs-lookup"><span data-stu-id="98e0f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="98e0f-139"><dt>DDE. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98e0f-139"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e0f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98e0f-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="98e0f-141">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="98e0f-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="98e0f-142">**DDE Poke**</span><span class="sxs-lookup"><span data-stu-id="98e0f-142">**DDEPOKE**</span></span>](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[<span data-ttu-id="98e0f-143">**Freeddelta param**</span><span class="sxs-lookup"><span data-stu-id="98e0f-143">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="98e0f-144">**Globaladdatom**</span><span class="sxs-lookup"><span data-stu-id="98e0f-144">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="98e0f-145">**MetafilePict**</span><span class="sxs-lookup"><span data-stu-id="98e0f-145">**METAFILEPICT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-metafilepict)
</dt> <dt>

[<span data-ttu-id="98e0f-146">**Packddelta param**</span><span class="sxs-lookup"><span data-stu-id="98e0f-146">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="98e0f-147">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="98e0f-147">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="98e0f-148">**Reuseddelta param**</span><span class="sxs-lookup"><span data-stu-id="98e0f-148">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="98e0f-149">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="98e0f-149">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="98e0f-150">**Unpackddelta param**</span><span class="sxs-lookup"><span data-stu-id="98e0f-150">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="98e0f-151">**WM-DDE-Bestätigung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="98e0f-151">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="98e0f-152">**Licher**</span><span class="sxs-lookup"><span data-stu-id="98e0f-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="98e0f-153">Informationen zu dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="98e0f-153">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

