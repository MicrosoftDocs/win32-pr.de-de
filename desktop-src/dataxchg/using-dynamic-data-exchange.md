---
title: Verwenden von dynamischer Datenaustausch
description: Dieses Thema enthält Codebeispiele zum dynamischen Datenaustausch.
ms.assetid: 6d94403b-64b4-4763-868a-3b94431dab79
keywords:
- Dynamischer Datenaustausch (DDE), Konversationen
- DDE (dynamischer Datenaustausch), Konversationen
- Datenaustausch, dynamischer Datenaustausch (DDE)
- Dynamischer Datenaustausch (DDE), Beispiele
- DDE (dynamischer Datenaustausch), Beispiele
- Dynamischer Datenaustausch (DDE), Befehle in Server Anwendungen
- DDE (dynamischer Datenaustausch), Befehle in Server Anwendungen
- Dynamischer Datenaustausch (DDE), Daten Verknüpfungen
- DDE (dynamischer Datenaustausch), Daten Verknüpfungen
- Dynamischer Datenaustausch (DDE), Elemente
- DDE (dynamischer Datenaustausch), Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe20c4dedc38303fe9bcb9c4b0fae42d03ee536
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315464"
---
# <a name="using-dynamic-data-exchange"></a><span data-ttu-id="e913e-114">Verwenden von dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="e913e-114">Using Dynamic Data Exchange</span></span>

<span data-ttu-id="e913e-115">Dieser Abschnitt enthält Codebeispiele zu den folgenden Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="e913e-115">This section has code samples on the following tasks:</span></span>

