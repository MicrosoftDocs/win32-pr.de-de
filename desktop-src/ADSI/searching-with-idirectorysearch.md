---
title: Suchen mit der IDirectorySearch-Schnittstelle
description: Die IDirectorySearch-Schnittstelle bietet eine Schnittstelle mit hohem Und geringem Mehraufwand zum Abfragen von Daten eines Verzeichnisses oder eines globalen Katalogs.
ms.assetid: da415cb2-f320-4be4-b5bd-053cd6a6b2fd
ms.tgt_platform: multiple
keywords:
- Suchen mit der IDirectorySearch-Schnittstelle ADSI
- Abfragen ADSI, Abfrageschnittstellen, IDirectorySearch
- ADSI ADSI , Beispielcode C/C++, Suchen eines Verzeichnisses mit IDirectorySearch
- IDirectorySearch ADSI , Verwenden von zum Durchsuchen eines Verzeichnisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c46700c48f82955bd01967808cd30f2fa078e3b6c998fb3beaac4bf7c7fe8707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023218"
---
# <a name="searching-with-the-idirectorysearch-interface"></a>Suchen mit der IDirectorySearch-Schnittstelle

Die [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) bietet eine Schnittstelle mit hohem Und geringem Mehraufwand zum Abfragen von Daten eines Verzeichnisses oder eines globalen Katalogs. Die **IDirectorySearch-COM-Schnittstelle** kann nur mit einer vtable verwendet werden und ist daher für automatisierungsbasierte Entwicklungsumgebungen nicht verfügbar.

**So führen Sie eine Suche aus**

1.  Binden an ein Objekt im Verzeichnis.
2.  Rufen [**Sie QueryInterface auf,**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) um den [**IDirectorySearch-Zeiger**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) zu erhalten.
3.  Führen Sie die Suche mit dem [**IDirectorySearch-Zeiger**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) aus. Rufen Sie [**die IDirectorySearch::ExecuteSearch-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) auf, und übergeben Sie einen Suchfilter, die angeforderten Attributnamen und andere Parameter.

Weitere Informationen zur Suchfiltersyntax finden Sie unter [Suchfiltersyntax](search-filter-syntax.md).

Die Abfrageausführung ist anbieterspezifisch. Bei einigen Anbietern erfolgt die tatsächliche Abfrageausführung erst, wenn [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) oder [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) aufgerufen wird. Die [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) funktioniert direkt mit Suchfiltern. Weder der SQL noch der LDAP-Dialekt sind erforderlich.

Die [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) stellt Methoden zum Aufzählen des Ergebnisses zeilenweisend bereit. Die [**IDirectorySearch::GetFirstRow-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) ruft die erste Zeile ab, und [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) verschiebt Sie in die nächste Zeile aus der aktuellen Zeile. Wenn Sie die letzte Zeile erreicht haben, gibt der Aufruf dieser Methoden den Fehlercode S \_ ADS \_ NOMORE \_ ROWS zurück. Im Gegensatz dazu [**verschiebt IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) Sie zeile für Zeile zurück. Der Rückgabewert S ADS NOMORE ROWS gibt an, dass Sie die \_ \_ erste Zeile des \_ Resultsets erreicht haben. Diese Methoden arbeiten mit dem im Arbeitsspeicher gespeicherten ResultSet auf dem Client. Wenn also seitenseitige und asynchrone Suchvorgänge ausgeführt werden und die Option CACHEERGEBNISSE deaktiviert ist, kann das \_ \_ Rückwärtsscrolling unerwartete Folgen haben.

Wenn Sie die entsprechende Zeile gefunden haben, rufen [**Sie IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) auf, um Spalten für Spalten Datenelemente zu erhalten. Für jeden Aufruf übergeben Sie den Namen der spalte von Interesse. Das zurückgegebene Datenelement ist ein Zeiger auf eine [**ADS \_ SEARCH \_ COLUMN-Struktur.**](/windows/desktop/api/Iads/ns-iads-ads_search_column) **GetColumn** ordnet diese Struktur für Sie zu, aber Sie müssen sie mit [**FreeColumn frei geben.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) Rufen [**Sie CloseSearchHandle auf,**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) um den Suchvorgang abschließen.

