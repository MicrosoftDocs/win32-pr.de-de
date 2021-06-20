---
description: Unterstützung für COM als Teil des Schreibens eines Transformationsfilters hinzugefügt. Dies ist der letzte Schritt in diesem Tutorial.
ms.assetid: 53e4f5b7-c85d-4b44-9a0c-0ad05ca872cc
title: 'Schritt 6: Hinzufügen von Unterstützung für COM'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097d51fa440812311edde9ce448916c66721a507
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406773"
---
# <a name="step-6-add-support-for-com"></a><span data-ttu-id="744b7-105">Schritt 6:</span><span class="sxs-lookup"><span data-stu-id="744b7-105">Step 6.</span></span> <span data-ttu-id="744b7-106">Hinzufügen von Unterstützung für COM</span><span class="sxs-lookup"><span data-stu-id="744b7-106">Add Support for COM</span></span>

<span data-ttu-id="744b7-107">Dies ist Schritt 6 des Tutorials [Schreiben von Transformationsfiltern.](writing-transform-filters.md)</span><span class="sxs-lookup"><span data-stu-id="744b7-107">This is step 6 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="744b7-108">Der letzte Schritt besteht darin, Unterstützung für COM hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="744b7-108">The final step is to add support for COM.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="744b7-109">Verweiszählung</span><span class="sxs-lookup"><span data-stu-id="744b7-109">Reference Counting</span></span>

