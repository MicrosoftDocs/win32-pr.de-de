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
# <a name="searching-with-the-idirectorysearch-interface"></a>Suchen mit der idirector ysearch-Schnittstelle

Die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle bietet eine Oberfläche mit geringem Verwaltungsaufwand zum Abfragen von Daten eines Verzeichnisses oder eines globalen Katalogs. Die **idirector ysearch** -com-Schnittstelle kann nur mit einer Vtable verwendet werden und ist daher für Automatisierungs basierte Entwicklungsumgebungen nicht verfügbar.

**So führen Sie eine Suche aus**

1.  Binden an ein Objekt im Verzeichnis.
2.  Ruft [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, um den [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Zeiger abzurufen.
3.  Führen Sie die Suche mithilfe des [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Zeigers aus. Nennen Sie die [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) -Methode, und übergeben Sie einen Suchfilter, die angeforderten Attributnamen und andere Parameter.

Weitere Informationen zur Suchfilter Syntax finden Sie unter [Syntax für Suchfilter](search-filter-syntax.md).

Die Abfrage Ausführung ist Anbieter spezifisch. Bei manchen Anbietern findet die tatsächliche Abfrage Ausführung erst statt, wenn " [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) " oder " [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) " aufgerufen wird. Die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle funktioniert direkt mit Suchfiltern. Weder der SQL-Dialekt noch der LDAP-Dialekt ist erforderlich.

Die [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle stellt Methoden bereit, um das Resultset zeilenweise aufzuzählen. Die [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) -Methode ruft die erste Zeile ab, und [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) wechselt zur nächsten Zeile aus der aktuellen Zeile. Wenn Sie die letzte Zeile erreicht haben, gibt der Aufruf dieser Methoden den \_ Fehlercode der S ADS \_ nomore- \_ Zeilen zurück. Umgekehrt verschiebt [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) Sie jeweils eine Zeile zurück. Ein S \_ ADS \_ nomore \_ Rows-Rückgabewert gibt an, dass Sie die erste Zeile des Resultsets erreicht haben. Diese Methoden arbeiten mit dem Resultset, das im Arbeitsspeicher ansässig ist, auf dem Client. Wenn also auslagerbare und asynchrone Suchvorgänge ausgeführt werden und \_ die \_ Option Cache Ergebnisse deaktiviert ist, kann der rückwärts Bildlauf unerwartete Folgen haben.

Wenn Sie die entsprechende Zeile gefunden haben, rufen Sie [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) auf, um Datenelemente, Spalte nach Spalte abzurufen. Für jeden-Befehl übergeben Sie den Namen der Spalte, die von Interesse ist. Das zurückgegebene Datenelement ist ein Zeiger auf eine [**ADS- \_ Such \_ Spalten**](/windows/desktop/api/Iads/ns-iads-ads_search_column) Struktur. **GetColumn** ordnet Ihnen diese Struktur zu, Sie müssen Sie jedoch mit [**freecolum**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn)freigeben. Ruft [**closesearchhandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) auf, um den Suchvorgang abzuschließen.

**So führen Sie eine Verzeichnis Suche aus**

1.  Binden an einen LDAP-Anbieter. Dabei kann es sich um einen Domänen Controller oder einen globalen Katalog Anbieter handeln.
2.  Rufen Sie die [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -com-Schnittstelle mit einem Aufrufen von [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); ab. Dieser Vorgang wurde möglicherweise in Schritt 1 während der ersten Bindung durchgeführt.

    Optional können Sie [**setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) aufrufen, um Optionen für die Behandlung der Ergebnisse Ihrer Suche auszuwählen.

3.  " [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch)" aufzurufen. Abhängig von den in [**setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) festgelegten Optionen kann dies die Ausführung der Abfrage starten.
4.  Aufrufen von [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) , um den Zeilen Index (intern zu [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) in die erste Zeile zu verschieben.
5.  Lesen Sie die Daten mithilfe von [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn)aus der Zeile, und geben Sie dann [**freecolumschlag**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) ein, um den von **GetColumn** belegten Arbeitsspeicher freizugeben.
6.  Wiederholen Sie Schritt 5, bis alle Daten aus dem Suchergebnis abgerufen wurden oder [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) S \_ ADS \_ nomore \_ Rows zurückgibt.
7.  Wenden Sie nach Abschluss des Vorgangs [**abandonsearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) und [**closesearchhandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) an.

Das folgende Codebeispiel zeigt dieses Szenario. Um mit der Bindung an ADSI zu beginnen, müssen Sie die [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion aufzurufen.


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



Dadurch wird ein Zeiger auf die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle bereitstellt.

Da nun eine COM-Schnittstelle für eine idirectoryinterface-Instanz vorhanden ist, müssen Sie [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)aufrufen.

Erstellen Sie ein Array von Attributnamen, die sich auf den Abruf der [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) -Funktion vorbereiten. Die Attributnamen werden innerhalb des Active Directory Schema definiert. Weitere Informationen zur Schema Definition finden Sie unter [ADSI-Schema Modell](adsi-schema-model.md). Die aufgelisteten Attributnamen werden zurückgegeben, wenn Sie vom-Objekt als Resultset der Suche unterstützt werden.


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



Nennen Sie nun die [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) -Funktion. Die Suche wird erst ausgeführt, wenn Sie die [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) -Methode aufrufen.


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



Aufrufen von [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) zum Durchlaufen von Zeilen im Ergebnis. Jede Zeile wird dann nach dem Attribut "Description" abgefragt. Wenn das Attribut gefunden wird, wird es angezeigt.


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



Um die Suche zu beenden, wenden Sie die Methode " [**abandonsearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) " an.

Wenn eine Seitengröße nicht festgelegt ist, wird [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) so lange blockiert, bis das gesamte Resultset an den Client zurückgegeben wird. Wenn die Seitengröße festgelegt ist, wird **GetNextRow** so lange blockiert, bis die erste Seite (Seitengröße = Anzahl der Zeilen in einer Seite) zurückgegeben wird. Wenn die Seitengröße festgelegt ist und die Abfrage sortiert werden soll und Sie nicht nach mindestens einem indizierten Attribut suchen, wird der Wert für die Seitengröße ignoriert, und der Server berechnet das gesamte Resultset, bevor die Daten zurückgegeben werden. Dies hat zur Folge, dass **GetNextRow** blockiert wird, bis die Abfrage abgeschlossen ist.

> [!Note]  
> Um diese Abfrage von einer Verzeichnis Suche zu einer globalen Katalog Suche zu ändern, wird der [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Rückruf geändert.

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 