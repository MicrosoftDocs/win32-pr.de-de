---
title: WM_DDE_EXECUTE Meldung (DDE. h)
description: Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine WM- \_ DDE- \_ Ausführungs Nachricht an eine DDE-Serveranwendung, um eine Zeichenfolge an den Server zu senden, die als eine Reihe von Befehlen verarbeitet werden soll.
ms.assetid: 23c18a57-83ee-4fd3-a5bc-71645bda34eb
keywords:
- WM_DDE_EXECUTE Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DDE_EXECUTE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957b5cadcd2383d535aa67258725bafff57ab4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391975"
---
# <a name="wm_dde_execute-message"></a><span data-ttu-id="a8db2-104">WM- \_ DDE- \_ Ausführungs Meldung</span><span class="sxs-lookup"><span data-stu-id="a8db2-104">WM\_DDE\_EXECUTE message</span></span>

<span data-ttu-id="a8db2-105">Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine **WM- \_ DDE- \_ Ausführungs** Nachricht an eine DDE-Serveranwendung, um eine Zeichenfolge an den Server zu senden, die als eine Reihe von Befehlen verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8db2-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_EXECUTE** message to a DDE server application to send a string to the server to be processed as a series of commands.</span></span> <span data-ttu-id="a8db2-106">Die Serveranwendung sendet eine [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht als Antwort.</span><span class="sxs-lookup"><span data-stu-id="a8db2-106">The server application is expected to post a [**WM\_DDE\_ACK**](wm-dde-ack.md) message in response.</span></span>

<span data-ttu-id="a8db2-107">Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="a8db2-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_EXECUTE     0x03E8
```



## <a name="parameters"></a><span data-ttu-id="a8db2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8db2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8db2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8db2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8db2-110">Ein Handle für das Client Fenster, das die Meldung bereitstellen soll.</span><span class="sxs-lookup"><span data-stu-id="a8db2-110">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="a8db2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8db2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8db2-112">Enthält ein globales Speicher Objekt, das auf eine ANSI-oder Unicode-Befehls Zeichenfolge verweist, abhängig von den in der Konversation beteiligten Windows-Typen.</span><span class="sxs-lookup"><span data-stu-id="a8db2-112">Contains a global memory object that references an ANSI or Unicode command string, depending on the types of windows involved in the conversation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8db2-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8db2-113">Remarks</span></span>

<span data-ttu-id="a8db2-114">Die Befehls Zeichenfolge ist eine auf NULL endenden Zeichenfolge, die aus einer oder mehreren in Klammern eingeschlossenen Opcode-Zeichen folgen besteht \[ \] .</span><span class="sxs-lookup"><span data-stu-id="a8db2-114">The command string is a null-terminated string consisting of one or more opcode strings enclosed in single brackets (\[ \]).</span></span> <span data-ttu-id="a8db2-115">Jede Opcode-Zeichenfolge weist die folgende Syntax auf, wobei die *Parameter* Liste optional ist:</span><span class="sxs-lookup"><span data-stu-id="a8db2-115">Each opcode string has the following syntax, where the *parameters* list is optional:</span></span>

<span data-ttu-id="a8db2-116">*Opcode-Parameter*</span><span class="sxs-lookup"><span data-stu-id="a8db2-116">*opcode parameters*</span></span>

<span data-ttu-id="a8db2-117">Der *Opcode* ist ein beliebiges von der Anwendung definiertes einzelnes Token.</span><span class="sxs-lookup"><span data-stu-id="a8db2-117">The *opcode* is any application-defined single token.</span></span> <span data-ttu-id="a8db2-118">Es darf keine Leerzeichen, Kommas, Klammern, eckige Klammern oder Anführungszeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a8db2-118">It cannot include spaces, commas, parentheses, brackets, or quotation marks.</span></span>

<span data-ttu-id="a8db2-119">Die *Parameter* Liste kann beliebige Anwendungs definierte Werte oder Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="a8db2-119">The *parameters* list can contain any application-defined value or values.</span></span> <span data-ttu-id="a8db2-120">Mehrere Parameter werden durch Kommas getrennt, und die gesamte Parameterliste wird in Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a8db2-120">Multiple parameters are separated by commas, and the entire parameter list is enclosed in parentheses.</span></span> <span data-ttu-id="a8db2-121">Parameter dürfen keine Kommas oder Klammern enthalten, außer innerhalb einer Zeichenfolge in Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="a8db2-121">Parameters cannot include commas or parentheses except inside a quoted string.</span></span> <span data-ttu-id="a8db2-122">Wenn eine eckige Klammer oder ein Klammer Zeichen in einer Zeichenfolge in Anführungszeichen eingeschlossen werden soll, muss Sie nicht verdoppelt werden, wie es bei den alten Regeln der Fall war.</span><span class="sxs-lookup"><span data-stu-id="a8db2-122">If a bracket or parenthesis character is to appear in a quoted string, it need not be doubled, as was the case under the old rules.</span></span>

<span data-ttu-id="a8db2-123">Folgende Befehls Zeichenfolgen sind gültig:</span><span class="sxs-lookup"><span data-stu-id="a8db2-123">The following are valid command strings:</span></span>


```
[connect][download(query1,results.txt)][disconnect] 
[query("sales per employee for each district")] 
[open("sample.xlm")][run("r1c1")] 
[quote_case("This is a "" character")] 
[bracket_or_paren_case("()s or []s should be no problem.")] 
```



<span data-ttu-id="a8db2-124">Beachten Sie, dass unter den alten Regeln Klammern und eckige Klammern wie folgt verdoppelt werden mussten:</span><span class="sxs-lookup"><span data-stu-id="a8db2-124">Note that, under the old rules, parentheses and brackets had to be doubled, as follows:</span></span>


```
[bracket_or_paren_case("(())s or [[]]s should be no problem.")] 
```



<span data-ttu-id="a8db2-125">Server sollten in der Lage sein, Befehle in beiden Form zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="a8db2-125">Servers should be able to parse commands in either form.</span></span>

<span data-ttu-id="a8db2-126">Unicode-Execute-Zeichen folgen sollten nur verwendet werden, wenn sowohl die Client-als auch die Server Fenster Handles bewirken, dass die [**iswindowunicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) -Funktion **true** zurückgibt</span><span class="sxs-lookup"><span data-stu-id="a8db2-126">Unicode execute strings should be used only when both the client and server window handles cause the [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) function to return **TRUE**.</span></span>

### <a name="posting"></a><span data-ttu-id="a8db2-127">Veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="a8db2-127">Posting</span></span>

<span data-ttu-id="a8db2-128">Die Client Anwendung ordnet das globale Speicher Objekt zu, indem Sie [](/windows/desktop/api/winbase/nf-winbase-globalalloc) die globalbelegungsfunktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a8db2-128">The client application allocates the global memory object by calling the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span>

<span data-ttu-id="a8db2-129">Bei der Verarbeitung der [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht, die der Server in Antwort auf eine **WM-DDE- \_ \_ Execute** -Nachricht sendet, muss die Client Anwendung das von der **WM \_ DDE \_ ACK** -Nachricht zurückgegebene Objekt löschen.</span><span class="sxs-lookup"><span data-stu-id="a8db2-129">When processing the [**WM\_DDE\_ACK**](wm-dde-ack.md) message that the server posts in reply to a **WM\_DDE\_EXECUTE** message, the client application must delete the object returned by the **WM\_DDE\_ACK** message.</span></span>

### <a name="receiving"></a><span data-ttu-id="a8db2-130">Empfangen</span><span class="sxs-lookup"><span data-stu-id="a8db2-130">Receiving</span></span>

<span data-ttu-id="a8db2-131">Die Serveranwendung sendet die " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) "-Nachricht, um positiv oder negativ zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="a8db2-131">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="a8db2-132">Der Server sollte das globale Speicher Objekt wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="a8db2-132">The server should reuse the global memory object.</span></span>

<span data-ttu-id="a8db2-133">Sofern nicht anders durch ein unter Protokoll angegeben, sollte der Server erst dann die [**WM \_ DDE \_ ACK**](wm-dde-ack.md) -Nachricht veröffentlichen, wenn alle durch die Execute-Befehls Zeichenfolge angegebenen Aktionen abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="a8db2-133">Unless specified otherwise by a sub-protocol, the server should not post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message until all the actions specified by the execute command string are completed.</span></span> <span data-ttu-id="a8db2-134">Die einzige Ausnahme von dieser Regel ist, wenn die Zeichenfolge bewirkt, dass der Server die Konversation beendet.</span><span class="sxs-lookup"><span data-stu-id="a8db2-134">The one exception to this rule is when the string causes the server to terminate the conversation.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8db2-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8db2-135">Requirements</span></span>



| <span data-ttu-id="a8db2-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8db2-136">Requirement</span></span> | <span data-ttu-id="a8db2-137">Wert</span><span class="sxs-lookup"><span data-stu-id="a8db2-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8db2-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8db2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a8db2-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8db2-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a8db2-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8db2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a8db2-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8db2-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a8db2-142">Header</span><span class="sxs-lookup"><span data-stu-id="a8db2-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8db2-143"><dt>DDE. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8db2-143"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8db2-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8db2-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="a8db2-145">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a8db2-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a8db2-146">**Iswindowunicode**</span><span class="sxs-lookup"><span data-stu-id="a8db2-146">**IsWindowUnicode**</span></span>](/windows/desktop/api/winuser/nf-winuser-iswindowunicode)
</dt> <dt>

[<span data-ttu-id="a8db2-147">**Packddelta param**</span><span class="sxs-lookup"><span data-stu-id="a8db2-147">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="a8db2-148">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="a8db2-148">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="a8db2-149">**Reuseddelta param**</span><span class="sxs-lookup"><span data-stu-id="a8db2-149">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="a8db2-150">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="a8db2-150">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="a8db2-151">**Unpackddelta param**</span><span class="sxs-lookup"><span data-stu-id="a8db2-151">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="a8db2-152">**WM-DDE-Bestätigung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8db2-152">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="a8db2-153">**Licher**</span><span class="sxs-lookup"><span data-stu-id="a8db2-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a8db2-154">Informationen zu dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="a8db2-154">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

