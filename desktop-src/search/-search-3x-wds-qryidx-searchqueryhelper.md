---
description: 'Sie können die isearchqueryhelper-Schnittstelle verwenden, um den Index abzufragen. Diese Schnittstelle wird als Hilfsklasse in isearchcatalogmanager (und ISearchCatalogManager2) implementiert und durch Aufrufen von isearchcatalogmanager:: getqueryhelper abgerufen.'
ms.assetid: 6e567c09-8763-4866-bf02-ad6651b454db
title: Abfragen des Indexes mit isearchqueryhelper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b9d970a1e3f416081d3b7fd3e9d6c2af0a2bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214463"
---
# <a name="querying-the-index-with-isearchqueryhelper"></a><span data-ttu-id="0b0b7-104">Abfragen des Indexes mit isearchqueryhelper</span><span class="sxs-lookup"><span data-stu-id="0b0b7-104">Querying the Index with ISearchQueryHelper</span></span>

<span data-ttu-id="0b0b7-105">Sie können die [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) -Schnittstelle verwenden, um den Index abzufragen.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-105">You can use the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface to query the index.</span></span> <span data-ttu-id="0b0b7-106">Diese Schnittstelle wird als Hilfsklasse in [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (und [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) implementiert und durch Aufrufen von [**isearchcatalogmanager:: getqueryhelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-106">This interface is implemented as a helper class to [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (and [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)), and is obtained by calling [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span></span> <span data-ttu-id="0b0b7-107">Diese Schnittstelle ermöglicht Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0b0b7-107">This interface permits you to:</span></span>

-   <span data-ttu-id="0b0b7-108">Rufen Sie eine OLE DB Verbindungs Zeichenfolge für die Verbindung mit der Windows Search-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-108">Obtain an OLE DB connection string to connect to the Windows Search database.</span></span>
-   <span data-ttu-id="0b0b7-109">Konvertieren von Benutzer Abfragen der erweiterten Abfrage Syntax (AQS) in Windows Search Structured Query Language (SQL).</span><span class="sxs-lookup"><span data-stu-id="0b0b7-109">Convert Advanced Query Syntax (AQS) user queries to Windows Search Structured Query Language (SQL).</span></span>
-   <span data-ttu-id="0b0b7-110">Geben Sie Abfrage Einschränkungen an, die in SQL ausgedrückt werden können, aber nicht in AQS.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-110">Specify query restrictions that can be expressed in SQL, but not in AQS.</span></span>

<span data-ttu-id="0b0b7-111">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="0b0b7-111">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="0b0b7-112">Ersten Einstieg in isearchqueryhelper</span><span class="sxs-lookup"><span data-stu-id="0b0b7-112">Getting Started with ISearchQueryHelper</span></span>](#getting-started-with-isearchqueryhelper)
-   [<span data-ttu-id="0b0b7-113">Verwenden der generatesqlfromuserquery-Methode</span><span class="sxs-lookup"><span data-stu-id="0b0b7-113">Using the GenerateSqlFromUserQuery Method</span></span>](#using-the-generatesqlfromuserquery-method)
-   [<span data-ttu-id="0b0b7-114">Arbeiten mit Gebiets Schema Bezeichnerzeichen</span><span class="sxs-lookup"><span data-stu-id="0b0b7-114">Working with Locale Identifiers</span></span>](#working-with-locale-identifiers)
-   [<span data-ttu-id="0b0b7-115">Arbeiten mit Eigenschaften und Spalten</span><span class="sxs-lookup"><span data-stu-id="0b0b7-115">Working with Properties and Columns</span></span>](#working-with-properties-and-columns)
-   [<span data-ttu-id="0b0b7-116">Arbeiten mit der Abfrage Begriffs Erweiterung</span><span class="sxs-lookup"><span data-stu-id="0b0b7-116">Working with Query Term Expansion</span></span>](#working-with-query-term-expansion)
-   [<span data-ttu-id="0b0b7-117">Arbeiten mit anderen isearchqueryhelper-Methoden</span><span class="sxs-lookup"><span data-stu-id="0b0b7-117">Working with Other ISearchQueryHelper Methods</span></span>](#working-with-other-isearchqueryhelper-methods)
-   [<span data-ttu-id="0b0b7-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b0b7-118">Related topics</span></span>](#related-topics)

## <a name="getting-started-with-isearchqueryhelper"></a><span data-ttu-id="0b0b7-119">Ersten Einstieg in isearchqueryhelper</span><span class="sxs-lookup"><span data-stu-id="0b0b7-119">Getting Started with ISearchQueryHelper</span></span>

<span data-ttu-id="0b0b7-120">Es gibt einige wichtige Schnittstellen und Methoden, die Sie kennen sollten, bevor Sie mit der [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) -Schnittstelle Programm gesteuert mit der Windows-Suche beginnen können.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-120">There are a few key interfaces and methods you should be aware of before you can start programmatically querying Windows Search using the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface.</span></span> <span data-ttu-id="0b0b7-121">Auf hoher Ebene müssen Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="0b0b7-121">At a high level, you need to follow these steps:</span></span>

1.  <span data-ttu-id="0b0b7-122">Instanziieren Sie eine [**isearchmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) -Instanz.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-122">Instantiate an [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) instance.</span></span>
    ```
    // Create ISearchManager instance
    ISearchManager* pSearchManager;

    // Use library SearchSDK.lib for CLSID_CSearchManager.
    hr = CoCreateInstance(CLSID_CSearchManager, NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));      
    ```

    

2.  <span data-ttu-id="0b0b7-123">Rufen Sie mithilfe von [**isearchmanager:: getCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog)eine Instanz von [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) ab.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-123">Obtain an instance of [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) using [**ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog).</span></span> <span data-ttu-id="0b0b7-124">Der Name des System Katalogs für Windows Search lautet `SYSTEMINDEX` .</span><span class="sxs-lookup"><span data-stu-id="0b0b7-124">The name of the system catalog for Windows Search is `SYSTEMINDEX`.</span></span>
    ```
    // Create ISearchCatalogManager instance 
    ISearchCatalogManager* pSearchCatalogManager;

    // Call ISearchManager::GetCatalog for "SystemIndex" to access the catalog to the ISearchCatalogManager
    hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
            
    ```

    

3.  <span data-ttu-id="0b0b7-125">Rufen Sie eine Instanz von [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) mithilfe von [**isearchcatalogmanager:: getqueryhelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)ab.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-125">Obtain an instance of [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) using [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span></span>
    ```
    // Call ISearchCatalogManager::GetQueryHelper to get the ISearchQueryHelper interface
    ISearchQueryHelper* pQueryHelper;

    hr = pSearchCatalogManager->GetQueryHelper(&pQueryHelper);
            
    ```

    

4.  <span data-ttu-id="0b0b7-126">Nachdem Sie über eine Instanz von [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)verfügen, können Sie die Verbindungs Zeichenfolge abrufen, die zum Herstellen einer Verbindung mit dem Windows Search-Index OLE DB-Connector verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-126">After you have an instance of [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), you can then get the connection string used to connect to the Windows Search index OLE DB connector.</span></span>
    ```
    // Call get_ConnectionString to get the OLE DB connection string
    LPWSTR pszConnectionString=NULL;

    hr = pQueryHelper->get_ConnectionString(&pszConnectionString);
    // NOTE: YOU MUST call CoTaskMemFree() on the string
        
    ```

    

## <a name="using-the-generatesqlfromuserquery-method"></a><span data-ttu-id="0b0b7-127">Verwenden der generatesqlfromuserquery-Methode</span><span class="sxs-lookup"><span data-stu-id="0b0b7-127">Using the GenerateSqlFromUserQuery Method</span></span>

<span data-ttu-id="0b0b7-128">Die [**isearchqueryhelper:: generatesqlfromuserquery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) -Methode wandelt Benutzereingaben in eine SQL-Abfrage Zeichenfolge um, die dann an den OLE DB-Anbieter für Windows Search übermittelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-128">The [**ISearchQueryHelper::GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) method transforms user input into a SQL query string, which can then be submitted to the OLE DB provider for Windows Search.</span></span> <span data-ttu-id="0b0b7-129">Diese Methode übersetzt die vom Benutzer eingegebene [Erweiterte Abfrage Syntax](-search-3x-advancedquerysyntax.md) (AQS) oder die NQS-Abfrage (Natural Query Syntax) in SQL und ermöglicht das Hinzufügen anderer SQL-Fragmente nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-129">This method translates the [Advanced Query Syntax](-search-3x-advancedquerysyntax.md) (AQS) or Natural Query Syntax (NQS) query entered by the user into SQL, and lets you add other SQL fragments as needed.</span></span>

<span data-ttu-id="0b0b7-130">Die SQL-Abfrage Zeichenfolge wird im folgenden Format zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="0b0b7-130">The SQL query string is returned in the following form:</span></span>


```
SELECT <QuerySelectColumns> 
FROM <CatalogName that created query helper>
WHERE <Result of interpreting the user query passed into this function according to QuerySyntax>
      [ AND|OR <QueryWhereRestrictions> ]
    
```



<span data-ttu-id="0b0b7-131">Es folgt ein Beispiel für die SQL-Zeichenfolge, die vom-Befehl zurückgegeben wird `GenerateSQLFromUserQuery("comput")` :</span><span class="sxs-lookup"><span data-stu-id="0b0b7-131">The following is an example of the SQL string returned from the call `GenerateSQLFromUserQuery("comput")`:</span></span>


```
SELECT "System.ItemUrl" 
FROM "SystemIndex" 
WHERE ((CONTAINS(*,'"comput*"',1033) RANK BY COERCION(Absolute, 1)) OR 
       (FREETEXT(("System.ItemNameDisplay":0.9, *:0.1), 'comput', 1033) AND CONTAINS(*,'"comput"',1033)))
ORDER BY "System.ItemUrl"
```



> [!Note]  
> <span data-ttu-id="0b0b7-132">Die-Methode generiert sowohl den fretext-als auch das-Prädikat "enthält", da "enthält allein" keine sinnvolle Rangfolge generiert</span><span class="sxs-lookup"><span data-stu-id="0b0b7-132">The method generates both the FREETEXT and the CONTAINS predicates because CONTAINS alone does not generate meaningful ranking.</span></span>

 

## <a name="working-with-locale-identifiers"></a><span data-ttu-id="0b0b7-133">Arbeiten mit Gebiets Schema Bezeichnerzeichen</span><span class="sxs-lookup"><span data-stu-id="0b0b7-133">Working with Locale Identifiers</span></span>



| <span data-ttu-id="0b0b7-134">Methode</span><span class="sxs-lookup"><span data-stu-id="0b0b7-134">Method</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="0b0b7-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b0b7-135">Description</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b0b7-136">[**Isearchqueryhelper:: get \_ querycontentlocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/</span><span class="sxs-lookup"><span data-stu-id="0b0b7-136">[**ISearchQueryHelper::get\_QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/</span></span><br/> [<span data-ttu-id="0b0b7-137">**Isearchqueryhelper::p UT \_ querycontentlocale**</span><span class="sxs-lookup"><span data-stu-id="0b0b7-137">**ISearchQueryHelper::put\_QueryContentLocale**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale)<br/> | <span data-ttu-id="0b0b7-138">Ruft den Sprachcode Bezeichner (LCID) der Abfrage ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-138">Gets/Puts the language code identifier (LCID) of the query.</span></span> <span data-ttu-id="0b0b7-139">Dadurch werden die richtigen Wörter Trennungen und Wort Stamm Erkennung zum Vergleichen von Abfrage Begriffen mit dem Katalog-/invertierten Index unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-139">This helps get the correct wordbreaker and stemmer to compare query terms against the catalog/inverted index.</span></span> <span data-ttu-id="0b0b7-140">Der Standardwert ist das aktuelle Eingabe Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-140">The default is the current input locale.</span></span> |
| <span data-ttu-id="0b0b7-141">[**Isearchqueryhelper:: get \_ querykeywordlocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/</span><span class="sxs-lookup"><span data-stu-id="0b0b7-141">[**ISearchQueryHelper::get\_QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/</span></span><br/> [<span data-ttu-id="0b0b7-142">**Isearchqueryhelper::p UT \_ querykeywordlocale**</span><span class="sxs-lookup"><span data-stu-id="0b0b7-142">**ISearchQueryHelper::put\_QueryKeywordLocale**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale)<br/> | <span data-ttu-id="0b0b7-143">Ruft die LCID für die Sprache ab, die beim Abfragen von AQS-Schlüsselwörtern (Advanced Query Syntax) verwendet werden soll, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-143">Gets/Puts the LCID for the language to use when parsing Advanced Query Syntax (AQS) keywords.</span></span> <span data-ttu-id="0b0b7-144">Der Standardwert ist das Standard Gebiets Schema des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-144">The default is the default user locale.</span></span>                                                                              |



 

<span data-ttu-id="0b0b7-145">Das **Inhalts** Gebiets Schema und das **Schlüsselwort** Gebiets Schema sind Gebiets Schema Bezeichner (Locale Identifier, LCID), die dem Suchmodul helfen, die richtigen Wörter Trennungen zu verwenden, indem die Sprache der Abfrage Begriffe und die Sprache der AQS-Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0b0b7-145">The **content locale** and **keyword locale** are locale identifiers (LCID) that help the search engine use the correct word breakers by identifying the language of the query terms and the language the AQS keywords.</span></span> <span data-ttu-id="0b0b7-146">Dabei handelt es sich nicht immer um die gleichen LCIDs, da Windows Search in einer Reihe von internationalen Versionen angeboten wird und auch mehrsprachige Benutzeroberflächen Pakete (MUI) für weitere Sprachen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-146">These are not always the same LCIDs because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="0b0b7-147">Das Content-Gebiets Schema identifiziert die LCID für die Sprache, die Benutzer in die Suchabfrage eingeben, während das Schlüsselwort locale die LCID identifiziert, die die Suchmaschine beim Durchsuchen von Schlüsselwörtern für die Erweiterte Abfrage Syntax (AQS) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-147">The content locale identifies the LCID for the language users input their search query in, while the keyword locale identifies the LCID the search engine uses when parsing Advanced Query Syntax (AQS) keywords.</span></span>

<span data-ttu-id="0b0b7-148">Wenn Sie z. b. die englischsprachige Version ohne MUI-Pakete haben, sind sowohl das Gebiets Schema des Inhalts Gebiets Schemas als auch das Schlüsselwort locale 1033.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-148">For example, if you have the English-US version with no MUI packs, both the content locale and keyword locale are 1033.</span></span> <span data-ttu-id="0b0b7-149">Wenn Sie über die deutsche Version ohne MUI-Pakete verfügen, sind sowohl das Gebiets Schema des Inhalts Gebiets Schemas als auch das Schlüsselwort locale 1031 (Gr-GR).</span><span class="sxs-lookup"><span data-stu-id="0b0b7-149">If you have the German version with no MUI packs, then both the content locale and keyword locale are 1031 (gr-gr).</span></span> <span data-ttu-id="0b0b7-150">Wenn Sie jedoch über die englische Version mit dem rumänischen MUI Pack verfügen, ist das Inhalts Gebiets Schema 2072 (RO), und das Schlüsselwort locale ist 1033 (en-US).</span><span class="sxs-lookup"><span data-stu-id="0b0b7-150">However, if you have the English version with the Romanian MUI pack, the content locale is 2072 (ro) and the keyword locale is 1033 (en-us).</span></span>

## <a name="working-with-properties-and-columns"></a><span data-ttu-id="0b0b7-151">Arbeiten mit Eigenschaften und Spalten</span><span class="sxs-lookup"><span data-stu-id="0b0b7-151">Working with Properties and Columns</span></span>



| <span data-ttu-id="0b0b7-152">Methoden</span><span class="sxs-lookup"><span data-stu-id="0b0b7-152">Methods</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="0b0b7-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b0b7-153">Description</span></span>                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b0b7-154">[**Isearchqueryhelper:: get \_ querycontentproperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/</span><span class="sxs-lookup"><span data-stu-id="0b0b7-154">[**ISearchQueryHelper::get\_QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/</span></span><br/> [<span data-ttu-id="0b0b7-155">**Isearchqueryhelper::p UT \_ querycontentproperties**</span><span class="sxs-lookup"><span data-stu-id="0b0b7-155">**ISearchQueryHelper::put\_QueryContentProperties**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties)<br/> | <span data-ttu-id="0b0b7-156">Dient zum Abrufen oder Festlegen der Inhalts Eigenschaften für die Suche (in der enthält-Klausel oder der frei Text Klausel aufgeführte Eigenschafts Spalte).</span><span class="sxs-lookup"><span data-stu-id="0b0b7-156">Gets/Sets the content properties for the search (property column listed in the CONTAINS or FREETEXT clauses).</span></span>                                   |
| <span data-ttu-id="0b0b7-157">[**Isearchqueryhelper:: get \_ queryselectcolumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/</span><span class="sxs-lookup"><span data-stu-id="0b0b7-157">[**ISearchQueryHelper::get\_QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/</span></span><br/> [<span data-ttu-id="0b0b7-158">**Isearchqueryhelper::p UT \_ queryselectcolumns**</span><span class="sxs-lookup"><span data-stu-id="0b0b7-158">**ISearchQueryHelper::put\_QuerySelectColumns**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns)<br/>                 | <span data-ttu-id="0b0b7-159">Ruft die in der SELECT-Anweisung angeforderten Spalten (oder Eigenschaften) ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-159">Gets/Sets the columns (or properties) requested in the SELECT statement.</span></span> <span data-ttu-id="0b0b7-160">Der Standardwert ist System. itemurl und Eigenschaften, die in der WHERE-Klausel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-160">The default is System.ItemUrl and properties used in the WHERE clause.</span></span> |



 

<span data-ttu-id="0b0b7-161">Elemente werden im Eigenschaften Speicher als Zeile dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-161">Items are represented in the property store as a row.</span></span> <span data-ttu-id="0b0b7-162">Jede Zeile enthält eine Reihe von Spalten, die Eigenschaften für dieses Element darstellen.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-162">Each row contains a number of columns that represent properties for that item.</span></span> <span data-ttu-id="0b0b7-163">Nicht alle Elemente haben einen Wert für eine bestimmte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-163">Not all items will have a value for a given property.</span></span> <span data-ttu-id="0b0b7-164">Beispielsweise enthält eine Audiodatei in der Regel keinen Wert für die System. Property. FromName-Eigenschaft, kann jedoch Informationen zu System. Music. Artist enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-164">For example, an audio file would typically not contain a value for the System.Property.FromName property but may contain information regarding the System.Music.Artist.</span></span>

<span data-ttu-id="0b0b7-165">Mit diesen Methoden greifen Sie auf die-Eigenschaft mit einer durch Trennzeichen getrennten, auf NULL endenden Unicode-Zeichenfolge zu, die einen oder mehrere Spaltennamen des Eigenschaften Stores angibt: "System.Document. Autor, System.Doc. Title ".</span><span class="sxs-lookup"><span data-stu-id="0b0b7-165">With these methods, you access or modify the property with a comma delimited, null-terminated, Unicode string that specifies one or more column names of the property store: "System.Document.Author, System.Document.Title".</span></span>

## <a name="working-with-query-term-expansion"></a><span data-ttu-id="0b0b7-166">Arbeiten mit der Abfrage Begriffs Erweiterung</span><span class="sxs-lookup"><span data-stu-id="0b0b7-166">Working with Query Term Expansion</span></span>



| <span data-ttu-id="0b0b7-167">Methoden</span><span class="sxs-lookup"><span data-stu-id="0b0b7-167">Methods</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="0b0b7-168">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b0b7-168">Description</span></span>                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="0b0b7-169">**Isearchqueryhelper:: get \_ querytermexpansion**</span><span class="sxs-lookup"><span data-stu-id="0b0b7-169">**ISearchQueryHelper::get\_QueryTermExpansion**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion)<br/> [<span data-ttu-id="0b0b7-170">**Isearchqueryhelper::p UT \_ querytermexpansion**</span><span class="sxs-lookup"><span data-stu-id="0b0b7-170">**ISearchQueryHelper::put\_QueryTermExpansion**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion)<br/> | <span data-ttu-id="0b0b7-171">Ruft das Erweiterungs Flag für den Suchbegriff ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-171">Gets/Sets the search term expansion flag.</span></span> |



 

<span data-ttu-id="0b0b7-172">Diese Methode ermöglicht die Erweiterung einiger Abfrage Ausdrücke mit Platzhalter Zeichen, ähnlich der Erweiterung regulärer Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-172">This method enables the expansion of some query terms with wild card characters, similar to regular expression expansion.</span></span> <span data-ttu-id="0b0b7-173">Präfix Erweiterung sucht nach Wörtern mit dem gleichen Präfix (Spaß/Trichter).</span><span class="sxs-lookup"><span data-stu-id="0b0b7-173">Prefix expansion searches for words with the same prefix (fun/funnel).</span></span> <span data-ttu-id="0b0b7-174">Wenn nicht festgelegt, lautet der Standardwert Such \_ Begriff " \_ alle" \_ .</span><span class="sxs-lookup"><span data-stu-id="0b0b7-174">If not set, the default value is SEARCH\_TERM\_PREFIX\_ALL.</span></span> <span data-ttu-id="0b0b7-175">Die folgenden Werte sind für die Enumeration der [**\_ \_ Erweiterungs**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) Enumeration unterstützt:</span><span class="sxs-lookup"><span data-stu-id="0b0b7-175">The supported values of the [**SEARCH\_TERM\_EXPANSION**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) enumeration are as follows:</span></span>

-   <span data-ttu-id="0b0b7-176">Such \_ Begriff \_ Präfix \_ alle-alle Suchbegriffe werden erweitert</span><span class="sxs-lookup"><span data-stu-id="0b0b7-176">SEARCH\_TERM\_PREFIX\_ALL - All search terms are expanded</span></span>
-   <span data-ttu-id="0b0b7-177">Such \_ Begriff \_ keine \_ Erweiterung-keine Suchbegriffe erweitert</span><span class="sxs-lookup"><span data-stu-id="0b0b7-177">SEARCH\_TERM\_NO\_EXPANSION - No search terms are expanded</span></span>

## <a name="working-with-other-isearchqueryhelper-methods"></a><span data-ttu-id="0b0b7-178">Arbeiten mit anderen isearchqueryhelper-Methoden</span><span class="sxs-lookup"><span data-stu-id="0b0b7-178">Working with Other ISearchQueryHelper Methods</span></span>

<span data-ttu-id="0b0b7-179">Viele der Methoden in der [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) -Schnittstelle werden verwendet, um Abfrage Argumente festzulegen oder die zurückgegebenen Eigenschaften zu definieren.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-179">Many of the methods in the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface are used to set query arguments or define the properties returned.</span></span>



| <span data-ttu-id="0b0b7-180">Methoden</span><span class="sxs-lookup"><span data-stu-id="0b0b7-180">Methods</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="0b0b7-181">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b0b7-181">Description</span></span>                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b0b7-182">**Isearchqueryhelper:: get \_ ConnectionString**</span><span class="sxs-lookup"><span data-stu-id="0b0b7-182">**ISearchQueryHelper::get\_ConnectionString**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)<br/>                                                                                                                                         | <span data-ttu-id="0b0b7-183">Gibt die OLE DB Verbindungs Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-183">Returns the OLE DB connection string.</span></span> <span data-ttu-id="0b0b7-184">Dies ist die bevorzugte Methode, um eine ordnungsgemäß formatierte und korrekte Verbindungs Zeichenfolge zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-184">This is the preferred method of getting a properly formatted and correct connection string.</span></span>                                  |
| [<span data-ttu-id="0b0b7-185">**Isearchqueryhelper:: get \_ querymaxresults**</span><span class="sxs-lookup"><span data-stu-id="0b0b7-185">**ISearchQueryHelper::get\_QueryMaxResults**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults)<br/> [<span data-ttu-id="0b0b7-186">**Isearchqueryhelper::p UT \_ querymaxresults**</span><span class="sxs-lookup"><span data-stu-id="0b0b7-186">**ISearchQueryHelper::put\_QueryMaxResults**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults)<br/>                             | <span data-ttu-id="0b0b7-187">Ruft die maximale Anzahl von Ergebnissen ab, die von einer Abfrage zurückgegeben werden sollen (d. h. Select Top n), oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-187">Gets/Sets the maximum number of results to be returned by a query (that is, SELECT TOP n).</span></span> <span data-ttu-id="0b0b7-188">Der Standardwert ist-1. Dies bedeutet, dass keine maximale Ergebnis Klausel generiert wird.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-188">The default is -1, meaning that no maximum results clause is generated.</span></span> |
| [<span data-ttu-id="0b0b7-189">**Isearchqueryhelper:: get \_ querysortierung**</span><span class="sxs-lookup"><span data-stu-id="0b0b7-189">**ISearchQueryHelper::get\_QuerySorting**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysorting)<br/> [<span data-ttu-id="0b0b7-190">**Isearchqueryhelper::p UT- \_ querysortierung**</span><span class="sxs-lookup"><span data-stu-id="0b0b7-190">**ISearchQueryHelper::put\_QuerySorting**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysorting)<br/>                                         | <span data-ttu-id="0b0b7-191">Gibt die Sortierreihenfolge für das Abfrageresultset zurück (Order by).</span><span class="sxs-lookup"><span data-stu-id="0b0b7-191">Gets/Sets the sort order for the query result set (ORDER BY).</span></span> <span data-ttu-id="0b0b7-192">Wenn keine ORDER BY-Klausel vorhanden ist, werden die Ergebnisse in nicht deterministischer Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-192">If no ORDER BY clause exists, the results are returned in non-deterministic order.</span></span>                   |
| [<span data-ttu-id="0b0b7-193">**Isearchqueryhelper:: get \_ querysyntax**</span><span class="sxs-lookup"><span data-stu-id="0b0b7-193">**ISearchQueryHelper::get\_QuerySyntax**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax)<br/> [<span data-ttu-id="0b0b7-194">**Isearchqueryhelper::p UT- \_ querysyntax**</span><span class="sxs-lookup"><span data-stu-id="0b0b7-194">**ISearchQueryHelper::put\_QuerySyntax**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax)<br/>                                             | <span data-ttu-id="0b0b7-195">Ruft die Syntax der Abfrage ab oder legt Sie fest: Erweiterte Abfrage Syntax oder Syntax für natürliche Abfragen.</span><span class="sxs-lookup"><span data-stu-id="0b0b7-195">Gets/Sets the syntax of the query: Advanced Query Syntax or Natural Query Syntax.</span></span>                                                                                  |
| [<span data-ttu-id="0b0b7-196">**Isearchqueryhelper:: get \_ querywhererestrictions**</span><span class="sxs-lookup"><span data-stu-id="0b0b7-196">**ISearchQueryHelper::get\_QueryWhereRestrictions**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions)<br/> [<span data-ttu-id="0b0b7-197">**Isearchqueryhelper::p UT \_ querywhererestrictions**</span><span class="sxs-lookup"><span data-stu-id="0b0b7-197">**ISearchQueryHelper::put\_QueryWhereRestrictions**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions)<br/> | <span data-ttu-id="0b0b7-198">Gibt die Einschränkungen an, die über WHERE-Klauseln angefügt werden</span><span class="sxs-lookup"><span data-stu-id="0b0b7-198">Gets/Sets the restrictions appended via WHERE clauses.</span></span>                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="0b0b7-199">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b0b7-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b0b7-200">Programm gesteuertes Abfragen des Indexes</span><span class="sxs-lookup"><span data-stu-id="0b0b7-200">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="0b0b7-201">Verwenden von SQL-und AQS-Ansätzen zum Abfragen des Indexes</span><span class="sxs-lookup"><span data-stu-id="0b0b7-201">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="0b0b7-202">Abfragen des Indexes mit dem Search-MS-Protokoll</span><span class="sxs-lookup"><span data-stu-id="0b0b7-202">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="0b0b7-203">Abfragen des Indexes mit der SQL-Syntax von Windows Search</span><span class="sxs-lookup"><span data-stu-id="0b0b7-203">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="0b0b7-204">Programm gesteuertes verwenden der erweiterten Abfrage Syntax</span><span class="sxs-lookup"><span data-stu-id="0b0b7-204">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 




