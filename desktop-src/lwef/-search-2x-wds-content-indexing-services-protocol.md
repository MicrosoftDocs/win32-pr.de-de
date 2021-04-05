---
title: Inhaltsindizierungsdienste-Protokoll
description: Dieses Dokument ist eine Spezifikation des Content Index Service-Protokolls.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c22bbda912333368e50d3e4a8ace2cd98856ea
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "103724225"
---
# <a name="content-indexing-services-protocol"></a>Inhaltsindizierungsdienste-Protokoll

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .

Protokollspezifikation, Version 0,12

-   [1 Einführung](#1-introduction)
    -   [1.1 Glossar](#11-glossary)
    -   [1.2 Verweise](#12-references)
    -   [1,3-Protokoll Übersicht (Synopsis)](#13-protocol-overview-synopsis)
    -   [1.4 Beziehung zu anderen Protokollen](#14-relationship-to-other-protocols)
    -   [1,5 Voraussetzungen und Voraussetzungen](#15-prerequisites-and-preconditions)
    -   [1.6 Anwendbarkeitsanweisung](#16-applicability-statement)
    -   [1.7 Versionsverwaltung und Funktionsübertragung](#17-versioning-and-capability-negotiation)
    -   [1.8 Durch Hersteller erweiterbare Felder](#18-vendor-extensible-fields)
    -   [1.9 Zuweisungen von Standards](#19-standards-assignments)
-   [2\. Nachrichten](#2-messages)
    -   [2.1 Transport](#21-transport)
    -   [2.2 Nachrichtensyntax](#22-message-syntax)
-   [3 Protokolldetails](#3-protocol-details)
    -   [3,1 Server Details](#31-server-details)
    -   [3,2 Client Details](#32-client-details)
-   [4 Beispiele für Protokolle](#4-protocol-examples)
    -   [4,1 Beispiel 1](#41-example-1)
    -   [4,2 Beispiel 2](#42-example-2)
-   [5 Sicherheit](#5-security)
    -   [5.1 Sicherheitsüberlegungen für Ausführende](#51-security-considerations-for-implementers)
    -   [5.2 Index von Sicherheitsparameter](#52-index-of-security-parameters)
-   [6 Index des Versions spezifischen Verhaltens](#6-index-of-version-specific-behavior)

Dieses Dokument ist eine Spezifikation des Content Index Service-Protokolls.

Die Dokumentation zum Arbeitsgruppen Server-Protokoll Programm (WSPP) ist für die Verwendung in Verbindung mit der Dokumentation zu öffentlichen Standards, den Konzepten der Netzwerk Programmierung und der verteilten Systeme von Windows-Arbeitsgruppen vorgesehen und geht davon aus, dass der Reader entweder mit dem oben erwähnten Material vertraut ist oder sofort darauf zugreifen kann.

Für eine WSPP-Protokollspezifikation ist die Verwendung von Microsoft-Programmier Tools oder Programmierumgebungen nicht erforderlich, damit ein Lizenznehmer eine Implementierung entwickeln kann. Lizenznehmer, die Zugriff auf Microsoft-Programmier Tools und-Umgebungen haben, können Sie nutzen.

## <a name="1-introduction"></a>1 Einführung

-   [1.1 Glossar](#11-glossary)
-   [1.2 Verweise](#12-references)
-   [1,3-Protokoll Übersicht (Synopsis)](#13-protocol-overview-synopsis)
-   [1.4 Beziehung zu anderen Protokollen](#14-relationship-to-other-protocols)
-   [1,5 Voraussetzungen und Voraussetzungen](#15-prerequisites-and-preconditions)
-   [1.6 Anwendbarkeitsanweisung](#16-applicability-statement)
-   [1.7 Versionsverwaltung und Funktionsübertragung](#17-versioning-and-capability-negotiation)
-   [1.8 Durch Hersteller erweiterbare Felder](#18-vendor-extensible-fields)
-   [1.9 Zuweisungen von Standards](#19-standards-assignments)

### <a name="11-glossary"></a>1.1 Glossar

> [!Note]  
> Die folgenden Begriffe sind im Glossar Abschnitt von \[ ms-sys definiert \] :
>
> -   GUID
> -   Little-in-
> -   Named Pipe
> -   Pfad

 

**Bindung**: eine Anforderung zum Einschließen einer bestimmten **Spalte** in ein zurück gegebenes **Rowset** . Die **Bindung** gibt eine Eigenschaft an, die in den Suchergebnissen enthalten sein soll.

**Bookmark**: ein Marker, der eine Zeile innerhalb einer Gruppe von Zeilen eindeutig identifiziert.

**Catalog**: die Organisationseinheit der obersten Ebene im Index Dienst. Sie stellt einen Satz indizierter Dokumente dar, mit denen Abfragen mithilfe des Inhalts Indizierungs Dienst Protokolls ausgeführt werden können.

**Category**: eine hierarchische Gruppierung von Zeilen. Beispielsweise kann ein Abfrageergebnis, das Autoren-und Titel Spalten enthält, basierend auf dem Autor kategorisiert werden. Jede Gruppe von Zeilen, die den gleichen Wert für Author enthält, würde eine Kategorie darstellen.

**Kapitel** : ein Bereich von **Zeilen** innerhalb einer Reihe von **Zeilen** .

**Column**: der Container für einen einzelnen Typ von Informationen in einer **Zeile** . Spalten werden Eigenschaftsnamen zugeordnet, und es wird angegeben, welche Eigenschaften für die **Befehls** **Strukturelemente der** Suchabfrage verwendet werden.

**Befehls** Struktur: eine Kombination aus **Einschränkungen** , **Kategorien** und **Sortier Reihenfolgen** , die für die Suchabfrage angegeben sind.

**Cursor**: eine Entität, die als Mechanismus verwendet wird, um eine **Zeile** oder einen kleinen **Zeilen** Block gleichzeitig in einem Satz von Daten zu bearbeiten, die in einem Resultset zurückgegeben werden. Ein **Cursor** wird auf einer einzelnen **Zeile** im Resultset positioniert. Nachdem der **Cursor** auf einer Zeile positioniert wurde, können Vorgänge für diese **Zeile** oder für einen **Zeilen** Block, beginnend an dieser Position, ausgeführt werden.

**Handle**: ein Token, das zum Identifizieren von und Aufrufen von **Cursorn** , **Kapiteln** und **Lesezeichen** verwendet werden kann.

**Index**: eine persistente Struktur, die den Text Inhalt enthält, der von einem **Indizierungs Dienst** aus Dateien entnommen wurde. Dies schließt die Liste der Wörter ein, die zusammen mit dem enthaltenden Dateinamen, dem Wort **Speicherort und** dem Gebiets Schema gespeichert werden.

**Indizierung**: der Prozess des Extrahierens von Text und Eigenschaften aus Dateien und Speichern der extrahierten Werte in den **Indizes** (für Text) und dem **Eigenschafts Cache** (für-Eigenschaften).

**Indizierungs Dienst**: ein Dienst, der indizierte **Kataloge** für den Inhalt und die Eigenschaften von Dateisystemen erstellt. Anwendungen können in den Katalogen nach Informationen aus den Dateien im indizierten Dateisystem suchen.

**Locale**: ein Bezeichner, wie in \[ MS-GPSI \] Anhang A angegeben, der die für die Sprache relevanten Einstellungen angibt. Diese Einstellungen geben an, wie Datumsangaben und Uhrzeiten formatiert werden sollen, Elemente alphabetisch sortiert werden müssen, Zeichen folgen verglichen werden sollen usw.

**Abfragen in natürlicher Sprache**: eine Abfrage, die anstelle der Abfrage Syntax mit der menschlichen Sprache erstellt wurde.

**Rausch Wort**: ein Wort, das vom Indizierungs Dienst ignoriert wird, wenn es in den für die Suchabfrage angegebenen **Einschränkungen** vorhanden ist, da es wenig diskriminierenden Wert hat. Zu den englischen Beispielen zählen "a", "and" und "The".

**Eigenschafts Cache**: ein Cache von Dateieigenschaften, die von einem **Indizierungs Dienst** extrahiert werden.

**Eigenschafts Indizierung**: der Prozess, bei dem ein **Index** von **Werttyp Eigenschaften** eines Dokuments erstellt wird, einschließlich Autor, Betreff, Typ, Wort Anzahl, gedruckte Seitenanzahl und beliebiger anderer Eigenschaften.

**Einschränkung**: ein Satz von Bedingungen, die eine Datei erfüllen muss, um in die Suchergebnisse aufgenommen zu werden, die der **Indizierungs Dienst** als Antwort auf eine Suchabfrage zurückgibt. Eine **Einschränkung** schränkt den Fokus einer Suchabfrage ein und schränkt die Dateien ein, die der **Indizierungs Dienst** in den Suchergebnissen in die Suchergebnisse eingibt, sodass Sie nur diejenigen enthalten, die den Bedingungen entsprechen.

**Row**: die Auflistung von **Spalten** , die die Eigenschaftswerte enthält, die eine einzelne Datei aus dem Satz von Dateien beschreiben, die mit den in der Suchabfrage an den **Indizierungs Dienst** angegebenen **Einschränkungen** übereinstimmen.

**Rowset**: eine Reihe von **Zeilen** , die in den Suchergebnissen zurückgegeben werden.

**Sortierreihenfolge**: der Satz von Regeln in einer Suchabfrage, die die Reihenfolge der Zeilen im Suchergebnis definieren. Jede Regel besteht aus einer Eigenschaft (Name, Größe usw.) und einer Richtung für die Reihenfolge (aufsteigend oder absteigend). Mehrere Regeln werden sequenziell angewendet.

**Texttyp-Eigenschaft**: eine Eigenschaft, die den Inhalt eines Dokuments beschreibt und nur unformatierten Text enthält, der mit dem Namen verknüpft ist.

**Value-Type-Eigenschaft**: eine Eigenschaft, die ein einzelnes Attribut eines gesamten Dokuments beschreibt. Eine Werttyp Eigenschaft hat eine Datentyp-ID und einen Wert dieses Datentyps, der mit dem Namen verknüpft ist.

**Virtual root**: ein alternativer Pfad zu einem Ordner. Ein physischer Ordner kann über 0 (null) oder mehr virtuelle Stämme verfügen. Pfade, die mit einem virtuellen Stamm beginnen, werden als virtuelle Pfade bezeichnet. /Server/vanityroot könnte z. b. ein virtuelles Stammverzeichnis von C: \\ IIS \\ Web "Ordner1" sein \\ . Dann hätte die Datei C: \\ IIS \\ Web \\ "Ordner1"default.htm den \\ virtuellen Pfad/Server/vanityroot/default.htm.

**Kann, sollte, muss, sollte nicht, dürfen nicht**: diese Begriffe (in allen Caps) werden wie unter RFC2119 beschrieben \[ verwendet \] . Alle Aussagen zu optionalem Verhalten enthalten die Worte KÖNNEN, SOLLTEN oder SOLLTEN NICHT.

### <a name="12-references"></a>1.2 Verweise

### <a name="121-normative-references"></a>1.2.1 Normative Verweise

\[IEEE754 \] Institute of Electrical and Electronics Engineers, "Standard für binäre Floating-Point Arithmetik", IEEE 754-1985, Oktober 1985, https://standards.ieee.org/standard/754-1985.html

\[MS-DCOM \] Microsoft Corporation, "verteilte Component Object Model Remote Protokolle", Juni 2006.

\[MS-GPSI \] Microsoft Corporation, "Gruppenrichtlinie für die Softwareinstallation Extension", Juni 2006.

\[MS-SMB \] Microsoft Corporation, "Microsoft Server Message Block (SMB)-Protokoll und-Erweiterungen", Mai 2006.

\[MS-sys \] Microsoft Corporation, "System Übersicht V4", Juli 2006.

\[Salton \] Salton, G., "Automatische Text Verarbeitung: Transformations Analyse und Abruf von Informationen nach Computer", 1988, ISBN 0-201-2227-8.

\[Unicode: \] das Unicode-Konsortium "der Unicode-Standard, Version 2,0", 1996, https://www.unicode.org

### <a name="122-informative-references"></a>1.2.2 Informative Verweise

\[MSDN-OLEDB \] Microsoft Corporation, OLE DB https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .

\[MSDN-queryerr \] Microsoft Corporation, Query-Execution-Werte, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp

### <a name="13-protocol-overview-synopsis"></a>1,3-Protokoll Übersicht (Synopsis)

Ein Content- **Indizierungs Dienst** hilft bei der effizienten Organisation der extrahierten Funktionen einer Sammlung von Dokumenten. Das Content Index Service-Protokoll (CISP) ermöglicht einem Client, mit einem Server zu kommunizieren, der einen Indizierungs Dienst zum Ausstellen von Abfragen und zum Verwalten des Index Servers durch einen Administrator verwendet.

Beim Verarbeiten von Dateien analysiert ein Index Dienst einen Satz von Dokumenten und organisiert seinen Inhalt so neu, dass die **Eigenschaften** dieser Dokumente als Reaktion auf Abfragen effizient zurückgegeben werden können. Eine Auflistung von Dokumenten, die abgefragt werden können, umfasst einen **Katalog** . Ein Katalog kann einen **Index** (für kurz Verweise auf Text) und einen **Eigenschafts Cache** (für den schnellen Abruf von Eigenschafts Werten) enthalten.

Konzeptionell besteht ein Katalog aus einer logischen "Tabelle" von Eigenschaften mit dem Text oder Wert und dem entsprechenden Gebiets Schema, das in **Spalten** der Tabelle gespeichert ist. Jede Zeile der Tabelle entspricht einem separaten Dokument im Geltungsbereich des Katalogs, und jede "Spalte" der Tabelle entspricht einer Eigenschaft.

Die von CISP ausgeführten speziellen Aufgaben werden in zwei Funktionsbereichen gruppiert:

-   Remote Verwaltung von Indizierungs Dienst Katalogen
-   Remote Abfragen von Indizierungs Dienst Katalogen.

### <a name="131-remote-administration-tasks"></a>1.3.1 Remote Verwaltungsaufgaben

CISP ermöglicht die folgenden Dienst Katalog-Verwaltungs Tasks von einem-Client:

-   Fragen Sie den aktuellen Status eines Index Dienst Katalogs auf dem Server ab.
-   Aktualisieren Sie den Status eines Index Dienst Katalogs.
-   Starten Sie den Indizierungsprozess für eine bestimmte Gruppe von Dateien.
-   Initialisieren Sie die Optimierung eines Indexes, um die Abfrageleistung zu verbessern.

Bei allen Remote Verwaltungsaufgaben wird ein einfaches Anforderungs-/Antwort-Modell befolgt. Auf dem Client wird kein Status für einen Verwaltungs Aufruf und administrative Anrufe in beliebiger Reihenfolge beibehalten.

### <a name="132-remote-querying"></a>1.3.2 Remote Abfragen

Mit CISP können Clients Such Abfragen für einen Remote Server ausführen, der einen Indizierungs Dienst gehostet.

Das Senden einer Suchabfrage ist ein mehrstufiger Prozess, der vom Client initiiert wird. Die Schritte lauten wie folgt:

1.  Der Client fordert eine Verbindung zu einem Server an, der einen Indizierungs Dienst gehostet.
2.  Der Client sendet die Parameter für die Suchabfrage, die Folgendes umfassen:
    -   Die **Einschränkungen** , die angeben, welche Dokumente in die Suchergebnisse eingeschlossen und/oder aus diesen ausgeschlossen werden sollen.
    -   Die Reihenfolge, in der die Suchergebnisse zurückgegeben werden sollen.
    -   Die Spalten, die im Resultset zurückgegeben werden sollen.
    -   Die maximale Anzahl von **Zeilen** , die für die Abfrage zurückgegeben werden sollen.
    -   Die maximale Zeit für die Abfrage Ausführung.

        Nachdem der Server die Anforderung des Clients zum Initiieren der Abfrage bestätigt hat, kann der Client Statusinformationen zur Abfrage anfordern, dies ist jedoch kein erforderlicher Schritt.

3.  Der Client gibt dann an, welche Eigenschaften der Server in die Suchergebnisse einschließen soll.
4.  Der Client fordert ein Resultset vom Server an, und der Server antwortet, indem er die Eigenschaftswerte für Dateien, die in den Ergebnissen für die Suchabfrage des Clients enthalten waren, an den Client sendet. Wenn der Wert einer Eigenschaft zu groß für einen einzelnen Antwort Puffer ist, sendet der Server die Eigenschaft nicht, sondern legt den Eigenschafts Status auf "verzögert" fest. Der Client fordert dann den Eigenschafts Wert separat an, indem er eine Reihe von Anforderungen für nachfolgende Blöcke des Werts verwendet und dann die Anforderung anderer Werte fortsetzt.
5.  Sobald der Client mit der Suchabfrage fertig ist und keine zusätzlichen Ergebnisse mehr erfordert, kontaktiert der Client den Server, um die Abfrage freizugeben.
6.  Nachdem der Server die Abfrage freigegeben hat, sendet der Client möglicherweise eine Anforderung zum Trennen der Verbindung mit dem Server. Die Verbindung wird dann geschlossen. Alternativ kann der Client eine andere Abfrage ausgeben und die Sequenz aus Schritt 2 wiederholen.

Windows-Verhalten: Dieses Protokoll wird unter Windows 2000, Windows XP, Windows Server 2003 und Windows Vista implementiert.

### <a name="14-relationship-to-other-protocols"></a>1.4 Beziehung zu anderen Protokollen

Der CISP basiert auf dem SMB \[ MS-SMB- \] Protokoll für den Nachrichten Transport. Kein anderes Protokoll hängt direkt vom Content Index Service-Protokoll ab.

*Windows-Verhalten: Anwendungen interagieren in der Regel mit einem OLE DB Schnittstellen Wrapper \[ MSDN-OLEDB \] (z. b. einem Protokoll Client) und nicht direkt mit dem Protokoll.*

### <a name="15-prerequisites-and-preconditions"></a>1,5 Voraussetzungen und Voraussetzungen

Es wird davon ausgegangen, dass der Client den Namen des Servers und einen Katalognamen abgerufen hat, bevor dieses Protokoll aufgerufen wird. Wie ein Client dies tut, liegt außerhalb des Gültigkeits Bereichs dieser Spezifikation.

Außerdem wird davon ausgegangen, dass der Client und der Server über eine Sicherheits Zuordnung verfügen, die mit Named Pipes \[ MS-SMB verwendbar ist \] .

### <a name="16-applicability-statement"></a>1.6 Anwendbarkeitsanweisung

CISP dient zum Abfragen und Verwalten von Katalogen auf einem Remote Server von einem Client. CISP ist in Windows Vista veraltet.

### <a name="17-versioning-and-capability-negotiation"></a>1.7 Versionsverwaltung und Funktionsübertragung

Dieses Protokoll verfügt über keine Mechanismen zur Versionierung oder Funktions Aushandlung.

### <a name="18-vendor-extensible-fields"></a>1.8 Durch Hersteller erweiterbare Felder

Dieses Protokoll verwendet HRESULTs, die Anbieter erweiterbar sind. Anbieter können Ihre eigenen Werte für dieses Feld auswählen, solange das C-Bit (0x20000000) gemäß den Angaben im Abschnitt 4.1.1 von \[ ms-sys festgelegt ist \] . Dies deutet darauf hin, dass es sich um einen Kundencode handelt.

Dieses Protokoll verwendet auch NTSTATUS-Werte, die aus dem in ms-sys definierten NTSTATUS-Nummernbereich entnommen werden \[ \] . Die Anbieter sollten diese Werte mit der jeweiligen Bedeutung wieder verwenden. Wenn Sie einen anderen Wert auswählen, wird das Risiko eines Konflikts in der Zukunft.

*Windows-Verhalten: Windows verwendet nur die Werte, die im Abschnitt 4.1.3 von \[ ms-sys angegeben sind \] .*

### <a name="181-property-ids"></a>1.8.1-Eigenschaften-IDs

Eigenschaften werden durch IDs dargestellt, die als eigen schafts-IDs bezeichnet werden. Jede Eigenschaft muss über eine Globally Unique Identifier verfügen. Dieser Bezeichner besteht aus einer **GUID** , die eine Auflistung von Eigenschaften darstellt, die als Eigenschaften Satz bezeichnet werden, sowie eine Zeichenfolge oder eine ganze Zahl mit 32 Bit, um die Eigenschaft innerhalb des Satzes zu identifizieren. Wenn die ganzzahlige Form von ID verwendet wird, werden die Werte 0x00000000, 0xFFFFFFFF und 0xFFFFFFFE als ungültig eingestuft.

Anbieter können garantieren, dass ihre Eigenschaften eindeutig definiert werden, indem Sie in einem Eigenschaften Satz platziert werden, der durch ihre eigene GUID definiert ist.

### <a name="19-standards-assignments"></a>1.9 Zuweisungen von Standards

Dieses Protokoll hat keine Standard Zuweisungen, sondern nur private Zuweisungen, die von Microsoft mithilfe von in anderen Protokollen angegebenen Zuordnungs Prozeduren hergestellt wurden.

Microsoft hat diesem Protokoll eine Named Pipe zugewiesen, wie in \[ MS-SMB angegeben \] . Die Zuweisung lautet:



| Parameter | Wert             | Referenz  |
|-----------|-------------------|------------|
| Pipename | \\Pipe- \\ ci- \_ Skaden | \[MS-SMB\] |



 

## <a name="2-messages"></a>2\. Nachrichten

-   [2.1 Transport](#21-transport)
-   [2.2 Nachrichtensyntax](#22-message-syntax)

### <a name="21-transport"></a>2.1 Transport

Alle Nachrichten müssen mithilfe einer Named Pipe transportiert werden, wie in \[ MS-SMB angegeben \] . Der folgende Pipename wird verwendet:

-   \\Pipe- \\ ci- \_ Skaden

Dieses Protokoll verwendet das zugrunde liegende SMB-Named Pipe-Protokoll, um die Identität des Aufrufers abzurufen, der die Verbindung hergestellt hat, wie im Abschnitt 2.2.8 of \[ MS-SMB angegeben \] . der Client muss die Sicherheits \_ Identifizierung als Identitätswechsel Ebene in der Anforderung festlegen, um die Named Pipe zu öffnen.

### <a name="22-message-syntax"></a>2.2 Nachrichtensyntax

Mehrere Strukturen und Nachrichten in den folgenden Abschnitten beziehen sich auf Kapitel-oder Lesezeichen Handles. Ein Handle ist eine lange 32-Bit-Struktur, die ein Kapitel oder Lesezeichen eindeutig identifiziert. Normalerweise empfangen Client Anwendungen handle-Werte über Methodenaufrufe. Es gibt jedoch einige bekannte Werte, die nicht von einem Server abgerufen werden müssen, was in der folgenden Tabelle angegeben ist:



| Wert                         | Bedeutung                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| DB \_ NULL \_ hChapter 0x00000000 | Ein Kapitel Handle für das ungeteilte Rowset, das alle Abfrageergebnisse enthält.    |
| Dbbmk \_ erste 0x00000001       | Ein Lesezeichen Handle für ein Lesezeichen, das die erste Zeile im Rowset identifiziert. |
| Dbbmk \_ Letzte 0x00000002        | Ein Lesezeichen Handle für ein Lesezeichen, das die letzte Zeile im Rowset identifiziert.  |



 

### <a name="221-structures"></a>2.2.1-Strukturen

In diesem Abschnitt werden Datenstrukturen ausführlich erläutert, die von CISP definiert und verwendet werden.

Alle 2-, 4-und 8-Byte-Ganzzahlen mit und ohne Vorzeichen in den folgenden Strukturen müssen in der Little-Endian-Byte Reihenfolge übertragen werden.

In der folgenden Tabelle werden die Datenstrukturen zusammengefasst, die in diesem Abschnitt definiert sind.



| Struktur                    | BESCHREIBUNG                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Cbasestoragevariant          | Enthält den Wert, für den eine Übereinstimmungs Operation für eine Eigenschaft durchgeführt werden soll, die in einer cpropertyeinschränkung-Struktur angegeben ist |
| SafeArray, SAFEARRAY2        | Enthält ein mehrdimensionales Array.                                                                                     |
| SAFEARRAYBOUND               | Stellt die Begrenzungen für eine Dimension eines Arrays dar, das in einer SAFEARRAY-Struktur angegeben ist.                                  |
| Cfullpropspec                | Enthält eine Eigenschafts Spezifikation.                                                                                     |
| Ccontent-Einschränkung          | Enthält eine Zeichenfolge, die mit einem Eigenschafts Wert im Eigenschaften Cache abgeglichen werden soll.                                                 |
| Ck                         | Enthält einen Eigenschafts Wert.                                                                                             |
| Cinternalpropertyeinschränkung | Enthält einen Eigenschafts Wert, der mit einem Vorgang verglichen werden soll.                                                                  |
| Cnatlanguagerestriction      | Enthält eine Abfrage in natürlicher Sprache für eine Eigenschaft.                                                                |
| Cnoderestriction             | Enthält ein Array von Befehlsstruktur Knoten, die die Einschränkungen für eine Abfrage angeben.                                       |
| "Cockrestriction"              | Enthält den Speicherort eines Worts in einem Ausdruck.                                                                           |
| Cpropertyeinschränkung         | Enthält einen Eigenschafts Wert, der mit einem Vorgang verglichen werden soll.                                                                  |
| Crangerestriction            | Enthält eine Einschränkung für einen Wertebereich.                                                                           |
| Cscoperestriction            | Enthält eine Einschränkung der Dateien, die durchsucht werden sollen.                                                                    |
| Csort                        | Identifiziert eine zu sortierende Spalte.                                                                                           |
| Csyneinschränkung              | Enthält ein Wort oder seine Synonyme für einen Abfrage Ausdruck.                                                                    |
| Cvectoreinschränkung           | Enthält eine gewichtete OR-Operation für einen Befehlsstruktur Knoten.                                                               |
| Cwordrestriction             | Enthält ein Wort für einen Abfrage Ausdruck.                                                                                    |
| Mit der Einschränkung                 | Enthält einen Knoten einer Abfrage Befehlsstruktur.                                                                               |
| Ccolumnset                   | Gibt die Anzahl der zurück zugebende Spalten an.                                                                             |
| Ccategorizationset           | Enthält Informationen zur Gruppierung eines Satzes von Abfrage Ergebnissen.                                                     |
| Ccategorizationspec          | Enthält eine Definition von Kategorien, in die Abfrageergebnisse kategorisiert werden.                                      |
| Cdbkolid                     | Enthält eine Spalte.                                                                                                     |
| Cdbprop                      | Enthält eine-Eigenschaft.                                                                                                   |
| CDbPropSet                   | Enthält einen Satz von Eigenschaften.                                                                                          |
| Cpidmapper                   | Enthält ein Array von Eigenschaften-IDs, die die Eigenschaften angeben, die in einem Rowset zurückgegeben werden sollen.                                     |
| Crowseekat                   | Enthält den Offset, bei dem Zeilen in einer cpmgetrowsin-Nachricht abgerufen werden sollen.                                                |
| Crowseekatratio              | Gibt den Punkt an, an dem mit dem Abrufen einer cpmgetrowsin-Nachricht begonnen werden soll.                                           |
| Crowseekbybookmark           | Gibt die Lesezeichen an, aus denen Zeilen für eine cpmgetrowsin-Nachricht abgerufen werden sollen.                                       |
| Crowseeknext                 | Enthält die Anzahl der Zeilen, die in einer cpmgetrowsin-Nachricht übersprungen werden sollen.                                                         |
| Crowsetproperties            | Enthält die Konfigurationsinformationen für eine Abfrage.                                                                    |
| Csortset                     | Enthält die Sortierreihenfolge für eine Abfrage.                                                                                   |
| Ctablecolumn                 | Enthält eine Spalte für die cpmsetbindungen-Nachricht.                                                                      |
| Serializedpropertyvalue      | Enthält einen serialisierten Wert.                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a>2.2.1.1 cbasestoragevariant

Die cbasestoragevariant-Struktur enthält den Wert, für den eine Übereinstimmungs Operation für eine Eigenschaft durchgeführt werden soll, die in der cpropertyeinschränkung-Struktur angegeben ist.



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

VType

vData1

vData2

vValue (Variable)



 

**VType**: ein Typindikator, der den Typ von vValue angibt. Es muss sich um einen der varenumum-Werte handeln, die in der folgenden Tabelle angegeben sind.



| Wert                 | Bedeutung                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ leer (0x0000)    | vValue ist nicht vorhanden.                                                                                                               |
| VT \_ NULL (0x0001)     | vValue ist nicht vorhanden.                                                                                                               |
| VT \_ I1 (0x0010)       | Eine 1-Byte-Ganzzahl mit Vorzeichen.                                                                                                             |
| VT \_ UI1 (0x0011)      | Eine 1-Byte-Ganzzahl ohne Vorzeichen.                                                                                                           |
| VT \_ I2 (0x0002)       | Eine 2-Byte-Ganzzahl mit Vorzeichen.                                                                                                             |
| VT \_ UI2 (0x0012)      | Eine 2-Byte-Ganzzahl ohne Vorzeichen.                                                                                                           |
| VT \_ bool (0x000b)     | Ein boolescher Wert. eine 2-Byte-Ganzzahl, die 0x0000 (false) oder 0xFFFF (true) enthält.                                                        |
| VT \_ I4 (0x0003)       | Eine 4-Byte-Ganzzahl mit Vorzeichen.                                                                                                             |
| VT \_ UI4 (0x0013)      | Eine 4-Byte-Ganzzahl ohne Vorzeichen.                                                                                                           |
| VT \_ R4 (0x0004)       | Eine IEEE 32-Bit-Gleit Komma Zahl, wie in \[ IEEE754 definiert \] .                                                                     |
| VT \_ int (0x0016)      | Eine 4-Byte-Ganzzahl mit Vorzeichen.                                                                                                             |
| VT \_ uint (0x0017)     | Eine 4-Byte-Ganzzahl ohne Vorzeichen.                                                                                                           |
| VT- \_ Fehler (0x000a)    | Eine 4-Byte-Ganzzahl ohne Vorzeichen, die ein HRESULT enthält, wie in \[ ms-sys angegeben \] .                                                         |
| VT \_ I8 (0x0014)       | Eine 8-Byte-Ganzzahl mit Vorzeichen.                                                                                                            |
| VT \_ UI8 (0x0015)      | Eine 8-Byte-Ganzzahl ohne Vorzeichen.                                                                                                          |
| VT \_ R8 (0x0005)       | Eine IEEE 64-Bit-Gleit Komma Zahl gemäß Definition in \[ IEEE754 \] .                                                                      |
| VT \_ CY (0x0006)       | Eine ganzzahlige Ganzzahl mit 8 Bytes (skaliert durch 10.000).                                                                               |
| VT- \_ Datum (0x0007)     | Eine 64-Bit-Gleit Komma Zahl, die die Anzahl von Tagen seit 00:00:00 am 31. Dezember 1899 darstellt (koordinierte Weltzeit).     |
| VT \_ FILETIME (0x0040) | Eine 64-Bit-Ganzzahl, die die Anzahl der 100-Nanosekunden-Intervalle seit 00:00:00 am 1. Januar 1601 (koordinierte Weltzeit) darstellt. |
| VT \_ Decimal (0x000e)  | Eine dezimale Struktur, wie im Abschnitt 2.2.1.1.1.1 angegeben.                                                                             |
| VT \_ CLSID (0x0048)    | Ein 16-Byte-Binärwert, der eine GUID enthält.                                                                                            |
| VT- \_ BLOB (0x0041)     | Eine 4-Byte-Ganzzahl ohne Vorzeichen von Bytes im BLOB, gefolgt von der Anzahl der Daten bytes.                                           |
| VT \_ BSTR (0x0008)     | Eine 4-Byte-Ganzzahl ohne Vorzeichen von Bytes in der Zeichenfolge, gefolgt von einer Zeichenfolge, wie unten unter vValue angegeben.                       |
| VT \_ LPSTR (0x001e)    | Eine mit NULL endende ANSI-Zeichenfolge.                                                                                                       |
| VT \_ LPWSTR (0x001F)   | Eine NULL terminierte Unicode- \[ Unicode- \] Zeichenfolge.                                                                                        |
| VT- \_ Variante (0x000c)  | Cbasestoragevariant. Muss mit einem Typmodifizierer des VT- \_ Arrays oder des VT- \_ Vektors kombiniert werden.                                               |



 

In der folgenden Tabelle werden die Typmodifizierer für VType angegeben. Typmodifizierer können mit VType Binary ORed sein, um die Bedeutung von vValue zu ändern, um anzugeben, dass es sich um einen von zwei möglichen Array Typen handelt.



| Wert               | Bedeutung                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT- \_ Vektor (0x1000) | Wenn der Typindikator mithilfe eines OR-Operators mit dem VT-Vektor kombiniert wird \_ , ist vValue ein Gezähltes Array von Werten des bestimmten Typs. Weitere Informationen finden Sie im Abschnitt 2.2.1.1.1.2. <br/> Dieser Typmodifizierer darf nicht mit den folgenden Typen kombiniert werden: VT \_ int, VT \_ uint, VT \_ Decimal, VT \_ BLOB, VT \_ BLOB \_ Object.<br/>                                    |
| VT- \_ Array (0x2000)  | Wenn der Typindikator von einem or-Operator mit dem VT-Array kombiniert wird \_ , ist der Wert ein SafeArray (wie im Abschnitt 2.2.1.1.1.3 angegeben), der Werte des angegebenen Typs enthält. <br/> Dieser Typmodifizierer darf nicht mit den folgenden Typen kombiniert werden: VT \_ I8, VT \_ UI8, VT \_ FILETIME, VT \_ CLSID, VT \_ BLOB, VT \_ BLOB \_ Object, VT \_ LPStr, VT \_ LPWSTR. <br/> |



 

**vData1**: Wenn VType \_ den Wert VT Decimal hat, wird der Wert dieses Felds als Skalierungs Feld im Abschnitt 2.2.1.1.1.1 angegeben. Für alle anderen vtypes muss der Wert auf 0x00 festgelegt werden.

**vData2**: Wenn VType \_ den Wert VT Decimal hat, wird der Wert dieses Felds im Abschnitt 2.2.1.1.1.1 als Sign-Feld angegeben. Für alle anderen vtypes muss der Wert auf 0x00 festgelegt werden.

**vValue**: der Wert für den Übereinstimmungs Vorgang. Die Syntax muss wie im Feld "VType" angegeben werden.

In der folgenden Tabelle werden die Größen für das vValue-Feld zusammengefasst, abhängig vom Feld "VType" für Datentypen mit fester Länge. Die Größe wird in Bytes angezeigt.



| VType                                                   | Size |
|---------------------------------------------------------|------|
| VT \_ I1, VT, \_ UI1                                        | 1    |
| VT \_ I2, VT \_ UI2, VT \_ bool                               | 2    |
| VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ int, VT \_ uint, VT \_ Error   | 4    |
| VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ Date, VT \_ FILETIME | 8    |
| VT \_ Decimal, VT \_ CLSID                                  | 16   |



 

Wenn VType auf VT \_ BLOB, VT \_ BSTR oder VT LPSTR festgelegt ist, \_ wird die Struktur von vValue in der folgenden Abbildung angegeben:



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

CBSIZE

blobdata (Variable, optional)



 

**CBSIZE**: Vorzeichen lose 32-Bit-Ganzzahl, die die Größe des blobdata-Felds in Bytes angibt. Wenn VType auf VT \_ BSTR oder VT \_ LPSTR festgelegt ist, muss CBSIZE auf 0x00000000 festgelegt werden, wenn die dargestellte Zeichenfolge eine leere Zeichenfolge ist.

**blobdata**: muss eine Länge von CBSIZE in Bytes aufweisen.

Wenn VType auf VT BLOB festgelegt ist \_ , handelt es sich bei diesem Feld um undurchsichtige binäre BLOB-Daten.

Wenn VType auf VT BSTR festgelegt ist \_ , handelt es sich bei diesem Feld um einen Satz von Zeichen in einem vom OEM ausgewählten Zeichensatz. Client und Server müssen so konfiguriert sein, dass Sie über interoperable Zeichensätze verfügen (Out-of-Band des Protokolls). Es ist nicht erforderlich, dass es auf NULL endet.

Für VType auf VT \_ LPSTR ist dieses Feld eine NULL-terminierte Zeichenfolge in einem vom OEM ausgewählten Zeichensatz. Client und Server müssen so konfiguriert sein, dass Sie über interoperable Zeichensätze verfügen (Out-of-Band des Protokolls).

Wenn VType auf VT \_ LPWSTR festgelegt ist, wird die Struktur von vValue im folgenden Diagramm angegeben:



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

cclen

String (Variable, optional)



 

**cclen**: nicht signierte 32-Bit-Ganzzahl, die die Größe des Zeichen folgen Felds in Unicode-Zeichen angibt. Muss für eine leere Zeichenfolge auf 0x00000000 festgelegt werden.

**String**: mit NULL endender Unicode-Zeichenfolge.

### <a name="22111-cbasestoragevariant-structures"></a>2.2.1.1.1 cbasestoragevariant-Strukturen

Die folgenden Strukturen werden in der cbasestoragevariant-Struktur verwendet.

### <a name="221111-decimal"></a>2.2.1.1.1.1 Dezimal

Mit Decimal wird ein genauer numerischer Wert mit fester Genauigkeit und fester Skala dargestellt.

Wenn VType auf VT \_ Decimal (0x0000e) festgelegt ist, müssen die Felder vData1 und vData2 von cbasestoragevariant wie folgt interpretiert werden:

**vData1**: die Anzahl der Ziffern rechts vom Dezimaltrennzeichen. Muss zwischen 0 und 28 liegen.

**vData2**: das Vorzeichen des numerischen Werts. Auf "0x00" festgelegt, wenn positiv, 0x80, wenn negativ.

Das vValue-Feld weist das folgende Format auf:



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

Mid32



 

**Hi32**: die höchsten 32 Bits der 96-Bit-Ganzzahl.

**Lo32**: die niedrigsten 32 Bits der 96-Bit-Ganzzahl.

**Mid32**: die mittleren 32 Bits der 96-Bit-Ganzzahl.

### <a name="221112-vt_vector"></a>2.2.1.1.1.2 VT- \_ Vektor

Der VT- \_ Vektor wird verwendet, um eindimensionale Arrays zu übergeben.



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

vvector Elements

vvector Data



 

**vvectorelements**: Vorzeichen lose 32-Bit-Ganzzahl, die die Anzahl der Elemente im vvectordata-Feld angibt.

**vvector Data**: ein Array von Elementen, die über einen von VType festgelegten Typ verfügen, bei dem das 0x1000-Bit gelöscht wurde. Die Größe eines einzelnen Elements fester Länge kann aus der Datentyp Tabelle mit fester Länge abgerufen werden, wie im Abschnitt 2.2.1.1 angegeben. Die Länge dieses Felds in Bytes kann durch Multiplizieren von vvectorelements anhand der Größe des einzelnen Elements berechnet werden.

Für Datentypen mit variabler Länge enthält vvector Data eine Sequenz von sequenzierten einfachen Typen, bei denen der Typ von VType angegeben wird, wobei das 0x1000-Bit gelöscht wird. Dies schließt einen Sonderfall ein, der von der VType VT \_ array \| VT \_ Variant (z. b. 0x100c) angegeben wird.

Die Elemente im vvectordata-Feld müssen durch 0 bis 3 Auffüll Zeichen voneinander getrennt werden, sodass jedes Element bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die dieses Array enthält. Wenn Auffüll-Bytes vorhanden sind, ist der Wert, den Sie enthalten, willkürlich. Der Inhalt der Auffüll Zeichen muss vom Empfänger ignoriert werden.

Für einen VType, der auf VT \_ Array VT Variant festgelegt ist \| \_ , ist der Typ für Elemente in dieser Sequenz cbasestoragevariant.

### <a name="221113-safearray"></a>2.2.1.1.1.3 SAFEARRAY

SAFEARRAY wird verwendet, um mehrdimensionale Arrays zu übergeben. Die Struktur enthält Informationen zur Array Größe sowie die Daten im Array.



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

cdims

ffeaturen

cbelements

Rgson (Variable)

Vdata (Variable)



 

**cdims**: ganze 16-Bit-Zahl ohne Vorzeichen, die die Anzahl der Dimensionen des mehrdimensionalen Arrays angibt.

**ffeaturen**: ein 16-Bit-Bitfeld. Die Werte stellen Funktionen dar, die von Anwendungen der oberen Schicht definiert werden und ignoriert werden müssen.

**cbelements**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der einzelnen Elemente des Arrays angibt.

**Rgsbound**: ein Array, das eine SAFEARRAYBOUND-Struktur enthält, die im Abschnitt 2.2.1.1.1.4 pro Dimension im SafeArray angegeben ist. Dieses Array verfügt über die linke Dimension First und die Dimension ganz rechts.

**VData**: ein Vektor gemarshallter Elemente eines bestimmten Typs, der durch den VType der enthaltenden cbasestoragevariant gekennzeichnet ist, wobei das Bit 0x2000 gelöscht ist.

VData wird ähnlich \_ wie der VT-Vektor wie im Abschnitt 2.2.1.1.1.2 angegeben, mit dem Unterschied, dass die Anzahl der Elemente nicht vor dem Vektor gespeichert wird. Stattdessen wird die Anzahl der Elemente berechnet, indem der Wert für "celements" mit allen sicheren Array Begrenzungen multipliziert wird, die im Feld "rgsabound" angegeben sind. Elemente werden in einem Vektor in der Reihenfolge von Dimensionen gespeichert, beginnend mit der äußersten rechten Dimension.

Das folgende Diagramm stellt visuell ein zweidimensionales Beispiel Array dar. In der ersten Dimension sind die celements gleich 4 (dargestellt horizontal) und llbound gleich 0, und die zweite Dimension hat die celements gleich 2 (vertikal dargestellt) und llbound gleich 0.



|            |            |            |            |
|------------|------------|------------|------------|
| 0x00000001 | 0x00000002 | 0x00000003 | 0x00000005 |
| 0x00000007 | 0x00000011 | 0x00000013 | 0x00000017 |



 

Mithilfe des obigen Diagramms enthalten VData die folgende Sequenz: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005 bei der, 0x00000017 (Iteration durch die Rechte äußerste Dimension und anschließendes erhöhen der nächsten Dimension). Die vorangehende rgsbound (die die "celements" und "LBound" aufzeichnet) lautet: 0x00000004, 0x00000000, 0x00000002, 0x00000000.

### <a name="221114-safearraybound"></a>2.2.1.1.1.4 SAFEARRAYBOUND

Die SAFEARRAYBOUND-Struktur stellt die Begrenzungen einer Dimension eines SAFEARRAY oder SAFEARRAY2 dar. Das Format lautet:



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

llbound



 

**celements**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente in der Dimension angibt.

**llbound**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die untere Grenze der Dimension angibt.

### <a name="221115-safearray2"></a>2.2.1.1.1.5 SAFEARRAY2

SAFEARRAY2 wird verwendet, um mehrdimensionale Arrays in serializedpropertyvalue zu übergeben. Die Struktur enthält Grenz Informationen und die Daten.



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

cdims

Rgson (Variable)

Vdata (Variable)



 

**cdims**: nicht signierte 32-Bit-Ganzzahl, die die Anzahl der Dimensionen des SAFEARRAY2 angibt.

**Rgsbound**: ein Array, das eine SAFEARRAYBOUND-Struktur enthält, wie im Abschnitt 2.2.1.1.1.4 pro Dimension in der SAFEARRAY2 angegeben. Dieses Array verfügt über die linke Dimension First und die Dimension ganz rechts.

**VData**: ein Vektor gemarshallter Elemente eines bestimmten Typs, der durch den dwType des enthaltenden serializedpropertyvalue angegeben wird, wobei Bit 0x2000 gelöscht ist. Das Format von VData entspricht dem, das für das VData-Feld von SAFEARRAY im Abschnitt 2.2.1.1.1.3 angegeben wurde.

### <a name="2212-cfullpropspec"></a>2.2.1.2 cfullpropspec

Die cfullpropspec-Struktur enthält eine Eigenschaften Satz-GUID und einen Eigenschafts Bezeichner, um die Eigenschaft eindeutig zu identifizieren.



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

\_guidpropset

...

...

...

ulkind

Prspec

Eigenschaftsname (Variable)



 

**\_ guidpropset**: die GUID des Eigenschaften Satzes, zu dem die Eigenschaft gehört.

**ulkind**: eine 32-Bit-Ganzzahl ohne Vorzeichen. Einer der folgenden Werte, der den Inhalt von prspec angibt.



| Wert                                            | Bedeutung                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| prspec \_ LPWSTR<br/> 0x00000000<br/> | Das Feld "prspec" gibt die Anzahl der Zeichen an, die nicht NULL sind, im Feldeigenschaften Name. |
| prspec- \_ PROPID<br/> 0x00000001<br/>  | Das Feld "prspec" gibt die eigen schafts-ID (PROPID) an.                                     |



 

**Prspec**: eine 32-Bit-Ganzzahl ohne Vorzeichen mit einer Bedeutung, wie im Feld ulkind angegeben.

**Eigenschaftsname**: Wenn ulkind auf prspec PROPID festgelegt ist \_ , darf dieses Feld nicht vorhanden sein. Wenn ulkind auf prspec \_ LPWSTR festgelegt ist, muss dieses Feld ein Array von prspec-Unicode-Zeichen ohne Berücksichtigung der Groß-und Kleinschreibung enthalten, das den Namen der Eigenschaft enthält.

### <a name="2213-ccontentrestriction"></a>2.2.1.3 Ccontent-Einschränkung

Die Ccontent-Einschränkungs Struktur enthält eine Zeichenfolge, die einer Eigenschaft im Eigenschaften Cache entspricht.



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

\_Property (Variable)

...

Padding1 (Variable)

Cc

\_pwcspphrase (Variable)

...

Padding2 (Variable)

lcid

\_ulgeneratemethod



 

**\_ Property**: eine cfullpropspec-Struktur, wie im Abschnitt 2.2.1.2 angegeben. Dieses Feld gibt die Eigenschaft an, für die ein Übereinstimmungs Vorgang durchgeführt werden soll.

**Padding1**: Dieses Feld muss zwischen 0 und 3 Byte lang sein. Die Länge dieses Felds muss so lauten, dass das folgende Feld bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die diese Struktur enthält. Wenn dieses Feld vorhanden ist (d. h. eine Länge ungleich 0 (null)), ist der enthaltene Wert beliebig. Der Inhalt dieses Felds muss vom Empfänger ignoriert werden.

**CC**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von Zeichen im \_ Feld "pwcspphrase" angibt.

**\_ pwcspphrase**: eine Unicode-Zeichenfolge, die nicht auf NULL fest steht und das Wort oder den Ausdruck darstellt, der mit der Eigenschaft verglichen werden soll Dieses Feld darf nicht leer sein. Das CC-Feld enthält die Länge der Zeichenfolge.

**Padding2**: Dieses Feld muss zwischen 0 und 3 Byte lang sein. Die Länge dieses Felds muss so lauten, dass das folgende Feld bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die diese Struktur enthält. Wenn dieses Feld vorhanden ist (d. h. eine Länge ungleich 0 (null)), ist der enthaltene Wert beliebig. Der Inhalt dieses Felds muss vom Empfänger ignoriert werden.

**LCID**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Gebiets Schema der \_ pwcspphrase angibt, wie in \[ MS-GPSI \] Anhang A angegeben.

**\_ ulgeneratemethod**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Methode angibt, die beim Generieren alternativer Wort Formulare verwendet werden soll.



| Wert                                                       | Bedeutung                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Methode \_ genau generieren<br/> 0x00000000<br/>    | Genaue Übereinstimmung.                                                                                                                                                                                                                                                                                      |
| \_Methoden \_ Präfix generieren<br/> 0x00000001 <br/>  | Präfix Übereinstimmung                                                                                                                                                                                                                                                                                     |
| \_Methode als \_ inflect generieren <br/> 0x00000002<br/> | Findet eine Entsprechung für ein Wort. Eine Einfügung eines Worts ist eine Variante des Stamm Worts im gleichen Teil der Sprache, die gemäß den linguistischen Regeln einer bestimmten Sprache geändert wurde. Beispielsweise umfassen "Swim", "swims", "Swimming" und "Swap" die inflektionen des Verbs "Swimming" in englischer Sprache. |



 

### <a name="2214-ckey"></a>2.2.1.4 CKey

Die CKey-Struktur enthält einen-Eigenschafts Wert.



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

Betrieben

buf (Variable)



 

**PROPID**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die eigen schafts-ID darstellt, wie im Abschnitt 1.8.1 erläutert. Bekannte Werte sind:



| Wert      | Bedeutung                                                 |
|------------|---------------------------------------------------------|
| 0xFFFFFFFF | Stellt eine ungültige Eigenschaften-ID dar und darf nicht verwendet werden. |
| 0xfffffffe | Stellt eine ungültige Eigenschaften-ID dar und darf nicht verwendet werden. |
| 0x00000000 | Stellt eine beliebige Eigenschaften-ID dar.                             |



 

**CB**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge von buf in Bytes enthält.

**buf**: eine Byte Sequenz, die den Wert der-Eigenschaft darstellt.

### <a name="2215-cinternalpropertyrestriction"></a>2.2.1.5 cinternalpropertyeinschränkung

Die cinternalpropertyeinschränkungs-Struktur enthält einen Eigenschafts Wert, der mit einem Vorgang abgeglichen werden soll.



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

\_RelOp

\_Lauer

\_prval (Variable)

restrictionpresent

nextrestriction (Variable)



 

**\_ RelOp**: eine 32-Bit-Ganzzahl, die die Beziehung angibt, die für die Eigenschaft auszuführen ist. Muss einen der folgenden Werte aufweisen:



| Wert                 | Bedeutung                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| PRLT 0x00000000       | Ein kleiner-als-Vergleich.                                                                                           |
| Prle 0x00000001       | Ein kleiner-als-oder-gleich-Vergleich.                                                                               |
| Prgt 0x00000002       | Ein größer-als-Vergleich.                                                                                        |
| Prge 0x00000003       | Ein größer-als-oder gleich-Vergleich.                                                                            |
| Preq 0x00000004       | Ein Gleichheits Vergleich.                                                                                           |
| Prne 0x00000005 bei der       | Ein nicht gleicher Vergleich.                                                                                           |
| Prre 0x00000006       | Ein Vergleich mit einem regulären Ausdruck.                                                                                  |
| Prallbits 0x00000007  | Ein bitweises and, das den rechten Operanden zurückgibt.                                                                     |
| Prsomebits 0x00000008 | Ein bitweises and, das einen Wert ungleich 0 (null) zurückgibt.                                                                       |
| PRAll 0x00000100      | Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden, und ist nur true, wenn der Vorgang für alle Zeilen "true" ist. |
| Prany 0x00000200      | Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden, und ist "true", wenn der Vorgang für eine beliebige Zeile "true" ist.       |



 

**\_ PID**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die eigen schafts-ID darstellt (siehe PROPID im Abschnitt 2.2.1.4).

**\_ prval**: ein cbasestoragevariant-Objekt, das den Wert enthält, der mit der Eigenschaft verknüpft werden soll.

**restrictionpresent**: Ein Bytewert, der angibt, ob das nextrestriction-Feld vorhanden ist. Muss auf 0x00 oder 0x01 festgelegt werden. Wenn der Wert auf 0x01 festgelegt ist, gibt restrictionpresent an, dass das Feld nextrestriction vorhanden ist. Wenn der Wert auf 0x00 festgelegt ist, gibt restrictionpresent an, dass das Feld nextrestriction nicht vorhanden ist.

**nextrestriction**: eine in Abschnitt 2.2.1.16 angegebene Struktur der Struktur, die eine weitere Einschränkung angibt.

### <a name="2216-cnatlanguagerestriction"></a>2.2.1.6 cnatlanguagerestriction

Die cnatlanguagerestriction-Struktur enthält eine **Abfrage in natürlicher Sprache** für eine Eigenschaft.



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

\_Property (Variable)

...

\_Auffüllung \_ CC (Variable)

Cc

\_pwcspphrase (Variable)

...

\_Auffüllen von \_ LCID (Variable)

Lcid



 

**\_ Property**: eine cfullpropspec-Struktur, wie im Abschnitt 2.2.1.3 angegeben. Dieses Feld gibt die Eigenschaft an, für die der Übereinstimmungs Vorgang durchgeführt werden soll.

**\_ Auffüllung \_ CC**: Dieses Feld muss zwischen 0 und 3 Byte lang sein. Die Länge dieses Felds muss so lauten, dass das folgende Feld bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die diese Struktur enthält. Wenn dieses Feld vorhanden ist (d. h. eine Länge ungleich 0 (null)), ist der enthaltene Wert beliebig. Der Inhalt dieses Felds muss vom Empfänger ignoriert werden.

**CC**: eine 32-Bit-Ganzzahl ohne Vorzeichen. Die Anzahl von Zeichen im \_ Feld "pwcspphrase".

**\_ pwcspphrase**: eine Unicode-Zeichenfolge, die nicht auf NULL fest steht und das Wort oder den Ausdruck darstellt, der mit der Eigenschaft verglichen werden soll Darf nicht leer sein. Das CC-Feld enthält die Länge der Zeichenfolge.

**\_ Auffüllung \_ LCID**: Dieses Feld muss zwischen 0 und 3 Byte lang sein. Die Länge dieses Felds muss so lauten, dass das folgende Feld bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die diese Struktur enthält. Wenn dieses Feld vorhanden ist (d. h. eine Länge ungleich 0 (null)), ist der enthaltene Wert beliebig. Der Inhalt dieses Felds muss vom Empfänger ignoriert werden.

**LCID**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Gebiets Schema der \_ pwcspphrase angibt, wie in \[ MS-GPSI \] Anhang A angegeben.

### <a name="2217-cnoderestriction"></a>2.2.1.7 cnoderestriction

Die cnoderestriction-Struktur enthält ein Array von **Befehls** Struktur Knoten, die die Einschränkungen für die Abfrage angeben.



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

\_CNode

\_panode (Variable)



 

**\_ CNode**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der im \_ panode-Feld enthaltenen ermittelungs Strukturen angibt.

**\_ panode**: ein Array von krestriction-Strukturen. Strukturen im Array müssen durch 0 bis 3 Auffüll Bytes voneinander getrennt werden, sodass jede Struktur bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die dieses Array enthält. Wenn Auffüll-Bytes vorhanden sind, ist der Wert, den Sie enthalten, willkürlich. Der Inhalt der Auffüll Zeichen muss vom Empfänger ignoriert werden.

### <a name="2218-coccrestriction"></a>2.2.1.8-"cockrestriction"

Die "cockrestriction"-Struktur enthält die Position eines Worts in einem Ausdruck.



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

\_OCC

\_cprevnoisewords

\_cnextnoisewords



 

**\_ OCC**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Offset des Worts in einer Abfrage Zeichenfolge in Einheiten von Wörtern angibt. Ein in dieser Spezifikation verwendetes Wort ist eine Einheit der Sprache in jedem Gebiets Schema, das eine Bedeutung hat.

**\_ cprevnoisewords**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von Füll **Wörtern** enthält, die zwischen diesem Wort und dem vorherigen Wort im Ausdruck auftreten.

**\_ cnextnoisewords**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von Füll Wörtern enthält, die zwischen diesem Wort und dem nächsten Wort im Ausdruck auftreten.

### <a name="2219-cpropertyrestriction"></a>2.2.1.9 cpropertyeinschränkung

Die cpropertyeinschränkungs-Struktur enthält einen Eigenschafts Wert, der mit einem Vorgang verglichen werden soll.



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

\_RelOp

\_Property (Variable)

\_prval (Variable)



 

**\_ RelOp**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Beziehung angibt, die für die Eigenschaft durchgeführt werden soll. Muss einen der folgenden Werte aufweisen.



| Wert                 | Bedeutung                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| PRLT 0x00000000       | Ein kleiner-als-Vergleich.                                                                                           |
| Prle 0x00000001       | Ein kleiner-als-oder-gleich-Vergleich.                                                                               |
| Prgt 0x00000002       | Ein größer-als-Vergleich.                                                                                        |
| Prge 0x00000003       | Ein größer-als-oder gleich-Vergleich.                                                                            |
| Preq 0x00000004       | Ein Gleichheits Vergleich.                                                                                           |
| Prne 0x00000005 bei der       | Ein nicht gleicher Vergleich.                                                                                           |
| Prre 0x00000006       | Ein Vergleich mit einem regulären Ausdruck.                                                                                  |
| Prallbits 0x00000007  | Ein bitweises and, das den rechten Operanden zurückgibt.                                                                     |
| Prsomebits 0x00000008 | Ein bitweises and, das einen Wert ungleich 0 (null) zurückgibt.                                                                       |
| PRAll 0x00000100      | Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden, und ist nur true, wenn der Vorgang für alle Zeilen "true" ist. |
| Prany 0x00000200      | Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden, und ist "true", wenn der Vorgang für eine beliebige Zeile "true" ist.       |



 

**\_ Property**: eine cfullpropspec-Struktur, wie in Abschnitt 2.2.1.2 angegeben, gibt die Eigenschaft an, für die ein Übereinstimmungs Vorgang durchgeführt werden soll.

**\_ prval**: eine cbasestoragevariant-Struktur, wie im Abschnitt 2.2.1.1 angegeben, die den Wert enthält, der mit der Eigenschaft verknüpft werden soll.

### <a name="22110-crangerestriction"></a>2.2.1.10 crangerestriction

Die crangerestriction-Struktur enthält eine Einschränkung für einen Wertebereich.



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

\_keystart (Variable)

\_keyend (Variable)



 

**\_ keystart**: eine CKey-Struktur, wie in Abschnitt 2.2.1.4 angegeben, die den Anfang des Bereichs enthält.

**\_ keyend**: eine CKey-Struktur, die das Ende des Bereichs enthält.

### <a name="22111-cscoperestriction"></a>2.2.1.11 cscoperestriction

Die cscoperestriction-Struktur enthält eine Einschränkung der Dateien, die durchsucht werden sollen.



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

Cclowerpath

\_lowerpath (Variable)

...

\_Auffüll Zeichen (Variable)

\_Füll

\_"f"

\_virtueller



 

**Cclowerpath**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von Unicode-Zeichen im \_ Feld "lowerpath" enthält.

**\_ lowerpath**: eine Unicode-Zeichenfolge ohne NULL-terminierte Unicode-Zeichenfolge, die den **Pfad** darstellt, auf den die Abfrage beschränkt Das cclowerpath-Feld enthält die Länge der Zeichenfolge.

**\_ Auffüllung**: Dieses Feld muss zwischen 0 und 3 Byte lang sein. Die Länge dieses Felds muss so lauten, dass das folgende Feld bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die diese Struktur enthält. Wenn dieses Feld vorhanden ist (d. h. eine Länge ungleich 0 (null)), ist der enthaltene Wert beliebig. Der Inhalt dieses Felds muss vom Empfänger ignoriert werden.

**\_ length**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge von ' \_ lowerpath ' in Unicode-Zeichen enthält. Dieser Wert muss mit dem Wert von cclowerpath identisch sein.

**\_ f rekursive**: eine 32-Bit-Ganzzahl ohne Vorzeichen. Muss auf 0x00000001 oder 0x00000000 festgelegt werden. Bei der Einstellung 0x00000001 muss der Server rekursiv alle Unterverzeichnisse des Pfads überprüfen. Wenn der Server auf 0x00000000 festgelegt ist, kann er keine Unterverzeichnisse untersuchen.

" **\_ f Virtual**": eine 32-Bit-Ganzzahl ohne Vorzeichen. Muss auf 0x00000001 oder 0x00000000 festgelegt werden. Wenn der Wert auf 0x00000001 festgelegt \_ ist, handelt es sich bei lowerpath um einen virtuellen Pfad (die Uniform Resource Locator (URL), die einem physischen Verzeichnis im Dateisystem zugeordnet ist) für eine Website. Wenn der Wert auf 0x00000000 festgelegt ist, \_ ist lowerpath ein Dateisystempfad.

### <a name="22112-csort"></a>2.2.1.12 csort

Die csort-Struktur identifiziert eine zu sortierende Spalte.



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

pidcolumn

dworder

locale



 

**pidcolumn**: eine 32-Bit-Ganzzahl ohne Vorzeichen. Die Nummer der Spalte, nach der sortiert werden soll.

**dworder**: eine 32-Bit-Ganzzahl ohne Vorzeichen. Muss einer der folgenden Werte sein, wobei angegeben wird, wie basierend auf der Spalte sortiert werden soll.



| Wert                        | Bedeutung                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| Abfrage \_ sortascend 0x00000000 | Die Zeilen müssen in aufsteigender Reihenfolge nach den Werten in der angegebenen Spalte sortiert werden.  |
| Abfrage absteigend \_ 0x00000001    | Die Zeilen müssen auf der Grundlage der Werte in der angegebenen Spalte in absteigender Reihenfolge sortiert werden. |



 

**locale**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Gebiets Schema angibt, das in \[ MS-GPSI \] Anhang A der Spalte angegeben ist.

### <a name="22113-csynrestriction"></a>2.2.1.13 csyneinschränkung

Die csyneinschränkungs-Struktur enthält ein Wort oder seine Synonyme für einen Abfrage Ausdruck.



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

ck

\_keyarray (Variable)

\_IsRange



 

**Einschränkung**: eine cockrestriction-Struktur, die die Position des Worts angibt.

**ckey**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im \_ keyarray-Array angibt.

**\_ keyarray**: ein Array von CKey-Strukturen, das ein Wort und seine Synonyme angibt.

**\_ IsRange**: bei Festlegung auf 0x01 sind die Schlüssel Präfixe, die abgeglichen werden sollen. Wenn der Wert auf 0x00 festgelegt ist, sind die Schlüssel genaue Werte für den Abgleich. \_"IsRange" darf nicht auf andere Werte festgelegt werden.

### <a name="22114-cvectorrestriction"></a>2.2.1.14 cvectoreinschränkung

Die cvectoreinschränkungs-Struktur enthält eine gewichtete OR-Operation für einen Befehlsstruktur Knoten.



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

\_Pres (Variable)

...

\_Auffüll Zeichen (Variable)

\_ulrankmethod



 

**\_ Pres**: eine cnoderestriction-Befehlsstruktur, auf der ein Rang oder ein Vorgang ausgeführt werden soll.

**\_ Auffüllung**: Dieses Feld muss zwischen 0 und 3 Byte lang sein. Die Länge dieses Felds muss so lauten, dass das folgende Feld bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die diese Struktur enthält. Wenn dieses Feld vorhanden ist (d. h. eine Länge ungleich 0 (null)), ist der enthaltene Wert beliebig. Der Inhalt dieses Felds muss vom Empfänger ignoriert werden.

**\_ ulrankmethod**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die einen Rang Folge Algorithmus angibt. Muss auf einen der folgenden Werte festgelegt werden.



| Wert                            | Bedeutung                                       |
|----------------------------------|-----------------------------------------------|
| Vektor \_ Rang \_ Min 0x00000000     | Verwenden Sie den minimalen \[ Salton-Algorithmus \] .             |
| Vektor \_ Rang \_ Max 0x00000001     | Verwenden Sie den maximalen Algorithmus \[ Salton \] .             |
| Vektor \_ Rang \_ innere 0x00000002   | Verwenden Sie den inneren Produkt Algorithmus \[ Salton \] .       |
| Vektor \_ Rang \_ Würfel 0x00000003    | Verwenden Sie den Würfel Koeffizient-Algorithmus \[ Salton \] .    |
| Vektor \_ Rang \_ Jaccard 0x00000004 | Verwenden Sie den Jaccard-Koeffizienten-Algorithmus \[ Salton \] . |



 

### <a name="22115-cwordrestriction"></a>2.2.1.15 cwordrestriction

Die cwordrestriction-Struktur enthält ein Wort für einen Abfrage Ausdruck.



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

\_Schlüssel (Variable)

\_IsRange



 

**Einschränkung**: eine cockrestriction-Struktur, die die Position des Worts angibt.

**\_ Key**: eine CKey-Struktur, die ein Wort angibt.

**\_ IsRange**: bei Festlegung auf 0x01 ist der Schlüssel ein Präfix, das abgeglichen werden soll. Wenn der Wert auf 0x00 festgelegt ist, ist der Schlüssel ein genauer Wert, der gefunden werden soll. \_"IsRange" darf nicht auf einen anderen Wert festgelegt werden.

### <a name="22116-crestriction"></a>2.2.1.16-Bindung

Die Struktur mit dem Aufstrich enthält einen Knoten einer Abfrage Befehlsstruktur.



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

\_ultype

Weight

Einschränkung



 

**\_ ultype**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die den für den Befehlsstruktur Knoten verwendeten Einschränkungstyp angibt. Muss auf einen der folgenden Werte festgelegt werden.



| Wert                    | Bedeutung                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| Rtnone 0x00000000        | Der Knoten stellt ein Füll Wort in einer Vektor Abfrage dar.                                         |
| Rtand 0x00000001         | Der Knoten enthält eine cnoderestriction, auf der eine logische and-Operation ausgeführt werden soll. |
| Rtor 0x00000002          | Der Knoten enthält eine cnoderestriction, auf der eine logische OR-Operation ausgeführt werden soll.  |
| Rtnot 0x00000003         | Der Knoten enthält eine Einschränkung, auf der ein Not-Vorgang ausgeführt werden soll.             |
| Rtcontent 0x00000004     | Der Knoten enthält eine Ccontent-Einschränkung.                                                    |
| Rtproperty 0x00000005 bei der    | Der Knoten enthält eine cpropertyeinschränkungs Einschränkung.                                                   |
| Rtnear 0x00000006   | Der Knoten enthält eine cnoderestriction, auf der eine near-Rangfolge ausgeführt werden soll.     |
| Rtvector 0x00000007      | Der Knoten enthält eine cvectoreinschränkung.                                                     |
| Rtnatlanguage 0x00000008 | Der Knoten enthält eine cnatlanguagerestriction.                                                |
| Rtscope 0x00000009       | Der Knoten enthält eine cscoperestriction.                                                      |
| Alle 0xfffffffffa         | Der Knoten enthält eine cinternalpropertyeinschränkungs Einschränkung.                                           |
| Rtrange 0xfffffffc       | Der Knoten enthält einen crangerestriction-Knoten.                                                      |
| Rtphrase 0xfffffffd      | Der Knoten enthält eine cnoderestriction, auf der eine Ausdrucks Übereinstimmung ausgeführt werden soll.          |
| Rtsynonym 0xfffffffe     | Der Knoten enthält eine csyneinschränkung.                                                        |
| Rtword 0xFFFFFFFF        | Der Knoten enthält ein cwordrestriction-Element.                                                       |



 

**Weight**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gewichtung des Knotens darstellt. Gewichtung gibt die Wichtigkeit des Knotens relativ zu anderen Knoten in der Abfrage Befehlsstruktur an. Höhere Gewichtungswerte sind wichtiger.

**Einschränkung**: der Einschränkungstyp für den Befehlsstruktur Knoten. Die Syntax muss wie im \_ Feld ultype angegeben werden.

### <a name="22117-ccolumnset"></a>2.2.1.17 ccolumnset

Die ccolumnset-Struktur gibt die Spalten Nummern an, die zurückgegeben werden sollen. Diese Struktur wird immer als Verweis auf eine bestimmte cpidmapper-Struktur (Abschnitt 2.2.1.23) verwendet.



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



 

**count**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im Index Array angibt.

**Indizes**: Array von 4-Byte-Ganzzahlen ohne Vorzeichen, das null basierte Indizes im apropspec-Array in der entsprechenden cpidmapper-Struktur darstellt.

### <a name="22118-ccategorizationset"></a>2.2.1.18 ccategorizationset

Die ccategorizationset-Struktur enthält Informationen zur Gruppierung eines Abfrageresultsets.



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

Kategorien (Variable)



 

**count**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im kategoriearray enthält.

**Categories**: Array der ccategorizationspec-Strukturen, die die Gruppierung der Abfrage angeben.

### <a name="22119-ccategorizationspec"></a>2.2.1.19 ccategorizationspec

Die ccategorizationspec-Struktur enthält eine Gruppierung für ein Abfrageresultset.



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

\_cscolumschlag (Variable)

\_ulCategType



 

**\_ cscolenns**: eine ccolumnset-Struktur, die die Spalten angibt, nach denen die Abfrage gruppiert werden soll.

**\_ ulCategType**: eine 32-Bit-Ganzzahl ohne Vorzeichen. Muss auf 0x00000000 festgelegt werden.

### <a name="22120-cdbcolid"></a>2.2.1.20 cdbcolid

Die cdbcolid-Struktur enthält eine-Spalte.



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

"ulid"

vstring (Variable)



 

**eKind**: muss auf einen der unten aufgeführten Werte festgelegt werden, der den Inhalt von "GUID" und "vValue" angibt.



| Wert                            | Bedeutung                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Dbkind- \_ GUID- \_ Name 0x00000000    | vstring enthält einen Eigenschaftsnamen.                                                                               |
| Dbkind \_ GUID \_ PROPID 0x00000001  | die OKD enthält eine 4-Byte-Ganzzahl, die die Eigenschaften-ID angibt.                                                      |
| Dbkind- \_ pguid- \_ Name 0x00000003   | vstring enthält einen Eigenschaftsnamen. Dieser Wert muss mit dem dbkind- \_ GUID-Namen behandelt werden \_ .                    |
| Dbkind \_ pguid \_ PROPID 0x00000004 | die OKD enthält eine 4-Byte-Ganzzahl, die die Eigenschaften-ID angibt. Dieser Wert muss mit der dbkind- \_ GUID- \_ PROPID identisch sein. |



 

**GUID**: die Eigenschafts-GUID.

**ulid**: Wenn eKind dbkind \_ GUID \_ PROPID oder dbkind \_ pguid \_ PROPID ist, enthält dieses Feld eine Ganzzahl ohne Vorzeichen, die die Eigenschaften-ID angibt. Wenn eKind den dbkind- \_ GUID- \_ Namen oder den dbkind- \_ pguid- \_ Namen aufweist, enthält dieses Feld eine Ganzzahl ohne Vorzeichen, die die Anzahl der im vstring-Feld enthaltenen Unicode-Zeichen angibt.

**vstring**: eine Unicode-Zeichenfolge, die nicht auf NULL fest steht und den Eigenschaftsnamen darstellt. Sie muss weggelassen werden, es sei denn, das eKind-Feld ist auf den dbkind- \_ GUID- \_ Namen oder den dbkind- \_ pguid- \_ Namen

### <a name="22121-cdbprop"></a>2.2.1.21 cdbprop

Die cdbprop-Struktur enthält eine-Eigenschaft.



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

Dbpropstatus

kolid (Variable)

vValue (Variable)



 

**DBPROPID**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Eigenschaften-ID angibt.

**DBPROPOPTIONS** : muss auf 0x00000000 festgelegt werden.

**Dbpropstatus**: muss auf 0x00000000 festgelegt werden.

**ColId**: eine cdbcolid-Struktur, wie im Abschnitt 2.2.1.20 angegeben, gibt die Spalte an, auf die die Eigenschaft angewendet wird.

**vValue**: ein cbasestoragevariant-Wert, der den Eigenschafts Wert enthält.

### <a name="221211-properties"></a>2.2.1.21.1-Eigenschaften

In diesem Abschnitt werden die Eigenschaften erläutert, die von CISP verwendet werden. Diese Eigenschaften werden in drei Eigenschaften Sätze gruppiert: Ident 2.2.1.21.1 Ified im Feld guidPropertySet der CDBPropSet-Struktur (Abschnitt 2.2.1.22).

In der folgenden Tabelle sind die Eigenschaften aufgelistet, die Teil der Eigenschaft "DBPROPSET \_ fscifrmwrk ext" sind \_ .



| Wert                                  | Bedeutung                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ ci- \_ Katalog \_ Name 0x00000002   | Gibt den Namen des Katalogs oder der Kataloge an, die abgefragt werden sollen. Der Wert muss ein VT \_ LPWSTR oder ein VT- \_ Vektor \| VT \_ LPWSTR sein.                                   |
| DBPROP \_ ci \_ include- \_ Bereiche 0x00000003 | Gibt einen oder mehrere Pfade an, die in die Abfrage eingeschlossen werden sollen. Der Wert muss ein VT \_ LPWSTR oder ein VT- \_ Vektor \| VT \_ LPWSTR sein.                                 |
| DBPROP \_ ci \_ - \_ bereichsflags 0x00000004    | Gibt an, wie die von der Eigenschaft DBPROP \_ CI include-Bereiche angegebenen Pfade \_ behandelt werden \_ sollen. Der Wert muss ein VT- \_ I4 oder ein VT \_ Vector \| VT I4 sein \_ . |
| DBPROP \_ ci \_ - \_ Abfragetyp 0x00000007     | Gibt den Typ der Abfrage an. Cdbcolid muss auf DB nullid festgelegt werden \_ .                                                                               |



 

In der folgenden Tabelle sind die Flags für die Eigenschaft DBPROP \_ ci \_ Scope \_ Flags aufgeführt:



| Wert                     | Bedeutung                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abfragen von \_ Deep 0x01          | Wenn dieser Wert festgelegt ist, wird angegeben, dass Dateien im Bereichs Verzeichnis und alle Unterverzeichnisse in den Ergebnissen enthalten sind. Wenn Clear, werden nur Dateien im Bereichs Verzeichnis in die Ergebnisse eingeschlossen. Darf nicht mit einer Abfrage Tiefe kombiniert werden \_ . |
| Abfrage des \_ virtuellen \_ Pfads 0x02 | Wenn festgelegt, wird angegeben, dass der Bereich ein virtueller Pfad ist. Wenn Clear, wird angegeben, dass es sich bei dem Bereich um ein physisches Verzeichnis handelt.                                                                                                         |



 

In der folgenden Tabelle sind die Abfrage Typen für die Eigenschaft DBPROP \_ ci- \_ Abfragetyp aufgelistet \_ :



| Wert                     | Bedeutung                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| Cinormale 0x00000000       | Eine reguläre Abfrage.                                                                                                   |
| Civirtualroots 0x00000001 | Die Abfrage fordert eine Liste der virtuellen Stämme des Katalogs an. Dieser Wert erfordert Administratorrechte. |
| Ciproperties 0x00000003   | Die Abfrage fordert eine Liste aller Eigenschaften an, die vom Index Dienst unterstützt werden.                            |
| Ciadminop 0x00000004      | Bei der Abfrage handelt es sich um einen administrativen Vorgang. Dieser Wert erfordert Administratorrechte.                           |



 

In der folgenden Tabelle werden die Eigenschaften aufgelistet, die Teil der Eigenschaft "DBPROPSET \_ queryext" sind.



| Wert                                      | Bedeutung                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ usecontentindex 0x00000002         | Gibt an, wie langsame Abfragen vom Index Dienst verarbeitet werden sollen. Der Wert muss ein VT-boolescher Wert sein \_ . TRUE gibt an, dass der Server diese Abfragen nicht ausführen kann.                                                                                    |
| DBPROP-Debug-Einschränkung \_ 0x00000003 | Gibt an, ob der Indizierungs Dienst das Kürzen von Ergebnissen durchführen soll. TRUE gibt an, dass der Server eine Kürzung der Ergebnisse auf eine Weise durchführen soll, mit der die Reaktionszeit für den Client optimiert wird. Der Wert muss ein VT-boolescher Wert sein \_ .             |
| DBPROP \_ useextendeddbtypes 0x00000004      | Gibt an, ob der Client VT- \_ Vektor Datentypen unterstützt. Wenn true, unterstützt der Client VT \_ Vector; Wenn false, wird der Server zum Konvertieren von VT- \_ Vektor Datentypen in VT- \_ Array Datentypen verwendet.  Der Wert muss ein VT- \_ boolescher Wert sein. |
| DBPROP \_ firstrows 0x00000007               | Gibt die zurück zugebende Zeilen Übereinstimmungen an. TRUE gibt an, dass der Server den ersten Satz übereinstimmender Zeilen zurückgeben soll. Wenn der Wert false ist, sollten die am besten passenden Zeilen zurückgegeben werden. Der Wert muss ein VT-boolescher Wert sein \_ .                                             |



 

In der folgenden Tabelle sind die Eigenschaften aufgelistet, die Teil der Eigenschaft "DBPROPSET \_ cifrmwrkcore ext" sind \_ .



| Wert/DBPROPID                 | Bedeutung                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP- \_ Computer 0x00000002       | Gibt die Namen der Computer an, auf denen eine Abfrage verarbeitet werden soll. Der Wert muss entweder "VT \_ BSTR" oder "VT \_ array \| VT \_ BSTR" lauten. |
| DBPROP- \_ Client- \_ CLSID 0x00000003 | Gibt eine Verbindungs Konstante für den Indizierungs Dienst an. Der Wert muss eine VT CLSID sein, die \_ 0x2a4880706f 80800a0c906241a enthält.  |



 

### <a name="22122-cdbpropset"></a>2.2.1.22 CDBPropSet

Die CDBPropSet-Struktur enthält eine Reihe von Eigenschaften. Beachten Sie, dass das erste Feld eine fest Größe hat, aber möglicherweise nicht an einem Offset ausgerichtet ist, bei dem es sich um ein 4-Byte-vielfache vom Beginn der Nachricht mit dieser Struktur handelt. Das Feld "cproperties" wird jedoch als solches ausgerichtet, weshalb das Format wie folgt dargestellt wird:



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

\_Auffüll Zeichen (Variable)

cproperties

a-Eigenschaften (Variable)



 

**guidPropertySet**: eine GUID, die den Eigenschaften Satz identifiziert. Muss auf das binäre Format festgelegt werden, das einem der folgenden Werte entspricht (im Formular der Zeichen folgen Darstellung dargestellt), und identifiziert den Eigenschaften Satz der Eigenschaften, die im Feld "aproperties" enthalten sind.



| Wert/GUID                                                                              | Name                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| DBPROPSET " \_ f-frmwrk" \_<br/> {A9BD1526-6A80-11D0-8C9D-0020AF1D740E}<br/>   | Framework-Eigenschaften Satz für Datei System-Inhalts Index |
| DBPROPSET \_ queryext<br/> {A7AC77ED-F8D7-11CE-A798-0020F8008025}<br/>          | Eigenschaften Satz für Abfrageerweiterung                     |
| DBPROPSET \_ cifrmwrkcore- \_ ext<br/> {AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}<br/> | Inhalts Index Framework-Kerneigenschaften Satz        |



 

**\_ Auffüllung**: Dieses Feld muss zwischen 0 und 3 Byte lang sein. Die Länge dieses Felds muss so lauten, dass das folgende Feld bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die diese Struktur enthält. Wenn dieses Feld vorhanden ist (d. h. eine Länge ungleich 0 (null)), ist der enthaltene Wert beliebig. Der Inhalt dieses Felds muss vom Empfänger ignoriert werden.

**cproperties**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im aproperties-Array enthält.

**aproperties**: ein Array aus cdbprop-Strukturen, wie in Abschnitt 0 angegeben, das Eigenschaften enthält. Strukturen im Array müssen durch 0 bis 3 Auffüll Bytes voneinander getrennt werden, sodass jede Struktur bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die dieses Array enthält. Wenn Auffüll-Bytes vorhanden sind, ist der Wert, den Sie enthalten, willkürlich. Der Inhalt der Auffüll Zeichen muss vom Empfänger ignoriert werden.

### <a name="22123-cpidmapper"></a>2.2.1.23 cpidmapper

Die cpidmapper-Struktur enthält ein Array von Eigenschaften-IDs, die die Eigenschaften angeben, die in einem Rowset zurückgegeben werden sollen.



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

apropspec

... veränder



 

**count**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im apropspec-Array enthält.

**apropspec**: Array von cfullpropspec-Strukturen, die die zurück zugebende Eigenschaften angeben. Strukturen im Array müssen durch 0 bis 3 Auffüll Zeichen voneinander getrennt werden, sodass jede Struktur über eine 4-Byte-Ausrichtung ab dem Anfang einer Nachricht verfügt. Bei solchen Füll Zeichen kann es sich um beliebige Werte handeln, die bei der Bestätigung ignoriert werden müssen.

### <a name="22124-crowseekat"></a>2.2.1.24 crowseekat

Die crowseekat-Struktur enthält den Offset, bei dem Zeilen in einer cpmgetrowsin-Nachricht abgerufen werden sollen.



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

\_hregion

\_cskip

\_bmkoffset



 

**\_ hregion**: muss auf 0x00000000 festgelegt werden und muss ignoriert werden.

**\_ cskip**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeilen enthält, die im Rowset übersprungen werden sollen.

**\_ bmkoffset**: ein 32-Bit-Wert, der das Handle des **Lesezeichens** darstellt, das die Anfangsposition angibt, ab der die Anzahl der in cskip angegebenen Zeilen vor dem Abruf übersprungen \_ werden soll.

### <a name="22125-crowseekatratio"></a>2.2.1.25 crowseekatratio

Die crowseekatratio-Struktur gibt den Punkt an, an dem mit dem Abrufen einer cpmgetrowsin-Nachricht begonnen werden soll.



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

Citblchapt

\_hregion

\_ulnumerator

\_ulnenner



 

**Citblchapt**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Rowset-Kapitel angibt, aus dem Zeilen abgerufen werden sollen.

**\_ hregion**: muss auf 0x00000000 festgelegt werden und muss ignoriert werden.

**\_ ulnumerator**: ganze Zahl ohne Vorzeichen mit einer Länge von 32 Bit, die den Zähler des Verhältnis von Zeilen in dem Kapitel darstellt, ab dem der Abruf begonnen werden soll.

**\_ ulnenner**: unsignierte 32-Bit-Ganzzahl, die den Nenner des Verhältnis von Zeilen in dem Kapitel darstellt, ab dem der Abruf begonnen werden soll. Muss größer als 0 (null) sein.

### <a name="22126-crowseekbybookmark"></a>2.2.1.26 crowseekbybookmark

Die crowseekbybookmark-Struktur gibt die Lesezeichen an, aus denen mit dem Abrufen von Zeilen für eine cpmgetrowsin-Nachricht begonnen werden soll.



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

\_hregion

\_cbookmarks

\_maxret

\_cvalidret

\_abookmarks (Variable)

\_askret (Variable)



 

**\_ hregion**: muss auf 0x00000000 festgelegt werden und muss ignoriert werden.

**\_ cbookmarks**: nicht signierte 32-Bit-Ganzzahl, die die Anzahl der Elemente im \_ abookmarks-Array darstellt.

**\_ maxret**: unsigned 32-Bit-Ganzzahl, die die Anzahl der Elemente im \_ askret-Array darstellt.

**\_ cvalidret**: unsignierte 32-Bit-Ganzzahl, die die Anzahl der gültigen Elemente im \_ askret-Array darstellt. Gültige Elemente wurden im Array definiert, ungültige Elemente sind jedoch nicht definiert.

**\_ abookmarks**: ein Array von Lesezeichen Handles (jedes dargestellt durch 4 Bytes), wie von einer cpmgetrowsout-Nachricht abgerufen.

**\_ askret**: ein Array von HRESULT-Werten. Wenn das crowseekbybookmark-Element als Teil der cpmgetrowsin-Anforderung gesendet wird, muss die Anzahl der Einträge im Array gleich \_ clese Zeichen sein. Wenn Sie vom Client gesendet werden, müssen die Werte auf 0 (null) festgelegt werden, und der Server muss den Inhalt des Arrays ignorieren. Wenn Sie vom Server gesendet werden (als Teil der cpmgetrowsout-Nachricht), geben die Werte im Array den Ergebnis Status für die einzelnen Zeilen Abruf Vorgänge an.

### <a name="22127-crowseeknext"></a>2.2.1.27 crowseeknext

Die crowseeknext-Struktur enthält die Anzahl der Zeilen, die in einer cpmgetrowsin-Nachricht übersprungen werden sollen.



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

Citblchapt

\_hregion

\_cskip



 

**Citblchapt**: Vorzeichen lose 32-Bit-Ganzzahl, die das Rowset-Kapitel angibt, aus dem Zeilen abgerufen werden sollen.

**\_ hregion**: muss auf 0x00000000 festgelegt werden und muss ignoriert werden.

**\_ cskip**: unsignierte 32-Bit-Ganzzahl, die die Anzahl der Zeilen darstellt, die im Rowset übersprungen werden sollen.

### <a name="22128-crowsetproperties"></a>2.2.1.28 crowsetproperties

Die crowsetproperties-Struktur enthält Konfigurationsinformationen für eine Abfrage.



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

\_ubooleanoptions

\_ulmaxopenrows

\_ulmemoryusage

\_cmaxresults

\_ccmdtimeout



 

**\_ ubooleanoptions**: die am wenigsten wichtigen 3 Bits dieses Felds müssen einen der folgenden drei Werte enthalten:



| Wert                  | Bedeutung                                                             |
|------------------------|---------------------------------------------------------------------|
| esequential 0x00000001 | Der Cursor kann nur vorwärts verschoben werden.                              |
| elocabel 0x00000003  | Der Cursor kann an eine beliebige Position verschoben werden.                            |
| escrollable 0x00000007 | Der Cursor kann an eine beliebige Position verschoben und in beliebiger Richtung abgerufen werden. |



 

Die übrigen Bits sind entweder eindeutig oder können auf eine beliebige Kombination der folgenden Werte logisch oder zusammengesetzt werden:



| Wert                     | Bedeutung                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| easynchronous 0x00000008  | Der Client wartet nicht auf den Abschluss der Ausführung.                                                          |
| efirstrows 0x00000080     | Gibt die ersten gefundenen Zeilen zurück, nicht die besten Übereinstimmungen.                                                    |
| eholdrows 0x00000200      | Der Server darf die Zeilen erst verwerfen, wenn der Client mit einer Abfrage abgeschlossen ist.                                     |
| echtem 0x00000800     | Das Rowset unterstützt Kapitel.                                                                               |
| eueinci 0x00001000         | Beantworten Sie die Abfrage nur über den Index, nicht über das Dateisystem.                                                  |
| edeferkürzen 0x00002000 | Der Indizierungs Dienst sollte die Reaktionszeit beim Entfernen von Ergebnissen an den Client optimieren. |



 

**\_ ulmaxopenrows**: ganze Zahl ohne Vorzeichen (32 Bit). Muss auf 0x00000000 festgelegt werden. Wird nicht verwendet und muss ignoriert werden.

**\_ ulmemoryusage**: ganze Zahl ohne Vorzeichen (32 Bit). Muss auf 0x00000000 festgelegt werden. Wird nicht verwendet und muss ignoriert werden.

**\_ cmaxresults**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die maximale Anzahl von Zeilen angibt, die für die Abfrage zurückgegeben werden sollen.

**\_ ccmdtimeout**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Sekunden angibt, nach der eine Abfrage ein Timeout und eine automatische Beendigung der Abfrage angibt, die von dem Zeitpunkt der Ausführung der Abfrage auf dem Server gezählt wird. Der Wert 0x00000000 bedeutet, dass für die Abfrage kein Timeout auftritt.

### <a name="22129-crowvariant"></a>2.2.1.29 crowvariant

Die crowvariant-Struktur enthält den Teil mit fester Größe eines Datentyps variabler Länge, der in der cpmgetrowsout-Nachricht gespeichert ist.



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

VType

"reserved1"

reserved2

Offset (optional)



 

**VType**: ein Typindikator, der den Typ von vValue angibt. Dabei muss es sich um einen der varenumum-Werte handeln, die im Abschnitt 2.2.1.1 angegeben sind.

**"reserved1"**: nicht verwendet. Der Wert kann auf einen beliebigen Wert festgelegt werden, und er muss beim Empfang ignoriert werden.

**"reserved2"**: nicht verwendet. Der Wert kann auf einen beliebigen Wert festgelegt werden, und er muss beim Empfang ignoriert werden.

**Offset**: ein Offset zu Daten variabler Länge (z. b. eine Zeichenfolge).  Dies muss ein 32-Bit-Wert (4 Bytes) sein, wenn 32-Bit-Offsets (gemäß den Regeln im Abschnitt 2.2.3.16) verwendet werden, oder ein 64-Byte-Wert (8 Bytes lang), wenn 64-Bit-Offsets verwendet werden.

### <a name="22130-csortset"></a>2.2.1.30 csortset

Die csortset-Struktur enthält die Sortierreihenfolge der Abfrage.



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

SortArray (Variable)



 

**count**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente in SortArray angibt.

**SortArray**: ein Array von csort-Strukturen, die die Reihenfolge beschreiben, in der die Ergebnisse der Abfrage sortiert werden. Strukturen im Array müssen durch 0 bis 3 Auffüll Zeichen voneinander getrennt werden, sodass jede Struktur über eine 4-Byte-Ausrichtung ab dem Anfang einer Nachricht verfügt. Bei solchen Füll Zeichen kann es sich um beliebige Werte handeln, die bei der Bestätigung ignoriert werden müssen.

### <a name="22131-ctablecolumn"></a>2.2.1.31 ctablecolumn

Die ctablecolumn-Struktur enthält eine Spalte einer cpmsetbindingsin-Nachricht.



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

PROPSPEC

... veränder

VType

Valueused

\_padding1 (optional)

Valueoffset (optional)

Valuesize (optional)

Status ausgewertet

\_padding2 (optional)

Status-ffset (optional)

Verlängert

\_padding3 (optional)

Längen Offset (optional)



 

**PROPSPEC**: eine cfullpropspec-Struktur, wie im Abschnitt 2.2.1.3 angegeben.

**VType**: gibt den Typ des in der Spalte enthaltenen Daten Werts an. Eine Liste der Werte für dieses Feld finden Sie im Feld "VType" im Abschnitt "2.2.1.1".

**Valueused**: ein 1-Byte-Feld, das auf 0x01 oder 0x00 festgelegt werden muss. Wenn der Wert auf 0x01 festgelegt ist, wird die Spalte innerhalb der Zeile mit fester Größe übertragen. Wenn Sie auf 0x00 festgelegt ist, wird der Wert der Spalte im Abschnitt variabler Länge am Ende des Puffers übertragen.

**\_ padding1**: ein 1-Byte-Feld, das vor valueoffset eingefügt werden muss, wenn valueoffset nicht bei einem geraden Offset vom Anfang der Nachricht beginnt. Der Wert dieses Byte ist willkürlich und muss ignoriert werden. Wenn valueused auf 0x00 festgelegt ist, darf dieses Feld nicht vorhanden sein.

**Valueoffset**: eine ganze 2-Byte-Ganzzahl ohne Vorzeichen, die den Offset des Spaltenwerts in der Zeile angibt. Wenn valueused auf 0x00 festgelegt ist, darf dieses Feld nicht vorhanden sein.

**Valuesize**: eine ganze 2-Byte-Ganzzahl ohne Vorzeichen, die die Größe des Spaltenwerts in Bytes angibt. Wenn valueused auf 0x00 festgelegt ist, darf dieses Feld nicht vorhanden sein.

**Status**: ein Byte-Feld, das auf 0x01 oder 0x00 festgelegt werden muss. Wenn der Wert auf 0x01 festgelegt ist, wird der Status der Spalte innerhalb der Zeile übertragen. Bei 0x00 wird der Status der Spalte nicht innerhalb der Zeile übertragen.

**\_ padding2**: ein 1-Byte-Feld, das vor statusoffset eingefügt werden muss, wenn das statusoffset-Feld ohne dieses Feld nicht am Anfang der Nachricht mit einem geraden Offset beginnen würde. Der Wert dieses Byte ist willkürlich und muss ignoriert werden. Wenn "Status" auf "0x00" festgelegt ist, darf dieses Feld nicht vorhanden sein.

**Statusoffset**: eine ganze 2-Byte-Ganzzahl ohne Vorzeichen, die den Offset des Spalten Status in der Zeile angibt. Wenn "Status" auf "0x00" festgelegt ist, darf dieses Feld nicht vorhanden sein.

**Verlängert**: ein Byte-Feld, das auf 0x01 oder 0x00 festgelegt werden muss. Wenn der Wert auf 0x01 festgelegt ist, wird die Länge der Spalte innerhalb der Zeile übertragen. Wenn 0x00, darf die Länge der Spalte nicht innerhalb der Zeile übertragen werden.

**\_ padding3**: ein 1-Byte-Feld, das vor dem Längen Offset eingefügt werden muss, wenn, ohne es ist, der Längen Offset nicht bei einem geraden Offset vom Anfang einer Nachricht beginnen würde. Der Wert dieses Byte ist willkürlich und muss ignoriert werden. Wenn die Längen Verwendung auf 0x00 festgelegt ist, darf dieses Feld nicht vorhanden sein.

**Längen Offset**: eine Vorzeichen lose 2-Byte-Ganzzahl, die den Offset der Spaltenlänge in der Zeile angibt. Wenn die Längen Verwendung auf 0x00 festgelegt ist, darf dieses Feld nicht vorhanden sein.

### <a name="22132-serializedpropertyvalue"></a>2.2.1.32 serializedpropertyvalue

Die serializedpropertyvalue-Struktur enthält einen serialisierten Wert.



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

RGB (Variable)



 

**dwType**: einer der Variant-Typen, der im Abschnitt 2.2.1.1 definiert ist und mit Varianten Typmodifizierer kombiniert werden kann. Für alle Variant-Typen, mit Ausnahme derjenigen, die mit dem VT- \_ Array kombiniert werden, hat serializedpropertyvalue dasselbe Layout wie cbasestoragevariant, wie im Abschnitt 2.2.1.1 angegeben. Wenn der Variant-Typ mit dem VT \_ -Arraytypmodifizierer kombiniert wird, wird SAFEARRAY2, der in Abschnitt 2.2.1.2.1.1 angegeben wird, anstelle von SAFEARRAY im vValue-Feld von cbasestoragevariant verwendet.

**RGB**: serialisierter Wert. Weitere Informationen finden Sie in den Details der Serialisierung für vValue in 2.2.1.1.

### <a name="222-message-headers"></a>2.2.2-Nachrichten Header

Alle Protokollnachrichten für den Inhalts Indizierungs Dienst haben einen 16-Byte-Header.

Im folgenden finden Sie ein Diagramm, das das Format des Content Index Service Protocol Message Headers anzeigt.



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

\_Meldung

\_Stands

\_ulchecksum

\_ulReserved2



 

\_**msg**: eine 32-Bit-Ganzzahl, die den Typ der Nachricht angibt, die auf den Header folgt. In der folgenden Tabelle werden die Protokollnachrichten für den Inhalts Indizierungs Dienst und die für jede Nachricht angegebenen ganzzahligen Werte aufgelistet. Wie in der Tabelle gezeigt, identifizieren einige Werte zwei Nachrichten in der Tabelle. In diesen Fällen kann die Nachricht, die auf den Header folgt, durch die Richtung des Nachrichten Flusses identifiziert werden. Wenn die Richtung "Client zu Server" lautet, wird die Meldung mit dem Namen "in" angezeigt, die an den Nachrichten Namen angehängt ist. Wenn die Richtung Server zu Client ist, wird die Meldung mit dem Namen "out" angezeigt, die an den Nachrichten Namen angehängt ist.



| Wert      | Bedeutung                                                     |
|------------|-------------------------------------------------------------|
| 0x000000c8 | Cpmconnectin oder cpmconnectout                               |
| 0x000000c9 | Cpmdisconnect                                               |
| 0x000000CA | Cpmkreatequeryin oder cpmkreatequeryout                       |
| 0x000000cb | Cpmfreecursorin oder cpmfreecursorout                         |
| 0x000000cc | Cpmgetrowsin oder cpmgetrowsout                               |
| 0x000000CD | Cpmratiofinishedin oder cpmratiofinishedout                   |
| 0x000000CE | Cpmcomparebmkin oder cpmcomparebmkout                         |
| 0x000000cf | Cpmgetapproximatepositionin oder cpmgetapproximatepositionout |
| 0x000000d0 | Cpmsetbindingsin                                            |
| 0x000000D1 | Cpmgetnotify                                                |
| 0x000000d2 | Cpmsendnotimayout                                            |
| 0x000000d7 | Cpmgetquerystatus oder cpmgetquerystatus                 |
| 0x000000d9 | Cpmcistatus out                                             |
| 0x000000e1 | Cpmforcemergein                                             |
| 0x000000e4 | Cpmfetchvaluein oder cpmfetchvalueout                         |
| 0x000000e6 | Cpmupdatedocumentsin                                        |
| 0x000000e7 | Cpmgetquerystatusexin oder pmgetquerystatusexout              |
| 0x000000e8 | Cpmrestartpositionin                                        |
| 0x000000e9 | Cpmstopasynchin                                             |
| 0x000000ec | Cpmsetsestatein oder cpmset-stateout                       |



 

\_**Status**: ein HRESULT \[ ms-sys \] , das den Status des angeforderten Vorgangs angibt.

\* *

*Windows-Verhalten: der Client legt das \_ Feld "Status" immer auf "0x00000000" fest.*

**\_ ulchecksum**: die \_ ulchecksum-Angabe muss in Abschnitt 3.2.4 für die folgenden Meldungen berechnet werden:

-   Cpmconnectin
-   Cpmkreatequeryin
-   Cpmsetbindingsin
-   Cpmgetrowsin
-   Cpmfetchvaluein

Für alle anderen Nachrichten \_ muss ulchecksum auf 0x00000000 festgelegt werden. Ein Client muss das \_ ulchecksum-Feld ignorieren.

**\_ ulReserved2**: muss auf 0 festgelegt und vom Empfänger ignoriert werden.

### <a name="223-messages"></a>2.2.3 Nachrichten

### <a name="2231-cpmcistateinout"></a>2.2.3.1 cpmcistatus out

Die cpmcistateinout-Nachricht enthält Informationen zum Status des Indizierungs Dienstanbieter. Das Format der cpmcistateinout-Nachricht, die auf den Header folgt, lautet:



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

cwordlist

cpersistentindex

cqueries

CDocuments

cfreshtest

dwmergeprogress

gut

cfiltereddocuments

ctotaldocuments

cpdingscans

dwindexsize

cuniquekeys

csecqdocuments

dwpropcachesize



 

**cbStruct**: eine 32-Bit-Ganzzahl ohne Vorzeichen. Die Größe dieser Nachricht in Bytes (mit Ausnahme des allgemeinen Headers). Muss auf 0x0000003c festgelegt werden.

**cwordlist**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der anfänglichen Indizes angibt, die für zuletzt indizierte Dokumente erstellt wurden.

**cpersistentindex**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der persistenten Indizes angibt.

**cqueries**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die eine Reihe von aktiv ausgelaufenden Abfragen angibt.

**CDocuments**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Dokumente angibt, die auf die Indizierung warten.

**cfreshtest**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von eindeutigen Dokumenten mit Informationen in Indizes angibt, die nicht vollständig für die Leistung optimiert sind.

**dwmergeprogress**: Vorzeichen lose 32-Bit-Ganzzahl ohne Vorzeichen, die den Abschluss Prozentsatz der aktuellen vollständigen Optimierung von Indizes angibt, wenn die Optimierung derzeit ausgeführt wird. Muss kleiner oder gleich 100 sein.

**eState**: Zustand der Inhalts Indizierung, wie von einer oder mehreren der CI- \_ Zustands \_ \* Konstanten angegeben, die in der folgenden Tabelle definiert sind.



| Wert                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CI- \_ Zustands \_ Schatten \_ Zusammenführung 0x00000001           | Der Indizierungs Dienst wird gerade einige der Indizes optimieren, um die Speicherauslastung zu reduzieren und die Abfrageleistung zu verbessern.                                                                                                                                                                                                                                                                                                                                                                |
| CI- \_ Status \_ Master \_ Merge 0x00000002           | Der Indizierungs Dienst wird für alle Indizes vollständig optimiert.                                                                                                                                                                                                                                                                                                                                                                                                                  |
| CI- \_ Status- \_ Inhalts \_ Scan \_ erforderlich 0x00000004 | Einige Dokumente im Index wurden geändert, und der Indizierungs Dienst muss bestimmen, welche hinzugefügt, geändert oder gelöscht wurden.                                                                                                                                                                                                                                                                                                                                                              |
| CI- \_ Status- \_ \_ Anfügen 0x00000008        | Der Indizierungs Dienst optimiert Indizes, um die Speicherauslastung zu reduzieren und die Abfrageleistung zu verbessern. Dieser Prozess ist umfassender als der vom CI- \_ Status- \_ \_ schattenmerge-Wert identifizierte, aber er ist nicht so umfassend wie durch den CI- \_ Status Master-Merge-Wert angegeben \_ \_ . Solche Optimierungen sind Implementierungs spezifisch, da Sie von der internen Speicherung von Daten abhängen. die Optimierungen wirken sich nicht auf das Protokoll in anderer Weise aus als der Antwortzeit. |
| CI- \_ Status Überprüfung \_ 0x00000010                | Der Indizierungs Dienst untersucht ein Verzeichnis oder eine Gruppe von Verzeichnissen, um zu ermitteln, ob seit der letzten Indizierung des Verzeichnisses Dateien hinzugefügt, gelöscht oder aktualisiert wurden.                                                                                                                                                                                                                                                                                                                 |
| CI-Status bei wieder \_ \_ Herstellung von 0x00000020              | Der Dienst beginnt mit dem zuletzt gespeicherten Zustand und wird gerade wieder hergestellt.                                                                                                                                                                                                                                                                                                                                                                                                        |
| CI- \_ Status \_ wenig Arbeits \_ Speicher 0x00000080             | Der größte Teil des virtuellen Speichers des Servers wird verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| CI-Status hoch-e/a \_ \_ \_ 0x00000100                | Die Ebene der Eingabe-/Ausgabeaktivität (e/a) auf dem Server ist relativ hoch.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CI- \_ Status \_ Master \_ Zusammenführung \_ angehalten 0x00000200   | Der Prozess der vollständigen Optimierung für alle Indizes, die gerade ausgeführt wurden, wurde angehalten. Dies wird nur für informative Zwecke angegeben und wirkt sich nicht auf CISP aus.                                                                                                                                                                                                                                                                                                                                  |
| CI-Status schreibgeschützt \_ \_ \_ 0x00000400              | Der Teil des Indizierungs Dienstanbieter, der neue Dokumente für die Indexerstellung aufnimmt, wurde angehalten. Dies wird nur für informative Zwecke angegeben und wirkt sich nicht auf CISP aus.                                                                                                                                                                                                                                                                                                                               |
| CI- \_ State \_ Akku \_ Power 0x00000800          | Der Teil des Indizierungs Dienstanbieter, der neue Dokumente für die Indexerstellung aufnimmt, wurde angehalten, um die Akku Lebensdauer zu sparen, aber dennoch Antworten auf die Abfragen. Dies wird nur für informative Zwecke angegeben und wirkt sich nicht auf CISP aus.                                                                                                                                                                                                                                                                 |
| CI- \_ Status \_ Benutzer \_ aktiv 0x00001000            | Der Teil des Indizierungs Dienstanbieter, der neue Dokumente für den Index abruft, wurde aufgrund einer hohen Aktivität durch den Benutzer (Tastatur oder Maus) angehalten, antwortet aber immer noch auf die Abfragen. Dies wird nur für informative Zwecke angegeben und wirkt sich nicht auf CISP aus.                                                                                                                                                                                                                                         |
| CI- \_ Status \_ beginnend 0x00002000                | Der Dienst wird gestartet. Abfragen können ausgeführt werden, aber das Scannen und die Benachrichtigung wurden noch nicht aktiviert. Dies wird nur für informative Zwecke angegeben und wirkt sich nicht auf CISP aus.                                                                                                                                                                                                                                                                                                                   |
| CI- \_ Status \_ Lesen von \_ USNs 0x00004000           | Der Dienst hat das vom Dateisystem beibehaltene Protokoll nicht gelesen, um Änderungen an Dateien oder Verzeichnissen in einem Volume nachzuverfolgen, sodass der Index möglicherweise nicht auf dem neuesten Stand ist.                                                                                                                                                                                                                                                                                                                                  |



 

**cfiltereddocuments**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dokumente angibt, die seit Beginn der Inhalts Indizierung indiziert wurden.

**ctotaldocuments**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Dokumente im System angibt.

**cpdingscans**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von ausstehenden Index Vorgängen auf hoher Ebene angibt. Die Bedeutung dieses Werts ist Anbieter spezifisch, aber größere Zahlen erwarten, dass mehr Indizierung übrig bleibt.

*Windows-Verhalten*: dieser Wert ist in der Regel 0 (null), mit dem Unterschied, dass die Indizierung nicht unmittelbar nach dem Start der Indizierung oder

**dwindexsize**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des Indexes (ohne den Eigenschafts Cache) in Megabyte angibt.

**cuniquekeys**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die ungefähre Anzahl eindeutiger Schlüssel im Katalog angibt.

**csecqdocuments**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dokumente angibt, die der Indizierungs Dienst aufgrund eines Fehlers während des anfänglichen Indizierungs Versuchs neu indizieren wird.

**dwpropcachesize**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des Eigenschafts Caches in Megabyte angibt.

### <a name="2232-cpmsetcatstatein"></a>2.2.3.2 cpmsetsestatuein

Die cpmsetsinstatein-Meldung legt den Status eines Katalogs fest. Das Format der cpmsetingstatein-Nachricht, die auf den Header folgt, lautet:



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

\_dwnewstate

\_Name der Kategorie (Variable, optional)



 

**\_ partid**: muss auf 0x00000001 festgelegt werden.

**\_ dwnewstate**: muss auf einen der folgenden Werte festgelegt werden, um den neuen Status des Katalogs anzugeben.



| Wert                         | Bedeutung                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cicat hat \_ 0x00000001 beendet.     | Der Katalog wurde beendet. Dieser Status bedeutet, dass keine neuen Dateien indiziert werden müssen, und es werden keine Such Abfragen verarbeitet.                                                     |
| Cicat schreibgeschützt \_ 0x00000002    | Der Katalog ist schreibgeschützt. Es werden keine neuen Dateien indiziert.                                                                                                               |
| Cicat \_ beschreibbare 0x00000004    | Der Katalog ist beschreibbar. Neue Dateien können indiziert und Such Abfragen verarbeitet werden.                                                                              |
| Cicat \_ keine \_ Abfrage 0x00000008   | Der Katalog ist nicht für Abfragen verfügbar.                                                                                                                              |
| Cicat \_ get \_ State 0x00000010  | Der Status des Katalogs soll nicht geändert werden, sondern nur abgerufen werden.                                                                                                          |
| Cicat \_ alle \_ geöffneten 0x00000020 | Eine Überprüfung, ob alle Kataloge gestartet wurden. Wenn dies der Fall ist, \_ wird das in der cpmsetsinstateout-Antwort an diese Nachricht gesendete dwoldstate-Feld als ungleich 0 (null) gemeldet. |



 

" **Name": der \_** Name des Katalogs, dessen Status geändert werden soll. Der Name muss eine NULL-terminierte Unicode-Zeichenfolge sein. Dieses Feld muss weggelassen werden, wenn " \_ dwnewstate" auf "cicat all geöffnet" festgelegt ist \_ \_ .

### <a name="2233-cpmsetcatstateout"></a>2.2.3.3 cpmset| stateout

Bei der cpmsetsinstateout-Nachricht handelt es sich um eine Antwort auf eine cpmsetsinstatein-Nachricht mit dem alten Status des Katalogs. Das Format der cpmset-stateout-Nachricht, die auf den Header folgt, lautet:



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

\_dwoldstate



 

**\_ dwoldstate**: einer der folgenden Werte, der den alten Status des Katalogs angibt.



| Wert                       | Bedeutung                                    |
|-----------------------------|--------------------------------------------|
| Cicat hat \_ 0x00000001 beendet.   | Der Katalog wurde beendet.                    |
| Cicat schreibgeschützt \_ 0x00000002  | Der Katalog ist schreibgeschützt.                  |
| Cicat \_ beschreibbare 0x00000004  | Der Katalog ist beschreibbar.                   |
| Cicat \_ keine \_ Abfrage 0x00000008 | Der Katalog ist nicht für Abfragen verfügbar. |



 

### <a name="2234-cpmupdatedocumentsin"></a>2.2.3.4 cpmupdatedocumentsin

Die cpmupdatedocumentsin-Nachricht weist den Server an, den angegebenen Pfad zu indizieren.

Der Server antwortet mit dem Nachrichten Header der cpmupdatedocumentsout-Nachricht, wobei die Ergebnisse der Anforderung im \_ Feld Status des Nachrichten Headers enthalten sind.

Das Format der cpmupdatedocumentsin-Nachricht, die auf den Header folgt, lautet:



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

\_frootpath (optional)

RootPath (Variable, optional)



 

**\_ Flag**: der Typ des auszuführenden Updates. Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird. Dieses Feld muss auf einen der folgenden Werte festgelegt werden:



| Wert                  | Bedeutung                                   |
|------------------------|-------------------------------------------|
| UPD \_ increm 0x00000000 | Es muss ein inkrementelles Update durchgeführt werden. |
| UPD \_ vollständig 0x00000001   | Es muss ein vollständiges Update durchgeführt werden.         |
| UPD \_ Init 0x00000002   | Es muss eine neue Initialisierung durchgeführt werden.  |



 

**\_ frootpath**: ein boolescher Wert, der angibt, ob das Feld RootPath einen Pfad angibt, in dem das Update durchgeführt werden soll. Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird. Dieses Feld muss auf 0x00000001 oder 0x00000000 festgelegt werden. Bei Festlegung auf 0x00000001 ist ein Pfad, in dem das Update durchgeführt werden soll, in RootPath enthalten. Wenn der Wert auf 0x00000000 festgelegt ist, wird das Update für alle indizierten Pfade ausgeführt.

**RootPath**: der Name des Pfads, der aktualisiert werden soll. Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird. Der Name muss eine NULL-terminierte Unicode-Zeichenfolge sein. Dieses Feld muss weggelassen werden \_ , wenn frootpath auf 0x00000000 festgelegt ist.

### <a name="2235-cpmforcemergein"></a>2.2.3.5 cpmforcemergein

Mit der cpmforcemergein-Meldung wird ein Server aufgefordert, jede erforderliche Wartung auszuführen, um die Abfrageleistung zu verbessern. Der Server antwortet mit dem Nachrichten Header der cpmforcemergein-Nachricht, wobei die Ergebnisse der im Feld Status enthaltenen Anforderung angezeigt werden \_ .

Das Format der cpmforcemergein-Nachricht, die auf den Header folgt, lautet:



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

\_partitiond (optional)



 

**\_ partitiond**: Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird. Wenn dieses Feld vorhanden ist, muss es auf 0x00000001 festgelegt werden.

### <a name="2236-cpmconnectin"></a>2.2.3.6 cpmconnectin

Die cpmconnectin-Nachricht beginnt eine Sitzung zwischen dem Client und dem Server.

Das Format der cpmconnectin-Nachricht, die auf den Header folgt, lautet:



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

\_iclientversion

\_"lclientisremote"

\_cbBlob1

\_cbBlob2

\_Auffüllung

...

...

MachineName

... veränder

UserName

... veränder

\_paddingcpropsets (optional, Variable)

cpropsets

PropertySet1 (Variable)

PropertySet2 (Variable)

\_paddingextpropset (optional, Variable)

cextpropset

apropertysets (Variable)



 

**\_ iclientversion**: eine 32-Bit-Ganzzahl, die angibt, ob der Server den Prüfsummen Wert validieren soll, der im \_ Feld ulchecksum der Nachrichten Header für vom Client gesendete Nachrichten angegeben ist. Wenn das \_ Feld iclientversion auf 0x00000008 oder höher festgelegt ist, muss der Server den \_ ulchecksum-Feldwert für die folgenden Meldungen überprüfen:

-   Cpmconnectin
-   Cpmkreatequeryin
-   Cpmfetchvaluein
-   Cpmgetrowsin
-   Cpmsetbindingsin

Ausführliche Informationen dazu, wie der-Server den vom Client angegebenen Wert im Feld ulchecksum für die oben aufgeführten Nachrichten überprüft, finden Sie im Abschnitt 3.2.5.

Wenn der Wert größer als 0x00000008 ist, wird angenommen, dass der Client 64-Bit-Offsets in cpmgetrowsout-Nachrichten verarbeiten kann. Weitere Informationen finden Sie im Abschnitt 2.2.3.16.

*Windows-Verhalten: auf Windows-Clients wird iclientversion wie folgt festgelegt*:



| Wert      | Bedeutung                                                              |
|------------|----------------------------------------------------------------------|
| 0x00000005 | Client Betriebssystem ist Windows 2000.                                           |
| 0x00000008 | Client Betriebssystem ist entweder 32 Bit Windows XP oder 32-Bit Windows Server 2003. |
| 0x00010008 | Client Betriebssystem ist entweder 64 Bit Windows XP oder 64-Bit Windows Server 2003. |



 

\_**fclientisremote**: ein boolescher Wert, der angibt, ob der Client auf einem anderen Computer als der Server ausgeführt wird. Muss auf 0x00000001 festgelegt werden.

\_**cbBlob1**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe in Bytes der cpropset-, PropertySet1-und PropertySet2-Felder kombiniert.

\_**cbBlob2**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der Felder cexpropset und apropertyset in Bytes angibt.

\_**Auffüllung**: 12 Bytes an Auffüll Zeichen, die beliebige Werte enthalten können und ignoriert werden müssen.

**MachineName**: der Computername des Clients. Die namens Zeichenfolge muss ein mit Null endendes Array mit weniger als 512 Unicode-Zeichen sein, einschließlich des NULL-Terminator.

**Username**: eine Zeichenfolge, die den Benutzernamen der Person darstellt, von der die Anwendung ausgeführt wird, die dieses Protokoll aufgerufen hat. Die namens Zeichenfolge muss ein mit Null endendes Array von weniger als 512 Unicode-Zeichen sein, wenn Sie mit MachineName verkettet werden.

**\_ paddingcpropsets**: Dieses Feld muss zwischen 0 und 7 Byte lang sein. Die Anzahl der Bytes muss die Zahl sein, die erforderlich ist, um den Byte Offset des Felds cpropsets vom Anfang der Nachricht, die diese Struktur enthält, als Vielfaches von 8 festzulegen. Der Wert der Bytes kann ein beliebiger Wert sein und muss vom Empfänger ignoriert werden.

**cpropsets**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der CDBPropSet-Strukturen, die diesem Feld folgen, angibt. Dieser Wert muss auf 0x0000002 festgelegt werden.

**PropertySet1**: eine CDBPropSet-Struktur mit guidPropertySet mit DBPROPSET " \_ f-frmwrk \_ ext" (siehe Abschnitt 2.2.1.22)

**PropertySet2**: eine CDBPropSet-Struktur mit guidPropertySet, die DBPROPSET \_ cifrmwrkcore \_ ext enthält (siehe Abschnitt 2.2.1.22).

\_**Paddingextpropset**: Dieses Feld muss zwischen 0 und 7 Byte lang sein. Die Anzahl der Bytes muss die Zahl sein, die erforderlich ist, um den Byte Offset des Felds cextpropsets vom Anfang der Nachricht, die diese Struktur enthält, als Vielfaches von 8 festzulegen. Der Wert der Bytes kann ein beliebiger Wert sein und muss vom Empfänger ignoriert werden.

**cextpropset**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der CDBPropSet-Strukturen, die diesem Feld folgen, angibt.

**apropertysets**: ein Array von CDBPropSet-Strukturen, das andere Eigenschaften angibt. Die Anzahl der Elemente in diesem Array muss gleich cextpropset sein.

### <a name="2237-cpmconnectout"></a>2.2.3.7 cpmconnectout

Die cpmconnectout-Nachricht enthält eine Antwort auf eine cpmconnectin-Nachricht.

Das Format der cpmconnectout-Nachricht, die auf den Header folgt, lautet:



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

\_Server Version

\_reserviert (Variable)



 

**\_ Server Version**:

Eine 32-Bit-Ganzzahl, die angibt, ob der Server 64-Bit-Offsets unterstützen kann *.* Weitere Informationen finden Sie im Abschnitt 2.2.3.16.



| Wert      | Bedeutung                                 |
|------------|-----------------------------------------|
| 0x00000007 | Der Server kann nur 32-Bit-Offsets senden. |
| 0x00010007 | Der Server kann 32-oder 64-Bit-Offsets senden.   |



 

**\_ reserviert**: reserviert. Der Server sendet möglicherweise eine beliebige Anzahl beliebiger Werte, und der Client muss diese Werte ignorieren, falls vorhanden.

### <a name="2238-cpmcreatequeryin"></a>2.2.3.8 cpmkreatequeryin

Die cpmkreatequeryin-Meldung erstellt eine neue Abfrage. Das Format der cpmkreatequeryin-Nachricht, die auf den Header folgt, lautet:



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

Ccolumnsetpresent

ColumnSet (optional)

... veränder

"Krestrictionpresent".

Einschränkung (optional)

... veränder

Csortsetpresent

Sortset (optional)

... veränder

Ccategorizationsetpresent

Kategorisierungs Satz (optional)

... veränder

Rowsetproperties

...

...

...

...

Pidmapper (Variable)



 

**Size**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Bytes vom Anfang dieses Felds bis zum Ende der Nachricht angibt.

**Ccolumnsetpresent**: ein Bytefeld, das angibt, ob das ColumnSet-Feld vorhanden ist. Dieses Feld muss auf 0x01 oder 0x00 festgelegt werden. Wenn der Wert auf 0x01 festgelegt ist, muss das ccolumnset-Feld vorhanden sein. Wenn der Wert auf 0x00 festgelegt ist, muss er nicht vorhanden sein.

**ColumnSet**: eine ccolumnset-Struktur, die die Spalten Nummern enthält, in denen die cpidmapper-Eigenschaften zurückgegeben werden sollen.

" **Krestrictionpresent**": ein Bytefeld, das angibt, ob das Einschränkungs Feld vorhanden ist. Wenn ein Wert ungleich 0 (null) festgelegt ist, muss das Einschränkungs Feld vorhanden sein. Wenn der Wert auf 0x00 festgelegt ist, muss die Einschränkung nicht vorhanden sein.

**Einschränkung**: eine Struktur mit dem Befehl, die die Befehlsstruktur der Abfrage enthält.

**Csortsetpresent**: ein Bytefeld, das angibt, ob das sortset-Feld vorhanden ist. Wenn ein Wert ungleich 0 (null) festgelegt ist, muss das sortset-Feld vorhanden sein. Wenn der Wert auf 0x00 festgelegt ist, muss sortset nicht vorhanden sein.

**Sortset**: eine csortset-Struktur, die die Sortierreihenfolge der Abfrage angibt.

**Ccategorizationsetpresent**: ein Bytefeld, das angibt, ob das Feld "ccategorizationset" vorhanden ist. Wenn ein Wert ungleich 0 (null) festgelegt ist, muss das Feld "ccategorizationset" vorhanden sein. Wenn der Wert auf 0x00 festgelegt ist, muss ccategorizationset nicht vorhanden sein.

**Ccategorizationset**: eine ccategorizationset-Struktur, die die Gruppen für die Abfrage enthält.

**Rowsetproperties**: eine crowsetproperties-Struktur, die Konfigurationsinformationen für die Abfrage bereitstellt.

**Pidmapper**: eine cpidmapper-Struktur, die Eigenschaften enthält, die in einem Rowset zurückgegeben werden sollen.

### <a name="2239-cpmcreatequeryout"></a>2.2.3.9 cpmkreatequeryout

Die cpmkreatequeryout-Nachricht enthält eine Antwort auf eine cpmkreatequeryin-Nachricht.

Das Format der cpmkreatequeryout-Nachricht, die auf den Header folgt, lautet:



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

\_"struesequential"

\_' f ' eindeutig

acursoren



 

**\_ ftruesequential**: ein informativer boolescher Wert, der angibt, ob die Abfrage die Ergebnisse schneller bereitstellen kann. Wenn es für die in cpmkreatequeryin angegebene Abfrage auf 0x00000001 festgelegt ist, kann der Server den Index so verwenden, dass Abfrageergebnisse wahrscheinlich schneller zugestellt werden. Bei der Festlegung auf 0x00000000 wäre eine größere Latenz beim Bereitstellen von Abfrage Ergebnissen vorhanden. Darf nicht auf einen anderen Wert festgelegt werden.

" **\_ f workidunique**": ein boolescher Wert, der angibt, ob die von den Cursorn referenzierten Dokument Bezeichner in den Abfrage Ergebnissen eindeutig sind. Wenn der Wert auf 0x00000001 festgelegt ist, sind die Bezeichner eindeutig. Wenn Sie auf 0x00000000 festgelegt ist, sind Sie nur innerhalb des Rowsets eindeutig.

**acursoren**: ein Array aus 32-Bit-Ganzzahlen ohne Vorzeichen, das die Handles für Cursor darstellt, wobei die Anzahl der Elemente gleich der Anzahl der Kategorien im Feld "kategorizationset" der cpmkreatequeryin-Nachricht ist.

### <a name="22310-cpmgetquerystatusin"></a>2.2.3.10 cpmgetquerystatus in

Die cpmgetquerystatusin-Meldung fordert den Status einer Abfrage an. Das Format der cpmgetquerystatusin-Nachricht, die auf den Header folgt, lautet:



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

\_hcursor



 

**\_ hcursor**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Handle aus der cpmkreatequeryout-Meldung darstellt, die die Abfrage identifiziert, für die Statusinformationen abgerufen werden sollen.

### <a name="22311-cpmgetquerystatusout"></a>2.2.3.11 cpmgetquerystatus-out

Die cpmgetquerystatusout-Meldung antwortet auf eine cpmgetquerystatusin-Nachricht mit dem Status der Abfrage. Das Format der cpmgetquerystatusout-Nachricht, die auf den Header folgt, lautet:



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

\_Stands



 

**\_ Status**: eine Bitmaske mit Werten, die in den unten stehenden Tabellen definiert sind, die die Abfrage beschreibt.

In der folgenden Tabelle sind die stat-Werte aufgelistet, die \_ \* durch Ausführen einer bitweisen and-Operation \_ mit 0x00000007 abgerufen werden. Das Ergebnis muss einer der folgenden sein:



| Konstante                 | Bedeutung                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| Stat \_ ausgelastet 0x00000000    | Die asynchrone Abfrage wird noch ausgeführt.                                          |
| Stat- \_ Fehler 0x00000001   | Die Abfrage weist einen Fehlerstatus auf.                                                   |
| Stat \_ done 0x00000002    | Die Abfrage ist fertiggestellt.                                                            |
| Stat- \_ Aktualisierung 0x00000003 | Die Abfrage ist fertiggestellt, aber Updates ergeben eine zusätzliche Abfrage Berechnung. |



 

In der folgenden Tabelle werden zusätzliche stat- \_ \* Bits aufgelistet, die unabhängig voneinander festgelegt werden können.



| Konstante                                    | Bedeutung                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Stat-Füll \_ \_ Wörter 0x00000010               | Füll Wörter wurden in der Inhalts Abfrage durch Platzhalter Zeichen ersetzt.                                                              |
| Stat- \_ Inhalt ist \_ \_ \_ veraltet 0x00000020     | Die Ergebnisse der Abfrage sind möglicherweise falsch, da die Abfrage geänderte, aber nicht indizierte Dateien umfasste.                             |
| Die stat- \_ Aktualisierung ist \_ unvollständig 0x00000040        | Die Ergebnisse der Abfrage sind möglicherweise falsch, da die Abfrage geänderte und neu indizierte Dateien umfasste, deren Inhalt nicht enthalten war. |
| Stat- \_ Inhalts \_ Abfrage \_ unvollständig 0x00000080 | Die Inhalts Abfrage war zu komplex und konnte nicht verwendet werden, anstatt den Inhalts Index zu verwenden.                          |
| Stat- \_ Zeit \_ Limit \_ überschritten 0x00000100      | Die Ergebnisse der Abfrage sind möglicherweise falsch, da die Abfrage Ausführungszeit die maximal zulässige Zeit erreicht hat.                    |



 

### <a name="22312-cpmgetquerystatusexin"></a>2.2.3.12 cpmgetquerystatusexin

Die cpmgetquerystatusexin-Nachricht fordert den Status einer Abfrage und zusätzliche Informationen, wie z. b. die Anzahl der indizierten Dokumente, die Anzahl der zu indizierenden Dokumente usw., an. Das Format der cpmgetquerystatusexin-Nachricht, die auf den Header folgt, lautet:



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

\_hcursor

\_BMK



 

**\_ hcursor**: ein 32-Bit-Wert, der das Handle aus der cpmkreatequeryout-Meldung darstellt, die die Abfrage identifiziert, für die Statusinformationen abgerufen werden sollen.

**\_ BMK**: ein 32-Bit-Wert, der das Handle eines Lesezeichens angibt, dessen Position abgerufen werden soll.

### <a name="22313-cpmgetquerystatusexout"></a>2.2.3.13 cpmgetquerystatusexout

Die cpmgetquerystatusexout-Nachricht antwortet mit dem Status der Abfrage und anderen Statusinformationen, wie in der Abbildung unten beschrieben, auf eine cpmgetquerystatusexin-Nachricht. Das Format der cpmgetquerystatusexout-Nachricht, die auf den Header folgt, lautet:



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

\_Stands

\_cfiltereddocuments

\_cdocumentstofilter

\_dwratiofinishednenner

\_dwratiofinishednumerator

\_irowbmk

\_crowstotal



 

**\_ Status**: einer der Stat \_ \* Werte, die im Abschnitt 2.2.3.11 angegeben sind.

**\_ cfiltereddocuments**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der indizierten Dokumente angibt

**\_ cdocumentstofilter**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dokumente angibt, die noch indiziert werden sollen.

**\_ dwratiofinishednenner**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Nenner des Verhältnisses der Dokumente angibt, die von der Abfrage verarbeitet wurden.

**\_ dwratiofinishednumerator**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Zähler für das Verhältnis der Dokumente angibt, die von der Abfrage verarbeitet wurden.

**\_ irowbmk**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die ungefähre Position des Lesezeichens im Rowset in Bezug auf Zeilen angibt.

**\_ crowstotal**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Zeilen im Rowset angibt.

### <a name="22314-cpmsetbindingsin"></a>2.2.3.14 cpmsetbindingsin

Die cpmsetbindingsin-Nachricht fordert die Bindung von Spalten an ein Rowset an. Der Server antwortet auf die cpmsetbindingsin-Anforderungs Nachricht, indem er den Header Abschnitt der cpmbindingsin-Nachricht mit den Ergebnissen der im Feld "Status" enthaltenen Anforderung enthält \_ . Das Format der cpmsetbindingsin-Nachricht, die auf den Header folgt, lautet:



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

\_hcursor (optional)

\_cbrow (optional)

\_cbbindingdesc (optional)

\_Dummy (optional)

CColumns (optional)

acolumschlag (Variable, optional)



 

**\_ hcursor**: ein 32-Bit-Wert, der das Handle aus der cpmkreatequeryout-Meldung darstellt, das die Zeile identifiziert, für die Bindungen festgelegt werden sollen. Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.

**\_ cbrow**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe einer Zeile in Bytes angibt. Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.

**\_ cbbindingdesc**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge der Felder nach dem Dummy-Feld in Bytes angibt \_ . Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.

**\_ Dummy**: Dieses Feld wird nicht verwendet und muss ignoriert werden. Sie kann auf einen beliebigen Wert festgelegt werden. Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.

**CColumns**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im acolenumns-Array angibt. Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.

**acolenns**: ein Array der ctablecolumn-Strukturen, das die Spalten einer Zeile im Rowset beschreibt. Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird. Strukturen im Array müssen durch 0 bis 3 Auffüll Zeichen voneinander getrennt werden, sodass jede Struktur über eine 4-Byte-Ausrichtung ab dem Anfang einer Nachricht verfügt. Bei solchen Füll Zeichen kann es sich um beliebige Werte handeln, die bei der Bestätigung ignoriert werden müssen.

### <a name="22315-cpmgetrowsin"></a>2.2.3.15 cpmgetrowsin

Die cpmgetrowsin-Nachricht fordert Zeilen aus einer Abfrage an. Das Format der cpmgetrowsin-Nachricht, die auf den Header folgt, lautet:



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

\_hcursor

\_crowstotransfer

\_cbrowwidth

\_cbseek

\_cbreserved

\_cbread-Puffer

\_ulclientbase

\_fbwdfetch

ETYPE

\_"chapt"

Seekdescription

...

... veränder



 

**\_ hcursor**: ein 32-Bit-Wert, der das Handle aus der cpmkreatequeryout-Meldung darstellt, die die Abfrage identifiziert, für die Zeilen abgerufen werden sollen.

**\_ crowstotransfer**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die maximale Anzahl von Zeilen angibt, die der Client als Antwort auf diese Nachricht empfangen möchte.

**\_ cbrowwidth**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge einer Zeile in Bytes angibt.

**\_ cbseek**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der Nachricht angibt, beginnend mit ETYPE.

**\_ cbreserved**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe einer cpmgetrowsout-Nachricht (in Bytes) angibt (ohne die Felder Zeilen und seekbeschreibungen). Dieser Wert wird in diesem Feld dem Wert des \_ cbseek-Felds hinzugefügt und anschließend verwendet, um das Feld Offset of rows in der cpmgetrowsout-Nachricht zu berechnen.

**\_ cbreadbuffer**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die auf den maximalen Wert von \_ cbrowwidth oder 1000 Mal auf das \_ nächste 512 Byte gerundet festgelegt werden muss. Der Wert darf 0x00004000 nicht überschreiten.

**\_ ulclientbase**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Basiswert angibt, der für Zeiger Berechnungen im Zeilen Puffer verwendet werden soll. Wenn 64-Bit-Offsets verwendet werden, wird das "reserved2"-Feld des Nachrichten Headers als obere 32-Bits und \_ ulclientbase als untere 32 Bits eines 64-Bit-Werts verwendet. Weitere Informationen finden Sie im Abschnitt 2.2.3.16.

**\_ fbwdfetch**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Reihenfolge angibt, in der die Zeilen abgerufen werden sollen. Wenn der Wert auf 0x00000001 festgelegt ist, werden die Zeilen in umgekehrter Reihenfolge abgerufen. Wenn der Wert auf 0x00000000 festgelegt ist, müssen die Zeilen in der Reihenfolge der Nachrichten abgerufen werden. Darf nicht auf andere Werte festgelegt werden.

**ETYPE**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die einen der folgenden Werte enthält, um den Typ des auszuführenden Vorgangs anzugeben.



| Wert                         | Bedeutung                                                  |
|-------------------------------|----------------------------------------------------------|
| erowseeknext 0x00000001       | Seekdescription enthält eine crowseeknext-Struktur.       |
| erowseekat 0x00000002         | Seekdescription enthält eine crowseekat-Struktur.         |
| erowseekatratio 0x00000003    | Seekdescription enthält eine crowseekatratio-Struktur.    |
| erowseekbybookmark 0x00000004 | Seekdescription enthält eine crowseekbybookmark-Struktur. |



 

**\_ chapt**: ein 32-Bit-Wert, der das Handle des Rowset-Kapitels darstellt.

**Seekdescription**: Dieses Feld muss eine Struktur des Typs enthalten, der durch den ETYPE-Wert angegeben wird.

### <a name="22316-cpmgetrowsout"></a>2.2.3.16 cpmgetrowsout

Die cpmgetrowsout-Meldung antwortet mit den Zeilen einer Abfrage auf eine cpmgetrowsin-Nachricht. -Server müssen Offsets in Datentypen variabler Länge im Feld Zeilen wie folgt formatieren:

-   Der Client hat angegeben, dass es sich um ein 32-Bit-System (0x00000008 oder weniger im iclientversion-Feld von cpmconnectin) handelt: Offsets sind 32-Bit-Ganzzahlen.
-   Der Client hat angegeben, dass es sich um ein 64-Bit-System ( \_ iclientversion > 0x00000008 in cpmconnectin) handelt, und der Server hat angegeben, dass es sich um ein 32-Bit-System \_ handelt (Serverversion ist in cpmconnectout auf 0x00000007 festgelegt): Offsets sind 32-Bit
-   Der Client hat angegeben, dass es sich um ein 64-Bit-System ( \_ iclientversion > 0x00000008 in cpmconnectin) handelt, und der Server hat angegeben, dass es sich um ein 64-Bit-System \_ handelt (Serverversion ist in cpmconnectout auf 0x00010007 festgelegt): Offsets sind 64-Bit

Das Format der cpmgetrowsout-Nachricht, die auf den Header folgt, lautet:



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

\_crowszurück gegeben

ETYPE

\_"chapt"

Seekdescription (optional, Variable)

...

...

paddinwächst (optional, Variable)

Zeilen



 

**\_ crowszurück gegeben**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der in Zeilen zurückgegebenen Zeilen angibt.

**ETYPE**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die einen der folgenden Werte enthält, um den Typ des auszuführenden rowseek-Vorgangs anzugeben.



| Wert                         | Bedeutung                                                  |
|-------------------------------|----------------------------------------------------------|
| erowsseeknone 0x00000000      | Keine seekdescription, seekdescription-Feld ignorieren.        |
| erowseeknext 0x00000001       | Seekdescription enthält eine crowseeknext-Struktur.       |
| erowseekat 0x00000002         | Seekdescription enthält eine crowseekat-Struktur.         |
| erowseekatratio 0x00000003    | Seekdescription enthält eine crowseekatratio-Struktur.    |
| erowseekbybookmark 0x00000004 | Seekdescription enthält eine crowseekbybookmark-Struktur. |



 

**\_ chapt**: ein 32-Bit-Wert, der das Handle des Rowset-Kapitels darstellt.

**Seekdescription**: Dieses Feld muss eine Struktur des Typs enthalten, der durch das ETYPE-Feld angegeben wird.

**paddingens**: Dieses Feld muss eine ausreichende Länge aufweisen (0 bis \_ cbreserved-1 Byte), um das Feld Zeilen \_ vom Anfang einer Nachricht in den cbreserved-Offset aufzurufen, wobei \_ cbreserved der Wert in der cpmgetrowsin-Nachricht ist. Bei den in diesem Feld verwendeten Füll Zeichen kann es sich um beliebige Werte handeln. Dieses Feld muss vom Empfänger ignoriert werden.

**Rows**: Zeilendaten werden gemäß den Spalten Informationen in der aktuellen cpmsetbindingsin-Nachricht entsprechend formatiert. Zeilen müssen in der Reihenfolge gespeichert werden (z. b. Zeile 1 vor Zeile 2).

Spalten mit fester Größe müssen in den Offsets gespeichert werden, die von der aktuellen cpmsetbindingsin-Nachricht angegeben werden.

Spalten mit variabler Größen (z. b. Zeichen folgen) müssen wie folgt gespeichert werden:

-   Die Variablen Daten selbst (z. b. die Zeichenfolge) werden in absteigender Reihenfolge am Ende des Puffers gespeichert (z. b. ist die Auflistung aller Variablen Daten für Zeile 1 am Ende, Zeile 2 am nächsten am nächsten usw.).
-   Der Bereich mit fester Größe (am Anfang des Zeilen Puffers) muss für jede Spalte eine crowvariant enthalten, die bei dem in der aktuellen cpmsetbindingsin-Nachricht angegebenen Offset gespeichert wird. VType muss den Datentyp (z.: VT \_ LPWSTR) enthalten. Wenn, wie durch die Regeln am Anfang des Abschnitts in diesem Abschnitt festgelegt, 32-Bit-Offsets verwendet werden, muss das Offset-Feld in crowvariant einen 32-Bit-Wert enthalten, der den Offset der Variablen Daten vom Anfang der cpmgetrowsout-Nachricht sowie den Wert von \_ ulclientbase angibt, der in der aktuellen cpmgetrowsin-Nachricht angegeben Wenn 64-Bit-Offsets verwendet werden, muss das Offset Feld in crowvariant einen 64-Bit-Wert enthalten, bei dem es sich um den Offset vom Anfang der cpmgetrowsout-Nachricht handelt, der einem 64-Bit-Wert hinzugefügt wird, der mithilfe von \_ ulclientbase als niedriger 32 Bits und \_ ulReserved2 als hohe 32 Bits erstellt wurde.

Wenn die cpmsetbindingsin-Nachricht z. b. die beiden Spalten Size (VT \_ I4) und Title (VT \_ LPWSTR) und \_ ulclientbase aus cpmgetrowsin den Wert 0x10000 angegeben haben, würden zwei Zeilen wie folgt angezeigt werden. Der in grau markierte Abschnitt ist der Teil des Puffers mit fester Länge.

![cpmsetbindingsin-Nachrichten Beispiel](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a>2.2.3.17 cpmratiofinishedin

Die cpmratiofinishedin-Nachricht fordert den Abschluss Prozentsatz einer Abfrage an. Das Format der cpmratiofinishedin-Nachricht, die auf den Header folgt, lautet:



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

\_hcursor

\_schnell



 

**\_ hcursor**: das Handle aus der cpmkreatequeryout-Nachricht, das die Abfrage identifiziert, für die Vervollständigungs Informationen angefordert werden sollen.

**\_ fquick**: muss auf 0x00000001 festgelegt werden. Nicht verwendet und muss vom Server ignoriert werden.

### <a name="22318-cpmratiofinishedout"></a>2.2.3.18 cpmratiofinishedout

Die cpmratiofinishedout-Meldung antwortet mit dem Abschluss Verhältnis einer Abfrage auf eine cpmratiofinishedin-Nachricht. Das Format der cpmratiofinishedout-Nachricht, die auf den Header folgt, lautet:



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

\_ ulnumerator

\_ulnenner

\_Crows

\_Zeilen-Zeilen



 

**\_ ulnumerator**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Zähler des Vervollständigungs Verhältnisses in Bezug auf Zeilen angibt.

**\_ ulnenner**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Nenner des Vervollständigungs Verhältnisses in Bezug auf Zeilen angibt. Muss größer als 0 (null) sein.

**\_ Crows**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Zeilen für die Abfrage angibt.

" **\_ f newrows**": ein boolescher Wert, der angibt, ob neue Zeilen verfügbar sind. Der Wert 0x00000001 gibt an, dass neue Zeilen im Rowset verfügbar sind. Der Wert 0x00000000 gibt an, dass das Rowset keine neuen Zeilen enthält. Dieses Feld darf nicht auf einen anderen Wert festgelegt werden.

### <a name="22319-cpmfetchvaluein"></a>2.2.3.19 cpmfetchvaluein

Die cpmfetchvaluein-Meldung fordert einen Eigenschafts Wert an, der zu groß war, um in einem Rowset zurückgegeben zu werden. Wie im Abschnitt 3.2.4.2.5 angegeben, wird diese Meldung wiederholt gesendet, um alle Bytes der Eigenschaft abzurufen und \_ cbsofar für jeden zu aktualisieren, bis das \_ Feld fmoreist der cpmfetchvalueout-Nachricht **auf false** festgelegt ist.

Das Format der cpmfetchvaluein-Nachricht, die auf den Header folgt, lautet:



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

\_WID

\_cbsofar

\_cbpropspec

\_cbblock

PROPSPEC (Variable)

...

\_Auffüll Zeichen (Variable)



 

**\_ wid**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Dokument-ID darstellt, die das Dokument identifiziert, für das eine Eigenschaft abgerufen werden soll.

**\_ cbsofar**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der zuvor für diese Eigenschaft übertragenen Bytes enthält. Muss in der ersten Nachricht auf 0x00000000 festgelegt werden.

**\_ cbpropspec**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des PROPSPEC-Felds in Bytes enthält.

**\_ cbchunk**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die maximale Anzahl von Bytes enthält, die der Absender in einer cpmfetchvalueout-Nachricht annehmen kann.

*Windows-Verhalten: Dieses Feld ist für alle Versionen von Windows auf 0x00004000 festgelegt.*

**PROPSPEC**: eine cfullpropspec-Struktur, die die abzurufende Eigenschaft angibt.

**\_ Auffüllung**: Dieses Feld muss die erforderliche Länge (0 bis 3 Bytes) aufweisen, um die Nachricht auf ein Vielfaches von 4 Bytes in der Länge zu füllen. Der Wert der Auffüll Bytes kann beliebiger Wert sein. Dieses Feld muss vom Empfänger ignoriert werden.

### <a name="22320-cpmfetchvalueout"></a>2.2.3.20 cpmfetchvalueout

Die cpmfetchvalueout-Nachricht antwortet auf eine cpmfetchvaluein-Nachricht mit einem Eigenschafts Wert aus einer vorherigen Abfrage. Wie im Abschnitt 3.1.5.2.8 angegeben, wird diese Nachricht nach jeder cpmfetchvaluein-Nachricht gesendet, bis alle Bytes der Eigenschaft übertragen werden.

Das Format der cpmfetchvalueout-Nachricht, die auf den Header folgt, lautet:



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

\_"gmore" vorhanden

\_"f" ist vorhanden.

VType

vValue (Variable)



 

**\_ cbValue**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtgröße in Bytes in vValue enthält.

" **\_ fimore"**: ein boolescher Wert, der angibt, ob weitere cpmfetchvalueout-Nachrichten verfügbar sind. Wenn der Wert auf 0x00000001 festgelegt ist, sind weitere cpmfetchvalueout-Meldungen vorhanden. Wenn Sie auf 0x00000000 festgelegt ist, sind keine weiteren cpmfetchvalueout-Meldungen verfügbar.

Boolescher **\_ Wert: ein** boolescher Wert, der angibt, ob ein Wert für die-Eigenschaft vorhanden ist. Wenn der Wert auf 0x00000001 festgelegt ist, ist ein Wert für die-Eigenschaft vorhanden. Wenn der Wert auf 0x00000000 festgelegt ist, ist kein Wert für die Eigenschaft vorhanden.

**VType**: ein Wert aus der VARENUM-Enumeration finden Sie im Abschnitt 2.2.1.1, in dem der Typ der Eigenschaft beschrieben wird.

**vValue**: ein Teil eines Bytearrays, das eine serializedpropertyvalue-Struktur enthält, wie im Abschnitt 2.2.1.32 angegeben, wobei der Offset des Anfangs des Teils der Wert von \_ cbsofar in cpmfetchvaluein ist. Die Länge des Teils, der durch das \_ cbValue-Feld angegeben wird, muss mit dem Wert von \_ cbblock in cpmfetchvaluein übereinstimmen, wenn \_ fmorevorhanden auf 0x00000001 festgelegt ist, und muss kleiner oder gleich dem Wert von \_ cbblock sein, andernfalls.

### <a name="22321-cpmgetnotify"></a>2.2.3.21 cpmgetnotify

Die cpmgetnotify-Nachricht fordert an, dass der Client über Rowsetänderungen benachrichtigt werden möchte.

Die Nachricht darf keinen Text enthalten. nur der Nachrichten Header, wie in Abschnitt 2.2.2 angegeben, muss gesendet werden.

### <a name="22322-cpmsendnotifyout"></a>2.2.3.22 cpmsendnotimayout

Die cpmsendnotifyout-Nachricht benachrichtigt den Client über eine Änderung der Ergebnisse einer Abfrage.

Diese Meldung wird nur gesendet, wenn eine Änderung auftritt. Das Format der cpmsendnotimayout-Nachricht, die auf den Header folgt, lautet:



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

\_watchnotify



 

**\_ watchnotify**: die Änderung an der Abfrage. Es muss sich um einen der folgenden Werte handeln:



| Wert                                     | Bedeutung                                             |
|-------------------------------------------|-----------------------------------------------------|
| Dbwatchnotify \_ rowschangi0x00000001     | Die Anzahl der Zeilen im abfragerowset hat sich geändert. |
| Dbwatchnotify \_ querydone 0x00000002       | Die Abfrage wurde abgeschlossen.                            |
| Dbwatchnotify \_ queryreausgeführte 0x00000003 | Die Abfrage wurde erneut ausgeführt.                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a>2.2.3.23 cpmgetapproximatepositionin

Die cpmgetapproximatepositionin-Meldung fordert die ungefähre Position eines Lesezeichens in einem Kapitel an. Das Format der cpmgetapproximatepositionin-Nachricht, die auf den Header folgt, lautet:



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

\_hcursor

\_"chapt"

\_BMK



 

**\_ hcursor**: ein 32-Bit-Wert, der den aus cpmkreatequeryout abgelegten Abfrage Cursor für das Rowset mit dem Lesezeichen darstellt.

**\_ chapt**: ein 32-Bit-Wert, der das Handle für das Kapitel darstellt, das das Lesezeichen enthält.

**\_ BMK**: ein 32-Bit-Wert, der das Handle für das Lesezeichen darstellt, für das die ungefähre Position abgerufen werden soll.

### <a name="22324-cpmgetapproximatepositionout"></a>2.2.3.24 cpmgetapproximatepositionout

Die cpmgetapproximatepositionout-Nachricht antwortet auf eine cpmgetapproximatepositionin-Meldung, die die ungefähre Position des Lesezeichens im Kapitel beschreibt. Das Format der cpmgetapproximatepositionout-Nachricht, die auf den Header folgt, lautet:



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



 

**\_ Zähler**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Zeilennummer des Lesezeichens im Rowset enthält. Wenn keine Zeilen vorhanden sind, muss dieses Feld auf 0x00000000 festgelegt werden.

**\_ Nenner**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeilen im Rowset enthält.

### <a name="22325-cpmcomparebmkin"></a>2.2.3.25 cpmcomparebmkin

Die cpmcomparebmkin-Nachricht fordert einen Vergleich zweier Lesezeichen in einem Kapitel an.

Das Format der cpmcomparebmkin-Nachricht, die auf den Header folgt, lautet:



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

\_hcursor

\_"chapt"

\_bmkfirst

\_bmksecond



 

\_**hcursor**: ein 32-Bit-Wert, der das Handle aus der cpmkreatequeryout-Nachricht für das Rowset darstellt, das die Lesezeichen enthält.

\_**chapt**: ein 32-Bit-Wert, der das Handle des Kapitels darstellt, das die zu vergleichenden Lesezeichen enthält.

\_**bmkfirst**: ein 32-Bit-Wert, der das Handle für das erste zu vergleichende Lesezeichen darstellt.

\_**bmksecond**: ein 32-Bit-Wert, der das Handle für das zweite zu vergleichende Lesezeichen darstellt.

### <a name="22326-cpmcomparebmkout"></a>2.2.3.26 cpmcomparebmkout

Die cpmcomparebmkout-Nachricht antwortet auf eine cpmcomparebmkin-Nachricht mit dem Vergleich der beiden Lesezeichen im Kapitel. Das Format der cpmcomparebmkout-Nachricht, die auf den Header folgt, lautet:



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

\_dwcomparison



 

\_**dwcomparison**: einer der folgenden Werte, der die relativen Positionen der beiden Lesezeichen im Kapitel angibt.



| Wert                               | Bedeutung                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| DbCompare \_ lt 0x00000000            | Das erste Lesezeichen wird vor dem zweiten positioniert.               |
| DbCompare \_ EQ 0x00000001            | Das erste Lesezeichen hat dieselbe Position wie die zweite.           |
| DbCompare \_ gt 0x00000002            | Das erste Lesezeichen ist nach dem zweiten positioniert.                |
| DbCompare \_ ne 0x00000003            | Das erste Lesezeichen hat nicht die gleiche Position wie die zweite. |
| DbCompare, nicht \_ vergleichbar mit 0x00000004 | Das erste Lesezeichen ist nicht mit dem zweiten Lesezeichen vergleichbar.               |



 

### <a name="22327-cpmrestartpositionin"></a>2.2.3.27 cpmrestartpositionin

Die cpmrestartpositionin-Meldung verschiebt die Abruf Position für einen Cursor an den Anfang des Kapitels. Wie im Abschnitt 3.1.5.2.12 angegeben, antwortet der Server mit derselben Nachricht, wobei die Ergebnisse der Anforderung im \_ Status-Feld des CISP-Headers enthalten sind.

Das Format der cpmrestartpositionin-Nachricht, die auf den Header folgt, lautet:



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

\_hcursor (optional)

\_chapt (optional)



 

**\_ hcursor**: ein 32-Bit-Wert, der das Handle darstellt, das aus einer cpmkreatequeryout-Nachricht abgerufen wird, die die Abfrage identifiziert, für die die Position neu gestartet werden soll. Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.

**\_ chapt**: ein 32-Bit-Wert, der das Handle eines Kapitels darstellt, aus dem Zeilen abgerufen werden sollen. Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.

### <a name="22328-cpmfreecursorin"></a>2.2.3.28 cpmfreecursorin

Die cpmfreecursorin-Meldung fordert die Freigabe eines Cursors an. Das Format der cpmfreecursorin-Nachricht, die auf den Header folgt, lautet:



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

\_hcursor



 

**\_ hcursor**: ein 32-Bit-Wert, der das Handle des Cursors von der cpmkreatequeryout-Nachricht darstellt, die freigegeben werden soll.

### <a name="22329-cpmfreecursorout"></a>2.2.3.29 cpmfreecursorout

Die cpmfreecursorout-Nachricht antwortet auf eine cpmfreecursorin-Nachricht mit den Ergebnissen der Freigabe eines Cursors. Das Format der cpmfreecursorout-Nachricht, die auf den Header folgt, lautet:



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

\_ccurrsorsrestdauer



 

**\_ ccursorsrestwert**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von Cursorn angibt, die noch für die Abfrage verwendet werden.

### <a name="22330-cpmdisconnect"></a>2.2.3.30 cpmdisconnect

Die cpmdisconnect-Nachricht beendet die Verbindung mit dem Server.

Die Nachricht darf keinen Text enthalten. nur der Nachrichten Header, wie in Abschnitt 2.2.2 angegeben, muss gesendet werden.

### <a name="224-errors"></a>2.2.4-Fehler

Alle Content Index Service-Protokollnachrichten müssen bei Erfolg 0x00000000 zurückgeben. Andernfalls geben Sie einen 32-Bit-Fehlercode ungleich 0 (null) zurück, der entweder ein HRESULT-oder ein NTSTATUS-Wert sein kann (siehe Abschnitt 1,8). Wenn ein Puffer zu klein ist, um ein Ergebnis zu erhalten, muss ein Status \_ Code \_ mit unzureichenden Ressourcen (0xc0000009a) zurückgegeben werden, und der fehlgeschlagene Vorgang sollte mit einem größeren Puffer wiederholt werden.

Alle anderen Fehler Werte müssen identisch behandelt werden.

(Beachten Sie, dass sich die Nummerierungen von HRESULT und NTSTATUS derzeit nicht überlappen, außer mit Werten gleicher Bedeutung, aber auch wenn Sie in Zukunft Konflikte verursachen würden, würden Sie keine Protokoll Probleme verursachen, solange der Wert für "Status \_ " Unzureichende \_ Ressourcen bleiben eindeutig, da alle anderen Fehler Werte identisch behandelt werden.)

## <a name="3-protocol-details"></a>3 Protokolldetails

-   [3,1 Server Details](#31-server-details)
-   [3,2 Client Details](#32-client-details)

CISP-Nachrichten Anforderungen für die Remote Abfrage von Indizierungs Dienst Katalogen erfordern keine bestimmte Sequenz. Es wird empfohlen, dass die höhere Ebene eine sinnvolle Nachrichten Sequenz befolgt, wie bei Nachrichten, die von dieser Sequenz oder mit ungültigen Daten empfangen werden, antwortet der Server jedoch mit einem Fehler. Einige Nachrichten sind auch von der höheren Ebene abhängig, die gültige Daten bereitstellt, die zuvor in der Sequenz in Nachrichten empfangen wurden.

Eine typische Nachrichten Sequenz für eine einfache Abfrage von einem Client an einen Remote Computer ist im folgenden Diagramm dargestellt.

![Nachrichten Sequenz für einfache Abfrage](images/protocoldetails.jpg)

Die Nachrichten, die im vorangehenden Diagramm dargestellt werden, stellen eine Teilmenge aller CISP-Nachrichten dar, die zum Abfragen eines remoteindizierungs-Dienst Katalogs verwendet werden.

### <a name="31-server-details"></a>3,1 Server Details

### <a name="311-abstract-data-model"></a>3.1.1 Abstraktes Datenmodell

Im folgenden Abschnitt werden Daten und Status angegeben, die vom CISP-Server verwaltet werden. Die hier bereitgestellten Daten dienen dazu, die Erläuterung der Verhalten des Protokolls zu vereinfachen. In diesem Abschnitt wird nicht vorgeschrieben, dass Implementierungen dieses Modells einhalten, solange das externe Verhalten mit dem in diesem Dokument beschriebenen übereinstimmt.

Ein Index Dienst, der den CISP implementiert, muss die folgenden abstrakten Datenelemente verwalten:

-   Die Liste der Clients, die mit dem Server verbunden sind.
-   Informationen zu den einzelnen Clients, einschließlich:
-   -   Client Version (wie in der im Abschnitt 2.2.3.6 angegebenen Meldung "cpmconnectin" angegeben)
    -   Katalog, der dem Client zugeordnet ist (durch eine cpmconnectin-Nachricht)
    -   Zusätzliche Client Eigenschaften, wie im Abschnitt 2.2.1.21.1 angegeben.
    -   Suchabfrage des Clients
    -   Liste der Cursor Handles für die Abfrage und Position im Resultset für jedes handle.
    -   Aktueller Satz von Bindungen
    -   Aktueller Status der Abfrage, die (für jeden Cursor) umfasst:
    -   -   Anzahl von Zeilen im Abfrageergebnis
        -   Zähler und Nenner des abfrageabschlusses
        -   Die letzte Anzahl von Zeilen, die von der aktuellen cpmratiofinishedout-Meldung für diesen Cursor gemeldet wurden.
        -   Ob die Abfrage vom Server auf Änderungen in den Abfrage Ergebnissen überwacht wird und ob Sie überwacht wird, was sich in den Abfrage Ergebnissen geändert hat, seit Sie zuletzt von cpmsendnotifyout an den Client gemeldet wurde
        -   Liste der Kapitel Handles, die von dieser Abfrage an einen Client bereitgestellt werden.
        -   Liste der Lesezeichen Handles für jeden Cursor, die von dieser Abfrage an einen Client bereitgestellt werden.

-   Der aktuelle Zustand des Indizierungs Dienstanbieter, der möglicherweise "nicht initialisiert", "wird ausgeführt" oder "heruntergefahren" ist. Beachten Sie, dass sich der Server in den meisten Fällen im Zustand "wird ausgeführt" befindet. Im folgenden finden Sie das zustandsautomatdiagramm für den Server:

    ![Zustands Automaten Diagramm des Index Dienst Servers](images/abstractdatamodel.jpg)

-   Katalog spezifische Informationen: Anzahl der indizierten Dokumente, Indexgröße, Anzahl eindeutiger Schlüssel usw. (siehe Abschnitt 2.2.3.1 for Complete List), State (entspricht den Werten von dwnewstate im Abschnitt 2.2.3.2).
-   Für jede unterstützte Sprache eine Datenbank von Wort Variationen, wie im Abschnitt 2.2.1.3 erläutert.

### <a name="312-timers"></a>3.1.2 Zeitgeber

Es sind keine protokolltimer erforderlich.

### <a name="313-initialization"></a>3.1.3 Initialisierung

Der Server muss bei der Initialisierung seinen Status auf "nicht initialisiert" festlegen und mit dem lauschen auf Nachrichten auf dem Named Pipe beginnen, der in Abschnitt 1,9 angegeben ist. Nachdem eine andere interne Initialisierung durchgeführt wurde, muss Sie in den Status "wird ausgeführt" übergehen.

### <a name="314-higher-layer-triggered-events"></a>3.1.4 Ausgelöste Ereignisse auf höherer Ebene

Keine.

### <a name="315-message-processing-and-sequencing-rules"></a>3.1.5 Nachrichtenverarbeitungs-und Sequenz Regeln

Wenn bei der Verarbeitung einer von einem Client gesendeten Nachricht ein Fehler auftritt, muss der Server wie folgt einen Fehler an den Client zurückmelden:

-   Verarbeitung der vom Client gesendeten Nachricht Abbrechen
-   Antworten Sie mit dem Nachrichten Header (nur) der vom Client gesendeten Nachricht, wobei das Nachrichten \_ Feld intakt bleibt.
-   Legen \_ Sie das Feld Status auf den Fehler Codewert fest.

Wenn eine Nachricht eingeht, muss der Server den Wert des msg-Felds überprüfen, \_ um festzustellen, ob es sich um einen bekannten Typ handelt (siehe Abschnitt 2.2.2). Wenn der Typ nicht bekannt ist, muss er einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.

Der Server muss dann den \_ Wert des ulchecksum-Felds überprüfen, wenn der Nachrichtentyp einer der folgenden ist:

-   Cpmconnectin (0x000000c8)
-   Cpmkreatequeryin (0x000000CA)
-   Cpmsetbindingsin (0x000000d0)
-   Cpmgetrowsin (0x000000cc)
-   Cpmfetchvaluein (0x000000e4)

Um den \_ Wert des Felds ulchecksum zu validieren, muss der Server den Wert, den der Client im \_ Feld iclientversion in der cpmconnectin-Nachricht angegeben hat, überprüfen.

Wenn das \_ Feld iclientversion nicht auf 0x00000008 festgelegt ist und das \_ Feld ulchecksum nicht auf 0x00000000 festgelegt ist, muss der Server einen \_ Fehler aufgrund eines ungültigen \_ Parameters (0xc000000D) melden. Der Server muss das \_ Feld ulchecksum für Clients nicht validieren, indem das \_ Feld iclientversion auf einen Wert kleiner als 0x00000008 festgelegt wird.

Wenn der \_ Wert des Felds iclientversionfield 0x00000008 oder größer ist, muss der Server überprüfen, ob das \_ Feld ulchecksum gemäß den Angaben in Abschnitt 3.2.4 berechnet wurde. Wenn der \_ ulchecksum-Wert ungültig ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.

Als nächstes überprüft der Server den Status in. Wenn der Status "nicht initialisiert" lautet, muss der Server einen \_ nicht initialisierten CI-E- \_ \_ Fehler (0x8004180b) melden. Wenn der Status "heruntergefahren" lautet, muss der Server den Fehler "CI \_ E \_ Shutdown (0x80041812)" melden.

Nachdem ein Header als gültig festgelegt wurde und der Server den Status "wird ausgeführt" aufweist, muss eine weitere Nachrichten spezifische Verarbeitung durchgeführt werden, wie in den folgenden Unterabschnitten angegeben.

### <a name="3151-remote-indexing-service-catalog-management"></a>3.1.5.1-Dienst Katalog Verwaltung für Remote Indizierung

### <a name="31511-receiving-a-cpmcistateinout-request"></a>3.1.5.1.1 empfangen einer cpmcianout-Anforderung

Wenn der Server eine cpmcistateinout-Nachrichten Anforderung vom Client empfängt, muss der Server zunächst prüfen, ob der Client in einer Liste verbundener Clients enthalten ist. Wenn der Client nicht in der Liste enthalten ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden. Andernfalls muss er auf den Client mit einer cpmcistateinout-Nachricht antworten und ihn mit Informationen zum zugeordneten Katalog des Clients auffüllen, wie in Abschnitt 2.2.3.1 angegeben.

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a>3.1.5.1.2 empfängt eine cpmseterstatuein-Anforderung

Wenn der Server eine cpmsetcatstatein-Nachrichten Anforderung vom Client empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob der Client über Administrator Zugriff verfügt. Wenn der Client keinen Administrator Zugriff hat, muss der Server einen Fehler vom Typ "Status \_ Zugriff \_ verweigert" (0xc0000022) melden.
-   Wenn \_ dwnewstate nicht gleich cicat \_ all geöffnet ist, \_ Ändern Sie den Status des im Feld "Name" angegebenen Katalogs, wie im Feld " \_ dwnewstate" angegeben. Weitere Informationen finden Sie im Abschnitt 2.2.3.2. Wenn der Server keinen Katalog mit dem im Feld "catname" angegebenen Namen findet, muss der Server den \_ Fehler "Ungültiger \_ Parameter (0xc000000D)" zurückgeben.
-   Antworten Sie auf den Client mit einer cpmsetsinstateout-Meldung, bei der \_ dwoldstate auf den vorherigen Status des Katalogs festgelegt werden muss. Wenn \_ dwnewstate gleich cicat \_ all geöffnet ist \_ , muss der Server den Status aller Kataloge überprüfen. wenn alle Elemente gestartet werden \_ , muss dwoldstate auf 0x00000001 festgelegt werden. andernfalls wird \_ dwoldstate auf 0x00000000 festgelegt.

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a>3.1.5.1.3 empfängt eine cpmupdatedocumentsin-Anforderung

Wenn der Server eine cpmupdatedocumentsin-Nachrichten Anforderung empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob der Client in einer Liste verbundener Clients (denen ein Katalog zugeordnet ist) enthalten ist. Wenn der Client nicht in der Liste enthalten ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Überprüfen Sie, ob der Client über Administrator Zugriff verfügt. Wenn der Client keinen Administrator Zugriff auf den Server hat, muss der Server den \_ Fehler Status Zugriff \_ verweigert (0xc0000022) melden.
-   Beginnen Sie mit dem Indizieren des vom Client angegebenen Pfads und Durchführung eines vollständigen oder inkrementellen Scans, abhängig vom Wert des \_ flagfelds in der cpmupdatedocumentsin-Nachricht. Wenn der Pfad nicht zuvor indiziert wurde, muss er der Auflistung indizierter Speicherorte hinzugefügt werden, und es muss eine vollständige Überprüfung durchgeführt werden. Wenn ein unzulässiger Wert des \_ Flags-Felds angegeben ist, muss der Server so agieren, als ob \_ Flag auf upd init festgelegt \_ und eine vollständige Überprüfung durchgeführt wurde. Dieser Vorgang muss in dem Katalog ausgeführt werden, der dem Client zugeordnet ist.
-   Antworten Sie auf den Client mit dem Nachrichten Header für cpmupdatedocumentsin, und legen \_ Sie das Feld Status auf die Ergebnisse der Anforderung fest.

### <a name="31514-receiving-a-cpmforcemergein-request"></a>3.1.5.1.4 Empfangen einer cpmforcemergein-Anforderung

Wenn der Server eine cpmforcemergein-Nachrichten Anforderung empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob der Client in einer Liste verbundener Clients (denen ein Katalog zugeordnet ist) enthalten ist. Wenn sich der Client nicht in der Liste befindet, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Überprüfen Sie, ob der Client über Administrator Zugriff verfügt. Wenn der Client keinen Administrator Zugriff hat, muss der Server einen Fehler vom Typ "Status \_ Zugriff \_ verweigert" (0xc0000022) melden.
-   Beginnen Sie jeden Wartungsprozess, der zum Verbessern der Abfrageleistung in einem Katalog erforderlich ist, der dem Client zugeordnet ist.
-   Antworten Sie auf den Client mit einem Nachrichten Header für cpmforcemergein, und legen \_ Sie das Feld Status auf die Ergebnisse der Anforderung fest.

Beachten Sie, dass der Wartungsprozess asynchron ist und fortgesetzt werden kann, nachdem der Client die Antwortnachricht empfangen hat. Dieser Prozess wirkt sich nicht direkt auf das Protokoll aus (außer der Antwortzeit).

### <a name="3152-remote-indexing-service-querying"></a>3.1.5.2 Remote Index Dienst Abfragen

### <a name="31521-receiving-a-cpmconnectin-request"></a>3.1.5.2.1 empfängt eine cpmconnectin-Anforderung

Wenn der Server eine cpmconnectin-Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob der Client in der Liste der verbundenen Clients enthalten ist. Wenn dies der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Überprüft, ob der angegebene Katalog vorhanden und nicht im beendeten Zustand ist. Wenn dies nicht der Fall ist, muss der Server einen Bericht "CI \_ E \_ No \_ catalog (0x8004181d)" haben.
-   Fügen Sie den Client der Liste der verbundenen Clients hinzu.
-   Ordnen Sie den Katalog dem Client zu.
-   Speichern Sie die Informationen, die in der cpmconnectin-Nachricht (z. b. Katalog Name, Client Version usw.) übermittelt wurden, im Client Zustand.
-   Reagieren Sie auf den Client mit einer cpmconnectout-Nachricht.

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a>3.1.5.2.2 empfängt eine cpmkreatequeryin-Anforderung.

Wenn der Server eine cpmkreatequeryin-Nachrichten Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob der Client in der Liste der verbundenen Clients enthalten ist. Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Überprüfen Sie, ob dem Client bereits eine Abfrage zugeordnet ist. Wenn dies der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Überprüfen Sie, ob der dem Client zugeordnete Katalog den Status aufweist, der die Verarbeitung von Abfragen ermöglicht (cicat \_ schreibgeschützt oder cicat \_ beschreib bar). Wenn dies nicht der Fall ist, muss der Server einen Fehler der Abfrage " \_ \_ keine \_ Abfrage (0x8004160c)" melden.
-   Analysieren Sie den Einschränkungs Satz, die Sortier Reihenfolgen und die in der Abfrage angegebenen Gruppierungen. Wenn auf dem Server ein Fehler auftritt, muss ein entsprechender Fehler gemeldet werden. Wenn dieser Schritt aus einem anderen Grund fehlschlägt, muss der Server den gefundenen Fehler melden. Weitere Informationen zum Indizieren von Dienst Abfrage Fehlern finden Sie unter \[ MSDN-queryerr \] .
-   Speichern Sie die Suchabfrage im Status für den Client.
-   Nehmen Sie alle Vorbereitungen vor, die zum Verarbeiten von Zeilen an einen Client erforderlich sind, und ordnen Sie die Abfrage den entsprechenden Cursor Handles zu (abhängig von Informationen, die in der Meldung "cpmkreatequeryin"
-   Fügen Sie diese Handles der Liste der Cursor Handles des Clients hinzu, und initialisieren Sie Listen von Kapitel Handles und Lesezeichen.
-   Initialisieren der Liste der Kapitel Handles für jeden Cursor in dieser Abfrage an DB \_ NULL \_ hChapter
-   Initialisieren Sie die Liste der Lesezeichen Handles für jeden Cursor in dieser Abfrage an einen Satz von dbbmk \_ First und dbbmk \_ Last.
-   Markieren Sie die Abfrage als nicht überwacht für Änderungen.
-   Initialisieren Sie die Anzahl der Zeilen für die aktuell berechnete Anzahl von Zeilen (die 0 sein kann, wenn die Abfrage nicht ausgeführt werden konnte, oder eine Zahl, wenn die Abfrage gerade ausgeführt wird), und initialisieren Sie den Zähler und den Nenner des abfrageabschlusses.
-   Reagieren Sie auf den Client mit einer cpmkreatequeryout-Nachricht.

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a>3.1.5.2.3 empfängt eine cpmgetquerystatus in-Anforderung.

Wenn der Server eine cpmgetquerystatusin-Nachrichten Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Überprüfen Sie, ob das Cursor Handle in einer Liste der Cursor Handles des Clients enthalten ist. Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.
-   Bereiten Sie eine cpmgetquerystatusout-Nachricht vor. Der Server muss den aktuellen Abfrage Status abrufen und im \_ Feld "qStatus" festlegen (Weitere Informationen finden Sie unter 2.2.3.11). Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server einen Fehler melden.
-   Reagieren Sie auf den Client mit der cpmgetquerystatusout-Nachricht.

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a>3.1.5.2.4 empfängt eine cpmgetquerystatusexin-Anforderung.

Wenn der Server eine cpmgetquerystatusexin-Nachrichten Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Überprüfen Sie, ob das übergebenen Cursor Handle in einer Liste der Cursor Handles des Clients enthalten ist. Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.
-   Bereiten Sie eine cpmgetquerystatusexout-Nachricht vor. Der Server muss den aktuellen Abfrage Status und den Abfrage Fortschritt abrufen und qStatus festlegen (siehe 2.2.3.11 auf mögliche Werte), \_ dwratiofinishednenner und \_ dwratiofinishedzähler. Anschließend muss die Anzahl der Zeilen in den Abfrage Ergebnissen auf \_ crowstotal festgelegt werden. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server melden, dass ein Fehler aufgetreten ist.
-   Rufen Sie Informationen zum Katalog des Clients ab, und füllen Sie \_ cfiltereddocuments und \_ cdocumentstofilter aus. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server melden, dass ein Fehler aufgetreten ist.
-   Rufen Sie die Position des Lesezeichens ab, das durch das Handle im \_ BMK-Feld angegeben wird, und füllen Sie das verbleibende \_ irowbmk-Feld in der cpmgetquerystatusexout-Nachricht aus. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server melden, dass ein Fehler aufgetreten ist.
-   Reagieren Sie auf den Client mit der cpmgetquerystatusexout-Nachricht.

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a>3.1.5.2.5 empfängt eine cpmratiofinishedin-Anforderung

Wenn der Server eine cpmratiofinishedin-Nachrichten Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Überprüfen Sie, ob das übergebenen Cursor Handle in der Liste der Cursor Handles des Clients enthalten ist. Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.
-   Bereiten Sie eine cpmratiofinishedout-Nachricht vor. Der Server muss den Abfrage Status des Clients abrufen und \_ ulzähator \_ -, ulnenner-und \_ Crows-Felder ausfüllen. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server melden, dass ein Fehler aufgetreten ist.
-   Wenn \_ Crows gleich der zuletzt gemeldeten Anzahl von Zeilen für diese Abfrage ist, legen \_ Sie fnewrows auf 0x00000000 fest, und legen Sie andernfalls 0x00000001 fest.
-   Aktualisieren Sie die zuletzt gemeldete Anzahl von Zeilen für diese Abfrage auf den Wert von \_ Crows.
-   Antworten Sie den Client mit der cpmratiofinishedout-Nachricht.

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a>3.1.5.2.6 empfängt eine cpmsetbindingsin-Anforderung.

Wenn der Server eine cpmsetbindingsin-Nachrichten Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Überprüfen Sie, ob das übergebenen Cursor Handle in der Liste der Cursor Handles des Clients enthalten ist. Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.
-   Stellen Sie sicher, dass die Bindungs Informationen gültig sind (d. h. Spalte zumindest den Wert, die Länge oder den Status, der zurückgegeben werden soll, keine Überlappung in Bindungen für Wert, Länge oder Status; und Wert, Länge und Status in der angegebenen Zeilengröße) und, wenn kein DB \_ e \_ badbindinfo (0x80040e08)-Fehler gemeldet wird.
-   Speichern Sie die Bindungs Informationen, die den im Feld acolumschlag angegebenen Spalten zugeordnet sind. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server melden, dass ein Fehler aufgetreten ist.
-   Antworten Sie auf den Client mit einem Nachrichten Header (nur) \_ , wenn msg auf cpmsetbindingsin festgelegt ist und \_ der Status auf die Ergebnisse der angegebenen Bindung festgelegt ist.

### <a name="31527-receiving-a-cpmgetrowsin-request"></a>3.1.5.2.7 empfängt eine cpmgetrowsin-Anforderung

Wenn der Server eine cpmgetrowsin-Nachrichten Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Überprüfen Sie, ob das übergebenen Cursor Handle in der athelist der Cursor Zieh Punkte des Clients ist. Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.
-   Überprüfen Sie, ob der Client über einen aktuellen Satz von Bindungen verfügt. Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.
-   Bereiten Sie eine cpmgetrowsout-Nachricht vor. Der Server muss den Cursor in den Abfrage Ergebnissen positionieren, wie in der Such Beschreibung angegeben. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server melden, dass ein Fehler aufgetreten ist.
-   Rufen Sie beliebig viele Zeilen ab, die in einen Puffer passen, die Größe wird durch den \_ cbread-Puffer angegeben, jedoch nicht mehr als durch \_ crowstotransfer angegeben. Beim Abrufen von Zeilen muss der Server den Eigenschafts Werttyp jeder ausgewählten Spalte mit dem im aktuellen Bindungs Satz des Clients (Abschnitt 3.1.1) angegebenen Typ vergleichen. Wenn der Typ in der Bindung nicht die VT \_ -Variante ist, muss der Server versuchen, den-Eigenschafts Wert der Spalte in diesen Typ zu konvertieren. Andernfalls \_ muss der Eigenschafts Wert im normalen Typ zurückgegeben werden, wenn das DBPROP useextendeddbtypes-Flag im DBPROPSET queryext-Eigenschaften Satz des Clients festgelegt ist \_ oder wenn der Eigenschafts Wert der Spalte kein VT- \_ Vektortyp ist. Wenn keines dieser Fälle zutrifft (d. h., der Server verfügt über einen VT \_ -Vektortyp, und der Client unterstützt keinen VT \_ -Vektor), muss der Server versuchen, ihn wie folgt in einen VT \_ -Arraytyp zu konvertieren: VT \_ I8, VT \_ UI8, VT \_ FILETIME und VT \_ CLSID Array-Elemente können nicht konvertiert werden, sondern fehlschlagen. VT \_ LPSTR-und VT \_ LPWSTR-Array Elemente müssen in VT \_ BSTR konvertiert werden; Array Elemente aller anderen Typen müssen unverändert bleiben. Wenn Zeilen Spalten außerdem Kapitel Handles oder Lesezeichen Handles enthalten, muss der Server die entsprechenden Listen aktualisieren. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server melden, dass ein Fehler aufgetreten ist.
-   Speichern Sie die tatsächliche Anzahl von Zeilen, die in \_ crowszurück gegeben werden.
-   Kopieren Sie die Such Beschreibung und das Kapitel Feld aus cpmgetrowsin in eine zu sendende cpmgetrowsout-Nachricht.
-   Speichert abgerufene Zeilen im Zeilen Feld (siehe Hinweis zum Status Byte unten und Abschnitt 2.2.3.16 für die Struktur des Rows-Felds).
-   Reagieren Sie auf den Client mit der cpmgetrowsout-Nachricht.

Hinweis für das Feld "Status Byte":

Wenn statusused in der ctablecolumn der cpmsetbindingin-Nachricht für die Spalte auf 0x01 festgelegt ist, muss der Server das Status Byte (das sich am statusoffset vom Anfang der Zeile befindet) auf einen der folgenden Werte festlegen:



| Wert | Bedeutung        |
|-------|----------------|
| 0x00  | Status       |
| 0x01  | Status verzögert |
| 0x02  | Status NULL     |



 

Wenn der Eigenschafts Wert für diese Zeile nicht vorhanden ist, muss der Server das Status Byte auf statusnull festlegen. Wenn der Wert zu groß ist, um in der cpmgetrowsout-Nachricht übertragen zu werden, muss der Server das Status Byte auf statusaufgeschoben festlegen. Andernfalls muss der Server das Status Byte auf statusok festlegen.

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a>3.1.5.2.8 empfängt eine cpmfetchvaluein-Anforderung

Wenn der Server eine cpmfetchvaluein-Nachrichten Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Bereiten Sie eine cpmfetchvalueout-Nachricht vor. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server einen Fehler melden.
-   Suchen Sie nach dem Dokument, das durch das \_ wid-Feld angegeben wird, und überprüfen Sie, ob die Eigenschaften-ID für dieses Dokument (später als "Eigenschafts Wert" bezeichnet) für diesen Client verfügbar ist. Wenn dieser Wert nicht verfügbar ist, muss der Server \_ fvalueist auf 0x00000000 festlegen und andernfalls \_ fvalueist auf 0x00000001 festgelegt. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server einen Fehler melden.
-   Wenn \_ fvalueist gleich 0x00000001 ist, muss der Server folgende Aktionen ausführen:
-   -   Serialisieren Sie den Eigenschafts Wert in eine serializedpropertyvalue-Struktur, und kopieren Sie, beginnend \_ mit dem cbsofar-Offset, höchstens \_ cbblock-bytes (aber nicht über das Ende der serialisierten Eigenschaft) in das vValue-Feld. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server einen Fehler melden.
    -   Legen \_ Sie cbValue auf die Anzahl der im vorherigen Schritt kopierten Bytes fest.
    -   Legen Sie VType auf den Eigenschaftentyp des Eigenschafts Werts fest.
    -   Wenn die Länge der serialisierten Eigenschaft größer als \_ cbsofar zu \_ cbValue addiert ist, wird Set \_ fmoreauf 0x00000001 festgelegt. andernfalls wird es auf 0x00000000 festgelegt.

-   Antworten auf den Client mit der cpmfetchvalueout-Meldung

### <a name="31529-receiving-a-cpmgetnotify-request"></a>3.1.5.2.9 empfängt eine cpmgetnotify-Anforderung

Wenn der Server eine cpmgetnotify-Nachricht von einem Client empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Wenn seit der letzten cpmsendnotifyout-Nachricht für diesen Client keine Änderungen im Abfrageresultset vorhanden sind, oder wenn die Abfrage zurzeit nicht auf Änderungen im Resultset überwacht wird, muss der Server mit der cpmgetnotify-Nachricht antworten und die Abfrage auf Änderungen im Resultset überwachen. Wenn das Abfrageresultset zu einem späteren Zeitpunkt geändert wird, muss der Server genau eine cpmsendnotifyout-Nachricht an den Client senden und muss die Änderung im \_ watchnotify-Feld angeben.
-   Wenn seit der letzten cpmsendnotifyout-Nachricht Änderungen am Abfrageresultset vorgenommen wurden, muss der Server mit cpmsendnotifyout Antworten und die Änderung im \_ watchnotify-Feld angeben. Beachten Sie, dass bei vielen Änderungen an den Abfrage Ergebnissen dbwatchnotify \_ rowschangidie Priorität hat (d. h., wenn die Abfrage erneut ausgeführt wurde, die Anzahl der Zeilen geändert wurde und die Abfrage erneut ausgeführt wurde, würde das gemeldete Ereignis dbwatchnotify \_ rowschangilauten).

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a>3.1.5.2.10 empfängt eine cpmgetapproximatepositionin-Anforderung.

Wenn der Server eine cpmgetapproximatepositionin-Nachrichten Anforderung vom Client empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Überprüfen Sie, ob der übergebenen Cursor Handle, Kapitel Handle und Lesezeichen Handle in den entsprechenden Listen aufgeführt sind. Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.
-   Suchen Sie eine Zeile, die mit dem Lesezeichen Handle in den Abfrage Ergebnissen verknüpft ist, und nähern Sie die Position der Zeile im Rowset, auf die durch das Kapitel handle verwiesen wird, und bestimmen Sie den Zähler und Nenner für die Position. Beachten Sie, dass das \_ \_ entsprechende Kapitel das hauptrowset der Abfrage ist, wenn es sich bei dem Kapitel handle um DB null hChapter handelt. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server einen Fehler melden.
-   Reagieren Sie auf den Client mit einer cpmfetchvalueout-Nachricht.

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a>3.1.5.2.11 empfängt eine cpmcomparebmkin-Anforderung

Wenn der Server eine cpmcomparebmkin-Nachrichten Anforderung vom Client empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Überprüfen Sie, ob der übergebenen Cursor Handle, Kapitel Handle und Lesezeichen Handles in den entsprechenden Listen aufgeführt sind. Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.
-   Bereiten Sie eine cpmcomparebmkout-Nachricht vor.
-   Wenn Lesezeichen Handles gleich sind, \_ muss dwcomparison auf DbCompare EQ festgelegt werden \_ .
-   Wenn eines der Lesezeichen Handles zuerst dbbmk \_ First oder dbbmk \_ Last ist, \_ muss dwcomparison auf DbCompare ne festgelegt werden \_ .
-   Andernfalls muss der Server folgende Aktionen ausführen:
-   -   Suchen von Zeilen, auf die von jedem Lesezeichen Handle in den Abfrage Ergebnissen verwiesen wird
    -   Wenn eine der Zeilen nicht in dem Kapitel liegt, das durch das Kapitel Handle in cpmcomparebmkin angegeben wird, \_ muss dwcomparison auf DbCompare notcompare festgelegt werden \_ .
    -   Wenn sich beide Zeilen im gleichen Kapitel befinden, muss der Server eine Position der Zeilen im Rowset anweisen, auf die durch den Handle dieses Kapitels verwiesen wird. Anschließend müssen Sie Positionswerte vergleichen und \_ dwcomparison auf DbCompare lt festlegen, \_ Wenn die Position der ersten Zeile kleiner ist als die Position der zweiten Zeile \_ . andernfalls muss dwcomparison auf DbCompare gt festgelegt werden \_ .

-   Reagieren Sie auf den Client mit der gefüllten cpmcomparebmkout-Nachricht.

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a>3.1.5.2.12 empfängt eine cpmrestartpositionin-Anforderung.

Wenn der Server die cpmrestartpositionin-Nachrichten Anforderung vom Client empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Überprüfen Sie, ob der übergebenen Cursor Handle und das Kapitel Handle in den entsprechenden Listen vorliegen. Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.
-   Bewegen Sie den Cursor an den Anfang des Kapitels, der durch das Kapitel Handle identifiziert wird. Beachten Sie, dass das \_ \_ entsprechende Kapitel das hauptrowset der Abfrage ist, wenn es sich bei dem Kapitel handle um DB null hChapter handelt. Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server einen Fehler melden.
-   Reagieren Sie auf den Client mit einer cpmrestartpositionin-Nachricht.

### <a name="315213-receiving-a-cpmfreecursorin-request"></a>3.1.5.2.13 empfängt eine cpmfreecursorin-Anforderung.

Wenn der Server eine cpmfreecursorin-Nachrichten Anforderung vom Client empfängt, muss der Server folgende Aktionen ausführen:

-   Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist. Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.
-   Überprüfen Sie, ob das übergebenen Cursor Handle in der Liste der Cursor Handles des Clients enthalten ist. Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.
-   Geben Sie den Cursor und die zugehörigen Ressourcen (siehe Abschnitt 3.1.1 für die komplette Liste) für dieses Cursor Handle frei.
-   Entfernen Sie den Cursor aus der Liste der Cursor für diesen Client.
-   Antworten Sie mit einer cpmfreecursorout-Meldung, und legen Sie das \_ Feld ccursorsrestwert auf die Anzahl der verbleibenden Cursors fest. in der Liste dieses Clients.
-   Wenn für diesen Client keine weiteren Cursor vorhanden sind, muss der Server die Abfrage und die zugehörigen Ressourcen freigeben (siehe Abschnitt 3.1.1).

### <a name="315214-receiving-a-cpmdisconnect-request"></a>3.1.5.2.14 empfängt eine cpmdisconnect-Anforderung

Wenn der Server eine cpmdisconnect-Nachrichten Anforderung vom Client empfängt, muss der Server den Client aus der Liste der verbundenen Clients entfernen und alle dem Client zugeordneten Ressourcen freigeben.

### <a name="316-timer-events"></a>3.1.6-Timer-Ereignisse

Keine.

### <a name="317-other-local-events"></a>3.1.7 andere lokale Ereignisse

Wenn der Server angehalten wird, muss er zunächst in den Zustand "Herunterfahren" übergehen. Er muss dann das lauschen an der Pipe beenden, alle anderen Implementierungs spezifischen Aufgaben für das Herunterfahren ausführen und dann in den Zustand "beendet" übergehen.

### <a name="32-client-details"></a>3,2 Client Details

### <a name="321-abstract-data-model"></a>3.2.1 abstraktes Datenmodell

Im folgenden Abschnitt werden die Daten und der Status des Inhalts Index Dienst-Protokoll Clients angegeben. Die bereitgestellten Daten dienen dazu, die Erläuterung der Verhalten des Protokolls zu vereinfachen. In diesem Abschnitt wird nicht vorgeschrieben, dass Implementierungen dieses Modells einhalten, solange das externe Verhalten mit dem in diesem Dokument beschriebenen übereinstimmt.

Ein Client weist den folgenden abstrakten Zustand auf:

-   **Letzte gesendete Nachricht**: eine Kopie der letzten Nachricht, die an den Server gesendet wurde.
-   **Aktueller Eigenschafts Wert**: ein partieller Wert einer "verzögerten" Eigenschaft, die gerade abgerufen wird.
-   **Aktuell empfangene Bytes**: die Anzahl von Bytes, die bisher für den aktuellen Eigenschafts Wert empfangen wurden.
-   **Status der Named Pipe-Verbindung**: eine Verbindung mit dem Server

### <a name="322-timers"></a>3.2.2 Timer

Es sind keine protokolltimer erforderlich.

### <a name="323-initialization"></a>3.2.3-Initialisierung

Es werden keine Aktionen ausgeführt, bis eine höhere ebenenanforderung empfangen wird.

### <a name="324-higher-layer-triggered-events"></a>3.2.4 Higher-Layer ausgelöste Ereignisse

Wenn eine Anforderung von einer höheren Ebene empfangen wird, muss der Client eine Named Pipe Verbindung mit dem Server herstellen, wobei die in Abschnitt 2,1 angegebenen Details verwendet werden. Wenn dies nicht möglich ist, muss die Anforderung höherer Ebene fehlgeschlagen sein. Das heißt, wenn eine Verbindung nicht hergestellt werden kann, liegt es in der Verantwortung der höheren Ebene, wenn dies gewünscht wird.

Einem Header muss ein in Abschnitt 2.2.2 angegebener Feldsatz vorausgesetzt werden.

Bei Nachrichten, die als Prüfsumme ungleich NULL angegeben werden, \_ muss der ulchecksum-Wert wie folgt berechnet werden:

1.  Der Inhalt der Nachricht nach dem \_ ulReserved2-Feld im Nachrichten Header muss als Sequenz von 32-Bit-Ganzzahlen interpretiert werden. Der Client muss die Summe der numerischen Werte berechnen, die durch die ganzen Zahlen angegeben werden.
2.  Berechnen Sie das bitweise XOR dieses Werts mit 0x59533959.
3.  Subtrahieren Sie den von der Meldung angegebenen Wert \_ aus dem Wert, der sich aus dem bitweisen XOR ergibt.

### <a name="3241-remote-indexing-service-catalog-management"></a>3.2.4.1-Dienst Katalog Verwaltung für Remote Indizierung

Jede Nachricht wird von einer Anforderung von der höheren Ebene ausgelöst. Es wird keine Nachrichten Sequenz vom Client für CISP-Nachrichten Anforderungen für die Remote Verwaltung von Katalogen erzwungen, aber (mit Ausnahme einer cpmsetcatstatein-Meldung) antwortet der Server nur mit Erfolg, wenn der Client zuvor über eine cpmconnectin-Nachricht eine Verbindung hergestellt hat.

### <a name="32411-sending-a-cpmcistateinout-request"></a>3.2.4.1.1 Senden einer cpmcistatueinout-Anforderung

In der Regel wird der Protokoll Client von der höheren Ebene aufgefordert, eine cpmcistateinout-Nachricht zu senden, wenn Informationen zum Indizieren von Diensten auf dem Server erforderlich sind.

Wenn Sie aufgefordert werden, diese Nachricht zu senden, muss der Client folgende Aktionen ausführen:

-   Senden Sie eine cpmcistateinout-Nachricht, wie im Abschnitt 2.2.3.1 angegeben, an den Server.
-   Warten Sie, bis die Meldung "cpmcistateinout" vom Server empfangen wurde, und verwerfen Sie alle anderen Nachrichten im Hintergrund.
-   Melden Sie den Wert des \_ Felds Status der Antwort, und bei erfolgreicher Ausführung die Informationsstruktur zurück zur höheren Ebene.

### <a name="32412-sending-a-cpmsetcatstatein-request"></a>3.2.4.1.2 Senden einer cpmset| Status-Anforderung

In der Regel wird der Protokoll Client von der höheren Ebene aufgefordert, eine cpmsetsinstatein-Nachricht zu senden, wenn er Informationen zu einem Katalog oder zu allen Katalogen benötigt. Für diese Nachricht muss die höhere Ebene dem Protokoll Client einen Wert für \_ dwnewstate und ggf. den Namen des Katalogs bereitstellen.

Wenn Sie aufgefordert werden, diese Nachricht zu senden, muss der Client folgende Aktionen ausführen:

-   Senden Sie eine cpmsetcatstatein-Nachricht, wie in 2.2.3.2 angegeben, an den Server.
-   Warten Sie, bis eine cpmsetcatstateout-Nachricht vom Server empfangen wurde, und verwerfen Sie alle anderen Nachrichten im Hintergrund.
-   Melden Sie den Wert des \_ Felds Status der Antwort. wenn der Wert erfolgreich war, wird \_ dwoldstate wieder auf die höhere Ebene zurückgegeben.

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a>3.2.4.1.3 Senden einer cpmupdatedocumentsin-Anforderung

Die höhere Ebene fordert normalerweise auf, diese Nachricht zu senden, wenn Sie Dokumente in einem vorhandenen Pfad aktualisieren oder dem Index einen neuen Dateipfad hinzufügen muss. Daher besteht die höhere Ebene darin, den Pfad und den Typ eines Scans bereitzustellen, der im Abschnitt 2.2.3.4 angegeben ist, in dem ein inkrementelles oder vollständiges Update für vorhandene Pfade vorgesehen ist, und die neue Initialisierung ist für neue Pfade vorgesehen.

Der Client muss die folgenden Schritte ausführen, um die Anforderung höherer Ebene verarbeiten zu können:

-   Senden Sie eine cpmupdatedocumentsin-Nachricht, wie im Abschnitt 2.2.3.4 angegeben, an den Server.
-   Warten Sie, bis die cpmupdatedocumentsin-Nachricht vom Server empfangen wurde, und verwerfen Sie alle anderen Nachrichten im Hintergrund.
-   Melden Sie den Wert des \_ Felds Status der Antwort zurück an die höhere Ebene.

### <a name="32414-sending-a-cpmforcemergein-request"></a>3.2.4.1.4 Senden einer cpmforcemergein-Anforderung

In der Regel fordert die höhere Schicht auf, diese Nachricht zu senden, wenn die Abfrageleistung verbessert werden muss, oder Sie ist Teil der geplanten Dienst Wartung für die Indizierung.

Um der höheren Ebene gerecht zu werden, muss der Client folgende Aktionen ausführen:

-   Senden Sie die im Abschnitt 2.2.3.5 angegebene cpmforcemergein-Nachricht an den Server.
-   Warten Sie, bis eine cpmupdatedocumentsin-Nachricht vom Server empfangen wurde, und verwerfen Sie alle anderen Nachrichten im Hintergrund.
-   Melden Sie den Wert des \_ Felds Status der Antwort zurück an die höhere Ebene.

### <a name="3242-remote-indexing-service-catalog-query-messages"></a>3.2.4.2-Dienst Katalog-Abfrage Nachrichten für Remote Indizierung

Mit Ausnahme von "cpmgetrowsin/cpmgetrowsout", "cpmfetchvaluein/cpmfetchvalueout" besteht eine 1:1-Beziehung zwischen CISP-Nachrichten und Anforderungen höherer Ebenen. Für die beiden oben genannten Ausnahmen können vom Client mehrere Nachrichten generiert werden, um die Größenanforderungen zu erfüllen oder eine gesamte Eigenschaft abzurufen. Die höhere Ebene verfolgt in der Regel alle Abfrage spezifischen Informationen (z. b. geöffnetes Cursor Handle, zulässige Werte für Lesezeichen und Kapitel Handles, wid-Werte für verzögerte Eigenschaftswerte usw.) und nach, wenn der Client in einem verbundenen Zustand ist. Dies wird jedoch vom Client nicht erzwungen.

Zu Veranschaulichung veranschaulicht der Client Teil des Diagramms in Abschnitt 3 diese Sequenz für eine einfache Indizierungs Dienst Abfrage.

### <a name="32421-sending-a-cpmconnectin-request"></a>3.2.4.2.1 Senden einer cpmconnectin-Anforderung

Bei dieser Nachricht handelt es sich in der Regel um die erste Anforderung von der höheren Ebene (wenn der Client nicht verbunden ist, wird der Großteil der Nachrichten vom Server mit Ausnahme von cpmsetcatstatein nicht ausgeführt). Die höhere Ebene stellt dem Protokoll Client Informationen zur Verfügung, die zum Herstellen einer Verbindung erforderlich sind.

Um die höhere Ebene zu verarbeiten, muss der Client die folgenden Schritte ausführen:

-   Füllen Sie die Nachricht mit Informationen aus, die der Client der höheren Ebene bereitgestellt hat (siehe Abschnitt 2.2.3.6) in \_ iclientversion, MachineName, username, PropertySet1, PropertySet2 und apropertyset.
-   Legen Sie " \_ lclientisremote", " \_ cbblob", "cbBlob2", " \_ cpropset" und "cextpropset" gemäß 2.2.3.6 fest
-   Legen Sie die Prüfsumme im \_ Feld ulchecksum fest.
-   Sendet die cpmconnectin-Nachricht an den Server.
-   Warten Sie, bis eine cpmconnectout-Nachricht vom Server empfangen wurde, und verwerfen Sie alle anderen Nachrichten im Hintergrund.
-   Melden Sie den Wert des \_ Felds Status der Antwort. wenn dies erfolgreich war, wird die \_ Server Version wieder auf die höhere Ebene zurückgegeben.

Zu informativen Zwecken wird erwartet, dass höhere Ebenen in der Regel die folgenden Aktionen ausführen, wenn eine Verbindung erfolgreich hergestellt wird, diese werden jedoch vom CISP-Client nicht erzwungen:

-   Verwenden von Remote Index-Dienst Katalog-Verwaltungsnachrichten für administrative Aufgaben
-   Verwenden Sie eine cpmkreatequeryin-Anforderung, um eine Suchabfrage zu erstellen, mit der Ergebnisse aus dem Katalog abgerufen werden.

### <a name="32422-sending-a-cpmcreatequeryin-request"></a>3.2.4.2.2 Senden einer cpmkreatequeryin-Anforderung

Die höhere Ebene stellt in der Regel Informationen für die Abfrage Erstellung bereit, sobald der Protokoll Client verbunden ist. Die höhere Ebene stellt dem Client einen Einschränkungs Satz, Spalten Satz, Sortier Reihenfolgen-Regeln und einen Kategoriesatz (die jeweils weggelassen werden können), Rowseteigenschaften und Eigenschaften-ID-Mapper-Struktur bereit.

Wenn diese Anforderung von einer höheren Ebene empfangen wird, muss der Client die folgenden Schritte ausführen:

-   Bereiten Sie ein cpmkreatequeryout wie folgt vor.
-   -   Wenn ein Spalten Satz vorhanden ist, legen Sie ccolumnssetvoreinstellung auf 0x01 fest, und füllen Sie das columnsset-Feld aus.
    -   Wenn Einschränkungen vorhanden sind, legen Sie "" auf "0x01" fest, und füllen Sie das Einschränkungs Feld aus.
    -   Wenn eine Sortier Menge vorhanden ist, füllen Sie das sortset-Feld aus.
    -   Wenn ein Kategorisierungs Satz vorhanden ist, legen Sie csortsetpresent auf 0x01 fest, und füllen Sie das Feld kategorizationset aus.
    -   Legen Sie die übrigen Felder wie in 2.2.3.8 angegeben fest.

-   Berechnen Sie \_ das ulchecksum-Feld in der Kopfzeile.
-   Senden Sie die cpmkreatequeryin-Nachricht an den Server.
-   Warten Sie, bis eine cpmkreatequeryout-Nachricht empfangen wird (siehe Details im Abschnitt 3.2.5.1.1), und verwerfen Sie alle anderen Nachrichten im Hintergrund.
-   Melden Sie den Wert des \_ Felds Status der Antwort, und, wenn er erfolgreich war, das Array von Cursor Handles und informative boolesche Werte (wie in 2.2.3.9 angegeben) zurück zur höheren Ebene.

### <a name="32423-sending-a-cpmsetbindingsin-request"></a>3.2.4.2.3 Senden einer cpmsetbindingsin-Anforderung

In der Regel legt die höhere Ebene Bindungen für jede Spalte fest, die in den Zeilen zurückgegeben wird, wenn Sie bereits über ein gültiges Cursor Handle verfügt (nach dem erfolgreichen Empfang von cpmkreatequeryout siehe Abschnitt 3.2.5.1.1). Bei der höheren Version wird erwartet, dass ein Array von ctablecolumn-Strukturen, wie im Abschnitt 2.2.4.31 angegeben, für das Feld acolumschlag und ein gültiges Cursor Handle bereitgestellt wird.

Wenn diese Anforderung von der höheren Ebene empfangen wird, muss der Client die folgenden Schritte ausführen:

-   Berechnen Sie die Anzahl der ctablecolumn-Strukturen im acolenumns-Array, und legen Sie das CColumns-Feld auf diesen Wert fest.
-   Berechnen Sie die Gesamtgröße der CColumns-und acolenns-Felder in Bytes, und legen \_ Sie für das Feld cbbindingdesc den Wert fest.
-   Legen Sie in der cpmsetbindingsin-Nachricht angegebene Felder auf die Werte fest, die von der höheren Anwendungsebene bereitgestellt werden. Legen \_ Sie das Feld ulchecksum auf den im Abschnitt 3.2.5 angegebenen Wert fest.
-   Sendet die abgeschlossene cpmsetbindignsin-Nachricht an den Server.
-   Warten Sie, bis eine cpmsetbindingsin-Nachricht vom Server empfangen wurde, und verwerfen Sie andere Nachrichten.
-   Geben Sie den Status \_ des Felds Status der Antwort auf die höhere Ebene an.

Zu informativen Zwecken wird erwartet, dass eine höhere Ebene in der Regel einen Client anfordert, eine cpmgetrowsin-Nachricht zu senden. Dies wird jedoch nicht durch das Content Index Service-Protokoll erzwungen.

### <a name="32424-sending-a-cpmgetrowsin-request"></a>3.2.4.2.4 Senden einer cpmgetrowsin-Anforderung

Wenn die höhere Ebene im Begriff ist, Zeilen Informationen zu empfangen, stellt Sie Protokoll Client einen gültigen Cursor und ein Kapitel Handle bereit und gibt entsprechende Such Beschreibungen. In der Regel wird eine höhere Ebene erwartet, wenn Sie über ein gültiges Cursor-und/oder Kapitel Handle verfügt und die Bindungen mit der cpmsetbindingsin-Nachricht festgelegt wurden. Um auf das Rowset in einem Kapitel zuzugreifen, besteht die höhere Ebene darin, das Kapitel Handle zu verwenden, das vom Server in einer früheren cpmgetrowsout-Nachricht empfangen wurde.

Wenn diese Anforderung von der höheren Ebene empfangen wird, muss der Client die folgenden Schritte ausführen:

-   Bestimmen Sie, welcher ganzzahlige Wert ohne Vorzeichen für das \_ cbreadbuffer-Feld angegeben werden soll. Um diesen Wert zu bestimmen, muss der Client den maximalen Wert von folgendem annehmen:
-   -   1000-mal der Wert des c- \_ rowstotransfer-Felds.
    -   Wert von \_ cbrowwidth, aufgerundet auf das nächste 512 Byte Vielfache.
    -   Verwenden Sie die höhere dieser beiden Werte, bis zum 16-KB-Limit.
    -   In Fällen, in denen eine einzelne Zeile größer als 16K ist, kann der Server keine Ergebnisse an diese Abfrage zurückgeben.

Geben Sie eine Client Basis für Zeilendaten variabler Größe im Client Adressraum im \_ Feld ulclientbase an.

*Windows-Verhalten: bei einem 32-Bit-Client, der mit einem 32-Bit-Server kommuniziert, oder einem 64-Bit-Client, der mit einem 64-Bit-Server kommuniziert, wird dieser Wert auf eine Speicheradresse des empfangenden Puffers im Anwendungsprozess festgelegt. Dies ermöglicht die Verwendung von Zeigern, die im Feld Zeilen von cpmgetrowsout als korrekte Speicher Zeiger in einem Client Anwendungsprozess angezeigt werden. Andernfalls wird Sie auf 0x00000000 festgelegt.*

-   Berechnen Sie die Größe der Such Beschreibung, und legen Sie Sie im \_ Feld cbseek fest.
-   Legen Sie den Wert von cbreserved (der als Offset für Zeilen Start fungieren soll) auf den Wert von \_ cbseek Plus 0x14 fest.
-   Senden Sie eine cpmconnectin-Nachricht, die in 2.2.3.15 angegeben ist, an den Server.

### <a name="32425-sending-a-cpmfetchvaluein-request"></a>3.2.4.2.5 Senden einer cpmfetchvaluein-Anforderung

Wenn der Client eine cpmgetrowsout-Antwort vom Server empfängt, bei der das Status-Feld der Spalte auf statusaufgeschoben (0x01) festgelegt ist, bedeutet dies, dass der Eigenschafts Wert nicht im Zeilen Feld der cpmgetrowsout-Nachricht enthalten war. In diesem Fall wird der Protokoll Client von der höheren Ebene in der Regel aufgefordert, den Wert mithilfe der cpmfetchvaluein-Nachricht abzurufen. Außerdem wird der Wert PROPSPEC und \_ wid für eine verzögerte Eigenschaft bereitgestellt, die der Protokoll Client in der ersten cpmfetchvaluein-Nachricht verwenden muss.

Wenn dies die erste cpmfetchvaluein-Nachricht ist, die der Client zum Anfordern der angegebenen Eigenschaft gesendet hat, muss der Client die folgenden Schritte ausführen:

-   Legen Sie alle Felder in einer Nachricht fest, wie im Abschnitt 2.2.3.19 angegeben.
-   Legen \_ Sie cbsofar auf 0x00000000 fest.
-   Aktuelle empfangene Bytes auf 0 festlegen.
-   Senden Sie die cpmfetchvaluein-Nachricht an den Server.

### <a name="32426-sending-a-cpmfreecursorin-request"></a>3.2.4.2.6 Senden einer cpmfreecursorin-Anforderung

Wenn die Suchabfrage von der höheren Ebene nicht mehr verwendet wird, können die Ressourcen auf dem Server freigegeben werden, indem der Client aufgefordert wird, eine cpmfreecursorin-Nachricht zu senden.

Wenn diese Anforderung empfangen wird, muss der Client eine in 2.2.3.28 angegebene cpmfreecursorin-Nachricht an den Server senden, die das von der oberen Ebene angegebene Handle enthält.

### <a name="32427-sending-a-cpmdisconnect-message"></a>3.2.4.2.7 Senden einer cpmdisconnect-Nachricht

Wenn die höhere Ebene keine Abfragen für den Indizierungs Dienst aufweist, kann die Anwendung zum Freigeben von mehr Server Ressourcen von der Anwendung anfordern, dass der Client eine cpmdisconnect-Nachricht an den Server sendet. Wenn diese Abfrage empfangen wird, muss der Client die Nachricht einfach wie angefordert senden. Vom Server wird keine Antwort auf diese Nachricht ausgegeben.

### <a name="325-message-processing-and-sequencing-rules"></a>3.2.5 Nachrichtenverarbeitungs-und Sequenz Regeln

Wenn der Client eine Nachrichten Antwort vom Server empfängt, muss der Client die zuletzt gesendete Nachricht verwenden, um zu ermitteln, ob die vom Server empfangene Nachricht vom Client erwartet wird. Alle Nachrichten mit \_ einem Nachrichtenfeld, die sich von dem in der letzten Sende Nachricht unterscheiden, müssen ignoriert werden.

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a>3.2.5.1 empfängt eine cpmkreatequeryout-Antwort

Wenn der Client eine cpmanatequeryout-Nachrichten Antwort vom Server empfängt, muss der Client den \_ Status zurückgeben und (wenn der Status erfolgreich ist) den Cursor Werte zurück auf eine höhere Ebene zurücksetzen. Alle weiteren Aktionen befinden sich auf der höheren Ebene.

Wenn die höhere Ebene die Abfrage Struktur kennt, wird immer erwartet, dass die richtige Anzahl von Cursor Handles in der cpmkreateoueryout-Nachricht zurückgegeben wird. Die Cursor Zieh Punkte werden in der folgenden Reihenfolge zurückgegeben: das erste Handle ist das unformatierte Rowset, das zweite ist das erste unterteilte Rowset (das die Gruppierung der Ergebnisse auf der Grundlage der ersten Kategorie ist, die im Feld "kategorizationset" der cpmkreatequeryin-Nachricht angegeben ist).

Für informative Zwecke wird erwartet, dass höhere Ebenen die folgenden Aktionen ausführen können. Diese werden jedoch nicht vom CISP-Client erzwungen:

-   Verwenden Sie cpmsetbindingsin, um Bindungen für einzelne Spalten festzulegen, und führen Sie nachfolgende Aktionen für den Abfrage Pfad aus.
-   Verwenden Sie cpmgetquerystatusin, um den Ausführungs Fortschritt einer Abfrage zu überprüfen.
-   Verwenden Sie cpmratiofinishedin, um den Abschluss Prozentsatz der Abfrage anzufordern.

### <a name="3252-receiving-a-cpmgetrowsout-response"></a>3.2.5.2 empfangen einer cpmgetrowsout-Antwort

Wenn der Client eine cpmgetrowsout-Nachrichten Antwort vom Server empfängt, muss der Client die folgenden Schritte ausführen:

-   Überprüfen Sie, ob das \_ Feld Status in der Kopfzeile Erfolg oder Fehler anzeigt.
-   Wenn der \_ Statuswert \_ \_ zu \_ klein ist (0xc0000023), muss der Client den Status der letzten gesendeten Nachricht überprüfen. Wenn keine cpmgetrowsin-Nachricht enthalten ist, muss die empfangene Nachricht automatisch ignoriert werden. Andernfalls muss der Client eine neue cpmgetrowsin-Nachricht an den Server senden, wobei alle Felder identisch mit der gespeicherten Nachricht sind, mit dem Unterschied, dass der \_ cbread-Puffer um 512 (aber nicht größer als 0x4000) erweitert werden muss. Wenn \_ der Status Status \_ Puffer \_ zu \_ klein ist (0xc0000023) und die letzte gesendete Nachricht bereits \_ den Wert 0x4000 hat, muss der Client den Fehler auf der höheren Ebene melden.
-   Wenn der \_ Statuswert ein anderer Fehlerwert ist, muss der Client den Fehler auf die höhere Ebene angeben.
-   Wenn der \_ Statuswert Erfolg anzeigt, müssen die Ergebnisse bis zu der höheren Ebene angezeigt werden, die die Informationen anfordert, und weitere Aktionen befinden sich auf der höheren Ebene.

Für informative Zwecke wird erwartet, dass höhere Ebenen in der Regel die folgenden Aktionen ausführen. Diese werden jedoch nicht vom Dienst Protokoll Client für die Inhalts Indizierung erzwungen:

-   Wenn die Werte in Zeilen die Dokument-IDs darstellen, speichert Kapitel oder Lesezeichen die höhere Ebene in der Regel für die Verwendung in nachfolgenden Vorgängen, die gültige Dokument-IDs, Kapitel oder Lesezeichen Handles einschließen.
-   Die höhere Ebene speichert oder verwendet normalerweise die Daten von Zeilen Werten.
-   Bei Werten, die als verzögerte höhere Ebene gekennzeichnet waren, wird der Wert mithilfe von cpmfetchvaluein-Nachrichten abgerufen.
-   Die Such Beschreibung wird ebenfalls an eine höhere Ebene zurückgegeben und kann von der höheren Ebene wieder verwendet oder überprüft werden.

Wenn die höhere Ebene für informative Zwecke Handles für Kapitel und Lesezeichen angefordert hat, die in den Zeilen empfangen wurden, kann es folgende Aktionen ausführen:

-   Verwenden Sie cpmgetquerystatusexin, um den Ausführungs Status einer Abfrage sowie weitere Statusinformationen (z. b. die Anzahl der gefilterten Dokumente, die verbleibenden Dokumente, die zu filternden Dokumente, das Verhältnis der von der Abfrage verarbeiteten Dokumente, die Gesamtanzahl der Zeilen in der Abfrage und die Position des Lesezeichens im Rowset) zu überprüfen.
-   Verwenden Sie cpmgetnotify, um anzufordern, dass der Server den Client über Rowsetänderungen benachrichtigt.
-   Verwenden Sie cpmgetapproximatepositionin, um die ungefähre Position eines Lesezeichens in einem Kapitel anzufordern.
-   Verwenden Sie cpmcomparebmkin, um einen Vergleich zweier Lesezeichen in einem Kapitel anzufordern.
-   Verwenden Sie cpmrestartpositionin zum Server, um die Position des Cursors auf den Anfang des Rowsets zu ändern.

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a>3.2.5.3 empfängt eine cpmfetchvalueout-Antwort

Wenn der Client eine cpmgetrowsout-Nachrichten Antwort vom Server empfängt, muss der Client die folgenden Schritte ausführen:

-   Überprüfen Sie, ob das \_ Feld Status in der Kopfzeile Erfolg oder Fehler anzeigt. Benachrichtigen Sie bei einem Fehler die höhere Ebene. Andernfalls fahren Sie mit fort.
-   Überprüfen Sie \_ fvalueexist, und wenn Sie auf 0x00000000 festgelegt ist, Benachrichtigen Sie die höhere Ebene, dass der Wert nicht gefunden wurde.
-   Fügen Sie andernfalls \_ cbValue-Bytes aus vValue an den aktuellen Eigenschafts Wert an.
-   Wenn \_ \_ fmoreist auf 0x00000001 festgelegt ist, erhöhen \_ Sie die aktuellen bytes, die von \_ cbValue empfangen werden, und senden Sie eine cpmfetchvaluein-Nachricht an den Server \_ . Legen Sie cbsofar auf den Wert der empfangenen aktuellen bytes, \_ cbpropspec auf NULL und \_ cbblock auf die Puffergröße fest, die von der höheren Ebene gewünscht wird.
-   Wenn \_ fmoreist auf 0x00000000 festgelegt ist, geben Sie den Eigenschafts Wert des aktuellen Eigenschafts Werts auf die höhere Ebene an.

### <a name="3254-receiving-a-cpmfreecursorout-response"></a>3.2.5.4 empfängt eine cpmfreecursorout-Antwort

Wenn der Client eine erfolgreiche cpmfreecursorout-Nachrichten Antwort vom Server empfängt, muss der Client den \_ Wert "ccursor Rest" an die höhere Ebene zurückgeben.

Die folgenden Informationen werden nur für informative Zwecke angegeben und vom CISP-Client nicht erzwungen. Die höhere Ebene wird erwartet, dass Cursor Zieh Punkte nachverfolgt und nicht verwendet werden, die bereits freigegeben wurden. Sobald die Anzahl der \_ ccurrsors gleich 0x00000000 ist, kann die höhere Ebene die Verbindung verwenden, um eine andere Abfrage anzugeben (mithilfe einer cpmkreatequeryin-Nachricht).

### <a name="326-timer-events"></a>3.2.6-Timer-Ereignisse

Keine.

### <a name="327-other-local-events"></a>3.2.7 andere lokale Ereignisse

Keine.

## <a name="4-protocol-examples"></a>4 Beispiele für Protokolle

-   [4,1 Beispiel 1](#41-example-1)
-   [4,2 Beispiel 2](#42-example-2)

### <a name="41-example-1"></a>4,1 Beispiel 1

Im folgenden Beispiel wird ein Szenario betrachtet, bei dem der Benutzer John auf Computer a die Größe der Dateien abrufen möchte, die das Wort "Microsoft" aus dem Satz von Dokumenten enthalten, die auf Server X im Katalog System gespeichert sind. Nehmen wir an, dass auf Computer a ein 32-Bit-Betriebssystem unter Windows XP ausgeführt wird und auf dem Computer X ein 32-Bit Windows Server 2003-Betriebssystem ausgeführt wird.

1.  Der Benutzer öffnet eine Suchanwendung und gibt die Suchabfrage ein. Die Anwendung übergibt die Suchabfrage wiederum an den Protokoll Client.
2.  Der Protokoll Client stellt eine Verbindung mit dem Indizierungs Server X her. Der Protokoll Client verwendet die Named Pipe \\ Pipe- \\ ci- \_ Skaden, um eine Verbindung mit dem Server X über SMB herzustellen.
3.  Der Protokoll Client bereitet dann eine cpmconnectin-Nachricht mit den folgenden Werten vor:

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   **\_ msg** wird auf 0x000000c8 festgelegt, was darauf hinweist, dass es sich hierbei um eine cpmconnectin-Nachricht handelt.
    -   der **\_ Status** ist auf 0x00000000 festgelegt.
    -   **\_ ulchecksum** enthält die Prüfsumme, wie in Abschnitt 3.2.4 angegeben.
    -   **\_ ulReserved2** wird auf 0x00000000 festgelegt.

    Der Nachrichtentext wird wie folgt aufgefüllt:

    -   **\_ iclientversion** ist auf 0x00000008 festgelegt und gibt an, dass der Server das Prüfsummen Feld validieren soll.
    -   **\_ fclientisremote** ist auf 0x00000001 festgelegt und zeigt an, dass der Server ein Remote Server ist.
    -   **\_ cbBlob1** wird auf die Größe (in Bytes) der cpropset-, PropertySet1-und PropertySet2-Felder kombiniert.
    -   **\_ cbBlob2** wird auf 0x00000004 festgelegt (d.h. keine zusätzlichen Eigenschaften Sätze).
    -   **MachineName** ist auf festgelegt.
    -   Der **Benutzername** ist auf John festgelegt.
    -   **cpropsets** ist auf 0x00000002 festgelegt.
    -   Das **PropertySet1** -Feld ist vom Typ CDBPropSet. Die CDBPropSet-Struktur, die das Feld "PropertySet1" enthält, wird wie folgt aufgefüllt:
        -   Das Feld " **guidpropset** " ist auf "A9BD1526-6A80-11D0-8C9D-0020AF1D740E" (DBPROPSET \_ fscifrmwrk \_ ext) festgelegt.
        -   **cproperties** -Feld ist auf 0x00000004 festgelegt.
        -   das Feld " **aProp** " ist ein Array von cdbprop-Strukturen.

            Für das **\[ arequi0 \]** -Element:

            -   **PROPID** ist auf 0x00000002 (DBPROP \_ ci- \_ Katalog \_ Name) festgelegt.
            -   **DBPROPOPTIONS** ist auf 0x0000000 festgelegt.
            -   **Dbpropstatus** ist auf 0x00000000 festgelegt.
            -   Für das **ColId** -Element:
                -   **eKind** ist auf 0x00000001 (dbkind \_ GUID \_ PROPID) festgelegt.
                -   **GUID** ist NULL (alle Nullen), was bedeutet, dass der Wert für die Abfrage gilt, nicht nur für eine einzelne Spalte.
                -   " **ulid** " ist auf "0x00000000" festgelegt.
            -   Für das **vValue** -Element:
                -   **VType** ist auf 0x001F (VT \_ LPWSTR) festgelegt.
                -   **vValue** ist auf "System" festgelegt, den Namen des gewünschten Katalogs.

            Für das **\[ arequi1 \]** -Element:

            -   **PROPID** ist auf 0x00000007 (DBPROP \_ ci- \_ Abfragetyp \_ ) festgelegt.
            -   **DBPROPOPTIONS** ist auf 0x0000000 festgelegt.
            -   **Dbpropstatus** ist Set to0x00000000.
            -   Für das **ColId** -Element:
                -   **eKind** ist auf 0x00000001 (dbkind \_ GUID \_ PROPID) festgelegt.
                -   **GUID** ist NULL (alle Nullen), was bedeutet, dass der Wert für die Abfrage gilt, nicht nur für eine einzelne Spalte.
                -   " **ulid** " ist auf "0x00000000" festgelegt.
            -   Für das **vValue** -Element:
                -   **VType** ist auf 0x0003 erfordert (VT \_ I4) festgelegt.
                -   **vValue** ist auf 0x00000000 (cinormal) festgelegt, was bedeutet, dass es sich um eine reguläre Abfrage handelt.

            Für das Element " **\[ arequi2 \]** ":

            -   **PROPID** ist auf 0x00000004 (DBPROP \_ ci- \_ bereichsflags) festgelegt \_ .
            -   **DBPROPOPTIONS** ist auf 0x0000000 festgelegt.
            -   **Dbpropstatus** ist auf 0x00000000 festgelegt.
            -   Für das **ColId** -Element:
                -   **eKind** ist auf 0x00000001 (dbkind \_ GUID \_ PROPID) festgelegt.
                -   **GUID** ist NULL (alle Nullen), was bedeutet, dass der Wert für die Abfrage gilt, nicht nur für eine einzelne Spalte.
                -   " **ulid** " ist auf "0x00000000" festgelegt.
            -   Für das **vValue** -Element:
                -   **VType**: 0x1003 (VT \_ Vector \| VT \_ I4)
                -   **vValue**: 0x00000001/0x00000001 (ein Element mit Wert 1), d.h. Such Unterordner

            Für das Element " **\[ arequi3 \]** ":

            -   **PROPID**: 0x00000003 (DBPROP \_ ci \_ include- \_ Bereiche)
            -   **DBPROPOPTIONS**: 0x0000000
            -   **Dbpropstatus**: 0x00000000
            -   Für das **ColId** -Element:
                -   **eKind** ist auf 0x00000001 (dbkind \_ GUID \_ PROPID) festgelegt.
                -   **GUID** ist NULL (alle Nullen), was bedeutet, dass der Wert für die Abfrage gilt, nicht nur für eine einzelne Spalte.
                -   " **ulid** " ist auf 0x00000000 festgelegt.
            -   Für das **vValue** -Element:
                -   **VType** ist auf 0x101 f (VT \_ Vector \| VT \_ LPWSTR) festgelegt.
                -   **vValue** ist auf 0x00000001/0x00000002/"" festgelegt \\ (ein Element mit einer null-terminierten Zeichenfolge mit 2 Zeichen), d. h. der Stamm Bereich.

    -   Das Feld **PropertySet2** ist vom Typ CDBPropSet.

        Die CDBPropSet-Struktur, die das Feld "PropertySet1" enthält, wird wie folgt aufgefüllt:

        -   **Guidpropset** ist auf AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D festgelegt (DBPROPSET \_ cifrmwrkcore \_ ext).
        -   **cproperties** -Feld ist auf 0x00000001 festgelegt.
        -   Das Feld " **aProp** " ist ein Array von cdbprop-Strukturen.

            Für das **\[ arequi0 \]** -Element:

            -   **PROPID** ist auf 0x00000002 (DBPROP- \_ Computer) festgelegt.
            -   **DBPROPOPTIONS** ist auf 0x0000000 festgelegt.
            -   **Dbpropstatus** ist auf 0x00000000 festgelegt.
            -   Für das **ColId** -Element:
                -   **eKind** ist auf 0x00000001 (dbkind \_ GUID \_ PROPID) festgelegt,
                -   **GUID** ist NULL (alle Nullen), was bedeutet, dass der Wert für die Abfrage gilt, nicht nur für eine einzelne Spalte.
                -   " **ulid** " ist auf "0x00000000" festgelegt.
            -   Für **vValue** -Element:
                -   **VType**: 0x0008 (VT \_ BSTR)
                -   **vValue**: 0x04/"X" (4 Bytes/NULL-terminierte Unicode-Zeichenfolge), d. h. "x", Name eines Servers.

    -   Das **cextpropset** -Feld ist auf 0x00000000 festgelegt.
    -   Das **apropertysets** -Array ist nicht vorhanden.
    -   Je nach Bedarf werden verschiedene Auffüll Felder ausgefüllt. Die Nachricht wird an den Server gesendet.

4.  Der Server überprüft, ob **\_ ulchecksum** korrekt ist, überprüft, ob der Benutzer zum Ausführen dieser Anforderung autorisiert ist, und antwortet mit einer cpmconnectout-Nachricht.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   **\_ msg** wird auf 0x000000c8 festgelegt, was darauf hinweist, dass es sich hierbei um eine cpmconnectout-Nachricht handelt.
    -   der **\_ Status** wird auf 0x0000000 festgelegt, was den Erfolg angibt.
    -   **\_ ulchecksum** ist auf 0 festgelegt.
    -   **\_ ulReserved2** wird auf 0x00000000 festgelegt.

    Der Nachrichtentext wird wie folgt aufgefüllt:

    -   das Feld **\_ Serverversion** ist auf 0x00000007 (32-Bit Windows XP oder 32-Bit Windows Server 2003) festgelegt.
    -   **\_ reservierte** Felder werden mit beliebigen Daten gefüllt.

5.  Der Client bereitet eine cpmkreatequeryin-Nachricht vor.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   **\_ msg** wird auf 0x000000CA festgelegt, was darauf hinweist, dass es sich hierbei um eine cpmkreatequeryin-Nachricht handelt.
    -   der **\_ Status** ist auf 0x00000000 festgelegt.
    -   **\_ ulchecksum** enthält die Prüfsumme, berechnet nach 3.2.5.
    -   **\_ ulReserved2** wird auf 0x00000000 festgelegt.

    Der Nachrichtentext wird wie folgt aufgefüllt:

    -   Das **Größen** Feld ist auf die Größe der restlichen Nachricht festgelegt.
    -   Das Feld " **ccolumnsetpresent** " ist auf "0x01" festgelegt.
    -   Das **ColumnSet** -Feld ist vom Typ "ccolumnset". Die ccolumnset-Struktur, die dieses Feld enthält, wird wie folgt festgelegt:
        -   Das **\_ count** -Feld ist auf 0x00000001 festgelegt, um anzugeben, dass eine Spalte zurückgegeben
        -   Das **Index** Array ist 0x00000000, das den ersten Eintrag in \_ apropspec angibt.
    -   Das Feld " **krestrictionpresent** " ist auf 0x01 festgelegt, um anzugeben, dass das **Einschränkungs** Feld vorhanden
    -   Das **Einschränkungs** Feld ist vom Typ "krestriction" und wird auf Folgendes festgelegt:
        -   **\_ ultype** ist auf 0x00000004 (rtcontent) festgelegt.
        -   **\_ Weight** ist auf 0x00000000 festgelegt.
    -   Der Rest des Felds enthält eine Ccontent-Einschränkungs Struktur:
        -   Die **\_ Eigenschaft** ist auf GUID B725F130-47EF-101A-A5F1-02608c9eebac/0x00000001 (für prspec \_ PROPID)/0x13 festgelegt, die den Dokument Text darstellt.
        -   **\_ CC** ist auf 0x00000009 festgelegt.
        -   **\_ pwcspphrase** ist auf die Zeichenfolge "Microsoft" festgelegt.
        -   **\_ LCID** ist auf 0x409 (für Englisch) festgelegt.
        -   **\_ ulgeneratemethod** ist auf 0x00000000 (exakte Entsprechung) festgelegt.
    -   **Csortpresent** ist auf 0x00 festgelegt.
    -   " **Ccategorizationsetpresent** " ist auf "0x00" festgelegt.
    -   **Rowsetproperties** wird wie folgt festgelegt:
        -   **\_ ubooleanoptions** ist auf 0x00000001 (sequenziell) festgelegt.
        -   **\_ ulmaxopenrows** ist auf 0x00000000 festgelegt.
        -   **\_ ulmemoryusage** ist auf 0x00000000 festgelegt.
        -   \_**cmaxresults** ist auf 0x00000100 festgelegt (gibt höchstens 256 Zeilen zurück).
        -   **\_ ccmdtimeout** ist auf 0x00000000 (nie Timeout) festgelegt.
    -   **Pidmapper** ist auf Folgendes festgelegt:
        -   **\_ count** ist auf 0x00000001 festgelegt.
        -   **\_ apropspec** ist auf GUID B725F130-47ef-101 a-A5-F1-02608c9eebac/0x00000001 (für prspec \_ PROPID)/0x0000000c festgelegt, das die Windows-Dateigrößen Eigenschaft darstellt.

6.  Der Server verarbeitet ihn und antwortet mit einer cpmkreatequeryout-Nachricht.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   **\_ msg** wird auf 0x000000CA festgelegt, was darauf hinweist, dass es sich hierbei um eine cpmkreatequeryout-Nachricht handelt.
    -   der **\_ Status** ist auf "erfolgreich" festgelegt.
    -   **\_ ulchecksum** ist auf 0x00000000 (oder einen beliebigen anderen beliebigen Wert) festgelegt.
    -   **\_ ulReserved2** wird auf 0x00000000 (oder einen beliebigen anderen beliebigen Wert) festgelegt.

    Der Nachrichtentext wird wie folgt aufgefüllt:

    -   **\_ ftrueseqeuntial** ist auf 0x00000000 festgelegt und zeigt an, dass die Abfrage einen Index verwenden kann.
    -   **\_ fworkidunique** ist auf 0x00000001 festgelegt.
    -   Das **acursors** -Array enthält nur ein-Element, das ein Cursor Handle für diese Abfrage darstellt. Der Wert hängt vom Status des Servers ab. Nehmen wir an, dass der zurückgegebene Wert 0xaaaaaaaa ist.

7.  Der Client gibt eine cpmsetbindingsin-Anforderungs Nachricht aus, um das Format einer Zeile zu definieren.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   die Meldung wird auf 0x000000d0 festgelegt, was darauf hinweist, dass es sich hierbei um eine cpmsetbindingsin- **\_ Nachricht handelt.**
    -   der **\_ Status** ist auf "erfolgreich" festgelegt.
    -   **\_ ulchecksum** ist auf 0x00000000 (oder einen beliebigen anderen beliebigen Wert) festgelegt.
    -   **\_ ulReserved2** wird auf 0x00000000 (oder einen beliebigen anderen beliebigen Wert) festgelegt.

    Der Nachrichtentext wird wie folgt aufgefüllt:

    -   **\_ hcursor** ist auf 0xaaaaaaaa festgelegt.
    -   **\_ cbrow** ist auf 0x10 (groß genug für Spalten) festgelegt.
    -   " **\_ cbbindingdesc** " wird auf die Größe der **\_ CColumns** -und **\_ acolenns** -Felder kombiniert.
    -   **\_ CColumns** ist auf 0x00000001 festgelegt.
    -   Das **\_ acolumns** -Array ist auf eine ctablecolumn-Struktur mit folgenden Werten festgelegt:
    -   -   **\_ PROPSPEC** ist auf GUID b725f130-47ef-101 a-A5-F1-02608c9eebac/0x00000001 (für prspec \_ PROPID)/0x0000000c festgelegt, das die Windows-Dateigrößen Eigenschaft darstellt.
        -   **\_ VType** ist auf 0x0015 (VT \_ UI8) festgelegt.
        -   **\_ Valueused** ist auf 0x01 festgelegt (Spalte in Zeile übertragen).
        -   **\_ Valueoffset** ist auf 0x0002 (am Anfang der Zeile) festgelegt.
        -   **\_ Valuesize** ist auf 0x08 (Größe eines VT- \_ UI8) festgelegt.
        -   **\_ Status** wird auf 0x01 festgelegt.
        -   " **\_ Status-ffset** " ist auf "0x0A" festgelegt.
        -   Die **\_ Längen Verwendung** wird auf 0x00 festgelegt.

8.  Der Server verarbeitet ihn und antwortet mit einer cpmsetbindingsin-Nachricht.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   die **\_ Meldung wird auf** 0x000000d0 festgelegt.
    -   der **\_ Status** ist auf "erfolgreich" festgelegt.
    -   **\_ ulchecksum** ist auf 0x00000000 (oder einen beliebigen anderen beliebigen Wert) festgelegt.
    -   **\_ ulReserved2** wird auf 0x00000000 (oder einen beliebigen anderen beliebigen Wert) festgelegt.

9.  Der Client gibt eine cpmgetrowsin-Anforderungs Nachricht aus. Nehmen wir an, dass der Client auf die Annahme von 100 Zeilen an dieser Stelle vorbereitet ist und Sie in aufsteigender Reihenfolge anfordert.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   die Meldung wird auf 0x000000cc festgelegt, was darauf hinweist, dass es sich um eine cpmgetrowsin- **\_ Nachricht handelt.**
    -   der **\_ Status** ist auf 0x00000000 festgelegt.
    -   **\_ ulchecksum** enthält die Prüfsumme, berechnet gemäß Abschnitt 0.
    -   **\_ ulReserved2** wird auf 0x00000000 festgelegt.

    Der Nachrichtentext wird wie folgt aufgefüllt:

    -   **\_ hcursor** ist auf 0xaaaaaaaa festgelegt.
    -   **\_ crowstotransfer** ist auf 0x00000064 festgelegt.
    -   **\_ crowwidth** ist auf 0x00000010 (aus Bindungen) festgelegt.
    -   **\_ cbseek** ist auf 0x14 festgelegt, d. h. die Größe der ETYPE \_ -, chapt-und crowseeknext-Felder kombiniert.
    -   **\_ cbreserved** ist auf 0x18 (0x14 Plus \_ cbseek) festgelegt.
    -   **\_ cbreadbuffer** ist auf 0x800 (0x64 \* 0x10 aufgerundet auf das nächste Vielfache von 0x200) festgelegt.
    -   **\_ ulclientbase** ist auf 0x00000000 festgelegt.
    -   **\_ fbwdfetch** ist auf 0x00000000 festgelegt, um anzugeben, dass die Zeilen in der Reihenfolge abgerufen werden sollen.
    -   **ETYPE** ist auf 0x0000001 festgelegt, um anzugeben, dass der Client nächste Zeilen anfordert.
    -   " **\_ chapt** " wird auf 0 (kein in Kapitel unterteilt) festgelegt.
    -   **Seekdescription** ist auf crowseeknext festgelegt. Die crowseeknext-Struktur enthält die folgenden Werte:
        -   **Citblchapt** ist auf 0x00000000 festgelegt.
        -   **\_ hregion** ist auf 0x00000000 festgelegt.
        -   **\_ cskip** ist auf 0 festgelegt, um anzugeben, dass der Client keine Zeilen auslassen möchte.

10. Der Server verarbeitet ihn und antwortet mit einer cpmgetrowsout-Nachricht. Nehmen wir an, dass der Server 100 Dokumente gefunden hat, die das Wort "Microsoft" enthalten.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   die Meldung wird auf 0x000000cc festgelegt, was darauf hinweist, dass es sich um eine cpmgetrowsout- **\_ Nachricht handelt.**
    -   der **\_ Status** ist auf "erfolgreich" festgelegt.
    -   **\_ ulchecksum** ist auf 0x00000000 festgelegt.
    -   **\_ ulReserved2** wird auf 0x00000000 festgelegt.

    Der Nachrichtentext wird wie folgt aufgefüllt:

    -   **\_ Crowszurück gegeben** ist auf 0x00000064 festgelegt.
    -   **ETYPE** ist auf 0x00000001 festgelegt.
    -   " **\_ chapt** " ist auf "0x00000000" (kein in Kapitel unterteilt) festgelegt.
    -   **Seekdescription** enthält eine crowseeknext-Struktur, die wie folgt aufgefüllt wird:
        -   **Citblchapt** ist auf 0x00000000 festgelegt.
        -   **\_ hregion** ist auf 0x00000000 festgelegt.
        -   **\_ cskip** ist auf 0 festgelegt, um anzugeben, dass der Client keine Zeilen auslassen möchte.
    -   **Zeilen** enthalten die Größe der 100-Dokumente, die das Wort "Microsoft" enthalten. Da es sich hierbei um Daten mit fester Größe handelt, wird Sie einfach als Liste von 100, 8-Byte-Ganzzahlen ohne Vorzeichen strukturiert.

11. Der Client sendet eine cpmdisconnect-Nachricht, um die Verbindung zu beenden.

    Der Header der Nachricht wird wie folgt aufgefüllt:

    -   **\_ msg** wird auf 0x000000c9 festgelegt, was darauf hinweist, dass es sich um eine cpmdisconnect-Nachricht handelt.
    -   der **\_ Status** ist auf 0x00000000 festgelegt.
    -   **\_ ulchecksum** ist auf 0x00000000 festgelegt.

12. Der Server verarbeitet die Nachricht und entfernt den gesamten Client Zustand.

### <a name="42-example-2"></a>4,2 Beispiel 2

Im vorherigen Beispiel war die Abfrage recht einfach. Lassen Sie uns nun eine etwas komplexere Abfrage in Erwägung gezogen. Nehmen wir an, dass der Benutzer die Größe der Dokumente abrufen möchte, die beide die folgenden Wörter enthalten: "Microsoft" und "Office". Dies wird angegeben, indem das Einschränkungs Feld in der in Schritt 5 gesendeten Meldung cpmkreatequeryin wie folgt geändert wird:

Das **Einschränkungs** Feld ist vom Typ "krestriction" und wird auf Folgendes festgelegt:

-   -   **\_ ultype** ist auf 0x00000004 (rtand) festgelegt.
    -   **\_ Weight** ist auf 0x00000000 festgelegt.

Der Rest des Felds enthält eine cnoderestriction-Struktur:

-   -   **\_ CNode** ist auf 0x00000002 festgelegt und gibt an, dass zwei Knoten im panode-Array vorhanden sind.
    -   Das **\_ panode** -Feld ist ein Array aus zwei Struktur Strukturen.

        **\_ panode \[ 0 \]** enthält:

        -   -   **\_ ultype** ist auf 0x00000004 (rtcontent) festgelegt.
            -   **\_ Weight** ist auf 0x00000000 festgelegt.
            -   Der Rest des Felds enthält eine Ccontent-Einschränkungs Struktur:
                -   Die **\_ Eigenschaft** ist auf GUID b725f130-47ef-101A-a5f1-02608c9eebac/0x00000001 (für prspec \_ PROPID)/0x13 festgelegt.
                -   **\_ CC** ist auf 0x00000009 festgelegt.
                -   **\_ pwcspphrase** ist auf die Zeichenfolge "Microsoft" festgelegt.
                -   **\_ LCID** ist auf 0x409 (für Englisch) festgelegt.
                -   **\_ ulgeneratemethod** ist auf 0x00000000 (exakte Entsprechung) festgelegt.

        **\_ panode \[ 1 \]** enthält:

        -   -   **\_ ultype** ist auf 0x00000004 (rtcontent) festgelegt.
            -   **\_ Weight** ist auf 0x00000000 festgelegt.
            -   Der Rest des Felds enthält eine Ccontent-Einschränkungs Struktur:
                -   Die **\_ Eigenschaft** ist auf GUID b725f130-47ef-101A-a5f1-02608c9eebac/0x00000001 (für prspec \_ PROPID)/0x13 festgelegt.
                -   **\_ CC** ist auf 0x00000006 festgelegt.
                -   **\_ pwcspphrase** ist auf die Zeichenfolge "Office" festgelegt.
                -   **\_ LCID** ist auf 0x409 (für Englisch) festgelegt.
                -   **\_ ulgeneratemethod** ist auf 0x00000000 (exakte Entsprechung) festgelegt.

## <a name="5-security"></a>5 Sicherheit

### <a name="51-security-considerations-for-implementers"></a>5.1 Sicherheitsüberlegungen für Ausführende

Indizierung von Implementierungen, bei denen sichere Inhalte indiziert werden, sollte in Erwägung gezogen werden, den von SMB MS-SMB bereitgestellten Benutzer Kontext \[ \] zum Kürzen von Suchergebnissen zu verwenden

### <a name="52-index-of-security-parameters"></a>5.2 Index von Sicherheitsparameter



| Sicherheits Parameter  | `Section` |
|---------------------|---------|
| Ebene des Identitätswechsels | 2.1     |



 

## <a name="6-index-of-version-specific-behavior"></a>6 Index des Versions spezifischen Verhaltens



| Versions spezifisches Verhalten                                                                         | `Section`   | Windows 2000 | Windows XP | Windows Server 2003 |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| Dieses Protokoll ist unter Windows 2000, Windows XP, Windows Server 2003 und Windows Vista implementiert. | 1.3.2     | X            | X          | X                   |
| Anwendungen interagieren in der Regel mit einem OLE DB Schnittstellen Wrapper                                  | 1.4       | X            | X          | X                   |
| NTSTATUS-Werte                                                                                   | 1.8       | X            | X          | X                   |
| Der Client legt das \_ Feld Status in den einzelnen Nachrichten Headern fest.                                        | 2.2.2     | X            | X          | X                   |
| der cpdingscans-Wert ist in der Regel NULL                                                               | 2.2.3.1   | X            | X          | X                   |
| iclientversion-Wert                                                                              | 2.2.3.6   | X            | X          | X                   |
| \_cbchunk-Wert                                                                                   | 2.2.3.19  | X            | X          | X                   |
| 32-Bit-und 64-Bit-Speicheradressen                                                                | 3.2.4.2.4 | X            | X          | X                   |



 

 

 





