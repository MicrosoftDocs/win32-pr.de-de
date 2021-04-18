---
title: WM_DDE_DATA Meldung (DDE. h)
description: Eine DDE-Serveranwendung (dynamischer Datenaustausch) sendet eine WM- \_ DDE- \_ Daten Nachricht an eine DDE-Client Anwendung, um ein Datenelement an den Client zu übergeben oder den Client über die Verfügbarkeit eines Datenelements zu benachrichtigen.
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- WM_DDE_DATA Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DDE_DATA
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f045ff07e01023e6535eb00dcb78400e4c9519a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338535"
---
# <a name="wm_dde_data-message"></a><span data-ttu-id="38ae1-104">WM \_ DDE- \_ Daten Meldung</span><span class="sxs-lookup"><span data-stu-id="38ae1-104">WM\_DDE\_DATA message</span></span>

<span data-ttu-id="38ae1-105">Eine DDE-Serveranwendung (dynamischer Datenaustausch) sendet eine **WM- \_ DDE- \_ Daten** Nachricht an eine DDE-Client Anwendung, um ein Datenelement an den Client zu übergeben oder den Client über die Verfügbarkeit eines Datenelements zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="38ae1-105">A Dynamic Data Exchange (DDE) server application posts a **WM\_DDE\_DATA** message to a DDE client application to pass a data item to the client or to notify the client of the availability of a data item.</span></span>

