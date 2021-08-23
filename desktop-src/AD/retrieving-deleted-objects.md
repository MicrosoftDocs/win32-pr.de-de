---
title: Abrufen gelöschter Objekte
description: Gelöschte Objekte werden im Container Gelöschte Objekte gespeichert.
ms.assetid: dc9a6466-204b-4a78-b0f3-9c03c13a374b
ms.tgt_platform: multiple
keywords:
- Abrufen von Deleted Objects AD
- Objekt-AD, Abrufen gelöschter Objekte
- Active Directory, Verwenden, Abrufen gelöschter Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b033a992599fecfc372bf578c1bade54867fd8332c3e114103a69264f736b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025088"
---
# <a name="retrieving-deleted-objects"></a>Abrufen gelöschter Objekte

Gelöschte Objekte werden im Container Gelöschte Objekte gespeichert. Der Container für gelöschte Objekte ist normalerweise nicht sichtbar, aber der Container für gelöschte Objekte kann von einem Mitglied der Administratorengruppe gebunden werden. Der Inhalt des Containers für gelöschte Objekte kann aufzählt werden, und einzelne Attribute für gelöschte Objekte können über die [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/iads/nn-iads-idirectorysearch) mit der **Sucheinstellung ADS \_ SEARCHPREF \_ TOMBSTONE** ermittelt werden.

Der Container für gelöschte Objekte kann durch Binden an den bekannten **GUID-GUID-Container \_ für \_ \_ gelöschte OBJEKTE,** der in Ntdsapi.h definiert ist, ermittelt werden. Weitere Informationen zum Binden an bekannte GUIDs finden Sie unter Binden an [Well-Known-Objekte mithilfe von WKGUID.](binding-to-well-known-objects-using-wkguid.md)

Geben Sie **die OPTION ADS FAST \_ \_ BIND** an, wenn Sie eine Bindung an den Container für gelöschte Objekte erstellen. Dies bedeutet, dass die ADSI-Schnittstellen, die zum Arbeiten mit einem Objekt in Active Directory Domain Services verwendet werden, z. B. [**IADs**](/windows/desktop/api/iads/nn-iads-iads) und [**IADsPropertyList,**](/windows/desktop/api/iads/nn-iads-iadspropertylist)nicht im Container gelöschte Objekte verwendet werden können. Weitere Informationen und ein Codebeispiel, das zeigt, wie eine Bindung an den Container für gelöschte Objekte erstellt wird, finden Sie weiter unten in der Beispielfunktion GetDeletedObjectsContainer.

