---
description: Schlüssel Übergang
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: Schlüssel Übergang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e4f83bbe26f49989d612efe718c2d838ce7f1d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860095"
---
# <a name="key-transition"></a><span data-ttu-id="409b5-103">Schlüssel Übergang</span><span class="sxs-lookup"><span data-stu-id="409b5-103">Key Transition</span></span>

> [!Note]  
> <span data-ttu-id="409b5-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="409b5-104">\[Deprecated.</span></span> <span data-ttu-id="409b5-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="409b5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="409b5-106">Der Schlüssel Übergang führt die Schlüssel Erstellung basierend auf RGB-Wert, Alpha-Wert, Farbton oder Leuchtkraft durch.</span><span class="sxs-lookup"><span data-stu-id="409b5-106">The Key transition performs keying based on RGB value, alpha value, hue or luminance.</span></span>

<span data-ttu-id="409b5-107">Die folgende Abbildung zeigt den Schlüssel Übergang:</span><span class="sxs-lookup"><span data-stu-id="409b5-107">The following image shows the key transition:</span></span>

![Schlüssel Übergang](images/trans-key.png)

<span data-ttu-id="409b5-109">Klassen-ID (CLSID): {C5B19592-145E-11d3-9F04-006008039E37}</span><span class="sxs-lookup"><span data-stu-id="409b5-109">Class ID (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}</span></span>

<span data-ttu-id="409b5-110">CLSID-Variablen Name: CLSID \_ dxtkey</span><span class="sxs-lookup"><span data-stu-id="409b5-110">CLSID Variable Name: CLSID\_DxtKey</span></span>

<span data-ttu-id="409b5-111">Anzeige Name: "dxtkey"</span><span class="sxs-lookup"><span data-stu-id="409b5-111">Friendly Name: "DxtKey"</span></span>

<span data-ttu-id="409b5-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="409b5-112">Properties</span></span>



