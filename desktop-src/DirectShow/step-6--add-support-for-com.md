---
description: Unterstützung für COM beim Schreiben eines Transformationsfilters hinzugefügt. Dies ist der letzte Schritt in diesem Tutorial.
ms.assetid: 53e4f5b7-c85d-4b44-9a0c-0ad05ca872cc
title: 'Schritt 6: Hinzufügen von Unterstützung für COM'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354299ed9ed2f752e0041b82af712e7a9c5411eb7bb7e16588267183442edf68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964900"
---
# <a name="step-6-add-support-for-com"></a>Schritt 6: Hinzufügen von Unterstützung für COM

Dies ist Schritt 6 des Tutorials [Schreiben von Transformationsfiltern](writing-transform-filters.md).

Der letzte Schritt besteht im Hinzufügen von Unterstützung für COM.

## <a name="reference-counting"></a>Verweiszählung

Sie müssen [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) oder [**IUnknown::Release nicht implementieren.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) Alle Filter- und Pinklassen werden von [**CUnknown**](cunknown.md)ableiten, das die Verweiszählung verarbeitet.

## <a name="queryinterface"></a>QueryInterface

Alle Filter- und Pinklassen implementieren [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für alle COM-Schnittstellen, die sie erben. [**CTransformFilter**](ctransformfilter.md) erbt beispielsweise [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (über [**CBaseFilter).**](cbasefilter.md) Wenn Ihr Filter keine zusätzlichen Schnittstellen verfügbar macht, müssen Sie nichts anderes tun.

Um zusätzliche Schnittstellen verfügbar zu machen, überschreiben Sie [**die CUnknown::NonDelegatingQueryInterface-Methode.**](cunknown-nondelegatingqueryinterface.md) Angenommen, Ihr Filter implementiert eine benutzerdefinierte Schnittstelle namens IMyCustomInterface. Gehen Sie wie folgt vor, um diese Schnittstelle für Clients verfügbar zu machen:

-   Leiten Sie ihre Filterklasse von dieser Schnittstelle ab.
-   Legen Sie das [**DECLARE \_ IUNKNOWN-Makro**](declare-iunknown.md) im Abschnitt öffentliche Deklaration ab.
-   Überschreiben [**Sie NonDelegatingQueryInterface,**](cunknown-nondelegatingqueryinterface.md) um die IID Ihrer Schnittstelle zu überprüfen und einen Zeiger auf Ihren Filter zurück.

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



Weitere Informationen finden Sie unter [Implementieren von IUnknown](how-to-implement-iunknown.md).

## <a name="object-creation"></a>Objekterstellung

Wenn Sie ihren Filter in einer DLL packen und anderen Clients zur Verfügung stellen möchten, müssen Sie [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) und andere zugehörige COM-Funktionen unterstützen. Die Basisklassenbibliothek implementiert den größten Teil davon. Sie müssen lediglich einige Informationen zu Ihrem Filter bereitstellen. Dieser Abschnitt bietet eine kurze Übersicht über die zu verwendenden Informationen. Weitere Informationen finden Sie unter [Erstellen einer DirectShow-Filter-DLL.](how-to-create-a-dll.md)

Schreiben Sie zunächst eine statische Klassenmethode, die eine neue Instanz des Filters zurückgibt. Sie können dieser Methode einen anderen Namen geben, aber die Signatur muss mit der im folgenden Beispiel gezeigten übereinstimmen:


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



Deklarieren Sie als Nächstes ein globales Array von [**CFactoryTemplate-Klasseninstanzen**](cfactorytemplate.md) mit dem Namen *g \_ Templates*. Jede **CFactoryTemplate-Klasse** enthält Registrierungsinformationen für einen Filter. Mehrere Filter können sich in einer einzelnen DLL befinden. fügen Sie einfach zusätzliche **CFactoryTemplate-Einträge** ein. Sie können auch andere COM-Objekte deklarieren, z. B. Eigenschaftenseiten.


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



Definieren Sie eine globale ganze Zahl mit dem Namen *g \_ cTemplates,* deren Wert der Länge des *g \_ Templates-Arrays* entspricht:


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



Implementieren Sie abschließend die DLL-Registrierungsfunktionen. Das folgende Beispiel zeigt die minimale Implementierung für diese Funktionen:


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



## <a name="filter-registry-entries"></a>Filtern von Registrierungseinträgen

In den vorherigen Beispielen wird gezeigt, wie die CLSID eines Filters für COM registriert wird. Bei vielen Filtern ist dies ausreichend. Anschließend wird erwartet, dass der Client den Filter mitHilfe von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) erstellt und dem Filterdiagramm durch Aufrufen von [**IFilterGraph::AddFilter hinzufüge.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) In einigen Fällen möchten Sie jedoch möglicherweise zusätzliche Informationen zum Filter in der Registrierung bereitstellen. Diese Informationen führen folgende Schritte aus:

-   Ermöglicht Clients, den Filter mithilfe der [Filterzuordnung oder](filter-mapper.md) des [Systemgeräte-Enumerators zu finden.](system-device-enumerator.md)
-   Ermöglicht dem Filter Graph-Manager, den Filter während der automatischen Graph-Entwicklung zu finden.

Im folgenden Beispiel wird der RLE-Encoderfilter in der Kategorie Videovideovideo registriert. Weitere Informationen finden Sie unter [Registrieren von DirectShow-Filtern.](how-to-register-directshow-filters.md) Lesen Sie unbedingt den Abschnitt Richtlinien zum [Registrieren von Filtern,](guidelines-for-registering-filters.md)in dem die empfohlenen Methoden für die Filterregistrierung beschrieben werden.


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



Außerdem müssen Filter nicht in DLLs gepackt werden. In einigen Fällen können Sie einen speziellen Filter schreiben, der nur für eine bestimmte Anwendung entwickelt wurde. In diesem Fall können Sie die Filterklasse direkt in Ihrer Anwendung kompilieren und mit dem Operator erstellen, wie `new` im folgenden Beispiel gezeigt:


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

[Intelligente Verbinden](intelligent-connect.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> <dt>

[Schreiben von Transformationsfiltern](writing-transform-filters.md)
</dt> </dl>

 

 