-   [<span data-ttu-id="e913e-116">Initiieren einer Konversation</span><span class="sxs-lookup"><span data-stu-id="e913e-116">Initiating a Conversation</span></span>](#initiating-a-conversation)
-   [<span data-ttu-id="e913e-117">Übertragen eines einzelnen Elements</span><span class="sxs-lookup"><span data-stu-id="e913e-117">Transferring a Single Item</span></span>](#transferring-a-single-item)
    -   [<span data-ttu-id="e913e-118">Abrufen eines Elements vom Server</span><span class="sxs-lookup"><span data-stu-id="e913e-118">Retrieving an Item from the Server</span></span>](#retrieving-an-item-from-the-server)
    -   [<span data-ttu-id="e913e-119">Ein Element wird an den Server übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e913e-119">Submitting an Item to the Server</span></span>](#submitting-an-item-to-the-server)
-   [<span data-ttu-id="e913e-120">Einrichten einer permanenten Datenverknüpfung</span><span class="sxs-lookup"><span data-stu-id="e913e-120">Establishing a Permanent Data Link</span></span>](#establishing-a-permanent-data-link)
    -   [<span data-ttu-id="e913e-121">Initiieren einer Datenverknüpfung</span><span class="sxs-lookup"><span data-stu-id="e913e-121">Initiating a Data Link</span></span>](#initiating-a-data-link)
    -   [<span data-ttu-id="e913e-122">Initiieren einer Datenverknüpfung mit dem Befehl "Link einfügen"</span><span class="sxs-lookup"><span data-stu-id="e913e-122">Initiating a Data Link with the Paste Link Command</span></span>](#initiating-a-data-link-with-the-paste-link-command)
    -   [<span data-ttu-id="e913e-123">Benachrichtigen des Clients, dass sich Daten geändert haben</span><span class="sxs-lookup"><span data-stu-id="e913e-123">Notifying the Client that Data Has Changed</span></span>](#notifying-the-client-that-data-has-changed)
    -   [<span data-ttu-id="e913e-124">Beenden eines Daten Links</span><span class="sxs-lookup"><span data-stu-id="e913e-124">Terminating a Data Link</span></span>](#terminating-a-data-link)
-   [<span data-ttu-id="e913e-125">Ausführen von Befehlen in einer Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="e913e-125">Carrying Out Commands in a Server Application</span></span>](#carrying-out-commands-in-a-server-application)
-   [<span data-ttu-id="e913e-126">Beenden einer Konversation</span><span class="sxs-lookup"><span data-stu-id="e913e-126">Terminating a Conversation</span></span>](#terminating-a-conversation)

## <a name="initiating-a-conversation"></a><span data-ttu-id="e913e-127">Initiieren einer Konversation</span><span class="sxs-lookup"><span data-stu-id="e913e-127">Initiating a Conversation</span></span>

<span data-ttu-id="e913e-128">Zum Initiieren einer dynamischer Datenaustausch (DDE)-Konversation sendet der Client eine " [**WM DDE"- \_ \_ Initiierungs**](wm-dde-initiate.md) Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e913e-128">To initiate a Dynamic Data Exchange (DDE) conversation, the client sends a [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message.</span></span> <span data-ttu-id="e913e-129">Normalerweise überträgt der Client diese Nachricht, indem [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)aufgerufen wird, wobei – 1 als erster Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-129">Usually, the client broadcasts this message by calling [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), with –1 as the first parameter.</span></span> <span data-ttu-id="e913e-130">Wenn die Anwendung bereits über das Fenster Handle für die Serveranwendung verfügt, kann Sie die Nachricht direkt an dieses Fenster senden.</span><span class="sxs-lookup"><span data-stu-id="e913e-130">If the application already has the window handle to the server application, it can send the message directly to that window.</span></span> <span data-ttu-id="e913e-131">Der Client bereitet Atome für den Anwendungsnamen und den Themen Namen vor, indem [**Global addatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-131">The client prepares atoms for the application name and topic name by calling [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma).</span></span> <span data-ttu-id="e913e-132">Der Client kann Konversationen mit jeder potenziellen Serveranwendung und für jedes beliebige mögliche Thema anfordern, indem er **null** -(Platzhalter) Atome für die Anwendung und das Thema bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e913e-132">The client can request conversations with any potential server application and for any potential topic by supplying **NULL** (wildcard) atoms for the application and topic.</span></span>

<span data-ttu-id="e913e-133">Im folgenden Beispiel wird veranschaulicht, wie der Client eine Konversation initiiert, wobei sowohl die Anwendung als auch das Thema angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e913e-133">The following example illustrates how the client initiates a conversation, where both the application and topic are specified.</span></span>


```
    static BOOL fInInitiate = FALSE; 
    char *szApplication; 
    char *szTopic; 
    atomApplication = *szApplication == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szApplication); 
    atomTopic = *szTopic == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szTopic); 
 
    fInInitiate = TRUE; 
    SendMessage((HWND) HWND_BROADCAST, // broadcasts message 
        WM_DDE_INITIATE,               // initiates conversation 
        (WPARAM) hwndClientDDE,        // handle to client DDE window 
        MAKELONG(atomApplication,      // application-name atom 
            atomTopic));               // topic-name atom 
    fInInitiate = FALSE; 
    if (atomApplication != NULL) 
        GlobalDeleteAtom(atomApplication); 
    if (atomTopic != NULL) 
        GlobalDeleteAtom(atomTopic);
```



> [!Note]  
> <span data-ttu-id="e913e-134">Wenn Ihre Anwendung **null** -Atome verwendet, müssen Sie nicht die Funktionen [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) und [**globaldeleteatom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) verwenden.</span><span class="sxs-lookup"><span data-stu-id="e913e-134">If your application uses **NULL** atoms, you need not use the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) and [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) functions.</span></span> <span data-ttu-id="e913e-135">In diesem Beispiel erstellt die Client Anwendung zwei globale Atome, die den Namen des Servers und den Namen des Themas enthalten.</span><span class="sxs-lookup"><span data-stu-id="e913e-135">In this example, the client application creates two global atoms containing the name of the server and the name of the topic, respectively.</span></span>

 

<span data-ttu-id="e913e-136">Die Client Anwendung sendet eine [**WM- \_ DDE- \_ Initiierungs**](wm-dde-initiate.md) Nachricht mit diesen beiden Atomen im *LPARAM* -Parameter der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e913e-136">The client application sends a [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message with these two atoms in the *lParam* parameter of the message.</span></span> <span data-ttu-id="e913e-137">Beim Abrufen der [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion weist das besondere Fenster Handle – 1 das System an, diese Nachricht an alle anderen aktiven Anwendungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="e913e-137">In the call to the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function, the special window handle –1 directs the system to send this message to all other active applications.</span></span> <span data-ttu-id="e913e-138">**SendMessage** kehrt nicht an die Client Anwendung zurück, bis alle Anwendungen, die die Nachricht empfangen, wiederum die Steuerung an das System zurückgegeben haben.</span><span class="sxs-lookup"><span data-stu-id="e913e-138">**SendMessage** does not return to the client application until all applications that receive the message have, in turn, returned control to the system.</span></span> <span data-ttu-id="e913e-139">Dies bedeutet, dass alle von den Server Anwendungen gesendeten [**WM- \_ DDE- \_ ACK**](wm-dde-ack.md) -Nachrichten vom Client bis zu dem Zeitpunkt verarbeitet wurden, an dem der **SendMessage** -Aufruf zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e913e-139">This means that all [**WM\_DDE\_ACK**](wm-dde-ack.md) messages sent in reply by the server applications are guaranteed to have been processed by the client by the time the **SendMessage** call has returned.</span></span>

<span data-ttu-id="e913e-140">Nachdem [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) zurückgegeben wurde, löscht die Client Anwendung die globalen Atome.</span><span class="sxs-lookup"><span data-stu-id="e913e-140">After [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application deletes the global atoms.</span></span>

<span data-ttu-id="e913e-141">Server Anwendungen reagieren gemäß der im folgenden Diagramm dargestellten Logik.</span><span class="sxs-lookup"><span data-stu-id="e913e-141">Server applications respond according to the logic illustrated in the following diagram.</span></span>

![Antwort Logik der Serveranwendung](images/csdde-01.png)

<span data-ttu-id="e913e-143">Um ein oder mehrere Themen zu bestätigen, muss der Server Atome für jede Konversation erstellen (erfordert doppelte Anwendungsnamen Atome, wenn mehrere Themen vorhanden sind) und eine [**WM \_ DDE \_ ACK**](wm-dde-ack.md) -Nachricht für jede Konversation senden, wie im folgenden Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e913e-143">To acknowledge one or more topics, the server must create atoms for each conversation (requiring duplicate application-name atoms if there are multiple topics) and send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each conversation, as illustrated in the following example.</span></span>


```
if ((atomApplication = GlobalAddAtom("Server")) != 0) 
{ 
    if ((atomTopic = GlobalAddAtom(szTopic)) != 0) 
    { 
        SendMessage(hwndClientDDE, 
            WM_DDE_ACK, 
            (WPARAM) hwndServerDDE, 
            MAKELONG(atomApplication, atomTopic)); 
        GlobalDeleteAtom(atomApplication); 
    } 
 
    GlobalDeleteAtom(atomTopic); 
} 
 
if ((atomApplication == 0) || (atomTopic == 0)) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="e913e-144">Wenn ein Server mit der Meldung " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) " antwortet, sollte die Client Anwendung ein Handle im Server Fenster speichern.</span><span class="sxs-lookup"><span data-stu-id="e913e-144">When a server responds with a [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the client application should save a handle to the server window.</span></span> <span data-ttu-id="e913e-145">Der Client, der das Handle als *wParam* -Parameter der **WM \_ DDE \_ ACK** -Nachricht empfängt, sendet dann alle nachfolgenden DDE-Nachrichten an das Server Fenster, das von diesem Handle identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-145">The client receiving the handle as the *wParam* parameter of the **WM\_DDE\_ACK** message then sends all subsequent DDE messages to the server window this handle identifies.</span></span>

<span data-ttu-id="e913e-146">Wenn Ihre Client Anwendung ein **null** -Atom für den Anwendungsnamen oder den Themen Namen verwendet, erwarten Sie, dass die Anwendung Bestätigungen von mehr als einer Serveranwendung empfängt.</span><span class="sxs-lookup"><span data-stu-id="e913e-146">If your client application uses a **NULL** atom for the application name or topic name, expect the application to receive acknowledgments from more than one server application.</span></span> <span data-ttu-id="e913e-147">Mehrere Bestätigungen können auch von mehreren Instanzen eines DDE-Servers stammen, auch wenn Ihre Client Anwendung keine **Atome verwendet.**</span><span class="sxs-lookup"><span data-stu-id="e913e-147">Multiple acknowledgements can also come from multiple instances of a DDE server, even if your client application does not **NULL** use atoms.</span></span> <span data-ttu-id="e913e-148">Ein Server sollte für jede Konversation immer ein eindeutiges Fenster verwenden.</span><span class="sxs-lookup"><span data-stu-id="e913e-148">A server should always use a unique window for each conversation.</span></span> <span data-ttu-id="e913e-149">Die Fenster Prozedur in der Client Anwendung kann ein Handle für das Server Fenster (bereitgestellt als *LPARAM* -Parameter von [**WM \_ DDE \_ initiieren**](wm-dde-initiate.md)) verwenden, um mehrere Konversationen zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="e913e-149">The window procedure in the client application can use a handle to the server window (provided as the *lParam* parameter of [**WM\_DDE\_INITIATE**](wm-dde-initiate.md)) to track multiple conversations.</span></span> <span data-ttu-id="e913e-150">Dies ermöglicht es einem einzelnen Client Fenster, mehrere Konversationen zu verarbeiten, ohne dass eine Verbindung mit einem neuen Client Fenster für jede Konversation hergestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="e913e-150">This allows a single client window to process several conversations without needing to terminate and reconnect with a new client window for each conversation.</span></span>

## <a name="transferring-a-single-item"></a><span data-ttu-id="e913e-151">Übertragen eines einzelnen Elements</span><span class="sxs-lookup"><span data-stu-id="e913e-151">Transferring a Single Item</span></span>

<span data-ttu-id="e913e-152">Nachdem eine DDE-Konversation eingerichtet wurde, kann der Client entweder den Wert eines Datenelements vom Server abrufen, indem er die [**WM- \_ DDE- \_ Anforderungs**](wm-dde-request.md) Nachricht ausgibt, oder einen Datenelement Wert an den Server übermitteln, indem [**WM \_ DDE \_ Poke**](wm-dde-poke.md)ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-152">Once a DDE conversation has been established, the client can either retrieve the value of a data item from the server by issuing the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message, or submit a data-item value to the server by issuing [**WM\_DDE\_POKE**](wm-dde-poke.md).</span></span>

-   [<span data-ttu-id="e913e-153">Abrufen eines Elements vom Server</span><span class="sxs-lookup"><span data-stu-id="e913e-153">Retrieving an Item from the Server</span></span>](#retrieving-an-item-from-the-server)
-   [<span data-ttu-id="e913e-154">Ein Element wird an den Server übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e913e-154">Submitting an Item to the Server</span></span>](#submitting-an-item-to-the-server)

### <a name="retrieving-an-item-from-the-server"></a><span data-ttu-id="e913e-155">Abrufen eines Elements vom Server</span><span class="sxs-lookup"><span data-stu-id="e913e-155">Retrieving an Item from the Server</span></span>

<span data-ttu-id="e913e-156">Zum Abrufen eines Elements vom Server sendet der Client dem Server eine WM- [**\_ DDE- \_ Anforderungs**](wm-dde-request.md) Nachricht, die das abzurufende Element und Format angibt, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e913e-156">To retrieve an item from the server, the client sends the server a [**WM\_DDE\_REQUEST**](wm-dde-request.md) message specifying the item and format to retrieve, as shown in the following example.</span></span>


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_REQUEST, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_REQUEST, CF_TEXT, atomItem))) 
    {
        GlobalDeleteAtom(atomItem); 
    }
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="e913e-157">In diesem Beispiel gibt der Client den **CF- \_ Text** des Zwischenablage Formats als bevorzugtes Format für das angeforderte Datenelement an.</span><span class="sxs-lookup"><span data-stu-id="e913e-157">In this example, the client specifies the clipboard format **CF\_TEXT** as the preferred format for the requested data item.</span></span>

<span data-ttu-id="e913e-158">Der Empfänger (Server) der [**WM- \_ DDE- \_ Anforderungs**](wm-dde-request.md) Nachricht muss das Element Atom in der Regel löschen, aber wenn der [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Rückruf fehlschlägt, muss der Client das Atom löschen.</span><span class="sxs-lookup"><span data-stu-id="e913e-158">The receiver (server) of the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message typically must delete the item atom, but if the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) call fails, the client must delete the atom.</span></span>

<span data-ttu-id="e913e-159">Wenn der Server Zugriff auf das angeforderte Element hat und ihn im angeforderten Format rendert, kopiert der Server den Elementwert als frei gegebenes Speicher Objekt und sendet dem Client eine [**WM \_ DDE- \_ Daten**](wm-dde-data.md) Nachricht, wie im folgenden Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e913e-159">If the server has access to the requested item and can render it in the requested format, the server copies the item value as a shared memory object and sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message, as illustrated in the following example.</span></span>


```
// Allocate the size of the DDE data header, plus the data: a 
// string,<CR><LF><NULL>. The byte for the string's terminating 
// null character is counted by DDEDATA.Value[1].

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEDATA) + *pcch + 2)))  
{
    return; 
}
 
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData)))  
{
    GlobalFree(hData); 
    return; 
} 
 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpData->Value, *pcch +1, (LPCSTR) szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
} 
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItemName)) != 0) 
{ 
    lParam = PackDDElParam(WM_DDE_ACK, (UINT) hData, atomItem); 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            lParam)) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_ACK, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors.  
}
```



<span data-ttu-id="e913e-160">In diesem Beispiel weist die Serveranwendung ein Speicher Objekt zu, das das Datenelement enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="e913e-160">In this example, the server application allocates a memory object to contain the data item.</span></span> <span data-ttu-id="e913e-161">Das Datenobjekt wird als [**DDE Data**](/windows/desktop/api/Dde/ns-dde-ddedata) -Struktur initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e913e-161">The data object is initialized as a [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure.</span></span>

<span data-ttu-id="e913e-162">Die Serveranwendung legt dann den **cfFormat** -Member der Struktur auf CF \_ Text fest, um der Client Anwendung mitzuteilen, dass die Daten im Text Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="e913e-162">The server application then sets the **cfFormat** member of the structure to CF\_TEXT to inform the client application that the data is in text format.</span></span> <span data-ttu-id="e913e-163">Der Client antwortet, indem er den Wert der angeforderten Daten in das **Wertmember** der [**DDE Data**](/windows/desktop/api/Dde/ns-dde-ddedata) -Struktur kopiert.</span><span class="sxs-lookup"><span data-stu-id="e913e-163">The client responds by copying the value of the requested data into the **Value** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure.</span></span> <span data-ttu-id="e913e-164">Nachdem der Server das Datenobjekt ausgefüllt hat, entsperrt der Server die Daten und erstellt ein globales Atom, das den Namen des Datenelements enthält.</span><span class="sxs-lookup"><span data-stu-id="e913e-164">After the server has filled the data object, the server unlocks the data and creates a global atom containing the name of the data item.</span></span>

<span data-ttu-id="e913e-165">Schließlich gibt der Server die [**WM \_ DDE- \_ Daten**](wm-dde-data.md) Nachricht durch Aufrufen von [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)aus.</span><span class="sxs-lookup"><span data-stu-id="e913e-165">Finally, the server issues the [**WM\_DDE\_DATA**](wm-dde-data.md) message by calling [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea).</span></span> <span data-ttu-id="e913e-166">Das Handle für das Datenobjekt und das Atom mit dem Elementnamen werden von der [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) -Funktion in den *LPARAM* -Parameter der Nachricht gepackt.</span><span class="sxs-lookup"><span data-stu-id="e913e-166">The handle to the data object and the atom containing the item name are packed into the *lParam* parameter of the message by the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function.</span></span>

<span data-ttu-id="e913e-167">Wenn [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) fehlschlägt, muss der Server die [**freeddelta param**](/windows/desktop/api/Dde/nf-dde-freeddelparam) -Funktion verwenden, um den gepackten *LPARAM* -Parameter freizugeben.</span><span class="sxs-lookup"><span data-stu-id="e913e-167">If [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) fails, the server must use the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function to free the packed *lParam* parameter.</span></span> <span data-ttu-id="e913e-168">Der Server muss auch den gepackten *LPARAM* -Parameter für die empfangene [**WM- \_ DDE- \_ Anforderungs**](wm-dde-request.md) Nachricht freigeben.</span><span class="sxs-lookup"><span data-stu-id="e913e-168">The server must also free the packed *lParam* parameter for the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message it received.</span></span>

<span data-ttu-id="e913e-169">Wenn der Server die Anforderung nicht erfüllen kann, sendet er eine negative [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung an den Client, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e913e-169">If the server cannot satisfy the request, it sends a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message to the client, as shown in the following example.</span></span>


```
// Negative acknowledgment. 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 0, atomItem));
```



<span data-ttu-id="e913e-170">Beim Empfang einer [**WM- \_ DDE- \_ Daten**](wm-dde-data.md) Nachricht verarbeitet der Client den Datenelement Wert nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="e913e-170">Upon receiving a [**WM\_DDE\_DATA**](wm-dde-data.md) message, the client processes the data-item value as appropriate.</span></span> <span data-ttu-id="e913e-171">Wenn das **fakkreq** -Element, auf das in der **WM- \_ DDE- \_ Daten** Meldung verwiesen wird, 1 ist, muss der Server dem Server eine positive [**WM \_ DDE \_ ACK**](wm-dde-ack.md) -Nachricht senden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e913e-171">Then, if the **fAckReq** member pointed to in the **WM\_DDE\_DATA** message is 1, the client must send the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message, as shown in the following example.</span></span>


```
UnpackDDElParam(WM_DDE_DATA, lParam, (PUINT) &hData, 
    (PUINT) &atomItem); 
