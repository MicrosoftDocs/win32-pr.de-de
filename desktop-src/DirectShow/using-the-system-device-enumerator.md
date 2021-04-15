---
description: Verwenden des Enumerators für System Geräte
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: Verwenden des Enumerators für System Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f8f66cb64e9f7bb51d6b0716b9fa23cf531435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556421"
---
# <a name="using-the-system-device-enumerator"></a><span data-ttu-id="86c3a-103">Verwenden des Enumerators für System Geräte</span><span class="sxs-lookup"><span data-stu-id="86c3a-103">Using the System Device Enumerator</span></span>

<span data-ttu-id="86c3a-104">Der Enumerator für System Geräte bietet eine einheitliche Möglichkeit zum Auflisten der auf dem System eines Benutzers registrierten Filter, nach Kategorie.</span><span class="sxs-lookup"><span data-stu-id="86c3a-104">The System Device Enumerator provides a uniform way to enumerate, by category, the filters registered on a user's system.</span></span> <span data-ttu-id="86c3a-105">Außerdem unterscheidet es sich zwischen einzelnen Hardware Geräten, auch wenn Sie vom gleichen Filter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="86c3a-105">Moreover, it differentiates between individual hardware devices, even if the same filter supports them.</span></span> <span data-ttu-id="86c3a-106">Dies ist besonders nützlich für Geräte, die die Windows-Treibermodell (WDM) und den ksproxy-Filter verwenden.</span><span class="sxs-lookup"><span data-stu-id="86c3a-106">This is particularly useful for devices that use the Windows Driver Model (WDM) and the KSProxy filter.</span></span> <span data-ttu-id="86c3a-107">Der Benutzer kann z. b. über mehrere WDM-Video Erfassungsgeräte verfügen, die alle vom gleichen Filter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="86c3a-107">For example, the user might have several WDM video capture devices, all supported by the same filter.</span></span> <span data-ttu-id="86c3a-108">Der Enumerator für System Geräte behandelt diese als separate Geräte Instanzen.</span><span class="sxs-lookup"><span data-stu-id="86c3a-108">The System Device Enumerator treats them as separate device instances.</span></span>

<span data-ttu-id="86c3a-109">Der Enumerator für System Geräte erstellt einen Enumerator für eine bestimmte Kategorie, z. b. Audioerfassung oder Video Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="86c3a-109">The System Device Enumerator works by creating an enumerator for a specific category, such as audio capture or video compression.</span></span> <span data-ttu-id="86c3a-110">Der kategorieenumerator gibt einen eindeutigen Moniker für jedes Gerät in der Kategorie zurück.</span><span class="sxs-lookup"><span data-stu-id="86c3a-110">The category enumerator returns a unique moniker for each device in the category.</span></span> <span data-ttu-id="86c3a-111">Der kategorieenumerator enthält automatisch alle relevanten Plug & Play Geräte in der Kategorie.</span><span class="sxs-lookup"><span data-stu-id="86c3a-111">The category enumerator automatically includes any relevant Plug and Play devices in the category.</span></span> <span data-ttu-id="86c3a-112">Eine Liste der Kategorien finden Sie unter [Filter Kategorien](filter-categories.md).</span><span class="sxs-lookup"><span data-stu-id="86c3a-112">For a list of categories, see [Filter Categories](filter-categories.md).</span></span>

<span data-ttu-id="86c3a-113">Gehen Sie folgendermaßen vor, um den Enumerator für System Geräte zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="86c3a-113">To use the System Device Enumerator, do the following:</span></span>