<span data-ttu-id="38ae1-106">Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="38ae1-106">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_DATA        0x03E05
```



## <a name="parameters"></a><span data-ttu-id="38ae1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="38ae1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38ae1-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38ae1-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38ae1-109">Ein Handle für das Server Fenster, das die Meldung bereitstellen soll.</span><span class="sxs-lookup"><span data-stu-id="38ae1-109">A handle to the server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="38ae1-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38ae1-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38ae1-111">Das nieder wertige Wort ist ein Handle für ein globales Speicher Objekt, das eine [**ddedata**](/windows/desktop/api/Dde/ns-dde-ddedata) -Struktur mit den Daten und zusätzlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="38ae1-111">The low-order word is a handle to a global memory object containing a [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure with the data and additional information.</span></span> <span data-ttu-id="38ae1-112">Das Handle sollte auf **null** festgelegt werden, wenn der Server den Client darüber benachrichtigt, dass sich der Datenelement Wert während eines warm Daten Links geändert hat.</span><span class="sxs-lookup"><span data-stu-id="38ae1-112">The handle should be set to **NULL** if the server is notifying the client that the data-item value has changed during a warm data link.</span></span> <span data-ttu-id="38ae1-113">Ein warmer Link wird vom Client erstellt, der eine [**WM- \_ DDE \_**](wm-dde-advise.md) -Benachrichtigungs Meldung mit dem festgelegten " **f"-** Bit sendet.</span><span class="sxs-lookup"><span data-stu-id="38ae1-113">A warm link is established by the client sending a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message with the **fDeferUpd** bit set.</span></span>

<span data-ttu-id="38ae1-114">Das höchst wertige Wort enthält ein Atom, das das Datenelement identifiziert, für das die Daten oder Benachrichtigungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="38ae1-114">The high-order word contains an atom that identifies the data item for which the data or notification is sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38ae1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38ae1-115">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="38ae1-116">Veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="38ae1-116">Posting</span></span>

<span data-ttu-id="38ae1-117">Die Serveranwendung ordnet das globale Speicher Objekt mithilfe der [**globalbelegungsfunktion**](/windows/desktop/api/winbase/nf-winbase-globalalloc) zu.</span><span class="sxs-lookup"><span data-stu-id="38ae1-117">The server application allocates the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="38ae1-118">Das Atom wird mithilfe der [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) -Funktion zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="38ae1-118">It allocates the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="38ae1-119">Der Server muss den *LPARAM* -Parameter der **WM-DDE- \_ \_ Daten** durch Aufrufen der [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) -Funktion oder der [**reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) -Funktion erstellen oder wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="38ae1-119">The server must create or reuse the **WM\_DDE\_DATA** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="38ae1-120">Wenn die empfangende (Client-) Anwendung mit einer negativen [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung antwortet, muss die Posting (Server)-Anwendung das globale Speicher Objekt löschen. andernfalls muss der Client das Objekt löschen, nachdem der Inhalt durch Aufrufen der [**unpackddelta param**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) -Funktion extrahiert wurde.</span><span class="sxs-lookup"><span data-stu-id="38ae1-120">If the receiving (client) application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the posting (server) application must delete the global memory object; otherwise, the client must delete the object after extracting its contents by calling the [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) function.</span></span>

<span data-ttu-id="38ae1-121">Wenn die Serveranwendung den **frelease** -Member der [**DDE Data**](/windows/desktop/api/Dde/ns-dde-ddedata) -Struktur auf **false** festlegt, ist der Server dafür verantwortlich, das Objekt zu löschen, wenn eine positive oder negative Bestätigung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="38ae1-121">If the server application sets the **fRelease** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to **FALSE**, the server is responsible for deleting the object upon receiving either a positive or negative acknowledgment.</span></span>

<span data-ttu-id="38ae1-122">Die Serveranwendung sollte nicht sowohl die **fakkreq** -als auch die **frelease** -Member der [**DDE Data**](/windows/desktop/api/Dde/ns-dde-ddedata) -Struktur auf **false** festlegen.</span><span class="sxs-lookup"><span data-stu-id="38ae1-122">The server application should not set both the **fAckReq** and **fRelease** members of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to **FALSE**.</span></span> <span data-ttu-id="38ae1-123">Wenn beide Member auf **false** festgelegt sind, kann der Server nicht bestimmen, wann das Objekt gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="38ae1-123">If both members are set to **FALSE**, it is impossible for the server to determine when to delete the object.</span></span>

### <a name="receiving"></a><span data-ttu-id="38ae1-124">Empfangen</span><span class="sxs-lookup"><span data-stu-id="38ae1-124">Receiving</span></span>

<span data-ttu-id="38ae1-125">Wenn " **fakkreq** " den Wert " **true**" hat, sollte die Client Anwendung die " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) "-Nachricht bereitstellen, um positiv oder negativ</span><span class="sxs-lookup"><span data-stu-id="38ae1-125">If **fAckReq** is **TRUE**, the client application should post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="38ae1-126">Beim Veröffentlichen der **WM- \_ DDE \_**-Bestätigung kann der Client entweder das Atom wieder verwenden oder es löschen und ein neues erstellen.</span><span class="sxs-lookup"><span data-stu-id="38ae1-126">When posting **WM\_DDE\_ACK**, the client can either reuse the atom, or it can delete it and create a new one.</span></span>

<span data-ttu-id="38ae1-127">Der Client muss den Parameter " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *LPARAM* " durch Aufrufen der [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) -Funktion oder der [**reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) -Funktion erstellen oder wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="38ae1-127">The client must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="38ae1-128">Wenn " **fakkreq** " den Wert " **false**" hat, sollte die Client Anwendung das Atom löschen.</span><span class="sxs-lookup"><span data-stu-id="38ae1-128">If **fAckReq** is **FALSE**, the client application should delete the atom.</span></span>

<span data-ttu-id="38ae1-129">Wenn die Bereitstellung des globalen Speicher Objekts durch die Anwendungs Bereitstellung als **null** festgelegt wurde, kann die empfangende Anwendung den Server zum Senden der Daten anfordern, indem eine [**WM-DDE- \_ \_ Anforderungs**](wm-dde-request.md) Nachricht</span><span class="sxs-lookup"><span data-stu-id="38ae1-129">If the posting application specified global memory object as **NULL**, the receiving application can request the server to send the data by posting a [**WM\_DDE\_REQUEST**](wm-dde-request.md) message.</span></span>

<span data-ttu-id="38ae1-130">Nachdem eine **WM- \_ DDE- \_ Daten** Nachricht verarbeitet wurde, in der das globale Speicher Objekt nicht **null** ist, muss der Client das Objekt freigeben, es sei denn, eine der folgenden Bedingungen ist erfüllt:</span><span class="sxs-lookup"><span data-stu-id="38ae1-130">After processing a **WM\_DDE\_DATA** message in which the global memory object is not **NULL**, the client should free the object, unless one of the following conditions is true:</span></span>

-   <span data-ttu-id="38ae1-131">Der **frelease** -Member ist **false**.</span><span class="sxs-lookup"><span data-stu-id="38ae1-131">The **fRelease** member is **FALSE**.</span></span>
-   <span data-ttu-id="38ae1-132">Der **frelease** -Member ist **true**, aber die Client Anwendung antwortet mit einer negativen [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="38ae1-132">The **fRelease** member is **TRUE**, but the client application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="38ae1-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38ae1-133">Requirements</span></span>



| <span data-ttu-id="38ae1-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38ae1-134">Requirement</span></span> | <span data-ttu-id="38ae1-135">Wert</span><span class="sxs-lookup"><span data-stu-id="38ae1-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38ae1-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38ae1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="38ae1-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38ae1-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="38ae1-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38ae1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="38ae1-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38ae1-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="38ae1-140">Header</span><span class="sxs-lookup"><span data-stu-id="38ae1-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="38ae1-141"><dt>DDE. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38ae1-141"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38ae1-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38ae1-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="38ae1-143">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="38ae1-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="38ae1-144">**DDE-Daten**</span><span class="sxs-lookup"><span data-stu-id="38ae1-144">**DDEDATA**</span></span>](/windows/desktop/api/Dde/ns-dde-ddedata)
</dt> <dt>

[<span data-ttu-id="38ae1-145">**Freeddelta param**</span><span class="sxs-lookup"><span data-stu-id="38ae1-145">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="38ae1-146">**Globaladdatom**</span><span class="sxs-lookup"><span data-stu-id="38ae1-146">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="38ae1-147">**Packddelta param**</span><span class="sxs-lookup"><span data-stu-id="38ae1-147">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="38ae1-148">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="38ae1-148">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="38ae1-149">**Reuseddelta param**</span><span class="sxs-lookup"><span data-stu-id="38ae1-149">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="38ae1-150">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="38ae1-150">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="38ae1-151">**Unpackddelta param**</span><span class="sxs-lookup"><span data-stu-id="38ae1-151">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="38ae1-152">**WM-DDE-Bestätigung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="38ae1-152">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="38ae1-153">**WM \_ DDE- \_ Empfehlung**</span><span class="sxs-lookup"><span data-stu-id="38ae1-153">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

[<span data-ttu-id="38ae1-154">**WM \_ DDE \_ Poke**</span><span class="sxs-lookup"><span data-stu-id="38ae1-154">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="38ae1-155">**WM- \_ DDE- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="38ae1-155">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

<span data-ttu-id="38ae1-156">**Licher**</span><span class="sxs-lookup"><span data-stu-id="38ae1-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="38ae1-157">Informationen zu dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="38ae1-157">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

