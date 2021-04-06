---
title: Paging mit idirector ysearch
description: Paging gibt an, wie viele Zeilen der Server an den Client zurückgibt.
ms.assetid: cf4aa56a-c6f7-47c8-956d-512a5cffbf22
ms.tgt_platform: multiple
keywords:
- Paging mit idirector ysearch ADSI
- ADSI, Search, idirector ysearch, andere Suchoptionen, Paging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e9fdf001f5908f6c3fc7321c8c94cda09f1b96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947336"
---
# <a name="paging-with-idirectorysearch"></a><span data-ttu-id="85b6c-105">Paging mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="85b6c-105">Paging with IDirectorySearch</span></span>

<span data-ttu-id="85b6c-106">Paging gibt an, wie viele Zeilen der Server an den Client zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="85b6c-106">Paging specifies how many rows that the server returns to the client.</span></span> <span data-ttu-id="85b6c-107">Eine Seite kann durch die Anzahl von Zeilen oder ein Zeitlimit definiert werden.</span><span class="sxs-lookup"><span data-stu-id="85b6c-107">A page can be defined by the number of rows or a time limit.</span></span> <span data-ttu-id="85b6c-108">Das ADSI COM-Objekt ruft jede Ergebnisseite auf Grundlage der in der folgenden Tabelle aufgeführten Werte ab.</span><span class="sxs-lookup"><span data-stu-id="85b6c-108">The ADSI COM object retrieves each page of results based on the values listed in the following table.</span></span> <span data-ttu-id="85b6c-109">Der Aufrufer ruft [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) auf, wenn er das Seiten Ende erreicht hat, und das ADSI COM-Objekt ruft die nächste Seite ab.</span><span class="sxs-lookup"><span data-stu-id="85b6c-109">The caller calls [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) when it has reached the page end, and the ADSI COM object retrieves the next page.</span></span>



| <span data-ttu-id="85b6c-110">Wert</span><span class="sxs-lookup"><span data-stu-id="85b6c-110">Value</span></span>                                   | <span data-ttu-id="85b6c-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85b6c-111">Description</span></span>                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85b6c-112">**Anzeigen von \_ searchpref \_ Page Size**</span><span class="sxs-lookup"><span data-stu-id="85b6c-112">**ADS\_SEARCHPREF\_PAGESIZE**</span></span>           | <span data-ttu-id="85b6c-113">Gibt die maximale Anzahl von Zeilen an, die auf einer Seite zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85b6c-113">Specifies the maximum number of rows to return in a page.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="85b6c-114">**Auslagerungszeit- \_ \_ \_ \_ Limit für Werbeeinblendungen**</span><span class="sxs-lookup"><span data-stu-id="85b6c-114">**ADS\_SEARCHPREF\_PAGED\_TIME\_LIMIT**</span></span> | <span data-ttu-id="85b6c-115">Gibt die maximale Zeit in Sekunden an, die der Server zum Sammeln einer Ergebnisseite aufwenden soll, bevor die Seite an den Client zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="85b6c-115">Specifies the maximum time, in seconds, that the server should spend collecting a page of results before returning the page to the client.</span></span> <span data-ttu-id="85b6c-116">Wenn der Grenzwert erreicht wird, beendet der Server die Suche und gibt die bereits für die Seite abgerufenen Zeilen zurück.</span><span class="sxs-lookup"><span data-stu-id="85b6c-116">If the limit is reached, the server stops the search and returns the rows already retrieved for the page.</span></span> |



 

<span data-ttu-id="85b6c-117">Wenn keine dieser Sucheinstellungen festgelegt ist, ist der Standardwert kein Paging.</span><span class="sxs-lookup"><span data-stu-id="85b6c-117">If neither of these search preferences is set, the default is no paging.</span></span> <span data-ttu-id="85b6c-118">Suchen der Active Directory, die ohne Paging ausgeführt werden, sind auf die Rückgabe von maximal den ersten 1000 Datensätzen beschränkt. Daher müssen Sie eine seitenweise Suche verwenden, wenn die Möglichkeit besteht, dass das Resultset mehr als 1000 Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="85b6c-118">Searches of the Active Directory performed without paging are limited to returning a maximum of the first 1000 records, so you must use a paged search if there is the possibility that the result set will contain more than 1000 items.</span></span>

<span data-ttu-id="85b6c-119">Ein Suchvorgang kann dazu führen, dass eine große Anzahl von Objekten zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="85b6c-119">A search operation may result in a large number of objects being returned.</span></span> <span data-ttu-id="85b6c-120">Wenn der Server das Ergebnis in einem Satz zurückgibt, kann dies die Leistung des Clients und des Servers verringern und die Netzwerk Auslastung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="85b6c-120">If the server returns the result in one set, it could decrease the performance of the client and server, as well as affect the network load.</span></span> <span data-ttu-id="85b6c-121">Eine auslagerbare Suche kann verwendet werden, um dies zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="85b6c-121">Paged searches can be used to prevent this.</span></span> <span data-ttu-id="85b6c-122">In einer auslagerenen Suche kann der Client Ergebnisse in kleineren Paketen akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="85b6c-122">In a paged search, the client can accept results in smaller packets.</span></span> <span data-ttu-id="85b6c-123">Die Größe eines Pakets wird als Suchseiten Größe bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="85b6c-123">The size of a packet is known as the search page size.</span></span>

