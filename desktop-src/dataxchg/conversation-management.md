---
title: Konversations Verwaltung
description: In diesem Thema werden die Konversationen zwischen einem Client und einem Server erörtert.
ms.assetid: 4e5ff1a1-d46a-4e2a-a37c-8df951f2a1ee
keywords:
- Windows-Benutzeroberfläche, dynamischer Datenaustausch (DDE)
- Dynamischer Datenaustausch (DDE), Konversationen
- DDE (dynamischer Datenaustausch), Konversationen
- Datenaustausch, dynamischer Datenaustausch (DDE)
- Windows-Benutzeroberfläche, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
- Dynamischer Datenaustausch Management Library (Ddeml), Konversationen
- Ddeml (dynamischer Datenaustausch Management Library), Konversationen
- Datenaustausch, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
- Dynamischer Datenaustausch (DDE), mehrere Konversationen
- DDE (dynamischer Datenaustausch), mehrere Konversationen
- Dynamischer Datenaustausch Management Library (Ddeml), mehrere Konversationen
- Ddeml (dynamischer Datenaustausch-Verwaltungs Bibliothek), mehrere Konversationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca1a0a8e02bceb6b2f69051d89df289871fdd42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340866"
---
# <a name="conversation-management"></a><span data-ttu-id="9d789-115">Konversations Verwaltung</span><span class="sxs-lookup"><span data-stu-id="9d789-115">Conversation Management</span></span>

<span data-ttu-id="9d789-116">Eine Konversation zwischen einem Client und einem Server wird immer bei der Client Anforderung eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="9d789-116">A conversation between a client and a server is always established at the request of the client.</span></span> <span data-ttu-id="9d789-117">Wenn eine Konversation eingerichtet wird, erhält jeder Partner ein Handle, das die Konversation identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9d789-117">When a conversation is established, each partner receives a handle that identifies the conversation.</span></span> <span data-ttu-id="9d789-118">Die Partner verwenden dieses Handle in anderen Ddeml-Funktionen (dynamischer Datenaustausch Management Library), um Transaktionen zu senden und die Konversation zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="9d789-118">The partners use this handle in other Dynamic Data Exchange Management Library (DDEML) functions to send transactions and manage the conversation.</span></span> <span data-ttu-id="9d789-119">Ein Client kann eine Konversation mit einem einzelnen Server anfordern oder mehrere Konversationen mit einem oder mehreren Servern anfordern.</span><span class="sxs-lookup"><span data-stu-id="9d789-119">A client can request a conversation with a single server, or it can request multiple conversations with one or more servers.</span></span>

<span data-ttu-id="9d789-120">In den folgenden Themen wird beschrieben, wie eine Anwendung neue Konversationen herstellt und Informationen über vorhandene Konversationen abruft</span><span class="sxs-lookup"><span data-stu-id="9d789-120">The following topics describe how an application establishes new conversations and gets information about existing conversations.</span></span>

