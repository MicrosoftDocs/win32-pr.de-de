---
description: Aufzählen von Effekten und Übergängen
ms.assetid: 364b7bfb-5d6e-4ca6-b0c8-7a0180c3f61a
title: Aufzählen von Effekten und Übergängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e533f36501ac8da6015cc31eea6c2c111bf6a208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345397"
---
# <a name="enumerating-effects-and-transitions"></a><span data-ttu-id="6d5ff-103">Aufzählen von Effekten und Übergängen</span><span class="sxs-lookup"><span data-stu-id="6d5ff-103">Enumerating Effects and Transitions</span></span>

<span data-ttu-id="6d5ff-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="6d5ff-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="6d5ff-105">DirectShow stellt ein [System Geräte-Enumeratorobjekt](system-device-enumerator.md) zum Auflisten von Geräten bereit.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-105">DirectShow provides a [System Device Enumerator](system-device-enumerator.md) object for enumerating devices.</span></span> <span data-ttu-id="6d5ff-106">Sie können Sie verwenden, um Moniker für Effekte oder Übergänge abzurufen, die auf dem System des Benutzers installiert sind.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-106">You can use it to retrieve monikers for effects or transitions installed on the user's system.</span></span>

<span data-ttu-id="6d5ff-107">Der Enumerator für Systemgeräte macht die [**ikreatedevenum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-107">The system device enumerator exposes the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span> <span data-ttu-id="6d5ff-108">Es werden kategorieenumeratoren für angegebene Gerätekategorien zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-108">It returns category enumerators for specified device categories.</span></span> <span data-ttu-id="6d5ff-109">Ein kategorieenumerator wiederum macht die [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) -Schnittstelle verfügbar und gibt Moniker für jedes Gerät in der Kategorie zurück.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-109">A category enumerator, in turn, exposes the [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) interface and returns monikers for each device in the category.</span></span> <span data-ttu-id="6d5ff-110">Eine ausführliche Erläuterung der Verwendung von **ikreatedevenum** finden Sie unter Auflisten von [Geräten und Filtern](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="6d5ff-110">For a detailed discussion of using **ICreateDevEnum**, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span> <span data-ttu-id="6d5ff-111">Im folgenden finden Sie eine kurze Zusammenfassung, die speziell für DirectShow-Bearbeitungs Dienste gilt.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-111">The following is a brief summary, specific to DirectShow Editing Services.</span></span>

<span data-ttu-id="6d5ff-112">Führen Sie die folgenden Schritte aus, um Effekte oder Übergänge aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-112">To enumerate effects or transitions, perform the following steps.</span></span>

1.  <span data-ttu-id="6d5ff-113">Erstellen Sie eine Instanz des Enumerators für Systemgeräte.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-113">Create an instance of the system device enumerator.</span></span>
2.  <span data-ttu-id="6d5ff-114">Rufen Sie die [**ikreatedevenum:: feateclassenumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) -Methode auf, um einen kategorieenumerator abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-114">Call the [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method to retrieve a category enumerator.</span></span> <span data-ttu-id="6d5ff-115">Kategorien werden durch Klassen Bezeichner (CLSIDs) definiert.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-115">Categories are defined by class identifiers (CLSIDs).</span></span> <span data-ttu-id="6d5ff-116">Verwenden Sie CLSID- \_ VideoEffects1Category für Effekte oder CLSID \_ VideoEffects2Category für Übergänge.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-116">Use CLSID\_VideoEffects1Category for effects or CLSID\_VideoEffects2Category for transitions.</span></span>
3.  <span data-ttu-id="6d5ff-117">Rufen Sie **IEnumMoniker:: Next** auf, um jeden Moniker in der-Enumeration abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-117">Call **IEnumMoniker::Next** to retrieve each moniker in the enumeration.</span></span>
4.  <span data-ttu-id="6d5ff-118">Rufen Sie für jeden Moniker **IMoniker:: bindesstorage** auf, um den zugehörigen Eigenschaften Behälter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-118">For each moniker, call **IMoniker::BindToStorage** to retrieve its associated property bag.</span></span>

<span data-ttu-id="6d5ff-119">Der Eigenschaften Behälter enthält den anzeigen Amen und die Globally Unique Identifier (GUID) für den Effekt oder den Übergang.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-119">The property bag contains the friendly name and the globally unique identifier (GUID) for the effect or transition.</span></span> <span data-ttu-id="6d5ff-120">Eine Anwendung kann eine Liste von anzeigen Amen anzeigen und dann die entsprechende GUID abrufen.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-120">An application can display a list of friendly names and then obtain the corresponding GUID.</span></span>

<span data-ttu-id="6d5ff-121">Diese Schritte werden im folgenden Codebeispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6d5ff-121">The following code example illustrates these steps.</span></span>


```C++
ICreateDevEnum *pCreateDevEnum = NULL;
IEnumMoniker *pEnumMoniker = NULL;

// Create the System Device Enumerator.
HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
    CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, (void**)&pCreateDevEnum);
if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

// Create an enumerator for the video effects category.
hr = pCreateDevEnum->CreateClassEnumerator(
    CLSID_VideoEffects1Category,  // Video effects category. 
    &pEnumMoniker, 0);               

// Note: Use CLSID_VideoEffects2Category for video transitions.

if (hr == S_OK)  // S_FALSE means the category is empty.
{
    // Enumerate each video effect.
    IMoniker *pMoniker;
    while (S_OK == pEnumMoniker->Next(1, &pMoniker, NULL))
    {
        IPropertyBag *pBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pBag);
        if(FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(OLESTR("FriendlyName"), &var, NULL);
        if (SUCCEEDED(hr))
        {
            if ( ... )  // Check if var.bstrVal is the name you want.
            {
                VARIANT var2;
                GUID guid;
                var2.vt = VT_BSTR;
                pBag->Read(OLESTR("guid"), &var2, NULL);
                CLSIDFromString(var2.bstrVal, &guid);
                VariantClear(&var2);
                // GUID is now the CLSID for the effect.
            }
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnumMoniker->Release();
}
pCreateDevEnum->Release();
```



## <a name="related-topics"></a><span data-ttu-id="6d5ff-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d5ff-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d5ff-123">Arbeiten mit Effekten und Übergängen</span><span class="sxs-lookup"><span data-stu-id="6d5ff-123">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
