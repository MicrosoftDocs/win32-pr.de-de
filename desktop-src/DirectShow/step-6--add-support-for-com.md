---
description: 'Schritt 6:'
ms.assetid: 53e4f5b7-c85d-4b44-9a0c-0ad05ca872cc
title: 'Schritt 6: Unterstützung für com hinzufügen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e477cc22650604bce623874c0afbba1063609e44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369749"
---
# <a name="step-6-add-support-for-com"></a>Schritt 6: Unterstützung für com hinzufügen

Dies ist Schritt 6 des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).

Der letzte Schritt besteht im Hinzufügen der Unterstützung für com.

## <a name="reference-counting"></a>Verweis Zählung

[**IUnknown:: adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) oder [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)muss nicht implementiert werden. Alle Filter-und PIN-Klassen werden von [**cunknown**](cunknown.md)abgeleitet, das die Verweis Zählung behandelt.

## <a name="queryinterface"></a>QueryInterface

Alle Filter-und PIN-Klassen implementieren [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für beliebige com-Schnittstellen, die Sie erben. [**Ctransformfilter**](ctransformfilter.md) erbt z. b. [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (über [**cbasefilter**](cbasefilter.md)). Wenn Ihr Filter keine weiteren Schnittstellen verfügbar macht, müssen Sie nichts weiter tun.

Um zusätzliche Schnittstellen verfügbar zu machen, überschreiben Sie die [**cunknown:: nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md) -Methode. Nehmen Sie beispielsweise an, dass Ihr Filter eine benutzerdefinierte Schnittstelle namens imycustominterface implementiert. Gehen Sie folgendermaßen vor, um diese Schnittstelle für Clients verfügbar zu machen:

-   Leiten Sie die Filterklasse von dieser Schnittstelle ab.
-   Fügen Sie das Makro [**Declare \_ IUnknown**](declare-iunknown.md) in den Abschnitt öffentliche Deklaration ein.
-   Überschreiben Sie [**nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md) , um die IID der Schnittstelle zu überprüfen und einen Zeiger auf den Filter zurückzugeben.

Diese Schritte sind im folgenden Code dargestellt:


```C++
CMyFilter : public CBaseFilter, public IMyCustomInterface
{
public:
    DECLARE_IUNKNOWN
    STDMETHODIMP NonDelegatingQueryInterface(REFIID iid, void **ppv);
};
STDMETHODIMP CMyFilter::NonDelegatingQueryInterface(REFIID iid, void **ppv)
{
    if (riid == IID_IMyCustomInterface) {
        return GetInterface(static_cast<IMyCustomInterface*>(this), ppv);
    }
    return CBaseFilter::NonDelegatingQueryInterface(riid,ppv);
}
```



Weitere Informationen finden Sie unter Gewusst [wie: Implementieren von IUnknown](how-to-implement-iunknown.md).

## <a name="object-creation"></a>Objekterstellung

Wenn Sie beabsichtigen, den Filter in einer DLL zu verpacken und für andere Clients verfügbar zu machen, müssen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) und andere verwandte com-Funktionen unterstützen. Die Basisklassen Bibliothek implementiert den größten Teil dieses. Sie müssen nur einige Informationen zu Ihrem Filter angeben. In diesem Abschnitt erhalten Sie einen kurzen Überblick über die Vorgehensweise. Weitere Informationen finden [Sie unter Erstellen einer DirectShow-Filter-DLL](how-to-create-a-dll.md).

Schreiben Sie zunächst eine statische Klassenmethode, die eine neue Instanz des Filters zurückgibt. Sie können diese Methode beliebig benennen, aber die Signatur muss mit der Signatur identisch sein, die im folgenden Beispiel gezeigt wird:


```C++
CUnknown * WINAPI CRleFilter::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr)
{
    CRleFilter *pFilter = new CRleFilter();
    if (pFilter== NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pFilter;
}
```



Deklarieren Sie als nächstes ein globales Array von [**cfactorytemplate**](cfactorytemplate.md) -Klassen Instanzen mit dem Namen *g \_ Templates*. Jede **cfactorytemplate** -Klasse enthält Registrierungsinformationen für einen Filter. Mehrere Filter können sich in einer einzelnen DLL befinden. Fügen Sie einfach zusätzliche **cfactoriytemplate** -Einträge ein. Sie können auch andere COM-Objekte deklarieren, z. b. Eigenschaften Seiten.


```C++
static WCHAR g_wszName[] = L"My RLE Encoder";
CFactoryTemplate g_Templates[] = 
{
  { 
    g_wszName,
    &CLSID_RLEFilter,
    CRleFilter::CreateInstance,
    NULL,
    NULL
  }
};
```



Definieren Sie eine globale Ganzzahl mit dem Namen *g \_ ctemplates* , deren Wert der Länge des *g- \_ Vorlagen* Arrays gleicht:


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



Implementieren Sie schließlich die dll-Registrierungsfunktionen. Das folgende Beispiel zeigt die minimale Implementierung für diese Funktionen:


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}
STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



