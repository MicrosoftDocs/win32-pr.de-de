---
title: Verwenden von IDirectorySearch und IDirectoryObject für den Bereichs Abruf
description: Mithilfe der IDirectoryObject-Schnittstelle oder der IDirectorySearch-Schnittstelle können Sie einen Bereich von Eigenschafts Werten abrufen. Geben Sie hierzu das Attribut und den Bereich für eines der in der Abfrage angeforderten Attribute an.
ms.assetid: 4d9d2a98-51d5-4326-b43e-a2ac3bc54a75
ms.tgt_platform: multiple
keywords:
- IDirectorySearch ADSI, Verwendung von für den Bereich zum Abrufen von Mitgliedern einer Gruppe
- IDirectoryObject ADSI, Verwendung von für den Bereich zum Abrufen von Mitgliedern einer Gruppe
- ADSI für Bereichs Abruf, Verwendung von IDirectorySearch und IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591d2cf7b65b7a8159a92de324f18fbe93164f0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338559"
---
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a><span data-ttu-id="0d6ae-107">Verwenden von IDirectorySearch und IDirectoryObject für den Bereichs Abruf</span><span class="sxs-lookup"><span data-stu-id="0d6ae-107">Using IDirectorySearch and IDirectoryObject for Range Retrieval</span></span>