if (!(lpDDEData = (DDEDATA FAR*) GlobalLock(hData)) 
        || (lpDDEData->cfFormat != CF_TEXT)) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // Negative ACK. 
} 
 
// Copy data from lpDDEData here. 
 
if (lpDDEData->fAckReq) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0x8000, 
            atomItem)); // Positive ACK 
} 
 
bRelease = lpDDEData->fRelease; 
GlobalUnlock(hData); 
if (bRelease) 
    GlobalFree(hData);
```



<span data-ttu-id="e913e-172">In diesem Beispiel untersucht der Client das Format der Daten.</span><span class="sxs-lookup"><span data-stu-id="e913e-172">In this example, the client examines the format of the data.</span></span> <span data-ttu-id="e913e-173">Wenn das Format nicht der **CF- \_ Text** ist (oder wenn der Client den Arbeitsspeicher für die Daten nicht sperren kann), sendet der Client eine negative [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht, um anzugeben, dass die Daten nicht verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="e913e-173">If the format is not **CF\_TEXT** (or if the client cannot lock the memory for the data), the client sends a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message to indicate that it cannot process the data.</span></span> <span data-ttu-id="e913e-174">Wenn der Client ein Daten Handle nicht sperren kann, da das Handle das **fakkreq** -Element enthält, sollte der Client keine negative **WM- \_ DDE \_** -Bestätigungsnachricht senden.</span><span class="sxs-lookup"><span data-stu-id="e913e-174">If the client cannot lock a data handle because the handle contains the **fAckReq** member, the client should not send a negative **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="e913e-175">Stattdessen sollte der Client die Konversation beenden.</span><span class="sxs-lookup"><span data-stu-id="e913e-175">Instead, the client should terminate the conversation.</span></span>

<span data-ttu-id="e913e-176">Wenn ein Client eine negative Bestätigung als Antwort auf eine WM- [**\_ DDE- \_ Daten**](wm-dde-data.md) Nachricht sendet, ist der Server dafür verantwortlich, den Speicher freizugeben (aber nicht den *LPARAM* -Parameter), auf den von der mit der negativen Bestätigung verknüpften **WM \_ DDE- \_ Daten** Meldung verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-176">If a client sends a negative acknowledgment in response to a [**WM\_DDE\_DATA**](wm-dde-data.md) message, the server is responsible for freeing the memory (but not the *lParam* parameter) referenced by the **WM\_DDE\_DATA** message associated with the negative acknowledgment.</span></span>

<span data-ttu-id="e913e-177">Wenn die Daten verarbeitet werden können, überprüft der Client den **fakkreq** -Member der [**ddedata**](/windows/desktop/api/Dde/ns-dde-ddedata) -Struktur, um zu bestimmen, ob der Server die Daten informiert hat, dass der Client die Daten erfolgreich empfangen und verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="e913e-177">If it can process the data, the client examines the **fAckReq** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to determine whether the server requested that it be informed that the client received and processed the data successfully.</span></span> <span data-ttu-id="e913e-178">Wenn der Server diese Informationen angefordert hat, sendet der Client dem Server eine positive [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="e913e-178">If the server did request this information, the client sends the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="e913e-179">Da durch das Entsperren von Daten der Zeiger auf die Daten ungültig wird, speichert der Client den Wert des **frelease** -Members, bevor das Datenobjekt entsperrt wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-179">Because unlocking data invalidates the pointer to the data, the client saves the value of the **fRelease** member before unlocking the data object.</span></span> <span data-ttu-id="e913e-180">Nach dem Speichern des Werts wird der Client vom Client überprüft, um zu bestimmen, ob die Serveranwendung den Speicher des Clients angefordert hat. der Client verhält sich entsprechend.</span><span class="sxs-lookup"><span data-stu-id="e913e-180">After saving the value, the client then examines it to determine whether the server application requested the client to free the memory containing the data; the client acts accordingly.</span></span>

<span data-ttu-id="e913e-181">Nachdem eine negative [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung empfangen wurde, kann der Client wieder denselben Elementwert anfordern und ein anderes Zwischenablage Format angeben.</span><span class="sxs-lookup"><span data-stu-id="e913e-181">Upon receiving a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the client can ask for the same item value again, specifying a different clipboard format.</span></span> <span data-ttu-id="e913e-182">In der Regel fragt ein Client zunächst das komplexeste Format ab, das er unterstützen kann, und führt dann ggf. durch progressivste Formate einen Schritt aus, bis es von dem Server bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e913e-182">Typically, a client will first ask for the most complex format it can support, then step down if necessary through progressively simpler formats until it finds one the server can provide.</span></span>

<span data-ttu-id="e913e-183">Wenn der Server das Formatierungselement des Themas System unterstützt, kann der Client feststellen, welche Zwischenablage Formate der Server unterstützt, anstatt Sie jedes Mal zu ermitteln, wenn der Client ein Element anfordert.</span><span class="sxs-lookup"><span data-stu-id="e913e-183">If the server supports the Formats item of the system topic, the client can determine once what clipboard formats the server supports, instead of determining them each time the client requests an item.</span></span>

### <a name="submitting-an-item-to-the-server"></a><span data-ttu-id="e913e-184">Ein Element wird an den Server übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e913e-184">Submitting an Item to the Server</span></span>

<span data-ttu-id="e913e-185">Der Client kann einen Elementwert mithilfe der [**WM- \_ DDE- \_ Poke**](wm-dde-poke.md) -Nachricht an den Server senden.</span><span class="sxs-lookup"><span data-stu-id="e913e-185">The client may send an item value to the server by using the [**WM\_DDE\_POKE**](wm-dde-poke.md) message.</span></span> <span data-ttu-id="e913e-186">Der Client rendert das zu sendende Element und sendet die **WM- \_ DDE- \_ Poke** -Nachricht, wie im folgenden Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e913e-186">The client renders the item to be sent and sends the **WM\_DDE\_POKE** message, as illustrated in the following example.</span></span>


```
size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hPokeData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEPOKE) + *pcch + 2))) 
{
    return; 
}
 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData))) 
{ 
    GlobalFree(hPokeData); 
    return; 
} 
 
