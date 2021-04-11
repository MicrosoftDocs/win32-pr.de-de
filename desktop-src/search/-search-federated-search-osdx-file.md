---
description: Beschreibt, wie eine OpenSearch-Beschreibungsdatei (OSDX-Datei) erstellt wird, um externe Datenspeicher über das OpenSearch-Protokoll mit dem Windows-Client zu verbinden.
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406b166d6963517d692ef9de8292190d7eb92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958784"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a><span data-ttu-id="b2238-103">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="b2238-103">Creating an OpenSearch Description File in Windows Federated Search</span></span>

<span data-ttu-id="b2238-104">Beschreibt, wie eine OpenSearch-Beschreibungsdatei (OSDX-Datei) erstellt wird, um externe Datenspeicher über das [OpenSearch](https://github.com/dewitt/opensearch) -Protokoll mit dem Windows-Client zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="b2238-104">Describes how to create an OpenSearch Description (.osdx) file to connect external data stores to the Windows Client via the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="b2238-105">Mit der Verbund Suche können Benutzer einen Remote Datenspeicher durchsuchen und die Ergebnisse innerhalb von Windows-Explorer anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b2238-105">Federated search enables users to search a remote data store and view the results from within Windows Explorer.</span></span>

<span data-ttu-id="b2238-106">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="b2238-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b2238-107">OpenSearch-Beschreibungsdatei</span><span class="sxs-lookup"><span data-stu-id="b2238-107">OpenSearch Description File</span></span>](#opensearch-description-file)
    -   [<span data-ttu-id="b2238-108">Erforderliche untergeordnete Elemente für Mininum</span><span class="sxs-lookup"><span data-stu-id="b2238-108">Mininum Required Child Elements</span></span>](#mininum-required-child-elements)
-   [<span data-ttu-id="b2238-109">Standard Elemente in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="b2238-109">Standard Elements in Windows Federated Search</span></span>](#standard-elements-in-windows-federated-search)
    -   [<span data-ttu-id="b2238-110">Kurznamen</span><span class="sxs-lookup"><span data-stu-id="b2238-110">Shortname</span></span>](#shortname)
    -   [<span data-ttu-id="b2238-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2238-111">Description</span></span>](#description)
    -   [<span data-ttu-id="b2238-112">URL-Vorlage für RSS/Atom-Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="b2238-112">URL Template for RSS/Atom Results</span></span>](#url-template-for-rssatom-results)
    -   [<span data-ttu-id="b2238-113">URL-Vorlage für Webergebnisse</span><span class="sxs-lookup"><span data-stu-id="b2238-113">URL Template for web Results</span></span>](#url-template-for-web-results)
    -   [<span data-ttu-id="b2238-114">URL-Vorlagen Parameter</span><span class="sxs-lookup"><span data-stu-id="b2238-114">URL Template Parameters</span></span>](#url-template-parameters)
    -   [<span data-ttu-id="b2238-115">Auslagerbare Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="b2238-115">Paged Results</span></span>](#paged-results)
    -   [<span data-ttu-id="b2238-116">Paging mit dem Element Index</span><span class="sxs-lookup"><span data-stu-id="b2238-116">Paging Using the Item Index</span></span>](#paging-using-the-item-index)
    -   [<span data-ttu-id="b2238-117">Paging mit dem Seiten Index</span><span class="sxs-lookup"><span data-stu-id="b2238-117">Paging Using the Page Index</span></span>](#paging-using-the-page-index)
    -   [<span data-ttu-id="b2238-118">Seitengröße</span><span class="sxs-lookup"><span data-stu-id="b2238-118">Page Size</span></span>](#page-size)
-   [<span data-ttu-id="b2238-119">Erweiterte Elemente in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="b2238-119">Extended Elements in Windows Federated Search</span></span>](#extended-elements-in-windows-federated-search)
    -   [<span data-ttu-id="b2238-120">Maximale Ergebnis Anzahl</span><span class="sxs-lookup"><span data-stu-id="b2238-120">Maximum Result Count</span></span>](#maximum-result-count)
    -   [<span data-ttu-id="b2238-121">Eigenschaftszuordnung</span><span class="sxs-lookup"><span data-stu-id="b2238-121">Property Mapping</span></span>](#property-mapping)
-   [<span data-ttu-id="b2238-122">Vorschauen</span><span class="sxs-lookup"><span data-stu-id="b2238-122">Previews</span></span>](#previews)
-   [<span data-ttu-id="b2238-123">Menü Element "Datei Speicherort öffnen"</span><span class="sxs-lookup"><span data-stu-id="b2238-123">Open File Location Menu Item</span></span>](#open-file-location-menu-item)
-   [<span data-ttu-id="b2238-124">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b2238-124">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="b2238-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b2238-125">Related topics</span></span>](#related-topics)

## <a name="opensearch-description-file"></a><span data-ttu-id="b2238-126">OpenSearch-Beschreibungsdatei</span><span class="sxs-lookup"><span data-stu-id="b2238-126">OpenSearch Description File</span></span>

<span data-ttu-id="b2238-127">Eine OpenSearch-Beschreibungsdatei (OSDX-Datei) für die Windows-Verbund Suche muss die folgenden Regeln einhalten:</span><span class="sxs-lookup"><span data-stu-id="b2238-127">An OpenSearch Description (.osdx) file for Windows Federated Search must abide by the following rules:</span></span>

-   <span data-ttu-id="b2238-128">Ein gültiges OpenSearch-Beschreibungs Dokument, wie in der [OpenSearch](https://github.com/dewitt/opensearch) 1,1-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="b2238-128">Be a valid OpenSearch Description document, as defined by the [OpenSearch](https://github.com/dewitt/opensearch) 1.1 specification.</span></span>
-   <span data-ttu-id="b2238-129">Stellen Sie eine URL-Vorlage mit einem RSS-oder Atom-Formattyp bereit.</span><span class="sxs-lookup"><span data-stu-id="b2238-129">Provide a URL template with either an RSS or an Atom format type.</span></span>
-   <span data-ttu-id="b2238-130">Verwenden Sie die Dateinamenerweiterung. OSDX, oder lassen Sie sich beim Herunterladen aus dem Web mit der Dateinamenerweiterung. OSDX verknüpft.</span><span class="sxs-lookup"><span data-stu-id="b2238-130">Use the .osdx file name extension, or be associated with the .osdx file name extension when downloading from the web.</span></span> <span data-ttu-id="b2238-131">Beispielsweise ist es nicht erforderlich, dass ein Server. OSDX verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2238-131">For example, a server is not required to use .osdx.</span></span> <span data-ttu-id="b2238-132">Ein Server kann die Datei mit einer beliebigen Dateinamenerweiterung (z. b.. Xml) zurückgeben und so behandelt werden, als ob es sich um eine OSDX-Datei handelt, wenn Sie den richtigen MIME-Typ für OpenSearch-Beschreibungs Dokumente (OSDX-Dateien) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2238-132">A server can return the file with any file name extension, such as .xml for example, and treated as if it were an .osdx file if it uses the correct MIME Type for OpenSearch Description documents (.osdx files).</span></span>
-   <span data-ttu-id="b2238-133">Geben Sie einen Wert für das **Shortname** -Element an (empfohlen).</span><span class="sxs-lookup"><span data-stu-id="b2238-133">Provide a **ShortName** element value (recommended).</span></span>

### <a name="mininum-required-child-elements"></a><span data-ttu-id="b2238-134">Erforderliche untergeordnete Elemente für Mininum</span><span class="sxs-lookup"><span data-stu-id="b2238-134">Mininum Required Child Elements</span></span>

<span data-ttu-id="b2238-135">Die folgende OSDX-Beispieldatei besteht aus **Kurzname** und `Url` Elementen, bei denen es sich um die mindestens erforderlichen untergeordneten Elemente handelt.</span><span class="sxs-lookup"><span data-stu-id="b2238-135">The following example .osdx file consists of **ShortName** and `Url` elements, which are the minimum required child elements.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a><span data-ttu-id="b2238-136">Standard Elemente in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="b2238-136">Standard Elements in Windows Federated Search</span></span>

<span data-ttu-id="b2238-137">Zusätzlich zu den minimalen untergeordneten Elementen unterstützt die Verbund Suche die folgenden Standardelemente.</span><span class="sxs-lookup"><span data-stu-id="b2238-137">In addition to the minimum child elements, federated search supports the following standard elements.</span></span>

### <a name="shortname"></a><span data-ttu-id="b2238-138">Kurznamen</span><span class="sxs-lookup"><span data-stu-id="b2238-138">Shortname</span></span>

<span data-ttu-id="b2238-139">Windows verwendet den **Shortname** -Elementwert, um die Datei ". searchconnector-MS" (Suchconnector) zu benennen, die erstellt wird, wenn der Benutzer die OSDX-Datei öffnet.</span><span class="sxs-lookup"><span data-stu-id="b2238-139">Windows uses the **ShortName** element value to name the .searchconnector-ms (search connector) file that is created when the user opens the .osdx file.</span></span> <span data-ttu-id="b2238-140">Windows stellt sicher, dass für den generierten Dateinamen nur Zeichen verwendet werden, die in Windows-Dateinamen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b2238-140">Windows ensures that the generated file name uses only characters that are allowed in Windows file names.</span></span> <span data-ttu-id="b2238-141">Wenn kein **Shortname** -Wert angegeben wird, versucht die Datei ". searchconnector-MS" stattdessen, den Dateinamen der OSDX-Datei zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2238-141">If no **ShortName** value is provided, the .searchconnector-ms file tries to use the file name of the .osdx file instead.</span></span>

<span data-ttu-id="b2238-142">Der folgende Code veranschaulicht, wie das **Shortname** -Element in einer OSDX-Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2238-142">The following code illustrates how to use the **ShortName** element in an .osdx file.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a><span data-ttu-id="b2238-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2238-143">Description</span></span>

<span data-ttu-id="b2238-144">Windows verwendet den Wert **Description** -Element, um die im Detailbereich von Windows-Explorer angezeigte Dateibeschreibung aufzufüllen, wenn ein Benutzer eine searchconnector-MS-Datei auswählt.</span><span class="sxs-lookup"><span data-stu-id="b2238-144">Windows uses the **Description** element value to populate the file description shown in the Windows Explorer details pane when a user selects a .searchconnector-ms file.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a><span data-ttu-id="b2238-145">URL-Vorlage für RSS/Atom-Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="b2238-145">URL Template for RSS/Atom Results</span></span>

<span data-ttu-id="b2238-146">Die OSDX-Datei muss ein **URL-Format** Element und ein **Vorlagen** Attribut (eine URL-Vorlage) enthalten, das Ergebnisse im RSS-oder Atom-Format zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b2238-146">The .osdx file must include one **Url format** element and **template** attribute (a URL template) that returns results in either RSS or Atom format.</span></span> <span data-ttu-id="b2238-147">Das Format-Attribut muss `application/rss+xml` für RSS-formatierte Ergebnisse oder `application/atom+xml` für Atom-formatierte Ergebnisse auf festgelegt werden, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2238-147">The format attribute must be set to `application/rss+xml` for RSS formatted results, or `application/atom+xml` for Atom formatted results, as shown in the following code.</span></span>

> [!Note]  
> <span data-ttu-id="b2238-148">Das **URL-Format** Element und das **Vorlagen** Attribut werden häufig als URL-Vorlage bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b2238-148">The **Url format** element and **template** attribute are commonly known as a URL template.</span></span>

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a><span data-ttu-id="b2238-149">URL-Vorlage für Webergebnisse</span><span class="sxs-lookup"><span data-stu-id="b2238-149">URL Template for web Results</span></span>

<span data-ttu-id="b2238-150">Wenn eine Version der Suchergebnisse vorhanden ist, die in einem Webbrowser angezeigt werden kann, sollten Sie ein URL- **Format =** `text/html` Element und ein **Vorlagen** Attribut angeben, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2238-150">If there is a version of the search results that can be viewed in a web browser, you should provide a **Url format=**`text/html` element, and **template** attribute, as shown in the following code.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



<span data-ttu-id="b2238-151">Wenn Sie ein **URL-Format = "Text/HTML"** -Element und ein **Vorlagen** Attribut angeben, wird in der Windows-Explorer-Befehlsleiste eine Schaltfläche angezeigt, die dem Benutzer ermöglicht, einen Webbrowser zu öffnen, um die Suchergebnisse anzuzeigen, wenn der Benutzer eine Abfrage ausführt.</span><span class="sxs-lookup"><span data-stu-id="b2238-151">If you provide a **Url format="text/html"** element and **template** attribute, a button appears in the Windows Explorer command bar, as shown in the following screen shot, that enables the user to open a web browser to view the search results when the user performs a query.</span></span>

![Screenshot der websuchschaltfläche.](images/websearchroll-overcommandbarbutton.png)

<span data-ttu-id="b2238-153">Das Rollback der Abfrage an die Webbenutzer Oberfläche des Daten Stores ist in einigen Szenarien wichtig.</span><span class="sxs-lookup"><span data-stu-id="b2238-153">The roll-over of the query back to the data store's web UI is important in some scenarios.</span></span> <span data-ttu-id="b2238-154">Beispielsweise kann ein Benutzer mehr als 100 Ergebnisse anzeigen (die Standard Anzahl der Elemente, die der OpenSearch-Anbieter anfordert).</span><span class="sxs-lookup"><span data-stu-id="b2238-154">For example, a user may want to view more than 100 results (the default number of items the OpenSearch provider requests).</span></span> <span data-ttu-id="b2238-155">Wenn dies der Fall ist, kann der Benutzer auch Suchfunktionen verwenden, die nur auf der Website des Daten Stores verfügbar sind, wie z. b. das erneute Abfragen mit einer anderen Sortierreihenfolge oder das pivotieren und Filtern der Abfrage mit zugehörigen Metadaten.</span><span class="sxs-lookup"><span data-stu-id="b2238-155">If so, the user may also want to use search features that are available only on the data store's website, such as re-querying with a different sort order, or pivoting and filtering the query with related metadata.</span></span>

### <a name="url-template-parameters"></a><span data-ttu-id="b2238-156">URL-Vorlagen Parameter</span><span class="sxs-lookup"><span data-stu-id="b2238-156">URL Template Parameters</span></span>

<span data-ttu-id="b2238-157">Der OpenSearch-Anbieter führt immer die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="b2238-157">The OpenSearch provider performs always the following actions:</span></span>

1.  <span data-ttu-id="b2238-158">Verwendet die URL-Vorlage, um die Anforderung an den Webdienst zu senden.</span><span class="sxs-lookup"><span data-stu-id="b2238-158">Uses the URL template to send the request to the web service.</span></span>
2.  <span data-ttu-id="b2238-159">Versucht, die in der URL-Vorlage gefundenen Token vor dem Senden der Anforderung an den Webdienst wie folgt zu ersetzen:</span><span class="sxs-lookup"><span data-stu-id="b2238-159">Attempts to replace the tokens found in the URL template before sending the request to the web service, as follows:</span></span>
    -   <span data-ttu-id="b2238-160">Ersetzt die in der folgenden Tabelle aufgeführten OpenSearch-Standard Token.</span><span class="sxs-lookup"><span data-stu-id="b2238-160">Replaces the standard OpenSearch tokens that are listed in the following table.</span></span>
    -   <span data-ttu-id="b2238-161">Entfernt alle Token, die nicht in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b2238-161">Removes any tokens that are not listed in the following table.</span></span>



| <span data-ttu-id="b2238-162">Unterstütztes Token</span><span class="sxs-lookup"><span data-stu-id="b2238-162">Supported token</span></span>  | <span data-ttu-id="b2238-163">Verwendung durch den OpenSearch-Anbieter</span><span class="sxs-lookup"><span data-stu-id="b2238-163">How used by OpenSearch provider</span></span>                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2238-164">{searchTerms}</span><span class="sxs-lookup"><span data-stu-id="b2238-164">{searchTerms}</span></span>    | <span data-ttu-id="b2238-165">Ersetzt durch die Suchbegriffe, die vom Benutzer in das Eingabefeld für die Windows-Explorer-Suche eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b2238-165">Replaced with the search terms that the user types in the Windows Explorer search input box.</span></span><br/>                                         |
| <span data-ttu-id="b2238-166">Start Index</span><span class="sxs-lookup"><span data-stu-id="b2238-166">{startIndex}</span></span>     | <span data-ttu-id="b2238-167">Wird verwendet, wenn Ergebnisse in "Pages" erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="b2238-167">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="b2238-168">Ersetzt durch den Index für das erste Ergebnis Element, das zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2238-168">Replaced with the index for the first result item to return.</span></span><br/>                        |
| <span data-ttu-id="b2238-169">Startpage</span><span class="sxs-lookup"><span data-stu-id="b2238-169">{startPage}</span></span>      | <span data-ttu-id="b2238-170">Wird verwendet, wenn Ergebnisse in "Pages" erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="b2238-170">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="b2238-171">Ersetzt durch die Seitenzahl der zurück zugebende Anzahl von Suchergebnissen.</span><span class="sxs-lookup"><span data-stu-id="b2238-171">Replaced with the page number of the set of search results to return.</span></span><br/>               |
| <span data-ttu-id="b2238-172">Countdown</span><span class="sxs-lookup"><span data-stu-id="b2238-172">{count}</span></span>          | <span data-ttu-id="b2238-173">Wird verwendet, wenn Ergebnisse in "Pages" erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="b2238-173">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="b2238-174">Wird durch die Anzahl der Suchergebnisse pro Seite ersetzt, die Windows-Explorer anfordert.</span><span class="sxs-lookup"><span data-stu-id="b2238-174">Replaced with the number of search results per page that Windows Explorer requests.</span></span><br/> |
| <span data-ttu-id="b2238-175">Kurse</span><span class="sxs-lookup"><span data-stu-id="b2238-175">{language}</span></span>       | <span data-ttu-id="b2238-176">Wird durch eine Zeichenfolge ersetzt, die die Sprache der gesendeten Abfrage angibt.</span><span class="sxs-lookup"><span data-stu-id="b2238-176">Replaced with a string that indicates the language of the query being sent.</span></span><br/>                                                          |
| <span data-ttu-id="b2238-177">{InputEncoding}</span><span class="sxs-lookup"><span data-stu-id="b2238-177">{inputEncoding}</span></span>  | <span data-ttu-id="b2238-178">Ersetzt durch eine Zeichenfolge (z. b. UTF-16), die die Zeichencodierung der gesendeten Abfrage angibt.</span><span class="sxs-lookup"><span data-stu-id="b2238-178">Replaced with a string (such "UTF-16") that indicates the character encoding of the query being sent.</span></span><br/>                                |
| <span data-ttu-id="b2238-179">outputEncoding</span><span class="sxs-lookup"><span data-stu-id="b2238-179">{outputEncoding}</span></span> | <span data-ttu-id="b2238-180">Ersetzt durch eine Zeichenfolge (z. b. "UTF-16"), die die gewünschte Zeichencodierung für die Antwort des Webdiensts angibt.</span><span class="sxs-lookup"><span data-stu-id="b2238-180">Replaced with a string (such as "UTF-16") that indicates the desired character encoding for the response from the web service.</span></span><br/>       |



 

### <a name="paged-results"></a><span data-ttu-id="b2238-181">Auslagerbare Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="b2238-181">Paged Results</span></span>

<span data-ttu-id="b2238-182">Möglicherweise möchten Sie die Anzahl der pro Anforderung zurückgegebenen Ergebnisse einschränken.</span><span class="sxs-lookup"><span data-stu-id="b2238-182">You may want to limit the number of results returned per request.</span></span> <span data-ttu-id="b2238-183">Sie können eine "Seite" der Ergebnisse gleichzeitig zurückgeben oder festlegen, dass der OpenSearch-Anbieter zusätzliche Ergebnis Ergebnisse entweder nach Element Nummer oder Seitenzahl erhält.</span><span class="sxs-lookup"><span data-stu-id="b2238-183">You can opt to return a "page" of results at a time, or to have the OpenSearch provider get additional pages of results either by item number or page number.</span></span> <span data-ttu-id="b2238-184">Wenn Sie z. b. 20 Ergebnisse pro Seite senden, beginnt die erste gesendete Seite an Element Index 1 und auf Seite 1. die zweite Seite, die Sie senden, beginnt an Element Index 21 und auf Seite 2.</span><span class="sxs-lookup"><span data-stu-id="b2238-184">For example, if you send twenty results per page, the first page you send starts at item index 1 and at page 1; the second page you send starts at item index 21 and at page 2.</span></span> <span data-ttu-id="b2238-185">Sie können definieren, wie der OpenSearch-Anbieter Elemente anfordern soll, indem Sie entweder das- `{startItem}` oder das- `{startPage}` Token in der URL-Vorlage verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2238-185">You can define how you want the OpenSearch provider to request items by using either the `{startItem}` or the `{startPage}` token in the URL template.</span></span>

### <a name="paging-using-the-item-index"></a><span data-ttu-id="b2238-186">Paging mit dem Element Index</span><span class="sxs-lookup"><span data-stu-id="b2238-186">Paging Using the Item Index</span></span>

<span data-ttu-id="b2238-187">Ein Element Index identifiziert das erste Ergebnis Element auf einer Seite mit Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="b2238-187">An item index identifies the first result item in a page of results.</span></span> <span data-ttu-id="b2238-188">Wenn Sie möchten, dass Clients Anforderungen mithilfe eines Element Indexes senden, können Sie das `{startIndex}` Token in Ihrem **URL** -Element **Vorlagen** Attribut verwenden, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2238-188">If you want clients to send requests using an item index, you can use the `{startIndex}` token in your **Url** element **template** attribute, as shown in the following code.</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



<span data-ttu-id="b2238-189">Der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter ersetzt dann das Token in der URL durch einen Start Index Wert.</span><span class="sxs-lookup"><span data-stu-id="b2238-189">The [OpenSearch](https://github.com/dewitt/opensearch) provider then replaces the token in the URL with a starting index value.</span></span> <span data-ttu-id="b2238-190">Die erste Anforderung beginnt mit dem ersten Element, wie im folgenden Beispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="b2238-190">The first request starts with the first item, as illustrated in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&start=1
```



<span data-ttu-id="b2238-191">Der OpenSearch-Anbieter kann weitere Elemente erhalten, indem er den `{startIndex}` Parameterwert ändert und eine neue Anforderung ausgibt.</span><span class="sxs-lookup"><span data-stu-id="b2238-191">The OpenSearch provider can get additional items by changing the `{startIndex}` parameter value and issuing a new request.</span></span> <span data-ttu-id="b2238-192">Der Anbieter wiederholt diesen Prozess, bis er genügend Ergebnisse zum erfüllen seines Limits erhält oder das Ende der Ergebnisse erreicht.</span><span class="sxs-lookup"><span data-stu-id="b2238-192">The provider repeats this process until it gets enough results to satisfy its limit, or reaches the end of the results.</span></span> <span data-ttu-id="b2238-193">Der OpenSearch-Anbieter prüft die Anzahl der Elemente, die vom Webdienst auf der ersten Seite der Ergebnisse zurückgegeben werden, und legt die erwartete Seitengröße auf diese Zahl fest.</span><span class="sxs-lookup"><span data-stu-id="b2238-193">The OpenSearch provider looks at the number of items returned by the web service in the first page of results, and sets the expected page size to that number.</span></span> <span data-ttu-id="b2238-194">Diese Zahl wird verwendet, um den `{startIndex}` Wert für nachfolgende Anforderungen zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="b2238-194">It uses that number to increment the `{startIndex}` value for subsequent requests.</span></span> <span data-ttu-id="b2238-195">Wenn der Webdienst z. b. 20 Ergebnisse in der ersten Anforderung zurückgibt, legt der Anbieter die erwartete Seitengröße auf 20 fest.</span><span class="sxs-lookup"><span data-stu-id="b2238-195">For example, if the web service returns 20 results in the first request, then the provider sets the expected page size to 20.</span></span> <span data-ttu-id="b2238-196">Bei der nächsten Anforderung ersetzt der Anbieter `{startIndex}` durch den Wert 21, um die nächsten 20 Elemente zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b2238-196">For the next request, the provider replaces `{startIndex}` with the value of 21 to get the next 20 items.</span></span>

> [!Note]  
> <span data-ttu-id="b2238-197">Wenn eine vom Webdienst zurückgegebene Ergebnisseite weniger Elemente aufweist als die erwartete Seitengröße, geht der OpenSearch-Anbieter davon aus, dass er die letzte Seite der Ergebnisse empfangen hat, und hält keine Anforderungen mehr an.</span><span class="sxs-lookup"><span data-stu-id="b2238-197">If a page of results returned by the web service has fewer items than the expected page size, then the OpenSearch provider assumes it has received the last page of results and stops making requests.</span></span>

 

### <a name="paging-using-the-page-index"></a><span data-ttu-id="b2238-198">Paging mit dem Seiten Index</span><span class="sxs-lookup"><span data-stu-id="b2238-198">Paging Using the Page Index</span></span>

<span data-ttu-id="b2238-199">Ein Seitenindex identifiziert die angegebene Seite der Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="b2238-199">A page index identifies the specified page of results.</span></span> <span data-ttu-id="b2238-200">Wenn Sie möchten, dass Clients Anforderungen mithilfe einer Seitenzahl senden, können Sie das `{startPage}` Token in Ihrem **URL-Format** Element **Template** -Attribut verwenden, um anzugeben, wie im folgenden Beispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="b2238-200">If you want clients to send requests using a page number, you can use the `{startPage}` token in your **Url format** element **template** attribute to indicate that, as illustrated in the following example:</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



<span data-ttu-id="b2238-201">Der OpenSearch-Anbieter ersetzt dann das Token in der URL durch einen page number-Parameter.</span><span class="sxs-lookup"><span data-stu-id="b2238-201">The OpenSearch provider then replaces the token in the URL with a page number parameter.</span></span> <span data-ttu-id="b2238-202">Die erste Anforderung beginnt mit der ersten Seite, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="b2238-202">The first request starts with the first page, as shown in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> <span data-ttu-id="b2238-203">Wenn eine vom Webdienst zurückgegebene Ergebnisseite weniger Elemente aufweist als die erwartete Seitengröße, geht der OpenSearch-Anbieter davon aus, dass er die letzte Seite der Ergebnisse empfangen hat, und hält keine Anforderungen mehr an.</span><span class="sxs-lookup"><span data-stu-id="b2238-203">If a page of results returned by the web service has fewer items than the expected page size, then the OpenSearch provider assumes it has received the last page of results and stops making requests.</span></span>

 

### <a name="page-size"></a><span data-ttu-id="b2238-204">Page Size</span><span class="sxs-lookup"><span data-stu-id="b2238-204">Page Size</span></span>

<span data-ttu-id="b2238-205">Möglicherweise möchten Sie den Webdienst so konfigurieren, dass eine Anforderung zum Angeben der Größe der Seiten mithilfe eines Parameters in der URL zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="b2238-205">You may want to configure your web service to permit a request to specify the size of the pages by using some parameter in the URL.</span></span> <span data-ttu-id="b2238-206">Eine Anforderung muss in der OSDX-Datei angegeben werden, indem das `{count}` Token wie folgt verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="b2238-206">A request must be specified in the .osdx file by using the `{count}` token, as follows:</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



<span data-ttu-id="b2238-207">Der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter kann dann die gewünschte Seitengröße in Anzahl der Ergebnisse pro Seite festlegen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="b2238-207">The [OpenSearch](https://github.com/dewitt/opensearch) provider can then set the desired page size, in number of results per page, as shown in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



<span data-ttu-id="b2238-208">Standardmäßig stellt der OpenSearch-Anbieter Anforderungen mithilfe einer Seitengröße von 50.</span><span class="sxs-lookup"><span data-stu-id="b2238-208">By default the OpenSearch provider makes requests using a page size of 50.</span></span> <span data-ttu-id="b2238-209">Wenn Sie eine andere Seitengröße wünschen, geben Sie kein `{count}` Token an, und platzieren Sie die gewünschte Zahl stattdessen direkt im **URL-Vorlagen** Element.</span><span class="sxs-lookup"><span data-stu-id="b2238-209">If you want a different page size, then do not provide a `{count}` token, and instead place the desired number directly in the **Url template** element.</span></span>

<span data-ttu-id="b2238-210">Der OpenSearch-Anbieter bestimmt die Seitengröße basierend auf der Anzahl der Ergebnisse, die bei der ersten Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b2238-210">The OpenSearch provider determines the page size based on the number of results returned on the first request.</span></span> <span data-ttu-id="b2238-211">Wenn die erste empfangene Ergebnisseite weniger Elemente enthält als die angeforderte Anzahl, setzt der Anbieter die Seitengröße für alle nachfolgenden Seiten Anforderungen zurück.</span><span class="sxs-lookup"><span data-stu-id="b2238-211">If the first page of results received has fewer items than the count requested, the provider resets the page size for any subsequent page requests.</span></span> <span data-ttu-id="b2238-212">Wenn nachfolgende Seiten Anforderungen weniger Elemente als angefordert zurückgeben, geht der OpenSearch-Anbieter davon aus, dass er das Ende der Ergebnisse erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="b2238-212">If subsequent page requests return fewer items than requested, the OpenSearch provider assumes that it has reached the end of the results.</span></span>

## <a name="extended-elements-in-windows-federated-search"></a><span data-ttu-id="b2238-213">Erweiterte Elemente in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="b2238-213">Extended Elements in Windows Federated Search</span></span>

<span data-ttu-id="b2238-214">Zusätzlich zu den Standardelementen unterstützt die Verbund Suche die folgenden erweiterten Elemente: **maximumresultcount** und **resultsprocessing.**</span><span class="sxs-lookup"><span data-stu-id="b2238-214">In addition to the standard elements, federated search supports the following extended elements: **MaximumResultCount** and **ResultsProcessing**.</span></span>

<span data-ttu-id="b2238-215">Da diese erweiterten untergeordneten Elemente in der [OpenSearch](https://github.com/dewitt/opensearch) v 1.1-Spezifikation nicht unterstützt werden, müssen Sie mithilfe des folgenden Namespace hinzugefügt werden:</span><span class="sxs-lookup"><span data-stu-id="b2238-215">Because these extended child elements are not supported in the [OpenSearch](https://github.com/dewitt/opensearch) v1.1 specification, they must be added by using the following namespace:</span></span>


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a><span data-ttu-id="b2238-216">Maximale Ergebnis Anzahl</span><span class="sxs-lookup"><span data-stu-id="b2238-216">Maximum Result Count</span></span>

<span data-ttu-id="b2238-217">Standardmäßig sind Suchconnectors auf 100-Ergebnisse pro Benutzer Abfrage beschränkt.</span><span class="sxs-lookup"><span data-stu-id="b2238-217">By default, search connectors are limited to 100 results per user query.</span></span> <span data-ttu-id="b2238-218">Diese Beschränkung kann angepasst werden, indem Sie das **maximumresultcount** -Element in die OSD-Datei einschließen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="b2238-218">This limit can be customized by including the **MaximumResultCount** element within the OSD file as shown in the following example:</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



<span data-ttu-id="b2238-219">Im vorangehenden Beispiel wird das Namespace Präfix `ms-ose` im **opensearchdescription** -Element der obersten Ebene deklariert und dann als Präfix im Elementnamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2238-219">The preceding example declares the namespace prefix `ms-ose` in the top-level **OpenSearchDescription** element, and then uses it as a prefix in the element name.</span></span> <span data-ttu-id="b2238-220">Diese Deklaration ist erforderlich, weil **maximumresultcount** in der [OpenSearch](https://github.com/dewitt/opensearch) v 1.1-Spezifikation nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b2238-220">This declaration is required because the **MaximumResultCount** is not supported in the [OpenSearch](https://github.com/dewitt/opensearch) v1.1 specification.</span></span>

### <a name="property-mapping"></a><span data-ttu-id="b2238-221">Eigenschaftszuordnung</span><span class="sxs-lookup"><span data-stu-id="b2238-221">Property Mapping</span></span>

<span data-ttu-id="b2238-222">Wenn Ergebnisse vom Webdienst als RSS-oder Atom-Feed zurückgegeben werden, muss der OpenSearch-Anbieter die Element Metadaten in den Feeds den Eigenschaften zuordnen, die von der Windows-Shell verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="b2238-222">When results are returned by the web service as an RSS or Atom feed, the OpenSearch provider must map the item metadata in the feeds to properties that the Windows Shell can use.</span></span> <span data-ttu-id="b2238-223">Der folgende Screenshot veranschaulicht, wie der OpenSearch-Anbieter einige der standardmäßigen RSS-Elemente zuordnet.</span><span class="sxs-lookup"><span data-stu-id="b2238-223">The following screen shot illustrates how the OpenSearch provider maps some of the default RSS elements.</span></span>

![Screenshot mit integrierten RSS-zu-Windows-shelleigenschaftenzuordnungen](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a><span data-ttu-id="b2238-225">Standardzuordnungen</span><span class="sxs-lookup"><span data-stu-id="b2238-225">Default Mappings</span></span>

<span data-ttu-id="b2238-226">In der folgenden Tabelle sind die Standard Zuordnungen von RSS-XML-Elementen zu den Windows Shell-Systemeigenschaften aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2238-226">The default mappings of RSS XML elements to Windows Shell system properties, are listed in the following table.</span></span> <span data-ttu-id="b2238-227">XML-Pfade sind relativ zum Item-Element.</span><span class="sxs-lookup"><span data-stu-id="b2238-227">XML paths are relative to the item element.</span></span> <span data-ttu-id="b2238-228">Das `"media:"` Präfix wird vom [Namespace](https://www.rssboard.org/media-rss) Namespace für Yahoo-Suche definiert.</span><span class="sxs-lookup"><span data-stu-id="b2238-228">The `"media:"` prefix is defined by the [Yahoo Search Namespace](https://www.rssboard.org/media-rss) namespace.</span></span>



| <span data-ttu-id="b2238-229">RSS-XML-Pfad</span><span class="sxs-lookup"><span data-stu-id="b2238-229">RSS XML path</span></span>                  | <span data-ttu-id="b2238-230">Windows Shell-Eigenschaft (Kanonischer Name)</span><span class="sxs-lookup"><span data-stu-id="b2238-230">Windows Shell property (canonical name)</span></span> |
|-------------------------------|-----------------------------------------|
| <span data-ttu-id="b2238-231">Link</span><span class="sxs-lookup"><span data-stu-id="b2238-231">Link</span></span>                          | <span data-ttu-id="b2238-232">System. itemurl</span><span class="sxs-lookup"><span data-stu-id="b2238-232">System.ItemUrl</span></span>                          |
| <span data-ttu-id="b2238-233">Titel</span><span class="sxs-lookup"><span data-stu-id="b2238-233">Title</span></span>                         | <span data-ttu-id="b2238-234">System. ItemName</span><span class="sxs-lookup"><span data-stu-id="b2238-234">System.ItemName</span></span>                         |
| <span data-ttu-id="b2238-235">Autor</span><span class="sxs-lookup"><span data-stu-id="b2238-235">Author</span></span>                        | <span data-ttu-id="b2238-236">System.Author</span><span class="sxs-lookup"><span data-stu-id="b2238-236">System.Author</span></span>                           |
| <span data-ttu-id="b2238-237">pubDate</span><span class="sxs-lookup"><span data-stu-id="b2238-237">pubDate</span></span>                       | <span data-ttu-id="b2238-238">System. DateModified</span><span class="sxs-lookup"><span data-stu-id="b2238-238">System.DateModified</span></span>                     |
| <span data-ttu-id="b2238-239">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2238-239">Description</span></span>                   | <span data-ttu-id="b2238-240">System. autosummary</span><span class="sxs-lookup"><span data-stu-id="b2238-240">System.AutoSummary</span></span>                      |
| <span data-ttu-id="b2238-241">Category</span><span class="sxs-lookup"><span data-stu-id="b2238-241">Category</span></span>                      | <span data-ttu-id="b2238-242">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="b2238-242">System.Keywords</span></span>                         |
| enclosure/@type               | <span data-ttu-id="b2238-243">System. MimeType</span><span class="sxs-lookup"><span data-stu-id="b2238-243">System.MIMEType</span></span>                         |
| enclosure/@length             | <span data-ttu-id="b2238-244">System. Size</span><span class="sxs-lookup"><span data-stu-id="b2238-244">System.Size</span></span>                             |
| enclosure/@url                | <span data-ttu-id="b2238-245">System. contenturl</span><span class="sxs-lookup"><span data-stu-id="b2238-245">System.ContentUrl</span></span>                       |
| <span data-ttu-id="b2238-246">Medien: Kategorie</span><span class="sxs-lookup"><span data-stu-id="b2238-246">media:category</span></span>                | <span data-ttu-id="b2238-247">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="b2238-247">System.Keywords</span></span>                         |
| media:content/@fileSize       | <span data-ttu-id="b2238-248">System. Size</span><span class="sxs-lookup"><span data-stu-id="b2238-248">System.Size</span></span>                             |
| media:content/@type           | <span data-ttu-id="b2238-249">System. MimeType</span><span class="sxs-lookup"><span data-stu-id="b2238-249">System.MIMEType</span></span>                         |
| media:content/@url            | <span data-ttu-id="b2238-250">System. contenturl</span><span class="sxs-lookup"><span data-stu-id="b2238-250">System.ContentUrl</span></span>                       |
| media:group/content/@fileSize | <span data-ttu-id="b2238-251">System. Size</span><span class="sxs-lookup"><span data-stu-id="b2238-251">System.Size</span></span>                             |
| media:group/content/@type     | <span data-ttu-id="b2238-252">System. MimeType</span><span class="sxs-lookup"><span data-stu-id="b2238-252">System.MIMEType</span></span>                         |
| media:group/content/@url      | <span data-ttu-id="b2238-253">System. contenturl</span><span class="sxs-lookup"><span data-stu-id="b2238-253">System.ContentUrl</span></span>                       |
| media:thumbnail/@url          | <span data-ttu-id="b2238-254">System. itemthumbnailurl</span><span class="sxs-lookup"><span data-stu-id="b2238-254">System.ItemThumbnailUrl</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="b2238-255">Zusätzlich zu den Standard Zuordnungen von Standard-RSS-oder Atom-Elementen können Sie weitere Windows Shell-Systemeigenschaften zuordnen, indem Sie für jede der Eigenschaften zusätzliche XML-Elemente in den Windows-Namespace einschließen.</span><span class="sxs-lookup"><span data-stu-id="b2238-255">In addition to the default mappings of standard RSS or Atom elements, you can map other Windows Shell system properties by including additional XML elements in the Windows namespace for each of the properties.</span></span> <span data-ttu-id="b2238-256">Sie können auch Elemente aus anderen vorhandenen XML-Namespaces (z. b. mediarss, iTunes usw.) zuordnen, indem Sie eine benutzerdefinierte Eigenschaften Zuordnung in der OSDX-Datei hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b2238-256">You can also map elements from other existing XML namespaces such as MediaRSS, iTunes, and so forth, by adding custom property mapping in the .osdx file.</span></span>

 

### <a name="custom-property-mappings"></a><span data-ttu-id="b2238-257">Zuordnungen von benutzerdefinierten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2238-257">Custom Property Mappings</span></span>

<span data-ttu-id="b2238-258">Sie können die Zuordnung von Elementen aus der RSS-Ausgabe zu Windows Shell-Systemeigenschaften anpassen, indem Sie die Zuordnung in der OSDX-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="b2238-258">You can customize the mapping of elements from your RSS output to Windows Shell system properties by specifying the mapping in the .osdx file.</span></span>

<span data-ttu-id="b2238-259">Die RSS-Ausgabe gibt Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="b2238-259">The RSS output specifies:</span></span>

-   <span data-ttu-id="b2238-260">Ein XML-Namespace und</span><span class="sxs-lookup"><span data-stu-id="b2238-260">An XML namespace, and</span></span>
-   <span data-ttu-id="b2238-261">Für alle untergeordneten Elemente eines Elements ein Elementname, der zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2238-261">For any child element of an item, an element name to map against.</span></span>

<span data-ttu-id="b2238-262">Die OSDX-Datei identifiziert eine Windows-shelleigenschaft für jeden Elementnamen in einem Namespace.</span><span class="sxs-lookup"><span data-stu-id="b2238-262">The .osdx file identifies a Windows Shell property for each element name in a namespace.</span></span> <span data-ttu-id="b2238-263">Die Eigenschaften Zuordnungen, die Sie in ihrer OSDX-Datei definieren, überschreiben die Standard Zuordnungen, sofern vorhanden, für diese angegebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b2238-263">The property mappings that you define in your .osdx file override the default mappings, if they exist, for those specified properties.</span></span>

<span data-ttu-id="b2238-264">Im folgenden Diagramm wird veranschaulicht, wie eine RSS-Erweiterung Windows-Eigenschaften (Kanonischer Name) zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="b2238-264">The following diagram illustrates how an RSS extension maps to Windows properties (canonical name).</span></span>

![Diagramm, das anzeigt, dass die Kombination aus XML-Namespace und XML-Pfad den kanonischen Namen erzeugt](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a><span data-ttu-id="b2238-266">Beispiel-RSS-Ergebnisse und OSD-Eigenschaften Zuordnung</span><span class="sxs-lookup"><span data-stu-id="b2238-266">Example RSS results and OSD Property Mapping</span></span>

<span data-ttu-id="b2238-267">Die folgende RSS-Beispielausgabe identifiziert `https://example.com/schema/2009` als XML-Namespace mit dem Präfix "example".</span><span class="sxs-lookup"><span data-stu-id="b2238-267">The following example RSS output identifies `https://example.com/schema/2009` as the XML namespace with the prefix "example".</span></span> <span data-ttu-id="b2238-268">Dieses Präfix muss wieder vor dem **e-Mail-** Element angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b2238-268">This prefix must appear again before the **email** element.</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



<span data-ttu-id="b2238-269">In der folgenden OSDX-Beispieldatei wird das XML **-e-Mail-** Element der Windows Shell-Eigenschaft [System. Contact. EmailAddress](../properties/props-system-contact-emailaddress.md)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b2238-269">In the following example .osdx file, the XML **email** element maps to the Windows Shell property [System.Contact.EmailAddress](../properties/props-system-contact-emailaddress.md).</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/"
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
...
 <ms-ose:ResultsProcessing format="application/rss+xml">
   <ms-ose:PropertyMapList>
     <ms-ose:PropertyMap sourceNamespaceURI="https://example.com/schema/2009/" >
       <ms-ose:Source path="email">
         <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace" name="System.Contact.EmailAddress" />
       </ms-ose:Source>
     </ms-ose:PropertyMap>
   </ms-ose:PropertyMapList>
 </ms-ose:ResultsProcessing>
...
</OpenSearchDescription>
```



<span data-ttu-id="b2238-270">Es gibt einige Eigenschaften, die nicht zugeordnet werden können, da die Werte für Sie entweder später überschrieben werden oder nicht bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="b2238-270">There are some properties that cannot be mapped because values for them are either overridden later or are not editable.</span></span> <span data-ttu-id="b2238-271">Beispielsweise kann [System. itemfolderpathdisplay](../properties/props-system-itempathdisplay.md) oder [System. itempathdisplaynarrow](../properties/props-system-itempathdisplaynarrow.md) nicht zugeordnet werden, da Sie aus dem URL-Wert berechnet werden, der in den Link-oder Gehäuse Elementen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b2238-271">For example, [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) or [System.ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) cannot be mapped because they are calculated from the URL value provided in either the link or enclosure elements.</span></span>

### <a name="thumbnails"></a><span data-ttu-id="b2238-272">Miniaturbilder</span><span class="sxs-lookup"><span data-stu-id="b2238-272">Thumbnails</span></span>

<span data-ttu-id="b2238-273">Miniaturbild-URLs können für jedes Element mithilfe des Mediums " **Miniaturansicht URL =" "** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b2238-273">Thumbnail image URLs can be provided for any item by using the **media:thumbnail url=""** element.</span></span> <span data-ttu-id="b2238-274">Die ideale Auflösung beträgt 150 x 150 Pixel.</span><span class="sxs-lookup"><span data-stu-id="b2238-274">The ideal resolution is 150 x 150 pixels.</span></span> <span data-ttu-id="b2238-275">Die größten unterstützten Miniaturansichten sind 256 x 256 Pixel.</span><span class="sxs-lookup"><span data-stu-id="b2238-275">The largest thumbnails supported are 256 x 256 pixels.</span></span> <span data-ttu-id="b2238-276">Das Bereitstellen größerer Abbilder erfordert mehr Bandbreite, sodass der Benutzer keinen zusätzlichen Vorteil hat.</span><span class="sxs-lookup"><span data-stu-id="b2238-276">Providing larger images takes more bandwidth for no extra benefit to the user.</span></span>

### <a name="open-file-location-context-menu"></a><span data-ttu-id="b2238-277">Kontextmenü für Datei Speicherort öffnen</span><span class="sxs-lookup"><span data-stu-id="b2238-277">Open File Location Context Menu</span></span>

<span data-ttu-id="b2238-278">Windows stellt ein Kontextmenü mit dem Namen " **Open File Location** " für Ergebnis Elemente bereit.</span><span class="sxs-lookup"><span data-stu-id="b2238-278">Windows provides a shortcut menu named **Open file location** for result items.</span></span> <span data-ttu-id="b2238-279">Wenn der Benutzer ein Element aus diesem Menü auswählt, wird die "übergeordnete" URL für das ausgewählte Element geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b2238-279">If the user selects an item from that menu, the "parent" URL for the selected item is opened.</span></span> <span data-ttu-id="b2238-280">Wenn die URL eine Web-URL ist (z. b.) `https://...` , wird der Webbrowser geöffnet und zu dieser URL navigiert.</span><span class="sxs-lookup"><span data-stu-id="b2238-280">If the URL is a web URL, such as `https://...`, the web browser is opened and navigated to that URL.</span></span> <span data-ttu-id="b2238-281">Ihr Feed sollte für jedes Element eine benutzerdefinierte URL bereitstellen, um sicherzustellen, dass Windows eine gültige URL öffnet.</span><span class="sxs-lookup"><span data-stu-id="b2238-281">Your feed should provide a custom URL for each item to ensure that Windows opens a valid URL.</span></span> <span data-ttu-id="b2238-282">Dies kann erreicht werden, indem die URL in ein Element innerhalb des XML-Elements eingeschlossen wird, wie im folgenden Beispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="b2238-282">This can be accomplished by including the URL within an element inside the item's XML, as illustrated in the following example:</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" 
    xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <link>https://example.com/pictures.aspx?id=01</link>
      <win:System.ItemFolderPathDisplay>https://example.com/pictures_list.aspx
   </win:System.ItemFolderPathDisplay>
   </item>
...
```



<span data-ttu-id="b2238-283">Wenn diese Eigenschaft nicht explizit im XML-Code des Elements festgelegt ist, legt der OpenSearch-Anbieter diese auf den übergeordneten Ordner der URL des Elements fest.</span><span class="sxs-lookup"><span data-stu-id="b2238-283">If this property is not explicitly set in the item's XML, the OpenSearch provider sets it to the parent folder of the URL of the item.</span></span> <span data-ttu-id="b2238-284">Im obigen Beispiel würde der OpenSearch-Anbieter den Linkwert verwenden und den Eigenschafts Wert [System. itemfolderpathdisplay](../properties/props-system-itemfolderpathdisplay.md) der Windows-Shell auf festlegen `"https://example.com/"` .</span><span class="sxs-lookup"><span data-stu-id="b2238-284">In the example above, the OpenSearch provider would use the link value, and set the [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) Windows Shell property value to `"https://example.com/"`.</span></span>

### <a name="customize-windows-explorer-views-with-property-description-lists"></a><span data-ttu-id="b2238-285">Anpassen von Windows Explorer-Ansichten mit Eigenschaften Beschreibungs Listen</span><span class="sxs-lookup"><span data-stu-id="b2238-285">Customize Windows Explorer Views with Property Description Lists</span></span>

<span data-ttu-id="b2238-286">Einige Windows Explorer-Ansichts Layouts werden durch Eigenschafts Beschreibungs Listen oder proplists definiert.</span><span class="sxs-lookup"><span data-stu-id="b2238-286">Some Windows Explorer view layouts are defined by property description lists, or proplists.</span></span> <span data-ttu-id="b2238-287">Eine proplist ist eine durch Semikolons getrennte Liste von Eigenschaften, z `"prop:System.ItemName; System.Author"` . b., die verwendet wird, um zu steuern, wie Ihre Ergebnisse in Windows-Explorer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b2238-287">A proplist is a semicolon-delimited list of properties, such as `"prop:System.ItemName; System.Author"`, that is used to control how your results appear in Windows Explorer.</span></span>

<span data-ttu-id="b2238-288">Die Benutzeroberflächen Bereiche von Windows Explorer, die mithilfe von proplists angepasst werden können, werden im folgenden Screenshot veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="b2238-288">The UI areas of Windows Explorer that can be customized by using proplists are illustrated in the following screen shot:</span></span>

![Screenshot der Benutzeroberflächen Bereiche von Windows Explorer, die mithilfe von proplists angepasst werden können](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

<span data-ttu-id="b2238-290">Jedem Bereich von Windows Explorer ist ein Satz von proplists zugeordnet, die selbst als Eigenschaften angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b2238-290">Each area of Windows Explorer has an associated set of proplists, which themselves are specified as properties.</span></span> <span data-ttu-id="b2238-291">Sie können benutzerdefinierte proplisten für einzelne Elemente in den Resultsets oder für alle Elemente in einem Resultset angeben.</span><span class="sxs-lookup"><span data-stu-id="b2238-291">You can specify custom proplists for individual items in your result sets or for all items in a set of results.</span></span>



| <span data-ttu-id="b2238-292">Benutzeroberflächen Bereich zum Anpassen</span><span class="sxs-lookup"><span data-stu-id="b2238-292">UI Area to customize</span></span>               | <span data-ttu-id="b2238-293">Windows Shell-Eigenschaft, die die Anpassung implementiert</span><span class="sxs-lookup"><span data-stu-id="b2238-293">Windows Shell property that implements the customization</span></span> |
|------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="b2238-294">Inhalts Ansichtsmodus (bei der Suche)</span><span class="sxs-lookup"><span data-stu-id="b2238-294">Content view mode (when searching)</span></span> | <span data-ttu-id="b2238-295">System. proplist. contentviewmodeforsearch</span><span class="sxs-lookup"><span data-stu-id="b2238-295">System.PropList.ContentViewModeForSearch</span></span>                 |
| <span data-ttu-id="b2238-296">Inhalts Ansichtsmodus (beim Durchsuchen)</span><span class="sxs-lookup"><span data-stu-id="b2238-296">Content view mode (when browsing)</span></span>  | <span data-ttu-id="b2238-297">System. proplist. contentviewmodeforbrowse</span><span class="sxs-lookup"><span data-stu-id="b2238-297">System.PropList.ContentViewModeForBrowse</span></span>                 |
| <span data-ttu-id="b2238-298">Kachel Ansichtsmodus</span><span class="sxs-lookup"><span data-stu-id="b2238-298">Tile view mode</span></span>                     | <span data-ttu-id="b2238-299">System. proplist. tileingefo</span><span class="sxs-lookup"><span data-stu-id="b2238-299">System.PropList.TileInfo</span></span>                                 |
| <span data-ttu-id="b2238-300">Detailbereich</span><span class="sxs-lookup"><span data-stu-id="b2238-300">Details pane</span></span>                       | <span data-ttu-id="b2238-301">System. proplist. previewdetails</span><span class="sxs-lookup"><span data-stu-id="b2238-301">System.PropList.PreviewDetails</span></span>                           |
| <span data-ttu-id="b2238-302">Infotip (QuickInfo des Elements)</span><span class="sxs-lookup"><span data-stu-id="b2238-302">Infotip (item's hover tooltip)</span></span>     | <span data-ttu-id="b2238-303">System. proplist. infotip</span><span class="sxs-lookup"><span data-stu-id="b2238-303">System.PropList.Infotip</span></span>                                  |



 

 

<span data-ttu-id="b2238-304">**So geben Sie eine eindeutige proplist für ein einzelnes Element an:**</span><span class="sxs-lookup"><span data-stu-id="b2238-304">**To specify a unique proplist for an individual item:**</span></span>

1.  <span data-ttu-id="b2238-305">Fügen Sie in der RSS-Ausgabe ein benutzerdefiniertes Element hinzu, das die anzufügende proplist darstellt.</span><span class="sxs-lookup"><span data-stu-id="b2238-305">In your RSS output, add a custom element representing the proplist you want to customize.</span></span> <span data-ttu-id="b2238-306">Im folgenden Beispiel wird z. b. die Liste für den Detailbereich festgelegt:</span><span class="sxs-lookup"><span data-stu-id="b2238-306">For example, the following example sets the list for the details pane:</span></span>
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  <span data-ttu-id="b2238-307">Wenn Sie eine Eigenschaft auf alle Elemente in den Suchergebnissen anwenden möchten, ohne die RSS-Ausgabe zu ändern, geben Sie eine proplist innerhalb eines **MS-ose: propertydefaultvalues** -Elements in der OSDX-Datei an, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="b2238-307">To apply a property to every item in the search results without modifying the RSS output, specify a proplist within an **ms-ose:PropertyDefaultValues** element in the .osdx file, as shown in the following example:</span></span>

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a><span data-ttu-id="b2238-308">Layout des Inhalts Ansichtsmodus von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2238-308">Content View Mode Layout of Properties</span></span>

<span data-ttu-id="b2238-309">Die Liste der Eigenschaften, die in den " **System. proplist. contentviewmodeforsearch** " und " **System. proplist. contentviewmodeforbrowse** "-proplist angegeben sind, bestimmt, was im Inhalts Ansichtsmodus angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b2238-309">The list of properties specified in the **System.PropList.ContentViewModeForSearch** and **System.PropList.ContentViewModeForBrowse** proplists determines what is shown in Content view mode.</span></span> <span data-ttu-id="b2238-310">Weitere Informationen zu Eigenschafts Listen finden Sie unter [proplist](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).</span><span class="sxs-lookup"><span data-stu-id="b2238-310">For more information about property lists, see [PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).</span></span>

<span data-ttu-id="b2238-311">Die Eigenschaften werden entsprechend den im folgenden Layoutmuster gezeigten Zahlen angeordnet:</span><span class="sxs-lookup"><span data-stu-id="b2238-311">The properties are laid out according to the numbers shown in the following layout pattern:</span></span>

![Screenshot mit dem standardlayoutmuster in der Inhaltsansicht](images/propertiesnumberslayoutpattern.png)

<span data-ttu-id="b2238-313">Wenn Sie die folgende Liste von Eigenschaften verwenden,</span><span class="sxs-lookup"><span data-stu-id="b2238-313">If we use the following list of properties,</span></span>


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



<span data-ttu-id="b2238-314">Anschließend wird die folgende Anzeige angezeigt:</span><span class="sxs-lookup"><span data-stu-id="b2238-314">Then we see the following display:</span></span>

![Screenshot mit Beispiel Eigenschaften Layout](images/samplepropertylayout.png)

> [!Note]  
> <span data-ttu-id="b2238-316">Um die beste Lesbarkeit zu erzielen, sollten die Eigenschaften, die in der Spalte ganz rechts angezeigt werden, mit der Bezeichnung gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="b2238-316">For the best readability, the properties shown in the right-most column should be labeled.</span></span>

 

### <a name="property-list-flags"></a><span data-ttu-id="b2238-317">Eigenschaften Listen-Flags</span><span class="sxs-lookup"><span data-stu-id="b2238-317">Property List Flags</span></span>

<span data-ttu-id="b2238-318">Nur eines der Flags, das in der proplists-Dokumentation definiert ist, gilt für die Anzeige von Elementen im Content View Mode Layouts: ` "~"` .</span><span class="sxs-lookup"><span data-stu-id="b2238-318">Only one of the flags defined in the proplists documentation applies to the display of items in Content View mode layouts:` "~"`.</span></span> <span data-ttu-id="b2238-319">In den vorherigen Beispielen werden in der Windows-Explorer-Ansicht einige Eigenschaften wie z. b. Beschriftungen `Tags: animals; zoo; lion` .</span><span class="sxs-lookup"><span data-stu-id="b2238-319">In the previous examples, the Windows Explorer view labels some of the properties, such as `Tags: animals; zoo; lion`.</span></span> <span data-ttu-id="b2238-320">Dies ist das Standardverhalten, wenn Sie eine Eigenschaft in der Liste angeben.</span><span class="sxs-lookup"><span data-stu-id="b2238-320">That is the default behavior when you specify a property in the list.</span></span> <span data-ttu-id="b2238-321">Beispielsweise enthält die proplist `"System.Author"` , die als angezeigt wird `"Authors: value"` .</span><span class="sxs-lookup"><span data-stu-id="b2238-321">For example, the proplist has `"System.Author"` which is displayed as `"Authors: value"`.</span></span> <span data-ttu-id="b2238-322">Wenn Sie die Eigenschaften Bezeichnung ausblenden möchten, platzieren Sie eine `"~"` vor dem Eigenschaftsnamen.</span><span class="sxs-lookup"><span data-stu-id="b2238-322">When you want to hide the property label, place a `"~"` in front of the property name.</span></span> <span data-ttu-id="b2238-323">Wenn die proplist beispielsweise ist `"~System.Size"` , wird die Eigenschaft nur als Wert ohne die Bezeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2238-323">For example, if the proplist has `"~System.Size"`, the property is displayed as just a value, without the label.</span></span>

## <a name="previews"></a><span data-ttu-id="b2238-324">Vorschau</span><span class="sxs-lookup"><span data-stu-id="b2238-324">Previews</span></span>

<span data-ttu-id="b2238-325">Wenn der Benutzer ein Ergebnis Element in Windows-Explorer auswählt und der Vorschaubereich geöffnet ist, wird der Inhalt des Elements in der Vorschau angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2238-325">When the user selects a result item in Windows Explorer and the preview pane is open, the content of the item is previewed.</span></span>

<span data-ttu-id="b2238-326">Der Inhalt, der in der Vorschau angezeigt werden soll, wird durch eine URL angegeben, die wie folgt bestimmt wird:</span><span class="sxs-lookup"><span data-stu-id="b2238-326">The content to show in the preview is specified by a URL, that is determined as follows:</span></span>

1.  <span data-ttu-id="b2238-327">Wenn die Eigenschaft **System. webpreviewurl** Windows Shell für das Element festgelegt ist, verwenden Sie diese URL.</span><span class="sxs-lookup"><span data-stu-id="b2238-327">If the **System.WebPreviewUrl** Windows Shell property is set for the item, then use that URL.</span></span>
    > [!Note]  
    > <span data-ttu-id="b2238-328">Die-Eigenschaft muss in der RSS mithilfe des Windows Shell-Namespace oder explizit in der OSDX-Datei zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b2238-328">The property needs to be provided in the RSS by using the Windows Shell namespace, or explicitly mapped in the .osdx file.</span></span>

     

2.  <span data-ttu-id="b2238-329">Wenn dies nicht der Typ ist, verwenden Sie stattdessen die Link-URL.</span><span class="sxs-lookup"><span data-stu-id="b2238-329">If not, then use the link URL instead.</span></span>

<span data-ttu-id="b2238-330">Diese Logik wird im folgenden Flussdiagramm veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b2238-330">The following flowchart shows this logic.</span></span>

![Flussdiagramm, das zeigt, wie Windows Explorer die URL für die Vorschau auswählt](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

<span data-ttu-id="b2238-332">Es ist möglich, eine andere URL als Vorschauversion für das Element selbst zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2238-332">It is possible to use a different URL for the preview than for the item itself.</span></span> <span data-ttu-id="b2238-333">Wenn Sie also unterschiedliche URLs für die Link-URL und das Gehäuse oder bereitstellen `media:content URL` , verwendet Windows Explorer die Link-URL für die Vorschau des Elements, verwendet jedoch die andere URL für die Dateityp Erkennung, das Öffnen, das Herunterladen usw.</span><span class="sxs-lookup"><span data-stu-id="b2238-333">This means that if you provide different URLs for the link URL and the enclosure or `media:content URL`, Windows Explorer uses the link URL for previews of the item but uses the other URL for file type detection, opening, downloading, and so forth.</span></span>

<span data-ttu-id="b2238-334">Bestimmen der zu verwendenden URL durch Windows-Explorer:</span><span class="sxs-lookup"><span data-stu-id="b2238-334">How Windows Explorer determines what URL to use:</span></span>

1.  <span data-ttu-id="b2238-335">Wenn Sie eine Zuordnung zu [System. itemfolderpathdisplay](../properties/props-system-itemfolderpathdisplay.md)bereitstellen, verwendet Windows Explorer diese URL.</span><span class="sxs-lookup"><span data-stu-id="b2238-335">If you provide a mapping to [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md), then Windows Explorer uses that URL</span></span>
2.  <span data-ttu-id="b2238-336">Wenn Sie keine Zuordnung bereitstellen, identifiziert Windows Explorer, ob sich die Link-und die Gehäuse-URLs unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="b2238-336">If you do not provide a mapping, then Windows Explorer identifies whether the link and enclosure URLs are different.</span></span> <span data-ttu-id="b2238-337">Wenn dies der Fall ist, verwendet Windows Explorer die Link-URL.</span><span class="sxs-lookup"><span data-stu-id="b2238-337">If so, then Windows Explorer uses the link URL.</span></span>
3.  <span data-ttu-id="b2238-338">Wenn die URLs identisch sind oder nur eine Link-URL vorhanden ist, analysiert Windows Explorer den Link, um den übergeordneten Container zu suchen, indem der Dateiname aus der vollständigen URL entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b2238-338">If the URLs are the same or if there is only a link URL, then Windows Explorer parses the link to find the parent container by removing the file name from the full URL.</span></span>
    > [!Note]  
    > <span data-ttu-id="b2238-339">Wenn Sie erkennen, dass die URL-Verarbeitung zu inaktiven Links für den Dienst führen würde, sollten Sie eine explizite Zuordnung für die Eigenschaft bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b2238-339">If you recognize that the URL parsing would result in dead links for your service, you should provide an explicit mapping for the property.</span></span>

     

## <a name="open-file-location-menu-item"></a><span data-ttu-id="b2238-340">Menü Element "Datei Speicherort öffnen"</span><span class="sxs-lookup"><span data-stu-id="b2238-340">Open File Location Menu Item</span></span>

<span data-ttu-id="b2238-341">Wenn Sie mit der rechten Maustaste auf ein Element klicken, wird der Menübefehl **Datei Speicherort öffnen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2238-341">When a right-clicks an item, the **Open file location** menu command appears.</span></span> <span data-ttu-id="b2238-342">Mit diesem Befehl wird der Benutzer in den Container für das Element oder den Speicherort dieses Elements gelangen.</span><span class="sxs-lookup"><span data-stu-id="b2238-342">This command takes the user to the container for or location of that item.</span></span> <span data-ttu-id="b2238-343">Wenn Sie z. b. in einer SharePoint-Suche diese Option für eine Datei in einer Dokumentbibliothek auswählen, wird der Stamm der Dokumentbibliothek im Webbrowser geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b2238-343">For example, in a SharePoint search, selecting this option for a file in a document library would open the document library root in the web browser.</span></span>

<span data-ttu-id="b2238-344">Wenn ein Benutzer auf **Datei Speicherort öffnen** klickt, versucht Windows Explorer, mithilfe der im folgenden Flussdiagramm gezeigten Logik einen übergeordneten Container zu finden:</span><span class="sxs-lookup"><span data-stu-id="b2238-344">When a user clicks **Open file location**, Windows Explorer attempts to find a parent container, by using the logic shown in the following flowchart:</span></span>

![Flussdiagramm, das zeigt, wie Windows Explorer einen übergeordneten Container identifiziert](images/howwindowsexploreridentifiesaparentcontainer.png)

## <a name="additional-resources"></a><span data-ttu-id="b2238-346">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b2238-346">Additional Resources</span></span>

<span data-ttu-id="b2238-347">Weitere Informationen zum Implementieren eines Such Verbunds in Remote Datenspeicher mithilfe von OpenSearch-Technologien in Windows 7 und höher finden Sie unter "zusätzliche Ressourcen" bei der [Verbund Suche in Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b2238-347">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2238-348">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b2238-348">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2238-349">Verbundsuche in Windows 10</span><span class="sxs-lookup"><span data-stu-id="b2238-349">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="b2238-350">Ersten Einstieg in die Verbund Suche in Windows</span><span class="sxs-lookup"><span data-stu-id="b2238-350">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="b2238-351">Verbinden des Webdiensts in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="b2238-351">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="b2238-352">Aktivieren des Datenspeicher in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="b2238-352">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="b2238-353">Bewährte Methoden bei der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="b2238-353">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="b2238-354">Bereitstellen von Suchconnectors in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="b2238-354">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