<span data-ttu-id="0d6ae-108">Mithilfe der [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle oder der [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle können Sie einen Bereich von Eigenschafts Werten abrufen.</span><span class="sxs-lookup"><span data-stu-id="0d6ae-108">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) or [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interfaces can be used to retrieve a range of property values.</span></span> <span data-ttu-id="0d6ae-109">Geben Sie hierzu das Attribut und den Bereich für eines der in der Abfrage angeforderten Attribute an.</span><span class="sxs-lookup"><span data-stu-id="0d6ae-109">To do this, specify the attribute and range for one of the attributes requested in the query.</span></span>

## <a name="range-retrieval-with-idirectoryobject"></a><span data-ttu-id="0d6ae-110">Bereichs Abruf mit IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="0d6ae-110">Range Retrieval with IDirectoryObject</span></span>

<span data-ttu-id="0d6ae-111">Die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle kann für den Bereichs Abruf verwendet werden, indem das Attribut und der Bereich für eines der Attribute im *pattributesname* -Array angegeben werden, wenn die [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0d6ae-111">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface can be used for range retrieval by specifying the attribute and range for one of the attributes in the *pAttributesName* array when calling the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method.</span></span>


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



<span data-ttu-id="0d6ae-112">Weitere Informationen und ein Codebeispiel, das zeigt, wie die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle für den Bereichs Abruf verwendet wird, finden Sie unter [Beispielcode für den Bereich mit IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="0d6ae-112">For more information and a code example that shows how to use the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface for range retrieval, see [Example Code for Ranging with IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).</span></span>

## <a name="range-retrieval-with-idirectorysearch"></a><span data-ttu-id="0d6ae-113">Bereichs Abruf mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="0d6ae-113">Range Retrieval with IDirectorySearch</span></span>

<span data-ttu-id="0d6ae-114">Die [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle kann für den Bereichs Abruf verwendet werden, indem das Attribut und der Bereich für eines der abgerufenen Attribute im *pattributesname* -Array angegeben werden, wenn die [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0d6ae-114">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface can be used for range retrieval by specifying the attribute and range for one of the retrieved attributes in the *pAttributesName* array when calling the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method.</span></span>


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



<span data-ttu-id="0d6ae-115">Wenn Sie die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle für den Bereichs Abruf verwenden, gibt es ein Problem, das speziell behandelt werden muss.</span><span class="sxs-lookup"><span data-stu-id="0d6ae-115">When using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for range retrieval, there is one problem that must be specifically addressed.</span></span> <span data-ttu-id="0d6ae-116">Wenn der angeforderte Bereich die Anzahl der verbleibenden Werte überschreitet, gibt [**idirector ysearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) die **E \_ ADS- \_ Spalte \_ nicht \_ festgelegt** zurück.</span><span class="sxs-lookup"><span data-stu-id="0d6ae-116">When the range requested exceeds the number of remaining values, [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) will return **E\_ADS\_COLUMN\_NOT\_SET**.</span></span> <span data-ttu-id="0d6ae-117">Um die restlichen Werte abzurufen, muss der Bereichs Platzhalter "" verwendet werden \* .</span><span class="sxs-lookup"><span data-stu-id="0d6ae-117">To retrieve the remaining values, it is necessary to use the range wildcard '\*'.</span></span> <span data-ttu-id="0d6ae-118">Wenn eine Gruppe z. b. 150 Mitglieder enthält, können die Mitglieds Werte 0-100 normalerweise mithilfe des Bereichs Abrufs abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0d6ae-118">For example, if a group contains 150 members, member values 0-100 can be retrieved normally using ranged retrieval.</span></span> <span data-ttu-id="0d6ae-119">Wenn der Bereich 101-200 dann angefordert wird, gibt **idirector ysearch:: GetColumn** die **E \_ ADS- \_ Spalte \_ nicht \_ festgelegt** zurück.</span><span class="sxs-lookup"><span data-stu-id="0d6ae-119">If range 101-200 is then requested, **IDirectorySearch::GetColumn** will return **E\_ADS\_COLUMN\_NOT\_SET**.</span></span> <span data-ttu-id="0d6ae-120">Dieses Problem kann mithilfe der [**IDirectorySearch:: getnextcolumnname**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) -Methode vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="0d6ae-120">This problem can be avoided by using the [**IDirectorySearch::GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) method.</span></span> <span data-ttu-id="0d6ae-121">In der Regel gibt **getnextcolumnname** die ursprüngliche Abfrage Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="0d6ae-121">Normally, **GetNextColumnName** will return the original query string.</span></span> <span data-ttu-id="0d6ae-122">Wenn jedoch der angeforderte Bereich die Anzahl der verbleibenden Werte überschreitet, gibt **getnextcolumnname** eine geänderte Version der Abfrage Zeichenfolge zurück, indem der Wert für den hohen Bereich durch den Bereichs Platzhalter "" ersetzt wird \* .</span><span class="sxs-lookup"><span data-stu-id="0d6ae-122">However, when the range requested exceeds the number of remaining values, **GetNextColumnName** will return a modified version of the query string by replacing the high range value with the range wildcard '\*'.</span></span> <span data-ttu-id="0d6ae-123">Im obigen Beispiel wird die erste Abfrage mit der Attribut Zeichenfolge "Member; Range = 0-100" und **getnextcolumnname** "Member; Range = 0-100" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0d6ae-123">In the example above, the first query would be performed with an attribute string of "member;range=0-100" and **GetNextColumnName** will return "member;range=0-100".</span></span> <span data-ttu-id="0d6ae-124">In der zweiten Abfrage lautet die Attribut Zeichenfolge "Member; Range = 101-200", aber **getnextcolumnname** gibt "Member; Range = 101- \* " zurück.</span><span class="sxs-lookup"><span data-stu-id="0d6ae-124">In the second query, the attribute string would be "member;range=101-200", but **GetNextColumnName** will return "member;range=101-\*".</span></span> <span data-ttu-id="0d6ae-125">Dieser Fall kann durch Vergleichen der ursprünglichen Attribut Zeichenfolge mit dem Ergebnis von **getnextcolumnname** ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="0d6ae-125">This case can be determined by comparing the original attribute string to the result of **GetNextColumnName**.</span></span> <span data-ttu-id="0d6ae-126">Wenn sich die Zeichen folgen unterscheiden, sollte der letzte Block von Werten erneut mit dem Bereichs Platzhalter angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="0d6ae-126">If the strings are different, the last block of values should be requested again with the range wildcard.</span></span>

<span data-ttu-id="0d6ae-127">Weitere Informationen und ein Codebeispiel, das zeigt, wie die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle für den Bereichs Abruf verwendet wird, finden Sie unter [Beispielcode für den Bereich mit idirector ysearch](example-code-for-ranging-with-idirectorysearch.md).</span><span class="sxs-lookup"><span data-stu-id="0d6ae-127">For more information and a code example that shows how to use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for range retrieval, see [Example Code for Ranging with IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).</span></span>

 

 




