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
# <a name="step-6-add-support-for-com"></a><span data-ttu-id="af93d-104">Schritt 6:</span><span class="sxs-lookup"><span data-stu-id="af93d-104">Step 6.</span></span> <span data-ttu-id="af93d-105">Unterstützung für com hinzufügen</span><span class="sxs-lookup"><span data-stu-id="af93d-105">Add Support for COM</span></span>

<span data-ttu-id="af93d-106">Dies ist Schritt 6 des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="af93d-106">This is step 6 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="af93d-107">Der letzte Schritt besteht im Hinzufügen der Unterstützung für com.</span><span class="sxs-lookup"><span data-stu-id="af93d-107">The final step is to add support for COM.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="af93d-108">Verweis Zählung</span><span class="sxs-lookup"><span data-stu-id="af93d-108">Reference Counting</span></span>

<span data-ttu-id="af93d-109">[**IUnknown:: adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) oder [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)muss nicht implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="af93d-109">You do not have to implement [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) or [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="af93d-110">Alle Filter-und PIN-Klassen werden von [**cunknown**](cunknown.md)abgeleitet, das die Verweis Zählung behandelt.</span><span class="sxs-lookup"><span data-stu-id="af93d-110">All of the filter and pin classes derive from [**CUnknown**](cunknown.md), which handles reference counting.</span></span>

## <a name="queryinterface"></a><span data-ttu-id="af93d-111">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="af93d-111">QueryInterface</span></span>

<span data-ttu-id="af93d-112">Alle Filter-und PIN-Klassen implementieren [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für beliebige com-Schnittstellen, die Sie erben.</span><span class="sxs-lookup"><span data-stu-id="af93d-112">All of the filter and pin classes implement [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for any COM interfaces they inherit.</span></span> <span data-ttu-id="af93d-113">[**Ctransformfilter**](ctransformfilter.md) erbt z. b. [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (über [**cbasefilter**](cbasefilter.md)).</span><span class="sxs-lookup"><span data-stu-id="af93d-113">For example, [**CTransformFilter**](ctransformfilter.md) inherits [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (through [**CBaseFilter**](cbasefilter.md)).</span></span> <span data-ttu-id="af93d-114">Wenn Ihr Filter keine weiteren Schnittstellen verfügbar macht, müssen Sie nichts weiter tun.</span><span class="sxs-lookup"><span data-stu-id="af93d-114">If your filter does not expose any additional interfaces, you do not have to do anything else.</span></span>

<span data-ttu-id="af93d-115">Um zusätzliche Schnittstellen verfügbar zu machen, überschreiben Sie die [**cunknown:: nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="af93d-115">To expose additional interfaces, override the [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method.</span></span> <span data-ttu-id="af93d-116">Nehmen Sie beispielsweise an, dass Ihr Filter eine benutzerdefinierte Schnittstelle namens imycustominterface implementiert.</span><span class="sxs-lookup"><span data-stu-id="af93d-116">For example, suppose your filter implements a custom interface named IMyCustomInterface.</span></span> <span data-ttu-id="af93d-117">Gehen Sie folgendermaßen vor, um diese Schnittstelle für Clients verfügbar zu machen:</span><span class="sxs-lookup"><span data-stu-id="af93d-117">To expose this interface to clients, do the following:</span></span>

-   <span data-ttu-id="af93d-118">Leiten Sie die Filterklasse von dieser Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="af93d-118">Derive your filter class from that interface.</span></span>
-   <span data-ttu-id="af93d-119">Fügen Sie das Makro [**Declare \_ IUnknown**](declare-iunknown.md) in den Abschnitt öffentliche Deklaration ein.</span><span class="sxs-lookup"><span data-stu-id="af93d-119">Put the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section.</span></span>
-   <span data-ttu-id="af93d-120">Überschreiben Sie [**nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md) , um die IID der Schnittstelle zu überprüfen und einen Zeiger auf den Filter zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="af93d-120">Override [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IID of your interface and return a pointer to your filter.</span></span>

<span data-ttu-id="af93d-121">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="af93d-121">The following code shows these steps:</span></span>


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



<span data-ttu-id="af93d-122">Weitere Informationen finden Sie unter Gewusst [wie: Implementieren von IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="af93d-122">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="object-creation"></a><span data-ttu-id="af93d-123">Objekterstellung</span><span class="sxs-lookup"><span data-stu-id="af93d-123">Object Creation</span></span>

<span data-ttu-id="af93d-124">Wenn Sie beabsichtigen, den Filter in einer DLL zu verpacken und für andere Clients verfügbar zu machen, müssen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) und andere verwandte com-Funktionen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="af93d-124">If you plan to package your filter in a DLL and make it available to other clients, you must support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and other related COM functions.</span></span> <span data-ttu-id="af93d-125">Die Basisklassen Bibliothek implementiert den größten Teil dieses. Sie müssen nur einige Informationen zu Ihrem Filter angeben.</span><span class="sxs-lookup"><span data-stu-id="af93d-125">The base class library implements most of this; you just need to provide some information about your filter.</span></span> <span data-ttu-id="af93d-126">In diesem Abschnitt erhalten Sie einen kurzen Überblick über die Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="af93d-126">This section gives a brief overview of what to do.</span></span> <span data-ttu-id="af93d-127">Weitere Informationen finden [Sie unter Erstellen einer DirectShow-Filter-DLL](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="af93d-127">For details, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="af93d-128">Schreiben Sie zunächst eine statische Klassenmethode, die eine neue Instanz des Filters zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="af93d-128">First, write a static class method that returns a new instance of your filter.</span></span> <span data-ttu-id="af93d-129">Sie können diese Methode beliebig benennen, aber die Signatur muss mit der Signatur identisch sein, die im folgenden Beispiel gezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="af93d-129">You can name this method anything you like, but the signature must match the one shown in the following example:</span></span>


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



<span data-ttu-id="af93d-130">Deklarieren Sie als nächstes ein globales Array von [**cfactorytemplate**](cfactorytemplate.md) -Klassen Instanzen mit dem Namen *g \_ Templates*.</span><span class="sxs-lookup"><span data-stu-id="af93d-130">Next, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) class instances, named *g\_Templates*.</span></span> <span data-ttu-id="af93d-131">Jede **cfactorytemplate** -Klasse enthält Registrierungsinformationen für einen Filter.</span><span class="sxs-lookup"><span data-stu-id="af93d-131">Each **CFactoryTemplate** class contains registry information for one filter.</span></span> <span data-ttu-id="af93d-132">Mehrere Filter können sich in einer einzelnen DLL befinden. Fügen Sie einfach zusätzliche **cfactoriytemplate** -Einträge ein.</span><span class="sxs-lookup"><span data-stu-id="af93d-132">Several filters can reside in a single DLL; simply include additional **CFactoryTemplate** entries.</span></span> <span data-ttu-id="af93d-133">Sie können auch andere COM-Objekte deklarieren, z. b. Eigenschaften Seiten.</span><span class="sxs-lookup"><span data-stu-id="af93d-133">You can also declare other COM objects, such as property pages.</span></span>


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



<span data-ttu-id="af93d-134">Definieren Sie eine globale Ganzzahl mit dem Namen *g \_ ctemplates* , deren Wert der Länge des *g- \_ Vorlagen* Arrays gleicht:</span><span class="sxs-lookup"><span data-stu-id="af93d-134">Define a global integer named *g\_cTemplates* whose value equals the length of the *g\_Templates* array:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



<span data-ttu-id="af93d-135">Implementieren Sie schließlich die dll-Registrierungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="af93d-135">Finally, implement the DLL registration functions.</span></span> <span data-ttu-id="af93d-136">Das folgende Beispiel zeigt die minimale Implementierung für diese Funktionen:</span><span class="sxs-lookup"><span data-stu-id="af93d-136">The following example shows the minimal implementation for these functions:</span></span>


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



## <a name="filter-registry-entries"></a><span data-ttu-id="af93d-137">Registrierungseinträge Filtern</span><span class="sxs-lookup"><span data-stu-id="af93d-137">Filter Registry Entries</span></span>

<span data-ttu-id="af93d-138">In den vorherigen Beispielen wird gezeigt, wie die CLSID eines Filters für com registriert wird.</span><span class="sxs-lookup"><span data-stu-id="af93d-138">The previous examples show how to register a filter's CLSID for COM.</span></span> <span data-ttu-id="af93d-139">Für viele Filter ist dies ausreichend.</span><span class="sxs-lookup"><span data-stu-id="af93d-139">For many filters, this is sufficient.</span></span> <span data-ttu-id="af93d-140">Anschließend wird erwartet, dass der Client den Filter mithilfe von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) erstellt und ihn dem Filter Diagramm durch Aufrufen von [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter)hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="af93d-140">The client is then expected to create the filter using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and add it to the filter graph by calling [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span></span> <span data-ttu-id="af93d-141">In einigen Fällen möchten Sie jedoch möglicherweise zusätzliche Informationen über den Filter in der Registrierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="af93d-141">In some cases, however, you might want to provide additional information about the filter in the registry.</span></span> <span data-ttu-id="af93d-142">Diese Informationen werden wie folgt durchführt:</span><span class="sxs-lookup"><span data-stu-id="af93d-142">This information does the following:</span></span>

-   <span data-ttu-id="af93d-143">Ermöglicht Clients das Ermitteln des Filters mithilfe des [Filter Mappers](filter-mapper.md) oder des [System Geräte Enumerators](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="af93d-143">Enables clients to discover the filter using the [Filter Mapper](filter-mapper.md) or the [System Device Enumerator](system-device-enumerator.md).</span></span>
-   <span data-ttu-id="af93d-144">Ermöglicht es dem Filter Graph-Manager, den Filter während der automatischen Diagramm erbaubildung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="af93d-144">Enables the Filter Graph Manager to discover the filter during automatic graph building.</span></span>

<span data-ttu-id="af93d-145">Im folgenden Beispiel wird der RLE-Encoder-Filter in der Kategorie Video-Kompressor registriert.</span><span class="sxs-lookup"><span data-stu-id="af93d-145">The following example registers the RLE encoder filter in the video compressor category.</span></span> <span data-ttu-id="af93d-146">Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="af93d-146">For details, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="af93d-147">Lesen Sie unbedingt den Abschnitt [Richtlinien zum Registrieren von Filtern](guidelines-for-registering-filters.md), in denen die empfohlenen Vorgehensweisen für die Filter Registrierung beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="af93d-147">Be sure to read the section [Guidelines for Registering Filters](guidelines-for-registering-filters.md), which describes the recommended practices for filter registration.</span></span>


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



<span data-ttu-id="af93d-148">Außerdem müssen Filter nicht in DLLs verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="af93d-148">Also, filters do not have to be packaged inside DLLs.</span></span> <span data-ttu-id="af93d-149">In einigen Fällen können Sie einen speziellen Filter schreiben, der nur für eine bestimmte Anwendung entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="af93d-149">In some cases, you might write a specialized filter that is designed only for a specific application.</span></span> <span data-ttu-id="af93d-150">In diesem Fall können Sie die Filterklasse direkt in der Anwendung kompilieren und mit dem- `new` Operator erstellen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="af93d-150">In that case, you can compile the filter class directly in your application, and create it with the `new` operator, as shown in the following example:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="af93d-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af93d-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af93d-152">Intelligent Connect</span><span class="sxs-lookup"><span data-stu-id="af93d-152">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="af93d-153">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="af93d-153">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="af93d-154">Schreiben von Transformations Filtern</span><span class="sxs-lookup"><span data-stu-id="af93d-154">Writing Transform Filters</span></span>](writing-transform-filters.md)
</dt> </dl>

 

 
