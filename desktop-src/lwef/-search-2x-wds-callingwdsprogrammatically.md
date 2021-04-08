---
title: Programm gesteuertes Aufrufen von WDS
description: Die Microsoft Windows-Desktop Suche (WDS) 2. x kann Programm gesteuert mithilfe der executeQuery-Methode und der ExecuteSQLQuery-Methode in der ISearchDesktop-Schnittstelle abgefragt werden.
ms.assetid: 38426f63-2039-410e-8c70-ebd9fc269d74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc76264b7939311273fbda334292dfb255cde8f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727049"
---
# <a name="calling-wds-programmatically"></a><span data-ttu-id="cc034-103">Programm gesteuertes Aufrufen von WDS</span><span class="sxs-lookup"><span data-stu-id="cc034-103">Calling WDS Programmatically</span></span>

> [!NOTE]
> <span data-ttu-id="cc034-104">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="cc034-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="cc034-105">Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="cc034-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="cc034-106">Die Microsoft Windows-Desktop Suche (WDS) 2. x kann Programm gesteuert mithilfe der **ExecuteQuery** -Methode und der **ExecuteSQLQuery** -Methode in der [**ISearchDesktop-**](/previous-versions//aa965729(v=vs.85)) Schnittstelle abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="cc034-106">Microsoft Windows Desktop Search (WDS) 2.x can be queried programmatically using the **ExecuteQuery** and **ExecuteSQLQuery** methods in the [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) interface.</span></span> <span data-ttu-id="cc034-107">Die **ExecuteQuery** -Methode gibt basierend auf dem Abfragetext, den Spalten und den Einschränkungen, die als Parameter übergeben werden, einen Daten Satz Satz aus dem Index zurück.</span><span class="sxs-lookup"><span data-stu-id="cc034-107">The **ExecuteQuery** method returns a record set from the index based on the query text, columns, and restrictions passed as parameters.</span></span> <span data-ttu-id="cc034-108">Die **ExecuteSQLQuery** -Methode gibt auch einen Datensatz-Satz von Ergebnissen zurück, erfordert jedoch den genauen Structured Query Language (SQL)-Befehl, der übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc034-108">The **ExecuteSQLQuery** method also returns a record set of results but requires the exact Structured Query Language (SQL) command to be passed in.</span></span> <span data-ttu-id="cc034-109">**ExecuteQuery** sollte in den meisten Szenarien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc034-109">**ExecuteQuery** should be used in most scenarios.</span></span>

## <a name="regular-queries"></a><span data-ttu-id="cc034-110">Reguläre Abfragen</span><span class="sxs-lookup"><span data-stu-id="cc034-110">Regular Queries</span></span>

<span data-ttu-id="cc034-111">Reguläre Abfragen sind solche, die vom Benutzer in das WDS-Eingabefeld eingegeben werden, einschließlich der [erweiterten Abfrage Syntax](-search-2x-wds-aqsreference.md).</span><span class="sxs-lookup"><span data-stu-id="cc034-111">Regular queries are those typed into the WDS input box by the user including all [Advanced Query Syntax](-search-2x-wds-aqsreference.md).</span></span> <span data-ttu-id="cc034-112">Die Abfrage wird zusammen mit den zurück zugebende WDS 2. x- [Schema](-search-2x-wds-schematable.md) Spalten, der Spalte und der Reihenfolge zum Sortieren von Ergebnissen an **ExecuteQuery** und in allen Klauseln zur Einschränkung der Ergebnisse von übergeben.</span><span class="sxs-lookup"><span data-stu-id="cc034-112">The query is passed to **ExecuteQuery** along with the WDS 2.x [schema](-search-2x-wds-schematable.md) columns to return, the column and order to sort results, and any clauses to restrict results by.</span></span>

<span data-ttu-id="cc034-113">Die-Methode weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="cc034-113">The method has the form:</span></span>

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| <span data-ttu-id="cc034-114">Richtung</span><span class="sxs-lookup"><span data-stu-id="cc034-114">Direction</span></span> | <span data-ttu-id="cc034-115">Variable</span><span class="sxs-lookup"><span data-stu-id="cc034-115">Variable</span></span>           | <span data-ttu-id="cc034-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc034-116">Description</span></span>                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc034-117">In</span><span class="sxs-lookup"><span data-stu-id="cc034-117">In</span></span>        | <span data-ttu-id="cc034-118">lpcwstrinquery</span><span class="sxs-lookup"><span data-stu-id="cc034-118">lpcwstrQuery</span></span>       | <span data-ttu-id="cc034-119">Der Abfragetext.</span><span class="sxs-lookup"><span data-stu-id="cc034-119">The query text.</span></span> <span data-ttu-id="cc034-120">Diese Abfrage ist identisch mit einer Abfrage, die in das Such Textfeld in der Benutzeroberfläche der Windows-Desktop Suche eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="cc034-120">This query is the same as a query typed into the search text box in the Windows Desktop Search user interface.</span></span> <br/> <span data-ttu-id="cc034-121">Beispiel: `"from:Zara dinner plans"`</span><span class="sxs-lookup"><span data-stu-id="cc034-121">For example: `"from:Zara dinner plans"`</span></span><br/> |
| <span data-ttu-id="cc034-122">In</span><span class="sxs-lookup"><span data-stu-id="cc034-122">In</span></span>        | <span data-ttu-id="cc034-123">lpcwstrincolumn</span><span class="sxs-lookup"><span data-stu-id="cc034-123">lpcwstrColumn</span></span>      | <span data-ttu-id="cc034-124">Die einzuschließenden Spalten, getrennt durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="cc034-124">The columns to include, separated by commas.</span></span> <br/> <span data-ttu-id="cc034-125">Beispiel: `"DocTitle, Url"`</span><span class="sxs-lookup"><span data-stu-id="cc034-125">For example: `"DocTitle, Url"`</span></span><br/>                                                                                            |
| <span data-ttu-id="cc034-126">In</span><span class="sxs-lookup"><span data-stu-id="cc034-126">In</span></span>        | <span data-ttu-id="cc034-127">lpcwstrausort</span><span class="sxs-lookup"><span data-stu-id="cc034-127">lpcwstrSort</span></span>        | <span data-ttu-id="cc034-128">Die zu sortierende Überschreibungs Spalte, gefolgt von ASC für aufsteigend oder absteigend für absteigend.</span><span class="sxs-lookup"><span data-stu-id="cc034-128">The Override Column to sort by followed by ASC for ascending or DESC for descending.</span></span> <br/> <span data-ttu-id="cc034-129">Beispiel: `"LastAuthor DESC"`</span><span class="sxs-lookup"><span data-stu-id="cc034-129">For example: `"LastAuthor DESC"`</span></span><br/>                                                  |
| <span data-ttu-id="cc034-130">In</span><span class="sxs-lookup"><span data-stu-id="cc034-130">In</span></span>        | <span data-ttu-id="cc034-131">lpcwstraueinschränkung</span><span class="sxs-lookup"><span data-stu-id="cc034-131">lpcwstrRestriction</span></span> | <span data-ttu-id="cc034-132">Einschränkungen zum Anfügen von WHERE-Klauseln in der Windows-Desktop Suche wählen Sie aus.</span><span class="sxs-lookup"><span data-stu-id="cc034-132">Restrictions to append through WHERE clauses in the Windows Desktop Search select.</span></span> <br/> <span data-ttu-id="cc034-133">Beispiel: `"Contains(LastAuthor, 'Bill')"`</span><span class="sxs-lookup"><span data-stu-id="cc034-133">For example: `"Contains(LastAuthor, 'Bill')"`</span></span><br/>                                       |
| <span data-ttu-id="cc034-134">aus</span><span class="sxs-lookup"><span data-stu-id="cc034-134">Out</span></span>       | <span data-ttu-id="cc034-135">ppirs</span><span class="sxs-lookup"><span data-stu-id="cc034-135">ppiRs</span></span>              | <span data-ttu-id="cc034-136">Der resultierende Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="cc034-136">The resulting record set</span></span><br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a><span data-ttu-id="cc034-137">SQL-Abfragen</span><span class="sxs-lookup"><span data-stu-id="cc034-137">SQL Queries</span></span>

<span data-ttu-id="cc034-138">Die **ISearchDesktop.Executesqlquery** -Methode wird verwendet, um direkte WDS-Datenbankabfragen zu senden.</span><span class="sxs-lookup"><span data-stu-id="cc034-138">The **ISearchDesktop.ExecuteSQLQuery** method is used to send direct WDS database queries.</span></span> <span data-ttu-id="cc034-139">Die Syntax für die Abfragen ähnelt der für SharePoint Server verwendeten, zusammen mit der Möglichkeit, SQL GROUP BY-Klauseln im Monarch-Stil zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc034-139">The syntax for the queries is similar to that used for SharePoint Server, along with the ability to use Monarch-style SQL GROUP BY clauses.</span></span> <span data-ttu-id="cc034-140">Die Abfrage wird für den Index genau so ausgeführt, wie Sie übergeben wird, ohne dass eine zusätzliche Verarbeitung der erweiterten Abfrage Syntax erfolgt, wie die ExecuteQuery-API dies tut.</span><span class="sxs-lookup"><span data-stu-id="cc034-140">The query is executed against the index exactly as it is passed in with no additional processing of Advanced Query Syntax as the ExecuteQuery API does.</span></span>

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

<span data-ttu-id="cc034-141">Die-Methode weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="cc034-141">The method has the form:</span></span>

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| <span data-ttu-id="cc034-142">Richtung</span><span class="sxs-lookup"><span data-stu-id="cc034-142">Direction</span></span> | <span data-ttu-id="cc034-143">Variable</span><span class="sxs-lookup"><span data-stu-id="cc034-143">Variable</span></span>   | <span data-ttu-id="cc034-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc034-144">Description</span></span>                                    |
|-----------|------------|------------------------------------------------|
| <span data-ttu-id="cc034-145">In</span><span class="sxs-lookup"><span data-stu-id="cc034-145">In</span></span>        | <span data-ttu-id="cc034-146">lpcwstrausql</span><span class="sxs-lookup"><span data-stu-id="cc034-146">lpcwstrSQL</span></span> | <span data-ttu-id="cc034-147">Die SQL-Abfrage, die für den WDS-Index ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc034-147">The SQL query to execute against the WDS index</span></span> |
| <span data-ttu-id="cc034-148">aus</span><span class="sxs-lookup"><span data-stu-id="cc034-148">Out</span></span>       | <span data-ttu-id="cc034-149">ppirs</span><span class="sxs-lookup"><span data-stu-id="cc034-149">ppiRs</span></span>      | <span data-ttu-id="cc034-150">Der resultierende Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="cc034-150">The resulting record set</span></span>                       |



 

<span data-ttu-id="cc034-151">Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="cc034-151">Resources:</span></span>

-   <span data-ttu-id="cc034-152">Unterstützungs Dateien für die ISearchDesktop-Schnittstelle: https://addins.msn.com/support/WDSSDK.zip</span><span class="sxs-lookup"><span data-stu-id="cc034-152">Support files for the ISearchDesktop interface: https://addins.msn.com/support/WDSSDK.zip</span></span>
-   <span data-ttu-id="cc034-153">ISearchDesktop c#-Beispiel: https://addins.msn.com/support/WDSSample.zip</span><span class="sxs-lookup"><span data-stu-id="cc034-153">ISearchDesktop C# Sample: https://addins.msn.com/support/WDSSample.zip</span></span>

## <a name="sample-c-code"></a><span data-ttu-id="cc034-154">Beispiel C++ Code</span><span class="sxs-lookup"><span data-stu-id="cc034-154">Sample C++ Code</span></span>

> [!Note]
>
> <span data-ttu-id="cc034-155">Dieser Code und diese Informationen werden "wie immer" bereitgestellt, ohne jegliche Gewährleistungen jeglicher Art, entweder ausgedrückt oder impliziert, einschließlich, aber nicht beschränkt auf die impliziten Gewährleistungen der Handels Üblichkeit und/oder Eignung für einen bestimmten Zweck.</span><span class="sxs-lookup"><span data-stu-id="cc034-155">THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE.</span></span>
>
> <span data-ttu-id="cc034-156">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cc034-156">Copyright (C) Microsoft.</span></span> <span data-ttu-id="cc034-157">Alle Rechte vorbehalten.</span><span class="sxs-lookup"><span data-stu-id="cc034-157">All rights reserved.</span></span>

 


```
#include <stdio.h>
#include <wchar.h>
#include <windows.h>
#include <msnldl.h>
#include <adoint.h>
#include <adoguids.h>
 
HRESULT TestExecuteQuery(ISearchDesktop *psd)
{
ADORecordset *prs = NULL;
 
    HRESULT hr;
 
    hr = psd->ExecuteQuery( L"ToName:Moishe", 
                            L"DocTitle,DocFormat", 
                            L"PrimaryDate DESC", 
                            L"Contains('text')", 
                            &prs);
    if (SUCCEEDED(hr))
        prs->Release();
    return hr;
}
 
HRESULT TestExecuteSQLQuery(ISearchDesktop *psd)
{
    ADORecordset *prs = NULL;
    HRESULT hr;

    hr = psd->ExecuteSQLQuery(L"select DocTitle from MyIndex..Scope() where contains('text')", &prs);

    if (SUCCEEDED(hr))
      prs->Release();
    return hr;
}
 
extern "C" int __cdecl wmain( int argc, WCHAR * argv[] )
{
    SCODE sc = CoInitialize(0);
    ISearchDesktop *psd = NULL;
    HRESULT         hr;
     
    if (SUCCEEDED(hr = CoCreateInstance(__uuidof(SearchDesktop), NULL, CLSCTX_INPROC_SERVER, 
                                        __uuidof(ISearchDesktop), (void**)&psd)))
          {
             TestExecuteSQLQuery(psd);
             TestExecuteQuery(psd);
             psd->Release();
          }
          CoUninitialize();
}
```



## <a name="related-topics"></a><span data-ttu-id="cc034-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cc034-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="cc034-159">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="cc034-159">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cc034-160">Erweiterte Abfragesyntax</span><span class="sxs-lookup"><span data-stu-id="cc034-160">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="cc034-161">Wahrgenommene Typen</span><span class="sxs-lookup"><span data-stu-id="cc034-161">Perceived Types</span></span>](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[<span data-ttu-id="cc034-162">Aufrufen von WDS von Webseiten</span><span class="sxs-lookup"><span data-stu-id="cc034-162">Calling WDS from Web Pages</span></span>](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

