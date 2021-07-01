---
title: Inhaltsindizierungsdienste-Protokoll
description: Dieses Dokument ist eine Spezifikation des Content Indexing Service-Protokolls.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14573dac5a7a6818234c086d05b52e5b81c2a1c1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119735"
---
# <a name="content-indexing-services-protocol"></a>Inhaltsindizierungsdienste-Protokoll

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren [Versionen Windows Search.](../search/-search-3x-wds-overview.md)

Protokollspezifikation, Version 0.12

-   [1 Einführung](#1-introduction)
    -   [1.1 Glossar](#11-glossary)
    -   [1.2 Verweise](#12-references)
    -   [1.3 Protokollübersicht (Synopsis)](#13-protocol-overview-synopsis)
    -   [1.4 Beziehung zu anderen Protokollen](#14-relationship-to-other-protocols)
    -   [1.5 Voraussetzungen und Vorbedingungen](#15-prerequisites-and-preconditions)
    -   [1.6 Anwendbarkeitsanweisung](#16-applicability-statement)
    -   [1.7 Versionsverwaltung und Funktionsübertragung](#17-versioning-and-capability-negotiation)
    -   [1.8 Durch Hersteller erweiterbare Felder](#18-vendor-extensible-fields)
    -   [1.9 Zuweisungen von Standards](#19-standards-assignments)
-   [2\. Nachrichten](#2-messages)
    -   [2.1 Transport](#21-transport)
    -   [2.2 Nachrichtensyntax](#22-message-syntax)
-   [3 Protokolldetails](#3-protocol-details)
    -   [3.1 Serverdetails](#31-server-details)
    -   [3.2 Clientdetails](#32-client-details)
-   [4 Beispiele für Protokolle](#4-protocol-examples)
    -   [4.1 Beispiel 1](#41-example-1)
    -   [4.2 Beispiel 2](#42-example-2)
-   [5 Sicherheit](#5-security)
    -   [5.1 Sicherheitsüberlegungen für Ausführende](#51-security-considerations-for-implementers)
    -   [5.2 Index von Sicherheitsparameter](#52-index-of-security-parameters)
-   [6 Index des versionsspezifischen Verhaltens](#6-index-of-version-specific-behavior)

Dieses Dokument ist eine Spezifikation des Content Indexing Service-Protokolls.

Die WSPP-Dokumentation (Workgroup Server Protocol Program) ist für die Verwendung in Verbindung mit dokumentation zu öffentlichen Standards, Netzwerkprogrammierungsart und Konzepten verteilter Windows-Arbeitsgruppensysteme vorgesehen und setzt voraus, dass der Leser entweder mit dem oben genannten Material vertraut ist oder sofortigen Zugriff darauf hat.

Eine WSPP-Protokollspezifikation erfordert nicht die Verwendung von Microsoft-Programmiertools oder -Programmierumgebungen, damit ein Lizenzer eine Implementierung entwickeln kann. Lizenzlizenzen, die Zugriff auf Microsoft-Programmiertools und -umgebungen haben, können diese nutzen.

## <a name="1-introduction"></a>1 Einführung

-   [1.1 Glossar](#11-glossary)
-   [1.2 Verweise](#12-references)
-   [1.3 Protokollübersicht (Synopsis)](#13-protocol-overview-synopsis)
-   [1.4 Beziehung zu anderen Protokollen](#14-relationship-to-other-protocols)
-   [1.5 Voraussetzungen und Vorbedingungen](#15-prerequisites-and-preconditions)
-   [1.6 Anwendbarkeitsanweisung](#16-applicability-statement)
-   [1.7 Versionsverwaltung und Funktionsübertragung](#17-versioning-and-capability-negotiation)
-   [1.8 Durch Hersteller erweiterbare Felder](#18-vendor-extensible-fields)
-   [1.9 Zuweisungen von Standards](#19-standards-assignments)

### <a name="11-glossary"></a>1.1 Glossar

> [!Note]  
> Die folgenden Begriffe werden im Glossarabschnitt von \[ MS-SYS \] definiert:
>
> -   GUID
> -   Little Endian
> -   Named Pipe
> -   `Path`

 

**Bindung:** Eine Anforderung zum Einbinden einer **bestimmten Spalte** in ein zurückgegebenes **Rowset.** Die **Bindung** gibt eine Eigenschaft an, die in die Suchergebnisse aufgenommen werden soll.

**Lesezeichen:** Ein Marker, der eine Zeile innerhalb einer Gruppe von Zeilen eindeutig identifiziert.

**Katalog:** Die Organisationseinheit der höchsten Ebene im Indizierungsdienst. Sie stellt einen Satz indizierter Dokumente dar, für die Abfragen mithilfe des Content Indexing Service-Protokolls ausgeführt werden können.

**Kategorie:** Eine hierarchische Gruppierung von Zeilen. Beispielsweise kann ein Abfrageergebnis, das die Spalten author und title enthält, basierend auf dem Autor kategorisiert werden. Jede Gruppe von Zeilen, die denselben Wert für author enthalten, würde eine Kategorie bilden.

**Kapitel** : Ein Zeilenbereich **innerhalb** einer Gruppe von **Zeilen.**

**Spalte:** Der Container für einen einzelnen Informationstyp in einer **Zeile.** Spalten werden Eigenschaftsnamen zuordnen und angeben, welche Eigenschaften für die Befehlsstrukturelemente der **Suchabfrage** **verwendet** werden.

**Befehlsstruktur:** Eine Kombination aus **Einschränkungen,** **Kategorien** und Sortierreihenfolge, die für die Suchabfrage angegeben ist. 

**Cursor:** Eine Entität, die als Mechanismus  zum Arbeiten mit  einer Zeile oder einem kleinen Zeilenblock gleichzeitig in einem Satz von Daten verwendet wird, die in einem Resultset zurückgegeben werden. Ein **Cursor** wird in einer einzelnen Zeile **innerhalb des** Resultsets positioniert. Nachdem der **Cursor** in einer Zeile positioniert wurde, können Vorgänge für diese Zeile oder für einen Zeilenblock ausgeführt **werden,** **der** an dieser Position beginnt.

**Handle:** Ein Token, das verwendet werden kann, um **Cursor,** Kapitel und Lesezeichen zu identifizieren **und darauf zu zugreifen.** 

**Index:** Eine persistente Struktur, die den Textinhalt enthält, der von einem Indizierungsdienst aus Dateien **gezogen wurde.** Dies schließt die Liste der Wörter ein, die zusammen mit dem enthaltenden Dateinamen, der Wortposition und dem **-Locale gespeichert werden.**

**Indizierung:** Der Prozess, bei dem Text und Eigenschaften aus Dateien extrahiert und die extrahierten Werte in den Indizes **(für** Text) und im Eigenschaftencache **(für** Eigenschaften) gespeichert werden.

**Indizierungsdienst:** Ein Dienst, der indizierte **Kataloge** für den Inhalt und die Eigenschaften von Dateisystemen erstellt. Anwendungen können die Kataloge nach Informationen aus den Dateien im indizierten Dateisystem durchsuchen.

**Locale**: Ein Bezeichner, wie in \[ MS-GPSI Anhang A angegeben, der Einstellungen \] im Zusammenhang mit der Sprache angibt. Diese Einstellungen geben an, wie Datumsangaben und Zeiten formatiert, Elemente alphabetisch sortiert, Zeichenfolgen verglichen werden sollen, und so weiter.

**Abfrage in natürlicher Sprache:** Eine Abfrage, die mit menschlicher Sprache anstelle der Abfragesyntax erstellt wurde.

**Rauschwort:** Ein Wort, das vom Indizierungsdienst  ignoriert wird, wenn es in den für die Suchabfrage angegebenen Einschränkungen vorhanden ist, da es nur einen geringen wertwert hat. Beispiele für Englisch sind "a", "and" und "the".

**Eigenschaftencache:** Ein Cache von Dateieigenschaften, die von einem **Indizierungsdienst extrahiert wurden.**

**Eigenschaftenindizierung:** Der Prozess  zum  Erstellen eines Indexes von Werttypeigenschaften eines Dokuments, einschließlich Autor, Betreff, Typ, Wortanzahl, Anzahl gedruckter Seiten und anderer Eigenschaften.

**Einschränkung:** Eine Reihe von Bedingungen, die eine Datei erfüllen muss, um in die Suchergebnisse aufgenommen zu werden, die vom Indizierungsdienst **als** Reaktion auf eine Suchabfrage zurückgegeben werden. Eine **Einschränkung** schränkt den Fokus einer Suchabfrage  ein und beschränkt die Dateien, die der Indizierungsdienst in die Suchergebnisse einschränkt, auf dieJenigen, die den Bedingungen entsprechen.

**Row**: Die Auflistung von Spalten **mit** den Eigenschaftswerten, die eine  einzelne Datei aus dem Satz von Dateien beschreiben, die den Einschränkungen in der an den Indizierungsdienst übermittelten Suchabfrage **entsprechen.**

**Rowset:** Eine Reihe von **Zeilen, die** in den Suchergebnissen zurückgegeben werden.

**Sortierreihenfolge:** Der Satz von Regeln in einer Suchabfrage, die die Reihenfolge der Zeilen im Suchergebnis definieren. Jede Regel besteht aus einer Eigenschaft (Name, Größe usw.) und einer Richtung für die Reihenfolge (aufsteigend oder absteigend). Mehrere Regeln werden sequenziell angewendet.

**Texttypeigenschaft:** Eine Eigenschaft, die den Inhalt eines Dokuments beschreibt und dem Namen nur unformatierten Text zugeordnet ist.

**Werttypeigenschaft:** Eine Eigenschaft, die ein einzelnes Attribut eines gesamten Dokuments beschreibt. Eine Werttypeigenschaft verfügt über eine Datentyp-ID und einen Wert dieses Datentyps, der dem Namen zugeordnet ist.

**Virtueller Stamm:** Ein alternativer Pfad zu einem Ordner. Ein physischer Ordner kann null oder mehr virtuelle Stämme haben. Pfade, die mit einem virtuellen Stamm beginnen, werden als virtuelle Pfade bezeichnet. Beispielsweise kann /server/vanityroot ein virtueller Stamm von C: \\ IIS \\ web \\ folder1 sein. Anschließend würde die Datei C: IIS web folder1default.htm den virtuellen Pfad \\ \\ \\ \\ /server/vanityroot/default.htm.

**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT:** Diese Begriffe (in allen Obergrenzen) werden wie in \[ RFC2119 beschrieben \] verwendet. Alle Aussagen zu optionalem Verhalten enthalten die Worte KÖNNEN, SOLLTEN oder SOLLTEN NICHT.

### <a name="12-references"></a>1.2 Verweise

### <a name="121-normative-references"></a>1.2.1 Normative Verweise

\[IEEE754 \] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html

\[MS-DCOM \] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", Juni 2006.

\[MS-GPSI \] Microsoft Corporation, "Gruppenrichtlinie für die Softwareinstallation Extension", Juni 2006.

\[MS-SMB \] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions", Mai 2006.

\[MS-SYS \] Microsoft Corporation, "Systemübersicht v4", Juli 2006.

\[SALTON \] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.

\[UNICODE \] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org

### <a name="122-informative-references"></a>1.2.2 Informative Verweise

\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .

\[MSDN-QUERYERR \] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp

### <a name="13-protocol-overview-synopsis"></a>1.3 Protokollübersicht (Synopsis)

Ein **Inhaltsindizierungsdienst** hilft dabei, die extrahierten Funktionen einer Sammlung von Dokumenten effizient zu organisieren. Das Content Indexing Service-Protokoll (CISP) ermöglicht einem Client die Kommunikation mit einem Server, der einen Indizierungsdienst hostet, um Abfragen auszugeben und einem Administrator die Verwaltung des Indizierungsservers zu ermöglichen.

Bei der Verarbeitung von Dateien analysiert ein Indizierungsdienst eine Reihe von Dokumenten und organisiert ihren Inhalt so neu, dass **Eigenschaften** dieser Dokumente als Reaktion auf Abfragen effizient zurückgegeben werden können. Eine Auflistung von Dokumenten, die abgefragt werden können, umfasst einen **Katalog.** Ein Katalog kann einen **Index** (für kurze Verweise auf Text) und einen **Eigenschaftencache** (zum schnellen Abrufen von Eigenschaftswerten) enthalten.

Konzeptionell besteht ein Katalog aus einer logischen "Tabelle" von Eigenschaften mit dem Text oder Wert und dem entsprechenden Gebietsschema, das in **Spalten** der Tabelle gespeichert ist. Jede "Zeile" der Tabelle entspricht einem separaten Dokument im Bereich des Katalogs, und jede "Spalte" der Tabelle entspricht einer -Eigenschaft.

Die von CISP ausgeführten spezifischen Aufgaben werden in zwei Funktionsbereiche gruppiert:

-   Remoteverwaltung von Indizierungsdienstkatalogen,
-   Remoteabfragen von Indizierungsdienstkatalogen.

### <a name="131-remote-administration-tasks"></a>1.3.1 Remoteverwaltungsaufgaben

CISP ermöglicht die folgenden Indizierungsdienst-Katalogverwaltungsaufgaben von einem Client aus:

-   Fragen Sie den aktuellen Status eines Indizierungsdienstkatalogs auf dem Server ab.
-   Aktualisieren sie den Status eines Indizierungsdienstkatalogs.
-   Starten Sie den Indizierungsprozess für einen bestimmten Satz von Dateien.
-   Initiieren Sie die Optimierung eines Indexes, um die Abfrageleistung zu verbessern.

Alle Remoteverwaltungsaufgaben folgen einem einfachen Anforderungs-/Antwortmodell. Für Verwaltungsaufrufe wird kein Zustand auf dem Client beibehalten, und Verwaltungsaufrufe können in beliebiger Reihenfolge erfolgen.

### <a name="132-remote-querying"></a>1.3.2 Remoteabfragen

CISP ermöglicht Clients das Ausführen von Suchabfragen für einen Remoteserver, der einen Indizierungsdienst hostet.

Das Senden einer Suchabfrage ist ein mehrstufiger Prozess, der vom Client initiiert wird. Die Schritte lauten wie folgt:

1.  Der Client fordert eine Verbindung mit einem Server an, der einen Indizierungsdienst hostet.
2.  Der Client sendet die Parameter für die Suchabfrage, einschließlich:
    -   Die **Einschränkungen,** mit denen angegeben wird, welche Dokumente in die Suchergebnisse aufgenommen bzw. aus diesen ausgeschlossen werden sollen.
    -   Die Reihenfolge, in der die Suchergebnisse zurückgegeben werden sollen.
    -   Die Spalten, die im Resultset zurückgegeben werden sollen.
    -   Die maximale Anzahl von **Zeilen,** die für die Abfrage zurückgegeben werden sollen.
    -   Die maximale Zeit für die Abfrageausführung.

        Nachdem der Server die Anforderung des Clients zum Initiieren der Abfrage bestätigt hat, kann der Client Statusinformationen zur Abfrage anfordern, dies ist jedoch kein erforderlicher Schritt.

3.  Der Client gibt dann an, welche Eigenschaften der Server in die Suchergebnisse aufnehmen soll.
4.  Der Client fordert ein Resultset vom Server an, und der Server antwortet, indem er dem Client die Eigenschaftswerte für Dateien sendet, die in den Ergebnissen für die Suchabfrage des Clients enthalten waren. Wenn der Wert einer Eigenschaft zu groß ist, um in einen einzelnen Antwortpuffer zu passen, sendet der Server die Eigenschaft nicht, sondern legt den Eigenschaftsstatus auf verzögert fest. Der Client fordert den Eigenschaftswert dann separat mithilfe einer Reihe von Anforderungen für aufeinander folgende Blöcke des Werts an und setzt dann die Anforderung anderer Werte fort.
5.  Sobald der Client mit der Suchabfrage fertig ist und keine zusätzlichen Ergebnisse mehr benötigt, kontaktiert der Client den Server, um die Abfrage freizugeben.
6.  Nachdem der Server die Abfrage freigegeben hat, kann der Client eine Anforderung senden, um die Verbindung mit dem Server zu trennen. Die Verbindung wird dann geschlossen. Alternativ kann der Client eine weitere Abfrage ausführen und die Sequenz aus Schritt 2 wiederholen.

Windows-Verhalten: Dieses Protokoll ist unter Windows 2000, Windows XP, Windows Server 2003 und Windows Vista implementiert.

### <a name="14-relationship-to-other-protocols"></a>1.4 Beziehung zu anderen Protokollen

CISP verwendet das SMB \[ MS-SMB-Protokoll für den \] Nachrichtentransport. Kein anderes Protokoll hängt direkt vom Content Indexing Service-Protokoll ab.

*Windows-Verhalten: Anwendungen interagieren in der Regel mit einem OLE DB Schnittstellenwrapper \[ MSDN-OLEDB \] (z.B. einem Protokollclient) und nicht direkt mit dem Protokoll.*

### <a name="15-prerequisites-and-preconditions"></a>1.5 Voraussetzungen und Vorbedingungen

Es wird davon ausgegangen, dass der Client den Namen des Servers und einen Katalognamen abgerufen hat, bevor dieses Protokoll aufgerufen wird. Die Vorgehensweise eines Clients liegt außerhalb des Bereichs dieser Spezifikation.

Außerdem wird davon ausgegangen, dass client und server über eine Sicherheitszuordnung verfügen, die mit Named Pipes MS-SMB verwendet werden \[ \] kann.

### <a name="16-applicability-statement"></a>1.6 Anwendbarkeitsanweisung

CISP ist für das Abfragen und Verwalten von Katalogen auf einem Remoteserver von einem Client aus konzipiert. CISP ist unter Windows Vista veraltet.

### <a name="17-versioning-and-capability-negotiation"></a>1.7 Versionsverwaltung und Funktionsübertragung

Dieses Protokoll verfügt über keine Mechanismen zur Versions- oder Funktionsaushandlung.

### <a name="18-vendor-extensible-fields"></a>1.8 Durch Hersteller erweiterbare Felder

Dieses Protokoll verwendet HRESULTs, die vom Anbieter erweiterbar sind. Anbieter können ihre eigenen Werte für dieses Feld auswählen, solange das C-Bit (0x20000000) wie in Abschnitt 4.1.1 von MS-SYS angegeben festgelegt \[ \] ist, was angibt, dass es sich um einen Kundencode handelt.

Dieses Protokoll verwendet auch NTSTATUS-Werte, die aus dem in MS-SYS definierten \[ NTSTATUS-Nummernbereich \] stammen. Anbieter SOLLTEN diese Werte mit ihrer angegebenen Bedeutung wiederverwenden. Die Auswahl eines anderen Werts birgt das Risiko eines Konflikts in der Zukunft.

*Windows-Verhalten: Windows verwendet nur die in Abschnitt 4.1.3 von MS-SYS angegebenen \[ \] Werte.*

### <a name="181-property-ids"></a>1.8.1 Eigenschaften-IDs

Eigenschaften werden durch IDs dargestellt, die als Eigenschaften-IDs bezeichnet werden. Jede Eigenschaft muss über einen global eindeutigen Bezeichner verfügen. Dieser Bezeichner besteht aus einer **GUID,** die eine Auflistung von Eigenschaften darstellt, die als Eigenschaftensatz bezeichnet werden, sowie einer Zeichenfolge oder einer 32-Bit-Ganzzahl, um die Eigenschaft innerhalb des Satzes zu identifizieren. Wenn die ganzzahlige Form der ID verwendet wird, werden die Werte 0x00000000, 0xFFFFFFFF und 0xFFFFFFFE als ungültig betrachtet.

Anbieter können sicherstellen, dass ihre Eigenschaften eindeutig definiert werden, indem sie sie in einem Eigenschaftensatz platzieren, der durch ihre eigene GUID definiert wird.

### <a name="19-standards-assignments"></a>1.9 Zuweisungen von Standards

Dieses Protokoll weist keine Standardzuweisungen auf, sondern nur private Zuweisungen, die von Microsoft mithilfe von Zuordnungsverfahren vorgenommen werden, die in anderen Protokollen angegeben sind.

Microsoft hat diesem Protokoll eine Benannte Pipe zugeordnet, wie in \[ MS-SMB \] angegeben. Die Zuweisung ist:



| Parameter | Wert             | Verweis  |
|-----------|-------------------|------------|
| Pipename | \\\\ \_ Pipe-CI-SKADS | \[MS-SMB\] |



 

## <a name="2-messages"></a>2\. Nachrichten

-   [2.1 Transport](#21-transport)
-   [2.2 Nachrichtensyntax](#22-message-syntax)

### <a name="21-transport"></a>2.1 Transport

Alle Nachrichten MÜSSEN mithilfe einer Named Pipe übertragen werden, wie in \[ MS-SMB \] angegeben. Der folgende Pipename wird verwendet:

-   \\\\ \_ Pipe-CI-SKADS

Dieses Protokoll verwendet das zugrunde liegende SMB-Named Pipe-Protokoll, um die Identität des Aufrufers abzurufen, der die Verbindung hergestellt hat, wie in Abschnitt 2.2.8 von \[ MS-SMB \] angegeben. Der Client MUSS SECURITY \_ IDENTIFICATION als ImpersonationLevel in der Anforderung festlegen, um die Named Pipe zu öffnen.

### <a name="22-message-syntax"></a>2.2 Nachrichtensyntax

Mehrere Strukturen und Meldungen in den folgenden Abschnitten beziehen sich auf Kapitel- oder Lesezeichenhandles. Ein Handle ist eine 32-Bit-lange nicht transparente Struktur, die ein Kapitel oder Lesezeichen eindeutig identifiziert. In der Regel empfangen Clientanwendungen Handlewerte über Methodenaufrufe. es gibt jedoch mehrere bekannte Werte, die nicht von einem Server abgerufen werden müssen, dessen Bedeutung in der folgenden Tabelle angegeben ist:



| Wert                         | Bedeutung                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| DB \_ NULL \_ HCHAPTER 0x00000000 | Ein Kapitelhandle für das nicht gekachelte Rowset, das alle Abfrageergebnisse enthält.    |
| DBBMK \_ FIRST 0x00000001       | Ein Lesezeichenhandle für ein Lesezeichen, das die erste Zeile im Rowset identifiziert. |
| DBBMK \_ LAST 0x00000002        | Ein Lesezeichenhand handle für ein Lesezeichen, das die letzte Zeile im Rowset identifiziert.  |



 

### <a name="221-structures"></a>2.2.1 Strukturen

In diesem Abschnitt werden Datenstrukturen beschrieben, die von CISP definiert und verwendet werden.

Alle 2-, 4- und 8-Byte-Ganzzahlen mit und ohne Vorzeichen in den folgenden Strukturen MÜSSEN in Little-Endian-Byte-Reihenfolge übertragen werden.

In der folgenden Tabelle sind die in diesem Abschnitt definierten Datenstrukturen zusammengefasst.



| Struktur                    | Beschreibung                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| CBaseStorageVariant          | Enthält den Wert, für den eine Übereinstimmungsoperation für eine In einer CPropertyRestriction-Struktur angegebene Eigenschaft durchgeführt werden soll. |
| SAFEARRAY, SAFEARRAY2        | Enthält ein mehrdimensionales Array.                                                                                     |
| SAFEARRAYBOUND               | Stellt die Begrenzungen für eine Dimension eines Arrays dar, das in einer SAFEARRAY-Struktur angegeben ist.                                  |
| CFullPropSpec                | Enthält eine Eigenschaftenspezifikation.                                                                                     |
| CContentRestriction          | Enthält eine Zeichenfolge, die mit einem Eigenschaftswert im Eigenschaftencache übereinstimmen soll.                                                 |
| CKey                         | Enthält einen Eigenschaftswert.                                                                                             |
| CInternalPropertyRestriction | Enthält einen Eigenschaftswert, der mit einem Vorgang übereinstimmen soll.                                                                  |
| CNatLanguageRestriction      | Enthält eine Abfrage in natürlicher Sprache für eine Eigenschaft.                                                                |
| CNodeRestriction             | Enthält ein Array von Befehlsstrukturknoten, die die Einschränkungen für eine Abfrage angeben.                                       |
| COccRestriction              | Enthält die Position eines Worts in einem Ausdruck.                                                                           |
| CPropertyRestriction         | Enthält einen Eigenschaftswert, der mit einem Vorgang übereinstimmen soll.                                                                  |
| CRangeRestriction            | Enthält eine Einschränkung für einen Bereich von Werten.                                                                           |
| CScopeRestriction            | Enthält eine Einschränkung für die zu durchsuchenden Dateien.                                                                    |
| CSort                        | Identifiziert eine zu sortierende Spalte.                                                                                           |
| CSynRestriction              | Enthält ein Wort oder seine Synonyme für einen Abfrageaussatz.                                                                    |
| CVectorRestriction           | Enthält einen gewichteten OR-Vorgang auf einem Befehlsstrukturknoten.                                                               |
| CWordRestriction             | Enthält ein Wort für einen Abfrageaussatz.                                                                                    |
| CRestriction                 | Enthält einen Knoten einer Abfragebefehlsstruktur.                                                                               |
| CColumnSet                   | Gibt die Anzahl der zurückgibtden Spalten an.                                                                             |
| CCategorizationSet           | Enthält Informationen zum Gruppieren eines Sets von Abfrageergebnissen.                                                     |
| CCategorizationSpec          | Enthält eine Definition von Kategorien, in die Abfrageergebnisse kategorisiert werden.                                      |
| CDbColId                     | Enthält eine Spalte.                                                                                                     |
| CDbProp                      | Enthält eine -Eigenschaft.                                                                                                   |
| CDbPropSet                   | Enthält einen Satz von Eigenschaften.                                                                                          |
| CPidMapper                   | Enthält ein Array von Eigenschaften-IDs, die die Eigenschaften angeben, die in einem Rowset zurückgegeben werden sollen.                                     |
| CRowSeekAt                   | Enthält den Offset, an dem Zeilen in einer CPMGetRowsIn-Nachricht abgerufen werden sollen.                                                |
| CRowSeekAtRatio              | Identifiziert den Punkt, an dem der Abruf für eine CPMGetRowsIn-Nachricht beginnen soll.                                           |
| CRowSeekByBookmark           | Identifiziert die Lesezeichen, aus denen Zeilen für eine CPMGetRowsIn-Nachricht abgerufen werden sollen.                                       |
| CRowSeekNext                 | Enthält die Anzahl der Zeilen, die in einer CPMGetRowsIn-Nachricht übersprungen werden sollen.                                                         |
| CRowsetProperties            | Enthält die Konfigurationsinformationen für eine Abfrage.                                                                    |
| CSortSet                     | Enthält die Sortierreihenfolge für eine Abfrage.                                                                                   |
| CTableColumn                 | Enthält eine Spalte für die CPMSetBindings-Nachricht.                                                                      |
| SERIALIZEDPROPERTYVALUE      | Enthält einen serialisierten Wert.                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a>2.2.1.1 CBaseStorageVariant

Die CBaseStorageVariant-Struktur enthält den Wert, für den ein Übereinstimmungsvorgang für eine Eigenschaft durchgeführt werden soll, die in der CPropertyRestriction-Struktur angegeben ist.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vType

vData1

vData2

vValue (Variable)



 

**vType:** Ein Typindikator, der den Typ von vValue angibt. Es MUSS einer der in der folgenden Tabelle angegebenen VARENUM-Werte sein.



| Wert                 | Bedeutung                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ EMPTY (0x0000)    | vValue ist nicht vorhanden.                                                                                                               |
| VT \_ NULL (0x0001)     | vValue ist nicht vorhanden.                                                                                                               |
| VT \_ I1 (0x0010)       | Eine 1-Byte-Ganzzahl mit Vorzeichen.                                                                                                             |
| VT \_ UI1 (0x0011)      | Eine 1-Byte-Ganzzahl ohne Vorzeichen.                                                                                                           |
| VT \_ I2 (0x0002)       | Eine 2-Byte-Ganzzahl mit Vorzeichen.                                                                                                             |
| VT \_ UI2 (0x0012)      | Eine 2-Byte-Ganzzahl ohne Vorzeichen.                                                                                                           |
| VT \_ BOOL (0x000B)     | Ein boolescher Wert; eine 2-Byte-Ganzzahl, die 0x0000 (FALSE) oder 0xFFFF (TRUE) enthält.                                                        |
| VT \_ I4 (0x0003)       | Eine 4-Byte-Ganzzahl mit Vorzeichen.                                                                                                             |
| VT \_ UI4 (0x0013)      | Eine 4-Byte-Ganzzahl ohne Vorzeichen.                                                                                                           |
| VT \_ R4 (0x0004)       | Eine IEEE 32-Bit-Gleitkommazahl, wie in \[ IEEE754 \] definiert.                                                                     |
| VT \_ INT (0x0016)      | Eine 4-Byte-Ganzzahl mit Vorzeichen.                                                                                                             |
| VT \_ UINT (0x0017)     | Eine 4-Byte-Ganzzahl ohne Vorzeichen.                                                                                                           |
| \_VT-FEHLER (0x000A)    | Eine 4-Byte-Ganzzahl ohne Vorzeichen, die ein HRESULT enthält, wie in \[ MS-SYS \] angegeben.                                                         |
| VT \_ I8 (0x0014)       | Eine 8-Byte-Ganzzahl mit Vorzeichen.                                                                                                            |
| VT \_ UI8 (0x0015)      | Eine 8-Byte-Ganzzahl ohne Vorzeichen.                                                                                                          |
| VT \_ R8 (0x0005)       | Eine IEEE-64-Bit-Gleitkommazahl gemäß definition in \[ IEEE754 \] .                                                                      |
| VT \_ CY (0x0006)       | Eine 8-Byte-Ganzzahl mit zwei Komplementen (um 10.000 skaliert).                                                                               |
| VT \_ DATE (0x0007)     | Eine 64-Bit-Gleitkommazahl, die die Anzahl der Tage seit 00:00:00 Uhr am 31. Dezember 1899 (koordinierte Weltzeit) darstellt.     |
| VT \_ FILETIME (0x0040) | Eine 64-Bit-Ganzzahl, die die Anzahl der Intervalle von 100 Nanosekunden seit 00:00:00 Uhr am 1. Januar 1601 (koordinierte Weltzeit) darstellt. |
| VT \_ DECIMAL (0x000E)  | Eine DECIMAL-Struktur, wie in Abschnitt 2.2.1.1.1.1 angegeben.                                                                             |
| VT \_ CLSID (0x0048)    | Ein 16-Byte-Binärwert, der eine GUID enthält.                                                                                            |
| \_VT-BLOB (0x0041)     | Eine 4-Byte-ganzzahlige Anzahl von Bytes ohne Vorzeichen im Blob, gefolgt von dieser Anzahl von Datenbytes.                                           |
| VT \_ BSTR (0x0008)     | Eine 4-Byte-Ganzzahlanzahl ohne Vorzeichen in der Zeichenfolge, gefolgt von einer Zeichenfolge, wie unten unter vValue angegeben.                       |
| VT \_ LPSTR (0x001E)    | Eine AUF NULL beendete ANSI-Zeichenfolge.                                                                                                       |
| VT \_ LPWSTR (0x001F)   | Eine unicode-Unicode-Zeichenfolge mit \[ \] NULL-Terminierung.                                                                                        |
| VT \_ VARIANT (0x000C)  | CBaseStorageVariant. MUSS mit einem Typmodifizierer von VT \_ ARRAY oder VT VECTOR kombiniert \_ werden.                                               |



 

In der folgenden Tabelle werden die Typmodifizierer für vType angegeben. Typmodifizierer können binäres ORed mit vType sein, um die Bedeutung von vValue zu ändern und anzugeben, dass es sich um einen von zwei möglichen Arraytypen handelt.



| Wert               | Bedeutung                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ VECTOR (0x1000) | Wenn der Typindikator mithilfe eines OR-Operators mit VT VECTOR kombiniert wird, ist vValue ein gezähltes Array von Werten \_ des angegebenen Typs. Weitere Informationen finden Sie in Abschnitt 2.2.1.1.1.2. <br/> Dieser Typmodifizierer DARF NICHT mit den folgenden Typen kombiniert werden: VT \_ INT, VT \_ UINT, VT \_ DECIMAL, VT \_ BLOB, VT \_ BLOB \_ OBJECT.<br/>                                    |
| VT \_ ARRAY (0x2000)  | Wenn der Typindikator durch einen OR-Operator mit VT ARRAY kombiniert wird, ist der Wert ein \_ SAFEARRAY (wie in Abschnitt 2.2.1.1.1.3 angegeben), das Werte des angegebenen Typs enthält. <br/> Dieser Typmodifizierer DARF NICHT mit den folgenden Typen kombiniert werden: VT \_ I8, VT \_ UI8, VT \_ FILETIME, VT \_ CLSID, VT \_ BLOB, VT \_ BLOB \_ OBJECT, VT \_ LPSTR, VT \_ LPWSTR. <br/> |



 

**vData1:** Wenn vType VT DECIMAL ist, wird der Wert dieses Felds als Scale-Feld in Abschnitt \_ 2.2.1.1.1.1 angegeben. Für alle anderen vTypes MUSS der Wert auf 0x00.

**vData2:** Wenn vType VT DECIMAL ist, wird der Wert dieses Felds im Abschnitt \_ 2.2.1.1.1.1.1 als Feld Sign angegeben. Für alle anderen vTypes MUSS der Wert auf 0x00.

**vValue:** Der Wert für den Ab übereinstimmungsvorgang. Die Syntax MUSS wie im vType-Feld angegeben sein.

In der folgenden Tabelle sind die Größen für das vValue-Feld zusammengefasst, abhängig vom vType-Feld für Datentypen fester Länge. Die Größe ist in Bytes.



| vType                                                   | Size |
|---------------------------------------------------------|------|
| VT \_ I1, VT, \_ UI1                                        | 1    |
| VT \_ I2, VT \_ UI2, VT \_ BOOL                               | 2    |
| VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ INT, VT \_ UINT, VT \_ ERROR   | 4    |
| VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ DATE, VT \_ FILETIME | 8    |
| VT \_ DECIMAL, VT \_ CLSID                                  | 16   |



 

Wenn vType auf VT BLOB, VT BSTR oder VT LPSTR festgelegt ist, wird die Struktur von \_ \_ \_ vValue im folgenden Diagramm angegeben:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cbSize

blobData (Variable, optional)



 

**cbSize:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des blobData-Felds in Bytes angibt. Wenn vType auf VT BSTR oder VT LPSTR festgelegt ist, MUSS cbSize auf 0x00000000 festgelegt werden, wenn die dargestellte Zeichenfolge eine \_ \_ leere Zeichenfolge ist.

**blobData:** MUSS die Länge cbSize in Bytes haben.

Für vType, das auf VT BLOB festgelegt ist, handelt es sich bei \_ diesem Feld um nicht transparente binäre Blobdaten.

Für vType, der auf VT BSTR festgelegt ist, ist dieses Feld ein Zeichensatz \_ in einem oem-ausgewählten Zeichensatz. Client und Server MÜSSEN so konfiguriert sein, dass sie interoperable Zeichensätze (Out-of-Band des Protokolls) haben. Es ist nicht erforderlich, dass sie auf NULL beendet wird.

Für vType, das auf VT LPSTR festgelegt ist, ist dieses Feld eine auf NULL terminierte Zeichenfolge in einem \_ oem-ausgewählten Zeichensatz. Client und Server MÜSSEN so konfiguriert sein, dass sie interoperable Zeichensätze (Out-of-Band des Protokolls) haben.

Wenn vType auf VT LPWSTR festgelegt ist, wird die Struktur von \_ vValue im folgenden Diagramm angegeben:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

ccLen

string (variable, optional)



 

**ccLen:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des Zeichenfolgenfelds in Unicode-Zeichen angibt. MUSS für eine leere Zeichenfolge auf 0x00000000 festgelegt werden.

**string:** Mit NULL beendete Unicode-Zeichenfolge.

### <a name="22111-cbasestoragevariant-structures"></a>2.2.1.1.1 CBaseStorageVariant-Strukturen

Die folgenden Strukturen werden in der CBaseStorageVariant-Struktur verwendet.

### <a name="221111-decimal"></a>2.2.1.1.1.1 DECIMAL

DECIMAL wird verwendet, um einen genauen numerischen Wert mit fester Genauigkeit und fester Dezimalstellenzahl zu darstellen.

Wenn vType auf VT DECIMAL (0x0000E) festgelegt ist, müssen die Felder \_ vData1 und vData2 von CBaseStorageVariant wie folgt interpretiert werden:

**vData1:** Die Anzahl der Ziffern rechts vom Dezimaltrennzeichen. MUSS im Bereich von 0 bis 28 liegen.

**vData2:** Das Vorzeichen des numerischen Werts. Legen Sie auf 0x00, wenn positiv, 0x80, wenn negativ.

Das Format des vValue-Felds lautet:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Hi32

Lo32

Mitte 32



 

**Hi32**: Die höchsten 32 Bits der 96-Bit-Ganzzahl.

**Lo32:** Die niedrigsten 32 Bits der 96-Bit-Ganzzahl.

**Mid32:** Die mittleren 32 Bits der 96-Bit-Ganzzahl.

### <a name="221112-vt_vector"></a>2.2.1.1.1.2 VT \_ VECTOR

VT \_ Vector wird verwendet, um eindimensionale Arrays zu übergeben.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vVectorElements

vVectorData



 

**vVectorElements:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im Feld vVectorData angibt.

**vVectorData:** Ein Array von Elementen, deren Typ durch vType mit dem 0x1000 bit cleared angegeben wird. Die Größe eines einzelnen Elements mit fester Länge kann aus der Tabelle des Datentyps fester Länge abgerufen werden, wie in Abschnitt 2.2.1.1 angegeben. Die Länge dieses Felds in Bytes kann berechnet werden, indem vVectorElements mit der Größe des einzelnen Elements multipliziert wird.

Für Datentypen variabler Länge enthält vVectorData eine Sequenz von aufeinander folgenden gemarshallten einfachen Typen, wobei der Typ durch vType angegeben wird, wobei das 0x1000 Bit gelöscht ist. Dies schließt einen Sonderfall ein, der durch vType VT \_ ARRAY \| VT \_ VARIANT (d.h. 0x100C) angegeben wird.

Die Elemente im vVectorData-Feld MÜSSEN durch 0 bis 3 Auffüllungsbytes getrennt werden, sodass jedes Element bei einem Offset beginnt, der ein Vielfaches von 4 Bytes vom Anfang der Nachricht ist, die dieses Array enthält. Wenn auffüllende Bytes vorhanden sind, ist der darin enthaltene Wert willkürlich. Der Inhalt der Auffüllungsbytes MUSS vom Empfänger ignoriert werden.

Für einen vType, der auf VT ARRAY VT VARIANT festgelegt \_ \| \_ ist, ist der Typ für Elemente in dieser Sequenz CBaseStorageVariant.

### <a name="221113-safearray"></a>2.2.1.1.1.3 SAFEARRAY

SAFEARRAY wird verwendet, um mehrdimensionale Arrays zu übergeben. Die -Struktur enthält Informationen zur Arraygröße sowie die Daten im Array.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cDims

fFeatures

cbElements

Rgsabound (Variable)

vData (Variable)



 

**cDims:** 16-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dimensionen des mehrdimensionalen Arrays angibt.

**fFeatures:** Ein 16-Bit-Bitfeld. Die Werte stellen Features dar, die von Anwendungen der oberen Ebene definiert werden und IGNORIERT WERDEN MÜSSEN.

**cbElements:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der einzelnen Elemente des Arrays angibt.

**Rgsabound:** Ein Array, das eine SAFEARRAYBOUND-Struktur enthält, wie in Abschnitt 2.2.1.1.1.4 angegeben, pro Dimension im SAFEARRAY. Dieses Array hat zuerst die linke dimension und die rechteste Dimension die letzte Dimension.

**vData:** Ein Vektor gemarshallter Elemente eines bestimmten Typs, der durch den vType des enthaltenden CBaseStorageVariant angegeben wird, wobei das Bit gelöscht 0x2000.

vData wird ähnlich wie VT VECTOR gemarshallt, \_ wie in Abschnitt 2.2.1.1.1.2 angegeben, mit dem Unterschied, dass die Anzahl der Elemente nicht vor dem Vektor gespeichert wird. Stattdessen wird die Anzahl der Elemente berechnet, indem der cElements-Wert mit allen sicheren Arraygrenzen multipliziert wird, die im Feld Rgsabound angegeben sind. Elemente werden in einem Vektor in der Reihenfolge der Dimensionen gespeichert, wobei sie beginnend mit der rechten Dimension iterieren.

Das folgende Diagramm stellt ein zweidimensionales Beispielarray visuell dar. Die erste Dimension hat cElements gleich 4 (horizontal dargestellt) und lLbound gleich 0, und die zweite Dimension weist cElements gleich 2 (vertikal dargestellt) und lLbound gleich 0 auf.

:::row:::
    :::column:::
        0x00000001
    :::column-end:::
    :::column:::
        0x00000002
    :::column-end:::
    :::column:::
        0x00000003
    :::column-end:::
    :::column:::
        0x00000005
    :::column-end:::
:::row-end:::

::row:::
    :::column:::
        0x00000007
    :::column-end:::
    :::column:::
        0x00000011
    :::column-end:::
    :::column:::
        0x00000013
    :::column-end:::
    :::column:::
        0x00000017
    :::column-end:::
:::row-end:::

Mithilfe des obigen Diagramms enthält vData die folgende Sequenz: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (durchlaufen Sie zuerst die äußerste rechte Dimension, und erhöhen Sie dann die nächste Dimension). Die vorangehende Rgsabound-Klasse (die cElements und Lbound aufzeichnet) wäre: 0x00000004, 0x00000000, 0x00000002, 0x00000000.

### <a name="221114-safearraybound"></a>2.2.1.1.1.4 SAFEARRAYBOUND

Die SAFEARRAYBOUND-Struktur stellt die Grenzen einer Dimension eines SAFEARRAY- oder SAFEARRAY2-Geräts dar. Das Format lautet:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cElements

lLbound



 

**cElements:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente in der Dimension angibt.

**lLbound:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die untere Grenze der Dimension angibt.

### <a name="221115-safearray2"></a>2.2.1.1.1.5 SAFEARRAY2

SAFEARRAY2 wird verwendet, um mehrdimensionale Arrays in SERIALIZEDPROPERTYVALUE zu übergeben. Die -Struktur enthält Sowohl Begrenzungsinformationen als auch die Daten.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cDims

Rgsabound (Variable)

vData (Variable)



 

**cDims:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dimensionen von SAFEARRAY2 angibt.

**Rgsabound:** Ein Array, das eine SAFEARRAYBOUND-Struktur enthält, wie in Abschnitt 2.2.1.1.1.4 pro Dimension in SAFEARRAY2 angegeben. Dieses Array weist zuerst die äußerste linke dimension und zuletzt die rechte Dimension auf.

**vData:** Ein Vektor gemarshallter Elemente eines bestimmten Typs, der durch den dwType des enthaltenden SERIALIZEDPROPERTYVALUE angegeben wird, wobei bit 0x2000 gelöscht wird. Das Format von vData entspricht dem Format, das für das vData-Feld von SAFEARRAY in Abschnitt 2.2.1.1.1.3 angegeben wurde.

### <a name="2212-cfullpropspec"></a>2.2.1.2 CFullPropSpec

Die CFullPropSpec-Struktur enthält eine Eigenschaftensatz-GUID und einen Eigenschaftenbezeichner, um die Eigenschaft eindeutig zu identifizieren.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_guidPropSet

...

...

...

ulKind

PrSpec

Eigenschaftenname (Variable)



 

**\_ guidPropSet:** Die GUID des Eigenschaftensatzes, zu dem die Eigenschaft gehört.

**ulKind:** Eine 32-Bit-Ganzzahl ohne Vorzeichen. Einer der folgenden Werte unten, der den Inhalt von PrSpec angibt.



| Wert                                            | Bedeutung                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| PRSPEC \_ LPWSTR<br/> 0x00000000<br/> | Das PrSpec-Feld gibt die Anzahl der Nicht-NULL-Zeichen im Feld Eigenschaftenname an. |
| PRSPEC \_ PROPID<br/> 0x00000001<br/>  | Das PrSpec-Feld gibt die Eigenschaften-ID (PROPID) an.                                     |



 

**PrSpec:** Eine 32-Bit-Ganzzahl ohne Vorzeichen mit einer Bedeutung, die durch das ulKind-Feld angegeben wird.

**Eigenschaftenname:** Wenn ulKind auf PRSPEC PROPID festgelegt \_ ist, DARF dieses Feld NICHT vorhanden sein. Wenn ulKind auf PRSPEC LPWSTR festgelegt ist, MUSS dieses Feld ein Array von Unicode-Zeichen enthalten, bei denen die \_ Groß-/Kleinschreibung nicht beachtet wird und das den Namen der Eigenschaft enthält.

### <a name="2213-ccontentrestriction"></a>2.2.1.3 CContentRestriction

Die CContentRestriction-Struktur enthält eine Zeichenfolge, die mit einer Eigenschaft im Eigenschaftencache übereinstimmt.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Eigenschaft (Variable)

...

Padding1 (Variable)

Cc

\_pwcsPhrase (Variable)

...

Padding2 (Variable)

lcid

\_ulGenerateMethod



 

**\_ Property:** Eine CFullPropSpec-Struktur, wie in Abschnitt 2.2.1.2 angegeben. Dieses Feld gibt die Eigenschaft an, für die ein Übereinstimmungsvorgang durchgeführt werden soll.

**Padding1:** Dieses Feld MUSS 0 bis 3 Byte lang sein. Die Länge dieses Felds MUSS so lang sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Byte ab dem Anfang der Nachricht ist, die diese Struktur enthält. Wenn dieses Feld vorhanden ist (d. h. länge ungleich null), ist der enthaltene Wert willkürlich. Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.

**Cc:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeichen im \_ Feld pwcsPhrase angibt.

**\_ pwcsPhrase:** Eine unicode-Zeichenfolge ohne NULL-Terminierung, die das Wort oder den Ausdruck darstellt, das bzw. der mit der Eigenschaft übereinstimmen soll. Dieses Feld DARF NICHT leer sein. Das Feld Cc enthält die Länge der Zeichenfolge.

**Padding2:** Dieses Feld MUSS 0 bis 3 Byte lang sein. Die Länge dieses Felds MUSS so lang sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Byte ab dem Anfang der Nachricht ist, die diese Struktur enthält. Wenn dieses Feld vorhanden ist (d. h. länge ungleich null), ist der enthaltene Wert willkürlich. Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.

**Lcid:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Locale von \_ pwcsPhrase angibt, wie in \[ MS-GPSI \] Anhang A angegeben.

**\_ ulGenerateMethod:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Methode angibt, die beim Generieren alternativer Wortformen verwendet werden soll.



| Wert                                                       | Bedeutung                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GENERATE \_ METHOD \_ EXACT<br/> 0x00000000<br/>    | Genaue Übereinstimmung.                                                                                                                                                                                                                                                                                      |
| \_METHODENPRÄFIX \_ GENERIEREN<br/> 0x00000001 <br/>  | Präfix-Übereinstimmung.                                                                                                                                                                                                                                                                                     |
| GENERATE \_ METHOD \_ INFLECT <br/> 0x00000002<br/> | Entspricht den Inflectionen eines Worts. Eine Inflection eines Worts ist eine Variante des Stammworts im gleichen Sprachteil, der gemäß linguistischen Regeln einer bestimmten Sprache geändert wurde. Beispiele für die Inflectionen des Verbs "swim" auf Englisch sind "swim", "swims", "swam" und "swam". |



 

### <a name="2214-ckey"></a>2.2.1.4 CKey

Die CKey-Struktur enthält einen Eigenschaftswert.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

PROPID

Cb

buf (Variable)



 

**PROPID:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Eigenschaften-ID darstellt, wie in Abschnitt 1.8.1 erläutert. Bekannte Werte sind:



| Wert      | Bedeutung                                                 |
|------------|---------------------------------------------------------|
| 0xFFFFFFFF | Stellt eine ungültige Eigenschaften-ID dar und DARF NICHT verwendet werden. |
| 0xFFFFFFFE | Stellt eine ungültige Eigenschaften-ID dar und DARF NICHT verwendet werden. |
| 0x00000000 | Stellt eine beliebige Eigenschaften-ID dar.                             |



 

**Cb:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge von buf in Bytes enthält.

**buf:** Eine Bytesequenz, die den Wert der Eigenschaft darstellt.

### <a name="2215-cinternalpropertyrestriction"></a>2.2.1.5 CInternalPropertyRestriction

Die CInternalPropertyRestriction-Struktur enthält einen Eigenschaftswert, der mit einem Vorgang übereinstimmt.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_relop

\_Pid

\_prval (Variable)

restrictionPresent

nextRestriction (Variable)



 

**\_ relop**: Eine 32-Bit-Ganzzahl, die die Beziehung angibt, die für die -Eigenschaft ausgeführt werden soll. MUSS einer der folgenden Werte sein:



| Wert                 | Bedeutung                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| PRLT-0x00000000       | Ein Kleiner-als-Vergleich.                                                                                           |
| PRLE-0x00000001       | Ein Kleiner-als- oder Gleich-Vergleich.                                                                               |
| PRGT-0x00000002       | Ein Größer-als-Vergleich.                                                                                        |
| PRGE-0x00000003       | Ein Größer-als- oder Gleich-Vergleich.                                                                            |
| PREQ 0x00000004       | Ein Gleichheitsvergleich.                                                                                           |
| PRNE-0x00000005       | Ein ungleicher Vergleich.                                                                                           |
| PRRE-0x00000006       | Ein Vergleich eines regulären Ausdrucks.                                                                                  |
| PRAllBits 0x00000007  | Ein bitweises AND, das den rechten Operanden zurückgibt.                                                                     |
| PRSomeBits-0x00000008 | Ein bitweises AND, das einen Wert ungleich 0 (null) zurückgibt.                                                                       |
| PRAll 0x00000100      | Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden und ist nur true, wenn der Vorgang für alle Zeilen true ist. |
| PRAny-0x00000200      | Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden, und ist true, wenn der Vorgang für eine Zeile true ist.       |



 

**\_ pid:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Eigenschaften-ID darstellt (siehe PROPID in Abschnitt 2.2.1.4).

**\_ prval:** Ein CBaseStorageVariant, das den Wert enthält, der mit der -Eigenschaft in Beziehung stehen soll.

**restrictionPresent:** Ein Bytewert, der angibt, ob das nextRestriction-Feld vorhanden ist. MUSS entweder auf 0x00 oder 0x01 festgelegt werden. Wenn sie auf 0x01 festgelegt ist, gibt restrictionPresent an, dass das Feld nextRestriction vorhanden ist. Wenn sie auf 0x00 festgelegt ist, gibt restrictionPresent an, dass das Feld nextRestriction nicht vorhanden ist.

**nextRestriction:** Eine CRestriction-Struktur, wie in Abschnitt 2.2.1.16 angegeben, die eine weitere Einschränkung angibt.

### <a name="2216-cnatlanguagerestriction"></a>2.2.1.6 CNatLanguageRestriction

Die CNatLanguageRestriction-Struktur enthält eine Abfrageübersprechung in **natürlicher Sprache** für eine Eigenschaft.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Eigenschaft (Variable)

...

\_Auf padding \_ cc (variable)

Cc

\_pwcsPhrase (Variable)

...

\_Auf padding \_ lcid (variable)

Lcid



 

**\_ Property:** Eine CFullPropSpec-Struktur, wie in Abschnitt 2.2.1.3 angegeben. Dieses Feld gibt die Eigenschaft an, für die der Ab übereinstimmungsvorgang durchgeführt werden soll.

**\_ padding \_ cc:** Dieses Feld MUSS 0 bis 3 Bytes lang sein. Die Länge dieses Felds MUSS so lang sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Byte ab dem Anfang der Nachricht ist, die diese Struktur enthält. Wenn dieses Feld vorhanden ist (d. h. länge ungleich null), ist der enthaltene Wert willkürlich. Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.

**Cc:** Eine 32-Bit-Ganzzahl ohne Vorzeichen. Die Anzahl der Zeichen im \_ Feld pwcsPhrase.

**\_ pwcsPhrase:** Eine unicode-Zeichenfolge ohne NULL-Terminierung, die das Wort oder den Ausdruck darstellt, das bzw. der mit der Eigenschaft übereinstimmen soll. DARF NICHT leer sein. Das Feld Cc enthält die Länge der Zeichenfolge.

**\_ padding \_ lcid**: Dieses Feld MUSS 0 bis 3 Bytes lang sein. Die Länge dieses Felds MUSS so lang sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Byte ab dem Anfang der Nachricht ist, die diese Struktur enthält. Wenn dieses Feld vorhanden ist (d. h. länge ungleich null), ist der enthaltene Wert willkürlich. Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.

**Lcid:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Locale von \_ pwcsPhrase angibt, wie in \[ MS-GPSI \] Anhang A angegeben.

### <a name="2217-cnoderestriction"></a>2.2.1.7 CNodeRestriction

Die CNodeRestriction-Struktur enthält ein Array von **Befehlsstrukturknoten,** die die Einschränkungen für die Abfrage angeben.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cNode

\_paNode (Variable)



 

**\_ cNode:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der im PaNode-Feld enthaltenen CRestriction-Strukturen \_ angibt.

**\_ paNode:** Ein Array von CRestriction-Strukturen. Strukturen im Array MÜSSEN durch 0 bis 3 Auf abstandsbytes getrennt werden, damit jede Struktur an einem Offset beginnt, der ein Vielfaches von 4 Bytes vom Anfang der Nachricht ist, die dieses Array enthält. Wenn Auf padding bytes vorhanden sind, ist der Wert, den sie enthalten, willkürlich. Der Inhalt der Auf padding-Bytes MUSS vom Empfänger ignoriert werden.

### <a name="2218-coccrestriction"></a>2.2.1.8 COccRestriction

Die COccRestriction-Struktur enthält die Position eines Worts in einem Ausdruck.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Occ

\_cPrevNoiseWords

\_cNextNoiseWords



 

**\_ occ:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Offset des Worts in einer Abfragezeichenfolge in Worteinheiten angibt. Ein Wort, wie es in dieser Spezifikation verwendet wird, ist eine Spracheinheit in jedem Beliebigen, das eine Bedeutung hat.

**\_ cPrevNoiseWords:** Eine 32-Bit-Ganzzahl ohne  Vorzeichen, die die Anzahl der Rauschwörter enthält, die zwischen diesem Wort und dem vorherigen Wort im Ausdruck auftreten.

**\_ cNextNoiseWords:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Rauschwörter enthält, die zwischen diesem Wort und dem nächsten Wort im Ausdruck auftreten.

### <a name="2219-cpropertyrestriction"></a>2.2.1.9 CPropertyRestriction

Die CPropertyRestriction-Struktur enthält einen Eigenschaftswert, der mit einem Vorgang übereinstimmen soll.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_relop

\_Eigenschaft (Variable)

\_prval (Variable)



 

**\_ relop:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Beziehung angibt, die für die -Eigenschaft verwendet werden soll. MUSS einer der folgenden Werte sein.



| Wert                 | Bedeutung                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| PRLT-0x00000000       | Ein Kleiner-als-Vergleich.                                                                                           |
| PRLE-0x00000001       | Ein Kleiner-als- oder gleich-Vergleich.                                                                               |
| PRGT-0x00000002       | Ein Größer-als-Vergleich.                                                                                        |
| PRGE-0x00000003       | Ein Größer-als- oder gleich-Vergleich.                                                                            |
| PREQ-0x00000004       | Ein Gleichheitsvergleich.                                                                                           |
| PRNE-0x00000005       | Ein nicht gleicher Vergleich.                                                                                           |
| PRRE-0x00000006       | Ein Vergleich mit regulären Ausdrücken.                                                                                  |
| PRAllBits 0x00000007  | Ein bitweises AND, das den rechten Operanden zurückgibt.                                                                     |
| PRSomeBits 0x00000008 | Ein bitweises AND, das einen Wert ungleich 0 (null) zurückgibt.                                                                       |
| PRAll 0x00000100      | Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden und ist nur true, wenn der Vorgang für alle Zeilen true ist. |
| PRAny-0x00000200      | Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden, und ist TRUE, wenn der Vorgang für eine zeile true ist.       |



 

**\_ Eigenschaft:** Eine CFullPropSpec-Struktur, wie in Abschnitt 2.2.1.2 angegeben, die die Eigenschaft angibt, für die ein Übereinstimmungsvorgang durchgeführt werden soll.

**\_ prval:** Eine CBaseStorageVariant-Struktur, wie in Abschnitt 2.2.1.1 angegeben, die den Wert enthält, der mit der Eigenschaft in Beziehung stehen soll.

### <a name="22110-crangerestriction"></a>2.2.1.10 CRangeRestriction

Die CRangeRestriction-Struktur enthält eine Einschränkung für einen Bereich von Werten.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_keyStart (Variable)

\_keyEnd (Variable)



 

**\_ keyStart:** Eine CKey-Struktur, wie in Abschnitt 2.2.1.4 angegeben, die den Anfang des Bereichs enthält.

**\_ keyEnd:** Eine CKey-Struktur, die das Ende des Bereichs enthält.

### <a name="22111-cscoperestriction"></a>2.2.1.11 CScopeRestriction

Die CScopeRestriction-Struktur enthält eine Einschränkung für die zu durchsuchenden Dateien.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CcLowerPath

\_lowerPath (Variable)

...

\_Padding (Variable)

\_Länge

\_fRecursive

\_fVirtuelle



 

**CcLowerPath:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von Unicode-Zeichen im \_ feld lowerPath enthält.

**\_ lowerPath:** Eine unicode-Zeichenfolge ohne  NULL-Terminierung, die den Pfad darstellt, auf den die Abfrage eingeschränkt werden soll. Das Feld CcLowerPath enthält die Länge der Zeichenfolge.

**\_ Padding**: Dieses Feld MUSS 0 bis 3 Byte lang sein. Die Länge dieses Felds MUSS so lang sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Byte ab dem Anfang der Nachricht ist, die diese Struktur enthält. Wenn dieses Feld vorhanden ist (d. h. länge ungleich null), ist der enthaltene Wert willkürlich. Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.

**\_ length:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge \_ von lowerPath in Unicode-Zeichen enthält. Dies MUSS der gleiche Wert wie CcLowerPath sein.

**\_ fRecursive:** Eine 32-Bit-Ganzzahl ohne Vorzeichen. MUSS auf 0x00000001 oder 0x00000000. Wenn auf 0x00000001 festgelegt ist, überprüft der Server rekursiv alle Unterverzeichnisse des Pfads. Wenn auf 0x00000000 festgelegt ist, überprüft der Server keine Unterverzeichnisse.

**\_ fVirtual:** Eine 32-Bit-Ganzzahl ohne Vorzeichen. MUSS auf 0x00000001 oder 0x00000000. Wenn diese 0x00000001, ist lowerPath ein virtueller Pfad (der Uniform Resource Locator (URL), der einem physischen Verzeichnis im Dateisystem \_ zugeordnet ist) für eine Website. Wenn diese 0x00000000, \_ ist lowerPath ein Dateisystempfad.

### <a name="22112-csort"></a>2.2.1.12 CSort

Die CSort-Struktur identifiziert eine zu sortierende Spalte.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

pidColumn

dwOrder

locale



 

**pidColumn:** Eine 32-Bit-Ganzzahl ohne Vorzeichen. Die Nummer der Spalte, nach der sortiert werden soll.

**dwOrder:** Eine 32-Bit-Ganzzahl ohne Vorzeichen. MUSS einer der folgenden Werte sein und angeben, wie basierend auf der Spalte sortiert werden soll.



| Wert                        | Bedeutung                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| \_SORTASCEND-ABFRAGE 0x00000000 | Die Zeilen müssen basierend auf den Werten in der angegebenen Spalte in aufsteigender Reihenfolge sortiert werden.  |
| QUERY \_ DESCEND 0x00000001    | Die Zeilen müssen basierend auf den Werten in der angegebenen Spalte in absteigender Reihenfolge sortiert werden. |



 

**locale:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Im MS-GPSI Anhang A angegebene Locale \[ \] der Spalte angibt.

### <a name="22113-csynrestriction"></a>2.2.1.13 CSynRestriction

Die CSynRestriction-Struktur enthält ein Wort oder seine Synonyme für einen Abfrageaussatz.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Einschränkung

...

...

cKey

\_keyArray (Variable)

\_isRange



 

**Einschränkung:** Eine COccRestriction-Struktur, die die Position des Worts an gibt.

**cKey:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im \_ keyArray-Array angibt.

**\_ keyArray:** Ein Array von CKey-Strukturen, die ein Wort und seine Synonyme angeben.

**\_ isRange:** Wenn auf 0x01 festgelegt ist, sind die Schlüssel Präfixe, die übereinstimmen. Wenn diese 0x00 festgelegt ist, sind die Schlüssel exakte Werte, die übereinstimmen. \_isRange DARF NICHT auf andere Werte festgelegt werden.

### <a name="22114-cvectorrestriction"></a>2.2.1.14 CVectorRestriction

Die CVectorRestriction-Struktur enthält einen gewichteten OR-Vorgang auf einem Befehlsstrukturknoten.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_pres (Variable)

...

\_Auf padding (Variable)

\_ulRankMethod



 

**\_ pres:** Eine CNodeRestriction-Befehlsstruktur, für die ein or-Vorgang mit Rang angegeben werden soll.

**\_ Padding**: Dieses Feld MUSS 0 bis 3 Byte lang sein. Die Länge dieses Felds MUSS so lang sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Byte ab dem Anfang der Nachricht ist, die diese Struktur enthält. Wenn dieses Feld vorhanden ist (d. h. länge ungleich null), ist der enthaltene Wert willkürlich. Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.

**\_ ulRankMethod:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die einen Rangfolgealgorithmus angibt. MUSS auf einen der folgenden Werte festgelegt werden.



| Wert                            | Bedeutung                                       |
|----------------------------------|-----------------------------------------------|
| VECTOR \_ RANK \_ MIN 0x00000000     | Verwenden Sie den minimalen \[ SALTON-Algorithmus. \]             |
| VECTOR \_ RANK \_ MAX 0x00000001     | Verwenden Sie den maximalen \[ SALTON-Algorithmus. \]             |
| VECTOR \_ RANK \_ INNER 0X00000002   | Verwenden Sie den inneren Produktalgorithmus \[ SALTON \] .       |
| VECTOR \_ RANK \_ DICE-0x00000003    | Verwenden Sie den Dice-Koeffizientenalgorithmus \[ SALTON \] .    |
| VECTOR \_ RANK \_ JACCARD-0x00000004 | Verwenden Sie den Jaccard-Koeffizientenalgorithmus \[ SALTON \] . |



 

### <a name="22115-cwordrestriction"></a>2.2.1.15 CWordRestriction

Die CWordRestriction-Struktur enthält ein Wort für einen Abfrageaussatz.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Einschränkung

...

...

\_key (Variable)

\_isRange



 

**restriction:** Eine COccRestriction-Struktur, die die Position des Worts an gibt.

**\_ key:** Eine CKey-Struktur, die ein Wort an gibt.

**\_ isRange:** Wenn auf 0x01 festgelegt ist, ist der Schlüssel ein Präfix, das übereinstimmen soll. Wenn der Wert auf 0x00 festgelegt ist, ist der Schlüssel ein exakter Wert, der übereinstimmen soll. \_isRange DARF NICHT auf einen anderen Wert festgelegt werden.

### <a name="22116-crestriction"></a>2.2.1.16 CRestriction

Die CRestriction-Struktur enthält einen Knoten einer Abfragebefehlsstruktur.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_ulType

Weight

Einschränkung



 

**\_ ulType:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Einschränkungstyp angibt, der für den Befehlsstrukturknoten verwendet wird. MUSS auf einen der folgenden Werte festgelegt werden.



| Wert                    | Bedeutung                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| RTNone 0x00000000        | Der Knoten stellt ein Rauschwort in einer Vektorabfrage dar.                                         |
| RTAnd 0x00000001         | Der Knoten enthält eine CNodeRestriction, für die ein logischer AND-Vorgang ausgeführt werden soll. |
| RTOr-0x00000002          | Der Knoten enthält eine CNodeRestriction, für die ein logischer OR-Vorgang ausgeführt werden soll.  |
| RTNot 0x00000003         | Der Knoten enthält eine CRestriction, für die ein NOT-Vorgang ausgeführt werden soll.             |
| RTContent 0x00000004     | Der Knoten enthält eine CContentRestriction.                                                    |
| RTProperty-0x00000005    | Der Knoten enthält eine CPropertyRestriction.                                                   |
| RTProximity 0x00000006   | Der Knoten enthält eine CNodeRestriction, für die eine Näherungsrangfolge durchgeführt werden soll.     |
| RTVector-0x00000007      | Der Knoten enthält eine CVectorRestriction.                                                     |
| RTNatLanguage 0x00000008 | Der Knoten enthält eine CNatLanguageRestriction.                                                |
| RTScope 0x00000009       | Der Knoten enthält eine CScopeRestriction.                                                      |
| PRAny-0xFFFFFFFA         | Der Knoten enthält eine CInternalPropertyRestriction.                                           |
| RTRange 0xFFFFFFFC       | Der Knoten enthält eine CRangeRestriction.                                                      |
| RTPhrase-0xFFFFFFFD      | Der Knoten enthält eine CNodeRestriction, für die eine Ausdrucks match ausgeführt werden soll.          |
| RTSynonym 0xFFFFFFFE     | Der Knoten enthält eine CSynRestriction.                                                        |
| RTWord-0xFFFFFFFF        | Der Knoten enthält eine CWordRestriction.                                                       |



 

**Gewichtung:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gewichtung des Knotens darstellt. Die Gewichtung gibt die Wichtigkeit des Knotens relativ zu anderen Knoten in der Abfragebefehlsstruktur an. Höhere Gewichtungswerte sind wichtiger.

**Einschränkung:** Der Einschränkungstyp für den Befehlsstrukturknoten. Die Syntax MUSS wie durch das \_ ulType-Feld angegeben sein.

### <a name="22117-ccolumnset"></a>2.2.1.17 CColumnSet

Die CColumnSet-Struktur gibt die spaltennummern an, die zurückgegeben werden sollen. Diese Struktur wird immer als Verweis auf eine bestimmte CPidMapper-Struktur verwendet (Abschnitt 2.2.1.23).



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

count

Indizes (Variable)



 

**count:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im Indexarray angibt.

**indexes:** Array von 4-Byte-Ganzzahlen ohne Vorzeichen, die nullbasierte Indizes im aPropSpec-Array in der entsprechenden CPidMapper-Struktur darstellen.

### <a name="22118-ccategorizationset"></a>2.2.1.18 CCategorizationSet

Die CCategorizationSet-Struktur enthält Informationen über die Gruppierung eines Abfrageergebnissets.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

count

categories (variable)



 

**count:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im Categories-Array enthält.

**categories:** Array von CCategorizationSpec-Strukturen, die die Gruppierung der Abfrage angeben.

### <a name="22119-ccategorizationspec"></a>2.2.1.19 CCategorizationSpec

Die CCategorizationSpec-Struktur enthält eine Gruppierung für ein Abfrageergebnissatz.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_csColumns (Variable)

\_ulCategType



 

**\_ csColumns:** Eine CColumnSet-Struktur, die die Spalten angibt, nach denen die Abfrage gruppiert werden soll.

**\_ ulCategType:** Eine 32-Bit-Ganzzahl ohne Vorzeichen. MUSS auf "0x00000000.

### <a name="22120-cdbcolid"></a>2.2.1.20 CDbColId

Die CDbColId-Struktur enthält eine Spalte.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

eKind

GUID

...

...

...

ulId

vString (Variable)



 

**eKind:** MUSS auf einen der folgenden Werte festgelegt werden, der den Inhalt von GUID und vValue angibt.



| Wert                            | Bedeutung                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| NAME DER \_ \_ DBKIND-GUID 0x00000000    | vString enthält einen Eigenschaftennamen.                                                                               |
| \_PROPID-0x00000001 \_  | ulId enthält eine 4-Byte-Ganzzahl, die die Eigenschaften-ID angibt.                                                      |
| DBKIND \_ PGUID \_ NAME 0x00000003   | vString enthält einen Eigenschaftennamen. Dieser Wert MUSS mit DBKIND \_ GUID \_ NAME identisch sein.                    |
| DBKIND \_ PGUID \_ PROPID 0x00000004 | ulId enthält eine 4-Byte-Ganzzahl, die die Eigenschaften-ID angibt. Dieser Wert MUSS mit DBKIND \_ GUID \_ PROPID identisch sein. |



 

**GUID:** Die Eigenschaften-GUID.

**ulId:** Wenn eKind DBKIND \_ GUID PROPID oder DBKIND PGUID PROPID ist, enthält dieses Feld eine ganze Zahl ohne Vorzeichen, die die \_ \_ \_ Eigenschaften-ID angibt. Wenn eKind DBKIND GUID NAME oder DBKIND PGUID NAME ist, enthält dieses Feld eine ganze Zahl ohne Vorzeichen, die die Anzahl von Unicode-Zeichen angibt, die \_ \_ im \_ \_ vString-Feld enthalten sind.

**vString:** Eine nicht auf NULL terminierte Unicode-Zeichenfolge, die den Eigenschaftennamen darstellt. Sie MUSS weggelassen werden, es sei denn, das eKind-Feld ist auf DBKIND \_ GUID \_ NAME oder DBKIND \_ PGUID \_ NAME festgelegt.

### <a name="22121-cdbprop"></a>2.2.1.21 CDbProp

Die CDbProp-Struktur enthält eine -Eigenschaft.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

DBPROPID

DBPROPOPTIONS

DBPROPSTATUS

- (Variable)

vValue (Variable)



 

**DBPROPID:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Eigenschaften-ID angibt.

**DBPROPOPTIONS:** MUSS auf 0x00000000.

**DBPROPSTATUS:** MUSS auf 0x00000000.

**– eine** CDbColId-Struktur, wie in Abschnitt 2.2.1.20 angegeben, die die Spalte angibt, für die die Eigenschaft gilt.

**vValue:** Eine CBaseStorageVariant,die den Eigenschaftswert enthält.

### <a name="221211-properties"></a>2.2.1.21.1 Eigenschaften

In diesem Abschnitt werden die Eigenschaften beschrieben, die von CISP verwendet werden. Diese Eigenschaften werden in drei Eigenschaftensätze ident2.2.1.21.1 im Feld guidPropertySet der CDbPropSet-Struktur (Abschnitt 2.2.1.22) eingeteilt.

In der folgenden Tabelle sind die Eigenschaften aufgeführt, die Teil des DBPROPSET \_ FSCIFRMWRK \_ EXT-Eigenschaftensatz sind.



| Wert                                  | Bedeutung                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ CI CATALOG NAME \_ \_ 0x00000002   | Gibt den Namen des Katalogs oder der Kataloge an, der bzw. die abfragen werden soll. Der Wert MUSS ein VT \_ LPWSTR oder ein VT \_ VECTOR \| VT \_ LPWSTR sein.                                   |
| DBPROP \_ CI \_ INCLUDE \_ SCOPES 0x00000003 | Gibt einen oder mehrere Pfade an, die in die Abfrage eingeschlossen werden sollen. Der Wert MUSS ein VT \_ LPWSTR oder ein VT \_ VECTOR \| VT \_ LPWSTR sein.                                 |
| DBPROP \_ CI \_ SCOPE \_ FLAGS 0x00000004    | Gibt an, wie die von der DBPROP \_ CI \_ INCLUDE \_ SCOPES-Eigenschaft angegebenen Pfade behandelt werden sollen. Der Wert MUSS ein VT \_ I4 oder ein VT \_ VECTOR \| VT \_ I4 sein. |
| ABFRAGETYP \_ "DBPROP \_ \_ CI" 0x00000007     | Gibt den Typ der Abfrage an. Die CDbColId MUSS auf DB \_ NULLID festgelegt werden.                                                                               |



 

In der folgenden Tabelle sind die Flags für die DBPROP \_ CI \_ SCOPE \_ FLAGS-Eigenschaft aufgeführt:



| Wert                     | Bedeutung                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| QUERY \_ DEEP 0x01          | Wenn festgelegt, gibt an, dass Dateien im Bereichsverzeichnis und in allen Unterverzeichnissen in den Ergebnissen enthalten sind. Wenn dies klar ist, sind nur Dateien im Bereichsverzeichnis in den Ergebnissen enthalten. DARF NICHT mit QUERY DEEP kombiniert \_ werden. |
| QUERY \_ VIRTUAL \_ PATH 0x02 | Wenn festgelegt, gibt an, dass der Bereich ein virtueller Pfad ist. Wenn dies klar ist, gibt an, dass der Bereich ein physisches Verzeichnis ist.                                                                                                         |



 

In der folgenden Tabelle sind die Abfragetypen für die DBPROP \_ CI \_ QUERY \_ TYPE-Eigenschaft aufgeführt:



| Wert                     | Bedeutung                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| CiNormal 0x00000000       | Eine reguläre Abfrage.                                                                                                   |
| CiVirtualRoots-0x00000001 | Die Abfrage fordert eine Liste der virtuellen Stämme des Katalogs an. Dieser Wert erfordert Administratorrechte. |
| CiProperties-0x00000003   | Die Abfrage fordert eine Liste aller Eigenschaften an, die vom Indizierungsdienst unterstützt werden.                            |
| CiAdminOp 0x00000004      | Die Abfrage ist ein Verwaltungsvorgang. Dieser Wert erfordert Administratorrechte.                           |



 

In der folgenden Tabelle sind die Eigenschaften aufgeführt, die Teil des DBPROPSET \_ QUERYEXT-Eigenschaftensatz sind.



| Wert                                      | Bedeutung                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ USECONTENTINDEX 0x00000002         | Gibt an, wie der Indizierungsdienst langsame Abfragen verarbeiten soll. Der Wert MUSS eine \_ VT-BOOL sein. True gibt an, dass der Server für diese Abfragen einen Fehler ausführen darf.                                                                                    |
| DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003 | Gibt an, ob der Indizierungsdienst das Kürzen von Ergebnissen durchführen soll. True gibt an, dass der Server das Kürzen von Ergebnissen in einer Weise in Betracht ziehen soll, die die Antwortzeit für den Client optimiert. Der Wert MUSS eine \_ VT-BOOL sein.             |
| DBPROP \_ USEEXTENDEDDBTYPES 0x00000004      | Gibt an, ob der Client VT \_ VECTOR-Datentypen unterstützt. True gibt an, dass der Client VT VECTOR unterstützt. Bei FALSE konvertiert der Server VT VECTOR-Datentypen in \_ \_ VT \_ ARRAY-Datentypen.  Der Wert MUSS eine \_ VT-BOOL sein. |
| DBPROP \_ FIRSTROWS-0x00000007               | Gibt an, dass die Zeile entspricht, die zurückgibt. True gibt den ersten Satz übereinstimmende Zeilen zurück. False gibt an, dass die am besten übereinstimmenden Zeilen zurückgegeben werden sollen. Der Wert MUSS eine \_ VT-BOOL sein.                                             |



 

In der folgenden Tabelle sind die Eigenschaften aufgeführt, die Teil des DBPROPSET \_ CIFRMWRKCORE \_ EXT-Eigenschaftensatz sind.



| Value/DBPROPID                 | Bedeutung                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ MACHINE 0x00000002       | Gibt die Namen der Computer an, auf denen eine Abfrage verarbeitet werden soll. Der Wert MUSS entweder VT \_ BSTR oder VT \_ ARRAY \| VT \_ BSTR sein. |
| DBPROP \_ CLIENT \_ CLSID 0x00000003 | Gibt eine Verbindungskonst constant für den Indizierungsdienst an. Der Wert MUSS eine \_ VT-CLSID sein, die 0x2A4880706FD911D0A80800A0C906241A.  |



 

### <a name="22122-cdbpropset"></a>2.2.1.22 CDbPropSet

Die CDbPropSet-Struktur enthält einen Satz von Eigenschaften. Beachten Sie, dass das erste Feld eine feste Größe hat, aber möglicherweise nicht an einem Offset ausgerichtet ist, bei dem es sich um ein 4-Byte-Vielfaches vom Anfang der Nachricht handelt, die diese Struktur enthält. Das Feld cProperties ist jedoch so ausgerichtet, und daher wird das Format wie folgt dargestellt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

guidPropertySet

...

...

...

...

\_Auf padding (Variable)

cProperties

aProps (Variable)



 

**guidPropertySet:** Eine GUID, die den Eigenschaftensatz identifiziert. MUSS auf das binäre Formular festgelegt werden, das einem der folgenden Werte entspricht (in Form einer Zeichenfolgendarstellung dargestellt), die den Eigenschaftensatz der eigenschaften identifiziert, die im aProps-Feld enthalten sind.



| Wert/GUID                                                                              | Name                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| DBPROPSET \_ FSCIFRMWRK \_ EXT<br/> {A9BD1526-6A80-11D0-8C9D-0020AF1D740E}<br/>   | File System Content Index Framework-Eigenschaftensatz |
| DBPROPSET \_ QUERYEXT<br/> {A7AC77ED-F8D7-11CE-A798-0020F8008025}<br/>          | Eigenschaftensatz der Abfrageerweiterung                     |
| DBPROPSET \_ CIFRMWRKCORE \_ EXT<br/> {AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}<br/> | Content Index Framework Core-Eigenschaftensatz        |



 

**\_ Padding**: Dieses Feld MUSS 0 bis 3 Byte lang sein. Die Länge dieses Felds MUSS so lang sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Byte ab dem Anfang der Nachricht ist, die diese Struktur enthält. Wenn dieses Feld vorhanden ist (d. h. länge ungleich 0), ist der enthaltene Wert willkürlich. Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.

**cProperties:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im aProps-Array enthält.

**aProps:** Ein Array von CDbProp-Strukturen, wie in Abschnitt 0 angegeben, das Eigenschaften enthält. Strukturen im Array MÜSSEN durch 0 bis 3 Auf abstandsbytes getrennt werden, damit jede Struktur an einem Offset beginnt, der ein Vielfaches von 4 Bytes vom Anfang der Nachricht ist, die dieses Array enthält. Wenn Auf padding bytes vorhanden sind, ist der Wert, den sie enthalten, willkürlich. Der Inhalt der Auf padding-Bytes MUSS vom Empfänger ignoriert werden.

### <a name="22123-cpidmapper"></a>2.2.1.23 CPidMapper

Die CPidMapper-Struktur enthält ein Array von Eigenschaften-IDs, die die Eigenschaften angeben, die in einem Rowset zurückgegeben werden sollen.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

count

aPropSpec

... (Variable)



 

**count:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im aPropSpec-Array enthält.

**aPropSpec:** Array von CFullPropSpec-Strukturen, die die zurückzugebenden Eigenschaften angeben. Strukturen im Array MÜSSEN durch 0 bis 3 Auffüllungsbytes getrennt werden, sodass jede Struktur eine 4-Byte-Ausrichtung vom Anfang einer Nachricht aufweist. Solche Auffüllungsbytes können beliebige Werte sein, und MÜSSEN beim Empfang ignoriert werden.

### <a name="22124-crowseekat"></a>2.2.1.24 CRowSeekAt

Die CRowSeekAt-Struktur enthält den Offset, an dem Zeilen in einer CPMGetRowsIn-Nachricht abgerufen werden sollen.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hRegion

\_cskip

\_bmkOffset



 

**\_ hRegion:** MUSS auf 0x00000000 festgelegt werden, und MUSS ignoriert werden.

**\_ cskip:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeilen enthält, die im Rowset übersprungen werden sollen.

**\_ bmkOffset:** Ein 32-Bit-Wert, der das Handle des **Lesezeichens** darstellt, das die Anfangsposition angibt, von der aus die in cskip angegebene Anzahl von Zeilen übersprungen werden \_ soll, bevor mit dem Abrufen begonnen wird.

### <a name="22125-crowseekatratio"></a>2.2.1.25 CRowSeekAtRatio

Die CRowSeekAtRatio-Struktur identifiziert den Punkt, an dem mit dem Abrufen einer CPMGetRowsIn-Nachricht begonnen werden soll.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CiTblChapt

\_hRegion

\_ulNumerator

\_ulDenominator



 

**CiTblChapt:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Rowsetkapitel angibt, aus dem Zeilen abgerufen werden sollen.

**\_ hRegion:** MUSS auf 0x00000000 festgelegt werden, und MUSS ignoriert werden.

**\_ ulNumerator:** 32-Bit-Ganzzahl ohne Vorzeichen, die den Zähler des Verhältnisses der Zeilen im Kapitel darstellt, an dem mit dem Abruf begonnen werden soll.

**\_ ulDenominator:** 32-Bit-Ganzzahl ohne Vorzeichen, die den Nenner des Zeilenverhältnisses im Kapitel darstellt, an dem mit dem Abruf begonnen werden soll. MUSS größer als 0 (null) sein.

### <a name="22126-crowseekbybookmark"></a>2.2.1.26 CRowSeekByBookmark

Die CRowSeekByBookmark-Struktur identifiziert die Lesezeichen, aus denen Zeilen für eine CPMGetRowsIn-Nachricht abgerufen werden sollen.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hRegion

\_cBookmarks

\_maxRet

\_cValidRet

\_aBookmarks (Variable)

\_ascRet (Variable)



 

**\_ hRegion:** MUSS auf 0x00000000 festgelegt werden, und MUSS ignoriert werden.

**\_ cBookmarks:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im \_ aBookmarks-Array darstellt.

**\_ maxRet:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im \_ ascRet-Array darstellt.

**\_ cValidRet:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl gültiger Elemente im \_ ascRet-Array darstellt. Gültige Elemente wurden im Array definiert, während ungültige Elemente nicht definiert sind.

**\_ aBookmarks:** Ein Array von Lesezeichenhandles (jeweils durch 4 Bytes dargestellt), wie aus einer CPMGetRowsOut-Nachricht abgerufen.

**\_ ascRet:** Ein Array von HRESULT-Werten. Wenn CRowSeekByBookMark als Teil der CPMGetRowsIn-Anforderung gesendet wird, MUSS die Anzahl der Einträge im Array \_ gleich cBookMarks sein. Beim Senden durch den Client MÜSSEN die Werte auf 0 festgelegt werden, und der Server MUSS den Inhalt des Arrays ignorieren. Beim Senden durch den Server (als Teil der CPMGetRowsOut-Nachricht) geben die Werte im Array den Ergebnisstatus für jeden Zeilenabruf an.

### <a name="22127-crowseeknext"></a>2.2.1.27 CRowSeekNext

Die CRowSeekNext-Struktur enthält die Anzahl der Zeilen, die in einer CPMGetRowsIn-Nachricht übersprungen werden sollen.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CiTblChapt

\_hRegion

\_cskip



 

**CiTblChapt:** 32-Bit-Ganzzahl ohne Vorzeichen, die das Rowsetkapitel angibt, aus dem Zeilen abgerufen werden sollen.

**\_ hRegion:** MUSS auf 0x00000000 festgelegt werden, und MUSS ignoriert werden.

**\_ cskip:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeilen darstellt, die im Rowset übersprungen werden sollen.

### <a name="22128-crowsetproperties"></a>2.2.1.28 CRowsetProperties

Die CRowsetProperties-Struktur enthält Konfigurationsinformationen für eine Abfrage.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_uBooleanOptions

\_ulMaxOpenRows

\_ulMemoryUsage

\_cMaxResults

\_cCmdTimeout



 

**\_ uBooleanOptions:** Die 3 Bits dieses Felds mit der geringsten Bedeutung MÜSSEN einen der folgenden drei Werte enthalten:



| Wert                  | Bedeutung                                                             |
|------------------------|---------------------------------------------------------------------|
| eSequential 0x00000001 | Der Cursor kann nur vorwärts bewegt werden.                              |
| eLocatable 0x00000003  | Der Cursor kann an eine beliebige Position verschoben werden.                            |
| eScrollable 0x00000007 | Der Cursor kann an eine beliebige Position verschoben und in beliebiger Richtung abgerufen werden. |



 

Die verbleibenden Bits können entweder klar sein oder auf eine beliebige Kombination der folgenden Werte festgelegt werden, logisch OR'd zusammen:



| Wert                     | Bedeutung                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| eAsynchronous 0x00000008  | Der Client wartet nicht auf den Abschluss der Ausführung.                                                          |
| eFirstRows 0x00000080     | Gibt die ersten gefundenen Zeilen zurück, nicht die besten Übereinstimmungen.                                                    |
| eHoldRows 0x00000200      | Der Server DARF KEINE Zeilen verwerfen, bis der Client mit einer Abfrage fertig ist.                                     |
| eChaptered 0x00000800     | Das Rowset unterstützt Kapitel.                                                                               |
| eUseCI 0x00001000         | Beantworten Sie nur die Abfrage aus dem Index, nicht aus dem Dateisystem.                                                  |
| eDeferTrimming 0x00002000 | Der Indizierungsdienst sollte beim Entfernen von Ergebnissen die Optimierung der Antwortzeit für den Client in Betracht ziehen. |



 

**\_ ulMaxOpenRows:** 32-Bit-Ganzzahl ohne Vorzeichen. Muss auf 0x00000000 festgelegt werden. Nicht verwendet und MUSS ignoriert werden.

**\_ ulMemoryUsage:** 32-Bit-Ganzzahl ohne Vorzeichen. Muss auf 0x00000000 festgelegt werden. Nicht verwendet und MUSS ignoriert werden.

**\_ cMaxResults:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die maximale Anzahl von Zeilen angibt, die für die Abfrage zurückgegeben werden sollen.

**\_ cCmdTimeout:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Sekunden angibt, nach denen für eine Abfrage ein Timeout und ein automatisches Beenden ausgeführt werden soll. Dabei wird ab dem Zeitpunkt gezählt, zu dem die Abfrage auf dem Server ausgeführt wird. Der Wert 0x00000000 bedeutet, dass für die Abfrage kein Time out erfolgt.

### <a name="22129-crowvariant"></a>2.2.1.29 CRowVariant

Die CRowVariant-Struktur enthält den festen Größenteil eines Datentyps variabler Länge, der in der CPMGetRowsOut-Nachricht gespeichert ist.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vType

reserviert1

reserved2

Offset (optional)



 

**vType:** Ein Typindikator, der den Typ von vValue angibt. Dabei MUSS es sich um einen der in Abschnitt 2.2.1.1 angegebenen VARENUM-Werte handeln.

**reserved1:** Nicht verwendet. Der Wert kann auf einen beliebigen Wert festgelegt werden, und er MUSS beim Empfang ignoriert werden.

**reserved2:** Nicht verwendet. Der Wert kann auf einen beliebigen Wert festgelegt werden, und er MUSS beim Empfang ignoriert werden.

**Offset:** Ein Offset zu Daten variabler Länge (z. B. eine Zeichenfolge).  Dies MUSS ein 32-Bit-Wert (4 Bytes lang) sein, wenn 32-Bit-Offsets verwendet werden (gemäß den Regeln in Abschnitt 2.2.3.16) oder ein 64-Byte-Wert (8 Bytes lang), wenn 64-Bit-Offsets verwendet werden.

### <a name="22130-csortset"></a>2.2.1.30 CSortSet

Die CSortSet-Struktur enthält die Sortierreihenfolge der Abfrage.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Anzahl

sortArray (Variable)



 

**count:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente in sortArray angibt.

**sortArray:** Ein Array von CSort-Strukturen, das die Reihenfolge beschreibt, in der die Ergebnisse der Abfrage sortiert werden sollen. Strukturen im Array MÜSSEN durch 0 bis 3 Auffüllungsbytes getrennt werden, sodass jede Struktur eine 4-Byte-Ausrichtung vom Anfang einer Nachricht aufweist. Solche Auffüllungsbytes können beliebige Werte sein, und MÜSSEN beim Empfang ignoriert werden.

### <a name="22131-ctablecolumn"></a>2.2.1.31 CTableColumn

Die CTableColumn-Struktur enthält eine Spalte einer CPMSetBindingsIn-Nachricht.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

PropSpec

... (Variable)

vType

ValueUsed

\_padding1 (optional)

ValueOffset (optional)

ValueSize (optional)

StatusUsed

\_padding2 (optional)

StatusOffset (optional)

LengthUsed

\_padding3 (optional)

LengthOffset (optional)



 

**PropSpec:** Eine CFullPropSpec-Struktur gemäß Abschnitt 2.2.1.3.

**vType:** Gibt den Typ des in der Spalte enthaltenen Datenwerts an. Die Liste der Werte für dieses Feld finden Sie im Feld vType in Abschnitt 2.2.1.1.

**ValueUsed:** Ein 1-Byte-Feld, das auf 0x01 oder 0x00 festgelegt werden MUSS. Wenn 0x01 festgelegt ist, wird die Spalte innerhalb der Zeile mit fester Größe übertragen. Wenn 0x00 festgelegt ist, wird der Wert der Spalte im Abschnitt mit variabler Länge am Ende des Puffers übertragen.

**\_ padding1:** Ein 1-Byte-Feld, das vor ValueOffset eingefügt werden MUSS, wenn ValueOffset ohne dieses Feld nicht mit einem geraden Offset vom Anfang der Nachricht beginnen würde. Der Wert dieses Byte ist willkürlich und MUSS ignoriert werden. Wenn ValueUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.

**ValueOffset:** Eine 2-Byte-Ganzzahl ohne Vorzeichen, die den Offset des Spaltenwerts in der Zeile angibt. Wenn ValueUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.

**ValueSize:** Eine 2-Byte-Ganzzahl ohne Vorzeichen, die die Größe des Spaltenwerts in Bytes angibt. Wenn ValueUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.

**StatusUsed:** Ein 1-Byte-Feld, das auf 0x01 oder 0x00 festgelegt werden MUSS. Wenn 0x01 festgelegt ist, wird der Status der Spalte innerhalb der Zeile übertragen. Wenn 0x00, wird der Status der Spalte nicht innerhalb der Zeile übertragen.

**\_ padding2:** Ein 1-Byte-Feld, das vor StatusOffset eingefügt werden MUSS, wenn das Feld StatusOffset ohne dieses Feld nicht mit einem geraden Offset vom Anfang der Nachricht beginnen würde. Der Wert dieses Byte ist willkürlich und MUSS ignoriert werden. Wenn StatusUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.

**StatusOffset:** Eine 2-Byte-Ganzzahl ohne Vorzeichen, die den Offset des Spaltenstatus in der Zeile angibt. Wenn StatusUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.

**LengthUsed:** Ein 1-Byte-Feld, das auf 0x01 oder 0x00 festgelegt werden MUSS. Wenn 0x01 festgelegt ist, wird die Länge der Spalte innerhalb der Zeile übertragen. Wenn 0x00, DARF die Länge der Spalte NICHT innerhalb der Zeile übertragen werden.

**\_ padding3:** Ein 1-Byte-Feld, das vor LengthOffset eingefügt werden MUSS, wenn LengthOffset ohne dieses Feld nicht mit einem geraden Offset vom Anfang einer Nachricht beginnen würde. Der Wert dieses Byte ist willkürlich und MUSS ignoriert werden. Wenn LengthUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.

**LengthOffset:** Eine 2-Byte-Ganzzahl ohne Vorzeichen, die den Offset der Spaltenlänge in der Zeile angibt. Wenn LengthUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.

### <a name="22132-serializedpropertyvalue"></a>2.2.1.32 SERIALIZEDPROPERTYVALUE

Die SERIALIZEDPROPERTYVALUE-Struktur enthält einen serialisierten Wert.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

dwType

rgb (Variable)



 

**dwType:** Einer der in Abschnitt 2.2.1.1 definierten Variantentypen, der mit Variant-Typmodifizierern kombiniert werden kann. Für alle Variantentypen, mit Ausnahme der mit VT ARRAY kombinierten \_ Typen, weist SERIALIZEDPROPERTYVALUE das gleiche Layout wie CBaseStorageVariant auf, wie in Abschnitt 2.2.1.1 angegeben. Wenn der Variant-Typ mit dem VT \_ ARRAY-Typmodifizierer kombiniert wird, wird SAFEARRAY2 gemäß Abschnitt 2.2.1.2.1.1 anstelle von SAFEARRAY im vValue-Feld von CBaseStorageVariant verwendet.

**rgb:** Serialisierter Wert. Weitere Informationen finden Sie unter Serialisierung für vValue in 2.2.1.1.

### <a name="222-message-headers"></a>2.2.2 Nachrichtenheader

Alle Content Indexing Service Protocol-Nachrichten verfügen über einen 16-Byte-Header.

Unten sehen Sie ein Diagramm, das das Nachrichtenheaderformat des Content Indexing Service Protocol zeigt.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_mldg

\_Status

\_ulChecksum

\_ulReserved2



 

\_**msg:** Eine 32-Bit-Ganzzahl, die den Typ der Nachricht nach dem Header angibt. In der folgenden Tabelle sind die Meldungen des Content Indexing Service-Protokolls und die für jede Nachricht angegebenen ganzzahligen Werte aufgeführt. Wie in der Tabelle gezeigt, identifizieren einige Werte zwei Meldungen in der Tabelle. In diesen Fällen kann die Nachricht, die auf den Header folgt, durch die Richtung des Nachrichtenflusses identifiziert werden. Wenn die Richtung Client zu Server ist, wird die Meldung mit "In" angegeben, die an den Nachrichtennamen angefügt ist. Wenn die Richtung Server zu Client ist, wird die Nachricht mit "Out" angegeben, die an den Nachrichtennamen angefügt ist.



| Wert      | Bedeutung                                                     |
|------------|-------------------------------------------------------------|
| 0x000000C8 | CPMConnectIn oder CPMConnectOut                               |
| 0x000000C9 | CPMDisconnect                                               |
| 0x000000CA | CPMCreateQueryIn oder CPMCreateQueryOut                       |
| 0x000000CB | CPMFreeCursorIn oder CPMFreeCursorOut                         |
| 0x000000CC | CPMGetRowsIn oder CPMGetRowsOut                               |
| 0x000000CD | CPMRatioFinishedIn oder CPMRatioFinishedOut                   |
| 0x000000CE | CPMCompareBmkIn oder CPMCompareBmkOut                         |
| 0x000000CF | CPMGetApproximatePositionIn oder CPMGetApproximatePositionOut |
| 0x000000D0 | CPMSetBindingsIn                                            |
| 0x000000D1 | CPMGetNotify                                                |
| 0x000000D2 | CPMSendNotifyOut                                            |
| 0x000000D7 | CPMGetQueryStatusIn oder CPMGetQueryStatusOut                 |
| 0x000000D9 | CPMCiStateInOut                                             |
| 0x000000E1 | CPMForceMergeIn                                             |
| 0x000000E4 | CPMFetchValueIn oder CPMFetchValueOut                         |
| 0x000000E6 | CPMUpdateDocumentsIn                                        |
| 0x000000E7 | CPMGetQueryStatusExIn oder PMGetQueryStatusExOut              |
| 0x000000E8 | CPMRestartPositionIn                                        |
| 0x000000E9 | CPMStopAsynchIn                                             |
| 0x000000EC | CPMSetCatStateIn oder CPMSetCatStateOut                       |



 

\_**status:** Ein HRESULT \[ MS-SYS, \] das den Status des angeforderten Vorgangs angibt.

\* *

*Windows-Verhalten: Der Client legt das \_ Statusfeld immer auf 0x00000000.*

**\_ ulChecksum:** Das ulChecksum MUSS wie in Abschnitt \_ 3.2.4 für die folgenden Meldungen angegeben berechnet werden:

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMSetBindingsIn
-   CPMGetRowsIn
-   CPMFetchValueIn

Für alle anderen Nachrichten MUSS \_ ulChecksum auf 0x00000000. Ein Client MUSS das \_ ulChecksum-Feld ignorieren.

**\_ ulReserved2:** MUSS auf 0 festgelegt und vom Empfänger ignoriert werden.

### <a name="223-messages"></a>2.2.3 Nachrichten

### <a name="2231-cpmcistateinout"></a>2.2.3.1 CPMCiStateInOut

Die CPMCiStateInOut-Nachricht enthält Informationen zum Status des Indizierungsdiensts. Das Format der CPMCiStateInOut-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cbStruct

cWordList

cPersistentIndex

cQueries

cDocuments

cFreshTest

dwMergeProgress

Estate

cFilteredDocuments

cTotalDocuments

cPendingScans

dwIndexSize

cUniqueKeys

cSecQDocuments

dwPropCacheSize



 

**cbStruct:** Eine 32-Bit-Ganzzahl ohne Vorzeichen. Die Größe dieser Nachricht in Bytes (mit Ausnahme des allgemeinen Headers). MUSS auf 0x0000003C festgelegt werden.

**cWordList:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der anfänglichen Indizes angibt, die für kürzlich indizierte Dokumente erstellt wurden.

**cPersistentIndex:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl persistenter Indizes angibt.

**cQueries:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die eine Anzahl aktiv ausgeführter Abfragen angibt.

**cDocuments:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Dokumente angibt, die auf die Indizierung warten.

**cFreshTest:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl eindeutiger Dokumente mit Informationen in Indizes angibt, die nicht vollständig leistungsoptimiert sind.

**dwMergeProgress:** 32-Bit-Ganzzahl ohne Vorzeichen, die den Abschlussprozentsatz der aktuellen vollständigen Optimierung von Indizes angibt, wenn die Optimierung gerade ausgeführt wird. MUSS kleiner oder gleich 100 sein.

**eState:** Status der Inhaltsindizierung, wie von einer oder mehreren CI \_ \_ \* STATE-Konstanten angegeben, die in der folgenden Tabelle definiert sind.



| Wert                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CI \_ STATE SHADOW MERGE \_ \_ 0x00000001           | Der Indizierungsdienst optimiert derzeit einige indizes, um die Speicherauslastung zu reduzieren und die Abfrageleistung zu verbessern.                                                                                                                                                                                                                                                                                                                                                                |
| CI \_ STATE MASTER MERGE \_ \_ 0x00000002           | Der Indizierungsdienst wird derzeit für alle Indizes vollständig optimiert.                                                                                                                                                                                                                                                                                                                                                                                                                  |
| CI \_ STATE CONTENT SCAN REQUIRED \_ \_ \_ 0x00000004 | Einige Dokumente im Index wurden geändert, und der Indizierungsdienst muss bestimmen, welche hinzugefügt, geändert oder gelöscht wurden.                                                                                                                                                                                                                                                                                                                                                              |
| CI \_ STATE \_ ANNEALING \_ MERGE 0x00000008        | Der Indizierungsdienst optimiert derzeit Indizes, um die Speicherauslastung zu reduzieren und die Abfrageleistung zu verbessern. Dieser Prozess ist umfassender als der durch den CI STATE SHADOW MERGE-Wert identifizierte \_ \_ \_ Prozess, ist jedoch nicht so umfassend wie durch den CI \_ STATE MASTER \_ \_ MERGE-Wert angegeben. Solche Optimierungen sind implementierungsspezifisch, da sie davon abhängen, wie Daten intern gespeichert werden. Die Optimierungen wirken sich nur auf die Antwortzeit auf das Protokoll aus. |
| \_CI STATE SCANNING \_ 0x00000010                | Der Indizierungsdienst untersucht ein Verzeichnis oder eine Gruppe von Verzeichnissen, um festzustellen, ob Dateien seit dem letzten Indizieren des Verzeichnisses hinzugefügt, gelöscht oder aktualisiert wurden.                                                                                                                                                                                                                                                                                                                 |
| CI \_ STATE \_ RECOVERING 0x00000020              | Der Dienst beginnt mit dem letzten gespeicherten Zustand und wird gerade wiederhergestellt.                                                                                                                                                                                                                                                                                                                                                                                                        |
| CI \_ STATE LOW MEMORY \_ \_ 0x00000080             | Der größte Teil des virtuellen Arbeitsspeichers des Servers wird verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| CI \_ STATE HIGH IO \_ \_ 0x00000100                | Die E/A-Aktivität (Input/Output) auf dem Server ist relativ hoch.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CI \_ STATE MASTER MERGE \_ \_ \_ PAUSED 0x00000200   | Der Prozess der vollständigen Optimierung für alle Indizes, die gerade ausgeführt wurden, wurde angehalten. Dies dient nur zu Informationszwecken und wirkt sich nicht auf CISP aus.                                                                                                                                                                                                                                                                                                                                  |
| CI \_ STATE READ ONLY \_ \_ 0x00000400              | Der Teil des Indizierungsdiensts, der neue zu indizierende Dokumente aufnimmt, wurde angehalten. Dies dient nur zu Informationszwecken und wirkt sich nicht auf CISP aus.                                                                                                                                                                                                                                                                                                                               |
| CI \_ STATE BATTERY POWER \_ \_ 0x00000800          | Der Teil des Indizierungsdiensts, der neue zu indizierende Dokumente aufnimmt, wurde angehalten, um die Akkulebensdauer zu sparen, antwortet aber weiterhin auf die Abfragen. Dies dient nur zu Informationszwecken und wirkt sich nicht auf CISP aus.                                                                                                                                                                                                                                                                 |
| CI \_ STATE USER ACTIVE \_ \_ 0x00001000            | Der Teil des Indizierungsdiensts, der neue zu indizierende Dokumente aufnimmt, wurde aufgrund einer hohen Aktivität durch den Benutzer (Tastatur oder Maus) angehalten, antwortet aber weiterhin auf die Abfragen. Dies dient nur zu Informationszwecken und wirkt sich nicht auf CISP aus.                                                                                                                                                                                                                                         |
| CI \_ STATE \_ STARTING 0x00002000                | Der Dienst wird gestartet. Abfragen können ausgeführt werden, aber die Überprüfung und Benachrichtigung wurden noch nicht aktiviert. Dies dient nur zu Informationszwecken und wirkt sich nicht auf CISP aus.                                                                                                                                                                                                                                                                                                                   |
| CI \_ STATE \_ READING \_ USNS 0x00004000           | Der Dienst hat das vom Dateisystem gespeicherte Protokoll nicht gelesen, um Änderungen an Dateien oder Verzeichnissen auf einem Volume nachzuverfolgen, sodass der Index möglicherweise nicht auf dem neuesten Stand ist.                                                                                                                                                                                                                                                                                                                                  |



 

**cFilteredDocuments:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Seit Beginn der Inhaltsindizierung indizierten Dokumente angibt.

**cTotalDocuments:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Dokumente im System angibt.

**cPendingScans:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl ausstehender Indizierungsvorgänge auf hoher Ebene angibt. Die Bedeutung dieses Werts ist anbieterspezifisch, aber es wird erwartet, dass größere Zahlen darauf hindeuten, dass mehr Indizierung verbleibt.

*Windows-Verhalten:* Dieser Wert ist in der Regel 0 (null), es sei denn, er liegt unmittelbar nach dem Starten der Indizierung oder nach einem Benachrichtigungswarteschlangenüberlauf vor.

**dwIndexSize:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des Indexes (mit Ausnahme des Eigenschaftencaches) in Megabyte angibt.

**cUniqueKeys:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die ungefähre Anzahl eindeutiger Schlüssel im Katalog angibt.

**cSecQDocuments:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dokumente angibt, die der Indizierungsdienst aufgrund eines Fehlers während des ersten Indizierungsversuchs erneut indiziert.

**dwPropCacheSize:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des Eigenschaftencaches in Megabyte angibt.

### <a name="2232-cpmsetcatstatein"></a>2.2.3.2 CPMSetCatStateIn

Die CPMSetCatStateIn-Nachricht legt den Status eines Katalogs fest. Das Format der CPMSetCatStateIn-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_partID

\_dwNewState

\_CatName (Variable, optional)



 

**\_ partID:** MUSS auf 0x00000001 festgelegt werden.

**\_ dwNewState:** MUSS auf einen der folgenden Werte festgelegt werden, der den neuen Status des Katalogs angibt.



| Wert                         | Bedeutung                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CICAT \_ STOPPED 0x00000001     | Der Katalog wird beendet. Dieser Zustand bedeutet, dass keine neuen Dateien indiziert und keine Suchabfragen verarbeitet werden sollen.                                                     |
| CICAT \_ READONLY-0x00000002    | Der Katalog ist schreibgeschützt. Es sollen keine neuen Dateien indiziert werden.                                                                                                               |
| CICAT \_ WRITABLE-0x00000004    | Der Katalog kann geschrieben werden. Neue Dateien können indiziert werden, und Suchabfragen müssen verarbeitet werden.                                                                              |
| CICAT \_ NO \_ QUERY 0x00000008   | Der Katalog ist nicht für Abfragen verfügbar.                                                                                                                              |
| CICAT \_ GET \_ STATE 0x00000010  | Der Status des Katalogs soll nicht geändert, sondern nur abgerufen werden.                                                                                                          |
| CICAT \_ ALL \_ OPENED 0x00000020 | Eine Überprüfung, um festzustellen, ob alle Kataloge gestartet wurden. Wenn ja, wird das \_ feld dwOldState, das in der CPMSetCatStateOut-Antwort an diese Nachricht gesendet wird, als ungleich 0 (null) gemeldet. |



 

**\_ CatName:** Der Name des Katalogs, dessen Status geändert werden soll. Der Name MUSS eine auf NULL endende Unicode-Zeichenfolge sein. Dieses Feld MUSS weggelassen werden, wenn \_ dwNewState auf CICAT ALL OPENED festgelegt \_ \_ ist.

### <a name="2233-cpmsetcatstateout"></a>2.2.3.3 CPMSetCatStateOut

Die CPMSetCatStateOut-Nachricht ist eine Antwort auf eine CPMSetCatStateIn-Nachricht mit dem alten Status des Katalogs. Das Format der CPMSetCatStateOut-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_dwOldState



 

**\_ dwOldState:** Einer der folgenden Werte, der den alten Status des Katalogs angibt.



| Wert                       | Bedeutung                                    |
|-----------------------------|--------------------------------------------|
| CICAT \_ STOPPED 0x00000001   | Der Katalog wird beendet.                    |
| CICAT \_ READONLY-0x00000002  | Der Katalog ist schreibgeschützt.                  |
| CICAT \_ WRITABLE 0x00000004  | Der Katalog ist schreibbar.                   |
| CICAT \_ NO \_ QUERY 0x00000008 | Der Katalog ist nicht für Abfragen verfügbar. |



 

### <a name="2234-cpmupdatedocumentsin"></a>2.2.3.4 CPMUpdateDocumentsIn

Die CPMUpdateDocumentsIn-Nachricht weist den Server an, den angegebenen Pfad zu indiziert.

Der Server antwortet mit dem Nachrichtenheader der CPMUpdateDocumentsOut-Nachricht, wobei die Ergebnisse der Anforderung im \_ Statusfeld des Nachrichtenheaders enthalten sind.

Das Format der CPMUpdateDocumentsIn-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Flag (optional)

\_fRootPath (optional)

RootPath (Variable, optional)



 

**\_ flag:** Der Typ des auszuführenden Updates. Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird. Dieses Feld MUSS auf einen der folgenden Werte festgelegt werden:



| Wert                  | Bedeutung                                   |
|------------------------|-------------------------------------------|
| UPD \_ INCREM 0x00000000 | Ein inkrementelles Update muss ausgeführt werden. |
| UPD \_ FULL 0x00000001   | Ein vollständiges Update muss ausgeführt werden.         |
| UPD \_ INIT 0x00000002   | Eine neue Initialisierung wird ausgeführt.  |



 

**\_ fRootPath:** Ein boolescher Wert, der angibt, ob das RootPath-Feld einen Pfad angibt, unter dem das Update ausgeführt werden soll. Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird. Dieses Feld MUSS auf 0x00000001 oder 0x00000000 festgelegt werden. Wenn 0x00000001 festgelegt ist, ist ein Pfad, auf dem das Update ausgeführt werden soll, in RootPath enthalten. Wenn 0x00000000 festgelegt ist, muss das Update für alle indizierten Pfade ausgeführt werden.

**RootPath:** Der Name des pfads, der aktualisiert werden soll. Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird. Der Name MUSS eine auf NULL endende Unicode-Zeichenfolge sein. Dieses Feld MUSS weggelassen werden, wenn \_ fRootPath auf 0x00000000 festgelegt ist.

### <a name="2235-cpmforcemergein"></a>2.2.3.5 CPMForceMergeIn

Die CPMForceMergeIn-Nachricht fordert einen Server zur Durchführung von Wartungsarbeiten an, die zur Verbesserung der Abfrageleistung erforderlich sind. Der Server antworte mit dem Nachrichtenheader der CPMForceMergeIn-Nachricht, wobei die Ergebnisse der Anforderung im Statusfeld enthalten \_ sind.

Das Format der CPMForceMergeIn-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_partID (optional)



 

**\_ partID:** Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird. Wenn dieses Feld vorhanden ist, MUSS es auf 0x00000001 festgelegt werden.

### <a name="2236-cpmconnectin"></a>2.2.3.6 CPMConnectIn

Die CPMConnectIn-Nachricht startet eine Sitzung zwischen Client und Server.

Das Format der CPMConnectIn-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_iClientVersion

\_fClientIsRemote

\_cbBlob1

\_cbBlob2

\_Polsterung

...

...

MachineName

... (Variable)

UserName (Benutzername)

... (Variable)

\_paddingcPropSets (optional, Variable)

cPropSets

PropertySet1 (Variable)

PropertySet2 (Variable)

\_paddingExtPropset (optional, Variable)

cExtPropSet

aPropertySets (Variable)



 

**\_ iClientVersion:** Eine 32-Bit-Ganzzahl, die angibt, ob der Server den Prüfsummenwert überprüfen soll, der im \_ ulChecksum-Feld der Nachrichtenheader für vom Client gesendete Nachrichten angegeben ist. Wenn das \_ Feld iClientVersion auf 0x00000008 oder höher festgelegt ist, MUSS der Server den \_ UlChecksum-Feldwert für die folgenden Meldungen überprüfen:

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMFetchValueIn
-   CPMGetRowsIn
-   CPMSetBindingsIn

Ausführliche Informationen dazu, wie der Server den vom Client im UlChecksum-Feld für die oben aufgeführten Nachrichten angegebenen Wert überprüft, finden Sie in Abschnitt 3.2.5.

Wenn der Wert größer als 0x00000008 wird davon ausgegangen, dass der Client 64-Bit-Offsets in CPMGetRowsOut-Nachrichten verarbeiten kann. Weitere Informationen finden Sie in Abschnitt 2.2.3.16.

*Windows-Verhalten: Auf Windows-Clients wird die iClientVersion wie folgt festgelegt:*



| Wert      | Bedeutung                                                              |
|------------|----------------------------------------------------------------------|
| 0x00000005 | Das Clientbetriebssystem ist Windows 2000.                                           |
| 0x00000008 | Das Clientbetriebssystem ist entweder 32-Bit-Windows XP oder 32-Bit-Windows Server 2003. |
| 0x00010008 | Das Clientbetriebssystem ist entweder 64-Bit-Windows XP oder 64-Bit-Windows Server 2003. |



 

\_**fClientIsRemote:** Ein boolescher Wert, der angibt, ob der Client auf einem anderen Computer als dem Server ausgeführt wird. MUSS auf 0x00000001 festgelegt werden.

\_**cbBlob1:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der Felder cPropSet, PropertySet1 und PropertySet2 in Bytes angibt, kombiniert.

\_**cbBlob2:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der Felder cExPropSet und aPropertySet in Bytes angibt, kombiniert.

\_**Auffüllung:** 12 Bytes auffüllen, die beliebige Werte enthalten können, und MÜSSEN ignoriert werden.

**MachineName:** Der Computername des Clients. Die Namenszeichenfolge MUSS ein nullterminiertes Array mit weniger als 512 Unicode-Zeichen sein, einschließlich des NULL-Abschlusszeichens.

**UserName:** Eine Zeichenfolge, die den Benutzernamen der Person darstellt, die die Anwendung ausführt, die dieses Protokoll aufgerufen hat. Die Namenszeichenfolge MUSS ein mit NULL endendes Array mit weniger als 512 Unicode-Zeichen sein, wenn sie mit MachineName verkettet wird.

**\_ paddingcPropSets:** Dieses Feld MUSS 0 bis 7 Bytes lang sein. Die Anzahl der Bytes MUSS die Anzahl sein, die erforderlich ist, um den Byteoffset des cPropSets-Felds vom Anfang der Nachricht, die diese Struktur enthält, auf ein Vielfaches von 8 zu setzen. Der Wert der Bytes kann ein beliebiger Wert sein, und MUSS vom Empfänger ignoriert werden.

**cPropSets:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der CDbPropSet-Strukturen angibt, die diesem Feld folgen. Dieser Wert MUSS auf 0x0000002 festgelegt werden.

**PropertySet1:** Eine CDbPropSet-Struktur mit guidPropertySet, die DBPROPSET \_ FSCIFRMWRK EXT enthält \_ (siehe Abschnitt 2.2.1.22).

**PropertySet2:** Eine CDbPropSet-Struktur mit guidPropertySet, die DBPROPSET \_ CIFRMWRKCORE EXT enthält \_ (siehe Abschnitt 2.2.1.22).

\_**PaddingExtPropset:** Dieses Feld MUSS 0 bis 7 Bytes lang sein. Die Anzahl der Bytes MUSS die Anzahl sein, die erforderlich ist, um den Byteoffset des Felds cExtPropSets vom Anfang der Nachricht, die diese Struktur enthält, auf ein Vielfaches von 8 zu setzen. Der Wert der Bytes kann ein beliebiger Wert sein, und MUSS vom Empfänger ignoriert werden.

**cExtPropSet:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der CDbPropSet-Strukturen angibt, die diesem Feld folgen.

**aPropertySets:** Ein Array von CDbPropSet-Strukturen, die andere Eigenschaften angeben. Die Anzahl der Elemente in diesem Array MUSS cExtPropSet entsprechen.

### <a name="2237-cpmconnectout"></a>2.2.3.7 CPMConnectOut

Die CPMConnectOut-Nachricht enthält eine Antwort auf eine CPMConnectIn-Nachricht.

Das Format der CPMConnectOut-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_serverVersion

\_reserviert (Variable)



 

**\_ serverVersion**:

Eine 32-Bit-Ganzzahl, die angibt, ob der Server 64-Bit-Offsets unterstützen *kann.* Weitere Informationen finden Sie in Abschnitt 2.2.3.16.



| Wert      | Bedeutung                                 |
|------------|-----------------------------------------|
| 0x00000007 | Der Server kann nur 32-Bit-Offsets senden. |
| 0x00010007 | Der Server kann 32- oder 64-Bit-Offsets senden.   |



 

**\_ reserviert:** Reserviert. Der Server KANN eine beliebige Anzahl beliebiger Werte senden, und der Client MUSS diese Werte ignorieren, sofern vorhanden.

### <a name="2238-cpmcreatequeryin"></a>2.2.3.8 CPMCreateQueryIn

Die CPMCreateQueryIn-Nachricht erstellt eine neue Abfrage. Das Format der CPMCreateQueryIn-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Size

CColumnSetPresent

ColumnSet (optional)

... (Variable)

CRestrictionPresent.

Einschränkung (optional)

... (Variable)

CSortSetPresent

SortSet (optional)

... (Variable)

CCategorizationSetPresent

CategorizationSet (optional)

... (Variable)

RowSetProperties

...

...

...

...

PidMapper (Variable)



 

**Größe:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Bytes vom Anfang dieses Felds bis zum Ende der Nachricht angibt.

**CColumnSetPresent:** Ein Bytefeld, das angibt, ob das ColumnSet-Feld vorhanden ist. Dieses Feld MUSS auf 0x01 oder 0x00 festgelegt werden. Wenn auf 0x01 muss das Feld CColumnSet vorhanden sein. Wenn sie auf 0x00 festgelegt ist, MUSS sie fehlen.

**ColumnSet:** Eine CColumnSet-Struktur, die die Spaltennummern enthält, in denen die Eigenschaften von CPidMapper zurückgegeben werden sollen.

**CRestrictionPresent:** Ein Bytefeld, das angibt, ob das Feld Einschränkung vorhanden ist. Wenn ein Wert ungleich 0 (null) festgelegt ist, MUSS das Feld Einschränkung vorhanden sein. Wenn sie auf 0x00 festgelegt ist, MUSS die Einschränkung nicht vorhanden sein.

**Einschränkung:** Eine CRestriction-Struktur, die die Befehlsstruktur der Abfrage enthält.

**CSortSetPresent:** Ein Bytefeld, das angibt, ob das SortSet-Feld vorhanden ist. Wenn ein Wert ungleich 0 (null) festgelegt ist, MUSS das SortSet-Feld vorhanden sein. Wenn diese Einstellung auf 0x00 festgelegt ist, MUSS SortSet fehlen.

**SortSet:** Eine CSortSet-Struktur, die die Sortierreihenfolge der Abfrage angibt.

**CCategorizationSetPresent:** Ein Bytefeld, das angibt, ob das Feld CCategorizationSet vorhanden ist. Wenn ein Wert ungleich 0 (null) festgelegt ist, MUSS das Feld CCategorizationSet vorhanden sein. Wenn CCategorizationSet auf 0x00 festgelegt ist, MUSS es nicht vorhanden sein.

**CCategorizationSet:** Eine CCategorizationSet-Struktur, die die Gruppen für die Abfrage enthält.

**RowSetProperties:** Eine CRowsetProperties-Struktur, die Konfigurationsinformationen für die Abfrage bereitstellt.

**PidMapper:** Eine CPidMapper-Struktur, die Eigenschaften enthält, die in einem Rowset zurückgegeben werden sollen.

### <a name="2239-cpmcreatequeryout"></a>2.2.3.9 CPMCreateQueryOut

Die CPMCreateQueryOut-Nachricht enthält eine Antwort auf eine CPMCreateQueryIn-Nachricht.

Das Format der CPMCreateQueryOut-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_fTrueSequential

\_fWorkIdUnique

aCursors



 

**\_ fTrueSequential:** Ein informativer boolescher Wert, der angibt, ob die Abfrage ergebnisse schneller liefern kann. Wenn für die in CPMCreateQueryIn bereitgestellte Abfrage 0x00000001 festgelegt ist, kann der Server den Index so verwenden, dass die Abfrageergebnisse wahrscheinlich schneller übermittelt werden. Wenn sie auf 0x00000000 festgelegt ist, kommt es bei der Übermittlung von Abfrageergebnissen zu einer höheren Latenz. DARF nicht auf einen anderen Wert festgelegt werden.

**\_ fWorkIdUnique:** Ein boolescher Wert, der angibt, ob die Dokumentbezeichner, auf die die Cursor zeigen, in den Abfrageergebnissen eindeutig sind. Wenn 0x00000001 festgelegt ist, sind die Bezeichner eindeutig. Wenn sie auf 0x00000000 festgelegt sind, sind sie nur im gesamten Rowset eindeutig.

**aCursors:** Ein Array von 32-Bit-Ganzzahlen ohne Vorzeichen, die die Handles für Cursor darstellen, wobei die Anzahl der Elemente der Anzahl der Kategorien im Feld CategorizationSet der CPMCreateQueryIn-Nachricht entspricht.

### <a name="22310-cpmgetquerystatusin"></a>2.2.3.10 CPMGetQueryStatusIn

Die CPMGetQueryStatusIn-Nachricht fordert den Status einer Abfrage an. Das Format der CPMGetQueryStatusIn-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor



 

**\_ hCursor:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Handle aus der CPMCreateQueryOut-Nachricht darstellt, die die Abfrage identifiziert, für die Statusinformationen abgerufen werden sollen.

### <a name="22311-cpmgetquerystatusout"></a>2.2.3.11 CPMGetQueryStatusOut

Die CPMGetQueryStatusOut-Nachricht antwortet auf eine CPMGetQueryStatusIn-Nachricht mit dem Status der Abfrage. Das Format der CPMGetQueryStatusOut-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Status



 

**\_ Status:** Eine Bitmaske mit Werten, die in den folgenden Tabellen definiert sind, die die Abfrage beschreiben.

In der folgenden Tabelle sind die STAT-Werte aufgeführt, \_ \* die durch ausführen eines bitweisen AND-Vorgangs für \_ Status mit 0x00000007. Das Ergebnis MUSS eines der folgenden sein:



| Konstante                 | Bedeutung                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| STAT \_ BUSY 0x00000000    | Die asynchrone Abfrage wird weiterhin ausgeführt.                                          |
| STAT \_ ERROR 0x00000001   | Die Abfrage befindet sich in einem Fehlerzustand.                                                   |
| STAT \_ DONE 0x00000002    | Die Abfrage ist abgeschlossen.                                                            |
| STAT \_ REFRESH 0x00000003 | Die Abfrage ist abgeschlossen, aber Updates führen zu einer zusätzlichen Abfrageberechnung. |



 

In der folgenden Tabelle sind zusätzliche \_ \* STAT-Bits aufgeführt, die unabhängig voneinander festgelegt werden können.



| Konstante                                    | Bedeutung                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| STAT \_ NOISE \_ WORDS 0x00000010               | Füllwörter wurden in der Inhaltsabfrage durch Platzhalterzeichen ersetzt.                                                              |
| VERALTETER \_ \_ STAT-INHALT \_ \_ 0x00000020     | Die Ergebnisse der Abfrage sind möglicherweise falsch, da die Abfrage geänderte, aber nicht indizierte Dateien umfasst.                             |
| STAT \_ REFRESH \_ INCOMPLETE 0x00000040        | Die Ergebnisse der Abfrage sind möglicherweise falsch, da die Abfrage geänderte und neu indizierte Dateien umfasst, deren Inhalt nicht enthalten war. |
| STAT \_ CONTENT QUERY INCOMPLETE \_ \_ 0x00000080 | Die Inhaltsabfrage war zu komplex, um die Enumeration abzuschließen oder zu erfordern, anstatt den Inhaltsindex zu verwenden.                          |
| STAT \_ TIME \_ LIMIT \_ EXCEEDED 0x00000100      | Die Ergebnisse der Abfrage sind möglicherweise falsch, da die Ausführungszeit der Abfrage die maximal zulässige Zeit erreicht hat.                    |



 

### <a name="22312-cpmgetquerystatusexin"></a>2.2.3.12 CPMGetQueryStatusExIn

Die CPMGetQueryStatusExIn-Nachricht fordert den Status einer Abfrage und zusätzliche Informationen an, z. B. die Anzahl der indizierten Dokumente, die Anzahl der zu indizierten Dokumente usw. Das Format der CPMGetQueryStatusExIn-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_bmk



 

**\_ hCursor:** Ein 32-Bit-Wert, der das Handle aus der CPMCreateQueryOut-Nachricht darstellt, die die Abfrage identifiziert, für die Statusinformationen abgerufen werden sollen.

**\_ bmk:** Ein 32-Bit-Wert, der das Handle eines Lesezeichens angibt, dessen Position abgerufen werden soll.

### <a name="22313-cpmgetquerystatusexout"></a>2.2.3.13 CPMGetQueryStatusExOut

Die CPMGetQueryStatusExOut-Nachricht antwortet auf eine CPMGetQueryStatusExIn-Nachricht mit dem Status der Abfrage und anderen Statusinformationen, wie im folgenden Diagramm dargestellt. Das Format der CPMGetQueryStatusExOut-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Status

\_cFilteredDocuments

\_cDocumentsToFilter

\_dwRatioFinishedDenominator

\_dwRatioFinishedNumerator

\_iRowBmk

\_cRowsTotal



 

**\_ Status:** Einer der STAT-Werte \_ \* -Werte, die in Abschnitt 2.2.3.11 angegeben sind.

**\_ cFilteredDocuments:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der indizierten Dokumente angibt.

**\_ cDocumentsToFilter:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dokumente angibt, die noch indiziert werden müssen.

**\_ dwRatioFinishedDenominator:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Nenner des Verhältnisses der Dokumente angibt, die die Abfrage verarbeitet hat.

**\_ dwRatioFinishedNumerator:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Zähler des Verhältnisses der Dokumente angibt, die die Abfrage verarbeitet hat.

**\_ iRowBmk:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die ungefähre Position des Lesezeichens im Rowset in Bezug auf Zeilen angibt.

**\_ cRowsTotal:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Zeilen im Rowset angibt.

### <a name="22314-cpmsetbindingsin"></a>2.2.3.14 CPMSetBindingsIn

Die CPMSetBindingsIn-Nachricht fordert die Bindung von Spalten an ein Rowset an. Der Server antwortet mithilfe des Headerabschnitts der CPMBindingsIn-Nachricht mit den Ergebnissen der Anforderung, die im Statusfeld enthalten sind, auf die ANFORDERUNGsnachricht CPMSetBindingsIn. \_ Das Format der CPMSetBindingsIn-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor (optional)

\_cbRow (optional)

\_cbBindingDesc (optional)

\_dummy (optional)

cColumns (optional)

aColumns (Variable, optional)



 

**\_ hCursor:** Ein 32-Bit-Wert, der das Handle aus der CPMCreateQueryOut-Nachricht darstellt, die die Zeile identifiziert, für die Bindungen festgelegt werden sollen. Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.

**\_ cbRow:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe einer Zeile in Bytes angibt. Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.

**\_ cbBindingDesc:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge der Felder nach dem Dummyfeld in Bytes \_ angibt. Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.

**\_ dummy:** Dieses Feld wird nicht verwendet und MUSS ignoriert werden. Sie kann auf einen beliebigen Wert festgelegt werden. Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.

**cColumns:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im Array aColumns angibt. Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.

**aColumns:** Ein Array der CTableColumn-Strukturen, die die Spalten einer Zeile im Rowset beschreiben. Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird. Strukturen im Array MÜSSEN durch 0 bis 3 Auffüllungsbytes getrennt werden, sodass jede Struktur eine 4-Byte-Ausrichtung vom Anfang einer Nachricht aufweist. Solche Auffüllungsbytes können beliebige Werte sein, und MÜSSEN beim Empfang ignoriert werden.

### <a name="22315-cpmgetrowsin"></a>2.2.3.15 CPMGetRowsIn

Die CPMGetRowsIn-Nachricht fordert Zeilen aus einer Abfrage an. Das Format der CPMGetRowsIn-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_cRowsToTransfer

\_cbRowWidth

\_cbSeek

\_cbReserved

\_cbReadBuffer

\_ulClientBase

\_fBwdFetch

eType

\_chapt

SeekDescription

...

... (Variable)



 

**\_ hCursor:** Ein 32-Bit-Wert, der das Handle aus der CPMCreateQueryOut-Nachricht darstellt, die die Abfrage identifiziert, für die Zeilen abgerufen werden sollen.

**\_ cRowsToTransfer:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die maximale Anzahl von Zeilen angibt, die der Client als Antwort auf diese Nachricht empfangen möchte.

**\_ cbRowWidth:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge einer Zeile in Bytes angibt.

**\_ cbSeek:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der Nachricht angibt, die mit eType beginnt.

**\_ cbReserved:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe einer CPMGetRowsOut-Nachricht in Bytes angibt (ohne die Felder Rows und SeekDescriptions). Dieser Wert in diesem Feld wird dem Wert des \_ cbSeek-Felds hinzugefügt und dann verwendet, um den Offset des Rows-Felds in der CPMGetRowsOut-Nachricht zu berechnen.

**\_ cbReadBuffer:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die auf das Maximum des Werts von \_ cbRowWidth oder das 1000-fache des Werts von \_ cRowsToTransfer festgelegt werden MUSS, aufgerundet auf das nächste 512-Byte-Vielfache. Der Wert DARF 0x00004000 NICHT überschreiten.

**\_ ulClientBase:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Basiswert angibt, der für Zeigerberechnungen im Zeilenpuffer verwendet werden soll. Wenn 64-Bit-Offsets verwendet werden, wird das Feld reserved2 des Nachrichtenheaders als obere 32-Bit-Klasse und \_ ulClientBase als unteres 32-Bit-Feld eines 64-Bit-Werts verwendet. Weitere Informationen finden Sie in Abschnitt 2.2.3.16.

**\_ fBwdFetch:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Reihenfolge angibt, in der die Zeilen abgerufen werden sollen. Wenn 0x00000001 festgelegt ist, werden die Zeilen in umgekehrter Reihenfolge abgerufen. Wenn 0x00000000 festgelegt ist, werden die Zeilen in vorwärts gerichteter Reihenfolge abgerufen. DARF NICHT auf andere Werte festgelegt werden.

**eType:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die einen der folgenden Werte enthält, um den Typ des durchzuführenden Vorgangs anzugeben.



| Wert                         | Bedeutung                                                  |
|-------------------------------|----------------------------------------------------------|
| eRowSeekNext 0x00000001       | SeekDescription enthält eine CRowSeekNext-Struktur.       |
| eRowSeekAt 0x00000002         | SeekDescription enthält eine CRowSeekAt-Struktur.         |
| eRowSeekAtRatio 0x00000003    | SeekDescription enthält eine CRowSeekAtRatio-Struktur.    |
| eRowSeekByBookmark-0x00000004 | SeekDescription enthält eine CRowSeekByBookmark-Struktur. |



 

**\_ chapt:** Ein 32-Bit-Wert, der das Handle des Rowset-Kapitels darstellt.

**SeekDescription:** Dieses Feld MUSS eine Struktur des Typs enthalten, der durch den eType-Wert angegeben wird.

### <a name="22316-cpmgetrowsout"></a>2.2.3.16 CPMGetRowsOut

Die CPMGetRowsOut-Nachricht antwortet auf eine CPMGetRowsIn-Nachricht mit den Zeilen einer Abfrage. Server MÜSSEN Offsets wie folgt in Datentypen variabler Länge im Feld Zeilen formatieren:

-   Client hat angegeben, dass es sich um ein 32-Bit-System handelt (0x00000008 oder weniger im iClientVersion-Feld von CPMConnectIn): Offsets sind 32-Bit-Ganzzahlen.
-   Der Client hat angegeben, dass es sich um ein 64-Bit-System handelt ( iClientVersion > 0x00000008 in CPMConnectIn), und server gibt an, dass es sich um ein \_ 32-Bit-System handelt ( serverVersion auf \_ 0x00000007 in CPMConnectOut festgelegt): Offsets sind 32-Bit-Ganzzahlen
-   Der Client hat angegeben, dass es sich um ein 64-Bit-System handelt ( iClientVersion > 0x00000008 in CPMConnectIn), und der Server hat angegeben, dass es sich um ein \_ 64-Bit-System handelt ( serverVersion auf \_ 0x00010007 in CPMConnectOut festgelegt): Offsets sind 64-Bit-Ganzzahlen.

Das Format der CPMGetRowsOut-Nachricht, die auf den Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cRowsReturned

eType

\_chapt

SeekDescription (optional, Variable)

...

...

paddingRows (optional, variable)

Zeilen



 

**\_ cRowsReturned:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der in Zeilen zurückgegebenen Zeilen angibt.

**eType:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die einen der folgenden Werte enthält, um den Typ des rowseek-Vorgangs anzugeben, der durchgeführt werden soll.



| Wert                         | Bedeutung                                                  |
|-------------------------------|----------------------------------------------------------|
| eRowsSeekNone 0x00000000      | No SeekDescription, ignore SeekDescription field.        |
| eRowSeekNext 0x00000001       | SeekDescription enthält eine CRowSeekNext-Struktur.       |
| eRowSeekAt 0x00000002         | SeekDescription enthält eine CRowSeekAt-Struktur.         |
| eRowSeekAtRatio 0x00000003    | SeekDescription enthält eine CRowSeekAtRatio-Struktur.    |
| eRowSeekByBookmark-0x00000004 | SeekDescription enthält eine CRowSeekByBookmark-Struktur. |



 

**\_ chapt:** Ein 32-Bit-Wert, der das Handle des Rowset-Kapitels darstellt.

**SeekDescription:** Dieses Feld MUSS eine Struktur des Typs enthalten, der durch das eType-Feld angegeben wird.

**paddingRows:** Dieses Feld MUSS eine ausreichende Länge (0 bis cbReserved-1 Byte) haben, um das Rows-Feld vom Anfang einer Nachricht bis zum cbReserved-Offset zu auffüllung, wobei cbReserved der Wert in der \_ \_ \_ CPMGetRowsIn-Nachricht ist. Die in diesem Feld verwendeten Auf padding-Bytes können beliebige Werte sein. Dieses Feld MUSS vom Empfänger ignoriert werden.

**Zeilen:** Zeilendaten werden gemäß den Spalteninformationen in der letzten CPMSetBindingsIn-Nachricht formatiert. Zeilen MÜSSEN in vorwärts geordneter Reihenfolge gespeichert werden (z. B. Zeile 1 vor Zeile 2).

Spalten mit fester Größe MÜSSEN an den Offsets gespeichert werden, die von der letzten CPMSetBindingsIn-Nachricht angegeben werden.

Spalten variabler Größe (z. B. Zeichenfolgen) MÜSSEN wie folgt gespeichert werden:

-   Die Variablendaten selbst (z. B. die Zeichenfolge) werden am Ende des Puffers in absteigender Reihenfolge gespeichert (z. B. befindet sich die Auflistung aller Variablendaten für Zeile 1 am Ende, Zeile 2 am nächsten usw.).
-   Der Bereich mit fester Größe (am Anfang des Zeilenpuffers) MUSS eine CRowVariant für jede Spalte enthalten, die an dem Offset gespeichert ist, der in der letzten CPMSetBindingsIn-Nachricht angegeben ist. vType MUSS den Datentyp enthalten (z.B. VT \_ LPWSTR). Wenn, wie durch die Regeln am Anfang dieses Abschnitts festgelegt, 32-Bit-Offsets verwendet werden, muss das Feld Offset in CRowVariant einen 32-Bit-Wert enthalten, der den Offset der Variablendaten vom Anfang der CPMGetRowsOut-Nachricht sowie den Wert von ulClientBase enthält, der in der letzten \_ CPMGetRowsIn-Nachricht angegeben ist. Wenn 64-Bit-Offsets verwendet werden, muss das Feld Offset in CRowVariant einen 64-Bit-Wert enthalten, der der Offset vom Anfang der CPMGetRowsOut-Nachricht ist, der einem 64-Bit-Wert hinzugefügt wird, der mithilfe von ulClientBase als niedriger \_ 32-Bit-Wert und ulReserved2 als hohe \_ 32-Bit-Werte zusammengesetzt wird.

Wenn in der CPMSetBindingsIn-Nachricht beispielsweise die beiden Spalten Size (VT \_ I4) und Title (VT \_ LPWSTR) und ulClientBase von CPMGetRowsIn 0x10000 werden zwei Zeilen wie folgt \_ angezeigt. Der grau markierte Abschnitt ist der Teil mit fester Länge des Puffers.

![Beispiel für eine cpmsetbindingsin-Nachricht](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a>2.2.3.17 CPMRatioFinishedIn

Die CPMRatioFinishedIn-Nachricht fordert den Abschlussprozentsatz einer Abfrage an. Das Format der CPMRatioFinishedIn-Nachricht, die dem Header folgt, lautet:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_fQuick



 

**\_ hCursor:** Das Handle aus der CPMCreateQueryOut-Nachricht, das die Abfrage identifiziert, für die Abschlussinformationen angefordert werden sollen.

**\_ fQuick:** MUSS auf 0x00000001 festgelegt werden. Nicht verwendet und MÜSSEN vom Server ignoriert werden.

### <a name="22318-cpmratiofinishedout"></a>2.2.3.18 CPMRatioFinishedOut

Die CPMRatioFinishedOut-Nachricht antwortet auf eine CPMRatioFinishedIn-Nachricht mit dem Abschlussverhältnis einer Abfrage. Das Format der CPMRatioFinishedOut-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_ ulNumerator

\_ulDenominator

\_Krähen

\_fNewRows



 

**\_ ulNumerator:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Zähler des Vervollständigungsverhältnisses in Bezug auf Zeilen angibt.

**\_ ulDenominator:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Nenner des Vervollständigungsverhältnisses in Bezug auf Zeilen angibt. MUSS größer als 0 (null) sein.

**\_ cRows:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Zeilen für die Abfrage angibt.

**\_ fNewRows:** Ein boolescher Wert, der angibt, ob neue Zeilen verfügbar sind. Der Wert 0x00000001 gibt an, dass neue Zeilen im Rowset verfügbar sind. Der Wert 0x00000000 gibt an, dass das Rowset keine neuen Zeilen enthält. Dieses Feld DARF NICHT auf andere Werte festgelegt werden.

### <a name="22319-cpmfetchvaluein"></a>2.2.3.19 CPMFetchValueIn

Die CPMFetchValueIn-Nachricht fordert einen Eigenschaftswert an, der für die Rückgabe in einem Rowset zu groß war. Wie in Abschnitt 3.2.4.2.5 angegeben, wird diese Meldung wiederholt gesendet, um alle Bytes der Eigenschaft abzurufen, wobei \_ cbSoFar für jede aktualisiert wird, bis das \_ fMoreExists-Feld der CPMFetchValueOut-Nachricht auf **FALSE** festgelegt ist.

Das Format der CPMFetchValueIn-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Wid

\_cbSoFar

\_cbPropSpec

\_cbChunk

PropSpec (Variable)

...

\_Auffüllen (Variable)



 

**\_ wid**: Eine 32-Bit-Ganzzahl ohne Vorzeichen, die Informationen über die Dokument-ID enthält, die das Dokument identifiziert, für das eine Eigenschaft abgerufen werden soll.

**\_ cbSoFar:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Bytes enthält, die zuvor für diese Eigenschaft übertragen wurden. MUSS in der ersten Nachricht auf 0x00000000 festgelegt werden.

**\_ cbPropSpec:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des PropSpec-Felds in Bytes enthält.

**\_ cbChunk:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die maximale Anzahl von Bytes enthält, die der Absender in einer CPMFetchValueOut-Nachricht akzeptieren kann.

*Windows-Verhalten: Dieses Feld ist für alle Versionen von Windows auf 0x00004000 festgelegt.*

**PropSpec:** Eine CFullPropSpec-Struktur, die die abzurufende Eigenschaft angibt.

**\_ auffüllen:** Dieses Feld MUSS die erforderliche Länge (0 bis 3 Bytes) haben, um die Nachricht auf ein Vielfaches von 4 Bytes aufzufüllen. Der Wert der Auffüllungsbytes kann ein beliebiger Wert sein. Dieses Feld MUSS vom Empfänger ignoriert werden.

### <a name="22320-cpmfetchvalueout"></a>2.2.3.20 CPMFetchValueOut

Die CPMFetchValueOut-Nachricht antwortet auf eine CPMFetchValueIn-Nachricht mit einem Eigenschaftswert aus einer vorherigen Abfrage. Wie in Abschnitt 3.1.5.2.8 angegeben, wird diese Nachricht nach jeder CPMFetchValueIn-Nachricht gesendet, bis alle Bytes der Eigenschaft übertragen werden.

Das Format der CPMFetchValueOut-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cbValue

\_fMoreExists

\_fValueExists

vType

vValue (Variable)



 

**\_ cbValue:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtgröße in Bytes in vValue enthält.

**\_ fMoreExists:** Ein boolescher Wert, der angibt, ob zusätzliche CPMFetchValueOut-Meldungen verfügbar sind. Wenn 0x00000001 festgelegt ist, gibt es zusätzliche CPMFetchValueOut-Meldungen. Wenn 0x00000000 festgelegt ist, sind keine zusätzlichen CPMFetchValueOut-Meldungen verfügbar.

**\_ fValueExists:** Ein boolescher Wert, der angibt, ob ein Wert für die Eigenschaft vorhanden ist. Wenn 0x00000001 festgelegt ist, ist ein Wert für die Eigenschaft vorhanden. Wenn 0x00000000 festgelegt ist, ist kein Wert für die Eigenschaft vorhanden.

**vType:** Ein Wert aus der VARENUM-Enumeration. Ausführliche Informationen zum Typ der Eigenschaft finden Sie in Abschnitt 2.2.1.1.

**vValue:** Ein Teil eines Bytearrays, der eine SERIALIZEDPROPERTYVALUE-Struktur enthält, wie in Abschnitt 2.2.1.32 angegeben, wobei der Offset des Anfangs des Teils der Wert von \_ cbSoFar in CPMFetchValueIn ist. Die Länge des durch das cbValue-Feld angegebenen Teils \_ MUSS dem Wert von \_ cbChunk in CPMFetchValueIn entsprechen, wenn \_ fMoreExists auf 0x00000001 festgelegt ist, und MUSS andernfalls kleiner oder gleich dem Wert von \_ cbChunk sein.

### <a name="22321-cpmgetnotify"></a>2.2.3.21 CPMGetNotify

Die CPMGetNotify-Nachricht fordert an, dass der Client über Rowsetänderungen benachrichtigt werden soll.

Die Nachricht DARF KEINEN Text enthalten. nur der Nachrichtenheader gemäß Abschnitt 2.2.2 gesendet werden soll.

### <a name="22322-cpmsendnotifyout"></a>2.2.3.22 CPMSendNotifyOut

Die CPMSendNotifyOut-Nachricht benachrichtigt den Client über eine Änderung an den Ergebnissen einer Abfrage.

Diese Meldung wird nur gesendet, wenn eine Änderung auftritt. Das Format der CPMSendNotifyOut-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_watchNotify



 

**\_ watchNotify:** Die Änderung an der Abfrage. Es MUSS einer der folgenden Werte sein:



| Wert                                     | Bedeutung                                             |
|-------------------------------------------|-----------------------------------------------------|
| DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001     | Die Anzahl der Zeilen im Abfragerowset hat sich geändert. |
| DBWATCHNOTIFY \_ QUERYDONE 0x00000002       | Die Abfrage wurde abgeschlossen.                            |
| DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003 | Die Abfrage wurde erneut ausgeführt.                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a>2.2.3.23 CPMGetApproximatePositionIn

Die CPMGetApproximatePositionIn-Nachricht fordert die ungefähre Position eines Lesezeichens in einem Kapitel an. Das Format der CPMGetApproximatePositionIn-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_chapt

\_bmk



 

**\_ hCursor:** Ein 32-Bit-Wert, der den Abfragecursor darstellt, der aus CPMCreateQueryOut für das Rowset abgerufen wurde, das das Lesezeichen enthält.

**\_ chapt:** Ein 32-Bit-Wert, der das Handle für das Kapitel darstellt, das das Lesezeichen enthält.

**\_ bmk:** Ein 32-Bit-Wert, der das Handle für das Lesezeichen darstellt, für das die ungefähre Position abgerufen werden soll.

### <a name="22324-cpmgetapproximatepositionout"></a>2.2.3.24 CPMGetApproximatePositionOut

Die CPMGetApproximatePositionOut-Nachricht antwortet auf eine CPMGetApproximatePositionIn-Nachricht, die die ungefähre Position des Lesezeichens im Kapitel beschreibt. Das Format der CPMGetApproximatePositionOut-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Dividend

\_Divisor



 

**\_ numerator:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Zeilennummer des Lesezeichens im Rowset enthält. Wenn keine Zeilen vorhanden sind, MUSS dieses Feld auf 0x00000000.

**\_ Nenner:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeilen im Rowset enthält.

### <a name="22325-cpmcomparebmkin"></a>2.2.3.25 CPMCompareBmkIn

Die CPMCompareBmkIn-Nachricht fordert einen Vergleich zweier Lesezeichen in einem Kapitel an.

Das Format der CPMCompareBmkIn-Nachricht, die auf den Header folgt, lautet:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_chapt

\_bmkFirst

\_bmkSecond



 

\_**hCursor:** Ein 32-Bit-Wert, der das Handle der CPMCreateQueryOut-Nachricht für das Rowset darstellt, das die Lesezeichen enthält.

\_**chapt:** Ein 32-Bit-Wert, der das Handle des Kapitels darstellt, das die zu vergleichenden Lesezeichen enthält.

\_**bmkFirst:** Ein 32-Bit-Wert, der das Handle für das erste zu vergleichende Lesezeichen darstellt.

\_**bmkSecond:** Ein 32-Bit-Wert, der das Handle für das zweite zu vergleichende Lesezeichen darstellt.

### <a name="22326-cpmcomparebmkout"></a>2.2.3.26 CPMCompareBmkOut

Die CPMCompareBmkOut-Nachricht antwortet auf eine CPMCompareBmkIn-Nachricht mit dem Vergleich der beiden Lesezeichen im Kapitel. Das Format der CPMCompareBmkOut-Nachricht, die auf den Header folgt, lautet:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_dwComparison



 

\_**dwComparison:** Einer der folgenden Werte, der die relativen Positionen der beiden Lesezeichen im Kapitel angibt.



| Wert                               | Bedeutung                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| DBCOMPARE \_ LT 0x00000000            | Das erste Lesezeichen wird vor dem zweiten positioniert.               |
| DBCOMPARE \_ EQ 0x00000001            | Das erste Lesezeichen hat die gleiche Position wie das zweite.           |
| DBCOMPARE \_ GT 0x00000002            | Das erste Lesezeichen wird nach dem zweiten positioniert.                |
| DBCOMPARE \_ NE 0x00000003            | Das erste Lesezeichen hat nicht die gleiche Position wie das zweite. |
| DBCOMPARE \_ NOTCOMPARABLE 0x00000004 | Das erste Lesezeichen ist nicht mit dem zweiten vergleichbar.               |



 

### <a name="22327-cpmrestartpositionin"></a>2.2.3.27 CPMRestartPositionIn

Die CPMRestartPositionIn-Nachricht verschiebt die Abrufposition für einen Cursor an den Anfang des Kapitels. Wie in Abschnitt 3.1.5.2.12 angegeben, antworte der Server mit der gleichen Meldung, wobei die Ergebnisse der Anforderung im \_ Statusfeld des CISP-Headers enthalten sind.

Das Format der CPMRestartPositionIn-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor (optional)

\_chapt (optional)



 

**\_ hCursor:** Ein 32-Bit-Wert, der das Handle darstellt, das aus einer CPMCreateQueryOut-Nachricht abgerufen wurde und die Abfrage identifiziert, für die die Position neu gestartet werden soll. Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.

**\_ chapt:** Ein 32-Bit-Wert, der das Handle eines Kapitels darstellt, aus dem Zeilen abgerufen werden sollen. Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.

### <a name="22328-cpmfreecursorin"></a>2.2.3.28 CPMFreeCursorIn

Die CPMFreeCursorIn-Nachricht fordert die Freigabe eines Cursors an. Das Format der CPMFreeCursorIn-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor



 

**\_ hCursor:** Ein 32-Bit-Wert, der das Handle des Cursors aus der freizugebenden CPMCreateQueryOut-Nachricht darstellt.

### <a name="22329-cpmfreecursorout"></a>2.2.3.29 CPMFreeCursorOut

Die CPMFreeCursorOut-Nachricht antwortet auf eine CPMFreeCursorIn-Nachricht mit den Ergebnissen der Freigabe eines Cursors. Das Format der CPMFreeCursorOut-Nachricht, die dem Header folgt, lautet wie folgt:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cCursorsRemaining



 

**\_ cCursorsRemaining:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der cursors angibt, die noch für die Abfrage verwendet werden.

### <a name="22330-cpmdisconnect"></a>2.2.3.30 CPMDisconnect

Die CPMDisconnect-Nachricht beendet die Verbindung mit dem Server.

Die Nachricht DARF KEINEN Text enthalten. nur der Nachrichtenheader gemäß Abschnitt 2.2.2 gesendet werden soll.

### <a name="224-errors"></a>2.2.4 Fehler

Alle Content Indexing Service Protocol-Meldungen MÜSSEN bei Erfolg 0x00000000 zurückgeben. Andernfalls geben sie einen 32-Bit-Fehlercode ungleich 0 (null) zurück, der entweder ein HRESULT- oder ein NTSTATUS-Wert sein kann (siehe Abschnitt 1.8). Wenn ein Puffer zu klein für ein Ergebnis ist, MUSS der Statuscode STATUS \_ INSUFFICIENT \_ RESOURCES (0xC0000009A) zurückgegeben werden, und der fehlerhafte Vorgang sollte mit einem größeren Puffer wiederholt werden.

Alle anderen Fehlerwerte MÜSSEN gleich behandelt werden.

(Beachten Sie, dass sich die Nummerierungsräume HRESULT und NTSTATUS derzeit nur mit Werten mit identischer Bedeutung überschneiden. Selbst wenn sie in Zukunft konflikteig sein sollten, würde dies keine Protokollprobleme verursachen, solange der Wert für STATUS \_ INSUFFICIENT \_ RESOURCES bleibt eindeutig, da alle anderen Fehlerwerte gleich behandelt werden.)

## <a name="3-protocol-details"></a>3 Protokolldetails

-   [3.1 Serverdetails](#31-server-details)
-   [3.2 Clientdetails](#32-client-details)

CISP-Nachrichtenanforderungen zum Remoteabfragen der Indizierungsdienstkataloge erfordern keine bestimmte Sequenz. Es wird jedoch empfohlen, dass die höhere Ebene einer sinnvollen Nachrichtensequenz folgt, da der Server bei Nachrichten, die aus dieser Sequenz oder mit ungültigen Daten empfangen werden, mit einem Fehler antwortet. Einige Nachrichten sind auch von der höheren Ebene abhängig, die gültige Daten bereitstellt, die in Früheren Nachrichten in der Sequenz empfangen wurden.

Eine typische Nachrichtensequenz für eine einfache Abfrage von einem Client an einen Remotecomputer ist im folgenden Diagramm dargestellt.

![Nachrichtensequenz für einfache Abfragen](images/protocoldetails.jpg)

Die im vorherigen Diagramm dargestellten Nachrichten stellen eine Teilmenge aller CISP-Nachrichten dar, die zum Abfragen eines Remoteindizierungsdienstkatalogs verwendet werden.

### <a name="31-server-details"></a>3.1 Serverdetails

### <a name="311-abstract-data-model"></a>3.1.1 Abstraktes Datenmodell

Im folgenden Abschnitt werden Daten und der Zustand angegeben, die vom CISP-Server verwaltet werden. Die hier bereitgestellten Daten sollen die Erklärung des Verhaltens des Protokolls erleichtern. In diesem Abschnitt wird nicht vorausgesetzt, dass Implementierungen diesem Modell entsprechen, solange ihr externes Verhalten mit dem in diesem Dokument beschriebenen übereinstimmt.

Ein Indizierungsdienst, der CISP implementiert, MUSS die folgenden abstrakten Datenelemente verwalten:

-   Die Liste der Clients, die mit dem Server verbunden sind
-   Informationen zu jedem Client, einschließlich:
-   -   Clientversion (wie in der IN Abschnitt 2.2.3.6 angegebenen CPMConnectIn-Nachricht angegeben)
    -   Katalog, der dem Client zugeordnet ist (durch eine CPMConnectIn-Nachricht)
    -   Zusätzliche Clienteigenschaften, wie in Abschnitt 2.2.1.21.1 angegeben.
    -   Suchabfrage des Clients
    -   Liste der Cursorhandles für die Abfrage und Position im Resultset für jedes Handle.
    -   Aktueller Satz von Bindungen
    -   Aktueller Status der Abfrage, der (für jeden Cursor) enthält:
    -   -   Anzahl der Zeilen im Abfrageergebnis
        -   Zähler und Nenner des Abfrageabschlusses
        -   Letzte Anzahl von Zeilen, die von der letzten CPMRatioFinishedOut-Meldung für diesen Cursor gemeldet wurden
        -   Gibt an, ob die Abfrage vom Server auf Änderungen der Abfrageergebnisse überwacht wird und ob sie überwacht wird, welche Änderungen in den Abfrageergebnissen seit der letzten Clientmeldung durch CPMSendNotifyOut vorgenommen wurden.
        -   Liste der Kapitelhandles, die von dieser Abfrage an einen Client verarbeitet werden.
        -   Liste der Lesezeichenhandles für jeden Cursor, die von dieser Abfrage an einen Client bedient werden.

-   Der aktuelle Status des Indizierungsdiensts, der möglicherweise "nicht initialisiert", "wird ausgeführt" oder "heruntergefahren" ist. Beachten Sie, dass sich der Server größtenteils im Status "Wird ausgeführt" befindet. Im Folgenden ist das Zustandsautomatendiagramm für den Server dargestellt:

    ![Zustandsautomatendiagramm des Indizierungsdienstservers](images/abstractdatamodel.jpg)

-   Katalogspezifische Informationen: Anzahl indizierter Dokumente, Indexgröße, Anzahl eindeutiger Schlüssel usw. (eine vollständige Liste finden Sie in Abschnitt 2.2.3.1), Status (entspricht den Werten von dwNewState in Abschnitt 2.2.3.2).
-   Für jede unterstützte Sprache eine Datenbank mit Wortvariationen, wie in Abschnitt 2.2.1.3 erläutert.

### <a name="312-timers"></a>3.1.2 Zeitgeber

Es sind keine Protokollzeiter erforderlich.

### <a name="313-initialization"></a>3.1.3 Initialisierung

Nach der Initialisierung MUSS der Server seinen Zustand auf "nicht initialisiert" festlegen und mit dem Lauschen auf Nachrichten in der in Abschnitt 1.9 angegebenen Named Pipe beginnen. Nach jeder anderen internen Initialisierung MUSS sie in den Zustand "Wird ausgeführt" überwechseln.

### <a name="314-higher-layer-triggered-events"></a>3.1.4 Ausgelöste Ereignisse auf höherer Ebene

Keine.

### <a name="315-message-processing-and-sequencing-rules"></a>3.1.5 Nachrichtenverarbeitungs- und Sequenzierungsregeln

Wenn während der Verarbeitung einer von einem Client gesendeten Nachricht ein Fehler auftritt, MUSS der Server wie folgt einen Fehler an den Client melden:

-   Beenden der Verarbeitung der vom Client gesendeten Nachricht
-   Antworten Sie mit dem Nachrichtenheader (nur) der vom Client gesendeten Nachricht, und behalten Sie \_ dabei das msg-Feld bei.
-   Legen Sie \_ das Statusfeld auf den Fehlercodewert fest.

Wenn eine Nachricht eintrifft, MUSS der Server den Msg-Feldwert überprüfen, um zu überprüfen, ob es sich um einen bekannten Typ handelt \_ (siehe Abschnitt 2.2.2). Wenn der Typ nicht bekannt ist, MUSS er den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.

Der Server MUSS dann den \_ Feldwert ulChecksum überprüfen, wenn der Nachrichtentyp einer der folgenden ist:

-   CPMConnectIn (0x000000C8)
-   CPMCreateQueryIn (0x000000CA)
-   CPMSetBindingsIn (0x000000D0)
-   CPMGetRowsIn (0x000000CC)
-   CPMFetchValueIn (0x000000E4)

Um den ulChecksum-Feldwert zu überprüfen, MUSS der Server den Wert überprüfen, den der Client \_ im \_ Feld iClientVersion in der CPMConnectIn-Nachricht angegeben hat.

Wenn das Feld iClientVersion nicht auf 0x00000008 und das feld ulChecksum nicht auf 0x00000000 festgelegt ist, MUSS der Server einen \_ \_ STATUS INVALID PARAMETER \_ \_ (0xC000000D)-Fehler melden. Server MUST NOT validate the \_ ulChecksum field for clients the set the \_ iClientVersion field to a value less than 0x00000008.

Wenn der Feldwert iClientVersionfield 0x00000008 ist, MUSS der Server überprüfen, ob das feld ulChecksum wie in Abschnitt \_ \_ 3.2.4 angegeben berechnet wurde. Wenn der \_ ulChecksum-Wert ungültig ist, MUSS der Server den Fehler STATUS \_ INVALID PARAMETER \_ (0xC000000D) melden.

Als Nächstes überprüft der Server, in welchem Zustand er sich befindet. Wenn der Status "nicht initialisiert" ist, MUSS der Server einen CI \_ E \_ NOT \_ INITIALIZED(0x8004180B)-Fehler melden. Wenn der Status "heruntergefahren" ist, MUSS der Server einen CI \_ E \_ SHUTDOWN-Fehler (0x80041812 melden.

Sobald ein Header als gültig festgelegt wurde und sich der Server im Status "Wird ausgeführt" befing, MUSS eine weitere nachrichtenspezifische Verarbeitung erfolgen, wie in den folgenden Unterabschnitten angegeben.

### <a name="3151-remote-indexing-service-catalog-management"></a>3.1.5.1 Katalogverwaltung des Remoteindizierungsdiensts

### <a name="31511-receiving-a-cpmcistateinout-request"></a>3.1.5.1.1 Empfangen einer CPMCiStateInOut-Anforderung

Wenn der Server eine CPMCIStateInOut-Nachrichtenanforderung vom Client empfängt, MUSS der Server zunächst überprüfen, ob sich der Client in einer Liste verbundener Clients befindet. Wenn der Client nicht in der Liste enthalten ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden. Andernfalls MUSS er dem Client mit einer CPMCIStateInOut-Nachricht antworten und diese mit Informationen zum zugeordneten Katalog des Clients auffüllen, wie in Abschnitt 2.2.3.1 angegeben.

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a>3.1.5.1.2 Empfangen einer CPMSetCatStateIn-Anforderung

Wenn der Server eine CPMSetCatStateIn-Nachrichtenanforderung vom Client empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob der Client über Administratorzugriff verfügt. Wenn der Client keinen Administratorzugriff hat, MUSS der Server den Fehler STATUS \_ ACCESS \_ DENIED (0xC0000022) melden.
-   Wenn dwNewState nicht gleich CICAT ALL OPENED ist, ändern Sie den Status des Katalogs, der im Feld CatName angegeben ist, wie im \_ \_ Feld \_ \_ dwNewState angegeben. Weitere Informationen finden Sie in Abschnitt 2.2.3.2. Wenn der Server keinen Katalog mit dem im Feld CatName angegebenen Namen findet, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) zurückgeben.
-   Reagieren Sie auf den Client mit einer CPMSetCatStateOut-Meldung, wobei dwOldState auf den vorherigen Zustand des \_ Katalogs festgelegt werden muss. Wenn dwNewState gleich CICAT ALL OPENED ist, MUSS der Server den Status aller Kataloge überprüfen. Wenn alle Kataloge gestartet werden, muss dwOldState auf 0x00000001 und \_ \_ andernfalls \_ \_ \_ dwOldState auf 0x00000000.

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a>3.1.5.1.3 Empfangen einer CPMUpdateDocumentsIn-Anforderung

Wenn der Server eine CPMUpdateDocumentsIn-Nachrichtenanforderung empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob sich der Client in einer Liste verbundener Clients befindet (denen ein Katalog zugeordnet ist). Wenn der Client nicht in der Liste enthalten ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.
-   Überprüfen Sie, ob der Client über Administratorzugriff verfügt. Wenn der Client keinen Administratorzugriff auf den Server hat, MUSS der Server den Fehler STATUS \_ ACCESS \_ DENIED (0xC0000022) melden.
-   Beginnen Sie mit der Indizierung des vom Client angegebenen Pfads, und führen Sie je nach Wert des Flagfelds in der \_ CPMUpdateDocumentsIn-Nachricht eine vollständige oder inkrementelle Überprüfung durch. Wenn der Pfad zuvor nicht indiziert wurde, MUSS er der Auflistung der indizierten Speicherorte hinzugefügt und eine vollständige Überprüfung durchgeführt werden. Wenn ein unzulässiger Wert des Flagfelds angegeben wird, MUSS der Server so agieren, als ob das Flag auf UPD INIT festgelegt wurde, und \_ \_ eine vollständige Überprüfung \_ durchführen. Dieser Vorgang MUSS in dem Katalog ausgeführt werden, der dem Client zugeordnet ist.
-   Reagieren Sie mit dem Nachrichtenheader für CPMUpdateDocumentsIn auf den Client, und legen Sie das Statusfeld auf die \_ Ergebnisse der Anforderung fest.

### <a name="31514-receiving-a-cpmforcemergein-request"></a>3.1.5.1.4 Empfangen einer CPMForceMergeIn-Anforderung

Wenn der Server eine CPMForceMergeIn-Nachrichtenanforderung empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob sich der Client in einer Liste verbundener Clients befindet (denen ein Katalog zugeordnet ist). Wenn der Client nicht in der Liste enthalten ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.
-   Überprüfen Sie, ob der Client über Administratorzugriff verfügt. Wenn der Client keinen Administratorzugriff hat, MUSS der Server den Fehler STATUS \_ ACCESS \_ DENIED (0xC0000022) melden.
-   Starten Sie alle Wartungsprozesse, die erforderlich sind, um die Abfrageleistung für einen Katalog zu verbessern, der dem Client zugeordnet ist.
-   Reagieren Sie auf den Client mit einem Nachrichtenheader für CPMForceMergeIn, und legen Sie das Statusfeld auf die \_ Ergebnisse der Anforderung fest.

Beachten Sie, dass der Wartungsvorgang asynchron ist und fortgesetzt werden kann, nachdem der Client die Antwortnachricht empfangen hat. Dieser Prozess wirkt sich nicht direkt auf das Protokoll aus (mit Abkungszeit).

### <a name="3152-remote-indexing-service-querying"></a>3.1.5.2 Abfragen des Remoteindizierungsdiensts

### <a name="31521-receiving-a-cpmconnectin-request"></a>3.1.5.2.1 Empfangen einer CPMConnectIn-Anforderung

Wenn der Server eine CPMConnectIn-Anforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob sich der Client in der Liste der verbundenen Clients befindet. Wenn dies der Fall ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.
-   Überprüft, ob der angegebene Katalog vorhanden ist und sich nicht im Zustand "Beendet" befliegt. Wenn dies nicht der Fall ist, MUSS der Server einen CI \_ E \_ NO CATALOG \_ -Fehler (0x8004181D) melden.
-   Fügen Sie den Client der Liste der verbundenen Clients hinzu.
-   Ordnen Sie den Katalog dem Client zu.
-   Speichern Sie die in der CPMConnectIn-Nachricht übergebenen Informationen (z. B. Katalogname, Clientversion usw.) im Clientzustand.
-   Antworten Sie mit einer CPMConnectOut-Nachricht auf den Client.

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a>3.1.5.2.2 Empfangen einer CPMCreateQueryIn-Anforderung

Wenn der Server eine CPMCreateQueryIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob sich der Client in der Liste der verbundenen Clients befindet. Wenn dies nicht der Fall ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.
-   Überprüfen Sie, ob dem Client bereits eine Abfrage zugeordnet ist. Wenn dies der Fall ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.
-   Überprüfen Sie, ob sich der dem Client zugeordnete Katalog im Zustand befindet, der die Verarbeitung von Abfragen ermöglicht (CICAT \_ READONLY oder CICAT \_ WRITABLE). Wenn dies nicht der Fall ist, MUSS der Server einen QUERY \_ S \_ NO QUERY \_ (0x8004160C)-Fehler melden.
-   Analysieren Sie die in der Abfrage angegebenen Einschränkungssatz, Sortierreihenfolge und Gruppierungen. Wenn auf dem Server ein Fehler auftritt, MUSS er einen entsprechenden Fehler melden. Wenn dieser Schritt aus einem anderen Grund fehlschlägt, MUSS der Server den aufgetretenen Fehler melden. Informationen zu Indizierungsfehlern bei Dienstabfragen finden Sie unter \[ MSDN-QUERYERR \] .
-   Speichern Sie die Suchabfrage im Zustand für den Client.
-   Treffen Sie alle erforderlichen Vorbereitungen, um Zeilen an einen Client zu übergeben, und ordnen Sie die Abfrage den entsprechenden Cursorhandles zu (abhängig von den informationen, die in der CPMCreateQueryIn-Nachricht übergeben werden).
-   Fügen Sie diese Handles der Liste der Cursorhandles des Clients hinzu, und initialisieren Sie Listen mit Kapitelhandles und Lesezeichen.
-   Initialisieren der Liste der Kapitelhandles für jeden Cursor in dieser Abfrage auf DB \_ NULL \_ HCHAPTER
-   Initialisieren Sie die Liste der Lesezeichenhandles für jeden Cursor in dieser Abfrage auf einen Satz von DBBMK \_ FIRST und DBBMK \_ LAST.
-   Markieren Sie die Abfrage als nicht überwacht auf Änderungen.
-   Initialisieren Sie die Anzahl der Zeilen mit der derzeit berechneten Anzahl von Zeilen (die 0 sein kann, wenn die Abfrage nicht gestartet wurde, oder eine zahl, wenn die Abfrage ausgeführt wird), und initialisieren Sie den Zähler und Denominator des Abfrageabschlusses.
-   Reagieren Sie auf den Client mit einer CPMCreateQueryOut-Nachricht.

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a>3.1.5.2.3 Empfangen einer CPMGetQueryStatusIn-Anforderung

Wenn der Server eine CPMGetQueryStatusIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.
-   Überprüfen Sie, ob sich das Cursorhandle in einer Liste der Cursorhandles des Clients befindet. Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.
-   Bereiten Sie eine CPMGetQueryStatusOut-Nachricht vor. Der Server MUSS den aktuellen Abfragestatus abrufen und im Feld QStatus festlegen \_ (mögliche Werte finden Sie unter 2.2.3.11). Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.
-   Reagieren Sie mit der MELDUNG CPMGetQueryStatusOut auf den Client.

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a>3.1.5.2.4 Empfangen einer CPMGetQueryStatusExIn-Anforderung

Wenn der Server eine CPMGetQueryStatusExIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.
-   Überprüfen Sie, ob das übergebene Cursorhandle in einer Liste der Cursorhandles des Clients enthalten ist. Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.
-   Bereiten Sie eine CPMGetQueryStatusExOut-Nachricht vor. Der Server MUSS den aktuellen Abfragestatus und Abfragestatus abrufen und QStatus festlegen (mögliche Werte finden Sie unter 2.2.3.11), \_ dwRatioFinishedDenominator \_ bzw. dwRatioFinishedNumerator. Anschließend MUSS die Anzahl der Zeilen in den Abfrageergebnissen auf \_ cRowsTotal festgelegt werden. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.
-   Rufen Sie Informationen zum Clientkatalog ab, und geben Sie \_ cFilteredDocuments und \_ cDocumentsToFilter ein. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.
-   Rufen Sie die Position des Lesezeichens ab, die durch das Handle im \_ bmk-Feld angegeben wird, und füllen Sie das verbleibende \_ iRowBmk-Feld in der CPMGetQueryStatusExOut-Meldung aus. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.
-   Antworten Sie mit der CPMGetQueryStatusExOut-Meldung auf den Client.

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a>3.1.5.2.5 Empfangen einer CPMRatioFinishedIn-Anforderung

Wenn der Server eine CPMRatioFinishedIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.
-   Überprüfen Sie, ob das übergebene Cursorhandle in der Liste der Cursorhandles des Clients enthalten ist. Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.
-   Bereiten Sie eine CPMRatioFinishedOut-Nachricht vor. Der Server MUSS den Abfragestatus des Clients abrufen und \_ die Felder ulNumerator, \_ ulDenominator und \_ cRows ausfüllen. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.
-   Wenn \_ cRows gleich der letzten gemeldeten Anzahl von Zeilen für diese Abfrage ist, legen Sie \_ fNewRows auf 0x00000000 fest, andernfalls auf 0x00000001.
-   Aktualisieren Sie die zuletzt gemeldete Anzahl von Zeilen für diese Abfrage auf den Wert von \_ cRows.
-   Antworten Sie mit der Meldung CPMRatioFinishedOut auf den Client.

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a>3.1.5.2.6 Empfangen einer CPMSetBindingsIn-Anforderung

Wenn der Server eine CPMSetBindingsIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.
-   Überprüfen Sie, ob das übergebene Cursorhandle in der Liste der Cursorhandles des Clients enthalten ist. Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.
-   Vergewissern Sie sich, dass Bindungsinformationen gültig sind (d. h., die Spalte gibt mindestens den Wert, die Länge oder den Status an, der zurückgegeben werden soll, keine Überlappung der Bindungen für Wert, Länge oder Status, und Wert, Länge und Status passen in die angegebene Zeilengröße), und melden Sie andernfalls einen \_ DB E \_ BADBINDINFO-Fehler (0x80040E08).
-   Speichern Sie die Bindungsinformationen, die den im Feld aColumns angegebenen Spalten zugeordnet sind. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.
-   Reagieren Sie auf den Client mit einem Nachrichtenheader (nur), wobei \_ msg auf CPMSetBindingsIn und \_ der Status auf die Ergebnisse der angegebenen Bindung festgelegt ist.

### <a name="31527-receiving-a-cpmgetrowsin-request"></a>3.1.5.2.7 Empfangen einer CPMGetRowsIn-Anforderung

Wenn der Server eine CPMGetRowsIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.
-   Überprüfen Sie, ob sich das übergebene Cursorhandle in der Liste der Cursorhandles des Clients befindet. Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.
-   Überprüfen Sie, ob der Client über einen aktuellen Satz von Bindungen verfügt. Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.
-   Bereiten Sie eine CPMGetRowsOut-Nachricht vor. Der Server MUSS den Cursor wie in der Suchbeschreibung angegeben in Abfrageergebnissen positionieren. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.
-   Rufen Sie so viele Zeilen ab, wie in einen Puffer passen, dessen Größe durch \_ cbReadBuffer angegeben wird, aber nicht mehr als durch \_ cRowsToTransfer angegeben. Beim Abrufen von Zeilen MUSS der Server den Eigenschaftswerttyp jeder ausgewählten Spalte mit dem Typ vergleichen, der im aktuellen Bindungssatz des Clients (Abschnitt 3.1.1) angegeben ist. Wenn der Typ in der Bindung nicht VT \_ VARIANT ist, MUSS der Server versuchen, den Eigenschaftswert der Spalte in diesen Typ zu konvertieren. Andernfalls MUSS der Eigenschaftswert in seinem normalen Typ zurückgegeben werden, wenn das DBPROP \_ USEEXTENDEDDBTYPES-Flag im DBPROPSET \_ QUERYEXT-Eigenschaftensatz des Clients festgelegt ist oder wenn der Eigenschaftswert der Spalte kein VT \_ VECTOR-Typ ist. Wenn keines davon der Fall ist (d. h. der Server hat einen VT \_ VECTOR-Typ, und der Client unterstützt VT \_ VECTOR nicht), MUSS der Server versuchen, ihn wie folgt in einen \_ VT ARRAY-Typ zu konvertieren: VT \_ I8, VT \_ UI8, VT \_ FILETIME und VT \_ CLSID Array-Elemente können nicht konvertiert werden und schlagen stattdessen fehl. VT \_ LPSTR- und VT \_ LPWSTR-Arrayelemente MÜSSEN in VT BSTR konvertiert \_ werden. Arrayelemente aller anderen Typen MÜSSEN unverändert bleiben. Wenn Zeilenspalten Kapitelhandles oder Lesezeichenhandles enthalten, MUSS der Server die entsprechenden Listen aktualisieren. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.
-   Speichern Sie die tatsächliche Anzahl der abgerufenen Zeilen in \_ cRowsReturned.
-   Kopieren Sie die Suchbeschreibung und das Kapitelfeld aus CPMGetRowsIn in eine zu sendende CPMGetRowsOut-Nachricht.
-   Speichern Sie abgerufene Zeilen im Feld Rows (siehe Hinweis zum Status byte unten und Abschnitt 2.2.3.16 zur Struktur des Rows-Felds).
-   Antworten Sie mit der CPMGetRowsOut-Meldung auf den Client.

Hinweis zum Status-Bytefeld:

Wenn StatusUsed auf 0x01 in CTableColumn der CPMSetBindingIn-Nachricht für die Spalte festgelegt ist, MUSS der Server das Status byte (das sich am Anfang der Zeile unter StatusOffset befindet) für diese Spalte auf einen der folgenden Werte festlegen:



| Wert | Bedeutung        |
|-------|----------------|
| 0x00  | StatusOK       |
| 0x01  | StatusDeferred |
| 0x02  | StatusNull     |



 

Wenn der Eigenschaftswert für diese Zeile nicht vorhanden ist, MUSS der Server das Status-Byte auf StatusNull festlegen. Wenn der Wert zu groß ist, um in der CPMGetRowsOut-Nachricht übertragen zu werden, MUSS der Server das Status-Byte auf StatusDeferred festlegen. Andernfalls MUSS der Server das Status-Byte auf StatusOK festlegen.

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a>3.1.5.2.8 Empfangen einer CPMFetchValueIn-Anforderung

Wenn der Server eine CPMFetchValueIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.
-   Bereiten Sie eine CPMFetchValueOut-Nachricht vor. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.
-   Suchen Sie das durch das Feld wid angegebene Dokument, \_ und überprüfen Sie, ob die Eigenschaften-ID für dieses Dokument (später als "Eigenschaftswert" bezeichnet) durch die PropSpec-Struktur für diesen Client verfügbar ist. Wenn dieser Wert nicht verfügbar ist, MUSS der Server \_ fValueExists auf 0x00000000 und andernfalls \_ fValueExists auf 0x00000001 festlegen. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.
-   Wenn \_ fValueExists gleich 0x00000001 MUSS der Server folgende Schritte ausführen:
-   -   Serialisieren Sie den Eigenschaftswert in eine SERIALIZEDPROPERTYVALUE-Struktur, und kopieren Sie ab dem \_ cbSoFar-Offset \_ höchstens cbChunk-Bytes (jedoch nicht hinter dem Ende der serialisierten Eigenschaft) in das vValue-Feld. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.
    -   Legen Sie cbValue auf die Anzahl der Bytes fest, \_ die im vorherigen Schritt kopiert wurden.
    -   Legen Sie vType auf den Eigenschaftstyp des Eigenschaftswerts fest.
    -   Wenn die Länge der serialisierten Eigenschaft größer als \_ cbSoFar \_ ist, die cbValue hinzugefügt wurde, legen Sie \_ fMoreExists auf 0x00000001 fest, andernfalls auf 0x00000000.

-   Reagieren auf den Client mit der CPMFetchValueOut-Meldung

### <a name="31529-receiving-a-cpmgetnotify-request"></a>3.1.5.2.9 Empfangen einer CPMGetNotify-Anforderung

Wenn der Server eine CPMGetNotify-Nachricht von einem Client empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.
-   Wenn seit der letzten CPMSendNotifyOut-Nachricht für diesen Client keine Änderungen am Abfrageresultset vorgenommen wurden oder die Abfrage derzeit nicht auf Änderungen im Resultset überwacht wird, MUSS der Server mit der CPMGetNotify-Meldung antworten und damit beginnen, die Abfrage auf Änderungen im Resultset zu überwachen. Wenn das Abfrageergebnisset zu einem späteren Zeitpunkt geändert wird, MUSS der Server genau eine CPMSendNotifyOut-Nachricht an den Client senden und DIE Änderung im \_ Feld watchNotify angeben.
-   Wenn seit der letzten CPMSendNotifyOut-Nachricht Änderungen am Abfrageresultset vorgenommen wurden, MUSS der Server mit CPMSendNotifyOut antworten und DIE Änderung im \_ Feld watchNotify angeben. Beachten Sie, dass DBWATCHNOTIFY ROWSCHANGED bei vielen Änderungen an den Abfrageergebnissen \_ Priorität hat (d. h., wenn die Abfrage durchgeführt, erneut ausgeführt und dann die Anzahl der Geänderten Zeilen und die Abfrage erneut durchgeführt wurden, lautet das gemeldete Ereignis DBWATCHNOTIFY \_ ROWSCHANGED).

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a>3.1.5.2.10 Empfangen einer CPMGetApproximatePositionIn-Anforderung

Wenn der Server eine CPMGetApproximatePositionIn-Nachrichtenanforderung vom Client empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.
-   Überprüfen Sie, ob das Cursorhandle, das Kapitelhandle und das übergebene Lesezeichenhandle in den entsprechenden Listen enthalten sind. Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.
-   Suchen Sie eine Zeile, die dem Lesezeichenhandle in den Abfrageergebnissen zugeordnet ist, und ermitteln Sie die Position der Zeile im Rowset, auf die das Kapitelhandle verweist, und bestimmen Sie den Zähler und Nenner für die Position. Beachten Sie, dass das entsprechende Kapitel das Hauptrowset der Abfrage ist, wenn das Kapitelhandle DB \_ NULL \_ HCHAPTER ist. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.
-   Reagieren Sie auf den Client mit einer CPMFetchValueOut-Meldung.

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a>3.1.5.2.11 Empfangen einer CPMCompareBmkIn-Anforderung

Wenn der Server eine CPMCompareBmkIn-Nachrichtenanforderung vom Client empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.
-   Überprüfen Sie, ob die übergebenen Cursorhandles, Kapitelhandles und Lesezeichenhandles in entsprechenden Listen enthalten sind. Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.
-   Bereiten Sie eine CPMCompareBmkOut-Nachricht vor.
-   Wenn Lesezeichenhandles gleich sind, \_ muss dwComparison AUF DBCOMPARE EQ festgelegt \_ sein.
-   Wenn eines der Lesezeichenhandles DBBMK \_ FIRST oder DBBMK \_ LAST ist, muss \_ dwComparison auf DBCOMPARE NE festgelegt \_ werden.
-   Andernfalls MUSS der Server folgende Schritte ausführen:
-   -   Suchen von Zeilen, auf die von jedem Lesezeichenhandle in den Abfrageergebnissen verwiesen wird
    -   Wenn sich eine der Zeilen nicht im Kapitel befindet, das vom Kapitelhandle in CPMCompareBmkIn angegeben wird, \_ muss dwComparison auf DBCOMPARE \_ NOTCOMPARABLE festgelegt werden.
    -   Wenn sich beide Zeilen im selben Kapitel befinden, MUSS der Server eine Ungefährung der Position dieser Zeilen im Rowset herstellen, auf das im Handle dieses Kapitels verwiesen wird. Anschließend MÜSSEN Positionswerte verglichen und \_ dwComparison auf DBCOMPARE LT festgelegt \_ werden, wenn die Position der ersten Zeile kleiner als die Position der zweiten Zeile ist. Andernfalls \_ MUSS dwComparison auf DBCOMPARE GT festgelegt \_ werden.

-   Reagieren Sie auf den Client mit einer ausgefüllten CPMCompareBmkOut-Nachricht.

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a>3.1.5.2.12 Empfangen einer CPMRestartPositionIn-Anforderung

Wenn der Server die CPMRestartPositionIn-Nachrichtenanforderung vom Client empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.
-   Überprüfen Sie, ob das Cursorhandle und das übergebene Kapitelhandle in den entsprechenden Listen enthalten sind. Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.
-   Bewegen Sie den Cursor an den Anfang des Kapitels, der durch das Kapitelhandle identifiziert wird. Beachten Sie, dass das entsprechende Kapitel das Hauptrowset der Abfrage ist, wenn das Kapitelhandle DB \_ NULL \_ HCHAPTER ist. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.
-   Reagieren Sie mit einer CPMRestartPositionIn-Nachricht auf den Client.

### <a name="315213-receiving-a-cpmfreecursorin-request"></a>3.1.5.2.13 Empfangen einer CPMFreeCursorIn-Anforderung

Wenn der Server eine CPMFreeCursorIn-Nachrichtenanforderung vom Client empfängt, MUSS der Server folgende Schritte ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.
-   Überprüfen Sie, ob das übergebene Cursorhandle in der Liste der Cursorhandles des Clients enthalten ist. Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.
-   Geben Sie den Cursor und die zugehörigen Ressourcen (eine vollständige Liste finden Sie in Abschnitt 3.1.1) für dieses Cursorhandle frei.
-   Entfernen Sie den Cursor aus der Liste der Cursor für diesen Client.
-   Antworten Sie mit einer CPMFreeCursorOut-Nachricht, und legen Sie das \_ Feld cCursorsRemaining mit der Anzahl der verbleibenden Cursor fest. in der Liste dieses Clients.
-   Wenn für diesen Client keine Cursor mehr vorhanden sind, MUSS der Server die Abfrage und die zugehörigen Ressourcen freigeben (siehe Abschnitt 3.1.1).

### <a name="315214-receiving-a-cpmdisconnect-request"></a>3.1.5.2.14 Empfangen einer CPMDisconnect-Anforderung

Wenn der Server eine CPMDisconnect-Nachrichtenanforderung vom Client empfängt, MUSS der Server den Client aus der Liste der verbundenen Clients entfernen und alle ressourcen freigeben, die dem Client zugeordnet sind.

### <a name="316-timer-events"></a>3.1.6 Timerereignisse

Keine.

### <a name="317-other-local-events"></a>3.1.7 Andere lokale Ereignisse

Wenn der Server beendet wird, MUSS er zuerst in den Zustand "Herunterfahren" übergehen. Sie MUSS dann die Überwachung der Pipe beenden, alle anderen implementierungsspezifischen Aufgaben zum Herunterfahren ausführen und dann in den Zustand "Beendet" übergehen.

### <a name="32-client-details"></a>3.2 Clientdetails

### <a name="321-abstract-data-model"></a>3.2.1 Abstraktes Datenmodell

Im folgenden Abschnitt werden die Daten und der Status angegeben, die vom Client des Content Indexing Service Protocol verwaltet werden. Die bereitgestellten Daten sollen die Erklärung des Verhaltens des Protokolls erleichtern. In diesem Abschnitt wird nicht vorausgesetzt, dass Implementierungen diesem Modell entsprechen, solange ihr externes Verhalten mit dem in diesem Dokument beschriebenen übereinstimmt.

Ein Client weist den folgenden abstrakten Zustand auf:

-   **Letzte gesendete Nachricht:** Eine Kopie der letzten an den Server gesendeten Nachricht.
-   **Aktueller Eigenschaftswert:** Ein Teilwert einer "verzögerten" Eigenschaft, die gerade abgerufen wird.
-   **Aktuelle empfangene Bytes:** Die Anzahl der bytes, die bisher für den aktuellen Eigenschaftswert empfangen wurden.
-   **Named Pipe-Verbindungsstatus:** Eine Verbindung mit dem Server

### <a name="322-timers"></a>3.2.2 Timer

Es sind keine Protokolltimer erforderlich.

### <a name="323-initialization"></a>3.2.3 Initialisierung

Es werden keine Aktionen ausgeführt, bis eine Anforderung auf höherer Ebene empfangen wird.

### <a name="324-higher-layer-triggered-events"></a>3.2.4 Higher-Layer Ausgelöste Ereignisse

Wenn eine Anforderung von einer höheren Ebene empfangen wird, MUSS der Client unter Verwendung der in Abschnitt 2.1 angegebenen Details eine Named Pipe-Verbindung mit dem Server herstellen. Wenn dies nicht möglich ist, MUSS bei der Anforderung der höheren Ebene ein Fehler aufgetreten sein. Das heißt, bei einem Verbindungsfehler liegt es in der Verantwortung der höheren Ebene, dies bei Bedarf erneut zu versuchen.

Ein Header MUSS mit Feldern vorangestellt werden, die wie in Abschnitt 2.2.2 angegeben festgelegt sind.

Für Nachrichten, für die angegeben wird, dass eine Prüfsumme ungleich 0 (null) erforderlich ist, MUSS der \_ ulChecksum-Wert wie folgt berechnet werden:

1.  Der Inhalt der Nachricht nach dem \_ ulReserved2-Feld im Nachrichtenheader MUSS als Sequenz von 32-Bit-Ganzzahlen interpretiert werden. Der Client MUSS die Summe der numerischen Werte berechnen, die von diesen ganzen Zahlen angegeben werden.
2.  Berechnen Sie den bitweisen XOR dieses Werts mit 0x59533959.
3.  Subtrahieren Sie den von msg angegebenen Wert \_ von dem Wert, der sich aus dem bitweisen XOR ergibt.

### <a name="3241-remote-indexing-service-catalog-management"></a>3.2.4.1 Katalogverwaltung des Remoteindizierungsdiensts

Jede Nachricht wird durch eine Anforderung von der höheren Ebene ausgelöst. Es wird keine Nachrichtensequenz vom Client für CISP-Nachrichtenanforderungen zur Remoteverwaltung von Katalogen erzwungen, aber (mit Ausnahme einer CPMSetCatStateIn-Nachricht) antwortet der Server nur dann mit Erfolg, wenn der Client zuvor über eine CPMConnectIn-Nachricht eine Verbindung hergestellt hat.

### <a name="32411-sending-a-cpmcistateinout-request"></a>3.2.4.1.1 Senden einer CPMCiStateInOut-Anforderung

In der Regel fordert die höhere Ebene den Protokollclient auf, eine CPMCiStateInOut-Nachricht zu senden, wenn informationen zum Indizieren von Diensten auf dem Server erforderlich sind.

Wenn der Client aufgefordert wird, diese Nachricht zu senden, MUSS er folgende Schritte ausführen:

-   Senden Sie eine CPMCiStateInOut-Nachricht wie in Abschnitt 2.2.3.1 angegeben an den Server.
-   Warten Sie, bis die CPMCiStateInOut-Nachricht vom Server empfangen wird, und verwerfen Sie automatisch alle anderen Nachrichten.
-   Melden Sie den Wert des \_ Statusfelds der Antwort, und wenn dies erfolgreich war, wird die Informationsstruktur wieder auf die höhere Ebene zurückgestellt.

### <a name="32412-sending-a-cpmsetcatstatein-request"></a>3.2.4.1.2 Senden einer CPMSetCatStateIn-Anforderung

In der Regel fordert die höhere Ebene den Protokollclient auf, eine CPMSetCatStateIn-Nachricht zu senden, wenn Informationen über einen Katalog oder den gesamten Katalog erforderlich sind. Für diese Nachricht muss die höhere Ebene dem Protokollclient einen Wert für \_ dwNewState und ggf. den Namen des Katalogs bereitstellen.

Wenn der Client aufgefordert wird, diese Nachricht zu senden, MUSS er folgende Schritte ausführen:

-   Senden Sie eine CPMSetCatStateIn-Nachricht wie in 2.2.3.2 angegeben an den Server.
-   Warten Sie, bis eine CPMSetCatStateOut-Nachricht vom Server empfangen wird, und verwerfen Sie automatisch alle anderen Nachrichten.
-   Melden Sie den Wert des \_ Statusfelds der Antwort, und wenn dies erfolgreich war, wird \_ dwOldState wieder auf die höhere Ebene zurückgesetzt.

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a>3.2.4.1.3 Senden einer CPMUpdateDocumentsIn-Anforderung

Die höhere Ebene fordert in der Regel zum Senden dieser Nachricht auf, wenn dokumente im vorhandenen Pfad aktualisiert oder dem Index ein neuer Dateipfad hinzugefügt werden muss. Daher besteht die höhere Ebene darin, den Pfad und den Typ eines Scans bereitzustellen, wie in Abschnitt 2.2.3.4 angegeben, wobei ein inkrementelles oder vollständiges Update für vorhandene Pfade und neue Initialisierung für neue Pfade vorgesehen ist.

Um die Anforderung der höheren Ebene zu erfüllen, MUSS der Client folgende Schritte ausführen:

-   Senden Sie eine CPMUpdateDocumentsIn-Nachricht wie in Abschnitt 2.2.3.4 angegeben an den Server.
-   Warten Sie auf den Empfang der CPMUpdateDocumentsIn-Nachricht vom Server, und verwerfen Sie alle anderen Nachrichten im Hintergrund.
-   Melden Sie den Wert des \_ Statusfelds der Antwort an die höhere Ebene zurück.

### <a name="32414-sending-a-cpmforcemergein-request"></a>3.2.4.1.4 Senden einer CPMForceMergeIn-Anforderung

In der Regel fordert die höhere Ebene an, diese Nachricht zu senden, wenn die Abfrageleistung verbessert werden muss oder dies Teil der geplanten Wartung des Indizierungsdiensts ist.

Um die höhere Ebene zu bedienen, MUSS der Client Folgendes tun:

-   Senden Sie die CPMForceMergeIn-Nachricht gemäß Abschnitt 2.2.3.5 an den Server.
-   Warten Sie auf den Empfang einer CPMUpdateDocumentsIn-Nachricht vom Server, und verwerfen Sie alle anderen Nachrichten im Hintergrund.
-   Melden Sie den Wert des \_ Statusfelds der Antwort an die höhere Ebene zurück.

### <a name="3242-remote-indexing-service-catalog-query-messages"></a>3.2.4.2 Abfragenachrichten des Remoteindizierungsdienstkatalogs

Mit Ausnahme von CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut besteht eine 1:1-Beziehung zwischen CISP-Nachrichten und Anforderungen höherer Ebene. Für die beiden oben genannten Ausnahmen können vom Client mehrere Nachrichten generiert werden, um entweder die Größenanforderungen zu erfüllen oder eine vollständige Eigenschaft abzurufen. Die höhere Ebene verfolgt in der Regel alle abfragespezifischen Informationen nach (z. B. geöffnete Cursorhandles, rechtliche Werte für Lesezeichen- und Kapitelhandles, wid-Werte für verzögerte Eigenschaftswerte usw.) und verfolgt auch nach, ob sich der Client in einem verbundenen Zustand befindet. Dies wird jedoch nicht vom Client erzwungen.

Zur Veranschaulichung veranschaulicht der Clientteil des Diagramms in Abschnitt 3 diese Sequenz für eine einfache Abfrage des Indizierungsdiensts.

### <a name="32421-sending-a-cpmconnectin-request"></a>3.2.4.2.1 Senden einer CPMConnectIn-Anforderung

Diese Meldung ist in der Regel die erste Anforderung von der höheren Ebene (wenn der Client nicht verbunden ist, tritt auf dem Server ein Fehler bei den meisten Nachrichten mit Ausnahme von CPMSetCatStateIn auf). Die höhere Ebene stellt dem Protokollclient Informationen zur Verfügung, die für die Verbindung erforderlich sind.

Um die höhere Ebene zu bedienen, MUSS der Client Folgendes tun:

-   Füllen Sie die Nachricht mithilfe der Informationen aus, die der Client der höheren Ebene bereitgestellt hat (siehe Abschnitt 2.2.3.6) in \_ iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 und aPropertySet.
-   Legen \_ Sie fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet und cExtPropSet wie in 2.2.3.6 angegeben fest.
-   Legen Sie die Prüfsumme im \_ Feld ulChecksum fest.
-   Senden Sie die CPMConnectIn-Nachricht an den Server.
-   Warten Sie auf den Empfang einer CPMConnectOut-Nachricht vom Server, und verwerfen Sie alle anderen Nachrichten im Hintergrund.
-   Melden Sie den Wert des Statusfelds der Antwort und, falls erfolgreich, die \_ \_ serverVersion zurück zur höheren Ebene.

Zu Informationszwecken wird erwartet, dass höhere Ebenen bei erfolgreicher Verbindung in der Regel die folgenden Aktionen ausführen, diese jedoch nicht vom CISP-Client erzwungen werden:

-   Verwenden von Katalogverwaltungsmeldungen des Remoteindizierungsdiensts für Verwaltungsaufgaben
-   Verwenden Sie eine CPMCreateQueryIn-Anforderung, um eine Suchabfrage zum Abrufen von Ergebnissen aus dem Katalog zu erstellen.

### <a name="32422-sending-a-cpmcreatequeryin-request"></a>3.2.4.2.2 Senden einer CPMCreateQueryIn-Anforderung

Die höhere Ebene stellt in der Regel Informationen für die Abfrageerstellung zur Verfügung, sobald der Protokollclient verbunden ist. Die höhere Ebene stellt dem Client einen Einschränkungssatz, einen Spaltensatz, Sortierreihenfolgeregeln und einen Kategorisierungssatz (jede davon kann weggelassen werden), Rowseteigenschaften und die Struktur des Eigenschaften-ID-Mappers zur Verwendung.

Wenn diese Anforderung von einer höheren Ebene empfangen wird, MUSS der Client Folgendes tun:

-   Bereiten Sie ein CPMCreateQueryOut wie folgt vor.
-   -   Wenn ein Spaltensatz vorhanden ist, legen Sie CColumnsSetPreset auf 0x01 und füllen Sie das Feld ColumnsSet aus.
    -   Wenn Einschränkungen vorhanden sind, legen Sie CRestrictionPresent auf 0x01 und füllen Sie das Feld Einschränkung aus.
    -   Wenn eine Sortierreihenfolge vorhanden ist, füllen Sie das Feld SortSet aus.
    -   Wenn ein Kategorisierungssatz vorhanden ist, legen Sie CSortSetPresent auf 0x01 und füllen Sie das Feld CategorizationSet aus.
    -   Legen Sie die restlichen Felder wie in 2.2.3.8 angegeben fest.

-   Berechnen \_ Sie das ulCheckSum-Feld im Header.
-   Senden Sie die Nachricht CPMCreateQueryIn an den Server.
-   Warten Sie auf den Empfang der CPMCreateQueryOut-Nachricht (siehe Details in Abschnitt 3.2.5.1.1), und verwerfen Sie alle anderen Nachrichten im Hintergrund.
-   Melden Sie den Wert des Statusfelds der Antwort und, falls erfolgreich, das Array von Cursorhandles und informative boolesche Werte \_ (wie in 2.2.3.9 angegeben) zurück zur höheren Ebene.

### <a name="32423-sending-a-cpmsetbindingsin-request"></a>3.2.4.2.3 Senden einer CPMSetBindingsIn-Anforderung

In der Regel werden von der höheren Ebene Bindungen für jede Spalte festgelegt, die in den Zeilen zurückgegeben wird, wenn sie bereits über ein gültiges Cursorhandl verfügt (siehe Abschnitt 3.2.5.1.1, nachdem CPMCreateQueryOut erfolgreich empfangen wurde). Von der höheren Wird erwartet, dass sie ein Array von CTableColumn-Strukturen für das Feld aColumns und ein gültiges Cursorhand handle bereitstellen, wie in Abschnitt 2.2.4.31 angegeben.

Wenn diese Anforderung von der höheren Ebene empfangen wird, MUSS der Client Folgendes tun:

-   Berechnen Sie die Anzahl der CTableColumn-Strukturen im Array aColumns, und legen Sie das Feld cColumns auf diesen Wert fest.
-   Berechnen Sie die Gesamtgröße der Felder cColumns und aColumns in Bytes, und legen Sie das \_ Feld cbBindingDesc auf diesen Wert fest.
-   Legen Sie die angegebenen Felder in der CPMSetBindingsIn-Nachricht auf die Werte fest, die von der höheren Anwendungsschicht bereitgestellt werden. Legen Sie \_ das feld ulChecksum auf den wert fest, der gemäß Abschnitt 3.2.5 berechnet wird.
-   Senden Sie die fertige CPMSetBindignsIn-Nachricht an den Server.
-   Warten Sie auf den Empfang einer CPMSetBindingsIn-Nachricht vom Server, und verwerfen Sie andere Nachrichten.
-   Geben Sie den Status aus \_ dem Statusfeld der Antwort an die höhere Ebene an.

Aus informativen Gründen wird erwartet, dass höhere Ebenen in der Regel einen Client zum Senden einer CPMGetRowsIn-Nachricht anfordern, dies wird jedoch nicht durch das Content Indexing Service-Protokoll erzwungen.

### <a name="32424-sending-a-cpmgetrowsin-request"></a>3.2.4.2.4 Senden einer CPMGetRowsIn-Anforderung

Wenn die höhere Ebene Zeileninformationen empfangen möchte, stellt sie dem Protokollclient ein gültiges Cursor- und Kapitelhand handle und eine entsprechende Suchbeschreibung zur Verfügung. In der Regel wird eine höhere Ebene erwartet, wenn sie über einen gültigen Cursor und/oder Kapitelhandpunkt verfügt und die Bindungen mit der CPMSetBindingsIn-Nachricht festgelegt wurden. Für den Zugriff auf das Rowset in einem Kapitel ist die höhere Ebene die Verwendung des Kapitelhandlings, das vom Server in einer vorherigen CPMGetRowsOut-Nachricht empfangen wurde.

Wenn diese Anforderung von der höheren Ebene empfangen wird, MUSS der Client Folgendes tun:

-   Bestimmen Sie, welcher ganzzahlige Wert ohne Vorzeichen für das \_ Feld cbReadBuffer angegeben werden soll. Um diesen Wert zu bestimmen, MUSS der Client den maximal folgenden Wert verwenden:
-   -   Das Tausendfache des Werts des Felds c \_ RowsToTransfer.
    -   Wert von \_ cbRowWidth, aufgerundet auf das nächste 512-Byte-Vielfache.
    -   Nehmen Sie den höheren dieser beiden Werte bis zum Grenzwert von 16.000.
    -   In Fällen, in denen eine einzelne Zeile größer als 16.000 ist, kann der Server keine Ergebnisse an diese Abfrage zurückgeben.

Geben Sie eine Clientbasis für Zeilendaten variabler Größe im Clientadressenraum im \_ Feld ulClientBase an.

*Windows-Verhalten: Bei einem 32-Bit-Client, der mit einem 32-Bit-Server spricht, oder einem 64-Bit-Client, der mit einem 64-Bit-Server spricht, wird dieser Wert auf eine Speicheradresse des empfangenden Puffers im Anwendungsprozess festgelegt. Dadurch können Zeiger, die im Rows-Feld von CPMGetRowsOut empfangen werden, richtige Speicherzeige in einem Clientanwendungsprozess sein. Andernfalls wird sie auf 0x00000000.*

-   Berechnen Sie die Größe der Suchbeschreibung, und legen Sie sie im \_ Feld cbSeek fest.
-   Legen Sie den Wert von cbReserved (der als Offset für Zeilenstart fungieren würde) auf den Wert \_ cbSeek plus 0x14.
-   Senden Sie eine CPMConnectIn-Nachricht wie in 2.2.3.15 angegeben an den Server.

### <a name="32425-sending-a-cpmfetchvaluein-request"></a>3.2.4.2.5 Senden einer CPMFetchValueIn-Anforderung

Wenn der Client eine CPMGetRowsOut-Antwort vom Server empfängt, bei der das Feld Status der Spalte auf StatusDeferred (0x01) festgelegt ist, bedeutet dies, dass der Eigenschaftswert nicht im Feld Zeilen der CPMGetRowsOut-Nachricht enthalten war. In diesem Fall fordert die höhere Ebene den Protokollclient in der Regel auf, den Wert mithilfe der CPMFetchValueIn-Nachricht abzurufen, und stellt den PropSpec- und wid-Wert für eine verzögerte Eigenschaft zur Anwendung, die der Protokollclient in der ersten \_ CPMFetchValueIn-Nachricht verwenden muss.

Wenn dies die erste CPMFetchValueIn-Nachricht ist, die der Client gesendet hat, um die angegebene Eigenschaft an fordern, MUSS der Client Folgendes tun:

-   Legen Sie alle Felder in einer Nachricht wie in Abschnitt 2.2.3.19 angegeben fest.
-   Legen \_ Sie cbSoFar auf 0x00000000.
-   Legen Sie Aktuelle empfangene Bytes auf 0 fest.
-   Senden Sie die CPMFetchValueIn-Nachricht an den Server.

### <a name="32426-sending-a-cpmfreecursorin-request"></a>3.2.4.2.6 Senden einer CPMFreeCursorIn-Anforderung

Sobald die höhere Ebene die Suchabfrage nicht mehr verwendet, kann sie die Ressourcen auf dem Server frei geben, indem der Client aufgefordert wird, eine CPMFreeCursorIn-Nachricht zu senden.

Wenn diese Anforderung empfangen wird, MUSS der Client eine CPMFreeCursorIn-Nachricht wie in 2.2.3.28 angegeben an den Server senden, die das von der oberen Ebene angegebene Handle enthält.

### <a name="32427-sending-a-cpmdisconnect-message"></a>3.2.4.2.7 Senden einer CPMDisconnect-Nachricht

Wenn die höhere Ebene keine Abfragen mehr für den Indizierungsdienst enthält, fordert die Anwendung möglicherweise an, dass der Client eine CPMDisconnect-Nachricht an den Server sendet, um weitere Serverressourcen frei zu geben. Wenn diese Abfrage empfangen wird, MUSS der Client die Nachricht einfach wie angefordert senden. Es gibt keine Antwort auf diese Nachricht vom Server.

### <a name="325-message-processing-and-sequencing-rules"></a>3.2.5 Nachrichtenverarbeitungs- und Sequenzierungsregeln

Wenn der Client eine Nachrichtenantwort vom Server empfängt, MUSS der Client die zuletzt gesendete Nachricht verwenden, um zu bestimmen, ob es sich bei der vom Server empfangenen Nachricht um die vom Client erwartete Nachricht handelt. Alle Nachrichten mit \_ einem msg-Feld, die sich von dem unter Letzte Sendenachricht unterscheiden, MÜSSEN ignoriert werden.

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a>3.2.5.1 Empfangen einer CPMCreateQueryOut-Antwort

Wenn der Client eine CPMCreateQueryOut-Meldungsantwort vom Server empfängt, MUSS der Client den Status zurückgeben und (wenn der Status erfolgreich ist) Cursorhandlwerte wieder auf eine höhere \_ Ebene verarbeiten. Alle weiteren Aktionen werden bis zur höheren Ebene durchgeführt.

Da die höhere Ebene die Abfragestruktur kennt, erwartet sie immer, dass in der CPMCreateOueryOut-Nachricht die richtige Anzahl von Cursorhandles zurückgegeben wird. Die Cursorhandles werden in der folgenden Reihenfolge zurückgegeben: Das erste Handle ist für das nicht gekapte Rowset, das zweite für das erste kapitelte Rowset (die Gruppierung von Ergebnissen basierend auf der ersten Kategorie, die im CategorizationSet-Feld der CPMCreateQueryIn-Nachricht angegeben ist).

Zu Informationszwecken wird erwartet, dass höhere Ebenen die folgenden Aktionen ausführen können, diese werden jedoch nicht vom CISP-Client erzwungen:

-   Verwenden Sie CPMSetBindingsIn, um Bindungen für einzelne Spalten zu setzen und alle nachfolgenden Aktionen für den Abfragepfad auszuführen.
-   Verwenden Sie CPMGetQueryStatusIn, um den Ausführungsstatus einer Abfrage zu überprüfen.
-   Verwenden Sie CPMRatioFinishedIn, um den Vervollständigungsprozentsatz der Abfrage an fordern.

### <a name="3252-receiving-a-cpmgetrowsout-response"></a>3.2.5.2 Empfangen einer CPMGetRowsOut-Antwort

Wenn der Client eine CPMGetRowsOut-Meldungsantwort vom Server empfängt, MUSS der Client folgende Schritte ausführen:

-   Überprüfen Sie, ob \_ das Statusfeld im Header auf Erfolg oder Fehler hinweist.
-   Wenn der \_ Statuswert STATUS \_ BUFFER TOO \_ SMALL (0xC0000023) ist, MUSS der Client den Status \_ Letzte gesendete Nachricht überprüfen. Wenn sie keine CPMGetRowsIn-Nachricht enthält, MUSS die empfangene Nachricht im Hintergrund ignoriert werden. Andernfalls MUSS der Client eine neue CPMGetRowsIn-Nachricht mit allen Feldern, die mit dem gespeicherten identisch sind, an den Server senden, mit der Ausnahme, dass der \_ cbReadBuffer um 512 erhöht werden MUSS (aber nicht größer als 0x4000). Wenn \_ status STATUS BUFFER TOO SMALL \_ (0xC0000023) lautet und Last Message Sent bereits \_ \_ \_ cbReadBuffer aufweist, 0x4000 muss der Client den Fehler bis zur höheren Ebene melden.
-   Wenn der \_ Statuswert ein anderer Fehlerwert ist, MUSS der Client den Fehler bis zur höheren Ebene angeben.
-   Wenn der \_ Statuswert auf Erfolg hinweist, MÜSSEN die Ergebnisse bis zur höheren Ebene angezeigt werden, die die Informationen anfordert, und weitere Aktionen befinden sich auf der höheren Ebene.

Zu Informationszwecken wird erwartet, dass höhere Ebenen in der Regel die folgenden Aktionen ausführen, diese werden jedoch nicht vom Client des Inhaltsindizierungsdienstprotokolls erzwungen:

-   Wenn die Werte in Zeilen die Dokument-IDs darstellen, speichert die Kapitel- oder Lesezeichenhandles die höhere Ebene in der Regel für die Verwendung in nachfolgenden Vorgängen, die gültige Dokument-IDs, Kapitel- oder Lesezeichenhandles umfassen.
-   Auf der höheren Ebene werden die Daten aus Zeilenwerten in der Regel gespeichert, angezeigt oder anderweitig verwendet.
-   Für die Werte, die als verzögerte höhere Ebene markiert wurden, ruft den Wert mithilfe von CPMFetchValueIn-Nachrichten ab.
-   Die Suchbeschreibung wird ebenfalls an eine höhere Ebene zurückgegeben und kann von der höheren Ebene wiederverwendet oder untersucht werden.

Wenn die höhere Ebene zu Informationszwecken Handles für Kapitel und Lesezeichen anfordert, die in den Zeilen empfangen wurden, kann dies folgendermaßen erfolgen:

-   Verwenden Sie CPMGetQueryStatusExIn, um den Ausführungsstatus einer Abfrage sowie zusätzliche Statusinformationen zu überprüfen, z. B. die Anzahl der gefilterten Dokumente, die zu filternden Dokumente, das Verhältnis der von der Abfrage verarbeiteten Dokumente, die Gesamtzahl der Zeilen in der Abfrage und die Position des Lesezeichens im Rowset.
-   Verwenden Sie CPMGetNotify, um anzufordern, dass der Server den Client über Rowsetänderungen benachrichtigt.
-   Verwenden Sie CPMGetApproximatePositionIn, um die ungefähre Position eines Lesezeichens in einem Kapitel anzufordern.
-   Verwenden Sie CPMCompareBmkIn, um einen Vergleich zweier Lesezeichen in einem Kapitel anzufordern.
-   Verwenden Sie CPMRestartPositionIn auf dem Server, um die Position des Cursors in den Anfang des Rowsets zu ändern.

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a>3.2.5.3 Empfangen einer CPMFetchValueOut-Antwort

Wenn der Client eine CPMGetRowsOut-Meldungsantwort vom Server empfängt, MUSS der Client folgende Schritte ausführen:

-   Überprüfen Sie, ob das \_ Statusfeld im Header erfolg- oder fehlerbesagend ist. Bei einem Fehler wird die höhere Ebene benachrichtigt. Fahren Sie andernfalls weiter unten fort.
-   Überprüfen Sie \_ fValueExist, und wenn diese Einstellung auf 0x00000000 die höhere Ebene benachrichtigen, dass der Wert nicht gefunden wurde.
-   Andernfalls fügen Sie \_ cbValue-Bytes von vValue an den aktuellen Eigenschaftswert an.
-   Wenn \_ \_ fMoreExists auf 0x00000001 dann von \_ cbValue empfangene aktuelle Bytes erhöht \_ und eine CPMFetchValueIn-Nachricht an den Server gesendet wird, legen Sie \_ cbSoFar auf den Wert von Current Bytes Received, \_ cbPropSpec auf 0 (null) und \_ cbChunk auf die Puffergröße fest, die von der höheren Ebene gewünscht wird.
-   Wenn \_ fMoreExists auf 0x00000000, geben Sie den Eigenschaftswert von Aktueller Eigenschaftswert auf die höhere Ebene an.

### <a name="3254-receiving-a-cpmfreecursorout-response"></a>3.2.5.4 Empfangen einer CPMFreeCursorOut-Antwort

Wenn der Client eine erfolgreiche CPMFreeCursorOut-Nachrichtenantwort vom Server empfängt, MUSS der Client den \_ cCursorsRemaining-Wert an die höhere Ebene zurückgeben.

Die folgenden Informationen dienen nur zu Informationszwecken und werden nicht vom CISP-Client erzwungen. Von der höheren Ebene wird erwartet, dass sie Cursorhandles nachverfolgt und nicht diejenigen verwendet, die bereits freigegeben wurden. Sobald die Anzahl von \_ cCursorsRemaining gleich 0x00000000 ist, kann die höhere Ebene die Verbindung verwenden, um eine andere Abfrage anzugeben (mithilfe einer CPMCreateQueryIn-Nachricht).

### <a name="326-timer-events"></a>3.2.6 Timerereignisse

Keine.

### <a name="327-other-local-events"></a>3.2.7 Andere lokale Ereignisse

Keine.

## <a name="4-protocol-examples"></a>4 Beispiele für Protokolle

-   [4.1 Beispiel 1](#41-example-1)
-   [4.2 Beispiel 2](#42-example-2)

### <a name="41-example-1"></a>4.1 Beispiel 1

Im folgenden Beispiel betrachten wir ein Szenario, in dem der Benutzer JOHN auf Computer A die Dateigrößen abrufen möchte, die das Wort "Microsoft" aus dem Satz von Dokumenten enthalten, die auf Server X im KatalogSYSTEM gespeichert sind. Angenommen, Computer A führt ein 32-Bit-Betriebssystem unter Windows XP und Computer X ein 32-Bit-Betriebssystem unter Windows Server 2003 aus.

1.  Der Benutzer startet eine Suchanwendung und gibt die Suchabfrage ein. Die Anwendung übergibt die Suchabfrage wiederum an den Protokollclient.
2.  Der Protokollclient stellt eine Verbindung mit dem Indizierungsserver X her. Der Protokollclient verwendet die Named Pipe \\ Pipe \\ CI \_ SKADS, um über SMB eine Verbindung mit dem Server X herzustellen.
3.  Der Protokollclient bereitet dann eine CPMConnectIn-Nachricht mit den folgenden Werten vor:

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   **\_ msg** ist auf 0x000000C8 festgelegt und gibt an, dass es sich um eine CPMConnectIn-Nachricht handelt.
    -   **\_ status** ist auf 0x00000000 festgelegt.
    -   **\_ ulChecksum** enthält die Prüfsumme, die gemäß Abschnitt 3.2.4 berechnet wird.
    -   **\_ ulReserved2** ist auf 0x00000000 festgelegt.

    Der Text der Nachricht wird wie folgt aufgefüllt:

    -   **\_ iClientVersion** ist auf 0x00000008 festgelegt und gibt an, dass der Server das Prüfsummenfeld überprüfen soll.
    -   **\_ fClientIsRemote** ist auf 0x00000001 festgelegt, was angibt, dass der Server ein Remoteserver ist.
    -   **\_ cbBlob1** wird auf die Größe der Felder cPropSet, PropertySet1 und PropertySet2 in Bytes festgelegt.
    -   **\_ cbBlob2** ist auf 0x00000004 festgelegt (d. h. keine zusätzlichen Eigenschaftensätze).
    -   **MachineName** ist auf A festgelegt.
    -   **UserName** ist auf JOHN festgelegt.
    -   **cPropSets** ist auf 0x00000002 festgelegt.
    -   **Das PropertySet1-Feld** ist vom Typ CDbPropSet. Die CDbPropSet-Struktur, die das PropertySet1-Feld umfasst, wird wie folgt aufgefüllt:
        -   **Das Feld GuidPropSet** ist auf A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT) festgelegt.
        -   Das Feld **cProperties** ist auf 0x00000004 festgelegt.
        -   Das Feld **aProps** ist ein Array von CDbProp-Strukturen.

            Für das **aProps \[ \] 0-Element:**

            -   **PropId** ist auf 0x00000002 (DBPROP \_ CI CATALOG \_ \_ NAME) festgelegt.
            -   **DBPROPOPTIONS** ist auf 0x0000000 festgelegt.
            -   **DBPROPSTATUS** ist auf 0x00000000 festgelegt.
            -   Für das **ColId-Element:**
                -   **eKind** ist auf 0x00000001 (DBKIND \_ GUID \_ PROPID) festgelegt.
                -   **GUID** ist NULL (alle Nullen), d. h., der Wert gilt für die Abfrage, nicht nur für eine einzelne Spalte.
                -   **ulID** ist auf 0x00000000 festgelegt.
            -   Für das **vValue-Element:**
                -   **vType** ist auf 0x001F (VT \_ LPWSTR) festgelegt.
                -   **vValue** ist auf "SYSTEM", den Namen des gewünschten Katalogs, festgelegt.

            Für das **aProps \[ \] 1-Element:**

            -   **PropId** ist auf 0x00000007 festgelegt (DBPROP \_ CI \_ QUERY \_ TYPE)
            -   **DBPROPOPTIONS** ist auf 0x0000000 festgelegt.
            -   **DBPROPSTATUS** ist auf0x00000000 festgelegt.
            -   Für das **ColId-Element:**
                -   **eKind** ist auf 0x00000001 (DBKIND \_ GUID \_ PROPID) festgelegt.
                -   **GUID** ist NULL (alle Nullen), d. h., der Wert gilt für die Abfrage, nicht nur für eine einzelne Spalte.
                -   **ulID** ist auf 0x00000000 festgelegt.
            -   Für das **vValue-Element:**
                -   **vType** ist auf 0x0003 (VT \_ I4) festgelegt.
                -   **vValue** ist auf 0x00000000 (CiNormal) festgelegt, was bedeutet, dass es sich um eine reguläre Abfrage handelt.

            Für das **aProps \[ \] 2-Element:**

            -   **PropId** ist auf 0x00000004 (DBPROP \_ CI SCOPE \_ \_ FLAGS) festgelegt.
            -   **DBPROPOPTIONS** ist auf 0x0000000 festgelegt.
            -   **DBPROPSTATUS** ist auf 0x00000000 festgelegt.
            -   Für das **ColId-Element:**
                -   **eKind** ist auf 0x00000001 (DBKIND \_ GUID \_ PROPID) festgelegt.
                -   **GUID** ist NULL (alle Nullen), d. h., der Wert gilt für die Abfrage, nicht nur für eine einzelne Spalte.
                -   **ulID** ist auf 0x00000000 festgelegt.
            -   Für das **vValue-Element:**
                -   **vType:** 0x1003 (VT \_ VECTOR \| VT \_ I4)
                -   **vValue:** 0x00000001/0x00000001 (ein Element mit dem Wert 1), d. h. Suchunterordner

            Für das **aProps \[ \] 3-Element:**

            -   **PropId:** 0x00000003 (DBPROP \_ CI \_ INCLUDE \_ SCOPES)
            -   **DBPROPOPTIONS:** 0x0000000
            -   **DBPROPSTATUS:** 0x00000000
            -   Für das **ColId-Element:**
                -   **eKind** ist auf 0x00000001 (DBKIND \_ GUID \_ PROPID) festgelegt.
                -   **GUID** ist NULL (alle Nullen), d. h., der Wert gilt für die Abfrage, nicht nur für eine einzelne Spalte.
                -   **ulID** ist auf 0x00000000 festgelegt.
            -   Für das **vValue-Element:**
                -   **vType** ist auf 0x101F (VT \_ VECTOR \| VT \_ LPWSTR) festgelegt.
                -   **vValue** ist auf 0x00000001/ 0x00000002 / " \\ " (ein Element mit einer 2-Zeichen-NULL-endende Zeichenfolge) festgelegt, was den Stammbereich bedeutet.

    -   Das **PropertySet2-Feld** ist vom Typ CDbPropSet.

        Die CDbPropSet-Struktur, die das PropertySet1-Feld umfasst, wird wie folgt aufgefüllt:

        -   **GuidPropSet** ist auf AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT) festgelegt.
        -   Das Feld **cProperties** ist auf 0x00000001 festgelegt.
        -   Das Feld **aProps** ist ein Array von CDbProp-Strukturen.

            Für das **aProps \[ \] 0-Element:**

            -   **PropId** ist auf 0x00000002 (DBPROP \_ MACHINE) festgelegt.
            -   **DBPROPOPTIONS** ist auf 0x0000000 festgelegt.
            -   **DBPROPSTATUS** ist auf 0x00000000 festgelegt.
            -   Für das **ColId-Element:**
                -   **eKind** ist auf 0x00000001 (DBKIND \_ GUID \_ PROPID) festgelegt.
                -   **GUID** ist NULL (alle Nullen), d. h., der Wert gilt für die Abfrage, nicht nur für eine einzelne Spalte.
                -   **ulID** ist auf 0x00000000 festgelegt.
            -   Für **vValue-Element:**
                -   **vType:** 0x0008 (VT \_ BSTR)
                -   **vValue:** 0x04/"X" (4 Bytes/NULL-terminierte Unicode-Zeichenfolge), was "X" -name eines Servers bedeutet.

    -   Das Feld **cExtPropSet** ist auf 0x00000000 festgelegt.
    -   **Das Array aPropertySets** ist nicht vorhanden.
    -   Bei Bedarf werden verschiedene Auffüllungsfelder ausgefüllt. Die Nachricht wird an den Server gesendet.

4.  Der Server überprüft, ob **\_ ulChecksum** korrekt ist, überprüft, ob der Benutzer berechtigt ist, diese Anforderung zu senden, und antwortet mit einer CPMConnectOut-Nachricht.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   **\_ msg** ist auf 0x000000C8 festgelegt und gibt an, dass es sich um eine CPMConnectOut-Nachricht handelt.
    -   **\_ status** ist auf 0x0000000 festgelegt, die SUCCESS angibt.
    -   **\_ ulChecksum** ist auf 0 festgelegt.
    -   **\_ ulReserved2** ist auf 0x00000000 festgelegt.

    Der Nachrichtentext wird wie folgt aufgefüllt:

    -   Das Feld **\_ serverVersion** ist auf 0x00000007 (32-Bit Windows XP oder 32-Bit Windows Server 2003) festgelegt.
    -   **\_ Reservierte** Felder werden mit beliebigen Daten gefüllt.

5.  Der Client bereitet eine CPMCreateQueryIn-Nachricht vor.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   **\_ msg** ist auf 0x000000CA festgelegt, was angibt, dass es sich um eine CPMCreateQueryIn-Nachricht handelt.
    -   **\_ status** ist auf 0x00000000 festgelegt.
    -   **\_ ulChecksum** enthält die Prüfsumme, die gemäß 3.2.5 berechnet wird.
    -   **\_ ulReserved2** ist auf 0x00000000 festgelegt.

    Der Nachrichtentext wird wie folgt aufgefüllt:

    -   **Das** Feld Größe wird auf die Größe der restlichen Nachricht festgelegt.
    -   Das Feld **CColumnSetPresent** ist auf 0x01 festgelegt.
    -   **Das ColumnSet-Feld** ist vom Typ CColumnSet. Die CColumnSet-Struktur, aus der dieses Feld besteht, wird wie folgt festgelegt:
        -   **\_ das Feld count** ist auf 0x00000001 festgelegt, der angibt, dass eine Spalte zurückgegeben wird.
        -   **indexes-Array** ist 0x00000000 gibt den ersten Eintrag in \_ aPropSpec an.
    -   Das Feld **CRestrictionPresent** ist auf 0x01 festgelegt, das angibt, dass das Feld **Einschränkung** vorhanden ist.
    -   **Das Einschränkungsfeld** ist vom Typ CRestriction und auf festgelegt:
        -   **\_ ulType** ist auf 0x00000004 (RTContent) festgelegt.
        -   **\_ weight** ist auf 0x00000000 festgelegt.
    -   Der Rest des Felds enthält eine CContentRestriction-Struktur:
        -   **\_ Die Eigenschaft** ist auf GUID B725F130-47EF-101A-A5F1-02608c9eebac/0x00000001 (für PRSPEC \_ PROPID) /0x13 festgelegt, die den Dokumenttext darstellt.
        -   **\_ Cc** ist auf 0x00000009 festgelegt.
        -   **\_ pwcsphrase** wird auf die Zeichenfolge "Microsoft" festgelegt.
        -   **\_ lcid** ist auf 0x409 (für Englisch) festgelegt.
        -   **\_ ulGenerateMethod** ist auf 0x00000000 (genaue Übereinstimmung) festgelegt.
    -   **CSortPresent** ist auf 0x00 festgelegt.
    -   **CCategorizationSetPresent** ist auf 0x00 festgelegt.
    -   **RowSetProperties** wird wie folgt festgelegt:
        -   **\_ uBooleanOptions** ist auf 0x00000001 (sequenziell) festgelegt.
        -   **\_ ulMaxOpenRows** ist auf 0x00000000 festgelegt.
        -   **\_ ulMemoryUsage** ist auf 0x00000000 festgelegt.
        -   \_**cMaxResults** ist auf 0x00000100 festgelegt (höchstens 256 Zeilen zurückgeben).
        -   **\_ cCmdTimeOut** ist auf 0x00000000 festgelegt (kein Timeout).
    -   **PidMapper** ist auf:
        -   **\_ count** ist auf 0x00000001 festgelegt.
        -   **\_ aPropSpec** ist auf GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC/0x00000001 (für PRSPEC \_ PROPID) / 0x0000000c festgelegt, die die Windows-Dateigrößeneigenschaft darstellt.

6.  Der Server verarbeitet sie und antwortet mit einer CPMCreateQueryOut-Meldung.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   **\_ msg** ist auf 0x000000CA festgelegt und gibt an, dass es sich um eine CPMCreateQueryOut-Nachricht handelt.
    -   **\_ status** ist auf SUCCESS festgelegt.
    -   **\_ ulChecksum** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.
    -   **\_ ulReserved2** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.

    Der Nachrichtentext wird wie folgt aufgefüllt:

    -   **\_ fTrueSeqeuntial** ist auf 0x00000000 festgelegt, was angibt, dass die Abfrage einen Index verwenden kann.
    -   **\_ fWorkIdUnique** ist auf 0x00000001 festgelegt.
    -   Das **aCursors-Array** enthält nur ein Element, das ein Cursorhandle für diese Abfrage darstellt. Der Wert hängt vom Status des Servers ab. Angenommen, der zurückgegebene Wert ist 0xAAAAAAAA.

7.  Der Client gibt eine CPMSetBindingsIn-Anforderungsnachricht aus, um das Format einer Zeile zu definieren.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   **\_ msg** ist auf 0x000000D0 festgelegt, was angibt, dass es sich um eine CPMSetBindingsIn-Nachricht handelt.
    -   **\_ status** ist auf SUCCESS festgelegt.
    -   **\_ ulChecksum** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.
    -   **\_ ulReserved2** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.

    Der Nachrichtentext wird wie folgt aufgefüllt:

    -   **\_ hCursor** ist auf 0xAAAAAAAA festgelegt.
    -   **\_ cbRow** ist auf 0x10 festgelegt (groß genug für Spalten).
    -   **\_ cbBindingDesc** wird auf die Größe der Felder **\_ cColumns** und **\_ aColumns** kombiniert festgelegt.
    -   **\_ cColumns** ist auf 0x00000001 festgelegt.
    -   **\_ Das aColumns-Array** ist so festgelegt, dass es eine CTableColumn-Struktur enthält, die Folgendes enthält:
    -   -   **\_ PropSpec** ist auf GUID b725f130-47ef-101a-a5-f1-02608c9eebac /0x00000001 (für PRSPEC \_ PROPID) / 0x0000000c festgelegt, die die Windows-Dateigrößeneigenschaft darstellt.
        -   **\_ vType** ist auf 0x0015 (VT \_ UI8) festgelegt.
        -   **\_ ValueUsed** ist auf 0x01 festgelegt (Spalte in Zeile übertragen).
        -   **\_ ValueOffset** ist auf 0x0002 (am Anfang der Zeile) festgelegt.
        -   **\_ ValueSize** ist auf 0x08 (Größe einer VT \_ UI8) festgelegt.
        -   **\_ StatusUsed** ist auf 0x01 festgelegt.
        -   **\_ StatusOffset** ist auf 0x0A festgelegt.
        -   **\_ LengthUsed** ist auf 0x00 festgelegt.

8.  Der Server verarbeitet sie und antwortet mit einer CPMSetBindingsIn-Nachricht.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   **\_ msg** ist auf 0x000000D0 festgelegt.
    -   **\_ status** ist auf SUCCESS festgelegt.
    -   **\_ ulChecksum** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.
    -   **\_ ulReserved2** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.

9.  Der Client gibt eine CPMGetRowsIn-Anforderungsnachricht aus. Angenommen, der Client ist bereit, an diesem Punkt 100 Zeilen zu akzeptieren, und möchte diese in aufsteigender Reihenfolge haben.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   **\_ msg** ist auf 0x000000CC festgelegt, was angibt, dass es sich um eine CPMGetRowsIn-Nachricht handelt.
    -   **\_ status** ist auf 0x00000000
    -   **\_ ulChecksum** enthält die Prüfsumme, die gemäß Abschnitt 0 berechnet wird.
    -   **\_ ulReserved2** ist auf 0x00000000 festgelegt.

    Der Text der Nachricht wird wie folgt aufgefüllt:

    -   **\_ hCursor** ist auf 0xAAAAAAAA festgelegt.
    -   **\_ cRowsToTransfer** ist auf 0x00000064 festgelegt.
    -   **\_ cRowWidth** ist auf 0x00000010 (aus Bindungen) festgelegt.
    -   **\_ cbSeek** ist auf 0x14 festgelegt, wobei es sich um die Größe der Felder eType, \_ chapt und CRowSeekNext handelt.
    -   **\_ cbReserved** ist auf 0x18 (0x14 plus \_ cbSeek) festgelegt.
    -   **\_ cbReadBuffer** ist auf 0x800 festgelegt (0x64 \* 0x10 auf das nächste Vielfache von 0x200 aufgerundet).
    -   **\_ ulClientBase** ist auf 0x00000000 festgelegt.
    -   **\_ fBwdfetch** wird auf 0x00000000 festgelegt, der angibt, dass die Zeilen in vorwärts gerichteter Reihenfolge abgerufen werden sollen.
    -   **eType** wird auf 0x0000001 festgelegt, der angibt, dass der Client die nächsten Zeilen benötigt.
    -   **\_ chapt** ist auf 0 (kein Kapitelergebnis) festgelegt.
    -   **SeekDescription** ist auf CRowSeekNext festgelegt. Die CRowSeekNext-Struktur enthält die folgenden Werte:
        -   **CiTblChapt** ist auf 0x00000000 festgelegt.
        -   **\_ hRegion** ist auf 0x00000000 festgelegt.
        -   **\_ cSkip** ist auf 0 festgelegt, was angibt, dass der Client keine Zeilen überspringen möchte.

10. Der Server verarbeitet sie und antwortet mit einer CPMGetRowsOut-Meldung. Angenommen, der Server hat 100 Dokumente gefunden, die das Wort "Microsoft" enthalten.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   **\_ msg** ist auf 0x000000CC festgelegt und gibt an, dass es sich um eine CPMGetRowsOut-Meldung handelt.
    -   **\_ status** ist auf SUCCESS festgelegt.
    -   **\_ ulChecksum** ist auf 0x00000000 festgelegt.
    -   **\_ ulReserved2** ist auf 0x00000000 festgelegt.

    Der Text der Nachricht wird wie folgt aufgefüllt:

    -   **\_ CRowsReturned** ist auf 0x00000064 festgelegt.
    -   **eType** ist auf 0x00000001 festgelegt.
    -   **\_ chapt** ist auf 0x00000000 festgelegt (kein Kapitelergebnis).
    -   **SeekDescription** enthält eine CRowSeekNext-Struktur, die wie folgt aufgefüllt wird:
        -   **CiTblChapt** ist auf 0x00000000 festgelegt.
        -   **\_ hRegion** ist auf 0x00000000 festgelegt.
        -   **\_ cSkip** ist auf 0 festgelegt, was angibt, dass der Client keine Zeilen überspringen möchte.
    -   **Zeilen** enthalten die Größe der 100 Dokumente, die das Wort "Microsoft" enthalten. Da es sich um Daten mit fester Größe handelt, wird sie einfach als Liste mit 100 ganzen Zahlen ohne Vorzeichen mit 8 Byte strukturiert.

11. Der Client sendet eine CPMDisconnect-Nachricht, um die Verbindung zu beenden.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   **\_ msg** ist auf 0x000000C9 festgelegt und gibt an, dass es sich um eine CPMDisconnect-Nachricht handelt.
    -   **\_ status** ist auf 0x00000000 festgelegt.
    -   **\_ ulChecksum** ist auf 0x00000000 festgelegt.

12. Der Server verarbeitet die Nachricht und entfernt den gesamten Clientstatus.

### <a name="42-example-2"></a>4.2 Beispiel 2

Im vorherigen Beispiel war die Abfrage recht einfach. Betrachten wir nun eine etwas komplexere Abfrage. Angenommen, der Benutzer möchte die Größe der Dokumente abrufen, die die folgenden Wörter enthalten: "Microsoft" und "Office". Dies wird angegeben, indem Sie das Feld Einschränkung in der in Schritt 5 gesendeten CPMCreateQueryIn-Nachricht wie folgt ändern:

Das Feld **Einschränkung** hat den Typ CRestriction und ist auf Folgendes festgelegt:

-   -   **\_ ulType** ist auf 0x00000004 (RTAnd) festgelegt.
    -   **\_ weight** ist auf 0x00000000 festgelegt.

Der Rest des Felds enthält eine CNodeRestriction-Struktur:

-   -   **\_ cNode** ist auf 0x00000002 festgelegt und gibt an, dass das PaNode-Array zwei Knoten enthält.
    -   Das **\_ PaNode-Feld** ist ein Array von zwei CRestriction-Strukturen.

        **\_ paNode \[ 0 \]** enthält:

        -   -   **\_ ulType** ist auf 0x00000004 (RTContent) festgelegt.
            -   **\_ weight** ist auf 0x00000000 festgelegt.
            -   Der Rest des Felds enthält eine CContentRestriction-Struktur:
                -   **\_ Die Eigenschaft** ist auf GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (für PRSPEC \_ PROPID) /0x13 festgelegt.
                -   **\_ Cc** ist auf 0x00000009 festgelegt.
                -   **\_ pwcsphrase** wird auf die Zeichenfolge "Microsoft" festgelegt.
                -   **\_ lcid** ist auf 0x409 (für Englisch) festgelegt.
                -   **\_ ulGenerateMethod** ist auf 0x00000000 (genaue Übereinstimmung) festgelegt.

        **\_ paNode \[ 1 \]** enthält:

        -   -   **\_ ulType** ist auf 0x00000004 (RTContent) festgelegt.
            -   **\_ weight** ist auf 0x00000000 festgelegt.
            -   Der Rest des Felds enthält eine CContentRestriction-Struktur:
                -   **\_ Die Eigenschaft** ist auf GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (für PRSPEC \_ PROPID) /0x13 festgelegt.
                -   **\_ Cc** ist auf 0x00000006 festgelegt.
                -   **\_ pwcsphrase** ist auf die Zeichenfolge "Office" festgelegt.
                -   **\_ lcid** ist auf 0x409 (für Englisch) festgelegt.
                -   **\_ ulGenerateMethod** ist auf 0x00000000 (genaue Übereinstimmung) festgelegt.

## <a name="5-security"></a>5 Sicherheit

### <a name="51-security-considerations-for-implementers"></a>5.1 Sicherheitsüberlegungen für Ausführende

Indizierungsimplementierungen, die sichere Inhalte indizieren, sollten die Verwendung des von SMB MS-SMB bereitgestellten Benutzerkontexts in Betracht ziehen, um Suchergebnisse zu kürzen und nur die zurückzugeben, \[ auf die der \] Aufrufer zugreifen kann.

### <a name="52-index-of-security-parameters"></a>5.2 Index von Sicherheitsparameter



| Sicherheitsparameter  | `Section` |
|---------------------|---------|
| Ebene des Identitätswechsels | 2.1     |



 

## <a name="6-index-of-version-specific-behavior"></a>6 Index des versionsspezifischen Verhaltens



| Versionsspezifisches Verhalten                                                                         | `Section`   | Windows 2000 | Windows XP | Windows Server 2003 |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| Dieses Protokoll ist unter Windows 2000, Windows XP, Windows Server 2003 und Windows Vista implementiert. | 1.3.2     | X            | X          | X                   |
| Anwendungen interagieren in der Regel mit einem OLE DB-Wrapper.                                  | 1.4       | X            | X          | X                   |
| NTSTATUS-Werte                                                                                   | 1.8       | X            | X          | X                   |
| Der Client legt das \_ Statusfeld in jedem Nachrichtenheader fest.                                        | 2.2.2     | X            | X          | X                   |
| cPendingScans-Wert ist in der Regel 0 (null)                                                               | 2.2.3.1   | X            | X          | X                   |
| iClientVersion-Wert                                                                              | 2.2.3.6   | X            | X          | X                   |
| \_cbChunk-Wert                                                                                   | 2.2.3.19  | X            | X          | X                   |
| 32-Bit- und 64-Bit-Speicheradressen                                                                | 3.2.4.2.4 | X            | X          | X                   |



 

 

 





