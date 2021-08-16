---
title: Transaktionsverwaltung (Daten Exchange)
description: In diesem Thema wird erläutert, wie ein Client Transaktionen senden kann, um Daten und Dienste vom Server abzurufen.
ms.assetid: 2d08ffa3-cbd7-4806-b94f-979938322c38
keywords:
- Windows Benutzeroberfläche,dynamische Daten Exchange (DDE)
- dynamische Daten Exchange (DDE), Transaktionen
- DDE (dynamische Daten Exchange),Transaktionen
- Datenaustausch, dynamische Daten Exchange (DDE)
- Windows Benutzeroberfläche,dynamische Daten Exchange Management Library (DDEML)
- dynamische Daten Exchange Management Library (DDEML), Transaktionen
- DDEML (dynamische Daten Exchange Management Library),Transaktionen
- Datenaustausch,dynamische Daten Exchange Management Library (DDEML)
- dynamische Daten Exchange (DDE), Anforderungstransaktionen
- DDE (dynamische Daten Exchange),Anforderungstransaktionen
- dynamische Daten Exchange Management Library (DDEML), Anforderungstransaktionen
- DDEML (dynamische Daten Exchange Management Library),Anforderungstransaktionen
- dynamische Daten Exchange (DDE), transaktionen
- DDE (dynamische Daten Exchange),Transaktionen
- dynamische Daten Exchange Management Library (DDEML), transaktionen
- DDEML (dynamische Daten Exchange-Verwaltungsbibliothek),Transaktionen
- dynamische Daten Exchange (DDE),Beratung von Transaktionen
- DDE (dynamische Daten Exchange),Beratung von Transaktionen
- dynamische Daten Exchange Management Library (DDEML), Beratung von Transaktionen
- DDEML (dynamische Daten Exchange Management Library),Beratung von Transaktionen
- dynamische Daten Exchange (DDE),Transaktionen ausführen
- DDE (dynamische Daten Exchange),Transaktionen ausführen
- dynamische Daten Exchange Management Library (DDEML), Transaktionen ausführen
- DDEML (dynamische Daten Exchange Verwaltungsbibliothek),Transaktionen ausführen
- dynamische Daten Exchange (DDE), synchrone Transaktionen
- DDE (dynamische Daten Exchange),synchrone Transaktionen
- dynamische Daten Exchange Management Library (DDEML), synchrone Transaktionen
- DDEML (dynamische Daten Exchange Management Library),synchrone Transaktionen
- dynamische Daten Exchange (DDE), asynchrone Transaktionen
- DDE (dynamische Daten Exchange),asynchrone Transaktionen
- dynamische Daten Exchange Management Library (DDEML), asynchrone Transaktionen
- DDEML (dynamische Daten Exchange Management Library),asynchrone Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5065c9e909a4589cd7d2d157fc1151c2efd42a4ddfc3c29d84fd26f0ea184dea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128573"
---
# <a name="transaction-management-data-exchange"></a>Transaktionsverwaltung (Daten Exchange)

Nach dem Einrichten einer Konversation mit einem Server kann ein Client Transaktionen senden, um Daten und Dienste vom Server abzurufen.

In den folgenden Themen werden die Transaktionstypen beschrieben, die Clients für die Interaktion mit einem Server verwenden können.