| <span data-ttu-id="409b5-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="409b5-113">Property</span></span>   | <span data-ttu-id="409b5-114">type</span><span class="sxs-lookup"><span data-stu-id="409b5-114">Type</span></span>  | <span data-ttu-id="409b5-115">Gültiger Bereich</span><span class="sxs-lookup"><span data-stu-id="409b5-115">Valid range</span></span>           | <span data-ttu-id="409b5-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="409b5-116">Description</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="409b5-117">Gilt für</span><span class="sxs-lookup"><span data-stu-id="409b5-117">Applies To</span></span>                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="409b5-118">Farbton</span><span class="sxs-lookup"><span data-stu-id="409b5-118">Hue</span></span>        | <span data-ttu-id="409b5-119">INT</span><span class="sxs-lookup"><span data-stu-id="409b5-119">int</span></span>   | <span data-ttu-id="409b5-120">0 – 360</span><span class="sxs-lookup"><span data-stu-id="409b5-120">0–360</span></span>                 | <span data-ttu-id="409b5-121">Der Farbton Wert, für den der Schlüssel angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="409b5-121">The hue value on which to key.</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="409b5-122">Farbton</span><span class="sxs-lookup"><span data-stu-id="409b5-122">Hue</span></span>                            |
| <span data-ttu-id="409b5-123">Invertierung</span><span class="sxs-lookup"><span data-stu-id="409b5-123">Invert</span></span>     | <span data-ttu-id="409b5-124">BOOL</span><span class="sxs-lookup"><span data-stu-id="409b5-124">BOOL</span></span>  | <span data-ttu-id="409b5-125">**False** oder **true**</span><span class="sxs-lookup"><span data-stu-id="409b5-125">**FALSE** or **TRUE**</span></span> | <span data-ttu-id="409b5-126">Boolescher Wert, der angibt, ob die Standardoperation des Schlüssels umgekehrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="409b5-126">Boolean value indicating whether to invert the default operation of the key.</span></span> <span data-ttu-id="409b5-127">Wenn der Wert **false** ist, werden die Pixel im überliegenden Bild standardmäßig transparent gemacht.</span><span class="sxs-lookup"><span data-stu-id="409b5-127">If **FALSE**, pixels in the overlying image are made transparent in the default manner.</span></span> <span data-ttu-id="409b5-128">Wenn **true**, kehrt der Vorgang um.</span><span class="sxs-lookup"><span data-stu-id="409b5-128">If **TRUE**, the operation inverts.</span></span>                                                   | <span data-ttu-id="409b5-129">Chroma, Hue, Leuchtkraft, nicht rot</span><span class="sxs-lookup"><span data-stu-id="409b5-129">Chroma, Hue, Luminance, Nonred</span></span> |
| <span data-ttu-id="409b5-130">KeyType</span><span class="sxs-lookup"><span data-stu-id="409b5-130">KeyType</span></span>    | <span data-ttu-id="409b5-131">INT</span><span class="sxs-lookup"><span data-stu-id="409b5-131">int</span></span>   | <span data-ttu-id="409b5-132">Siehe Hinweise</span><span class="sxs-lookup"><span data-stu-id="409b5-132">See Remarks</span></span>           | <span data-ttu-id="409b5-133">Gibt den Typ des Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="409b5-133">Specifies the type of key.</span></span> <span data-ttu-id="409b5-134">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="409b5-134">For more information, see Remarks.</span></span>                                                                                                                                                                                              | <span data-ttu-id="409b5-135">Alle</span><span class="sxs-lookup"><span data-stu-id="409b5-135">All</span></span>                            |
| <span data-ttu-id="409b5-136">Luminance</span><span class="sxs-lookup"><span data-stu-id="409b5-136">Luminance</span></span>  | <span data-ttu-id="409b5-137">INT</span><span class="sxs-lookup"><span data-stu-id="409b5-137">int</span></span>   | <span data-ttu-id="409b5-138">0 – 100</span><span class="sxs-lookup"><span data-stu-id="409b5-138">0–100</span></span>                 | <span data-ttu-id="409b5-139">Der Wert für die Leuchtkraft, auf den der Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="409b5-139">The luminance value on which to key.</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="409b5-140">Luminance</span><span class="sxs-lookup"><span data-stu-id="409b5-140">Luminance</span></span>                      |
| <span data-ttu-id="409b5-141">RGB</span><span class="sxs-lookup"><span data-stu-id="409b5-141">RGB</span></span>        | <span data-ttu-id="409b5-142">DWORD</span><span class="sxs-lookup"><span data-stu-id="409b5-142">DWORD</span></span> | <span data-ttu-id="409b5-143">0x0 – 0xffffff</span><span class="sxs-lookup"><span data-stu-id="409b5-143">0x0 – 0xFFFFFF</span></span>        | <span data-ttu-id="409b5-144">Die Farbe, in der der Schlüssel angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="409b5-144">The color on which to key.</span></span> <span data-ttu-id="409b5-145">Der Wert ist eine hexadezimale Zahl mit dem Format 0x *RRGGBB*, wobei *RR* der rote Wert, *GG* der grüne Wert und *BB* der blaue Wert ist.</span><span class="sxs-lookup"><span data-stu-id="409b5-145">The value is a hexadecimal number with the format 0x *RRGGBB*, where *RR* is the red value, *GG* is the green value, and *BB* is the blue value.</span></span> <span data-ttu-id="409b5-146">(Rein rot, grün und blau sind 0xFF0000, 0x00FF00 bzw. 0x0000FF.)</span><span class="sxs-lookup"><span data-stu-id="409b5-146">(Pure red, green, and blue are 0xFF0000, 0x00FF00, and 0x0000FF, respectively.)</span></span> | <span data-ttu-id="409b5-147">Chroma</span><span class="sxs-lookup"><span data-stu-id="409b5-147">Chroma</span></span>                         |
| <span data-ttu-id="409b5-148">Ähnlichkeit</span><span class="sxs-lookup"><span data-stu-id="409b5-148">Similarity</span></span> | <span data-ttu-id="409b5-149">INT</span><span class="sxs-lookup"><span data-stu-id="409b5-149">int</span></span>   | <span data-ttu-id="409b5-150">0 – 100</span><span class="sxs-lookup"><span data-stu-id="409b5-150">0–100</span></span>                 | <span data-ttu-id="409b5-151">Der Bereich der Farbdaten, der transparent wird.</span><span class="sxs-lookup"><span data-stu-id="409b5-151">The range of color data that becomes transparent.</span></span> <span data-ttu-id="409b5-152">Bei höheren Werten ist eine größere Anzahl ähnlicher Farben transparent.</span><span class="sxs-lookup"><span data-stu-id="409b5-152">At higher values, a wider range of similar colors is transparent.</span></span>                                                                                                                                        | <span data-ttu-id="409b5-153">Chroma, nicht rot</span><span class="sxs-lookup"><span data-stu-id="409b5-153">Chroma, Nonred</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="409b5-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="409b5-154">Remarks</span></span>

