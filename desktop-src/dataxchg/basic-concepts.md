---
title: Grundlegende Konzepte
description: In diesem Thema werden wichtige Konzepte für den dynamischen Datenaustausch erläutert.
ms.assetid: 37826d83-4dcd-484f-b1aa-87bf309c5c09
keywords:
- Windows Benutzeroberfläche,dynamische Daten Exchange (DDE)
- Windows Benutzeroberfläche,dynamische Daten Exchange Management Library (DDEML)
- dynamische Daten Exchange (DDE), Clientserverinteraktion
- DDE (dynamische Daten Exchange), Clientserverinteraktion
- Datenaustausch,dynamische Daten Exchange (DDE)
- Datenaustausch,dynamische Daten Exchange Management Library (DDEML)
- dynamische Daten Exchange (DDE), Clientanwendungen
- DDE (dynamische Daten Exchange),Clientanwendungen
- dynamische Daten Exchange (DDE), Serveranwendungen
- DDE (dynamische Daten Exchange),Serveranwendungen
- dynamische Daten Exchange (DDE), Rückruffunktionen
- DDE (dynamische Daten Exchange),Rückruffunktionen
- dynamische Daten Exchange (DDE), Transaktionen
- DDE (dynamische Daten Exchange),Transaktionen
- dynamische Daten Exchange (DDE), Dienstnamen
- DDE (dynamische Daten Exchange),Dienstnamen
- dynamische Daten Exchange (DDE), Elementnamen
- DDE (dynamische Daten Exchange),Elementnamen
- dynamische Daten Exchange (DDE), Themennamen
- DDE (dynamische Daten Exchange),Themennamen
- dynamische Daten Exchange (DDE),Systemthema
- DDE (dynamische Daten Exchange),Systemthema
- dynamische Daten Exchange Management Library (DDEML), Initialisierung
- DDEML (dynamische Daten Exchange Management Library), Initialisierung
- dynamische Daten Exchange Management Library (DDEML), Rückruffunktionen
- DDEML (dynamische Daten Exchange Management Library), Rückruffunktionen
- dynamische Daten Exchange Management Library (DDEML), Zeichenfolgenverwaltung
- DDEML (dynamische Daten Exchange Management Library), Zeichenfolgenverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fae271c359afd571cf6c51fb3387a15f1496416e5eb54b055ef518fd213f30fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128622"
---
# <a name="basic-concepts-dde"></a>Grundkonzepte (DDE)

Diese Konzepte sind entscheidend für das Verständnis dynamische Daten Exchange (DDE) und der dynamische Daten Exchange Management Library (DDEML).

