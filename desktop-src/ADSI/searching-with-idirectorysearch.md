---
title: Suchen mit der idirector ysearch-Schnittstelle
description: Die idirector ysearch-Schnittstelle bietet eine Oberfläche mit geringem Verwaltungsaufwand zum Abfragen von Daten eines Verzeichnisses oder eines globalen Katalogs.
ms.assetid: da415cb2-f320-4be4-b5bd-053cd6a6b2fd
ms.tgt_platform: multiple
keywords:
- Suchen mit der idirector ysearch-Schnittstelle ADSI
- Abfragen von ADSI, Abfrageschnittstellen, idirecterysearch
- ADSI ADSI, Beispiel Code C/C++, Suchen eines Verzeichnisses mit idirector ysearch
- Idirectoriysearch ADSI, Verwendung von zum Durchsuchen eines Verzeichnisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2738e163f672fb0000275e2fb9d885442ae6693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858479"
---
# <a name="searching-with-the-idirectorysearch-interface"></a><span data-ttu-id="e80d9-107">Suchen mit der idirector ysearch-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e80d9-107">Searching with the IDirectorySearch Interface</span></span>

<span data-ttu-id="e80d9-108">Die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle bietet eine Oberfläche mit geringem Verwaltungsaufwand zum Abfragen von Daten eines Verzeichnisses oder eines globalen Katalogs.</span><span class="sxs-lookup"><span data-stu-id="e80d9-108">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provides a high-level and low-overhead interface for querying data of a directory or a global catalog.</span></span> <span data-ttu-id="e80d9-109">Die **idirector ysearch** -com-Schnittstelle kann nur mit einer Vtable verwendet werden und ist daher für Automatisierungs basierte Entwicklungsumgebungen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e80d9-109">The **IDirectorySearch** COM interface can be used only with a vtable, and thus, is not available to Automation-based development environments.</span></span>

<span data-ttu-id="e80d9-110">**So führen Sie eine Suche aus**</span><span class="sxs-lookup"><span data-stu-id="e80d9-110">**To perform a search**</span></span>

