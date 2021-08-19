---
title: Verwenden von IDirectorySearch und IDirectoryObject für den Bereichsabruf
description: Die Schnittstellen IDirectoryObject oder IDirectorySearch können verwendet werden, um einen Bereich von Eigenschaftswerten abzurufen. Geben Sie hierzu das Attribut und den Bereich für eines der in der Abfrage angeforderten Attribute an.
ms.assetid: 4d9d2a98-51d5-4326-b43e-a2ac3bc54a75
ms.tgt_platform: multiple
keywords:
- IDirectorySearch ADSI , Verwenden von für den Bereich zum Abrufen von Mitgliedern einer Gruppe
- IDirectoryObject ADSI , Verwenden von für den Bereich zum Abrufen von Mitgliedern einer Gruppe
- Bereichsabruf ADSI mit IDirectorySearch und IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506d061dd49c98bdb3b8cc731a28d0dc0ee5fe9a0df5816abf259ece17e456ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023058"
---
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a>Verwenden von IDirectorySearch und IDirectoryObject für den Bereichsabruf

Die [**Schnittstellen IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) oder [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) können verwendet werden, um einen Bereich von Eigenschaftswerten abzurufen. Geben Sie hierzu das Attribut und den Bereich für eines der in der Abfrage angeforderten Attribute an.

## <a name="range-retrieval-with-idirectoryobject"></a>Bereichsabruf mit IDirectoryObject

Die [**IDirectoryObject-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) kann für den Bereichsabruf verwendet werden, indem beim Aufrufen der [**IDirectoryObject::GetObjectAttributes-Methode**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) das Attribut und der Bereich für eines der Attribute im *pAttributesName-Array* angegeben werden.


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



Weitere Informationen und ein Codebeispiel, das zeigt, wie die [**IDirectoryObject-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) für den Bereichsabruf verwendet wird, finden Sie unter [Beispielcode für Ranging mit IDirectoryObject.](example-code-for-ranging-with-idirectoryobject.md)

## <a name="range-retrieval-with-idirectorysearch"></a>Bereichsabruf mit IDirectorySearch

Die [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) kann zum Abrufen von Bereichen verwendet werden, indem beim Aufrufen der [**IDirectorySearch::ExecuteSearch-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) das Attribut und der Bereich für eines der abgerufenen Attribute im *pAttributesName-Array* angegeben werden.


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



Wenn Sie die [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) für den Bereichsabruf verwenden, gibt es ein Problem, das speziell behoben werden muss. Wenn der angeforderte Bereich die Anzahl der verbleibenden Werte überschreitet, gibt [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) **E ADS COLUMN NOT \_ \_ \_ \_ SET** zurück. Um die verbleibenden Werte abzurufen, ist es erforderlich, den Bereichs platzhalter " " " zu \* verwenden. Wenn eine Gruppe beispielsweise 150 Elemente enthält, können die Elementwerte 0 bis 100 mithilfe des Bereichsabrufs normal abgerufen werden. Wenn der Bereich 101-200 angefordert wird, gibt **IDirectorySearch::GetColumn** **E ADS COLUMN NOT \_ \_ \_ \_ SET** zurück. Dieses Problem kann mithilfe der [**IDirectorySearch::GetNextColumnName-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) vermieden werden. Normalerweise gibt **GetNextColumnName** die ursprüngliche Abfragezeichenfolge zurück. Wenn der angeforderte Bereich jedoch die Anzahl der verbleibenden Werte überschreitet, gibt **GetNextColumnName** eine geänderte Version der Abfragezeichenfolge zurück, indem der hohe Bereichswert durch den Bereichs platzhalter " " " ersetzt \* wird. Im obigen Beispiel wird die erste Abfrage mit der Attributzeichenfolge "member;range=0-100" ausgeführt, und **GetNextColumnName** gibt "member;range=0-100" zurück. In der zweiten Abfrage wäre die Attributzeichenfolge "member;range=101-200", aber **GetNextColumnName** gibt "member;range=101- \* " zurück. Dieser Fall kann ermittelt werden, indem die ursprüngliche Attributzeichenfolge mit dem Ergebnis von **GetNextColumnName** verglichen wird. Wenn sich die Zeichenfolgen unterscheiden, sollte der letzte Werteblock erneut mit dem Bereichs-Platzhalter angefordert werden.

Weitere Informationen und ein Codebeispiel, das zeigt, wie die [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) für den Bereichsabruf verwendet wird, finden Sie unter [Beispielcode für Ranging mit IDirectorySearch.](example-code-for-ranging-with-idirectorysearch.md)

 

 




