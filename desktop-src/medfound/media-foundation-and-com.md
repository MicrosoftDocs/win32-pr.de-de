---
description: Microsoft Media Foundation verwendet eine Mischung aus com-Konstrukten, ist aber keine vollständig com-basierte API.
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: Media Foundation und com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb7d05bac6a3f4deef2c004c6980ef1351c3823
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106353260"
---
# <a name="media-foundation-and-com"></a><span data-ttu-id="be8ac-103">Media Foundation und com</span><span class="sxs-lookup"><span data-stu-id="be8ac-103">Media Foundation and COM</span></span>

<span data-ttu-id="be8ac-104">Microsoft Media Foundation verwendet eine Mischung aus com-Konstrukten, ist aber keine vollständig com-basierte API.</span><span class="sxs-lookup"><span data-stu-id="be8ac-104">Microsoft Media Foundation uses a mix of COM constructs, but is not a fully COM-based API.</span></span> <span data-ttu-id="be8ac-105">In diesem Thema wird die Interaktion zwischen com und Media Foundation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="be8ac-105">This topic describes the interaction between COM and Media Foundation.</span></span> <span data-ttu-id="be8ac-106">Außerdem werden einige bewährte Methoden für die Entwicklung von Media Foundation-Plug-in-Komponenten definiert.</span><span class="sxs-lookup"><span data-stu-id="be8ac-106">It also defines some best practices for developing Media Foundation plug-in components.</span></span> <span data-ttu-id="be8ac-107">Die folgenden Vorgehensweisen helfen Ihnen, einige häufige, aber feine Programmierfehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="be8ac-107">Following these practices can help you to avoid some common but subtle programming errors.</span></span>

