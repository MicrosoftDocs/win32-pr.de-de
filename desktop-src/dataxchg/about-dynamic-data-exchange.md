---
title: Informationen zu dynamischer Datenaustausch
description: In diesem Thema wird die Datenübertragung zwischen Anwendungen erläutert.
ms.assetid: 0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb
keywords:
- Dynamischer Datenaustausch (DDE), Informationen zu
- DDE (dynamischer Datenaustausch), Informationen zu
- Datenaustausch, dynamischer Datenaustausch (DDE)
- Dynamischer Datenaustausch (DDE), Verknüpfen mit Echtzeitdaten
- DDE (dynamischer Datenaustausch), Verknüpfen mit Echtzeitdaten
- Dynamischer Datenaustausch (DDE), Erstellen von Verbund Dokumenten
- DDE (dynamischer Datenaustausch), Erstellen von Verbund Dokumenten
- Dynamischer Datenaustausch (DDE), Daten Abfragen
- DDE (dynamischer Datenaustausch), Daten Abfragen
- Dynamischer Datenaustausch (DDE), Beispiele
- DDE (dynamischer Datenaustausch), Beispiele
- Dynamischer Datenaustausch (DDE), Identitätswechsel
- DDE (dynamischer Datenaustausch), Identitätswechsel
- Dynamischer Datenaustausch (DDE), Nachrichten
- DDE (dynamischer Datenaustausch), Nachrichten
- Dynamischer Datenaustausch (DDE), Atome
- DDE (dynamischer Datenaustausch), Atome
- Dynamischer Datenaustausch (DDE), Shared Memory-Objekte
- DDE (dynamischer Datenaustausch), Shared Memory-Objekte
- Dynamischer Datenaustausch (DDE), Parameter Verpackungs Funktionen
- DDE (dynamischer Datenaustausch), Parameter Verpackungs Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d38574e9182255e8f6761520aea60575d8affbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390816"
---
# <a name="about-dynamic-data-exchange"></a>Informationen zu dynamischer Datenaustausch

Windows stellt verschiedene Methoden zum Übertragen von Daten zwischen Anwendungen bereit. Eine Methode ist die Verwendung des dynamischer Datenaustausch (DDE)-Protokolls. Das DDE-Protokoll besteht aus einer Reihe von Nachrichten und Richtlinien. Es sendet Nachrichten zwischen Anwendungen, die Daten gemeinsam nutzen, und nutzt gemeinsam genutzten Speicher, um Daten zwischen Anwendungen auszutauschen. Anwendungen können das DDE-Protokoll für einmalige Datenübertragungen und für den kontinuierlichen Austausch verwenden, bei dem Anwendungen Updates an einander senden, wenn neue Daten verfügbar sind.

Windows unterstützt auch die Ddeml (dynamischer Datenaustausch Management Library). Die Ddeml ist eine Dynamic Link Library (dll), mit der Anwendungen Daten freigeben können. Die Ddeml stellt Funktionen und Nachrichten bereit, die das Hinzufügen von DDE-Funktionen zu einer Anwendung vereinfachen. Anstatt DDE-Nachrichten direkt zu senden, zu veröffentlichen und zu verarbeiten, verwendet eine Anwendung die Ddeml-Funktionen, um DDE-Konversationen zu verwalten. (Eine DDE-Konversation ist die Interaktion zwischen Client-und Server Anwendungen.)

Die Ddeml bietet auch eine Möglichkeit zum Verwalten der Zeichen folgen und Daten, die von DDE-Anwendungen gemeinsam genutzt werden. Anstatt Atome und Zeiger auf freigegebene Speicher Objekte zu verwenden, erstellen und verarbeiten DDE-Anwendungen Zeichen folgen Handles, die Zeichen folgen und Daten Handles identifizieren, die Speicher Objekte identifizieren. Die Ddeml ermöglicht es einer Serveranwendung auch, die von ihr unterstützten Dienstnamen zu registrieren. Die Namen werden an andere Anwendungen im System übertragen, die die Namen zum Herstellen einer Verbindung mit dem Server verwenden können. Außerdem gewährleistet die Ddeml die Kompatibilität zwischen DDE-Anwendungen, indem Sie gezwungen wird, das DDE-Protokoll auf konsistente Weise zu implementieren.