lpPokeData->fRelease = TRUE; 
lpPokeData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpPokeData->Value, *pcch +1, (LPCSTR) szValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpPokeData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hPokeData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItem)) != 0) 
{ 
 
        if (!PostMessage(hwndServerDDE, 
                WM_DDE_POKE, 
                (WPARAM) hwndClientDDE, 
                PackDDElParam(WM_DDE_POKE, (UINT) hPokeData, 
                    atomItem))) 
        { 
            GlobalDeleteAtom(atomItem); 
            GlobalFree(hPokeData); 
        } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
} 
```



> [!Note]  
> <span data-ttu-id="e913e-187">Das Senden von Daten mithilfe einer [**WM- \_ DDE- \_ Poke**](wm-dde-poke.md) -Nachricht ist im Wesentlichen identisch mit dem Senden der Daten mithilfe von [**WM-DDE- \_ \_ Daten**](wm-dde-data.md), mit der Ausnahme, dass **WM \_ DDE \_ Poke** vom Client an den Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-187">Sending data by using a [**WM\_DDE\_POKE**](wm-dde-poke.md) message is essentially the same as sending it by using [**WM\_DDE\_DATA**](wm-dde-data.md), except that **WM\_DDE\_POKE** is sent from the client to the server.</span></span>

 

<span data-ttu-id="e913e-188">Wenn der Server den Datenelement Wert in dem vom Client gerenderten Format akzeptieren kann, verarbeitet der Server den Elementwert nach Bedarf und sendet dem Client eine positive [**WM \_ DDE \_ ACK**](wm-dde-ack.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e913e-188">If the server is able to accept the data-item value in the format rendered by the client, the server processes the item value as appropriate and sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="e913e-189">Wenn der Elementwert aufgrund seines Formats oder aus anderen Gründen nicht verarbeitet werden kann, sendet der Server dem Client eine negative **WM \_ DDE \_ ACK** -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e913e-189">If it is unable to process the item value, because of its format or for other reasons, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>


```
UnpackDDElParam(WM_DDE_POKE, lParam, (PUINT) &hPokeData, 
    (PUINT) &atomItem); 
GlobalGetAtomName(atomItem, szItemName, ITEM_NAME_MAX_SIZE); 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData)) 
        || lpPokeData->cfFormat != CF_TEXT 
        || !IsItemSupportedByServer(szItemName)) 
{ 
    PostMessage(hwndClientDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndServerDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // negative ACK  
}
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
} 
hResult = StringCchCopy(szItemValue, *pcch +1, lpPokeData->Value); // copies value 
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
bRelease = lpPokeData->fRelease; 
GlobalUnlock(hPokeData); 
if (bRelease) 
{ 
    GlobalFree(hPokeData); 
} 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 
         0x8000, atomItem));    // positive ACK.
```



<span data-ttu-id="e913e-190">In diesem Beispiel ruft der Server [**globalgetatomname**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) auf, um den Namen des vom Client gesendeten Elements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e913e-190">In this example, the server calls [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) to retrieve the name of the item the client sent.</span></span> <span data-ttu-id="e913e-191">Der Server bestimmt dann, ob das Element unterstützt wird und ob das Element im richtigen Format (CF-Text) gerendert wird \_ .</span><span class="sxs-lookup"><span data-stu-id="e913e-191">The server then determines whether it supports the item and whether the item is rendered in the correct format (that is, CF\_TEXT).</span></span> <span data-ttu-id="e913e-192">Wenn das Element nicht unterstützt wird und nicht im richtigen Format gerendert wird oder der Server den Arbeitsspeicher für die Daten nicht sperren kann, sendet der Server eine negative Bestätigung an die Client Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="e913e-192">If the item is not supported and not rendered in the correct format, or if the server cannot lock the memory for the data, the server sends a negative acknowledgment back to the client application.</span></span> <span data-ttu-id="e913e-193">Beachten Sie, dass das Senden einer negativen Bestätigung in diesem Fall korrekt ist, da bei [**WM \_ DDE \_ Poke**](wm-dde-poke.md) -Nachrichten immer angenommen wird, dass der **fakkreq** -Member festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e913e-193">Note that in this case, sending a negative acknowledgment is correct because [**WM\_DDE\_POKE**](wm-dde-poke.md) messages are always assumed to have the **fAckReq** member set.</span></span> <span data-ttu-id="e913e-194">Der Server sollte den Member ignorieren.</span><span class="sxs-lookup"><span data-stu-id="e913e-194">The server should ignore the member.</span></span>

<span data-ttu-id="e913e-195">Wenn ein Server eine negative Bestätigung als Antwort auf eine WM- [**\_ DDE- \_ Poke**](wm-dde-poke.md) -Nachricht sendet, ist der Client für die Freigabe des Arbeitsspeichers (aber nicht für den *LPARAM* -Parameter) verantwortlich, auf den von der mit der negativen Bestätigung verknüpften **WM-DDE- \_ \_ Poke** -Meldung verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-195">If a server sends a negative acknowledgment in response to a [**WM\_DDE\_POKE**](wm-dde-poke.md) message, the client is responsible for freeing the memory (but not the *lParam* parameter) referenced by the **WM\_DDE\_POKE** message associated with the negative acknowledgment.</span></span>

## <a name="establishing-a-permanent-data-link"></a><span data-ttu-id="e913e-196">Einrichten einer permanenten Datenverknüpfung</span><span class="sxs-lookup"><span data-stu-id="e913e-196">Establishing a Permanent Data Link</span></span>

<span data-ttu-id="e913e-197">Eine Client Anwendung kann DDE verwenden, um einen Link zu einem Element in einer Serveranwendung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="e913e-197">A client application can use DDE to establish a link to an item in a server application.</span></span> <span data-ttu-id="e913e-198">Nachdem ein solcher Link festgelegt wurde, sendet der Server regelmäßige Aktualisierungen des verknüpften Elements an den Client, in der Regel, wenn der Wert des Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-198">After such a link is established, the server sends periodic updates of the linked item to the client, typically, whenever the value of the item changes.</span></span> <span data-ttu-id="e913e-199">Daher wird ein dauerhafter Datenstrom zwischen den beiden Anwendungen eingerichtet. dieser Datenstrom bleibt so lange bestehen, bis er explizit getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-199">Thus, a permanent data stream is established between the two applications; this data stream remains in place until it is explicitly disconnected.</span></span>

### <a name="initiating-a-data-link"></a><span data-ttu-id="e913e-200">Initiieren einer Datenverknüpfung</span><span class="sxs-lookup"><span data-stu-id="e913e-200">Initiating a Data Link</span></span>

<span data-ttu-id="e913e-201">Der Client initiiert eine Datenverknüpfung, indem er eine Meldung vom Typ " [**WM \_ DDE \_**](wm-dde-advise.md) " veröffentlicht, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e913e-201">The client initiates a data link by posting a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, as shown in the following example.</span></span>


```
if (!(hOptions = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(DDEADVISE)))) 
    return; 