<span data-ttu-id="409b5-155">Der Typ des Schlüssels, der ausgeführt wird, hängt vom Wert der **KeyType** -Eigenschaft ab, die einen der folgenden Werte aufweisen muss:</span><span class="sxs-lookup"><span data-stu-id="409b5-155">The type of key that is performed depends on the value of the **KeyType** property, which must be one of the following:</span></span>



| <span data-ttu-id="409b5-156">Wert</span><span class="sxs-lookup"><span data-stu-id="409b5-156">Value</span></span> | <span data-ttu-id="409b5-157">Enumeration</span><span class="sxs-lookup"><span data-stu-id="409b5-157">Enumeration</span></span>       | <span data-ttu-id="409b5-158">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="409b5-158">Description</span></span>                                           |
|-------|-------------------|-------------------------------------------------------|
| <span data-ttu-id="409b5-159">0</span><span class="sxs-lookup"><span data-stu-id="409b5-159">0</span></span>     | <span data-ttu-id="409b5-160">dxtkey \_ RGB</span><span class="sxs-lookup"><span data-stu-id="409b5-160">DXTKEY\_RGB</span></span>       | <span data-ttu-id="409b5-161">Chroma-Schlüssel (Schlüssel nach RGB-Wert).</span><span class="sxs-lookup"><span data-stu-id="409b5-161">Chroma key (key by RGB value).</span></span>                        |
| <span data-ttu-id="409b5-162">1</span><span class="sxs-lookup"><span data-stu-id="409b5-162">1</span></span>     | <span data-ttu-id="409b5-163">dxtkey \_ nicht rot</span><span class="sxs-lookup"><span data-stu-id="409b5-163">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="409b5-164">Nicht-rote Taste.</span><span class="sxs-lookup"><span data-stu-id="409b5-164">Nonred key.</span></span> <span data-ttu-id="409b5-165">(Macht blaue und grüne Bereiche transparent.)</span><span class="sxs-lookup"><span data-stu-id="409b5-165">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="409b5-166">2</span><span class="sxs-lookup"><span data-stu-id="409b5-166">2</span></span>     | <span data-ttu-id="409b5-167">dxtkey- \_ Leuchtkraft</span><span class="sxs-lookup"><span data-stu-id="409b5-167">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="409b5-168">Der Schlüssel für die Leuchtkraft.</span><span class="sxs-lookup"><span data-stu-id="409b5-168">Luminance key.</span></span>                                        |
| <span data-ttu-id="409b5-169">3</span><span class="sxs-lookup"><span data-stu-id="409b5-169">3</span></span>     | <span data-ttu-id="409b5-170">dxtkey \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="409b5-170">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="409b5-171">Schlüssel nach Alpha Wert.</span><span class="sxs-lookup"><span data-stu-id="409b5-171">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="409b5-172">4</span><span class="sxs-lookup"><span data-stu-id="409b5-172">4</span></span>     | <span data-ttu-id="409b5-173">dxtkey- \_ Farbton</span><span class="sxs-lookup"><span data-stu-id="409b5-173">DXTKEY\_HUE</span></span>       | <span data-ttu-id="409b5-174">Schlüssel nach Farbton.</span><span class="sxs-lookup"><span data-stu-id="409b5-174">Key by hue.</span></span>                                           |



 

<span data-ttu-id="409b5-175">Der Schlüsseltyp ist standardmäßig dxtkey \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="409b5-175">The key type defaults to DXTKEY\_ALPHA.</span></span>

 

 



