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
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a>Verwenden von IDirectorySearch und IDirectoryObject für den Bereichs Abruf

Mithilfe der [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle oder der [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle können Sie einen Bereich von Eigenschafts Werten abrufen. Geben Sie hierzu das Attribut und den Bereich für eines der in der Abfrage angeforderten Attribute an.

## <a name="range-retrieval-with-idirectoryobject"></a>Bereichs Abruf mit IDirectoryObject

Die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle kann für den Bereichs Abruf verwendet werden, indem das Attribut und der Bereich für eines der Attribute im *pattributesname* -Array angegeben werden, wenn die [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) -Methode aufgerufen wird.


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



Weitere Informationen und ein Codebeispiel, das zeigt, wie die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle für den Bereichs Abruf verwendet wird, finden Sie unter [Beispielcode für den Bereich mit IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).

## <a name="range-retrieval-with-idirectorysearch"></a>Bereichs Abruf mit idirector ysearch

Die [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle kann für den Bereichs Abruf verwendet werden, indem das Attribut und der Bereich für eines der abgerufenen Attribute im *pattributesname* -Array angegeben werden, wenn die [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) -Methode aufgerufen wird.


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



Wenn Sie die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle für den Bereichs Abruf verwenden, gibt es ein Problem, das speziell behandelt werden muss. Wenn der angeforderte Bereich die Anzahl der verbleibenden Werte überschreitet, gibt [**idirector ysearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) die **E \_ ADS- \_ Spalte \_ nicht \_ festgelegt** zurück. Um die restlichen Werte abzurufen, muss der Bereichs Platzhalter "" verwendet werden \* . Wenn eine Gruppe z. b. 150 Mitglieder enthält, können die Mitglieds Werte 0-100 normalerweise mithilfe des Bereichs Abrufs abgerufen werden. Wenn der Bereich 101-200 dann angefordert wird, gibt **idirector ysearch:: GetColumn** die **E \_ ADS- \_ Spalte \_ nicht \_ festgelegt** zurück. Dieses Problem kann mithilfe der [**IDirectorySearch:: getnextcolumnname**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) -Methode vermieden werden. In der Regel gibt **getnextcolumnname** die ursprüngliche Abfrage Zeichenfolge zurück. Wenn jedoch der angeforderte Bereich die Anzahl der verbleibenden Werte überschreitet, gibt **getnextcolumnname** eine geänderte Version der Abfrage Zeichenfolge zurück, indem der Wert für den hohen Bereich durch den Bereichs Platzhalter "" ersetzt wird \* . Im obigen Beispiel wird die erste Abfrage mit der Attribut Zeichenfolge "Member; Range = 0-100" und **getnextcolumnname** "Member; Range = 0-100" zurückgegeben. In der zweiten Abfrage lautet die Attribut Zeichenfolge "Member; Range = 101-200", aber **getnextcolumnname** gibt "Member; Range = 101- \* " zurück. Dieser Fall kann durch Vergleichen der ursprünglichen Attribut Zeichenfolge mit dem Ergebnis von **getnextcolumnname** ermittelt werden. Wenn sich die Zeichen folgen unterscheiden, sollte der letzte Block von Werten erneut mit dem Bereichs Platzhalter angefordert werden.

Weitere Informationen und ein Codebeispiel, das zeigt, wie die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle für den Bereichs Abruf verwendet wird, finden Sie unter [Beispielcode für den Bereich mit idirector ysearch](example-code-for-ranging-with-idirectorysearch.md).

 

 