<span data-ttu-id="85b6c-124">Auslagerbare Suchvorgänge bieten sowohl dem Client als auch dem Server Vorteile.</span><span class="sxs-lookup"><span data-stu-id="85b6c-124">Paged searches offer benefits to both the client and the server.</span></span> <span data-ttu-id="85b6c-125">Der Client kann bei der Darstellung der Ergebnisse für Benutzer reaktionsfähiger sein.</span><span class="sxs-lookup"><span data-stu-id="85b6c-125">The client can be more responsive in presenting the results to users.</span></span> <span data-ttu-id="85b6c-126">Dies ist besonders wichtig für grafische Benutzeroberflächen Tools, die den Fenster Anzeige Prozess starten können, während der andere Thread gleichzeitig die Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="85b6c-126">This is especially relevant to graphical user interface tools that can begin the window display process while the other thread concurrently receives the data.</span></span>

<span data-ttu-id="85b6c-127">Auf Serverseite wird der Vorgang durch seitenweise Suchen skalierbar.</span><span class="sxs-lookup"><span data-stu-id="85b6c-127">On the server side, paged searches make the operation scalable.</span></span> <span data-ttu-id="85b6c-128">Wenn z. b. 100 Clients Suchanforderungen gleichzeitig ausgeben und im Durchschnitt jeder Client 200 Objekte empfängt.</span><span class="sxs-lookup"><span data-stu-id="85b6c-128">For example, if one hundred clients issue search requests simultaneously and, on the average, each client receives two hundred objects.</span></span> <span data-ttu-id="85b6c-129">Wenn keine Seitengröße angegeben ist, muss der Server im ungünstigsten Fall über ausreichend Arbeitsspeicher verfügen, um 20.000 Objekte zu speichern.</span><span class="sxs-lookup"><span data-stu-id="85b6c-129">If no page size is specified, in the worst-case scenario, the server must have sufficient memory to hold 20,000 objects.</span></span> <span data-ttu-id="85b6c-130">Wenn hingegen jeder Client eine Seitengröße angibt (z. b. zehn Objekte), wird die Arbeitsspeicher Anforderung auf dem Server um den Faktor 20 reduziert.</span><span class="sxs-lookup"><span data-stu-id="85b6c-130">Conversely, if each client specifies a page size to be, for example, ten objects, the memory requirement on the server is thus reduced by a factor of 20.</span></span>

<span data-ttu-id="85b6c-131">Außerdem kann ein Client mit einer auslagerungssuche den Vorgang abbrechen, der gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85b6c-131">In addition, using a paged search, a client can abandon the operation in progress.</span></span> <span data-ttu-id="85b6c-132">Im Gegensatz dazu empfängt der Client in einer nicht Auslagerungs Suche ein Resultset in einem Paket.</span><span class="sxs-lookup"><span data-stu-id="85b6c-132">In contrast, in a non-paged search, the client receives a result set in one packet.</span></span> <span data-ttu-id="85b6c-133">Dadurch kann die Netzwerkleistung verringert werden.</span><span class="sxs-lookup"><span data-stu-id="85b6c-133">This can decrease network performance.</span></span>

<span data-ttu-id="85b6c-134">ADSI behandelt die Seitengröße für den Client.</span><span class="sxs-lookup"><span data-stu-id="85b6c-134">ADSI handles the page size for the client.</span></span> <span data-ttu-id="85b6c-135">Der Client muss die Anzahl der aktuell ausgeführten Objekte nicht zählen.</span><span class="sxs-lookup"><span data-stu-id="85b6c-135">The client does not have to count the number of objects in progress.</span></span> <span data-ttu-id="85b6c-136">ADSI kapselt die Server Interaktion für den Client.</span><span class="sxs-lookup"><span data-stu-id="85b6c-136">ADSI encapsulates the server interaction for the client.</span></span> <span data-ttu-id="85b6c-137">Aus Sicht des Clients gibt die Suche ein umfassendes Resultset zurück.</span><span class="sxs-lookup"><span data-stu-id="85b6c-137">From the client perspective, the search returns a complete result set.</span></span>

<span data-ttu-id="85b6c-138">Es wird empfohlen, Paging zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="85b6c-138">It is recommended that paging is used.</span></span>

<span data-ttu-id="85b6c-139">Wenn Sie eine maximale Seitengröße angeben möchten, legen Sie die Suchoption **ADS \_ searchpref \_ PageSize** mit einem **\_ ganzzahligen adstype** -Wert fest, der auf die maximale Anzahl von Zeilen pro Seite in dem an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode über gebenden ADS festgelegt ist. [**\_ \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)</span><span class="sxs-lookup"><span data-stu-id="85b6c-139">To specify a maximum page size, set an **ADS\_SEARCHPREF\_PAGESIZE** search option with an **ADSTYPE\_INTEGER** value set to the maximum number of rows per page in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="85b6c-140">Im folgenden Codebeispiel wird gezeigt, wie die maximale Seitengröße festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="85b6c-140">The following code example shows how to set the maximum page size.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



<span data-ttu-id="85b6c-141">Um einen Seiten Zeitraum anzugeben, legen Sie die Suchoption für das Auslagerungs **\_ \_ \_ Zeit \_ Limit für Werbe** Einblendungen auf einen Wert vom Typ " **adstype \_** " fest, der auf die maximale Anzahl von Sekunden festgelegt ist, die der Server für das Abrufen einer Seite im [**ADS- \_ \_ infoarray**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) mit der [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode aufwenden soll.</span><span class="sxs-lookup"><span data-stu-id="85b6c-141">To specify a page time, set an **ADS\_SEARCHPREF\_PAGED\_TIME\_LIMIT** search option with an **ADSTYPE\_INTEGER** value set to the maximum number of seconds that the server should spend retrieving a page in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="85b6c-142">Im folgenden Codebeispiel wird gezeigt, wie die Seiten Zeit angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="85b6c-142">The following code example shows how to specify page time.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




