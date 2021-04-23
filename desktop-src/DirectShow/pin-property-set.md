---
description: Pin-Eigenschaftssatz
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Pin-Eigenschaftssatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53955ba1f075094c4fb2f6324ed143ca54f72c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909618"
---
# <a name="pin-property-set"></a><span data-ttu-id="f53b5-103">Pin-Eigenschaftssatz</span><span class="sxs-lookup"><span data-stu-id="f53b5-103">Pin Property Set</span></span>

<span data-ttu-id="f53b5-104">Der Pin-Eigenschaftensatz gibt die Pinkategorie für eine Stecknadel in einem Filter zurück.</span><span class="sxs-lookup"><span data-stu-id="f53b5-104">The pin property set returns the pin category for a pin on a filter.</span></span> <span data-ttu-id="f53b5-105">Die Kategorie wird vom Filter festgelegt, wenn er die Stecknadel erstellt. Die Kategorie gibt an, welche Art von Daten der Pin von diesem Pin übermittelt oder empfängt.</span><span class="sxs-lookup"><span data-stu-id="f53b5-105">The category is set by the filter when it creates the pin; the category indicates what type of data the pin is delivered or receives by this pin.</span></span>



| <span data-ttu-id="f53b5-106">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="f53b5-106">Label</span></span> | <span data-ttu-id="f53b5-107">Wert</span><span class="sxs-lookup"><span data-stu-id="f53b5-107">Value</span></span> |
|-------------------|----------------------|
| <span data-ttu-id="f53b5-108">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="f53b5-108">Property Set GUID</span></span> | <span data-ttu-id="f53b5-109">**AMPROPSETID \_ Pin**</span><span class="sxs-lookup"><span data-stu-id="f53b5-109">**AMPROPSETID\_Pin**</span></span> |



 



| <span data-ttu-id="f53b5-110">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="f53b5-110">Property ID</span></span>                   | <span data-ttu-id="f53b5-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f53b5-111">Description</span></span>                      |
|-------------------------------|----------------------------------|
| <span data-ttu-id="f53b5-112">**\_AMPROPERTY-PIN-KATEGORIE \_**</span><span class="sxs-lookup"><span data-stu-id="f53b5-112">**AMPROPERTY\_PIN\_CATEGORY**</span></span> | <span data-ttu-id="f53b5-113">Gibt die Kategorie eines Stecknadels an.</span><span class="sxs-lookup"><span data-stu-id="f53b5-113">Specifies the category of a pin.</span></span> |



 

<span data-ttu-id="f53b5-114">DirectShow definiert die folgenden Pinkategorien in der Headerdatei "Uuids.h".</span><span class="sxs-lookup"><span data-stu-id="f53b5-114">DirectShow defines the following pin categories in the Uuids.h header file.</span></span>