-   [Anforderungstransaktion](#request-transaction)
-   [Transaktion der 100-Prozent-Transaktion](#poke-transaction)
-   [Advise-Transaktion](#advise-transaction)
-   [Transaktion ausführen](#execute-transaction)
-   [Synchrone und asynchrone Transaktionen](#synchronous-and-asynchronous-transactions)
-   [Transaktionssteuerung](#transaction-control)
-   [Transaktionsklassen](#transaction-classes)
-   [Transaktionstypen](#transaction-types)

## <a name="request-transaction"></a>Anforderungstransaktion

Eine Clientanwendung kann die [**XTYP \_ REQUEST-Transaktion**](xtyp-request.md) verwenden, um ein Datenelement von einer Serveranwendung anzufordern. Der Client ruft die [**DdeClientTransaction-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) auf, wobei **XTYP \_ REQUEST** als Transaktionstyp und das Datenelement angegeben werden, das die Anwendung benötigt.

Die dynamische Daten Exchange Management Library (DDEML) übergibt die [**XTYP \_ REQUEST-Transaktion**](xtyp-request.md) an den Server und gibt dabei den Themennamen, den Elementnamen und das vom Client angeforderte Datenformat an. Wenn der Server das angeforderte Thema, Element und Format unterstützt, sollte der Server ein Datenhandle zurückgeben, das den aktuellen Wert des Elements identifiziert. Die DDEML übergibt dieses Handle als Rückgabewert von [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)an den Client. Der Server sollte **NULL** zurückgeben, wenn er das angeforderte Thema, Element oder Format nicht unterstützt.

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) verwendet den *lpdwResult-Parameter,* um ein Transaktionsstatusflag an den Client zurückzugeben. Wenn der Server die [**XTYP \_ REQUEST-Transaktion**](xtyp-request.md) nicht verarbeitet, gibt **DdeClientTransaction** **NULL** zurück, und *lpdwResult* zeigt auf das Flag DDE \_ FNOTPROCESSED oder DDE \_ FBUSY. Wenn das DDE \_ FNOTPROCESSED-Flag zurückgegeben wird, kann der Client nicht ermitteln, warum der Server die Transaktion nicht verarbeitet hat.

Wenn ein Server die [**XTYP \_ REQUEST-Transaktion**](xtyp-request.md) nicht unterstützt, sollte er das CBF \_ FAIL \_ REQUESTS-Filterflag in der [**DdeInitialize-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) angeben. Dieses Flag verhindert, dass die DDEML die Transaktion an den Server sendet.

## <a name="poke-transaction"></a>Transaktion der 100-Prozent-Transaktion

Ein Client kann nicht angeforderte Daten an einen Server senden, indem [**er DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) verwendet, um eine [**\_ XTYP-TRANSAKTION**](xtyp-poke.md) AN die Rückruffunktion eines Servers zu senden.

Die Clientanwendung erstellt zunächst einen Puffer, der die an den Server zu sendenden Daten enthält, und übergibt dann einen Zeiger auf den Puffer als Parameter an [**DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) Alternativ kann der Client die [**DdeCreateDataHandle-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) verwenden, um ein Datenhandle abzurufen, das die Daten identifiziert, und das Handle dann an **DdeClientTransaction** zu übergeben. In beiden Fällen gibt der Client auch den Themennamen, den Elementnamen und das Datenformat an, wenn **er DdeClientTransaction aufruft.**

Die DDEML übergibt die [**\_ XTYP-TRANSAKTION**](xtyp-poke.md) an den Server und gibt dabei den Themennamen, den Elementnamen und das Datenformat an, die der Client angefordert hat. Um das Datenelement und -format zu akzeptieren, sollte der Server DDE \_ FACK zurückgeben. Um die Daten abzulehnen, sollte der Server DDE \_ FNOTPROCESSED zurückgeben. Wenn der Server zu ausgelastet ist, um die Daten zu akzeptieren, sollte der Server DDE \_ FBUSY zurückgeben.

Wenn [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) zurückgegeben wird, kann der Client den *lpdwResult-Parameter* verwenden, um auf das Transaktionsstatusflag zuzugreifen. Wenn das Flag DDE \_ FBUSY ist, sollte der Client die Transaktion später erneut senden.

Wenn ein Server die [**\_ XTYP-TRANSAKTION NICHT**](xtyp-poke.md) unterstützt, sollte er das CBF FAIL FAIL \_ \_ FAILES-Filterflag in [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)angeben. Dieses Flag verhindert, dass die DDEML diese Transaktion an den Server sendet.

## <a name="advise-transaction"></a>Advise-Transaktion

Eine Clientanwendung kann die DDEML verwenden, um einen oder mehrere Links zu Elementen in einer Serveranwendung herzustellen. Wenn ein solcher Link eingerichtet wurde, sendet der Server regelmäßig Updates über das verknüpfte Element an den Client (in der Regel, wenn sich der Wert des Elements ändert, das der Serveranwendung zugeordnet ist). Durch das Verknüpfen wird eine Advise-Schleife zwischen den beiden Anwendungen eingerichtet, die bis zum Ende des Clients vorhanden ist.

Es gibt zwei Arten von Empfehlungsschleifen: "heiß" und "warm". In einer hot advise-Schleife sendet der Server sofort ein Datenhandle, das den geänderten Wert identifiziert. In einer warmen Advise-Schleife benachrichtigt der Server den Client, dass sich der Wert des Elements geändert hat, sendet das Datenhandle jedoch erst, wenn der Client dies anfordert.

Ein Client kann eine hot advise-Schleife mit einem Server anfordern, indem er den [**XTYP \_ ADVSTART-Transaktionstyp**](xtyp-advstart.md) in einem Aufruf von [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)angibt. Um eine warme Advise-Schleife anzufordern, muss der Client das XTYPF \_ NODATA-Flag mit dem **XTYP \_ ADVSTART-Transaktionstyp** kombinieren. In beiden Fällen übergibt die DDEML die **XTYP \_ ADVSTART-Transaktion** an die rückruffunktion dynamische Daten Exchange (DDE) des Servers. Die DDE-Rückruffunktion des Servers sollte die Parameter untersuchen, die die **XTYP \_ ADVSTART-Transaktion** (einschließlich des angeforderten Formats, des Themennamens und des Elementnamens) begleitet, und dann **TRUE** zurückgeben, um der Advise-Schleife zu erlauben, oder **FALSE,** um sie zu verweigern.

Nachdem eine Advise-Schleife eingerichtet wurde, sollte die Serveranwendung die [**DdePostAdvise-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) aufrufen, wenn sich der Wert des Elements ändert, das dem angeforderten Elementnamen zugeordnet ist. Dieser Aufruf führt dazu, dass eine [**XTYP \_ AD TRANSACTIONQ-Transaktion**](xtyp-advreq.md) an die eigene DDE-Rückruffunktion des Servers gesendet wird. Die DDE-Rückruffunktion des Servers sollte ein Datenhandle zurückgeben, das den neuen Wert des Datenelements identifiziert. Die DDEML benachrichtigt den Client dann, dass sich das angegebene Element geändert hat, indem die [**XTYP \_ ADVDATA-Transaktion**](xtyp-advdata.md) an die DDE-Rückruffunktion des Clients gesendet wird.

Wenn der Client eine hot advise-Schleife angefordert hat, übergibt die DDEML das Datenhandle während der [**XTYP \_ ADVDATA-Transaktion**](xtyp-advdata.md) an das geänderte Element an den Client. Andernfalls kann der Client eine [**XTYP \_ REQUEST-Transaktion**](xtyp-request.md) senden, um das Datenhandle abzurufen.

Es ist möglich, dass ein Server Updates schneller sendet, als ein Client die neuen Daten verarbeiten kann. Die Geschwindigkeit von Updates kann ein Problem für einen Client sein, der lange Verarbeitungsvorgänge für die Daten ausführen muss. In diesem Fall sollte der Client das \_ XTYPF-ACKREQ-Flag angeben, wenn eine Advise-Schleife angefordert wird. Dieses Flag bewirkt, dass der Server wartet, bis der Client bestätigt, dass er ein Datenelement empfangen und verarbeitet hat, bevor der Server das nächste Datenelement sendet. Advise-Schleifen, die mit dem XTYPF ACKREQ-Flag eingerichtet werden, \_ sind mit schnellen Servern stabiler, können aber gelegentlich Updates übersehen. Advise-Schleifen, die ohne das \_ XTYPF-ACKREQ-Flag eingerichtet wurden, lassen updates garantiert nicht aus, solange der Client mit dem Server mithalten kann.

Ein Client kann eine Advise-Schleife beenden, indem er den [**XTYP \_ ADVSTOP-Transaktionstyp**](xtyp-advstop.md) in einem Aufruf von [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)angibt.

Wenn ein Server keine Advise-Schleifen unterstützt, sollte er das CBF \_ FAIL \_ ADVISE-Filterflag in der [**DdeInitialize-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) angeben. Dieses Flag verhindert, dass DDEML die [**XTYP \_ ADVSTART-**](xtyp-advstart.md) und [**XTYP \_ ADVSTOP-Transaktionen**](xtyp-advstop.md) an den Server sendet.

## <a name="execute-transaction"></a>Transaktion ausführen

Ein Client kann die [**XTYP \_ EXECUTE-Transaktion**](xtyp-execute.md) verwenden, um einen Server zum Ausführen eines Befehls oder einer Reihe von Befehlen zu veranlassen.

Um einen Serverbefehl auszuführen, erstellt der Client zunächst einen Puffer, der eine Befehlszeichenfolge für die Ausführung des Servers enthält, und übergibt dann entweder einen Zeiger auf den Puffer oder ein Datenhandle, das den Puffer identifiziert, wenn [**er DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)aufruft. Weitere erforderliche Parameter sind das Konversationshandle, das Zeichenfolgenhandle für Elementnamen, die Formatspezifikation und der [**XTYP \_ EXECUTE-Transaktionstyp.**](xtyp-execute.md) Eine Anwendung, die ein Datenhandle zum Übergeben von Ausführungsdaten erstellt, muss **NULL** für den *hszItem-Parameter* der [**DdeCreateDataHandle-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) und null für den *uFmt-Parameter* angeben.

Die DDEML übergibt die [**XTYP \_ EXECUTE-Transaktion**](xtyp-execute.md) an die DDE-Rückruffunktion des Servers und gibt den Formatnamen, das Konversationshandle, den Themennamen und das Datenhandle an, die die Befehlszeichenfolge identifizieren. Wenn der Server den Befehl unterstützt, sollte er die [**DdeAccessData-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) verwenden, um einen Zeiger auf die Befehlszeichenfolge abzurufen, den Befehl auszuführen und dann DDE \_ FACK zurückzugeben. Wenn der Server den Befehl nicht unterstützt oder die Transaktion nicht abschließen kann, sollte DDE \_ FNOTPROCESSED zurückgegeben werden. Der Server sollte DDE \_ FBUSY zurückgeben, wenn er zu stark ausgelastet ist, um die Transaktion abzuschließen.

Im Allgemeinen sollte die Rückruffunktion eines Servers die [**XTYP \_ EXECUTE-Transaktion**](xtyp-execute.md) verarbeiten, bevor mit den folgenden Ausnahmen zurückgegeben wird:

1.  Wenn der mit der [**XTYP \_ EXECUTE-Transaktion**](xtyp-execute.md) übergebene Befehl den Server zum Beenden anfordert, sollte der Server erst beendet werden, wenn seine Rückruffunktion von der Verarbeitung von **XTYP \_ EXECUTE** zurückgegeben wird.
2.  Wenn der Server einen Vorgang ausführen muss, z. B. die Verarbeitung eines Dialogfelds oder einer DDE-Transaktion, die DDEML-Rekursionsprobleme verursachen kann, sollte der Server den CBR \_ BLOCK-Rückgabecode zurückgeben, um die Ausführungstransaktion zu blockieren, den Vorgang auszuführen und dann die Verarbeitung der Ausführungstransaktion fortzusetzen.

Wenn [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) zurückgegeben wird, kann der Client den *lpdwResult-Parameter* verwenden, um auf das Transaktionsstatusflag zuzugreifen. Wenn das Flag DDE \_ FBUSY ist, sollte der Client die Transaktion später erneut senden.

Wenn ein Server die [**XTYP \_ EXECUTE-Transaktion**](xtyp-execute.md) nicht unterstützt, sollte er das CBF \_ FAIL \_ EXECUTES-Filterflag in der [**DdeInitialize-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) angeben. Dadurch wird verhindert, dass die DDEML die Transaktion an den Server sendet.

## <a name="synchronous-and-asynchronous-transactions"></a>Synchrone und asynchrone Transaktionen

Ein Client kann entweder synchrone oder asynchrone Transaktionen senden. In einer synchronen Transaktion gibt der Client einen Time out-Wert an, der die maximale Zeitspanne angibt, die auf die Verarbeitung der Transaktion durch den Server gewartet wird. [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) gibt erst dann zurück, wenn der Server die Transaktion verarbeitet, die Transaktion fehlschlägt oder der Time out-Wert abläuft. Der Client gibt den Time out-Wert an, wenn **er DdeClientTransaction** aufruft.

Während einer synchronen Transaktion wechselt der Client in eine modale Schleife, während er auf die Verarbeitung der Transaktion wartet. Der Client kann weiterhin Benutzereingaben verarbeiten, aber keine weitere synchrone Transaktion senden, bis [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) zurückgegeben wird.

Ein Client sendet eine asynchrone Transaktion, indem er das TIMEOUT \_ ASYNC-Flag in [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)angibt. Die Funktion gibt zurück, nachdem die Transaktion begonnen hat, und übergibt einen Transaktionsbezeichner an den Client. Wenn der Server die Verarbeitung der asynchronen Transaktion abgeschlossen hat, sendet die DDEML eine [**XTYP \_ XACT \_ COMPLETE-Transaktion**](xtyp-xact-complete.md) an den Client. Einer der Parameter, den DDEML während der **XTYP \_ XACT \_ COMPLETE-Transaktion** an den Client übergibt, ist der Transaktionsbezeichner. Indem dieser Transaktionsbezeichner mit dem von **DdeClientTransaction** zurückgegebenen Bezeichner verglichen wird, identifiziert der Client, welche asynchrone Transaktion der Server verarbeitet hat.

Ein Client kann die [**DdeSetUserHandle-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddesetuserhandle) als Hilfe bei der Verarbeitung einer asynchronen Transaktion verwenden. Diese Funktion ermöglicht es einem Client, einem Konversationshandle und einem Transaktionsbezeichner einen von der Anwendung definierten Wert zuzuordnen. Der Client kann die [**DdeQueryConvInfo-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) während der [**XTYP \_ XACT \_ COMPLETE-Transaktion**](xtyp-xact-complete.md) verwenden, um den von der Anwendung definierten Wert abzurufen. Aufgrund dieser Funktion muss eine Anwendung keine Liste aktiver Transaktionsbezeichner verwalten.

Wenn ein Client eine Anforderung für Daten mithilfe einer synchronen Transaktion erfolgreich abschließt, kann die DDEML nicht feststellen, wann der Client die empfangenen Daten verwendet hat. Die Clientanwendung muss das empfangene Datenhandle an die [**DdeFreeDataHandle-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) übergeben und die DDEML benachrichtigen, dass das Handle nicht mehr verwendet wird. Datenhandles, die von synchronen Transaktionen zurückgegeben werden, befinden sich effektiv im Besitz des Clients.

Wenn ein Server eine asynchrone Transaktion nicht rechtzeitig verarbeitet, kann der Client die Transaktion abbrechen, indem er die [**DdeAbtaxinTransaction-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeabandontransaction) aufruft. Die DDEML gibt alle Ressourcen frei, die der Transaktion zugeordnet sind, und verwirft die Ergebnisse der Transaktion, wenn die Verarbeitung durch den Server abgeschlossen ist. Ein Time out während einer synchronen Transaktion bricht die Transaktion effektiv ab.

Die asynchrone Transaktionsmethode wird für Anwendungen bereitgestellt, die eine große Anzahl von DDE-Transaktionen senden müssen, während gleichzeitig eine beträchtliche Verarbeitungsmenge ausgeführt wird, z. B. Berechnungen. Die asynchrone Methode ist auch in Anwendungen nützlich, die die Verarbeitung von DDE-Transaktionen vorübergehend beenden müssen, damit sie andere Aufgaben ohne Unterbrechung ausführen können. In den meisten anderen Situationen sollte eine Anwendung die synchrone Methode verwenden.

Synchrone Transaktionen sind einfacher zu verwalten und schneller als asynchrone Transaktionen. Allerdings kann jeweils nur eine synchrone Transaktion ausgeführt werden, während viele asynchrone Transaktionen gleichzeitig ausgeführt werden können. Bei synchronen Transaktionen kann ein langsamer Server dazu führen, dass ein Client im Leerlauf bleibt, während er auf eine Antwort wartet. Außerdem bewirken synchrone Transaktionen, dass der Client in eine modale Schleife eintritt, die die Nachrichtenfilterung in der eigenen Nachrichtenschleife der Anwendung umgehen könnte.

Wenn der Client eine Hookprozedur zum Filtern von Nachrichten installiert hat (d. h. den \_ WH-MSGFILTER-Hooktyp in einem Aufruf der [**SetWindowsHookEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa) angegeben hat), bewirkt eine synchrone Transaktion nicht, dass das System die Hookprozedur umgeht. Wenn ein Eingabeereignis auftritt, während der Client auf das Ende einer synchronen Transaktion wartet, empfängt die Hookprozedur einen \_ MSGF-DDEMGR-Hookcode. Die Hauptgefahr bei der Verwendung einer modalen synchronen Transaktionsschleife besteht darin, dass eine modale Schleife, die von einem Dialogfeld erstellt wird, den Vorgang beeinträchtigen kann. Asynchrone Transaktionen sollten immer verwendet werden, wenn die DDEML von einer DLL verwendet wird.

## <a name="transaction-control"></a>Transaktionssteuerung

Eine Anwendung kann Transaktionen an ihre DDE-Rückruffunktion anhalten, entweder die Transaktionen, die einem bestimmten Konversationshandle zugeordnet sind, oder alle Transaktionen, unabhängig vom Konversationshandle. Diese Funktion ist nützlich, wenn eine Anwendung eine Transaktion empfängt, die eine lange Verarbeitung erfordert. In einem solchen Fall kann die Anwendung den CBR \_ BLOCK-Rückgabecode zurückgeben, um zukünftige Transaktionen, die dem Konversationshandle der Transaktion zugeordnet sind, anzuordnen, sodass die Anwendung andere Konversationen verarbeiten kann.

Nach Abschluss der Verarbeitung ruft die Anwendung die [**DdeEnableCallback-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) auf, um Transaktionen fortzusetzen, die der angehaltenen Konversation zugeordnet sind. Der Aufruf von **DdeEnableCallback** bewirkt, dass die DDEML die Transaktion erneut einfügt, die dazu geführt hat, dass die Anwendung die Konversation angehalten hat. Daher sollte die Anwendung das Ergebnis der Transaktion so speichern, dass sie das Ergebnis abrufen und zurückgeben kann, ohne die Transaktion erneut zu verarbeiten.

Eine Anwendung kann alle Transaktionen anhalten, die einem bestimmten Konversationshandle zugeordnet sind, indem das Handle und das EC \_ DISABLE-Flag in einem Aufruf von [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)angegeben werden. Durch Angeben eines **NULL-Handles** kann eine Anwendung alle Transaktionen für alle Konversationen anhalten.

Wenn eine Konversation angehalten wurde, speichert die DDEML Transaktionen für die Konversation in einer Transaktionswarteschlange. Wenn die Anwendung die Konversation erneut eingibt, entfernt die DDEML die gespeicherten Transaktionen aus der Warteschlange und übergibt jede Transaktion an die entsprechende Rückruffunktion. Die Kapazität der Transaktionswarteschlange ist groß, aber eine Anwendung sollte eine angehaltene Konversation so schnell wie möglich wieder verfügbar machen, um den Verlust von Transaktionen zu vermeiden.

Eine Anwendung kann die übliche Transaktionsverarbeitung fortsetzen, indem sie das EC \_ ENABLEALL-Flag in [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)angibt. Für eine kontrolliertere Wiederaufnahme der Transaktionsverarbeitung kann die Anwendung das EC \_ ENABLEONE-Flag angeben. Dieses Flag entfernt eine Transaktion aus der Transaktionswarteschlange und übergibt sie an die entsprechende Rückruffunktion. Nachdem diese Transaktion verarbeitet wurde, werden alle Konversationen wieder deaktiviert.

Wenn das EC \_ ENABLEONE-Flag und ein Konversationshandle im Aufruf von [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)angegeben sind, wird nur diese Konversation blockiert, nachdem die Transaktion verarbeitet wurde. Wenn  ein NULL-Konversationshandle angegeben wird, werden alle Konversationen blockiert, nachdem eine Transaktion in einer Beliebigen Konversation verarbeitet wurde.

## <a name="transaction-classes"></a>Transaktionsklassen

Die DDEML verfügt über vier Klassen von Transaktionen. Jede Klasse wird durch eine Konstante identifiziert, die mit dem \_ XCLASS-Präfix beginnt. Die Klassen werden in der DDEML-Headerdatei definiert. Der Klassenwert wird mit dem Transaktionstypwert kombiniert und an die DDE-Rückruffunktion der empfangenden Anwendung übergeben.

Die -Klasse einer Transaktion bestimmt den Rückgabewert, der von einer Rückruffunktion zurückgegeben werden soll, wenn sie die Transaktion verarbeitet. Die folgenden Rückgabewerte und Transaktionstypen sind jeder der vier Transaktionsklassen zugeordnet.



| Klasse                | Rückgabewert                                                     | Transaktion                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| XCLASS \_ BOOL         | **TRUE** oder **FALSE**                                            | [**XTYP \_ ADVSTART**](xtyp-advstart.md)<br/> [**XTYP \_ CONNECT**](xtyp-connect.md)<br/>                                                                                                                                                                                                                                                                                            |
| XCLASS \_ DATA         | Ein Datenhandle, der CBR \_ BLOCK-Rückgabecode oder **NULL**           | [**XTYP \_ AD AUSLASSUNGSZEICHEN**](xtyp-advreq.md)<br/> [**XTYP \_ REQUEST**](xtyp-request.md)<br/> [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md)<br/>                                                                                                                                                                                                                                       |
| \_XCLASS-FLAGS        | Ein Transaktionsflag: DDE \_ FACK, DDE \_ FBUSY oder DDE \_ FNOTPROCESSED | [**XTYP \_ ADVDATA**](xtyp-advdata.md)<br/> [**XTYP \_ EXECUTE**](xtyp-execute.md)<br/> [**\_XTYP-TYPISCHEN**](xtyp-poke.md)<br/>                                                                                                                                                                                                                                                   |
| \_XCLASS-BENACHRICHTIGUNG | Keine                                                             | [**XTYP \_ ADVSTOP**](xtyp-advstop.md)<br/> [**XTYP \_ CONNECT \_ CONFIRM**](xtyp-connect-confirm.md)<br/> [**XTYP \_ DISCONNECT**](xtyp-disconnect.md)<br/> [**\_XTYP-FEHLER**](xtyp-error.md)<br/> [**XTYP \_ REGISTER**](xtyp-register.md)<br/> [**XTYP \_ UNREGISTER**](xtyp-unregister.md)<br/> [**XTYP \_ XACT \_ COMPLETE**](xtyp-xact-complete.md)<br/> |



 

## <a name="transaction-types"></a>Transaktionstypen

Jeder DDE-Transaktionstyp verfügt über einen Empfänger und eine zugeordnete Aktivität, die bewirkt, dass die DDEML jeden Typ generiert.



| Transaktionstyp                                       | Receiver                   | Ursache                                                                                                                                                                         |
|--------------------------------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XTYP \_ ADVDATA**](xtyp-advdata.md)                  | Client                     | Ein Server hat auf eine [**XTYP \_ ADTYPQ-Transaktion**](xtyp-advreq.md) geantwortet, indem er ein Datenhand handle zurücksendet.                                                                          |
| [**XTYP \_ ADAKKAQ**](xtyp-advreq.md)                    | Server                     | Ein Server mit dem Namen [**DdePostAdvise-Funktion,**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) der angibt, dass sich der Wert eines Datenelements in einer Advise-Schleife geändert hat.                                  |
| [**XTYP \_ ADVSTART**](xtyp-advstart.md)                | Server                     | Ein Client hat den [**XTYP \_ ADVSTART-Transaktionstyp**](xtyp-advstart.md) in einem Aufruf der [**DdeClientTransaction-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) angegeben.               |
| [**XTYP \_ ADVSTOP**](xtyp-advstop.md)                  | Server                     | Ein Client hat den [**XTYP \_ ADVSTOP-Transaktionstyp**](xtyp-advstop.md) in einem Aufruf von [**DdeClientTransaction angegeben.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)                              |
| [**XTYP \_ CONNECT**](xtyp-connect.md)                  | Server                     | Ein Client hat die [**DdeConnect-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) aufgerufen und einen dienst- und themennamen angegeben, der vom Server unterstützt wird.                                            |
| [**XTYP \_ CONNECT \_ CONFIRM**](xtyp-connect-confirm.md) | Server                     | Der Server hat **TRUE** als Reaktion auf eine [**XTYP \_ CONNECT- oder**](xtyp-connect.md) [**XTYP \_ WILDCONNECT-Transaktion**](xtyp-wildconnect.md) zurückgegeben.                            |
| [**XTYP \_ DISCONNECT**](xtyp-disconnect.md)            | Client/Server              | Ein Partner in einer Konversation namens [**DdeDisconnect-Funktion,**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) wodurch beide Partner diese Transaktion erhalten.                                    |
| [**\_XTYP-FEHLER**](xtyp-error.md)                      | Client/Server              | Ein kritischer Fehler ist aufgetreten. Die DDEML hat möglicherweise nicht genügend Ressourcen, um fortzufahren.                                                                                       |
| [**XTYP \_ EXECUTE**](xtyp-execute.md)                  | Server                     | Ein Client hat den [**XTYP \_ EXECUTE-Transaktionstyp**](xtyp-execute.md) in einem Aufruf von [**DdeClientTransaction angegeben.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)                              |
| [**XTYP \_ MONITOR**](xtyp-monitor.md)                  | DDE-Überwachungsanwendung | Im System ist ein DDE-Ereignis aufgetreten. Weitere Informationen zu DDE-Überwachungsanwendungen finden Sie unter [Überwachen von Anwendungen.](monitoring-applications.md)                       |
| [**XTYP \_ POKE**](xtyp-poke.md)                        | Server                     | Ein Client hat den [**XTYP \_ POKE-Transaktionstyp**](xtyp-poke.md) in einem Aufruf von [**DdeClientTransaction angegeben.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)                                    |
| [**XTYP \_ REGISTER**](xtyp-register.md)                | Client/Server              | Eine Serveranwendung hat die [**DdeNameService-Funktion verwendet,**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) um einen Dienstnamen zu registrieren.                                                                   |
| [**\_XTYP-ANFORDERUNG**](xtyp-request.md)                  | Server                     | Ein Client hat den [**XTYP \_ REQUEST-Transaktionstyp**](xtyp-request.md) in einem Aufruf von [**DdeClientTransaction angegeben.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)                              |
| [**XTYP \_ UNREGISTER**](xtyp-unregister.md)            | Client/Server              | Eine Serveranwendung hat [**DdeNameService verwendet,**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) um die Registrierung eines Dienstnamens zu aufheben.                                                                              |
| [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md)          | Server                     | Ein Client mit dem Namen [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) oder [**DdeConnectList,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) der **NULL** für den Dienstnamen, den Themennamen oder beides angibt. |
| [**XTYP \_ XACT \_ COMPLETE**](xtyp-xact-complete.md)     | Client                     | Eine asynchrone Transaktion, die gesendet wird, wenn der Client das TIMEOUT ASYNC-Flag in einem Aufruf von \_ [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)angegeben hat, wurde abgeschlossen.         |



 

 

