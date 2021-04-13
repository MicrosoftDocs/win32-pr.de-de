---
title: Histogrammeffekt
description: Verwenden Sie den histogrammeffekt, um ein Histogramm für die Eingabe Bitmap basierend auf der angegebenen Anzahl von Containern zu generieren.
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- histogrammeffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b654ffb2b830914b00a59490ceb429b5de9c51cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391829"
---
# <a name="histogram-effect"></a><span data-ttu-id="7982f-104">Histogrammeffekt</span><span class="sxs-lookup"><span data-stu-id="7982f-104">Histogram effect</span></span>

<span data-ttu-id="7982f-105">Verwenden Sie den histogrammeffekt, um ein Histogramm für die Eingabe Bitmap basierend auf der angegebenen Anzahl von Containern zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7982f-105">Use the histogram effect to generate a histogram for the input bitmap based on the specified number of bins.</span></span>

<span data-ttu-id="7982f-106">Die CLSID für diesen Effekt ist CLSID \_ D2D1Histogram.</span><span class="sxs-lookup"><span data-stu-id="7982f-106">The CLSID for this effect is CLSID\_D2D1Histogram.</span></span>

-   [<span data-ttu-id="7982f-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7982f-107">Example</span></span>](#example)
-   [<span data-ttu-id="7982f-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7982f-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="7982f-109">Kanalselektoren</span><span class="sxs-lookup"><span data-stu-id="7982f-109">Channel selectors</span></span>](#channel-selectors)
-   [<span data-ttu-id="7982f-110">Datenausgabe</span><span class="sxs-lookup"><span data-stu-id="7982f-110">Data output</span></span>](#data-output)
-   [<span data-ttu-id="7982f-111">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="7982f-111">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="7982f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7982f-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7982f-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7982f-113">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="7982f-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7982f-114">Example</span></span>



| <span data-ttu-id="7982f-115">Vorher</span><span class="sxs-lookup"><span data-stu-id="7982f-115">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg) |
| <span data-ttu-id="7982f-117">Diagramm der histogrammausgabedaten</span><span class="sxs-lookup"><span data-stu-id="7982f-117">Graph of the histogram output data</span></span>                         |
| ![das Bild nach der Transformation.](images/33-histogram.png) |



 


```C++
ComPtr<ID2D1Effect> histogramEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Histogram, &histogramEffect);

histogramEffect->SetInputEffect(0, m_2DAffineTransformEffectRight.Get());
histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, D2D1_CHANNEL_SELECTOR_G);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(histogramEffect.Get());
m_d2dContext->EndDraw();

// The histogram data is only available once the effect has been 'drawn'.
int histogramBinCount;

HRESULT hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, &histogramBinCount);

float *histogramData = new float[histogramBinCount];
hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, 
                               reinterpret_cast<BYTE*>(histogramData), 
                               histogramBinCount * sizeof(float));
```



## <a name="effect-properties"></a><span data-ttu-id="7982f-119">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7982f-119">Effect properties</span></span>

<span data-ttu-id="7982f-120">Hier ist die Gleichung, um die Ausgabe zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7982f-120">Here's the equation to generate the output.</span></span>

![die Gleichung, die die Ausgabe des histogrammeffekts generieren soll.](images/histogram-formula.png)

<span data-ttu-id="7982f-122">*ich* werde zwischen 0 und der Anzahl der Behälter ausgewertet. Der Effekt generiert ein Histogramm für Pixelwerte zwischen 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="7982f-122">*i* is evaluated from 0 to the number of bins. The effect generates a histogram for pixel values between 0 and 1.</span></span> <span data-ttu-id="7982f-123">Werte, die außerhalb dieses Bereichs liegen, werden an den Bereich gebunden.</span><span class="sxs-lookup"><span data-stu-id="7982f-123">Values outside of this range are clamped to the range.</span></span> <span data-ttu-id="7982f-124">Der Bereich eines bestimmten Bucket hängt von der Anzahl der Eimer ab.</span><span class="sxs-lookup"><span data-stu-id="7982f-124">The range of a particular bucket depends on the number of buckets.</span></span> <span data-ttu-id="7982f-125">Dieser Effekt funktioniert bei geraden Bitmap-Pixeln.</span><span class="sxs-lookup"><span data-stu-id="7982f-125">This effect works on straight bitmap pixels.</span></span> <span data-ttu-id="7982f-126">Die Farbkanäle der Eingabe Bitmap werden durch den Alphakanal dividiert, um diesen Effekt zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="7982f-126">The color channels of the input bitmap are divided by the alpha channel to compute this effect.</span></span>



| <span data-ttu-id="7982f-127">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="7982f-127">Display name and index enumeration</span></span>                                             | <span data-ttu-id="7982f-128">Typ und Standardwert</span><span class="sxs-lookup"><span data-stu-id="7982f-128">Type and default value</span></span>                                                   | <span data-ttu-id="7982f-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7982f-129">Description</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7982f-130">Numbins</span><span class="sxs-lookup"><span data-stu-id="7982f-130">NumBins</span></span><br/> <span data-ttu-id="7982f-131">D2D1 \_ Histogram \_ Prop \_ NUM- \_ Behälter</span><span class="sxs-lookup"><span data-stu-id="7982f-131">D2D1\_HISTOGRAM\_PROP\_NUM\_BINS</span></span><br/>                 | <span data-ttu-id="7982f-132">UINT32</span><span class="sxs-lookup"><span data-stu-id="7982f-132">UINT32</span></span><br/> <span data-ttu-id="7982f-133">256</span><span class="sxs-lookup"><span data-stu-id="7982f-133">256</span></span><br/>                                         | <span data-ttu-id="7982f-134">Gibt die Anzahl der für das Histogramm verwendeten Container an.</span><span class="sxs-lookup"><span data-stu-id="7982f-134">Specifies the number of bins used for the histogram.</span></span> <span data-ttu-id="7982f-135">Der Bereich der Intensitätswerte, die in einem bestimmten Bucket liegen, hängt von der Anzahl der angegebenen Bucket ab.</span><span class="sxs-lookup"><span data-stu-id="7982f-135">The range of intensity values that fall into a particular bucket depend on the number of specified buckets.</span></span>                              |
| <span data-ttu-id="7982f-136">Channelselect</span><span class="sxs-lookup"><span data-stu-id="7982f-136">ChannelSelect</span></span><br/> <span data-ttu-id="7982f-137">D2D1 \_ Histogramm- \_ Prop- \_ Kanal \_ auswählen</span><span class="sxs-lookup"><span data-stu-id="7982f-137">D2D1\_HISTOGRAM\_PROP\_CHANNEL\_SELECT</span></span><br/>     | <span data-ttu-id="7982f-138">D2D1 \_ - \_ kanalselektor</span><span class="sxs-lookup"><span data-stu-id="7982f-138">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="7982f-139">D2D1 \_ - \_ kanalselektor \_ R</span><span class="sxs-lookup"><span data-stu-id="7982f-139">D2D1\_CHANNEL\_SELECTOR\_R</span></span><br/> | <span data-ttu-id="7982f-140">Gibt den Kanal an, der zum Generieren des Histogramms verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7982f-140">Specifies the channel used to generate the histogram.</span></span> <span data-ttu-id="7982f-141">Dieser Effekt hat eine einzelne Datenausgabe, die dem angegebenen Kanal entspricht.</span><span class="sxs-lookup"><span data-stu-id="7982f-141">This effect has a single data output corresponding to the specified channel.</span></span> <span data-ttu-id="7982f-142">Weitere Informationen finden Sie unter [kanalselektoren](#channel-selectors) .</span><span class="sxs-lookup"><span data-stu-id="7982f-142">See [Channel selectors](#channel-selectors) for more info.</span></span> |
| <span data-ttu-id="7982f-143">Histogrammausgabe</span><span class="sxs-lookup"><span data-stu-id="7982f-143">HistogramOutput</span></span><br/> <span data-ttu-id="7982f-144">D2D1 \_ Histogramm \_ - \_ \_ Compilerausgabe</span><span class="sxs-lookup"><span data-stu-id="7982f-144">D2D1\_HISTOGRAM\_PROP\_HISTOGRAM\_OUTPUT</span></span><br/> | <span data-ttu-id="7982f-145">Hafen\[\]</span><span class="sxs-lookup"><span data-stu-id="7982f-145">FLOAT\[\]</span></span><br/> <span data-ttu-id="7982f-146">Nur Ausgabe Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7982f-146">Output property only.</span></span><br/>                    | <span data-ttu-id="7982f-147">Das Ausgabe Array.</span><span class="sxs-lookup"><span data-stu-id="7982f-147">The output array.</span></span>                                                                                                                                                                             |



 

## <a name="channel-selectors"></a><span data-ttu-id="7982f-148">Kanalselektoren</span><span class="sxs-lookup"><span data-stu-id="7982f-148">Channel selectors</span></span>



| <span data-ttu-id="7982f-149">Enumeration</span><span class="sxs-lookup"><span data-stu-id="7982f-149">Enumeration</span></span>                | <span data-ttu-id="7982f-150">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7982f-150">Description</span></span>                                                           |
|----------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="7982f-151">D2D1 \_ - \_ kanalselektor \_ R</span><span class="sxs-lookup"><span data-stu-id="7982f-151">D2D1\_CHANNEL\_SELECTOR\_R</span></span> | <span data-ttu-id="7982f-152">Der Effekt generiert die histogrammausgabe basierend auf dem roten Kanal.</span><span class="sxs-lookup"><span data-stu-id="7982f-152">The effect generates the histogram output based on the red channel.</span></span>   |
| <span data-ttu-id="7982f-153">D2D1 \_ Kanal \_ Auswahl \_ G</span><span class="sxs-lookup"><span data-stu-id="7982f-153">D2D1\_CHANNEL\_SELECTOR\_G</span></span> | <span data-ttu-id="7982f-154">Der Effekt generiert die histogrammausgabe basierend auf dem grünen Kanal.</span><span class="sxs-lookup"><span data-stu-id="7982f-154">The effect generates the histogram output based on the green channel.</span></span> |
| <span data-ttu-id="7982f-155">D2D1 \_ - \_ kanalselektor \_ B</span><span class="sxs-lookup"><span data-stu-id="7982f-155">D2D1\_CHANNEL\_SELECTOR\_B</span></span> | <span data-ttu-id="7982f-156">Der Effekt generiert die histogrammausgabe basierend auf dem blauen Kanal.</span><span class="sxs-lookup"><span data-stu-id="7982f-156">The effect generates the histogram output based on the blue channel.</span></span>  |
| <span data-ttu-id="7982f-157">D2D1 \_ \_ kanalselektor \_ A</span><span class="sxs-lookup"><span data-stu-id="7982f-157">D2D1\_CHANNEL\_SELECTOR\_A</span></span> | <span data-ttu-id="7982f-158">Der Effekt generiert die histogrammausgabe basierend auf dem Alphakanal.</span><span class="sxs-lookup"><span data-stu-id="7982f-158">The effect generates the histogram output based on the alpha channel.</span></span> |



 

## <a name="data-output"></a><span data-ttu-id="7982f-159">Datenausgabe</span><span class="sxs-lookup"><span data-stu-id="7982f-159">Data output</span></span>

<span data-ttu-id="7982f-160">Dieser Effekt gibt einen float-Wert \[ \] mit der Anzahl der Elemente aus, die der Anzahl der angegebenen Behälter entspricht. Jedes Element in der Gleit Komma Zahl \[ \] ist ein float-Wert.</span><span class="sxs-lookup"><span data-stu-id="7982f-160">This effect outputs a FLOAT\[\], with the number of elements corresponding to the number of specified bins. Each element in the FLOAT\[\] is a float.</span></span> <span data-ttu-id="7982f-161">Der Wert des-Elements entspricht der Anzahl der Elemente in diesem bin.</span><span class="sxs-lookup"><span data-stu-id="7982f-161">The value of the element corresponds to the number of elements in that bin.</span></span>

## <a name="remarks"></a><span data-ttu-id="7982f-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7982f-162">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7982f-163">Die Methode " [**deateeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) " schlägt fehl, wenn das Gerät DirectCompute nicht unterstützt und HRESULT = D2DERR \_ unzureichende \_ Gerätefunktionen zurückgibt \_ .</span><span class="sxs-lookup"><span data-stu-id="7982f-163">The [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method fails if the device doesn't support DirectCompute and returns HRESULT = D2DERR\_INSUFFICIENT\_DEVICE\_CAPABILITIES.</span></span> <span data-ttu-id="7982f-164">Alle DirectX11 Cards und DirectX10-Karten, die DirectCompute unterstützen, können den Effekt nutzen.</span><span class="sxs-lookup"><span data-stu-id="7982f-164">All DirectX11 cards and DirectX10 cards that support DirectCompute can use the effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7982f-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7982f-165">Requirements</span></span>



| <span data-ttu-id="7982f-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7982f-166">Requirement</span></span> | <span data-ttu-id="7982f-167">Wert</span><span class="sxs-lookup"><span data-stu-id="7982f-167">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7982f-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7982f-168">Minimum supported client</span></span> | <span data-ttu-id="7982f-169">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7982f-169">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7982f-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7982f-170">Minimum supported server</span></span> | <span data-ttu-id="7982f-171">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7982f-171">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7982f-172">Header</span><span class="sxs-lookup"><span data-stu-id="7982f-172">Header</span></span>                   | <span data-ttu-id="7982f-173">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="7982f-173">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="7982f-174">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7982f-174">Library</span></span>                  | <span data-ttu-id="7982f-175">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="7982f-175">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="7982f-176">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7982f-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7982f-177">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="7982f-177">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

