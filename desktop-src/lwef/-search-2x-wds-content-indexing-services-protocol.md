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
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="64c16-103">Inhaltsindizierungsdienste-Protokoll</span><span class="sxs-lookup"><span data-stu-id="64c16-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="64c16-104">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="64c16-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="64c16-105">Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="64c16-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="64c16-106">Protokollspezifikation, Version 0,12</span><span class="sxs-lookup"><span data-stu-id="64c16-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="64c16-107">1 Einführung</span><span class="sxs-lookup"><span data-stu-id="64c16-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="64c16-108">1.1 Glossar</span><span class="sxs-lookup"><span data-stu-id="64c16-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="64c16-109">1.2 Verweise</span><span class="sxs-lookup"><span data-stu-id="64c16-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="64c16-110">1,3-Protokoll Übersicht (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="64c16-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="64c16-111">1.4 Beziehung zu anderen Protokollen</span><span class="sxs-lookup"><span data-stu-id="64c16-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="64c16-112">1,5 Voraussetzungen und Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="64c16-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="64c16-113">1.6 Anwendbarkeitsanweisung</span><span class="sxs-lookup"><span data-stu-id="64c16-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="64c16-114">1.7 Versionsverwaltung und Funktionsübertragung</span><span class="sxs-lookup"><span data-stu-id="64c16-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="64c16-115">1.8 Durch Hersteller erweiterbare Felder</span><span class="sxs-lookup"><span data-stu-id="64c16-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="64c16-116">1.9 Zuweisungen von Standards</span><span class="sxs-lookup"><span data-stu-id="64c16-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="64c16-117">2\. Nachrichten</span><span class="sxs-lookup"><span data-stu-id="64c16-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="64c16-118">2.1 Transport</span><span class="sxs-lookup"><span data-stu-id="64c16-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="64c16-119">2.2 Nachrichtensyntax</span><span class="sxs-lookup"><span data-stu-id="64c16-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="64c16-120">3 Protokolldetails</span><span class="sxs-lookup"><span data-stu-id="64c16-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="64c16-121">3,1 Server Details</span><span class="sxs-lookup"><span data-stu-id="64c16-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="64c16-122">3,2 Client Details</span><span class="sxs-lookup"><span data-stu-id="64c16-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="64c16-123">4 Beispiele für Protokolle</span><span class="sxs-lookup"><span data-stu-id="64c16-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="64c16-124">4,1 Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="64c16-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="64c16-125">4,2 Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="64c16-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="64c16-126">5 Sicherheit</span><span class="sxs-lookup"><span data-stu-id="64c16-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="64c16-127">5.1 Sicherheitsüberlegungen für Ausführende</span><span class="sxs-lookup"><span data-stu-id="64c16-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="64c16-128">5.2 Index von Sicherheitsparameter</span><span class="sxs-lookup"><span data-stu-id="64c16-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="64c16-129">6 Index des Versions spezifischen Verhaltens</span><span class="sxs-lookup"><span data-stu-id="64c16-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="64c16-130">Dieses Dokument ist eine Spezifikation des Content Index Service-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="64c16-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="64c16-131">Die Dokumentation zum Arbeitsgruppen Server-Protokoll Programm (WSPP) ist für die Verwendung in Verbindung mit der Dokumentation zu öffentlichen Standards, den Konzepten der Netzwerk Programmierung und der verteilten Systeme von Windows-Arbeitsgruppen vorgesehen und geht davon aus, dass der Reader entweder mit dem oben erwähnten Material vertraut ist oder sofort darauf zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="64c16-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="64c16-132">Für eine WSPP-Protokollspezifikation ist die Verwendung von Microsoft-Programmier Tools oder Programmierumgebungen nicht erforderlich, damit ein Lizenznehmer eine Implementierung entwickeln kann.</span><span class="sxs-lookup"><span data-stu-id="64c16-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="64c16-133">Lizenznehmer, die Zugriff auf Microsoft-Programmier Tools und-Umgebungen haben, können Sie nutzen.</span><span class="sxs-lookup"><span data-stu-id="64c16-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="64c16-134">1 Einführung</span><span class="sxs-lookup"><span data-stu-id="64c16-134">1 Introduction</span></span>

-   [<span data-ttu-id="64c16-135">1.1 Glossar</span><span class="sxs-lookup"><span data-stu-id="64c16-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="64c16-136">1.2 Verweise</span><span class="sxs-lookup"><span data-stu-id="64c16-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="64c16-137">1,3-Protokoll Übersicht (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="64c16-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="64c16-138">1.4 Beziehung zu anderen Protokollen</span><span class="sxs-lookup"><span data-stu-id="64c16-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="64c16-139">1,5 Voraussetzungen und Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="64c16-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="64c16-140">1.6 Anwendbarkeitsanweisung</span><span class="sxs-lookup"><span data-stu-id="64c16-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="64c16-141">1.7 Versionsverwaltung und Funktionsübertragung</span><span class="sxs-lookup"><span data-stu-id="64c16-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="64c16-142">1.8 Durch Hersteller erweiterbare Felder</span><span class="sxs-lookup"><span data-stu-id="64c16-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="64c16-143">1.9 Zuweisungen von Standards</span><span class="sxs-lookup"><span data-stu-id="64c16-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="64c16-144">1.1 Glossar</span><span class="sxs-lookup"><span data-stu-id="64c16-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="64c16-145">Die folgenden Begriffe sind im Glossar Abschnitt von \[ ms-sys definiert \] :</span><span class="sxs-lookup"><span data-stu-id="64c16-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="64c16-146">GUID</span><span class="sxs-lookup"><span data-stu-id="64c16-146">GUID</span></span>
> -   <span data-ttu-id="64c16-147">Little-in-</span><span class="sxs-lookup"><span data-stu-id="64c16-147">Little Endian</span></span>
> -   <span data-ttu-id="64c16-148">Named Pipe</span><span class="sxs-lookup"><span data-stu-id="64c16-148">Named Pipe</span></span>
> -   <span data-ttu-id="64c16-149">Pfad</span><span class="sxs-lookup"><span data-stu-id="64c16-149">Path</span></span>

 

<span data-ttu-id="64c16-150">**Bindung**: eine Anforderung zum Einschließen einer bestimmten **Spalte** in ein zurück gegebenes **Rowset** .</span><span class="sxs-lookup"><span data-stu-id="64c16-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="64c16-151">Die **Bindung** gibt eine Eigenschaft an, die in den Suchergebnissen enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="64c16-152">**Bookmark**: ein Marker, der eine Zeile innerhalb einer Gruppe von Zeilen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="64c16-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="64c16-153">**Catalog**: die Organisationseinheit der obersten Ebene im Index Dienst.</span><span class="sxs-lookup"><span data-stu-id="64c16-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="64c16-154">Sie stellt einen Satz indizierter Dokumente dar, mit denen Abfragen mithilfe des Inhalts Indizierungs Dienst Protokolls ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="64c16-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="64c16-155">**Category**: eine hierarchische Gruppierung von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="64c16-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="64c16-156">Beispielsweise kann ein Abfrageergebnis, das Autoren-und Titel Spalten enthält, basierend auf dem Autor kategorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="64c16-157">Jede Gruppe von Zeilen, die den gleichen Wert für Author enthält, würde eine Kategorie darstellen.</span><span class="sxs-lookup"><span data-stu-id="64c16-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="64c16-158">**Kapitel** : ein Bereich von **Zeilen** innerhalb einer Reihe von **Zeilen** .</span><span class="sxs-lookup"><span data-stu-id="64c16-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="64c16-159">**Column**: der Container für einen einzelnen Typ von Informationen in einer **Zeile** .</span><span class="sxs-lookup"><span data-stu-id="64c16-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="64c16-160">Spalten werden Eigenschaftsnamen zugeordnet, und es wird angegeben, welche Eigenschaften für die **Befehls** **Strukturelemente der** Suchabfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="64c16-161">**Befehls** Struktur: eine Kombination aus **Einschränkungen** , **Kategorien** und **Sortier Reihenfolgen** , die für die Suchabfrage angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="64c16-162">**Cursor**: eine Entität, die als Mechanismus verwendet wird, um eine **Zeile** oder einen kleinen **Zeilen** Block gleichzeitig in einem Satz von Daten zu bearbeiten, die in einem Resultset zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="64c16-163">Ein **Cursor** wird auf einer einzelnen **Zeile** im Resultset positioniert.</span><span class="sxs-lookup"><span data-stu-id="64c16-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="64c16-164">Nachdem der **Cursor** auf einer Zeile positioniert wurde, können Vorgänge für diese **Zeile** oder für einen **Zeilen** Block, beginnend an dieser Position, ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="64c16-165">**Handle**: ein Token, das zum Identifizieren von und Aufrufen von **Cursorn** , **Kapiteln** und **Lesezeichen** verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="64c16-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="64c16-166">**Index**: eine persistente Struktur, die den Text Inhalt enthält, der von einem **Indizierungs Dienst** aus Dateien entnommen wurde.</span><span class="sxs-lookup"><span data-stu-id="64c16-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="64c16-167">Dies schließt die Liste der Wörter ein, die zusammen mit dem enthaltenden Dateinamen, dem Wort **Speicherort und** dem Gebiets Schema gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="64c16-168">**Indizierung**: der Prozess des Extrahierens von Text und Eigenschaften aus Dateien und Speichern der extrahierten Werte in den **Indizes** (für Text) und dem **Eigenschafts Cache** (für-Eigenschaften).</span><span class="sxs-lookup"><span data-stu-id="64c16-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="64c16-169">**Indizierungs Dienst**: ein Dienst, der indizierte **Kataloge** für den Inhalt und die Eigenschaften von Dateisystemen erstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="64c16-170">Anwendungen können in den Katalogen nach Informationen aus den Dateien im indizierten Dateisystem suchen.</span><span class="sxs-lookup"><span data-stu-id="64c16-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="64c16-171">**Locale**: ein Bezeichner, wie in \[ MS-GPSI \] Anhang A angegeben, der die für die Sprache relevanten Einstellungen angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="64c16-172">Diese Einstellungen geben an, wie Datumsangaben und Uhrzeiten formatiert werden sollen, Elemente alphabetisch sortiert werden müssen, Zeichen folgen verglichen werden sollen usw.</span><span class="sxs-lookup"><span data-stu-id="64c16-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="64c16-173">**Abfragen in natürlicher Sprache**: eine Abfrage, die anstelle der Abfrage Syntax mit der menschlichen Sprache erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="64c16-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="64c16-174">**Rausch Wort**: ein Wort, das vom Indizierungs Dienst ignoriert wird, wenn es in den für die Suchabfrage angegebenen **Einschränkungen** vorhanden ist, da es wenig diskriminierenden Wert hat.</span><span class="sxs-lookup"><span data-stu-id="64c16-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="64c16-175">Zu den englischen Beispielen zählen "a", "and" und "The".</span><span class="sxs-lookup"><span data-stu-id="64c16-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="64c16-176">**Eigenschafts Cache**: ein Cache von Dateieigenschaften, die von einem **Indizierungs Dienst** extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="64c16-177">**Eigenschafts Indizierung**: der Prozess, bei dem ein **Index** von **Werttyp Eigenschaften** eines Dokuments erstellt wird, einschließlich Autor, Betreff, Typ, Wort Anzahl, gedruckte Seitenanzahl und beliebiger anderer Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="64c16-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="64c16-178">**Einschränkung**: ein Satz von Bedingungen, die eine Datei erfüllen muss, um in die Suchergebnisse aufgenommen zu werden, die der **Indizierungs Dienst** als Antwort auf eine Suchabfrage zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="64c16-179">Eine **Einschränkung** schränkt den Fokus einer Suchabfrage ein und schränkt die Dateien ein, die der **Indizierungs Dienst** in den Suchergebnissen in die Suchergebnisse eingibt, sodass Sie nur diejenigen enthalten, die den Bedingungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="64c16-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="64c16-180">**Row**: die Auflistung von **Spalten** , die die Eigenschaftswerte enthält, die eine einzelne Datei aus dem Satz von Dateien beschreiben, die mit den in der Suchabfrage an den **Indizierungs Dienst** angegebenen **Einschränkungen** übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="64c16-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="64c16-181">**Rowset**: eine Reihe von **Zeilen** , die in den Suchergebnissen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="64c16-182">**Sortierreihenfolge**: der Satz von Regeln in einer Suchabfrage, die die Reihenfolge der Zeilen im Suchergebnis definieren.</span><span class="sxs-lookup"><span data-stu-id="64c16-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="64c16-183">Jede Regel besteht aus einer Eigenschaft (Name, Größe usw.) und einer Richtung für die Reihenfolge (aufsteigend oder absteigend).</span><span class="sxs-lookup"><span data-stu-id="64c16-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="64c16-184">Mehrere Regeln werden sequenziell angewendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="64c16-185">**Texttyp-Eigenschaft**: eine Eigenschaft, die den Inhalt eines Dokuments beschreibt und nur unformatierten Text enthält, der mit dem Namen verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="64c16-186">**Value-Type-Eigenschaft**: eine Eigenschaft, die ein einzelnes Attribut eines gesamten Dokuments beschreibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="64c16-187">Eine Werttyp Eigenschaft hat eine Datentyp-ID und einen Wert dieses Datentyps, der mit dem Namen verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="64c16-188">**Virtual root**: ein alternativer Pfad zu einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="64c16-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="64c16-189">Ein physischer Ordner kann über 0 (null) oder mehr virtuelle Stämme verfügen.</span><span class="sxs-lookup"><span data-stu-id="64c16-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="64c16-190">Pfade, die mit einem virtuellen Stamm beginnen, werden als virtuelle Pfade bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="64c16-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="64c16-191">/Server/vanityroot könnte z. b. ein virtuelles Stammverzeichnis von C: \\ IIS \\ Web "Ordner1" sein \\ .</span><span class="sxs-lookup"><span data-stu-id="64c16-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="64c16-192">Dann hätte die Datei C: \\ IIS \\ Web \\ "Ordner1"default.htm den \\ virtuellen Pfad/Server/vanityroot/default.htm.</span><span class="sxs-lookup"><span data-stu-id="64c16-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="64c16-193">**Kann, sollte, muss, sollte nicht, dürfen nicht**: diese Begriffe (in allen Caps) werden wie unter RFC2119 beschrieben \[ verwendet \] .</span><span class="sxs-lookup"><span data-stu-id="64c16-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="64c16-194">Alle Aussagen zu optionalem Verhalten enthalten die Worte KÖNNEN, SOLLTEN oder SOLLTEN NICHT.</span><span class="sxs-lookup"><span data-stu-id="64c16-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="64c16-195">1.2 Verweise</span><span class="sxs-lookup"><span data-stu-id="64c16-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="64c16-196">1.2.1 Normative Verweise</span><span class="sxs-lookup"><span data-stu-id="64c16-196">1.2.1 Normative References</span></span>

<span data-ttu-id="64c16-197">\[IEEE754 \] Institute of Electrical and Electronics Engineers, "Standard für binäre Floating-Point Arithmetik", IEEE 754-1985, Oktober 1985, https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="64c16-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="64c16-198">\[MS-DCOM \] Microsoft Corporation, "verteilte Component Object Model Remote Protokolle", Juni 2006.</span><span class="sxs-lookup"><span data-stu-id="64c16-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="64c16-199">\[MS-GPSI \] Microsoft Corporation, "Gruppenrichtlinie für die Softwareinstallation Extension", Juni 2006.</span><span class="sxs-lookup"><span data-stu-id="64c16-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="64c16-200">\[MS-SMB \] Microsoft Corporation, "Microsoft Server Message Block (SMB)-Protokoll und-Erweiterungen", Mai 2006.</span><span class="sxs-lookup"><span data-stu-id="64c16-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="64c16-201">\[MS-sys \] Microsoft Corporation, "System Übersicht V4", Juli 2006.</span><span class="sxs-lookup"><span data-stu-id="64c16-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="64c16-202">\[Salton \] Salton, G., "Automatische Text Verarbeitung: Transformations Analyse und Abruf von Informationen nach Computer", 1988, ISBN 0-201-2227-8.</span><span class="sxs-lookup"><span data-stu-id="64c16-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="64c16-203">\[Unicode: \] das Unicode-Konsortium "der Unicode-Standard, Version 2,0", 1996, https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="64c16-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="64c16-204">1.2.2 Informative Verweise</span><span class="sxs-lookup"><span data-stu-id="64c16-204">1.2.2 Informative References</span></span>

<span data-ttu-id="64c16-205">\[MSDN-OLEDB \] Microsoft Corporation, OLE DB https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .</span><span class="sxs-lookup"><span data-stu-id="64c16-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="64c16-206">\[MSDN-queryerr \] Microsoft Corporation, Query-Execution-Werte, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="64c16-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="64c16-207">1,3-Protokoll Übersicht (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="64c16-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="64c16-208">Ein Content- **Indizierungs Dienst** hilft bei der effizienten Organisation der extrahierten Funktionen einer Sammlung von Dokumenten.</span><span class="sxs-lookup"><span data-stu-id="64c16-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="64c16-209">Das Content Index Service-Protokoll (CISP) ermöglicht einem Client, mit einem Server zu kommunizieren, der einen Indizierungs Dienst zum Ausstellen von Abfragen und zum Verwalten des Index Servers durch einen Administrator verwendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="64c16-210">Beim Verarbeiten von Dateien analysiert ein Index Dienst einen Satz von Dokumenten und organisiert seinen Inhalt so neu, dass die **Eigenschaften** dieser Dokumente als Reaktion auf Abfragen effizient zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="64c16-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="64c16-211">Eine Auflistung von Dokumenten, die abgefragt werden können, umfasst einen **Katalog** .</span><span class="sxs-lookup"><span data-stu-id="64c16-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="64c16-212">Ein Katalog kann einen **Index** (für kurz Verweise auf Text) und einen **Eigenschafts Cache** (für den schnellen Abruf von Eigenschafts Werten) enthalten.</span><span class="sxs-lookup"><span data-stu-id="64c16-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="64c16-213">Konzeptionell besteht ein Katalog aus einer logischen "Tabelle" von Eigenschaften mit dem Text oder Wert und dem entsprechenden Gebiets Schema, das in **Spalten** der Tabelle gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="64c16-214">Jede Zeile der Tabelle entspricht einem separaten Dokument im Geltungsbereich des Katalogs, und jede "Spalte" der Tabelle entspricht einer Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="64c16-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="64c16-215">Die von CISP ausgeführten speziellen Aufgaben werden in zwei Funktionsbereichen gruppiert:</span><span class="sxs-lookup"><span data-stu-id="64c16-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="64c16-216">Remote Verwaltung von Indizierungs Dienst Katalogen</span><span class="sxs-lookup"><span data-stu-id="64c16-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="64c16-217">Remote Abfragen von Indizierungs Dienst Katalogen.</span><span class="sxs-lookup"><span data-stu-id="64c16-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="64c16-218">1.3.1 Remote Verwaltungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="64c16-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="64c16-219">CISP ermöglicht die folgenden Dienst Katalog-Verwaltungs Tasks von einem-Client:</span><span class="sxs-lookup"><span data-stu-id="64c16-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="64c16-220">Fragen Sie den aktuellen Status eines Index Dienst Katalogs auf dem Server ab.</span><span class="sxs-lookup"><span data-stu-id="64c16-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="64c16-221">Aktualisieren Sie den Status eines Index Dienst Katalogs.</span><span class="sxs-lookup"><span data-stu-id="64c16-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="64c16-222">Starten Sie den Indizierungsprozess für eine bestimmte Gruppe von Dateien.</span><span class="sxs-lookup"><span data-stu-id="64c16-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="64c16-223">Initialisieren Sie die Optimierung eines Indexes, um die Abfrageleistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="64c16-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="64c16-224">Bei allen Remote Verwaltungsaufgaben wird ein einfaches Anforderungs-/Antwort-Modell befolgt.</span><span class="sxs-lookup"><span data-stu-id="64c16-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="64c16-225">Auf dem Client wird kein Status für einen Verwaltungs Aufruf und administrative Anrufe in beliebiger Reihenfolge beibehalten.</span><span class="sxs-lookup"><span data-stu-id="64c16-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="64c16-226">1.3.2 Remote Abfragen</span><span class="sxs-lookup"><span data-stu-id="64c16-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="64c16-227">Mit CISP können Clients Such Abfragen für einen Remote Server ausführen, der einen Indizierungs Dienst gehostet.</span><span class="sxs-lookup"><span data-stu-id="64c16-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="64c16-228">Das Senden einer Suchabfrage ist ein mehrstufiger Prozess, der vom Client initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="64c16-229">Die Schritte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="64c16-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="64c16-230">Der Client fordert eine Verbindung zu einem Server an, der einen Indizierungs Dienst gehostet.</span><span class="sxs-lookup"><span data-stu-id="64c16-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="64c16-231">Der Client sendet die Parameter für die Suchabfrage, die Folgendes umfassen:</span><span class="sxs-lookup"><span data-stu-id="64c16-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="64c16-232">Die **Einschränkungen** , die angeben, welche Dokumente in die Suchergebnisse eingeschlossen und/oder aus diesen ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="64c16-233">Die Reihenfolge, in der die Suchergebnisse zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="64c16-234">Die Spalten, die im Resultset zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="64c16-235">Die maximale Anzahl von **Zeilen** , die für die Abfrage zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="64c16-236">Die maximale Zeit für die Abfrage Ausführung.</span><span class="sxs-lookup"><span data-stu-id="64c16-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="64c16-237">Nachdem der Server die Anforderung des Clients zum Initiieren der Abfrage bestätigt hat, kann der Client Statusinformationen zur Abfrage anfordern, dies ist jedoch kein erforderlicher Schritt.</span><span class="sxs-lookup"><span data-stu-id="64c16-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="64c16-238">Der Client gibt dann an, welche Eigenschaften der Server in die Suchergebnisse einschließen soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="64c16-239">Der Client fordert ein Resultset vom Server an, und der Server antwortet, indem er die Eigenschaftswerte für Dateien, die in den Ergebnissen für die Suchabfrage des Clients enthalten waren, an den Client sendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="64c16-240">Wenn der Wert einer Eigenschaft zu groß für einen einzelnen Antwort Puffer ist, sendet der Server die Eigenschaft nicht, sondern legt den Eigenschafts Status auf "verzögert" fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="64c16-241">Der Client fordert dann den Eigenschafts Wert separat an, indem er eine Reihe von Anforderungen für nachfolgende Blöcke des Werts verwendet und dann die Anforderung anderer Werte fortsetzt.</span><span class="sxs-lookup"><span data-stu-id="64c16-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="64c16-242">Sobald der Client mit der Suchabfrage fertig ist und keine zusätzlichen Ergebnisse mehr erfordert, kontaktiert der Client den Server, um die Abfrage freizugeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="64c16-243">Nachdem der Server die Abfrage freigegeben hat, sendet der Client möglicherweise eine Anforderung zum Trennen der Verbindung mit dem Server.</span><span class="sxs-lookup"><span data-stu-id="64c16-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="64c16-244">Die Verbindung wird dann geschlossen.</span><span class="sxs-lookup"><span data-stu-id="64c16-244">The connection is then closed.</span></span> <span data-ttu-id="64c16-245">Alternativ kann der Client eine andere Abfrage ausgeben und die Sequenz aus Schritt 2 wiederholen.</span><span class="sxs-lookup"><span data-stu-id="64c16-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="64c16-246">Windows-Verhalten: Dieses Protokoll wird unter Windows 2000, Windows XP, Windows Server 2003 und Windows Vista implementiert.</span><span class="sxs-lookup"><span data-stu-id="64c16-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="64c16-247">1.4 Beziehung zu anderen Protokollen</span><span class="sxs-lookup"><span data-stu-id="64c16-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="64c16-248">Der CISP basiert auf dem SMB \[ MS-SMB- \] Protokoll für den Nachrichten Transport.</span><span class="sxs-lookup"><span data-stu-id="64c16-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="64c16-249">Kein anderes Protokoll hängt direkt vom Content Index Service-Protokoll ab.</span><span class="sxs-lookup"><span data-stu-id="64c16-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="64c16-250">*Windows-Verhalten: Anwendungen interagieren in der Regel mit einem OLE DB Schnittstellen Wrapper \[ MSDN-OLEDB \] (z. b. einem Protokoll Client) und nicht direkt mit dem Protokoll.*</span><span class="sxs-lookup"><span data-stu-id="64c16-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="64c16-251">1,5 Voraussetzungen und Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="64c16-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="64c16-252">Es wird davon ausgegangen, dass der Client den Namen des Servers und einen Katalognamen abgerufen hat, bevor dieses Protokoll aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="64c16-253">Wie ein Client dies tut, liegt außerhalb des Gültigkeits Bereichs dieser Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="64c16-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="64c16-254">Außerdem wird davon ausgegangen, dass der Client und der Server über eine Sicherheits Zuordnung verfügen, die mit Named Pipes \[ MS-SMB verwendbar ist \] .</span><span class="sxs-lookup"><span data-stu-id="64c16-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="64c16-255">1.6 Anwendbarkeitsanweisung</span><span class="sxs-lookup"><span data-stu-id="64c16-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="64c16-256">CISP dient zum Abfragen und Verwalten von Katalogen auf einem Remote Server von einem Client.</span><span class="sxs-lookup"><span data-stu-id="64c16-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="64c16-257">CISP ist in Windows Vista veraltet.</span><span class="sxs-lookup"><span data-stu-id="64c16-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="64c16-258">1.7 Versionsverwaltung und Funktionsübertragung</span><span class="sxs-lookup"><span data-stu-id="64c16-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="64c16-259">Dieses Protokoll verfügt über keine Mechanismen zur Versionierung oder Funktions Aushandlung.</span><span class="sxs-lookup"><span data-stu-id="64c16-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="64c16-260">1.8 Durch Hersteller erweiterbare Felder</span><span class="sxs-lookup"><span data-stu-id="64c16-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="64c16-261">Dieses Protokoll verwendet HRESULTs, die Anbieter erweiterbar sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="64c16-262">Anbieter können Ihre eigenen Werte für dieses Feld auswählen, solange das C-Bit (0x20000000) gemäß den Angaben im Abschnitt 4.1.1 von \[ ms-sys festgelegt ist \] . Dies deutet darauf hin, dass es sich um einen Kundencode handelt.</span><span class="sxs-lookup"><span data-stu-id="64c16-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="64c16-263">Dieses Protokoll verwendet auch NTSTATUS-Werte, die aus dem in ms-sys definierten NTSTATUS-Nummernbereich entnommen werden \[ \] .</span><span class="sxs-lookup"><span data-stu-id="64c16-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="64c16-264">Die Anbieter sollten diese Werte mit der jeweiligen Bedeutung wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="64c16-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="64c16-265">Wenn Sie einen anderen Wert auswählen, wird das Risiko eines Konflikts in der Zukunft.</span><span class="sxs-lookup"><span data-stu-id="64c16-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="64c16-266">*Windows-Verhalten: Windows verwendet nur die Werte, die im Abschnitt 4.1.3 von \[ ms-sys angegeben sind \] .*</span><span class="sxs-lookup"><span data-stu-id="64c16-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="64c16-267">1.8.1-Eigenschaften-IDs</span><span class="sxs-lookup"><span data-stu-id="64c16-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="64c16-268">Eigenschaften werden durch IDs dargestellt, die als eigen schafts-IDs bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="64c16-269">Jede Eigenschaft muss über eine Globally Unique Identifier verfügen.</span><span class="sxs-lookup"><span data-stu-id="64c16-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="64c16-270">Dieser Bezeichner besteht aus einer **GUID** , die eine Auflistung von Eigenschaften darstellt, die als Eigenschaften Satz bezeichnet werden, sowie eine Zeichenfolge oder eine ganze Zahl mit 32 Bit, um die Eigenschaft innerhalb des Satzes zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="64c16-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="64c16-271">Wenn die ganzzahlige Form von ID verwendet wird, werden die Werte 0x00000000, 0xFFFFFFFF und 0xFFFFFFFE als ungültig eingestuft.</span><span class="sxs-lookup"><span data-stu-id="64c16-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="64c16-272">Anbieter können garantieren, dass ihre Eigenschaften eindeutig definiert werden, indem Sie in einem Eigenschaften Satz platziert werden, der durch ihre eigene GUID definiert ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="64c16-273">1.9 Zuweisungen von Standards</span><span class="sxs-lookup"><span data-stu-id="64c16-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="64c16-274">Dieses Protokoll hat keine Standard Zuweisungen, sondern nur private Zuweisungen, die von Microsoft mithilfe von in anderen Protokollen angegebenen Zuordnungs Prozeduren hergestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="64c16-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="64c16-275">Microsoft hat diesem Protokoll eine Named Pipe zugewiesen, wie in \[ MS-SMB angegeben \] .</span><span class="sxs-lookup"><span data-stu-id="64c16-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="64c16-276">Die Zuweisung lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-276">The assignment is:</span></span>



| <span data-ttu-id="64c16-277">Parameter</span><span class="sxs-lookup"><span data-stu-id="64c16-277">Parameter</span></span> | <span data-ttu-id="64c16-278">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-278">Value</span></span>             | <span data-ttu-id="64c16-279">Referenz</span><span class="sxs-lookup"><span data-stu-id="64c16-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="64c16-280">Pipename</span><span class="sxs-lookup"><span data-stu-id="64c16-280">Pipe name</span></span> | <span data-ttu-id="64c16-281">\\Pipe- \\ ci- \_ Skaden</span><span class="sxs-lookup"><span data-stu-id="64c16-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="64c16-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="64c16-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="64c16-283">2\. Nachrichten</span><span class="sxs-lookup"><span data-stu-id="64c16-283">2 Messages</span></span>

-   [<span data-ttu-id="64c16-284">2.1 Transport</span><span class="sxs-lookup"><span data-stu-id="64c16-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="64c16-285">2.2 Nachrichtensyntax</span><span class="sxs-lookup"><span data-stu-id="64c16-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="64c16-286">2.1 Transport</span><span class="sxs-lookup"><span data-stu-id="64c16-286">2.1 Transport</span></span>

<span data-ttu-id="64c16-287">Alle Nachrichten müssen mithilfe einer Named Pipe transportiert werden, wie in \[ MS-SMB angegeben \] .</span><span class="sxs-lookup"><span data-stu-id="64c16-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="64c16-288">Der folgende Pipename wird verwendet:</span><span class="sxs-lookup"><span data-stu-id="64c16-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="64c16-289">\\Pipe- \\ ci- \_ Skaden</span><span class="sxs-lookup"><span data-stu-id="64c16-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="64c16-290">Dieses Protokoll verwendet das zugrunde liegende SMB-Named Pipe-Protokoll, um die Identität des Aufrufers abzurufen, der die Verbindung hergestellt hat, wie im Abschnitt 2.2.8 of \[ MS-SMB angegeben \] . der Client muss die Sicherheits \_ Identifizierung als Identitätswechsel Ebene in der Anforderung festlegen, um die Named Pipe zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="64c16-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="64c16-291">2.2 Nachrichtensyntax</span><span class="sxs-lookup"><span data-stu-id="64c16-291">2.2 Message Syntax</span></span>

<span data-ttu-id="64c16-292">Mehrere Strukturen und Nachrichten in den folgenden Abschnitten beziehen sich auf Kapitel-oder Lesezeichen Handles.</span><span class="sxs-lookup"><span data-stu-id="64c16-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="64c16-293">Ein Handle ist eine lange 32-Bit-Struktur, die ein Kapitel oder Lesezeichen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="64c16-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="64c16-294">Normalerweise empfangen Client Anwendungen handle-Werte über Methodenaufrufe. Es gibt jedoch einige bekannte Werte, die nicht von einem Server abgerufen werden müssen, was in der folgenden Tabelle angegeben ist:</span><span class="sxs-lookup"><span data-stu-id="64c16-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="64c16-295">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-295">Value</span></span>                         | <span data-ttu-id="64c16-296">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-297">DB \_ NULL \_ hChapter 0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="64c16-298">Ein Kapitel Handle für das ungeteilte Rowset, das alle Abfrageergebnisse enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="64c16-299">Dbbmk \_ erste 0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="64c16-300">Ein Lesezeichen Handle für ein Lesezeichen, das die erste Zeile im Rowset identifiziert.</span><span class="sxs-lookup"><span data-stu-id="64c16-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="64c16-301">Dbbmk \_ Letzte 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="64c16-302">Ein Lesezeichen Handle für ein Lesezeichen, das die letzte Zeile im Rowset identifiziert.</span><span class="sxs-lookup"><span data-stu-id="64c16-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="64c16-303">2.2.1-Strukturen</span><span class="sxs-lookup"><span data-stu-id="64c16-303">2.2.1 Structures</span></span>

<span data-ttu-id="64c16-304">In diesem Abschnitt werden Datenstrukturen ausführlich erläutert, die von CISP definiert und verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="64c16-305">Alle 2-, 4-und 8-Byte-Ganzzahlen mit und ohne Vorzeichen in den folgenden Strukturen müssen in der Little-Endian-Byte Reihenfolge übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="64c16-306">In der folgenden Tabelle werden die Datenstrukturen zusammengefasst, die in diesem Abschnitt definiert sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="64c16-307">Struktur</span><span class="sxs-lookup"><span data-stu-id="64c16-307">Structure</span></span>                    | <span data-ttu-id="64c16-308">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64c16-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-309">Cbasestoragevariant</span><span class="sxs-lookup"><span data-stu-id="64c16-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="64c16-310">Enthält den Wert, für den eine Übereinstimmungs Operation für eine Eigenschaft durchgeführt werden soll, die in einer cpropertyeinschränkung-Struktur angegeben ist</span><span class="sxs-lookup"><span data-stu-id="64c16-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="64c16-311">SafeArray, SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="64c16-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="64c16-312">Enthält ein mehrdimensionales Array.</span><span class="sxs-lookup"><span data-stu-id="64c16-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="64c16-313">SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="64c16-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="64c16-314">Stellt die Begrenzungen für eine Dimension eines Arrays dar, das in einer SAFEARRAY-Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="64c16-315">Cfullpropspec</span><span class="sxs-lookup"><span data-stu-id="64c16-315">CFullPropSpec</span></span>                | <span data-ttu-id="64c16-316">Enthält eine Eigenschafts Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="64c16-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="64c16-317">Ccontent-Einschränkung</span><span class="sxs-lookup"><span data-stu-id="64c16-317">CContentRestriction</span></span>          | <span data-ttu-id="64c16-318">Enthält eine Zeichenfolge, die mit einem Eigenschafts Wert im Eigenschaften Cache abgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="64c16-319">Ck</span><span class="sxs-lookup"><span data-stu-id="64c16-319">CKey</span></span>                         | <span data-ttu-id="64c16-320">Enthält einen Eigenschafts Wert.</span><span class="sxs-lookup"><span data-stu-id="64c16-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="64c16-321">Cinternalpropertyeinschränkung</span><span class="sxs-lookup"><span data-stu-id="64c16-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="64c16-322">Enthält einen Eigenschafts Wert, der mit einem Vorgang verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="64c16-323">Cnatlanguagerestriction</span><span class="sxs-lookup"><span data-stu-id="64c16-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="64c16-324">Enthält eine Abfrage in natürlicher Sprache für eine Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="64c16-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="64c16-325">Cnoderestriction</span><span class="sxs-lookup"><span data-stu-id="64c16-325">CNodeRestriction</span></span>             | <span data-ttu-id="64c16-326">Enthält ein Array von Befehlsstruktur Knoten, die die Einschränkungen für eine Abfrage angeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="64c16-327">"Cockrestriction"</span><span class="sxs-lookup"><span data-stu-id="64c16-327">COccRestriction</span></span>              | <span data-ttu-id="64c16-328">Enthält den Speicherort eines Worts in einem Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="64c16-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="64c16-329">Cpropertyeinschränkung</span><span class="sxs-lookup"><span data-stu-id="64c16-329">CPropertyRestriction</span></span>         | <span data-ttu-id="64c16-330">Enthält einen Eigenschafts Wert, der mit einem Vorgang verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="64c16-331">Crangerestriction</span><span class="sxs-lookup"><span data-stu-id="64c16-331">CRangeRestriction</span></span>            | <span data-ttu-id="64c16-332">Enthält eine Einschränkung für einen Wertebereich.</span><span class="sxs-lookup"><span data-stu-id="64c16-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="64c16-333">Cscoperestriction</span><span class="sxs-lookup"><span data-stu-id="64c16-333">CScopeRestriction</span></span>            | <span data-ttu-id="64c16-334">Enthält eine Einschränkung der Dateien, die durchsucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="64c16-335">Csort</span><span class="sxs-lookup"><span data-stu-id="64c16-335">CSort</span></span>                        | <span data-ttu-id="64c16-336">Identifiziert eine zu sortierende Spalte.</span><span class="sxs-lookup"><span data-stu-id="64c16-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="64c16-337">Csyneinschränkung</span><span class="sxs-lookup"><span data-stu-id="64c16-337">CSynRestriction</span></span>              | <span data-ttu-id="64c16-338">Enthält ein Wort oder seine Synonyme für einen Abfrage Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="64c16-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="64c16-339">Cvectoreinschränkung</span><span class="sxs-lookup"><span data-stu-id="64c16-339">CVectorRestriction</span></span>           | <span data-ttu-id="64c16-340">Enthält eine gewichtete OR-Operation für einen Befehlsstruktur Knoten.</span><span class="sxs-lookup"><span data-stu-id="64c16-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="64c16-341">Cwordrestriction</span><span class="sxs-lookup"><span data-stu-id="64c16-341">CWordRestriction</span></span>             | <span data-ttu-id="64c16-342">Enthält ein Wort für einen Abfrage Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="64c16-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="64c16-343">Mit der Einschränkung</span><span class="sxs-lookup"><span data-stu-id="64c16-343">CRestriction</span></span>                 | <span data-ttu-id="64c16-344">Enthält einen Knoten einer Abfrage Befehlsstruktur.</span><span class="sxs-lookup"><span data-stu-id="64c16-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="64c16-345">Ccolumnset</span><span class="sxs-lookup"><span data-stu-id="64c16-345">CColumnSet</span></span>                   | <span data-ttu-id="64c16-346">Gibt die Anzahl der zurück zugebende Spalten an.</span><span class="sxs-lookup"><span data-stu-id="64c16-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="64c16-347">Ccategorizationset</span><span class="sxs-lookup"><span data-stu-id="64c16-347">CCategorizationSet</span></span>           | <span data-ttu-id="64c16-348">Enthält Informationen zur Gruppierung eines Satzes von Abfrage Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="64c16-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="64c16-349">Ccategorizationspec</span><span class="sxs-lookup"><span data-stu-id="64c16-349">CCategorizationSpec</span></span>          | <span data-ttu-id="64c16-350">Enthält eine Definition von Kategorien, in die Abfrageergebnisse kategorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="64c16-351">Cdbkolid</span><span class="sxs-lookup"><span data-stu-id="64c16-351">CDbColId</span></span>                     | <span data-ttu-id="64c16-352">Enthält eine Spalte.</span><span class="sxs-lookup"><span data-stu-id="64c16-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="64c16-353">Cdbprop</span><span class="sxs-lookup"><span data-stu-id="64c16-353">CDbProp</span></span>                      | <span data-ttu-id="64c16-354">Enthält eine-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="64c16-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="64c16-355">CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="64c16-355">CDbPropSet</span></span>                   | <span data-ttu-id="64c16-356">Enthält einen Satz von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="64c16-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="64c16-357">Cpidmapper</span><span class="sxs-lookup"><span data-stu-id="64c16-357">CPidMapper</span></span>                   | <span data-ttu-id="64c16-358">Enthält ein Array von Eigenschaften-IDs, die die Eigenschaften angeben, die in einem Rowset zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="64c16-359">Crowseekat</span><span class="sxs-lookup"><span data-stu-id="64c16-359">CRowSeekAt</span></span>                   | <span data-ttu-id="64c16-360">Enthält den Offset, bei dem Zeilen in einer cpmgetrowsin-Nachricht abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="64c16-361">Crowseekatratio</span><span class="sxs-lookup"><span data-stu-id="64c16-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="64c16-362">Gibt den Punkt an, an dem mit dem Abrufen einer cpmgetrowsin-Nachricht begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="64c16-363">Crowseekbybookmark</span><span class="sxs-lookup"><span data-stu-id="64c16-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="64c16-364">Gibt die Lesezeichen an, aus denen Zeilen für eine cpmgetrowsin-Nachricht abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="64c16-365">Crowseeknext</span><span class="sxs-lookup"><span data-stu-id="64c16-365">CRowSeekNext</span></span>                 | <span data-ttu-id="64c16-366">Enthält die Anzahl der Zeilen, die in einer cpmgetrowsin-Nachricht übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="64c16-367">Crowsetproperties</span><span class="sxs-lookup"><span data-stu-id="64c16-367">CRowsetProperties</span></span>            | <span data-ttu-id="64c16-368">Enthält die Konfigurationsinformationen für eine Abfrage.</span><span class="sxs-lookup"><span data-stu-id="64c16-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="64c16-369">Csortset</span><span class="sxs-lookup"><span data-stu-id="64c16-369">CSortSet</span></span>                     | <span data-ttu-id="64c16-370">Enthält die Sortierreihenfolge für eine Abfrage.</span><span class="sxs-lookup"><span data-stu-id="64c16-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="64c16-371">Ctablecolumn</span><span class="sxs-lookup"><span data-stu-id="64c16-371">CTableColumn</span></span>                 | <span data-ttu-id="64c16-372">Enthält eine Spalte für die cpmsetbindungen-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="64c16-373">Serializedpropertyvalue</span><span class="sxs-lookup"><span data-stu-id="64c16-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="64c16-374">Enthält einen serialisierten Wert.</span><span class="sxs-lookup"><span data-stu-id="64c16-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="64c16-375">2.2.1.1 cbasestoragevariant</span><span class="sxs-lookup"><span data-stu-id="64c16-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="64c16-376">Die cbasestoragevariant-Struktur enthält den Wert, für den eine Übereinstimmungs Operation für eine Eigenschaft durchgeführt werden soll, die in der cpropertyeinschränkung-Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="64c16-377">0</span><span class="sxs-lookup"><span data-stu-id="64c16-377">0</span></span>

<span data-ttu-id="64c16-378">1</span><span class="sxs-lookup"><span data-stu-id="64c16-378">1</span></span>

<span data-ttu-id="64c16-379">2</span><span class="sxs-lookup"><span data-stu-id="64c16-379">2</span></span>

<span data-ttu-id="64c16-380">3</span><span class="sxs-lookup"><span data-stu-id="64c16-380">3</span></span>

<span data-ttu-id="64c16-381">4</span><span class="sxs-lookup"><span data-stu-id="64c16-381">4</span></span>

<span data-ttu-id="64c16-382">5</span><span class="sxs-lookup"><span data-stu-id="64c16-382">5</span></span>

<span data-ttu-id="64c16-383">6</span><span class="sxs-lookup"><span data-stu-id="64c16-383">6</span></span>

<span data-ttu-id="64c16-384">7</span><span class="sxs-lookup"><span data-stu-id="64c16-384">7</span></span>

<span data-ttu-id="64c16-385">8</span><span class="sxs-lookup"><span data-stu-id="64c16-385">8</span></span>

<span data-ttu-id="64c16-386">9</span><span class="sxs-lookup"><span data-stu-id="64c16-386">9</span></span>

<span data-ttu-id="64c16-387">1</span><span class="sxs-lookup"><span data-stu-id="64c16-387">1</span></span><br/> <span data-ttu-id="64c16-388">0</span><span class="sxs-lookup"><span data-stu-id="64c16-388">0</span></span><br/>

<span data-ttu-id="64c16-389">1</span><span class="sxs-lookup"><span data-stu-id="64c16-389">1</span></span>

<span data-ttu-id="64c16-390">2</span><span class="sxs-lookup"><span data-stu-id="64c16-390">2</span></span>

<span data-ttu-id="64c16-391">3</span><span class="sxs-lookup"><span data-stu-id="64c16-391">3</span></span>

<span data-ttu-id="64c16-392">4</span><span class="sxs-lookup"><span data-stu-id="64c16-392">4</span></span>

<span data-ttu-id="64c16-393">5</span><span class="sxs-lookup"><span data-stu-id="64c16-393">5</span></span>

<span data-ttu-id="64c16-394">6</span><span class="sxs-lookup"><span data-stu-id="64c16-394">6</span></span>

<span data-ttu-id="64c16-395">7</span><span class="sxs-lookup"><span data-stu-id="64c16-395">7</span></span>

<span data-ttu-id="64c16-396">8</span><span class="sxs-lookup"><span data-stu-id="64c16-396">8</span></span>

<span data-ttu-id="64c16-397">9</span><span class="sxs-lookup"><span data-stu-id="64c16-397">9</span></span>

<span data-ttu-id="64c16-398">2</span><span class="sxs-lookup"><span data-stu-id="64c16-398">2</span></span><br/> <span data-ttu-id="64c16-399">0</span><span class="sxs-lookup"><span data-stu-id="64c16-399">0</span></span><br/>

<span data-ttu-id="64c16-400">1</span><span class="sxs-lookup"><span data-stu-id="64c16-400">1</span></span>

<span data-ttu-id="64c16-401">2</span><span class="sxs-lookup"><span data-stu-id="64c16-401">2</span></span>

<span data-ttu-id="64c16-402">3</span><span class="sxs-lookup"><span data-stu-id="64c16-402">3</span></span>

<span data-ttu-id="64c16-403">4</span><span class="sxs-lookup"><span data-stu-id="64c16-403">4</span></span>

<span data-ttu-id="64c16-404">5</span><span class="sxs-lookup"><span data-stu-id="64c16-404">5</span></span>

<span data-ttu-id="64c16-405">6</span><span class="sxs-lookup"><span data-stu-id="64c16-405">6</span></span>

<span data-ttu-id="64c16-406">7</span><span class="sxs-lookup"><span data-stu-id="64c16-406">7</span></span>

<span data-ttu-id="64c16-407">8</span><span class="sxs-lookup"><span data-stu-id="64c16-407">8</span></span>

<span data-ttu-id="64c16-408">9</span><span class="sxs-lookup"><span data-stu-id="64c16-408">9</span></span>

<span data-ttu-id="64c16-409">3</span><span class="sxs-lookup"><span data-stu-id="64c16-409">3</span></span><br/> <span data-ttu-id="64c16-410">0</span><span class="sxs-lookup"><span data-stu-id="64c16-410">0</span></span><br/>

<span data-ttu-id="64c16-411">1</span><span class="sxs-lookup"><span data-stu-id="64c16-411">1</span></span>

<span data-ttu-id="64c16-412">VType</span><span class="sxs-lookup"><span data-stu-id="64c16-412">vType</span></span>

<span data-ttu-id="64c16-413">vData1</span><span class="sxs-lookup"><span data-stu-id="64c16-413">vData1</span></span>

<span data-ttu-id="64c16-414">vData2</span><span class="sxs-lookup"><span data-stu-id="64c16-414">vData2</span></span>

<span data-ttu-id="64c16-415">vValue (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-415">vValue (variable)</span></span>



 

<span data-ttu-id="64c16-416">**VType**: ein Typindikator, der den Typ von vValue angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="64c16-417">Es muss sich um einen der varenumum-Werte handeln, die in der folgenden Tabelle angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="64c16-418">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-418">Value</span></span>                 | <span data-ttu-id="64c16-419">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-420">VT \_ leer (0x0000)</span><span class="sxs-lookup"><span data-stu-id="64c16-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="64c16-421">vValue ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="64c16-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="64c16-422">VT \_ NULL (0x0001)</span><span class="sxs-lookup"><span data-stu-id="64c16-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="64c16-423">vValue ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="64c16-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="64c16-424">VT \_ I1 (0x0010)</span><span class="sxs-lookup"><span data-stu-id="64c16-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="64c16-425">Eine 1-Byte-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="64c16-426">VT \_ UI1 (0x0011)</span><span class="sxs-lookup"><span data-stu-id="64c16-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="64c16-427">Eine 1-Byte-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="64c16-428">VT \_ I2 (0x0002)</span><span class="sxs-lookup"><span data-stu-id="64c16-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="64c16-429">Eine 2-Byte-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="64c16-430">VT \_ UI2 (0x0012)</span><span class="sxs-lookup"><span data-stu-id="64c16-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="64c16-431">Eine 2-Byte-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="64c16-432">VT \_ bool (0x000b)</span><span class="sxs-lookup"><span data-stu-id="64c16-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="64c16-433">Ein boolescher Wert. eine 2-Byte-Ganzzahl, die 0x0000 (false) oder 0xFFFF (true) enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="64c16-434">VT \_ I4 (0x0003)</span><span class="sxs-lookup"><span data-stu-id="64c16-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="64c16-435">Eine 4-Byte-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="64c16-436">VT \_ UI4 (0x0013)</span><span class="sxs-lookup"><span data-stu-id="64c16-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="64c16-437">Eine 4-Byte-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="64c16-438">VT \_ R4 (0x0004)</span><span class="sxs-lookup"><span data-stu-id="64c16-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="64c16-439">Eine IEEE 32-Bit-Gleit Komma Zahl, wie in \[ IEEE754 definiert \] .</span><span class="sxs-lookup"><span data-stu-id="64c16-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="64c16-440">VT \_ int (0x0016)</span><span class="sxs-lookup"><span data-stu-id="64c16-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="64c16-441">Eine 4-Byte-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="64c16-442">VT \_ uint (0x0017)</span><span class="sxs-lookup"><span data-stu-id="64c16-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="64c16-443">Eine 4-Byte-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="64c16-444">VT- \_ Fehler (0x000a)</span><span class="sxs-lookup"><span data-stu-id="64c16-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="64c16-445">Eine 4-Byte-Ganzzahl ohne Vorzeichen, die ein HRESULT enthält, wie in \[ ms-sys angegeben \] .</span><span class="sxs-lookup"><span data-stu-id="64c16-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="64c16-446">VT \_ I8 (0x0014)</span><span class="sxs-lookup"><span data-stu-id="64c16-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="64c16-447">Eine 8-Byte-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="64c16-448">VT \_ UI8 (0x0015)</span><span class="sxs-lookup"><span data-stu-id="64c16-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="64c16-449">Eine 8-Byte-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="64c16-450">VT \_ R8 (0x0005)</span><span class="sxs-lookup"><span data-stu-id="64c16-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="64c16-451">Eine IEEE 64-Bit-Gleit Komma Zahl gemäß Definition in \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="64c16-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="64c16-452">VT \_ CY (0x0006)</span><span class="sxs-lookup"><span data-stu-id="64c16-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="64c16-453">Eine ganzzahlige Ganzzahl mit 8 Bytes (skaliert durch 10.000).</span><span class="sxs-lookup"><span data-stu-id="64c16-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="64c16-454">VT- \_ Datum (0x0007)</span><span class="sxs-lookup"><span data-stu-id="64c16-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="64c16-455">Eine 64-Bit-Gleit Komma Zahl, die die Anzahl von Tagen seit 00:00:00 am 31. Dezember 1899 darstellt (koordinierte Weltzeit).</span><span class="sxs-lookup"><span data-stu-id="64c16-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="64c16-456">VT \_ FILETIME (0x0040)</span><span class="sxs-lookup"><span data-stu-id="64c16-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="64c16-457">Eine 64-Bit-Ganzzahl, die die Anzahl der 100-Nanosekunden-Intervalle seit 00:00:00 am 1. Januar 1601 (koordinierte Weltzeit) darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="64c16-458">VT \_ Decimal (0x000e)</span><span class="sxs-lookup"><span data-stu-id="64c16-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="64c16-459">Eine dezimale Struktur, wie im Abschnitt 2.2.1.1.1.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="64c16-460">VT \_ CLSID (0x0048)</span><span class="sxs-lookup"><span data-stu-id="64c16-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="64c16-461">Ein 16-Byte-Binärwert, der eine GUID enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="64c16-462">VT- \_ BLOB (0x0041)</span><span class="sxs-lookup"><span data-stu-id="64c16-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="64c16-463">Eine 4-Byte-Ganzzahl ohne Vorzeichen von Bytes im BLOB, gefolgt von der Anzahl der Daten bytes.</span><span class="sxs-lookup"><span data-stu-id="64c16-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="64c16-464">VT \_ BSTR (0x0008)</span><span class="sxs-lookup"><span data-stu-id="64c16-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="64c16-465">Eine 4-Byte-Ganzzahl ohne Vorzeichen von Bytes in der Zeichenfolge, gefolgt von einer Zeichenfolge, wie unten unter vValue angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="64c16-466">VT \_ LPSTR (0x001e)</span><span class="sxs-lookup"><span data-stu-id="64c16-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="64c16-467">Eine mit NULL endende ANSI-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="64c16-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="64c16-468">VT \_ LPWSTR (0x001F)</span><span class="sxs-lookup"><span data-stu-id="64c16-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="64c16-469">Eine NULL terminierte Unicode- \[ Unicode- \] Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="64c16-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="64c16-470">VT- \_ Variante (0x000c)</span><span class="sxs-lookup"><span data-stu-id="64c16-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="64c16-471">Cbasestoragevariant.</span><span class="sxs-lookup"><span data-stu-id="64c16-471">CBaseStorageVariant.</span></span> <span data-ttu-id="64c16-472">Muss mit einem Typmodifizierer des VT- \_ Arrays oder des VT- \_ Vektors kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="64c16-473">In der folgenden Tabelle werden die Typmodifizierer für VType angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="64c16-474">Typmodifizierer können mit VType Binary ORed sein, um die Bedeutung von vValue zu ändern, um anzugeben, dass es sich um einen von zwei möglichen Array Typen handelt.</span><span class="sxs-lookup"><span data-stu-id="64c16-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="64c16-475">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-475">Value</span></span>               | <span data-ttu-id="64c16-476">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-477">VT- \_ Vektor (0x1000)</span><span class="sxs-lookup"><span data-stu-id="64c16-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="64c16-478">Wenn der Typindikator mithilfe eines OR-Operators mit dem VT-Vektor kombiniert wird \_ , ist vValue ein Gezähltes Array von Werten des bestimmten Typs.</span><span class="sxs-lookup"><span data-stu-id="64c16-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="64c16-479">Weitere Informationen finden Sie im Abschnitt 2.2.1.1.1.2.</span><span class="sxs-lookup"><span data-stu-id="64c16-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="64c16-480">Dieser Typmodifizierer darf nicht mit den folgenden Typen kombiniert werden: VT \_ int, VT \_ uint, VT \_ Decimal, VT \_ BLOB, VT \_ BLOB \_ Object.</span><span class="sxs-lookup"><span data-stu-id="64c16-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="64c16-481">VT- \_ Array (0x2000)</span><span class="sxs-lookup"><span data-stu-id="64c16-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="64c16-482">Wenn der Typindikator von einem or-Operator mit dem VT-Array kombiniert wird \_ , ist der Wert ein SafeArray (wie im Abschnitt 2.2.1.1.1.3 angegeben), der Werte des angegebenen Typs enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="64c16-483">Dieser Typmodifizierer darf nicht mit den folgenden Typen kombiniert werden: VT \_ I8, VT \_ UI8, VT \_ FILETIME, VT \_ CLSID, VT \_ BLOB, VT \_ BLOB \_ Object, VT \_ LPStr, VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="64c16-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="64c16-484">**vData1**: Wenn VType \_ den Wert VT Decimal hat, wird der Wert dieses Felds als Skalierungs Feld im Abschnitt 2.2.1.1.1.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="64c16-485">Für alle anderen vtypes muss der Wert auf 0x00 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="64c16-486">**vData2**: Wenn VType \_ den Wert VT Decimal hat, wird der Wert dieses Felds im Abschnitt 2.2.1.1.1.1 als Sign-Feld angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="64c16-487">Für alle anderen vtypes muss der Wert auf 0x00 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="64c16-488">**vValue**: der Wert für den Übereinstimmungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="64c16-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="64c16-489">Die Syntax muss wie im Feld "VType" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="64c16-490">In der folgenden Tabelle werden die Größen für das vValue-Feld zusammengefasst, abhängig vom Feld "VType" für Datentypen mit fester Länge.</span><span class="sxs-lookup"><span data-stu-id="64c16-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="64c16-491">Die Größe wird in Bytes angezeigt.</span><span class="sxs-lookup"><span data-stu-id="64c16-491">The size is in bytes.</span></span>



| <span data-ttu-id="64c16-492">VType</span><span class="sxs-lookup"><span data-stu-id="64c16-492">vType</span></span>                                                   | <span data-ttu-id="64c16-493">Size</span><span class="sxs-lookup"><span data-stu-id="64c16-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="64c16-494">VT \_ I1, VT, \_ UI1</span><span class="sxs-lookup"><span data-stu-id="64c16-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="64c16-495">1</span><span class="sxs-lookup"><span data-stu-id="64c16-495">1</span></span>    |
| <span data-ttu-id="64c16-496">VT \_ I2, VT \_ UI2, VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="64c16-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="64c16-497">2</span><span class="sxs-lookup"><span data-stu-id="64c16-497">2</span></span>    |
| <span data-ttu-id="64c16-498">VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ int, VT \_ uint, VT \_ Error</span><span class="sxs-lookup"><span data-stu-id="64c16-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="64c16-499">4</span><span class="sxs-lookup"><span data-stu-id="64c16-499">4</span></span>    |
| <span data-ttu-id="64c16-500">VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ Date, VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="64c16-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="64c16-501">8</span><span class="sxs-lookup"><span data-stu-id="64c16-501">8</span></span>    |
| <span data-ttu-id="64c16-502">VT \_ Decimal, VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="64c16-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="64c16-503">16</span><span class="sxs-lookup"><span data-stu-id="64c16-503">16</span></span>   |



 

<span data-ttu-id="64c16-504">Wenn VType auf VT \_ BLOB, VT \_ BSTR oder VT LPSTR festgelegt ist, \_ wird die Struktur von vValue in der folgenden Abbildung angegeben:</span><span class="sxs-lookup"><span data-stu-id="64c16-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="64c16-505">0</span><span class="sxs-lookup"><span data-stu-id="64c16-505">0</span></span>

<span data-ttu-id="64c16-506">1</span><span class="sxs-lookup"><span data-stu-id="64c16-506">1</span></span>

<span data-ttu-id="64c16-507">2</span><span class="sxs-lookup"><span data-stu-id="64c16-507">2</span></span>

<span data-ttu-id="64c16-508">3</span><span class="sxs-lookup"><span data-stu-id="64c16-508">3</span></span>

<span data-ttu-id="64c16-509">4</span><span class="sxs-lookup"><span data-stu-id="64c16-509">4</span></span>

<span data-ttu-id="64c16-510">5</span><span class="sxs-lookup"><span data-stu-id="64c16-510">5</span></span>

<span data-ttu-id="64c16-511">6</span><span class="sxs-lookup"><span data-stu-id="64c16-511">6</span></span>

<span data-ttu-id="64c16-512">7</span><span class="sxs-lookup"><span data-stu-id="64c16-512">7</span></span>

<span data-ttu-id="64c16-513">8</span><span class="sxs-lookup"><span data-stu-id="64c16-513">8</span></span>

<span data-ttu-id="64c16-514">9</span><span class="sxs-lookup"><span data-stu-id="64c16-514">9</span></span>

<span data-ttu-id="64c16-515">1</span><span class="sxs-lookup"><span data-stu-id="64c16-515">1</span></span><br/> <span data-ttu-id="64c16-516">0</span><span class="sxs-lookup"><span data-stu-id="64c16-516">0</span></span><br/>

<span data-ttu-id="64c16-517">1</span><span class="sxs-lookup"><span data-stu-id="64c16-517">1</span></span>

<span data-ttu-id="64c16-518">2</span><span class="sxs-lookup"><span data-stu-id="64c16-518">2</span></span>

<span data-ttu-id="64c16-519">3</span><span class="sxs-lookup"><span data-stu-id="64c16-519">3</span></span>

<span data-ttu-id="64c16-520">4</span><span class="sxs-lookup"><span data-stu-id="64c16-520">4</span></span>

<span data-ttu-id="64c16-521">5</span><span class="sxs-lookup"><span data-stu-id="64c16-521">5</span></span>

<span data-ttu-id="64c16-522">6</span><span class="sxs-lookup"><span data-stu-id="64c16-522">6</span></span>

<span data-ttu-id="64c16-523">7</span><span class="sxs-lookup"><span data-stu-id="64c16-523">7</span></span>

<span data-ttu-id="64c16-524">8</span><span class="sxs-lookup"><span data-stu-id="64c16-524">8</span></span>

<span data-ttu-id="64c16-525">9</span><span class="sxs-lookup"><span data-stu-id="64c16-525">9</span></span>

<span data-ttu-id="64c16-526">2</span><span class="sxs-lookup"><span data-stu-id="64c16-526">2</span></span><br/> <span data-ttu-id="64c16-527">0</span><span class="sxs-lookup"><span data-stu-id="64c16-527">0</span></span><br/>

<span data-ttu-id="64c16-528">1</span><span class="sxs-lookup"><span data-stu-id="64c16-528">1</span></span>

<span data-ttu-id="64c16-529">2</span><span class="sxs-lookup"><span data-stu-id="64c16-529">2</span></span>

<span data-ttu-id="64c16-530">3</span><span class="sxs-lookup"><span data-stu-id="64c16-530">3</span></span>

<span data-ttu-id="64c16-531">4</span><span class="sxs-lookup"><span data-stu-id="64c16-531">4</span></span>

<span data-ttu-id="64c16-532">5</span><span class="sxs-lookup"><span data-stu-id="64c16-532">5</span></span>

<span data-ttu-id="64c16-533">6</span><span class="sxs-lookup"><span data-stu-id="64c16-533">6</span></span>

<span data-ttu-id="64c16-534">7</span><span class="sxs-lookup"><span data-stu-id="64c16-534">7</span></span>

<span data-ttu-id="64c16-535">8</span><span class="sxs-lookup"><span data-stu-id="64c16-535">8</span></span>

<span data-ttu-id="64c16-536">9</span><span class="sxs-lookup"><span data-stu-id="64c16-536">9</span></span>

<span data-ttu-id="64c16-537">3</span><span class="sxs-lookup"><span data-stu-id="64c16-537">3</span></span><br/> <span data-ttu-id="64c16-538">0</span><span class="sxs-lookup"><span data-stu-id="64c16-538">0</span></span><br/>

<span data-ttu-id="64c16-539">1</span><span class="sxs-lookup"><span data-stu-id="64c16-539">1</span></span>

<span data-ttu-id="64c16-540">CBSIZE</span><span class="sxs-lookup"><span data-stu-id="64c16-540">cbSize</span></span>

<span data-ttu-id="64c16-541">blobdata (Variable, optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="64c16-542">**CBSIZE**: Vorzeichen lose 32-Bit-Ganzzahl, die die Größe des blobdata-Felds in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="64c16-543">Wenn VType auf VT \_ BSTR oder VT \_ LPSTR festgelegt ist, muss CBSIZE auf 0x00000000 festgelegt werden, wenn die dargestellte Zeichenfolge eine leere Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="64c16-544">**blobdata**: muss eine Länge von CBSIZE in Bytes aufweisen.</span><span class="sxs-lookup"><span data-stu-id="64c16-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="64c16-545">Wenn VType auf VT BLOB festgelegt ist \_ , handelt es sich bei diesem Feld um undurchsichtige binäre BLOB-Daten.</span><span class="sxs-lookup"><span data-stu-id="64c16-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="64c16-546">Wenn VType auf VT BSTR festgelegt ist \_ , handelt es sich bei diesem Feld um einen Satz von Zeichen in einem vom OEM ausgewählten Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="64c16-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="64c16-547">Client und Server müssen so konfiguriert sein, dass Sie über interoperable Zeichensätze verfügen (Out-of-Band des Protokolls).</span><span class="sxs-lookup"><span data-stu-id="64c16-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="64c16-548">Es ist nicht erforderlich, dass es auf NULL endet.</span><span class="sxs-lookup"><span data-stu-id="64c16-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="64c16-549">Für VType auf VT \_ LPSTR ist dieses Feld eine NULL-terminierte Zeichenfolge in einem vom OEM ausgewählten Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="64c16-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="64c16-550">Client und Server müssen so konfiguriert sein, dass Sie über interoperable Zeichensätze verfügen (Out-of-Band des Protokolls).</span><span class="sxs-lookup"><span data-stu-id="64c16-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="64c16-551">Wenn VType auf VT \_ LPWSTR festgelegt ist, wird die Struktur von vValue im folgenden Diagramm angegeben:</span><span class="sxs-lookup"><span data-stu-id="64c16-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="64c16-552">0</span><span class="sxs-lookup"><span data-stu-id="64c16-552">0</span></span>

<span data-ttu-id="64c16-553">1</span><span class="sxs-lookup"><span data-stu-id="64c16-553">1</span></span>

<span data-ttu-id="64c16-554">2</span><span class="sxs-lookup"><span data-stu-id="64c16-554">2</span></span>

<span data-ttu-id="64c16-555">3</span><span class="sxs-lookup"><span data-stu-id="64c16-555">3</span></span>

<span data-ttu-id="64c16-556">4</span><span class="sxs-lookup"><span data-stu-id="64c16-556">4</span></span>

<span data-ttu-id="64c16-557">5</span><span class="sxs-lookup"><span data-stu-id="64c16-557">5</span></span>

<span data-ttu-id="64c16-558">6</span><span class="sxs-lookup"><span data-stu-id="64c16-558">6</span></span>

<span data-ttu-id="64c16-559">7</span><span class="sxs-lookup"><span data-stu-id="64c16-559">7</span></span>

<span data-ttu-id="64c16-560">8</span><span class="sxs-lookup"><span data-stu-id="64c16-560">8</span></span>

<span data-ttu-id="64c16-561">9</span><span class="sxs-lookup"><span data-stu-id="64c16-561">9</span></span>

<span data-ttu-id="64c16-562">1</span><span class="sxs-lookup"><span data-stu-id="64c16-562">1</span></span><br/> <span data-ttu-id="64c16-563">0</span><span class="sxs-lookup"><span data-stu-id="64c16-563">0</span></span><br/>

<span data-ttu-id="64c16-564">1</span><span class="sxs-lookup"><span data-stu-id="64c16-564">1</span></span>

<span data-ttu-id="64c16-565">2</span><span class="sxs-lookup"><span data-stu-id="64c16-565">2</span></span>

<span data-ttu-id="64c16-566">3</span><span class="sxs-lookup"><span data-stu-id="64c16-566">3</span></span>

<span data-ttu-id="64c16-567">4</span><span class="sxs-lookup"><span data-stu-id="64c16-567">4</span></span>

<span data-ttu-id="64c16-568">5</span><span class="sxs-lookup"><span data-stu-id="64c16-568">5</span></span>

<span data-ttu-id="64c16-569">6</span><span class="sxs-lookup"><span data-stu-id="64c16-569">6</span></span>

<span data-ttu-id="64c16-570">7</span><span class="sxs-lookup"><span data-stu-id="64c16-570">7</span></span>

<span data-ttu-id="64c16-571">8</span><span class="sxs-lookup"><span data-stu-id="64c16-571">8</span></span>

<span data-ttu-id="64c16-572">9</span><span class="sxs-lookup"><span data-stu-id="64c16-572">9</span></span>

<span data-ttu-id="64c16-573">2</span><span class="sxs-lookup"><span data-stu-id="64c16-573">2</span></span><br/> <span data-ttu-id="64c16-574">0</span><span class="sxs-lookup"><span data-stu-id="64c16-574">0</span></span><br/>

<span data-ttu-id="64c16-575">1</span><span class="sxs-lookup"><span data-stu-id="64c16-575">1</span></span>

<span data-ttu-id="64c16-576">2</span><span class="sxs-lookup"><span data-stu-id="64c16-576">2</span></span>

<span data-ttu-id="64c16-577">3</span><span class="sxs-lookup"><span data-stu-id="64c16-577">3</span></span>

<span data-ttu-id="64c16-578">4</span><span class="sxs-lookup"><span data-stu-id="64c16-578">4</span></span>

<span data-ttu-id="64c16-579">5</span><span class="sxs-lookup"><span data-stu-id="64c16-579">5</span></span>

<span data-ttu-id="64c16-580">6</span><span class="sxs-lookup"><span data-stu-id="64c16-580">6</span></span>

<span data-ttu-id="64c16-581">7</span><span class="sxs-lookup"><span data-stu-id="64c16-581">7</span></span>

<span data-ttu-id="64c16-582">8</span><span class="sxs-lookup"><span data-stu-id="64c16-582">8</span></span>

<span data-ttu-id="64c16-583">9</span><span class="sxs-lookup"><span data-stu-id="64c16-583">9</span></span>

<span data-ttu-id="64c16-584">3</span><span class="sxs-lookup"><span data-stu-id="64c16-584">3</span></span><br/> <span data-ttu-id="64c16-585">0</span><span class="sxs-lookup"><span data-stu-id="64c16-585">0</span></span><br/>

<span data-ttu-id="64c16-586">1</span><span class="sxs-lookup"><span data-stu-id="64c16-586">1</span></span>

<span data-ttu-id="64c16-587">cclen</span><span class="sxs-lookup"><span data-stu-id="64c16-587">ccLen</span></span>

<span data-ttu-id="64c16-588">String (Variable, optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-588">string (variable, optional)</span></span>



 

<span data-ttu-id="64c16-589">**cclen**: nicht signierte 32-Bit-Ganzzahl, die die Größe des Zeichen folgen Felds in Unicode-Zeichen angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="64c16-590">Muss für eine leere Zeichenfolge auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="64c16-591">**String**: mit NULL endender Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="64c16-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="64c16-592">2.2.1.1.1 cbasestoragevariant-Strukturen</span><span class="sxs-lookup"><span data-stu-id="64c16-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="64c16-593">Die folgenden Strukturen werden in der cbasestoragevariant-Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="64c16-594">2.2.1.1.1.1 Dezimal</span><span class="sxs-lookup"><span data-stu-id="64c16-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="64c16-595">Mit Decimal wird ein genauer numerischer Wert mit fester Genauigkeit und fester Skala dargestellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="64c16-596">Wenn VType auf VT \_ Decimal (0x0000e) festgelegt ist, müssen die Felder vData1 und vData2 von cbasestoragevariant wie folgt interpretiert werden:</span><span class="sxs-lookup"><span data-stu-id="64c16-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="64c16-597">**vData1**: die Anzahl der Ziffern rechts vom Dezimaltrennzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="64c16-598">Muss zwischen 0 und 28 liegen.</span><span class="sxs-lookup"><span data-stu-id="64c16-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="64c16-599">**vData2**: das Vorzeichen des numerischen Werts.</span><span class="sxs-lookup"><span data-stu-id="64c16-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="64c16-600">Auf "0x00" festgelegt, wenn positiv, 0x80, wenn negativ.</span><span class="sxs-lookup"><span data-stu-id="64c16-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="64c16-601">Das vValue-Feld weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="64c16-601">The format of the vValue field is:</span></span>



<span data-ttu-id="64c16-602">0</span><span class="sxs-lookup"><span data-stu-id="64c16-602">0</span></span>

<span data-ttu-id="64c16-603">1</span><span class="sxs-lookup"><span data-stu-id="64c16-603">1</span></span>

<span data-ttu-id="64c16-604">2</span><span class="sxs-lookup"><span data-stu-id="64c16-604">2</span></span>

<span data-ttu-id="64c16-605">3</span><span class="sxs-lookup"><span data-stu-id="64c16-605">3</span></span>

<span data-ttu-id="64c16-606">4</span><span class="sxs-lookup"><span data-stu-id="64c16-606">4</span></span>

<span data-ttu-id="64c16-607">5</span><span class="sxs-lookup"><span data-stu-id="64c16-607">5</span></span>

<span data-ttu-id="64c16-608">6</span><span class="sxs-lookup"><span data-stu-id="64c16-608">6</span></span>

<span data-ttu-id="64c16-609">7</span><span class="sxs-lookup"><span data-stu-id="64c16-609">7</span></span>

<span data-ttu-id="64c16-610">8</span><span class="sxs-lookup"><span data-stu-id="64c16-610">8</span></span>

<span data-ttu-id="64c16-611">9</span><span class="sxs-lookup"><span data-stu-id="64c16-611">9</span></span>

<span data-ttu-id="64c16-612">1</span><span class="sxs-lookup"><span data-stu-id="64c16-612">1</span></span><br/> <span data-ttu-id="64c16-613">0</span><span class="sxs-lookup"><span data-stu-id="64c16-613">0</span></span><br/>

<span data-ttu-id="64c16-614">1</span><span class="sxs-lookup"><span data-stu-id="64c16-614">1</span></span>

<span data-ttu-id="64c16-615">2</span><span class="sxs-lookup"><span data-stu-id="64c16-615">2</span></span>

<span data-ttu-id="64c16-616">3</span><span class="sxs-lookup"><span data-stu-id="64c16-616">3</span></span>

<span data-ttu-id="64c16-617">4</span><span class="sxs-lookup"><span data-stu-id="64c16-617">4</span></span>

<span data-ttu-id="64c16-618">5</span><span class="sxs-lookup"><span data-stu-id="64c16-618">5</span></span>

<span data-ttu-id="64c16-619">6</span><span class="sxs-lookup"><span data-stu-id="64c16-619">6</span></span>

<span data-ttu-id="64c16-620">7</span><span class="sxs-lookup"><span data-stu-id="64c16-620">7</span></span>

<span data-ttu-id="64c16-621">8</span><span class="sxs-lookup"><span data-stu-id="64c16-621">8</span></span>

<span data-ttu-id="64c16-622">9</span><span class="sxs-lookup"><span data-stu-id="64c16-622">9</span></span>

<span data-ttu-id="64c16-623">2</span><span class="sxs-lookup"><span data-stu-id="64c16-623">2</span></span><br/> <span data-ttu-id="64c16-624">0</span><span class="sxs-lookup"><span data-stu-id="64c16-624">0</span></span><br/>

<span data-ttu-id="64c16-625">1</span><span class="sxs-lookup"><span data-stu-id="64c16-625">1</span></span>

<span data-ttu-id="64c16-626">2</span><span class="sxs-lookup"><span data-stu-id="64c16-626">2</span></span>

<span data-ttu-id="64c16-627">3</span><span class="sxs-lookup"><span data-stu-id="64c16-627">3</span></span>

<span data-ttu-id="64c16-628">4</span><span class="sxs-lookup"><span data-stu-id="64c16-628">4</span></span>

<span data-ttu-id="64c16-629">5</span><span class="sxs-lookup"><span data-stu-id="64c16-629">5</span></span>

<span data-ttu-id="64c16-630">6</span><span class="sxs-lookup"><span data-stu-id="64c16-630">6</span></span>

<span data-ttu-id="64c16-631">7</span><span class="sxs-lookup"><span data-stu-id="64c16-631">7</span></span>

<span data-ttu-id="64c16-632">8</span><span class="sxs-lookup"><span data-stu-id="64c16-632">8</span></span>

<span data-ttu-id="64c16-633">9</span><span class="sxs-lookup"><span data-stu-id="64c16-633">9</span></span>

<span data-ttu-id="64c16-634">3</span><span class="sxs-lookup"><span data-stu-id="64c16-634">3</span></span><br/> <span data-ttu-id="64c16-635">0</span><span class="sxs-lookup"><span data-stu-id="64c16-635">0</span></span><br/>

<span data-ttu-id="64c16-636">1</span><span class="sxs-lookup"><span data-stu-id="64c16-636">1</span></span>

<span data-ttu-id="64c16-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="64c16-637">Hi32</span></span>

<span data-ttu-id="64c16-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="64c16-638">Lo32</span></span>

<span data-ttu-id="64c16-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="64c16-639">Mid32</span></span>



 

<span data-ttu-id="64c16-640">**Hi32**: die höchsten 32 Bits der 96-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="64c16-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="64c16-641">**Lo32**: die niedrigsten 32 Bits der 96-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="64c16-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="64c16-642">**Mid32**: die mittleren 32 Bits der 96-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="64c16-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="64c16-643">2.2.1.1.1.2 VT- \_ Vektor</span><span class="sxs-lookup"><span data-stu-id="64c16-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="64c16-644">Der VT- \_ Vektor wird verwendet, um eindimensionale Arrays zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="64c16-645">0</span><span class="sxs-lookup"><span data-stu-id="64c16-645">0</span></span>

<span data-ttu-id="64c16-646">1</span><span class="sxs-lookup"><span data-stu-id="64c16-646">1</span></span>

<span data-ttu-id="64c16-647">2</span><span class="sxs-lookup"><span data-stu-id="64c16-647">2</span></span>

<span data-ttu-id="64c16-648">3</span><span class="sxs-lookup"><span data-stu-id="64c16-648">3</span></span>

<span data-ttu-id="64c16-649">4</span><span class="sxs-lookup"><span data-stu-id="64c16-649">4</span></span>

<span data-ttu-id="64c16-650">5</span><span class="sxs-lookup"><span data-stu-id="64c16-650">5</span></span>

<span data-ttu-id="64c16-651">6</span><span class="sxs-lookup"><span data-stu-id="64c16-651">6</span></span>

<span data-ttu-id="64c16-652">7</span><span class="sxs-lookup"><span data-stu-id="64c16-652">7</span></span>

<span data-ttu-id="64c16-653">8</span><span class="sxs-lookup"><span data-stu-id="64c16-653">8</span></span>

<span data-ttu-id="64c16-654">9</span><span class="sxs-lookup"><span data-stu-id="64c16-654">9</span></span>

<span data-ttu-id="64c16-655">1</span><span class="sxs-lookup"><span data-stu-id="64c16-655">1</span></span><br/> <span data-ttu-id="64c16-656">0</span><span class="sxs-lookup"><span data-stu-id="64c16-656">0</span></span><br/>

<span data-ttu-id="64c16-657">1</span><span class="sxs-lookup"><span data-stu-id="64c16-657">1</span></span>

<span data-ttu-id="64c16-658">2</span><span class="sxs-lookup"><span data-stu-id="64c16-658">2</span></span>

<span data-ttu-id="64c16-659">3</span><span class="sxs-lookup"><span data-stu-id="64c16-659">3</span></span>

<span data-ttu-id="64c16-660">4</span><span class="sxs-lookup"><span data-stu-id="64c16-660">4</span></span>

<span data-ttu-id="64c16-661">5</span><span class="sxs-lookup"><span data-stu-id="64c16-661">5</span></span>

<span data-ttu-id="64c16-662">6</span><span class="sxs-lookup"><span data-stu-id="64c16-662">6</span></span>

<span data-ttu-id="64c16-663">7</span><span class="sxs-lookup"><span data-stu-id="64c16-663">7</span></span>

<span data-ttu-id="64c16-664">8</span><span class="sxs-lookup"><span data-stu-id="64c16-664">8</span></span>

<span data-ttu-id="64c16-665">9</span><span class="sxs-lookup"><span data-stu-id="64c16-665">9</span></span>

<span data-ttu-id="64c16-666">2</span><span class="sxs-lookup"><span data-stu-id="64c16-666">2</span></span><br/> <span data-ttu-id="64c16-667">0</span><span class="sxs-lookup"><span data-stu-id="64c16-667">0</span></span><br/>

<span data-ttu-id="64c16-668">1</span><span class="sxs-lookup"><span data-stu-id="64c16-668">1</span></span>

<span data-ttu-id="64c16-669">2</span><span class="sxs-lookup"><span data-stu-id="64c16-669">2</span></span>

<span data-ttu-id="64c16-670">3</span><span class="sxs-lookup"><span data-stu-id="64c16-670">3</span></span>

<span data-ttu-id="64c16-671">4</span><span class="sxs-lookup"><span data-stu-id="64c16-671">4</span></span>

<span data-ttu-id="64c16-672">5</span><span class="sxs-lookup"><span data-stu-id="64c16-672">5</span></span>

<span data-ttu-id="64c16-673">6</span><span class="sxs-lookup"><span data-stu-id="64c16-673">6</span></span>

<span data-ttu-id="64c16-674">7</span><span class="sxs-lookup"><span data-stu-id="64c16-674">7</span></span>

<span data-ttu-id="64c16-675">8</span><span class="sxs-lookup"><span data-stu-id="64c16-675">8</span></span>

<span data-ttu-id="64c16-676">9</span><span class="sxs-lookup"><span data-stu-id="64c16-676">9</span></span>

<span data-ttu-id="64c16-677">3</span><span class="sxs-lookup"><span data-stu-id="64c16-677">3</span></span><br/> <span data-ttu-id="64c16-678">0</span><span class="sxs-lookup"><span data-stu-id="64c16-678">0</span></span><br/>

<span data-ttu-id="64c16-679">1</span><span class="sxs-lookup"><span data-stu-id="64c16-679">1</span></span>

<span data-ttu-id="64c16-680">vvector Elements</span><span class="sxs-lookup"><span data-stu-id="64c16-680">vVectorElements</span></span>

<span data-ttu-id="64c16-681">vvector Data</span><span class="sxs-lookup"><span data-stu-id="64c16-681">vVectorData</span></span>



 

<span data-ttu-id="64c16-682">**vvectorelements**: Vorzeichen lose 32-Bit-Ganzzahl, die die Anzahl der Elemente im vvectordata-Feld angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="64c16-683">**vvector Data**: ein Array von Elementen, die über einen von VType festgelegten Typ verfügen, bei dem das 0x1000-Bit gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="64c16-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="64c16-684">Die Größe eines einzelnen Elements fester Länge kann aus der Datentyp Tabelle mit fester Länge abgerufen werden, wie im Abschnitt 2.2.1.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="64c16-685">Die Länge dieses Felds in Bytes kann durch Multiplizieren von vvectorelements anhand der Größe des einzelnen Elements berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="64c16-686">Für Datentypen mit variabler Länge enthält vvector Data eine Sequenz von sequenzierten einfachen Typen, bei denen der Typ von VType angegeben wird, wobei das 0x1000-Bit gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="64c16-687">Dies schließt einen Sonderfall ein, der von der VType VT \_ array \| VT \_ Variant (z. b. 0x100c) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="64c16-688">Die Elemente im vvectordata-Feld müssen durch 0 bis 3 Auffüll Zeichen voneinander getrennt werden, sodass jedes Element bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die dieses Array enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="64c16-689">Wenn Auffüll-Bytes vorhanden sind, ist der Wert, den Sie enthalten, willkürlich.</span><span class="sxs-lookup"><span data-stu-id="64c16-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="64c16-690">Der Inhalt der Auffüll Zeichen muss vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="64c16-691">Für einen VType, der auf VT \_ Array VT Variant festgelegt ist \| \_ , ist der Typ für Elemente in dieser Sequenz cbasestoragevariant.</span><span class="sxs-lookup"><span data-stu-id="64c16-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="64c16-692">2.2.1.1.1.3 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="64c16-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="64c16-693">SAFEARRAY wird verwendet, um mehrdimensionale Arrays zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="64c16-694">Die Struktur enthält Informationen zur Array Größe sowie die Daten im Array.</span><span class="sxs-lookup"><span data-stu-id="64c16-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="64c16-695">0</span><span class="sxs-lookup"><span data-stu-id="64c16-695">0</span></span>

<span data-ttu-id="64c16-696">1</span><span class="sxs-lookup"><span data-stu-id="64c16-696">1</span></span>

<span data-ttu-id="64c16-697">2</span><span class="sxs-lookup"><span data-stu-id="64c16-697">2</span></span>

<span data-ttu-id="64c16-698">3</span><span class="sxs-lookup"><span data-stu-id="64c16-698">3</span></span>

<span data-ttu-id="64c16-699">4</span><span class="sxs-lookup"><span data-stu-id="64c16-699">4</span></span>

<span data-ttu-id="64c16-700">5</span><span class="sxs-lookup"><span data-stu-id="64c16-700">5</span></span>

<span data-ttu-id="64c16-701">6</span><span class="sxs-lookup"><span data-stu-id="64c16-701">6</span></span>

<span data-ttu-id="64c16-702">7</span><span class="sxs-lookup"><span data-stu-id="64c16-702">7</span></span>

<span data-ttu-id="64c16-703">8</span><span class="sxs-lookup"><span data-stu-id="64c16-703">8</span></span>

<span data-ttu-id="64c16-704">9</span><span class="sxs-lookup"><span data-stu-id="64c16-704">9</span></span>

<span data-ttu-id="64c16-705">1</span><span class="sxs-lookup"><span data-stu-id="64c16-705">1</span></span><br/> <span data-ttu-id="64c16-706">0</span><span class="sxs-lookup"><span data-stu-id="64c16-706">0</span></span><br/>

<span data-ttu-id="64c16-707">1</span><span class="sxs-lookup"><span data-stu-id="64c16-707">1</span></span>

<span data-ttu-id="64c16-708">2</span><span class="sxs-lookup"><span data-stu-id="64c16-708">2</span></span>

<span data-ttu-id="64c16-709">3</span><span class="sxs-lookup"><span data-stu-id="64c16-709">3</span></span>

<span data-ttu-id="64c16-710">4</span><span class="sxs-lookup"><span data-stu-id="64c16-710">4</span></span>

<span data-ttu-id="64c16-711">5</span><span class="sxs-lookup"><span data-stu-id="64c16-711">5</span></span>

<span data-ttu-id="64c16-712">6</span><span class="sxs-lookup"><span data-stu-id="64c16-712">6</span></span>

<span data-ttu-id="64c16-713">7</span><span class="sxs-lookup"><span data-stu-id="64c16-713">7</span></span>

<span data-ttu-id="64c16-714">8</span><span class="sxs-lookup"><span data-stu-id="64c16-714">8</span></span>

<span data-ttu-id="64c16-715">9</span><span class="sxs-lookup"><span data-stu-id="64c16-715">9</span></span>

<span data-ttu-id="64c16-716">2</span><span class="sxs-lookup"><span data-stu-id="64c16-716">2</span></span><br/> <span data-ttu-id="64c16-717">0</span><span class="sxs-lookup"><span data-stu-id="64c16-717">0</span></span><br/>

<span data-ttu-id="64c16-718">1</span><span class="sxs-lookup"><span data-stu-id="64c16-718">1</span></span>

<span data-ttu-id="64c16-719">2</span><span class="sxs-lookup"><span data-stu-id="64c16-719">2</span></span>

<span data-ttu-id="64c16-720">3</span><span class="sxs-lookup"><span data-stu-id="64c16-720">3</span></span>

<span data-ttu-id="64c16-721">4</span><span class="sxs-lookup"><span data-stu-id="64c16-721">4</span></span>

<span data-ttu-id="64c16-722">5</span><span class="sxs-lookup"><span data-stu-id="64c16-722">5</span></span>

<span data-ttu-id="64c16-723">6</span><span class="sxs-lookup"><span data-stu-id="64c16-723">6</span></span>

<span data-ttu-id="64c16-724">7</span><span class="sxs-lookup"><span data-stu-id="64c16-724">7</span></span>

<span data-ttu-id="64c16-725">8</span><span class="sxs-lookup"><span data-stu-id="64c16-725">8</span></span>

<span data-ttu-id="64c16-726">9</span><span class="sxs-lookup"><span data-stu-id="64c16-726">9</span></span>

<span data-ttu-id="64c16-727">3</span><span class="sxs-lookup"><span data-stu-id="64c16-727">3</span></span><br/> <span data-ttu-id="64c16-728">0</span><span class="sxs-lookup"><span data-stu-id="64c16-728">0</span></span><br/>

<span data-ttu-id="64c16-729">1</span><span class="sxs-lookup"><span data-stu-id="64c16-729">1</span></span>

<span data-ttu-id="64c16-730">cdims</span><span class="sxs-lookup"><span data-stu-id="64c16-730">cDims</span></span>

<span data-ttu-id="64c16-731">ffeaturen</span><span class="sxs-lookup"><span data-stu-id="64c16-731">fFeatures</span></span>

<span data-ttu-id="64c16-732">cbelements</span><span class="sxs-lookup"><span data-stu-id="64c16-732">cbElements</span></span>

<span data-ttu-id="64c16-733">Rgson (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-733">Rgsabound (variable)</span></span>

<span data-ttu-id="64c16-734">Vdata (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-734">vData (variable)</span></span>



 

<span data-ttu-id="64c16-735">**cdims**: ganze 16-Bit-Zahl ohne Vorzeichen, die die Anzahl der Dimensionen des mehrdimensionalen Arrays angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="64c16-736">**ffeaturen**: ein 16-Bit-Bitfeld.</span><span class="sxs-lookup"><span data-stu-id="64c16-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="64c16-737">Die Werte stellen Funktionen dar, die von Anwendungen der oberen Schicht definiert werden und ignoriert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="64c16-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="64c16-738">**cbelements**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der einzelnen Elemente des Arrays angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="64c16-739">**Rgsbound**: ein Array, das eine SAFEARRAYBOUND-Struktur enthält, die im Abschnitt 2.2.1.1.1.4 pro Dimension im SafeArray angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="64c16-740">Dieses Array verfügt über die linke Dimension First und die Dimension ganz rechts.</span><span class="sxs-lookup"><span data-stu-id="64c16-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="64c16-741">**VData**: ein Vektor gemarshallter Elemente eines bestimmten Typs, der durch den VType der enthaltenden cbasestoragevariant gekennzeichnet ist, wobei das Bit 0x2000 gelöscht ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="64c16-742">VData wird ähnlich \_ wie der VT-Vektor wie im Abschnitt 2.2.1.1.1.2 angegeben, mit dem Unterschied, dass die Anzahl der Elemente nicht vor dem Vektor gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="64c16-743">Stattdessen wird die Anzahl der Elemente berechnet, indem der Wert für "celements" mit allen sicheren Array Begrenzungen multipliziert wird, die im Feld "rgsabound" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="64c16-744">Elemente werden in einem Vektor in der Reihenfolge von Dimensionen gespeichert, beginnend mit der äußersten rechten Dimension.</span><span class="sxs-lookup"><span data-stu-id="64c16-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="64c16-745">Das folgende Diagramm stellt visuell ein zweidimensionales Beispiel Array dar.</span><span class="sxs-lookup"><span data-stu-id="64c16-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="64c16-746">In der ersten Dimension sind die celements gleich 4 (dargestellt horizontal) und llbound gleich 0, und die zweite Dimension hat die celements gleich 2 (vertikal dargestellt) und llbound gleich 0.</span><span class="sxs-lookup"><span data-stu-id="64c16-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>



|            |            |            |            |
|------------|------------|------------|------------|
| <span data-ttu-id="64c16-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-747">0x00000001</span></span> | <span data-ttu-id="64c16-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-748">0x00000002</span></span> | <span data-ttu-id="64c16-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-749">0x00000003</span></span> | <span data-ttu-id="64c16-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="64c16-750">0x00000005</span></span> |
| <span data-ttu-id="64c16-751">0x00000007</span><span class="sxs-lookup"><span data-stu-id="64c16-751">0x00000007</span></span> | <span data-ttu-id="64c16-752">0x00000011</span><span class="sxs-lookup"><span data-stu-id="64c16-752">0x00000011</span></span> | <span data-ttu-id="64c16-753">0x00000013</span><span class="sxs-lookup"><span data-stu-id="64c16-753">0x00000013</span></span> | <span data-ttu-id="64c16-754">0x00000017</span><span class="sxs-lookup"><span data-stu-id="64c16-754">0x00000017</span></span> |



 

<span data-ttu-id="64c16-755">Mithilfe des obigen Diagramms enthalten VData die folgende Sequenz: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005 bei der, 0x00000017 (Iteration durch die Rechte äußerste Dimension und anschließendes erhöhen der nächsten Dimension).</span><span class="sxs-lookup"><span data-stu-id="64c16-755">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="64c16-756">Die vorangehende rgsbound (die die "celements" und "LBound" aufzeichnet) lautet: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="64c16-756">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="64c16-757">2.2.1.1.1.4 SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="64c16-757">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="64c16-758">Die SAFEARRAYBOUND-Struktur stellt die Begrenzungen einer Dimension eines SAFEARRAY oder SAFEARRAY2 dar.</span><span class="sxs-lookup"><span data-stu-id="64c16-758">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="64c16-759">Das Format lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-759">Its format is:</span></span>



<span data-ttu-id="64c16-760">0</span><span class="sxs-lookup"><span data-stu-id="64c16-760">0</span></span>

<span data-ttu-id="64c16-761">1</span><span class="sxs-lookup"><span data-stu-id="64c16-761">1</span></span>

<span data-ttu-id="64c16-762">2</span><span class="sxs-lookup"><span data-stu-id="64c16-762">2</span></span>

<span data-ttu-id="64c16-763">3</span><span class="sxs-lookup"><span data-stu-id="64c16-763">3</span></span>

<span data-ttu-id="64c16-764">4</span><span class="sxs-lookup"><span data-stu-id="64c16-764">4</span></span>

<span data-ttu-id="64c16-765">5</span><span class="sxs-lookup"><span data-stu-id="64c16-765">5</span></span>

<span data-ttu-id="64c16-766">6</span><span class="sxs-lookup"><span data-stu-id="64c16-766">6</span></span>

<span data-ttu-id="64c16-767">7</span><span class="sxs-lookup"><span data-stu-id="64c16-767">7</span></span>

<span data-ttu-id="64c16-768">8</span><span class="sxs-lookup"><span data-stu-id="64c16-768">8</span></span>

<span data-ttu-id="64c16-769">9</span><span class="sxs-lookup"><span data-stu-id="64c16-769">9</span></span>

<span data-ttu-id="64c16-770">1</span><span class="sxs-lookup"><span data-stu-id="64c16-770">1</span></span><br/> <span data-ttu-id="64c16-771">0</span><span class="sxs-lookup"><span data-stu-id="64c16-771">0</span></span><br/>

<span data-ttu-id="64c16-772">1</span><span class="sxs-lookup"><span data-stu-id="64c16-772">1</span></span>

<span data-ttu-id="64c16-773">2</span><span class="sxs-lookup"><span data-stu-id="64c16-773">2</span></span>

<span data-ttu-id="64c16-774">3</span><span class="sxs-lookup"><span data-stu-id="64c16-774">3</span></span>

<span data-ttu-id="64c16-775">4</span><span class="sxs-lookup"><span data-stu-id="64c16-775">4</span></span>

<span data-ttu-id="64c16-776">5</span><span class="sxs-lookup"><span data-stu-id="64c16-776">5</span></span>

<span data-ttu-id="64c16-777">6</span><span class="sxs-lookup"><span data-stu-id="64c16-777">6</span></span>

<span data-ttu-id="64c16-778">7</span><span class="sxs-lookup"><span data-stu-id="64c16-778">7</span></span>

<span data-ttu-id="64c16-779">8</span><span class="sxs-lookup"><span data-stu-id="64c16-779">8</span></span>

<span data-ttu-id="64c16-780">9</span><span class="sxs-lookup"><span data-stu-id="64c16-780">9</span></span>

<span data-ttu-id="64c16-781">2</span><span class="sxs-lookup"><span data-stu-id="64c16-781">2</span></span><br/> <span data-ttu-id="64c16-782">0</span><span class="sxs-lookup"><span data-stu-id="64c16-782">0</span></span><br/>

<span data-ttu-id="64c16-783">1</span><span class="sxs-lookup"><span data-stu-id="64c16-783">1</span></span>

<span data-ttu-id="64c16-784">2</span><span class="sxs-lookup"><span data-stu-id="64c16-784">2</span></span>

<span data-ttu-id="64c16-785">3</span><span class="sxs-lookup"><span data-stu-id="64c16-785">3</span></span>

<span data-ttu-id="64c16-786">4</span><span class="sxs-lookup"><span data-stu-id="64c16-786">4</span></span>

<span data-ttu-id="64c16-787">5</span><span class="sxs-lookup"><span data-stu-id="64c16-787">5</span></span>

<span data-ttu-id="64c16-788">6</span><span class="sxs-lookup"><span data-stu-id="64c16-788">6</span></span>

<span data-ttu-id="64c16-789">7</span><span class="sxs-lookup"><span data-stu-id="64c16-789">7</span></span>

<span data-ttu-id="64c16-790">8</span><span class="sxs-lookup"><span data-stu-id="64c16-790">8</span></span>

<span data-ttu-id="64c16-791">9</span><span class="sxs-lookup"><span data-stu-id="64c16-791">9</span></span>

<span data-ttu-id="64c16-792">3</span><span class="sxs-lookup"><span data-stu-id="64c16-792">3</span></span><br/> <span data-ttu-id="64c16-793">0</span><span class="sxs-lookup"><span data-stu-id="64c16-793">0</span></span><br/>

<span data-ttu-id="64c16-794">1</span><span class="sxs-lookup"><span data-stu-id="64c16-794">1</span></span>

<span data-ttu-id="64c16-795">cElements</span><span class="sxs-lookup"><span data-stu-id="64c16-795">cElements</span></span>

<span data-ttu-id="64c16-796">llbound</span><span class="sxs-lookup"><span data-stu-id="64c16-796">lLbound</span></span>



 

<span data-ttu-id="64c16-797">**celements**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente in der Dimension angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-797">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="64c16-798">**llbound**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die untere Grenze der Dimension angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-798">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="64c16-799">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="64c16-799">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="64c16-800">SAFEARRAY2 wird verwendet, um mehrdimensionale Arrays in serializedpropertyvalue zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-800">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="64c16-801">Die Struktur enthält Grenz Informationen und die Daten.</span><span class="sxs-lookup"><span data-stu-id="64c16-801">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="64c16-802">0</span><span class="sxs-lookup"><span data-stu-id="64c16-802">0</span></span>

<span data-ttu-id="64c16-803">1</span><span class="sxs-lookup"><span data-stu-id="64c16-803">1</span></span>

<span data-ttu-id="64c16-804">2</span><span class="sxs-lookup"><span data-stu-id="64c16-804">2</span></span>

<span data-ttu-id="64c16-805">3</span><span class="sxs-lookup"><span data-stu-id="64c16-805">3</span></span>

<span data-ttu-id="64c16-806">4</span><span class="sxs-lookup"><span data-stu-id="64c16-806">4</span></span>

<span data-ttu-id="64c16-807">5</span><span class="sxs-lookup"><span data-stu-id="64c16-807">5</span></span>

<span data-ttu-id="64c16-808">6</span><span class="sxs-lookup"><span data-stu-id="64c16-808">6</span></span>

<span data-ttu-id="64c16-809">7</span><span class="sxs-lookup"><span data-stu-id="64c16-809">7</span></span>

<span data-ttu-id="64c16-810">8</span><span class="sxs-lookup"><span data-stu-id="64c16-810">8</span></span>

<span data-ttu-id="64c16-811">9</span><span class="sxs-lookup"><span data-stu-id="64c16-811">9</span></span>

<span data-ttu-id="64c16-812">1</span><span class="sxs-lookup"><span data-stu-id="64c16-812">1</span></span><br/> <span data-ttu-id="64c16-813">0</span><span class="sxs-lookup"><span data-stu-id="64c16-813">0</span></span><br/>

<span data-ttu-id="64c16-814">1</span><span class="sxs-lookup"><span data-stu-id="64c16-814">1</span></span>

<span data-ttu-id="64c16-815">2</span><span class="sxs-lookup"><span data-stu-id="64c16-815">2</span></span>

<span data-ttu-id="64c16-816">3</span><span class="sxs-lookup"><span data-stu-id="64c16-816">3</span></span>

<span data-ttu-id="64c16-817">4</span><span class="sxs-lookup"><span data-stu-id="64c16-817">4</span></span>

<span data-ttu-id="64c16-818">5</span><span class="sxs-lookup"><span data-stu-id="64c16-818">5</span></span>

<span data-ttu-id="64c16-819">6</span><span class="sxs-lookup"><span data-stu-id="64c16-819">6</span></span>

<span data-ttu-id="64c16-820">7</span><span class="sxs-lookup"><span data-stu-id="64c16-820">7</span></span>

<span data-ttu-id="64c16-821">8</span><span class="sxs-lookup"><span data-stu-id="64c16-821">8</span></span>

<span data-ttu-id="64c16-822">9</span><span class="sxs-lookup"><span data-stu-id="64c16-822">9</span></span>

<span data-ttu-id="64c16-823">2</span><span class="sxs-lookup"><span data-stu-id="64c16-823">2</span></span><br/> <span data-ttu-id="64c16-824">0</span><span class="sxs-lookup"><span data-stu-id="64c16-824">0</span></span><br/>

<span data-ttu-id="64c16-825">1</span><span class="sxs-lookup"><span data-stu-id="64c16-825">1</span></span>

<span data-ttu-id="64c16-826">2</span><span class="sxs-lookup"><span data-stu-id="64c16-826">2</span></span>

<span data-ttu-id="64c16-827">3</span><span class="sxs-lookup"><span data-stu-id="64c16-827">3</span></span>

<span data-ttu-id="64c16-828">4</span><span class="sxs-lookup"><span data-stu-id="64c16-828">4</span></span>

<span data-ttu-id="64c16-829">5</span><span class="sxs-lookup"><span data-stu-id="64c16-829">5</span></span>

<span data-ttu-id="64c16-830">6</span><span class="sxs-lookup"><span data-stu-id="64c16-830">6</span></span>

<span data-ttu-id="64c16-831">7</span><span class="sxs-lookup"><span data-stu-id="64c16-831">7</span></span>

<span data-ttu-id="64c16-832">8</span><span class="sxs-lookup"><span data-stu-id="64c16-832">8</span></span>

<span data-ttu-id="64c16-833">9</span><span class="sxs-lookup"><span data-stu-id="64c16-833">9</span></span>

<span data-ttu-id="64c16-834">3</span><span class="sxs-lookup"><span data-stu-id="64c16-834">3</span></span><br/> <span data-ttu-id="64c16-835">0</span><span class="sxs-lookup"><span data-stu-id="64c16-835">0</span></span><br/>

<span data-ttu-id="64c16-836">1</span><span class="sxs-lookup"><span data-stu-id="64c16-836">1</span></span>

<span data-ttu-id="64c16-837">cdims</span><span class="sxs-lookup"><span data-stu-id="64c16-837">cDims</span></span>

<span data-ttu-id="64c16-838">Rgson (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-838">Rgsabound (variable)</span></span>

<span data-ttu-id="64c16-839">Vdata (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-839">vData (variable)</span></span>



 

<span data-ttu-id="64c16-840">**cdims**: nicht signierte 32-Bit-Ganzzahl, die die Anzahl der Dimensionen des SAFEARRAY2 angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-840">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="64c16-841">**Rgsbound**: ein Array, das eine SAFEARRAYBOUND-Struktur enthält, wie im Abschnitt 2.2.1.1.1.4 pro Dimension in der SAFEARRAY2 angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-841">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="64c16-842">Dieses Array verfügt über die linke Dimension First und die Dimension ganz rechts.</span><span class="sxs-lookup"><span data-stu-id="64c16-842">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="64c16-843">**VData**: ein Vektor gemarshallter Elemente eines bestimmten Typs, der durch den dwType des enthaltenden serializedpropertyvalue angegeben wird, wobei Bit 0x2000 gelöscht ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-843">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="64c16-844">Das Format von VData entspricht dem, das für das VData-Feld von SAFEARRAY im Abschnitt 2.2.1.1.1.3 angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="64c16-844">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="64c16-845">2.2.1.2 cfullpropspec</span><span class="sxs-lookup"><span data-stu-id="64c16-845">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="64c16-846">Die cfullpropspec-Struktur enthält eine Eigenschaften Satz-GUID und einen Eigenschafts Bezeichner, um die Eigenschaft eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="64c16-846">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="64c16-847">0</span><span class="sxs-lookup"><span data-stu-id="64c16-847">0</span></span>

<span data-ttu-id="64c16-848">1</span><span class="sxs-lookup"><span data-stu-id="64c16-848">1</span></span>

<span data-ttu-id="64c16-849">2</span><span class="sxs-lookup"><span data-stu-id="64c16-849">2</span></span>

<span data-ttu-id="64c16-850">3</span><span class="sxs-lookup"><span data-stu-id="64c16-850">3</span></span>

<span data-ttu-id="64c16-851">4</span><span class="sxs-lookup"><span data-stu-id="64c16-851">4</span></span>

<span data-ttu-id="64c16-852">5</span><span class="sxs-lookup"><span data-stu-id="64c16-852">5</span></span>

<span data-ttu-id="64c16-853">6</span><span class="sxs-lookup"><span data-stu-id="64c16-853">6</span></span>

<span data-ttu-id="64c16-854">7</span><span class="sxs-lookup"><span data-stu-id="64c16-854">7</span></span>

<span data-ttu-id="64c16-855">8</span><span class="sxs-lookup"><span data-stu-id="64c16-855">8</span></span>

<span data-ttu-id="64c16-856">9</span><span class="sxs-lookup"><span data-stu-id="64c16-856">9</span></span>

<span data-ttu-id="64c16-857">1</span><span class="sxs-lookup"><span data-stu-id="64c16-857">1</span></span><br/> <span data-ttu-id="64c16-858">0</span><span class="sxs-lookup"><span data-stu-id="64c16-858">0</span></span><br/>

<span data-ttu-id="64c16-859">1</span><span class="sxs-lookup"><span data-stu-id="64c16-859">1</span></span>

<span data-ttu-id="64c16-860">2</span><span class="sxs-lookup"><span data-stu-id="64c16-860">2</span></span>

<span data-ttu-id="64c16-861">3</span><span class="sxs-lookup"><span data-stu-id="64c16-861">3</span></span>

<span data-ttu-id="64c16-862">4</span><span class="sxs-lookup"><span data-stu-id="64c16-862">4</span></span>

<span data-ttu-id="64c16-863">5</span><span class="sxs-lookup"><span data-stu-id="64c16-863">5</span></span>

<span data-ttu-id="64c16-864">6</span><span class="sxs-lookup"><span data-stu-id="64c16-864">6</span></span>

<span data-ttu-id="64c16-865">7</span><span class="sxs-lookup"><span data-stu-id="64c16-865">7</span></span>

<span data-ttu-id="64c16-866">8</span><span class="sxs-lookup"><span data-stu-id="64c16-866">8</span></span>

<span data-ttu-id="64c16-867">9</span><span class="sxs-lookup"><span data-stu-id="64c16-867">9</span></span>

<span data-ttu-id="64c16-868">2</span><span class="sxs-lookup"><span data-stu-id="64c16-868">2</span></span><br/> <span data-ttu-id="64c16-869">0</span><span class="sxs-lookup"><span data-stu-id="64c16-869">0</span></span><br/>

<span data-ttu-id="64c16-870">1</span><span class="sxs-lookup"><span data-stu-id="64c16-870">1</span></span>

<span data-ttu-id="64c16-871">2</span><span class="sxs-lookup"><span data-stu-id="64c16-871">2</span></span>

<span data-ttu-id="64c16-872">3</span><span class="sxs-lookup"><span data-stu-id="64c16-872">3</span></span>

<span data-ttu-id="64c16-873">4</span><span class="sxs-lookup"><span data-stu-id="64c16-873">4</span></span>

<span data-ttu-id="64c16-874">5</span><span class="sxs-lookup"><span data-stu-id="64c16-874">5</span></span>

<span data-ttu-id="64c16-875">6</span><span class="sxs-lookup"><span data-stu-id="64c16-875">6</span></span>

<span data-ttu-id="64c16-876">7</span><span class="sxs-lookup"><span data-stu-id="64c16-876">7</span></span>

<span data-ttu-id="64c16-877">8</span><span class="sxs-lookup"><span data-stu-id="64c16-877">8</span></span>

<span data-ttu-id="64c16-878">9</span><span class="sxs-lookup"><span data-stu-id="64c16-878">9</span></span>

<span data-ttu-id="64c16-879">3</span><span class="sxs-lookup"><span data-stu-id="64c16-879">3</span></span><br/> <span data-ttu-id="64c16-880">0</span><span class="sxs-lookup"><span data-stu-id="64c16-880">0</span></span><br/>

<span data-ttu-id="64c16-881">1</span><span class="sxs-lookup"><span data-stu-id="64c16-881">1</span></span>

<span data-ttu-id="64c16-882">\_guidpropset</span><span class="sxs-lookup"><span data-stu-id="64c16-882">\_guidPropSet</span></span>

<span data-ttu-id="64c16-883">...</span><span class="sxs-lookup"><span data-stu-id="64c16-883">...</span></span>

<span data-ttu-id="64c16-884">...</span><span class="sxs-lookup"><span data-stu-id="64c16-884">...</span></span>

<span data-ttu-id="64c16-885">...</span><span class="sxs-lookup"><span data-stu-id="64c16-885">...</span></span>

<span data-ttu-id="64c16-886">ulkind</span><span class="sxs-lookup"><span data-stu-id="64c16-886">ulKind</span></span>

<span data-ttu-id="64c16-887">Prspec</span><span class="sxs-lookup"><span data-stu-id="64c16-887">PrSpec</span></span>

<span data-ttu-id="64c16-888">Eigenschaftsname (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-888">Property name (variable)</span></span>



 

<span data-ttu-id="64c16-889">**\_ guidpropset**: die GUID des Eigenschaften Satzes, zu dem die Eigenschaft gehört.</span><span class="sxs-lookup"><span data-stu-id="64c16-889">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="64c16-890">**ulkind**: eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-890">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="64c16-891">Einer der folgenden Werte, der den Inhalt von prspec angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-891">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="64c16-892">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-892">Value</span></span>                                            | <span data-ttu-id="64c16-893">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-893">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-894">prspec \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="64c16-894">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="64c16-895">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-895">0x00000000</span></span><br/> | <span data-ttu-id="64c16-896">Das Feld "prspec" gibt die Anzahl der Zeichen an, die nicht NULL sind, im Feldeigenschaften Name.</span><span class="sxs-lookup"><span data-stu-id="64c16-896">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="64c16-897">prspec- \_ PROPID</span><span class="sxs-lookup"><span data-stu-id="64c16-897">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="64c16-898">0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-898">0x00000001</span></span><br/>  | <span data-ttu-id="64c16-899">Das Feld "prspec" gibt die eigen schafts-ID (PROPID) an.</span><span class="sxs-lookup"><span data-stu-id="64c16-899">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="64c16-900">**Prspec**: eine 32-Bit-Ganzzahl ohne Vorzeichen mit einer Bedeutung, wie im Feld ulkind angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-900">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="64c16-901">**Eigenschaftsname**: Wenn ulkind auf prspec PROPID festgelegt ist \_ , darf dieses Feld nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-901">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="64c16-902">Wenn ulkind auf prspec \_ LPWSTR festgelegt ist, muss dieses Feld ein Array von prspec-Unicode-Zeichen ohne Berücksichtigung der Groß-und Kleinschreibung enthalten, das den Namen der Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-902">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="64c16-903">2.2.1.3 Ccontent-Einschränkung</span><span class="sxs-lookup"><span data-stu-id="64c16-903">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="64c16-904">Die Ccontent-Einschränkungs Struktur enthält eine Zeichenfolge, die einer Eigenschaft im Eigenschaften Cache entspricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-904">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="64c16-905">0</span><span class="sxs-lookup"><span data-stu-id="64c16-905">0</span></span>

<span data-ttu-id="64c16-906">1</span><span class="sxs-lookup"><span data-stu-id="64c16-906">1</span></span>

<span data-ttu-id="64c16-907">2</span><span class="sxs-lookup"><span data-stu-id="64c16-907">2</span></span>

<span data-ttu-id="64c16-908">3</span><span class="sxs-lookup"><span data-stu-id="64c16-908">3</span></span>

<span data-ttu-id="64c16-909">4</span><span class="sxs-lookup"><span data-stu-id="64c16-909">4</span></span>

<span data-ttu-id="64c16-910">5</span><span class="sxs-lookup"><span data-stu-id="64c16-910">5</span></span>

<span data-ttu-id="64c16-911">6</span><span class="sxs-lookup"><span data-stu-id="64c16-911">6</span></span>

<span data-ttu-id="64c16-912">7</span><span class="sxs-lookup"><span data-stu-id="64c16-912">7</span></span>

<span data-ttu-id="64c16-913">8</span><span class="sxs-lookup"><span data-stu-id="64c16-913">8</span></span>

<span data-ttu-id="64c16-914">9</span><span class="sxs-lookup"><span data-stu-id="64c16-914">9</span></span>

<span data-ttu-id="64c16-915">1</span><span class="sxs-lookup"><span data-stu-id="64c16-915">1</span></span><br/> <span data-ttu-id="64c16-916">0</span><span class="sxs-lookup"><span data-stu-id="64c16-916">0</span></span><br/>

<span data-ttu-id="64c16-917">1</span><span class="sxs-lookup"><span data-stu-id="64c16-917">1</span></span>

<span data-ttu-id="64c16-918">2</span><span class="sxs-lookup"><span data-stu-id="64c16-918">2</span></span>

<span data-ttu-id="64c16-919">3</span><span class="sxs-lookup"><span data-stu-id="64c16-919">3</span></span>

<span data-ttu-id="64c16-920">4</span><span class="sxs-lookup"><span data-stu-id="64c16-920">4</span></span>

<span data-ttu-id="64c16-921">5</span><span class="sxs-lookup"><span data-stu-id="64c16-921">5</span></span>

<span data-ttu-id="64c16-922">6</span><span class="sxs-lookup"><span data-stu-id="64c16-922">6</span></span>

<span data-ttu-id="64c16-923">7</span><span class="sxs-lookup"><span data-stu-id="64c16-923">7</span></span>

<span data-ttu-id="64c16-924">8</span><span class="sxs-lookup"><span data-stu-id="64c16-924">8</span></span>

<span data-ttu-id="64c16-925">9</span><span class="sxs-lookup"><span data-stu-id="64c16-925">9</span></span>

<span data-ttu-id="64c16-926">2</span><span class="sxs-lookup"><span data-stu-id="64c16-926">2</span></span><br/> <span data-ttu-id="64c16-927">0</span><span class="sxs-lookup"><span data-stu-id="64c16-927">0</span></span><br/>

<span data-ttu-id="64c16-928">1</span><span class="sxs-lookup"><span data-stu-id="64c16-928">1</span></span>

<span data-ttu-id="64c16-929">2</span><span class="sxs-lookup"><span data-stu-id="64c16-929">2</span></span>

<span data-ttu-id="64c16-930">3</span><span class="sxs-lookup"><span data-stu-id="64c16-930">3</span></span>

<span data-ttu-id="64c16-931">4</span><span class="sxs-lookup"><span data-stu-id="64c16-931">4</span></span>

<span data-ttu-id="64c16-932">5</span><span class="sxs-lookup"><span data-stu-id="64c16-932">5</span></span>

<span data-ttu-id="64c16-933">6</span><span class="sxs-lookup"><span data-stu-id="64c16-933">6</span></span>

<span data-ttu-id="64c16-934">7</span><span class="sxs-lookup"><span data-stu-id="64c16-934">7</span></span>

<span data-ttu-id="64c16-935">8</span><span class="sxs-lookup"><span data-stu-id="64c16-935">8</span></span>

<span data-ttu-id="64c16-936">9</span><span class="sxs-lookup"><span data-stu-id="64c16-936">9</span></span>

<span data-ttu-id="64c16-937">3</span><span class="sxs-lookup"><span data-stu-id="64c16-937">3</span></span><br/> <span data-ttu-id="64c16-938">0</span><span class="sxs-lookup"><span data-stu-id="64c16-938">0</span></span><br/>

<span data-ttu-id="64c16-939">1</span><span class="sxs-lookup"><span data-stu-id="64c16-939">1</span></span>

<span data-ttu-id="64c16-940">\_Property (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-940">\_Property (variable)</span></span>

<span data-ttu-id="64c16-941">...</span><span class="sxs-lookup"><span data-stu-id="64c16-941">...</span></span>

<span data-ttu-id="64c16-942">Padding1 (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-942">Padding1 (variable)</span></span>

<span data-ttu-id="64c16-943">Cc</span><span class="sxs-lookup"><span data-stu-id="64c16-943">Cc</span></span>

<span data-ttu-id="64c16-944">\_pwcspphrase (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-944">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="64c16-945">...</span><span class="sxs-lookup"><span data-stu-id="64c16-945">...</span></span>

<span data-ttu-id="64c16-946">Padding2 (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-946">Padding2 (variable)</span></span>

<span data-ttu-id="64c16-947">lcid</span><span class="sxs-lookup"><span data-stu-id="64c16-947">lcid</span></span>

<span data-ttu-id="64c16-948">\_ulgeneratemethod</span><span class="sxs-lookup"><span data-stu-id="64c16-948">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="64c16-949">**\_ Property**: eine cfullpropspec-Struktur, wie im Abschnitt 2.2.1.2 angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-949">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="64c16-950">Dieses Feld gibt die Eigenschaft an, für die ein Übereinstimmungs Vorgang durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-950">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="64c16-951">**Padding1**: Dieses Feld muss zwischen 0 und 3 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-951">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="64c16-952">Die Länge dieses Felds muss so lauten, dass das folgende Feld bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-952">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="64c16-953">Wenn dieses Feld vorhanden ist (d. h. eine Länge ungleich 0 (null)), ist der enthaltene Wert beliebig.</span><span class="sxs-lookup"><span data-stu-id="64c16-953">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="64c16-954">Der Inhalt dieses Felds muss vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-954">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="64c16-955">**CC**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von Zeichen im \_ Feld "pwcspphrase" angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-955">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="64c16-956">**\_ pwcspphrase**: eine Unicode-Zeichenfolge, die nicht auf NULL fest steht und das Wort oder den Ausdruck darstellt, der mit der Eigenschaft verglichen werden soll</span><span class="sxs-lookup"><span data-stu-id="64c16-956">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="64c16-957">Dieses Feld darf nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-957">This field MUST NOT be empty.</span></span> <span data-ttu-id="64c16-958">Das CC-Feld enthält die Länge der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="64c16-958">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="64c16-959">**Padding2**: Dieses Feld muss zwischen 0 und 3 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-959">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="64c16-960">Die Länge dieses Felds muss so lauten, dass das folgende Feld bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-960">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="64c16-961">Wenn dieses Feld vorhanden ist (d. h. eine Länge ungleich 0 (null)), ist der enthaltene Wert beliebig.</span><span class="sxs-lookup"><span data-stu-id="64c16-961">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="64c16-962">Der Inhalt dieses Felds muss vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-962">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="64c16-963">**LCID**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Gebiets Schema der \_ pwcspphrase angibt, wie in \[ MS-GPSI \] Anhang A angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-963">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="64c16-964">**\_ ulgeneratemethod**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Methode angibt, die beim Generieren alternativer Wort Formulare verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-964">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="64c16-965">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-965">Value</span></span>                                                       | <span data-ttu-id="64c16-966">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-966">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-967">\_Methode \_ genau generieren</span><span class="sxs-lookup"><span data-stu-id="64c16-967">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="64c16-968">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-968">0x00000000</span></span><br/>    | <span data-ttu-id="64c16-969">Genaue Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="64c16-969">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="64c16-970">\_Methoden \_ Präfix generieren</span><span class="sxs-lookup"><span data-stu-id="64c16-970">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="64c16-971">0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-971">0x00000001</span></span> <br/>  | <span data-ttu-id="64c16-972">Präfix Übereinstimmung</span><span class="sxs-lookup"><span data-stu-id="64c16-972">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="64c16-973">\_Methode als \_ inflect generieren</span><span class="sxs-lookup"><span data-stu-id="64c16-973">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="64c16-974">0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-974">0x00000002</span></span><br/> | <span data-ttu-id="64c16-975">Findet eine Entsprechung für ein Wort.</span><span class="sxs-lookup"><span data-stu-id="64c16-975">Matches inflections of a word.</span></span> <span data-ttu-id="64c16-976">Eine Einfügung eines Worts ist eine Variante des Stamm Worts im gleichen Teil der Sprache, die gemäß den linguistischen Regeln einer bestimmten Sprache geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="64c16-976">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="64c16-977">Beispielsweise umfassen "Swim", "swims", "Swimming" und "Swap" die inflektionen des Verbs "Swimming" in englischer Sprache.</span><span class="sxs-lookup"><span data-stu-id="64c16-977">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="64c16-978">2.2.1.4 CKey</span><span class="sxs-lookup"><span data-stu-id="64c16-978">2.2.1.4 CKey</span></span>

<span data-ttu-id="64c16-979">Die CKey-Struktur enthält einen-Eigenschafts Wert.</span><span class="sxs-lookup"><span data-stu-id="64c16-979">The CKey structure contains a property value.</span></span>



<span data-ttu-id="64c16-980">0</span><span class="sxs-lookup"><span data-stu-id="64c16-980">0</span></span>

<span data-ttu-id="64c16-981">1</span><span class="sxs-lookup"><span data-stu-id="64c16-981">1</span></span>

<span data-ttu-id="64c16-982">2</span><span class="sxs-lookup"><span data-stu-id="64c16-982">2</span></span>

<span data-ttu-id="64c16-983">3</span><span class="sxs-lookup"><span data-stu-id="64c16-983">3</span></span>

<span data-ttu-id="64c16-984">4</span><span class="sxs-lookup"><span data-stu-id="64c16-984">4</span></span>

<span data-ttu-id="64c16-985">5</span><span class="sxs-lookup"><span data-stu-id="64c16-985">5</span></span>

<span data-ttu-id="64c16-986">6</span><span class="sxs-lookup"><span data-stu-id="64c16-986">6</span></span>

<span data-ttu-id="64c16-987">7</span><span class="sxs-lookup"><span data-stu-id="64c16-987">7</span></span>

<span data-ttu-id="64c16-988">8</span><span class="sxs-lookup"><span data-stu-id="64c16-988">8</span></span>

<span data-ttu-id="64c16-989">9</span><span class="sxs-lookup"><span data-stu-id="64c16-989">9</span></span>

<span data-ttu-id="64c16-990">1</span><span class="sxs-lookup"><span data-stu-id="64c16-990">1</span></span><br/> <span data-ttu-id="64c16-991">0</span><span class="sxs-lookup"><span data-stu-id="64c16-991">0</span></span><br/>

<span data-ttu-id="64c16-992">1</span><span class="sxs-lookup"><span data-stu-id="64c16-992">1</span></span>

<span data-ttu-id="64c16-993">2</span><span class="sxs-lookup"><span data-stu-id="64c16-993">2</span></span>

<span data-ttu-id="64c16-994">3</span><span class="sxs-lookup"><span data-stu-id="64c16-994">3</span></span>

<span data-ttu-id="64c16-995">4</span><span class="sxs-lookup"><span data-stu-id="64c16-995">4</span></span>

<span data-ttu-id="64c16-996">5</span><span class="sxs-lookup"><span data-stu-id="64c16-996">5</span></span>

<span data-ttu-id="64c16-997">6</span><span class="sxs-lookup"><span data-stu-id="64c16-997">6</span></span>

<span data-ttu-id="64c16-998">7</span><span class="sxs-lookup"><span data-stu-id="64c16-998">7</span></span>

<span data-ttu-id="64c16-999">8</span><span class="sxs-lookup"><span data-stu-id="64c16-999">8</span></span>

<span data-ttu-id="64c16-1000">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1000">9</span></span>

<span data-ttu-id="64c16-1001">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1001">2</span></span><br/> <span data-ttu-id="64c16-1002">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1002">0</span></span><br/>

<span data-ttu-id="64c16-1003">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1003">1</span></span>

<span data-ttu-id="64c16-1004">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1004">2</span></span>

<span data-ttu-id="64c16-1005">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1005">3</span></span>

<span data-ttu-id="64c16-1006">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1006">4</span></span>

<span data-ttu-id="64c16-1007">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1007">5</span></span>

<span data-ttu-id="64c16-1008">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1008">6</span></span>

<span data-ttu-id="64c16-1009">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1009">7</span></span>

<span data-ttu-id="64c16-1010">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1010">8</span></span>

<span data-ttu-id="64c16-1011">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1011">9</span></span>

<span data-ttu-id="64c16-1012">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1012">3</span></span><br/> <span data-ttu-id="64c16-1013">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1013">0</span></span><br/>

<span data-ttu-id="64c16-1014">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1014">1</span></span>

<span data-ttu-id="64c16-1015">PROPID</span><span class="sxs-lookup"><span data-stu-id="64c16-1015">PROPID</span></span>

<span data-ttu-id="64c16-1016">Betrieben</span><span class="sxs-lookup"><span data-stu-id="64c16-1016">Cb</span></span>

<span data-ttu-id="64c16-1017">buf (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1017">buf (variable)</span></span>



 

<span data-ttu-id="64c16-1018">**PROPID**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die eigen schafts-ID darstellt, wie im Abschnitt 1.8.1 erläutert.</span><span class="sxs-lookup"><span data-stu-id="64c16-1018">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="64c16-1019">Bekannte Werte sind:</span><span class="sxs-lookup"><span data-stu-id="64c16-1019">Well-known values are:</span></span>



| <span data-ttu-id="64c16-1020">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-1020">Value</span></span>      | <span data-ttu-id="64c16-1021">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-1021">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="64c16-1022">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="64c16-1022">0xFFFFFFFF</span></span> | <span data-ttu-id="64c16-1023">Stellt eine ungültige Eigenschaften-ID dar und darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1023">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="64c16-1024">0xfffffffe</span><span class="sxs-lookup"><span data-stu-id="64c16-1024">0xFFFFFFFE</span></span> | <span data-ttu-id="64c16-1025">Stellt eine ungültige Eigenschaften-ID dar und darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1025">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="64c16-1026">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-1026">0x00000000</span></span> | <span data-ttu-id="64c16-1027">Stellt eine beliebige Eigenschaften-ID dar.</span><span class="sxs-lookup"><span data-stu-id="64c16-1027">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="64c16-1028">**CB**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge von buf in Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-1028">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="64c16-1029">**buf**: eine Byte Sequenz, die den Wert der-Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1029">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="64c16-1030">2.2.1.5 cinternalpropertyeinschränkung</span><span class="sxs-lookup"><span data-stu-id="64c16-1030">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="64c16-1031">Die cinternalpropertyeinschränkungs-Struktur enthält einen Eigenschafts Wert, der mit einem Vorgang abgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1031">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="64c16-1032">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1032">0</span></span>

<span data-ttu-id="64c16-1033">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1033">1</span></span>

<span data-ttu-id="64c16-1034">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1034">2</span></span>

<span data-ttu-id="64c16-1035">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1035">3</span></span>

<span data-ttu-id="64c16-1036">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1036">4</span></span>

<span data-ttu-id="64c16-1037">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1037">5</span></span>

<span data-ttu-id="64c16-1038">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1038">6</span></span>

<span data-ttu-id="64c16-1039">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1039">7</span></span>

<span data-ttu-id="64c16-1040">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1040">8</span></span>

<span data-ttu-id="64c16-1041">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1041">9</span></span>

<span data-ttu-id="64c16-1042">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1042">1</span></span><br/> <span data-ttu-id="64c16-1043">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1043">0</span></span><br/>

<span data-ttu-id="64c16-1044">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1044">1</span></span>

<span data-ttu-id="64c16-1045">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1045">2</span></span>

<span data-ttu-id="64c16-1046">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1046">3</span></span>

<span data-ttu-id="64c16-1047">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1047">4</span></span>

<span data-ttu-id="64c16-1048">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1048">5</span></span>

<span data-ttu-id="64c16-1049">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1049">6</span></span>

<span data-ttu-id="64c16-1050">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1050">7</span></span>

<span data-ttu-id="64c16-1051">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1051">8</span></span>

<span data-ttu-id="64c16-1052">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1052">9</span></span>

<span data-ttu-id="64c16-1053">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1053">2</span></span><br/> <span data-ttu-id="64c16-1054">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1054">0</span></span><br/>

<span data-ttu-id="64c16-1055">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1055">1</span></span>

<span data-ttu-id="64c16-1056">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1056">2</span></span>

<span data-ttu-id="64c16-1057">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1057">3</span></span>

<span data-ttu-id="64c16-1058">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1058">4</span></span>

<span data-ttu-id="64c16-1059">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1059">5</span></span>

<span data-ttu-id="64c16-1060">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1060">6</span></span>

<span data-ttu-id="64c16-1061">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1061">7</span></span>

<span data-ttu-id="64c16-1062">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1062">8</span></span>

<span data-ttu-id="64c16-1063">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1063">9</span></span>

<span data-ttu-id="64c16-1064">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1064">3</span></span><br/> <span data-ttu-id="64c16-1065">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1065">0</span></span><br/>

<span data-ttu-id="64c16-1066">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1066">1</span></span>

<span data-ttu-id="64c16-1067">\_RelOp</span><span class="sxs-lookup"><span data-stu-id="64c16-1067">\_relop</span></span>

<span data-ttu-id="64c16-1068">\_Lauer</span><span class="sxs-lookup"><span data-stu-id="64c16-1068">\_pid</span></span>

<span data-ttu-id="64c16-1069">\_prval (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1069">\_prval (variable)</span></span>

<span data-ttu-id="64c16-1070">restrictionpresent</span><span class="sxs-lookup"><span data-stu-id="64c16-1070">restrictionPresent</span></span>

<span data-ttu-id="64c16-1071">nextrestriction (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1071">nextRestriction (variable)</span></span>



 

<span data-ttu-id="64c16-1072">**\_ RelOp**: eine 32-Bit-Ganzzahl, die die Beziehung angibt, die für die Eigenschaft auszuführen ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-1072">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="64c16-1073">Muss einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="64c16-1073">MUST be one of the following values:</span></span>



| <span data-ttu-id="64c16-1074">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-1074">Value</span></span>                 | <span data-ttu-id="64c16-1075">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-1075">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-1076">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-1076">PRLT 0x00000000</span></span>       | <span data-ttu-id="64c16-1077">Ein kleiner-als-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="64c16-1077">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="64c16-1078">Prle 0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-1078">PRLE 0x00000001</span></span>       | <span data-ttu-id="64c16-1079">Ein kleiner-als-oder-gleich-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="64c16-1079">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="64c16-1080">Prgt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-1080">PRGT 0x00000002</span></span>       | <span data-ttu-id="64c16-1081">Ein größer-als-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="64c16-1081">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="64c16-1082">Prge 0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-1082">PRGE 0x00000003</span></span>       | <span data-ttu-id="64c16-1083">Ein größer-als-oder gleich-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="64c16-1083">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="64c16-1084">Preq 0x00000004</span><span class="sxs-lookup"><span data-stu-id="64c16-1084">PREQ 0x00000004</span></span>       | <span data-ttu-id="64c16-1085">Ein Gleichheits Vergleich.</span><span class="sxs-lookup"><span data-stu-id="64c16-1085">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="64c16-1086">Prne 0x00000005 bei der</span><span class="sxs-lookup"><span data-stu-id="64c16-1086">PRNE 0x00000005</span></span>       | <span data-ttu-id="64c16-1087">Ein nicht gleicher Vergleich.</span><span class="sxs-lookup"><span data-stu-id="64c16-1087">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="64c16-1088">Prre 0x00000006</span><span class="sxs-lookup"><span data-stu-id="64c16-1088">PRRE 0x00000006</span></span>       | <span data-ttu-id="64c16-1089">Ein Vergleich mit einem regulären Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="64c16-1089">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="64c16-1090">Prallbits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="64c16-1090">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="64c16-1091">Ein bitweises and, das den rechten Operanden zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1091">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="64c16-1092">Prsomebits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="64c16-1092">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="64c16-1093">Ein bitweises and, das einen Wert ungleich 0 (null) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1093">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="64c16-1094">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="64c16-1094">PRAll 0x00000100</span></span>      | <span data-ttu-id="64c16-1095">Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden, und ist nur true, wenn der Vorgang für alle Zeilen "true" ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-1095">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="64c16-1096">Prany 0x00000200</span><span class="sxs-lookup"><span data-stu-id="64c16-1096">PRAny 0x00000200</span></span>      | <span data-ttu-id="64c16-1097">Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden, und ist "true", wenn der Vorgang für eine beliebige Zeile "true" ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-1097">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="64c16-1098">**\_ PID**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die eigen schafts-ID darstellt (siehe PROPID im Abschnitt 2.2.1.4).</span><span class="sxs-lookup"><span data-stu-id="64c16-1098">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="64c16-1099">**\_ prval**: ein cbasestoragevariant-Objekt, das den Wert enthält, der mit der Eigenschaft verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1099">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="64c16-1100">**restrictionpresent**: Ein Bytewert, der angibt, ob das nextrestriction-Feld vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-1100">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="64c16-1101">Muss auf 0x00 oder 0x01 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1101">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="64c16-1102">Wenn der Wert auf 0x01 festgelegt ist, gibt restrictionpresent an, dass das Feld nextrestriction vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-1102">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="64c16-1103">Wenn der Wert auf 0x00 festgelegt ist, gibt restrictionpresent an, dass das Feld nextrestriction nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-1103">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="64c16-1104">**nextrestriction**: eine in Abschnitt 2.2.1.16 angegebene Struktur der Struktur, die eine weitere Einschränkung angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1104">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="64c16-1105">2.2.1.6 cnatlanguagerestriction</span><span class="sxs-lookup"><span data-stu-id="64c16-1105">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="64c16-1106">Die cnatlanguagerestriction-Struktur enthält eine **Abfrage in natürlicher Sprache** für eine Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="64c16-1106">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="64c16-1107">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1107">0</span></span>

<span data-ttu-id="64c16-1108">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1108">1</span></span>

<span data-ttu-id="64c16-1109">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1109">2</span></span>

<span data-ttu-id="64c16-1110">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1110">3</span></span>

<span data-ttu-id="64c16-1111">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1111">4</span></span>

<span data-ttu-id="64c16-1112">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1112">5</span></span>

<span data-ttu-id="64c16-1113">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1113">6</span></span>

<span data-ttu-id="64c16-1114">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1114">7</span></span>

<span data-ttu-id="64c16-1115">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1115">8</span></span>

<span data-ttu-id="64c16-1116">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1116">9</span></span>

<span data-ttu-id="64c16-1117">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1117">1</span></span><br/> <span data-ttu-id="64c16-1118">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1118">0</span></span><br/>

<span data-ttu-id="64c16-1119">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1119">1</span></span>

<span data-ttu-id="64c16-1120">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1120">2</span></span>

<span data-ttu-id="64c16-1121">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1121">3</span></span>

<span data-ttu-id="64c16-1122">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1122">4</span></span>

<span data-ttu-id="64c16-1123">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1123">5</span></span>

<span data-ttu-id="64c16-1124">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1124">6</span></span>

<span data-ttu-id="64c16-1125">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1125">7</span></span>

<span data-ttu-id="64c16-1126">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1126">8</span></span>

<span data-ttu-id="64c16-1127">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1127">9</span></span>

<span data-ttu-id="64c16-1128">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1128">2</span></span><br/> <span data-ttu-id="64c16-1129">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1129">0</span></span><br/>

<span data-ttu-id="64c16-1130">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1130">1</span></span>

<span data-ttu-id="64c16-1131">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1131">2</span></span>

<span data-ttu-id="64c16-1132">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1132">3</span></span>

<span data-ttu-id="64c16-1133">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1133">4</span></span>

<span data-ttu-id="64c16-1134">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1134">5</span></span>

<span data-ttu-id="64c16-1135">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1135">6</span></span>

<span data-ttu-id="64c16-1136">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1136">7</span></span>

<span data-ttu-id="64c16-1137">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1137">8</span></span>

<span data-ttu-id="64c16-1138">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1138">9</span></span>

<span data-ttu-id="64c16-1139">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1139">3</span></span><br/> <span data-ttu-id="64c16-1140">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1140">0</span></span><br/>

<span data-ttu-id="64c16-1141">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1141">1</span></span>

<span data-ttu-id="64c16-1142">\_Property (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1142">\_Property (variable)</span></span>

<span data-ttu-id="64c16-1143">...</span><span class="sxs-lookup"><span data-stu-id="64c16-1143">...</span></span>

<span data-ttu-id="64c16-1144">\_Auffüllung \_ CC (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1144">\_padding\_cc (variable)</span></span>

<span data-ttu-id="64c16-1145">Cc</span><span class="sxs-lookup"><span data-stu-id="64c16-1145">Cc</span></span>

<span data-ttu-id="64c16-1146">\_pwcspphrase (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1146">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="64c16-1147">...</span><span class="sxs-lookup"><span data-stu-id="64c16-1147">...</span></span>

<span data-ttu-id="64c16-1148">\_Auffüllen von \_ LCID (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1148">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="64c16-1149">Lcid</span><span class="sxs-lookup"><span data-stu-id="64c16-1149">Lcid</span></span>



 

<span data-ttu-id="64c16-1150">**\_ Property**: eine cfullpropspec-Struktur, wie im Abschnitt 2.2.1.3 angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-1150">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="64c16-1151">Dieses Feld gibt die Eigenschaft an, für die der Übereinstimmungs Vorgang durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1151">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="64c16-1152">**\_ Auffüllung \_ CC**: Dieses Feld muss zwischen 0 und 3 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-1152">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="64c16-1153">Die Länge dieses Felds muss so lauten, dass das folgende Feld bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-1153">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="64c16-1154">Wenn dieses Feld vorhanden ist (d. h. eine Länge ungleich 0 (null)), ist der enthaltene Wert beliebig.</span><span class="sxs-lookup"><span data-stu-id="64c16-1154">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="64c16-1155">Der Inhalt dieses Felds muss vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1155">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="64c16-1156">**CC**: eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1156">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="64c16-1157">Die Anzahl von Zeichen im \_ Feld "pwcspphrase".</span><span class="sxs-lookup"><span data-stu-id="64c16-1157">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="64c16-1158">**\_ pwcspphrase**: eine Unicode-Zeichenfolge, die nicht auf NULL fest steht und das Wort oder den Ausdruck darstellt, der mit der Eigenschaft verglichen werden soll</span><span class="sxs-lookup"><span data-stu-id="64c16-1158">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="64c16-1159">Darf nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-1159">MUST NOT be empty.</span></span> <span data-ttu-id="64c16-1160">Das CC-Feld enthält die Länge der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="64c16-1160">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="64c16-1161">**\_ Auffüllung \_ LCID**: Dieses Feld muss zwischen 0 und 3 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-1161">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="64c16-1162">Die Länge dieses Felds muss so lauten, dass das folgende Feld bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-1162">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="64c16-1163">Wenn dieses Feld vorhanden ist (d. h. eine Länge ungleich 0 (null)), ist der enthaltene Wert beliebig.</span><span class="sxs-lookup"><span data-stu-id="64c16-1163">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="64c16-1164">Der Inhalt dieses Felds muss vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1164">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="64c16-1165">**LCID**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Gebiets Schema der \_ pwcspphrase angibt, wie in \[ MS-GPSI \] Anhang A angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-1165">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="64c16-1166">2.2.1.7 cnoderestriction</span><span class="sxs-lookup"><span data-stu-id="64c16-1166">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="64c16-1167">Die cnoderestriction-Struktur enthält ein Array von **Befehls** Struktur Knoten, die die Einschränkungen für die Abfrage angeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-1167">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="64c16-1168">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1168">0</span></span>

<span data-ttu-id="64c16-1169">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1169">1</span></span>

<span data-ttu-id="64c16-1170">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1170">2</span></span>

<span data-ttu-id="64c16-1171">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1171">3</span></span>

<span data-ttu-id="64c16-1172">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1172">4</span></span>

<span data-ttu-id="64c16-1173">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1173">5</span></span>

<span data-ttu-id="64c16-1174">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1174">6</span></span>

<span data-ttu-id="64c16-1175">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1175">7</span></span>

<span data-ttu-id="64c16-1176">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1176">8</span></span>

<span data-ttu-id="64c16-1177">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1177">9</span></span>

<span data-ttu-id="64c16-1178">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1178">1</span></span><br/> <span data-ttu-id="64c16-1179">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1179">0</span></span><br/>

<span data-ttu-id="64c16-1180">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1180">1</span></span>

<span data-ttu-id="64c16-1181">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1181">2</span></span>

<span data-ttu-id="64c16-1182">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1182">3</span></span>

<span data-ttu-id="64c16-1183">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1183">4</span></span>

<span data-ttu-id="64c16-1184">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1184">5</span></span>

<span data-ttu-id="64c16-1185">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1185">6</span></span>

<span data-ttu-id="64c16-1186">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1186">7</span></span>

<span data-ttu-id="64c16-1187">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1187">8</span></span>

<span data-ttu-id="64c16-1188">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1188">9</span></span>

<span data-ttu-id="64c16-1189">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1189">2</span></span><br/> <span data-ttu-id="64c16-1190">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1190">0</span></span><br/>

<span data-ttu-id="64c16-1191">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1191">1</span></span>

<span data-ttu-id="64c16-1192">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1192">2</span></span>

<span data-ttu-id="64c16-1193">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1193">3</span></span>

<span data-ttu-id="64c16-1194">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1194">4</span></span>

<span data-ttu-id="64c16-1195">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1195">5</span></span>

<span data-ttu-id="64c16-1196">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1196">6</span></span>

<span data-ttu-id="64c16-1197">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1197">7</span></span>

<span data-ttu-id="64c16-1198">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1198">8</span></span>

<span data-ttu-id="64c16-1199">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1199">9</span></span>

<span data-ttu-id="64c16-1200">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1200">3</span></span><br/> <span data-ttu-id="64c16-1201">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1201">0</span></span><br/>

<span data-ttu-id="64c16-1202">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1202">1</span></span>

<span data-ttu-id="64c16-1203">\_CNode</span><span class="sxs-lookup"><span data-stu-id="64c16-1203">\_cNode</span></span>

<span data-ttu-id="64c16-1204">\_panode (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1204">\_paNode (variable)</span></span>



 

<span data-ttu-id="64c16-1205">**\_ CNode**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der im \_ panode-Feld enthaltenen ermittelungs Strukturen angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1205">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="64c16-1206">**\_ panode**: ein Array von krestriction-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1206">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="64c16-1207">Strukturen im Array müssen durch 0 bis 3 Auffüll Bytes voneinander getrennt werden, sodass jede Struktur bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die dieses Array enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-1207">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="64c16-1208">Wenn Auffüll-Bytes vorhanden sind, ist der Wert, den Sie enthalten, willkürlich.</span><span class="sxs-lookup"><span data-stu-id="64c16-1208">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="64c16-1209">Der Inhalt der Auffüll Zeichen muss vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1209">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="64c16-1210">2.2.1.8-"cockrestriction"</span><span class="sxs-lookup"><span data-stu-id="64c16-1210">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="64c16-1211">Die "cockrestriction"-Struktur enthält die Position eines Worts in einem Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="64c16-1211">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="64c16-1212">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1212">0</span></span>

<span data-ttu-id="64c16-1213">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1213">1</span></span>

<span data-ttu-id="64c16-1214">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1214">2</span></span>

<span data-ttu-id="64c16-1215">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1215">3</span></span>

<span data-ttu-id="64c16-1216">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1216">4</span></span>

<span data-ttu-id="64c16-1217">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1217">5</span></span>

<span data-ttu-id="64c16-1218">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1218">6</span></span>

<span data-ttu-id="64c16-1219">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1219">7</span></span>

<span data-ttu-id="64c16-1220">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1220">8</span></span>

<span data-ttu-id="64c16-1221">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1221">9</span></span>

<span data-ttu-id="64c16-1222">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1222">1</span></span><br/> <span data-ttu-id="64c16-1223">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1223">0</span></span><br/>

<span data-ttu-id="64c16-1224">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1224">1</span></span>

<span data-ttu-id="64c16-1225">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1225">2</span></span>

<span data-ttu-id="64c16-1226">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1226">3</span></span>

<span data-ttu-id="64c16-1227">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1227">4</span></span>

<span data-ttu-id="64c16-1228">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1228">5</span></span>

<span data-ttu-id="64c16-1229">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1229">6</span></span>

<span data-ttu-id="64c16-1230">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1230">7</span></span>

<span data-ttu-id="64c16-1231">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1231">8</span></span>

<span data-ttu-id="64c16-1232">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1232">9</span></span>

<span data-ttu-id="64c16-1233">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1233">2</span></span><br/> <span data-ttu-id="64c16-1234">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1234">0</span></span><br/>

<span data-ttu-id="64c16-1235">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1235">1</span></span>

<span data-ttu-id="64c16-1236">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1236">2</span></span>

<span data-ttu-id="64c16-1237">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1237">3</span></span>

<span data-ttu-id="64c16-1238">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1238">4</span></span>

<span data-ttu-id="64c16-1239">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1239">5</span></span>

<span data-ttu-id="64c16-1240">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1240">6</span></span>

<span data-ttu-id="64c16-1241">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1241">7</span></span>

<span data-ttu-id="64c16-1242">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1242">8</span></span>

<span data-ttu-id="64c16-1243">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1243">9</span></span>

<span data-ttu-id="64c16-1244">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1244">3</span></span><br/> <span data-ttu-id="64c16-1245">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1245">0</span></span><br/>

<span data-ttu-id="64c16-1246">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1246">1</span></span>

<span data-ttu-id="64c16-1247">\_OCC</span><span class="sxs-lookup"><span data-stu-id="64c16-1247">\_occ</span></span>

<span data-ttu-id="64c16-1248">\_cprevnoisewords</span><span class="sxs-lookup"><span data-stu-id="64c16-1248">\_cPrevNoiseWords</span></span>

<span data-ttu-id="64c16-1249">\_cnextnoisewords</span><span class="sxs-lookup"><span data-stu-id="64c16-1249">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="64c16-1250">**\_ OCC**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Offset des Worts in einer Abfrage Zeichenfolge in Einheiten von Wörtern angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1250">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="64c16-1251">Ein in dieser Spezifikation verwendetes Wort ist eine Einheit der Sprache in jedem Gebiets Schema, das eine Bedeutung hat.</span><span class="sxs-lookup"><span data-stu-id="64c16-1251">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="64c16-1252">**\_ cprevnoisewords**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von Füll **Wörtern** enthält, die zwischen diesem Wort und dem vorherigen Wort im Ausdruck auftreten.</span><span class="sxs-lookup"><span data-stu-id="64c16-1252">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="64c16-1253">**\_ cnextnoisewords**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von Füll Wörtern enthält, die zwischen diesem Wort und dem nächsten Wort im Ausdruck auftreten.</span><span class="sxs-lookup"><span data-stu-id="64c16-1253">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="64c16-1254">2.2.1.9 cpropertyeinschränkung</span><span class="sxs-lookup"><span data-stu-id="64c16-1254">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="64c16-1255">Die cpropertyeinschränkungs-Struktur enthält einen Eigenschafts Wert, der mit einem Vorgang verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1255">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="64c16-1256">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1256">0</span></span>

<span data-ttu-id="64c16-1257">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1257">1</span></span>

<span data-ttu-id="64c16-1258">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1258">2</span></span>

<span data-ttu-id="64c16-1259">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1259">3</span></span>

<span data-ttu-id="64c16-1260">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1260">4</span></span>

<span data-ttu-id="64c16-1261">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1261">5</span></span>

<span data-ttu-id="64c16-1262">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1262">6</span></span>

<span data-ttu-id="64c16-1263">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1263">7</span></span>

<span data-ttu-id="64c16-1264">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1264">8</span></span>

<span data-ttu-id="64c16-1265">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1265">9</span></span>

<span data-ttu-id="64c16-1266">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1266">1</span></span><br/> <span data-ttu-id="64c16-1267">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1267">0</span></span><br/>

<span data-ttu-id="64c16-1268">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1268">1</span></span>

<span data-ttu-id="64c16-1269">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1269">2</span></span>

<span data-ttu-id="64c16-1270">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1270">3</span></span>

<span data-ttu-id="64c16-1271">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1271">4</span></span>

<span data-ttu-id="64c16-1272">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1272">5</span></span>

<span data-ttu-id="64c16-1273">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1273">6</span></span>

<span data-ttu-id="64c16-1274">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1274">7</span></span>

<span data-ttu-id="64c16-1275">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1275">8</span></span>

<span data-ttu-id="64c16-1276">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1276">9</span></span>

<span data-ttu-id="64c16-1277">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1277">2</span></span><br/> <span data-ttu-id="64c16-1278">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1278">0</span></span><br/>

<span data-ttu-id="64c16-1279">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1279">1</span></span>

<span data-ttu-id="64c16-1280">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1280">2</span></span>

<span data-ttu-id="64c16-1281">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1281">3</span></span>

<span data-ttu-id="64c16-1282">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1282">4</span></span>

<span data-ttu-id="64c16-1283">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1283">5</span></span>

<span data-ttu-id="64c16-1284">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1284">6</span></span>

<span data-ttu-id="64c16-1285">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1285">7</span></span>

<span data-ttu-id="64c16-1286">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1286">8</span></span>

<span data-ttu-id="64c16-1287">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1287">9</span></span>

<span data-ttu-id="64c16-1288">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1288">3</span></span><br/> <span data-ttu-id="64c16-1289">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1289">0</span></span><br/>

<span data-ttu-id="64c16-1290">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1290">1</span></span>

<span data-ttu-id="64c16-1291">\_RelOp</span><span class="sxs-lookup"><span data-stu-id="64c16-1291">\_relop</span></span>

<span data-ttu-id="64c16-1292">\_Property (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1292">\_Property (variable)</span></span>

<span data-ttu-id="64c16-1293">\_prval (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1293">\_prval (variable)</span></span>



 

<span data-ttu-id="64c16-1294">**\_ RelOp**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Beziehung angibt, die für die Eigenschaft durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1294">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="64c16-1295">Muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1295">MUST be one of the following values.</span></span>



| <span data-ttu-id="64c16-1296">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-1296">Value</span></span>                 | <span data-ttu-id="64c16-1297">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-1297">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-1298">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-1298">PRLT 0x00000000</span></span>       | <span data-ttu-id="64c16-1299">Ein kleiner-als-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="64c16-1299">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="64c16-1300">Prle 0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-1300">PRLE 0x00000001</span></span>       | <span data-ttu-id="64c16-1301">Ein kleiner-als-oder-gleich-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="64c16-1301">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="64c16-1302">Prgt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-1302">PRGT 0x00000002</span></span>       | <span data-ttu-id="64c16-1303">Ein größer-als-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="64c16-1303">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="64c16-1304">Prge 0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-1304">PRGE 0x00000003</span></span>       | <span data-ttu-id="64c16-1305">Ein größer-als-oder gleich-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="64c16-1305">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="64c16-1306">Preq 0x00000004</span><span class="sxs-lookup"><span data-stu-id="64c16-1306">PREQ 0x00000004</span></span>       | <span data-ttu-id="64c16-1307">Ein Gleichheits Vergleich.</span><span class="sxs-lookup"><span data-stu-id="64c16-1307">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="64c16-1308">Prne 0x00000005 bei der</span><span class="sxs-lookup"><span data-stu-id="64c16-1308">PRNE 0x00000005</span></span>       | <span data-ttu-id="64c16-1309">Ein nicht gleicher Vergleich.</span><span class="sxs-lookup"><span data-stu-id="64c16-1309">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="64c16-1310">Prre 0x00000006</span><span class="sxs-lookup"><span data-stu-id="64c16-1310">PRRE 0x00000006</span></span>       | <span data-ttu-id="64c16-1311">Ein Vergleich mit einem regulären Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="64c16-1311">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="64c16-1312">Prallbits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="64c16-1312">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="64c16-1313">Ein bitweises and, das den rechten Operanden zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1313">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="64c16-1314">Prsomebits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="64c16-1314">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="64c16-1315">Ein bitweises and, das einen Wert ungleich 0 (null) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1315">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="64c16-1316">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="64c16-1316">PRAll 0x00000100</span></span>      | <span data-ttu-id="64c16-1317">Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden, und ist nur true, wenn der Vorgang für alle Zeilen "true" ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-1317">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="64c16-1318">Prany 0x00000200</span><span class="sxs-lookup"><span data-stu-id="64c16-1318">PRAny 0x00000200</span></span>      | <span data-ttu-id="64c16-1319">Der Vorgang muss für eine Spalte eines Rowsets ausgeführt werden, und ist "true", wenn der Vorgang für eine beliebige Zeile "true" ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-1319">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="64c16-1320">**\_ Property**: eine cfullpropspec-Struktur, wie in Abschnitt 2.2.1.2 angegeben, gibt die Eigenschaft an, für die ein Übereinstimmungs Vorgang durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1320">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="64c16-1321">**\_ prval**: eine cbasestoragevariant-Struktur, wie im Abschnitt 2.2.1.1 angegeben, die den Wert enthält, der mit der Eigenschaft verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1321">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="64c16-1322">2.2.1.10 crangerestriction</span><span class="sxs-lookup"><span data-stu-id="64c16-1322">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="64c16-1323">Die crangerestriction-Struktur enthält eine Einschränkung für einen Wertebereich.</span><span class="sxs-lookup"><span data-stu-id="64c16-1323">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="64c16-1324">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1324">0</span></span>

<span data-ttu-id="64c16-1325">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1325">1</span></span>

<span data-ttu-id="64c16-1326">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1326">2</span></span>

<span data-ttu-id="64c16-1327">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1327">3</span></span>

<span data-ttu-id="64c16-1328">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1328">4</span></span>

<span data-ttu-id="64c16-1329">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1329">5</span></span>

<span data-ttu-id="64c16-1330">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1330">6</span></span>

<span data-ttu-id="64c16-1331">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1331">7</span></span>

<span data-ttu-id="64c16-1332">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1332">8</span></span>

<span data-ttu-id="64c16-1333">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1333">9</span></span>

<span data-ttu-id="64c16-1334">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1334">1</span></span><br/> <span data-ttu-id="64c16-1335">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1335">0</span></span><br/>

<span data-ttu-id="64c16-1336">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1336">1</span></span>

<span data-ttu-id="64c16-1337">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1337">2</span></span>

<span data-ttu-id="64c16-1338">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1338">3</span></span>

<span data-ttu-id="64c16-1339">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1339">4</span></span>

<span data-ttu-id="64c16-1340">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1340">5</span></span>

<span data-ttu-id="64c16-1341">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1341">6</span></span>

<span data-ttu-id="64c16-1342">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1342">7</span></span>

<span data-ttu-id="64c16-1343">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1343">8</span></span>

<span data-ttu-id="64c16-1344">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1344">9</span></span>

<span data-ttu-id="64c16-1345">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1345">2</span></span><br/> <span data-ttu-id="64c16-1346">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1346">0</span></span><br/>

<span data-ttu-id="64c16-1347">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1347">1</span></span>

<span data-ttu-id="64c16-1348">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1348">2</span></span>

<span data-ttu-id="64c16-1349">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1349">3</span></span>

<span data-ttu-id="64c16-1350">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1350">4</span></span>

<span data-ttu-id="64c16-1351">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1351">5</span></span>

<span data-ttu-id="64c16-1352">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1352">6</span></span>

<span data-ttu-id="64c16-1353">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1353">7</span></span>

<span data-ttu-id="64c16-1354">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1354">8</span></span>

<span data-ttu-id="64c16-1355">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1355">9</span></span>

<span data-ttu-id="64c16-1356">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1356">3</span></span><br/> <span data-ttu-id="64c16-1357">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1357">0</span></span><br/>

<span data-ttu-id="64c16-1358">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1358">1</span></span>

<span data-ttu-id="64c16-1359">\_keystart (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1359">\_keyStart (variable)</span></span>

<span data-ttu-id="64c16-1360">\_keyend (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1360">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="64c16-1361">**\_ keystart**: eine CKey-Struktur, wie in Abschnitt 2.2.1.4 angegeben, die den Anfang des Bereichs enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-1361">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="64c16-1362">**\_ keyend**: eine CKey-Struktur, die das Ende des Bereichs enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-1362">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="64c16-1363">2.2.1.11 cscoperestriction</span><span class="sxs-lookup"><span data-stu-id="64c16-1363">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="64c16-1364">Die cscoperestriction-Struktur enthält eine Einschränkung der Dateien, die durchsucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1364">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="64c16-1365">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1365">0</span></span>

<span data-ttu-id="64c16-1366">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1366">1</span></span>

<span data-ttu-id="64c16-1367">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1367">2</span></span>

<span data-ttu-id="64c16-1368">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1368">3</span></span>

<span data-ttu-id="64c16-1369">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1369">4</span></span>

<span data-ttu-id="64c16-1370">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1370">5</span></span>

<span data-ttu-id="64c16-1371">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1371">6</span></span>

<span data-ttu-id="64c16-1372">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1372">7</span></span>

<span data-ttu-id="64c16-1373">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1373">8</span></span>

<span data-ttu-id="64c16-1374">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1374">9</span></span>

<span data-ttu-id="64c16-1375">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1375">1</span></span><br/> <span data-ttu-id="64c16-1376">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1376">0</span></span><br/>

<span data-ttu-id="64c16-1377">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1377">1</span></span>

<span data-ttu-id="64c16-1378">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1378">2</span></span>

<span data-ttu-id="64c16-1379">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1379">3</span></span>

<span data-ttu-id="64c16-1380">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1380">4</span></span>

<span data-ttu-id="64c16-1381">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1381">5</span></span>

<span data-ttu-id="64c16-1382">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1382">6</span></span>

<span data-ttu-id="64c16-1383">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1383">7</span></span>

<span data-ttu-id="64c16-1384">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1384">8</span></span>

<span data-ttu-id="64c16-1385">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1385">9</span></span>

<span data-ttu-id="64c16-1386">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1386">2</span></span><br/> <span data-ttu-id="64c16-1387">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1387">0</span></span><br/>

<span data-ttu-id="64c16-1388">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1388">1</span></span>

<span data-ttu-id="64c16-1389">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1389">2</span></span>

<span data-ttu-id="64c16-1390">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1390">3</span></span>

<span data-ttu-id="64c16-1391">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1391">4</span></span>

<span data-ttu-id="64c16-1392">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1392">5</span></span>

<span data-ttu-id="64c16-1393">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1393">6</span></span>

<span data-ttu-id="64c16-1394">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1394">7</span></span>

<span data-ttu-id="64c16-1395">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1395">8</span></span>

<span data-ttu-id="64c16-1396">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1396">9</span></span>

<span data-ttu-id="64c16-1397">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1397">3</span></span><br/> <span data-ttu-id="64c16-1398">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1398">0</span></span><br/>

<span data-ttu-id="64c16-1399">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1399">1</span></span>

<span data-ttu-id="64c16-1400">Cclowerpath</span><span class="sxs-lookup"><span data-stu-id="64c16-1400">CcLowerPath</span></span>

<span data-ttu-id="64c16-1401">\_lowerpath (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1401">\_lowerPath (variable)</span></span>

<span data-ttu-id="64c16-1402">...</span><span class="sxs-lookup"><span data-stu-id="64c16-1402">...</span></span>

<span data-ttu-id="64c16-1403">\_Auffüll Zeichen (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1403">\_padding ( variable)</span></span>

<span data-ttu-id="64c16-1404">\_Füll</span><span class="sxs-lookup"><span data-stu-id="64c16-1404">\_length</span></span>

<span data-ttu-id="64c16-1405">\_"f"</span><span class="sxs-lookup"><span data-stu-id="64c16-1405">\_fRecursive</span></span>

<span data-ttu-id="64c16-1406">\_virtueller</span><span class="sxs-lookup"><span data-stu-id="64c16-1406">\_fVirtual</span></span>



 

<span data-ttu-id="64c16-1407">**Cclowerpath**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von Unicode-Zeichen im \_ Feld "lowerpath" enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-1407">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="64c16-1408">**\_ lowerpath**: eine Unicode-Zeichenfolge ohne NULL-terminierte Unicode-Zeichenfolge, die den **Pfad** darstellt, auf den die Abfrage beschränkt</span><span class="sxs-lookup"><span data-stu-id="64c16-1408">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="64c16-1409">Das cclowerpath-Feld enthält die Länge der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="64c16-1409">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="64c16-1410">**\_ Auffüllung**: Dieses Feld muss zwischen 0 und 3 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-1410">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="64c16-1411">Die Länge dieses Felds muss so lauten, dass das folgende Feld bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-1411">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="64c16-1412">Wenn dieses Feld vorhanden ist (d. h. eine Länge ungleich 0 (null)), ist der enthaltene Wert beliebig.</span><span class="sxs-lookup"><span data-stu-id="64c16-1412">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="64c16-1413">Der Inhalt dieses Felds muss vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1413">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="64c16-1414">**\_ length**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge von ' \_ lowerpath ' in Unicode-Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-1414">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="64c16-1415">Dieser Wert muss mit dem Wert von cclowerpath identisch sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-1415">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="64c16-1416">**\_ f rekursive**: eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1416">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="64c16-1417">Muss auf 0x00000001 oder 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1417">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="64c16-1418">Bei der Einstellung 0x00000001 muss der Server rekursiv alle Unterverzeichnisse des Pfads überprüfen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1418">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="64c16-1419">Wenn der Server auf 0x00000000 festgelegt ist, kann er keine Unterverzeichnisse untersuchen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1419">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="64c16-1420">" **\_ f Virtual**": eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1420">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="64c16-1421">Muss auf 0x00000001 oder 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1421">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="64c16-1422">Wenn der Wert auf 0x00000001 festgelegt \_ ist, handelt es sich bei lowerpath um einen virtuellen Pfad (die Uniform Resource Locator (URL), die einem physischen Verzeichnis im Dateisystem zugeordnet ist) für eine Website.</span><span class="sxs-lookup"><span data-stu-id="64c16-1422">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="64c16-1423">Wenn der Wert auf 0x00000000 festgelegt ist, \_ ist lowerpath ein Dateisystempfad.</span><span class="sxs-lookup"><span data-stu-id="64c16-1423">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="64c16-1424">2.2.1.12 csort</span><span class="sxs-lookup"><span data-stu-id="64c16-1424">2.2.1.12 CSort</span></span>

<span data-ttu-id="64c16-1425">Die csort-Struktur identifiziert eine zu sortierende Spalte.</span><span class="sxs-lookup"><span data-stu-id="64c16-1425">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="64c16-1426">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1426">0</span></span>

<span data-ttu-id="64c16-1427">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1427">1</span></span>

<span data-ttu-id="64c16-1428">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1428">2</span></span>

<span data-ttu-id="64c16-1429">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1429">3</span></span>

<span data-ttu-id="64c16-1430">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1430">4</span></span>

<span data-ttu-id="64c16-1431">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1431">5</span></span>

<span data-ttu-id="64c16-1432">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1432">6</span></span>

<span data-ttu-id="64c16-1433">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1433">7</span></span>

<span data-ttu-id="64c16-1434">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1434">8</span></span>

<span data-ttu-id="64c16-1435">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1435">9</span></span>

<span data-ttu-id="64c16-1436">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1436">1</span></span><br/> <span data-ttu-id="64c16-1437">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1437">0</span></span><br/>

<span data-ttu-id="64c16-1438">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1438">1</span></span>

<span data-ttu-id="64c16-1439">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1439">2</span></span>

<span data-ttu-id="64c16-1440">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1440">3</span></span>

<span data-ttu-id="64c16-1441">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1441">4</span></span>

<span data-ttu-id="64c16-1442">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1442">5</span></span>

<span data-ttu-id="64c16-1443">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1443">6</span></span>

<span data-ttu-id="64c16-1444">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1444">7</span></span>

<span data-ttu-id="64c16-1445">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1445">8</span></span>

<span data-ttu-id="64c16-1446">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1446">9</span></span>

<span data-ttu-id="64c16-1447">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1447">2</span></span><br/> <span data-ttu-id="64c16-1448">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1448">0</span></span><br/>

<span data-ttu-id="64c16-1449">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1449">1</span></span>

<span data-ttu-id="64c16-1450">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1450">2</span></span>

<span data-ttu-id="64c16-1451">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1451">3</span></span>

<span data-ttu-id="64c16-1452">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1452">4</span></span>

<span data-ttu-id="64c16-1453">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1453">5</span></span>

<span data-ttu-id="64c16-1454">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1454">6</span></span>

<span data-ttu-id="64c16-1455">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1455">7</span></span>

<span data-ttu-id="64c16-1456">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1456">8</span></span>

<span data-ttu-id="64c16-1457">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1457">9</span></span>

<span data-ttu-id="64c16-1458">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1458">3</span></span><br/> <span data-ttu-id="64c16-1459">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1459">0</span></span><br/>

<span data-ttu-id="64c16-1460">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1460">1</span></span>

<span data-ttu-id="64c16-1461">pidcolumn</span><span class="sxs-lookup"><span data-stu-id="64c16-1461">pidColumn</span></span>

<span data-ttu-id="64c16-1462">dworder</span><span class="sxs-lookup"><span data-stu-id="64c16-1462">dwOrder</span></span>

<span data-ttu-id="64c16-1463">locale</span><span class="sxs-lookup"><span data-stu-id="64c16-1463">locale</span></span>



 

<span data-ttu-id="64c16-1464">**pidcolumn**: eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1464">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="64c16-1465">Die Nummer der Spalte, nach der sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1465">The number of the column to sort by.</span></span>

<span data-ttu-id="64c16-1466">**dworder**: eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1466">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="64c16-1467">Muss einer der folgenden Werte sein, wobei angegeben wird, wie basierend auf der Spalte sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1467">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="64c16-1468">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-1468">Value</span></span>                        | <span data-ttu-id="64c16-1469">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-1469">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-1470">Abfrage \_ sortascend 0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-1470">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="64c16-1471">Die Zeilen müssen in aufsteigender Reihenfolge nach den Werten in der angegebenen Spalte sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1471">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="64c16-1472">Abfrage absteigend \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-1472">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="64c16-1473">Die Zeilen müssen auf der Grundlage der Werte in der angegebenen Spalte in absteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1473">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="64c16-1474">**locale**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Gebiets Schema angibt, das in \[ MS-GPSI \] Anhang A der Spalte angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-1474">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="64c16-1475">2.2.1.13 csyneinschränkung</span><span class="sxs-lookup"><span data-stu-id="64c16-1475">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="64c16-1476">Die csyneinschränkungs-Struktur enthält ein Wort oder seine Synonyme für einen Abfrage Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="64c16-1476">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="64c16-1477">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1477">0</span></span>

<span data-ttu-id="64c16-1478">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1478">1</span></span>

<span data-ttu-id="64c16-1479">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1479">2</span></span>

<span data-ttu-id="64c16-1480">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1480">3</span></span>

<span data-ttu-id="64c16-1481">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1481">4</span></span>

<span data-ttu-id="64c16-1482">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1482">5</span></span>

<span data-ttu-id="64c16-1483">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1483">6</span></span>

<span data-ttu-id="64c16-1484">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1484">7</span></span>

<span data-ttu-id="64c16-1485">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1485">8</span></span>

<span data-ttu-id="64c16-1486">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1486">9</span></span>

<span data-ttu-id="64c16-1487">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1487">1</span></span><br/> <span data-ttu-id="64c16-1488">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1488">0</span></span><br/>

<span data-ttu-id="64c16-1489">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1489">1</span></span>

<span data-ttu-id="64c16-1490">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1490">2</span></span>

<span data-ttu-id="64c16-1491">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1491">3</span></span>

<span data-ttu-id="64c16-1492">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1492">4</span></span>

<span data-ttu-id="64c16-1493">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1493">5</span></span>

<span data-ttu-id="64c16-1494">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1494">6</span></span>

<span data-ttu-id="64c16-1495">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1495">7</span></span>

<span data-ttu-id="64c16-1496">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1496">8</span></span>

<span data-ttu-id="64c16-1497">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1497">9</span></span>

<span data-ttu-id="64c16-1498">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1498">2</span></span><br/> <span data-ttu-id="64c16-1499">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1499">0</span></span><br/>

<span data-ttu-id="64c16-1500">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1500">1</span></span>

<span data-ttu-id="64c16-1501">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1501">2</span></span>

<span data-ttu-id="64c16-1502">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1502">3</span></span>

<span data-ttu-id="64c16-1503">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1503">4</span></span>

<span data-ttu-id="64c16-1504">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1504">5</span></span>

<span data-ttu-id="64c16-1505">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1505">6</span></span>

<span data-ttu-id="64c16-1506">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1506">7</span></span>

<span data-ttu-id="64c16-1507">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1507">8</span></span>

<span data-ttu-id="64c16-1508">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1508">9</span></span>

<span data-ttu-id="64c16-1509">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1509">3</span></span><br/> <span data-ttu-id="64c16-1510">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1510">0</span></span><br/>

<span data-ttu-id="64c16-1511">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1511">1</span></span>

<span data-ttu-id="64c16-1512">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="64c16-1512">Restriction</span></span>

<span data-ttu-id="64c16-1513">...</span><span class="sxs-lookup"><span data-stu-id="64c16-1513">...</span></span>

<span data-ttu-id="64c16-1514">...</span><span class="sxs-lookup"><span data-stu-id="64c16-1514">...</span></span>

<span data-ttu-id="64c16-1515">ck</span><span class="sxs-lookup"><span data-stu-id="64c16-1515">cKey</span></span>

<span data-ttu-id="64c16-1516">\_keyarray (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1516">\_keyArray (variable)</span></span>

<span data-ttu-id="64c16-1517">\_IsRange</span><span class="sxs-lookup"><span data-stu-id="64c16-1517">\_isRange</span></span>



 

<span data-ttu-id="64c16-1518">**Einschränkung**: eine cockrestriction-Struktur, die die Position des Worts angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1518">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="64c16-1519">**ckey**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im \_ keyarray-Array angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1519">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="64c16-1520">**\_ keyarray**: ein Array von CKey-Strukturen, das ein Wort und seine Synonyme angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1520">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="64c16-1521">**\_ IsRange**: bei Festlegung auf 0x01 sind die Schlüssel Präfixe, die abgeglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1521">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="64c16-1522">Wenn der Wert auf 0x00 festgelegt ist, sind die Schlüssel genaue Werte für den Abgleich.</span><span class="sxs-lookup"><span data-stu-id="64c16-1522">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="64c16-1523">\_"IsRange" darf nicht auf andere Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1523">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="64c16-1524">2.2.1.14 cvectoreinschränkung</span><span class="sxs-lookup"><span data-stu-id="64c16-1524">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="64c16-1525">Die cvectoreinschränkungs-Struktur enthält eine gewichtete OR-Operation für einen Befehlsstruktur Knoten.</span><span class="sxs-lookup"><span data-stu-id="64c16-1525">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="64c16-1526">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1526">0</span></span>

<span data-ttu-id="64c16-1527">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1527">1</span></span>

<span data-ttu-id="64c16-1528">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1528">2</span></span>

<span data-ttu-id="64c16-1529">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1529">3</span></span>

<span data-ttu-id="64c16-1530">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1530">4</span></span>

<span data-ttu-id="64c16-1531">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1531">5</span></span>

<span data-ttu-id="64c16-1532">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1532">6</span></span>

<span data-ttu-id="64c16-1533">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1533">7</span></span>

<span data-ttu-id="64c16-1534">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1534">8</span></span>

<span data-ttu-id="64c16-1535">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1535">9</span></span>

<span data-ttu-id="64c16-1536">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1536">1</span></span><br/> <span data-ttu-id="64c16-1537">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1537">0</span></span><br/>

<span data-ttu-id="64c16-1538">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1538">1</span></span>

<span data-ttu-id="64c16-1539">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1539">2</span></span>

<span data-ttu-id="64c16-1540">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1540">3</span></span>

<span data-ttu-id="64c16-1541">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1541">4</span></span>

<span data-ttu-id="64c16-1542">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1542">5</span></span>

<span data-ttu-id="64c16-1543">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1543">6</span></span>

<span data-ttu-id="64c16-1544">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1544">7</span></span>

<span data-ttu-id="64c16-1545">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1545">8</span></span>

<span data-ttu-id="64c16-1546">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1546">9</span></span>

<span data-ttu-id="64c16-1547">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1547">2</span></span><br/> <span data-ttu-id="64c16-1548">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1548">0</span></span><br/>

<span data-ttu-id="64c16-1549">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1549">1</span></span>

<span data-ttu-id="64c16-1550">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1550">2</span></span>

<span data-ttu-id="64c16-1551">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1551">3</span></span>

<span data-ttu-id="64c16-1552">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1552">4</span></span>

<span data-ttu-id="64c16-1553">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1553">5</span></span>

<span data-ttu-id="64c16-1554">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1554">6</span></span>

<span data-ttu-id="64c16-1555">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1555">7</span></span>

<span data-ttu-id="64c16-1556">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1556">8</span></span>

<span data-ttu-id="64c16-1557">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1557">9</span></span>

<span data-ttu-id="64c16-1558">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1558">3</span></span><br/> <span data-ttu-id="64c16-1559">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1559">0</span></span><br/>

<span data-ttu-id="64c16-1560">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1560">1</span></span>

<span data-ttu-id="64c16-1561">\_Pres (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1561">\_pres (variable)</span></span>

<span data-ttu-id="64c16-1562">...</span><span class="sxs-lookup"><span data-stu-id="64c16-1562">...</span></span>

<span data-ttu-id="64c16-1563">\_Auffüll Zeichen (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1563">\_padding (variable)</span></span>

<span data-ttu-id="64c16-1564">\_ulrankmethod</span><span class="sxs-lookup"><span data-stu-id="64c16-1564">\_ulRankMethod</span></span>



 

<span data-ttu-id="64c16-1565">**\_ Pres**: eine cnoderestriction-Befehlsstruktur, auf der ein Rang oder ein Vorgang ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1565">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="64c16-1566">**\_ Auffüllung**: Dieses Feld muss zwischen 0 und 3 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-1566">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="64c16-1567">Die Länge dieses Felds muss so lauten, dass das folgende Feld bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-1567">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="64c16-1568">Wenn dieses Feld vorhanden ist (d. h. eine Länge ungleich 0 (null)), ist der enthaltene Wert beliebig.</span><span class="sxs-lookup"><span data-stu-id="64c16-1568">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="64c16-1569">Der Inhalt dieses Felds muss vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1569">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="64c16-1570">**\_ ulrankmethod**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die einen Rang Folge Algorithmus angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1570">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="64c16-1571">Muss auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1571">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="64c16-1572">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-1572">Value</span></span>                            | <span data-ttu-id="64c16-1573">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-1573">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="64c16-1574">Vektor \_ Rang \_ Min 0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-1574">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="64c16-1575">Verwenden Sie den minimalen \[ Salton-Algorithmus \] .</span><span class="sxs-lookup"><span data-stu-id="64c16-1575">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="64c16-1576">Vektor \_ Rang \_ Max 0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-1576">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="64c16-1577">Verwenden Sie den maximalen Algorithmus \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="64c16-1577">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="64c16-1578">Vektor \_ Rang \_ innere 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-1578">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="64c16-1579">Verwenden Sie den inneren Produkt Algorithmus \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="64c16-1579">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="64c16-1580">Vektor \_ Rang \_ Würfel 0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-1580">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="64c16-1581">Verwenden Sie den Würfel Koeffizient-Algorithmus \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="64c16-1581">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="64c16-1582">Vektor \_ Rang \_ Jaccard 0x00000004</span><span class="sxs-lookup"><span data-stu-id="64c16-1582">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="64c16-1583">Verwenden Sie den Jaccard-Koeffizienten-Algorithmus \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="64c16-1583">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="64c16-1584">2.2.1.15 cwordrestriction</span><span class="sxs-lookup"><span data-stu-id="64c16-1584">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="64c16-1585">Die cwordrestriction-Struktur enthält ein Wort für einen Abfrage Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="64c16-1585">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="64c16-1586">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1586">0</span></span>

<span data-ttu-id="64c16-1587">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1587">1</span></span>

<span data-ttu-id="64c16-1588">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1588">2</span></span>

<span data-ttu-id="64c16-1589">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1589">3</span></span>

<span data-ttu-id="64c16-1590">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1590">4</span></span>

<span data-ttu-id="64c16-1591">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1591">5</span></span>

<span data-ttu-id="64c16-1592">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1592">6</span></span>

<span data-ttu-id="64c16-1593">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1593">7</span></span>

<span data-ttu-id="64c16-1594">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1594">8</span></span>

<span data-ttu-id="64c16-1595">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1595">9</span></span>

<span data-ttu-id="64c16-1596">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1596">1</span></span><br/> <span data-ttu-id="64c16-1597">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1597">0</span></span><br/>

<span data-ttu-id="64c16-1598">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1598">1</span></span>

<span data-ttu-id="64c16-1599">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1599">2</span></span>

<span data-ttu-id="64c16-1600">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1600">3</span></span>

<span data-ttu-id="64c16-1601">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1601">4</span></span>

<span data-ttu-id="64c16-1602">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1602">5</span></span>

<span data-ttu-id="64c16-1603">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1603">6</span></span>

<span data-ttu-id="64c16-1604">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1604">7</span></span>

<span data-ttu-id="64c16-1605">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1605">8</span></span>

<span data-ttu-id="64c16-1606">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1606">9</span></span>

<span data-ttu-id="64c16-1607">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1607">2</span></span><br/> <span data-ttu-id="64c16-1608">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1608">0</span></span><br/>

<span data-ttu-id="64c16-1609">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1609">1</span></span>

<span data-ttu-id="64c16-1610">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1610">2</span></span>

<span data-ttu-id="64c16-1611">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1611">3</span></span>

<span data-ttu-id="64c16-1612">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1612">4</span></span>

<span data-ttu-id="64c16-1613">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1613">5</span></span>

<span data-ttu-id="64c16-1614">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1614">6</span></span>

<span data-ttu-id="64c16-1615">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1615">7</span></span>

<span data-ttu-id="64c16-1616">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1616">8</span></span>

<span data-ttu-id="64c16-1617">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1617">9</span></span>

<span data-ttu-id="64c16-1618">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1618">3</span></span><br/> <span data-ttu-id="64c16-1619">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1619">0</span></span><br/>

<span data-ttu-id="64c16-1620">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1620">1</span></span>

<span data-ttu-id="64c16-1621">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="64c16-1621">restriction</span></span>

<span data-ttu-id="64c16-1622">...</span><span class="sxs-lookup"><span data-stu-id="64c16-1622">...</span></span>

<span data-ttu-id="64c16-1623">...</span><span class="sxs-lookup"><span data-stu-id="64c16-1623">...</span></span>

<span data-ttu-id="64c16-1624">\_Schlüssel (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1624">\_key (variable)</span></span>

<span data-ttu-id="64c16-1625">\_IsRange</span><span class="sxs-lookup"><span data-stu-id="64c16-1625">\_isRange</span></span>



 

<span data-ttu-id="64c16-1626">**Einschränkung**: eine cockrestriction-Struktur, die die Position des Worts angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1626">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="64c16-1627">**\_ Key**: eine CKey-Struktur, die ein Wort angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1627">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="64c16-1628">**\_ IsRange**: bei Festlegung auf 0x01 ist der Schlüssel ein Präfix, das abgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1628">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="64c16-1629">Wenn der Wert auf 0x00 festgelegt ist, ist der Schlüssel ein genauer Wert, der gefunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1629">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="64c16-1630">\_"IsRange" darf nicht auf einen anderen Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1630">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="64c16-1631">2.2.1.16-Bindung</span><span class="sxs-lookup"><span data-stu-id="64c16-1631">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="64c16-1632">Die Struktur mit dem Aufstrich enthält einen Knoten einer Abfrage Befehlsstruktur.</span><span class="sxs-lookup"><span data-stu-id="64c16-1632">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="64c16-1633">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1633">0</span></span>

<span data-ttu-id="64c16-1634">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1634">1</span></span>

<span data-ttu-id="64c16-1635">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1635">2</span></span>

<span data-ttu-id="64c16-1636">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1636">3</span></span>

<span data-ttu-id="64c16-1637">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1637">4</span></span>

<span data-ttu-id="64c16-1638">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1638">5</span></span>

<span data-ttu-id="64c16-1639">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1639">6</span></span>

<span data-ttu-id="64c16-1640">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1640">7</span></span>

<span data-ttu-id="64c16-1641">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1641">8</span></span>

<span data-ttu-id="64c16-1642">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1642">9</span></span>

<span data-ttu-id="64c16-1643">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1643">1</span></span><br/> <span data-ttu-id="64c16-1644">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1644">0</span></span><br/>

<span data-ttu-id="64c16-1645">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1645">1</span></span>

<span data-ttu-id="64c16-1646">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1646">2</span></span>

<span data-ttu-id="64c16-1647">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1647">3</span></span>

<span data-ttu-id="64c16-1648">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1648">4</span></span>

<span data-ttu-id="64c16-1649">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1649">5</span></span>

<span data-ttu-id="64c16-1650">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1650">6</span></span>

<span data-ttu-id="64c16-1651">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1651">7</span></span>

<span data-ttu-id="64c16-1652">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1652">8</span></span>

<span data-ttu-id="64c16-1653">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1653">9</span></span>

<span data-ttu-id="64c16-1654">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1654">2</span></span><br/> <span data-ttu-id="64c16-1655">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1655">0</span></span><br/>

<span data-ttu-id="64c16-1656">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1656">1</span></span>

<span data-ttu-id="64c16-1657">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1657">2</span></span>

<span data-ttu-id="64c16-1658">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1658">3</span></span>

<span data-ttu-id="64c16-1659">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1659">4</span></span>

<span data-ttu-id="64c16-1660">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1660">5</span></span>

<span data-ttu-id="64c16-1661">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1661">6</span></span>

<span data-ttu-id="64c16-1662">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1662">7</span></span>

<span data-ttu-id="64c16-1663">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1663">8</span></span>

<span data-ttu-id="64c16-1664">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1664">9</span></span>

<span data-ttu-id="64c16-1665">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1665">3</span></span><br/> <span data-ttu-id="64c16-1666">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1666">0</span></span><br/>

<span data-ttu-id="64c16-1667">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1667">1</span></span>

<span data-ttu-id="64c16-1668">\_ultype</span><span class="sxs-lookup"><span data-stu-id="64c16-1668">\_ulType</span></span>

<span data-ttu-id="64c16-1669">Weight</span><span class="sxs-lookup"><span data-stu-id="64c16-1669">Weight</span></span>

<span data-ttu-id="64c16-1670">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="64c16-1670">Restriction</span></span>



 

<span data-ttu-id="64c16-1671">**\_ ultype**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die den für den Befehlsstruktur Knoten verwendeten Einschränkungstyp angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1671">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="64c16-1672">Muss auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1672">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="64c16-1673">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-1673">Value</span></span>                    | <span data-ttu-id="64c16-1674">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-1674">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-1675">Rtnone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-1675">RTNone 0x00000000</span></span>        | <span data-ttu-id="64c16-1676">Der Knoten stellt ein Füll Wort in einer Vektor Abfrage dar.</span><span class="sxs-lookup"><span data-stu-id="64c16-1676">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="64c16-1677">Rtand 0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-1677">RTAnd 0x00000001</span></span>         | <span data-ttu-id="64c16-1678">Der Knoten enthält eine cnoderestriction, auf der eine logische and-Operation ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1678">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="64c16-1679">Rtor 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-1679">RTOr 0x00000002</span></span>          | <span data-ttu-id="64c16-1680">Der Knoten enthält eine cnoderestriction, auf der eine logische OR-Operation ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1680">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="64c16-1681">Rtnot 0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-1681">RTNot 0x00000003</span></span>         | <span data-ttu-id="64c16-1682">Der Knoten enthält eine Einschränkung, auf der ein Not-Vorgang ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1682">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="64c16-1683">Rtcontent 0x00000004</span><span class="sxs-lookup"><span data-stu-id="64c16-1683">RTContent 0x00000004</span></span>     | <span data-ttu-id="64c16-1684">Der Knoten enthält eine Ccontent-Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="64c16-1684">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="64c16-1685">Rtproperty 0x00000005 bei der</span><span class="sxs-lookup"><span data-stu-id="64c16-1685">RTProperty 0x00000005</span></span>    | <span data-ttu-id="64c16-1686">Der Knoten enthält eine cpropertyeinschränkungs Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="64c16-1686">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="64c16-1687">Rtnear 0x00000006</span><span class="sxs-lookup"><span data-stu-id="64c16-1687">RTProximity 0x00000006</span></span>   | <span data-ttu-id="64c16-1688">Der Knoten enthält eine cnoderestriction, auf der eine near-Rangfolge ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1688">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="64c16-1689">Rtvector 0x00000007</span><span class="sxs-lookup"><span data-stu-id="64c16-1689">RTVector 0x00000007</span></span>      | <span data-ttu-id="64c16-1690">Der Knoten enthält eine cvectoreinschränkung.</span><span class="sxs-lookup"><span data-stu-id="64c16-1690">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="64c16-1691">Rtnatlanguage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="64c16-1691">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="64c16-1692">Der Knoten enthält eine cnatlanguagerestriction.</span><span class="sxs-lookup"><span data-stu-id="64c16-1692">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="64c16-1693">Rtscope 0x00000009</span><span class="sxs-lookup"><span data-stu-id="64c16-1693">RTScope 0x00000009</span></span>       | <span data-ttu-id="64c16-1694">Der Knoten enthält eine cscoperestriction.</span><span class="sxs-lookup"><span data-stu-id="64c16-1694">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="64c16-1695">Alle 0xfffffffffa</span><span class="sxs-lookup"><span data-stu-id="64c16-1695">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="64c16-1696">Der Knoten enthält eine cinternalpropertyeinschränkungs Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="64c16-1696">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="64c16-1697">Rtrange 0xfffffffc</span><span class="sxs-lookup"><span data-stu-id="64c16-1697">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="64c16-1698">Der Knoten enthält einen crangerestriction-Knoten.</span><span class="sxs-lookup"><span data-stu-id="64c16-1698">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="64c16-1699">Rtphrase 0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="64c16-1699">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="64c16-1700">Der Knoten enthält eine cnoderestriction, auf der eine Ausdrucks Übereinstimmung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1700">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="64c16-1701">Rtsynonym 0xfffffffe</span><span class="sxs-lookup"><span data-stu-id="64c16-1701">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="64c16-1702">Der Knoten enthält eine csyneinschränkung.</span><span class="sxs-lookup"><span data-stu-id="64c16-1702">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="64c16-1703">Rtword 0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="64c16-1703">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="64c16-1704">Der Knoten enthält ein cwordrestriction-Element.</span><span class="sxs-lookup"><span data-stu-id="64c16-1704">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="64c16-1705">**Weight**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gewichtung des Knotens darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1705">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="64c16-1706">Gewichtung gibt die Wichtigkeit des Knotens relativ zu anderen Knoten in der Abfrage Befehlsstruktur an.</span><span class="sxs-lookup"><span data-stu-id="64c16-1706">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="64c16-1707">Höhere Gewichtungswerte sind wichtiger.</span><span class="sxs-lookup"><span data-stu-id="64c16-1707">Higher weight values are more important.</span></span>

<span data-ttu-id="64c16-1708">**Einschränkung**: der Einschränkungstyp für den Befehlsstruktur Knoten.</span><span class="sxs-lookup"><span data-stu-id="64c16-1708">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="64c16-1709">Die Syntax muss wie im \_ Feld ultype angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1709">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="64c16-1710">2.2.1.17 ccolumnset</span><span class="sxs-lookup"><span data-stu-id="64c16-1710">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="64c16-1711">Die ccolumnset-Struktur gibt die Spalten Nummern an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1711">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="64c16-1712">Diese Struktur wird immer als Verweis auf eine bestimmte cpidmapper-Struktur (Abschnitt 2.2.1.23) verwendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-1712">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="64c16-1713">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1713">0</span></span>

<span data-ttu-id="64c16-1714">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1714">1</span></span>

<span data-ttu-id="64c16-1715">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1715">2</span></span>

<span data-ttu-id="64c16-1716">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1716">3</span></span>

<span data-ttu-id="64c16-1717">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1717">4</span></span>

<span data-ttu-id="64c16-1718">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1718">5</span></span>

<span data-ttu-id="64c16-1719">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1719">6</span></span>

<span data-ttu-id="64c16-1720">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1720">7</span></span>

<span data-ttu-id="64c16-1721">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1721">8</span></span>

<span data-ttu-id="64c16-1722">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1722">9</span></span>

<span data-ttu-id="64c16-1723">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1723">1</span></span><br/> <span data-ttu-id="64c16-1724">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1724">0</span></span><br/>

<span data-ttu-id="64c16-1725">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1725">1</span></span>

<span data-ttu-id="64c16-1726">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1726">2</span></span>

<span data-ttu-id="64c16-1727">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1727">3</span></span>

<span data-ttu-id="64c16-1728">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1728">4</span></span>

<span data-ttu-id="64c16-1729">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1729">5</span></span>

<span data-ttu-id="64c16-1730">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1730">6</span></span>

<span data-ttu-id="64c16-1731">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1731">7</span></span>

<span data-ttu-id="64c16-1732">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1732">8</span></span>

<span data-ttu-id="64c16-1733">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1733">9</span></span>

<span data-ttu-id="64c16-1734">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1734">2</span></span><br/> <span data-ttu-id="64c16-1735">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1735">0</span></span><br/>

<span data-ttu-id="64c16-1736">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1736">1</span></span>

<span data-ttu-id="64c16-1737">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1737">2</span></span>

<span data-ttu-id="64c16-1738">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1738">3</span></span>

<span data-ttu-id="64c16-1739">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1739">4</span></span>

<span data-ttu-id="64c16-1740">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1740">5</span></span>

<span data-ttu-id="64c16-1741">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1741">6</span></span>

<span data-ttu-id="64c16-1742">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1742">7</span></span>

<span data-ttu-id="64c16-1743">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1743">8</span></span>

<span data-ttu-id="64c16-1744">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1744">9</span></span>

<span data-ttu-id="64c16-1745">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1745">3</span></span><br/> <span data-ttu-id="64c16-1746">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1746">0</span></span><br/>

<span data-ttu-id="64c16-1747">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1747">1</span></span>

<span data-ttu-id="64c16-1748">count</span><span class="sxs-lookup"><span data-stu-id="64c16-1748">count</span></span>

<span data-ttu-id="64c16-1749">Indizes (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1749">indexes (variable)</span></span>



 

<span data-ttu-id="64c16-1750">**count**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im Index Array angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1750">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="64c16-1751">**Indizes**: Array von 4-Byte-Ganzzahlen ohne Vorzeichen, das null basierte Indizes im apropspec-Array in der entsprechenden cpidmapper-Struktur darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1751">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="64c16-1752">2.2.1.18 ccategorizationset</span><span class="sxs-lookup"><span data-stu-id="64c16-1752">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="64c16-1753">Die ccategorizationset-Struktur enthält Informationen zur Gruppierung eines Abfrageresultsets.</span><span class="sxs-lookup"><span data-stu-id="64c16-1753">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="64c16-1754">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1754">0</span></span>

<span data-ttu-id="64c16-1755">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1755">1</span></span>

<span data-ttu-id="64c16-1756">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1756">2</span></span>

<span data-ttu-id="64c16-1757">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1757">3</span></span>

<span data-ttu-id="64c16-1758">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1758">4</span></span>

<span data-ttu-id="64c16-1759">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1759">5</span></span>

<span data-ttu-id="64c16-1760">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1760">6</span></span>

<span data-ttu-id="64c16-1761">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1761">7</span></span>

<span data-ttu-id="64c16-1762">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1762">8</span></span>

<span data-ttu-id="64c16-1763">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1763">9</span></span>

<span data-ttu-id="64c16-1764">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1764">1</span></span><br/> <span data-ttu-id="64c16-1765">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1765">0</span></span><br/>

<span data-ttu-id="64c16-1766">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1766">1</span></span>

<span data-ttu-id="64c16-1767">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1767">2</span></span>

<span data-ttu-id="64c16-1768">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1768">3</span></span>

<span data-ttu-id="64c16-1769">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1769">4</span></span>

<span data-ttu-id="64c16-1770">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1770">5</span></span>

<span data-ttu-id="64c16-1771">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1771">6</span></span>

<span data-ttu-id="64c16-1772">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1772">7</span></span>

<span data-ttu-id="64c16-1773">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1773">8</span></span>

<span data-ttu-id="64c16-1774">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1774">9</span></span>

<span data-ttu-id="64c16-1775">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1775">2</span></span><br/> <span data-ttu-id="64c16-1776">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1776">0</span></span><br/>

<span data-ttu-id="64c16-1777">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1777">1</span></span>

<span data-ttu-id="64c16-1778">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1778">2</span></span>

<span data-ttu-id="64c16-1779">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1779">3</span></span>

<span data-ttu-id="64c16-1780">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1780">4</span></span>

<span data-ttu-id="64c16-1781">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1781">5</span></span>

<span data-ttu-id="64c16-1782">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1782">6</span></span>

<span data-ttu-id="64c16-1783">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1783">7</span></span>

<span data-ttu-id="64c16-1784">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1784">8</span></span>

<span data-ttu-id="64c16-1785">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1785">9</span></span>

<span data-ttu-id="64c16-1786">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1786">3</span></span><br/> <span data-ttu-id="64c16-1787">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1787">0</span></span><br/>

<span data-ttu-id="64c16-1788">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1788">1</span></span>

<span data-ttu-id="64c16-1789">count</span><span class="sxs-lookup"><span data-stu-id="64c16-1789">count</span></span>

<span data-ttu-id="64c16-1790">Kategorien (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1790">categories (variable)</span></span>



 

<span data-ttu-id="64c16-1791">**count**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im kategoriearray enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-1791">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="64c16-1792">**Categories**: Array der ccategorizationspec-Strukturen, die die Gruppierung der Abfrage angeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-1792">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="64c16-1793">2.2.1.19 ccategorizationspec</span><span class="sxs-lookup"><span data-stu-id="64c16-1793">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="64c16-1794">Die ccategorizationspec-Struktur enthält eine Gruppierung für ein Abfrageresultset.</span><span class="sxs-lookup"><span data-stu-id="64c16-1794">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="64c16-1795">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1795">0</span></span>

<span data-ttu-id="64c16-1796">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1796">1</span></span>

<span data-ttu-id="64c16-1797">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1797">2</span></span>

<span data-ttu-id="64c16-1798">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1798">3</span></span>

<span data-ttu-id="64c16-1799">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1799">4</span></span>

<span data-ttu-id="64c16-1800">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1800">5</span></span>

<span data-ttu-id="64c16-1801">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1801">6</span></span>

<span data-ttu-id="64c16-1802">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1802">7</span></span>

<span data-ttu-id="64c16-1803">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1803">8</span></span>

<span data-ttu-id="64c16-1804">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1804">9</span></span>

<span data-ttu-id="64c16-1805">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1805">1</span></span><br/> <span data-ttu-id="64c16-1806">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1806">0</span></span><br/>

<span data-ttu-id="64c16-1807">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1807">1</span></span>

<span data-ttu-id="64c16-1808">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1808">2</span></span>

<span data-ttu-id="64c16-1809">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1809">3</span></span>

<span data-ttu-id="64c16-1810">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1810">4</span></span>

<span data-ttu-id="64c16-1811">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1811">5</span></span>

<span data-ttu-id="64c16-1812">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1812">6</span></span>

<span data-ttu-id="64c16-1813">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1813">7</span></span>

<span data-ttu-id="64c16-1814">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1814">8</span></span>

<span data-ttu-id="64c16-1815">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1815">9</span></span>

<span data-ttu-id="64c16-1816">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1816">2</span></span><br/> <span data-ttu-id="64c16-1817">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1817">0</span></span><br/>

<span data-ttu-id="64c16-1818">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1818">1</span></span>

<span data-ttu-id="64c16-1819">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1819">2</span></span>

<span data-ttu-id="64c16-1820">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1820">3</span></span>

<span data-ttu-id="64c16-1821">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1821">4</span></span>

<span data-ttu-id="64c16-1822">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1822">5</span></span>

<span data-ttu-id="64c16-1823">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1823">6</span></span>

<span data-ttu-id="64c16-1824">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1824">7</span></span>

<span data-ttu-id="64c16-1825">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1825">8</span></span>

<span data-ttu-id="64c16-1826">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1826">9</span></span>

<span data-ttu-id="64c16-1827">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1827">3</span></span><br/> <span data-ttu-id="64c16-1828">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1828">0</span></span><br/>

<span data-ttu-id="64c16-1829">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1829">1</span></span>

<span data-ttu-id="64c16-1830">\_cscolumschlag (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1830">\_csColumns (variable)</span></span>

<span data-ttu-id="64c16-1831">\_ulCategType</span><span class="sxs-lookup"><span data-stu-id="64c16-1831">\_ulCategType</span></span>



 

<span data-ttu-id="64c16-1832">**\_ cscolenns**: eine ccolumnset-Struktur, die die Spalten angibt, nach denen die Abfrage gruppiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1832">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="64c16-1833">**\_ ulCategType**: eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1833">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="64c16-1834">Muss auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1834">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="64c16-1835">2.2.1.20 cdbcolid</span><span class="sxs-lookup"><span data-stu-id="64c16-1835">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="64c16-1836">Die cdbcolid-Struktur enthält eine-Spalte.</span><span class="sxs-lookup"><span data-stu-id="64c16-1836">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="64c16-1837">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1837">0</span></span>

<span data-ttu-id="64c16-1838">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1838">1</span></span>

<span data-ttu-id="64c16-1839">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1839">2</span></span>

<span data-ttu-id="64c16-1840">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1840">3</span></span>

<span data-ttu-id="64c16-1841">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1841">4</span></span>

<span data-ttu-id="64c16-1842">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1842">5</span></span>

<span data-ttu-id="64c16-1843">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1843">6</span></span>

<span data-ttu-id="64c16-1844">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1844">7</span></span>

<span data-ttu-id="64c16-1845">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1845">8</span></span>

<span data-ttu-id="64c16-1846">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1846">9</span></span>

<span data-ttu-id="64c16-1847">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1847">1</span></span><br/> <span data-ttu-id="64c16-1848">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1848">0</span></span><br/>

<span data-ttu-id="64c16-1849">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1849">1</span></span>

<span data-ttu-id="64c16-1850">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1850">2</span></span>

<span data-ttu-id="64c16-1851">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1851">3</span></span>

<span data-ttu-id="64c16-1852">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1852">4</span></span>

<span data-ttu-id="64c16-1853">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1853">5</span></span>

<span data-ttu-id="64c16-1854">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1854">6</span></span>

<span data-ttu-id="64c16-1855">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1855">7</span></span>

<span data-ttu-id="64c16-1856">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1856">8</span></span>

<span data-ttu-id="64c16-1857">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1857">9</span></span>

<span data-ttu-id="64c16-1858">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1858">2</span></span><br/> <span data-ttu-id="64c16-1859">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1859">0</span></span><br/>

<span data-ttu-id="64c16-1860">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1860">1</span></span>

<span data-ttu-id="64c16-1861">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1861">2</span></span>

<span data-ttu-id="64c16-1862">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1862">3</span></span>

<span data-ttu-id="64c16-1863">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1863">4</span></span>

<span data-ttu-id="64c16-1864">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1864">5</span></span>

<span data-ttu-id="64c16-1865">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1865">6</span></span>

<span data-ttu-id="64c16-1866">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1866">7</span></span>

<span data-ttu-id="64c16-1867">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1867">8</span></span>

<span data-ttu-id="64c16-1868">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1868">9</span></span>

<span data-ttu-id="64c16-1869">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1869">3</span></span><br/> <span data-ttu-id="64c16-1870">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1870">0</span></span><br/>

<span data-ttu-id="64c16-1871">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1871">1</span></span>

<span data-ttu-id="64c16-1872">eKind</span><span class="sxs-lookup"><span data-stu-id="64c16-1872">eKind</span></span>

<span data-ttu-id="64c16-1873">GUID</span><span class="sxs-lookup"><span data-stu-id="64c16-1873">GUID</span></span>

<span data-ttu-id="64c16-1874">...</span><span class="sxs-lookup"><span data-stu-id="64c16-1874">...</span></span>

<span data-ttu-id="64c16-1875">...</span><span class="sxs-lookup"><span data-stu-id="64c16-1875">...</span></span>

<span data-ttu-id="64c16-1876">...</span><span class="sxs-lookup"><span data-stu-id="64c16-1876">...</span></span>

<span data-ttu-id="64c16-1877">"ulid"</span><span class="sxs-lookup"><span data-stu-id="64c16-1877">ulId</span></span>

<span data-ttu-id="64c16-1878">vstring (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1878">vString (variable)</span></span>



 

<span data-ttu-id="64c16-1879">**eKind**: muss auf einen der unten aufgeführten Werte festgelegt werden, der den Inhalt von "GUID" und "vValue" angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1879">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="64c16-1880">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-1880">Value</span></span>                            | <span data-ttu-id="64c16-1881">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-1881">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-1882">Dbkind- \_ GUID- \_ Name 0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-1882">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="64c16-1883">vstring enthält einen Eigenschaftsnamen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1883">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="64c16-1884">Dbkind \_ GUID \_ PROPID 0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-1884">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="64c16-1885">die OKD enthält eine 4-Byte-Ganzzahl, die die Eigenschaften-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1885">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="64c16-1886">Dbkind- \_ pguid- \_ Name 0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-1886">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="64c16-1887">vstring enthält einen Eigenschaftsnamen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1887">vString contains a property name.</span></span> <span data-ttu-id="64c16-1888">Dieser Wert muss mit dem dbkind- \_ GUID-Namen behandelt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-1888">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="64c16-1889">Dbkind \_ pguid \_ PROPID 0x00000004</span><span class="sxs-lookup"><span data-stu-id="64c16-1889">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="64c16-1890">die OKD enthält eine 4-Byte-Ganzzahl, die die Eigenschaften-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1890">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="64c16-1891">Dieser Wert muss mit der dbkind- \_ GUID- \_ PROPID identisch sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-1891">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="64c16-1892">**GUID**: die Eigenschafts-GUID.</span><span class="sxs-lookup"><span data-stu-id="64c16-1892">**GUID**: The property GUID.</span></span>

<span data-ttu-id="64c16-1893">**ulid**: Wenn eKind dbkind \_ GUID \_ PROPID oder dbkind \_ pguid \_ PROPID ist, enthält dieses Feld eine Ganzzahl ohne Vorzeichen, die die Eigenschaften-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1893">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="64c16-1894">Wenn eKind den dbkind- \_ GUID- \_ Namen oder den dbkind- \_ pguid- \_ Namen aufweist, enthält dieses Feld eine Ganzzahl ohne Vorzeichen, die die Anzahl der im vstring-Feld enthaltenen Unicode-Zeichen angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1894">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="64c16-1895">**vstring**: eine Unicode-Zeichenfolge, die nicht auf NULL fest steht und den Eigenschaftsnamen darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1895">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="64c16-1896">Sie muss weggelassen werden, es sei denn, das eKind-Feld ist auf den dbkind- \_ GUID- \_ Namen oder den dbkind- \_ pguid- \_ Namen</span><span class="sxs-lookup"><span data-stu-id="64c16-1896">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="64c16-1897">2.2.1.21 cdbprop</span><span class="sxs-lookup"><span data-stu-id="64c16-1897">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="64c16-1898">Die cdbprop-Struktur enthält eine-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="64c16-1898">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="64c16-1899">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1899">0</span></span>

<span data-ttu-id="64c16-1900">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1900">1</span></span>

<span data-ttu-id="64c16-1901">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1901">2</span></span>

<span data-ttu-id="64c16-1902">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1902">3</span></span>

<span data-ttu-id="64c16-1903">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1903">4</span></span>

<span data-ttu-id="64c16-1904">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1904">5</span></span>

<span data-ttu-id="64c16-1905">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1905">6</span></span>

<span data-ttu-id="64c16-1906">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1906">7</span></span>

<span data-ttu-id="64c16-1907">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1907">8</span></span>

<span data-ttu-id="64c16-1908">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1908">9</span></span>

<span data-ttu-id="64c16-1909">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1909">1</span></span><br/> <span data-ttu-id="64c16-1910">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1910">0</span></span><br/>

<span data-ttu-id="64c16-1911">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1911">1</span></span>

<span data-ttu-id="64c16-1912">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1912">2</span></span>

<span data-ttu-id="64c16-1913">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1913">3</span></span>

<span data-ttu-id="64c16-1914">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1914">4</span></span>

<span data-ttu-id="64c16-1915">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1915">5</span></span>

<span data-ttu-id="64c16-1916">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1916">6</span></span>

<span data-ttu-id="64c16-1917">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1917">7</span></span>

<span data-ttu-id="64c16-1918">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1918">8</span></span>

<span data-ttu-id="64c16-1919">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1919">9</span></span>

<span data-ttu-id="64c16-1920">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1920">2</span></span><br/> <span data-ttu-id="64c16-1921">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1921">0</span></span><br/>

<span data-ttu-id="64c16-1922">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1922">1</span></span>

<span data-ttu-id="64c16-1923">2</span><span class="sxs-lookup"><span data-stu-id="64c16-1923">2</span></span>

<span data-ttu-id="64c16-1924">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1924">3</span></span>

<span data-ttu-id="64c16-1925">4</span><span class="sxs-lookup"><span data-stu-id="64c16-1925">4</span></span>

<span data-ttu-id="64c16-1926">5</span><span class="sxs-lookup"><span data-stu-id="64c16-1926">5</span></span>

<span data-ttu-id="64c16-1927">6</span><span class="sxs-lookup"><span data-stu-id="64c16-1927">6</span></span>

<span data-ttu-id="64c16-1928">7</span><span class="sxs-lookup"><span data-stu-id="64c16-1928">7</span></span>

<span data-ttu-id="64c16-1929">8</span><span class="sxs-lookup"><span data-stu-id="64c16-1929">8</span></span>

<span data-ttu-id="64c16-1930">9</span><span class="sxs-lookup"><span data-stu-id="64c16-1930">9</span></span>

<span data-ttu-id="64c16-1931">3</span><span class="sxs-lookup"><span data-stu-id="64c16-1931">3</span></span><br/> <span data-ttu-id="64c16-1932">0</span><span class="sxs-lookup"><span data-stu-id="64c16-1932">0</span></span><br/>

<span data-ttu-id="64c16-1933">1</span><span class="sxs-lookup"><span data-stu-id="64c16-1933">1</span></span>

<span data-ttu-id="64c16-1934">DBPROPID</span><span class="sxs-lookup"><span data-stu-id="64c16-1934">DBPROPID</span></span>

<span data-ttu-id="64c16-1935">DBPROPOPTIONS</span><span class="sxs-lookup"><span data-stu-id="64c16-1935">DBPROPOPTIONS</span></span>

<span data-ttu-id="64c16-1936">Dbpropstatus</span><span class="sxs-lookup"><span data-stu-id="64c16-1936">DBPROPSTATUS</span></span>

<span data-ttu-id="64c16-1937">kolid (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1937">colid (variable)</span></span>

<span data-ttu-id="64c16-1938">vValue (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-1938">vValue (variable)</span></span>



 

<span data-ttu-id="64c16-1939">**DBPROPID**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Eigenschaften-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1939">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="64c16-1940">**DBPROPOPTIONS** : muss auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1940">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="64c16-1941">**Dbpropstatus**: muss auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1941">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="64c16-1942">**ColId**: eine cdbcolid-Struktur, wie im Abschnitt 2.2.1.20 angegeben, gibt die Spalte an, auf die die Eigenschaft angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-1942">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="64c16-1943">**vValue**: ein cbasestoragevariant-Wert, der den Eigenschafts Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-1943">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="64c16-1944">2.2.1.21.1-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="64c16-1944">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="64c16-1945">In diesem Abschnitt werden die Eigenschaften erläutert, die von CISP verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1945">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="64c16-1946">Diese Eigenschaften werden in drei Eigenschaften Sätze gruppiert: Ident 2.2.1.21.1 Ified im Feld guidPropertySet der CDBPropSet-Struktur (Abschnitt 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="64c16-1946">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="64c16-1947">In der folgenden Tabelle sind die Eigenschaften aufgelistet, die Teil der Eigenschaft "DBPROPSET \_ fscifrmwrk ext" sind \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-1947">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="64c16-1948">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-1948">Value</span></span>                                  | <span data-ttu-id="64c16-1949">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-1949">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-1950">DBPROP \_ ci- \_ Katalog \_ Name 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-1950">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="64c16-1951">Gibt den Namen des Katalogs oder der Kataloge an, die abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1951">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="64c16-1952">Der Wert muss ein VT \_ LPWSTR oder ein VT- \_ Vektor \| VT \_ LPWSTR sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="64c16-1953">DBPROP \_ ci \_ include- \_ Bereiche 0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-1953">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="64c16-1954">Gibt einen oder mehrere Pfade an, die in die Abfrage eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1954">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="64c16-1955">Der Wert muss ein VT \_ LPWSTR oder ein VT- \_ Vektor \| VT \_ LPWSTR sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-1955">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="64c16-1956">DBPROP \_ ci \_ - \_ bereichsflags 0x00000004</span><span class="sxs-lookup"><span data-stu-id="64c16-1956">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="64c16-1957">Gibt an, wie die von der Eigenschaft DBPROP \_ CI include-Bereiche angegebenen Pfade \_ behandelt werden \_ sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1957">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="64c16-1958">Der Wert muss ein VT- \_ I4 oder ein VT \_ Vector \| VT I4 sein \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-1958">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="64c16-1959">DBPROP \_ ci \_ - \_ Abfragetyp 0x00000007</span><span class="sxs-lookup"><span data-stu-id="64c16-1959">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="64c16-1960">Gibt den Typ der Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="64c16-1960">Specifies the type of query.</span></span> <span data-ttu-id="64c16-1961">Cdbcolid muss auf DB nullid festgelegt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-1961">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="64c16-1962">In der folgenden Tabelle sind die Flags für die Eigenschaft DBPROP \_ ci \_ Scope \_ Flags aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="64c16-1962">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="64c16-1963">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-1963">Value</span></span>                     | <span data-ttu-id="64c16-1964">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-1964">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-1965">Abfragen von \_ Deep 0x01</span><span class="sxs-lookup"><span data-stu-id="64c16-1965">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="64c16-1966">Wenn dieser Wert festgelegt ist, wird angegeben, dass Dateien im Bereichs Verzeichnis und alle Unterverzeichnisse in den Ergebnissen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-1966">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="64c16-1967">Wenn Clear, werden nur Dateien im Bereichs Verzeichnis in die Ergebnisse eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1967">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="64c16-1968">Darf nicht mit einer Abfrage Tiefe kombiniert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-1968">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="64c16-1969">Abfrage des \_ virtuellen \_ Pfads 0x02</span><span class="sxs-lookup"><span data-stu-id="64c16-1969">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="64c16-1970">Wenn festgelegt, wird angegeben, dass der Bereich ein virtueller Pfad ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-1970">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="64c16-1971">Wenn Clear, wird angegeben, dass es sich bei dem Bereich um ein physisches Verzeichnis handelt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1971">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="64c16-1972">In der folgenden Tabelle sind die Abfrage Typen für die Eigenschaft DBPROP \_ ci- \_ Abfragetyp aufgelistet \_ :</span><span class="sxs-lookup"><span data-stu-id="64c16-1972">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="64c16-1973">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-1973">Value</span></span>                     | <span data-ttu-id="64c16-1974">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-1974">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-1975">Cinormale 0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-1975">CiNormal 0x00000000</span></span>       | <span data-ttu-id="64c16-1976">Eine reguläre Abfrage.</span><span class="sxs-lookup"><span data-stu-id="64c16-1976">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="64c16-1977">Civirtualroots 0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-1977">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="64c16-1978">Die Abfrage fordert eine Liste der virtuellen Stämme des Katalogs an.</span><span class="sxs-lookup"><span data-stu-id="64c16-1978">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="64c16-1979">Dieser Wert erfordert Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="64c16-1979">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="64c16-1980">Ciproperties 0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-1980">CiProperties 0x00000003</span></span>   | <span data-ttu-id="64c16-1981">Die Abfrage fordert eine Liste aller Eigenschaften an, die vom Index Dienst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-1981">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="64c16-1982">Ciadminop 0x00000004</span><span class="sxs-lookup"><span data-stu-id="64c16-1982">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="64c16-1983">Bei der Abfrage handelt es sich um einen administrativen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="64c16-1983">The query is an administrative operation.</span></span> <span data-ttu-id="64c16-1984">Dieser Wert erfordert Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="64c16-1984">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="64c16-1985">In der folgenden Tabelle werden die Eigenschaften aufgelistet, die Teil der Eigenschaft "DBPROPSET \_ queryext" sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-1985">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="64c16-1986">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-1986">Value</span></span>                                      | <span data-ttu-id="64c16-1987">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-1987">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-1988">DBPROP \_ usecontentindex 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-1988">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="64c16-1989">Gibt an, wie langsame Abfragen vom Index Dienst verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-1989">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="64c16-1990">Der Wert muss ein VT-boolescher Wert sein \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-1990">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="64c16-1991">TRUE gibt an, dass der Server diese Abfragen nicht ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="64c16-1991">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="64c16-1992">DBPROP-Debug-Einschränkung \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-1992">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="64c16-1993">Gibt an, ob der Indizierungs Dienst das Kürzen von Ergebnissen durchführen soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-1993">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="64c16-1994">TRUE gibt an, dass der Server eine Kürzung der Ergebnisse auf eine Weise durchführen soll, mit der die Reaktionszeit für den Client optimiert wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-1994">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="64c16-1995">Der Wert muss ein VT-boolescher Wert sein \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-1995">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="64c16-1996">DBPROP \_ useextendeddbtypes 0x00000004</span><span class="sxs-lookup"><span data-stu-id="64c16-1996">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="64c16-1997">Gibt an, ob der Client VT- \_ Vektor Datentypen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="64c16-1997">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="64c16-1998">Wenn true, unterstützt der Client VT \_ Vector; Wenn false, wird der Server zum Konvertieren von VT- \_ Vektor Datentypen in VT- \_ Array Datentypen verwendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-1998">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="64c16-1999">Der Wert muss ein VT- \_ boolescher Wert sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-1999">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="64c16-2000">DBPROP \_ firstrows 0x00000007</span><span class="sxs-lookup"><span data-stu-id="64c16-2000">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="64c16-2001">Gibt die zurück zugebende Zeilen Übereinstimmungen an.</span><span class="sxs-lookup"><span data-stu-id="64c16-2001">Indicates the row matches to return.</span></span> <span data-ttu-id="64c16-2002">TRUE gibt an, dass der Server den ersten Satz übereinstimmender Zeilen zurückgeben soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-2002">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="64c16-2003">Wenn der Wert false ist, sollten die am besten passenden Zeilen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2003">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="64c16-2004">Der Wert muss ein VT-boolescher Wert sein \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-2004">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="64c16-2005">In der folgenden Tabelle sind die Eigenschaften aufgelistet, die Teil der Eigenschaft "DBPROPSET \_ cifrmwrkcore ext" sind \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-2005">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="64c16-2006">Wert/DBPROPID</span><span class="sxs-lookup"><span data-stu-id="64c16-2006">Value / DBPROPID</span></span>                 | <span data-ttu-id="64c16-2007">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-2007">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-2008">DBPROP- \_ Computer 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-2008">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="64c16-2009">Gibt die Namen der Computer an, auf denen eine Abfrage verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-2009">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="64c16-2010">Der Wert muss entweder "VT \_ BSTR" oder "VT \_ array \| VT \_ BSTR" lauten.</span><span class="sxs-lookup"><span data-stu-id="64c16-2010">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="64c16-2011">DBPROP- \_ Client- \_ CLSID 0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-2011">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="64c16-2012">Gibt eine Verbindungs Konstante für den Indizierungs Dienst an.</span><span class="sxs-lookup"><span data-stu-id="64c16-2012">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="64c16-2013">Der Wert muss eine VT CLSID sein, die \_ 0x2a4880706f 80800a0c906241a enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-2013">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="64c16-2014">2.2.1.22 CDBPropSet</span><span class="sxs-lookup"><span data-stu-id="64c16-2014">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="64c16-2015">Die CDBPropSet-Struktur enthält eine Reihe von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="64c16-2015">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="64c16-2016">Beachten Sie, dass das erste Feld eine fest Größe hat, aber möglicherweise nicht an einem Offset ausgerichtet ist, bei dem es sich um ein 4-Byte-vielfache vom Beginn der Nachricht mit dieser Struktur handelt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2016">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="64c16-2017">Das Feld "cproperties" wird jedoch als solches ausgerichtet, weshalb das Format wie folgt dargestellt wird:</span><span class="sxs-lookup"><span data-stu-id="64c16-2017">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="64c16-2018">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2018">0</span></span>

<span data-ttu-id="64c16-2019">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2019">1</span></span>

<span data-ttu-id="64c16-2020">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2020">2</span></span>

<span data-ttu-id="64c16-2021">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2021">3</span></span>

<span data-ttu-id="64c16-2022">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2022">4</span></span>

<span data-ttu-id="64c16-2023">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2023">5</span></span>

<span data-ttu-id="64c16-2024">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2024">6</span></span>

<span data-ttu-id="64c16-2025">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2025">7</span></span>

<span data-ttu-id="64c16-2026">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2026">8</span></span>

<span data-ttu-id="64c16-2027">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2027">9</span></span>

<span data-ttu-id="64c16-2028">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2028">1</span></span><br/> <span data-ttu-id="64c16-2029">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2029">0</span></span><br/>

<span data-ttu-id="64c16-2030">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2030">1</span></span>

<span data-ttu-id="64c16-2031">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2031">2</span></span>

<span data-ttu-id="64c16-2032">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2032">3</span></span>

<span data-ttu-id="64c16-2033">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2033">4</span></span>

<span data-ttu-id="64c16-2034">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2034">5</span></span>

<span data-ttu-id="64c16-2035">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2035">6</span></span>

<span data-ttu-id="64c16-2036">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2036">7</span></span>

<span data-ttu-id="64c16-2037">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2037">8</span></span>

<span data-ttu-id="64c16-2038">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2038">9</span></span>

<span data-ttu-id="64c16-2039">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2039">2</span></span><br/> <span data-ttu-id="64c16-2040">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2040">0</span></span><br/>

<span data-ttu-id="64c16-2041">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2041">1</span></span>

<span data-ttu-id="64c16-2042">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2042">2</span></span>

<span data-ttu-id="64c16-2043">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2043">3</span></span>

<span data-ttu-id="64c16-2044">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2044">4</span></span>

<span data-ttu-id="64c16-2045">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2045">5</span></span>

<span data-ttu-id="64c16-2046">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2046">6</span></span>

<span data-ttu-id="64c16-2047">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2047">7</span></span>

<span data-ttu-id="64c16-2048">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2048">8</span></span>

<span data-ttu-id="64c16-2049">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2049">9</span></span>

<span data-ttu-id="64c16-2050">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2050">3</span></span><br/> <span data-ttu-id="64c16-2051">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2051">0</span></span><br/>

<span data-ttu-id="64c16-2052">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2052">1</span></span>

<span data-ttu-id="64c16-2053">guidPropertySet</span><span class="sxs-lookup"><span data-stu-id="64c16-2053">guidPropertySet</span></span>

<span data-ttu-id="64c16-2054">...</span><span class="sxs-lookup"><span data-stu-id="64c16-2054">...</span></span>

<span data-ttu-id="64c16-2055">...</span><span class="sxs-lookup"><span data-stu-id="64c16-2055">...</span></span>

<span data-ttu-id="64c16-2056">...</span><span class="sxs-lookup"><span data-stu-id="64c16-2056">...</span></span>

<span data-ttu-id="64c16-2057">...</span><span class="sxs-lookup"><span data-stu-id="64c16-2057">...</span></span>

<span data-ttu-id="64c16-2058">\_Auffüll Zeichen (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-2058">\_padding (variable)</span></span>

<span data-ttu-id="64c16-2059">cproperties</span><span class="sxs-lookup"><span data-stu-id="64c16-2059">cProperties</span></span>

<span data-ttu-id="64c16-2060">a-Eigenschaften (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-2060">aProps (variable)</span></span>



 

<span data-ttu-id="64c16-2061">**guidPropertySet**: eine GUID, die den Eigenschaften Satz identifiziert.</span><span class="sxs-lookup"><span data-stu-id="64c16-2061">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="64c16-2062">Muss auf das binäre Format festgelegt werden, das einem der folgenden Werte entspricht (im Formular der Zeichen folgen Darstellung dargestellt), und identifiziert den Eigenschaften Satz der Eigenschaften, die im Feld "aproperties" enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-2062">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="64c16-2063">Wert/GUID</span><span class="sxs-lookup"><span data-stu-id="64c16-2063">Value / GUID</span></span>                                                                              | <span data-ttu-id="64c16-2064">Name</span><span class="sxs-lookup"><span data-stu-id="64c16-2064">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="64c16-2065">DBPROPSET " \_ f-frmwrk" \_</span><span class="sxs-lookup"><span data-stu-id="64c16-2065">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="64c16-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="64c16-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="64c16-2067">Framework-Eigenschaften Satz für Datei System-Inhalts Index</span><span class="sxs-lookup"><span data-stu-id="64c16-2067">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="64c16-2068">DBPROPSET \_ queryext</span><span class="sxs-lookup"><span data-stu-id="64c16-2068">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="64c16-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="64c16-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="64c16-2070">Eigenschaften Satz für Abfrageerweiterung</span><span class="sxs-lookup"><span data-stu-id="64c16-2070">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="64c16-2071">DBPROPSET \_ cifrmwrkcore- \_ ext</span><span class="sxs-lookup"><span data-stu-id="64c16-2071">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="64c16-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="64c16-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="64c16-2073">Inhalts Index Framework-Kerneigenschaften Satz</span><span class="sxs-lookup"><span data-stu-id="64c16-2073">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="64c16-2074">**\_ Auffüllung**: Dieses Feld muss zwischen 0 und 3 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-2074">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="64c16-2075">Die Länge dieses Felds muss so lauten, dass das folgende Feld bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die diese Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-2075">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="64c16-2076">Wenn dieses Feld vorhanden ist (d. h. eine Länge ungleich 0 (null)), ist der enthaltene Wert beliebig.</span><span class="sxs-lookup"><span data-stu-id="64c16-2076">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="64c16-2077">Der Inhalt dieses Felds muss vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2077">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="64c16-2078">**cproperties**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im aproperties-Array enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-2078">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="64c16-2079">**aproperties**: ein Array aus cdbprop-Strukturen, wie in Abschnitt 0 angegeben, das Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-2079">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="64c16-2080">Strukturen im Array müssen durch 0 bis 3 Auffüll Bytes voneinander getrennt werden, sodass jede Struktur bei einem Offset beginnt, bei dem es sich um ein Vielfaches von 4 Bytes vom Anfang der Nachricht handelt, die dieses Array enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-2080">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="64c16-2081">Wenn Auffüll-Bytes vorhanden sind, ist der Wert, den Sie enthalten, willkürlich.</span><span class="sxs-lookup"><span data-stu-id="64c16-2081">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="64c16-2082">Der Inhalt der Auffüll Zeichen muss vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2082">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="64c16-2083">2.2.1.23 cpidmapper</span><span class="sxs-lookup"><span data-stu-id="64c16-2083">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="64c16-2084">Die cpidmapper-Struktur enthält ein Array von Eigenschaften-IDs, die die Eigenschaften angeben, die in einem Rowset zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2084">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="64c16-2085">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2085">0</span></span>

<span data-ttu-id="64c16-2086">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2086">1</span></span>

<span data-ttu-id="64c16-2087">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2087">2</span></span>

<span data-ttu-id="64c16-2088">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2088">3</span></span>

<span data-ttu-id="64c16-2089">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2089">4</span></span>

<span data-ttu-id="64c16-2090">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2090">5</span></span>

<span data-ttu-id="64c16-2091">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2091">6</span></span>

<span data-ttu-id="64c16-2092">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2092">7</span></span>

<span data-ttu-id="64c16-2093">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2093">8</span></span>

<span data-ttu-id="64c16-2094">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2094">9</span></span>

<span data-ttu-id="64c16-2095">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2095">1</span></span><br/> <span data-ttu-id="64c16-2096">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2096">0</span></span><br/>

<span data-ttu-id="64c16-2097">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2097">1</span></span>

<span data-ttu-id="64c16-2098">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2098">2</span></span>

<span data-ttu-id="64c16-2099">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2099">3</span></span>

<span data-ttu-id="64c16-2100">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2100">4</span></span>

<span data-ttu-id="64c16-2101">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2101">5</span></span>

<span data-ttu-id="64c16-2102">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2102">6</span></span>

<span data-ttu-id="64c16-2103">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2103">7</span></span>

<span data-ttu-id="64c16-2104">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2104">8</span></span>

<span data-ttu-id="64c16-2105">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2105">9</span></span>

<span data-ttu-id="64c16-2106">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2106">2</span></span><br/> <span data-ttu-id="64c16-2107">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2107">0</span></span><br/>

<span data-ttu-id="64c16-2108">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2108">1</span></span>

<span data-ttu-id="64c16-2109">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2109">2</span></span>

<span data-ttu-id="64c16-2110">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2110">3</span></span>

<span data-ttu-id="64c16-2111">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2111">4</span></span>

<span data-ttu-id="64c16-2112">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2112">5</span></span>

<span data-ttu-id="64c16-2113">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2113">6</span></span>

<span data-ttu-id="64c16-2114">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2114">7</span></span>

<span data-ttu-id="64c16-2115">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2115">8</span></span>

<span data-ttu-id="64c16-2116">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2116">9</span></span>

<span data-ttu-id="64c16-2117">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2117">3</span></span><br/> <span data-ttu-id="64c16-2118">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2118">0</span></span><br/>

<span data-ttu-id="64c16-2119">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2119">1</span></span>

<span data-ttu-id="64c16-2120">count</span><span class="sxs-lookup"><span data-stu-id="64c16-2120">count</span></span>

<span data-ttu-id="64c16-2121">apropspec</span><span class="sxs-lookup"><span data-stu-id="64c16-2121">aPropSpec</span></span>

<span data-ttu-id="64c16-2122">... veränder</span><span class="sxs-lookup"><span data-stu-id="64c16-2122">... (variable)</span></span>



 

<span data-ttu-id="64c16-2123">**count**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im apropspec-Array enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-2123">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="64c16-2124">**apropspec**: Array von cfullpropspec-Strukturen, die die zurück zugebende Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-2124">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="64c16-2125">Strukturen im Array müssen durch 0 bis 3 Auffüll Zeichen voneinander getrennt werden, sodass jede Struktur über eine 4-Byte-Ausrichtung ab dem Anfang einer Nachricht verfügt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2125">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="64c16-2126">Bei solchen Füll Zeichen kann es sich um beliebige Werte handeln, die bei der Bestätigung ignoriert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2126">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="64c16-2127">2.2.1.24 crowseekat</span><span class="sxs-lookup"><span data-stu-id="64c16-2127">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="64c16-2128">Die crowseekat-Struktur enthält den Offset, bei dem Zeilen in einer cpmgetrowsin-Nachricht abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2128">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="64c16-2129">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2129">0</span></span>

<span data-ttu-id="64c16-2130">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2130">1</span></span>

<span data-ttu-id="64c16-2131">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2131">2</span></span>

<span data-ttu-id="64c16-2132">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2132">3</span></span>

<span data-ttu-id="64c16-2133">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2133">4</span></span>

<span data-ttu-id="64c16-2134">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2134">5</span></span>

<span data-ttu-id="64c16-2135">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2135">6</span></span>

<span data-ttu-id="64c16-2136">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2136">7</span></span>

<span data-ttu-id="64c16-2137">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2137">8</span></span>

<span data-ttu-id="64c16-2138">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2138">9</span></span>

<span data-ttu-id="64c16-2139">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2139">1</span></span><br/> <span data-ttu-id="64c16-2140">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2140">0</span></span><br/>

<span data-ttu-id="64c16-2141">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2141">1</span></span>

<span data-ttu-id="64c16-2142">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2142">2</span></span>

<span data-ttu-id="64c16-2143">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2143">3</span></span>

<span data-ttu-id="64c16-2144">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2144">4</span></span>

<span data-ttu-id="64c16-2145">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2145">5</span></span>

<span data-ttu-id="64c16-2146">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2146">6</span></span>

<span data-ttu-id="64c16-2147">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2147">7</span></span>

<span data-ttu-id="64c16-2148">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2148">8</span></span>

<span data-ttu-id="64c16-2149">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2149">9</span></span>

<span data-ttu-id="64c16-2150">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2150">2</span></span><br/> <span data-ttu-id="64c16-2151">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2151">0</span></span><br/>

<span data-ttu-id="64c16-2152">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2152">1</span></span>

<span data-ttu-id="64c16-2153">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2153">2</span></span>

<span data-ttu-id="64c16-2154">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2154">3</span></span>

<span data-ttu-id="64c16-2155">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2155">4</span></span>

<span data-ttu-id="64c16-2156">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2156">5</span></span>

<span data-ttu-id="64c16-2157">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2157">6</span></span>

<span data-ttu-id="64c16-2158">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2158">7</span></span>

<span data-ttu-id="64c16-2159">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2159">8</span></span>

<span data-ttu-id="64c16-2160">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2160">9</span></span>

<span data-ttu-id="64c16-2161">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2161">3</span></span><br/> <span data-ttu-id="64c16-2162">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2162">0</span></span><br/>

<span data-ttu-id="64c16-2163">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2163">1</span></span>

<span data-ttu-id="64c16-2164">\_hregion</span><span class="sxs-lookup"><span data-stu-id="64c16-2164">\_hRegion</span></span>

<span data-ttu-id="64c16-2165">\_cskip</span><span class="sxs-lookup"><span data-stu-id="64c16-2165">\_cskip</span></span>

<span data-ttu-id="64c16-2166">\_bmkoffset</span><span class="sxs-lookup"><span data-stu-id="64c16-2166">\_bmkOffset</span></span>



 

<span data-ttu-id="64c16-2167">**\_ hregion**: muss auf 0x00000000 festgelegt werden und muss ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2167">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="64c16-2168">**\_ cskip**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeilen enthält, die im Rowset übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2168">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="64c16-2169">**\_ bmkoffset**: ein 32-Bit-Wert, der das Handle des **Lesezeichens** darstellt, das die Anfangsposition angibt, ab der die Anzahl der in cskip angegebenen Zeilen vor dem Abruf übersprungen \_ werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-2169">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="64c16-2170">2.2.1.25 crowseekatratio</span><span class="sxs-lookup"><span data-stu-id="64c16-2170">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="64c16-2171">Die crowseekatratio-Struktur gibt den Punkt an, an dem mit dem Abrufen einer cpmgetrowsin-Nachricht begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-2171">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="64c16-2172">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2172">0</span></span>

<span data-ttu-id="64c16-2173">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2173">1</span></span>

<span data-ttu-id="64c16-2174">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2174">2</span></span>

<span data-ttu-id="64c16-2175">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2175">3</span></span>

<span data-ttu-id="64c16-2176">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2176">4</span></span>

<span data-ttu-id="64c16-2177">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2177">5</span></span>

<span data-ttu-id="64c16-2178">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2178">6</span></span>

<span data-ttu-id="64c16-2179">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2179">7</span></span>

<span data-ttu-id="64c16-2180">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2180">8</span></span>

<span data-ttu-id="64c16-2181">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2181">9</span></span>

<span data-ttu-id="64c16-2182">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2182">1</span></span><br/> <span data-ttu-id="64c16-2183">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2183">0</span></span><br/>

<span data-ttu-id="64c16-2184">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2184">1</span></span>

<span data-ttu-id="64c16-2185">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2185">2</span></span>

<span data-ttu-id="64c16-2186">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2186">3</span></span>

<span data-ttu-id="64c16-2187">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2187">4</span></span>

<span data-ttu-id="64c16-2188">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2188">5</span></span>

<span data-ttu-id="64c16-2189">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2189">6</span></span>

<span data-ttu-id="64c16-2190">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2190">7</span></span>

<span data-ttu-id="64c16-2191">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2191">8</span></span>

<span data-ttu-id="64c16-2192">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2192">9</span></span>

<span data-ttu-id="64c16-2193">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2193">2</span></span><br/> <span data-ttu-id="64c16-2194">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2194">0</span></span><br/>

<span data-ttu-id="64c16-2195">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2195">1</span></span>

<span data-ttu-id="64c16-2196">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2196">2</span></span>

<span data-ttu-id="64c16-2197">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2197">3</span></span>

<span data-ttu-id="64c16-2198">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2198">4</span></span>

<span data-ttu-id="64c16-2199">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2199">5</span></span>

<span data-ttu-id="64c16-2200">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2200">6</span></span>

<span data-ttu-id="64c16-2201">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2201">7</span></span>

<span data-ttu-id="64c16-2202">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2202">8</span></span>

<span data-ttu-id="64c16-2203">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2203">9</span></span>

<span data-ttu-id="64c16-2204">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2204">3</span></span><br/> <span data-ttu-id="64c16-2205">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2205">0</span></span><br/>

<span data-ttu-id="64c16-2206">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2206">1</span></span>

<span data-ttu-id="64c16-2207">Citblchapt</span><span class="sxs-lookup"><span data-stu-id="64c16-2207">CiTblChapt</span></span>

<span data-ttu-id="64c16-2208">\_hregion</span><span class="sxs-lookup"><span data-stu-id="64c16-2208">\_hRegion</span></span>

<span data-ttu-id="64c16-2209">\_ulnumerator</span><span class="sxs-lookup"><span data-stu-id="64c16-2209">\_ulNumerator</span></span>

<span data-ttu-id="64c16-2210">\_ulnenner</span><span class="sxs-lookup"><span data-stu-id="64c16-2210">\_ulDenominator</span></span>



 

<span data-ttu-id="64c16-2211">**Citblchapt**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Rowset-Kapitel angibt, aus dem Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2211">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="64c16-2212">**\_ hregion**: muss auf 0x00000000 festgelegt werden und muss ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2212">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="64c16-2213">**\_ ulnumerator**: ganze Zahl ohne Vorzeichen mit einer Länge von 32 Bit, die den Zähler des Verhältnis von Zeilen in dem Kapitel darstellt, ab dem der Abruf begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-2213">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="64c16-2214">**\_ ulnenner**: unsignierte 32-Bit-Ganzzahl, die den Nenner des Verhältnis von Zeilen in dem Kapitel darstellt, ab dem der Abruf begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-2214">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="64c16-2215">Muss größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-2215">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="64c16-2216">2.2.1.26 crowseekbybookmark</span><span class="sxs-lookup"><span data-stu-id="64c16-2216">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="64c16-2217">Die crowseekbybookmark-Struktur gibt die Lesezeichen an, aus denen mit dem Abrufen von Zeilen für eine cpmgetrowsin-Nachricht begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-2217">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="64c16-2218">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2218">0</span></span>

<span data-ttu-id="64c16-2219">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2219">1</span></span>

<span data-ttu-id="64c16-2220">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2220">2</span></span>

<span data-ttu-id="64c16-2221">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2221">3</span></span>

<span data-ttu-id="64c16-2222">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2222">4</span></span>

<span data-ttu-id="64c16-2223">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2223">5</span></span>

<span data-ttu-id="64c16-2224">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2224">6</span></span>

<span data-ttu-id="64c16-2225">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2225">7</span></span>

<span data-ttu-id="64c16-2226">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2226">8</span></span>

<span data-ttu-id="64c16-2227">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2227">9</span></span>

<span data-ttu-id="64c16-2228">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2228">1</span></span><br/> <span data-ttu-id="64c16-2229">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2229">0</span></span><br/>

<span data-ttu-id="64c16-2230">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2230">1</span></span>

<span data-ttu-id="64c16-2231">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2231">2</span></span>

<span data-ttu-id="64c16-2232">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2232">3</span></span>

<span data-ttu-id="64c16-2233">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2233">4</span></span>

<span data-ttu-id="64c16-2234">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2234">5</span></span>

<span data-ttu-id="64c16-2235">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2235">6</span></span>

<span data-ttu-id="64c16-2236">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2236">7</span></span>

<span data-ttu-id="64c16-2237">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2237">8</span></span>

<span data-ttu-id="64c16-2238">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2238">9</span></span>

<span data-ttu-id="64c16-2239">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2239">2</span></span><br/> <span data-ttu-id="64c16-2240">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2240">0</span></span><br/>

<span data-ttu-id="64c16-2241">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2241">1</span></span>

<span data-ttu-id="64c16-2242">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2242">2</span></span>

<span data-ttu-id="64c16-2243">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2243">3</span></span>

<span data-ttu-id="64c16-2244">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2244">4</span></span>

<span data-ttu-id="64c16-2245">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2245">5</span></span>

<span data-ttu-id="64c16-2246">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2246">6</span></span>

<span data-ttu-id="64c16-2247">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2247">7</span></span>

<span data-ttu-id="64c16-2248">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2248">8</span></span>

<span data-ttu-id="64c16-2249">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2249">9</span></span>

<span data-ttu-id="64c16-2250">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2250">3</span></span><br/> <span data-ttu-id="64c16-2251">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2251">0</span></span><br/>

<span data-ttu-id="64c16-2252">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2252">1</span></span>

<span data-ttu-id="64c16-2253">\_hregion</span><span class="sxs-lookup"><span data-stu-id="64c16-2253">\_hRegion</span></span>

<span data-ttu-id="64c16-2254">\_cbookmarks</span><span class="sxs-lookup"><span data-stu-id="64c16-2254">\_cBookmarks</span></span>

<span data-ttu-id="64c16-2255">\_maxret</span><span class="sxs-lookup"><span data-stu-id="64c16-2255">\_maxRet</span></span>

<span data-ttu-id="64c16-2256">\_cvalidret</span><span class="sxs-lookup"><span data-stu-id="64c16-2256">\_cValidRet</span></span>

<span data-ttu-id="64c16-2257">\_abookmarks (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-2257">\_aBookmarks (variable)</span></span>

<span data-ttu-id="64c16-2258">\_askret (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-2258">\_ascRet (variable)</span></span>



 

<span data-ttu-id="64c16-2259">**\_ hregion**: muss auf 0x00000000 festgelegt werden und muss ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2259">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="64c16-2260">**\_ cbookmarks**: nicht signierte 32-Bit-Ganzzahl, die die Anzahl der Elemente im \_ abookmarks-Array darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2260">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="64c16-2261">**\_ maxret**: unsigned 32-Bit-Ganzzahl, die die Anzahl der Elemente im \_ askret-Array darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2261">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="64c16-2262">**\_ cvalidret**: unsignierte 32-Bit-Ganzzahl, die die Anzahl der gültigen Elemente im \_ askret-Array darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2262">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="64c16-2263">Gültige Elemente wurden im Array definiert, ungültige Elemente sind jedoch nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="64c16-2263">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="64c16-2264">**\_ abookmarks**: ein Array von Lesezeichen Handles (jedes dargestellt durch 4 Bytes), wie von einer cpmgetrowsout-Nachricht abgerufen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2264">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="64c16-2265">**\_ askret**: ein Array von HRESULT-Werten.</span><span class="sxs-lookup"><span data-stu-id="64c16-2265">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="64c16-2266">Wenn das crowseekbybookmark-Element als Teil der cpmgetrowsin-Anforderung gesendet wird, muss die Anzahl der Einträge im Array gleich \_ clese Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-2266">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="64c16-2267">Wenn Sie vom Client gesendet werden, müssen die Werte auf 0 (null) festgelegt werden, und der Server muss den Inhalt des Arrays ignorieren.</span><span class="sxs-lookup"><span data-stu-id="64c16-2267">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="64c16-2268">Wenn Sie vom Server gesendet werden (als Teil der cpmgetrowsout-Nachricht), geben die Werte im Array den Ergebnis Status für die einzelnen Zeilen Abruf Vorgänge an.</span><span class="sxs-lookup"><span data-stu-id="64c16-2268">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="64c16-2269">2.2.1.27 crowseeknext</span><span class="sxs-lookup"><span data-stu-id="64c16-2269">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="64c16-2270">Die crowseeknext-Struktur enthält die Anzahl der Zeilen, die in einer cpmgetrowsin-Nachricht übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2270">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="64c16-2271">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2271">0</span></span>

<span data-ttu-id="64c16-2272">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2272">1</span></span>

<span data-ttu-id="64c16-2273">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2273">2</span></span>

<span data-ttu-id="64c16-2274">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2274">3</span></span>

<span data-ttu-id="64c16-2275">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2275">4</span></span>

<span data-ttu-id="64c16-2276">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2276">5</span></span>

<span data-ttu-id="64c16-2277">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2277">6</span></span>

<span data-ttu-id="64c16-2278">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2278">7</span></span>

<span data-ttu-id="64c16-2279">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2279">8</span></span>

<span data-ttu-id="64c16-2280">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2280">9</span></span>

<span data-ttu-id="64c16-2281">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2281">1</span></span><br/> <span data-ttu-id="64c16-2282">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2282">0</span></span><br/>

<span data-ttu-id="64c16-2283">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2283">1</span></span>

<span data-ttu-id="64c16-2284">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2284">2</span></span>

<span data-ttu-id="64c16-2285">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2285">3</span></span>

<span data-ttu-id="64c16-2286">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2286">4</span></span>

<span data-ttu-id="64c16-2287">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2287">5</span></span>

<span data-ttu-id="64c16-2288">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2288">6</span></span>

<span data-ttu-id="64c16-2289">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2289">7</span></span>

<span data-ttu-id="64c16-2290">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2290">8</span></span>

<span data-ttu-id="64c16-2291">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2291">9</span></span>

<span data-ttu-id="64c16-2292">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2292">2</span></span><br/> <span data-ttu-id="64c16-2293">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2293">0</span></span><br/>

<span data-ttu-id="64c16-2294">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2294">1</span></span>

<span data-ttu-id="64c16-2295">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2295">2</span></span>

<span data-ttu-id="64c16-2296">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2296">3</span></span>

<span data-ttu-id="64c16-2297">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2297">4</span></span>

<span data-ttu-id="64c16-2298">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2298">5</span></span>

<span data-ttu-id="64c16-2299">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2299">6</span></span>

<span data-ttu-id="64c16-2300">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2300">7</span></span>

<span data-ttu-id="64c16-2301">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2301">8</span></span>

<span data-ttu-id="64c16-2302">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2302">9</span></span>

<span data-ttu-id="64c16-2303">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2303">3</span></span><br/> <span data-ttu-id="64c16-2304">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2304">0</span></span><br/>

<span data-ttu-id="64c16-2305">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2305">1</span></span>

<span data-ttu-id="64c16-2306">Citblchapt</span><span class="sxs-lookup"><span data-stu-id="64c16-2306">CiTblChapt</span></span>

<span data-ttu-id="64c16-2307">\_hregion</span><span class="sxs-lookup"><span data-stu-id="64c16-2307">\_hRegion</span></span>

<span data-ttu-id="64c16-2308">\_cskip</span><span class="sxs-lookup"><span data-stu-id="64c16-2308">\_cskip</span></span>



 

<span data-ttu-id="64c16-2309">**Citblchapt**: Vorzeichen lose 32-Bit-Ganzzahl, die das Rowset-Kapitel angibt, aus dem Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2309">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="64c16-2310">**\_ hregion**: muss auf 0x00000000 festgelegt werden und muss ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2310">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="64c16-2311">**\_ cskip**: unsignierte 32-Bit-Ganzzahl, die die Anzahl der Zeilen darstellt, die im Rowset übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2311">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="64c16-2312">2.2.1.28 crowsetproperties</span><span class="sxs-lookup"><span data-stu-id="64c16-2312">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="64c16-2313">Die crowsetproperties-Struktur enthält Konfigurationsinformationen für eine Abfrage.</span><span class="sxs-lookup"><span data-stu-id="64c16-2313">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="64c16-2314">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2314">0</span></span>

<span data-ttu-id="64c16-2315">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2315">1</span></span>

<span data-ttu-id="64c16-2316">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2316">2</span></span>

<span data-ttu-id="64c16-2317">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2317">3</span></span>

<span data-ttu-id="64c16-2318">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2318">4</span></span>

<span data-ttu-id="64c16-2319">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2319">5</span></span>

<span data-ttu-id="64c16-2320">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2320">6</span></span>

<span data-ttu-id="64c16-2321">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2321">7</span></span>

<span data-ttu-id="64c16-2322">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2322">8</span></span>

<span data-ttu-id="64c16-2323">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2323">9</span></span>

<span data-ttu-id="64c16-2324">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2324">1</span></span><br/> <span data-ttu-id="64c16-2325">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2325">0</span></span><br/>

<span data-ttu-id="64c16-2326">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2326">1</span></span>

<span data-ttu-id="64c16-2327">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2327">2</span></span>

<span data-ttu-id="64c16-2328">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2328">3</span></span>

<span data-ttu-id="64c16-2329">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2329">4</span></span>

<span data-ttu-id="64c16-2330">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2330">5</span></span>

<span data-ttu-id="64c16-2331">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2331">6</span></span>

<span data-ttu-id="64c16-2332">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2332">7</span></span>

<span data-ttu-id="64c16-2333">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2333">8</span></span>

<span data-ttu-id="64c16-2334">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2334">9</span></span>

<span data-ttu-id="64c16-2335">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2335">2</span></span><br/> <span data-ttu-id="64c16-2336">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2336">0</span></span><br/>

<span data-ttu-id="64c16-2337">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2337">1</span></span>

<span data-ttu-id="64c16-2338">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2338">2</span></span>

<span data-ttu-id="64c16-2339">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2339">3</span></span>

<span data-ttu-id="64c16-2340">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2340">4</span></span>

<span data-ttu-id="64c16-2341">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2341">5</span></span>

<span data-ttu-id="64c16-2342">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2342">6</span></span>

<span data-ttu-id="64c16-2343">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2343">7</span></span>

<span data-ttu-id="64c16-2344">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2344">8</span></span>

<span data-ttu-id="64c16-2345">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2345">9</span></span>

<span data-ttu-id="64c16-2346">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2346">3</span></span><br/> <span data-ttu-id="64c16-2347">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2347">0</span></span><br/>

<span data-ttu-id="64c16-2348">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2348">1</span></span>

<span data-ttu-id="64c16-2349">\_ubooleanoptions</span><span class="sxs-lookup"><span data-stu-id="64c16-2349">\_uBooleanOptions</span></span>

<span data-ttu-id="64c16-2350">\_ulmaxopenrows</span><span class="sxs-lookup"><span data-stu-id="64c16-2350">\_ulMaxOpenRows</span></span>

<span data-ttu-id="64c16-2351">\_ulmemoryusage</span><span class="sxs-lookup"><span data-stu-id="64c16-2351">\_ulMemoryUsage</span></span>

<span data-ttu-id="64c16-2352">\_cmaxresults</span><span class="sxs-lookup"><span data-stu-id="64c16-2352">\_cMaxResults</span></span>

<span data-ttu-id="64c16-2353">\_ccmdtimeout</span><span class="sxs-lookup"><span data-stu-id="64c16-2353">\_cCmdTimeout</span></span>



 

<span data-ttu-id="64c16-2354">**\_ ubooleanoptions**: die am wenigsten wichtigen 3 Bits dieses Felds müssen einen der folgenden drei Werte enthalten:</span><span class="sxs-lookup"><span data-stu-id="64c16-2354">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="64c16-2355">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-2355">Value</span></span>                  | <span data-ttu-id="64c16-2356">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-2356">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="64c16-2357">esequential 0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-2357">eSequential 0x00000001</span></span> | <span data-ttu-id="64c16-2358">Der Cursor kann nur vorwärts verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2358">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="64c16-2359">elocabel 0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-2359">eLocatable 0x00000003</span></span>  | <span data-ttu-id="64c16-2360">Der Cursor kann an eine beliebige Position verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2360">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="64c16-2361">escrollable 0x00000007</span><span class="sxs-lookup"><span data-stu-id="64c16-2361">eScrollable 0x00000007</span></span> | <span data-ttu-id="64c16-2362">Der Cursor kann an eine beliebige Position verschoben und in beliebiger Richtung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2362">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="64c16-2363">Die übrigen Bits sind entweder eindeutig oder können auf eine beliebige Kombination der folgenden Werte logisch oder zusammengesetzt werden:</span><span class="sxs-lookup"><span data-stu-id="64c16-2363">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="64c16-2364">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-2364">Value</span></span>                     | <span data-ttu-id="64c16-2365">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-2365">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-2366">easynchronous 0x00000008</span><span class="sxs-lookup"><span data-stu-id="64c16-2366">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="64c16-2367">Der Client wartet nicht auf den Abschluss der Ausführung.</span><span class="sxs-lookup"><span data-stu-id="64c16-2367">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="64c16-2368">efirstrows 0x00000080</span><span class="sxs-lookup"><span data-stu-id="64c16-2368">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="64c16-2369">Gibt die ersten gefundenen Zeilen zurück, nicht die besten Übereinstimmungen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2369">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="64c16-2370">eholdrows 0x00000200</span><span class="sxs-lookup"><span data-stu-id="64c16-2370">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="64c16-2371">Der Server darf die Zeilen erst verwerfen, wenn der Client mit einer Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-2371">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="64c16-2372">echtem 0x00000800</span><span class="sxs-lookup"><span data-stu-id="64c16-2372">eChaptered 0x00000800</span></span>     | <span data-ttu-id="64c16-2373">Das Rowset unterstützt Kapitel.</span><span class="sxs-lookup"><span data-stu-id="64c16-2373">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="64c16-2374">eueinci 0x00001000</span><span class="sxs-lookup"><span data-stu-id="64c16-2374">eUseCI 0x00001000</span></span>         | <span data-ttu-id="64c16-2375">Beantworten Sie die Abfrage nur über den Index, nicht über das Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="64c16-2375">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="64c16-2376">edeferkürzen 0x00002000</span><span class="sxs-lookup"><span data-stu-id="64c16-2376">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="64c16-2377">Der Indizierungs Dienst sollte die Reaktionszeit beim Entfernen von Ergebnissen an den Client optimieren.</span><span class="sxs-lookup"><span data-stu-id="64c16-2377">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="64c16-2378">**\_ ulmaxopenrows**: ganze Zahl ohne Vorzeichen (32 Bit).</span><span class="sxs-lookup"><span data-stu-id="64c16-2378">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="64c16-2379">Muss auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="64c16-2380">Wird nicht verwendet und muss ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="64c16-2381">**\_ ulmemoryusage**: ganze Zahl ohne Vorzeichen (32 Bit).</span><span class="sxs-lookup"><span data-stu-id="64c16-2381">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="64c16-2382">Muss auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2382">Must be set to 0x00000000.</span></span> <span data-ttu-id="64c16-2383">Wird nicht verwendet und muss ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2383">Not used and MUST be ignored.</span></span>

<span data-ttu-id="64c16-2384">**\_ cmaxresults**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die maximale Anzahl von Zeilen angibt, die für die Abfrage zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2384">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="64c16-2385">**\_ ccmdtimeout**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Sekunden angibt, nach der eine Abfrage ein Timeout und eine automatische Beendigung der Abfrage angibt, die von dem Zeitpunkt der Ausführung der Abfrage auf dem Server gezählt wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-2385">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="64c16-2386">Der Wert 0x00000000 bedeutet, dass für die Abfrage kein Timeout auftritt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2386">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="64c16-2387">2.2.1.29 crowvariant</span><span class="sxs-lookup"><span data-stu-id="64c16-2387">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="64c16-2388">Die crowvariant-Struktur enthält den Teil mit fester Größe eines Datentyps variabler Länge, der in der cpmgetrowsout-Nachricht gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-2388">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="64c16-2389">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2389">0</span></span>

<span data-ttu-id="64c16-2390">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2390">1</span></span>

<span data-ttu-id="64c16-2391">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2391">2</span></span>

<span data-ttu-id="64c16-2392">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2392">3</span></span>

<span data-ttu-id="64c16-2393">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2393">4</span></span>

<span data-ttu-id="64c16-2394">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2394">5</span></span>

<span data-ttu-id="64c16-2395">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2395">6</span></span>

<span data-ttu-id="64c16-2396">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2396">7</span></span>

<span data-ttu-id="64c16-2397">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2397">8</span></span>

<span data-ttu-id="64c16-2398">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2398">9</span></span>

<span data-ttu-id="64c16-2399">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2399">1</span></span><br/> <span data-ttu-id="64c16-2400">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2400">0</span></span><br/>

<span data-ttu-id="64c16-2401">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2401">1</span></span>

<span data-ttu-id="64c16-2402">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2402">2</span></span>

<span data-ttu-id="64c16-2403">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2403">3</span></span>

<span data-ttu-id="64c16-2404">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2404">4</span></span>

<span data-ttu-id="64c16-2405">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2405">5</span></span>

<span data-ttu-id="64c16-2406">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2406">6</span></span>

<span data-ttu-id="64c16-2407">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2407">7</span></span>

<span data-ttu-id="64c16-2408">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2408">8</span></span>

<span data-ttu-id="64c16-2409">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2409">9</span></span>

<span data-ttu-id="64c16-2410">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2410">2</span></span><br/> <span data-ttu-id="64c16-2411">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2411">0</span></span><br/>

<span data-ttu-id="64c16-2412">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2412">1</span></span>

<span data-ttu-id="64c16-2413">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2413">2</span></span>

<span data-ttu-id="64c16-2414">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2414">3</span></span>

<span data-ttu-id="64c16-2415">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2415">4</span></span>

<span data-ttu-id="64c16-2416">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2416">5</span></span>

<span data-ttu-id="64c16-2417">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2417">6</span></span>

<span data-ttu-id="64c16-2418">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2418">7</span></span>

<span data-ttu-id="64c16-2419">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2419">8</span></span>

<span data-ttu-id="64c16-2420">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2420">9</span></span>

<span data-ttu-id="64c16-2421">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2421">3</span></span><br/> <span data-ttu-id="64c16-2422">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2422">0</span></span><br/>

<span data-ttu-id="64c16-2423">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2423">1</span></span>

<span data-ttu-id="64c16-2424">VType</span><span class="sxs-lookup"><span data-stu-id="64c16-2424">vType</span></span>

<span data-ttu-id="64c16-2425">"reserved1"</span><span class="sxs-lookup"><span data-stu-id="64c16-2425">reserved1</span></span>

<span data-ttu-id="64c16-2426">reserved2</span><span class="sxs-lookup"><span data-stu-id="64c16-2426">reserved2</span></span>

<span data-ttu-id="64c16-2427">Offset (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-2427">Offset (optional)</span></span>



 

<span data-ttu-id="64c16-2428">**VType**: ein Typindikator, der den Typ von vValue angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2428">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="64c16-2429">Dabei muss es sich um einen der varenumum-Werte handeln, die im Abschnitt 2.2.1.1 angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-2429">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="64c16-2430">**"reserved1"**: nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-2430">**reserved1**: Not used.</span></span> <span data-ttu-id="64c16-2431">Der Wert kann auf einen beliebigen Wert festgelegt werden, und er muss beim Empfang ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2431">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="64c16-2432">**"reserved2"**: nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-2432">**reserved2**: Not used.</span></span> <span data-ttu-id="64c16-2433">Der Wert kann auf einen beliebigen Wert festgelegt werden, und er muss beim Empfang ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2433">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="64c16-2434">**Offset**: ein Offset zu Daten variabler Länge (z. b. eine Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="64c16-2434">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="64c16-2435">Dies muss ein 32-Bit-Wert (4 Bytes) sein, wenn 32-Bit-Offsets (gemäß den Regeln im Abschnitt 2.2.3.16) verwendet werden, oder ein 64-Byte-Wert (8 Bytes lang), wenn 64-Bit-Offsets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2435">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="64c16-2436">2.2.1.30 csortset</span><span class="sxs-lookup"><span data-stu-id="64c16-2436">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="64c16-2437">Die csortset-Struktur enthält die Sortierreihenfolge der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="64c16-2437">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="64c16-2438">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2438">0</span></span>

<span data-ttu-id="64c16-2439">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2439">1</span></span>

<span data-ttu-id="64c16-2440">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2440">2</span></span>

<span data-ttu-id="64c16-2441">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2441">3</span></span>

<span data-ttu-id="64c16-2442">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2442">4</span></span>

<span data-ttu-id="64c16-2443">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2443">5</span></span>

<span data-ttu-id="64c16-2444">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2444">6</span></span>

<span data-ttu-id="64c16-2445">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2445">7</span></span>

<span data-ttu-id="64c16-2446">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2446">8</span></span>

<span data-ttu-id="64c16-2447">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2447">9</span></span>

<span data-ttu-id="64c16-2448">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2448">1</span></span><br/> <span data-ttu-id="64c16-2449">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2449">0</span></span><br/>

<span data-ttu-id="64c16-2450">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2450">1</span></span>

<span data-ttu-id="64c16-2451">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2451">2</span></span>

<span data-ttu-id="64c16-2452">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2452">3</span></span>

<span data-ttu-id="64c16-2453">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2453">4</span></span>

<span data-ttu-id="64c16-2454">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2454">5</span></span>

<span data-ttu-id="64c16-2455">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2455">6</span></span>

<span data-ttu-id="64c16-2456">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2456">7</span></span>

<span data-ttu-id="64c16-2457">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2457">8</span></span>

<span data-ttu-id="64c16-2458">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2458">9</span></span>

<span data-ttu-id="64c16-2459">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2459">2</span></span><br/> <span data-ttu-id="64c16-2460">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2460">0</span></span><br/>

<span data-ttu-id="64c16-2461">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2461">1</span></span>

<span data-ttu-id="64c16-2462">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2462">2</span></span>

<span data-ttu-id="64c16-2463">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2463">3</span></span>

<span data-ttu-id="64c16-2464">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2464">4</span></span>

<span data-ttu-id="64c16-2465">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2465">5</span></span>

<span data-ttu-id="64c16-2466">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2466">6</span></span>

<span data-ttu-id="64c16-2467">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2467">7</span></span>

<span data-ttu-id="64c16-2468">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2468">8</span></span>

<span data-ttu-id="64c16-2469">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2469">9</span></span>

<span data-ttu-id="64c16-2470">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2470">3</span></span><br/> <span data-ttu-id="64c16-2471">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2471">0</span></span><br/>

<span data-ttu-id="64c16-2472">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2472">1</span></span>

<span data-ttu-id="64c16-2473">Anzahl</span><span class="sxs-lookup"><span data-stu-id="64c16-2473">Count</span></span>

<span data-ttu-id="64c16-2474">SortArray (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-2474">sortArray (variable)</span></span>



 

<span data-ttu-id="64c16-2475">**count**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente in SortArray angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2475">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="64c16-2476">**SortArray**: ein Array von csort-Strukturen, die die Reihenfolge beschreiben, in der die Ergebnisse der Abfrage sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2476">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="64c16-2477">Strukturen im Array müssen durch 0 bis 3 Auffüll Zeichen voneinander getrennt werden, sodass jede Struktur über eine 4-Byte-Ausrichtung ab dem Anfang einer Nachricht verfügt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2477">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="64c16-2478">Bei solchen Füll Zeichen kann es sich um beliebige Werte handeln, die bei der Bestätigung ignoriert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2478">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="64c16-2479">2.2.1.31 ctablecolumn</span><span class="sxs-lookup"><span data-stu-id="64c16-2479">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="64c16-2480">Die ctablecolumn-Struktur enthält eine Spalte einer cpmsetbindingsin-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-2480">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="64c16-2481">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2481">0</span></span>

<span data-ttu-id="64c16-2482">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2482">1</span></span>

<span data-ttu-id="64c16-2483">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2483">2</span></span>

<span data-ttu-id="64c16-2484">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2484">3</span></span>

<span data-ttu-id="64c16-2485">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2485">4</span></span>

<span data-ttu-id="64c16-2486">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2486">5</span></span>

<span data-ttu-id="64c16-2487">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2487">6</span></span>

<span data-ttu-id="64c16-2488">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2488">7</span></span>

<span data-ttu-id="64c16-2489">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2489">8</span></span>

<span data-ttu-id="64c16-2490">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2490">9</span></span>

<span data-ttu-id="64c16-2491">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2491">1</span></span><br/> <span data-ttu-id="64c16-2492">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2492">0</span></span><br/>

<span data-ttu-id="64c16-2493">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2493">1</span></span>

<span data-ttu-id="64c16-2494">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2494">2</span></span>

<span data-ttu-id="64c16-2495">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2495">3</span></span>

<span data-ttu-id="64c16-2496">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2496">4</span></span>

<span data-ttu-id="64c16-2497">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2497">5</span></span>

<span data-ttu-id="64c16-2498">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2498">6</span></span>

<span data-ttu-id="64c16-2499">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2499">7</span></span>

<span data-ttu-id="64c16-2500">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2500">8</span></span>

<span data-ttu-id="64c16-2501">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2501">9</span></span>

<span data-ttu-id="64c16-2502">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2502">2</span></span><br/> <span data-ttu-id="64c16-2503">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2503">0</span></span><br/>

<span data-ttu-id="64c16-2504">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2504">1</span></span>

<span data-ttu-id="64c16-2505">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2505">2</span></span>

<span data-ttu-id="64c16-2506">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2506">3</span></span>

<span data-ttu-id="64c16-2507">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2507">4</span></span>

<span data-ttu-id="64c16-2508">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2508">5</span></span>

<span data-ttu-id="64c16-2509">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2509">6</span></span>

<span data-ttu-id="64c16-2510">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2510">7</span></span>

<span data-ttu-id="64c16-2511">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2511">8</span></span>

<span data-ttu-id="64c16-2512">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2512">9</span></span>

<span data-ttu-id="64c16-2513">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2513">3</span></span><br/> <span data-ttu-id="64c16-2514">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2514">0</span></span><br/>

<span data-ttu-id="64c16-2515">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2515">1</span></span>

<span data-ttu-id="64c16-2516">PROPSPEC</span><span class="sxs-lookup"><span data-stu-id="64c16-2516">PropSpec</span></span>

<span data-ttu-id="64c16-2517">... veränder</span><span class="sxs-lookup"><span data-stu-id="64c16-2517">...(variable)</span></span>

<span data-ttu-id="64c16-2518">VType</span><span class="sxs-lookup"><span data-stu-id="64c16-2518">vType</span></span>

<span data-ttu-id="64c16-2519">Valueused</span><span class="sxs-lookup"><span data-stu-id="64c16-2519">ValueUsed</span></span>

<span data-ttu-id="64c16-2520">\_padding1 (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-2520">\_padding1 (optional)</span></span>

<span data-ttu-id="64c16-2521">Valueoffset (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-2521">ValueOffset (optional)</span></span>

<span data-ttu-id="64c16-2522">Valuesize (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-2522">ValueSize (optional)</span></span>

<span data-ttu-id="64c16-2523">Status ausgewertet</span><span class="sxs-lookup"><span data-stu-id="64c16-2523">StatusUsed</span></span>

<span data-ttu-id="64c16-2524">\_padding2 (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-2524">\_padding2 (optional)</span></span>

<span data-ttu-id="64c16-2525">Status-ffset (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-2525">StatusOffset (optional)</span></span>

<span data-ttu-id="64c16-2526">Verlängert</span><span class="sxs-lookup"><span data-stu-id="64c16-2526">LengthUsed</span></span>

<span data-ttu-id="64c16-2527">\_padding3 (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-2527">\_padding3 (optional)</span></span>

<span data-ttu-id="64c16-2528">Längen Offset (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-2528">LengthOffset (optional)</span></span>



 

<span data-ttu-id="64c16-2529">**PROPSPEC**: eine cfullpropspec-Struktur, wie im Abschnitt 2.2.1.3 angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-2529">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="64c16-2530">**VType**: gibt den Typ des in der Spalte enthaltenen Daten Werts an.</span><span class="sxs-lookup"><span data-stu-id="64c16-2530">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="64c16-2531">Eine Liste der Werte für dieses Feld finden Sie im Feld "VType" im Abschnitt "2.2.1.1".</span><span class="sxs-lookup"><span data-stu-id="64c16-2531">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="64c16-2532">**Valueused**: ein 1-Byte-Feld, das auf 0x01 oder 0x00 festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="64c16-2532">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="64c16-2533">Wenn der Wert auf 0x01 festgelegt ist, wird die Spalte innerhalb der Zeile mit fester Größe übertragen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2533">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="64c16-2534">Wenn Sie auf 0x00 festgelegt ist, wird der Wert der Spalte im Abschnitt variabler Länge am Ende des Puffers übertragen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2534">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="64c16-2535">**\_ padding1**: ein 1-Byte-Feld, das vor valueoffset eingefügt werden muss, wenn valueoffset nicht bei einem geraden Offset vom Anfang der Nachricht beginnt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2535">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="64c16-2536">Der Wert dieses Byte ist willkürlich und muss ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2536">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="64c16-2537">Wenn valueused auf 0x00 festgelegt ist, darf dieses Feld nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-2537">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="64c16-2538">**Valueoffset**: eine ganze 2-Byte-Ganzzahl ohne Vorzeichen, die den Offset des Spaltenwerts in der Zeile angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2538">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="64c16-2539">Wenn valueused auf 0x00 festgelegt ist, darf dieses Feld nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-2539">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="64c16-2540">**Valuesize**: eine ganze 2-Byte-Ganzzahl ohne Vorzeichen, die die Größe des Spaltenwerts in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2540">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="64c16-2541">Wenn valueused auf 0x00 festgelegt ist, darf dieses Feld nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-2541">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="64c16-2542">**Status**: ein Byte-Feld, das auf 0x01 oder 0x00 festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="64c16-2542">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="64c16-2543">Wenn der Wert auf 0x01 festgelegt ist, wird der Status der Spalte innerhalb der Zeile übertragen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2543">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="64c16-2544">Bei 0x00 wird der Status der Spalte nicht innerhalb der Zeile übertragen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2544">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="64c16-2545">**\_ padding2**: ein 1-Byte-Feld, das vor statusoffset eingefügt werden muss, wenn das statusoffset-Feld ohne dieses Feld nicht am Anfang der Nachricht mit einem geraden Offset beginnen würde.</span><span class="sxs-lookup"><span data-stu-id="64c16-2545">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="64c16-2546">Der Wert dieses Byte ist willkürlich und muss ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2546">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="64c16-2547">Wenn "Status" auf "0x00" festgelegt ist, darf dieses Feld nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-2547">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="64c16-2548">**Statusoffset**: eine ganze 2-Byte-Ganzzahl ohne Vorzeichen, die den Offset des Spalten Status in der Zeile angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2548">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="64c16-2549">Wenn "Status" auf "0x00" festgelegt ist, darf dieses Feld nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-2549">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="64c16-2550">**Verlängert**: ein Byte-Feld, das auf 0x01 oder 0x00 festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="64c16-2550">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="64c16-2551">Wenn der Wert auf 0x01 festgelegt ist, wird die Länge der Spalte innerhalb der Zeile übertragen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2551">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="64c16-2552">Wenn 0x00, darf die Länge der Spalte nicht innerhalb der Zeile übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2552">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="64c16-2553">**\_ padding3**: ein 1-Byte-Feld, das vor dem Längen Offset eingefügt werden muss, wenn, ohne es ist, der Längen Offset nicht bei einem geraden Offset vom Anfang einer Nachricht beginnen würde.</span><span class="sxs-lookup"><span data-stu-id="64c16-2553">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="64c16-2554">Der Wert dieses Byte ist willkürlich und muss ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2554">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="64c16-2555">Wenn die Längen Verwendung auf 0x00 festgelegt ist, darf dieses Feld nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-2555">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="64c16-2556">**Längen Offset**: eine Vorzeichen lose 2-Byte-Ganzzahl, die den Offset der Spaltenlänge in der Zeile angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2556">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="64c16-2557">Wenn die Längen Verwendung auf 0x00 festgelegt ist, darf dieses Feld nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-2557">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="64c16-2558">2.2.1.32 serializedpropertyvalue</span><span class="sxs-lookup"><span data-stu-id="64c16-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="64c16-2559">Die serializedpropertyvalue-Struktur enthält einen serialisierten Wert.</span><span class="sxs-lookup"><span data-stu-id="64c16-2559">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="64c16-2560">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2560">0</span></span>

<span data-ttu-id="64c16-2561">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2561">1</span></span>

<span data-ttu-id="64c16-2562">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2562">2</span></span>

<span data-ttu-id="64c16-2563">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2563">3</span></span>

<span data-ttu-id="64c16-2564">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2564">4</span></span>

<span data-ttu-id="64c16-2565">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2565">5</span></span>

<span data-ttu-id="64c16-2566">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2566">6</span></span>

<span data-ttu-id="64c16-2567">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2567">7</span></span>

<span data-ttu-id="64c16-2568">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2568">8</span></span>

<span data-ttu-id="64c16-2569">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2569">9</span></span>

<span data-ttu-id="64c16-2570">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2570">1</span></span><br/> <span data-ttu-id="64c16-2571">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2571">0</span></span><br/>

<span data-ttu-id="64c16-2572">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2572">1</span></span>

<span data-ttu-id="64c16-2573">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2573">2</span></span>

<span data-ttu-id="64c16-2574">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2574">3</span></span>

<span data-ttu-id="64c16-2575">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2575">4</span></span>

<span data-ttu-id="64c16-2576">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2576">5</span></span>

<span data-ttu-id="64c16-2577">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2577">6</span></span>

<span data-ttu-id="64c16-2578">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2578">7</span></span>

<span data-ttu-id="64c16-2579">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2579">8</span></span>

<span data-ttu-id="64c16-2580">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2580">9</span></span>

<span data-ttu-id="64c16-2581">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2581">2</span></span><br/> <span data-ttu-id="64c16-2582">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2582">0</span></span><br/>

<span data-ttu-id="64c16-2583">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2583">1</span></span>

<span data-ttu-id="64c16-2584">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2584">2</span></span>

<span data-ttu-id="64c16-2585">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2585">3</span></span>

<span data-ttu-id="64c16-2586">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2586">4</span></span>

<span data-ttu-id="64c16-2587">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2587">5</span></span>

<span data-ttu-id="64c16-2588">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2588">6</span></span>

<span data-ttu-id="64c16-2589">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2589">7</span></span>

<span data-ttu-id="64c16-2590">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2590">8</span></span>

<span data-ttu-id="64c16-2591">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2591">9</span></span>

<span data-ttu-id="64c16-2592">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2592">3</span></span><br/> <span data-ttu-id="64c16-2593">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2593">0</span></span><br/>

<span data-ttu-id="64c16-2594">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2594">1</span></span>

<span data-ttu-id="64c16-2595">dwType</span><span class="sxs-lookup"><span data-stu-id="64c16-2595">dwType</span></span>

<span data-ttu-id="64c16-2596">RGB (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-2596">rgb (variable)</span></span>



 

<span data-ttu-id="64c16-2597">**dwType**: einer der Variant-Typen, der im Abschnitt 2.2.1.1 definiert ist und mit Varianten Typmodifizierer kombiniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="64c16-2597">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="64c16-2598">Für alle Variant-Typen, mit Ausnahme derjenigen, die mit dem VT- \_ Array kombiniert werden, hat serializedpropertyvalue dasselbe Layout wie cbasestoragevariant, wie im Abschnitt 2.2.1.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-2598">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="64c16-2599">Wenn der Variant-Typ mit dem VT \_ -Arraytypmodifizierer kombiniert wird, wird SAFEARRAY2, der in Abschnitt 2.2.1.2.1.1 angegeben wird, anstelle von SAFEARRAY im vValue-Feld von cbasestoragevariant verwendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-2599">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="64c16-2600">**RGB**: serialisierter Wert.</span><span class="sxs-lookup"><span data-stu-id="64c16-2600">**rgb**: Serialized value.</span></span> <span data-ttu-id="64c16-2601">Weitere Informationen finden Sie in den Details der Serialisierung für vValue in 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="64c16-2601">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="64c16-2602">2.2.2-Nachrichten Header</span><span class="sxs-lookup"><span data-stu-id="64c16-2602">2.2.2 Message Headers</span></span>

<span data-ttu-id="64c16-2603">Alle Protokollnachrichten für den Inhalts Indizierungs Dienst haben einen 16-Byte-Header.</span><span class="sxs-lookup"><span data-stu-id="64c16-2603">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="64c16-2604">Im folgenden finden Sie ein Diagramm, das das Format des Content Index Service Protocol Message Headers anzeigt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2604">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="64c16-2605">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2605">0</span></span>

<span data-ttu-id="64c16-2606">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2606">1</span></span>

<span data-ttu-id="64c16-2607">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2607">2</span></span>

<span data-ttu-id="64c16-2608">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2608">3</span></span>

<span data-ttu-id="64c16-2609">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2609">4</span></span>

<span data-ttu-id="64c16-2610">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2610">5</span></span>

<span data-ttu-id="64c16-2611">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2611">6</span></span>

<span data-ttu-id="64c16-2612">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2612">7</span></span>

<span data-ttu-id="64c16-2613">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2613">8</span></span>

<span data-ttu-id="64c16-2614">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2614">9</span></span>

<span data-ttu-id="64c16-2615">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2615">1</span></span><br/> <span data-ttu-id="64c16-2616">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2616">0</span></span><br/>

<span data-ttu-id="64c16-2617">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2617">1</span></span>

<span data-ttu-id="64c16-2618">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2618">2</span></span>

<span data-ttu-id="64c16-2619">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2619">3</span></span>

<span data-ttu-id="64c16-2620">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2620">4</span></span>

<span data-ttu-id="64c16-2621">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2621">5</span></span>

<span data-ttu-id="64c16-2622">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2622">6</span></span>

<span data-ttu-id="64c16-2623">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2623">7</span></span>

<span data-ttu-id="64c16-2624">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2624">8</span></span>

<span data-ttu-id="64c16-2625">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2625">9</span></span>

<span data-ttu-id="64c16-2626">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2626">2</span></span><br/> <span data-ttu-id="64c16-2627">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2627">0</span></span><br/>

<span data-ttu-id="64c16-2628">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2628">1</span></span>

<span data-ttu-id="64c16-2629">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2629">2</span></span>

<span data-ttu-id="64c16-2630">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2630">3</span></span>

<span data-ttu-id="64c16-2631">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2631">4</span></span>

<span data-ttu-id="64c16-2632">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2632">5</span></span>

<span data-ttu-id="64c16-2633">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2633">6</span></span>

<span data-ttu-id="64c16-2634">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2634">7</span></span>

<span data-ttu-id="64c16-2635">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2635">8</span></span>

<span data-ttu-id="64c16-2636">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2636">9</span></span>

<span data-ttu-id="64c16-2637">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2637">3</span></span><br/> <span data-ttu-id="64c16-2638">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2638">0</span></span><br/>

<span data-ttu-id="64c16-2639">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2639">1</span></span>

<span data-ttu-id="64c16-2640">\_Meldung</span><span class="sxs-lookup"><span data-stu-id="64c16-2640">\_msg</span></span>

<span data-ttu-id="64c16-2641">\_Stands</span><span class="sxs-lookup"><span data-stu-id="64c16-2641">\_status</span></span>

<span data-ttu-id="64c16-2642">\_ulchecksum</span><span class="sxs-lookup"><span data-stu-id="64c16-2642">\_ulChecksum</span></span>

<span data-ttu-id="64c16-2643">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="64c16-2643">\_ulReserved2</span></span>



 

<span data-ttu-id="64c16-2644">\_**msg**: eine 32-Bit-Ganzzahl, die den Typ der Nachricht angibt, die auf den Header folgt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2644">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="64c16-2645">In der folgenden Tabelle werden die Protokollnachrichten für den Inhalts Indizierungs Dienst und die für jede Nachricht angegebenen ganzzahligen Werte aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="64c16-2645">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="64c16-2646">Wie in der Tabelle gezeigt, identifizieren einige Werte zwei Nachrichten in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="64c16-2646">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="64c16-2647">In diesen Fällen kann die Nachricht, die auf den Header folgt, durch die Richtung des Nachrichten Flusses identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2647">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="64c16-2648">Wenn die Richtung "Client zu Server" lautet, wird die Meldung mit dem Namen "in" angezeigt, die an den Nachrichten Namen angehängt ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-2648">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="64c16-2649">Wenn die Richtung Server zu Client ist, wird die Meldung mit dem Namen "out" angezeigt, die an den Nachrichten Namen angehängt ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-2649">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="64c16-2650">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-2650">Value</span></span>      | <span data-ttu-id="64c16-2651">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-2651">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="64c16-2652">0x000000c8</span><span class="sxs-lookup"><span data-stu-id="64c16-2652">0x000000C8</span></span> | <span data-ttu-id="64c16-2653">Cpmconnectin oder cpmconnectout</span><span class="sxs-lookup"><span data-stu-id="64c16-2653">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="64c16-2654">0x000000c9</span><span class="sxs-lookup"><span data-stu-id="64c16-2654">0x000000C9</span></span> | <span data-ttu-id="64c16-2655">Cpmdisconnect</span><span class="sxs-lookup"><span data-stu-id="64c16-2655">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="64c16-2656">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="64c16-2656">0x000000CA</span></span> | <span data-ttu-id="64c16-2657">Cpmkreatequeryin oder cpmkreatequeryout</span><span class="sxs-lookup"><span data-stu-id="64c16-2657">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="64c16-2658">0x000000cb</span><span class="sxs-lookup"><span data-stu-id="64c16-2658">0x000000CB</span></span> | <span data-ttu-id="64c16-2659">Cpmfreecursorin oder cpmfreecursorout</span><span class="sxs-lookup"><span data-stu-id="64c16-2659">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="64c16-2660">0x000000cc</span><span class="sxs-lookup"><span data-stu-id="64c16-2660">0x000000CC</span></span> | <span data-ttu-id="64c16-2661">Cpmgetrowsin oder cpmgetrowsout</span><span class="sxs-lookup"><span data-stu-id="64c16-2661">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="64c16-2662">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="64c16-2662">0x000000CD</span></span> | <span data-ttu-id="64c16-2663">Cpmratiofinishedin oder cpmratiofinishedout</span><span class="sxs-lookup"><span data-stu-id="64c16-2663">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="64c16-2664">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="64c16-2664">0x000000CE</span></span> | <span data-ttu-id="64c16-2665">Cpmcomparebmkin oder cpmcomparebmkout</span><span class="sxs-lookup"><span data-stu-id="64c16-2665">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="64c16-2666">0x000000cf</span><span class="sxs-lookup"><span data-stu-id="64c16-2666">0x000000CF</span></span> | <span data-ttu-id="64c16-2667">Cpmgetapproximatepositionin oder cpmgetapproximatepositionout</span><span class="sxs-lookup"><span data-stu-id="64c16-2667">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="64c16-2668">0x000000d0</span><span class="sxs-lookup"><span data-stu-id="64c16-2668">0x000000D0</span></span> | <span data-ttu-id="64c16-2669">Cpmsetbindingsin</span><span class="sxs-lookup"><span data-stu-id="64c16-2669">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="64c16-2670">0x000000D1</span><span class="sxs-lookup"><span data-stu-id="64c16-2670">0x000000D1</span></span> | <span data-ttu-id="64c16-2671">Cpmgetnotify</span><span class="sxs-lookup"><span data-stu-id="64c16-2671">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="64c16-2672">0x000000d2</span><span class="sxs-lookup"><span data-stu-id="64c16-2672">0x000000D2</span></span> | <span data-ttu-id="64c16-2673">Cpmsendnotimayout</span><span class="sxs-lookup"><span data-stu-id="64c16-2673">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="64c16-2674">0x000000d7</span><span class="sxs-lookup"><span data-stu-id="64c16-2674">0x000000D7</span></span> | <span data-ttu-id="64c16-2675">Cpmgetquerystatus oder cpmgetquerystatus</span><span class="sxs-lookup"><span data-stu-id="64c16-2675">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="64c16-2676">0x000000d9</span><span class="sxs-lookup"><span data-stu-id="64c16-2676">0x000000D9</span></span> | <span data-ttu-id="64c16-2677">Cpmcistatus out</span><span class="sxs-lookup"><span data-stu-id="64c16-2677">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="64c16-2678">0x000000e1</span><span class="sxs-lookup"><span data-stu-id="64c16-2678">0x000000E1</span></span> | <span data-ttu-id="64c16-2679">Cpmforcemergein</span><span class="sxs-lookup"><span data-stu-id="64c16-2679">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="64c16-2680">0x000000e4</span><span class="sxs-lookup"><span data-stu-id="64c16-2680">0x000000E4</span></span> | <span data-ttu-id="64c16-2681">Cpmfetchvaluein oder cpmfetchvalueout</span><span class="sxs-lookup"><span data-stu-id="64c16-2681">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="64c16-2682">0x000000e6</span><span class="sxs-lookup"><span data-stu-id="64c16-2682">0x000000E6</span></span> | <span data-ttu-id="64c16-2683">Cpmupdatedocumentsin</span><span class="sxs-lookup"><span data-stu-id="64c16-2683">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="64c16-2684">0x000000e7</span><span class="sxs-lookup"><span data-stu-id="64c16-2684">0x000000E7</span></span> | <span data-ttu-id="64c16-2685">Cpmgetquerystatusexin oder pmgetquerystatusexout</span><span class="sxs-lookup"><span data-stu-id="64c16-2685">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="64c16-2686">0x000000e8</span><span class="sxs-lookup"><span data-stu-id="64c16-2686">0x000000E8</span></span> | <span data-ttu-id="64c16-2687">Cpmrestartpositionin</span><span class="sxs-lookup"><span data-stu-id="64c16-2687">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="64c16-2688">0x000000e9</span><span class="sxs-lookup"><span data-stu-id="64c16-2688">0x000000E9</span></span> | <span data-ttu-id="64c16-2689">Cpmstopasynchin</span><span class="sxs-lookup"><span data-stu-id="64c16-2689">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="64c16-2690">0x000000ec</span><span class="sxs-lookup"><span data-stu-id="64c16-2690">0x000000EC</span></span> | <span data-ttu-id="64c16-2691">Cpmsetsestatein oder cpmset-stateout</span><span class="sxs-lookup"><span data-stu-id="64c16-2691">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="64c16-2692">\_**Status**: ein HRESULT \[ ms-sys \] , das den Status des angeforderten Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2692">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="64c16-2693">*Windows-Verhalten: der Client legt das \_ Feld "Status" immer auf "0x00000000" fest.*</span><span class="sxs-lookup"><span data-stu-id="64c16-2693">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="64c16-2694">**\_ ulchecksum**: die \_ ulchecksum-Angabe muss in Abschnitt 3.2.4 für die folgenden Meldungen berechnet werden:</span><span class="sxs-lookup"><span data-stu-id="64c16-2694">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="64c16-2695">Cpmconnectin</span><span class="sxs-lookup"><span data-stu-id="64c16-2695">CPMConnectIn</span></span>
-   <span data-ttu-id="64c16-2696">Cpmkreatequeryin</span><span class="sxs-lookup"><span data-stu-id="64c16-2696">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="64c16-2697">Cpmsetbindingsin</span><span class="sxs-lookup"><span data-stu-id="64c16-2697">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="64c16-2698">Cpmgetrowsin</span><span class="sxs-lookup"><span data-stu-id="64c16-2698">CPMGetRowsIn</span></span>
-   <span data-ttu-id="64c16-2699">Cpmfetchvaluein</span><span class="sxs-lookup"><span data-stu-id="64c16-2699">CPMFetchValueIn</span></span>

<span data-ttu-id="64c16-2700">Für alle anderen Nachrichten \_ muss ulchecksum auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2700">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="64c16-2701">Ein Client muss das \_ ulchecksum-Feld ignorieren.</span><span class="sxs-lookup"><span data-stu-id="64c16-2701">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="64c16-2702">**\_ ulReserved2**: muss auf 0 festgelegt und vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2702">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="64c16-2703">2.2.3 Nachrichten</span><span class="sxs-lookup"><span data-stu-id="64c16-2703">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="64c16-2704">2.2.3.1 cpmcistatus out</span><span class="sxs-lookup"><span data-stu-id="64c16-2704">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="64c16-2705">Die cpmcistateinout-Nachricht enthält Informationen zum Status des Indizierungs Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="64c16-2705">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="64c16-2706">Das Format der cpmcistateinout-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-2706">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="64c16-2707">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2707">0</span></span>

<span data-ttu-id="64c16-2708">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2708">1</span></span>

<span data-ttu-id="64c16-2709">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2709">2</span></span>

<span data-ttu-id="64c16-2710">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2710">3</span></span>

<span data-ttu-id="64c16-2711">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2711">4</span></span>

<span data-ttu-id="64c16-2712">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2712">5</span></span>

<span data-ttu-id="64c16-2713">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2713">6</span></span>

<span data-ttu-id="64c16-2714">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2714">7</span></span>

<span data-ttu-id="64c16-2715">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2715">8</span></span>

<span data-ttu-id="64c16-2716">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2716">9</span></span>

<span data-ttu-id="64c16-2717">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2717">1</span></span><br/> <span data-ttu-id="64c16-2718">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2718">0</span></span><br/>

<span data-ttu-id="64c16-2719">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2719">1</span></span>

<span data-ttu-id="64c16-2720">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2720">2</span></span>

<span data-ttu-id="64c16-2721">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2721">3</span></span>

<span data-ttu-id="64c16-2722">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2722">4</span></span>

<span data-ttu-id="64c16-2723">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2723">5</span></span>

<span data-ttu-id="64c16-2724">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2724">6</span></span>

<span data-ttu-id="64c16-2725">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2725">7</span></span>

<span data-ttu-id="64c16-2726">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2726">8</span></span>

<span data-ttu-id="64c16-2727">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2727">9</span></span>

<span data-ttu-id="64c16-2728">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2728">2</span></span><br/> <span data-ttu-id="64c16-2729">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2729">0</span></span><br/>

<span data-ttu-id="64c16-2730">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2730">1</span></span>

<span data-ttu-id="64c16-2731">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2731">2</span></span>

<span data-ttu-id="64c16-2732">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2732">3</span></span>

<span data-ttu-id="64c16-2733">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2733">4</span></span>

<span data-ttu-id="64c16-2734">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2734">5</span></span>

<span data-ttu-id="64c16-2735">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2735">6</span></span>

<span data-ttu-id="64c16-2736">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2736">7</span></span>

<span data-ttu-id="64c16-2737">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2737">8</span></span>

<span data-ttu-id="64c16-2738">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2738">9</span></span>

<span data-ttu-id="64c16-2739">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2739">3</span></span><br/> <span data-ttu-id="64c16-2740">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2740">0</span></span><br/>

<span data-ttu-id="64c16-2741">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2741">1</span></span>

<span data-ttu-id="64c16-2742">cbStruct</span><span class="sxs-lookup"><span data-stu-id="64c16-2742">cbStruct</span></span>

<span data-ttu-id="64c16-2743">cwordlist</span><span class="sxs-lookup"><span data-stu-id="64c16-2743">cWordList</span></span>

<span data-ttu-id="64c16-2744">cpersistentindex</span><span class="sxs-lookup"><span data-stu-id="64c16-2744">cPersistentIndex</span></span>

<span data-ttu-id="64c16-2745">cqueries</span><span class="sxs-lookup"><span data-stu-id="64c16-2745">cQueries</span></span>

<span data-ttu-id="64c16-2746">CDocuments</span><span class="sxs-lookup"><span data-stu-id="64c16-2746">cDocuments</span></span>

<span data-ttu-id="64c16-2747">cfreshtest</span><span class="sxs-lookup"><span data-stu-id="64c16-2747">cFreshTest</span></span>

<span data-ttu-id="64c16-2748">dwmergeprogress</span><span class="sxs-lookup"><span data-stu-id="64c16-2748">dwMergeProgress</span></span>

<span data-ttu-id="64c16-2749">gut</span><span class="sxs-lookup"><span data-stu-id="64c16-2749">eState</span></span>

<span data-ttu-id="64c16-2750">cfiltereddocuments</span><span class="sxs-lookup"><span data-stu-id="64c16-2750">cFilteredDocuments</span></span>

<span data-ttu-id="64c16-2751">ctotaldocuments</span><span class="sxs-lookup"><span data-stu-id="64c16-2751">cTotalDocuments</span></span>

<span data-ttu-id="64c16-2752">cpdingscans</span><span class="sxs-lookup"><span data-stu-id="64c16-2752">cPendingScans</span></span>

<span data-ttu-id="64c16-2753">dwindexsize</span><span class="sxs-lookup"><span data-stu-id="64c16-2753">dwIndexSize</span></span>

<span data-ttu-id="64c16-2754">cuniquekeys</span><span class="sxs-lookup"><span data-stu-id="64c16-2754">cUniqueKeys</span></span>

<span data-ttu-id="64c16-2755">csecqdocuments</span><span class="sxs-lookup"><span data-stu-id="64c16-2755">cSecQDocuments</span></span>

<span data-ttu-id="64c16-2756">dwpropcachesize</span><span class="sxs-lookup"><span data-stu-id="64c16-2756">dwPropCacheSize</span></span>



 

<span data-ttu-id="64c16-2757">**cbStruct**: eine 32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2757">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="64c16-2758">Die Größe dieser Nachricht in Bytes (mit Ausnahme des allgemeinen Headers).</span><span class="sxs-lookup"><span data-stu-id="64c16-2758">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="64c16-2759">Muss auf 0x0000003c festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2759">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="64c16-2760">**cwordlist**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der anfänglichen Indizes angibt, die für zuletzt indizierte Dokumente erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2760">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="64c16-2761">**cpersistentindex**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der persistenten Indizes angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2761">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="64c16-2762">**cqueries**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die eine Reihe von aktiv ausgelaufenden Abfragen angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2762">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="64c16-2763">**CDocuments**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Dokumente angibt, die auf die Indizierung warten.</span><span class="sxs-lookup"><span data-stu-id="64c16-2763">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="64c16-2764">**cfreshtest**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von eindeutigen Dokumenten mit Informationen in Indizes angibt, die nicht vollständig für die Leistung optimiert sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-2764">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="64c16-2765">**dwmergeprogress**: Vorzeichen lose 32-Bit-Ganzzahl ohne Vorzeichen, die den Abschluss Prozentsatz der aktuellen vollständigen Optimierung von Indizes angibt, wenn die Optimierung derzeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-2765">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="64c16-2766">Muss kleiner oder gleich 100 sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-2766">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="64c16-2767">**eState**: Zustand der Inhalts Indizierung, wie von einer oder mehreren der CI- \_ Zustands \_ \* Konstanten angegeben, die in der folgenden Tabelle definiert sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-2767">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="64c16-2768">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-2768">Value</span></span>                                         | <span data-ttu-id="64c16-2769">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-2769">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-2770">CI- \_ Zustands \_ Schatten \_ Zusammenführung 0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-2770">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="64c16-2771">Der Indizierungs Dienst wird gerade einige der Indizes optimieren, um die Speicherauslastung zu reduzieren und die Abfrageleistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="64c16-2771">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="64c16-2772">CI- \_ Status \_ Master \_ Merge 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-2772">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="64c16-2773">Der Indizierungs Dienst wird für alle Indizes vollständig optimiert.</span><span class="sxs-lookup"><span data-stu-id="64c16-2773">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="64c16-2774">CI- \_ Status- \_ Inhalts \_ Scan \_ erforderlich 0x00000004</span><span class="sxs-lookup"><span data-stu-id="64c16-2774">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="64c16-2775">Einige Dokumente im Index wurden geändert, und der Indizierungs Dienst muss bestimmen, welche hinzugefügt, geändert oder gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2775">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="64c16-2776">CI- \_ Status- \_ \_ Anfügen 0x00000008</span><span class="sxs-lookup"><span data-stu-id="64c16-2776">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="64c16-2777">Der Indizierungs Dienst optimiert Indizes, um die Speicherauslastung zu reduzieren und die Abfrageleistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="64c16-2777">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="64c16-2778">Dieser Prozess ist umfassender als der vom CI- \_ Status- \_ \_ schattenmerge-Wert identifizierte, aber er ist nicht so umfassend wie durch den CI- \_ Status Master-Merge-Wert angegeben \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-2778">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="64c16-2779">Solche Optimierungen sind Implementierungs spezifisch, da Sie von der internen Speicherung von Daten abhängen. die Optimierungen wirken sich nicht auf das Protokoll in anderer Weise aus als der Antwortzeit.</span><span class="sxs-lookup"><span data-stu-id="64c16-2779">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="64c16-2780">CI- \_ Status Überprüfung \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="64c16-2780">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="64c16-2781">Der Indizierungs Dienst untersucht ein Verzeichnis oder eine Gruppe von Verzeichnissen, um zu ermitteln, ob seit der letzten Indizierung des Verzeichnisses Dateien hinzugefügt, gelöscht oder aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2781">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="64c16-2782">CI-Status bei wieder \_ \_ Herstellung von 0x00000020</span><span class="sxs-lookup"><span data-stu-id="64c16-2782">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="64c16-2783">Der Dienst beginnt mit dem zuletzt gespeicherten Zustand und wird gerade wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2783">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="64c16-2784">CI- \_ Status \_ wenig Arbeits \_ Speicher 0x00000080</span><span class="sxs-lookup"><span data-stu-id="64c16-2784">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="64c16-2785">Der größte Teil des virtuellen Speichers des Servers wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-2785">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="64c16-2786">CI-Status hoch-e/a \_ \_ \_ 0x00000100</span><span class="sxs-lookup"><span data-stu-id="64c16-2786">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="64c16-2787">Die Ebene der Eingabe-/Ausgabeaktivität (e/a) auf dem Server ist relativ hoch.</span><span class="sxs-lookup"><span data-stu-id="64c16-2787">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="64c16-2788">CI- \_ Status \_ Master \_ Zusammenführung \_ angehalten 0x00000200</span><span class="sxs-lookup"><span data-stu-id="64c16-2788">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="64c16-2789">Der Prozess der vollständigen Optimierung für alle Indizes, die gerade ausgeführt wurden, wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="64c16-2789">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="64c16-2790">Dies wird nur für informative Zwecke angegeben und wirkt sich nicht auf CISP aus.</span><span class="sxs-lookup"><span data-stu-id="64c16-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="64c16-2791">CI-Status schreibgeschützt \_ \_ \_ 0x00000400</span><span class="sxs-lookup"><span data-stu-id="64c16-2791">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="64c16-2792">Der Teil des Indizierungs Dienstanbieter, der neue Dokumente für die Indexerstellung aufnimmt, wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="64c16-2792">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="64c16-2793">Dies wird nur für informative Zwecke angegeben und wirkt sich nicht auf CISP aus.</span><span class="sxs-lookup"><span data-stu-id="64c16-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="64c16-2794">CI- \_ State \_ Akku \_ Power 0x00000800</span><span class="sxs-lookup"><span data-stu-id="64c16-2794">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="64c16-2795">Der Teil des Indizierungs Dienstanbieter, der neue Dokumente für die Indexerstellung aufnimmt, wurde angehalten, um die Akku Lebensdauer zu sparen, aber dennoch Antworten auf die Abfragen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2795">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="64c16-2796">Dies wird nur für informative Zwecke angegeben und wirkt sich nicht auf CISP aus.</span><span class="sxs-lookup"><span data-stu-id="64c16-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="64c16-2797">CI- \_ Status \_ Benutzer \_ aktiv 0x00001000</span><span class="sxs-lookup"><span data-stu-id="64c16-2797">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="64c16-2798">Der Teil des Indizierungs Dienstanbieter, der neue Dokumente für den Index abruft, wurde aufgrund einer hohen Aktivität durch den Benutzer (Tastatur oder Maus) angehalten, antwortet aber immer noch auf die Abfragen.</span><span class="sxs-lookup"><span data-stu-id="64c16-2798">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="64c16-2799">Dies wird nur für informative Zwecke angegeben und wirkt sich nicht auf CISP aus.</span><span class="sxs-lookup"><span data-stu-id="64c16-2799">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="64c16-2800">CI- \_ Status \_ beginnend 0x00002000</span><span class="sxs-lookup"><span data-stu-id="64c16-2800">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="64c16-2801">Der Dienst wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="64c16-2801">The service is starting.</span></span> <span data-ttu-id="64c16-2802">Abfragen können ausgeführt werden, aber das Scannen und die Benachrichtigung wurden noch nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="64c16-2802">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="64c16-2803">Dies wird nur für informative Zwecke angegeben und wirkt sich nicht auf CISP aus.</span><span class="sxs-lookup"><span data-stu-id="64c16-2803">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="64c16-2804">CI- \_ Status \_ Lesen von \_ USNs 0x00004000</span><span class="sxs-lookup"><span data-stu-id="64c16-2804">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="64c16-2805">Der Dienst hat das vom Dateisystem beibehaltene Protokoll nicht gelesen, um Änderungen an Dateien oder Verzeichnissen in einem Volume nachzuverfolgen, sodass der Index möglicherweise nicht auf dem neuesten Stand ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-2805">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="64c16-2806">**cfiltereddocuments**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dokumente angibt, die seit Beginn der Inhalts Indizierung indiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2806">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="64c16-2807">**ctotaldocuments**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Dokumente im System angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2807">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="64c16-2808">**cpdingscans**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von ausstehenden Index Vorgängen auf hoher Ebene angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2808">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="64c16-2809">Die Bedeutung dieses Werts ist Anbieter spezifisch, aber größere Zahlen erwarten, dass mehr Indizierung übrig bleibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2809">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="64c16-2810">*Windows-Verhalten*: dieser Wert ist in der Regel 0 (null), mit dem Unterschied, dass die Indizierung nicht unmittelbar nach dem Start der Indizierung oder</span><span class="sxs-lookup"><span data-stu-id="64c16-2810">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="64c16-2811">**dwindexsize**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des Indexes (ohne den Eigenschafts Cache) in Megabyte angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2811">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="64c16-2812">**cuniquekeys**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die ungefähre Anzahl eindeutiger Schlüssel im Katalog angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2812">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="64c16-2813">**csecqdocuments**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dokumente angibt, die der Indizierungs Dienst aufgrund eines Fehlers während des anfänglichen Indizierungs Versuchs neu indizieren wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-2813">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="64c16-2814">**dwpropcachesize**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des Eigenschafts Caches in Megabyte angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2814">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="64c16-2815">2.2.3.2 cpmsetsestatuein</span><span class="sxs-lookup"><span data-stu-id="64c16-2815">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="64c16-2816">Die cpmsetsinstatein-Meldung legt den Status eines Katalogs fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-2816">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="64c16-2817">Das Format der cpmsetingstatein-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-2817">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="64c16-2818">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2818">0</span></span>

<span data-ttu-id="64c16-2819">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2819">1</span></span>

<span data-ttu-id="64c16-2820">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2820">2</span></span>

<span data-ttu-id="64c16-2821">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2821">3</span></span>

<span data-ttu-id="64c16-2822">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2822">4</span></span>

<span data-ttu-id="64c16-2823">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2823">5</span></span>

<span data-ttu-id="64c16-2824">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2824">6</span></span>

<span data-ttu-id="64c16-2825">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2825">7</span></span>

<span data-ttu-id="64c16-2826">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2826">8</span></span>

<span data-ttu-id="64c16-2827">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2827">9</span></span>

<span data-ttu-id="64c16-2828">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2828">1</span></span><br/> <span data-ttu-id="64c16-2829">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2829">0</span></span><br/>

<span data-ttu-id="64c16-2830">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2830">1</span></span>

<span data-ttu-id="64c16-2831">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2831">2</span></span>

<span data-ttu-id="64c16-2832">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2832">3</span></span>

<span data-ttu-id="64c16-2833">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2833">4</span></span>

<span data-ttu-id="64c16-2834">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2834">5</span></span>

<span data-ttu-id="64c16-2835">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2835">6</span></span>

<span data-ttu-id="64c16-2836">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2836">7</span></span>

<span data-ttu-id="64c16-2837">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2837">8</span></span>

<span data-ttu-id="64c16-2838">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2838">9</span></span>

<span data-ttu-id="64c16-2839">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2839">2</span></span><br/> <span data-ttu-id="64c16-2840">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2840">0</span></span><br/>

<span data-ttu-id="64c16-2841">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2841">1</span></span>

<span data-ttu-id="64c16-2842">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2842">2</span></span>

<span data-ttu-id="64c16-2843">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2843">3</span></span>

<span data-ttu-id="64c16-2844">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2844">4</span></span>

<span data-ttu-id="64c16-2845">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2845">5</span></span>

<span data-ttu-id="64c16-2846">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2846">6</span></span>

<span data-ttu-id="64c16-2847">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2847">7</span></span>

<span data-ttu-id="64c16-2848">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2848">8</span></span>

<span data-ttu-id="64c16-2849">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2849">9</span></span>

<span data-ttu-id="64c16-2850">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2850">3</span></span><br/> <span data-ttu-id="64c16-2851">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2851">0</span></span><br/>

<span data-ttu-id="64c16-2852">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2852">1</span></span>

<span data-ttu-id="64c16-2853">\_partID</span><span class="sxs-lookup"><span data-stu-id="64c16-2853">\_partID</span></span>

<span data-ttu-id="64c16-2854">\_dwnewstate</span><span class="sxs-lookup"><span data-stu-id="64c16-2854">\_dwNewState</span></span>

<span data-ttu-id="64c16-2855">\_Name der Kategorie (Variable, optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-2855">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="64c16-2856">**\_ partid**: muss auf 0x00000001 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2856">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="64c16-2857">**\_ dwnewstate**: muss auf einen der folgenden Werte festgelegt werden, um den neuen Status des Katalogs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-2857">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="64c16-2858">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-2858">Value</span></span>                         | <span data-ttu-id="64c16-2859">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-2859">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-2860">Cicat hat \_ 0x00000001 beendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-2860">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="64c16-2861">Der Katalog wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-2861">The catalog is stopped.</span></span> <span data-ttu-id="64c16-2862">Dieser Status bedeutet, dass keine neuen Dateien indiziert werden müssen, und es werden keine Such Abfragen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="64c16-2862">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="64c16-2863">Cicat schreibgeschützt \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-2863">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="64c16-2864">Der Katalog ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2864">The catalog is read-only.</span></span> <span data-ttu-id="64c16-2865">Es werden keine neuen Dateien indiziert.</span><span class="sxs-lookup"><span data-stu-id="64c16-2865">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="64c16-2866">Cicat \_ beschreibbare 0x00000004</span><span class="sxs-lookup"><span data-stu-id="64c16-2866">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="64c16-2867">Der Katalog ist beschreibbar.</span><span class="sxs-lookup"><span data-stu-id="64c16-2867">The catalog is writable.</span></span> <span data-ttu-id="64c16-2868">Neue Dateien können indiziert und Such Abfragen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2868">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="64c16-2869">Cicat \_ keine \_ Abfrage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="64c16-2869">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="64c16-2870">Der Katalog ist nicht für Abfragen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="64c16-2870">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="64c16-2871">Cicat \_ get \_ State 0x00000010</span><span class="sxs-lookup"><span data-stu-id="64c16-2871">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="64c16-2872">Der Status des Katalogs soll nicht geändert werden, sondern nur abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2872">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="64c16-2873">Cicat \_ alle \_ geöffneten 0x00000020</span><span class="sxs-lookup"><span data-stu-id="64c16-2873">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="64c16-2874">Eine Überprüfung, ob alle Kataloge gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2874">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="64c16-2875">Wenn dies der Fall ist, \_ wird das in der cpmsetsinstateout-Antwort an diese Nachricht gesendete dwoldstate-Feld als ungleich 0 (null) gemeldet.</span><span class="sxs-lookup"><span data-stu-id="64c16-2875">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="64c16-2876">" **Name": der \_** Name des Katalogs, dessen Status geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-2876">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="64c16-2877">Der Name muss eine NULL-terminierte Unicode-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-2877">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="64c16-2878">Dieses Feld muss weggelassen werden, wenn " \_ dwnewstate" auf "cicat all geöffnet" festgelegt ist \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-2878">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="64c16-2879">2.2.3.3 cpmset| stateout</span><span class="sxs-lookup"><span data-stu-id="64c16-2879">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="64c16-2880">Bei der cpmsetsinstateout-Nachricht handelt es sich um eine Antwort auf eine cpmsetsinstatein-Nachricht mit dem alten Status des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="64c16-2880">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="64c16-2881">Das Format der cpmset-stateout-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-2881">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="64c16-2882">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2882">0</span></span>

<span data-ttu-id="64c16-2883">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2883">1</span></span>

<span data-ttu-id="64c16-2884">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2884">2</span></span>

<span data-ttu-id="64c16-2885">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2885">3</span></span>

<span data-ttu-id="64c16-2886">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2886">4</span></span>

<span data-ttu-id="64c16-2887">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2887">5</span></span>

<span data-ttu-id="64c16-2888">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2888">6</span></span>

<span data-ttu-id="64c16-2889">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2889">7</span></span>

<span data-ttu-id="64c16-2890">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2890">8</span></span>

<span data-ttu-id="64c16-2891">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2891">9</span></span>

<span data-ttu-id="64c16-2892">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2892">1</span></span><br/> <span data-ttu-id="64c16-2893">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2893">0</span></span><br/>

<span data-ttu-id="64c16-2894">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2894">1</span></span>

<span data-ttu-id="64c16-2895">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2895">2</span></span>

<span data-ttu-id="64c16-2896">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2896">3</span></span>

<span data-ttu-id="64c16-2897">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2897">4</span></span>

<span data-ttu-id="64c16-2898">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2898">5</span></span>

<span data-ttu-id="64c16-2899">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2899">6</span></span>

<span data-ttu-id="64c16-2900">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2900">7</span></span>

<span data-ttu-id="64c16-2901">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2901">8</span></span>

<span data-ttu-id="64c16-2902">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2902">9</span></span>

<span data-ttu-id="64c16-2903">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2903">2</span></span><br/> <span data-ttu-id="64c16-2904">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2904">0</span></span><br/>

<span data-ttu-id="64c16-2905">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2905">1</span></span>

<span data-ttu-id="64c16-2906">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2906">2</span></span>

<span data-ttu-id="64c16-2907">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2907">3</span></span>

<span data-ttu-id="64c16-2908">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2908">4</span></span>

<span data-ttu-id="64c16-2909">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2909">5</span></span>

<span data-ttu-id="64c16-2910">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2910">6</span></span>

<span data-ttu-id="64c16-2911">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2911">7</span></span>

<span data-ttu-id="64c16-2912">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2912">8</span></span>

<span data-ttu-id="64c16-2913">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2913">9</span></span>

<span data-ttu-id="64c16-2914">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2914">3</span></span><br/> <span data-ttu-id="64c16-2915">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2915">0</span></span><br/>

<span data-ttu-id="64c16-2916">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2916">1</span></span>

<span data-ttu-id="64c16-2917">\_dwoldstate</span><span class="sxs-lookup"><span data-stu-id="64c16-2917">\_dwOldState</span></span>



 

<span data-ttu-id="64c16-2918">**\_ dwoldstate**: einer der folgenden Werte, der den alten Status des Katalogs angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2918">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="64c16-2919">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-2919">Value</span></span>                       | <span data-ttu-id="64c16-2920">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-2920">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="64c16-2921">Cicat hat \_ 0x00000001 beendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-2921">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="64c16-2922">Der Katalog wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-2922">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="64c16-2923">Cicat schreibgeschützt \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-2923">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="64c16-2924">Der Katalog ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2924">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="64c16-2925">Cicat \_ beschreibbare 0x00000004</span><span class="sxs-lookup"><span data-stu-id="64c16-2925">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="64c16-2926">Der Katalog ist beschreibbar.</span><span class="sxs-lookup"><span data-stu-id="64c16-2926">The catalog is writable.</span></span>                   |
| <span data-ttu-id="64c16-2927">Cicat \_ keine \_ Abfrage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="64c16-2927">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="64c16-2928">Der Katalog ist nicht für Abfragen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="64c16-2928">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="64c16-2929">2.2.3.4 cpmupdatedocumentsin</span><span class="sxs-lookup"><span data-stu-id="64c16-2929">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="64c16-2930">Die cpmupdatedocumentsin-Nachricht weist den Server an, den angegebenen Pfad zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="64c16-2930">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="64c16-2931">Der Server antwortet mit dem Nachrichten Header der cpmupdatedocumentsout-Nachricht, wobei die Ergebnisse der Anforderung im \_ Feld Status des Nachrichten Headers enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-2931">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="64c16-2932">Das Format der cpmupdatedocumentsin-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-2932">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="64c16-2933">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2933">0</span></span>

<span data-ttu-id="64c16-2934">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2934">1</span></span>

<span data-ttu-id="64c16-2935">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2935">2</span></span>

<span data-ttu-id="64c16-2936">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2936">3</span></span>

<span data-ttu-id="64c16-2937">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2937">4</span></span>

<span data-ttu-id="64c16-2938">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2938">5</span></span>

<span data-ttu-id="64c16-2939">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2939">6</span></span>

<span data-ttu-id="64c16-2940">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2940">7</span></span>

<span data-ttu-id="64c16-2941">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2941">8</span></span>

<span data-ttu-id="64c16-2942">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2942">9</span></span>

<span data-ttu-id="64c16-2943">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2943">1</span></span><br/> <span data-ttu-id="64c16-2944">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2944">0</span></span><br/>

<span data-ttu-id="64c16-2945">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2945">1</span></span>

<span data-ttu-id="64c16-2946">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2946">2</span></span>

<span data-ttu-id="64c16-2947">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2947">3</span></span>

<span data-ttu-id="64c16-2948">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2948">4</span></span>

<span data-ttu-id="64c16-2949">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2949">5</span></span>

<span data-ttu-id="64c16-2950">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2950">6</span></span>

<span data-ttu-id="64c16-2951">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2951">7</span></span>

<span data-ttu-id="64c16-2952">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2952">8</span></span>

<span data-ttu-id="64c16-2953">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2953">9</span></span>

<span data-ttu-id="64c16-2954">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2954">2</span></span><br/> <span data-ttu-id="64c16-2955">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2955">0</span></span><br/>

<span data-ttu-id="64c16-2956">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2956">1</span></span>

<span data-ttu-id="64c16-2957">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2957">2</span></span>

<span data-ttu-id="64c16-2958">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2958">3</span></span>

<span data-ttu-id="64c16-2959">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2959">4</span></span>

<span data-ttu-id="64c16-2960">5</span><span class="sxs-lookup"><span data-stu-id="64c16-2960">5</span></span>

<span data-ttu-id="64c16-2961">6</span><span class="sxs-lookup"><span data-stu-id="64c16-2961">6</span></span>

<span data-ttu-id="64c16-2962">7</span><span class="sxs-lookup"><span data-stu-id="64c16-2962">7</span></span>

<span data-ttu-id="64c16-2963">8</span><span class="sxs-lookup"><span data-stu-id="64c16-2963">8</span></span>

<span data-ttu-id="64c16-2964">9</span><span class="sxs-lookup"><span data-stu-id="64c16-2964">9</span></span>

<span data-ttu-id="64c16-2965">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2965">3</span></span><br/> <span data-ttu-id="64c16-2966">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2966">0</span></span><br/>

<span data-ttu-id="64c16-2967">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2967">1</span></span>

<span data-ttu-id="64c16-2968">\_Flag (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-2968">\_flag (optional)</span></span>

<span data-ttu-id="64c16-2969">\_frootpath (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-2969">\_fRootPath (optional)</span></span>

<span data-ttu-id="64c16-2970">RootPath (Variable, optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-2970">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="64c16-2971">**\_ Flag**: der Typ des auszuführenden Updates.</span><span class="sxs-lookup"><span data-stu-id="64c16-2971">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="64c16-2972">Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-2972">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="64c16-2973">Dieses Feld muss auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="64c16-2973">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="64c16-2974">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-2974">Value</span></span>                  | <span data-ttu-id="64c16-2975">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-2975">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="64c16-2976">UPD \_ increm 0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-2976">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="64c16-2977">Es muss ein inkrementelles Update durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2977">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="64c16-2978">UPD \_ vollständig 0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-2978">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="64c16-2979">Es muss ein vollständiges Update durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2979">A full update is to be performed.</span></span>         |
| <span data-ttu-id="64c16-2980">UPD \_ Init 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-2980">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="64c16-2981">Es muss eine neue Initialisierung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2981">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="64c16-2982">**\_ frootpath**: ein boolescher Wert, der angibt, ob das Feld RootPath einen Pfad angibt, in dem das Update durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-2982">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="64c16-2983">Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-2983">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="64c16-2984">Dieses Feld muss auf 0x00000001 oder 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-2984">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="64c16-2985">Bei Festlegung auf 0x00000001 ist ein Pfad, in dem das Update durchgeführt werden soll, in RootPath enthalten.</span><span class="sxs-lookup"><span data-stu-id="64c16-2985">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="64c16-2986">Wenn der Wert auf 0x00000000 festgelegt ist, wird das Update für alle indizierten Pfade ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64c16-2986">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="64c16-2987">**RootPath**: der Name des Pfads, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-2987">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="64c16-2988">Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-2988">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="64c16-2989">Der Name muss eine NULL-terminierte Unicode-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-2989">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="64c16-2990">Dieses Feld muss weggelassen werden \_ , wenn frootpath auf 0x00000000 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-2990">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="64c16-2991">2.2.3.5 cpmforcemergein</span><span class="sxs-lookup"><span data-stu-id="64c16-2991">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="64c16-2992">Mit der cpmforcemergein-Meldung wird ein Server aufgefordert, jede erforderliche Wartung auszuführen, um die Abfrageleistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="64c16-2992">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="64c16-2993">Der Server antwortet mit dem Nachrichten Header der cpmforcemergein-Nachricht, wobei die Ergebnisse der im Feld Status enthaltenen Anforderung angezeigt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-2993">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="64c16-2994">Das Format der cpmforcemergein-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-2994">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="64c16-2995">0</span><span class="sxs-lookup"><span data-stu-id="64c16-2995">0</span></span>

<span data-ttu-id="64c16-2996">1</span><span class="sxs-lookup"><span data-stu-id="64c16-2996">1</span></span>

<span data-ttu-id="64c16-2997">2</span><span class="sxs-lookup"><span data-stu-id="64c16-2997">2</span></span>

<span data-ttu-id="64c16-2998">3</span><span class="sxs-lookup"><span data-stu-id="64c16-2998">3</span></span>

<span data-ttu-id="64c16-2999">4</span><span class="sxs-lookup"><span data-stu-id="64c16-2999">4</span></span>

<span data-ttu-id="64c16-3000">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3000">5</span></span>

<span data-ttu-id="64c16-3001">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3001">6</span></span>

<span data-ttu-id="64c16-3002">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3002">7</span></span>

<span data-ttu-id="64c16-3003">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3003">8</span></span>

<span data-ttu-id="64c16-3004">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3004">9</span></span>

<span data-ttu-id="64c16-3005">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3005">1</span></span><br/> <span data-ttu-id="64c16-3006">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3006">0</span></span><br/>

<span data-ttu-id="64c16-3007">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3007">1</span></span>

<span data-ttu-id="64c16-3008">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3008">2</span></span>

<span data-ttu-id="64c16-3009">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3009">3</span></span>

<span data-ttu-id="64c16-3010">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3010">4</span></span>

<span data-ttu-id="64c16-3011">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3011">5</span></span>

<span data-ttu-id="64c16-3012">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3012">6</span></span>

<span data-ttu-id="64c16-3013">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3013">7</span></span>

<span data-ttu-id="64c16-3014">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3014">8</span></span>

<span data-ttu-id="64c16-3015">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3015">9</span></span>

<span data-ttu-id="64c16-3016">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3016">2</span></span><br/> <span data-ttu-id="64c16-3017">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3017">0</span></span><br/>

<span data-ttu-id="64c16-3018">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3018">1</span></span>

<span data-ttu-id="64c16-3019">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3019">2</span></span>

<span data-ttu-id="64c16-3020">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3020">3</span></span>

<span data-ttu-id="64c16-3021">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3021">4</span></span>

<span data-ttu-id="64c16-3022">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3022">5</span></span>

<span data-ttu-id="64c16-3023">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3023">6</span></span>

<span data-ttu-id="64c16-3024">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3024">7</span></span>

<span data-ttu-id="64c16-3025">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3025">8</span></span>

<span data-ttu-id="64c16-3026">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3026">9</span></span>

<span data-ttu-id="64c16-3027">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3027">3</span></span><br/> <span data-ttu-id="64c16-3028">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3028">0</span></span><br/>

<span data-ttu-id="64c16-3029">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3029">1</span></span>

<span data-ttu-id="64c16-3030">\_partitiond (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-3030">\_partID (optional)</span></span>



 

<span data-ttu-id="64c16-3031">**\_ partitiond**: Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-3031">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="64c16-3032">Wenn dieses Feld vorhanden ist, muss es auf 0x00000001 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3032">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="64c16-3033">2.2.3.6 cpmconnectin</span><span class="sxs-lookup"><span data-stu-id="64c16-3033">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="64c16-3034">Die cpmconnectin-Nachricht beginnt eine Sitzung zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="64c16-3034">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="64c16-3035">Das Format der cpmconnectin-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3035">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="64c16-3036">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3036">0</span></span>

<span data-ttu-id="64c16-3037">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3037">1</span></span>

<span data-ttu-id="64c16-3038">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3038">2</span></span>

<span data-ttu-id="64c16-3039">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3039">3</span></span>

<span data-ttu-id="64c16-3040">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3040">4</span></span>

<span data-ttu-id="64c16-3041">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3041">5</span></span>

<span data-ttu-id="64c16-3042">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3042">6</span></span>

<span data-ttu-id="64c16-3043">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3043">7</span></span>

<span data-ttu-id="64c16-3044">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3044">8</span></span>

<span data-ttu-id="64c16-3045">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3045">9</span></span>

<span data-ttu-id="64c16-3046">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3046">1</span></span><br/> <span data-ttu-id="64c16-3047">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3047">0</span></span><br/>

<span data-ttu-id="64c16-3048">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3048">1</span></span>

<span data-ttu-id="64c16-3049">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3049">2</span></span>

<span data-ttu-id="64c16-3050">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3050">3</span></span>

<span data-ttu-id="64c16-3051">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3051">4</span></span>

<span data-ttu-id="64c16-3052">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3052">5</span></span>

<span data-ttu-id="64c16-3053">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3053">6</span></span>

<span data-ttu-id="64c16-3054">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3054">7</span></span>

<span data-ttu-id="64c16-3055">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3055">8</span></span>

<span data-ttu-id="64c16-3056">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3056">9</span></span>

<span data-ttu-id="64c16-3057">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3057">2</span></span><br/> <span data-ttu-id="64c16-3058">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3058">0</span></span><br/>

<span data-ttu-id="64c16-3059">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3059">1</span></span>

<span data-ttu-id="64c16-3060">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3060">2</span></span>

<span data-ttu-id="64c16-3061">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3061">3</span></span>

<span data-ttu-id="64c16-3062">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3062">4</span></span>

<span data-ttu-id="64c16-3063">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3063">5</span></span>

<span data-ttu-id="64c16-3064">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3064">6</span></span>

<span data-ttu-id="64c16-3065">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3065">7</span></span>

<span data-ttu-id="64c16-3066">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3066">8</span></span>

<span data-ttu-id="64c16-3067">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3067">9</span></span>

<span data-ttu-id="64c16-3068">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3068">3</span></span><br/> <span data-ttu-id="64c16-3069">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3069">0</span></span><br/>

<span data-ttu-id="64c16-3070">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3070">1</span></span>

<span data-ttu-id="64c16-3071">\_iclientversion</span><span class="sxs-lookup"><span data-stu-id="64c16-3071">\_iClientVersion</span></span>

<span data-ttu-id="64c16-3072">\_"lclientisremote"</span><span class="sxs-lookup"><span data-stu-id="64c16-3072">\_fClientIsRemote</span></span>

<span data-ttu-id="64c16-3073">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="64c16-3073">\_cbBlob1</span></span>

<span data-ttu-id="64c16-3074">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="64c16-3074">\_cbBlob2</span></span>

<span data-ttu-id="64c16-3075">\_Auffüllung</span><span class="sxs-lookup"><span data-stu-id="64c16-3075">\_padding</span></span>

<span data-ttu-id="64c16-3076">...</span><span class="sxs-lookup"><span data-stu-id="64c16-3076">...</span></span>

<span data-ttu-id="64c16-3077">...</span><span class="sxs-lookup"><span data-stu-id="64c16-3077">...</span></span>

<span data-ttu-id="64c16-3078">MachineName</span><span class="sxs-lookup"><span data-stu-id="64c16-3078">MachineName</span></span>

<span data-ttu-id="64c16-3079">... veränder</span><span class="sxs-lookup"><span data-stu-id="64c16-3079">... (variable)</span></span>

<span data-ttu-id="64c16-3080">UserName</span><span class="sxs-lookup"><span data-stu-id="64c16-3080">UserName</span></span>

<span data-ttu-id="64c16-3081">... veränder</span><span class="sxs-lookup"><span data-stu-id="64c16-3081">... (variable)</span></span>

<span data-ttu-id="64c16-3082">\_paddingcpropsets (optional, Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-3082">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="64c16-3083">cpropsets</span><span class="sxs-lookup"><span data-stu-id="64c16-3083">cPropSets</span></span>

<span data-ttu-id="64c16-3084">PropertySet1 (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-3084">PropertySet1 (variable)</span></span>

<span data-ttu-id="64c16-3085">PropertySet2 (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-3085">PropertySet2 (variable)</span></span>

<span data-ttu-id="64c16-3086">\_paddingextpropset (optional, Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-3086">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="64c16-3087">cextpropset</span><span class="sxs-lookup"><span data-stu-id="64c16-3087">cExtPropSet</span></span>

<span data-ttu-id="64c16-3088">apropertysets (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-3088">aPropertySets (variable)</span></span>



 

<span data-ttu-id="64c16-3089">**\_ iclientversion**: eine 32-Bit-Ganzzahl, die angibt, ob der Server den Prüfsummen Wert validieren soll, der im \_ Feld ulchecksum der Nachrichten Header für vom Client gesendete Nachrichten angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-3089">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="64c16-3090">Wenn das \_ Feld iclientversion auf 0x00000008 oder höher festgelegt ist, muss der Server den \_ ulchecksum-Feldwert für die folgenden Meldungen überprüfen:</span><span class="sxs-lookup"><span data-stu-id="64c16-3090">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="64c16-3091">Cpmconnectin</span><span class="sxs-lookup"><span data-stu-id="64c16-3091">CPMConnectIn</span></span>
-   <span data-ttu-id="64c16-3092">Cpmkreatequeryin</span><span class="sxs-lookup"><span data-stu-id="64c16-3092">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="64c16-3093">Cpmfetchvaluein</span><span class="sxs-lookup"><span data-stu-id="64c16-3093">CPMFetchValueIn</span></span>
-   <span data-ttu-id="64c16-3094">Cpmgetrowsin</span><span class="sxs-lookup"><span data-stu-id="64c16-3094">CPMGetRowsIn</span></span>
-   <span data-ttu-id="64c16-3095">Cpmsetbindingsin</span><span class="sxs-lookup"><span data-stu-id="64c16-3095">CPMSetBindingsIn</span></span>

<span data-ttu-id="64c16-3096">Ausführliche Informationen dazu, wie der-Server den vom Client angegebenen Wert im Feld ulchecksum für die oben aufgeführten Nachrichten überprüft, finden Sie im Abschnitt 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="64c16-3096">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="64c16-3097">Wenn der Wert größer als 0x00000008 ist, wird angenommen, dass der Client 64-Bit-Offsets in cpmgetrowsout-Nachrichten verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="64c16-3097">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="64c16-3098">Weitere Informationen finden Sie im Abschnitt 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="64c16-3098">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="64c16-3099">*Windows-Verhalten: auf Windows-Clients wird iclientversion wie folgt festgelegt*:</span><span class="sxs-lookup"><span data-stu-id="64c16-3099">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="64c16-3100">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-3100">Value</span></span>      | <span data-ttu-id="64c16-3101">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-3101">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="64c16-3102">0x00000005</span><span class="sxs-lookup"><span data-stu-id="64c16-3102">0x00000005</span></span> | <span data-ttu-id="64c16-3103">Client Betriebssystem ist Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="64c16-3103">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="64c16-3104">0x00000008</span><span class="sxs-lookup"><span data-stu-id="64c16-3104">0x00000008</span></span> | <span data-ttu-id="64c16-3105">Client Betriebssystem ist entweder 32 Bit Windows XP oder 32-Bit Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="64c16-3105">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="64c16-3106">0x00010008</span><span class="sxs-lookup"><span data-stu-id="64c16-3106">0x00010008</span></span> | <span data-ttu-id="64c16-3107">Client Betriebssystem ist entweder 64 Bit Windows XP oder 64-Bit Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="64c16-3107">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="64c16-3108">\_**fclientisremote**: ein boolescher Wert, der angibt, ob der Client auf einem anderen Computer als der Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-3108">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="64c16-3109">Muss auf 0x00000001 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3109">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="64c16-3110">\_**cbBlob1**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe in Bytes der cpropset-, PropertySet1-und PropertySet2-Felder kombiniert.</span><span class="sxs-lookup"><span data-stu-id="64c16-3110">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="64c16-3111">\_**cbBlob2**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der Felder cexpropset und apropertyset in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3111">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="64c16-3112">\_**Auffüllung**: 12 Bytes an Auffüll Zeichen, die beliebige Werte enthalten können und ignoriert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3112">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="64c16-3113">**MachineName**: der Computername des Clients.</span><span class="sxs-lookup"><span data-stu-id="64c16-3113">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="64c16-3114">Die namens Zeichenfolge muss ein mit Null endendes Array mit weniger als 512 Unicode-Zeichen sein, einschließlich des NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="64c16-3114">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="64c16-3115">**Username**: eine Zeichenfolge, die den Benutzernamen der Person darstellt, von der die Anwendung ausgeführt wird, die dieses Protokoll aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="64c16-3115">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="64c16-3116">Die namens Zeichenfolge muss ein mit Null endendes Array von weniger als 512 Unicode-Zeichen sein, wenn Sie mit MachineName verkettet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3116">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="64c16-3117">**\_ paddingcpropsets**: Dieses Feld muss zwischen 0 und 7 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-3117">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="64c16-3118">Die Anzahl der Bytes muss die Zahl sein, die erforderlich ist, um den Byte Offset des Felds cpropsets vom Anfang der Nachricht, die diese Struktur enthält, als Vielfaches von 8 festzulegen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3118">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="64c16-3119">Der Wert der Bytes kann ein beliebiger Wert sein und muss vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3119">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="64c16-3120">**cpropsets**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der CDBPropSet-Strukturen, die diesem Feld folgen, angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3120">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="64c16-3121">Dieser Wert muss auf 0x0000002 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3121">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="64c16-3122">**PropertySet1**: eine CDBPropSet-Struktur mit guidPropertySet mit DBPROPSET " \_ f-frmwrk \_ ext" (siehe Abschnitt 2.2.1.22)</span><span class="sxs-lookup"><span data-stu-id="64c16-3122">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="64c16-3123">**PropertySet2**: eine CDBPropSet-Struktur mit guidPropertySet, die DBPROPSET \_ cifrmwrkcore \_ ext enthält (siehe Abschnitt 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="64c16-3123">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="64c16-3124">\_**Paddingextpropset**: Dieses Feld muss zwischen 0 und 7 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-3124">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="64c16-3125">Die Anzahl der Bytes muss die Zahl sein, die erforderlich ist, um den Byte Offset des Felds cextpropsets vom Anfang der Nachricht, die diese Struktur enthält, als Vielfaches von 8 festzulegen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3125">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="64c16-3126">Der Wert der Bytes kann ein beliebiger Wert sein und muss vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3126">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="64c16-3127">**cextpropset**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der CDBPropSet-Strukturen, die diesem Feld folgen, angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3127">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="64c16-3128">**apropertysets**: ein Array von CDBPropSet-Strukturen, das andere Eigenschaften angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3128">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="64c16-3129">Die Anzahl der Elemente in diesem Array muss gleich cextpropset sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-3129">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="64c16-3130">2.2.3.7 cpmconnectout</span><span class="sxs-lookup"><span data-stu-id="64c16-3130">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="64c16-3131">Die cpmconnectout-Nachricht enthält eine Antwort auf eine cpmconnectin-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-3131">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="64c16-3132">Das Format der cpmconnectout-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3132">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="64c16-3133">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3133">0</span></span>

<span data-ttu-id="64c16-3134">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3134">1</span></span>

<span data-ttu-id="64c16-3135">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3135">2</span></span>

<span data-ttu-id="64c16-3136">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3136">3</span></span>

<span data-ttu-id="64c16-3137">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3137">4</span></span>

<span data-ttu-id="64c16-3138">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3138">5</span></span>

<span data-ttu-id="64c16-3139">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3139">6</span></span>

<span data-ttu-id="64c16-3140">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3140">7</span></span>

<span data-ttu-id="64c16-3141">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3141">8</span></span>

<span data-ttu-id="64c16-3142">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3142">9</span></span>

<span data-ttu-id="64c16-3143">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3143">1</span></span><br/> <span data-ttu-id="64c16-3144">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3144">0</span></span><br/>

<span data-ttu-id="64c16-3145">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3145">1</span></span>

<span data-ttu-id="64c16-3146">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3146">2</span></span>

<span data-ttu-id="64c16-3147">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3147">3</span></span>

<span data-ttu-id="64c16-3148">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3148">4</span></span>

<span data-ttu-id="64c16-3149">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3149">5</span></span>

<span data-ttu-id="64c16-3150">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3150">6</span></span>

<span data-ttu-id="64c16-3151">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3151">7</span></span>

<span data-ttu-id="64c16-3152">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3152">8</span></span>

<span data-ttu-id="64c16-3153">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3153">9</span></span>

<span data-ttu-id="64c16-3154">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3154">2</span></span><br/> <span data-ttu-id="64c16-3155">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3155">0</span></span><br/>

<span data-ttu-id="64c16-3156">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3156">1</span></span>

<span data-ttu-id="64c16-3157">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3157">2</span></span>

<span data-ttu-id="64c16-3158">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3158">3</span></span>

<span data-ttu-id="64c16-3159">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3159">4</span></span>

<span data-ttu-id="64c16-3160">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3160">5</span></span>

<span data-ttu-id="64c16-3161">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3161">6</span></span>

<span data-ttu-id="64c16-3162">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3162">7</span></span>

<span data-ttu-id="64c16-3163">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3163">8</span></span>

<span data-ttu-id="64c16-3164">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3164">9</span></span>

<span data-ttu-id="64c16-3165">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3165">3</span></span><br/> <span data-ttu-id="64c16-3166">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3166">0</span></span><br/>

<span data-ttu-id="64c16-3167">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3167">1</span></span>

<span data-ttu-id="64c16-3168">\_Server Version</span><span class="sxs-lookup"><span data-stu-id="64c16-3168">\_serverVersion</span></span>

<span data-ttu-id="64c16-3169">\_reserviert (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-3169">\_reserved (variable)</span></span>



 

<span data-ttu-id="64c16-3170">**\_ Server Version**:</span><span class="sxs-lookup"><span data-stu-id="64c16-3170">**\_serverVersion**:</span></span>

<span data-ttu-id="64c16-3171">Eine 32-Bit-Ganzzahl, die angibt, ob der Server 64-Bit-Offsets unterstützen kann *.*</span><span class="sxs-lookup"><span data-stu-id="64c16-3171">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="64c16-3172">Weitere Informationen finden Sie im Abschnitt 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="64c16-3172">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="64c16-3173">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-3173">Value</span></span>      | <span data-ttu-id="64c16-3174">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-3174">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="64c16-3175">0x00000007</span><span class="sxs-lookup"><span data-stu-id="64c16-3175">0x00000007</span></span> | <span data-ttu-id="64c16-3176">Der Server kann nur 32-Bit-Offsets senden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3176">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="64c16-3177">0x00010007</span><span class="sxs-lookup"><span data-stu-id="64c16-3177">0x00010007</span></span> | <span data-ttu-id="64c16-3178">Der Server kann 32-oder 64-Bit-Offsets senden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3178">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="64c16-3179">**\_ reserviert**: reserviert.</span><span class="sxs-lookup"><span data-stu-id="64c16-3179">**\_reserved**: Reserved.</span></span> <span data-ttu-id="64c16-3180">Der Server sendet möglicherweise eine beliebige Anzahl beliebiger Werte, und der Client muss diese Werte ignorieren, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3180">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="64c16-3181">2.2.3.8 cpmkreatequeryin</span><span class="sxs-lookup"><span data-stu-id="64c16-3181">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="64c16-3182">Die cpmkreatequeryin-Meldung erstellt eine neue Abfrage.</span><span class="sxs-lookup"><span data-stu-id="64c16-3182">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="64c16-3183">Das Format der cpmkreatequeryin-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3183">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="64c16-3184">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3184">0</span></span>

<span data-ttu-id="64c16-3185">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3185">1</span></span>

<span data-ttu-id="64c16-3186">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3186">2</span></span>

<span data-ttu-id="64c16-3187">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3187">3</span></span>

<span data-ttu-id="64c16-3188">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3188">4</span></span>

<span data-ttu-id="64c16-3189">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3189">5</span></span>

<span data-ttu-id="64c16-3190">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3190">6</span></span>

<span data-ttu-id="64c16-3191">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3191">7</span></span>

<span data-ttu-id="64c16-3192">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3192">8</span></span>

<span data-ttu-id="64c16-3193">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3193">9</span></span>

<span data-ttu-id="64c16-3194">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3194">1</span></span><br/> <span data-ttu-id="64c16-3195">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3195">0</span></span><br/>

<span data-ttu-id="64c16-3196">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3196">1</span></span>

<span data-ttu-id="64c16-3197">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3197">2</span></span>

<span data-ttu-id="64c16-3198">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3198">3</span></span>

<span data-ttu-id="64c16-3199">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3199">4</span></span>

<span data-ttu-id="64c16-3200">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3200">5</span></span>

<span data-ttu-id="64c16-3201">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3201">6</span></span>

<span data-ttu-id="64c16-3202">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3202">7</span></span>

<span data-ttu-id="64c16-3203">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3203">8</span></span>

<span data-ttu-id="64c16-3204">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3204">9</span></span>

<span data-ttu-id="64c16-3205">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3205">2</span></span><br/> <span data-ttu-id="64c16-3206">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3206">0</span></span><br/>

<span data-ttu-id="64c16-3207">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3207">1</span></span>

<span data-ttu-id="64c16-3208">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3208">2</span></span>

<span data-ttu-id="64c16-3209">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3209">3</span></span>

<span data-ttu-id="64c16-3210">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3210">4</span></span>

<span data-ttu-id="64c16-3211">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3211">5</span></span>

<span data-ttu-id="64c16-3212">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3212">6</span></span>

<span data-ttu-id="64c16-3213">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3213">7</span></span>

<span data-ttu-id="64c16-3214">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3214">8</span></span>

<span data-ttu-id="64c16-3215">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3215">9</span></span>

<span data-ttu-id="64c16-3216">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3216">3</span></span><br/> <span data-ttu-id="64c16-3217">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3217">0</span></span><br/>

<span data-ttu-id="64c16-3218">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3218">1</span></span>

<span data-ttu-id="64c16-3219">Size</span><span class="sxs-lookup"><span data-stu-id="64c16-3219">Size</span></span>

<span data-ttu-id="64c16-3220">Ccolumnsetpresent</span><span class="sxs-lookup"><span data-stu-id="64c16-3220">CColumnSetPresent</span></span>

<span data-ttu-id="64c16-3221">ColumnSet (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-3221">ColumnSet (optional)</span></span>

<span data-ttu-id="64c16-3222">... veränder</span><span class="sxs-lookup"><span data-stu-id="64c16-3222">... (variable)</span></span>

<span data-ttu-id="64c16-3223">"Krestrictionpresent".</span><span class="sxs-lookup"><span data-stu-id="64c16-3223">CRestrictionPresent.</span></span>

<span data-ttu-id="64c16-3224">Einschränkung (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-3224">Restriction (optional)</span></span>

<span data-ttu-id="64c16-3225">... veränder</span><span class="sxs-lookup"><span data-stu-id="64c16-3225">... (variable)</span></span>

<span data-ttu-id="64c16-3226">Csortsetpresent</span><span class="sxs-lookup"><span data-stu-id="64c16-3226">CSortSetPresent</span></span>

<span data-ttu-id="64c16-3227">Sortset (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-3227">SortSet (optional)</span></span>

<span data-ttu-id="64c16-3228">... veränder</span><span class="sxs-lookup"><span data-stu-id="64c16-3228">... (variable)</span></span>

<span data-ttu-id="64c16-3229">Ccategorizationsetpresent</span><span class="sxs-lookup"><span data-stu-id="64c16-3229">CCategorizationSetPresent</span></span>

<span data-ttu-id="64c16-3230">Kategorisierungs Satz (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-3230">CategorizationSet (optional)</span></span>

<span data-ttu-id="64c16-3231">... veränder</span><span class="sxs-lookup"><span data-stu-id="64c16-3231">... (variable)</span></span>

<span data-ttu-id="64c16-3232">Rowsetproperties</span><span class="sxs-lookup"><span data-stu-id="64c16-3232">RowSetProperties</span></span>

<span data-ttu-id="64c16-3233">...</span><span class="sxs-lookup"><span data-stu-id="64c16-3233">...</span></span>

<span data-ttu-id="64c16-3234">...</span><span class="sxs-lookup"><span data-stu-id="64c16-3234">...</span></span>

<span data-ttu-id="64c16-3235">...</span><span class="sxs-lookup"><span data-stu-id="64c16-3235">...</span></span>

<span data-ttu-id="64c16-3236">...</span><span class="sxs-lookup"><span data-stu-id="64c16-3236">...</span></span>

<span data-ttu-id="64c16-3237">Pidmapper (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-3237">PidMapper (variable)</span></span>



 

<span data-ttu-id="64c16-3238">**Size**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Bytes vom Anfang dieses Felds bis zum Ende der Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3238">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="64c16-3239">**Ccolumnsetpresent**: ein Bytefeld, das angibt, ob das ColumnSet-Feld vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-3239">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="64c16-3240">Dieses Feld muss auf 0x01 oder 0x00 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3240">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="64c16-3241">Wenn der Wert auf 0x01 festgelegt ist, muss das ccolumnset-Feld vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-3241">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="64c16-3242">Wenn der Wert auf 0x00 festgelegt ist, muss er nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-3242">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="64c16-3243">**ColumnSet**: eine ccolumnset-Struktur, die die Spalten Nummern enthält, in denen die cpidmapper-Eigenschaften zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3243">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="64c16-3244">" **Krestrictionpresent**": ein Bytefeld, das angibt, ob das Einschränkungs Feld vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-3244">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="64c16-3245">Wenn ein Wert ungleich 0 (null) festgelegt ist, muss das Einschränkungs Feld vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-3245">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="64c16-3246">Wenn der Wert auf 0x00 festgelegt ist, muss die Einschränkung nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-3246">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="64c16-3247">**Einschränkung**: eine Struktur mit dem Befehl, die die Befehlsstruktur der Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-3247">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="64c16-3248">**Csortsetpresent**: ein Bytefeld, das angibt, ob das sortset-Feld vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-3248">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="64c16-3249">Wenn ein Wert ungleich 0 (null) festgelegt ist, muss das sortset-Feld vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-3249">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="64c16-3250">Wenn der Wert auf 0x00 festgelegt ist, muss sortset nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-3250">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="64c16-3251">**Sortset**: eine csortset-Struktur, die die Sortierreihenfolge der Abfrage angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3251">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="64c16-3252">**Ccategorizationsetpresent**: ein Bytefeld, das angibt, ob das Feld "ccategorizationset" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-3252">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="64c16-3253">Wenn ein Wert ungleich 0 (null) festgelegt ist, muss das Feld "ccategorizationset" vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-3253">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="64c16-3254">Wenn der Wert auf 0x00 festgelegt ist, muss ccategorizationset nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-3254">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="64c16-3255">**Ccategorizationset**: eine ccategorizationset-Struktur, die die Gruppen für die Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-3255">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="64c16-3256">**Rowsetproperties**: eine crowsetproperties-Struktur, die Konfigurationsinformationen für die Abfrage bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3256">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="64c16-3257">**Pidmapper**: eine cpidmapper-Struktur, die Eigenschaften enthält, die in einem Rowset zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3257">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="64c16-3258">2.2.3.9 cpmkreatequeryout</span><span class="sxs-lookup"><span data-stu-id="64c16-3258">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="64c16-3259">Die cpmkreatequeryout-Nachricht enthält eine Antwort auf eine cpmkreatequeryin-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-3259">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="64c16-3260">Das Format der cpmkreatequeryout-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3260">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="64c16-3261">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3261">0</span></span>

<span data-ttu-id="64c16-3262">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3262">1</span></span>

<span data-ttu-id="64c16-3263">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3263">2</span></span>

<span data-ttu-id="64c16-3264">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3264">3</span></span>

<span data-ttu-id="64c16-3265">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3265">4</span></span>

<span data-ttu-id="64c16-3266">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3266">5</span></span>

<span data-ttu-id="64c16-3267">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3267">6</span></span>

<span data-ttu-id="64c16-3268">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3268">7</span></span>

<span data-ttu-id="64c16-3269">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3269">8</span></span>

<span data-ttu-id="64c16-3270">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3270">9</span></span>

<span data-ttu-id="64c16-3271">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3271">1</span></span><br/> <span data-ttu-id="64c16-3272">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3272">0</span></span><br/>

<span data-ttu-id="64c16-3273">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3273">1</span></span>

<span data-ttu-id="64c16-3274">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3274">2</span></span>

<span data-ttu-id="64c16-3275">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3275">3</span></span>

<span data-ttu-id="64c16-3276">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3276">4</span></span>

<span data-ttu-id="64c16-3277">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3277">5</span></span>

<span data-ttu-id="64c16-3278">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3278">6</span></span>

<span data-ttu-id="64c16-3279">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3279">7</span></span>

<span data-ttu-id="64c16-3280">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3280">8</span></span>

<span data-ttu-id="64c16-3281">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3281">9</span></span>

<span data-ttu-id="64c16-3282">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3282">2</span></span><br/> <span data-ttu-id="64c16-3283">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3283">0</span></span><br/>

<span data-ttu-id="64c16-3284">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3284">1</span></span>

<span data-ttu-id="64c16-3285">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3285">2</span></span>

<span data-ttu-id="64c16-3286">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3286">3</span></span>

<span data-ttu-id="64c16-3287">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3287">4</span></span>

<span data-ttu-id="64c16-3288">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3288">5</span></span>

<span data-ttu-id="64c16-3289">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3289">6</span></span>

<span data-ttu-id="64c16-3290">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3290">7</span></span>

<span data-ttu-id="64c16-3291">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3291">8</span></span>

<span data-ttu-id="64c16-3292">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3292">9</span></span>

<span data-ttu-id="64c16-3293">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3293">3</span></span><br/> <span data-ttu-id="64c16-3294">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3294">0</span></span><br/>

<span data-ttu-id="64c16-3295">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3295">1</span></span>

<span data-ttu-id="64c16-3296">\_"struesequential"</span><span class="sxs-lookup"><span data-stu-id="64c16-3296">\_fTrueSequential</span></span>

<span data-ttu-id="64c16-3297">\_' f ' eindeutig</span><span class="sxs-lookup"><span data-stu-id="64c16-3297">\_fWorkIdUnique</span></span>

<span data-ttu-id="64c16-3298">acursoren</span><span class="sxs-lookup"><span data-stu-id="64c16-3298">aCursors</span></span>



 

<span data-ttu-id="64c16-3299">**\_ ftruesequential**: ein informativer boolescher Wert, der angibt, ob die Abfrage die Ergebnisse schneller bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="64c16-3299">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="64c16-3300">Wenn es für die in cpmkreatequeryin angegebene Abfrage auf 0x00000001 festgelegt ist, kann der Server den Index so verwenden, dass Abfrageergebnisse wahrscheinlich schneller zugestellt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3300">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="64c16-3301">Bei der Festlegung auf 0x00000000 wäre eine größere Latenz beim Bereitstellen von Abfrage Ergebnissen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3301">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="64c16-3302">Darf nicht auf einen anderen Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3302">MUST not be set to any other value.</span></span>

<span data-ttu-id="64c16-3303">" **\_ f workidunique**": ein boolescher Wert, der angibt, ob die von den Cursorn referenzierten Dokument Bezeichner in den Abfrage Ergebnissen eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-3303">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="64c16-3304">Wenn der Wert auf 0x00000001 festgelegt ist, sind die Bezeichner eindeutig.</span><span class="sxs-lookup"><span data-stu-id="64c16-3304">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="64c16-3305">Wenn Sie auf 0x00000000 festgelegt ist, sind Sie nur innerhalb des Rowsets eindeutig.</span><span class="sxs-lookup"><span data-stu-id="64c16-3305">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="64c16-3306">**acursoren**: ein Array aus 32-Bit-Ganzzahlen ohne Vorzeichen, das die Handles für Cursor darstellt, wobei die Anzahl der Elemente gleich der Anzahl der Kategorien im Feld "kategorizationset" der cpmkreatequeryin-Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-3306">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="64c16-3307">2.2.3.10 cpmgetquerystatus in</span><span class="sxs-lookup"><span data-stu-id="64c16-3307">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="64c16-3308">Die cpmgetquerystatusin-Meldung fordert den Status einer Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="64c16-3308">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="64c16-3309">Das Format der cpmgetquerystatusin-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3309">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="64c16-3310">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3310">0</span></span>

<span data-ttu-id="64c16-3311">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3311">1</span></span>

<span data-ttu-id="64c16-3312">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3312">2</span></span>

<span data-ttu-id="64c16-3313">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3313">3</span></span>

<span data-ttu-id="64c16-3314">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3314">4</span></span>

<span data-ttu-id="64c16-3315">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3315">5</span></span>

<span data-ttu-id="64c16-3316">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3316">6</span></span>

<span data-ttu-id="64c16-3317">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3317">7</span></span>

<span data-ttu-id="64c16-3318">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3318">8</span></span>

<span data-ttu-id="64c16-3319">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3319">9</span></span>

<span data-ttu-id="64c16-3320">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3320">1</span></span><br/> <span data-ttu-id="64c16-3321">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3321">0</span></span><br/>

<span data-ttu-id="64c16-3322">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3322">1</span></span>

<span data-ttu-id="64c16-3323">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3323">2</span></span>

<span data-ttu-id="64c16-3324">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3324">3</span></span>

<span data-ttu-id="64c16-3325">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3325">4</span></span>

<span data-ttu-id="64c16-3326">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3326">5</span></span>

<span data-ttu-id="64c16-3327">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3327">6</span></span>

<span data-ttu-id="64c16-3328">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3328">7</span></span>

<span data-ttu-id="64c16-3329">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3329">8</span></span>

<span data-ttu-id="64c16-3330">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3330">9</span></span>

<span data-ttu-id="64c16-3331">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3331">2</span></span><br/> <span data-ttu-id="64c16-3332">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3332">0</span></span><br/>

<span data-ttu-id="64c16-3333">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3333">1</span></span>

<span data-ttu-id="64c16-3334">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3334">2</span></span>

<span data-ttu-id="64c16-3335">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3335">3</span></span>

<span data-ttu-id="64c16-3336">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3336">4</span></span>

<span data-ttu-id="64c16-3337">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3337">5</span></span>

<span data-ttu-id="64c16-3338">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3338">6</span></span>

<span data-ttu-id="64c16-3339">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3339">7</span></span>

<span data-ttu-id="64c16-3340">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3340">8</span></span>

<span data-ttu-id="64c16-3341">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3341">9</span></span>

<span data-ttu-id="64c16-3342">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3342">3</span></span><br/> <span data-ttu-id="64c16-3343">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3343">0</span></span><br/>

<span data-ttu-id="64c16-3344">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3344">1</span></span>

<span data-ttu-id="64c16-3345">\_hcursor</span><span class="sxs-lookup"><span data-stu-id="64c16-3345">\_hCursor</span></span>



 

<span data-ttu-id="64c16-3346">**\_ hcursor**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die das Handle aus der cpmkreatequeryout-Meldung darstellt, die die Abfrage identifiziert, für die Statusinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3346">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="64c16-3347">2.2.3.11 cpmgetquerystatus-out</span><span class="sxs-lookup"><span data-stu-id="64c16-3347">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="64c16-3348">Die cpmgetquerystatusout-Meldung antwortet auf eine cpmgetquerystatusin-Nachricht mit dem Status der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="64c16-3348">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="64c16-3349">Das Format der cpmgetquerystatusout-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3349">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="64c16-3350">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3350">0</span></span>

<span data-ttu-id="64c16-3351">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3351">1</span></span>

<span data-ttu-id="64c16-3352">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3352">2</span></span>

<span data-ttu-id="64c16-3353">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3353">3</span></span>

<span data-ttu-id="64c16-3354">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3354">4</span></span>

<span data-ttu-id="64c16-3355">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3355">5</span></span>

<span data-ttu-id="64c16-3356">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3356">6</span></span>

<span data-ttu-id="64c16-3357">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3357">7</span></span>

<span data-ttu-id="64c16-3358">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3358">8</span></span>

<span data-ttu-id="64c16-3359">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3359">9</span></span>

<span data-ttu-id="64c16-3360">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3360">1</span></span><br/> <span data-ttu-id="64c16-3361">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3361">0</span></span><br/>

<span data-ttu-id="64c16-3362">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3362">1</span></span>

<span data-ttu-id="64c16-3363">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3363">2</span></span>

<span data-ttu-id="64c16-3364">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3364">3</span></span>

<span data-ttu-id="64c16-3365">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3365">4</span></span>

<span data-ttu-id="64c16-3366">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3366">5</span></span>

<span data-ttu-id="64c16-3367">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3367">6</span></span>

<span data-ttu-id="64c16-3368">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3368">7</span></span>

<span data-ttu-id="64c16-3369">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3369">8</span></span>

<span data-ttu-id="64c16-3370">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3370">9</span></span>

<span data-ttu-id="64c16-3371">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3371">2</span></span><br/> <span data-ttu-id="64c16-3372">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3372">0</span></span><br/>

<span data-ttu-id="64c16-3373">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3373">1</span></span>

<span data-ttu-id="64c16-3374">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3374">2</span></span>

<span data-ttu-id="64c16-3375">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3375">3</span></span>

<span data-ttu-id="64c16-3376">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3376">4</span></span>

<span data-ttu-id="64c16-3377">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3377">5</span></span>

<span data-ttu-id="64c16-3378">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3378">6</span></span>

<span data-ttu-id="64c16-3379">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3379">7</span></span>

<span data-ttu-id="64c16-3380">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3380">8</span></span>

<span data-ttu-id="64c16-3381">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3381">9</span></span>

<span data-ttu-id="64c16-3382">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3382">3</span></span><br/> <span data-ttu-id="64c16-3383">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3383">0</span></span><br/>

<span data-ttu-id="64c16-3384">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3384">1</span></span>

<span data-ttu-id="64c16-3385">\_Stands</span><span class="sxs-lookup"><span data-stu-id="64c16-3385">\_Status</span></span>



 

<span data-ttu-id="64c16-3386">**\_ Status**: eine Bitmaske mit Werten, die in den unten stehenden Tabellen definiert sind, die die Abfrage beschreibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3386">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="64c16-3387">In der folgenden Tabelle sind die stat-Werte aufgelistet, die \_ \* durch Ausführen einer bitweisen and-Operation \_ mit 0x00000007 abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3387">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="64c16-3388">Das Ergebnis muss einer der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="64c16-3388">The result MUST be one of the following:</span></span>



| <span data-ttu-id="64c16-3389">Konstante</span><span class="sxs-lookup"><span data-stu-id="64c16-3389">Constant</span></span>                 | <span data-ttu-id="64c16-3390">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-3390">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-3391">Stat \_ ausgelastet 0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-3391">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="64c16-3392">Die asynchrone Abfrage wird noch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3392">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="64c16-3393">Stat- \_ Fehler 0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-3393">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="64c16-3394">Die Abfrage weist einen Fehlerstatus auf.</span><span class="sxs-lookup"><span data-stu-id="64c16-3394">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="64c16-3395">Stat \_ done 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-3395">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="64c16-3396">Die Abfrage ist fertiggestellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3396">The query is complete.</span></span>                                                            |
| <span data-ttu-id="64c16-3397">Stat- \_ Aktualisierung 0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-3397">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="64c16-3398">Die Abfrage ist fertiggestellt, aber Updates ergeben eine zusätzliche Abfrage Berechnung.</span><span class="sxs-lookup"><span data-stu-id="64c16-3398">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="64c16-3399">In der folgenden Tabelle werden zusätzliche stat- \_ \* Bits aufgelistet, die unabhängig voneinander festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="64c16-3399">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="64c16-3400">Konstante</span><span class="sxs-lookup"><span data-stu-id="64c16-3400">Constant</span></span>                                    | <span data-ttu-id="64c16-3401">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-3401">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c16-3402">Stat-Füll \_ \_ Wörter 0x00000010</span><span class="sxs-lookup"><span data-stu-id="64c16-3402">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="64c16-3403">Füll Wörter wurden in der Inhalts Abfrage durch Platzhalter Zeichen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3403">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="64c16-3404">Stat- \_ Inhalt ist \_ \_ \_ veraltet 0x00000020</span><span class="sxs-lookup"><span data-stu-id="64c16-3404">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="64c16-3405">Die Ergebnisse der Abfrage sind möglicherweise falsch, da die Abfrage geänderte, aber nicht indizierte Dateien umfasste.</span><span class="sxs-lookup"><span data-stu-id="64c16-3405">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="64c16-3406">Die stat- \_ Aktualisierung ist \_ unvollständig 0x00000040</span><span class="sxs-lookup"><span data-stu-id="64c16-3406">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="64c16-3407">Die Ergebnisse der Abfrage sind möglicherweise falsch, da die Abfrage geänderte und neu indizierte Dateien umfasste, deren Inhalt nicht enthalten war.</span><span class="sxs-lookup"><span data-stu-id="64c16-3407">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="64c16-3408">Stat- \_ Inhalts \_ Abfrage \_ unvollständig 0x00000080</span><span class="sxs-lookup"><span data-stu-id="64c16-3408">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="64c16-3409">Die Inhalts Abfrage war zu komplex und konnte nicht verwendet werden, anstatt den Inhalts Index zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3409">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="64c16-3410">Stat- \_ Zeit \_ Limit \_ überschritten 0x00000100</span><span class="sxs-lookup"><span data-stu-id="64c16-3410">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="64c16-3411">Die Ergebnisse der Abfrage sind möglicherweise falsch, da die Abfrage Ausführungszeit die maximal zulässige Zeit erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="64c16-3411">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="64c16-3412">2.2.3.12 cpmgetquerystatusexin</span><span class="sxs-lookup"><span data-stu-id="64c16-3412">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="64c16-3413">Die cpmgetquerystatusexin-Nachricht fordert den Status einer Abfrage und zusätzliche Informationen, wie z. b. die Anzahl der indizierten Dokumente, die Anzahl der zu indizierenden Dokumente usw., an.</span><span class="sxs-lookup"><span data-stu-id="64c16-3413">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="64c16-3414">Das Format der cpmgetquerystatusexin-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3414">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="64c16-3415">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3415">0</span></span>

<span data-ttu-id="64c16-3416">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3416">1</span></span>

<span data-ttu-id="64c16-3417">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3417">2</span></span>

<span data-ttu-id="64c16-3418">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3418">3</span></span>

<span data-ttu-id="64c16-3419">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3419">4</span></span>

<span data-ttu-id="64c16-3420">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3420">5</span></span>

<span data-ttu-id="64c16-3421">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3421">6</span></span>

<span data-ttu-id="64c16-3422">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3422">7</span></span>

<span data-ttu-id="64c16-3423">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3423">8</span></span>

<span data-ttu-id="64c16-3424">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3424">9</span></span>

<span data-ttu-id="64c16-3425">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3425">1</span></span><br/> <span data-ttu-id="64c16-3426">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3426">0</span></span><br/>

<span data-ttu-id="64c16-3427">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3427">1</span></span>

<span data-ttu-id="64c16-3428">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3428">2</span></span>

<span data-ttu-id="64c16-3429">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3429">3</span></span>

<span data-ttu-id="64c16-3430">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3430">4</span></span>

<span data-ttu-id="64c16-3431">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3431">5</span></span>

<span data-ttu-id="64c16-3432">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3432">6</span></span>

<span data-ttu-id="64c16-3433">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3433">7</span></span>

<span data-ttu-id="64c16-3434">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3434">8</span></span>

<span data-ttu-id="64c16-3435">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3435">9</span></span>

<span data-ttu-id="64c16-3436">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3436">2</span></span><br/> <span data-ttu-id="64c16-3437">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3437">0</span></span><br/>

<span data-ttu-id="64c16-3438">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3438">1</span></span>

<span data-ttu-id="64c16-3439">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3439">2</span></span>

<span data-ttu-id="64c16-3440">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3440">3</span></span>

<span data-ttu-id="64c16-3441">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3441">4</span></span>

<span data-ttu-id="64c16-3442">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3442">5</span></span>

<span data-ttu-id="64c16-3443">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3443">6</span></span>

<span data-ttu-id="64c16-3444">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3444">7</span></span>

<span data-ttu-id="64c16-3445">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3445">8</span></span>

<span data-ttu-id="64c16-3446">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3446">9</span></span>

<span data-ttu-id="64c16-3447">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3447">3</span></span><br/> <span data-ttu-id="64c16-3448">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3448">0</span></span><br/>

<span data-ttu-id="64c16-3449">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3449">1</span></span>

<span data-ttu-id="64c16-3450">\_hcursor</span><span class="sxs-lookup"><span data-stu-id="64c16-3450">\_hCursor</span></span>

<span data-ttu-id="64c16-3451">\_BMK</span><span class="sxs-lookup"><span data-stu-id="64c16-3451">\_bmk</span></span>



 

<span data-ttu-id="64c16-3452">**\_ hcursor**: ein 32-Bit-Wert, der das Handle aus der cpmkreatequeryout-Meldung darstellt, die die Abfrage identifiziert, für die Statusinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3452">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="64c16-3453">**\_ BMK**: ein 32-Bit-Wert, der das Handle eines Lesezeichens angibt, dessen Position abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-3453">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="64c16-3454">2.2.3.13 cpmgetquerystatusexout</span><span class="sxs-lookup"><span data-stu-id="64c16-3454">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="64c16-3455">Die cpmgetquerystatusexout-Nachricht antwortet mit dem Status der Abfrage und anderen Statusinformationen, wie in der Abbildung unten beschrieben, auf eine cpmgetquerystatusexin-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-3455">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="64c16-3456">Das Format der cpmgetquerystatusexout-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3456">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="64c16-3457">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3457">0</span></span>

<span data-ttu-id="64c16-3458">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3458">1</span></span>

<span data-ttu-id="64c16-3459">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3459">2</span></span>

<span data-ttu-id="64c16-3460">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3460">3</span></span>

<span data-ttu-id="64c16-3461">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3461">4</span></span>

<span data-ttu-id="64c16-3462">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3462">5</span></span>

<span data-ttu-id="64c16-3463">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3463">6</span></span>

<span data-ttu-id="64c16-3464">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3464">7</span></span>

<span data-ttu-id="64c16-3465">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3465">8</span></span>

<span data-ttu-id="64c16-3466">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3466">9</span></span>

<span data-ttu-id="64c16-3467">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3467">1</span></span><br/> <span data-ttu-id="64c16-3468">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3468">0</span></span><br/>

<span data-ttu-id="64c16-3469">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3469">1</span></span>

<span data-ttu-id="64c16-3470">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3470">2</span></span>

<span data-ttu-id="64c16-3471">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3471">3</span></span>

<span data-ttu-id="64c16-3472">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3472">4</span></span>

<span data-ttu-id="64c16-3473">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3473">5</span></span>

<span data-ttu-id="64c16-3474">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3474">6</span></span>

<span data-ttu-id="64c16-3475">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3475">7</span></span>

<span data-ttu-id="64c16-3476">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3476">8</span></span>

<span data-ttu-id="64c16-3477">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3477">9</span></span>

<span data-ttu-id="64c16-3478">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3478">2</span></span><br/> <span data-ttu-id="64c16-3479">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3479">0</span></span><br/>

<span data-ttu-id="64c16-3480">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3480">1</span></span>

<span data-ttu-id="64c16-3481">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3481">2</span></span>

<span data-ttu-id="64c16-3482">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3482">3</span></span>

<span data-ttu-id="64c16-3483">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3483">4</span></span>

<span data-ttu-id="64c16-3484">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3484">5</span></span>

<span data-ttu-id="64c16-3485">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3485">6</span></span>

<span data-ttu-id="64c16-3486">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3486">7</span></span>

<span data-ttu-id="64c16-3487">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3487">8</span></span>

<span data-ttu-id="64c16-3488">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3488">9</span></span>

<span data-ttu-id="64c16-3489">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3489">3</span></span><br/> <span data-ttu-id="64c16-3490">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3490">0</span></span><br/>

<span data-ttu-id="64c16-3491">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3491">1</span></span>

<span data-ttu-id="64c16-3492">\_Stands</span><span class="sxs-lookup"><span data-stu-id="64c16-3492">\_Status</span></span>

<span data-ttu-id="64c16-3493">\_cfiltereddocuments</span><span class="sxs-lookup"><span data-stu-id="64c16-3493">\_cFilteredDocuments</span></span>

<span data-ttu-id="64c16-3494">\_cdocumentstofilter</span><span class="sxs-lookup"><span data-stu-id="64c16-3494">\_cDocumentsToFilter</span></span>

<span data-ttu-id="64c16-3495">\_dwratiofinishednenner</span><span class="sxs-lookup"><span data-stu-id="64c16-3495">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="64c16-3496">\_dwratiofinishednumerator</span><span class="sxs-lookup"><span data-stu-id="64c16-3496">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="64c16-3497">\_irowbmk</span><span class="sxs-lookup"><span data-stu-id="64c16-3497">\_iRowBmk</span></span>

<span data-ttu-id="64c16-3498">\_crowstotal</span><span class="sxs-lookup"><span data-stu-id="64c16-3498">\_cRowsTotal</span></span>



 

<span data-ttu-id="64c16-3499">**\_ Status**: einer der Stat \_ \* Werte, die im Abschnitt 2.2.3.11 angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-3499">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="64c16-3500">**\_ cfiltereddocuments**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der indizierten Dokumente angibt</span><span class="sxs-lookup"><span data-stu-id="64c16-3500">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="64c16-3501">**\_ cdocumentstofilter**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Dokumente angibt, die noch indiziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3501">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="64c16-3502">**\_ dwratiofinishednenner**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Nenner des Verhältnisses der Dokumente angibt, die von der Abfrage verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3502">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="64c16-3503">**\_ dwratiofinishednumerator**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Zähler für das Verhältnis der Dokumente angibt, die von der Abfrage verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3503">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="64c16-3504">**\_ irowbmk**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die ungefähre Position des Lesezeichens im Rowset in Bezug auf Zeilen angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3504">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="64c16-3505">**\_ crowstotal**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Zeilen im Rowset angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3505">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="64c16-3506">2.2.3.14 cpmsetbindingsin</span><span class="sxs-lookup"><span data-stu-id="64c16-3506">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="64c16-3507">Die cpmsetbindingsin-Nachricht fordert die Bindung von Spalten an ein Rowset an.</span><span class="sxs-lookup"><span data-stu-id="64c16-3507">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="64c16-3508">Der Server antwortet auf die cpmsetbindingsin-Anforderungs Nachricht, indem er den Header Abschnitt der cpmbindingsin-Nachricht mit den Ergebnissen der im Feld "Status" enthaltenen Anforderung enthält \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-3508">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="64c16-3509">Das Format der cpmsetbindingsin-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3509">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="64c16-3510">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3510">0</span></span>

<span data-ttu-id="64c16-3511">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3511">1</span></span>

<span data-ttu-id="64c16-3512">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3512">2</span></span>

<span data-ttu-id="64c16-3513">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3513">3</span></span>

<span data-ttu-id="64c16-3514">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3514">4</span></span>

<span data-ttu-id="64c16-3515">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3515">5</span></span>

<span data-ttu-id="64c16-3516">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3516">6</span></span>

<span data-ttu-id="64c16-3517">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3517">7</span></span>

<span data-ttu-id="64c16-3518">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3518">8</span></span>

<span data-ttu-id="64c16-3519">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3519">9</span></span>

<span data-ttu-id="64c16-3520">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3520">1</span></span><br/> <span data-ttu-id="64c16-3521">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3521">0</span></span><br/>

<span data-ttu-id="64c16-3522">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3522">1</span></span>

<span data-ttu-id="64c16-3523">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3523">2</span></span>

<span data-ttu-id="64c16-3524">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3524">3</span></span>

<span data-ttu-id="64c16-3525">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3525">4</span></span>

<span data-ttu-id="64c16-3526">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3526">5</span></span>

<span data-ttu-id="64c16-3527">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3527">6</span></span>

<span data-ttu-id="64c16-3528">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3528">7</span></span>

<span data-ttu-id="64c16-3529">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3529">8</span></span>

<span data-ttu-id="64c16-3530">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3530">9</span></span>

<span data-ttu-id="64c16-3531">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3531">2</span></span><br/> <span data-ttu-id="64c16-3532">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3532">0</span></span><br/>

<span data-ttu-id="64c16-3533">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3533">1</span></span>

<span data-ttu-id="64c16-3534">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3534">2</span></span>

<span data-ttu-id="64c16-3535">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3535">3</span></span>

<span data-ttu-id="64c16-3536">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3536">4</span></span>

<span data-ttu-id="64c16-3537">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3537">5</span></span>

<span data-ttu-id="64c16-3538">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3538">6</span></span>

<span data-ttu-id="64c16-3539">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3539">7</span></span>

<span data-ttu-id="64c16-3540">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3540">8</span></span>

<span data-ttu-id="64c16-3541">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3541">9</span></span>

<span data-ttu-id="64c16-3542">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3542">3</span></span><br/> <span data-ttu-id="64c16-3543">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3543">0</span></span><br/>

<span data-ttu-id="64c16-3544">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3544">1</span></span>

<span data-ttu-id="64c16-3545">\_hcursor (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-3545">\_hCursor (optional)</span></span>

<span data-ttu-id="64c16-3546">\_cbrow (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-3546">\_cbRow (optional)</span></span>

<span data-ttu-id="64c16-3547">\_cbbindingdesc (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-3547">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="64c16-3548">\_Dummy (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-3548">\_dummy (optional)</span></span>

<span data-ttu-id="64c16-3549">CColumns (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-3549">cColumns (optional)</span></span>

<span data-ttu-id="64c16-3550">acolumschlag (Variable, optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-3550">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="64c16-3551">**\_ hcursor**: ein 32-Bit-Wert, der das Handle aus der cpmkreatequeryout-Meldung darstellt, das die Zeile identifiziert, für die Bindungen festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3551">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="64c16-3552">Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-3552">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="64c16-3553">**\_ cbrow**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe einer Zeile in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3553">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="64c16-3554">Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-3554">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="64c16-3555">**\_ cbbindingdesc**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge der Felder nach dem Dummy-Feld in Bytes angibt \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-3555">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="64c16-3556">Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="64c16-3557">**\_ Dummy**: Dieses Feld wird nicht verwendet und muss ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3557">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="64c16-3558">Sie kann auf einen beliebigen Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3558">It can be set to any arbitrary value.</span></span> <span data-ttu-id="64c16-3559">Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-3559">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="64c16-3560">**CColumns**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Elemente im acolenumns-Array angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3560">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="64c16-3561">Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-3561">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="64c16-3562">**acolenns**: ein Array der ctablecolumn-Strukturen, das die Spalten einer Zeile im Rowset beschreibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3562">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="64c16-3563">Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-3563">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="64c16-3564">Strukturen im Array müssen durch 0 bis 3 Auffüll Zeichen voneinander getrennt werden, sodass jede Struktur über eine 4-Byte-Ausrichtung ab dem Anfang einer Nachricht verfügt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3564">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="64c16-3565">Bei solchen Füll Zeichen kann es sich um beliebige Werte handeln, die bei der Bestätigung ignoriert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3565">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="64c16-3566">2.2.3.15 cpmgetrowsin</span><span class="sxs-lookup"><span data-stu-id="64c16-3566">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="64c16-3567">Die cpmgetrowsin-Nachricht fordert Zeilen aus einer Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="64c16-3567">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="64c16-3568">Das Format der cpmgetrowsin-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3568">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="64c16-3569">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3569">0</span></span>

<span data-ttu-id="64c16-3570">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3570">1</span></span>

<span data-ttu-id="64c16-3571">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3571">2</span></span>

<span data-ttu-id="64c16-3572">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3572">3</span></span>

<span data-ttu-id="64c16-3573">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3573">4</span></span>

<span data-ttu-id="64c16-3574">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3574">5</span></span>

<span data-ttu-id="64c16-3575">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3575">6</span></span>

<span data-ttu-id="64c16-3576">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3576">7</span></span>

<span data-ttu-id="64c16-3577">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3577">8</span></span>

<span data-ttu-id="64c16-3578">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3578">9</span></span>

<span data-ttu-id="64c16-3579">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3579">1</span></span><br/> <span data-ttu-id="64c16-3580">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3580">0</span></span><br/>

<span data-ttu-id="64c16-3581">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3581">1</span></span>

<span data-ttu-id="64c16-3582">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3582">2</span></span>

<span data-ttu-id="64c16-3583">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3583">3</span></span>

<span data-ttu-id="64c16-3584">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3584">4</span></span>

<span data-ttu-id="64c16-3585">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3585">5</span></span>

<span data-ttu-id="64c16-3586">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3586">6</span></span>

<span data-ttu-id="64c16-3587">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3587">7</span></span>

<span data-ttu-id="64c16-3588">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3588">8</span></span>

<span data-ttu-id="64c16-3589">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3589">9</span></span>

<span data-ttu-id="64c16-3590">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3590">2</span></span><br/> <span data-ttu-id="64c16-3591">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3591">0</span></span><br/>

<span data-ttu-id="64c16-3592">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3592">1</span></span>

<span data-ttu-id="64c16-3593">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3593">2</span></span>

<span data-ttu-id="64c16-3594">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3594">3</span></span>

<span data-ttu-id="64c16-3595">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3595">4</span></span>

<span data-ttu-id="64c16-3596">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3596">5</span></span>

<span data-ttu-id="64c16-3597">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3597">6</span></span>

<span data-ttu-id="64c16-3598">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3598">7</span></span>

<span data-ttu-id="64c16-3599">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3599">8</span></span>

<span data-ttu-id="64c16-3600">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3600">9</span></span>

<span data-ttu-id="64c16-3601">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3601">3</span></span><br/> <span data-ttu-id="64c16-3602">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3602">0</span></span><br/>

<span data-ttu-id="64c16-3603">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3603">1</span></span>

<span data-ttu-id="64c16-3604">\_hcursor</span><span class="sxs-lookup"><span data-stu-id="64c16-3604">\_hCursor</span></span>

<span data-ttu-id="64c16-3605">\_crowstotransfer</span><span class="sxs-lookup"><span data-stu-id="64c16-3605">\_cRowsToTransfer</span></span>

<span data-ttu-id="64c16-3606">\_cbrowwidth</span><span class="sxs-lookup"><span data-stu-id="64c16-3606">\_cbRowWidth</span></span>

<span data-ttu-id="64c16-3607">\_cbseek</span><span class="sxs-lookup"><span data-stu-id="64c16-3607">\_cbSeek</span></span>

<span data-ttu-id="64c16-3608">\_cbreserved</span><span class="sxs-lookup"><span data-stu-id="64c16-3608">\_cbReserved</span></span>

<span data-ttu-id="64c16-3609">\_cbread-Puffer</span><span class="sxs-lookup"><span data-stu-id="64c16-3609">\_cbReadBuffer</span></span>

<span data-ttu-id="64c16-3610">\_ulclientbase</span><span class="sxs-lookup"><span data-stu-id="64c16-3610">\_ulClientBase</span></span>

<span data-ttu-id="64c16-3611">\_fbwdfetch</span><span class="sxs-lookup"><span data-stu-id="64c16-3611">\_fBwdFetch</span></span>

<span data-ttu-id="64c16-3612">ETYPE</span><span class="sxs-lookup"><span data-stu-id="64c16-3612">eType</span></span>

<span data-ttu-id="64c16-3613">\_"chapt"</span><span class="sxs-lookup"><span data-stu-id="64c16-3613">\_chapt</span></span>

<span data-ttu-id="64c16-3614">Seekdescription</span><span class="sxs-lookup"><span data-stu-id="64c16-3614">SeekDescription</span></span>

<span data-ttu-id="64c16-3615">...</span><span class="sxs-lookup"><span data-stu-id="64c16-3615">...</span></span>

<span data-ttu-id="64c16-3616">... veränder</span><span class="sxs-lookup"><span data-stu-id="64c16-3616">... (variable)</span></span>



 

<span data-ttu-id="64c16-3617">**\_ hcursor**: ein 32-Bit-Wert, der das Handle aus der cpmkreatequeryout-Meldung darstellt, die die Abfrage identifiziert, für die Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3617">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="64c16-3618">**\_ crowstotransfer**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die maximale Anzahl von Zeilen angibt, die der Client als Antwort auf diese Nachricht empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="64c16-3618">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="64c16-3619">**\_ cbrowwidth**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Länge einer Zeile in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3619">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="64c16-3620">**\_ cbseek**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe der Nachricht angibt, beginnend mit ETYPE.</span><span class="sxs-lookup"><span data-stu-id="64c16-3620">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="64c16-3621">**\_ cbreserved**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe einer cpmgetrowsout-Nachricht (in Bytes) angibt (ohne die Felder Zeilen und seekbeschreibungen).</span><span class="sxs-lookup"><span data-stu-id="64c16-3621">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="64c16-3622">Dieser Wert wird in diesem Feld dem Wert des \_ cbseek-Felds hinzugefügt und anschließend verwendet, um das Feld Offset of rows in der cpmgetrowsout-Nachricht zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3622">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="64c16-3623">**\_ cbreadbuffer**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die auf den maximalen Wert von \_ cbrowwidth oder 1000 Mal auf das \_ nächste 512 Byte gerundet festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="64c16-3623">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="64c16-3624">Der Wert darf 0x00004000 nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="64c16-3624">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="64c16-3625">**\_ ulclientbase**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Basiswert angibt, der für Zeiger Berechnungen im Zeilen Puffer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-3625">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="64c16-3626">Wenn 64-Bit-Offsets verwendet werden, wird das "reserved2"-Feld des Nachrichten Headers als obere 32-Bits und \_ ulclientbase als untere 32 Bits eines 64-Bit-Werts verwendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-3626">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="64c16-3627">Weitere Informationen finden Sie im Abschnitt 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="64c16-3627">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="64c16-3628">**\_ fbwdfetch**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Reihenfolge angibt, in der die Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3628">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="64c16-3629">Wenn der Wert auf 0x00000001 festgelegt ist, werden die Zeilen in umgekehrter Reihenfolge abgerufen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3629">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="64c16-3630">Wenn der Wert auf 0x00000000 festgelegt ist, müssen die Zeilen in der Reihenfolge der Nachrichten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3630">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="64c16-3631">Darf nicht auf andere Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3631">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="64c16-3632">**ETYPE**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die einen der folgenden Werte enthält, um den Typ des auszuführenden Vorgangs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-3632">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="64c16-3633">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-3633">Value</span></span>                         | <span data-ttu-id="64c16-3634">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-3634">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="64c16-3635">erowseeknext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-3635">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="64c16-3636">Seekdescription enthält eine crowseeknext-Struktur.</span><span class="sxs-lookup"><span data-stu-id="64c16-3636">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="64c16-3637">erowseekat 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-3637">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="64c16-3638">Seekdescription enthält eine crowseekat-Struktur.</span><span class="sxs-lookup"><span data-stu-id="64c16-3638">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="64c16-3639">erowseekatratio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-3639">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="64c16-3640">Seekdescription enthält eine crowseekatratio-Struktur.</span><span class="sxs-lookup"><span data-stu-id="64c16-3640">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="64c16-3641">erowseekbybookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="64c16-3641">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="64c16-3642">Seekdescription enthält eine crowseekbybookmark-Struktur.</span><span class="sxs-lookup"><span data-stu-id="64c16-3642">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="64c16-3643">**\_ chapt**: ein 32-Bit-Wert, der das Handle des Rowset-Kapitels darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3643">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="64c16-3644">**Seekdescription**: Dieses Feld muss eine Struktur des Typs enthalten, der durch den ETYPE-Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-3644">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="64c16-3645">2.2.3.16 cpmgetrowsout</span><span class="sxs-lookup"><span data-stu-id="64c16-3645">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="64c16-3646">Die cpmgetrowsout-Meldung antwortet mit den Zeilen einer Abfrage auf eine cpmgetrowsin-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-3646">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="64c16-3647">-Server müssen Offsets in Datentypen variabler Länge im Feld Zeilen wie folgt formatieren:</span><span class="sxs-lookup"><span data-stu-id="64c16-3647">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="64c16-3648">Der Client hat angegeben, dass es sich um ein 32-Bit-System (0x00000008 oder weniger im iclientversion-Feld von cpmconnectin) handelt: Offsets sind 32-Bit-Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3648">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="64c16-3649">Der Client hat angegeben, dass es sich um ein 64-Bit-System ( \_ iclientversion > 0x00000008 in cpmconnectin) handelt, und der Server hat angegeben, dass es sich um ein 32-Bit-System \_ handelt (Serverversion ist in cpmconnectout auf 0x00000007 festgelegt): Offsets sind 32-Bit</span><span class="sxs-lookup"><span data-stu-id="64c16-3649">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="64c16-3650">Der Client hat angegeben, dass es sich um ein 64-Bit-System ( \_ iclientversion > 0x00000008 in cpmconnectin) handelt, und der Server hat angegeben, dass es sich um ein 64-Bit-System \_ handelt (Serverversion ist in cpmconnectout auf 0x00010007 festgelegt): Offsets sind 64-Bit</span><span class="sxs-lookup"><span data-stu-id="64c16-3650">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="64c16-3651">Das Format der cpmgetrowsout-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3651">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="64c16-3652">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3652">0</span></span>

<span data-ttu-id="64c16-3653">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3653">1</span></span>

<span data-ttu-id="64c16-3654">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3654">2</span></span>

<span data-ttu-id="64c16-3655">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3655">3</span></span>

<span data-ttu-id="64c16-3656">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3656">4</span></span>

<span data-ttu-id="64c16-3657">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3657">5</span></span>

<span data-ttu-id="64c16-3658">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3658">6</span></span>

<span data-ttu-id="64c16-3659">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3659">7</span></span>

<span data-ttu-id="64c16-3660">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3660">8</span></span>

<span data-ttu-id="64c16-3661">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3661">9</span></span>

<span data-ttu-id="64c16-3662">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3662">1</span></span><br/> <span data-ttu-id="64c16-3663">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3663">0</span></span><br/>

<span data-ttu-id="64c16-3664">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3664">1</span></span>

<span data-ttu-id="64c16-3665">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3665">2</span></span>

<span data-ttu-id="64c16-3666">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3666">3</span></span>

<span data-ttu-id="64c16-3667">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3667">4</span></span>

<span data-ttu-id="64c16-3668">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3668">5</span></span>

<span data-ttu-id="64c16-3669">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3669">6</span></span>

<span data-ttu-id="64c16-3670">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3670">7</span></span>

<span data-ttu-id="64c16-3671">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3671">8</span></span>

<span data-ttu-id="64c16-3672">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3672">9</span></span>

<span data-ttu-id="64c16-3673">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3673">2</span></span><br/> <span data-ttu-id="64c16-3674">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3674">0</span></span><br/>

<span data-ttu-id="64c16-3675">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3675">1</span></span>

<span data-ttu-id="64c16-3676">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3676">2</span></span>

<span data-ttu-id="64c16-3677">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3677">3</span></span>

<span data-ttu-id="64c16-3678">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3678">4</span></span>

<span data-ttu-id="64c16-3679">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3679">5</span></span>

<span data-ttu-id="64c16-3680">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3680">6</span></span>

<span data-ttu-id="64c16-3681">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3681">7</span></span>

<span data-ttu-id="64c16-3682">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3682">8</span></span>

<span data-ttu-id="64c16-3683">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3683">9</span></span>

<span data-ttu-id="64c16-3684">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3684">3</span></span><br/> <span data-ttu-id="64c16-3685">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3685">0</span></span><br/>

<span data-ttu-id="64c16-3686">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3686">1</span></span>

<span data-ttu-id="64c16-3687">\_crowszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="64c16-3687">\_cRowsReturned</span></span>

<span data-ttu-id="64c16-3688">ETYPE</span><span class="sxs-lookup"><span data-stu-id="64c16-3688">eType</span></span>

<span data-ttu-id="64c16-3689">\_"chapt"</span><span class="sxs-lookup"><span data-stu-id="64c16-3689">\_chapt</span></span>

<span data-ttu-id="64c16-3690">Seekdescription (optional, Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-3690">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="64c16-3691">...</span><span class="sxs-lookup"><span data-stu-id="64c16-3691">...</span></span>

<span data-ttu-id="64c16-3692">...</span><span class="sxs-lookup"><span data-stu-id="64c16-3692">...</span></span>

<span data-ttu-id="64c16-3693">paddinwächst (optional, Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-3693">paddingRows (optional, variable)</span></span>

<span data-ttu-id="64c16-3694">Zeilen</span><span class="sxs-lookup"><span data-stu-id="64c16-3694">Rows</span></span>



 

<span data-ttu-id="64c16-3695">**\_ crowszurück gegeben**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der in Zeilen zurückgegebenen Zeilen angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3695">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="64c16-3696">**ETYPE**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die einen der folgenden Werte enthält, um den Typ des auszuführenden rowseek-Vorgangs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-3696">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="64c16-3697">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-3697">Value</span></span>                         | <span data-ttu-id="64c16-3698">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-3698">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="64c16-3699">erowsseeknone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-3699">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="64c16-3700">Keine seekdescription, seekdescription-Feld ignorieren.</span><span class="sxs-lookup"><span data-stu-id="64c16-3700">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="64c16-3701">erowseeknext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-3701">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="64c16-3702">Seekdescription enthält eine crowseeknext-Struktur.</span><span class="sxs-lookup"><span data-stu-id="64c16-3702">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="64c16-3703">erowseekat 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-3703">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="64c16-3704">Seekdescription enthält eine crowseekat-Struktur.</span><span class="sxs-lookup"><span data-stu-id="64c16-3704">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="64c16-3705">erowseekatratio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-3705">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="64c16-3706">Seekdescription enthält eine crowseekatratio-Struktur.</span><span class="sxs-lookup"><span data-stu-id="64c16-3706">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="64c16-3707">erowseekbybookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="64c16-3707">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="64c16-3708">Seekdescription enthält eine crowseekbybookmark-Struktur.</span><span class="sxs-lookup"><span data-stu-id="64c16-3708">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="64c16-3709">**\_ chapt**: ein 32-Bit-Wert, der das Handle des Rowset-Kapitels darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3709">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="64c16-3710">**Seekdescription**: Dieses Feld muss eine Struktur des Typs enthalten, der durch das ETYPE-Feld angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-3710">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="64c16-3711">**paddingens**: Dieses Feld muss eine ausreichende Länge aufweisen (0 bis \_ cbreserved-1 Byte), um das Feld Zeilen \_ vom Anfang einer Nachricht in den cbreserved-Offset aufzurufen, wobei \_ cbreserved der Wert in der cpmgetrowsin-Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-3711">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="64c16-3712">Bei den in diesem Feld verwendeten Füll Zeichen kann es sich um beliebige Werte handeln.</span><span class="sxs-lookup"><span data-stu-id="64c16-3712">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="64c16-3713">Dieses Feld muss vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3713">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="64c16-3714">**Rows**: Zeilendaten werden gemäß den Spalten Informationen in der aktuellen cpmsetbindingsin-Nachricht entsprechend formatiert.</span><span class="sxs-lookup"><span data-stu-id="64c16-3714">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="64c16-3715">Zeilen müssen in der Reihenfolge gespeichert werden (z. b. Zeile 1 vor Zeile 2).</span><span class="sxs-lookup"><span data-stu-id="64c16-3715">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="64c16-3716">Spalten mit fester Größe müssen in den Offsets gespeichert werden, die von der aktuellen cpmsetbindingsin-Nachricht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3716">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="64c16-3717">Spalten mit variabler Größen (z. b. Zeichen folgen) müssen wie folgt gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="64c16-3717">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="64c16-3718">Die Variablen Daten selbst (z. b. die Zeichenfolge) werden in absteigender Reihenfolge am Ende des Puffers gespeichert (z. b. ist die Auflistung aller Variablen Daten für Zeile 1 am Ende, Zeile 2 am nächsten am nächsten usw.).</span><span class="sxs-lookup"><span data-stu-id="64c16-3718">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="64c16-3719">Der Bereich mit fester Größe (am Anfang des Zeilen Puffers) muss für jede Spalte eine crowvariant enthalten, die bei dem in der aktuellen cpmsetbindingsin-Nachricht angegebenen Offset gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-3719">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="64c16-3720">VType muss den Datentyp (z.: VT \_ LPWSTR) enthalten.</span><span class="sxs-lookup"><span data-stu-id="64c16-3720">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="64c16-3721">Wenn, wie durch die Regeln am Anfang des Abschnitts in diesem Abschnitt festgelegt, 32-Bit-Offsets verwendet werden, muss das Offset-Feld in crowvariant einen 32-Bit-Wert enthalten, der den Offset der Variablen Daten vom Anfang der cpmgetrowsout-Nachricht sowie den Wert von \_ ulclientbase angibt, der in der aktuellen cpmgetrowsin-Nachricht angegeben</span><span class="sxs-lookup"><span data-stu-id="64c16-3721">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="64c16-3722">Wenn 64-Bit-Offsets verwendet werden, muss das Offset Feld in crowvariant einen 64-Bit-Wert enthalten, bei dem es sich um den Offset vom Anfang der cpmgetrowsout-Nachricht handelt, der einem 64-Bit-Wert hinzugefügt wird, der mithilfe von \_ ulclientbase als niedriger 32 Bits und \_ ulReserved2 als hohe 32 Bits erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="64c16-3722">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="64c16-3723">Wenn die cpmsetbindingsin-Nachricht z. b. die beiden Spalten Size (VT \_ I4) und Title (VT \_ LPWSTR) und \_ ulclientbase aus cpmgetrowsin den Wert 0x10000 angegeben haben, würden zwei Zeilen wie folgt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3723">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="64c16-3724">Der in grau markierte Abschnitt ist der Teil des Puffers mit fester Länge.</span><span class="sxs-lookup"><span data-stu-id="64c16-3724">The section marked in grey is the fixed-length part of the buffer.</span></span>

![cpmsetbindingsin-Nachrichten Beispiel](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="64c16-3726">2.2.3.17 cpmratiofinishedin</span><span class="sxs-lookup"><span data-stu-id="64c16-3726">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="64c16-3727">Die cpmratiofinishedin-Nachricht fordert den Abschluss Prozentsatz einer Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="64c16-3727">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="64c16-3728">Das Format der cpmratiofinishedin-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3728">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="64c16-3729">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3729">0</span></span>

<span data-ttu-id="64c16-3730">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3730">1</span></span>

<span data-ttu-id="64c16-3731">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3731">2</span></span>

<span data-ttu-id="64c16-3732">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3732">3</span></span>

<span data-ttu-id="64c16-3733">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3733">4</span></span>

<span data-ttu-id="64c16-3734">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3734">5</span></span>

<span data-ttu-id="64c16-3735">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3735">6</span></span>

<span data-ttu-id="64c16-3736">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3736">7</span></span>

<span data-ttu-id="64c16-3737">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3737">8</span></span>

<span data-ttu-id="64c16-3738">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3738">9</span></span>

<span data-ttu-id="64c16-3739">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3739">1</span></span><br/> <span data-ttu-id="64c16-3740">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3740">0</span></span><br/>

<span data-ttu-id="64c16-3741">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3741">1</span></span>

<span data-ttu-id="64c16-3742">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3742">2</span></span>

<span data-ttu-id="64c16-3743">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3743">3</span></span>

<span data-ttu-id="64c16-3744">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3744">4</span></span>

<span data-ttu-id="64c16-3745">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3745">5</span></span>

<span data-ttu-id="64c16-3746">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3746">6</span></span>

<span data-ttu-id="64c16-3747">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3747">7</span></span>

<span data-ttu-id="64c16-3748">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3748">8</span></span>

<span data-ttu-id="64c16-3749">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3749">9</span></span>

<span data-ttu-id="64c16-3750">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3750">2</span></span><br/> <span data-ttu-id="64c16-3751">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3751">0</span></span><br/>

<span data-ttu-id="64c16-3752">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3752">1</span></span>

<span data-ttu-id="64c16-3753">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3753">2</span></span>

<span data-ttu-id="64c16-3754">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3754">3</span></span>

<span data-ttu-id="64c16-3755">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3755">4</span></span>

<span data-ttu-id="64c16-3756">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3756">5</span></span>

<span data-ttu-id="64c16-3757">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3757">6</span></span>

<span data-ttu-id="64c16-3758">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3758">7</span></span>

<span data-ttu-id="64c16-3759">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3759">8</span></span>

<span data-ttu-id="64c16-3760">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3760">9</span></span>

<span data-ttu-id="64c16-3761">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3761">3</span></span><br/> <span data-ttu-id="64c16-3762">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3762">0</span></span><br/>

<span data-ttu-id="64c16-3763">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3763">1</span></span>

<span data-ttu-id="64c16-3764">\_hcursor</span><span class="sxs-lookup"><span data-stu-id="64c16-3764">\_hCursor</span></span>

<span data-ttu-id="64c16-3765">\_schnell</span><span class="sxs-lookup"><span data-stu-id="64c16-3765">\_fQuick</span></span>



 

<span data-ttu-id="64c16-3766">**\_ hcursor**: das Handle aus der cpmkreatequeryout-Nachricht, das die Abfrage identifiziert, für die Vervollständigungs Informationen angefordert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3766">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="64c16-3767">**\_ fquick**: muss auf 0x00000001 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3767">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="64c16-3768">Nicht verwendet und muss vom Server ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3768">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="64c16-3769">2.2.3.18 cpmratiofinishedout</span><span class="sxs-lookup"><span data-stu-id="64c16-3769">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="64c16-3770">Die cpmratiofinishedout-Meldung antwortet mit dem Abschluss Verhältnis einer Abfrage auf eine cpmratiofinishedin-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-3770">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="64c16-3771">Das Format der cpmratiofinishedout-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3771">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="64c16-3772">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3772">0</span></span>

<span data-ttu-id="64c16-3773">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3773">1</span></span>

<span data-ttu-id="64c16-3774">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3774">2</span></span>

<span data-ttu-id="64c16-3775">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3775">3</span></span>

<span data-ttu-id="64c16-3776">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3776">4</span></span>

<span data-ttu-id="64c16-3777">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3777">5</span></span>

<span data-ttu-id="64c16-3778">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3778">6</span></span>

<span data-ttu-id="64c16-3779">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3779">7</span></span>

<span data-ttu-id="64c16-3780">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3780">8</span></span>

<span data-ttu-id="64c16-3781">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3781">9</span></span>

<span data-ttu-id="64c16-3782">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3782">1</span></span><br/> <span data-ttu-id="64c16-3783">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3783">0</span></span><br/>

<span data-ttu-id="64c16-3784">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3784">1</span></span>

<span data-ttu-id="64c16-3785">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3785">2</span></span>

<span data-ttu-id="64c16-3786">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3786">3</span></span>

<span data-ttu-id="64c16-3787">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3787">4</span></span>

<span data-ttu-id="64c16-3788">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3788">5</span></span>

<span data-ttu-id="64c16-3789">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3789">6</span></span>

<span data-ttu-id="64c16-3790">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3790">7</span></span>

<span data-ttu-id="64c16-3791">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3791">8</span></span>

<span data-ttu-id="64c16-3792">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3792">9</span></span>

<span data-ttu-id="64c16-3793">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3793">2</span></span><br/> <span data-ttu-id="64c16-3794">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3794">0</span></span><br/>

<span data-ttu-id="64c16-3795">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3795">1</span></span>

<span data-ttu-id="64c16-3796">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3796">2</span></span>

<span data-ttu-id="64c16-3797">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3797">3</span></span>

<span data-ttu-id="64c16-3798">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3798">4</span></span>

<span data-ttu-id="64c16-3799">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3799">5</span></span>

<span data-ttu-id="64c16-3800">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3800">6</span></span>

<span data-ttu-id="64c16-3801">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3801">7</span></span>

<span data-ttu-id="64c16-3802">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3802">8</span></span>

<span data-ttu-id="64c16-3803">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3803">9</span></span>

<span data-ttu-id="64c16-3804">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3804">3</span></span><br/> <span data-ttu-id="64c16-3805">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3805">0</span></span><br/>

<span data-ttu-id="64c16-3806">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3806">1</span></span>

<span data-ttu-id="64c16-3807">\_ ulnumerator</span><span class="sxs-lookup"><span data-stu-id="64c16-3807">\_ ulNumerator</span></span>

<span data-ttu-id="64c16-3808">\_ulnenner</span><span class="sxs-lookup"><span data-stu-id="64c16-3808">\_ulDenominator</span></span>

<span data-ttu-id="64c16-3809">\_Crows</span><span class="sxs-lookup"><span data-stu-id="64c16-3809">\_cRows</span></span>

<span data-ttu-id="64c16-3810">\_Zeilen-Zeilen</span><span class="sxs-lookup"><span data-stu-id="64c16-3810">\_fNewRows</span></span>



 

<span data-ttu-id="64c16-3811">**\_ ulnumerator**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Zähler des Vervollständigungs Verhältnisses in Bezug auf Zeilen angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3811">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="64c16-3812">**\_ ulnenner**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die den Nenner des Vervollständigungs Verhältnisses in Bezug auf Zeilen angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3812">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="64c16-3813">Muss größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-3813">MUST be greater than zero.</span></span>

<span data-ttu-id="64c16-3814">**\_ Crows**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtzahl der Zeilen für die Abfrage angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3814">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="64c16-3815">" **\_ f newrows**": ein boolescher Wert, der angibt, ob neue Zeilen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-3815">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="64c16-3816">Der Wert 0x00000001 gibt an, dass neue Zeilen im Rowset verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-3816">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="64c16-3817">Der Wert 0x00000000 gibt an, dass das Rowset keine neuen Zeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-3817">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="64c16-3818">Dieses Feld darf nicht auf einen anderen Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3818">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="64c16-3819">2.2.3.19 cpmfetchvaluein</span><span class="sxs-lookup"><span data-stu-id="64c16-3819">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="64c16-3820">Die cpmfetchvaluein-Meldung fordert einen Eigenschafts Wert an, der zu groß war, um in einem Rowset zurückgegeben zu werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3820">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="64c16-3821">Wie im Abschnitt 3.2.4.2.5 angegeben, wird diese Meldung wiederholt gesendet, um alle Bytes der Eigenschaft abzurufen und \_ cbsofar für jeden zu aktualisieren, bis das \_ Feld fmoreist der cpmfetchvalueout-Nachricht **auf false** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-3821">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="64c16-3822">Das Format der cpmfetchvaluein-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3822">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="64c16-3823">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3823">0</span></span>

<span data-ttu-id="64c16-3824">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3824">1</span></span>

<span data-ttu-id="64c16-3825">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3825">2</span></span>

<span data-ttu-id="64c16-3826">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3826">3</span></span>

<span data-ttu-id="64c16-3827">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3827">4</span></span>

<span data-ttu-id="64c16-3828">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3828">5</span></span>

<span data-ttu-id="64c16-3829">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3829">6</span></span>

<span data-ttu-id="64c16-3830">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3830">7</span></span>

<span data-ttu-id="64c16-3831">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3831">8</span></span>

<span data-ttu-id="64c16-3832">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3832">9</span></span>

<span data-ttu-id="64c16-3833">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3833">1</span></span><br/> <span data-ttu-id="64c16-3834">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3834">0</span></span><br/>

<span data-ttu-id="64c16-3835">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3835">1</span></span>

<span data-ttu-id="64c16-3836">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3836">2</span></span>

<span data-ttu-id="64c16-3837">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3837">3</span></span>

<span data-ttu-id="64c16-3838">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3838">4</span></span>

<span data-ttu-id="64c16-3839">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3839">5</span></span>

<span data-ttu-id="64c16-3840">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3840">6</span></span>

<span data-ttu-id="64c16-3841">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3841">7</span></span>

<span data-ttu-id="64c16-3842">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3842">8</span></span>

<span data-ttu-id="64c16-3843">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3843">9</span></span>

<span data-ttu-id="64c16-3844">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3844">2</span></span><br/> <span data-ttu-id="64c16-3845">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3845">0</span></span><br/>

<span data-ttu-id="64c16-3846">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3846">1</span></span>

<span data-ttu-id="64c16-3847">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3847">2</span></span>

<span data-ttu-id="64c16-3848">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3848">3</span></span>

<span data-ttu-id="64c16-3849">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3849">4</span></span>

<span data-ttu-id="64c16-3850">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3850">5</span></span>

<span data-ttu-id="64c16-3851">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3851">6</span></span>

<span data-ttu-id="64c16-3852">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3852">7</span></span>

<span data-ttu-id="64c16-3853">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3853">8</span></span>

<span data-ttu-id="64c16-3854">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3854">9</span></span>

<span data-ttu-id="64c16-3855">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3855">3</span></span><br/> <span data-ttu-id="64c16-3856">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3856">0</span></span><br/>

<span data-ttu-id="64c16-3857">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3857">1</span></span>

<span data-ttu-id="64c16-3858">\_WID</span><span class="sxs-lookup"><span data-stu-id="64c16-3858">\_wid</span></span>

<span data-ttu-id="64c16-3859">\_cbsofar</span><span class="sxs-lookup"><span data-stu-id="64c16-3859">\_cbSoFar</span></span>

<span data-ttu-id="64c16-3860">\_cbpropspec</span><span class="sxs-lookup"><span data-stu-id="64c16-3860">\_cbPropSpec</span></span>

<span data-ttu-id="64c16-3861">\_cbblock</span><span class="sxs-lookup"><span data-stu-id="64c16-3861">\_cbChunk</span></span>

<span data-ttu-id="64c16-3862">PROPSPEC (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-3862">PropSpec (variable)</span></span>

<span data-ttu-id="64c16-3863">...</span><span class="sxs-lookup"><span data-stu-id="64c16-3863">...</span></span>

<span data-ttu-id="64c16-3864">\_Auffüll Zeichen (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-3864">\_padding (variable)</span></span>



 

<span data-ttu-id="64c16-3865">**\_ wid**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Dokument-ID darstellt, die das Dokument identifiziert, für das eine Eigenschaft abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-3865">**\_wid**: A 32-bit unsigned integer representing the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="64c16-3866">**\_ cbsofar**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der zuvor für diese Eigenschaft übertragenen Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-3866">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="64c16-3867">Muss in der ersten Nachricht auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3867">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="64c16-3868">**\_ cbpropspec**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Größe des PROPSPEC-Felds in Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-3868">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="64c16-3869">**\_ cbchunk**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die maximale Anzahl von Bytes enthält, die der Absender in einer cpmfetchvalueout-Nachricht annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="64c16-3869">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="64c16-3870">*Windows-Verhalten: Dieses Feld ist für alle Versionen von Windows auf 0x00004000 festgelegt.*</span><span class="sxs-lookup"><span data-stu-id="64c16-3870">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="64c16-3871">**PROPSPEC**: eine cfullpropspec-Struktur, die die abzurufende Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3871">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="64c16-3872">**\_ Auffüllung**: Dieses Feld muss die erforderliche Länge (0 bis 3 Bytes) aufweisen, um die Nachricht auf ein Vielfaches von 4 Bytes in der Länge zu füllen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3872">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="64c16-3873">Der Wert der Auffüll Bytes kann beliebiger Wert sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-3873">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="64c16-3874">Dieses Feld muss vom Empfänger ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3874">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="64c16-3875">2.2.3.20 cpmfetchvalueout</span><span class="sxs-lookup"><span data-stu-id="64c16-3875">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="64c16-3876">Die cpmfetchvalueout-Nachricht antwortet auf eine cpmfetchvaluein-Nachricht mit einem Eigenschafts Wert aus einer vorherigen Abfrage.</span><span class="sxs-lookup"><span data-stu-id="64c16-3876">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="64c16-3877">Wie im Abschnitt 3.1.5.2.8 angegeben, wird diese Nachricht nach jeder cpmfetchvaluein-Nachricht gesendet, bis alle Bytes der Eigenschaft übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3877">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="64c16-3878">Das Format der cpmfetchvalueout-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3878">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="64c16-3879">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3879">0</span></span>

<span data-ttu-id="64c16-3880">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3880">1</span></span>

<span data-ttu-id="64c16-3881">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3881">2</span></span>

<span data-ttu-id="64c16-3882">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3882">3</span></span>

<span data-ttu-id="64c16-3883">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3883">4</span></span>

<span data-ttu-id="64c16-3884">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3884">5</span></span>

<span data-ttu-id="64c16-3885">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3885">6</span></span>

<span data-ttu-id="64c16-3886">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3886">7</span></span>

<span data-ttu-id="64c16-3887">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3887">8</span></span>

<span data-ttu-id="64c16-3888">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3888">9</span></span>

<span data-ttu-id="64c16-3889">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3889">1</span></span><br/> <span data-ttu-id="64c16-3890">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3890">0</span></span><br/>

<span data-ttu-id="64c16-3891">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3891">1</span></span>

<span data-ttu-id="64c16-3892">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3892">2</span></span>

<span data-ttu-id="64c16-3893">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3893">3</span></span>

<span data-ttu-id="64c16-3894">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3894">4</span></span>

<span data-ttu-id="64c16-3895">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3895">5</span></span>

<span data-ttu-id="64c16-3896">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3896">6</span></span>

<span data-ttu-id="64c16-3897">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3897">7</span></span>

<span data-ttu-id="64c16-3898">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3898">8</span></span>

<span data-ttu-id="64c16-3899">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3899">9</span></span>

<span data-ttu-id="64c16-3900">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3900">2</span></span><br/> <span data-ttu-id="64c16-3901">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3901">0</span></span><br/>

<span data-ttu-id="64c16-3902">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3902">1</span></span>

<span data-ttu-id="64c16-3903">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3903">2</span></span>

<span data-ttu-id="64c16-3904">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3904">3</span></span>

<span data-ttu-id="64c16-3905">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3905">4</span></span>

<span data-ttu-id="64c16-3906">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3906">5</span></span>

<span data-ttu-id="64c16-3907">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3907">6</span></span>

<span data-ttu-id="64c16-3908">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3908">7</span></span>

<span data-ttu-id="64c16-3909">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3909">8</span></span>

<span data-ttu-id="64c16-3910">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3910">9</span></span>

<span data-ttu-id="64c16-3911">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3911">3</span></span><br/> <span data-ttu-id="64c16-3912">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3912">0</span></span><br/>

<span data-ttu-id="64c16-3913">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3913">1</span></span>

<span data-ttu-id="64c16-3914">\_cbValue</span><span class="sxs-lookup"><span data-stu-id="64c16-3914">\_cbValue</span></span>

<span data-ttu-id="64c16-3915">\_"gmore" vorhanden</span><span class="sxs-lookup"><span data-stu-id="64c16-3915">\_fMoreExists</span></span>

<span data-ttu-id="64c16-3916">\_"f" ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3916">\_fValueExists</span></span>

<span data-ttu-id="64c16-3917">VType</span><span class="sxs-lookup"><span data-stu-id="64c16-3917">vType</span></span>

<span data-ttu-id="64c16-3918">vValue (Variable)</span><span class="sxs-lookup"><span data-stu-id="64c16-3918">vValue (variable)</span></span>



 

<span data-ttu-id="64c16-3919">**\_ cbValue**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Gesamtgröße in Bytes in vValue enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-3919">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="64c16-3920">" **\_ fimore"**: ein boolescher Wert, der angibt, ob weitere cpmfetchvalueout-Nachrichten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-3920">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="64c16-3921">Wenn der Wert auf 0x00000001 festgelegt ist, sind weitere cpmfetchvalueout-Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3921">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="64c16-3922">Wenn Sie auf 0x00000000 festgelegt ist, sind keine weiteren cpmfetchvalueout-Meldungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="64c16-3922">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="64c16-3923">Boolescher **\_ Wert: ein** boolescher Wert, der angibt, ob ein Wert für die-Eigenschaft vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-3923">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="64c16-3924">Wenn der Wert auf 0x00000001 festgelegt ist, ist ein Wert für die-Eigenschaft vorhanden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3924">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="64c16-3925">Wenn der Wert auf 0x00000000 festgelegt ist, ist kein Wert für die Eigenschaft vorhanden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3925">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="64c16-3926">**VType**: ein Wert aus der VARENUM-Enumeration finden Sie im Abschnitt 2.2.1.1, in dem der Typ der Eigenschaft beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-3926">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="64c16-3927">**vValue**: ein Teil eines Bytearrays, das eine serializedpropertyvalue-Struktur enthält, wie im Abschnitt 2.2.1.32 angegeben, wobei der Offset des Anfangs des Teils der Wert von \_ cbsofar in cpmfetchvaluein ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-3927">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="64c16-3928">Die Länge des Teils, der durch das \_ cbValue-Feld angegeben wird, muss mit dem Wert von \_ cbblock in cpmfetchvaluein übereinstimmen, wenn \_ fmorevorhanden auf 0x00000001 festgelegt ist, und muss kleiner oder gleich dem Wert von \_ cbblock sein, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="64c16-3928">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="64c16-3929">2.2.3.21 cpmgetnotify</span><span class="sxs-lookup"><span data-stu-id="64c16-3929">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="64c16-3930">Die cpmgetnotify-Nachricht fordert an, dass der Client über Rowsetänderungen benachrichtigt werden möchte.</span><span class="sxs-lookup"><span data-stu-id="64c16-3930">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="64c16-3931">Die Nachricht darf keinen Text enthalten. nur der Nachrichten Header, wie in Abschnitt 2.2.2 angegeben, muss gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-3931">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="64c16-3932">2.2.3.22 cpmsendnotimayout</span><span class="sxs-lookup"><span data-stu-id="64c16-3932">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="64c16-3933">Die cpmsendnotifyout-Nachricht benachrichtigt den Client über eine Änderung der Ergebnisse einer Abfrage.</span><span class="sxs-lookup"><span data-stu-id="64c16-3933">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="64c16-3934">Diese Meldung wird nur gesendet, wenn eine Änderung auftritt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3934">This message is only sent when a change occurs.</span></span> <span data-ttu-id="64c16-3935">Das Format der cpmsendnotimayout-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3935">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="64c16-3936">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3936">0</span></span>

<span data-ttu-id="64c16-3937">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3937">1</span></span>

<span data-ttu-id="64c16-3938">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3938">2</span></span>

<span data-ttu-id="64c16-3939">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3939">3</span></span>

<span data-ttu-id="64c16-3940">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3940">4</span></span>

<span data-ttu-id="64c16-3941">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3941">5</span></span>

<span data-ttu-id="64c16-3942">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3942">6</span></span>

<span data-ttu-id="64c16-3943">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3943">7</span></span>

<span data-ttu-id="64c16-3944">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3944">8</span></span>

<span data-ttu-id="64c16-3945">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3945">9</span></span>

<span data-ttu-id="64c16-3946">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3946">1</span></span><br/> <span data-ttu-id="64c16-3947">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3947">0</span></span><br/>

<span data-ttu-id="64c16-3948">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3948">1</span></span>

<span data-ttu-id="64c16-3949">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3949">2</span></span>

<span data-ttu-id="64c16-3950">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3950">3</span></span>

<span data-ttu-id="64c16-3951">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3951">4</span></span>

<span data-ttu-id="64c16-3952">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3952">5</span></span>

<span data-ttu-id="64c16-3953">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3953">6</span></span>

<span data-ttu-id="64c16-3954">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3954">7</span></span>

<span data-ttu-id="64c16-3955">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3955">8</span></span>

<span data-ttu-id="64c16-3956">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3956">9</span></span>

<span data-ttu-id="64c16-3957">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3957">2</span></span><br/> <span data-ttu-id="64c16-3958">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3958">0</span></span><br/>

<span data-ttu-id="64c16-3959">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3959">1</span></span>

<span data-ttu-id="64c16-3960">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3960">2</span></span>

<span data-ttu-id="64c16-3961">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3961">3</span></span>

<span data-ttu-id="64c16-3962">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3962">4</span></span>

<span data-ttu-id="64c16-3963">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3963">5</span></span>

<span data-ttu-id="64c16-3964">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3964">6</span></span>

<span data-ttu-id="64c16-3965">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3965">7</span></span>

<span data-ttu-id="64c16-3966">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3966">8</span></span>

<span data-ttu-id="64c16-3967">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3967">9</span></span>

<span data-ttu-id="64c16-3968">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3968">3</span></span><br/> <span data-ttu-id="64c16-3969">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3969">0</span></span><br/>

<span data-ttu-id="64c16-3970">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3970">1</span></span>

<span data-ttu-id="64c16-3971">\_watchnotify</span><span class="sxs-lookup"><span data-stu-id="64c16-3971">\_watchNotify</span></span>



 

<span data-ttu-id="64c16-3972">**\_ watchnotify**: die Änderung an der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="64c16-3972">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="64c16-3973">Es muss sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="64c16-3973">It MUST be one of the following values:</span></span>



| <span data-ttu-id="64c16-3974">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-3974">Value</span></span>                                     | <span data-ttu-id="64c16-3975">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-3975">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="64c16-3976">Dbwatchnotify \_ rowschangi0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-3976">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="64c16-3977">Die Anzahl der Zeilen im abfragerowset hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="64c16-3977">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="64c16-3978">Dbwatchnotify \_ querydone 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-3978">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="64c16-3979">Die Abfrage wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="64c16-3979">The query has completed.</span></span>                            |
| <span data-ttu-id="64c16-3980">Dbwatchnotify \_ queryreausgeführte 0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-3980">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="64c16-3981">Die Abfrage wurde erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64c16-3981">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="64c16-3982">2.2.3.23 cpmgetapproximatepositionin</span><span class="sxs-lookup"><span data-stu-id="64c16-3982">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="64c16-3983">Die cpmgetapproximatepositionin-Meldung fordert die ungefähre Position eines Lesezeichens in einem Kapitel an.</span><span class="sxs-lookup"><span data-stu-id="64c16-3983">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="64c16-3984">Das Format der cpmgetapproximatepositionin-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-3984">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="64c16-3985">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3985">0</span></span>

<span data-ttu-id="64c16-3986">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3986">1</span></span>

<span data-ttu-id="64c16-3987">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3987">2</span></span>

<span data-ttu-id="64c16-3988">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3988">3</span></span>

<span data-ttu-id="64c16-3989">4</span><span class="sxs-lookup"><span data-stu-id="64c16-3989">4</span></span>

<span data-ttu-id="64c16-3990">5</span><span class="sxs-lookup"><span data-stu-id="64c16-3990">5</span></span>

<span data-ttu-id="64c16-3991">6</span><span class="sxs-lookup"><span data-stu-id="64c16-3991">6</span></span>

<span data-ttu-id="64c16-3992">7</span><span class="sxs-lookup"><span data-stu-id="64c16-3992">7</span></span>

<span data-ttu-id="64c16-3993">8</span><span class="sxs-lookup"><span data-stu-id="64c16-3993">8</span></span>

<span data-ttu-id="64c16-3994">9</span><span class="sxs-lookup"><span data-stu-id="64c16-3994">9</span></span>

<span data-ttu-id="64c16-3995">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3995">1</span></span><br/> <span data-ttu-id="64c16-3996">0</span><span class="sxs-lookup"><span data-stu-id="64c16-3996">0</span></span><br/>

<span data-ttu-id="64c16-3997">1</span><span class="sxs-lookup"><span data-stu-id="64c16-3997">1</span></span>

<span data-ttu-id="64c16-3998">2</span><span class="sxs-lookup"><span data-stu-id="64c16-3998">2</span></span>

<span data-ttu-id="64c16-3999">3</span><span class="sxs-lookup"><span data-stu-id="64c16-3999">3</span></span>

<span data-ttu-id="64c16-4000">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4000">4</span></span>

<span data-ttu-id="64c16-4001">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4001">5</span></span>

<span data-ttu-id="64c16-4002">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4002">6</span></span>

<span data-ttu-id="64c16-4003">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4003">7</span></span>

<span data-ttu-id="64c16-4004">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4004">8</span></span>

<span data-ttu-id="64c16-4005">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4005">9</span></span>

<span data-ttu-id="64c16-4006">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4006">2</span></span><br/> <span data-ttu-id="64c16-4007">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4007">0</span></span><br/>

<span data-ttu-id="64c16-4008">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4008">1</span></span>

<span data-ttu-id="64c16-4009">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4009">2</span></span>

<span data-ttu-id="64c16-4010">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4010">3</span></span>

<span data-ttu-id="64c16-4011">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4011">4</span></span>

<span data-ttu-id="64c16-4012">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4012">5</span></span>

<span data-ttu-id="64c16-4013">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4013">6</span></span>

<span data-ttu-id="64c16-4014">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4014">7</span></span>

<span data-ttu-id="64c16-4015">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4015">8</span></span>

<span data-ttu-id="64c16-4016">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4016">9</span></span>

<span data-ttu-id="64c16-4017">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4017">3</span></span><br/> <span data-ttu-id="64c16-4018">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4018">0</span></span><br/>

<span data-ttu-id="64c16-4019">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4019">1</span></span>

<span data-ttu-id="64c16-4020">\_hcursor</span><span class="sxs-lookup"><span data-stu-id="64c16-4020">\_hCursor</span></span>

<span data-ttu-id="64c16-4021">\_"chapt"</span><span class="sxs-lookup"><span data-stu-id="64c16-4021">\_chapt</span></span>

<span data-ttu-id="64c16-4022">\_BMK</span><span class="sxs-lookup"><span data-stu-id="64c16-4022">\_bmk</span></span>



 

<span data-ttu-id="64c16-4023">**\_ hcursor**: ein 32-Bit-Wert, der den aus cpmkreatequeryout abgelegten Abfrage Cursor für das Rowset mit dem Lesezeichen darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4023">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="64c16-4024">**\_ chapt**: ein 32-Bit-Wert, der das Handle für das Kapitel darstellt, das das Lesezeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-4024">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="64c16-4025">**\_ BMK**: ein 32-Bit-Wert, der das Handle für das Lesezeichen darstellt, für das die ungefähre Position abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-4025">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="64c16-4026">2.2.3.24 cpmgetapproximatepositionout</span><span class="sxs-lookup"><span data-stu-id="64c16-4026">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="64c16-4027">Die cpmgetapproximatepositionout-Nachricht antwortet auf eine cpmgetapproximatepositionin-Meldung, die die ungefähre Position des Lesezeichens im Kapitel beschreibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4027">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="64c16-4028">Das Format der cpmgetapproximatepositionout-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-4028">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="64c16-4029">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4029">0</span></span>

<span data-ttu-id="64c16-4030">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4030">1</span></span>

<span data-ttu-id="64c16-4031">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4031">2</span></span>

<span data-ttu-id="64c16-4032">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4032">3</span></span>

<span data-ttu-id="64c16-4033">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4033">4</span></span>

<span data-ttu-id="64c16-4034">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4034">5</span></span>

<span data-ttu-id="64c16-4035">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4035">6</span></span>

<span data-ttu-id="64c16-4036">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4036">7</span></span>

<span data-ttu-id="64c16-4037">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4037">8</span></span>

<span data-ttu-id="64c16-4038">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4038">9</span></span>

<span data-ttu-id="64c16-4039">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4039">1</span></span><br/> <span data-ttu-id="64c16-4040">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4040">0</span></span><br/>

<span data-ttu-id="64c16-4041">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4041">1</span></span>

<span data-ttu-id="64c16-4042">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4042">2</span></span>

<span data-ttu-id="64c16-4043">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4043">3</span></span>

<span data-ttu-id="64c16-4044">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4044">4</span></span>

<span data-ttu-id="64c16-4045">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4045">5</span></span>

<span data-ttu-id="64c16-4046">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4046">6</span></span>

<span data-ttu-id="64c16-4047">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4047">7</span></span>

<span data-ttu-id="64c16-4048">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4048">8</span></span>

<span data-ttu-id="64c16-4049">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4049">9</span></span>

<span data-ttu-id="64c16-4050">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4050">2</span></span><br/> <span data-ttu-id="64c16-4051">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4051">0</span></span><br/>

<span data-ttu-id="64c16-4052">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4052">1</span></span>

<span data-ttu-id="64c16-4053">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4053">2</span></span>

<span data-ttu-id="64c16-4054">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4054">3</span></span>

<span data-ttu-id="64c16-4055">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4055">4</span></span>

<span data-ttu-id="64c16-4056">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4056">5</span></span>

<span data-ttu-id="64c16-4057">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4057">6</span></span>

<span data-ttu-id="64c16-4058">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4058">7</span></span>

<span data-ttu-id="64c16-4059">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4059">8</span></span>

<span data-ttu-id="64c16-4060">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4060">9</span></span>

<span data-ttu-id="64c16-4061">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4061">3</span></span><br/> <span data-ttu-id="64c16-4062">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4062">0</span></span><br/>

<span data-ttu-id="64c16-4063">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4063">1</span></span>

<span data-ttu-id="64c16-4064">\_Dividend</span><span class="sxs-lookup"><span data-stu-id="64c16-4064">\_numerator</span></span>

<span data-ttu-id="64c16-4065">\_Divisor</span><span class="sxs-lookup"><span data-stu-id="64c16-4065">\_denominator</span></span>



 

<span data-ttu-id="64c16-4066">**\_ Zähler**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Zeilennummer des Lesezeichens im Rowset enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-4066">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="64c16-4067">Wenn keine Zeilen vorhanden sind, muss dieses Feld auf 0x00000000 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4067">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="64c16-4068">**\_ Nenner**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl der Zeilen im Rowset enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-4068">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="64c16-4069">2.2.3.25 cpmcomparebmkin</span><span class="sxs-lookup"><span data-stu-id="64c16-4069">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="64c16-4070">Die cpmcomparebmkin-Nachricht fordert einen Vergleich zweier Lesezeichen in einem Kapitel an.</span><span class="sxs-lookup"><span data-stu-id="64c16-4070">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="64c16-4071">Das Format der cpmcomparebmkin-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-4071">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="64c16-4072">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4072">0</span></span>

<span data-ttu-id="64c16-4073">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4073">1</span></span>

<span data-ttu-id="64c16-4074">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4074">2</span></span>

<span data-ttu-id="64c16-4075">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4075">3</span></span>

<span data-ttu-id="64c16-4076">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4076">4</span></span>

<span data-ttu-id="64c16-4077">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4077">5</span></span>

<span data-ttu-id="64c16-4078">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4078">6</span></span>

<span data-ttu-id="64c16-4079">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4079">7</span></span>

<span data-ttu-id="64c16-4080">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4080">8</span></span>

<span data-ttu-id="64c16-4081">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4081">9</span></span>

<span data-ttu-id="64c16-4082">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4082">1</span></span><br/> <span data-ttu-id="64c16-4083">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4083">0</span></span><br/>

<span data-ttu-id="64c16-4084">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4084">1</span></span>

<span data-ttu-id="64c16-4085">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4085">2</span></span>

<span data-ttu-id="64c16-4086">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4086">3</span></span>

<span data-ttu-id="64c16-4087">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4087">4</span></span>

<span data-ttu-id="64c16-4088">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4088">5</span></span>

<span data-ttu-id="64c16-4089">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4089">6</span></span>

<span data-ttu-id="64c16-4090">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4090">7</span></span>

<span data-ttu-id="64c16-4091">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4091">8</span></span>

<span data-ttu-id="64c16-4092">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4092">9</span></span>

<span data-ttu-id="64c16-4093">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4093">2</span></span><br/> <span data-ttu-id="64c16-4094">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4094">0</span></span><br/>

<span data-ttu-id="64c16-4095">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4095">1</span></span>

<span data-ttu-id="64c16-4096">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4096">2</span></span>

<span data-ttu-id="64c16-4097">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4097">3</span></span>

<span data-ttu-id="64c16-4098">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4098">4</span></span>

<span data-ttu-id="64c16-4099">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4099">5</span></span>

<span data-ttu-id="64c16-4100">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4100">6</span></span>

<span data-ttu-id="64c16-4101">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4101">7</span></span>

<span data-ttu-id="64c16-4102">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4102">8</span></span>

<span data-ttu-id="64c16-4103">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4103">9</span></span>

<span data-ttu-id="64c16-4104">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4104">3</span></span><br/> <span data-ttu-id="64c16-4105">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4105">0</span></span><br/>

<span data-ttu-id="64c16-4106">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4106">1</span></span>

<span data-ttu-id="64c16-4107">\_hcursor</span><span class="sxs-lookup"><span data-stu-id="64c16-4107">\_hCursor</span></span>

<span data-ttu-id="64c16-4108">\_"chapt"</span><span class="sxs-lookup"><span data-stu-id="64c16-4108">\_chapt</span></span>

<span data-ttu-id="64c16-4109">\_bmkfirst</span><span class="sxs-lookup"><span data-stu-id="64c16-4109">\_bmkFirst</span></span>

<span data-ttu-id="64c16-4110">\_bmksecond</span><span class="sxs-lookup"><span data-stu-id="64c16-4110">\_bmkSecond</span></span>



 

<span data-ttu-id="64c16-4111">\_**hcursor**: ein 32-Bit-Wert, der das Handle aus der cpmkreatequeryout-Nachricht für das Rowset darstellt, das die Lesezeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-4111">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="64c16-4112">\_**chapt**: ein 32-Bit-Wert, der das Handle des Kapitels darstellt, das die zu vergleichenden Lesezeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-4112">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="64c16-4113">\_**bmkfirst**: ein 32-Bit-Wert, der das Handle für das erste zu vergleichende Lesezeichen darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4113">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="64c16-4114">\_**bmksecond**: ein 32-Bit-Wert, der das Handle für das zweite zu vergleichende Lesezeichen darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4114">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="64c16-4115">2.2.3.26 cpmcomparebmkout</span><span class="sxs-lookup"><span data-stu-id="64c16-4115">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="64c16-4116">Die cpmcomparebmkout-Nachricht antwortet auf eine cpmcomparebmkin-Nachricht mit dem Vergleich der beiden Lesezeichen im Kapitel.</span><span class="sxs-lookup"><span data-stu-id="64c16-4116">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="64c16-4117">Das Format der cpmcomparebmkout-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-4117">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="64c16-4118">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4118">0</span></span>

<span data-ttu-id="64c16-4119">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4119">1</span></span>

<span data-ttu-id="64c16-4120">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4120">2</span></span>

<span data-ttu-id="64c16-4121">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4121">3</span></span>

<span data-ttu-id="64c16-4122">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4122">4</span></span>

<span data-ttu-id="64c16-4123">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4123">5</span></span>

<span data-ttu-id="64c16-4124">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4124">6</span></span>

<span data-ttu-id="64c16-4125">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4125">7</span></span>

<span data-ttu-id="64c16-4126">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4126">8</span></span>

<span data-ttu-id="64c16-4127">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4127">9</span></span>

<span data-ttu-id="64c16-4128">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4128">1</span></span><br/> <span data-ttu-id="64c16-4129">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4129">0</span></span><br/>

<span data-ttu-id="64c16-4130">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4130">1</span></span>

<span data-ttu-id="64c16-4131">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4131">2</span></span>

<span data-ttu-id="64c16-4132">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4132">3</span></span>

<span data-ttu-id="64c16-4133">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4133">4</span></span>

<span data-ttu-id="64c16-4134">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4134">5</span></span>

<span data-ttu-id="64c16-4135">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4135">6</span></span>

<span data-ttu-id="64c16-4136">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4136">7</span></span>

<span data-ttu-id="64c16-4137">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4137">8</span></span>

<span data-ttu-id="64c16-4138">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4138">9</span></span>

<span data-ttu-id="64c16-4139">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4139">2</span></span><br/> <span data-ttu-id="64c16-4140">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4140">0</span></span><br/>

<span data-ttu-id="64c16-4141">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4141">1</span></span>

<span data-ttu-id="64c16-4142">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4142">2</span></span>

<span data-ttu-id="64c16-4143">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4143">3</span></span>

<span data-ttu-id="64c16-4144">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4144">4</span></span>

<span data-ttu-id="64c16-4145">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4145">5</span></span>

<span data-ttu-id="64c16-4146">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4146">6</span></span>

<span data-ttu-id="64c16-4147">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4147">7</span></span>

<span data-ttu-id="64c16-4148">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4148">8</span></span>

<span data-ttu-id="64c16-4149">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4149">9</span></span>

<span data-ttu-id="64c16-4150">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4150">3</span></span><br/> <span data-ttu-id="64c16-4151">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4151">0</span></span><br/>

<span data-ttu-id="64c16-4152">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4152">1</span></span>

<span data-ttu-id="64c16-4153">\_dwcomparison</span><span class="sxs-lookup"><span data-stu-id="64c16-4153">\_dwComparison</span></span>



 

<span data-ttu-id="64c16-4154">\_**dwcomparison**: einer der folgenden Werte, der die relativen Positionen der beiden Lesezeichen im Kapitel angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4154">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="64c16-4155">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-4155">Value</span></span>                               | <span data-ttu-id="64c16-4156">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-4156">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="64c16-4157">DbCompare \_ lt 0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-4157">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="64c16-4158">Das erste Lesezeichen wird vor dem zweiten positioniert.</span><span class="sxs-lookup"><span data-stu-id="64c16-4158">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="64c16-4159">DbCompare \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="64c16-4159">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="64c16-4160">Das erste Lesezeichen hat dieselbe Position wie die zweite.</span><span class="sxs-lookup"><span data-stu-id="64c16-4160">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="64c16-4161">DbCompare \_ gt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="64c16-4161">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="64c16-4162">Das erste Lesezeichen ist nach dem zweiten positioniert.</span><span class="sxs-lookup"><span data-stu-id="64c16-4162">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="64c16-4163">DbCompare \_ ne 0x00000003</span><span class="sxs-lookup"><span data-stu-id="64c16-4163">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="64c16-4164">Das erste Lesezeichen hat nicht die gleiche Position wie die zweite.</span><span class="sxs-lookup"><span data-stu-id="64c16-4164">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="64c16-4165">DbCompare, nicht \_ vergleichbar mit 0x00000004</span><span class="sxs-lookup"><span data-stu-id="64c16-4165">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="64c16-4166">Das erste Lesezeichen ist nicht mit dem zweiten Lesezeichen vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="64c16-4166">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="64c16-4167">2.2.3.27 cpmrestartpositionin</span><span class="sxs-lookup"><span data-stu-id="64c16-4167">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="64c16-4168">Die cpmrestartpositionin-Meldung verschiebt die Abruf Position für einen Cursor an den Anfang des Kapitels.</span><span class="sxs-lookup"><span data-stu-id="64c16-4168">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="64c16-4169">Wie im Abschnitt 3.1.5.2.12 angegeben, antwortet der Server mit derselben Nachricht, wobei die Ergebnisse der Anforderung im \_ Status-Feld des CISP-Headers enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-4169">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="64c16-4170">Das Format der cpmrestartpositionin-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-4170">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="64c16-4171">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4171">0</span></span>

<span data-ttu-id="64c16-4172">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4172">1</span></span>

<span data-ttu-id="64c16-4173">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4173">2</span></span>

<span data-ttu-id="64c16-4174">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4174">3</span></span>

<span data-ttu-id="64c16-4175">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4175">4</span></span>

<span data-ttu-id="64c16-4176">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4176">5</span></span>

<span data-ttu-id="64c16-4177">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4177">6</span></span>

<span data-ttu-id="64c16-4178">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4178">7</span></span>

<span data-ttu-id="64c16-4179">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4179">8</span></span>

<span data-ttu-id="64c16-4180">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4180">9</span></span>

<span data-ttu-id="64c16-4181">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4181">1</span></span><br/> <span data-ttu-id="64c16-4182">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4182">0</span></span><br/>

<span data-ttu-id="64c16-4183">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4183">1</span></span>

<span data-ttu-id="64c16-4184">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4184">2</span></span>

<span data-ttu-id="64c16-4185">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4185">3</span></span>

<span data-ttu-id="64c16-4186">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4186">4</span></span>

<span data-ttu-id="64c16-4187">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4187">5</span></span>

<span data-ttu-id="64c16-4188">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4188">6</span></span>

<span data-ttu-id="64c16-4189">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4189">7</span></span>

<span data-ttu-id="64c16-4190">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4190">8</span></span>

<span data-ttu-id="64c16-4191">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4191">9</span></span>

<span data-ttu-id="64c16-4192">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4192">2</span></span><br/> <span data-ttu-id="64c16-4193">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4193">0</span></span><br/>

<span data-ttu-id="64c16-4194">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4194">1</span></span>

<span data-ttu-id="64c16-4195">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4195">2</span></span>

<span data-ttu-id="64c16-4196">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4196">3</span></span>

<span data-ttu-id="64c16-4197">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4197">4</span></span>

<span data-ttu-id="64c16-4198">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4198">5</span></span>

<span data-ttu-id="64c16-4199">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4199">6</span></span>

<span data-ttu-id="64c16-4200">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4200">7</span></span>

<span data-ttu-id="64c16-4201">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4201">8</span></span>

<span data-ttu-id="64c16-4202">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4202">9</span></span>

<span data-ttu-id="64c16-4203">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4203">3</span></span><br/> <span data-ttu-id="64c16-4204">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4204">0</span></span><br/>

<span data-ttu-id="64c16-4205">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4205">1</span></span>

<span data-ttu-id="64c16-4206">\_hcursor (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-4206">\_hCursor (optional)</span></span>

<span data-ttu-id="64c16-4207">\_chapt (optional)</span><span class="sxs-lookup"><span data-stu-id="64c16-4207">\_chapt (optional)</span></span>



 

<span data-ttu-id="64c16-4208">**\_ hcursor**: ein 32-Bit-Wert, der das Handle darstellt, das aus einer cpmkreatequeryout-Nachricht abgerufen wird, die die Abfrage identifiziert, für die die Position neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-4208">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="64c16-4209">Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-4209">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="64c16-4210">**\_ chapt**: ein 32-Bit-Wert, der das Handle eines Kapitels darstellt, aus dem Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4210">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="64c16-4211">Dieses Feld muss vorhanden sein, wenn die Nachricht vom Client gesendet wird, und muss nicht vorhanden sein, wenn die Nachricht vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-4211">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="64c16-4212">2.2.3.28 cpmfreecursorin</span><span class="sxs-lookup"><span data-stu-id="64c16-4212">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="64c16-4213">Die cpmfreecursorin-Meldung fordert die Freigabe eines Cursors an.</span><span class="sxs-lookup"><span data-stu-id="64c16-4213">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="64c16-4214">Das Format der cpmfreecursorin-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-4214">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="64c16-4215">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4215">0</span></span>

<span data-ttu-id="64c16-4216">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4216">1</span></span>

<span data-ttu-id="64c16-4217">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4217">2</span></span>

<span data-ttu-id="64c16-4218">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4218">3</span></span>

<span data-ttu-id="64c16-4219">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4219">4</span></span>

<span data-ttu-id="64c16-4220">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4220">5</span></span>

<span data-ttu-id="64c16-4221">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4221">6</span></span>

<span data-ttu-id="64c16-4222">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4222">7</span></span>

<span data-ttu-id="64c16-4223">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4223">8</span></span>

<span data-ttu-id="64c16-4224">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4224">9</span></span>

<span data-ttu-id="64c16-4225">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4225">1</span></span><br/> <span data-ttu-id="64c16-4226">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4226">0</span></span><br/>

<span data-ttu-id="64c16-4227">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4227">1</span></span>

<span data-ttu-id="64c16-4228">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4228">2</span></span>

<span data-ttu-id="64c16-4229">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4229">3</span></span>

<span data-ttu-id="64c16-4230">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4230">4</span></span>

<span data-ttu-id="64c16-4231">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4231">5</span></span>

<span data-ttu-id="64c16-4232">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4232">6</span></span>

<span data-ttu-id="64c16-4233">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4233">7</span></span>

<span data-ttu-id="64c16-4234">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4234">8</span></span>

<span data-ttu-id="64c16-4235">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4235">9</span></span>

<span data-ttu-id="64c16-4236">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4236">2</span></span><br/> <span data-ttu-id="64c16-4237">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4237">0</span></span><br/>

<span data-ttu-id="64c16-4238">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4238">1</span></span>

<span data-ttu-id="64c16-4239">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4239">2</span></span>

<span data-ttu-id="64c16-4240">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4240">3</span></span>

<span data-ttu-id="64c16-4241">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4241">4</span></span>

<span data-ttu-id="64c16-4242">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4242">5</span></span>

<span data-ttu-id="64c16-4243">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4243">6</span></span>

<span data-ttu-id="64c16-4244">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4244">7</span></span>

<span data-ttu-id="64c16-4245">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4245">8</span></span>

<span data-ttu-id="64c16-4246">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4246">9</span></span>

<span data-ttu-id="64c16-4247">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4247">3</span></span><br/> <span data-ttu-id="64c16-4248">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4248">0</span></span><br/>

<span data-ttu-id="64c16-4249">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4249">1</span></span>

<span data-ttu-id="64c16-4250">\_hcursor</span><span class="sxs-lookup"><span data-stu-id="64c16-4250">\_hCursor</span></span>



 

<span data-ttu-id="64c16-4251">**\_ hcursor**: ein 32-Bit-Wert, der das Handle des Cursors von der cpmkreatequeryout-Nachricht darstellt, die freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-4251">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="64c16-4252">2.2.3.29 cpmfreecursorout</span><span class="sxs-lookup"><span data-stu-id="64c16-4252">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="64c16-4253">Die cpmfreecursorout-Nachricht antwortet auf eine cpmfreecursorin-Nachricht mit den Ergebnissen der Freigabe eines Cursors.</span><span class="sxs-lookup"><span data-stu-id="64c16-4253">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="64c16-4254">Das Format der cpmfreecursorout-Nachricht, die auf den Header folgt, lautet:</span><span class="sxs-lookup"><span data-stu-id="64c16-4254">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="64c16-4255">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4255">0</span></span>

<span data-ttu-id="64c16-4256">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4256">1</span></span>

<span data-ttu-id="64c16-4257">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4257">2</span></span>

<span data-ttu-id="64c16-4258">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4258">3</span></span>

<span data-ttu-id="64c16-4259">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4259">4</span></span>

<span data-ttu-id="64c16-4260">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4260">5</span></span>

<span data-ttu-id="64c16-4261">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4261">6</span></span>

<span data-ttu-id="64c16-4262">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4262">7</span></span>

<span data-ttu-id="64c16-4263">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4263">8</span></span>

<span data-ttu-id="64c16-4264">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4264">9</span></span>

<span data-ttu-id="64c16-4265">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4265">1</span></span><br/> <span data-ttu-id="64c16-4266">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4266">0</span></span><br/>

<span data-ttu-id="64c16-4267">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4267">1</span></span>

<span data-ttu-id="64c16-4268">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4268">2</span></span>

<span data-ttu-id="64c16-4269">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4269">3</span></span>

<span data-ttu-id="64c16-4270">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4270">4</span></span>

<span data-ttu-id="64c16-4271">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4271">5</span></span>

<span data-ttu-id="64c16-4272">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4272">6</span></span>

<span data-ttu-id="64c16-4273">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4273">7</span></span>

<span data-ttu-id="64c16-4274">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4274">8</span></span>

<span data-ttu-id="64c16-4275">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4275">9</span></span>

<span data-ttu-id="64c16-4276">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4276">2</span></span><br/> <span data-ttu-id="64c16-4277">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4277">0</span></span><br/>

<span data-ttu-id="64c16-4278">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4278">1</span></span>

<span data-ttu-id="64c16-4279">2</span><span class="sxs-lookup"><span data-stu-id="64c16-4279">2</span></span>

<span data-ttu-id="64c16-4280">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4280">3</span></span>

<span data-ttu-id="64c16-4281">4</span><span class="sxs-lookup"><span data-stu-id="64c16-4281">4</span></span>

<span data-ttu-id="64c16-4282">5</span><span class="sxs-lookup"><span data-stu-id="64c16-4282">5</span></span>

<span data-ttu-id="64c16-4283">6</span><span class="sxs-lookup"><span data-stu-id="64c16-4283">6</span></span>

<span data-ttu-id="64c16-4284">7</span><span class="sxs-lookup"><span data-stu-id="64c16-4284">7</span></span>

<span data-ttu-id="64c16-4285">8</span><span class="sxs-lookup"><span data-stu-id="64c16-4285">8</span></span>

<span data-ttu-id="64c16-4286">9</span><span class="sxs-lookup"><span data-stu-id="64c16-4286">9</span></span>

<span data-ttu-id="64c16-4287">3</span><span class="sxs-lookup"><span data-stu-id="64c16-4287">3</span></span><br/> <span data-ttu-id="64c16-4288">0</span><span class="sxs-lookup"><span data-stu-id="64c16-4288">0</span></span><br/>

<span data-ttu-id="64c16-4289">1</span><span class="sxs-lookup"><span data-stu-id="64c16-4289">1</span></span>

<span data-ttu-id="64c16-4290">\_ccurrsorsrestdauer</span><span class="sxs-lookup"><span data-stu-id="64c16-4290">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="64c16-4291">**\_ ccursorsrestwert**: eine 32-Bit-Ganzzahl ohne Vorzeichen, die die Anzahl von Cursorn angibt, die noch für die Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4291">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="64c16-4292">2.2.3.30 cpmdisconnect</span><span class="sxs-lookup"><span data-stu-id="64c16-4292">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="64c16-4293">Die cpmdisconnect-Nachricht beendet die Verbindung mit dem Server.</span><span class="sxs-lookup"><span data-stu-id="64c16-4293">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="64c16-4294">Die Nachricht darf keinen Text enthalten. nur der Nachrichten Header, wie in Abschnitt 2.2.2 angegeben, muss gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4294">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="64c16-4295">2.2.4-Fehler</span><span class="sxs-lookup"><span data-stu-id="64c16-4295">2.2.4 Errors</span></span>

<span data-ttu-id="64c16-4296">Alle Content Index Service-Protokollnachrichten müssen bei Erfolg 0x00000000 zurückgeben. Andernfalls geben Sie einen 32-Bit-Fehlercode ungleich 0 (null) zurück, der entweder ein HRESULT-oder ein NTSTATUS-Wert sein kann (siehe Abschnitt 1,8).</span><span class="sxs-lookup"><span data-stu-id="64c16-4296">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="64c16-4297">Wenn ein Puffer zu klein ist, um ein Ergebnis zu erhalten, muss ein Status \_ Code \_ mit unzureichenden Ressourcen (0xc0000009a) zurückgegeben werden, und der fehlgeschlagene Vorgang sollte mit einem größeren Puffer wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4297">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="64c16-4298">Alle anderen Fehler Werte müssen identisch behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4298">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="64c16-4299">(Beachten Sie, dass sich die Nummerierungen von HRESULT und NTSTATUS derzeit nicht überlappen, außer mit Werten gleicher Bedeutung, aber auch wenn Sie in Zukunft Konflikte verursachen würden, würden Sie keine Protokoll Probleme verursachen, solange der Wert für "Status \_ " Unzureichende \_ Ressourcen bleiben eindeutig, da alle anderen Fehler Werte identisch behandelt werden.)</span><span class="sxs-lookup"><span data-stu-id="64c16-4299">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="64c16-4300">3 Protokolldetails</span><span class="sxs-lookup"><span data-stu-id="64c16-4300">3 Protocol Details</span></span>

-   [<span data-ttu-id="64c16-4301">3,1 Server Details</span><span class="sxs-lookup"><span data-stu-id="64c16-4301">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="64c16-4302">3,2 Client Details</span><span class="sxs-lookup"><span data-stu-id="64c16-4302">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="64c16-4303">CISP-Nachrichten Anforderungen für die Remote Abfrage von Indizierungs Dienst Katalogen erfordern keine bestimmte Sequenz.</span><span class="sxs-lookup"><span data-stu-id="64c16-4303">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="64c16-4304">Es wird empfohlen, dass die höhere Ebene eine sinnvolle Nachrichten Sequenz befolgt, wie bei Nachrichten, die von dieser Sequenz oder mit ungültigen Daten empfangen werden, antwortet der Server jedoch mit einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="64c16-4304">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="64c16-4305">Einige Nachrichten sind auch von der höheren Ebene abhängig, die gültige Daten bereitstellt, die zuvor in der Sequenz in Nachrichten empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4305">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="64c16-4306">Eine typische Nachrichten Sequenz für eine einfache Abfrage von einem Client an einen Remote Computer ist im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4306">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![Nachrichten Sequenz für einfache Abfrage](images/protocoldetails.jpg)

<span data-ttu-id="64c16-4308">Die Nachrichten, die im vorangehenden Diagramm dargestellt werden, stellen eine Teilmenge aller CISP-Nachrichten dar, die zum Abfragen eines remoteindizierungs-Dienst Katalogs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4308">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="64c16-4309">3,1 Server Details</span><span class="sxs-lookup"><span data-stu-id="64c16-4309">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="64c16-4310">3.1.1 Abstraktes Datenmodell</span><span class="sxs-lookup"><span data-stu-id="64c16-4310">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="64c16-4311">Im folgenden Abschnitt werden Daten und Status angegeben, die vom CISP-Server verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4311">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="64c16-4312">Die hier bereitgestellten Daten dienen dazu, die Erläuterung der Verhalten des Protokolls zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4312">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="64c16-4313">In diesem Abschnitt wird nicht vorgeschrieben, dass Implementierungen dieses Modells einhalten, solange das externe Verhalten mit dem in diesem Dokument beschriebenen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4313">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="64c16-4314">Ein Index Dienst, der den CISP implementiert, muss die folgenden abstrakten Datenelemente verwalten:</span><span class="sxs-lookup"><span data-stu-id="64c16-4314">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="64c16-4315">Die Liste der Clients, die mit dem Server verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-4315">The list of clients connected to the server</span></span>
-   <span data-ttu-id="64c16-4316">Informationen zu den einzelnen Clients, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="64c16-4316">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="64c16-4317">Client Version (wie in der im Abschnitt 2.2.3.6 angegebenen Meldung "cpmconnectin" angegeben)</span><span class="sxs-lookup"><span data-stu-id="64c16-4317">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="64c16-4318">Katalog, der dem Client zugeordnet ist (durch eine cpmconnectin-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="64c16-4318">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="64c16-4319">Zusätzliche Client Eigenschaften, wie im Abschnitt 2.2.1.21.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4319">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="64c16-4320">Suchabfrage des Clients</span><span class="sxs-lookup"><span data-stu-id="64c16-4320">Client's search query</span></span>
    -   <span data-ttu-id="64c16-4321">Liste der Cursor Handles für die Abfrage und Position im Resultset für jedes handle.</span><span class="sxs-lookup"><span data-stu-id="64c16-4321">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="64c16-4322">Aktueller Satz von Bindungen</span><span class="sxs-lookup"><span data-stu-id="64c16-4322">Current set of bindings</span></span>
    -   <span data-ttu-id="64c16-4323">Aktueller Status der Abfrage, die (für jeden Cursor) umfasst:</span><span class="sxs-lookup"><span data-stu-id="64c16-4323">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="64c16-4324">Anzahl von Zeilen im Abfrageergebnis</span><span class="sxs-lookup"><span data-stu-id="64c16-4324">Number of rows in query result</span></span>
        -   <span data-ttu-id="64c16-4325">Zähler und Nenner des abfrageabschlusses</span><span class="sxs-lookup"><span data-stu-id="64c16-4325">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="64c16-4326">Die letzte Anzahl von Zeilen, die von der aktuellen cpmratiofinishedout-Meldung für diesen Cursor gemeldet wurden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4326">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="64c16-4327">Ob die Abfrage vom Server auf Änderungen in den Abfrage Ergebnissen überwacht wird und ob Sie überwacht wird, was sich in den Abfrage Ergebnissen geändert hat, seit Sie zuletzt von cpmsendnotifyout an den Client gemeldet wurde</span><span class="sxs-lookup"><span data-stu-id="64c16-4327">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="64c16-4328">Liste der Kapitel Handles, die von dieser Abfrage an einen Client bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4328">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="64c16-4329">Liste der Lesezeichen Handles für jeden Cursor, die von dieser Abfrage an einen Client bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4329">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="64c16-4330">Der aktuelle Zustand des Indizierungs Dienstanbieter, der möglicherweise "nicht initialisiert", "wird ausgeführt" oder "heruntergefahren" ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4330">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="64c16-4331">Beachten Sie, dass sich der Server in den meisten Fällen im Zustand "wird ausgeführt" befindet.</span><span class="sxs-lookup"><span data-stu-id="64c16-4331">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="64c16-4332">Im folgenden finden Sie das zustandsautomatdiagramm für den Server:</span><span class="sxs-lookup"><span data-stu-id="64c16-4332">Following is the state machine diagram for the server:</span></span>

    ![Zustands Automaten Diagramm des Index Dienst Servers](images/abstractdatamodel.jpg)

-   <span data-ttu-id="64c16-4334">Katalog spezifische Informationen: Anzahl der indizierten Dokumente, Indexgröße, Anzahl eindeutiger Schlüssel usw. (siehe Abschnitt 2.2.3.1 for Complete List), State (entspricht den Werten von dwnewstate im Abschnitt 2.2.3.2).</span><span class="sxs-lookup"><span data-stu-id="64c16-4334">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="64c16-4335">Für jede unterstützte Sprache eine Datenbank von Wort Variationen, wie im Abschnitt 2.2.1.3 erläutert.</span><span class="sxs-lookup"><span data-stu-id="64c16-4335">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="64c16-4336">3.1.2 Zeitgeber</span><span class="sxs-lookup"><span data-stu-id="64c16-4336">3.1.2 Timers</span></span>

<span data-ttu-id="64c16-4337">Es sind keine protokolltimer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="64c16-4337">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="64c16-4338">3.1.3 Initialisierung</span><span class="sxs-lookup"><span data-stu-id="64c16-4338">3.1.3 Initialization</span></span>

<span data-ttu-id="64c16-4339">Der Server muss bei der Initialisierung seinen Status auf "nicht initialisiert" festlegen und mit dem lauschen auf Nachrichten auf dem Named Pipe beginnen, der in Abschnitt 1,9 angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4339">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="64c16-4340">Nachdem eine andere interne Initialisierung durchgeführt wurde, muss Sie in den Status "wird ausgeführt" übergehen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4340">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="64c16-4341">3.1.4 Ausgelöste Ereignisse auf höherer Ebene</span><span class="sxs-lookup"><span data-stu-id="64c16-4341">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="64c16-4342">Keine.</span><span class="sxs-lookup"><span data-stu-id="64c16-4342">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="64c16-4343">3.1.5 Nachrichtenverarbeitungs-und Sequenz Regeln</span><span class="sxs-lookup"><span data-stu-id="64c16-4343">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="64c16-4344">Wenn bei der Verarbeitung einer von einem Client gesendeten Nachricht ein Fehler auftritt, muss der Server wie folgt einen Fehler an den Client zurückmelden:</span><span class="sxs-lookup"><span data-stu-id="64c16-4344">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="64c16-4345">Verarbeitung der vom Client gesendeten Nachricht Abbrechen</span><span class="sxs-lookup"><span data-stu-id="64c16-4345">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="64c16-4346">Antworten Sie mit dem Nachrichten Header (nur) der vom Client gesendeten Nachricht, wobei das Nachrichten \_ Feld intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4346">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="64c16-4347">Legen \_ Sie das Feld Status auf den Fehler Codewert fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-4347">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="64c16-4348">Wenn eine Nachricht eingeht, muss der Server den Wert des msg-Felds überprüfen, \_ um festzustellen, ob es sich um einen bekannten Typ handelt (siehe Abschnitt 2.2.2).</span><span class="sxs-lookup"><span data-stu-id="64c16-4348">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="64c16-4349">Wenn der Typ nicht bekannt ist, muss er einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4349">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="64c16-4350">Der Server muss dann den \_ Wert des ulchecksum-Felds überprüfen, wenn der Nachrichtentyp einer der folgenden ist:</span><span class="sxs-lookup"><span data-stu-id="64c16-4350">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="64c16-4351">Cpmconnectin (0x000000c8)</span><span class="sxs-lookup"><span data-stu-id="64c16-4351">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="64c16-4352">Cpmkreatequeryin (0x000000CA)</span><span class="sxs-lookup"><span data-stu-id="64c16-4352">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="64c16-4353">Cpmsetbindingsin (0x000000d0)</span><span class="sxs-lookup"><span data-stu-id="64c16-4353">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="64c16-4354">Cpmgetrowsin (0x000000cc)</span><span class="sxs-lookup"><span data-stu-id="64c16-4354">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="64c16-4355">Cpmfetchvaluein (0x000000e4)</span><span class="sxs-lookup"><span data-stu-id="64c16-4355">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="64c16-4356">Um den \_ Wert des Felds ulchecksum zu validieren, muss der Server den Wert, den der Client im \_ Feld iclientversion in der cpmconnectin-Nachricht angegeben hat, überprüfen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4356">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="64c16-4357">Wenn das \_ Feld iclientversion nicht auf 0x00000008 festgelegt ist und das \_ Feld ulchecksum nicht auf 0x00000000 festgelegt ist, muss der Server einen \_ Fehler aufgrund eines ungültigen \_ Parameters (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4357">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="64c16-4358">Der Server muss das \_ Feld ulchecksum für Clients nicht validieren, indem das \_ Feld iclientversion auf einen Wert kleiner als 0x00000008 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-4358">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="64c16-4359">Wenn der \_ Wert des Felds iclientversionfield 0x00000008 oder größer ist, muss der Server überprüfen, ob das \_ Feld ulchecksum gemäß den Angaben in Abschnitt 3.2.4 berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="64c16-4359">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="64c16-4360">Wenn der \_ ulchecksum-Wert ungültig ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4360">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="64c16-4361">Als nächstes überprüft der Server den Status in.</span><span class="sxs-lookup"><span data-stu-id="64c16-4361">Next, the server checks which state is it in.</span></span> <span data-ttu-id="64c16-4362">Wenn der Status "nicht initialisiert" lautet, muss der Server einen \_ nicht initialisierten CI-E- \_ \_ Fehler (0x8004180b) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4362">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="64c16-4363">Wenn der Status "heruntergefahren" lautet, muss der Server den Fehler "CI \_ E \_ Shutdown (0x80041812)" melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4363">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="64c16-4364">Nachdem ein Header als gültig festgelegt wurde und der Server den Status "wird ausgeführt" aufweist, muss eine weitere Nachrichten spezifische Verarbeitung durchgeführt werden, wie in den folgenden Unterabschnitten angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4364">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="64c16-4365">3.1.5.1-Dienst Katalog Verwaltung für Remote Indizierung</span><span class="sxs-lookup"><span data-stu-id="64c16-4365">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="64c16-4366">3.1.5.1.1 empfangen einer cpmcianout-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4366">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="64c16-4367">Wenn der Server eine cpmcistateinout-Nachrichten Anforderung vom Client empfängt, muss der Server zunächst prüfen, ob der Client in einer Liste verbundener Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4367">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="64c16-4368">Wenn der Client nicht in der Liste enthalten ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4368">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="64c16-4369">Andernfalls muss er auf den Client mit einer cpmcistateinout-Nachricht antworten und ihn mit Informationen zum zugeordneten Katalog des Clients auffüllen, wie in Abschnitt 2.2.3.1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4369">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="64c16-4370">3.1.5.1.2 empfängt eine cpmseterstatuein-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4370">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="64c16-4371">Wenn der Server eine cpmsetcatstatein-Nachrichten Anforderung vom Client empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4371">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4372">Überprüfen Sie, ob der Client über Administrator Zugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4372">Check that client has administrative access.</span></span> <span data-ttu-id="64c16-4373">Wenn der Client keinen Administrator Zugriff hat, muss der Server einen Fehler vom Typ "Status \_ Zugriff \_ verweigert" (0xc0000022) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4373">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="64c16-4374">Wenn \_ dwnewstate nicht gleich cicat \_ all geöffnet ist, \_ Ändern Sie den Status des im Feld "Name" angegebenen Katalogs, wie im Feld " \_ dwnewstate" angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4374">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="64c16-4375">Weitere Informationen finden Sie im Abschnitt 2.2.3.2.</span><span class="sxs-lookup"><span data-stu-id="64c16-4375">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="64c16-4376">Wenn der Server keinen Katalog mit dem im Feld "catname" angegebenen Namen findet, muss der Server den \_ Fehler "Ungültiger \_ Parameter (0xc000000D)" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4376">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4377">Antworten Sie auf den Client mit einer cpmsetsinstateout-Meldung, bei der \_ dwoldstate auf den vorherigen Status des Katalogs festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="64c16-4377">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="64c16-4378">Wenn \_ dwnewstate gleich cicat \_ all geöffnet ist \_ , muss der Server den Status aller Kataloge überprüfen. wenn alle Elemente gestartet werden \_ , muss dwoldstate auf 0x00000001 festgelegt werden. andernfalls wird \_ dwoldstate auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4378">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="64c16-4379">3.1.5.1.3 empfängt eine cpmupdatedocumentsin-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4379">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="64c16-4380">Wenn der Server eine cpmupdatedocumentsin-Nachrichten Anforderung empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4380">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4381">Überprüfen Sie, ob der Client in einer Liste verbundener Clients (denen ein Katalog zugeordnet ist) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4381">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="64c16-4382">Wenn der Client nicht in der Liste enthalten ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4382">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4383">Überprüfen Sie, ob der Client über Administrator Zugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4383">Check that client has administrative access.</span></span> <span data-ttu-id="64c16-4384">Wenn der Client keinen Administrator Zugriff auf den Server hat, muss der Server den \_ Fehler Status Zugriff \_ verweigert (0xc0000022) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4384">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="64c16-4385">Beginnen Sie mit dem Indizieren des vom Client angegebenen Pfads und Durchführung eines vollständigen oder inkrementellen Scans, abhängig vom Wert des \_ flagfelds in der cpmupdatedocumentsin-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-4385">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="64c16-4386">Wenn der Pfad nicht zuvor indiziert wurde, muss er der Auflistung indizierter Speicherorte hinzugefügt werden, und es muss eine vollständige Überprüfung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4386">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="64c16-4387">Wenn ein unzulässiger Wert des \_ Flags-Felds angegeben ist, muss der Server so agieren, als ob \_ Flag auf upd init festgelegt \_ und eine vollständige Überprüfung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="64c16-4387">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="64c16-4388">Dieser Vorgang muss in dem Katalog ausgeführt werden, der dem Client zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4388">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="64c16-4389">Antworten Sie auf den Client mit dem Nachrichten Header für cpmupdatedocumentsin, und legen \_ Sie das Feld Status auf die Ergebnisse der Anforderung fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-4389">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="64c16-4390">3.1.5.1.4 Empfangen einer cpmforcemergein-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4390">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="64c16-4391">Wenn der Server eine cpmforcemergein-Nachrichten Anforderung empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4391">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4392">Überprüfen Sie, ob der Client in einer Liste verbundener Clients (denen ein Katalog zugeordnet ist) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4392">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="64c16-4393">Wenn sich der Client nicht in der Liste befindet, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4393">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4394">Überprüfen Sie, ob der Client über Administrator Zugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4394">Check that client has administrative access.</span></span> <span data-ttu-id="64c16-4395">Wenn der Client keinen Administrator Zugriff hat, muss der Server einen Fehler vom Typ "Status \_ Zugriff \_ verweigert" (0xc0000022) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4395">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="64c16-4396">Beginnen Sie jeden Wartungsprozess, der zum Verbessern der Abfrageleistung in einem Katalog erforderlich ist, der dem Client zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4396">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="64c16-4397">Antworten Sie auf den Client mit einem Nachrichten Header für cpmforcemergein, und legen \_ Sie das Feld Status auf die Ergebnisse der Anforderung fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-4397">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="64c16-4398">Beachten Sie, dass der Wartungsprozess asynchron ist und fortgesetzt werden kann, nachdem der Client die Antwortnachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="64c16-4398">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="64c16-4399">Dieser Prozess wirkt sich nicht direkt auf das Protokoll aus (außer der Antwortzeit).</span><span class="sxs-lookup"><span data-stu-id="64c16-4399">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="64c16-4400">3.1.5.2 Remote Index Dienst Abfragen</span><span class="sxs-lookup"><span data-stu-id="64c16-4400">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="64c16-4401">3.1.5.2.1 empfängt eine cpmconnectin-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4401">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="64c16-4402">Wenn der Server eine cpmconnectin-Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4402">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4403">Überprüfen Sie, ob der Client in der Liste der verbundenen Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4403">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="64c16-4404">Wenn dies der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4404">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4405">Überprüft, ob der angegebene Katalog vorhanden und nicht im beendeten Zustand ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4405">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="64c16-4406">Wenn dies nicht der Fall ist, muss der Server einen Bericht "CI \_ E \_ No \_ catalog (0x8004181d)" haben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4406">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="64c16-4407">Fügen Sie den Client der Liste der verbundenen Clients hinzu.</span><span class="sxs-lookup"><span data-stu-id="64c16-4407">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="64c16-4408">Ordnen Sie den Katalog dem Client zu.</span><span class="sxs-lookup"><span data-stu-id="64c16-4408">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="64c16-4409">Speichern Sie die Informationen, die in der cpmconnectin-Nachricht (z. b. Katalog Name, Client Version usw.) übermittelt wurden, im Client Zustand.</span><span class="sxs-lookup"><span data-stu-id="64c16-4409">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="64c16-4410">Reagieren Sie auf den Client mit einer cpmconnectout-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-4410">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="64c16-4411">3.1.5.2.2 empfängt eine cpmkreatequeryin-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="64c16-4411">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="64c16-4412">Wenn der Server eine cpmkreatequeryin-Nachrichten Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4412">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4413">Überprüfen Sie, ob der Client in der Liste der verbundenen Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4413">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="64c16-4414">Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4414">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4415">Überprüfen Sie, ob dem Client bereits eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4415">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="64c16-4416">Wenn dies der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4416">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4417">Überprüfen Sie, ob der dem Client zugeordnete Katalog den Status aufweist, der die Verarbeitung von Abfragen ermöglicht (cicat \_ schreibgeschützt oder cicat \_ beschreib bar).</span><span class="sxs-lookup"><span data-stu-id="64c16-4417">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="64c16-4418">Wenn dies nicht der Fall ist, muss der Server einen Fehler der Abfrage " \_ \_ keine \_ Abfrage (0x8004160c)" melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4418">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="64c16-4419">Analysieren Sie den Einschränkungs Satz, die Sortier Reihenfolgen und die in der Abfrage angegebenen Gruppierungen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4419">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="64c16-4420">Wenn auf dem Server ein Fehler auftritt, muss ein entsprechender Fehler gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4420">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="64c16-4421">Wenn dieser Schritt aus einem anderen Grund fehlschlägt, muss der Server den gefundenen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4421">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="64c16-4422">Weitere Informationen zum Indizieren von Dienst Abfrage Fehlern finden Sie unter \[ MSDN-queryerr \] .</span><span class="sxs-lookup"><span data-stu-id="64c16-4422">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="64c16-4423">Speichern Sie die Suchabfrage im Status für den Client.</span><span class="sxs-lookup"><span data-stu-id="64c16-4423">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="64c16-4424">Nehmen Sie alle Vorbereitungen vor, die zum Verarbeiten von Zeilen an einen Client erforderlich sind, und ordnen Sie die Abfrage den entsprechenden Cursor Handles zu (abhängig von Informationen, die in der Meldung "cpmkreatequeryin"</span><span class="sxs-lookup"><span data-stu-id="64c16-4424">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="64c16-4425">Fügen Sie diese Handles der Liste der Cursor Handles des Clients hinzu, und initialisieren Sie Listen von Kapitel Handles und Lesezeichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4425">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="64c16-4426">Initialisieren der Liste der Kapitel Handles für jeden Cursor in dieser Abfrage an DB \_ NULL \_ hChapter</span><span class="sxs-lookup"><span data-stu-id="64c16-4426">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="64c16-4427">Initialisieren Sie die Liste der Lesezeichen Handles für jeden Cursor in dieser Abfrage an einen Satz von dbbmk \_ First und dbbmk \_ Last.</span><span class="sxs-lookup"><span data-stu-id="64c16-4427">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="64c16-4428">Markieren Sie die Abfrage als nicht überwacht für Änderungen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4428">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="64c16-4429">Initialisieren Sie die Anzahl der Zeilen für die aktuell berechnete Anzahl von Zeilen (die 0 sein kann, wenn die Abfrage nicht ausgeführt werden konnte, oder eine Zahl, wenn die Abfrage gerade ausgeführt wird), und initialisieren Sie den Zähler und den Nenner des abfrageabschlusses.</span><span class="sxs-lookup"><span data-stu-id="64c16-4429">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="64c16-4430">Reagieren Sie auf den Client mit einer cpmkreatequeryout-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-4430">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="64c16-4431">3.1.5.2.3 empfängt eine cpmgetquerystatus in-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="64c16-4431">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="64c16-4432">Wenn der Server eine cpmgetquerystatusin-Nachrichten Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4432">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4433">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4433">Check if the client has query associated with it.</span></span> <span data-ttu-id="64c16-4434">Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4434">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4435">Überprüfen Sie, ob das Cursor Handle in einer Liste der Cursor Handles des Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4435">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="64c16-4436">Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4436">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="64c16-4437">Bereiten Sie eine cpmgetquerystatusout-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="64c16-4437">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="64c16-4438">Der Server muss den aktuellen Abfrage Status abrufen und im \_ Feld "qStatus" festlegen (Weitere Informationen finden Sie unter 2.2.3.11).</span><span class="sxs-lookup"><span data-stu-id="64c16-4438">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="64c16-4439">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4439">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="64c16-4440">Reagieren Sie auf den Client mit der cpmgetquerystatusout-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-4440">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="64c16-4441">3.1.5.2.4 empfängt eine cpmgetquerystatusexin-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="64c16-4441">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="64c16-4442">Wenn der Server eine cpmgetquerystatusexin-Nachrichten Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4442">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4443">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4443">Check if the client has a query associated with it.</span></span> <span data-ttu-id="64c16-4444">Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4444">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4445">Überprüfen Sie, ob das übergebenen Cursor Handle in einer Liste der Cursor Handles des Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4445">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="64c16-4446">Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4446">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="64c16-4447">Bereiten Sie eine cpmgetquerystatusexout-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="64c16-4447">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="64c16-4448">Der Server muss den aktuellen Abfrage Status und den Abfrage Fortschritt abrufen und qStatus festlegen (siehe 2.2.3.11 auf mögliche Werte), \_ dwratiofinishednenner und \_ dwratiofinishedzähler.</span><span class="sxs-lookup"><span data-stu-id="64c16-4448">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="64c16-4449">Anschließend muss die Anzahl der Zeilen in den Abfrage Ergebnissen auf \_ crowstotal festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4449">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="64c16-4450">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4450">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="64c16-4451">Rufen Sie Informationen zum Katalog des Clients ab, und füllen Sie \_ cfiltereddocuments und \_ cdocumentstofilter aus.</span><span class="sxs-lookup"><span data-stu-id="64c16-4451">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="64c16-4452">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4452">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="64c16-4453">Rufen Sie die Position des Lesezeichens ab, das durch das Handle im \_ BMK-Feld angegeben wird, und füllen Sie das verbleibende \_ irowbmk-Feld in der cpmgetquerystatusexout-Nachricht aus.</span><span class="sxs-lookup"><span data-stu-id="64c16-4453">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="64c16-4454">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4454">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="64c16-4455">Reagieren Sie auf den Client mit der cpmgetquerystatusexout-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-4455">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="64c16-4456">3.1.5.2.5 empfängt eine cpmratiofinishedin-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4456">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="64c16-4457">Wenn der Server eine cpmratiofinishedin-Nachrichten Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4457">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4458">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4458">Check if the client has query associated with it.</span></span> <span data-ttu-id="64c16-4459">Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4459">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4460">Überprüfen Sie, ob das übergebenen Cursor Handle in der Liste der Cursor Handles des Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4460">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="64c16-4461">Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4461">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="64c16-4462">Bereiten Sie eine cpmratiofinishedout-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="64c16-4462">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="64c16-4463">Der Server muss den Abfrage Status des Clients abrufen und \_ ulzähator \_ -, ulnenner-und \_ Crows-Felder ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4463">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="64c16-4464">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4464">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="64c16-4465">Wenn \_ Crows gleich der zuletzt gemeldeten Anzahl von Zeilen für diese Abfrage ist, legen \_ Sie fnewrows auf 0x00000000 fest, und legen Sie andernfalls 0x00000001 fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-4465">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="64c16-4466">Aktualisieren Sie die zuletzt gemeldete Anzahl von Zeilen für diese Abfrage auf den Wert von \_ Crows.</span><span class="sxs-lookup"><span data-stu-id="64c16-4466">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="64c16-4467">Antworten Sie den Client mit der cpmratiofinishedout-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-4467">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="64c16-4468">3.1.5.2.6 empfängt eine cpmsetbindingsin-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="64c16-4468">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="64c16-4469">Wenn der Server eine cpmsetbindingsin-Nachrichten Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4469">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4470">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4470">Check if the client has a query associated with it.</span></span> <span data-ttu-id="64c16-4471">Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4471">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4472">Überprüfen Sie, ob das übergebenen Cursor Handle in der Liste der Cursor Handles des Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4472">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="64c16-4473">Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4473">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="64c16-4474">Stellen Sie sicher, dass die Bindungs Informationen gültig sind (d. h. Spalte zumindest den Wert, die Länge oder den Status, der zurückgegeben werden soll, keine Überlappung in Bindungen für Wert, Länge oder Status; und Wert, Länge und Status in der angegebenen Zeilengröße) und, wenn kein DB \_ e \_ badbindinfo (0x80040e08)-Fehler gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-4474">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="64c16-4475">Speichern Sie die Bindungs Informationen, die den im Feld acolumschlag angegebenen Spalten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-4475">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="64c16-4476">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4476">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="64c16-4477">Antworten Sie auf den Client mit einem Nachrichten Header (nur) \_ , wenn msg auf cpmsetbindingsin festgelegt ist und \_ der Status auf die Ergebnisse der angegebenen Bindung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4477">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="64c16-4478">3.1.5.2.7 empfängt eine cpmgetrowsin-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4478">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="64c16-4479">Wenn der Server eine cpmgetrowsin-Nachrichten Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4479">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4480">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4480">Check if the client has query associated with it.</span></span> <span data-ttu-id="64c16-4481">Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4481">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4482">Überprüfen Sie, ob das übergebenen Cursor Handle in der athelist der Cursor Zieh Punkte des Clients ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4482">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="64c16-4483">Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4483">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="64c16-4484">Überprüfen Sie, ob der Client über einen aktuellen Satz von Bindungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4484">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="64c16-4485">Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4485">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="64c16-4486">Bereiten Sie eine cpmgetrowsout-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="64c16-4486">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="64c16-4487">Der Server muss den Cursor in den Abfrage Ergebnissen positionieren, wie in der Such Beschreibung angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4487">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="64c16-4488">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4488">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="64c16-4489">Rufen Sie beliebig viele Zeilen ab, die in einen Puffer passen, die Größe wird durch den \_ cbread-Puffer angegeben, jedoch nicht mehr als durch \_ crowstotransfer angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4489">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="64c16-4490">Beim Abrufen von Zeilen muss der Server den Eigenschafts Werttyp jeder ausgewählten Spalte mit dem im aktuellen Bindungs Satz des Clients (Abschnitt 3.1.1) angegebenen Typ vergleichen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4490">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="64c16-4491">Wenn der Typ in der Bindung nicht die VT \_ -Variante ist, muss der Server versuchen, den-Eigenschafts Wert der Spalte in diesen Typ zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="64c16-4491">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="64c16-4492">Andernfalls \_ muss der Eigenschafts Wert im normalen Typ zurückgegeben werden, wenn das DBPROP useextendeddbtypes-Flag im DBPROPSET queryext-Eigenschaften Satz des Clients festgelegt ist \_ oder wenn der Eigenschafts Wert der Spalte kein VT- \_ Vektortyp ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4492">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="64c16-4493">Wenn keines dieser Fälle zutrifft (d. h., der Server verfügt über einen VT \_ -Vektortyp, und der Client unterstützt keinen VT \_ -Vektor), muss der Server versuchen, ihn wie folgt in einen VT \_ -Arraytyp zu konvertieren: VT \_ I8, VT \_ UI8, VT \_ FILETIME und VT \_ CLSID Array-Elemente können nicht konvertiert werden, sondern fehlschlagen. VT \_ LPSTR-und VT \_ LPWSTR-Array Elemente müssen in VT \_ BSTR konvertiert werden; Array Elemente aller anderen Typen müssen unverändert bleiben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4493">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="64c16-4494">Wenn Zeilen Spalten außerdem Kapitel Handles oder Lesezeichen Handles enthalten, muss der Server die entsprechenden Listen aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="64c16-4494">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="64c16-4495">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server melden, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4495">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="64c16-4496">Speichern Sie die tatsächliche Anzahl von Zeilen, die in \_ crowszurück gegeben werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4496">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="64c16-4497">Kopieren Sie die Such Beschreibung und das Kapitel Feld aus cpmgetrowsin in eine zu sendende cpmgetrowsout-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-4497">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="64c16-4498">Speichert abgerufene Zeilen im Zeilen Feld (siehe Hinweis zum Status Byte unten und Abschnitt 2.2.3.16 für die Struktur des Rows-Felds).</span><span class="sxs-lookup"><span data-stu-id="64c16-4498">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="64c16-4499">Reagieren Sie auf den Client mit der cpmgetrowsout-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-4499">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="64c16-4500">Hinweis für das Feld "Status Byte":</span><span class="sxs-lookup"><span data-stu-id="64c16-4500">Note on status byte field:</span></span>

<span data-ttu-id="64c16-4501">Wenn statusused in der ctablecolumn der cpmsetbindingin-Nachricht für die Spalte auf 0x01 festgelegt ist, muss der Server das Status Byte (das sich am statusoffset vom Anfang der Zeile befindet) auf einen der folgenden Werte festlegen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4501">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="64c16-4502">Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-4502">Value</span></span> | <span data-ttu-id="64c16-4503">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64c16-4503">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="64c16-4504">0x00</span><span class="sxs-lookup"><span data-stu-id="64c16-4504">0x00</span></span>  | <span data-ttu-id="64c16-4505">Status</span><span class="sxs-lookup"><span data-stu-id="64c16-4505">StatusOK</span></span>       |
| <span data-ttu-id="64c16-4506">0x01</span><span class="sxs-lookup"><span data-stu-id="64c16-4506">0x01</span></span>  | <span data-ttu-id="64c16-4507">Status verzögert</span><span class="sxs-lookup"><span data-stu-id="64c16-4507">StatusDeferred</span></span> |
| <span data-ttu-id="64c16-4508">0x02</span><span class="sxs-lookup"><span data-stu-id="64c16-4508">0x02</span></span>  | <span data-ttu-id="64c16-4509">Status NULL</span><span class="sxs-lookup"><span data-stu-id="64c16-4509">StatusNull</span></span>     |



 

<span data-ttu-id="64c16-4510">Wenn der Eigenschafts Wert für diese Zeile nicht vorhanden ist, muss der Server das Status Byte auf statusnull festlegen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4510">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="64c16-4511">Wenn der Wert zu groß ist, um in der cpmgetrowsout-Nachricht übertragen zu werden, muss der Server das Status Byte auf statusaufgeschoben festlegen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4511">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="64c16-4512">Andernfalls muss der Server das Status Byte auf statusok festlegen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4512">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="64c16-4513">3.1.5.2.8 empfängt eine cpmfetchvaluein-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4513">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="64c16-4514">Wenn der Server eine cpmfetchvaluein-Nachrichten Anforderung von einem Client empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4514">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4515">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4515">Check if the client has query associated with it.</span></span> <span data-ttu-id="64c16-4516">Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4516">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4517">Bereiten Sie eine cpmfetchvalueout-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="64c16-4517">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="64c16-4518">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="64c16-4519">Suchen Sie nach dem Dokument, das durch das \_ wid-Feld angegeben wird, und überprüfen Sie, ob die Eigenschaften-ID für dieses Dokument (später als "Eigenschafts Wert" bezeichnet) für diesen Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4519">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="64c16-4520">Wenn dieser Wert nicht verfügbar ist, muss der Server \_ fvalueist auf 0x00000000 festlegen und andernfalls \_ fvalueist auf 0x00000001 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4520">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="64c16-4521">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4521">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="64c16-4522">Wenn \_ fvalueist gleich 0x00000001 ist, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4522">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="64c16-4523">Serialisieren Sie den Eigenschafts Wert in eine serializedpropertyvalue-Struktur, und kopieren Sie, beginnend \_ mit dem cbsofar-Offset, höchstens \_ cbblock-bytes (aber nicht über das Ende der serialisierten Eigenschaft) in das vValue-Feld.</span><span class="sxs-lookup"><span data-stu-id="64c16-4523">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="64c16-4524">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4524">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="64c16-4525">Legen \_ Sie cbValue auf die Anzahl der im vorherigen Schritt kopierten Bytes fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-4525">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="64c16-4526">Legen Sie VType auf den Eigenschaftentyp des Eigenschafts Werts fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-4526">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="64c16-4527">Wenn die Länge der serialisierten Eigenschaft größer als \_ cbsofar zu \_ cbValue addiert ist, wird Set \_ fmoreauf 0x00000001 festgelegt. andernfalls wird es auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4527">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="64c16-4528">Antworten auf den Client mit der cpmfetchvalueout-Meldung</span><span class="sxs-lookup"><span data-stu-id="64c16-4528">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="64c16-4529">3.1.5.2.9 empfängt eine cpmgetnotify-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4529">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="64c16-4530">Wenn der Server eine cpmgetnotify-Nachricht von einem Client empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4530">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4531">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4531">Check if the client has query associated with it.</span></span> <span data-ttu-id="64c16-4532">Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4532">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4533">Wenn seit der letzten cpmsendnotifyout-Nachricht für diesen Client keine Änderungen im Abfrageresultset vorhanden sind, oder wenn die Abfrage zurzeit nicht auf Änderungen im Resultset überwacht wird, muss der Server mit der cpmgetnotify-Nachricht antworten und die Abfrage auf Änderungen im Resultset überwachen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4533">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="64c16-4534">Wenn das Abfrageresultset zu einem späteren Zeitpunkt geändert wird, muss der Server genau eine cpmsendnotifyout-Nachricht an den Client senden und muss die Änderung im \_ watchnotify-Feld angeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4534">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="64c16-4535">Wenn seit der letzten cpmsendnotifyout-Nachricht Änderungen am Abfrageresultset vorgenommen wurden, muss der Server mit cpmsendnotifyout Antworten und die Änderung im \_ watchnotify-Feld angeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4535">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="64c16-4536">Beachten Sie, dass bei vielen Änderungen an den Abfrage Ergebnissen dbwatchnotify \_ rowschangidie Priorität hat (d. h., wenn die Abfrage erneut ausgeführt wurde, die Anzahl der Zeilen geändert wurde und die Abfrage erneut ausgeführt wurde, würde das gemeldete Ereignis dbwatchnotify \_ rowschangilauten).</span><span class="sxs-lookup"><span data-stu-id="64c16-4536">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="64c16-4537">3.1.5.2.10 empfängt eine cpmgetapproximatepositionin-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="64c16-4537">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="64c16-4538">Wenn der Server eine cpmgetapproximatepositionin-Nachrichten Anforderung vom Client empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4538">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4539">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4539">Check if the client has a query associated with it.</span></span> <span data-ttu-id="64c16-4540">Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4540">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4541">Überprüfen Sie, ob der übergebenen Cursor Handle, Kapitel Handle und Lesezeichen Handle in den entsprechenden Listen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-4541">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="64c16-4542">Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4542">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="64c16-4543">Suchen Sie eine Zeile, die mit dem Lesezeichen Handle in den Abfrage Ergebnissen verknüpft ist, und nähern Sie die Position der Zeile im Rowset, auf die durch das Kapitel handle verwiesen wird, und bestimmen Sie den Zähler und Nenner für die Position.</span><span class="sxs-lookup"><span data-stu-id="64c16-4543">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="64c16-4544">Beachten Sie, dass das \_ \_ entsprechende Kapitel das hauptrowset der Abfrage ist, wenn es sich bei dem Kapitel handle um DB null hChapter handelt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4544">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="64c16-4545">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4545">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="64c16-4546">Reagieren Sie auf den Client mit einer cpmfetchvalueout-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-4546">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="64c16-4547">3.1.5.2.11 empfängt eine cpmcomparebmkin-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4547">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="64c16-4548">Wenn der Server eine cpmcomparebmkin-Nachrichten Anforderung vom Client empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4548">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4549">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4549">Check if the client has a query associated with it.</span></span> <span data-ttu-id="64c16-4550">Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4550">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4551">Überprüfen Sie, ob der übergebenen Cursor Handle, Kapitel Handle und Lesezeichen Handles in den entsprechenden Listen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-4551">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="64c16-4552">Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4552">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="64c16-4553">Bereiten Sie eine cpmcomparebmkout-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="64c16-4553">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="64c16-4554">Wenn Lesezeichen Handles gleich sind, \_ muss dwcomparison auf DbCompare EQ festgelegt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-4554">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="64c16-4555">Wenn eines der Lesezeichen Handles zuerst dbbmk \_ First oder dbbmk \_ Last ist, \_ muss dwcomparison auf DbCompare ne festgelegt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-4555">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="64c16-4556">Andernfalls muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4556">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="64c16-4557">Suchen von Zeilen, auf die von jedem Lesezeichen Handle in den Abfrage Ergebnissen verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="64c16-4557">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="64c16-4558">Wenn eine der Zeilen nicht in dem Kapitel liegt, das durch das Kapitel Handle in cpmcomparebmkin angegeben wird, \_ muss dwcomparison auf DbCompare notcompare festgelegt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-4558">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="64c16-4559">Wenn sich beide Zeilen im gleichen Kapitel befinden, muss der Server eine Position der Zeilen im Rowset anweisen, auf die durch den Handle dieses Kapitels verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-4559">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="64c16-4560">Anschließend müssen Sie Positionswerte vergleichen und \_ dwcomparison auf DbCompare lt festlegen, \_ Wenn die Position der ersten Zeile kleiner ist als die Position der zweiten Zeile \_ . andernfalls muss dwcomparison auf DbCompare gt festgelegt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-4560">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="64c16-4561">Reagieren Sie auf den Client mit der gefüllten cpmcomparebmkout-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-4561">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="64c16-4562">3.1.5.2.12 empfängt eine cpmrestartpositionin-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="64c16-4562">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="64c16-4563">Wenn der Server die cpmrestartpositionin-Nachrichten Anforderung vom Client empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4563">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4564">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4564">Check if the client has a query associated with it.</span></span> <span data-ttu-id="64c16-4565">Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4565">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4566">Überprüfen Sie, ob der übergebenen Cursor Handle und das Kapitel Handle in den entsprechenden Listen vorliegen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4566">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="64c16-4567">Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4567">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="64c16-4568">Bewegen Sie den Cursor an den Anfang des Kapitels, der durch das Kapitel Handle identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-4568">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="64c16-4569">Beachten Sie, dass das \_ \_ entsprechende Kapitel das hauptrowset der Abfrage ist, wenn es sich bei dem Kapitel handle um DB null hChapter handelt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4569">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="64c16-4570">Wenn dieser Schritt aus irgendeinem Grund fehlschlägt, muss der Server einen Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4570">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="64c16-4571">Reagieren Sie auf den Client mit einer cpmrestartpositionin-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-4571">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="64c16-4572">3.1.5.2.13 empfängt eine cpmfreecursorin-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="64c16-4572">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="64c16-4573">Wenn der Server eine cpmfreecursorin-Nachrichten Anforderung vom Client empfängt, muss der Server folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4573">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4574">Überprüfen Sie, ob dem Client eine Abfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4574">Check if the client has a query associated with it.</span></span> <span data-ttu-id="64c16-4575">Wenn dies nicht der Fall ist, muss der Server einen \_ ungültigen \_ Parameter Fehler (0xc000000D) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4575">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="64c16-4576">Überprüfen Sie, ob das übergebenen Cursor Handle in der Liste der Cursor Handles des Clients enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4576">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="64c16-4577">Wenn dies nicht der Fall ist, muss der Server einen E \_ Fail-Fehler (0x80004005) melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4577">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="64c16-4578">Geben Sie den Cursor und die zugehörigen Ressourcen (siehe Abschnitt 3.1.1 für die komplette Liste) für dieses Cursor Handle frei.</span><span class="sxs-lookup"><span data-stu-id="64c16-4578">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="64c16-4579">Entfernen Sie den Cursor aus der Liste der Cursor für diesen Client.</span><span class="sxs-lookup"><span data-stu-id="64c16-4579">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="64c16-4580">Antworten Sie mit einer cpmfreecursorout-Meldung, und legen Sie das \_ Feld ccursorsrestwert auf die Anzahl der verbleibenden Cursors fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-4580">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="64c16-4581">in der Liste dieses Clients.</span><span class="sxs-lookup"><span data-stu-id="64c16-4581">in this client's list.</span></span>
-   <span data-ttu-id="64c16-4582">Wenn für diesen Client keine weiteren Cursor vorhanden sind, muss der Server die Abfrage und die zugehörigen Ressourcen freigeben (siehe Abschnitt 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="64c16-4582">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="64c16-4583">3.1.5.2.14 empfängt eine cpmdisconnect-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4583">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="64c16-4584">Wenn der Server eine cpmdisconnect-Nachrichten Anforderung vom Client empfängt, muss der Server den Client aus der Liste der verbundenen Clients entfernen und alle dem Client zugeordneten Ressourcen freigeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4584">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="64c16-4585">3.1.6-Timer-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="64c16-4585">3.1.6 Timer Events</span></span>

<span data-ttu-id="64c16-4586">Keine.</span><span class="sxs-lookup"><span data-stu-id="64c16-4586">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="64c16-4587">3.1.7 andere lokale Ereignisse</span><span class="sxs-lookup"><span data-stu-id="64c16-4587">3.1.7 Other Local Events</span></span>

<span data-ttu-id="64c16-4588">Wenn der Server angehalten wird, muss er zunächst in den Zustand "Herunterfahren" übergehen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4588">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="64c16-4589">Er muss dann das lauschen an der Pipe beenden, alle anderen Implementierungs spezifischen Aufgaben für das Herunterfahren ausführen und dann in den Zustand "beendet" übergehen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4589">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="64c16-4590">3,2 Client Details</span><span class="sxs-lookup"><span data-stu-id="64c16-4590">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="64c16-4591">3.2.1 abstraktes Datenmodell</span><span class="sxs-lookup"><span data-stu-id="64c16-4591">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="64c16-4592">Im folgenden Abschnitt werden die Daten und der Status des Inhalts Index Dienst-Protokoll Clients angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4592">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="64c16-4593">Die bereitgestellten Daten dienen dazu, die Erläuterung der Verhalten des Protokolls zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4593">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="64c16-4594">In diesem Abschnitt wird nicht vorgeschrieben, dass Implementierungen dieses Modells einhalten, solange das externe Verhalten mit dem in diesem Dokument beschriebenen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4594">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="64c16-4595">Ein Client weist den folgenden abstrakten Zustand auf:</span><span class="sxs-lookup"><span data-stu-id="64c16-4595">A client has the following abstract state:</span></span>

-   <span data-ttu-id="64c16-4596">**Letzte gesendete Nachricht**: eine Kopie der letzten Nachricht, die an den Server gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="64c16-4596">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="64c16-4597">**Aktueller Eigenschafts Wert**: ein partieller Wert einer "verzögerten" Eigenschaft, die gerade abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-4597">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="64c16-4598">**Aktuell empfangene Bytes**: die Anzahl von Bytes, die bisher für den aktuellen Eigenschafts Wert empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4598">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="64c16-4599">**Status der Named Pipe-Verbindung**: eine Verbindung mit dem Server</span><span class="sxs-lookup"><span data-stu-id="64c16-4599">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="64c16-4600">3.2.2 Timer</span><span class="sxs-lookup"><span data-stu-id="64c16-4600">3.2.2 Timers</span></span>

<span data-ttu-id="64c16-4601">Es sind keine protokolltimer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="64c16-4601">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="64c16-4602">3.2.3-Initialisierung</span><span class="sxs-lookup"><span data-stu-id="64c16-4602">3.2.3 Initialization</span></span>

<span data-ttu-id="64c16-4603">Es werden keine Aktionen ausgeführt, bis eine höhere ebenenanforderung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-4603">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="64c16-4604">3.2.4 Higher-Layer ausgelöste Ereignisse</span><span class="sxs-lookup"><span data-stu-id="64c16-4604">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="64c16-4605">Wenn eine Anforderung von einer höheren Ebene empfangen wird, muss der Client eine Named Pipe Verbindung mit dem Server herstellen, wobei die in Abschnitt 2,1 angegebenen Details verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4605">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="64c16-4606">Wenn dies nicht möglich ist, muss die Anforderung höherer Ebene fehlgeschlagen sein.</span><span class="sxs-lookup"><span data-stu-id="64c16-4606">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="64c16-4607">Das heißt, wenn eine Verbindung nicht hergestellt werden kann, liegt es in der Verantwortung der höheren Ebene, wenn dies gewünscht wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-4607">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="64c16-4608">Einem Header muss ein in Abschnitt 2.2.2 angegebener Feldsatz vorausgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4608">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="64c16-4609">Bei Nachrichten, die als Prüfsumme ungleich NULL angegeben werden, \_ muss der ulchecksum-Wert wie folgt berechnet werden:</span><span class="sxs-lookup"><span data-stu-id="64c16-4609">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="64c16-4610">Der Inhalt der Nachricht nach dem \_ ulReserved2-Feld im Nachrichten Header muss als Sequenz von 32-Bit-Ganzzahlen interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4610">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="64c16-4611">Der Client muss die Summe der numerischen Werte berechnen, die durch die ganzen Zahlen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4611">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="64c16-4612">Berechnen Sie das bitweise XOR dieses Werts mit 0x59533959.</span><span class="sxs-lookup"><span data-stu-id="64c16-4612">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="64c16-4613">Subtrahieren Sie den von der Meldung angegebenen Wert \_ aus dem Wert, der sich aus dem bitweisen XOR ergibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4613">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="64c16-4614">3.2.4.1-Dienst Katalog Verwaltung für Remote Indizierung</span><span class="sxs-lookup"><span data-stu-id="64c16-4614">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="64c16-4615">Jede Nachricht wird von einer Anforderung von der höheren Ebene ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="64c16-4615">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="64c16-4616">Es wird keine Nachrichten Sequenz vom Client für CISP-Nachrichten Anforderungen für die Remote Verwaltung von Katalogen erzwungen, aber (mit Ausnahme einer cpmsetcatstatein-Meldung) antwortet der Server nur mit Erfolg, wenn der Client zuvor über eine cpmconnectin-Nachricht eine Verbindung hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="64c16-4616">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="64c16-4617">3.2.4.1.1 Senden einer cpmcistatueinout-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4617">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="64c16-4618">In der Regel wird der Protokoll Client von der höheren Ebene aufgefordert, eine cpmcistateinout-Nachricht zu senden, wenn Informationen zum Indizieren von Diensten auf dem Server erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-4618">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="64c16-4619">Wenn Sie aufgefordert werden, diese Nachricht zu senden, muss der Client folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4619">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4620">Senden Sie eine cpmcistateinout-Nachricht, wie im Abschnitt 2.2.3.1 angegeben, an den Server.</span><span class="sxs-lookup"><span data-stu-id="64c16-4620">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="64c16-4621">Warten Sie, bis die Meldung "cpmcistateinout" vom Server empfangen wurde, und verwerfen Sie alle anderen Nachrichten im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="64c16-4621">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="64c16-4622">Melden Sie den Wert des \_ Felds Status der Antwort, und bei erfolgreicher Ausführung die Informationsstruktur zurück zur höheren Ebene.</span><span class="sxs-lookup"><span data-stu-id="64c16-4622">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="64c16-4623">3.2.4.1.2 Senden einer cpmset| Status-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4623">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="64c16-4624">In der Regel wird der Protokoll Client von der höheren Ebene aufgefordert, eine cpmsetsinstatein-Nachricht zu senden, wenn er Informationen zu einem Katalog oder zu allen Katalogen benötigt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4624">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="64c16-4625">Für diese Nachricht muss die höhere Ebene dem Protokoll Client einen Wert für \_ dwnewstate und ggf. den Namen des Katalogs bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4625">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="64c16-4626">Wenn Sie aufgefordert werden, diese Nachricht zu senden, muss der Client folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4626">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4627">Senden Sie eine cpmsetcatstatein-Nachricht, wie in 2.2.3.2 angegeben, an den Server.</span><span class="sxs-lookup"><span data-stu-id="64c16-4627">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="64c16-4628">Warten Sie, bis eine cpmsetcatstateout-Nachricht vom Server empfangen wurde, und verwerfen Sie alle anderen Nachrichten im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="64c16-4628">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="64c16-4629">Melden Sie den Wert des \_ Felds Status der Antwort. wenn der Wert erfolgreich war, wird \_ dwoldstate wieder auf die höhere Ebene zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4629">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="64c16-4630">3.2.4.1.3 Senden einer cpmupdatedocumentsin-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4630">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="64c16-4631">Die höhere Ebene fordert normalerweise auf, diese Nachricht zu senden, wenn Sie Dokumente in einem vorhandenen Pfad aktualisieren oder dem Index einen neuen Dateipfad hinzufügen muss.</span><span class="sxs-lookup"><span data-stu-id="64c16-4631">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="64c16-4632">Daher besteht die höhere Ebene darin, den Pfad und den Typ eines Scans bereitzustellen, der im Abschnitt 2.2.3.4 angegeben ist, in dem ein inkrementelles oder vollständiges Update für vorhandene Pfade vorgesehen ist, und die neue Initialisierung ist für neue Pfade vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4632">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="64c16-4633">Der Client muss die folgenden Schritte ausführen, um die Anforderung höherer Ebene verarbeiten zu können:</span><span class="sxs-lookup"><span data-stu-id="64c16-4633">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4634">Senden Sie eine cpmupdatedocumentsin-Nachricht, wie im Abschnitt 2.2.3.4 angegeben, an den Server.</span><span class="sxs-lookup"><span data-stu-id="64c16-4634">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="64c16-4635">Warten Sie, bis die cpmupdatedocumentsin-Nachricht vom Server empfangen wurde, und verwerfen Sie alle anderen Nachrichten im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="64c16-4635">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="64c16-4636">Melden Sie den Wert des \_ Felds Status der Antwort zurück an die höhere Ebene.</span><span class="sxs-lookup"><span data-stu-id="64c16-4636">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="64c16-4637">3.2.4.1.4 Senden einer cpmforcemergein-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4637">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="64c16-4638">In der Regel fordert die höhere Schicht auf, diese Nachricht zu senden, wenn die Abfrageleistung verbessert werden muss, oder Sie ist Teil der geplanten Dienst Wartung für die Indizierung.</span><span class="sxs-lookup"><span data-stu-id="64c16-4638">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="64c16-4639">Um der höheren Ebene gerecht zu werden, muss der Client folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4639">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4640">Senden Sie die im Abschnitt 2.2.3.5 angegebene cpmforcemergein-Nachricht an den Server.</span><span class="sxs-lookup"><span data-stu-id="64c16-4640">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="64c16-4641">Warten Sie, bis eine cpmupdatedocumentsin-Nachricht vom Server empfangen wurde, und verwerfen Sie alle anderen Nachrichten im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="64c16-4641">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="64c16-4642">Melden Sie den Wert des \_ Felds Status der Antwort zurück an die höhere Ebene.</span><span class="sxs-lookup"><span data-stu-id="64c16-4642">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="64c16-4643">3.2.4.2-Dienst Katalog-Abfrage Nachrichten für Remote Indizierung</span><span class="sxs-lookup"><span data-stu-id="64c16-4643">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="64c16-4644">Mit Ausnahme von "cpmgetrowsin/cpmgetrowsout", "cpmfetchvaluein/cpmfetchvalueout" besteht eine 1:1-Beziehung zwischen CISP-Nachrichten und Anforderungen höherer Ebenen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4644">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="64c16-4645">Für die beiden oben genannten Ausnahmen können vom Client mehrere Nachrichten generiert werden, um die Größenanforderungen zu erfüllen oder eine gesamte Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4645">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="64c16-4646">Die höhere Ebene verfolgt in der Regel alle Abfrage spezifischen Informationen (z. b. geöffnetes Cursor Handle, zulässige Werte für Lesezeichen und Kapitel Handles, wid-Werte für verzögerte Eigenschaftswerte usw.) und nach, wenn der Client in einem verbundenen Zustand ist. Dies wird jedoch vom Client nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4646">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="64c16-4647">Zu Veranschaulichung veranschaulicht der Client Teil des Diagramms in Abschnitt 3 diese Sequenz für eine einfache Indizierungs Dienst Abfrage.</span><span class="sxs-lookup"><span data-stu-id="64c16-4647">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="64c16-4648">3.2.4.2.1 Senden einer cpmconnectin-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4648">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="64c16-4649">Bei dieser Nachricht handelt es sich in der Regel um die erste Anforderung von der höheren Ebene (wenn der Client nicht verbunden ist, wird der Großteil der Nachrichten vom Server mit Ausnahme von cpmsetcatstatein nicht ausgeführt).</span><span class="sxs-lookup"><span data-stu-id="64c16-4649">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="64c16-4650">Die höhere Ebene stellt dem Protokoll Client Informationen zur Verfügung, die zum Herstellen einer Verbindung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-4650">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="64c16-4651">Um die höhere Ebene zu verarbeiten, muss der Client die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4651">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4652">Füllen Sie die Nachricht mit Informationen aus, die der Client der höheren Ebene bereitgestellt hat (siehe Abschnitt 2.2.3.6) in \_ iclientversion, MachineName, username, PropertySet1, PropertySet2 und apropertyset.</span><span class="sxs-lookup"><span data-stu-id="64c16-4652">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="64c16-4653">Legen Sie " \_ lclientisremote", " \_ cbblob", "cbBlob2", " \_ cpropset" und "cextpropset" gemäß 2.2.3.6 fest</span><span class="sxs-lookup"><span data-stu-id="64c16-4653">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="64c16-4654">Legen Sie die Prüfsumme im \_ Feld ulchecksum fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-4654">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="64c16-4655">Sendet die cpmconnectin-Nachricht an den Server.</span><span class="sxs-lookup"><span data-stu-id="64c16-4655">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="64c16-4656">Warten Sie, bis eine cpmconnectout-Nachricht vom Server empfangen wurde, und verwerfen Sie alle anderen Nachrichten im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="64c16-4656">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="64c16-4657">Melden Sie den Wert des \_ Felds Status der Antwort. wenn dies erfolgreich war, wird die \_ Server Version wieder auf die höhere Ebene zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4657">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="64c16-4658">Zu informativen Zwecken wird erwartet, dass höhere Ebenen in der Regel die folgenden Aktionen ausführen, wenn eine Verbindung erfolgreich hergestellt wird, diese werden jedoch vom CISP-Client nicht erzwungen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4658">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="64c16-4659">Verwenden von Remote Index-Dienst Katalog-Verwaltungsnachrichten für administrative Aufgaben</span><span class="sxs-lookup"><span data-stu-id="64c16-4659">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="64c16-4660">Verwenden Sie eine cpmkreatequeryin-Anforderung, um eine Suchabfrage zu erstellen, mit der Ergebnisse aus dem Katalog abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4660">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="64c16-4661">3.2.4.2.2 Senden einer cpmkreatequeryin-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4661">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="64c16-4662">Die höhere Ebene stellt in der Regel Informationen für die Abfrage Erstellung bereit, sobald der Protokoll Client verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4662">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="64c16-4663">Die höhere Ebene stellt dem Client einen Einschränkungs Satz, Spalten Satz, Sortier Reihenfolgen-Regeln und einen Kategoriesatz (die jeweils weggelassen werden können), Rowseteigenschaften und Eigenschaften-ID-Mapper-Struktur bereit.</span><span class="sxs-lookup"><span data-stu-id="64c16-4663">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="64c16-4664">Wenn diese Anforderung von einer höheren Ebene empfangen wird, muss der Client die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4664">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4665">Bereiten Sie ein cpmkreatequeryout wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="64c16-4665">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="64c16-4666">Wenn ein Spalten Satz vorhanden ist, legen Sie ccolumnssetvoreinstellung auf 0x01 fest, und füllen Sie das columnsset-Feld aus.</span><span class="sxs-lookup"><span data-stu-id="64c16-4666">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="64c16-4667">Wenn Einschränkungen vorhanden sind, legen Sie "" auf "0x01" fest, und füllen Sie das Einschränkungs Feld aus.</span><span class="sxs-lookup"><span data-stu-id="64c16-4667">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="64c16-4668">Wenn eine Sortier Menge vorhanden ist, füllen Sie das sortset-Feld aus.</span><span class="sxs-lookup"><span data-stu-id="64c16-4668">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="64c16-4669">Wenn ein Kategorisierungs Satz vorhanden ist, legen Sie csortsetpresent auf 0x01 fest, und füllen Sie das Feld kategorizationset aus.</span><span class="sxs-lookup"><span data-stu-id="64c16-4669">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="64c16-4670">Legen Sie die übrigen Felder wie in 2.2.3.8 angegeben fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-4670">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="64c16-4671">Berechnen Sie \_ das ulchecksum-Feld in der Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="64c16-4671">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="64c16-4672">Senden Sie die cpmkreatequeryin-Nachricht an den Server.</span><span class="sxs-lookup"><span data-stu-id="64c16-4672">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="64c16-4673">Warten Sie, bis eine cpmkreatequeryout-Nachricht empfangen wird (siehe Details im Abschnitt 3.2.5.1.1), und verwerfen Sie alle anderen Nachrichten im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="64c16-4673">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="64c16-4674">Melden Sie den Wert des \_ Felds Status der Antwort, und, wenn er erfolgreich war, das Array von Cursor Handles und informative boolesche Werte (wie in 2.2.3.9 angegeben) zurück zur höheren Ebene.</span><span class="sxs-lookup"><span data-stu-id="64c16-4674">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="64c16-4675">3.2.4.2.3 Senden einer cpmsetbindingsin-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4675">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="64c16-4676">In der Regel legt die höhere Ebene Bindungen für jede Spalte fest, die in den Zeilen zurückgegeben wird, wenn Sie bereits über ein gültiges Cursor Handle verfügt (nach dem erfolgreichen Empfang von cpmkreatequeryout siehe Abschnitt 3.2.5.1.1).</span><span class="sxs-lookup"><span data-stu-id="64c16-4676">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="64c16-4677">Bei der höheren Version wird erwartet, dass ein Array von ctablecolumn-Strukturen, wie im Abschnitt 2.2.4.31 angegeben, für das Feld acolumschlag und ein gültiges Cursor Handle bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-4677">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="64c16-4678">Wenn diese Anforderung von der höheren Ebene empfangen wird, muss der Client die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4678">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4679">Berechnen Sie die Anzahl der ctablecolumn-Strukturen im acolenumns-Array, und legen Sie das CColumns-Feld auf diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-4679">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="64c16-4680">Berechnen Sie die Gesamtgröße der CColumns-und acolenns-Felder in Bytes, und legen \_ Sie für das Feld cbbindingdesc den Wert fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-4680">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="64c16-4681">Legen Sie in der cpmsetbindingsin-Nachricht angegebene Felder auf die Werte fest, die von der höheren Anwendungsebene bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4681">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="64c16-4682">Legen \_ Sie das Feld ulchecksum auf den im Abschnitt 3.2.5 angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-4682">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="64c16-4683">Sendet die abgeschlossene cpmsetbindignsin-Nachricht an den Server.</span><span class="sxs-lookup"><span data-stu-id="64c16-4683">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="64c16-4684">Warten Sie, bis eine cpmsetbindingsin-Nachricht vom Server empfangen wurde, und verwerfen Sie andere Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="64c16-4684">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="64c16-4685">Geben Sie den Status \_ des Felds Status der Antwort auf die höhere Ebene an.</span><span class="sxs-lookup"><span data-stu-id="64c16-4685">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="64c16-4686">Zu informativen Zwecken wird erwartet, dass eine höhere Ebene in der Regel einen Client anfordert, eine cpmgetrowsin-Nachricht zu senden. Dies wird jedoch nicht durch das Content Index Service-Protokoll erzwungen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4686">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="64c16-4687">3.2.4.2.4 Senden einer cpmgetrowsin-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4687">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="64c16-4688">Wenn die höhere Ebene im Begriff ist, Zeilen Informationen zu empfangen, stellt Sie Protokoll Client einen gültigen Cursor und ein Kapitel Handle bereit und gibt entsprechende Such Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4688">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="64c16-4689">In der Regel wird eine höhere Ebene erwartet, wenn Sie über ein gültiges Cursor-und/oder Kapitel Handle verfügt und die Bindungen mit der cpmsetbindingsin-Nachricht festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4689">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="64c16-4690">Um auf das Rowset in einem Kapitel zuzugreifen, besteht die höhere Ebene darin, das Kapitel Handle zu verwenden, das vom Server in einer früheren cpmgetrowsout-Nachricht empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="64c16-4690">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="64c16-4691">Wenn diese Anforderung von der höheren Ebene empfangen wird, muss der Client die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4691">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4692">Bestimmen Sie, welcher ganzzahlige Wert ohne Vorzeichen für das \_ cbreadbuffer-Feld angegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-4692">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="64c16-4693">Um diesen Wert zu bestimmen, muss der Client den maximalen Wert von folgendem annehmen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4693">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="64c16-4694">1000-mal der Wert des c- \_ rowstotransfer-Felds.</span><span class="sxs-lookup"><span data-stu-id="64c16-4694">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="64c16-4695">Wert von \_ cbrowwidth, aufgerundet auf das nächste 512 Byte Vielfache.</span><span class="sxs-lookup"><span data-stu-id="64c16-4695">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="64c16-4696">Verwenden Sie die höhere dieser beiden Werte, bis zum 16-KB-Limit.</span><span class="sxs-lookup"><span data-stu-id="64c16-4696">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="64c16-4697">In Fällen, in denen eine einzelne Zeile größer als 16K ist, kann der Server keine Ergebnisse an diese Abfrage zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4697">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="64c16-4698">Geben Sie eine Client Basis für Zeilendaten variabler Größe im Client Adressraum im \_ Feld ulclientbase an.</span><span class="sxs-lookup"><span data-stu-id="64c16-4698">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="64c16-4699">*Windows-Verhalten: bei einem 32-Bit-Client, der mit einem 32-Bit-Server kommuniziert, oder einem 64-Bit-Client, der mit einem 64-Bit-Server kommuniziert, wird dieser Wert auf eine Speicheradresse des empfangenden Puffers im Anwendungsprozess festgelegt. Dies ermöglicht die Verwendung von Zeigern, die im Feld Zeilen von cpmgetrowsout als korrekte Speicher Zeiger in einem Client Anwendungsprozess angezeigt werden. Andernfalls wird Sie auf 0x00000000 festgelegt.*</span><span class="sxs-lookup"><span data-stu-id="64c16-4699">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="64c16-4700">Berechnen Sie die Größe der Such Beschreibung, und legen Sie Sie im \_ Feld cbseek fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-4700">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="64c16-4701">Legen Sie den Wert von cbreserved (der als Offset für Zeilen Start fungieren soll) auf den Wert von \_ cbseek Plus 0x14 fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-4701">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="64c16-4702">Senden Sie eine cpmconnectin-Nachricht, die in 2.2.3.15 angegeben ist, an den Server.</span><span class="sxs-lookup"><span data-stu-id="64c16-4702">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="64c16-4703">3.2.4.2.5 Senden einer cpmfetchvaluein-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4703">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="64c16-4704">Wenn der Client eine cpmgetrowsout-Antwort vom Server empfängt, bei der das Status-Feld der Spalte auf statusaufgeschoben (0x01) festgelegt ist, bedeutet dies, dass der Eigenschafts Wert nicht im Zeilen Feld der cpmgetrowsout-Nachricht enthalten war.</span><span class="sxs-lookup"><span data-stu-id="64c16-4704">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="64c16-4705">In diesem Fall wird der Protokoll Client von der höheren Ebene in der Regel aufgefordert, den Wert mithilfe der cpmfetchvaluein-Nachricht abzurufen. Außerdem wird der Wert PROPSPEC und \_ wid für eine verzögerte Eigenschaft bereitgestellt, die der Protokoll Client in der ersten cpmfetchvaluein-Nachricht verwenden muss.</span><span class="sxs-lookup"><span data-stu-id="64c16-4705">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="64c16-4706">Wenn dies die erste cpmfetchvaluein-Nachricht ist, die der Client zum Anfordern der angegebenen Eigenschaft gesendet hat, muss der Client die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4706">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4707">Legen Sie alle Felder in einer Nachricht fest, wie im Abschnitt 2.2.3.19 angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4707">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="64c16-4708">Legen \_ Sie cbsofar auf 0x00000000 fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-4708">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="64c16-4709">Aktuelle empfangene Bytes auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4709">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="64c16-4710">Senden Sie die cpmfetchvaluein-Nachricht an den Server.</span><span class="sxs-lookup"><span data-stu-id="64c16-4710">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="64c16-4711">3.2.4.2.6 Senden einer cpmfreecursorin-Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c16-4711">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="64c16-4712">Wenn die Suchabfrage von der höheren Ebene nicht mehr verwendet wird, können die Ressourcen auf dem Server freigegeben werden, indem der Client aufgefordert wird, eine cpmfreecursorin-Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4712">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="64c16-4713">Wenn diese Anforderung empfangen wird, muss der Client eine in 2.2.3.28 angegebene cpmfreecursorin-Nachricht an den Server senden, die das von der oberen Ebene angegebene Handle enthält.</span><span class="sxs-lookup"><span data-stu-id="64c16-4713">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="64c16-4714">3.2.4.2.7 Senden einer cpmdisconnect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="64c16-4714">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="64c16-4715">Wenn die höhere Ebene keine Abfragen für den Indizierungs Dienst aufweist, kann die Anwendung zum Freigeben von mehr Server Ressourcen von der Anwendung anfordern, dass der Client eine cpmdisconnect-Nachricht an den Server sendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-4715">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="64c16-4716">Wenn diese Abfrage empfangen wird, muss der Client die Nachricht einfach wie angefordert senden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4716">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="64c16-4717">Vom Server wird keine Antwort auf diese Nachricht ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4717">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="64c16-4718">3.2.5 Nachrichtenverarbeitungs-und Sequenz Regeln</span><span class="sxs-lookup"><span data-stu-id="64c16-4718">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="64c16-4719">Wenn der Client eine Nachrichten Antwort vom Server empfängt, muss der Client die zuletzt gesendete Nachricht verwenden, um zu ermitteln, ob die vom Server empfangene Nachricht vom Client erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-4719">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="64c16-4720">Alle Nachrichten mit \_ einem Nachrichtenfeld, die sich von dem in der letzten Sende Nachricht unterscheiden, müssen ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4720">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="64c16-4721">3.2.5.1 empfängt eine cpmkreatequeryout-Antwort</span><span class="sxs-lookup"><span data-stu-id="64c16-4721">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="64c16-4722">Wenn der Client eine cpmanatequeryout-Nachrichten Antwort vom Server empfängt, muss der Client den \_ Status zurückgeben und (wenn der Status erfolgreich ist) den Cursor Werte zurück auf eine höhere Ebene zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4722">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="64c16-4723">Alle weiteren Aktionen befinden sich auf der höheren Ebene.</span><span class="sxs-lookup"><span data-stu-id="64c16-4723">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="64c16-4724">Wenn die höhere Ebene die Abfrage Struktur kennt, wird immer erwartet, dass die richtige Anzahl von Cursor Handles in der cpmkreateoueryout-Nachricht zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-4724">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="64c16-4725">Die Cursor Zieh Punkte werden in der folgenden Reihenfolge zurückgegeben: das erste Handle ist das unformatierte Rowset, das zweite ist das erste unterteilte Rowset (das die Gruppierung der Ergebnisse auf der Grundlage der ersten Kategorie ist, die im Feld "kategorizationset" der cpmkreatequeryin-Nachricht angegeben ist).</span><span class="sxs-lookup"><span data-stu-id="64c16-4725">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="64c16-4726">Für informative Zwecke wird erwartet, dass höhere Ebenen die folgenden Aktionen ausführen können. Diese werden jedoch nicht vom CISP-Client erzwungen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4726">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="64c16-4727">Verwenden Sie cpmsetbindingsin, um Bindungen für einzelne Spalten festzulegen, und führen Sie nachfolgende Aktionen für den Abfrage Pfad aus.</span><span class="sxs-lookup"><span data-stu-id="64c16-4727">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="64c16-4728">Verwenden Sie cpmgetquerystatusin, um den Ausführungs Fortschritt einer Abfrage zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4728">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="64c16-4729">Verwenden Sie cpmratiofinishedin, um den Abschluss Prozentsatz der Abfrage anzufordern.</span><span class="sxs-lookup"><span data-stu-id="64c16-4729">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="64c16-4730">3.2.5.2 empfangen einer cpmgetrowsout-Antwort</span><span class="sxs-lookup"><span data-stu-id="64c16-4730">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="64c16-4731">Wenn der Client eine cpmgetrowsout-Nachrichten Antwort vom Server empfängt, muss der Client die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4731">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4732">Überprüfen Sie, ob das \_ Feld Status in der Kopfzeile Erfolg oder Fehler anzeigt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4732">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="64c16-4733">Wenn der \_ Statuswert \_ \_ zu \_ klein ist (0xc0000023), muss der Client den Status der letzten gesendeten Nachricht überprüfen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4733">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="64c16-4734">Wenn keine cpmgetrowsin-Nachricht enthalten ist, muss die empfangene Nachricht automatisch ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4734">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="64c16-4735">Andernfalls muss der Client eine neue cpmgetrowsin-Nachricht an den Server senden, wobei alle Felder identisch mit der gespeicherten Nachricht sind, mit dem Unterschied, dass der \_ cbread-Puffer um 512 (aber nicht größer als 0x4000) erweitert werden muss.</span><span class="sxs-lookup"><span data-stu-id="64c16-4735">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="64c16-4736">Wenn \_ der Status Status \_ Puffer \_ zu \_ klein ist (0xc0000023) und die letzte gesendete Nachricht bereits \_ den Wert 0x4000 hat, muss der Client den Fehler auf der höheren Ebene melden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4736">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="64c16-4737">Wenn der \_ Statuswert ein anderer Fehlerwert ist, muss der Client den Fehler auf die höhere Ebene angeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4737">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="64c16-4738">Wenn der \_ Statuswert Erfolg anzeigt, müssen die Ergebnisse bis zu der höheren Ebene angezeigt werden, die die Informationen anfordert, und weitere Aktionen befinden sich auf der höheren Ebene.</span><span class="sxs-lookup"><span data-stu-id="64c16-4738">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="64c16-4739">Für informative Zwecke wird erwartet, dass höhere Ebenen in der Regel die folgenden Aktionen ausführen. Diese werden jedoch nicht vom Dienst Protokoll Client für die Inhalts Indizierung erzwungen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4739">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="64c16-4740">Wenn die Werte in Zeilen die Dokument-IDs darstellen, speichert Kapitel oder Lesezeichen die höhere Ebene in der Regel für die Verwendung in nachfolgenden Vorgängen, die gültige Dokument-IDs, Kapitel oder Lesezeichen Handles einschließen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4740">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="64c16-4741">Die höhere Ebene speichert oder verwendet normalerweise die Daten von Zeilen Werten.</span><span class="sxs-lookup"><span data-stu-id="64c16-4741">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="64c16-4742">Bei Werten, die als verzögerte höhere Ebene gekennzeichnet waren, wird der Wert mithilfe von cpmfetchvaluein-Nachrichten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4742">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="64c16-4743">Die Such Beschreibung wird ebenfalls an eine höhere Ebene zurückgegeben und kann von der höheren Ebene wieder verwendet oder überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4743">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="64c16-4744">Wenn die höhere Ebene für informative Zwecke Handles für Kapitel und Lesezeichen angefordert hat, die in den Zeilen empfangen wurden, kann es folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4744">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="64c16-4745">Verwenden Sie cpmgetquerystatusexin, um den Ausführungs Status einer Abfrage sowie weitere Statusinformationen (z. b. die Anzahl der gefilterten Dokumente, die verbleibenden Dokumente, die zu filternden Dokumente, das Verhältnis der von der Abfrage verarbeiteten Dokumente, die Gesamtanzahl der Zeilen in der Abfrage und die Position des Lesezeichens im Rowset) zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4745">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="64c16-4746">Verwenden Sie cpmgetnotify, um anzufordern, dass der Server den Client über Rowsetänderungen benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4746">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="64c16-4747">Verwenden Sie cpmgetapproximatepositionin, um die ungefähre Position eines Lesezeichens in einem Kapitel anzufordern.</span><span class="sxs-lookup"><span data-stu-id="64c16-4747">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="64c16-4748">Verwenden Sie cpmcomparebmkin, um einen Vergleich zweier Lesezeichen in einem Kapitel anzufordern.</span><span class="sxs-lookup"><span data-stu-id="64c16-4748">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="64c16-4749">Verwenden Sie cpmrestartpositionin zum Server, um die Position des Cursors auf den Anfang des Rowsets zu ändern.</span><span class="sxs-lookup"><span data-stu-id="64c16-4749">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="64c16-4750">3.2.5.3 empfängt eine cpmfetchvalueout-Antwort</span><span class="sxs-lookup"><span data-stu-id="64c16-4750">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="64c16-4751">Wenn der Client eine cpmgetrowsout-Nachrichten Antwort vom Server empfängt, muss der Client die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="64c16-4751">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="64c16-4752">Überprüfen Sie, ob das \_ Feld Status in der Kopfzeile Erfolg oder Fehler anzeigt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4752">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="64c16-4753">Benachrichtigen Sie bei einem Fehler die höhere Ebene.</span><span class="sxs-lookup"><span data-stu-id="64c16-4753">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="64c16-4754">Andernfalls fahren Sie mit fort.</span><span class="sxs-lookup"><span data-stu-id="64c16-4754">Otherwise, continue below.</span></span>
-   <span data-ttu-id="64c16-4755">Überprüfen Sie \_ fvalueexist, und wenn Sie auf 0x00000000 festgelegt ist, Benachrichtigen Sie die höhere Ebene, dass der Wert nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="64c16-4755">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="64c16-4756">Fügen Sie andernfalls \_ cbValue-Bytes aus vValue an den aktuellen Eigenschafts Wert an.</span><span class="sxs-lookup"><span data-stu-id="64c16-4756">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="64c16-4757">Wenn \_ \_ fmoreist auf 0x00000001 festgelegt ist, erhöhen \_ Sie die aktuellen bytes, die von \_ cbValue empfangen werden, und senden Sie eine cpmfetchvaluein-Nachricht an den Server \_ . Legen Sie cbsofar auf den Wert der empfangenen aktuellen bytes, \_ cbpropspec auf NULL und \_ cbblock auf die Puffergröße fest, die von der höheren Ebene gewünscht wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-4757">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="64c16-4758">Wenn \_ fmoreist auf 0x00000000 festgelegt ist, geben Sie den Eigenschafts Wert des aktuellen Eigenschafts Werts auf die höhere Ebene an.</span><span class="sxs-lookup"><span data-stu-id="64c16-4758">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="64c16-4759">3.2.5.4 empfängt eine cpmfreecursorout-Antwort</span><span class="sxs-lookup"><span data-stu-id="64c16-4759">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="64c16-4760">Wenn der Client eine erfolgreiche cpmfreecursorout-Nachrichten Antwort vom Server empfängt, muss der Client den \_ Wert "ccursor Rest" an die höhere Ebene zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4760">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="64c16-4761">Die folgenden Informationen werden nur für informative Zwecke angegeben und vom CISP-Client nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4761">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="64c16-4762">Die höhere Ebene wird erwartet, dass Cursor Zieh Punkte nachverfolgt und nicht verwendet werden, die bereits freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4762">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="64c16-4763">Sobald die Anzahl der \_ ccurrsors gleich 0x00000000 ist, kann die höhere Ebene die Verbindung verwenden, um eine andere Abfrage anzugeben (mithilfe einer cpmkreatequeryin-Nachricht).</span><span class="sxs-lookup"><span data-stu-id="64c16-4763">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="64c16-4764">3.2.6-Timer-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="64c16-4764">3.2.6 Timer Events</span></span>

<span data-ttu-id="64c16-4765">Keine.</span><span class="sxs-lookup"><span data-stu-id="64c16-4765">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="64c16-4766">3.2.7 andere lokale Ereignisse</span><span class="sxs-lookup"><span data-stu-id="64c16-4766">3.2.7 Other Local Events</span></span>

<span data-ttu-id="64c16-4767">Keine.</span><span class="sxs-lookup"><span data-stu-id="64c16-4767">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="64c16-4768">4 Beispiele für Protokolle</span><span class="sxs-lookup"><span data-stu-id="64c16-4768">4 Protocol Examples</span></span>

-   [<span data-ttu-id="64c16-4769">4,1 Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="64c16-4769">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="64c16-4770">4,2 Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="64c16-4770">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="64c16-4771">4,1 Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="64c16-4771">4.1 Example 1</span></span>

<span data-ttu-id="64c16-4772">Im folgenden Beispiel wird ein Szenario betrachtet, bei dem der Benutzer John auf Computer a die Größe der Dateien abrufen möchte, die das Wort "Microsoft" aus dem Satz von Dokumenten enthalten, die auf Server X im Katalog System gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-4772">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="64c16-4773">Nehmen wir an, dass auf Computer a ein 32-Bit-Betriebssystem unter Windows XP ausgeführt wird und auf dem Computer X ein 32-Bit Windows Server 2003-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64c16-4773">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="64c16-4774">Der Benutzer öffnet eine Suchanwendung und gibt die Suchabfrage ein.</span><span class="sxs-lookup"><span data-stu-id="64c16-4774">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="64c16-4775">Die Anwendung übergibt die Suchabfrage wiederum an den Protokoll Client.</span><span class="sxs-lookup"><span data-stu-id="64c16-4775">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="64c16-4776">Der Protokoll Client stellt eine Verbindung mit dem Indizierungs Server X her. Der Protokoll Client verwendet die Named Pipe \\ Pipe- \\ ci- \_ Skaden, um eine Verbindung mit dem Server X über SMB herzustellen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4776">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="64c16-4777">Der Protokoll Client bereitet dann eine cpmconnectin-Nachricht mit den folgenden Werten vor:</span><span class="sxs-lookup"><span data-stu-id="64c16-4777">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="64c16-4778">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4778">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4779">**\_ msg** wird auf 0x000000c8 festgelegt, was darauf hinweist, dass es sich hierbei um eine cpmconnectin-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4779">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="64c16-4780">der **\_ Status** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4780">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="64c16-4781">**\_ ulchecksum** enthält die Prüfsumme, wie in Abschnitt 3.2.4 angegeben.</span><span class="sxs-lookup"><span data-stu-id="64c16-4781">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="64c16-4782">**\_ ulReserved2** wird auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4782">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="64c16-4783">Der Nachrichtentext wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4783">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4784">**\_ iclientversion** ist auf 0x00000008 festgelegt und gibt an, dass der Server das Prüfsummen Feld validieren soll.</span><span class="sxs-lookup"><span data-stu-id="64c16-4784">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="64c16-4785">**\_ fclientisremote** ist auf 0x00000001 festgelegt und zeigt an, dass der Server ein Remote Server ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4785">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="64c16-4786">**\_ cbBlob1** wird auf die Größe (in Bytes) der cpropset-, PropertySet1-und PropertySet2-Felder kombiniert.</span><span class="sxs-lookup"><span data-stu-id="64c16-4786">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="64c16-4787">**\_ cbBlob2** wird auf 0x00000004 festgelegt (d.h. keine zusätzlichen Eigenschaften Sätze).</span><span class="sxs-lookup"><span data-stu-id="64c16-4787">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="64c16-4788">**MachineName** ist auf festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4788">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="64c16-4789">Der **Benutzername** ist auf John festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4789">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="64c16-4790">**cpropsets** ist auf 0x00000002 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4790">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="64c16-4791">Das **PropertySet1** -Feld ist vom Typ CDBPropSet.</span><span class="sxs-lookup"><span data-stu-id="64c16-4791">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="64c16-4792">Die CDBPropSet-Struktur, die das Feld "PropertySet1" enthält, wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4792">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="64c16-4793">Das Feld " **guidpropset** " ist auf "A9BD1526-6A80-11D0-8C9D-0020AF1D740E" (DBPROPSET \_ fscifrmwrk \_ ext) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4793">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="64c16-4794">**cproperties** -Feld ist auf 0x00000004 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4794">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="64c16-4795">das Feld " **aProp** " ist ein Array von cdbprop-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4795">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="64c16-4796">Für das **\[ arequi0 \]** -Element:</span><span class="sxs-lookup"><span data-stu-id="64c16-4796">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="64c16-4797">**PROPID** ist auf 0x00000002 (DBPROP \_ ci- \_ Katalog \_ Name) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4797">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="64c16-4798">**DBPROPOPTIONS** ist auf 0x0000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4798">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="64c16-4799">**Dbpropstatus** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4799">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="64c16-4800">Für das **ColId** -Element:</span><span class="sxs-lookup"><span data-stu-id="64c16-4800">For the **ColId** element:</span></span>
                -   <span data-ttu-id="64c16-4801">**eKind** ist auf 0x00000001 (dbkind \_ GUID \_ PROPID) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4801">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="64c16-4802">**GUID** ist NULL (alle Nullen), was bedeutet, dass der Wert für die Abfrage gilt, nicht nur für eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="64c16-4802">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="64c16-4803">" **ulid** " ist auf "0x00000000" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4803">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="64c16-4804">Für das **vValue** -Element:</span><span class="sxs-lookup"><span data-stu-id="64c16-4804">For the **vValue** element:</span></span>
                -   <span data-ttu-id="64c16-4805">**VType** ist auf 0x001F (VT \_ LPWSTR) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4805">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="64c16-4806">**vValue** ist auf "System" festgelegt, den Namen des gewünschten Katalogs.</span><span class="sxs-lookup"><span data-stu-id="64c16-4806">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="64c16-4807">Für das **\[ arequi1 \]** -Element:</span><span class="sxs-lookup"><span data-stu-id="64c16-4807">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="64c16-4808">**PROPID** ist auf 0x00000007 (DBPROP \_ ci- \_ Abfragetyp \_ ) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4808">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="64c16-4809">**DBPROPOPTIONS** ist auf 0x0000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4809">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="64c16-4810">**Dbpropstatus** ist Set to0x00000000.</span><span class="sxs-lookup"><span data-stu-id="64c16-4810">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="64c16-4811">Für das **ColId** -Element:</span><span class="sxs-lookup"><span data-stu-id="64c16-4811">For the **ColId** element:</span></span>
                -   <span data-ttu-id="64c16-4812">**eKind** ist auf 0x00000001 (dbkind \_ GUID \_ PROPID) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4812">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="64c16-4813">**GUID** ist NULL (alle Nullen), was bedeutet, dass der Wert für die Abfrage gilt, nicht nur für eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="64c16-4813">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="64c16-4814">" **ulid** " ist auf "0x00000000" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4814">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="64c16-4815">Für das **vValue** -Element:</span><span class="sxs-lookup"><span data-stu-id="64c16-4815">For the **vValue** element:</span></span>
                -   <span data-ttu-id="64c16-4816">**VType** ist auf 0x0003 erfordert (VT \_ I4) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4816">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="64c16-4817">**vValue** ist auf 0x00000000 (cinormal) festgelegt, was bedeutet, dass es sich um eine reguläre Abfrage handelt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4817">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="64c16-4818">Für das Element " **\[ arequi2 \]** ":</span><span class="sxs-lookup"><span data-stu-id="64c16-4818">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="64c16-4819">**PROPID** ist auf 0x00000004 (DBPROP \_ ci- \_ bereichsflags) festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="64c16-4819">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="64c16-4820">**DBPROPOPTIONS** ist auf 0x0000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4820">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="64c16-4821">**Dbpropstatus** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4821">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="64c16-4822">Für das **ColId** -Element:</span><span class="sxs-lookup"><span data-stu-id="64c16-4822">For the **ColId** element:</span></span>
                -   <span data-ttu-id="64c16-4823">**eKind** ist auf 0x00000001 (dbkind \_ GUID \_ PROPID) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4823">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="64c16-4824">**GUID** ist NULL (alle Nullen), was bedeutet, dass der Wert für die Abfrage gilt, nicht nur für eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="64c16-4824">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="64c16-4825">" **ulid** " ist auf "0x00000000" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4825">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="64c16-4826">Für das **vValue** -Element:</span><span class="sxs-lookup"><span data-stu-id="64c16-4826">For the **vValue** element:</span></span>
                -   <span data-ttu-id="64c16-4827">**VType**: 0x1003 (VT \_ Vector \| VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="64c16-4827">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="64c16-4828">**vValue**: 0x00000001/0x00000001 (ein Element mit Wert 1), d.h. Such Unterordner</span><span class="sxs-lookup"><span data-stu-id="64c16-4828">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="64c16-4829">Für das Element " **\[ arequi3 \]** ":</span><span class="sxs-lookup"><span data-stu-id="64c16-4829">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="64c16-4830">**PROPID**: 0x00000003 (DBPROP \_ ci \_ include- \_ Bereiche)</span><span class="sxs-lookup"><span data-stu-id="64c16-4830">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="64c16-4831">**DBPROPOPTIONS**: 0x0000000</span><span class="sxs-lookup"><span data-stu-id="64c16-4831">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="64c16-4832">**Dbpropstatus**: 0x00000000</span><span class="sxs-lookup"><span data-stu-id="64c16-4832">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="64c16-4833">Für das **ColId** -Element:</span><span class="sxs-lookup"><span data-stu-id="64c16-4833">For the **ColId** element:</span></span>
                -   <span data-ttu-id="64c16-4834">**eKind** ist auf 0x00000001 (dbkind \_ GUID \_ PROPID) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4834">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="64c16-4835">**GUID** ist NULL (alle Nullen), was bedeutet, dass der Wert für die Abfrage gilt, nicht nur für eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="64c16-4835">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="64c16-4836">" **ulid** " ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4836">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="64c16-4837">Für das **vValue** -Element:</span><span class="sxs-lookup"><span data-stu-id="64c16-4837">For the **vValue** element:</span></span>
                -   <span data-ttu-id="64c16-4838">**VType** ist auf 0x101 f (VT \_ Vector \| VT \_ LPWSTR) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4838">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="64c16-4839">**vValue** ist auf 0x00000001/0x00000002/"" festgelegt \\ (ein Element mit einer null-terminierten Zeichenfolge mit 2 Zeichen), d. h. der Stamm Bereich.</span><span class="sxs-lookup"><span data-stu-id="64c16-4839">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="64c16-4840">Das Feld **PropertySet2** ist vom Typ CDBPropSet.</span><span class="sxs-lookup"><span data-stu-id="64c16-4840">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="64c16-4841">Die CDBPropSet-Struktur, die das Feld "PropertySet1" enthält, wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4841">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="64c16-4842">**Guidpropset** ist auf AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D festgelegt (DBPROPSET \_ cifrmwrkcore \_ ext).</span><span class="sxs-lookup"><span data-stu-id="64c16-4842">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="64c16-4843">**cproperties** -Feld ist auf 0x00000001 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4843">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="64c16-4844">Das Feld " **aProp** " ist ein Array von cdbprop-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4844">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="64c16-4845">Für das **\[ arequi0 \]** -Element:</span><span class="sxs-lookup"><span data-stu-id="64c16-4845">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="64c16-4846">**PROPID** ist auf 0x00000002 (DBPROP- \_ Computer) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4846">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="64c16-4847">**DBPROPOPTIONS** ist auf 0x0000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4847">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="64c16-4848">**Dbpropstatus** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4848">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="64c16-4849">Für das **ColId** -Element:</span><span class="sxs-lookup"><span data-stu-id="64c16-4849">For the **ColId** element:</span></span>
                -   <span data-ttu-id="64c16-4850">**eKind** ist auf 0x00000001 (dbkind \_ GUID \_ PROPID) festgelegt,</span><span class="sxs-lookup"><span data-stu-id="64c16-4850">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="64c16-4851">**GUID** ist NULL (alle Nullen), was bedeutet, dass der Wert für die Abfrage gilt, nicht nur für eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="64c16-4851">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="64c16-4852">" **ulid** " ist auf "0x00000000" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4852">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="64c16-4853">Für **vValue** -Element:</span><span class="sxs-lookup"><span data-stu-id="64c16-4853">For **vValue** element:</span></span>
                -   <span data-ttu-id="64c16-4854">**VType**: 0x0008 (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="64c16-4854">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="64c16-4855">**vValue**: 0x04/"X" (4 Bytes/NULL-terminierte Unicode-Zeichenfolge), d. h. "x", Name eines Servers.</span><span class="sxs-lookup"><span data-stu-id="64c16-4855">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="64c16-4856">Das **cextpropset** -Feld ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4856">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="64c16-4857">Das **apropertysets** -Array ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4857">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="64c16-4858">Je nach Bedarf werden verschiedene Auffüll Felder ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4858">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="64c16-4859">Die Nachricht wird an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="64c16-4859">The message is sent to the server.</span></span>

4.  <span data-ttu-id="64c16-4860">Der Server überprüft, ob **\_ ulchecksum** korrekt ist, überprüft, ob der Benutzer zum Ausführen dieser Anforderung autorisiert ist, und antwortet mit einer cpmconnectout-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-4860">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="64c16-4861">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4861">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4862">**\_ msg** wird auf 0x000000c8 festgelegt, was darauf hinweist, dass es sich hierbei um eine cpmconnectout-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4862">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="64c16-4863">der **\_ Status** wird auf 0x0000000 festgelegt, was den Erfolg angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4863">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="64c16-4864">**\_ ulchecksum** ist auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4864">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="64c16-4865">**\_ ulReserved2** wird auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4865">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="64c16-4866">Der Nachrichtentext wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4866">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4867">das Feld **\_ Serverversion** ist auf 0x00000007 (32-Bit Windows XP oder 32-Bit Windows Server 2003) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4867">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="64c16-4868">**\_ reservierte** Felder werden mit beliebigen Daten gefüllt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4868">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="64c16-4869">Der Client bereitet eine cpmkreatequeryin-Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="64c16-4869">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="64c16-4870">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4870">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4871">**\_ msg** wird auf 0x000000CA festgelegt, was darauf hinweist, dass es sich hierbei um eine cpmkreatequeryin-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4871">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="64c16-4872">der **\_ Status** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4872">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="64c16-4873">**\_ ulchecksum** enthält die Prüfsumme, berechnet nach 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="64c16-4873">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="64c16-4874">**\_ ulReserved2** wird auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4874">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="64c16-4875">Der Nachrichtentext wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4875">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4876">Das **Größen** Feld ist auf die Größe der restlichen Nachricht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4876">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="64c16-4877">Das Feld " **ccolumnsetpresent** " ist auf "0x01" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4877">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="64c16-4878">Das **ColumnSet** -Feld ist vom Typ "ccolumnset".</span><span class="sxs-lookup"><span data-stu-id="64c16-4878">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="64c16-4879">Die ccolumnset-Struktur, die dieses Feld enthält, wird wie folgt festgelegt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4879">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="64c16-4880">Das **\_ count** -Feld ist auf 0x00000001 festgelegt, um anzugeben, dass eine Spalte zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="64c16-4880">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="64c16-4881">Das **Index** Array ist 0x00000000, das den ersten Eintrag in \_ apropspec angibt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4881">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="64c16-4882">Das Feld " **krestrictionpresent** " ist auf 0x01 festgelegt, um anzugeben, dass das **Einschränkungs** Feld vorhanden</span><span class="sxs-lookup"><span data-stu-id="64c16-4882">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="64c16-4883">Das **Einschränkungs** Feld ist vom Typ "krestriction" und wird auf Folgendes festgelegt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4883">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="64c16-4884">**\_ ultype** ist auf 0x00000004 (rtcontent) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4884">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="64c16-4885">**\_ Weight** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4885">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="64c16-4886">Der Rest des Felds enthält eine Ccontent-Einschränkungs Struktur:</span><span class="sxs-lookup"><span data-stu-id="64c16-4886">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="64c16-4887">Die **\_ Eigenschaft** ist auf GUID B725F130-47EF-101A-A5F1-02608c9eebac/0x00000001 (für prspec \_ PROPID)/0x13 festgelegt, die den Dokument Text darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4887">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="64c16-4888">**\_ CC** ist auf 0x00000009 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4888">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="64c16-4889">**\_ pwcspphrase** ist auf die Zeichenfolge "Microsoft" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4889">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="64c16-4890">**\_ LCID** ist auf 0x409 (für Englisch) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4890">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="64c16-4891">**\_ ulgeneratemethod** ist auf 0x00000000 (exakte Entsprechung) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4891">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="64c16-4892">**Csortpresent** ist auf 0x00 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4892">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="64c16-4893">" **Ccategorizationsetpresent** " ist auf "0x00" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4893">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="64c16-4894">**Rowsetproperties** wird wie folgt festgelegt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4894">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="64c16-4895">**\_ ubooleanoptions** ist auf 0x00000001 (sequenziell) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4895">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="64c16-4896">**\_ ulmaxopenrows** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4896">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="64c16-4897">**\_ ulmemoryusage** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4897">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="64c16-4898">\_**cmaxresults** ist auf 0x00000100 festgelegt (gibt höchstens 256 Zeilen zurück).</span><span class="sxs-lookup"><span data-stu-id="64c16-4898">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="64c16-4899">**\_ ccmdtimeout** ist auf 0x00000000 (nie Timeout) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4899">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="64c16-4900">**Pidmapper** ist auf Folgendes festgelegt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4900">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="64c16-4901">**\_ count** ist auf 0x00000001 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4901">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="64c16-4902">**\_ apropspec** ist auf GUID B725F130-47ef-101 a-A5-F1-02608c9eebac/0x00000001 (für prspec \_ PROPID)/0x0000000c festgelegt, das die Windows-Dateigrößen Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4902">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="64c16-4903">Der Server verarbeitet ihn und antwortet mit einer cpmkreatequeryout-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-4903">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="64c16-4904">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4904">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4905">**\_ msg** wird auf 0x000000CA festgelegt, was darauf hinweist, dass es sich hierbei um eine cpmkreatequeryout-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4905">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="64c16-4906">der **\_ Status** ist auf "erfolgreich" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4906">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="64c16-4907">**\_ ulchecksum** ist auf 0x00000000 (oder einen beliebigen anderen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4907">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="64c16-4908">**\_ ulReserved2** wird auf 0x00000000 (oder einen beliebigen anderen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4908">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="64c16-4909">Der Nachrichtentext wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4909">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4910">**\_ ftrueseqeuntial** ist auf 0x00000000 festgelegt und zeigt an, dass die Abfrage einen Index verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="64c16-4910">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="64c16-4911">**\_ fworkidunique** ist auf 0x00000001 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4911">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="64c16-4912">Das **acursors** -Array enthält nur ein-Element, das ein Cursor Handle für diese Abfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4912">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="64c16-4913">Der Wert hängt vom Status des Servers ab.</span><span class="sxs-lookup"><span data-stu-id="64c16-4913">The value depends on the state of the server.</span></span> <span data-ttu-id="64c16-4914">Nehmen wir an, dass der zurückgegebene Wert 0xaaaaaaaa ist.</span><span class="sxs-lookup"><span data-stu-id="64c16-4914">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="64c16-4915">Der Client gibt eine cpmsetbindingsin-Anforderungs Nachricht aus, um das Format einer Zeile zu definieren.</span><span class="sxs-lookup"><span data-stu-id="64c16-4915">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="64c16-4916">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4916">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4917">die Meldung wird auf 0x000000d0 festgelegt, was darauf hinweist, dass es sich hierbei um eine cpmsetbindingsin- **\_ Nachricht handelt.**</span><span class="sxs-lookup"><span data-stu-id="64c16-4917">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="64c16-4918">der **\_ Status** ist auf "erfolgreich" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4918">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="64c16-4919">**\_ ulchecksum** ist auf 0x00000000 (oder einen beliebigen anderen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4919">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="64c16-4920">**\_ ulReserved2** wird auf 0x00000000 (oder einen beliebigen anderen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4920">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="64c16-4921">Der Nachrichtentext wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4921">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4922">**\_ hcursor** ist auf 0xaaaaaaaa festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4922">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="64c16-4923">**\_ cbrow** ist auf 0x10 (groß genug für Spalten) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4923">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="64c16-4924">" **\_ cbbindingdesc** " wird auf die Größe der **\_ CColumns** -und **\_ acolenns** -Felder kombiniert.</span><span class="sxs-lookup"><span data-stu-id="64c16-4924">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="64c16-4925">**\_ CColumns** ist auf 0x00000001 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4925">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="64c16-4926">Das **\_ acolumns** -Array ist auf eine ctablecolumn-Struktur mit folgenden Werten festgelegt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4926">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="64c16-4927">**\_ PROPSPEC** ist auf GUID b725f130-47ef-101 a-A5-F1-02608c9eebac/0x00000001 (für prspec \_ PROPID)/0x0000000c festgelegt, das die Windows-Dateigrößen Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4927">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="64c16-4928">**\_ VType** ist auf 0x0015 (VT \_ UI8) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4928">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="64c16-4929">**\_ Valueused** ist auf 0x01 festgelegt (Spalte in Zeile übertragen).</span><span class="sxs-lookup"><span data-stu-id="64c16-4929">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="64c16-4930">**\_ Valueoffset** ist auf 0x0002 (am Anfang der Zeile) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4930">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="64c16-4931">**\_ Valuesize** ist auf 0x08 (Größe eines VT- \_ UI8) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4931">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="64c16-4932">**\_ Status** wird auf 0x01 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4932">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="64c16-4933">" **\_ Status-ffset** " ist auf "0x0A" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4933">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="64c16-4934">Die **\_ Längen Verwendung** wird auf 0x00 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4934">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="64c16-4935">Der Server verarbeitet ihn und antwortet mit einer cpmsetbindingsin-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-4935">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="64c16-4936">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4936">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4937">die **\_ Meldung wird auf** 0x000000d0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4937">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="64c16-4938">der **\_ Status** ist auf "erfolgreich" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4938">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="64c16-4939">**\_ ulchecksum** ist auf 0x00000000 (oder einen beliebigen anderen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4939">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="64c16-4940">**\_ ulReserved2** wird auf 0x00000000 (oder einen beliebigen anderen beliebigen Wert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4940">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="64c16-4941">Der Client gibt eine cpmgetrowsin-Anforderungs Nachricht aus.</span><span class="sxs-lookup"><span data-stu-id="64c16-4941">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="64c16-4942">Nehmen wir an, dass der Client auf die Annahme von 100 Zeilen an dieser Stelle vorbereitet ist und Sie in aufsteigender Reihenfolge anfordert.</span><span class="sxs-lookup"><span data-stu-id="64c16-4942">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="64c16-4943">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4943">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4944">die Meldung wird auf 0x000000cc festgelegt, was darauf hinweist, dass es sich um eine cpmgetrowsin- **\_ Nachricht handelt.**</span><span class="sxs-lookup"><span data-stu-id="64c16-4944">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="64c16-4945">der **\_ Status** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4945">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="64c16-4946">**\_ ulchecksum** enthält die Prüfsumme, berechnet gemäß Abschnitt 0.</span><span class="sxs-lookup"><span data-stu-id="64c16-4946">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="64c16-4947">**\_ ulReserved2** wird auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4947">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="64c16-4948">Der Nachrichtentext wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4948">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4949">**\_ hcursor** ist auf 0xaaaaaaaa festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4949">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="64c16-4950">**\_ crowstotransfer** ist auf 0x00000064 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4950">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="64c16-4951">**\_ crowwidth** ist auf 0x00000010 (aus Bindungen) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4951">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="64c16-4952">**\_ cbseek** ist auf 0x14 festgelegt, d. h. die Größe der ETYPE \_ -, chapt-und crowseeknext-Felder kombiniert.</span><span class="sxs-lookup"><span data-stu-id="64c16-4952">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="64c16-4953">**\_ cbreserved** ist auf 0x18 (0x14 Plus \_ cbseek) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4953">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="64c16-4954">**\_ cbreadbuffer** ist auf 0x800 (0x64 \* 0x10 aufgerundet auf das nächste Vielfache von 0x200) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4954">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="64c16-4955">**\_ ulclientbase** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4955">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="64c16-4956">**\_ fbwdfetch** ist auf 0x00000000 festgelegt, um anzugeben, dass die Zeilen in der Reihenfolge abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4956">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="64c16-4957">**ETYPE** ist auf 0x0000001 festgelegt, um anzugeben, dass der Client nächste Zeilen anfordert.</span><span class="sxs-lookup"><span data-stu-id="64c16-4957">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="64c16-4958">" **\_ chapt** " wird auf 0 (kein in Kapitel unterteilt) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4958">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="64c16-4959">**Seekdescription** ist auf crowseeknext festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4959">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="64c16-4960">Die crowseeknext-Struktur enthält die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="64c16-4960">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="64c16-4961">**Citblchapt** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4961">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="64c16-4962">**\_ hregion** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4962">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="64c16-4963">**\_ cskip** ist auf 0 festgelegt, um anzugeben, dass der Client keine Zeilen auslassen möchte.</span><span class="sxs-lookup"><span data-stu-id="64c16-4963">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="64c16-4964">Der Server verarbeitet ihn und antwortet mit einer cpmgetrowsout-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64c16-4964">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="64c16-4965">Nehmen wir an, dass der Server 100 Dokumente gefunden hat, die das Wort "Microsoft" enthalten.</span><span class="sxs-lookup"><span data-stu-id="64c16-4965">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="64c16-4966">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4966">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4967">die Meldung wird auf 0x000000cc festgelegt, was darauf hinweist, dass es sich um eine cpmgetrowsout- **\_ Nachricht handelt.**</span><span class="sxs-lookup"><span data-stu-id="64c16-4967">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="64c16-4968">der **\_ Status** ist auf "erfolgreich" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4968">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="64c16-4969">**\_ ulchecksum** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4969">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="64c16-4970">**\_ ulReserved2** wird auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4970">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="64c16-4971">Der Nachrichtentext wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4971">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4972">**\_ Crowszurück gegeben** ist auf 0x00000064 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4972">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="64c16-4973">**ETYPE** ist auf 0x00000001 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4973">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="64c16-4974">" **\_ chapt** " ist auf "0x00000000" (kein in Kapitel unterteilt) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4974">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="64c16-4975">**Seekdescription** enthält eine crowseeknext-Struktur, die wie folgt aufgefüllt wird:</span><span class="sxs-lookup"><span data-stu-id="64c16-4975">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="64c16-4976">**Citblchapt** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4976">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="64c16-4977">**\_ hregion** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4977">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="64c16-4978">**\_ cskip** ist auf 0 festgelegt, um anzugeben, dass der Client keine Zeilen auslassen möchte.</span><span class="sxs-lookup"><span data-stu-id="64c16-4978">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="64c16-4979">**Zeilen** enthalten die Größe der 100-Dokumente, die das Wort "Microsoft" enthalten.</span><span class="sxs-lookup"><span data-stu-id="64c16-4979">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="64c16-4980">Da es sich hierbei um Daten mit fester Größe handelt, wird Sie einfach als Liste von 100, 8-Byte-Ganzzahlen ohne Vorzeichen strukturiert.</span><span class="sxs-lookup"><span data-stu-id="64c16-4980">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="64c16-4981">Der Client sendet eine cpmdisconnect-Nachricht, um die Verbindung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="64c16-4981">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="64c16-4982">Der Header der Nachricht wird wie folgt aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4982">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="64c16-4983">**\_ msg** wird auf 0x000000c9 festgelegt, was darauf hinweist, dass es sich um eine cpmdisconnect-Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4983">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="64c16-4984">der **\_ Status** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4984">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="64c16-4985">**\_ ulchecksum** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4985">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="64c16-4986">Der Server verarbeitet die Nachricht und entfernt den gesamten Client Zustand.</span><span class="sxs-lookup"><span data-stu-id="64c16-4986">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="64c16-4987">4,2 Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="64c16-4987">4.2 Example 2</span></span>

<span data-ttu-id="64c16-4988">Im vorherigen Beispiel war die Abfrage recht einfach.</span><span class="sxs-lookup"><span data-stu-id="64c16-4988">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="64c16-4989">Lassen Sie uns nun eine etwas komplexere Abfrage in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4989">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="64c16-4990">Nehmen wir an, dass der Benutzer die Größe der Dokumente abrufen möchte, die beide die folgenden Wörter enthalten: "Microsoft" und "Office".</span><span class="sxs-lookup"><span data-stu-id="64c16-4990">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="64c16-4991">Dies wird angegeben, indem das Einschränkungs Feld in der in Schritt 5 gesendeten Meldung cpmkreatequeryin wie folgt geändert wird:</span><span class="sxs-lookup"><span data-stu-id="64c16-4991">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="64c16-4992">Das **Einschränkungs** Feld ist vom Typ "krestriction" und wird auf Folgendes festgelegt:</span><span class="sxs-lookup"><span data-stu-id="64c16-4992">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="64c16-4993">**\_ ultype** ist auf 0x00000004 (rtand) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4993">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="64c16-4994">**\_ Weight** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4994">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="64c16-4995">Der Rest des Felds enthält eine cnoderestriction-Struktur:</span><span class="sxs-lookup"><span data-stu-id="64c16-4995">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="64c16-4996">**\_ CNode** ist auf 0x00000002 festgelegt und gibt an, dass zwei Knoten im panode-Array vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="64c16-4996">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="64c16-4997">Das **\_ panode** -Feld ist ein Array aus zwei Struktur Strukturen.</span><span class="sxs-lookup"><span data-stu-id="64c16-4997">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="64c16-4998">**\_ panode \[ 0 \]** enthält:</span><span class="sxs-lookup"><span data-stu-id="64c16-4998">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="64c16-4999">**\_ ultype** ist auf 0x00000004 (rtcontent) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-4999">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="64c16-5000">**\_ Weight** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-5000">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="64c16-5001">Der Rest des Felds enthält eine Ccontent-Einschränkungs Struktur:</span><span class="sxs-lookup"><span data-stu-id="64c16-5001">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="64c16-5002">Die **\_ Eigenschaft** ist auf GUID b725f130-47ef-101A-a5f1-02608c9eebac/0x00000001 (für prspec \_ PROPID)/0x13 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-5002">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="64c16-5003">**\_ CC** ist auf 0x00000009 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-5003">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="64c16-5004">**\_ pwcspphrase** ist auf die Zeichenfolge "Microsoft" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-5004">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="64c16-5005">**\_ LCID** ist auf 0x409 (für Englisch) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-5005">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="64c16-5006">**\_ ulgeneratemethod** ist auf 0x00000000 (exakte Entsprechung) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-5006">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="64c16-5007">**\_ panode \[ 1 \]** enthält:</span><span class="sxs-lookup"><span data-stu-id="64c16-5007">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="64c16-5008">**\_ ultype** ist auf 0x00000004 (rtcontent) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-5008">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="64c16-5009">**\_ Weight** ist auf 0x00000000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-5009">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="64c16-5010">Der Rest des Felds enthält eine Ccontent-Einschränkungs Struktur:</span><span class="sxs-lookup"><span data-stu-id="64c16-5010">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="64c16-5011">Die **\_ Eigenschaft** ist auf GUID b725f130-47ef-101A-a5f1-02608c9eebac/0x00000001 (für prspec \_ PROPID)/0x13 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-5011">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="64c16-5012">**\_ CC** ist auf 0x00000006 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-5012">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="64c16-5013">**\_ pwcspphrase** ist auf die Zeichenfolge "Office" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-5013">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="64c16-5014">**\_ LCID** ist auf 0x409 (für Englisch) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-5014">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="64c16-5015">**\_ ulgeneratemethod** ist auf 0x00000000 (exakte Entsprechung) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="64c16-5015">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="64c16-5016">5 Sicherheit</span><span class="sxs-lookup"><span data-stu-id="64c16-5016">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="64c16-5017">5.1 Sicherheitsüberlegungen für Ausführende</span><span class="sxs-lookup"><span data-stu-id="64c16-5017">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="64c16-5018">Indizierung von Implementierungen, bei denen sichere Inhalte indiziert werden, sollte in Erwägung gezogen werden, den von SMB MS-SMB bereitgestellten Benutzer Kontext \[ \] zum Kürzen von Suchergebnissen zu verwenden</span><span class="sxs-lookup"><span data-stu-id="64c16-5018">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="64c16-5019">5.2 Index von Sicherheitsparameter</span><span class="sxs-lookup"><span data-stu-id="64c16-5019">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="64c16-5020">Sicherheits Parameter</span><span class="sxs-lookup"><span data-stu-id="64c16-5020">Security Parameter</span></span>  | <span data-ttu-id="64c16-5021">`Section`</span><span class="sxs-lookup"><span data-stu-id="64c16-5021">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="64c16-5022">Ebene des Identitätswechsels</span><span class="sxs-lookup"><span data-stu-id="64c16-5022">Impersonation level</span></span> | <span data-ttu-id="64c16-5023">2.1</span><span class="sxs-lookup"><span data-stu-id="64c16-5023">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="64c16-5024">6 Index des Versions spezifischen Verhaltens</span><span class="sxs-lookup"><span data-stu-id="64c16-5024">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="64c16-5025">Versions spezifisches Verhalten</span><span class="sxs-lookup"><span data-stu-id="64c16-5025">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="64c16-5026">`Section`</span><span class="sxs-lookup"><span data-stu-id="64c16-5026">Section</span></span>   | <span data-ttu-id="64c16-5027">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="64c16-5027">Windows 2000</span></span> | <span data-ttu-id="64c16-5028">Windows XP</span><span class="sxs-lookup"><span data-stu-id="64c16-5028">Windows XP</span></span> | <span data-ttu-id="64c16-5029">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="64c16-5029">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="64c16-5030">Dieses Protokoll ist unter Windows 2000, Windows XP, Windows Server 2003 und Windows Vista implementiert.</span><span class="sxs-lookup"><span data-stu-id="64c16-5030">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="64c16-5031">1.3.2</span><span class="sxs-lookup"><span data-stu-id="64c16-5031">1.3.2</span></span>     | <span data-ttu-id="64c16-5032">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5032">X</span></span>            | <span data-ttu-id="64c16-5033">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5033">X</span></span>          | <span data-ttu-id="64c16-5034">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5034">X</span></span>                   |
| <span data-ttu-id="64c16-5035">Anwendungen interagieren in der Regel mit einem OLE DB Schnittstellen Wrapper</span><span class="sxs-lookup"><span data-stu-id="64c16-5035">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="64c16-5036">1.4</span><span class="sxs-lookup"><span data-stu-id="64c16-5036">1.4</span></span>       | <span data-ttu-id="64c16-5037">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5037">X</span></span>            | <span data-ttu-id="64c16-5038">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5038">X</span></span>          | <span data-ttu-id="64c16-5039">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5039">X</span></span>                   |
| <span data-ttu-id="64c16-5040">NTSTATUS-Werte</span><span class="sxs-lookup"><span data-stu-id="64c16-5040">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="64c16-5041">1.8</span><span class="sxs-lookup"><span data-stu-id="64c16-5041">1.8</span></span>       | <span data-ttu-id="64c16-5042">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5042">X</span></span>            | <span data-ttu-id="64c16-5043">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5043">X</span></span>          | <span data-ttu-id="64c16-5044">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5044">X</span></span>                   |
| <span data-ttu-id="64c16-5045">Der Client legt das \_ Feld Status in den einzelnen Nachrichten Headern fest.</span><span class="sxs-lookup"><span data-stu-id="64c16-5045">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="64c16-5046">2.2.2</span><span class="sxs-lookup"><span data-stu-id="64c16-5046">2.2.2</span></span>     | <span data-ttu-id="64c16-5047">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5047">X</span></span>            | <span data-ttu-id="64c16-5048">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5048">X</span></span>          | <span data-ttu-id="64c16-5049">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5049">X</span></span>                   |
| <span data-ttu-id="64c16-5050">der cpdingscans-Wert ist in der Regel NULL</span><span class="sxs-lookup"><span data-stu-id="64c16-5050">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="64c16-5051">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="64c16-5051">2.2.3.1</span></span>   | <span data-ttu-id="64c16-5052">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5052">X</span></span>            | <span data-ttu-id="64c16-5053">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5053">X</span></span>          | <span data-ttu-id="64c16-5054">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5054">X</span></span>                   |
| <span data-ttu-id="64c16-5055">iclientversion-Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-5055">iClientVersion value</span></span>                                                                              | <span data-ttu-id="64c16-5056">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="64c16-5056">2.2.3.6</span></span>   | <span data-ttu-id="64c16-5057">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5057">X</span></span>            | <span data-ttu-id="64c16-5058">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5058">X</span></span>          | <span data-ttu-id="64c16-5059">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5059">X</span></span>                   |
| <span data-ttu-id="64c16-5060">\_cbchunk-Wert</span><span class="sxs-lookup"><span data-stu-id="64c16-5060">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="64c16-5061">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="64c16-5061">2.2.3.19</span></span>  | <span data-ttu-id="64c16-5062">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5062">X</span></span>            | <span data-ttu-id="64c16-5063">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5063">X</span></span>          | <span data-ttu-id="64c16-5064">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5064">X</span></span>                   |
| <span data-ttu-id="64c16-5065">32-Bit-und 64-Bit-Speicheradressen</span><span class="sxs-lookup"><span data-stu-id="64c16-5065">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="64c16-5066">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="64c16-5066">3.2.4.2.4</span></span> | <span data-ttu-id="64c16-5067">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5067">X</span></span>            | <span data-ttu-id="64c16-5068">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5068">X</span></span>          | <span data-ttu-id="64c16-5069">X</span><span class="sxs-lookup"><span data-stu-id="64c16-5069">X</span></span>                   |



 

 

 