| <span data-ttu-id="f53b5-115">Kategorie-GUID</span><span class="sxs-lookup"><span data-stu-id="f53b5-115">Category GUID</span></span>                     | <span data-ttu-id="f53b5-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f53b5-116">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f53b5-117">**PINKATEGORIE \_ \_ ANALOGVIDEOIN**</span><span class="sxs-lookup"><span data-stu-id="f53b5-117">**PIN\_CATEGORY\_ANALOGVIDEOIN**</span></span>  | <span data-ttu-id="f53b5-118">Eingabepin des Erfassungsfilters, der analog verwendet und digitalisiert.</span><span class="sxs-lookup"><span data-stu-id="f53b5-118">Input pin of the capture filter that takes analog and digitizes it.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="f53b5-119">**AUFNAHME DER \_ \_ PINKATEGORIE**</span><span class="sxs-lookup"><span data-stu-id="f53b5-119">**PIN\_CATEGORY\_CAPTURE**</span></span>        | <span data-ttu-id="f53b5-120">Aufnahmepin.</span><span class="sxs-lookup"><span data-stu-id="f53b5-120">Capture pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f53b5-121">**PINKATEGORIE \_ \_ CC**</span><span class="sxs-lookup"><span data-stu-id="f53b5-121">**PIN\_CATEGORY\_CC**</span></span>             | <span data-ttu-id="f53b5-122">Heften Sie die Untertiteldaten aus Zeile 21 an.</span><span class="sxs-lookup"><span data-stu-id="f53b5-122">Pin providing closed captioning data from Line 21.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="f53b5-123">**\_EDS DER \_ PIN-KATEGORIE**</span><span class="sxs-lookup"><span data-stu-id="f53b5-123">**PIN\_CATEGORY\_EDS**</span></span>            | <span data-ttu-id="f53b5-124">Pin für erweiterte Data Services (Zeile 21, sogar Felder).</span><span class="sxs-lookup"><span data-stu-id="f53b5-124">Pin providing Extended Data Services (Line 21, even fields).</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f53b5-125">**\_ \_ PIN-KATEGORIE -HEFTE**</span><span class="sxs-lookup"><span data-stu-id="f53b5-125">**PIN\_CATEGORY\_NABTS**</span></span>          | <span data-ttu-id="f53b5-126">Heften Sie die Daten des Us-amerikanischen Videotext-Standards an.</span><span class="sxs-lookup"><span data-stu-id="f53b5-126">Pin providing North American Videotext Standard data.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="f53b5-127">**\_VORSCHAU DER PIN-KATEGORIE \_**</span><span class="sxs-lookup"><span data-stu-id="f53b5-127">**PIN\_CATEGORY\_PREVIEW**</span></span>        | <span data-ttu-id="f53b5-128">Vorschau-Stecknadel.</span><span class="sxs-lookup"><span data-stu-id="f53b5-128">Preview pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f53b5-129">**PIN \_ CATEGORY \_ STILL**</span><span class="sxs-lookup"><span data-stu-id="f53b5-129">**PIN\_CATEGORY\_STILL**</span></span>          | <span data-ttu-id="f53b5-130">Stecknadel, die ein Standbild bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f53b5-130">Pin that provides a still image.</span></span> <span data-ttu-id="f53b5-131">Der Erfassungspin des Filters muss verbunden sein, bevor der Pin für das Standbild verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="f53b5-131">The filter's capture pin must be connected before the still-image pin is connected.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="f53b5-132">**PIN \_ CATEGORY \_ TELETEXT**</span><span class="sxs-lookup"><span data-stu-id="f53b5-132">**PIN\_CATEGORY\_TELETEXT**</span></span>       | <span data-ttu-id="f53b5-133">Anheften der Bereitstellung von Teletext (eine Untertitelvariante).</span><span class="sxs-lookup"><span data-stu-id="f53b5-133">Pin providing teletext (a closed captioning variant).</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="f53b5-134">**PIN \_ CATEGORY \_ TIMECODE**</span><span class="sxs-lookup"><span data-stu-id="f53b5-134">**PIN\_CATEGORY\_TIMECODE**</span></span>       | <span data-ttu-id="f53b5-135">Anheften der Bereitstellung von Zeitcodedaten.</span><span class="sxs-lookup"><span data-stu-id="f53b5-135">Pin providing timecode data.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f53b5-136">**PIN \_ CATEGORY \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="f53b5-136">**PIN\_CATEGORY\_VBI**</span></span>            | <span data-ttu-id="f53b5-137">Stecknadel, die Daten zum vertikalen Leerungsintervall bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f53b5-137">Pin providing vertical blanking interval data.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f53b5-138">**PIN \_ CATEGORY \_ VIDEOPORT**</span><span class="sxs-lookup"><span data-stu-id="f53b5-138">**PIN\_CATEGORY\_VIDEOPORT**</span></span>      | <span data-ttu-id="f53b5-139">Videoausgabepin, der mit dem Eingabepin 0 (null) auf dem [Overlay-Mixer](overlay-mixer-filter.md)verbunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="f53b5-139">Video output pin to be connected to input pin zero on the [Overlay Mixer](overlay-mixer-filter.md).</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="f53b5-140">**PIN \_ CATEGORY \_ VIDEOPORT \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="f53b5-140">**PIN\_CATEGORY\_VIDEOPORT\_VBI**</span></span> | <span data-ttu-id="f53b5-141">Stecknadel für die Verbindung mit der [VBI-Oberflächenbelegung](vbi-surface-allocator.md), dem VBI-Oberflächenbelegungsfilter, der benötigt wird, um den richtigen Videospeicher für Dinge wie Untertitelüberlagerungen in Szenarien zuzuweisen, in denen ein Videoport verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f53b5-141">Pin to be connected to the [VBI Surface Allocator](vbi-surface-allocator.md), the VBI surface allocator filter that is needed to allocate the correct video memory for things like closed captioning overlays in scenarios where a video port is being used.</span></span> <span data-ttu-id="f53b5-142">PCI-, IEEE 1394- und USB-Szenarien verwenden diesen Filter nicht.</span><span class="sxs-lookup"><span data-stu-id="f53b5-142">PCI, IEEE 1394, and USB scenarios do not use this filter.</span></span> |
| <span data-ttu-id="f53b5-143">**PINNAME \_ VIDEO \_ CC \_ CAPTURE**</span><span class="sxs-lookup"><span data-stu-id="f53b5-143">**PINNAME\_VIDEO\_CC\_CAPTURE**</span></span>   | <span data-ttu-id="f53b5-144">Hardwareslicing-Pin für Untertitel</span><span class="sxs-lookup"><span data-stu-id="f53b5-144">Hardware slicing closed-captioning pin</span></span>                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="f53b5-145">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f53b5-145">This property is read-only.</span></span>

### <a name="example-code"></a><span data-ttu-id="f53b5-146">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="f53b5-146">Example Code</span></span>

<span data-ttu-id="f53b5-147">Der folgende Code zeigt, wie Sie überprüfen, ob ein Pin diesen Eigenschaftensatz unterstützt, und wenn ja, wie Sie die Pinkategorie abrufen:</span><span class="sxs-lookup"><span data-stu-id="f53b5-147">The following code shows how to check whether a pin supports this property set, and if so, how to obtain the pin category:</span></span>


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="f53b5-148">In diesem Beispiel wird die [SafeRelease-Funktion](../medfound/saferelease.md) verwendet, um Schnittstellenzeiger freizugeben.</span><span class="sxs-lookup"><span data-stu-id="f53b5-148">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f53b5-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f53b5-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f53b5-150">Anheftanforderungen für Erfassungsfilter</span><span class="sxs-lookup"><span data-stu-id="f53b5-150">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="f53b5-151">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="f53b5-151">Property Sets</span></span>](property-sets.md)
</dt> <dt>

[<span data-ttu-id="f53b5-152">Arbeiten mit Pinkategorien</span><span class="sxs-lookup"><span data-stu-id="f53b5-152">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 
