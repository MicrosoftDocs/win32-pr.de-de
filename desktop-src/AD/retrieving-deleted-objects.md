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
# <a name="retrieving-deleted-objects"></a><span data-ttu-id="dbfac-106">Abrufen von gelöschten Objekten</span><span class="sxs-lookup"><span data-stu-id="dbfac-106">Retrieving Deleted Objects</span></span>

<span data-ttu-id="dbfac-107">Gelöschte Objekte werden im Container Gelöschte Objekte gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dbfac-107">Deleted objects are stored in the Deleted Objects container.</span></span> <span data-ttu-id="dbfac-108">Der Container "Gelöschte Objekte" ist normalerweise nicht sichtbar, aber der Container "Gelöschte Objekte" kann von einem Mitglied der Gruppe "Administratoren" gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="dbfac-108">The Deleted Objects container is not normally visible, but the Deleted Objects container can be bound to by a member of the administrators group.</span></span> <span data-ttu-id="dbfac-109">Der Inhalt des gelöschten Objects-Containers kann aufgelistet werden, und einzelne gelöschte Objekt Attribute können mithilfe der [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Schnittstelle mit der Such Einstellung der Tombstone-Suche " **ADS \_ searchpref \_** " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dbfac-109">The contents of the Deleted Objects container can be enumerated and individual deleted object attributes can be obtained using the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface with the **ADS\_SEARCHPREF\_TOMBSTONE** search preference.</span></span>

<span data-ttu-id="dbfac-110">Der Container "Gelöschte Objekte" kann durch die Bindung an den bekannten Container für GUID- **GUID- \_ \_ Objekte \_** abgerufen werden, der in "NTDSAPI. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="dbfac-110">The Deleted Objects container can be obtained by binding to the well-known GUID **GUID\_DELETED\_OBJECTS\_CONTAINER** defined in Ntdsapi.h.</span></span> <span data-ttu-id="dbfac-111">Weitere Informationen zum Binden an bekannte GUIDs finden [Sie unterbinden an Well-Known Objekte mithilfe von wkguid](binding-to-well-known-objects-using-wkguid.md).</span><span class="sxs-lookup"><span data-stu-id="dbfac-111">For more information about binding to well-known GUIDs, see [Binding to Well-Known Objects Using WKGUID](binding-to-well-known-objects-using-wkguid.md).</span></span>

<span data-ttu-id="dbfac-112">Legen Sie die Option **ADS \_ fast \_ Bind** bei der Bindung an den Container für gelöschte Objekte fest.</span><span class="sxs-lookup"><span data-stu-id="dbfac-112">Specify the **ADS\_FAST\_BIND** option when binding to the Deleted Objects container.</span></span> <span data-ttu-id="dbfac-113">Dies bedeutet, dass die ADSI-Schnittstellen, die für die Arbeit mit einem Objekt in Active Directory Domain Services verwendet werden, z. b. [**IADs**](/windows/desktop/api/iads/nn-iads-iads) und [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), nicht für den Container für gelöschte Objekte verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="dbfac-113">This means that the ADSI interfaces used to work with an object in Active Directory Domain Services, such as [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), cannot be used on the Deleted Objects container.</span></span> <span data-ttu-id="dbfac-114">Weitere Informationen und ein Codebeispiel, das die Bindung an den Container für gelöschte Objekte veranschaulicht, finden Sie unten in der Beispiel Funktion getdeletedobjeczcontainer.</span><span class="sxs-lookup"><span data-stu-id="dbfac-114">For more information and a code example that shows how to bind to the Deleted Objects container, see the GetDeletedObjectsContainer example function below.</span></span>

