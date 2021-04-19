---
description: Sammeln von Fine-Tuning Informationen
ms.assetid: 0d9ea896-e0a9-411b-9a10-e366e3686a34
title: Sammeln von Fine-Tuning Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27d191f677acc9306202bce141ef8f6683b43c61
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346185"
---
# <a name="collecting-fine-tuning-information"></a><span data-ttu-id="a8711-103">Sammeln von Fine-Tuning Informationen</span><span class="sxs-lookup"><span data-stu-id="a8711-103">Collecting Fine-Tuning Information</span></span>

<span data-ttu-id="a8711-104">Obwohl normalerweise eine exakte Kabel Frequenz erwartet wird, können Broadcast Häufigkeiten von der Broadcast Station nach oben oder unten angepasst werden, um potenzielle Störungen durch benachbarte Kanäle zu verringern.</span><span class="sxs-lookup"><span data-stu-id="a8711-104">Although cable frequencies are generally expected to be exact, broadcast frequencies may be adjusted up or down several kHz by the broadcast station to reduce potential interference with neighboring channels.</span></span>

<span data-ttu-id="a8711-105">Wenn der TV-Tuner die Genauigkeit eines Kanals filtert, sucht er nach dem genauesten Signal.</span><span class="sxs-lookup"><span data-stu-id="a8711-105">When the TV Tuner filter tunes to a channel, it scans for the most precise signal.</span></span> <span data-ttu-id="a8711-106">Gehen Sie folgendermaßen vor, um diese Informationen für nachfolgende Optimierungs Vorgänge in der Registrierung zu speichern:</span><span class="sxs-lookup"><span data-stu-id="a8711-106">To save this information in the registry for subsequent tuning operations, do the following:</span></span>

1.  <span data-ttu-id="a8711-107">Nennen Sie [**iamtuner:: channelminmax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) , um den Bereich der Häufigkeits Einträge in der Tabelle Current Frequency zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a8711-107">Call [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) to determine the range of frequency entries in the current frequency table.</span></span>
2.  <span data-ttu-id="a8711-108">Nennen Sie die Methode [**iamtuner::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) einmal für jeden Häufigkeits Index im Bereich.</span><span class="sxs-lookup"><span data-stu-id="a8711-108">Call the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method once for each frequency index in the range.</span></span>
3.  <span data-ttu-id="a8711-109">Wenden Sie [**iamtvtuner:: storeautotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) an, um die Informationen zur Feinabstimmung in der Registrierung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a8711-109">Call [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) to save the fine-tuning information in the registry.</span></span> <span data-ttu-id="a8711-110">Die Informationen werden unter dem Registrierungsschlüssel für den aktuellen Optimierungs Bereich gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a8711-110">The information is stored under the registry key for the current tuning space.</span></span>

<span data-ttu-id="a8711-111">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="a8711-111">The following code shows these steps:</span></span>


```C++
long lMin = 0, lMax = 0;
hr = pTuner->ChannelMinMax(&lMin, &lMax);
if (SUCCEEDED(hr))
{
    for (long i = lMin; i <= lMax; i++)
    {
        pTuner->put_Channel(i, AMTUNER_SUBCHAN_DEFAULT,
            AMTUNER_SUBCHAN_DEFAULT)
    }
    pTuner->StoreAutoTune();
}
```



<span data-ttu-id="a8711-112">Bei früheren Versionen des TV-Tuner-Filters wurde die [**iamtvtuner:: Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) -Methode für die Feinabstimmung empfohlen.</span><span class="sxs-lookup"><span data-stu-id="a8711-112">With earlier versions of the TV Tuner filter, the [**IAMTVTuner::AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) method was recommended for fine-tuning.</span></span> <span data-ttu-id="a8711-113">Diese Methode ignoriert jedoch alle Häufigkeits Überschreitungen, sodass ihre Verwendung nicht mehr empfohlen wird.</span><span class="sxs-lookup"><span data-stu-id="a8711-113">However, this method ignores any frequency overrides, so its use is no longer recommended.</span></span> <span data-ttu-id="a8711-114">Der folgende Code entspricht der **Autotune** -Methode, funktioniert aber ordnungsgemäß mit Häufigkeits Überschreitungen:</span><span class="sxs-lookup"><span data-stu-id="a8711-114">The following code is equivalent to the **AutoTune** method, but works correctly with frequency overrides:</span></span>


```C++
HRESULT MyAutoTune(IAMTVTuner *pTuner, long lIndex, long *plFoundSignal)
{
    long SignalStrength = AMTUNER_NOSIGNAL;
    HRESULT hr;
    hr = pTuner->put_Channel(lIndex, AMTUNER_SUBCHAN_DEFAULT, AMTUNER_SUBCHAN_DEFAULT);
    if (NOERROR == hr)
        pTuner->SignalPresent(&SignalStrength);
    *plFoundSignal = (SignalStrength != AMTUNER_NOSIGNAL);
        return hr;
}
```



<span data-ttu-id="a8711-115">Beim Broadcast Empfang ist es nicht immer möglich, eine horizontale Sperre zu erhalten, obwohl das Bild angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a8711-115">With broadcast reception, it is not always possible to get a horizontal lock, although the picture is viewable.</span></span> <span data-ttu-id="a8711-116">In diesen Fällen erhält die Tuner-Hardware eine Häufigkeits Sperre, aber der Decoder hat keine horizontale Sperre.</span><span class="sxs-lookup"><span data-stu-id="a8711-116">In these cases, the tuner hardware will have a frequency lock, but the decoder will not have horizontal lock.</span></span> <span data-ttu-id="a8711-117">Diese Bedingung kann erkannt werden, wenn Sie " [**Put \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) " oder " [**Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) " durch Untersuchen des Rückgabecodes verwenden.</span><span class="sxs-lookup"><span data-stu-id="a8711-117">This condition can be detected when using [**put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) or [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) by examining the return code.</span></span>



