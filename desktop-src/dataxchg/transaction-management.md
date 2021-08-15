---
title: Transaktionsverwaltung (Exchange)
description: In diesem Thema wird erläutert, wie ein Client Transaktionen senden kann, um Daten und Dienste vom Server zu erhalten.
ms.assetid: 2d08ffa3-cbd7-4806-b94f-979938322c38
keywords:
- Windows Benutzeroberfläche,dynamische Daten Exchange (DDE)
- dynamische Daten Exchange (DDE), Transaktionen
- DDE (dynamische Daten Exchange),Transaktionen
- Datenaustausch,dynamische Daten Exchange (DDE)
- Windows Benutzeroberfläche,dynamische Daten Exchange Management Library (DDEML)
- dynamische Daten Exchange Management Library (DDEML), Transaktionen
- DDEML (dynamische Daten Exchange Management Library), Transaktionen
- Datenaustausch,dynamische Daten Exchange Management Library (DDEML)
- dynamische Daten Exchange (DDE), Anforderungstransaktionen
- DDE (dynamische Daten Exchange), Anforderungstransaktionen
- dynamische Daten Exchange Management Library (DDEML), Anforderungstransaktionen
- DDEML (dynamische Daten Exchange Management Library), Anforderungstransaktionen
- dynamische Daten Exchange (DDE), Poke-Transaktionen
- DDE (dynamische Daten Exchange),Poke-Transaktionen
- dynamische Daten Exchange Management Library (DDEML), Poke-Transaktionen
- DDEML (dynamische Daten Exchange Management Library), Poke-Transaktionen
- dynamische Daten Exchange (DDE), Transaktionen empfehlen
- DDE (dynamische Daten Exchange),Advise-Transaktionen
- dynamische Daten Exchange Management Library (DDEML), Transaktionen empfehlen
- DDEML (dynamische Daten Exchange Management Library),advise transactions
- dynamische Daten Exchange (DDE), Transaktionen ausführen
- DDE (dynamische Daten Exchange), Transaktionen ausführen
- dynamische Daten Exchange Management Library (DDEML), Transaktionen ausführen
- DDEML (dynamische Daten Exchange Management Library), Transaktionen ausführen
- dynamische Daten Exchange (DDE), synchrone Transaktionen
- DDE (dynamische Daten Exchange),synchrone Transaktionen
- dynamische Daten Exchange Management Library (DDEML), synchrone Transaktionen
- DDEML (dynamische Daten Exchange Management Library), synchrone Transaktionen
- dynamische Daten Exchange (DDE), asynchrone Transaktionen
- DDE (dynamische Daten Exchange),asynchrone Transaktionen
- dynamische Daten Exchange Management Library (DDEML), asynchrone Transaktionen
- DDEML (dynamische Daten Exchange Management Library), asynchrone Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5065c9e909a4589cd7d2d157fc1151c2efd42a4ddfc3c29d84fd26f0ea184dea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128573"
---
# <a name="transaction-management-data-exchange"></a>Transaktionsverwaltung (Exchange)

Nachdem eine Konversation mit einem Server hergestellt wurde, kann ein Client Transaktionen senden, um Daten und Dienste vom Server zu erhalten.

In den folgenden Themen werden die Transaktionstypen beschrieben, die Clients für die Interaktion mit einem Server verwenden können.