-   [Aufzählen gelöschter Objekte](#enumerating-deleted-objects)
-   [Suchen eines bestimmten gelöschten Objekts](#finding-a-specific-deleted-object)
    -   [GetDeletedObjectsContainer](#getdeletedobjectscontainer)
    -   [EnumDeletedObjects](#enumdeletedobjects)
    -   [FindDeletedObjectByGUID](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a>Aufzählen gelöschter Objekte

Die [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/iads/nn-iads-idirectorysearch) wird verwendet, um nach gelöschten Objekten zu suchen.

**So aufzählen Sie gelöschte Objekte**

1.  Abrufen der [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/iads/nn-iads-idirectorysearch) für den Container für gelöschte Objekte. Dies erfolgt durch Binden an den Container für gelöschte Objekte und Anfordern der **IDirectorySearch-Schnittstelle.** Weitere Informationen und ein Codebeispiel, das zeigt, wie eine Bindung an den Container für gelöschte Objekte erstellt wird, finden Sie im folgenden Beispiel für eine **GetDeletedObjectsContainer-Funktion.**
2.  Legen Sie **die Sucheinstellung ADS \_ SEARCHPREF \_ SEARCH \_ SCOPE** mithilfe der [**IDirectorySearch::SetSearchPreference-Methode**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) auf **ADS SCOPE \_ \_ ONELEVEL** fest. Die **EINSTELLUNG ADS SCOPE \_ \_ SUBTREE** kann ebenfalls verwendet werden, aber der Container für gelöschte Objekte ist nur eine Ebene, sodass die Verwendung von **ADS SCOPE \_ \_ SUBTREE** redundant ist.
3.  Legen Sie **die SUCHeinstellung ADS \_ SEARCHPREF \_ TOMBSTONE** auf **TRUE fest.** Dies bewirkt, dass die Suche gelöschte Objekte enthält.
4.  Legen Sie **die Sucheinstellung ADS \_ SEARCHPREF \_ PAGESIZE** auf einen Wert kleiner oder gleich 1000 fest. Dies ist optional, aber wenn dies nicht erfolgt, können nicht mehr als 1.000 gelöschte Objekte abgerufen werden.
5.  Legen Sie den Suchfilter im [**IDirectorySearch::ExecuteSearch-Aufruf**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) auf "(isDeleted=**TRUE**)" fest. Dies bewirkt, dass bei der Suche nur Objekte abgerufen werden, für die **das Attribut isDeleted** auf **TRUE festgelegt ist.**

Einen Codebeispielcode, der zeigt, wie gelöschte Objekte aufzählt werden, finden Sie im folgenden **EnumDeletedObjects-Funktionsbeispiel.**

Die Suche kann weiter verbessert werden, indem dem Suchfilter hinzugefügt wird, wie unter [LDAP-Dialekt gezeigt.](/windows/desktop/ADSI/ldap-dialect) Um beispielsweise nach allen gelöschten Objekten mit einem Namen zu suchen, der mit "Jeff" beginnt, wird der Suchfilter auf "(&(isDeleted=**TRUE**)(cn=Jeff \* ))" festgelegt.

Da gelöschte Objekte die meisten ihrer Attribute entfernt haben, wenn sie gelöscht werden, ist es nicht möglich, eine direkte Bindung an ein gelöschtes Objekt zu erstellen. Die **OPTION ADS FAST \_ \_ BIND** muss beim Binden an ein gelöschtes Objekt angegeben werden. Dies bedeutet, dass die ADSI-Schnittstellen, die für die Arbeit mit einem Active Directory Domain Services-Objekt verwendet werden, z. B. [**IADs**](/windows/desktop/api/iads/nn-iads-iads) und [**IADsPropertyList,**](/windows/desktop/api/iads/nn-iads-iadspropertylist)nicht für einen gelöschten Objektcontainer verwendet werden können.

## <a name="finding-a-specific-deleted-object"></a>Suchen eines bestimmten gelöschten Objekts

Es ist auch möglich, ein bestimmtes gelöschtes Objekt zu finden. Wenn **die objectGUID des** Objekts bekannt ist, kann sie verwendet werden, um mit diesem bestimmten **objectGUID-Objekt nach dem Objekt zu suchen.** Weitere Informationen und ein Codebeispiel, das zeigt, wie sie ein bestimmtes gelöschtes Objekt finden, finden Sie weiter unten unter **FindDeletedObjectByGUID.**

### <a name="getdeletedobjectscontainer"></a>GetDeletedObjectsContainer

Das folgende C++-Codebeispiel zeigt, wie eine Bindung an den Container für gelöschte Objekte erstellt wird.


```C++
//***************************************************************************
//
//  GetDeletedObjectsContainer()
//
//  Binds to the Deleted Object container.
//
//***************************************************************************

HRESULT GetDeletedObjectsContainer(IADsContainer **ppContainer)
{
    if(NULL == ppContainer)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADs *pRoot;

    *ppContainer = NULL;

    // Bind to the rootDSE object.
    hr = ADsOpenObject(L"LDAP://rootDSE",
                    NULL,
                    NULL,
                    ADS_SECURE_AUTHENTICATION,
                    IID_IADs,
                    (LPVOID*)&pRoot);
    if(SUCCEEDED(hr))
    {
        VARIANT var;
        
        VariantInit(&var);

        // Get the current domain DN.
        hr = pRoot->Get(CComBSTR("defaultNamingContext"), &var);
        if(SUCCEEDED(hr))
        {
            // Build the binding string.
            LPWSTR pwszFormat = L"LDAP://<WKGUID=%s,%s>";
            LPWSTR pwszPath;

            pwszPath = new WCHAR[wcslen(pwszFormat) + wcslen(GUID_DELETED_OBJECTS_CONTAINER_W) + wcslen(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, pwszFormat, GUID_DELETED_OBJECTS_CONTAINER_W, var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_FAST_BIND | ADS_SECURE_AUTHENTICATION,
                                IID_IADsContainer,
                                (LPVOID*)ppContainer);

                delete pwszPath;
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }

            VariantClear(&var);        
        }

        pRoot->Release(); 
    }

    return hr;
}

```



### <a name="enumdeletedobjects"></a>EnumDeletedObjects

Das folgende C++-Codebeispiel zeigt, wie die Objekte im Container Gelöschte Objekte aufzählt werden.


```C++
//***************************************************************************
//
//  EnumDeletedObjects()
//
//  Enumerates all of the objects in the Deleted Objects container.
//
//***************************************************************************

HRESULT EnumDeletedObjects()
{
    HRESULT hr;
    IADsContainer *pDeletedObjectsCont = NULL;
    IDirectorySearch *pSearch = NULL;

    hr = GetDeletedObjectsContainer(&pDeletedObjectsCont);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    hr = pDeletedObjectsCont->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Only search for direct child objects of the container.
    ADS_SEARCHPREF_INFO rgSearchPrefs[3];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_ONELEVEL;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the page size.
    rgSearchPrefs[2].dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
    rgSearchPrefs[2].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[2].vValue.Integer = 1000;

    // Set the search preference
    hr = pSearch->SetSearchPreference(rgSearchPrefs, ARRAYSIZE(rgSearchPrefs));
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    LPWSTR pszSearch = L"(cn=*)";

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search
    hr = pSearch->ExecuteSearch(    pszSearch,
                                    rgAttributes,
                                    ARRAYSIZE(rgAttributes),
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;
                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pDeletedObjectsCont)
    {
        pDeletedObjectsCont->Release();
    }

    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}

```



### <a name="finddeletedobjectbyguid"></a>FindDeletedObjectByGUID

Das folgende C++-Codebeispiel zeigt, wie sie ein bestimmtes gelöschtes Objekt aus der **objectGUID-Eigenschaft des Objekts** finden.


```C++
HRESULT FindDeletedObjectByGUID(IADs *padsDomain, GUID *pguid)
{
    HRESULT hr;
    IDirectorySearch *pSearch = NULL;
    LPWSTR pwszGuid = NULL;

    hr = padsDomain->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Search the entire tree.
    ADS_SEARCHPREF_INFO rgSearchPrefs[2];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_SUBTREE;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the search preference.
    hr = pSearch->SetSearchPreference(rgSearchPrefs, 2);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    hr = ADsEncodeBinaryData((LPBYTE)pguid, sizeof(GUID), &pwszGuid);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    LPWSTR pwszFormat = L"(objectGUID=%s)";

    LPWSTR pwszSearch = new WCHAR[lstrlenW(pwszFormat) + lstrlenW(pwszGuid) + 1];
    if(NULL == pwszSearch)
    {
        goto cleanup;
    }
    
    swprintf_s(pwszSearch, pwszFormat, pwszGuid);
    
    FreeADsMem(pwszGuid);

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search.
    hr = pSearch->ExecuteSearch(    pwszSearch,
                                    rgAttributes,
                                    3,
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data.
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                GUID guid;
                                LPBYTE pb = col.pADsValues[x].OctetString.lpValue;
                                WCHAR wszGUID[MAX_PATH];

                                // Convert the octet string into a GUID.
                                guid.Data1 = *((long*)pb);
                                pb += sizeof(guid.Data1);
                                guid.Data2 = *((short*)pb);
                                pb += sizeof(guid.Data2);
                                guid.Data3 = *((short*)pb);
                                pb += sizeof(guid.Data3);
                                CopyMemory(&guid.Data4, pb, sizeof(guid.Data4));

                                // Convert the GUID into a string.
                                StringFromGUID2(guid, wszGUID, MAX_PATH);
                                wprintf(wszGUID);

                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                                OutputDebugStringW(wszGUID);
                                OutputDebugStringW(L"\n");

                                {
                                    DWORD a;

                                    for(a = 0, *wszGUID = 0; a < col.pADsValues[x].OctetString.dwLength; a++)
                                    {
                                        swprintf_s(wszGUID + lstrlenW(wszGUID), L"%02X", *(LPBYTE)(col.pADsValues[x].OctetString.lpValue + a));
                                    }

                                    OutputDebugStringW(wszGUID);
                                    OutputDebugStringW(L"\n");
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pwszSearch)
    {
        delete pwszSearch;
    }
    
    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}
```



 

 