if (!(lpOptions = (DDEADVISE FAR*) GlobalLock(hOptions))) 
{ 
    GlobalFree(hOptions); 
    return; 
} 
 
lpOptions->cfFormat = CF_TEXT; 
lpOptions->fAckReq = TRUE; 
lpOptions->fDeferUpd = FALSE; 
GlobalUnlock(hOptions); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!(PostMessage(hwndServerDDE, 
            WM_DDE_ADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_ADVISE, (UINT) hOptions, 
                atomItem)))) 
    { 
        GlobalDeleteAtom(atomItem); 
        GlobalFree(hOptions); 
        FreeDDElParam(WM_DDE_ADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors 
 
}
```



<span data-ttu-id="e913e-202">In diesem Beispiel legt die Client Anwendung das **fdeferupd-** Flag der [**WM- \_ DDE- \_ Empfehlung**](wm-dde-advise.md) -Nachricht auf **false** fest.</span><span class="sxs-lookup"><span data-stu-id="e913e-202">In this example, the client application sets the **fDeferUpd** flag of the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to **FALSE**.</span></span> <span data-ttu-id="e913e-203">Dadurch wird die Serveranwendung angewiesen, die Daten immer dann an den Client zu senden, wenn sich die Daten ändern.</span><span class="sxs-lookup"><span data-stu-id="e913e-203">This directs the server application to send the data to the client whenever the data changes.</span></span>

<span data-ttu-id="e913e-204">Wenn der Server die Anforderung " [**WM DDE- \_ \_ Empfehlung**](wm-dde-advise.md) " nicht bedienen kann, sendet er dem Client eine negative [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="e913e-204">If the server is unable to service the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) request, it sends the client a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="e913e-205">Wenn der Server jedoch Zugriff auf das Element hat und ihn im angeforderten Format renderengen kann, notiert der Server den neuen Link (wobei die im *hoptions* -Parameter angegebenen Flags wieder hergestellt werden) und sendet dem Client eine positive **WM \_ DDE \_ ACK** -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e913e-205">But if the server has access to the item and can render it in the requested format, the server notes the new link (recalling the flags specified in the *hOptions* parameter) and sends the client a positive **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="e913e-206">Von diesem Zeitpunkt an sendet der Server die neuen Daten [**jedes \_ \_**](wm-dde-unadvise.md) Mal, wenn der Wert des Elements auf dem Server geändert wird, an den Client.</span><span class="sxs-lookup"><span data-stu-id="e913e-206">From then on, until the client issues a matching [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message, the server sends the new data to the client every time the value of the item changes in the server.</span></span>

<span data-ttu-id="e913e-207">Die Meldung " [**WM \_ DDE- \_ Empfehlung**](wm-dde-advise.md) " gibt das Format der Daten an, die während des Links ausgetauscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e913e-207">The [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message establishes the format of the data to be exchanged during the link.</span></span> <span data-ttu-id="e913e-208">Wenn der Client versucht, eine andere Verknüpfung mit demselben Element herzustellen, aber ein anderes Datenformat verwendet, kann der Server das zweite Datenformat ablehnen oder versuchen, es zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e913e-208">If the client attempts to establish another link with the same item but is using a different data format, the server can choose to reject the second data format or attempt to support it.</span></span> <span data-ttu-id="e913e-209">Wenn ein warmer Link für ein beliebiges Datenelement eingerichtet wurde, kann der Server jeweils nur ein Datenformat unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e913e-209">If a warm link has been established for any data item, the server can support only one data format at a time.</span></span> <span data-ttu-id="e913e-210">Dies liegt daran, dass die [**WM- \_ DDE- \_ Daten**](wm-dde-data.md) Nachricht für einen warmen Link ein **null** -Daten Handle enthält, das andernfalls die Formatierungsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="e913e-210">This is because the [**WM\_DDE\_DATA**](wm-dde-data.md) message for a warm link has a **NULL** data handle, which otherwise contains the format information.</span></span> <span data-ttu-id="e913e-211">Folglich muss ein Server alle warmen Verknüpfungen für ein Element ablehnen, das bereits verknüpft ist, und alle Verknüpfungen für ein Element ablehnen, das über warme Links verfügt.</span><span class="sxs-lookup"><span data-stu-id="e913e-211">Thus, a server must reject all warm links for an item already linked, and must reject all links for an item that has warm links.</span></span> <span data-ttu-id="e913e-212">Eine andere Interpretation kann sein, dass der Server das Format und den heißen oder den warmen Zustand eines Links ändert, wenn ein zweiter Link für das gleiche Datenelement angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-212">Another interpretation may be that the server changes the format and the hot or warm state of a link when a second link is requested for the same data item.</span></span>

<span data-ttu-id="e913e-213">Im Allgemeinen sollten Client Anwendungen nicht versuchen, mehr als einen Link gleichzeitig für ein Datenelement einzurichten.</span><span class="sxs-lookup"><span data-stu-id="e913e-213">In general, client applications should not attempt to establish more than one link at a time for a data item.</span></span>

### <a name="initiating-a-data-link-with-the-paste-link-command"></a><span data-ttu-id="e913e-214">Initiieren einer Datenverknüpfung mit dem Befehl "Link einfügen"</span><span class="sxs-lookup"><span data-stu-id="e913e-214">Initiating a Data Link with the Paste Link Command</span></span>

<span data-ttu-id="e913e-215">Anwendungen, die Hot-oder warm-Daten Verknüpfungen unterstützen, unterstützen in der Regel das registrierte Zwischenablage Format</span><span class="sxs-lookup"><span data-stu-id="e913e-215">Applications that support hot or warm data links typically support a registered clipboard format named Link.</span></span> <span data-ttu-id="e913e-216">Wenn Sie den Befehlen zum Kopieren und Einfügen von Anwendungen zugeordnet sind, ermöglicht dieses Zwischenablage Format dem Benutzer das Einrichten von DDE-Konversationen zwischen Anwendungen, indem einfach ein Datenelement in der Serveranwendung kopiert und in die Client Anwendung eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-216">When associated with the application's Copy and Paste Link commands, this clipboard format enables the user to establish DDE conversations between applications simply by copying a data item in the server application and pasting it into the client application.</span></span>

<span data-ttu-id="e913e-217">Eine Serveranwendung unterstützt das Format der Link Zwischenablage, indem Sie in der Zwischenablage eine Zeichenfolge platziert, die die Anwendungs-, Thema-und Elementnamen enthält, wenn der Benutzer im Menü **Bearbeiten** den Befehl **Kopieren** auswählt.</span><span class="sxs-lookup"><span data-stu-id="e913e-217">A server application supports the Link clipboard format by placing in the clipboard a string containing the application, topic, and item names when the user chooses the **Copy** command from the **Edit** menu.</span></span> <span data-ttu-id="e913e-218">Im folgenden ist das Standard Verknüpfungs Format aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="e913e-218">Following is the standard Link format:</span></span>

<span data-ttu-id="e913e-219">*Anwendung ***\\ 0*** Thema ***\\ 0*** Element \* \* \* \\ 0 \\ 0*\*</span><span class="sxs-lookup"><span data-stu-id="e913e-219">*application ***\\0*** topic ***\\0*** item\*\*\*\\0\\0*\*</span></span>

<span data-ttu-id="e913e-220">Ein einzelnes Null-Zeichen trennt die Namen, und zwei NULL-Zeichen beenden die gesamte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e913e-220">A single null character separates the names, and two null characters terminate the entire string.</span></span>

<span data-ttu-id="e913e-221">Die Client-und Server Anwendungen müssen das Format der Link Zwischenablage wie folgt registrieren:</span><span class="sxs-lookup"><span data-stu-id="e913e-221">Both the client and server applications must register the Link clipboard format, as shown:</span></span>


```
cfLink = RegisterClipboardFormat("Link");
```



<span data-ttu-id="e913e-222">Eine Client Anwendung unterstützt das Format der Link Zwischenablage mithilfe eines Befehls zum Einfügen von Links im Menü Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e913e-222">A client application supports the Link clipboard format by means of a Paste Link command on its Edit menu.</span></span> <span data-ttu-id="e913e-223">Wenn der Benutzer diesen Befehl auswählt, analysiert die Client Anwendung die Anwendungs-, Thema-und Elementnamen aus den Zwischenablage Daten des Verknüpfungs Formats.</span><span class="sxs-lookup"><span data-stu-id="e913e-223">When the user chooses this command, the client application parses the application, topic, and item names from the Link-format clipboard data.</span></span> <span data-ttu-id="e913e-224">Mit diesen Namen initiiert die Client Anwendung eine Konversation für die Anwendung und das Thema, wenn eine solche Konversation nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e913e-224">Using these names, the client application initiates a conversation for the application and topic, if such a conversation does not already exist.</span></span> <span data-ttu-id="e913e-225">Die Client Anwendung sendet eine [**WM- \_ DDE \_**](wm-dde-advise.md) -Benachrichtigungs Meldung an die Serveranwendung und gibt dabei den Elementnamen an, der in den Zwischenablage Daten des Link Formats enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e913e-225">The client application then sends a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to the server application, specifying the item name contained in the Link-format clipboard data.</span></span>

<span data-ttu-id="e913e-226">Im folgenden finden Sie ein Beispiel für die Antwort einer Client Anwendung, wenn der Benutzer den Befehl Link einfügen auswählt.</span><span class="sxs-lookup"><span data-stu-id="e913e-226">Following is an example of a client application's response when the user chooses the Paste Link command.</span></span>


```
void DoPasteLink(hwndClientDDE) 
HWND hwndClientDDE; 
{ 
    HANDLE hData; 
    LPSTR lpData; 
    HWND hwndServerDDE; 
    CHAR szApplication[APP_MAX_SIZE + 1]; 
    CHAR szTopic[TOPIC_MAX_SIZE + 1]; 
    CHAR szItem[ITEM_MAX_SIZE + 1]; 
    size_t * nBufLen; 
 HRESULT hResult;
 
    if (OpenClipboard(hwndClientDDE)) 
    { 
        if (!(hData = GetClipboardData(cfLink)) || 
                !(lpData = GlobalLock(hData))) 
        { 
            CloseClipboard(); 
            return; 
        } 
 
        // Parse the clipboard data.
  hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
// TODO: Write error handler.
  return;
 }
 if (*nBufLen >= APP_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szApplication, APP_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
// TODO: Write error handler.
  return;
 }
        lpData += (*nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= TOPIC_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szTopic, TOPIC_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 }
        lpData += (nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= ITEM_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }

 hResult = StringCchCopy(szItem, ITEM_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 } 
        GlobalUnlock(hData); 
        CloseClipboard(); 
 
        if (hwndServerDDE = 
                FindServerGivenAppTopic(szApplication, szTopic)) 
        { 
            // App/topic conversation is already started. 
 
            if (DoesAdviseAlreadyExist(hwndServerDDE, szItem)) 
            {
                MessageBox(hwndMain, 
                    "Advisory already established", 
                    "Client", MB_ICONEXCLAMATION | MB_OK); 
            }
            else SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
        } 
        else 
        { 
            // Client must initiate a new conversation first. 
            SendInitiate(szApplication, szTopic); 
            if (hwndServerDDE = 
                    FindServerGivenAppTopic(szApplication, 
                        szTopic)) 
            {
                SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
            }
        } 
    } 
    return; 
}
```



<span data-ttu-id="e913e-227">In diesem Beispiel öffnet die Client Anwendung die Zwischenablage und bestimmt, ob Sie Daten im Verknüpfungs Format (d. h. cflink) enthält, das zuvor registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="e913e-227">In this example, the client application opens the clipboard and determines whether it contains data in the Link format (that is, cfLink) it had previously registered.</span></span> <span data-ttu-id="e913e-228">Wenn dies nicht der Fall ist oder wenn die Daten in der Zwischenablage nicht gesperrt werden können, gibt der Client zurück.</span><span class="sxs-lookup"><span data-stu-id="e913e-228">If not, or if it cannot lock the data in the clipboard, the client returns.</span></span>

<span data-ttu-id="e913e-229">Nachdem die Client Anwendung einen Zeiger auf die Zwischenablage Daten abgerufen hat, analysiert Sie die Daten, um die Anwendungs-, Thema-und Elementnamen zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="e913e-229">After the client application retrieves a pointer to the clipboard data, it parses the data to extract the application, topic, and item names.</span></span>

<span data-ttu-id="e913e-230">Die Client Anwendung bestimmt, ob eine Konversation für das Thema bereits zwischen der Anwendung und der Serveranwendung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e913e-230">The client application determines whether a conversation on the topic already exists between it and the server application.</span></span> <span data-ttu-id="e913e-231">Wenn eine Konversation vorhanden ist, überprüft der Client, ob für das Datenelement bereits ein Link vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e913e-231">If a conversation does exist, the client checks whether a link already exists for the data item.</span></span> <span data-ttu-id="e913e-232">Wenn ein solcher Link vorhanden ist, zeigt der Client dem Benutzer ein Meldungs Feld an. Andernfalls wird eine eigene *sendempfehlung* -Funktion aufgerufen, um eine [**WM- \_ DDE \_**](wm-dde-advise.md) -Benachrichtigungs Meldung an den Server für das Element zu senden.</span><span class="sxs-lookup"><span data-stu-id="e913e-232">If such a link exists, the client displays a message box to the user; otherwise, it calls its own *SendAdvise* function to send a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to the server for the item.</span></span>

<span data-ttu-id="e913e-233">Wenn eine Konversation für das Thema nicht bereits zwischen dem Client und dem Server vorhanden ist, ruft der Client zuerst seine eigene *sendinitiate* -Funktion auf, um die [**WM-DDE- \_ \_ Initiierungs**](wm-dde-initiate.md) Nachricht zu senden und eine Konversation anzufordern. Anschließend ruft er eine eigene *findserfehlervenapptopic* -Funktion auf, um die Konversation mit dem Fenster, das im Auftrag der Serveranwendung</span><span class="sxs-lookup"><span data-stu-id="e913e-233">If a conversation on the topic does not already exist between the client and the server, the client first calls its own *SendInitiate* function to broadcast the [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message to request a conversation and, second, calls its own *FindServerGivenAppTopic* function to establish the conversation with the window that responds on behalf of the server application.</span></span> <span data-ttu-id="e913e-234">Nachdem die Konversation begonnen hat, ruft die Client Anwendung *SendRequest* auf, um den Link anzufordern.</span><span class="sxs-lookup"><span data-stu-id="e913e-234">After the conversation has begun, the client application calls *SendAdvise* to request the link.</span></span>

### <a name="notifying-the-client-that-data-has-changed"></a><span data-ttu-id="e913e-235">Benachrichtigen des Clients, dass sich Daten geändert haben</span><span class="sxs-lookup"><span data-stu-id="e913e-235">Notifying the Client that Data Has Changed</span></span>

<span data-ttu-id="e913e-236">Wenn der Client mithilfe der WM-DDE- [**\_ \_ Empfehlung**](wm-dde-advise.md) eine Verknüpfung herstellt, während der " **fdeferupd"-** Member in der [**ddedata**](/windows/desktop/api/Dde/ns-dde-ddedata) -Struktur nicht festgelegt ist (d. h. gleich 0 (null)), hat der Client angefordert, dass der Server jedes Mal das Datenelement sendet, wenn sich der Wert des Elements ändert.</span><span class="sxs-lookup"><span data-stu-id="e913e-236">When the client establishes a link by using the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, with the **fDeferUpd** member not set (that is, equal to zero) in the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure, the client has requested the server send the data item each time the item's value changes.</span></span> <span data-ttu-id="e913e-237">In solchen Fällen rendert der Server den neuen Wert des Datenelements im zuvor angegebenen Format und sendet dem Client eine [**WM DDE- \_ \_ Daten**](wm-dde-data.md) Nachricht, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e913e-237">In such cases, the server renders the new value of the data item in the previously specified format and sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message, as shown in the following example.</span></span>


```
// Allocate the size of a DDE data header, plus data (a string), 
// plus a <CR><LF><NULL> 

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  sizeof(DDEDATA) + *pcch + 3))) 
{
    return; 
}
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData))) 
{ 
    GlobalFree(hData); 
    return; 
} 
lpData->fAckReq = bAckRequest;       // as in original WM_DDE_ADVISE 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy(lpData->Value, *pcch +1, szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
// add CR/LF for CF_TEXT format
hResult = StringCchCat(lpData->Value, *pcch + 3, "\r\n");
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            PackDDElParam(WM_DDE_DATA, (UINT) hData, atomItem))) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_DATA, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
 
}
```



<span data-ttu-id="e913e-238">In diesem Beispiel verarbeitet der Client den Elementwert nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="e913e-238">In this example, the client processes the item value as appropriate.</span></span> <span data-ttu-id="e913e-239">Wenn das **fakkreq** -Flag für das Element festgelegt ist, sendet der Client dem Server eine positive [**WM \_ DDE \_ ACK**](wm-dde-ack.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e913e-239">If the **fAckReq** flag for the item is set, the client sends the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="e913e-240">Wenn der Client den Link festlegt, wobei das **fdeferupd-** Element festgelegt ist (d. h. gleich 1), hat der Client angefordert, dass nur eine Benachrichtigung, nicht die Daten selbst, gesendet werden, wenn sich die Daten ändern.</span><span class="sxs-lookup"><span data-stu-id="e913e-240">When the client establishes the link, with the **fDeferUpd** member set (that is, equal to 1), the client has requested that only a notification, not the data itself, be sent each time the data changes.</span></span> <span data-ttu-id="e913e-241">In solchen Fällen, wenn sich der Elementwert ändert, wird der Wert vom Server nicht dargestellt, sondern es wird einfach eine [**WM- \_ DDE- \_ Daten**](wm-dde-data.md) Nachricht mit einem NULL-Daten Handle an den Client gesendet, wie im folgenden Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e913e-241">In such cases, when the item value changes, the server does not render the value but simply sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message with a null data handle, as illustrated in the following example.</span></span>


```
if (bDeferUpd)      // check whether flag was set in WM_DDE_ADVISE
{
    if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
    { 
        if (!PostMessage(hwndClientDDE, 
                WM_DDE_DATA, 
                (WPARAM) hwndServerDDE, 
                PackDDElParam(WM_DDE_DATA, 0, 
                    atomItem)))                  // NULL data
        {
            GlobalDeleteAtom(atomItem); 
            FreeDDElParam(WM_DDE_DATA, lParam); 
        } 
    } 
} 
 