<span data-ttu-id="744b7-110">Sie müssen [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) oder [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)nicht implementieren.</span><span class="sxs-lookup"><span data-stu-id="744b7-110">You do not have to implement [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) or [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="744b7-111">Alle Filter- und Stecknadelklassen werden von [**CUnknown**](cunknown.md)abgeleitet, das die Verweiszählung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="744b7-111">All of the filter and pin classes derive from [**CUnknown**](cunknown.md), which handles reference counting.</span></span>

## <a name="queryinterface"></a><span data-ttu-id="744b7-112">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="744b7-112">QueryInterface</span></span>

<span data-ttu-id="744b7-113">Alle Filter- und Stecknadelklassen implementieren [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für alle COM-Schnittstellen, die sie erben.</span><span class="sxs-lookup"><span data-stu-id="744b7-113">All of the filter and pin classes implement [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for any COM interfaces they inherit.</span></span> <span data-ttu-id="744b7-114">Beispielsweise erbt [**CTransformFilter**](ctransformfilter.md) [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (über [**CBaseFilter**](cbasefilter.md)).</span><span class="sxs-lookup"><span data-stu-id="744b7-114">For example, [**CTransformFilter**](ctransformfilter.md) inherits [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (through [**CBaseFilter**](cbasefilter.md)).</span></span> <span data-ttu-id="744b7-115">Wenn Ihr Filter keine zusätzlichen Schnittstellen verfügbar macht, müssen Sie nichts anderes tun.</span><span class="sxs-lookup"><span data-stu-id="744b7-115">If your filter does not expose any additional interfaces, you do not have to do anything else.</span></span>

<span data-ttu-id="744b7-116">Um zusätzliche Schnittstellen verfügbar zu machen, überschreiben Sie die [**CUnknown::NonDelegatingQueryInterface-Methode.**](cunknown-nondelegatingqueryinterface.md)</span><span class="sxs-lookup"><span data-stu-id="744b7-116">To expose additional interfaces, override the [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method.</span></span> <span data-ttu-id="744b7-117">Angenommen, Ihr Filter implementiert eine benutzerdefinierte Schnittstelle mit dem Namen IMyCustomInterface.</span><span class="sxs-lookup"><span data-stu-id="744b7-117">For example, suppose your filter implements a custom interface named IMyCustomInterface.</span></span> <span data-ttu-id="744b7-118">Gehen Sie wie folgt vor, um diese Schnittstelle für Clients verfügbar zu machen:</span><span class="sxs-lookup"><span data-stu-id="744b7-118">To expose this interface to clients, do the following:</span></span>

-   <span data-ttu-id="744b7-119">Leiten Sie Ihre Filterklasse von dieser Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="744b7-119">Derive your filter class from that interface.</span></span>
-   <span data-ttu-id="744b7-120">Legen Sie das [**DECLARE \_ IUNKNOWN-Makro**](declare-iunknown.md) im Abschnitt öffentliche Deklaration ab.</span><span class="sxs-lookup"><span data-stu-id="744b7-120">Put the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section.</span></span>
-   <span data-ttu-id="744b7-121">Überschreiben Sie [**NonDelegatingQueryInterface,**](cunknown-nondelegatingqueryinterface.md) um nach der IID Ihrer Schnittstelle zu suchen und einen Zeiger auf Ihren Filter zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="744b7-121">Override [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IID of your interface and return a pointer to your filter.</span></span>

<span data-ttu-id="744b7-122">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="744b7-122">The following code shows these steps:</span></span>


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



<span data-ttu-id="744b7-123">Weitere Informationen finden Sie unter [Implementieren von IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="744b7-123">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="object-creation"></a><span data-ttu-id="744b7-124">Objekterstellung</span><span class="sxs-lookup"><span data-stu-id="744b7-124">Object Creation</span></span>

<span data-ttu-id="744b7-125">Wenn Sie den Filter in einer DLL packen und für andere Clients verfügbar machen möchten, müssen Sie [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) und andere zugehörige COM-Funktionen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="744b7-125">If you plan to package your filter in a DLL and make it available to other clients, you must support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and other related COM functions.</span></span> <span data-ttu-id="744b7-126">Die Basisklassenbibliothek implementiert die meisten dieser Funktionen. Sie müssen nur einige Informationen zu Ihrem Filter angeben.</span><span class="sxs-lookup"><span data-stu-id="744b7-126">The base class library implements most of this; you just need to provide some information about your filter.</span></span> <span data-ttu-id="744b7-127">Dieser Abschnitt bietet eine kurze Übersicht über die zu erledigende Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="744b7-127">This section gives a brief overview of what to do.</span></span> <span data-ttu-id="744b7-128">Weitere Informationen finden Sie unter [Erstellen einer DirectShow-Filter-DLL.](how-to-create-a-dll.md)</span><span class="sxs-lookup"><span data-stu-id="744b7-128">For details, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="744b7-129">Schreiben Sie zunächst eine statische Klassenmethode, die eine neue Instanz Ihres Filters zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="744b7-129">First, write a static class method that returns a new instance of your filter.</span></span> <span data-ttu-id="744b7-130">Sie können diese Methode beliebig benennen, aber die Signatur muss mit der signatur übereinstimmen, die im folgenden Beispiel gezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="744b7-130">You can name this method anything you like, but the signature must match the one shown in the following example:</span></span>


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



<span data-ttu-id="744b7-131">Deklarieren Sie als Nächstes ein globales Array von [**CFactoryTemplate-Klasseninstanzen**](cfactorytemplate.md) mit dem Namen *g \_ Templates*.</span><span class="sxs-lookup"><span data-stu-id="744b7-131">Next, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) class instances, named *g\_Templates*.</span></span> <span data-ttu-id="744b7-132">Jede **CFactoryTemplate-Klasse** enthält Registrierungsinformationen für einen Filter.</span><span class="sxs-lookup"><span data-stu-id="744b7-132">Each **CFactoryTemplate** class contains registry information for one filter.</span></span> <span data-ttu-id="744b7-133">Mehrere Filter können sich in einer einzelnen DLL befinden. fügen Sie einfach zusätzliche **CFactoryTemplate-Einträge** ein.</span><span class="sxs-lookup"><span data-stu-id="744b7-133">Several filters can reside in a single DLL; simply include additional **CFactoryTemplate** entries.</span></span> <span data-ttu-id="744b7-134">Sie können auch andere COM-Objekte deklarieren, z. B. Eigenschaftenseiten.</span><span class="sxs-lookup"><span data-stu-id="744b7-134">You can also declare other COM objects, such as property pages.</span></span>


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



<span data-ttu-id="744b7-135">Definieren Sie eine globale ganze Zahl mit dem Namen *g \_ cTemplates,* deren Wert der Länge des *g \_ Templates-Arrays* entspricht:</span><span class="sxs-lookup"><span data-stu-id="744b7-135">Define a global integer named *g\_cTemplates* whose value equals the length of the *g\_Templates* array:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



<span data-ttu-id="744b7-136">Implementieren Sie abschließend die DLL-Registrierungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="744b7-136">Finally, implement the DLL registration functions.</span></span> <span data-ttu-id="744b7-137">Das folgende Beispiel zeigt die minimale Implementierung für diese Funktionen:</span><span class="sxs-lookup"><span data-stu-id="744b7-137">The following example shows the minimal implementation for these functions:</span></span>


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



## <a name="filter-registry-entries"></a><span data-ttu-id="744b7-138">Filtern von Registrierungseinträgen</span><span class="sxs-lookup"><span data-stu-id="744b7-138">Filter Registry Entries</span></span>

<span data-ttu-id="744b7-139">Die vorherigen Beispiele zeigen, wie die CLSID eines Filters für COM registriert wird.</span><span class="sxs-lookup"><span data-stu-id="744b7-139">The previous examples show how to register a filter's CLSID for COM.</span></span> <span data-ttu-id="744b7-140">Für viele Filter ist dies ausreichend.</span><span class="sxs-lookup"><span data-stu-id="744b7-140">For many filters, this is sufficient.</span></span> <span data-ttu-id="744b7-141">Vom Client wird dann erwartet, dass er den Filter mitHilfe von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) erstellt und dem Filterdiagramm durch Aufrufen von [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter)hinzufüg.</span><span class="sxs-lookup"><span data-stu-id="744b7-141">The client is then expected to create the filter using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and add it to the filter graph by calling [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span></span> <span data-ttu-id="744b7-142">In einigen Fällen sollten Sie jedoch zusätzliche Informationen zum Filter in der Registrierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="744b7-142">In some cases, however, you might want to provide additional information about the filter in the registry.</span></span> <span data-ttu-id="744b7-143">Diese Informationen haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="744b7-143">This information does the following:</span></span>

-   <span data-ttu-id="744b7-144">Ermöglicht Clients das Ermitteln des Filters mithilfe der [Filterzuordnung](filter-mapper.md) oder des [Systemgeräte-Enumerators.](system-device-enumerator.md)</span><span class="sxs-lookup"><span data-stu-id="744b7-144">Enables clients to discover the filter using the [Filter Mapper](filter-mapper.md) or the [System Device Enumerator](system-device-enumerator.md).</span></span>
-   <span data-ttu-id="744b7-145">Ermöglicht dem Filtergraph-Manager, den Filter während der automatischen Grapherstellung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="744b7-145">Enables the Filter Graph Manager to discover the filter during automatic graph building.</span></span>

<span data-ttu-id="744b7-146">Im folgenden Beispiel wird der RLE-Encoderfilter in der Kategorie Videokomprimierung registriert.</span><span class="sxs-lookup"><span data-stu-id="744b7-146">The following example registers the RLE encoder filter in the video compressor category.</span></span> <span data-ttu-id="744b7-147">Weitere Informationen finden Sie unter [Registrieren von DirectShow-Filtern.](how-to-register-directshow-filters.md)</span><span class="sxs-lookup"><span data-stu-id="744b7-147">For details, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="744b7-148">Lesen Sie unbedingt den Abschnitt [Richtlinien zum Registrieren von Filtern,](guidelines-for-registering-filters.md)in dem die empfohlenen Methoden für die Filterregistrierung beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="744b7-148">Be sure to read the section [Guidelines for Registering Filters](guidelines-for-registering-filters.md), which describes the recommended practices for filter registration.</span></span>


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



<span data-ttu-id="744b7-149">Außerdem müssen Filter nicht in DLLs gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="744b7-149">Also, filters do not have to be packaged inside DLLs.</span></span> <span data-ttu-id="744b7-150">In einigen Fällen können Sie einen speziellen Filter schreiben, der nur für eine bestimmte Anwendung konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="744b7-150">In some cases, you might write a specialized filter that is designed only for a specific application.</span></span> <span data-ttu-id="744b7-151">In diesem Fall können Sie die Filterklasse direkt in Ihrer Anwendung kompilieren und mit dem `new` -Operator erstellen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="744b7-151">In that case, you can compile the filter class directly in your application, and create it with the `new` operator, as shown in the following example:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="744b7-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="744b7-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="744b7-153">Intelligent Connect</span><span class="sxs-lookup"><span data-stu-id="744b7-153">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="744b7-154">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="744b7-154">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="744b7-155">Schreiben von Transformationsfiltern</span><span class="sxs-lookup"><span data-stu-id="744b7-155">Writing Transform Filters</span></span>](writing-transform-filters.md)
</dt> </dl>

 

 