## <a name="filter-registry-entries"></a>Registrierungseinträge Filtern

In den vorherigen Beispielen wird gezeigt, wie die CLSID eines Filters für com registriert wird. Für viele Filter ist dies ausreichend. Anschließend wird erwartet, dass der Client den Filter mithilfe von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) erstellt und ihn dem Filter Diagramm durch Aufrufen von [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter)hinzufügt. In einigen Fällen möchten Sie jedoch möglicherweise zusätzliche Informationen über den Filter in der Registrierung bereitstellen. Diese Informationen werden wie folgt durchführt:

-   Ermöglicht Clients das Ermitteln des Filters mithilfe des [Filter Mappers](filter-mapper.md) oder des [System Geräte Enumerators](system-device-enumerator.md).
-   Ermöglicht es dem Filter Graph-Manager, den Filter während der automatischen Diagramm erbaubildung zu ermitteln.

Im folgenden Beispiel wird der RLE-Encoder-Filter in der Kategorie Video-Kompressor registriert. Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md). Lesen Sie unbedingt den Abschnitt [Richtlinien zum Registrieren von Filtern](guidelines-for-registering-filters.md), in denen die empfohlenen Vorgehensweisen für die Filter Registrierung beschrieben werden.


```C++
// Declare media type information.
FOURCCMap fccMap = FCC('MRLE'); 
REGPINTYPES sudInputTypes = { &MEDIATYPE_Video, &GUID_NULL };
REGPINTYPES sudOutputTypes = { &MEDIATYPE_Video, (GUID*)&fccMap };

// Declare pin information.
REGFILTERPINS sudPinReg[] = {
    // Input pin.
    { 0, FALSE, // Rendered?
         FALSE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudInputTypes  // Media types.
    },
    // Output pin.
    { 0, FALSE, // Rendered?
         TRUE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudOutputTypes      // Media types.
    }
};
 
// Declare filter information.
REGFILTER2 rf2FilterReg = {
    1,                // Version number.
    MERIT_DO_NOT_USE, // Merit.
    2,                // Number of pins.
    sudPinReg         // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->RegisterFilter(
            CLSID_RLEFilter,                // Filter CLSID. 
            g_wszName,                       // Filter name.
            NULL,                            // Device moniker. 
            &CLSID_VideoCompressorCategory,  // Video compressor category.
            g_wszName,                       // Instance data.
            &rf2FilterReg                    // Filter information.
            );
        pFM2->Release();
    }
    return hr;
}

STDAPI DllUnregisterServer()
{
    HRESULT hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_RLEFilter);
        pFM2->Release();
    }
    return hr;
}
```



Außerdem müssen Filter nicht in DLLs verpackt werden. In einigen Fällen können Sie einen speziellen Filter schreiben, der nur für eine bestimmte Anwendung entworfen wurde. In diesem Fall können Sie die Filterklasse direkt in der Anwendung kompilieren und mit dem- `new` Operator erstellen, wie im folgenden Beispiel gezeigt:


```C++
#include "MyFilter.h"  // Header file that declares the filter class.
// Compile and link MyFilter.cpp.
int main()
{
    IBaseFilter *pFilter = 0;
    {
        // Scope to hide pF.
        CMyFilter* pF = new MyFilter();
        if (!pF)
        {
            printf("Could not create MyFilter.\n");
            return 1;
        }
        pF->QueryInterface(IID_IBaseFilter, 
            reinterpret_cast<void**>(&pFilter));
    }
    
    /* Now use pFilter as normal. */
    
    pFilter->Release();  // Deletes the filter.
    return 0;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Intelligent Connect](intelligent-connect.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> <dt>

[Schreiben von Transformations Filtern](writing-transform-filters.md)
</dt> </dl>

 

 
