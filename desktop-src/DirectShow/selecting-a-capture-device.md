---
description: Auswählen eines Erfassungs Geräts
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: Auswählen eines Erfassungs Geräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b599728c6bd2d98b89285b6008923aa4fb2a3aef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342725"
---
# <a name="selecting-a-capture-device"></a><span data-ttu-id="f187a-103">Auswählen eines Erfassungs Geräts</span><span class="sxs-lookup"><span data-stu-id="f187a-103">Selecting a Capture Device</span></span>

<span data-ttu-id="f187a-104">Verwenden Sie zum Auswählen eines Audiogeräts oder Video Erfassungs Geräts den [Enumerator "Systemgeräte](system-device-enumerator.md)", der im Thema [Verwenden des Enumerators "Systemgeräte](using-the-system-device-enumerator.md)" beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f187a-104">To select an audio or video capture device, use the [System Device Enumerator](system-device-enumerator.md), described in the topic [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span> <span data-ttu-id="f187a-105">Der Enumerator für System Geräte gibt eine Sammlung von gerätermonikern zurück, die nach Gerätekategorie ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="f187a-105">The System Device Enumerator returns a collection of device monikers, selected by device category.</span></span> <span data-ttu-id="f187a-106">Ein *Moniker* ist ein COM-Objekt, das Informationen über ein anderes Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="f187a-106">A *moniker* is a COM object that contains information about another object.</span></span> <span data-ttu-id="f187a-107">Moniker ermöglichen es der Anwendung, Informationen zu einem Objekt zu erhalten, ohne das Objekt tatsächlich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f187a-107">Monikers enable the application to get information about an object without actually creating the object.</span></span> <span data-ttu-id="f187a-108">Später kann die Anwendung den Moniker zum Erstellen des Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="f187a-108">Later, the application can use the moniker to create the object.</span></span> <span data-ttu-id="f187a-109">Weitere Informationen zu Monikern finden Sie in der Dokumentation für [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).</span><span class="sxs-lookup"><span data-stu-id="f187a-109">For more information about monikers, see the documentation for [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).</span></span>

<span data-ttu-id="f187a-110">Führen Sie die folgenden Schritte aus, um den Enumerator für System Geräte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f187a-110">To use the System Device Enumerator, perform the following steps.</span></span>

1.  <span data-ttu-id="f187a-111">Rufen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um eine Instanz des Enumerators für System Geräte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f187a-111">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create an instance of the System Device Enumerator.</span></span>
2.  <span data-ttu-id="f187a-112">Nennen Sie [**ikreatedevenum:: feateclassenumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) , und geben Sie die Gerätekategorie als GUID an.</span><span class="sxs-lookup"><span data-stu-id="f187a-112">Call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) and specify the device category as a GUID.</span></span> <span data-ttu-id="f187a-113">Für Erfassungsgeräte sind die folgenden Kategorien relevant.</span><span class="sxs-lookup"><span data-stu-id="f187a-113">For capture devices, the following categories are relevant.</span></span> 

    | <span data-ttu-id="f187a-114">Kategorie-GUID</span><span class="sxs-lookup"><span data-stu-id="f187a-114">Category GUID</span></span>                       | <span data-ttu-id="f187a-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f187a-115">Description</span></span>           |
    |-------------------------------------|-----------------------|
    | <span data-ttu-id="f187a-116">**CLSID \_ audioinputentvicecategory**</span><span class="sxs-lookup"><span data-stu-id="f187a-116">**CLSID\_AudioInputDeviceCategory**</span></span> | <span data-ttu-id="f187a-117">Audioerfassungs Geräte</span><span class="sxs-lookup"><span data-stu-id="f187a-117">Audio capture devices</span></span> |
    | <span data-ttu-id="f187a-118">**CLSID \_ videoinputentvicecategory**</span><span class="sxs-lookup"><span data-stu-id="f187a-118">**CLSID\_VideoInputDeviceCategory**</span></span> | <span data-ttu-id="f187a-119">Video Erfassungsgeräte</span><span class="sxs-lookup"><span data-stu-id="f187a-119">Video capture devices</span></span> |

    

     

    <span data-ttu-id="f187a-120">Wenn eine Videokamera über ein integriertes Mikrofon verfügt, wird Sie in beiden Kategorien angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f187a-120">If a video camera has an integrated microphone, it appears in both categories.</span></span> <span data-ttu-id="f187a-121">Die Kamera und das Mikrofon werden jedoch vom System als separate Geräte behandelt, um Aufzählungs-, Geräte-und datenstreamingvorgänge durchlaufen zu können.</span><span class="sxs-lookup"><span data-stu-id="f187a-121">However, the camera and microphone are treated as separate devices by the system, for purposes of enumeration, device creation, and data streaming.</span></span>

3.  <span data-ttu-id="f187a-122">Die Methode " [**kreateclassenumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) " gibt einen Zeiger auf die [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="f187a-122">The [**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method returns a pointer to the [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface.</span></span> <span data-ttu-id="f187a-123">Um die Moniker aufzuzählen, nennen Sie [**IEnumMoniker:: Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).</span><span class="sxs-lookup"><span data-stu-id="f187a-123">To enumerate the monikers, call [**IEnumMoniker::Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).</span></span>

<span data-ttu-id="f187a-124">Mit dem folgenden Code wird ein Enumerator für eine angegebene Gerätekategorie erstellt.</span><span class="sxs-lookup"><span data-stu-id="f187a-124">The following code creates an enumerator for a specified device category.</span></span>


```C++
#include <windows.h>
#include <dshow.h>

#pragma comment(lib, "strmiids")

HRESULT EnumerateDevices(REFGUID category, IEnumMoniker **ppEnum)
{
    // Create the System Device Enumerator.
    ICreateDevEnum *pDevEnum;
    HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL,  
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDevEnum));

    if (SUCCEEDED(hr))
    {
        // Create an enumerator for the category.
        hr = pDevEnum->CreateClassEnumerator(category, ppEnum, 0);
        if (hr == S_FALSE)
        {
            hr = VFW_E_NOT_FOUND;  // The category is empty. Treat as an error.
        }
        pDevEnum->Release();
    }
    return hr;
}
```



<span data-ttu-id="f187a-125">Mit der [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) -Schnittstelle wird eine Liste der [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) -Schnittstellen aufgelistet, von denen jede einen gerätermoniker darstellt.</span><span class="sxs-lookup"><span data-stu-id="f187a-125">The [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface enumerates a list of [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interfaces, each of which represents a device moniker.</span></span> <span data-ttu-id="f187a-126">Die Anwendung kann Eigenschaften aus dem Moniker lesen oder den Moniker zum Erstellen eines DirectShow-Erfassungs Filters für das Gerät verwenden.</span><span class="sxs-lookup"><span data-stu-id="f187a-126">The application can read properties from the moniker, or use the moniker to create a DirectShow capture filter for the device.</span></span> <span data-ttu-id="f187a-127">Monikereigenschaften werden als **Variant** -Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f187a-127">Moniker properties are returned as **VARIANT** values.</span></span> <span data-ttu-id="f187a-128">Die folgenden Eigenschaften werden von gerätermonikern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f187a-128">The following properties are supported by device monikers.</span></span>



| <span data-ttu-id="f187a-129">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f187a-129">Property</span></span>       | <span data-ttu-id="f187a-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f187a-130">Description</span></span>                                                               | <span data-ttu-id="f187a-131">VARIANT-Typ</span><span class="sxs-lookup"><span data-stu-id="f187a-131">VARIANT Type</span></span> |
|----------------|---------------------------------------------------------------------------|--------------|
| <span data-ttu-id="f187a-132">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f187a-132">"FriendlyName"</span></span> | <span data-ttu-id="f187a-133">Der Name des Geräts.</span><span class="sxs-lookup"><span data-stu-id="f187a-133">The name of the device.</span></span>                                                   | <span data-ttu-id="f187a-134">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="f187a-134">**VT\_BSTR**</span></span> |
| <span data-ttu-id="f187a-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f187a-135">"Description"</span></span>  | <span data-ttu-id="f187a-136">Eine Beschreibung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="f187a-136">A description of the device.</span></span>                                              | <span data-ttu-id="f187a-137">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="f187a-137">**VT\_BSTR**</span></span> |
| <span data-ttu-id="f187a-138">DevicePath</span><span class="sxs-lookup"><span data-stu-id="f187a-138">"DevicePath"</span></span>   | <span data-ttu-id="f187a-139">Eine eindeutige Zeichenfolge, die das Gerät identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f187a-139">A unique string that identifies the device.</span></span> <span data-ttu-id="f187a-140">(Nur Video Erfassungsgeräte.)</span><span class="sxs-lookup"><span data-stu-id="f187a-140">(Video capture devices only.)</span></span> | <span data-ttu-id="f187a-141">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="f187a-141">**VT\_BSTR**</span></span> |
| <span data-ttu-id="f187a-142">"Waveingeid"</span><span class="sxs-lookup"><span data-stu-id="f187a-142">"WaveInID"</span></span>     | <span data-ttu-id="f187a-143">Der Bezeichner für ein audioerfassungs Gerät.</span><span class="sxs-lookup"><span data-stu-id="f187a-143">The identifier for an audio capture device.</span></span> <span data-ttu-id="f187a-144">(Nur audioerfassungs Geräte.)</span><span class="sxs-lookup"><span data-stu-id="f187a-144">(Audio capture devices only.)</span></span> | <span data-ttu-id="f187a-145">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="f187a-145">**VT\_I4**</span></span>   |



 

<span data-ttu-id="f187a-146">Die Eigenschaften "FriendlyName" und "Description" sind für die Anzeige in einer Benutzeroberfläche geeignet.</span><span class="sxs-lookup"><span data-stu-id="f187a-146">The "FriendlyName" and "Description" properties are suitable for displaying in a UI.</span></span>

-   <span data-ttu-id="f187a-147">Die Eigenschaft "FriendlyName" ist für jedes Gerät verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f187a-147">The "FriendlyName" property is available for every device.</span></span> <span data-ttu-id="f187a-148">Sie enthält einen lesbaren Namen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="f187a-148">It contains a human-readable name for the device.</span></span>
-   <span data-ttu-id="f187a-149">Die "Description"-Eigenschaft ist nur für DV-und D-VHS/MPEG-Camcorder-Geräte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f187a-149">The "Description" property is available only for DV and D-VHS/MPEG camcorder devices.</span></span> <span data-ttu-id="f187a-150">Weitere Informationen finden Sie unter [msdv Driver](msdv-driver.md) und [mstape Driver](mstape-driver.md).</span><span class="sxs-lookup"><span data-stu-id="f187a-150">For more information, see [MSDV Driver](msdv-driver.md) and [MSTape Driver](mstape-driver.md).</span></span> <span data-ttu-id="f187a-151">Wenn Sie verfügbar ist, enthält Sie eine Beschreibung des Geräts, das spezifischer ist als die Eigenschaft "FriendlyName".</span><span class="sxs-lookup"><span data-stu-id="f187a-151">If available, it contains a description of the device which is more specific than the "FriendlyName" property.</span></span> <span data-ttu-id="f187a-152">In der Regel enthält Sie den Herstellernamen.</span><span class="sxs-lookup"><span data-stu-id="f187a-152">Typically it includes the vendor name.</span></span>
-   <span data-ttu-id="f187a-153">Die Eigenschaft "DevicePath" ist keine für menschenlesbare Zeichenfolge, Sie ist jedoch für jedes Video Erfassungsgerät im System eindeutig.</span><span class="sxs-lookup"><span data-stu-id="f187a-153">The "DevicePath" property is not a human-readable string, but is guaranteed to be unique for each video capture device on the system.</span></span> <span data-ttu-id="f187a-154">Mit dieser Eigenschaft können Sie zwischen zwei oder mehr Instanzen desselben Geräte Modells unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="f187a-154">You can use this property to distinguish between two or more instances of the same model of device.</span></span>
-   <span data-ttu-id="f187a-155">Wenn die Eigenschaft "waveinid" vorhanden ist, bedeutet dies, dass der DirectShow-Erfassungs Filter die [Waveform-audioapis](../multimedia/waveform-audio.md) intern verwendet, um mit dem Gerät zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="f187a-155">If the "WaveInID" property is present, it means the DirectShow capture filter uses the [Waveform Audio](../multimedia/waveform-audio.md) APIs internally to communicate with the device.</span></span> <span data-ttu-id="f187a-156">Der Wert der waveiniid-Eigenschaft entspricht dem Bezeichner, der von den \**\* WaveIn* _-Funktionen verwendet wird, z. b. [_ *waveiniopen* \*](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).</span><span class="sxs-lookup"><span data-stu-id="f187a-156">The value of the "WaveInID" property corresponds to the identifier used by the \**waveIn\** _ functions, such as [_ *waveInOpen*\*](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).</span></span>

<span data-ttu-id="f187a-157">Führen Sie die folgenden Schritte aus, um Eigenschaften aus dem Moniker zu lesen.</span><span class="sxs-lookup"><span data-stu-id="f187a-157">To read properties from the moniker, perform the following steps.</span></span>

1.  <span data-ttu-id="f187a-158">Aufrufen von [**IMoniker:: bindesstorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) zum Abrufen eines Zeigers auf die [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f187a-158">Call [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) to get a pointer to the [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) interface.</span></span>
2.  <span data-ttu-id="f187a-159">Aufrufen von **IPropertyBag:: Read** , um die Eigenschaft zu lesen.</span><span class="sxs-lookup"><span data-stu-id="f187a-159">Call **IPropertyBag::Read** to read the property.</span></span>

<span data-ttu-id="f187a-160">Im folgenden Codebeispiel wird gezeigt, wie Sie eine Liste von gerätermonikern auflisten und die Eigenschaften erhalten.</span><span class="sxs-lookup"><span data-stu-id="f187a-160">The following code example shows how to enumerate a list of device monikers and get the properties.</span></span>


```C++
void DisplayDeviceInformation(IEnumMoniker *pEnum)
{
    IMoniker *pMoniker = NULL;

    while (pEnum->Next(1, &pMoniker, NULL) == S_OK)
    {
        IPropertyBag *pPropBag;
        HRESULT hr = pMoniker->BindToStorage(0, 0, IID_PPV_ARGS(&pPropBag));
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue;  
        } 

        VARIANT var;
        VariantInit(&var);

        // Get description or friendly name.
        hr = pPropBag->Read(L"Description", &var, 0);
        if (FAILED(hr))
        {
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
        }
        if (SUCCEEDED(hr))
        {
            printf("%S\n", var.bstrVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Write(L"FriendlyName", &var);

        // WaveInID applies only to audio capture devices.
        hr = pPropBag->Read(L"WaveInID", &var, 0);
        if (SUCCEEDED(hr))
        {
            printf("WaveIn ID: %d\n", var.lVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Read(L"DevicePath", &var, 0);
        if (SUCCEEDED(hr))
        {
            // The device path is not intended for display.
            printf("Device path: %S\n", var.bstrVal);
            VariantClear(&var); 
        }

        pPropBag->Release();
        pMoniker->Release();
    }
}

void main()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        IEnumMoniker *pEnum;

        hr = EnumerateDevices(CLSID_VideoInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        hr = EnumerateDevices(CLSID_AudioInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        CoUninitialize();
    }
}
```



<span data-ttu-id="f187a-161">Um einen DirectShow-Erfassungs Filter für das Gerät zu erstellen, rufen Sie die [**IMoniker:: BindTo Object**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) -Methode auf, um einen [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Zeiger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f187a-161">To create a DirectShow capture filter for the device, call the [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) method to get an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span> <span data-ttu-id="f187a-162">Klicken Sie dann auf [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , um dem Filter Diagramm den Filter hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="f187a-162">Then call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the filter graph:</span></span>


```C++
IBaseFilter *pCap = NULL;
hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter, (void**)&pCap);
if (SUCCEEDED(hr))
{
    hr = m_pGraph->AddFilter(pCap, L"Capture Filter");
}
```



## <a name="related-topics"></a><span data-ttu-id="f187a-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f187a-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f187a-164">Audioerfassung</span><span class="sxs-lookup"><span data-stu-id="f187a-164">Audio Capture</span></span>](audio-capture.md)
</dt> <dt>

[<span data-ttu-id="f187a-165">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="f187a-165">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