-   [Anforderungstransaktion](#request-transaction)
-   [Poke-Transaktion](#poke-transaction)
-   [Transaktion empfehlen](#advise-transaction)
-   [Transaktion ausführen](#execute-transaction)
-   [Synchrone und asynchrone Transaktionen](#synchronous-and-asynchronous-transactions)
-   [Transaktionssteuerung](#transaction-control)
-   [Transaktionsklassen](#transaction-classes)
-   [Transaktionstypen](#transaction-types)

## <a name="request-transaction"></a>Anforderungstransaktion

Eine Clientanwendung kann mithilfe der [**XTYP \_ REQUEST-Transaktion**](xtyp-request.md) ein Datenelement von einer Serveranwendung anfordern. Der Client ruft die [**DdeClientTransaction-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) auf, gibt **XTYP \_ REQUEST** als Transaktionstyp und das datenelement an, das die Anwendung benötigt.

Die dynamische Daten Exchange Management Library (DDEML) übergibt die [**XTYP \_ REQUEST-Transaktion**](xtyp-request.md) an den Server und gibt dabei den Vom Client angeforderten Themennamen, Elementnamen und das Datenformat an. Wenn der Server das angeforderte Thema, Element und Format unterstützt, sollte der Server ein Datenhand handle zurückgeben, das den aktuellen Wert des Elements identifiziert. Die DDEML übergibt dieses Handle als Rückgabewert von [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)an den Client. Der Server sollte **NULL zurückgeben,** wenn er das angeforderte Thema, Element oder Format nicht unterstützt.

[**DdeClientTransaction verwendet**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) den *lpdwResult-Parameter,* um ein Transaktionsstatusflag an den Client zurückgibt. Wenn der Server die [**XTYP \_ REQUEST-Transaktion**](xtyp-request.md) nicht verarbeitet, gibt **DdeClientTransaction** **NULL** zurück, und *lpdwResult* zeigt auf das Flag \_ DDE FNOTPROCESSED oder \_ DDE FBUSY. Wenn das Flag DDE FNOTPROCESSED zurückgegeben wird, kann der Client nicht ermitteln, warum der Server \_ die Transaktion nicht verarbeitet hat.

Wenn ein Server die [**XTYP \_ REQUEST-Transaktion**](xtyp-request.md) nicht unterstützt, sollte er das CBF FAIL REQUESTS-Filterflag \_ in der \_ [**DdeInitialize-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) angeben. Dieses Flag verhindert, dass die DDEML die Transaktion an den Server sendet.

## <a name="poke-transaction"></a>Poke-Transaktion

Ein Client kann nicht angeforderte Daten an einen Server senden, indem [**er DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) verwendet, um eine [**XTYP \_ POKE-Transaktion**](xtyp-poke.md) an die Rückruffunktion eines Servers zu senden.

Die Clientanwendung erstellt zunächst einen Puffer, der die an den Server zu sendenden Daten enthält, und übergibt dann einen Zeiger auf den Puffer als Parameter an [**DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) Alternativ kann der Client die [**DdeCreateDataHandle-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) verwenden, um ein Datenhandle zu erhalten, das die Daten identifiziert, und das Handle dann **an DdeClientTransaction übergeben.** In beiden Fällen gibt der Client auch den Themennamen, den Elementnamen und das Datenformat an, wenn **er DdeClientTransaction aufruft.**

Die DDEML übergibt die [**XTYP \_ POKE-Transaktion**](xtyp-poke.md) an den Server und gibt dabei den Themennamen, den Elementnamen und das Datenformat an, das der Client angefordert hat. Um das Datenelement und -format zu akzeptieren, sollte der Server DDE \_ FACK zurückgeben. Um die Daten abzulehnen, sollte der Server DDE \_ FNOTPROCESSED zurückgeben. Wenn der Server zu ausgelastet ist, um die Daten zu akzeptieren, sollte der Server DDE \_ FBUSY zurückgeben.

Wenn [**DdeClientTransaction zurückgegeben**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) wird, kann der Client den *lpdwResult-Parameter* verwenden, um auf das Transaktionsstatusflag zuzugreifen. Wenn das Flag DDE \_ FBUSY ist, sollte der Client die Transaktion später erneut senden.

Wenn ein Server die [**XTYP \_ POKE-Transaktion**](xtyp-poke.md) nicht unterstützt, sollte er das CBF \_ FAIL POKES-Filterflag in \_ [**DdeInitialize angeben.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Dieses Flag verhindert, dass die DDEML diese Transaktion an den Server sendet.

## <a name="advise-transaction"></a>Transaktion empfehlen

Eine Clientanwendung kann DDEML verwenden, um einen oder mehrere Links zu Elementen in einer Serveranwendung herzustellen. Wenn ein solcher Link eingerichtet wurde, sendet der Server regelmäßige Updates über das verknüpfte Element an den Client (in der Regel immer, wenn sich der Wert des Elements ändert, das der Serveranwendung zugeordnet ist). Beim Verknüpfen wird eine Advise-Schleife zwischen den beiden Anwendungen erstellt, die so lange bestehen bleibt, bis der Client sie beendet.

Es gibt zwei Arten von Advise-Schleifen: "heiß" und "warm". In einer Hot-Advise-Schleife sendet der Server sofort ein Datenhand handle, das den geänderten Wert identifiziert. In einer warmen Advise-Schleife benachrichtigt der Server den Client darüber, dass sich der Wert des Elements geändert hat, sendet das Datenhand handle jedoch erst, wenn der Client es anfing.

Ein Client kann eine Hot-Advise-Schleife mit einem Server anfordern, indem er den [**XTYP \_ ADVSTART-Transaktionstyp**](xtyp-advstart.md) in einem Aufruf von [**DdeClientTransaction ankämmt.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) Zum Anfordern einer warm advise-Schleife muss der Client das XTYPF NODATA-Flag mit \_ dem **XTYP \_ ADVSTART-Transaktionstyp** kombinieren. In beiden Fall übergibt die DDEML die **XTYP \_ ADVSTART-Transaktion** an die rückruffunktion dynamische Daten Exchange (DDE) des Servers. Die DDE-Rückruffunktion des Servers sollte die Parameter untersuchen, die die **XTYP \_ ADVSTART-Transaktion** begleiten (einschließlich des angeforderten Formats, des Themennamens und des Elementnamens) und dann **TRUE** zurückgeben, damit die Advise-Schleife oder **FALSE** sie verweigern kann.

Nachdem eine Advise-Schleife eingerichtet wurde, sollte die Serveranwendung die [**DdePostAdvise-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) aufrufen, wenn sich der Wert des Elements ändert, das dem angeforderten Elementnamen zugeordnet ist. Dieser Aufruf führt dazu, dass [**eine XTYP \_ ADPROTOKOLLQ-Transaktion**](xtyp-advreq.md) an die eigene DDE-Rückruffunktion des Servers gesendet wird. Die DDE-Rückruffunktion des Servers sollte ein Datenhand handle zurückgeben, das den neuen Wert des Datenelements identifiziert. Die DDEML benachrichtigt dann den Client, dass sich das angegebene Element geändert hat, indem die [**XTYP \_ ADVDATA-Transaktion**](xtyp-advdata.md) an die DDE-Rückruffunktion des Clients sendet.

Wenn der Client eine Hot Advise-Schleife angefordert hat, übergibt die DDEML das Datenhandle während der [**XTYP \_ ADVDATA-Transaktion**](xtyp-advdata.md) an das geänderte Element an den Client. Andernfalls kann der Client eine [**XTYP \_ REQUEST-Transaktion**](xtyp-request.md) senden, um das Datenhand handle zu erhalten.

Es ist möglich, dass ein Server Updates schneller sendet, als ein Client die neuen Daten verarbeiten kann. Die Geschwindigkeit von Updates kann ein Problem für einen Client sein, der lange Verarbeitungsvorgänge für die Daten ausführen muss. In diesem Fall sollte der Client beim Anfordern einer Advise-Schleife das Flag XTYPF \_ ACKREQ angeben. Dieses Flag bewirkt, dass der Server wartet, bis der Client bestätigt, dass er ein Datenelement empfangen und verarbeitet hat, bevor der Server das nächste Datenelement sendet. Advise-Schleifen, die mit dem XTYPF ACKREQ-Flag eingerichtet werden, sind stabiler bei schnellen Servern, können aber gelegentlich \_ Updates übersehen. Advise-Schleifen, die ohne das XTYPF-ACKREQ-Flag eingerichtet wurden, werden updates garantiert nicht übersehen, solange der Client mit \_ dem Server auf dem Laufenden bleibt.

Ein Client kann eine Advise-Schleife beenden, indem der [**XTYP \_ ADVSTOP-Transaktionstyp**](xtyp-advstop.md) in einem Aufruf von [**DdeClientTransaction angegeben wird.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)

Wenn ein Server keine Advise-Schleifen unterstützt, sollte er das CBF FAIL ADVISES-Filterflag \_ in der \_ [**DdeInitialize-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) angeben. Dieses Flag verhindert, dass die DDEML die [**XTYP \_ ADVSTART-**](xtyp-advstart.md) und [**XTYP \_ ADVSTOP-Transaktionen**](xtyp-advstop.md) an den Server sendet.

## <a name="execute-transaction"></a>Transaktion ausführen

Ein Client kann die [**XTYP \_ EXECUTE-Transaktion**](xtyp-execute.md) verwenden, um zu bewirken, dass ein Server einen Befehl oder eine Reihe von Befehlen ausführt.

Um einen Serverbefehl auszuführen, erstellt der Client zunächst einen Puffer, der eine Befehlszeichenfolge für die Ausführung des Servers enthält, und übergibt dann entweder einen Zeiger auf den Puffer oder ein Datenhand handle, das den Puffer identifiziert, wenn [**DdeClientTransaction aufruft.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) Weitere erforderliche Parameter sind das Konversationshand handle, das Elementnamen-Zeichenfolgenhand handle, die Formatspezifikation und der [**XTYP \_ EXECUTE-Transaktionstyp.**](xtyp-execute.md) Eine Anwendung, die ein Datenhandle zur Übergabe von Ausführungsdaten erstellt, muss **NULL** für den *hszItem-Parameter* der [**DdeCreateDataHandle-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) und 0 (null) für den *uFmt-Parameter* angeben.

Die DDEML übergibt die [**XTYP \_ EXECUTE-Transaktion**](xtyp-execute.md) an die DDE-Rückruffunktion des Servers und gibt den Formatnamen, das Konversationshandle, den Themennamen und das Datenhandle an, die die Befehlszeichenfolge identifizieren. Wenn der Server den Befehl unterstützt, sollte er die [**DdeAccessData-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) verwenden, um einen Zeiger auf die Befehlszeichenfolge zu erhalten, den Befehl auszuführen und dann DDE \_ FACK zurückgibt. Wenn der Server den Befehl nicht unterstützt oder die Transaktion nicht abschließen kann, sollte er DDE \_ FNOTPROCESSED zurückgeben. Der Server sollte DDE FBUSY zurückgeben, wenn er zu ausgelastet \_ ist, um die Transaktion abzuschließen.

Im Allgemeinen sollte die Rückruffunktion eines Servers die [**XTYP \_ EXECUTE-Transaktion**](xtyp-execute.md) vor der Rückgabe mit den folgenden Ausnahmen verarbeiten:

1.  Wenn der mit der [**XTYP \_ EXECUTE-Transaktion**](xtyp-execute.md) übergebene Befehl den Server zum Beenden an fordert, sollte der Server erst beendet werden, nachdem die Rückruffunktion von der Verarbeitung von XTYP EXECUTE zurückgegeben **\_ wurde.**
2.  Wenn der Server einen Vorgang ausführen muss, z. B. die Verarbeitung eines Dialogfelds oder einer DDE-Transaktion, die zu DDEML-Rekursionsproblemen führen kann, sollte der Server den CBR BLOCK-Rückgabecode zurückgeben, um die Transaktion auszuführen, den Vorgang auszuführen und dann die Verarbeitung der Transaktion \_ fortsetzen.

Wenn [**DdeClientTransaction zurückgegeben**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) wird, kann der Client den *lpdwResult-Parameter* verwenden, um auf das Transaktionsstatusflag zuzugreifen. Wenn das Flag DDE \_ FBUSY ist, sollte der Client die Transaktion später erneut senden.

Wenn ein Server die [**XTYP \_ EXECUTE-Transaktion**](xtyp-execute.md) nicht unterstützt, sollte er das CBF FAIL EXECUTES-Filterflag \_ in der \_ [**DdeInitialize-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) angeben. Dadurch wird verhindert, dass die DDEML die Transaktion an den Server sendet.

## <a name="synchronous-and-asynchronous-transactions"></a>Synchrone und asynchrone Transaktionen

Ein Client kann synchrone oder asynchrone Transaktionen senden. In einer synchronen Transaktion gibt der Client einen Time out-Wert an, der die maximale Wartezeit angibt, bis der Server die Transaktion verarbeiten kann. [**DdeClientTransaction wird erst**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) zurückgegeben, wenn der Server die Transaktion verarbeitet, die Transaktion fehlschlägt oder der Time out-Wert abläuft. Der Client gibt den Time out-Wert an, wenn **er DdeClientTransaction aufruft.**

Während einer synchronen Transaktion geht der Client in eine modale Schleife über, während auf die Verarbeitung der Transaktion gewartet wird. Der Client kann weiterhin Benutzereingaben verarbeiten, aber erst dann eine weitere synchrone Transaktion senden, wenn [**DdeClientTransaction zurückgegeben**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) wird.

Ein Client sendet eine asynchrone Transaktion durch Angabe des TIMEOUT \_ ASYNC-Flags in [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Die Funktion gibt zurück, nachdem die Transaktion begonnen hat, und übergibt einen Transaktionsbezeichner an den Client. Wenn der Server die Verarbeitung der asynchronen Transaktion abgeschlossen hat, sendet die DDEML eine [**XTYP \_ XACT \_ COMPLETE-Transaktion**](xtyp-xact-complete.md) an den Client. Einer der Parameter, die die DDEML während der **\_ XTYP XACT \_ COMPLETE-Transaktion** an den Client übergibt, ist der Transaktionsbezeichner. Indem dieser Transaktionsbezeichner mit dem von **DdeClientTransaction** zurückgegebenen Bezeichner verglichen wird, identifiziert der Client, welche asynchrone Transaktion der Server verarbeitet hat.

Ein Client kann die [**DdeSetUserHandle-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddesetuserhandle) als Hilfe bei der Verarbeitung einer asynchronen Transaktion verwenden. Mit dieser Funktion kann ein Client einen anwendungsdefinierten Wert einem Konversationshand handle und einem Transaktionsbezeichner zuordnen. Der Client kann die [**DdeQueryConvInfo-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) während der [**XTYP \_ XACT \_ COMPLETE-Transaktion**](xtyp-xact-complete.md) verwenden, um den anwendungsdefinierten Wert zu erhalten. Aufgrund dieser Funktion muss eine Anwendung keine Liste aktiver Transaktionsbezeichner verwalten.

Wenn ein Client eine Datenanforderung mithilfe einer synchronen Transaktion erfolgreich abgeschlossen hat, kann die DDEML nicht feststellen, wann der Client die empfangenen Daten nicht mehr verwendet hat. Die Clientanwendung muss das empfangene Datenhandle an die [**DdeFreeDataHandle-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) übergeben und dem DDEML mitteilen, dass das Handle nicht mehr verwendet wird. Datenhandles, die von synchronen Transaktionen zurückgegeben werden, befinden sich im effektiven Besitz des Clients.

Wenn ein Server eine asynchrone Transaktion nicht rechtzeitig verarbeiten kann, kann der Client die Transaktion durch Aufrufen der [**DdeAbungnTransaction-Funktion verabbruchen.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeabandontransaction) Die DDEML gibt alle ressourcen frei, die der Transaktion zugeordnet sind, und verwirft die Ergebnisse der Transaktion, wenn die Verarbeitung durch den Server abgeschlossen ist. Ein Time out während einer synchronen Transaktion bricht die Transaktion effektiv ab.

Die asynchrone Transaktionsmethode wird für Anwendungen bereitgestellt, die eine große Anzahl von DDE-Transaktionen senden müssen, während gleichzeitig eine beträchtliche Menge an Verarbeitungen ausgeführt wird, z. B. Berechnungen. Die asynchrone Methode ist auch in Anwendungen nützlich, die die Verarbeitung von DDE-Transaktionen vorübergehend beenden müssen, damit sie andere Aufgaben ohne Unterbrechung ausführen können. In den meisten anderen Situationen sollte eine Anwendung die synchrone -Methode verwenden.

Synchrone Transaktionen sind einfacher zu verwalten und schneller als asynchrone Transaktionen. Es kann jedoch nur eine synchrone Transaktion gleichzeitig ausgeführt werden, während viele asynchrone Transaktionen gleichzeitig ausgeführt werden können. Bei synchronen Transaktionen kann ein langsamer Server dazu führen, dass ein Client im Leerlauf bleibt, während er auf eine Antwort wartet. Synchrone Transaktionen bewirken außerdem, dass der Client eine modale Schleife eingeht, die die Nachrichtenfilterung in der eigenen Nachrichtenschleife der Anwendung umgehen könnte.

Wenn der Client eine Hookprozedur zum Filtern von Nachrichten installiert hat (d. h. den WH MSGFILTER-Hooktyp in einem Aufruf der \_ [**SetWindowsHookEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa) angegeben hat), verursacht eine synchrone Transaktion nicht, dass das System die Hookprozedur umgeht. Wenn ein Eingabeereignis auftritt, während der Client auf das Ende einer synchronen Transaktion wartet, empfängt die Hookprozedur einen MSGF \_ DDEMGR-Hookcode. Die Hauptgefährdung der Verwendung einer modalen Synchrontransaktionsschleife ist, dass eine modale Schleife, die von einem Dialogfeld erstellt wird, den Vorgang beeinträchtigen kann. Asynchrone Transaktionen sollten immer verwendet werden, wenn die DDEML von einer DLL verwendet wird.

## <a name="transaction-control"></a>Transaktionssteuerung

Eine Anwendung kann Transaktionen für ihre DDE-Rückruffunktion entweder für transaktionen, die einem bestimmten Konversationshand handle zugeordnet sind, oder für alle Transaktionen unabhängig vom Konversationshand handle aussetzen. Diese Funktion ist nützlich, wenn eine Anwendung eine Transaktion empfängt, die eine langwierige Verarbeitung erfordert. In einem solchen Fall kann die Anwendung den CBR BLOCK-Rückgabecode zurückgeben, um zukünftige Transaktionen, die mit dem Konversationshand handle der Transaktion verknüpft sind, an die Hand zu geben, damit die Anwendung andere Konversationen \_ verarbeiten kann.

Nach Abschluss der Verarbeitung ruft die Anwendung die [**DdeEnableCallback-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) auf, um transaktionen, die der angehaltenen Konversation zugeordnet sind, wieder aufzunehmen. Der **Aufruf von DdeEnableCallback** bewirkt, dass die DDEML die Transaktion erneut senden muss, die dazu führte, dass die Anwendung die Konversation angehalten hat. Aus diesem Grund sollte die Anwendung das Ergebnis der Transaktion so speichern, dass sie das Ergebnis abrufen und zurückgeben kann, ohne die Transaktion erneut zu verarbeiten.

Eine Anwendung kann alle Transaktionen, die einem bestimmten Konversationshand handle zugeordnet sind, durch Angabe des Handles und des EC DISABLE-Flags in einem Aufruf von \_ [**DdeEnableCallback ansetzen.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) Durch Die Angabe eines **NULL-Handles** kann eine Anwendung alle Transaktionen für alle Konversationen ansetzen.

Wenn eine Konversation angehalten wurde, speichert die DDEML Transaktionen für die Konversation in einer Transaktionswarteschlange. Wenn die Anwendung die Konversation erneut eingibt, entfernt die DDEML die gespeicherten Transaktionen aus der Warteschlange und übergibt jede Transaktion an die entsprechende Rückruffunktion. Die Kapazität der Transaktionswarteschlange ist groß, aber eine Anwendung sollte eine angehaltene Konversation so schnell wie möglich erneut ermöglichen, um den Verlust von Transaktionen zu vermeiden.

Eine Anwendung kann die übliche Transaktionsverarbeitung fortsetzen, indem das EC \_ ENABLEALL-Flag in [**DdeEnableCallback angegeben wird.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) Für eine kontrolliertere Wiederaufnahme der Transaktionsverarbeitung kann die Anwendung das EC \_ ENABLEONE-Flag angeben. Dieses Flag entfernt eine Transaktion aus der Transaktionswarteschlange und übergibt sie an die entsprechende Rückruffunktion. Nachdem diese Transaktion verarbeitet wurde, werden alle Konversationen wieder deaktiviert.

Wenn das EC ENABLEONE-Flag und ein Konversationshand handle im Aufruf von \_ [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)angegeben werden, wird nur diese Konversation blockiert, nachdem die Transaktion verarbeitet wurde. Wenn ein **NULL-Konversationshand** handle angegeben wird, werden alle Konversationen blockiert, nachdem eine Transaktion in einer Konversation verarbeitet wurde.

## <a name="transaction-classes"></a>Transaktionsklassen

Die DDEML verfügt über vier Klassen von Transaktionen. Jede Klasse wird durch eine Konstante identifiziert, die mit dem XCLASS-Präfix \_ beginnt. Die Klassen werden in der DDEML-Headerdatei definiert. Der Klassenwert wird mit dem Transaktionstypwert kombiniert und an die DDE-Rückruffunktion der empfangenden Anwendung übergeben.

Die -Klasse einer Transaktion bestimmt den Rückgabewert, den eine Rückruffunktion zurückgeben soll, wenn sie die Transaktion verarbeitet. Die folgenden Rückgabewerte und Transaktionstypen sind jeder der vier Transaktionsklassen zugeordnet.



| Klasse                | Rückgabewert                                                     | Transaktion                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| XCLASS \_ BOOL         | **TRUE** oder **FALSE**                                            | [**XTYP \_ ADVSTART**](xtyp-advstart.md)<br/> [**XTYP \_ CONNECT**](xtyp-connect.md)<br/>                                                                                                                                                                                                                                                                                            |
| XCLASS \_ DATA         | Ein Datenhand handle, der CBR \_ BLOCK-Rückgabecode oder **NULL**           | [**XTYP \_ ADAKKAQ**](xtyp-advreq.md)<br/> [**\_XTYP-ANFORDERUNG**](xtyp-request.md)<br/> [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md)<br/>                                                                                                                                                                                                                                       |
| \_XCLASS-FLAGS        | Ein Transaktionsflag: DDE \_ FACK, DDE \_ FBUSY oder DDE \_ FNOTPROCESSED | [**XTYP \_ ADVDATA**](xtyp-advdata.md)<br/> [**XTYP \_ EXECUTE**](xtyp-execute.md)<br/> [**XTYP \_ POKE**](xtyp-poke.md)<br/>                                                                                                                                                                                                                                                   |
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



 

 

