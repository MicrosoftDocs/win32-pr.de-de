---
title: Inhaltsindizierungsdienste-Protokoll
description: Dieses Dokument ist eine Spezifikation des Content Indexing Service-Protokolls.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5265d9d8c802b278b4349ef4b8248b068dc7edc4
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492292"
---
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="cc80c-103">Inhaltsindizierungsdienste-Protokoll</span><span class="sxs-lookup"><span data-stu-id="cc80c-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="cc80c-104">Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="cc80c-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="cc80c-105">Verwenden Sie in späteren [Versionen Windows Search.](../search/-search-3x-wds-overview.md)</span><span class="sxs-lookup"><span data-stu-id="cc80c-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="cc80c-106">Protokollspezifikation, Version 0.12</span><span class="sxs-lookup"><span data-stu-id="cc80c-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="cc80c-107">1 Einführung</span><span class="sxs-lookup"><span data-stu-id="cc80c-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="cc80c-108">1.1 Glossar</span><span class="sxs-lookup"><span data-stu-id="cc80c-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="cc80c-109">1.2 Verweise</span><span class="sxs-lookup"><span data-stu-id="cc80c-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="cc80c-110">1.3 Protokollübersicht (Zusammenfassung)</span><span class="sxs-lookup"><span data-stu-id="cc80c-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="cc80c-111">1.4 Beziehung zu anderen Protokollen</span><span class="sxs-lookup"><span data-stu-id="cc80c-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="cc80c-112">1.5 Voraussetzungen und Vorbedingungen</span><span class="sxs-lookup"><span data-stu-id="cc80c-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="cc80c-113">1.6 Anwendbarkeitsanweisung</span><span class="sxs-lookup"><span data-stu-id="cc80c-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="cc80c-114">1.7 Versionsverwaltung und Funktionsübertragung</span><span class="sxs-lookup"><span data-stu-id="cc80c-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="cc80c-115">1.8 Durch Hersteller erweiterbare Felder</span><span class="sxs-lookup"><span data-stu-id="cc80c-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="cc80c-116">1.9 Zuweisungen von Standards</span><span class="sxs-lookup"><span data-stu-id="cc80c-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="cc80c-117">2\. Nachrichten</span><span class="sxs-lookup"><span data-stu-id="cc80c-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="cc80c-118">2.1 Transport</span><span class="sxs-lookup"><span data-stu-id="cc80c-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="cc80c-119">2.2 Nachrichtensyntax</span><span class="sxs-lookup"><span data-stu-id="cc80c-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="cc80c-120">3 Protokolldetails</span><span class="sxs-lookup"><span data-stu-id="cc80c-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="cc80c-121">3.1 Serverdetails</span><span class="sxs-lookup"><span data-stu-id="cc80c-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="cc80c-122">3.2 Clientdetails</span><span class="sxs-lookup"><span data-stu-id="cc80c-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="cc80c-123">4 Beispiele für Protokolle</span><span class="sxs-lookup"><span data-stu-id="cc80c-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="cc80c-124">4.1 Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc80c-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="cc80c-125">4.2 Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cc80c-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="cc80c-126">5 Sicherheit</span><span class="sxs-lookup"><span data-stu-id="cc80c-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="cc80c-127">5.1 Sicherheitsüberlegungen für Ausführende</span><span class="sxs-lookup"><span data-stu-id="cc80c-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="cc80c-128">5.2 Index von Sicherheitsparameter</span><span class="sxs-lookup"><span data-stu-id="cc80c-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="cc80c-129">6 Index des versionsspezifischen Verhaltens</span><span class="sxs-lookup"><span data-stu-id="cc80c-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="cc80c-130">Dieses Dokument ist eine Spezifikation des Content Indexing Service-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="cc80c-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="cc80c-131">Die WSPP-Dokumentation (Workgroup Server Protocol Program) ist für die Verwendung in Verbindung mit dokumentation zu öffentlichen Standards, Netzwerkprogrammierungsart und Konzepten verteilter Windows-Arbeitsgruppensysteme vorgesehen und setzt voraus, dass der Leser entweder mit dem oben genannten Material vertraut ist oder sofortigen Zugriff darauf hat.</span><span class="sxs-lookup"><span data-stu-id="cc80c-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="cc80c-132">Eine WSPP-Protokollspezifikation erfordert nicht die Verwendung von Microsoft-Programmiertools oder -Programmierumgebungen, damit ein Lizenzer eine Implementierung entwickeln kann.</span><span class="sxs-lookup"><span data-stu-id="cc80c-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="cc80c-133">Lizenzlizenzen, die Zugriff auf Microsoft-Programmiertools und -umgebungen haben, können diese nutzen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="cc80c-134">1 Einführung</span><span class="sxs-lookup"><span data-stu-id="cc80c-134">1 Introduction</span></span>

-   [<span data-ttu-id="cc80c-135">1.1 Glossar</span><span class="sxs-lookup"><span data-stu-id="cc80c-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="cc80c-136">1.2 Verweise</span><span class="sxs-lookup"><span data-stu-id="cc80c-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="cc80c-137">1.3 Protokollübersicht (Zusammenfassung)</span><span class="sxs-lookup"><span data-stu-id="cc80c-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="cc80c-138">1.4 Beziehung zu anderen Protokollen</span><span class="sxs-lookup"><span data-stu-id="cc80c-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="cc80c-139">1.5 Voraussetzungen und Vorbedingungen</span><span class="sxs-lookup"><span data-stu-id="cc80c-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="cc80c-140">1.6 Anwendbarkeitsanweisung</span><span class="sxs-lookup"><span data-stu-id="cc80c-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="cc80c-141">1.7 Versionsverwaltung und Funktionsübertragung</span><span class="sxs-lookup"><span data-stu-id="cc80c-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="cc80c-142">1.8 Durch Hersteller erweiterbare Felder</span><span class="sxs-lookup"><span data-stu-id="cc80c-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="cc80c-143">1.9 Zuweisungen von Standards</span><span class="sxs-lookup"><span data-stu-id="cc80c-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="cc80c-144">1.1 Glossar</span><span class="sxs-lookup"><span data-stu-id="cc80c-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="cc80c-145">Die folgenden Begriffe werden im Glossarabschnitt von \[ MS-SYS \] definiert:</span><span class="sxs-lookup"><span data-stu-id="cc80c-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="cc80c-146">GUID</span><span class="sxs-lookup"><span data-stu-id="cc80c-146">GUID</span></span>
> -   <span data-ttu-id="cc80c-147">Little Endian</span><span class="sxs-lookup"><span data-stu-id="cc80c-147">Little Endian</span></span>
> -   <span data-ttu-id="cc80c-148">Named Pipe</span><span class="sxs-lookup"><span data-stu-id="cc80c-148">Named Pipe</span></span>
> -   <span data-ttu-id="cc80c-149">`Path`</span><span class="sxs-lookup"><span data-stu-id="cc80c-149">Path</span></span>

 

<span data-ttu-id="cc80c-150">**Bindung:** Eine Anforderung zum Einschließen einer bestimmten **Spalte** in ein zurückgegebenes **Rowset.**</span><span class="sxs-lookup"><span data-stu-id="cc80c-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="cc80c-151">Die **Bindung** gibt eine Eigenschaft an, die in die Suchergebnisse aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="cc80c-152">**Lesezeichen:** Ein Marker, der eine Zeile innerhalb einer Gruppe von Zeilen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="cc80c-153">**Catalog:** Die Organisationseinheit auf oberster Ebene im Indizierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="cc80c-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="cc80c-154">Es stellt eine Reihe indizierter Dokumente dar, für die Abfragen mithilfe des Content Indexing Service-Protokolls ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="cc80c-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="cc80c-155">**Kategorie:** Eine hierarchische Gruppierung von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="cc80c-156">Beispielsweise kann ein Abfrageergebnis, das Spalten für Autor und Titel enthält, basierend auf dem Autor kategorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="cc80c-157">Jede Gruppe von Zeilen, die denselben Wert für author enthält, würde eine Kategorie darstellen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="cc80c-158">**Kapitel:** Ein **Zeilenbereich** innerhalb einer Gruppe von **Zeilen.**</span><span class="sxs-lookup"><span data-stu-id="cc80c-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="cc80c-159">**Spalte:** Der Container für einen einzelnen Informationstyp in einer **Zeile.**</span><span class="sxs-lookup"><span data-stu-id="cc80c-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="cc80c-160">Spalten werden Eigenschaftennamen zugeordnet und geben an, welche  Eigenschaften für die **Befehlsstrukturelemente** der Suchabfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="cc80c-161">**Befehlsstruktur:** Eine Kombination aus **Einschränkungen,** **Kategorien** und **Sortierreihenfolgen,** die für die Suchabfrage angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="cc80c-162">**Cursor:** Eine Entität, die als Mechanismus zum Arbeiten mit jeweils einer **Zeile** oder einem kleinen **Zeilenblock** in einem Satz von Daten verwendet wird, die in einem Resultset zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="cc80c-163">Ein **Cursor** wird in einer einzelnen **Zeile** im Resultset positioniert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="cc80c-164">Nachdem der **Cursor** in einer Zeile positioniert wurde, können Vorgänge für diese **Zeile** oder für einen **Zeilenblock** ausgeführt werden, der an dieser Position beginnt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="cc80c-165">**Handle:** Ein Token, das verwendet werden kann, um **Cursor,** **Kapitel** und **Lesezeichen** zu identifizieren und darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="cc80c-166">**Index:** Eine persistente Struktur, die den Textinhalt enthält, der von einem **Indizierungsdienst** aus Dateien abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="cc80c-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="cc80c-167">Dies schließt die Liste der Wörter ein, die zusammen mit dem enthaltenden Dateinamen, der Wortposition und dem **Gebietsschema** gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="cc80c-168">**Indizierung:** Der Prozess, bei dem Text und Eigenschaften aus Dateien extrahiert und die extrahierten Werte in den Indizes **(für** Text) und im Eigenschaftencache **(für** Eigenschaften) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="cc80c-169">**Indizierungsdienst:** Ein Dienst, der indizierte **Kataloge** für den Inhalt und die Eigenschaften von Dateisystemen erstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="cc80c-170">Anwendungen können die Kataloge nach Informationen aus den Dateien im indizierten Dateisystem durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="cc80c-171">**Locale**: Ein Bezeichner, wie in \[ MS-GPSI Anhang A angegeben, der Einstellungen \] im Zusammenhang mit der Sprache angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="cc80c-172">Diese Einstellungen geben an, wie Datums- und Zeitangaben formatiert, Elemente alphabetisch sortiert, Zeichenfolgen verglichen werden sollen, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="cc80c-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="cc80c-173">**Abfrage in natürlicher Sprache:** Eine Abfrage, die mit menschlicher Sprache anstelle der Abfragesyntax erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="cc80c-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="cc80c-174">**Rauschwort:** Ein Wort, das vom Indizierungsdienst  ignoriert wird, wenn es in den für die Suchabfrage angegebenen Einschränkungen vorhanden ist, da es nur einen geringen wertwert hat.</span><span class="sxs-lookup"><span data-stu-id="cc80c-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="cc80c-175">Beispiele für Englisch sind "a", "and" und "the".</span><span class="sxs-lookup"><span data-stu-id="cc80c-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="cc80c-176">**Eigenschaftencache:** Ein Cache von Dateieigenschaften, die von einem **Indizierungsdienst extrahiert wurden.**</span><span class="sxs-lookup"><span data-stu-id="cc80c-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="cc80c-177">**Eigenschaftenindizierung:** Der Prozess  zum  Erstellen eines Indexes von Werttypeigenschaften eines Dokuments, einschließlich Autor, Betreff, Typ, Wortanzahl, Anzahl gedruckter Seiten und anderer Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cc80c-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="cc80c-178">**Einschränkung:** Eine Reihe von Bedingungen, die eine Datei erfüllen muss, um in die Suchergebnisse aufgenommen zu werden, die vom Indizierungsdienst **als** Reaktion auf eine Suchabfrage zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="cc80c-179">Eine **Einschränkung** schränkt den Fokus einer Suchabfrage  ein und beschränkt die Dateien, die der Indizierungsdienst in die Suchergebnisse einfing, auf dieJenigen, die den Bedingungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="cc80c-180">**Row**: Die Auflistung von Spalten **mit** den Eigenschaftswerten, die eine  einzelne Datei aus dem Satz von Dateien beschreiben, die den Einschränkungen in der an den Indizierungsdienst übermittelten Suchabfrage **entsprechen.**</span><span class="sxs-lookup"><span data-stu-id="cc80c-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="cc80c-181">**Rowset:** Eine Reihe von **Zeilen, die** in den Suchergebnissen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="cc80c-182">**Sortierreihenfolge:** Der Satz von Regeln in einer Suchabfrage, die die Reihenfolge der Zeilen im Suchergebnis definieren.</span><span class="sxs-lookup"><span data-stu-id="cc80c-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="cc80c-183">Jede Regel besteht aus einer Eigenschaft (Name, Größe usw.) und einer Richtung für die Reihenfolge (aufsteigend oder absteigend).</span><span class="sxs-lookup"><span data-stu-id="cc80c-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="cc80c-184">Mehrere Regeln werden sequenziell angewendet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="cc80c-185">**Texttypeigenschaft:** Eine Eigenschaft, die den Inhalt eines Dokuments beschreibt und dem Namen nur unformatierten Text zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="cc80c-186">**Value-type Property**: Eine Eigenschaft, die ein einzelnes Attribut eines gesamten Dokuments beschreibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="cc80c-187">Eine Werttypeigenschaft verfügt über eine Datentyp-ID und einen Wert dieses Datentyps, der dem Namen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="cc80c-188">**Virtueller Stamm:** Ein alternativer Pfad zu einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="cc80c-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="cc80c-189">Ein physischer Ordner kann 0 (null) oder mehr virtuelle Stammordner enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="cc80c-190">Pfade, die mit einem virtuellen Stamm beginnen, werden als virtuelle Pfade bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="cc80c-191">Beispielsweise kann /server/vanityroot ein virtueller Stamm von C: \\ \\ IIS-Webordner1 \\ sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="cc80c-192">Dann würde die Datei C: \\ IIS \\ web \\ folder1 \\default.htm den virtuellen Pfad /server/vanityroot/default.htm aufweisen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="cc80c-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT:** Diese Begriffe (in allen Obergrenzen) werden wie in \[ RFC2119 beschrieben \] verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="cc80c-194">Alle Aussagen zu optionalem Verhalten enthalten die Worte KÖNNEN, SOLLTEN oder SOLLTEN NICHT.</span><span class="sxs-lookup"><span data-stu-id="cc80c-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="cc80c-195">1.2 Verweise</span><span class="sxs-lookup"><span data-stu-id="cc80c-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="cc80c-196">1.2.1 Normative Verweise</span><span class="sxs-lookup"><span data-stu-id="cc80c-196">1.2.1 Normative References</span></span>

<span data-ttu-id="cc80c-197">\[IEEE754 \] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="cc80c-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="cc80c-198">\[MS-DCOM \] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", Juni 2006.</span><span class="sxs-lookup"><span data-stu-id="cc80c-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="cc80c-199">\[MS-GPSI \] Microsoft Corporation, "Gruppenrichtlinie für die Softwareinstallation Extension", Juni 2006.</span><span class="sxs-lookup"><span data-stu-id="cc80c-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="cc80c-200">\[MS-SMB \] Microsoft Corporation, "Microsoft Server Message Block (SMB)-Protokoll und -Erweiterungen", Mai 2006.</span><span class="sxs-lookup"><span data-stu-id="cc80c-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="cc80c-201">\[MS-SYS \] Microsoft Corporation, "Systemübersicht v4", Juli 2006.</span><span class="sxs-lookup"><span data-stu-id="cc80c-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="cc80c-202">\[SALTON \] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span><span class="sxs-lookup"><span data-stu-id="cc80c-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="cc80c-203">\[UNICODE \] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="cc80c-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="cc80c-204">1.2.2 Informative Verweise</span><span class="sxs-lookup"><span data-stu-id="cc80c-204">1.2.2 Informative References</span></span>

<span data-ttu-id="cc80c-205">\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .</span><span class="sxs-lookup"><span data-stu-id="cc80c-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="cc80c-206">\[MSDN-QUERYERR \] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="cc80c-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="cc80c-207">1.3 Protokollübersicht (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="cc80c-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="cc80c-208">Ein **Inhaltsindizierungsdienst hilft** dabei, die extrahierten Features einer Sammlung von Dokumenten effizient zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="cc80c-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="cc80c-209">Das Content Indexing Service-Protokoll (CISP) ermöglicht einem Client die Kommunikation mit einem Server, der einen Indizierungsdienst hosten, um Abfragen aus senden zu können, und einem Administrator die Verwaltung des Indizierungsservers zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="cc80c-210">Bei der Verarbeitung von Dateien analysiert ein Indizierungsdienst eine Reihe von Dokumenten  und organisiert ihren Inhalt so neu, dass Eigenschaften dieser Dokumente effizient als Reaktion auf Abfragen zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="cc80c-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="cc80c-211">Eine Auflistung von Dokumenten, die abgefragt werden können, umfasst einen **Katalog.**</span><span class="sxs-lookup"><span data-stu-id="cc80c-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="cc80c-212">Ein Katalog kann einen **Index** (für die Kurzreferenz zu Text) und einen Eigenschaftencache **(zum** schnellen Abrufen von Eigenschaftswerten) enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="cc80c-213">Konzeptionell besteht ein Katalog aus einer logischen "Tabelle" von Eigenschaften mit dem Text oder Wert und dem entsprechenden **In** spalten der Tabelle gespeicherten Locale.</span><span class="sxs-lookup"><span data-stu-id="cc80c-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="cc80c-214">Jede "Zeile" der Tabelle entspricht einem separaten Dokument im Gültigkeitsbereich des Katalogs, und jede "Spalte" der Tabelle entspricht einer -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cc80c-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="cc80c-215">Die spezifischen Aufgaben, die von CISP ausgeführt werden, werden in zwei Funktionsbereiche eingekreist:</span><span class="sxs-lookup"><span data-stu-id="cc80c-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="cc80c-216">Remoteverwaltung von Indizierungsdienstkatalogen,</span><span class="sxs-lookup"><span data-stu-id="cc80c-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="cc80c-217">Remoteabfragen von Indizierungsdienstkatalogen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="cc80c-218">1.3.1 Remoteverwaltungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="cc80c-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="cc80c-219">CISP ermöglicht die folgenden Indizierungsdienst-Katalogverwaltungsaufgaben von einem Client aus:</span><span class="sxs-lookup"><span data-stu-id="cc80c-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="cc80c-220">Fragen Sie den aktuellen Status eines Indizierungsdienstkatalogs auf dem Server ab.</span><span class="sxs-lookup"><span data-stu-id="cc80c-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="cc80c-221">Aktualisiert den Status eines Indizierungsdienstkatalogs.</span><span class="sxs-lookup"><span data-stu-id="cc80c-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="cc80c-222">Starten Sie den Indizierungsprozess für einen bestimmten Satz von Dateien.</span><span class="sxs-lookup"><span data-stu-id="cc80c-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="cc80c-223">Initiieren Sie die Optimierung eines Indexes, um die Abfrageleistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="cc80c-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="cc80c-224">Alle Remoteverwaltungsaufgaben folgen einem einfachen Anforderungs-/Antwortmodell.</span><span class="sxs-lookup"><span data-stu-id="cc80c-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="cc80c-225">Auf dem Client wird kein Zustand für jeden Verwaltungsaufruf beibehalten, und Verwaltungsaufrufe können in beliebiger Reihenfolge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="cc80c-226">1.3.2 Remoteabfragen</span><span class="sxs-lookup"><span data-stu-id="cc80c-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="cc80c-227">CISP ermöglicht Clients das Ausführen von Suchabfragen für einen Remoteserver, der einen Indizierungsdienst hostet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="cc80c-228">Das Senden einer Suchabfrage ist ein mehrstufiger Prozess, der vom Client initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="cc80c-229">Die Schritte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="cc80c-230">Der Client fordert eine Verbindung mit einem Server an, der einen Indizierungsdienst hostet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="cc80c-231">Der Client sendet die Parameter für die Suchabfrage, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="cc80c-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="cc80c-232">Die **Einschränkungen,** mit denen angegeben wird, welche Dokumente in die Suchergebnisse aufgenommen bzw. aus diesen ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="cc80c-233">Die Reihenfolge, in der die Suchergebnisse zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="cc80c-234">Die Spalten, die im Resultset zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="cc80c-235">Die maximale Anzahl von **Zeilen,** die für die Abfrage zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="cc80c-236">Die maximale Zeit für die Abfrageausführung.</span><span class="sxs-lookup"><span data-stu-id="cc80c-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="cc80c-237">Nachdem der Server die Anforderung des Clients zum Initiieren der Abfrage bestätigt hat, kann der Client Statusinformationen zur Abfrage anfordern, dies ist jedoch kein erforderlicher Schritt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="cc80c-238">Der Client gibt dann an, welche Eigenschaften der Server in die Suchergebnisse aufnehmen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="cc80c-239">Der Client fordert ein Resultset vom Server an, und der Server antwortet, indem er dem Client die Eigenschaftswerte für Dateien sendet, die in den Ergebnissen für die Suchabfrage des Clients enthalten waren.</span><span class="sxs-lookup"><span data-stu-id="cc80c-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="cc80c-240">Wenn der Wert einer Eigenschaft zu groß ist, um in einen einzelnen Antwortpuffer zu passen, sendet der Server die Eigenschaft nicht, sondern legt den Eigenschaftsstatus auf verzögert fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="cc80c-241">Der Client fordert den Eigenschaftswert dann separat mithilfe einer Reihe von Anforderungen für aufeinander folgende Blöcke des Werts an und setzt dann die Anforderung anderer Werte fort.</span><span class="sxs-lookup"><span data-stu-id="cc80c-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="cc80c-242">Sobald der Client mit der Suchabfrage fertig ist und keine zusätzlichen Ergebnisse mehr benötigt, kontaktiert der Client den Server, um die Abfrage freizugeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="cc80c-243">Nachdem der Server die Abfrage freigegeben hat, kann der Client eine Anforderung senden, um die Verbindung mit dem Server zu trennen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="cc80c-244">Die Verbindung wird dann geschlossen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-244">The connection is then closed.</span></span> <span data-ttu-id="cc80c-245">Alternativ kann der Client eine weitere Abfrage ausführen und die Sequenz aus Schritt 2 wiederholen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="cc80c-246">Windows-Verhalten: Dieses Protokoll ist unter Windows 2000, Windows XP, Windows Server 2003 und Windows Vista implementiert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="cc80c-247">1.4 Beziehung zu anderen Protokollen</span><span class="sxs-lookup"><span data-stu-id="cc80c-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="cc80c-248">Der CISP verwendet das SMB \[ MS-SMB-Protokoll \] für den Nachrichtentransport.</span><span class="sxs-lookup"><span data-stu-id="cc80c-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="cc80c-249">Kein anderes Protokoll hängt direkt vom Content Indexing Service-Protokoll ab.</span><span class="sxs-lookup"><span data-stu-id="cc80c-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="cc80c-250">*Windows-Verhalten: Anwendungen interagieren in der Regel mit einem OLE DB-Schnittstellenwrapper \[ MSDN-OLEDB (z. B. einem Protokollclient) und nicht direkt \] mit dem Protokoll.*</span><span class="sxs-lookup"><span data-stu-id="cc80c-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="cc80c-251">1.5 Voraussetzungen und Vorbedingungen</span><span class="sxs-lookup"><span data-stu-id="cc80c-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="cc80c-252">Es wird davon ausgegangen, dass der Client den Namen des Servers und einen Katalognamen erhalten hat, bevor dieses Protokoll aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="cc80c-253">Wie ein Client dies tut, liegt außerhalb des Bereichs dieser Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="cc80c-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="cc80c-254">Es wird auch davon ausgegangen, dass der Client und der Server über eine Sicherheits-Zuordnung verfügen, die mit Named Pipes \[ MS-SMB verwendet werden \] kann.</span><span class="sxs-lookup"><span data-stu-id="cc80c-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="cc80c-255">1.6 Anwendbarkeitsanweisung</span><span class="sxs-lookup"><span data-stu-id="cc80c-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="cc80c-256">CISP ist für das Abfragen und Verwalten von Katalogen auf einem Remoteserver über einen Client konzipiert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="cc80c-257">CISP ist unter Windows Vista veraltet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="cc80c-258">1.7 Versionsverwaltung und Funktionsübertragung</span><span class="sxs-lookup"><span data-stu-id="cc80c-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="cc80c-259">Dieses Protokoll verfügt über keine Mechanismen zur Versions- oder Funktionsaushandlung.</span><span class="sxs-lookup"><span data-stu-id="cc80c-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="cc80c-260">1.8 Durch Hersteller erweiterbare Felder</span><span class="sxs-lookup"><span data-stu-id="cc80c-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="cc80c-261">Dieses Protokoll verwendet HRESULTs, die anbietererweiterbar sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="cc80c-262">Anbieter können ihre eigenen Werte für dieses Feld auswählen, solange das C-Bit (0x20000000) wie in Abschnitt 4.1.1 von MS-SYS angegeben festgelegt ist, was angibt, dass es sich um einen Kundencode \[ \] handelt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="cc80c-263">Dieses Protokoll verwendet auch NTSTATUS-Werte aus dem NTSTATUS-Nummernbereich, der in \[ MS-SYS definiert \] ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="cc80c-264">Anbieter SOLLTEN diese Werte mit ihrer angegebenen Bedeutung wiederverwenden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="cc80c-265">Wenn Sie einen anderen Wert auswählen, besteht das Risiko eines zukünftigen Kollisionsrisikos.</span><span class="sxs-lookup"><span data-stu-id="cc80c-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="cc80c-266">*Windows-Verhalten: Windows verwendet nur die Werte, die in Abschnitt 4.1.3 von \[ MS-SYS angegeben \] sind.*</span><span class="sxs-lookup"><span data-stu-id="cc80c-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="cc80c-267">1.8.1 Eigenschaften-IDs</span><span class="sxs-lookup"><span data-stu-id="cc80c-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="cc80c-268">Eigenschaften werden durch IDs dargestellt, die als Eigenschaften-IDs bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="cc80c-269">Jede Eigenschaft muss einen global eindeutigen Bezeichner haben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="cc80c-270">Dieser Bezeichner besteht aus einer **GUID,** die eine Auflistung von Eigenschaften darstellt, die als Eigenschaftensatz bezeichnet wird, sowie entweder eine Zeichenfolge oder eine 32-Bit-Ganzzahl, um die Eigenschaft innerhalb des Sets zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cc80c-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="cc80c-271">Wenn die ganzzahlige Form der ID verwendet wird, werden die Werte 0x00000000, 0xFFFFFFFF und 0xFFFFFFFE als ungültig betrachtet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="cc80c-272">Anbieter können sicherstellen, dass ihre Eigenschaften eindeutig definiert werden, indem sie sie in einem Eigenschaftensatz platzieren, der durch ihre eigene GUID definiert wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="cc80c-273">1.9 Zuweisungen von Standards</span><span class="sxs-lookup"><span data-stu-id="cc80c-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="cc80c-274">Dieses Protokoll weist keine Standardzuweisungen auf, sondern nur private Zuweisungen, die von Microsoft mithilfe von Zuordnungsverfahren vorgenommen werden, die in anderen Protokollen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="cc80c-275">Microsoft hat diesem Protokoll eine Benannte Pipe zugeordnet, wie in \[ MS-SMB \] angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="cc80c-276">Die Zuweisung ist:</span><span class="sxs-lookup"><span data-stu-id="cc80c-276">The assignment is:</span></span>



| <span data-ttu-id="cc80c-277">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc80c-277">Parameter</span></span> | <span data-ttu-id="cc80c-278">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-278">Value</span></span>             | <span data-ttu-id="cc80c-279">Verweis</span><span class="sxs-lookup"><span data-stu-id="cc80c-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="cc80c-280">Pipename</span><span class="sxs-lookup"><span data-stu-id="cc80c-280">Pipe name</span></span> | <span data-ttu-id="cc80c-281">\\\\ \_ Pipe-CI-SKADS</span><span class="sxs-lookup"><span data-stu-id="cc80c-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="cc80c-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="cc80c-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="cc80c-283">2\. Nachrichten</span><span class="sxs-lookup"><span data-stu-id="cc80c-283">2 Messages</span></span>

-   [<span data-ttu-id="cc80c-284">2.1 Transport</span><span class="sxs-lookup"><span data-stu-id="cc80c-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="cc80c-285">2.2 Nachrichtensyntax</span><span class="sxs-lookup"><span data-stu-id="cc80c-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="cc80c-286">2.1 Transport</span><span class="sxs-lookup"><span data-stu-id="cc80c-286">2.1 Transport</span></span>

<span data-ttu-id="cc80c-287">Alle Nachrichten MÜSSEN mithilfe einer Named Pipe übertragen werden, wie in \[ MS-SMB \] angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="cc80c-288">Der folgende Pipename wird verwendet:</span><span class="sxs-lookup"><span data-stu-id="cc80c-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="cc80c-289">\\\\ \_ Pipe-CI-SKADS</span><span class="sxs-lookup"><span data-stu-id="cc80c-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="cc80c-290">Dieses Protokoll verwendet das zugrunde liegende SMB-Named Pipe-Protokoll, um die Identität des Aufrufers abzurufen, der die Verbindung hergestellt hat, wie in Abschnitt 2.2.8 von \[ MS-SMB \] angegeben. Der Client MUSS SECURITY \_ IDENTIFICATION als ImpersonationLevel in der Anforderung festlegen, um die Named Pipe zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="cc80c-291">2.2 Nachrichtensyntax</span><span class="sxs-lookup"><span data-stu-id="cc80c-291">2.2 Message Syntax</span></span>

<span data-ttu-id="cc80c-292">Mehrere Strukturen und Meldungen in den folgenden Abschnitten beziehen sich auf Kapitel- oder Lesezeichenhandles.</span><span class="sxs-lookup"><span data-stu-id="cc80c-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="cc80c-293">Ein Handle ist eine 32-Bit-lange nicht transparente Struktur, die ein Kapitel oder Lesezeichen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="cc80c-294">In der Regel empfangen Clientanwendungen Handlewerte über Methodenaufrufe. es gibt jedoch mehrere bekannte Werte, die nicht von einem Server abgerufen werden müssen, dessen Bedeutung in der folgenden Tabelle angegeben ist:</span><span class="sxs-lookup"><span data-stu-id="cc80c-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="cc80c-295">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-295">Value</span></span>                         | <span data-ttu-id="cc80c-296">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-297">DB \_ NULL \_ HCHAPTER 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="cc80c-298">Ein Kapitelhandle für das nicht gekachelte Rowset, das alle Abfrageergebnisse enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="cc80c-299">DBBMK \_ FIRST 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="cc80c-300">Ein Lesezeichenhandle für ein Lesezeichen, das die erste Zeile im Rowset identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="cc80c-301">DBBMK \_ LAST 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="cc80c-302">Ein Lesezeichenhand handle für ein Lesezeichen, das die letzte Zeile im Rowset identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="cc80c-303">2.2.1 Strukturen</span><span class="sxs-lookup"><span data-stu-id="cc80c-303">2.2.1 Structures</span></span>

<span data-ttu-id="cc80c-304">In diesem Abschnitt werden Datenstrukturen beschrieben, die von CISP definiert und verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="cc80c-305">Alle 2-, 4- und 8-Byte-Ganzzahlen mit und ohne Vorzeichen in den folgenden Strukturen MÜSSEN in Little-Endian-Byte-Reihenfolge übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="cc80c-306">In der folgenden Tabelle sind die in diesem Abschnitt definierten Datenstrukturen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="cc80c-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="cc80c-307">Struktur</span><span class="sxs-lookup"><span data-stu-id="cc80c-307">Structure</span></span>                    | <span data-ttu-id="cc80c-308">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc80c-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-309">CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="cc80c-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="cc80c-310">Enthält den Wert, für den eine Übereinstimmungsoperation für eine In einer CPropertyRestriction-Struktur angegebene Eigenschaft durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="cc80c-311">SAFEARRAY, SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="cc80c-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="cc80c-312">Enthält ein mehrdimensionales Array.</span><span class="sxs-lookup"><span data-stu-id="cc80c-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="cc80c-313">SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="cc80c-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="cc80c-314">Stellt die Begrenzungen für eine Dimension eines Arrays dar, das in einer SAFEARRAY-Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="cc80c-315">CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="cc80c-315">CFullPropSpec</span></span>                | <span data-ttu-id="cc80c-316">Enthält eine Eigenschaftenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="cc80c-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="cc80c-317">CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-317">CContentRestriction</span></span>          | <span data-ttu-id="cc80c-318">Enthält eine Zeichenfolge, die mit einem Eigenschaftswert im Eigenschaftencache übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="cc80c-319">CKey</span><span class="sxs-lookup"><span data-stu-id="cc80c-319">CKey</span></span>                         | <span data-ttu-id="cc80c-320">Enthält einen Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="cc80c-321">CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="cc80c-322">Enthält einen Eigenschaftswert, der mit einem Vorgang übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="cc80c-323">CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="cc80c-324">Enthält eine Abfrage in natürlicher Sprache für eine Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cc80c-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="cc80c-325">CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-325">CNodeRestriction</span></span>             | <span data-ttu-id="cc80c-326">Enthält ein Array von Befehlsstrukturknoten, die die Einschränkungen für eine Abfrage angeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="cc80c-327">COccRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-327">COccRestriction</span></span>              | <span data-ttu-id="cc80c-328">Enthält die Position eines Worts in einem Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="cc80c-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="cc80c-329">CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-329">CPropertyRestriction</span></span>         | <span data-ttu-id="cc80c-330">Enthält einen Eigenschaftswert, der mit einem Vorgang übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="cc80c-331">CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-331">CRangeRestriction</span></span>            | <span data-ttu-id="cc80c-332">Enthält eine Einschränkung für einen Wertebereich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="cc80c-333">CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-333">CScopeRestriction</span></span>            | <span data-ttu-id="cc80c-334">Enthält eine Einschränkung für die zu durchsuchenden Dateien.</span><span class="sxs-lookup"><span data-stu-id="cc80c-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="cc80c-335">CSort</span><span class="sxs-lookup"><span data-stu-id="cc80c-335">CSort</span></span>                        | <span data-ttu-id="cc80c-336">Identifiziert eine zu sortierende Spalte.</span><span class="sxs-lookup"><span data-stu-id="cc80c-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="cc80c-337">CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-337">CSynRestriction</span></span>              | <span data-ttu-id="cc80c-338">Enthält ein Wort oder seine Synonyme für einen Abfragebegriff.</span><span class="sxs-lookup"><span data-stu-id="cc80c-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="cc80c-339">CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-339">CVectorRestriction</span></span>           | <span data-ttu-id="cc80c-340">Enthält einen gewichteten OR-Vorgang auf einem Befehlsstrukturknoten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="cc80c-341">CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-341">CWordRestriction</span></span>             | <span data-ttu-id="cc80c-342">Enthält ein Wort für einen Abfragebegriff.</span><span class="sxs-lookup"><span data-stu-id="cc80c-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="cc80c-343">CRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-343">CRestriction</span></span>                 | <span data-ttu-id="cc80c-344">Enthält einen Knoten einer Abfragebefehlsstruktur.</span><span class="sxs-lookup"><span data-stu-id="cc80c-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="cc80c-345">CColumnSet</span><span class="sxs-lookup"><span data-stu-id="cc80c-345">CColumnSet</span></span>                   | <span data-ttu-id="cc80c-346">Gibt die Anzahl der zurückgibtden Spalten an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="cc80c-347">CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="cc80c-347">CCategorizationSet</span></span>           | <span data-ttu-id="cc80c-348">Enthält Informationen zum Gruppieren eines Sets von Abfrageergebnissen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="cc80c-349">CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="cc80c-349">CCategorizationSpec</span></span>          | <span data-ttu-id="cc80c-350">Enthält eine Definition von Kategorien, in die Abfrageergebnisse kategorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="cc80c-351">CDbColId</span><span class="sxs-lookup"><span data-stu-id="cc80c-351">CDbColId</span></span>                     | <span data-ttu-id="cc80c-352">Enthält eine Spalte.</span><span class="sxs-lookup"><span data-stu-id="cc80c-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="cc80c-353">CDbProp</span><span class="sxs-lookup"><span data-stu-id="cc80c-353">CDbProp</span></span>                      | <span data-ttu-id="cc80c-354">Enthält eine -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cc80c-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="cc80c-355">CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="cc80c-355">CDbPropSet</span></span>                   | <span data-ttu-id="cc80c-356">Enthält einen Satz von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cc80c-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="cc80c-357">CPidMapper</span><span class="sxs-lookup"><span data-stu-id="cc80c-357">CPidMapper</span></span>                   | <span data-ttu-id="cc80c-358">Enthält ein Array von Eigenschaften-IDs, die die Eigenschaften angeben, die in einem Rowset zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="cc80c-359">CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="cc80c-359">CRowSeekAt</span></span>                   | <span data-ttu-id="cc80c-360">Enthält den Offset, an dem Zeilen in einer CPMGetRowsIn-Nachricht abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="cc80c-361">CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="cc80c-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="cc80c-362">Identifiziert den Punkt, an dem der Abruf für eine CPMGetRowsIn-Nachricht beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="cc80c-363">CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="cc80c-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="cc80c-364">Identifiziert die Lesezeichen, aus denen Zeilen für eine CPMGetRowsIn-Nachricht abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="cc80c-365">CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="cc80c-365">CRowSeekNext</span></span>                 | <span data-ttu-id="cc80c-366">Enthält die Anzahl der Zeilen, die in einer CPMGetRowsIn-Nachricht übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="cc80c-367">CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="cc80c-367">CRowsetProperties</span></span>            | <span data-ttu-id="cc80c-368">Enthält die Konfigurationsinformationen für eine Abfrage.</span><span class="sxs-lookup"><span data-stu-id="cc80c-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="cc80c-369">CSortSet</span><span class="sxs-lookup"><span data-stu-id="cc80c-369">CSortSet</span></span>                     | <span data-ttu-id="cc80c-370">Enthält die Sortierreihenfolge für eine Abfrage.</span><span class="sxs-lookup"><span data-stu-id="cc80c-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="cc80c-371">CTableColumn</span><span class="sxs-lookup"><span data-stu-id="cc80c-371">CTableColumn</span></span>                 | <span data-ttu-id="cc80c-372">Enthält eine Spalte für die CPMSetBindings-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="cc80c-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="cc80c-373">SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="cc80c-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="cc80c-374">Enthält einen serialisierten Wert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="cc80c-375">2.2.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="cc80c-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="cc80c-376">Die CBaseStorageVariant-Struktur enthält den Wert, für den ein Übereinstimmungsvorgang für eine in der CPropertyRestriction-Struktur angegebene Eigenschaft ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="cc80c-377">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-377">0</span></span>

<span data-ttu-id="cc80c-378">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-378">1</span></span>

<span data-ttu-id="cc80c-379">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-379">2</span></span>

<span data-ttu-id="cc80c-380">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-380">3</span></span>

<span data-ttu-id="cc80c-381">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-381">4</span></span>

<span data-ttu-id="cc80c-382">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-382">5</span></span>

<span data-ttu-id="cc80c-383">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-383">6</span></span>

<span data-ttu-id="cc80c-384">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-384">7</span></span>

<span data-ttu-id="cc80c-385">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-385">8</span></span>

<span data-ttu-id="cc80c-386">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-386">9</span></span>

<span data-ttu-id="cc80c-387">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-387">1</span></span><br/> <span data-ttu-id="cc80c-388">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-388">0</span></span><br/>

<span data-ttu-id="cc80c-389">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-389">1</span></span>

<span data-ttu-id="cc80c-390">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-390">2</span></span>

<span data-ttu-id="cc80c-391">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-391">3</span></span>

<span data-ttu-id="cc80c-392">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-392">4</span></span>

<span data-ttu-id="cc80c-393">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-393">5</span></span>

<span data-ttu-id="cc80c-394">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-394">6</span></span>

<span data-ttu-id="cc80c-395">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-395">7</span></span>

<span data-ttu-id="cc80c-396">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-396">8</span></span>

<span data-ttu-id="cc80c-397">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-397">9</span></span>

<span data-ttu-id="cc80c-398">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-398">2</span></span><br/> <span data-ttu-id="cc80c-399">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-399">0</span></span><br/>

<span data-ttu-id="cc80c-400">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-400">1</span></span>

<span data-ttu-id="cc80c-401">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-401">2</span></span>

<span data-ttu-id="cc80c-402">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-402">3</span></span>

<span data-ttu-id="cc80c-403">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-403">4</span></span>

<span data-ttu-id="cc80c-404">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-404">5</span></span>

<span data-ttu-id="cc80c-405">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-405">6</span></span>

<span data-ttu-id="cc80c-406">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-406">7</span></span>

<span data-ttu-id="cc80c-407">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-407">8</span></span>

<span data-ttu-id="cc80c-408">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-408">9</span></span>

<span data-ttu-id="cc80c-409">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-409">3</span></span><br/> <span data-ttu-id="cc80c-410">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-410">0</span></span><br/>

<span data-ttu-id="cc80c-411">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-411">1</span></span>

<span data-ttu-id="cc80c-412">vType</span><span class="sxs-lookup"><span data-stu-id="cc80c-412">vType</span></span>

<span data-ttu-id="cc80c-413">vData1</span><span class="sxs-lookup"><span data-stu-id="cc80c-413">vData1</span></span>

<span data-ttu-id="cc80c-414">vData2</span><span class="sxs-lookup"><span data-stu-id="cc80c-414">vData2</span></span>

<span data-ttu-id="cc80c-415">vValue (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-415">vValue (variable)</span></span>



 

<span data-ttu-id="cc80c-416">**vType:** Ein Typindikator, der den Typ von vValue angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="cc80c-417">Dies MUSS einer der in der folgenden Tabelle angegebenen VARENUM-Werte sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="cc80c-418">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-418">Value</span></span>                 | <span data-ttu-id="cc80c-419">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-420">VT \_ EMPTY (0x0000)</span><span class="sxs-lookup"><span data-stu-id="cc80c-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="cc80c-421">vValue ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="cc80c-422">VT \_ NULL (0x0001)</span><span class="sxs-lookup"><span data-stu-id="cc80c-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="cc80c-423">vValue ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="cc80c-424">VT \_ I1 (0x0010)</span><span class="sxs-lookup"><span data-stu-id="cc80c-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="cc80c-425">Eine 1-Byte-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="cc80c-426">VT \_ UI1 (0x0011)</span><span class="sxs-lookup"><span data-stu-id="cc80c-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="cc80c-427">Eine 1-Byte-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="cc80c-428">VT \_ I2 (0x0002)</span><span class="sxs-lookup"><span data-stu-id="cc80c-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="cc80c-429">Eine 2-Byte-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="cc80c-430">VT \_ UI2 (0x0012)</span><span class="sxs-lookup"><span data-stu-id="cc80c-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="cc80c-431">Eine 2-Byte-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="cc80c-432">VT \_ BOOL (0x000B)</span><span class="sxs-lookup"><span data-stu-id="cc80c-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="cc80c-433">Ein boolescher Wert; eine 2-Byte-Ganzzahl, die 0x0000 (FALSE) oder 0xFFFF (TRUE) enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="cc80c-434">VT \_ I4 (0x0003)</span><span class="sxs-lookup"><span data-stu-id="cc80c-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="cc80c-435">Eine 4-Byte-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="cc80c-436">VT \_ UI4 (0x0013)</span><span class="sxs-lookup"><span data-stu-id="cc80c-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="cc80c-437">Eine 4-Byte-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="cc80c-438">VT \_ R4 (0x0004)</span><span class="sxs-lookup"><span data-stu-id="cc80c-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="cc80c-439">Eine IEEE 32-Bit-Gleitkommazahl, wie in \[ IEEE754 \] definiert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="cc80c-440">VT \_ INT (0x0016)</span><span class="sxs-lookup"><span data-stu-id="cc80c-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="cc80c-441">Eine 4-Byte-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="cc80c-442">VT \_ UINT (0x0017)</span><span class="sxs-lookup"><span data-stu-id="cc80c-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="cc80c-443">Eine 4-Byte-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="cc80c-444">\_VT-FEHLER (0x000A)</span><span class="sxs-lookup"><span data-stu-id="cc80c-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="cc80c-445">Eine 4-Byte-Ganzzahl ohne Vorzeichen, die ein HRESULT enthält, wie in \[ MS-SYS \] angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="cc80c-446">VT \_ I8 (0x0014)</span><span class="sxs-lookup"><span data-stu-id="cc80c-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="cc80c-447">Eine 8-Byte-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="cc80c-448">VT \_ UI8 (0x0015)</span><span class="sxs-lookup"><span data-stu-id="cc80c-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="cc80c-449">Eine 8-Byte-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="cc80c-450">VT \_ R8 (0x0005)</span><span class="sxs-lookup"><span data-stu-id="cc80c-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="cc80c-451">Eine IEEE 64-Bit-Gleitkommazahl, wie in \[ IEEE754 \] definiert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="cc80c-452">VT \_ CY (0x0006)</span><span class="sxs-lookup"><span data-stu-id="cc80c-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="cc80c-453">Eine 8-Byte-Komplement-Ganzzahl (skaliert um 10.000).</span><span class="sxs-lookup"><span data-stu-id="cc80c-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="cc80c-454">VT \_ DATE (0x0007)</span><span class="sxs-lookup"><span data-stu-id="cc80c-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="cc80c-455">Eine 64-Bit-Gleitkommazahl, die die Anzahl der Tage seit 00:00:00 Uhr am 31. Dezember 1899 (koordinierte Weltzeit) darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="cc80c-456">VT \_ FILETIME (0x0040)</span><span class="sxs-lookup"><span data-stu-id="cc80c-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="cc80c-457">Eine 64-Bit-Ganzzahl, die die Anzahl von 100-Nanosekunden-Intervallen seit 00:00:00 Uhr am 1. Januar 1601 darstellt (koordinierte Weltzeit).</span><span class="sxs-lookup"><span data-stu-id="cc80c-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="cc80c-458">VT \_ DECIMAL (0x000E)</span><span class="sxs-lookup"><span data-stu-id="cc80c-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="cc80c-459">Eine DECIMAL-Struktur, wie in Abschnitt 2.2.1.1.1.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="cc80c-460">VT \_ CLSID (0x0048)</span><span class="sxs-lookup"><span data-stu-id="cc80c-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="cc80c-461">Ein 16-Byte-Binärwert, der eine GUID enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="cc80c-462">\_VT-BLOB (0x0041)</span><span class="sxs-lookup"><span data-stu-id="cc80c-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="cc80c-463">Eine 4-Byte-ganzzahlige Anzahl von Bytes ohne Vorzeichen im Blob, gefolgt von dieser Anzahl von Datenbytes.</span><span class="sxs-lookup"><span data-stu-id="cc80c-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="cc80c-464">VT \_ BSTR (0x0008)</span><span class="sxs-lookup"><span data-stu-id="cc80c-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="cc80c-465">Eine 4-Byte-Ganzzahl ohne Vorzeichen in der Zeichenfolge, gefolgt von einer Zeichenfolge, wie unten unter vValue angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="cc80c-466">VT \_ LPSTR (0x001E)</span><span class="sxs-lookup"><span data-stu-id="cc80c-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="cc80c-467">Eine AUF NULL endende ANSI-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cc80c-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="cc80c-468">VT \_ LPWSTR (0x001F)</span><span class="sxs-lookup"><span data-stu-id="cc80c-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="cc80c-469">Eine UNICODE-Zeichenfolge mit \[ NULL-Terminierung. \]</span><span class="sxs-lookup"><span data-stu-id="cc80c-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="cc80c-470">VT \_ VARIANT (0x000C)</span><span class="sxs-lookup"><span data-stu-id="cc80c-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="cc80c-471">CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="cc80c-471">CBaseStorageVariant.</span></span> <span data-ttu-id="cc80c-472">MUSS mit einem Typmodifizierer von VT \_ ARRAY oder VT VECTOR kombiniert \_ werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="cc80c-473">In der folgenden Tabelle werden die Typmodifizierer für vType angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="cc80c-474">Typmodifizierer können binäres ORed mit vType sein, um die Bedeutung von vValue zu ändern und anzugeben, dass es sich um einen von zwei möglichen Arraytypen handelt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="cc80c-475">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-475">Value</span></span>               | <span data-ttu-id="cc80c-476">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-477">VT \_ VECTOR (0x1000)</span><span class="sxs-lookup"><span data-stu-id="cc80c-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="cc80c-478">Wenn der Typindikator mithilfe eines OR-Operators mit VT VECTOR kombiniert wird, ist vValue ein gezähltes Array von Werten \_ des angegebenen Typs.</span><span class="sxs-lookup"><span data-stu-id="cc80c-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="cc80c-479">Weitere Informationen finden Sie in Abschnitt 2.2.1.1.1.2.</span><span class="sxs-lookup"><span data-stu-id="cc80c-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="cc80c-480">Dieser Typmodifizierer DARF NICHT mit den folgenden Typen kombiniert werden: VT \_ INT, VT \_ UINT, VT \_ DECIMAL, VT \_ BLOB, VT \_ BLOB \_ OBJECT.</span><span class="sxs-lookup"><span data-stu-id="cc80c-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="cc80c-481">VT \_ ARRAY (0x2000)</span><span class="sxs-lookup"><span data-stu-id="cc80c-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="cc80c-482">Wenn der Typindikator durch einen OR-Operator mit VT ARRAY kombiniert wird, ist der Wert ein \_ SAFEARRAY (wie in Abschnitt 2.2.1.1.1.3 angegeben), das Werte des angegebenen Typs enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="cc80c-483">Dieser Typmodifizierer DARF NICHT mit den folgenden Typen kombiniert werden: VT \_ I8, VT \_ UI8, VT \_ FILETIME, VT \_ CLSID, VT \_ BLOB, VT \_ BLOB \_ OBJECT, VT \_ LPSTR, VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="cc80c-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="cc80c-484">**vData1:** Wenn vType VT DECIMAL ist, wird der Wert dieses Felds als Scale-Feld in Abschnitt \_ 2.2.1.1.1.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="cc80c-485">Für alle anderen vTypes MUSS der Wert auf 0x00.</span><span class="sxs-lookup"><span data-stu-id="cc80c-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="cc80c-486">**vData2:** Wenn vType VT DECIMAL ist, wird der Wert dieses Felds im Abschnitt \_ 2.2.1.1.1.1.1 als Feld Sign angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="cc80c-487">Für alle anderen vTypes MUSS der Wert auf 0x00.</span><span class="sxs-lookup"><span data-stu-id="cc80c-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="cc80c-488">**vValue:** Der Wert für den Ab übereinstimmungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="cc80c-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="cc80c-489">Die Syntax MUSS wie im vType-Feld angegeben sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="cc80c-490">In der folgenden Tabelle sind die Größen für das vValue-Feld zusammengefasst, abhängig vom vType-Feld für Datentypen fester Länge.</span><span class="sxs-lookup"><span data-stu-id="cc80c-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="cc80c-491">Die Größe ist in Bytes.</span><span class="sxs-lookup"><span data-stu-id="cc80c-491">The size is in bytes.</span></span>



| <span data-ttu-id="cc80c-492">vType</span><span class="sxs-lookup"><span data-stu-id="cc80c-492">vType</span></span>                                                   | <span data-ttu-id="cc80c-493">Size</span><span class="sxs-lookup"><span data-stu-id="cc80c-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="cc80c-494">VT \_ I1, VT, \_ UI1</span><span class="sxs-lookup"><span data-stu-id="cc80c-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="cc80c-495">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-495">1</span></span>    |
| <span data-ttu-id="cc80c-496">VT \_ I2, VT \_ UI2, VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="cc80c-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="cc80c-497">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-497">2</span></span>    |
| <span data-ttu-id="cc80c-498">VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ INT, VT \_ UINT, VT \_ ERROR</span><span class="sxs-lookup"><span data-stu-id="cc80c-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="cc80c-499">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-499">4</span></span>    |
| <span data-ttu-id="cc80c-500">VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ DATE, VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="cc80c-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="cc80c-501">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-501">8</span></span>    |
| <span data-ttu-id="cc80c-502">VT \_ DECIMAL, VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="cc80c-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="cc80c-503">16</span><span class="sxs-lookup"><span data-stu-id="cc80c-503">16</span></span>   |



 

<span data-ttu-id="cc80c-504">Wenn vType auf VT \_ BLOB, VT BSTR oder VT LPSTR festgelegt ist, \_ wird die Struktur von \_ vValue im folgenden Diagramm angegeben:</span><span class="sxs-lookup"><span data-stu-id="cc80c-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="cc80c-505">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-505">0</span></span>

<span data-ttu-id="cc80c-506">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-506">1</span></span>

<span data-ttu-id="cc80c-507">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-507">2</span></span>

<span data-ttu-id="cc80c-508">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-508">3</span></span>

<span data-ttu-id="cc80c-509">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-509">4</span></span>

<span data-ttu-id="cc80c-510">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-510">5</span></span>

<span data-ttu-id="cc80c-511">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-511">6</span></span>

<span data-ttu-id="cc80c-512">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-512">7</span></span>

<span data-ttu-id="cc80c-513">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-513">8</span></span>

<span data-ttu-id="cc80c-514">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-514">9</span></span>

<span data-ttu-id="cc80c-515">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-515">1</span></span><br/> <span data-ttu-id="cc80c-516">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-516">0</span></span><br/>

<span data-ttu-id="cc80c-517">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-517">1</span></span>

<span data-ttu-id="cc80c-518">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-518">2</span></span>

<span data-ttu-id="cc80c-519">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-519">3</span></span>

<span data-ttu-id="cc80c-520">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-520">4</span></span>

<span data-ttu-id="cc80c-521">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-521">5</span></span>

<span data-ttu-id="cc80c-522">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-522">6</span></span>

<span data-ttu-id="cc80c-523">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-523">7</span></span>

<span data-ttu-id="cc80c-524">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-524">8</span></span>

<span data-ttu-id="cc80c-525">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-525">9</span></span>

<span data-ttu-id="cc80c-526">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-526">2</span></span><br/> <span data-ttu-id="cc80c-527">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-527">0</span></span><br/>

<span data-ttu-id="cc80c-528">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-528">1</span></span>

<span data-ttu-id="cc80c-529">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-529">2</span></span>

<span data-ttu-id="cc80c-530">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-530">3</span></span>

<span data-ttu-id="cc80c-531">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-531">4</span></span>

<span data-ttu-id="cc80c-532">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-532">5</span></span>

<span data-ttu-id="cc80c-533">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-533">6</span></span>

<span data-ttu-id="cc80c-534">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-534">7</span></span>

<span data-ttu-id="cc80c-535">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-535">8</span></span>

<span data-ttu-id="cc80c-536">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-536">9</span></span>

<span data-ttu-id="cc80c-537">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-537">3</span></span><br/> <span data-ttu-id="cc80c-538">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-538">0</span></span><br/>

<span data-ttu-id="cc80c-539">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-539">1</span></span>

<span data-ttu-id="cc80c-540">cbSize</span><span class="sxs-lookup"><span data-stu-id="cc80c-540">cbSize</span></span>

<span data-ttu-id="cc80c-541">blobData (Variable, optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="cc80c-542">**cbSize:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des blobData-Felds in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="cc80c-543">Wenn vType auf VT \_ BSTR oder VT LPSTR festgelegt \_ ist, MUSS cbSize auf 0x00000000 festgelegt werden, wenn die dargestellte Zeichenfolge eine leere Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="cc80c-544">**blobData:** MUSS die Länge cbSize in Bytes haben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="cc80c-545">Bei vType, das auf VT-BLOB festgelegt ist, handelt es sich bei diesem Feld um \_ nicht transparente binäre Blobdaten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="cc80c-546">Bei vType, das auf VT BSTR festgelegt ist, handelt es sich bei diesem Feld um \_ einen Satz von Zeichen in einem vom OEM ausgewählten Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="cc80c-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="cc80c-547">Client und Server MÜSSEN so konfiguriert sein, dass sie über interoperable Zeichensätze verfügen (out-of-band des Protokolls).</span><span class="sxs-lookup"><span data-stu-id="cc80c-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="cc80c-548">Es ist nicht erforderlich, dass sie NULL-terminiert ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="cc80c-549">Bei vType, das auf VT LPSTR festgelegt \_ ist, ist dieses Feld eine auf NULL endende Zeichenfolge in einem vom OEM ausgewählten Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="cc80c-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="cc80c-550">Client und Server MÜSSEN so konfiguriert sein, dass sie über interoperable Zeichensätze verfügen (out-of-band des Protokolls).</span><span class="sxs-lookup"><span data-stu-id="cc80c-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="cc80c-551">Wenn vType auf VT \_ LPWSTR festgelegt ist, wird die Struktur von vValue im folgenden Diagramm angegeben:</span><span class="sxs-lookup"><span data-stu-id="cc80c-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="cc80c-552">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-552">0</span></span>

<span data-ttu-id="cc80c-553">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-553">1</span></span>

<span data-ttu-id="cc80c-554">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-554">2</span></span>

<span data-ttu-id="cc80c-555">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-555">3</span></span>

<span data-ttu-id="cc80c-556">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-556">4</span></span>

<span data-ttu-id="cc80c-557">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-557">5</span></span>

<span data-ttu-id="cc80c-558">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-558">6</span></span>

<span data-ttu-id="cc80c-559">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-559">7</span></span>

<span data-ttu-id="cc80c-560">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-560">8</span></span>

<span data-ttu-id="cc80c-561">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-561">9</span></span>

<span data-ttu-id="cc80c-562">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-562">1</span></span><br/> <span data-ttu-id="cc80c-563">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-563">0</span></span><br/>

<span data-ttu-id="cc80c-564">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-564">1</span></span>

<span data-ttu-id="cc80c-565">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-565">2</span></span>

<span data-ttu-id="cc80c-566">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-566">3</span></span>

<span data-ttu-id="cc80c-567">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-567">4</span></span>

<span data-ttu-id="cc80c-568">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-568">5</span></span>

<span data-ttu-id="cc80c-569">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-569">6</span></span>

<span data-ttu-id="cc80c-570">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-570">7</span></span>

<span data-ttu-id="cc80c-571">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-571">8</span></span>

<span data-ttu-id="cc80c-572">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-572">9</span></span>

<span data-ttu-id="cc80c-573">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-573">2</span></span><br/> <span data-ttu-id="cc80c-574">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-574">0</span></span><br/>

<span data-ttu-id="cc80c-575">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-575">1</span></span>

<span data-ttu-id="cc80c-576">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-576">2</span></span>

<span data-ttu-id="cc80c-577">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-577">3</span></span>

<span data-ttu-id="cc80c-578">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-578">4</span></span>

<span data-ttu-id="cc80c-579">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-579">5</span></span>

<span data-ttu-id="cc80c-580">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-580">6</span></span>

<span data-ttu-id="cc80c-581">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-581">7</span></span>

<span data-ttu-id="cc80c-582">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-582">8</span></span>

<span data-ttu-id="cc80c-583">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-583">9</span></span>

<span data-ttu-id="cc80c-584">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-584">3</span></span><br/> <span data-ttu-id="cc80c-585">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-585">0</span></span><br/>

<span data-ttu-id="cc80c-586">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-586">1</span></span>

<span data-ttu-id="cc80c-587">ccLen</span><span class="sxs-lookup"><span data-stu-id="cc80c-587">ccLen</span></span>

<span data-ttu-id="cc80c-588">string (variable, optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-588">string (variable, optional)</span></span>



 

<span data-ttu-id="cc80c-589">**ccLen:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des Zeichenfolgenfelds in Unicode-Zeichen angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="cc80c-590">MUSS für eine leere Zeichenfolge auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="cc80c-591">**string:** Mit NULL beendete Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cc80c-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="cc80c-592">2.2.1.1.1 CBaseStorageVariant-Strukturen</span><span class="sxs-lookup"><span data-stu-id="cc80c-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="cc80c-593">Die folgenden Strukturen werden in der CBaseStorageVariant-Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="cc80c-594">2.2.1.1.1.1 DECIMAL</span><span class="sxs-lookup"><span data-stu-id="cc80c-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="cc80c-595">DECIMAL wird verwendet, um einen genauen numerischen Wert mit fester Genauigkeit und fester Dezimalstellenzahl zu darstellen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="cc80c-596">Wenn vType auf VT DECIMAL (0x0000E) festgelegt ist, MÜSSEN die Felder \_ vData1 und vData2 von CBaseStorageVariant wie folgt interpretiert werden:</span><span class="sxs-lookup"><span data-stu-id="cc80c-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="cc80c-597">**vData1:** Die Anzahl der Ziffern rechts vom Dezimaltrennzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="cc80c-598">MUSS im Bereich von 0 bis 28 liegen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="cc80c-599">**vData2:** Das Vorzeichen des numerischen Werts.</span><span class="sxs-lookup"><span data-stu-id="cc80c-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="cc80c-600">Legen Sie auf 0x00, wenn positiv, 0x80, wenn negativ.</span><span class="sxs-lookup"><span data-stu-id="cc80c-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="cc80c-601">Das Format des vValue-Felds ist:</span><span class="sxs-lookup"><span data-stu-id="cc80c-601">The format of the vValue field is:</span></span>



<span data-ttu-id="cc80c-602">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-602">0</span></span>

<span data-ttu-id="cc80c-603">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-603">1</span></span>

<span data-ttu-id="cc80c-604">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-604">2</span></span>

<span data-ttu-id="cc80c-605">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-605">3</span></span>

<span data-ttu-id="cc80c-606">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-606">4</span></span>

<span data-ttu-id="cc80c-607">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-607">5</span></span>

<span data-ttu-id="cc80c-608">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-608">6</span></span>

<span data-ttu-id="cc80c-609">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-609">7</span></span>

<span data-ttu-id="cc80c-610">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-610">8</span></span>

<span data-ttu-id="cc80c-611">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-611">9</span></span>

<span data-ttu-id="cc80c-612">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-612">1</span></span><br/> <span data-ttu-id="cc80c-613">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-613">0</span></span><br/>

<span data-ttu-id="cc80c-614">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-614">1</span></span>

<span data-ttu-id="cc80c-615">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-615">2</span></span>

<span data-ttu-id="cc80c-616">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-616">3</span></span>

<span data-ttu-id="cc80c-617">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-617">4</span></span>

<span data-ttu-id="cc80c-618">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-618">5</span></span>

<span data-ttu-id="cc80c-619">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-619">6</span></span>

<span data-ttu-id="cc80c-620">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-620">7</span></span>

<span data-ttu-id="cc80c-621">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-621">8</span></span>

<span data-ttu-id="cc80c-622">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-622">9</span></span>

<span data-ttu-id="cc80c-623">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-623">2</span></span><br/> <span data-ttu-id="cc80c-624">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-624">0</span></span><br/>

<span data-ttu-id="cc80c-625">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-625">1</span></span>

<span data-ttu-id="cc80c-626">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-626">2</span></span>

<span data-ttu-id="cc80c-627">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-627">3</span></span>

<span data-ttu-id="cc80c-628">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-628">4</span></span>

<span data-ttu-id="cc80c-629">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-629">5</span></span>

<span data-ttu-id="cc80c-630">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-630">6</span></span>

<span data-ttu-id="cc80c-631">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-631">7</span></span>

<span data-ttu-id="cc80c-632">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-632">8</span></span>

<span data-ttu-id="cc80c-633">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-633">9</span></span>

<span data-ttu-id="cc80c-634">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-634">3</span></span><br/> <span data-ttu-id="cc80c-635">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-635">0</span></span><br/>

<span data-ttu-id="cc80c-636">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-636">1</span></span>

<span data-ttu-id="cc80c-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="cc80c-637">Hi32</span></span>

<span data-ttu-id="cc80c-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="cc80c-638">Lo32</span></span>

<span data-ttu-id="cc80c-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="cc80c-639">Mid32</span></span>



 

<span data-ttu-id="cc80c-640">**Hi32:** Die höchsten 32 Bits der 96-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="cc80c-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="cc80c-641">**Lo32**: Die niedrigsten 32 Bits der 96-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="cc80c-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="cc80c-642">**Mid32:** Die mittleren 32 Bits der 96-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="cc80c-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="cc80c-643">2.2.1.1.1.2 VT \_ VECTOR</span><span class="sxs-lookup"><span data-stu-id="cc80c-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="cc80c-644">VT \_ Vector wird verwendet, um eindimensionale Arrays zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="cc80c-645">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-645">0</span></span>

<span data-ttu-id="cc80c-646">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-646">1</span></span>

<span data-ttu-id="cc80c-647">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-647">2</span></span>

<span data-ttu-id="cc80c-648">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-648">3</span></span>

<span data-ttu-id="cc80c-649">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-649">4</span></span>

<span data-ttu-id="cc80c-650">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-650">5</span></span>

<span data-ttu-id="cc80c-651">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-651">6</span></span>

<span data-ttu-id="cc80c-652">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-652">7</span></span>

<span data-ttu-id="cc80c-653">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-653">8</span></span>

<span data-ttu-id="cc80c-654">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-654">9</span></span>

<span data-ttu-id="cc80c-655">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-655">1</span></span><br/> <span data-ttu-id="cc80c-656">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-656">0</span></span><br/>

<span data-ttu-id="cc80c-657">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-657">1</span></span>

<span data-ttu-id="cc80c-658">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-658">2</span></span>

<span data-ttu-id="cc80c-659">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-659">3</span></span>

<span data-ttu-id="cc80c-660">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-660">4</span></span>

<span data-ttu-id="cc80c-661">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-661">5</span></span>

<span data-ttu-id="cc80c-662">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-662">6</span></span>

<span data-ttu-id="cc80c-663">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-663">7</span></span>

<span data-ttu-id="cc80c-664">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-664">8</span></span>

<span data-ttu-id="cc80c-665">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-665">9</span></span>

<span data-ttu-id="cc80c-666">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-666">2</span></span><br/> <span data-ttu-id="cc80c-667">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-667">0</span></span><br/>

<span data-ttu-id="cc80c-668">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-668">1</span></span>

<span data-ttu-id="cc80c-669">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-669">2</span></span>

<span data-ttu-id="cc80c-670">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-670">3</span></span>

<span data-ttu-id="cc80c-671">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-671">4</span></span>

<span data-ttu-id="cc80c-672">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-672">5</span></span>

<span data-ttu-id="cc80c-673">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-673">6</span></span>

<span data-ttu-id="cc80c-674">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-674">7</span></span>

<span data-ttu-id="cc80c-675">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-675">8</span></span>

<span data-ttu-id="cc80c-676">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-676">9</span></span>

<span data-ttu-id="cc80c-677">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-677">3</span></span><br/> <span data-ttu-id="cc80c-678">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-678">0</span></span><br/>

<span data-ttu-id="cc80c-679">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-679">1</span></span>

<span data-ttu-id="cc80c-680">vVectorElements</span><span class="sxs-lookup"><span data-stu-id="cc80c-680">vVectorElements</span></span>

<span data-ttu-id="cc80c-681">vVectorData</span><span class="sxs-lookup"><span data-stu-id="cc80c-681">vVectorData</span></span>



 

<span data-ttu-id="cc80c-682">**vVectorElements:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im vVectorData-Feld angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="cc80c-683">**vVectorData:** Ein Array von Elementen, deren Typ durch vType angegeben ist, wobei das 0x1000 Bit gelöscht ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="cc80c-684">Die Größe eines einzelnen Elements mit fester Länge kann aus der Tabelle des Datentyps fester Länge abgerufen werden, wie in Abschnitt 2.2.1.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="cc80c-685">Die Länge dieses Felds in Bytes kann berechnet werden, indem vVectorElements mit der Größe des einzelnen Elements multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="cc80c-686">Für Datentypen variabler Länge enthält vVectorData eine Sequenz von aufeinander folgenden gemarshallten einfachen Typen, wobei der Typ durch vType angegeben wird, wobei das 0x1000 Bit gelöscht ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="cc80c-687">Dies schließt einen Sonderfall ein, der durch vType VT \_ ARRAY \| VT \_ VARIANT (d.h. 0x100C) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="cc80c-688">Die Elemente im vVectorData-Feld MÜSSEN durch 0 bis 3 Auffüllungsbytes getrennt werden, sodass jedes Element bei einem Offset beginnt, der ein Vielfaches von 4 Bytes vom Anfang der Nachricht ist, die dieses Array enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="cc80c-689">Wenn auffüllende Bytes vorhanden sind, ist der darin enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="cc80c-690">Der Inhalt der Auffüllungsbytes MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cc80c-691">Für einen vType, der auf VT ARRAY VT VARIANT festgelegt \_ \| \_ ist, ist der Typ für Elemente in dieser Sequenz CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="cc80c-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="cc80c-692">2.2.1.1.1.3 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="cc80c-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="cc80c-693">SAFEARRAY wird verwendet, um mehrdimensionale Arrays zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="cc80c-694">Die -Struktur enthält Informationen zur Arraygröße sowie die Daten im Array.</span><span class="sxs-lookup"><span data-stu-id="cc80c-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="cc80c-695">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-695">0</span></span>

<span data-ttu-id="cc80c-696">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-696">1</span></span>

<span data-ttu-id="cc80c-697">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-697">2</span></span>

<span data-ttu-id="cc80c-698">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-698">3</span></span>

<span data-ttu-id="cc80c-699">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-699">4</span></span>

<span data-ttu-id="cc80c-700">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-700">5</span></span>

<span data-ttu-id="cc80c-701">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-701">6</span></span>

<span data-ttu-id="cc80c-702">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-702">7</span></span>

<span data-ttu-id="cc80c-703">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-703">8</span></span>

<span data-ttu-id="cc80c-704">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-704">9</span></span>

<span data-ttu-id="cc80c-705">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-705">1</span></span><br/> <span data-ttu-id="cc80c-706">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-706">0</span></span><br/>

<span data-ttu-id="cc80c-707">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-707">1</span></span>

<span data-ttu-id="cc80c-708">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-708">2</span></span>

<span data-ttu-id="cc80c-709">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-709">3</span></span>

<span data-ttu-id="cc80c-710">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-710">4</span></span>

<span data-ttu-id="cc80c-711">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-711">5</span></span>

<span data-ttu-id="cc80c-712">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-712">6</span></span>

<span data-ttu-id="cc80c-713">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-713">7</span></span>

<span data-ttu-id="cc80c-714">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-714">8</span></span>

<span data-ttu-id="cc80c-715">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-715">9</span></span>

<span data-ttu-id="cc80c-716">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-716">2</span></span><br/> <span data-ttu-id="cc80c-717">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-717">0</span></span><br/>

<span data-ttu-id="cc80c-718">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-718">1</span></span>

<span data-ttu-id="cc80c-719">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-719">2</span></span>

<span data-ttu-id="cc80c-720">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-720">3</span></span>

<span data-ttu-id="cc80c-721">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-721">4</span></span>

<span data-ttu-id="cc80c-722">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-722">5</span></span>

<span data-ttu-id="cc80c-723">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-723">6</span></span>

<span data-ttu-id="cc80c-724">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-724">7</span></span>

<span data-ttu-id="cc80c-725">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-725">8</span></span>

<span data-ttu-id="cc80c-726">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-726">9</span></span>

<span data-ttu-id="cc80c-727">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-727">3</span></span><br/> <span data-ttu-id="cc80c-728">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-728">0</span></span><br/>

<span data-ttu-id="cc80c-729">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-729">1</span></span>

<span data-ttu-id="cc80c-730">cDims</span><span class="sxs-lookup"><span data-stu-id="cc80c-730">cDims</span></span>

<span data-ttu-id="cc80c-731">fFeatures</span><span class="sxs-lookup"><span data-stu-id="cc80c-731">fFeatures</span></span>

<span data-ttu-id="cc80c-732">cbElements</span><span class="sxs-lookup"><span data-stu-id="cc80c-732">cbElements</span></span>

<span data-ttu-id="cc80c-733">Rgsabound (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-733">Rgsabound (variable)</span></span>

<span data-ttu-id="cc80c-734">vData (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-734">vData (variable)</span></span>



 

<span data-ttu-id="cc80c-735">**cDims:** 16-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dimensionen des mehrdimensionalen Arrays angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="cc80c-736">**fFeatures:** Ein 16-Bit-Bitfeld.</span><span class="sxs-lookup"><span data-stu-id="cc80c-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="cc80c-737">Die Werte stellen Features dar, die von Anwendungen der oberen Ebene definiert werden und ignoriert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="cc80c-738">**cbElements:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe jedes Elements des Arrays angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="cc80c-739">**Rgsabound:** Ein Array, das eine SAFEARRAYBOUND-Struktur enthält, wie in Abschnitt 2.2.1.1.1.4 angegeben, pro Dimension im SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="cc80c-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="cc80c-740">Dieses Array verfügt zuerst über die dimension-ganz links und zuletzt über die rechte Dimension.</span><span class="sxs-lookup"><span data-stu-id="cc80c-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="cc80c-741">**vData:** Ein Vektor gemarshallter Elemente eines bestimmten Typs, der durch den vType der enthaltenden CBaseStorageVariant angegeben wird, während das Bit 0x2000 wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="cc80c-742">vData wird ähnlich wie VT VECTOR gemarshallt, wie in Abschnitt 2.2.1.1.1.2 angegeben, mit dem Unterschied, dass die Anzahl der Elemente nicht vor dem Vektor gespeichert \_ wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="cc80c-743">Stattdessen wird die Anzahl der Elemente berechnet, indem der cElements-Wert mit allen sicheren Array-Begrenzungen multipliziert wird, die im Feld Rgsabound angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="cc80c-744">Elemente werden in einem Vektor in der Reihenfolge der Dimensionen gespeichert, die mit der rechten Dimension beginnen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="cc80c-745">Das folgende Diagramm stellt ein zweidimensionales Beispielarray visuell dar.</span><span class="sxs-lookup"><span data-stu-id="cc80c-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="cc80c-746">Die erste Dimension hat cElements gleich 4 (horizontal dargestellt) und lLbound gleich 0, und die zweite Dimension hat cElements gleich 2 (vertikal dargestellt) und lLbound gleich 0.</span><span class="sxs-lookup"><span data-stu-id="cc80c-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>



|            |            |            |            |
|------------|------------|------------|------------|
| <span data-ttu-id="cc80c-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-747">0x00000001</span></span> | <span data-ttu-id="cc80c-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-748">0x00000002</span></span> | <span data-ttu-id="cc80c-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-749">0x00000003</span></span> | <span data-ttu-id="cc80c-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="cc80c-750">0x00000005</span></span> |
| <span data-ttu-id="cc80c-751">0x00000007</span><span class="sxs-lookup"><span data-stu-id="cc80c-751">0x00000007</span></span> | <span data-ttu-id="cc80c-752">0x00000011</span><span class="sxs-lookup"><span data-stu-id="cc80c-752">0x00000011</span></span> | <span data-ttu-id="cc80c-753">0x00000013</span><span class="sxs-lookup"><span data-stu-id="cc80c-753">0x00000013</span></span> | <span data-ttu-id="cc80c-754">0x00000017</span><span class="sxs-lookup"><span data-stu-id="cc80c-754">0x00000017</span></span> |



 

<span data-ttu-id="cc80c-755">Mithilfe des obigen Diagramms enthält vData die folgende Sequenz: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (zuerst die oberste Dimension durch iterieren und dann die nächste Dimension erhöhen).</span><span class="sxs-lookup"><span data-stu-id="cc80c-755">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="cc80c-756">Die vorangehende Rgsabound-Klasse (die cElements und Lbound auf zeichnet) wäre: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-756">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="cc80c-757">2.2.1.1.1.4 SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="cc80c-757">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="cc80c-758">Die SAFEARRAYBOUND-Struktur stellt die Grenzen einer Dimension von SAFEARRAY oder SAFEARRAY2 dar.</span><span class="sxs-lookup"><span data-stu-id="cc80c-758">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="cc80c-759">Das Format lautet:</span><span class="sxs-lookup"><span data-stu-id="cc80c-759">Its format is:</span></span>



<span data-ttu-id="cc80c-760">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-760">0</span></span>

<span data-ttu-id="cc80c-761">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-761">1</span></span>

<span data-ttu-id="cc80c-762">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-762">2</span></span>

<span data-ttu-id="cc80c-763">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-763">3</span></span>

<span data-ttu-id="cc80c-764">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-764">4</span></span>

<span data-ttu-id="cc80c-765">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-765">5</span></span>

<span data-ttu-id="cc80c-766">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-766">6</span></span>

<span data-ttu-id="cc80c-767">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-767">7</span></span>

<span data-ttu-id="cc80c-768">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-768">8</span></span>

<span data-ttu-id="cc80c-769">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-769">9</span></span>

<span data-ttu-id="cc80c-770">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-770">1</span></span><br/> <span data-ttu-id="cc80c-771">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-771">0</span></span><br/>

<span data-ttu-id="cc80c-772">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-772">1</span></span>

<span data-ttu-id="cc80c-773">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-773">2</span></span>

<span data-ttu-id="cc80c-774">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-774">3</span></span>

<span data-ttu-id="cc80c-775">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-775">4</span></span>

<span data-ttu-id="cc80c-776">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-776">5</span></span>

<span data-ttu-id="cc80c-777">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-777">6</span></span>

<span data-ttu-id="cc80c-778">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-778">7</span></span>

<span data-ttu-id="cc80c-779">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-779">8</span></span>

<span data-ttu-id="cc80c-780">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-780">9</span></span>

<span data-ttu-id="cc80c-781">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-781">2</span></span><br/> <span data-ttu-id="cc80c-782">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-782">0</span></span><br/>

<span data-ttu-id="cc80c-783">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-783">1</span></span>

<span data-ttu-id="cc80c-784">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-784">2</span></span>

<span data-ttu-id="cc80c-785">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-785">3</span></span>

<span data-ttu-id="cc80c-786">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-786">4</span></span>

<span data-ttu-id="cc80c-787">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-787">5</span></span>

<span data-ttu-id="cc80c-788">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-788">6</span></span>

<span data-ttu-id="cc80c-789">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-789">7</span></span>

<span data-ttu-id="cc80c-790">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-790">8</span></span>

<span data-ttu-id="cc80c-791">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-791">9</span></span>

<span data-ttu-id="cc80c-792">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-792">3</span></span><br/> <span data-ttu-id="cc80c-793">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-793">0</span></span><br/>

<span data-ttu-id="cc80c-794">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-794">1</span></span>

<span data-ttu-id="cc80c-795">cElements</span><span class="sxs-lookup"><span data-stu-id="cc80c-795">cElements</span></span>

<span data-ttu-id="cc80c-796">lLbound</span><span class="sxs-lookup"><span data-stu-id="cc80c-796">lLbound</span></span>



 

<span data-ttu-id="cc80c-797">**cElements:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente in der Dimension angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-797">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="cc80c-798">**lLbound:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die untere Grenze der Dimension angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-798">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="cc80c-799">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="cc80c-799">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="cc80c-800">SAFEARRAY2 wird verwendet, um mehrdimensionale Arrays in SERIALIZEDPROPERTYVALUE zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-800">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="cc80c-801">Die -Struktur enthält Sowohl Begrenzungsinformationen als auch die Daten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-801">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="cc80c-802">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-802">0</span></span>

<span data-ttu-id="cc80c-803">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-803">1</span></span>

<span data-ttu-id="cc80c-804">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-804">2</span></span>

<span data-ttu-id="cc80c-805">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-805">3</span></span>

<span data-ttu-id="cc80c-806">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-806">4</span></span>

<span data-ttu-id="cc80c-807">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-807">5</span></span>

<span data-ttu-id="cc80c-808">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-808">6</span></span>

<span data-ttu-id="cc80c-809">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-809">7</span></span>

<span data-ttu-id="cc80c-810">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-810">8</span></span>

<span data-ttu-id="cc80c-811">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-811">9</span></span>

<span data-ttu-id="cc80c-812">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-812">1</span></span><br/> <span data-ttu-id="cc80c-813">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-813">0</span></span><br/>

<span data-ttu-id="cc80c-814">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-814">1</span></span>

<span data-ttu-id="cc80c-815">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-815">2</span></span>

<span data-ttu-id="cc80c-816">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-816">3</span></span>

<span data-ttu-id="cc80c-817">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-817">4</span></span>

<span data-ttu-id="cc80c-818">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-818">5</span></span>

<span data-ttu-id="cc80c-819">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-819">6</span></span>

<span data-ttu-id="cc80c-820">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-820">7</span></span>

<span data-ttu-id="cc80c-821">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-821">8</span></span>

<span data-ttu-id="cc80c-822">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-822">9</span></span>

<span data-ttu-id="cc80c-823">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-823">2</span></span><br/> <span data-ttu-id="cc80c-824">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-824">0</span></span><br/>

<span data-ttu-id="cc80c-825">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-825">1</span></span>

<span data-ttu-id="cc80c-826">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-826">2</span></span>

<span data-ttu-id="cc80c-827">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-827">3</span></span>

<span data-ttu-id="cc80c-828">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-828">4</span></span>

<span data-ttu-id="cc80c-829">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-829">5</span></span>

<span data-ttu-id="cc80c-830">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-830">6</span></span>

<span data-ttu-id="cc80c-831">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-831">7</span></span>

<span data-ttu-id="cc80c-832">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-832">8</span></span>

<span data-ttu-id="cc80c-833">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-833">9</span></span>

<span data-ttu-id="cc80c-834">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-834">3</span></span><br/> <span data-ttu-id="cc80c-835">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-835">0</span></span><br/>

<span data-ttu-id="cc80c-836">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-836">1</span></span>

<span data-ttu-id="cc80c-837">cDims</span><span class="sxs-lookup"><span data-stu-id="cc80c-837">cDims</span></span>

<span data-ttu-id="cc80c-838">Rgsabound (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-838">Rgsabound (variable)</span></span>

<span data-ttu-id="cc80c-839">vData (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-839">vData (variable)</span></span>



 

<span data-ttu-id="cc80c-840">**cDims:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dimensionen von SAFEARRAY2 angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-840">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="cc80c-841">**Rgsabound:** Ein Array, das eine SAFEARRAYBOUND-Struktur enthält, wie in Abschnitt 2.2.1.1.1.4 pro Dimension in SAFEARRAY2 angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-841">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="cc80c-842">Dieses Array weist zuerst die äußerste linke dimension und zuletzt die rechte Dimension auf.</span><span class="sxs-lookup"><span data-stu-id="cc80c-842">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="cc80c-843">**vData:** Ein Vektor gemarshallter Elemente eines bestimmten Typs, der durch den dwType des enthaltenden SERIALIZEDPROPERTYVALUE angegeben wird, wobei bit 0x2000 gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-843">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="cc80c-844">Das Format von vData entspricht dem Format, das für das vData-Feld von SAFEARRAY in Abschnitt 2.2.1.1.1.3 angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="cc80c-844">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="cc80c-845">2.2.1.2 CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="cc80c-845">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="cc80c-846">Die CFullPropSpec-Struktur enthält eine Eigenschaftensatz-GUID und einen Eigenschaftenbezeichner, um die Eigenschaft eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cc80c-846">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="cc80c-847">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-847">0</span></span>

<span data-ttu-id="cc80c-848">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-848">1</span></span>

<span data-ttu-id="cc80c-849">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-849">2</span></span>

<span data-ttu-id="cc80c-850">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-850">3</span></span>

<span data-ttu-id="cc80c-851">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-851">4</span></span>

<span data-ttu-id="cc80c-852">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-852">5</span></span>

<span data-ttu-id="cc80c-853">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-853">6</span></span>

<span data-ttu-id="cc80c-854">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-854">7</span></span>

<span data-ttu-id="cc80c-855">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-855">8</span></span>

<span data-ttu-id="cc80c-856">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-856">9</span></span>

<span data-ttu-id="cc80c-857">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-857">1</span></span><br/> <span data-ttu-id="cc80c-858">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-858">0</span></span><br/>

<span data-ttu-id="cc80c-859">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-859">1</span></span>

<span data-ttu-id="cc80c-860">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-860">2</span></span>

<span data-ttu-id="cc80c-861">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-861">3</span></span>

<span data-ttu-id="cc80c-862">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-862">4</span></span>

<span data-ttu-id="cc80c-863">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-863">5</span></span>

<span data-ttu-id="cc80c-864">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-864">6</span></span>

<span data-ttu-id="cc80c-865">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-865">7</span></span>

<span data-ttu-id="cc80c-866">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-866">8</span></span>

<span data-ttu-id="cc80c-867">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-867">9</span></span>

<span data-ttu-id="cc80c-868">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-868">2</span></span><br/> <span data-ttu-id="cc80c-869">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-869">0</span></span><br/>

<span data-ttu-id="cc80c-870">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-870">1</span></span>

<span data-ttu-id="cc80c-871">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-871">2</span></span>

<span data-ttu-id="cc80c-872">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-872">3</span></span>

<span data-ttu-id="cc80c-873">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-873">4</span></span>

<span data-ttu-id="cc80c-874">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-874">5</span></span>

<span data-ttu-id="cc80c-875">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-875">6</span></span>

<span data-ttu-id="cc80c-876">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-876">7</span></span>

<span data-ttu-id="cc80c-877">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-877">8</span></span>

<span data-ttu-id="cc80c-878">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-878">9</span></span>

<span data-ttu-id="cc80c-879">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-879">3</span></span><br/> <span data-ttu-id="cc80c-880">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-880">0</span></span><br/>

<span data-ttu-id="cc80c-881">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-881">1</span></span>

<span data-ttu-id="cc80c-882">\_guidPropSet</span><span class="sxs-lookup"><span data-stu-id="cc80c-882">\_guidPropSet</span></span>

<span data-ttu-id="cc80c-883">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-883">...</span></span>

<span data-ttu-id="cc80c-884">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-884">...</span></span>

<span data-ttu-id="cc80c-885">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-885">...</span></span>

<span data-ttu-id="cc80c-886">ulKind</span><span class="sxs-lookup"><span data-stu-id="cc80c-886">ulKind</span></span>

<span data-ttu-id="cc80c-887">PrSpec</span><span class="sxs-lookup"><span data-stu-id="cc80c-887">PrSpec</span></span>

<span data-ttu-id="cc80c-888">Eigenschaftenname (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-888">Property name (variable)</span></span>



 

<span data-ttu-id="cc80c-889">**\_ guidPropSet:** Die GUID des Eigenschaftensets, zu dem die Eigenschaft gehört.</span><span class="sxs-lookup"><span data-stu-id="cc80c-889">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="cc80c-890">**ulKind:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-890">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cc80c-891">Einer der folgenden Werte unten, der den Inhalt von PrSpec angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-891">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="cc80c-892">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-892">Value</span></span>                                            | <span data-ttu-id="cc80c-893">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-893">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-894">PRSPEC \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="cc80c-894">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="cc80c-895">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-895">0x00000000</span></span><br/> | <span data-ttu-id="cc80c-896">Das PrSpec-Feld gibt die Anzahl von Zeichen ohne NULL im Feld Eigenschaftenname an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-896">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="cc80c-897">PRSPEC \_ PROPID</span><span class="sxs-lookup"><span data-stu-id="cc80c-897">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="cc80c-898">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-898">0x00000001</span></span><br/>  | <span data-ttu-id="cc80c-899">Das PrSpec-Feld gibt die Eigenschaften-ID (PROPID) an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-899">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="cc80c-900">**PrSpec:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, deren Bedeutung durch das ulKind-Feld angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-900">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="cc80c-901">**Eigenschaftenname:** Wenn ulKind auf PRSPEC PROPID festgelegt \_ ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-901">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="cc80c-902">Wenn ulKind auf PRSPEC LPWSTR festgelegt ist, MUSS dieses Feld ein Array von \_ Nicht-NULL-Unicode-Zeichen von PrSpec enthalten, das den Namen der Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-902">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="cc80c-903">2.2.1.3 CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-903">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="cc80c-904">Die CContentRestriction-Struktur enthält eine Zeichenfolge, die mit einer Eigenschaft im Eigenschaftencache übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-904">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="cc80c-905">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-905">0</span></span>

<span data-ttu-id="cc80c-906">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-906">1</span></span>

<span data-ttu-id="cc80c-907">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-907">2</span></span>

<span data-ttu-id="cc80c-908">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-908">3</span></span>

<span data-ttu-id="cc80c-909">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-909">4</span></span>

<span data-ttu-id="cc80c-910">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-910">5</span></span>

<span data-ttu-id="cc80c-911">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-911">6</span></span>

<span data-ttu-id="cc80c-912">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-912">7</span></span>

<span data-ttu-id="cc80c-913">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-913">8</span></span>

<span data-ttu-id="cc80c-914">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-914">9</span></span>

<span data-ttu-id="cc80c-915">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-915">1</span></span><br/> <span data-ttu-id="cc80c-916">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-916">0</span></span><br/>

<span data-ttu-id="cc80c-917">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-917">1</span></span>

<span data-ttu-id="cc80c-918">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-918">2</span></span>

<span data-ttu-id="cc80c-919">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-919">3</span></span>

<span data-ttu-id="cc80c-920">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-920">4</span></span>

<span data-ttu-id="cc80c-921">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-921">5</span></span>

<span data-ttu-id="cc80c-922">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-922">6</span></span>

<span data-ttu-id="cc80c-923">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-923">7</span></span>

<span data-ttu-id="cc80c-924">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-924">8</span></span>

<span data-ttu-id="cc80c-925">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-925">9</span></span>

<span data-ttu-id="cc80c-926">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-926">2</span></span><br/> <span data-ttu-id="cc80c-927">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-927">0</span></span><br/>

<span data-ttu-id="cc80c-928">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-928">1</span></span>

<span data-ttu-id="cc80c-929">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-929">2</span></span>

<span data-ttu-id="cc80c-930">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-930">3</span></span>

<span data-ttu-id="cc80c-931">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-931">4</span></span>

<span data-ttu-id="cc80c-932">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-932">5</span></span>

<span data-ttu-id="cc80c-933">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-933">6</span></span>

<span data-ttu-id="cc80c-934">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-934">7</span></span>

<span data-ttu-id="cc80c-935">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-935">8</span></span>

<span data-ttu-id="cc80c-936">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-936">9</span></span>

<span data-ttu-id="cc80c-937">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-937">3</span></span><br/> <span data-ttu-id="cc80c-938">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-938">0</span></span><br/>

<span data-ttu-id="cc80c-939">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-939">1</span></span>

<span data-ttu-id="cc80c-940">\_Eigenschaft (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-940">\_Property (variable)</span></span>

<span data-ttu-id="cc80c-941">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-941">...</span></span>

<span data-ttu-id="cc80c-942">Padding1 (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-942">Padding1 (variable)</span></span>

<span data-ttu-id="cc80c-943">Cc</span><span class="sxs-lookup"><span data-stu-id="cc80c-943">Cc</span></span>

<span data-ttu-id="cc80c-944">\_pwcsPhrase (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-944">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="cc80c-945">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-945">...</span></span>

<span data-ttu-id="cc80c-946">Padding2 (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-946">Padding2 (variable)</span></span>

<span data-ttu-id="cc80c-947">lcid</span><span class="sxs-lookup"><span data-stu-id="cc80c-947">lcid</span></span>

<span data-ttu-id="cc80c-948">\_ulGenerateMethod</span><span class="sxs-lookup"><span data-stu-id="cc80c-948">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="cc80c-949">**\_ Property:** Eine CFullPropSpec-Struktur, wie in Abschnitt 2.2.1.2 angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-949">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="cc80c-950">Dieses Feld gibt die Eigenschaft an, für die ein Übereinstimmungsvorgang ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-950">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="cc80c-951">**Padding1:** Dieses Feld MUSS 0 bis 3 Bytes lang sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-951">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cc80c-952">Die Länge dieses Felds MUSS so sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Bytes ab dem Anfang der Nachricht ist, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-952">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cc80c-953">Wenn dieses Feld vorhanden ist (d. h. die Länge ungleich null), ist der darin enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-953">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cc80c-954">Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-954">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cc80c-955">**Cc:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeichen im \_ PwcsPhrase-Feld angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-955">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="cc80c-956">**\_ pwcsPhrase:** Eine Nicht-NULL-terminierte Unicode-Zeichenfolge, die das Wort oder den Ausdruck darstellt, das bzw. der mit der -Eigenschaft übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-956">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="cc80c-957">Dieses Feld DARF NICHT leer sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-957">This field MUST NOT be empty.</span></span> <span data-ttu-id="cc80c-958">Das Feld Cc enthält die Länge der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cc80c-958">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="cc80c-959">**Auffüllen2:** Dieses Feld MUSS 0 bis 3 Bytes lang sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-959">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cc80c-960">Die Länge dieses Felds MUSS so sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Bytes ab dem Anfang der Nachricht ist, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-960">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cc80c-961">Wenn dieses Feld vorhanden ist (d. h. die Länge ungleich null), ist der darin enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-961">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cc80c-962">Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-962">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cc80c-963">**Lcid:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Gebietsschema von \_ pwcsPhrase angibt, wie in ANHANG A von \[ MS-GPSI \] angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-963">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="cc80c-964">**\_ ulGenerateMethod:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Methode angibt, die beim Generieren alternativer Wortformen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-964">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="cc80c-965">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-965">Value</span></span>                                                       | <span data-ttu-id="cc80c-966">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-966">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-967">GENERATE \_ METHOD \_ EXACT</span><span class="sxs-lookup"><span data-stu-id="cc80c-967">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="cc80c-968">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-968">0x00000000</span></span><br/>    | <span data-ttu-id="cc80c-969">Genaue Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="cc80c-969">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="cc80c-970">GENERIEREN \_ DES \_ METHODENPRÄFIXES</span><span class="sxs-lookup"><span data-stu-id="cc80c-970">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="cc80c-971">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-971">0x00000001</span></span> <br/>  | <span data-ttu-id="cc80c-972">Präfixübersprechung.</span><span class="sxs-lookup"><span data-stu-id="cc80c-972">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="cc80c-973">GENERATE \_ METHOD \_ INFLECT</span><span class="sxs-lookup"><span data-stu-id="cc80c-973">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="cc80c-974">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-974">0x00000002</span></span><br/> | <span data-ttu-id="cc80c-975">Entspricht den Flexionen eines Worts.</span><span class="sxs-lookup"><span data-stu-id="cc80c-975">Matches inflections of a word.</span></span> <span data-ttu-id="cc80c-976">Eine Inflection eines Worts ist eine Variante des Stammworts im gleichen Sprachteil, der gemäß linguistischen Regeln einer bestimmten Sprache geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="cc80c-976">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="cc80c-977">Beispiele für die Inflectionen des Verbs "swim" auf Englisch sind "swim", "swims", "pools" und "swam".</span><span class="sxs-lookup"><span data-stu-id="cc80c-977">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="cc80c-978">2.2.1.4 CKey</span><span class="sxs-lookup"><span data-stu-id="cc80c-978">2.2.1.4 CKey</span></span>

<span data-ttu-id="cc80c-979">Die CKey-Struktur enthält einen Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-979">The CKey structure contains a property value.</span></span>



<span data-ttu-id="cc80c-980">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-980">0</span></span>

<span data-ttu-id="cc80c-981">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-981">1</span></span>

<span data-ttu-id="cc80c-982">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-982">2</span></span>

<span data-ttu-id="cc80c-983">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-983">3</span></span>

<span data-ttu-id="cc80c-984">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-984">4</span></span>

<span data-ttu-id="cc80c-985">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-985">5</span></span>

<span data-ttu-id="cc80c-986">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-986">6</span></span>

<span data-ttu-id="cc80c-987">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-987">7</span></span>

<span data-ttu-id="cc80c-988">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-988">8</span></span>

<span data-ttu-id="cc80c-989">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-989">9</span></span>

<span data-ttu-id="cc80c-990">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-990">1</span></span><br/> <span data-ttu-id="cc80c-991">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-991">0</span></span><br/>

<span data-ttu-id="cc80c-992">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-992">1</span></span>

<span data-ttu-id="cc80c-993">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-993">2</span></span>

<span data-ttu-id="cc80c-994">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-994">3</span></span>

<span data-ttu-id="cc80c-995">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-995">4</span></span>

<span data-ttu-id="cc80c-996">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-996">5</span></span>

<span data-ttu-id="cc80c-997">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-997">6</span></span>

<span data-ttu-id="cc80c-998">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-998">7</span></span>

<span data-ttu-id="cc80c-999">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-999">8</span></span>

<span data-ttu-id="cc80c-1000">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1000">9</span></span>

<span data-ttu-id="cc80c-1001">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1001">2</span></span><br/> <span data-ttu-id="cc80c-1002">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1002">0</span></span><br/>

<span data-ttu-id="cc80c-1003">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1003">1</span></span>

<span data-ttu-id="cc80c-1004">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1004">2</span></span>

<span data-ttu-id="cc80c-1005">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1005">3</span></span>

<span data-ttu-id="cc80c-1006">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1006">4</span></span>

<span data-ttu-id="cc80c-1007">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1007">5</span></span>

<span data-ttu-id="cc80c-1008">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1008">6</span></span>

<span data-ttu-id="cc80c-1009">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1009">7</span></span>

<span data-ttu-id="cc80c-1010">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1010">8</span></span>

<span data-ttu-id="cc80c-1011">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1011">9</span></span>

<span data-ttu-id="cc80c-1012">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1012">3</span></span><br/> <span data-ttu-id="cc80c-1013">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1013">0</span></span><br/>

<span data-ttu-id="cc80c-1014">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1014">1</span></span>

<span data-ttu-id="cc80c-1015">PROPID</span><span class="sxs-lookup"><span data-stu-id="cc80c-1015">PROPID</span></span>

<span data-ttu-id="cc80c-1016">Cb</span><span class="sxs-lookup"><span data-stu-id="cc80c-1016">Cb</span></span>

<span data-ttu-id="cc80c-1017">buf (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1017">buf (variable)</span></span>



 

<span data-ttu-id="cc80c-1018">**PROPID:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Eigenschaften-ID darstellt, wie in Abschnitt 1.8.1 erläutert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1018">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="cc80c-1019">Bekannte Werte sind:</span><span class="sxs-lookup"><span data-stu-id="cc80c-1019">Well-known values are:</span></span>



| <span data-ttu-id="cc80c-1020">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-1020">Value</span></span>      | <span data-ttu-id="cc80c-1021">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-1021">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="cc80c-1022">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="cc80c-1022">0xFFFFFFFF</span></span> | <span data-ttu-id="cc80c-1023">Stellt eine ungültige Eigenschaften-ID dar und DARF NICHT verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1023">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="cc80c-1024">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="cc80c-1024">0xFFFFFFFE</span></span> | <span data-ttu-id="cc80c-1025">Stellt eine ungültige Eigenschaften-ID dar und DARF NICHT verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1025">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="cc80c-1026">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-1026">0x00000000</span></span> | <span data-ttu-id="cc80c-1027">Stellt eine beliebige Eigenschaften-ID dar.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1027">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="cc80c-1028">**Cb:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge von buf in Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1028">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="cc80c-1029">**buf:** Eine Bytesequenz, die den Wert der -Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1029">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="cc80c-1030">2.2.1.5 CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-1030">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="cc80c-1031">Die CInternalPropertyRestriction-Struktur enthält einen Eigenschaftswert, der mit einem Vorgang übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1031">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="cc80c-1032">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1032">0</span></span>

<span data-ttu-id="cc80c-1033">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1033">1</span></span>

<span data-ttu-id="cc80c-1034">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1034">2</span></span>

<span data-ttu-id="cc80c-1035">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1035">3</span></span>

<span data-ttu-id="cc80c-1036">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1036">4</span></span>

<span data-ttu-id="cc80c-1037">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1037">5</span></span>

<span data-ttu-id="cc80c-1038">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1038">6</span></span>

<span data-ttu-id="cc80c-1039">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1039">7</span></span>

<span data-ttu-id="cc80c-1040">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1040">8</span></span>

<span data-ttu-id="cc80c-1041">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1041">9</span></span>

<span data-ttu-id="cc80c-1042">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1042">1</span></span><br/> <span data-ttu-id="cc80c-1043">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1043">0</span></span><br/>

<span data-ttu-id="cc80c-1044">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1044">1</span></span>

<span data-ttu-id="cc80c-1045">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1045">2</span></span>

<span data-ttu-id="cc80c-1046">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1046">3</span></span>

<span data-ttu-id="cc80c-1047">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1047">4</span></span>

<span data-ttu-id="cc80c-1048">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1048">5</span></span>

<span data-ttu-id="cc80c-1049">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1049">6</span></span>

<span data-ttu-id="cc80c-1050">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1050">7</span></span>

<span data-ttu-id="cc80c-1051">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1051">8</span></span>

<span data-ttu-id="cc80c-1052">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1052">9</span></span>

<span data-ttu-id="cc80c-1053">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1053">2</span></span><br/> <span data-ttu-id="cc80c-1054">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1054">0</span></span><br/>

<span data-ttu-id="cc80c-1055">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1055">1</span></span>

<span data-ttu-id="cc80c-1056">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1056">2</span></span>

<span data-ttu-id="cc80c-1057">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1057">3</span></span>

<span data-ttu-id="cc80c-1058">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1058">4</span></span>

<span data-ttu-id="cc80c-1059">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1059">5</span></span>

<span data-ttu-id="cc80c-1060">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1060">6</span></span>

<span data-ttu-id="cc80c-1061">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1061">7</span></span>

<span data-ttu-id="cc80c-1062">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1062">8</span></span>

<span data-ttu-id="cc80c-1063">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1063">9</span></span>

<span data-ttu-id="cc80c-1064">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1064">3</span></span><br/> <span data-ttu-id="cc80c-1065">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1065">0</span></span><br/>

<span data-ttu-id="cc80c-1066">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1066">1</span></span>

<span data-ttu-id="cc80c-1067">\_relop</span><span class="sxs-lookup"><span data-stu-id="cc80c-1067">\_relop</span></span>

<span data-ttu-id="cc80c-1068">\_Pid</span><span class="sxs-lookup"><span data-stu-id="cc80c-1068">\_pid</span></span>

<span data-ttu-id="cc80c-1069">\_prval (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1069">\_prval (variable)</span></span>

<span data-ttu-id="cc80c-1070">restrictionPresent</span><span class="sxs-lookup"><span data-stu-id="cc80c-1070">restrictionPresent</span></span>

<span data-ttu-id="cc80c-1071">nextRestriction (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1071">nextRestriction (variable)</span></span>



 

<span data-ttu-id="cc80c-1072">**\_ relop**: Eine 32-Bit-Ganzzahl, die die Beziehung angibt, die für die -Eigenschaft ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1072">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="cc80c-1073">MUSS einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="cc80c-1073">MUST be one of the following values:</span></span>



| <span data-ttu-id="cc80c-1074">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-1074">Value</span></span>                 | <span data-ttu-id="cc80c-1075">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-1075">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-1076">PRLT-0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-1076">PRLT 0x00000000</span></span>       | <span data-ttu-id="cc80c-1077">Ein Kleiner-als-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1077">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="cc80c-1078">PRLE-0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-1078">PRLE 0x00000001</span></span>       | <span data-ttu-id="cc80c-1079">Ein Kleiner-als- oder Gleich-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1079">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="cc80c-1080">PRGT-0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-1080">PRGT 0x00000002</span></span>       | <span data-ttu-id="cc80c-1081">Ein Größer-als-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1081">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="cc80c-1082">PRGE-0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-1082">PRGE 0x00000003</span></span>       | <span data-ttu-id="cc80c-1083">Ein Größer-als- oder Gleich-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1083">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="cc80c-1084">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cc80c-1084">PREQ 0x00000004</span></span>       | <span data-ttu-id="cc80c-1085">Ein Gleichheitsvergleich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1085">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="cc80c-1086">PRNE-0x00000005</span><span class="sxs-lookup"><span data-stu-id="cc80c-1086">PRNE 0x00000005</span></span>       | <span data-ttu-id="cc80c-1087">Ein ungleicher Vergleich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1087">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="cc80c-1088">PRRE-0x00000006</span><span class="sxs-lookup"><span data-stu-id="cc80c-1088">PRRE 0x00000006</span></span>       | <span data-ttu-id="cc80c-1089">Ein Vergleich eines regulären Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1089">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="cc80c-1090">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="cc80c-1090">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="cc80c-1091">Ein bitweises AND, das den rechten Operanden zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1091">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="cc80c-1092">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cc80c-1092">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="cc80c-1093">Ein bitweises AND, das einen Wert ungleich 0 (null) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1093">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="cc80c-1094">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="cc80c-1094">PRAll 0x00000100</span></span>      | <span data-ttu-id="cc80c-1095">Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden und ist nur true, wenn der Vorgang für alle Zeilen true ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1095">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="cc80c-1096">PRAny-0x00000200</span><span class="sxs-lookup"><span data-stu-id="cc80c-1096">PRAny 0x00000200</span></span>      | <span data-ttu-id="cc80c-1097">Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden, und ist TRUE, wenn der Vorgang für eine zeile true ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1097">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="cc80c-1098">**\_ pid:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Eigenschaften-ID darstellt (siehe PROPID in Abschnitt 2.2.1.4).</span><span class="sxs-lookup"><span data-stu-id="cc80c-1098">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="cc80c-1099">**\_ prval:** Eine CBaseStorageVariant mit dem Wert, der mit der Eigenschaft in Beziehung stehen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1099">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="cc80c-1100">**restrictionPresent:** Ein Bytewert, der angibt, ob das NextRestriction-Feld vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1100">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="cc80c-1101">MUSS entweder auf 0x00 oder 0x01.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1101">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="cc80c-1102">Wenn sie auf 0x01, gibt restrictionPresent an, dass das Feld nextRestriction vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1102">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="cc80c-1103">Wenn sie auf 0x00, gibt restrictionPresent an, dass das Feld nextRestriction nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1103">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="cc80c-1104">**nextRestriction:** Eine CRestriction-Struktur, wie in Abschnitt 2.2.1.16 angegeben und gibt eine weitere Einschränkung an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1104">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="cc80c-1105">2.2.1.6 CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-1105">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="cc80c-1106">Die CNatLanguageRestriction-Struktur enthält **eine** Abfrage in natürlicher Sprache für eine Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1106">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="cc80c-1107">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1107">0</span></span>

<span data-ttu-id="cc80c-1108">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1108">1</span></span>

<span data-ttu-id="cc80c-1109">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1109">2</span></span>

<span data-ttu-id="cc80c-1110">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1110">3</span></span>

<span data-ttu-id="cc80c-1111">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1111">4</span></span>

<span data-ttu-id="cc80c-1112">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1112">5</span></span>

<span data-ttu-id="cc80c-1113">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1113">6</span></span>

<span data-ttu-id="cc80c-1114">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1114">7</span></span>

<span data-ttu-id="cc80c-1115">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1115">8</span></span>

<span data-ttu-id="cc80c-1116">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1116">9</span></span>

<span data-ttu-id="cc80c-1117">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1117">1</span></span><br/> <span data-ttu-id="cc80c-1118">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1118">0</span></span><br/>

<span data-ttu-id="cc80c-1119">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1119">1</span></span>

<span data-ttu-id="cc80c-1120">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1120">2</span></span>

<span data-ttu-id="cc80c-1121">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1121">3</span></span>

<span data-ttu-id="cc80c-1122">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1122">4</span></span>

<span data-ttu-id="cc80c-1123">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1123">5</span></span>

<span data-ttu-id="cc80c-1124">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1124">6</span></span>

<span data-ttu-id="cc80c-1125">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1125">7</span></span>

<span data-ttu-id="cc80c-1126">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1126">8</span></span>

<span data-ttu-id="cc80c-1127">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1127">9</span></span>

<span data-ttu-id="cc80c-1128">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1128">2</span></span><br/> <span data-ttu-id="cc80c-1129">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1129">0</span></span><br/>

<span data-ttu-id="cc80c-1130">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1130">1</span></span>

<span data-ttu-id="cc80c-1131">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1131">2</span></span>

<span data-ttu-id="cc80c-1132">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1132">3</span></span>

<span data-ttu-id="cc80c-1133">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1133">4</span></span>

<span data-ttu-id="cc80c-1134">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1134">5</span></span>

<span data-ttu-id="cc80c-1135">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1135">6</span></span>

<span data-ttu-id="cc80c-1136">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1136">7</span></span>

<span data-ttu-id="cc80c-1137">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1137">8</span></span>

<span data-ttu-id="cc80c-1138">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1138">9</span></span>

<span data-ttu-id="cc80c-1139">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1139">3</span></span><br/> <span data-ttu-id="cc80c-1140">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1140">0</span></span><br/>

<span data-ttu-id="cc80c-1141">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1141">1</span></span>

<span data-ttu-id="cc80c-1142">\_Eigenschaft (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1142">\_Property (variable)</span></span>

<span data-ttu-id="cc80c-1143">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-1143">...</span></span>

<span data-ttu-id="cc80c-1144">\_Auf padding \_ cc (variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1144">\_padding\_cc (variable)</span></span>

<span data-ttu-id="cc80c-1145">Cc</span><span class="sxs-lookup"><span data-stu-id="cc80c-1145">Cc</span></span>

<span data-ttu-id="cc80c-1146">\_pwcsPhrase (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1146">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="cc80c-1147">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-1147">...</span></span>

<span data-ttu-id="cc80c-1148">\_Auf padding \_ lcid (variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1148">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="cc80c-1149">Lcid</span><span class="sxs-lookup"><span data-stu-id="cc80c-1149">Lcid</span></span>



 

<span data-ttu-id="cc80c-1150">**\_ Property:** Eine CFullPropSpec-Struktur, wie in Abschnitt 2.2.1.3 angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1150">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="cc80c-1151">Dieses Feld gibt die Eigenschaft an, für die der Übereinstimmungsvorgang ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1151">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="cc80c-1152">**\_ auffüllen \_ von cc:** Dieses Feld MUSS 0 bis 3 Bytes lang sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1152">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cc80c-1153">Die Länge dieses Felds MUSS so sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Bytes ab dem Anfang der Nachricht ist, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1153">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cc80c-1154">Wenn dieses Feld vorhanden ist (d. h. die Länge ungleich null), ist der darin enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1154">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cc80c-1155">Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1155">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cc80c-1156">**Cc:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1156">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cc80c-1157">Die Anzahl der Zeichen im \_ PwcsPhrase-Feld.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1157">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="cc80c-1158">**\_ pwcsPhrase:** Eine Nicht-NULL-terminierte Unicode-Zeichenfolge, die das Wort oder den Ausdruck darstellt, das bzw. der mit der -Eigenschaft übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1158">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="cc80c-1159">DARF NICHT leer sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1159">MUST NOT be empty.</span></span> <span data-ttu-id="cc80c-1160">Das Feld Cc enthält die Länge der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1160">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="cc80c-1161">**\_ padding \_ lcid**: Dieses Feld MUSS 0 bis 3 Bytes lang sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1161">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cc80c-1162">Die Länge dieses Felds MUSS so sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Bytes ab dem Anfang der Nachricht ist, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1162">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cc80c-1163">Wenn dieses Feld vorhanden ist (d. h. die Länge ungleich null), ist der darin enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1163">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cc80c-1164">Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1164">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cc80c-1165">**Lcid:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Gebietsschema von \_ pwcsPhrase angibt, wie in ANHANG A von \[ MS-GPSI \] angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1165">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="cc80c-1166">2.2.1.7 CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-1166">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="cc80c-1167">Die CNodeRestriction-Struktur enthält ein Array von **Befehlsstrukturknoten,** die die Einschränkungen für die Abfrage angeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1167">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="cc80c-1168">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1168">0</span></span>

<span data-ttu-id="cc80c-1169">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1169">1</span></span>

<span data-ttu-id="cc80c-1170">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1170">2</span></span>

<span data-ttu-id="cc80c-1171">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1171">3</span></span>

<span data-ttu-id="cc80c-1172">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1172">4</span></span>

<span data-ttu-id="cc80c-1173">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1173">5</span></span>

<span data-ttu-id="cc80c-1174">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1174">6</span></span>

<span data-ttu-id="cc80c-1175">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1175">7</span></span>

<span data-ttu-id="cc80c-1176">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1176">8</span></span>

<span data-ttu-id="cc80c-1177">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1177">9</span></span>

<span data-ttu-id="cc80c-1178">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1178">1</span></span><br/> <span data-ttu-id="cc80c-1179">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1179">0</span></span><br/>

<span data-ttu-id="cc80c-1180">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1180">1</span></span>

<span data-ttu-id="cc80c-1181">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1181">2</span></span>

<span data-ttu-id="cc80c-1182">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1182">3</span></span>

<span data-ttu-id="cc80c-1183">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1183">4</span></span>

<span data-ttu-id="cc80c-1184">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1184">5</span></span>

<span data-ttu-id="cc80c-1185">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1185">6</span></span>

<span data-ttu-id="cc80c-1186">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1186">7</span></span>

<span data-ttu-id="cc80c-1187">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1187">8</span></span>

<span data-ttu-id="cc80c-1188">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1188">9</span></span>

<span data-ttu-id="cc80c-1189">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1189">2</span></span><br/> <span data-ttu-id="cc80c-1190">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1190">0</span></span><br/>

<span data-ttu-id="cc80c-1191">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1191">1</span></span>

<span data-ttu-id="cc80c-1192">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1192">2</span></span>

<span data-ttu-id="cc80c-1193">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1193">3</span></span>

<span data-ttu-id="cc80c-1194">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1194">4</span></span>

<span data-ttu-id="cc80c-1195">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1195">5</span></span>

<span data-ttu-id="cc80c-1196">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1196">6</span></span>

<span data-ttu-id="cc80c-1197">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1197">7</span></span>

<span data-ttu-id="cc80c-1198">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1198">8</span></span>

<span data-ttu-id="cc80c-1199">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1199">9</span></span>

<span data-ttu-id="cc80c-1200">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1200">3</span></span><br/> <span data-ttu-id="cc80c-1201">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1201">0</span></span><br/>

<span data-ttu-id="cc80c-1202">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1202">1</span></span>

<span data-ttu-id="cc80c-1203">\_cNode</span><span class="sxs-lookup"><span data-stu-id="cc80c-1203">\_cNode</span></span>

<span data-ttu-id="cc80c-1204">\_paNode (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1204">\_paNode (variable)</span></span>



 

<span data-ttu-id="cc80c-1205">**\_ cNode:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der im PaNode-Feld enthaltenen CRestriction-Strukturen \_ angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1205">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="cc80c-1206">**\_ paNode:** Ein Array von CRestriction-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1206">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="cc80c-1207">Strukturen im Array MÜSSEN durch 0 bis 3 Auf abstandsbytes getrennt werden, damit jede Struktur an einem Offset beginnt, der ein Vielfaches von 4 Bytes vom Anfang der Nachricht ist, die dieses Array enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1207">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="cc80c-1208">Wenn Auf padding bytes vorhanden sind, ist der Wert, den sie enthalten, willkürlich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1208">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="cc80c-1209">Der Inhalt der Auf padding-Bytes MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1209">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="cc80c-1210">2.2.1.8 COccRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-1210">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="cc80c-1211">Die COccRestriction-Struktur enthält die Position eines Worts in einem Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1211">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="cc80c-1212">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1212">0</span></span>

<span data-ttu-id="cc80c-1213">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1213">1</span></span>

<span data-ttu-id="cc80c-1214">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1214">2</span></span>

<span data-ttu-id="cc80c-1215">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1215">3</span></span>

<span data-ttu-id="cc80c-1216">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1216">4</span></span>

<span data-ttu-id="cc80c-1217">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1217">5</span></span>

<span data-ttu-id="cc80c-1218">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1218">6</span></span>

<span data-ttu-id="cc80c-1219">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1219">7</span></span>

<span data-ttu-id="cc80c-1220">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1220">8</span></span>

<span data-ttu-id="cc80c-1221">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1221">9</span></span>

<span data-ttu-id="cc80c-1222">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1222">1</span></span><br/> <span data-ttu-id="cc80c-1223">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1223">0</span></span><br/>

<span data-ttu-id="cc80c-1224">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1224">1</span></span>

<span data-ttu-id="cc80c-1225">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1225">2</span></span>

<span data-ttu-id="cc80c-1226">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1226">3</span></span>

<span data-ttu-id="cc80c-1227">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1227">4</span></span>

<span data-ttu-id="cc80c-1228">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1228">5</span></span>

<span data-ttu-id="cc80c-1229">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1229">6</span></span>

<span data-ttu-id="cc80c-1230">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1230">7</span></span>

<span data-ttu-id="cc80c-1231">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1231">8</span></span>

<span data-ttu-id="cc80c-1232">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1232">9</span></span>

<span data-ttu-id="cc80c-1233">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1233">2</span></span><br/> <span data-ttu-id="cc80c-1234">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1234">0</span></span><br/>

<span data-ttu-id="cc80c-1235">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1235">1</span></span>

<span data-ttu-id="cc80c-1236">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1236">2</span></span>

<span data-ttu-id="cc80c-1237">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1237">3</span></span>

<span data-ttu-id="cc80c-1238">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1238">4</span></span>

<span data-ttu-id="cc80c-1239">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1239">5</span></span>

<span data-ttu-id="cc80c-1240">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1240">6</span></span>

<span data-ttu-id="cc80c-1241">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1241">7</span></span>

<span data-ttu-id="cc80c-1242">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1242">8</span></span>

<span data-ttu-id="cc80c-1243">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1243">9</span></span>

<span data-ttu-id="cc80c-1244">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1244">3</span></span><br/> <span data-ttu-id="cc80c-1245">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1245">0</span></span><br/>

<span data-ttu-id="cc80c-1246">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1246">1</span></span>

<span data-ttu-id="cc80c-1247">\_Occ</span><span class="sxs-lookup"><span data-stu-id="cc80c-1247">\_occ</span></span>

<span data-ttu-id="cc80c-1248">\_cPrevNoiseWords</span><span class="sxs-lookup"><span data-stu-id="cc80c-1248">\_cPrevNoiseWords</span></span>

<span data-ttu-id="cc80c-1249">\_cNextNoiseWords</span><span class="sxs-lookup"><span data-stu-id="cc80c-1249">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="cc80c-1250">**\_ occ:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Offset des Worts in einer Abfragezeichenfolge in Worteinheiten angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1250">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="cc80c-1251">Ein Wort, wie es in dieser Spezifikation verwendet wird, ist eine Spracheinheit in jedem Beliebigen, das eine Bedeutung hat.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1251">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="cc80c-1252">**\_ cPrevNoiseWords:** Eine 32-Bit-Ganzzahl ohne  Vorzeichen, die die Anzahl der Rauschwörter enthält, die zwischen diesem Wort und dem vorherigen Wort im Ausdruck auftreten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1252">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="cc80c-1253">**\_ cNextNoiseWords:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Rauschwörter enthält, die zwischen diesem Wort und dem nächsten Wort im Ausdruck auftreten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1253">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="cc80c-1254">2.2.1.9 CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-1254">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="cc80c-1255">Die CPropertyRestriction-Struktur enthält einen Eigenschaftswert, der mit einem Vorgang übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1255">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="cc80c-1256">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1256">0</span></span>

<span data-ttu-id="cc80c-1257">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1257">1</span></span>

<span data-ttu-id="cc80c-1258">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1258">2</span></span>

<span data-ttu-id="cc80c-1259">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1259">3</span></span>

<span data-ttu-id="cc80c-1260">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1260">4</span></span>

<span data-ttu-id="cc80c-1261">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1261">5</span></span>

<span data-ttu-id="cc80c-1262">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1262">6</span></span>

<span data-ttu-id="cc80c-1263">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1263">7</span></span>

<span data-ttu-id="cc80c-1264">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1264">8</span></span>

<span data-ttu-id="cc80c-1265">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1265">9</span></span>

<span data-ttu-id="cc80c-1266">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1266">1</span></span><br/> <span data-ttu-id="cc80c-1267">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1267">0</span></span><br/>

<span data-ttu-id="cc80c-1268">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1268">1</span></span>

<span data-ttu-id="cc80c-1269">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1269">2</span></span>

<span data-ttu-id="cc80c-1270">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1270">3</span></span>

<span data-ttu-id="cc80c-1271">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1271">4</span></span>

<span data-ttu-id="cc80c-1272">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1272">5</span></span>

<span data-ttu-id="cc80c-1273">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1273">6</span></span>

<span data-ttu-id="cc80c-1274">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1274">7</span></span>

<span data-ttu-id="cc80c-1275">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1275">8</span></span>

<span data-ttu-id="cc80c-1276">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1276">9</span></span>

<span data-ttu-id="cc80c-1277">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1277">2</span></span><br/> <span data-ttu-id="cc80c-1278">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1278">0</span></span><br/>

<span data-ttu-id="cc80c-1279">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1279">1</span></span>

<span data-ttu-id="cc80c-1280">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1280">2</span></span>

<span data-ttu-id="cc80c-1281">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1281">3</span></span>

<span data-ttu-id="cc80c-1282">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1282">4</span></span>

<span data-ttu-id="cc80c-1283">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1283">5</span></span>

<span data-ttu-id="cc80c-1284">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1284">6</span></span>

<span data-ttu-id="cc80c-1285">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1285">7</span></span>

<span data-ttu-id="cc80c-1286">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1286">8</span></span>

<span data-ttu-id="cc80c-1287">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1287">9</span></span>

<span data-ttu-id="cc80c-1288">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1288">3</span></span><br/> <span data-ttu-id="cc80c-1289">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1289">0</span></span><br/>

<span data-ttu-id="cc80c-1290">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1290">1</span></span>

<span data-ttu-id="cc80c-1291">\_relop</span><span class="sxs-lookup"><span data-stu-id="cc80c-1291">\_relop</span></span>

<span data-ttu-id="cc80c-1292">\_Eigenschaft (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1292">\_Property (variable)</span></span>

<span data-ttu-id="cc80c-1293">\_prval (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1293">\_prval (variable)</span></span>



 

<span data-ttu-id="cc80c-1294">**\_ relop:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Beziehung angibt, die für die -Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1294">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="cc80c-1295">MUSS einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1295">MUST be one of the following values.</span></span>



| <span data-ttu-id="cc80c-1296">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-1296">Value</span></span>                 | <span data-ttu-id="cc80c-1297">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-1297">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-1298">PRLT-0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-1298">PRLT 0x00000000</span></span>       | <span data-ttu-id="cc80c-1299">Ein Kleiner-als-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1299">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="cc80c-1300">PRLE-0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-1300">PRLE 0x00000001</span></span>       | <span data-ttu-id="cc80c-1301">Ein Kleiner-als- oder Gleich-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1301">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="cc80c-1302">PRGT-0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-1302">PRGT 0x00000002</span></span>       | <span data-ttu-id="cc80c-1303">Ein Größer-als-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1303">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="cc80c-1304">PRGE-0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-1304">PRGE 0x00000003</span></span>       | <span data-ttu-id="cc80c-1305">Ein Größer-als- oder Gleich-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1305">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="cc80c-1306">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cc80c-1306">PREQ 0x00000004</span></span>       | <span data-ttu-id="cc80c-1307">Ein Gleichheitsvergleich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1307">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="cc80c-1308">PRNE-0x00000005</span><span class="sxs-lookup"><span data-stu-id="cc80c-1308">PRNE 0x00000005</span></span>       | <span data-ttu-id="cc80c-1309">Ein ungleicher Vergleich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1309">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="cc80c-1310">PRRE-0x00000006</span><span class="sxs-lookup"><span data-stu-id="cc80c-1310">PRRE 0x00000006</span></span>       | <span data-ttu-id="cc80c-1311">Ein Vergleich eines regulären Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1311">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="cc80c-1312">PRAllBits-0x00000007</span><span class="sxs-lookup"><span data-stu-id="cc80c-1312">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="cc80c-1313">Ein bitweises AND, das den rechten Operanden zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1313">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="cc80c-1314">PRSomeBits-0x00000008</span><span class="sxs-lookup"><span data-stu-id="cc80c-1314">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="cc80c-1315">Ein bitweises AND, das einen Wert ungleich 0 (null) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1315">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="cc80c-1316">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="cc80c-1316">PRAll 0x00000100</span></span>      | <span data-ttu-id="cc80c-1317">Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden und ist nur true, wenn der Vorgang für alle Zeilen true ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1317">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="cc80c-1318">PRAny-0x00000200</span><span class="sxs-lookup"><span data-stu-id="cc80c-1318">PRAny 0x00000200</span></span>      | <span data-ttu-id="cc80c-1319">Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden, und ist TRUE, wenn der Vorgang für eine zeile true ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1319">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="cc80c-1320">**\_ Eigenschaft:** Eine CFullPropSpec-Struktur, wie in Abschnitt 2.2.1.2 angegeben, die die Eigenschaft angibt, für die ein Übereinstimmungsvorgang durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1320">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="cc80c-1321">**\_ prval:** Eine CBaseStorageVariant-Struktur, wie in Abschnitt 2.2.1.1 angegeben, die den Wert enthält, der mit der Eigenschaft in Beziehung stehen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1321">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="cc80c-1322">2.2.1.10 CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-1322">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="cc80c-1323">Die CRangeRestriction-Struktur enthält eine Einschränkung für einen Bereich von Werten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1323">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="cc80c-1324">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1324">0</span></span>

<span data-ttu-id="cc80c-1325">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1325">1</span></span>

<span data-ttu-id="cc80c-1326">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1326">2</span></span>

<span data-ttu-id="cc80c-1327">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1327">3</span></span>

<span data-ttu-id="cc80c-1328">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1328">4</span></span>

<span data-ttu-id="cc80c-1329">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1329">5</span></span>

<span data-ttu-id="cc80c-1330">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1330">6</span></span>

<span data-ttu-id="cc80c-1331">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1331">7</span></span>

<span data-ttu-id="cc80c-1332">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1332">8</span></span>

<span data-ttu-id="cc80c-1333">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1333">9</span></span>

<span data-ttu-id="cc80c-1334">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1334">1</span></span><br/> <span data-ttu-id="cc80c-1335">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1335">0</span></span><br/>

<span data-ttu-id="cc80c-1336">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1336">1</span></span>

<span data-ttu-id="cc80c-1337">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1337">2</span></span>

<span data-ttu-id="cc80c-1338">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1338">3</span></span>

<span data-ttu-id="cc80c-1339">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1339">4</span></span>

<span data-ttu-id="cc80c-1340">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1340">5</span></span>

<span data-ttu-id="cc80c-1341">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1341">6</span></span>

<span data-ttu-id="cc80c-1342">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1342">7</span></span>

<span data-ttu-id="cc80c-1343">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1343">8</span></span>

<span data-ttu-id="cc80c-1344">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1344">9</span></span>

<span data-ttu-id="cc80c-1345">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1345">2</span></span><br/> <span data-ttu-id="cc80c-1346">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1346">0</span></span><br/>

<span data-ttu-id="cc80c-1347">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1347">1</span></span>

<span data-ttu-id="cc80c-1348">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1348">2</span></span>

<span data-ttu-id="cc80c-1349">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1349">3</span></span>

<span data-ttu-id="cc80c-1350">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1350">4</span></span>

<span data-ttu-id="cc80c-1351">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1351">5</span></span>

<span data-ttu-id="cc80c-1352">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1352">6</span></span>

<span data-ttu-id="cc80c-1353">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1353">7</span></span>

<span data-ttu-id="cc80c-1354">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1354">8</span></span>

<span data-ttu-id="cc80c-1355">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1355">9</span></span>

<span data-ttu-id="cc80c-1356">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1356">3</span></span><br/> <span data-ttu-id="cc80c-1357">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1357">0</span></span><br/>

<span data-ttu-id="cc80c-1358">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1358">1</span></span>

<span data-ttu-id="cc80c-1359">\_keyStart (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1359">\_keyStart (variable)</span></span>

<span data-ttu-id="cc80c-1360">\_keyEnd (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1360">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="cc80c-1361">**\_ keyStart:** Eine CKey-Struktur, wie in Abschnitt 2.2.1.4 angegeben, die den Anfang des Bereichs enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1361">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="cc80c-1362">**\_ keyEnd:** Eine CKey-Struktur, die das Ende des Bereichs enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1362">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="cc80c-1363">2.2.1.11 CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-1363">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="cc80c-1364">Die CScopeRestriction-Struktur enthält eine Einschränkung für die zu durchsuchenden Dateien.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1364">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="cc80c-1365">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1365">0</span></span>

<span data-ttu-id="cc80c-1366">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1366">1</span></span>

<span data-ttu-id="cc80c-1367">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1367">2</span></span>

<span data-ttu-id="cc80c-1368">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1368">3</span></span>

<span data-ttu-id="cc80c-1369">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1369">4</span></span>

<span data-ttu-id="cc80c-1370">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1370">5</span></span>

<span data-ttu-id="cc80c-1371">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1371">6</span></span>

<span data-ttu-id="cc80c-1372">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1372">7</span></span>

<span data-ttu-id="cc80c-1373">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1373">8</span></span>

<span data-ttu-id="cc80c-1374">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1374">9</span></span>

<span data-ttu-id="cc80c-1375">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1375">1</span></span><br/> <span data-ttu-id="cc80c-1376">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1376">0</span></span><br/>

<span data-ttu-id="cc80c-1377">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1377">1</span></span>

<span data-ttu-id="cc80c-1378">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1378">2</span></span>

<span data-ttu-id="cc80c-1379">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1379">3</span></span>

<span data-ttu-id="cc80c-1380">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1380">4</span></span>

<span data-ttu-id="cc80c-1381">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1381">5</span></span>

<span data-ttu-id="cc80c-1382">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1382">6</span></span>

<span data-ttu-id="cc80c-1383">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1383">7</span></span>

<span data-ttu-id="cc80c-1384">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1384">8</span></span>

<span data-ttu-id="cc80c-1385">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1385">9</span></span>

<span data-ttu-id="cc80c-1386">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1386">2</span></span><br/> <span data-ttu-id="cc80c-1387">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1387">0</span></span><br/>

<span data-ttu-id="cc80c-1388">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1388">1</span></span>

<span data-ttu-id="cc80c-1389">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1389">2</span></span>

<span data-ttu-id="cc80c-1390">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1390">3</span></span>

<span data-ttu-id="cc80c-1391">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1391">4</span></span>

<span data-ttu-id="cc80c-1392">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1392">5</span></span>

<span data-ttu-id="cc80c-1393">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1393">6</span></span>

<span data-ttu-id="cc80c-1394">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1394">7</span></span>

<span data-ttu-id="cc80c-1395">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1395">8</span></span>

<span data-ttu-id="cc80c-1396">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1396">9</span></span>

<span data-ttu-id="cc80c-1397">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1397">3</span></span><br/> <span data-ttu-id="cc80c-1398">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1398">0</span></span><br/>

<span data-ttu-id="cc80c-1399">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1399">1</span></span>

<span data-ttu-id="cc80c-1400">CcLowerPath</span><span class="sxs-lookup"><span data-stu-id="cc80c-1400">CcLowerPath</span></span>

<span data-ttu-id="cc80c-1401">\_lowerPath (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1401">\_lowerPath (variable)</span></span>

<span data-ttu-id="cc80c-1402">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-1402">...</span></span>

<span data-ttu-id="cc80c-1403">\_Padding (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1403">\_padding ( variable)</span></span>

<span data-ttu-id="cc80c-1404">\_Länge</span><span class="sxs-lookup"><span data-stu-id="cc80c-1404">\_length</span></span>

<span data-ttu-id="cc80c-1405">\_fRecursive</span><span class="sxs-lookup"><span data-stu-id="cc80c-1405">\_fRecursive</span></span>

<span data-ttu-id="cc80c-1406">\_fVirtuelle</span><span class="sxs-lookup"><span data-stu-id="cc80c-1406">\_fVirtual</span></span>



 

<span data-ttu-id="cc80c-1407">**CcLowerPath:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von Unicode-Zeichen im \_ feld lowerPath enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1407">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="cc80c-1408">**\_ lowerPath:** Eine Nicht-NULL-terminierte Unicode-Zeichenfolge, die den **Pfad** darstellt, auf den die Abfrage beschränkt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1408">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="cc80c-1409">Das Feld CcLowerPath enthält die Länge der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1409">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="cc80c-1410">**\_ Auffüllung:** Dieses Feld MUSS 0 bis 3 Bytes lang sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1410">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cc80c-1411">Die Länge dieses Felds MUSS so sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Bytes ab dem Anfang der Nachricht ist, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1411">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cc80c-1412">Wenn dieses Feld vorhanden ist (d. h. die Länge ungleich null), ist der darin enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1412">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cc80c-1413">Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1413">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cc80c-1414">**\_ length:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge von \_ lowerPath in Unicode-Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1414">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="cc80c-1415">Dies MUSS derselbe Wert wie CcLowerPath sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1415">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="cc80c-1416">**\_ fRecursive:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1416">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cc80c-1417">MUSS auf 0x00000001 oder 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1417">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="cc80c-1418">Wenn 0x00000001 festgelegt ist, überprüft der Server rekursiv alle Unterverzeichnisse des Pfads.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1418">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="cc80c-1419">Wenn 0x00000000 festgelegt ist, soll der Server keine Unterverzeichnisse untersuchen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1419">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="cc80c-1420">**\_ fVirtual:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1420">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cc80c-1421">MUSS auf 0x00000001 oder 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1421">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="cc80c-1422">Wenn lowerPath auf 0x00000001 festgelegt \_ ist, ist dies ein virtueller Pfad (die Uniform Resource Locator (URL), die einem physischen Verzeichnis im Dateisystem zugeordnet ist) für eine Website.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1422">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="cc80c-1423">Wenn lowerPath auf 0x00000000 festgelegt \_ ist, ist dies ein Dateisystempfad.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1423">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="cc80c-1424">2.2.1.12 CSort</span><span class="sxs-lookup"><span data-stu-id="cc80c-1424">2.2.1.12 CSort</span></span>

<span data-ttu-id="cc80c-1425">Die CSort-Struktur identifiziert eine zu sortierende Spalte.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1425">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="cc80c-1426">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1426">0</span></span>

<span data-ttu-id="cc80c-1427">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1427">1</span></span>

<span data-ttu-id="cc80c-1428">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1428">2</span></span>

<span data-ttu-id="cc80c-1429">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1429">3</span></span>

<span data-ttu-id="cc80c-1430">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1430">4</span></span>

<span data-ttu-id="cc80c-1431">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1431">5</span></span>

<span data-ttu-id="cc80c-1432">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1432">6</span></span>

<span data-ttu-id="cc80c-1433">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1433">7</span></span>

<span data-ttu-id="cc80c-1434">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1434">8</span></span>

<span data-ttu-id="cc80c-1435">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1435">9</span></span>

<span data-ttu-id="cc80c-1436">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1436">1</span></span><br/> <span data-ttu-id="cc80c-1437">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1437">0</span></span><br/>

<span data-ttu-id="cc80c-1438">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1438">1</span></span>

<span data-ttu-id="cc80c-1439">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1439">2</span></span>

<span data-ttu-id="cc80c-1440">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1440">3</span></span>

<span data-ttu-id="cc80c-1441">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1441">4</span></span>

<span data-ttu-id="cc80c-1442">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1442">5</span></span>

<span data-ttu-id="cc80c-1443">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1443">6</span></span>

<span data-ttu-id="cc80c-1444">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1444">7</span></span>

<span data-ttu-id="cc80c-1445">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1445">8</span></span>

<span data-ttu-id="cc80c-1446">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1446">9</span></span>

<span data-ttu-id="cc80c-1447">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1447">2</span></span><br/> <span data-ttu-id="cc80c-1448">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1448">0</span></span><br/>

<span data-ttu-id="cc80c-1449">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1449">1</span></span>

<span data-ttu-id="cc80c-1450">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1450">2</span></span>

<span data-ttu-id="cc80c-1451">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1451">3</span></span>

<span data-ttu-id="cc80c-1452">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1452">4</span></span>

<span data-ttu-id="cc80c-1453">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1453">5</span></span>

<span data-ttu-id="cc80c-1454">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1454">6</span></span>

<span data-ttu-id="cc80c-1455">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1455">7</span></span>

<span data-ttu-id="cc80c-1456">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1456">8</span></span>

<span data-ttu-id="cc80c-1457">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1457">9</span></span>

<span data-ttu-id="cc80c-1458">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1458">3</span></span><br/> <span data-ttu-id="cc80c-1459">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1459">0</span></span><br/>

<span data-ttu-id="cc80c-1460">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1460">1</span></span>

<span data-ttu-id="cc80c-1461">pidColumn</span><span class="sxs-lookup"><span data-stu-id="cc80c-1461">pidColumn</span></span>

<span data-ttu-id="cc80c-1462">dwOrder</span><span class="sxs-lookup"><span data-stu-id="cc80c-1462">dwOrder</span></span>

<span data-ttu-id="cc80c-1463">locale</span><span class="sxs-lookup"><span data-stu-id="cc80c-1463">locale</span></span>



 

<span data-ttu-id="cc80c-1464">**pidColumn:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1464">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cc80c-1465">Die Nummer der Spalte, nach der sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1465">The number of the column to sort by.</span></span>

<span data-ttu-id="cc80c-1466">**dwOrder:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1466">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cc80c-1467">MUSS einer der folgenden Werte sein und angeben, wie basierend auf der Spalte sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1467">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="cc80c-1468">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-1468">Value</span></span>                        | <span data-ttu-id="cc80c-1469">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-1469">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-1470">\_SORTASCEND-ABFRAGE 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-1470">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="cc80c-1471">Die Zeilen müssen basierend auf den Werten in der angegebenen Spalte in aufsteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1471">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="cc80c-1472">QUERY \_ DESCEND 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-1472">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="cc80c-1473">Die Zeilen müssen basierend auf den Werten in der angegebenen Spalte in absteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1473">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="cc80c-1474">**locale:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Im MS-GPSI-Anhang A angegebene Locale \[ \] der Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1474">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="cc80c-1475">2.2.1.13 CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-1475">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="cc80c-1476">Die CSynRestriction-Struktur enthält ein Wort oder seine Synonyme für einen Abfrageaussatz.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1476">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="cc80c-1477">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1477">0</span></span>

<span data-ttu-id="cc80c-1478">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1478">1</span></span>

<span data-ttu-id="cc80c-1479">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1479">2</span></span>

<span data-ttu-id="cc80c-1480">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1480">3</span></span>

<span data-ttu-id="cc80c-1481">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1481">4</span></span>

<span data-ttu-id="cc80c-1482">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1482">5</span></span>

<span data-ttu-id="cc80c-1483">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1483">6</span></span>

<span data-ttu-id="cc80c-1484">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1484">7</span></span>

<span data-ttu-id="cc80c-1485">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1485">8</span></span>

<span data-ttu-id="cc80c-1486">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1486">9</span></span>

<span data-ttu-id="cc80c-1487">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1487">1</span></span><br/> <span data-ttu-id="cc80c-1488">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1488">0</span></span><br/>

<span data-ttu-id="cc80c-1489">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1489">1</span></span>

<span data-ttu-id="cc80c-1490">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1490">2</span></span>

<span data-ttu-id="cc80c-1491">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1491">3</span></span>

<span data-ttu-id="cc80c-1492">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1492">4</span></span>

<span data-ttu-id="cc80c-1493">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1493">5</span></span>

<span data-ttu-id="cc80c-1494">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1494">6</span></span>

<span data-ttu-id="cc80c-1495">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1495">7</span></span>

<span data-ttu-id="cc80c-1496">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1496">8</span></span>

<span data-ttu-id="cc80c-1497">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1497">9</span></span>

<span data-ttu-id="cc80c-1498">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1498">2</span></span><br/> <span data-ttu-id="cc80c-1499">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1499">0</span></span><br/>

<span data-ttu-id="cc80c-1500">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1500">1</span></span>

<span data-ttu-id="cc80c-1501">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1501">2</span></span>

<span data-ttu-id="cc80c-1502">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1502">3</span></span>

<span data-ttu-id="cc80c-1503">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1503">4</span></span>

<span data-ttu-id="cc80c-1504">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1504">5</span></span>

<span data-ttu-id="cc80c-1505">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1505">6</span></span>

<span data-ttu-id="cc80c-1506">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1506">7</span></span>

<span data-ttu-id="cc80c-1507">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1507">8</span></span>

<span data-ttu-id="cc80c-1508">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1508">9</span></span>

<span data-ttu-id="cc80c-1509">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1509">3</span></span><br/> <span data-ttu-id="cc80c-1510">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1510">0</span></span><br/>

<span data-ttu-id="cc80c-1511">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1511">1</span></span>

<span data-ttu-id="cc80c-1512">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="cc80c-1512">Restriction</span></span>

<span data-ttu-id="cc80c-1513">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-1513">...</span></span>

<span data-ttu-id="cc80c-1514">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-1514">...</span></span>

<span data-ttu-id="cc80c-1515">cKey</span><span class="sxs-lookup"><span data-stu-id="cc80c-1515">cKey</span></span>

<span data-ttu-id="cc80c-1516">\_keyArray (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1516">\_keyArray (variable)</span></span>

<span data-ttu-id="cc80c-1517">\_isRange</span><span class="sxs-lookup"><span data-stu-id="cc80c-1517">\_isRange</span></span>



 

<span data-ttu-id="cc80c-1518">**Einschränkung:** Eine COccRestriction-Struktur, die die Position des Worts an gibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1518">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="cc80c-1519">**cKey:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im \_ keyArray-Array angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1519">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="cc80c-1520">**\_ keyArray:** Ein Array von CKey-Strukturen, die ein Wort und seine Synonyme angeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1520">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="cc80c-1521">**\_ isRange:** Wenn auf 0x01 festgelegt ist, sind die Schlüssel Präfixe, die übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1521">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="cc80c-1522">Wenn diese 0x00 festgelegt ist, sind die Schlüssel exakte Übereinstimmende Werte.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1522">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="cc80c-1523">\_isRange DARF NICHT auf andere Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1523">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="cc80c-1524">2.2.1.14 CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-1524">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="cc80c-1525">Die CVectorRestriction-Struktur enthält einen gewichteten OR-Vorgang auf einem Befehlsstrukturknoten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1525">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="cc80c-1526">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1526">0</span></span>

<span data-ttu-id="cc80c-1527">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1527">1</span></span>

<span data-ttu-id="cc80c-1528">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1528">2</span></span>

<span data-ttu-id="cc80c-1529">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1529">3</span></span>

<span data-ttu-id="cc80c-1530">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1530">4</span></span>

<span data-ttu-id="cc80c-1531">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1531">5</span></span>

<span data-ttu-id="cc80c-1532">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1532">6</span></span>

<span data-ttu-id="cc80c-1533">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1533">7</span></span>

<span data-ttu-id="cc80c-1534">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1534">8</span></span>

<span data-ttu-id="cc80c-1535">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1535">9</span></span>

<span data-ttu-id="cc80c-1536">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1536">1</span></span><br/> <span data-ttu-id="cc80c-1537">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1537">0</span></span><br/>

<span data-ttu-id="cc80c-1538">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1538">1</span></span>

<span data-ttu-id="cc80c-1539">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1539">2</span></span>

<span data-ttu-id="cc80c-1540">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1540">3</span></span>

<span data-ttu-id="cc80c-1541">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1541">4</span></span>

<span data-ttu-id="cc80c-1542">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1542">5</span></span>

<span data-ttu-id="cc80c-1543">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1543">6</span></span>

<span data-ttu-id="cc80c-1544">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1544">7</span></span>

<span data-ttu-id="cc80c-1545">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1545">8</span></span>

<span data-ttu-id="cc80c-1546">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1546">9</span></span>

<span data-ttu-id="cc80c-1547">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1547">2</span></span><br/> <span data-ttu-id="cc80c-1548">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1548">0</span></span><br/>

<span data-ttu-id="cc80c-1549">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1549">1</span></span>

<span data-ttu-id="cc80c-1550">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1550">2</span></span>

<span data-ttu-id="cc80c-1551">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1551">3</span></span>

<span data-ttu-id="cc80c-1552">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1552">4</span></span>

<span data-ttu-id="cc80c-1553">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1553">5</span></span>

<span data-ttu-id="cc80c-1554">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1554">6</span></span>

<span data-ttu-id="cc80c-1555">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1555">7</span></span>

<span data-ttu-id="cc80c-1556">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1556">8</span></span>

<span data-ttu-id="cc80c-1557">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1557">9</span></span>

<span data-ttu-id="cc80c-1558">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1558">3</span></span><br/> <span data-ttu-id="cc80c-1559">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1559">0</span></span><br/>

<span data-ttu-id="cc80c-1560">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1560">1</span></span>

<span data-ttu-id="cc80c-1561">\_pres (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1561">\_pres (variable)</span></span>

<span data-ttu-id="cc80c-1562">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-1562">...</span></span>

<span data-ttu-id="cc80c-1563">\_Auffüllen (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1563">\_padding (variable)</span></span>

<span data-ttu-id="cc80c-1564">\_ulRankMethod</span><span class="sxs-lookup"><span data-stu-id="cc80c-1564">\_ulRankMethod</span></span>



 

<span data-ttu-id="cc80c-1565">**\_ pres:** Eine CNodeRestriction-Befehlsstruktur, für die ein or-Vorgang mit Rangfolge ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1565">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="cc80c-1566">**\_ Auffüllung:** Dieses Feld MUSS 0 bis 3 Bytes lang sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1566">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cc80c-1567">Die Länge dieses Felds MUSS so sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Bytes ab dem Anfang der Nachricht ist, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1567">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cc80c-1568">Wenn dieses Feld vorhanden ist (d. h. die Länge ungleich null), ist der darin enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1568">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cc80c-1569">Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1569">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cc80c-1570">**\_ ulRankMethod:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die einen Rangfolgealgorithmus angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1570">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="cc80c-1571">MUSS auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1571">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="cc80c-1572">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-1572">Value</span></span>                            | <span data-ttu-id="cc80c-1573">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-1573">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="cc80c-1574">VECTOR \_ RANK \_ MIN 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-1574">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="cc80c-1575">Verwenden Sie den \[ SALTON-Mindestalgorithmus. \]</span><span class="sxs-lookup"><span data-stu-id="cc80c-1575">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="cc80c-1576">VECTOR \_ RANK \_ MAX 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-1576">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="cc80c-1577">Verwenden Sie den maximalen \[ SALTON-Algorithmus. \]</span><span class="sxs-lookup"><span data-stu-id="cc80c-1577">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="cc80c-1578">VECTOR \_ RANK \_ INNER 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-1578">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="cc80c-1579">Verwenden Sie den inneren Produktalgorithmus \[ SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="cc80c-1579">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="cc80c-1580">VECTOR \_ RANK \_ DICE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-1580">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="cc80c-1581">Verwenden Sie den Würfelkoeffizientenalgorithmus \[ SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="cc80c-1581">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="cc80c-1582">VECTOR \_ RANK \_ JACCARD-0x00000004</span><span class="sxs-lookup"><span data-stu-id="cc80c-1582">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="cc80c-1583">Verwenden Sie den Jaccard-Koeffizientenalgorithmus \[ SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="cc80c-1583">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="cc80c-1584">2.2.1.15 CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-1584">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="cc80c-1585">Die CWordRestriction-Struktur enthält ein Wort für einen Abfrageaussatz.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1585">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="cc80c-1586">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1586">0</span></span>

<span data-ttu-id="cc80c-1587">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1587">1</span></span>

<span data-ttu-id="cc80c-1588">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1588">2</span></span>

<span data-ttu-id="cc80c-1589">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1589">3</span></span>

<span data-ttu-id="cc80c-1590">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1590">4</span></span>

<span data-ttu-id="cc80c-1591">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1591">5</span></span>

<span data-ttu-id="cc80c-1592">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1592">6</span></span>

<span data-ttu-id="cc80c-1593">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1593">7</span></span>

<span data-ttu-id="cc80c-1594">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1594">8</span></span>

<span data-ttu-id="cc80c-1595">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1595">9</span></span>

<span data-ttu-id="cc80c-1596">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1596">1</span></span><br/> <span data-ttu-id="cc80c-1597">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1597">0</span></span><br/>

<span data-ttu-id="cc80c-1598">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1598">1</span></span>

<span data-ttu-id="cc80c-1599">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1599">2</span></span>

<span data-ttu-id="cc80c-1600">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1600">3</span></span>

<span data-ttu-id="cc80c-1601">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1601">4</span></span>

<span data-ttu-id="cc80c-1602">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1602">5</span></span>

<span data-ttu-id="cc80c-1603">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1603">6</span></span>

<span data-ttu-id="cc80c-1604">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1604">7</span></span>

<span data-ttu-id="cc80c-1605">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1605">8</span></span>

<span data-ttu-id="cc80c-1606">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1606">9</span></span>

<span data-ttu-id="cc80c-1607">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1607">2</span></span><br/> <span data-ttu-id="cc80c-1608">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1608">0</span></span><br/>

<span data-ttu-id="cc80c-1609">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1609">1</span></span>

<span data-ttu-id="cc80c-1610">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1610">2</span></span>

<span data-ttu-id="cc80c-1611">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1611">3</span></span>

<span data-ttu-id="cc80c-1612">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1612">4</span></span>

<span data-ttu-id="cc80c-1613">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1613">5</span></span>

<span data-ttu-id="cc80c-1614">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1614">6</span></span>

<span data-ttu-id="cc80c-1615">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1615">7</span></span>

<span data-ttu-id="cc80c-1616">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1616">8</span></span>

<span data-ttu-id="cc80c-1617">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1617">9</span></span>

<span data-ttu-id="cc80c-1618">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1618">3</span></span><br/> <span data-ttu-id="cc80c-1619">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1619">0</span></span><br/>

<span data-ttu-id="cc80c-1620">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1620">1</span></span>

<span data-ttu-id="cc80c-1621">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="cc80c-1621">restriction</span></span>

<span data-ttu-id="cc80c-1622">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-1622">...</span></span>

<span data-ttu-id="cc80c-1623">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-1623">...</span></span>

<span data-ttu-id="cc80c-1624">\_key (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1624">\_key (variable)</span></span>

<span data-ttu-id="cc80c-1625">\_isRange</span><span class="sxs-lookup"><span data-stu-id="cc80c-1625">\_isRange</span></span>



 

<span data-ttu-id="cc80c-1626">**restriction:** Eine COccRestriction-Struktur, die die Position des Worts an gibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1626">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="cc80c-1627">**\_ key:** Eine CKey-Struktur, die ein Wort an gibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1627">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="cc80c-1628">**\_ isRange:** Wenn auf 0x01 festgelegt ist, ist der Schlüssel ein Präfix, das übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1628">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="cc80c-1629">Wenn der Wert auf 0x00 festgelegt ist, ist der Schlüssel ein exakter Wert, der übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1629">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="cc80c-1630">\_isRange DARF NICHT auf einen anderen Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1630">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="cc80c-1631">2.2.1.16 CRestriction</span><span class="sxs-lookup"><span data-stu-id="cc80c-1631">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="cc80c-1632">Die CRestriction-Struktur enthält einen Knoten einer Abfragebefehlsstruktur.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1632">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="cc80c-1633">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1633">0</span></span>

<span data-ttu-id="cc80c-1634">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1634">1</span></span>

<span data-ttu-id="cc80c-1635">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1635">2</span></span>

<span data-ttu-id="cc80c-1636">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1636">3</span></span>

<span data-ttu-id="cc80c-1637">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1637">4</span></span>

<span data-ttu-id="cc80c-1638">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1638">5</span></span>

<span data-ttu-id="cc80c-1639">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1639">6</span></span>

<span data-ttu-id="cc80c-1640">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1640">7</span></span>

<span data-ttu-id="cc80c-1641">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1641">8</span></span>

<span data-ttu-id="cc80c-1642">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1642">9</span></span>

<span data-ttu-id="cc80c-1643">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1643">1</span></span><br/> <span data-ttu-id="cc80c-1644">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1644">0</span></span><br/>

<span data-ttu-id="cc80c-1645">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1645">1</span></span>

<span data-ttu-id="cc80c-1646">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1646">2</span></span>

<span data-ttu-id="cc80c-1647">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1647">3</span></span>

<span data-ttu-id="cc80c-1648">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1648">4</span></span>

<span data-ttu-id="cc80c-1649">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1649">5</span></span>

<span data-ttu-id="cc80c-1650">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1650">6</span></span>

<span data-ttu-id="cc80c-1651">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1651">7</span></span>

<span data-ttu-id="cc80c-1652">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1652">8</span></span>

<span data-ttu-id="cc80c-1653">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1653">9</span></span>

<span data-ttu-id="cc80c-1654">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1654">2</span></span><br/> <span data-ttu-id="cc80c-1655">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1655">0</span></span><br/>

<span data-ttu-id="cc80c-1656">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1656">1</span></span>

<span data-ttu-id="cc80c-1657">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1657">2</span></span>

<span data-ttu-id="cc80c-1658">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1658">3</span></span>

<span data-ttu-id="cc80c-1659">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1659">4</span></span>

<span data-ttu-id="cc80c-1660">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1660">5</span></span>

<span data-ttu-id="cc80c-1661">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1661">6</span></span>

<span data-ttu-id="cc80c-1662">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1662">7</span></span>

<span data-ttu-id="cc80c-1663">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1663">8</span></span>

<span data-ttu-id="cc80c-1664">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1664">9</span></span>

<span data-ttu-id="cc80c-1665">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1665">3</span></span><br/> <span data-ttu-id="cc80c-1666">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1666">0</span></span><br/>

<span data-ttu-id="cc80c-1667">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1667">1</span></span>

<span data-ttu-id="cc80c-1668">\_ulType</span><span class="sxs-lookup"><span data-stu-id="cc80c-1668">\_ulType</span></span>

<span data-ttu-id="cc80c-1669">Weight</span><span class="sxs-lookup"><span data-stu-id="cc80c-1669">Weight</span></span>

<span data-ttu-id="cc80c-1670">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="cc80c-1670">Restriction</span></span>



 

<span data-ttu-id="cc80c-1671">**\_ ulType:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Einschränkungstyp angibt, der für den Befehlsstrukturknoten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1671">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="cc80c-1672">MUSS auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1672">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="cc80c-1673">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-1673">Value</span></span>                    | <span data-ttu-id="cc80c-1674">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-1674">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-1675">RTNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-1675">RTNone 0x00000000</span></span>        | <span data-ttu-id="cc80c-1676">Der Knoten stellt ein Rauschwort in einer Vektorabfrage dar.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1676">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="cc80c-1677">RTAnd 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-1677">RTAnd 0x00000001</span></span>         | <span data-ttu-id="cc80c-1678">Der Knoten enthält eine CNodeRestriction, für die ein logischer AND-Vorgang ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1678">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="cc80c-1679">RTOr 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-1679">RTOr 0x00000002</span></span>          | <span data-ttu-id="cc80c-1680">Der Knoten enthält eine CNodeRestriction, für die ein logischer OR-Vorgang ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1680">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="cc80c-1681">RTNot 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-1681">RTNot 0x00000003</span></span>         | <span data-ttu-id="cc80c-1682">Der Knoten enthält eine CRestriction, für die ein NOT-Vorgang ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1682">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="cc80c-1683">RTContent 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cc80c-1683">RTContent 0x00000004</span></span>     | <span data-ttu-id="cc80c-1684">Der Knoten enthält eine CContentRestriction.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1684">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="cc80c-1685">RTProperty-0x00000005</span><span class="sxs-lookup"><span data-stu-id="cc80c-1685">RTProperty 0x00000005</span></span>    | <span data-ttu-id="cc80c-1686">Der Knoten enthält eine CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1686">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="cc80c-1687">RTProximity 0x00000006</span><span class="sxs-lookup"><span data-stu-id="cc80c-1687">RTProximity 0x00000006</span></span>   | <span data-ttu-id="cc80c-1688">Der Knoten enthält eine CNodeRestriction, für die eine Näherungsrangfolge durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1688">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="cc80c-1689">RTVector 0x00000007</span><span class="sxs-lookup"><span data-stu-id="cc80c-1689">RTVector 0x00000007</span></span>      | <span data-ttu-id="cc80c-1690">Der Knoten enthält eine CVectorRestriction.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1690">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="cc80c-1691">RTNatLanguage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cc80c-1691">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="cc80c-1692">Der Knoten enthält eine CNatLanguageRestriction.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1692">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="cc80c-1693">RTScope 0x00000009</span><span class="sxs-lookup"><span data-stu-id="cc80c-1693">RTScope 0x00000009</span></span>       | <span data-ttu-id="cc80c-1694">Der Knoten enthält eine CScopeRestriction.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1694">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="cc80c-1695">PRAny-0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="cc80c-1695">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="cc80c-1696">Der Knoten enthält eine CInternalPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1696">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="cc80c-1697">RTRange 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="cc80c-1697">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="cc80c-1698">Der Knoten enthält eine CRangeRestriction.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1698">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="cc80c-1699">RTPhrase-0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="cc80c-1699">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="cc80c-1700">Der Knoten enthält eine CNodeRestriction, für die eine Ausdrucks match ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1700">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="cc80c-1701">RTSynonym 0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="cc80c-1701">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="cc80c-1702">Der Knoten enthält eine CSynRestriction.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1702">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="cc80c-1703">RTWord-0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="cc80c-1703">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="cc80c-1704">Der Knoten enthält eine CWordRestriction.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1704">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="cc80c-1705">**Gewichtung:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gewichtung des Knotens darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1705">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="cc80c-1706">Die Gewichtung gibt die Wichtigkeit des Knotens relativ zu anderen Knoten in der Abfragebefehlsstruktur an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1706">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="cc80c-1707">Höhere Gewichtungswerte sind wichtiger.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1707">Higher weight values are more important.</span></span>

<span data-ttu-id="cc80c-1708">**Einschränkung:** Der Einschränkungstyp für den Befehlsstrukturknoten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1708">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="cc80c-1709">Die Syntax MUSS wie durch das \_ ulType-Feld angegeben sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1709">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="cc80c-1710">2.2.1.17 CColumnSet</span><span class="sxs-lookup"><span data-stu-id="cc80c-1710">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="cc80c-1711">Die CColumnSet-Struktur gibt die spaltennummern an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1711">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="cc80c-1712">Diese Struktur wird immer als Verweis auf eine bestimmte CPidMapper-Struktur verwendet (Abschnitt 2.2.1.23).</span><span class="sxs-lookup"><span data-stu-id="cc80c-1712">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="cc80c-1713">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1713">0</span></span>

<span data-ttu-id="cc80c-1714">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1714">1</span></span>

<span data-ttu-id="cc80c-1715">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1715">2</span></span>

<span data-ttu-id="cc80c-1716">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1716">3</span></span>

<span data-ttu-id="cc80c-1717">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1717">4</span></span>

<span data-ttu-id="cc80c-1718">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1718">5</span></span>

<span data-ttu-id="cc80c-1719">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1719">6</span></span>

<span data-ttu-id="cc80c-1720">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1720">7</span></span>

<span data-ttu-id="cc80c-1721">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1721">8</span></span>

<span data-ttu-id="cc80c-1722">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1722">9</span></span>

<span data-ttu-id="cc80c-1723">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1723">1</span></span><br/> <span data-ttu-id="cc80c-1724">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1724">0</span></span><br/>

<span data-ttu-id="cc80c-1725">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1725">1</span></span>

<span data-ttu-id="cc80c-1726">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1726">2</span></span>

<span data-ttu-id="cc80c-1727">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1727">3</span></span>

<span data-ttu-id="cc80c-1728">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1728">4</span></span>

<span data-ttu-id="cc80c-1729">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1729">5</span></span>

<span data-ttu-id="cc80c-1730">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1730">6</span></span>

<span data-ttu-id="cc80c-1731">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1731">7</span></span>

<span data-ttu-id="cc80c-1732">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1732">8</span></span>

<span data-ttu-id="cc80c-1733">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1733">9</span></span>

<span data-ttu-id="cc80c-1734">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1734">2</span></span><br/> <span data-ttu-id="cc80c-1735">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1735">0</span></span><br/>

<span data-ttu-id="cc80c-1736">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1736">1</span></span>

<span data-ttu-id="cc80c-1737">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1737">2</span></span>

<span data-ttu-id="cc80c-1738">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1738">3</span></span>

<span data-ttu-id="cc80c-1739">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1739">4</span></span>

<span data-ttu-id="cc80c-1740">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1740">5</span></span>

<span data-ttu-id="cc80c-1741">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1741">6</span></span>

<span data-ttu-id="cc80c-1742">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1742">7</span></span>

<span data-ttu-id="cc80c-1743">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1743">8</span></span>

<span data-ttu-id="cc80c-1744">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1744">9</span></span>

<span data-ttu-id="cc80c-1745">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1745">3</span></span><br/> <span data-ttu-id="cc80c-1746">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1746">0</span></span><br/>

<span data-ttu-id="cc80c-1747">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1747">1</span></span>

<span data-ttu-id="cc80c-1748">count</span><span class="sxs-lookup"><span data-stu-id="cc80c-1748">count</span></span>

<span data-ttu-id="cc80c-1749">Indizes (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1749">indexes (variable)</span></span>



 

<span data-ttu-id="cc80c-1750">**count:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im Indexarray angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1750">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="cc80c-1751">**indexes:** Array von 4-Byte-Ganzzahlen ohne Vorzeichen, die nullbasierte Indizes im aPropSpec-Array in der entsprechenden CPidMapper-Struktur darstellen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1751">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="cc80c-1752">2.2.1.18 CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="cc80c-1752">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="cc80c-1753">Die CCategorizationSet-Struktur enthält Informationen über die Gruppierung eines Abfrageergebnissets.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1753">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="cc80c-1754">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1754">0</span></span>

<span data-ttu-id="cc80c-1755">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1755">1</span></span>

<span data-ttu-id="cc80c-1756">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1756">2</span></span>

<span data-ttu-id="cc80c-1757">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1757">3</span></span>

<span data-ttu-id="cc80c-1758">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1758">4</span></span>

<span data-ttu-id="cc80c-1759">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1759">5</span></span>

<span data-ttu-id="cc80c-1760">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1760">6</span></span>

<span data-ttu-id="cc80c-1761">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1761">7</span></span>

<span data-ttu-id="cc80c-1762">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1762">8</span></span>

<span data-ttu-id="cc80c-1763">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1763">9</span></span>

<span data-ttu-id="cc80c-1764">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1764">1</span></span><br/> <span data-ttu-id="cc80c-1765">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1765">0</span></span><br/>

<span data-ttu-id="cc80c-1766">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1766">1</span></span>

<span data-ttu-id="cc80c-1767">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1767">2</span></span>

<span data-ttu-id="cc80c-1768">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1768">3</span></span>

<span data-ttu-id="cc80c-1769">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1769">4</span></span>

<span data-ttu-id="cc80c-1770">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1770">5</span></span>

<span data-ttu-id="cc80c-1771">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1771">6</span></span>

<span data-ttu-id="cc80c-1772">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1772">7</span></span>

<span data-ttu-id="cc80c-1773">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1773">8</span></span>

<span data-ttu-id="cc80c-1774">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1774">9</span></span>

<span data-ttu-id="cc80c-1775">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1775">2</span></span><br/> <span data-ttu-id="cc80c-1776">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1776">0</span></span><br/>

<span data-ttu-id="cc80c-1777">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1777">1</span></span>

<span data-ttu-id="cc80c-1778">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1778">2</span></span>

<span data-ttu-id="cc80c-1779">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1779">3</span></span>

<span data-ttu-id="cc80c-1780">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1780">4</span></span>

<span data-ttu-id="cc80c-1781">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1781">5</span></span>

<span data-ttu-id="cc80c-1782">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1782">6</span></span>

<span data-ttu-id="cc80c-1783">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1783">7</span></span>

<span data-ttu-id="cc80c-1784">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1784">8</span></span>

<span data-ttu-id="cc80c-1785">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1785">9</span></span>

<span data-ttu-id="cc80c-1786">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1786">3</span></span><br/> <span data-ttu-id="cc80c-1787">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1787">0</span></span><br/>

<span data-ttu-id="cc80c-1788">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1788">1</span></span>

<span data-ttu-id="cc80c-1789">count</span><span class="sxs-lookup"><span data-stu-id="cc80c-1789">count</span></span>

<span data-ttu-id="cc80c-1790">categories (variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1790">categories (variable)</span></span>



 

<span data-ttu-id="cc80c-1791">**count:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im Array categories enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1791">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="cc80c-1792">**categories**: Array von CCategorizationSpec-Strukturen, die die Gruppierung der Abfrage angeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1792">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="cc80c-1793">2.2.1.19 CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="cc80c-1793">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="cc80c-1794">Die CCategorizationSpec-Struktur enthält eine Gruppierung für ein Abfrageresultset.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1794">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="cc80c-1795">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1795">0</span></span>

<span data-ttu-id="cc80c-1796">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1796">1</span></span>

<span data-ttu-id="cc80c-1797">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1797">2</span></span>

<span data-ttu-id="cc80c-1798">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1798">3</span></span>

<span data-ttu-id="cc80c-1799">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1799">4</span></span>

<span data-ttu-id="cc80c-1800">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1800">5</span></span>

<span data-ttu-id="cc80c-1801">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1801">6</span></span>

<span data-ttu-id="cc80c-1802">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1802">7</span></span>

<span data-ttu-id="cc80c-1803">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1803">8</span></span>

<span data-ttu-id="cc80c-1804">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1804">9</span></span>

<span data-ttu-id="cc80c-1805">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1805">1</span></span><br/> <span data-ttu-id="cc80c-1806">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1806">0</span></span><br/>

<span data-ttu-id="cc80c-1807">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1807">1</span></span>

<span data-ttu-id="cc80c-1808">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1808">2</span></span>

<span data-ttu-id="cc80c-1809">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1809">3</span></span>

<span data-ttu-id="cc80c-1810">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1810">4</span></span>

<span data-ttu-id="cc80c-1811">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1811">5</span></span>

<span data-ttu-id="cc80c-1812">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1812">6</span></span>

<span data-ttu-id="cc80c-1813">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1813">7</span></span>

<span data-ttu-id="cc80c-1814">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1814">8</span></span>

<span data-ttu-id="cc80c-1815">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1815">9</span></span>

<span data-ttu-id="cc80c-1816">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1816">2</span></span><br/> <span data-ttu-id="cc80c-1817">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1817">0</span></span><br/>

<span data-ttu-id="cc80c-1818">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1818">1</span></span>

<span data-ttu-id="cc80c-1819">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1819">2</span></span>

<span data-ttu-id="cc80c-1820">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1820">3</span></span>

<span data-ttu-id="cc80c-1821">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1821">4</span></span>

<span data-ttu-id="cc80c-1822">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1822">5</span></span>

<span data-ttu-id="cc80c-1823">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1823">6</span></span>

<span data-ttu-id="cc80c-1824">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1824">7</span></span>

<span data-ttu-id="cc80c-1825">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1825">8</span></span>

<span data-ttu-id="cc80c-1826">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1826">9</span></span>

<span data-ttu-id="cc80c-1827">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1827">3</span></span><br/> <span data-ttu-id="cc80c-1828">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1828">0</span></span><br/>

<span data-ttu-id="cc80c-1829">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1829">1</span></span>

<span data-ttu-id="cc80c-1830">\_csColumns (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1830">\_csColumns (variable)</span></span>

<span data-ttu-id="cc80c-1831">\_ulCategType</span><span class="sxs-lookup"><span data-stu-id="cc80c-1831">\_ulCategType</span></span>



 

<span data-ttu-id="cc80c-1832">**\_ csColumns:** Eine CColumnSet-Struktur, die die Spalten angibt, nach denen die Abfrage gruppiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1832">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="cc80c-1833">**\_ ulCategType:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1833">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cc80c-1834">MUSS auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1834">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="cc80c-1835">2.2.1.20 CDbColId</span><span class="sxs-lookup"><span data-stu-id="cc80c-1835">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="cc80c-1836">Die CDbColId-Struktur enthält eine Spalte.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1836">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="cc80c-1837">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1837">0</span></span>

<span data-ttu-id="cc80c-1838">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1838">1</span></span>

<span data-ttu-id="cc80c-1839">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1839">2</span></span>

<span data-ttu-id="cc80c-1840">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1840">3</span></span>

<span data-ttu-id="cc80c-1841">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1841">4</span></span>

<span data-ttu-id="cc80c-1842">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1842">5</span></span>

<span data-ttu-id="cc80c-1843">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1843">6</span></span>

<span data-ttu-id="cc80c-1844">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1844">7</span></span>

<span data-ttu-id="cc80c-1845">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1845">8</span></span>

<span data-ttu-id="cc80c-1846">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1846">9</span></span>

<span data-ttu-id="cc80c-1847">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1847">1</span></span><br/> <span data-ttu-id="cc80c-1848">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1848">0</span></span><br/>

<span data-ttu-id="cc80c-1849">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1849">1</span></span>

<span data-ttu-id="cc80c-1850">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1850">2</span></span>

<span data-ttu-id="cc80c-1851">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1851">3</span></span>

<span data-ttu-id="cc80c-1852">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1852">4</span></span>

<span data-ttu-id="cc80c-1853">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1853">5</span></span>

<span data-ttu-id="cc80c-1854">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1854">6</span></span>

<span data-ttu-id="cc80c-1855">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1855">7</span></span>

<span data-ttu-id="cc80c-1856">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1856">8</span></span>

<span data-ttu-id="cc80c-1857">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1857">9</span></span>

<span data-ttu-id="cc80c-1858">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1858">2</span></span><br/> <span data-ttu-id="cc80c-1859">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1859">0</span></span><br/>

<span data-ttu-id="cc80c-1860">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1860">1</span></span>

<span data-ttu-id="cc80c-1861">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1861">2</span></span>

<span data-ttu-id="cc80c-1862">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1862">3</span></span>

<span data-ttu-id="cc80c-1863">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1863">4</span></span>

<span data-ttu-id="cc80c-1864">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1864">5</span></span>

<span data-ttu-id="cc80c-1865">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1865">6</span></span>

<span data-ttu-id="cc80c-1866">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1866">7</span></span>

<span data-ttu-id="cc80c-1867">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1867">8</span></span>

<span data-ttu-id="cc80c-1868">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1868">9</span></span>

<span data-ttu-id="cc80c-1869">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1869">3</span></span><br/> <span data-ttu-id="cc80c-1870">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1870">0</span></span><br/>

<span data-ttu-id="cc80c-1871">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1871">1</span></span>

<span data-ttu-id="cc80c-1872">eKind</span><span class="sxs-lookup"><span data-stu-id="cc80c-1872">eKind</span></span>

<span data-ttu-id="cc80c-1873">GUID</span><span class="sxs-lookup"><span data-stu-id="cc80c-1873">GUID</span></span>

<span data-ttu-id="cc80c-1874">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-1874">...</span></span>

<span data-ttu-id="cc80c-1875">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-1875">...</span></span>

<span data-ttu-id="cc80c-1876">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-1876">...</span></span>

<span data-ttu-id="cc80c-1877">ulId</span><span class="sxs-lookup"><span data-stu-id="cc80c-1877">ulId</span></span>

<span data-ttu-id="cc80c-1878">vString (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1878">vString (variable)</span></span>



 

<span data-ttu-id="cc80c-1879">**eKind:** MUSS auf einen der folgenden Werte festgelegt werden, der den Inhalt von GUID und vValue angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1879">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="cc80c-1880">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-1880">Value</span></span>                            | <span data-ttu-id="cc80c-1881">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-1881">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-1882">DBKIND \_ GUID \_ NAME 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-1882">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="cc80c-1883">vString enthält einen Eigenschaftennamen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1883">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="cc80c-1884">DBKIND \_ GUID \_ PROPID 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-1884">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="cc80c-1885">ulId enthält eine 4-Byte-Ganzzahl, die die Eigenschaften-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1885">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="cc80c-1886">DBKIND \_ PGUID \_ NAME 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-1886">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="cc80c-1887">vString enthält einen Eigenschaftennamen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1887">vString contains a property name.</span></span> <span data-ttu-id="cc80c-1888">Dieser Wert MUSS mit DBKIND \_ GUID \_ NAME identisch sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1888">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="cc80c-1889">DBKIND \_ PGUID \_ PROPID 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cc80c-1889">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="cc80c-1890">ulId enthält eine 4-Byte-Ganzzahl, die die Eigenschaften-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1890">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="cc80c-1891">Dieser Wert MUSS mit DBKIND \_ GUID \_ PROPID identisch sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1891">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="cc80c-1892">**GUID:** Die Eigenschaften-GUID.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1892">**GUID**: The property GUID.</span></span>

<span data-ttu-id="cc80c-1893">**ulId:** Wenn eKind DBKIND \_ GUID PROPID oder DBKIND PGUID PROPID ist, enthält dieses Feld eine ganze Zahl ohne Vorzeichen, die die \_ \_ \_ Eigenschaften-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1893">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="cc80c-1894">Wenn eKind DBKIND GUID NAME oder DBKIND PGUID NAME ist, enthält dieses Feld eine ganze Zahl ohne Vorzeichen, die die Anzahl von Unicode-Zeichen angibt, die \_ \_ im \_ \_ vString-Feld enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1894">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="cc80c-1895">**vString:** Eine nicht auf NULL terminierte Unicode-Zeichenfolge, die den Eigenschaftennamen darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1895">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="cc80c-1896">Sie MUSS weggelassen werden, es sei denn, das eKind-Feld ist auf DBKIND \_ GUID \_ NAME oder DBKIND \_ PGUID \_ NAME festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1896">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="cc80c-1897">2.2.1.21 CDbProp</span><span class="sxs-lookup"><span data-stu-id="cc80c-1897">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="cc80c-1898">Die CDbProp-Struktur enthält eine -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1898">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="cc80c-1899">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1899">0</span></span>

<span data-ttu-id="cc80c-1900">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1900">1</span></span>

<span data-ttu-id="cc80c-1901">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1901">2</span></span>

<span data-ttu-id="cc80c-1902">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1902">3</span></span>

<span data-ttu-id="cc80c-1903">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1903">4</span></span>

<span data-ttu-id="cc80c-1904">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1904">5</span></span>

<span data-ttu-id="cc80c-1905">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1905">6</span></span>

<span data-ttu-id="cc80c-1906">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1906">7</span></span>

<span data-ttu-id="cc80c-1907">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1907">8</span></span>

<span data-ttu-id="cc80c-1908">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1908">9</span></span>

<span data-ttu-id="cc80c-1909">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1909">1</span></span><br/> <span data-ttu-id="cc80c-1910">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1910">0</span></span><br/>

<span data-ttu-id="cc80c-1911">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1911">1</span></span>

<span data-ttu-id="cc80c-1912">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1912">2</span></span>

<span data-ttu-id="cc80c-1913">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1913">3</span></span>

<span data-ttu-id="cc80c-1914">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1914">4</span></span>

<span data-ttu-id="cc80c-1915">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1915">5</span></span>

<span data-ttu-id="cc80c-1916">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1916">6</span></span>

<span data-ttu-id="cc80c-1917">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1917">7</span></span>

<span data-ttu-id="cc80c-1918">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1918">8</span></span>

<span data-ttu-id="cc80c-1919">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1919">9</span></span>

<span data-ttu-id="cc80c-1920">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1920">2</span></span><br/> <span data-ttu-id="cc80c-1921">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1921">0</span></span><br/>

<span data-ttu-id="cc80c-1922">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1922">1</span></span>

<span data-ttu-id="cc80c-1923">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-1923">2</span></span>

<span data-ttu-id="cc80c-1924">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1924">3</span></span>

<span data-ttu-id="cc80c-1925">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-1925">4</span></span>

<span data-ttu-id="cc80c-1926">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-1926">5</span></span>

<span data-ttu-id="cc80c-1927">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-1927">6</span></span>

<span data-ttu-id="cc80c-1928">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-1928">7</span></span>

<span data-ttu-id="cc80c-1929">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-1929">8</span></span>

<span data-ttu-id="cc80c-1930">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-1930">9</span></span>

<span data-ttu-id="cc80c-1931">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-1931">3</span></span><br/> <span data-ttu-id="cc80c-1932">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-1932">0</span></span><br/>

<span data-ttu-id="cc80c-1933">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-1933">1</span></span>

<span data-ttu-id="cc80c-1934">DBPROPID</span><span class="sxs-lookup"><span data-stu-id="cc80c-1934">DBPROPID</span></span>

<span data-ttu-id="cc80c-1935">DBPROPOPTIONS</span><span class="sxs-lookup"><span data-stu-id="cc80c-1935">DBPROPOPTIONS</span></span>

<span data-ttu-id="cc80c-1936">DBPROPSTATUS</span><span class="sxs-lookup"><span data-stu-id="cc80c-1936">DBPROPSTATUS</span></span>

<span data-ttu-id="cc80c-1937">("variable")</span><span class="sxs-lookup"><span data-stu-id="cc80c-1937">colid (variable)</span></span>

<span data-ttu-id="cc80c-1938">vValue (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-1938">vValue (variable)</span></span>



 

<span data-ttu-id="cc80c-1939">**DBPROPID:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Eigenschaften-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1939">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="cc80c-1940">**DBPROPOPTIONS:** MUSS auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1940">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="cc80c-1941">**DBPROPSTATUS:** MUSS auf "0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1941">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="cc80c-1942">**dlld:** Eine CDbColId-Struktur, wie in Abschnitt 2.2.1.20 angegeben, die die Spalte angibt, für die die Eigenschaft gilt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1942">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="cc80c-1943">**vValue:** Ein CBaseStorageVariant, der den Eigenschaftswert enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1943">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="cc80c-1944">2.2.1.21.1 Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc80c-1944">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="cc80c-1945">In diesem Abschnitt werden die Eigenschaften beschrieben, die von CISP verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1945">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="cc80c-1946">Diese Eigenschaften werden in drei Eigenschaftensätze gruppiert: ident2.2.1.21.1, die im Feld guidPropertySet der CDbPropSet-Struktur (Abschnitt 2.2.1.22) überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1946">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="cc80c-1947">In der folgenden Tabelle sind die Eigenschaften aufgeführt, die Teil des DBPROPSET \_ FSCIFRMWRK \_ EXT-Eigenschaftensatzes sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1947">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="cc80c-1948">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-1948">Value</span></span>                                  | <span data-ttu-id="cc80c-1949">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-1949">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-1950">DBPROP \_ CI CATALOG NAME \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-1950">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="cc80c-1951">Gibt den Namen des oder der abzufragenden Kataloge an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1951">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="cc80c-1952">Der Wert MUSS ein VT \_ LPWSTR oder ein VT \_ VECTOR \| VT \_ LPWSTR sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="cc80c-1953">DBPROP \_ CI \_ INCLUDE \_ SCOPES 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-1953">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="cc80c-1954">Gibt einen oder mehrere Pfade an, die in die Abfrage eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1954">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="cc80c-1955">Der Wert MUSS ein VT \_ LPWSTR oder ein VT \_ VECTOR \| VT \_ LPWSTR sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1955">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="cc80c-1956">DBPROP \_ CI \_ SCOPE \_ FLAGS 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cc80c-1956">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="cc80c-1957">Gibt an, wie die von der DBPROP \_ CI \_ INCLUDE SCOPES-Eigenschaft angegebenen Pfade \_ behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1957">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="cc80c-1958">Der Wert MUSS ein VT \_ I4 oder ein VT \_ VECTOR \| VT \_ I4 sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1958">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="cc80c-1959">DBPROP \_ CI QUERY TYPE \_ \_ 0x00000007</span><span class="sxs-lookup"><span data-stu-id="cc80c-1959">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="cc80c-1960">Gibt den Typ der Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1960">Specifies the type of query.</span></span> <span data-ttu-id="cc80c-1961">Die CDbColId MUSS auf DB NULLID festgelegt \_ werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1961">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="cc80c-1962">In der folgenden Tabelle sind die Flags für die DBPROP \_ CI \_ SCOPE \_ FLAGS-Eigenschaft aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-1962">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="cc80c-1963">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-1963">Value</span></span>                     | <span data-ttu-id="cc80c-1964">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-1964">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-1965">QUERY \_ DEEP 0x01</span><span class="sxs-lookup"><span data-stu-id="cc80c-1965">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="cc80c-1966">Wenn festgelegt, gibt an, dass Dateien im Bereichsverzeichnis und in allen Unterverzeichnissen in den Ergebnissen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1966">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="cc80c-1967">Wenn dies klar ist, sind nur Dateien im Bereichsverzeichnis in den Ergebnissen enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1967">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="cc80c-1968">DARF NICHT mit QUERY DEEP kombiniert \_ werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1968">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="cc80c-1969">QUERY \_ VIRTUAL \_ PATH 0x02</span><span class="sxs-lookup"><span data-stu-id="cc80c-1969">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="cc80c-1970">Wenn festgelegt, gibt an, dass der Bereich ein virtueller Pfad ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1970">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="cc80c-1971">Wenn dies klar ist, gibt an, dass der Bereich ein physisches Verzeichnis ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1971">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="cc80c-1972">In der folgenden Tabelle sind die Abfragetypen für die DBPROP \_ CI \_ QUERY \_ TYPE-Eigenschaft aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-1972">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="cc80c-1973">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-1973">Value</span></span>                     | <span data-ttu-id="cc80c-1974">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-1974">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-1975">CiNormal 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-1975">CiNormal 0x00000000</span></span>       | <span data-ttu-id="cc80c-1976">Eine reguläre Abfrage.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1976">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="cc80c-1977">CiVirtualRoots-0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-1977">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="cc80c-1978">Die Abfrage fordert eine Liste der virtuellen Stämme des Katalogs an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1978">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="cc80c-1979">Dieser Wert erfordert Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1979">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="cc80c-1980">CiProperties-0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-1980">CiProperties 0x00000003</span></span>   | <span data-ttu-id="cc80c-1981">Die Abfrage fordert eine Liste aller Eigenschaften an, die vom Indizierungsdienst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1981">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="cc80c-1982">CiAdminOp-0x00000004</span><span class="sxs-lookup"><span data-stu-id="cc80c-1982">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="cc80c-1983">Die Abfrage ist ein Verwaltungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1983">The query is an administrative operation.</span></span> <span data-ttu-id="cc80c-1984">Dieser Wert erfordert Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1984">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="cc80c-1985">In der folgenden Tabelle sind die Eigenschaften aufgeführt, die Teil des DBPROPSET \_ QUERYEXT-Eigenschaftensatz sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1985">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="cc80c-1986">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-1986">Value</span></span>                                      | <span data-ttu-id="cc80c-1987">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-1987">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-1988">DBPROP \_ USECONTENTINDEX-0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-1988">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="cc80c-1989">Gibt an, wie der Indizierungsdienst langsame Abfragen verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1989">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="cc80c-1990">Der Wert MUSS ein \_ VT-BOOL sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1990">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="cc80c-1991">True gibt an, dass der Server diese Abfragen nicht erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1991">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="cc80c-1992">DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-1992">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="cc80c-1993">Gibt an, ob der Indizierungsdienst das Kürzen von Ergebnissen ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1993">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="cc80c-1994">True gibt an, dass der Server in Erwägung ziehen soll, Ergebnisse so zu kürzen, dass die Antwortzeit für den Client optimiert wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1994">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="cc80c-1995">Der Wert MUSS ein \_ VT-BOOL sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1995">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="cc80c-1996">DBPROP \_ USEEXTENDEDDBTYPES 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cc80c-1996">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="cc80c-1997">Gibt an, ob der Client VT \_ VECTOR-Datentypen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1997">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="cc80c-1998">True gibt an, dass der Client VT \_ VECTOR unterstützt. Bei FALSE konvertiert der Server VT \_ VECTOR-Datentypen in VT \_ ARRAY-Datentypen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1998">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="cc80c-1999">Der Wert MUSS eine \_ VT-BOOL sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-1999">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="cc80c-2000">DBPROP \_ FIRSTROWS-0x00000007</span><span class="sxs-lookup"><span data-stu-id="cc80c-2000">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="cc80c-2001">Gibt die zurückzugebenden Zeilen übereinstimmungen an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2001">Indicates the row matches to return.</span></span> <span data-ttu-id="cc80c-2002">True gibt an, dass der Server den ersten Satz übereinstimmender Zeilen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2002">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="cc80c-2003">False gibt an, dass die am besten übereinstimmenden Zeilen zurückgegeben werden sollten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2003">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="cc80c-2004">Der Wert MUSS ein \_ VT-BOOL sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2004">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="cc80c-2005">In der folgenden Tabelle sind die Eigenschaften aufgeführt, die Teil des DBPROPSET \_ CIFRMWRKCORE \_ EXT-Eigenschaftensatzes sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2005">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="cc80c-2006">Value/DBPROPID</span><span class="sxs-lookup"><span data-stu-id="cc80c-2006">Value / DBPROPID</span></span>                 | <span data-ttu-id="cc80c-2007">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-2007">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-2008">DBPROP \_ MACHINE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-2008">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="cc80c-2009">Gibt die Namen der Computer an, auf denen eine Abfrage verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2009">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="cc80c-2010">Der Wert MUSS entweder VT \_ BSTR oder VT \_ ARRAY \| VT \_ BSTR sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2010">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="cc80c-2011">DBPROP \_ CLIENT \_ CLSID 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-2011">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="cc80c-2012">Gibt eine Verbindungskonst constant für den Indizierungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2012">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="cc80c-2013">Der Wert MUSS eine \_ VT-CLSID sein, die 0x2A4880706FD911D0A80800A0C906241A.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2013">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="cc80c-2014">2.2.1.22 CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="cc80c-2014">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="cc80c-2015">Die CDbPropSet-Struktur enthält einen Satz von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2015">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="cc80c-2016">Beachten Sie, dass das erste Feld eine feste Größe hat, aber möglicherweise nicht an einem Offset ausgerichtet ist, bei dem es sich um ein 4-Byte-Vielfaches vom Anfang der Nachricht handelt, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2016">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="cc80c-2017">Das Feld cProperties ist jedoch so ausgerichtet, und das Format wird daher wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-2017">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="cc80c-2018">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2018">0</span></span>

<span data-ttu-id="cc80c-2019">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2019">1</span></span>

<span data-ttu-id="cc80c-2020">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2020">2</span></span>

<span data-ttu-id="cc80c-2021">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2021">3</span></span>

<span data-ttu-id="cc80c-2022">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2022">4</span></span>

<span data-ttu-id="cc80c-2023">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2023">5</span></span>

<span data-ttu-id="cc80c-2024">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2024">6</span></span>

<span data-ttu-id="cc80c-2025">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2025">7</span></span>

<span data-ttu-id="cc80c-2026">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2026">8</span></span>

<span data-ttu-id="cc80c-2027">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2027">9</span></span>

<span data-ttu-id="cc80c-2028">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2028">1</span></span><br/> <span data-ttu-id="cc80c-2029">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2029">0</span></span><br/>

<span data-ttu-id="cc80c-2030">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2030">1</span></span>

<span data-ttu-id="cc80c-2031">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2031">2</span></span>

<span data-ttu-id="cc80c-2032">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2032">3</span></span>

<span data-ttu-id="cc80c-2033">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2033">4</span></span>

<span data-ttu-id="cc80c-2034">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2034">5</span></span>

<span data-ttu-id="cc80c-2035">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2035">6</span></span>

<span data-ttu-id="cc80c-2036">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2036">7</span></span>

<span data-ttu-id="cc80c-2037">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2037">8</span></span>

<span data-ttu-id="cc80c-2038">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2038">9</span></span>

<span data-ttu-id="cc80c-2039">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2039">2</span></span><br/> <span data-ttu-id="cc80c-2040">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2040">0</span></span><br/>

<span data-ttu-id="cc80c-2041">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2041">1</span></span>

<span data-ttu-id="cc80c-2042">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2042">2</span></span>

<span data-ttu-id="cc80c-2043">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2043">3</span></span>

<span data-ttu-id="cc80c-2044">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2044">4</span></span>

<span data-ttu-id="cc80c-2045">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2045">5</span></span>

<span data-ttu-id="cc80c-2046">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2046">6</span></span>

<span data-ttu-id="cc80c-2047">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2047">7</span></span>

<span data-ttu-id="cc80c-2048">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2048">8</span></span>

<span data-ttu-id="cc80c-2049">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2049">9</span></span>

<span data-ttu-id="cc80c-2050">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2050">3</span></span><br/> <span data-ttu-id="cc80c-2051">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2051">0</span></span><br/>

<span data-ttu-id="cc80c-2052">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2052">1</span></span>

<span data-ttu-id="cc80c-2053">guidPropertySet</span><span class="sxs-lookup"><span data-stu-id="cc80c-2053">guidPropertySet</span></span>

<span data-ttu-id="cc80c-2054">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-2054">...</span></span>

<span data-ttu-id="cc80c-2055">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-2055">...</span></span>

<span data-ttu-id="cc80c-2056">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-2056">...</span></span>

<span data-ttu-id="cc80c-2057">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-2057">...</span></span>

<span data-ttu-id="cc80c-2058">\_Auf padding (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2058">\_padding (variable)</span></span>

<span data-ttu-id="cc80c-2059">cProperties</span><span class="sxs-lookup"><span data-stu-id="cc80c-2059">cProperties</span></span>

<span data-ttu-id="cc80c-2060">aProps (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2060">aProps (variable)</span></span>



 

<span data-ttu-id="cc80c-2061">**guidPropertySet:** Eine GUID, die den Eigenschaftensatz identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2061">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="cc80c-2062">MUSS auf das binäre Formular festgelegt werden, das einem der folgenden Werte entspricht (in Form einer Zeichenfolgendarstellung dargestellt), die den Eigenschaftensatz der eigenschaften identifiziert, die im aProps-Feld enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2062">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="cc80c-2063">Wert/GUID</span><span class="sxs-lookup"><span data-stu-id="cc80c-2063">Value / GUID</span></span>                                                                              | <span data-ttu-id="cc80c-2064">Name</span><span class="sxs-lookup"><span data-stu-id="cc80c-2064">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="cc80c-2065">DBPROPSET \_ FSCIFRMWRK \_ EXT</span><span class="sxs-lookup"><span data-stu-id="cc80c-2065">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="cc80c-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="cc80c-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="cc80c-2067">File System Content Index Framework-Eigenschaftensatz</span><span class="sxs-lookup"><span data-stu-id="cc80c-2067">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="cc80c-2068">DBPROPSET \_ QUERYEXT</span><span class="sxs-lookup"><span data-stu-id="cc80c-2068">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="cc80c-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="cc80c-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="cc80c-2070">Eigenschaftensatz der Abfrageerweiterung</span><span class="sxs-lookup"><span data-stu-id="cc80c-2070">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="cc80c-2071">DBPROPSET \_ CIFRMWRKCORE \_ EXT</span><span class="sxs-lookup"><span data-stu-id="cc80c-2071">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="cc80c-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="cc80c-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="cc80c-2073">Content Index Framework Core Property Set</span><span class="sxs-lookup"><span data-stu-id="cc80c-2073">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="cc80c-2074">**\_ Auffüllung:** Dieses Feld MUSS 0 bis 3 Bytes lang sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2074">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cc80c-2075">Die Länge dieses Felds MUSS so sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Bytes ab dem Anfang der Nachricht ist, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2075">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cc80c-2076">Wenn dieses Feld vorhanden ist (d. h. die Länge ungleich null), ist der darin enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2076">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cc80c-2077">Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2077">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cc80c-2078">**cProperties:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im aProps-Array enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2078">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="cc80c-2079">**aProps:** Ein Array von CDbProp-Strukturen, wie in Abschnitt 0 angegeben, das Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2079">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="cc80c-2080">Strukturen im Array MÜSSEN durch 0 bis 3 Auffüllungsbytes getrennt werden, sodass jede Struktur bei einem Offset beginnt, der ein Vielfaches von 4 Bytes vom Anfang der Nachricht ist, die dieses Array enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2080">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="cc80c-2081">Wenn auffüllende Bytes vorhanden sind, ist der darin enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2081">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="cc80c-2082">Der Inhalt der Auffüllungsbytes MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2082">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="cc80c-2083">2.2.1.23 CPidMapper</span><span class="sxs-lookup"><span data-stu-id="cc80c-2083">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="cc80c-2084">Die CPidMapper-Struktur enthält ein Array von Eigenschaften-IDs, die die Eigenschaften angeben, die in einem Rowset zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2084">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="cc80c-2085">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2085">0</span></span>

<span data-ttu-id="cc80c-2086">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2086">1</span></span>

<span data-ttu-id="cc80c-2087">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2087">2</span></span>

<span data-ttu-id="cc80c-2088">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2088">3</span></span>

<span data-ttu-id="cc80c-2089">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2089">4</span></span>

<span data-ttu-id="cc80c-2090">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2090">5</span></span>

<span data-ttu-id="cc80c-2091">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2091">6</span></span>

<span data-ttu-id="cc80c-2092">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2092">7</span></span>

<span data-ttu-id="cc80c-2093">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2093">8</span></span>

<span data-ttu-id="cc80c-2094">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2094">9</span></span>

<span data-ttu-id="cc80c-2095">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2095">1</span></span><br/> <span data-ttu-id="cc80c-2096">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2096">0</span></span><br/>

<span data-ttu-id="cc80c-2097">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2097">1</span></span>

<span data-ttu-id="cc80c-2098">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2098">2</span></span>

<span data-ttu-id="cc80c-2099">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2099">3</span></span>

<span data-ttu-id="cc80c-2100">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2100">4</span></span>

<span data-ttu-id="cc80c-2101">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2101">5</span></span>

<span data-ttu-id="cc80c-2102">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2102">6</span></span>

<span data-ttu-id="cc80c-2103">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2103">7</span></span>

<span data-ttu-id="cc80c-2104">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2104">8</span></span>

<span data-ttu-id="cc80c-2105">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2105">9</span></span>

<span data-ttu-id="cc80c-2106">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2106">2</span></span><br/> <span data-ttu-id="cc80c-2107">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2107">0</span></span><br/>

<span data-ttu-id="cc80c-2108">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2108">1</span></span>

<span data-ttu-id="cc80c-2109">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2109">2</span></span>

<span data-ttu-id="cc80c-2110">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2110">3</span></span>

<span data-ttu-id="cc80c-2111">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2111">4</span></span>

<span data-ttu-id="cc80c-2112">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2112">5</span></span>

<span data-ttu-id="cc80c-2113">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2113">6</span></span>

<span data-ttu-id="cc80c-2114">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2114">7</span></span>

<span data-ttu-id="cc80c-2115">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2115">8</span></span>

<span data-ttu-id="cc80c-2116">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2116">9</span></span>

<span data-ttu-id="cc80c-2117">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2117">3</span></span><br/> <span data-ttu-id="cc80c-2118">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2118">0</span></span><br/>

<span data-ttu-id="cc80c-2119">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2119">1</span></span>

<span data-ttu-id="cc80c-2120">count</span><span class="sxs-lookup"><span data-stu-id="cc80c-2120">count</span></span>

<span data-ttu-id="cc80c-2121">aPropSpec</span><span class="sxs-lookup"><span data-stu-id="cc80c-2121">aPropSpec</span></span>

<span data-ttu-id="cc80c-2122">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2122">... (variable)</span></span>



 

<span data-ttu-id="cc80c-2123">**count:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im aPropSpec-Array enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2123">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="cc80c-2124">**aPropSpec:** Array von CFullPropSpec-Strukturen, die die zurückzugebenden Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2124">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="cc80c-2125">Strukturen im Array MÜSSEN durch 0 bis 3 Auffüllungsbytes getrennt werden, sodass jede Struktur eine 4-Byte-Ausrichtung vom Anfang einer Nachricht aufweist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2125">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="cc80c-2126">Solche Auffüllungsbytes können beliebige Werte sein, und MÜSSEN beim Empfang ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2126">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="cc80c-2127">2.2.1.24 CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="cc80c-2127">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="cc80c-2128">Die CRowSeekAt-Struktur enthält den Offset, an dem Zeilen in einer CPMGetRowsIn-Nachricht abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2128">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="cc80c-2129">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2129">0</span></span>

<span data-ttu-id="cc80c-2130">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2130">1</span></span>

<span data-ttu-id="cc80c-2131">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2131">2</span></span>

<span data-ttu-id="cc80c-2132">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2132">3</span></span>

<span data-ttu-id="cc80c-2133">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2133">4</span></span>

<span data-ttu-id="cc80c-2134">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2134">5</span></span>

<span data-ttu-id="cc80c-2135">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2135">6</span></span>

<span data-ttu-id="cc80c-2136">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2136">7</span></span>

<span data-ttu-id="cc80c-2137">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2137">8</span></span>

<span data-ttu-id="cc80c-2138">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2138">9</span></span>

<span data-ttu-id="cc80c-2139">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2139">1</span></span><br/> <span data-ttu-id="cc80c-2140">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2140">0</span></span><br/>

<span data-ttu-id="cc80c-2141">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2141">1</span></span>

<span data-ttu-id="cc80c-2142">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2142">2</span></span>

<span data-ttu-id="cc80c-2143">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2143">3</span></span>

<span data-ttu-id="cc80c-2144">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2144">4</span></span>

<span data-ttu-id="cc80c-2145">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2145">5</span></span>

<span data-ttu-id="cc80c-2146">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2146">6</span></span>

<span data-ttu-id="cc80c-2147">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2147">7</span></span>

<span data-ttu-id="cc80c-2148">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2148">8</span></span>

<span data-ttu-id="cc80c-2149">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2149">9</span></span>

<span data-ttu-id="cc80c-2150">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2150">2</span></span><br/> <span data-ttu-id="cc80c-2151">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2151">0</span></span><br/>

<span data-ttu-id="cc80c-2152">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2152">1</span></span>

<span data-ttu-id="cc80c-2153">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2153">2</span></span>

<span data-ttu-id="cc80c-2154">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2154">3</span></span>

<span data-ttu-id="cc80c-2155">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2155">4</span></span>

<span data-ttu-id="cc80c-2156">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2156">5</span></span>

<span data-ttu-id="cc80c-2157">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2157">6</span></span>

<span data-ttu-id="cc80c-2158">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2158">7</span></span>

<span data-ttu-id="cc80c-2159">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2159">8</span></span>

<span data-ttu-id="cc80c-2160">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2160">9</span></span>

<span data-ttu-id="cc80c-2161">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2161">3</span></span><br/> <span data-ttu-id="cc80c-2162">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2162">0</span></span><br/>

<span data-ttu-id="cc80c-2163">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2163">1</span></span>

<span data-ttu-id="cc80c-2164">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="cc80c-2164">\_hRegion</span></span>

<span data-ttu-id="cc80c-2165">\_cskip</span><span class="sxs-lookup"><span data-stu-id="cc80c-2165">\_cskip</span></span>

<span data-ttu-id="cc80c-2166">\_bmkOffset</span><span class="sxs-lookup"><span data-stu-id="cc80c-2166">\_bmkOffset</span></span>



 

<span data-ttu-id="cc80c-2167">**\_ hRegion:** MUSS auf 0x00000000 und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2167">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="cc80c-2168">**\_ cskip:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeilen enthält, die im Rowset übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2168">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="cc80c-2169">**\_ bmkOffset:** Ein 32-Bit-Wert,  der das Handle des Lesezeichens darstellt und die Startposition angibt, von der aus die Anzahl der in cskip angegebenen Zeilen vor beginn des Abrufs übersprungen \_ werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2169">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="cc80c-2170">2.2.1.25 CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="cc80c-2170">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="cc80c-2171">Die CRowSeekAtRatio-Struktur identifiziert den Punkt, an dem der Abruf für eine CPMGetRowsIn-Nachricht beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2171">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="cc80c-2172">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2172">0</span></span>

<span data-ttu-id="cc80c-2173">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2173">1</span></span>

<span data-ttu-id="cc80c-2174">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2174">2</span></span>

<span data-ttu-id="cc80c-2175">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2175">3</span></span>

<span data-ttu-id="cc80c-2176">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2176">4</span></span>

<span data-ttu-id="cc80c-2177">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2177">5</span></span>

<span data-ttu-id="cc80c-2178">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2178">6</span></span>

<span data-ttu-id="cc80c-2179">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2179">7</span></span>

<span data-ttu-id="cc80c-2180">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2180">8</span></span>

<span data-ttu-id="cc80c-2181">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2181">9</span></span>

<span data-ttu-id="cc80c-2182">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2182">1</span></span><br/> <span data-ttu-id="cc80c-2183">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2183">0</span></span><br/>

<span data-ttu-id="cc80c-2184">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2184">1</span></span>

<span data-ttu-id="cc80c-2185">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2185">2</span></span>

<span data-ttu-id="cc80c-2186">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2186">3</span></span>

<span data-ttu-id="cc80c-2187">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2187">4</span></span>

<span data-ttu-id="cc80c-2188">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2188">5</span></span>

<span data-ttu-id="cc80c-2189">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2189">6</span></span>

<span data-ttu-id="cc80c-2190">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2190">7</span></span>

<span data-ttu-id="cc80c-2191">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2191">8</span></span>

<span data-ttu-id="cc80c-2192">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2192">9</span></span>

<span data-ttu-id="cc80c-2193">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2193">2</span></span><br/> <span data-ttu-id="cc80c-2194">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2194">0</span></span><br/>

<span data-ttu-id="cc80c-2195">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2195">1</span></span>

<span data-ttu-id="cc80c-2196">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2196">2</span></span>

<span data-ttu-id="cc80c-2197">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2197">3</span></span>

<span data-ttu-id="cc80c-2198">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2198">4</span></span>

<span data-ttu-id="cc80c-2199">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2199">5</span></span>

<span data-ttu-id="cc80c-2200">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2200">6</span></span>

<span data-ttu-id="cc80c-2201">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2201">7</span></span>

<span data-ttu-id="cc80c-2202">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2202">8</span></span>

<span data-ttu-id="cc80c-2203">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2203">9</span></span>

<span data-ttu-id="cc80c-2204">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2204">3</span></span><br/> <span data-ttu-id="cc80c-2205">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2205">0</span></span><br/>

<span data-ttu-id="cc80c-2206">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2206">1</span></span>

<span data-ttu-id="cc80c-2207">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="cc80c-2207">CiTblChapt</span></span>

<span data-ttu-id="cc80c-2208">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="cc80c-2208">\_hRegion</span></span>

<span data-ttu-id="cc80c-2209">\_ulNumerator</span><span class="sxs-lookup"><span data-stu-id="cc80c-2209">\_ulNumerator</span></span>

<span data-ttu-id="cc80c-2210">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="cc80c-2210">\_ulDenominator</span></span>



 

<span data-ttu-id="cc80c-2211">**CiTblChapt:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Rowset-Kapitel angibt, aus dem Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2211">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="cc80c-2212">**\_ hRegion:** MUSS auf 0x00000000 und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2212">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="cc80c-2213">**\_ ulNumerator:** 32-Bit-Ganzzahl ohne Vorzeichen, die den Zähler des Zeilenverhältnisses im Kapitel darstellt, ab dem mit dem Abruf begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2213">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="cc80c-2214">**\_ ulDenominator:** 32-Bit-Ganzzahl ohne Vorzeichen, die den Nenner des Zeilenverhältnisses im Kapitel darstellt, ab dem mit dem Abruf begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2214">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="cc80c-2215">MUSS größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2215">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="cc80c-2216">2.2.1.26 CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="cc80c-2216">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="cc80c-2217">Die CRowSeekByBookmark-Struktur identifiziert die Lesezeichen, aus denen Zeilen für eine CPMGetRowsIn-Nachricht abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2217">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="cc80c-2218">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2218">0</span></span>

<span data-ttu-id="cc80c-2219">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2219">1</span></span>

<span data-ttu-id="cc80c-2220">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2220">2</span></span>

<span data-ttu-id="cc80c-2221">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2221">3</span></span>

<span data-ttu-id="cc80c-2222">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2222">4</span></span>

<span data-ttu-id="cc80c-2223">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2223">5</span></span>

<span data-ttu-id="cc80c-2224">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2224">6</span></span>

<span data-ttu-id="cc80c-2225">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2225">7</span></span>

<span data-ttu-id="cc80c-2226">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2226">8</span></span>

<span data-ttu-id="cc80c-2227">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2227">9</span></span>

<span data-ttu-id="cc80c-2228">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2228">1</span></span><br/> <span data-ttu-id="cc80c-2229">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2229">0</span></span><br/>

<span data-ttu-id="cc80c-2230">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2230">1</span></span>

<span data-ttu-id="cc80c-2231">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2231">2</span></span>

<span data-ttu-id="cc80c-2232">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2232">3</span></span>

<span data-ttu-id="cc80c-2233">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2233">4</span></span>

<span data-ttu-id="cc80c-2234">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2234">5</span></span>

<span data-ttu-id="cc80c-2235">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2235">6</span></span>

<span data-ttu-id="cc80c-2236">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2236">7</span></span>

<span data-ttu-id="cc80c-2237">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2237">8</span></span>

<span data-ttu-id="cc80c-2238">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2238">9</span></span>

<span data-ttu-id="cc80c-2239">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2239">2</span></span><br/> <span data-ttu-id="cc80c-2240">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2240">0</span></span><br/>

<span data-ttu-id="cc80c-2241">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2241">1</span></span>

<span data-ttu-id="cc80c-2242">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2242">2</span></span>

<span data-ttu-id="cc80c-2243">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2243">3</span></span>

<span data-ttu-id="cc80c-2244">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2244">4</span></span>

<span data-ttu-id="cc80c-2245">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2245">5</span></span>

<span data-ttu-id="cc80c-2246">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2246">6</span></span>

<span data-ttu-id="cc80c-2247">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2247">7</span></span>

<span data-ttu-id="cc80c-2248">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2248">8</span></span>

<span data-ttu-id="cc80c-2249">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2249">9</span></span>

<span data-ttu-id="cc80c-2250">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2250">3</span></span><br/> <span data-ttu-id="cc80c-2251">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2251">0</span></span><br/>

<span data-ttu-id="cc80c-2252">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2252">1</span></span>

<span data-ttu-id="cc80c-2253">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="cc80c-2253">\_hRegion</span></span>

<span data-ttu-id="cc80c-2254">\_cBookmarks</span><span class="sxs-lookup"><span data-stu-id="cc80c-2254">\_cBookmarks</span></span>

<span data-ttu-id="cc80c-2255">\_maxRet</span><span class="sxs-lookup"><span data-stu-id="cc80c-2255">\_maxRet</span></span>

<span data-ttu-id="cc80c-2256">\_cValidRet</span><span class="sxs-lookup"><span data-stu-id="cc80c-2256">\_cValidRet</span></span>

<span data-ttu-id="cc80c-2257">\_aBookmarks (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2257">\_aBookmarks (variable)</span></span>

<span data-ttu-id="cc80c-2258">\_ascRet (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2258">\_ascRet (variable)</span></span>



 

<span data-ttu-id="cc80c-2259">**\_ hRegion:** MUSS auf 0x00000000 festgelegt werden, und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2259">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="cc80c-2260">**\_ cBookmarks:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im \_ aBookmarks-Array darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2260">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="cc80c-2261">**\_ maxRet:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im \_ ascRet-Array darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2261">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="cc80c-2262">**\_ cValidRet:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl gültiger Elemente im \_ ascRet-Array darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2262">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="cc80c-2263">Gültige Elemente wurden im Array definiert, während ungültige Elemente nicht definiert sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2263">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="cc80c-2264">**\_ aBookmarks:** Ein Array von Lesezeichenhandles (jeweils durch 4 Bytes dargestellt), wie aus einer CPMGetRowsOut-Nachricht abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2264">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="cc80c-2265">**\_ ascRet:** Ein Array von HRESULT-Werten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2265">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="cc80c-2266">Wenn CRowSeekByBookMark als Teil der CPMGetRowsIn-Anforderung gesendet wird, MUSS die Anzahl der Einträge im Array \_ gleich cBookMarks sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2266">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="cc80c-2267">Beim Senden durch den Client MÜSSEN die Werte auf 0 festgelegt werden, und der Server MUSS den Inhalt des Arrays ignorieren.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2267">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="cc80c-2268">Beim Senden durch den Server (als Teil der CPMGetRowsOut-Nachricht) geben die Werte im Array den Ergebnisstatus für jeden Zeilenabruf an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2268">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="cc80c-2269">2.2.1.27 CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="cc80c-2269">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="cc80c-2270">Die CRowSeekNext-Struktur enthält die Anzahl der Zeilen, die in einer CPMGetRowsIn-Nachricht übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2270">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="cc80c-2271">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2271">0</span></span>

<span data-ttu-id="cc80c-2272">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2272">1</span></span>

<span data-ttu-id="cc80c-2273">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2273">2</span></span>

<span data-ttu-id="cc80c-2274">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2274">3</span></span>

<span data-ttu-id="cc80c-2275">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2275">4</span></span>

<span data-ttu-id="cc80c-2276">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2276">5</span></span>

<span data-ttu-id="cc80c-2277">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2277">6</span></span>

<span data-ttu-id="cc80c-2278">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2278">7</span></span>

<span data-ttu-id="cc80c-2279">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2279">8</span></span>

<span data-ttu-id="cc80c-2280">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2280">9</span></span>

<span data-ttu-id="cc80c-2281">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2281">1</span></span><br/> <span data-ttu-id="cc80c-2282">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2282">0</span></span><br/>

<span data-ttu-id="cc80c-2283">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2283">1</span></span>

<span data-ttu-id="cc80c-2284">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2284">2</span></span>

<span data-ttu-id="cc80c-2285">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2285">3</span></span>

<span data-ttu-id="cc80c-2286">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2286">4</span></span>

<span data-ttu-id="cc80c-2287">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2287">5</span></span>

<span data-ttu-id="cc80c-2288">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2288">6</span></span>

<span data-ttu-id="cc80c-2289">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2289">7</span></span>

<span data-ttu-id="cc80c-2290">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2290">8</span></span>

<span data-ttu-id="cc80c-2291">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2291">9</span></span>

<span data-ttu-id="cc80c-2292">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2292">2</span></span><br/> <span data-ttu-id="cc80c-2293">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2293">0</span></span><br/>

<span data-ttu-id="cc80c-2294">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2294">1</span></span>

<span data-ttu-id="cc80c-2295">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2295">2</span></span>

<span data-ttu-id="cc80c-2296">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2296">3</span></span>

<span data-ttu-id="cc80c-2297">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2297">4</span></span>

<span data-ttu-id="cc80c-2298">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2298">5</span></span>

<span data-ttu-id="cc80c-2299">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2299">6</span></span>

<span data-ttu-id="cc80c-2300">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2300">7</span></span>

<span data-ttu-id="cc80c-2301">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2301">8</span></span>

<span data-ttu-id="cc80c-2302">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2302">9</span></span>

<span data-ttu-id="cc80c-2303">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2303">3</span></span><br/> <span data-ttu-id="cc80c-2304">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2304">0</span></span><br/>

<span data-ttu-id="cc80c-2305">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2305">1</span></span>

<span data-ttu-id="cc80c-2306">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="cc80c-2306">CiTblChapt</span></span>

<span data-ttu-id="cc80c-2307">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="cc80c-2307">\_hRegion</span></span>

<span data-ttu-id="cc80c-2308">\_cskip</span><span class="sxs-lookup"><span data-stu-id="cc80c-2308">\_cskip</span></span>



 

<span data-ttu-id="cc80c-2309">**CiTblChapt:** 32-Bit-Ganzzahl ohne Vorzeichen, die das Rowset-Kapitel angibt, aus dem Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2309">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="cc80c-2310">**\_ hRegion:** MUSS auf 0x00000000 und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2310">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="cc80c-2311">**\_ cskip**: 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeilen darstellt, die im Rowset übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2311">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="cc80c-2312">2.2.1.28 CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="cc80c-2312">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="cc80c-2313">Die CRowsetProperties-Struktur enthält Konfigurationsinformationen für eine Abfrage.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2313">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="cc80c-2314">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2314">0</span></span>

<span data-ttu-id="cc80c-2315">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2315">1</span></span>

<span data-ttu-id="cc80c-2316">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2316">2</span></span>

<span data-ttu-id="cc80c-2317">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2317">3</span></span>

<span data-ttu-id="cc80c-2318">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2318">4</span></span>

<span data-ttu-id="cc80c-2319">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2319">5</span></span>

<span data-ttu-id="cc80c-2320">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2320">6</span></span>

<span data-ttu-id="cc80c-2321">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2321">7</span></span>

<span data-ttu-id="cc80c-2322">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2322">8</span></span>

<span data-ttu-id="cc80c-2323">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2323">9</span></span>

<span data-ttu-id="cc80c-2324">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2324">1</span></span><br/> <span data-ttu-id="cc80c-2325">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2325">0</span></span><br/>

<span data-ttu-id="cc80c-2326">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2326">1</span></span>

<span data-ttu-id="cc80c-2327">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2327">2</span></span>

<span data-ttu-id="cc80c-2328">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2328">3</span></span>

<span data-ttu-id="cc80c-2329">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2329">4</span></span>

<span data-ttu-id="cc80c-2330">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2330">5</span></span>

<span data-ttu-id="cc80c-2331">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2331">6</span></span>

<span data-ttu-id="cc80c-2332">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2332">7</span></span>

<span data-ttu-id="cc80c-2333">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2333">8</span></span>

<span data-ttu-id="cc80c-2334">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2334">9</span></span>

<span data-ttu-id="cc80c-2335">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2335">2</span></span><br/> <span data-ttu-id="cc80c-2336">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2336">0</span></span><br/>

<span data-ttu-id="cc80c-2337">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2337">1</span></span>

<span data-ttu-id="cc80c-2338">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2338">2</span></span>

<span data-ttu-id="cc80c-2339">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2339">3</span></span>

<span data-ttu-id="cc80c-2340">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2340">4</span></span>

<span data-ttu-id="cc80c-2341">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2341">5</span></span>

<span data-ttu-id="cc80c-2342">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2342">6</span></span>

<span data-ttu-id="cc80c-2343">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2343">7</span></span>

<span data-ttu-id="cc80c-2344">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2344">8</span></span>

<span data-ttu-id="cc80c-2345">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2345">9</span></span>

<span data-ttu-id="cc80c-2346">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2346">3</span></span><br/> <span data-ttu-id="cc80c-2347">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2347">0</span></span><br/>

<span data-ttu-id="cc80c-2348">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2348">1</span></span>

<span data-ttu-id="cc80c-2349">\_uBooleanOptions</span><span class="sxs-lookup"><span data-stu-id="cc80c-2349">\_uBooleanOptions</span></span>

<span data-ttu-id="cc80c-2350">\_ulMaxOpenRows</span><span class="sxs-lookup"><span data-stu-id="cc80c-2350">\_ulMaxOpenRows</span></span>

<span data-ttu-id="cc80c-2351">\_ulMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="cc80c-2351">\_ulMemoryUsage</span></span>

<span data-ttu-id="cc80c-2352">\_cMaxResults</span><span class="sxs-lookup"><span data-stu-id="cc80c-2352">\_cMaxResults</span></span>

<span data-ttu-id="cc80c-2353">\_cCmdTimeout</span><span class="sxs-lookup"><span data-stu-id="cc80c-2353">\_cCmdTimeout</span></span>



 

<span data-ttu-id="cc80c-2354">**\_ uBooleanOptions:** Die am wenigsten signifikanten 3 Bits dieses Felds MÜSSEN einen der folgenden drei Werte enthalten:</span><span class="sxs-lookup"><span data-stu-id="cc80c-2354">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="cc80c-2355">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-2355">Value</span></span>                  | <span data-ttu-id="cc80c-2356">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-2356">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cc80c-2357">eSequential 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-2357">eSequential 0x00000001</span></span> | <span data-ttu-id="cc80c-2358">Der Cursor kann nur vorwärts verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2358">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="cc80c-2359">eLocatable-0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-2359">eLocatable 0x00000003</span></span>  | <span data-ttu-id="cc80c-2360">Der Cursor kann an eine beliebige Position verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2360">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="cc80c-2361">eScrollable-0x00000007</span><span class="sxs-lookup"><span data-stu-id="cc80c-2361">eScrollable 0x00000007</span></span> | <span data-ttu-id="cc80c-2362">Der Cursor kann an eine beliebige Position verschoben und in beliebige Richtung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2362">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="cc80c-2363">Die verbleibenden Bits können entweder klar sein oder auf eine beliebige Kombination der folgenden Werte logisch OR'd zusammen festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="cc80c-2363">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="cc80c-2364">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-2364">Value</span></span>                     | <span data-ttu-id="cc80c-2365">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-2365">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-2366">eAsynchronous 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cc80c-2366">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="cc80c-2367">Der Client wartet nicht auf den Abschluss der Ausführung.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2367">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="cc80c-2368">eFirstRows 0x00000080</span><span class="sxs-lookup"><span data-stu-id="cc80c-2368">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="cc80c-2369">Gibt die ersten gefundenen Zeilen zurück, nicht die besten Übereinstimmungen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2369">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="cc80c-2370">eHoldRows 0x00000200</span><span class="sxs-lookup"><span data-stu-id="cc80c-2370">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="cc80c-2371">Der Server DARF KEINE Zeilen verwerfen, bis der Client mit einer Abfrage fertig ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2371">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="cc80c-2372">eChaptered 0x00000800</span><span class="sxs-lookup"><span data-stu-id="cc80c-2372">eChaptered 0x00000800</span></span>     | <span data-ttu-id="cc80c-2373">Das Rowset unterstützt Kapitel.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2373">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="cc80c-2374">eUseCI 0x00001000</span><span class="sxs-lookup"><span data-stu-id="cc80c-2374">eUseCI 0x00001000</span></span>         | <span data-ttu-id="cc80c-2375">Beantworten Sie nur die Abfrage aus dem Index, nicht aus dem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2375">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="cc80c-2376">eDeferTrimming 0x00002000</span><span class="sxs-lookup"><span data-stu-id="cc80c-2376">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="cc80c-2377">Der Indizierungsdienst sollte beim Entfernen von Ergebnissen die Optimierung der Antwortzeit für den Client in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2377">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="cc80c-2378">**\_ ulMaxOpenRows:** 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2378">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="cc80c-2379">Muss auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="cc80c-2380">Nicht verwendet und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="cc80c-2381">**\_ ulMemoryUsage:** 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2381">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="cc80c-2382">Muss auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2382">Must be set to 0x00000000.</span></span> <span data-ttu-id="cc80c-2383">Nicht verwendet und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2383">Not used and MUST be ignored.</span></span>

<span data-ttu-id="cc80c-2384">**\_ cMaxResults:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die maximale Anzahl von Zeilen angibt, die für die Abfrage zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2384">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="cc80c-2385">**\_ cCmdTimeout:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Sekunden angibt, nach denen für eine Abfrage ein Timeout und ein automatisches Beenden ausgeführt werden soll. Dabei wird ab dem Zeitpunkt gezählt, zu dem die Abfrage auf dem Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2385">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="cc80c-2386">Der Wert 0x00000000 bedeutet, dass für die Abfrage kein Time out erfolgt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2386">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="cc80c-2387">2.2.1.29 CRowVariant</span><span class="sxs-lookup"><span data-stu-id="cc80c-2387">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="cc80c-2388">Die CRowVariant-Struktur enthält den Teil mit fester Größe eines Datentyps variabler Länge, der in der CPMGetRowsOut-Nachricht gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2388">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="cc80c-2389">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2389">0</span></span>

<span data-ttu-id="cc80c-2390">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2390">1</span></span>

<span data-ttu-id="cc80c-2391">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2391">2</span></span>

<span data-ttu-id="cc80c-2392">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2392">3</span></span>

<span data-ttu-id="cc80c-2393">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2393">4</span></span>

<span data-ttu-id="cc80c-2394">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2394">5</span></span>

<span data-ttu-id="cc80c-2395">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2395">6</span></span>

<span data-ttu-id="cc80c-2396">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2396">7</span></span>

<span data-ttu-id="cc80c-2397">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2397">8</span></span>

<span data-ttu-id="cc80c-2398">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2398">9</span></span>

<span data-ttu-id="cc80c-2399">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2399">1</span></span><br/> <span data-ttu-id="cc80c-2400">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2400">0</span></span><br/>

<span data-ttu-id="cc80c-2401">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2401">1</span></span>

<span data-ttu-id="cc80c-2402">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2402">2</span></span>

<span data-ttu-id="cc80c-2403">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2403">3</span></span>

<span data-ttu-id="cc80c-2404">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2404">4</span></span>

<span data-ttu-id="cc80c-2405">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2405">5</span></span>

<span data-ttu-id="cc80c-2406">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2406">6</span></span>

<span data-ttu-id="cc80c-2407">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2407">7</span></span>

<span data-ttu-id="cc80c-2408">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2408">8</span></span>

<span data-ttu-id="cc80c-2409">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2409">9</span></span>

<span data-ttu-id="cc80c-2410">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2410">2</span></span><br/> <span data-ttu-id="cc80c-2411">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2411">0</span></span><br/>

<span data-ttu-id="cc80c-2412">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2412">1</span></span>

<span data-ttu-id="cc80c-2413">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2413">2</span></span>

<span data-ttu-id="cc80c-2414">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2414">3</span></span>

<span data-ttu-id="cc80c-2415">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2415">4</span></span>

<span data-ttu-id="cc80c-2416">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2416">5</span></span>

<span data-ttu-id="cc80c-2417">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2417">6</span></span>

<span data-ttu-id="cc80c-2418">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2418">7</span></span>

<span data-ttu-id="cc80c-2419">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2419">8</span></span>

<span data-ttu-id="cc80c-2420">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2420">9</span></span>

<span data-ttu-id="cc80c-2421">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2421">3</span></span><br/> <span data-ttu-id="cc80c-2422">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2422">0</span></span><br/>

<span data-ttu-id="cc80c-2423">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2423">1</span></span>

<span data-ttu-id="cc80c-2424">vType</span><span class="sxs-lookup"><span data-stu-id="cc80c-2424">vType</span></span>

<span data-ttu-id="cc80c-2425">reserved1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2425">reserved1</span></span>

<span data-ttu-id="cc80c-2426">reserved2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2426">reserved2</span></span>

<span data-ttu-id="cc80c-2427">Offset (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2427">Offset (optional)</span></span>



 

<span data-ttu-id="cc80c-2428">**vType:** Ein Typindikator, der den Typ von vValue angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2428">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="cc80c-2429">Es MUSS einer der VARENUM-Werte sein, die in Abschnitt 2.2.1.1 angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2429">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="cc80c-2430">**reserved1:** Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2430">**reserved1**: Not used.</span></span> <span data-ttu-id="cc80c-2431">Der Wert kann auf einen beliebigen Wert festgelegt werden und MUSS beim Empfang ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2431">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="cc80c-2432">**reserved2:** Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2432">**reserved2**: Not used.</span></span> <span data-ttu-id="cc80c-2433">Der Wert kann auf einen beliebigen Wert festgelegt werden und MUSS beim Empfang ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2433">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="cc80c-2434">**Offset:** Ein Offset zu Daten variabler Länge (z. B. eine Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="cc80c-2434">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="cc80c-2435">Dies MUSS ein 32-Bit-Wert (4 Byte lang) sein, wenn 32-Bit-Offsets verwendet werden (nach den Regeln in Abschnitt 2.2.3.16) oder ein 64-Byte-Wert (8 Byte lang), wenn 64-Bit-Offsets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2435">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="cc80c-2436">2.2.1.30 CSortSet</span><span class="sxs-lookup"><span data-stu-id="cc80c-2436">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="cc80c-2437">Die CSortSet-Struktur enthält die Sortierreihenfolge der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2437">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="cc80c-2438">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2438">0</span></span>

<span data-ttu-id="cc80c-2439">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2439">1</span></span>

<span data-ttu-id="cc80c-2440">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2440">2</span></span>

<span data-ttu-id="cc80c-2441">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2441">3</span></span>

<span data-ttu-id="cc80c-2442">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2442">4</span></span>

<span data-ttu-id="cc80c-2443">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2443">5</span></span>

<span data-ttu-id="cc80c-2444">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2444">6</span></span>

<span data-ttu-id="cc80c-2445">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2445">7</span></span>

<span data-ttu-id="cc80c-2446">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2446">8</span></span>

<span data-ttu-id="cc80c-2447">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2447">9</span></span>

<span data-ttu-id="cc80c-2448">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2448">1</span></span><br/> <span data-ttu-id="cc80c-2449">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2449">0</span></span><br/>

<span data-ttu-id="cc80c-2450">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2450">1</span></span>

<span data-ttu-id="cc80c-2451">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2451">2</span></span>

<span data-ttu-id="cc80c-2452">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2452">3</span></span>

<span data-ttu-id="cc80c-2453">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2453">4</span></span>

<span data-ttu-id="cc80c-2454">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2454">5</span></span>

<span data-ttu-id="cc80c-2455">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2455">6</span></span>

<span data-ttu-id="cc80c-2456">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2456">7</span></span>

<span data-ttu-id="cc80c-2457">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2457">8</span></span>

<span data-ttu-id="cc80c-2458">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2458">9</span></span>

<span data-ttu-id="cc80c-2459">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2459">2</span></span><br/> <span data-ttu-id="cc80c-2460">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2460">0</span></span><br/>

<span data-ttu-id="cc80c-2461">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2461">1</span></span>

<span data-ttu-id="cc80c-2462">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2462">2</span></span>

<span data-ttu-id="cc80c-2463">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2463">3</span></span>

<span data-ttu-id="cc80c-2464">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2464">4</span></span>

<span data-ttu-id="cc80c-2465">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2465">5</span></span>

<span data-ttu-id="cc80c-2466">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2466">6</span></span>

<span data-ttu-id="cc80c-2467">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2467">7</span></span>

<span data-ttu-id="cc80c-2468">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2468">8</span></span>

<span data-ttu-id="cc80c-2469">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2469">9</span></span>

<span data-ttu-id="cc80c-2470">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2470">3</span></span><br/> <span data-ttu-id="cc80c-2471">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2471">0</span></span><br/>

<span data-ttu-id="cc80c-2472">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2472">1</span></span>

<span data-ttu-id="cc80c-2473">Anzahl</span><span class="sxs-lookup"><span data-stu-id="cc80c-2473">Count</span></span>

<span data-ttu-id="cc80c-2474">sortArray (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2474">sortArray (variable)</span></span>



 

<span data-ttu-id="cc80c-2475">**count:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente in sortArray angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2475">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="cc80c-2476">**sortArray:** Ein Array von CSort-Strukturen, das die Reihenfolge beschreibt, in der die Ergebnisse der Abfrage sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2476">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="cc80c-2477">Strukturen im Array MÜSSEN durch 0 bis 3 Auf padding bytes getrennt werden, damit jede Struktur eine 4-Byte-Ausrichtung vom Anfang einer Nachricht hat.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2477">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="cc80c-2478">Solche Auffüllungsbytes können beliebige Werte sein, und MÜSSEN beim Empfang ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2478">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="cc80c-2479">2.2.1.31 CTableColumn</span><span class="sxs-lookup"><span data-stu-id="cc80c-2479">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="cc80c-2480">Die CTableColumn-Struktur enthält eine Spalte einer CPMSetBindingsIn-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2480">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="cc80c-2481">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2481">0</span></span>

<span data-ttu-id="cc80c-2482">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2482">1</span></span>

<span data-ttu-id="cc80c-2483">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2483">2</span></span>

<span data-ttu-id="cc80c-2484">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2484">3</span></span>

<span data-ttu-id="cc80c-2485">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2485">4</span></span>

<span data-ttu-id="cc80c-2486">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2486">5</span></span>

<span data-ttu-id="cc80c-2487">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2487">6</span></span>

<span data-ttu-id="cc80c-2488">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2488">7</span></span>

<span data-ttu-id="cc80c-2489">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2489">8</span></span>

<span data-ttu-id="cc80c-2490">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2490">9</span></span>

<span data-ttu-id="cc80c-2491">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2491">1</span></span><br/> <span data-ttu-id="cc80c-2492">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2492">0</span></span><br/>

<span data-ttu-id="cc80c-2493">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2493">1</span></span>

<span data-ttu-id="cc80c-2494">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2494">2</span></span>

<span data-ttu-id="cc80c-2495">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2495">3</span></span>

<span data-ttu-id="cc80c-2496">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2496">4</span></span>

<span data-ttu-id="cc80c-2497">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2497">5</span></span>

<span data-ttu-id="cc80c-2498">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2498">6</span></span>

<span data-ttu-id="cc80c-2499">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2499">7</span></span>

<span data-ttu-id="cc80c-2500">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2500">8</span></span>

<span data-ttu-id="cc80c-2501">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2501">9</span></span>

<span data-ttu-id="cc80c-2502">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2502">2</span></span><br/> <span data-ttu-id="cc80c-2503">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2503">0</span></span><br/>

<span data-ttu-id="cc80c-2504">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2504">1</span></span>

<span data-ttu-id="cc80c-2505">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2505">2</span></span>

<span data-ttu-id="cc80c-2506">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2506">3</span></span>

<span data-ttu-id="cc80c-2507">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2507">4</span></span>

<span data-ttu-id="cc80c-2508">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2508">5</span></span>

<span data-ttu-id="cc80c-2509">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2509">6</span></span>

<span data-ttu-id="cc80c-2510">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2510">7</span></span>

<span data-ttu-id="cc80c-2511">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2511">8</span></span>

<span data-ttu-id="cc80c-2512">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2512">9</span></span>

<span data-ttu-id="cc80c-2513">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2513">3</span></span><br/> <span data-ttu-id="cc80c-2514">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2514">0</span></span><br/>

<span data-ttu-id="cc80c-2515">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2515">1</span></span>

<span data-ttu-id="cc80c-2516">PropSpec</span><span class="sxs-lookup"><span data-stu-id="cc80c-2516">PropSpec</span></span>

<span data-ttu-id="cc80c-2517">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2517">...(variable)</span></span>

<span data-ttu-id="cc80c-2518">vType</span><span class="sxs-lookup"><span data-stu-id="cc80c-2518">vType</span></span>

<span data-ttu-id="cc80c-2519">ValueUsed</span><span class="sxs-lookup"><span data-stu-id="cc80c-2519">ValueUsed</span></span>

<span data-ttu-id="cc80c-2520">\_padding1 (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2520">\_padding1 (optional)</span></span>

<span data-ttu-id="cc80c-2521">ValueOffset (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2521">ValueOffset (optional)</span></span>

<span data-ttu-id="cc80c-2522">ValueSize (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2522">ValueSize (optional)</span></span>

<span data-ttu-id="cc80c-2523">StatusUsed</span><span class="sxs-lookup"><span data-stu-id="cc80c-2523">StatusUsed</span></span>

<span data-ttu-id="cc80c-2524">\_padding2 (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2524">\_padding2 (optional)</span></span>

<span data-ttu-id="cc80c-2525">StatusOffset (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2525">StatusOffset (optional)</span></span>

<span data-ttu-id="cc80c-2526">LengthUsed</span><span class="sxs-lookup"><span data-stu-id="cc80c-2526">LengthUsed</span></span>

<span data-ttu-id="cc80c-2527">\_Padding3 (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2527">\_padding3 (optional)</span></span>

<span data-ttu-id="cc80c-2528">LengthOffset (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2528">LengthOffset (optional)</span></span>



 

<span data-ttu-id="cc80c-2529">**PropSpec:** Eine CFullPropSpec-Struktur gemäß Abschnitt 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2529">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="cc80c-2530">**vType:** Gibt den Typ des in der Spalte enthaltenen Datenwerts an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2530">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="cc80c-2531">Die Liste der Werte für dieses Feld finden Sie im Feld vType in Abschnitt 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2531">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="cc80c-2532">**ValueUsed:** Ein 1-Byte-Feld, das auf 0x01 oder 0x00 festgelegt werden MUSS.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2532">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="cc80c-2533">Wenn auf 0x01 festgelegt ist, wird die Spalte innerhalb der Zeile fester Größe übertragen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2533">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="cc80c-2534">Wenn auf 0x00 festgelegt ist, wird der Wert der Spalte im Abschnitt variabler Länge am Ende des Puffers übertragen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2534">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="cc80c-2535">**\_ padding1:** Ein 1-Byte-Feld, das vor ValueOffset eingefügt werden muss, wenn ValueOffset ohne dieses Feld nicht an einem gleichmäßigen Offset vom Anfang der Nachricht beginnen würde.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2535">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="cc80c-2536">Der Wert dieses Byte ist beliebig und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2536">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="cc80c-2537">Wenn ValueUsed auf 0x00 ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2537">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cc80c-2538">**ValueOffset:** Eine 2-Byte-Ganzzahl ohne Vorzeichen, die den Offset des Spaltenwerts in der Zeile angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2538">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="cc80c-2539">Wenn ValueUsed auf 0x00 ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2539">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cc80c-2540">**ValueSize:** Eine 2-Byte-Ganzzahl ohne Vorzeichen, die die Größe des Spaltenwerts in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2540">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="cc80c-2541">Wenn ValueUsed auf 0x00 ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2541">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cc80c-2542">**StatusUsed:** Ein Ein-Byte-Feld, das auf 0x01 oder 0x00.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2542">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="cc80c-2543">Wenn auf 0x01 festgelegt ist, wird der Status der Spalte innerhalb der Zeile übertragen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2543">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="cc80c-2544">Wenn 0x00, wird der Status der Spalte nicht innerhalb der Zeile übertragen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2544">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="cc80c-2545">**\_ padding2:** Ein Ein-Byte-Feld, das vor StatusOffset eingefügt werden muss, wenn ohne das Feld StatusOffset nicht an einem gleichmäßigen Offset vom Anfang der Nachricht beginnen würde.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2545">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="cc80c-2546">Der Wert dieses Byte ist beliebig und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2546">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="cc80c-2547">Wenn StatusUsed auf 0x00 ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2547">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cc80c-2548">**StatusOffset:** Eine 2-Byte-Ganzzahl ohne Vorzeichen, die den Offset des Spaltenstatus in der Zeile angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2548">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="cc80c-2549">Wenn StatusUsed auf 0x00 ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2549">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cc80c-2550">**LengthUsed:** Ein Ein-Byte-Feld, das auf 0x01 oder 0x00.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2550">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="cc80c-2551">Wenn auf 0x01 festgelegt ist, wird die Länge der Spalte innerhalb der Zeile übertragen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2551">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="cc80c-2552">Wenn 0x00, DARF die Länge der Spalte NICHT innerhalb der Zeile übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2552">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="cc80c-2553">**\_ padding3:** Ein 1-Byte-Feld, das vor LengthOffset eingefügt werden MUSS, wenn LengthOffset ohne dieses Feld nicht mit einem geraden Offset vom Anfang einer Nachricht beginnen würde.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2553">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="cc80c-2554">Der Wert dieses Byte ist willkürlich und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2554">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="cc80c-2555">Wenn LengthUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2555">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cc80c-2556">**LengthOffset:** Eine 2-Byte-Ganzzahl ohne Vorzeichen, die den Offset der Spaltenlänge in der Zeile angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2556">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="cc80c-2557">Wenn LengthUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2557">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="cc80c-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="cc80c-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="cc80c-2559">Die SERIALIZEDPROPERTYVALUE-Struktur enthält einen serialisierten Wert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2559">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="cc80c-2560">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2560">0</span></span>

<span data-ttu-id="cc80c-2561">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2561">1</span></span>

<span data-ttu-id="cc80c-2562">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2562">2</span></span>

<span data-ttu-id="cc80c-2563">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2563">3</span></span>

<span data-ttu-id="cc80c-2564">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2564">4</span></span>

<span data-ttu-id="cc80c-2565">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2565">5</span></span>

<span data-ttu-id="cc80c-2566">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2566">6</span></span>

<span data-ttu-id="cc80c-2567">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2567">7</span></span>

<span data-ttu-id="cc80c-2568">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2568">8</span></span>

<span data-ttu-id="cc80c-2569">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2569">9</span></span>

<span data-ttu-id="cc80c-2570">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2570">1</span></span><br/> <span data-ttu-id="cc80c-2571">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2571">0</span></span><br/>

<span data-ttu-id="cc80c-2572">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2572">1</span></span>

<span data-ttu-id="cc80c-2573">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2573">2</span></span>

<span data-ttu-id="cc80c-2574">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2574">3</span></span>

<span data-ttu-id="cc80c-2575">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2575">4</span></span>

<span data-ttu-id="cc80c-2576">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2576">5</span></span>

<span data-ttu-id="cc80c-2577">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2577">6</span></span>

<span data-ttu-id="cc80c-2578">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2578">7</span></span>

<span data-ttu-id="cc80c-2579">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2579">8</span></span>

<span data-ttu-id="cc80c-2580">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2580">9</span></span>

<span data-ttu-id="cc80c-2581">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2581">2</span></span><br/> <span data-ttu-id="cc80c-2582">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2582">0</span></span><br/>

<span data-ttu-id="cc80c-2583">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2583">1</span></span>

<span data-ttu-id="cc80c-2584">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2584">2</span></span>

<span data-ttu-id="cc80c-2585">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2585">3</span></span>

<span data-ttu-id="cc80c-2586">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2586">4</span></span>

<span data-ttu-id="cc80c-2587">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2587">5</span></span>

<span data-ttu-id="cc80c-2588">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2588">6</span></span>

<span data-ttu-id="cc80c-2589">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2589">7</span></span>

<span data-ttu-id="cc80c-2590">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2590">8</span></span>

<span data-ttu-id="cc80c-2591">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2591">9</span></span>

<span data-ttu-id="cc80c-2592">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2592">3</span></span><br/> <span data-ttu-id="cc80c-2593">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2593">0</span></span><br/>

<span data-ttu-id="cc80c-2594">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2594">1</span></span>

<span data-ttu-id="cc80c-2595">dwType</span><span class="sxs-lookup"><span data-stu-id="cc80c-2595">dwType</span></span>

<span data-ttu-id="cc80c-2596">rgb (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2596">rgb (variable)</span></span>



 

<span data-ttu-id="cc80c-2597">**dwType:** Einer der in Abschnitt 2.2.1.1 definierten Variantentypen, der mit Variant-Typmodifizierern kombiniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2597">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="cc80c-2598">Für alle Variantentypen, mit Ausnahme der mit VT ARRAY kombinierten \_ Typen, weist SERIALIZEDPROPERTYVALUE das gleiche Layout wie CBaseStorageVariant auf, wie in Abschnitt 2.2.1.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2598">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="cc80c-2599">Wenn der Variant-Typ mit dem VT \_ ARRAY-Typmodifizierer kombiniert wird, wird SAFEARRAY2 gemäß Abschnitt 2.2.1.2.1.1 anstelle von SAFEARRAY im vValue-Feld von CBaseStorageVariant verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2599">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="cc80c-2600">**rgb:** Serialisierter Wert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2600">**rgb**: Serialized value.</span></span> <span data-ttu-id="cc80c-2601">Weitere Informationen finden Sie unter Serialisierung für vValue in 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2601">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="cc80c-2602">2.2.2 Nachrichtenheader</span><span class="sxs-lookup"><span data-stu-id="cc80c-2602">2.2.2 Message Headers</span></span>

<span data-ttu-id="cc80c-2603">Alle Content Indexing Service Protocol-Nachrichten verfügen über einen 16-Byte-Header.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2603">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="cc80c-2604">Unten sehen Sie ein Diagramm, das das Nachrichtenheaderformat des Content Indexing Service Protocol zeigt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2604">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="cc80c-2605">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2605">0</span></span>

<span data-ttu-id="cc80c-2606">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2606">1</span></span>

<span data-ttu-id="cc80c-2607">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2607">2</span></span>

<span data-ttu-id="cc80c-2608">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2608">3</span></span>

<span data-ttu-id="cc80c-2609">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2609">4</span></span>

<span data-ttu-id="cc80c-2610">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2610">5</span></span>

<span data-ttu-id="cc80c-2611">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2611">6</span></span>

<span data-ttu-id="cc80c-2612">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2612">7</span></span>

<span data-ttu-id="cc80c-2613">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2613">8</span></span>

<span data-ttu-id="cc80c-2614">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2614">9</span></span>

<span data-ttu-id="cc80c-2615">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2615">1</span></span><br/> <span data-ttu-id="cc80c-2616">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2616">0</span></span><br/>

<span data-ttu-id="cc80c-2617">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2617">1</span></span>

<span data-ttu-id="cc80c-2618">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2618">2</span></span>

<span data-ttu-id="cc80c-2619">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2619">3</span></span>

<span data-ttu-id="cc80c-2620">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2620">4</span></span>

<span data-ttu-id="cc80c-2621">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2621">5</span></span>

<span data-ttu-id="cc80c-2622">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2622">6</span></span>

<span data-ttu-id="cc80c-2623">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2623">7</span></span>

<span data-ttu-id="cc80c-2624">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2624">8</span></span>

<span data-ttu-id="cc80c-2625">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2625">9</span></span>

<span data-ttu-id="cc80c-2626">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2626">2</span></span><br/> <span data-ttu-id="cc80c-2627">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2627">0</span></span><br/>

<span data-ttu-id="cc80c-2628">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2628">1</span></span>

<span data-ttu-id="cc80c-2629">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2629">2</span></span>

<span data-ttu-id="cc80c-2630">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2630">3</span></span>

<span data-ttu-id="cc80c-2631">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2631">4</span></span>

<span data-ttu-id="cc80c-2632">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2632">5</span></span>

<span data-ttu-id="cc80c-2633">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2633">6</span></span>

<span data-ttu-id="cc80c-2634">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2634">7</span></span>

<span data-ttu-id="cc80c-2635">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2635">8</span></span>

<span data-ttu-id="cc80c-2636">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2636">9</span></span>

<span data-ttu-id="cc80c-2637">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2637">3</span></span><br/> <span data-ttu-id="cc80c-2638">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2638">0</span></span><br/>

<span data-ttu-id="cc80c-2639">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2639">1</span></span>

<span data-ttu-id="cc80c-2640">\_Msg</span><span class="sxs-lookup"><span data-stu-id="cc80c-2640">\_msg</span></span>

<span data-ttu-id="cc80c-2641">\_Status</span><span class="sxs-lookup"><span data-stu-id="cc80c-2641">\_status</span></span>

<span data-ttu-id="cc80c-2642">\_ulChecksum</span><span class="sxs-lookup"><span data-stu-id="cc80c-2642">\_ulChecksum</span></span>

<span data-ttu-id="cc80c-2643">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2643">\_ulReserved2</span></span>



 

<span data-ttu-id="cc80c-2644">\_**msg:** Eine 32-Bit-Ganzzahl, die den Typ der Nachricht nach dem Header angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2644">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="cc80c-2645">In der folgenden Tabelle sind die Meldungen des Content Indexing Service-Protokolls und die für jede Nachricht angegebenen ganzzahligen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2645">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="cc80c-2646">Wie in der Tabelle gezeigt, identifizieren einige Werte zwei Nachrichten in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2646">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="cc80c-2647">In diesen Fällen kann die Nachricht, die auf den Header folgt, durch die Richtung des Nachrichtenflusses identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2647">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="cc80c-2648">Wenn die Richtung Client zu Server ist, wird die Meldung mit "In" angegeben, die an den Nachrichtennamen angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2648">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="cc80c-2649">Wenn die Richtung Server zu Client ist, wird die Nachricht mit "Out" angegeben, die an den Nachrichtennamen angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2649">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="cc80c-2650">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-2650">Value</span></span>      | <span data-ttu-id="cc80c-2651">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-2651">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="cc80c-2652">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2652">0x000000C8</span></span> | <span data-ttu-id="cc80c-2653">CPMConnectIn oder CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-2653">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="cc80c-2654">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2654">0x000000C9</span></span> | <span data-ttu-id="cc80c-2655">CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="cc80c-2655">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="cc80c-2656">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="cc80c-2656">0x000000CA</span></span> | <span data-ttu-id="cc80c-2657">CPMCreateQueryIn oder CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-2657">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="cc80c-2658">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="cc80c-2658">0x000000CB</span></span> | <span data-ttu-id="cc80c-2659">CPMFreeCursorIn oder CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-2659">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="cc80c-2660">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="cc80c-2660">0x000000CC</span></span> | <span data-ttu-id="cc80c-2661">CPMGetRowsIn oder CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-2661">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="cc80c-2662">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="cc80c-2662">0x000000CD</span></span> | <span data-ttu-id="cc80c-2663">CPMRatioFinishedIn oder CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-2663">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="cc80c-2664">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="cc80c-2664">0x000000CE</span></span> | <span data-ttu-id="cc80c-2665">CPMCompareBmkIn oder CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-2665">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="cc80c-2666">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="cc80c-2666">0x000000CF</span></span> | <span data-ttu-id="cc80c-2667">CPMGetApproximatePositionIn oder CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-2667">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="cc80c-2668">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2668">0x000000D0</span></span> | <span data-ttu-id="cc80c-2669">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-2669">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="cc80c-2670">0x000000D1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2670">0x000000D1</span></span> | <span data-ttu-id="cc80c-2671">CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="cc80c-2671">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="cc80c-2672">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2672">0x000000D2</span></span> | <span data-ttu-id="cc80c-2673">CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-2673">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="cc80c-2674">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2674">0x000000D7</span></span> | <span data-ttu-id="cc80c-2675">CPMGetQueryStatusIn oder CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-2675">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="cc80c-2676">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2676">0x000000D9</span></span> | <span data-ttu-id="cc80c-2677">CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-2677">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="cc80c-2678">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2678">0x000000E1</span></span> | <span data-ttu-id="cc80c-2679">CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-2679">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="cc80c-2680">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2680">0x000000E4</span></span> | <span data-ttu-id="cc80c-2681">CPMFetchValueIn oder CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-2681">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="cc80c-2682">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2682">0x000000E6</span></span> | <span data-ttu-id="cc80c-2683">CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-2683">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="cc80c-2684">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2684">0x000000E7</span></span> | <span data-ttu-id="cc80c-2685">CPMGetQueryStatusExIn oder PMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-2685">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="cc80c-2686">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2686">0x000000E8</span></span> | <span data-ttu-id="cc80c-2687">CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-2687">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="cc80c-2688">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2688">0x000000E9</span></span> | <span data-ttu-id="cc80c-2689">CPMStopAsynchIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-2689">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="cc80c-2690">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="cc80c-2690">0x000000EC</span></span> | <span data-ttu-id="cc80c-2691">CPMSetCatStateIn oder CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-2691">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="cc80c-2692">\_**status:** Ein HRESULT \[ MS-SYS, \] das den Status des angeforderten Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2692">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="cc80c-2693">*Windows-Verhalten: Der Client legt das \_ Statusfeld immer auf 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="cc80c-2693">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="cc80c-2694">**\_ ulChecksum:** UlChecksum MUSS wie in Abschnitt \_ 3.2.4 für die folgenden Meldungen angegeben berechnet werden:</span><span class="sxs-lookup"><span data-stu-id="cc80c-2694">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="cc80c-2695">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-2695">CPMConnectIn</span></span>
-   <span data-ttu-id="cc80c-2696">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-2696">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="cc80c-2697">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-2697">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="cc80c-2698">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-2698">CPMGetRowsIn</span></span>
-   <span data-ttu-id="cc80c-2699">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-2699">CPMFetchValueIn</span></span>

<span data-ttu-id="cc80c-2700">Für alle anderen Nachrichten MUSS \_ ulChecksum auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2700">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="cc80c-2701">Ein Client MUSS das \_ UlChecksum-Feld ignorieren.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2701">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="cc80c-2702">**\_ ulReserved2:** MUSS auf 0 festgelegt und vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2702">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="cc80c-2703">2.2.3 Nachrichten</span><span class="sxs-lookup"><span data-stu-id="cc80c-2703">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="cc80c-2704">2.2.3.1 CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-2704">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="cc80c-2705">Die CPMCiStateInOut-Nachricht enthält Informationen zum Status des Indizierungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2705">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="cc80c-2706">Das Format der CPMCiStateInOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-2706">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="cc80c-2707">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2707">0</span></span>

<span data-ttu-id="cc80c-2708">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2708">1</span></span>

<span data-ttu-id="cc80c-2709">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2709">2</span></span>

<span data-ttu-id="cc80c-2710">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2710">3</span></span>

<span data-ttu-id="cc80c-2711">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2711">4</span></span>

<span data-ttu-id="cc80c-2712">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2712">5</span></span>

<span data-ttu-id="cc80c-2713">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2713">6</span></span>

<span data-ttu-id="cc80c-2714">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2714">7</span></span>

<span data-ttu-id="cc80c-2715">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2715">8</span></span>

<span data-ttu-id="cc80c-2716">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2716">9</span></span>

<span data-ttu-id="cc80c-2717">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2717">1</span></span><br/> <span data-ttu-id="cc80c-2718">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2718">0</span></span><br/>

<span data-ttu-id="cc80c-2719">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2719">1</span></span>

<span data-ttu-id="cc80c-2720">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2720">2</span></span>

<span data-ttu-id="cc80c-2721">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2721">3</span></span>

<span data-ttu-id="cc80c-2722">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2722">4</span></span>

<span data-ttu-id="cc80c-2723">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2723">5</span></span>

<span data-ttu-id="cc80c-2724">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2724">6</span></span>

<span data-ttu-id="cc80c-2725">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2725">7</span></span>

<span data-ttu-id="cc80c-2726">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2726">8</span></span>

<span data-ttu-id="cc80c-2727">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2727">9</span></span>

<span data-ttu-id="cc80c-2728">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2728">2</span></span><br/> <span data-ttu-id="cc80c-2729">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2729">0</span></span><br/>

<span data-ttu-id="cc80c-2730">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2730">1</span></span>

<span data-ttu-id="cc80c-2731">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2731">2</span></span>

<span data-ttu-id="cc80c-2732">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2732">3</span></span>

<span data-ttu-id="cc80c-2733">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2733">4</span></span>

<span data-ttu-id="cc80c-2734">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2734">5</span></span>

<span data-ttu-id="cc80c-2735">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2735">6</span></span>

<span data-ttu-id="cc80c-2736">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2736">7</span></span>

<span data-ttu-id="cc80c-2737">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2737">8</span></span>

<span data-ttu-id="cc80c-2738">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2738">9</span></span>

<span data-ttu-id="cc80c-2739">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2739">3</span></span><br/> <span data-ttu-id="cc80c-2740">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2740">0</span></span><br/>

<span data-ttu-id="cc80c-2741">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2741">1</span></span>

<span data-ttu-id="cc80c-2742">cbStruct</span><span class="sxs-lookup"><span data-stu-id="cc80c-2742">cbStruct</span></span>

<span data-ttu-id="cc80c-2743">cWordList</span><span class="sxs-lookup"><span data-stu-id="cc80c-2743">cWordList</span></span>

<span data-ttu-id="cc80c-2744">cPersistentIndex</span><span class="sxs-lookup"><span data-stu-id="cc80c-2744">cPersistentIndex</span></span>

<span data-ttu-id="cc80c-2745">cQueries</span><span class="sxs-lookup"><span data-stu-id="cc80c-2745">cQueries</span></span>

<span data-ttu-id="cc80c-2746">cDocuments</span><span class="sxs-lookup"><span data-stu-id="cc80c-2746">cDocuments</span></span>

<span data-ttu-id="cc80c-2747">cFreshTest</span><span class="sxs-lookup"><span data-stu-id="cc80c-2747">cFreshTest</span></span>

<span data-ttu-id="cc80c-2748">dwMergeProgress</span><span class="sxs-lookup"><span data-stu-id="cc80c-2748">dwMergeProgress</span></span>

<span data-ttu-id="cc80c-2749">Estate</span><span class="sxs-lookup"><span data-stu-id="cc80c-2749">eState</span></span>

<span data-ttu-id="cc80c-2750">cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="cc80c-2750">cFilteredDocuments</span></span>

<span data-ttu-id="cc80c-2751">cTotalDocuments</span><span class="sxs-lookup"><span data-stu-id="cc80c-2751">cTotalDocuments</span></span>

<span data-ttu-id="cc80c-2752">cPendingScans</span><span class="sxs-lookup"><span data-stu-id="cc80c-2752">cPendingScans</span></span>

<span data-ttu-id="cc80c-2753">dwIndexSize</span><span class="sxs-lookup"><span data-stu-id="cc80c-2753">dwIndexSize</span></span>

<span data-ttu-id="cc80c-2754">cUniqueKeys</span><span class="sxs-lookup"><span data-stu-id="cc80c-2754">cUniqueKeys</span></span>

<span data-ttu-id="cc80c-2755">cSecQDocuments</span><span class="sxs-lookup"><span data-stu-id="cc80c-2755">cSecQDocuments</span></span>

<span data-ttu-id="cc80c-2756">dwPropCacheSize</span><span class="sxs-lookup"><span data-stu-id="cc80c-2756">dwPropCacheSize</span></span>



 

<span data-ttu-id="cc80c-2757">**cbStruct:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2757">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cc80c-2758">Die Größe dieser Nachricht in Bytes (mit Ausnahme des allgemeinen Headers).</span><span class="sxs-lookup"><span data-stu-id="cc80c-2758">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="cc80c-2759">MUSS auf 0x0000003C festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2759">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="cc80c-2760">**cWordList:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der anfänglichen Indizes angibt, die für kürzlich indizierte Dokumente erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2760">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="cc80c-2761">**cPersistentIndex:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der persistenten Indizes angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2761">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="cc80c-2762">**cQueries:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die eine Reihe aktiv ausgeführter Abfragen angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2762">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="cc80c-2763">**cDocuments:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Dokumente angibt, die auf die Indizierung warten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2763">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="cc80c-2764">**cFreshTest:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl eindeutiger Dokumente mit Informationen in Indizes angibt, die nicht vollständig für die Leistung optimiert sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2764">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="cc80c-2765">**dwMergeProgress:** 32-Bit-Ganzzahl ohne Vorzeichen, die den Vervollständigungsprozentsatz der aktuellen vollständigen Optimierung von Indizes angibt, wenn die Optimierung gerade läuft.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2765">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="cc80c-2766">MUSS kleiner oder gleich 100 sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2766">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="cc80c-2767">**eState:** Status der Inhaltsindizierung, wie er von einer oder mehr der CI STATE-Konstanten angegeben wird, die \_ in der folgenden Tabelle definiert \_ \* sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2767">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="cc80c-2768">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-2768">Value</span></span>                                         | <span data-ttu-id="cc80c-2769">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-2769">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-2770">CI \_ STATE SHADOW MERGE \_ \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-2770">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="cc80c-2771">Der Indizierungsdienst optimiert einige der Indizes, um die Speicherauslastung zu reduzieren und die Abfrageleistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2771">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="cc80c-2772">CI \_ STATE \_ MASTER \_ MERGE-0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-2772">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="cc80c-2773">Der Indizierungsdienst wird für alle Indizes vollständig optimiert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2773">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cc80c-2774">CI \_ STATE CONTENT SCAN REQUIRED \_ \_ \_ 0X00000004</span><span class="sxs-lookup"><span data-stu-id="cc80c-2774">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="cc80c-2775">Einige Dokumente im Index wurden geändert, und der Indizierungsdienst muss bestimmen, welche hinzugefügt, geändert oder gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2775">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="cc80c-2776">CI \_ STATE \_ ANNEALING \_ MERGE 0X00000008</span><span class="sxs-lookup"><span data-stu-id="cc80c-2776">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="cc80c-2777">Der Indizierungsdienst optimiert Indizes, um die Speicherauslastung zu reduzieren und die Abfrageleistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2777">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="cc80c-2778">Dieser Prozess ist umfassender als der durch den CI STATE SHADOW MERGE-Wert identifizierte Prozess, aber er ist nicht so umfassend wie durch den \_ \_ CI STATE MASTER \_ \_ \_ \_ MERGE-Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2778">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="cc80c-2779">Solche Optimierungen sind implementierungsspezifisch, da sie davon abhängen, wie Daten intern gespeichert werden. Die Optimierungen wirken sich nur auf die Antwortzeit auf das Protokoll aus.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2779">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="cc80c-2780">CI \_ STATE \_ SCANNING-0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc80c-2780">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="cc80c-2781">Der Indizierungsdienst untersucht ein Verzeichnis oder eine Gruppe von Verzeichnissen, um festzustellen, ob Dateien seit dem letzten Indizieren des Verzeichnisses hinzugefügt, gelöscht oder aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2781">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cc80c-2782">CI \_ STATE \_ RECOVERING 0x00000020</span><span class="sxs-lookup"><span data-stu-id="cc80c-2782">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="cc80c-2783">Der Dienst beginnt mit dem letzten gespeicherten Zustand und wird gerade wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2783">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cc80c-2784">CI \_ STATE LOW MEMORY \_ \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="cc80c-2784">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="cc80c-2785">Der größte Teil des virtuellen Arbeitsspeichers des Servers wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2785">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="cc80c-2786">CI \_ STATE HIGH IO \_ \_ 0x00000100</span><span class="sxs-lookup"><span data-stu-id="cc80c-2786">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="cc80c-2787">Die E/A-Aktivität (Input/Output) auf dem Server ist relativ hoch.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2787">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="cc80c-2788">CI \_ STATE MASTER MERGE \_ \_ \_ PAUSED 0x00000200</span><span class="sxs-lookup"><span data-stu-id="cc80c-2788">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="cc80c-2789">Der Prozess der vollständigen Optimierung für alle Indizes, die gerade ausgeführt wurden, wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2789">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="cc80c-2790">Dies dient nur zu Informationszwecken und wirkt sich nicht auf CISP aus.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cc80c-2791">CI \_ STATE READ ONLY \_ \_ 0x00000400</span><span class="sxs-lookup"><span data-stu-id="cc80c-2791">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="cc80c-2792">Der Teil des Indizierungsdiensts, der neue zu indizierende Dokumente aufnimmt, wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2792">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="cc80c-2793">Dies dient nur zu Informationszwecken und wirkt sich nicht auf CISP aus.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="cc80c-2794">CI \_ STATE BATTERY POWER \_ \_ 0x00000800</span><span class="sxs-lookup"><span data-stu-id="cc80c-2794">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="cc80c-2795">Der Teil des Indizierungsdiensts, der neue zu indizierende Dokumente aufnimmt, wurde angehalten, um die Akkulebensdauer zu sparen, antwortet aber weiterhin auf die Abfragen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2795">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="cc80c-2796">Dies dient nur zu Informationszwecken und wirkt sich nicht auf CISP aus.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cc80c-2797">CI \_ STATE USER ACTIVE \_ \_ 0x00001000</span><span class="sxs-lookup"><span data-stu-id="cc80c-2797">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="cc80c-2798">Der Teil des Indizierungsdiensts, der neue zu indizierende Dokumente aufnimmt, wurde aufgrund einer hohen Aktivität durch den Benutzer (Tastatur oder Maus) angehalten, antwortet aber weiterhin auf die Abfragen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2798">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="cc80c-2799">Dies dient nur zu Informationszwecken und wirkt sich nicht auf CISP aus.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2799">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="cc80c-2800">CI \_ STATE \_ STARTING 0x00002000</span><span class="sxs-lookup"><span data-stu-id="cc80c-2800">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="cc80c-2801">Der Dienst wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2801">The service is starting.</span></span> <span data-ttu-id="cc80c-2802">Abfragen können ausgeführt werden, überprüfungen und Benachrichtigungen wurden jedoch noch nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2802">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="cc80c-2803">Dies dient nur zu Informationszwecken und wirkt sich nicht auf CISP aus.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2803">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cc80c-2804">CI \_ STATE \_ READING \_ USNS 0x00004000</span><span class="sxs-lookup"><span data-stu-id="cc80c-2804">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="cc80c-2805">Der Dienst hat das vom Dateisystem gespeicherte Protokoll nicht gelesen, um Änderungen an Dateien oder Verzeichnissen auf einem Volume nachderherzustellen, sodass der Index möglicherweise nicht auf dem neuesten Stand ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2805">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="cc80c-2806">**cFilteredDocuments:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der seit Beginn der Inhaltsindizierung indizierten Dokumente angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2806">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="cc80c-2807">**cTotalDocuments:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Dokumente im System angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2807">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="cc80c-2808">**cPendingScans:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl ausstehender Indizierungsvorgänge auf hoher Ebene angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2808">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="cc80c-2809">Die Bedeutung dieses Werts ist anbieterspezifisch, aber es wird erwartet, dass größere Zahlen darauf hindeuten, dass mehr Indizierung verbleibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2809">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="cc80c-2810">*Windows-Verhalten:* Dieser Wert ist in der Regel 0 (null), außer unmittelbar nach dem Start der Indizierung oder nach einem Überlauf einer Benachrichtigungswarteschlange.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2810">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="cc80c-2811">**dwIndexSize:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des Indexes (mit Ausnahme des Eigenschaftencaches) in Megabyte angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2811">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="cc80c-2812">**cUniqueKeys:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die ungefähre Anzahl eindeutiger Schlüssel im Katalog angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2812">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="cc80c-2813">**cSecQDocuments:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dokumente angibt, die der Indizierungsdienst aufgrund eines Fehlers während des ersten Indizierungsversuchs erneut versucht.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2813">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="cc80c-2814">**dwPropCacheSize:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des Eigenschaftencaches in Megabyte angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2814">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="cc80c-2815">2.2.3.2 CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-2815">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="cc80c-2816">Die CPMSetCatStateIn-Meldung legt den Status eines Katalogs fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2816">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="cc80c-2817">Das Format der CPMSetCatStateIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-2817">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="cc80c-2818">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2818">0</span></span>

<span data-ttu-id="cc80c-2819">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2819">1</span></span>

<span data-ttu-id="cc80c-2820">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2820">2</span></span>

<span data-ttu-id="cc80c-2821">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2821">3</span></span>

<span data-ttu-id="cc80c-2822">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2822">4</span></span>

<span data-ttu-id="cc80c-2823">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2823">5</span></span>

<span data-ttu-id="cc80c-2824">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2824">6</span></span>

<span data-ttu-id="cc80c-2825">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2825">7</span></span>

<span data-ttu-id="cc80c-2826">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2826">8</span></span>

<span data-ttu-id="cc80c-2827">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2827">9</span></span>

<span data-ttu-id="cc80c-2828">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2828">1</span></span><br/> <span data-ttu-id="cc80c-2829">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2829">0</span></span><br/>

<span data-ttu-id="cc80c-2830">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2830">1</span></span>

<span data-ttu-id="cc80c-2831">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2831">2</span></span>

<span data-ttu-id="cc80c-2832">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2832">3</span></span>

<span data-ttu-id="cc80c-2833">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2833">4</span></span>

<span data-ttu-id="cc80c-2834">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2834">5</span></span>

<span data-ttu-id="cc80c-2835">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2835">6</span></span>

<span data-ttu-id="cc80c-2836">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2836">7</span></span>

<span data-ttu-id="cc80c-2837">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2837">8</span></span>

<span data-ttu-id="cc80c-2838">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2838">9</span></span>

<span data-ttu-id="cc80c-2839">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2839">2</span></span><br/> <span data-ttu-id="cc80c-2840">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2840">0</span></span><br/>

<span data-ttu-id="cc80c-2841">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2841">1</span></span>

<span data-ttu-id="cc80c-2842">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2842">2</span></span>

<span data-ttu-id="cc80c-2843">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2843">3</span></span>

<span data-ttu-id="cc80c-2844">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2844">4</span></span>

<span data-ttu-id="cc80c-2845">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2845">5</span></span>

<span data-ttu-id="cc80c-2846">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2846">6</span></span>

<span data-ttu-id="cc80c-2847">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2847">7</span></span>

<span data-ttu-id="cc80c-2848">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2848">8</span></span>

<span data-ttu-id="cc80c-2849">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2849">9</span></span>

<span data-ttu-id="cc80c-2850">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2850">3</span></span><br/> <span data-ttu-id="cc80c-2851">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2851">0</span></span><br/>

<span data-ttu-id="cc80c-2852">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2852">1</span></span>

<span data-ttu-id="cc80c-2853">\_partID</span><span class="sxs-lookup"><span data-stu-id="cc80c-2853">\_partID</span></span>

<span data-ttu-id="cc80c-2854">\_dwNewState</span><span class="sxs-lookup"><span data-stu-id="cc80c-2854">\_dwNewState</span></span>

<span data-ttu-id="cc80c-2855">\_CatName (Variable, optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2855">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="cc80c-2856">**\_ partID:** MUSS auf "0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2856">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="cc80c-2857">**\_ dwNewState:** MUSS auf einen der folgenden Werte festgelegt werden, der den neuen Status des Katalogs angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2857">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="cc80c-2858">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-2858">Value</span></span>                         | <span data-ttu-id="cc80c-2859">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-2859">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-2860">CICAT \_ STOPPED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-2860">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="cc80c-2861">Der Katalog wird beendet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2861">The catalog is stopped.</span></span> <span data-ttu-id="cc80c-2862">Dieser Zustand bedeutet, dass keine neuen Dateien indiziert und keine Suchabfragen verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2862">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="cc80c-2863">CICAT \_ READONLY-0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-2863">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="cc80c-2864">Der Katalog ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2864">The catalog is read-only.</span></span> <span data-ttu-id="cc80c-2865">Es sollen keine neuen Dateien indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2865">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="cc80c-2866">CICAT \_ WRITABLE-0x00000004</span><span class="sxs-lookup"><span data-stu-id="cc80c-2866">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="cc80c-2867">Der Katalog kann geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2867">The catalog is writable.</span></span> <span data-ttu-id="cc80c-2868">Neue Dateien können indiziert werden, und Suchabfragen müssen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2868">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="cc80c-2869">CICAT \_ NO \_ QUERY 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cc80c-2869">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="cc80c-2870">Der Katalog ist nicht für Abfragen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2870">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="cc80c-2871">CICAT \_ GET \_ STATE 0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc80c-2871">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="cc80c-2872">Der Status des Katalogs soll nicht geändert, sondern nur abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2872">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="cc80c-2873">CICAT \_ ALL \_ OPENED 0x00000020</span><span class="sxs-lookup"><span data-stu-id="cc80c-2873">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="cc80c-2874">Eine Überprüfung, um festzustellen, ob alle Kataloge gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2874">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="cc80c-2875">Wenn ja, wird das \_ feld dwOldState, das in der CPMSetCatStateOut-Antwort an diese Nachricht gesendet wird, als ungleich 0 (null) gemeldet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2875">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="cc80c-2876">**\_ CatName:** Der Name des Katalogs, dessen Status geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2876">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="cc80c-2877">Der Name MUSS eine auf NULL endende Unicode-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2877">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="cc80c-2878">Dieses Feld MUSS weggelassen werden, wenn \_ dwNewState auf CICAT ALL OPENED festgelegt \_ \_ ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2878">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="cc80c-2879">2.2.3.3 CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-2879">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="cc80c-2880">Die CPMSetCatStateOut-Nachricht ist eine Antwort auf eine CPMSetCatStateIn-Nachricht mit dem alten Status des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2880">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="cc80c-2881">Das Format der CPMSetCatStateOut-Nachricht, die auf den Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-2881">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="cc80c-2882">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2882">0</span></span>

<span data-ttu-id="cc80c-2883">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2883">1</span></span>

<span data-ttu-id="cc80c-2884">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2884">2</span></span>

<span data-ttu-id="cc80c-2885">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2885">3</span></span>

<span data-ttu-id="cc80c-2886">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2886">4</span></span>

<span data-ttu-id="cc80c-2887">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2887">5</span></span>

<span data-ttu-id="cc80c-2888">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2888">6</span></span>

<span data-ttu-id="cc80c-2889">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2889">7</span></span>

<span data-ttu-id="cc80c-2890">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2890">8</span></span>

<span data-ttu-id="cc80c-2891">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2891">9</span></span>

<span data-ttu-id="cc80c-2892">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2892">1</span></span><br/> <span data-ttu-id="cc80c-2893">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2893">0</span></span><br/>

<span data-ttu-id="cc80c-2894">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2894">1</span></span>

<span data-ttu-id="cc80c-2895">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2895">2</span></span>

<span data-ttu-id="cc80c-2896">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2896">3</span></span>

<span data-ttu-id="cc80c-2897">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2897">4</span></span>

<span data-ttu-id="cc80c-2898">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2898">5</span></span>

<span data-ttu-id="cc80c-2899">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2899">6</span></span>

<span data-ttu-id="cc80c-2900">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2900">7</span></span>

<span data-ttu-id="cc80c-2901">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2901">8</span></span>

<span data-ttu-id="cc80c-2902">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2902">9</span></span>

<span data-ttu-id="cc80c-2903">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2903">2</span></span><br/> <span data-ttu-id="cc80c-2904">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2904">0</span></span><br/>

<span data-ttu-id="cc80c-2905">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2905">1</span></span>

<span data-ttu-id="cc80c-2906">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2906">2</span></span>

<span data-ttu-id="cc80c-2907">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2907">3</span></span>

<span data-ttu-id="cc80c-2908">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2908">4</span></span>

<span data-ttu-id="cc80c-2909">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2909">5</span></span>

<span data-ttu-id="cc80c-2910">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2910">6</span></span>

<span data-ttu-id="cc80c-2911">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2911">7</span></span>

<span data-ttu-id="cc80c-2912">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2912">8</span></span>

<span data-ttu-id="cc80c-2913">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2913">9</span></span>

<span data-ttu-id="cc80c-2914">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2914">3</span></span><br/> <span data-ttu-id="cc80c-2915">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2915">0</span></span><br/>

<span data-ttu-id="cc80c-2916">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2916">1</span></span>

<span data-ttu-id="cc80c-2917">\_dwOldState</span><span class="sxs-lookup"><span data-stu-id="cc80c-2917">\_dwOldState</span></span>



 

<span data-ttu-id="cc80c-2918">**\_ dwOldState:** Einer der folgenden Werte, der den alten Zustand des Katalogs angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2918">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="cc80c-2919">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-2919">Value</span></span>                       | <span data-ttu-id="cc80c-2920">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-2920">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="cc80c-2921">CICAT \_ STOPPED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-2921">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="cc80c-2922">Der Katalog wird beendet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2922">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="cc80c-2923">CICAT \_ READONLY 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-2923">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="cc80c-2924">Der Katalog ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2924">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="cc80c-2925">CICAT \_ WRITABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cc80c-2925">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="cc80c-2926">Der Katalog ist beschreibbar.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2926">The catalog is writable.</span></span>                   |
| <span data-ttu-id="cc80c-2927">CICAT \_ NO \_ QUERY 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cc80c-2927">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="cc80c-2928">Der Katalog ist nicht für Abfragen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2928">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="cc80c-2929">2.2.3.4 CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-2929">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="cc80c-2930">Die CPMUpdateDocumentsIn-Nachricht leitet den Server an, den angegebenen Pfad zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2930">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="cc80c-2931">Der Server antwortet mit dem Nachrichtenheader der CPMUpdateDocumentsOut-Nachricht, und die Ergebnisse der Anforderung sind im Statusfeld des \_ Nachrichtenheaders enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2931">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="cc80c-2932">Das Format der CPMUpdateDocumentsIn-Nachricht, die auf den Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-2932">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="cc80c-2933">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2933">0</span></span>

<span data-ttu-id="cc80c-2934">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2934">1</span></span>

<span data-ttu-id="cc80c-2935">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2935">2</span></span>

<span data-ttu-id="cc80c-2936">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2936">3</span></span>

<span data-ttu-id="cc80c-2937">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2937">4</span></span>

<span data-ttu-id="cc80c-2938">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2938">5</span></span>

<span data-ttu-id="cc80c-2939">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2939">6</span></span>

<span data-ttu-id="cc80c-2940">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2940">7</span></span>

<span data-ttu-id="cc80c-2941">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2941">8</span></span>

<span data-ttu-id="cc80c-2942">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2942">9</span></span>

<span data-ttu-id="cc80c-2943">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2943">1</span></span><br/> <span data-ttu-id="cc80c-2944">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2944">0</span></span><br/>

<span data-ttu-id="cc80c-2945">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2945">1</span></span>

<span data-ttu-id="cc80c-2946">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2946">2</span></span>

<span data-ttu-id="cc80c-2947">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2947">3</span></span>

<span data-ttu-id="cc80c-2948">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2948">4</span></span>

<span data-ttu-id="cc80c-2949">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2949">5</span></span>

<span data-ttu-id="cc80c-2950">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2950">6</span></span>

<span data-ttu-id="cc80c-2951">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2951">7</span></span>

<span data-ttu-id="cc80c-2952">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2952">8</span></span>

<span data-ttu-id="cc80c-2953">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2953">9</span></span>

<span data-ttu-id="cc80c-2954">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2954">2</span></span><br/> <span data-ttu-id="cc80c-2955">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2955">0</span></span><br/>

<span data-ttu-id="cc80c-2956">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2956">1</span></span>

<span data-ttu-id="cc80c-2957">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2957">2</span></span>

<span data-ttu-id="cc80c-2958">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2958">3</span></span>

<span data-ttu-id="cc80c-2959">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2959">4</span></span>

<span data-ttu-id="cc80c-2960">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-2960">5</span></span>

<span data-ttu-id="cc80c-2961">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-2961">6</span></span>

<span data-ttu-id="cc80c-2962">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-2962">7</span></span>

<span data-ttu-id="cc80c-2963">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-2963">8</span></span>

<span data-ttu-id="cc80c-2964">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-2964">9</span></span>

<span data-ttu-id="cc80c-2965">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2965">3</span></span><br/> <span data-ttu-id="cc80c-2966">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2966">0</span></span><br/>

<span data-ttu-id="cc80c-2967">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2967">1</span></span>

<span data-ttu-id="cc80c-2968">\_Flag (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2968">\_flag (optional)</span></span>

<span data-ttu-id="cc80c-2969">\_fRootPath (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2969">\_fRootPath (optional)</span></span>

<span data-ttu-id="cc80c-2970">RootPath (Variable, optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-2970">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="cc80c-2971">**\_ flag:** Der Typ des auszuführenden Updates.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2971">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="cc80c-2972">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2972">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="cc80c-2973">Dieses Feld MUSS auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="cc80c-2973">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="cc80c-2974">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-2974">Value</span></span>                  | <span data-ttu-id="cc80c-2975">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-2975">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="cc80c-2976">UPD \_ INCREM 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-2976">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="cc80c-2977">Ein inkrementelles Update muss ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2977">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="cc80c-2978">UPD \_ FULL 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-2978">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="cc80c-2979">Ein vollständiges Update muss ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2979">A full update is to be performed.</span></span>         |
| <span data-ttu-id="cc80c-2980">UPD \_ INIT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-2980">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="cc80c-2981">Eine neue Initialisierung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2981">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="cc80c-2982">**\_ fRootPath:** Ein boolescher Wert, der angibt, ob das RootPath-Feld einen Pfad angibt, unter dem das Update ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2982">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="cc80c-2983">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2983">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="cc80c-2984">Dieses Feld MUSS auf 0x00000001 oder 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2984">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="cc80c-2985">Wenn auf 0x00000001 festgelegt ist, ist ein Pfad, auf dem das Update ausgeführt werden soll, in RootPath enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2985">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="cc80c-2986">Wenn 0x00000000 festgelegt ist, muss das Update für alle indizierten Pfade ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2986">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="cc80c-2987">**RootPath:** Der Name des pfads, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2987">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="cc80c-2988">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2988">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="cc80c-2989">Der Name MUSS eine auf NULL endende Unicode-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2989">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="cc80c-2990">Dieses Feld MUSS weggelassen werden, wenn \_ fRootPath auf 0x00000000 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2990">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="cc80c-2991">2.2.3.5 CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-2991">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="cc80c-2992">Die CPMForceMergeIn-Nachricht fordert einen Server zur Durchführung von Wartungsarbeiten an, die zur Verbesserung der Abfrageleistung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2992">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="cc80c-2993">Der Server antwortet mit dem Nachrichtenheader der CPMForceMergeIn-Nachricht, und die Ergebnisse der Anforderung sind im \_ Statusfeld enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-2993">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="cc80c-2994">Das Format der CPMForceMergeIn-Nachricht, die auf den Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-2994">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="cc80c-2995">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-2995">0</span></span>

<span data-ttu-id="cc80c-2996">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-2996">1</span></span>

<span data-ttu-id="cc80c-2997">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-2997">2</span></span>

<span data-ttu-id="cc80c-2998">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-2998">3</span></span>

<span data-ttu-id="cc80c-2999">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-2999">4</span></span>

<span data-ttu-id="cc80c-3000">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3000">5</span></span>

<span data-ttu-id="cc80c-3001">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3001">6</span></span>

<span data-ttu-id="cc80c-3002">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3002">7</span></span>

<span data-ttu-id="cc80c-3003">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3003">8</span></span>

<span data-ttu-id="cc80c-3004">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3004">9</span></span>

<span data-ttu-id="cc80c-3005">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3005">1</span></span><br/> <span data-ttu-id="cc80c-3006">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3006">0</span></span><br/>

<span data-ttu-id="cc80c-3007">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3007">1</span></span>

<span data-ttu-id="cc80c-3008">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3008">2</span></span>

<span data-ttu-id="cc80c-3009">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3009">3</span></span>

<span data-ttu-id="cc80c-3010">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3010">4</span></span>

<span data-ttu-id="cc80c-3011">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3011">5</span></span>

<span data-ttu-id="cc80c-3012">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3012">6</span></span>

<span data-ttu-id="cc80c-3013">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3013">7</span></span>

<span data-ttu-id="cc80c-3014">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3014">8</span></span>

<span data-ttu-id="cc80c-3015">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3015">9</span></span>

<span data-ttu-id="cc80c-3016">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3016">2</span></span><br/> <span data-ttu-id="cc80c-3017">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3017">0</span></span><br/>

<span data-ttu-id="cc80c-3018">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3018">1</span></span>

<span data-ttu-id="cc80c-3019">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3019">2</span></span>

<span data-ttu-id="cc80c-3020">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3020">3</span></span>

<span data-ttu-id="cc80c-3021">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3021">4</span></span>

<span data-ttu-id="cc80c-3022">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3022">5</span></span>

<span data-ttu-id="cc80c-3023">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3023">6</span></span>

<span data-ttu-id="cc80c-3024">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3024">7</span></span>

<span data-ttu-id="cc80c-3025">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3025">8</span></span>

<span data-ttu-id="cc80c-3026">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3026">9</span></span>

<span data-ttu-id="cc80c-3027">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3027">3</span></span><br/> <span data-ttu-id="cc80c-3028">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3028">0</span></span><br/>

<span data-ttu-id="cc80c-3029">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3029">1</span></span>

<span data-ttu-id="cc80c-3030">\_partID (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3030">\_partID (optional)</span></span>



 

<span data-ttu-id="cc80c-3031">**\_ partID:** Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3031">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="cc80c-3032">Wenn dieses Feld vorhanden ist, MUSS es auf 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3032">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="cc80c-3033">2.2.3.6 CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-3033">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="cc80c-3034">Die CPMConnectIn-Nachricht beginnt eine Sitzung zwischen Client und Server.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3034">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="cc80c-3035">Das Format der CPMConnectIn-Nachricht, die auf den Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3035">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3036">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3036">0</span></span>

<span data-ttu-id="cc80c-3037">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3037">1</span></span>

<span data-ttu-id="cc80c-3038">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3038">2</span></span>

<span data-ttu-id="cc80c-3039">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3039">3</span></span>

<span data-ttu-id="cc80c-3040">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3040">4</span></span>

<span data-ttu-id="cc80c-3041">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3041">5</span></span>

<span data-ttu-id="cc80c-3042">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3042">6</span></span>

<span data-ttu-id="cc80c-3043">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3043">7</span></span>

<span data-ttu-id="cc80c-3044">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3044">8</span></span>

<span data-ttu-id="cc80c-3045">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3045">9</span></span>

<span data-ttu-id="cc80c-3046">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3046">1</span></span><br/> <span data-ttu-id="cc80c-3047">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3047">0</span></span><br/>

<span data-ttu-id="cc80c-3048">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3048">1</span></span>

<span data-ttu-id="cc80c-3049">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3049">2</span></span>

<span data-ttu-id="cc80c-3050">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3050">3</span></span>

<span data-ttu-id="cc80c-3051">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3051">4</span></span>

<span data-ttu-id="cc80c-3052">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3052">5</span></span>

<span data-ttu-id="cc80c-3053">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3053">6</span></span>

<span data-ttu-id="cc80c-3054">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3054">7</span></span>

<span data-ttu-id="cc80c-3055">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3055">8</span></span>

<span data-ttu-id="cc80c-3056">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3056">9</span></span>

<span data-ttu-id="cc80c-3057">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3057">2</span></span><br/> <span data-ttu-id="cc80c-3058">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3058">0</span></span><br/>

<span data-ttu-id="cc80c-3059">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3059">1</span></span>

<span data-ttu-id="cc80c-3060">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3060">2</span></span>

<span data-ttu-id="cc80c-3061">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3061">3</span></span>

<span data-ttu-id="cc80c-3062">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3062">4</span></span>

<span data-ttu-id="cc80c-3063">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3063">5</span></span>

<span data-ttu-id="cc80c-3064">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3064">6</span></span>

<span data-ttu-id="cc80c-3065">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3065">7</span></span>

<span data-ttu-id="cc80c-3066">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3066">8</span></span>

<span data-ttu-id="cc80c-3067">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3067">9</span></span>

<span data-ttu-id="cc80c-3068">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3068">3</span></span><br/> <span data-ttu-id="cc80c-3069">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3069">0</span></span><br/>

<span data-ttu-id="cc80c-3070">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3070">1</span></span>

<span data-ttu-id="cc80c-3071">\_iClientVersion</span><span class="sxs-lookup"><span data-stu-id="cc80c-3071">\_iClientVersion</span></span>

<span data-ttu-id="cc80c-3072">\_fClientIsRemote</span><span class="sxs-lookup"><span data-stu-id="cc80c-3072">\_fClientIsRemote</span></span>

<span data-ttu-id="cc80c-3073">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3073">\_cbBlob1</span></span>

<span data-ttu-id="cc80c-3074">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3074">\_cbBlob2</span></span>

<span data-ttu-id="cc80c-3075">\_Polsterung</span><span class="sxs-lookup"><span data-stu-id="cc80c-3075">\_padding</span></span>

<span data-ttu-id="cc80c-3076">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-3076">...</span></span>

<span data-ttu-id="cc80c-3077">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-3077">...</span></span>

<span data-ttu-id="cc80c-3078">MachineName</span><span class="sxs-lookup"><span data-stu-id="cc80c-3078">MachineName</span></span>

<span data-ttu-id="cc80c-3079">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3079">... (variable)</span></span>

<span data-ttu-id="cc80c-3080">UserName</span><span class="sxs-lookup"><span data-stu-id="cc80c-3080">UserName</span></span>

<span data-ttu-id="cc80c-3081">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3081">... (variable)</span></span>

<span data-ttu-id="cc80c-3082">\_paddingcPropSets (optional, Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3082">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="cc80c-3083">cPropSets</span><span class="sxs-lookup"><span data-stu-id="cc80c-3083">cPropSets</span></span>

<span data-ttu-id="cc80c-3084">PropertySet1 (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3084">PropertySet1 (variable)</span></span>

<span data-ttu-id="cc80c-3085">PropertySet2 (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3085">PropertySet2 (variable)</span></span>

<span data-ttu-id="cc80c-3086">\_paddingExtPropset (optional, Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3086">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="cc80c-3087">cExtPropSet</span><span class="sxs-lookup"><span data-stu-id="cc80c-3087">cExtPropSet</span></span>

<span data-ttu-id="cc80c-3088">aPropertySets (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3088">aPropertySets (variable)</span></span>



 

<span data-ttu-id="cc80c-3089">**\_ iClientVersion:** Eine 32-Bit-Ganzzahl, die angibt, ob der Server den Prüfsummenwert überprüfen soll, der im \_ UlChecksum-Feld der Nachrichtenheader für vom Client gesendete Nachrichten angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3089">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="cc80c-3090">Wenn das \_ Feld iClientVersion auf 0x00000008 oder höher festgelegt ist, MUSS der Server den \_ UlChecksum-Feldwert für die folgenden Meldungen überprüfen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3090">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="cc80c-3091">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-3091">CPMConnectIn</span></span>
-   <span data-ttu-id="cc80c-3092">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-3092">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="cc80c-3093">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-3093">CPMFetchValueIn</span></span>
-   <span data-ttu-id="cc80c-3094">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-3094">CPMGetRowsIn</span></span>
-   <span data-ttu-id="cc80c-3095">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-3095">CPMSetBindingsIn</span></span>

<span data-ttu-id="cc80c-3096">Ausführliche Informationen dazu, wie der Server den vom Client im UlChecksum-Feld für die oben aufgeführten Nachrichten angegebenen Wert überprüft, finden Sie in Abschnitt 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3096">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="cc80c-3097">Wenn der Wert größer als 0x00000008 wird davon ausgegangen, dass der Client 64-Bit-Offsets in CPMGetRowsOut-Nachrichten verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3097">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="cc80c-3098">Weitere Informationen finden Sie in Abschnitt 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3098">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="cc80c-3099">*Windows-Verhalten: Auf Windows-Clients wird die iClientVersion wie folgt festgelegt:*</span><span class="sxs-lookup"><span data-stu-id="cc80c-3099">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="cc80c-3100">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-3100">Value</span></span>      | <span data-ttu-id="cc80c-3101">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-3101">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="cc80c-3102">0x00000005</span><span class="sxs-lookup"><span data-stu-id="cc80c-3102">0x00000005</span></span> | <span data-ttu-id="cc80c-3103">Das Clientbetriebssystem ist Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3103">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="cc80c-3104">0x00000008</span><span class="sxs-lookup"><span data-stu-id="cc80c-3104">0x00000008</span></span> | <span data-ttu-id="cc80c-3105">Das Clientbetriebssystem ist entweder 32-Bit-Windows XP oder 32-Bit-Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3105">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="cc80c-3106">0x00010008</span><span class="sxs-lookup"><span data-stu-id="cc80c-3106">0x00010008</span></span> | <span data-ttu-id="cc80c-3107">Das Clientbetriebssystem ist entweder 64-Bit-Windows XP oder 64-Bit-Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3107">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="cc80c-3108">\_**fClientIsRemote:** Ein boolescher Wert, der angibt, ob der Client auf einem anderen Computer als dem Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3108">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="cc80c-3109">MUSS auf 0x00000001 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3109">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="cc80c-3110">\_**cbBlob1:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der Felder cPropSet, PropertySet1 und PropertySet2 in Bytes angibt, kombiniert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3110">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="cc80c-3111">\_**cbBlob2:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe von cExPropSet- und aPropertySet-Feldern in Bytes angibt, kombiniert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3111">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="cc80c-3112">\_**Padding:** 12 Byte Auf padding, die beliebige Werte enthalten können und IGNORIERT WERDEN MÜSSEN.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3112">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="cc80c-3113">**MachineName:** Der Computername des Clients.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3113">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="cc80c-3114">Die Namenszeichenfolge MUSS ein array mit NULL-Terminierung sein, das weniger als 512 Unicode-Zeichen enthält, einschließlich des NULL-Abschlusszeichens.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3114">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="cc80c-3115">**UserName:** Eine Zeichenfolge, die den Benutzernamen der Person darstellt, die die Anwendung ausgeführt, die dieses Protokoll aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3115">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="cc80c-3116">Die Namenszeichenfolge MUSS ein array mit NULL-Terminierung sein, das weniger als 512 Unicode-Zeichen enthält, wenn sie mit MachineName verkettet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3116">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="cc80c-3117">**\_ paddingcPropSets:** Dieses Feld MUSS 0 bis 7 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3117">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="cc80c-3118">Die Anzahl der Bytes MUSS die Zahl sein, die erforderlich ist, um den Byteoffset des cPropSets-Felds vom Anfang der Nachricht, die diese Struktur enthält, ein Vielfaches von 8 zu machen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3118">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="cc80c-3119">Der Wert der Bytes kann ein beliebiger Wert sein, und MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3119">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cc80c-3120">**cPropSets:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der CDbPropSet-Strukturen nach diesem Feld angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3120">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="cc80c-3121">Dieser Wert MUSS auf "0x0000002.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3121">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="cc80c-3122">**PropertySet1:** Eine CDbPropSet-Struktur mit guidPropertySet, die DBPROPSET \_ FSCIFRMWRK \_ EXT enthält (siehe Abschnitt 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="cc80c-3122">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="cc80c-3123">**PropertySet2:** Eine CDbPropSet-Struktur mit guidPropertySet, die DBPROPSET \_ CIFRMWRKCORE \_ EXT enthält (siehe Abschnitt 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="cc80c-3123">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="cc80c-3124">\_**PaddingExtPropset:** Dieses Feld MUSS 0 bis 7 Bytes lang sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3124">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="cc80c-3125">Die Anzahl der Bytes MUSS die Zahl sein, die erforderlich ist, um den Byteoffset des Felds cExtPropSets vom Anfang der Nachricht, die diese Struktur enthält, ein Vielfaches von 8 zu machen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3125">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="cc80c-3126">Der Wert der Bytes kann ein beliebiger Wert sein, und MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3126">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cc80c-3127">**cExtPropSet:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der CDbPropSet-Strukturen nach diesem Feld angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3127">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="cc80c-3128">**aPropertySets:** Ein Array von CDbPropSet-Strukturen, die andere Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3128">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="cc80c-3129">Die Anzahl der Elemente in diesem Array MUSS cExtPropSet entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3129">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="cc80c-3130">2.2.3.7 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-3130">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="cc80c-3131">Die CPMConnectOut-Nachricht enthält eine Antwort auf eine CPMConnectIn-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3131">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="cc80c-3132">Das Format der CPMConnectOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3132">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3133">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3133">0</span></span>

<span data-ttu-id="cc80c-3134">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3134">1</span></span>

<span data-ttu-id="cc80c-3135">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3135">2</span></span>

<span data-ttu-id="cc80c-3136">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3136">3</span></span>

<span data-ttu-id="cc80c-3137">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3137">4</span></span>

<span data-ttu-id="cc80c-3138">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3138">5</span></span>

<span data-ttu-id="cc80c-3139">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3139">6</span></span>

<span data-ttu-id="cc80c-3140">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3140">7</span></span>

<span data-ttu-id="cc80c-3141">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3141">8</span></span>

<span data-ttu-id="cc80c-3142">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3142">9</span></span>

<span data-ttu-id="cc80c-3143">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3143">1</span></span><br/> <span data-ttu-id="cc80c-3144">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3144">0</span></span><br/>

<span data-ttu-id="cc80c-3145">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3145">1</span></span>

<span data-ttu-id="cc80c-3146">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3146">2</span></span>

<span data-ttu-id="cc80c-3147">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3147">3</span></span>

<span data-ttu-id="cc80c-3148">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3148">4</span></span>

<span data-ttu-id="cc80c-3149">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3149">5</span></span>

<span data-ttu-id="cc80c-3150">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3150">6</span></span>

<span data-ttu-id="cc80c-3151">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3151">7</span></span>

<span data-ttu-id="cc80c-3152">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3152">8</span></span>

<span data-ttu-id="cc80c-3153">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3153">9</span></span>

<span data-ttu-id="cc80c-3154">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3154">2</span></span><br/> <span data-ttu-id="cc80c-3155">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3155">0</span></span><br/>

<span data-ttu-id="cc80c-3156">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3156">1</span></span>

<span data-ttu-id="cc80c-3157">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3157">2</span></span>

<span data-ttu-id="cc80c-3158">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3158">3</span></span>

<span data-ttu-id="cc80c-3159">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3159">4</span></span>

<span data-ttu-id="cc80c-3160">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3160">5</span></span>

<span data-ttu-id="cc80c-3161">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3161">6</span></span>

<span data-ttu-id="cc80c-3162">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3162">7</span></span>

<span data-ttu-id="cc80c-3163">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3163">8</span></span>

<span data-ttu-id="cc80c-3164">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3164">9</span></span>

<span data-ttu-id="cc80c-3165">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3165">3</span></span><br/> <span data-ttu-id="cc80c-3166">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3166">0</span></span><br/>

<span data-ttu-id="cc80c-3167">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3167">1</span></span>

<span data-ttu-id="cc80c-3168">\_serverVersion</span><span class="sxs-lookup"><span data-stu-id="cc80c-3168">\_serverVersion</span></span>

<span data-ttu-id="cc80c-3169">\_reserviert (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3169">\_reserved (variable)</span></span>



 

<span data-ttu-id="cc80c-3170">**\_ serverVersion**:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3170">**\_serverVersion**:</span></span>

<span data-ttu-id="cc80c-3171">Eine 32-Bit-Ganzzahl, die angibt, ob der Server 64-Bit-Offsets unterstützen *kann.*</span><span class="sxs-lookup"><span data-stu-id="cc80c-3171">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="cc80c-3172">Weitere Informationen finden Sie in Abschnitt 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3172">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="cc80c-3173">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-3173">Value</span></span>      | <span data-ttu-id="cc80c-3174">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-3174">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="cc80c-3175">0x00000007</span><span class="sxs-lookup"><span data-stu-id="cc80c-3175">0x00000007</span></span> | <span data-ttu-id="cc80c-3176">Der Server kann nur 32-Bit-Offsets senden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3176">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="cc80c-3177">0x00010007</span><span class="sxs-lookup"><span data-stu-id="cc80c-3177">0x00010007</span></span> | <span data-ttu-id="cc80c-3178">Der Server kann 32- oder 64-Bit-Offsets senden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3178">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="cc80c-3179">**\_ reserviert:** Reserviert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3179">**\_reserved**: Reserved.</span></span> <span data-ttu-id="cc80c-3180">Der Server KANN eine beliebige Anzahl beliebiger Werte senden, und der Client MUSS diese Werte ignorieren, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3180">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="cc80c-3181">2.2.3.8 CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-3181">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="cc80c-3182">Die CPMCreateQueryIn-Nachricht erstellt eine neue Abfrage.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3182">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="cc80c-3183">Das Format der CPMCreateQueryIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3183">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3184">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3184">0</span></span>

<span data-ttu-id="cc80c-3185">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3185">1</span></span>

<span data-ttu-id="cc80c-3186">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3186">2</span></span>

<span data-ttu-id="cc80c-3187">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3187">3</span></span>

<span data-ttu-id="cc80c-3188">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3188">4</span></span>

<span data-ttu-id="cc80c-3189">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3189">5</span></span>

<span data-ttu-id="cc80c-3190">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3190">6</span></span>

<span data-ttu-id="cc80c-3191">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3191">7</span></span>

<span data-ttu-id="cc80c-3192">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3192">8</span></span>

<span data-ttu-id="cc80c-3193">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3193">9</span></span>

<span data-ttu-id="cc80c-3194">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3194">1</span></span><br/> <span data-ttu-id="cc80c-3195">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3195">0</span></span><br/>

<span data-ttu-id="cc80c-3196">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3196">1</span></span>

<span data-ttu-id="cc80c-3197">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3197">2</span></span>

<span data-ttu-id="cc80c-3198">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3198">3</span></span>

<span data-ttu-id="cc80c-3199">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3199">4</span></span>

<span data-ttu-id="cc80c-3200">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3200">5</span></span>

<span data-ttu-id="cc80c-3201">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3201">6</span></span>

<span data-ttu-id="cc80c-3202">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3202">7</span></span>

<span data-ttu-id="cc80c-3203">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3203">8</span></span>

<span data-ttu-id="cc80c-3204">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3204">9</span></span>

<span data-ttu-id="cc80c-3205">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3205">2</span></span><br/> <span data-ttu-id="cc80c-3206">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3206">0</span></span><br/>

<span data-ttu-id="cc80c-3207">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3207">1</span></span>

<span data-ttu-id="cc80c-3208">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3208">2</span></span>

<span data-ttu-id="cc80c-3209">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3209">3</span></span>

<span data-ttu-id="cc80c-3210">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3210">4</span></span>

<span data-ttu-id="cc80c-3211">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3211">5</span></span>

<span data-ttu-id="cc80c-3212">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3212">6</span></span>

<span data-ttu-id="cc80c-3213">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3213">7</span></span>

<span data-ttu-id="cc80c-3214">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3214">8</span></span>

<span data-ttu-id="cc80c-3215">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3215">9</span></span>

<span data-ttu-id="cc80c-3216">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3216">3</span></span><br/> <span data-ttu-id="cc80c-3217">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3217">0</span></span><br/>

<span data-ttu-id="cc80c-3218">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3218">1</span></span>

<span data-ttu-id="cc80c-3219">Size</span><span class="sxs-lookup"><span data-stu-id="cc80c-3219">Size</span></span>

<span data-ttu-id="cc80c-3220">CColumnSetPresent</span><span class="sxs-lookup"><span data-stu-id="cc80c-3220">CColumnSetPresent</span></span>

<span data-ttu-id="cc80c-3221">ColumnSet (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3221">ColumnSet (optional)</span></span>

<span data-ttu-id="cc80c-3222">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3222">... (variable)</span></span>

<span data-ttu-id="cc80c-3223">CRestrictionPresent.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3223">CRestrictionPresent.</span></span>

<span data-ttu-id="cc80c-3224">Einschränkung (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3224">Restriction (optional)</span></span>

<span data-ttu-id="cc80c-3225">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3225">... (variable)</span></span>

<span data-ttu-id="cc80c-3226">CSortSetPresent</span><span class="sxs-lookup"><span data-stu-id="cc80c-3226">CSortSetPresent</span></span>

<span data-ttu-id="cc80c-3227">SortSet (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3227">SortSet (optional)</span></span>

<span data-ttu-id="cc80c-3228">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3228">... (variable)</span></span>

<span data-ttu-id="cc80c-3229">CCategorizationSetPresent</span><span class="sxs-lookup"><span data-stu-id="cc80c-3229">CCategorizationSetPresent</span></span>

<span data-ttu-id="cc80c-3230">CategorizationSet (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3230">CategorizationSet (optional)</span></span>

<span data-ttu-id="cc80c-3231">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3231">... (variable)</span></span>

<span data-ttu-id="cc80c-3232">RowSetProperties</span><span class="sxs-lookup"><span data-stu-id="cc80c-3232">RowSetProperties</span></span>

<span data-ttu-id="cc80c-3233">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-3233">...</span></span>

<span data-ttu-id="cc80c-3234">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-3234">...</span></span>

<span data-ttu-id="cc80c-3235">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-3235">...</span></span>

<span data-ttu-id="cc80c-3236">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-3236">...</span></span>

<span data-ttu-id="cc80c-3237">PidMapper (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3237">PidMapper (variable)</span></span>



 

<span data-ttu-id="cc80c-3238">**Größe:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Bytes vom Anfang dieses Felds bis zum Ende der Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3238">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="cc80c-3239">**CColumnSetPresent:** Ein Bytefeld, das angibt, ob das ColumnSet-Feld vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3239">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="cc80c-3240">Dieses Feld MUSS auf 0x01 oder 0x00.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3240">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="cc80c-3241">Wenn diese 0x01 muss das CColumnSet-Feld vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3241">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="cc80c-3242">Wenn sie auf 0x00 festgelegt ist, MUSS sie nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3242">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="cc80c-3243">**ColumnSet:** Eine CColumnSet-Struktur, die die Spaltennummern enthält, in denen die Eigenschaften von CPidMapper zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3243">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="cc80c-3244">**CRestrictionPresent:** Ein Bytefeld, das angibt, ob das Feld Einschränkung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3244">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="cc80c-3245">Wenn dieses Feld auf einen Wert ungleich 0 (null) festgelegt ist, MUSS das Feld Einschränkung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3245">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="cc80c-3246">Wenn diese 0x00 festgelegt ist, DARF die Einschränkung nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3246">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="cc80c-3247">**Einschränkung:** Eine CRestriction-Struktur, die die Befehlsstruktur der Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3247">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="cc80c-3248">**CSortSetPresent:** Ein Bytefeld, das angibt, ob das SortSet-Feld vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3248">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="cc80c-3249">Wenn ein Wert ungleich 0 (null) festgelegt ist, MUSS das SortSet-Feld vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3249">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="cc80c-3250">Wenn sortSet auf 0x00 festgelegt ist, MUSS es nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3250">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="cc80c-3251">**SortSet:** Eine CSortSet-Struktur, die die Sortierreihenfolge der Abfrage angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3251">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="cc80c-3252">**CCategorizationSetPresent:** Ein Bytefeld, das angibt, ob das Feld CCategorizationSet vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3252">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="cc80c-3253">Wenn ein Wert ungleich 0 (null) festgelegt ist, MUSS das Feld CCategorizationSet vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3253">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="cc80c-3254">Wenn CCategorizationSet auf 0x00 festgelegt ist, MUSS es nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3254">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="cc80c-3255">**CCategorizationSet:** Eine CCategorizationSet-Struktur, die die Gruppen für die Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3255">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="cc80c-3256">**RowSetProperties:** Eine CRowsetProperties-Struktur, die Konfigurationsinformationen für die Abfrage bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3256">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="cc80c-3257">**PidMapper:** Eine CPidMapper-Struktur, die Eigenschaften enthält, die in einem Rowset zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3257">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="cc80c-3258">2.2.3.9 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-3258">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="cc80c-3259">Die CPMCreateQueryOut-Nachricht enthält eine Antwort auf eine CPMCreateQueryIn-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3259">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="cc80c-3260">Das Format der CPMCreateQueryOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3260">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3261">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3261">0</span></span>

<span data-ttu-id="cc80c-3262">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3262">1</span></span>

<span data-ttu-id="cc80c-3263">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3263">2</span></span>

<span data-ttu-id="cc80c-3264">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3264">3</span></span>

<span data-ttu-id="cc80c-3265">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3265">4</span></span>

<span data-ttu-id="cc80c-3266">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3266">5</span></span>

<span data-ttu-id="cc80c-3267">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3267">6</span></span>

<span data-ttu-id="cc80c-3268">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3268">7</span></span>

<span data-ttu-id="cc80c-3269">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3269">8</span></span>

<span data-ttu-id="cc80c-3270">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3270">9</span></span>

<span data-ttu-id="cc80c-3271">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3271">1</span></span><br/> <span data-ttu-id="cc80c-3272">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3272">0</span></span><br/>

<span data-ttu-id="cc80c-3273">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3273">1</span></span>

<span data-ttu-id="cc80c-3274">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3274">2</span></span>

<span data-ttu-id="cc80c-3275">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3275">3</span></span>

<span data-ttu-id="cc80c-3276">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3276">4</span></span>

<span data-ttu-id="cc80c-3277">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3277">5</span></span>

<span data-ttu-id="cc80c-3278">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3278">6</span></span>

<span data-ttu-id="cc80c-3279">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3279">7</span></span>

<span data-ttu-id="cc80c-3280">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3280">8</span></span>

<span data-ttu-id="cc80c-3281">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3281">9</span></span>

<span data-ttu-id="cc80c-3282">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3282">2</span></span><br/> <span data-ttu-id="cc80c-3283">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3283">0</span></span><br/>

<span data-ttu-id="cc80c-3284">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3284">1</span></span>

<span data-ttu-id="cc80c-3285">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3285">2</span></span>

<span data-ttu-id="cc80c-3286">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3286">3</span></span>

<span data-ttu-id="cc80c-3287">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3287">4</span></span>

<span data-ttu-id="cc80c-3288">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3288">5</span></span>

<span data-ttu-id="cc80c-3289">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3289">6</span></span>

<span data-ttu-id="cc80c-3290">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3290">7</span></span>

<span data-ttu-id="cc80c-3291">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3291">8</span></span>

<span data-ttu-id="cc80c-3292">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3292">9</span></span>

<span data-ttu-id="cc80c-3293">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3293">3</span></span><br/> <span data-ttu-id="cc80c-3294">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3294">0</span></span><br/>

<span data-ttu-id="cc80c-3295">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3295">1</span></span>

<span data-ttu-id="cc80c-3296">\_fTrueSequential</span><span class="sxs-lookup"><span data-stu-id="cc80c-3296">\_fTrueSequential</span></span>

<span data-ttu-id="cc80c-3297">\_fWorkIdUnique</span><span class="sxs-lookup"><span data-stu-id="cc80c-3297">\_fWorkIdUnique</span></span>

<span data-ttu-id="cc80c-3298">aCursors</span><span class="sxs-lookup"><span data-stu-id="cc80c-3298">aCursors</span></span>



 

<span data-ttu-id="cc80c-3299">**\_ fTrueSequential:** Ein informativer boolescher Wert, der angibt, ob die Abfrage ergebnisse schneller liefern kann.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3299">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="cc80c-3300">Wenn für die in CPMCreateQueryIn bereitgestellte Abfrage 0x00000001 festgelegt ist, kann der Server den Index so verwenden, dass die Abfrageergebnisse wahrscheinlich schneller übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3300">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="cc80c-3301">Wenn sie auf 0x00000000 festgelegt ist, kommt es bei der Übermittlung von Abfrageergebnissen zu einer höheren Latenz.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3301">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="cc80c-3302">DARF nicht auf einen anderen Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3302">MUST not be set to any other value.</span></span>

<span data-ttu-id="cc80c-3303">**\_ fWorkIdUnique:** Ein boolescher Wert, der angibt, ob die Dokumentbezeichner, auf die die Cursor zeigen, in den Abfrageergebnissen eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3303">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="cc80c-3304">Wenn diese 0x00000001, sind die Bezeichner eindeutig.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3304">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="cc80c-3305">Wenn diese 0x00000000, sind sie nur im gesamten Rowset eindeutig.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3305">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="cc80c-3306">**aCursors:** Ein Array von 32-Bit-Ganzzahlen ohne Vorzeichen, die die Handles für Cursor darstellen, mit der Anzahl von Elementen, die der Anzahl der Kategorien im CategorizationSet-Feld der CPMCreateQueryIn-Nachricht entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3306">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="cc80c-3307">2.2.3.10 CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-3307">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="cc80c-3308">Die CPMGetQueryStatusIn-Nachricht fordert den Status einer Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3308">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="cc80c-3309">Das Format der CPMGetQueryStatusIn-Nachricht, die auf den Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3309">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3310">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3310">0</span></span>

<span data-ttu-id="cc80c-3311">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3311">1</span></span>

<span data-ttu-id="cc80c-3312">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3312">2</span></span>

<span data-ttu-id="cc80c-3313">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3313">3</span></span>

<span data-ttu-id="cc80c-3314">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3314">4</span></span>

<span data-ttu-id="cc80c-3315">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3315">5</span></span>

<span data-ttu-id="cc80c-3316">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3316">6</span></span>

<span data-ttu-id="cc80c-3317">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3317">7</span></span>

<span data-ttu-id="cc80c-3318">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3318">8</span></span>

<span data-ttu-id="cc80c-3319">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3319">9</span></span>

<span data-ttu-id="cc80c-3320">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3320">1</span></span><br/> <span data-ttu-id="cc80c-3321">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3321">0</span></span><br/>

<span data-ttu-id="cc80c-3322">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3322">1</span></span>

<span data-ttu-id="cc80c-3323">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3323">2</span></span>

<span data-ttu-id="cc80c-3324">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3324">3</span></span>

<span data-ttu-id="cc80c-3325">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3325">4</span></span>

<span data-ttu-id="cc80c-3326">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3326">5</span></span>

<span data-ttu-id="cc80c-3327">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3327">6</span></span>

<span data-ttu-id="cc80c-3328">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3328">7</span></span>

<span data-ttu-id="cc80c-3329">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3329">8</span></span>

<span data-ttu-id="cc80c-3330">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3330">9</span></span>

<span data-ttu-id="cc80c-3331">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3331">2</span></span><br/> <span data-ttu-id="cc80c-3332">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3332">0</span></span><br/>

<span data-ttu-id="cc80c-3333">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3333">1</span></span>

<span data-ttu-id="cc80c-3334">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3334">2</span></span>

<span data-ttu-id="cc80c-3335">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3335">3</span></span>

<span data-ttu-id="cc80c-3336">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3336">4</span></span>

<span data-ttu-id="cc80c-3337">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3337">5</span></span>

<span data-ttu-id="cc80c-3338">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3338">6</span></span>

<span data-ttu-id="cc80c-3339">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3339">7</span></span>

<span data-ttu-id="cc80c-3340">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3340">8</span></span>

<span data-ttu-id="cc80c-3341">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3341">9</span></span>

<span data-ttu-id="cc80c-3342">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3342">3</span></span><br/> <span data-ttu-id="cc80c-3343">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3343">0</span></span><br/>

<span data-ttu-id="cc80c-3344">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3344">1</span></span>

<span data-ttu-id="cc80c-3345">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cc80c-3345">\_hCursor</span></span>



 

<span data-ttu-id="cc80c-3346">**\_ hCursor:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Handle aus der CPMCreateQueryOut-Nachricht darstellt, die die Abfrage identifiziert, für die Statusinformationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3346">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="cc80c-3347">2.2.3.11 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-3347">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="cc80c-3348">Die CPMGetQueryStatusOut-Nachricht antwortet auf eine CPMGetQueryStatusIn-Nachricht mit dem Status der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3348">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="cc80c-3349">Das Format der CPMGetQueryStatusOut-Nachricht, die auf den Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3349">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3350">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3350">0</span></span>

<span data-ttu-id="cc80c-3351">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3351">1</span></span>

<span data-ttu-id="cc80c-3352">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3352">2</span></span>

<span data-ttu-id="cc80c-3353">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3353">3</span></span>

<span data-ttu-id="cc80c-3354">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3354">4</span></span>

<span data-ttu-id="cc80c-3355">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3355">5</span></span>

<span data-ttu-id="cc80c-3356">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3356">6</span></span>

<span data-ttu-id="cc80c-3357">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3357">7</span></span>

<span data-ttu-id="cc80c-3358">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3358">8</span></span>

<span data-ttu-id="cc80c-3359">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3359">9</span></span>

<span data-ttu-id="cc80c-3360">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3360">1</span></span><br/> <span data-ttu-id="cc80c-3361">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3361">0</span></span><br/>

<span data-ttu-id="cc80c-3362">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3362">1</span></span>

<span data-ttu-id="cc80c-3363">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3363">2</span></span>

<span data-ttu-id="cc80c-3364">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3364">3</span></span>

<span data-ttu-id="cc80c-3365">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3365">4</span></span>

<span data-ttu-id="cc80c-3366">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3366">5</span></span>

<span data-ttu-id="cc80c-3367">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3367">6</span></span>

<span data-ttu-id="cc80c-3368">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3368">7</span></span>

<span data-ttu-id="cc80c-3369">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3369">8</span></span>

<span data-ttu-id="cc80c-3370">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3370">9</span></span>

<span data-ttu-id="cc80c-3371">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3371">2</span></span><br/> <span data-ttu-id="cc80c-3372">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3372">0</span></span><br/>

<span data-ttu-id="cc80c-3373">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3373">1</span></span>

<span data-ttu-id="cc80c-3374">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3374">2</span></span>

<span data-ttu-id="cc80c-3375">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3375">3</span></span>

<span data-ttu-id="cc80c-3376">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3376">4</span></span>

<span data-ttu-id="cc80c-3377">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3377">5</span></span>

<span data-ttu-id="cc80c-3378">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3378">6</span></span>

<span data-ttu-id="cc80c-3379">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3379">7</span></span>

<span data-ttu-id="cc80c-3380">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3380">8</span></span>

<span data-ttu-id="cc80c-3381">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3381">9</span></span>

<span data-ttu-id="cc80c-3382">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3382">3</span></span><br/> <span data-ttu-id="cc80c-3383">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3383">0</span></span><br/>

<span data-ttu-id="cc80c-3384">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3384">1</span></span>

<span data-ttu-id="cc80c-3385">\_Status</span><span class="sxs-lookup"><span data-stu-id="cc80c-3385">\_Status</span></span>



 

<span data-ttu-id="cc80c-3386">**\_ Status:** Eine Bitmaske mit Werten, die in den folgenden Tabellen definiert sind und die Abfrage beschreiben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3386">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="cc80c-3387">In der folgenden Tabelle sind die STAT-Werte aufgeführt, die durch Ausführen einer bitweise AND-Operation für \_ \* Status mit \_ 0x00000007.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3387">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="cc80c-3388">Das Ergebnis MUSS eines der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3388">The result MUST be one of the following:</span></span>



| <span data-ttu-id="cc80c-3389">Konstante</span><span class="sxs-lookup"><span data-stu-id="cc80c-3389">Constant</span></span>                 | <span data-ttu-id="cc80c-3390">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-3390">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-3391">STAT \_ BUSY 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-3391">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="cc80c-3392">Die asynchrone Abfrage wird weiterhin ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3392">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="cc80c-3393">STAT \_ ERROR 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-3393">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="cc80c-3394">Die Abfrage befindet sich in einem Fehlerzustand.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3394">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="cc80c-3395">STAT \_ DONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-3395">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="cc80c-3396">Die Abfrage ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3396">The query is complete.</span></span>                                                            |
| <span data-ttu-id="cc80c-3397">STAT \_ REFRESH 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-3397">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="cc80c-3398">Die Abfrage ist abgeschlossen, aber Updates führen zu einer zusätzlichen Abfrageberechnung.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3398">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="cc80c-3399">In der folgenden Tabelle sind zusätzliche \_ \* STAT-Bits aufgeführt, die unabhängig voneinander festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3399">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="cc80c-3400">Konstante</span><span class="sxs-lookup"><span data-stu-id="cc80c-3400">Constant</span></span>                                    | <span data-ttu-id="cc80c-3401">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-3401">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc80c-3402">STAT \_ NOISE \_ WORDS 0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc80c-3402">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="cc80c-3403">Füllwörter wurden in der Inhaltsabfrage durch Platzhalterzeichen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3403">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="cc80c-3404">VERALTETE \_ \_ \_ \_ 0X00000020</span><span class="sxs-lookup"><span data-stu-id="cc80c-3404">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="cc80c-3405">Die Ergebnisse der Abfrage sind möglicherweise falsch, da die Abfrage geänderte, aber nicht indizierte Dateien umfasst.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3405">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="cc80c-3406">\_STAT REFRESH \_ INCOMPLETE 0x00000040</span><span class="sxs-lookup"><span data-stu-id="cc80c-3406">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="cc80c-3407">Die Ergebnisse der Abfrage sind möglicherweise falsch, da die Abfrage geänderte und neu indizierte Dateien umfasste, deren Inhalt nicht enthalten war.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3407">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="cc80c-3408">STAT \_ CONTENT QUERY INCOMPLETE \_ \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="cc80c-3408">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="cc80c-3409">Die Inhaltsabfrage war zu komplex, um die Enumeration abzuschließen oder zu erfordern, anstatt den Inhaltsindex zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3409">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="cc80c-3410">STAT \_ TIME \_ LIMIT \_ EXCEEDED 0x00000100</span><span class="sxs-lookup"><span data-stu-id="cc80c-3410">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="cc80c-3411">Die Ergebnisse der Abfrage sind möglicherweise falsch, da die Ausführungszeit der Abfrage die maximal zulässige Zeit erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3411">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="cc80c-3412">2.2.3.12 CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-3412">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="cc80c-3413">Die CPMGetQueryStatusExIn-Nachricht fordert den Status einer Abfrage und zusätzliche Informationen an, z. B. die Anzahl der indizierten Dokumente, die Anzahl der zu indizierten Dokumente usw.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3413">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="cc80c-3414">Das Format der CPMGetQueryStatusExIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3414">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3415">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3415">0</span></span>

<span data-ttu-id="cc80c-3416">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3416">1</span></span>

<span data-ttu-id="cc80c-3417">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3417">2</span></span>

<span data-ttu-id="cc80c-3418">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3418">3</span></span>

<span data-ttu-id="cc80c-3419">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3419">4</span></span>

<span data-ttu-id="cc80c-3420">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3420">5</span></span>

<span data-ttu-id="cc80c-3421">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3421">6</span></span>

<span data-ttu-id="cc80c-3422">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3422">7</span></span>

<span data-ttu-id="cc80c-3423">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3423">8</span></span>

<span data-ttu-id="cc80c-3424">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3424">9</span></span>

<span data-ttu-id="cc80c-3425">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3425">1</span></span><br/> <span data-ttu-id="cc80c-3426">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3426">0</span></span><br/>

<span data-ttu-id="cc80c-3427">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3427">1</span></span>

<span data-ttu-id="cc80c-3428">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3428">2</span></span>

<span data-ttu-id="cc80c-3429">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3429">3</span></span>

<span data-ttu-id="cc80c-3430">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3430">4</span></span>

<span data-ttu-id="cc80c-3431">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3431">5</span></span>

<span data-ttu-id="cc80c-3432">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3432">6</span></span>

<span data-ttu-id="cc80c-3433">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3433">7</span></span>

<span data-ttu-id="cc80c-3434">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3434">8</span></span>

<span data-ttu-id="cc80c-3435">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3435">9</span></span>

<span data-ttu-id="cc80c-3436">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3436">2</span></span><br/> <span data-ttu-id="cc80c-3437">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3437">0</span></span><br/>

<span data-ttu-id="cc80c-3438">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3438">1</span></span>

<span data-ttu-id="cc80c-3439">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3439">2</span></span>

<span data-ttu-id="cc80c-3440">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3440">3</span></span>

<span data-ttu-id="cc80c-3441">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3441">4</span></span>

<span data-ttu-id="cc80c-3442">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3442">5</span></span>

<span data-ttu-id="cc80c-3443">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3443">6</span></span>

<span data-ttu-id="cc80c-3444">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3444">7</span></span>

<span data-ttu-id="cc80c-3445">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3445">8</span></span>

<span data-ttu-id="cc80c-3446">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3446">9</span></span>

<span data-ttu-id="cc80c-3447">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3447">3</span></span><br/> <span data-ttu-id="cc80c-3448">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3448">0</span></span><br/>

<span data-ttu-id="cc80c-3449">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3449">1</span></span>

<span data-ttu-id="cc80c-3450">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cc80c-3450">\_hCursor</span></span>

<span data-ttu-id="cc80c-3451">\_bmk</span><span class="sxs-lookup"><span data-stu-id="cc80c-3451">\_bmk</span></span>



 

<span data-ttu-id="cc80c-3452">**\_ hCursor:** Ein 32-Bit-Wert, der das Handle aus der CPMCreateQueryOut-Nachricht darstellt und die Abfrage identifiziert, für die Statusinformationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3452">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="cc80c-3453">**\_ bmk:** Ein 32-Bit-Wert, der das Handle eines Lesezeichens angibt, dessen Position abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3453">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="cc80c-3454">2.2.3.13 CPMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-3454">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="cc80c-3455">Die CPMGetQueryStatusExOut-Nachricht antwortet auf eine CPMGetQueryStatusExIn-Nachricht mit dem Status der Abfrage und anderen Statusinformationen, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3455">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="cc80c-3456">Das Format der CPMGetQueryStatusExOut-Nachricht, die auf den Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3456">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3457">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3457">0</span></span>

<span data-ttu-id="cc80c-3458">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3458">1</span></span>

<span data-ttu-id="cc80c-3459">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3459">2</span></span>

<span data-ttu-id="cc80c-3460">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3460">3</span></span>

<span data-ttu-id="cc80c-3461">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3461">4</span></span>

<span data-ttu-id="cc80c-3462">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3462">5</span></span>

<span data-ttu-id="cc80c-3463">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3463">6</span></span>

<span data-ttu-id="cc80c-3464">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3464">7</span></span>

<span data-ttu-id="cc80c-3465">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3465">8</span></span>

<span data-ttu-id="cc80c-3466">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3466">9</span></span>

<span data-ttu-id="cc80c-3467">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3467">1</span></span><br/> <span data-ttu-id="cc80c-3468">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3468">0</span></span><br/>

<span data-ttu-id="cc80c-3469">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3469">1</span></span>

<span data-ttu-id="cc80c-3470">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3470">2</span></span>

<span data-ttu-id="cc80c-3471">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3471">3</span></span>

<span data-ttu-id="cc80c-3472">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3472">4</span></span>

<span data-ttu-id="cc80c-3473">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3473">5</span></span>

<span data-ttu-id="cc80c-3474">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3474">6</span></span>

<span data-ttu-id="cc80c-3475">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3475">7</span></span>

<span data-ttu-id="cc80c-3476">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3476">8</span></span>

<span data-ttu-id="cc80c-3477">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3477">9</span></span>

<span data-ttu-id="cc80c-3478">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3478">2</span></span><br/> <span data-ttu-id="cc80c-3479">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3479">0</span></span><br/>

<span data-ttu-id="cc80c-3480">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3480">1</span></span>

<span data-ttu-id="cc80c-3481">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3481">2</span></span>

<span data-ttu-id="cc80c-3482">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3482">3</span></span>

<span data-ttu-id="cc80c-3483">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3483">4</span></span>

<span data-ttu-id="cc80c-3484">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3484">5</span></span>

<span data-ttu-id="cc80c-3485">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3485">6</span></span>

<span data-ttu-id="cc80c-3486">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3486">7</span></span>

<span data-ttu-id="cc80c-3487">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3487">8</span></span>

<span data-ttu-id="cc80c-3488">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3488">9</span></span>

<span data-ttu-id="cc80c-3489">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3489">3</span></span><br/> <span data-ttu-id="cc80c-3490">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3490">0</span></span><br/>

<span data-ttu-id="cc80c-3491">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3491">1</span></span>

<span data-ttu-id="cc80c-3492">\_Status</span><span class="sxs-lookup"><span data-stu-id="cc80c-3492">\_Status</span></span>

<span data-ttu-id="cc80c-3493">\_cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="cc80c-3493">\_cFilteredDocuments</span></span>

<span data-ttu-id="cc80c-3494">\_cDocumentsToFilter</span><span class="sxs-lookup"><span data-stu-id="cc80c-3494">\_cDocumentsToFilter</span></span>

<span data-ttu-id="cc80c-3495">\_dwRatioFinishedDenominator</span><span class="sxs-lookup"><span data-stu-id="cc80c-3495">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="cc80c-3496">\_dwRatioFinishedNumerator</span><span class="sxs-lookup"><span data-stu-id="cc80c-3496">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="cc80c-3497">\_iRowBmk</span><span class="sxs-lookup"><span data-stu-id="cc80c-3497">\_iRowBmk</span></span>

<span data-ttu-id="cc80c-3498">\_cRowsTotal</span><span class="sxs-lookup"><span data-stu-id="cc80c-3498">\_cRowsTotal</span></span>



 

<span data-ttu-id="cc80c-3499">**\_ Status:** Eines der STAT \_ \* -Werte, die in Abschnitt 2.2.3.11 angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3499">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="cc80c-3500">**\_ cFilteredDocuments:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der indizierten Dokumente angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3500">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="cc80c-3501">**\_ cDocumentsToFilter:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die angibt, wie viele Dokumente noch indiziert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3501">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="cc80c-3502">**\_ dwRatioFinishedDenominator:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Nenner des Verhältnisses von Dokumenten angibt, die die Abfrage verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3502">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="cc80c-3503">**\_ dwRatioFinishedNumerator:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Zähler des Verhältnisses von Dokumenten angibt, die die Abfrage verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3503">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="cc80c-3504">**\_ iRowBmk:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die ungefähre Position des Lesezeichens im Rowset in Bezug auf Zeilen angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3504">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="cc80c-3505">**\_ cRowsTotal:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Zeilen im Rowset angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3505">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="cc80c-3506">2.2.3.14 CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-3506">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="cc80c-3507">Die CPMSetBindingsIn-Nachricht fordert die Bindung von Spalten an ein Rowset an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3507">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="cc80c-3508">Der Server antwortet mithilfe des Headerabschnitts der CPMBindingsIn-Nachricht mit den Ergebnissen der Anforderung im Statusfeld auf die Anforderungsnachricht CPMSetBindingsIn. \_</span><span class="sxs-lookup"><span data-stu-id="cc80c-3508">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="cc80c-3509">Das Format der CPMSetBindingsIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3509">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3510">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3510">0</span></span>

<span data-ttu-id="cc80c-3511">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3511">1</span></span>

<span data-ttu-id="cc80c-3512">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3512">2</span></span>

<span data-ttu-id="cc80c-3513">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3513">3</span></span>

<span data-ttu-id="cc80c-3514">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3514">4</span></span>

<span data-ttu-id="cc80c-3515">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3515">5</span></span>

<span data-ttu-id="cc80c-3516">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3516">6</span></span>

<span data-ttu-id="cc80c-3517">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3517">7</span></span>

<span data-ttu-id="cc80c-3518">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3518">8</span></span>

<span data-ttu-id="cc80c-3519">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3519">9</span></span>

<span data-ttu-id="cc80c-3520">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3520">1</span></span><br/> <span data-ttu-id="cc80c-3521">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3521">0</span></span><br/>

<span data-ttu-id="cc80c-3522">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3522">1</span></span>

<span data-ttu-id="cc80c-3523">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3523">2</span></span>

<span data-ttu-id="cc80c-3524">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3524">3</span></span>

<span data-ttu-id="cc80c-3525">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3525">4</span></span>

<span data-ttu-id="cc80c-3526">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3526">5</span></span>

<span data-ttu-id="cc80c-3527">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3527">6</span></span>

<span data-ttu-id="cc80c-3528">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3528">7</span></span>

<span data-ttu-id="cc80c-3529">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3529">8</span></span>

<span data-ttu-id="cc80c-3530">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3530">9</span></span>

<span data-ttu-id="cc80c-3531">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3531">2</span></span><br/> <span data-ttu-id="cc80c-3532">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3532">0</span></span><br/>

<span data-ttu-id="cc80c-3533">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3533">1</span></span>

<span data-ttu-id="cc80c-3534">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3534">2</span></span>

<span data-ttu-id="cc80c-3535">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3535">3</span></span>

<span data-ttu-id="cc80c-3536">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3536">4</span></span>

<span data-ttu-id="cc80c-3537">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3537">5</span></span>

<span data-ttu-id="cc80c-3538">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3538">6</span></span>

<span data-ttu-id="cc80c-3539">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3539">7</span></span>

<span data-ttu-id="cc80c-3540">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3540">8</span></span>

<span data-ttu-id="cc80c-3541">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3541">9</span></span>

<span data-ttu-id="cc80c-3542">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3542">3</span></span><br/> <span data-ttu-id="cc80c-3543">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3543">0</span></span><br/>

<span data-ttu-id="cc80c-3544">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3544">1</span></span>

<span data-ttu-id="cc80c-3545">\_hCursor (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3545">\_hCursor (optional)</span></span>

<span data-ttu-id="cc80c-3546">\_cbRow (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3546">\_cbRow (optional)</span></span>

<span data-ttu-id="cc80c-3547">\_cbBindingDesc (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3547">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="cc80c-3548">\_dummy (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3548">\_dummy (optional)</span></span>

<span data-ttu-id="cc80c-3549">cColumns (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3549">cColumns (optional)</span></span>

<span data-ttu-id="cc80c-3550">aColumns (Variable, optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3550">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="cc80c-3551">**\_ hCursor:** Ein 32-Bit-Wert, der das Handle aus der CPMCreateQueryOut-Nachricht darstellt, die die Zeile identifiziert, für die Bindungen festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3551">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="cc80c-3552">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3552">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cc80c-3553">**\_ cbRow:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe einer Zeile in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3553">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="cc80c-3554">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3554">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cc80c-3555">**\_ cbBindingDesc:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge der Felder nach dem Dummyfeld in Bytes \_ angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3555">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="cc80c-3556">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cc80c-3557">**\_ dummy:** Dieses Feld wird nicht verwendet und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3557">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="cc80c-3558">Sie kann auf einen beliebigen Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3558">It can be set to any arbitrary value.</span></span> <span data-ttu-id="cc80c-3559">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3559">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cc80c-3560">**cColumns:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im Array aColumns angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3560">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="cc80c-3561">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3561">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cc80c-3562">**aColumns:** Ein Array der CTableColumn-Strukturen, das die Spalten einer Zeile im Rowset beschreibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3562">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="cc80c-3563">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3563">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="cc80c-3564">Strukturen im Array MÜSSEN durch 0 bis 3 Auf padding bytes getrennt werden, damit jede Struktur eine 4-Byte-Ausrichtung vom Anfang einer Nachricht hat.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3564">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="cc80c-3565">Solche Auf padding-Bytes können beliebige Werte sein und MÜSSEN beim Empfang ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3565">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="cc80c-3566">2.2.3.15 CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-3566">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="cc80c-3567">Die CPMGetRowsIn-Nachricht fordert Zeilen aus einer Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3567">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="cc80c-3568">Das Format der CPMGetRowsIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3568">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3569">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3569">0</span></span>

<span data-ttu-id="cc80c-3570">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3570">1</span></span>

<span data-ttu-id="cc80c-3571">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3571">2</span></span>

<span data-ttu-id="cc80c-3572">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3572">3</span></span>

<span data-ttu-id="cc80c-3573">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3573">4</span></span>

<span data-ttu-id="cc80c-3574">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3574">5</span></span>

<span data-ttu-id="cc80c-3575">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3575">6</span></span>

<span data-ttu-id="cc80c-3576">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3576">7</span></span>

<span data-ttu-id="cc80c-3577">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3577">8</span></span>

<span data-ttu-id="cc80c-3578">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3578">9</span></span>

<span data-ttu-id="cc80c-3579">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3579">1</span></span><br/> <span data-ttu-id="cc80c-3580">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3580">0</span></span><br/>

<span data-ttu-id="cc80c-3581">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3581">1</span></span>

<span data-ttu-id="cc80c-3582">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3582">2</span></span>

<span data-ttu-id="cc80c-3583">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3583">3</span></span>

<span data-ttu-id="cc80c-3584">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3584">4</span></span>

<span data-ttu-id="cc80c-3585">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3585">5</span></span>

<span data-ttu-id="cc80c-3586">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3586">6</span></span>

<span data-ttu-id="cc80c-3587">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3587">7</span></span>

<span data-ttu-id="cc80c-3588">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3588">8</span></span>

<span data-ttu-id="cc80c-3589">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3589">9</span></span>

<span data-ttu-id="cc80c-3590">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3590">2</span></span><br/> <span data-ttu-id="cc80c-3591">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3591">0</span></span><br/>

<span data-ttu-id="cc80c-3592">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3592">1</span></span>

<span data-ttu-id="cc80c-3593">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3593">2</span></span>

<span data-ttu-id="cc80c-3594">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3594">3</span></span>

<span data-ttu-id="cc80c-3595">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3595">4</span></span>

<span data-ttu-id="cc80c-3596">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3596">5</span></span>

<span data-ttu-id="cc80c-3597">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3597">6</span></span>

<span data-ttu-id="cc80c-3598">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3598">7</span></span>

<span data-ttu-id="cc80c-3599">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3599">8</span></span>

<span data-ttu-id="cc80c-3600">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3600">9</span></span>

<span data-ttu-id="cc80c-3601">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3601">3</span></span><br/> <span data-ttu-id="cc80c-3602">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3602">0</span></span><br/>

<span data-ttu-id="cc80c-3603">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3603">1</span></span>

<span data-ttu-id="cc80c-3604">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cc80c-3604">\_hCursor</span></span>

<span data-ttu-id="cc80c-3605">\_cRowsToTransfer</span><span class="sxs-lookup"><span data-stu-id="cc80c-3605">\_cRowsToTransfer</span></span>

<span data-ttu-id="cc80c-3606">\_cbRowWidth</span><span class="sxs-lookup"><span data-stu-id="cc80c-3606">\_cbRowWidth</span></span>

<span data-ttu-id="cc80c-3607">\_cbSeek</span><span class="sxs-lookup"><span data-stu-id="cc80c-3607">\_cbSeek</span></span>

<span data-ttu-id="cc80c-3608">\_cbReserved</span><span class="sxs-lookup"><span data-stu-id="cc80c-3608">\_cbReserved</span></span>

<span data-ttu-id="cc80c-3609">\_cbReadBuffer</span><span class="sxs-lookup"><span data-stu-id="cc80c-3609">\_cbReadBuffer</span></span>

<span data-ttu-id="cc80c-3610">\_ulClientBase</span><span class="sxs-lookup"><span data-stu-id="cc80c-3610">\_ulClientBase</span></span>

<span data-ttu-id="cc80c-3611">\_fBwdFetch</span><span class="sxs-lookup"><span data-stu-id="cc80c-3611">\_fBwdFetch</span></span>

<span data-ttu-id="cc80c-3612">eType</span><span class="sxs-lookup"><span data-stu-id="cc80c-3612">eType</span></span>

<span data-ttu-id="cc80c-3613">\_chapt</span><span class="sxs-lookup"><span data-stu-id="cc80c-3613">\_chapt</span></span>

<span data-ttu-id="cc80c-3614">SeekDescription</span><span class="sxs-lookup"><span data-stu-id="cc80c-3614">SeekDescription</span></span>

<span data-ttu-id="cc80c-3615">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-3615">...</span></span>

<span data-ttu-id="cc80c-3616">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3616">... (variable)</span></span>



 

<span data-ttu-id="cc80c-3617">**\_ hCursor:** Ein 32-Bit-Wert, der das Handle aus der CPMCreateQueryOut-Nachricht darstellt, die die Abfrage identifiziert, für die Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3617">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="cc80c-3618">**\_ cRowsToTransfer:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die maximale Anzahl von Zeilen angibt, die der Client als Antwort auf diese Nachricht empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3618">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="cc80c-3619">**\_ cbRowWidth:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge einer Zeile in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3619">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="cc80c-3620">**\_ cbSeek:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der Nachricht angibt, die mit eType beginnt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3620">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="cc80c-3621">**\_ cbReserved:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe einer CPMGetRowsOut-Nachricht in Bytes angibt (ohne die Felder Rows und SeekDescriptions).</span><span class="sxs-lookup"><span data-stu-id="cc80c-3621">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="cc80c-3622">Dieser Wert in diesem Feld wird dem Wert des \_ cbSeek-Felds hinzugefügt und dann verwendet, um den Offset des Rows-Felds in der CPMGetRowsOut-Nachricht zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3622">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="cc80c-3623">**\_ cbReadBuffer:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die auf das Maximum des Werts von \_ cbRowWidth oder das 1000-fache des Werts von \_ cRowsToTransfer festgelegt werden MUSS, aufgerundet auf das nächste 512-Byte-Vielfache.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3623">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="cc80c-3624">Der Wert DARF 0x00004000 NICHT überschreiten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3624">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="cc80c-3625">**\_ ulClientBase:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Basiswert angibt, der für Zeigerberechnungen im Zeilenpuffer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3625">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="cc80c-3626">Wenn 64-Bit-Offsets verwendet werden, wird das Feld reserved2 des Nachrichtenheaders als obere 32-Bit-Klasse und \_ ulClientBase als die unteren 32 Bits eines 64-Bit-Werts verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3626">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="cc80c-3627">Weitere Informationen finden Sie in Abschnitt 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3627">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="cc80c-3628">**\_ fBwdFetch:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Reihenfolge angibt, in der die Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3628">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="cc80c-3629">Wenn 0x00000001 festgelegt ist, werden die Zeilen in umgekehrter Reihenfolge abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3629">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="cc80c-3630">Wenn 0x00000000 festgelegt ist, werden die Zeilen in vorwärts gerichteter Reihenfolge abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3630">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="cc80c-3631">DARF NICHT auf andere Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3631">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="cc80c-3632">**eType:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die einen der folgenden Werte enthält, um den Typ des auszuführenden Vorgangs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3632">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="cc80c-3633">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-3633">Value</span></span>                         | <span data-ttu-id="cc80c-3634">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-3634">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="cc80c-3635">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-3635">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="cc80c-3636">SeekDescription enthält eine CRowSeekNext-Struktur.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3636">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="cc80c-3637">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-3637">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="cc80c-3638">SeekDescription enthält eine CRowSeekAt-Struktur.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3638">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="cc80c-3639">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-3639">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="cc80c-3640">SeekDescription enthält eine CRowSeekAtRatio-Struktur.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3640">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="cc80c-3641">eRowSeekByBookmark-0x00000004</span><span class="sxs-lookup"><span data-stu-id="cc80c-3641">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="cc80c-3642">SeekDescription enthält eine CRowSeekByBookmark-Struktur.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3642">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="cc80c-3643">**\_ chapt:** Ein 32-Bit-Wert, der das Handle des Rowset-Kapitels darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3643">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="cc80c-3644">**SeekDescription:** Dieses Feld MUSS eine Struktur des Typs enthalten, der durch den eType-Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3644">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="cc80c-3645">2.2.3.16 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-3645">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="cc80c-3646">Die CPMGetRowsOut-Nachricht antwortet auf eine CPMGetRowsIn-Nachricht mit den Zeilen einer Abfrage.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3646">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="cc80c-3647">Server MÜSSEN Offsets wie folgt in Datentypen variabler Länge im Feld Zeilen formatieren:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3647">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="cc80c-3648">Client hat angegeben, dass es sich um ein 32-Bit-System handelt (0x00000008 oder weniger im iClientVersion-Feld von CPMConnectIn): Offsets sind 32-Bit-Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3648">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="cc80c-3649">Der Client hat angegeben, dass es sich um ein 64-Bit-System handelt ( iClientVersion > 0x00000008 in CPMConnectIn), und server gibt an, dass es sich um ein \_ 32-Bit-System handelt ( serverVersion auf \_ 0x00000007 in CPMConnectOut festgelegt): Offsets sind 32-Bit-Ganzzahlen</span><span class="sxs-lookup"><span data-stu-id="cc80c-3649">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="cc80c-3650">Der Client hat angegeben, dass es sich um ein 64-Bit-System handelt ( iClientVersion > 0x00000008 in CPMConnectIn), und der Server hat angegeben, dass es sich um ein \_ 64-Bit-System handelt ( serverVersion auf \_ 0x00010007 in CPMConnectOut festgelegt): Offsets sind 64-Bit-Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3650">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="cc80c-3651">Das Format der CPMGetRowsOut-Nachricht, die auf den Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3651">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3652">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3652">0</span></span>

<span data-ttu-id="cc80c-3653">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3653">1</span></span>

<span data-ttu-id="cc80c-3654">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3654">2</span></span>

<span data-ttu-id="cc80c-3655">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3655">3</span></span>

<span data-ttu-id="cc80c-3656">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3656">4</span></span>

<span data-ttu-id="cc80c-3657">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3657">5</span></span>

<span data-ttu-id="cc80c-3658">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3658">6</span></span>

<span data-ttu-id="cc80c-3659">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3659">7</span></span>

<span data-ttu-id="cc80c-3660">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3660">8</span></span>

<span data-ttu-id="cc80c-3661">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3661">9</span></span>

<span data-ttu-id="cc80c-3662">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3662">1</span></span><br/> <span data-ttu-id="cc80c-3663">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3663">0</span></span><br/>

<span data-ttu-id="cc80c-3664">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3664">1</span></span>

<span data-ttu-id="cc80c-3665">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3665">2</span></span>

<span data-ttu-id="cc80c-3666">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3666">3</span></span>

<span data-ttu-id="cc80c-3667">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3667">4</span></span>

<span data-ttu-id="cc80c-3668">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3668">5</span></span>

<span data-ttu-id="cc80c-3669">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3669">6</span></span>

<span data-ttu-id="cc80c-3670">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3670">7</span></span>

<span data-ttu-id="cc80c-3671">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3671">8</span></span>

<span data-ttu-id="cc80c-3672">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3672">9</span></span>

<span data-ttu-id="cc80c-3673">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3673">2</span></span><br/> <span data-ttu-id="cc80c-3674">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3674">0</span></span><br/>

<span data-ttu-id="cc80c-3675">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3675">1</span></span>

<span data-ttu-id="cc80c-3676">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3676">2</span></span>

<span data-ttu-id="cc80c-3677">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3677">3</span></span>

<span data-ttu-id="cc80c-3678">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3678">4</span></span>

<span data-ttu-id="cc80c-3679">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3679">5</span></span>

<span data-ttu-id="cc80c-3680">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3680">6</span></span>

<span data-ttu-id="cc80c-3681">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3681">7</span></span>

<span data-ttu-id="cc80c-3682">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3682">8</span></span>

<span data-ttu-id="cc80c-3683">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3683">9</span></span>

<span data-ttu-id="cc80c-3684">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3684">3</span></span><br/> <span data-ttu-id="cc80c-3685">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3685">0</span></span><br/>

<span data-ttu-id="cc80c-3686">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3686">1</span></span>

<span data-ttu-id="cc80c-3687">\_cRowsReturned</span><span class="sxs-lookup"><span data-stu-id="cc80c-3687">\_cRowsReturned</span></span>

<span data-ttu-id="cc80c-3688">eType</span><span class="sxs-lookup"><span data-stu-id="cc80c-3688">eType</span></span>

<span data-ttu-id="cc80c-3689">\_chapt</span><span class="sxs-lookup"><span data-stu-id="cc80c-3689">\_chapt</span></span>

<span data-ttu-id="cc80c-3690">SeekDescription (optional, Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3690">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="cc80c-3691">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-3691">...</span></span>

<span data-ttu-id="cc80c-3692">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-3692">...</span></span>

<span data-ttu-id="cc80c-3693">paddingRows (optional, variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3693">paddingRows (optional, variable)</span></span>

<span data-ttu-id="cc80c-3694">Zeilen</span><span class="sxs-lookup"><span data-stu-id="cc80c-3694">Rows</span></span>



 

<span data-ttu-id="cc80c-3695">**\_ cRowsReturned:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der in Zeilen zurückgegebenen Zeilen angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3695">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="cc80c-3696">**eType:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die einen der folgenden Werte enthält, um den Typ des rowseek-Vorgangs anzugeben, der durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3696">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="cc80c-3697">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-3697">Value</span></span>                         | <span data-ttu-id="cc80c-3698">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-3698">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="cc80c-3699">eRowsSeekNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-3699">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="cc80c-3700">Keine SeekDescription, SeekDescription-Feld ignorieren.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3700">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="cc80c-3701">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-3701">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="cc80c-3702">SeekDescription enthält eine CRowSeekNext-Struktur.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3702">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="cc80c-3703">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-3703">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="cc80c-3704">SeekDescription enthält eine CRowSeekAt-Struktur.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3704">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="cc80c-3705">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-3705">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="cc80c-3706">SeekDescription enthält eine CRowSeekAtRatio-Struktur.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3706">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="cc80c-3707">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cc80c-3707">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="cc80c-3708">SeekDescription enthält eine CRowSeekByBookmark-Struktur.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3708">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="cc80c-3709">**\_ chapt:** Ein 32-Bit-Wert, der das Handle des Rowsetkapitels darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3709">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="cc80c-3710">**SeekDescription:** Dieses Feld MUSS eine Struktur des Typs enthalten, der durch das eType-Feld angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3710">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="cc80c-3711">**paddingRows:** Dieses Feld MUSS eine ausreichende Länge (0 bis \_ cbReserved-1 Bytes) aufweisen, um das Rows-Feld \_ auf cbReserved offset vom Anfang einer Nachricht aufzufüllen, wobei \_ cbReserved der Wert in der CPMGetRowsIn-Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3711">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="cc80c-3712">Das Auffüllen von Bytes, die in diesem Feld verwendet werden, kann ein beliebiger Wert sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3712">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="cc80c-3713">Dieses Feld MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3713">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cc80c-3714">**Zeilen:** Zeilendaten werden gemäß den Spalteninformationen in der neuesten CPMSetBindingsIn-Nachricht formatiert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3714">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="cc80c-3715">Zeilen MÜSSEN in vorwärts gerichteter Reihenfolge gespeichert werden (z. B. Zeile 1 vor Zeile 2).</span><span class="sxs-lookup"><span data-stu-id="cc80c-3715">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="cc80c-3716">Spalten fester Größe MÜSSEN an den Offsets gespeichert werden, die durch die neueste CPMSetBindingsIn-Nachricht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3716">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="cc80c-3717">Spalten variabler Größe (z. B. Zeichenfolgen) MÜSSEN wie folgt gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3717">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="cc80c-3718">Die Variablendaten selbst (z. B. die Zeichenfolge) werden am Ende des Puffers in absteigender Reihenfolge gespeichert (z. B. die Auflistung aller Variablendaten für Zeile 1 befindet sich am Ende, Zeile 2 am nächsten usw.).</span><span class="sxs-lookup"><span data-stu-id="cc80c-3718">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="cc80c-3719">Der Bereich mit fester Größe (am Anfang des Zeilenpuffers) MUSS eine CRowVariant für jede Spalte enthalten, die an dem Offset gespeichert ist, der in der letzten CPMSetBindingsIn-Nachricht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3719">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="cc80c-3720">vType MUSS den Datentyp enthalten (z.B. VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="cc80c-3720">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="cc80c-3721">Wenn, wie durch die Regeln am Anfang dieses Abschnitts festgelegt, 32-Bit-Offsets verwendet werden, muss das Feld Offset in CRowVariant einen 32-Bit-Wert enthalten, der den Offset der Variablendaten vom Anfang der CPMGetRowsOut-Nachricht sowie den Wert von ulClientBase enthält, der in der letzten \_ CPMGetRowsIn-Nachricht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3721">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="cc80c-3722">Wenn 64-Bit-Offsets verwendet werden, muss das Feld Offset in CRowVariant einen 64-Bit-Wert enthalten, der der Offset vom Anfang der CPMGetRowsOut-Nachricht ist, der einem 64-Bit-Wert hinzugefügt wird, der mithilfe von ulClientBase als niedriger \_ 32-Bit-Wert und ulReserved2 als hohe \_ 32-Bit-Werte zusammengesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3722">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="cc80c-3723">Wenn in der CPMSetBindingsIn-Nachricht beispielsweise zwei Spalten angegeben wurden: Größe (VT \_ I4) und Titel (VT \_ LPWSTR) und ulClientBase von CPMGetRowsIn 0x10000 dann würden zwei Zeilen wie folgt \_ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3723">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="cc80c-3724">Der grau markierte Abschnitt ist der Teil mit fester Länge des Puffers.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3724">The section marked in grey is the fixed-length part of the buffer.</span></span>

![Beispiel für eine cpmsetbindingsin-Nachricht](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="cc80c-3726">2.2.3.17 CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-3726">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="cc80c-3727">Die CPMRatioFinishedIn-Nachricht fordert den Abschlussprozentsatz einer Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3727">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="cc80c-3728">Das Format der CPMRatioFinishedIn-Nachricht, die dem Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3728">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3729">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3729">0</span></span>

<span data-ttu-id="cc80c-3730">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3730">1</span></span>

<span data-ttu-id="cc80c-3731">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3731">2</span></span>

<span data-ttu-id="cc80c-3732">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3732">3</span></span>

<span data-ttu-id="cc80c-3733">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3733">4</span></span>

<span data-ttu-id="cc80c-3734">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3734">5</span></span>

<span data-ttu-id="cc80c-3735">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3735">6</span></span>

<span data-ttu-id="cc80c-3736">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3736">7</span></span>

<span data-ttu-id="cc80c-3737">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3737">8</span></span>

<span data-ttu-id="cc80c-3738">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3738">9</span></span>

<span data-ttu-id="cc80c-3739">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3739">1</span></span><br/> <span data-ttu-id="cc80c-3740">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3740">0</span></span><br/>

<span data-ttu-id="cc80c-3741">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3741">1</span></span>

<span data-ttu-id="cc80c-3742">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3742">2</span></span>

<span data-ttu-id="cc80c-3743">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3743">3</span></span>

<span data-ttu-id="cc80c-3744">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3744">4</span></span>

<span data-ttu-id="cc80c-3745">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3745">5</span></span>

<span data-ttu-id="cc80c-3746">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3746">6</span></span>

<span data-ttu-id="cc80c-3747">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3747">7</span></span>

<span data-ttu-id="cc80c-3748">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3748">8</span></span>

<span data-ttu-id="cc80c-3749">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3749">9</span></span>

<span data-ttu-id="cc80c-3750">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3750">2</span></span><br/> <span data-ttu-id="cc80c-3751">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3751">0</span></span><br/>

<span data-ttu-id="cc80c-3752">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3752">1</span></span>

<span data-ttu-id="cc80c-3753">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3753">2</span></span>

<span data-ttu-id="cc80c-3754">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3754">3</span></span>

<span data-ttu-id="cc80c-3755">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3755">4</span></span>

<span data-ttu-id="cc80c-3756">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3756">5</span></span>

<span data-ttu-id="cc80c-3757">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3757">6</span></span>

<span data-ttu-id="cc80c-3758">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3758">7</span></span>

<span data-ttu-id="cc80c-3759">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3759">8</span></span>

<span data-ttu-id="cc80c-3760">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3760">9</span></span>

<span data-ttu-id="cc80c-3761">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3761">3</span></span><br/> <span data-ttu-id="cc80c-3762">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3762">0</span></span><br/>

<span data-ttu-id="cc80c-3763">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3763">1</span></span>

<span data-ttu-id="cc80c-3764">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cc80c-3764">\_hCursor</span></span>

<span data-ttu-id="cc80c-3765">\_fQuick</span><span class="sxs-lookup"><span data-stu-id="cc80c-3765">\_fQuick</span></span>



 

<span data-ttu-id="cc80c-3766">**\_ hCursor:** Das Handle aus der CPMCreateQueryOut-Nachricht, das die Abfrage identifiziert, für die Abschlussinformationen anfordern werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3766">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="cc80c-3767">**\_ fQuick:** MUSS auf "0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3767">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="cc80c-3768">Nicht verwendet und MÜSSEN vom Server ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3768">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="cc80c-3769">2.2.3.18 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-3769">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="cc80c-3770">Die CPMRatioFinishedOut-Nachricht antwortet auf eine CPMRatioFinishedIn-Nachricht mit dem Vervollständigungsverhältnis einer Abfrage.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3770">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="cc80c-3771">Das Format der CPMRatioFinishedOut-Nachricht, die dem Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3771">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3772">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3772">0</span></span>

<span data-ttu-id="cc80c-3773">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3773">1</span></span>

<span data-ttu-id="cc80c-3774">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3774">2</span></span>

<span data-ttu-id="cc80c-3775">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3775">3</span></span>

<span data-ttu-id="cc80c-3776">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3776">4</span></span>

<span data-ttu-id="cc80c-3777">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3777">5</span></span>

<span data-ttu-id="cc80c-3778">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3778">6</span></span>

<span data-ttu-id="cc80c-3779">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3779">7</span></span>

<span data-ttu-id="cc80c-3780">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3780">8</span></span>

<span data-ttu-id="cc80c-3781">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3781">9</span></span>

<span data-ttu-id="cc80c-3782">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3782">1</span></span><br/> <span data-ttu-id="cc80c-3783">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3783">0</span></span><br/>

<span data-ttu-id="cc80c-3784">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3784">1</span></span>

<span data-ttu-id="cc80c-3785">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3785">2</span></span>

<span data-ttu-id="cc80c-3786">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3786">3</span></span>

<span data-ttu-id="cc80c-3787">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3787">4</span></span>

<span data-ttu-id="cc80c-3788">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3788">5</span></span>

<span data-ttu-id="cc80c-3789">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3789">6</span></span>

<span data-ttu-id="cc80c-3790">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3790">7</span></span>

<span data-ttu-id="cc80c-3791">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3791">8</span></span>

<span data-ttu-id="cc80c-3792">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3792">9</span></span>

<span data-ttu-id="cc80c-3793">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3793">2</span></span><br/> <span data-ttu-id="cc80c-3794">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3794">0</span></span><br/>

<span data-ttu-id="cc80c-3795">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3795">1</span></span>

<span data-ttu-id="cc80c-3796">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3796">2</span></span>

<span data-ttu-id="cc80c-3797">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3797">3</span></span>

<span data-ttu-id="cc80c-3798">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3798">4</span></span>

<span data-ttu-id="cc80c-3799">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3799">5</span></span>

<span data-ttu-id="cc80c-3800">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3800">6</span></span>

<span data-ttu-id="cc80c-3801">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3801">7</span></span>

<span data-ttu-id="cc80c-3802">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3802">8</span></span>

<span data-ttu-id="cc80c-3803">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3803">9</span></span>

<span data-ttu-id="cc80c-3804">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3804">3</span></span><br/> <span data-ttu-id="cc80c-3805">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3805">0</span></span><br/>

<span data-ttu-id="cc80c-3806">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3806">1</span></span>

<span data-ttu-id="cc80c-3807">\_ ulNumerator</span><span class="sxs-lookup"><span data-stu-id="cc80c-3807">\_ ulNumerator</span></span>

<span data-ttu-id="cc80c-3808">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="cc80c-3808">\_ulDenominator</span></span>

<span data-ttu-id="cc80c-3809">\_Krähen</span><span class="sxs-lookup"><span data-stu-id="cc80c-3809">\_cRows</span></span>

<span data-ttu-id="cc80c-3810">\_fNewRows</span><span class="sxs-lookup"><span data-stu-id="cc80c-3810">\_fNewRows</span></span>



 

<span data-ttu-id="cc80c-3811">**\_ ulNumerator:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Zähler des Vervollständigungsverhältnisses in Bezug auf Zeilen angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3811">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="cc80c-3812">**\_ ulDenominator:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Nenner des Vervollständigungsverhältnisses in Bezug auf Zeilen angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3812">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="cc80c-3813">MUSS größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3813">MUST be greater than zero.</span></span>

<span data-ttu-id="cc80c-3814">**\_ cRows:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Zeilen für die Abfrage angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3814">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="cc80c-3815">**\_ fNewRows:** Ein boolescher Wert, der angibt, ob neue Zeilen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3815">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="cc80c-3816">Der Wert 0x00000001 gibt an, dass neue Zeilen im Rowset verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3816">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="cc80c-3817">Der Wert 0x00000000 gibt an, dass das Rowset keine neuen Zeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3817">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="cc80c-3818">Dieses Feld DARF NICHT auf andere Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3818">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="cc80c-3819">2.2.3.19 CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-3819">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="cc80c-3820">Die CPMFetchValueIn-Nachricht fordert einen Eigenschaftswert an, der für die Rückgabe in einem Rowset zu groß war.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3820">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="cc80c-3821">Wie in Abschnitt 3.2.4.2.5 angegeben, wird diese Meldung wiederholt gesendet, um alle Bytes der Eigenschaft abzurufen, wobei \_ cbSoFar für jede aktualisiert wird, bis das \_ fMoreExists-Feld der CPMFetchValueOut-Nachricht auf **FALSE** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3821">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="cc80c-3822">Das Format der CPMFetchValueIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3822">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3823">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3823">0</span></span>

<span data-ttu-id="cc80c-3824">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3824">1</span></span>

<span data-ttu-id="cc80c-3825">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3825">2</span></span>

<span data-ttu-id="cc80c-3826">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3826">3</span></span>

<span data-ttu-id="cc80c-3827">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3827">4</span></span>

<span data-ttu-id="cc80c-3828">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3828">5</span></span>

<span data-ttu-id="cc80c-3829">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3829">6</span></span>

<span data-ttu-id="cc80c-3830">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3830">7</span></span>

<span data-ttu-id="cc80c-3831">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3831">8</span></span>

<span data-ttu-id="cc80c-3832">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3832">9</span></span>

<span data-ttu-id="cc80c-3833">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3833">1</span></span><br/> <span data-ttu-id="cc80c-3834">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3834">0</span></span><br/>

<span data-ttu-id="cc80c-3835">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3835">1</span></span>

<span data-ttu-id="cc80c-3836">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3836">2</span></span>

<span data-ttu-id="cc80c-3837">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3837">3</span></span>

<span data-ttu-id="cc80c-3838">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3838">4</span></span>

<span data-ttu-id="cc80c-3839">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3839">5</span></span>

<span data-ttu-id="cc80c-3840">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3840">6</span></span>

<span data-ttu-id="cc80c-3841">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3841">7</span></span>

<span data-ttu-id="cc80c-3842">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3842">8</span></span>

<span data-ttu-id="cc80c-3843">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3843">9</span></span>

<span data-ttu-id="cc80c-3844">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3844">2</span></span><br/> <span data-ttu-id="cc80c-3845">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3845">0</span></span><br/>

<span data-ttu-id="cc80c-3846">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3846">1</span></span>

<span data-ttu-id="cc80c-3847">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3847">2</span></span>

<span data-ttu-id="cc80c-3848">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3848">3</span></span>

<span data-ttu-id="cc80c-3849">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3849">4</span></span>

<span data-ttu-id="cc80c-3850">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3850">5</span></span>

<span data-ttu-id="cc80c-3851">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3851">6</span></span>

<span data-ttu-id="cc80c-3852">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3852">7</span></span>

<span data-ttu-id="cc80c-3853">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3853">8</span></span>

<span data-ttu-id="cc80c-3854">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3854">9</span></span>

<span data-ttu-id="cc80c-3855">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3855">3</span></span><br/> <span data-ttu-id="cc80c-3856">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3856">0</span></span><br/>

<span data-ttu-id="cc80c-3857">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3857">1</span></span>

<span data-ttu-id="cc80c-3858">\_Wid</span><span class="sxs-lookup"><span data-stu-id="cc80c-3858">\_wid</span></span>

<span data-ttu-id="cc80c-3859">\_cbSoFar</span><span class="sxs-lookup"><span data-stu-id="cc80c-3859">\_cbSoFar</span></span>

<span data-ttu-id="cc80c-3860">\_cbPropSpec</span><span class="sxs-lookup"><span data-stu-id="cc80c-3860">\_cbPropSpec</span></span>

<span data-ttu-id="cc80c-3861">\_cbChunk</span><span class="sxs-lookup"><span data-stu-id="cc80c-3861">\_cbChunk</span></span>

<span data-ttu-id="cc80c-3862">PropSpec (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3862">PropSpec (variable)</span></span>

<span data-ttu-id="cc80c-3863">...</span><span class="sxs-lookup"><span data-stu-id="cc80c-3863">...</span></span>

<span data-ttu-id="cc80c-3864">\_Auffüllen (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3864">\_padding (variable)</span></span>



 

<span data-ttu-id="cc80c-3865">**\_ wid:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die Informationen zur Dokument-ID enthält, die das Dokument identifiziert, für das eine Eigenschaft abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3865">**\_wid**: A 32-bit unsigned integer containing information about the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="cc80c-3866">**\_ cbSoFar:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der zuvor für diese Eigenschaft übertragenen Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3866">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="cc80c-3867">MUSS auf die 0x00000000 in der ersten Nachricht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3867">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="cc80c-3868">**\_ cbPropSpec:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des PropSpec-Felds in Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3868">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="cc80c-3869">**\_ cbChunk:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die maximale Anzahl von Bytes enthält, die der Absender in einer CPMFetchValueOut-Nachricht akzeptieren kann.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3869">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="cc80c-3870">*Windows-Verhalten: Dieses Feld ist auf 0x00004000 windows-Versionen festgelegt.*</span><span class="sxs-lookup"><span data-stu-id="cc80c-3870">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="cc80c-3871">**PropSpec:** Eine CFullPropSpec-Struktur, die die abzurufende Eigenschaft an gibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3871">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="cc80c-3872">**\_ Padding**: Dieses Feld MUSS die erforderliche Länge (0 bis 3 Bytes) haben, um die Nachricht auf ein Vielfaches von 4 Bytes zu aufpaddieren.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3872">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="cc80c-3873">Der Wert der Auf padding-Bytes kann ein beliebiger Wert sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3873">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="cc80c-3874">Dieses Feld MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3874">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="cc80c-3875">2.2.3.20 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-3875">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="cc80c-3876">Die CPMFetchValueOut-Nachricht antwortet auf eine CPMFetchValueIn-Nachricht mit einem Eigenschaftswert aus einer vorherigen Abfrage.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3876">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="cc80c-3877">Wie in Abschnitt 3.1.5.2.8 angegeben, wird diese Nachricht nach jeder CPMFetchValueIn-Nachricht gesendet, bis alle Bytes der Eigenschaft übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3877">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="cc80c-3878">Das Format der CPMFetchValueOut-Nachricht, die auf den Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3878">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3879">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3879">0</span></span>

<span data-ttu-id="cc80c-3880">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3880">1</span></span>

<span data-ttu-id="cc80c-3881">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3881">2</span></span>

<span data-ttu-id="cc80c-3882">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3882">3</span></span>

<span data-ttu-id="cc80c-3883">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3883">4</span></span>

<span data-ttu-id="cc80c-3884">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3884">5</span></span>

<span data-ttu-id="cc80c-3885">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3885">6</span></span>

<span data-ttu-id="cc80c-3886">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3886">7</span></span>

<span data-ttu-id="cc80c-3887">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3887">8</span></span>

<span data-ttu-id="cc80c-3888">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3888">9</span></span>

<span data-ttu-id="cc80c-3889">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3889">1</span></span><br/> <span data-ttu-id="cc80c-3890">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3890">0</span></span><br/>

<span data-ttu-id="cc80c-3891">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3891">1</span></span>

<span data-ttu-id="cc80c-3892">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3892">2</span></span>

<span data-ttu-id="cc80c-3893">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3893">3</span></span>

<span data-ttu-id="cc80c-3894">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3894">4</span></span>

<span data-ttu-id="cc80c-3895">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3895">5</span></span>

<span data-ttu-id="cc80c-3896">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3896">6</span></span>

<span data-ttu-id="cc80c-3897">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3897">7</span></span>

<span data-ttu-id="cc80c-3898">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3898">8</span></span>

<span data-ttu-id="cc80c-3899">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3899">9</span></span>

<span data-ttu-id="cc80c-3900">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3900">2</span></span><br/> <span data-ttu-id="cc80c-3901">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3901">0</span></span><br/>

<span data-ttu-id="cc80c-3902">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3902">1</span></span>

<span data-ttu-id="cc80c-3903">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3903">2</span></span>

<span data-ttu-id="cc80c-3904">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3904">3</span></span>

<span data-ttu-id="cc80c-3905">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3905">4</span></span>

<span data-ttu-id="cc80c-3906">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3906">5</span></span>

<span data-ttu-id="cc80c-3907">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3907">6</span></span>

<span data-ttu-id="cc80c-3908">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3908">7</span></span>

<span data-ttu-id="cc80c-3909">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3909">8</span></span>

<span data-ttu-id="cc80c-3910">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3910">9</span></span>

<span data-ttu-id="cc80c-3911">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3911">3</span></span><br/> <span data-ttu-id="cc80c-3912">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3912">0</span></span><br/>

<span data-ttu-id="cc80c-3913">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3913">1</span></span>

<span data-ttu-id="cc80c-3914">\_cbValue</span><span class="sxs-lookup"><span data-stu-id="cc80c-3914">\_cbValue</span></span>

<span data-ttu-id="cc80c-3915">\_fMoreExists</span><span class="sxs-lookup"><span data-stu-id="cc80c-3915">\_fMoreExists</span></span>

<span data-ttu-id="cc80c-3916">\_fValueExists</span><span class="sxs-lookup"><span data-stu-id="cc80c-3916">\_fValueExists</span></span>

<span data-ttu-id="cc80c-3917">vType</span><span class="sxs-lookup"><span data-stu-id="cc80c-3917">vType</span></span>

<span data-ttu-id="cc80c-3918">vValue (Variable)</span><span class="sxs-lookup"><span data-stu-id="cc80c-3918">vValue (variable)</span></span>



 

<span data-ttu-id="cc80c-3919">**\_ cbValue:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtgröße in Byte in vValue enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3919">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="cc80c-3920">**\_ fMoreExists:** Ein boolescher Wert, der angibt, ob zusätzliche CPMFetchValueOut-Nachrichten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3920">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="cc80c-3921">Wenn 0x00000001 festgelegt ist, gibt es zusätzliche CPMFetchValueOut-Meldungen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3921">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="cc80c-3922">Wenn 0x00000000 festgelegt ist, sind keine zusätzlichen CPMFetchValueOut-Meldungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3922">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="cc80c-3923">**\_ fValueExists:** Ein boolescher Wert, der angibt, ob ein Wert für die Eigenschaft vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3923">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="cc80c-3924">Wenn 0x00000001 festgelegt ist, ist ein Wert für die Eigenschaft vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3924">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="cc80c-3925">Wenn auf 0x00000000 festgelegt ist, ist kein Wert für die Eigenschaft vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3925">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="cc80c-3926">**vType:** Ein Wert aus der VARENUM-Enumeration. Ausführliche Informationen zum Typ der Eigenschaft finden Sie in Abschnitt 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3926">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="cc80c-3927">**vValue:** Ein Teil eines Bytearrays, der eine SERIALIZEDPROPERTYVALUE-Struktur enthält, wie in Abschnitt 2.2.1.32 angegeben, wobei der Offset des Anfangs des Teils der Wert von \_ cbSoFar in CPMFetchValueIn ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3927">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="cc80c-3928">Die Länge des durch das cbValue-Feld angegebenen Teils \_ MUSS dem Wert von \_ cbChunk in CPMFetchValueIn entsprechen, wenn \_ fMoreExists auf 0x00000001 festgelegt ist, und MUSS andernfalls kleiner oder gleich dem Wert von \_ cbChunk sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3928">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="cc80c-3929">2.2.3.21 CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="cc80c-3929">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="cc80c-3930">Die CPMGetNotify-Nachricht fordert an, dass der Client über Rowsetänderungen benachrichtigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3930">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="cc80c-3931">Die Nachricht DARF KEINEN Text enthalten. nur der In Abschnitt 2.2.2 angegebene Nachrichtenheader muss gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3931">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="cc80c-3932">2.2.3.22 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-3932">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="cc80c-3933">Die CPMSendNotifyOut-Nachricht benachrichtigt den Client über eine Änderung an den Ergebnissen einer Abfrage.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3933">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="cc80c-3934">Diese Meldung wird nur gesendet, wenn eine Änderung auftritt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3934">This message is only sent when a change occurs.</span></span> <span data-ttu-id="cc80c-3935">Das Format der CPMSendNotifyOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3935">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3936">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3936">0</span></span>

<span data-ttu-id="cc80c-3937">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3937">1</span></span>

<span data-ttu-id="cc80c-3938">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3938">2</span></span>

<span data-ttu-id="cc80c-3939">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3939">3</span></span>

<span data-ttu-id="cc80c-3940">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3940">4</span></span>

<span data-ttu-id="cc80c-3941">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3941">5</span></span>

<span data-ttu-id="cc80c-3942">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3942">6</span></span>

<span data-ttu-id="cc80c-3943">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3943">7</span></span>

<span data-ttu-id="cc80c-3944">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3944">8</span></span>

<span data-ttu-id="cc80c-3945">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3945">9</span></span>

<span data-ttu-id="cc80c-3946">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3946">1</span></span><br/> <span data-ttu-id="cc80c-3947">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3947">0</span></span><br/>

<span data-ttu-id="cc80c-3948">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3948">1</span></span>

<span data-ttu-id="cc80c-3949">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3949">2</span></span>

<span data-ttu-id="cc80c-3950">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3950">3</span></span>

<span data-ttu-id="cc80c-3951">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3951">4</span></span>

<span data-ttu-id="cc80c-3952">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3952">5</span></span>

<span data-ttu-id="cc80c-3953">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3953">6</span></span>

<span data-ttu-id="cc80c-3954">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3954">7</span></span>

<span data-ttu-id="cc80c-3955">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3955">8</span></span>

<span data-ttu-id="cc80c-3956">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3956">9</span></span>

<span data-ttu-id="cc80c-3957">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3957">2</span></span><br/> <span data-ttu-id="cc80c-3958">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3958">0</span></span><br/>

<span data-ttu-id="cc80c-3959">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3959">1</span></span>

<span data-ttu-id="cc80c-3960">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3960">2</span></span>

<span data-ttu-id="cc80c-3961">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3961">3</span></span>

<span data-ttu-id="cc80c-3962">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3962">4</span></span>

<span data-ttu-id="cc80c-3963">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3963">5</span></span>

<span data-ttu-id="cc80c-3964">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3964">6</span></span>

<span data-ttu-id="cc80c-3965">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3965">7</span></span>

<span data-ttu-id="cc80c-3966">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3966">8</span></span>

<span data-ttu-id="cc80c-3967">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3967">9</span></span>

<span data-ttu-id="cc80c-3968">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3968">3</span></span><br/> <span data-ttu-id="cc80c-3969">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3969">0</span></span><br/>

<span data-ttu-id="cc80c-3970">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3970">1</span></span>

<span data-ttu-id="cc80c-3971">\_watchNotify</span><span class="sxs-lookup"><span data-stu-id="cc80c-3971">\_watchNotify</span></span>



 

<span data-ttu-id="cc80c-3972">**\_ watchNotify:** Die Änderung an der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3972">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="cc80c-3973">Es MUSS einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3973">It MUST be one of the following values:</span></span>



| <span data-ttu-id="cc80c-3974">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-3974">Value</span></span>                                     | <span data-ttu-id="cc80c-3975">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-3975">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="cc80c-3976">DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-3976">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="cc80c-3977">Die Anzahl der Zeilen im Abfragerowset hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3977">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="cc80c-3978">DBWATCHNOTIFY \_ QUERYDONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-3978">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="cc80c-3979">Die Abfrage wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3979">The query has completed.</span></span>                            |
| <span data-ttu-id="cc80c-3980">DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-3980">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="cc80c-3981">Die Abfrage wurde erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3981">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="cc80c-3982">2.2.3.23 CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-3982">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="cc80c-3983">Die CPMGetApproximatePositionIn-Nachricht fordert die ungefähre Position eines Lesezeichens in einem Kapitel an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-3983">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="cc80c-3984">Das Format der CPMGetApproximatePositionIn-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="cc80c-3984">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="cc80c-3985">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3985">0</span></span>

<span data-ttu-id="cc80c-3986">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3986">1</span></span>

<span data-ttu-id="cc80c-3987">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3987">2</span></span>

<span data-ttu-id="cc80c-3988">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3988">3</span></span>

<span data-ttu-id="cc80c-3989">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-3989">4</span></span>

<span data-ttu-id="cc80c-3990">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-3990">5</span></span>

<span data-ttu-id="cc80c-3991">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-3991">6</span></span>

<span data-ttu-id="cc80c-3992">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-3992">7</span></span>

<span data-ttu-id="cc80c-3993">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-3993">8</span></span>

<span data-ttu-id="cc80c-3994">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-3994">9</span></span>

<span data-ttu-id="cc80c-3995">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3995">1</span></span><br/> <span data-ttu-id="cc80c-3996">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-3996">0</span></span><br/>

<span data-ttu-id="cc80c-3997">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-3997">1</span></span>

<span data-ttu-id="cc80c-3998">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-3998">2</span></span>

<span data-ttu-id="cc80c-3999">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-3999">3</span></span>

<span data-ttu-id="cc80c-4000">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4000">4</span></span>

<span data-ttu-id="cc80c-4001">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4001">5</span></span>

<span data-ttu-id="cc80c-4002">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4002">6</span></span>

<span data-ttu-id="cc80c-4003">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4003">7</span></span>

<span data-ttu-id="cc80c-4004">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4004">8</span></span>

<span data-ttu-id="cc80c-4005">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4005">9</span></span>

<span data-ttu-id="cc80c-4006">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4006">2</span></span><br/> <span data-ttu-id="cc80c-4007">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4007">0</span></span><br/>

<span data-ttu-id="cc80c-4008">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4008">1</span></span>

<span data-ttu-id="cc80c-4009">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4009">2</span></span>

<span data-ttu-id="cc80c-4010">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4010">3</span></span>

<span data-ttu-id="cc80c-4011">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4011">4</span></span>

<span data-ttu-id="cc80c-4012">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4012">5</span></span>

<span data-ttu-id="cc80c-4013">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4013">6</span></span>

<span data-ttu-id="cc80c-4014">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4014">7</span></span>

<span data-ttu-id="cc80c-4015">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4015">8</span></span>

<span data-ttu-id="cc80c-4016">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4016">9</span></span>

<span data-ttu-id="cc80c-4017">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4017">3</span></span><br/> <span data-ttu-id="cc80c-4018">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4018">0</span></span><br/>

<span data-ttu-id="cc80c-4019">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4019">1</span></span>

<span data-ttu-id="cc80c-4020">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cc80c-4020">\_hCursor</span></span>

<span data-ttu-id="cc80c-4021">\_chapt</span><span class="sxs-lookup"><span data-stu-id="cc80c-4021">\_chapt</span></span>

<span data-ttu-id="cc80c-4022">\_bmk</span><span class="sxs-lookup"><span data-stu-id="cc80c-4022">\_bmk</span></span>



 

<span data-ttu-id="cc80c-4023">**\_ hCursor:** Ein 32-Bit-Wert, der den Abfragecursor darstellt, der von CPMCreateQueryOut für das Rowset mit dem Lesezeichen erhalten wurde.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4023">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="cc80c-4024">**\_ chapt:** Ein 32-Bit-Wert, der das Handle für das Kapitel darstellt, das das Lesezeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4024">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="cc80c-4025">**\_ bmk:** Ein 32-Bit-Wert, der das Handle für das Lesezeichen darstellt, für das die ungefähre Position abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4025">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="cc80c-4026">2.2.3.24 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-4026">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="cc80c-4027">Die CPMGetApproximatePositionOut-Nachricht antwortet auf eine CPMGetApproximatePositionIn-Nachricht, die die ungefähre Position des Lesezeichens im Kapitel beschreibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4027">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="cc80c-4028">Das Format der CPMGetApproximatePositionOut-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4028">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="cc80c-4029">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4029">0</span></span>

<span data-ttu-id="cc80c-4030">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4030">1</span></span>

<span data-ttu-id="cc80c-4031">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4031">2</span></span>

<span data-ttu-id="cc80c-4032">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4032">3</span></span>

<span data-ttu-id="cc80c-4033">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4033">4</span></span>

<span data-ttu-id="cc80c-4034">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4034">5</span></span>

<span data-ttu-id="cc80c-4035">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4035">6</span></span>

<span data-ttu-id="cc80c-4036">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4036">7</span></span>

<span data-ttu-id="cc80c-4037">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4037">8</span></span>

<span data-ttu-id="cc80c-4038">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4038">9</span></span>

<span data-ttu-id="cc80c-4039">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4039">1</span></span><br/> <span data-ttu-id="cc80c-4040">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4040">0</span></span><br/>

<span data-ttu-id="cc80c-4041">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4041">1</span></span>

<span data-ttu-id="cc80c-4042">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4042">2</span></span>

<span data-ttu-id="cc80c-4043">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4043">3</span></span>

<span data-ttu-id="cc80c-4044">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4044">4</span></span>

<span data-ttu-id="cc80c-4045">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4045">5</span></span>

<span data-ttu-id="cc80c-4046">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4046">6</span></span>

<span data-ttu-id="cc80c-4047">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4047">7</span></span>

<span data-ttu-id="cc80c-4048">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4048">8</span></span>

<span data-ttu-id="cc80c-4049">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4049">9</span></span>

<span data-ttu-id="cc80c-4050">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4050">2</span></span><br/> <span data-ttu-id="cc80c-4051">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4051">0</span></span><br/>

<span data-ttu-id="cc80c-4052">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4052">1</span></span>

<span data-ttu-id="cc80c-4053">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4053">2</span></span>

<span data-ttu-id="cc80c-4054">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4054">3</span></span>

<span data-ttu-id="cc80c-4055">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4055">4</span></span>

<span data-ttu-id="cc80c-4056">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4056">5</span></span>

<span data-ttu-id="cc80c-4057">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4057">6</span></span>

<span data-ttu-id="cc80c-4058">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4058">7</span></span>

<span data-ttu-id="cc80c-4059">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4059">8</span></span>

<span data-ttu-id="cc80c-4060">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4060">9</span></span>

<span data-ttu-id="cc80c-4061">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4061">3</span></span><br/> <span data-ttu-id="cc80c-4062">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4062">0</span></span><br/>

<span data-ttu-id="cc80c-4063">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4063">1</span></span>

<span data-ttu-id="cc80c-4064">\_Dividend</span><span class="sxs-lookup"><span data-stu-id="cc80c-4064">\_numerator</span></span>

<span data-ttu-id="cc80c-4065">\_Divisor</span><span class="sxs-lookup"><span data-stu-id="cc80c-4065">\_denominator</span></span>



 

<span data-ttu-id="cc80c-4066">**\_ Zähler:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Zeilennummer des Lesezeichens im Rowset enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4066">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="cc80c-4067">Wenn keine Zeilen vorhanden sind, MUSS dieses Feld auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4067">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="cc80c-4068">**\_ Nenner:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeilen im Rowset enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4068">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="cc80c-4069">2.2.3.25 CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-4069">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="cc80c-4070">Die CPMCompareBmkIn-Nachricht fordert einen Vergleich von zwei Lesezeichen in einem Kapitel an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4070">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="cc80c-4071">Das Format der CPMCompareBmkIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4071">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="cc80c-4072">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4072">0</span></span>

<span data-ttu-id="cc80c-4073">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4073">1</span></span>

<span data-ttu-id="cc80c-4074">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4074">2</span></span>

<span data-ttu-id="cc80c-4075">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4075">3</span></span>

<span data-ttu-id="cc80c-4076">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4076">4</span></span>

<span data-ttu-id="cc80c-4077">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4077">5</span></span>

<span data-ttu-id="cc80c-4078">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4078">6</span></span>

<span data-ttu-id="cc80c-4079">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4079">7</span></span>

<span data-ttu-id="cc80c-4080">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4080">8</span></span>

<span data-ttu-id="cc80c-4081">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4081">9</span></span>

<span data-ttu-id="cc80c-4082">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4082">1</span></span><br/> <span data-ttu-id="cc80c-4083">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4083">0</span></span><br/>

<span data-ttu-id="cc80c-4084">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4084">1</span></span>

<span data-ttu-id="cc80c-4085">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4085">2</span></span>

<span data-ttu-id="cc80c-4086">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4086">3</span></span>

<span data-ttu-id="cc80c-4087">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4087">4</span></span>

<span data-ttu-id="cc80c-4088">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4088">5</span></span>

<span data-ttu-id="cc80c-4089">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4089">6</span></span>

<span data-ttu-id="cc80c-4090">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4090">7</span></span>

<span data-ttu-id="cc80c-4091">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4091">8</span></span>

<span data-ttu-id="cc80c-4092">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4092">9</span></span>

<span data-ttu-id="cc80c-4093">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4093">2</span></span><br/> <span data-ttu-id="cc80c-4094">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4094">0</span></span><br/>

<span data-ttu-id="cc80c-4095">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4095">1</span></span>

<span data-ttu-id="cc80c-4096">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4096">2</span></span>

<span data-ttu-id="cc80c-4097">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4097">3</span></span>

<span data-ttu-id="cc80c-4098">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4098">4</span></span>

<span data-ttu-id="cc80c-4099">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4099">5</span></span>

<span data-ttu-id="cc80c-4100">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4100">6</span></span>

<span data-ttu-id="cc80c-4101">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4101">7</span></span>

<span data-ttu-id="cc80c-4102">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4102">8</span></span>

<span data-ttu-id="cc80c-4103">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4103">9</span></span>

<span data-ttu-id="cc80c-4104">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4104">3</span></span><br/> <span data-ttu-id="cc80c-4105">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4105">0</span></span><br/>

<span data-ttu-id="cc80c-4106">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4106">1</span></span>

<span data-ttu-id="cc80c-4107">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cc80c-4107">\_hCursor</span></span>

<span data-ttu-id="cc80c-4108">\_chapt</span><span class="sxs-lookup"><span data-stu-id="cc80c-4108">\_chapt</span></span>

<span data-ttu-id="cc80c-4109">\_bmkFirst</span><span class="sxs-lookup"><span data-stu-id="cc80c-4109">\_bmkFirst</span></span>

<span data-ttu-id="cc80c-4110">\_bmkSecond</span><span class="sxs-lookup"><span data-stu-id="cc80c-4110">\_bmkSecond</span></span>



 

<span data-ttu-id="cc80c-4111">\_**hCursor:** Ein 32-Bit-Wert, der das Handle der CPMCreateQueryOut-Nachricht für das Rowset darstellt, das die Lesezeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4111">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="cc80c-4112">\_**chapt:** Ein 32-Bit-Wert, der das Handle des Kapitels darstellt, das die zu vergleichenden Lesezeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4112">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="cc80c-4113">\_**bmkFirst:** Ein 32-Bit-Wert, der das Handle für das erste zu vergleichende Lesezeichen darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4113">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="cc80c-4114">\_**bmkSecond:** Ein 32-Bit-Wert, der das Handle für das zweite zu vergleichende Lesezeichen darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4114">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="cc80c-4115">2.2.3.26 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-4115">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="cc80c-4116">Die CPMCompareBmkOut-Nachricht antwortet auf eine CPMCompareBmkIn-Nachricht mit dem Vergleich der beiden Lesezeichen im Kapitel.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4116">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="cc80c-4117">Das Format der CPMCompareBmkOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4117">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="cc80c-4118">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4118">0</span></span>

<span data-ttu-id="cc80c-4119">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4119">1</span></span>

<span data-ttu-id="cc80c-4120">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4120">2</span></span>

<span data-ttu-id="cc80c-4121">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4121">3</span></span>

<span data-ttu-id="cc80c-4122">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4122">4</span></span>

<span data-ttu-id="cc80c-4123">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4123">5</span></span>

<span data-ttu-id="cc80c-4124">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4124">6</span></span>

<span data-ttu-id="cc80c-4125">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4125">7</span></span>

<span data-ttu-id="cc80c-4126">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4126">8</span></span>

<span data-ttu-id="cc80c-4127">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4127">9</span></span>

<span data-ttu-id="cc80c-4128">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4128">1</span></span><br/> <span data-ttu-id="cc80c-4129">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4129">0</span></span><br/>

<span data-ttu-id="cc80c-4130">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4130">1</span></span>

<span data-ttu-id="cc80c-4131">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4131">2</span></span>

<span data-ttu-id="cc80c-4132">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4132">3</span></span>

<span data-ttu-id="cc80c-4133">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4133">4</span></span>

<span data-ttu-id="cc80c-4134">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4134">5</span></span>

<span data-ttu-id="cc80c-4135">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4135">6</span></span>

<span data-ttu-id="cc80c-4136">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4136">7</span></span>

<span data-ttu-id="cc80c-4137">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4137">8</span></span>

<span data-ttu-id="cc80c-4138">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4138">9</span></span>

<span data-ttu-id="cc80c-4139">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4139">2</span></span><br/> <span data-ttu-id="cc80c-4140">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4140">0</span></span><br/>

<span data-ttu-id="cc80c-4141">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4141">1</span></span>

<span data-ttu-id="cc80c-4142">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4142">2</span></span>

<span data-ttu-id="cc80c-4143">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4143">3</span></span>

<span data-ttu-id="cc80c-4144">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4144">4</span></span>

<span data-ttu-id="cc80c-4145">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4145">5</span></span>

<span data-ttu-id="cc80c-4146">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4146">6</span></span>

<span data-ttu-id="cc80c-4147">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4147">7</span></span>

<span data-ttu-id="cc80c-4148">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4148">8</span></span>

<span data-ttu-id="cc80c-4149">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4149">9</span></span>

<span data-ttu-id="cc80c-4150">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4150">3</span></span><br/> <span data-ttu-id="cc80c-4151">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4151">0</span></span><br/>

<span data-ttu-id="cc80c-4152">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4152">1</span></span>

<span data-ttu-id="cc80c-4153">\_dwComparison</span><span class="sxs-lookup"><span data-stu-id="cc80c-4153">\_dwComparison</span></span>



 

<span data-ttu-id="cc80c-4154">\_**dwComparison:** Einer der folgenden Werte, der die relativen Positionen der beiden Lesezeichen im Kapitel angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4154">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="cc80c-4155">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-4155">Value</span></span>                               | <span data-ttu-id="cc80c-4156">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4156">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cc80c-4157">DBCOMPARE \_ LT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-4157">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="cc80c-4158">Das erste Lesezeichen wird vor dem zweiten positioniert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4158">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="cc80c-4159">DBCOMPARE \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc80c-4159">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="cc80c-4160">Das erste Lesezeichen hat die gleiche Position wie das zweite.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4160">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="cc80c-4161">DBCOMPARE \_ GT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc80c-4161">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="cc80c-4162">Das erste Lesezeichen wird nach dem zweiten positioniert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4162">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="cc80c-4163">DBCOMPARE \_ NE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cc80c-4163">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="cc80c-4164">Das erste Lesezeichen hat nicht die gleiche Position wie das zweite.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4164">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="cc80c-4165">DBCOMPARE \_ NOTCOMPARABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cc80c-4165">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="cc80c-4166">Das erste Lesezeichen ist nicht mit dem zweiten vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4166">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="cc80c-4167">2.2.3.27 CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-4167">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="cc80c-4168">Die CPMRestartPositionIn-Meldung verschiebt die Abrufposition für einen Cursor an den Anfang des Kapitels.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4168">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="cc80c-4169">Wie in Abschnitt 3.1.5.2.12 angegeben, antwortet der Server mit der gleichen Nachricht, und die Ergebnisse der Anforderung sind im Statusfeld des \_ CISP-Headers enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4169">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="cc80c-4170">Das Format der CPMRestartPositionIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4170">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="cc80c-4171">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4171">0</span></span>

<span data-ttu-id="cc80c-4172">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4172">1</span></span>

<span data-ttu-id="cc80c-4173">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4173">2</span></span>

<span data-ttu-id="cc80c-4174">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4174">3</span></span>

<span data-ttu-id="cc80c-4175">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4175">4</span></span>

<span data-ttu-id="cc80c-4176">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4176">5</span></span>

<span data-ttu-id="cc80c-4177">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4177">6</span></span>

<span data-ttu-id="cc80c-4178">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4178">7</span></span>

<span data-ttu-id="cc80c-4179">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4179">8</span></span>

<span data-ttu-id="cc80c-4180">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4180">9</span></span>

<span data-ttu-id="cc80c-4181">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4181">1</span></span><br/> <span data-ttu-id="cc80c-4182">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4182">0</span></span><br/>

<span data-ttu-id="cc80c-4183">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4183">1</span></span>

<span data-ttu-id="cc80c-4184">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4184">2</span></span>

<span data-ttu-id="cc80c-4185">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4185">3</span></span>

<span data-ttu-id="cc80c-4186">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4186">4</span></span>

<span data-ttu-id="cc80c-4187">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4187">5</span></span>

<span data-ttu-id="cc80c-4188">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4188">6</span></span>

<span data-ttu-id="cc80c-4189">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4189">7</span></span>

<span data-ttu-id="cc80c-4190">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4190">8</span></span>

<span data-ttu-id="cc80c-4191">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4191">9</span></span>

<span data-ttu-id="cc80c-4192">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4192">2</span></span><br/> <span data-ttu-id="cc80c-4193">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4193">0</span></span><br/>

<span data-ttu-id="cc80c-4194">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4194">1</span></span>

<span data-ttu-id="cc80c-4195">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4195">2</span></span>

<span data-ttu-id="cc80c-4196">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4196">3</span></span>

<span data-ttu-id="cc80c-4197">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4197">4</span></span>

<span data-ttu-id="cc80c-4198">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4198">5</span></span>

<span data-ttu-id="cc80c-4199">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4199">6</span></span>

<span data-ttu-id="cc80c-4200">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4200">7</span></span>

<span data-ttu-id="cc80c-4201">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4201">8</span></span>

<span data-ttu-id="cc80c-4202">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4202">9</span></span>

<span data-ttu-id="cc80c-4203">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4203">3</span></span><br/> <span data-ttu-id="cc80c-4204">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4204">0</span></span><br/>

<span data-ttu-id="cc80c-4205">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4205">1</span></span>

<span data-ttu-id="cc80c-4206">\_hCursor (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-4206">\_hCursor (optional)</span></span>

<span data-ttu-id="cc80c-4207">\_chapt (optional)</span><span class="sxs-lookup"><span data-stu-id="cc80c-4207">\_chapt (optional)</span></span>



 

<span data-ttu-id="cc80c-4208">**\_ hCursor:** Ein 32-Bit-Wert, der das Handle darstellt, das aus einer CPMCreateQueryOut-Nachricht ermittelt wird, die die Abfrage identifiziert, für die die Position neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4208">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="cc80c-4209">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4209">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cc80c-4210">**\_ chapt:** Ein 32-Bit-Wert, der das Handle eines Kapitels darstellt, aus dem Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4210">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="cc80c-4211">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4211">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="cc80c-4212">2.2.3.28 CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="cc80c-4212">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="cc80c-4213">Die CPMFreeCursorIn-Nachricht fordert die Freigabe eines Cursors an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4213">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="cc80c-4214">Das Format der CPMFreeCursorIn-Nachricht, die auf den Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4214">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="cc80c-4215">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4215">0</span></span>

<span data-ttu-id="cc80c-4216">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4216">1</span></span>

<span data-ttu-id="cc80c-4217">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4217">2</span></span>

<span data-ttu-id="cc80c-4218">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4218">3</span></span>

<span data-ttu-id="cc80c-4219">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4219">4</span></span>

<span data-ttu-id="cc80c-4220">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4220">5</span></span>

<span data-ttu-id="cc80c-4221">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4221">6</span></span>

<span data-ttu-id="cc80c-4222">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4222">7</span></span>

<span data-ttu-id="cc80c-4223">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4223">8</span></span>

<span data-ttu-id="cc80c-4224">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4224">9</span></span>

<span data-ttu-id="cc80c-4225">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4225">1</span></span><br/> <span data-ttu-id="cc80c-4226">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4226">0</span></span><br/>

<span data-ttu-id="cc80c-4227">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4227">1</span></span>

<span data-ttu-id="cc80c-4228">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4228">2</span></span>

<span data-ttu-id="cc80c-4229">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4229">3</span></span>

<span data-ttu-id="cc80c-4230">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4230">4</span></span>

<span data-ttu-id="cc80c-4231">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4231">5</span></span>

<span data-ttu-id="cc80c-4232">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4232">6</span></span>

<span data-ttu-id="cc80c-4233">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4233">7</span></span>

<span data-ttu-id="cc80c-4234">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4234">8</span></span>

<span data-ttu-id="cc80c-4235">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4235">9</span></span>

<span data-ttu-id="cc80c-4236">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4236">2</span></span><br/> <span data-ttu-id="cc80c-4237">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4237">0</span></span><br/>

<span data-ttu-id="cc80c-4238">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4238">1</span></span>

<span data-ttu-id="cc80c-4239">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4239">2</span></span>

<span data-ttu-id="cc80c-4240">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4240">3</span></span>

<span data-ttu-id="cc80c-4241">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4241">4</span></span>

<span data-ttu-id="cc80c-4242">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4242">5</span></span>

<span data-ttu-id="cc80c-4243">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4243">6</span></span>

<span data-ttu-id="cc80c-4244">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4244">7</span></span>

<span data-ttu-id="cc80c-4245">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4245">8</span></span>

<span data-ttu-id="cc80c-4246">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4246">9</span></span>

<span data-ttu-id="cc80c-4247">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4247">3</span></span><br/> <span data-ttu-id="cc80c-4248">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4248">0</span></span><br/>

<span data-ttu-id="cc80c-4249">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4249">1</span></span>

<span data-ttu-id="cc80c-4250">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cc80c-4250">\_hCursor</span></span>



 

<span data-ttu-id="cc80c-4251">**\_ hCursor:** Ein 32-Bit-Wert, der das Handle des Cursors aus der zu veröffentlichenden CPMCreateQueryOut-Nachricht darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4251">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="cc80c-4252">2.2.3.29 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="cc80c-4252">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="cc80c-4253">Die CPMFreeCursorOut-Nachricht antwortet auf eine CPMFreeCursorIn-Nachricht mit den Ergebnissen der Freigabe eines Cursors.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4253">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="cc80c-4254">Das Format der CPMFreeCursorOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4254">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="cc80c-4255">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4255">0</span></span>

<span data-ttu-id="cc80c-4256">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4256">1</span></span>

<span data-ttu-id="cc80c-4257">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4257">2</span></span>

<span data-ttu-id="cc80c-4258">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4258">3</span></span>

<span data-ttu-id="cc80c-4259">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4259">4</span></span>

<span data-ttu-id="cc80c-4260">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4260">5</span></span>

<span data-ttu-id="cc80c-4261">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4261">6</span></span>

<span data-ttu-id="cc80c-4262">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4262">7</span></span>

<span data-ttu-id="cc80c-4263">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4263">8</span></span>

<span data-ttu-id="cc80c-4264">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4264">9</span></span>

<span data-ttu-id="cc80c-4265">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4265">1</span></span><br/> <span data-ttu-id="cc80c-4266">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4266">0</span></span><br/>

<span data-ttu-id="cc80c-4267">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4267">1</span></span>

<span data-ttu-id="cc80c-4268">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4268">2</span></span>

<span data-ttu-id="cc80c-4269">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4269">3</span></span>

<span data-ttu-id="cc80c-4270">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4270">4</span></span>

<span data-ttu-id="cc80c-4271">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4271">5</span></span>

<span data-ttu-id="cc80c-4272">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4272">6</span></span>

<span data-ttu-id="cc80c-4273">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4273">7</span></span>

<span data-ttu-id="cc80c-4274">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4274">8</span></span>

<span data-ttu-id="cc80c-4275">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4275">9</span></span>

<span data-ttu-id="cc80c-4276">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4276">2</span></span><br/> <span data-ttu-id="cc80c-4277">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4277">0</span></span><br/>

<span data-ttu-id="cc80c-4278">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4278">1</span></span>

<span data-ttu-id="cc80c-4279">2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4279">2</span></span>

<span data-ttu-id="cc80c-4280">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4280">3</span></span>

<span data-ttu-id="cc80c-4281">4</span><span class="sxs-lookup"><span data-stu-id="cc80c-4281">4</span></span>

<span data-ttu-id="cc80c-4282">5</span><span class="sxs-lookup"><span data-stu-id="cc80c-4282">5</span></span>

<span data-ttu-id="cc80c-4283">6</span><span class="sxs-lookup"><span data-stu-id="cc80c-4283">6</span></span>

<span data-ttu-id="cc80c-4284">7</span><span class="sxs-lookup"><span data-stu-id="cc80c-4284">7</span></span>

<span data-ttu-id="cc80c-4285">8</span><span class="sxs-lookup"><span data-stu-id="cc80c-4285">8</span></span>

<span data-ttu-id="cc80c-4286">9</span><span class="sxs-lookup"><span data-stu-id="cc80c-4286">9</span></span>

<span data-ttu-id="cc80c-4287">3</span><span class="sxs-lookup"><span data-stu-id="cc80c-4287">3</span></span><br/> <span data-ttu-id="cc80c-4288">0</span><span class="sxs-lookup"><span data-stu-id="cc80c-4288">0</span></span><br/>

<span data-ttu-id="cc80c-4289">1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4289">1</span></span>

<span data-ttu-id="cc80c-4290">\_cCursorsRemaining</span><span class="sxs-lookup"><span data-stu-id="cc80c-4290">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="cc80c-4291">**\_ cCursorsRemaining:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der cursors angibt, die noch für die Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4291">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="cc80c-4292">2.2.3.30 CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="cc80c-4292">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="cc80c-4293">Die CPMDisconnect-Nachricht beendet die Verbindung mit dem Server.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4293">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="cc80c-4294">Die Nachricht DARF KEINEN Text enthalten. nur der Nachrichtenheader gemäß Abschnitt 2.2.2 gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4294">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="cc80c-4295">2.2.4 Fehler</span><span class="sxs-lookup"><span data-stu-id="cc80c-4295">2.2.4 Errors</span></span>

<span data-ttu-id="cc80c-4296">Alle Content Indexing Service Protocol-Meldungen MÜSSEN bei Erfolg 0x00000000 zurückgeben. Andernfalls geben sie einen 32-Bit-Fehlercode ungleich 0 (null) zurück, der entweder ein HRESULT- oder ein NTSTATUS-Wert sein kann (siehe Abschnitt 1.8).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4296">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="cc80c-4297">Wenn ein Puffer zu klein für ein Ergebnis ist, MUSS der Statuscode STATUS \_ INSUFFICIENT \_ RESOURCES (0xC0000009A) zurückgegeben werden, und der fehlerhafte Vorgang sollte mit einem größeren Puffer wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4297">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="cc80c-4298">Alle anderen Fehlerwerte MÜSSEN gleich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4298">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="cc80c-4299">(Beachten Sie, dass sich die Nummerierungsräume HRESULT und NTSTATUS derzeit nur mit Werten mit identischer Bedeutung überschneiden. Selbst wenn sie in Zukunft konflikteig sein sollten, würde dies keine Protokollprobleme verursachen, solange der Wert für STATUS \_ INSUFFICIENT \_ RESOURCES bleibt eindeutig, da alle anderen Fehlerwerte gleich behandelt werden.)</span><span class="sxs-lookup"><span data-stu-id="cc80c-4299">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="cc80c-4300">3 Protokolldetails</span><span class="sxs-lookup"><span data-stu-id="cc80c-4300">3 Protocol Details</span></span>

-   [<span data-ttu-id="cc80c-4301">3.1 Serverdetails</span><span class="sxs-lookup"><span data-stu-id="cc80c-4301">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="cc80c-4302">3.2 Clientdetails</span><span class="sxs-lookup"><span data-stu-id="cc80c-4302">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="cc80c-4303">CISP-Nachrichtenanforderungen zum Remoteabfragen der Indizierungsdienstkataloge erfordern keine bestimmte Sequenz.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4303">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="cc80c-4304">Es wird jedoch empfohlen, dass die höhere Ebene einer sinnvollen Nachrichtensequenz folgt, da der Server bei Nachrichten, die aus dieser Sequenz oder mit ungültigen Daten empfangen werden, mit einem Fehler antwortet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4304">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="cc80c-4305">Einige Nachrichten sind auch von der höheren Ebene abhängig, die gültige Daten bereitstellt, die in Früheren Nachrichten in der Sequenz empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4305">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="cc80c-4306">Eine typische Nachrichtensequenz für eine einfache Abfrage von einem Client an einen Remotecomputer ist im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4306">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![Nachrichtensequenz für einfache Abfragen](images/protocoldetails.jpg)

<span data-ttu-id="cc80c-4308">Die im vorherigen Diagramm dargestellten Nachrichten stellen eine Teilmenge aller CISP-Nachrichten dar, die zum Abfragen eines Remoteindizierungsdienstkatalogs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4308">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="cc80c-4309">3.1 Serverdetails</span><span class="sxs-lookup"><span data-stu-id="cc80c-4309">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="cc80c-4310">3.1.1 Abstraktes Datenmodell</span><span class="sxs-lookup"><span data-stu-id="cc80c-4310">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="cc80c-4311">Im folgenden Abschnitt werden die vom CISP-Server verwalteten Daten und der Zustand angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4311">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="cc80c-4312">Mit den hier bereitgestellten Daten soll das Verhalten des Protokolls erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4312">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="cc80c-4313">In diesem Abschnitt ist nicht die Einhaltung dieses Modells durch Implementierungen vorschrieben, solange ihr externes Verhalten mit dem in diesem Dokument beschriebenen Verhalten konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4313">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="cc80c-4314">Ein Indizierungsdienst, der den CISP implementieren muss die folgenden abstrakten Datenelemente verwalten:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4314">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="cc80c-4315">Die Liste der clients, die mit dem Server verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4315">The list of clients connected to the server</span></span>
-   <span data-ttu-id="cc80c-4316">Informationen zu jedem Client, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4316">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="cc80c-4317">Clientversion (wie in der CPMConnectIn-Nachricht angegeben in Abschnitt 2.2.3.6)</span><span class="sxs-lookup"><span data-stu-id="cc80c-4317">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="cc80c-4318">Katalog, der dem Client zugeordnet ist (durch eine CPMConnectIn-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="cc80c-4318">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="cc80c-4319">Zusätzliche Clienteigenschaften, wie in Abschnitt 2.2.1.21.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4319">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="cc80c-4320">Suchabfrage des Clients</span><span class="sxs-lookup"><span data-stu-id="cc80c-4320">Client's search query</span></span>
    -   <span data-ttu-id="cc80c-4321">Liste der Cursorhandles für die Abfrage und Position im ResultSet für jedes Handle.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4321">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="cc80c-4322">Aktueller Satz von Bindungen</span><span class="sxs-lookup"><span data-stu-id="cc80c-4322">Current set of bindings</span></span>
    -   <span data-ttu-id="cc80c-4323">Aktueller Status der Abfrage, einschließlich (für jeden Cursor):</span><span class="sxs-lookup"><span data-stu-id="cc80c-4323">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="cc80c-4324">Anzahl der Zeilen im Abfrageergebnis</span><span class="sxs-lookup"><span data-stu-id="cc80c-4324">Number of rows in query result</span></span>
        -   <span data-ttu-id="cc80c-4325">Zähler und Nenner der Abfrageerledigung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4325">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="cc80c-4326">Letzte Anzahl von Zeilen, die von der letzten CPMRatioFinishedOut-Meldung für diesen Cursor gemeldet wurden</span><span class="sxs-lookup"><span data-stu-id="cc80c-4326">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="cc80c-4327">Ob die Abfrage vom Server auf Änderungen in den Abfrageergebnissen überwacht wird und ob sie überwacht wird, was sich in den Abfrageergebnissen geändert hat, seit sie zuletzt von CPMSendNotifyOut an den Client gemeldet wurde</span><span class="sxs-lookup"><span data-stu-id="cc80c-4327">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="cc80c-4328">Liste der Kapitelhandles, die von dieser Abfrage für einen Client verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4328">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="cc80c-4329">Liste der Lesezeichenhandles für jeden Cursor, die von dieser Abfrage an einen Client bedient werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4329">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="cc80c-4330">Der aktuelle Status des Indizierungsdiensts, der möglicherweise "nicht initialisiert", "wird ausgeführt" oder "heruntergefahren" ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4330">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="cc80c-4331">Beachten Sie, dass sich der Server größtenteils im Status "Wird ausgeführt" befindet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4331">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="cc80c-4332">Im Folgenden ist das Zustandsautomatendiagramm für den Server dargestellt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4332">Following is the state machine diagram for the server:</span></span>

    ![Zustandsautomatendiagramm des Indizierungsdienstservers](images/abstractdatamodel.jpg)

-   <span data-ttu-id="cc80c-4334">Katalogspezifische Informationen: Anzahl der indizierten Dokumente, Indexgröße, Anzahl eindeutiger Schlüssel usw. (vollständige Liste finden Sie in Abschnitt 2.2.3.1), Status (entspricht den Werten von dwNewState in Abschnitt 2.2.3.2).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4334">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="cc80c-4335">Für jede unterstützte Sprache eine Datenbank mit Wortvarianten, wie in Abschnitt 2.2.1.3 erläutert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4335">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="cc80c-4336">3.1.2 Zeitgeber</span><span class="sxs-lookup"><span data-stu-id="cc80c-4336">3.1.2 Timers</span></span>

<span data-ttu-id="cc80c-4337">Es sind keine Protokolltimer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4337">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="cc80c-4338">3.1.3 Initialisierung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4338">3.1.3 Initialization</span></span>

<span data-ttu-id="cc80c-4339">Bei der Initialisierung MUSS der Server seinen Zustand auf "nicht initialisiert" festlegen und mit dem Lauschen auf Nachrichten an der in Abschnitt 1.9 angegebenen Named Pipe beginnen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4339">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="cc80c-4340">Nachdem sie eine andere interne Initialisierung ausgeführt hat, MUSS sie in den Zustand "Wird ausgeführt" übergehen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4340">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="cc80c-4341">3.1.4 Ausgelöste Ereignisse auf höherer Ebene</span><span class="sxs-lookup"><span data-stu-id="cc80c-4341">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="cc80c-4342">Keine.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4342">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="cc80c-4343">3.1.5 Nachrichtenverarbeitungs- und Sequenzierungsregeln</span><span class="sxs-lookup"><span data-stu-id="cc80c-4343">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="cc80c-4344">Wenn während der Verarbeitung einer von einem Client gesendeten Nachricht ein Fehler auftritt, MUSS der Server einen Fehler wie folgt an den Client melden:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4344">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="cc80c-4345">Beenden der Verarbeitung der vom Client gesendeten Nachricht</span><span class="sxs-lookup"><span data-stu-id="cc80c-4345">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="cc80c-4346">Antworten Sie mit dem Nachrichtenheader (nur) der vom Client gesendeten Nachricht, und behalten Sie dabei \_ das Msg-Feld bei.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4346">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="cc80c-4347">Legen Sie das \_ Statusfeld auf den Fehlercodewert fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4347">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="cc80c-4348">Wenn eine Nachricht eingeht, MUSS der Server den \_ Msg-Feldwert überprüfen, um festzustellen, ob es sich um einen bekannten Typ handelt (siehe Abschnitt 2.2.2).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4348">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="cc80c-4349">Wenn der Typ nicht bekannt ist, MUSS er einen STATUS \_ INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4349">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="cc80c-4350">Der Server MUSS dann den \_ UlChecksum-Feldwert überprüfen, wenn der Nachrichtentyp einer der folgenden Ist:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4350">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="cc80c-4351">CPMConnectIn (0x000000C8)</span><span class="sxs-lookup"><span data-stu-id="cc80c-4351">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="cc80c-4352">CPMCreateQueryIn (0x000000CA)</span><span class="sxs-lookup"><span data-stu-id="cc80c-4352">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="cc80c-4353">CPMSetBindingsIn (0x000000D0)</span><span class="sxs-lookup"><span data-stu-id="cc80c-4353">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="cc80c-4354">CPMGetRowsIn (0x000000CC)</span><span class="sxs-lookup"><span data-stu-id="cc80c-4354">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="cc80c-4355">CPMFetchValueIn (0x000000E4)</span><span class="sxs-lookup"><span data-stu-id="cc80c-4355">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="cc80c-4356">Um den ulChecksum-Feldwert zu überprüfen, MUSS der Server den Wert überprüfen, den der Client \_ im \_ Feld iClientVersion in der CPMConnectIn-Nachricht angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4356">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="cc80c-4357">Wenn das Feld iClientVersion nicht auf 0x00000008 und das feld ulChecksum nicht auf 0x00000000 festgelegt ist, MUSS der Server einen \_ \_ STATUS INVALID PARAMETER \_ \_ (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4357">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="cc80c-4358">Server MUST NOT validate the \_ ulChecksum field for clients the set the \_ iClientVersion field to a value less than 0x00000008.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4358">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="cc80c-4359">Wenn der Feldwert iClientVersionfield 0x00000008 ist, MUSS der Server überprüfen, ob das feld ulChecksum wie in Abschnitt \_ \_ 3.2.4 angegeben berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4359">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="cc80c-4360">Wenn der \_ ulChecksum-Wert ungültig ist, MUSS der Server den Fehler STATUS \_ INVALID PARAMETER \_ (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4360">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="cc80c-4361">Als Nächstes überprüft der Server, in welchem Zustand er sich befindet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4361">Next, the server checks which state is it in.</span></span> <span data-ttu-id="cc80c-4362">Wenn der Status "nicht initialisiert" ist, MUSS der Server einen CI \_ E \_ NOT \_ INITIALIZED(0x8004180B)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4362">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="cc80c-4363">Wenn der Status "heruntergefahren" ist, MUSS der Server einen CI \_ E \_ SHUTDOWN-Fehler (0x80041812 melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4363">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="cc80c-4364">Sobald ein Header als gültig festgelegt wurde und sich der Server im Status "Wird ausgeführt" befing, MUSS eine weitere nachrichtenspezifische Verarbeitung erfolgen, wie in den folgenden Unterabschnitten angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4364">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="cc80c-4365">3.1.5.1 Katalogverwaltung des Remoteindizierungsdiensts</span><span class="sxs-lookup"><span data-stu-id="cc80c-4365">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="cc80c-4366">3.1.5.1.1 Empfangen einer CPMCiStateInOut-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4366">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="cc80c-4367">Wenn der Server eine CPMCIStateInOut-Nachrichtenanforderung vom Client empfängt, MUSS der Server zunächst überprüfen, ob sich der Client in einer Liste verbundener Clients befindet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4367">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="cc80c-4368">Wenn der Client nicht in der Liste enthalten ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4368">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="cc80c-4369">Andernfalls MUSS er an den Client mit einer CPMCIStateInOut-Nachricht antworten und mit Informationen zum zugeordneten Katalog des Clients auffüllen, wie in Abschnitt 2.2.3.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4369">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="cc80c-4370">3.1.5.1.2 Empfangen einer CPMSetCatStateIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4370">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="cc80c-4371">Wenn der Server eine CPMSetCatStateIn-Nachrichtenanforderung vom Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4371">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4372">Überprüfen Sie, ob der Client über Administratorzugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4372">Check that client has administrative access.</span></span> <span data-ttu-id="cc80c-4373">Wenn der Client keinen Administratorzugriff hat, MUSS der Server einen \_ STATUS ACCESS \_ DENIED(0xC0000022)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4373">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="cc80c-4374">Wenn \_ dwNewState ungleich CICAT \_ ALL OPENED \_ ist, ändern Sie den Status des Katalogs, der im Feld CatName angegeben ist, wie im \_ Feld dwNewState angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4374">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="cc80c-4375">Weitere Informationen finden Sie in Abschnitt 2.2.3.2.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4375">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="cc80c-4376">Wenn der Server keinen Katalog mit dem im Feld CatName angegebenen Namen findet, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4376">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4377">Reagieren Sie auf den Client mit einer CPMSetCatStateOut-Meldung, bei \_ der dwOldState auf den vorherigen Status des Katalogs festgelegt werden MUSS.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4377">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="cc80c-4378">Wenn \_ dwNewState gleich CICAT ALL OPENED ist, \_ MUSS der Server den Status aller \_ Kataloge überprüfen. Wenn alle kataloge gestartet werden, MUSS \_ dwOldState auf 0x00000001 und andernfalls \_ dwOldState auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4378">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="cc80c-4379">3.1.5.1.3 Empfangen einer CPMUpdateDocumentsIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4379">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="cc80c-4380">Wenn der Server eine CPMUpdateDocumentsIn-Nachrichtenanforderung empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4380">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4381">Überprüfen Sie, ob sich der Client in einer Liste verbundener Clients befindet (denen ein Katalog zugeordnet ist).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4381">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="cc80c-4382">Wenn der Client nicht in der Liste enthalten ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4382">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4383">Überprüfen Sie, ob der Client über Administratorzugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4383">Check that client has administrative access.</span></span> <span data-ttu-id="cc80c-4384">Wenn der Client keinen Administratorzugriff auf den Server hat, MUSS der Server einen \_ STATUS ACCESS \_ DENIED(0xC0000022)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4384">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="cc80c-4385">Beginnen Sie den Prozess der Indizierung des vom Client angegebenen Pfads, indem Sie abhängig vom Wert des Flagfelds in der CPMUpdateDocumentsIn-Nachricht eine vollständige oder inkrementelle Überprüfung \_ durchführen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4385">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="cc80c-4386">Wenn der Pfad nicht zuvor indiziert wurde, MUSS er der Auflistung indizierter Speicherorte hinzugefügt und eine vollständige Überprüfung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4386">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="cc80c-4387">Wenn ein ungültiger Wert des \_ Flagfelds angegeben wird, MUSS der Server so vorgehen, als ob \_ das Flag auf UPD INIT festgelegt wäre, \_ und eine vollständige Überprüfung ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4387">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="cc80c-4388">Dieser Vorgang MUSS in dem Katalog ausgeführt werden, der dem Client zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4388">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="cc80c-4389">Reagieren Sie mit dem Nachrichtenheader für CPMUpdateDocumentsIn auf den Client, und legen Sie das Statusfeld auf die \_ Ergebnisse der Anforderung fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4389">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="cc80c-4390">3.1.5.1.4 Empfangen einer CPMForceMergeIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4390">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="cc80c-4391">Wenn der Server eine CPMForceMergeIn-Nachrichtenanforderung empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4391">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4392">Überprüfen Sie, ob sich der Client in einer Liste verbundener Clients befindet (denen ein Katalog zugeordnet ist).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4392">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="cc80c-4393">Wenn der Client nicht in der Liste enthalten ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4393">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4394">Überprüfen Sie, ob der Client über Administratorzugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4394">Check that client has administrative access.</span></span> <span data-ttu-id="cc80c-4395">Wenn der Client keinen Administratorzugriff hat, MUSS der Server den Fehler STATUS \_ ACCESS \_ DENIED (0xC0000022) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4395">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="cc80c-4396">Starten Sie alle Wartungsprozesse, die erforderlich sind, um die Abfrageleistung für einen Katalog zu verbessern, der dem Client zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4396">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="cc80c-4397">Reagieren Sie mit einem Nachrichtenheader für CPMForceMergeIn auf den Client, und legen Sie das Statusfeld auf die \_ Ergebnisse der Anforderung fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4397">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="cc80c-4398">Beachten Sie, dass der Wartungsvorgang asynchron ist und fortgesetzt werden kann, nachdem der Client die Antwortnachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4398">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="cc80c-4399">Dieser Prozess wirkt sich nicht direkt auf das Protokoll aus (mit Einer Anderen als der Antwortzeit).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4399">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="cc80c-4400">3.1.5.2 Abfragen des Remoteindizierungsdiensts</span><span class="sxs-lookup"><span data-stu-id="cc80c-4400">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="cc80c-4401">3.1.5.2.1 Empfangen einer CPMConnectIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4401">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="cc80c-4402">Wenn der Server eine CPMConnectIn-Anforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4402">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4403">Überprüfen Sie, ob sich der Client in der Liste der verbundenen Clients befindet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4403">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="cc80c-4404">Wenn dies der Fall ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4404">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4405">Überprüft, ob der angegebene Katalog vorhanden ist und sich nicht im Zustand "Beendet" befliegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4405">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="cc80c-4406">Wenn dies nicht der Fall ist, MUSS der Server einen CI \_ E \_ NO CATALOG \_ -Fehler (0x8004181D) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4406">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="cc80c-4407">Fügen Sie den Client der Liste der verbundenen Clients hinzu.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4407">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="cc80c-4408">Ordnen Sie den Katalog dem Client zu.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4408">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="cc80c-4409">Speichern Sie die in der CPMConnectIn-Nachricht übergebenen Informationen (z. B. Katalogname, Clientversion usw.) im Clientzustand.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4409">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="cc80c-4410">Reagieren Sie mit einer CPMConnectOut-Nachricht auf den Client.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4410">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="cc80c-4411">3.1.5.2.2 Empfangen einer CPMCreateQueryIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4411">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="cc80c-4412">Wenn der Server eine CPMCreateQueryIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4412">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4413">Überprüfen Sie, ob der Client in der Liste der verbundenen Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4413">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="cc80c-4414">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4414">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4415">Überprüfen Sie, ob dem Client bereits eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4415">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="cc80c-4416">Wenn dies der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4416">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4417">Überprüfen Sie, ob sich der dem Client zugeordnete Katalog im Zustand befindet, der die Verarbeitung von Abfragen ermöglicht (CICAT \_ READONLY oder CICAT \_ WRITABLE).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4417">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="cc80c-4418">Wenn dies nicht der Fall ist, MUSS der Server einen \_ QUERY S \_ NO \_ QUERY-Fehler (0x8004160C) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4418">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="cc80c-4419">Analysieren Sie den Einschränkungssatz, die Sortierreihenfolgen und die in der Abfrage angegebenen Gruppierungen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4419">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="cc80c-4420">Wenn auf dem Server ein Fehler auftritt, MUSS ein entsprechender Fehler gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4420">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="cc80c-4421">Wenn dieser Schritt aus einem anderen Grund fehlschlägt, MUSS der Server den aufgetretenen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4421">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="cc80c-4422">Informationen zu Indizierungsdienst-Abfragefehlern finden Sie unter \[ MSDN-QUERYERR \] .</span><span class="sxs-lookup"><span data-stu-id="cc80c-4422">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="cc80c-4423">Speichern Sie die Suchabfrage im Zustand für den Client.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4423">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="cc80c-4424">Treffen Sie alle erforderlichen Vorbereitungen, um Zeilen an einen Client zu übermitteln, und ordnen Sie die Abfrage den entsprechenden Cursorhandles zu (abhängig von den informationen, die in der CPMCreateQueryIn-Nachricht übergeben werden).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4424">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="cc80c-4425">Fügen Sie diese Handles der Liste der Cursorhandles des Clients hinzu, und initialisieren Sie Listen von Kapitelhandles und Lesezeichen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4425">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="cc80c-4426">Initialisieren der Liste der Kapitelhandles für jeden Cursor in dieser Abfrage in DB \_ NULL \_ HCHAPTER</span><span class="sxs-lookup"><span data-stu-id="cc80c-4426">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="cc80c-4427">Initialisieren Sie die Liste der Lesezeichenhandles für jeden Cursor in dieser Abfrage mit einem Satz von DBBMK \_ FIRST und DBBMK \_ LAST.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4427">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="cc80c-4428">Markieren Sie die Abfrage als nicht auf Änderungen überwacht.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4428">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="cc80c-4429">Initialisieren Sie die Anzahl der Zeilen mit der derzeit berechneten Anzahl von Zeilen (die 0 sein kann, wenn die Abfrage nicht gestartet wurde, oder eine zahl, wenn die Abfrage ausgeführt wird), und initialisieren Sie den Zähler und Denominator des Abfrageabschlusses.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4429">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="cc80c-4430">Reagieren Sie mit einer CPMCreateQueryOut-Nachricht auf den Client.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4430">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="cc80c-4431">3.1.5.2.3 Empfangen einer CPMGetQueryStatusIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4431">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="cc80c-4432">Wenn der Server eine CPMGetQueryStatusIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4432">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4433">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4433">Check if the client has query associated with it.</span></span> <span data-ttu-id="cc80c-4434">Wenn dies nicht der Fall ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4434">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4435">Überprüfen Sie, ob das Cursorhandles in einer Liste der Cursorhandles des Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4435">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="cc80c-4436">Wenn dies nicht der Fall ist, MUSS der Server den Fehler E \_ FAIL (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4436">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cc80c-4437">Bereiten Sie eine CPMGetQueryStatusOut-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4437">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="cc80c-4438">Der Server MUSS den aktuellen Abfragestatus abrufen und im QStatus-Feld festlegen (mögliche Werte finden Sie unter \_ 2.2.3.11).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4438">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="cc80c-4439">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4439">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="cc80c-4440">Reagieren Sie mit der Nachricht CPMGetQueryStatusOut auf den Client.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4440">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="cc80c-4441">3.1.5.2.4 Empfangen einer CPMGetQueryStatusExIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4441">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="cc80c-4442">Wenn der Server eine CPMGetQueryStatusExIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4442">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4443">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4443">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cc80c-4444">Wenn dies nicht der Fall ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4444">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4445">Überprüfen Sie, ob das übergebene Cursorhandles in einer Liste der Cursorhandles des Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4445">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="cc80c-4446">Wenn dies nicht der Fall ist, MUSS der Server den Fehler E \_ FAIL (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4446">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cc80c-4447">Bereiten Sie eine CPMGetQueryStatusExOut-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4447">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="cc80c-4448">Der Server MUSS den aktuellen Abfragestatus und den Abfragestatus abrufen und QStatus festlegen (mögliche Werte finden Sie unter 2.2.3.11), \_ dwRatioFinishedDenominator bzw. \_ dwRatioFinishedNumerator.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4448">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="cc80c-4449">Anschließend MUSS die Anzahl der Zeilen in den Abfrageergebnissen auf \_ cRowsTotal festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4449">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="cc80c-4450">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4450">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cc80c-4451">Rufen Sie Informationen zum Clientkatalog ab, und geben Sie \_ cFilteredDocuments und \_ cDocumentsToFilter ein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4451">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="cc80c-4452">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4452">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cc80c-4453">Rufen Sie die Position des Lesezeichens ab, das durch das Handle im \_ bmk-Feld angegeben wird, und füllen Sie das verbleibende \_ iRowBmk-Feld in der CPMGetQueryStatusExOut-Meldung aus.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4453">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="cc80c-4454">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4454">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cc80c-4455">Reagieren Sie mit der MELDUNG CPMGetQueryStatusExOut auf den Client.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4455">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="cc80c-4456">3.1.5.2.5 Empfangen einer CPMRatioFinishedIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4456">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="cc80c-4457">Wenn der Server eine CPMRatioFinishedIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4457">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4458">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4458">Check if the client has query associated with it.</span></span> <span data-ttu-id="cc80c-4459">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4459">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4460">Überprüfen Sie, ob das übergebene Cursorhandle in der Liste der Cursorhandles des Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4460">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="cc80c-4461">Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4461">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cc80c-4462">Bereiten Sie eine CPMRatioFinishedOut-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4462">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="cc80c-4463">Der Server MUSS den Abfragestatus des Clients abrufen und \_ die Felder ulNumerator, \_ ulDenominator und \_ cRows ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4463">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="cc80c-4464">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4464">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cc80c-4465">Wenn \_ cRows gleich der letzten gemeldeten Anzahl von Zeilen für diese Abfrage ist, legen Sie \_ fNewRows auf 0x00000000 fest, andernfalls auf 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4465">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="cc80c-4466">Aktualisieren Sie die zuletzt gemeldete Anzahl von Zeilen für diese Abfrage auf den Wert von \_ cRows.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4466">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="cc80c-4467">Antworten Sie mit der Meldung CPMRatioFinishedOut auf den Client.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4467">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="cc80c-4468">3.1.5.2.6 Empfangen einer CPMSetBindingsIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4468">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="cc80c-4469">Wenn der Server eine CPMSetBindingsIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4469">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4470">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4470">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cc80c-4471">Wenn dies nicht der Fall ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4471">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4472">Überprüfen Sie, ob das übergebene Cursorhandles in der Liste der Cursorhandles des Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4472">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="cc80c-4473">Wenn dies nicht der Fall ist, MUSS der Server den Fehler E \_ FAIL (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4473">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cc80c-4474">Vergewissern Sie sich, dass Bindungsinformationen gültig sind (d. h., die Spalte gibt mindestens den Wert, die Länge oder den Status an, der zurückgegeben werden soll; keine Überlappung der Bindungen für Wert, Länge oder Status; Wert, Länge und Status passt in die angegebene Zeilengröße) und melden, wenn kein DB \_ E \_ BADBINDINFO (0x80040E08)-Fehler ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4474">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="cc80c-4475">Speichern Sie die Bindungsinformationen, die den im Feld aColumns angegebenen Spalten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4475">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="cc80c-4476">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4476">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cc80c-4477">Reagieren Sie auf den Client mit einem Nachrichtenheader (nur), bei dem msg auf \_ CPMSetBindingsIn und status auf die Ergebnisse der angegebenen \_ Bindung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4477">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="cc80c-4478">3.1.5.2.7 Empfangen einer CPMGetRowsIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4478">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="cc80c-4479">Wenn der Server eine CPMGetRowsIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4479">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4480">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4480">Check if the client has query associated with it.</span></span> <span data-ttu-id="cc80c-4481">Wenn dies nicht der Fall ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4481">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4482">Überprüfen Sie, ob sich das übergebene Cursorhandles in der Athelist der Cursorhandles des Clients befindet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4482">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="cc80c-4483">Wenn dies nicht der Fall ist, MUSS der Server den Fehler E \_ FAIL (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4483">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cc80c-4484">Überprüfen Sie, ob der Client über einen aktuellen Satz von Bindungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4484">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="cc80c-4485">Wenn dies nicht der Fall ist, MUSS der Server den Fehler E \_ FAIL (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4485">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cc80c-4486">Bereiten Sie eine CPMGetRowsOut-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4486">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="cc80c-4487">Der Server MUSS den Cursor in Abfrageergebnissen positionieren, wie in der Suchbeschreibung angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4487">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="cc80c-4488">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4488">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cc80c-4489">Rufen Sie so viele Zeilen ab, wie in einen Puffer passen, dessen Größe durch \_ cbReadBuffer angegeben wird, aber nicht mehr als durch \_ cRowsToTransfer angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4489">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="cc80c-4490">Beim Abrufen von Zeilen MUSS der Server den Eigenschaftswerttyp jeder ausgewählten Spalte mit dem Typ vergleichen, der im aktuellen Bindungssatz des Clients (Abschnitt 3.1.1) angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4490">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="cc80c-4491">Wenn der Typ in der Bindung nicht VT \_ VARIANT ist, MUSS der Server versuchen, den Eigenschaftswert der Spalte in diesen Typ zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4491">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="cc80c-4492">Andernfalls MUSS der Eigenschaftswert in seinem normalen Typ zurückgegeben werden, wenn das DBPROP \_ USEEXTENDEDDBTYPES-Flag im DBPROPSET \_ QUERYEXT-Eigenschaftensatz des Clients festgelegt ist oder wenn der Eigenschaftswert der Spalte kein VT \_ VECTOR-Typ ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4492">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="cc80c-4493">Wenn keines davon der Fall ist (d. h. der Server hat einen VT \_ VECTOR-Typ, und der Client unterstützt VT \_ VECTOR nicht), MUSS der Server versuchen, ihn wie folgt in einen \_ VT ARRAY-Typ zu konvertieren: VT \_ I8, VT \_ UI8, VT \_ FILETIME und VT \_ CLSID Array-Elemente können nicht konvertiert werden und schlagen stattdessen fehl. VT \_ LPSTR- und VT \_ LPWSTR-Arrayelemente MÜSSEN in VT BSTR konvertiert \_ werden. Arrayelemente aller anderen Typen MÜSSEN unverändert bleiben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4493">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="cc80c-4494">Wenn Zeilenspalten Kapitelhandles oder Lesezeichenhandles enthalten, MUSS der Server die entsprechenden Listen aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4494">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="cc80c-4495">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4495">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cc80c-4496">Speichern Sie die tatsächliche Anzahl der abgerufenen Zeilen in \_ cRowsReturned.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4496">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="cc80c-4497">Kopieren Sie die Suchbeschreibung und das Kapitelfeld aus CPMGetRowsIn in eine zu sendende CPMGetRowsOut-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4497">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="cc80c-4498">Speichern Sie abgerufene Zeilen im Feld Zeilen (siehe Hinweis zum Status byte unten und Abschnitt 2.2.3.16 zur Struktur des Rows-Felds).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4498">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="cc80c-4499">Reagieren Sie mit der CPMGetRowsOut-Meldung auf den Client.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4499">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="cc80c-4500">Hinweis zum Status-Bytefeld:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4500">Note on status byte field:</span></span>

<span data-ttu-id="cc80c-4501">Wenn StatusUsed auf 0x01 in CTableColumn der CPMSetBindingIn-Nachricht für die Spalte festgelegt ist, MUSS der Server das Status byte (das sich am Anfang der Zeile unter StatusOffset befindet) für diese Spalte auf einen der folgenden Werte festlegen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4501">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="cc80c-4502">Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-4502">Value</span></span> | <span data-ttu-id="cc80c-4503">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4503">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="cc80c-4504">0x00</span><span class="sxs-lookup"><span data-stu-id="cc80c-4504">0x00</span></span>  | <span data-ttu-id="cc80c-4505">StatusOK</span><span class="sxs-lookup"><span data-stu-id="cc80c-4505">StatusOK</span></span>       |
| <span data-ttu-id="cc80c-4506">0x01</span><span class="sxs-lookup"><span data-stu-id="cc80c-4506">0x01</span></span>  | <span data-ttu-id="cc80c-4507">StatusDeferred</span><span class="sxs-lookup"><span data-stu-id="cc80c-4507">StatusDeferred</span></span> |
| <span data-ttu-id="cc80c-4508">0x02</span><span class="sxs-lookup"><span data-stu-id="cc80c-4508">0x02</span></span>  | <span data-ttu-id="cc80c-4509">StatusNull</span><span class="sxs-lookup"><span data-stu-id="cc80c-4509">StatusNull</span></span>     |



 

<span data-ttu-id="cc80c-4510">Wenn der Eigenschaftswert für diese Zeile nicht vorhanden ist, MUSS der Server das Status byte auf StatusNull festlegen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4510">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="cc80c-4511">Wenn der Wert zu groß ist, um in der CPMGetRowsOut-Nachricht übertragen zu werden, MUSS der Server das Status byte auf StatusDeferred festlegen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4511">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="cc80c-4512">Andernfalls MUSS der Server das Status byte auf StatusOK festlegen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4512">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="cc80c-4513">3.1.5.2.8 Empfangen einer CPMFetchValueIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4513">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="cc80c-4514">Wenn der Server eine CPMFetchValueIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4514">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4515">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4515">Check if the client has query associated with it.</span></span> <span data-ttu-id="cc80c-4516">Wenn dies nicht der Fall ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4516">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4517">Bereiten Sie eine CPMFetchValueOut-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4517">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="cc80c-4518">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="cc80c-4519">Suchen Sie das durch das Feld wid angegebene Dokument, und überprüfen Sie, ob die Eigenschaften-ID für dieses Dokument (später als "Eigenschaftswert" bezeichnet) für diesen Client verfügbar \_ ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4519">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="cc80c-4520">Wenn dieser Wert nicht verfügbar ist, MUSS der Server \_ fValueExists auf 0x00000000 festlegen, andernfalls \_ fValueExists auf 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4520">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="cc80c-4521">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4521">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="cc80c-4522">Wenn \_ fValueExists gleich 0x00000001 muss der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4522">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="cc80c-4523">Serialisieren Sie den Eigenschaftswert in eine SERIALIZEDPROPERTYVALUE-Struktur, und kopieren Sie ab dem cbSoFar-Offset alle cbChunk-Bytes (jedoch nicht über das Ende der serialisierten Eigenschaft hinaus) in das \_ \_ vValue-Feld.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4523">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="cc80c-4524">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4524">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="cc80c-4525">Legen \_ Sie cbValue auf die Anzahl der Bytes fest, die im vorherigen Schritt kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4525">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="cc80c-4526">Legen Sie vType auf den Eigenschaftentyp des Eigenschaftswerts fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4526">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="cc80c-4527">Wenn die Länge der serialisierten Eigenschaft größer als cbSoFar ist, die cbValue hinzugefügt wurde, legen Sie fMoreExists auf 0x00000001 \_ \_ \_ fest, andernfalls auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4527">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="cc80c-4528">Antworten auf den Client mit der CPMFetchValueOut-Nachricht</span><span class="sxs-lookup"><span data-stu-id="cc80c-4528">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="cc80c-4529">3.1.5.2.9 Empfangen einer CPMGetNotify-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4529">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="cc80c-4530">Wenn der Server eine CPMGetNotify-Nachricht von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4530">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4531">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4531">Check if the client has query associated with it.</span></span> <span data-ttu-id="cc80c-4532">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4532">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4533">Wenn seit der letzten CPMSendNotifyOut-Nachricht für diesen Client keine Änderungen am Abfrageresultset vorgenommen wurden oder die Abfrage derzeit nicht auf Änderungen im Resultset überwacht wird, MUSS der Server mit der CPMGetNotify-Meldung antworten und mit der Überwachung der Abfrage auf Änderungen im Resultset beginnen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4533">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="cc80c-4534">Wenn das Abfrageergebnisset zu einem späteren Zeitpunkt geändert wird, MUSS der Server genau eine CPMSendNotifyOut-Nachricht an den Client senden und DIE Änderung im \_ Feld watchNotify angeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4534">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="cc80c-4535">Wenn seit der letzten CPMSendNotifyOut-Nachricht Änderungen am Abfrageresultset vorgenommen wurden, MUSS der Server mit CPMSendNotifyOut antworten und DIE Änderung im \_ Feld watchNotify angeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4535">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="cc80c-4536">Beachten Sie, dass DBWATCHNOTIFY ROWSCHANGED bei vielen Änderungen an den Abfrageergebnissen \_ Priorität hat (d. h., wenn die Abfrage durchgeführt, erneut ausgeführt und dann die Anzahl der Zeilen geändert wurde und die Abfrage erneut durchgeführt wurde, lautet das gemeldete Ereignis DBWATCHNOTIFY \_ ROWSCHANGED).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4536">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="cc80c-4537">3.1.5.2.10 Empfangen einer CPMGetApproximatePositionIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4537">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="cc80c-4538">Wenn der Server eine CPMGetApproximatePositionIn-Nachrichtenanforderung vom Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4538">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4539">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4539">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cc80c-4540">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4540">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4541">Überprüfen Sie, ob das Cursorhandle, das Kapitelhandle und das übergebene Lesezeichenhandle in den entsprechenden Listen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4541">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="cc80c-4542">Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4542">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cc80c-4543">Suchen Sie eine Zeile, die dem Lesezeichenhandle in den Abfrageergebnissen zugeordnet ist, und ermitteln Sie die Position der Zeile im Rowset, auf die das Kapitelhandle verweist, und bestimmen Sie den Zähler und Nenner für die Position.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4543">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="cc80c-4544">Beachten Sie, dass das entsprechende Kapitel das Haupt rowset der Abfrage ist, wenn das Kapitelhand handle DB \_ NULL \_ HCHAPTER ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4544">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="cc80c-4545">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4545">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="cc80c-4546">Reagieren Sie mit einer CPMFetchValueOut-Nachricht auf den Client.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4546">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="cc80c-4547">3.1.5.2.11 Empfangen einer CPMCompareBmkIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4547">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="cc80c-4548">Wenn der Server eine CPMCompareBmkIn-Nachrichtenanforderung vom Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4548">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4549">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4549">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cc80c-4550">Wenn dies nicht der Fall ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4550">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4551">Überprüfen Sie, ob das Cursorhandles, das Kapitelhandles und die übergebenen Lesezeichenhandles in den entsprechenden Listen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4551">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="cc80c-4552">Wenn dies nicht der Fall ist, MUSS der Server den Fehler E \_ FAIL (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4552">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cc80c-4553">Bereiten Sie eine CPMCompareBmkOut-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4553">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="cc80c-4554">Wenn Lesezeichenhandles gleich sind, \_ muss dwComparison AUF DBCOMPARE EQ festgelegt \_ werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4554">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="cc80c-4555">Wenn eines der Lesezeichenhandles DBBMK FIRST oder DBBMK LAST ist, muss \_ \_ \_ dwComparison auf DBCOMPARE NE festgelegt \_ werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4555">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="cc80c-4556">Andernfalls MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4556">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="cc80c-4557">Suchen von Zeilen, auf die von jedem Lesezeichenhand handle in den Abfrageergebnissen verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="cc80c-4557">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="cc80c-4558">Wenn sich eine der Zeilen nicht im Kapitel befindet, das durch das Kapitelhand handle in CPMCompareBmkIn angegeben ist, muss \_ dwComparison auf DBCOMPARE \_ NOTCOMPARABLE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4558">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="cc80c-4559">Wenn sich beide Zeilen im selben Kapitel befinden, muss der Server andernfalls eine ungefähre Position dieser Zeilen im Rowset herstellen, auf das durch das Handle dieses Kapitels verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4559">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="cc80c-4560">Anschließend MÜSSEN Positionswerte verglichen und dwComparison auf DBCOMPARE LT festgelegt werden, wenn die Position der ersten Zeile kleiner als die Position der zweiten Zeile ist. Andernfalls MUSS \_ \_ \_ dwComparison auf DBCOMPARE GT festgelegt \_ werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4560">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="cc80c-4561">Antworten Sie dem Client mit einer ausgefüllten CPMCompareBmkOut-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4561">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="cc80c-4562">3.1.5.2.12 Empfangen einer CPMRestartPositionIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4562">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="cc80c-4563">Wenn der Server die CPMRestartPositionIn-Nachrichtenanforderung vom Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4563">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4564">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4564">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cc80c-4565">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4565">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4566">Überprüfen Sie, ob das Cursorhandle und das übergebene Kapitelhandle in den entsprechenden Listen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4566">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="cc80c-4567">Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4567">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cc80c-4568">Bewegen Sie den Cursor an den Anfang des Kapitels, der durch das Kapitelhandle identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4568">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="cc80c-4569">Beachten Sie, dass das entsprechende Kapitel das Hauptrowset der Abfrage ist, wenn das Kapitelhandle DB \_ NULL \_ HCHAPTER ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4569">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="cc80c-4570">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4570">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="cc80c-4571">Reagieren Sie auf den Client mit einer CPMRestartPositionIn-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4571">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="cc80c-4572">3.1.5.2.13 Empfangen einer CPMFreeCursorIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4572">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="cc80c-4573">Wenn der Server eine CPMFreeCursorIn-Nachrichtenanforderung vom Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4573">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4574">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4574">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cc80c-4575">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4575">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cc80c-4576">Überprüfen Sie, ob das übergebene Cursorhandle in der Liste der Cursorhandles des Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4576">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="cc80c-4577">Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4577">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cc80c-4578">Geben Sie den Cursor und die zugehörigen Ressourcen (eine vollständige Liste finden Sie in Abschnitt 3.1.1) für dieses Cursorhandle frei.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4578">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="cc80c-4579">Entfernen Sie den Cursor aus der Liste der Cursor für diesen Client.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4579">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="cc80c-4580">Antworten Sie mit einer CPMFreeCursorOut-Nachricht, und legen Sie das \_ Feld cCursorsRemaining mit der Anzahl der verbleibenden Cursor fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4580">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="cc80c-4581">in der Liste dieses Clients.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4581">in this client's list.</span></span>
-   <span data-ttu-id="cc80c-4582">Wenn für diesen Client keine Cursor mehr vorhanden sind, MUSS der Server die Abfrage und die zugehörigen Ressourcen freigeben (siehe Abschnitt 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4582">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="cc80c-4583">3.1.5.2.14 Empfangen einer CPMDisconnect-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4583">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="cc80c-4584">Wenn der Server eine CPMDisconnect-Nachrichtenanforderung vom Client empfängt, MUSS der Server den Client aus der Liste der verbundenen Clients entfernen und alle dem Client zugeordneten Ressourcen frei geben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4584">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="cc80c-4585">3.1.6 Timerereignisse</span><span class="sxs-lookup"><span data-stu-id="cc80c-4585">3.1.6 Timer Events</span></span>

<span data-ttu-id="cc80c-4586">Keine.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4586">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="cc80c-4587">3.1.7 Andere lokale Ereignisse</span><span class="sxs-lookup"><span data-stu-id="cc80c-4587">3.1.7 Other Local Events</span></span>

<span data-ttu-id="cc80c-4588">Wenn der Server beendet wird, MUSS er zuerst in den Zustand "Herunterfahren" überwechseln.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4588">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="cc80c-4589">Er MUSS dann die Lauschfunktion an der Pipe beenden, andere implementierungsspezifische Herunterfahrensaufgaben ausführen und dann in den Zustand "Beendet" überwechseln.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4589">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="cc80c-4590">3.2 Clientdetails</span><span class="sxs-lookup"><span data-stu-id="cc80c-4590">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="cc80c-4591">3.2.1 Abstraktes Datenmodell</span><span class="sxs-lookup"><span data-stu-id="cc80c-4591">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="cc80c-4592">Im folgenden Abschnitt werden die Vom Content Indexing Service Protocol-Client verwalteten Daten und Zustand angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4592">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="cc80c-4593">Mit den bereitgestellten Daten soll das Verhalten des Protokolls erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4593">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="cc80c-4594">In diesem Abschnitt ist nicht die Einhaltung dieses Modells durch Implementierungen vorschrieben, solange ihr externes Verhalten mit dem in diesem Dokument beschriebenen Verhalten konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4594">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="cc80c-4595">Ein Client hat den folgenden abstrakten Zustand:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4595">A client has the following abstract state:</span></span>

-   <span data-ttu-id="cc80c-4596">**Letzte gesendete Nachricht:** Eine Kopie der letzten nachricht, die an den Server gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4596">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="cc80c-4597">**Aktueller Eigenschaftswert:** Ein Teilwert einer verzögerten Eigenschaft, die gerade abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4597">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="cc80c-4598">**Aktuelle empfangene Bytes:** Die Anzahl der bytes, die bisher für den aktuellen Eigenschaftswert empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4598">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="cc80c-4599">**Named Pipe-Verbindungsstatus:** Eine Verbindung mit dem Server</span><span class="sxs-lookup"><span data-stu-id="cc80c-4599">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="cc80c-4600">3.2.2 Timer</span><span class="sxs-lookup"><span data-stu-id="cc80c-4600">3.2.2 Timers</span></span>

<span data-ttu-id="cc80c-4601">Es sind keine Protokollzeiter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4601">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="cc80c-4602">3.2.3 Initialisierung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4602">3.2.3 Initialization</span></span>

<span data-ttu-id="cc80c-4603">Es werden keine Aktionen durchgeführt, bis eine Anforderung auf höherer Ebene empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4603">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="cc80c-4604">3.2.4 Higher-Layer ausgelöste Ereignisse</span><span class="sxs-lookup"><span data-stu-id="cc80c-4604">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="cc80c-4605">Wenn eine Anforderung von einer höheren Ebene empfangen wird, MUSS der Client unter Verwendung der in Abschnitt 2.1 angegebenen Details eine Named Pipe-Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4605">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="cc80c-4606">Wenn dies nicht möglich ist, MUSS bei der Anforderung der höheren Ebene ein Fehler aufgetreten sein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4606">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="cc80c-4607">Das heißt, bei einem Verbindungsfehler liegt es in der Verantwortung der höheren Ebene, dies bei Bedarf erneut zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4607">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="cc80c-4608">Ein Header MUSS mit feldern vorangestellt werden, wie in Abschnitt 2.2.2 angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4608">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="cc80c-4609">Für Nachrichten, für die angegeben wird, dass eine Prüfsumme ungleich 0 (null) erforderlich ist, MUSS der \_ ulChecksum-Wert wie folgt berechnet werden:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4609">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="cc80c-4610">Der Inhalt der Nachricht nach dem \_ ulReserved2-Feld im Nachrichtenheader MUSS als Sequenz von 32-Bit-Ganzzahlen interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4610">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="cc80c-4611">Der Client MUSS die Summe der numerischen Werte berechnen, die von diesen ganzen Zahlen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4611">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="cc80c-4612">Berechnen Sie den bitweisen XOR dieses Werts mit 0x59533959.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4612">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="cc80c-4613">Subtrahieren Sie den von msg angegebenen Wert \_ von dem Wert, der sich aus dem bitweisen XOR ergibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4613">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="cc80c-4614">3.2.4.1 Katalogverwaltung des Remoteindizierungsdiensts</span><span class="sxs-lookup"><span data-stu-id="cc80c-4614">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="cc80c-4615">Jede Nachricht wird durch eine Anforderung von der höheren Ebene ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4615">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="cc80c-4616">Es wird keine Nachrichtensequenz vom Client für CISP-Nachrichtenanforderungen für die Remoteverwaltung von Katalogen erzwungen, aber (mit Ausnahme einer CPMSetCatStateIn-Nachricht) antwortet der Server nur dann mit Erfolg, wenn der Client zuvor über eine CPMConnectIn-Nachricht eine Verbindung hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4616">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="cc80c-4617">3.2.4.1.1 Senden einer CPMCiStateInOut-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4617">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="cc80c-4618">In der Regel fordert die höhere Ebene den Protokollclient auf, eine CPMCiStateInOut-Nachricht zu senden, wenn informationen zum Indizieren von Diensten auf dem Server erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4618">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="cc80c-4619">Wenn der Client aufgefordert wird, diese Nachricht zu senden, MUSS er folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4619">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4620">Senden Sie eine CPMCiStateInOut-Nachricht wie in Abschnitt 2.2.3.1 angegeben an den Server.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4620">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="cc80c-4621">Warten Sie, bis die CPMCiStateInOut-Nachricht vom Server empfangen wird, und verwerfen Sie automatisch alle anderen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4621">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="cc80c-4622">Melden Sie den Wert des \_ Statusfelds der Antwort, und wenn dies erfolgreich war, wird die Informationsstruktur wieder auf die höhere Ebene zurückgestellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4622">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="cc80c-4623">3.2.4.1.2 Senden einer CPMSetCatStateIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4623">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="cc80c-4624">In der Regel fordert die höhere Ebene den Protokollclient auf, eine CPMSetCatStateIn-Nachricht zu senden, wenn Informationen zu einem Katalog oder einem Katalog erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4624">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="cc80c-4625">Für diese Nachricht muss die höhere Ebene dem Protokollclient einen Wert für dwNewState und bei Bedarf den Namen \_ des Katalogs bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4625">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="cc80c-4626">Wenn der Client aufgefordert wird, diese Nachricht zu senden, MUSS er folgende Schritte unternehmen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4626">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4627">Senden Sie eine CPMSetCatStateIn-Nachricht wie in 2.2.3.2 angegeben an den Server.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4627">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="cc80c-4628">Warten Sie auf den Empfang einer CPMSetCatStateOut-Nachricht vom Server, und verwerfen Sie alle anderen Nachrichten im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4628">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="cc80c-4629">Melden Sie den Wert des Statusfelds der Antwort, und wenn die Antwort erfolgreich war, wird \_ \_ dwOldState wieder an die höhere Ebene zurückgesagt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4629">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="cc80c-4630">3.2.4.1.3 Senden einer CPMUpdateDocumentsIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4630">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="cc80c-4631">Die höhere Ebene fordert in der Regel dazu auf, diese Nachricht zu senden, wenn entweder Dokumente im vorhandenen Pfad aktualisiert oder dem Index ein neuer Dateipfad hinzugefügt werden muss.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4631">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="cc80c-4632">Daher besteht die höhere Ebene in der Bereitstellung des Pfads und Typs einer Überprüfung, die wie in Abschnitt 2.2.3.4 angegeben ist, wobei ein inkrementelles oder vollständiges Update für vorhandene Pfade und eine neue Initialisierung für neue Pfade bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4632">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="cc80c-4633">Um die Anforderung auf höherer Ebene zu bedienen, MUSS der Client Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4633">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4634">Senden Sie eine CPMUpdateDocumentsIn-Nachricht wie in Abschnitt 2.2.3.4 angegeben an den Server.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4634">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="cc80c-4635">Warten Sie auf den Empfang der CPMUpdateDocumentsIn-Nachricht vom Server, und verwerfen Sie alle anderen Nachrichten im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4635">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="cc80c-4636">Melden Sie den Wert des \_ Statusfelds der Antwort an die höhere Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4636">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="cc80c-4637">3.2.4.1.4 Senden einer CPMForceMergeIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4637">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="cc80c-4638">In der Regel fordert die höhere Ebene an, diese Nachricht zu senden, wenn die Abfrageleistung verbessert werden muss oder dies Teil der geplanten Wartung des Indizierungsdiensts ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4638">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="cc80c-4639">Um die höhere Ebene zu bedienen, MUSS der Client Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4639">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4640">Senden Sie die CPMForceMergeIn-Nachricht gemäß Abschnitt 2.2.3.5 an den Server.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4640">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="cc80c-4641">Warten Sie auf den Empfang einer CPMUpdateDocumentsIn-Nachricht vom Server, und verwerfen Sie alle anderen Nachrichten im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4641">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="cc80c-4642">Melden Sie den Wert des \_ Statusfelds der Antwort an die höhere Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4642">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="cc80c-4643">3.2.4.2 Katalogabfragemeldungen des Remoteindizierungsdiensts</span><span class="sxs-lookup"><span data-stu-id="cc80c-4643">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="cc80c-4644">Mit Ausnahme von CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut besteht eine 1:1-Beziehung zwischen CISP-Nachrichten und Anforderungen höherer Ebenen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4644">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="cc80c-4645">Für die beiden oben genannten Ausnahmen können mehrere Nachrichten vom Client generiert werden, um entweder die Größenanforderungen zu erfüllen oder eine vollständige Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4645">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="cc80c-4646">Die höhere Ebene verfolgt in der Regel alle abfragespezifischen Informationen (z. B. geöffnete Cursorhandles, rechtliche Werte für Lesezeichen- und Kapitelhandles, wid-Werte für verzögerte Eigenschaftswerte usw.) und verfolgt auch, ob sich der Client in einem verbundenen Zustand befindet, aber dies wird vom Client in keiner Weise erzwungen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4646">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="cc80c-4647">Zur Veranschaulichung veranschaulicht der Clientteil des Diagramms in Abschnitt 3 diese Sequenz für eine einfache Indizierungsdienstabfrage.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4647">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="cc80c-4648">3.2.4.2.1 Senden einer CPMConnectIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4648">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="cc80c-4649">Diese Nachricht ist in der Regel die erste Anforderung von der höheren Ebene (als ob der Client nicht verbunden ist, schlägt der Server die meisten Nachrichten mit Ausnahme von CPMSetCatStateIn fehl).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4649">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="cc80c-4650">Die höhere Ebene stellt dem Protokollclient informationen bereit, die für die Verbindungsherstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4650">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="cc80c-4651">Um die höhere Ebene zu bedienen, MUSS der Client folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4651">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4652">Geben Sie die Nachricht mithilfe von Informationen ein, die der Client auf höherer Ebene (siehe Abschnitt 2.2.3.6) in \_ iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 und aPropertySet bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4652">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="cc80c-4653">Legen Sie \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet und cExtPropSet wie in 2.2.3.6 angegeben fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4653">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="cc80c-4654">Legen Sie die Prüfsumme im \_ UlChecksum-Feld fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4654">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="cc80c-4655">Senden Sie die CPMConnectIn-Nachricht an den Server.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4655">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="cc80c-4656">Warten Sie, bis sie eine CPMConnectOut-Nachricht vom Server zurückerlangt, und verwerfen Sie automatisch alle anderen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4656">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="cc80c-4657">Melden Sie den Wert des \_ Statusfelds der Antwort, und wenn dies erfolgreich war, wird die \_ serverVersion wieder auf die höhere Ebene zurückgeleitet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4657">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="cc80c-4658">Zu Informationszwecken wird erwartet, dass höhere Ebenen bei erfolgreicher Verbindung in der Regel die folgenden Aktionen ausführen, diese jedoch nicht vom CISP-Client erzwungen werden:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4658">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="cc80c-4659">Verwenden von Katalogverwaltungsmeldungen des Remoteindizierungsdiensts für administrative Aufgaben</span><span class="sxs-lookup"><span data-stu-id="cc80c-4659">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="cc80c-4660">Verwenden Sie eine CPMCreateQueryIn-Anforderung, um eine Suchabfrage zum Abrufen von Ergebnissen aus dem Katalog zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4660">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="cc80c-4661">3.2.4.2.2 Senden einer CPMCreateQueryIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4661">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="cc80c-4662">Die höhere Ebene stellt in der Regel Informationen für die Abfrageerstellung zur Verfügung, sobald der Protokollclient verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4662">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="cc80c-4663">Auf der höheren Ebene werden dem Client Einschränkungen festgelegt, Spalten festgelegt, Sortierreihenfolgeregeln und Kategorisierungssatz (jede kann weggelassen werden), Rowseteigenschaften und Eigenschaften-ID-Zuordnungsstruktur.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4663">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="cc80c-4664">Wenn diese Anforderung von einer höheren Ebene empfangen wird, MUSS der Client Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4664">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4665">Bereiten Sie ein CPMCreateQueryOut wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4665">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="cc80c-4666">Wenn ein Spaltensatz vorhanden ist, legen Sie CColumnsSetPreset auf 0x01 und füllen Sie das Feld ColumnsSet aus.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4666">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="cc80c-4667">Wenn Einschränkungen vorhanden sind, legen Sie CRestrictionPresent auf 0x01 und füllen Sie das Feld Einschränkung aus.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4667">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="cc80c-4668">Wenn eine Sortierreihenfolge vorhanden ist, füllen Sie das Feld SortSet aus.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4668">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="cc80c-4669">Wenn ein Kategorisierungssatz vorhanden ist, legen Sie CSortSetPresent auf 0x01 und füllen Sie das Feld CategorizationSet aus.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4669">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="cc80c-4670">Legen Sie die restlichen Felder wie in 2.2.3.8 angegeben fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4670">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="cc80c-4671">Berechnen \_ Sie das ulCheckSum-Feld im Header.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4671">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="cc80c-4672">Senden Sie die Nachricht CPMCreateQueryIn an den Server.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4672">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="cc80c-4673">Warten Sie auf den Empfang der CPMCreateQueryOut-Nachricht (siehe Details in Abschnitt 3.2.5.1.1), und verwerfen Sie alle anderen Nachrichten im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4673">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="cc80c-4674">Melden Sie den Wert des Statusfelds der Antwort und, falls erfolgreich, das Array von Cursorhandles und informative boolesche Werte \_ (wie in 2.2.3.9 angegeben) zurück zur höheren Ebene.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4674">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="cc80c-4675">3.2.4.2.3 Senden einer CPMSetBindingsIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4675">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="cc80c-4676">In der Regel werden von der höheren Ebene Bindungen für jede Spalte festgelegt, die in den Zeilen zurückgegeben wird, wenn sie bereits über ein gültiges Cursorhandl verfügt (siehe Abschnitt 3.2.5.1.1, nachdem CPMCreateQueryOut erfolgreich empfangen wurde).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4676">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="cc80c-4677">Der höhere Wert wird erwartet, um ein Array von CTableColumn-Strukturen bereitzustellen, wie in Abschnitt 2.2.4.31 angegeben, für das Feld aColumns und ein gültiges Cursorhandle.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4677">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="cc80c-4678">Wenn diese Anforderung von der höheren Ebene empfangen wird, MUSS der Client folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4678">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4679">Berechnen Sie die Anzahl der CTableColumn-Strukturen im Array aColumns, und legen Sie das Feld cColumns auf diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4679">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="cc80c-4680">Berechnen Sie die Gesamtgröße der Felder cColumns und aColumns in Bytes, und legen Sie das \_ Feld cbBindingDesc auf diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4680">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="cc80c-4681">Legen Sie die angegebenen Felder in der CPMSetBindingsIn-Nachricht auf die Werte fest, die von der höheren Anwendungsschicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4681">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="cc80c-4682">Legen Sie das \_ UlChecksum-Feld auf den Wert fest, der gemäß Abschnitt 3.2.5 berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4682">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="cc80c-4683">Senden Sie die fertige CPMSetBindignsIn-Nachricht an den Server.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4683">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="cc80c-4684">Warten Sie, bis eine CPMSetBindingsIn-Nachricht vom Server empfangen wird, und verwerfen Sie andere Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4684">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="cc80c-4685">Geben Sie den Status aus dem \_ Statusfeld der Antwort auf die höhere Ebene an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4685">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="cc80c-4686">Zu Informationszwecken wird erwartet, dass höhere Ebenen in der Regel einen Client zum Senden einer CPMGetRowsIn-Nachricht auffordern, dies wird jedoch nicht vom Content Indexing Service-Protokoll erzwungen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4686">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="cc80c-4687">3.2.4.2.4 Senden einer CPMGetRowsIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4687">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="cc80c-4688">Wenn die höhere Ebene Zeileninformationen empfängt, stellt sie dem Protokollclient einen gültigen Cursor und ein gültiges Kapitelhandle zur Verfügung und gibt eine entsprechende Suchbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4688">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="cc80c-4689">In der Regel wird davon ausgegangen, dass eine höhere Ebene über einen gültigen Cursor und/oder ein gültiges Kapitelhandle verfügt und die Bindungen mit der CPMSetBindingsIn-Nachricht festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4689">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="cc80c-4690">Für den Zugriff auf das Rowset in einem Kapitel wird auf der höheren Ebene ein Kapitelhandle verwendet, das vom Server in einer früheren CPMGetRowsOut-Nachricht empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4690">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="cc80c-4691">Wenn diese Anforderung von der höheren Ebene empfangen wird, MUSS der Client folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4691">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4692">Bestimmen Sie, welcher ganzzahlige Wert ohne Vorzeichen für das feld cbReadBuffer angegeben werden \_ soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4692">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="cc80c-4693">Um diesen Wert zu bestimmen, MUSS der Client den maximal zulässigen Wert aus folgenden Werten übernehmen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4693">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="cc80c-4694">Tausendfacher Wert des \_ Felds c RowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4694">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="cc80c-4695">Der Wert von \_ cbRowWidth, auf das nächste 512-Byte-Vielfache aufgerundet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4695">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="cc80c-4696">Nehmen Sie den höheren dieser beiden Werte bis zum Grenzwert von 16.000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4696">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="cc80c-4697">In Fällen, in denen eine einzelne Zeile größer als 16.000 ist, kann der Server keine Ergebnisse an diese Abfrage zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4697">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="cc80c-4698">Geben Sie eine Clientbasis für Zeilendaten variabler Größe im Clientadressenraum im \_ Feld ulClientBase an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4698">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="cc80c-4699">*Windows-Verhalten: Bei einem 32-Bit-Client, der mit einem 32-Bit-Server spricht, oder einem 64-Bit-Client, der mit einem 64-Bit-Server spricht, wird dieser Wert auf eine Speicheradresse des empfangenden Puffers im Anwendungsprozess festgelegt. Dadurch können Zeiger, die im Rows-Feld von CPMGetRowsOut empfangen werden, richtige Speicherzeige in einem Clientanwendungsprozess sein. Andernfalls wird sie auf 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="cc80c-4699">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="cc80c-4700">Berechnen Sie die Größe der Suchbeschreibung, und legen Sie sie im \_ Feld cbSeek fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4700">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="cc80c-4701">Legen Sie den Wert von cbReserved (der als Offset für Zeilenstart fungieren würde) auf den Wert \_ cbSeek plus 0x14.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4701">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="cc80c-4702">Senden Sie eine CPMConnectIn-Nachricht wie in 2.2.3.15 angegeben an den Server.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4702">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="cc80c-4703">3.2.4.2.5 Senden einer CPMFetchValueIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4703">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="cc80c-4704">Wenn der Client eine CPMGetRowsOut-Antwort vom Server empfängt, bei der das Feld Status der Spalte auf StatusDeferred (0x01) festgelegt ist, bedeutet dies, dass der Eigenschaftswert nicht im Feld Zeilen der CPMGetRowsOut-Nachricht enthalten war.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4704">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="cc80c-4705">In diesem Fall fordert die höhere Ebene den Protokollclient in der Regel auf, den Wert mithilfe der CPMFetchValueIn-Nachricht abzurufen, und stellt den PropSpec- und wid-Wert für eine verzögerte Eigenschaft zur Anwendung, die der Protokollclient in der ersten \_ CPMFetchValueIn-Nachricht verwenden muss.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4705">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="cc80c-4706">Wenn dies die erste CPMFetchValueIn-Nachricht ist, die der Client gesendet hat, um die angegebene Eigenschaft an fordern zu können, MUSS der Client folgende Schritte unternehmen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4706">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4707">Legen Sie alle Felder in einer Nachricht wie in Abschnitt 2.2.3.19 angegeben fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4707">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="cc80c-4708">Legen \_ Sie cbSoFar auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4708">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="cc80c-4709">Legen Sie Aktuelle empfangene Bytes auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4709">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="cc80c-4710">Senden Sie die CPMFetchValueIn-Nachricht an den Server.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4710">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="cc80c-4711">3.2.4.2.6 Senden einer CPMFreeCursorIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc80c-4711">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="cc80c-4712">Sobald die höhere Ebene die Suchabfrage nicht mehr verwendet, kann sie die Ressourcen auf dem Server frei geben, indem der Client aufgefordert wird, eine CPMFreeCursorIn-Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4712">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="cc80c-4713">Wenn diese Anforderung empfangen wird, MUSS der Client eine CPMFreeCursorIn-Nachricht gemäß 2.2.3.28 an den Server senden, die das von der oberen Ebene angegebene Handle enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4713">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="cc80c-4714">3.2.4.2.7 Senden einer CPMDisconnect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="cc80c-4714">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="cc80c-4715">Wenn die höhere Ebene keine Weiteren Abfragen für den Indizierungsdienst aufnimmt, fordert die Anwendung möglicherweise an, dass der Client eine CPMDisconnect-Nachricht an den Server sendet, um weitere Serverressourcen frei zu machen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4715">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="cc80c-4716">Wenn diese Abfrage empfangen wird, MUSS der Client die Nachricht einfach wie angefordert senden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4716">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="cc80c-4717">Es gibt keine Antwort vom Server auf diese Meldung.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4717">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="cc80c-4718">3.2.5 Nachrichtenverarbeitungs- und Sequenzierungsregeln</span><span class="sxs-lookup"><span data-stu-id="cc80c-4718">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="cc80c-4719">Wenn der Client eine Meldungsantwort vom Server empfängt, MUSS der Client die Zuletzt gesendete Nachricht verwenden, um zu bestimmen, ob die vom Server empfangene Nachricht die vom Client erwartete Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4719">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="cc80c-4720">Alle Nachrichten mit \_ msg-Feld, die sich von dem in Letzte Sendenachricht unterscheiden, MÜSSEN ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4720">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="cc80c-4721">3.2.5.1 Empfangen einer CPMCreateQueryOut-Antwort</span><span class="sxs-lookup"><span data-stu-id="cc80c-4721">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="cc80c-4722">Wenn der Client eine CPMCreateQueryOut-Meldungsantwort vom Server empfängt, MUSS der Client den Status zurückgeben \_ und (wenn der Status erfolgreich ist) Cursorwerte zurück auf eine höhere Ebene verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4722">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="cc80c-4723">Alle weiteren Aktionen liegen bis zur höheren Ebene.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4723">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="cc80c-4724">Da die höhere Ebene die Abfragestruktur kennt, wird immer erwartet, dass die richtige Anzahl von Cursorhandles in der CPMCreateOueryOut-Nachricht zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4724">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="cc80c-4725">Die Cursorhandles werden in der folgenden Reihenfolge zurückgegeben: Das erste Handle ist für das nicht gekachelte Rowset, das zweite für das erste Kapitelrowset (dies ist die Gruppierung der Ergebnisse basierend auf der ersten Kategorie, die im Feld CategorizationSet der CPMCreateQueryIn-Nachricht angegeben ist).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4725">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="cc80c-4726">Zu Informationszwecken wird erwartet, dass höhere Ebenen die folgenden Aktionen ausführen können, diese werden jedoch nicht vom CISP-Client erzwungen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4726">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="cc80c-4727">Verwenden Sie CPMSetBindingsIn, um Bindungen für einzelne Spalten festzulegen und nachfolgende Aktionen für den Abfragepfad durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4727">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="cc80c-4728">Verwenden Sie CPMGetQueryStatusIn, um den Ausführungsstatus einer Abfrage zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4728">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="cc80c-4729">Verwenden Sie CPMRatioFinishedIn, um den Abschlussprozentsatz der Abfrage anzufordern.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4729">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="cc80c-4730">3.2.5.2 Empfangen einer CPMGetRowsOut-Antwort</span><span class="sxs-lookup"><span data-stu-id="cc80c-4730">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="cc80c-4731">Wenn der Client eine CPMGetRowsOut-Meldungsantwort vom Server empfängt, MUSS der Client folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4731">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4732">Überprüfen Sie, ob \_ das Statusfeld im Header auf Erfolg oder Fehler hinweist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4732">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="cc80c-4733">Wenn der \_ Statuswert STATUS \_ BUFFER TOO \_ SMALL (0xC0000023) ist, MUSS der Client den Status \_ Letzte gesendete Nachricht überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4733">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="cc80c-4734">Wenn sie keine CPMGetRowsIn-Nachricht enthält, MUSS die empfangene Nachricht automatisch ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4734">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="cc80c-4735">Andernfalls MUSS der Client eine neue CPMGetRowsIn-Nachricht mit allen Feldern senden, die mit dem gespeicherten identisch sind, mit der Ausnahme, dass cbReadBuffer um 512 erhöht werden muss (jedoch nicht größer als \_ 0x4000).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4735">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="cc80c-4736">Wenn \_ status status is STATUS BUFFER TOO SMALL \_ (0xC0000023) and Last Message Sent already has \_ \_ \_ cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4736">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="cc80c-4737">Wenn der Statuswert ein anderer Fehlerwert ist, MUSS der Client den Fehler \_ bis zur höheren Ebene angeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4737">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="cc80c-4738">Wenn der Statuswert auf Erfolg hinweist, MÜSSEN die Ergebnisse bis zur höheren Ebene angegeben werden, die die Informationen angibt, und weitere Aktionen bis zur \_ höheren Ebene.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4738">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="cc80c-4739">Zu Informationszwecken wird erwartet, dass höhere Ebenen in der Regel die folgenden Aktionen ausführen, diese werden jedoch nicht vom Content Indexing Service Protocol-Client erzwungen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4739">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="cc80c-4740">Wenn die Werte in Zeilen die Dokument-IDs darstellen, werden sie von Kapiteln oder Lesezeichenhandles auf der höheren Ebene in der Regel für die Verwendung in nachfolgenden Vorgängen gespeichert, die gültige Dokument-IDs, Kapitel- oder Lesezeichenhandles umfassen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4740">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="cc80c-4741">In der höheren Ebene werden die Daten aus Zeilenwerten in der Regel gespeichert, angezeigt oder anderweitig verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4741">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="cc80c-4742">Für die Werte, die als verzögerte höhere Ebene markiert wurden, ruft den Wert mithilfe von CPMFetchValueIn-Nachrichten ab.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4742">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="cc80c-4743">Die Suchbeschreibung wird auch an eine höhere Ebene zurückgegeben und kann von der höheren Ebene wiederverwendet oder untersucht werden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4743">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="cc80c-4744">Wenn die höhere Ebene kapitel- und lesezeichen, die in den Zeilen empfangen wurden, zu informativen Zwecken Handles angefordert hat, kann dies Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4744">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="cc80c-4745">Verwenden Sie CPMGetQueryStatusExIn, um den Ausführungsstatus einer Abfrage sowie zusätzliche Statusinformationen zu überprüfen, z. B. die Anzahl der gefilterten Dokumente, die zu filternden Dokumente, das Verhältnis der von der Abfrage verarbeiteten Dokumente, die Gesamtzahl der Zeilen in der Abfrage und die Position des Lesezeichens im Rowset.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4745">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="cc80c-4746">Verwenden Sie CPMGetNotify, um anzufordern, dass der Server den Client über Rowsetänderungen benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4746">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="cc80c-4747">Verwenden Sie CPMGetApproximatePositionIn, um die ungefähre Position eines Lesezeichens in einem Kapitel anzufordern.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4747">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="cc80c-4748">Verwenden Sie CPMCompareBmkIn, um einen Vergleich zweier Lesezeichen in einem Kapitel anzufordern.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4748">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="cc80c-4749">Verwenden Sie CPMRestartPositionIn auf dem Server, um die Position des Cursors in den Anfang des Rowsets zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4749">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="cc80c-4750">3.2.5.3 Empfangen einer CPMFetchValueOut-Antwort</span><span class="sxs-lookup"><span data-stu-id="cc80c-4750">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="cc80c-4751">Wenn der Client eine CPMGetRowsOut-Meldungsantwort vom Server empfängt, MUSS der Client folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4751">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="cc80c-4752">Überprüfen Sie, ob das \_ Statusfeld im Header erfolg- oder fehlerbesagend ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4752">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="cc80c-4753">Bei einem Fehler wird die höhere Ebene benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4753">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="cc80c-4754">Fahren Sie andernfalls weiter unten fort.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4754">Otherwise, continue below.</span></span>
-   <span data-ttu-id="cc80c-4755">Überprüfen Sie \_ fValueExist, und wenn diese Einstellung auf 0x00000000 die höhere Ebene benachrichtigen, dass der Wert nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4755">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="cc80c-4756">Andernfalls fügen Sie \_ cbValue-Bytes von vValue an den aktuellen Eigenschaftswert an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4756">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="cc80c-4757">Wenn \_ \_ fMoreExists auf 0x00000001 dann von cbValue empfangene aktuelle Bytes inkrementiert \_ und eine \_ CPMFetchValueIn-Nachricht an den Server gesendet wird, legen Sie \_ cbSoFar auf den Wert von Current Bytes Received, \_ cbPropSpec auf 0 (null) und \_ cbChunk auf die Puffergröße fest, die von der höheren Ebene gewünscht wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4757">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="cc80c-4758">Wenn \_ fMoreExists auf 0x00000000 geben Sie den Eigenschaftswert von Aktueller Eigenschaftswert auf die höhere Ebene an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4758">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="cc80c-4759">3.2.5.4 Empfangen einer CPMFreeCursorOut-Antwort</span><span class="sxs-lookup"><span data-stu-id="cc80c-4759">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="cc80c-4760">Wenn der Client eine erfolgreiche CPMFreeCursorOut-Nachrichtenantwort vom Server empfängt, MUSS der Client den \_ cCursorsRemaining-Wert an die höhere Ebene zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4760">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="cc80c-4761">Die folgenden Informationen dienen nur zu Informationszwecken und werden nicht vom CISP-Client erzwungen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4761">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="cc80c-4762">Von der höheren Ebene wird erwartet, dass sie Cursorhandles nachverfolgt und keine handles verwendet, die bereits frei wurden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4762">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="cc80c-4763">Sobald die Anzahl von cCursorsRemaining gleich 0x00000000 ist, kann die höhere Ebene die Verbindung verwenden, um eine andere Abfrage anzugeben (mithilfe einer \_ CPMCreateQueryIn-Nachricht).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4763">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="cc80c-4764">3.2.6 Timerereignisse</span><span class="sxs-lookup"><span data-stu-id="cc80c-4764">3.2.6 Timer Events</span></span>

<span data-ttu-id="cc80c-4765">Keine.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4765">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="cc80c-4766">3.2.7 Andere lokale Ereignisse</span><span class="sxs-lookup"><span data-stu-id="cc80c-4766">3.2.7 Other Local Events</span></span>

<span data-ttu-id="cc80c-4767">Keine.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4767">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="cc80c-4768">4 Beispiele für Protokolle</span><span class="sxs-lookup"><span data-stu-id="cc80c-4768">4 Protocol Examples</span></span>

-   [<span data-ttu-id="cc80c-4769">4.1 Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4769">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="cc80c-4770">4.2 Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4770">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="cc80c-4771">4.1 Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc80c-4771">4.1 Example 1</span></span>

<span data-ttu-id="cc80c-4772">Im folgenden Beispiel betrachten wir ein Szenario, in dem der Benutzer JOHN auf Computer A die Größe von Dateien, die das Wort "Microsoft" enthalten, aus dem Satz von Dokumenten abrufen möchte, die auf Server X im Katalog SYSTEM gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4772">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="cc80c-4773">Nehmen wir an, dass Computer A ein 32-Bit-Betriebssystem Windows XP und Computer X ein 32-Bit-Betriebssystem von Windows Server 2003 verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4773">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="cc80c-4774">Der Benutzer startet eine Suchanwendung und gibt die Suchabfrage ein.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4774">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="cc80c-4775">Die Anwendung übergibt die Suchabfrage wiederum an den Protokollclient.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4775">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="cc80c-4776">Der Protokollclient stellt eine Verbindung mit dem Indizierungsserver X ein. Der Protokollclient verwendet die Named Pipe \\ Pipe \\ CI \_ SKADS, um über SMB eine Verbindung mit dem Server X herzustellen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4776">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="cc80c-4777">Der Protokollclient bereitet dann eine CPMConnectIn-Nachricht mit den folgenden Werten vor:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4777">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="cc80c-4778">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4778">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4779">**\_ msg** ist auf 0x000000C8, was angibt, dass es sich um eine CPMConnectIn-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4779">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="cc80c-4780">**\_ status** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4780">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cc80c-4781">**\_ ulChecksum** enthält die Prüfsumme, die wie in Abschnitt 3.2.4 angegeben berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4781">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="cc80c-4782">**\_ ulReserved2** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4782">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="cc80c-4783">Der Text der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4783">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4784">**\_ iClientVersion** ist auf 0x00000008, was angibt, dass der Server das Prüfsummenfeld überprüfen soll.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4784">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="cc80c-4785">**\_ fClientIsRemote** ist auf 0x00000001 festgelegt, was angibt, dass der Server ein Remoteserver ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4785">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="cc80c-4786">**\_ cbBlob1** wird auf die Größe der Felder cPropSet, PropertySet1 und PropertySet2 in Bytes festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4786">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="cc80c-4787">**\_ cbBlob2** ist auf 0x00000004 festgelegt (d. h. keine zusätzlichen Eigenschaftensätze).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4787">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="cc80c-4788">**MachineName** ist auf A festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4788">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="cc80c-4789">**UserName** ist auf JOHN festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4789">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="cc80c-4790">**cPropSets** ist auf 0x00000002 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4790">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="cc80c-4791">**Das PropertySet1-Feld** ist vom Typ CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4791">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="cc80c-4792">Die CDbPropSet-Struktur, die das PropertySet1-Feld umfasst, wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4792">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="cc80c-4793">**Das Feld GuidPropSet** ist auf A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4793">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="cc80c-4794">Das Feld **cProperties** ist auf 0x00000004 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4794">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="cc80c-4795">Das Feld **aProps** ist ein Array von CDbProp-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4795">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="cc80c-4796">Für das **aProps \[ \] 0-Element:**</span><span class="sxs-lookup"><span data-stu-id="cc80c-4796">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="cc80c-4797">**PropId** ist auf 0x00000002 (DBPROP \_ CI CATALOG \_ \_ NAME) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4797">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="cc80c-4798">**DBPROPOPTIONS** ist auf 0x0000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4798">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="cc80c-4799">**DBPROPSTATUS** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4799">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cc80c-4800">Für das **ColId-Element:**</span><span class="sxs-lookup"><span data-stu-id="cc80c-4800">For the **ColId** element:</span></span>
                -   <span data-ttu-id="cc80c-4801">**eKind** ist auf 0x00000001 (DBKIND \_ GUID \_ PROPID) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4801">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="cc80c-4802">**GUID** ist NULL (alle Nullen), d. h., der Wert gilt für die Abfrage, nicht nur für eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4802">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="cc80c-4803">**ulID** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4803">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cc80c-4804">Für das **vValue-Element:**</span><span class="sxs-lookup"><span data-stu-id="cc80c-4804">For the **vValue** element:</span></span>
                -   <span data-ttu-id="cc80c-4805">**vType** ist auf 0x001F (VT \_ LPWSTR) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4805">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="cc80c-4806">**vValue** ist auf "SYSTEM", den Namen des gewünschten Katalogs, festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4806">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="cc80c-4807">Für das **aProps \[ \] 1-Element:**</span><span class="sxs-lookup"><span data-stu-id="cc80c-4807">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="cc80c-4808">**PropId** ist auf 0x00000007 (DBPROP \_ CI QUERY \_ \_ TYPE) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4808">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="cc80c-4809">**DBPROPOPTIONS** ist auf 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4809">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="cc80c-4810">**DBPROPSTATUS** ist auf0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4810">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="cc80c-4811">Für das **ColId-Element:**</span><span class="sxs-lookup"><span data-stu-id="cc80c-4811">For the **ColId** element:</span></span>
                -   <span data-ttu-id="cc80c-4812">**eKind** ist auf 0x00000001 (DBKIND \_ GUID \_ PROPID) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4812">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="cc80c-4813">**GUID** ist NULL (alle Nullen), d. h., der Wert gilt für die Abfrage, nicht nur für eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4813">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="cc80c-4814">**ulID** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4814">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cc80c-4815">Für das **vValue-Element:**</span><span class="sxs-lookup"><span data-stu-id="cc80c-4815">For the **vValue** element:</span></span>
                -   <span data-ttu-id="cc80c-4816">**vType** ist auf 0x0003 (VT \_ I4) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4816">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="cc80c-4817">**vValue** ist auf 0x00000000 (CiNormal) festgelegt, was bedeutet, dass es sich um eine reguläre Abfrage handelt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4817">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="cc80c-4818">Für das **aProps \[ \] 2-Element:**</span><span class="sxs-lookup"><span data-stu-id="cc80c-4818">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="cc80c-4819">**PropId** ist auf 0x00000004 (DBPROP \_ CI SCOPE \_ \_ FLAGS) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4819">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="cc80c-4820">**DBPROPOPTIONS** ist auf 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4820">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="cc80c-4821">**DBPROPSTATUS** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4821">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cc80c-4822">Für das **ColId-Element:**</span><span class="sxs-lookup"><span data-stu-id="cc80c-4822">For the **ColId** element:</span></span>
                -   <span data-ttu-id="cc80c-4823">**eKind** ist auf 0x00000001 (DBKIND \_ GUID \_ PROPID) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4823">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="cc80c-4824">**Die GUID** ist NULL (alle Nullen), d. h., der Wert gilt für die Abfrage, nicht nur für eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4824">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="cc80c-4825">**ulID** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4825">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cc80c-4826">Für das **vValue-Element:**</span><span class="sxs-lookup"><span data-stu-id="cc80c-4826">For the **vValue** element:</span></span>
                -   <span data-ttu-id="cc80c-4827">**vType:** 0x1003 (VT \_ VECTOR \| VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="cc80c-4827">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="cc80c-4828">**vValue:** 0x00000001/0x00000001 (ein Element mit dem Wert 1), d. h. Suchunterordner</span><span class="sxs-lookup"><span data-stu-id="cc80c-4828">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="cc80c-4829">Für das **aProps \[ \] 3-Element:**</span><span class="sxs-lookup"><span data-stu-id="cc80c-4829">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="cc80c-4830">**PropId:** 0x00000003 (DBPROP \_ CI \_ INCLUDE \_ SCOPES)</span><span class="sxs-lookup"><span data-stu-id="cc80c-4830">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="cc80c-4831">**DBPROPOPTIONS:** 0x0000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-4831">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="cc80c-4832">**DBPROPSTATUS:** 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-4832">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="cc80c-4833">Für das **ColId-Element:**</span><span class="sxs-lookup"><span data-stu-id="cc80c-4833">For the **ColId** element:</span></span>
                -   <span data-ttu-id="cc80c-4834">**eKind** ist auf 0x00000001 (DBKIND \_ GUID \_ PROPID) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4834">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="cc80c-4835">**GUID** ist NULL (alle Nullen), d. h., der Wert gilt für die Abfrage, nicht nur für eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4835">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="cc80c-4836">**ulID** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4836">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="cc80c-4837">Für das **vValue-Element:**</span><span class="sxs-lookup"><span data-stu-id="cc80c-4837">For the **vValue** element:</span></span>
                -   <span data-ttu-id="cc80c-4838">**vType** ist auf 0x101F (VT \_ VECTOR \| VT \_ LPWSTR) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4838">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="cc80c-4839">**vValue** ist auf 0x00000001/0x00000002/" \\ " (ein Element mit einer 2-Zeichen-NULL-endende Zeichenfolge) festgelegt, was dem Stammbereich entspricht.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4839">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="cc80c-4840">Das **PropertySet2-Feld** ist vom Typ CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4840">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="cc80c-4841">Die CDbPropSet-Struktur, die das PropertySet1-Feld umfasst, wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4841">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="cc80c-4842">**GuidPropSet** ist auf AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4842">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="cc80c-4843">Das Feld **cProperties** ist auf 0x00000001 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4843">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="cc80c-4844">Das Feld **aProps** ist ein Array von CDbProp-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4844">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="cc80c-4845">Für das **aProps \[ \] 0-Element:**</span><span class="sxs-lookup"><span data-stu-id="cc80c-4845">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="cc80c-4846">**PropId** ist auf 0x00000002 (DBPROP \_ MACHINE) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4846">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="cc80c-4847">**DBPROPOPTIONS** ist auf 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4847">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="cc80c-4848">**DBPROPSTATUS** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4848">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cc80c-4849">Für das **ColId-Element:**</span><span class="sxs-lookup"><span data-stu-id="cc80c-4849">For the **ColId** element:</span></span>
                -   <span data-ttu-id="cc80c-4850">**eKind** ist auf 0x00000001 (DBKIND \_ GUID \_ PROPID) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4850">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="cc80c-4851">**Die GUID** ist NULL (alle Nullen), d. h., der Wert gilt für die Abfrage, nicht nur für eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4851">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="cc80c-4852">**ulID** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4852">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cc80c-4853">Für **vValue-Element:**</span><span class="sxs-lookup"><span data-stu-id="cc80c-4853">For **vValue** element:</span></span>
                -   <span data-ttu-id="cc80c-4854">**vType:** 0x0008 (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="cc80c-4854">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="cc80c-4855">**vValue**: 0x04/ "X" (4 Bytes/auf NULL terminiert Unicode-Zeichenfolge), was "X" -Name eines Servers bedeutet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4855">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="cc80c-4856">**Das Feld cExtPropSet** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4856">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cc80c-4857">**Das Array aPropertySets** ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4857">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="cc80c-4858">Bei Bedarf werden verschiedene Auffüllfelder ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4858">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="cc80c-4859">Die Nachricht wird an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4859">The message is sent to the server.</span></span>

4.  <span data-ttu-id="cc80c-4860">Der Server überprüft, ob **\_ ulChecksum** richtig ist, überprüft, ob der Benutzer berechtigt ist, diese Anforderung zu stellen, und antwortet mit einer CPMConnectOut-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4860">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="cc80c-4861">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4861">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4862">**\_ msg** ist auf 0x000000C8, was angibt, dass es sich um eine CPMConnectOut-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4862">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="cc80c-4863">**\_ status** ist auf festgelegt, 0x0000000 SUCCESS angibt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4863">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="cc80c-4864">**\_ ulChecksum** ist auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4864">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="cc80c-4865">**\_ ulReserved2** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4865">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="cc80c-4866">Der Text der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4866">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4867">Das Feld **\_ serverVersion** ist auf 0x00000007 (32-Bit Windows XP oder 32-Bit Windows Server 2003) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4867">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="cc80c-4868">**\_ Reservierte** Felder werden mit beliebigen Daten gefüllt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4868">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="cc80c-4869">Der Client bereitet eine CPMCreateQueryIn-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4869">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="cc80c-4870">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4870">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4871">**\_ msg** ist auf 0x000000CA festgelegt, was angibt, dass es sich um eine CPMCreateQueryIn-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4871">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="cc80c-4872">**\_ status** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4872">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cc80c-4873">**\_ ulChecksum** enthält die Prüfsumme, die gemäß 3.2.5 berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4873">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="cc80c-4874">**\_ ulReserved2** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4874">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="cc80c-4875">Der Text der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4875">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4876">**Das** Feld Größe wird auf die Größe der restlichen Nachricht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4876">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="cc80c-4877">Das Feld **CColumnSetPresent** ist auf 0x01 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4877">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="cc80c-4878">**Das ColumnSet-Feld** ist vom Typ CColumnSet.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4878">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="cc80c-4879">Die CColumnSet-Struktur, aus der dieses Feld besteht, wird wie folgt festgelegt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4879">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="cc80c-4880">**\_ das Feld count** ist auf 0x00000001 festgelegt, der angibt, dass eine Spalte zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4880">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="cc80c-4881">**indexes-Array** ist 0x00000000 gibt den ersten Eintrag in \_ aPropSpec an.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4881">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="cc80c-4882">Das Feld **CRestrictionPresent** ist auf 0x01 festgelegt, das angibt, dass das Feld **Einschränkung** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4882">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="cc80c-4883">**Das Einschränkungsfeld** ist vom Typ CRestriction und auf festgelegt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4883">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="cc80c-4884">**\_ ulType** ist auf 0x00000004 (RTContent) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4884">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="cc80c-4885">**\_ weight** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4885">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cc80c-4886">Der Rest des Felds enthält eine CContentRestriction-Struktur:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4886">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="cc80c-4887">**\_** Die Eigenschaft ist auf GUID B725F130-47EF-101A-A5F1-02608c9eebac/ 0x00000001 (für PRSPEC PROPID) / 0x13 festgelegt, die den \_ Dokumentkörper darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4887">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="cc80c-4888">**\_ Cc** ist auf 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4888">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="cc80c-4889">**\_ pwcsphrase** ist auf die Zeichenfolge "Microsoft" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4889">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="cc80c-4890">**\_ lcid** ist auf 0x409 (für Englisch) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4890">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="cc80c-4891">**\_ ulGenerateMethod** ist auf 0x00000000 (genaue Übereinstimmung) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4891">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="cc80c-4892">**CSortPresent** ist auf 0x00.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4892">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="cc80c-4893">**CCategorizationSetPresent** ist auf 0x00.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4893">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="cc80c-4894">**RowSetProperties** wird wie folgt festgelegt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4894">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="cc80c-4895">**\_ uBooleanOptions** ist auf 0x00000001 (sequenziell) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4895">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="cc80c-4896">**\_ ulMaxOpenRows** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4896">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cc80c-4897">**\_ ulMemoryUsage** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4897">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cc80c-4898">\_**cMaxResults** ist auf 0x00000100 festgelegt (gibt mindestens 256 Zeilen zurück).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4898">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="cc80c-4899">**\_ cCmdTimeOut** ist auf 0x00000000 festgelegt (nie Timeout).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4899">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="cc80c-4900">**PidMapper** ist auf:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4900">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="cc80c-4901">**\_ count** ist auf 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4901">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="cc80c-4902">**\_ aPropSpec** ist auf GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC/ 0x00000001 (für PRSPEC PROPID) / 0x0000000c festgelegt, was die \_ Windows-Dateigrößeneigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4902">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="cc80c-4903">Der Server verarbeitet sie und antwortet mit einer CPMCreateQueryOut-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4903">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="cc80c-4904">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4904">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4905">**\_ msg** ist auf 0x000000CA festgelegt und gibt an, dass es sich um eine CPMCreateQueryOut-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4905">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="cc80c-4906">**\_ status** ist auf SUCCESS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4906">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="cc80c-4907">**\_ ulChecksum** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4907">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="cc80c-4908">**\_ ulReserved2** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4908">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="cc80c-4909">Der Nachrichtentext wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4909">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4910">**\_ fTrueSeqeuntial** ist auf 0x00000000 festgelegt, was angibt, dass die Abfrage einen Index verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4910">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="cc80c-4911">**\_ fWorkIdUnique** ist auf 0x00000001 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4911">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="cc80c-4912">Das **aCursors-Array** enthält nur ein Element, das ein Cursorhandle für diese Abfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4912">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="cc80c-4913">Der Wert hängt vom Status des Servers ab.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4913">The value depends on the state of the server.</span></span> <span data-ttu-id="cc80c-4914">Angenommen, der zurückgegebene Wert ist 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4914">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="cc80c-4915">Der Client gibt eine CPMSetBindingsIn-Anforderungsnachricht aus, um das Format einer Zeile zu definieren.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4915">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="cc80c-4916">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4916">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4917">**\_ msg** ist auf 0x000000D0 festgelegt, was angibt, dass es sich um eine CPMSetBindingsIn-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4917">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="cc80c-4918">**\_ status** ist auf SUCCESS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4918">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="cc80c-4919">**\_ ulChecksum** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4919">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="cc80c-4920">**\_ ulReserved2** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4920">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="cc80c-4921">Der Text der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4921">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4922">**\_ hCursor** ist auf 0xAAAAAAAA festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4922">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="cc80c-4923">**\_ cbRow** ist auf 0x10 festgelegt (groß genug für Spalten).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4923">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="cc80c-4924">**\_ cbBindingDesc** wird auf die Größe der Felder **\_ cColumns** und **\_ aColumns** kombiniert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4924">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="cc80c-4925">**\_ cColumns** ist auf 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4925">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="cc80c-4926">**\_ Das Array aColumns** ist so festgelegt, dass es eine CTableColumn-Struktur enthält, die Folgendes enthält:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4926">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="cc80c-4927">**\_ PropSpec** ist auf GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (für PRSPEC PROPID) / 0x0000000c festgelegt, was die Windows-Dateigrößeneigenschaft \_ darstellt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4927">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="cc80c-4928">**\_ vType** ist auf 0x0015 (VT \_ UI8) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4928">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="cc80c-4929">**\_ ValueUsed** wird auf 0x01 (Spalte in Zeile übertragen) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4929">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="cc80c-4930">**\_ ValueOffset** ist auf 0x0002 (am Anfang der Zeile) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4930">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="cc80c-4931">**\_ ValueSize** ist auf 0x08 (Größe einer VT \_ UI8) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4931">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="cc80c-4932">**\_ StatusUsed** ist auf 0x01.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4932">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="cc80c-4933">**\_ StatusOffset** ist auf 0x0A.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4933">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="cc80c-4934">**\_ LengthUsed** ist auf 0x00.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4934">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="cc80c-4935">Der Server verarbeitet sie und antwortet mit einer CPMSetBindingsIn-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4935">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="cc80c-4936">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4936">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4937">**\_ msg** ist auf 0x000000D0.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4937">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="cc80c-4938">**\_ status** ist auf SUCCESS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4938">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="cc80c-4939">**\_ ulChecksum** wird auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4939">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="cc80c-4940">**\_ ulReserved2** wird auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4940">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="cc80c-4941">Der Client gibt eine CPMGetRowsIn-Anforderungsnachricht aus.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4941">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="cc80c-4942">Angenommen, der Client ist bereit, an diesem Punkt 100 Zeilen zu akzeptieren, und möchte sie in aufsteigender Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4942">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="cc80c-4943">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4943">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4944">**\_ msg** ist auf 0x000000CC, was angibt, dass es sich um eine CPMGetRowsIn-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4944">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="cc80c-4945">**\_ status** ist auf 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc80c-4945">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="cc80c-4946">**\_ ulChecksum** enthält die Prüfsumme, die gemäß Abschnitt 0 berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4946">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="cc80c-4947">**\_ ulReserved2** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4947">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="cc80c-4948">Der Text der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4948">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4949">**\_ hCursor** ist auf 0xAAAAAAAA festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4949">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="cc80c-4950">**\_ cRowsToTransfer** ist auf 0x00000064 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4950">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="cc80c-4951">**\_ cRowWidth** ist auf 0x00000010 (aus Bindungen) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4951">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="cc80c-4952">**\_ cbSeek** ist auf 0x14 festgelegt, wobei es sich um die Größe der Felder eType, \_ chapt und CRowSeekNext handelt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4952">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="cc80c-4953">**\_ cbReserved** ist auf 0x18 (0x14 plus \_ cbSeek) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4953">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="cc80c-4954">**\_ cbReadBuffer** ist auf 0x800 festgelegt (0x64 \* 0x10 auf das nächste Vielfache von 0x200 aufgerundet).</span><span class="sxs-lookup"><span data-stu-id="cc80c-4954">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="cc80c-4955">**\_ ulClientBase** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4955">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cc80c-4956">**\_ fBwdfetch** wird auf 0x00000000 festgelegt, der angibt, dass die Zeilen in vorwärts gerichteter Reihenfolge abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4956">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="cc80c-4957">**eType** wird auf 0x0000001 festgelegt, der angibt, dass der Client die nächsten Zeilen wünscht.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4957">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="cc80c-4958">**\_ chapt** ist auf 0 (kein Kapitelergebnis) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4958">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="cc80c-4959">**SeekDescription** ist auf CRowSeekNext festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4959">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="cc80c-4960">Die CRowSeekNext-Struktur enthält die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4960">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="cc80c-4961">**CiTblChapt** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4961">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cc80c-4962">**\_ hRegion** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4962">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cc80c-4963">**\_ cSkip** ist auf 0 festgelegt, was angibt, dass der Client keine Zeilen überspringen möchte.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4963">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="cc80c-4964">Der Server verarbeitet sie und antwortet mit einer CPMGetRowsOut-Meldung.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4964">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="cc80c-4965">Angenommen, der Server hat 100 Dokumente gefunden, die das Wort "Microsoft" enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4965">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="cc80c-4966">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4966">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4967">**\_ msg** ist auf 0x000000CC, was angibt, dass es sich um eine CPMGetRowsOut-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4967">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="cc80c-4968">**\_ status** ist auf SUCCESS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4968">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="cc80c-4969">**\_ ulChecksum** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4969">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cc80c-4970">**\_ ulReserved2** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4970">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="cc80c-4971">Der Text der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4971">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4972">**\_ CRowsReturned** ist auf 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4972">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="cc80c-4973">**eType** ist auf 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4973">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="cc80c-4974">**\_ chapt** ist auf 0x00000000 (kein kapiteliertes Ergebnis) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4974">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="cc80c-4975">**SeekDescription** enthält eine CRowSeekNext-Struktur, die wie folgt aufgefüllt wird:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4975">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="cc80c-4976">**CiTblChapt** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4976">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cc80c-4977">**\_ hRegion** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4977">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cc80c-4978">**\_ cSkip ist** auf 0 festgelegt, was bedeutet, dass der Client keine Zeilen überspringen möchte.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4978">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="cc80c-4979">**Zeilen** enthalten die Größe der 100 Dokumente, die das Wort "Microsoft" enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4979">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="cc80c-4980">Da es sich um Daten fester Größe handelt, werden sie einfach als Liste mit 100 8-Byte-Ganzzahlen ohne Vorzeichen strukturiert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4980">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="cc80c-4981">Der Client sendet eine CPMDisconnect-Nachricht, um die Verbindung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4981">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="cc80c-4982">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4982">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cc80c-4983">**\_ msg** ist auf 0x000000C9, was angibt, dass es sich um eine CPMDisconnect-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4983">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="cc80c-4984">**\_ status** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4984">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cc80c-4985">**\_ ulChecksum** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4985">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="cc80c-4986">Der Server verarbeitet die Nachricht und entfernt den gesamten Clientstatus.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4986">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="cc80c-4987">4.2 Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cc80c-4987">4.2 Example 2</span></span>

<span data-ttu-id="cc80c-4988">Im vorherigen Beispiel war die Abfrage recht einfach.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4988">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="cc80c-4989">Betrachten wir nun eine etwas komplexere Abfrage.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4989">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="cc80c-4990">Angenommen, der Benutzer möchte die Größe der Dokumente abrufen, die die folgenden Wörter enthalten: "Microsoft" und "Office".</span><span class="sxs-lookup"><span data-stu-id="cc80c-4990">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="cc80c-4991">Dies wird angegeben, indem Sie das Feld Einschränkung in der in Schritt 5 gesendeten CPMCreateQueryIn-Nachricht wie folgt ändern:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4991">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="cc80c-4992">Das Feld **Einschränkung** hat den Typ CRestriction und ist auf Folgendes festgelegt:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4992">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="cc80c-4993">**\_ ulType** ist auf 0x00000004 (RTAnd) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4993">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="cc80c-4994">**\_ weight** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4994">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="cc80c-4995">Der Rest des Felds enthält eine CNodeRestriction-Struktur:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4995">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="cc80c-4996">**\_ cNode** ist auf 0x00000002 festgelegt und gibt an, dass das PaNode-Array zwei Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4996">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="cc80c-4997">Das **\_ PaNode-Feld** ist ein Array von zwei CRestriction-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4997">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="cc80c-4998">**\_ paNode \[ 0 \]** enthält:</span><span class="sxs-lookup"><span data-stu-id="cc80c-4998">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="cc80c-4999">**\_ ulType** ist auf 0x00000004 (RTContent) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-4999">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="cc80c-5000">**\_ weight** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5000">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cc80c-5001">Der Rest des Felds enthält eine CContentRestriction-Struktur:</span><span class="sxs-lookup"><span data-stu-id="cc80c-5001">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="cc80c-5002">**\_ Die Eigenschaft** ist auf GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (für PRSPEC \_ PROPID) /0x13 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5002">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="cc80c-5003">**\_ Cc** ist auf 0x00000009 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5003">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="cc80c-5004">**\_ pwcsphrase** ist auf die Zeichenfolge "Microsoft" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5004">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="cc80c-5005">**\_ lcid** ist auf 0x409 (für Englisch) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5005">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="cc80c-5006">**\_ ulGenerateMethod** ist auf 0x00000000 (genaue Übereinstimmung) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5006">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="cc80c-5007">**\_ paNode \[ 1 \]** enthält:</span><span class="sxs-lookup"><span data-stu-id="cc80c-5007">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="cc80c-5008">**\_ ulType** ist auf 0x00000004 (RTContent) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5008">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="cc80c-5009">**\_ weight** ist auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5009">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cc80c-5010">Der Rest des Felds enthält eine CContentRestriction-Struktur:</span><span class="sxs-lookup"><span data-stu-id="cc80c-5010">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="cc80c-5011">**\_ Die** Eigenschaft ist auf GUID b725f130-47ef-101a-a5f1-02608c9eebac/ 0x00000001 (für PRSPEC \_ PROPID) / 0x13.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5011">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="cc80c-5012">**\_ Cc** ist auf 0x00000006.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5012">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="cc80c-5013">**\_ pwcsphrase** ist auf die Zeichenfolge "Office" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5013">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="cc80c-5014">**\_ lcid** ist auf 0x409 (für Englisch) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5014">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="cc80c-5015">**\_ ulGenerateMethod** ist auf 0x00000000 (genaue Übereinstimmung) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5015">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="cc80c-5016">5 Sicherheit</span><span class="sxs-lookup"><span data-stu-id="cc80c-5016">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="cc80c-5017">5.1 Sicherheitsüberlegungen für Ausführende</span><span class="sxs-lookup"><span data-stu-id="cc80c-5017">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="cc80c-5018">Indizierungsimplementierungen, die sicheren Inhalt indizieren, sollten die Verwendung des von SMB MS-SMB bereitgestellten Benutzerkontexts in Betracht ziehen, um Suchergebnisse zu kürzen und nur die für den Aufrufer zugänglichen \[ \] Zurücksenden von Suchergebnissen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5018">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="cc80c-5019">5.2 Index von Sicherheitsparameter</span><span class="sxs-lookup"><span data-stu-id="cc80c-5019">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="cc80c-5020">Sicherheitsparameter</span><span class="sxs-lookup"><span data-stu-id="cc80c-5020">Security Parameter</span></span>  | <span data-ttu-id="cc80c-5021">Abschnitt</span><span class="sxs-lookup"><span data-stu-id="cc80c-5021">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="cc80c-5022">Ebene des Identitätswechsels</span><span class="sxs-lookup"><span data-stu-id="cc80c-5022">Impersonation level</span></span> | <span data-ttu-id="cc80c-5023">2.1</span><span class="sxs-lookup"><span data-stu-id="cc80c-5023">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="cc80c-5024">6 Index des versionsspezifischen Verhaltens</span><span class="sxs-lookup"><span data-stu-id="cc80c-5024">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="cc80c-5025">Versionsspezifisches Verhalten</span><span class="sxs-lookup"><span data-stu-id="cc80c-5025">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="cc80c-5026">Abschnitt</span><span class="sxs-lookup"><span data-stu-id="cc80c-5026">Section</span></span>   | <span data-ttu-id="cc80c-5027">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cc80c-5027">Windows 2000</span></span> | <span data-ttu-id="cc80c-5028">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cc80c-5028">Windows XP</span></span> | <span data-ttu-id="cc80c-5029">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cc80c-5029">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="cc80c-5030">Dieses Protokoll wird unter Windows 2000, Windows XP, Windows Server 2003 und Windows Vista implementiert.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5030">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="cc80c-5031">1.3.2</span><span class="sxs-lookup"><span data-stu-id="cc80c-5031">1.3.2</span></span>     | <span data-ttu-id="cc80c-5032">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5032">X</span></span>            | <span data-ttu-id="cc80c-5033">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5033">X</span></span>          | <span data-ttu-id="cc80c-5034">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5034">X</span></span>                   |
| <span data-ttu-id="cc80c-5035">Anwendungen interagieren in der Regel mit einem OLE DB-Wrapper.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5035">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="cc80c-5036">1.4</span><span class="sxs-lookup"><span data-stu-id="cc80c-5036">1.4</span></span>       | <span data-ttu-id="cc80c-5037">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5037">X</span></span>            | <span data-ttu-id="cc80c-5038">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5038">X</span></span>          | <span data-ttu-id="cc80c-5039">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5039">X</span></span>                   |
| <span data-ttu-id="cc80c-5040">NTSTATUS-Werte</span><span class="sxs-lookup"><span data-stu-id="cc80c-5040">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="cc80c-5041">1.8</span><span class="sxs-lookup"><span data-stu-id="cc80c-5041">1.8</span></span>       | <span data-ttu-id="cc80c-5042">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5042">X</span></span>            | <span data-ttu-id="cc80c-5043">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5043">X</span></span>          | <span data-ttu-id="cc80c-5044">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5044">X</span></span>                   |
| <span data-ttu-id="cc80c-5045">Der Client legt das \_ Statusfeld in jedem Nachrichtenheader fest.</span><span class="sxs-lookup"><span data-stu-id="cc80c-5045">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="cc80c-5046">2.2.2</span><span class="sxs-lookup"><span data-stu-id="cc80c-5046">2.2.2</span></span>     | <span data-ttu-id="cc80c-5047">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5047">X</span></span>            | <span data-ttu-id="cc80c-5048">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5048">X</span></span>          | <span data-ttu-id="cc80c-5049">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5049">X</span></span>                   |
| <span data-ttu-id="cc80c-5050">cPendingScans-Wert ist in der Regel 0 (null)</span><span class="sxs-lookup"><span data-stu-id="cc80c-5050">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="cc80c-5051">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="cc80c-5051">2.2.3.1</span></span>   | <span data-ttu-id="cc80c-5052">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5052">X</span></span>            | <span data-ttu-id="cc80c-5053">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5053">X</span></span>          | <span data-ttu-id="cc80c-5054">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5054">X</span></span>                   |
| <span data-ttu-id="cc80c-5055">iClientVersion-Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-5055">iClientVersion value</span></span>                                                                              | <span data-ttu-id="cc80c-5056">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="cc80c-5056">2.2.3.6</span></span>   | <span data-ttu-id="cc80c-5057">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5057">X</span></span>            | <span data-ttu-id="cc80c-5058">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5058">X</span></span>          | <span data-ttu-id="cc80c-5059">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5059">X</span></span>                   |
| <span data-ttu-id="cc80c-5060">\_cbChunk-Wert</span><span class="sxs-lookup"><span data-stu-id="cc80c-5060">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="cc80c-5061">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="cc80c-5061">2.2.3.19</span></span>  | <span data-ttu-id="cc80c-5062">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5062">X</span></span>            | <span data-ttu-id="cc80c-5063">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5063">X</span></span>          | <span data-ttu-id="cc80c-5064">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5064">X</span></span>                   |
| <span data-ttu-id="cc80c-5065">32-Bit- und 64-Bit-Speicheradressen</span><span class="sxs-lookup"><span data-stu-id="cc80c-5065">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="cc80c-5066">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="cc80c-5066">3.2.4.2.4</span></span> | <span data-ttu-id="cc80c-5067">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5067">X</span></span>            | <span data-ttu-id="cc80c-5068">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5068">X</span></span>          | <span data-ttu-id="cc80c-5069">X</span><span class="sxs-lookup"><span data-stu-id="cc80c-5069">X</span></span>                   |



 

 

 





