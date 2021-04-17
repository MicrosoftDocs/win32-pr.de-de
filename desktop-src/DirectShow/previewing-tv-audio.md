---
description: Vorschau der TV-Audiodatei
ms.assetid: 25da8bcc-51c1-49f0-b4b5-885ff4f254d8
title: Vorschau der TV-Audiodatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cc63583c946d47ed744eacd51f0939ec852d53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481483"
---
# <a name="previewing-tv-audio"></a><span data-ttu-id="4b3cc-103">Vorschau der TV-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="4b3cc-103">Previewing TV Audio</span></span>

<span data-ttu-id="4b3cc-104">Zum Anzeigen einer Vorschau der TV-Audiodaten leiten Sie die Audiodecoder-PIN auf dem Querbalken Filter an die audiotuner-Pin weiter.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-104">To preview TV audio, route the Audio Decoder pin on the crossbar filter to the Audio Tuner pin.</span></span> <span data-ttu-id="4b3cc-105">Zum stumm schalten der Audiodatei leiten Sie die PIN des Audiodecoders an-1 weiter, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-105">To mute the audio, route the Audio Decoder pin to -1, as shown in the following diagram.</span></span> <span data-ttu-id="4b3cc-106">(Crossbar-Filter werden in [Arbeiten mit Kreuz leisten](working-with-crossbars.md)beschrieben.)</span><span class="sxs-lookup"><span data-stu-id="4b3cc-106">(Crossbar filters are described in [Working with Crossbars](working-with-crossbars.md).)</span></span>

![Routing der Audiodecoder-PIN](images/vidcap07.png)

<span data-ttu-id="4b3cc-108">Die grundlegende Vorgehensweise sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="4b3cc-108">The basic approach is as follows:</span></span>

1.  <span data-ttu-id="4b3cc-109">Verwenden Sie die [**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) -Methode, um den Querbalken Filter zu suchen.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-109">Use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to locate the crossbar filter.</span></span>
2.  <span data-ttu-id="4b3cc-110">Verwenden Sie die [**iamcrossbar:: get \_ crossbarpininfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) -Methode, um die Eingabe-und Ausgabe Pins des quer Zieh Filters aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-110">Use the [**IAMCrossbar::get\_CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) method to enumerate the crossbar filter's input and output pins.</span></span> <span data-ttu-id="4b3cc-111">Suchen Sie nach einem Audiodecoder-Ausgabepin und einer audiotuner-Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-111">Search for an audio decoder output pin and an audio tuner input pin.</span></span>
3.  <span data-ttu-id="4b3cc-112">Wenn Sie die richtigen Pins gefunden haben, können Sie [**iamcrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) zum Weiterleiten der Pins anrufen.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-112">If you find the correct pins, call [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) to route the pins.</span></span> <span data-ttu-id="4b3cc-113">Wenn dies nicht der Grund ist, überprüfen Sie Upstream nach einer anderen quer Leiste, und wiederholen</span><span class="sxs-lookup"><span data-stu-id="4b3cc-113">If not, look upstream for another crossbar and repeat the process.</span></span>
4.  <span data-ttu-id="4b3cc-114">Zum stumm schalten der Audiodatei leiten Sie die PIN des Audiodecoders an-1 weiter.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-114">To mute the audio, route the audio decoder pin to -1.</span></span>

<span data-ttu-id="4b3cc-115">Die meisten TV-Tuner verwenden einen einzelnen Querbalken Filter, einige verwenden jedoch zwei Kreuz leisten Filter.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-115">Most TV tuners use a single crossbar filter, but some use two crossbar filters.</span></span> <span data-ttu-id="4b3cc-116">Daher müssen Sie möglicherweise nach einer zweiten quer Leiste suchen, wenn der erste Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-116">Therefore, you might have to search for a second crossbar if the first one fails.</span></span>

> [!Note]  
> <span data-ttu-id="4b3cc-117">Im Gegensatz zu dem, was Sie möglicherweise erwartet haben, ist kein audioerfassungs Filter oder audiorenderer erforderlich, um eine Vorschau der Audiodatei anzuzeigen, da zwischen der gatewaykarte und der Soundkarte eine physische Verbindung besteht.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-117">Contrary to what you might expect, no audio capture filter or audio renderer is required to preview the audio, because there is a physical connection between the tuner card and the sound card.</span></span>

 

<span data-ttu-id="4b3cc-118">Der folgende Code zeigt diese Schritte ausführlicher.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-118">The following code shows these steps in more detail.</span></span> <span data-ttu-id="4b3cc-119">Im folgenden finden Sie eine Hilfsfunktion, die einen Querbalken Filter nach einem angegebenen Pin-Typ durchsucht:</span><span class="sxs-lookup"><span data-stu-id="4b3cc-119">First, here is a helper function that searches a crossbar filter for a specified pin type:</span></span>


```C++
HRESULT FindCrossbarPin(
    IAMCrossbar *pXBar,                 // Pointer to the crossbar.
    PhysicalConnectorType PhysicalType, // Pin type to match.
    PIN_DIRECTION Dir,                  // Pin direction.
    long *pIndex)       // Receives the index of the pin, if found.
{
    BOOL bInput = (Dir == PINDIR_INPUT ? TRUE : FALSE);

    // Find out how many pins the crossbar has.
    long cOut, cIn;
    HRESULT hr = pXBar->get_PinCounts(&cOut, &cIn);
    if (FAILED(hr)) return hr;
    // Enumerate pins and look for a matching pin.
    long count = (bInput ? cIn : cOut);
    for (long i = 0; i < count; i++)
    {
        long iRelated = 0;
        long ThisPhysicalType = 0;
        hr = pXBar->get_CrossbarPinInfo(bInput, i, &iRelated,
            &ThisPhysicalType);
        if (SUCCEEDED(hr) && ThisPhysicalType == PhysicalType)
        {
            // Found a match, return the index.
            *pIndex = i;
            return S_OK;
        }
    }
    // Did not find a matching pin.
    return E_FAIL;
}
```



