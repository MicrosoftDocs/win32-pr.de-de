---
title: Lesen von attributeSchema-und classSchema-Objekten
description: Dieses Thema enthält Codebeispiele und Richtlinien für das direkte Lesen von attributeSchema-und classSchema-Objekten im Schema Container.
ms.assetid: a60558e1-88a1-493c-9340-a90143b11f60
ms.tgt_platform: multiple
keywords:
- Lesen von attributeSchema-und classSchema-Objekten AD
- Objekte AD, Lesen von attributeSchema-und classSchema-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910d387809f7be8af22d494974021e5e6a47d0ab
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101434"
---
# <a name="reading-attributeschema-and-classschema-objects"></a><span data-ttu-id="39d6c-105">Lesen von attributeSchema-und classSchema-Objekten</span><span class="sxs-lookup"><span data-stu-id="39d6c-105">Reading attributeSchema and classSchema Objects</span></span>

<span data-ttu-id="39d6c-106">Dieses Thema enthält Codebeispiele und Richtlinien für das direkte Lesen von **attributeSchema** -und **classSchema** -Objekten im Schema Container.</span><span class="sxs-lookup"><span data-stu-id="39d6c-106">This topic provides code examples and guidelines for reading directly from **attributeSchema** and **classSchema** objects in the schema container.</span></span> <span data-ttu-id="39d6c-107">Beachten Sie, dass in den meisten Programmier Situationen beim Lesen von Daten über eine Klassen-oder Attribut Definition das Lesen von Daten aus dem abstrakten Schema effektiver ist, wie unter [Lesen des abstrakten Schemas](reading-the-abstract-schema.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="39d6c-107">Be aware that, in most programming situations, when you must read data about a class or attribute definition, it is more effective to read data from the abstract schema as described in [Reading the Abstract Schema](reading-the-abstract-schema.md).</span></span>

<span data-ttu-id="39d6c-108">Die Schnittstellen und Techniken, die zum Lesen aus dem Schema Container verwendet werden, sind diejenigen, die zum Lesen von Objekten in Active Directory Domain Services verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39d6c-108">The interfaces and techniques used to read from the schema container are those used to read any object in Active Directory Domain Services.</span></span> <span data-ttu-id="39d6c-109">Die Richtlinien umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="39d6c-109">The guidelines include:</span></span>

-   <span data-ttu-id="39d6c-110">Um eine Bindung zum Schema Container herzustellen, rufen Sie den Distinguished Name ab, der durch Binden an RootDSE abgerufen werden kann, und lesen Sie die **schemaNamingContext** -Eigenschaft, wie unter [Server lose Bindung und RootDSE](serverless-binding-and-rootdse.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="39d6c-110">To bind to the schema container, obtain its distinguished name which can be retrieved by binding to rootDSE and reading the **schemaNamingContext** property, as described in [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>
-   <span data-ttu-id="39d6c-111">Verwenden Sie einen [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Zeiger für den Schema Container, um die **attributeSchema** -und **classSchema** -Objekte aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="39d6c-111">Use an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer for the schema container to enumerate the **attributeSchema** and **classSchema** objects.</span></span>
-   <span data-ttu-id="39d6c-112">Verwenden Sie die [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -oder [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) -Schnittstelle, um die Eigenschaften eines **attributeSchema** -Objekts und eines **classSchema** -Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="39d6c-112">Use the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) interface to retrieve the properties of an **attributeSchema** and **classSchema** object.</span></span>
-   <span data-ttu-id="39d6c-113">Verwenden Sie die [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) -oder [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) -Funktionen, um direkt an ein **attributeSchema** -oder **classSchema** -Objekt zu binden.</span><span class="sxs-lookup"><span data-stu-id="39d6c-113">Use the [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) or [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) functions to bind directly to an **attributeSchema** or **classSchema** object.</span></span>
-   <span data-ttu-id="39d6c-114">Wenn Sie mehrere **attributeSchema** -oder **classSchema** -Objekte lesen, können Sie die Leistung erhöhen, indem Sie an einen [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Zeiger auf den Schema Container binden und die [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) -Methode verwenden, um eine Bindung an die einzelnen Klassen-und Attribut Objekte herzustellen.</span><span class="sxs-lookup"><span data-stu-id="39d6c-114">If you are reading multiple **attributeSchema** or **classSchema** objects, you can increase performance by binding to an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer on the schema container and using the [**IADsContainer.GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) method to bind to the individual class and attribute objects.</span></span> <span data-ttu-id="39d6c-115">Dies ist effizienter als das Durchführen von wiederholten [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) -oder [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) -aufrufen, um eine Bindung an die einzelnen Klassen-und Attribut Objekte herzustellen.</span><span class="sxs-lookup"><span data-stu-id="39d6c-115">This is more efficient than making repeated [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) or [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) calls to bind to the individual class and attribute objects.</span></span> <span data-ttu-id="39d6c-116">Verwenden Sie das **CN** -Attribut, um den relativen Pfad für den **IADsContainer. GetObject** -aufrufen zu erstellen (z. b. "CN = User" für das **classSchema** -Objekt für die User-Klasse).</span><span class="sxs-lookup"><span data-stu-id="39d6c-116">Use the **cn** attribute to build the relative path for the **IADsContainer.GetObject** call (for example, "cn=user" for the **classSchema** object for the user class).</span></span>
-   <span data-ttu-id="39d6c-117">Verwenden Sie einen [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Zeiger für den Schema Container, um das Schema nach Attributen oder Klassen abzufragen, die einem Suchfilter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="39d6c-117">Use an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer for the schema container to query the schema for attributes or classes that match a search filter.</span></span>

<span data-ttu-id="39d6c-118">Ein Codebeispiel, in dem verschiedene Methoden zum Suchen nach Schema Objekten veranschaulicht werden, finden Sie unter [Beispielcode für die Suche nach Schema Objekten](example-code-for-searching-for-schema-objects.md).</span><span class="sxs-lookup"><span data-stu-id="39d6c-118">For a code example that demonstrates different methods of searching for schema objects, see [Example Code for Searching for Schema Objects](example-code-for-searching-for-schema-objects.md).</span></span>

<span data-ttu-id="39d6c-119">Das folgende C++-Codebeispiel bindet an einen [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Zeiger auf den Schema Container und verwendet dann die [**ADsBuildEnumerator**](/windows/desktop/api/adshlp/nf-adshlp-adsbuildenumerator) -und [**adsenumeratenext**](/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext) -Funktionen, um seinen Inhalt aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="39d6c-119">The following C++ code example binds to an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer on the schema container and then uses the [**ADsBuildEnumerator**](/windows/desktop/api/adshlp/nf-adshlp-adsbuildenumerator) and [**ADsEnumerateNext**](/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext) functions to enumerate its contents.</span></span> <span data-ttu-id="39d6c-120">Beachten Sie, dass die-Enumeration alle **attributeSchema** -und **classSchema** -Objekte sowie ein einzelnes **unter Schema** Objekt enthält, das das abstrakte Schema ist.</span><span class="sxs-lookup"><span data-stu-id="39d6c-120">Be aware that the enumeration includes all **attributeSchema** and **classSchema** objects as well as a single **subSchema** object, which is the abstract schema.</span></span>

<span data-ttu-id="39d6c-121">Im Codebeispiel wird für jedes enumerierte Objekt die [**IADs. Class**](/windows/desktop/ADSI/iads-property-methods) -Eigenschaft verwendet, um zu bestimmen, ob es sich um ein **attributeSchema** -oder **classSchema** -Objekt handelt.</span><span class="sxs-lookup"><span data-stu-id="39d6c-121">For each enumerated object, the code example uses the [**IADs.Class**](/windows/desktop/ADSI/iads-property-methods) property to determine whether it is an **attributeSchema** or **classSchema** object.</span></span> <span data-ttu-id="39d6c-122">Das Codebeispiel zeigt, wie Sie die Eigenschaften lesen, die aus dem abstrakten Schema nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="39d6c-122">The code example shows how to read the properties that are unavailable from the abstract schema.</span></span>


```C++
//  Add activeds.lib to the project.
//  Add adsiid.lib to the project.

#include "stdafx.h"
#include <windows.h>
#include <stdio.h>
#include <ole2.h>
#include <activeds.h>
#include <atlbase.h>

//  Forward declarations.
void ProcessAttribute(IADs *pChild);
void ProcessClass(IADs *pChild);

//  Entry point for the application.
int wmain(int argc, WCHAR* argv[])
{
    HRESULT hr;

    hr = CoInitialize(NULL);
    if(SUCCEEDED(hr))
    {
        CComBSTR sbstrDSPath;
        CComVariant svar;
        IADs *pRootDSE = NULL;
        IADsContainer *pSchema = NULL;  
        IEnumVARIANT *pEnum = NULL;
        ULONG lFetch;
        CComBSTR sbstrClass; 
        DWORD dwClasses = 0, dwAttributes = 0, dwUnknownClass = 0;

        //  Bind to rootDSE to get the schemaNamingContext property.
        hr = ADsGetObject(L"LDAP://rootDSE", IID_IADs, (void**)&pRootDSE);
        if (FAILED(hr)) 
        {
            wprintf(L"ADsGetObject failed: 0x%x\n", hr);
            goto cleanup;
        }

        hr = pRootDSE->Get(CComBSTR("schemaNamingContext"), &svar);
        sbstrDSPath = "LDAP://";
        sbstrDSPath += svar.bstrVal;

        //  Bind to the actual schema container.
        wprintf(L"Binding to %s\n", sbstrDSPath);
        hr = ADsGetObject(sbstrDSPath, IID_IADsContainer, (void**) &pSchema);
        if (FAILED(hr)) 
        {
            wprintf(L"ADsGetObject to schema failed: 0x%x\n", hr);
            goto cleanup;
        }

        //  Enumerate the attribute and class objects in the schema container.
        hr = ADsBuildEnumerator(pSchema, &pEnum);
        if (FAILED(hr)) 
        {
            wprintf(L"ADsBuildEnumerator failed: 0x%x\n", hr);
            goto cleanup;
        }

        hr = ADsEnumerateNext(pEnum, 1, &svar, &lFetch);
        while(S_OK == hr && 1 == lFetch)
        {
            IADs *pChild = NULL;

            //  Get an IADs pointer on the child object.
            hr = V_DISPATCH(&svar)->QueryInterface(IID_IADs, (void**) &pChild);
            if (SUCCEEDED(hr)) 
            {
                //  Verify that this is a class, attribute, or subSchema object.
                hr = pChild->get_Class(&sbstrClass);
                if (SUCCEEDED(hr)) 
                {
                    //  Get data. This depends on type of schema element.
                    if (_wcsicmp(L"classSchema", sbstrClass) == 0)
                    {
                        dwClasses++;
                        wprintf(L"%s\n", sbstrClass);
                        ProcessClass(pChild);
                        wprintf(L"\n");
                    }
                    else if (_wcsicmp(L"attributeSchema", sbstrClass) == 0)
                    {
                        dwAttributes++;
                        wprintf(L"%s\n", sbstrClass);
                        ProcessAttribute(pChild);
                        wprintf(L"\n");
                    }
                    else if (_wcsicmp(L"subSchema", sbstrClass) == 0) 
                    {
                        wprintf(L"abstract schema");
                        wprintf(L"\n");
                    }
                    else
                    {
                        dwUnknownClass++;
                    }
                }

                pChild->Release();
            }

            hr = ADsEnumerateNext(pEnum, 1, &svar, &lFetch);
        }

        wprintf(L"Classes: %u\nAttributes: %u\nUnknown: %u\n", dwClasses, dwAttributes, dwUnknownClass);

cleanup:
        if (pRootDSE)
        {
            pRootDSE->Release();
        }

        if (pEnum)
        {
            ADsFreeEnumerator(pEnum);
        }

        if (pSchema)
        {
            pSchema->Release();
        }

    }    

    CoUninitialize();

    return 0;
}


//  PrintGUIDFromVariant
//  Prints a GUID in string format.
void PrintGUIDFromVariant(VARIANT varGUID)
{
    HRESULT hr;
    void HUGEP *pArray;
    WCHAR szGUID[40];
    LPGUID pGUID;

    DWORD dwLen = sizeof(GUID);

    hr = SafeArrayAccessData(V_ARRAY(&varGUID), &pArray);
    if(SUCCEEDED(hr))
    {
        pGUID = (LPGUID)pArray;

        //  Convert GUID to string.
        StringFromGUID2(*pGUID, szGUID, 40); 

        //  Print GUID.
        wprintf(L",%s",szGUID);

        SafeArrayUnaccessData(V_ARRAY(&varGUID));
    }
}


// PrintADSPropertyValue
void PrintADSPropertyValue(VARIANT var, BSTR bstrPropName, HRESULT hr) 
{
    if (E_ADS_PROPERTY_NOT_FOUND == hr)
    {
        wprintf(L"-- not set --\n");
    }
    else if (FAILED(hr))
    {
        wprintf(L"get %s failed: 0x%x\n", bstrPropName, hr);
    }
    else 
    {
        switch (var.vt) 
        {
        case VT_BSTR:
            wprintf(L"%s\n", var.bstrVal);
            break;

        case VT_I4:
            wprintf(L"%u\n", var.iVal);
            break;

        case VT_BOOL:
            wprintf(L"%s\n", var.boolVal ? L"TRUE" : L"FALSE");
            break;

        default:
            wprintf(L"-- ??? --\n");
        }
    }
}

//  ProcessAttribute
//  Gets information about an attributeClass object.
void ProcessAttribute(IADs *pChild)
{
    HRESULT hr;
    CComVariant svar;
    CComBSTR sbstrPropName;

    //  Get the attribute Common-Name (cn) property. 
    sbstrPropName = "cn";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the attribute lDAPDisplayName.
    sbstrPropName = "lDAPDisplayName";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class linkID. 
    sbstrPropName = "linkID";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the attribute schemaIDGUID. 
    sbstrPropName = "schemaIDGUID";
    hr = pChild->Get(sbstrPropName, &svar);
    if (E_ADS_PROPERTY_NOT_FOUND == hr)
    {
        wprintf(L"-- not set --\n");
    }
    else if(SUCCEEDED(hr))
    {
        PrintGUIDFromVariant(svar);
    }

    //  Get the attribute attributeSecurityGUID. 
    sbstrPropName = "attributeSecurityGUID";
    hr = pChild->Get(sbstrPropName, &svar);
    if (E_ADS_PROPERTY_NOT_FOUND == hr)
    {
        wprintf(L"-- not set --\n");
    }
    else if (SUCCEEDED(hr))
    {
        PrintGUIDFromVariant(svar);
    }

    //  Get the attribute attributeSyntax property. 
    sbstrPropName = "attributeSyntax";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the attribute's oMSyntax property. 
    sbstrPropName = "oMSyntax";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);
}


//  ProcessClass
//  Gets information about a schema class.
void ProcessClass(IADs *pChild)
{
    HRESULT hr;
    CComVariant svar;
    CComBSTR sbstrPropName;

    //  Get the class cn.
    sbstrPropName = "cn";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class lDAPDisplayName.
    sbstrPropName = "lDAPDisplayName";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class schemaIDGUID. 
    sbstrPropName = "schemaIDGUID";
    hr = pChild->Get(sbstrPropName, &svar);
    if (FAILED(hr))
    {
        wprintf(L",get schemaIDGUID failed: 0x%x", hr);
    }
    else 
    {
        PrintGUIDFromVariant(svar);
    }

    //  Get the class adminDescription property. 
    sbstrPropName = "adminDescription";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class adminDisplayName property. 
    sbstrPropName = "adminDisplayName";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class rDNAttID. 
    sbstrPropName = "rDNAttID";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class defaultHidingValue. 
    sbstrPropName = "defaultHidingValue";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class defaultObjectCategory. 
    sbstrPropName = "defaultObjectCategory";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class systemOnly value.
    sbstrPropName = "systemOnly";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class defaultSecurityDescriptor.
    sbstrPropName = "defaultSecurityDescriptor";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);
}
```



 

 