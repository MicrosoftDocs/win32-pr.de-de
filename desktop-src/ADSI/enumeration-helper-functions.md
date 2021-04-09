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
# <a name="enumeration-helper-functions"></a>Enumerationshilfsobjekte

Es gibt drei enumeratorhilfsfunktionen, die von C/C++ verwendet werden können, um die Navigation von Active Directory-Objekten zu unterstützen. Dabei handelt es sich um [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**adsenumeratenext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)und [**adsfreenumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).

## <a name="adsbuildenumerator"></a>Adsbuildenzuerator

Die [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) -Hilfsfunktion kapselt den Code, der zum Erstellen eines Enumeratorobjekts erforderlich ist. Die [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) -Methode wird aufgerufen, um ein Enumeratorobjekt zu erstellen, und anschließend wird die [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) aufgerufen, um einen Zeiger auf die [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für dieses Objekt zu erhalten. Das Enumerationsobjekt ist der Automatisierungs Mechanismus zum Aufzählen von Containern. Verwenden Sie die [**adsfreenumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) -Funktion, um dieses Enumeratorobjekt freizugeben.

## <a name="adsenumeratenext"></a>Adsenzueratenext

Die Hilfsfunktion [**adsenumeratenext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) füllt ein Variant-Array mit Elementen, die aus einem Enumeratorobjekt abgerufen werden. Die Anzahl der abgerufenen Elemente kann kleiner sein als die angeforderte Anzahl.

## <a name="adsfreeenumerator"></a>Adsfreenumerator

Gibt ein Enumeratorobjekt frei, das zuvor über die [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) -Funktion erstellt wurde.

Das folgende Codebeispiel zeigt eine Funktion, die enumeratorhilfsobjekte in C++ verwendet.


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



 

 