1.  <span data-ttu-id="e80d9-111">Binden an ein Objekt im Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="e80d9-111">Bind to an object in the directory.</span></span>
2.  <span data-ttu-id="e80d9-112">Ruft [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, um den [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Zeiger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e80d9-112">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pointer.</span></span>
3.  <span data-ttu-id="e80d9-113">Führen Sie die Suche mithilfe des [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Zeigers aus.</span><span class="sxs-lookup"><span data-stu-id="e80d9-113">Run the search using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pointer.</span></span> <span data-ttu-id="e80d9-114">Nennen Sie die [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) -Methode, und übergeben Sie einen Suchfilter, die angeforderten Attributnamen und andere Parameter.</span><span class="sxs-lookup"><span data-stu-id="e80d9-114">Call the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method, and pass a search filter, the requested attribute names, and other parameters.</span></span>

<span data-ttu-id="e80d9-115">Weitere Informationen zur Suchfilter Syntax finden Sie unter [Syntax für Suchfilter](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e80d9-115">For more information about the search filter syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

<span data-ttu-id="e80d9-116">Die Abfrage Ausführung ist Anbieter spezifisch.</span><span class="sxs-lookup"><span data-stu-id="e80d9-116">Query execution is provider-specific.</span></span> <span data-ttu-id="e80d9-117">Bei manchen Anbietern findet die tatsächliche Abfrage Ausführung erst statt, wenn " [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) " oder " [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e80d9-117">With some providers, the actual query execution does not occur until [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) is called.</span></span> <span data-ttu-id="e80d9-118">Die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle funktioniert direkt mit Suchfiltern.</span><span class="sxs-lookup"><span data-stu-id="e80d9-118">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface works with search filters directly.</span></span> <span data-ttu-id="e80d9-119">Weder der SQL-Dialekt noch der LDAP-Dialekt ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e80d9-119">Neither the SQL dialect nor the LDAP dialect are required.</span></span>

<span data-ttu-id="e80d9-120">Die [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle stellt Methoden bereit, um das Resultset zeilenweise aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="e80d9-120">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provides methods to enumerate the result set, row by row.</span></span> <span data-ttu-id="e80d9-121">Die [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) -Methode ruft die erste Zeile ab, und [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) wechselt zur nächsten Zeile aus der aktuellen Zeile.</span><span class="sxs-lookup"><span data-stu-id="e80d9-121">The [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) method retrieves the first row and [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) moves you to the next row from the current row.</span></span> <span data-ttu-id="e80d9-122">Wenn Sie die letzte Zeile erreicht haben, gibt der Aufruf dieser Methoden den \_ Fehlercode der S ADS \_ nomore- \_ Zeilen zurück.</span><span class="sxs-lookup"><span data-stu-id="e80d9-122">When you have reached the last row, calling these methods returns the S\_ADS\_NOMORE\_ROWS error code.</span></span> <span data-ttu-id="e80d9-123">Umgekehrt verschiebt [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) Sie jeweils eine Zeile zurück.</span><span class="sxs-lookup"><span data-stu-id="e80d9-123">Conversely, [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) moves you back one row at a time.</span></span> <span data-ttu-id="e80d9-124">Ein S \_ ADS \_ nomore \_ Rows-Rückgabewert gibt an, dass Sie die erste Zeile des Resultsets erreicht haben.</span><span class="sxs-lookup"><span data-stu-id="e80d9-124">An S\_ADS\_NOMORE\_ROWS return value indicates that you have reached the first row of the result set.</span></span> <span data-ttu-id="e80d9-125">Diese Methoden arbeiten mit dem Resultset, das im Arbeitsspeicher ansässig ist, auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="e80d9-125">These methods operate on the result set, resident in memory, on the client.</span></span> <span data-ttu-id="e80d9-126">Wenn also auslagerbare und asynchrone Suchvorgänge ausgeführt werden und \_ die \_ Option Cache Ergebnisse deaktiviert ist, kann der rückwärts Bildlauf unerwartete Folgen haben.</span><span class="sxs-lookup"><span data-stu-id="e80d9-126">Thus, when paged and asynchronous searches are performed and the \_CACHE\_RESULTS option is turned off, backward scrolling can have unexpected consequences.</span></span>

<span data-ttu-id="e80d9-127">Wenn Sie die entsprechende Zeile gefunden haben, rufen Sie [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) auf, um Datenelemente, Spalte nach Spalte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e80d9-127">When you have located the appropriate row, call [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) to obtain data items, column by column.</span></span> <span data-ttu-id="e80d9-128">Für jeden-Befehl übergeben Sie den Namen der Spalte, die von Interesse ist.</span><span class="sxs-lookup"><span data-stu-id="e80d9-128">For each call, you pass the name of the column of interest.</span></span> <span data-ttu-id="e80d9-129">Das zurückgegebene Datenelement ist ein Zeiger auf eine [**ADS- \_ Such \_ Spalten**](/windows/desktop/api/Iads/ns-iads-ads_search_column) Struktur.</span><span class="sxs-lookup"><span data-stu-id="e80d9-129">The data item returned is a pointer to an [**ADS\_SEARCH\_COLUMN**](/windows/desktop/api/Iads/ns-iads-ads_search_column) structure.</span></span> <span data-ttu-id="e80d9-130">**GetColumn** ordnet Ihnen diese Struktur zu, Sie müssen Sie jedoch mit [**freecolum**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn)freigeben.</span><span class="sxs-lookup"><span data-stu-id="e80d9-130">**GetColumn** allocates this structure for you, but you must free it using [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn).</span></span> <span data-ttu-id="e80d9-131">Ruft [**closesearchhandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) auf, um den Suchvorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e80d9-131">Call [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) to complete the search operation.</span></span>

<span data-ttu-id="e80d9-132">**So führen Sie eine Verzeichnis Suche aus**</span><span class="sxs-lookup"><span data-stu-id="e80d9-132">**To perform a directory search**</span></span>

1.  <span data-ttu-id="e80d9-133">Binden an einen LDAP-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="e80d9-133">Bind to an LDAP provider.</span></span> <span data-ttu-id="e80d9-134">Dabei kann es sich um einen Domänen Controller oder einen globalen Katalog Anbieter handeln.</span><span class="sxs-lookup"><span data-stu-id="e80d9-134">It may be a domain controller or a global catalog provider.</span></span>
2.  <span data-ttu-id="e80d9-135">Rufen Sie die [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -com-Schnittstelle mit einem Aufrufen von [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); ab. Dieser Vorgang wurde möglicherweise in Schritt 1 während der ersten Bindung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e80d9-135">Retrieve the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) COM Interface with a call to [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); this operation may have been done in Step 1 during the initial binding.</span></span>

    <span data-ttu-id="e80d9-136">Optional können Sie [**setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) aufrufen, um Optionen für die Behandlung der Ergebnisse Ihrer Suche auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="e80d9-136">Optionally, call [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) to select options for handling the results of your search.</span></span>

3.  <span data-ttu-id="e80d9-137">" [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch)" aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e80d9-137">Call [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).</span></span> <span data-ttu-id="e80d9-138">Abhängig von den in [**setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) festgelegten Optionen kann dies die Ausführung der Abfrage starten.</span><span class="sxs-lookup"><span data-stu-id="e80d9-138">Depending on the options set in [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) this may, or may not, begin query execution.</span></span>
4.  <span data-ttu-id="e80d9-139">Aufrufen von [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) , um den Zeilen Index (intern zu [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) in die erste Zeile zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="e80d9-139">Call [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) to move the row index (internal to [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) to the first row.</span></span>
5.  <span data-ttu-id="e80d9-140">Lesen Sie die Daten mithilfe von [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn)aus der Zeile, und geben Sie dann [**freecolumschlag**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) ein, um den von **GetColumn** belegten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="e80d9-140">Read the data from the row using [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn), then call [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) to release the memory allocated by **GetColumn**.</span></span>
6.  <span data-ttu-id="e80d9-141">Wiederholen Sie Schritt 5, bis alle Daten aus dem Suchergebnis abgerufen wurden oder [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) S \_ ADS \_ nomore \_ Rows zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e80d9-141">Repeat Step 5 until all data is retrieved from the search result, or until [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) returns S\_ADS\_NOMORE\_ROWS.</span></span>
7.  <span data-ttu-id="e80d9-142">Wenden Sie nach Abschluss des Vorgangs [**abandonsearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) und [**closesearchhandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) an.</span><span class="sxs-lookup"><span data-stu-id="e80d9-142">Call [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) and [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) when complete.</span></span>

<span data-ttu-id="e80d9-143">Das folgende Codebeispiel zeigt dieses Szenario.</span><span class="sxs-lookup"><span data-stu-id="e80d9-143">The following code example shows this scenario.</span></span> <span data-ttu-id="e80d9-144">Um mit der Bindung an ADSI zu beginnen, müssen Sie die [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e80d9-144">To start binding to ADSI, call the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>


```C++
HRESULT hr = S_OK; // COM result variable
ADS_SEARCH_COLUMN col;  // COL for iterations
LPWSTR szUsername = NULL; // user name
LPWSTR szPassword = NULL; // password
 
// Interface Pointers.
IDirectorySearch     *pDSSearch    =NULL;
 
// Initialize COM.
CoInitialize(0);

// Add code to securely retrieve the user name and password or
// leave both as NULL to use the default security context.
 
// Open a connection with server.
hr = ADsOpenObject(L"LDAP://coho.salmon.Fabrikam.com", 
szUsername,
szPassword,
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



<span data-ttu-id="e80d9-145">Dadurch wird ein Zeiger auf die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e80d9-145">This provides a pointer to the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

<span data-ttu-id="e80d9-146">Da nun eine COM-Schnittstelle für eine idirectoryinterface-Instanz vorhanden ist, müssen Sie [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e80d9-146">Now that there is a COM interface for an IDirectoryInterface instance, call [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).</span></span>

<span data-ttu-id="e80d9-147">Erstellen Sie ein Array von Attributnamen, die sich auf den Abruf der [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) -Funktion vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="e80d9-147">Build an array of attribute names to prepare to call the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) function.</span></span> <span data-ttu-id="e80d9-148">Die Attributnamen werden innerhalb des Active Directory Schema definiert.</span><span class="sxs-lookup"><span data-stu-id="e80d9-148">The attribute names are defined within the schema of Active Directory.</span></span> <span data-ttu-id="e80d9-149">Weitere Informationen zur Schema Definition finden Sie unter [ADSI-Schema Modell](adsi-schema-model.md).</span><span class="sxs-lookup"><span data-stu-id="e80d9-149">For more information about the schema definition, see [ADSI Schema Model](adsi-schema-model.md).</span></span> <span data-ttu-id="e80d9-150">Die aufgelisteten Attributnamen werden zurückgegeben, wenn Sie vom-Objekt als Resultset der Suche unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e80d9-150">The attribute names listed are returned, if supported by the object, as the result set of the search.</span></span>


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



<span data-ttu-id="e80d9-151">Nennen Sie nun die [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e80d9-151">Now, call the [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) function.</span></span> <span data-ttu-id="e80d9-152">Die Suche wird erst ausgeführt, wenn Sie die [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e80d9-152">The search does not run until you call the [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) method.</span></span>


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



<span data-ttu-id="e80d9-153">Aufrufen von [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) zum Durchlaufen von Zeilen im Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="e80d9-153">Call [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) to iterate rows in the result.</span></span> <span data-ttu-id="e80d9-154">Jede Zeile wird dann nach dem Attribut "Description" abgefragt.</span><span class="sxs-lookup"><span data-stu-id="e80d9-154">Each row is then queried for the "description" attribute.</span></span> <span data-ttu-id="e80d9-155">Wenn das Attribut gefunden wird, wird es angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e80d9-155">If the attribute is found, it is displayed.</span></span>


```C++
LPWSTR pszColumn;
    while( pDSSearch->GetNextRow( hSearch) != S_ADS_NOMORE_ROWS )
    {
        // Get the property.
        hr = pDSSearch->GetColumn( hSearch, L"description", &col );
 
        // If this object supports this attribute, display it.
        if ( SUCCEEDED(hr) )
        { 
           if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
              wprintf(L"The description property:%s\r\n", col.pADsValues->CaseIgnoreString); 
           pDSSearch->FreeColumn( &col );
        }
        else
            puts("description property NOT available");
        puts("------------------------------------------------");
        dwCount++;
    }
    pDSSearch->CloseSearchHandle(hSearch);
    pDSSearch->Release();
```



<span data-ttu-id="e80d9-156">Um die Suche zu beenden, wenden Sie die Methode " [**abandonsearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) " an.</span><span class="sxs-lookup"><span data-stu-id="e80d9-156">To end the search, call the [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) method.</span></span>

<span data-ttu-id="e80d9-157">Wenn eine Seitengröße nicht festgelegt ist, wird [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) so lange blockiert, bis das gesamte Resultset an den Client zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e80d9-157">Be aware that if a page size is not set, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) blocks until the entire result set is returned to the client.</span></span> <span data-ttu-id="e80d9-158">Wenn die Seitengröße festgelegt ist, wird **GetNextRow** so lange blockiert, bis die erste Seite (Seitengröße = Anzahl der Zeilen in einer Seite) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e80d9-158">If page size is set, then **GetNextRow** blocks until the first page (page size = number of rows in a page) is returned.</span></span> <span data-ttu-id="e80d9-159">Wenn die Seitengröße festgelegt ist und die Abfrage sortiert werden soll und Sie nicht nach mindestens einem indizierten Attribut suchen, wird der Wert für die Seitengröße ignoriert, und der Server berechnet das gesamte Resultset, bevor die Daten zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e80d9-159">If page size is set and the query is to be sorted and you are not searching on at least one indexed attribute, then the page size value is ignored, and the server calculates the entire result set prior to returning the data.</span></span> <span data-ttu-id="e80d9-160">Dies hat zur Folge, dass **GetNextRow** blockiert wird, bis die Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e80d9-160">This has the effect of **GetNextRow** blocking until the query completes.</span></span>

> [!Note]  
> <span data-ttu-id="e80d9-161">Um diese Abfrage von einer Verzeichnis Suche zu einer globalen Katalog Suche zu ändern, wird der [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Rückruf geändert.</span><span class="sxs-lookup"><span data-stu-id="e80d9-161">To change this query from a directory search to a global catalog search, the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) call is changed.</span></span>

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 