---
title: Transaktions Verwaltung (Datenaustausch)
description: In diesem Thema wird erläutert, wie ein Client Transaktionen senden kann, um Daten und Dienste vom Server abzurufen.
ms.assetid: 2d08ffa3-cbd7-4806-b94f-979938322c38
keywords:
- Windows-Benutzeroberfläche, dynamischer Datenaustausch (DDE)
- Dynamischer Datenaustausch (DDE), Transaktionen
- DDE (dynamischer Datenaustausch), Transaktionen
- Datenaustausch, dynamischer Datenaustausch (DDE)
- Windows-Benutzeroberfläche, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
- Dynamischer Datenaustausch Management Library (Ddeml), Transaktionen
- Ddeml (dynamischer Datenaustausch-Verwaltungs Bibliothek), Transaktionen
- Datenaustausch, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
- Dynamischer Datenaustausch (DDE), Anforderungs Transaktionen
- DDE (dynamischer Datenaustausch), Anforderungs Transaktionen
- Dynamischer Datenaustausch Management Library (Ddeml), Anforderungs Transaktionen
- Ddeml (dynamischer Datenaustausch-Verwaltungs Bibliothek), Anforderungs Transaktionen
- Dynamischer Datenaustausch (DDE), Poke-Transaktionen
- DDE (dynamischer Datenaustausch), Poke-Transaktionen
- Dynamischer Datenaustausch Management Library (Ddeml), Poke-Transaktionen
- Ddeml (dynamischer Datenaustausch Verwaltungs Bibliothek), Poke-Transaktionen
- Dynamischer Datenaustausch (DDE), Anraten von Transaktionen
- DDE (dynamischer Datenaustausch), Anraten von Transaktionen
- Dynamischer Datenaustausch Management Library (Ddeml), Anraten von Transaktionen
- Ddeml (dynamischer Datenaustausch-Verwaltungs Bibliothek), Anraten von Transaktionen
- Dynamischer Datenaustausch (DDE), Transaktionen ausführen
- DDE (dynamischer Datenaustausch), Transaktionen ausführen
- Ddeml (dynamischer Datenaustausch Management Library), Transaktionen ausführen
- Ddeml (dynamischer Datenaustausch-Verwaltungs Bibliothek), Transaktionen ausführen
- Dynamischer Datenaustausch (DDE), synchrone Transaktionen
- DDE (dynamischer Datenaustausch), synchrone Transaktionen
- Ddeml (dynamischer Datenaustausch Management Library), synchrone Transaktionen
- Ddeml (dynamischer Datenaustausch-Verwaltungs Bibliothek), synchrone Transaktionen
- Dynamischer Datenaustausch (DDE), asynchrone Transaktionen
- DDE (dynamischer Datenaustausch), asynchrone Transaktionen
- Ddeml (dynamischer Datenaustausch Management Library), asynchrone Transaktionen
- Ddeml (dynamischer Datenaustausch Verwaltungs Bibliothek), asynchrone Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570aa48b4dcdbb31855b3e1b15a091908feb2ba4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039131"
---
# <a name="transaction-management-data-exchange"></a>Transaktions Verwaltung (Datenaustausch)

Nachdem eine Konversation mit einem Server eingerichtet wurde, kann ein Client Transaktionen senden, um Daten und Dienste vom Server abzurufen.

In den folgenden Themen werden die Transaktionstypen beschrieben, die von Clients für die Interaktion mit einem-Server verwendet werden können.

