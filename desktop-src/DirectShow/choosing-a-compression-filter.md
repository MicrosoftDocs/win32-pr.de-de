---
description: Auswählen eines Komprimierungs Filters
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Auswählen eines Komprimierungs Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64ebebf41c35ed6aed9ab47d853c03ba720a31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125510"
---
# <a name="choosing-a-compression-filter"></a><span data-ttu-id="f27d0-103">Auswählen eines Komprimierungs Filters</span><span class="sxs-lookup"><span data-stu-id="f27d0-103">Choosing a Compression Filter</span></span>

<span data-ttu-id="f27d0-104">Verschiedene Arten von Softwarekomponenten können Video-oder Audiokomprimierung durchführen, z. b.:</span><span class="sxs-lookup"><span data-stu-id="f27d0-104">Several types of software components can perform video or audio compression, such as:</span></span>

-   <span data-ttu-id="f27d0-105">Native DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="f27d0-105">Native DirectShow filters</span></span>
-   <span data-ttu-id="f27d0-106">Codecs für Video Komprimierungs-Manager (VCM)</span><span class="sxs-lookup"><span data-stu-id="f27d0-106">Video Compression Manager (VCM) codecs</span></span>
-   <span data-ttu-id="f27d0-107">Codecs für den Audiokomprimierungs-Manager (ACM)</span><span class="sxs-lookup"><span data-stu-id="f27d0-107">Audio Compression Manager (ACM) codecs</span></span>
-   <span data-ttu-id="f27d0-108">DirectX Media Objects (DMOs)</span><span class="sxs-lookup"><span data-stu-id="f27d0-108">DirectX Media Objects (DMOs)</span></span>

<span data-ttu-id="f27d0-109">In DirectShow werden VCM-Codecs durch den [AVI-Kompressor-Filter](avi-compressor-filter.md)umschlossen, und ACM-Codecs werden durch den [ACM-Wrapper Filter](acm-wrapper-filter.md)umschlossen.</span><span class="sxs-lookup"><span data-stu-id="f27d0-109">In DirectShow, VCM codecs are wrapped by the [AVI Compressor Filter](avi-compressor-filter.md), and ACM codecs are wrapped by the [ACM Wrapper Filter](acm-wrapper-filter.md).</span></span> <span data-ttu-id="f27d0-110">DMOS werden durch den [DMO-Wrapper Filter](dmo-wrapper-filter.md)umschlossen.</span><span class="sxs-lookup"><span data-stu-id="f27d0-110">DMOs are wrapped by the [DMO Wrapper Filter](dmo-wrapper-filter.md).</span></span> <span data-ttu-id="f27d0-111">Der Enumerator für Systemgeräte bietet eine konsistente Möglichkeit zum Auflisten und Erstellen eines dieser kompressortypen, ohne sich Gedanken über das zugrunde liegende Modell machen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="f27d0-111">The system device enumerator provides a consistent way to enumerate and create any of these compressor types, without worrying about the underlying model.</span></span>

