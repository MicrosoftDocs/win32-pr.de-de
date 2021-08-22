---
title: Enumerationshilfsfunktionen
description: Es gibt drei Enumeratorhilfsfunktionen, die von C/C++ verwendet werden können, um die Navigation von Active Directory-Objekten zu unterstützen. Dabei handelt es sich um ADsBuildEnumerator, ADsEnumerateNext und ADsFreeEnumerator.
ms.assetid: 019958c8-5bf5-45eb-871c-796ff3750cdc
ms.tgt_platform: multiple
keywords:
- ADsBuildEnumerator ADSI mit
- ADsEnumerateNext ADSI mit
- ADsFreeEnumerator ADSI mit
- ADSI ADSI, Beispielcode C/C++ mit ADsBuildEnumerator ADsEnumerateNext und ADsFreeEnumerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c110fbc4fddd420bf8205d6c2d894c7d4f4daf8287312c2d0d86002f5520310b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082654"
---
# <a name="enumeration-helper-functions"></a>Enumerationshilfsfunktionen

Es gibt drei Enumeratorhilfsfunktionen, die von C/C++ verwendet werden können, um die Navigation von Active Directory-Objekten zu unterstützen. Dabei handelt [**es sich um ADsBuildEnumerator,**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)und [**ADsFreeEnumerator.**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)

## <a name="adsbuildenumerator"></a>ADsBuildEnumerator

Die [**Hilfsfunktion ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) kapselt den Code, der zum Erstellen eines Enumeratorobjekts erforderlich ist. Sie ruft die [**IADsContainer::get \_ \_ NewEnum-Methode**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) auf, um ein Enumeratorobjekt zu erstellen, und ruft dann die [**QueryInterface-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) auf, um einen Zeiger auf die [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für dieses Objekt abzurufen. Das Enumerationsobjekt ist der Automatisierungsmechanismus zum Aufzählen von Containern. Verwenden Sie die [**ADsFreeEnumerator-Funktion,**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) um dieses Enumeratorobjekt freizugeben.

## <a name="adsenumeratenext"></a>ADsEnumerateNext

Die [**Hilfsfunktion ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) füllt ein VARIANT-Array mit Elementen auf, die aus einem Enumeratorobjekt abgerufen werden. Die Anzahl der abgerufenen Elemente kann kleiner als die angeforderte Anzahl sein.

## <a name="adsfreeenumerator"></a>ADsFreeEnumerator

Gibt ein Enumeratorobjekt frei, das zuvor über die [**ADsBuildEnumerator-Funktion**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) erstellt wurde.

Das folgende Codebeispiel zeigt eine Funktion, die Enumeratorhilfsfunktionen in C++ verwendet.


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



 

 