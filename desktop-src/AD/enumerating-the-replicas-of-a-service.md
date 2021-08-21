---
title: Aufzählen der Replikate eines Diensts
description: Dieses Thema enthält ein Codebeispiel, das die installierten Instanzen eines replizierten Diensts auf verschiedenen Hostcomputern in einem Unternehmen aufzählt.
ms.assetid: 9dc3f932-c3e1-4ce1-a945-12d68838304e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cce0b1a9da8eac974682514cd283f8e530388727a2b674765a39056e94a0c95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429253"
---
# <a name="enumerating-the-replicas-of-a-service"></a>Aufzählen der Replikate eines Diensts

Dieses Thema enthält ein Codebeispiel, das die installierten Instanzen eines replizierten Diensts auf verschiedenen Hostcomputern in einem Unternehmen aufzählt. Um das Dienstkontokennwort für jede Instanz eines replizierten Diensts zu ändern, verwenden Sie dieses Codebeispiel in Verbindung mit dem Codebeispiel im Thema [Ändern](changing-the-password-on-a-serviceampaposs-user-account.md) des Kennworts für das Benutzerkonto eines Diensts.

Im Codebeispiel wird davon ausgegangen, dass jede Dienstinstanz über ein eigenes Dienstverbindungspunktobjekt (Service Connection Point, SCP) im Verzeichnis verfügt. Ein SCP ist ein Objekt der [**serviceConnectionPoint-Klasse.**](/windows/desktop/ADSchema/c-serviceconnectionpoint) Diese Klasse verfügt über **ein Schlüsselwortattribut,** bei dem es sich um ein mehrwertiges Attribut handelt, das in jeden globalen Katalog (GC) in der Gesamtstruktur repliziert wird. Das **Keywords-Attribut** des SCP jeder Instanz enthält die Produkt-GUID des Diensts. Dadurch können alle SCPs für die verschiedenen Dienstinstanzen gesucht werden,  indem eine GC nach Objekten mit einem Schlüsselwortattribut gesucht wird, das der Produkt-GUID entspricht.

Das Codebeispiel erhält einen [**IDirectorySearch-Zeiger**](/windows/desktop/api/iads/nn-iads-idirectorysearch) auf einen GC und verwendet die [**IDirectorySearch::ExecuteSearch-Methode,**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) um nach den SCPs zu suchen. Beachten Sie, dass die GC ein partielles Replikat für jeden SCP enthält. Das heißt, sie enthält einige der SCP-Attribute, aber nicht alle. Konzentrieren Sie sich in diesem Codebeispiel auf das **attribut serviceDNSName,** das den DNS-Namen des Hostservers für diese Dienstinstanz enthält. Da **serviceDNSName nicht** eines der attributes ist, die in einer GC repliziert werden, verwendet das Codebeispiel einen zweistufigen Prozess zum Abrufen. Zunächst wird die GC-Suche verwendet, um den Distinguished Name (DN) des SCP abzurufen. Anschließend wird dieser DN verwendet, um eine direkte Bindung an den SCP zu erhalten, um die **serviceDNSName-Eigenschaft** abzurufen.


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



 

 