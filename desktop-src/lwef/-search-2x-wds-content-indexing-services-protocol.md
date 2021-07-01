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
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="c3671-103">Inhaltsindizierungsdienste-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c3671-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="c3671-104">Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="c3671-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c3671-105">Verwenden Sie in späteren [Versionen Windows Search.](../search/-search-3x-wds-overview.md)</span><span class="sxs-lookup"><span data-stu-id="c3671-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="c3671-106">Protokollspezifikation, Version 0.12</span><span class="sxs-lookup"><span data-stu-id="c3671-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="c3671-107">1 Einführung</span><span class="sxs-lookup"><span data-stu-id="c3671-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="c3671-108">1.1 Glossar</span><span class="sxs-lookup"><span data-stu-id="c3671-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="c3671-109">1.2 Verweise</span><span class="sxs-lookup"><span data-stu-id="c3671-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="c3671-110">1.3 Protokollübersicht (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="c3671-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="c3671-111">1.4 Beziehung zu anderen Protokollen</span><span class="sxs-lookup"><span data-stu-id="c3671-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="c3671-112">1.5 Voraussetzungen und Vorbedingungen</span><span class="sxs-lookup"><span data-stu-id="c3671-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="c3671-113">1.6 Anwendbarkeitsanweisung</span><span class="sxs-lookup"><span data-stu-id="c3671-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="c3671-114">1.7 Versionsverwaltung und Funktionsübertragung</span><span class="sxs-lookup"><span data-stu-id="c3671-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="c3671-115">1.8 Durch Hersteller erweiterbare Felder</span><span class="sxs-lookup"><span data-stu-id="c3671-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="c3671-116">1.9 Zuweisungen von Standards</span><span class="sxs-lookup"><span data-stu-id="c3671-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="c3671-117">2\. Nachrichten</span><span class="sxs-lookup"><span data-stu-id="c3671-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="c3671-118">2.1 Transport</span><span class="sxs-lookup"><span data-stu-id="c3671-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="c3671-119">2.2 Nachrichtensyntax</span><span class="sxs-lookup"><span data-stu-id="c3671-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="c3671-120">3 Protokolldetails</span><span class="sxs-lookup"><span data-stu-id="c3671-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="c3671-121">3.1 Serverdetails</span><span class="sxs-lookup"><span data-stu-id="c3671-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="c3671-122">3.2 Clientdetails</span><span class="sxs-lookup"><span data-stu-id="c3671-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="c3671-123">4 Beispiele für Protokolle</span><span class="sxs-lookup"><span data-stu-id="c3671-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="c3671-124">4.1 Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3671-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="c3671-125">4.2 Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c3671-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="c3671-126">5 Sicherheit</span><span class="sxs-lookup"><span data-stu-id="c3671-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="c3671-127">5.1 Sicherheitsüberlegungen für Ausführende</span><span class="sxs-lookup"><span data-stu-id="c3671-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="c3671-128">5.2 Index von Sicherheitsparameter</span><span class="sxs-lookup"><span data-stu-id="c3671-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="c3671-129">6 Index des versionsspezifischen Verhaltens</span><span class="sxs-lookup"><span data-stu-id="c3671-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="c3671-130">Dieses Dokument ist eine Spezifikation des Content Indexing Service-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="c3671-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="c3671-131">Die WSPP-Dokumentation (Workgroup Server Protocol Program) ist für die Verwendung in Verbindung mit dokumentation zu öffentlichen Standards, Netzwerkprogrammierungsart und Konzepten verteilter Windows-Arbeitsgruppensysteme vorgesehen und setzt voraus, dass der Leser entweder mit dem oben genannten Material vertraut ist oder sofortigen Zugriff darauf hat.</span><span class="sxs-lookup"><span data-stu-id="c3671-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="c3671-132">Eine WSPP-Protokollspezifikation erfordert nicht die Verwendung von Microsoft-Programmiertools oder -Programmierumgebungen, damit ein Lizenzer eine Implementierung entwickeln kann.</span><span class="sxs-lookup"><span data-stu-id="c3671-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="c3671-133">Lizenzlizenzen, die Zugriff auf Microsoft-Programmiertools und -umgebungen haben, können diese nutzen.</span><span class="sxs-lookup"><span data-stu-id="c3671-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="c3671-134">1 Einführung</span><span class="sxs-lookup"><span data-stu-id="c3671-134">1 Introduction</span></span>

-   [<span data-ttu-id="c3671-135">1.1 Glossar</span><span class="sxs-lookup"><span data-stu-id="c3671-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="c3671-136">1.2 Verweise</span><span class="sxs-lookup"><span data-stu-id="c3671-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="c3671-137">1.3 Protokollübersicht (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="c3671-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="c3671-138">1.4 Beziehung zu anderen Protokollen</span><span class="sxs-lookup"><span data-stu-id="c3671-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="c3671-139">1.5 Voraussetzungen und Vorbedingungen</span><span class="sxs-lookup"><span data-stu-id="c3671-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="c3671-140">1.6 Anwendbarkeitsanweisung</span><span class="sxs-lookup"><span data-stu-id="c3671-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="c3671-141">1.7 Versionsverwaltung und Funktionsübertragung</span><span class="sxs-lookup"><span data-stu-id="c3671-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="c3671-142">1.8 Durch Hersteller erweiterbare Felder</span><span class="sxs-lookup"><span data-stu-id="c3671-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="c3671-143">1.9 Zuweisungen von Standards</span><span class="sxs-lookup"><span data-stu-id="c3671-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="c3671-144">1.1 Glossar</span><span class="sxs-lookup"><span data-stu-id="c3671-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="c3671-145">Die folgenden Begriffe werden im Glossarabschnitt von \[ MS-SYS \] definiert:</span><span class="sxs-lookup"><span data-stu-id="c3671-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="c3671-146">GUID</span><span class="sxs-lookup"><span data-stu-id="c3671-146">GUID</span></span>
> -   <span data-ttu-id="c3671-147">Little Endian</span><span class="sxs-lookup"><span data-stu-id="c3671-147">Little Endian</span></span>
> -   <span data-ttu-id="c3671-148">Named Pipe</span><span class="sxs-lookup"><span data-stu-id="c3671-148">Named Pipe</span></span>
> -   <span data-ttu-id="c3671-149">`Path`</span><span class="sxs-lookup"><span data-stu-id="c3671-149">Path</span></span>

 

<span data-ttu-id="c3671-150">**Bindung:** Eine Anforderung zum Einbinden einer **bestimmten Spalte** in ein zurückgegebenes **Rowset.**</span><span class="sxs-lookup"><span data-stu-id="c3671-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="c3671-151">Die **Bindung** gibt eine Eigenschaft an, die in die Suchergebnisse aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="c3671-152">**Lesezeichen:** Ein Marker, der eine Zeile innerhalb einer Gruppe von Zeilen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c3671-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="c3671-153">**Katalog:** Die Organisationseinheit der höchsten Ebene im Indizierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="c3671-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="c3671-154">Sie stellt einen Satz indizierter Dokumente dar, für die Abfragen mithilfe des Content Indexing Service-Protokolls ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="c3671-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="c3671-155">**Kategorie:** Eine hierarchische Gruppierung von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="c3671-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="c3671-156">Beispielsweise kann ein Abfrageergebnis, das die Spalten author und title enthält, basierend auf dem Autor kategorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="c3671-157">Jede Gruppe von Zeilen, die denselben Wert für author enthalten, würde eine Kategorie bilden.</span><span class="sxs-lookup"><span data-stu-id="c3671-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="c3671-158">**Kapitel** : Ein Zeilenbereich **innerhalb** einer Gruppe von **Zeilen.**</span><span class="sxs-lookup"><span data-stu-id="c3671-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="c3671-159">**Spalte:** Der Container für einen einzelnen Informationstyp in einer **Zeile.**</span><span class="sxs-lookup"><span data-stu-id="c3671-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="c3671-160">Spalten werden Eigenschaftsnamen zuordnen und angeben, welche Eigenschaften für die Befehlsstrukturelemente der **Suchabfrage** **verwendet** werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="c3671-161">**Befehlsstruktur:** Eine Kombination aus **Einschränkungen,** **Kategorien** und Sortierreihenfolge, die für die Suchabfrage angegeben ist. </span><span class="sxs-lookup"><span data-stu-id="c3671-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="c3671-162">**Cursor:** Eine Entität, die als Mechanismus  zum Arbeiten mit  einer Zeile oder einem kleinen Zeilenblock gleichzeitig in einem Satz von Daten verwendet wird, die in einem Resultset zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="c3671-163">Ein **Cursor** wird in einer einzelnen Zeile **innerhalb des** Resultsets positioniert.</span><span class="sxs-lookup"><span data-stu-id="c3671-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="c3671-164">Nachdem der **Cursor** in einer Zeile positioniert wurde, können Vorgänge für diese Zeile oder für einen Zeilenblock ausgeführt **werden,** **der** an dieser Position beginnt.</span><span class="sxs-lookup"><span data-stu-id="c3671-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="c3671-165">**Handle:** Ein Token, das verwendet werden kann, um **Cursor,** Kapitel und Lesezeichen zu identifizieren **und darauf zu zugreifen.** </span><span class="sxs-lookup"><span data-stu-id="c3671-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="c3671-166">**Index:** Eine persistente Struktur, die den Textinhalt enthält, der von einem Indizierungsdienst aus Dateien **gezogen wurde.**</span><span class="sxs-lookup"><span data-stu-id="c3671-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="c3671-167">Dies schließt die Liste der Wörter ein, die zusammen mit dem enthaltenden Dateinamen, der Wortposition und dem **-Locale gespeichert werden.**</span><span class="sxs-lookup"><span data-stu-id="c3671-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="c3671-168">**Indizierung:** Der Prozess, bei dem Text und Eigenschaften aus Dateien extrahiert und die extrahierten Werte in den Indizes **(für** Text) und im Eigenschaftencache **(für** Eigenschaften) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="c3671-169">**Indizierungsdienst:** Ein Dienst, der indizierte **Kataloge** für den Inhalt und die Eigenschaften von Dateisystemen erstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="c3671-170">Anwendungen können die Kataloge nach Informationen aus den Dateien im indizierten Dateisystem durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="c3671-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="c3671-171">**Locale**: Ein Bezeichner, wie in \[ MS-GPSI Anhang A angegeben, der Einstellungen \] im Zusammenhang mit der Sprache angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="c3671-172">Diese Einstellungen geben an, wie Datumsangaben und Zeiten formatiert, Elemente alphabetisch sortiert, Zeichenfolgen verglichen werden sollen, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="c3671-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="c3671-173">**Abfrage in natürlicher Sprache:** Eine Abfrage, die mit menschlicher Sprache anstelle der Abfragesyntax erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c3671-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="c3671-174">**Rauschwort:** Ein Wort, das vom Indizierungsdienst  ignoriert wird, wenn es in den für die Suchabfrage angegebenen Einschränkungen vorhanden ist, da es nur einen geringen wertwert hat.</span><span class="sxs-lookup"><span data-stu-id="c3671-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="c3671-175">Beispiele für Englisch sind "a", "and" und "the".</span><span class="sxs-lookup"><span data-stu-id="c3671-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="c3671-176">**Eigenschaftencache:** Ein Cache von Dateieigenschaften, die von einem **Indizierungsdienst extrahiert wurden.**</span><span class="sxs-lookup"><span data-stu-id="c3671-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="c3671-177">**Eigenschaftenindizierung:** Der Prozess  zum  Erstellen eines Indexes von Werttypeigenschaften eines Dokuments, einschließlich Autor, Betreff, Typ, Wortanzahl, Anzahl gedruckter Seiten und anderer Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c3671-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="c3671-178">**Einschränkung:** Eine Reihe von Bedingungen, die eine Datei erfüllen muss, um in die Suchergebnisse aufgenommen zu werden, die vom Indizierungsdienst **als** Reaktion auf eine Suchabfrage zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="c3671-179">Eine **Einschränkung** schränkt den Fokus einer Suchabfrage  ein und beschränkt die Dateien, die der Indizierungsdienst in die Suchergebnisse einschränkt, auf dieJenigen, die den Bedingungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c3671-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="c3671-180">**Row**: Die Auflistung von Spalten **mit** den Eigenschaftswerten, die eine  einzelne Datei aus dem Satz von Dateien beschreiben, die den Einschränkungen in der an den Indizierungsdienst übermittelten Suchabfrage **entsprechen.**</span><span class="sxs-lookup"><span data-stu-id="c3671-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="c3671-181">**Rowset:** Eine Reihe von **Zeilen, die** in den Suchergebnissen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="c3671-182">**Sortierreihenfolge:** Der Satz von Regeln in einer Suchabfrage, die die Reihenfolge der Zeilen im Suchergebnis definieren.</span><span class="sxs-lookup"><span data-stu-id="c3671-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="c3671-183">Jede Regel besteht aus einer Eigenschaft (Name, Größe usw.) und einer Richtung für die Reihenfolge (aufsteigend oder absteigend).</span><span class="sxs-lookup"><span data-stu-id="c3671-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="c3671-184">Mehrere Regeln werden sequenziell angewendet.</span><span class="sxs-lookup"><span data-stu-id="c3671-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="c3671-185">**Texttypeigenschaft:** Eine Eigenschaft, die den Inhalt eines Dokuments beschreibt und dem Namen nur unformatierten Text zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="c3671-186">**Werttypeigenschaft:** Eine Eigenschaft, die ein einzelnes Attribut eines gesamten Dokuments beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="c3671-187">Eine Werttypeigenschaft verfügt über eine Datentyp-ID und einen Wert dieses Datentyps, der dem Namen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="c3671-188">**Virtueller Stamm:** Ein alternativer Pfad zu einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="c3671-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="c3671-189">Ein physischer Ordner kann null oder mehr virtuelle Stämme haben.</span><span class="sxs-lookup"><span data-stu-id="c3671-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="c3671-190">Pfade, die mit einem virtuellen Stamm beginnen, werden als virtuelle Pfade bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c3671-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="c3671-191">Beispielsweise kann /server/vanityroot ein virtueller Stamm von C: \\ IIS \\ web \\ folder1 sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="c3671-192">Anschließend würde die Datei C: IIS web folder1default.htm den virtuellen Pfad \\ \\ \\ \\ /server/vanityroot/default.htm.</span><span class="sxs-lookup"><span data-stu-id="c3671-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="c3671-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT:** Diese Begriffe (in allen Obergrenzen) werden wie in \[ RFC2119 beschrieben \] verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3671-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="c3671-194">Alle Aussagen zu optionalem Verhalten enthalten die Worte KÖNNEN, SOLLTEN oder SOLLTEN NICHT.</span><span class="sxs-lookup"><span data-stu-id="c3671-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="c3671-195">1.2 Verweise</span><span class="sxs-lookup"><span data-stu-id="c3671-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="c3671-196">1.2.1 Normative Verweise</span><span class="sxs-lookup"><span data-stu-id="c3671-196">1.2.1 Normative References</span></span>

<span data-ttu-id="c3671-197">\[IEEE754 \] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="c3671-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="c3671-198">\[MS-DCOM \] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", Juni 2006.</span><span class="sxs-lookup"><span data-stu-id="c3671-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="c3671-199">\[MS-GPSI \] Microsoft Corporation, "Gruppenrichtlinie für die Softwareinstallation Extension", Juni 2006.</span><span class="sxs-lookup"><span data-stu-id="c3671-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="c3671-200">\[MS-SMB \] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions", Mai 2006.</span><span class="sxs-lookup"><span data-stu-id="c3671-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="c3671-201">\[MS-SYS \] Microsoft Corporation, "Systemübersicht v4", Juli 2006.</span><span class="sxs-lookup"><span data-stu-id="c3671-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="c3671-202">\[SALTON \] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span><span class="sxs-lookup"><span data-stu-id="c3671-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="c3671-203">\[UNICODE \] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="c3671-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="c3671-204">1.2.2 Informative Verweise</span><span class="sxs-lookup"><span data-stu-id="c3671-204">1.2.2 Informative References</span></span>

<span data-ttu-id="c3671-205">\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .</span><span class="sxs-lookup"><span data-stu-id="c3671-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="c3671-206">\[MSDN-QUERYERR \] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="c3671-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="c3671-207">1.3 Protokollübersicht (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="c3671-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="c3671-208">Ein **Inhaltsindizierungsdienst** hilft dabei, die extrahierten Funktionen einer Sammlung von Dokumenten effizient zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="c3671-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="c3671-209">Das Content Indexing Service-Protokoll (CISP) ermöglicht einem Client die Kommunikation mit einem Server, der einen Indizierungsdienst hostet, um Abfragen auszugeben und einem Administrator die Verwaltung des Indizierungsservers zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="c3671-210">Bei der Verarbeitung von Dateien analysiert ein Indizierungsdienst eine Reihe von Dokumenten und organisiert ihren Inhalt so neu, dass **Eigenschaften** dieser Dokumente als Reaktion auf Abfragen effizient zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="c3671-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="c3671-211">Eine Auflistung von Dokumenten, die abgefragt werden können, umfasst einen **Katalog.**</span><span class="sxs-lookup"><span data-stu-id="c3671-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="c3671-212">Ein Katalog kann einen **Index** (für kurze Verweise auf Text) und einen **Eigenschaftencache** (zum schnellen Abrufen von Eigenschaftswerten) enthalten.</span><span class="sxs-lookup"><span data-stu-id="c3671-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="c3671-213">Konzeptionell besteht ein Katalog aus einer logischen "Tabelle" von Eigenschaften mit dem Text oder Wert und dem entsprechenden Gebietsschema, das in **Spalten** der Tabelle gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="c3671-214">Jede "Zeile" der Tabelle entspricht einem separaten Dokument im Bereich des Katalogs, und jede "Spalte" der Tabelle entspricht einer -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c3671-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="c3671-215">Die von CISP ausgeführten spezifischen Aufgaben werden in zwei Funktionsbereiche gruppiert:</span><span class="sxs-lookup"><span data-stu-id="c3671-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="c3671-216">Remoteverwaltung von Indizierungsdienstkatalogen,</span><span class="sxs-lookup"><span data-stu-id="c3671-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="c3671-217">Remoteabfragen von Indizierungsdienstkatalogen.</span><span class="sxs-lookup"><span data-stu-id="c3671-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="c3671-218">1.3.1 Remoteverwaltungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="c3671-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="c3671-219">CISP ermöglicht die folgenden Indizierungsdienst-Katalogverwaltungsaufgaben von einem Client aus:</span><span class="sxs-lookup"><span data-stu-id="c3671-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="c3671-220">Fragen Sie den aktuellen Status eines Indizierungsdienstkatalogs auf dem Server ab.</span><span class="sxs-lookup"><span data-stu-id="c3671-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="c3671-221">Aktualisieren sie den Status eines Indizierungsdienstkatalogs.</span><span class="sxs-lookup"><span data-stu-id="c3671-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="c3671-222">Starten Sie den Indizierungsprozess für einen bestimmten Satz von Dateien.</span><span class="sxs-lookup"><span data-stu-id="c3671-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="c3671-223">Initiieren Sie die Optimierung eines Indexes, um die Abfrageleistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="c3671-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="c3671-224">Alle Remoteverwaltungsaufgaben folgen einem einfachen Anforderungs-/Antwortmodell.</span><span class="sxs-lookup"><span data-stu-id="c3671-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="c3671-225">Für Verwaltungsaufrufe wird kein Zustand auf dem Client beibehalten, und Verwaltungsaufrufe können in beliebiger Reihenfolge erfolgen.</span><span class="sxs-lookup"><span data-stu-id="c3671-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="c3671-226">1.3.2 Remoteabfragen</span><span class="sxs-lookup"><span data-stu-id="c3671-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="c3671-227">CISP ermöglicht Clients das Ausführen von Suchabfragen für einen Remoteserver, der einen Indizierungsdienst hostet.</span><span class="sxs-lookup"><span data-stu-id="c3671-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="c3671-228">Das Senden einer Suchabfrage ist ein mehrstufiger Prozess, der vom Client initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="c3671-229">Die Schritte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="c3671-230">Der Client fordert eine Verbindung mit einem Server an, der einen Indizierungsdienst hostet.</span><span class="sxs-lookup"><span data-stu-id="c3671-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="c3671-231">Der Client sendet die Parameter für die Suchabfrage, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="c3671-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="c3671-232">Die **Einschränkungen,** mit denen angegeben wird, welche Dokumente in die Suchergebnisse aufgenommen bzw. aus diesen ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="c3671-233">Die Reihenfolge, in der die Suchergebnisse zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="c3671-234">Die Spalten, die im Resultset zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="c3671-235">Die maximale Anzahl von **Zeilen,** die für die Abfrage zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="c3671-236">Die maximale Zeit für die Abfrageausführung.</span><span class="sxs-lookup"><span data-stu-id="c3671-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="c3671-237">Nachdem der Server die Anforderung des Clients zum Initiieren der Abfrage bestätigt hat, kann der Client Statusinformationen zur Abfrage anfordern, dies ist jedoch kein erforderlicher Schritt.</span><span class="sxs-lookup"><span data-stu-id="c3671-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="c3671-238">Der Client gibt dann an, welche Eigenschaften der Server in die Suchergebnisse aufnehmen soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="c3671-239">Der Client fordert ein Resultset vom Server an, und der Server antwortet, indem er dem Client die Eigenschaftswerte für Dateien sendet, die in den Ergebnissen für die Suchabfrage des Clients enthalten waren.</span><span class="sxs-lookup"><span data-stu-id="c3671-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="c3671-240">Wenn der Wert einer Eigenschaft zu groß ist, um in einen einzelnen Antwortpuffer zu passen, sendet der Server die Eigenschaft nicht, sondern legt den Eigenschaftsstatus auf verzögert fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="c3671-241">Der Client fordert den Eigenschaftswert dann separat mithilfe einer Reihe von Anforderungen für aufeinander folgende Blöcke des Werts an und setzt dann die Anforderung anderer Werte fort.</span><span class="sxs-lookup"><span data-stu-id="c3671-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="c3671-242">Sobald der Client mit der Suchabfrage fertig ist und keine zusätzlichen Ergebnisse mehr benötigt, kontaktiert der Client den Server, um die Abfrage freizugeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="c3671-243">Nachdem der Server die Abfrage freigegeben hat, kann der Client eine Anforderung senden, um die Verbindung mit dem Server zu trennen.</span><span class="sxs-lookup"><span data-stu-id="c3671-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="c3671-244">Die Verbindung wird dann geschlossen.</span><span class="sxs-lookup"><span data-stu-id="c3671-244">The connection is then closed.</span></span> <span data-ttu-id="c3671-245">Alternativ kann der Client eine weitere Abfrage ausführen und die Sequenz aus Schritt 2 wiederholen.</span><span class="sxs-lookup"><span data-stu-id="c3671-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="c3671-246">Windows-Verhalten: Dieses Protokoll ist unter Windows 2000, Windows XP, Windows Server 2003 und Windows Vista implementiert.</span><span class="sxs-lookup"><span data-stu-id="c3671-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="c3671-247">1.4 Beziehung zu anderen Protokollen</span><span class="sxs-lookup"><span data-stu-id="c3671-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="c3671-248">CISP verwendet das SMB \[ MS-SMB-Protokoll für den \] Nachrichtentransport.</span><span class="sxs-lookup"><span data-stu-id="c3671-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="c3671-249">Kein anderes Protokoll hängt direkt vom Content Indexing Service-Protokoll ab.</span><span class="sxs-lookup"><span data-stu-id="c3671-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="c3671-250">*Windows-Verhalten: Anwendungen interagieren in der Regel mit einem OLE DB Schnittstellenwrapper \[ MSDN-OLEDB \] (z.B. einem Protokollclient) und nicht direkt mit dem Protokoll.*</span><span class="sxs-lookup"><span data-stu-id="c3671-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="c3671-251">1.5 Voraussetzungen und Vorbedingungen</span><span class="sxs-lookup"><span data-stu-id="c3671-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="c3671-252">Es wird davon ausgegangen, dass der Client den Namen des Servers und einen Katalognamen abgerufen hat, bevor dieses Protokoll aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="c3671-253">Die Vorgehensweise eines Clients liegt außerhalb des Bereichs dieser Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="c3671-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="c3671-254">Außerdem wird davon ausgegangen, dass client und server über eine Sicherheitszuordnung verfügen, die mit Named Pipes MS-SMB verwendet werden \[ \] kann.</span><span class="sxs-lookup"><span data-stu-id="c3671-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="c3671-255">1.6 Anwendbarkeitsanweisung</span><span class="sxs-lookup"><span data-stu-id="c3671-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="c3671-256">CISP ist für das Abfragen und Verwalten von Katalogen auf einem Remoteserver von einem Client aus konzipiert.</span><span class="sxs-lookup"><span data-stu-id="c3671-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="c3671-257">CISP ist unter Windows Vista veraltet.</span><span class="sxs-lookup"><span data-stu-id="c3671-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="c3671-258">1.7 Versionsverwaltung und Funktionsübertragung</span><span class="sxs-lookup"><span data-stu-id="c3671-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="c3671-259">Dieses Protokoll verfügt über keine Mechanismen zur Versions- oder Funktionsaushandlung.</span><span class="sxs-lookup"><span data-stu-id="c3671-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="c3671-260">1.8 Durch Hersteller erweiterbare Felder</span><span class="sxs-lookup"><span data-stu-id="c3671-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="c3671-261">Dieses Protokoll verwendet HRESULTs, die vom Anbieter erweiterbar sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="c3671-262">Anbieter können ihre eigenen Werte für dieses Feld auswählen, solange das C-Bit (0x20000000) wie in Abschnitt 4.1.1 von MS-SYS angegeben festgelegt \[ \] ist, was angibt, dass es sich um einen Kundencode handelt.</span><span class="sxs-lookup"><span data-stu-id="c3671-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="c3671-263">Dieses Protokoll verwendet auch NTSTATUS-Werte, die aus dem in MS-SYS definierten \[ NTSTATUS-Nummernbereich \] stammen.</span><span class="sxs-lookup"><span data-stu-id="c3671-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="c3671-264">Anbieter SOLLTEN diese Werte mit ihrer angegebenen Bedeutung wiederverwenden.</span><span class="sxs-lookup"><span data-stu-id="c3671-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="c3671-265">Die Auswahl eines anderen Werts birgt das Risiko eines Konflikts in der Zukunft.</span><span class="sxs-lookup"><span data-stu-id="c3671-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="c3671-266">*Windows-Verhalten: Windows verwendet nur die in Abschnitt 4.1.3 von MS-SYS angegebenen \[ \] Werte.*</span><span class="sxs-lookup"><span data-stu-id="c3671-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="c3671-267">1.8.1 Eigenschaften-IDs</span><span class="sxs-lookup"><span data-stu-id="c3671-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="c3671-268">Eigenschaften werden durch IDs dargestellt, die als Eigenschaften-IDs bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="c3671-269">Jede Eigenschaft muss über einen global eindeutigen Bezeichner verfügen.</span><span class="sxs-lookup"><span data-stu-id="c3671-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="c3671-270">Dieser Bezeichner besteht aus einer **GUID,** die eine Auflistung von Eigenschaften darstellt, die als Eigenschaftensatz bezeichnet werden, sowie einer Zeichenfolge oder einer 32-Bit-Ganzzahl, um die Eigenschaft innerhalb des Satzes zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c3671-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="c3671-271">Wenn die ganzzahlige Form der ID verwendet wird, werden die Werte 0x00000000, 0xFFFFFFFF und 0xFFFFFFFE als ungültig betrachtet.</span><span class="sxs-lookup"><span data-stu-id="c3671-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="c3671-272">Anbieter können sicherstellen, dass ihre Eigenschaften eindeutig definiert werden, indem sie sie in einem Eigenschaftensatz platzieren, der durch ihre eigene GUID definiert wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="c3671-273">1.9 Zuweisungen von Standards</span><span class="sxs-lookup"><span data-stu-id="c3671-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="c3671-274">Dieses Protokoll weist keine Standardzuweisungen auf, sondern nur private Zuweisungen, die von Microsoft mithilfe von Zuordnungsverfahren vorgenommen werden, die in anderen Protokollen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="c3671-275">Microsoft hat diesem Protokoll eine Benannte Pipe zugeordnet, wie in \[ MS-SMB \] angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="c3671-276">Die Zuweisung ist:</span><span class="sxs-lookup"><span data-stu-id="c3671-276">The assignment is:</span></span>



| <span data-ttu-id="c3671-277">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3671-277">Parameter</span></span> | <span data-ttu-id="c3671-278">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-278">Value</span></span>             | <span data-ttu-id="c3671-279">Verweis</span><span class="sxs-lookup"><span data-stu-id="c3671-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="c3671-280">Pipename</span><span class="sxs-lookup"><span data-stu-id="c3671-280">Pipe name</span></span> | <span data-ttu-id="c3671-281">\\\\ \_ Pipe-CI-SKADS</span><span class="sxs-lookup"><span data-stu-id="c3671-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="c3671-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="c3671-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="c3671-283">2\. Nachrichten</span><span class="sxs-lookup"><span data-stu-id="c3671-283">2 Messages</span></span>

-   [<span data-ttu-id="c3671-284">2.1 Transport</span><span class="sxs-lookup"><span data-stu-id="c3671-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="c3671-285">2.2 Nachrichtensyntax</span><span class="sxs-lookup"><span data-stu-id="c3671-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="c3671-286">2.1 Transport</span><span class="sxs-lookup"><span data-stu-id="c3671-286">2.1 Transport</span></span>

<span data-ttu-id="c3671-287">Alle Nachrichten MÜSSEN mithilfe einer Named Pipe übertragen werden, wie in \[ MS-SMB \] angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="c3671-288">Der folgende Pipename wird verwendet:</span><span class="sxs-lookup"><span data-stu-id="c3671-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="c3671-289">\\\\ \_ Pipe-CI-SKADS</span><span class="sxs-lookup"><span data-stu-id="c3671-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="c3671-290">Dieses Protokoll verwendet das zugrunde liegende SMB-Named Pipe-Protokoll, um die Identität des Aufrufers abzurufen, der die Verbindung hergestellt hat, wie in Abschnitt 2.2.8 von \[ MS-SMB \] angegeben. Der Client MUSS SECURITY \_ IDENTIFICATION als ImpersonationLevel in der Anforderung festlegen, um die Named Pipe zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c3671-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="c3671-291">2.2 Nachrichtensyntax</span><span class="sxs-lookup"><span data-stu-id="c3671-291">2.2 Message Syntax</span></span>

<span data-ttu-id="c3671-292">Mehrere Strukturen und Meldungen in den folgenden Abschnitten beziehen sich auf Kapitel- oder Lesezeichenhandles.</span><span class="sxs-lookup"><span data-stu-id="c3671-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="c3671-293">Ein Handle ist eine 32-Bit-lange nicht transparente Struktur, die ein Kapitel oder Lesezeichen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c3671-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="c3671-294">In der Regel empfangen Clientanwendungen Handlewerte über Methodenaufrufe. es gibt jedoch mehrere bekannte Werte, die nicht von einem Server abgerufen werden müssen, dessen Bedeutung in der folgenden Tabelle angegeben ist:</span><span class="sxs-lookup"><span data-stu-id="c3671-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="c3671-295">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-295">Value</span></span>                         | <span data-ttu-id="c3671-296">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-297">DB \_ NULL \_ HCHAPTER 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="c3671-298">Ein Kapitelhandle für das nicht gekachelte Rowset, das alle Abfrageergebnisse enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="c3671-299">DBBMK \_ FIRST 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="c3671-300">Ein Lesezeichenhandle für ein Lesezeichen, das die erste Zeile im Rowset identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c3671-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="c3671-301">DBBMK \_ LAST 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="c3671-302">Ein Lesezeichenhand handle für ein Lesezeichen, das die letzte Zeile im Rowset identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c3671-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="c3671-303">2.2.1 Strukturen</span><span class="sxs-lookup"><span data-stu-id="c3671-303">2.2.1 Structures</span></span>

<span data-ttu-id="c3671-304">In diesem Abschnitt werden Datenstrukturen beschrieben, die von CISP definiert und verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="c3671-305">Alle 2-, 4- und 8-Byte-Ganzzahlen mit und ohne Vorzeichen in den folgenden Strukturen MÜSSEN in Little-Endian-Byte-Reihenfolge übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="c3671-306">In der folgenden Tabelle sind die in diesem Abschnitt definierten Datenstrukturen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="c3671-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="c3671-307">Struktur</span><span class="sxs-lookup"><span data-stu-id="c3671-307">Structure</span></span>                    | <span data-ttu-id="c3671-308">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3671-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-309">CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="c3671-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="c3671-310">Enthält den Wert, für den eine Übereinstimmungsoperation für eine In einer CPropertyRestriction-Struktur angegebene Eigenschaft durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="c3671-311">SAFEARRAY, SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="c3671-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="c3671-312">Enthält ein mehrdimensionales Array.</span><span class="sxs-lookup"><span data-stu-id="c3671-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="c3671-313">SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="c3671-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="c3671-314">Stellt die Begrenzungen für eine Dimension eines Arrays dar, das in einer SAFEARRAY-Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="c3671-315">CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="c3671-315">CFullPropSpec</span></span>                | <span data-ttu-id="c3671-316">Enthält eine Eigenschaftenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="c3671-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="c3671-317">CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-317">CContentRestriction</span></span>          | <span data-ttu-id="c3671-318">Enthält eine Zeichenfolge, die mit einem Eigenschaftswert im Eigenschaftencache übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="c3671-319">CKey</span><span class="sxs-lookup"><span data-stu-id="c3671-319">CKey</span></span>                         | <span data-ttu-id="c3671-320">Enthält einen Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="c3671-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="c3671-321">CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="c3671-322">Enthält einen Eigenschaftswert, der mit einem Vorgang übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="c3671-323">CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="c3671-324">Enthält eine Abfrage in natürlicher Sprache für eine Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c3671-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="c3671-325">CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-325">CNodeRestriction</span></span>             | <span data-ttu-id="c3671-326">Enthält ein Array von Befehlsstrukturknoten, die die Einschränkungen für eine Abfrage angeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="c3671-327">COccRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-327">COccRestriction</span></span>              | <span data-ttu-id="c3671-328">Enthält die Position eines Worts in einem Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="c3671-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="c3671-329">CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-329">CPropertyRestriction</span></span>         | <span data-ttu-id="c3671-330">Enthält einen Eigenschaftswert, der mit einem Vorgang übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="c3671-331">CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-331">CRangeRestriction</span></span>            | <span data-ttu-id="c3671-332">Enthält eine Einschränkung für einen Bereich von Werten.</span><span class="sxs-lookup"><span data-stu-id="c3671-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="c3671-333">CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-333">CScopeRestriction</span></span>            | <span data-ttu-id="c3671-334">Enthält eine Einschränkung für die zu durchsuchenden Dateien.</span><span class="sxs-lookup"><span data-stu-id="c3671-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="c3671-335">CSort</span><span class="sxs-lookup"><span data-stu-id="c3671-335">CSort</span></span>                        | <span data-ttu-id="c3671-336">Identifiziert eine zu sortierende Spalte.</span><span class="sxs-lookup"><span data-stu-id="c3671-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="c3671-337">CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-337">CSynRestriction</span></span>              | <span data-ttu-id="c3671-338">Enthält ein Wort oder seine Synonyme für einen Abfrageaussatz.</span><span class="sxs-lookup"><span data-stu-id="c3671-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="c3671-339">CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-339">CVectorRestriction</span></span>           | <span data-ttu-id="c3671-340">Enthält einen gewichteten OR-Vorgang auf einem Befehlsstrukturknoten.</span><span class="sxs-lookup"><span data-stu-id="c3671-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="c3671-341">CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-341">CWordRestriction</span></span>             | <span data-ttu-id="c3671-342">Enthält ein Wort für einen Abfrageaussatz.</span><span class="sxs-lookup"><span data-stu-id="c3671-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="c3671-343">CRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-343">CRestriction</span></span>                 | <span data-ttu-id="c3671-344">Enthält einen Knoten einer Abfragebefehlsstruktur.</span><span class="sxs-lookup"><span data-stu-id="c3671-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="c3671-345">CColumnSet</span><span class="sxs-lookup"><span data-stu-id="c3671-345">CColumnSet</span></span>                   | <span data-ttu-id="c3671-346">Gibt die Anzahl der zurückgibtden Spalten an.</span><span class="sxs-lookup"><span data-stu-id="c3671-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="c3671-347">CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="c3671-347">CCategorizationSet</span></span>           | <span data-ttu-id="c3671-348">Enthält Informationen zum Gruppieren eines Sets von Abfrageergebnissen.</span><span class="sxs-lookup"><span data-stu-id="c3671-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="c3671-349">CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="c3671-349">CCategorizationSpec</span></span>          | <span data-ttu-id="c3671-350">Enthält eine Definition von Kategorien, in die Abfrageergebnisse kategorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="c3671-351">CDbColId</span><span class="sxs-lookup"><span data-stu-id="c3671-351">CDbColId</span></span>                     | <span data-ttu-id="c3671-352">Enthält eine Spalte.</span><span class="sxs-lookup"><span data-stu-id="c3671-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="c3671-353">CDbProp</span><span class="sxs-lookup"><span data-stu-id="c3671-353">CDbProp</span></span>                      | <span data-ttu-id="c3671-354">Enthält eine -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c3671-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="c3671-355">CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="c3671-355">CDbPropSet</span></span>                   | <span data-ttu-id="c3671-356">Enthält einen Satz von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c3671-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="c3671-357">CPidMapper</span><span class="sxs-lookup"><span data-stu-id="c3671-357">CPidMapper</span></span>                   | <span data-ttu-id="c3671-358">Enthält ein Array von Eigenschaften-IDs, die die Eigenschaften angeben, die in einem Rowset zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="c3671-359">CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="c3671-359">CRowSeekAt</span></span>                   | <span data-ttu-id="c3671-360">Enthält den Offset, an dem Zeilen in einer CPMGetRowsIn-Nachricht abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="c3671-361">CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="c3671-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="c3671-362">Identifiziert den Punkt, an dem der Abruf für eine CPMGetRowsIn-Nachricht beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="c3671-363">CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="c3671-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="c3671-364">Identifiziert die Lesezeichen, aus denen Zeilen für eine CPMGetRowsIn-Nachricht abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="c3671-365">CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="c3671-365">CRowSeekNext</span></span>                 | <span data-ttu-id="c3671-366">Enthält die Anzahl der Zeilen, die in einer CPMGetRowsIn-Nachricht übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="c3671-367">CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="c3671-367">CRowsetProperties</span></span>            | <span data-ttu-id="c3671-368">Enthält die Konfigurationsinformationen für eine Abfrage.</span><span class="sxs-lookup"><span data-stu-id="c3671-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="c3671-369">CSortSet</span><span class="sxs-lookup"><span data-stu-id="c3671-369">CSortSet</span></span>                     | <span data-ttu-id="c3671-370">Enthält die Sortierreihenfolge für eine Abfrage.</span><span class="sxs-lookup"><span data-stu-id="c3671-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="c3671-371">CTableColumn</span><span class="sxs-lookup"><span data-stu-id="c3671-371">CTableColumn</span></span>                 | <span data-ttu-id="c3671-372">Enthält eine Spalte für die CPMSetBindings-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c3671-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="c3671-373">SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="c3671-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="c3671-374">Enthält einen serialisierten Wert.</span><span class="sxs-lookup"><span data-stu-id="c3671-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="c3671-375">2.2.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="c3671-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="c3671-376">Die CBaseStorageVariant-Struktur enthält den Wert, für den ein Übereinstimmungsvorgang für eine Eigenschaft durchgeführt werden soll, die in der CPropertyRestriction-Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="c3671-377">0</span><span class="sxs-lookup"><span data-stu-id="c3671-377">0</span></span>

<span data-ttu-id="c3671-378">1</span><span class="sxs-lookup"><span data-stu-id="c3671-378">1</span></span>

<span data-ttu-id="c3671-379">2</span><span class="sxs-lookup"><span data-stu-id="c3671-379">2</span></span>

<span data-ttu-id="c3671-380">3</span><span class="sxs-lookup"><span data-stu-id="c3671-380">3</span></span>

<span data-ttu-id="c3671-381">4</span><span class="sxs-lookup"><span data-stu-id="c3671-381">4</span></span>

<span data-ttu-id="c3671-382">5</span><span class="sxs-lookup"><span data-stu-id="c3671-382">5</span></span>

<span data-ttu-id="c3671-383">6</span><span class="sxs-lookup"><span data-stu-id="c3671-383">6</span></span>

<span data-ttu-id="c3671-384">7</span><span class="sxs-lookup"><span data-stu-id="c3671-384">7</span></span>

<span data-ttu-id="c3671-385">8</span><span class="sxs-lookup"><span data-stu-id="c3671-385">8</span></span>

<span data-ttu-id="c3671-386">9</span><span class="sxs-lookup"><span data-stu-id="c3671-386">9</span></span>

<span data-ttu-id="c3671-387">1</span><span class="sxs-lookup"><span data-stu-id="c3671-387">1</span></span><br/> <span data-ttu-id="c3671-388">0</span><span class="sxs-lookup"><span data-stu-id="c3671-388">0</span></span><br/>

<span data-ttu-id="c3671-389">1</span><span class="sxs-lookup"><span data-stu-id="c3671-389">1</span></span>

<span data-ttu-id="c3671-390">2</span><span class="sxs-lookup"><span data-stu-id="c3671-390">2</span></span>

<span data-ttu-id="c3671-391">3</span><span class="sxs-lookup"><span data-stu-id="c3671-391">3</span></span>

<span data-ttu-id="c3671-392">4</span><span class="sxs-lookup"><span data-stu-id="c3671-392">4</span></span>

<span data-ttu-id="c3671-393">5</span><span class="sxs-lookup"><span data-stu-id="c3671-393">5</span></span>

<span data-ttu-id="c3671-394">6</span><span class="sxs-lookup"><span data-stu-id="c3671-394">6</span></span>

<span data-ttu-id="c3671-395">7</span><span class="sxs-lookup"><span data-stu-id="c3671-395">7</span></span>

<span data-ttu-id="c3671-396">8</span><span class="sxs-lookup"><span data-stu-id="c3671-396">8</span></span>

<span data-ttu-id="c3671-397">9</span><span class="sxs-lookup"><span data-stu-id="c3671-397">9</span></span>

<span data-ttu-id="c3671-398">2</span><span class="sxs-lookup"><span data-stu-id="c3671-398">2</span></span><br/> <span data-ttu-id="c3671-399">0</span><span class="sxs-lookup"><span data-stu-id="c3671-399">0</span></span><br/>

<span data-ttu-id="c3671-400">1</span><span class="sxs-lookup"><span data-stu-id="c3671-400">1</span></span>

<span data-ttu-id="c3671-401">2</span><span class="sxs-lookup"><span data-stu-id="c3671-401">2</span></span>

<span data-ttu-id="c3671-402">3</span><span class="sxs-lookup"><span data-stu-id="c3671-402">3</span></span>

<span data-ttu-id="c3671-403">4</span><span class="sxs-lookup"><span data-stu-id="c3671-403">4</span></span>

<span data-ttu-id="c3671-404">5</span><span class="sxs-lookup"><span data-stu-id="c3671-404">5</span></span>

<span data-ttu-id="c3671-405">6</span><span class="sxs-lookup"><span data-stu-id="c3671-405">6</span></span>

<span data-ttu-id="c3671-406">7</span><span class="sxs-lookup"><span data-stu-id="c3671-406">7</span></span>

<span data-ttu-id="c3671-407">8</span><span class="sxs-lookup"><span data-stu-id="c3671-407">8</span></span>

<span data-ttu-id="c3671-408">9</span><span class="sxs-lookup"><span data-stu-id="c3671-408">9</span></span>

<span data-ttu-id="c3671-409">3</span><span class="sxs-lookup"><span data-stu-id="c3671-409">3</span></span><br/> <span data-ttu-id="c3671-410">0</span><span class="sxs-lookup"><span data-stu-id="c3671-410">0</span></span><br/>

<span data-ttu-id="c3671-411">1</span><span class="sxs-lookup"><span data-stu-id="c3671-411">1</span></span>

<span data-ttu-id="c3671-412">vType</span><span class="sxs-lookup"><span data-stu-id="c3671-412">vType</span></span>

<span data-ttu-id="c3671-413">vData1</span><span class="sxs-lookup"><span data-stu-id="c3671-413">vData1</span></span>

<span data-ttu-id="c3671-414">vData2</span><span class="sxs-lookup"><span data-stu-id="c3671-414">vData2</span></span>

<span data-ttu-id="c3671-415">vValue (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-415">vValue (variable)</span></span>



 

<span data-ttu-id="c3671-416">**vType:** Ein Typindikator, der den Typ von vValue angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="c3671-417">Es MUSS einer der in der folgenden Tabelle angegebenen VARENUM-Werte sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="c3671-418">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-418">Value</span></span>                 | <span data-ttu-id="c3671-419">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-420">VT \_ EMPTY (0x0000)</span><span class="sxs-lookup"><span data-stu-id="c3671-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="c3671-421">vValue ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c3671-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="c3671-422">VT \_ NULL (0x0001)</span><span class="sxs-lookup"><span data-stu-id="c3671-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="c3671-423">vValue ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c3671-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="c3671-424">VT \_ I1 (0x0010)</span><span class="sxs-lookup"><span data-stu-id="c3671-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="c3671-425">Eine 1-Byte-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="c3671-426">VT \_ UI1 (0x0011)</span><span class="sxs-lookup"><span data-stu-id="c3671-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="c3671-427">Eine 1-Byte-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="c3671-428">VT \_ I2 (0x0002)</span><span class="sxs-lookup"><span data-stu-id="c3671-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="c3671-429">Eine 2-Byte-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="c3671-430">VT \_ UI2 (0x0012)</span><span class="sxs-lookup"><span data-stu-id="c3671-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="c3671-431">Eine 2-Byte-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="c3671-432">VT \_ BOOL (0x000B)</span><span class="sxs-lookup"><span data-stu-id="c3671-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="c3671-433">Ein boolescher Wert; eine 2-Byte-Ganzzahl, die 0x0000 (FALSE) oder 0xFFFF (TRUE) enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="c3671-434">VT \_ I4 (0x0003)</span><span class="sxs-lookup"><span data-stu-id="c3671-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="c3671-435">Eine 4-Byte-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="c3671-436">VT \_ UI4 (0x0013)</span><span class="sxs-lookup"><span data-stu-id="c3671-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="c3671-437">Eine 4-Byte-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="c3671-438">VT \_ R4 (0x0004)</span><span class="sxs-lookup"><span data-stu-id="c3671-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="c3671-439">Eine IEEE 32-Bit-Gleitkommazahl, wie in \[ IEEE754 \] definiert.</span><span class="sxs-lookup"><span data-stu-id="c3671-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="c3671-440">VT \_ INT (0x0016)</span><span class="sxs-lookup"><span data-stu-id="c3671-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="c3671-441">Eine 4-Byte-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="c3671-442">VT \_ UINT (0x0017)</span><span class="sxs-lookup"><span data-stu-id="c3671-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="c3671-443">Eine 4-Byte-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="c3671-444">\_VT-FEHLER (0x000A)</span><span class="sxs-lookup"><span data-stu-id="c3671-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="c3671-445">Eine 4-Byte-Ganzzahl ohne Vorzeichen, die ein HRESULT enthält, wie in \[ MS-SYS \] angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="c3671-446">VT \_ I8 (0x0014)</span><span class="sxs-lookup"><span data-stu-id="c3671-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="c3671-447">Eine 8-Byte-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="c3671-448">VT \_ UI8 (0x0015)</span><span class="sxs-lookup"><span data-stu-id="c3671-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="c3671-449">Eine 8-Byte-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="c3671-450">VT \_ R8 (0x0005)</span><span class="sxs-lookup"><span data-stu-id="c3671-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="c3671-451">Eine IEEE-64-Bit-Gleitkommazahl gemäß definition in \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="c3671-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="c3671-452">VT \_ CY (0x0006)</span><span class="sxs-lookup"><span data-stu-id="c3671-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="c3671-453">Eine 8-Byte-Ganzzahl mit zwei Komplementen (um 10.000 skaliert).</span><span class="sxs-lookup"><span data-stu-id="c3671-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="c3671-454">VT \_ DATE (0x0007)</span><span class="sxs-lookup"><span data-stu-id="c3671-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="c3671-455">Eine 64-Bit-Gleitkommazahl, die die Anzahl der Tage seit 00:00:00 Uhr am 31. Dezember 1899 (koordinierte Weltzeit) darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="c3671-456">VT \_ FILETIME (0x0040)</span><span class="sxs-lookup"><span data-stu-id="c3671-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="c3671-457">Eine 64-Bit-Ganzzahl, die die Anzahl der Intervalle von 100 Nanosekunden seit 00:00:00 Uhr am 1. Januar 1601 (koordinierte Weltzeit) darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="c3671-458">VT \_ DECIMAL (0x000E)</span><span class="sxs-lookup"><span data-stu-id="c3671-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="c3671-459">Eine DECIMAL-Struktur, wie in Abschnitt 2.2.1.1.1.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="c3671-460">VT \_ CLSID (0x0048)</span><span class="sxs-lookup"><span data-stu-id="c3671-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="c3671-461">Ein 16-Byte-Binärwert, der eine GUID enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="c3671-462">\_VT-BLOB (0x0041)</span><span class="sxs-lookup"><span data-stu-id="c3671-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="c3671-463">Eine 4-Byte-ganzzahlige Anzahl von Bytes ohne Vorzeichen im Blob, gefolgt von dieser Anzahl von Datenbytes.</span><span class="sxs-lookup"><span data-stu-id="c3671-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="c3671-464">VT \_ BSTR (0x0008)</span><span class="sxs-lookup"><span data-stu-id="c3671-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="c3671-465">Eine 4-Byte-Ganzzahlanzahl ohne Vorzeichen in der Zeichenfolge, gefolgt von einer Zeichenfolge, wie unten unter vValue angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="c3671-466">VT \_ LPSTR (0x001E)</span><span class="sxs-lookup"><span data-stu-id="c3671-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="c3671-467">Eine AUF NULL beendete ANSI-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c3671-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="c3671-468">VT \_ LPWSTR (0x001F)</span><span class="sxs-lookup"><span data-stu-id="c3671-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="c3671-469">Eine unicode-Unicode-Zeichenfolge mit \[ \] NULL-Terminierung.</span><span class="sxs-lookup"><span data-stu-id="c3671-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="c3671-470">VT \_ VARIANT (0x000C)</span><span class="sxs-lookup"><span data-stu-id="c3671-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="c3671-471">CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="c3671-471">CBaseStorageVariant.</span></span> <span data-ttu-id="c3671-472">MUSS mit einem Typmodifizierer von VT \_ ARRAY oder VT VECTOR kombiniert \_ werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="c3671-473">In der folgenden Tabelle werden die Typmodifizierer für vType angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="c3671-474">Typmodifizierer können binäres ORed mit vType sein, um die Bedeutung von vValue zu ändern und anzugeben, dass es sich um einen von zwei möglichen Arraytypen handelt.</span><span class="sxs-lookup"><span data-stu-id="c3671-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="c3671-475">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-475">Value</span></span>               | <span data-ttu-id="c3671-476">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-477">VT \_ VECTOR (0x1000)</span><span class="sxs-lookup"><span data-stu-id="c3671-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="c3671-478">Wenn der Typindikator mithilfe eines OR-Operators mit VT VECTOR kombiniert wird, ist vValue ein gezähltes Array von Werten \_ des angegebenen Typs.</span><span class="sxs-lookup"><span data-stu-id="c3671-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="c3671-479">Weitere Informationen finden Sie in Abschnitt 2.2.1.1.1.2.</span><span class="sxs-lookup"><span data-stu-id="c3671-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="c3671-480">Dieser Typmodifizierer DARF NICHT mit den folgenden Typen kombiniert werden: VT \_ INT, VT \_ UINT, VT \_ DECIMAL, VT \_ BLOB, VT \_ BLOB \_ OBJECT.</span><span class="sxs-lookup"><span data-stu-id="c3671-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="c3671-481">VT \_ ARRAY (0x2000)</span><span class="sxs-lookup"><span data-stu-id="c3671-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="c3671-482">Wenn der Typindikator durch einen OR-Operator mit VT ARRAY kombiniert wird, ist der Wert ein \_ SAFEARRAY (wie in Abschnitt 2.2.1.1.1.3 angegeben), das Werte des angegebenen Typs enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="c3671-483">Dieser Typmodifizierer DARF NICHT mit den folgenden Typen kombiniert werden: VT \_ I8, VT \_ UI8, VT \_ FILETIME, VT \_ CLSID, VT \_ BLOB, VT \_ BLOB \_ OBJECT, VT \_ LPSTR, VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="c3671-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="c3671-484">**vData1:** Wenn vType VT DECIMAL ist, wird der Wert dieses Felds als Scale-Feld in Abschnitt \_ 2.2.1.1.1.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="c3671-485">Für alle anderen vTypes MUSS der Wert auf 0x00.</span><span class="sxs-lookup"><span data-stu-id="c3671-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="c3671-486">**vData2:** Wenn vType VT DECIMAL ist, wird der Wert dieses Felds im Abschnitt \_ 2.2.1.1.1.1.1 als Feld Sign angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="c3671-487">Für alle anderen vTypes MUSS der Wert auf 0x00.</span><span class="sxs-lookup"><span data-stu-id="c3671-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="c3671-488">**vValue:** Der Wert für den Ab übereinstimmungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="c3671-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="c3671-489">Die Syntax MUSS wie im vType-Feld angegeben sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="c3671-490">In der folgenden Tabelle sind die Größen für das vValue-Feld zusammengefasst, abhängig vom vType-Feld für Datentypen fester Länge.</span><span class="sxs-lookup"><span data-stu-id="c3671-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="c3671-491">Die Größe ist in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c3671-491">The size is in bytes.</span></span>



| <span data-ttu-id="c3671-492">vType</span><span class="sxs-lookup"><span data-stu-id="c3671-492">vType</span></span>                                                   | <span data-ttu-id="c3671-493">Size</span><span class="sxs-lookup"><span data-stu-id="c3671-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="c3671-494">VT \_ I1, VT, \_ UI1</span><span class="sxs-lookup"><span data-stu-id="c3671-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="c3671-495">1</span><span class="sxs-lookup"><span data-stu-id="c3671-495">1</span></span>    |
| <span data-ttu-id="c3671-496">VT \_ I2, VT \_ UI2, VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="c3671-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="c3671-497">2</span><span class="sxs-lookup"><span data-stu-id="c3671-497">2</span></span>    |
| <span data-ttu-id="c3671-498">VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ INT, VT \_ UINT, VT \_ ERROR</span><span class="sxs-lookup"><span data-stu-id="c3671-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="c3671-499">4</span><span class="sxs-lookup"><span data-stu-id="c3671-499">4</span></span>    |
| <span data-ttu-id="c3671-500">VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ DATE, VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="c3671-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="c3671-501">8</span><span class="sxs-lookup"><span data-stu-id="c3671-501">8</span></span>    |
| <span data-ttu-id="c3671-502">VT \_ DECIMAL, VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="c3671-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="c3671-503">16</span><span class="sxs-lookup"><span data-stu-id="c3671-503">16</span></span>   |



 

<span data-ttu-id="c3671-504">Wenn vType auf VT BLOB, VT BSTR oder VT LPSTR festgelegt ist, wird die Struktur von \_ \_ \_ vValue im folgenden Diagramm angegeben:</span><span class="sxs-lookup"><span data-stu-id="c3671-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="c3671-505">0</span><span class="sxs-lookup"><span data-stu-id="c3671-505">0</span></span>

<span data-ttu-id="c3671-506">1</span><span class="sxs-lookup"><span data-stu-id="c3671-506">1</span></span>

<span data-ttu-id="c3671-507">2</span><span class="sxs-lookup"><span data-stu-id="c3671-507">2</span></span>

<span data-ttu-id="c3671-508">3</span><span class="sxs-lookup"><span data-stu-id="c3671-508">3</span></span>

<span data-ttu-id="c3671-509">4</span><span class="sxs-lookup"><span data-stu-id="c3671-509">4</span></span>

<span data-ttu-id="c3671-510">5</span><span class="sxs-lookup"><span data-stu-id="c3671-510">5</span></span>

<span data-ttu-id="c3671-511">6</span><span class="sxs-lookup"><span data-stu-id="c3671-511">6</span></span>

<span data-ttu-id="c3671-512">7</span><span class="sxs-lookup"><span data-stu-id="c3671-512">7</span></span>

<span data-ttu-id="c3671-513">8</span><span class="sxs-lookup"><span data-stu-id="c3671-513">8</span></span>

<span data-ttu-id="c3671-514">9</span><span class="sxs-lookup"><span data-stu-id="c3671-514">9</span></span>

<span data-ttu-id="c3671-515">1</span><span class="sxs-lookup"><span data-stu-id="c3671-515">1</span></span><br/> <span data-ttu-id="c3671-516">0</span><span class="sxs-lookup"><span data-stu-id="c3671-516">0</span></span><br/>

<span data-ttu-id="c3671-517">1</span><span class="sxs-lookup"><span data-stu-id="c3671-517">1</span></span>

<span data-ttu-id="c3671-518">2</span><span class="sxs-lookup"><span data-stu-id="c3671-518">2</span></span>

<span data-ttu-id="c3671-519">3</span><span class="sxs-lookup"><span data-stu-id="c3671-519">3</span></span>

<span data-ttu-id="c3671-520">4</span><span class="sxs-lookup"><span data-stu-id="c3671-520">4</span></span>

<span data-ttu-id="c3671-521">5</span><span class="sxs-lookup"><span data-stu-id="c3671-521">5</span></span>

<span data-ttu-id="c3671-522">6</span><span class="sxs-lookup"><span data-stu-id="c3671-522">6</span></span>

<span data-ttu-id="c3671-523">7</span><span class="sxs-lookup"><span data-stu-id="c3671-523">7</span></span>

<span data-ttu-id="c3671-524">8</span><span class="sxs-lookup"><span data-stu-id="c3671-524">8</span></span>

<span data-ttu-id="c3671-525">9</span><span class="sxs-lookup"><span data-stu-id="c3671-525">9</span></span>

<span data-ttu-id="c3671-526">2</span><span class="sxs-lookup"><span data-stu-id="c3671-526">2</span></span><br/> <span data-ttu-id="c3671-527">0</span><span class="sxs-lookup"><span data-stu-id="c3671-527">0</span></span><br/>

<span data-ttu-id="c3671-528">1</span><span class="sxs-lookup"><span data-stu-id="c3671-528">1</span></span>

<span data-ttu-id="c3671-529">2</span><span class="sxs-lookup"><span data-stu-id="c3671-529">2</span></span>

<span data-ttu-id="c3671-530">3</span><span class="sxs-lookup"><span data-stu-id="c3671-530">3</span></span>

<span data-ttu-id="c3671-531">4</span><span class="sxs-lookup"><span data-stu-id="c3671-531">4</span></span>

<span data-ttu-id="c3671-532">5</span><span class="sxs-lookup"><span data-stu-id="c3671-532">5</span></span>

<span data-ttu-id="c3671-533">6</span><span class="sxs-lookup"><span data-stu-id="c3671-533">6</span></span>

<span data-ttu-id="c3671-534">7</span><span class="sxs-lookup"><span data-stu-id="c3671-534">7</span></span>

<span data-ttu-id="c3671-535">8</span><span class="sxs-lookup"><span data-stu-id="c3671-535">8</span></span>

<span data-ttu-id="c3671-536">9</span><span class="sxs-lookup"><span data-stu-id="c3671-536">9</span></span>

<span data-ttu-id="c3671-537">3</span><span class="sxs-lookup"><span data-stu-id="c3671-537">3</span></span><br/> <span data-ttu-id="c3671-538">0</span><span class="sxs-lookup"><span data-stu-id="c3671-538">0</span></span><br/>

<span data-ttu-id="c3671-539">1</span><span class="sxs-lookup"><span data-stu-id="c3671-539">1</span></span>

<span data-ttu-id="c3671-540">cbSize</span><span class="sxs-lookup"><span data-stu-id="c3671-540">cbSize</span></span>

<span data-ttu-id="c3671-541">blobData (Variable, optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="c3671-542">**cbSize:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des blobData-Felds in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="c3671-543">Wenn vType auf VT BSTR oder VT LPSTR festgelegt ist, MUSS cbSize auf 0x00000000 festgelegt werden, wenn die dargestellte Zeichenfolge eine \_ \_ leere Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="c3671-544">**blobData:** MUSS die Länge cbSize in Bytes haben.</span><span class="sxs-lookup"><span data-stu-id="c3671-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="c3671-545">Für vType, das auf VT BLOB festgelegt ist, handelt es sich bei \_ diesem Feld um nicht transparente binäre Blobdaten.</span><span class="sxs-lookup"><span data-stu-id="c3671-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="c3671-546">Für vType, der auf VT BSTR festgelegt ist, ist dieses Feld ein Zeichensatz \_ in einem oem-ausgewählten Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="c3671-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="c3671-547">Client und Server MÜSSEN so konfiguriert sein, dass sie interoperable Zeichensätze (Out-of-Band des Protokolls) haben.</span><span class="sxs-lookup"><span data-stu-id="c3671-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="c3671-548">Es ist nicht erforderlich, dass sie auf NULL beendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="c3671-549">Für vType, das auf VT LPSTR festgelegt ist, ist dieses Feld eine auf NULL terminierte Zeichenfolge in einem \_ oem-ausgewählten Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="c3671-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="c3671-550">Client und Server MÜSSEN so konfiguriert sein, dass sie interoperable Zeichensätze (Out-of-Band des Protokolls) haben.</span><span class="sxs-lookup"><span data-stu-id="c3671-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="c3671-551">Wenn vType auf VT LPWSTR festgelegt ist, wird die Struktur von \_ vValue im folgenden Diagramm angegeben:</span><span class="sxs-lookup"><span data-stu-id="c3671-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="c3671-552">0</span><span class="sxs-lookup"><span data-stu-id="c3671-552">0</span></span>

<span data-ttu-id="c3671-553">1</span><span class="sxs-lookup"><span data-stu-id="c3671-553">1</span></span>

<span data-ttu-id="c3671-554">2</span><span class="sxs-lookup"><span data-stu-id="c3671-554">2</span></span>

<span data-ttu-id="c3671-555">3</span><span class="sxs-lookup"><span data-stu-id="c3671-555">3</span></span>

<span data-ttu-id="c3671-556">4</span><span class="sxs-lookup"><span data-stu-id="c3671-556">4</span></span>

<span data-ttu-id="c3671-557">5</span><span class="sxs-lookup"><span data-stu-id="c3671-557">5</span></span>

<span data-ttu-id="c3671-558">6</span><span class="sxs-lookup"><span data-stu-id="c3671-558">6</span></span>

<span data-ttu-id="c3671-559">7</span><span class="sxs-lookup"><span data-stu-id="c3671-559">7</span></span>

<span data-ttu-id="c3671-560">8</span><span class="sxs-lookup"><span data-stu-id="c3671-560">8</span></span>

<span data-ttu-id="c3671-561">9</span><span class="sxs-lookup"><span data-stu-id="c3671-561">9</span></span>

<span data-ttu-id="c3671-562">1</span><span class="sxs-lookup"><span data-stu-id="c3671-562">1</span></span><br/> <span data-ttu-id="c3671-563">0</span><span class="sxs-lookup"><span data-stu-id="c3671-563">0</span></span><br/>

<span data-ttu-id="c3671-564">1</span><span class="sxs-lookup"><span data-stu-id="c3671-564">1</span></span>

<span data-ttu-id="c3671-565">2</span><span class="sxs-lookup"><span data-stu-id="c3671-565">2</span></span>

<span data-ttu-id="c3671-566">3</span><span class="sxs-lookup"><span data-stu-id="c3671-566">3</span></span>

<span data-ttu-id="c3671-567">4</span><span class="sxs-lookup"><span data-stu-id="c3671-567">4</span></span>

<span data-ttu-id="c3671-568">5</span><span class="sxs-lookup"><span data-stu-id="c3671-568">5</span></span>

<span data-ttu-id="c3671-569">6</span><span class="sxs-lookup"><span data-stu-id="c3671-569">6</span></span>

<span data-ttu-id="c3671-570">7</span><span class="sxs-lookup"><span data-stu-id="c3671-570">7</span></span>

<span data-ttu-id="c3671-571">8</span><span class="sxs-lookup"><span data-stu-id="c3671-571">8</span></span>

<span data-ttu-id="c3671-572">9</span><span class="sxs-lookup"><span data-stu-id="c3671-572">9</span></span>

<span data-ttu-id="c3671-573">2</span><span class="sxs-lookup"><span data-stu-id="c3671-573">2</span></span><br/> <span data-ttu-id="c3671-574">0</span><span class="sxs-lookup"><span data-stu-id="c3671-574">0</span></span><br/>

<span data-ttu-id="c3671-575">1</span><span class="sxs-lookup"><span data-stu-id="c3671-575">1</span></span>

<span data-ttu-id="c3671-576">2</span><span class="sxs-lookup"><span data-stu-id="c3671-576">2</span></span>

<span data-ttu-id="c3671-577">3</span><span class="sxs-lookup"><span data-stu-id="c3671-577">3</span></span>

<span data-ttu-id="c3671-578">4</span><span class="sxs-lookup"><span data-stu-id="c3671-578">4</span></span>

<span data-ttu-id="c3671-579">5</span><span class="sxs-lookup"><span data-stu-id="c3671-579">5</span></span>

<span data-ttu-id="c3671-580">6</span><span class="sxs-lookup"><span data-stu-id="c3671-580">6</span></span>

<span data-ttu-id="c3671-581">7</span><span class="sxs-lookup"><span data-stu-id="c3671-581">7</span></span>

<span data-ttu-id="c3671-582">8</span><span class="sxs-lookup"><span data-stu-id="c3671-582">8</span></span>

<span data-ttu-id="c3671-583">9</span><span class="sxs-lookup"><span data-stu-id="c3671-583">9</span></span>

<span data-ttu-id="c3671-584">3</span><span class="sxs-lookup"><span data-stu-id="c3671-584">3</span></span><br/> <span data-ttu-id="c3671-585">0</span><span class="sxs-lookup"><span data-stu-id="c3671-585">0</span></span><br/>

<span data-ttu-id="c3671-586">1</span><span class="sxs-lookup"><span data-stu-id="c3671-586">1</span></span>

<span data-ttu-id="c3671-587">ccLen</span><span class="sxs-lookup"><span data-stu-id="c3671-587">ccLen</span></span>

<span data-ttu-id="c3671-588">string (variable, optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-588">string (variable, optional)</span></span>



 

<span data-ttu-id="c3671-589">**ccLen:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des Zeichenfolgenfelds in Unicode-Zeichen angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="c3671-590">MUSS für eine leere Zeichenfolge auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="c3671-591">**string:** Mit NULL beendete Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c3671-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="c3671-592">2.2.1.1.1 CBaseStorageVariant-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c3671-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="c3671-593">Die folgenden Strukturen werden in der CBaseStorageVariant-Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3671-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="c3671-594">2.2.1.1.1.1 DECIMAL</span><span class="sxs-lookup"><span data-stu-id="c3671-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="c3671-595">DECIMAL wird verwendet, um einen genauen numerischen Wert mit fester Genauigkeit und fester Dezimalstellenzahl zu darstellen.</span><span class="sxs-lookup"><span data-stu-id="c3671-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="c3671-596">Wenn vType auf VT DECIMAL (0x0000E) festgelegt ist, müssen die Felder \_ vData1 und vData2 von CBaseStorageVariant wie folgt interpretiert werden:</span><span class="sxs-lookup"><span data-stu-id="c3671-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="c3671-597">**vData1:** Die Anzahl der Ziffern rechts vom Dezimaltrennzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="c3671-598">MUSS im Bereich von 0 bis 28 liegen.</span><span class="sxs-lookup"><span data-stu-id="c3671-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="c3671-599">**vData2:** Das Vorzeichen des numerischen Werts.</span><span class="sxs-lookup"><span data-stu-id="c3671-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="c3671-600">Legen Sie auf 0x00, wenn positiv, 0x80, wenn negativ.</span><span class="sxs-lookup"><span data-stu-id="c3671-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="c3671-601">Das Format des vValue-Felds lautet:</span><span class="sxs-lookup"><span data-stu-id="c3671-601">The format of the vValue field is:</span></span>



<span data-ttu-id="c3671-602">0</span><span class="sxs-lookup"><span data-stu-id="c3671-602">0</span></span>

<span data-ttu-id="c3671-603">1</span><span class="sxs-lookup"><span data-stu-id="c3671-603">1</span></span>

<span data-ttu-id="c3671-604">2</span><span class="sxs-lookup"><span data-stu-id="c3671-604">2</span></span>

<span data-ttu-id="c3671-605">3</span><span class="sxs-lookup"><span data-stu-id="c3671-605">3</span></span>

<span data-ttu-id="c3671-606">4</span><span class="sxs-lookup"><span data-stu-id="c3671-606">4</span></span>

<span data-ttu-id="c3671-607">5</span><span class="sxs-lookup"><span data-stu-id="c3671-607">5</span></span>

<span data-ttu-id="c3671-608">6</span><span class="sxs-lookup"><span data-stu-id="c3671-608">6</span></span>

<span data-ttu-id="c3671-609">7</span><span class="sxs-lookup"><span data-stu-id="c3671-609">7</span></span>

<span data-ttu-id="c3671-610">8</span><span class="sxs-lookup"><span data-stu-id="c3671-610">8</span></span>

<span data-ttu-id="c3671-611">9</span><span class="sxs-lookup"><span data-stu-id="c3671-611">9</span></span>

<span data-ttu-id="c3671-612">1</span><span class="sxs-lookup"><span data-stu-id="c3671-612">1</span></span><br/> <span data-ttu-id="c3671-613">0</span><span class="sxs-lookup"><span data-stu-id="c3671-613">0</span></span><br/>

<span data-ttu-id="c3671-614">1</span><span class="sxs-lookup"><span data-stu-id="c3671-614">1</span></span>

<span data-ttu-id="c3671-615">2</span><span class="sxs-lookup"><span data-stu-id="c3671-615">2</span></span>

<span data-ttu-id="c3671-616">3</span><span class="sxs-lookup"><span data-stu-id="c3671-616">3</span></span>

<span data-ttu-id="c3671-617">4</span><span class="sxs-lookup"><span data-stu-id="c3671-617">4</span></span>

<span data-ttu-id="c3671-618">5</span><span class="sxs-lookup"><span data-stu-id="c3671-618">5</span></span>

<span data-ttu-id="c3671-619">6</span><span class="sxs-lookup"><span data-stu-id="c3671-619">6</span></span>

<span data-ttu-id="c3671-620">7</span><span class="sxs-lookup"><span data-stu-id="c3671-620">7</span></span>

<span data-ttu-id="c3671-621">8</span><span class="sxs-lookup"><span data-stu-id="c3671-621">8</span></span>

<span data-ttu-id="c3671-622">9</span><span class="sxs-lookup"><span data-stu-id="c3671-622">9</span></span>

<span data-ttu-id="c3671-623">2</span><span class="sxs-lookup"><span data-stu-id="c3671-623">2</span></span><br/> <span data-ttu-id="c3671-624">0</span><span class="sxs-lookup"><span data-stu-id="c3671-624">0</span></span><br/>

<span data-ttu-id="c3671-625">1</span><span class="sxs-lookup"><span data-stu-id="c3671-625">1</span></span>

<span data-ttu-id="c3671-626">2</span><span class="sxs-lookup"><span data-stu-id="c3671-626">2</span></span>

<span data-ttu-id="c3671-627">3</span><span class="sxs-lookup"><span data-stu-id="c3671-627">3</span></span>

<span data-ttu-id="c3671-628">4</span><span class="sxs-lookup"><span data-stu-id="c3671-628">4</span></span>

<span data-ttu-id="c3671-629">5</span><span class="sxs-lookup"><span data-stu-id="c3671-629">5</span></span>

<span data-ttu-id="c3671-630">6</span><span class="sxs-lookup"><span data-stu-id="c3671-630">6</span></span>

<span data-ttu-id="c3671-631">7</span><span class="sxs-lookup"><span data-stu-id="c3671-631">7</span></span>

<span data-ttu-id="c3671-632">8</span><span class="sxs-lookup"><span data-stu-id="c3671-632">8</span></span>

<span data-ttu-id="c3671-633">9</span><span class="sxs-lookup"><span data-stu-id="c3671-633">9</span></span>

<span data-ttu-id="c3671-634">3</span><span class="sxs-lookup"><span data-stu-id="c3671-634">3</span></span><br/> <span data-ttu-id="c3671-635">0</span><span class="sxs-lookup"><span data-stu-id="c3671-635">0</span></span><br/>

<span data-ttu-id="c3671-636">1</span><span class="sxs-lookup"><span data-stu-id="c3671-636">1</span></span>

<span data-ttu-id="c3671-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="c3671-637">Hi32</span></span>

<span data-ttu-id="c3671-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="c3671-638">Lo32</span></span>

<span data-ttu-id="c3671-639">Mitte 32</span><span class="sxs-lookup"><span data-stu-id="c3671-639">Mid32</span></span>



 

<span data-ttu-id="c3671-640">**Hi32**: Die höchsten 32 Bits der 96-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="c3671-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="c3671-641">**Lo32:** Die niedrigsten 32 Bits der 96-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="c3671-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="c3671-642">**Mid32:** Die mittleren 32 Bits der 96-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="c3671-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="c3671-643">2.2.1.1.1.2 VT \_ VECTOR</span><span class="sxs-lookup"><span data-stu-id="c3671-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="c3671-644">VT \_ Vector wird verwendet, um eindimensionale Arrays zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="c3671-645">0</span><span class="sxs-lookup"><span data-stu-id="c3671-645">0</span></span>

<span data-ttu-id="c3671-646">1</span><span class="sxs-lookup"><span data-stu-id="c3671-646">1</span></span>

<span data-ttu-id="c3671-647">2</span><span class="sxs-lookup"><span data-stu-id="c3671-647">2</span></span>

<span data-ttu-id="c3671-648">3</span><span class="sxs-lookup"><span data-stu-id="c3671-648">3</span></span>

<span data-ttu-id="c3671-649">4</span><span class="sxs-lookup"><span data-stu-id="c3671-649">4</span></span>

<span data-ttu-id="c3671-650">5</span><span class="sxs-lookup"><span data-stu-id="c3671-650">5</span></span>

<span data-ttu-id="c3671-651">6</span><span class="sxs-lookup"><span data-stu-id="c3671-651">6</span></span>

<span data-ttu-id="c3671-652">7</span><span class="sxs-lookup"><span data-stu-id="c3671-652">7</span></span>

<span data-ttu-id="c3671-653">8</span><span class="sxs-lookup"><span data-stu-id="c3671-653">8</span></span>

<span data-ttu-id="c3671-654">9</span><span class="sxs-lookup"><span data-stu-id="c3671-654">9</span></span>

<span data-ttu-id="c3671-655">1</span><span class="sxs-lookup"><span data-stu-id="c3671-655">1</span></span><br/> <span data-ttu-id="c3671-656">0</span><span class="sxs-lookup"><span data-stu-id="c3671-656">0</span></span><br/>

<span data-ttu-id="c3671-657">1</span><span class="sxs-lookup"><span data-stu-id="c3671-657">1</span></span>

<span data-ttu-id="c3671-658">2</span><span class="sxs-lookup"><span data-stu-id="c3671-658">2</span></span>

<span data-ttu-id="c3671-659">3</span><span class="sxs-lookup"><span data-stu-id="c3671-659">3</span></span>

<span data-ttu-id="c3671-660">4</span><span class="sxs-lookup"><span data-stu-id="c3671-660">4</span></span>

<span data-ttu-id="c3671-661">5</span><span class="sxs-lookup"><span data-stu-id="c3671-661">5</span></span>

<span data-ttu-id="c3671-662">6</span><span class="sxs-lookup"><span data-stu-id="c3671-662">6</span></span>

<span data-ttu-id="c3671-663">7</span><span class="sxs-lookup"><span data-stu-id="c3671-663">7</span></span>

<span data-ttu-id="c3671-664">8</span><span class="sxs-lookup"><span data-stu-id="c3671-664">8</span></span>

<span data-ttu-id="c3671-665">9</span><span class="sxs-lookup"><span data-stu-id="c3671-665">9</span></span>

<span data-ttu-id="c3671-666">2</span><span class="sxs-lookup"><span data-stu-id="c3671-666">2</span></span><br/> <span data-ttu-id="c3671-667">0</span><span class="sxs-lookup"><span data-stu-id="c3671-667">0</span></span><br/>

<span data-ttu-id="c3671-668">1</span><span class="sxs-lookup"><span data-stu-id="c3671-668">1</span></span>

<span data-ttu-id="c3671-669">2</span><span class="sxs-lookup"><span data-stu-id="c3671-669">2</span></span>

<span data-ttu-id="c3671-670">3</span><span class="sxs-lookup"><span data-stu-id="c3671-670">3</span></span>

<span data-ttu-id="c3671-671">4</span><span class="sxs-lookup"><span data-stu-id="c3671-671">4</span></span>

<span data-ttu-id="c3671-672">5</span><span class="sxs-lookup"><span data-stu-id="c3671-672">5</span></span>

<span data-ttu-id="c3671-673">6</span><span class="sxs-lookup"><span data-stu-id="c3671-673">6</span></span>

<span data-ttu-id="c3671-674">7</span><span class="sxs-lookup"><span data-stu-id="c3671-674">7</span></span>

<span data-ttu-id="c3671-675">8</span><span class="sxs-lookup"><span data-stu-id="c3671-675">8</span></span>

<span data-ttu-id="c3671-676">9</span><span class="sxs-lookup"><span data-stu-id="c3671-676">9</span></span>

<span data-ttu-id="c3671-677">3</span><span class="sxs-lookup"><span data-stu-id="c3671-677">3</span></span><br/> <span data-ttu-id="c3671-678">0</span><span class="sxs-lookup"><span data-stu-id="c3671-678">0</span></span><br/>

<span data-ttu-id="c3671-679">1</span><span class="sxs-lookup"><span data-stu-id="c3671-679">1</span></span>

<span data-ttu-id="c3671-680">vVectorElements</span><span class="sxs-lookup"><span data-stu-id="c3671-680">vVectorElements</span></span>

<span data-ttu-id="c3671-681">vVectorData</span><span class="sxs-lookup"><span data-stu-id="c3671-681">vVectorData</span></span>



 

<span data-ttu-id="c3671-682">**vVectorElements:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im Feld vVectorData angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="c3671-683">**vVectorData:** Ein Array von Elementen, deren Typ durch vType mit dem 0x1000 bit cleared angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="c3671-684">Die Größe eines einzelnen Elements mit fester Länge kann aus der Tabelle des Datentyps fester Länge abgerufen werden, wie in Abschnitt 2.2.1.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="c3671-685">Die Länge dieses Felds in Bytes kann berechnet werden, indem vVectorElements mit der Größe des einzelnen Elements multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="c3671-686">Für Datentypen variabler Länge enthält vVectorData eine Sequenz von aufeinander folgenden gemarshallten einfachen Typen, wobei der Typ durch vType angegeben wird, wobei das 0x1000 Bit gelöscht ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="c3671-687">Dies schließt einen Sonderfall ein, der durch vType VT \_ ARRAY \| VT \_ VARIANT (d.h. 0x100C) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="c3671-688">Die Elemente im vVectorData-Feld MÜSSEN durch 0 bis 3 Auffüllungsbytes getrennt werden, sodass jedes Element bei einem Offset beginnt, der ein Vielfaches von 4 Bytes vom Anfang der Nachricht ist, die dieses Array enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="c3671-689">Wenn auffüllende Bytes vorhanden sind, ist der darin enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="c3671-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="c3671-690">Der Inhalt der Auffüllungsbytes MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3671-691">Für einen vType, der auf VT ARRAY VT VARIANT festgelegt \_ \| \_ ist, ist der Typ für Elemente in dieser Sequenz CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="c3671-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="c3671-692">2.2.1.1.1.3 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="c3671-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="c3671-693">SAFEARRAY wird verwendet, um mehrdimensionale Arrays zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="c3671-694">Die -Struktur enthält Informationen zur Arraygröße sowie die Daten im Array.</span><span class="sxs-lookup"><span data-stu-id="c3671-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="c3671-695">0</span><span class="sxs-lookup"><span data-stu-id="c3671-695">0</span></span>

<span data-ttu-id="c3671-696">1</span><span class="sxs-lookup"><span data-stu-id="c3671-696">1</span></span>

<span data-ttu-id="c3671-697">2</span><span class="sxs-lookup"><span data-stu-id="c3671-697">2</span></span>

<span data-ttu-id="c3671-698">3</span><span class="sxs-lookup"><span data-stu-id="c3671-698">3</span></span>

<span data-ttu-id="c3671-699">4</span><span class="sxs-lookup"><span data-stu-id="c3671-699">4</span></span>

<span data-ttu-id="c3671-700">5</span><span class="sxs-lookup"><span data-stu-id="c3671-700">5</span></span>

<span data-ttu-id="c3671-701">6</span><span class="sxs-lookup"><span data-stu-id="c3671-701">6</span></span>

<span data-ttu-id="c3671-702">7</span><span class="sxs-lookup"><span data-stu-id="c3671-702">7</span></span>

<span data-ttu-id="c3671-703">8</span><span class="sxs-lookup"><span data-stu-id="c3671-703">8</span></span>

<span data-ttu-id="c3671-704">9</span><span class="sxs-lookup"><span data-stu-id="c3671-704">9</span></span>

<span data-ttu-id="c3671-705">1</span><span class="sxs-lookup"><span data-stu-id="c3671-705">1</span></span><br/> <span data-ttu-id="c3671-706">0</span><span class="sxs-lookup"><span data-stu-id="c3671-706">0</span></span><br/>

<span data-ttu-id="c3671-707">1</span><span class="sxs-lookup"><span data-stu-id="c3671-707">1</span></span>

<span data-ttu-id="c3671-708">2</span><span class="sxs-lookup"><span data-stu-id="c3671-708">2</span></span>

<span data-ttu-id="c3671-709">3</span><span class="sxs-lookup"><span data-stu-id="c3671-709">3</span></span>

<span data-ttu-id="c3671-710">4</span><span class="sxs-lookup"><span data-stu-id="c3671-710">4</span></span>

<span data-ttu-id="c3671-711">5</span><span class="sxs-lookup"><span data-stu-id="c3671-711">5</span></span>

<span data-ttu-id="c3671-712">6</span><span class="sxs-lookup"><span data-stu-id="c3671-712">6</span></span>

<span data-ttu-id="c3671-713">7</span><span class="sxs-lookup"><span data-stu-id="c3671-713">7</span></span>

<span data-ttu-id="c3671-714">8</span><span class="sxs-lookup"><span data-stu-id="c3671-714">8</span></span>

<span data-ttu-id="c3671-715">9</span><span class="sxs-lookup"><span data-stu-id="c3671-715">9</span></span>

<span data-ttu-id="c3671-716">2</span><span class="sxs-lookup"><span data-stu-id="c3671-716">2</span></span><br/> <span data-ttu-id="c3671-717">0</span><span class="sxs-lookup"><span data-stu-id="c3671-717">0</span></span><br/>

<span data-ttu-id="c3671-718">1</span><span class="sxs-lookup"><span data-stu-id="c3671-718">1</span></span>

<span data-ttu-id="c3671-719">2</span><span class="sxs-lookup"><span data-stu-id="c3671-719">2</span></span>

<span data-ttu-id="c3671-720">3</span><span class="sxs-lookup"><span data-stu-id="c3671-720">3</span></span>

<span data-ttu-id="c3671-721">4</span><span class="sxs-lookup"><span data-stu-id="c3671-721">4</span></span>

<span data-ttu-id="c3671-722">5</span><span class="sxs-lookup"><span data-stu-id="c3671-722">5</span></span>

<span data-ttu-id="c3671-723">6</span><span class="sxs-lookup"><span data-stu-id="c3671-723">6</span></span>

<span data-ttu-id="c3671-724">7</span><span class="sxs-lookup"><span data-stu-id="c3671-724">7</span></span>

<span data-ttu-id="c3671-725">8</span><span class="sxs-lookup"><span data-stu-id="c3671-725">8</span></span>

<span data-ttu-id="c3671-726">9</span><span class="sxs-lookup"><span data-stu-id="c3671-726">9</span></span>

<span data-ttu-id="c3671-727">3</span><span class="sxs-lookup"><span data-stu-id="c3671-727">3</span></span><br/> <span data-ttu-id="c3671-728">0</span><span class="sxs-lookup"><span data-stu-id="c3671-728">0</span></span><br/>

<span data-ttu-id="c3671-729">1</span><span class="sxs-lookup"><span data-stu-id="c3671-729">1</span></span>

<span data-ttu-id="c3671-730">cDims</span><span class="sxs-lookup"><span data-stu-id="c3671-730">cDims</span></span>

<span data-ttu-id="c3671-731">fFeatures</span><span class="sxs-lookup"><span data-stu-id="c3671-731">fFeatures</span></span>

<span data-ttu-id="c3671-732">cbElements</span><span class="sxs-lookup"><span data-stu-id="c3671-732">cbElements</span></span>

<span data-ttu-id="c3671-733">Rgsabound (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-733">Rgsabound (variable)</span></span>

<span data-ttu-id="c3671-734">vData (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-734">vData (variable)</span></span>



 

<span data-ttu-id="c3671-735">**cDims:** 16-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dimensionen des mehrdimensionalen Arrays angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="c3671-736">**fFeatures:** Ein 16-Bit-Bitfeld.</span><span class="sxs-lookup"><span data-stu-id="c3671-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="c3671-737">Die Werte stellen Features dar, die von Anwendungen der oberen Ebene definiert werden und IGNORIERT WERDEN MÜSSEN.</span><span class="sxs-lookup"><span data-stu-id="c3671-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="c3671-738">**cbElements:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der einzelnen Elemente des Arrays angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="c3671-739">**Rgsabound:** Ein Array, das eine SAFEARRAYBOUND-Struktur enthält, wie in Abschnitt 2.2.1.1.1.4 angegeben, pro Dimension im SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="c3671-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="c3671-740">Dieses Array hat zuerst die linke dimension und die rechteste Dimension die letzte Dimension.</span><span class="sxs-lookup"><span data-stu-id="c3671-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="c3671-741">**vData:** Ein Vektor gemarshallter Elemente eines bestimmten Typs, der durch den vType des enthaltenden CBaseStorageVariant angegeben wird, wobei das Bit gelöscht 0x2000.</span><span class="sxs-lookup"><span data-stu-id="c3671-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="c3671-742">vData wird ähnlich wie VT VECTOR gemarshallt, \_ wie in Abschnitt 2.2.1.1.1.2 angegeben, mit dem Unterschied, dass die Anzahl der Elemente nicht vor dem Vektor gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="c3671-743">Stattdessen wird die Anzahl der Elemente berechnet, indem der cElements-Wert mit allen sicheren Arraygrenzen multipliziert wird, die im Feld Rgsabound angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="c3671-744">Elemente werden in einem Vektor in der Reihenfolge der Dimensionen gespeichert, wobei sie beginnend mit der rechten Dimension iterieren.</span><span class="sxs-lookup"><span data-stu-id="c3671-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="c3671-745">Das folgende Diagramm stellt ein zweidimensionales Beispielarray visuell dar.</span><span class="sxs-lookup"><span data-stu-id="c3671-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="c3671-746">Die erste Dimension hat cElements gleich 4 (horizontal dargestellt) und lLbound gleich 0, und die zweite Dimension weist cElements gleich 2 (vertikal dargestellt) und lLbound gleich 0 auf.</span><span class="sxs-lookup"><span data-stu-id="c3671-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="c3671-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-747">0x00000001</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="c3671-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-748">0x00000002</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="c3671-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-749">0x00000003</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="c3671-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="c3671-750">0x00000005</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="c3671-751">::row:::</span><span class="sxs-lookup"><span data-stu-id="c3671-751">::row:::</span></span>
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

<span data-ttu-id="c3671-752">Mithilfe des obigen Diagramms enthält vData die folgende Sequenz: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (durchlaufen Sie zuerst die äußerste rechte Dimension, und erhöhen Sie dann die nächste Dimension).</span><span class="sxs-lookup"><span data-stu-id="c3671-752">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="c3671-753">Die vorangehende Rgsabound-Klasse (die cElements und Lbound aufzeichnet) wäre: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3671-753">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="c3671-754">2.2.1.1.1.4 SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="c3671-754">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="c3671-755">Die SAFEARRAYBOUND-Struktur stellt die Grenzen einer Dimension eines SAFEARRAY- oder SAFEARRAY2-Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="c3671-755">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="c3671-756">Das Format lautet:</span><span class="sxs-lookup"><span data-stu-id="c3671-756">Its format is:</span></span>



<span data-ttu-id="c3671-757">0</span><span class="sxs-lookup"><span data-stu-id="c3671-757">0</span></span>

<span data-ttu-id="c3671-758">1</span><span class="sxs-lookup"><span data-stu-id="c3671-758">1</span></span>

<span data-ttu-id="c3671-759">2</span><span class="sxs-lookup"><span data-stu-id="c3671-759">2</span></span>

<span data-ttu-id="c3671-760">3</span><span class="sxs-lookup"><span data-stu-id="c3671-760">3</span></span>

<span data-ttu-id="c3671-761">4</span><span class="sxs-lookup"><span data-stu-id="c3671-761">4</span></span>

<span data-ttu-id="c3671-762">5</span><span class="sxs-lookup"><span data-stu-id="c3671-762">5</span></span>

<span data-ttu-id="c3671-763">6</span><span class="sxs-lookup"><span data-stu-id="c3671-763">6</span></span>

<span data-ttu-id="c3671-764">7</span><span class="sxs-lookup"><span data-stu-id="c3671-764">7</span></span>

<span data-ttu-id="c3671-765">8</span><span class="sxs-lookup"><span data-stu-id="c3671-765">8</span></span>

<span data-ttu-id="c3671-766">9</span><span class="sxs-lookup"><span data-stu-id="c3671-766">9</span></span>

<span data-ttu-id="c3671-767">1</span><span class="sxs-lookup"><span data-stu-id="c3671-767">1</span></span><br/> <span data-ttu-id="c3671-768">0</span><span class="sxs-lookup"><span data-stu-id="c3671-768">0</span></span><br/>

<span data-ttu-id="c3671-769">1</span><span class="sxs-lookup"><span data-stu-id="c3671-769">1</span></span>

<span data-ttu-id="c3671-770">2</span><span class="sxs-lookup"><span data-stu-id="c3671-770">2</span></span>

<span data-ttu-id="c3671-771">3</span><span class="sxs-lookup"><span data-stu-id="c3671-771">3</span></span>

<span data-ttu-id="c3671-772">4</span><span class="sxs-lookup"><span data-stu-id="c3671-772">4</span></span>

<span data-ttu-id="c3671-773">5</span><span class="sxs-lookup"><span data-stu-id="c3671-773">5</span></span>

<span data-ttu-id="c3671-774">6</span><span class="sxs-lookup"><span data-stu-id="c3671-774">6</span></span>

<span data-ttu-id="c3671-775">7</span><span class="sxs-lookup"><span data-stu-id="c3671-775">7</span></span>

<span data-ttu-id="c3671-776">8</span><span class="sxs-lookup"><span data-stu-id="c3671-776">8</span></span>

<span data-ttu-id="c3671-777">9</span><span class="sxs-lookup"><span data-stu-id="c3671-777">9</span></span>

<span data-ttu-id="c3671-778">2</span><span class="sxs-lookup"><span data-stu-id="c3671-778">2</span></span><br/> <span data-ttu-id="c3671-779">0</span><span class="sxs-lookup"><span data-stu-id="c3671-779">0</span></span><br/>

<span data-ttu-id="c3671-780">1</span><span class="sxs-lookup"><span data-stu-id="c3671-780">1</span></span>

<span data-ttu-id="c3671-781">2</span><span class="sxs-lookup"><span data-stu-id="c3671-781">2</span></span>

<span data-ttu-id="c3671-782">3</span><span class="sxs-lookup"><span data-stu-id="c3671-782">3</span></span>

<span data-ttu-id="c3671-783">4</span><span class="sxs-lookup"><span data-stu-id="c3671-783">4</span></span>

<span data-ttu-id="c3671-784">5</span><span class="sxs-lookup"><span data-stu-id="c3671-784">5</span></span>

<span data-ttu-id="c3671-785">6</span><span class="sxs-lookup"><span data-stu-id="c3671-785">6</span></span>

<span data-ttu-id="c3671-786">7</span><span class="sxs-lookup"><span data-stu-id="c3671-786">7</span></span>

<span data-ttu-id="c3671-787">8</span><span class="sxs-lookup"><span data-stu-id="c3671-787">8</span></span>

<span data-ttu-id="c3671-788">9</span><span class="sxs-lookup"><span data-stu-id="c3671-788">9</span></span>

<span data-ttu-id="c3671-789">3</span><span class="sxs-lookup"><span data-stu-id="c3671-789">3</span></span><br/> <span data-ttu-id="c3671-790">0</span><span class="sxs-lookup"><span data-stu-id="c3671-790">0</span></span><br/>

<span data-ttu-id="c3671-791">1</span><span class="sxs-lookup"><span data-stu-id="c3671-791">1</span></span>

<span data-ttu-id="c3671-792">cElements</span><span class="sxs-lookup"><span data-stu-id="c3671-792">cElements</span></span>

<span data-ttu-id="c3671-793">lLbound</span><span class="sxs-lookup"><span data-stu-id="c3671-793">lLbound</span></span>



 

<span data-ttu-id="c3671-794">**cElements:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente in der Dimension angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-794">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="c3671-795">**lLbound:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die untere Grenze der Dimension angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-795">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="c3671-796">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="c3671-796">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="c3671-797">SAFEARRAY2 wird verwendet, um mehrdimensionale Arrays in SERIALIZEDPROPERTYVALUE zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-797">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="c3671-798">Die -Struktur enthält Sowohl Begrenzungsinformationen als auch die Daten.</span><span class="sxs-lookup"><span data-stu-id="c3671-798">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="c3671-799">0</span><span class="sxs-lookup"><span data-stu-id="c3671-799">0</span></span>

<span data-ttu-id="c3671-800">1</span><span class="sxs-lookup"><span data-stu-id="c3671-800">1</span></span>

<span data-ttu-id="c3671-801">2</span><span class="sxs-lookup"><span data-stu-id="c3671-801">2</span></span>

<span data-ttu-id="c3671-802">3</span><span class="sxs-lookup"><span data-stu-id="c3671-802">3</span></span>

<span data-ttu-id="c3671-803">4</span><span class="sxs-lookup"><span data-stu-id="c3671-803">4</span></span>

<span data-ttu-id="c3671-804">5</span><span class="sxs-lookup"><span data-stu-id="c3671-804">5</span></span>

<span data-ttu-id="c3671-805">6</span><span class="sxs-lookup"><span data-stu-id="c3671-805">6</span></span>

<span data-ttu-id="c3671-806">7</span><span class="sxs-lookup"><span data-stu-id="c3671-806">7</span></span>

<span data-ttu-id="c3671-807">8</span><span class="sxs-lookup"><span data-stu-id="c3671-807">8</span></span>

<span data-ttu-id="c3671-808">9</span><span class="sxs-lookup"><span data-stu-id="c3671-808">9</span></span>

<span data-ttu-id="c3671-809">1</span><span class="sxs-lookup"><span data-stu-id="c3671-809">1</span></span><br/> <span data-ttu-id="c3671-810">0</span><span class="sxs-lookup"><span data-stu-id="c3671-810">0</span></span><br/>

<span data-ttu-id="c3671-811">1</span><span class="sxs-lookup"><span data-stu-id="c3671-811">1</span></span>

<span data-ttu-id="c3671-812">2</span><span class="sxs-lookup"><span data-stu-id="c3671-812">2</span></span>

<span data-ttu-id="c3671-813">3</span><span class="sxs-lookup"><span data-stu-id="c3671-813">3</span></span>

<span data-ttu-id="c3671-814">4</span><span class="sxs-lookup"><span data-stu-id="c3671-814">4</span></span>

<span data-ttu-id="c3671-815">5</span><span class="sxs-lookup"><span data-stu-id="c3671-815">5</span></span>

<span data-ttu-id="c3671-816">6</span><span class="sxs-lookup"><span data-stu-id="c3671-816">6</span></span>

<span data-ttu-id="c3671-817">7</span><span class="sxs-lookup"><span data-stu-id="c3671-817">7</span></span>

<span data-ttu-id="c3671-818">8</span><span class="sxs-lookup"><span data-stu-id="c3671-818">8</span></span>

<span data-ttu-id="c3671-819">9</span><span class="sxs-lookup"><span data-stu-id="c3671-819">9</span></span>

<span data-ttu-id="c3671-820">2</span><span class="sxs-lookup"><span data-stu-id="c3671-820">2</span></span><br/> <span data-ttu-id="c3671-821">0</span><span class="sxs-lookup"><span data-stu-id="c3671-821">0</span></span><br/>

<span data-ttu-id="c3671-822">1</span><span class="sxs-lookup"><span data-stu-id="c3671-822">1</span></span>

<span data-ttu-id="c3671-823">2</span><span class="sxs-lookup"><span data-stu-id="c3671-823">2</span></span>

<span data-ttu-id="c3671-824">3</span><span class="sxs-lookup"><span data-stu-id="c3671-824">3</span></span>

<span data-ttu-id="c3671-825">4</span><span class="sxs-lookup"><span data-stu-id="c3671-825">4</span></span>

<span data-ttu-id="c3671-826">5</span><span class="sxs-lookup"><span data-stu-id="c3671-826">5</span></span>

<span data-ttu-id="c3671-827">6</span><span class="sxs-lookup"><span data-stu-id="c3671-827">6</span></span>

<span data-ttu-id="c3671-828">7</span><span class="sxs-lookup"><span data-stu-id="c3671-828">7</span></span>

<span data-ttu-id="c3671-829">8</span><span class="sxs-lookup"><span data-stu-id="c3671-829">8</span></span>

<span data-ttu-id="c3671-830">9</span><span class="sxs-lookup"><span data-stu-id="c3671-830">9</span></span>

<span data-ttu-id="c3671-831">3</span><span class="sxs-lookup"><span data-stu-id="c3671-831">3</span></span><br/> <span data-ttu-id="c3671-832">0</span><span class="sxs-lookup"><span data-stu-id="c3671-832">0</span></span><br/>

<span data-ttu-id="c3671-833">1</span><span class="sxs-lookup"><span data-stu-id="c3671-833">1</span></span>

<span data-ttu-id="c3671-834">cDims</span><span class="sxs-lookup"><span data-stu-id="c3671-834">cDims</span></span>

<span data-ttu-id="c3671-835">Rgsabound (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-835">Rgsabound (variable)</span></span>

<span data-ttu-id="c3671-836">vData (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-836">vData (variable)</span></span>



 

<span data-ttu-id="c3671-837">**cDims:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dimensionen von SAFEARRAY2 angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-837">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="c3671-838">**Rgsabound:** Ein Array, das eine SAFEARRAYBOUND-Struktur enthält, wie in Abschnitt 2.2.1.1.1.4 pro Dimension in SAFEARRAY2 angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-838">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="c3671-839">Dieses Array weist zuerst die äußerste linke dimension und zuletzt die rechte Dimension auf.</span><span class="sxs-lookup"><span data-stu-id="c3671-839">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="c3671-840">**vData:** Ein Vektor gemarshallter Elemente eines bestimmten Typs, der durch den dwType des enthaltenden SERIALIZEDPROPERTYVALUE angegeben wird, wobei bit 0x2000 gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-840">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="c3671-841">Das Format von vData entspricht dem Format, das für das vData-Feld von SAFEARRAY in Abschnitt 2.2.1.1.1.3 angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c3671-841">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="c3671-842">2.2.1.2 CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="c3671-842">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="c3671-843">Die CFullPropSpec-Struktur enthält eine Eigenschaftensatz-GUID und einen Eigenschaftenbezeichner, um die Eigenschaft eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c3671-843">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="c3671-844">0</span><span class="sxs-lookup"><span data-stu-id="c3671-844">0</span></span>

<span data-ttu-id="c3671-845">1</span><span class="sxs-lookup"><span data-stu-id="c3671-845">1</span></span>

<span data-ttu-id="c3671-846">2</span><span class="sxs-lookup"><span data-stu-id="c3671-846">2</span></span>

<span data-ttu-id="c3671-847">3</span><span class="sxs-lookup"><span data-stu-id="c3671-847">3</span></span>

<span data-ttu-id="c3671-848">4</span><span class="sxs-lookup"><span data-stu-id="c3671-848">4</span></span>

<span data-ttu-id="c3671-849">5</span><span class="sxs-lookup"><span data-stu-id="c3671-849">5</span></span>

<span data-ttu-id="c3671-850">6</span><span class="sxs-lookup"><span data-stu-id="c3671-850">6</span></span>

<span data-ttu-id="c3671-851">7</span><span class="sxs-lookup"><span data-stu-id="c3671-851">7</span></span>

<span data-ttu-id="c3671-852">8</span><span class="sxs-lookup"><span data-stu-id="c3671-852">8</span></span>

<span data-ttu-id="c3671-853">9</span><span class="sxs-lookup"><span data-stu-id="c3671-853">9</span></span>

<span data-ttu-id="c3671-854">1</span><span class="sxs-lookup"><span data-stu-id="c3671-854">1</span></span><br/> <span data-ttu-id="c3671-855">0</span><span class="sxs-lookup"><span data-stu-id="c3671-855">0</span></span><br/>

<span data-ttu-id="c3671-856">1</span><span class="sxs-lookup"><span data-stu-id="c3671-856">1</span></span>

<span data-ttu-id="c3671-857">2</span><span class="sxs-lookup"><span data-stu-id="c3671-857">2</span></span>

<span data-ttu-id="c3671-858">3</span><span class="sxs-lookup"><span data-stu-id="c3671-858">3</span></span>

<span data-ttu-id="c3671-859">4</span><span class="sxs-lookup"><span data-stu-id="c3671-859">4</span></span>

<span data-ttu-id="c3671-860">5</span><span class="sxs-lookup"><span data-stu-id="c3671-860">5</span></span>

<span data-ttu-id="c3671-861">6</span><span class="sxs-lookup"><span data-stu-id="c3671-861">6</span></span>

<span data-ttu-id="c3671-862">7</span><span class="sxs-lookup"><span data-stu-id="c3671-862">7</span></span>

<span data-ttu-id="c3671-863">8</span><span class="sxs-lookup"><span data-stu-id="c3671-863">8</span></span>

<span data-ttu-id="c3671-864">9</span><span class="sxs-lookup"><span data-stu-id="c3671-864">9</span></span>

<span data-ttu-id="c3671-865">2</span><span class="sxs-lookup"><span data-stu-id="c3671-865">2</span></span><br/> <span data-ttu-id="c3671-866">0</span><span class="sxs-lookup"><span data-stu-id="c3671-866">0</span></span><br/>

<span data-ttu-id="c3671-867">1</span><span class="sxs-lookup"><span data-stu-id="c3671-867">1</span></span>

<span data-ttu-id="c3671-868">2</span><span class="sxs-lookup"><span data-stu-id="c3671-868">2</span></span>

<span data-ttu-id="c3671-869">3</span><span class="sxs-lookup"><span data-stu-id="c3671-869">3</span></span>

<span data-ttu-id="c3671-870">4</span><span class="sxs-lookup"><span data-stu-id="c3671-870">4</span></span>

<span data-ttu-id="c3671-871">5</span><span class="sxs-lookup"><span data-stu-id="c3671-871">5</span></span>

<span data-ttu-id="c3671-872">6</span><span class="sxs-lookup"><span data-stu-id="c3671-872">6</span></span>

<span data-ttu-id="c3671-873">7</span><span class="sxs-lookup"><span data-stu-id="c3671-873">7</span></span>

<span data-ttu-id="c3671-874">8</span><span class="sxs-lookup"><span data-stu-id="c3671-874">8</span></span>

<span data-ttu-id="c3671-875">9</span><span class="sxs-lookup"><span data-stu-id="c3671-875">9</span></span>

<span data-ttu-id="c3671-876">3</span><span class="sxs-lookup"><span data-stu-id="c3671-876">3</span></span><br/> <span data-ttu-id="c3671-877">0</span><span class="sxs-lookup"><span data-stu-id="c3671-877">0</span></span><br/>

<span data-ttu-id="c3671-878">1</span><span class="sxs-lookup"><span data-stu-id="c3671-878">1</span></span>

<span data-ttu-id="c3671-879">\_guidPropSet</span><span class="sxs-lookup"><span data-stu-id="c3671-879">\_guidPropSet</span></span>

<span data-ttu-id="c3671-880">...</span><span class="sxs-lookup"><span data-stu-id="c3671-880">...</span></span>

<span data-ttu-id="c3671-881">...</span><span class="sxs-lookup"><span data-stu-id="c3671-881">...</span></span>

<span data-ttu-id="c3671-882">...</span><span class="sxs-lookup"><span data-stu-id="c3671-882">...</span></span>

<span data-ttu-id="c3671-883">ulKind</span><span class="sxs-lookup"><span data-stu-id="c3671-883">ulKind</span></span>

<span data-ttu-id="c3671-884">PrSpec</span><span class="sxs-lookup"><span data-stu-id="c3671-884">PrSpec</span></span>

<span data-ttu-id="c3671-885">Eigenschaftenname (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-885">Property name (variable)</span></span>



 

<span data-ttu-id="c3671-886">**\_ guidPropSet:** Die GUID des Eigenschaftensatzes, zu dem die Eigenschaft gehört.</span><span class="sxs-lookup"><span data-stu-id="c3671-886">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="c3671-887">**ulKind:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-887">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3671-888">Einer der folgenden Werte unten, der den Inhalt von PrSpec angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-888">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="c3671-889">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-889">Value</span></span>                                            | <span data-ttu-id="c3671-890">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-890">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-891">PRSPEC \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="c3671-891">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="c3671-892">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-892">0x00000000</span></span><br/> | <span data-ttu-id="c3671-893">Das PrSpec-Feld gibt die Anzahl der Nicht-NULL-Zeichen im Feld Eigenschaftenname an.</span><span class="sxs-lookup"><span data-stu-id="c3671-893">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="c3671-894">PRSPEC \_ PROPID</span><span class="sxs-lookup"><span data-stu-id="c3671-894">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="c3671-895">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-895">0x00000001</span></span><br/>  | <span data-ttu-id="c3671-896">Das PrSpec-Feld gibt die Eigenschaften-ID (PROPID) an.</span><span class="sxs-lookup"><span data-stu-id="c3671-896">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="c3671-897">**PrSpec:** Eine 32-Bit-Ganzzahl ohne Vorzeichen mit einer Bedeutung, die durch das ulKind-Feld angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-897">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="c3671-898">**Eigenschaftenname:** Wenn ulKind auf PRSPEC PROPID festgelegt \_ ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-898">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="c3671-899">Wenn ulKind auf PRSPEC LPWSTR festgelegt ist, MUSS dieses Feld ein Array von Unicode-Zeichen enthalten, bei denen die \_ Groß-/Kleinschreibung nicht beachtet wird und das den Namen der Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-899">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="c3671-900">2.2.1.3 CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-900">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="c3671-901">Die CContentRestriction-Struktur enthält eine Zeichenfolge, die mit einer Eigenschaft im Eigenschaftencache übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c3671-901">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="c3671-902">0</span><span class="sxs-lookup"><span data-stu-id="c3671-902">0</span></span>

<span data-ttu-id="c3671-903">1</span><span class="sxs-lookup"><span data-stu-id="c3671-903">1</span></span>

<span data-ttu-id="c3671-904">2</span><span class="sxs-lookup"><span data-stu-id="c3671-904">2</span></span>

<span data-ttu-id="c3671-905">3</span><span class="sxs-lookup"><span data-stu-id="c3671-905">3</span></span>

<span data-ttu-id="c3671-906">4</span><span class="sxs-lookup"><span data-stu-id="c3671-906">4</span></span>

<span data-ttu-id="c3671-907">5</span><span class="sxs-lookup"><span data-stu-id="c3671-907">5</span></span>

<span data-ttu-id="c3671-908">6</span><span class="sxs-lookup"><span data-stu-id="c3671-908">6</span></span>

<span data-ttu-id="c3671-909">7</span><span class="sxs-lookup"><span data-stu-id="c3671-909">7</span></span>

<span data-ttu-id="c3671-910">8</span><span class="sxs-lookup"><span data-stu-id="c3671-910">8</span></span>

<span data-ttu-id="c3671-911">9</span><span class="sxs-lookup"><span data-stu-id="c3671-911">9</span></span>

<span data-ttu-id="c3671-912">1</span><span class="sxs-lookup"><span data-stu-id="c3671-912">1</span></span><br/> <span data-ttu-id="c3671-913">0</span><span class="sxs-lookup"><span data-stu-id="c3671-913">0</span></span><br/>

<span data-ttu-id="c3671-914">1</span><span class="sxs-lookup"><span data-stu-id="c3671-914">1</span></span>

<span data-ttu-id="c3671-915">2</span><span class="sxs-lookup"><span data-stu-id="c3671-915">2</span></span>

<span data-ttu-id="c3671-916">3</span><span class="sxs-lookup"><span data-stu-id="c3671-916">3</span></span>

<span data-ttu-id="c3671-917">4</span><span class="sxs-lookup"><span data-stu-id="c3671-917">4</span></span>

<span data-ttu-id="c3671-918">5</span><span class="sxs-lookup"><span data-stu-id="c3671-918">5</span></span>

<span data-ttu-id="c3671-919">6</span><span class="sxs-lookup"><span data-stu-id="c3671-919">6</span></span>

<span data-ttu-id="c3671-920">7</span><span class="sxs-lookup"><span data-stu-id="c3671-920">7</span></span>

<span data-ttu-id="c3671-921">8</span><span class="sxs-lookup"><span data-stu-id="c3671-921">8</span></span>

<span data-ttu-id="c3671-922">9</span><span class="sxs-lookup"><span data-stu-id="c3671-922">9</span></span>

<span data-ttu-id="c3671-923">2</span><span class="sxs-lookup"><span data-stu-id="c3671-923">2</span></span><br/> <span data-ttu-id="c3671-924">0</span><span class="sxs-lookup"><span data-stu-id="c3671-924">0</span></span><br/>

<span data-ttu-id="c3671-925">1</span><span class="sxs-lookup"><span data-stu-id="c3671-925">1</span></span>

<span data-ttu-id="c3671-926">2</span><span class="sxs-lookup"><span data-stu-id="c3671-926">2</span></span>

<span data-ttu-id="c3671-927">3</span><span class="sxs-lookup"><span data-stu-id="c3671-927">3</span></span>

<span data-ttu-id="c3671-928">4</span><span class="sxs-lookup"><span data-stu-id="c3671-928">4</span></span>

<span data-ttu-id="c3671-929">5</span><span class="sxs-lookup"><span data-stu-id="c3671-929">5</span></span>

<span data-ttu-id="c3671-930">6</span><span class="sxs-lookup"><span data-stu-id="c3671-930">6</span></span>

<span data-ttu-id="c3671-931">7</span><span class="sxs-lookup"><span data-stu-id="c3671-931">7</span></span>

<span data-ttu-id="c3671-932">8</span><span class="sxs-lookup"><span data-stu-id="c3671-932">8</span></span>

<span data-ttu-id="c3671-933">9</span><span class="sxs-lookup"><span data-stu-id="c3671-933">9</span></span>

<span data-ttu-id="c3671-934">3</span><span class="sxs-lookup"><span data-stu-id="c3671-934">3</span></span><br/> <span data-ttu-id="c3671-935">0</span><span class="sxs-lookup"><span data-stu-id="c3671-935">0</span></span><br/>

<span data-ttu-id="c3671-936">1</span><span class="sxs-lookup"><span data-stu-id="c3671-936">1</span></span>

<span data-ttu-id="c3671-937">\_Eigenschaft (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-937">\_Property (variable)</span></span>

<span data-ttu-id="c3671-938">...</span><span class="sxs-lookup"><span data-stu-id="c3671-938">...</span></span>

<span data-ttu-id="c3671-939">Padding1 (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-939">Padding1 (variable)</span></span>

<span data-ttu-id="c3671-940">Cc</span><span class="sxs-lookup"><span data-stu-id="c3671-940">Cc</span></span>

<span data-ttu-id="c3671-941">\_pwcsPhrase (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-941">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="c3671-942">...</span><span class="sxs-lookup"><span data-stu-id="c3671-942">...</span></span>

<span data-ttu-id="c3671-943">Padding2 (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-943">Padding2 (variable)</span></span>

<span data-ttu-id="c3671-944">lcid</span><span class="sxs-lookup"><span data-stu-id="c3671-944">lcid</span></span>

<span data-ttu-id="c3671-945">\_ulGenerateMethod</span><span class="sxs-lookup"><span data-stu-id="c3671-945">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="c3671-946">**\_ Property:** Eine CFullPropSpec-Struktur, wie in Abschnitt 2.2.1.2 angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-946">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="c3671-947">Dieses Feld gibt die Eigenschaft an, für die ein Übereinstimmungsvorgang durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-947">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="c3671-948">**Padding1:** Dieses Feld MUSS 0 bis 3 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-948">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="c3671-949">Die Länge dieses Felds MUSS so lang sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Byte ab dem Anfang der Nachricht ist, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-949">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="c3671-950">Wenn dieses Feld vorhanden ist (d. h. länge ungleich null), ist der enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="c3671-950">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="c3671-951">Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-951">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3671-952">**Cc:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeichen im \_ Feld pwcsPhrase angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-952">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="c3671-953">**\_ pwcsPhrase:** Eine unicode-Zeichenfolge ohne NULL-Terminierung, die das Wort oder den Ausdruck darstellt, das bzw. der mit der Eigenschaft übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-953">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="c3671-954">Dieses Feld DARF NICHT leer sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-954">This field MUST NOT be empty.</span></span> <span data-ttu-id="c3671-955">Das Feld Cc enthält die Länge der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c3671-955">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="c3671-956">**Padding2:** Dieses Feld MUSS 0 bis 3 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-956">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="c3671-957">Die Länge dieses Felds MUSS so lang sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Byte ab dem Anfang der Nachricht ist, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-957">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="c3671-958">Wenn dieses Feld vorhanden ist (d. h. länge ungleich null), ist der enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="c3671-958">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="c3671-959">Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-959">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3671-960">**Lcid:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Locale von \_ pwcsPhrase angibt, wie in \[ MS-GPSI \] Anhang A angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-960">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="c3671-961">**\_ ulGenerateMethod:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Methode angibt, die beim Generieren alternativer Wortformen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-961">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="c3671-962">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-962">Value</span></span>                                                       | <span data-ttu-id="c3671-963">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-963">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-964">GENERATE \_ METHOD \_ EXACT</span><span class="sxs-lookup"><span data-stu-id="c3671-964">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="c3671-965">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-965">0x00000000</span></span><br/>    | <span data-ttu-id="c3671-966">Genaue Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="c3671-966">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c3671-967">\_METHODENPRÄFIX \_ GENERIEREN</span><span class="sxs-lookup"><span data-stu-id="c3671-967">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="c3671-968">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-968">0x00000001</span></span> <br/>  | <span data-ttu-id="c3671-969">Präfix-Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="c3671-969">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="c3671-970">GENERATE \_ METHOD \_ INFLECT</span><span class="sxs-lookup"><span data-stu-id="c3671-970">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="c3671-971">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-971">0x00000002</span></span><br/> | <span data-ttu-id="c3671-972">Entspricht den Inflectionen eines Worts.</span><span class="sxs-lookup"><span data-stu-id="c3671-972">Matches inflections of a word.</span></span> <span data-ttu-id="c3671-973">Eine Inflection eines Worts ist eine Variante des Stammworts im gleichen Sprachteil, der gemäß linguistischen Regeln einer bestimmten Sprache geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c3671-973">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="c3671-974">Beispiele für die Inflectionen des Verbs "swim" auf Englisch sind "swim", "swims", "swam" und "swam".</span><span class="sxs-lookup"><span data-stu-id="c3671-974">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="c3671-975">2.2.1.4 CKey</span><span class="sxs-lookup"><span data-stu-id="c3671-975">2.2.1.4 CKey</span></span>

<span data-ttu-id="c3671-976">Die CKey-Struktur enthält einen Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="c3671-976">The CKey structure contains a property value.</span></span>



<span data-ttu-id="c3671-977">0</span><span class="sxs-lookup"><span data-stu-id="c3671-977">0</span></span>

<span data-ttu-id="c3671-978">1</span><span class="sxs-lookup"><span data-stu-id="c3671-978">1</span></span>

<span data-ttu-id="c3671-979">2</span><span class="sxs-lookup"><span data-stu-id="c3671-979">2</span></span>

<span data-ttu-id="c3671-980">3</span><span class="sxs-lookup"><span data-stu-id="c3671-980">3</span></span>

<span data-ttu-id="c3671-981">4</span><span class="sxs-lookup"><span data-stu-id="c3671-981">4</span></span>

<span data-ttu-id="c3671-982">5</span><span class="sxs-lookup"><span data-stu-id="c3671-982">5</span></span>

<span data-ttu-id="c3671-983">6</span><span class="sxs-lookup"><span data-stu-id="c3671-983">6</span></span>

<span data-ttu-id="c3671-984">7</span><span class="sxs-lookup"><span data-stu-id="c3671-984">7</span></span>

<span data-ttu-id="c3671-985">8</span><span class="sxs-lookup"><span data-stu-id="c3671-985">8</span></span>

<span data-ttu-id="c3671-986">9</span><span class="sxs-lookup"><span data-stu-id="c3671-986">9</span></span>

<span data-ttu-id="c3671-987">1</span><span class="sxs-lookup"><span data-stu-id="c3671-987">1</span></span><br/> <span data-ttu-id="c3671-988">0</span><span class="sxs-lookup"><span data-stu-id="c3671-988">0</span></span><br/>

<span data-ttu-id="c3671-989">1</span><span class="sxs-lookup"><span data-stu-id="c3671-989">1</span></span>

<span data-ttu-id="c3671-990">2</span><span class="sxs-lookup"><span data-stu-id="c3671-990">2</span></span>

<span data-ttu-id="c3671-991">3</span><span class="sxs-lookup"><span data-stu-id="c3671-991">3</span></span>

<span data-ttu-id="c3671-992">4</span><span class="sxs-lookup"><span data-stu-id="c3671-992">4</span></span>

<span data-ttu-id="c3671-993">5</span><span class="sxs-lookup"><span data-stu-id="c3671-993">5</span></span>

<span data-ttu-id="c3671-994">6</span><span class="sxs-lookup"><span data-stu-id="c3671-994">6</span></span>

<span data-ttu-id="c3671-995">7</span><span class="sxs-lookup"><span data-stu-id="c3671-995">7</span></span>

<span data-ttu-id="c3671-996">8</span><span class="sxs-lookup"><span data-stu-id="c3671-996">8</span></span>

<span data-ttu-id="c3671-997">9</span><span class="sxs-lookup"><span data-stu-id="c3671-997">9</span></span>

<span data-ttu-id="c3671-998">2</span><span class="sxs-lookup"><span data-stu-id="c3671-998">2</span></span><br/> <span data-ttu-id="c3671-999">0</span><span class="sxs-lookup"><span data-stu-id="c3671-999">0</span></span><br/>

<span data-ttu-id="c3671-1000">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1000">1</span></span>

<span data-ttu-id="c3671-1001">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1001">2</span></span>

<span data-ttu-id="c3671-1002">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1002">3</span></span>

<span data-ttu-id="c3671-1003">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1003">4</span></span>

<span data-ttu-id="c3671-1004">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1004">5</span></span>

<span data-ttu-id="c3671-1005">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1005">6</span></span>

<span data-ttu-id="c3671-1006">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1006">7</span></span>

<span data-ttu-id="c3671-1007">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1007">8</span></span>

<span data-ttu-id="c3671-1008">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1008">9</span></span>

<span data-ttu-id="c3671-1009">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1009">3</span></span><br/> <span data-ttu-id="c3671-1010">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1010">0</span></span><br/>

<span data-ttu-id="c3671-1011">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1011">1</span></span>

<span data-ttu-id="c3671-1012">PROPID</span><span class="sxs-lookup"><span data-stu-id="c3671-1012">PROPID</span></span>

<span data-ttu-id="c3671-1013">Cb</span><span class="sxs-lookup"><span data-stu-id="c3671-1013">Cb</span></span>

<span data-ttu-id="c3671-1014">buf (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1014">buf (variable)</span></span>



 

<span data-ttu-id="c3671-1015">**PROPID:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Eigenschaften-ID darstellt, wie in Abschnitt 1.8.1 erläutert.</span><span class="sxs-lookup"><span data-stu-id="c3671-1015">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="c3671-1016">Bekannte Werte sind:</span><span class="sxs-lookup"><span data-stu-id="c3671-1016">Well-known values are:</span></span>



| <span data-ttu-id="c3671-1017">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-1017">Value</span></span>      | <span data-ttu-id="c3671-1018">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-1018">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="c3671-1019">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="c3671-1019">0xFFFFFFFF</span></span> | <span data-ttu-id="c3671-1020">Stellt eine ungültige Eigenschaften-ID dar und DARF NICHT verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1020">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="c3671-1021">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="c3671-1021">0xFFFFFFFE</span></span> | <span data-ttu-id="c3671-1022">Stellt eine ungültige Eigenschaften-ID dar und DARF NICHT verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1022">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="c3671-1023">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-1023">0x00000000</span></span> | <span data-ttu-id="c3671-1024">Stellt eine beliebige Eigenschaften-ID dar.</span><span class="sxs-lookup"><span data-stu-id="c3671-1024">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="c3671-1025">**Cb:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge von buf in Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-1025">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="c3671-1026">**buf:** Eine Bytesequenz, die den Wert der Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1026">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="c3671-1027">2.2.1.5 CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-1027">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="c3671-1028">Die CInternalPropertyRestriction-Struktur enthält einen Eigenschaftswert, der mit einem Vorgang übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1028">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="c3671-1029">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1029">0</span></span>

<span data-ttu-id="c3671-1030">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1030">1</span></span>

<span data-ttu-id="c3671-1031">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1031">2</span></span>

<span data-ttu-id="c3671-1032">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1032">3</span></span>

<span data-ttu-id="c3671-1033">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1033">4</span></span>

<span data-ttu-id="c3671-1034">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1034">5</span></span>

<span data-ttu-id="c3671-1035">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1035">6</span></span>

<span data-ttu-id="c3671-1036">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1036">7</span></span>

<span data-ttu-id="c3671-1037">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1037">8</span></span>

<span data-ttu-id="c3671-1038">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1038">9</span></span>

<span data-ttu-id="c3671-1039">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1039">1</span></span><br/> <span data-ttu-id="c3671-1040">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1040">0</span></span><br/>

<span data-ttu-id="c3671-1041">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1041">1</span></span>

<span data-ttu-id="c3671-1042">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1042">2</span></span>

<span data-ttu-id="c3671-1043">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1043">3</span></span>

<span data-ttu-id="c3671-1044">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1044">4</span></span>

<span data-ttu-id="c3671-1045">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1045">5</span></span>

<span data-ttu-id="c3671-1046">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1046">6</span></span>

<span data-ttu-id="c3671-1047">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1047">7</span></span>

<span data-ttu-id="c3671-1048">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1048">8</span></span>

<span data-ttu-id="c3671-1049">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1049">9</span></span>

<span data-ttu-id="c3671-1050">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1050">2</span></span><br/> <span data-ttu-id="c3671-1051">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1051">0</span></span><br/>

<span data-ttu-id="c3671-1052">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1052">1</span></span>

<span data-ttu-id="c3671-1053">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1053">2</span></span>

<span data-ttu-id="c3671-1054">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1054">3</span></span>

<span data-ttu-id="c3671-1055">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1055">4</span></span>

<span data-ttu-id="c3671-1056">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1056">5</span></span>

<span data-ttu-id="c3671-1057">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1057">6</span></span>

<span data-ttu-id="c3671-1058">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1058">7</span></span>

<span data-ttu-id="c3671-1059">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1059">8</span></span>

<span data-ttu-id="c3671-1060">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1060">9</span></span>

<span data-ttu-id="c3671-1061">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1061">3</span></span><br/> <span data-ttu-id="c3671-1062">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1062">0</span></span><br/>

<span data-ttu-id="c3671-1063">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1063">1</span></span>

<span data-ttu-id="c3671-1064">\_relop</span><span class="sxs-lookup"><span data-stu-id="c3671-1064">\_relop</span></span>

<span data-ttu-id="c3671-1065">\_Pid</span><span class="sxs-lookup"><span data-stu-id="c3671-1065">\_pid</span></span>

<span data-ttu-id="c3671-1066">\_prval (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1066">\_prval (variable)</span></span>

<span data-ttu-id="c3671-1067">restrictionPresent</span><span class="sxs-lookup"><span data-stu-id="c3671-1067">restrictionPresent</span></span>

<span data-ttu-id="c3671-1068">nextRestriction (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1068">nextRestriction (variable)</span></span>



 

<span data-ttu-id="c3671-1069">**\_ relop**: Eine 32-Bit-Ganzzahl, die die Beziehung angibt, die für die -Eigenschaft ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1069">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="c3671-1070">MUSS einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="c3671-1070">MUST be one of the following values:</span></span>



| <span data-ttu-id="c3671-1071">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-1071">Value</span></span>                 | <span data-ttu-id="c3671-1072">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-1072">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-1073">PRLT-0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-1073">PRLT 0x00000000</span></span>       | <span data-ttu-id="c3671-1074">Ein Kleiner-als-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1074">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="c3671-1075">PRLE-0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-1075">PRLE 0x00000001</span></span>       | <span data-ttu-id="c3671-1076">Ein Kleiner-als- oder Gleich-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1076">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="c3671-1077">PRGT-0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-1077">PRGT 0x00000002</span></span>       | <span data-ttu-id="c3671-1078">Ein Größer-als-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1078">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="c3671-1079">PRGE-0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-1079">PRGE 0x00000003</span></span>       | <span data-ttu-id="c3671-1080">Ein Größer-als- oder Gleich-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1080">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="c3671-1081">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3671-1081">PREQ 0x00000004</span></span>       | <span data-ttu-id="c3671-1082">Ein Gleichheitsvergleich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1082">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="c3671-1083">PRNE-0x00000005</span><span class="sxs-lookup"><span data-stu-id="c3671-1083">PRNE 0x00000005</span></span>       | <span data-ttu-id="c3671-1084">Ein ungleicher Vergleich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1084">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="c3671-1085">PRRE-0x00000006</span><span class="sxs-lookup"><span data-stu-id="c3671-1085">PRRE 0x00000006</span></span>       | <span data-ttu-id="c3671-1086">Ein Vergleich eines regulären Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="c3671-1086">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="c3671-1087">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="c3671-1087">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="c3671-1088">Ein bitweises AND, das den rechten Operanden zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1088">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="c3671-1089">PRSomeBits-0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3671-1089">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="c3671-1090">Ein bitweises AND, das einen Wert ungleich 0 (null) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1090">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="c3671-1091">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="c3671-1091">PRAll 0x00000100</span></span>      | <span data-ttu-id="c3671-1092">Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden und ist nur true, wenn der Vorgang für alle Zeilen true ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-1092">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="c3671-1093">PRAny-0x00000200</span><span class="sxs-lookup"><span data-stu-id="c3671-1093">PRAny 0x00000200</span></span>      | <span data-ttu-id="c3671-1094">Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden, und ist true, wenn der Vorgang für eine Zeile true ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-1094">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="c3671-1095">**\_ pid:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Eigenschaften-ID darstellt (siehe PROPID in Abschnitt 2.2.1.4).</span><span class="sxs-lookup"><span data-stu-id="c3671-1095">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="c3671-1096">**\_ prval:** Ein CBaseStorageVariant, das den Wert enthält, der mit der -Eigenschaft in Beziehung stehen soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1096">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="c3671-1097">**restrictionPresent:** Ein Bytewert, der angibt, ob das nextRestriction-Feld vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-1097">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="c3671-1098">MUSS entweder auf 0x00 oder 0x01 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1098">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="c3671-1099">Wenn sie auf 0x01 festgelegt ist, gibt restrictionPresent an, dass das Feld nextRestriction vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-1099">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="c3671-1100">Wenn sie auf 0x00 festgelegt ist, gibt restrictionPresent an, dass das Feld nextRestriction nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-1100">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="c3671-1101">**nextRestriction:** Eine CRestriction-Struktur, wie in Abschnitt 2.2.1.16 angegeben, die eine weitere Einschränkung angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1101">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="c3671-1102">2.2.1.6 CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-1102">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="c3671-1103">Die CNatLanguageRestriction-Struktur enthält eine Abfrageübersprechung in **natürlicher Sprache** für eine Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c3671-1103">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="c3671-1104">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1104">0</span></span>

<span data-ttu-id="c3671-1105">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1105">1</span></span>

<span data-ttu-id="c3671-1106">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1106">2</span></span>

<span data-ttu-id="c3671-1107">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1107">3</span></span>

<span data-ttu-id="c3671-1108">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1108">4</span></span>

<span data-ttu-id="c3671-1109">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1109">5</span></span>

<span data-ttu-id="c3671-1110">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1110">6</span></span>

<span data-ttu-id="c3671-1111">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1111">7</span></span>

<span data-ttu-id="c3671-1112">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1112">8</span></span>

<span data-ttu-id="c3671-1113">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1113">9</span></span>

<span data-ttu-id="c3671-1114">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1114">1</span></span><br/> <span data-ttu-id="c3671-1115">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1115">0</span></span><br/>

<span data-ttu-id="c3671-1116">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1116">1</span></span>

<span data-ttu-id="c3671-1117">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1117">2</span></span>

<span data-ttu-id="c3671-1118">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1118">3</span></span>

<span data-ttu-id="c3671-1119">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1119">4</span></span>

<span data-ttu-id="c3671-1120">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1120">5</span></span>

<span data-ttu-id="c3671-1121">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1121">6</span></span>

<span data-ttu-id="c3671-1122">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1122">7</span></span>

<span data-ttu-id="c3671-1123">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1123">8</span></span>

<span data-ttu-id="c3671-1124">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1124">9</span></span>

<span data-ttu-id="c3671-1125">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1125">2</span></span><br/> <span data-ttu-id="c3671-1126">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1126">0</span></span><br/>

<span data-ttu-id="c3671-1127">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1127">1</span></span>

<span data-ttu-id="c3671-1128">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1128">2</span></span>

<span data-ttu-id="c3671-1129">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1129">3</span></span>

<span data-ttu-id="c3671-1130">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1130">4</span></span>

<span data-ttu-id="c3671-1131">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1131">5</span></span>

<span data-ttu-id="c3671-1132">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1132">6</span></span>

<span data-ttu-id="c3671-1133">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1133">7</span></span>

<span data-ttu-id="c3671-1134">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1134">8</span></span>

<span data-ttu-id="c3671-1135">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1135">9</span></span>

<span data-ttu-id="c3671-1136">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1136">3</span></span><br/> <span data-ttu-id="c3671-1137">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1137">0</span></span><br/>

<span data-ttu-id="c3671-1138">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1138">1</span></span>

<span data-ttu-id="c3671-1139">\_Eigenschaft (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1139">\_Property (variable)</span></span>

<span data-ttu-id="c3671-1140">...</span><span class="sxs-lookup"><span data-stu-id="c3671-1140">...</span></span>

<span data-ttu-id="c3671-1141">\_Auf padding \_ cc (variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1141">\_padding\_cc (variable)</span></span>

<span data-ttu-id="c3671-1142">Cc</span><span class="sxs-lookup"><span data-stu-id="c3671-1142">Cc</span></span>

<span data-ttu-id="c3671-1143">\_pwcsPhrase (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1143">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="c3671-1144">...</span><span class="sxs-lookup"><span data-stu-id="c3671-1144">...</span></span>

<span data-ttu-id="c3671-1145">\_Auf padding \_ lcid (variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1145">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="c3671-1146">Lcid</span><span class="sxs-lookup"><span data-stu-id="c3671-1146">Lcid</span></span>



 

<span data-ttu-id="c3671-1147">**\_ Property:** Eine CFullPropSpec-Struktur, wie in Abschnitt 2.2.1.3 angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-1147">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="c3671-1148">Dieses Feld gibt die Eigenschaft an, für die der Ab übereinstimmungsvorgang durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1148">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="c3671-1149">**\_ padding \_ cc:** Dieses Feld MUSS 0 bis 3 Bytes lang sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1149">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="c3671-1150">Die Länge dieses Felds MUSS so lang sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Byte ab dem Anfang der Nachricht ist, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-1150">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="c3671-1151">Wenn dieses Feld vorhanden ist (d. h. länge ungleich null), ist der enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1151">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="c3671-1152">Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1152">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3671-1153">**Cc:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1153">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3671-1154">Die Anzahl der Zeichen im \_ Feld pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="c3671-1154">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="c3671-1155">**\_ pwcsPhrase:** Eine unicode-Zeichenfolge ohne NULL-Terminierung, die das Wort oder den Ausdruck darstellt, das bzw. der mit der Eigenschaft übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1155">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="c3671-1156">DARF NICHT leer sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1156">MUST NOT be empty.</span></span> <span data-ttu-id="c3671-1157">Das Feld Cc enthält die Länge der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c3671-1157">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="c3671-1158">**\_ padding \_ lcid**: Dieses Feld MUSS 0 bis 3 Bytes lang sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1158">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="c3671-1159">Die Länge dieses Felds MUSS so lang sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Byte ab dem Anfang der Nachricht ist, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-1159">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="c3671-1160">Wenn dieses Feld vorhanden ist (d. h. länge ungleich null), ist der enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1160">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="c3671-1161">Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1161">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3671-1162">**Lcid:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Locale von \_ pwcsPhrase angibt, wie in \[ MS-GPSI \] Anhang A angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-1162">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="c3671-1163">2.2.1.7 CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-1163">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="c3671-1164">Die CNodeRestriction-Struktur enthält ein Array von **Befehlsstrukturknoten,** die die Einschränkungen für die Abfrage angeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-1164">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="c3671-1165">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1165">0</span></span>

<span data-ttu-id="c3671-1166">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1166">1</span></span>

<span data-ttu-id="c3671-1167">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1167">2</span></span>

<span data-ttu-id="c3671-1168">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1168">3</span></span>

<span data-ttu-id="c3671-1169">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1169">4</span></span>

<span data-ttu-id="c3671-1170">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1170">5</span></span>

<span data-ttu-id="c3671-1171">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1171">6</span></span>

<span data-ttu-id="c3671-1172">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1172">7</span></span>

<span data-ttu-id="c3671-1173">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1173">8</span></span>

<span data-ttu-id="c3671-1174">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1174">9</span></span>

<span data-ttu-id="c3671-1175">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1175">1</span></span><br/> <span data-ttu-id="c3671-1176">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1176">0</span></span><br/>

<span data-ttu-id="c3671-1177">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1177">1</span></span>

<span data-ttu-id="c3671-1178">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1178">2</span></span>

<span data-ttu-id="c3671-1179">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1179">3</span></span>

<span data-ttu-id="c3671-1180">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1180">4</span></span>

<span data-ttu-id="c3671-1181">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1181">5</span></span>

<span data-ttu-id="c3671-1182">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1182">6</span></span>

<span data-ttu-id="c3671-1183">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1183">7</span></span>

<span data-ttu-id="c3671-1184">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1184">8</span></span>

<span data-ttu-id="c3671-1185">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1185">9</span></span>

<span data-ttu-id="c3671-1186">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1186">2</span></span><br/> <span data-ttu-id="c3671-1187">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1187">0</span></span><br/>

<span data-ttu-id="c3671-1188">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1188">1</span></span>

<span data-ttu-id="c3671-1189">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1189">2</span></span>

<span data-ttu-id="c3671-1190">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1190">3</span></span>

<span data-ttu-id="c3671-1191">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1191">4</span></span>

<span data-ttu-id="c3671-1192">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1192">5</span></span>

<span data-ttu-id="c3671-1193">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1193">6</span></span>

<span data-ttu-id="c3671-1194">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1194">7</span></span>

<span data-ttu-id="c3671-1195">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1195">8</span></span>

<span data-ttu-id="c3671-1196">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1196">9</span></span>

<span data-ttu-id="c3671-1197">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1197">3</span></span><br/> <span data-ttu-id="c3671-1198">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1198">0</span></span><br/>

<span data-ttu-id="c3671-1199">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1199">1</span></span>

<span data-ttu-id="c3671-1200">\_cNode</span><span class="sxs-lookup"><span data-stu-id="c3671-1200">\_cNode</span></span>

<span data-ttu-id="c3671-1201">\_paNode (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1201">\_paNode (variable)</span></span>



 

<span data-ttu-id="c3671-1202">**\_ cNode:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der im PaNode-Feld enthaltenen CRestriction-Strukturen \_ angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1202">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="c3671-1203">**\_ paNode:** Ein Array von CRestriction-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1203">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="c3671-1204">Strukturen im Array MÜSSEN durch 0 bis 3 Auf abstandsbytes getrennt werden, damit jede Struktur an einem Offset beginnt, der ein Vielfaches von 4 Bytes vom Anfang der Nachricht ist, die dieses Array enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-1204">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="c3671-1205">Wenn Auf padding bytes vorhanden sind, ist der Wert, den sie enthalten, willkürlich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1205">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="c3671-1206">Der Inhalt der Auf padding-Bytes MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1206">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="c3671-1207">2.2.1.8 COccRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-1207">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="c3671-1208">Die COccRestriction-Struktur enthält die Position eines Worts in einem Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="c3671-1208">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="c3671-1209">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1209">0</span></span>

<span data-ttu-id="c3671-1210">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1210">1</span></span>

<span data-ttu-id="c3671-1211">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1211">2</span></span>

<span data-ttu-id="c3671-1212">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1212">3</span></span>

<span data-ttu-id="c3671-1213">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1213">4</span></span>

<span data-ttu-id="c3671-1214">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1214">5</span></span>

<span data-ttu-id="c3671-1215">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1215">6</span></span>

<span data-ttu-id="c3671-1216">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1216">7</span></span>

<span data-ttu-id="c3671-1217">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1217">8</span></span>

<span data-ttu-id="c3671-1218">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1218">9</span></span>

<span data-ttu-id="c3671-1219">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1219">1</span></span><br/> <span data-ttu-id="c3671-1220">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1220">0</span></span><br/>

<span data-ttu-id="c3671-1221">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1221">1</span></span>

<span data-ttu-id="c3671-1222">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1222">2</span></span>

<span data-ttu-id="c3671-1223">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1223">3</span></span>

<span data-ttu-id="c3671-1224">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1224">4</span></span>

<span data-ttu-id="c3671-1225">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1225">5</span></span>

<span data-ttu-id="c3671-1226">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1226">6</span></span>

<span data-ttu-id="c3671-1227">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1227">7</span></span>

<span data-ttu-id="c3671-1228">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1228">8</span></span>

<span data-ttu-id="c3671-1229">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1229">9</span></span>

<span data-ttu-id="c3671-1230">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1230">2</span></span><br/> <span data-ttu-id="c3671-1231">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1231">0</span></span><br/>

<span data-ttu-id="c3671-1232">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1232">1</span></span>

<span data-ttu-id="c3671-1233">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1233">2</span></span>

<span data-ttu-id="c3671-1234">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1234">3</span></span>

<span data-ttu-id="c3671-1235">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1235">4</span></span>

<span data-ttu-id="c3671-1236">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1236">5</span></span>

<span data-ttu-id="c3671-1237">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1237">6</span></span>

<span data-ttu-id="c3671-1238">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1238">7</span></span>

<span data-ttu-id="c3671-1239">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1239">8</span></span>

<span data-ttu-id="c3671-1240">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1240">9</span></span>

<span data-ttu-id="c3671-1241">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1241">3</span></span><br/> <span data-ttu-id="c3671-1242">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1242">0</span></span><br/>

<span data-ttu-id="c3671-1243">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1243">1</span></span>

<span data-ttu-id="c3671-1244">\_Occ</span><span class="sxs-lookup"><span data-stu-id="c3671-1244">\_occ</span></span>

<span data-ttu-id="c3671-1245">\_cPrevNoiseWords</span><span class="sxs-lookup"><span data-stu-id="c3671-1245">\_cPrevNoiseWords</span></span>

<span data-ttu-id="c3671-1246">\_cNextNoiseWords</span><span class="sxs-lookup"><span data-stu-id="c3671-1246">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="c3671-1247">**\_ occ:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Offset des Worts in einer Abfragezeichenfolge in Worteinheiten angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1247">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="c3671-1248">Ein Wort, wie es in dieser Spezifikation verwendet wird, ist eine Spracheinheit in jedem Beliebigen, das eine Bedeutung hat.</span><span class="sxs-lookup"><span data-stu-id="c3671-1248">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="c3671-1249">**\_ cPrevNoiseWords:** Eine 32-Bit-Ganzzahl ohne  Vorzeichen, die die Anzahl der Rauschwörter enthält, die zwischen diesem Wort und dem vorherigen Wort im Ausdruck auftreten.</span><span class="sxs-lookup"><span data-stu-id="c3671-1249">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="c3671-1250">**\_ cNextNoiseWords:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Rauschwörter enthält, die zwischen diesem Wort und dem nächsten Wort im Ausdruck auftreten.</span><span class="sxs-lookup"><span data-stu-id="c3671-1250">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="c3671-1251">2.2.1.9 CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-1251">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="c3671-1252">Die CPropertyRestriction-Struktur enthält einen Eigenschaftswert, der mit einem Vorgang übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1252">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="c3671-1253">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1253">0</span></span>

<span data-ttu-id="c3671-1254">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1254">1</span></span>

<span data-ttu-id="c3671-1255">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1255">2</span></span>

<span data-ttu-id="c3671-1256">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1256">3</span></span>

<span data-ttu-id="c3671-1257">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1257">4</span></span>

<span data-ttu-id="c3671-1258">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1258">5</span></span>

<span data-ttu-id="c3671-1259">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1259">6</span></span>

<span data-ttu-id="c3671-1260">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1260">7</span></span>

<span data-ttu-id="c3671-1261">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1261">8</span></span>

<span data-ttu-id="c3671-1262">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1262">9</span></span>

<span data-ttu-id="c3671-1263">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1263">1</span></span><br/> <span data-ttu-id="c3671-1264">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1264">0</span></span><br/>

<span data-ttu-id="c3671-1265">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1265">1</span></span>

<span data-ttu-id="c3671-1266">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1266">2</span></span>

<span data-ttu-id="c3671-1267">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1267">3</span></span>

<span data-ttu-id="c3671-1268">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1268">4</span></span>

<span data-ttu-id="c3671-1269">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1269">5</span></span>

<span data-ttu-id="c3671-1270">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1270">6</span></span>

<span data-ttu-id="c3671-1271">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1271">7</span></span>

<span data-ttu-id="c3671-1272">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1272">8</span></span>

<span data-ttu-id="c3671-1273">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1273">9</span></span>

<span data-ttu-id="c3671-1274">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1274">2</span></span><br/> <span data-ttu-id="c3671-1275">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1275">0</span></span><br/>

<span data-ttu-id="c3671-1276">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1276">1</span></span>

<span data-ttu-id="c3671-1277">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1277">2</span></span>

<span data-ttu-id="c3671-1278">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1278">3</span></span>

<span data-ttu-id="c3671-1279">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1279">4</span></span>

<span data-ttu-id="c3671-1280">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1280">5</span></span>

<span data-ttu-id="c3671-1281">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1281">6</span></span>

<span data-ttu-id="c3671-1282">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1282">7</span></span>

<span data-ttu-id="c3671-1283">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1283">8</span></span>

<span data-ttu-id="c3671-1284">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1284">9</span></span>

<span data-ttu-id="c3671-1285">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1285">3</span></span><br/> <span data-ttu-id="c3671-1286">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1286">0</span></span><br/>

<span data-ttu-id="c3671-1287">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1287">1</span></span>

<span data-ttu-id="c3671-1288">\_relop</span><span class="sxs-lookup"><span data-stu-id="c3671-1288">\_relop</span></span>

<span data-ttu-id="c3671-1289">\_Eigenschaft (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1289">\_Property (variable)</span></span>

<span data-ttu-id="c3671-1290">\_prval (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1290">\_prval (variable)</span></span>



 

<span data-ttu-id="c3671-1291">**\_ relop:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Beziehung angibt, die für die -Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1291">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="c3671-1292">MUSS einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1292">MUST be one of the following values.</span></span>



| <span data-ttu-id="c3671-1293">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-1293">Value</span></span>                 | <span data-ttu-id="c3671-1294">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-1294">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-1295">PRLT-0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-1295">PRLT 0x00000000</span></span>       | <span data-ttu-id="c3671-1296">Ein Kleiner-als-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1296">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="c3671-1297">PRLE-0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-1297">PRLE 0x00000001</span></span>       | <span data-ttu-id="c3671-1298">Ein Kleiner-als- oder gleich-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1298">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="c3671-1299">PRGT-0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-1299">PRGT 0x00000002</span></span>       | <span data-ttu-id="c3671-1300">Ein Größer-als-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1300">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="c3671-1301">PRGE-0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-1301">PRGE 0x00000003</span></span>       | <span data-ttu-id="c3671-1302">Ein Größer-als- oder gleich-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1302">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="c3671-1303">PREQ-0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3671-1303">PREQ 0x00000004</span></span>       | <span data-ttu-id="c3671-1304">Ein Gleichheitsvergleich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1304">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="c3671-1305">PRNE-0x00000005</span><span class="sxs-lookup"><span data-stu-id="c3671-1305">PRNE 0x00000005</span></span>       | <span data-ttu-id="c3671-1306">Ein nicht gleicher Vergleich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1306">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="c3671-1307">PRRE-0x00000006</span><span class="sxs-lookup"><span data-stu-id="c3671-1307">PRRE 0x00000006</span></span>       | <span data-ttu-id="c3671-1308">Ein Vergleich mit regulären Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="c3671-1308">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="c3671-1309">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="c3671-1309">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="c3671-1310">Ein bitweises AND, das den rechten Operanden zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1310">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="c3671-1311">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3671-1311">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="c3671-1312">Ein bitweises AND, das einen Wert ungleich 0 (null) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1312">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="c3671-1313">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="c3671-1313">PRAll 0x00000100</span></span>      | <span data-ttu-id="c3671-1314">Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden und ist nur true, wenn der Vorgang für alle Zeilen true ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-1314">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="c3671-1315">PRAny-0x00000200</span><span class="sxs-lookup"><span data-stu-id="c3671-1315">PRAny 0x00000200</span></span>      | <span data-ttu-id="c3671-1316">Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden, und ist TRUE, wenn der Vorgang für eine zeile true ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-1316">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="c3671-1317">**\_ Eigenschaft:** Eine CFullPropSpec-Struktur, wie in Abschnitt 2.2.1.2 angegeben, die die Eigenschaft angibt, für die ein Übereinstimmungsvorgang durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1317">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="c3671-1318">**\_ prval:** Eine CBaseStorageVariant-Struktur, wie in Abschnitt 2.2.1.1 angegeben, die den Wert enthält, der mit der Eigenschaft in Beziehung stehen soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1318">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="c3671-1319">2.2.1.10 CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-1319">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="c3671-1320">Die CRangeRestriction-Struktur enthält eine Einschränkung für einen Bereich von Werten.</span><span class="sxs-lookup"><span data-stu-id="c3671-1320">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="c3671-1321">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1321">0</span></span>

<span data-ttu-id="c3671-1322">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1322">1</span></span>

<span data-ttu-id="c3671-1323">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1323">2</span></span>

<span data-ttu-id="c3671-1324">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1324">3</span></span>

<span data-ttu-id="c3671-1325">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1325">4</span></span>

<span data-ttu-id="c3671-1326">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1326">5</span></span>

<span data-ttu-id="c3671-1327">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1327">6</span></span>

<span data-ttu-id="c3671-1328">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1328">7</span></span>

<span data-ttu-id="c3671-1329">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1329">8</span></span>

<span data-ttu-id="c3671-1330">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1330">9</span></span>

<span data-ttu-id="c3671-1331">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1331">1</span></span><br/> <span data-ttu-id="c3671-1332">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1332">0</span></span><br/>

<span data-ttu-id="c3671-1333">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1333">1</span></span>

<span data-ttu-id="c3671-1334">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1334">2</span></span>

<span data-ttu-id="c3671-1335">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1335">3</span></span>

<span data-ttu-id="c3671-1336">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1336">4</span></span>

<span data-ttu-id="c3671-1337">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1337">5</span></span>

<span data-ttu-id="c3671-1338">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1338">6</span></span>

<span data-ttu-id="c3671-1339">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1339">7</span></span>

<span data-ttu-id="c3671-1340">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1340">8</span></span>

<span data-ttu-id="c3671-1341">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1341">9</span></span>

<span data-ttu-id="c3671-1342">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1342">2</span></span><br/> <span data-ttu-id="c3671-1343">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1343">0</span></span><br/>

<span data-ttu-id="c3671-1344">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1344">1</span></span>

<span data-ttu-id="c3671-1345">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1345">2</span></span>

<span data-ttu-id="c3671-1346">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1346">3</span></span>

<span data-ttu-id="c3671-1347">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1347">4</span></span>

<span data-ttu-id="c3671-1348">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1348">5</span></span>

<span data-ttu-id="c3671-1349">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1349">6</span></span>

<span data-ttu-id="c3671-1350">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1350">7</span></span>

<span data-ttu-id="c3671-1351">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1351">8</span></span>

<span data-ttu-id="c3671-1352">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1352">9</span></span>

<span data-ttu-id="c3671-1353">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1353">3</span></span><br/> <span data-ttu-id="c3671-1354">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1354">0</span></span><br/>

<span data-ttu-id="c3671-1355">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1355">1</span></span>

<span data-ttu-id="c3671-1356">\_keyStart (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1356">\_keyStart (variable)</span></span>

<span data-ttu-id="c3671-1357">\_keyEnd (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1357">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="c3671-1358">**\_ keyStart:** Eine CKey-Struktur, wie in Abschnitt 2.2.1.4 angegeben, die den Anfang des Bereichs enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-1358">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="c3671-1359">**\_ keyEnd:** Eine CKey-Struktur, die das Ende des Bereichs enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-1359">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="c3671-1360">2.2.1.11 CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-1360">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="c3671-1361">Die CScopeRestriction-Struktur enthält eine Einschränkung für die zu durchsuchenden Dateien.</span><span class="sxs-lookup"><span data-stu-id="c3671-1361">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="c3671-1362">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1362">0</span></span>

<span data-ttu-id="c3671-1363">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1363">1</span></span>

<span data-ttu-id="c3671-1364">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1364">2</span></span>

<span data-ttu-id="c3671-1365">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1365">3</span></span>

<span data-ttu-id="c3671-1366">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1366">4</span></span>

<span data-ttu-id="c3671-1367">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1367">5</span></span>

<span data-ttu-id="c3671-1368">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1368">6</span></span>

<span data-ttu-id="c3671-1369">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1369">7</span></span>

<span data-ttu-id="c3671-1370">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1370">8</span></span>

<span data-ttu-id="c3671-1371">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1371">9</span></span>

<span data-ttu-id="c3671-1372">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1372">1</span></span><br/> <span data-ttu-id="c3671-1373">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1373">0</span></span><br/>

<span data-ttu-id="c3671-1374">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1374">1</span></span>

<span data-ttu-id="c3671-1375">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1375">2</span></span>

<span data-ttu-id="c3671-1376">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1376">3</span></span>

<span data-ttu-id="c3671-1377">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1377">4</span></span>

<span data-ttu-id="c3671-1378">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1378">5</span></span>

<span data-ttu-id="c3671-1379">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1379">6</span></span>

<span data-ttu-id="c3671-1380">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1380">7</span></span>

<span data-ttu-id="c3671-1381">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1381">8</span></span>

<span data-ttu-id="c3671-1382">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1382">9</span></span>

<span data-ttu-id="c3671-1383">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1383">2</span></span><br/> <span data-ttu-id="c3671-1384">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1384">0</span></span><br/>

<span data-ttu-id="c3671-1385">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1385">1</span></span>

<span data-ttu-id="c3671-1386">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1386">2</span></span>

<span data-ttu-id="c3671-1387">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1387">3</span></span>

<span data-ttu-id="c3671-1388">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1388">4</span></span>

<span data-ttu-id="c3671-1389">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1389">5</span></span>

<span data-ttu-id="c3671-1390">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1390">6</span></span>

<span data-ttu-id="c3671-1391">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1391">7</span></span>

<span data-ttu-id="c3671-1392">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1392">8</span></span>

<span data-ttu-id="c3671-1393">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1393">9</span></span>

<span data-ttu-id="c3671-1394">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1394">3</span></span><br/> <span data-ttu-id="c3671-1395">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1395">0</span></span><br/>

<span data-ttu-id="c3671-1396">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1396">1</span></span>

<span data-ttu-id="c3671-1397">CcLowerPath</span><span class="sxs-lookup"><span data-stu-id="c3671-1397">CcLowerPath</span></span>

<span data-ttu-id="c3671-1398">\_lowerPath (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1398">\_lowerPath (variable)</span></span>

<span data-ttu-id="c3671-1399">...</span><span class="sxs-lookup"><span data-stu-id="c3671-1399">...</span></span>

<span data-ttu-id="c3671-1400">\_Padding (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1400">\_padding ( variable)</span></span>

<span data-ttu-id="c3671-1401">\_Länge</span><span class="sxs-lookup"><span data-stu-id="c3671-1401">\_length</span></span>

<span data-ttu-id="c3671-1402">\_fRecursive</span><span class="sxs-lookup"><span data-stu-id="c3671-1402">\_fRecursive</span></span>

<span data-ttu-id="c3671-1403">\_fVirtuelle</span><span class="sxs-lookup"><span data-stu-id="c3671-1403">\_fVirtual</span></span>



 

<span data-ttu-id="c3671-1404">**CcLowerPath:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von Unicode-Zeichen im \_ feld lowerPath enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-1404">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="c3671-1405">**\_ lowerPath:** Eine unicode-Zeichenfolge ohne  NULL-Terminierung, die den Pfad darstellt, auf den die Abfrage eingeschränkt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1405">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="c3671-1406">Das Feld CcLowerPath enthält die Länge der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c3671-1406">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="c3671-1407">**\_ Padding**: Dieses Feld MUSS 0 bis 3 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1407">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="c3671-1408">Die Länge dieses Felds MUSS so lang sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Byte ab dem Anfang der Nachricht ist, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-1408">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="c3671-1409">Wenn dieses Feld vorhanden ist (d. h. länge ungleich null), ist der enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1409">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="c3671-1410">Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1410">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3671-1411">**\_ length:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge \_ von lowerPath in Unicode-Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-1411">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="c3671-1412">Dies MUSS der gleiche Wert wie CcLowerPath sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1412">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="c3671-1413">**\_ fRecursive:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1413">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3671-1414">MUSS auf 0x00000001 oder 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3671-1414">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="c3671-1415">Wenn auf 0x00000001 festgelegt ist, überprüft der Server rekursiv alle Unterverzeichnisse des Pfads.</span><span class="sxs-lookup"><span data-stu-id="c3671-1415">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="c3671-1416">Wenn auf 0x00000000 festgelegt ist, überprüft der Server keine Unterverzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="c3671-1416">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="c3671-1417">**\_ fVirtual:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1417">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3671-1418">MUSS auf 0x00000001 oder 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3671-1418">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="c3671-1419">Wenn diese 0x00000001, ist lowerPath ein virtueller Pfad (der Uniform Resource Locator (URL), der einem physischen Verzeichnis im Dateisystem \_ zugeordnet ist) für eine Website.</span><span class="sxs-lookup"><span data-stu-id="c3671-1419">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="c3671-1420">Wenn diese 0x00000000, \_ ist lowerPath ein Dateisystempfad.</span><span class="sxs-lookup"><span data-stu-id="c3671-1420">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="c3671-1421">2.2.1.12 CSort</span><span class="sxs-lookup"><span data-stu-id="c3671-1421">2.2.1.12 CSort</span></span>

<span data-ttu-id="c3671-1422">Die CSort-Struktur identifiziert eine zu sortierende Spalte.</span><span class="sxs-lookup"><span data-stu-id="c3671-1422">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="c3671-1423">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1423">0</span></span>

<span data-ttu-id="c3671-1424">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1424">1</span></span>

<span data-ttu-id="c3671-1425">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1425">2</span></span>

<span data-ttu-id="c3671-1426">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1426">3</span></span>

<span data-ttu-id="c3671-1427">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1427">4</span></span>

<span data-ttu-id="c3671-1428">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1428">5</span></span>

<span data-ttu-id="c3671-1429">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1429">6</span></span>

<span data-ttu-id="c3671-1430">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1430">7</span></span>

<span data-ttu-id="c3671-1431">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1431">8</span></span>

<span data-ttu-id="c3671-1432">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1432">9</span></span>

<span data-ttu-id="c3671-1433">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1433">1</span></span><br/> <span data-ttu-id="c3671-1434">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1434">0</span></span><br/>

<span data-ttu-id="c3671-1435">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1435">1</span></span>

<span data-ttu-id="c3671-1436">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1436">2</span></span>

<span data-ttu-id="c3671-1437">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1437">3</span></span>

<span data-ttu-id="c3671-1438">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1438">4</span></span>

<span data-ttu-id="c3671-1439">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1439">5</span></span>

<span data-ttu-id="c3671-1440">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1440">6</span></span>

<span data-ttu-id="c3671-1441">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1441">7</span></span>

<span data-ttu-id="c3671-1442">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1442">8</span></span>

<span data-ttu-id="c3671-1443">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1443">9</span></span>

<span data-ttu-id="c3671-1444">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1444">2</span></span><br/> <span data-ttu-id="c3671-1445">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1445">0</span></span><br/>

<span data-ttu-id="c3671-1446">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1446">1</span></span>

<span data-ttu-id="c3671-1447">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1447">2</span></span>

<span data-ttu-id="c3671-1448">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1448">3</span></span>

<span data-ttu-id="c3671-1449">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1449">4</span></span>

<span data-ttu-id="c3671-1450">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1450">5</span></span>

<span data-ttu-id="c3671-1451">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1451">6</span></span>

<span data-ttu-id="c3671-1452">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1452">7</span></span>

<span data-ttu-id="c3671-1453">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1453">8</span></span>

<span data-ttu-id="c3671-1454">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1454">9</span></span>

<span data-ttu-id="c3671-1455">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1455">3</span></span><br/> <span data-ttu-id="c3671-1456">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1456">0</span></span><br/>

<span data-ttu-id="c3671-1457">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1457">1</span></span>

<span data-ttu-id="c3671-1458">pidColumn</span><span class="sxs-lookup"><span data-stu-id="c3671-1458">pidColumn</span></span>

<span data-ttu-id="c3671-1459">dwOrder</span><span class="sxs-lookup"><span data-stu-id="c3671-1459">dwOrder</span></span>

<span data-ttu-id="c3671-1460">locale</span><span class="sxs-lookup"><span data-stu-id="c3671-1460">locale</span></span>



 

<span data-ttu-id="c3671-1461">**pidColumn:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1461">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3671-1462">Die Nummer der Spalte, nach der sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1462">The number of the column to sort by.</span></span>

<span data-ttu-id="c3671-1463">**dwOrder:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1463">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3671-1464">MUSS einer der folgenden Werte sein und angeben, wie basierend auf der Spalte sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1464">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="c3671-1465">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-1465">Value</span></span>                        | <span data-ttu-id="c3671-1466">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-1466">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-1467">\_SORTASCEND-ABFRAGE 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-1467">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="c3671-1468">Die Zeilen müssen basierend auf den Werten in der angegebenen Spalte in aufsteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1468">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="c3671-1469">QUERY \_ DESCEND 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-1469">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="c3671-1470">Die Zeilen müssen basierend auf den Werten in der angegebenen Spalte in absteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1470">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="c3671-1471">**locale:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Im MS-GPSI Anhang A angegebene Locale \[ \] der Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1471">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="c3671-1472">2.2.1.13 CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-1472">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="c3671-1473">Die CSynRestriction-Struktur enthält ein Wort oder seine Synonyme für einen Abfrageaussatz.</span><span class="sxs-lookup"><span data-stu-id="c3671-1473">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="c3671-1474">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1474">0</span></span>

<span data-ttu-id="c3671-1475">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1475">1</span></span>

<span data-ttu-id="c3671-1476">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1476">2</span></span>

<span data-ttu-id="c3671-1477">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1477">3</span></span>

<span data-ttu-id="c3671-1478">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1478">4</span></span>

<span data-ttu-id="c3671-1479">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1479">5</span></span>

<span data-ttu-id="c3671-1480">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1480">6</span></span>

<span data-ttu-id="c3671-1481">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1481">7</span></span>

<span data-ttu-id="c3671-1482">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1482">8</span></span>

<span data-ttu-id="c3671-1483">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1483">9</span></span>

<span data-ttu-id="c3671-1484">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1484">1</span></span><br/> <span data-ttu-id="c3671-1485">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1485">0</span></span><br/>

<span data-ttu-id="c3671-1486">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1486">1</span></span>

<span data-ttu-id="c3671-1487">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1487">2</span></span>

<span data-ttu-id="c3671-1488">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1488">3</span></span>

<span data-ttu-id="c3671-1489">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1489">4</span></span>

<span data-ttu-id="c3671-1490">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1490">5</span></span>

<span data-ttu-id="c3671-1491">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1491">6</span></span>

<span data-ttu-id="c3671-1492">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1492">7</span></span>

<span data-ttu-id="c3671-1493">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1493">8</span></span>

<span data-ttu-id="c3671-1494">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1494">9</span></span>

<span data-ttu-id="c3671-1495">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1495">2</span></span><br/> <span data-ttu-id="c3671-1496">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1496">0</span></span><br/>

<span data-ttu-id="c3671-1497">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1497">1</span></span>

<span data-ttu-id="c3671-1498">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1498">2</span></span>

<span data-ttu-id="c3671-1499">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1499">3</span></span>

<span data-ttu-id="c3671-1500">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1500">4</span></span>

<span data-ttu-id="c3671-1501">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1501">5</span></span>

<span data-ttu-id="c3671-1502">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1502">6</span></span>

<span data-ttu-id="c3671-1503">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1503">7</span></span>

<span data-ttu-id="c3671-1504">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1504">8</span></span>

<span data-ttu-id="c3671-1505">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1505">9</span></span>

<span data-ttu-id="c3671-1506">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1506">3</span></span><br/> <span data-ttu-id="c3671-1507">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1507">0</span></span><br/>

<span data-ttu-id="c3671-1508">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1508">1</span></span>

<span data-ttu-id="c3671-1509">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="c3671-1509">Restriction</span></span>

<span data-ttu-id="c3671-1510">...</span><span class="sxs-lookup"><span data-stu-id="c3671-1510">...</span></span>

<span data-ttu-id="c3671-1511">...</span><span class="sxs-lookup"><span data-stu-id="c3671-1511">...</span></span>

<span data-ttu-id="c3671-1512">cKey</span><span class="sxs-lookup"><span data-stu-id="c3671-1512">cKey</span></span>

<span data-ttu-id="c3671-1513">\_keyArray (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1513">\_keyArray (variable)</span></span>

<span data-ttu-id="c3671-1514">\_isRange</span><span class="sxs-lookup"><span data-stu-id="c3671-1514">\_isRange</span></span>



 

<span data-ttu-id="c3671-1515">**Einschränkung:** Eine COccRestriction-Struktur, die die Position des Worts an gibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1515">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="c3671-1516">**cKey:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im \_ keyArray-Array angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1516">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="c3671-1517">**\_ keyArray:** Ein Array von CKey-Strukturen, die ein Wort und seine Synonyme angeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-1517">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="c3671-1518">**\_ isRange:** Wenn auf 0x01 festgelegt ist, sind die Schlüssel Präfixe, die übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1518">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="c3671-1519">Wenn diese 0x00 festgelegt ist, sind die Schlüssel exakte Werte, die übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1519">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="c3671-1520">\_isRange DARF NICHT auf andere Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1520">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="c3671-1521">2.2.1.14 CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-1521">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="c3671-1522">Die CVectorRestriction-Struktur enthält einen gewichteten OR-Vorgang auf einem Befehlsstrukturknoten.</span><span class="sxs-lookup"><span data-stu-id="c3671-1522">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="c3671-1523">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1523">0</span></span>

<span data-ttu-id="c3671-1524">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1524">1</span></span>

<span data-ttu-id="c3671-1525">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1525">2</span></span>

<span data-ttu-id="c3671-1526">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1526">3</span></span>

<span data-ttu-id="c3671-1527">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1527">4</span></span>

<span data-ttu-id="c3671-1528">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1528">5</span></span>

<span data-ttu-id="c3671-1529">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1529">6</span></span>

<span data-ttu-id="c3671-1530">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1530">7</span></span>

<span data-ttu-id="c3671-1531">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1531">8</span></span>

<span data-ttu-id="c3671-1532">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1532">9</span></span>

<span data-ttu-id="c3671-1533">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1533">1</span></span><br/> <span data-ttu-id="c3671-1534">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1534">0</span></span><br/>

<span data-ttu-id="c3671-1535">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1535">1</span></span>

<span data-ttu-id="c3671-1536">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1536">2</span></span>

<span data-ttu-id="c3671-1537">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1537">3</span></span>

<span data-ttu-id="c3671-1538">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1538">4</span></span>

<span data-ttu-id="c3671-1539">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1539">5</span></span>

<span data-ttu-id="c3671-1540">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1540">6</span></span>

<span data-ttu-id="c3671-1541">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1541">7</span></span>

<span data-ttu-id="c3671-1542">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1542">8</span></span>

<span data-ttu-id="c3671-1543">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1543">9</span></span>

<span data-ttu-id="c3671-1544">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1544">2</span></span><br/> <span data-ttu-id="c3671-1545">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1545">0</span></span><br/>

<span data-ttu-id="c3671-1546">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1546">1</span></span>

<span data-ttu-id="c3671-1547">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1547">2</span></span>

<span data-ttu-id="c3671-1548">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1548">3</span></span>

<span data-ttu-id="c3671-1549">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1549">4</span></span>

<span data-ttu-id="c3671-1550">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1550">5</span></span>

<span data-ttu-id="c3671-1551">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1551">6</span></span>

<span data-ttu-id="c3671-1552">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1552">7</span></span>

<span data-ttu-id="c3671-1553">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1553">8</span></span>

<span data-ttu-id="c3671-1554">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1554">9</span></span>

<span data-ttu-id="c3671-1555">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1555">3</span></span><br/> <span data-ttu-id="c3671-1556">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1556">0</span></span><br/>

<span data-ttu-id="c3671-1557">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1557">1</span></span>

<span data-ttu-id="c3671-1558">\_pres (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1558">\_pres (variable)</span></span>

<span data-ttu-id="c3671-1559">...</span><span class="sxs-lookup"><span data-stu-id="c3671-1559">...</span></span>

<span data-ttu-id="c3671-1560">\_Auf padding (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1560">\_padding (variable)</span></span>

<span data-ttu-id="c3671-1561">\_ulRankMethod</span><span class="sxs-lookup"><span data-stu-id="c3671-1561">\_ulRankMethod</span></span>



 

<span data-ttu-id="c3671-1562">**\_ pres:** Eine CNodeRestriction-Befehlsstruktur, für die ein or-Vorgang mit Rang angegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1562">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="c3671-1563">**\_ Padding**: Dieses Feld MUSS 0 bis 3 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1563">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="c3671-1564">Die Länge dieses Felds MUSS so lang sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Byte ab dem Anfang der Nachricht ist, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-1564">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="c3671-1565">Wenn dieses Feld vorhanden ist (d. h. länge ungleich null), ist der enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="c3671-1565">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="c3671-1566">Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1566">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3671-1567">**\_ ulRankMethod:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die einen Rangfolgealgorithmus angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1567">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="c3671-1568">MUSS auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1568">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="c3671-1569">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-1569">Value</span></span>                            | <span data-ttu-id="c3671-1570">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-1570">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="c3671-1571">VECTOR \_ RANK \_ MIN 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-1571">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="c3671-1572">Verwenden Sie den minimalen \[ SALTON-Algorithmus. \]</span><span class="sxs-lookup"><span data-stu-id="c3671-1572">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="c3671-1573">VECTOR \_ RANK \_ MAX 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-1573">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="c3671-1574">Verwenden Sie den maximalen \[ SALTON-Algorithmus. \]</span><span class="sxs-lookup"><span data-stu-id="c3671-1574">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="c3671-1575">VECTOR \_ RANK \_ INNER 0X00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-1575">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="c3671-1576">Verwenden Sie den inneren Produktalgorithmus \[ SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="c3671-1576">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="c3671-1577">VECTOR \_ RANK \_ DICE-0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-1577">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="c3671-1578">Verwenden Sie den Dice-Koeffizientenalgorithmus \[ SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="c3671-1578">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="c3671-1579">VECTOR \_ RANK \_ JACCARD-0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3671-1579">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="c3671-1580">Verwenden Sie den Jaccard-Koeffizientenalgorithmus \[ SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="c3671-1580">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="c3671-1581">2.2.1.15 CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-1581">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="c3671-1582">Die CWordRestriction-Struktur enthält ein Wort für einen Abfrageaussatz.</span><span class="sxs-lookup"><span data-stu-id="c3671-1582">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="c3671-1583">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1583">0</span></span>

<span data-ttu-id="c3671-1584">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1584">1</span></span>

<span data-ttu-id="c3671-1585">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1585">2</span></span>

<span data-ttu-id="c3671-1586">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1586">3</span></span>

<span data-ttu-id="c3671-1587">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1587">4</span></span>

<span data-ttu-id="c3671-1588">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1588">5</span></span>

<span data-ttu-id="c3671-1589">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1589">6</span></span>

<span data-ttu-id="c3671-1590">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1590">7</span></span>

<span data-ttu-id="c3671-1591">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1591">8</span></span>

<span data-ttu-id="c3671-1592">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1592">9</span></span>

<span data-ttu-id="c3671-1593">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1593">1</span></span><br/> <span data-ttu-id="c3671-1594">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1594">0</span></span><br/>

<span data-ttu-id="c3671-1595">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1595">1</span></span>

<span data-ttu-id="c3671-1596">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1596">2</span></span>

<span data-ttu-id="c3671-1597">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1597">3</span></span>

<span data-ttu-id="c3671-1598">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1598">4</span></span>

<span data-ttu-id="c3671-1599">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1599">5</span></span>

<span data-ttu-id="c3671-1600">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1600">6</span></span>

<span data-ttu-id="c3671-1601">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1601">7</span></span>

<span data-ttu-id="c3671-1602">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1602">8</span></span>

<span data-ttu-id="c3671-1603">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1603">9</span></span>

<span data-ttu-id="c3671-1604">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1604">2</span></span><br/> <span data-ttu-id="c3671-1605">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1605">0</span></span><br/>

<span data-ttu-id="c3671-1606">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1606">1</span></span>

<span data-ttu-id="c3671-1607">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1607">2</span></span>

<span data-ttu-id="c3671-1608">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1608">3</span></span>

<span data-ttu-id="c3671-1609">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1609">4</span></span>

<span data-ttu-id="c3671-1610">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1610">5</span></span>

<span data-ttu-id="c3671-1611">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1611">6</span></span>

<span data-ttu-id="c3671-1612">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1612">7</span></span>

<span data-ttu-id="c3671-1613">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1613">8</span></span>

<span data-ttu-id="c3671-1614">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1614">9</span></span>

<span data-ttu-id="c3671-1615">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1615">3</span></span><br/> <span data-ttu-id="c3671-1616">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1616">0</span></span><br/>

<span data-ttu-id="c3671-1617">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1617">1</span></span>

<span data-ttu-id="c3671-1618">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="c3671-1618">restriction</span></span>

<span data-ttu-id="c3671-1619">...</span><span class="sxs-lookup"><span data-stu-id="c3671-1619">...</span></span>

<span data-ttu-id="c3671-1620">...</span><span class="sxs-lookup"><span data-stu-id="c3671-1620">...</span></span>

<span data-ttu-id="c3671-1621">\_key (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1621">\_key (variable)</span></span>

<span data-ttu-id="c3671-1622">\_isRange</span><span class="sxs-lookup"><span data-stu-id="c3671-1622">\_isRange</span></span>



 

<span data-ttu-id="c3671-1623">**restriction:** Eine COccRestriction-Struktur, die die Position des Worts an gibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1623">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="c3671-1624">**\_ key:** Eine CKey-Struktur, die ein Wort an gibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1624">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="c3671-1625">**\_ isRange:** Wenn auf 0x01 festgelegt ist, ist der Schlüssel ein Präfix, das übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1625">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="c3671-1626">Wenn der Wert auf 0x00 festgelegt ist, ist der Schlüssel ein exakter Wert, der übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1626">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="c3671-1627">\_isRange DARF NICHT auf einen anderen Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1627">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="c3671-1628">2.2.1.16 CRestriction</span><span class="sxs-lookup"><span data-stu-id="c3671-1628">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="c3671-1629">Die CRestriction-Struktur enthält einen Knoten einer Abfragebefehlsstruktur.</span><span class="sxs-lookup"><span data-stu-id="c3671-1629">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="c3671-1630">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1630">0</span></span>

<span data-ttu-id="c3671-1631">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1631">1</span></span>

<span data-ttu-id="c3671-1632">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1632">2</span></span>

<span data-ttu-id="c3671-1633">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1633">3</span></span>

<span data-ttu-id="c3671-1634">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1634">4</span></span>

<span data-ttu-id="c3671-1635">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1635">5</span></span>

<span data-ttu-id="c3671-1636">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1636">6</span></span>

<span data-ttu-id="c3671-1637">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1637">7</span></span>

<span data-ttu-id="c3671-1638">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1638">8</span></span>

<span data-ttu-id="c3671-1639">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1639">9</span></span>

<span data-ttu-id="c3671-1640">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1640">1</span></span><br/> <span data-ttu-id="c3671-1641">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1641">0</span></span><br/>

<span data-ttu-id="c3671-1642">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1642">1</span></span>

<span data-ttu-id="c3671-1643">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1643">2</span></span>

<span data-ttu-id="c3671-1644">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1644">3</span></span>

<span data-ttu-id="c3671-1645">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1645">4</span></span>

<span data-ttu-id="c3671-1646">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1646">5</span></span>

<span data-ttu-id="c3671-1647">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1647">6</span></span>

<span data-ttu-id="c3671-1648">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1648">7</span></span>

<span data-ttu-id="c3671-1649">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1649">8</span></span>

<span data-ttu-id="c3671-1650">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1650">9</span></span>

<span data-ttu-id="c3671-1651">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1651">2</span></span><br/> <span data-ttu-id="c3671-1652">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1652">0</span></span><br/>

<span data-ttu-id="c3671-1653">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1653">1</span></span>

<span data-ttu-id="c3671-1654">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1654">2</span></span>

<span data-ttu-id="c3671-1655">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1655">3</span></span>

<span data-ttu-id="c3671-1656">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1656">4</span></span>

<span data-ttu-id="c3671-1657">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1657">5</span></span>

<span data-ttu-id="c3671-1658">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1658">6</span></span>

<span data-ttu-id="c3671-1659">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1659">7</span></span>

<span data-ttu-id="c3671-1660">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1660">8</span></span>

<span data-ttu-id="c3671-1661">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1661">9</span></span>

<span data-ttu-id="c3671-1662">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1662">3</span></span><br/> <span data-ttu-id="c3671-1663">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1663">0</span></span><br/>

<span data-ttu-id="c3671-1664">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1664">1</span></span>

<span data-ttu-id="c3671-1665">\_ulType</span><span class="sxs-lookup"><span data-stu-id="c3671-1665">\_ulType</span></span>

<span data-ttu-id="c3671-1666">Weight</span><span class="sxs-lookup"><span data-stu-id="c3671-1666">Weight</span></span>

<span data-ttu-id="c3671-1667">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="c3671-1667">Restriction</span></span>



 

<span data-ttu-id="c3671-1668">**\_ ulType:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Einschränkungstyp angibt, der für den Befehlsstrukturknoten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-1668">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="c3671-1669">MUSS auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1669">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="c3671-1670">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-1670">Value</span></span>                    | <span data-ttu-id="c3671-1671">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-1671">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-1672">RTNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-1672">RTNone 0x00000000</span></span>        | <span data-ttu-id="c3671-1673">Der Knoten stellt ein Rauschwort in einer Vektorabfrage dar.</span><span class="sxs-lookup"><span data-stu-id="c3671-1673">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="c3671-1674">RTAnd 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-1674">RTAnd 0x00000001</span></span>         | <span data-ttu-id="c3671-1675">Der Knoten enthält eine CNodeRestriction, für die ein logischer AND-Vorgang ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1675">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="c3671-1676">RTOr-0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-1676">RTOr 0x00000002</span></span>          | <span data-ttu-id="c3671-1677">Der Knoten enthält eine CNodeRestriction, für die ein logischer OR-Vorgang ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1677">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="c3671-1678">RTNot 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-1678">RTNot 0x00000003</span></span>         | <span data-ttu-id="c3671-1679">Der Knoten enthält eine CRestriction, für die ein NOT-Vorgang ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1679">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="c3671-1680">RTContent 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3671-1680">RTContent 0x00000004</span></span>     | <span data-ttu-id="c3671-1681">Der Knoten enthält eine CContentRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3671-1681">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="c3671-1682">RTProperty-0x00000005</span><span class="sxs-lookup"><span data-stu-id="c3671-1682">RTProperty 0x00000005</span></span>    | <span data-ttu-id="c3671-1683">Der Knoten enthält eine CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3671-1683">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="c3671-1684">RTProximity 0x00000006</span><span class="sxs-lookup"><span data-stu-id="c3671-1684">RTProximity 0x00000006</span></span>   | <span data-ttu-id="c3671-1685">Der Knoten enthält eine CNodeRestriction, für die eine Näherungsrangfolge durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1685">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="c3671-1686">RTVector-0x00000007</span><span class="sxs-lookup"><span data-stu-id="c3671-1686">RTVector 0x00000007</span></span>      | <span data-ttu-id="c3671-1687">Der Knoten enthält eine CVectorRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3671-1687">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="c3671-1688">RTNatLanguage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3671-1688">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="c3671-1689">Der Knoten enthält eine CNatLanguageRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3671-1689">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="c3671-1690">RTScope 0x00000009</span><span class="sxs-lookup"><span data-stu-id="c3671-1690">RTScope 0x00000009</span></span>       | <span data-ttu-id="c3671-1691">Der Knoten enthält eine CScopeRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3671-1691">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="c3671-1692">PRAny-0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="c3671-1692">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="c3671-1693">Der Knoten enthält eine CInternalPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3671-1693">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="c3671-1694">RTRange 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="c3671-1694">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="c3671-1695">Der Knoten enthält eine CRangeRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3671-1695">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="c3671-1696">RTPhrase-0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="c3671-1696">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="c3671-1697">Der Knoten enthält eine CNodeRestriction, für die eine Ausdrucks match ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1697">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="c3671-1698">RTSynonym 0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="c3671-1698">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="c3671-1699">Der Knoten enthält eine CSynRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3671-1699">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="c3671-1700">RTWord-0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="c3671-1700">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="c3671-1701">Der Knoten enthält eine CWordRestriction.</span><span class="sxs-lookup"><span data-stu-id="c3671-1701">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="c3671-1702">**Gewichtung:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gewichtung des Knotens darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1702">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="c3671-1703">Die Gewichtung gibt die Wichtigkeit des Knotens relativ zu anderen Knoten in der Abfragebefehlsstruktur an.</span><span class="sxs-lookup"><span data-stu-id="c3671-1703">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="c3671-1704">Höhere Gewichtungswerte sind wichtiger.</span><span class="sxs-lookup"><span data-stu-id="c3671-1704">Higher weight values are more important.</span></span>

<span data-ttu-id="c3671-1705">**Einschränkung:** Der Einschränkungstyp für den Befehlsstrukturknoten.</span><span class="sxs-lookup"><span data-stu-id="c3671-1705">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="c3671-1706">Die Syntax MUSS wie durch das \_ ulType-Feld angegeben sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1706">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="c3671-1707">2.2.1.17 CColumnSet</span><span class="sxs-lookup"><span data-stu-id="c3671-1707">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="c3671-1708">Die CColumnSet-Struktur gibt die spaltennummern an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1708">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="c3671-1709">Diese Struktur wird immer als Verweis auf eine bestimmte CPidMapper-Struktur verwendet (Abschnitt 2.2.1.23).</span><span class="sxs-lookup"><span data-stu-id="c3671-1709">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="c3671-1710">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1710">0</span></span>

<span data-ttu-id="c3671-1711">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1711">1</span></span>

<span data-ttu-id="c3671-1712">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1712">2</span></span>

<span data-ttu-id="c3671-1713">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1713">3</span></span>

<span data-ttu-id="c3671-1714">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1714">4</span></span>

<span data-ttu-id="c3671-1715">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1715">5</span></span>

<span data-ttu-id="c3671-1716">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1716">6</span></span>

<span data-ttu-id="c3671-1717">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1717">7</span></span>

<span data-ttu-id="c3671-1718">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1718">8</span></span>

<span data-ttu-id="c3671-1719">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1719">9</span></span>

<span data-ttu-id="c3671-1720">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1720">1</span></span><br/> <span data-ttu-id="c3671-1721">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1721">0</span></span><br/>

<span data-ttu-id="c3671-1722">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1722">1</span></span>

<span data-ttu-id="c3671-1723">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1723">2</span></span>

<span data-ttu-id="c3671-1724">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1724">3</span></span>

<span data-ttu-id="c3671-1725">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1725">4</span></span>

<span data-ttu-id="c3671-1726">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1726">5</span></span>

<span data-ttu-id="c3671-1727">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1727">6</span></span>

<span data-ttu-id="c3671-1728">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1728">7</span></span>

<span data-ttu-id="c3671-1729">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1729">8</span></span>

<span data-ttu-id="c3671-1730">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1730">9</span></span>

<span data-ttu-id="c3671-1731">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1731">2</span></span><br/> <span data-ttu-id="c3671-1732">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1732">0</span></span><br/>

<span data-ttu-id="c3671-1733">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1733">1</span></span>

<span data-ttu-id="c3671-1734">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1734">2</span></span>

<span data-ttu-id="c3671-1735">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1735">3</span></span>

<span data-ttu-id="c3671-1736">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1736">4</span></span>

<span data-ttu-id="c3671-1737">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1737">5</span></span>

<span data-ttu-id="c3671-1738">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1738">6</span></span>

<span data-ttu-id="c3671-1739">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1739">7</span></span>

<span data-ttu-id="c3671-1740">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1740">8</span></span>

<span data-ttu-id="c3671-1741">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1741">9</span></span>

<span data-ttu-id="c3671-1742">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1742">3</span></span><br/> <span data-ttu-id="c3671-1743">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1743">0</span></span><br/>

<span data-ttu-id="c3671-1744">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1744">1</span></span>

<span data-ttu-id="c3671-1745">count</span><span class="sxs-lookup"><span data-stu-id="c3671-1745">count</span></span>

<span data-ttu-id="c3671-1746">Indizes (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1746">indexes (variable)</span></span>



 

<span data-ttu-id="c3671-1747">**count:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im Indexarray angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1747">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="c3671-1748">**indexes:** Array von 4-Byte-Ganzzahlen ohne Vorzeichen, die nullbasierte Indizes im aPropSpec-Array in der entsprechenden CPidMapper-Struktur darstellen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1748">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="c3671-1749">2.2.1.18 CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="c3671-1749">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="c3671-1750">Die CCategorizationSet-Struktur enthält Informationen über die Gruppierung eines Abfrageergebnissets.</span><span class="sxs-lookup"><span data-stu-id="c3671-1750">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="c3671-1751">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1751">0</span></span>

<span data-ttu-id="c3671-1752">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1752">1</span></span>

<span data-ttu-id="c3671-1753">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1753">2</span></span>

<span data-ttu-id="c3671-1754">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1754">3</span></span>

<span data-ttu-id="c3671-1755">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1755">4</span></span>

<span data-ttu-id="c3671-1756">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1756">5</span></span>

<span data-ttu-id="c3671-1757">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1757">6</span></span>

<span data-ttu-id="c3671-1758">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1758">7</span></span>

<span data-ttu-id="c3671-1759">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1759">8</span></span>

<span data-ttu-id="c3671-1760">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1760">9</span></span>

<span data-ttu-id="c3671-1761">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1761">1</span></span><br/> <span data-ttu-id="c3671-1762">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1762">0</span></span><br/>

<span data-ttu-id="c3671-1763">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1763">1</span></span>

<span data-ttu-id="c3671-1764">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1764">2</span></span>

<span data-ttu-id="c3671-1765">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1765">3</span></span>

<span data-ttu-id="c3671-1766">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1766">4</span></span>

<span data-ttu-id="c3671-1767">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1767">5</span></span>

<span data-ttu-id="c3671-1768">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1768">6</span></span>

<span data-ttu-id="c3671-1769">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1769">7</span></span>

<span data-ttu-id="c3671-1770">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1770">8</span></span>

<span data-ttu-id="c3671-1771">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1771">9</span></span>

<span data-ttu-id="c3671-1772">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1772">2</span></span><br/> <span data-ttu-id="c3671-1773">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1773">0</span></span><br/>

<span data-ttu-id="c3671-1774">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1774">1</span></span>

<span data-ttu-id="c3671-1775">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1775">2</span></span>

<span data-ttu-id="c3671-1776">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1776">3</span></span>

<span data-ttu-id="c3671-1777">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1777">4</span></span>

<span data-ttu-id="c3671-1778">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1778">5</span></span>

<span data-ttu-id="c3671-1779">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1779">6</span></span>

<span data-ttu-id="c3671-1780">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1780">7</span></span>

<span data-ttu-id="c3671-1781">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1781">8</span></span>

<span data-ttu-id="c3671-1782">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1782">9</span></span>

<span data-ttu-id="c3671-1783">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1783">3</span></span><br/> <span data-ttu-id="c3671-1784">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1784">0</span></span><br/>

<span data-ttu-id="c3671-1785">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1785">1</span></span>

<span data-ttu-id="c3671-1786">count</span><span class="sxs-lookup"><span data-stu-id="c3671-1786">count</span></span>

<span data-ttu-id="c3671-1787">categories (variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1787">categories (variable)</span></span>



 

<span data-ttu-id="c3671-1788">**count:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im Categories-Array enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-1788">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="c3671-1789">**categories:** Array von CCategorizationSpec-Strukturen, die die Gruppierung der Abfrage angeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-1789">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="c3671-1790">2.2.1.19 CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="c3671-1790">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="c3671-1791">Die CCategorizationSpec-Struktur enthält eine Gruppierung für ein Abfrageergebnissatz.</span><span class="sxs-lookup"><span data-stu-id="c3671-1791">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="c3671-1792">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1792">0</span></span>

<span data-ttu-id="c3671-1793">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1793">1</span></span>

<span data-ttu-id="c3671-1794">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1794">2</span></span>

<span data-ttu-id="c3671-1795">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1795">3</span></span>

<span data-ttu-id="c3671-1796">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1796">4</span></span>

<span data-ttu-id="c3671-1797">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1797">5</span></span>

<span data-ttu-id="c3671-1798">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1798">6</span></span>

<span data-ttu-id="c3671-1799">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1799">7</span></span>

<span data-ttu-id="c3671-1800">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1800">8</span></span>

<span data-ttu-id="c3671-1801">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1801">9</span></span>

<span data-ttu-id="c3671-1802">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1802">1</span></span><br/> <span data-ttu-id="c3671-1803">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1803">0</span></span><br/>

<span data-ttu-id="c3671-1804">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1804">1</span></span>

<span data-ttu-id="c3671-1805">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1805">2</span></span>

<span data-ttu-id="c3671-1806">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1806">3</span></span>

<span data-ttu-id="c3671-1807">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1807">4</span></span>

<span data-ttu-id="c3671-1808">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1808">5</span></span>

<span data-ttu-id="c3671-1809">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1809">6</span></span>

<span data-ttu-id="c3671-1810">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1810">7</span></span>

<span data-ttu-id="c3671-1811">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1811">8</span></span>

<span data-ttu-id="c3671-1812">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1812">9</span></span>

<span data-ttu-id="c3671-1813">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1813">2</span></span><br/> <span data-ttu-id="c3671-1814">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1814">0</span></span><br/>

<span data-ttu-id="c3671-1815">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1815">1</span></span>

<span data-ttu-id="c3671-1816">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1816">2</span></span>

<span data-ttu-id="c3671-1817">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1817">3</span></span>

<span data-ttu-id="c3671-1818">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1818">4</span></span>

<span data-ttu-id="c3671-1819">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1819">5</span></span>

<span data-ttu-id="c3671-1820">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1820">6</span></span>

<span data-ttu-id="c3671-1821">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1821">7</span></span>

<span data-ttu-id="c3671-1822">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1822">8</span></span>

<span data-ttu-id="c3671-1823">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1823">9</span></span>

<span data-ttu-id="c3671-1824">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1824">3</span></span><br/> <span data-ttu-id="c3671-1825">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1825">0</span></span><br/>

<span data-ttu-id="c3671-1826">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1826">1</span></span>

<span data-ttu-id="c3671-1827">\_csColumns (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1827">\_csColumns (variable)</span></span>

<span data-ttu-id="c3671-1828">\_ulCategType</span><span class="sxs-lookup"><span data-stu-id="c3671-1828">\_ulCategType</span></span>



 

<span data-ttu-id="c3671-1829">**\_ csColumns:** Eine CColumnSet-Struktur, die die Spalten angibt, nach denen die Abfrage gruppiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1829">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="c3671-1830">**\_ ulCategType:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1830">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3671-1831">MUSS auf "0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3671-1831">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="c3671-1832">2.2.1.20 CDbColId</span><span class="sxs-lookup"><span data-stu-id="c3671-1832">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="c3671-1833">Die CDbColId-Struktur enthält eine Spalte.</span><span class="sxs-lookup"><span data-stu-id="c3671-1833">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="c3671-1834">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1834">0</span></span>

<span data-ttu-id="c3671-1835">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1835">1</span></span>

<span data-ttu-id="c3671-1836">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1836">2</span></span>

<span data-ttu-id="c3671-1837">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1837">3</span></span>

<span data-ttu-id="c3671-1838">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1838">4</span></span>

<span data-ttu-id="c3671-1839">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1839">5</span></span>

<span data-ttu-id="c3671-1840">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1840">6</span></span>

<span data-ttu-id="c3671-1841">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1841">7</span></span>

<span data-ttu-id="c3671-1842">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1842">8</span></span>

<span data-ttu-id="c3671-1843">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1843">9</span></span>

<span data-ttu-id="c3671-1844">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1844">1</span></span><br/> <span data-ttu-id="c3671-1845">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1845">0</span></span><br/>

<span data-ttu-id="c3671-1846">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1846">1</span></span>

<span data-ttu-id="c3671-1847">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1847">2</span></span>

<span data-ttu-id="c3671-1848">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1848">3</span></span>

<span data-ttu-id="c3671-1849">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1849">4</span></span>

<span data-ttu-id="c3671-1850">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1850">5</span></span>

<span data-ttu-id="c3671-1851">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1851">6</span></span>

<span data-ttu-id="c3671-1852">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1852">7</span></span>

<span data-ttu-id="c3671-1853">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1853">8</span></span>

<span data-ttu-id="c3671-1854">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1854">9</span></span>

<span data-ttu-id="c3671-1855">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1855">2</span></span><br/> <span data-ttu-id="c3671-1856">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1856">0</span></span><br/>

<span data-ttu-id="c3671-1857">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1857">1</span></span>

<span data-ttu-id="c3671-1858">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1858">2</span></span>

<span data-ttu-id="c3671-1859">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1859">3</span></span>

<span data-ttu-id="c3671-1860">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1860">4</span></span>

<span data-ttu-id="c3671-1861">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1861">5</span></span>

<span data-ttu-id="c3671-1862">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1862">6</span></span>

<span data-ttu-id="c3671-1863">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1863">7</span></span>

<span data-ttu-id="c3671-1864">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1864">8</span></span>

<span data-ttu-id="c3671-1865">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1865">9</span></span>

<span data-ttu-id="c3671-1866">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1866">3</span></span><br/> <span data-ttu-id="c3671-1867">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1867">0</span></span><br/>

<span data-ttu-id="c3671-1868">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1868">1</span></span>

<span data-ttu-id="c3671-1869">eKind</span><span class="sxs-lookup"><span data-stu-id="c3671-1869">eKind</span></span>

<span data-ttu-id="c3671-1870">GUID</span><span class="sxs-lookup"><span data-stu-id="c3671-1870">GUID</span></span>

<span data-ttu-id="c3671-1871">...</span><span class="sxs-lookup"><span data-stu-id="c3671-1871">...</span></span>

<span data-ttu-id="c3671-1872">...</span><span class="sxs-lookup"><span data-stu-id="c3671-1872">...</span></span>

<span data-ttu-id="c3671-1873">...</span><span class="sxs-lookup"><span data-stu-id="c3671-1873">...</span></span>

<span data-ttu-id="c3671-1874">ulId</span><span class="sxs-lookup"><span data-stu-id="c3671-1874">ulId</span></span>

<span data-ttu-id="c3671-1875">vString (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1875">vString (variable)</span></span>



 

<span data-ttu-id="c3671-1876">**eKind:** MUSS auf einen der folgenden Werte festgelegt werden, der den Inhalt von GUID und vValue angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1876">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="c3671-1877">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-1877">Value</span></span>                            | <span data-ttu-id="c3671-1878">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-1878">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-1879">NAME DER \_ \_ DBKIND-GUID 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-1879">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="c3671-1880">vString enthält einen Eigenschaftennamen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1880">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="c3671-1881">\_PROPID-0x00000001 \_</span><span class="sxs-lookup"><span data-stu-id="c3671-1881">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="c3671-1882">ulId enthält eine 4-Byte-Ganzzahl, die die Eigenschaften-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1882">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="c3671-1883">DBKIND \_ PGUID \_ NAME 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-1883">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="c3671-1884">vString enthält einen Eigenschaftennamen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1884">vString contains a property name.</span></span> <span data-ttu-id="c3671-1885">Dieser Wert MUSS mit DBKIND \_ GUID \_ NAME identisch sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1885">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="c3671-1886">DBKIND \_ PGUID \_ PROPID 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3671-1886">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="c3671-1887">ulId enthält eine 4-Byte-Ganzzahl, die die Eigenschaften-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1887">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="c3671-1888">Dieser Wert MUSS mit DBKIND \_ GUID \_ PROPID identisch sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1888">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="c3671-1889">**GUID:** Die Eigenschaften-GUID.</span><span class="sxs-lookup"><span data-stu-id="c3671-1889">**GUID**: The property GUID.</span></span>

<span data-ttu-id="c3671-1890">**ulId:** Wenn eKind DBKIND \_ GUID PROPID oder DBKIND PGUID PROPID ist, enthält dieses Feld eine ganze Zahl ohne Vorzeichen, die die \_ \_ \_ Eigenschaften-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1890">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="c3671-1891">Wenn eKind DBKIND GUID NAME oder DBKIND PGUID NAME ist, enthält dieses Feld eine ganze Zahl ohne Vorzeichen, die die Anzahl von Unicode-Zeichen angibt, die \_ \_ im \_ \_ vString-Feld enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-1891">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="c3671-1892">**vString:** Eine nicht auf NULL terminierte Unicode-Zeichenfolge, die den Eigenschaftennamen darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1892">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="c3671-1893">Sie MUSS weggelassen werden, es sei denn, das eKind-Feld ist auf DBKIND \_ GUID \_ NAME oder DBKIND \_ PGUID \_ NAME festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1893">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="c3671-1894">2.2.1.21 CDbProp</span><span class="sxs-lookup"><span data-stu-id="c3671-1894">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="c3671-1895">Die CDbProp-Struktur enthält eine -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c3671-1895">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="c3671-1896">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1896">0</span></span>

<span data-ttu-id="c3671-1897">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1897">1</span></span>

<span data-ttu-id="c3671-1898">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1898">2</span></span>

<span data-ttu-id="c3671-1899">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1899">3</span></span>

<span data-ttu-id="c3671-1900">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1900">4</span></span>

<span data-ttu-id="c3671-1901">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1901">5</span></span>

<span data-ttu-id="c3671-1902">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1902">6</span></span>

<span data-ttu-id="c3671-1903">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1903">7</span></span>

<span data-ttu-id="c3671-1904">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1904">8</span></span>

<span data-ttu-id="c3671-1905">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1905">9</span></span>

<span data-ttu-id="c3671-1906">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1906">1</span></span><br/> <span data-ttu-id="c3671-1907">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1907">0</span></span><br/>

<span data-ttu-id="c3671-1908">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1908">1</span></span>

<span data-ttu-id="c3671-1909">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1909">2</span></span>

<span data-ttu-id="c3671-1910">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1910">3</span></span>

<span data-ttu-id="c3671-1911">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1911">4</span></span>

<span data-ttu-id="c3671-1912">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1912">5</span></span>

<span data-ttu-id="c3671-1913">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1913">6</span></span>

<span data-ttu-id="c3671-1914">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1914">7</span></span>

<span data-ttu-id="c3671-1915">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1915">8</span></span>

<span data-ttu-id="c3671-1916">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1916">9</span></span>

<span data-ttu-id="c3671-1917">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1917">2</span></span><br/> <span data-ttu-id="c3671-1918">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1918">0</span></span><br/>

<span data-ttu-id="c3671-1919">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1919">1</span></span>

<span data-ttu-id="c3671-1920">2</span><span class="sxs-lookup"><span data-stu-id="c3671-1920">2</span></span>

<span data-ttu-id="c3671-1921">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1921">3</span></span>

<span data-ttu-id="c3671-1922">4</span><span class="sxs-lookup"><span data-stu-id="c3671-1922">4</span></span>

<span data-ttu-id="c3671-1923">5</span><span class="sxs-lookup"><span data-stu-id="c3671-1923">5</span></span>

<span data-ttu-id="c3671-1924">6</span><span class="sxs-lookup"><span data-stu-id="c3671-1924">6</span></span>

<span data-ttu-id="c3671-1925">7</span><span class="sxs-lookup"><span data-stu-id="c3671-1925">7</span></span>

<span data-ttu-id="c3671-1926">8</span><span class="sxs-lookup"><span data-stu-id="c3671-1926">8</span></span>

<span data-ttu-id="c3671-1927">9</span><span class="sxs-lookup"><span data-stu-id="c3671-1927">9</span></span>

<span data-ttu-id="c3671-1928">3</span><span class="sxs-lookup"><span data-stu-id="c3671-1928">3</span></span><br/> <span data-ttu-id="c3671-1929">0</span><span class="sxs-lookup"><span data-stu-id="c3671-1929">0</span></span><br/>

<span data-ttu-id="c3671-1930">1</span><span class="sxs-lookup"><span data-stu-id="c3671-1930">1</span></span>

<span data-ttu-id="c3671-1931">DBPROPID</span><span class="sxs-lookup"><span data-stu-id="c3671-1931">DBPROPID</span></span>

<span data-ttu-id="c3671-1932">DBPROPOPTIONS</span><span class="sxs-lookup"><span data-stu-id="c3671-1932">DBPROPOPTIONS</span></span>

<span data-ttu-id="c3671-1933">DBPROPSTATUS</span><span class="sxs-lookup"><span data-stu-id="c3671-1933">DBPROPSTATUS</span></span>

<span data-ttu-id="c3671-1934">- (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1934">colid (variable)</span></span>

<span data-ttu-id="c3671-1935">vValue (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-1935">vValue (variable)</span></span>



 

<span data-ttu-id="c3671-1936">**DBPROPID:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Eigenschaften-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1936">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="c3671-1937">**DBPROPOPTIONS:** MUSS auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3671-1937">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="c3671-1938">**DBPROPSTATUS:** MUSS auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3671-1938">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="c3671-1939">**– eine** CDbColId-Struktur, wie in Abschnitt 2.2.1.20 angegeben, die die Spalte angibt, für die die Eigenschaft gilt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1939">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="c3671-1940">**vValue:** Eine CBaseStorageVariant,die den Eigenschaftswert enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-1940">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="c3671-1941">2.2.1.21.1 Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3671-1941">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="c3671-1942">In diesem Abschnitt werden die Eigenschaften beschrieben, die von CISP verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1942">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="c3671-1943">Diese Eigenschaften werden in drei Eigenschaftensätze ident2.2.1.21.1 im Feld guidPropertySet der CDbPropSet-Struktur (Abschnitt 2.2.1.22) eingeteilt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1943">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="c3671-1944">In der folgenden Tabelle sind die Eigenschaften aufgeführt, die Teil des DBPROPSET \_ FSCIFRMWRK \_ EXT-Eigenschaftensatz sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-1944">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="c3671-1945">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-1945">Value</span></span>                                  | <span data-ttu-id="c3671-1946">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-1946">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-1947">DBPROP \_ CI CATALOG NAME \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-1947">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="c3671-1948">Gibt den Namen des Katalogs oder der Kataloge an, der bzw. die abfragen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1948">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="c3671-1949">Der Wert MUSS ein VT \_ LPWSTR oder ein VT \_ VECTOR \| VT \_ LPWSTR sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1949">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="c3671-1950">DBPROP \_ CI \_ INCLUDE \_ SCOPES 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-1950">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="c3671-1951">Gibt einen oder mehrere Pfade an, die in die Abfrage eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1951">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="c3671-1952">Der Wert MUSS ein VT \_ LPWSTR oder ein VT \_ VECTOR \| VT \_ LPWSTR sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="c3671-1953">DBPROP \_ CI \_ SCOPE \_ FLAGS 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3671-1953">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="c3671-1954">Gibt an, wie die von der DBPROP \_ CI \_ INCLUDE \_ SCOPES-Eigenschaft angegebenen Pfade behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1954">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="c3671-1955">Der Wert MUSS ein VT \_ I4 oder ein VT \_ VECTOR \| VT \_ I4 sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1955">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="c3671-1956">ABFRAGETYP \_ "DBPROP \_ \_ CI" 0x00000007</span><span class="sxs-lookup"><span data-stu-id="c3671-1956">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="c3671-1957">Gibt den Typ der Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="c3671-1957">Specifies the type of query.</span></span> <span data-ttu-id="c3671-1958">Die CDbColId MUSS auf DB \_ NULLID festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1958">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="c3671-1959">In der folgenden Tabelle sind die Flags für die DBPROP \_ CI \_ SCOPE \_ FLAGS-Eigenschaft aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="c3671-1959">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="c3671-1960">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-1960">Value</span></span>                     | <span data-ttu-id="c3671-1961">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-1961">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-1962">QUERY \_ DEEP 0x01</span><span class="sxs-lookup"><span data-stu-id="c3671-1962">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="c3671-1963">Wenn festgelegt, gibt an, dass Dateien im Bereichsverzeichnis und in allen Unterverzeichnissen in den Ergebnissen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-1963">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="c3671-1964">Wenn dies klar ist, sind nur Dateien im Bereichsverzeichnis in den Ergebnissen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c3671-1964">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="c3671-1965">DARF NICHT mit QUERY DEEP kombiniert \_ werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1965">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="c3671-1966">QUERY \_ VIRTUAL \_ PATH 0x02</span><span class="sxs-lookup"><span data-stu-id="c3671-1966">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="c3671-1967">Wenn festgelegt, gibt an, dass der Bereich ein virtueller Pfad ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-1967">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="c3671-1968">Wenn dies klar ist, gibt an, dass der Bereich ein physisches Verzeichnis ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-1968">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="c3671-1969">In der folgenden Tabelle sind die Abfragetypen für die DBPROP \_ CI \_ QUERY \_ TYPE-Eigenschaft aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="c3671-1969">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="c3671-1970">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-1970">Value</span></span>                     | <span data-ttu-id="c3671-1971">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-1971">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-1972">CiNormal 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-1972">CiNormal 0x00000000</span></span>       | <span data-ttu-id="c3671-1973">Eine reguläre Abfrage.</span><span class="sxs-lookup"><span data-stu-id="c3671-1973">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="c3671-1974">CiVirtualRoots-0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-1974">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="c3671-1975">Die Abfrage fordert eine Liste der virtuellen Stämme des Katalogs an.</span><span class="sxs-lookup"><span data-stu-id="c3671-1975">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="c3671-1976">Dieser Wert erfordert Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="c3671-1976">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="c3671-1977">CiProperties-0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-1977">CiProperties 0x00000003</span></span>   | <span data-ttu-id="c3671-1978">Die Abfrage fordert eine Liste aller Eigenschaften an, die vom Indizierungsdienst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-1978">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="c3671-1979">CiAdminOp 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3671-1979">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="c3671-1980">Die Abfrage ist ein Verwaltungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="c3671-1980">The query is an administrative operation.</span></span> <span data-ttu-id="c3671-1981">Dieser Wert erfordert Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="c3671-1981">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="c3671-1982">In der folgenden Tabelle sind die Eigenschaften aufgeführt, die Teil des DBPROPSET \_ QUERYEXT-Eigenschaftensatz sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-1982">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="c3671-1983">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-1983">Value</span></span>                                      | <span data-ttu-id="c3671-1984">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-1984">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-1985">DBPROP \_ USECONTENTINDEX 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-1985">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="c3671-1986">Gibt an, wie der Indizierungsdienst langsame Abfragen verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1986">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="c3671-1987">Der Wert MUSS eine \_ VT-BOOL sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1987">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="c3671-1988">True gibt an, dass der Server für diese Abfragen einen Fehler ausführen darf.</span><span class="sxs-lookup"><span data-stu-id="c3671-1988">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="c3671-1989">DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-1989">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="c3671-1990">Gibt an, ob der Indizierungsdienst das Kürzen von Ergebnissen durchführen soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-1990">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="c3671-1991">True gibt an, dass der Server das Kürzen von Ergebnissen in einer Weise in Betracht ziehen soll, die die Antwortzeit für den Client optimiert.</span><span class="sxs-lookup"><span data-stu-id="c3671-1991">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="c3671-1992">Der Wert MUSS eine \_ VT-BOOL sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1992">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="c3671-1993">DBPROP \_ USEEXTENDEDDBTYPES 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3671-1993">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="c3671-1994">Gibt an, ob der Client VT \_ VECTOR-Datentypen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1994">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="c3671-1995">True gibt an, dass der Client VT VECTOR unterstützt. Bei FALSE konvertiert der Server VT VECTOR-Datentypen in \_ \_ VT \_ ARRAY-Datentypen.</span><span class="sxs-lookup"><span data-stu-id="c3671-1995">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="c3671-1996">Der Wert MUSS eine \_ VT-BOOL sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-1996">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="c3671-1997">DBPROP \_ FIRSTROWS-0x00000007</span><span class="sxs-lookup"><span data-stu-id="c3671-1997">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="c3671-1998">Gibt an, dass die Zeile entspricht, die zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-1998">Indicates the row matches to return.</span></span> <span data-ttu-id="c3671-1999">True gibt den ersten Satz übereinstimmende Zeilen zurück.</span><span class="sxs-lookup"><span data-stu-id="c3671-1999">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="c3671-2000">False gibt an, dass die am besten übereinstimmenden Zeilen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2000">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="c3671-2001">Der Wert MUSS eine \_ VT-BOOL sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-2001">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="c3671-2002">In der folgenden Tabelle sind die Eigenschaften aufgeführt, die Teil des DBPROPSET \_ CIFRMWRKCORE \_ EXT-Eigenschaftensatz sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-2002">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="c3671-2003">Value/DBPROPID</span><span class="sxs-lookup"><span data-stu-id="c3671-2003">Value / DBPROPID</span></span>                 | <span data-ttu-id="c3671-2004">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-2004">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-2005">DBPROP \_ MACHINE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-2005">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="c3671-2006">Gibt die Namen der Computer an, auf denen eine Abfrage verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-2006">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="c3671-2007">Der Wert MUSS entweder VT \_ BSTR oder VT \_ ARRAY \| VT \_ BSTR sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-2007">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="c3671-2008">DBPROP \_ CLIENT \_ CLSID 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-2008">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="c3671-2009">Gibt eine Verbindungskonst constant für den Indizierungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="c3671-2009">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="c3671-2010">Der Wert MUSS eine \_ VT-CLSID sein, die 0x2A4880706FD911D0A80800A0C906241A.</span><span class="sxs-lookup"><span data-stu-id="c3671-2010">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="c3671-2011">2.2.1.22 CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="c3671-2011">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="c3671-2012">Die CDbPropSet-Struktur enthält einen Satz von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c3671-2012">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="c3671-2013">Beachten Sie, dass das erste Feld eine feste Größe hat, aber möglicherweise nicht an einem Offset ausgerichtet ist, bei dem es sich um ein 4-Byte-Vielfaches vom Anfang der Nachricht handelt, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-2013">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="c3671-2014">Das Feld cProperties ist jedoch so ausgerichtet, und daher wird das Format wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="c3671-2014">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="c3671-2015">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2015">0</span></span>

<span data-ttu-id="c3671-2016">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2016">1</span></span>

<span data-ttu-id="c3671-2017">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2017">2</span></span>

<span data-ttu-id="c3671-2018">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2018">3</span></span>

<span data-ttu-id="c3671-2019">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2019">4</span></span>

<span data-ttu-id="c3671-2020">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2020">5</span></span>

<span data-ttu-id="c3671-2021">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2021">6</span></span>

<span data-ttu-id="c3671-2022">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2022">7</span></span>

<span data-ttu-id="c3671-2023">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2023">8</span></span>

<span data-ttu-id="c3671-2024">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2024">9</span></span>

<span data-ttu-id="c3671-2025">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2025">1</span></span><br/> <span data-ttu-id="c3671-2026">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2026">0</span></span><br/>

<span data-ttu-id="c3671-2027">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2027">1</span></span>

<span data-ttu-id="c3671-2028">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2028">2</span></span>

<span data-ttu-id="c3671-2029">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2029">3</span></span>

<span data-ttu-id="c3671-2030">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2030">4</span></span>

<span data-ttu-id="c3671-2031">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2031">5</span></span>

<span data-ttu-id="c3671-2032">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2032">6</span></span>

<span data-ttu-id="c3671-2033">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2033">7</span></span>

<span data-ttu-id="c3671-2034">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2034">8</span></span>

<span data-ttu-id="c3671-2035">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2035">9</span></span>

<span data-ttu-id="c3671-2036">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2036">2</span></span><br/> <span data-ttu-id="c3671-2037">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2037">0</span></span><br/>

<span data-ttu-id="c3671-2038">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2038">1</span></span>

<span data-ttu-id="c3671-2039">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2039">2</span></span>

<span data-ttu-id="c3671-2040">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2040">3</span></span>

<span data-ttu-id="c3671-2041">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2041">4</span></span>

<span data-ttu-id="c3671-2042">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2042">5</span></span>

<span data-ttu-id="c3671-2043">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2043">6</span></span>

<span data-ttu-id="c3671-2044">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2044">7</span></span>

<span data-ttu-id="c3671-2045">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2045">8</span></span>

<span data-ttu-id="c3671-2046">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2046">9</span></span>

<span data-ttu-id="c3671-2047">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2047">3</span></span><br/> <span data-ttu-id="c3671-2048">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2048">0</span></span><br/>

<span data-ttu-id="c3671-2049">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2049">1</span></span>

<span data-ttu-id="c3671-2050">guidPropertySet</span><span class="sxs-lookup"><span data-stu-id="c3671-2050">guidPropertySet</span></span>

<span data-ttu-id="c3671-2051">...</span><span class="sxs-lookup"><span data-stu-id="c3671-2051">...</span></span>

<span data-ttu-id="c3671-2052">...</span><span class="sxs-lookup"><span data-stu-id="c3671-2052">...</span></span>

<span data-ttu-id="c3671-2053">...</span><span class="sxs-lookup"><span data-stu-id="c3671-2053">...</span></span>

<span data-ttu-id="c3671-2054">...</span><span class="sxs-lookup"><span data-stu-id="c3671-2054">...</span></span>

<span data-ttu-id="c3671-2055">\_Auf padding (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-2055">\_padding (variable)</span></span>

<span data-ttu-id="c3671-2056">cProperties</span><span class="sxs-lookup"><span data-stu-id="c3671-2056">cProperties</span></span>

<span data-ttu-id="c3671-2057">aProps (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-2057">aProps (variable)</span></span>



 

<span data-ttu-id="c3671-2058">**guidPropertySet:** Eine GUID, die den Eigenschaftensatz identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c3671-2058">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="c3671-2059">MUSS auf das binäre Formular festgelegt werden, das einem der folgenden Werte entspricht (in Form einer Zeichenfolgendarstellung dargestellt), die den Eigenschaftensatz der eigenschaften identifiziert, die im aProps-Feld enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-2059">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="c3671-2060">Wert/GUID</span><span class="sxs-lookup"><span data-stu-id="c3671-2060">Value / GUID</span></span>                                                                              | <span data-ttu-id="c3671-2061">Name</span><span class="sxs-lookup"><span data-stu-id="c3671-2061">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="c3671-2062">DBPROPSET \_ FSCIFRMWRK \_ EXT</span><span class="sxs-lookup"><span data-stu-id="c3671-2062">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="c3671-2063">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="c3671-2063">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="c3671-2064">File System Content Index Framework-Eigenschaftensatz</span><span class="sxs-lookup"><span data-stu-id="c3671-2064">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="c3671-2065">DBPROPSET \_ QUERYEXT</span><span class="sxs-lookup"><span data-stu-id="c3671-2065">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="c3671-2066">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="c3671-2066">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="c3671-2067">Eigenschaftensatz der Abfrageerweiterung</span><span class="sxs-lookup"><span data-stu-id="c3671-2067">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="c3671-2068">DBPROPSET \_ CIFRMWRKCORE \_ EXT</span><span class="sxs-lookup"><span data-stu-id="c3671-2068">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="c3671-2069">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="c3671-2069">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="c3671-2070">Content Index Framework Core-Eigenschaftensatz</span><span class="sxs-lookup"><span data-stu-id="c3671-2070">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="c3671-2071">**\_ Padding**: Dieses Feld MUSS 0 bis 3 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-2071">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="c3671-2072">Die Länge dieses Felds MUSS so lang sein, dass das folgende Feld bei einem Offset beginnt, der ein Vielfaches von 4 Byte ab dem Anfang der Nachricht ist, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-2072">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="c3671-2073">Wenn dieses Feld vorhanden ist (d. h. länge ungleich 0), ist der enthaltene Wert willkürlich.</span><span class="sxs-lookup"><span data-stu-id="c3671-2073">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="c3671-2074">Der Inhalt dieses Felds MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2074">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3671-2075">**cProperties:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im aProps-Array enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-2075">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="c3671-2076">**aProps:** Ein Array von CDbProp-Strukturen, wie in Abschnitt 0 angegeben, das Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-2076">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="c3671-2077">Strukturen im Array MÜSSEN durch 0 bis 3 Auf abstandsbytes getrennt werden, damit jede Struktur an einem Offset beginnt, der ein Vielfaches von 4 Bytes vom Anfang der Nachricht ist, die dieses Array enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-2077">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="c3671-2078">Wenn Auf padding bytes vorhanden sind, ist der Wert, den sie enthalten, willkürlich.</span><span class="sxs-lookup"><span data-stu-id="c3671-2078">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="c3671-2079">Der Inhalt der Auf padding-Bytes MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2079">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="c3671-2080">2.2.1.23 CPidMapper</span><span class="sxs-lookup"><span data-stu-id="c3671-2080">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="c3671-2081">Die CPidMapper-Struktur enthält ein Array von Eigenschaften-IDs, die die Eigenschaften angeben, die in einem Rowset zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2081">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="c3671-2082">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2082">0</span></span>

<span data-ttu-id="c3671-2083">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2083">1</span></span>

<span data-ttu-id="c3671-2084">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2084">2</span></span>

<span data-ttu-id="c3671-2085">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2085">3</span></span>

<span data-ttu-id="c3671-2086">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2086">4</span></span>

<span data-ttu-id="c3671-2087">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2087">5</span></span>

<span data-ttu-id="c3671-2088">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2088">6</span></span>

<span data-ttu-id="c3671-2089">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2089">7</span></span>

<span data-ttu-id="c3671-2090">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2090">8</span></span>

<span data-ttu-id="c3671-2091">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2091">9</span></span>

<span data-ttu-id="c3671-2092">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2092">1</span></span><br/> <span data-ttu-id="c3671-2093">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2093">0</span></span><br/>

<span data-ttu-id="c3671-2094">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2094">1</span></span>

<span data-ttu-id="c3671-2095">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2095">2</span></span>

<span data-ttu-id="c3671-2096">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2096">3</span></span>

<span data-ttu-id="c3671-2097">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2097">4</span></span>

<span data-ttu-id="c3671-2098">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2098">5</span></span>

<span data-ttu-id="c3671-2099">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2099">6</span></span>

<span data-ttu-id="c3671-2100">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2100">7</span></span>

<span data-ttu-id="c3671-2101">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2101">8</span></span>

<span data-ttu-id="c3671-2102">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2102">9</span></span>

<span data-ttu-id="c3671-2103">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2103">2</span></span><br/> <span data-ttu-id="c3671-2104">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2104">0</span></span><br/>

<span data-ttu-id="c3671-2105">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2105">1</span></span>

<span data-ttu-id="c3671-2106">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2106">2</span></span>

<span data-ttu-id="c3671-2107">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2107">3</span></span>

<span data-ttu-id="c3671-2108">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2108">4</span></span>

<span data-ttu-id="c3671-2109">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2109">5</span></span>

<span data-ttu-id="c3671-2110">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2110">6</span></span>

<span data-ttu-id="c3671-2111">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2111">7</span></span>

<span data-ttu-id="c3671-2112">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2112">8</span></span>

<span data-ttu-id="c3671-2113">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2113">9</span></span>

<span data-ttu-id="c3671-2114">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2114">3</span></span><br/> <span data-ttu-id="c3671-2115">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2115">0</span></span><br/>

<span data-ttu-id="c3671-2116">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2116">1</span></span>

<span data-ttu-id="c3671-2117">count</span><span class="sxs-lookup"><span data-stu-id="c3671-2117">count</span></span>

<span data-ttu-id="c3671-2118">aPropSpec</span><span class="sxs-lookup"><span data-stu-id="c3671-2118">aPropSpec</span></span>

<span data-ttu-id="c3671-2119">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-2119">... (variable)</span></span>



 

<span data-ttu-id="c3671-2120">**count:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im aPropSpec-Array enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-2120">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="c3671-2121">**aPropSpec:** Array von CFullPropSpec-Strukturen, die die zurückzugebenden Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-2121">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="c3671-2122">Strukturen im Array MÜSSEN durch 0 bis 3 Auffüllungsbytes getrennt werden, sodass jede Struktur eine 4-Byte-Ausrichtung vom Anfang einer Nachricht aufweist.</span><span class="sxs-lookup"><span data-stu-id="c3671-2122">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="c3671-2123">Solche Auffüllungsbytes können beliebige Werte sein, und MÜSSEN beim Empfang ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2123">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="c3671-2124">2.2.1.24 CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="c3671-2124">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="c3671-2125">Die CRowSeekAt-Struktur enthält den Offset, an dem Zeilen in einer CPMGetRowsIn-Nachricht abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2125">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="c3671-2126">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2126">0</span></span>

<span data-ttu-id="c3671-2127">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2127">1</span></span>

<span data-ttu-id="c3671-2128">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2128">2</span></span>

<span data-ttu-id="c3671-2129">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2129">3</span></span>

<span data-ttu-id="c3671-2130">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2130">4</span></span>

<span data-ttu-id="c3671-2131">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2131">5</span></span>

<span data-ttu-id="c3671-2132">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2132">6</span></span>

<span data-ttu-id="c3671-2133">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2133">7</span></span>

<span data-ttu-id="c3671-2134">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2134">8</span></span>

<span data-ttu-id="c3671-2135">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2135">9</span></span>

<span data-ttu-id="c3671-2136">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2136">1</span></span><br/> <span data-ttu-id="c3671-2137">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2137">0</span></span><br/>

<span data-ttu-id="c3671-2138">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2138">1</span></span>

<span data-ttu-id="c3671-2139">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2139">2</span></span>

<span data-ttu-id="c3671-2140">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2140">3</span></span>

<span data-ttu-id="c3671-2141">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2141">4</span></span>

<span data-ttu-id="c3671-2142">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2142">5</span></span>

<span data-ttu-id="c3671-2143">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2143">6</span></span>

<span data-ttu-id="c3671-2144">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2144">7</span></span>

<span data-ttu-id="c3671-2145">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2145">8</span></span>

<span data-ttu-id="c3671-2146">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2146">9</span></span>

<span data-ttu-id="c3671-2147">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2147">2</span></span><br/> <span data-ttu-id="c3671-2148">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2148">0</span></span><br/>

<span data-ttu-id="c3671-2149">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2149">1</span></span>

<span data-ttu-id="c3671-2150">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2150">2</span></span>

<span data-ttu-id="c3671-2151">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2151">3</span></span>

<span data-ttu-id="c3671-2152">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2152">4</span></span>

<span data-ttu-id="c3671-2153">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2153">5</span></span>

<span data-ttu-id="c3671-2154">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2154">6</span></span>

<span data-ttu-id="c3671-2155">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2155">7</span></span>

<span data-ttu-id="c3671-2156">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2156">8</span></span>

<span data-ttu-id="c3671-2157">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2157">9</span></span>

<span data-ttu-id="c3671-2158">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2158">3</span></span><br/> <span data-ttu-id="c3671-2159">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2159">0</span></span><br/>

<span data-ttu-id="c3671-2160">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2160">1</span></span>

<span data-ttu-id="c3671-2161">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="c3671-2161">\_hRegion</span></span>

<span data-ttu-id="c3671-2162">\_cskip</span><span class="sxs-lookup"><span data-stu-id="c3671-2162">\_cskip</span></span>

<span data-ttu-id="c3671-2163">\_bmkOffset</span><span class="sxs-lookup"><span data-stu-id="c3671-2163">\_bmkOffset</span></span>



 

<span data-ttu-id="c3671-2164">**\_ hRegion:** MUSS auf 0x00000000 festgelegt werden, und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2164">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="c3671-2165">**\_ cskip:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeilen enthält, die im Rowset übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2165">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="c3671-2166">**\_ bmkOffset:** Ein 32-Bit-Wert, der das Handle des **Lesezeichens** darstellt, das die Anfangsposition angibt, von der aus die in cskip angegebene Anzahl von Zeilen übersprungen werden \_ soll, bevor mit dem Abrufen begonnen wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-2166">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="c3671-2167">2.2.1.25 CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="c3671-2167">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="c3671-2168">Die CRowSeekAtRatio-Struktur identifiziert den Punkt, an dem mit dem Abrufen einer CPMGetRowsIn-Nachricht begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-2168">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="c3671-2169">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2169">0</span></span>

<span data-ttu-id="c3671-2170">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2170">1</span></span>

<span data-ttu-id="c3671-2171">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2171">2</span></span>

<span data-ttu-id="c3671-2172">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2172">3</span></span>

<span data-ttu-id="c3671-2173">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2173">4</span></span>

<span data-ttu-id="c3671-2174">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2174">5</span></span>

<span data-ttu-id="c3671-2175">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2175">6</span></span>

<span data-ttu-id="c3671-2176">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2176">7</span></span>

<span data-ttu-id="c3671-2177">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2177">8</span></span>

<span data-ttu-id="c3671-2178">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2178">9</span></span>

<span data-ttu-id="c3671-2179">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2179">1</span></span><br/> <span data-ttu-id="c3671-2180">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2180">0</span></span><br/>

<span data-ttu-id="c3671-2181">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2181">1</span></span>

<span data-ttu-id="c3671-2182">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2182">2</span></span>

<span data-ttu-id="c3671-2183">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2183">3</span></span>

<span data-ttu-id="c3671-2184">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2184">4</span></span>

<span data-ttu-id="c3671-2185">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2185">5</span></span>

<span data-ttu-id="c3671-2186">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2186">6</span></span>

<span data-ttu-id="c3671-2187">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2187">7</span></span>

<span data-ttu-id="c3671-2188">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2188">8</span></span>

<span data-ttu-id="c3671-2189">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2189">9</span></span>

<span data-ttu-id="c3671-2190">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2190">2</span></span><br/> <span data-ttu-id="c3671-2191">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2191">0</span></span><br/>

<span data-ttu-id="c3671-2192">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2192">1</span></span>

<span data-ttu-id="c3671-2193">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2193">2</span></span>

<span data-ttu-id="c3671-2194">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2194">3</span></span>

<span data-ttu-id="c3671-2195">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2195">4</span></span>

<span data-ttu-id="c3671-2196">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2196">5</span></span>

<span data-ttu-id="c3671-2197">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2197">6</span></span>

<span data-ttu-id="c3671-2198">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2198">7</span></span>

<span data-ttu-id="c3671-2199">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2199">8</span></span>

<span data-ttu-id="c3671-2200">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2200">9</span></span>

<span data-ttu-id="c3671-2201">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2201">3</span></span><br/> <span data-ttu-id="c3671-2202">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2202">0</span></span><br/>

<span data-ttu-id="c3671-2203">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2203">1</span></span>

<span data-ttu-id="c3671-2204">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="c3671-2204">CiTblChapt</span></span>

<span data-ttu-id="c3671-2205">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="c3671-2205">\_hRegion</span></span>

<span data-ttu-id="c3671-2206">\_ulNumerator</span><span class="sxs-lookup"><span data-stu-id="c3671-2206">\_ulNumerator</span></span>

<span data-ttu-id="c3671-2207">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="c3671-2207">\_ulDenominator</span></span>



 

<span data-ttu-id="c3671-2208">**CiTblChapt:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Rowsetkapitel angibt, aus dem Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2208">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="c3671-2209">**\_ hRegion:** MUSS auf 0x00000000 festgelegt werden, und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2209">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="c3671-2210">**\_ ulNumerator:** 32-Bit-Ganzzahl ohne Vorzeichen, die den Zähler des Verhältnisses der Zeilen im Kapitel darstellt, an dem mit dem Abruf begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-2210">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="c3671-2211">**\_ ulDenominator:** 32-Bit-Ganzzahl ohne Vorzeichen, die den Nenner des Zeilenverhältnisses im Kapitel darstellt, an dem mit dem Abruf begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-2211">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="c3671-2212">MUSS größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-2212">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="c3671-2213">2.2.1.26 CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="c3671-2213">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="c3671-2214">Die CRowSeekByBookmark-Struktur identifiziert die Lesezeichen, aus denen Zeilen für eine CPMGetRowsIn-Nachricht abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2214">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="c3671-2215">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2215">0</span></span>

<span data-ttu-id="c3671-2216">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2216">1</span></span>

<span data-ttu-id="c3671-2217">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2217">2</span></span>

<span data-ttu-id="c3671-2218">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2218">3</span></span>

<span data-ttu-id="c3671-2219">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2219">4</span></span>

<span data-ttu-id="c3671-2220">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2220">5</span></span>

<span data-ttu-id="c3671-2221">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2221">6</span></span>

<span data-ttu-id="c3671-2222">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2222">7</span></span>

<span data-ttu-id="c3671-2223">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2223">8</span></span>

<span data-ttu-id="c3671-2224">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2224">9</span></span>

<span data-ttu-id="c3671-2225">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2225">1</span></span><br/> <span data-ttu-id="c3671-2226">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2226">0</span></span><br/>

<span data-ttu-id="c3671-2227">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2227">1</span></span>

<span data-ttu-id="c3671-2228">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2228">2</span></span>

<span data-ttu-id="c3671-2229">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2229">3</span></span>

<span data-ttu-id="c3671-2230">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2230">4</span></span>

<span data-ttu-id="c3671-2231">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2231">5</span></span>

<span data-ttu-id="c3671-2232">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2232">6</span></span>

<span data-ttu-id="c3671-2233">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2233">7</span></span>

<span data-ttu-id="c3671-2234">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2234">8</span></span>

<span data-ttu-id="c3671-2235">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2235">9</span></span>

<span data-ttu-id="c3671-2236">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2236">2</span></span><br/> <span data-ttu-id="c3671-2237">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2237">0</span></span><br/>

<span data-ttu-id="c3671-2238">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2238">1</span></span>

<span data-ttu-id="c3671-2239">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2239">2</span></span>

<span data-ttu-id="c3671-2240">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2240">3</span></span>

<span data-ttu-id="c3671-2241">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2241">4</span></span>

<span data-ttu-id="c3671-2242">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2242">5</span></span>

<span data-ttu-id="c3671-2243">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2243">6</span></span>

<span data-ttu-id="c3671-2244">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2244">7</span></span>

<span data-ttu-id="c3671-2245">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2245">8</span></span>

<span data-ttu-id="c3671-2246">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2246">9</span></span>

<span data-ttu-id="c3671-2247">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2247">3</span></span><br/> <span data-ttu-id="c3671-2248">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2248">0</span></span><br/>

<span data-ttu-id="c3671-2249">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2249">1</span></span>

<span data-ttu-id="c3671-2250">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="c3671-2250">\_hRegion</span></span>

<span data-ttu-id="c3671-2251">\_cBookmarks</span><span class="sxs-lookup"><span data-stu-id="c3671-2251">\_cBookmarks</span></span>

<span data-ttu-id="c3671-2252">\_maxRet</span><span class="sxs-lookup"><span data-stu-id="c3671-2252">\_maxRet</span></span>

<span data-ttu-id="c3671-2253">\_cValidRet</span><span class="sxs-lookup"><span data-stu-id="c3671-2253">\_cValidRet</span></span>

<span data-ttu-id="c3671-2254">\_aBookmarks (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-2254">\_aBookmarks (variable)</span></span>

<span data-ttu-id="c3671-2255">\_ascRet (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-2255">\_ascRet (variable)</span></span>



 

<span data-ttu-id="c3671-2256">**\_ hRegion:** MUSS auf 0x00000000 festgelegt werden, und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2256">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="c3671-2257">**\_ cBookmarks:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im \_ aBookmarks-Array darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2257">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="c3671-2258">**\_ maxRet:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im \_ ascRet-Array darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2258">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="c3671-2259">**\_ cValidRet:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl gültiger Elemente im \_ ascRet-Array darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2259">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="c3671-2260">Gültige Elemente wurden im Array definiert, während ungültige Elemente nicht definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-2260">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="c3671-2261">**\_ aBookmarks:** Ein Array von Lesezeichenhandles (jeweils durch 4 Bytes dargestellt), wie aus einer CPMGetRowsOut-Nachricht abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2261">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="c3671-2262">**\_ ascRet:** Ein Array von HRESULT-Werten.</span><span class="sxs-lookup"><span data-stu-id="c3671-2262">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="c3671-2263">Wenn CRowSeekByBookMark als Teil der CPMGetRowsIn-Anforderung gesendet wird, MUSS die Anzahl der Einträge im Array \_ gleich cBookMarks sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-2263">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="c3671-2264">Beim Senden durch den Client MÜSSEN die Werte auf 0 festgelegt werden, und der Server MUSS den Inhalt des Arrays ignorieren.</span><span class="sxs-lookup"><span data-stu-id="c3671-2264">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="c3671-2265">Beim Senden durch den Server (als Teil der CPMGetRowsOut-Nachricht) geben die Werte im Array den Ergebnisstatus für jeden Zeilenabruf an.</span><span class="sxs-lookup"><span data-stu-id="c3671-2265">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="c3671-2266">2.2.1.27 CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="c3671-2266">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="c3671-2267">Die CRowSeekNext-Struktur enthält die Anzahl der Zeilen, die in einer CPMGetRowsIn-Nachricht übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2267">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="c3671-2268">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2268">0</span></span>

<span data-ttu-id="c3671-2269">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2269">1</span></span>

<span data-ttu-id="c3671-2270">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2270">2</span></span>

<span data-ttu-id="c3671-2271">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2271">3</span></span>

<span data-ttu-id="c3671-2272">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2272">4</span></span>

<span data-ttu-id="c3671-2273">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2273">5</span></span>

<span data-ttu-id="c3671-2274">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2274">6</span></span>

<span data-ttu-id="c3671-2275">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2275">7</span></span>

<span data-ttu-id="c3671-2276">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2276">8</span></span>

<span data-ttu-id="c3671-2277">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2277">9</span></span>

<span data-ttu-id="c3671-2278">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2278">1</span></span><br/> <span data-ttu-id="c3671-2279">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2279">0</span></span><br/>

<span data-ttu-id="c3671-2280">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2280">1</span></span>

<span data-ttu-id="c3671-2281">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2281">2</span></span>

<span data-ttu-id="c3671-2282">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2282">3</span></span>

<span data-ttu-id="c3671-2283">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2283">4</span></span>

<span data-ttu-id="c3671-2284">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2284">5</span></span>

<span data-ttu-id="c3671-2285">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2285">6</span></span>

<span data-ttu-id="c3671-2286">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2286">7</span></span>

<span data-ttu-id="c3671-2287">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2287">8</span></span>

<span data-ttu-id="c3671-2288">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2288">9</span></span>

<span data-ttu-id="c3671-2289">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2289">2</span></span><br/> <span data-ttu-id="c3671-2290">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2290">0</span></span><br/>

<span data-ttu-id="c3671-2291">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2291">1</span></span>

<span data-ttu-id="c3671-2292">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2292">2</span></span>

<span data-ttu-id="c3671-2293">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2293">3</span></span>

<span data-ttu-id="c3671-2294">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2294">4</span></span>

<span data-ttu-id="c3671-2295">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2295">5</span></span>

<span data-ttu-id="c3671-2296">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2296">6</span></span>

<span data-ttu-id="c3671-2297">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2297">7</span></span>

<span data-ttu-id="c3671-2298">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2298">8</span></span>

<span data-ttu-id="c3671-2299">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2299">9</span></span>

<span data-ttu-id="c3671-2300">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2300">3</span></span><br/> <span data-ttu-id="c3671-2301">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2301">0</span></span><br/>

<span data-ttu-id="c3671-2302">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2302">1</span></span>

<span data-ttu-id="c3671-2303">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="c3671-2303">CiTblChapt</span></span>

<span data-ttu-id="c3671-2304">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="c3671-2304">\_hRegion</span></span>

<span data-ttu-id="c3671-2305">\_cskip</span><span class="sxs-lookup"><span data-stu-id="c3671-2305">\_cskip</span></span>



 

<span data-ttu-id="c3671-2306">**CiTblChapt:** 32-Bit-Ganzzahl ohne Vorzeichen, die das Rowsetkapitel angibt, aus dem Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2306">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="c3671-2307">**\_ hRegion:** MUSS auf 0x00000000 festgelegt werden, und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2307">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="c3671-2308">**\_ cskip:** 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeilen darstellt, die im Rowset übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2308">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="c3671-2309">2.2.1.28 CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="c3671-2309">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="c3671-2310">Die CRowsetProperties-Struktur enthält Konfigurationsinformationen für eine Abfrage.</span><span class="sxs-lookup"><span data-stu-id="c3671-2310">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="c3671-2311">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2311">0</span></span>

<span data-ttu-id="c3671-2312">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2312">1</span></span>

<span data-ttu-id="c3671-2313">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2313">2</span></span>

<span data-ttu-id="c3671-2314">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2314">3</span></span>

<span data-ttu-id="c3671-2315">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2315">4</span></span>

<span data-ttu-id="c3671-2316">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2316">5</span></span>

<span data-ttu-id="c3671-2317">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2317">6</span></span>

<span data-ttu-id="c3671-2318">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2318">7</span></span>

<span data-ttu-id="c3671-2319">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2319">8</span></span>

<span data-ttu-id="c3671-2320">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2320">9</span></span>

<span data-ttu-id="c3671-2321">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2321">1</span></span><br/> <span data-ttu-id="c3671-2322">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2322">0</span></span><br/>

<span data-ttu-id="c3671-2323">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2323">1</span></span>

<span data-ttu-id="c3671-2324">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2324">2</span></span>

<span data-ttu-id="c3671-2325">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2325">3</span></span>

<span data-ttu-id="c3671-2326">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2326">4</span></span>

<span data-ttu-id="c3671-2327">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2327">5</span></span>

<span data-ttu-id="c3671-2328">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2328">6</span></span>

<span data-ttu-id="c3671-2329">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2329">7</span></span>

<span data-ttu-id="c3671-2330">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2330">8</span></span>

<span data-ttu-id="c3671-2331">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2331">9</span></span>

<span data-ttu-id="c3671-2332">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2332">2</span></span><br/> <span data-ttu-id="c3671-2333">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2333">0</span></span><br/>

<span data-ttu-id="c3671-2334">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2334">1</span></span>

<span data-ttu-id="c3671-2335">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2335">2</span></span>

<span data-ttu-id="c3671-2336">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2336">3</span></span>

<span data-ttu-id="c3671-2337">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2337">4</span></span>

<span data-ttu-id="c3671-2338">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2338">5</span></span>

<span data-ttu-id="c3671-2339">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2339">6</span></span>

<span data-ttu-id="c3671-2340">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2340">7</span></span>

<span data-ttu-id="c3671-2341">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2341">8</span></span>

<span data-ttu-id="c3671-2342">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2342">9</span></span>

<span data-ttu-id="c3671-2343">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2343">3</span></span><br/> <span data-ttu-id="c3671-2344">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2344">0</span></span><br/>

<span data-ttu-id="c3671-2345">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2345">1</span></span>

<span data-ttu-id="c3671-2346">\_uBooleanOptions</span><span class="sxs-lookup"><span data-stu-id="c3671-2346">\_uBooleanOptions</span></span>

<span data-ttu-id="c3671-2347">\_ulMaxOpenRows</span><span class="sxs-lookup"><span data-stu-id="c3671-2347">\_ulMaxOpenRows</span></span>

<span data-ttu-id="c3671-2348">\_ulMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="c3671-2348">\_ulMemoryUsage</span></span>

<span data-ttu-id="c3671-2349">\_cMaxResults</span><span class="sxs-lookup"><span data-stu-id="c3671-2349">\_cMaxResults</span></span>

<span data-ttu-id="c3671-2350">\_cCmdTimeout</span><span class="sxs-lookup"><span data-stu-id="c3671-2350">\_cCmdTimeout</span></span>



 

<span data-ttu-id="c3671-2351">**\_ uBooleanOptions:** Die 3 Bits dieses Felds mit der geringsten Bedeutung MÜSSEN einen der folgenden drei Werte enthalten:</span><span class="sxs-lookup"><span data-stu-id="c3671-2351">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="c3671-2352">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-2352">Value</span></span>                  | <span data-ttu-id="c3671-2353">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-2353">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c3671-2354">eSequential 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-2354">eSequential 0x00000001</span></span> | <span data-ttu-id="c3671-2355">Der Cursor kann nur vorwärts bewegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2355">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="c3671-2356">eLocatable 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-2356">eLocatable 0x00000003</span></span>  | <span data-ttu-id="c3671-2357">Der Cursor kann an eine beliebige Position verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2357">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="c3671-2358">eScrollable 0x00000007</span><span class="sxs-lookup"><span data-stu-id="c3671-2358">eScrollable 0x00000007</span></span> | <span data-ttu-id="c3671-2359">Der Cursor kann an eine beliebige Position verschoben und in beliebiger Richtung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2359">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="c3671-2360">Die verbleibenden Bits können entweder klar sein oder auf eine beliebige Kombination der folgenden Werte festgelegt werden, logisch OR'd zusammen:</span><span class="sxs-lookup"><span data-stu-id="c3671-2360">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="c3671-2361">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-2361">Value</span></span>                     | <span data-ttu-id="c3671-2362">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-2362">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-2363">eAsynchronous 0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3671-2363">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="c3671-2364">Der Client wartet nicht auf den Abschluss der Ausführung.</span><span class="sxs-lookup"><span data-stu-id="c3671-2364">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="c3671-2365">eFirstRows 0x00000080</span><span class="sxs-lookup"><span data-stu-id="c3671-2365">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="c3671-2366">Gibt die ersten gefundenen Zeilen zurück, nicht die besten Übereinstimmungen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2366">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="c3671-2367">eHoldRows 0x00000200</span><span class="sxs-lookup"><span data-stu-id="c3671-2367">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="c3671-2368">Der Server DARF KEINE Zeilen verwerfen, bis der Client mit einer Abfrage fertig ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-2368">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="c3671-2369">eChaptered 0x00000800</span><span class="sxs-lookup"><span data-stu-id="c3671-2369">eChaptered 0x00000800</span></span>     | <span data-ttu-id="c3671-2370">Das Rowset unterstützt Kapitel.</span><span class="sxs-lookup"><span data-stu-id="c3671-2370">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="c3671-2371">eUseCI 0x00001000</span><span class="sxs-lookup"><span data-stu-id="c3671-2371">eUseCI 0x00001000</span></span>         | <span data-ttu-id="c3671-2372">Beantworten Sie nur die Abfrage aus dem Index, nicht aus dem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="c3671-2372">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="c3671-2373">eDeferTrimming 0x00002000</span><span class="sxs-lookup"><span data-stu-id="c3671-2373">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="c3671-2374">Der Indizierungsdienst sollte beim Entfernen von Ergebnissen die Optimierung der Antwortzeit für den Client in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2374">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="c3671-2375">**\_ ulMaxOpenRows:** 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2375">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="c3671-2376">Muss auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2376">Must be set to 0x00000000.</span></span> <span data-ttu-id="c3671-2377">Nicht verwendet und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2377">Not used and MUST be ignored.</span></span>

<span data-ttu-id="c3671-2378">**\_ ulMemoryUsage:** 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2378">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="c3671-2379">Muss auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="c3671-2380">Nicht verwendet und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="c3671-2381">**\_ cMaxResults:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die maximale Anzahl von Zeilen angibt, die für die Abfrage zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2381">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="c3671-2382">**\_ cCmdTimeout:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Sekunden angibt, nach denen für eine Abfrage ein Timeout und ein automatisches Beenden ausgeführt werden soll. Dabei wird ab dem Zeitpunkt gezählt, zu dem die Abfrage auf dem Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-2382">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="c3671-2383">Der Wert 0x00000000 bedeutet, dass für die Abfrage kein Time out erfolgt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2383">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="c3671-2384">2.2.1.29 CRowVariant</span><span class="sxs-lookup"><span data-stu-id="c3671-2384">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="c3671-2385">Die CRowVariant-Struktur enthält den festen Größenteil eines Datentyps variabler Länge, der in der CPMGetRowsOut-Nachricht gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-2385">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="c3671-2386">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2386">0</span></span>

<span data-ttu-id="c3671-2387">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2387">1</span></span>

<span data-ttu-id="c3671-2388">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2388">2</span></span>

<span data-ttu-id="c3671-2389">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2389">3</span></span>

<span data-ttu-id="c3671-2390">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2390">4</span></span>

<span data-ttu-id="c3671-2391">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2391">5</span></span>

<span data-ttu-id="c3671-2392">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2392">6</span></span>

<span data-ttu-id="c3671-2393">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2393">7</span></span>

<span data-ttu-id="c3671-2394">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2394">8</span></span>

<span data-ttu-id="c3671-2395">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2395">9</span></span>

<span data-ttu-id="c3671-2396">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2396">1</span></span><br/> <span data-ttu-id="c3671-2397">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2397">0</span></span><br/>

<span data-ttu-id="c3671-2398">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2398">1</span></span>

<span data-ttu-id="c3671-2399">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2399">2</span></span>

<span data-ttu-id="c3671-2400">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2400">3</span></span>

<span data-ttu-id="c3671-2401">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2401">4</span></span>

<span data-ttu-id="c3671-2402">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2402">5</span></span>

<span data-ttu-id="c3671-2403">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2403">6</span></span>

<span data-ttu-id="c3671-2404">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2404">7</span></span>

<span data-ttu-id="c3671-2405">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2405">8</span></span>

<span data-ttu-id="c3671-2406">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2406">9</span></span>

<span data-ttu-id="c3671-2407">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2407">2</span></span><br/> <span data-ttu-id="c3671-2408">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2408">0</span></span><br/>

<span data-ttu-id="c3671-2409">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2409">1</span></span>

<span data-ttu-id="c3671-2410">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2410">2</span></span>

<span data-ttu-id="c3671-2411">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2411">3</span></span>

<span data-ttu-id="c3671-2412">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2412">4</span></span>

<span data-ttu-id="c3671-2413">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2413">5</span></span>

<span data-ttu-id="c3671-2414">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2414">6</span></span>

<span data-ttu-id="c3671-2415">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2415">7</span></span>

<span data-ttu-id="c3671-2416">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2416">8</span></span>

<span data-ttu-id="c3671-2417">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2417">9</span></span>

<span data-ttu-id="c3671-2418">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2418">3</span></span><br/> <span data-ttu-id="c3671-2419">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2419">0</span></span><br/>

<span data-ttu-id="c3671-2420">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2420">1</span></span>

<span data-ttu-id="c3671-2421">vType</span><span class="sxs-lookup"><span data-stu-id="c3671-2421">vType</span></span>

<span data-ttu-id="c3671-2422">reserviert1</span><span class="sxs-lookup"><span data-stu-id="c3671-2422">reserved1</span></span>

<span data-ttu-id="c3671-2423">reserved2</span><span class="sxs-lookup"><span data-stu-id="c3671-2423">reserved2</span></span>

<span data-ttu-id="c3671-2424">Offset (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-2424">Offset (optional)</span></span>



 

<span data-ttu-id="c3671-2425">**vType:** Ein Typindikator, der den Typ von vValue angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2425">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="c3671-2426">Dabei MUSS es sich um einen der in Abschnitt 2.2.1.1 angegebenen VARENUM-Werte handeln.</span><span class="sxs-lookup"><span data-stu-id="c3671-2426">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="c3671-2427">**reserved1:** Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3671-2427">**reserved1**: Not used.</span></span> <span data-ttu-id="c3671-2428">Der Wert kann auf einen beliebigen Wert festgelegt werden, und er MUSS beim Empfang ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2428">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="c3671-2429">**reserved2:** Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3671-2429">**reserved2**: Not used.</span></span> <span data-ttu-id="c3671-2430">Der Wert kann auf einen beliebigen Wert festgelegt werden, und er MUSS beim Empfang ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2430">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="c3671-2431">**Offset:** Ein Offset zu Daten variabler Länge (z. B. eine Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="c3671-2431">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="c3671-2432">Dies MUSS ein 32-Bit-Wert (4 Bytes lang) sein, wenn 32-Bit-Offsets verwendet werden (gemäß den Regeln in Abschnitt 2.2.3.16) oder ein 64-Byte-Wert (8 Bytes lang), wenn 64-Bit-Offsets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2432">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="c3671-2433">2.2.1.30 CSortSet</span><span class="sxs-lookup"><span data-stu-id="c3671-2433">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="c3671-2434">Die CSortSet-Struktur enthält die Sortierreihenfolge der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="c3671-2434">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="c3671-2435">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2435">0</span></span>

<span data-ttu-id="c3671-2436">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2436">1</span></span>

<span data-ttu-id="c3671-2437">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2437">2</span></span>

<span data-ttu-id="c3671-2438">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2438">3</span></span>

<span data-ttu-id="c3671-2439">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2439">4</span></span>

<span data-ttu-id="c3671-2440">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2440">5</span></span>

<span data-ttu-id="c3671-2441">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2441">6</span></span>

<span data-ttu-id="c3671-2442">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2442">7</span></span>

<span data-ttu-id="c3671-2443">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2443">8</span></span>

<span data-ttu-id="c3671-2444">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2444">9</span></span>

<span data-ttu-id="c3671-2445">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2445">1</span></span><br/> <span data-ttu-id="c3671-2446">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2446">0</span></span><br/>

<span data-ttu-id="c3671-2447">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2447">1</span></span>

<span data-ttu-id="c3671-2448">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2448">2</span></span>

<span data-ttu-id="c3671-2449">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2449">3</span></span>

<span data-ttu-id="c3671-2450">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2450">4</span></span>

<span data-ttu-id="c3671-2451">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2451">5</span></span>

<span data-ttu-id="c3671-2452">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2452">6</span></span>

<span data-ttu-id="c3671-2453">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2453">7</span></span>

<span data-ttu-id="c3671-2454">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2454">8</span></span>

<span data-ttu-id="c3671-2455">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2455">9</span></span>

<span data-ttu-id="c3671-2456">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2456">2</span></span><br/> <span data-ttu-id="c3671-2457">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2457">0</span></span><br/>

<span data-ttu-id="c3671-2458">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2458">1</span></span>

<span data-ttu-id="c3671-2459">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2459">2</span></span>

<span data-ttu-id="c3671-2460">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2460">3</span></span>

<span data-ttu-id="c3671-2461">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2461">4</span></span>

<span data-ttu-id="c3671-2462">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2462">5</span></span>

<span data-ttu-id="c3671-2463">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2463">6</span></span>

<span data-ttu-id="c3671-2464">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2464">7</span></span>

<span data-ttu-id="c3671-2465">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2465">8</span></span>

<span data-ttu-id="c3671-2466">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2466">9</span></span>

<span data-ttu-id="c3671-2467">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2467">3</span></span><br/> <span data-ttu-id="c3671-2468">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2468">0</span></span><br/>

<span data-ttu-id="c3671-2469">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2469">1</span></span>

<span data-ttu-id="c3671-2470">Anzahl</span><span class="sxs-lookup"><span data-stu-id="c3671-2470">Count</span></span>

<span data-ttu-id="c3671-2471">sortArray (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-2471">sortArray (variable)</span></span>



 

<span data-ttu-id="c3671-2472">**count:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente in sortArray angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2472">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="c3671-2473">**sortArray:** Ein Array von CSort-Strukturen, das die Reihenfolge beschreibt, in der die Ergebnisse der Abfrage sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2473">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="c3671-2474">Strukturen im Array MÜSSEN durch 0 bis 3 Auffüllungsbytes getrennt werden, sodass jede Struktur eine 4-Byte-Ausrichtung vom Anfang einer Nachricht aufweist.</span><span class="sxs-lookup"><span data-stu-id="c3671-2474">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="c3671-2475">Solche Auffüllungsbytes können beliebige Werte sein, und MÜSSEN beim Empfang ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2475">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="c3671-2476">2.2.1.31 CTableColumn</span><span class="sxs-lookup"><span data-stu-id="c3671-2476">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="c3671-2477">Die CTableColumn-Struktur enthält eine Spalte einer CPMSetBindingsIn-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c3671-2477">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="c3671-2478">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2478">0</span></span>

<span data-ttu-id="c3671-2479">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2479">1</span></span>

<span data-ttu-id="c3671-2480">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2480">2</span></span>

<span data-ttu-id="c3671-2481">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2481">3</span></span>

<span data-ttu-id="c3671-2482">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2482">4</span></span>

<span data-ttu-id="c3671-2483">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2483">5</span></span>

<span data-ttu-id="c3671-2484">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2484">6</span></span>

<span data-ttu-id="c3671-2485">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2485">7</span></span>

<span data-ttu-id="c3671-2486">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2486">8</span></span>

<span data-ttu-id="c3671-2487">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2487">9</span></span>

<span data-ttu-id="c3671-2488">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2488">1</span></span><br/> <span data-ttu-id="c3671-2489">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2489">0</span></span><br/>

<span data-ttu-id="c3671-2490">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2490">1</span></span>

<span data-ttu-id="c3671-2491">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2491">2</span></span>

<span data-ttu-id="c3671-2492">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2492">3</span></span>

<span data-ttu-id="c3671-2493">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2493">4</span></span>

<span data-ttu-id="c3671-2494">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2494">5</span></span>

<span data-ttu-id="c3671-2495">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2495">6</span></span>

<span data-ttu-id="c3671-2496">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2496">7</span></span>

<span data-ttu-id="c3671-2497">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2497">8</span></span>

<span data-ttu-id="c3671-2498">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2498">9</span></span>

<span data-ttu-id="c3671-2499">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2499">2</span></span><br/> <span data-ttu-id="c3671-2500">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2500">0</span></span><br/>

<span data-ttu-id="c3671-2501">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2501">1</span></span>

<span data-ttu-id="c3671-2502">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2502">2</span></span>

<span data-ttu-id="c3671-2503">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2503">3</span></span>

<span data-ttu-id="c3671-2504">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2504">4</span></span>

<span data-ttu-id="c3671-2505">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2505">5</span></span>

<span data-ttu-id="c3671-2506">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2506">6</span></span>

<span data-ttu-id="c3671-2507">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2507">7</span></span>

<span data-ttu-id="c3671-2508">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2508">8</span></span>

<span data-ttu-id="c3671-2509">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2509">9</span></span>

<span data-ttu-id="c3671-2510">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2510">3</span></span><br/> <span data-ttu-id="c3671-2511">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2511">0</span></span><br/>

<span data-ttu-id="c3671-2512">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2512">1</span></span>

<span data-ttu-id="c3671-2513">PropSpec</span><span class="sxs-lookup"><span data-stu-id="c3671-2513">PropSpec</span></span>

<span data-ttu-id="c3671-2514">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-2514">...(variable)</span></span>

<span data-ttu-id="c3671-2515">vType</span><span class="sxs-lookup"><span data-stu-id="c3671-2515">vType</span></span>

<span data-ttu-id="c3671-2516">ValueUsed</span><span class="sxs-lookup"><span data-stu-id="c3671-2516">ValueUsed</span></span>

<span data-ttu-id="c3671-2517">\_padding1 (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-2517">\_padding1 (optional)</span></span>

<span data-ttu-id="c3671-2518">ValueOffset (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-2518">ValueOffset (optional)</span></span>

<span data-ttu-id="c3671-2519">ValueSize (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-2519">ValueSize (optional)</span></span>

<span data-ttu-id="c3671-2520">StatusUsed</span><span class="sxs-lookup"><span data-stu-id="c3671-2520">StatusUsed</span></span>

<span data-ttu-id="c3671-2521">\_padding2 (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-2521">\_padding2 (optional)</span></span>

<span data-ttu-id="c3671-2522">StatusOffset (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-2522">StatusOffset (optional)</span></span>

<span data-ttu-id="c3671-2523">LengthUsed</span><span class="sxs-lookup"><span data-stu-id="c3671-2523">LengthUsed</span></span>

<span data-ttu-id="c3671-2524">\_padding3 (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-2524">\_padding3 (optional)</span></span>

<span data-ttu-id="c3671-2525">LengthOffset (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-2525">LengthOffset (optional)</span></span>



 

<span data-ttu-id="c3671-2526">**PropSpec:** Eine CFullPropSpec-Struktur gemäß Abschnitt 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="c3671-2526">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="c3671-2527">**vType:** Gibt den Typ des in der Spalte enthaltenen Datenwerts an.</span><span class="sxs-lookup"><span data-stu-id="c3671-2527">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="c3671-2528">Die Liste der Werte für dieses Feld finden Sie im Feld vType in Abschnitt 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="c3671-2528">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="c3671-2529">**ValueUsed:** Ein 1-Byte-Feld, das auf 0x01 oder 0x00 festgelegt werden MUSS.</span><span class="sxs-lookup"><span data-stu-id="c3671-2529">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="c3671-2530">Wenn 0x01 festgelegt ist, wird die Spalte innerhalb der Zeile mit fester Größe übertragen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2530">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="c3671-2531">Wenn 0x00 festgelegt ist, wird der Wert der Spalte im Abschnitt mit variabler Länge am Ende des Puffers übertragen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2531">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="c3671-2532">**\_ padding1:** Ein 1-Byte-Feld, das vor ValueOffset eingefügt werden MUSS, wenn ValueOffset ohne dieses Feld nicht mit einem geraden Offset vom Anfang der Nachricht beginnen würde.</span><span class="sxs-lookup"><span data-stu-id="c3671-2532">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="c3671-2533">Der Wert dieses Byte ist willkürlich und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2533">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="c3671-2534">Wenn ValueUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-2534">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="c3671-2535">**ValueOffset:** Eine 2-Byte-Ganzzahl ohne Vorzeichen, die den Offset des Spaltenwerts in der Zeile angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2535">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="c3671-2536">Wenn ValueUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-2536">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="c3671-2537">**ValueSize:** Eine 2-Byte-Ganzzahl ohne Vorzeichen, die die Größe des Spaltenwerts in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2537">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="c3671-2538">Wenn ValueUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-2538">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="c3671-2539">**StatusUsed:** Ein 1-Byte-Feld, das auf 0x01 oder 0x00 festgelegt werden MUSS.</span><span class="sxs-lookup"><span data-stu-id="c3671-2539">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="c3671-2540">Wenn 0x01 festgelegt ist, wird der Status der Spalte innerhalb der Zeile übertragen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2540">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="c3671-2541">Wenn 0x00, wird der Status der Spalte nicht innerhalb der Zeile übertragen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2541">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="c3671-2542">**\_ padding2:** Ein 1-Byte-Feld, das vor StatusOffset eingefügt werden MUSS, wenn das Feld StatusOffset ohne dieses Feld nicht mit einem geraden Offset vom Anfang der Nachricht beginnen würde.</span><span class="sxs-lookup"><span data-stu-id="c3671-2542">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="c3671-2543">Der Wert dieses Byte ist willkürlich und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2543">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="c3671-2544">Wenn StatusUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-2544">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="c3671-2545">**StatusOffset:** Eine 2-Byte-Ganzzahl ohne Vorzeichen, die den Offset des Spaltenstatus in der Zeile angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2545">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="c3671-2546">Wenn StatusUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-2546">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="c3671-2547">**LengthUsed:** Ein 1-Byte-Feld, das auf 0x01 oder 0x00 festgelegt werden MUSS.</span><span class="sxs-lookup"><span data-stu-id="c3671-2547">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="c3671-2548">Wenn 0x01 festgelegt ist, wird die Länge der Spalte innerhalb der Zeile übertragen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2548">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="c3671-2549">Wenn 0x00, DARF die Länge der Spalte NICHT innerhalb der Zeile übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2549">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="c3671-2550">**\_ padding3:** Ein 1-Byte-Feld, das vor LengthOffset eingefügt werden MUSS, wenn LengthOffset ohne dieses Feld nicht mit einem geraden Offset vom Anfang einer Nachricht beginnen würde.</span><span class="sxs-lookup"><span data-stu-id="c3671-2550">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="c3671-2551">Der Wert dieses Byte ist willkürlich und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2551">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="c3671-2552">Wenn LengthUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-2552">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="c3671-2553">**LengthOffset:** Eine 2-Byte-Ganzzahl ohne Vorzeichen, die den Offset der Spaltenlänge in der Zeile angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2553">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="c3671-2554">Wenn LengthUsed auf 0x00 festgelegt ist, DARF dieses Feld NICHT vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-2554">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="c3671-2555">2.2.1.32 SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="c3671-2555">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="c3671-2556">Die SERIALIZEDPROPERTYVALUE-Struktur enthält einen serialisierten Wert.</span><span class="sxs-lookup"><span data-stu-id="c3671-2556">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="c3671-2557">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2557">0</span></span>

<span data-ttu-id="c3671-2558">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2558">1</span></span>

<span data-ttu-id="c3671-2559">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2559">2</span></span>

<span data-ttu-id="c3671-2560">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2560">3</span></span>

<span data-ttu-id="c3671-2561">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2561">4</span></span>

<span data-ttu-id="c3671-2562">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2562">5</span></span>

<span data-ttu-id="c3671-2563">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2563">6</span></span>

<span data-ttu-id="c3671-2564">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2564">7</span></span>

<span data-ttu-id="c3671-2565">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2565">8</span></span>

<span data-ttu-id="c3671-2566">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2566">9</span></span>

<span data-ttu-id="c3671-2567">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2567">1</span></span><br/> <span data-ttu-id="c3671-2568">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2568">0</span></span><br/>

<span data-ttu-id="c3671-2569">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2569">1</span></span>

<span data-ttu-id="c3671-2570">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2570">2</span></span>

<span data-ttu-id="c3671-2571">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2571">3</span></span>

<span data-ttu-id="c3671-2572">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2572">4</span></span>

<span data-ttu-id="c3671-2573">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2573">5</span></span>

<span data-ttu-id="c3671-2574">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2574">6</span></span>

<span data-ttu-id="c3671-2575">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2575">7</span></span>

<span data-ttu-id="c3671-2576">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2576">8</span></span>

<span data-ttu-id="c3671-2577">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2577">9</span></span>

<span data-ttu-id="c3671-2578">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2578">2</span></span><br/> <span data-ttu-id="c3671-2579">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2579">0</span></span><br/>

<span data-ttu-id="c3671-2580">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2580">1</span></span>

<span data-ttu-id="c3671-2581">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2581">2</span></span>

<span data-ttu-id="c3671-2582">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2582">3</span></span>

<span data-ttu-id="c3671-2583">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2583">4</span></span>

<span data-ttu-id="c3671-2584">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2584">5</span></span>

<span data-ttu-id="c3671-2585">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2585">6</span></span>

<span data-ttu-id="c3671-2586">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2586">7</span></span>

<span data-ttu-id="c3671-2587">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2587">8</span></span>

<span data-ttu-id="c3671-2588">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2588">9</span></span>

<span data-ttu-id="c3671-2589">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2589">3</span></span><br/> <span data-ttu-id="c3671-2590">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2590">0</span></span><br/>

<span data-ttu-id="c3671-2591">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2591">1</span></span>

<span data-ttu-id="c3671-2592">dwType</span><span class="sxs-lookup"><span data-stu-id="c3671-2592">dwType</span></span>

<span data-ttu-id="c3671-2593">rgb (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-2593">rgb (variable)</span></span>



 

<span data-ttu-id="c3671-2594">**dwType:** Einer der in Abschnitt 2.2.1.1 definierten Variantentypen, der mit Variant-Typmodifizierern kombiniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c3671-2594">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="c3671-2595">Für alle Variantentypen, mit Ausnahme der mit VT ARRAY kombinierten \_ Typen, weist SERIALIZEDPROPERTYVALUE das gleiche Layout wie CBaseStorageVariant auf, wie in Abschnitt 2.2.1.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-2595">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="c3671-2596">Wenn der Variant-Typ mit dem VT \_ ARRAY-Typmodifizierer kombiniert wird, wird SAFEARRAY2 gemäß Abschnitt 2.2.1.2.1.1 anstelle von SAFEARRAY im vValue-Feld von CBaseStorageVariant verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3671-2596">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="c3671-2597">**rgb:** Serialisierter Wert.</span><span class="sxs-lookup"><span data-stu-id="c3671-2597">**rgb**: Serialized value.</span></span> <span data-ttu-id="c3671-2598">Weitere Informationen finden Sie unter Serialisierung für vValue in 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="c3671-2598">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="c3671-2599">2.2.2 Nachrichtenheader</span><span class="sxs-lookup"><span data-stu-id="c3671-2599">2.2.2 Message Headers</span></span>

<span data-ttu-id="c3671-2600">Alle Content Indexing Service Protocol-Nachrichten verfügen über einen 16-Byte-Header.</span><span class="sxs-lookup"><span data-stu-id="c3671-2600">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="c3671-2601">Unten sehen Sie ein Diagramm, das das Nachrichtenheaderformat des Content Indexing Service Protocol zeigt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2601">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="c3671-2602">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2602">0</span></span>

<span data-ttu-id="c3671-2603">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2603">1</span></span>

<span data-ttu-id="c3671-2604">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2604">2</span></span>

<span data-ttu-id="c3671-2605">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2605">3</span></span>

<span data-ttu-id="c3671-2606">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2606">4</span></span>

<span data-ttu-id="c3671-2607">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2607">5</span></span>

<span data-ttu-id="c3671-2608">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2608">6</span></span>

<span data-ttu-id="c3671-2609">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2609">7</span></span>

<span data-ttu-id="c3671-2610">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2610">8</span></span>

<span data-ttu-id="c3671-2611">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2611">9</span></span>

<span data-ttu-id="c3671-2612">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2612">1</span></span><br/> <span data-ttu-id="c3671-2613">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2613">0</span></span><br/>

<span data-ttu-id="c3671-2614">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2614">1</span></span>

<span data-ttu-id="c3671-2615">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2615">2</span></span>

<span data-ttu-id="c3671-2616">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2616">3</span></span>

<span data-ttu-id="c3671-2617">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2617">4</span></span>

<span data-ttu-id="c3671-2618">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2618">5</span></span>

<span data-ttu-id="c3671-2619">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2619">6</span></span>

<span data-ttu-id="c3671-2620">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2620">7</span></span>

<span data-ttu-id="c3671-2621">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2621">8</span></span>

<span data-ttu-id="c3671-2622">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2622">9</span></span>

<span data-ttu-id="c3671-2623">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2623">2</span></span><br/> <span data-ttu-id="c3671-2624">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2624">0</span></span><br/>

<span data-ttu-id="c3671-2625">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2625">1</span></span>

<span data-ttu-id="c3671-2626">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2626">2</span></span>

<span data-ttu-id="c3671-2627">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2627">3</span></span>

<span data-ttu-id="c3671-2628">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2628">4</span></span>

<span data-ttu-id="c3671-2629">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2629">5</span></span>

<span data-ttu-id="c3671-2630">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2630">6</span></span>

<span data-ttu-id="c3671-2631">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2631">7</span></span>

<span data-ttu-id="c3671-2632">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2632">8</span></span>

<span data-ttu-id="c3671-2633">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2633">9</span></span>

<span data-ttu-id="c3671-2634">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2634">3</span></span><br/> <span data-ttu-id="c3671-2635">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2635">0</span></span><br/>

<span data-ttu-id="c3671-2636">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2636">1</span></span>

<span data-ttu-id="c3671-2637">\_mldg</span><span class="sxs-lookup"><span data-stu-id="c3671-2637">\_msg</span></span>

<span data-ttu-id="c3671-2638">\_Status</span><span class="sxs-lookup"><span data-stu-id="c3671-2638">\_status</span></span>

<span data-ttu-id="c3671-2639">\_ulChecksum</span><span class="sxs-lookup"><span data-stu-id="c3671-2639">\_ulChecksum</span></span>

<span data-ttu-id="c3671-2640">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="c3671-2640">\_ulReserved2</span></span>



 

<span data-ttu-id="c3671-2641">\_**msg:** Eine 32-Bit-Ganzzahl, die den Typ der Nachricht nach dem Header angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2641">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="c3671-2642">In der folgenden Tabelle sind die Meldungen des Content Indexing Service-Protokolls und die für jede Nachricht angegebenen ganzzahligen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2642">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="c3671-2643">Wie in der Tabelle gezeigt, identifizieren einige Werte zwei Meldungen in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c3671-2643">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="c3671-2644">In diesen Fällen kann die Nachricht, die auf den Header folgt, durch die Richtung des Nachrichtenflusses identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2644">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="c3671-2645">Wenn die Richtung Client zu Server ist, wird die Meldung mit "In" angegeben, die an den Nachrichtennamen angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-2645">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="c3671-2646">Wenn die Richtung Server zu Client ist, wird die Nachricht mit "Out" angegeben, die an den Nachrichtennamen angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-2646">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="c3671-2647">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-2647">Value</span></span>      | <span data-ttu-id="c3671-2648">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-2648">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="c3671-2649">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="c3671-2649">0x000000C8</span></span> | <span data-ttu-id="c3671-2650">CPMConnectIn oder CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="c3671-2650">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="c3671-2651">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="c3671-2651">0x000000C9</span></span> | <span data-ttu-id="c3671-2652">CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="c3671-2652">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="c3671-2653">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="c3671-2653">0x000000CA</span></span> | <span data-ttu-id="c3671-2654">CPMCreateQueryIn oder CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="c3671-2654">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="c3671-2655">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="c3671-2655">0x000000CB</span></span> | <span data-ttu-id="c3671-2656">CPMFreeCursorIn oder CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="c3671-2656">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="c3671-2657">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="c3671-2657">0x000000CC</span></span> | <span data-ttu-id="c3671-2658">CPMGetRowsIn oder CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="c3671-2658">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="c3671-2659">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="c3671-2659">0x000000CD</span></span> | <span data-ttu-id="c3671-2660">CPMRatioFinishedIn oder CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="c3671-2660">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="c3671-2661">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="c3671-2661">0x000000CE</span></span> | <span data-ttu-id="c3671-2662">CPMCompareBmkIn oder CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="c3671-2662">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="c3671-2663">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="c3671-2663">0x000000CF</span></span> | <span data-ttu-id="c3671-2664">CPMGetApproximatePositionIn oder CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="c3671-2664">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="c3671-2665">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="c3671-2665">0x000000D0</span></span> | <span data-ttu-id="c3671-2666">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="c3671-2666">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="c3671-2667">0x000000D1</span><span class="sxs-lookup"><span data-stu-id="c3671-2667">0x000000D1</span></span> | <span data-ttu-id="c3671-2668">CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="c3671-2668">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="c3671-2669">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="c3671-2669">0x000000D2</span></span> | <span data-ttu-id="c3671-2670">CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="c3671-2670">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="c3671-2671">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="c3671-2671">0x000000D7</span></span> | <span data-ttu-id="c3671-2672">CPMGetQueryStatusIn oder CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="c3671-2672">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="c3671-2673">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="c3671-2673">0x000000D9</span></span> | <span data-ttu-id="c3671-2674">CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="c3671-2674">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="c3671-2675">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="c3671-2675">0x000000E1</span></span> | <span data-ttu-id="c3671-2676">CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="c3671-2676">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="c3671-2677">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="c3671-2677">0x000000E4</span></span> | <span data-ttu-id="c3671-2678">CPMFetchValueIn oder CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="c3671-2678">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="c3671-2679">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="c3671-2679">0x000000E6</span></span> | <span data-ttu-id="c3671-2680">CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="c3671-2680">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="c3671-2681">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="c3671-2681">0x000000E7</span></span> | <span data-ttu-id="c3671-2682">CPMGetQueryStatusExIn oder PMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="c3671-2682">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="c3671-2683">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="c3671-2683">0x000000E8</span></span> | <span data-ttu-id="c3671-2684">CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="c3671-2684">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="c3671-2685">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="c3671-2685">0x000000E9</span></span> | <span data-ttu-id="c3671-2686">CPMStopAsynchIn</span><span class="sxs-lookup"><span data-stu-id="c3671-2686">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="c3671-2687">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="c3671-2687">0x000000EC</span></span> | <span data-ttu-id="c3671-2688">CPMSetCatStateIn oder CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="c3671-2688">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="c3671-2689">\_**status:** Ein HRESULT \[ MS-SYS, \] das den Status des angeforderten Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2689">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="c3671-2690">*Windows-Verhalten: Der Client legt das \_ Statusfeld immer auf 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="c3671-2690">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="c3671-2691">**\_ ulChecksum:** Das ulChecksum MUSS wie in Abschnitt \_ 3.2.4 für die folgenden Meldungen angegeben berechnet werden:</span><span class="sxs-lookup"><span data-stu-id="c3671-2691">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="c3671-2692">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="c3671-2692">CPMConnectIn</span></span>
-   <span data-ttu-id="c3671-2693">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="c3671-2693">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="c3671-2694">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="c3671-2694">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="c3671-2695">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="c3671-2695">CPMGetRowsIn</span></span>
-   <span data-ttu-id="c3671-2696">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="c3671-2696">CPMFetchValueIn</span></span>

<span data-ttu-id="c3671-2697">Für alle anderen Nachrichten MUSS \_ ulChecksum auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3671-2697">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="c3671-2698">Ein Client MUSS das \_ ulChecksum-Feld ignorieren.</span><span class="sxs-lookup"><span data-stu-id="c3671-2698">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="c3671-2699">**\_ ulReserved2:** MUSS auf 0 festgelegt und vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2699">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="c3671-2700">2.2.3 Nachrichten</span><span class="sxs-lookup"><span data-stu-id="c3671-2700">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="c3671-2701">2.2.3.1 CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="c3671-2701">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="c3671-2702">Die CPMCiStateInOut-Nachricht enthält Informationen zum Status des Indizierungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="c3671-2702">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="c3671-2703">Das Format der CPMCiStateInOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-2703">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="c3671-2704">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2704">0</span></span>

<span data-ttu-id="c3671-2705">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2705">1</span></span>

<span data-ttu-id="c3671-2706">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2706">2</span></span>

<span data-ttu-id="c3671-2707">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2707">3</span></span>

<span data-ttu-id="c3671-2708">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2708">4</span></span>

<span data-ttu-id="c3671-2709">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2709">5</span></span>

<span data-ttu-id="c3671-2710">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2710">6</span></span>

<span data-ttu-id="c3671-2711">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2711">7</span></span>

<span data-ttu-id="c3671-2712">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2712">8</span></span>

<span data-ttu-id="c3671-2713">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2713">9</span></span>

<span data-ttu-id="c3671-2714">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2714">1</span></span><br/> <span data-ttu-id="c3671-2715">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2715">0</span></span><br/>

<span data-ttu-id="c3671-2716">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2716">1</span></span>

<span data-ttu-id="c3671-2717">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2717">2</span></span>

<span data-ttu-id="c3671-2718">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2718">3</span></span>

<span data-ttu-id="c3671-2719">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2719">4</span></span>

<span data-ttu-id="c3671-2720">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2720">5</span></span>

<span data-ttu-id="c3671-2721">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2721">6</span></span>

<span data-ttu-id="c3671-2722">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2722">7</span></span>

<span data-ttu-id="c3671-2723">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2723">8</span></span>

<span data-ttu-id="c3671-2724">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2724">9</span></span>

<span data-ttu-id="c3671-2725">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2725">2</span></span><br/> <span data-ttu-id="c3671-2726">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2726">0</span></span><br/>

<span data-ttu-id="c3671-2727">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2727">1</span></span>

<span data-ttu-id="c3671-2728">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2728">2</span></span>

<span data-ttu-id="c3671-2729">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2729">3</span></span>

<span data-ttu-id="c3671-2730">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2730">4</span></span>

<span data-ttu-id="c3671-2731">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2731">5</span></span>

<span data-ttu-id="c3671-2732">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2732">6</span></span>

<span data-ttu-id="c3671-2733">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2733">7</span></span>

<span data-ttu-id="c3671-2734">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2734">8</span></span>

<span data-ttu-id="c3671-2735">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2735">9</span></span>

<span data-ttu-id="c3671-2736">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2736">3</span></span><br/> <span data-ttu-id="c3671-2737">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2737">0</span></span><br/>

<span data-ttu-id="c3671-2738">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2738">1</span></span>

<span data-ttu-id="c3671-2739">cbStruct</span><span class="sxs-lookup"><span data-stu-id="c3671-2739">cbStruct</span></span>

<span data-ttu-id="c3671-2740">cWordList</span><span class="sxs-lookup"><span data-stu-id="c3671-2740">cWordList</span></span>

<span data-ttu-id="c3671-2741">cPersistentIndex</span><span class="sxs-lookup"><span data-stu-id="c3671-2741">cPersistentIndex</span></span>

<span data-ttu-id="c3671-2742">cQueries</span><span class="sxs-lookup"><span data-stu-id="c3671-2742">cQueries</span></span>

<span data-ttu-id="c3671-2743">cDocuments</span><span class="sxs-lookup"><span data-stu-id="c3671-2743">cDocuments</span></span>

<span data-ttu-id="c3671-2744">cFreshTest</span><span class="sxs-lookup"><span data-stu-id="c3671-2744">cFreshTest</span></span>

<span data-ttu-id="c3671-2745">dwMergeProgress</span><span class="sxs-lookup"><span data-stu-id="c3671-2745">dwMergeProgress</span></span>

<span data-ttu-id="c3671-2746">Estate</span><span class="sxs-lookup"><span data-stu-id="c3671-2746">eState</span></span>

<span data-ttu-id="c3671-2747">cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="c3671-2747">cFilteredDocuments</span></span>

<span data-ttu-id="c3671-2748">cTotalDocuments</span><span class="sxs-lookup"><span data-stu-id="c3671-2748">cTotalDocuments</span></span>

<span data-ttu-id="c3671-2749">cPendingScans</span><span class="sxs-lookup"><span data-stu-id="c3671-2749">cPendingScans</span></span>

<span data-ttu-id="c3671-2750">dwIndexSize</span><span class="sxs-lookup"><span data-stu-id="c3671-2750">dwIndexSize</span></span>

<span data-ttu-id="c3671-2751">cUniqueKeys</span><span class="sxs-lookup"><span data-stu-id="c3671-2751">cUniqueKeys</span></span>

<span data-ttu-id="c3671-2752">cSecQDocuments</span><span class="sxs-lookup"><span data-stu-id="c3671-2752">cSecQDocuments</span></span>

<span data-ttu-id="c3671-2753">dwPropCacheSize</span><span class="sxs-lookup"><span data-stu-id="c3671-2753">dwPropCacheSize</span></span>



 

<span data-ttu-id="c3671-2754">**cbStruct:** Eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2754">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="c3671-2755">Die Größe dieser Nachricht in Bytes (mit Ausnahme des allgemeinen Headers).</span><span class="sxs-lookup"><span data-stu-id="c3671-2755">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="c3671-2756">MUSS auf 0x0000003C festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2756">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="c3671-2757">**cWordList:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der anfänglichen Indizes angibt, die für kürzlich indizierte Dokumente erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2757">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="c3671-2758">**cPersistentIndex:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl persistenter Indizes angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2758">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="c3671-2759">**cQueries:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die eine Anzahl aktiv ausgeführter Abfragen angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2759">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="c3671-2760">**cDocuments:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Dokumente angibt, die auf die Indizierung warten.</span><span class="sxs-lookup"><span data-stu-id="c3671-2760">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="c3671-2761">**cFreshTest:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl eindeutiger Dokumente mit Informationen in Indizes angibt, die nicht vollständig leistungsoptimiert sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-2761">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="c3671-2762">**dwMergeProgress:** 32-Bit-Ganzzahl ohne Vorzeichen, die den Abschlussprozentsatz der aktuellen vollständigen Optimierung von Indizes angibt, wenn die Optimierung gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-2762">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="c3671-2763">MUSS kleiner oder gleich 100 sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-2763">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="c3671-2764">**eState:** Status der Inhaltsindizierung, wie von einer oder mehreren CI \_ \_ \* STATE-Konstanten angegeben, die in der folgenden Tabelle definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-2764">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="c3671-2765">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-2765">Value</span></span>                                         | <span data-ttu-id="c3671-2766">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-2766">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-2767">CI \_ STATE SHADOW MERGE \_ \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-2767">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="c3671-2768">Der Indizierungsdienst optimiert derzeit einige indizes, um die Speicherauslastung zu reduzieren und die Abfrageleistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="c3671-2768">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="c3671-2769">CI \_ STATE MASTER MERGE \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-2769">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="c3671-2770">Der Indizierungsdienst wird derzeit für alle Indizes vollständig optimiert.</span><span class="sxs-lookup"><span data-stu-id="c3671-2770">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c3671-2771">CI \_ STATE CONTENT SCAN REQUIRED \_ \_ \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3671-2771">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="c3671-2772">Einige Dokumente im Index wurden geändert, und der Indizierungsdienst muss bestimmen, welche hinzugefügt, geändert oder gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2772">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c3671-2773">CI \_ STATE \_ ANNEALING \_ MERGE 0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3671-2773">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="c3671-2774">Der Indizierungsdienst optimiert derzeit Indizes, um die Speicherauslastung zu reduzieren und die Abfrageleistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="c3671-2774">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="c3671-2775">Dieser Prozess ist umfassender als der durch den CI STATE SHADOW MERGE-Wert identifizierte \_ \_ \_ Prozess, ist jedoch nicht so umfassend wie durch den CI \_ STATE MASTER \_ \_ MERGE-Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-2775">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="c3671-2776">Solche Optimierungen sind implementierungsspezifisch, da sie davon abhängen, wie Daten intern gespeichert werden. Die Optimierungen wirken sich nur auf die Antwortzeit auf das Protokoll aus.</span><span class="sxs-lookup"><span data-stu-id="c3671-2776">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="c3671-2777">\_CI STATE SCANNING \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3671-2777">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="c3671-2778">Der Indizierungsdienst untersucht ein Verzeichnis oder eine Gruppe von Verzeichnissen, um festzustellen, ob Dateien seit dem letzten Indizieren des Verzeichnisses hinzugefügt, gelöscht oder aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2778">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c3671-2779">CI \_ STATE \_ RECOVERING 0x00000020</span><span class="sxs-lookup"><span data-stu-id="c3671-2779">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="c3671-2780">Der Dienst beginnt mit dem letzten gespeicherten Zustand und wird gerade wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2780">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c3671-2781">CI \_ STATE LOW MEMORY \_ \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="c3671-2781">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="c3671-2782">Der größte Teil des virtuellen Arbeitsspeichers des Servers wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3671-2782">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="c3671-2783">CI \_ STATE HIGH IO \_ \_ 0x00000100</span><span class="sxs-lookup"><span data-stu-id="c3671-2783">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="c3671-2784">Die E/A-Aktivität (Input/Output) auf dem Server ist relativ hoch.</span><span class="sxs-lookup"><span data-stu-id="c3671-2784">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="c3671-2785">CI \_ STATE MASTER MERGE \_ \_ \_ PAUSED 0x00000200</span><span class="sxs-lookup"><span data-stu-id="c3671-2785">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="c3671-2786">Der Prozess der vollständigen Optimierung für alle Indizes, die gerade ausgeführt wurden, wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="c3671-2786">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="c3671-2787">Dies dient nur zu Informationszwecken und wirkt sich nicht auf CISP aus.</span><span class="sxs-lookup"><span data-stu-id="c3671-2787">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c3671-2788">CI \_ STATE READ ONLY \_ \_ 0x00000400</span><span class="sxs-lookup"><span data-stu-id="c3671-2788">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="c3671-2789">Der Teil des Indizierungsdiensts, der neue zu indizierende Dokumente aufnimmt, wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="c3671-2789">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="c3671-2790">Dies dient nur zu Informationszwecken und wirkt sich nicht auf CISP aus.</span><span class="sxs-lookup"><span data-stu-id="c3671-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="c3671-2791">CI \_ STATE BATTERY POWER \_ \_ 0x00000800</span><span class="sxs-lookup"><span data-stu-id="c3671-2791">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="c3671-2792">Der Teil des Indizierungsdiensts, der neue zu indizierende Dokumente aufnimmt, wurde angehalten, um die Akkulebensdauer zu sparen, antwortet aber weiterhin auf die Abfragen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2792">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="c3671-2793">Dies dient nur zu Informationszwecken und wirkt sich nicht auf CISP aus.</span><span class="sxs-lookup"><span data-stu-id="c3671-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c3671-2794">CI \_ STATE USER ACTIVE \_ \_ 0x00001000</span><span class="sxs-lookup"><span data-stu-id="c3671-2794">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="c3671-2795">Der Teil des Indizierungsdiensts, der neue zu indizierende Dokumente aufnimmt, wurde aufgrund einer hohen Aktivität durch den Benutzer (Tastatur oder Maus) angehalten, antwortet aber weiterhin auf die Abfragen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2795">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="c3671-2796">Dies dient nur zu Informationszwecken und wirkt sich nicht auf CISP aus.</span><span class="sxs-lookup"><span data-stu-id="c3671-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="c3671-2797">CI \_ STATE \_ STARTING 0x00002000</span><span class="sxs-lookup"><span data-stu-id="c3671-2797">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="c3671-2798">Der Dienst wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="c3671-2798">The service is starting.</span></span> <span data-ttu-id="c3671-2799">Abfragen können ausgeführt werden, aber die Überprüfung und Benachrichtigung wurden noch nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c3671-2799">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="c3671-2800">Dies dient nur zu Informationszwecken und wirkt sich nicht auf CISP aus.</span><span class="sxs-lookup"><span data-stu-id="c3671-2800">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c3671-2801">CI \_ STATE \_ READING \_ USNS 0x00004000</span><span class="sxs-lookup"><span data-stu-id="c3671-2801">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="c3671-2802">Der Dienst hat das vom Dateisystem gespeicherte Protokoll nicht gelesen, um Änderungen an Dateien oder Verzeichnissen auf einem Volume nachzuverfolgen, sodass der Index möglicherweise nicht auf dem neuesten Stand ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-2802">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="c3671-2803">**cFilteredDocuments:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Seit Beginn der Inhaltsindizierung indizierten Dokumente angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2803">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="c3671-2804">**cTotalDocuments:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Dokumente im System angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2804">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="c3671-2805">**cPendingScans:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl ausstehender Indizierungsvorgänge auf hoher Ebene angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2805">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="c3671-2806">Die Bedeutung dieses Werts ist anbieterspezifisch, aber es wird erwartet, dass größere Zahlen darauf hindeuten, dass mehr Indizierung verbleibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2806">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="c3671-2807">*Windows-Verhalten:* Dieser Wert ist in der Regel 0 (null), es sei denn, er liegt unmittelbar nach dem Starten der Indizierung oder nach einem Benachrichtigungswarteschlangenüberlauf vor.</span><span class="sxs-lookup"><span data-stu-id="c3671-2807">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="c3671-2808">**dwIndexSize:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des Indexes (mit Ausnahme des Eigenschaftencaches) in Megabyte angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2808">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="c3671-2809">**cUniqueKeys:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die ungefähre Anzahl eindeutiger Schlüssel im Katalog angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2809">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="c3671-2810">**cSecQDocuments:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dokumente angibt, die der Indizierungsdienst aufgrund eines Fehlers während des ersten Indizierungsversuchs erneut indiziert.</span><span class="sxs-lookup"><span data-stu-id="c3671-2810">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="c3671-2811">**dwPropCacheSize:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des Eigenschaftencaches in Megabyte angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2811">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="c3671-2812">2.2.3.2 CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="c3671-2812">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="c3671-2813">Die CPMSetCatStateIn-Nachricht legt den Status eines Katalogs fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-2813">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="c3671-2814">Das Format der CPMSetCatStateIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-2814">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="c3671-2815">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2815">0</span></span>

<span data-ttu-id="c3671-2816">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2816">1</span></span>

<span data-ttu-id="c3671-2817">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2817">2</span></span>

<span data-ttu-id="c3671-2818">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2818">3</span></span>

<span data-ttu-id="c3671-2819">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2819">4</span></span>

<span data-ttu-id="c3671-2820">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2820">5</span></span>

<span data-ttu-id="c3671-2821">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2821">6</span></span>

<span data-ttu-id="c3671-2822">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2822">7</span></span>

<span data-ttu-id="c3671-2823">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2823">8</span></span>

<span data-ttu-id="c3671-2824">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2824">9</span></span>

<span data-ttu-id="c3671-2825">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2825">1</span></span><br/> <span data-ttu-id="c3671-2826">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2826">0</span></span><br/>

<span data-ttu-id="c3671-2827">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2827">1</span></span>

<span data-ttu-id="c3671-2828">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2828">2</span></span>

<span data-ttu-id="c3671-2829">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2829">3</span></span>

<span data-ttu-id="c3671-2830">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2830">4</span></span>

<span data-ttu-id="c3671-2831">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2831">5</span></span>

<span data-ttu-id="c3671-2832">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2832">6</span></span>

<span data-ttu-id="c3671-2833">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2833">7</span></span>

<span data-ttu-id="c3671-2834">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2834">8</span></span>

<span data-ttu-id="c3671-2835">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2835">9</span></span>

<span data-ttu-id="c3671-2836">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2836">2</span></span><br/> <span data-ttu-id="c3671-2837">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2837">0</span></span><br/>

<span data-ttu-id="c3671-2838">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2838">1</span></span>

<span data-ttu-id="c3671-2839">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2839">2</span></span>

<span data-ttu-id="c3671-2840">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2840">3</span></span>

<span data-ttu-id="c3671-2841">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2841">4</span></span>

<span data-ttu-id="c3671-2842">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2842">5</span></span>

<span data-ttu-id="c3671-2843">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2843">6</span></span>

<span data-ttu-id="c3671-2844">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2844">7</span></span>

<span data-ttu-id="c3671-2845">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2845">8</span></span>

<span data-ttu-id="c3671-2846">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2846">9</span></span>

<span data-ttu-id="c3671-2847">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2847">3</span></span><br/> <span data-ttu-id="c3671-2848">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2848">0</span></span><br/>

<span data-ttu-id="c3671-2849">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2849">1</span></span>

<span data-ttu-id="c3671-2850">\_partID</span><span class="sxs-lookup"><span data-stu-id="c3671-2850">\_partID</span></span>

<span data-ttu-id="c3671-2851">\_dwNewState</span><span class="sxs-lookup"><span data-stu-id="c3671-2851">\_dwNewState</span></span>

<span data-ttu-id="c3671-2852">\_CatName (Variable, optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-2852">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="c3671-2853">**\_ partID:** MUSS auf 0x00000001 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2853">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="c3671-2854">**\_ dwNewState:** MUSS auf einen der folgenden Werte festgelegt werden, der den neuen Status des Katalogs angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2854">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="c3671-2855">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-2855">Value</span></span>                         | <span data-ttu-id="c3671-2856">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-2856">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-2857">CICAT \_ STOPPED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-2857">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="c3671-2858">Der Katalog wird beendet.</span><span class="sxs-lookup"><span data-stu-id="c3671-2858">The catalog is stopped.</span></span> <span data-ttu-id="c3671-2859">Dieser Zustand bedeutet, dass keine neuen Dateien indiziert und keine Suchabfragen verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-2859">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="c3671-2860">CICAT \_ READONLY-0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-2860">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="c3671-2861">Der Katalog ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2861">The catalog is read-only.</span></span> <span data-ttu-id="c3671-2862">Es sollen keine neuen Dateien indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2862">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="c3671-2863">CICAT \_ WRITABLE-0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3671-2863">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="c3671-2864">Der Katalog kann geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2864">The catalog is writable.</span></span> <span data-ttu-id="c3671-2865">Neue Dateien können indiziert werden, und Suchabfragen müssen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2865">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="c3671-2866">CICAT \_ NO \_ QUERY 0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3671-2866">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="c3671-2867">Der Katalog ist nicht für Abfragen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c3671-2867">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="c3671-2868">CICAT \_ GET \_ STATE 0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3671-2868">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="c3671-2869">Der Status des Katalogs soll nicht geändert, sondern nur abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2869">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="c3671-2870">CICAT \_ ALL \_ OPENED 0x00000020</span><span class="sxs-lookup"><span data-stu-id="c3671-2870">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="c3671-2871">Eine Überprüfung, um festzustellen, ob alle Kataloge gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2871">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="c3671-2872">Wenn ja, wird das \_ feld dwOldState, das in der CPMSetCatStateOut-Antwort an diese Nachricht gesendet wird, als ungleich 0 (null) gemeldet.</span><span class="sxs-lookup"><span data-stu-id="c3671-2872">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="c3671-2873">**\_ CatName:** Der Name des Katalogs, dessen Status geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-2873">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="c3671-2874">Der Name MUSS eine auf NULL endende Unicode-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-2874">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="c3671-2875">Dieses Feld MUSS weggelassen werden, wenn \_ dwNewState auf CICAT ALL OPENED festgelegt \_ \_ ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-2875">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="c3671-2876">2.2.3.3 CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="c3671-2876">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="c3671-2877">Die CPMSetCatStateOut-Nachricht ist eine Antwort auf eine CPMSetCatStateIn-Nachricht mit dem alten Status des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="c3671-2877">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="c3671-2878">Das Format der CPMSetCatStateOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-2878">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="c3671-2879">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2879">0</span></span>

<span data-ttu-id="c3671-2880">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2880">1</span></span>

<span data-ttu-id="c3671-2881">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2881">2</span></span>

<span data-ttu-id="c3671-2882">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2882">3</span></span>

<span data-ttu-id="c3671-2883">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2883">4</span></span>

<span data-ttu-id="c3671-2884">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2884">5</span></span>

<span data-ttu-id="c3671-2885">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2885">6</span></span>

<span data-ttu-id="c3671-2886">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2886">7</span></span>

<span data-ttu-id="c3671-2887">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2887">8</span></span>

<span data-ttu-id="c3671-2888">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2888">9</span></span>

<span data-ttu-id="c3671-2889">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2889">1</span></span><br/> <span data-ttu-id="c3671-2890">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2890">0</span></span><br/>

<span data-ttu-id="c3671-2891">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2891">1</span></span>

<span data-ttu-id="c3671-2892">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2892">2</span></span>

<span data-ttu-id="c3671-2893">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2893">3</span></span>

<span data-ttu-id="c3671-2894">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2894">4</span></span>

<span data-ttu-id="c3671-2895">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2895">5</span></span>

<span data-ttu-id="c3671-2896">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2896">6</span></span>

<span data-ttu-id="c3671-2897">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2897">7</span></span>

<span data-ttu-id="c3671-2898">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2898">8</span></span>

<span data-ttu-id="c3671-2899">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2899">9</span></span>

<span data-ttu-id="c3671-2900">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2900">2</span></span><br/> <span data-ttu-id="c3671-2901">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2901">0</span></span><br/>

<span data-ttu-id="c3671-2902">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2902">1</span></span>

<span data-ttu-id="c3671-2903">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2903">2</span></span>

<span data-ttu-id="c3671-2904">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2904">3</span></span>

<span data-ttu-id="c3671-2905">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2905">4</span></span>

<span data-ttu-id="c3671-2906">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2906">5</span></span>

<span data-ttu-id="c3671-2907">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2907">6</span></span>

<span data-ttu-id="c3671-2908">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2908">7</span></span>

<span data-ttu-id="c3671-2909">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2909">8</span></span>

<span data-ttu-id="c3671-2910">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2910">9</span></span>

<span data-ttu-id="c3671-2911">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2911">3</span></span><br/> <span data-ttu-id="c3671-2912">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2912">0</span></span><br/>

<span data-ttu-id="c3671-2913">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2913">1</span></span>

<span data-ttu-id="c3671-2914">\_dwOldState</span><span class="sxs-lookup"><span data-stu-id="c3671-2914">\_dwOldState</span></span>



 

<span data-ttu-id="c3671-2915">**\_ dwOldState:** Einer der folgenden Werte, der den alten Status des Katalogs angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2915">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="c3671-2916">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-2916">Value</span></span>                       | <span data-ttu-id="c3671-2917">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-2917">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="c3671-2918">CICAT \_ STOPPED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-2918">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="c3671-2919">Der Katalog wird beendet.</span><span class="sxs-lookup"><span data-stu-id="c3671-2919">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="c3671-2920">CICAT \_ READONLY-0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-2920">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="c3671-2921">Der Katalog ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2921">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="c3671-2922">CICAT \_ WRITABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3671-2922">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="c3671-2923">Der Katalog ist schreibbar.</span><span class="sxs-lookup"><span data-stu-id="c3671-2923">The catalog is writable.</span></span>                   |
| <span data-ttu-id="c3671-2924">CICAT \_ NO \_ QUERY 0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3671-2924">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="c3671-2925">Der Katalog ist nicht für Abfragen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c3671-2925">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="c3671-2926">2.2.3.4 CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="c3671-2926">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="c3671-2927">Die CPMUpdateDocumentsIn-Nachricht weist den Server an, den angegebenen Pfad zu indiziert.</span><span class="sxs-lookup"><span data-stu-id="c3671-2927">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="c3671-2928">Der Server antwortet mit dem Nachrichtenheader der CPMUpdateDocumentsOut-Nachricht, wobei die Ergebnisse der Anforderung im \_ Statusfeld des Nachrichtenheaders enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-2928">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="c3671-2929">Das Format der CPMUpdateDocumentsIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-2929">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="c3671-2930">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2930">0</span></span>

<span data-ttu-id="c3671-2931">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2931">1</span></span>

<span data-ttu-id="c3671-2932">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2932">2</span></span>

<span data-ttu-id="c3671-2933">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2933">3</span></span>

<span data-ttu-id="c3671-2934">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2934">4</span></span>

<span data-ttu-id="c3671-2935">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2935">5</span></span>

<span data-ttu-id="c3671-2936">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2936">6</span></span>

<span data-ttu-id="c3671-2937">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2937">7</span></span>

<span data-ttu-id="c3671-2938">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2938">8</span></span>

<span data-ttu-id="c3671-2939">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2939">9</span></span>

<span data-ttu-id="c3671-2940">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2940">1</span></span><br/> <span data-ttu-id="c3671-2941">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2941">0</span></span><br/>

<span data-ttu-id="c3671-2942">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2942">1</span></span>

<span data-ttu-id="c3671-2943">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2943">2</span></span>

<span data-ttu-id="c3671-2944">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2944">3</span></span>

<span data-ttu-id="c3671-2945">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2945">4</span></span>

<span data-ttu-id="c3671-2946">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2946">5</span></span>

<span data-ttu-id="c3671-2947">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2947">6</span></span>

<span data-ttu-id="c3671-2948">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2948">7</span></span>

<span data-ttu-id="c3671-2949">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2949">8</span></span>

<span data-ttu-id="c3671-2950">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2950">9</span></span>

<span data-ttu-id="c3671-2951">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2951">2</span></span><br/> <span data-ttu-id="c3671-2952">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2952">0</span></span><br/>

<span data-ttu-id="c3671-2953">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2953">1</span></span>

<span data-ttu-id="c3671-2954">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2954">2</span></span>

<span data-ttu-id="c3671-2955">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2955">3</span></span>

<span data-ttu-id="c3671-2956">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2956">4</span></span>

<span data-ttu-id="c3671-2957">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2957">5</span></span>

<span data-ttu-id="c3671-2958">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2958">6</span></span>

<span data-ttu-id="c3671-2959">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2959">7</span></span>

<span data-ttu-id="c3671-2960">8</span><span class="sxs-lookup"><span data-stu-id="c3671-2960">8</span></span>

<span data-ttu-id="c3671-2961">9</span><span class="sxs-lookup"><span data-stu-id="c3671-2961">9</span></span>

<span data-ttu-id="c3671-2962">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2962">3</span></span><br/> <span data-ttu-id="c3671-2963">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2963">0</span></span><br/>

<span data-ttu-id="c3671-2964">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2964">1</span></span>

<span data-ttu-id="c3671-2965">\_Flag (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-2965">\_flag (optional)</span></span>

<span data-ttu-id="c3671-2966">\_fRootPath (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-2966">\_fRootPath (optional)</span></span>

<span data-ttu-id="c3671-2967">RootPath (Variable, optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-2967">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="c3671-2968">**\_ flag:** Der Typ des auszuführenden Updates.</span><span class="sxs-lookup"><span data-stu-id="c3671-2968">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="c3671-2969">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-2969">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="c3671-2970">Dieses Feld MUSS auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c3671-2970">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="c3671-2971">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-2971">Value</span></span>                  | <span data-ttu-id="c3671-2972">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-2972">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c3671-2973">UPD \_ INCREM 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-2973">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="c3671-2974">Ein inkrementelles Update muss ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2974">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="c3671-2975">UPD \_ FULL 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-2975">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="c3671-2976">Ein vollständiges Update muss ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2976">A full update is to be performed.</span></span>         |
| <span data-ttu-id="c3671-2977">UPD \_ INIT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-2977">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="c3671-2978">Eine neue Initialisierung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3671-2978">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="c3671-2979">**\_ fRootPath:** Ein boolescher Wert, der angibt, ob das RootPath-Feld einen Pfad angibt, unter dem das Update ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-2979">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="c3671-2980">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-2980">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="c3671-2981">Dieses Feld MUSS auf 0x00000001 oder 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2981">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="c3671-2982">Wenn 0x00000001 festgelegt ist, ist ein Pfad, auf dem das Update ausgeführt werden soll, in RootPath enthalten.</span><span class="sxs-lookup"><span data-stu-id="c3671-2982">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="c3671-2983">Wenn 0x00000000 festgelegt ist, muss das Update für alle indizierten Pfade ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-2983">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="c3671-2984">**RootPath:** Der Name des pfads, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-2984">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="c3671-2985">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-2985">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="c3671-2986">Der Name MUSS eine auf NULL endende Unicode-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-2986">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="c3671-2987">Dieses Feld MUSS weggelassen werden, wenn \_ fRootPath auf 0x00000000 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-2987">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="c3671-2988">2.2.3.5 CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="c3671-2988">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="c3671-2989">Die CPMForceMergeIn-Nachricht fordert einen Server zur Durchführung von Wartungsarbeiten an, die zur Verbesserung der Abfrageleistung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-2989">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="c3671-2990">Der Server antworte mit dem Nachrichtenheader der CPMForceMergeIn-Nachricht, wobei die Ergebnisse der Anforderung im Statusfeld enthalten \_ sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-2990">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="c3671-2991">Das Format der CPMForceMergeIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-2991">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="c3671-2992">0</span><span class="sxs-lookup"><span data-stu-id="c3671-2992">0</span></span>

<span data-ttu-id="c3671-2993">1</span><span class="sxs-lookup"><span data-stu-id="c3671-2993">1</span></span>

<span data-ttu-id="c3671-2994">2</span><span class="sxs-lookup"><span data-stu-id="c3671-2994">2</span></span>

<span data-ttu-id="c3671-2995">3</span><span class="sxs-lookup"><span data-stu-id="c3671-2995">3</span></span>

<span data-ttu-id="c3671-2996">4</span><span class="sxs-lookup"><span data-stu-id="c3671-2996">4</span></span>

<span data-ttu-id="c3671-2997">5</span><span class="sxs-lookup"><span data-stu-id="c3671-2997">5</span></span>

<span data-ttu-id="c3671-2998">6</span><span class="sxs-lookup"><span data-stu-id="c3671-2998">6</span></span>

<span data-ttu-id="c3671-2999">7</span><span class="sxs-lookup"><span data-stu-id="c3671-2999">7</span></span>

<span data-ttu-id="c3671-3000">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3000">8</span></span>

<span data-ttu-id="c3671-3001">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3001">9</span></span>

<span data-ttu-id="c3671-3002">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3002">1</span></span><br/> <span data-ttu-id="c3671-3003">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3003">0</span></span><br/>

<span data-ttu-id="c3671-3004">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3004">1</span></span>

<span data-ttu-id="c3671-3005">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3005">2</span></span>

<span data-ttu-id="c3671-3006">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3006">3</span></span>

<span data-ttu-id="c3671-3007">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3007">4</span></span>

<span data-ttu-id="c3671-3008">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3008">5</span></span>

<span data-ttu-id="c3671-3009">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3009">6</span></span>

<span data-ttu-id="c3671-3010">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3010">7</span></span>

<span data-ttu-id="c3671-3011">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3011">8</span></span>

<span data-ttu-id="c3671-3012">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3012">9</span></span>

<span data-ttu-id="c3671-3013">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3013">2</span></span><br/> <span data-ttu-id="c3671-3014">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3014">0</span></span><br/>

<span data-ttu-id="c3671-3015">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3015">1</span></span>

<span data-ttu-id="c3671-3016">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3016">2</span></span>

<span data-ttu-id="c3671-3017">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3017">3</span></span>

<span data-ttu-id="c3671-3018">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3018">4</span></span>

<span data-ttu-id="c3671-3019">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3019">5</span></span>

<span data-ttu-id="c3671-3020">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3020">6</span></span>

<span data-ttu-id="c3671-3021">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3021">7</span></span>

<span data-ttu-id="c3671-3022">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3022">8</span></span>

<span data-ttu-id="c3671-3023">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3023">9</span></span>

<span data-ttu-id="c3671-3024">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3024">3</span></span><br/> <span data-ttu-id="c3671-3025">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3025">0</span></span><br/>

<span data-ttu-id="c3671-3026">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3026">1</span></span>

<span data-ttu-id="c3671-3027">\_partID (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-3027">\_partID (optional)</span></span>



 

<span data-ttu-id="c3671-3028">**\_ partID:** Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-3028">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="c3671-3029">Wenn dieses Feld vorhanden ist, MUSS es auf 0x00000001 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3029">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="c3671-3030">2.2.3.6 CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="c3671-3030">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="c3671-3031">Die CPMConnectIn-Nachricht startet eine Sitzung zwischen Client und Server.</span><span class="sxs-lookup"><span data-stu-id="c3671-3031">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="c3671-3032">Das Format der CPMConnectIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3032">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="c3671-3033">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3033">0</span></span>

<span data-ttu-id="c3671-3034">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3034">1</span></span>

<span data-ttu-id="c3671-3035">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3035">2</span></span>

<span data-ttu-id="c3671-3036">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3036">3</span></span>

<span data-ttu-id="c3671-3037">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3037">4</span></span>

<span data-ttu-id="c3671-3038">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3038">5</span></span>

<span data-ttu-id="c3671-3039">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3039">6</span></span>

<span data-ttu-id="c3671-3040">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3040">7</span></span>

<span data-ttu-id="c3671-3041">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3041">8</span></span>

<span data-ttu-id="c3671-3042">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3042">9</span></span>

<span data-ttu-id="c3671-3043">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3043">1</span></span><br/> <span data-ttu-id="c3671-3044">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3044">0</span></span><br/>

<span data-ttu-id="c3671-3045">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3045">1</span></span>

<span data-ttu-id="c3671-3046">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3046">2</span></span>

<span data-ttu-id="c3671-3047">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3047">3</span></span>

<span data-ttu-id="c3671-3048">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3048">4</span></span>

<span data-ttu-id="c3671-3049">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3049">5</span></span>

<span data-ttu-id="c3671-3050">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3050">6</span></span>

<span data-ttu-id="c3671-3051">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3051">7</span></span>

<span data-ttu-id="c3671-3052">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3052">8</span></span>

<span data-ttu-id="c3671-3053">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3053">9</span></span>

<span data-ttu-id="c3671-3054">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3054">2</span></span><br/> <span data-ttu-id="c3671-3055">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3055">0</span></span><br/>

<span data-ttu-id="c3671-3056">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3056">1</span></span>

<span data-ttu-id="c3671-3057">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3057">2</span></span>

<span data-ttu-id="c3671-3058">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3058">3</span></span>

<span data-ttu-id="c3671-3059">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3059">4</span></span>

<span data-ttu-id="c3671-3060">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3060">5</span></span>

<span data-ttu-id="c3671-3061">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3061">6</span></span>

<span data-ttu-id="c3671-3062">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3062">7</span></span>

<span data-ttu-id="c3671-3063">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3063">8</span></span>

<span data-ttu-id="c3671-3064">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3064">9</span></span>

<span data-ttu-id="c3671-3065">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3065">3</span></span><br/> <span data-ttu-id="c3671-3066">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3066">0</span></span><br/>

<span data-ttu-id="c3671-3067">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3067">1</span></span>

<span data-ttu-id="c3671-3068">\_iClientVersion</span><span class="sxs-lookup"><span data-stu-id="c3671-3068">\_iClientVersion</span></span>

<span data-ttu-id="c3671-3069">\_fClientIsRemote</span><span class="sxs-lookup"><span data-stu-id="c3671-3069">\_fClientIsRemote</span></span>

<span data-ttu-id="c3671-3070">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="c3671-3070">\_cbBlob1</span></span>

<span data-ttu-id="c3671-3071">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="c3671-3071">\_cbBlob2</span></span>

<span data-ttu-id="c3671-3072">\_Polsterung</span><span class="sxs-lookup"><span data-stu-id="c3671-3072">\_padding</span></span>

<span data-ttu-id="c3671-3073">...</span><span class="sxs-lookup"><span data-stu-id="c3671-3073">...</span></span>

<span data-ttu-id="c3671-3074">...</span><span class="sxs-lookup"><span data-stu-id="c3671-3074">...</span></span>

<span data-ttu-id="c3671-3075">MachineName</span><span class="sxs-lookup"><span data-stu-id="c3671-3075">MachineName</span></span>

<span data-ttu-id="c3671-3076">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3076">... (variable)</span></span>

<span data-ttu-id="c3671-3077">UserName (Benutzername)</span><span class="sxs-lookup"><span data-stu-id="c3671-3077">UserName</span></span>

<span data-ttu-id="c3671-3078">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3078">... (variable)</span></span>

<span data-ttu-id="c3671-3079">\_paddingcPropSets (optional, Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3079">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="c3671-3080">cPropSets</span><span class="sxs-lookup"><span data-stu-id="c3671-3080">cPropSets</span></span>

<span data-ttu-id="c3671-3081">PropertySet1 (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3081">PropertySet1 (variable)</span></span>

<span data-ttu-id="c3671-3082">PropertySet2 (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3082">PropertySet2 (variable)</span></span>

<span data-ttu-id="c3671-3083">\_paddingExtPropset (optional, Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3083">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="c3671-3084">cExtPropSet</span><span class="sxs-lookup"><span data-stu-id="c3671-3084">cExtPropSet</span></span>

<span data-ttu-id="c3671-3085">aPropertySets (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3085">aPropertySets (variable)</span></span>



 

<span data-ttu-id="c3671-3086">**\_ iClientVersion:** Eine 32-Bit-Ganzzahl, die angibt, ob der Server den Prüfsummenwert überprüfen soll, der im \_ ulChecksum-Feld der Nachrichtenheader für vom Client gesendete Nachrichten angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-3086">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="c3671-3087">Wenn das \_ Feld iClientVersion auf 0x00000008 oder höher festgelegt ist, MUSS der Server den \_ UlChecksum-Feldwert für die folgenden Meldungen überprüfen:</span><span class="sxs-lookup"><span data-stu-id="c3671-3087">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="c3671-3088">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="c3671-3088">CPMConnectIn</span></span>
-   <span data-ttu-id="c3671-3089">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="c3671-3089">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="c3671-3090">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="c3671-3090">CPMFetchValueIn</span></span>
-   <span data-ttu-id="c3671-3091">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="c3671-3091">CPMGetRowsIn</span></span>
-   <span data-ttu-id="c3671-3092">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="c3671-3092">CPMSetBindingsIn</span></span>

<span data-ttu-id="c3671-3093">Ausführliche Informationen dazu, wie der Server den vom Client im UlChecksum-Feld für die oben aufgeführten Nachrichten angegebenen Wert überprüft, finden Sie in Abschnitt 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="c3671-3093">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="c3671-3094">Wenn der Wert größer als 0x00000008 wird davon ausgegangen, dass der Client 64-Bit-Offsets in CPMGetRowsOut-Nachrichten verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="c3671-3094">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="c3671-3095">Weitere Informationen finden Sie in Abschnitt 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="c3671-3095">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="c3671-3096">*Windows-Verhalten: Auf Windows-Clients wird die iClientVersion wie folgt festgelegt:*</span><span class="sxs-lookup"><span data-stu-id="c3671-3096">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="c3671-3097">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-3097">Value</span></span>      | <span data-ttu-id="c3671-3098">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-3098">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="c3671-3099">0x00000005</span><span class="sxs-lookup"><span data-stu-id="c3671-3099">0x00000005</span></span> | <span data-ttu-id="c3671-3100">Das Clientbetriebssystem ist Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c3671-3100">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="c3671-3101">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3671-3101">0x00000008</span></span> | <span data-ttu-id="c3671-3102">Das Clientbetriebssystem ist entweder 32-Bit-Windows XP oder 32-Bit-Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c3671-3102">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="c3671-3103">0x00010008</span><span class="sxs-lookup"><span data-stu-id="c3671-3103">0x00010008</span></span> | <span data-ttu-id="c3671-3104">Das Clientbetriebssystem ist entweder 64-Bit-Windows XP oder 64-Bit-Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c3671-3104">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="c3671-3105">\_**fClientIsRemote:** Ein boolescher Wert, der angibt, ob der Client auf einem anderen Computer als dem Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-3105">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="c3671-3106">MUSS auf 0x00000001 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3106">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="c3671-3107">\_**cbBlob1:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der Felder cPropSet, PropertySet1 und PropertySet2 in Bytes angibt, kombiniert.</span><span class="sxs-lookup"><span data-stu-id="c3671-3107">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="c3671-3108">\_**cbBlob2:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der Felder cExPropSet und aPropertySet in Bytes angibt, kombiniert.</span><span class="sxs-lookup"><span data-stu-id="c3671-3108">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="c3671-3109">\_**Auffüllung:** 12 Bytes auffüllen, die beliebige Werte enthalten können, und MÜSSEN ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3109">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="c3671-3110">**MachineName:** Der Computername des Clients.</span><span class="sxs-lookup"><span data-stu-id="c3671-3110">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="c3671-3111">Die Namenszeichenfolge MUSS ein nullterminiertes Array mit weniger als 512 Unicode-Zeichen sein, einschließlich des NULL-Abschlusszeichens.</span><span class="sxs-lookup"><span data-stu-id="c3671-3111">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="c3671-3112">**UserName:** Eine Zeichenfolge, die den Benutzernamen der Person darstellt, die die Anwendung ausführt, die dieses Protokoll aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="c3671-3112">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="c3671-3113">Die Namenszeichenfolge MUSS ein mit NULL endendes Array mit weniger als 512 Unicode-Zeichen sein, wenn sie mit MachineName verkettet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-3113">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="c3671-3114">**\_ paddingcPropSets:** Dieses Feld MUSS 0 bis 7 Bytes lang sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-3114">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="c3671-3115">Die Anzahl der Bytes MUSS die Anzahl sein, die erforderlich ist, um den Byteoffset des cPropSets-Felds vom Anfang der Nachricht, die diese Struktur enthält, auf ein Vielfaches von 8 zu setzen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3115">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="c3671-3116">Der Wert der Bytes kann ein beliebiger Wert sein, und MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3116">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3671-3117">**cPropSets:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der CDbPropSet-Strukturen angibt, die diesem Feld folgen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3117">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="c3671-3118">Dieser Wert MUSS auf 0x0000002 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3118">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="c3671-3119">**PropertySet1:** Eine CDbPropSet-Struktur mit guidPropertySet, die DBPROPSET \_ FSCIFRMWRK EXT enthält \_ (siehe Abschnitt 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="c3671-3119">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="c3671-3120">**PropertySet2:** Eine CDbPropSet-Struktur mit guidPropertySet, die DBPROPSET \_ CIFRMWRKCORE EXT enthält \_ (siehe Abschnitt 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="c3671-3120">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="c3671-3121">\_**PaddingExtPropset:** Dieses Feld MUSS 0 bis 7 Bytes lang sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-3121">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="c3671-3122">Die Anzahl der Bytes MUSS die Anzahl sein, die erforderlich ist, um den Byteoffset des Felds cExtPropSets vom Anfang der Nachricht, die diese Struktur enthält, auf ein Vielfaches von 8 zu setzen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3122">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="c3671-3123">Der Wert der Bytes kann ein beliebiger Wert sein, und MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3123">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3671-3124">**cExtPropSet:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der CDbPropSet-Strukturen angibt, die diesem Feld folgen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3124">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="c3671-3125">**aPropertySets:** Ein Array von CDbPropSet-Strukturen, die andere Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-3125">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="c3671-3126">Die Anzahl der Elemente in diesem Array MUSS cExtPropSet entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3126">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="c3671-3127">2.2.3.7 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="c3671-3127">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="c3671-3128">Die CPMConnectOut-Nachricht enthält eine Antwort auf eine CPMConnectIn-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c3671-3128">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="c3671-3129">Das Format der CPMConnectOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3129">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="c3671-3130">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3130">0</span></span>

<span data-ttu-id="c3671-3131">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3131">1</span></span>

<span data-ttu-id="c3671-3132">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3132">2</span></span>

<span data-ttu-id="c3671-3133">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3133">3</span></span>

<span data-ttu-id="c3671-3134">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3134">4</span></span>

<span data-ttu-id="c3671-3135">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3135">5</span></span>

<span data-ttu-id="c3671-3136">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3136">6</span></span>

<span data-ttu-id="c3671-3137">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3137">7</span></span>

<span data-ttu-id="c3671-3138">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3138">8</span></span>

<span data-ttu-id="c3671-3139">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3139">9</span></span>

<span data-ttu-id="c3671-3140">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3140">1</span></span><br/> <span data-ttu-id="c3671-3141">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3141">0</span></span><br/>

<span data-ttu-id="c3671-3142">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3142">1</span></span>

<span data-ttu-id="c3671-3143">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3143">2</span></span>

<span data-ttu-id="c3671-3144">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3144">3</span></span>

<span data-ttu-id="c3671-3145">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3145">4</span></span>

<span data-ttu-id="c3671-3146">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3146">5</span></span>

<span data-ttu-id="c3671-3147">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3147">6</span></span>

<span data-ttu-id="c3671-3148">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3148">7</span></span>

<span data-ttu-id="c3671-3149">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3149">8</span></span>

<span data-ttu-id="c3671-3150">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3150">9</span></span>

<span data-ttu-id="c3671-3151">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3151">2</span></span><br/> <span data-ttu-id="c3671-3152">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3152">0</span></span><br/>

<span data-ttu-id="c3671-3153">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3153">1</span></span>

<span data-ttu-id="c3671-3154">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3154">2</span></span>

<span data-ttu-id="c3671-3155">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3155">3</span></span>

<span data-ttu-id="c3671-3156">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3156">4</span></span>

<span data-ttu-id="c3671-3157">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3157">5</span></span>

<span data-ttu-id="c3671-3158">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3158">6</span></span>

<span data-ttu-id="c3671-3159">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3159">7</span></span>

<span data-ttu-id="c3671-3160">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3160">8</span></span>

<span data-ttu-id="c3671-3161">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3161">9</span></span>

<span data-ttu-id="c3671-3162">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3162">3</span></span><br/> <span data-ttu-id="c3671-3163">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3163">0</span></span><br/>

<span data-ttu-id="c3671-3164">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3164">1</span></span>

<span data-ttu-id="c3671-3165">\_serverVersion</span><span class="sxs-lookup"><span data-stu-id="c3671-3165">\_serverVersion</span></span>

<span data-ttu-id="c3671-3166">\_reserviert (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3166">\_reserved (variable)</span></span>



 

<span data-ttu-id="c3671-3167">**\_ serverVersion**:</span><span class="sxs-lookup"><span data-stu-id="c3671-3167">**\_serverVersion**:</span></span>

<span data-ttu-id="c3671-3168">Eine 32-Bit-Ganzzahl, die angibt, ob der Server 64-Bit-Offsets unterstützen *kann.*</span><span class="sxs-lookup"><span data-stu-id="c3671-3168">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="c3671-3169">Weitere Informationen finden Sie in Abschnitt 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="c3671-3169">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="c3671-3170">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-3170">Value</span></span>      | <span data-ttu-id="c3671-3171">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-3171">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="c3671-3172">0x00000007</span><span class="sxs-lookup"><span data-stu-id="c3671-3172">0x00000007</span></span> | <span data-ttu-id="c3671-3173">Der Server kann nur 32-Bit-Offsets senden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3173">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="c3671-3174">0x00010007</span><span class="sxs-lookup"><span data-stu-id="c3671-3174">0x00010007</span></span> | <span data-ttu-id="c3671-3175">Der Server kann 32- oder 64-Bit-Offsets senden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3175">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="c3671-3176">**\_ reserviert:** Reserviert.</span><span class="sxs-lookup"><span data-stu-id="c3671-3176">**\_reserved**: Reserved.</span></span> <span data-ttu-id="c3671-3177">Der Server KANN eine beliebige Anzahl beliebiger Werte senden, und der Client MUSS diese Werte ignorieren, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3177">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="c3671-3178">2.2.3.8 CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="c3671-3178">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="c3671-3179">Die CPMCreateQueryIn-Nachricht erstellt eine neue Abfrage.</span><span class="sxs-lookup"><span data-stu-id="c3671-3179">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="c3671-3180">Das Format der CPMCreateQueryIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3180">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="c3671-3181">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3181">0</span></span>

<span data-ttu-id="c3671-3182">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3182">1</span></span>

<span data-ttu-id="c3671-3183">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3183">2</span></span>

<span data-ttu-id="c3671-3184">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3184">3</span></span>

<span data-ttu-id="c3671-3185">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3185">4</span></span>

<span data-ttu-id="c3671-3186">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3186">5</span></span>

<span data-ttu-id="c3671-3187">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3187">6</span></span>

<span data-ttu-id="c3671-3188">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3188">7</span></span>

<span data-ttu-id="c3671-3189">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3189">8</span></span>

<span data-ttu-id="c3671-3190">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3190">9</span></span>

<span data-ttu-id="c3671-3191">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3191">1</span></span><br/> <span data-ttu-id="c3671-3192">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3192">0</span></span><br/>

<span data-ttu-id="c3671-3193">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3193">1</span></span>

<span data-ttu-id="c3671-3194">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3194">2</span></span>

<span data-ttu-id="c3671-3195">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3195">3</span></span>

<span data-ttu-id="c3671-3196">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3196">4</span></span>

<span data-ttu-id="c3671-3197">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3197">5</span></span>

<span data-ttu-id="c3671-3198">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3198">6</span></span>

<span data-ttu-id="c3671-3199">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3199">7</span></span>

<span data-ttu-id="c3671-3200">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3200">8</span></span>

<span data-ttu-id="c3671-3201">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3201">9</span></span>

<span data-ttu-id="c3671-3202">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3202">2</span></span><br/> <span data-ttu-id="c3671-3203">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3203">0</span></span><br/>

<span data-ttu-id="c3671-3204">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3204">1</span></span>

<span data-ttu-id="c3671-3205">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3205">2</span></span>

<span data-ttu-id="c3671-3206">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3206">3</span></span>

<span data-ttu-id="c3671-3207">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3207">4</span></span>

<span data-ttu-id="c3671-3208">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3208">5</span></span>

<span data-ttu-id="c3671-3209">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3209">6</span></span>

<span data-ttu-id="c3671-3210">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3210">7</span></span>

<span data-ttu-id="c3671-3211">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3211">8</span></span>

<span data-ttu-id="c3671-3212">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3212">9</span></span>

<span data-ttu-id="c3671-3213">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3213">3</span></span><br/> <span data-ttu-id="c3671-3214">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3214">0</span></span><br/>

<span data-ttu-id="c3671-3215">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3215">1</span></span>

<span data-ttu-id="c3671-3216">Size</span><span class="sxs-lookup"><span data-stu-id="c3671-3216">Size</span></span>

<span data-ttu-id="c3671-3217">CColumnSetPresent</span><span class="sxs-lookup"><span data-stu-id="c3671-3217">CColumnSetPresent</span></span>

<span data-ttu-id="c3671-3218">ColumnSet (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-3218">ColumnSet (optional)</span></span>

<span data-ttu-id="c3671-3219">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3219">... (variable)</span></span>

<span data-ttu-id="c3671-3220">CRestrictionPresent.</span><span class="sxs-lookup"><span data-stu-id="c3671-3220">CRestrictionPresent.</span></span>

<span data-ttu-id="c3671-3221">Einschränkung (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-3221">Restriction (optional)</span></span>

<span data-ttu-id="c3671-3222">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3222">... (variable)</span></span>

<span data-ttu-id="c3671-3223">CSortSetPresent</span><span class="sxs-lookup"><span data-stu-id="c3671-3223">CSortSetPresent</span></span>

<span data-ttu-id="c3671-3224">SortSet (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-3224">SortSet (optional)</span></span>

<span data-ttu-id="c3671-3225">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3225">... (variable)</span></span>

<span data-ttu-id="c3671-3226">CCategorizationSetPresent</span><span class="sxs-lookup"><span data-stu-id="c3671-3226">CCategorizationSetPresent</span></span>

<span data-ttu-id="c3671-3227">CategorizationSet (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-3227">CategorizationSet (optional)</span></span>

<span data-ttu-id="c3671-3228">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3228">... (variable)</span></span>

<span data-ttu-id="c3671-3229">RowSetProperties</span><span class="sxs-lookup"><span data-stu-id="c3671-3229">RowSetProperties</span></span>

<span data-ttu-id="c3671-3230">...</span><span class="sxs-lookup"><span data-stu-id="c3671-3230">...</span></span>

<span data-ttu-id="c3671-3231">...</span><span class="sxs-lookup"><span data-stu-id="c3671-3231">...</span></span>

<span data-ttu-id="c3671-3232">...</span><span class="sxs-lookup"><span data-stu-id="c3671-3232">...</span></span>

<span data-ttu-id="c3671-3233">...</span><span class="sxs-lookup"><span data-stu-id="c3671-3233">...</span></span>

<span data-ttu-id="c3671-3234">PidMapper (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3234">PidMapper (variable)</span></span>



 

<span data-ttu-id="c3671-3235">**Größe:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Bytes vom Anfang dieses Felds bis zum Ende der Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3235">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="c3671-3236">**CColumnSetPresent:** Ein Bytefeld, das angibt, ob das ColumnSet-Feld vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-3236">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="c3671-3237">Dieses Feld MUSS auf 0x01 oder 0x00 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3237">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="c3671-3238">Wenn auf 0x01 muss das Feld CColumnSet vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-3238">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="c3671-3239">Wenn sie auf 0x00 festgelegt ist, MUSS sie fehlen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3239">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="c3671-3240">**ColumnSet:** Eine CColumnSet-Struktur, die die Spaltennummern enthält, in denen die Eigenschaften von CPidMapper zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3240">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="c3671-3241">**CRestrictionPresent:** Ein Bytefeld, das angibt, ob das Feld Einschränkung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-3241">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="c3671-3242">Wenn ein Wert ungleich 0 (null) festgelegt ist, MUSS das Feld Einschränkung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-3242">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="c3671-3243">Wenn sie auf 0x00 festgelegt ist, MUSS die Einschränkung nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-3243">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="c3671-3244">**Einschränkung:** Eine CRestriction-Struktur, die die Befehlsstruktur der Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-3244">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="c3671-3245">**CSortSetPresent:** Ein Bytefeld, das angibt, ob das SortSet-Feld vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-3245">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="c3671-3246">Wenn ein Wert ungleich 0 (null) festgelegt ist, MUSS das SortSet-Feld vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-3246">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="c3671-3247">Wenn diese Einstellung auf 0x00 festgelegt ist, MUSS SortSet fehlen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3247">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="c3671-3248">**SortSet:** Eine CSortSet-Struktur, die die Sortierreihenfolge der Abfrage angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3248">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="c3671-3249">**CCategorizationSetPresent:** Ein Bytefeld, das angibt, ob das Feld CCategorizationSet vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-3249">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="c3671-3250">Wenn ein Wert ungleich 0 (null) festgelegt ist, MUSS das Feld CCategorizationSet vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-3250">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="c3671-3251">Wenn CCategorizationSet auf 0x00 festgelegt ist, MUSS es nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-3251">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="c3671-3252">**CCategorizationSet:** Eine CCategorizationSet-Struktur, die die Gruppen für die Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-3252">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="c3671-3253">**RowSetProperties:** Eine CRowsetProperties-Struktur, die Konfigurationsinformationen für die Abfrage bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3253">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="c3671-3254">**PidMapper:** Eine CPidMapper-Struktur, die Eigenschaften enthält, die in einem Rowset zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3254">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="c3671-3255">2.2.3.9 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="c3671-3255">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="c3671-3256">Die CPMCreateQueryOut-Nachricht enthält eine Antwort auf eine CPMCreateQueryIn-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c3671-3256">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="c3671-3257">Das Format der CPMCreateQueryOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3257">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="c3671-3258">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3258">0</span></span>

<span data-ttu-id="c3671-3259">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3259">1</span></span>

<span data-ttu-id="c3671-3260">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3260">2</span></span>

<span data-ttu-id="c3671-3261">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3261">3</span></span>

<span data-ttu-id="c3671-3262">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3262">4</span></span>

<span data-ttu-id="c3671-3263">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3263">5</span></span>

<span data-ttu-id="c3671-3264">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3264">6</span></span>

<span data-ttu-id="c3671-3265">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3265">7</span></span>

<span data-ttu-id="c3671-3266">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3266">8</span></span>

<span data-ttu-id="c3671-3267">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3267">9</span></span>

<span data-ttu-id="c3671-3268">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3268">1</span></span><br/> <span data-ttu-id="c3671-3269">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3269">0</span></span><br/>

<span data-ttu-id="c3671-3270">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3270">1</span></span>

<span data-ttu-id="c3671-3271">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3271">2</span></span>

<span data-ttu-id="c3671-3272">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3272">3</span></span>

<span data-ttu-id="c3671-3273">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3273">4</span></span>

<span data-ttu-id="c3671-3274">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3274">5</span></span>

<span data-ttu-id="c3671-3275">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3275">6</span></span>

<span data-ttu-id="c3671-3276">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3276">7</span></span>

<span data-ttu-id="c3671-3277">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3277">8</span></span>

<span data-ttu-id="c3671-3278">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3278">9</span></span>

<span data-ttu-id="c3671-3279">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3279">2</span></span><br/> <span data-ttu-id="c3671-3280">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3280">0</span></span><br/>

<span data-ttu-id="c3671-3281">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3281">1</span></span>

<span data-ttu-id="c3671-3282">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3282">2</span></span>

<span data-ttu-id="c3671-3283">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3283">3</span></span>

<span data-ttu-id="c3671-3284">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3284">4</span></span>

<span data-ttu-id="c3671-3285">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3285">5</span></span>

<span data-ttu-id="c3671-3286">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3286">6</span></span>

<span data-ttu-id="c3671-3287">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3287">7</span></span>

<span data-ttu-id="c3671-3288">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3288">8</span></span>

<span data-ttu-id="c3671-3289">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3289">9</span></span>

<span data-ttu-id="c3671-3290">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3290">3</span></span><br/> <span data-ttu-id="c3671-3291">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3291">0</span></span><br/>

<span data-ttu-id="c3671-3292">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3292">1</span></span>

<span data-ttu-id="c3671-3293">\_fTrueSequential</span><span class="sxs-lookup"><span data-stu-id="c3671-3293">\_fTrueSequential</span></span>

<span data-ttu-id="c3671-3294">\_fWorkIdUnique</span><span class="sxs-lookup"><span data-stu-id="c3671-3294">\_fWorkIdUnique</span></span>

<span data-ttu-id="c3671-3295">aCursors</span><span class="sxs-lookup"><span data-stu-id="c3671-3295">aCursors</span></span>



 

<span data-ttu-id="c3671-3296">**\_ fTrueSequential:** Ein informativer boolescher Wert, der angibt, ob die Abfrage ergebnisse schneller liefern kann.</span><span class="sxs-lookup"><span data-stu-id="c3671-3296">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="c3671-3297">Wenn für die in CPMCreateQueryIn bereitgestellte Abfrage 0x00000001 festgelegt ist, kann der Server den Index so verwenden, dass die Abfrageergebnisse wahrscheinlich schneller übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3297">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="c3671-3298">Wenn sie auf 0x00000000 festgelegt ist, kommt es bei der Übermittlung von Abfrageergebnissen zu einer höheren Latenz.</span><span class="sxs-lookup"><span data-stu-id="c3671-3298">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="c3671-3299">DARF nicht auf einen anderen Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3299">MUST not be set to any other value.</span></span>

<span data-ttu-id="c3671-3300">**\_ fWorkIdUnique:** Ein boolescher Wert, der angibt, ob die Dokumentbezeichner, auf die die Cursor zeigen, in den Abfrageergebnissen eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-3300">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="c3671-3301">Wenn 0x00000001 festgelegt ist, sind die Bezeichner eindeutig.</span><span class="sxs-lookup"><span data-stu-id="c3671-3301">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="c3671-3302">Wenn sie auf 0x00000000 festgelegt sind, sind sie nur im gesamten Rowset eindeutig.</span><span class="sxs-lookup"><span data-stu-id="c3671-3302">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="c3671-3303">**aCursors:** Ein Array von 32-Bit-Ganzzahlen ohne Vorzeichen, die die Handles für Cursor darstellen, wobei die Anzahl der Elemente der Anzahl der Kategorien im Feld CategorizationSet der CPMCreateQueryIn-Nachricht entspricht.</span><span class="sxs-lookup"><span data-stu-id="c3671-3303">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="c3671-3304">2.2.3.10 CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="c3671-3304">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="c3671-3305">Die CPMGetQueryStatusIn-Nachricht fordert den Status einer Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="c3671-3305">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="c3671-3306">Das Format der CPMGetQueryStatusIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3306">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="c3671-3307">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3307">0</span></span>

<span data-ttu-id="c3671-3308">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3308">1</span></span>

<span data-ttu-id="c3671-3309">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3309">2</span></span>

<span data-ttu-id="c3671-3310">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3310">3</span></span>

<span data-ttu-id="c3671-3311">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3311">4</span></span>

<span data-ttu-id="c3671-3312">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3312">5</span></span>

<span data-ttu-id="c3671-3313">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3313">6</span></span>

<span data-ttu-id="c3671-3314">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3314">7</span></span>

<span data-ttu-id="c3671-3315">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3315">8</span></span>

<span data-ttu-id="c3671-3316">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3316">9</span></span>

<span data-ttu-id="c3671-3317">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3317">1</span></span><br/> <span data-ttu-id="c3671-3318">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3318">0</span></span><br/>

<span data-ttu-id="c3671-3319">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3319">1</span></span>

<span data-ttu-id="c3671-3320">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3320">2</span></span>

<span data-ttu-id="c3671-3321">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3321">3</span></span>

<span data-ttu-id="c3671-3322">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3322">4</span></span>

<span data-ttu-id="c3671-3323">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3323">5</span></span>

<span data-ttu-id="c3671-3324">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3324">6</span></span>

<span data-ttu-id="c3671-3325">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3325">7</span></span>

<span data-ttu-id="c3671-3326">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3326">8</span></span>

<span data-ttu-id="c3671-3327">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3327">9</span></span>

<span data-ttu-id="c3671-3328">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3328">2</span></span><br/> <span data-ttu-id="c3671-3329">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3329">0</span></span><br/>

<span data-ttu-id="c3671-3330">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3330">1</span></span>

<span data-ttu-id="c3671-3331">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3331">2</span></span>

<span data-ttu-id="c3671-3332">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3332">3</span></span>

<span data-ttu-id="c3671-3333">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3333">4</span></span>

<span data-ttu-id="c3671-3334">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3334">5</span></span>

<span data-ttu-id="c3671-3335">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3335">6</span></span>

<span data-ttu-id="c3671-3336">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3336">7</span></span>

<span data-ttu-id="c3671-3337">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3337">8</span></span>

<span data-ttu-id="c3671-3338">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3338">9</span></span>

<span data-ttu-id="c3671-3339">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3339">3</span></span><br/> <span data-ttu-id="c3671-3340">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3340">0</span></span><br/>

<span data-ttu-id="c3671-3341">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3341">1</span></span>

<span data-ttu-id="c3671-3342">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="c3671-3342">\_hCursor</span></span>



 

<span data-ttu-id="c3671-3343">**\_ hCursor:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Handle aus der CPMCreateQueryOut-Nachricht darstellt, die die Abfrage identifiziert, für die Statusinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3343">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="c3671-3344">2.2.3.11 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="c3671-3344">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="c3671-3345">Die CPMGetQueryStatusOut-Nachricht antwortet auf eine CPMGetQueryStatusIn-Nachricht mit dem Status der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="c3671-3345">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="c3671-3346">Das Format der CPMGetQueryStatusOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3346">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="c3671-3347">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3347">0</span></span>

<span data-ttu-id="c3671-3348">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3348">1</span></span>

<span data-ttu-id="c3671-3349">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3349">2</span></span>

<span data-ttu-id="c3671-3350">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3350">3</span></span>

<span data-ttu-id="c3671-3351">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3351">4</span></span>

<span data-ttu-id="c3671-3352">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3352">5</span></span>

<span data-ttu-id="c3671-3353">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3353">6</span></span>

<span data-ttu-id="c3671-3354">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3354">7</span></span>

<span data-ttu-id="c3671-3355">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3355">8</span></span>

<span data-ttu-id="c3671-3356">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3356">9</span></span>

<span data-ttu-id="c3671-3357">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3357">1</span></span><br/> <span data-ttu-id="c3671-3358">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3358">0</span></span><br/>

<span data-ttu-id="c3671-3359">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3359">1</span></span>

<span data-ttu-id="c3671-3360">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3360">2</span></span>

<span data-ttu-id="c3671-3361">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3361">3</span></span>

<span data-ttu-id="c3671-3362">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3362">4</span></span>

<span data-ttu-id="c3671-3363">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3363">5</span></span>

<span data-ttu-id="c3671-3364">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3364">6</span></span>

<span data-ttu-id="c3671-3365">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3365">7</span></span>

<span data-ttu-id="c3671-3366">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3366">8</span></span>

<span data-ttu-id="c3671-3367">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3367">9</span></span>

<span data-ttu-id="c3671-3368">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3368">2</span></span><br/> <span data-ttu-id="c3671-3369">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3369">0</span></span><br/>

<span data-ttu-id="c3671-3370">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3370">1</span></span>

<span data-ttu-id="c3671-3371">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3371">2</span></span>

<span data-ttu-id="c3671-3372">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3372">3</span></span>

<span data-ttu-id="c3671-3373">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3373">4</span></span>

<span data-ttu-id="c3671-3374">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3374">5</span></span>

<span data-ttu-id="c3671-3375">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3375">6</span></span>

<span data-ttu-id="c3671-3376">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3376">7</span></span>

<span data-ttu-id="c3671-3377">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3377">8</span></span>

<span data-ttu-id="c3671-3378">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3378">9</span></span>

<span data-ttu-id="c3671-3379">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3379">3</span></span><br/> <span data-ttu-id="c3671-3380">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3380">0</span></span><br/>

<span data-ttu-id="c3671-3381">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3381">1</span></span>

<span data-ttu-id="c3671-3382">\_Status</span><span class="sxs-lookup"><span data-stu-id="c3671-3382">\_Status</span></span>



 

<span data-ttu-id="c3671-3383">**\_ Status:** Eine Bitmaske mit Werten, die in den folgenden Tabellen definiert sind, die die Abfrage beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c3671-3383">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="c3671-3384">In der folgenden Tabelle sind die STAT-Werte aufgeführt, \_ \* die durch ausführen eines bitweisen AND-Vorgangs für \_ Status mit 0x00000007.</span><span class="sxs-lookup"><span data-stu-id="c3671-3384">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="c3671-3385">Das Ergebnis MUSS eines der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="c3671-3385">The result MUST be one of the following:</span></span>



| <span data-ttu-id="c3671-3386">Konstante</span><span class="sxs-lookup"><span data-stu-id="c3671-3386">Constant</span></span>                 | <span data-ttu-id="c3671-3387">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-3387">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-3388">STAT \_ BUSY 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-3388">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="c3671-3389">Die asynchrone Abfrage wird weiterhin ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3389">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="c3671-3390">STAT \_ ERROR 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-3390">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="c3671-3391">Die Abfrage befindet sich in einem Fehlerzustand.</span><span class="sxs-lookup"><span data-stu-id="c3671-3391">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="c3671-3392">STAT \_ DONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-3392">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="c3671-3393">Die Abfrage ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3393">The query is complete.</span></span>                                                            |
| <span data-ttu-id="c3671-3394">STAT \_ REFRESH 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-3394">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="c3671-3395">Die Abfrage ist abgeschlossen, aber Updates führen zu einer zusätzlichen Abfrageberechnung.</span><span class="sxs-lookup"><span data-stu-id="c3671-3395">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="c3671-3396">In der folgenden Tabelle sind zusätzliche \_ \* STAT-Bits aufgeführt, die unabhängig voneinander festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="c3671-3396">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="c3671-3397">Konstante</span><span class="sxs-lookup"><span data-stu-id="c3671-3397">Constant</span></span>                                    | <span data-ttu-id="c3671-3398">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-3398">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3671-3399">STAT \_ NOISE \_ WORDS 0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3671-3399">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="c3671-3400">Füllwörter wurden in der Inhaltsabfrage durch Platzhalterzeichen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3400">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="c3671-3401">VERALTETER \_ \_ STAT-INHALT \_ \_ 0x00000020</span><span class="sxs-lookup"><span data-stu-id="c3671-3401">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="c3671-3402">Die Ergebnisse der Abfrage sind möglicherweise falsch, da die Abfrage geänderte, aber nicht indizierte Dateien umfasst.</span><span class="sxs-lookup"><span data-stu-id="c3671-3402">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="c3671-3403">STAT \_ REFRESH \_ INCOMPLETE 0x00000040</span><span class="sxs-lookup"><span data-stu-id="c3671-3403">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="c3671-3404">Die Ergebnisse der Abfrage sind möglicherweise falsch, da die Abfrage geänderte und neu indizierte Dateien umfasst, deren Inhalt nicht enthalten war.</span><span class="sxs-lookup"><span data-stu-id="c3671-3404">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="c3671-3405">STAT \_ CONTENT QUERY INCOMPLETE \_ \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="c3671-3405">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="c3671-3406">Die Inhaltsabfrage war zu komplex, um die Enumeration abzuschließen oder zu erfordern, anstatt den Inhaltsindex zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3406">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="c3671-3407">STAT \_ TIME \_ LIMIT \_ EXCEEDED 0x00000100</span><span class="sxs-lookup"><span data-stu-id="c3671-3407">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="c3671-3408">Die Ergebnisse der Abfrage sind möglicherweise falsch, da die Ausführungszeit der Abfrage die maximal zulässige Zeit erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="c3671-3408">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="c3671-3409">2.2.3.12 CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="c3671-3409">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="c3671-3410">Die CPMGetQueryStatusExIn-Nachricht fordert den Status einer Abfrage und zusätzliche Informationen an, z. B. die Anzahl der indizierten Dokumente, die Anzahl der zu indizierten Dokumente usw.</span><span class="sxs-lookup"><span data-stu-id="c3671-3410">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="c3671-3411">Das Format der CPMGetQueryStatusExIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3411">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="c3671-3412">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3412">0</span></span>

<span data-ttu-id="c3671-3413">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3413">1</span></span>

<span data-ttu-id="c3671-3414">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3414">2</span></span>

<span data-ttu-id="c3671-3415">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3415">3</span></span>

<span data-ttu-id="c3671-3416">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3416">4</span></span>

<span data-ttu-id="c3671-3417">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3417">5</span></span>

<span data-ttu-id="c3671-3418">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3418">6</span></span>

<span data-ttu-id="c3671-3419">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3419">7</span></span>

<span data-ttu-id="c3671-3420">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3420">8</span></span>

<span data-ttu-id="c3671-3421">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3421">9</span></span>

<span data-ttu-id="c3671-3422">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3422">1</span></span><br/> <span data-ttu-id="c3671-3423">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3423">0</span></span><br/>

<span data-ttu-id="c3671-3424">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3424">1</span></span>

<span data-ttu-id="c3671-3425">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3425">2</span></span>

<span data-ttu-id="c3671-3426">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3426">3</span></span>

<span data-ttu-id="c3671-3427">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3427">4</span></span>

<span data-ttu-id="c3671-3428">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3428">5</span></span>

<span data-ttu-id="c3671-3429">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3429">6</span></span>

<span data-ttu-id="c3671-3430">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3430">7</span></span>

<span data-ttu-id="c3671-3431">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3431">8</span></span>

<span data-ttu-id="c3671-3432">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3432">9</span></span>

<span data-ttu-id="c3671-3433">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3433">2</span></span><br/> <span data-ttu-id="c3671-3434">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3434">0</span></span><br/>

<span data-ttu-id="c3671-3435">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3435">1</span></span>

<span data-ttu-id="c3671-3436">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3436">2</span></span>

<span data-ttu-id="c3671-3437">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3437">3</span></span>

<span data-ttu-id="c3671-3438">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3438">4</span></span>

<span data-ttu-id="c3671-3439">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3439">5</span></span>

<span data-ttu-id="c3671-3440">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3440">6</span></span>

<span data-ttu-id="c3671-3441">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3441">7</span></span>

<span data-ttu-id="c3671-3442">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3442">8</span></span>

<span data-ttu-id="c3671-3443">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3443">9</span></span>

<span data-ttu-id="c3671-3444">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3444">3</span></span><br/> <span data-ttu-id="c3671-3445">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3445">0</span></span><br/>

<span data-ttu-id="c3671-3446">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3446">1</span></span>

<span data-ttu-id="c3671-3447">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="c3671-3447">\_hCursor</span></span>

<span data-ttu-id="c3671-3448">\_bmk</span><span class="sxs-lookup"><span data-stu-id="c3671-3448">\_bmk</span></span>



 

<span data-ttu-id="c3671-3449">**\_ hCursor:** Ein 32-Bit-Wert, der das Handle aus der CPMCreateQueryOut-Nachricht darstellt, die die Abfrage identifiziert, für die Statusinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3449">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="c3671-3450">**\_ bmk:** Ein 32-Bit-Wert, der das Handle eines Lesezeichens angibt, dessen Position abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-3450">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="c3671-3451">2.2.3.13 CPMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="c3671-3451">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="c3671-3452">Die CPMGetQueryStatusExOut-Nachricht antwortet auf eine CPMGetQueryStatusExIn-Nachricht mit dem Status der Abfrage und anderen Statusinformationen, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3452">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="c3671-3453">Das Format der CPMGetQueryStatusExOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3453">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="c3671-3454">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3454">0</span></span>

<span data-ttu-id="c3671-3455">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3455">1</span></span>

<span data-ttu-id="c3671-3456">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3456">2</span></span>

<span data-ttu-id="c3671-3457">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3457">3</span></span>

<span data-ttu-id="c3671-3458">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3458">4</span></span>

<span data-ttu-id="c3671-3459">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3459">5</span></span>

<span data-ttu-id="c3671-3460">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3460">6</span></span>

<span data-ttu-id="c3671-3461">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3461">7</span></span>

<span data-ttu-id="c3671-3462">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3462">8</span></span>

<span data-ttu-id="c3671-3463">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3463">9</span></span>

<span data-ttu-id="c3671-3464">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3464">1</span></span><br/> <span data-ttu-id="c3671-3465">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3465">0</span></span><br/>

<span data-ttu-id="c3671-3466">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3466">1</span></span>

<span data-ttu-id="c3671-3467">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3467">2</span></span>

<span data-ttu-id="c3671-3468">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3468">3</span></span>

<span data-ttu-id="c3671-3469">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3469">4</span></span>

<span data-ttu-id="c3671-3470">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3470">5</span></span>

<span data-ttu-id="c3671-3471">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3471">6</span></span>

<span data-ttu-id="c3671-3472">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3472">7</span></span>

<span data-ttu-id="c3671-3473">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3473">8</span></span>

<span data-ttu-id="c3671-3474">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3474">9</span></span>

<span data-ttu-id="c3671-3475">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3475">2</span></span><br/> <span data-ttu-id="c3671-3476">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3476">0</span></span><br/>

<span data-ttu-id="c3671-3477">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3477">1</span></span>

<span data-ttu-id="c3671-3478">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3478">2</span></span>

<span data-ttu-id="c3671-3479">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3479">3</span></span>

<span data-ttu-id="c3671-3480">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3480">4</span></span>

<span data-ttu-id="c3671-3481">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3481">5</span></span>

<span data-ttu-id="c3671-3482">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3482">6</span></span>

<span data-ttu-id="c3671-3483">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3483">7</span></span>

<span data-ttu-id="c3671-3484">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3484">8</span></span>

<span data-ttu-id="c3671-3485">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3485">9</span></span>

<span data-ttu-id="c3671-3486">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3486">3</span></span><br/> <span data-ttu-id="c3671-3487">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3487">0</span></span><br/>

<span data-ttu-id="c3671-3488">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3488">1</span></span>

<span data-ttu-id="c3671-3489">\_Status</span><span class="sxs-lookup"><span data-stu-id="c3671-3489">\_Status</span></span>

<span data-ttu-id="c3671-3490">\_cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="c3671-3490">\_cFilteredDocuments</span></span>

<span data-ttu-id="c3671-3491">\_cDocumentsToFilter</span><span class="sxs-lookup"><span data-stu-id="c3671-3491">\_cDocumentsToFilter</span></span>

<span data-ttu-id="c3671-3492">\_dwRatioFinishedDenominator</span><span class="sxs-lookup"><span data-stu-id="c3671-3492">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="c3671-3493">\_dwRatioFinishedNumerator</span><span class="sxs-lookup"><span data-stu-id="c3671-3493">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="c3671-3494">\_iRowBmk</span><span class="sxs-lookup"><span data-stu-id="c3671-3494">\_iRowBmk</span></span>

<span data-ttu-id="c3671-3495">\_cRowsTotal</span><span class="sxs-lookup"><span data-stu-id="c3671-3495">\_cRowsTotal</span></span>



 

<span data-ttu-id="c3671-3496">**\_ Status:** Einer der STAT-Werte \_ \* -Werte, die in Abschnitt 2.2.3.11 angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-3496">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="c3671-3497">**\_ cFilteredDocuments:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der indizierten Dokumente angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3497">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="c3671-3498">**\_ cDocumentsToFilter:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dokumente angibt, die noch indiziert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3498">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="c3671-3499">**\_ dwRatioFinishedDenominator:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Nenner des Verhältnisses der Dokumente angibt, die die Abfrage verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="c3671-3499">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="c3671-3500">**\_ dwRatioFinishedNumerator:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Zähler des Verhältnisses der Dokumente angibt, die die Abfrage verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="c3671-3500">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="c3671-3501">**\_ iRowBmk:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die ungefähre Position des Lesezeichens im Rowset in Bezug auf Zeilen angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3501">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="c3671-3502">**\_ cRowsTotal:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Zeilen im Rowset angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3502">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="c3671-3503">2.2.3.14 CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="c3671-3503">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="c3671-3504">Die CPMSetBindingsIn-Nachricht fordert die Bindung von Spalten an ein Rowset an.</span><span class="sxs-lookup"><span data-stu-id="c3671-3504">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="c3671-3505">Der Server antwortet mithilfe des Headerabschnitts der CPMBindingsIn-Nachricht mit den Ergebnissen der Anforderung, die im Statusfeld enthalten sind, auf die ANFORDERUNGsnachricht CPMSetBindingsIn. \_</span><span class="sxs-lookup"><span data-stu-id="c3671-3505">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="c3671-3506">Das Format der CPMSetBindingsIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3506">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="c3671-3507">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3507">0</span></span>

<span data-ttu-id="c3671-3508">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3508">1</span></span>

<span data-ttu-id="c3671-3509">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3509">2</span></span>

<span data-ttu-id="c3671-3510">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3510">3</span></span>

<span data-ttu-id="c3671-3511">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3511">4</span></span>

<span data-ttu-id="c3671-3512">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3512">5</span></span>

<span data-ttu-id="c3671-3513">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3513">6</span></span>

<span data-ttu-id="c3671-3514">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3514">7</span></span>

<span data-ttu-id="c3671-3515">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3515">8</span></span>

<span data-ttu-id="c3671-3516">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3516">9</span></span>

<span data-ttu-id="c3671-3517">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3517">1</span></span><br/> <span data-ttu-id="c3671-3518">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3518">0</span></span><br/>

<span data-ttu-id="c3671-3519">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3519">1</span></span>

<span data-ttu-id="c3671-3520">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3520">2</span></span>

<span data-ttu-id="c3671-3521">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3521">3</span></span>

<span data-ttu-id="c3671-3522">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3522">4</span></span>

<span data-ttu-id="c3671-3523">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3523">5</span></span>

<span data-ttu-id="c3671-3524">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3524">6</span></span>

<span data-ttu-id="c3671-3525">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3525">7</span></span>

<span data-ttu-id="c3671-3526">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3526">8</span></span>

<span data-ttu-id="c3671-3527">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3527">9</span></span>

<span data-ttu-id="c3671-3528">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3528">2</span></span><br/> <span data-ttu-id="c3671-3529">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3529">0</span></span><br/>

<span data-ttu-id="c3671-3530">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3530">1</span></span>

<span data-ttu-id="c3671-3531">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3531">2</span></span>

<span data-ttu-id="c3671-3532">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3532">3</span></span>

<span data-ttu-id="c3671-3533">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3533">4</span></span>

<span data-ttu-id="c3671-3534">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3534">5</span></span>

<span data-ttu-id="c3671-3535">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3535">6</span></span>

<span data-ttu-id="c3671-3536">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3536">7</span></span>

<span data-ttu-id="c3671-3537">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3537">8</span></span>

<span data-ttu-id="c3671-3538">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3538">9</span></span>

<span data-ttu-id="c3671-3539">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3539">3</span></span><br/> <span data-ttu-id="c3671-3540">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3540">0</span></span><br/>

<span data-ttu-id="c3671-3541">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3541">1</span></span>

<span data-ttu-id="c3671-3542">\_hCursor (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-3542">\_hCursor (optional)</span></span>

<span data-ttu-id="c3671-3543">\_cbRow (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-3543">\_cbRow (optional)</span></span>

<span data-ttu-id="c3671-3544">\_cbBindingDesc (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-3544">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="c3671-3545">\_dummy (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-3545">\_dummy (optional)</span></span>

<span data-ttu-id="c3671-3546">cColumns (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-3546">cColumns (optional)</span></span>

<span data-ttu-id="c3671-3547">aColumns (Variable, optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-3547">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="c3671-3548">**\_ hCursor:** Ein 32-Bit-Wert, der das Handle aus der CPMCreateQueryOut-Nachricht darstellt, die die Zeile identifiziert, für die Bindungen festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3548">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="c3671-3549">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-3549">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="c3671-3550">**\_ cbRow:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe einer Zeile in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3550">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="c3671-3551">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-3551">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="c3671-3552">**\_ cbBindingDesc:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge der Felder nach dem Dummyfeld in Bytes \_ angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3552">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="c3671-3553">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-3553">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="c3671-3554">**\_ dummy:** Dieses Feld wird nicht verwendet und MUSS ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3554">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="c3671-3555">Sie kann auf einen beliebigen Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3555">It can be set to any arbitrary value.</span></span> <span data-ttu-id="c3671-3556">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="c3671-3557">**cColumns:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im Array aColumns angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3557">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="c3671-3558">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-3558">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="c3671-3559">**aColumns:** Ein Array der CTableColumn-Strukturen, die die Spalten einer Zeile im Rowset beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c3671-3559">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="c3671-3560">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS fehlen, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-3560">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="c3671-3561">Strukturen im Array MÜSSEN durch 0 bis 3 Auffüllungsbytes getrennt werden, sodass jede Struktur eine 4-Byte-Ausrichtung vom Anfang einer Nachricht aufweist.</span><span class="sxs-lookup"><span data-stu-id="c3671-3561">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="c3671-3562">Solche Auffüllungsbytes können beliebige Werte sein, und MÜSSEN beim Empfang ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3562">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="c3671-3563">2.2.3.15 CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="c3671-3563">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="c3671-3564">Die CPMGetRowsIn-Nachricht fordert Zeilen aus einer Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="c3671-3564">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="c3671-3565">Das Format der CPMGetRowsIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3565">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="c3671-3566">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3566">0</span></span>

<span data-ttu-id="c3671-3567">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3567">1</span></span>

<span data-ttu-id="c3671-3568">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3568">2</span></span>

<span data-ttu-id="c3671-3569">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3569">3</span></span>

<span data-ttu-id="c3671-3570">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3570">4</span></span>

<span data-ttu-id="c3671-3571">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3571">5</span></span>

<span data-ttu-id="c3671-3572">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3572">6</span></span>

<span data-ttu-id="c3671-3573">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3573">7</span></span>

<span data-ttu-id="c3671-3574">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3574">8</span></span>

<span data-ttu-id="c3671-3575">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3575">9</span></span>

<span data-ttu-id="c3671-3576">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3576">1</span></span><br/> <span data-ttu-id="c3671-3577">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3577">0</span></span><br/>

<span data-ttu-id="c3671-3578">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3578">1</span></span>

<span data-ttu-id="c3671-3579">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3579">2</span></span>

<span data-ttu-id="c3671-3580">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3580">3</span></span>

<span data-ttu-id="c3671-3581">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3581">4</span></span>

<span data-ttu-id="c3671-3582">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3582">5</span></span>

<span data-ttu-id="c3671-3583">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3583">6</span></span>

<span data-ttu-id="c3671-3584">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3584">7</span></span>

<span data-ttu-id="c3671-3585">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3585">8</span></span>

<span data-ttu-id="c3671-3586">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3586">9</span></span>

<span data-ttu-id="c3671-3587">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3587">2</span></span><br/> <span data-ttu-id="c3671-3588">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3588">0</span></span><br/>

<span data-ttu-id="c3671-3589">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3589">1</span></span>

<span data-ttu-id="c3671-3590">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3590">2</span></span>

<span data-ttu-id="c3671-3591">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3591">3</span></span>

<span data-ttu-id="c3671-3592">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3592">4</span></span>

<span data-ttu-id="c3671-3593">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3593">5</span></span>

<span data-ttu-id="c3671-3594">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3594">6</span></span>

<span data-ttu-id="c3671-3595">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3595">7</span></span>

<span data-ttu-id="c3671-3596">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3596">8</span></span>

<span data-ttu-id="c3671-3597">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3597">9</span></span>

<span data-ttu-id="c3671-3598">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3598">3</span></span><br/> <span data-ttu-id="c3671-3599">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3599">0</span></span><br/>

<span data-ttu-id="c3671-3600">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3600">1</span></span>

<span data-ttu-id="c3671-3601">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="c3671-3601">\_hCursor</span></span>

<span data-ttu-id="c3671-3602">\_cRowsToTransfer</span><span class="sxs-lookup"><span data-stu-id="c3671-3602">\_cRowsToTransfer</span></span>

<span data-ttu-id="c3671-3603">\_cbRowWidth</span><span class="sxs-lookup"><span data-stu-id="c3671-3603">\_cbRowWidth</span></span>

<span data-ttu-id="c3671-3604">\_cbSeek</span><span class="sxs-lookup"><span data-stu-id="c3671-3604">\_cbSeek</span></span>

<span data-ttu-id="c3671-3605">\_cbReserved</span><span class="sxs-lookup"><span data-stu-id="c3671-3605">\_cbReserved</span></span>

<span data-ttu-id="c3671-3606">\_cbReadBuffer</span><span class="sxs-lookup"><span data-stu-id="c3671-3606">\_cbReadBuffer</span></span>

<span data-ttu-id="c3671-3607">\_ulClientBase</span><span class="sxs-lookup"><span data-stu-id="c3671-3607">\_ulClientBase</span></span>

<span data-ttu-id="c3671-3608">\_fBwdFetch</span><span class="sxs-lookup"><span data-stu-id="c3671-3608">\_fBwdFetch</span></span>

<span data-ttu-id="c3671-3609">eType</span><span class="sxs-lookup"><span data-stu-id="c3671-3609">eType</span></span>

<span data-ttu-id="c3671-3610">\_chapt</span><span class="sxs-lookup"><span data-stu-id="c3671-3610">\_chapt</span></span>

<span data-ttu-id="c3671-3611">SeekDescription</span><span class="sxs-lookup"><span data-stu-id="c3671-3611">SeekDescription</span></span>

<span data-ttu-id="c3671-3612">...</span><span class="sxs-lookup"><span data-stu-id="c3671-3612">...</span></span>

<span data-ttu-id="c3671-3613">... (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3613">... (variable)</span></span>



 

<span data-ttu-id="c3671-3614">**\_ hCursor:** Ein 32-Bit-Wert, der das Handle aus der CPMCreateQueryOut-Nachricht darstellt, die die Abfrage identifiziert, für die Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3614">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="c3671-3615">**\_ cRowsToTransfer:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die maximale Anzahl von Zeilen angibt, die der Client als Antwort auf diese Nachricht empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="c3671-3615">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="c3671-3616">**\_ cbRowWidth:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge einer Zeile in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3616">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="c3671-3617">**\_ cbSeek:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der Nachricht angibt, die mit eType beginnt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3617">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="c3671-3618">**\_ cbReserved:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe einer CPMGetRowsOut-Nachricht in Bytes angibt (ohne die Felder Rows und SeekDescriptions).</span><span class="sxs-lookup"><span data-stu-id="c3671-3618">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="c3671-3619">Dieser Wert in diesem Feld wird dem Wert des \_ cbSeek-Felds hinzugefügt und dann verwendet, um den Offset des Rows-Felds in der CPMGetRowsOut-Nachricht zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3619">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="c3671-3620">**\_ cbReadBuffer:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die auf das Maximum des Werts von \_ cbRowWidth oder das 1000-fache des Werts von \_ cRowsToTransfer festgelegt werden MUSS, aufgerundet auf das nächste 512-Byte-Vielfache.</span><span class="sxs-lookup"><span data-stu-id="c3671-3620">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="c3671-3621">Der Wert DARF 0x00004000 NICHT überschreiten.</span><span class="sxs-lookup"><span data-stu-id="c3671-3621">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="c3671-3622">**\_ ulClientBase:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Basiswert angibt, der für Zeigerberechnungen im Zeilenpuffer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-3622">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="c3671-3623">Wenn 64-Bit-Offsets verwendet werden, wird das Feld reserved2 des Nachrichtenheaders als obere 32-Bit-Klasse und \_ ulClientBase als unteres 32-Bit-Feld eines 64-Bit-Werts verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3671-3623">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="c3671-3624">Weitere Informationen finden Sie in Abschnitt 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="c3671-3624">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="c3671-3625">**\_ fBwdFetch:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Reihenfolge angibt, in der die Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3625">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="c3671-3626">Wenn 0x00000001 festgelegt ist, werden die Zeilen in umgekehrter Reihenfolge abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3626">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="c3671-3627">Wenn 0x00000000 festgelegt ist, werden die Zeilen in vorwärts gerichteter Reihenfolge abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3627">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="c3671-3628">DARF NICHT auf andere Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3628">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="c3671-3629">**eType:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die einen der folgenden Werte enthält, um den Typ des durchzuführenden Vorgangs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-3629">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="c3671-3630">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-3630">Value</span></span>                         | <span data-ttu-id="c3671-3631">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-3631">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="c3671-3632">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-3632">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="c3671-3633">SeekDescription enthält eine CRowSeekNext-Struktur.</span><span class="sxs-lookup"><span data-stu-id="c3671-3633">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="c3671-3634">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-3634">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="c3671-3635">SeekDescription enthält eine CRowSeekAt-Struktur.</span><span class="sxs-lookup"><span data-stu-id="c3671-3635">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="c3671-3636">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-3636">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="c3671-3637">SeekDescription enthält eine CRowSeekAtRatio-Struktur.</span><span class="sxs-lookup"><span data-stu-id="c3671-3637">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="c3671-3638">eRowSeekByBookmark-0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3671-3638">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="c3671-3639">SeekDescription enthält eine CRowSeekByBookmark-Struktur.</span><span class="sxs-lookup"><span data-stu-id="c3671-3639">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="c3671-3640">**\_ chapt:** Ein 32-Bit-Wert, der das Handle des Rowset-Kapitels darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3640">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="c3671-3641">**SeekDescription:** Dieses Feld MUSS eine Struktur des Typs enthalten, der durch den eType-Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-3641">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="c3671-3642">2.2.3.16 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="c3671-3642">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="c3671-3643">Die CPMGetRowsOut-Nachricht antwortet auf eine CPMGetRowsIn-Nachricht mit den Zeilen einer Abfrage.</span><span class="sxs-lookup"><span data-stu-id="c3671-3643">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="c3671-3644">Server MÜSSEN Offsets wie folgt in Datentypen variabler Länge im Feld Zeilen formatieren:</span><span class="sxs-lookup"><span data-stu-id="c3671-3644">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="c3671-3645">Client hat angegeben, dass es sich um ein 32-Bit-System handelt (0x00000008 oder weniger im iClientVersion-Feld von CPMConnectIn): Offsets sind 32-Bit-Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3645">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="c3671-3646">Der Client hat angegeben, dass es sich um ein 64-Bit-System handelt ( iClientVersion > 0x00000008 in CPMConnectIn), und server gibt an, dass es sich um ein \_ 32-Bit-System handelt ( serverVersion auf \_ 0x00000007 in CPMConnectOut festgelegt): Offsets sind 32-Bit-Ganzzahlen</span><span class="sxs-lookup"><span data-stu-id="c3671-3646">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="c3671-3647">Der Client hat angegeben, dass es sich um ein 64-Bit-System handelt ( iClientVersion > 0x00000008 in CPMConnectIn), und der Server hat angegeben, dass es sich um ein \_ 64-Bit-System handelt ( serverVersion auf \_ 0x00010007 in CPMConnectOut festgelegt): Offsets sind 64-Bit-Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3647">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="c3671-3648">Das Format der CPMGetRowsOut-Nachricht, die auf den Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3648">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="c3671-3649">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3649">0</span></span>

<span data-ttu-id="c3671-3650">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3650">1</span></span>

<span data-ttu-id="c3671-3651">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3651">2</span></span>

<span data-ttu-id="c3671-3652">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3652">3</span></span>

<span data-ttu-id="c3671-3653">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3653">4</span></span>

<span data-ttu-id="c3671-3654">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3654">5</span></span>

<span data-ttu-id="c3671-3655">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3655">6</span></span>

<span data-ttu-id="c3671-3656">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3656">7</span></span>

<span data-ttu-id="c3671-3657">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3657">8</span></span>

<span data-ttu-id="c3671-3658">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3658">9</span></span>

<span data-ttu-id="c3671-3659">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3659">1</span></span><br/> <span data-ttu-id="c3671-3660">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3660">0</span></span><br/>

<span data-ttu-id="c3671-3661">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3661">1</span></span>

<span data-ttu-id="c3671-3662">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3662">2</span></span>

<span data-ttu-id="c3671-3663">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3663">3</span></span>

<span data-ttu-id="c3671-3664">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3664">4</span></span>

<span data-ttu-id="c3671-3665">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3665">5</span></span>

<span data-ttu-id="c3671-3666">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3666">6</span></span>

<span data-ttu-id="c3671-3667">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3667">7</span></span>

<span data-ttu-id="c3671-3668">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3668">8</span></span>

<span data-ttu-id="c3671-3669">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3669">9</span></span>

<span data-ttu-id="c3671-3670">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3670">2</span></span><br/> <span data-ttu-id="c3671-3671">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3671">0</span></span><br/>

<span data-ttu-id="c3671-3672">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3672">1</span></span>

<span data-ttu-id="c3671-3673">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3673">2</span></span>

<span data-ttu-id="c3671-3674">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3674">3</span></span>

<span data-ttu-id="c3671-3675">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3675">4</span></span>

<span data-ttu-id="c3671-3676">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3676">5</span></span>

<span data-ttu-id="c3671-3677">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3677">6</span></span>

<span data-ttu-id="c3671-3678">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3678">7</span></span>

<span data-ttu-id="c3671-3679">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3679">8</span></span>

<span data-ttu-id="c3671-3680">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3680">9</span></span>

<span data-ttu-id="c3671-3681">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3681">3</span></span><br/> <span data-ttu-id="c3671-3682">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3682">0</span></span><br/>

<span data-ttu-id="c3671-3683">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3683">1</span></span>

<span data-ttu-id="c3671-3684">\_cRowsReturned</span><span class="sxs-lookup"><span data-stu-id="c3671-3684">\_cRowsReturned</span></span>

<span data-ttu-id="c3671-3685">eType</span><span class="sxs-lookup"><span data-stu-id="c3671-3685">eType</span></span>

<span data-ttu-id="c3671-3686">\_chapt</span><span class="sxs-lookup"><span data-stu-id="c3671-3686">\_chapt</span></span>

<span data-ttu-id="c3671-3687">SeekDescription (optional, Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3687">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="c3671-3688">...</span><span class="sxs-lookup"><span data-stu-id="c3671-3688">...</span></span>

<span data-ttu-id="c3671-3689">...</span><span class="sxs-lookup"><span data-stu-id="c3671-3689">...</span></span>

<span data-ttu-id="c3671-3690">paddingRows (optional, variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3690">paddingRows (optional, variable)</span></span>

<span data-ttu-id="c3671-3691">Zeilen</span><span class="sxs-lookup"><span data-stu-id="c3671-3691">Rows</span></span>



 

<span data-ttu-id="c3671-3692">**\_ cRowsReturned:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der in Zeilen zurückgegebenen Zeilen angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3692">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="c3671-3693">**eType:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die einen der folgenden Werte enthält, um den Typ des rowseek-Vorgangs anzugeben, der durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-3693">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="c3671-3694">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-3694">Value</span></span>                         | <span data-ttu-id="c3671-3695">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-3695">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="c3671-3696">eRowsSeekNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-3696">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="c3671-3697">No SeekDescription, ignore SeekDescription field.</span><span class="sxs-lookup"><span data-stu-id="c3671-3697">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="c3671-3698">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-3698">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="c3671-3699">SeekDescription enthält eine CRowSeekNext-Struktur.</span><span class="sxs-lookup"><span data-stu-id="c3671-3699">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="c3671-3700">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-3700">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="c3671-3701">SeekDescription enthält eine CRowSeekAt-Struktur.</span><span class="sxs-lookup"><span data-stu-id="c3671-3701">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="c3671-3702">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-3702">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="c3671-3703">SeekDescription enthält eine CRowSeekAtRatio-Struktur.</span><span class="sxs-lookup"><span data-stu-id="c3671-3703">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="c3671-3704">eRowSeekByBookmark-0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3671-3704">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="c3671-3705">SeekDescription enthält eine CRowSeekByBookmark-Struktur.</span><span class="sxs-lookup"><span data-stu-id="c3671-3705">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="c3671-3706">**\_ chapt:** Ein 32-Bit-Wert, der das Handle des Rowset-Kapitels darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3706">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="c3671-3707">**SeekDescription:** Dieses Feld MUSS eine Struktur des Typs enthalten, der durch das eType-Feld angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-3707">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="c3671-3708">**paddingRows:** Dieses Feld MUSS eine ausreichende Länge (0 bis cbReserved-1 Byte) haben, um das Rows-Feld vom Anfang einer Nachricht bis zum cbReserved-Offset zu auffüllung, wobei cbReserved der Wert in der \_ \_ \_ CPMGetRowsIn-Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-3708">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="c3671-3709">Die in diesem Feld verwendeten Auf padding-Bytes können beliebige Werte sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-3709">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="c3671-3710">Dieses Feld MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3710">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="c3671-3711">**Zeilen:** Zeilendaten werden gemäß den Spalteninformationen in der letzten CPMSetBindingsIn-Nachricht formatiert.</span><span class="sxs-lookup"><span data-stu-id="c3671-3711">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="c3671-3712">Zeilen MÜSSEN in vorwärts geordneter Reihenfolge gespeichert werden (z. B. Zeile 1 vor Zeile 2).</span><span class="sxs-lookup"><span data-stu-id="c3671-3712">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="c3671-3713">Spalten mit fester Größe MÜSSEN an den Offsets gespeichert werden, die von der letzten CPMSetBindingsIn-Nachricht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3713">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="c3671-3714">Spalten variabler Größe (z. B. Zeichenfolgen) MÜSSEN wie folgt gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="c3671-3714">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="c3671-3715">Die Variablendaten selbst (z. B. die Zeichenfolge) werden am Ende des Puffers in absteigender Reihenfolge gespeichert (z. B. befindet sich die Auflistung aller Variablendaten für Zeile 1 am Ende, Zeile 2 am nächsten usw.).</span><span class="sxs-lookup"><span data-stu-id="c3671-3715">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="c3671-3716">Der Bereich mit fester Größe (am Anfang des Zeilenpuffers) MUSS eine CRowVariant für jede Spalte enthalten, die an dem Offset gespeichert ist, der in der letzten CPMSetBindingsIn-Nachricht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-3716">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="c3671-3717">vType MUSS den Datentyp enthalten (z.B. VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="c3671-3717">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="c3671-3718">Wenn, wie durch die Regeln am Anfang dieses Abschnitts festgelegt, 32-Bit-Offsets verwendet werden, muss das Feld Offset in CRowVariant einen 32-Bit-Wert enthalten, der den Offset der Variablendaten vom Anfang der CPMGetRowsOut-Nachricht sowie den Wert von ulClientBase enthält, der in der letzten \_ CPMGetRowsIn-Nachricht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-3718">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="c3671-3719">Wenn 64-Bit-Offsets verwendet werden, muss das Feld Offset in CRowVariant einen 64-Bit-Wert enthalten, der der Offset vom Anfang der CPMGetRowsOut-Nachricht ist, der einem 64-Bit-Wert hinzugefügt wird, der mithilfe von ulClientBase als niedriger \_ 32-Bit-Wert und ulReserved2 als hohe \_ 32-Bit-Werte zusammengesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-3719">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="c3671-3720">Wenn in der CPMSetBindingsIn-Nachricht beispielsweise die beiden Spalten Size (VT \_ I4) und Title (VT \_ LPWSTR) und ulClientBase von CPMGetRowsIn 0x10000 werden zwei Zeilen wie folgt \_ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3720">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="c3671-3721">Der grau markierte Abschnitt ist der Teil mit fester Länge des Puffers.</span><span class="sxs-lookup"><span data-stu-id="c3671-3721">The section marked in grey is the fixed-length part of the buffer.</span></span>

![Beispiel für eine cpmsetbindingsin-Nachricht](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="c3671-3723">2.2.3.17 CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="c3671-3723">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="c3671-3724">Die CPMRatioFinishedIn-Nachricht fordert den Abschlussprozentsatz einer Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="c3671-3724">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="c3671-3725">Das Format der CPMRatioFinishedIn-Nachricht, die dem Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="c3671-3725">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="c3671-3726">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3726">0</span></span>

<span data-ttu-id="c3671-3727">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3727">1</span></span>

<span data-ttu-id="c3671-3728">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3728">2</span></span>

<span data-ttu-id="c3671-3729">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3729">3</span></span>

<span data-ttu-id="c3671-3730">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3730">4</span></span>

<span data-ttu-id="c3671-3731">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3731">5</span></span>

<span data-ttu-id="c3671-3732">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3732">6</span></span>

<span data-ttu-id="c3671-3733">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3733">7</span></span>

<span data-ttu-id="c3671-3734">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3734">8</span></span>

<span data-ttu-id="c3671-3735">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3735">9</span></span>

<span data-ttu-id="c3671-3736">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3736">1</span></span><br/> <span data-ttu-id="c3671-3737">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3737">0</span></span><br/>

<span data-ttu-id="c3671-3738">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3738">1</span></span>

<span data-ttu-id="c3671-3739">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3739">2</span></span>

<span data-ttu-id="c3671-3740">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3740">3</span></span>

<span data-ttu-id="c3671-3741">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3741">4</span></span>

<span data-ttu-id="c3671-3742">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3742">5</span></span>

<span data-ttu-id="c3671-3743">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3743">6</span></span>

<span data-ttu-id="c3671-3744">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3744">7</span></span>

<span data-ttu-id="c3671-3745">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3745">8</span></span>

<span data-ttu-id="c3671-3746">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3746">9</span></span>

<span data-ttu-id="c3671-3747">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3747">2</span></span><br/> <span data-ttu-id="c3671-3748">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3748">0</span></span><br/>

<span data-ttu-id="c3671-3749">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3749">1</span></span>

<span data-ttu-id="c3671-3750">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3750">2</span></span>

<span data-ttu-id="c3671-3751">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3751">3</span></span>

<span data-ttu-id="c3671-3752">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3752">4</span></span>

<span data-ttu-id="c3671-3753">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3753">5</span></span>

<span data-ttu-id="c3671-3754">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3754">6</span></span>

<span data-ttu-id="c3671-3755">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3755">7</span></span>

<span data-ttu-id="c3671-3756">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3756">8</span></span>

<span data-ttu-id="c3671-3757">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3757">9</span></span>

<span data-ttu-id="c3671-3758">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3758">3</span></span><br/> <span data-ttu-id="c3671-3759">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3759">0</span></span><br/>

<span data-ttu-id="c3671-3760">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3760">1</span></span>

<span data-ttu-id="c3671-3761">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="c3671-3761">\_hCursor</span></span>

<span data-ttu-id="c3671-3762">\_fQuick</span><span class="sxs-lookup"><span data-stu-id="c3671-3762">\_fQuick</span></span>



 

<span data-ttu-id="c3671-3763">**\_ hCursor:** Das Handle aus der CPMCreateQueryOut-Nachricht, das die Abfrage identifiziert, für die Abschlussinformationen angefordert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3763">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="c3671-3764">**\_ fQuick:** MUSS auf 0x00000001 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3764">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="c3671-3765">Nicht verwendet und MÜSSEN vom Server ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3765">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="c3671-3766">2.2.3.18 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="c3671-3766">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="c3671-3767">Die CPMRatioFinishedOut-Nachricht antwortet auf eine CPMRatioFinishedIn-Nachricht mit dem Abschlussverhältnis einer Abfrage.</span><span class="sxs-lookup"><span data-stu-id="c3671-3767">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="c3671-3768">Das Format der CPMRatioFinishedOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3768">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="c3671-3769">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3769">0</span></span>

<span data-ttu-id="c3671-3770">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3770">1</span></span>

<span data-ttu-id="c3671-3771">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3771">2</span></span>

<span data-ttu-id="c3671-3772">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3772">3</span></span>

<span data-ttu-id="c3671-3773">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3773">4</span></span>

<span data-ttu-id="c3671-3774">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3774">5</span></span>

<span data-ttu-id="c3671-3775">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3775">6</span></span>

<span data-ttu-id="c3671-3776">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3776">7</span></span>

<span data-ttu-id="c3671-3777">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3777">8</span></span>

<span data-ttu-id="c3671-3778">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3778">9</span></span>

<span data-ttu-id="c3671-3779">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3779">1</span></span><br/> <span data-ttu-id="c3671-3780">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3780">0</span></span><br/>

<span data-ttu-id="c3671-3781">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3781">1</span></span>

<span data-ttu-id="c3671-3782">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3782">2</span></span>

<span data-ttu-id="c3671-3783">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3783">3</span></span>

<span data-ttu-id="c3671-3784">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3784">4</span></span>

<span data-ttu-id="c3671-3785">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3785">5</span></span>

<span data-ttu-id="c3671-3786">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3786">6</span></span>

<span data-ttu-id="c3671-3787">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3787">7</span></span>

<span data-ttu-id="c3671-3788">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3788">8</span></span>

<span data-ttu-id="c3671-3789">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3789">9</span></span>

<span data-ttu-id="c3671-3790">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3790">2</span></span><br/> <span data-ttu-id="c3671-3791">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3791">0</span></span><br/>

<span data-ttu-id="c3671-3792">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3792">1</span></span>

<span data-ttu-id="c3671-3793">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3793">2</span></span>

<span data-ttu-id="c3671-3794">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3794">3</span></span>

<span data-ttu-id="c3671-3795">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3795">4</span></span>

<span data-ttu-id="c3671-3796">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3796">5</span></span>

<span data-ttu-id="c3671-3797">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3797">6</span></span>

<span data-ttu-id="c3671-3798">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3798">7</span></span>

<span data-ttu-id="c3671-3799">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3799">8</span></span>

<span data-ttu-id="c3671-3800">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3800">9</span></span>

<span data-ttu-id="c3671-3801">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3801">3</span></span><br/> <span data-ttu-id="c3671-3802">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3802">0</span></span><br/>

<span data-ttu-id="c3671-3803">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3803">1</span></span>

<span data-ttu-id="c3671-3804">\_ ulNumerator</span><span class="sxs-lookup"><span data-stu-id="c3671-3804">\_ ulNumerator</span></span>

<span data-ttu-id="c3671-3805">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="c3671-3805">\_ulDenominator</span></span>

<span data-ttu-id="c3671-3806">\_Krähen</span><span class="sxs-lookup"><span data-stu-id="c3671-3806">\_cRows</span></span>

<span data-ttu-id="c3671-3807">\_fNewRows</span><span class="sxs-lookup"><span data-stu-id="c3671-3807">\_fNewRows</span></span>



 

<span data-ttu-id="c3671-3808">**\_ ulNumerator:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Zähler des Vervollständigungsverhältnisses in Bezug auf Zeilen angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3808">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="c3671-3809">**\_ ulDenominator:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Nenner des Vervollständigungsverhältnisses in Bezug auf Zeilen angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3809">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="c3671-3810">MUSS größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-3810">MUST be greater than zero.</span></span>

<span data-ttu-id="c3671-3811">**\_ cRows:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Zeilen für die Abfrage angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3811">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="c3671-3812">**\_ fNewRows:** Ein boolescher Wert, der angibt, ob neue Zeilen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-3812">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="c3671-3813">Der Wert 0x00000001 gibt an, dass neue Zeilen im Rowset verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-3813">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="c3671-3814">Der Wert 0x00000000 gibt an, dass das Rowset keine neuen Zeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-3814">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="c3671-3815">Dieses Feld DARF NICHT auf andere Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3815">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="c3671-3816">2.2.3.19 CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="c3671-3816">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="c3671-3817">Die CPMFetchValueIn-Nachricht fordert einen Eigenschaftswert an, der für die Rückgabe in einem Rowset zu groß war.</span><span class="sxs-lookup"><span data-stu-id="c3671-3817">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="c3671-3818">Wie in Abschnitt 3.2.4.2.5 angegeben, wird diese Meldung wiederholt gesendet, um alle Bytes der Eigenschaft abzurufen, wobei \_ cbSoFar für jede aktualisiert wird, bis das \_ fMoreExists-Feld der CPMFetchValueOut-Nachricht auf **FALSE** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-3818">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="c3671-3819">Das Format der CPMFetchValueIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3819">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="c3671-3820">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3820">0</span></span>

<span data-ttu-id="c3671-3821">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3821">1</span></span>

<span data-ttu-id="c3671-3822">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3822">2</span></span>

<span data-ttu-id="c3671-3823">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3823">3</span></span>

<span data-ttu-id="c3671-3824">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3824">4</span></span>

<span data-ttu-id="c3671-3825">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3825">5</span></span>

<span data-ttu-id="c3671-3826">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3826">6</span></span>

<span data-ttu-id="c3671-3827">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3827">7</span></span>

<span data-ttu-id="c3671-3828">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3828">8</span></span>

<span data-ttu-id="c3671-3829">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3829">9</span></span>

<span data-ttu-id="c3671-3830">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3830">1</span></span><br/> <span data-ttu-id="c3671-3831">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3831">0</span></span><br/>

<span data-ttu-id="c3671-3832">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3832">1</span></span>

<span data-ttu-id="c3671-3833">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3833">2</span></span>

<span data-ttu-id="c3671-3834">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3834">3</span></span>

<span data-ttu-id="c3671-3835">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3835">4</span></span>

<span data-ttu-id="c3671-3836">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3836">5</span></span>

<span data-ttu-id="c3671-3837">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3837">6</span></span>

<span data-ttu-id="c3671-3838">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3838">7</span></span>

<span data-ttu-id="c3671-3839">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3839">8</span></span>

<span data-ttu-id="c3671-3840">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3840">9</span></span>

<span data-ttu-id="c3671-3841">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3841">2</span></span><br/> <span data-ttu-id="c3671-3842">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3842">0</span></span><br/>

<span data-ttu-id="c3671-3843">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3843">1</span></span>

<span data-ttu-id="c3671-3844">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3844">2</span></span>

<span data-ttu-id="c3671-3845">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3845">3</span></span>

<span data-ttu-id="c3671-3846">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3846">4</span></span>

<span data-ttu-id="c3671-3847">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3847">5</span></span>

<span data-ttu-id="c3671-3848">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3848">6</span></span>

<span data-ttu-id="c3671-3849">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3849">7</span></span>

<span data-ttu-id="c3671-3850">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3850">8</span></span>

<span data-ttu-id="c3671-3851">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3851">9</span></span>

<span data-ttu-id="c3671-3852">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3852">3</span></span><br/> <span data-ttu-id="c3671-3853">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3853">0</span></span><br/>

<span data-ttu-id="c3671-3854">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3854">1</span></span>

<span data-ttu-id="c3671-3855">\_Wid</span><span class="sxs-lookup"><span data-stu-id="c3671-3855">\_wid</span></span>

<span data-ttu-id="c3671-3856">\_cbSoFar</span><span class="sxs-lookup"><span data-stu-id="c3671-3856">\_cbSoFar</span></span>

<span data-ttu-id="c3671-3857">\_cbPropSpec</span><span class="sxs-lookup"><span data-stu-id="c3671-3857">\_cbPropSpec</span></span>

<span data-ttu-id="c3671-3858">\_cbChunk</span><span class="sxs-lookup"><span data-stu-id="c3671-3858">\_cbChunk</span></span>

<span data-ttu-id="c3671-3859">PropSpec (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3859">PropSpec (variable)</span></span>

<span data-ttu-id="c3671-3860">...</span><span class="sxs-lookup"><span data-stu-id="c3671-3860">...</span></span>

<span data-ttu-id="c3671-3861">\_Auffüllen (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3861">\_padding (variable)</span></span>



 

<span data-ttu-id="c3671-3862">**\_ wid**: Eine 32-Bit-Ganzzahl ohne Vorzeichen, die Informationen über die Dokument-ID enthält, die das Dokument identifiziert, für das eine Eigenschaft abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-3862">**\_wid**: A 32-bit unsigned integer containing information about the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="c3671-3863">**\_ cbSoFar:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Bytes enthält, die zuvor für diese Eigenschaft übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3863">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="c3671-3864">MUSS in der ersten Nachricht auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3864">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="c3671-3865">**\_ cbPropSpec:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des PropSpec-Felds in Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-3865">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="c3671-3866">**\_ cbChunk:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die maximale Anzahl von Bytes enthält, die der Absender in einer CPMFetchValueOut-Nachricht akzeptieren kann.</span><span class="sxs-lookup"><span data-stu-id="c3671-3866">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="c3671-3867">*Windows-Verhalten: Dieses Feld ist für alle Versionen von Windows auf 0x00004000 festgelegt.*</span><span class="sxs-lookup"><span data-stu-id="c3671-3867">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="c3671-3868">**PropSpec:** Eine CFullPropSpec-Struktur, die die abzurufende Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3868">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="c3671-3869">**\_ auffüllen:** Dieses Feld MUSS die erforderliche Länge (0 bis 3 Bytes) haben, um die Nachricht auf ein Vielfaches von 4 Bytes aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3869">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="c3671-3870">Der Wert der Auffüllungsbytes kann ein beliebiger Wert sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-3870">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="c3671-3871">Dieses Feld MUSS vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3871">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="c3671-3872">2.2.3.20 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="c3671-3872">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="c3671-3873">Die CPMFetchValueOut-Nachricht antwortet auf eine CPMFetchValueIn-Nachricht mit einem Eigenschaftswert aus einer vorherigen Abfrage.</span><span class="sxs-lookup"><span data-stu-id="c3671-3873">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="c3671-3874">Wie in Abschnitt 3.1.5.2.8 angegeben, wird diese Nachricht nach jeder CPMFetchValueIn-Nachricht gesendet, bis alle Bytes der Eigenschaft übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3874">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="c3671-3875">Das Format der CPMFetchValueOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3875">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="c3671-3876">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3876">0</span></span>

<span data-ttu-id="c3671-3877">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3877">1</span></span>

<span data-ttu-id="c3671-3878">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3878">2</span></span>

<span data-ttu-id="c3671-3879">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3879">3</span></span>

<span data-ttu-id="c3671-3880">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3880">4</span></span>

<span data-ttu-id="c3671-3881">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3881">5</span></span>

<span data-ttu-id="c3671-3882">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3882">6</span></span>

<span data-ttu-id="c3671-3883">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3883">7</span></span>

<span data-ttu-id="c3671-3884">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3884">8</span></span>

<span data-ttu-id="c3671-3885">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3885">9</span></span>

<span data-ttu-id="c3671-3886">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3886">1</span></span><br/> <span data-ttu-id="c3671-3887">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3887">0</span></span><br/>

<span data-ttu-id="c3671-3888">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3888">1</span></span>

<span data-ttu-id="c3671-3889">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3889">2</span></span>

<span data-ttu-id="c3671-3890">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3890">3</span></span>

<span data-ttu-id="c3671-3891">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3891">4</span></span>

<span data-ttu-id="c3671-3892">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3892">5</span></span>

<span data-ttu-id="c3671-3893">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3893">6</span></span>

<span data-ttu-id="c3671-3894">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3894">7</span></span>

<span data-ttu-id="c3671-3895">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3895">8</span></span>

<span data-ttu-id="c3671-3896">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3896">9</span></span>

<span data-ttu-id="c3671-3897">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3897">2</span></span><br/> <span data-ttu-id="c3671-3898">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3898">0</span></span><br/>

<span data-ttu-id="c3671-3899">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3899">1</span></span>

<span data-ttu-id="c3671-3900">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3900">2</span></span>

<span data-ttu-id="c3671-3901">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3901">3</span></span>

<span data-ttu-id="c3671-3902">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3902">4</span></span>

<span data-ttu-id="c3671-3903">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3903">5</span></span>

<span data-ttu-id="c3671-3904">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3904">6</span></span>

<span data-ttu-id="c3671-3905">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3905">7</span></span>

<span data-ttu-id="c3671-3906">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3906">8</span></span>

<span data-ttu-id="c3671-3907">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3907">9</span></span>

<span data-ttu-id="c3671-3908">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3908">3</span></span><br/> <span data-ttu-id="c3671-3909">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3909">0</span></span><br/>

<span data-ttu-id="c3671-3910">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3910">1</span></span>

<span data-ttu-id="c3671-3911">\_cbValue</span><span class="sxs-lookup"><span data-stu-id="c3671-3911">\_cbValue</span></span>

<span data-ttu-id="c3671-3912">\_fMoreExists</span><span class="sxs-lookup"><span data-stu-id="c3671-3912">\_fMoreExists</span></span>

<span data-ttu-id="c3671-3913">\_fValueExists</span><span class="sxs-lookup"><span data-stu-id="c3671-3913">\_fValueExists</span></span>

<span data-ttu-id="c3671-3914">vType</span><span class="sxs-lookup"><span data-stu-id="c3671-3914">vType</span></span>

<span data-ttu-id="c3671-3915">vValue (Variable)</span><span class="sxs-lookup"><span data-stu-id="c3671-3915">vValue (variable)</span></span>



 

<span data-ttu-id="c3671-3916">**\_ cbValue:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtgröße in Bytes in vValue enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-3916">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="c3671-3917">**\_ fMoreExists:** Ein boolescher Wert, der angibt, ob zusätzliche CPMFetchValueOut-Meldungen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-3917">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="c3671-3918">Wenn 0x00000001 festgelegt ist, gibt es zusätzliche CPMFetchValueOut-Meldungen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3918">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="c3671-3919">Wenn 0x00000000 festgelegt ist, sind keine zusätzlichen CPMFetchValueOut-Meldungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c3671-3919">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="c3671-3920">**\_ fValueExists:** Ein boolescher Wert, der angibt, ob ein Wert für die Eigenschaft vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-3920">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="c3671-3921">Wenn 0x00000001 festgelegt ist, ist ein Wert für die Eigenschaft vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3921">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="c3671-3922">Wenn 0x00000000 festgelegt ist, ist kein Wert für die Eigenschaft vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c3671-3922">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="c3671-3923">**vType:** Ein Wert aus der VARENUM-Enumeration. Ausführliche Informationen zum Typ der Eigenschaft finden Sie in Abschnitt 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="c3671-3923">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="c3671-3924">**vValue:** Ein Teil eines Bytearrays, der eine SERIALIZEDPROPERTYVALUE-Struktur enthält, wie in Abschnitt 2.2.1.32 angegeben, wobei der Offset des Anfangs des Teils der Wert von \_ cbSoFar in CPMFetchValueIn ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-3924">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="c3671-3925">Die Länge des durch das cbValue-Feld angegebenen Teils \_ MUSS dem Wert von \_ cbChunk in CPMFetchValueIn entsprechen, wenn \_ fMoreExists auf 0x00000001 festgelegt ist, und MUSS andernfalls kleiner oder gleich dem Wert von \_ cbChunk sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-3925">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="c3671-3926">2.2.3.21 CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="c3671-3926">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="c3671-3927">Die CPMGetNotify-Nachricht fordert an, dass der Client über Rowsetänderungen benachrichtigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-3927">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="c3671-3928">Die Nachricht DARF KEINEN Text enthalten. nur der Nachrichtenheader gemäß Abschnitt 2.2.2 gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-3928">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="c3671-3929">2.2.3.22 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="c3671-3929">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="c3671-3930">Die CPMSendNotifyOut-Nachricht benachrichtigt den Client über eine Änderung an den Ergebnissen einer Abfrage.</span><span class="sxs-lookup"><span data-stu-id="c3671-3930">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="c3671-3931">Diese Meldung wird nur gesendet, wenn eine Änderung auftritt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3931">This message is only sent when a change occurs.</span></span> <span data-ttu-id="c3671-3932">Das Format der CPMSendNotifyOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3932">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="c3671-3933">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3933">0</span></span>

<span data-ttu-id="c3671-3934">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3934">1</span></span>

<span data-ttu-id="c3671-3935">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3935">2</span></span>

<span data-ttu-id="c3671-3936">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3936">3</span></span>

<span data-ttu-id="c3671-3937">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3937">4</span></span>

<span data-ttu-id="c3671-3938">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3938">5</span></span>

<span data-ttu-id="c3671-3939">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3939">6</span></span>

<span data-ttu-id="c3671-3940">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3940">7</span></span>

<span data-ttu-id="c3671-3941">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3941">8</span></span>

<span data-ttu-id="c3671-3942">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3942">9</span></span>

<span data-ttu-id="c3671-3943">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3943">1</span></span><br/> <span data-ttu-id="c3671-3944">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3944">0</span></span><br/>

<span data-ttu-id="c3671-3945">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3945">1</span></span>

<span data-ttu-id="c3671-3946">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3946">2</span></span>

<span data-ttu-id="c3671-3947">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3947">3</span></span>

<span data-ttu-id="c3671-3948">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3948">4</span></span>

<span data-ttu-id="c3671-3949">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3949">5</span></span>

<span data-ttu-id="c3671-3950">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3950">6</span></span>

<span data-ttu-id="c3671-3951">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3951">7</span></span>

<span data-ttu-id="c3671-3952">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3952">8</span></span>

<span data-ttu-id="c3671-3953">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3953">9</span></span>

<span data-ttu-id="c3671-3954">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3954">2</span></span><br/> <span data-ttu-id="c3671-3955">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3955">0</span></span><br/>

<span data-ttu-id="c3671-3956">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3956">1</span></span>

<span data-ttu-id="c3671-3957">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3957">2</span></span>

<span data-ttu-id="c3671-3958">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3958">3</span></span>

<span data-ttu-id="c3671-3959">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3959">4</span></span>

<span data-ttu-id="c3671-3960">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3960">5</span></span>

<span data-ttu-id="c3671-3961">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3961">6</span></span>

<span data-ttu-id="c3671-3962">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3962">7</span></span>

<span data-ttu-id="c3671-3963">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3963">8</span></span>

<span data-ttu-id="c3671-3964">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3964">9</span></span>

<span data-ttu-id="c3671-3965">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3965">3</span></span><br/> <span data-ttu-id="c3671-3966">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3966">0</span></span><br/>

<span data-ttu-id="c3671-3967">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3967">1</span></span>

<span data-ttu-id="c3671-3968">\_watchNotify</span><span class="sxs-lookup"><span data-stu-id="c3671-3968">\_watchNotify</span></span>



 

<span data-ttu-id="c3671-3969">**\_ watchNotify:** Die Änderung an der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="c3671-3969">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="c3671-3970">Es MUSS einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="c3671-3970">It MUST be one of the following values:</span></span>



| <span data-ttu-id="c3671-3971">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-3971">Value</span></span>                                     | <span data-ttu-id="c3671-3972">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-3972">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="c3671-3973">DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-3973">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="c3671-3974">Die Anzahl der Zeilen im Abfragerowset hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="c3671-3974">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="c3671-3975">DBWATCHNOTIFY \_ QUERYDONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-3975">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="c3671-3976">Die Abfrage wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c3671-3976">The query has completed.</span></span>                            |
| <span data-ttu-id="c3671-3977">DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-3977">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="c3671-3978">Die Abfrage wurde erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3671-3978">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="c3671-3979">2.2.3.23 CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="c3671-3979">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="c3671-3980">Die CPMGetApproximatePositionIn-Nachricht fordert die ungefähre Position eines Lesezeichens in einem Kapitel an.</span><span class="sxs-lookup"><span data-stu-id="c3671-3980">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="c3671-3981">Das Format der CPMGetApproximatePositionIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-3981">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="c3671-3982">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3982">0</span></span>

<span data-ttu-id="c3671-3983">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3983">1</span></span>

<span data-ttu-id="c3671-3984">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3984">2</span></span>

<span data-ttu-id="c3671-3985">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3985">3</span></span>

<span data-ttu-id="c3671-3986">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3986">4</span></span>

<span data-ttu-id="c3671-3987">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3987">5</span></span>

<span data-ttu-id="c3671-3988">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3988">6</span></span>

<span data-ttu-id="c3671-3989">7</span><span class="sxs-lookup"><span data-stu-id="c3671-3989">7</span></span>

<span data-ttu-id="c3671-3990">8</span><span class="sxs-lookup"><span data-stu-id="c3671-3990">8</span></span>

<span data-ttu-id="c3671-3991">9</span><span class="sxs-lookup"><span data-stu-id="c3671-3991">9</span></span>

<span data-ttu-id="c3671-3992">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3992">1</span></span><br/> <span data-ttu-id="c3671-3993">0</span><span class="sxs-lookup"><span data-stu-id="c3671-3993">0</span></span><br/>

<span data-ttu-id="c3671-3994">1</span><span class="sxs-lookup"><span data-stu-id="c3671-3994">1</span></span>

<span data-ttu-id="c3671-3995">2</span><span class="sxs-lookup"><span data-stu-id="c3671-3995">2</span></span>

<span data-ttu-id="c3671-3996">3</span><span class="sxs-lookup"><span data-stu-id="c3671-3996">3</span></span>

<span data-ttu-id="c3671-3997">4</span><span class="sxs-lookup"><span data-stu-id="c3671-3997">4</span></span>

<span data-ttu-id="c3671-3998">5</span><span class="sxs-lookup"><span data-stu-id="c3671-3998">5</span></span>

<span data-ttu-id="c3671-3999">6</span><span class="sxs-lookup"><span data-stu-id="c3671-3999">6</span></span>

<span data-ttu-id="c3671-4000">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4000">7</span></span>

<span data-ttu-id="c3671-4001">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4001">8</span></span>

<span data-ttu-id="c3671-4002">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4002">9</span></span>

<span data-ttu-id="c3671-4003">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4003">2</span></span><br/> <span data-ttu-id="c3671-4004">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4004">0</span></span><br/>

<span data-ttu-id="c3671-4005">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4005">1</span></span>

<span data-ttu-id="c3671-4006">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4006">2</span></span>

<span data-ttu-id="c3671-4007">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4007">3</span></span>

<span data-ttu-id="c3671-4008">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4008">4</span></span>

<span data-ttu-id="c3671-4009">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4009">5</span></span>

<span data-ttu-id="c3671-4010">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4010">6</span></span>

<span data-ttu-id="c3671-4011">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4011">7</span></span>

<span data-ttu-id="c3671-4012">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4012">8</span></span>

<span data-ttu-id="c3671-4013">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4013">9</span></span>

<span data-ttu-id="c3671-4014">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4014">3</span></span><br/> <span data-ttu-id="c3671-4015">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4015">0</span></span><br/>

<span data-ttu-id="c3671-4016">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4016">1</span></span>

<span data-ttu-id="c3671-4017">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="c3671-4017">\_hCursor</span></span>

<span data-ttu-id="c3671-4018">\_chapt</span><span class="sxs-lookup"><span data-stu-id="c3671-4018">\_chapt</span></span>

<span data-ttu-id="c3671-4019">\_bmk</span><span class="sxs-lookup"><span data-stu-id="c3671-4019">\_bmk</span></span>



 

<span data-ttu-id="c3671-4020">**\_ hCursor:** Ein 32-Bit-Wert, der den Abfragecursor darstellt, der aus CPMCreateQueryOut für das Rowset abgerufen wurde, das das Lesezeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-4020">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="c3671-4021">**\_ chapt:** Ein 32-Bit-Wert, der das Handle für das Kapitel darstellt, das das Lesezeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-4021">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="c3671-4022">**\_ bmk:** Ein 32-Bit-Wert, der das Handle für das Lesezeichen darstellt, für das die ungefähre Position abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-4022">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="c3671-4023">2.2.3.24 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="c3671-4023">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="c3671-4024">Die CPMGetApproximatePositionOut-Nachricht antwortet auf eine CPMGetApproximatePositionIn-Nachricht, die die ungefähre Position des Lesezeichens im Kapitel beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4024">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="c3671-4025">Das Format der CPMGetApproximatePositionOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4025">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="c3671-4026">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4026">0</span></span>

<span data-ttu-id="c3671-4027">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4027">1</span></span>

<span data-ttu-id="c3671-4028">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4028">2</span></span>

<span data-ttu-id="c3671-4029">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4029">3</span></span>

<span data-ttu-id="c3671-4030">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4030">4</span></span>

<span data-ttu-id="c3671-4031">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4031">5</span></span>

<span data-ttu-id="c3671-4032">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4032">6</span></span>

<span data-ttu-id="c3671-4033">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4033">7</span></span>

<span data-ttu-id="c3671-4034">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4034">8</span></span>

<span data-ttu-id="c3671-4035">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4035">9</span></span>

<span data-ttu-id="c3671-4036">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4036">1</span></span><br/> <span data-ttu-id="c3671-4037">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4037">0</span></span><br/>

<span data-ttu-id="c3671-4038">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4038">1</span></span>

<span data-ttu-id="c3671-4039">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4039">2</span></span>

<span data-ttu-id="c3671-4040">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4040">3</span></span>

<span data-ttu-id="c3671-4041">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4041">4</span></span>

<span data-ttu-id="c3671-4042">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4042">5</span></span>

<span data-ttu-id="c3671-4043">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4043">6</span></span>

<span data-ttu-id="c3671-4044">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4044">7</span></span>

<span data-ttu-id="c3671-4045">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4045">8</span></span>

<span data-ttu-id="c3671-4046">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4046">9</span></span>

<span data-ttu-id="c3671-4047">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4047">2</span></span><br/> <span data-ttu-id="c3671-4048">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4048">0</span></span><br/>

<span data-ttu-id="c3671-4049">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4049">1</span></span>

<span data-ttu-id="c3671-4050">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4050">2</span></span>

<span data-ttu-id="c3671-4051">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4051">3</span></span>

<span data-ttu-id="c3671-4052">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4052">4</span></span>

<span data-ttu-id="c3671-4053">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4053">5</span></span>

<span data-ttu-id="c3671-4054">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4054">6</span></span>

<span data-ttu-id="c3671-4055">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4055">7</span></span>

<span data-ttu-id="c3671-4056">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4056">8</span></span>

<span data-ttu-id="c3671-4057">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4057">9</span></span>

<span data-ttu-id="c3671-4058">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4058">3</span></span><br/> <span data-ttu-id="c3671-4059">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4059">0</span></span><br/>

<span data-ttu-id="c3671-4060">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4060">1</span></span>

<span data-ttu-id="c3671-4061">\_Dividend</span><span class="sxs-lookup"><span data-stu-id="c3671-4061">\_numerator</span></span>

<span data-ttu-id="c3671-4062">\_Divisor</span><span class="sxs-lookup"><span data-stu-id="c3671-4062">\_denominator</span></span>



 

<span data-ttu-id="c3671-4063">**\_ numerator:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Zeilennummer des Lesezeichens im Rowset enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-4063">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="c3671-4064">Wenn keine Zeilen vorhanden sind, MUSS dieses Feld auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3671-4064">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="c3671-4065">**\_ Nenner:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeilen im Rowset enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-4065">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="c3671-4066">2.2.3.25 CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="c3671-4066">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="c3671-4067">Die CPMCompareBmkIn-Nachricht fordert einen Vergleich zweier Lesezeichen in einem Kapitel an.</span><span class="sxs-lookup"><span data-stu-id="c3671-4067">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="c3671-4068">Das Format der CPMCompareBmkIn-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="c3671-4068">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="c3671-4069">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4069">0</span></span>

<span data-ttu-id="c3671-4070">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4070">1</span></span>

<span data-ttu-id="c3671-4071">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4071">2</span></span>

<span data-ttu-id="c3671-4072">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4072">3</span></span>

<span data-ttu-id="c3671-4073">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4073">4</span></span>

<span data-ttu-id="c3671-4074">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4074">5</span></span>

<span data-ttu-id="c3671-4075">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4075">6</span></span>

<span data-ttu-id="c3671-4076">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4076">7</span></span>

<span data-ttu-id="c3671-4077">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4077">8</span></span>

<span data-ttu-id="c3671-4078">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4078">9</span></span>

<span data-ttu-id="c3671-4079">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4079">1</span></span><br/> <span data-ttu-id="c3671-4080">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4080">0</span></span><br/>

<span data-ttu-id="c3671-4081">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4081">1</span></span>

<span data-ttu-id="c3671-4082">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4082">2</span></span>

<span data-ttu-id="c3671-4083">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4083">3</span></span>

<span data-ttu-id="c3671-4084">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4084">4</span></span>

<span data-ttu-id="c3671-4085">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4085">5</span></span>

<span data-ttu-id="c3671-4086">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4086">6</span></span>

<span data-ttu-id="c3671-4087">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4087">7</span></span>

<span data-ttu-id="c3671-4088">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4088">8</span></span>

<span data-ttu-id="c3671-4089">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4089">9</span></span>

<span data-ttu-id="c3671-4090">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4090">2</span></span><br/> <span data-ttu-id="c3671-4091">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4091">0</span></span><br/>

<span data-ttu-id="c3671-4092">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4092">1</span></span>

<span data-ttu-id="c3671-4093">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4093">2</span></span>

<span data-ttu-id="c3671-4094">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4094">3</span></span>

<span data-ttu-id="c3671-4095">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4095">4</span></span>

<span data-ttu-id="c3671-4096">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4096">5</span></span>

<span data-ttu-id="c3671-4097">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4097">6</span></span>

<span data-ttu-id="c3671-4098">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4098">7</span></span>

<span data-ttu-id="c3671-4099">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4099">8</span></span>

<span data-ttu-id="c3671-4100">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4100">9</span></span>

<span data-ttu-id="c3671-4101">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4101">3</span></span><br/> <span data-ttu-id="c3671-4102">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4102">0</span></span><br/>

<span data-ttu-id="c3671-4103">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4103">1</span></span>

<span data-ttu-id="c3671-4104">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="c3671-4104">\_hCursor</span></span>

<span data-ttu-id="c3671-4105">\_chapt</span><span class="sxs-lookup"><span data-stu-id="c3671-4105">\_chapt</span></span>

<span data-ttu-id="c3671-4106">\_bmkFirst</span><span class="sxs-lookup"><span data-stu-id="c3671-4106">\_bmkFirst</span></span>

<span data-ttu-id="c3671-4107">\_bmkSecond</span><span class="sxs-lookup"><span data-stu-id="c3671-4107">\_bmkSecond</span></span>



 

<span data-ttu-id="c3671-4108">\_**hCursor:** Ein 32-Bit-Wert, der das Handle der CPMCreateQueryOut-Nachricht für das Rowset darstellt, das die Lesezeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-4108">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="c3671-4109">\_**chapt:** Ein 32-Bit-Wert, der das Handle des Kapitels darstellt, das die zu vergleichenden Lesezeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-4109">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="c3671-4110">\_**bmkFirst:** Ein 32-Bit-Wert, der das Handle für das erste zu vergleichende Lesezeichen darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4110">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="c3671-4111">\_**bmkSecond:** Ein 32-Bit-Wert, der das Handle für das zweite zu vergleichende Lesezeichen darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4111">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="c3671-4112">2.2.3.26 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="c3671-4112">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="c3671-4113">Die CPMCompareBmkOut-Nachricht antwortet auf eine CPMCompareBmkIn-Nachricht mit dem Vergleich der beiden Lesezeichen im Kapitel.</span><span class="sxs-lookup"><span data-stu-id="c3671-4113">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="c3671-4114">Das Format der CPMCompareBmkOut-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="c3671-4114">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="c3671-4115">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4115">0</span></span>

<span data-ttu-id="c3671-4116">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4116">1</span></span>

<span data-ttu-id="c3671-4117">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4117">2</span></span>

<span data-ttu-id="c3671-4118">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4118">3</span></span>

<span data-ttu-id="c3671-4119">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4119">4</span></span>

<span data-ttu-id="c3671-4120">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4120">5</span></span>

<span data-ttu-id="c3671-4121">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4121">6</span></span>

<span data-ttu-id="c3671-4122">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4122">7</span></span>

<span data-ttu-id="c3671-4123">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4123">8</span></span>

<span data-ttu-id="c3671-4124">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4124">9</span></span>

<span data-ttu-id="c3671-4125">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4125">1</span></span><br/> <span data-ttu-id="c3671-4126">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4126">0</span></span><br/>

<span data-ttu-id="c3671-4127">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4127">1</span></span>

<span data-ttu-id="c3671-4128">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4128">2</span></span>

<span data-ttu-id="c3671-4129">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4129">3</span></span>

<span data-ttu-id="c3671-4130">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4130">4</span></span>

<span data-ttu-id="c3671-4131">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4131">5</span></span>

<span data-ttu-id="c3671-4132">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4132">6</span></span>

<span data-ttu-id="c3671-4133">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4133">7</span></span>

<span data-ttu-id="c3671-4134">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4134">8</span></span>

<span data-ttu-id="c3671-4135">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4135">9</span></span>

<span data-ttu-id="c3671-4136">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4136">2</span></span><br/> <span data-ttu-id="c3671-4137">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4137">0</span></span><br/>

<span data-ttu-id="c3671-4138">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4138">1</span></span>

<span data-ttu-id="c3671-4139">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4139">2</span></span>

<span data-ttu-id="c3671-4140">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4140">3</span></span>

<span data-ttu-id="c3671-4141">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4141">4</span></span>

<span data-ttu-id="c3671-4142">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4142">5</span></span>

<span data-ttu-id="c3671-4143">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4143">6</span></span>

<span data-ttu-id="c3671-4144">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4144">7</span></span>

<span data-ttu-id="c3671-4145">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4145">8</span></span>

<span data-ttu-id="c3671-4146">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4146">9</span></span>

<span data-ttu-id="c3671-4147">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4147">3</span></span><br/> <span data-ttu-id="c3671-4148">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4148">0</span></span><br/>

<span data-ttu-id="c3671-4149">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4149">1</span></span>

<span data-ttu-id="c3671-4150">\_dwComparison</span><span class="sxs-lookup"><span data-stu-id="c3671-4150">\_dwComparison</span></span>



 

<span data-ttu-id="c3671-4151">\_**dwComparison:** Einer der folgenden Werte, der die relativen Positionen der beiden Lesezeichen im Kapitel angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4151">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="c3671-4152">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-4152">Value</span></span>                               | <span data-ttu-id="c3671-4153">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-4153">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="c3671-4154">DBCOMPARE \_ LT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-4154">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="c3671-4155">Das erste Lesezeichen wird vor dem zweiten positioniert.</span><span class="sxs-lookup"><span data-stu-id="c3671-4155">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="c3671-4156">DBCOMPARE \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3671-4156">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="c3671-4157">Das erste Lesezeichen hat die gleiche Position wie das zweite.</span><span class="sxs-lookup"><span data-stu-id="c3671-4157">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="c3671-4158">DBCOMPARE \_ GT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3671-4158">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="c3671-4159">Das erste Lesezeichen wird nach dem zweiten positioniert.</span><span class="sxs-lookup"><span data-stu-id="c3671-4159">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="c3671-4160">DBCOMPARE \_ NE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3671-4160">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="c3671-4161">Das erste Lesezeichen hat nicht die gleiche Position wie das zweite.</span><span class="sxs-lookup"><span data-stu-id="c3671-4161">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="c3671-4162">DBCOMPARE \_ NOTCOMPARABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3671-4162">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="c3671-4163">Das erste Lesezeichen ist nicht mit dem zweiten vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="c3671-4163">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="c3671-4164">2.2.3.27 CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="c3671-4164">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="c3671-4165">Die CPMRestartPositionIn-Nachricht verschiebt die Abrufposition für einen Cursor an den Anfang des Kapitels.</span><span class="sxs-lookup"><span data-stu-id="c3671-4165">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="c3671-4166">Wie in Abschnitt 3.1.5.2.12 angegeben, antworte der Server mit der gleichen Meldung, wobei die Ergebnisse der Anforderung im \_ Statusfeld des CISP-Headers enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-4166">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="c3671-4167">Das Format der CPMRestartPositionIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4167">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="c3671-4168">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4168">0</span></span>

<span data-ttu-id="c3671-4169">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4169">1</span></span>

<span data-ttu-id="c3671-4170">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4170">2</span></span>

<span data-ttu-id="c3671-4171">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4171">3</span></span>

<span data-ttu-id="c3671-4172">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4172">4</span></span>

<span data-ttu-id="c3671-4173">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4173">5</span></span>

<span data-ttu-id="c3671-4174">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4174">6</span></span>

<span data-ttu-id="c3671-4175">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4175">7</span></span>

<span data-ttu-id="c3671-4176">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4176">8</span></span>

<span data-ttu-id="c3671-4177">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4177">9</span></span>

<span data-ttu-id="c3671-4178">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4178">1</span></span><br/> <span data-ttu-id="c3671-4179">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4179">0</span></span><br/>

<span data-ttu-id="c3671-4180">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4180">1</span></span>

<span data-ttu-id="c3671-4181">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4181">2</span></span>

<span data-ttu-id="c3671-4182">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4182">3</span></span>

<span data-ttu-id="c3671-4183">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4183">4</span></span>

<span data-ttu-id="c3671-4184">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4184">5</span></span>

<span data-ttu-id="c3671-4185">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4185">6</span></span>

<span data-ttu-id="c3671-4186">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4186">7</span></span>

<span data-ttu-id="c3671-4187">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4187">8</span></span>

<span data-ttu-id="c3671-4188">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4188">9</span></span>

<span data-ttu-id="c3671-4189">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4189">2</span></span><br/> <span data-ttu-id="c3671-4190">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4190">0</span></span><br/>

<span data-ttu-id="c3671-4191">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4191">1</span></span>

<span data-ttu-id="c3671-4192">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4192">2</span></span>

<span data-ttu-id="c3671-4193">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4193">3</span></span>

<span data-ttu-id="c3671-4194">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4194">4</span></span>

<span data-ttu-id="c3671-4195">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4195">5</span></span>

<span data-ttu-id="c3671-4196">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4196">6</span></span>

<span data-ttu-id="c3671-4197">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4197">7</span></span>

<span data-ttu-id="c3671-4198">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4198">8</span></span>

<span data-ttu-id="c3671-4199">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4199">9</span></span>

<span data-ttu-id="c3671-4200">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4200">3</span></span><br/> <span data-ttu-id="c3671-4201">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4201">0</span></span><br/>

<span data-ttu-id="c3671-4202">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4202">1</span></span>

<span data-ttu-id="c3671-4203">\_hCursor (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-4203">\_hCursor (optional)</span></span>

<span data-ttu-id="c3671-4204">\_chapt (optional)</span><span class="sxs-lookup"><span data-stu-id="c3671-4204">\_chapt (optional)</span></span>



 

<span data-ttu-id="c3671-4205">**\_ hCursor:** Ein 32-Bit-Wert, der das Handle darstellt, das aus einer CPMCreateQueryOut-Nachricht abgerufen wurde und die Abfrage identifiziert, für die die Position neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-4205">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="c3671-4206">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-4206">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="c3671-4207">**\_ chapt:** Ein 32-Bit-Wert, der das Handle eines Kapitels darstellt, aus dem Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4207">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="c3671-4208">Dieses Feld MUSS vorhanden sein, wenn die Nachricht vom Client gesendet wird, und MUSS nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-4208">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="c3671-4209">2.2.3.28 CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="c3671-4209">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="c3671-4210">Die CPMFreeCursorIn-Nachricht fordert die Freigabe eines Cursors an.</span><span class="sxs-lookup"><span data-stu-id="c3671-4210">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="c3671-4211">Das Format der CPMFreeCursorIn-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4211">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="c3671-4212">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4212">0</span></span>

<span data-ttu-id="c3671-4213">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4213">1</span></span>

<span data-ttu-id="c3671-4214">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4214">2</span></span>

<span data-ttu-id="c3671-4215">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4215">3</span></span>

<span data-ttu-id="c3671-4216">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4216">4</span></span>

<span data-ttu-id="c3671-4217">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4217">5</span></span>

<span data-ttu-id="c3671-4218">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4218">6</span></span>

<span data-ttu-id="c3671-4219">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4219">7</span></span>

<span data-ttu-id="c3671-4220">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4220">8</span></span>

<span data-ttu-id="c3671-4221">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4221">9</span></span>

<span data-ttu-id="c3671-4222">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4222">1</span></span><br/> <span data-ttu-id="c3671-4223">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4223">0</span></span><br/>

<span data-ttu-id="c3671-4224">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4224">1</span></span>

<span data-ttu-id="c3671-4225">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4225">2</span></span>

<span data-ttu-id="c3671-4226">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4226">3</span></span>

<span data-ttu-id="c3671-4227">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4227">4</span></span>

<span data-ttu-id="c3671-4228">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4228">5</span></span>

<span data-ttu-id="c3671-4229">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4229">6</span></span>

<span data-ttu-id="c3671-4230">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4230">7</span></span>

<span data-ttu-id="c3671-4231">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4231">8</span></span>

<span data-ttu-id="c3671-4232">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4232">9</span></span>

<span data-ttu-id="c3671-4233">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4233">2</span></span><br/> <span data-ttu-id="c3671-4234">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4234">0</span></span><br/>

<span data-ttu-id="c3671-4235">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4235">1</span></span>

<span data-ttu-id="c3671-4236">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4236">2</span></span>

<span data-ttu-id="c3671-4237">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4237">3</span></span>

<span data-ttu-id="c3671-4238">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4238">4</span></span>

<span data-ttu-id="c3671-4239">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4239">5</span></span>

<span data-ttu-id="c3671-4240">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4240">6</span></span>

<span data-ttu-id="c3671-4241">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4241">7</span></span>

<span data-ttu-id="c3671-4242">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4242">8</span></span>

<span data-ttu-id="c3671-4243">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4243">9</span></span>

<span data-ttu-id="c3671-4244">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4244">3</span></span><br/> <span data-ttu-id="c3671-4245">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4245">0</span></span><br/>

<span data-ttu-id="c3671-4246">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4246">1</span></span>

<span data-ttu-id="c3671-4247">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="c3671-4247">\_hCursor</span></span>



 

<span data-ttu-id="c3671-4248">**\_ hCursor:** Ein 32-Bit-Wert, der das Handle des Cursors aus der freizugebenden CPMCreateQueryOut-Nachricht darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4248">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="c3671-4249">2.2.3.29 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="c3671-4249">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="c3671-4250">Die CPMFreeCursorOut-Nachricht antwortet auf eine CPMFreeCursorIn-Nachricht mit den Ergebnissen der Freigabe eines Cursors.</span><span class="sxs-lookup"><span data-stu-id="c3671-4250">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="c3671-4251">Das Format der CPMFreeCursorOut-Nachricht, die dem Header folgt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4251">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="c3671-4252">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4252">0</span></span>

<span data-ttu-id="c3671-4253">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4253">1</span></span>

<span data-ttu-id="c3671-4254">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4254">2</span></span>

<span data-ttu-id="c3671-4255">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4255">3</span></span>

<span data-ttu-id="c3671-4256">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4256">4</span></span>

<span data-ttu-id="c3671-4257">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4257">5</span></span>

<span data-ttu-id="c3671-4258">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4258">6</span></span>

<span data-ttu-id="c3671-4259">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4259">7</span></span>

<span data-ttu-id="c3671-4260">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4260">8</span></span>

<span data-ttu-id="c3671-4261">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4261">9</span></span>

<span data-ttu-id="c3671-4262">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4262">1</span></span><br/> <span data-ttu-id="c3671-4263">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4263">0</span></span><br/>

<span data-ttu-id="c3671-4264">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4264">1</span></span>

<span data-ttu-id="c3671-4265">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4265">2</span></span>

<span data-ttu-id="c3671-4266">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4266">3</span></span>

<span data-ttu-id="c3671-4267">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4267">4</span></span>

<span data-ttu-id="c3671-4268">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4268">5</span></span>

<span data-ttu-id="c3671-4269">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4269">6</span></span>

<span data-ttu-id="c3671-4270">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4270">7</span></span>

<span data-ttu-id="c3671-4271">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4271">8</span></span>

<span data-ttu-id="c3671-4272">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4272">9</span></span>

<span data-ttu-id="c3671-4273">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4273">2</span></span><br/> <span data-ttu-id="c3671-4274">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4274">0</span></span><br/>

<span data-ttu-id="c3671-4275">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4275">1</span></span>

<span data-ttu-id="c3671-4276">2</span><span class="sxs-lookup"><span data-stu-id="c3671-4276">2</span></span>

<span data-ttu-id="c3671-4277">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4277">3</span></span>

<span data-ttu-id="c3671-4278">4</span><span class="sxs-lookup"><span data-stu-id="c3671-4278">4</span></span>

<span data-ttu-id="c3671-4279">5</span><span class="sxs-lookup"><span data-stu-id="c3671-4279">5</span></span>

<span data-ttu-id="c3671-4280">6</span><span class="sxs-lookup"><span data-stu-id="c3671-4280">6</span></span>

<span data-ttu-id="c3671-4281">7</span><span class="sxs-lookup"><span data-stu-id="c3671-4281">7</span></span>

<span data-ttu-id="c3671-4282">8</span><span class="sxs-lookup"><span data-stu-id="c3671-4282">8</span></span>

<span data-ttu-id="c3671-4283">9</span><span class="sxs-lookup"><span data-stu-id="c3671-4283">9</span></span>

<span data-ttu-id="c3671-4284">3</span><span class="sxs-lookup"><span data-stu-id="c3671-4284">3</span></span><br/> <span data-ttu-id="c3671-4285">0</span><span class="sxs-lookup"><span data-stu-id="c3671-4285">0</span></span><br/>

<span data-ttu-id="c3671-4286">1</span><span class="sxs-lookup"><span data-stu-id="c3671-4286">1</span></span>

<span data-ttu-id="c3671-4287">\_cCursorsRemaining</span><span class="sxs-lookup"><span data-stu-id="c3671-4287">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="c3671-4288">**\_ cCursorsRemaining:** Eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der cursors angibt, die noch für die Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4288">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="c3671-4289">2.2.3.30 CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="c3671-4289">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="c3671-4290">Die CPMDisconnect-Nachricht beendet die Verbindung mit dem Server.</span><span class="sxs-lookup"><span data-stu-id="c3671-4290">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="c3671-4291">Die Nachricht DARF KEINEN Text enthalten. nur der Nachrichtenheader gemäß Abschnitt 2.2.2 gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-4291">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="c3671-4292">2.2.4 Fehler</span><span class="sxs-lookup"><span data-stu-id="c3671-4292">2.2.4 Errors</span></span>

<span data-ttu-id="c3671-4293">Alle Content Indexing Service Protocol-Meldungen MÜSSEN bei Erfolg 0x00000000 zurückgeben. Andernfalls geben sie einen 32-Bit-Fehlercode ungleich 0 (null) zurück, der entweder ein HRESULT- oder ein NTSTATUS-Wert sein kann (siehe Abschnitt 1.8).</span><span class="sxs-lookup"><span data-stu-id="c3671-4293">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="c3671-4294">Wenn ein Puffer zu klein für ein Ergebnis ist, MUSS der Statuscode STATUS \_ INSUFFICIENT \_ RESOURCES (0xC0000009A) zurückgegeben werden, und der fehlerhafte Vorgang sollte mit einem größeren Puffer wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4294">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="c3671-4295">Alle anderen Fehlerwerte MÜSSEN gleich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4295">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="c3671-4296">(Beachten Sie, dass sich die Nummerierungsräume HRESULT und NTSTATUS derzeit nur mit Werten mit identischer Bedeutung überschneiden. Selbst wenn sie in Zukunft konflikteig sein sollten, würde dies keine Protokollprobleme verursachen, solange der Wert für STATUS \_ INSUFFICIENT \_ RESOURCES bleibt eindeutig, da alle anderen Fehlerwerte gleich behandelt werden.)</span><span class="sxs-lookup"><span data-stu-id="c3671-4296">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="c3671-4297">3 Protokolldetails</span><span class="sxs-lookup"><span data-stu-id="c3671-4297">3 Protocol Details</span></span>

-   [<span data-ttu-id="c3671-4298">3.1 Serverdetails</span><span class="sxs-lookup"><span data-stu-id="c3671-4298">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="c3671-4299">3.2 Clientdetails</span><span class="sxs-lookup"><span data-stu-id="c3671-4299">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="c3671-4300">CISP-Nachrichtenanforderungen zum Remoteabfragen der Indizierungsdienstkataloge erfordern keine bestimmte Sequenz.</span><span class="sxs-lookup"><span data-stu-id="c3671-4300">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="c3671-4301">Es wird jedoch empfohlen, dass die höhere Ebene einer sinnvollen Nachrichtensequenz folgt, da der Server bei Nachrichten, die aus dieser Sequenz oder mit ungültigen Daten empfangen werden, mit einem Fehler antwortet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4301">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="c3671-4302">Einige Nachrichten sind auch von der höheren Ebene abhängig, die gültige Daten bereitstellt, die in Früheren Nachrichten in der Sequenz empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4302">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="c3671-4303">Eine typische Nachrichtensequenz für eine einfache Abfrage von einem Client an einen Remotecomputer ist im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4303">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![Nachrichtensequenz für einfache Abfragen](images/protocoldetails.jpg)

<span data-ttu-id="c3671-4305">Die im vorherigen Diagramm dargestellten Nachrichten stellen eine Teilmenge aller CISP-Nachrichten dar, die zum Abfragen eines Remoteindizierungsdienstkatalogs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4305">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="c3671-4306">3.1 Serverdetails</span><span class="sxs-lookup"><span data-stu-id="c3671-4306">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="c3671-4307">3.1.1 Abstraktes Datenmodell</span><span class="sxs-lookup"><span data-stu-id="c3671-4307">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="c3671-4308">Im folgenden Abschnitt werden Daten und der Zustand angegeben, die vom CISP-Server verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4308">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="c3671-4309">Die hier bereitgestellten Daten sollen die Erklärung des Verhaltens des Protokolls erleichtern.</span><span class="sxs-lookup"><span data-stu-id="c3671-4309">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="c3671-4310">In diesem Abschnitt wird nicht vorausgesetzt, dass Implementierungen diesem Modell entsprechen, solange ihr externes Verhalten mit dem in diesem Dokument beschriebenen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4310">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="c3671-4311">Ein Indizierungsdienst, der CISP implementiert, MUSS die folgenden abstrakten Datenelemente verwalten:</span><span class="sxs-lookup"><span data-stu-id="c3671-4311">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="c3671-4312">Die Liste der Clients, die mit dem Server verbunden sind</span><span class="sxs-lookup"><span data-stu-id="c3671-4312">The list of clients connected to the server</span></span>
-   <span data-ttu-id="c3671-4313">Informationen zu jedem Client, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="c3671-4313">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="c3671-4314">Clientversion (wie in der IN Abschnitt 2.2.3.6 angegebenen CPMConnectIn-Nachricht angegeben)</span><span class="sxs-lookup"><span data-stu-id="c3671-4314">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="c3671-4315">Katalog, der dem Client zugeordnet ist (durch eine CPMConnectIn-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="c3671-4315">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="c3671-4316">Zusätzliche Clienteigenschaften, wie in Abschnitt 2.2.1.21.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-4316">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="c3671-4317">Suchabfrage des Clients</span><span class="sxs-lookup"><span data-stu-id="c3671-4317">Client's search query</span></span>
    -   <span data-ttu-id="c3671-4318">Liste der Cursorhandles für die Abfrage und Position im Resultset für jedes Handle.</span><span class="sxs-lookup"><span data-stu-id="c3671-4318">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="c3671-4319">Aktueller Satz von Bindungen</span><span class="sxs-lookup"><span data-stu-id="c3671-4319">Current set of bindings</span></span>
    -   <span data-ttu-id="c3671-4320">Aktueller Status der Abfrage, der (für jeden Cursor) enthält:</span><span class="sxs-lookup"><span data-stu-id="c3671-4320">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="c3671-4321">Anzahl der Zeilen im Abfrageergebnis</span><span class="sxs-lookup"><span data-stu-id="c3671-4321">Number of rows in query result</span></span>
        -   <span data-ttu-id="c3671-4322">Zähler und Nenner des Abfrageabschlusses</span><span class="sxs-lookup"><span data-stu-id="c3671-4322">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="c3671-4323">Letzte Anzahl von Zeilen, die von der letzten CPMRatioFinishedOut-Meldung für diesen Cursor gemeldet wurden</span><span class="sxs-lookup"><span data-stu-id="c3671-4323">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="c3671-4324">Gibt an, ob die Abfrage vom Server auf Änderungen der Abfrageergebnisse überwacht wird und ob sie überwacht wird, welche Änderungen in den Abfrageergebnissen seit der letzten Clientmeldung durch CPMSendNotifyOut vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4324">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="c3671-4325">Liste der Kapitelhandles, die von dieser Abfrage an einen Client verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4325">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="c3671-4326">Liste der Lesezeichenhandles für jeden Cursor, die von dieser Abfrage an einen Client bedient werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4326">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="c3671-4327">Der aktuelle Status des Indizierungsdiensts, der möglicherweise "nicht initialisiert", "wird ausgeführt" oder "heruntergefahren" ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4327">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="c3671-4328">Beachten Sie, dass sich der Server größtenteils im Status "Wird ausgeführt" befindet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4328">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="c3671-4329">Im Folgenden ist das Zustandsautomatendiagramm für den Server dargestellt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4329">Following is the state machine diagram for the server:</span></span>

    ![Zustandsautomatendiagramm des Indizierungsdienstservers](images/abstractdatamodel.jpg)

-   <span data-ttu-id="c3671-4331">Katalogspezifische Informationen: Anzahl indizierter Dokumente, Indexgröße, Anzahl eindeutiger Schlüssel usw. (eine vollständige Liste finden Sie in Abschnitt 2.2.3.1), Status (entspricht den Werten von dwNewState in Abschnitt 2.2.3.2).</span><span class="sxs-lookup"><span data-stu-id="c3671-4331">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="c3671-4332">Für jede unterstützte Sprache eine Datenbank mit Wortvariationen, wie in Abschnitt 2.2.1.3 erläutert.</span><span class="sxs-lookup"><span data-stu-id="c3671-4332">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="c3671-4333">3.1.2 Zeitgeber</span><span class="sxs-lookup"><span data-stu-id="c3671-4333">3.1.2 Timers</span></span>

<span data-ttu-id="c3671-4334">Es sind keine Protokollzeiter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c3671-4334">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="c3671-4335">3.1.3 Initialisierung</span><span class="sxs-lookup"><span data-stu-id="c3671-4335">3.1.3 Initialization</span></span>

<span data-ttu-id="c3671-4336">Nach der Initialisierung MUSS der Server seinen Zustand auf "nicht initialisiert" festlegen und mit dem Lauschen auf Nachrichten in der in Abschnitt 1.9 angegebenen Named Pipe beginnen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4336">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="c3671-4337">Nach jeder anderen internen Initialisierung MUSS sie in den Zustand "Wird ausgeführt" überwechseln.</span><span class="sxs-lookup"><span data-stu-id="c3671-4337">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="c3671-4338">3.1.4 Ausgelöste Ereignisse auf höherer Ebene</span><span class="sxs-lookup"><span data-stu-id="c3671-4338">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="c3671-4339">Keine.</span><span class="sxs-lookup"><span data-stu-id="c3671-4339">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="c3671-4340">3.1.5 Nachrichtenverarbeitungs- und Sequenzierungsregeln</span><span class="sxs-lookup"><span data-stu-id="c3671-4340">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="c3671-4341">Wenn während der Verarbeitung einer von einem Client gesendeten Nachricht ein Fehler auftritt, MUSS der Server wie folgt einen Fehler an den Client melden:</span><span class="sxs-lookup"><span data-stu-id="c3671-4341">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="c3671-4342">Beenden der Verarbeitung der vom Client gesendeten Nachricht</span><span class="sxs-lookup"><span data-stu-id="c3671-4342">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="c3671-4343">Antworten Sie mit dem Nachrichtenheader (nur) der vom Client gesendeten Nachricht, und behalten Sie \_ dabei das msg-Feld bei.</span><span class="sxs-lookup"><span data-stu-id="c3671-4343">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="c3671-4344">Legen Sie \_ das Statusfeld auf den Fehlercodewert fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-4344">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="c3671-4345">Wenn eine Nachricht eintrifft, MUSS der Server den Msg-Feldwert überprüfen, um zu überprüfen, ob es sich um einen bekannten Typ handelt \_ (siehe Abschnitt 2.2.2).</span><span class="sxs-lookup"><span data-stu-id="c3671-4345">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="c3671-4346">Wenn der Typ nicht bekannt ist, MUSS er den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4346">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="c3671-4347">Der Server MUSS dann den \_ Feldwert ulChecksum überprüfen, wenn der Nachrichtentyp einer der folgenden ist:</span><span class="sxs-lookup"><span data-stu-id="c3671-4347">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="c3671-4348">CPMConnectIn (0x000000C8)</span><span class="sxs-lookup"><span data-stu-id="c3671-4348">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="c3671-4349">CPMCreateQueryIn (0x000000CA)</span><span class="sxs-lookup"><span data-stu-id="c3671-4349">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="c3671-4350">CPMSetBindingsIn (0x000000D0)</span><span class="sxs-lookup"><span data-stu-id="c3671-4350">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="c3671-4351">CPMGetRowsIn (0x000000CC)</span><span class="sxs-lookup"><span data-stu-id="c3671-4351">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="c3671-4352">CPMFetchValueIn (0x000000E4)</span><span class="sxs-lookup"><span data-stu-id="c3671-4352">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="c3671-4353">Um den ulChecksum-Feldwert zu überprüfen, MUSS der Server den Wert überprüfen, den der Client \_ im \_ Feld iClientVersion in der CPMConnectIn-Nachricht angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="c3671-4353">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="c3671-4354">Wenn das Feld iClientVersion nicht auf 0x00000008 und das feld ulChecksum nicht auf 0x00000000 festgelegt ist, MUSS der Server einen \_ \_ STATUS INVALID PARAMETER \_ \_ (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4354">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="c3671-4355">Server MUST NOT validate the \_ ulChecksum field for clients the set the \_ iClientVersion field to a value less than 0x00000008.</span><span class="sxs-lookup"><span data-stu-id="c3671-4355">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="c3671-4356">Wenn der Feldwert iClientVersionfield 0x00000008 ist, MUSS der Server überprüfen, ob das feld ulChecksum wie in Abschnitt \_ \_ 3.2.4 angegeben berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="c3671-4356">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="c3671-4357">Wenn der \_ ulChecksum-Wert ungültig ist, MUSS der Server den Fehler STATUS \_ INVALID PARAMETER \_ (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4357">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="c3671-4358">Als Nächstes überprüft der Server, in welchem Zustand er sich befindet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4358">Next, the server checks which state is it in.</span></span> <span data-ttu-id="c3671-4359">Wenn der Status "nicht initialisiert" ist, MUSS der Server einen CI \_ E \_ NOT \_ INITIALIZED(0x8004180B)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4359">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="c3671-4360">Wenn der Status "heruntergefahren" ist, MUSS der Server einen CI \_ E \_ SHUTDOWN-Fehler (0x80041812 melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4360">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="c3671-4361">Sobald ein Header als gültig festgelegt wurde und sich der Server im Status "Wird ausgeführt" befing, MUSS eine weitere nachrichtenspezifische Verarbeitung erfolgen, wie in den folgenden Unterabschnitten angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-4361">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="c3671-4362">3.1.5.1 Katalogverwaltung des Remoteindizierungsdiensts</span><span class="sxs-lookup"><span data-stu-id="c3671-4362">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="c3671-4363">3.1.5.1.1 Empfangen einer CPMCiStateInOut-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4363">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="c3671-4364">Wenn der Server eine CPMCIStateInOut-Nachrichtenanforderung vom Client empfängt, MUSS der Server zunächst überprüfen, ob sich der Client in einer Liste verbundener Clients befindet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4364">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="c3671-4365">Wenn der Client nicht in der Liste enthalten ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4365">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="c3671-4366">Andernfalls MUSS er dem Client mit einer CPMCIStateInOut-Nachricht antworten und diese mit Informationen zum zugeordneten Katalog des Clients auffüllen, wie in Abschnitt 2.2.3.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-4366">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="c3671-4367">3.1.5.1.2 Empfangen einer CPMSetCatStateIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4367">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="c3671-4368">Wenn der Server eine CPMSetCatStateIn-Nachrichtenanforderung vom Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4368">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4369">Überprüfen Sie, ob der Client über Administratorzugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4369">Check that client has administrative access.</span></span> <span data-ttu-id="c3671-4370">Wenn der Client keinen Administratorzugriff hat, MUSS der Server den Fehler STATUS \_ ACCESS \_ DENIED (0xC0000022) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4370">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="c3671-4371">Wenn dwNewState nicht gleich CICAT ALL OPENED ist, ändern Sie den Status des Katalogs, der im Feld CatName angegeben ist, wie im \_ \_ Feld \_ \_ dwNewState angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-4371">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="c3671-4372">Weitere Informationen finden Sie in Abschnitt 2.2.3.2.</span><span class="sxs-lookup"><span data-stu-id="c3671-4372">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="c3671-4373">Wenn der Server keinen Katalog mit dem im Feld CatName angegebenen Namen findet, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-4373">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4374">Reagieren Sie auf den Client mit einer CPMSetCatStateOut-Meldung, wobei dwOldState auf den vorherigen Zustand des \_ Katalogs festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c3671-4374">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="c3671-4375">Wenn dwNewState gleich CICAT ALL OPENED ist, MUSS der Server den Status aller Kataloge überprüfen. Wenn alle Kataloge gestartet werden, muss dwOldState auf 0x00000001 und \_ \_ andernfalls \_ \_ \_ dwOldState auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3671-4375">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="c3671-4376">3.1.5.1.3 Empfangen einer CPMUpdateDocumentsIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4376">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="c3671-4377">Wenn der Server eine CPMUpdateDocumentsIn-Nachrichtenanforderung empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4377">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4378">Überprüfen Sie, ob sich der Client in einer Liste verbundener Clients befindet (denen ein Katalog zugeordnet ist).</span><span class="sxs-lookup"><span data-stu-id="c3671-4378">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="c3671-4379">Wenn der Client nicht in der Liste enthalten ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4379">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4380">Überprüfen Sie, ob der Client über Administratorzugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4380">Check that client has administrative access.</span></span> <span data-ttu-id="c3671-4381">Wenn der Client keinen Administratorzugriff auf den Server hat, MUSS der Server den Fehler STATUS \_ ACCESS \_ DENIED (0xC0000022) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4381">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="c3671-4382">Beginnen Sie mit der Indizierung des vom Client angegebenen Pfads, und führen Sie je nach Wert des Flagfelds in der \_ CPMUpdateDocumentsIn-Nachricht eine vollständige oder inkrementelle Überprüfung durch.</span><span class="sxs-lookup"><span data-stu-id="c3671-4382">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="c3671-4383">Wenn der Pfad zuvor nicht indiziert wurde, MUSS er der Auflistung der indizierten Speicherorte hinzugefügt und eine vollständige Überprüfung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4383">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="c3671-4384">Wenn ein unzulässiger Wert des Flagfelds angegeben wird, MUSS der Server so agieren, als ob das Flag auf UPD INIT festgelegt wurde, und \_ \_ eine vollständige Überprüfung \_ durchführen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4384">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="c3671-4385">Dieser Vorgang MUSS in dem Katalog ausgeführt werden, der dem Client zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4385">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="c3671-4386">Reagieren Sie mit dem Nachrichtenheader für CPMUpdateDocumentsIn auf den Client, und legen Sie das Statusfeld auf die \_ Ergebnisse der Anforderung fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-4386">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="c3671-4387">3.1.5.1.4 Empfangen einer CPMForceMergeIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4387">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="c3671-4388">Wenn der Server eine CPMForceMergeIn-Nachrichtenanforderung empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4388">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4389">Überprüfen Sie, ob sich der Client in einer Liste verbundener Clients befindet (denen ein Katalog zugeordnet ist).</span><span class="sxs-lookup"><span data-stu-id="c3671-4389">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="c3671-4390">Wenn der Client nicht in der Liste enthalten ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4390">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4391">Überprüfen Sie, ob der Client über Administratorzugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4391">Check that client has administrative access.</span></span> <span data-ttu-id="c3671-4392">Wenn der Client keinen Administratorzugriff hat, MUSS der Server den Fehler STATUS \_ ACCESS \_ DENIED (0xC0000022) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4392">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="c3671-4393">Starten Sie alle Wartungsprozesse, die erforderlich sind, um die Abfrageleistung für einen Katalog zu verbessern, der dem Client zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4393">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="c3671-4394">Reagieren Sie auf den Client mit einem Nachrichtenheader für CPMForceMergeIn, und legen Sie das Statusfeld auf die \_ Ergebnisse der Anforderung fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-4394">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="c3671-4395">Beachten Sie, dass der Wartungsvorgang asynchron ist und fortgesetzt werden kann, nachdem der Client die Antwortnachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="c3671-4395">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="c3671-4396">Dieser Prozess wirkt sich nicht direkt auf das Protokoll aus (mit Abkungszeit).</span><span class="sxs-lookup"><span data-stu-id="c3671-4396">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="c3671-4397">3.1.5.2 Abfragen des Remoteindizierungsdiensts</span><span class="sxs-lookup"><span data-stu-id="c3671-4397">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="c3671-4398">3.1.5.2.1 Empfangen einer CPMConnectIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4398">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="c3671-4399">Wenn der Server eine CPMConnectIn-Anforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4399">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4400">Überprüfen Sie, ob sich der Client in der Liste der verbundenen Clients befindet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4400">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="c3671-4401">Wenn dies der Fall ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4401">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4402">Überprüft, ob der angegebene Katalog vorhanden ist und sich nicht im Zustand "Beendet" befliegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4402">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="c3671-4403">Wenn dies nicht der Fall ist, MUSS der Server einen CI \_ E \_ NO CATALOG \_ -Fehler (0x8004181D) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4403">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="c3671-4404">Fügen Sie den Client der Liste der verbundenen Clients hinzu.</span><span class="sxs-lookup"><span data-stu-id="c3671-4404">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="c3671-4405">Ordnen Sie den Katalog dem Client zu.</span><span class="sxs-lookup"><span data-stu-id="c3671-4405">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="c3671-4406">Speichern Sie die in der CPMConnectIn-Nachricht übergebenen Informationen (z. B. Katalogname, Clientversion usw.) im Clientzustand.</span><span class="sxs-lookup"><span data-stu-id="c3671-4406">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="c3671-4407">Antworten Sie mit einer CPMConnectOut-Nachricht auf den Client.</span><span class="sxs-lookup"><span data-stu-id="c3671-4407">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="c3671-4408">3.1.5.2.2 Empfangen einer CPMCreateQueryIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4408">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="c3671-4409">Wenn der Server eine CPMCreateQueryIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4409">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4410">Überprüfen Sie, ob sich der Client in der Liste der verbundenen Clients befindet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4410">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="c3671-4411">Wenn dies nicht der Fall ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4411">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4412">Überprüfen Sie, ob dem Client bereits eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4412">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="c3671-4413">Wenn dies der Fall ist, MUSS der Server den Fehler STATUS \_ INVALID \_ PARAMETER (0xC000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4413">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4414">Überprüfen Sie, ob sich der dem Client zugeordnete Katalog im Zustand befindet, der die Verarbeitung von Abfragen ermöglicht (CICAT \_ READONLY oder CICAT \_ WRITABLE).</span><span class="sxs-lookup"><span data-stu-id="c3671-4414">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="c3671-4415">Wenn dies nicht der Fall ist, MUSS der Server einen QUERY \_ S \_ NO QUERY \_ (0x8004160C)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4415">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="c3671-4416">Analysieren Sie die in der Abfrage angegebenen Einschränkungssatz, Sortierreihenfolge und Gruppierungen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4416">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="c3671-4417">Wenn auf dem Server ein Fehler auftritt, MUSS er einen entsprechenden Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4417">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="c3671-4418">Wenn dieser Schritt aus einem anderen Grund fehlschlägt, MUSS der Server den aufgetretenen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4418">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="c3671-4419">Informationen zu Indizierungsfehlern bei Dienstabfragen finden Sie unter \[ MSDN-QUERYERR \] .</span><span class="sxs-lookup"><span data-stu-id="c3671-4419">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="c3671-4420">Speichern Sie die Suchabfrage im Zustand für den Client.</span><span class="sxs-lookup"><span data-stu-id="c3671-4420">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="c3671-4421">Treffen Sie alle erforderlichen Vorbereitungen, um Zeilen an einen Client zu übergeben, und ordnen Sie die Abfrage den entsprechenden Cursorhandles zu (abhängig von den informationen, die in der CPMCreateQueryIn-Nachricht übergeben werden).</span><span class="sxs-lookup"><span data-stu-id="c3671-4421">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="c3671-4422">Fügen Sie diese Handles der Liste der Cursorhandles des Clients hinzu, und initialisieren Sie Listen mit Kapitelhandles und Lesezeichen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4422">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="c3671-4423">Initialisieren der Liste der Kapitelhandles für jeden Cursor in dieser Abfrage auf DB \_ NULL \_ HCHAPTER</span><span class="sxs-lookup"><span data-stu-id="c3671-4423">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="c3671-4424">Initialisieren Sie die Liste der Lesezeichenhandles für jeden Cursor in dieser Abfrage auf einen Satz von DBBMK \_ FIRST und DBBMK \_ LAST.</span><span class="sxs-lookup"><span data-stu-id="c3671-4424">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="c3671-4425">Markieren Sie die Abfrage als nicht überwacht auf Änderungen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4425">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="c3671-4426">Initialisieren Sie die Anzahl der Zeilen mit der derzeit berechneten Anzahl von Zeilen (die 0 sein kann, wenn die Abfrage nicht gestartet wurde, oder eine zahl, wenn die Abfrage ausgeführt wird), und initialisieren Sie den Zähler und Denominator des Abfrageabschlusses.</span><span class="sxs-lookup"><span data-stu-id="c3671-4426">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="c3671-4427">Reagieren Sie auf den Client mit einer CPMCreateQueryOut-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c3671-4427">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="c3671-4428">3.1.5.2.3 Empfangen einer CPMGetQueryStatusIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4428">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="c3671-4429">Wenn der Server eine CPMGetQueryStatusIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4429">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4430">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4430">Check if the client has query associated with it.</span></span> <span data-ttu-id="c3671-4431">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4431">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4432">Überprüfen Sie, ob sich das Cursorhandle in einer Liste der Cursorhandles des Clients befindet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4432">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="c3671-4433">Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4433">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3671-4434">Bereiten Sie eine CPMGetQueryStatusOut-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="c3671-4434">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="c3671-4435">Der Server MUSS den aktuellen Abfragestatus abrufen und im Feld QStatus festlegen \_ (mögliche Werte finden Sie unter 2.2.3.11).</span><span class="sxs-lookup"><span data-stu-id="c3671-4435">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="c3671-4436">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4436">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="c3671-4437">Reagieren Sie mit der MELDUNG CPMGetQueryStatusOut auf den Client.</span><span class="sxs-lookup"><span data-stu-id="c3671-4437">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="c3671-4438">3.1.5.2.4 Empfangen einer CPMGetQueryStatusExIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4438">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="c3671-4439">Wenn der Server eine CPMGetQueryStatusExIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4439">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4440">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4440">Check if the client has a query associated with it.</span></span> <span data-ttu-id="c3671-4441">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4441">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4442">Überprüfen Sie, ob das übergebene Cursorhandle in einer Liste der Cursorhandles des Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4442">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="c3671-4443">Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4443">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3671-4444">Bereiten Sie eine CPMGetQueryStatusExOut-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="c3671-4444">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="c3671-4445">Der Server MUSS den aktuellen Abfragestatus und Abfragestatus abrufen und QStatus festlegen (mögliche Werte finden Sie unter 2.2.3.11), \_ dwRatioFinishedDenominator \_ bzw. dwRatioFinishedNumerator.</span><span class="sxs-lookup"><span data-stu-id="c3671-4445">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="c3671-4446">Anschließend MUSS die Anzahl der Zeilen in den Abfrageergebnissen auf \_ cRowsTotal festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4446">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="c3671-4447">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4447">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="c3671-4448">Rufen Sie Informationen zum Clientkatalog ab, und geben Sie \_ cFilteredDocuments und \_ cDocumentsToFilter ein.</span><span class="sxs-lookup"><span data-stu-id="c3671-4448">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="c3671-4449">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4449">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="c3671-4450">Rufen Sie die Position des Lesezeichens ab, die durch das Handle im \_ bmk-Feld angegeben wird, und füllen Sie das verbleibende \_ iRowBmk-Feld in der CPMGetQueryStatusExOut-Meldung aus.</span><span class="sxs-lookup"><span data-stu-id="c3671-4450">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="c3671-4451">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4451">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="c3671-4452">Antworten Sie mit der CPMGetQueryStatusExOut-Meldung auf den Client.</span><span class="sxs-lookup"><span data-stu-id="c3671-4452">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="c3671-4453">3.1.5.2.5 Empfangen einer CPMRatioFinishedIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4453">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="c3671-4454">Wenn der Server eine CPMRatioFinishedIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4454">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4455">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4455">Check if the client has query associated with it.</span></span> <span data-ttu-id="c3671-4456">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4456">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4457">Überprüfen Sie, ob das übergebene Cursorhandle in der Liste der Cursorhandles des Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4457">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="c3671-4458">Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4458">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3671-4459">Bereiten Sie eine CPMRatioFinishedOut-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="c3671-4459">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="c3671-4460">Der Server MUSS den Abfragestatus des Clients abrufen und \_ die Felder ulNumerator, \_ ulDenominator und \_ cRows ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4460">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="c3671-4461">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4461">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="c3671-4462">Wenn \_ cRows gleich der letzten gemeldeten Anzahl von Zeilen für diese Abfrage ist, legen Sie \_ fNewRows auf 0x00000000 fest, andernfalls auf 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="c3671-4462">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="c3671-4463">Aktualisieren Sie die zuletzt gemeldete Anzahl von Zeilen für diese Abfrage auf den Wert von \_ cRows.</span><span class="sxs-lookup"><span data-stu-id="c3671-4463">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="c3671-4464">Antworten Sie mit der Meldung CPMRatioFinishedOut auf den Client.</span><span class="sxs-lookup"><span data-stu-id="c3671-4464">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="c3671-4465">3.1.5.2.6 Empfangen einer CPMSetBindingsIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4465">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="c3671-4466">Wenn der Server eine CPMSetBindingsIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4466">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4467">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4467">Check if the client has a query associated with it.</span></span> <span data-ttu-id="c3671-4468">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4468">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4469">Überprüfen Sie, ob das übergebene Cursorhandle in der Liste der Cursorhandles des Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4469">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="c3671-4470">Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4470">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3671-4471">Vergewissern Sie sich, dass Bindungsinformationen gültig sind (d. h., die Spalte gibt mindestens den Wert, die Länge oder den Status an, der zurückgegeben werden soll, keine Überlappung der Bindungen für Wert, Länge oder Status, und Wert, Länge und Status passen in die angegebene Zeilengröße), und melden Sie andernfalls einen \_ DB E \_ BADBINDINFO-Fehler (0x80040E08).</span><span class="sxs-lookup"><span data-stu-id="c3671-4471">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="c3671-4472">Speichern Sie die Bindungsinformationen, die den im Feld aColumns angegebenen Spalten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-4472">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="c3671-4473">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4473">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="c3671-4474">Reagieren Sie auf den Client mit einem Nachrichtenheader (nur), wobei \_ msg auf CPMSetBindingsIn und \_ der Status auf die Ergebnisse der angegebenen Bindung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4474">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="c3671-4475">3.1.5.2.7 Empfangen einer CPMGetRowsIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4475">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="c3671-4476">Wenn der Server eine CPMGetRowsIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4476">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4477">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4477">Check if the client has query associated with it.</span></span> <span data-ttu-id="c3671-4478">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4478">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4479">Überprüfen Sie, ob sich das übergebene Cursorhandle in der Liste der Cursorhandles des Clients befindet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4479">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="c3671-4480">Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4480">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3671-4481">Überprüfen Sie, ob der Client über einen aktuellen Satz von Bindungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4481">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="c3671-4482">Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4482">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3671-4483">Bereiten Sie eine CPMGetRowsOut-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="c3671-4483">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="c3671-4484">Der Server MUSS den Cursor wie in der Suchbeschreibung angegeben in Abfrageergebnissen positionieren.</span><span class="sxs-lookup"><span data-stu-id="c3671-4484">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="c3671-4485">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4485">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="c3671-4486">Rufen Sie so viele Zeilen ab, wie in einen Puffer passen, dessen Größe durch \_ cbReadBuffer angegeben wird, aber nicht mehr als durch \_ cRowsToTransfer angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-4486">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="c3671-4487">Beim Abrufen von Zeilen MUSS der Server den Eigenschaftswerttyp jeder ausgewählten Spalte mit dem Typ vergleichen, der im aktuellen Bindungssatz des Clients (Abschnitt 3.1.1) angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4487">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="c3671-4488">Wenn der Typ in der Bindung nicht VT \_ VARIANT ist, MUSS der Server versuchen, den Eigenschaftswert der Spalte in diesen Typ zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="c3671-4488">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="c3671-4489">Andernfalls MUSS der Eigenschaftswert in seinem normalen Typ zurückgegeben werden, wenn das DBPROP \_ USEEXTENDEDDBTYPES-Flag im DBPROPSET \_ QUERYEXT-Eigenschaftensatz des Clients festgelegt ist oder wenn der Eigenschaftswert der Spalte kein VT \_ VECTOR-Typ ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4489">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="c3671-4490">Wenn keines davon der Fall ist (d. h. der Server hat einen VT \_ VECTOR-Typ, und der Client unterstützt VT \_ VECTOR nicht), MUSS der Server versuchen, ihn wie folgt in einen \_ VT ARRAY-Typ zu konvertieren: VT \_ I8, VT \_ UI8, VT \_ FILETIME und VT \_ CLSID Array-Elemente können nicht konvertiert werden und schlagen stattdessen fehl. VT \_ LPSTR- und VT \_ LPWSTR-Arrayelemente MÜSSEN in VT BSTR konvertiert \_ werden. Arrayelemente aller anderen Typen MÜSSEN unverändert bleiben.</span><span class="sxs-lookup"><span data-stu-id="c3671-4490">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="c3671-4491">Wenn Zeilenspalten Kapitelhandles oder Lesezeichenhandles enthalten, MUSS der Server die entsprechenden Listen aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c3671-4491">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="c3671-4492">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4492">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="c3671-4493">Speichern Sie die tatsächliche Anzahl der abgerufenen Zeilen in \_ cRowsReturned.</span><span class="sxs-lookup"><span data-stu-id="c3671-4493">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="c3671-4494">Kopieren Sie die Suchbeschreibung und das Kapitelfeld aus CPMGetRowsIn in eine zu sendende CPMGetRowsOut-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c3671-4494">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="c3671-4495">Speichern Sie abgerufene Zeilen im Feld Rows (siehe Hinweis zum Status byte unten und Abschnitt 2.2.3.16 zur Struktur des Rows-Felds).</span><span class="sxs-lookup"><span data-stu-id="c3671-4495">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="c3671-4496">Antworten Sie mit der CPMGetRowsOut-Meldung auf den Client.</span><span class="sxs-lookup"><span data-stu-id="c3671-4496">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="c3671-4497">Hinweis zum Status-Bytefeld:</span><span class="sxs-lookup"><span data-stu-id="c3671-4497">Note on status byte field:</span></span>

<span data-ttu-id="c3671-4498">Wenn StatusUsed auf 0x01 in CTableColumn der CPMSetBindingIn-Nachricht für die Spalte festgelegt ist, MUSS der Server das Status byte (das sich am Anfang der Zeile unter StatusOffset befindet) für diese Spalte auf einen der folgenden Werte festlegen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4498">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="c3671-4499">Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-4499">Value</span></span> | <span data-ttu-id="c3671-4500">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3671-4500">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="c3671-4501">0x00</span><span class="sxs-lookup"><span data-stu-id="c3671-4501">0x00</span></span>  | <span data-ttu-id="c3671-4502">StatusOK</span><span class="sxs-lookup"><span data-stu-id="c3671-4502">StatusOK</span></span>       |
| <span data-ttu-id="c3671-4503">0x01</span><span class="sxs-lookup"><span data-stu-id="c3671-4503">0x01</span></span>  | <span data-ttu-id="c3671-4504">StatusDeferred</span><span class="sxs-lookup"><span data-stu-id="c3671-4504">StatusDeferred</span></span> |
| <span data-ttu-id="c3671-4505">0x02</span><span class="sxs-lookup"><span data-stu-id="c3671-4505">0x02</span></span>  | <span data-ttu-id="c3671-4506">StatusNull</span><span class="sxs-lookup"><span data-stu-id="c3671-4506">StatusNull</span></span>     |



 

<span data-ttu-id="c3671-4507">Wenn der Eigenschaftswert für diese Zeile nicht vorhanden ist, MUSS der Server das Status-Byte auf StatusNull festlegen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4507">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="c3671-4508">Wenn der Wert zu groß ist, um in der CPMGetRowsOut-Nachricht übertragen zu werden, MUSS der Server das Status-Byte auf StatusDeferred festlegen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4508">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="c3671-4509">Andernfalls MUSS der Server das Status-Byte auf StatusOK festlegen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4509">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="c3671-4510">3.1.5.2.8 Empfangen einer CPMFetchValueIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4510">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="c3671-4511">Wenn der Server eine CPMFetchValueIn-Nachrichtenanforderung von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4511">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4512">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4512">Check if the client has query associated with it.</span></span> <span data-ttu-id="c3671-4513">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4513">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4514">Bereiten Sie eine CPMFetchValueOut-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="c3671-4514">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="c3671-4515">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4515">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="c3671-4516">Suchen Sie das durch das Feld wid angegebene Dokument, \_ und überprüfen Sie, ob die Eigenschaften-ID für dieses Dokument (später als "Eigenschaftswert" bezeichnet) durch die PropSpec-Struktur für diesen Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4516">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="c3671-4517">Wenn dieser Wert nicht verfügbar ist, MUSS der Server \_ fValueExists auf 0x00000000 und andernfalls \_ fValueExists auf 0x00000001 festlegen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4517">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="c3671-4518">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="c3671-4519">Wenn \_ fValueExists gleich 0x00000001 MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4519">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="c3671-4520">Serialisieren Sie den Eigenschaftswert in eine SERIALIZEDPROPERTYVALUE-Struktur, und kopieren Sie ab dem \_ cbSoFar-Offset \_ höchstens cbChunk-Bytes (jedoch nicht hinter dem Ende der serialisierten Eigenschaft) in das vValue-Feld.</span><span class="sxs-lookup"><span data-stu-id="c3671-4520">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="c3671-4521">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4521">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="c3671-4522">Legen Sie cbValue auf die Anzahl der Bytes fest, \_ die im vorherigen Schritt kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4522">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="c3671-4523">Legen Sie vType auf den Eigenschaftstyp des Eigenschaftswerts fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-4523">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="c3671-4524">Wenn die Länge der serialisierten Eigenschaft größer als \_ cbSoFar \_ ist, die cbValue hinzugefügt wurde, legen Sie \_ fMoreExists auf 0x00000001 fest, andernfalls auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3671-4524">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="c3671-4525">Reagieren auf den Client mit der CPMFetchValueOut-Meldung</span><span class="sxs-lookup"><span data-stu-id="c3671-4525">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="c3671-4526">3.1.5.2.9 Empfangen einer CPMGetNotify-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4526">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="c3671-4527">Wenn der Server eine CPMGetNotify-Nachricht von einem Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4527">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4528">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4528">Check if the client has query associated with it.</span></span> <span data-ttu-id="c3671-4529">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4529">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4530">Wenn seit der letzten CPMSendNotifyOut-Nachricht für diesen Client keine Änderungen am Abfrageresultset vorgenommen wurden oder die Abfrage derzeit nicht auf Änderungen im Resultset überwacht wird, MUSS der Server mit der CPMGetNotify-Meldung antworten und damit beginnen, die Abfrage auf Änderungen im Resultset zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4530">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="c3671-4531">Wenn das Abfrageergebnisset zu einem späteren Zeitpunkt geändert wird, MUSS der Server genau eine CPMSendNotifyOut-Nachricht an den Client senden und DIE Änderung im \_ Feld watchNotify angeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-4531">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="c3671-4532">Wenn seit der letzten CPMSendNotifyOut-Nachricht Änderungen am Abfrageresultset vorgenommen wurden, MUSS der Server mit CPMSendNotifyOut antworten und DIE Änderung im \_ Feld watchNotify angeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-4532">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="c3671-4533">Beachten Sie, dass DBWATCHNOTIFY ROWSCHANGED bei vielen Änderungen an den Abfrageergebnissen \_ Priorität hat (d. h., wenn die Abfrage durchgeführt, erneut ausgeführt und dann die Anzahl der Geänderten Zeilen und die Abfrage erneut durchgeführt wurden, lautet das gemeldete Ereignis DBWATCHNOTIFY \_ ROWSCHANGED).</span><span class="sxs-lookup"><span data-stu-id="c3671-4533">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="c3671-4534">3.1.5.2.10 Empfangen einer CPMGetApproximatePositionIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4534">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="c3671-4535">Wenn der Server eine CPMGetApproximatePositionIn-Nachrichtenanforderung vom Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4535">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4536">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4536">Check if the client has a query associated with it.</span></span> <span data-ttu-id="c3671-4537">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4537">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4538">Überprüfen Sie, ob das Cursorhandle, das Kapitelhandle und das übergebene Lesezeichenhandle in den entsprechenden Listen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-4538">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="c3671-4539">Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4539">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3671-4540">Suchen Sie eine Zeile, die dem Lesezeichenhandle in den Abfrageergebnissen zugeordnet ist, und ermitteln Sie die Position der Zeile im Rowset, auf die das Kapitelhandle verweist, und bestimmen Sie den Zähler und Nenner für die Position.</span><span class="sxs-lookup"><span data-stu-id="c3671-4540">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="c3671-4541">Beachten Sie, dass das entsprechende Kapitel das Hauptrowset der Abfrage ist, wenn das Kapitelhandle DB \_ NULL \_ HCHAPTER ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4541">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="c3671-4542">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4542">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="c3671-4543">Reagieren Sie auf den Client mit einer CPMFetchValueOut-Meldung.</span><span class="sxs-lookup"><span data-stu-id="c3671-4543">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="c3671-4544">3.1.5.2.11 Empfangen einer CPMCompareBmkIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4544">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="c3671-4545">Wenn der Server eine CPMCompareBmkIn-Nachrichtenanforderung vom Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4545">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4546">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4546">Check if the client has a query associated with it.</span></span> <span data-ttu-id="c3671-4547">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4547">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4548">Überprüfen Sie, ob die übergebenen Cursorhandles, Kapitelhandles und Lesezeichenhandles in entsprechenden Listen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-4548">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="c3671-4549">Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4549">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3671-4550">Bereiten Sie eine CPMCompareBmkOut-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="c3671-4550">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="c3671-4551">Wenn Lesezeichenhandles gleich sind, \_ muss dwComparison AUF DBCOMPARE EQ festgelegt \_ sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-4551">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="c3671-4552">Wenn eines der Lesezeichenhandles DBBMK \_ FIRST oder DBBMK \_ LAST ist, muss \_ dwComparison auf DBCOMPARE NE festgelegt \_ werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4552">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="c3671-4553">Andernfalls MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4553">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="c3671-4554">Suchen von Zeilen, auf die von jedem Lesezeichenhandle in den Abfrageergebnissen verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="c3671-4554">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="c3671-4555">Wenn sich eine der Zeilen nicht im Kapitel befindet, das vom Kapitelhandle in CPMCompareBmkIn angegeben wird, \_ muss dwComparison auf DBCOMPARE \_ NOTCOMPARABLE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4555">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="c3671-4556">Wenn sich beide Zeilen im selben Kapitel befinden, MUSS der Server eine Ungefährung der Position dieser Zeilen im Rowset herstellen, auf das im Handle dieses Kapitels verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-4556">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="c3671-4557">Anschließend MÜSSEN Positionswerte verglichen und \_ dwComparison auf DBCOMPARE LT festgelegt \_ werden, wenn die Position der ersten Zeile kleiner als die Position der zweiten Zeile ist. Andernfalls \_ MUSS dwComparison auf DBCOMPARE GT festgelegt \_ werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4557">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="c3671-4558">Reagieren Sie auf den Client mit einer ausgefüllten CPMCompareBmkOut-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c3671-4558">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="c3671-4559">3.1.5.2.12 Empfangen einer CPMRestartPositionIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4559">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="c3671-4560">Wenn der Server die CPMRestartPositionIn-Nachrichtenanforderung vom Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4560">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4561">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4561">Check if the client has a query associated with it.</span></span> <span data-ttu-id="c3671-4562">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4562">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4563">Überprüfen Sie, ob das Cursorhandle und das übergebene Kapitelhandle in den entsprechenden Listen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-4563">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="c3671-4564">Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4564">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3671-4565">Bewegen Sie den Cursor an den Anfang des Kapitels, der durch das Kapitelhandle identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-4565">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="c3671-4566">Beachten Sie, dass das entsprechende Kapitel das Hauptrowset der Abfrage ist, wenn das Kapitelhandle DB \_ NULL \_ HCHAPTER ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4566">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="c3671-4567">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, MUSS der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4567">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="c3671-4568">Reagieren Sie mit einer CPMRestartPositionIn-Nachricht auf den Client.</span><span class="sxs-lookup"><span data-stu-id="c3671-4568">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="c3671-4569">3.1.5.2.13 Empfangen einer CPMFreeCursorIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4569">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="c3671-4570">Wenn der Server eine CPMFreeCursorIn-Nachrichtenanforderung vom Client empfängt, MUSS der Server folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4570">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4571">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4571">Check if the client has a query associated with it.</span></span> <span data-ttu-id="c3671-4572">Wenn dies nicht der Fall ist, MUSS der Server einen \_ STATUS INVALID \_ PARAMETER (0xC000000D)-Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4572">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="c3671-4573">Überprüfen Sie, ob das übergebene Cursorhandle in der Liste der Cursorhandles des Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4573">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="c3671-4574">Wenn dies nicht der Fall ist, MUSS der Server einen E \_ FAIL-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4574">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="c3671-4575">Geben Sie den Cursor und die zugehörigen Ressourcen (eine vollständige Liste finden Sie in Abschnitt 3.1.1) für dieses Cursorhandle frei.</span><span class="sxs-lookup"><span data-stu-id="c3671-4575">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="c3671-4576">Entfernen Sie den Cursor aus der Liste der Cursor für diesen Client.</span><span class="sxs-lookup"><span data-stu-id="c3671-4576">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="c3671-4577">Antworten Sie mit einer CPMFreeCursorOut-Nachricht, und legen Sie das \_ Feld cCursorsRemaining mit der Anzahl der verbleibenden Cursor fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-4577">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="c3671-4578">in der Liste dieses Clients.</span><span class="sxs-lookup"><span data-stu-id="c3671-4578">in this client's list.</span></span>
-   <span data-ttu-id="c3671-4579">Wenn für diesen Client keine Cursor mehr vorhanden sind, MUSS der Server die Abfrage und die zugehörigen Ressourcen freigeben (siehe Abschnitt 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="c3671-4579">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="c3671-4580">3.1.5.2.14 Empfangen einer CPMDisconnect-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4580">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="c3671-4581">Wenn der Server eine CPMDisconnect-Nachrichtenanforderung vom Client empfängt, MUSS der Server den Client aus der Liste der verbundenen Clients entfernen und alle ressourcen freigeben, die dem Client zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-4581">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="c3671-4582">3.1.6 Timerereignisse</span><span class="sxs-lookup"><span data-stu-id="c3671-4582">3.1.6 Timer Events</span></span>

<span data-ttu-id="c3671-4583">Keine.</span><span class="sxs-lookup"><span data-stu-id="c3671-4583">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="c3671-4584">3.1.7 Andere lokale Ereignisse</span><span class="sxs-lookup"><span data-stu-id="c3671-4584">3.1.7 Other Local Events</span></span>

<span data-ttu-id="c3671-4585">Wenn der Server beendet wird, MUSS er zuerst in den Zustand "Herunterfahren" übergehen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4585">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="c3671-4586">Sie MUSS dann die Überwachung der Pipe beenden, alle anderen implementierungsspezifischen Aufgaben zum Herunterfahren ausführen und dann in den Zustand "Beendet" übergehen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4586">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="c3671-4587">3.2 Clientdetails</span><span class="sxs-lookup"><span data-stu-id="c3671-4587">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="c3671-4588">3.2.1 Abstraktes Datenmodell</span><span class="sxs-lookup"><span data-stu-id="c3671-4588">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="c3671-4589">Im folgenden Abschnitt werden die Daten und der Status angegeben, die vom Client des Content Indexing Service Protocol verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4589">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="c3671-4590">Die bereitgestellten Daten sollen die Erklärung des Verhaltens des Protokolls erleichtern.</span><span class="sxs-lookup"><span data-stu-id="c3671-4590">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="c3671-4591">In diesem Abschnitt wird nicht vorausgesetzt, dass Implementierungen diesem Modell entsprechen, solange ihr externes Verhalten mit dem in diesem Dokument beschriebenen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4591">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="c3671-4592">Ein Client weist den folgenden abstrakten Zustand auf:</span><span class="sxs-lookup"><span data-stu-id="c3671-4592">A client has the following abstract state:</span></span>

-   <span data-ttu-id="c3671-4593">**Letzte gesendete Nachricht:** Eine Kopie der letzten an den Server gesendeten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c3671-4593">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="c3671-4594">**Aktueller Eigenschaftswert:** Ein Teilwert einer "verzögerten" Eigenschaft, die gerade abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-4594">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="c3671-4595">**Aktuelle empfangene Bytes:** Die Anzahl der bytes, die bisher für den aktuellen Eigenschaftswert empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4595">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="c3671-4596">**Named Pipe-Verbindungsstatus:** Eine Verbindung mit dem Server</span><span class="sxs-lookup"><span data-stu-id="c3671-4596">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="c3671-4597">3.2.2 Timer</span><span class="sxs-lookup"><span data-stu-id="c3671-4597">3.2.2 Timers</span></span>

<span data-ttu-id="c3671-4598">Es sind keine Protokolltimer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c3671-4598">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="c3671-4599">3.2.3 Initialisierung</span><span class="sxs-lookup"><span data-stu-id="c3671-4599">3.2.3 Initialization</span></span>

<span data-ttu-id="c3671-4600">Es werden keine Aktionen ausgeführt, bis eine Anforderung auf höherer Ebene empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-4600">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="c3671-4601">3.2.4 Higher-Layer Ausgelöste Ereignisse</span><span class="sxs-lookup"><span data-stu-id="c3671-4601">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="c3671-4602">Wenn eine Anforderung von einer höheren Ebene empfangen wird, MUSS der Client unter Verwendung der in Abschnitt 2.1 angegebenen Details eine Named Pipe-Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4602">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="c3671-4603">Wenn dies nicht möglich ist, MUSS bei der Anforderung der höheren Ebene ein Fehler aufgetreten sein.</span><span class="sxs-lookup"><span data-stu-id="c3671-4603">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="c3671-4604">Das heißt, bei einem Verbindungsfehler liegt es in der Verantwortung der höheren Ebene, dies bei Bedarf erneut zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4604">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="c3671-4605">Ein Header MUSS mit Feldern vorangestellt werden, die wie in Abschnitt 2.2.2 angegeben festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-4605">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="c3671-4606">Für Nachrichten, für die angegeben wird, dass eine Prüfsumme ungleich 0 (null) erforderlich ist, MUSS der \_ ulChecksum-Wert wie folgt berechnet werden:</span><span class="sxs-lookup"><span data-stu-id="c3671-4606">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="c3671-4607">Der Inhalt der Nachricht nach dem \_ ulReserved2-Feld im Nachrichtenheader MUSS als Sequenz von 32-Bit-Ganzzahlen interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4607">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="c3671-4608">Der Client MUSS die Summe der numerischen Werte berechnen, die von diesen ganzen Zahlen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4608">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="c3671-4609">Berechnen Sie den bitweisen XOR dieses Werts mit 0x59533959.</span><span class="sxs-lookup"><span data-stu-id="c3671-4609">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="c3671-4610">Subtrahieren Sie den von msg angegebenen Wert \_ von dem Wert, der sich aus dem bitweisen XOR ergibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4610">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="c3671-4611">3.2.4.1 Katalogverwaltung des Remoteindizierungsdiensts</span><span class="sxs-lookup"><span data-stu-id="c3671-4611">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="c3671-4612">Jede Nachricht wird durch eine Anforderung von der höheren Ebene ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="c3671-4612">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="c3671-4613">Es wird keine Nachrichtensequenz vom Client für CISP-Nachrichtenanforderungen zur Remoteverwaltung von Katalogen erzwungen, aber (mit Ausnahme einer CPMSetCatStateIn-Nachricht) antwortet der Server nur dann mit Erfolg, wenn der Client zuvor über eine CPMConnectIn-Nachricht eine Verbindung hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="c3671-4613">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="c3671-4614">3.2.4.1.1 Senden einer CPMCiStateInOut-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4614">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="c3671-4615">In der Regel fordert die höhere Ebene den Protokollclient auf, eine CPMCiStateInOut-Nachricht zu senden, wenn informationen zum Indizieren von Diensten auf dem Server erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-4615">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="c3671-4616">Wenn der Client aufgefordert wird, diese Nachricht zu senden, MUSS er folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4616">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4617">Senden Sie eine CPMCiStateInOut-Nachricht wie in Abschnitt 2.2.3.1 angegeben an den Server.</span><span class="sxs-lookup"><span data-stu-id="c3671-4617">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="c3671-4618">Warten Sie, bis die CPMCiStateInOut-Nachricht vom Server empfangen wird, und verwerfen Sie automatisch alle anderen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="c3671-4618">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="c3671-4619">Melden Sie den Wert des \_ Statusfelds der Antwort, und wenn dies erfolgreich war, wird die Informationsstruktur wieder auf die höhere Ebene zurückgestellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4619">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="c3671-4620">3.2.4.1.2 Senden einer CPMSetCatStateIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4620">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="c3671-4621">In der Regel fordert die höhere Ebene den Protokollclient auf, eine CPMSetCatStateIn-Nachricht zu senden, wenn Informationen über einen Katalog oder den gesamten Katalog erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-4621">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="c3671-4622">Für diese Nachricht muss die höhere Ebene dem Protokollclient einen Wert für \_ dwNewState und ggf. den Namen des Katalogs bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4622">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="c3671-4623">Wenn der Client aufgefordert wird, diese Nachricht zu senden, MUSS er folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4623">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4624">Senden Sie eine CPMSetCatStateIn-Nachricht wie in 2.2.3.2 angegeben an den Server.</span><span class="sxs-lookup"><span data-stu-id="c3671-4624">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="c3671-4625">Warten Sie, bis eine CPMSetCatStateOut-Nachricht vom Server empfangen wird, und verwerfen Sie automatisch alle anderen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="c3671-4625">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="c3671-4626">Melden Sie den Wert des \_ Statusfelds der Antwort, und wenn dies erfolgreich war, wird \_ dwOldState wieder auf die höhere Ebene zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4626">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="c3671-4627">3.2.4.1.3 Senden einer CPMUpdateDocumentsIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4627">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="c3671-4628">Die höhere Ebene fordert in der Regel zum Senden dieser Nachricht auf, wenn dokumente im vorhandenen Pfad aktualisiert oder dem Index ein neuer Dateipfad hinzugefügt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c3671-4628">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="c3671-4629">Daher besteht die höhere Ebene darin, den Pfad und den Typ eines Scans bereitzustellen, wie in Abschnitt 2.2.3.4 angegeben, wobei ein inkrementelles oder vollständiges Update für vorhandene Pfade und neue Initialisierung für neue Pfade vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4629">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="c3671-4630">Um die Anforderung der höheren Ebene zu erfüllen, MUSS der Client folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4630">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4631">Senden Sie eine CPMUpdateDocumentsIn-Nachricht wie in Abschnitt 2.2.3.4 angegeben an den Server.</span><span class="sxs-lookup"><span data-stu-id="c3671-4631">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="c3671-4632">Warten Sie auf den Empfang der CPMUpdateDocumentsIn-Nachricht vom Server, und verwerfen Sie alle anderen Nachrichten im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="c3671-4632">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="c3671-4633">Melden Sie den Wert des \_ Statusfelds der Antwort an die höhere Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="c3671-4633">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="c3671-4634">3.2.4.1.4 Senden einer CPMForceMergeIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4634">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="c3671-4635">In der Regel fordert die höhere Ebene an, diese Nachricht zu senden, wenn die Abfrageleistung verbessert werden muss oder dies Teil der geplanten Wartung des Indizierungsdiensts ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4635">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="c3671-4636">Um die höhere Ebene zu bedienen, MUSS der Client Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="c3671-4636">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4637">Senden Sie die CPMForceMergeIn-Nachricht gemäß Abschnitt 2.2.3.5 an den Server.</span><span class="sxs-lookup"><span data-stu-id="c3671-4637">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="c3671-4638">Warten Sie auf den Empfang einer CPMUpdateDocumentsIn-Nachricht vom Server, und verwerfen Sie alle anderen Nachrichten im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="c3671-4638">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="c3671-4639">Melden Sie den Wert des \_ Statusfelds der Antwort an die höhere Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="c3671-4639">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="c3671-4640">3.2.4.2 Abfragenachrichten des Remoteindizierungsdienstkatalogs</span><span class="sxs-lookup"><span data-stu-id="c3671-4640">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="c3671-4641">Mit Ausnahme von CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut besteht eine 1:1-Beziehung zwischen CISP-Nachrichten und Anforderungen höherer Ebene.</span><span class="sxs-lookup"><span data-stu-id="c3671-4641">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="c3671-4642">Für die beiden oben genannten Ausnahmen können vom Client mehrere Nachrichten generiert werden, um entweder die Größenanforderungen zu erfüllen oder eine vollständige Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4642">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="c3671-4643">Die höhere Ebene verfolgt in der Regel alle abfragespezifischen Informationen nach (z. B. geöffnete Cursorhandles, rechtliche Werte für Lesezeichen- und Kapitelhandles, wid-Werte für verzögerte Eigenschaftswerte usw.) und verfolgt auch nach, ob sich der Client in einem verbundenen Zustand befindet. Dies wird jedoch nicht vom Client erzwungen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4643">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="c3671-4644">Zur Veranschaulichung veranschaulicht der Clientteil des Diagramms in Abschnitt 3 diese Sequenz für eine einfache Abfrage des Indizierungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="c3671-4644">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="c3671-4645">3.2.4.2.1 Senden einer CPMConnectIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4645">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="c3671-4646">Diese Meldung ist in der Regel die erste Anforderung von der höheren Ebene (wenn der Client nicht verbunden ist, tritt auf dem Server ein Fehler bei den meisten Nachrichten mit Ausnahme von CPMSetCatStateIn auf).</span><span class="sxs-lookup"><span data-stu-id="c3671-4646">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="c3671-4647">Die höhere Ebene stellt dem Protokollclient Informationen zur Verfügung, die für die Verbindung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-4647">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="c3671-4648">Um die höhere Ebene zu bedienen, MUSS der Client Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="c3671-4648">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4649">Füllen Sie die Nachricht mithilfe der Informationen aus, die der Client der höheren Ebene bereitgestellt hat (siehe Abschnitt 2.2.3.6) in \_ iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 und aPropertySet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4649">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="c3671-4650">Legen \_ Sie fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet und cExtPropSet wie in 2.2.3.6 angegeben fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-4650">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="c3671-4651">Legen Sie die Prüfsumme im \_ Feld ulChecksum fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-4651">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="c3671-4652">Senden Sie die CPMConnectIn-Nachricht an den Server.</span><span class="sxs-lookup"><span data-stu-id="c3671-4652">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="c3671-4653">Warten Sie auf den Empfang einer CPMConnectOut-Nachricht vom Server, und verwerfen Sie alle anderen Nachrichten im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="c3671-4653">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="c3671-4654">Melden Sie den Wert des Statusfelds der Antwort und, falls erfolgreich, die \_ \_ serverVersion zurück zur höheren Ebene.</span><span class="sxs-lookup"><span data-stu-id="c3671-4654">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="c3671-4655">Zu Informationszwecken wird erwartet, dass höhere Ebenen bei erfolgreicher Verbindung in der Regel die folgenden Aktionen ausführen, diese jedoch nicht vom CISP-Client erzwungen werden:</span><span class="sxs-lookup"><span data-stu-id="c3671-4655">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="c3671-4656">Verwenden von Katalogverwaltungsmeldungen des Remoteindizierungsdiensts für Verwaltungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="c3671-4656">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="c3671-4657">Verwenden Sie eine CPMCreateQueryIn-Anforderung, um eine Suchabfrage zum Abrufen von Ergebnissen aus dem Katalog zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4657">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="c3671-4658">3.2.4.2.2 Senden einer CPMCreateQueryIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4658">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="c3671-4659">Die höhere Ebene stellt in der Regel Informationen für die Abfrageerstellung zur Verfügung, sobald der Protokollclient verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4659">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="c3671-4660">Die höhere Ebene stellt dem Client einen Einschränkungssatz, einen Spaltensatz, Sortierreihenfolgeregeln und einen Kategorisierungssatz (jede davon kann weggelassen werden), Rowseteigenschaften und die Struktur des Eigenschaften-ID-Mappers zur Verwendung.</span><span class="sxs-lookup"><span data-stu-id="c3671-4660">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="c3671-4661">Wenn diese Anforderung von einer höheren Ebene empfangen wird, MUSS der Client Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="c3671-4661">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4662">Bereiten Sie ein CPMCreateQueryOut wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="c3671-4662">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="c3671-4663">Wenn ein Spaltensatz vorhanden ist, legen Sie CColumnsSetPreset auf 0x01 und füllen Sie das Feld ColumnsSet aus.</span><span class="sxs-lookup"><span data-stu-id="c3671-4663">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="c3671-4664">Wenn Einschränkungen vorhanden sind, legen Sie CRestrictionPresent auf 0x01 und füllen Sie das Feld Einschränkung aus.</span><span class="sxs-lookup"><span data-stu-id="c3671-4664">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="c3671-4665">Wenn eine Sortierreihenfolge vorhanden ist, füllen Sie das Feld SortSet aus.</span><span class="sxs-lookup"><span data-stu-id="c3671-4665">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="c3671-4666">Wenn ein Kategorisierungssatz vorhanden ist, legen Sie CSortSetPresent auf 0x01 und füllen Sie das Feld CategorizationSet aus.</span><span class="sxs-lookup"><span data-stu-id="c3671-4666">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="c3671-4667">Legen Sie die restlichen Felder wie in 2.2.3.8 angegeben fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-4667">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="c3671-4668">Berechnen \_ Sie das ulCheckSum-Feld im Header.</span><span class="sxs-lookup"><span data-stu-id="c3671-4668">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="c3671-4669">Senden Sie die Nachricht CPMCreateQueryIn an den Server.</span><span class="sxs-lookup"><span data-stu-id="c3671-4669">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="c3671-4670">Warten Sie auf den Empfang der CPMCreateQueryOut-Nachricht (siehe Details in Abschnitt 3.2.5.1.1), und verwerfen Sie alle anderen Nachrichten im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="c3671-4670">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="c3671-4671">Melden Sie den Wert des Statusfelds der Antwort und, falls erfolgreich, das Array von Cursorhandles und informative boolesche Werte \_ (wie in 2.2.3.9 angegeben) zurück zur höheren Ebene.</span><span class="sxs-lookup"><span data-stu-id="c3671-4671">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="c3671-4672">3.2.4.2.3 Senden einer CPMSetBindingsIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4672">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="c3671-4673">In der Regel werden von der höheren Ebene Bindungen für jede Spalte festgelegt, die in den Zeilen zurückgegeben wird, wenn sie bereits über ein gültiges Cursorhandl verfügt (siehe Abschnitt 3.2.5.1.1, nachdem CPMCreateQueryOut erfolgreich empfangen wurde).</span><span class="sxs-lookup"><span data-stu-id="c3671-4673">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="c3671-4674">Von der höheren Wird erwartet, dass sie ein Array von CTableColumn-Strukturen für das Feld aColumns und ein gültiges Cursorhand handle bereitstellen, wie in Abschnitt 2.2.4.31 angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-4674">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="c3671-4675">Wenn diese Anforderung von der höheren Ebene empfangen wird, MUSS der Client Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="c3671-4675">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4676">Berechnen Sie die Anzahl der CTableColumn-Strukturen im Array aColumns, und legen Sie das Feld cColumns auf diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-4676">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="c3671-4677">Berechnen Sie die Gesamtgröße der Felder cColumns und aColumns in Bytes, und legen Sie das \_ Feld cbBindingDesc auf diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-4677">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="c3671-4678">Legen Sie die angegebenen Felder in der CPMSetBindingsIn-Nachricht auf die Werte fest, die von der höheren Anwendungsschicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4678">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="c3671-4679">Legen Sie \_ das feld ulChecksum auf den wert fest, der gemäß Abschnitt 3.2.5 berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-4679">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="c3671-4680">Senden Sie die fertige CPMSetBindignsIn-Nachricht an den Server.</span><span class="sxs-lookup"><span data-stu-id="c3671-4680">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="c3671-4681">Warten Sie auf den Empfang einer CPMSetBindingsIn-Nachricht vom Server, und verwerfen Sie andere Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="c3671-4681">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="c3671-4682">Geben Sie den Status aus \_ dem Statusfeld der Antwort an die höhere Ebene an.</span><span class="sxs-lookup"><span data-stu-id="c3671-4682">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="c3671-4683">Aus informativen Gründen wird erwartet, dass höhere Ebenen in der Regel einen Client zum Senden einer CPMGetRowsIn-Nachricht anfordern, dies wird jedoch nicht durch das Content Indexing Service-Protokoll erzwungen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4683">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="c3671-4684">3.2.4.2.4 Senden einer CPMGetRowsIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4684">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="c3671-4685">Wenn die höhere Ebene Zeileninformationen empfangen möchte, stellt sie dem Protokollclient ein gültiges Cursor- und Kapitelhand handle und eine entsprechende Suchbeschreibung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c3671-4685">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="c3671-4686">In der Regel wird eine höhere Ebene erwartet, wenn sie über einen gültigen Cursor und/oder Kapitelhandpunkt verfügt und die Bindungen mit der CPMSetBindingsIn-Nachricht festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4686">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="c3671-4687">Für den Zugriff auf das Rowset in einem Kapitel ist die höhere Ebene die Verwendung des Kapitelhandlings, das vom Server in einer vorherigen CPMGetRowsOut-Nachricht empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="c3671-4687">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="c3671-4688">Wenn diese Anforderung von der höheren Ebene empfangen wird, MUSS der Client Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="c3671-4688">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4689">Bestimmen Sie, welcher ganzzahlige Wert ohne Vorzeichen für das \_ Feld cbReadBuffer angegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-4689">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="c3671-4690">Um diesen Wert zu bestimmen, MUSS der Client den maximal folgenden Wert verwenden:</span><span class="sxs-lookup"><span data-stu-id="c3671-4690">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="c3671-4691">Das Tausendfache des Werts des Felds c \_ RowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="c3671-4691">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="c3671-4692">Wert von \_ cbRowWidth, aufgerundet auf das nächste 512-Byte-Vielfache.</span><span class="sxs-lookup"><span data-stu-id="c3671-4692">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="c3671-4693">Nehmen Sie den höheren dieser beiden Werte bis zum Grenzwert von 16.000.</span><span class="sxs-lookup"><span data-stu-id="c3671-4693">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="c3671-4694">In Fällen, in denen eine einzelne Zeile größer als 16.000 ist, kann der Server keine Ergebnisse an diese Abfrage zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-4694">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="c3671-4695">Geben Sie eine Clientbasis für Zeilendaten variabler Größe im Clientadressenraum im \_ Feld ulClientBase an.</span><span class="sxs-lookup"><span data-stu-id="c3671-4695">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="c3671-4696">*Windows-Verhalten: Bei einem 32-Bit-Client, der mit einem 32-Bit-Server spricht, oder einem 64-Bit-Client, der mit einem 64-Bit-Server spricht, wird dieser Wert auf eine Speicheradresse des empfangenden Puffers im Anwendungsprozess festgelegt. Dadurch können Zeiger, die im Rows-Feld von CPMGetRowsOut empfangen werden, richtige Speicherzeige in einem Clientanwendungsprozess sein. Andernfalls wird sie auf 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="c3671-4696">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="c3671-4697">Berechnen Sie die Größe der Suchbeschreibung, und legen Sie sie im \_ Feld cbSeek fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-4697">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="c3671-4698">Legen Sie den Wert von cbReserved (der als Offset für Zeilenstart fungieren würde) auf den Wert \_ cbSeek plus 0x14.</span><span class="sxs-lookup"><span data-stu-id="c3671-4698">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="c3671-4699">Senden Sie eine CPMConnectIn-Nachricht wie in 2.2.3.15 angegeben an den Server.</span><span class="sxs-lookup"><span data-stu-id="c3671-4699">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="c3671-4700">3.2.4.2.5 Senden einer CPMFetchValueIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4700">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="c3671-4701">Wenn der Client eine CPMGetRowsOut-Antwort vom Server empfängt, bei der das Feld Status der Spalte auf StatusDeferred (0x01) festgelegt ist, bedeutet dies, dass der Eigenschaftswert nicht im Feld Zeilen der CPMGetRowsOut-Nachricht enthalten war.</span><span class="sxs-lookup"><span data-stu-id="c3671-4701">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="c3671-4702">In diesem Fall fordert die höhere Ebene den Protokollclient in der Regel auf, den Wert mithilfe der CPMFetchValueIn-Nachricht abzurufen, und stellt den PropSpec- und wid-Wert für eine verzögerte Eigenschaft zur Anwendung, die der Protokollclient in der ersten \_ CPMFetchValueIn-Nachricht verwenden muss.</span><span class="sxs-lookup"><span data-stu-id="c3671-4702">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="c3671-4703">Wenn dies die erste CPMFetchValueIn-Nachricht ist, die der Client gesendet hat, um die angegebene Eigenschaft an fordern, MUSS der Client Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="c3671-4703">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4704">Legen Sie alle Felder in einer Nachricht wie in Abschnitt 2.2.3.19 angegeben fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-4704">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="c3671-4705">Legen \_ Sie cbSoFar auf 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="c3671-4705">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="c3671-4706">Legen Sie Aktuelle empfangene Bytes auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-4706">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="c3671-4707">Senden Sie die CPMFetchValueIn-Nachricht an den Server.</span><span class="sxs-lookup"><span data-stu-id="c3671-4707">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="c3671-4708">3.2.4.2.6 Senden einer CPMFreeCursorIn-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3671-4708">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="c3671-4709">Sobald die höhere Ebene die Suchabfrage nicht mehr verwendet, kann sie die Ressourcen auf dem Server frei geben, indem der Client aufgefordert wird, eine CPMFreeCursorIn-Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4709">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="c3671-4710">Wenn diese Anforderung empfangen wird, MUSS der Client eine CPMFreeCursorIn-Nachricht wie in 2.2.3.28 angegeben an den Server senden, die das von der oberen Ebene angegebene Handle enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-4710">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="c3671-4711">3.2.4.2.7 Senden einer CPMDisconnect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c3671-4711">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="c3671-4712">Wenn die höhere Ebene keine Abfragen mehr für den Indizierungsdienst enthält, fordert die Anwendung möglicherweise an, dass der Client eine CPMDisconnect-Nachricht an den Server sendet, um weitere Serverressourcen frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="c3671-4712">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="c3671-4713">Wenn diese Abfrage empfangen wird, MUSS der Client die Nachricht einfach wie angefordert senden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4713">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="c3671-4714">Es gibt keine Antwort auf diese Nachricht vom Server.</span><span class="sxs-lookup"><span data-stu-id="c3671-4714">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="c3671-4715">3.2.5 Nachrichtenverarbeitungs- und Sequenzierungsregeln</span><span class="sxs-lookup"><span data-stu-id="c3671-4715">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="c3671-4716">Wenn der Client eine Nachrichtenantwort vom Server empfängt, MUSS der Client die zuletzt gesendete Nachricht verwenden, um zu bestimmen, ob es sich bei der vom Server empfangenen Nachricht um die vom Client erwartete Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4716">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="c3671-4717">Alle Nachrichten mit \_ einem msg-Feld, die sich von dem unter Letzte Sendenachricht unterscheiden, MÜSSEN ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4717">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="c3671-4718">3.2.5.1 Empfangen einer CPMCreateQueryOut-Antwort</span><span class="sxs-lookup"><span data-stu-id="c3671-4718">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="c3671-4719">Wenn der Client eine CPMCreateQueryOut-Meldungsantwort vom Server empfängt, MUSS der Client den Status zurückgeben und (wenn der Status erfolgreich ist) Cursorhandlwerte wieder auf eine höhere \_ Ebene verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c3671-4719">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="c3671-4720">Alle weiteren Aktionen werden bis zur höheren Ebene durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4720">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="c3671-4721">Da die höhere Ebene die Abfragestruktur kennt, erwartet sie immer, dass in der CPMCreateOueryOut-Nachricht die richtige Anzahl von Cursorhandles zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-4721">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="c3671-4722">Die Cursorhandles werden in der folgenden Reihenfolge zurückgegeben: Das erste Handle ist für das nicht gekapte Rowset, das zweite für das erste kapitelte Rowset (die Gruppierung von Ergebnissen basierend auf der ersten Kategorie, die im CategorizationSet-Feld der CPMCreateQueryIn-Nachricht angegeben ist).</span><span class="sxs-lookup"><span data-stu-id="c3671-4722">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="c3671-4723">Zu Informationszwecken wird erwartet, dass höhere Ebenen die folgenden Aktionen ausführen können, diese werden jedoch nicht vom CISP-Client erzwungen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4723">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="c3671-4724">Verwenden Sie CPMSetBindingsIn, um Bindungen für einzelne Spalten zu setzen und alle nachfolgenden Aktionen für den Abfragepfad auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4724">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="c3671-4725">Verwenden Sie CPMGetQueryStatusIn, um den Ausführungsstatus einer Abfrage zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4725">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="c3671-4726">Verwenden Sie CPMRatioFinishedIn, um den Vervollständigungsprozentsatz der Abfrage an fordern.</span><span class="sxs-lookup"><span data-stu-id="c3671-4726">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="c3671-4727">3.2.5.2 Empfangen einer CPMGetRowsOut-Antwort</span><span class="sxs-lookup"><span data-stu-id="c3671-4727">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="c3671-4728">Wenn der Client eine CPMGetRowsOut-Meldungsantwort vom Server empfängt, MUSS der Client folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4728">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4729">Überprüfen Sie, ob \_ das Statusfeld im Header auf Erfolg oder Fehler hinweist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4729">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="c3671-4730">Wenn der \_ Statuswert STATUS \_ BUFFER TOO \_ SMALL (0xC0000023) ist, MUSS der Client den Status \_ Letzte gesendete Nachricht überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4730">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="c3671-4731">Wenn sie keine CPMGetRowsIn-Nachricht enthält, MUSS die empfangene Nachricht im Hintergrund ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4731">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="c3671-4732">Andernfalls MUSS der Client eine neue CPMGetRowsIn-Nachricht mit allen Feldern, die mit dem gespeicherten identisch sind, an den Server senden, mit der Ausnahme, dass der \_ cbReadBuffer um 512 erhöht werden MUSS (aber nicht größer als 0x4000).</span><span class="sxs-lookup"><span data-stu-id="c3671-4732">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="c3671-4733">Wenn \_ status STATUS BUFFER TOO SMALL \_ (0xC0000023) lautet und Last Message Sent bereits \_ \_ \_ cbReadBuffer aufweist, 0x4000 muss der Client den Fehler bis zur höheren Ebene melden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4733">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="c3671-4734">Wenn der \_ Statuswert ein anderer Fehlerwert ist, MUSS der Client den Fehler bis zur höheren Ebene angeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-4734">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="c3671-4735">Wenn der \_ Statuswert auf Erfolg hinweist, MÜSSEN die Ergebnisse bis zur höheren Ebene angezeigt werden, die die Informationen anfordert, und weitere Aktionen befinden sich auf der höheren Ebene.</span><span class="sxs-lookup"><span data-stu-id="c3671-4735">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="c3671-4736">Zu Informationszwecken wird erwartet, dass höhere Ebenen in der Regel die folgenden Aktionen ausführen, diese werden jedoch nicht vom Client des Inhaltsindizierungsdienstprotokolls erzwungen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4736">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="c3671-4737">Wenn die Werte in Zeilen die Dokument-IDs darstellen, speichert die Kapitel- oder Lesezeichenhandles die höhere Ebene in der Regel für die Verwendung in nachfolgenden Vorgängen, die gültige Dokument-IDs, Kapitel- oder Lesezeichenhandles umfassen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4737">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="c3671-4738">Auf der höheren Ebene werden die Daten aus Zeilenwerten in der Regel gespeichert, angezeigt oder anderweitig verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4738">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="c3671-4739">Für die Werte, die als verzögerte höhere Ebene markiert wurden, ruft den Wert mithilfe von CPMFetchValueIn-Nachrichten ab.</span><span class="sxs-lookup"><span data-stu-id="c3671-4739">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="c3671-4740">Die Suchbeschreibung wird ebenfalls an eine höhere Ebene zurückgegeben und kann von der höheren Ebene wiederverwendet oder untersucht werden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4740">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="c3671-4741">Wenn die höhere Ebene zu Informationszwecken Handles für Kapitel und Lesezeichen anfordert, die in den Zeilen empfangen wurden, kann dies folgendermaßen erfolgen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4741">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="c3671-4742">Verwenden Sie CPMGetQueryStatusExIn, um den Ausführungsstatus einer Abfrage sowie zusätzliche Statusinformationen zu überprüfen, z. B. die Anzahl der gefilterten Dokumente, die zu filternden Dokumente, das Verhältnis der von der Abfrage verarbeiteten Dokumente, die Gesamtzahl der Zeilen in der Abfrage und die Position des Lesezeichens im Rowset.</span><span class="sxs-lookup"><span data-stu-id="c3671-4742">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="c3671-4743">Verwenden Sie CPMGetNotify, um anzufordern, dass der Server den Client über Rowsetänderungen benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4743">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="c3671-4744">Verwenden Sie CPMGetApproximatePositionIn, um die ungefähre Position eines Lesezeichens in einem Kapitel anzufordern.</span><span class="sxs-lookup"><span data-stu-id="c3671-4744">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="c3671-4745">Verwenden Sie CPMCompareBmkIn, um einen Vergleich zweier Lesezeichen in einem Kapitel anzufordern.</span><span class="sxs-lookup"><span data-stu-id="c3671-4745">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="c3671-4746">Verwenden Sie CPMRestartPositionIn auf dem Server, um die Position des Cursors in den Anfang des Rowsets zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c3671-4746">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="c3671-4747">3.2.5.3 Empfangen einer CPMFetchValueOut-Antwort</span><span class="sxs-lookup"><span data-stu-id="c3671-4747">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="c3671-4748">Wenn der Client eine CPMGetRowsOut-Meldungsantwort vom Server empfängt, MUSS der Client folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c3671-4748">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="c3671-4749">Überprüfen Sie, ob das \_ Statusfeld im Header erfolg- oder fehlerbesagend ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4749">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="c3671-4750">Bei einem Fehler wird die höhere Ebene benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4750">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="c3671-4751">Fahren Sie andernfalls weiter unten fort.</span><span class="sxs-lookup"><span data-stu-id="c3671-4751">Otherwise, continue below.</span></span>
-   <span data-ttu-id="c3671-4752">Überprüfen Sie \_ fValueExist, und wenn diese Einstellung auf 0x00000000 die höhere Ebene benachrichtigen, dass der Wert nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="c3671-4752">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="c3671-4753">Andernfalls fügen Sie \_ cbValue-Bytes von vValue an den aktuellen Eigenschaftswert an.</span><span class="sxs-lookup"><span data-stu-id="c3671-4753">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="c3671-4754">Wenn \_ \_ fMoreExists auf 0x00000001 dann von \_ cbValue empfangene aktuelle Bytes erhöht \_ und eine CPMFetchValueIn-Nachricht an den Server gesendet wird, legen Sie \_ cbSoFar auf den Wert von Current Bytes Received, \_ cbPropSpec auf 0 (null) und \_ cbChunk auf die Puffergröße fest, die von der höheren Ebene gewünscht wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-4754">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="c3671-4755">Wenn \_ fMoreExists auf 0x00000000, geben Sie den Eigenschaftswert von Aktueller Eigenschaftswert auf die höhere Ebene an.</span><span class="sxs-lookup"><span data-stu-id="c3671-4755">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="c3671-4756">3.2.5.4 Empfangen einer CPMFreeCursorOut-Antwort</span><span class="sxs-lookup"><span data-stu-id="c3671-4756">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="c3671-4757">Wenn der Client eine erfolgreiche CPMFreeCursorOut-Nachrichtenantwort vom Server empfängt, MUSS der Client den \_ cCursorsRemaining-Wert an die höhere Ebene zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c3671-4757">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="c3671-4758">Die folgenden Informationen dienen nur zu Informationszwecken und werden nicht vom CISP-Client erzwungen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4758">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="c3671-4759">Von der höheren Ebene wird erwartet, dass sie Cursorhandles nachverfolgt und nicht diejenigen verwendet, die bereits freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4759">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="c3671-4760">Sobald die Anzahl von \_ cCursorsRemaining gleich 0x00000000 ist, kann die höhere Ebene die Verbindung verwenden, um eine andere Abfrage anzugeben (mithilfe einer CPMCreateQueryIn-Nachricht).</span><span class="sxs-lookup"><span data-stu-id="c3671-4760">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="c3671-4761">3.2.6 Timerereignisse</span><span class="sxs-lookup"><span data-stu-id="c3671-4761">3.2.6 Timer Events</span></span>

<span data-ttu-id="c3671-4762">Keine.</span><span class="sxs-lookup"><span data-stu-id="c3671-4762">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="c3671-4763">3.2.7 Andere lokale Ereignisse</span><span class="sxs-lookup"><span data-stu-id="c3671-4763">3.2.7 Other Local Events</span></span>

<span data-ttu-id="c3671-4764">Keine.</span><span class="sxs-lookup"><span data-stu-id="c3671-4764">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="c3671-4765">4 Beispiele für Protokolle</span><span class="sxs-lookup"><span data-stu-id="c3671-4765">4 Protocol Examples</span></span>

-   [<span data-ttu-id="c3671-4766">4.1 Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3671-4766">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="c3671-4767">4.2 Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c3671-4767">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="c3671-4768">4.1 Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3671-4768">4.1 Example 1</span></span>

<span data-ttu-id="c3671-4769">Im folgenden Beispiel betrachten wir ein Szenario, in dem der Benutzer JOHN auf Computer A die Dateigrößen abrufen möchte, die das Wort "Microsoft" aus dem Satz von Dokumenten enthalten, die auf Server X im KatalogSYSTEM gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="c3671-4769">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="c3671-4770">Angenommen, Computer A führt ein 32-Bit-Betriebssystem unter Windows XP und Computer X ein 32-Bit-Betriebssystem unter Windows Server 2003 aus.</span><span class="sxs-lookup"><span data-stu-id="c3671-4770">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="c3671-4771">Der Benutzer startet eine Suchanwendung und gibt die Suchabfrage ein.</span><span class="sxs-lookup"><span data-stu-id="c3671-4771">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="c3671-4772">Die Anwendung übergibt die Suchabfrage wiederum an den Protokollclient.</span><span class="sxs-lookup"><span data-stu-id="c3671-4772">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="c3671-4773">Der Protokollclient stellt eine Verbindung mit dem Indizierungsserver X her. Der Protokollclient verwendet die Named Pipe \\ Pipe \\ CI \_ SKADS, um über SMB eine Verbindung mit dem Server X herzustellen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4773">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="c3671-4774">Der Protokollclient bereitet dann eine CPMConnectIn-Nachricht mit den folgenden Werten vor:</span><span class="sxs-lookup"><span data-stu-id="c3671-4774">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="c3671-4775">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4775">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4776">**\_ msg** ist auf 0x000000C8 festgelegt und gibt an, dass es sich um eine CPMConnectIn-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4776">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="c3671-4777">**\_ status** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4777">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="c3671-4778">**\_ ulChecksum** enthält die Prüfsumme, die gemäß Abschnitt 3.2.4 berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-4778">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="c3671-4779">**\_ ulReserved2** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4779">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="c3671-4780">Der Text der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4780">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4781">**\_ iClientVersion** ist auf 0x00000008 festgelegt und gibt an, dass der Server das Prüfsummenfeld überprüfen soll.</span><span class="sxs-lookup"><span data-stu-id="c3671-4781">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="c3671-4782">**\_ fClientIsRemote** ist auf 0x00000001 festgelegt, was angibt, dass der Server ein Remoteserver ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4782">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="c3671-4783">**\_ cbBlob1** wird auf die Größe der Felder cPropSet, PropertySet1 und PropertySet2 in Bytes festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4783">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="c3671-4784">**\_ cbBlob2** ist auf 0x00000004 festgelegt (d. h. keine zusätzlichen Eigenschaftensätze).</span><span class="sxs-lookup"><span data-stu-id="c3671-4784">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="c3671-4785">**MachineName** ist auf A festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4785">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="c3671-4786">**UserName** ist auf JOHN festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4786">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="c3671-4787">**cPropSets** ist auf 0x00000002 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4787">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="c3671-4788">**Das PropertySet1-Feld** ist vom Typ CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4788">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="c3671-4789">Die CDbPropSet-Struktur, die das PropertySet1-Feld umfasst, wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4789">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="c3671-4790">**Das Feld GuidPropSet** ist auf A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4790">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="c3671-4791">Das Feld **cProperties** ist auf 0x00000004 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4791">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="c3671-4792">Das Feld **aProps** ist ein Array von CDbProp-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4792">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="c3671-4793">Für das **aProps \[ \] 0-Element:**</span><span class="sxs-lookup"><span data-stu-id="c3671-4793">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="c3671-4794">**PropId** ist auf 0x00000002 (DBPROP \_ CI CATALOG \_ \_ NAME) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4794">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="c3671-4795">**DBPROPOPTIONS** ist auf 0x0000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4795">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="c3671-4796">**DBPROPSTATUS** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4796">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3671-4797">Für das **ColId-Element:**</span><span class="sxs-lookup"><span data-stu-id="c3671-4797">For the **ColId** element:</span></span>
                -   <span data-ttu-id="c3671-4798">**eKind** ist auf 0x00000001 (DBKIND \_ GUID \_ PROPID) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4798">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="c3671-4799">**GUID** ist NULL (alle Nullen), d. h., der Wert gilt für die Abfrage, nicht nur für eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="c3671-4799">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="c3671-4800">**ulID** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4800">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3671-4801">Für das **vValue-Element:**</span><span class="sxs-lookup"><span data-stu-id="c3671-4801">For the **vValue** element:</span></span>
                -   <span data-ttu-id="c3671-4802">**vType** ist auf 0x001F (VT \_ LPWSTR) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4802">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="c3671-4803">**vValue** ist auf "SYSTEM", den Namen des gewünschten Katalogs, festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4803">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="c3671-4804">Für das **aProps \[ \] 1-Element:**</span><span class="sxs-lookup"><span data-stu-id="c3671-4804">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="c3671-4805">**PropId** ist auf 0x00000007 festgelegt (DBPROP \_ CI \_ QUERY \_ TYPE)</span><span class="sxs-lookup"><span data-stu-id="c3671-4805">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="c3671-4806">**DBPROPOPTIONS** ist auf 0x0000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4806">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="c3671-4807">**DBPROPSTATUS** ist auf0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4807">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="c3671-4808">Für das **ColId-Element:**</span><span class="sxs-lookup"><span data-stu-id="c3671-4808">For the **ColId** element:</span></span>
                -   <span data-ttu-id="c3671-4809">**eKind** ist auf 0x00000001 (DBKIND \_ GUID \_ PROPID) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4809">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="c3671-4810">**GUID** ist NULL (alle Nullen), d. h., der Wert gilt für die Abfrage, nicht nur für eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="c3671-4810">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="c3671-4811">**ulID** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4811">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3671-4812">Für das **vValue-Element:**</span><span class="sxs-lookup"><span data-stu-id="c3671-4812">For the **vValue** element:</span></span>
                -   <span data-ttu-id="c3671-4813">**vType** ist auf 0x0003 (VT \_ I4) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4813">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="c3671-4814">**vValue** ist auf 0x00000000 (CiNormal) festgelegt, was bedeutet, dass es sich um eine reguläre Abfrage handelt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4814">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="c3671-4815">Für das **aProps \[ \] 2-Element:**</span><span class="sxs-lookup"><span data-stu-id="c3671-4815">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="c3671-4816">**PropId** ist auf 0x00000004 (DBPROP \_ CI SCOPE \_ \_ FLAGS) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4816">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="c3671-4817">**DBPROPOPTIONS** ist auf 0x0000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4817">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="c3671-4818">**DBPROPSTATUS** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4818">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3671-4819">Für das **ColId-Element:**</span><span class="sxs-lookup"><span data-stu-id="c3671-4819">For the **ColId** element:</span></span>
                -   <span data-ttu-id="c3671-4820">**eKind** ist auf 0x00000001 (DBKIND \_ GUID \_ PROPID) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4820">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="c3671-4821">**GUID** ist NULL (alle Nullen), d. h., der Wert gilt für die Abfrage, nicht nur für eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="c3671-4821">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="c3671-4822">**ulID** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4822">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3671-4823">Für das **vValue-Element:**</span><span class="sxs-lookup"><span data-stu-id="c3671-4823">For the **vValue** element:</span></span>
                -   <span data-ttu-id="c3671-4824">**vType:** 0x1003 (VT \_ VECTOR \| VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="c3671-4824">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="c3671-4825">**vValue:** 0x00000001/0x00000001 (ein Element mit dem Wert 1), d. h. Suchunterordner</span><span class="sxs-lookup"><span data-stu-id="c3671-4825">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="c3671-4826">Für das **aProps \[ \] 3-Element:**</span><span class="sxs-lookup"><span data-stu-id="c3671-4826">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="c3671-4827">**PropId:** 0x00000003 (DBPROP \_ CI \_ INCLUDE \_ SCOPES)</span><span class="sxs-lookup"><span data-stu-id="c3671-4827">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="c3671-4828">**DBPROPOPTIONS:** 0x0000000</span><span class="sxs-lookup"><span data-stu-id="c3671-4828">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="c3671-4829">**DBPROPSTATUS:** 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-4829">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="c3671-4830">Für das **ColId-Element:**</span><span class="sxs-lookup"><span data-stu-id="c3671-4830">For the **ColId** element:</span></span>
                -   <span data-ttu-id="c3671-4831">**eKind** ist auf 0x00000001 (DBKIND \_ GUID \_ PROPID) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4831">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="c3671-4832">**GUID** ist NULL (alle Nullen), d. h., der Wert gilt für die Abfrage, nicht nur für eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="c3671-4832">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="c3671-4833">**ulID** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4833">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="c3671-4834">Für das **vValue-Element:**</span><span class="sxs-lookup"><span data-stu-id="c3671-4834">For the **vValue** element:</span></span>
                -   <span data-ttu-id="c3671-4835">**vType** ist auf 0x101F (VT \_ VECTOR \| VT \_ LPWSTR) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4835">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="c3671-4836">**vValue** ist auf 0x00000001/ 0x00000002 / " \\ " (ein Element mit einer 2-Zeichen-NULL-endende Zeichenfolge) festgelegt, was den Stammbereich bedeutet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4836">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="c3671-4837">Das **PropertySet2-Feld** ist vom Typ CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4837">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="c3671-4838">Die CDbPropSet-Struktur, die das PropertySet1-Feld umfasst, wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4838">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="c3671-4839">**GuidPropSet** ist auf AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4839">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="c3671-4840">Das Feld **cProperties** ist auf 0x00000001 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4840">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="c3671-4841">Das Feld **aProps** ist ein Array von CDbProp-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4841">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="c3671-4842">Für das **aProps \[ \] 0-Element:**</span><span class="sxs-lookup"><span data-stu-id="c3671-4842">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="c3671-4843">**PropId** ist auf 0x00000002 (DBPROP \_ MACHINE) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4843">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="c3671-4844">**DBPROPOPTIONS** ist auf 0x0000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4844">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="c3671-4845">**DBPROPSTATUS** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4845">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3671-4846">Für das **ColId-Element:**</span><span class="sxs-lookup"><span data-stu-id="c3671-4846">For the **ColId** element:</span></span>
                -   <span data-ttu-id="c3671-4847">**eKind** ist auf 0x00000001 (DBKIND \_ GUID \_ PROPID) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4847">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="c3671-4848">**GUID** ist NULL (alle Nullen), d. h., der Wert gilt für die Abfrage, nicht nur für eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="c3671-4848">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="c3671-4849">**ulID** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4849">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3671-4850">Für **vValue-Element:**</span><span class="sxs-lookup"><span data-stu-id="c3671-4850">For **vValue** element:</span></span>
                -   <span data-ttu-id="c3671-4851">**vType:** 0x0008 (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="c3671-4851">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="c3671-4852">**vValue:** 0x04/"X" (4 Bytes/NULL-terminierte Unicode-Zeichenfolge), was "X" -name eines Servers bedeutet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4852">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="c3671-4853">Das Feld **cExtPropSet** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4853">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="c3671-4854">**Das Array aPropertySets** ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4854">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="c3671-4855">Bei Bedarf werden verschiedene Auffüllungsfelder ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4855">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="c3671-4856">Die Nachricht wird an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4856">The message is sent to the server.</span></span>

4.  <span data-ttu-id="c3671-4857">Der Server überprüft, ob **\_ ulChecksum** korrekt ist, überprüft, ob der Benutzer berechtigt ist, diese Anforderung zu senden, und antwortet mit einer CPMConnectOut-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c3671-4857">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="c3671-4858">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4858">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4859">**\_ msg** ist auf 0x000000C8 festgelegt und gibt an, dass es sich um eine CPMConnectOut-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4859">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="c3671-4860">**\_ status** ist auf 0x0000000 festgelegt, die SUCCESS angibt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4860">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="c3671-4861">**\_ ulChecksum** ist auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4861">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="c3671-4862">**\_ ulReserved2** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4862">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="c3671-4863">Der Nachrichtentext wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4863">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4864">Das Feld **\_ serverVersion** ist auf 0x00000007 (32-Bit Windows XP oder 32-Bit Windows Server 2003) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4864">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="c3671-4865">**\_ Reservierte** Felder werden mit beliebigen Daten gefüllt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4865">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="c3671-4866">Der Client bereitet eine CPMCreateQueryIn-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="c3671-4866">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="c3671-4867">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4867">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4868">**\_ msg** ist auf 0x000000CA festgelegt, was angibt, dass es sich um eine CPMCreateQueryIn-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4868">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="c3671-4869">**\_ status** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4869">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="c3671-4870">**\_ ulChecksum** enthält die Prüfsumme, die gemäß 3.2.5 berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-4870">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="c3671-4871">**\_ ulReserved2** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4871">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="c3671-4872">Der Nachrichtentext wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4872">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4873">**Das** Feld Größe wird auf die Größe der restlichen Nachricht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4873">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="c3671-4874">Das Feld **CColumnSetPresent** ist auf 0x01 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4874">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="c3671-4875">**Das ColumnSet-Feld** ist vom Typ CColumnSet.</span><span class="sxs-lookup"><span data-stu-id="c3671-4875">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="c3671-4876">Die CColumnSet-Struktur, aus der dieses Feld besteht, wird wie folgt festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4876">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="c3671-4877">**\_ das Feld count** ist auf 0x00000001 festgelegt, der angibt, dass eine Spalte zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-4877">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="c3671-4878">**indexes-Array** ist 0x00000000 gibt den ersten Eintrag in \_ aPropSpec an.</span><span class="sxs-lookup"><span data-stu-id="c3671-4878">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="c3671-4879">Das Feld **CRestrictionPresent** ist auf 0x01 festgelegt, das angibt, dass das Feld **Einschränkung** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c3671-4879">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="c3671-4880">**Das Einschränkungsfeld** ist vom Typ CRestriction und auf festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4880">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="c3671-4881">**\_ ulType** ist auf 0x00000004 (RTContent) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4881">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="c3671-4882">**\_ weight** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4882">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="c3671-4883">Der Rest des Felds enthält eine CContentRestriction-Struktur:</span><span class="sxs-lookup"><span data-stu-id="c3671-4883">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="c3671-4884">**\_ Die Eigenschaft** ist auf GUID B725F130-47EF-101A-A5F1-02608c9eebac/0x00000001 (für PRSPEC \_ PROPID) /0x13 festgelegt, die den Dokumenttext darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4884">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="c3671-4885">**\_ Cc** ist auf 0x00000009 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4885">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="c3671-4886">**\_ pwcsphrase** wird auf die Zeichenfolge "Microsoft" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4886">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="c3671-4887">**\_ lcid** ist auf 0x409 (für Englisch) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4887">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="c3671-4888">**\_ ulGenerateMethod** ist auf 0x00000000 (genaue Übereinstimmung) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4888">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="c3671-4889">**CSortPresent** ist auf 0x00 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4889">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="c3671-4890">**CCategorizationSetPresent** ist auf 0x00 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4890">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="c3671-4891">**RowSetProperties** wird wie folgt festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4891">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="c3671-4892">**\_ uBooleanOptions** ist auf 0x00000001 (sequenziell) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4892">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="c3671-4893">**\_ ulMaxOpenRows** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4893">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="c3671-4894">**\_ ulMemoryUsage** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4894">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="c3671-4895">\_**cMaxResults** ist auf 0x00000100 festgelegt (höchstens 256 Zeilen zurückgeben).</span><span class="sxs-lookup"><span data-stu-id="c3671-4895">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="c3671-4896">**\_ cCmdTimeOut** ist auf 0x00000000 festgelegt (kein Timeout).</span><span class="sxs-lookup"><span data-stu-id="c3671-4896">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="c3671-4897">**PidMapper** ist auf:</span><span class="sxs-lookup"><span data-stu-id="c3671-4897">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="c3671-4898">**\_ count** ist auf 0x00000001 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4898">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="c3671-4899">**\_ aPropSpec** ist auf GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC/0x00000001 (für PRSPEC \_ PROPID) / 0x0000000c festgelegt, die die Windows-Dateigrößeneigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4899">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="c3671-4900">Der Server verarbeitet sie und antwortet mit einer CPMCreateQueryOut-Meldung.</span><span class="sxs-lookup"><span data-stu-id="c3671-4900">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="c3671-4901">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4901">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4902">**\_ msg** ist auf 0x000000CA festgelegt und gibt an, dass es sich um eine CPMCreateQueryOut-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4902">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="c3671-4903">**\_ status** ist auf SUCCESS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4903">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="c3671-4904">**\_ ulChecksum** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4904">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="c3671-4905">**\_ ulReserved2** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4905">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="c3671-4906">Der Nachrichtentext wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4906">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4907">**\_ fTrueSeqeuntial** ist auf 0x00000000 festgelegt, was angibt, dass die Abfrage einen Index verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="c3671-4907">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="c3671-4908">**\_ fWorkIdUnique** ist auf 0x00000001 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4908">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="c3671-4909">Das **aCursors-Array** enthält nur ein Element, das ein Cursorhandle für diese Abfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4909">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="c3671-4910">Der Wert hängt vom Status des Servers ab.</span><span class="sxs-lookup"><span data-stu-id="c3671-4910">The value depends on the state of the server.</span></span> <span data-ttu-id="c3671-4911">Angenommen, der zurückgegebene Wert ist 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="c3671-4911">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="c3671-4912">Der Client gibt eine CPMSetBindingsIn-Anforderungsnachricht aus, um das Format einer Zeile zu definieren.</span><span class="sxs-lookup"><span data-stu-id="c3671-4912">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="c3671-4913">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4913">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4914">**\_ msg** ist auf 0x000000D0 festgelegt, was angibt, dass es sich um eine CPMSetBindingsIn-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4914">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="c3671-4915">**\_ status** ist auf SUCCESS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4915">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="c3671-4916">**\_ ulChecksum** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4916">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="c3671-4917">**\_ ulReserved2** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4917">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="c3671-4918">Der Nachrichtentext wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4918">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4919">**\_ hCursor** ist auf 0xAAAAAAAA festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4919">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="c3671-4920">**\_ cbRow** ist auf 0x10 festgelegt (groß genug für Spalten).</span><span class="sxs-lookup"><span data-stu-id="c3671-4920">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="c3671-4921">**\_ cbBindingDesc** wird auf die Größe der Felder **\_ cColumns** und **\_ aColumns** kombiniert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4921">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="c3671-4922">**\_ cColumns** ist auf 0x00000001 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4922">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="c3671-4923">**\_ Das aColumns-Array** ist so festgelegt, dass es eine CTableColumn-Struktur enthält, die Folgendes enthält:</span><span class="sxs-lookup"><span data-stu-id="c3671-4923">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="c3671-4924">**\_ PropSpec** ist auf GUID b725f130-47ef-101a-a5-f1-02608c9eebac /0x00000001 (für PRSPEC \_ PROPID) / 0x0000000c festgelegt, die die Windows-Dateigrößeneigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4924">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="c3671-4925">**\_ vType** ist auf 0x0015 (VT \_ UI8) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4925">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="c3671-4926">**\_ ValueUsed** ist auf 0x01 festgelegt (Spalte in Zeile übertragen).</span><span class="sxs-lookup"><span data-stu-id="c3671-4926">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="c3671-4927">**\_ ValueOffset** ist auf 0x0002 (am Anfang der Zeile) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4927">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="c3671-4928">**\_ ValueSize** ist auf 0x08 (Größe einer VT \_ UI8) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4928">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="c3671-4929">**\_ StatusUsed** ist auf 0x01 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4929">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="c3671-4930">**\_ StatusOffset** ist auf 0x0A festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4930">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="c3671-4931">**\_ LengthUsed** ist auf 0x00 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4931">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="c3671-4932">Der Server verarbeitet sie und antwortet mit einer CPMSetBindingsIn-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c3671-4932">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="c3671-4933">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4933">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4934">**\_ msg** ist auf 0x000000D0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4934">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="c3671-4935">**\_ status** ist auf SUCCESS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4935">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="c3671-4936">**\_ ulChecksum** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4936">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="c3671-4937">**\_ ulReserved2** ist auf 0x00000000 (oder einen beliebigen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4937">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="c3671-4938">Der Client gibt eine CPMGetRowsIn-Anforderungsnachricht aus.</span><span class="sxs-lookup"><span data-stu-id="c3671-4938">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="c3671-4939">Angenommen, der Client ist bereit, an diesem Punkt 100 Zeilen zu akzeptieren, und möchte diese in aufsteigender Reihenfolge haben.</span><span class="sxs-lookup"><span data-stu-id="c3671-4939">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="c3671-4940">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4940">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4941">**\_ msg** ist auf 0x000000CC festgelegt, was angibt, dass es sich um eine CPMGetRowsIn-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4941">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="c3671-4942">**\_ status** ist auf 0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3671-4942">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="c3671-4943">**\_ ulChecksum** enthält die Prüfsumme, die gemäß Abschnitt 0 berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="c3671-4943">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="c3671-4944">**\_ ulReserved2** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4944">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="c3671-4945">Der Text der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4945">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4946">**\_ hCursor** ist auf 0xAAAAAAAA festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4946">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="c3671-4947">**\_ cRowsToTransfer** ist auf 0x00000064 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4947">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="c3671-4948">**\_ cRowWidth** ist auf 0x00000010 (aus Bindungen) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4948">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="c3671-4949">**\_ cbSeek** ist auf 0x14 festgelegt, wobei es sich um die Größe der Felder eType, \_ chapt und CRowSeekNext handelt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4949">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="c3671-4950">**\_ cbReserved** ist auf 0x18 (0x14 plus \_ cbSeek) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4950">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="c3671-4951">**\_ cbReadBuffer** ist auf 0x800 festgelegt (0x64 \* 0x10 auf das nächste Vielfache von 0x200 aufgerundet).</span><span class="sxs-lookup"><span data-stu-id="c3671-4951">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="c3671-4952">**\_ ulClientBase** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4952">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="c3671-4953">**\_ fBwdfetch** wird auf 0x00000000 festgelegt, der angibt, dass die Zeilen in vorwärts gerichteter Reihenfolge abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4953">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="c3671-4954">**eType** wird auf 0x0000001 festgelegt, der angibt, dass der Client die nächsten Zeilen benötigt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4954">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="c3671-4955">**\_ chapt** ist auf 0 (kein Kapitelergebnis) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4955">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="c3671-4956">**SeekDescription** ist auf CRowSeekNext festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4956">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="c3671-4957">Die CRowSeekNext-Struktur enthält die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="c3671-4957">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="c3671-4958">**CiTblChapt** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4958">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="c3671-4959">**\_ hRegion** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4959">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="c3671-4960">**\_ cSkip** ist auf 0 festgelegt, was angibt, dass der Client keine Zeilen überspringen möchte.</span><span class="sxs-lookup"><span data-stu-id="c3671-4960">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="c3671-4961">Der Server verarbeitet sie und antwortet mit einer CPMGetRowsOut-Meldung.</span><span class="sxs-lookup"><span data-stu-id="c3671-4961">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="c3671-4962">Angenommen, der Server hat 100 Dokumente gefunden, die das Wort "Microsoft" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c3671-4962">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="c3671-4963">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4963">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4964">**\_ msg** ist auf 0x000000CC festgelegt und gibt an, dass es sich um eine CPMGetRowsOut-Meldung handelt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4964">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="c3671-4965">**\_ status** ist auf SUCCESS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4965">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="c3671-4966">**\_ ulChecksum** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4966">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="c3671-4967">**\_ ulReserved2** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4967">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="c3671-4968">Der Text der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4968">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4969">**\_ CRowsReturned** ist auf 0x00000064 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4969">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="c3671-4970">**eType** ist auf 0x00000001 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4970">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="c3671-4971">**\_ chapt** ist auf 0x00000000 festgelegt (kein Kapitelergebnis).</span><span class="sxs-lookup"><span data-stu-id="c3671-4971">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="c3671-4972">**SeekDescription** enthält eine CRowSeekNext-Struktur, die wie folgt aufgefüllt wird:</span><span class="sxs-lookup"><span data-stu-id="c3671-4972">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="c3671-4973">**CiTblChapt** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4973">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="c3671-4974">**\_ hRegion** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4974">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="c3671-4975">**\_ cSkip** ist auf 0 festgelegt, was angibt, dass der Client keine Zeilen überspringen möchte.</span><span class="sxs-lookup"><span data-stu-id="c3671-4975">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="c3671-4976">**Zeilen** enthalten die Größe der 100 Dokumente, die das Wort "Microsoft" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c3671-4976">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="c3671-4977">Da es sich um Daten mit fester Größe handelt, wird sie einfach als Liste mit 100 ganzen Zahlen ohne Vorzeichen mit 8 Byte strukturiert.</span><span class="sxs-lookup"><span data-stu-id="c3671-4977">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="c3671-4978">Der Client sendet eine CPMDisconnect-Nachricht, um die Verbindung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="c3671-4978">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="c3671-4979">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4979">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="c3671-4980">**\_ msg** ist auf 0x000000C9 festgelegt und gibt an, dass es sich um eine CPMDisconnect-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4980">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="c3671-4981">**\_ status** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4981">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="c3671-4982">**\_ ulChecksum** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4982">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="c3671-4983">Der Server verarbeitet die Nachricht und entfernt den gesamten Clientstatus.</span><span class="sxs-lookup"><span data-stu-id="c3671-4983">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="c3671-4984">4.2 Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c3671-4984">4.2 Example 2</span></span>

<span data-ttu-id="c3671-4985">Im vorherigen Beispiel war die Abfrage recht einfach.</span><span class="sxs-lookup"><span data-stu-id="c3671-4985">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="c3671-4986">Betrachten wir nun eine etwas komplexere Abfrage.</span><span class="sxs-lookup"><span data-stu-id="c3671-4986">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="c3671-4987">Angenommen, der Benutzer möchte die Größe der Dokumente abrufen, die die folgenden Wörter enthalten: "Microsoft" und "Office".</span><span class="sxs-lookup"><span data-stu-id="c3671-4987">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="c3671-4988">Dies wird angegeben, indem Sie das Feld Einschränkung in der in Schritt 5 gesendeten CPMCreateQueryIn-Nachricht wie folgt ändern:</span><span class="sxs-lookup"><span data-stu-id="c3671-4988">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="c3671-4989">Das Feld **Einschränkung** hat den Typ CRestriction und ist auf Folgendes festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c3671-4989">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="c3671-4990">**\_ ulType** ist auf 0x00000004 (RTAnd) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4990">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="c3671-4991">**\_ weight** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4991">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="c3671-4992">Der Rest des Felds enthält eine CNodeRestriction-Struktur:</span><span class="sxs-lookup"><span data-stu-id="c3671-4992">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="c3671-4993">**\_ cNode** ist auf 0x00000002 festgelegt und gibt an, dass das PaNode-Array zwei Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="c3671-4993">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="c3671-4994">Das **\_ PaNode-Feld** ist ein Array von zwei CRestriction-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="c3671-4994">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="c3671-4995">**\_ paNode \[ 0 \]** enthält:</span><span class="sxs-lookup"><span data-stu-id="c3671-4995">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="c3671-4996">**\_ ulType** ist auf 0x00000004 (RTContent) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4996">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="c3671-4997">**\_ weight** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4997">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3671-4998">Der Rest des Felds enthält eine CContentRestriction-Struktur:</span><span class="sxs-lookup"><span data-stu-id="c3671-4998">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="c3671-4999">**\_ Die Eigenschaft** ist auf GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (für PRSPEC \_ PROPID) /0x13 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-4999">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="c3671-5000">**\_ Cc** ist auf 0x00000009 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-5000">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="c3671-5001">**\_ pwcsphrase** wird auf die Zeichenfolge "Microsoft" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-5001">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="c3671-5002">**\_ lcid** ist auf 0x409 (für Englisch) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-5002">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="c3671-5003">**\_ ulGenerateMethod** ist auf 0x00000000 (genaue Übereinstimmung) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-5003">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="c3671-5004">**\_ paNode \[ 1 \]** enthält:</span><span class="sxs-lookup"><span data-stu-id="c3671-5004">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="c3671-5005">**\_ ulType** ist auf 0x00000004 (RTContent) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-5005">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="c3671-5006">**\_ weight** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-5006">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="c3671-5007">Der Rest des Felds enthält eine CContentRestriction-Struktur:</span><span class="sxs-lookup"><span data-stu-id="c3671-5007">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="c3671-5008">**\_ Die Eigenschaft** ist auf GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (für PRSPEC \_ PROPID) /0x13 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-5008">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="c3671-5009">**\_ Cc** ist auf 0x00000006 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-5009">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="c3671-5010">**\_ pwcsphrase** ist auf die Zeichenfolge "Office" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-5010">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="c3671-5011">**\_ lcid** ist auf 0x409 (für Englisch) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-5011">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="c3671-5012">**\_ ulGenerateMethod** ist auf 0x00000000 (genaue Übereinstimmung) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3671-5012">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="c3671-5013">5 Sicherheit</span><span class="sxs-lookup"><span data-stu-id="c3671-5013">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="c3671-5014">5.1 Sicherheitsüberlegungen für Ausführende</span><span class="sxs-lookup"><span data-stu-id="c3671-5014">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="c3671-5015">Indizierungsimplementierungen, die sichere Inhalte indizieren, sollten die Verwendung des von SMB MS-SMB bereitgestellten Benutzerkontexts in Betracht ziehen, um Suchergebnisse zu kürzen und nur die zurückzugeben, \[ auf die der \] Aufrufer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="c3671-5015">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="c3671-5016">5.2 Index von Sicherheitsparameter</span><span class="sxs-lookup"><span data-stu-id="c3671-5016">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="c3671-5017">Sicherheitsparameter</span><span class="sxs-lookup"><span data-stu-id="c3671-5017">Security Parameter</span></span>  | <span data-ttu-id="c3671-5018">`Section`</span><span class="sxs-lookup"><span data-stu-id="c3671-5018">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="c3671-5019">Ebene des Identitätswechsels</span><span class="sxs-lookup"><span data-stu-id="c3671-5019">Impersonation level</span></span> | <span data-ttu-id="c3671-5020">2.1</span><span class="sxs-lookup"><span data-stu-id="c3671-5020">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="c3671-5021">6 Index des versionsspezifischen Verhaltens</span><span class="sxs-lookup"><span data-stu-id="c3671-5021">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="c3671-5022">Versionsspezifisches Verhalten</span><span class="sxs-lookup"><span data-stu-id="c3671-5022">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="c3671-5023">`Section`</span><span class="sxs-lookup"><span data-stu-id="c3671-5023">Section</span></span>   | <span data-ttu-id="c3671-5024">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c3671-5024">Windows 2000</span></span> | <span data-ttu-id="c3671-5025">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c3671-5025">Windows XP</span></span> | <span data-ttu-id="c3671-5026">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c3671-5026">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="c3671-5027">Dieses Protokoll ist unter Windows 2000, Windows XP, Windows Server 2003 und Windows Vista implementiert.</span><span class="sxs-lookup"><span data-stu-id="c3671-5027">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="c3671-5028">1.3.2</span><span class="sxs-lookup"><span data-stu-id="c3671-5028">1.3.2</span></span>     | <span data-ttu-id="c3671-5029">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5029">X</span></span>            | <span data-ttu-id="c3671-5030">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5030">X</span></span>          | <span data-ttu-id="c3671-5031">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5031">X</span></span>                   |
| <span data-ttu-id="c3671-5032">Anwendungen interagieren in der Regel mit einem OLE DB-Wrapper.</span><span class="sxs-lookup"><span data-stu-id="c3671-5032">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="c3671-5033">1.4</span><span class="sxs-lookup"><span data-stu-id="c3671-5033">1.4</span></span>       | <span data-ttu-id="c3671-5034">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5034">X</span></span>            | <span data-ttu-id="c3671-5035">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5035">X</span></span>          | <span data-ttu-id="c3671-5036">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5036">X</span></span>                   |
| <span data-ttu-id="c3671-5037">NTSTATUS-Werte</span><span class="sxs-lookup"><span data-stu-id="c3671-5037">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="c3671-5038">1.8</span><span class="sxs-lookup"><span data-stu-id="c3671-5038">1.8</span></span>       | <span data-ttu-id="c3671-5039">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5039">X</span></span>            | <span data-ttu-id="c3671-5040">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5040">X</span></span>          | <span data-ttu-id="c3671-5041">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5041">X</span></span>                   |
| <span data-ttu-id="c3671-5042">Der Client legt das \_ Statusfeld in jedem Nachrichtenheader fest.</span><span class="sxs-lookup"><span data-stu-id="c3671-5042">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="c3671-5043">2.2.2</span><span class="sxs-lookup"><span data-stu-id="c3671-5043">2.2.2</span></span>     | <span data-ttu-id="c3671-5044">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5044">X</span></span>            | <span data-ttu-id="c3671-5045">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5045">X</span></span>          | <span data-ttu-id="c3671-5046">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5046">X</span></span>                   |
| <span data-ttu-id="c3671-5047">cPendingScans-Wert ist in der Regel 0 (null)</span><span class="sxs-lookup"><span data-stu-id="c3671-5047">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="c3671-5048">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="c3671-5048">2.2.3.1</span></span>   | <span data-ttu-id="c3671-5049">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5049">X</span></span>            | <span data-ttu-id="c3671-5050">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5050">X</span></span>          | <span data-ttu-id="c3671-5051">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5051">X</span></span>                   |
| <span data-ttu-id="c3671-5052">iClientVersion-Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-5052">iClientVersion value</span></span>                                                                              | <span data-ttu-id="c3671-5053">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="c3671-5053">2.2.3.6</span></span>   | <span data-ttu-id="c3671-5054">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5054">X</span></span>            | <span data-ttu-id="c3671-5055">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5055">X</span></span>          | <span data-ttu-id="c3671-5056">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5056">X</span></span>                   |
| <span data-ttu-id="c3671-5057">\_cbChunk-Wert</span><span class="sxs-lookup"><span data-stu-id="c3671-5057">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="c3671-5058">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="c3671-5058">2.2.3.19</span></span>  | <span data-ttu-id="c3671-5059">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5059">X</span></span>            | <span data-ttu-id="c3671-5060">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5060">X</span></span>          | <span data-ttu-id="c3671-5061">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5061">X</span></span>                   |
| <span data-ttu-id="c3671-5062">32-Bit- und 64-Bit-Speicheradressen</span><span class="sxs-lookup"><span data-stu-id="c3671-5062">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="c3671-5063">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="c3671-5063">3.2.4.2.4</span></span> | <span data-ttu-id="c3671-5064">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5064">X</span></span>            | <span data-ttu-id="c3671-5065">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5065">X</span></span>          | <span data-ttu-id="c3671-5066">X</span><span class="sxs-lookup"><span data-stu-id="c3671-5066">X</span></span>                   |



 

 

 