if (atomItem == 0) 
{ 
     // Handle errors. 
} 
```



<span data-ttu-id="e913e-242">Bei Bedarf kann der Client den neuesten Wert des Datenelements anfordern, indem er eine normale [**WM- \_ DDE- \_ Anforderungs**](wm-dde-request.md) Nachricht ausgibt, oder er kann einfach den Hinweis vom Server ignorieren, dass sich die Daten geändert haben.</span><span class="sxs-lookup"><span data-stu-id="e913e-242">As necessary, the client can request the latest value of the data item by issuing a normal [**WM\_DDE\_REQUEST**](wm-dde-request.md) message, or it can simply ignore the notice from the server that the data has changed.</span></span> <span data-ttu-id="e913e-243">Wenn " **fakkreq** " gleich 1 ist, wird erwartet, dass der Client eine positive [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht an den Server sendet.</span><span class="sxs-lookup"><span data-stu-id="e913e-243">In either case, if **fAckReq** is equal to 1, the client is expected to send a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message to the server.</span></span>

### <a name="terminating-a-data-link"></a><span data-ttu-id="e913e-244">Beenden eines Daten Links</span><span class="sxs-lookup"><span data-stu-id="e913e-244">Terminating a Data Link</span></span>

<span data-ttu-id="e913e-245">Wenn der Client anfordert, dass eine bestimmte Datenverknüpfung beendet wird, sendet der Client dem Server eine Meldung vom Typ " [**WM \_ DDE \_ unempfehlung**](wm-dde-unadvise.md) ", wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e913e-245">If the client requests that a specific data link be terminated, the client sends the server a [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message, as shown in the following example.</span></span>


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_UNADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_UNADVISE, 0, atomItem))) 
    { 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_UNADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="e913e-246">Der Server überprüft, ob der Client zurzeit über einen Link zum bestimmten Element in dieser Konversation verfügt.</span><span class="sxs-lookup"><span data-stu-id="e913e-246">The server checks whether the client currently has a link to the specific item in this conversation.</span></span> <span data-ttu-id="e913e-247">Wenn ein Link vorhanden ist, sendet der Server dem Client eine positive [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung. der Server ist dann nicht mehr zum Senden von Updates über das Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e913e-247">If a link exists, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; the server is then no longer required to send updates about the item.</span></span> <span data-ttu-id="e913e-248">Wenn kein Link vorhanden ist, sendet der Server dem Client eine negative **WM \_ DDE \_** -Bestätigungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="e913e-248">If no link exists, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>

<span data-ttu-id="e913e-249">Die " [**WM \_ DDE \_ unempfehlung**](wm-dde-unadvise.md) "-Meldung gibt ein Datenformat an.</span><span class="sxs-lookup"><span data-stu-id="e913e-249">The [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message specifies a data format.</span></span> <span data-ttu-id="e913e-250">Bei einem Format von NULL wird der Server angewiesen, alle Verknüpfungen für das angegebene Element zu unterbinden, auch wenn mehrere heiße Verknüpfungen eingerichtet sind und jeweils ein anderes Format verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-250">A format of zero informs the server to stop all links for the specified item, even if several hot links are established and each uses a different format.</span></span>

<span data-ttu-id="e913e-251">Um alle Verknüpfungen für eine Konversation zu beenden, sendet die Client Anwendung dem Server eine [**\_ \_ nicht Empfehlung**](wm-dde-unadvise.md) -Nachricht vom Typ "WM DDE" mit einem NULL-Element Atom.</span><span class="sxs-lookup"><span data-stu-id="e913e-251">To terminate all links for a conversation, the client application sends the server a [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message with a null item atom.</span></span> <span data-ttu-id="e913e-252">Der Server bestimmt, ob für die Konversation mindestens ein Link eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="e913e-252">The server determines whether the conversation has at least one link currently established.</span></span> <span data-ttu-id="e913e-253">Wenn ein Link vorhanden ist, sendet der Server dem Client eine positive [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht. der Server muss dann keine Updates mehr in der Konversation senden.</span><span class="sxs-lookup"><span data-stu-id="e913e-253">If a link exists, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; the server then no longer has to send any updates in the conversation.</span></span> <span data-ttu-id="e913e-254">Wenn kein Link vorhanden ist, sendet der Server dem Client eine negative **WM \_ DDE \_** -Bestätigungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="e913e-254">If no link exists, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>

## <a name="carrying-out-commands-in-a-server-application"></a><span data-ttu-id="e913e-255">Ausführen von Befehlen in einer Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="e913e-255">Carrying Out Commands in a Server Application</span></span>

<span data-ttu-id="e913e-256">Anwendungen können die " [**WM \_ DDE \_ Execute**](wm-dde-execute.md) "-Nachricht verwenden, um zu veranlassen, dass ein bestimmter Befehl oder eine Reihe von Befehlen in einer anderen Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-256">Applications can use the [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message to cause a certain command or series of commands to be carried out in another application.</span></span> <span data-ttu-id="e913e-257">Hierzu sendet der Client dem Server eine **WM-DDE- \_ \_ Execute** -Nachricht mit einem Handle an eine Befehls Zeichenfolge, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e913e-257">To do this, the client sends the server a **WM\_DDE\_EXECUTE** message containing a handle to a command string, as shown in the following example.</span></span>


```
HRESULT hResult;
  