-   [Client- und Serverinteraktion](#client-and-server-interaction)
-   [Transaktionen und die DDE-Rückruffunktion](#transactions-and-the-dde-callback-function)
-   [Dienstnamen, Themennamen und Elementnamen](#service-names-topic-names-and-item-names)
-   [Systemthema](#system-topic)
-   [Initialisierung](#initialization)
-   [Rückruffunktion](#callback-function)
-   [Zeichenfolgenverwaltung](#string-management)
-   [DDEML und Threads](#ddeml-and-threads)

## <a name="client-and-server-interaction"></a>Client- und Serverinteraktion

DDE tritt immer zwischen einer Clientanwendung und einer Serveranwendung auf. Die *DDE-Clientanwendung* initiiert den Austausch, indem eine Konversation mit dem Server hergestellt wird, um Transaktionen an den Server zu senden. Eine Transaktion ist eine Anforderung für Daten oder Dienste. Die *DDE-Serveranwendung* reagiert auf Transaktionen, indem sie Dem Client Daten oder Dienste zur Verfügung stellt. Eine Grafikanwendung kann beispielsweise ein Balkendiagramm enthalten, das den vierteljährlichen Gewinn eines Unternehmens darstellt, aber die Daten für das Balkendiagramm können in einer Tabellenkalkulationsanwendung enthalten sein. Um die neuesten Gewinnzahlen zu erhalten, könnte die Grafikanwendung (der Client) eine Konversation mit der Tabellenkalkulationsanwendung (dem Server) herstellen. Die Grafikanwendung könnte dann eine Transaktion an die Tabellenkalkulationsanwendung senden und die neuesten Gewinnzahlen anfordern.

Ein Server kann über viele Clients gleichzeitig verfügen, und ein Client kann Daten von mehreren Servern anfordern. Eine Anwendung kann auch sowohl ein Client als auch ein Server sein. Entweder der Client oder der Server kann die Konversation jederzeit beenden.

## <a name="transactions-and-the-dde-callback-function"></a>Transaktionen und die DDE-Rückruffunktion

Die DDEML benachrichtigt eine Anwendung über DDE-Aktivitäten, die sich auf die Anwendung auswirken, indem Transaktionen an die DDE-Rückruffunktion der Anwendung sendet. Eine *DDE-Transaktion* ähnelt einer Nachricht, bei der es sich um eine benannte Konstante handelt, die von anderen Parametern begleitet wird, die zusätzliche Informationen zur Transaktion enthalten.

Die DDEML übergibt eine Transaktion an eine anwendungsdefinierte DDE-Rückruffunktion, die eine Aktion für den Typ der Transaktion ausgibt. Wenn eine Clientanwendung beispielsweise versucht, eine Konversation mit einer Serveranwendung herzustellen, ruft der Client die [**DdeConnect-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) auf. Diese Funktion bewirkt, dass DDEML eine [**XTYP \_ CONNECT-Transaktion**](xtyp-connect.md) an die DDE-Rückruffunktion des Servers sendet. Die Rückruffunktion kann die Konversation zulassen, indem **sie TRUE** an die DDEML zurücksendet, oder sie kann die Konversation verweigern, indem FALSE **zurückgegeben wird.** Eine ausführliche Erläuterung der Transaktionen finden Sie unter [Transaktionsverwaltung.](transaction-management.md)

## <a name="service-names-topic-names-and-item-names"></a>Dienstnamen, Themennamen und Elementnamen

Ein DDE-Server verwendet einen Drei-Ebenen-Hierarchiedienstnamen (in der vorherigen DDE-Dokumentation als "Anwendungsname" bezeichnet), einen Themennamen und einen Elementnamen, um eine Dateneinheit eindeutig zu identifizieren, die der Server während einer Konversation austauschen kann.

Ein *Dienstname ist* eine Zeichenfolge, auf die eine Serveranwendung reagiert, wenn ein Client versucht, eine Konversation mit dem Server herzustellen. Ein Client muss diesen Dienstnamen angeben, um eine Konversation mit dem Server herzustellen. Obwohl ein Server auf viele Dienstnamen antworten kann, antworten die meisten Server nur auf einen Namen.

Ein *Themenname ist* eine Zeichenfolge, die einen logischen Datenkontext identifiziert. Bei Servern, die dateibasierte Dokumente verwenden, sind Themennamen in der Regel Dateinamen. bei anderen Servern handelt es sich um andere anwendungsspezifische Zeichenfolgen. Ein Client muss einen Themennamen zusammen mit dem Dienstnamen eines Servers angeben, wenn er versucht, eine Konversation mit einem Server herzustellen.

Ein *Elementname ist* eine Zeichenfolge, die eine Dateneinheit identifiziert, die ein Server während einer Transaktion an einen Client übergeben kann. Beispielsweise kann ein Elementname eine ganze Zahl, eine Zeichenfolge, mehrere Textzeilen oder eine Bitmap identifizieren.

Mit den Dienst-, Themen- und Elementnamen kann der Client eine Konversation mit einem Server herstellen und Daten vom Server empfangen.

## <a name="system-topic"></a>Systemthema

Das Thema System bietet einen Kontext für Informationen, die für jeden DDE-Client von allgemeinem Interesse sind. Es wird empfohlen, dass Serveranwendungen das Thema System jederzeit unterstützen. Das Thema System wird in der DDEML definiert. H-Headerdatei als SZDDESYS \_ TOPIC.

Um zu bestimmen, welche Server vorhanden sind und welche Arten von Informationen sie bereitstellen können, kann eine Clientanwendung beim Start eine Konversation zum Thema System anfordern und den Gerätenamen auf **NULL festlegen.** Solche Platzhalter-Konversationen sind in Bezug auf die Systemleistung kostspielig, daher sollten sie auf ein Minimum beschränkt werden. Weitere Informationen zum Initiieren von DDE-Konversationen finden Sie unter [Conversation Management](conversation-management.md).

Ein Server muss die folgenden Elementnamen innerhalb des Themas System und alle anderen Elementnamen unterstützen, die für einen Client nützlich sind.



| Element                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SZDDE \_ ITEM \_ ITEMLIST    | Eine Liste der Elemente, die unter einem Nicht-Systemthema unterstützt werden. (Diese Liste kann von Moment zu Moment und von Thema zu Thema variieren.)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SZDDESYS-ELEMENTFORMATE \_ \_  | Eine durch Tabstopps getrennte Liste von Zeichenfolgen, die alle Formate der Zwischenablage darstellen, die möglicherweise von der Dienstanwendung unterstützt werden. Zeichenfolgen, die vordefinierte Zwischenablageformate darstellen, entsprechen den CF-Werten, bei denen \_ das Präfix \_ "CF" entfernt wurde. Beispielsweise wird das CF \_ TEXT-Format durch die Zeichenfolge "TEXT" dargestellt. Diese Zeichenfolgen müssen groß geschrieben werden, um sie weiter als vordefinierte Formate zu identifizieren. Die Liste der Formate muss in der Reihenfolge angezeigt werden, in der die Inhalte am meisten zu den am wenigsten inhaltsreich sind. Weitere Informationen zu Zwischenablageformaten und zum Rendern von Daten finden Sie unter [Zwischenablage](clipboard.md).<br/> |
| \_SZDDESYS-ELEMENTHILFE \_     | Benutzerlesbare Informationen von allgemeinem Interesse. Dieses Element muss mindestens Informationen zur Verwendung der DDE-Funktionen der Serveranwendung enthalten. Diese Informationen können u. a. angeben, wie Elemente in Themen angegeben werden, welche Ausführungszeichenfolgen der Server ausführen kann, welche Poke-Transaktionen zulässig sind und wie Hilfe zu anderen Systemthemaelementen zu finden ist.                                                                                                                                                                                                                           |
| SZDDESYS \_ ITEM \_ RTNMSG   | Unterstützende Details für die zuletzt verwendete [**WM \_ DDE \_ ACK-Meldung.**](wm-dde-ack.md) Dieses Element ist nützlich, wenn mehr als 8 Bits anwendungsspezifischer Rückgabedaten erforderlich sind.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_SZDDESYS-ELEMENTSTATUS \_   | Ein Hinweis auf den aktuellen Status des Servers. In der Regel unterstützt dieses Element nur das CF \_ TEXT-Format und enthält die Zeichenfolge Bereit oder Ausgelastet.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SZDDESYS-ELEMENT \_ \_ SYSITEMS | Eine Liste der Elemente, die von diesem Server unter dem Thema System unterstützt werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_SZDDESYS-ARTIKELTHEMEN \_   | Eine Liste der Themen, die vom Server zum aktuellen Zeitpunkt unterstützt werden. (Diese Liste kann von Moment zu Moment variieren.)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Diese Elementnamen sind Werte, die in der DDEML definiert sind. H-Headerdatei. Um Zeichenfolgenhandles für diese Zeichenfolgen zu erhalten, muss eine Anwendung die DDEML-Zeichenfolgenverwaltungsfunktionen wie bei jeder anderen Zeichenfolge in einer DDEML-Anwendung verwenden. Weitere Informationen zum Verwalten von Zeichenfolgen finden Sie unter [Zeichenfolgenverwaltung.](#string-management)

## <a name="initialization"></a>Initialisierung

Vor dem Aufrufen einer anderen DDEML-Funktion muss eine Anwendung die [**DdeInitialize-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) aufrufen. **DdeInitialize** erhält einen Instanzbezeichner für die Anwendung, registriert die DDE-Rückruffunktion der Anwendung beim DDE und gibt die Transaktionsfilterflags für die Rückruffunktion an.

Jede Instanz einer Anwendung oder DLL muss ihren Instanzbezeichner als *idInst-Parameter* an jede andere DDEML-Funktion übergeben, die sie erfordert. Der Zweck mehrerer DDEML-Instanzen besteht in der Unterstützung von DLLs, die die DDEML gleichzeitig verwenden müssen, wenn eine Anwendung sie verwendet. Eine Anwendung darf nicht mehr als eine Instanz der DDEML verwenden.

*Transaktionsfilter optimieren* die Systemleistung, indem verhindert wird, dass die DDEML unerwünschte Transaktionen an die DDE-Rückruffunktion der Anwendung übergehen kann. Eine Anwendung legt die Transaktionsfilter im [**DdeInitialize-Parameter**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) *ufCmd* fest. Eine Anwendung muss ein Transaktionsfilterflag für jeden Transaktionstyp angeben, den sie in der Rückruffunktion nicht verarbeiten kann. Eine Anwendung kann ihre Transaktionsfilter mit einem nachfolgenden Aufruf von **DdeInitialize ändern.** Weitere Informationen zu Transaktionen finden Sie unter [Transaktionsverwaltung.](transaction-management.md)

Das folgende Beispiel zeigt, wie eine Anwendung für die Verwendung der DDEML initialisiert wird.


```
DWORD idInst = 0; 
HINSTANCE hinst; 
 
DdeInitialize(&idInst,         // receives instance identifier 
    (PFNCALLBACK) DdeCallback, // pointer to callback function 
    CBF_FAIL_EXECUTES |        // filter XTYPE_EXECUTE 
    CBF_SKIP_ALLNOTIFICATIONS, // filter notifications 
    0); 
```



Eine Anwendung muss die [**DdeUninitialize-Funktion aufrufen,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) wenn sie die DDEML nicht mehr verwenden wird. Diese Funktion beendet alle derzeit für die Anwendung geöffneten Konversationen und gibt die DDEML-Ressourcen frei, die dem System für die Anwendung zugeordnet sind.

## <a name="callback-function"></a>Rückruffunktion

Eine Anwendung, die DDEML verwendet, muss eine Rückruffunktion bereitstellen, die die DDE-Ereignisse verarbeitet, die sich auf die Anwendung ausdehnen. Die DDEML benachrichtigt eine Anwendung über solche Ereignisse, indem Transaktionen an die DDE-Rückruffunktion der Anwendung sendet. Welche Transaktionen eine Rückruffunktion empfängt, hängt davon ab, welcher Rückruffilter die in [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) angegebene Anwendung kennzeichnet und ob es sich bei der Anwendung um einen Client, einen Server oder beides handelt. Weitere Informationen finden Sie unter [**DdeCallback**](/windows/win32/api/ddeml/nc-ddeml-pfncallback).

Das folgende Beispiel zeigt die allgemeine Struktur einer Rückruffunktion für eine typische Clientanwendung.


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



Der *uType-Parameter* gibt den Transaktionstyp an, der von der DDEML an die Rückruffunktion gesendet wird. Die Werte der verbleibenden Parameter hängen vom Transaktionstyp ab. Die Transaktionstypen und die Ereignisse, die sie generieren, werden in den folgenden Themen beschrieben. Ausführliche Informationen zu den einzelnen Transaktionstypen finden Sie unter [Transaktionsverwaltung.](transaction-management.md)

## <a name="string-management"></a>Zeichenfolgenverwaltung

Um eine DDE-Aufgabe auszuführen, benötigen viele DDEML-Funktionen Zugriff auf Zeichenfolgen. Beispielsweise muss ein Client einen Dienstnamen und einen Themennamen angeben, wenn er die [**DdeConnect-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) aufruft, um eine Konversation mit einem Server an fordern. Eine Anwendung gibt eine Zeichenfolge an, indem sie ein Zeichenfolgenhandle (String Handle, HSZ) anstelle eines Zeigers in einer DDEML-Funktion übergibt. Ein *Zeichenfolgenhand* handle ist ein vom System zugewiesener **DWORD-Wert,** der eine Zeichenfolge identifiziert.

Eine Anwendung kann ein Zeichenfolgenhandle für eine bestimmte Zeichenfolge abrufen, indem sie die [**DdeCreateStringHandle-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) aufruft. Diese Funktion registriert die Zeichenfolge beim System und gibt ein Zeichenfolgenhand handle an die Anwendung zurück. Die Anwendung kann das Handle an DDEML-Funktionen übergeben, die auf die Zeichenfolge zugreifen müssen. Im folgenden Beispiel werden Zeichenfolgenhandles für die Zeichenfolge des Systemthemas und die Dienstnamenzeichenfolge zurückgegeben.


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



Der *idInst-Parameter* im vorherigen Beispiel gibt den Instanzbezeichner an, der von der [**DdeInitialize-Funktion erhalten**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) wurde.

Die DDE-Rückruffunktion einer Anwendung empfängt während der meisten DDE-Transaktionen mindestens ein Zeichenfolgenhandles. Beispielsweise empfängt ein Server während der [**XTYP \_ REQUEST-Transaktion**](xtyp-request.md) zwei Zeichenfolgenhandles: einer identifiziert eine Zeichenfolge, die einen Themennamen angibt, und der andere identifiziert eine Zeichenfolge, die einen Elementnamen angibt. Eine Anwendung kann die Länge der Zeichenfolge abrufen, die einem Zeichenfolgenhand handle entspricht, und die Zeichenfolge in einen anwendungsdefinierten Puffer kopieren, indem sie die [**DdeQueryString-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) aufruft, wie im folgenden Beispiel gezeigt.


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



Ein instanzspezifisches Zeichenfolgenhand handle kann nicht vom Zeichenfolgenhand handle zur Zeichenfolge und zurück zum Zeichenfolgenhand handle zugeordnet werden. Obwohl [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) beispielsweise eine Zeichenfolge aus einem Zeichenfolgenhandle erstellt und [**dann DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) ein Zeichenfolgenhandle aus dieser Zeichenfolge erstellt, sind die beiden Handles nicht identisch, wie im folgenden Beispiel gezeigt.


```
DWORD idInst; 
DWORD cb; 
HSZ hszInst, hszNew; 
PSZ pszInst; 
DdeQueryString(idInst, hszInst, pszInst, cb, CP_WINANSI); 
hszNew = DdeCreateStringHandle(idInst, pszInst, CP_WINANSI); 
// hszNew != hszInst ! 
```



Verwenden Sie zum Vergleichen der Werte von zwei Zeichenfolgenhandles die [**DdeCmpStringHandles-Funktion.**](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles)

Ein Zeichenfolgenhand handle, das an die DDE-Rückruffunktion einer Anwendung übergeben wird, wird ungültig, wenn die Rückruffunktion zurückgegeben wird. Eine Anwendung kann ein Zeichenfolgenhandle zur Verwendung speichern, nachdem die Rückruffunktion mithilfe der [**DdeKeepStringHandle-Funktion zurückgegeben**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) wurde.

Wenn eine Anwendung [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea)aufruft, gibt das System die angegebene Zeichenfolge in eine Zeichenfolgentabelle ein und generiert ein Handle, das für den Zugriff auf die Zeichenfolge verwendet wird. Das System verwaltet auch eine Nutzungsanzahl für jede Zeichenfolge in der Zeichenfolgentabelle.

Wenn eine Anwendung [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) aufruft und eine Zeichenfolge angibt, die bereits in der Tabelle vorhanden ist, erhöht das System die Nutzungsanzahl, anstatt ein weiteres Vorkommen der Zeichenfolge hinzufügen zu müssen. (Eine Anwendung kann die Nutzungsanzahl auch mithilfe von [**DdeKeepStringHandle erhöhen.)**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) Wenn eine Anwendung die [**DdeFreeStringHandle-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle) aufruft, dekrementiert das System die Nutzungsanzahl.

Eine Zeichenfolge wird aus der Tabelle entfernt, wenn ihre Nutzungsanzahl 0 (null) entspricht. Da mehr als eine Anwendung das Handle für eine bestimmte Zeichenfolge abrufen kann, darf eine Anwendung ein Zeichenfolgenhand handle nicht mehrmals frei geben, als sie das Handle erstellt oder beibehalten hat. Andernfalls kann die Anwendung dazu führen, dass die Zeichenfolge aus der Tabelle entfernt wird, was anderen Anwendungen den Zugriff auf die Zeichenfolge verweigert.

Die DDEML-Zeichenfolgenverwaltungsfunktionen basieren auf dem Atom-Manager und unterliegen den gleichen Größenbeschränkungen wie Atome.

## <a name="ddeml-and-threads"></a>DDEML und Threads

Die [**DdeInitialize-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) registriert eine Anwendung bei der DDEML und erstellt eine DDEML-Instanz. Eine DDEML-Instanz ist thread-basiert und dem Thread zugeordnet, der **DdeInitialize aufgerufen hat.**

Alle DDEML-Funktionsaufrufe für Objekte, die zu einer DDEML-Instanz gehören, müssen aus demselben Thread erstellt werden, der [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) aufgerufen hat, um die Instanz zu erstellen. Wenn Sie eine DDEML-Funktion aus einem anderen Thread aufrufen, kann die Funktion nicht ausgeführt werden. Sie können nicht von einem anderen Thread als dem, der die Konversation zugeordnet hat, auf eine DDEML-Konversation zugreifen.

 