-   [<span data-ttu-id="9d789-121">Einzelne Konversationen</span><span class="sxs-lookup"><span data-stu-id="9d789-121">Single Conversations</span></span>](#single-conversations)
-   [<span data-ttu-id="9d789-122">Mehrere Konversationen</span><span class="sxs-lookup"><span data-stu-id="9d789-122">Multiple Conversations</span></span>](#multiple-conversations)

## <a name="single-conversations"></a><span data-ttu-id="9d789-123">Einzelne Konversationen</span><span class="sxs-lookup"><span data-stu-id="9d789-123">Single Conversations</span></span>

<span data-ttu-id="9d789-124">Eine Client Anwendung fordert eine einzelne Konversation mit einem Server durch Aufrufen der Funktion [**ddeconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) an und gibt Zeichen folgen Handles an, die die Zeichen folgen mit dem Dienstnamen der Serveranwendung und den Themen Namen für die Konversation angeben.</span><span class="sxs-lookup"><span data-stu-id="9d789-124">A client application requests a single conversation with a server by calling the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function and specifying string handles that identify the strings containing the service name of the server application and the topic name for the conversation.</span></span> <span data-ttu-id="9d789-125">Die Ddeml antwortet, indem die [**xtipp \_ Connect**](xtyp-connect.md) -Transaktion an die dynamischer Datenaustausch (DDE)-Rückruffunktion der einzelnen Server Anwendungen gesendet wird, die entweder einen Dienstnamen registriert haben, der mit dem in **ddeconnect** angegebenen übereinstimmt, oder die Dienst namens Filterung durch Aufrufen von [**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="9d789-125">The DDEML responds by sending the [**XTYP\_CONNECT**](xtyp-connect.md) transaction to the Dynamic Data Exchange (DDE) callback function of each server application that either has registered a service name that matches the one specified in **DdeConnect** or has turned service name filtering off by calling [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span></span> <span data-ttu-id="9d789-126">Ein Server kann **xtipp \_ Connect** -Transaktionen auch filtern, indem er \_ \_ in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion das Filter Flag für die CBF-Fehler Verbindungen angibt.</span><span class="sxs-lookup"><span data-stu-id="9d789-126">A server can also filter **XTYP\_CONNECT** transactions by specifying the CBF\_FAIL\_CONNECTIONS filter flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="9d789-127">Während der **xtipp \_ Connect** -Transaktion übergibt die Ddeml den Dienstnamen und den Themen Namen an den Server.</span><span class="sxs-lookup"><span data-stu-id="9d789-127">During the **XTYP\_CONNECT** transaction, the DDEML passes the service name and the topic name to the server.</span></span> <span data-ttu-id="9d789-128">Der Server muss die Namen überprüfen und **true** zurückgeben, wenn er das Paar aus Dienst Name und Themenname unterstützt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="9d789-128">The server must examine the names and return **TRUE** if it supports the service name and topic name pair or **FALSE** if it does not.</span></span>

<span data-ttu-id="9d789-129">Wenn kein Server positiv auf die Anforderung des Clients zum Herstellen einer Verbindung antwortet, empfängt der Client **null** von [**DDE Connect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) , und es wird keine Konversation eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="9d789-129">If no server responds positively to the client's request to connect, the client receives **NULL** from [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) and no conversation is established.</span></span> <span data-ttu-id="9d789-130">Wenn ein Server **true** zurückgibt, wird eine Konversation hergestellt, und der Client empfängt ein Konversations Handle – einem **DWORD** -Wert, der die Konversation identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9d789-130">If a server returns **TRUE**, a conversation is established and the client receives a conversation handle — a **DWORD** value that identifies the conversation.</span></span> <span data-ttu-id="9d789-131">Der Client verwendet das Handle in nachfolgenden Ddeml-aufrufen zum Abrufen von Daten vom Server.</span><span class="sxs-lookup"><span data-stu-id="9d789-131">The client uses the handle in subsequent DDEML calls to obtain data from the server.</span></span> <span data-ttu-id="9d789-132">Der Server empfängt die [**xtipp \_ Connect- \_ Bestätigungs**](xtyp-connect-confirm.md) Transaktion (es sei denn, der Server hat das Flag "CBF \_ Skip \_ Connect bestätigt Filter" angegeben \_ ).</span><span class="sxs-lookup"><span data-stu-id="9d789-132">The server receives the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction (unless the server specified the CBF\_SKIP\_CONNECT\_CONFIRMS filter flag).</span></span> <span data-ttu-id="9d789-133">Diese Transaktion übergibt das Konversations Handle an den Server.</span><span class="sxs-lookup"><span data-stu-id="9d789-133">This transaction passes the conversation handle to the server.</span></span>

<span data-ttu-id="9d789-134">Im folgenden Beispiel wird eine Konversation im Thema System mit einem Server angefordert, von dem der Dienst Name MyServer erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="9d789-134">The following example requests a conversation on the System topic with a server that recognizes the service name MyServer.</span></span> <span data-ttu-id="9d789-135">Die *hszservname* -und *hszsystop-Parameter* sind zuvor erstellte Zeichen folgen Handles.</span><span class="sxs-lookup"><span data-stu-id="9d789-135">The *hszServName* and *hszSysTopic* parameters are previously created string handles.</span></span>


```
HCONV hConv;         // conversation handle 
HWND hwndParent;     // parent window handle 
HSZ hszServName;     // service name string handle 
HSZ hszSysTopic;     // System topic string handle 
 
hConv = DdeConnect( 
    idInst,               // instance identifier 
    hszServName,          // service name string handle 
    hszSysTopic,          // System topic string handle 
    (PCONVCONTEXT) NULL); // use default context 
 
if (hConv == NULL) 
{ 
    MessageBox(hwndParent, "MyServer is unavailable.", 
        (LPSTR) NULL, MB_OK); 
    return FALSE; 
} 
```



<span data-ttu-id="9d789-136">Im vorherigen Beispiel bewirkt [**DDE Connect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) , dass die DDE-Rückruffunktion der MyServer-Anwendung eine [**XYP \_ Connect**](xtyp-connect.md) -Transaktion empfängt.</span><span class="sxs-lookup"><span data-stu-id="9d789-136">In the preceding example, [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) causes the DDE callback function of the MyServer application to receive an [**XTYP\_CONNECT**](xtyp-connect.md) transaction.</span></span>

<span data-ttu-id="9d789-137">Im folgenden Beispiel antwortet der Server auf die [**xtipp \_ Connect**](xtyp-connect.md) -Transaktion, indem er den Themen Namen String Handle der Ddeml vergleicht, die dem Server mit jedem Element in dem vom Server unterstützten Array von Themen namens Zeichen folgen behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="9d789-137">In the following example, the server responds to the [**XTYP\_CONNECT**](xtyp-connect.md) transaction by comparing the topic name string handle the DDEML passed to the server with each element in the array of topic name string handles the server supports.</span></span> <span data-ttu-id="9d789-138">Wenn der Server eine Suche findet, richtet er die Konversation ein.</span><span class="sxs-lookup"><span data-stu-id="9d789-138">If the server finds a match, it establishes the conversation.</span></span>


```
#define CTOPICS 5 
 
HSZ hsz1;                  // string handle passed by DDEML 
HSZ ahszTopics[CTOPICS];   // array of supported topics 
int i;                     // loop counter 
 
// Use a switch statement to examine transaction types. 
// Here is the connect case.
 
    case XTYP_CONNECT: 
        for (i = 0; i < CTOPICS; i++) 
        { 
            if (hsz1 == ahszTopics[i]) 
                return TRUE;   // establish a conversation 
        } 
 
        return FALSE; // Topic not supported; deny conversation.  
 
// Process other transaction types. 
```



<span data-ttu-id="9d789-139">Wenn der Server als Antwort auf die [**xtipp \_ Connect**](xtyp-connect.md) -Transaktion **true** zurückgibt, sendet die Ddeml eine [**xtipp \_ Connect- \_ Bestätigungs**](xtyp-connect-confirm.md) Transaktion an die DDE-Rückruffunktion des Servers.</span><span class="sxs-lookup"><span data-stu-id="9d789-139">If the server returns **TRUE** in response to the [**XTYP\_CONNECT**](xtyp-connect.md) transaction, the DDEML sends an [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server's DDE callback function.</span></span> <span data-ttu-id="9d789-140">Der Server kann das Handle für die Konversation abrufen, indem er diese Transaktion verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9d789-140">The server can obtain the handle to the conversation by processing this transaction.</span></span>

<span data-ttu-id="9d789-141">Ein Client kann eine Platzhalter Konversation einrichten, indem er **null** für den Dienstnamen-Zeichen folgen handle, den Themen Namen-Zeichen folgen handle oder beides in einem [**ddeconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)-aufrufswert angibt.</span><span class="sxs-lookup"><span data-stu-id="9d789-141">A client can establish a wildcard conversation by specifying **NULL** for the service name string handle, the topic name string handle, or both in a call to [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect).</span></span> <span data-ttu-id="9d789-142">Wenn mindestens einer der Zeichen folgen Handles **null** ist, sendet die Ddeml die XYP-Platzhalter-Transaktion an die Rückruf Funktionen aller DDE-Anwendungen (mit Ausnahme derjenigen, die die **XYP- \_ wildconnect** -Transaktion Filtern). [**\_**](xtyp-wildconnect.md)</span><span class="sxs-lookup"><span data-stu-id="9d789-142">If at least one of the string handles is **NULL**, the DDEML sends the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction to the callback functions of all DDE applications (except those that filter the **XTYP\_WILDCONNECT** transaction).</span></span> <span data-ttu-id="9d789-143">Jede Serveranwendung sollte Antworten, indem ein Daten Handle zurückgegeben wird, das ein mit Null endendes Array von [**hszpair**](/windows/win32/api/ddeml/ns-ddeml-hszpair) -Strukturen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9d789-143">Each server application should respond by returning a data handle that identifies a null-terminated array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="9d789-144">Wenn die Serveranwendung nicht " [**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) " aufgerufen hat, um die Dienstnamen zu registrieren, und wenn das Filtern auf on on ist, empfängt der Server keine **xType \_ wildconnect** -Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="9d789-144">If the server application has not called [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) to register its service names and if filtering is on, the server does not receive **XTYP\_WILDCONNECT** transactions.</span></span> <span data-ttu-id="9d789-145">Weitere Informationen zu Daten Handles finden Sie unter [Datenverwaltung](data-management.md).</span><span class="sxs-lookup"><span data-stu-id="9d789-145">For more information about data handles, see [Data Management](data-management.md).</span></span>

<span data-ttu-id="9d789-146">Das Array muss eine Struktur für jedes Paar aus Dienst Name und Themenname enthalten, das mit dem vom Client angegebenen paar übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="9d789-146">The array must contain one structure for each service name and topic name pair that matches the pair specified by the client.</span></span> <span data-ttu-id="9d789-147">Die Ddeml wählt eines der Paare aus, um eine Konversation einzurichten, und kehrt zum Client ein Handle zurück, das die Konversation identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9d789-147">The DDEML selects one of the pairs to establish a conversation and returns to the client a handle that identifies the conversation.</span></span> <span data-ttu-id="9d789-148">Die Ddeml sendet die [**xtipp \_ Connect- \_ Bestätigungs**](xtyp-connect-confirm.md) Transaktion an den Server (es sei denn, der Server filtert diese Transaktion).</span><span class="sxs-lookup"><span data-stu-id="9d789-148">The DDEML sends the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server (unless the server filters this transaction).</span></span> <span data-ttu-id="9d789-149">Das folgende Beispiel zeigt eine typische Serverantwort auf die [**\_ xtypisaconnect**](xtyp-wildconnect.md) -Transaktion.</span><span class="sxs-lookup"><span data-stu-id="9d789-149">The following example shows a typical server response to the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction.</span></span>


```
#define CTOPICS 2 
 
UINT uType; 
HSZPAIR ahszp[(CTOPICS + 1)]; 
HSZ ahszTopicList[CTOPICS]; 
HSZ hszServ, hszTopic; 
WORD i, j; 
 
if (uType == XTYP_WILDCONNECT) 
{ 
    // Scan the topic list and create an array of HSZPAIR structures. 
 
    j = 0; 
    for (i = 0; i < CTOPICS; i++) 
    { 
        if (hszTopic == (HSZ) NULL || 
                hszTopic == ahszTopicList[i]) 
        { 
            ahszp[j].hszSvc = hszServ; 
            ahszp[j++].hszTopic = ahszTopicList[i]; 
        } 
    } 
 
    // End the list with an HSZPAIR structure that contains NULL 
    // string handles as its members. 
 
    ahszp[j].hszSvc = NULL; 
    ahszp[j++].hszTopic = NULL; 
 
    // Return a handle to a global memory object containing the 
    // HSZPAIR structures. 
 
    return DdeCreateDataHandle( 
        idInst,          // instance identifier 
        (LPBYTE) &ahszp, // pointer to HSZPAIR array 
        sizeof(HSZ) * j, // length of the array 
        0,               // start at the beginning 
        (HSZ) NULL,      // no item name string 
        0,               // return the same format 
        0);              // let the system own it 
} 
```



<span data-ttu-id="9d789-150">Entweder der Client oder der Server kann eine Konversation jederzeit durch Aufrufen der [**ddedisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) -Funktion beenden.</span><span class="sxs-lookup"><span data-stu-id="9d789-150">Either the client or the server can terminate a conversation at any time by calling the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function.</span></span> <span data-ttu-id="9d789-151">Diese Funktion bewirkt, dass die Rückruffunktion des Partners in der Konversation die [**XYP \_**](xtyp-disconnect.md) -Trennungs Transaktion empfängt (es sei denn, der Partner hat das \_ filterflag "CBF Skip \_ disdisconnect" angegeben).</span><span class="sxs-lookup"><span data-stu-id="9d789-151">This function causes the callback function of the partner in the conversation to receive the [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transaction (unless the partner specified the CBF\_SKIP\_DISCONNECTS filter flag).</span></span> <span data-ttu-id="9d789-152">In der Regel antwortet eine Anwendung auf die " **XYP \_ Disconnect** "-Transaktion, indem Sie die [**ddequeryperformanfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) -Funktion verwendet, um Informationen über die beendete Konversation abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9d789-152">Typically, an application responds to the **XTYP\_DISCONNECT** transaction by using the [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) function to obtain information about the conversation that terminated.</span></span> <span data-ttu-id="9d789-153">Nachdem die Rückruffunktion die Verarbeitung der **XYP \_ Disconnect** -Transaktion zurückgegeben hat, ist das Konversations Handle nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="9d789-153">After the callback function returns from processing the **XTYP\_DISCONNECT** transaction, the conversation handle is no longer valid.</span></span>

<span data-ttu-id="9d789-154">Eine Client Anwendung, die eine [**XYP \_ Disconnect**](xtyp-disconnect.md) -Transaktion in der DDE-Rückruffunktion empfängt, kann versuchen, die Konversation durch Aufrufen der [**ddereconnetct**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) -Funktion wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="9d789-154">A client application that receives an [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transaction in its DDE callback function can attempt to reestablish the conversation by calling the [**DdeReconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) function.</span></span> <span data-ttu-id="9d789-155">Der Client muss **ddereconnetct** innerhalb seiner DDE-Rückruffunktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="9d789-155">The client must call **DdeReconnect** from within its DDE callback function.</span></span>

## <a name="multiple-conversations"></a><span data-ttu-id="9d789-156">Mehrere Konversationen</span><span class="sxs-lookup"><span data-stu-id="9d789-156">Multiple Conversations</span></span>

<span data-ttu-id="9d789-157">Eine Client Anwendung kann die [**DDE ConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) -Funktion verwenden, um zu bestimmen, ob relevante Server im System verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9d789-157">A client application can use the [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) function to determine whether any servers of interest are available in the system.</span></span> <span data-ttu-id="9d789-158">Ein Client gibt einen Dienstnamen und einen Themen Namen an, wenn er **ddeconnectlist** aufruft, wodurch die Ddeml die xttl-Transaktion an die DDE-Rückruf Funktionen aller Server sendet, die dem Dienstnamen entsprechen (außer denen, die die Transaktion Filtern). [**\_**](xtyp-wildconnect.md)</span><span class="sxs-lookup"><span data-stu-id="9d789-158">A client specifies a service name and topic name when it calls **DdeConnectList**, causing the DDEML to broadcast the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction to the DDE callback functions of all servers that match the service name (except those that filter the transaction).</span></span> <span data-ttu-id="9d789-159">Die Rückruffunktion eines Servers sollte ein Daten Handle zurückgeben, das ein mit Null endendes Array von [**hszpair**](/windows/win32/api/ddeml/ns-ddeml-hszpair) -Strukturen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9d789-159">A server's callback function should return a data handle that identifies a null-terminated array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="9d789-160">Das Array sollte eine Struktur für jedes Dienst Name-und Themen Namen Paar enthalten, das mit dem vom Client angegebenen paar übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="9d789-160">The array should contain one structure for each service name and topic name pair that matches the pair specified by the client.</span></span> <span data-ttu-id="9d789-161">Die Ddeml richtet eine Konversation für jede **hszpair** -Struktur ein, die vom Server ausgefüllt wird, und gibt ein Konversations Listen Handle an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="9d789-161">The DDEML establishes a conversation for each **HSZPAIR** structure filled by the server and returns a conversation list handle to the client.</span></span> <span data-ttu-id="9d789-162">Der Server empfängt das Konversations Handle über die [**XYP \_ Connect**](xtyp-connect.md) -Transaktion (es sei denn, der Server filtert diese Transaktion).</span><span class="sxs-lookup"><span data-stu-id="9d789-162">The server receives the conversation handle by way of the [**XTYP\_CONNECT**](xtyp-connect.md) transaction (unless the server filters this transaction).</span></span>

<span data-ttu-id="9d789-163">Ein Client kann **null** für den Dienstnamen, den Themen Namen oder beides angeben, wenn er [**ddeconnectlist**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)aufruft.</span><span class="sxs-lookup"><span data-stu-id="9d789-163">A client can specify **NULL** for the service name, topic name, or both when it calls [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="9d789-164">Wenn der Dienst Name **null** ist, reagieren alle Server im System, die den angegebenen Themen Namen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9d789-164">If the service name is **NULL**, all servers in the system that support the specified topic name respond.</span></span> <span data-ttu-id="9d789-165">Mit jedem antwortenden Server, einschließlich mehrerer Instanzen desselben Servers, wird eine Konversation eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="9d789-165">A conversation is established with each responding server, including multiple instances of the same server.</span></span> <span data-ttu-id="9d789-166">Wenn der Themenname **null** ist, wird für jedes Thema, das von jedem Server erkannt wird, der mit dem Dienstnamen übereinstimmt, eine Konversation eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="9d789-166">If the topic name is **NULL**, a conversation is established on each topic recognized by each server that matches the service name.</span></span>

<span data-ttu-id="9d789-167">Ein Client kann die [**ddequerynextserver**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) -Funktion und die [**ddequeryperformanfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) -Funktion verwenden, um die Server zu identifizieren, die auf [**ddeconnectlist**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)Antworten.</span><span class="sxs-lookup"><span data-stu-id="9d789-167">A client can use the [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) and [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) functions to identify the servers that respond to [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="9d789-168">**Ddequerynextserver** gibt das nächste Konversations Handle in einer Konversations Liste zurück, und **ddequeryüberzeugungs Info** füllt eine über [**zeugend**](/windows/win32/api/ddeml/ns-ddeml-convinfo) -Struktur mit Informationen über die Konversation aus.</span><span class="sxs-lookup"><span data-stu-id="9d789-168">**DdeQueryNextServer** returns the next conversation handle in a conversation list, and **DdeQueryConvInfo** fills a [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) structure with information about the conversation.</span></span> <span data-ttu-id="9d789-169">Der Client kann die von ihm benötigten Konversations Handles beibehalten und den Rest in der Konversations Liste verwerfen.</span><span class="sxs-lookup"><span data-stu-id="9d789-169">The client can keep the conversation handles that it needs and discard the rest from the conversation list.</span></span>

<span data-ttu-id="9d789-170">Im folgenden Beispiel wird [**ddeconnectlist**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) verwendet, um Konversationen mit allen Servern einzurichten, die das System Thema unterstützen. Anschließend werden die Funktionen [**ddequerynextserver**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) und [**ddequeryperformanfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) verwendet, um die Dienstnamen-Zeichen folgen Handles des Servers abzurufen und in einem Puffer zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9d789-170">The following example uses [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) to establish conversations with all servers that support the System topic and then uses the [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) and [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) functions to obtain the servers' service name string handles and store them in a buffer.</span></span>


```
HCONVLIST hconvList; // conversation list 
DWORD idInst;        // instance identifier 
HSZ hszSystem;       // System topic 
HCONV hconv = NULL;  // conversation handle 
CONVINFO ci;         // holds conversation data 
UINT cConv = 0;      // count of conv. handles 
HSZ *pHsz, *aHsz;    // point to string handles 
 
// Connect to all servers that support the System topic. 
 
hconvList = DdeConnectList(idInst, NULL, hszSystem, NULL, NULL); 
 
// Count the number of handles in the conversation list. 
 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
    cConv++; 
 
// Allocate a buffer for the string handles. 
 
hconv = NULL; 
aHsz = (HSZ *) LocalAlloc(LMEM_FIXED, cConv * sizeof(HSZ)); 
 
// Copy the string handles to the buffer. 
 
pHsz = aHsz; 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
{ 
    DdeQueryConvInfo(hconv, QID_SYNC, (PCONVINFO) &ci); 
    DdeKeepStringHandle(idInst, ci.hszSvcPartner); 
    *pHsz++ = ci.hszSvcPartner; 
} 
 
// Use the handles; converse with the servers. 
 
// Free the memory and terminate the conversations. 
 
LocalFree((HANDLE) aHsz); 
DdeDisconnectList(hconvList); 
```



<span data-ttu-id="9d789-171">Eine Anwendung kann eine einzelne Konversation in einer Konversations Liste durch Aufrufen der [**ddedisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) -Funktion beenden.</span><span class="sxs-lookup"><span data-stu-id="9d789-171">An application can terminate an individual conversation in a conversation list by calling the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function.</span></span> <span data-ttu-id="9d789-172">Eine Anwendung kann alle Konversationen in einer Konversations Liste durch Aufrufen der [**ddedisconnectlist**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) -Funktion beenden.</span><span class="sxs-lookup"><span data-stu-id="9d789-172">An application can terminate all conversations in a conversation list by calling the [**DdeDisconnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) function.</span></span> <span data-ttu-id="9d789-173">Beide Funktionen bewirken, dass die Ddeml [**XYP \_ Disconnect**](xtyp-disconnect.md) -Transaktionen an die DDE-Rückruffunktion der einzelnen Partner sendet.</span><span class="sxs-lookup"><span data-stu-id="9d789-173">Both functions cause the DDEML to send [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transactions to each partner's DDE callback function.</span></span> <span data-ttu-id="9d789-174">**DDE disconnectlist** sendet eine **XYP \_ Disconnect** -Transaktion für jedes Konversations Handle in der Liste.</span><span class="sxs-lookup"><span data-stu-id="9d789-174">**DdeDisconnectList** sends an **XTYP\_DISCONNECT** transaction for each conversation handle in the list.</span></span>

<span data-ttu-id="9d789-175">Ein Client kann eine Liste der Konversations Handles in einer Konversations Liste abrufen, indem er ein vorhandenes Konversations Listen Handle an [**DDE ConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)übergibt.</span><span class="sxs-lookup"><span data-stu-id="9d789-175">A client can retrieve a list of the conversation handles in a conversation list by passing an existing conversation list handle to [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="9d789-176">Der-enumerationsprozess entfernt die Handles von beendeten Konversationen aus der Liste, und nicht doppelte Konversationen, die dem angegebenen Dienstnamen und Themen Namen entsprechen, werden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9d789-176">The enumeration process removes the handles of terminated conversations from the list, and nonduplicate conversations that fit the specified service name and topic name are added.</span></span>

<span data-ttu-id="9d789-177">Wenn [**DDE ConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) ein vorhandenes Konversations Listen Handle angibt, erstellt die Funktion eine neue Konversations Liste, die die Handles aller neuen Konversationen und die Handles aus der vorhandenen Liste enthält.</span><span class="sxs-lookup"><span data-stu-id="9d789-177">If [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) specifies an existing conversation list handle, the function creates a new conversation list that contains the handles of any new conversations and the handles from the existing list.</span></span>

<span data-ttu-id="9d789-178">Wenn doppelte Konversationen vorhanden sind, versucht [**DDE ConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) , doppelte Konversations Handles in der Konversations Liste zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="9d789-178">If duplicate conversations exist, [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) attempts to prevent duplicate conversation handles in the conversation list.</span></span> <span data-ttu-id="9d789-179">Bei einer doppelten Konversation handelt es sich um eine zweite Konversation mit demselben Server unter demselben Dienstnamen und Themen Namen.</span><span class="sxs-lookup"><span data-stu-id="9d789-179">A duplicate conversation is a second conversation with the same server on the same service name and topic name.</span></span> <span data-ttu-id="9d789-180">Zwei dieser Konversationen hätten unterschiedliche Handles, aber Sie würden dieselbe Konversation identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9d789-180">Two such conversations would have different handles, yet they would identify the same conversation.</span></span>

 

 