-   [<span data-ttu-id="be8ac-108">Bewährte Methoden für Anwendungen</span><span class="sxs-lookup"><span data-stu-id="be8ac-108">Best Practices for Applications</span></span>](#best-practices-for-applications)
-   [<span data-ttu-id="be8ac-109">Bewährte Methoden für Media Foundation Komponenten</span><span class="sxs-lookup"><span data-stu-id="be8ac-109">Best Practices for Media Foundation Components</span></span>](#best-practices-for-media-foundation-components)
-   [<span data-ttu-id="be8ac-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="be8ac-110">Summary</span></span>](#summary)
-   [<span data-ttu-id="be8ac-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be8ac-111">Related topics</span></span>](#related-topics)

## <a name="best-practices-for-applications"></a><span data-ttu-id="be8ac-112">Bewährte Methoden für Anwendungen</span><span class="sxs-lookup"><span data-stu-id="be8ac-112">Best Practices for Applications</span></span>

<span data-ttu-id="be8ac-113">In Media Foundation werden die asynchrone Verarbeitung und Rückrufe von [Arbeits Warteschlangen](work-queues.md)verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="be8ac-113">In Media Foundation, asynchronous processing and callbacks are handled by [work queues](work-queues.md).</span></span> <span data-ttu-id="be8ac-114">Arbeits Warteschlangen verfügen immer über Multithread-Apartment-Threads (MTA), sodass eine Anwendung eine einfachere Implementierung hat, wenn Sie auch in einem MTA-Thread ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be8ac-114">Work queues always have multithreaded apartment (MTA) threads, so an application will have a simpler implementation if it runs on an MTA thread as well.</span></span> <span data-ttu-id="be8ac-115">Daher wird empfohlen, [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) mit dem **coinit- \_ Multithreaded** -Flag aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="be8ac-115">Therefore, it is recommended to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.</span></span>

<span data-ttu-id="be8ac-116">Mit Media Foundation werden keine STA-Objekte (Single Thread Apartment) in Arbeitswarteschlangen-Threads gemarshallt.</span><span class="sxs-lookup"><span data-stu-id="be8ac-116">Media Foundation does not marshal single-threaded apartment (STA) objects to work queue threads.</span></span> <span data-ttu-id="be8ac-117">Außerdem wird nicht sichergestellt, dass STA-invarianten verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="be8ac-117">Nor does it ensure that STA invariants are maintained.</span></span> <span data-ttu-id="be8ac-118">Daher muss eine STA-Anwendung darauf achten, STA-Objekte oder-Proxys nicht an Media Foundation-APIs zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="be8ac-118">Therefore, an STA application must be careful to not pass STA objects or proxies to Media Foundation APIs.</span></span> <span data-ttu-id="be8ac-119">Objekte, die nur STA-Objekte sind, werden in Media Foundation nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="be8ac-119">Objects that are STA-only are not supported in Media Foundation.</span></span>

<span data-ttu-id="be8ac-120">Wenn Sie über einen STA-Proxy für einen MTA oder ein frei Thread Objekt verfügen, kann das Objekt mithilfe eines Arbeits Warteschlangen Rückrufs an einen MTA-Proxy gemarshallt werden.</span><span class="sxs-lookup"><span data-stu-id="be8ac-120">If you have an STA proxy to an MTA or free-threaded object, the object can be marshaled to an MTA proxy by using a work-queue callback.</span></span> <span data-ttu-id="be8ac-121">Abhängig vom Objektmodell, das in der Registrierung für diese CLSID definiert ist, kann die [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion entweder einen Rohdaten Zeiger oder einen STA-Proxy zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="be8ac-121">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function can return either a raw pointer or an STA proxy, depending on the object model defined in the registry for that CLSID.</span></span> <span data-ttu-id="be8ac-122">Wenn ein STA-Proxy zurückgegeben wird, dürfen Sie den Zeiger nicht an eine Media Foundation-API übergeben.</span><span class="sxs-lookup"><span data-stu-id="be8ac-122">If an STA proxy is returned, you must not pass the pointer to a Media Foundation API.</span></span>

<span data-ttu-id="be8ac-123">Angenommen, Sie möchten einen **IPropertyStore** -Zeiger an die [**imfsourceresolver:: beginkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="be8ac-123">For example, suppose that you want to pass an **IPropertyStore** pointer to the [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method.</span></span> <span data-ttu-id="be8ac-124">Sie können **pscreatememorypropertystore** aufrufen, um den **IPropertyStore** -Zeiger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="be8ac-124">You might call **PSCreateMemoryPropertyStore** to create the **IPropertyStore** pointer.</span></span> <span data-ttu-id="be8ac-125">Wenn Sie von einem STA aufrufen, müssen Sie den Zeiger vor dem übergeben an **begincreateobjectfromurl** Mars Hallen.</span><span class="sxs-lookup"><span data-stu-id="be8ac-125">If you are calling from an STA, you must marshal the pointer before passing it to **BeginCreateObjectFromURL**.</span></span>

<span data-ttu-id="be8ac-126">Der folgende Code zeigt, wie ein STA-Proxy in eine Media Foundation-API gemarshallt wird.</span><span class="sxs-lookup"><span data-stu-id="be8ac-126">The following code shows how to marshal an STA proxy to a Media Foundation API.</span></span>


```C++
class CCreateSourceMarshalCallback
    : public IMFAsyncCallback
{
public:
    CCreateSourceMarshalCallback(
        LPCWSTR szURL, 
        IMFSourceResolver* pResolver, 
        IPropertyStore* pSourceProps, 
        IMFAsyncCallback* pCompletionCallback, 
        HRESULT& hr
        )
        : m_szURL(szURL), 
          m_pResolver(pResolver), 
          m_pCompletionCallback(pCompletionCallback),
          m_pGIT(NULL),
          m_cRef(1)
    {
        hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable, NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGIT));

        if(SUCCEEDED(hr))
        {
            hr = m_pGIT->RegisterInterfaceInGlobal(
                pSourceProps, IID_IPropertyStore, &m_dwInterfaceCookie);
        }
    }
    ~CCreateSourceMarshalCallback()
    {
        SafeRelease(&m_pResolver);
        SafeRelease(&m_pCompletionCallback);
        SafeRelease(&m_pGIT);
    }


    STDMETHOD_(ULONG, AddRef)()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHOD_(ULONG, Release)()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (0 == cRef)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHOD(QueryInterface)(REFIID riid, LPVOID* ppvObject)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCreateSourceMarshalCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppvObject);

    }

    STDMETHOD(GetParameters)(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHOD(Invoke)(IMFAsyncResult* pResult)
    {
        IPropertyStore *pSourceProps = NULL;

        HRESULT hr = m_pGIT->GetInterfaceFromGlobal(
            m_dwInterfaceCookie, 
            IID_PPV_ARGS(&pSourceProps)
            );

        if(SUCCEEDED(hr))
        {
            hr = m_pResolver->BeginCreateObjectFromURL(
                m_szURL, MF_RESOLUTION_MEDIASOURCE, pSourceProps, NULL, 
                m_pCompletionCallback, NULL);
        }

        SafeRelease(&pSourceProps);
        return hr;
    }

private:
    LPCWSTR m_szURL;
    IMFSourceResolver *m_pResolver;
    IMFAsyncCallback *m_pCompletionCallback;
    IGlobalInterfaceTable *m_pGIT;
    DWORD m_dwInterfaceCookie;
    LONG m_cRef;
};
```



<span data-ttu-id="be8ac-127">Weitere Informationen zur globalen Schnittstellen Tabelle finden Sie unter [**iglobalinterfaketable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span><span class="sxs-lookup"><span data-stu-id="be8ac-127">For more information about the global interface table, see [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span></span>

<span data-ttu-id="be8ac-128">Wenn Sie Media Foundation Prozess intern verwenden, sind Objekte, die von Media Foundation Methoden und Funktionen zurückgegeben werden, direkte Zeiger auf das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="be8ac-128">If you are using Media Foundation in-process, objects returned from Media Foundation methods and functions are direct pointers to the object.</span></span> <span data-ttu-id="be8ac-129">Bei prozessübergreifenden Media Foundation handelt es sich bei diesen Objekten möglicherweise um MTA-Proxys, die bei Bedarf in einen STA-Thread gemarshallt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="be8ac-129">For cross-process Media Foundation, these objects may be MTA proxies, and should be marshaled into an STA thread if needed there.</span></span> <span data-ttu-id="be8ac-130">Ebenso sind Objekte, die innerhalb eines Rückrufs abgerufen werden – z. b. eine Topologie aus dem [mesessiontopologystatus](mesessiontopologystatus.md) -Ereignis – direkte Zeiger, wenn Media Foundation Prozess intern verwendet wird, aber MTA-Proxys sind, wenn Media Foundation Prozess übergreifend verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be8ac-130">Similarly, objects obtained inside a callback — for example, a topology from the [MESessionTopologyStatus](mesessiontopologystatus.md) event — are direct pointers when Media Foundation is used in-process, but are MTA proxies when Media Foundation is used cross-process.</span></span>

> [!Note]  
> <span data-ttu-id="be8ac-131">Das häufigste Szenario für die Verwendung von Media Foundation Prozess übergreifender Prozess ist der [geschützte Medien Pfad](protected-media-path.md) (PMP).</span><span class="sxs-lookup"><span data-stu-id="be8ac-131">The most common scenario for using Media Foundation cross-process is with the [Protected Media Path](protected-media-path.md) (PMP).</span></span> <span data-ttu-id="be8ac-132">Diese Hinweise gelten jedoch für jede Situation, in der Media Foundation APIs über RPC verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be8ac-132">However, these remarks apply to any situation when Media Foundation APIs are used through RPC.</span></span>

 

<span data-ttu-id="be8ac-133">Alle Implementierungen von [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) sollten MTA-kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="be8ac-133">All implementations of [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) should be MTA-compatible.</span></span> <span data-ttu-id="be8ac-134">Diese Objekte müssen überhaupt keine COM-Objekte sein.</span><span class="sxs-lookup"><span data-stu-id="be8ac-134">These objects do not need to be COM objects at all.</span></span> <span data-ttu-id="be8ac-135">Wenn dies der Fall ist, können Sie nicht im STA ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="be8ac-135">But if they are, they cannot run in the STA.</span></span> <span data-ttu-id="be8ac-136">Die [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) -Funktion wird für einen MTA-Arbeits Warteschlangen Thread aufgerufen, und das angegebene [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Objekt ist entweder ein direkter Objekt Zeiger oder ein MTA-Proxy.</span><span class="sxs-lookup"><span data-stu-id="be8ac-136">The [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) function will be invoked on an MTA workqueue thread, and the provided [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) object will be either a direct object pointer or an MTA proxy.</span></span>

## <a name="best-practices-for-media-foundation-components"></a><span data-ttu-id="be8ac-137">Bewährte Methoden für Media Foundation Komponenten</span><span class="sxs-lookup"><span data-stu-id="be8ac-137">Best Practices for Media Foundation Components</span></span>

<span data-ttu-id="be8ac-138">Es gibt zwei Kategorien von Media Foundation-Objekten, die sich mit com befassen müssen.</span><span class="sxs-lookup"><span data-stu-id="be8ac-138">There are two categories of Media Foundation objects that need to be concerned about COM.</span></span> <span data-ttu-id="be8ac-139">Einige Komponenten, z. b. Transformationen oder Byte Datenstrom Handler, sind vollständige COM-Objekte, die von der CLSID erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="be8ac-139">Some components, such as transforms or byte stream handlers, are full COM objects created by CLSID.</span></span> <span data-ttu-id="be8ac-140">Diese Objekte müssen den Regeln für com-Apartments für Prozess interne und prozessübergreifende Media Foundation entsprechen.</span><span class="sxs-lookup"><span data-stu-id="be8ac-140">These objects must follow the rules for COM apartments, for both in-process and cross-process Media Foundation.</span></span> <span data-ttu-id="be8ac-141">Andere Media Foundation Komponenten sind keine vollständigen com-Objekte, benötigen aber com-Proxys für die prozessübergreifende Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="be8ac-141">Other Media Foundation components are not full COM objects, but do need COM proxies for cross-process playback.</span></span> <span data-ttu-id="be8ac-142">Zu den Objekten in dieser Kategorie zählen Medienquellen und Aktivierungs Objekte.</span><span class="sxs-lookup"><span data-stu-id="be8ac-142">Objects in this category include media sources and activation object.</span></span> <span data-ttu-id="be8ac-143">Diese Objekte können Apartment Probleme ignorieren, wenn Sie nur für Prozess interne Media Foundation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be8ac-143">These objects can ignore apartment issues if they will be used only for in-process Media Foundation.</span></span>

<span data-ttu-id="be8ac-144">Obwohl es sich nicht bei allen Media Foundation Objekten um COM-Objekte handelt, werden alle Media Foundation Schnittstellen von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="be8ac-144">Although not all Media Foundation objects are COM objects, all Media Foundation interfaces derive from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="be8ac-145">Daher müssen alle Media Foundation Objekte **IUnknown** gemäß com-Spezifikationen implementieren, einschließlich der Regeln für die Verweis Zählung und [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="be8ac-145">Therefore, all Media Foundation objects must implement **IUnknown** according to COM specifications, including the rules for reference counting and [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="be8ac-146">Alle Verweis gezählten Objekte sollten außerdem sicherstellen, dass [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) das Entladen des Moduls nicht zulässt, während die Objekte weiterhin persistent gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="be8ac-146">All reference counted objects should also ensure that [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) will not allow the module to be unloaded while the objects still persist.</span></span>

<span data-ttu-id="be8ac-147">Media Foundation Komponenten können keine STA-Objekte sein.</span><span class="sxs-lookup"><span data-stu-id="be8ac-147">Media Foundation components cannot be STA objects.</span></span> <span data-ttu-id="be8ac-148">Viele Media Foundation Objekte müssen überhaupt keine COM-Objekte sein.</span><span class="sxs-lookup"><span data-stu-id="be8ac-148">Many Media Foundation objects do not need to be COM objects at all.</span></span> <span data-ttu-id="be8ac-149">Wenn dies der Fall ist, können Sie nicht im STA ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="be8ac-149">But if they are, they cannot run in the STA.</span></span> <span data-ttu-id="be8ac-150">Alle Media Foundation Komponenten müssen Thread sicher sein.</span><span class="sxs-lookup"><span data-stu-id="be8ac-150">All Media Foundation components must be thread-safe.</span></span> <span data-ttu-id="be8ac-151">Einige Media Foundation Objekte müssen auch frei Thread-oder Apartment neutral sein.</span><span class="sxs-lookup"><span data-stu-id="be8ac-151">Some Media Foundation objects must be free-threaded or apartment-neutral as well.</span></span> <span data-ttu-id="be8ac-152">In der folgenden Tabelle sind die Anforderungen für benutzerdefinierte Schnittstellen Implementierungen angegeben:</span><span class="sxs-lookup"><span data-stu-id="be8ac-152">The following table specifies the requirements for custom interface implementations:</span></span>



| <span data-ttu-id="be8ac-153">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="be8ac-153">Interface</span></span>                                                          | <span data-ttu-id="be8ac-154">Category</span><span class="sxs-lookup"><span data-stu-id="be8ac-154">Category</span></span>            | <span data-ttu-id="be8ac-155">Benötigtes Apartment</span><span class="sxs-lookup"><span data-stu-id="be8ac-155">Required apartment</span></span>       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [<span data-ttu-id="be8ac-156">**Imfaktivate**</span><span class="sxs-lookup"><span data-stu-id="be8ac-156">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | <span data-ttu-id="be8ac-157">Prozess übergreifender Proxy</span><span class="sxs-lookup"><span data-stu-id="be8ac-157">Cross-process proxy</span></span> | <span data-ttu-id="be8ac-158">Free-Thread oder neutral</span><span class="sxs-lookup"><span data-stu-id="be8ac-158">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="be8ac-159">**IMF bytestreamhandler**</span><span class="sxs-lookup"><span data-stu-id="be8ac-159">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | <span data-ttu-id="be8ac-160">COM-Objekt</span><span class="sxs-lookup"><span data-stu-id="be8ac-160">COM object</span></span>          | <span data-ttu-id="be8ac-161">MTA</span><span class="sxs-lookup"><span data-stu-id="be8ac-161">MTA</span></span>                      |
| [<span data-ttu-id="be8ac-162">**IMF contentprotection Manager**</span><span class="sxs-lookup"><span data-stu-id="be8ac-162">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | <span data-ttu-id="be8ac-163">Prozess übergreifender Proxy</span><span class="sxs-lookup"><span data-stu-id="be8ac-163">Cross-process proxy</span></span> | <span data-ttu-id="be8ac-164">Free-Thread oder neutral</span><span class="sxs-lookup"><span data-stu-id="be8ac-164">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="be8ac-165">**IMF-Manager**</span><span class="sxs-lookup"><span data-stu-id="be8ac-165">**IMFQualityManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | <span data-ttu-id="be8ac-166">COM-Objekt</span><span class="sxs-lookup"><span data-stu-id="be8ac-166">COM object</span></span>          | <span data-ttu-id="be8ac-167">Free-Thread oder neutral</span><span class="sxs-lookup"><span data-stu-id="be8ac-167">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="be8ac-168">**Imfmediasource**</span><span class="sxs-lookup"><span data-stu-id="be8ac-168">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | <span data-ttu-id="be8ac-169">Prozess übergreifender Proxy</span><span class="sxs-lookup"><span data-stu-id="be8ac-169">Cross-process proxy</span></span> | <span data-ttu-id="be8ac-170">Free-Thread oder neutral</span><span class="sxs-lookup"><span data-stu-id="be8ac-170">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="be8ac-171">**IMF Schema Handler**</span><span class="sxs-lookup"><span data-stu-id="be8ac-171">**IMFSchemeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | <span data-ttu-id="be8ac-172">COM-Objekt</span><span class="sxs-lookup"><span data-stu-id="be8ac-172">COM object</span></span>          | <span data-ttu-id="be8ac-173">MTA</span><span class="sxs-lookup"><span data-stu-id="be8ac-173">MTA</span></span>                      |
| [<span data-ttu-id="be8ac-174">**Imftopoloader**</span><span class="sxs-lookup"><span data-stu-id="be8ac-174">**IMFTopoLoader**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | <span data-ttu-id="be8ac-175">COM-Objekt</span><span class="sxs-lookup"><span data-stu-id="be8ac-175">COM object</span></span>          | <span data-ttu-id="be8ac-176">Free-Thread oder neutral</span><span class="sxs-lookup"><span data-stu-id="be8ac-176">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="be8ac-177">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="be8ac-177">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | <span data-ttu-id="be8ac-178">COM-Objekt</span><span class="sxs-lookup"><span data-stu-id="be8ac-178">COM object</span></span>          | <span data-ttu-id="be8ac-179">MTA</span><span class="sxs-lookup"><span data-stu-id="be8ac-179">MTA</span></span>                      |



 

<span data-ttu-id="be8ac-180">Abhängig von der Implementierung sind möglicherweise weitere Anforderungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="be8ac-180">There may be additional requirements depending upon the implementation.</span></span> <span data-ttu-id="be8ac-181">Wenn eine Medien Senke z. b. eine andere Schnittstelle implementiert, die der Anwendung das Ausführen direkter Funktionsaufrufe an die Senke ermöglicht, muss die Senke frei Thread oder neutral sein, damit direkte prozessübergreifende Aufrufe möglich sind.</span><span class="sxs-lookup"><span data-stu-id="be8ac-181">For example, if a media sink implements another interface that enables the application to make direct function calls to the sink, the sink would need to be free-threaded or neutral, so that it could handle direct cross-process calls.</span></span> <span data-ttu-id="be8ac-182">Jedes Objekt ist möglicherweise frei Thread; in dieser Tabelle sind die Mindestanforderungen angegeben.</span><span class="sxs-lookup"><span data-stu-id="be8ac-182">Any object may be free-threaded; this table specifies the minimum requirements.</span></span>

<span data-ttu-id="be8ac-183">Die empfohlene Vorgehensweise zum Implementieren von frei Thread-oder neutralen Objekten besteht darin, den frei Hand Thread-Mars Haller zu aggregierten.</span><span class="sxs-lookup"><span data-stu-id="be8ac-183">The recommended way to implement free-threaded or neutral objects is by aggregating the free-threaded marshaler.</span></span> <span data-ttu-id="be8ac-184">Weitere Informationen finden Sie in der MSDN-Dokumentation zu [**cokreatefreethreadedmarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler).</span><span class="sxs-lookup"><span data-stu-id="be8ac-184">For more details, see the MSDN documentation on [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler).</span></span> <span data-ttu-id="be8ac-185">In Übereinstimmung mit der Anforderung, STA-Objekte oder-Proxys nicht an Media Foundation-APIs zu übergeben, müssen sich frei Thread Objekte keine Gedanken über das Marshalling von STA-Eingabe Zeigern in frei Thread Komponenten machen.</span><span class="sxs-lookup"><span data-stu-id="be8ac-185">In accordance with the requirement not to pass STA objects or proxies to Media Foundation APIs, free-threaded objects do not need to worry about marshaling STA input pointers in free-threaded components.</span></span>

<span data-ttu-id="be8ac-186">Komponenten, die die Arbeits Warteschlange für lange funktionsfähig verwenden (**mfasync- \_ Rückruf \_ Warteschlange \_ Long- \_ Funktion**), müssen mehr Sorgfalt walten lassen</span><span class="sxs-lookup"><span data-stu-id="be8ac-186">Components that use the long-function work queue (**MFASYNC\_CALLBACK\_QUEUE\_LONG\_FUNCTION**) must exercise more care.</span></span> <span data-ttu-id="be8ac-187">Threads in der Arbeits Warteschlange Long Function erstellen einen eigenen Sta.</span><span class="sxs-lookup"><span data-stu-id="be8ac-187">Threads in the long function workqueue create their own STA.</span></span> <span data-ttu-id="be8ac-188">Komponenten, die die Long-Funktions Arbeits Warteschlange für Rückrufe verwenden, sollten das Erstellen von COM-Objekten in diesen Threads vermeiden und bei Bedarf darauf achten, Proxys auf dem STA zu Mars Hallen.</span><span class="sxs-lookup"><span data-stu-id="be8ac-188">Components that use the long function workqueue for callbacks should avoid creating COM objects on these threads, and need to be careful to marshal proxies to the STA as necessary.</span></span>

## <a name="summary"></a><span data-ttu-id="be8ac-189">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="be8ac-189">Summary</span></span>

<span data-ttu-id="be8ac-190">Anwendungen haben einen einfacheren Zeit, wenn Sie mit Media Foundation über einen MTA-Thread interagieren, aber es ist möglich, Media Foundation von einem STA-Thread zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="be8ac-190">Applications will have an easier time if they interact with Media Foundation from an MTA thread, but it is possible with some care to use Media Foundation from an STA thread.</span></span> <span data-ttu-id="be8ac-191">Media Foundation verarbeitet STA-Komponenten nicht, und Anwendungen sollten darauf achten, STA-Objekte nicht an Media Foundation-APIs zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="be8ac-191">Media Foundation does not handle STA components, and applications should be careful not to pass STA objects to Media Foundation APIs.</span></span> <span data-ttu-id="be8ac-192">Einige Objekte haben zusätzliche Anforderungen, insbesondere Objekte, die in einer prozessübergreifenden Situation ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="be8ac-192">Some objects have additional requirements, especially objects that run in a cross-process situation.</span></span> <span data-ttu-id="be8ac-193">Die folgenden Richtlinien helfen dabei, com-Fehler, Deadlocks und unerwartete Verzögerungen bei der Medienverarbeitung zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="be8ac-193">Following these guidelines will help avoid COM errors, deadlocks, and unexpected delays in media processing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be8ac-194">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be8ac-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be8ac-195">Media Foundation Plattform-APIs</span><span class="sxs-lookup"><span data-stu-id="be8ac-195">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> <dt>

[<span data-ttu-id="be8ac-196">Media Foundation-Architektur</span><span class="sxs-lookup"><span data-stu-id="be8ac-196">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 