if (!(hCommand = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(szCommandString) + 1))) 
{
    return; 
}
if (!(lpCommand = GlobalLock(hCommand))) 
{ 
    GlobalFree(hCommand); 
    return; 
} 

hResult = StringCbCopy(lpCommand, sizeof(szCommandString), szCommandString);
if (hResult != S_OK)
{
// TODO: Write error handler.
 return;
}
 
GlobalUnlock(hCommand); 
if (!PostMessage(hwndServerDDE, 
        WM_DDE_EXECUTE, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_EXECUTE, 0, (UINT) hCommand))) 
{ 
    GlobalFree(hCommand); 
    FreeDDElParam(WM_DDE_EXECUTE, lParam); 
}
```



<span data-ttu-id="e913e-258">In diesem Beispiel versucht der Server, die angegebene Befehls Zeichenfolge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e913e-258">In this example, the server attempts to carry out the specified command string.</span></span> <span data-ttu-id="e913e-259">Wenn dies der Fall ist, sendet der Server dem Client eine positive [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht, andernfalls sendet er eine negative **WM- \_ DDE \_** -Bestätigungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="e913e-259">If it succeeds, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; otherwise, it sends a negative **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="e913e-260">Diese **WM- \_ DDE \_** -Bestätigungsnachricht verwendet das *hcommand* -handle, das in der ursprünglichen [**WM-DDE- \_ \_ Ausführungs**](wm-dde-execute.md) Nachricht weitergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e913e-260">This **WM\_DDE\_ACK** message reuses the *hCommand* handle passed in the original [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message.</span></span>

<span data-ttu-id="e913e-261">Wenn die Befehls Ausführungs Zeichenfolge des Clients anfordert, dass der Server beendet wird, sollte der Server Antworten, indem er eine positive [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht sendet und eine [**WM- \_ DDE \_**](wm-dde-terminate.md) -Beendigungs Nachricht vor dem Beenden sendet.</span><span class="sxs-lookup"><span data-stu-id="e913e-261">If the client's command execution string requests that the server terminate, the server should respond by sending a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message and then post a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message before terminating.</span></span> <span data-ttu-id="e913e-262">Alle anderen Befehle, die mit der " [**WM \_ DDE \_ Execute**](wm-dde-execute.md) "-Nachricht gesendet werden, sollten synchron ausgeführt werden, d. h., der Server sollte eine " **WM \_ DDE \_ ACK** "-Nachricht erst senden, nachdem der Befehl erfolgreich abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="e913e-262">All other commands sent with a [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message should be executed synchronously; that is, the server should send a **WM\_DDE\_ACK** message only after successfully completing the command.</span></span>

## <a name="terminating-a-conversation"></a><span data-ttu-id="e913e-263">Beenden einer Konversation</span><span class="sxs-lookup"><span data-stu-id="e913e-263">Terminating a Conversation</span></span>

<span data-ttu-id="e913e-264">Entweder kann der Client oder der Server eine [**WM- \_ DDE \_**](wm-dde-terminate.md) -Beendigungs Nachricht ausgeben, um eine Konversation zu einem beliebigen Zeitpunkt zu beenden.</span><span class="sxs-lookup"><span data-stu-id="e913e-264">Either the client or the server can issue a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message to terminate a conversation at any time.</span></span> <span data-ttu-id="e913e-265">Ebenso sollten sowohl die Client-als auch die Serveranwendung jederzeit darauf vorbereitet sein, diese Nachricht zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="e913e-265">Similarly, both the client and server applications should be prepared to receive this message at any time.</span></span> <span data-ttu-id="e913e-266">Eine Anwendung muss alle Ihre Konversationen beenden, bevor Sie heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-266">An application must terminate all of its conversations before shutting down.</span></span>

<span data-ttu-id="e913e-267">Im folgenden Beispiel stellt die Anwendung, die die Konversation beendet, eine " [**WM \_ DDE \_**](wm-dde-terminate.md) -Beendigungs Nachricht" gepostet.</span><span class="sxs-lookup"><span data-stu-id="e913e-267">In the following example, the application terminating the conversation posts a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message.</span></span>


```
PostMessage(hwndServerDDE, WM_DDE_TERMINATE, 
    (WPARAM) hwndClientDDE, 0);