1.  <span data-ttu-id="86c3a-114">Erstellen Sie den Enumerator für Systemgeräte durch Aufrufen von **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="86c3a-114">Create the system device enumerator by calling **CoCreateInstance**.</span></span> <span data-ttu-id="86c3a-115">Der Klassen Bezeichner (CLSID) ist CLSID \_ systemdeviceenum.</span><span class="sxs-lookup"><span data-stu-id="86c3a-115">The class identifier (CLSID) is CLSID\_SystemDeviceEnum.</span></span>
2.  <span data-ttu-id="86c3a-116">Abrufen eines kategorieenumerators durch Aufrufen von [**icreatedevenum:: createclassenumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) mit der CLSID der gewünschten Kategorie.</span><span class="sxs-lookup"><span data-stu-id="86c3a-116">Obtain a category enumerator by calling [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the CLSID of the desired category.</span></span> <span data-ttu-id="86c3a-117">Diese Methode gibt einen **IEnumMoniker** -Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="86c3a-117">This method returns an **IEnumMoniker** interface pointer.</span></span> <span data-ttu-id="86c3a-118">Wenn die Kategorie leer ist (oder nicht vorhanden ist), gibt die Methode " \_ false" anstelle eines Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="86c3a-118">If the category is empty (or does not exist), the method returns S\_FALSE rather than an error code.</span></span> <span data-ttu-id="86c3a-119">Wenn dies der Fall ist, ist der zurückgegebene **IEnumMoniker** -Zeiger **null** , und Dereferenzierung führt zu einer Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="86c3a-119">If so, the returned **IEnumMoniker** pointer is **NULL** and dereferencing it will cause an exception.</span></span> <span data-ttu-id="86c3a-120">Testen Sie daher explizit auf " \_ OK", wenn Sie " **createclassenumschlag**" aufrufen, statt das übliche Makro " **erfolgreich** " aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="86c3a-120">Therefore, explicitly test for S\_OK when you call **CreateClassEnumerator**, instead of calling the usual **SUCCEEDED** macro.</span></span>
3.  <span data-ttu-id="86c3a-121">Verwenden Sie die **IEnumMoniker:: Next** -Methode, um jeden Moniker aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="86c3a-121">Use the **IEnumMoniker::Next** method to enumerate each moniker.</span></span> <span data-ttu-id="86c3a-122">Diese Methode gibt einen **IMoniker** -Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="86c3a-122">This method returns an **IMoniker** interface pointer.</span></span> <span data-ttu-id="86c3a-123">Wenn die **nächste** Methode das Ende der Enumeration erreicht, gibt Sie auch s \_ false zurück. Überprüfen Sie daher erneut auf \_ OK.</span><span class="sxs-lookup"><span data-stu-id="86c3a-123">When the **Next** method reaches the end of the enumeration, it also returns S\_FALSE, so again check for S\_OK.</span></span>
4.  <span data-ttu-id="86c3a-124">Rufen Sie zum Abrufen des anzeigen Amens des Geräts (z. b. zur Anzeige auf der Benutzeroberfläche) die **IMoniker:: bindesstorage** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="86c3a-124">To retrieve the friendly name of the device (for example, to display in the user interface), call the **IMoniker::BindToStorage** method.</span></span>
5.  <span data-ttu-id="86c3a-125">Um den DirectShow-Filter zu erstellen und zu initialisieren, der das Gerät verwaltet, rufen Sie **IMoniker:: bindjeobject** für den Moniker auf.</span><span class="sxs-lookup"><span data-stu-id="86c3a-125">To create and initialize the DirectShow filter that manages the device, call **IMoniker::BindToObject** on the moniker.</span></span> <span data-ttu-id="86c3a-126">Nennen Sie [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , um dem Diagramm den Filter hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="86c3a-126">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the graph.</span></span>

<span data-ttu-id="86c3a-127">Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="86c3a-127">The following diagram illustrates this process.</span></span>

![Auflisten von Geräten](images/sysdevenum.png)

<span data-ttu-id="86c3a-129">Im folgenden Beispiel wird gezeigt, wie die auf dem System des Benutzers installierten Video-Kompressoren aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="86c3a-129">The following example shows how to enumerate the video compressors installed on the user's system.</span></span> <span data-ttu-id="86c3a-130">Aus Gründen der Übersichtlichkeit führt das Beispiel eine minimale Fehlerüberprüfung durch.</span><span class="sxs-lookup"><span data-stu-id="86c3a-130">For brevity, the example performs minimal error checking.</span></span>


```C++
// Create the System Device Enumerator.
HRESULT hr;
ICreateDevEnum *pSysDevEnum = NULL;
hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC_SERVER,
    IID_ICreateDevEnum, (void **)&pSysDevEnum);
if (FAILED(hr))
{
    return hr;
}

// Obtain a class enumerator for the video compressor category.
IEnumMoniker *pEnumCat = NULL;
hr = pSysDevEnum->CreateClassEnumerator(CLSID_VideoCompressorCategory, &pEnumCat, 0);

if (hr == S_OK) 
{
    // Enumerate the monikers.
    IMoniker *pMoniker = NULL;
    ULONG cFetched;
    while(pEnumCat->Next(1, &pMoniker, &cFetched) == S_OK)
    {
        IPropertyBag *pPropBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pPropBag);
        if (SUCCEEDED(hr))
        {
            // To retrieve the filter's friendly name, do the following:
            VARIANT varName;
            VariantInit(&varName);
            hr = pPropBag->Read(L"FriendlyName", &varName, 0);
            if (SUCCEEDED(hr))
            {
                // Display the name in your UI somehow.
            }
            VariantClear(&varName);

            // To create an instance of the filter, do the following:
            IBaseFilter *pFilter;
            hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter,
                (void**)&pFilter);
            // Now add the filter to the graph. 
            //Remember to release pFilter later.
            pPropBag->Release();
        }
        pMoniker->Release();
    }
    pEnumCat->Release();
}
pSysDevEnum->Release();
```



<span data-ttu-id="86c3a-131">**Gerätermoniker**</span><span class="sxs-lookup"><span data-stu-id="86c3a-131">**Device Monikers**</span></span>

<span data-ttu-id="86c3a-132">Für gerätermoniker können Sie den Moniker an die [**IFilterGraph2:: addsourcefilterformoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) -Methode übergeben, um einen Erfassungs Filter für das Gerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="86c3a-132">For device monikers, you can pass the moniker to the [**IFilterGraph2::AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) method to create a capture filter for the device.</span></span> <span data-ttu-id="86c3a-133">Beispielcode finden Sie in der Dokumentation für diese Methode.</span><span class="sxs-lookup"><span data-stu-id="86c3a-133">For example code, see the documentation for that method.</span></span>

<span data-ttu-id="86c3a-134">Die **IMoniker:: GetDisplayName** -Methode gibt den anzeigen Amen für den Moniker zurück.</span><span class="sxs-lookup"><span data-stu-id="86c3a-134">The **IMoniker::GetDisplayName** method returns the display name of the moniker.</span></span> <span data-ttu-id="86c3a-135">Obwohl der Anzeige Name lesbar ist, wird er in der Regel keinem Endbenutzer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="86c3a-135">Although the display name is readable, you would not typically display it to an end-user.</span></span> <span data-ttu-id="86c3a-136">Verwenden Sie stattdessen den anzeigen Amen aus dem Eigenschaften Behälter, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="86c3a-136">Get the friendly name from the property bag instead, as described previously.</span></span>

<span data-ttu-id="86c3a-137">Mit der **IMoniker::P artardisplayname** -Methode oder der **mkparser-DisplayName** -Funktion kann ein standardgerätermoniker für eine bestimmte Filterkategorie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="86c3a-137">The **IMoniker::ParseDisplayName** method or the **MkParseDisplayName** function can be used to create a default device moniker for a given filter category.</span></span> <span data-ttu-id="86c3a-138">Verwenden Sie einen anzeigen Amen mit dem Formular `@device:*:{category-clsid}` , wobei `category-clsid` die Zeichen folgen Darstellung der Kategorie-GUID ist.</span><span class="sxs-lookup"><span data-stu-id="86c3a-138">Use a display name with the form `@device:*:{category-clsid}`, where `category-clsid` is the string representation of the category GUID.</span></span> <span data-ttu-id="86c3a-139">Der standardmoniker ist der erste Moniker, der vom Geräte Enumerator für diese Kategorie zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="86c3a-139">The default moniker is the first moniker returned by the device enumerator for that category.</span></span>

 

 



