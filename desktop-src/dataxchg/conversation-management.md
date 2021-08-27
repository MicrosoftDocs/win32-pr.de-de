---
title: Konversationsverwaltung
description: In diesem Thema werden Konversationen zwischen einem Client und einem Server erläutert.
ms.assetid: 4e5ff1a1-d46a-4e2a-a37c-8df951f2a1ee
keywords:
- Windows Benutzeroberfläche,dynamische Daten Exchange (DDE)
- dynamische Daten Exchange (DDE), Konversationen
- DDE (dynamische Daten Exchange),Konversationen
- Datenaustausch,dynamische Daten Exchange (DDE)
- Windows Benutzeroberfläche,dynamische Daten Exchange Management Library (DDEML)
- dynamische Daten Exchange Management Library (DDEML), Conversations
- DDEML (dynamische Daten Exchange Management Library), Conversations
- Datenaustausch,dynamische Daten Exchange Management Library (DDEML)
- dynamische Daten Exchange (DDE), mehrere Konversationen
- DDE (dynamische Daten Exchange),mehrere Konversationen
- dynamische Daten Exchange Management Library (DDEML), mehrere Konversationen
- DDEML (dynamische Daten Exchange Management Library), mehrere Konversationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3531cc396a3b4d0eca5d7c11e3677aec9ea2ee35dcdac110455daee252f798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991330"
---
# <a name="conversation-management"></a>Konversationsverwaltung

Eine Konversation zwischen einem Client und einem Server wird immer auf Anforderung des Clients hergestellt. Wenn eine Konversation hergestellt wird, erhält jeder Partner ein Handle, das die Konversation identifiziert. Die Partner verwenden dieses Handle in anderen funktionen dynamische Daten Exchange Management Library (DDEML), um Transaktionen zu senden und die Konversation zu verwalten. Ein Client kann eine Konversation mit einem einzelnen Server oder mehrere Konversationen mit einem oder mehreren Servern anfordern.

In den folgenden Themen wird beschrieben, wie eine Anwendung neue Konversationen erstellt und Informationen zu vorhandenen Konversationen erhält.