-   [Anforderungs Transaktion](#request-transaction)
-   [Poke-Transaktion](#poke-transaction)
-   [Empfehlung für Transaktion](#advise-transaction)
-   [Transaktion ausführen](#execute-transaction)
-   [Synchrone und asynchrone Transaktionen](#synchronous-and-asynchronous-transactions)
-   [Transaktions Steuerung](#transaction-control)
-   [Transaktions Klassen](#transaction-classes)
-   [Transaktionstypen](#transaction-types)

## <a name="request-transaction"></a>Anforderungs Transaktion

Eine Client Anwendung kann die [**XYP- \_ Anforderungs**](xtyp-request.md) Transaktion verwenden, um ein Datenelement von einer Serveranwendung anzufordern. Der Client ruft die [**ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) -Funktion auf, wobei **xD- \_ Anforderungen** als Transaktionstyp angegeben und das Datenelement angegeben wird, das die Anwendung benötigt.

Die dynamischer Datenaustausch Management Library (Ddeml) übergibt die [**XYP- \_ Anforderungs**](xtyp-request.md) Transaktion an den Server und gibt dabei den Themen Namen, den Elementnamen und das vom Client angeforderte Datenformat an. Wenn der Server das angeforderte Thema, Element und Format unterstützt, sollte der Server ein Daten Handle zurückgeben, das den aktuellen Wert des Elements identifiziert. Die Ddeml übergibt dieses Handle als Rückgabewert von [**ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)an den Client. Der Server sollte **null** zurückgeben, wenn er das angeforderte Thema, das Element oder das Format nicht unterstützt.

[**Ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) verwendet den *lpdwresult* -Parameter, um ein transaktionsstatusflag an den Client zurückzugeben. Wenn der Server die [**XYP- \_ Anforderungs**](xtyp-request.md) Transaktion nicht verarbeitet, **gibt ddeclienttransaction** **null** zurück, und *lpdwresult* verweist auf das \_ Flag DDE fnotverarbeitete oder DDE \_ fbusy. Wenn das DDE-Flag mit dem Wert "DDE" \_ zurückgegeben wird, kann der Client nicht ermitteln, warum der Server die Transaktion nicht verarbeitet hat.

Wenn ein Server die [**XYP- \_ Anforderungs**](xtyp-request.md) Transaktion nicht unterstützt, sollte er \_ \_ in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion das Filter Flag für die CBF-Fehler Anforderungen angeben. Dieses Flag verhindert, dass die Ddeml die Transaktion an den Server sendet.

## <a name="poke-transaction"></a>Poke-Transaktion

Ein Client kann mithilfe von [**ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) nicht angeforderte Daten an einen Server senden, um eine [**XYP- \_ Poke**](xtyp-poke.md) -Transaktion an die Rückruffunktion eines Servers zu senden.

Die Client Anwendung erstellt zunächst einen Puffer, der die Daten enthält, die an den Server gesendet werden sollen, und übergibt dann einen Zeiger als Parameter an [**ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)an den Puffer. Alternativ kann der Client die [**ddecreatedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) -Funktion verwenden, um ein Daten Handle abzurufen, das die Daten identifiziert und dann das Handle an **DDE clienttransaction** übergibt. In beiden Fällen gibt der Client auch den Themen Namen, den Elementnamen und das Datenformat an, wenn er **ddeclienttransaction** aufruft.

Die Ddeml übergibt die [**XYP- \_ Poke**](xtyp-poke.md) -Transaktion an den Server und gibt den Themen Namen, den Elementnamen und das Datenformat an, die der Client angefordert hat. Um das Datenelement und das Format zu akzeptieren, sollte der Server DDE \_ fakk zurückgeben. Um die Daten abzulehnen, sollte der Server DDE \_ fnotverarbeitete zurückgeben. Wenn der Server zu stark ausgelastet ist, um die Daten zu akzeptieren, sollte der Server DDE \_ fbusy zurückgeben.

Wenn [**ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) zurückgegeben wird, kann der Client den *lpdwresult* -Parameter verwenden, um auf das Flag für den Transaktionsstatus zuzugreifen. Wenn das Flag DDE-vollständig \_ ausgelastet ist, sollte der Client die Transaktion später erneut senden.

Wenn ein Server die [**XYP- \_ Poke**](xtyp-poke.md) -Transaktion nicht unterstützt, sollte er das Flag "CBF \_ Fail \_ Pokes Filter" in " [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)" angeben. Dieses Flag verhindert, dass die Ddeml diese Transaktion an den Server sendet.

## <a name="advise-transaction"></a>Empfehlung für Transaktion

Eine Client Anwendung kann die Ddeml verwenden, um einen oder mehrere Verknüpfungen zu Elementen in einer Serveranwendung herzustellen. Wenn ein solcher Link festgelegt wurde, sendet der Server periodische Updates über das verknüpfte Element an den Client (in der Regel, wenn sich der Wert des Elements ändert, das mit der Serveranwendung verknüpft ist). Bei der Verknüpfung wird eine Empfehlung-Schleife zwischen den beiden Anwendungen erstellt, die weiterhin vorhanden sind, bis Sie vom Client beendet wird.

Es gibt zwei Arten von Empfehlung-Schleifen: "Hot" und "warm". In einer Hot-Empfehlung-Schleife sendet der Server sofort ein Daten handle, das den geänderten Wert identifiziert. In einer warmen Empfehlung-Schleife benachrichtigt der Server den Client, dass sich der Wert des Elements geändert hat, sendet das Daten handle jedoch erst, wenn es vom Client angefordert wird.

Ein Client kann eine Hot-Empfehlung-Schleife mit einem Server anfordern, indem er in einem [**ddeclienttransaction-dddeclienttransaction-ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)-Vorgang den [**xType \_**](xtyp-advstart.md) - Um eine warm-Empfehlung-Schleife anzufordern, muss der Client das xtypf \_ NODATA-Flag mit dem **xType- \_ advstart** -Transaktionstyp kombinieren. In beiden Ereignissen übergibt die Ddeml die **XYP- \_ advstart** -Transaktion an die dynamischer Datenaustausch (DDE)-Rückruffunktion des Servers. Die DDE-Rückruffunktion des Servers sollte die Parameter untersuchen, die die **XTT-advstart \_** -Transaktion (einschließlich des angeforderten Formats, Themen namens und Element namens) begleiten, und dann **true** zurückgeben, um die Empfehlung-Schleife zuzulassen, oder **false** , um sie abzulehnen.

Nachdem eine Empfehlung-Schleife eingerichtet wurde, sollte die Serveranwendung die [**DDE postadvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) -Funktion immer dann aufzurufen, wenn sich der Wert des Elements ändert, das dem angeforderten Elementnamen zugeordnet ist. Dieser Befehl führt dazu, dass eine [**xD- \_ advreq**](xtyp-advreq.md) -Transaktion an die eigene DDE-Rückruffunktion des Servers gesendet wird. Die DDE-Rückruffunktion des Servers sollte ein Daten Handle zurückgeben, das den neuen Wert des Datenelements identifiziert. Die Ddeml benachrichtigt den Client dann, dass das angegebene Element geändert wurde, indem er die [**XYP- \_ advdata**](xtyp-advdata.md) -Transaktion an die DDE-Rückruffunktion des Clients sendet.

Wenn der Client eine Hot-Empfehlung-Schleife angefordert hat, übergibt die Ddeml das Daten Handle während der [**xD- \_ advdata**](xtyp-advdata.md) -Transaktion an das geänderte Element an den Client. Andernfalls kann der Client eine [**XYP- \_ Anforderungs**](xtyp-request.md) Transaktion zum Abrufen des Daten Handles senden.

Es ist möglich, dass ein Server Updates schneller sendet, als ein Client die neuen Daten verarbeiten kann. Die Geschwindigkeit der Updates kann ein Problem für einen Client sein, der lange Verarbeitungsvorgänge für die Daten ausführen muss. In diesem Fall sollte der Client das xtypf- \_ ackreq-Flag angeben, wenn es eine Empfehlung-Schleife anfordert. Dieses Flag bewirkt, dass der Server auf den Client wartet, um zu bestätigen, dass er ein Datenelement empfangen und verarbeitet hat, bevor der Server das nächste Datenelement sendet. Mit dem xtypf-ackreq-Flag festgelegte Ratschläge-Schleifen \_ sind bei schnellen Servern robuster, können jedoch gelegentlich aktualisiert werden. Ohne das xtypf- \_ ackreq-Flag erstellende Empfehlung-Schleifen werden sichergestellt, dass Updates nicht übersehen werden, solange der Client den Server weiterhin verwendet.

Ein Client kann eine Empfehlung-Schleife beenden, indem [**\_**](xtyp-advstop.md) er in einem [**ddeclienttransaction-dddeclienttransaction-ddeclienttransaction-ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)-

Wenn ein Server keine Empfehlung-Schleifen unterstützt, sollte er \_ \_ in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion das Flag "CBF-Fehler-Filter" angeben. Mit diesem Flag wird verhindert, dass die Ddeml die [**XYP- \_ advstart**](xtyp-advstart.md) -und [**xD \_ advstopptransaktionen**](xtyp-advstop.md) an den Server sendet.

## <a name="execute-transaction"></a>Transaktion ausführen

Ein Client kann die [**xtyp- \_ Ausführungs**](xtyp-execute.md) Transaktion verwenden, um einen-Server zum Ausführen eines Befehls oder einer Reihe von Befehlen zu veranlassen.

Um einen Server Befehl auszuführen, erstellt der Client zunächst einen Puffer, der eine Befehls Zeichenfolge für den Server enthält, und übergibt dann entweder einen Zeiger an den Puffer oder ein Daten handle, das den Puffer identifiziert, wenn [**ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)aufgerufen wird. Weitere erforderliche Parameter sind u. a. das Konversations handle, der Zeichen folgen Handle des Element namens, die Format Spezifikation und der [**xType \_ Execute**](xtyp-execute.md) Transaction-Typ. Eine Anwendung, die ein Daten Handle zum Übergeben von Execute Data erstellt, muss für den Parameter " *hszitem* " der [**ddecreatedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) -Funktion **null** und für den *ufmt* -Parameter NULL angeben.

Die Ddeml übergibt die [**Xder- \_ Execute**](xtyp-execute.md) -Transaktion an die DDE-Rückruffunktion des Servers und gibt den Format Namen, das Konversations handle, den Themen Namen und das Daten Handle an, das die Befehls Zeichenfolge identifiziert. Wenn der Server den-Befehl unterstützt, sollte die [**DDEBUG Data**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) -Funktion verwendet werden, um einen Zeiger auf die Befehls Zeichenfolge zu erhalten, den Befehl auszuführen und dann DDE- \_ fakk zurückzugeben. Wenn der Server den Befehl nicht unterstützt oder die Transaktion nicht abgeschlossen werden kann, sollte DDE "f" zurückgegeben werden \_ . Der Server sollte DDE \_ fbusy zurückgeben, wenn er zu stark ausgelastet ist, um die Transaktion abzuschließen.

Im Allgemeinen sollte die Rückruffunktion eines Servers die [**XYP- \_ Execute**](xtyp-execute.md) -Transaktion verarbeiten, bevor Sie mit den folgenden Ausnahmen zurückgegeben wird:

1.  Wenn der-Befehl, der mit der [**xtipp- \_ Ausführungs Transaktion ausgeführt**](xtyp-execute.md) wird, den Server beendet, sollte der Server erst beendet werden, wenn die Rückruffunktion von der Verarbeitung von **\_ xtypexecute** zurückgegeben wird.
2.  Wenn der Server einen Vorgang ausführen muss, z. b. ein Dialogfeld oder eine DDE-Transaktion, die möglicherweise Probleme mit der Ddeml-Rekursion verursacht, sollte der Server den Rückgabecode des CBR-Blocks zurückgeben, \_ um die Ausführungs Transaktion zu blockieren, den Vorgang auszuführen und die Verarbeitung der Ausführungs Transaktion fortzusetzen.

Wenn [**ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) zurückgegeben wird, kann der Client den *lpdwresult* -Parameter verwenden, um auf das transaktionsstatusflag zuzugreifen. Wenn das Flag DDE-vollständig \_ ausgelastet ist, sollte der Client die Transaktion später erneut senden.

Wenn ein Server die [**xtyp- \_ Execute**](xtyp-execute.md) -Transaktion nicht unterstützt, sollte er das Flag CBF \_ Fail Execute \_ Filter in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angeben. Dadurch wird verhindert, dass die Ddeml die Transaktion an den Server sendet.

## <a name="synchronous-and-asynchronous-transactions"></a>Synchrone und asynchrone Transaktionen

Ein Client kann entweder synchrone oder asynchrone Transaktionen senden. In einer synchronen Transaktion gibt der Client einen Timeout Wert an, der angibt, wie lange es dauert, bis der Server die Transaktion verarbeitet. [**Ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) wird erst zurückgegeben, wenn der Server die Transaktion verarbeitet, die Transaktion fehlschlägt oder der Timeout Wert abläuft. Der Client gibt den Timeout Wert an, wenn er **ddeclienttransaction** aufruft.

Während einer synchronen Transaktion wechselt der Client in eine modale Schleife, während er darauf wartet, dass die Transaktion verarbeitet wird. Der Client kann weiterhin Benutzereingaben verarbeiten, aber keine weitere synchrone Transaktion senden, bis [**ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) zurückgibt.

Ein Client sendet eine asynchrone Transaktion, indem er \_ in [**ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)das Timeout-Async-Flag angibt. Die Funktion gibt zurück, nachdem die Transaktion begonnen hat, und übergibt einen Transaktions Bezeichner an den Client. Wenn der Server die Verarbeitung der asynchronen Transaktion abgeschlossen hat, sendet die Ddeml eine [**xttl- \_ \_ vollständige**](xtyp-xact-complete.md) Transaktion an den Client. Einer der Parameter, den die Ddeml während der **\_ \_ vollständigen xD** -Transaktion an den Client übergibt, ist der Transaktions Bezeichner. Durch vergleichen dieses Transaktions Bezeichners mit dem Bezeichner, der von **ddeclienttransaction** zurückgegeben wurde, ermittelt der Client, welche asynchrone Transaktion der Server verarbeitet hat.

Ein Client kann die [**ddesetuserhandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddesetuserhandle) -Funktion als Hilfe bei der Verarbeitung einer asynchronen Transaktion verwenden. Diese Funktion ermöglicht es einem Client, einen Anwendungs definierten Wert einem Konversations Handle und einem Transaktions Bezeichner zuzuordnen. Der Client kann die [**DDE queryperformanfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) -Funktion während der abgeschlossenen [**xD \_ - \_**](xtyp-xact-complete.md) Transaktion verwenden, um den von der Anwendung definierten Wert zu erhalten. Aufgrund dieser Funktion muss eine Anwendung keine Liste aktiver Transaktions Bezeichner verwalten.

Wenn ein Client eine Anforderung für Daten mit einer synchronen Transaktion erfolgreich abgeschlossen hat, kann die Ddeml nicht ermitteln, wann der Client die Verwendung der empfangenen Daten abgeschlossen hat. Die Client Anwendung muss das an die [**ddefredatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) -Funktion empfangene Daten Handle übergeben und die Ddeml Benachrichtigen, dass das Handle nicht mehr verwendet wird. Daten Handles, die von synchronen Transaktionen zurückgegeben werden, sind im Besitz des Clients.

Wenn eine asynchrone Transaktion von einem Server nicht rechtzeitig verarbeitet wird, kann der Client die Transaktion durch Aufrufen der [**ddeabandontransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeabandontransaction) -Funktion verwerfen. Die Ddeml gibt alle der Transaktion zugeordneten Ressourcen frei und verwirft die Ergebnisse der Transaktion, wenn der Server die Verarbeitung abschließt. Ein Timeout während einer synchronen Transaktion bricht die Transaktion effektiv ab.

Die asynchrone Transaktions Methode wird für Anwendungen bereitgestellt, die ein hohes Maß an DDE-Transaktionen senden müssen, während gleichzeitig eine beträchtliche Menge an Verarbeitung ausgeführt wird, z. b. das Durchführen von Berechnungen. Die asynchrone-Methode ist auch bei Anwendungen nützlich, die die Verarbeitung von DDE-Transaktionen vorübergehend beenden müssen, damit andere Aufgaben ohne Unterbrechung durchgeführt werden können. In den meisten anderen Situationen sollte eine Anwendung die synchrone-Methode verwenden.

Synchrone Transaktionen können einfacher gewartet werden und sind schneller als asynchrone Transaktionen. Es kann jedoch immer nur eine synchrone Transaktion gleichzeitig ausgeführt werden, während viele asynchrone Transaktionen gleichzeitig ausgeführt werden können. Bei synchronen Transaktionen kann ein langsamer Server bewirken, dass ein Client im Leerlauf bleibt, während er auf eine Antwort wartet. Außerdem bewirken synchrone Transaktionen, dass der Client eine modale Schleife eingibt, die das Filtern von Nachrichten in der eigenen Nachrichten Schleife der Anwendung umgehen könnte.

Wenn auf dem Client eine Hook-Prozedur zum Filtern von Nachrichten installiert ist (d. h., der "WH \_ msgfilter"-Hooktyp wird in einem Aufrufen der Funktion " [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa) " angegeben), bewirkt eine synchrone Transaktion nicht, dass die Hook-Prozedur umgangen wird. Wenn ein Eingabe Ereignis auftritt, während der Client auf das Ende einer synchronen Transaktion wartet, empfängt die Hook-Prozedur einen MSGF \_ ddemgr-Hook-Code. Die Hauptgefahr der Verwendung einer synchronen Transaktions Schleife besteht darin, dass eine modale Schleife, die von einem Dialogfeld erstellt wurde, den Vorgang beeinträchtigen kann. Asynchrone Transaktionen sollten immer verwendet werden, wenn die Ddeml von einer DLL verwendet wird.

## <a name="transaction-control"></a>Transaktions Steuerung

Eine Anwendung kann Transaktionen an Ihre DDE-Rückruffunktion aussetzen, entweder die Transaktionen, die einem bestimmten Konversations Handle zugeordnet sind, oder alle Transaktionen unabhängig vom Konversations handle. Diese Funktion ist nützlich, wenn eine Anwendung eine Transaktion empfängt, die eine lange Verarbeitung erfordert. In einem solchen Fall kann die Anwendung den Rückgabecode des CBR-Blocks zurückgeben, \_ um zukünftige Transaktionen anzuhalten, die dem Konversations Handle der Transaktion zugeordnet sind, damit die Anwendung andere Konversationen verarbeiten kann.

Wenn die Verarbeitung abgeschlossen ist, ruft die Anwendung die [**ddeenablecallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) -Funktion auf, um die mit der angehalten Konversation verknüpften Transaktionen wieder aufzunehmen. Das Aufrufen von **ddeenablecallback** bewirkt, dass die Ddeml die Transaktion erneut sendet, die dazu geführt hat, dass die Anwendung die Konversation ausgesetzt hat. Daher sollte die Anwendung das Ergebnis der Transaktion so speichern, dass Sie das Ergebnis abrufen und zurückgeben kann, ohne die Transaktion erneut zu verarbeiten.

Eine Anwendung kann alle Transaktionen aussetzen, die einem bestimmten Konversations Handle zugeordnet sind, indem das Handle und das Flag zum Deaktivieren von EC \_ in einem [**ddeenablecallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)-Befehl angegeben werden. Durch die Angabe eines **null** -Handles kann eine Anwendung alle Transaktionen für alle Konversationen aussetzen.

Wenn eine Konversation angehalten wurde, speichert die Ddeml Transaktionen für die Konversation in einer Transaktions Warteschlange. Wenn die Anwendung die Konversation erneut aktiviert, entfernt die Ddeml die gespeicherten Transaktionen aus der Warteschlange und übergibt jede Transaktion an die entsprechende Rückruffunktion. Die Kapazität der Transaktions Warteschlange ist groß, aber eine Anwendung sollte eine angehaltene Konversation so bald wie möglich wieder aktivieren, um den Verlust von Transaktionen zu vermeiden.

Eine Anwendung kann die übliche Transaktionsverarbeitung fortsetzen, indem das EC \_ enableall-Flag in [**ddeenablecallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)angegeben wird. Um die Wiederaufnahme der Transaktionsverarbeitung zu steuern, kann die Anwendung das Flag "EC \_ enableone" angeben. Dieses Flag entfernt eine Transaktion aus der Transaktions Warteschlange und übergibt sie an die entsprechende Rückruffunktion. Nachdem diese Transaktion verarbeitet wurde, werden alle Konversationen wieder deaktiviert.

Wenn das EC \_ -enableone-Flag und ein Konversations Handle im [**DDE enablecallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)-Befehl angegeben werden, wird nur diese Konversation blockiert, nachdem die Transaktion verarbeitet wurde. Wenn ein **null** -Konversations handle angegeben wird, werden alle Konversationen nach der Verarbeitung einer Transaktion in einer Konversation blockiert.

## <a name="transaction-classes"></a>Transaktions Klassen

Die Ddeml enthält vier Klassen von Transaktionen. Jede Klasse wird durch eine Konstante identifiziert, die mit dem xclass- \_ Präfix beginnt. Die Klassen werden in der Ddeml-Header Datei definiert. Der Klassen Wert wird mit dem Wert des Transaktions Typs kombiniert und an die DDE-Rückruffunktion der empfangenden Anwendung übermittelt.

Die Klasse einer Transaktion bestimmt den Rückgabewert, der von einer Rückruffunktion zurückgegeben wird, wenn Sie die Transaktion verarbeitet. Die folgenden Rückgabewerte und Transaktionstypen sind den einzelnen vier Transaktions Klassen zugeordnet.



| Klasse                | Rückgabewert                                                     | Transaktion                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| xclass \_ bool         | **True** oder **false**                                            | [**xttyp \_ advstart**](xtyp-advstart.md)<br/> [**xtipp- \_ Verbindung**](xtyp-connect.md)<br/>                                                                                                                                                                                                                                                                                            |
| xclass- \_ Daten         | Ein Daten handle, der CBR- \_ Block Rückgabecode oder **null** .           | [**xttyp \_ advreq**](xtyp-advreq.md)<br/> [**XYP- \_ Anforderung**](xtyp-request.md)<br/> [**\_xttwildconnect**](xtyp-wildconnect.md)<br/>                                                                                                                                                                                                                                       |
| xclass- \_ Flags        | Ein transaktionsflag: DDE \_ fakk, DDE \_ sausgelastet oder DDE-vollständig \_ verarbeitet | [**xttyp \_ advdata**](xtyp-advdata.md)<br/> [**xtyp \_ Ausführen**](xtyp-execute.md)<br/> [**XYP \_ Poke**](xtyp-poke.md)<br/>                                                                                                                                                                                                                                                   |
| xclass- \_ Benachrichtigung | Keine                                                             | [**xttyp \_ advstopps**](xtyp-advstop.md)<br/> [**xtipp \_ Connect- \_ Bestätigung**](xtyp-connect-confirm.md)<br/> [**xtipp- \_ Trennung**](xtyp-disconnect.md)<br/> [**XYP- \_ Fehler**](xtyp-error.md)<br/> [**XYP- \_ Register**](xtyp-register.md)<br/> [**Unregister von xttyp \_**](xtyp-unregister.md)<br/> [**\_xttxact-Vorgang ist \_ beendet**](xtyp-xact-complete.md)<br/> |



 

## <a name="transaction-types"></a>Transaktionstypen

Jeder DDE-Transaktionstyp verfügt über einen Empfänger und eine zugeordnete Aktivität, die bewirkt, dass die Ddeml jeden Typ generiert.



| Transaktionstyp                                       | Receiver                   | Ursache                                                                                                                                                                         |
|--------------------------------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**xttyp \_ advdata**](xtyp-advdata.md)                  | Client                     | Ein Server hat auf eine [**xD- \_ advreq**](xtyp-advreq.md) -Transaktion reagiert, indem ein Daten Handle zurückgegeben wurde.                                                                          |
| [**xttyp \_ advreq**](xtyp-advreq.md)                    | Server                     | Ein Server, der die [**DDE postadvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) -Funktion aufgerufen hat und angibt, dass sich der Wert eines Datenelements in einer-Benachrichtigungs Schleife geändert hat.                                  |
| [**xttyp \_ advstart**](xtyp-advstart.md)                | Server                     | Ein Client hat den [**xType \_ advstart**](xtyp-advstart.md) Transaction Type in einem aufzurufenden Befehl der [**ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) -Funktion angegeben.               |
| [**xttyp \_ advstopps**](xtyp-advstop.md)                  | Server                     | In einem [**\_**](xtyp-advstop.md) [**ddeclienttransaction-ddeclienttransaction-ddeclienttransaction-ddeclienttransaction-ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)-                              |
| [**xtipp- \_ Verbindung**](xtyp-connect.md)                  | Server                     | Ein Client hat die [**ddeconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) -Funktion aufgerufen und einen Dienstnamen und einen Themen Namen angegeben, der vom Server unterstützt wird.                                            |
| [**xtipp \_ Connect- \_ Bestätigung**](xtyp-connect-confirm.md) | Server                     | Der Server hat als Antwort auf eine [**xtipp \_ Connect**](xtyp-connect.md) -oder [**XYP \_ wildconnect**](xtyp-wildconnect.md) -Transaktion **true** zurückgegeben.                            |
| [**xtipp- \_ Trennung**](xtyp-disconnect.md)            | Client/Server              | Ein Partner in einer Konversation hat die [**DDE Disconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) -Funktion aufgerufen und bewirkt, dass beide Partner diese Transaktion empfangen.                                    |
| [**XYP- \_ Fehler**](xtyp-error.md)                      | Client/Server              | Ein kritischer Fehler ist aufgetreten. Die Ddeml verfügt möglicherweise nicht über genügend Ressourcen, um den Vorgang fortzusetzen.                                                                                       |
| [**xtyp \_ Ausführen**](xtyp-execute.md)                  | Server                     | Ein Client hat den [**xType \_ Execute**](xtyp-execute.md) Transaction-Typ in einem [**ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)-Befehl angegeben.                              |
| [**XYP- \_ Monitor**](xtyp-monitor.md)                  | DDE-Überwachungsanwendung | Ein DDE-Ereignis ist im System aufgetreten. Weitere Informationen zu DDE-Überwachungsanwendungen finden Sie unter über [Wachen von Anwendungen](monitoring-applications.md).                       |
| [**XYP \_ Poke**](xtyp-poke.md)                        | Server                     | Ein Client hat den [**xType \_ Poke**](xtyp-poke.md) -Transaktionstyp in einem [**ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)-Aufgabentyp angegeben.                                    |
| [**XYP- \_ Register**](xtyp-register.md)                | Client/Server              | Eine Serveranwendung hat die Funktion " [**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) " verwendet, um einen Dienstnamen zu registrieren.                                                                   |
| [**XYP- \_ Anforderung**](xtyp-request.md)                  | Server                     | Ein Client hat in einem [**ddeclienttransaction-ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)-Befehl den Transaktionstyp [**XYP \_ angefordert**](xtyp-request.md)                              |
| [**Unregister von xttyp \_**](xtyp-unregister.md)            | Client/Server              | Eine Serveranwendung hat [**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) zum Aufheben der Registrierung eines Dienst namens verwendet.                                                                              |
| [**\_xttwildconnect**](xtyp-wildconnect.md)          | Server                     | Ein Client hat die [**ddeconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) -oder [**ddeconnectlist**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) -Funktion aufgerufen und gibt **null** für den Dienstnamen, den Themen Namen oder beides an. |
| [**\_xttxact-Vorgang ist \_ beendet**](xtyp-xact-complete.md)     | Client                     | Eine asynchrone Transaktion, die gesendet wird, wenn der Client das Timeout- \_ Async-Flag in einem [**ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)-Befehl angegeben hat, wurde beendet.         |



 

 

