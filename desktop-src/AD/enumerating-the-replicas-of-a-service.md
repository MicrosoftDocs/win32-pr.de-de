---
title: Auflisten der Replikate eines Dienstanbieter
description: Dieses Thema enthält ein Codebeispiel, in dem die installierten Instanzen eines replizierten Diensts auf unterschiedlichen Host Computern im gesamten Unternehmen aufgelistet werden.
ms.assetid: 9dc3f932-c3e1-4ce1-a945-12d68838304e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 995cd665476a55b6bf717f356fafa54b0d2e10e6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104516709"
---
# <a name="enumerating-the-replicas-of-a-service"></a>Auflisten der Replikate eines Dienstanbieter

Dieses Thema enthält ein Codebeispiel, in dem die installierten Instanzen eines replizierten Diensts auf unterschiedlichen Host Computern im gesamten Unternehmen aufgelistet werden. Um das Kennwort des Dienst Kontos für jede Instanz eines replizierten Dienstanbieter zu ändern, verwenden Sie dieses Codebeispiel in Verbindung mit dem Codebeispiel im Thema [Ändern des Kennworts für das Benutzerkonto des Dienstanbieter](changing-the-password-on-a-serviceampaposs-user-account.md) .

Im Codebeispiel wird davon ausgegangen, dass jede Dienst Instanz über ein eigenes Dienst Verbindungspunkt-Objekt (Service Connection Point, SCP) im Verzeichnis verfügt. Ein SCP ist ein Objekt der [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) -Klasse. Diese Klasse verfügt über ein **Schlüssel** Wort Attribut, das ein mehr wertiges Attribut ist, das in den einzelnen globalen Katalog (GC) in der Gesamtstruktur repliziert wird. Das **Keywords** -Attribut der einzelnen Instanzen des Dienst Verbindungs Punkts enthält die Produkt-GUID der Dienst-. Dies ermöglicht die Suche nach allen SCPs für die verschiedenen Dienst Instanzen, indem ein GC nach Objekten mit einem **Schlüssel** Wort Attribut durchsucht wird, das der Produkt-GUID entspricht.