Vorhandene Anwendungen, die das Nachrichten basierte DDE-Protokoll verwenden, sind vollständig kompatibel mit denjenigen, die die Ddeml verwenden. Das heißt, eine Anwendung, die Nachrichten basiertes DDE verwendet, kann Konversationen einrichten und Transaktionen mit Anwendungen ausführen, die die Ddeml verwenden. Aufgrund der vielen Vorteile der Ddeml sollten neue Anwendungen Sie anstelle der DDE-Nachrichten verwenden. Um die API-Elemente der Ddeml zu verwenden, müssen Sie die Ddeml-Header Datei in die Quelldateien einschließen, eine Verknüpfung mit der Ddeml-Bibliothek herstellen und sicherstellen, dass sich die Ddeml-Bibliothek für dynamische Links im Suchpfad des Systems befindet.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [dynamischer Datenaustausch-Protokoll](#dynamic-data-exchange-protocol)
-   [Verwendung für Windows-dynamischer Datenaustausch](#uses-for-windows-dynamic-data-exchange)
-   [Aus Sicht des Benutzers dynamischer Datenaustausch](#dynamic-data-exchange-from-the-users-point-of-view)
-   [dynamischer Datenaustausch Konzepte](#dynamic-data-exchange-concepts)
    -   [Client, Server und Konversation](#client-server-and-conversation)
    -   [Anwendungs-, Themen-und Elementnamen](#application-topic-and-item-names)
    -   [Das System Thema](#the-system-topic)
    -   [Permanente Daten Verknüpfungen](#permanent-data-links)
    -   [Atome und Shared Memory-Objekte](#atoms-and-shared-memory-objects)
-   [Übersicht über dynamischer Datenaustausch Meldungen](#dynamic-data-exchange-messages-overview)
-   [dynamischer Datenaustausch Nachrichtenfluss](#dynamic-data-exchange-message-flow)
-   [Parameter Verpackungs Funktionen](#parameter-packing-functions)
-   [dynamischer Datenaustausch und Identitätswechsel](#dynamic-data-exchange-and-impersonation)

## <a name="dynamic-data-exchange-protocol"></a>dynamischer Datenaustausch-Protokoll

Da Windows über eine Nachrichten basierte Architektur verfügt, ist das Übergeben von Nachrichten die geeignetste Methode für die automatische Übertragung von Informationen zwischen Anwendungen. Nachrichten enthalten jedoch nur zwei Parameter (*wParam* und *LPARAM*), um Daten zu übergeben. Daher müssen diese Parameter indirekt auf andere Datenelemente verweisen, wenn mehr als ein paar Wörter von Informationen zwischen Anwendungen übergeben werden. Das DDE-Protokoll definiert genau, wie Anwendungen den *wParam* -Parameter und den *LPARAM* -Parameter verwenden sollten, um größere Datenmengen mithilfe globaler Atome und Shared Memory-Handles zu übergeben. Das DDE-Protokoll verfügt über bestimmte Regeln zum Zuordnen und Löschen von globalen Atomen und Shared Memory-Objekten.

Ein globales Atom ist ein Verweis auf eine Zeichenfolge. Im DDE-Protokoll erkennen Atome die Anwendungen, die Daten austauschen, die Art der Daten, die ausgetauscht werden, und die Datenelemente selbst. Weitere Informationen zu Atomen finden Sie unter Informationen [zu Atomen](about-atom-tables.md).

## <a name="uses-for-windows-dynamic-data-exchange"></a>Verwendung für Windows-dynamischer Datenaustausch

DDE eignet sich am besten für Datenaustausch Vorgänge, für die keine fortlaufende Benutzerinteraktion erforderlich ist. In der Regel stellt eine Anwendung eine Methode bereit, mit der der Benutzer den Link zwischen den Anwendungen, die Daten austauschen, einrichten kann. Sobald dieser Link eingerichtet ist, tauschen die Anwendungen Daten ohne weitere Benutzer Beteiligung aus.

DDE kann verwendet werden, um eine breite Palette von Anwendungs Features zu implementieren – beispielsweise:

-   Verknüpfen mit Echtzeitdaten, wie z. b. mit Aktienmarkt Updates, wissenschaftlichen Instrumenten oder Prozesskontrolle.
-   Erstellen von Verbund Dokumenten, z. b. einem Textverarbeitungsdokument, das ein Diagramm enthält, das von einer Grafikanwendung erzeugt wird. Mithilfe von DDE ändert sich das Diagramm, wenn die Quelldaten geändert werden, während der Rest des Dokuments unverändert bleibt.
-   Ausführen von Daten Abfragen zwischen Anwendungen, z. b. einem Arbeitsblatt, mit dem eine Datenbank nach überfälligen Konten abgefragt wird.

## <a name="dynamic-data-exchange-from-the-users-point-of-view"></a>Aus Sicht des Benutzers dynamischer Datenaustausch

Im folgenden Beispiel wird veranschaulicht, wie zwei DDE-Anwendungen zusammenarbeiten können, wie Sie aus der Sicht des Benutzers ersichtlich sind.

Eine Tabellen Kalkulations Tabelle möchte Microsoft Excel verwenden, um den Preis für eine bestimmte Aktie auf dem Börsenkurs in New York zu verfolgen. Der Benutzer hat eine Anwendung mit dem Namen "Quote", die wiederum Zugriff auf die Daten von NYSE hat. Die DDE-Konversation zwischen Excel und Anführungszeichen erfolgt wie folgt:

-   Der Benutzer initiiert die Konversation durch Angabe des Namens der Anwendung (Anführungszeichen), die die Daten und das jeweilige relevante Thema (NYSE) bereitstellt. Die resultierende DDE-Konversation wird verwendet, um Anführungszeichen für bestimmte Bestände anzufordern.
-   Excel überträgt die Anwendungs-und Themen Namen an alle DDE-Anwendungen, die zurzeit im System ausgeführt werden. Das Zitat gibt eine Konversation mit Excel über das Thema "NYSE" aus.
-   Der Benutzer kann dann eine Tabellen Kalkulations Tabelle in einer Zelle erstellen, die anfordert, dass die Tabelle automatisch aktualisiert wird, wenn sich ein bestimmtes Aktienangebot ändert. Beispielsweise kann der Benutzer immer dann eine automatische Aktualisierung anfordern, wenn eine Änderung im Verkauf von zaxx-Aktien durch Angabe der folgenden Excel-Formel erfolgt: = ' Quote ' \| ' NYSE '! Zaxx
-   Der Benutzer kann das automatische Aktualisieren des zaxx-Aktien Angebots jederzeit beenden. Andere Daten Verknüpfungen, die separat eingerichtet wurden (z. b. für Anführungszeichen für andere Aktien), bleiben in derselben NYSE-Konversation aktiv.
-   Der Benutzer kann auch die gesamte Konversation zwischen Excel und dem Angebot im Thema "NYSE" beenden, sodass keine bestimmten Daten Verknüpfungen in diesem Thema erstellt werden können, ohne dass eine neue Konversation initiiert wird.

## <a name="dynamic-data-exchange-concepts"></a>dynamischer Datenaustausch Konzepte

In den folgenden Abschnitten werden wichtige Konzepte und Begriffe erläutert, die für das Verständnis des dynamischen Datenaustauschs wichtig sind.

-   [Client, Server und Konversation](#client-server-and-conversation)
-   [Anwendungs-, Themen-und Elementnamen](#application-topic-and-item-names)
-   [Das System Thema](#the-system-topic)
-   [Permanente Daten Verknüpfungen](#permanent-data-links)
-   [Atome und Shared Memory-Objekte](#atoms-and-shared-memory-objects)

### <a name="client-server-and-conversation"></a>Client, Server und Konversation

Zwei an DDE beteiligte Anwendungen werden als Teil einer DDE-Konversation bezeichnet. Die Anwendung, die die Konversation initiiert, ist die DDE-Client Anwendung. die Anwendung, die auf den Client antwortet, ist die DDE-Serveranwendung. Eine Anwendung kann mehrere Konversationen gleichzeitig einbinden und als Client in manchen und als Server in anderen agieren.

Eine DDE-Konversation findet zwischen zwei Fenstern statt, einer für jede der beteiligten Anwendungen. Ein Fenster ist möglicherweise das Hauptfenster der Anwendung. ein Fenster, das einem bestimmten Dokument zugeordnet ist, wie in einer MDI-Anwendung (Multiple Document Interface). oder ein verborgenes (unsichtbares) Fenster, dessen einziger Zweck die Verarbeitung von DDE-Nachrichten ist.

Da eine DDE-Konversation durch das Paar von Handles für die in der Konversation beteiligten Fenster identifiziert wird, sollte kein Fenster in mehr als einer Konversation mit einem anderen Fenster eingebunden werden. Entweder muss die Client Anwendung oder die Serveranwendung für jede Ihrer Konversationen mit einem bestimmten Server oder einer Client Anwendung ein anderes Fenster bereitstellen.

Eine Anwendung kann sicherstellen, dass ein paar von Client-und Server Fenstern nie an mehr als einer Konversation beteiligt ist, indem für jede Konversation ein ausgeblendetes Fenster erstellt wird Der einzige Zweck dieses Fensters ist die Verarbeitung von DDE-Nachrichten.

### <a name="application-topic-and-item-names"></a>Anwendungs-, Themen-und Elementnamen

Das DDE-Protokoll identifiziert die Einheiten der Daten, die zwischen dem Client und dem Server mit einer Hierarchie mit drei Ebenen von Anwendungs-, Thema-und Elementnamen übermittelt werden.

Jede DDE-Konversation wird durch den Anwendungsnamen und das Thema eindeutig definiert. Am Anfang einer DDE-Konversation bestimmen der Client und der Server den Anwendungsnamen und das Thema. Der Anwendungsname ist in der Regel der Name der Serveranwendung. Wenn Excel z. b. als Server in einer Konversation fungiert, lautet der Anwendungsname Excel.

Das DDE-Thema ist eine allgemeine Klassifizierung von Daten, in denen mehrere Datenelemente während der Konversation "besprochen" (ausgetauscht) werden können. Bei Anwendungen, die auf dateibasierten Dokumenten basieren, ist das Thema normalerweise ein Dateiname. Bei anderen Anwendungen ist das Thema ein anwendungsspezifischer Name.

Da im Client-und Server Fenster eine DDE-Konversation verwendet wird, können der Anwendungsname und das Thema, die eine Konversation definieren, während der Konversation nicht geändert werden.

Ein DDE-Datenelement stellt Informationen im Zusammenhang mit dem zwischen den Anwendungen ausgetauschten Konversations Thema dar. Werte für das Datenelement können vom Server an den Client oder vom Client an den Server übermittelt werden. Daten können mit einem beliebigen Standard-Zwischenablage Format oder mit einem registrierten Zwischenablage Format übermittelt werden. Ein spezielles, registriertes Format namens Link identifiziert ein Element in einer DDE-Konversation. Weitere Informationen zu Zwischenablage Formaten finden Sie unter [Zwischenablage](clipboard.md).

### <a name="the-system-topic"></a>Das System Thema

Anwendungen sollten das Thema System jederzeit unterstützen. Dieses Thema enthält einen Kontext für Informationen, die für eine andere Anwendung von allgemeinem Interesse sein können.

Datenelement Werte müssen im Format der CF- [**\_ Text**](standard-clipboard-formats.md) Zwischenablage gerendert werden. Einzelne Elemente von Element Werten für ein System Thema müssen durch Tabstopps getrennt werden. In der folgenden Tabelle werden einige Elemente für das System Thema vorgeschlagen.



| Element          | BESCHREIBUNG                                                                                                                                                                                                                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Formate       | Durch Tabstopps getrennte Liste der Zwischenablage Formate, die von der Anwendung dargestellt werden können. In der Regel werden **\_ CF** -Formate mit dem "**CF \_**"-Teil der entfernten Namen aufgelistet (z. b. ist der CF- **\_ Text** als "**Text**" aufgeführt).                                                                                        |
| Hilfe          | Text, der kurz erläutert, wie der DDE-Server verwendet wird.                                                                                                                                                                                                                                                   |
| ReturnMessage | Unterstützende Details der zuletzt verwendeten [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht. Dieses Element ist nützlich, wenn mehr als acht Bits von anwendungsspezifischen Rückgabe Daten erforderlich sind.                                                                                                                |
| Status        | Gibt den aktuellen Status der Anwendung an. Wenn ein Server eine [**WM- \_ DDE- \_ Anforderungs**](wm-dde-request.md) Nachricht für dieses System Topic-Element empfängt, sollte er Antworten, indem er eine WM-DDE- [**\_ \_ Daten**](wm-dde-data.md) Meldung mit einer Zeichenfolge bereitstellt, die je nach Bedarf entweder ausgelastet oder bereit ist. |
| SysItems      | Liste der System Topic-Elemente, die von der Anwendung unterstützt werden.                                                                                                                                                                                                                                                    |
| Topicitemlist | Vergleichbar mit dem Element SysItems, mit der Ausnahme, dass topicitemlist für jedes andere Thema als das System Thema unterstützt werden soll. Dies ermöglicht das Durchsuchen der Elemente, die unter jedem Thema unterstützt werden. Wenn die Elemente nicht aufgelistet werden können, sollte dieses Element nur "topicitemlist" enthalten.                                  |
| Themen        | Liste der Themen, die von der Anwendung zum aktuellen Zeitpunkt unterstützt werden. Diese Liste kann von Zeit zu Zeit abweichen.                                                                                                                                                                                                  |



 

### <a name="permanent-data-links"></a>Permanente Daten Verknüpfungen

Nachdem eine DDE-Konversation begonnen hat, kann der Client eine oder mehrere permanente Daten Verknüpfungen mit dem Server einrichten. Ein Daten Link ist ein Kommunikationsmechanismus, mit dem der Server den Client benachrichtigt, wenn sich der Wert eines angegebenen Datenelements ändert. Der Daten Link ist in dem Sinne permanent, dass dieser Benachrichtigungs Prozess fortgesetzt wird, bis die Datenverknüpfung oder die DDE-Konversation selbst beendet wird.

Es gibt zwei Arten von permanenten DDE-Daten Verknüpfungen: "warm" und "Hot". Bei einem Link zu einem warmen Daten benachrichtigt der Server den Client, dass sich der Wert des Datenelements geändert hat, der Server sendet den Datenwert jedoch erst an den Client, wenn er vom Client angefordert wird. Bei einem Link für heiße Daten sendet der Server sofort den geänderten Datenwert an den Client.

Anwendungen, die warm-oder Hot-Daten Links unterstützen, stellen in der Regel einen Befehl zum **Kopieren** oder **Einfügen** von Links im **Bearbeitungs** Menü bereit, damit der Benutzer Links zwischen Anwendungen einrichten kann.

### <a name="atoms-and-shared-memory-objects"></a>Atome und Shared Memory-Objekte

Bestimmte Argumente von DDE-Nachrichten sind globale Atome oder Shared Memory-Objekte. Anwendungen, die diese Argumente verwenden, müssen explizite Regeln zum Zeitpunkt der Zuteilung und Löschung befolgen. In allen Fällen muss der Absender der Nachricht alle Atom-oder Shared Memory-Objekte löschen, die der beabsichtigte Empfänger aufgrund eines Fehler Zustands nicht empfängt, wie z. b. Fehler bei der [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion.

DDE verwendet freigegebene Speicher Objekte für drei Zwecke:

-   , Um einen auszutauschenden Datenelement Wert zu übertragen. Dabei handelt es sich um ein Element, auf das der *hdata* -Parameter in den [**WM-DDE- \_ \_ Daten**](wm-dde-data.md) -und [**WM \_ \_**](wm-dde-poke.md)
-   Zum Übertragen von Optionen in einer Nachricht. Dies ist ein Element, auf das durch den *hoptions* -Parameter in einer [**WM-DDE- \_ \_ Empfehlung**](wm-dde-advise.md) Meldung verwiesen wird.
-   , Wenn eine Befehls Ausführungs Zeichenfolge ausgeführt werden soll. Dabei handelt es sich um ein Element, auf das der *hcommands* -Parameter in der [**WM- \_ DDE- \_ Execute**](wm-dde-execute.md) -Nachricht und die zugehörige [**WM \_ \_**](wm-dde-ack.md)

Eine Anwendung, die ein DDE Shared Memory-Objekt empfängt, muss es als schreibgeschützt behandeln. Die Anwendung darf das Objekt nicht als gegenseitiger Lese-/Schreibbereich für den freien Datenaustausch verwenden.

Wie bei einem DDE-Atom sollte eine Anwendung ein frei gegebenes Speicher Objekt freigeben, um den Arbeitsspeicher effektiv zu verwalten. Die Anwendung sollte auch Speicher Objekte Sperren und entsperren.

## <a name="dynamic-data-exchange-messages-overview"></a>Übersicht über dynamischer Datenaustausch Meldungen

Da DDE ein Nachrichten basiertes Protokoll ist, werden keine Funktionen oder Bibliotheken verwendet. Alle DDE-Transaktionen werden durchgeführt, indem bestimmte definierte DDE-Meldungen zwischen den Client-und Server Fenstern übergeben werden.

Es sind neun DDE-Nachrichten vorhanden. die symbolischen Konstanten für diese Nachrichten werden in der DDE-Header Datei definiert. Bestimmte Strukturen für die verschiedenen DDE-Nachrichten werden in dieser Header Datei ebenfalls definiert.

In der folgenden Tabelle werden die DDE-Meldungen zusammengefasst.



| `Message`                                        | BESCHREIBUNG                                                                                                                                      |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM-DDE-Bestätigung \_ \_**](wm-dde-ack.md)             | Bestätigt, dass eine Nachricht empfangen oder nicht empfangen wird.                                                                                               |
| [**WM \_ DDE- \_ Empfehlung**](wm-dde-advise.md)       | Fordert die Serveranwendung auf, bei jeder Änderung ein Update oder eine Benachrichtigung für ein Datenelement bereitzustellen. Dadurch wird eine permanente Datenverknüpfung hergestellt. |
| [**WM- \_ DDE- \_ Daten**](wm-dde-data.md)           | Sendet einen Datenelement Wert an die Client Anwendung.                                                                                               |
| [**WM \_ DDE \_ Ausführen**](wm-dde-execute.md)     | Sendet eine Zeichenfolge an die Serveranwendung, bei der die Zeichenfolge als eine Reihe von Befehlen verarbeitet wird.                                       |
| [**WM \_ DDE \_ initiieren**](wm-dde-initiate.md)   | Initiiert eine Konversation zwischen Client-und Server Anwendungen.                                                                             |
| [**WM \_ DDE \_ Poke**](wm-dde-poke.md)           | Sendet einen Datenelement Wert an die Serveranwendung.                                                                                               |
| [**WM- \_ DDE- \_ Anforderung**](wm-dde-request.md)     | Fordert die Serveranwendung auf, den Wert eines Datenelements bereitzustellen.                                                                             |
| [**WM- \_ DDE \_ Beenden**](wm-dde-terminate.md) | Beendet eine Konversation.                                                                                                                       |
| [**WM \_ DDE \_ nicht Empfehlung**](wm-dde-unadvise.md)   | Beendet einen permanenten Daten Link.                                                                                                                |



 

Eine Anwendung ruft [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) auf, um die [**WM-DDE- \_ \_ initiierte**](wm-dde-initiate.md) Nachricht auszugeben, oder eine [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht, die als Reaktion auf **WM \_ DDE \_ initiieren** gesendet wird Alle anderen Nachrichten werden von [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)gesendet. Der erste Parameter dieser Aufrufe ist ein Handle für das empfangende Fenster. der zweite Parameter enthält die zu sendende Nachricht. der dritte Parameter identifiziert das sendende Fenster. und der vierte Parameter enthält die Nachrichten spezifischen Argumente.

## <a name="dynamic-data-exchange-message-flow"></a>dynamischer Datenaustausch Nachrichtenfluss

Eine typische DDE-Konversation besteht aus den folgenden Ereignissen:

1.  Die Client Anwendung initiiert die Konversation, und die Serveranwendung antwortet.
2.  Die Anwendungen tauschen Daten mit einer oder allen der folgenden Methoden aus:
    -   -   Die Serveranwendung sendet Daten an den Client bei der Client Anforderung.
        -   Die Client Anwendung sendet nicht angeforderte Daten an die Serveranwendung.
        -   Die Client Anwendung fordert die Serveranwendung auf, den Client zu benachrichtigen, wenn sich ein Datenelement ändert (der Link "warm"
        -   Die Client Anwendung fordert die Serveranwendung auf, Daten immer dann zu senden, wenn die Daten geändert werden (Hot Data Link).
        -   Die Serveranwendung führt einen Befehl bei der Client Anforderung aus.

3.  Die Client-oder Serveranwendung beendet die Konversation.

Ein Anwendungsfenster, das Anforderungen von einem Client oder Server verarbeitet, muss sie strikt in der Reihenfolge verarbeiten, in der Sie empfangen werden.

Ein Client kann Konversationen mit mehr als einem Server einrichten. ein Server kann über Konversationen mit mehreren Clients verfügen. Wenn Sie Nachrichten von mehreren Quellen verarbeiten, muss ein Client oder Server die Nachrichten einer Konversation synchron verarbeiten, aber nicht alle Nachrichten synchron verarbeiten. Anders ausgedrückt: Es kann bei Bedarf von einer Konversation in eine andere verschoben werden.

Wenn eine Anwendung eine eingehende Anforderung nicht verarbeiten kann, weil Sie auf eine DDE-Antwort wartet, muss Sie Deadlocks verhindern, indem Sie eine [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht mit dem **fbusy** -Member der [**ddeack**](/windows/desktop/api/Dde/ns-dde-ddeack) -Struktur bereitstellt, die auf 1 festgelegt ist. Eine Anwendung kann auch eine ausgelastete **WM- \_ DDE \_** -Bestätigungsnachricht senden, wenn eine eingehende Anforderung aus irgendeinem Grund nicht innerhalb eines angemessenen Zeitraums verarbeitet werden kann.

Eine Anwendung sollte in der Lage sein, den Ausfall eines Clients oder Servers zu behandeln, der innerhalb eines bestimmten Zeitraums auf eine Nachricht antwortet. Da das Timeout Intervall abhängig von der Art der Anwendung und der Konfiguration des Benutzer Systems (einschließlich der Verbindung mit einem Netzwerk) variieren kann, sollte die Anwendung dem Benutzer die Möglichkeit geben, das Intervall anzugeben.

## <a name="parameter-packing-functions"></a>Parameter Verpackungs Funktionen

Der *LPARAM* -Parameter vieler DDE-Nachrichten enthält zwei Datenelemente. Beispielsweise enthält das *LPARAM* der [**WM- \_ DDE- \_ Daten**](wm-dde-data.md) Nachricht ein Daten Handle und ein Atom. Anwendungen müssen die [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) -Funktion verwenden, um das Handle und Atom in einen *LPARAM* -Parameter zu packen, und die [**unpackddelta param**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) -Funktion, um die Werte zu entfernen. DDE-Anwendungen müssen **packddelta param** und **unpackddelta param** für alle Nachrichten verwenden, die während einer DDE-Konversation gepostet werden.

Anwendungen können auch die Funktionen [**reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) und [**freeddelta param**](/windows/desktop/api/Dde/nf-dde-freeddelparam) verwenden. **Reuseddelta param** ermöglicht einer DDE-Anwendung die Wiederverwendung eines gepackten *LPARAM* -Parameters, wodurch die Anzahl der Speicher Belegungen verringert wird, die die Anwendung während einer Konversation ausführen muss. Eine Anwendung kann " **freeddelta param** " verwenden, um den Arbeitsspeicher freizugeben, der einem während einer DDE-Konversation empfangenen Daten Handle zugeordnet ist.

## <a name="dynamic-data-exchange-and-impersonation"></a>dynamischer Datenaustausch und Identitätswechsel

Damit ein Server die Identität eines Clients annehmen kann, ruft der Client die [**ddesetqualityofservice**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) -Funktion auf. Die Struktur der [**sicherheitsidentitäts Wechsel \_ \_ Ebene**](/windows/win32/api/winnt/ne-winnt-security_impersonation_level) wird zum Steuern der Identitätswechsel Ebene verwendet, die der Server ausführen kann.

Ein DDE-Server kann die Identität eines DDE-Clients durch Aufrufen der Identität [**ateddeclientwindow**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) -Funktion annehmen. Ein Ddeml-Server sollte die [**DdeImpersonateClient**](/windows/desktop/api/Ddeml/nf-ddeml-ddeimpersonateclient) -Funktion verwenden.

 

 