<span data-ttu-id="f27d0-112">Ausführliche Informationen zum Enumerator für Systemgeräte finden [Sie unter Verwenden des Systemgeräte Enumerators](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="f27d0-112">For details about the system device enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span> <span data-ttu-id="f27d0-113">Kurz gesagt, alle DirectShow-Filter werden nach Kategorie klassifiziert, und jede Kategorie wird durch eine GUID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f27d0-113">Briefly, all DirectShow filters are classified by category, and each category is identified by a GUID.</span></span> <span data-ttu-id="f27d0-114">Bei Video-Kompressoren lautet die Kategorie GUID CLSID \_ videocompressorcategory.</span><span class="sxs-lookup"><span data-stu-id="f27d0-114">For video compressors, the category GUID is CLSID\_VideoCompressorCategory.</span></span> <span data-ttu-id="f27d0-115">Für audiokompressoren ist es CLSID \_ audiocompressorcategory.</span><span class="sxs-lookup"><span data-stu-id="f27d0-115">For audio compressors, it is CLSID\_AudioCompressorCategory.</span></span> <span data-ttu-id="f27d0-116">Zum Auflisten einer bestimmten Kategorie erstellt der Systemgeräte Enumerator ein *Enumeratorobjekt* , das die [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f27d0-116">To enumerate a particular category, the system device enumerator creates an *enumerator* object that supports the [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) interface.</span></span> <span data-ttu-id="f27d0-117">Diese Schnittstelle wird von der Anwendung zum Abrufen von gerätermonikern verwendet, wobei jeder gerätermoniker eine Instanz eines DirectShow-Filters darstellt.</span><span class="sxs-lookup"><span data-stu-id="f27d0-117">The application uses this interface to retrieve device monikers, where each device moniker represents an instance of a DirectShow filter.</span></span> <span data-ttu-id="f27d0-118">Sie können den Moniker verwenden, um den Filter zu erstellen, oder um den anzeigen amen des Geräts zu erhalten, ohne den Filter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f27d0-118">You can use the moniker to create the filter, or to get the device's friendly name without creating the filter.</span></span>

<span data-ttu-id="f27d0-119">Gehen Sie folgendermaßen vor, um die auf dem System des Benutzers verfügbaren Video-oder audiokompressoren aufzulisten:</span><span class="sxs-lookup"><span data-stu-id="f27d0-119">To enumerate the video or audio compressors available on the user's system, do the following:</span></span>

1.  <span data-ttu-id="f27d0-120">Rufen Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um den Enumerator für Systemgeräte zu erstellen, der über die Klassen-ID CLSID \_ systemdeviceenumeration verfügt.</span><span class="sxs-lookup"><span data-stu-id="f27d0-120">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the system device enumerator, which has a class ID of CLSID\_SystemDeviceEnum.</span></span>
2.  <span data-ttu-id="f27d0-121">Aufrufen von [**ikreatedevenum:: kreateclassenumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) mit der Filterkategorie GUID.</span><span class="sxs-lookup"><span data-stu-id="f27d0-121">Call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the filter category GUID.</span></span> <span data-ttu-id="f27d0-122">Die-Methode gibt einen **IEnumMoniker** -Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="f27d0-122">The method returns an **IEnumMoniker** interface pointer.</span></span>
3.  <span data-ttu-id="f27d0-123">Verwenden Sie die IEnumMoniker:: Next-Methode, um die gerätermoniker aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="f27d0-123">Use the IEnumMoniker::Next method to enumerate the device monikers.</span></span> <span data-ttu-id="f27d0-124">Diese Methode gibt eine [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) -Schnittstelle zurück, die den Moniker darstellt.</span><span class="sxs-lookup"><span data-stu-id="f27d0-124">This method returns an [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) interface, which represents the moniker.</span></span>

<span data-ttu-id="f27d0-125">Gehen Sie folgendermaßen vor, um den anzeigen Amen von einem Moniker zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="f27d0-125">To get the friendly name from a moniker, do the following:</span></span>

1.  <span data-ttu-id="f27d0-126">Aufrufen der **IMoniker:: bindesstorage** -Methode.</span><span class="sxs-lookup"><span data-stu-id="f27d0-126">Call the **IMoniker::BindToStorage** method.</span></span> <span data-ttu-id="f27d0-127">Diese Methode gibt einen **IPropertyBag** -Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="f27d0-127">This method returns an **IPropertyBag** interface pointer.</span></span>
2.  <span data-ttu-id="f27d0-128">Verwenden Sie die **IPropertyBag:: Read** -Methode, um die **FriendlyName** -Eigenschaft zu lesen.</span><span class="sxs-lookup"><span data-stu-id="f27d0-128">Use the **IPropertyBag::Read** method to read the **FriendlyName** property.</span></span>

<span data-ttu-id="f27d0-129">In der Regel würde eine Anwendung eine Liste von Kompressoren anzeigen, sodass der Benutzer eine Liste auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="f27d0-129">Typically, an application would display a list of compressors, so that the user could choose one.</span></span> <span data-ttu-id="f27d0-130">Der folgende Code füllt z. b. ein Listenfeld mit den Namen der verfügbaren Video-Kompressoren auf.</span><span class="sxs-lookup"><span data-stu-id="f27d0-130">For example, the following code populates a list box with the names of the available video compressors.</span></span>


```C++
void OnInitDialog(HWND hDlg)
{
    HRESULT hr;
    ICreateDevEnum *pSysDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    IMoniker *pMoniker = NULL;

    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, 
        (void**)&pSysDevEnum);
    if (FAILED(hr))
    {
        // Handle the error.
    }    

    hr = pSysDevEnum->CreateClassEnumerator(
             CLSID_VideoCompressorCategory, &pEnum, 0);
    if (hr == S_OK)  // S_FALSE means nothing in this category.
    {
        while (S_OK == pEnum->Next(1, &pMoniker, NULL))
        {
            IPropertyBag *pPropBag = NULL;
            pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
                (void **)&pPropBag);
            VARIANT var;
            VariantInit(&var);
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
            if (SUCCEEDED(hr))
            {
                LRESULT iSel = AddString(GetDlgItem(hDlg, 
                    IDC_CODEC_LIST), var.bstrVal);
            }   
            VariantClear(&var); 
            pPropBag->Release();
            pMoniker->Release();
        }
    }

    SendDlgItemMessage(hDlg, IDC_CODEC_LIST, 
                       LB_SETCURSEL, 0, 0);
    pSysDevEnum->Release();
    pEnum->Release();
}
```



<span data-ttu-id="f27d0-131">Um eine Filter Instanz aus dem Moniker zu erstellen, rufen Sie die **IMoniker:: BindTo Object** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="f27d0-131">To create a filter instance from the moniker, call the **IMoniker::BindToObject** method.</span></span> <span data-ttu-id="f27d0-132">Die-Methode gibt einen [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="f27d0-132">The method returns an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span>


```C++
IBaseFilter *pFilter = NULL;
hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, 
                                       (void**)&pFilter);
if (SUCCEEDED(hr))
{
    // Use the filter. 
    // Remember to release the IBaseFilter interface.
}
```



<span data-ttu-id="f27d0-133">Bei VCM-Codecs stellt jeder Moniker einen bestimmten Codec dar, auch wenn alle Codecs durch denselben AVI-Komprimierungs Filter umschließt werden.</span><span class="sxs-lookup"><span data-stu-id="f27d0-133">For VCM codecs, each moniker represents one particular codec, even though all of the codecs are wrapped by the same AVI Compression filter.</span></span> <span data-ttu-id="f27d0-134">Der Aufruf von " **BindToObject** " erstellt eine Instanz dieses Filters, die für diesen Codec initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f27d0-134">Calling **BindToObject** creates an instance of this filter, initialized for that codec.</span></span> <span data-ttu-id="f27d0-135">Aus diesem Grund können Sie **cokreateinstance** nicht direkt für den AVI-Komprimierungs Filter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f27d0-135">For this reason, you cannot call **CoCreateInstance** directly on the AVI Compression filter.</span></span> <span data-ttu-id="f27d0-136">Sie müssen den Enumerator "Systemgeräte" durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="f27d0-136">You must go through the system device enumerator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f27d0-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f27d0-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f27d0-138">Neukomprimieren einer AVI-Datei</span><span class="sxs-lookup"><span data-stu-id="f27d0-138">Recompressing an AVI File</span></span>](recompressing-an-avi-file.md)
</dt> </dl>

 

 