-   [Einzelne Konversationen](#single-conversations)
-   [Mehrere Konversationen](#multiple-conversations)

## <a name="single-conversations"></a>Einzelne Konversationen

Eine Clientanwendung fordert eine einzelne Konversation mit einem Server an, indem sie die [**DdeConnect-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) aufruft und Zeichenfolgenhandles angibt, die die Zeichenfolgen identifizieren, die den Dienstnamen der Serveranwendung und den Themennamen für die Konversation enthalten. Die DDEML antwortet, indem sie die [**XTYP \_ CONNECT-Transaktion**](xtyp-connect.md) an die dynamische Daten Exchange-Rückruffunktion (DDE) jeder Serveranwendung sendet, die entweder einen Dienstnamen registriert hat, der dem in **DdeConnect** angegebenen entspricht, oder die Dienstnamenfilterung durch Aufrufen von [**DdeNameService deaktiviert hat.**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) Ein Server kann **XTYP \_ CONNECT-Transaktionen** auch filtern, indem er das CBF FAIL CONNECTIONS-Filterflag \_ in der \_ [**DdeInitialize-Funktion anordnt.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Während der **XTYP \_ CONNECT-Transaktion** übergibt die DDEML den Dienstnamen und den Themennamen an den Server. Der Server muss die Namen überprüfen und **TRUE zurückgeben,** wenn er das Dienstnamen- und Themennamenpaar unterstützt, ander denn, er muss **FALSE** zurückgeben.

Wenn kein Server positiv auf die Verbindungsanforderung des Clients reagiert, empfängt der Client **NULL** von [**DdeConnect,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) und es wird keine Konversation hergestellt. Wenn ein Server **TRUE zurückgibt,** wird eine Konversation eingerichtet, und der Client empfängt ein Konversationshand handle – einen **DWORD-Wert,** der die Konversation identifiziert. Der Client verwendet das Handle in nachfolgenden DDEML-Aufrufen, um Daten vom Server zu erhalten. Der Server empfängt die [**XTYP \_ CONNECT \_ CONFIRM-Transaktion**](xtyp-connect-confirm.md) (es sei denn, der Server hat das FILTERflag CBF \_ SKIP CONNECT \_ \_ CONFIRMS angegeben). Diese Transaktion übergibt das Konversationshand handle an den Server.

Im folgenden Beispiel wird eine Konversation im Thema System mit einem Server, der den Dienstnamen MyServer erkennt, erforderlich. Die *Parameter hszServName* und *hszSysTopic sind* zuvor erstellte Zeichenfolgenhandles.


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



Im vorherigen Beispiel bewirkt [**DdeConnect,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) dass die DDE-Rückruffunktion der MyServer-Anwendung eine [**XTYP \_ CONNECT-Transaktion**](xtyp-connect.md) erhält.

Im folgenden Beispiel antwortet der Server auf die [**XTYP \_ CONNECT-Transaktion,**](xtyp-connect.md) indem er die Themennamenzeichenfolge vergleicht, die die an den Server übergebene DDEML mit jedem Element im Array von Themennamen-Zeichenfolgenhandles vergleicht, die der Server unterstützt. Wenn der Server eine Übereinstimmung findet, wird die Konversation hergestellt.


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



Wenn der Server **als** Antwort auf die [**XTYP \_ CONNECT-Transaktion**](xtyp-connect.md) TRUE zurückgibt, sendet die DDEML eine [**XTYP \_ CONNECT \_ CONFIRM-Transaktion**](xtyp-connect-confirm.md) an die DDE-Rückruffunktion des Servers. Der Server kann das Handle für die Konversation abrufen, indem er diese Transaktion verarbeitet.

Ein Client kann eine Platzhalter-Konversation einrichten, indem er **NULL** für das Zeichenfolgenhand handle des Dienstnamens, das Zeichenfolgenhand handle für den Themennamen oder beides in einem Aufruf von [**DdeConnect angibt.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) Wenn mindestens eines der Zeichenfolgenhandles **NULL** ist, sendet die DDEML die [**XTYP \_ WILDCONNECT-Transaktion**](xtyp-wildconnect.md) an die Rückruffunktionen aller DDE-Anwendungen (mit Ausnahme derer, die die **XTYP \_ WILDCONNECT-Transaktion filtern).** Jede Serveranwendung sollte reagieren, indem sie ein Datenhandl zurückgibt, das ein auf NULL beendetes Array von [**HSZPAIR-Strukturen**](/windows/win32/api/ddeml/ns-ddeml-hszpair) identifiziert. Wenn die Serveranwendung [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) nicht aufgerufen hat, um ihre Dienstnamen zu registrieren, und wenn filtert, erhält der Server keine **XTYP \_ WILDCONNECT-Transaktionen.** Weitere Informationen zu Datenhandles finden Sie unter [Datenverwaltung](data-management.md).

Das Array muss eine Struktur für jedes Dienstnamen- und Themennamenpaar enthalten, das dem vom Client angegebenen Paar entspricht. Die DDEML wählt eines der Paare aus, um eine Konversation zu erstellen, und gibt an den Client ein Handle zurück, das die Konversation identifiziert. Die DDEML sendet die [**XTYP \_ CONNECT \_ CONFIRM-Transaktion**](xtyp-connect-confirm.md) an den Server (es sei denn, der Server filtert diese Transaktion). Das folgende Beispiel zeigt eine typische Serverantwort auf die [**XTYP \_ WILDCONNECT-Transaktion.**](xtyp-wildconnect.md)


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



Entweder der Client oder der Server können eine Konversation jederzeit beenden, indem sie die [**DdeDisconnect-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) aufrufen. Diese Funktion bewirkt, dass die Rückruffunktion des Partners in der Konversation die [**XTYP \_ DISCONNECT-Transaktion**](xtyp-disconnect.md) erhält (es sei denn, der Partner hat das CBF \_ SKIP \_ DISCONNECTS-Filterflag angegeben). In der Regel antwortet eine Anwendung auf die **XTYP \_ DISCONNECT-Transaktion,** indem sie die [**DdeQueryConvInfo-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) verwendet, um Informationen über die beendete Konversation zu erhalten. Nachdem die Rückruffunktion von der Verarbeitung der **XTYP \_ DISCONNECT-Transaktion** zurückgegeben wurde, ist das Konversationshand handle nicht mehr gültig.

Eine Clientanwendung, die eine [**XTYP \_ DISCONNECT-Transaktion**](xtyp-disconnect.md) in ihrer DDE-Rückruffunktion empfängt, kann versuchen, die Konversation wiederherzustellen, indem sie die [**DdeReconnect-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) aufruft. Der Client muss **DdeReconnect innerhalb** seiner DDE-Rückruffunktion aufrufen.

## <a name="multiple-conversations"></a>Mehrere Konversationen

Eine Clientanwendung kann die [**DdeConnectList-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) verwenden, um zu bestimmen, ob im System andere Server verfügbar sind. Ein Client gibt einen Dienst- und Themennamen an, wenn **er DdeConnectList** aufruft. Dies führt dazu, dass die DDEML die [**XTYP \_ WILDCONNECT-Transaktion**](xtyp-wildconnect.md) an die DDE-Rückruffunktionen aller Server überträgt, die mit dem Dienstnamen übereinstimmen (mit Ausnahme der Server, die die Transaktion filtern). Die Rückruffunktion eines Servers sollte ein Datenhandl zurückgeben, das ein auf NULL beendetes Array von [**HSZPAIR-Strukturen identifiziert.**](/windows/win32/api/ddeml/ns-ddeml-hszpair) Das Array sollte eine Struktur für jedes Dienstnamen- und Themennamenpaar enthalten, das dem vom Client angegebenen Paar entspricht. Die DDEML richtet eine Konversation für jede vom Server gefüllte **HSZPAIR-Struktur** ein und gibt ein Konversationslistenhandle an den Client zurück. Der Server empfängt das Konversationshand handle über die [**XTYP \_ CONNECT-Transaktion**](xtyp-connect.md) (es sei denn, der Server filtert diese Transaktion).

Ein Client kann NULL **für** den Dienstnamen, den Themennamen oder beides angeben, wenn [**er DdeConnectList aufruft.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) Wenn der Dienstname **NULL ist,** antworten alle Server im System, die den angegebenen Themennamen unterstützen. Eine Konversation wird mit jedem antwortenden Server hergestellt, einschließlich mehrerer Instanzen desselben Servers. Wenn der Themenname **NULL ist,** wird eine Konversation für jedes Thema eingerichtet, das von jedem Server erkannt wird, der dem Dienstnamen entspricht.

Ein Client kann die [**Funktionen DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) und [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) verwenden, um die Server zu identifizieren, die auf [**DdeConnectList reagieren.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) **DdeQueryNextServer** gibt das nächste Konversationshand handle in einer Konversationsliste zurück, und **DdeQueryConvInfo** füllt eine [**CONVINFO-Struktur**](/windows/win32/api/ddeml/ns-ddeml-convinfo) mit Informationen zur Konversation auf. Der Client kann die benötigten Konversationshandles behalten und den Rest aus der Konversationsliste verwerfen.

Im folgenden Beispiel wird [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) verwendet, um Konversationen mit allen Servern herzustellen, die das Systemthema unterstützen. Anschließend werden die Funktionen [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) und [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) verwendet, um die Dienstnamen-Zeichenfolgenhandles der Server zu erhalten und in einem Puffer zu speichern.


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



Eine Anwendung kann eine einzelne Konversation in einer Konversationsliste beenden, indem sie die [**DdeDisconnect-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) aufruft. Eine Anwendung kann alle Konversationen in einer Konversationsliste beenden, indem sie die [**DdeDisconnectList-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) aufruft. Beide Funktionen bewirken, dass die DDEML [**XTYP \_ DISCONNECT-Transaktionen**](xtyp-disconnect.md) an die DDE-Rückruffunktion jedes Partners sendet. **DdeDisconnectList sendet** eine **XTYP \_ DISCONNECT-Transaktion** für jedes Konversationshand handle in der Liste.

Ein Client kann eine Liste der Konversationshandles in einer Konversationsliste abrufen, indem ein vorhandenes Konversationslistenhandles an [**DdeConnectList übergeben wird.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) Der Enumerationsprozess entfernt die Handles beendeter Konversationen aus der Liste, und nicht duplizierte Konversationen, die dem angegebenen Dienstnamen und Themennamen passen, werden hinzugefügt.

Wenn [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) ein vorhandenes Konversationslistenhandles angibt, erstellt die Funktion eine neue Konversationsliste, die die Handles aller neuen Konversationen und die Handles aus der vorhandenen Liste enthält.

Wenn doppelte Konversationen vorhanden sind, [**versucht DdeConnectList,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) doppelte Konversationshandles in der Konversationsliste zu verhindern. Eine doppelte Konversation ist eine zweite Konversation mit demselben Server unter demselben Dienstnamen und Themennamen. Zwei solche Konversationen würden unterschiedliche Handles haben, aber sie würden dieselbe Konversation identifizieren.

 

 




