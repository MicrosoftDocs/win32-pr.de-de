---
description: PIN-Eigenschaften Satz
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: PIN-Eigenschaften Satz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc2d3ed55d7fed70d37a92427d1288ed58aef65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392505"
---
# <a name="pin-property-set"></a><span data-ttu-id="0328a-103">PIN-Eigenschaften Satz</span><span class="sxs-lookup"><span data-stu-id="0328a-103">Pin Property Set</span></span>

<span data-ttu-id="0328a-104">Der PIN-Eigenschaften Satz gibt die PIN-Kategorie für eine PIN in einem Filter zurück.</span><span class="sxs-lookup"><span data-stu-id="0328a-104">The pin property set returns the pin category for a pin on a filter.</span></span> <span data-ttu-id="0328a-105">Die Kategorie wird vom Filter festgelegt, wenn die PIN erstellt wird. die Kategorie gibt an, welche Art von Daten die PIN übermittelt oder von dieser Pin empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="0328a-105">The category is set by the filter when it creates the pin; the category indicates what type of data the pin is delivered or receives by this pin.</span></span>



|                   |                      |
|-------------------|----------------------|
| <span data-ttu-id="0328a-106">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="0328a-106">Property Set GUID</span></span> | <span data-ttu-id="0328a-107">**Ampropeltid- \_ PIN**</span><span class="sxs-lookup"><span data-stu-id="0328a-107">**AMPROPSETID\_Pin**</span></span> |



 



| <span data-ttu-id="0328a-108">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="0328a-108">Property ID</span></span>                   | <span data-ttu-id="0328a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0328a-109">Description</span></span>                      |
|-------------------------------|----------------------------------|
| <span data-ttu-id="0328a-110">**amproperty- \_ Pin- \_ Kategorie**</span><span class="sxs-lookup"><span data-stu-id="0328a-110">**AMPROPERTY\_PIN\_CATEGORY**</span></span> | <span data-ttu-id="0328a-111">Gibt die Kategorie einer PIN an.</span><span class="sxs-lookup"><span data-stu-id="0328a-111">Specifies the category of a pin.</span></span> |



 

<span data-ttu-id="0328a-112">DirectShow definiert die folgenden Pin-Kategorien in der Header Datei "UUIDs. h".</span><span class="sxs-lookup"><span data-stu-id="0328a-112">DirectShow defines the following pin categories in the Uuids.h header file.</span></span>



