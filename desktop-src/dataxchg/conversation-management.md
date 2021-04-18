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
# <a name="conversation-management"></a>Konversations Verwaltung

Eine Konversation zwischen einem Client und einem Server wird immer bei der Client Anforderung eingerichtet. Wenn eine Konversation eingerichtet wird, erhält jeder Partner ein Handle, das die Konversation identifiziert. Die Partner verwenden dieses Handle in anderen Ddeml-Funktionen (dynamischer Datenaustausch Management Library), um Transaktionen zu senden und die Konversation zu verwalten. Ein Client kann eine Konversation mit einem einzelnen Server anfordern oder mehrere Konversationen mit einem oder mehreren Servern anfordern.

In den folgenden Themen wird beschrieben, wie eine Anwendung neue Konversationen herstellt und Informationen über vorhandene Konversationen abruft

-   [Einzelne Konversationen](#single-conversations)
-   [Mehrere Konversationen](#multiple-conversations)

## <a name="single-conversations"></a>Einzelne Konversationen

Eine Client Anwendung fordert eine einzelne Konversation mit einem Server durch Aufrufen der Funktion [**ddeconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) an und gibt Zeichen folgen Handles an, die die Zeichen folgen mit dem Dienstnamen der Serveranwendung und den Themen Namen für die Konversation angeben. Die Ddeml antwortet, indem die [**xtipp \_ Connect**](xtyp-connect.md) -Transaktion an die dynamischer Datenaustausch (DDE)-Rückruffunktion der einzelnen Server Anwendungen gesendet wird, die entweder einen Dienstnamen registriert haben, der mit dem in **ddeconnect** angegebenen übereinstimmt, oder die Dienst namens Filterung durch Aufrufen von [**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)aktiviert hat. Ein Server kann **xtipp \_ Connect** -Transaktionen auch filtern, indem er \_ \_ in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion das Filter Flag für die CBF-Fehler Verbindungen angibt. Während der **xtipp \_ Connect** -Transaktion übergibt die Ddeml den Dienstnamen und den Themen Namen an den Server. Der Server muss die Namen überprüfen und **true** zurückgeben, wenn er das Paar aus Dienst Name und Themenname unterstützt, andernfalls **false** .

Wenn kein Server positiv auf die Anforderung des Clients zum Herstellen einer Verbindung antwortet, empfängt der Client **null** von [**DDE Connect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) , und es wird keine Konversation eingerichtet. Wenn ein Server **true** zurückgibt, wird eine Konversation hergestellt, und der Client empfängt ein Konversations Handle – einem **DWORD** -Wert, der die Konversation identifiziert. Der Client verwendet das Handle in nachfolgenden Ddeml-aufrufen zum Abrufen von Daten vom Server. Der Server empfängt die [**xtipp \_ Connect- \_ Bestätigungs**](xtyp-connect-confirm.md) Transaktion (es sei denn, der Server hat das Flag "CBF \_ Skip \_ Connect bestätigt Filter" angegeben \_ ). Diese Transaktion übergibt das Konversations Handle an den Server.

Im folgenden Beispiel wird eine Konversation im Thema System mit einem Server angefordert, von dem der Dienst Name MyServer erkannt wird. Die *hszservname* -und *hszsystop-Parameter* sind zuvor erstellte Zeichen folgen Handles.


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



Im vorherigen Beispiel bewirkt [**DDE Connect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) , dass die DDE-Rückruffunktion der MyServer-Anwendung eine [**XYP \_ Connect**](xtyp-connect.md) -Transaktion empfängt.

Im folgenden Beispiel antwortet der Server auf die [**xtipp \_ Connect**](xtyp-connect.md) -Transaktion, indem er den Themen Namen String Handle der Ddeml vergleicht, die dem Server mit jedem Element in dem vom Server unterstützten Array von Themen namens Zeichen folgen behandelt wird. Wenn der Server eine Suche findet, richtet er die Konversation ein.


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



Wenn der Server als Antwort auf die [**xtipp \_ Connect**](xtyp-connect.md) -Transaktion **true** zurückgibt, sendet die Ddeml eine [**xtipp \_ Connect- \_ Bestätigungs**](xtyp-connect-confirm.md) Transaktion an die DDE-Rückruffunktion des Servers. Der Server kann das Handle für die Konversation abrufen, indem er diese Transaktion verarbeitet.

Ein Client kann eine Platzhalter Konversation einrichten, indem er **null** für den Dienstnamen-Zeichen folgen handle, den Themen Namen-Zeichen folgen handle oder beides in einem [**ddeconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)-aufrufswert angibt. Wenn mindestens einer der Zeichen folgen Handles **null** ist, sendet die Ddeml die XYP-Platzhalter-Transaktion an die Rückruf Funktionen aller DDE-Anwendungen (mit Ausnahme derjenigen, die die **XYP- \_ wildconnect** -Transaktion Filtern). [**\_**](xtyp-wildconnect.md) Jede Serveranwendung sollte Antworten, indem ein Daten Handle zurückgegeben wird, das ein mit Null endendes Array von [**hszpair**](/windows/win32/api/ddeml/ns-ddeml-hszpair) -Strukturen identifiziert. Wenn die Serveranwendung nicht " [**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) " aufgerufen hat, um die Dienstnamen zu registrieren, und wenn das Filtern auf on on ist, empfängt der Server keine **xType \_ wildconnect** -Transaktionen. Weitere Informationen zu Daten Handles finden Sie unter [Datenverwaltung](data-management.md).

Das Array muss eine Struktur für jedes Paar aus Dienst Name und Themenname enthalten, das mit dem vom Client angegebenen paar übereinstimmt. Die Ddeml wählt eines der Paare aus, um eine Konversation einzurichten, und kehrt zum Client ein Handle zurück, das die Konversation identifiziert. Die Ddeml sendet die [**xtipp \_ Connect- \_ Bestätigungs**](xtyp-connect-confirm.md) Transaktion an den Server (es sei denn, der Server filtert diese Transaktion). Das folgende Beispiel zeigt eine typische Serverantwort auf die [**\_ xtypisaconnect**](xtyp-wildconnect.md) -Transaktion.


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



Entweder der Client oder der Server kann eine Konversation jederzeit durch Aufrufen der [**ddedisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) -Funktion beenden. Diese Funktion bewirkt, dass die Rückruffunktion des Partners in der Konversation die [**XYP \_**](xtyp-disconnect.md) -Trennungs Transaktion empfängt (es sei denn, der Partner hat das \_ filterflag "CBF Skip \_ disdisconnect" angegeben). In der Regel antwortet eine Anwendung auf die " **XYP \_ Disconnect** "-Transaktion, indem Sie die [**ddequeryperformanfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) -Funktion verwendet, um Informationen über die beendete Konversation abzurufen. Nachdem die Rückruffunktion die Verarbeitung der **XYP \_ Disconnect** -Transaktion zurückgegeben hat, ist das Konversations Handle nicht mehr gültig.

Eine Client Anwendung, die eine [**XYP \_ Disconnect**](xtyp-disconnect.md) -Transaktion in der DDE-Rückruffunktion empfängt, kann versuchen, die Konversation durch Aufrufen der [**ddereconnetct**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) -Funktion wiederherzustellen. Der Client muss **ddereconnetct** innerhalb seiner DDE-Rückruffunktion abrufen.

## <a name="multiple-conversations"></a>Mehrere Konversationen

Eine Client Anwendung kann die [**DDE ConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) -Funktion verwenden, um zu bestimmen, ob relevante Server im System verfügbar sind. Ein Client gibt einen Dienstnamen und einen Themen Namen an, wenn er **ddeconnectlist** aufruft, wodurch die Ddeml die xttl-Transaktion an die DDE-Rückruf Funktionen aller Server sendet, die dem Dienstnamen entsprechen (außer denen, die die Transaktion Filtern). [**\_**](xtyp-wildconnect.md) Die Rückruffunktion eines Servers sollte ein Daten Handle zurückgeben, das ein mit Null endendes Array von [**hszpair**](/windows/win32/api/ddeml/ns-ddeml-hszpair) -Strukturen identifiziert. Das Array sollte eine Struktur für jedes Dienst Name-und Themen Namen Paar enthalten, das mit dem vom Client angegebenen paar übereinstimmt. Die Ddeml richtet eine Konversation für jede **hszpair** -Struktur ein, die vom Server ausgefüllt wird, und gibt ein Konversations Listen Handle an den Client zurück. Der Server empfängt das Konversations Handle über die [**XYP \_ Connect**](xtyp-connect.md) -Transaktion (es sei denn, der Server filtert diese Transaktion).

Ein Client kann **null** für den Dienstnamen, den Themen Namen oder beides angeben, wenn er [**ddeconnectlist**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)aufruft. Wenn der Dienst Name **null** ist, reagieren alle Server im System, die den angegebenen Themen Namen unterstützen. Mit jedem antwortenden Server, einschließlich mehrerer Instanzen desselben Servers, wird eine Konversation eingerichtet. Wenn der Themenname **null** ist, wird für jedes Thema, das von jedem Server erkannt wird, der mit dem Dienstnamen übereinstimmt, eine Konversation eingerichtet.

Ein Client kann die [**ddequerynextserver**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) -Funktion und die [**ddequeryperformanfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) -Funktion verwenden, um die Server zu identifizieren, die auf [**ddeconnectlist**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)Antworten. **Ddequerynextserver** gibt das nächste Konversations Handle in einer Konversations Liste zurück, und **ddequeryüberzeugungs Info** füllt eine über [**zeugend**](/windows/win32/api/ddeml/ns-ddeml-convinfo) -Struktur mit Informationen über die Konversation aus. Der Client kann die von ihm benötigten Konversations Handles beibehalten und den Rest in der Konversations Liste verwerfen.

Im folgenden Beispiel wird [**ddeconnectlist**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) verwendet, um Konversationen mit allen Servern einzurichten, die das System Thema unterstützen. Anschließend werden die Funktionen [**ddequerynextserver**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) und [**ddequeryperformanfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) verwendet, um die Dienstnamen-Zeichen folgen Handles des Servers abzurufen und in einem Puffer zu speichern.


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



Eine Anwendung kann eine einzelne Konversation in einer Konversations Liste durch Aufrufen der [**ddedisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) -Funktion beenden. Eine Anwendung kann alle Konversationen in einer Konversations Liste durch Aufrufen der [**ddedisconnectlist**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) -Funktion beenden. Beide Funktionen bewirken, dass die Ddeml [**XYP \_ Disconnect**](xtyp-disconnect.md) -Transaktionen an die DDE-Rückruffunktion der einzelnen Partner sendet. **DDE disconnectlist** sendet eine **XYP \_ Disconnect** -Transaktion für jedes Konversations Handle in der Liste.

Ein Client kann eine Liste der Konversations Handles in einer Konversations Liste abrufen, indem er ein vorhandenes Konversations Listen Handle an [**DDE ConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)übergibt. Der-enumerationsprozess entfernt die Handles von beendeten Konversationen aus der Liste, und nicht doppelte Konversationen, die dem angegebenen Dienstnamen und Themen Namen entsprechen, werden hinzugefügt.

Wenn [**DDE ConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) ein vorhandenes Konversations Listen Handle angibt, erstellt die Funktion eine neue Konversations Liste, die die Handles aller neuen Konversationen und die Handles aus der vorhandenen Liste enthält.

Wenn doppelte Konversationen vorhanden sind, versucht [**DDE ConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) , doppelte Konversations Handles in der Konversations Liste zu verhindern. Bei einer doppelten Konversation handelt es sich um eine zweite Konversation mit demselben Server unter demselben Dienstnamen und Themen Namen. Zwei dieser Konversationen hätten unterschiedliche Handles, aber Sie würden dieselbe Konversation identifizieren.

 

 




