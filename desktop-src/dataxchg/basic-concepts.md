---
title: Grundlegende Konzepte
description: In diesem Thema werden wichtige Konzepte zum dynamischen Datenaustausch erläutert.
ms.assetid: 37826d83-4dcd-484f-b1aa-87bf309c5c09
keywords:
- Windows-Benutzeroberfläche, dynamischer Datenaustausch (DDE)
- Windows-Benutzeroberfläche, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
- Dynamischer Datenaustausch (DDE), Client Server Interaktion
- DDE (dynamischer Datenaustausch), Client Server Interaktion
- Datenaustausch, dynamischer Datenaustausch (DDE)
- Datenaustausch, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
- Dynamischer Datenaustausch (DDE), Client Anwendungen
- DDE (dynamischer Datenaustausch), Client Anwendungen
- Dynamischer Datenaustausch (DDE), Server Anwendungen
- DDE (dynamischer Datenaustausch), Server Anwendungen
- Dynamischer Datenaustausch (DDE), Rückruf Funktionen
- DDE (dynamischer Datenaustausch), Rückruf Funktionen
- Dynamischer Datenaustausch (DDE), Transaktionen
- DDE (dynamischer Datenaustausch), Transaktionen
- Dynamischer Datenaustausch (DDE), Dienstnamen
- DDE (dynamischer Datenaustausch), Dienstnamen
- Dynamischer Datenaustausch (DDE), Elementnamen
- DDE (dynamischer Datenaustausch), Elementnamen
- Dynamischer Datenaustausch (DDE), Themen Namen
- DDE (dynamischer Datenaustausch), Themen Namen
- Dynamischer Datenaustausch (DDE), System Thema
- DDE (dynamischer Datenaustausch), System Thema
- Dynamischer Datenaustausch Management Library (Ddeml), Initialisierung
- Ddeml (dynamischer Datenaustausch-Verwaltungs Bibliothek), Initialisierung
- Dynamischer Datenaustausch Management Library (Ddeml), Rückruf Funktionen
- Ddeml (dynamischer Datenaustausch Management Library), Rückruf Funktionen
- Dynamischer Datenaustausch Management Library (Ddeml), Zeichen folgen Verwaltung
- Ddeml (dynamischer Datenaustausch-Verwaltungs Bibliothek), Zeichen folgen Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c564bffbcbb06ddc3a0e0fa4e0a9ed398d3ca55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727920"
---
# <a name="basic-concepts-dde"></a>Grundlegende Konzepte (DDE)

Diese Konzepte sind entscheidend, um dynamischer Datenaustausch (DDE) und die dynamischer Datenaustausch Management Library (Ddeml) zu verstehen.

