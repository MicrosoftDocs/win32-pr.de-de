---
title: Verwenden dynamische Daten Exchange
description: Dieses Thema enthält Codebeispiele zum dynamischen Datenaustausch.
ms.assetid: 6d94403b-64b4-4763-868a-3b94431dab79
keywords:
- dynamische Daten Exchange (DDE), Konversationen
- DDE (dynamische Daten Exchange),Konversationen
- Datenaustausch,dynamische Daten Exchange (DDE)
- dynamische Daten Exchange (DDE),Beispiele
- DDE (dynamische Daten Exchange),Beispiele
- dynamische Daten Exchange (DDE), Befehle in Serveranwendungen
- DDE (dynamische Daten Exchange),Befehle in Serveranwendungen
- dynamische Daten Exchange (DDE), Datenlinks
- DDE (dynamische Daten Exchange),Datenlinks
- dynamische Daten Exchange (DDE),items
- DDE (dynamische Daten Exchange),items
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3a279e02b65d5540e5494512a44eefdfecdb18607cb12731cf7daa0d8569de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953665"
---
# <a name="using-dynamic-data-exchange"></a>Verwenden dynamische Daten Exchange

Dieser Abschnitt enthält Codebeispiele für die folgenden Aufgaben:

-   [Initiieren einer Konversation](#initiating-a-conversation)
-   [Übertragen eines einzelnen Elements](#transferring-a-single-item)
    -   [Abrufen eines Elements vom Server](#retrieving-an-item-from-the-server)
    -   [Übermitteln eines Elements an den Server](#submitting-an-item-to-the-server)
-   [Einrichten eines permanenten Datenlinks](#establishing-a-permanent-data-link)
    -   [Initiieren eines Datenlinks](#initiating-a-data-link)
    -   [Initiieren eines Datenlinks mit dem Befehl "Link einfügen"](#initiating-a-data-link-with-the-paste-link-command)
    -   [Benachrichtigen des Clients über geänderte Daten](#notifying-the-client-that-data-has-changed)
    -   [Beenden eines Datenlinks](#terminating-a-data-link)
-   [Ausführen von Befehlen in einer Serveranwendung](#carrying-out-commands-in-a-server-application)
-   [Beenden einer Konversation](#terminating-a-conversation)

## <a name="initiating-a-conversation"></a>Initiieren einer Konversation

Zum Initiieren einer dynamische Daten Exchange (DDE) sendet der Client eine [**WM \_ DDE \_ INITIATE-Nachricht.**](wm-dde-initiate.md) In der Regel überträgt der Client diese Nachricht durch Aufrufen von [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)mit –1 als erstem Parameter. Wenn die Anwendung bereits über das Fensterhand handle für die Serveranwendung verfügt, kann sie die Nachricht direkt an dieses Fenster senden. Der Client bereitet Atome für den Anwendungs- und Themennamen vor, indem [**er GlobalAddAtom aufruft.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) Der Client kann Konversationen mit jeder potenziellen Serveranwendung  und für jedes potenzielle Thema anfordern, indem er NULL-Atome (Platzhalter) für die Anwendung und das Thema angibt.

Im folgenden Beispiel wird veranschaulicht, wie der Client eine Konversation initiiert, in der sowohl die Anwendung als auch das Thema angegeben werden.


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
> Wenn Ihre Anwendung **NULL-Atome** verwendet, müssen Sie nicht die [**Funktionen GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) und [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) verwenden. In diesem Beispiel erstellt die Clientanwendung zwei globale Atome, die den Namen des Servers bzw. des Themas enthalten.

 

Die Clientanwendung sendet eine [**WM \_ DDE \_ INITIATE-Nachricht**](wm-dde-initiate.md) mit diesen beiden Atomen im *lParam-Parameter* der Nachricht. Beim Aufruf der [**SendMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-sendmessage) leitet das spezielle Fensterhand handle –1 das System an, diese Nachricht an alle anderen aktiven Anwendungen zu senden. **SendMessage kehrt** erst an die Clientanwendung zurück, wenn alle Anwendungen, die die Nachricht empfangen, wiederum die Steuerung an das System zurückgegeben haben. Dies bedeutet, dass alle [**WM \_ DDE \_ ACK-Nachrichten,**](wm-dde-ack.md) die von den Serveranwendungen als Antwort gesendet werden, garantiert vom Client verarbeitet wurden, wenn der **SendMessage-Aufruf** zurückgegeben wurde.

Nachdem [**SendMessage zurückgegeben**](/windows/desktop/api/winuser/nf-winuser-sendmessage) wurde, löscht die Clientanwendung die globalen Atome.

Serveranwendungen reagieren entsprechend der Logik, die im folgenden Diagramm dargestellt ist.

![Antwortlogik der Serveranwendung](images/csdde-01.png)

Um ein oder mehrere Themen zu bestätigen, muss der Server Atome für jede Konversation erstellen (für die doppelte Atome des Anwendungsnamens erforderlich sind, wenn mehrere Themen vorhanden sind) und eine [**WM \_ DDE \_ ACK-Nachricht**](wm-dde-ack.md) für jede Konversation senden, wie im folgenden Beispiel veranschaulicht.


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



Wenn ein Server mit einer [**WM \_ DDE \_ ACK-Nachricht**](wm-dde-ack.md) antwortet, sollte die Clientanwendung ein Handle im Serverfenster speichern. Der Client, der das Handle als *wParam-Parameter* der **WM \_ DDE \_ ACK-Nachricht** empfängt, sendet dann alle nachfolgenden DDE-Nachrichten an das Serverfenster, das dieses Handle identifiziert.

Wenn Ihre Clientanwendung ein **NULL-Atom** für den Anwendungs- oder Themennamen verwendet, erwarten Sie, dass die Anwendung Bestätigungen von mehr als einer Serveranwendung erhält. Mehrere Bestätigungen können auch von mehreren Instanzen eines DDE-Servers stammen, auch wenn Ihre Clientanwendung keine **NULL-Atome** verwendet. Ein Server sollte immer ein eindeutiges Fenster für jede Konversation verwenden. Die Fensterprozedur in der Clientanwendung kann ein Handle für das Serverfenster (bereitgestellt als *lParam-Parameter* von [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)) verwenden, um mehrere Konversationen zu verfolgen. Dadurch kann ein einzelnes Clientfenster mehrere Konversationen verarbeiten, ohne dass für jede Konversation beendet und erneut eine Verbindung mit einem neuen Clientfenster hergestellt werden muss.

## <a name="transferring-a-single-item"></a>Übertragen eines einzelnen Elements

Nachdem eine DDE-Konversation eingerichtet wurde, kann der Client entweder den Wert eines Datenelements vom Server abrufen, indem er die [**WM \_ DDE \_ REQUEST-Nachricht**](wm-dde-request.md) ausstellen, oder einen Datenelementwert an den Server übermitteln, indem er [**WM \_ DDE \_ POKE**](wm-dde-poke.md)ausstellen.

-   [Abrufen eines Elements vom Server](#retrieving-an-item-from-the-server)
-   [Übermitteln eines Elements an den Server](#submitting-an-item-to-the-server)

### <a name="retrieving-an-item-from-the-server"></a>Abrufen eines Elements vom Server

Um ein Element vom Server abzurufen, sendet der Client dem Server eine [**WM \_ DDE \_ REQUEST-Nachricht,**](wm-dde-request.md) in der das abzurufende Element und Format angegeben werden, wie im folgenden Beispiel gezeigt.


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



In diesem Beispiel gibt der Client das Zwischenablageformat **CF \_ TEXT** als bevorzugtes Format für das angeforderte Datenelement an.

Der Empfänger (Server) der [**WM \_ DDE \_ REQUEST-Nachricht**](wm-dde-request.md) muss in der Regel das Elementatom löschen, aber wenn der [**PostMessage-Aufruf**](/windows/desktop/api/winuser/nf-winuser-postmessagea) fehlschlägt, muss der Client das Atom löschen.

Wenn der Server Zugriff auf das angeforderte Element hat und es im angeforderten Format rendern kann, kopiert der Server den Elementwert als Shared Memory-Objekt und sendet dem Client eine [**WM \_ DDE \_ DATA-Nachricht,**](wm-dde-data.md) wie im folgenden Beispiel veranschaulicht.


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



In diesem Beispiel ordnet die Serveranwendung ein Speicherobjekt zu, das das Datenelement enthalten soll. Das Datenobjekt wird als [**DDEDATA-Struktur**](/windows/desktop/api/Dde/ns-dde-ddedata) initialisiert.

Die Serveranwendung legt dann den **cfFormat-Member** der -Struktur auf CF TEXT fest, um die Clientanwendung darüber zu informieren, dass die Daten \_ im Textformat vorliegen. Der Client antwortet, indem er den Wert der angeforderten Daten in das **Value-Element** der [**DDEDATA-Struktur**](/windows/desktop/api/Dde/ns-dde-ddedata) kopiert. Nachdem der Server das Datenobjekt gefüllt hat, entsperrt der Server die Daten und erstellt ein globales Atom mit dem Namen des Datenelements.

Schließlich gibt der Server die [**WM \_ DDE \_ DATA-Nachricht aus,**](wm-dde-data.md) indem er [**PostMessage aufruft.**](/windows/desktop/api/winuser/nf-winuser-postmessagea) Das Handle für das Datenobjekt und das Atom, das den Elementnamen enthält, werden von der [**PackDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-packddelparam) in den *lParam-Parameter* der Nachricht gepackt.

Wenn [**PostMessage ausfällt,**](/windows/desktop/api/winuser/nf-winuser-postmessagea) muss der Server die [**FreeDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-freeddelparam) verwenden, um den gepackten *lParam-Parameter frei* zu geben. Der Server muss auch den gepackten *lParam-Parameter* für die empfangene [**WM \_ DDE \_ REQUEST-Nachricht**](wm-dde-request.md) freigibt.

Wenn der Server die Anforderung nicht erfüllen kann, sendet er eine negative [**WM \_ DDE \_ ACK-Nachricht**](wm-dde-ack.md) an den Client, wie im folgenden Beispiel gezeigt.


```
// Negative acknowledgment. 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 0, atomItem));
```



Beim Empfang einer [**WM \_ DDE \_ DATA-Nachricht**](wm-dde-data.md) verarbeitet der Client den Datenelementwert entsprechend. Wenn dann das **fAckReq-Mitglied,** auf das in der **WM \_ DDE \_ DATA-Nachricht** gezeigt wird, 1 ist, muss der Client dem Server eine positive [**WM \_ DDE \_ ACK-Nachricht**](wm-dde-ack.md) senden, wie im folgenden Beispiel gezeigt.


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



In diesem Beispiel untersucht der Client das Format der Daten. Wenn das Format nicht **CF \_ TEXT** ist (oder wenn der Client den Speicher für die Daten nicht sperren kann), sendet der Client eine negative [**WM \_ DDE \_ ACK-Meldung,**](wm-dde-ack.md) um anzugeben, dass die Daten nicht verarbeitet werden können. Wenn der Client ein Datenhand handle nicht sperren kann, da das Handle das **fAckReq-Mitglied** enthält, sollte der Client keine negative **WM \_ DDE \_ ACK-Nachricht** senden. Stattdessen sollte der Client die Konversation beenden.

Wenn ein Client als Antwort auf eine [**WM \_ DDE \_ DATA-Nachricht**](wm-dde-data.md) eine negative Bestätigung sendet, ist der Server dafür verantwortlich, den Arbeitsspeicher (aber nicht den *lParam-Parameter)* frei zu geben, auf den von der **WM \_ DDE \_ DATA-Nachricht** verwiesen wird, die der negativen Bestätigung zugeordnet ist.

Wenn die Daten verarbeitet werden können, überprüft der Client das **fAckReq-Element** der [**DDEDATA-Struktur,**](/windows/desktop/api/Dde/ns-dde-ddedata) um zu bestimmen, ob der Server angefordert hat, dass er darüber informiert wird, dass der Client die Daten erfolgreich empfangen und verarbeitet hat. Wenn der Server diese Informationen anfing, sendet der Client dem Server eine positive [**WM \_ DDE \_ ACK-Nachricht.**](wm-dde-ack.md)

Da das Entsperren von Daten den Zeiger auf die Daten ungültig macht, speichert der Client den Wert des **fRelease-Members,** bevor das Datenobjekt entsperrt wird. Nach dem Speichern des Werts überprüft der Client ihn, um zu ermitteln, ob die Serveranwendung den Client zum Freispeichern des Arbeitsspeichers mit den Daten aufgefordert hat. der Client verhält sich entsprechend.

Beim Empfang einer negativen [**WM \_ DDE \_ ACK-Meldung**](wm-dde-ack.md) kann der Client erneut denselben Elementwert angeben und dabei ein anderes Zwischenablageformat angeben. In der Regel fragt ein Client zunächst nach dem komplexesten Format, das er unterstützen kann, und geht dann bei Bedarf schrittweise einfachere Formate nach unten, bis er ein vom Server zur Verfügung stellen kann.

Wenn der Server das Formatelement des Systemthemas unterstützt, kann der Client bestimmen, welche Zwischenablageformate der Server unterstützt, anstatt sie bei jeder Anforderung eines Elements durch den Client zu bestimmen.

### <a name="submitting-an-item-to-the-server"></a>Übermitteln eines Elements an den Server

Der Client kann mithilfe der WM [**\_ DDE \_ POKE-Nachricht**](wm-dde-poke.md) einen Elementwert an den Server senden. Der Client rendert das zu sendende Element und sendet die **WM \_ DDE \_ POKE-Nachricht,** wie im folgenden Beispiel veranschaulicht.


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
> Das Senden von Daten mithilfe einer [**WM \_ DDE \_ POKE-Nachricht**](wm-dde-poke.md) ist im Wesentlichen identisch mit dem Senden mithilfe von [**WM \_ DDE \_ DATA,**](wm-dde-data.md)mit der Ausnahme, dass **WM \_ DDE \_ POKE** vom Client an den Server gesendet wird.

 

Wenn der Server den Datenelementwert im vom Client gerenderten Format akzeptieren kann, verarbeitet der Server den Elementwert entsprechend und sendet dem Client eine positive [**WM \_ DDE \_ ACK-Nachricht.**](wm-dde-ack.md) Wenn der Elementwert aufgrund seines Formats oder aus anderen Gründen nicht verarbeiten kann, sendet der Server dem Client eine negative **WM \_ DDE \_ ACK-Nachricht.**


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



In diesem Beispiel ruft der Server [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) auf, um den Namen des Elements abzurufen, das der Client gesendet hat. Der Server bestimmt dann, ob er das Element unterstützt und ob das Element im richtigen Format gerendert wird (d. h. CF \_ TEXT). Wenn das Element nicht unterstützt und nicht im richtigen Format gerendert wird oder der Server den Speicher für die Daten nicht sperren kann, sendet der Server eine negative Bestätigung zurück an die Clientanwendung. Beachten Sie, dass in diesem Fall das Senden einer negativen Bestätigung richtig ist, da bei [**WM \_ DDE \_ POKE-Nachrichten**](wm-dde-poke.md) immer davon ausgegangen wird, dass **der fAckReq-Member** festgelegt ist. Der Server sollte den Member ignorieren.

Wenn ein Server als Antwort auf eine [**WM \_ DDE \_ POKE-Nachricht**](wm-dde-poke.md) eine negative Bestätigung sendet, ist der Client dafür verantwortlich, den Arbeitsspeicher (aber nicht den *lParam-Parameter)* frei zu geben, auf den von der **WM \_ DDE \_ POKE-Nachricht** verwiesen wird, die der negativen Bestätigung zugeordnet ist.

## <a name="establishing-a-permanent-data-link"></a>Einrichten eines permanenten Datenlinks

Eine Clientanwendung kann DDE verwenden, um einen Link zu einem Element in einer Serveranwendung herzustellen. Nachdem ein solcher Link hergestellt wurde, sendet der Server regelmäßig Updates des verknüpften Elements an den Client, in der Regel immer dann, wenn sich der Wert des Elements ändert. Daher wird ein permanenter Datenstrom zwischen den beiden Anwendungen eingerichtet. Dieser Datenstrom bleibt bestehen, bis er explizit getrennt wird.

### <a name="initiating-a-data-link"></a>Initiieren eines Datenlinks

Der Client initiiert einen Datenlink, indem er eine [**WM \_ DDE \_ ADVISE-Nachricht**](wm-dde-advise.md) veröffentlicht, wie im folgenden Beispiel gezeigt.


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



In diesem Beispiel legt die Clientanwendung das **Flag fDeferUpd** der [**WM \_ DDE \_ ADVISE-Nachricht**](wm-dde-advise.md) auf **FALSE** fest. Dadurch wird die Serveranwendung aufgefordert, die Daten immer dann an den Client zu senden, wenn sich die Daten ändern.

Wenn der Server die [**WM \_ DDE \_ ADVISE-Anforderung**](wm-dde-advise.md) nicht bedienen kann, sendet er dem Client eine negative [**WM \_ \_ DDE-ACK-Nachricht.**](wm-dde-ack.md) Wenn der Server jedoch Zugriff auf das Element hat und es im angeforderten Format rendern kann, notiert der Server den neuen Link (ruft die im *hOptions-Parameter* angegebenen Flags ab) und sendet dem Client eine positive **WM \_ \_ DDE-ACK-Nachricht.** Von nun an sendet der Server die neuen Daten jedes Mal an den Client, wenn sich der Wert des Elements auf dem Server ändert, bis der Client eine entsprechende [**WM \_ DDE \_ UNADVISE-Nachricht**](wm-dde-unadvise.md) ausgibt.

Die [**WM \_ DDE \_ ADVISE-Nachricht**](wm-dde-advise.md) legt das Format der Daten fest, die während des Links ausgetauscht werden sollen. Wenn der Client versucht, einen anderen Link mit demselben Element herzustellen, aber ein anderes Datenformat verwendet, kann der Server das zweite Datenformat ablehnen oder versuchen, es zu unterstützen. Wenn für ein Beliebiges Datenelement ein warmer Link eingerichtet wurde, kann der Server jeweils nur ein Datenformat unterstützen. Dies liegt daran, dass die [**WM \_ DDE \_ DATA-Nachricht**](wm-dde-data.md) für einen warmen Link über ein **NULL-Datenhandle** verfügt, das andernfalls die Formatinformationen enthält. Daher muss ein Server alle warmen Links für ein element ablehnen, das bereits verknüpft ist, und alle Links für ein Element mit warmen Links ablehnen. Eine andere Interpretation kann sein, dass der Server das Format und den heißen oder warmen Zustand eines Links ändert, wenn ein zweiter Link für dasselbe Datenelement angefordert wird.

Im Allgemeinen sollten Clientanwendungen nicht versuchen, mehrere Verknüpfungen gleichzeitig für ein Datenelement herzustellen.

### <a name="initiating-a-data-link-with-the-paste-link-command"></a>Initiieren eines Datenlinks mit dem Befehl "Link einfügen"

Anwendungen, die heiße oder warme Datenlinks unterstützen, unterstützen in der Regel ein registriertes Zwischenablageformat mit dem Namen Link. Wenn dieses Zwischenablageformat den Befehlen "Link kopieren" und "Einfügen" der Anwendung zugeordnet ist, kann der Benutzer DDE-Konversationen zwischen Anwendungen einrichten, indem er einfach ein Datenelement in der Serveranwendung kopiert und in die Clientanwendung eingibt.

Eine Serveranwendung unterstützt das Format der Zwischenablage verknüpfen, indem sie in der Zwischenablage eine Zeichenfolge mit den Anwendungs-, Themen- und Elementnamen platziert, wenn der Benutzer im Menü **Bearbeiten** den Befehl **Kopieren** ausgibt. Im Folgenden ist das Standardformat Link dargestellt:

*application***\\ 0**_Thema_*_\\ 0_*_Element_*_\\ 0 \\ 0_*

Ein einzelnes NULL-Zeichen trennt die Namen, und zwei NULL-Zeichen beenden die gesamte Zeichenfolge.

Sowohl die Client- als auch die Serveranwendungen müssen das Format der Link-Zwischenablage registrieren, wie hier gezeigt:


```
cfLink = RegisterClipboardFormat("Link");
```



Eine Clientanwendung unterstützt das Format der Zwischenablage verknüpfen mithilfe eines Befehls Link einfügen im Menü Bearbeiten. Wenn der Benutzer diesen Befehl ausgibt, analysiert die Clientanwendung die Anwendungs-, Themen- und Elementnamen aus den Zwischenablagedaten im Linkformat. Mit diesen Namen initiiert die Clientanwendung eine Konversation für die Anwendung und das Thema, wenn eine solche Konversation noch nicht vorhanden ist. Die Clientanwendung sendet dann eine [**WM \_ DDE \_ ADVISE-Nachricht**](wm-dde-advise.md) an die Serveranwendung und gibt den Elementnamen an, der in den Daten der Zwischenablage im Linkformat enthalten ist.

Es folgt ein Beispiel für die Antwort einer Clientanwendung, wenn der Benutzer den Befehl Link einfügen ausgibt.


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



In diesem Beispiel öffnet die Clientanwendung die Zwischenablage und bestimmt, ob sie Daten im Zuvor registrierten Linkformat (cfLink) enthält. Andernfalls oder wenn die Daten in der Zwischenablage nicht gesperrt werden können, gibt der Client zurück.

Nachdem die Clientanwendung einen Zeiger auf die Zwischenablagedaten abgerufen hat, analysiert sie die Daten, um die Anwendungs-, Themen- und Elementnamen zu extrahieren.

Die Clientanwendung bestimmt, ob eine Konversation zu dem Thema bereits zwischen der Anwendung und der Serveranwendung vorhanden ist. Wenn eine Konversation vorhanden ist, überprüft der Client, ob für das Datenelement bereits ein Link vorhanden ist. Wenn ein solcher Link vorhanden ist, zeigt der Client dem Benutzer ein Meldungsfeld an. Andernfalls ruft sie eine eigene *SendAdvise-Funktion* auf, um eine [**WM \_ DDE \_ ADVISE-Nachricht**](wm-dde-advise.md) für das Element an den Server zu senden.

Wenn noch keine Konversation für das Thema zwischen client und server vorhanden ist, ruft der Client zunächst seine eigene *SendInitiate-Funktion* auf, um die [**WM \_ DDE \_ INITIATE-Nachricht**](wm-dde-initiate.md) zum Anfordern einer Konversation zu übertragen, und ruft dann seine eigene *FindServerGivenAppTopic-Funktion* auf, um die Konversation mit dem Fenster herzustellen, das im Namen der Serveranwendung antwortet. Nachdem die Konversation begonnen hat, ruft die Clientanwendung *SendAdvise* auf, um den Link anzufordern.

### <a name="notifying-the-client-that-data-has-changed"></a>Benachrichtigen des Clients, dass sich Daten geändert haben

Wenn der Client mithilfe der [**WM \_ DDE \_ ADVISE-Nachricht**](wm-dde-advise.md) einen Link herstellt und der **fDeferUpd-Member** in der [**DDEDATA-Struktur**](/windows/desktop/api/Dde/ns-dde-ddedata) nicht festgelegt ist (d. h. gleich 0), hat der Client angefordert, dass der Server das Datenelement jedes Mal sendet, wenn sich der Wert des Elements ändert. In solchen Fällen rendert der Server den neuen Wert des Datenelements im zuvor angegebenen Format und sendet dem Client eine [**WM \_ DDE \_ DATA-Nachricht,**](wm-dde-data.md) wie im folgenden Beispiel gezeigt.


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



In diesem Beispiel verarbeitet der Client den Elementwert nach Bedarf. Wenn das **fAckReq-Flag** für das Element festgelegt ist, sendet der Client dem Server eine positive [**WM \_ \_ DDE-ACK-Nachricht.**](wm-dde-ack.md)

Wenn der Client den Link mit dem festgelegten **fDeferUpd-Member** (d. h. gleich 1) herstellt, hat der Client angefordert, dass bei jeder Datenänderung nur eine Benachrichtigung gesendet wird, nicht die Daten selbst. Wenn sich der Elementwert in solchen Fällen ändert, rendert der Server den Wert nicht, sondern sendet dem Client einfach eine [**WM \_ DDE \_ DATA-Nachricht**](wm-dde-data.md) mit einem NULL-Datenhandle, wie im folgenden Beispiel veranschaulicht.


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



Bei Bedarf kann der Client den letzten Wert des Datenelements anfordern, indem er eine normale [**WM \_ DDE \_ REQUEST-Nachricht**](wm-dde-request.md) ausgibt, oder einfach den Hinweis vom Server ignorieren, dass sich die Daten geändert haben. Wenn **fAckReq** gleich 1 ist, wird vom Client in beiden Fällen erwartet, dass er eine positive [**WM \_ \_ DDE-ACK-Nachricht**](wm-dde-ack.md) an den Server sendet.

### <a name="terminating-a-data-link"></a>Beenden eines Datenlinks

Wenn der Client anfordert, dass ein bestimmter Datenlink beendet wird, sendet der Client dem Server eine [**WM \_ DDE \_ UNADVISE-Nachricht,**](wm-dde-unadvise.md) wie im folgenden Beispiel gezeigt.


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



Der Server überprüft, ob der Client derzeit über einen Link zu dem bestimmten Element in dieser Konversation verfügt. Wenn ein Link vorhanden ist, sendet der Server dem Client eine positive [**WM \_ \_ DDE-ACK-Nachricht.**](wm-dde-ack.md) Der Server muss dann keine Updates mehr über das Element senden. Wenn kein Link vorhanden ist, sendet der Server dem Client eine negative **WM \_ \_ DDE-ACK-Nachricht.**

Die [**WM \_ DDE \_ UNADVISE-Nachricht**](wm-dde-unadvise.md) gibt ein Datenformat an. Das Format 0 (null) weist den Server an, alle Links für das angegebene Element zu beenden, auch wenn mehrere hot-Links eingerichtet sind und jede ein anderes Format verwendet.

Um alle Links für eine Konversation zu beenden, sendet die Clientanwendung dem Server eine [**WM \_ DDE \_ UNADVISE-Nachricht**](wm-dde-unadvise.md) mit einem NULL-Element atom. Der Server bestimmt, ob für die Konversation derzeit mindestens ein Link eingerichtet ist. Wenn ein Link vorhanden ist, sendet der Server dem Client eine positive [**WM \_ \_ DDE-ACK-Nachricht.**](wm-dde-ack.md) Der Server muss dann keine Updates mehr in der Konversation senden. Wenn kein Link vorhanden ist, sendet der Server dem Client eine negative **WM \_ \_ DDE-ACK-Nachricht.**

## <a name="carrying-out-commands-in-a-server-application"></a>Ausführen von Befehlen in einer Serveranwendung

Anwendungen können die [**WM \_ DDE \_ EXECUTE-Nachricht**](wm-dde-execute.md) verwenden, um einen bestimmten Befehl oder eine Reihe von Befehlen in einer anderen Anwendung auszuführen. Dazu sendet der Client dem Server eine **WM \_ DDE \_ EXECUTE-Nachricht** mit einem Handle an eine Befehlszeichenfolge, wie im folgenden Beispiel gezeigt.


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



In diesem Beispiel versucht der Server, die angegebene Befehlszeichenfolge auszuführen. Wenn dies erfolgreich ist, sendet der Server dem Client eine positive [**WM \_ \_ DDE-ACK-Nachricht.**](wm-dde-ack.md) Andernfalls sendet er eine negative **WM \_ \_ DDE-ACK-Nachricht.** Diese **WM \_ \_ DDE-ACK-Nachricht** verwendet das *hCommand-Handle* wieder, das in der ursprünglichen [**WM \_ DDE \_ EXECUTE-Nachricht**](wm-dde-execute.md) übergeben wurde.

Wenn die Befehlsausführungszeichenfolge des Clients anfordert, dass der Server beendet wird, sollte der Server antworten, indem er eine positive [**WM \_ \_ DDE-ACK-Nachricht**](wm-dde-ack.md) sendet und dann eine [**WM \_ DDE \_ TERMINATE-Nachricht**](wm-dde-terminate.md) sendet, bevor er beendet wird. Alle anderen Befehle, die mit einer [**WM \_ DDE \_ EXECUTE-Nachricht**](wm-dde-execute.md) gesendet werden, sollten synchron ausgeführt werden. Das heißt, der Server sollte erst nach erfolgreichem Abschluss des Befehls eine **WM \_ \_ DDE-ACK-Nachricht** senden.

## <a name="terminating-a-conversation"></a>Beenden einer Konversation

Entweder der Client oder der Server kann eine [**WM \_ DDE \_ TERMINATE-Nachricht**](wm-dde-terminate.md) ausstellen, um eine Konversation jederzeit zu beenden. Auf ähnliche Weise sollten sowohl die Client- als auch die Serveranwendungen jederzeit darauf vorbereitet sein, diese Nachricht zu empfangen. Eine Anwendung muss alle Konversationen beenden, bevor sie heruntergefahren wird.

Im folgenden Beispiel sendet die Anwendung, die die Konversation beendet, eine [**WM \_ DDE \_ TERMINATE-Nachricht.**](wm-dde-terminate.md)


```
PostMessage(hwndServerDDE, WM_DDE_TERMINATE, 
    (WPARAM) hwndClientDDE, 0);
```



Dadurch wird die andere Anwendung darüber informiert, dass die sendende Anwendung keine weiteren Nachrichten sendet und der Empfänger das Fenster schließen kann. Es wird erwartet, dass der Empfänger in allen Fällen sofort antwortet, indem er eine [**WM \_ DDE \_ TERMINATE-Nachricht**](wm-dde-terminate.md) sendet. Der Empfänger darf keine negative, ausgelastete oder positive [**WM \_ \_ DDE-ACK-Nachricht**](wm-dde-ack.md) senden.

Nachdem eine Anwendung die [**WM \_ DDE \_ TERMINATE-Nachricht**](wm-dde-terminate.md) in einer DDE-Konversation an den Partner gesendet hat, darf sie nicht auf Nachrichten von diesem Partner reagieren, da der Partner möglicherweise das Fenster zerstört hat, an das die Antwort gesendet wird.

Wenn eine Anwendung nach dem Senden von **WM \_ DDE \_ TERMINATE** eine andere DDE-Nachricht als [**WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md) empfängt, sollte sie alle Objekte freigeben, die den empfangenen Nachrichten zugeordnet sind, mit Ausnahme der Datenhandles für [**WM \_ DDE \_ DATA-**](wm-dde-data.md) oder [**WM \_ DDE \_ BAGE-Nachrichten,**](wm-dde-poke.md) für die **kein** **fRelease-Member** festgelegt ist.

Wenn eine Anwendung beendet wird, sollten alle aktiven DDE-Konversationen beendet werden, bevor die Verarbeitung der [**WM \_ DESTROY-Nachricht**](/windows/desktop/winmsg/wm-destroy) abgeschlossen wird. Wenn eine Anwendung ihre aktiven DDE-Konversationen jedoch nicht beendet, beendet das System alle DDE-Konversationen, die einem Fenster zugeordnet sind, wenn das Fenster zerstört wird. Das folgende Beispiel zeigt, wie eine Serveranwendung alle DDE-Konversationen beendet.


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



 

 