-   [<span data-ttu-id="dbfac-115">Auflisten von gelöschten Objekten</span><span class="sxs-lookup"><span data-stu-id="dbfac-115">Enumerating Deleted Objects</span></span>](#enumerating-deleted-objects)
-   [<span data-ttu-id="dbfac-116">Suchen nach einem bestimmten gelöschten Objekt</span><span class="sxs-lookup"><span data-stu-id="dbfac-116">Finding a Specific Deleted Object</span></span>](#finding-a-specific-deleted-object)
    -   [<span data-ttu-id="dbfac-117">Getdeletedobjectcontainer</span><span class="sxs-lookup"><span data-stu-id="dbfac-117">GetDeletedObjectsContainer</span></span>](#getdeletedobjectscontainer)
    -   [<span data-ttu-id="dbfac-118">Enumdeletedobjects</span><span class="sxs-lookup"><span data-stu-id="dbfac-118">EnumDeletedObjects</span></span>](#enumdeletedobjects)
    -   [<span data-ttu-id="dbfac-119">Finddeletedobjectbyguid</span><span class="sxs-lookup"><span data-stu-id="dbfac-119">FindDeletedObjectByGUID</span></span>](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a><span data-ttu-id="dbfac-120">Auflisten von gelöschten Objekten</span><span class="sxs-lookup"><span data-stu-id="dbfac-120">Enumerating Deleted Objects</span></span>

<span data-ttu-id="dbfac-121">Die [**idirector ysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Schnittstelle wird verwendet, um nach gelöschten Objekten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="dbfac-121">The [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface is used to search for deleted objects.</span></span>

<span data-ttu-id="dbfac-122">**So zählen Sie gelöschte Objekte auf**</span><span class="sxs-lookup"><span data-stu-id="dbfac-122">**To enumerate deleted objects**</span></span>

1.  <span data-ttu-id="dbfac-123">Rufen Sie die [**idirector ysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Schnittstelle für den Container für gelöschte Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="dbfac-123">Obtain the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface for the Deleted Objects container.</span></span> <span data-ttu-id="dbfac-124">Dies wird erreicht, indem an den Container für gelöschte Objekte gebunden und die **idirectoriysearch** -Schnittstelle angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="dbfac-124">This is accomplished by binding to the Deleted Objects container and requesting the **IDirectorySearch** interface.</span></span> <span data-ttu-id="dbfac-125">Weitere Informationen und ein Codebeispiel, das die Bindung an den Container für gelöschte Objekte veranschaulicht, finden Sie im folgenden Beispiel für die **getdeletedobjeczcontainer** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="dbfac-125">For more information and a code example that shows how to bind to the Deleted Objects container, see the following **GetDeletedObjectsContainer** function example.</span></span>
2.  <span data-ttu-id="dbfac-126">Legen Sie die Such Einstellung " **ADS \_ searchpref \_ Search \_ Scope** Search" auf **ADS \_ Scope \_ onelevel** mithilfe der [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) -Methode fest.</span><span class="sxs-lookup"><span data-stu-id="dbfac-126">Set the **ADS\_SEARCHPREF\_SEARCH\_SCOPE** search preference to **ADS\_SCOPE\_ONELEVEL** using the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="dbfac-127">Die **Anzeige \_ Bereich- \_ Unterstruktur** Einstellung kann auch verwendet werden, aber der Container für gelöschte Objekte ist nur eine Ebene, daher ist die Verwendung der **ADS- \_ Bereichs \_ Teilstruktur** redundant.</span><span class="sxs-lookup"><span data-stu-id="dbfac-127">The **ADS\_SCOPE\_SUBTREE** preference can also be used, but the Deleted Objects container is only one level, so using **ADS\_SCOPE\_SUBTREE** is redundant.</span></span>
3.  <span data-ttu-id="dbfac-128">Legen Sie die Einstellung für die Tombstone-Suche von **ADS \_ \_ searchpref** auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="dbfac-128">Set the **ADS\_SEARCHPREF\_TOMBSTONE** search preference to **TRUE**.</span></span> <span data-ttu-id="dbfac-129">Dies bewirkt, dass die Suche gelöschte Objekte einschließt.</span><span class="sxs-lookup"><span data-stu-id="dbfac-129">This causes the search to include deleted objects.</span></span>
4.  <span data-ttu-id="dbfac-130">Legen Sie die Such Einstellung **ADS \_ searchpref \_ PageSize** auf einen Wert fest, der kleiner als oder gleich 1000 ist.</span><span class="sxs-lookup"><span data-stu-id="dbfac-130">Set the **ADS\_SEARCHPREF\_PAGESIZE** search preference to a value less than, or equal to, 1000.</span></span> <span data-ttu-id="dbfac-131">Dies ist optional, aber wenn dies nicht der Fall ist, können nicht mehr als 1000 gelöschte Objekte abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dbfac-131">This is optional, but if this is not done, no more than 1000 deleted objects can be retrieved.</span></span>
5.  <span data-ttu-id="dbfac-132">Legen Sie den Suchfilter im [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) -Aufrufs auf "(IsDeleted =**true**)" fest.</span><span class="sxs-lookup"><span data-stu-id="dbfac-132">Set the search filter in the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) call to "(isDeleted=**TRUE**)".</span></span> <span data-ttu-id="dbfac-133">Dies bewirkt, dass die Suche nur Objekte abruft, bei denen das **isDeleted** -Attribut auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dbfac-133">This causes the search to only retrieve objects with the **isDeleted** attribute set to **TRUE**.</span></span>

<span data-ttu-id="dbfac-134">Ein Codebeispiel Code, in dem das Auflisten von gelöschten Objekten veranschaulicht wird, finden Sie im folgenden Beispiel für eine **enumdeletedobjects** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="dbfac-134">For a code example code that shows how to enumerate deleted objects, see the following **EnumDeletedObjects** function example.</span></span>

<span data-ttu-id="dbfac-135">Die Suche kann weiter verfeinert werden, indem Sie dem Suchfilter hinzufügen, wie im [LDAP-Dialekt](/windows/desktop/ADSI/ldap-dialect)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="dbfac-135">The search can be refined further by adding to the search filter as shown in [LDAP Dialect](/windows/desktop/ADSI/ldap-dialect).</span></span> <span data-ttu-id="dbfac-136">Wenn Sie z. b. nach allen gelöschten Objekten suchen möchten, deren Name mit "Jeff" beginnt, wird der Suchfilter auf "(& (IsDeleted =**true**) (CN = Jeff \* ))" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dbfac-136">For example, to search for all of the deleted objects with a name that begins with "Jeff", the search filter would be set to "(&(isDeleted=**TRUE**)(cn=Jeff\*))".</span></span>

<span data-ttu-id="dbfac-137">Da bei gelöschten Objekten die meisten Attribute entfernt werden, wenn Sie gelöscht werden, ist es nicht möglich, direkt an ein gelöschtes Objekt zu binden.</span><span class="sxs-lookup"><span data-stu-id="dbfac-137">Because deleted objects have most of their attributes removed when they are deleted, it is not possible to bind directly to a deleted object.</span></span> <span data-ttu-id="dbfac-138">Die Option **ADS \_ fast \_ Bind** muss beim Binden an ein gelöschtes Objekt angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dbfac-138">The **ADS\_FAST\_BIND** option must be specified when binding to a deleted object.</span></span> <span data-ttu-id="dbfac-139">Dies bedeutet, dass die ADSI-Schnittstellen, die für die Arbeit mit einem Active Directory Domain Services Objekt verwendet werden, z. b. [**IADs**](/windows/desktop/api/iads/nn-iads-iads) und [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), nicht für einen gelöschten Objekt Container verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="dbfac-139">This means that the ADSI interfaces used to work with an Active Directory Domain Services object, such as [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), cannot be used on a deleted object container.</span></span>

## <a name="finding-a-specific-deleted-object"></a><span data-ttu-id="dbfac-140">Suchen nach einem bestimmten gelöschten Objekt</span><span class="sxs-lookup"><span data-stu-id="dbfac-140">Finding a Specific Deleted Object</span></span>

<span data-ttu-id="dbfac-141">Es ist auch möglich, ein bestimmtes gelöschtes Objekt zu finden.</span><span class="sxs-lookup"><span data-stu-id="dbfac-141">It is also possible to find a specific deleted object.</span></span> <span data-ttu-id="dbfac-142">Wenn die **objectGUID** des Objekts bekannt ist, kann Sie verwendet werden, um nach dem Objekt mit dieser spezifischen **objectGUID** zu suchen.</span><span class="sxs-lookup"><span data-stu-id="dbfac-142">If the **objectGUID** of the object is known, it can be used to search for the object with that specific **objectGUID**.</span></span> <span data-ttu-id="dbfac-143">Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie ein bestimmtes gelöschtes Objekt suchen, finden Sie unten unter **finddeletedobjectbyguid** .</span><span class="sxs-lookup"><span data-stu-id="dbfac-143">For more information and a code example that shows how to find a specific deleted object, see **FindDeletedObjectByGUID** below.</span></span>

### <a name="getdeletedobjectscontainer"></a><span data-ttu-id="dbfac-144">Getdeletedobjectcontainer</span><span class="sxs-lookup"><span data-stu-id="dbfac-144">GetDeletedObjectsContainer</span></span>

<span data-ttu-id="dbfac-145">Im folgenden C++-Codebeispiel wird gezeigt, wie Sie eine Bindung an den Container für gelöschte Objekte herstellen.</span><span class="sxs-lookup"><span data-stu-id="dbfac-145">The following C++ code example shows how to bind to the Deleted Objects container.</span></span>


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



### <a name="enumdeletedobjects"></a><span data-ttu-id="dbfac-146">Enumdeletedobjects</span><span class="sxs-lookup"><span data-stu-id="dbfac-146">EnumDeletedObjects</span></span>

<span data-ttu-id="dbfac-147">Im folgenden C++-Codebeispiel wird gezeigt, wie die-Objekte im Container für gelöschte Objekte aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="dbfac-147">The following C++ code example shows how to enumerate the objects in the Deleted Objects container.</span></span>


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



### <a name="finddeletedobjectbyguid"></a><span data-ttu-id="dbfac-148">Finddeletedobjectbyguid</span><span class="sxs-lookup"><span data-stu-id="dbfac-148">FindDeletedObjectByGUID</span></span>

<span data-ttu-id="dbfac-149">Im folgenden C++-Codebeispiel wird gezeigt, wie Sie ein bestimmtes gelöschtes Objekt aus der **objectGUID** -Eigenschaft des Objekts suchen.</span><span class="sxs-lookup"><span data-stu-id="dbfac-149">The following C++ code example shows how to find a specific deleted object from the object's **objectGUID** property.</span></span>


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



 

 