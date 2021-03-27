---
description: 'Das Search: Application-Protokoll ist eine erweiterbare Konvention zum Aufrufen der Desktop Suchanwendung unter Windows Vista mit Service Pack 1 (SP1) und höheren Versionen.'
title: Verwenden des Such Protokolls
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 91a1ec25-f6ab-4377-8478-20bc51a1d5df
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a9223a2a30cab85f8e1b0dac0d0df2dc4fe8f80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995030"
---
# <a name="using-the-search-protocol"></a><span data-ttu-id="3300f-103">Verwenden des Such Protokolls</span><span class="sxs-lookup"><span data-stu-id="3300f-103">Using the search Protocol</span></span>

<span data-ttu-id="3300f-104">Das **Search:** [Application-Protokoll](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) ist eine erweiterbare Konvention zum Aufrufen der Desktop Suchanwendung unter Windows Vista mit Service Pack 1 (SP1) und höheren Versionen.</span><span class="sxs-lookup"><span data-stu-id="3300f-104">The **search:** [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is an extensible convention for calling the desktop search application on Windows Vista with Service Pack 1 (SP1) and later versions.</span></span> <span data-ttu-id="3300f-105">Das Protokoll wurde in Windows Vista mit SP1 erstellt (Weitere Informationen finden Sie im Knowledge Base [-Artikelübersicht über Änderungen der Windows Vista-Desktop Suche in Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)), damit Windows eine Möglichkeit erhält, die standardmäßige Desktop Suchanwendung zu ermitteln und aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="3300f-105">The protocol was created in Windows Vista with SP1 (for information see the Knowledge Base article [Overview of Windows Vista desktop search Changes in Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)) to give Windows a way to determine and call the default desktop search application.</span></span>

<span data-ttu-id="3300f-106">Die Protokoll Syntax bietet eine Reihe von Parametern, die für die Durchführung allgemeiner Desktop Suchvorgänge nützlich sind, wie z. b. vom Benutzer eingegebene Suchbegriffe oder den Speicherort der Suche.</span><span class="sxs-lookup"><span data-stu-id="3300f-106">The protocol syntax provides a number of parameters useful for performing common desktop searches, such as user-entered search terms or the location on which the search was begun.</span></span> <span data-ttu-id="3300f-107">Wenn Benutzer von einem der beiden verfügbaren Such Einstiegspunkte (dem **Startmenü** oder Windows-Explorer) suchen, wird vom Betriebssystem das Such Protokoll verwendet, um die Standardanwendung für die Desktop Suche zu starten.</span><span class="sxs-lookup"><span data-stu-id="3300f-107">When users search from one of the two available search entry points (either the **Start** menu or Windows Explorer), the operating system uses the search protocol to launch the default desktop search application.</span></span> <span data-ttu-id="3300f-108">Dies geschieht, indem die vom Benutzer eingegebenen Suchbegriffe der standardmäßigen Such Protokoll Syntax hinzugefügt und diese Informationen an die Anwendung übergeben werden, die als Standard Suchanwendung registriert ist.</span><span class="sxs-lookup"><span data-stu-id="3300f-108">It does this by adding the user-entered search terms to the standard search protocol syntax and passing that information to the application registered as the default search application.</span></span>

<span data-ttu-id="3300f-109">Wenn keine anderen Desktop Suchanwendungen installiert sind, wird in einer in diese Einstiegspunkte eingegebenen Suche der Windows Search-Explorer gestartet.</span><span class="sxs-lookup"><span data-stu-id="3300f-109">If no other desktop search applications are installed, a search entered into these entry points launches the Windows Search Explorer.</span></span> <span data-ttu-id="3300f-110">Entwickler von Drittanbietern können Ihre Anwendungen jedoch erstellen, installieren und registrieren, um das Such Protokoll und die Standard Suchanwendung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3300f-110">However, third-party developers can create, install, and register their applications to handle the search protocol and to be the default search application.</span></span> <span data-ttu-id="3300f-111">Solche Anwendungen müssen die Syntax des Suchprotokolls unterstützen und sich mit dem [Standardprogramm für Programme](default-programs.md) registrieren, um eine nahtlose Windows-Funktionalität zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="3300f-111">Such applications need to support the search protocol syntax and register with the [Default Programs](default-programs.md) feature to ensure a seamless experience with Windows.</span></span>

<span data-ttu-id="3300f-112">Wenn Sie eine Anwendung entwickeln, die für eine bestimmte Desktop Suchanwendung verwendet oder erstellt werden soll, sollten Sie sich nicht ausschließlich auf das **Search:** -Protokoll verlassen.</span><span class="sxs-lookup"><span data-stu-id="3300f-112">If you develop an application that is intended to use or build upon a specific desktop search application, you should not depend exclusively on the **search:** protocol.</span></span> <span data-ttu-id="3300f-113">Da viele Anwendungen das **Search:** -Protokoll besitzen könnten, gibt es keine Garantie dafür, dass die Zielanwendung für die Desktop Suche Sie zu einem beliebigen Zeitpunkt übernimmt.</span><span class="sxs-lookup"><span data-stu-id="3300f-113">Because many applications could own the **search:** protocol, there is no guarantee that your targeted desktop search application will own it at any given time.</span></span> <span data-ttu-id="3300f-114">Stattdessen sollten Sie ein privates Such Protokoll verwenden, das von der Zielanwendung für die Desktop Suche definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3300f-114">Instead, you should use a private search protocol defined by that targeted desktop search application.</span></span> <span data-ttu-id="3300f-115">Dies bedeutet, dass Desktop Suchanwendungen, die als Plattform für Anwendungen von Drittanbietern gedacht sind, sowohl das **Search:** -Protokoll als auch das eigene proprietäre Such Protokoll unterstützen sollten.</span><span class="sxs-lookup"><span data-stu-id="3300f-115">This means that desktop search applications intended to be a platform for third-party applications should support both the **search:** protocol and their own proprietary search protocol.</span></span>

> [!Note]  
> <span data-ttu-id="3300f-116">Das **Search:** -Protokoll ersetzt nicht das proprietäre [Search-MS:-](../search/-search-3x-wds-qryidx-searchms.md) Protokoll.</span><span class="sxs-lookup"><span data-stu-id="3300f-116">The **search:** protocol does not replace the proprietary [search-ms:](../search/-search-3x-wds-qryidx-searchms.md) protocol.</span></span> <span data-ttu-id="3300f-117">Anwendungen können weiterhin das **Search-MS:-** Protokoll verwenden, um den Fenster Such-Explorer zu starten oder den Windows Search-Indexer automatisch abzufragen.</span><span class="sxs-lookup"><span data-stu-id="3300f-117">Applications can still use the **search-ms:** protocol to launch Window Search Explorer or to silently query the Windows Search indexer.</span></span>

 

<span data-ttu-id="3300f-118">In diesem Thema werden folgende Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="3300f-118">This topic covers the following:</span></span>

-   [<span data-ttu-id="3300f-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="3300f-119">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="3300f-120">Verwendung des Such Protokolls durch Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="3300f-120">Windows Vista with SP1 use of the search: protocol</span></span>](#windows-vista-with-sp1-use-of-the-search-protocol)
-   [<span data-ttu-id="3300f-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3300f-121">Examples</span></span>](#examples)
-   [<span data-ttu-id="3300f-122">Registrieren der Anwendung, die das Protokoll verarbeitet</span><span class="sxs-lookup"><span data-stu-id="3300f-122">Registering the Application that Handles the Protocol</span></span>](#registering-the-application-that-handles-the-protocol)
    -   [<span data-ttu-id="3300f-123">Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="3300f-123">Registry Entries</span></span>](#registry-entries)
-   [<span data-ttu-id="3300f-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3300f-124">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="3300f-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="3300f-125">Syntax</span></span>

<span data-ttu-id="3300f-126">Das Such Protokoll verwendet die folgende standardmäßige URL-codierte Syntax:</span><span class="sxs-lookup"><span data-stu-id="3300f-126">The search protocol uses the following standard URL-encoded syntax:</span></span>


```C++
search:parameter=value[&parameter=value]&
```



<span data-ttu-id="3300f-127">Die Syntax beginnt mit der Identifizierung des Protokolls selbst (**Search:**).</span><span class="sxs-lookup"><span data-stu-id="3300f-127">The syntax begins by identifying the protocol itself (**search:**).</span></span> <span data-ttu-id="3300f-128">Die Parameter/Wert-Paare sind Argumente, die an die Such-Engine übergeben werden, wie in der folgenden Tabelle beschrieben, in der alle möglichen Parameter für die Syntax des Suchprotokolls angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3300f-128">The parameter/value pairs are arguments passed to the Search engine, as described in the following table, which shows all of the possible parameters for the search protocol syntax.</span></span>



| <span data-ttu-id="3300f-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="3300f-129">Parameter</span></span>                                              | <span data-ttu-id="3300f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="3300f-130">Value</span></span>                                                         | <span data-ttu-id="3300f-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3300f-131">Description</span></span>                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3300f-132">Abfrage</span><span class="sxs-lookup"><span data-stu-id="3300f-132">query</span></span>                                                  | <span data-ttu-id="3300f-133">URL-codierter Text</span><span class="sxs-lookup"><span data-stu-id="3300f-133">URL-encoded text</span></span>                                              | <span data-ttu-id="3300f-134">Der vom Benutzer eingegebene Abfragetext.</span><span class="sxs-lookup"><span data-stu-id="3300f-134">The query text entered by the user.</span></span>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="3300f-135">InputLocale</span><span class="sxs-lookup"><span data-stu-id="3300f-135">inputlocale</span></span>](search-protocol-localeidentifiers.md)   | <span data-ttu-id="3300f-136">Beliebiger gültiger Sprachcode Bezeichner (LCID)</span><span class="sxs-lookup"><span data-stu-id="3300f-136">Any valid language code identifier (LCID)</span></span>                     | <span data-ttu-id="3300f-137">Die LCID, die die Eingabe Sprache für die Abfrage identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3300f-137">The LCID that identifies the input language for the query.</span></span>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="3300f-138">keywordlocale</span><span class="sxs-lookup"><span data-stu-id="3300f-138">keywordlocale</span></span>](search-protocol-localeidentifiers.md) | <span data-ttu-id="3300f-139">Eine beliebige gültige LCID</span><span class="sxs-lookup"><span data-stu-id="3300f-139">Any valid LCID</span></span>                                                | <span data-ttu-id="3300f-140">Die LCID, die die Sprache der internationalen Version des Indexers identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3300f-140">The LCID that identifies the language of the international version of the Indexer.</span></span> <span data-ttu-id="3300f-141">Der Standardwert ist 1033 (en-US).</span><span class="sxs-lookup"><span data-stu-id="3300f-141">The default is 1033 (en-us).</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="3300f-142">Breadcrumb)</span><span class="sxs-lookup"><span data-stu-id="3300f-142">crumb</span></span>](search-protocol-crumb.md)                     | <span data-ttu-id="3300f-143">AQS-Anweisung</span><span class="sxs-lookup"><span data-stu-id="3300f-143">AQS statement</span></span>                                                 | <span data-ttu-id="3300f-144">Dieses Argument schränkt den Bereich ein, der durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="3300f-144">This argument restricts the scope being searched.</span></span> <span data-ttu-id="3300f-145">In Windows Vista unterstützt das Such Protokoll vollständige AQS und eine spezielle Implementierung für ein `location` Argument.</span><span class="sxs-lookup"><span data-stu-id="3300f-145">In Windows Vista, the search protocol supports full AQS as well as a special implementation for a `location` argument.</span></span> <span data-ttu-id="3300f-146">In Windows XP unterstützt das Such Protokoll auch vollständige AQS, mit Ausnahme einer speziellen Implementierung von `kind` und `store` .</span><span class="sxs-lookup"><span data-stu-id="3300f-146">In Windows XP, the search protocol also supports full AQS, except for a special implementation of `kind` and `store`.</span></span> |
| [<span data-ttu-id="3300f-147">Syntax</span><span class="sxs-lookup"><span data-stu-id="3300f-147">syntax</span></span>](search-protocol-syntaxargument.md)           | <span data-ttu-id="3300f-148">NQS, AQS (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="3300f-148">NQS, AQS (not case sensitive)</span></span>                                 | <span data-ttu-id="3300f-149">Die Abfrage Syntax, die zum Durchsuchen des Indexes verwendet werden soll: entweder natürliche Abfrage Syntax oder Erweiterte Abfrage Syntax (AQS).</span><span class="sxs-lookup"><span data-stu-id="3300f-149">The query syntax to use to search the index: either Natural Query Syntax or Advanced Query Syntax (AQS).</span></span> <span data-ttu-id="3300f-150">AQS ist die Standardeinstellung und wird immer als analysiert und unterstützt angenommen.</span><span class="sxs-lookup"><span data-stu-id="3300f-150">AQS is the default and is always assumed parsed and supported.</span></span>                                                                                                                        |
| [<span data-ttu-id="3300f-151">stackedby</span><span class="sxs-lookup"><span data-stu-id="3300f-151">stackedby</span></span>](search-protocol-stackedby.md)             | <span data-ttu-id="3300f-152">Eine beliebige gültige Eigenschaft aus dem Eigenschaften System.</span><span class="sxs-lookup"><span data-stu-id="3300f-152">Any valid property from the property system</span></span>                   | <span data-ttu-id="3300f-153">Eine-Eigenschaft, die die Spalte angibt, nach der die Ergebnisse gestapelt werden.</span><span class="sxs-lookup"><span data-stu-id="3300f-153">A property that specifies the column to stack results by.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="3300f-154">subquery</span><span class="sxs-lookup"><span data-stu-id="3300f-154">subquery</span></span>](search-protocol-subquery.md)               | <span data-ttu-id="3300f-155">Ein vollständig angegebener Pfad für eine gespeicherte Suchdatei ( \* . Search-MS)</span><span class="sxs-lookup"><span data-stu-id="3300f-155">A fully specified path for a Saved Search file (\*.search-ms)</span></span> | <span data-ttu-id="3300f-156">Die Ergebnisse der Unterabfrage werden als Quelle für die Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="3300f-156">The results of the subquery are used as the source for the query.</span></span> <span data-ttu-id="3300f-157">Das heißt, dass die Abfrage Begriffe anhand der Ergebnisse der Unterabfrage gesucht werden.</span><span class="sxs-lookup"><span data-stu-id="3300f-157">That is, the query terms are searched for against the results of the subquery.</span></span>                                                                                                                                               |
| <span data-ttu-id="3300f-158">displayname</span><span class="sxs-lookup"><span data-stu-id="3300f-158">displayname</span></span>                                            | <span data-ttu-id="3300f-159">URL-codierte Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3300f-159">URL-encoded string</span></span>                                            | <span data-ttu-id="3300f-160">Der Name der aktuellen Suche.</span><span class="sxs-lookup"><span data-stu-id="3300f-160">The name of the current search.</span></span>                                                                                                                                                                                                                                                                |



 

## <a name="windows-vista-with-sp1-use-of-the-search-protocol"></a><span data-ttu-id="3300f-161">Verwendung des Such Protokolls durch Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="3300f-161">Windows Vista with SP1 use of the search: protocol</span></span>

<span data-ttu-id="3300f-162">Windows Vista mit SP1 verfügt über mehrere Einstiegspunkte, von denen das **Such** Protokoll aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3300f-162">Windows Vista with SP1 has several entry points from which it calls the **search:** protocol.</span></span> <span data-ttu-id="3300f-163">Diese Einstiegspunkte sind unten und die jeweils zugeordnete allgemeine Syntax aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3300f-163">These entry points are outlined below as well as the common syntax associated with each.</span></span>



| <span data-ttu-id="3300f-164">Such Protokoll-Einstiegspunkt</span><span class="sxs-lookup"><span data-stu-id="3300f-164">Search protocol entry point</span></span> | <span data-ttu-id="3300f-165">Standort</span><span class="sxs-lookup"><span data-stu-id="3300f-165">Location</span></span>         | <span data-ttu-id="3300f-166">Abfrage aufgerufen</span><span class="sxs-lookup"><span data-stu-id="3300f-166">Query called</span></span>                                                         |
|-----------------------------|------------------|----------------------------------------------------------------------|
| <span data-ttu-id="3300f-167">**Überall suchen**</span><span class="sxs-lookup"><span data-stu-id="3300f-167">**Search Everywhere**</span></span>       | <span data-ttu-id="3300f-168">**Startmenü**</span><span class="sxs-lookup"><span data-stu-id="3300f-168">**Start** menu</span></span>   | <span data-ttu-id="3300f-169">Search: Query =<*Suchbegriff*></span><span class="sxs-lookup"><span data-stu-id="3300f-169">search:query=<*Search Term*></span></span>                                   |
| <span data-ttu-id="3300f-170">**Überall suchen**</span><span class="sxs-lookup"><span data-stu-id="3300f-170">**Search Everywhere**</span></span>       | <span data-ttu-id="3300f-171">Windows-Explorer</span><span class="sxs-lookup"><span data-stu-id="3300f-171">Windows Explorer</span></span> | <span data-ttu-id="3300f-172">Suche: Abfrage =<*Suchbegriff*>&Crumb = Speicherort: <*Speicherort*></span><span class="sxs-lookup"><span data-stu-id="3300f-172">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |
| <span data-ttu-id="3300f-173">WINDOWS-TASTE+F</span><span class="sxs-lookup"><span data-stu-id="3300f-173">Windows logo key+F</span></span>          | <span data-ttu-id="3300f-174">Überall</span><span class="sxs-lookup"><span data-stu-id="3300f-174">Anywhere</span></span>         | <span data-ttu-id="3300f-175">Such</span><span class="sxs-lookup"><span data-stu-id="3300f-175">search:</span></span>                                                              |
| <span data-ttu-id="3300f-176">STRG+F</span><span class="sxs-lookup"><span data-stu-id="3300f-176">CTRL+F</span></span>                      | <span data-ttu-id="3300f-177">Windows-Explorer</span><span class="sxs-lookup"><span data-stu-id="3300f-177">Windows Explorer</span></span> | <span data-ttu-id="3300f-178">Suche: Abfrage =<*Suchbegriff*>&Crumb = Speicherort: <*Speicherort*></span><span class="sxs-lookup"><span data-stu-id="3300f-178">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |
| <span data-ttu-id="3300f-179">F3</span><span class="sxs-lookup"><span data-stu-id="3300f-179">F3</span></span>                          | <span data-ttu-id="3300f-180">**Startmenü**</span><span class="sxs-lookup"><span data-stu-id="3300f-180">**Start** menu</span></span>   | <span data-ttu-id="3300f-181">Such</span><span class="sxs-lookup"><span data-stu-id="3300f-181">search:</span></span>                                                              |
| <span data-ttu-id="3300f-182">F3</span><span class="sxs-lookup"><span data-stu-id="3300f-182">F3</span></span>                          | <span data-ttu-id="3300f-183">Windows-Explorer</span><span class="sxs-lookup"><span data-stu-id="3300f-183">Windows Explorer</span></span> | <span data-ttu-id="3300f-184">Suche: Abfrage =<*Suchbegriff*>&Crumb = Speicherort: <*Speicherort*></span><span class="sxs-lookup"><span data-stu-id="3300f-184">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |



 

<span data-ttu-id="3300f-185">Die Einstiegspunkte des Suchprotokolls von Windows Vista mit SP1 nutzen nicht alle möglichen Parameter im Such Protokoll.</span><span class="sxs-lookup"><span data-stu-id="3300f-185">The Windows Vista with SP1 search protocol entry points do not take advantage of all the possible parameters in the search protocol.</span></span> <span data-ttu-id="3300f-186">Anwendungen, die sich nur mit der Handhabung von Such Protokoll aufrufen von Windows Vista mit SP1 befassen, können die folgende Tabelle als Leitfaden für die Mindestanforderungen verwenden, die für die Implementierung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3300f-186">Applications that are only concerned with handling search protocol calls from Windows Vista with SP1 can use the following table as a guide to the minimum they need to implement.</span></span>



| <span data-ttu-id="3300f-187">Parameter</span><span class="sxs-lookup"><span data-stu-id="3300f-187">Parameter</span></span>                                              | <span data-ttu-id="3300f-188">Von Windows verwendet?</span><span class="sxs-lookup"><span data-stu-id="3300f-188">Used by Windows?</span></span> | <span data-ttu-id="3300f-189">Verwendung durch Windows Vista mit SP1 beim Aufrufen der Suche:</span><span class="sxs-lookup"><span data-stu-id="3300f-189">How Windows Vista with SP1 uses it when calling search:</span></span>                                                                                                                                                                                                                     |
|--------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3300f-190">Abfrage</span><span class="sxs-lookup"><span data-stu-id="3300f-190">query</span></span>                                                  | <span data-ttu-id="3300f-191">Ja</span><span class="sxs-lookup"><span data-stu-id="3300f-191">Yes</span></span>              | <span data-ttu-id="3300f-192">Der vom Benutzer eingegebene Abfragetext.</span><span class="sxs-lookup"><span data-stu-id="3300f-192">The query text entered by the user.</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="3300f-193">Breadcrumb)</span><span class="sxs-lookup"><span data-stu-id="3300f-193">crumb</span></span>](search-protocol-crumb.md)                     | <span data-ttu-id="3300f-194">Ja</span><span class="sxs-lookup"><span data-stu-id="3300f-194">Yes</span></span>              | <span data-ttu-id="3300f-195">[Breadcrumb)](search-protocol-crumb.md) verwendet das- `location` Argument, um den Speicherort der Abfrage anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3300f-195">[crumb](search-protocol-crumb.md) uses the `location` argument to specify where the query came from.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="3300f-196">subquery</span><span class="sxs-lookup"><span data-stu-id="3300f-196">subquery</span></span>](search-protocol-subquery.md)               | <span data-ttu-id="3300f-197">Ja</span><span class="sxs-lookup"><span data-stu-id="3300f-197">Yes</span></span>              | <span data-ttu-id="3300f-198">Die Ergebnisse des [Unterabfrage](search-protocol-subquery.md) Arguments werden als Bereich der zu durchsuchenden Elemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="3300f-198">The results of the [Subquery](search-protocol-subquery.md) argument are used as the scope of items to search.</span></span> <span data-ttu-id="3300f-199">Dies wird normalerweise verwendet, wenn ein Benutzer eine. Search-MS-Datei verwendet hat, um die standardmäßige Desktop Suchanwendung in dieser Suche zu suchen und anschließend aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="3300f-199">This would typically be used if a user was using a .search-ms file to search and then called the default desktop search application from within that search.</span></span> |
| [<span data-ttu-id="3300f-200">InputLocale</span><span class="sxs-lookup"><span data-stu-id="3300f-200">inputlocale</span></span>](search-protocol-localeidentifiers.md)   | <span data-ttu-id="3300f-201">Nein</span><span class="sxs-lookup"><span data-stu-id="3300f-201">No</span></span>               | <span data-ttu-id="3300f-202">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3300f-202">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="3300f-203">keywordlocale</span><span class="sxs-lookup"><span data-stu-id="3300f-203">keywordlocale</span></span>](search-protocol-localeidentifiers.md) | <span data-ttu-id="3300f-204">Nein</span><span class="sxs-lookup"><span data-stu-id="3300f-204">No</span></span>               | <span data-ttu-id="3300f-205">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3300f-205">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="3300f-206">Syntax</span><span class="sxs-lookup"><span data-stu-id="3300f-206">syntax</span></span>](search-protocol-syntaxargument.md)           | <span data-ttu-id="3300f-207">Nein</span><span class="sxs-lookup"><span data-stu-id="3300f-207">No</span></span>               | <span data-ttu-id="3300f-208">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3300f-208">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="3300f-209">stackedby</span><span class="sxs-lookup"><span data-stu-id="3300f-209">stackedby</span></span>](search-protocol-stackedby.md)             | <span data-ttu-id="3300f-210">Nein</span><span class="sxs-lookup"><span data-stu-id="3300f-210">No</span></span>               | <span data-ttu-id="3300f-211">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3300f-211">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3300f-212">displayname</span><span class="sxs-lookup"><span data-stu-id="3300f-212">displayname</span></span>                                            | <span data-ttu-id="3300f-213">Nein</span><span class="sxs-lookup"><span data-stu-id="3300f-213">No</span></span>               | <span data-ttu-id="3300f-214">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3300f-214">Not currently used.</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="examples"></a><span data-ttu-id="3300f-215">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3300f-215">Examples</span></span>

<span data-ttu-id="3300f-216">Wenn ein Benutzer im **Startmenü** "Microsoft" eingibt und auf " **überall suchen**" klickt, wird der resultierende Such Protokoll Befehl durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="3300f-216">If a user enters "Microsoft" in the **Start** menu and clicks **Search Everywhere**, the resulting search protocol call is made:</span></span>


```C++
search:query=microsoft&
```



<span data-ttu-id="3300f-217">Wenn ein Benutzer "Seattle" in Windows-Explorer innerhalb von "C: MyFolder" eingibt \\ und dann auf " **überall suchen**" klickt, wird der folgende Befehl durchgeführt, wobei Escapezeichen für ":" und "" verwendet werden \\ :</span><span class="sxs-lookup"><span data-stu-id="3300f-217">If a user enters "Seattle" in Windows Explorer within C:\\MyFolder and then clicks **Search Everywhere**, the following call is made, using escape characters for ':' and '\\':</span></span>


```C++
search:query=seattle&crumb=location:C%3A%5CMyFolder
```



## <a name="registering-the-application-that-handles-the-protocol"></a><span data-ttu-id="3300f-218">Registrieren der Anwendung, die das Protokoll verarbeitet</span><span class="sxs-lookup"><span data-stu-id="3300f-218">Registering the Application that Handles the Protocol</span></span>

<span data-ttu-id="3300f-219">Da sich mehrere Anwendungen mit dem Such Protokoll auseinandersetzen können, sollten Sie Ihre Anwendung bei der Installation mit der [Standardprogramm](default-programs.md) Funktion registrieren, damit der Benutzer den Standardwert leichter konfigurieren kann.</span><span class="sxs-lookup"><span data-stu-id="3300f-219">Because multiple applications can contend for the search protocol, you should register your application with the [Default Programs](default-programs.md) feature during installation to enable the user to configure the default more easily.</span></span> <span data-ttu-id="3300f-220">Zusätzlich zu den Installations Prozeduren, die normalerweise unter Windows XP verwendet werden, muss eine auf Windows Vista basierende Anwendung mit der Standardprogramm Funktion registriert werden, damit die Anwendung und die Benutzer die Standardeinstellungen nahtlos konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="3300f-220">In addition to the installation procedures normally practiced under Windows XP, a Windows Vista-based application must register with the Default Programs feature so that the application and users can seamlessly configure defaults.</span></span>

<span data-ttu-id="3300f-221">Nachdem Sie die erforderlichen Binärdateien auf dem Computer des Benutzers installiert haben, sollte die Installationsroutine die folgenden allgemeinen Aufgaben erfüllen:</span><span class="sxs-lookup"><span data-stu-id="3300f-221">After installing the necessary binary files on the user's computer, your installation routine should complete these general tasks:</span></span>

1.  <span data-ttu-id="3300f-222">Schreiben Sie ProgIDs auf **\_ den lokalen \_ HKEY-Computer**, wie unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3300f-222">Write ProgIDs to **HKEY\_LOCAL\_MACHINE**, as described below.</span></span> <span data-ttu-id="3300f-223">Beachten Sie, dass Anwendungen anwendungsspezifische ProgIDs für das Such Protokoll erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="3300f-223">Note that applications must create application-specific ProgIDs for the search protocol.</span></span>
2.  <span data-ttu-id="3300f-224">Die Such Protokoll Zuordnung auf Computer Ebene anfordern.</span><span class="sxs-lookup"><span data-stu-id="3300f-224">Claim machine-level search protocol association.</span></span>
3.  <span data-ttu-id="3300f-225">Registrieren Sie die Anwendung bei [Standardprogrammen](default-programs.md)(wie unter [Registrieren einer Anwendung für die Verwendung mit Standardprogrammen](default-programs.md)erläutert) als Kandidat für das Such Protokoll.</span><span class="sxs-lookup"><span data-stu-id="3300f-225">Register the application with [Default Programs](default-programs.md), as explained in [Registering an Application for Use with Default Programs](default-programs.md), as a contender for the search protocol.</span></span>

### <a name="registry-entries"></a><span data-ttu-id="3300f-226">Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="3300f-226">Registry Entries</span></span>

<span data-ttu-id="3300f-227">Im folgenden finden Sie Beispiele für die erforderlichen Registrierungseinträge für eine fiktive Anwendung der Desktop Suche.</span><span class="sxs-lookup"><span data-stu-id="3300f-227">The following are examples of the required registry entries for a fictional desktop search application, Contoso Search.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            URL Protocol = ""
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            DefaultIcon
               (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe,-7
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe %1
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Contoso Search = "Software\\Contoso\\Search\\Capabilities"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               ApplicationName = "Contoso Search Test App"
               ApplicationDescription = "Contoso search is a great new desktop search application"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               UrlAssociations
                  search = "contoso-search"
```

## <a name="related-topics"></a><span data-ttu-id="3300f-228">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3300f-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3300f-229">Erweiterte Abfragesyntax</span><span class="sxs-lookup"><span data-stu-id="3300f-229">Advanced Query Syntax</span></span>](../search/-search-3x-advancedquerysyntax.md)
</dt> <dt>

[<span data-ttu-id="3300f-230">Standardprogramme</span><span class="sxs-lookup"><span data-stu-id="3300f-230">Default Programs</span></span>](default-programs.md)
</dt> </dl>

 

 
