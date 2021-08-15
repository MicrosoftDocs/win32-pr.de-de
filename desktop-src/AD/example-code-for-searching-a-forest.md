---
title: Beispielcode für die Suche nach einer Gesamtstruktur
description: Dieses Thema enthält Beispielcode, der eine Gesamtstruktur durchsucht.
ms.assetid: 56740e95-548a-4e84-ab2e-2bb7a51b7e1e
ms.tgt_platform: multiple
keywords:
- 'Active Directory-Beispiele: Active Directory, Durchsuchen einer Gesamtstruktur'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92c71afeecebf96ba123e909ad408835de083b8d45cb259a7b371b8214cc5b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118190287"
---
# <a name="example-code-for-searching-a-forest"></a>Beispielcode für die Suche nach einer Gesamtstruktur

Dieses Thema enthält Beispielcode, der eine Gesamtstruktur durchsucht.

Im folgenden C/C++-Codebeispiel wird eine Bindung an den Stamm des globalen Katalogs erstellt, und das einzelne Objekt, das der Stamm der Gesamtstruktur ist, wird aufzählt, sodass es zum Durchsuchen der gesamten Gesamtstruktur verwendet werden kann.


```C++
Set gc = GetObject("GC:")
For each child in gc
    Set entpr = child
Next
' Now entpr is an object that can be used
' to search the entire forest.
```



Das folgende C/C++-Codebeispiel enthält eine Funktion, die einen [**IDirectorySearch-Zeiger**](/windows/desktop/api/iads/nn-iads-idirectorysearch) zurückgibt, mit dem die gesamte Gesamtstruktur durchsucht wird.

Die Funktion führt eine serverlose Bindung an den Stamm des globalen Katalogs aus, enumeriert das einzelne Element, das der Stamm der Gesamtstruktur ist und zum Durchsuchen der gesamten Gesamtstruktur verwendet werden kann, ruft [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, um einen [**IDirectorySearch-Zeiger**](/windows/desktop/api/iads/nn-iads-idirectorysearch) auf das Objekt zu erhalten, und gibt diesen Zeiger zur Verwendung durch den Aufrufer zurück, um die Gesamtstruktur zu durchsuchen.


```C++
HRESULT GetGC(IDirectorySearch **ppDS)
{
HRESULT hr;
IEnumVARIANT *pEnum = NULL;
IADsContainer *pCont = NULL;
VARIANT var;
IDispatch *pDisp = NULL;
ULONG lFetch;
 
// Set IDirectorySearch pointer to NULL.
*ppDS = NULL;
 
// First, bind to the GC: namespace container object. 
hr = ADsOpenObject(TEXT("GC:"),
                NULL,
                NULL,
                ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                IID_IADsContainer,
                (void**)&pCont);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsOpenObject failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Get an enumeration interface for the GC container to enumerate the 
// contents. The actual GC is the only child of the GC container.
hr = ADsBuildEnumerator(pCont, &pEnum);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsBuildEnumerator failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Now enumerate. There is only one child of the GC: object.
hr = pEnum->Next(1, &var, &lFetch);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsEnumerateNext failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Get the IDirectorySearch pointer.
if (( hr == S_OK ) && ( lFetch == 1 ) )     
{    
    pDisp = V_DISPATCH(&var);
    hr = pDisp->QueryInterface( IID_IDirectorySearch, (void**)ppDS); 
}
 
cleanup:
 
if (pEnum)
    ADsFreeEnumerator(pEnum);
if (pCont)
    pCont->Release();
if (pDisp)
    (pDisp)->Release();
return hr;
}
```



 

 