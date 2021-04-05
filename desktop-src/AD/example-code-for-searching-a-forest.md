---
title: Beispiel Code für das Durchsuchen einer Gesamtstruktur
description: Dieses Thema enthält Beispielcode, der eine Gesamtstruktur durchsucht.
ms.assetid: 56740e95-548a-4e84-ab2e-2bb7a51b7e1e
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, Durchsuchen einer Gesamtstruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c2fb0cde0f42167b19141ad178ea80ff8795b8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724528"
---
# <a name="example-code-for-searching-a-forest"></a>Beispiel Code für das Durchsuchen einer Gesamtstruktur

Dieses Thema enthält Beispielcode, der eine Gesamtstruktur durchsucht.

Das folgende C/C++-Codebeispiel bindet an den Stamm des globalen Katalogs und listet das einzelne-Objekt auf, das das Stammverzeichnis der Gesamtstruktur ist, sodass es zum Durchsuchen der gesamten Gesamtstruktur verwendet werden kann.


```C++
Set gc = GetObject("GC:")
For each child in gc
    Set entpr = child
Next
' Now entpr is an object that can be used
' to search the entire forest.
```



Das folgende C/C++-Codebeispiel enthält eine Funktion, die einen [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Zeiger zurückgibt, der zum Durchsuchen der gesamten Gesamtstruktur verwendet wird.

Die-Funktion führt eine Server lose Bindung an den Stamm des globalen Katalogs aus, zählt das einzelne Element auf, das der Stamm der Gesamtstruktur ist, und kann zum Durchsuchen der gesamten Gesamtstruktur verwendet werden, ruft [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, um einen [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Zeiger auf das Objekt zu erhalten, und gibt diesen Zeiger zurück, damit der Aufrufer die Gesamtstruktur durchsucht


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



 

 