**So führen Sie eine Verzeichnissuche aus**

1.  Binden an einen LDAP-Anbieter. Dies kann ein Domänencontroller oder ein globaler Kataloganbieter sein.
2.  Rufen Sie die [**IDirectorySearch-COM-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) mit einem Aufruf von [**QueryInterface ab.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) Dieser Vorgang wurde möglicherweise in Schritt 1 während der ersten Bindung durchgeführt.

    Rufen Sie optional [**SetSearchPreference auf,**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) um Optionen für die Verarbeitung der Suchergebnisse auszuwählen.

3.  Rufen Sie [**ExecuteSearch auf.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) Abhängig von den in [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) festgelegten Optionen kann die Abfrageausführung beginnen oder nicht.
4.  Rufen [**Sie GetNextRow auf,**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) um den Zeilenindex (intern in [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) in die erste Zeile zu verschieben.
5.  Lesen Sie die Daten aus der Zeile mit [**GetColumn,**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn)und rufen Sie [**dann FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) auf, um den von **GetColumn zugeordneten Arbeitsspeicher frei zu geben.**
6.  Wiederholen Sie Schritt 5, bis alle Daten aus dem Suchergebnis abgerufen werden, oder bis [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) S \_ ADS \_ NOMORE \_ ROWS zurückgibt.
7.  Rufen [**Sie AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) und [**CloseSearchHandle auf,**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) wenn Sie fertig sind.

Dieses Szenario wird im folgenden Codebeispiel veranschaulicht. Um mit der Bindung an ADSI zu beginnen, rufen Sie die [**ADsOpenObject-Funktion**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) auf.


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



Dies stellt einen Zeiger auf die [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) bereit.

Da es nun eine COM-Schnittstelle für eine IDirectoryInterface-Instanz gibt, rufen Sie [**IDirectorySearch::SetSearchPreference auf.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

Erstellen Sie ein Array von Attributnamen, um den Aufruf der [**IDirectorySearch::ExecuteSearch-Funktion**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) vorzubereiten. Die Attributnamen werden im Schema von Active Directory definiert. Weitere Informationen zur Schemadefinition finden Sie unter [ADSI-Schemamodell.](adsi-schema-model.md) Die aufgelisteten Attributnamen werden als Ergebnissatz der Suche zurückgegeben, wenn sie vom -Objekt unterstützt werden.


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



Rufen Sie nun die [**ExecuteSearch-Funktion**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) auf. Die Suche wird erst ausgeführt, wenn Sie die [**GetNextRow-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) aufrufen.


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



Rufen [**Sie GetNextRow auf,**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) um Zeilen im Ergebnis zu iterieren. Jede Zeile wird dann nach dem Attribut "description" abgefragt. Wenn das Attribut gefunden wird, wird es angezeigt.


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



Um die Suche zu beenden, rufen Sie die [**AbandonSearch-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) auf.

Beachten Sie, dass [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) blockiert, bis das gesamte Resultset an den Client zurückgegeben wird, wenn keine Seitengröße festgelegt ist. Wenn die Seitengröße festgelegt ist, wird **GetNextRow** blockiert, bis die erste Seite (Seitengröße = Anzahl der Zeilen auf einer Seite) zurückgegeben wird. Wenn die Seitengröße festgelegt ist und die Abfrage sortiert werden soll und Sie nicht nach mindestens einem indizierten Attribut suchen, wird der Wert der Seitengröße ignoriert, und der Server berechnet das gesamte Resultset, bevor die Daten zurückgegeben werden. Dies hat die Auswirkung, dass **GetNextRow** blockiert wird, bis die Abfrage abgeschlossen ist.

> [!Note]  
> Um diese Abfrage von einer Verzeichnissuche in eine globale Katalogsuche zu ändern, wird der [**ADsOpenObject-Aufruf**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) geändert.

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 