-   [Client-und Server Interaktion](#client-and-server-interaction)
-   [Transaktionen und die DDE-Rückruffunktion](#transactions-and-the-dde-callback-function)
-   [Dienstnamen, Themen Namen und Elementnamen](#service-names-topic-names-and-item-names)
-   [System Thema](#system-topic)
-   [Initialisierung](#initialization)
-   [Rückruffunktion](#callback-function)
-   [Zeichen folgen Verwaltung](#string-management)
-   [Ddeml und Threads](#ddeml-and-threads)

## <a name="client-and-server-interaction"></a>Client-und Server Interaktion

DDE tritt immer zwischen einer Client Anwendung und einer Serveranwendung auf. Die *DDE-Client Anwendung* initiiert den Austausch, indem Sie eine Konversation mit dem Server herstellt, um Transaktionen an den Server zu senden. Bei einer Transaktion handelt es sich um eine Anforderung für Daten oder Dienste. Die *DDE-Serveranwendung* reagiert auf Transaktionen, indem Daten oder Dienste für den Client bereitgestellt werden. Eine Grafikanwendung könnte z. b. ein Balkendiagramm enthalten, das den Quartalsgewinn einer Corporation repräsentiert, aber die Daten für das Balkendiagramm sind möglicherweise in einer Tabellenkalkulationsanwendung enthalten. Zum Abrufen der neuesten Gewinnzahlen könnte die Grafikanwendung (der Client) eine Konversation mit der Tabellenkalkulationsanwendung (dem Server) herstellen. Die Grafikanwendung könnte dann eine Transaktion an die Tabellenkalkulationsanwendung senden und dabei die neuesten Gewinnzahlen anfordern.

Ein Server kann über viele Clients gleichzeitig verfügen, und ein Client kann Daten von mehreren Servern anfordern. Bei einer Anwendung kann es sich auch um einen Client und einen Server handeln. Die Konversation kann entweder vom Client oder vom Server jederzeit beendet werden.

## <a name="transactions-and-the-dde-callback-function"></a>Transaktionen und die DDE-Rückruffunktion

Die Ddeml benachrichtigt eine Anwendung über DDE-Aktivitäten, die sich auf die Anwendung auswirken, indem Transaktionen an die DDE-Rückruffunktion der Anwendung gesendet werden. Eine *DDE-Transaktion* ähnelt einer Nachricht, bei der es sich um eine benannte Konstante handelt, die von anderen Parametern begleitet wird, die zusätzliche Informationen zur Transaktion enthalten.

Die Ddeml übergibt eine Transaktion an eine Anwendungs definierte DDE-Rückruffunktion, die eine Aktion ausführt, die für den Transaktionstyp geeignet ist. Wenn eine Client Anwendung z. b. versucht, eine Konversation mit einer Serveranwendung herzustellen, ruft der Client die [**ddeconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) -Funktion auf. Diese Funktion bewirkt, dass die Ddeml eine [**XYP \_ Connect**](xtyp-connect.md) -Transaktion an die DDE-Rückruffunktion des Servers sendet. Die Rückruffunktion kann die Konversation zulassen, indem Sie " **true** " an die Ddeml zurückgibt, oder die Konversation durch Rückgabe von " **false**" ablehnen. Eine ausführliche Erläuterung der Transaktionen finden Sie unter [Transaktions Verwaltung](transaction-management.md).

## <a name="service-names-topic-names-and-item-names"></a>Dienstnamen, Themen Namen und Elementnamen

Ein DDE-Server verwendet einen Hierarchie Dienstnamen mit drei Ebenen (in vorheriger DDE-Dokumentation als "Anwendungsname" bezeichnet), den Themen Namen und den Elementnamen zum eindeutigen Identifizieren einer Dateneinheit, die der Server während einer Konversation austauschen kann.

Ein *Dienst Name* ist eine Zeichenfolge, auf die eine Serveranwendung antwortet, wenn ein Client versucht, eine Konversation mit dem Server herzustellen. Ein Client muss diesen Dienstnamen angeben, um eine Konversation mit dem Server herzustellen. Obwohl ein Server auf viele Dienstnamen reagieren kann, reagieren die meisten Server nur auf einen Namen.

Ein *Themenname* ist eine Zeichenfolge, die einen logischen Datenkontext identifiziert. Bei Servern, die auf dateibasierten Dokumenten basieren, sind Themen Namen in der Regeldatei Namen. bei anderen Servern sind Sie andere anwendungsspezifische Zeichen folgen. Ein Client muss einen Themen Namen zusammen mit dem Dienstnamen eines Servers angeben, wenn er versucht, eine Konversation mit einem Server einzurichten.

Ein *ElementName* ist eine Zeichenfolge, die eine Dateneinheit identifiziert, die ein Server während einer Transaktion an einen Client übergeben kann. Ein Elementname kann z. b. eine ganze Zahl, eine Zeichenfolge, mehrere Absätze von Text oder eine Bitmap identifizieren.

Mithilfe der Dienst-, Thema-und Elementnamen kann der Client eine Konversation mit einem Server einrichten und Daten vom Server empfangen.

## <a name="system-topic"></a>System Thema

Das System Thema bietet einen Kontext für Informationen, die für alle DDE-Clients von allgemeinem Interesse sind. Es wird empfohlen, dass Server Anwendungen immer das Thema "System" unterstützen. Das System Thema ist in der Ddeml definiert. H-Header Datei als szddesys- \_ Thema.

Um zu ermitteln, welche Server vorhanden sind und welche Informationen Sie bereitstellen können, kann eine Client Anwendung eine Konversation im Thema System anfordern, wenn der Gerätename auf **null** festgelegt wird. Solche Platzhalter Konversationen sind in Bezug auf die Systemleistung kostspielig, sodass Sie auf ein Minimum beschränkt werden sollten. Weitere Informationen zum Initiieren von DDE-Konversationen finden Sie unter [Konversations Verwaltung](conversation-management.md).

Ein Server muss die folgenden Elementnamen innerhalb des System Themas und alle anderen Elementnamen unterstützen, die für einen Client nützlich sind.



| Element                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| szdde- \_ Element ( \_ itemlist)    | Eine Liste der Elemente, die unter einem nicht-System-Thema unterstützt werden. (Diese Liste kann von Zeit zu Zeit und von Thema zu Thema abweichen.)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| szddecosys- \_ Element \_ Formate  | Eine durch Tabstopps getrennte Liste von Zeichen folgen, die alle Zwischenablage Formate darstellen, die potenziell von der Dienst Anwendung unterstützt werden. Zeichen folgen, die vordefinierte Zwischenablage Formate darstellen, entsprechen den CF- \_ Werten, wobei das \_ Präfix "CF" entfernt wurde. Beispielsweise wird das CF- \_ Text Format durch die Zeichenfolge "Text" dargestellt. Diese Zeichen folgen müssen in Großbuchstaben angegeben werden, um Sie als vordefinierte Formate zu identifizieren. Die Liste der Formate muss in der Reihenfolge der meisten Inhalte der Inhalte enthalten sein, um den Inhalt möglichst wenig zu nutzen. Weitere Informationen zu Zwischenablage Formaten und Rendern von Daten finden Sie unter [Zwischenablage](clipboard.md).<br/> |
| szdde sys- \_ Element \_ Hilfe     | Vom Benutzer lesbare Informationen von allgemeinem Interesse. Dieses Element muss mindestens Informationen zur Verwendung der DDE-Funktionen der Serveranwendung enthalten. Diese Informationen können enthalten, sind jedoch nicht darauf beschränkt, wie Elemente innerhalb von Themen angegeben werden, welche Ausführungs Zeichenfolgen der Server ausführen kann, welche schaffen-Transaktionen zulässig sind und wie Hilfe zu anderen System Themen Elementen gefunden wird.                                                                                                                                                                                                                           |
| szdde sys- \_ Element \_ rtnmsg   | Unterstützende Details der zuletzt verwendeten [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht. Dieses Element ist nützlich, wenn mehr als 8 Bits von anwendungsspezifischen Rückgabe Daten erforderlich sind.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| szddesys- \_ Element \_ Status   | Ein Hinweis auf den aktuellen Status des Servers. In der Regel unterstützt dieses Element nur das CF \_ -Text Format und enthält die Zeichenfolge Ready oder ausgelastet.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| szdde sys- \_ Element \_ SysItems | Eine Liste der Elemente, die von diesem Server unter dem Thema "System" unterstützt werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Themen zu szdde sys-Elementen \_ \_   | Eine Liste der Themen, die vom Server zum aktuellen Zeitpunkt unterstützt werden. (Diese Liste kann sich von Zeit zu Zeit unterscheiden.)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Diese Elementnamen sind Werte, die in der Ddeml definiert werden. H-Header Datei. Um Zeichen folgen Handles für diese Zeichen folgen zu erhalten, muss eine Anwendung die Ddeml-Funktionen für die Zeichen folgen Verwaltung genauso wie für jede andere Zeichenfolge in einer Ddeml-Anwendung verwenden. Weitere Informationen zum Verwalten von Zeichen folgen finden Sie unter [Zeichen folgen Verwaltung](#string-management).

## <a name="initialization"></a>Initialisierung

Vor dem Aufrufen einer anderen Ddeml-Funktion muss eine Anwendung die [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion aufrufen. **DDEInitialize** erhält einen Instanzbezeichner für die Anwendung, registriert die DDE-Rückruffunktion der Anwendung bei DDE und gibt die transaktionsfilterflags für die Rückruffunktion an.

Jede Instanz einer Anwendung oder dll muss den Instanzbezeichner als *idinst* -Parameter an jede andere Ddeml-Funktion übergeben, die Sie benötigt. Der Zweck mehrerer Ddeml-Instanzen besteht darin, DLLs zu unterstützen, die die Ddeml zur gleichen Zeit verwenden müssen, die von einer Anwendung verwendet wird. Eine Anwendung darf nicht mehr als eine Instanz der Ddeml verwenden.

*Transaktions Filter* optimieren die Systemleistung, indem verhindert wird, dass die Ddeml unerwünschte Transaktionen an die DDE-Rückruffunktion der Anwendung übergibt. Eine Anwendung legt die Transaktions Filter im Parameter " [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) *ufcmd* " fest. Eine Anwendung muss ein transaktionsfilterflag für jeden Transaktionstyp angeben, der nicht in der Rückruffunktion verarbeitet wird. Eine Anwendung kann Ihre Transaktions Filter mit einem nachfolgenden Aufrufe von **DDEInitialize** ändern. Weitere Informationen zu Transaktionen finden Sie unter [Transaktions Verwaltung](transaction-management.md).

Im folgenden Beispiel wird gezeigt, wie eine Anwendung initialisiert wird, um die Ddeml zu verwenden.


```
DWORD idInst = 0; 
HINSTANCE hinst; 
 
DdeInitialize(&idInst,         // receives instance identifier 
    (PFNCALLBACK) DdeCallback, // pointer to callback function 
    CBF_FAIL_EXECUTES |        // filter XTYPE_EXECUTE 
    CBF_SKIP_ALLNOTIFICATIONS, // filter notifications 
    0); 
```



Eine Anwendung muss die [**ddeuninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) -Funktion aufrufen, wenn die Ddeml nicht mehr verwendet wird. Diese Funktion beendet alle Konversationen, die aktuell für die Anwendung geöffnet sind, und gibt die Ddeml-Ressourcen frei, die für die Anwendung reserviert wurden.

## <a name="callback-function"></a>Rückruffunktion

Eine Anwendung, die die Ddeml verwendet, muss eine Rückruffunktion bereitstellen, die die DDE-Ereignisse verarbeitet, die die Anwendung beeinträchtigen. Die Ddeml benachrichtigt eine Anwendung über solche Ereignisse, indem Transaktionen an die DDE-Rückruffunktion der Anwendung gesendet werden. Die Transaktionen, die eine Rückruffunktion empfängt, hängen davon ab, welcher Rückruf Filter die in [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) angegebene Anwendung verwendet und ob es sich bei der Anwendung um einen Client, einen Server oder beides handelt. Weitere Informationen finden Sie unter [**ddecallback**](/windows/win32/api/ddeml/nc-ddeml-pfncallback).

Das folgende Beispiel zeigt die allgemeine Struktur einer Rückruffunktion für eine typische Client Anwendung.


```
HDDEDATA CALLBACK DdeCallback(uType, uFmt, hconv, hsz1, 
    hsz2, hdata, dwData1, dwData2) 
UINT uType;       // transaction type 
UINT uFmt;        // clipboard data format 
HCONV hconv;      // handle to conversation 
HSZ hsz1;         // handle to string 
HSZ hsz2;         // handle to string 
HDDEDATA hdata;   // handle to global memory object 
DWORD dwData1;    // transaction-specific data 
DWORD dwData2;    // transaction-specific data 
{ 
    switch (uType) 
    { 
        case XTYP_REGISTER: 
        case XTYP_UNREGISTER: 
            . 
            . 
            . 
            return (HDDEDATA) NULL; 
 
        case XTYP_ADVDATA: 
            . 
            . 
            . 
            return (HDDEDATA) DDE_FACK; 
 
        case XTYP_XACT_COMPLETE: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        case XTYP_DISCONNECT: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        default: 
            return (HDDEDATA) NULL; 
    } 
} 
```



Der *uType* -Parameter gibt den Transaktionstyp an, der von der Ddeml an die Rückruffunktion gesendet wird. Die Werte der restlichen Parameter hängen vom Transaktionstyp ab. Die Transaktionstypen und die Ereignisse, die Sie generieren, werden in den folgenden Themen beschrieben. Ausführliche Informationen zu den einzelnen Transaktionstypen finden Sie unter [Transaktions Verwaltung](transaction-management.md).

## <a name="string-management"></a>Zeichen folgen Verwaltung

Um eine DDE-Aufgabe auszuführen, benötigen viele Ddeml-Funktionen Zugriff auf Zeichen folgen. Ein Client muss z. b. einen Dienstnamen und einen Themen Namen angeben, wenn er die [**ddeconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) -Funktion aufruft, um eine Konversation mit einem Server anzufordern. Eine Anwendung gibt eine Zeichenfolge an, indem ein Zeichen folgen handle (hsz) anstelle eines Zeigers in einer Ddeml-Funktion übergeben wird. Ein *Zeichen folgen handle* ist ein vom System zugewiesener **DWORD** -Wert, der eine Zeichenfolge identifiziert.

Eine Anwendung kann durch Aufrufen der [**ddecreatestringhandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) -Funktion ein Zeichen folgen Handle für eine bestimmte Zeichenfolge abrufen. Diese Funktion registriert die Zeichenfolge beim System und gibt ein Zeichen folgen Handle an die Anwendung zurück. Die Anwendung kann das Handle an Ddeml-Funktionen übergeben, die auf die Zeichenfolge zugreifen müssen. Im folgenden Beispiel werden Zeichen folgen Handles für die System-Themen Zeichenfolge und die Dienstnamen Zeichenfolge abgerufen.


```
HSZ hszServName; 
HSZ hszSysTopic; 
hszServName = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    "MyServer",     // string to register 
    CP_WINANSI);    // Windows ANSI code page 
 
hszSysTopic = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    SZDDESYS_TOPIC, // System topic 
    CP_WINANSI);    // Windows ANSI code page 
    
```



Der *idinst* -Parameter im vorangehenden Beispiel gibt den Instanzbezeichner an, der von der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion abgerufen wird.

Die DDE-Rückruffunktion einer Anwendung empfängt bei den meisten DDE-Transaktionen mindestens ein Zeichen folgen handle. Ein Server erhält z. b. zwei Zeichen folgen Handles während der [**xtion- \_ Anforderungs**](xtyp-request.md) Transaktion: eine identifiziert eine Zeichenfolge, die einen Themen Namen angibt, und die andere gibt eine Zeichenfolge an, die einen Elementnamen angibt. Eine Anwendung kann die Länge der Zeichenfolge abrufen, die einem Zeichen folgen Handle entspricht, und die Zeichenfolge in einen Anwendungs definierten Puffer kopieren, indem Sie die [**ddequerystring**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) -Funktion aufrufen, wie im folgenden Beispiel gezeigt.


```
DWORD idInst; 
DWORD cb; 
HSZ hszServ; 
PSTR pszServName; 
cb = DdeQueryString(idInst, hszServ, (LPSTR) NULL, 0, 
    CP_WINANSI) + 1; 
pszServName = (PSTR) LocalAlloc(LPTR, (UINT) cb); 
DdeQueryString(idInst, hszServ, pszServName, cb, CP_WINANSI); 
```



Ein instanzspezifisches Zeichen folgen Handle kann nicht vom Zeichen folgen Handle zur Zeichenfolge und zurück zum Zeichen folgen Handle zugeordnet werden. Obwohl [**dabquerystring**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) beispielsweise eine Zeichenfolge aus einem Zeichen folgen Handle erstellt und [**ddecreatestringhandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) ein Zeichen folgen Handle aus dieser Zeichenfolge erstellt, sind die beiden Handles nicht identisch, wie im folgenden Beispiel gezeigt.


```
DWORD idInst; 
DWORD cb; 
HSZ hszInst, hszNew; 
PSZ pszInst; 
DdeQueryString(idInst, hszInst, pszInst, cb, CP_WINANSI); 
hszNew = DdeCreateStringHandle(idInst, pszInst, CP_WINANSI); 
// hszNew != hszInst ! 
```



Um die Werte von zwei Zeichen folgen Handles zu vergleichen, verwenden Sie die Funktion [**ddecmpstringhandles**](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles) .

Ein Zeichen folgen handle, das an die DDE-Rückruffunktion einer Anwendung übertragen wird, wird bei Rückgabe der Rückruffunktion ungültig. Eine Anwendung kann ein Zeichen folgen Handle zur Verwendung speichern, nachdem die Rückruffunktion mithilfe der [**DDE keepstringhandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) -Funktion zurückgegeben wurde.

Wenn eine Anwendung " [**ddecreatestringhandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea)" aufruft, gibt das System die angegebene Zeichenfolge in eine Zeichen folgen Tabelle ein und generiert ein Handle, das für den Zugriff auf die Zeichenfolge verwendet wird. Das System verwaltet außerdem einen Verwendungs Zähler für jede Zeichenfolge in der Zeichen folgen Tabelle.

Wenn eine Anwendung " [**ddecreatestringhandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) " aufruft und eine Zeichenfolge angibt, die bereits in der Tabelle vorhanden ist, erhöht das System den Verwendungs Zähler, anstatt ein weiteres Vorkommen der Zeichenfolge hinzuzufügen. (Eine Anwendung kann auch die Verwendungs Anzahl mithilfe von [**DDE keepstringhandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle)erhöhen.) Wenn eine Anwendung die [**ddefrestringhandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle) -Funktion aufruft, verringert das System die Verwendungs Anzahl.

Eine Zeichenfolge wird aus der Tabelle entfernt, wenn die Verwendungs Anzahl gleich 0 (null) ist. Da mehr als eine Anwendung das Handle für eine bestimmte Zeichenfolge abrufen kann, darf eine Anwendung ein Zeichen folgen Handle nicht mehrmals freigeben, als das Handle erstellt oder beibehalten hat. Andernfalls kann die Anwendung bewirken, dass die Zeichenfolge aus der Tabelle entfernt wird, sodass andere Anwendungen den Zugriff auf die Zeichenfolge verweigern.

Die Funktionen der Ddeml-Zeichen folgen Verwaltung basieren auf dem Atom-Manager und unterliegen denselben Größenbeschränkungen wie Atome.

## <a name="ddeml-and-threads"></a>Ddeml und Threads

Die [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion registriert eine Anwendung bei der Ddeml und erstellt dabei eine Ddeml-Instanz. Eine Ddeml-Instanz ist Thread basiert, die dem Thread zugeordnet ist, der **DDEInitialize** aufgerufen hat.

Alle Ddeml-Funktionsaufrufe für Objekte, die zu einer Ddeml-Instanz gehören, müssen aus demselben Thread erstellt werden, der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) aufgerufen hat, um die Instanz zu erstellen. Wenn Sie eine Ddeml-Funktion von einem anderen Thread aus aufruft, schlägt die Funktion fehl. Sie können nicht auf eine Ddeml-Konversation von einem anderen Thread als dem, der die Konversation zugeordnet hat, zugreifen.

 

