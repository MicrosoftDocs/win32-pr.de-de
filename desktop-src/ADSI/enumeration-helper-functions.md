---
title: Enumerationshilfsobjekte
description: Es gibt drei enumeratorhilfsfunktionen, die von C/C++ verwendet werden können, um die Navigation von Active Directory-Objekten zu unterstützen. Dabei handelt es sich um ADsBuildEnumerator, adsenumeratenext und adsfreenumerator.
ms.assetid: 019958c8-5bf5-45eb-871c-796ff3750cdc
ms.tgt_platform: multiple
keywords:
- Adsbuildenumschlag ADSI, using
- Adseneneratenext ADSI, using
- Adsfreenumerator ADSI, using
- ADSI ADSI, Beispielcode C/C++, mit ADsBuildEnumerator adsenumeratenext und adsfreenumerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9597787202adf183435262eab9341957e19457
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102338"
---
# <a name="enumeration-helper-functions"></a><span data-ttu-id="f1e77-108">Enumerationshilfsobjekte</span><span class="sxs-lookup"><span data-stu-id="f1e77-108">Enumeration Helper Functions</span></span>

<span data-ttu-id="f1e77-109">Es gibt drei enumeratorhilfsfunktionen, die von C/C++ verwendet werden können, um die Navigation von Active Directory-Objekten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f1e77-109">There are three enumerator helper functions that can be used from C/C++ to aid in the navigation of Active Directory objects.</span></span> <span data-ttu-id="f1e77-110">Dabei handelt es sich um [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**adsenumeratenext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)und [**adsfreenumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).</span><span class="sxs-lookup"><span data-stu-id="f1e77-110">They are [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext), and [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).</span></span>

## <a name="adsbuildenumerator"></a><span data-ttu-id="f1e77-111">Adsbuildenzuerator</span><span class="sxs-lookup"><span data-stu-id="f1e77-111">ADsBuildEnumerator</span></span>

<span data-ttu-id="f1e77-112">Die [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) -Hilfsfunktion kapselt den Code, der zum Erstellen eines Enumeratorobjekts erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f1e77-112">The [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) helper function encapsulates the code required to create an enumerator object.</span></span> <span data-ttu-id="f1e77-113">Die [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) -Methode wird aufgerufen, um ein Enumeratorobjekt zu erstellen, und anschließend wird die [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) aufgerufen, um einen Zeiger auf die [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für dieses Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f1e77-113">It calls the [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) method to create an enumerator object and then calls the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) to get a pointer to the [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface for that object.</span></span> <span data-ttu-id="f1e77-114">Das Enumerationsobjekt ist der Automatisierungs Mechanismus zum Aufzählen von Containern.</span><span class="sxs-lookup"><span data-stu-id="f1e77-114">The enumeration object is the Automation mechanism to enumerate over containers.</span></span> <span data-ttu-id="f1e77-115">Verwenden Sie die [**adsfreenumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) -Funktion, um dieses Enumeratorobjekt freizugeben.</span><span class="sxs-lookup"><span data-stu-id="f1e77-115">Use the [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) function to release this enumerator object.</span></span>

## <a name="adsenumeratenext"></a><span data-ttu-id="f1e77-116">Adsenzueratenext</span><span class="sxs-lookup"><span data-stu-id="f1e77-116">ADsEnumerateNext</span></span>

<span data-ttu-id="f1e77-117">Die Hilfsfunktion [**adsenumeratenext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) füllt ein Variant-Array mit Elementen, die aus einem Enumeratorobjekt abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f1e77-117">The [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) helper function populates a VARIANT array with elements fetched from an enumerator object.</span></span> <span data-ttu-id="f1e77-118">Die Anzahl der abgerufenen Elemente kann kleiner sein als die angeforderte Anzahl.</span><span class="sxs-lookup"><span data-stu-id="f1e77-118">The number of elements retrieved can be smaller than the number requested.</span></span>

## <a name="adsfreeenumerator"></a><span data-ttu-id="f1e77-119">Adsfreenumerator</span><span class="sxs-lookup"><span data-stu-id="f1e77-119">ADsFreeEnumerator</span></span>

<span data-ttu-id="f1e77-120">Gibt ein Enumeratorobjekt frei, das zuvor über die [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) -Funktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f1e77-120">Frees an enumerator object previously created through the [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) function.</span></span>

<span data-ttu-id="f1e77-121">Das folgende Codebeispiel zeigt eine Funktion, die enumeratorhilfsobjekte in C++ verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1e77-121">The following code example shows a function that uses enumerator helper functions in C++.</span></span>


```C++
/*****************************************************************************
  Function:    TestEnumObject
  Arguments:   pszADsPath - ADsPath of the container to be enumerated (WCHAR*).
  Return:      S_OK if successful, an error code otherwise.
  Purpose:     Example using ADsBuildEnumerator, ADsEnumerateNext and
               ADsFreeEnumerator.
******************************************************************************/
#define MAX_ENUM      100  
 
HRESULT
TestEnumObject( LPWSTR pszADsPath )
{
    ULONG cElementFetched = 0L;
    IEnumVARIANT * pEnumVariant = NULL;
    VARIANT VariantArray[MAX_ENUM];
    HRESULT hr = S_OK;
    IADsContainer * pADsContainer =  NULL;
    DWORD dwObjects = 0, dwEnumCount = 0, i = 0;
    BOOL  fContinue = TRUE;
 
 
    hr = ADsGetObject(
                pszADsPath,
                IID_IADsContainer,
                (void **)&pADsContainer
                );
 
 
    if (FAILED(hr)) {
 
        printf("\"%S\" is not a valid container object.\n", pszADsPath) ;
        goto exitpoint ;
    }
 
    hr = ADsBuildEnumerator(
            pADsContainer,
            &pEnumVariant
            );
 
    if( FAILED( hr ) )
    {
      printf("ADsBuildEnumerator failed with %lx\n", hr ) ;
      goto exitpoint ;
    }
 
    fContinue  = TRUE;
    while (fContinue) {
 
        IADs *pObject ;
 
        hr = ADsEnumerateNext(
                    pEnumVariant,
                    MAX_ENUM,
                    VariantArray,
                    &cElementFetched
                    );

        if ( FAILED( hr ) )
        {
            printf("ADsEnumerateNext failed with %lx\n",hr);
            goto exitpoint;
        }
 
        if (hr == S_FALSE) {
            fContinue = FALSE;
        }
 
        dwEnumCount++;
 
        for (i = 0; i < cElementFetched; i++ ) {
 
            IDispatch *pDispatch    = NULL;
            BSTR        bstrADsPath = NULL;
 
            pDispatch = VariantArray[i].pdispVal;
 
            hr = V_DISPATCH( VariantArray + i )->QueryInterface(IID_IADs, (void **) &pObject) ;
 
            if( SUCCEEDED( hr ) )
            {
               pObject->get_ADsPath( &bstrADsPath );
               printf( "%S\n", bstrADsPath );
            }
            pObject->Release();
            VariantClear( VariantArray + i );
            SysFreeString( bstrADsPath );
        }
 
        dwObjects += cElementFetched;
    }
 
    printf("Total Number of Objects enumerated is %d\n", dwObjects);
 
exitpoint:
    if (pEnumVariant) {
        ADsFreeEnumerator( pEnumVariant );
    }
 
    if (pADsContainer) {
        pADsContainer->Release();
    }
 
    return(hr);
}
```



 

 