```



<span data-ttu-id="e913e-268">Dadurch wird der anderen Anwendung mitgeteilt, dass die sendende Anwendung keine weiteren Nachrichten sendet und der Empfänger das Fenster schließen kann.</span><span class="sxs-lookup"><span data-stu-id="e913e-268">This informs the other application that the sending application will send no further messages and the recipient can close its window.</span></span> <span data-ttu-id="e913e-269">In allen Fällen wird erwartet, dass der Empfänger umgehend antwortet, indem er eine Abbruch Meldung vom [**WM \_ \_**](wm-dde-terminate.md) -Dienst sendet.</span><span class="sxs-lookup"><span data-stu-id="e913e-269">The recipient is expected in all cases to respond promptly by sending a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message.</span></span> <span data-ttu-id="e913e-270">Der Empfänger darf keine negative, ausgelastete oder positive [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht senden.</span><span class="sxs-lookup"><span data-stu-id="e913e-270">The recipient must not send a negative, busy, or positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="e913e-271">Nachdem eine Anwendung die " [**WM \_ DDE \_**](wm-dde-terminate.md) "-Beendigungs Nachricht an den Partner in einer DDE-Konversation gesendet hat, darf Sie nicht auf Nachrichten von diesem Partner Antworten, da der Partner das Fenster, an den die Antwort gesendet wurde, möglicherweise zerstört hat.</span><span class="sxs-lookup"><span data-stu-id="e913e-271">After an application has sent the [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message to the partner in a DDE conversation, it must not respond to messages from that partner, since the partner might have destroyed the window to which the response would be sent.</span></span>

<span data-ttu-id="e913e-272">Wenn eine Anwendung eine DDE-Nachricht empfängt, die nicht [**WM \_ DDE \_ beendet**](wm-dde-terminate.md) , nachdem **die WM- \_ DDE \_ beendet** wurde, sollte Sie alle Objekte freigeben, die den empfangenen Nachrichten zugeordnet sind, mit Ausnahme der Daten Handles für [**WM-DDE- \_ \_ Daten**](wm-dde-data.md) oder [**WM \_ DDE \_ Poke**](wm-dde-poke.md) -Nachrichten, für die das **frelease** -Element **nicht** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e913e-272">If an application receives a DDE message other than [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) after it has posted **WM\_DDE\_TERMINATE**, it should free all objects associated with the received messages except the data handles for [**WM\_DDE\_DATA**](wm-dde-data.md) or [**WM\_DDE\_POKE**](wm-dde-poke.md) messages that do **not** have the **fRelease** member set.</span></span>

<span data-ttu-id="e913e-273">Wenn eine Anwendung gerade beendet wird, sollte Sie alle aktiven DDE-Konversationen beenden, bevor die Verarbeitung der WM-Lösch Nachricht abgeschlossen wird. [**\_**](/windows/desktop/winmsg/wm-destroy)</span><span class="sxs-lookup"><span data-stu-id="e913e-273">When an application is about to terminate, it should end all active DDE conversations before completing processing of the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="e913e-274">Wenn eine Anwendung jedoch nicht die aktiven DDE-Konversationen beendet, beendet das System alle DDE-Konversationen, die einem Fenster zugeordnet sind, wenn das Fenster zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="e913e-274">However, if an application does not end its active DDE conversations, the system will terminate any DDE conversations associated with a window when the window is destroyed.</span></span> <span data-ttu-id="e913e-275">Das folgende Beispiel zeigt, wie eine Serveranwendung alle DDE-Konversationen beendet.</span><span class="sxs-lookup"><span data-stu-id="e913e-275">The following example shows how a server application terminates all DDE conversations.</span></span>


```
void TerminateConversations(hwndServerDDE) 
HWND hwndServerDDE; 
{ 
    HWND hwndClientDDE; 
 
    // Terminate each active conversation. 
 
    while (hwndClientDDE = GetNextLink(hwndClientDDE)) 
    { 
        SendTerminate(hwndServerDDE, hwndClientDDE); 
    } 
    return; 
} 
 
BOOL AtLeastOneLinkActive(VOID) 
{ 
    return TRUE; 
} 
 
HWND GetNextLink(hwndDummy) 
    HWND hwndDummy; 
{ 
    return (HWND) 1; 
} 
 
VOID SendTerminate(HWND hwndServerDDE, HWND hwndClientDDE) 
{ 
    return; 
}
```



 

 