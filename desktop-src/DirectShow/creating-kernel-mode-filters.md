---
description: Erstellen von Kernel-Mode filtern
ms.assetid: cbc86a5d-c53a-44a0-aa81-5c41527a8f67
title: Erstellen von Kernel-Mode filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c915a08312e33f0e35245325fd8bce7e55e486c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125414"
---
# <a name="creating-kernel-mode-filters"></a><span data-ttu-id="5bc3a-103">Erstellen von Kernel-Mode filtern</span><span class="sxs-lookup"><span data-stu-id="5bc3a-103">Creating Kernel-Mode Filters</span></span>

<span data-ttu-id="5bc3a-104">Bestimmte kernelmodusfilter können nicht mithilfe von **cokreateinstance** erstellt werden und verfügen daher nicht über CLSIDs.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-104">Certain kernel-mode filters cannot be created through **CoCreateInstance**, and thus do not have CLSIDs.</span></span> <span data-ttu-id="5bc3a-105">Zu diesen Filtern gehören der " [Tee/Sink-to-Sink"-Konverter](tee-sink-to-sink-converter.md), der [CC-Decoderfilter](cc-decoder-filter.md) und der [WST-Codec](wst-codec-filter.md) -Filter.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-105">These filters include the [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md), the [CC Decoder](cc-decoder-filter.md) filter, and the [WST Codec](wst-codec-filter.md) filter.</span></span> <span data-ttu-id="5bc3a-106">Verwenden Sie zum Erstellen eines dieser Filter das [System Geräte-Enumeratorobjekt](system-device-enumerator.md) , und suchen Sie nach dem Namen des Filters.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-106">To create one of these filters, use the [System Device Enumerator](system-device-enumerator.md) object and search by the filter's name.</span></span>

1.  <span data-ttu-id="5bc3a-107">Erstellen Sie den Enumerator für System Geräte.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-107">Create the System Device Enumerator.</span></span>
2.  <span data-ttu-id="5bc3a-108">Aufrufen der [**ikreatedevenum:: feateclassenumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) -Methode mit der CLSID der Filterkategorie für diesen Filter.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-108">Call the [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method with the CLSID of the filter category for that filter.</span></span> <span data-ttu-id="5bc3a-109">Diese Methode erstellt einen Enumerator für die Filterkategorie.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-109">This method creates an enumerator for the filter category.</span></span> <span data-ttu-id="5bc3a-110">(Ein *Enumerator* ist einfach ein Objekt, das mithilfe einer definierten COM-Schnittstelle eine Liste anderer Objekte zurückgibt.) Der Enumerator gibt **IMoniker** -Zeiger zurück, die die Filter in dieser Kategorie darstellen.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-110">(An *enumerator* is simply an object that returns a list of other objects, using a defined COM interface.) The enumerator returns **IMoniker** pointers, which represent the filters in that category.</span></span>
3.  <span data-ttu-id="5bc3a-111">Zum Abrufen einer **IPropertyBag** -Schnittstelle für jeden Moniker muss **IMoniker:: bindesstorage** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-111">For each moniker, call **IMoniker::BindToStorage** to get an **IPropertyBag** interface.</span></span>
4.  <span data-ttu-id="5bc3a-112">Aufrufen von **IPropertyBag:: Read** zum Abrufen des Namens des Filters.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-112">Call **IPropertyBag::Read** to get the name of the filter.</span></span>
5.  <span data-ttu-id="5bc3a-113">Wenn der Name übereinstimmt, rufen Sie **IMoniker:: bindjeobject** auf, um den Filter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5bc3a-113">If the name matches, call **IMoniker::BindToObject** to create the filter.</span></span>

<span data-ttu-id="5bc3a-114">Der folgende Code zeigt eine Funktion, die diese Schritte ausführt:</span><span class="sxs-lookup"><span data-stu-id="5bc3a-114">The following code shows a function that performs these steps:</span></span>


```C++
HRESULT CreateKernelFilter(
    const GUID &guidCategory,  // Filter category.
    LPCOLESTR szName,          // The name of the filter.
    IBaseFilter **ppFilter     // Receives a pointer to the filter.
)
{
    HRESULT hr;
    ICreateDevEnum *pDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    if (!szName || !ppFilter) 
    {
        return E_POINTER;
    }

    // Create the system device enumerator.
    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC,
        IID_ICreateDevEnum, (void**)&pDevEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    // Create a class enumerator for the specified category.
    hr = pDevEnum->CreateClassEnumerator(guidCategory, &pEnum, 0);
    pDevEnum->Release();
    if (hr != S_OK) // S_FALSE means the category is empty.
    {
        return E_FAIL;
    }

    // Enumerate devices within this category.
    bool bFound = false;
    IMoniker *pMoniker;
    while (!bFound && (S_OK == pEnum->Next(1, &pMoniker, 0)))
    {
        IPropertyBag *pBag = NULL;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, (void **)&pBag);
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        // Check the friendly name.
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(L"FriendlyName", &var, NULL);
        if (SUCCEEDED(hr) && (lstrcmpiW(var.bstrVal, szName) == 0))
        {
            // This is the right filter.
            hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter,
                (void**)ppFilter);
            bFound = true;
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnum->Release();
    return (bFound ? hr : E_FAIL);
}
```



<span data-ttu-id="5bc3a-115">Im folgenden Codebeispiel wird diese Funktion verwendet, um den CC-Decoderfilter zu erstellen und dem Filter Diagramm hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="5bc3a-115">The following code example uses this function to create the CC Decoder filter and add it to the filter graph:</span></span>


```C++
IBaseFilter *pCC = NULL;
hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
    OLESTR("CC Decoder"), &pCC);
if (SUCCEEDED(hr))
{
    hr = pGraph->AddFilter(pCC, L"CC Decoder");
    pCC->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="5bc3a-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5bc3a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bc3a-117">Erweiterte Erfassungs Themen</span><span class="sxs-lookup"><span data-stu-id="5bc3a-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="5bc3a-118">Verwenden des Enumerators für System Geräte</span><span class="sxs-lookup"><span data-stu-id="5bc3a-118">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
</dt> </dl>

 

 