| <span data-ttu-id="a8711-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a8711-118">Value</span></span>    | <span data-ttu-id="a8711-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8711-119">Description</span></span>                                                                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8711-120">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="a8711-120">S\_OK</span></span>    | <span data-ttu-id="a8711-121">Der Tune-Vorgang war erfolgreich, und der Tuner hat eine Häufigkeits Sperre erhalten.</span><span class="sxs-lookup"><span data-stu-id="a8711-121">The tune operation succeeded and the tuner got a frequency lock.</span></span>                                                                                                                          |
| <span data-ttu-id="a8711-122">S \_ false</span><span class="sxs-lookup"><span data-stu-id="a8711-122">S\_FALSE</span></span> | <span data-ttu-id="a8711-123">Während des Tune-Vorgangs sind keine Fehler aufgetreten, aber der Tuner konnte keine Häufigkeits Sperre erhalten.</span><span class="sxs-lookup"><span data-stu-id="a8711-123">There were no errors during the tune operation, but the tuner was not able to get a frequency lock.</span></span> <span data-ttu-id="a8711-124">Es ist sehr unwahrscheinlich, dass es einen sichtbaren Kanal gibt, der aus diesem Vorgang resultiert.</span><span class="sxs-lookup"><span data-stu-id="a8711-124">It is highly unlikely that there is a viewable channel resulting from this operation.</span></span> |



 

<span data-ttu-id="a8711-125">Jeder andere Rückgabecode gibt an, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a8711-125">Any other return code indicates that some error occurred.</span></span>

<span data-ttu-id="a8711-126">Der Rückgabewert S \_ OK garantiert nicht, dass der Decoder über eine horizontale Sperre verfügt.</span><span class="sxs-lookup"><span data-stu-id="a8711-126">A return value of S\_OK does not guarantee that the decoder has a horizontal lock.</span></span> <span data-ttu-id="a8711-127">Die [**Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) -Methode aktualisiert den *foundsignal* -Parameter, um anzugeben, ob eine horizontale Sperre erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="a8711-127">The [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) method updates the *FoundSignal* parameter to indicate whether or not horizontal lock was achieved.</span></span> <span data-ttu-id="a8711-128">Die [**iamtuner:: signalpresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) -Methode gibt die gleichen Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="a8711-128">The [**IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) method returns the same information.</span></span>

<span data-ttu-id="a8711-129">Wenn der Rückgabewert S OK ist, kann \_ die Anwendung jedoch den *foundsignal* -Parameter ignorieren, da der Tuner eine Häufigkeits Sperre meldet.</span><span class="sxs-lookup"><span data-stu-id="a8711-129">When the return value is S\_OK, however, the application has the option of ignoring the *FoundSignal* parameter, because the tuner is reporting a frequency lock.</span></span> <span data-ttu-id="a8711-130">Es besteht die Möglichkeit einer Häufigkeits Sperre für Rauschen. diese Möglichkeit sollte jedoch gegen die Möglichkeit abgewogen werden, sichtbare Kanäle zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="a8711-130">There is the possibility of a frequency lock on noise, but this possibility should be weighed against the possibility of skipping viewable channels.</span></span>

## <a name="registry-conversion"></a><span data-ttu-id="a8711-131">Registrierungs Konvertierung</span><span class="sxs-lookup"><span data-stu-id="a8711-131">Registry Conversion</span></span>

<span data-ttu-id="a8711-132">Zur Unterstützung von Überschreibungs Überschreitungen hat sich das interne Format des Registrierungsschlüssels, der Informationen zur Feinabstimmung enthält, geändert.</span><span class="sxs-lookup"><span data-stu-id="a8711-132">To support frequency overrides, the internal format of the registry key that holds fine-tuning information has changed.</span></span> <span data-ttu-id="a8711-133">Das ursprüngliche Format wird weiterhin aus Gründen der Abwärtskompatibilität unterstützt, unterstützt jedoch keine Häufigkeits Überschreitungen.</span><span class="sxs-lookup"><span data-stu-id="a8711-133">The original format is still supported for backward compatibility, but it does not support frequency overrides.</span></span>

<span data-ttu-id="a8711-134">Das alte Registrierungs Format wird immer dann in das neue Format konvertiert, wenn die [**iamtvtuner:: storeautotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a8711-134">The old registry format is converted to the new format whenever the [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) method is called.</span></span> <span data-ttu-id="a8711-135">Wenn Ihre Anwendung Häufigkeits Überschreitungen hinzufügt, sollte Sie die **storeautotune** -Methode zum Konvertieren in das neue Registrierungs Format abrufen.</span><span class="sxs-lookup"><span data-stu-id="a8711-135">If your application adds frequency overrides, it should call the **StoreAutoTune** method to convert to the new registry format.</span></span> <span data-ttu-id="a8711-136">Vor dem Aufruf von **storeautotune** müssen keine fein Optimierungs Informationen erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="a8711-136">It is not necessary to collect any fine-tuning information before calling **StoreAutoTune**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8711-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a8711-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8711-138">Internationale Analog-TV-Optimierung</span><span class="sxs-lookup"><span data-stu-id="a8711-138">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



