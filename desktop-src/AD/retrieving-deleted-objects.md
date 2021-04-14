---
title: Abrufen von gelöschten Objekten
description: Gelöschte Objekte werden im Container Gelöschte Objekte gespeichert.
ms.assetid: dc9a6466-204b-4a78-b0f3-9c03c13a374b
ms.tgt_platform: multiple
keywords:
- Abrufen gelöschter Objekte AD
- Objekt-AD, Abrufen gelöschter Objekte
- Active Directory, verwenden, Abrufen gelöschter Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b2062c747e38bc0b3a9b1b793a102006c11512
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472493"
---
# <a name="retrieving-deleted-objects"></a>Abrufen von gelöschten Objekten

Gelöschte Objekte werden im Container Gelöschte Objekte gespeichert. Der Container "Gelöschte Objekte" ist normalerweise nicht sichtbar, aber der Container "Gelöschte Objekte" kann von einem Mitglied der Gruppe "Administratoren" gebunden werden. Der Inhalt des gelöschten Objects-Containers kann aufgelistet werden, und einzelne gelöschte Objekt Attribute können mithilfe der [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Schnittstelle mit der Such Einstellung der Tombstone-Suche " **ADS \_ searchpref \_** " abgerufen werden.

Der Container "Gelöschte Objekte" kann durch die Bindung an den bekannten Container für GUID- **GUID- \_ \_ Objekte \_** abgerufen werden, der in "NTDSAPI. h" definiert ist. Weitere Informationen zum Binden an bekannte GUIDs finden [Sie unterbinden an Well-Known Objekte mithilfe von wkguid](binding-to-well-known-objects-using-wkguid.md).

Legen Sie die Option **ADS \_ fast \_ Bind** bei der Bindung an den Container für gelöschte Objekte fest. Dies bedeutet, dass die ADSI-Schnittstellen, die für die Arbeit mit einem Objekt in Active Directory Domain Services verwendet werden, z. b. [**IADs**](/windows/desktop/api/iads/nn-iads-iads) und [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), nicht für den Container für gelöschte Objekte verwendet werden können. Weitere Informationen und ein Codebeispiel, das die Bindung an den Container für gelöschte Objekte veranschaulicht, finden Sie unten in der Beispiel Funktion getdeletedobjeczcontainer.

-   [Auflisten von gelöschten Objekten](#enumerating-deleted-objects)
-   [Suchen nach einem bestimmten gelöschten Objekt](#finding-a-specific-deleted-object)
    -   [Getdeletedobjectcontainer](#getdeletedobjectscontainer)
    -   [Enumdeletedobjects](#enumdeletedobjects)
    -   [Finddeletedobjectbyguid](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a>Auflisten von gelöschten Objekten

Die [**idirector ysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Schnittstelle wird verwendet, um nach gelöschten Objekten zu suchen.

**So zählen Sie gelöschte Objekte auf**

1.  Rufen Sie die [**idirector ysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Schnittstelle für den Container für gelöschte Objekte ab. Dies wird erreicht, indem an den Container für gelöschte Objekte gebunden und die **idirectoriysearch** -Schnittstelle angefordert wird. Weitere Informationen und ein Codebeispiel, das die Bindung an den Container für gelöschte Objekte veranschaulicht, finden Sie im folgenden Beispiel für die **getdeletedobjeczcontainer** -Funktion.
2.  Legen Sie die Such Einstellung " **ADS \_ searchpref \_ Search \_ Scope** Search" auf **ADS \_ Scope \_ onelevel** mithilfe der [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) -Methode fest. Die **Anzeige \_ Bereich- \_ Unterstruktur** Einstellung kann auch verwendet werden, aber der Container für gelöschte Objekte ist nur eine Ebene, daher ist die Verwendung der **ADS- \_ Bereichs \_ Teilstruktur** redundant.
3.  Legen Sie die Einstellung für die Tombstone-Suche von **ADS \_ \_ searchpref** auf **true** fest. Dies bewirkt, dass die Suche gelöschte Objekte einschließt.
4.  Legen Sie die Such Einstellung **ADS \_ searchpref \_ PageSize** auf einen Wert fest, der kleiner als oder gleich 1000 ist. Dies ist optional, aber wenn dies nicht der Fall ist, können nicht mehr als 1000 gelöschte Objekte abgerufen werden.
5.  Legen Sie den Suchfilter im [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) -Aufrufs auf "(IsDeleted =**true**)" fest. Dies bewirkt, dass die Suche nur Objekte abruft, bei denen das **isDeleted** -Attribut auf **true** festgelegt ist.

Ein Codebeispiel Code, in dem das Auflisten von gelöschten Objekten veranschaulicht wird, finden Sie im folgenden Beispiel für eine **enumdeletedobjects** -Funktion.

Die Suche kann weiter verfeinert werden, indem Sie dem Suchfilter hinzufügen, wie im [LDAP-Dialekt](/windows/desktop/ADSI/ldap-dialect)gezeigt. Wenn Sie z. b. nach allen gelöschten Objekten suchen möchten, deren Name mit "Jeff" beginnt, wird der Suchfilter auf "(& (IsDeleted =**true**) (CN = Jeff \* ))" festgelegt.

Da bei gelöschten Objekten die meisten Attribute entfernt werden, wenn Sie gelöscht werden, ist es nicht möglich, direkt an ein gelöschtes Objekt zu binden. Die Option **ADS \_ fast \_ Bind** muss beim Binden an ein gelöschtes Objekt angegeben werden. Dies bedeutet, dass die ADSI-Schnittstellen, die für die Arbeit mit einem Active Directory Domain Services Objekt verwendet werden, z. b. [**IADs**](/windows/desktop/api/iads/nn-iads-iads) und [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), nicht für einen gelöschten Objekt Container verwendet werden können.

## <a name="finding-a-specific-deleted-object"></a>Suchen nach einem bestimmten gelöschten Objekt

Es ist auch möglich, ein bestimmtes gelöschtes Objekt zu finden. Wenn die **objectGUID** des Objekts bekannt ist, kann Sie verwendet werden, um nach dem Objekt mit dieser spezifischen **objectGUID** zu suchen. Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie ein bestimmtes gelöschtes Objekt suchen, finden Sie unten unter **finddeletedobjectbyguid** .

### <a name="getdeletedobjectscontainer"></a>Getdeletedobjectcontainer

Im folgenden C++-Codebeispiel wird gezeigt, wie Sie eine Bindung an den Container für gelöschte Objekte herstellen.


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



### <a name="enumdeletedobjects"></a>Enumdeletedobjects

Im folgenden C++-Codebeispiel wird gezeigt, wie die-Objekte im Container für gelöschte Objekte aufgelistet werden.


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



### <a name="finddeletedobjectbyguid"></a>Finddeletedobjectbyguid

Im folgenden C++-Codebeispiel wird gezeigt, wie Sie ein bestimmtes gelöschtes Objekt aus der **objectGUID** -Eigenschaft des Objekts suchen.


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



 

 