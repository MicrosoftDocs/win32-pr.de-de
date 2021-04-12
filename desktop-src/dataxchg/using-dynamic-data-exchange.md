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
# <a name="using-dynamic-data-exchange"></a>Verwenden von dynamischer Datenaustausch

Dieser Abschnitt enthält Codebeispiele zu den folgenden Aufgaben:

-   [Initiieren einer Konversation](#initiating-a-conversation)
-   [Übertragen eines einzelnen Elements](#transferring-a-single-item)
    -   [Abrufen eines Elements vom Server](#retrieving-an-item-from-the-server)
    -   [Ein Element wird an den Server übermittelt.](#submitting-an-item-to-the-server)
-   [Einrichten einer permanenten Datenverknüpfung](#establishing-a-permanent-data-link)
    -   [Initiieren einer Datenverknüpfung](#initiating-a-data-link)
    -   [Initiieren einer Datenverknüpfung mit dem Befehl "Link einfügen"](#initiating-a-data-link-with-the-paste-link-command)
    -   [Benachrichtigen des Clients, dass sich Daten geändert haben](#notifying-the-client-that-data-has-changed)
    -   [Beenden eines Daten Links](#terminating-a-data-link)
-   [Ausführen von Befehlen in einer Server Anwendung](#carrying-out-commands-in-a-server-application)
-   [Beenden einer Konversation](#terminating-a-conversation)

## <a name="initiating-a-conversation"></a>Initiieren einer Konversation

Zum Initiieren einer dynamischer Datenaustausch (DDE)-Konversation sendet der Client eine " [**WM DDE"- \_ \_ Initiierungs**](wm-dde-initiate.md) Nachricht. Normalerweise überträgt der Client diese Nachricht, indem [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)aufgerufen wird, wobei – 1 als erster Parameter angegeben wird. Wenn die Anwendung bereits über das Fenster Handle für die Serveranwendung verfügt, kann Sie die Nachricht direkt an dieses Fenster senden. Der Client bereitet Atome für den Anwendungsnamen und den Themen Namen vor, indem [**Global addatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)aufgerufen wird. Der Client kann Konversationen mit jeder potenziellen Serveranwendung und für jedes beliebige mögliche Thema anfordern, indem er **null** -(Platzhalter) Atome für die Anwendung und das Thema bereitstellt.

Im folgenden Beispiel wird veranschaulicht, wie der Client eine Konversation initiiert, wobei sowohl die Anwendung als auch das Thema angegeben werden.


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
> Wenn Ihre Anwendung **null** -Atome verwendet, müssen Sie nicht die Funktionen [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) und [**globaldeleteatom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) verwenden. In diesem Beispiel erstellt die Client Anwendung zwei globale Atome, die den Namen des Servers und den Namen des Themas enthalten.

 

Die Client Anwendung sendet eine [**WM- \_ DDE- \_ Initiierungs**](wm-dde-initiate.md) Nachricht mit diesen beiden Atomen im *LPARAM* -Parameter der Nachricht. Beim Abrufen der [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion weist das besondere Fenster Handle – 1 das System an, diese Nachricht an alle anderen aktiven Anwendungen zu senden. **SendMessage** kehrt nicht an die Client Anwendung zurück, bis alle Anwendungen, die die Nachricht empfangen, wiederum die Steuerung an das System zurückgegeben haben. Dies bedeutet, dass alle von den Server Anwendungen gesendeten [**WM- \_ DDE- \_ ACK**](wm-dde-ack.md) -Nachrichten vom Client bis zu dem Zeitpunkt verarbeitet wurden, an dem der **SendMessage** -Aufruf zurückgegeben wurde.

Nachdem [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) zurückgegeben wurde, löscht die Client Anwendung die globalen Atome.

Server Anwendungen reagieren gemäß der im folgenden Diagramm dargestellten Logik.

![Antwort Logik der Serveranwendung](images/csdde-01.png)

Um ein oder mehrere Themen zu bestätigen, muss der Server Atome für jede Konversation erstellen (erfordert doppelte Anwendungsnamen Atome, wenn mehrere Themen vorhanden sind) und eine [**WM \_ DDE \_ ACK**](wm-dde-ack.md) -Nachricht für jede Konversation senden, wie im folgenden Beispiel veranschaulicht.


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



Wenn ein Server mit der Meldung " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) " antwortet, sollte die Client Anwendung ein Handle im Server Fenster speichern. Der Client, der das Handle als *wParam* -Parameter der **WM \_ DDE \_ ACK** -Nachricht empfängt, sendet dann alle nachfolgenden DDE-Nachrichten an das Server Fenster, das von diesem Handle identifiziert wird.

Wenn Ihre Client Anwendung ein **null** -Atom für den Anwendungsnamen oder den Themen Namen verwendet, erwarten Sie, dass die Anwendung Bestätigungen von mehr als einer Serveranwendung empfängt. Mehrere Bestätigungen können auch von mehreren Instanzen eines DDE-Servers stammen, auch wenn Ihre Client Anwendung keine **Atome verwendet.** Ein Server sollte für jede Konversation immer ein eindeutiges Fenster verwenden. Die Fenster Prozedur in der Client Anwendung kann ein Handle für das Server Fenster (bereitgestellt als *LPARAM* -Parameter von [**WM \_ DDE \_ initiieren**](wm-dde-initiate.md)) verwenden, um mehrere Konversationen zu verfolgen. Dies ermöglicht es einem einzelnen Client Fenster, mehrere Konversationen zu verarbeiten, ohne dass eine Verbindung mit einem neuen Client Fenster für jede Konversation hergestellt werden muss.

## <a name="transferring-a-single-item"></a>Übertragen eines einzelnen Elements

Nachdem eine DDE-Konversation eingerichtet wurde, kann der Client entweder den Wert eines Datenelements vom Server abrufen, indem er die [**WM- \_ DDE- \_ Anforderungs**](wm-dde-request.md) Nachricht ausgibt, oder einen Datenelement Wert an den Server übermitteln, indem [**WM \_ DDE \_ Poke**](wm-dde-poke.md)ausgegeben wird.

-   [Abrufen eines Elements vom Server](#retrieving-an-item-from-the-server)
-   [Ein Element wird an den Server übermittelt.](#submitting-an-item-to-the-server)

### <a name="retrieving-an-item-from-the-server"></a>Abrufen eines Elements vom Server

Zum Abrufen eines Elements vom Server sendet der Client dem Server eine WM- [**\_ DDE- \_ Anforderungs**](wm-dde-request.md) Nachricht, die das abzurufende Element und Format angibt, wie im folgenden Beispiel gezeigt.


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



In diesem Beispiel gibt der Client den **CF- \_ Text** des Zwischenablage Formats als bevorzugtes Format für das angeforderte Datenelement an.

Der Empfänger (Server) der [**WM- \_ DDE- \_ Anforderungs**](wm-dde-request.md) Nachricht muss das Element Atom in der Regel löschen, aber wenn der [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Rückruf fehlschlägt, muss der Client das Atom löschen.

Wenn der Server Zugriff auf das angeforderte Element hat und ihn im angeforderten Format rendert, kopiert der Server den Elementwert als frei gegebenes Speicher Objekt und sendet dem Client eine [**WM \_ DDE- \_ Daten**](wm-dde-data.md) Nachricht, wie im folgenden Beispiel veranschaulicht.


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



In diesem Beispiel weist die Serveranwendung ein Speicher Objekt zu, das das Datenelement enthalten soll. Das Datenobjekt wird als [**DDE Data**](/windows/desktop/api/Dde/ns-dde-ddedata) -Struktur initialisiert.

Die Serveranwendung legt dann den **cfFormat** -Member der Struktur auf CF \_ Text fest, um der Client Anwendung mitzuteilen, dass die Daten im Text Format vorliegen. Der Client antwortet, indem er den Wert der angeforderten Daten in das **Wertmember** der [**DDE Data**](/windows/desktop/api/Dde/ns-dde-ddedata) -Struktur kopiert. Nachdem der Server das Datenobjekt ausgefüllt hat, entsperrt der Server die Daten und erstellt ein globales Atom, das den Namen des Datenelements enthält.

Schließlich gibt der Server die [**WM \_ DDE- \_ Daten**](wm-dde-data.md) Nachricht durch Aufrufen von [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)aus. Das Handle für das Datenobjekt und das Atom mit dem Elementnamen werden von der [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) -Funktion in den *LPARAM* -Parameter der Nachricht gepackt.

Wenn [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) fehlschlägt, muss der Server die [**freeddelta param**](/windows/desktop/api/Dde/nf-dde-freeddelparam) -Funktion verwenden, um den gepackten *LPARAM* -Parameter freizugeben. Der Server muss auch den gepackten *LPARAM* -Parameter für die empfangene [**WM- \_ DDE- \_ Anforderungs**](wm-dde-request.md) Nachricht freigeben.

Wenn der Server die Anforderung nicht erfüllen kann, sendet er eine negative [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung an den Client, wie im folgenden Beispiel gezeigt.


```
// Negative acknowledgment. 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 0, atomItem));
```



Beim Empfang einer [**WM- \_ DDE- \_ Daten**](wm-dde-data.md) Nachricht verarbeitet der Client den Datenelement Wert nach Bedarf. Wenn das **fakkreq** -Element, auf das in der **WM- \_ DDE- \_ Daten** Meldung verwiesen wird, 1 ist, muss der Server dem Server eine positive [**WM \_ DDE \_ ACK**](wm-dde-ack.md) -Nachricht senden, wie im folgenden Beispiel gezeigt.


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



In diesem Beispiel untersucht der Client das Format der Daten. Wenn das Format nicht der **CF- \_ Text** ist (oder wenn der Client den Arbeitsspeicher für die Daten nicht sperren kann), sendet der Client eine negative [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht, um anzugeben, dass die Daten nicht verarbeitet werden können. Wenn der Client ein Daten Handle nicht sperren kann, da das Handle das **fakkreq** -Element enthält, sollte der Client keine negative **WM- \_ DDE \_** -Bestätigungsnachricht senden. Stattdessen sollte der Client die Konversation beenden.

Wenn ein Client eine negative Bestätigung als Antwort auf eine WM- [**\_ DDE- \_ Daten**](wm-dde-data.md) Nachricht sendet, ist der Server dafür verantwortlich, den Speicher freizugeben (aber nicht den *LPARAM* -Parameter), auf den von der mit der negativen Bestätigung verknüpften **WM \_ DDE- \_ Daten** Meldung verwiesen wird.

Wenn die Daten verarbeitet werden können, überprüft der Client den **fakkreq** -Member der [**ddedata**](/windows/desktop/api/Dde/ns-dde-ddedata) -Struktur, um zu bestimmen, ob der Server die Daten informiert hat, dass der Client die Daten erfolgreich empfangen und verarbeitet hat. Wenn der Server diese Informationen angefordert hat, sendet der Client dem Server eine positive [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht.

Da durch das Entsperren von Daten der Zeiger auf die Daten ungültig wird, speichert der Client den Wert des **frelease** -Members, bevor das Datenobjekt entsperrt wird. Nach dem Speichern des Werts wird der Client vom Client überprüft, um zu bestimmen, ob die Serveranwendung den Speicher des Clients angefordert hat. der Client verhält sich entsprechend.

Nachdem eine negative [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung empfangen wurde, kann der Client wieder denselben Elementwert anfordern und ein anderes Zwischenablage Format angeben. In der Regel fragt ein Client zunächst das komplexeste Format ab, das er unterstützen kann, und führt dann ggf. durch progressivste Formate einen Schritt aus, bis es von dem Server bereitgestellt werden kann.

Wenn der Server das Formatierungselement des Themas System unterstützt, kann der Client feststellen, welche Zwischenablage Formate der Server unterstützt, anstatt Sie jedes Mal zu ermitteln, wenn der Client ein Element anfordert.

### <a name="submitting-an-item-to-the-server"></a>Ein Element wird an den Server übermittelt.

Der Client kann einen Elementwert mithilfe der [**WM- \_ DDE- \_ Poke**](wm-dde-poke.md) -Nachricht an den Server senden. Der Client rendert das zu sendende Element und sendet die **WM- \_ DDE- \_ Poke** -Nachricht, wie im folgenden Beispiel veranschaulicht.


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
> Das Senden von Daten mithilfe einer [**WM- \_ DDE- \_ Poke**](wm-dde-poke.md) -Nachricht ist im Wesentlichen identisch mit dem Senden der Daten mithilfe von [**WM-DDE- \_ \_ Daten**](wm-dde-data.md), mit der Ausnahme, dass **WM \_ DDE \_ Poke** vom Client an den Server gesendet wird.

 

Wenn der Server den Datenelement Wert in dem vom Client gerenderten Format akzeptieren kann, verarbeitet der Server den Elementwert nach Bedarf und sendet dem Client eine positive [**WM \_ DDE \_ ACK**](wm-dde-ack.md) -Nachricht. Wenn der Elementwert aufgrund seines Formats oder aus anderen Gründen nicht verarbeitet werden kann, sendet der Server dem Client eine negative **WM \_ DDE \_ ACK** -Nachricht.


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



In diesem Beispiel ruft der Server [**globalgetatomname**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) auf, um den Namen des vom Client gesendeten Elements abzurufen. Der Server bestimmt dann, ob das Element unterstützt wird und ob das Element im richtigen Format (CF-Text) gerendert wird \_ . Wenn das Element nicht unterstützt wird und nicht im richtigen Format gerendert wird oder der Server den Arbeitsspeicher für die Daten nicht sperren kann, sendet der Server eine negative Bestätigung an die Client Anwendung zurück. Beachten Sie, dass das Senden einer negativen Bestätigung in diesem Fall korrekt ist, da bei [**WM \_ DDE \_ Poke**](wm-dde-poke.md) -Nachrichten immer angenommen wird, dass der **fakkreq** -Member festgelegt ist. Der Server sollte den Member ignorieren.

Wenn ein Server eine negative Bestätigung als Antwort auf eine WM- [**\_ DDE- \_ Poke**](wm-dde-poke.md) -Nachricht sendet, ist der Client für die Freigabe des Arbeitsspeichers (aber nicht für den *LPARAM* -Parameter) verantwortlich, auf den von der mit der negativen Bestätigung verknüpften **WM-DDE- \_ \_ Poke** -Meldung verwiesen wird.

## <a name="establishing-a-permanent-data-link"></a>Einrichten einer permanenten Datenverknüpfung

Eine Client Anwendung kann DDE verwenden, um einen Link zu einem Element in einer Serveranwendung herzustellen. Nachdem ein solcher Link festgelegt wurde, sendet der Server regelmäßige Aktualisierungen des verknüpften Elements an den Client, in der Regel, wenn der Wert des Elements geändert wird. Daher wird ein dauerhafter Datenstrom zwischen den beiden Anwendungen eingerichtet. dieser Datenstrom bleibt so lange bestehen, bis er explizit getrennt wird.

### <a name="initiating-a-data-link"></a>Initiieren einer Datenverknüpfung

Der Client initiiert eine Datenverknüpfung, indem er eine Meldung vom Typ " [**WM \_ DDE \_**](wm-dde-advise.md) " veröffentlicht, wie im folgenden Beispiel gezeigt.


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



In diesem Beispiel legt die Client Anwendung das **fdeferupd-** Flag der [**WM- \_ DDE- \_ Empfehlung**](wm-dde-advise.md) -Nachricht auf **false** fest. Dadurch wird die Serveranwendung angewiesen, die Daten immer dann an den Client zu senden, wenn sich die Daten ändern.

Wenn der Server die Anforderung " [**WM DDE- \_ \_ Empfehlung**](wm-dde-advise.md) " nicht bedienen kann, sendet er dem Client eine negative [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht. Wenn der Server jedoch Zugriff auf das Element hat und ihn im angeforderten Format renderengen kann, notiert der Server den neuen Link (wobei die im *hoptions* -Parameter angegebenen Flags wieder hergestellt werden) und sendet dem Client eine positive **WM \_ DDE \_ ACK** -Nachricht. Von diesem Zeitpunkt an sendet der Server die neuen Daten [**jedes \_ \_**](wm-dde-unadvise.md) Mal, wenn der Wert des Elements auf dem Server geändert wird, an den Client.

Die Meldung " [**WM \_ DDE- \_ Empfehlung**](wm-dde-advise.md) " gibt das Format der Daten an, die während des Links ausgetauscht werden sollen. Wenn der Client versucht, eine andere Verknüpfung mit demselben Element herzustellen, aber ein anderes Datenformat verwendet, kann der Server das zweite Datenformat ablehnen oder versuchen, es zu unterstützen. Wenn ein warmer Link für ein beliebiges Datenelement eingerichtet wurde, kann der Server jeweils nur ein Datenformat unterstützen. Dies liegt daran, dass die [**WM- \_ DDE- \_ Daten**](wm-dde-data.md) Nachricht für einen warmen Link ein **null** -Daten Handle enthält, das andernfalls die Formatierungsinformationen enthält. Folglich muss ein Server alle warmen Verknüpfungen für ein Element ablehnen, das bereits verknüpft ist, und alle Verknüpfungen für ein Element ablehnen, das über warme Links verfügt. Eine andere Interpretation kann sein, dass der Server das Format und den heißen oder den warmen Zustand eines Links ändert, wenn ein zweiter Link für das gleiche Datenelement angefordert wird.

Im Allgemeinen sollten Client Anwendungen nicht versuchen, mehr als einen Link gleichzeitig für ein Datenelement einzurichten.

### <a name="initiating-a-data-link-with-the-paste-link-command"></a>Initiieren einer Datenverknüpfung mit dem Befehl "Link einfügen"

Anwendungen, die Hot-oder warm-Daten Verknüpfungen unterstützen, unterstützen in der Regel das registrierte Zwischenablage Format Wenn Sie den Befehlen zum Kopieren und Einfügen von Anwendungen zugeordnet sind, ermöglicht dieses Zwischenablage Format dem Benutzer das Einrichten von DDE-Konversationen zwischen Anwendungen, indem einfach ein Datenelement in der Serveranwendung kopiert und in die Client Anwendung eingefügt wird.

Eine Serveranwendung unterstützt das Format der Link Zwischenablage, indem Sie in der Zwischenablage eine Zeichenfolge platziert, die die Anwendungs-, Thema-und Elementnamen enthält, wenn der Benutzer im Menü **Bearbeiten** den Befehl **Kopieren** auswählt. Im folgenden ist das Standard Verknüpfungs Format aufgeführt:

*Anwendung ***\\ 0*** Thema ***\\ 0*** Element * * * \\ 0 \\ 0**

Ein einzelnes Null-Zeichen trennt die Namen, und zwei NULL-Zeichen beenden die gesamte Zeichenfolge.

Die Client-und Server Anwendungen müssen das Format der Link Zwischenablage wie folgt registrieren:


```
cfLink = RegisterClipboardFormat("Link");
```



Eine Client Anwendung unterstützt das Format der Link Zwischenablage mithilfe eines Befehls zum Einfügen von Links im Menü Bearbeiten. Wenn der Benutzer diesen Befehl auswählt, analysiert die Client Anwendung die Anwendungs-, Thema-und Elementnamen aus den Zwischenablage Daten des Verknüpfungs Formats. Mit diesen Namen initiiert die Client Anwendung eine Konversation für die Anwendung und das Thema, wenn eine solche Konversation nicht bereits vorhanden ist. Die Client Anwendung sendet eine [**WM- \_ DDE \_**](wm-dde-advise.md) -Benachrichtigungs Meldung an die Serveranwendung und gibt dabei den Elementnamen an, der in den Zwischenablage Daten des Link Formats enthalten ist.

Im folgenden finden Sie ein Beispiel für die Antwort einer Client Anwendung, wenn der Benutzer den Befehl Link einfügen auswählt.


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



In diesem Beispiel öffnet die Client Anwendung die Zwischenablage und bestimmt, ob Sie Daten im Verknüpfungs Format (d. h. cflink) enthält, das zuvor registriert wurde. Wenn dies nicht der Fall ist oder wenn die Daten in der Zwischenablage nicht gesperrt werden können, gibt der Client zurück.

Nachdem die Client Anwendung einen Zeiger auf die Zwischenablage Daten abgerufen hat, analysiert Sie die Daten, um die Anwendungs-, Thema-und Elementnamen zu extrahieren.

Die Client Anwendung bestimmt, ob eine Konversation für das Thema bereits zwischen der Anwendung und der Serveranwendung vorhanden ist. Wenn eine Konversation vorhanden ist, überprüft der Client, ob für das Datenelement bereits ein Link vorhanden ist. Wenn ein solcher Link vorhanden ist, zeigt der Client dem Benutzer ein Meldungs Feld an. Andernfalls wird eine eigene *sendempfehlung* -Funktion aufgerufen, um eine [**WM- \_ DDE \_**](wm-dde-advise.md) -Benachrichtigungs Meldung an den Server für das Element zu senden.

Wenn eine Konversation für das Thema nicht bereits zwischen dem Client und dem Server vorhanden ist, ruft der Client zuerst seine eigene *sendinitiate* -Funktion auf, um die [**WM-DDE- \_ \_ Initiierungs**](wm-dde-initiate.md) Nachricht zu senden und eine Konversation anzufordern. Anschließend ruft er eine eigene *findserfehlervenapptopic* -Funktion auf, um die Konversation mit dem Fenster, das im Auftrag der Serveranwendung Nachdem die Konversation begonnen hat, ruft die Client Anwendung *SendRequest* auf, um den Link anzufordern.

### <a name="notifying-the-client-that-data-has-changed"></a>Benachrichtigen des Clients, dass sich Daten geändert haben

Wenn der Client mithilfe der WM-DDE- [**\_ \_ Empfehlung**](wm-dde-advise.md) eine Verknüpfung herstellt, während der " **fdeferupd"-** Member in der [**ddedata**](/windows/desktop/api/Dde/ns-dde-ddedata) -Struktur nicht festgelegt ist (d. h. gleich 0 (null)), hat der Client angefordert, dass der Server jedes Mal das Datenelement sendet, wenn sich der Wert des Elements ändert. In solchen Fällen rendert der Server den neuen Wert des Datenelements im zuvor angegebenen Format und sendet dem Client eine [**WM DDE- \_ \_ Daten**](wm-dde-data.md) Nachricht, wie im folgenden Beispiel gezeigt.


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



In diesem Beispiel verarbeitet der Client den Elementwert nach Bedarf. Wenn das **fakkreq** -Flag für das Element festgelegt ist, sendet der Client dem Server eine positive [**WM \_ DDE \_ ACK**](wm-dde-ack.md) -Nachricht.

Wenn der Client den Link festlegt, wobei das **fdeferupd-** Element festgelegt ist (d. h. gleich 1), hat der Client angefordert, dass nur eine Benachrichtigung, nicht die Daten selbst, gesendet werden, wenn sich die Daten ändern. In solchen Fällen, wenn sich der Elementwert ändert, wird der Wert vom Server nicht dargestellt, sondern es wird einfach eine [**WM- \_ DDE- \_ Daten**](wm-dde-data.md) Nachricht mit einem NULL-Daten Handle an den Client gesendet, wie im folgenden Beispiel veranschaulicht.


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



Bei Bedarf kann der Client den neuesten Wert des Datenelements anfordern, indem er eine normale [**WM- \_ DDE- \_ Anforderungs**](wm-dde-request.md) Nachricht ausgibt, oder er kann einfach den Hinweis vom Server ignorieren, dass sich die Daten geändert haben. Wenn " **fakkreq** " gleich 1 ist, wird erwartet, dass der Client eine positive [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht an den Server sendet.

### <a name="terminating-a-data-link"></a>Beenden eines Daten Links

Wenn der Client anfordert, dass eine bestimmte Datenverknüpfung beendet wird, sendet der Client dem Server eine Meldung vom Typ " [**WM \_ DDE \_ unempfehlung**](wm-dde-unadvise.md) ", wie im folgenden Beispiel gezeigt.


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



Der Server überprüft, ob der Client zurzeit über einen Link zum bestimmten Element in dieser Konversation verfügt. Wenn ein Link vorhanden ist, sendet der Server dem Client eine positive [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung. der Server ist dann nicht mehr zum Senden von Updates über das Element erforderlich. Wenn kein Link vorhanden ist, sendet der Server dem Client eine negative **WM \_ DDE \_** -Bestätigungsnachricht.

Die " [**WM \_ DDE \_ unempfehlung**](wm-dde-unadvise.md) "-Meldung gibt ein Datenformat an. Bei einem Format von NULL wird der Server angewiesen, alle Verknüpfungen für das angegebene Element zu unterbinden, auch wenn mehrere heiße Verknüpfungen eingerichtet sind und jeweils ein anderes Format verwendet wird.

Um alle Verknüpfungen für eine Konversation zu beenden, sendet die Client Anwendung dem Server eine [**\_ \_ nicht Empfehlung**](wm-dde-unadvise.md) -Nachricht vom Typ "WM DDE" mit einem NULL-Element Atom. Der Server bestimmt, ob für die Konversation mindestens ein Link eingerichtet ist. Wenn ein Link vorhanden ist, sendet der Server dem Client eine positive [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht. der Server muss dann keine Updates mehr in der Konversation senden. Wenn kein Link vorhanden ist, sendet der Server dem Client eine negative **WM \_ DDE \_** -Bestätigungsnachricht.

## <a name="carrying-out-commands-in-a-server-application"></a>Ausführen von Befehlen in einer Server Anwendung

Anwendungen können die " [**WM \_ DDE \_ Execute**](wm-dde-execute.md) "-Nachricht verwenden, um zu veranlassen, dass ein bestimmter Befehl oder eine Reihe von Befehlen in einer anderen Anwendung ausgeführt wird. Hierzu sendet der Client dem Server eine **WM-DDE- \_ \_ Execute** -Nachricht mit einem Handle an eine Befehls Zeichenfolge, wie im folgenden Beispiel gezeigt.


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



In diesem Beispiel versucht der Server, die angegebene Befehls Zeichenfolge auszuführen. Wenn dies der Fall ist, sendet der Server dem Client eine positive [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht, andernfalls sendet er eine negative **WM- \_ DDE \_** -Bestätigungsnachricht. Diese **WM- \_ DDE \_** -Bestätigungsnachricht verwendet das *hcommand* -handle, das in der ursprünglichen [**WM-DDE- \_ \_ Ausführungs**](wm-dde-execute.md) Nachricht weitergegeben wurde.

Wenn die Befehls Ausführungs Zeichenfolge des Clients anfordert, dass der Server beendet wird, sollte der Server Antworten, indem er eine positive [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht sendet und eine [**WM- \_ DDE \_**](wm-dde-terminate.md) -Beendigungs Nachricht vor dem Beenden sendet. Alle anderen Befehle, die mit der " [**WM \_ DDE \_ Execute**](wm-dde-execute.md) "-Nachricht gesendet werden, sollten synchron ausgeführt werden, d. h., der Server sollte eine " **WM \_ DDE \_ ACK** "-Nachricht erst senden, nachdem der Befehl erfolgreich abgeschlossen

## <a name="terminating-a-conversation"></a>Beenden einer Konversation

Entweder kann der Client oder der Server eine [**WM- \_ DDE \_**](wm-dde-terminate.md) -Beendigungs Nachricht ausgeben, um eine Konversation zu einem beliebigen Zeitpunkt zu beenden. Ebenso sollten sowohl die Client-als auch die Serveranwendung jederzeit darauf vorbereitet sein, diese Nachricht zu empfangen. Eine Anwendung muss alle Ihre Konversationen beenden, bevor Sie heruntergefahren wird.

Im folgenden Beispiel stellt die Anwendung, die die Konversation beendet, eine " [**WM \_ DDE \_**](wm-dde-terminate.md) -Beendigungs Nachricht" gepostet.


```
PostMessage(hwndServerDDE, WM_DDE_TERMINATE, 
    (WPARAM) hwndClientDDE, 0);
```



Dadurch wird der anderen Anwendung mitgeteilt, dass die sendende Anwendung keine weiteren Nachrichten sendet und der Empfänger das Fenster schließen kann. In allen Fällen wird erwartet, dass der Empfänger umgehend antwortet, indem er eine Abbruch Meldung vom [**WM \_ \_**](wm-dde-terminate.md) -Dienst sendet. Der Empfänger darf keine negative, ausgelastete oder positive [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht senden.

Nachdem eine Anwendung die " [**WM \_ DDE \_**](wm-dde-terminate.md) "-Beendigungs Nachricht an den Partner in einer DDE-Konversation gesendet hat, darf Sie nicht auf Nachrichten von diesem Partner Antworten, da der Partner das Fenster, an den die Antwort gesendet wurde, möglicherweise zerstört hat.

Wenn eine Anwendung eine DDE-Nachricht empfängt, die nicht [**WM \_ DDE \_ beendet**](wm-dde-terminate.md) , nachdem **die WM- \_ DDE \_ beendet** wurde, sollte Sie alle Objekte freigeben, die den empfangenen Nachrichten zugeordnet sind, mit Ausnahme der Daten Handles für [**WM-DDE- \_ \_ Daten**](wm-dde-data.md) oder [**WM \_ DDE \_ Poke**](wm-dde-poke.md) -Nachrichten, für die das **frelease** -Element **nicht** festgelegt ist.

Wenn eine Anwendung gerade beendet wird, sollte Sie alle aktiven DDE-Konversationen beenden, bevor die Verarbeitung der WM-Lösch Nachricht abgeschlossen wird. [**\_**](/windows/desktop/winmsg/wm-destroy) Wenn eine Anwendung jedoch nicht die aktiven DDE-Konversationen beendet, beendet das System alle DDE-Konversationen, die einem Fenster zugeordnet sind, wenn das Fenster zerstört wird. Das folgende Beispiel zeigt, wie eine Serveranwendung alle DDE-Konversationen beendet.


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



 

 