<span data-ttu-id="4b3cc-120">Die Next-Funktion versucht, die Audiodatei zu aktivieren oder zu stumm schalten, abhängig vom Wert des *bactivate* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-120">The next function attempts to activate or mute the audio, depending on the value of the *bActivate* parameter.</span></span> <span data-ttu-id="4b3cc-121">Es durchsucht den angegebenen Querbalken Filter nach den erforderlichen Pins.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-121">It searches the specified crossbar filter for the required pins.</span></span> <span data-ttu-id="4b3cc-122">Wenn Sie nicht gefunden werden kann, wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-122">If it cannot find them, it returns an error code.</span></span>


```C++
HRESULT ConnectAudio(IAMCrossbar *pXBar, BOOL bActivate)
{
    // Look for the Audio Decoder output pin.
    long i = 0;
    HRESULT hr = FindCrossbarPin(pXBar, PhysConn_Audio_AudioDecoder,
        PINDIR_OUTPUT, &i);
    if (SUCCEEDED(hr))
    {
        if (bActivate)  // Activate the audio. 
        {
            // Look for the Audio Tuner input pin.
            long j = 0;
            hr = FindCrossbarPin(pXBar, PhysConn_Audio_Tuner, 
                PINDIR_INPUT, &j);
            if (SUCCEEDED(hr))
            {
                return pXBar->Route(i, j);
            }
        }
        else  // Mute the audio
        {
            return pXBar->Route(i, -1);
        }
    }
    return E_FAIL;
}
```



<span data-ttu-id="4b3cc-123">Die Next-Funktion durchsucht das Filter Diagramm nach einem Querbalken Filter.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-123">The next function searches the filter graph for a crossbar filter.</span></span> <span data-ttu-id="4b3cc-124">Wenn ein solcher gefunden wird, versucht er, das Audiogerät zu aktivieren oder zu stumm schalten (mit der vorherigen Funktion).</span><span class="sxs-lookup"><span data-stu-id="4b3cc-124">If it finds one, it attempts to activate or mute the audio (using the previous function).</span></span> <span data-ttu-id="4b3cc-125">Wenn bei diesem Vorgang ein Fehler auftritt, durchsucht die Methode Upstream nach einer zweiten quer Leiste und versucht es erneut.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-125">If that operation fails, the method searches upstream for a second crossbar and tries again.</span></span> <span data-ttu-id="4b3cc-126">Eine allgemeinere Methode zum Verwalten mehrerer Crossbar-Filter in einem Diagramm finden Sie in der ccrossbar-Klasse in der amcap-Beispielanwendung.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-126">For a more generalized approach to managing multiple crossbar filters in a graph, see the CCrossbar class in the AmCap sample application.</span></span>


```C++
HRESULT ActivateAudio(ICaptureGraphBuilder2 *pBuild, IBaseFilter *pSrc,
  BOOL bActivate)
{
    // Search upstream for a crossbar.
    IAMCrossbar *pXBar1 = NULL;
    HRESULT hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
    if (SUCCEEDED(hr)) 
    {
        hr = ConnectAudio(pXBar1, bActivate);
        if (FAILED(hr))
        {
            // Look for another crossbar.
            IBaseFilter *pF = NULL;
            hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pF);
            if (SUCCEEDED(hr)) 
            {
                // Search upstream for another one.
                IAMCrossbar *pXBar2 = NULL;
                hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pF,
                    IID_IAMCrossbar, (void**)&pXBar2);
                pF->Release();
                if (SUCCEEDED(hr))
                {
                    hr = ConnectAudio(pXBar2, bActivate);
                    pXBar2->Release();
                }
            }
        }
        pXBar1->Release();
    }
    return hr;
}
```



<span data-ttu-id="4b3cc-127">Der folgende Code zeigt, wie diese Funktionen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="4b3cc-127">The following code shows how to call these functions:</span></span>


```C++
// Build the analog TV graph (not shown).
// Activate the audio.
hr = ActivateAudio(pBuild, pCap, TRUE);
// Later, mute the audio.
hr = ActivateAudio(pBuild, pCap, FALSE);
```



<span data-ttu-id="4b3cc-128">Beachten Sie, dass diese Beispiel Funktionen viele der gleichen Funktionsaufrufe wiederholen.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-128">Note that these example functions repeat many of the same function calls.</span></span> <span data-ttu-id="4b3cc-129">Sie zählen z. b. jedes Mal die Crossbar-Pins.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-129">For example, they enumerate the crossbar pins each time.</span></span> <span data-ttu-id="4b3cc-130">In einer echten Anwendung können Sie einige dieser Informationen zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-130">In a real application, you might cache some of this information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b3cc-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b3cc-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b3cc-132">Analog zum Fernsehgerät</span><span class="sxs-lookup"><span data-stu-id="4b3cc-132">Analog Television Audio</span></span>](analog-television-audio.md)
</dt> <dt>

[<span data-ttu-id="4b3cc-133">Arbeiten mit quer leisten</span><span class="sxs-lookup"><span data-stu-id="4b3cc-133">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