Im Codebeispiel wird ein [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Zeiger auf einen GC abgerufen, und die [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) -Methode wird verwendet, um nach SCPs zu suchen. Beachten Sie, dass die GC ein partielles Replikat für jeden SCP enthält. Das heißt, Sie enthält einige der SCP-Attribute, aber nicht alle. Konzentrieren Sie sich in diesem Codebeispiel auf das **servicednsname** -Attribut, das den DNS-Namen des Host Servers für diese Dienst Instanz enthält. Da **servicednsname** keinem der in einem GC replizierten Attribute entspricht, wird im Codebeispiel ein zweistufiger Prozess verwendet, um ihn abzurufen. Zuerst wird die GC-Suche verwendet, um den Distinguished Name (DN) des Dienst Verbindungs Punkts abzurufen. Anschließend wird dieser DN verwendet, um eine direkte Bindung zum Dienst Verbindungspunkt herzustellen, um die **servicednsname** -Eigenschaft abzurufen.


```C++
HRESULT EnumerateServiceInstances(
       LPWSTR szQuery,                // Search string filter.
       LPWSTR *pszAttribs,            // An array of attributes 
                                      // to retrieve.
       DWORD dwAttribs,               // # of attributes requested.
       DWORD *pdwAttribs,             // # of attributes retrieved.
       ADS_ATTR_INFO **ppPropEntries  // Returns a pointer to the 
                                      // retrieved attributes.
        )
{
HRESULT hr;
IEnumVARIANT *pEnum = NULL;
IADsContainer *pCont = NULL;
VARIANT var;
IDispatch *pDisp = NULL;
BSTR  bstrPath = NULL;
ULONG lFetch;
IADs *pADs = NULL;
int iRows=0;
static IDirectorySearch *pSearch = NULL;
static ADS_SEARCH_HANDLE hSearch = NULL;

// Parameters for IDirectoryObject.
IDirectoryObject *pSCP = NULL;
 
// Structures and parameters for IDirectorySearch.
DWORD               dwPref;
ADS_SEARCH_COLUMN   Col;
ADS_SEARCHPREF_INFO SearchPref[2];
 
// First time through; set up the search.
if (pSearch == NULL) 
{
    // Bind to the GC: namespace container object. The GC DN 
    // is a single immediate child of the GC: namespace, which must 
    // be obtained through enumeration.
    hr = ADsGetObject(L"GC:", 
        IID_IADsContainer, 
        (void**) &pCont );
    if (FAILED(hr)) {
        _tprintf(TEXT("ADsGetObject(GC) failed: 0x%x\n"), hr);
        goto Cleanup;
    }
 
    // Obtain an enumeration interface for the GC container. 
    hr = ADsBuildEnumerator(pCont,&pEnum);
    if (FAILED(hr)) {
        _tprintf(TEXT("ADsBuildEnumerator failed: 0x%x\n"), hr);
        goto Cleanup;
    }
 
    // Enumerate. There is only one child of the GC: object.
    hr = ADsEnumerateNext(pEnum,1,&var,&lFetch);
    if (( hr == S_OK ) && ( lFetch == 1 ) ) 
    {
        pDisp = V_DISPATCH(&var);
        hr = pDisp->QueryInterface( IID_IADs, (void**)&pADs);
        if (hr == S_OK) 
            hr = pADs->get_ADsPath(&bstrPath);
    }
    if (FAILED(hr)) {
        _tprintf(TEXT("Enumeration failed: 0x%x\n"), hr);
        goto Cleanup;
    }
 
    // Now bstrPath contains the ADsPath for the current GC.  
    // Bind the GC to get the search interface.
    hr = ADsGetObject(bstrPath, 
                      IID_IDirectorySearch, 
                      (void**)&pSearch);
    if (FAILED(hr)) {
        _tprintf(TEXT("Failed to bind search root: 0x%x\n"), hr);
        goto Cleanup;
    } 
 
    // Set up a deep search.
    // Thousands of objects are not expected
    // in this example; request 1000 rows per page.
    dwPref=sizeof(SearchPref)/sizeof(ADS_SEARCHPREF_INFO);
    SearchPref[0].dwSearchPref =    ADS_SEARCHPREF_SEARCH_SCOPE;
    SearchPref[0].vValue.dwType =   ADSTYPE_INTEGER;
    SearchPref[0].vValue.Integer =  ADS_SCOPE_SUBTREE;
 
    SearchPref[1].dwSearchPref =    ADS_SEARCHPREF_PAGESIZE;
    SearchPref[1].vValue.dwType =   ADSTYPE_INTEGER;
    SearchPref[1].vValue.Integer =  1000;
 
    hr = pSearch->SetSearchPreference(SearchPref, dwPref);
    if (FAILED(hr))    {
        _tprintf(TEXT("Failed to set search prefs: 0x%x\n"), hr);
        goto Cleanup;
    } 
 
    // Execute the search. From the GC, get the distinguished name 
    // of the SCP. Use the DN to bind to the SCP and get the other 
    // properties.
    hr = pSearch->ExecuteSearch(szQuery, pszAttribs, 1, &hSearch);
    if (FAILED(hr)) {
        _tprintf(TEXT("ExecuteSearch failed: 0x%x\n"), hr);
        goto Cleanup;
    } 
}
 
// Get the next row.
hr = pSearch->GetNextRow(hSearch);
 
// Process the row.
if (SUCCEEDED(hr) && hr !=S_ADS_NOMORE_ROWS) 
{
    // Get the distinguished name of the object in this row.
    hr = pSearch->GetColumn(hSearch, L"distinguishedName", &Col);
    if FAILED(hr) { 
        _tprintf(TEXT("GetColumn failed: 0x%x\n"), hr);
        goto Cleanup;
    }
    // Bind to the DN to get the properties.
    if (Col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
    {
        LPWSTR szSCPPath = 
          new WCHAR[7 + lstrlenW(Col.pADsValues->CaseIgnoreString) + 1];
        wcscpy_s(szSCPPath, L"LDAP://");
        wcscat_s(szSCPPath, Col.pADsValues->CaseIgnoreString);
        hr = ADsGetObject(szSCPPath, 
                          IID_IDirectoryObject,
                          (void**)&pSCP);
        delete szSCPPath;
        if (SUCCEEDED(hr)) 
        {
            hr = pSCP->GetObjectAttributes(pszAttribs, dwAttribs,
                          ppPropEntries, pdwAttribs);
            if(FAILED(hr)) {
                _tprintf(TEXT("GetObjectAttributes Failed."), hr);
                goto Cleanup;
            }
        }
    }
    pSearch->FreeColumn(&Col);}
 
Cleanup:
if (bstrPath)
    SysFreeString(bstrPath);
if (pSCP) 
    pSCP->Release();
if (pCont) 
    pCont->Release();
if (pEnum)
    ADsFreeEnumerator(pEnum);
if (pADs) 
    pADs->Release();
if (pDisp)
    pDisp->Release();
 
return hr;
 
}
```



 

 