| <span data-ttu-id="0328a-113">Kategorie-GUID</span><span class="sxs-lookup"><span data-stu-id="0328a-113">Category GUID</span></span>                     | <span data-ttu-id="0328a-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0328a-114">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0328a-115">**PIN- \_ Kategorie \_ Analog gvideoin**</span><span class="sxs-lookup"><span data-stu-id="0328a-115">**PIN\_CATEGORY\_ANALOGVIDEOIN**</span></span>  | <span data-ttu-id="0328a-116">Eingabepin des Erfassungs Filters, der die Analogie annimmt und Sie standardisiert.</span><span class="sxs-lookup"><span data-stu-id="0328a-116">Input pin of the capture filter that takes analog and digitizes it.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="0328a-117">**Erfassung der PIN- \_ Kategorie \_**</span><span class="sxs-lookup"><span data-stu-id="0328a-117">**PIN\_CATEGORY\_CAPTURE**</span></span>        | <span data-ttu-id="0328a-118">PIN erfassen.</span><span class="sxs-lookup"><span data-stu-id="0328a-118">Capture pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="0328a-119">**PIN- \_ Kategorie \_ CC**</span><span class="sxs-lookup"><span data-stu-id="0328a-119">**PIN\_CATEGORY\_CC**</span></span>             | <span data-ttu-id="0328a-120">PIN, die Untertitel Daten aus Zeile 21 bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0328a-120">Pin providing closed captioning data from Line 21.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="0328a-121">**PIN- \_ Kategorie \_ EDS**</span><span class="sxs-lookup"><span data-stu-id="0328a-121">**PIN\_CATEGORY\_EDS**</span></span>            | <span data-ttu-id="0328a-122">PIN, die erweiterte Data Services bereitstellt (Zeile 21, sogar Felder).</span><span class="sxs-lookup"><span data-stu-id="0328a-122">Pin providing Extended Data Services (Line 21, even fields).</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="0328a-123">**anheften der \_ Kategorie \_**</span><span class="sxs-lookup"><span data-stu-id="0328a-123">**PIN\_CATEGORY\_NABTS**</span></span>          | <span data-ttu-id="0328a-124">PIN, die Nordamerika-Videotext-Standard Daten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0328a-124">Pin providing North American Videotext Standard data.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="0328a-125">**\_Kategorie \_ Vorschau anheften**</span><span class="sxs-lookup"><span data-stu-id="0328a-125">**PIN\_CATEGORY\_PREVIEW**</span></span>        | <span data-ttu-id="0328a-126">Vorschau der PIN.</span><span class="sxs-lookup"><span data-stu-id="0328a-126">Preview pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="0328a-127">**PIN- \_ Kategorie \_ immer noch**</span><span class="sxs-lookup"><span data-stu-id="0328a-127">**PIN\_CATEGORY\_STILL**</span></span>          | <span data-ttu-id="0328a-128">PIN, die ein Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="0328a-128">Pin that provides a still image.</span></span> <span data-ttu-id="0328a-129">Die Erfassungs-PIN des Filters muss verbunden sein, bevor die PIN mit dem Bild "immer noch" verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="0328a-129">The filter's capture pin must be connected before the still-image pin is connected.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="0328a-130">**Kategorieinformationen für die PIN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0328a-130">**PIN\_CATEGORY\_TELETEXT**</span></span>       | <span data-ttu-id="0328a-131">PIN, die Teletext bereitstellt (eine Untertitel Variante).</span><span class="sxs-lookup"><span data-stu-id="0328a-131">Pin providing teletext (a closed captioning variant).</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="0328a-132">**\_ \_ Zeit Leitzahl der PIN-Kategorie**</span><span class="sxs-lookup"><span data-stu-id="0328a-132">**PIN\_CATEGORY\_TIMECODE**</span></span>       | <span data-ttu-id="0328a-133">PIN, die Zeit Code Daten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0328a-133">Pin providing timecode data.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="0328a-134">**PIN- \_ Kategorie \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="0328a-134">**PIN\_CATEGORY\_VBI**</span></span>            | <span data-ttu-id="0328a-135">Pin zur Bereitstellung vertikaler blankinginterval-Daten.</span><span class="sxs-lookup"><span data-stu-id="0328a-135">Pin providing vertical blanking interval data.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="0328a-136">**PIN- \_ Kategorie \_ Videoport**</span><span class="sxs-lookup"><span data-stu-id="0328a-136">**PIN\_CATEGORY\_VIDEOPORT**</span></span>      | <span data-ttu-id="0328a-137">Die Video Ausgabe-PIN, die mit der Eingabe-PIN NULL auf dem [Überlagerungs Mixer](overlay-mixer-filter.md)verbunden werden soll</span><span class="sxs-lookup"><span data-stu-id="0328a-137">Video output pin to be connected to input pin zero on the [Overlay Mixer](overlay-mixer-filter.md).</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="0328a-138">**PIN- \_ Kategorie \_ Videoport \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="0328a-138">**PIN\_CATEGORY\_VIDEOPORT\_VBI**</span></span> | <span data-ttu-id="0328a-139">Anheften an den [VBI Surface Allocator](vbi-surface-allocator.md), den VBI Surface Allocator-Filter, der benötigt wird, um den korrekten Videospeicher für Dinge wie Untertitel Überschriften in Szenarios zuzuordnen, in denen ein Videoport verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0328a-139">Pin to be connected to the [VBI Surface Allocator](vbi-surface-allocator.md), the VBI surface allocator filter that is needed to allocate the correct video memory for things like closed captioning overlays in scenarios where a video port is being used.</span></span> <span data-ttu-id="0328a-140">Dieser Filter wird von PCI-, IEEE 1394-und USB-Szenarien nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0328a-140">PCI, IEEE 1394, and USB scenarios do not use this filter.</span></span> |
| <span data-ttu-id="0328a-141">**Pinname \_ Video \_ CC \_ Capture**</span><span class="sxs-lookup"><span data-stu-id="0328a-141">**PINNAME\_VIDEO\_CC\_CAPTURE**</span></span>   | <span data-ttu-id="0328a-142">Hardware Aufteilung mit Untertitel</span><span class="sxs-lookup"><span data-stu-id="0328a-142">Hardware slicing closed-captioning pin</span></span>                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="0328a-143">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0328a-143">This property is read-only.</span></span>

### <a name="example-code"></a><span data-ttu-id="0328a-144">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="0328a-144">Example Code</span></span>

<span data-ttu-id="0328a-145">Der folgende Code zeigt, wie Sie überprüfen können, ob eine PIN diesen Eigenschaften Satz unterstützt, und wenn dies der Fall ist, wie Sie die PIN-Kategorie abrufen:</span><span class="sxs-lookup"><span data-stu-id="0328a-145">The following code shows how to check whether a pin supports this property set, and if so, how to obtain the pin category:</span></span>


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
> <span data-ttu-id="0328a-146">In diesem Beispiel wird die Funktion " [saferelease](../medfound/saferelease.md) " verwendet, um Schnittstellen Zeiger freizugeben.</span><span class="sxs-lookup"><span data-stu-id="0328a-146">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0328a-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0328a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0328a-148">PIN-Anforderungen für Erfassungs Filter</span><span class="sxs-lookup"><span data-stu-id="0328a-148">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="0328a-149">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="0328a-149">Property Sets</span></span>](property-sets.md)
</dt> <dt>

[<span data-ttu-id="0328a-150">Arbeiten mit PIN-Kategorien</span><span class="sxs-lookup"><span data-stu-id="0328a-150">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 
