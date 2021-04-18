---
description: Optimierung des analogen Fernseh ERS
ms.assetid: f4ae76e3-0f61-4a33-8ea4-ef14a117df6a
title: Optimierung des analogen Fernseh ERS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b85d0826340b913df88cb20dc538bc85943949b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343949"
---
# <a name="analog-television-tuning"></a><span data-ttu-id="75b61-103">Optimierung des analogen Fernseh ERS</span><span class="sxs-lookup"><span data-stu-id="75b61-103">Analog Television Tuning</span></span>

<span data-ttu-id="75b61-104">Die Optimierung wird durch den TV-Tuner-Filter über die [**iamtvtuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) -Schnittstelle gesteuert.</span><span class="sxs-lookup"><span data-stu-id="75b61-104">Tuning is controlled by the TV Tuner filter, through the [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) interface.</span></span> <span data-ttu-id="75b61-105">Die iamtvtuner-Schnittstelle erbt iamtuner.</span><span class="sxs-lookup"><span data-stu-id="75b61-105">The IAMTVTuner interface inherits IAMTuner.</span></span> <span data-ttu-id="75b61-106">Um einen Zeiger auf die-Schnittstelle zu erhalten, rufen Sie die [**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) -Methode wie folgt auf:</span><span class="sxs-lookup"><span data-stu-id="75b61-106">To obtain a pointer to the interface, call the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method as follows:</span></span>


```C++
IAMTVTuner *pTuner = NULL;
hr = pBuild->FindInterface(
    &LOOK_UPSTREAM_ONLY,  // Look upstream from pCap.
    NULL,                 // No particular media type.
    pCap,                 // Pointer to the capture filter.
    IID_IAMTVTuner, (void**)&pTuner);
if (SUCCEEDED(hr))
{
    // Use pTuner ...
    pTuner->Release();
}
```



<span data-ttu-id="75b61-107">Der erste Parameter gibt an, dass Upstream aus dem Erfassungs Filter gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="75b61-107">The first parameter indicates to search upstream from the capture filter.</span></span>

<span data-ttu-id="75b61-108">Häufigkeits Tabellen</span><span class="sxs-lookup"><span data-stu-id="75b61-108">Frequency Tables</span></span>

<span data-ttu-id="75b61-109">Intern speichert der TV-Tuner-Filter eine Liste der Häufigkeits Tabellen.</span><span class="sxs-lookup"><span data-stu-id="75b61-109">Internally, the TV Tuner filter keeps a list of frequency tables.</span></span> <span data-ttu-id="75b61-110">Jede Häufigkeits Tabelle entspricht der Broadcast-oder Kabel Frequenz für ein bestimmtes Land bzw. eine bestimmte Region.</span><span class="sxs-lookup"><span data-stu-id="75b61-110">Each frequency table corresponds to the broadcast or cable frequencies for a given country/region.</span></span> <span data-ttu-id="75b61-111">Es gibt auch eine generische "Unicable"-Häufigkeits Tabelle, die verwendet wird, wenn ein Land/eine Region keinen Standardsatz von Häufigkeits Zuweisungen hat.</span><span class="sxs-lookup"><span data-stu-id="75b61-111">There is also a generic "Unicable" frequency table, which is used when a country/region does not have a standard set of frequency assignments.</span></span>

<span data-ttu-id="75b61-112">Jede Häufigkeits Tabelle enthält eine Liste von Optimierungs Frequenzen.</span><span class="sxs-lookup"><span data-stu-id="75b61-112">Each frequency table contains a list of tuning frequencies.</span></span> <span data-ttu-id="75b61-113">In einigen Ländern bzw. Regionen entsprechen die Indizes in der Tabelle direkt den channelnummern – mit anderen Worten, die Häufigkeit für Channel n ist der n-ten Eintrag in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="75b61-113">For some countries/regions, the indexes in the table correspond directly to channel numbers — in other words, the frequency for channel n is the n th entry in the table.</span></span> <span data-ttu-id="75b61-114">Für einige Länder/Regionen gibt es jedoch keine direkte Entsprechung zwischen Kanalnummern und Frequenzen.</span><span class="sxs-lookup"><span data-stu-id="75b61-114">For some countries/regions, however, there is no direct correspondence between channel numbers and frequencies.</span></span> <span data-ttu-id="75b61-115">In diesem Fall muss die Anwendung eine Liste behalten, in der Kanalnummern (in der Regel vom Benutzer ausgewählt) für Häufigkeits Tabelleneinträge zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="75b61-115">In that case, the application must keep a list that maps channel numbers (typically chosen by the user) to frequency table entries.</span></span> <span data-ttu-id="75b61-116">Beispielsweise kann der Benutzer, der als "Channel 5" angezeigt wird, in der Tabelle "Frequency" die Einstiegsnummer 12 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="75b61-116">For example, what the user sees as "channel 5" might be entry number 12 in the frequency table.</span></span>

<span data-ttu-id="75b61-117">Weitere Informationen finden Sie unter [internationale analoge TV-](international-analog-tv-tuning.md)Optimierung.</span><span class="sxs-lookup"><span data-stu-id="75b61-117">For details, see [International Analog TV Tuning](international-analog-tv-tuning.md).</span></span>

<span data-ttu-id="75b61-118">Grundlegende Optimierungs Vorgänge</span><span class="sxs-lookup"><span data-stu-id="75b61-118">Basic Tuning Operations</span></span>

<span data-ttu-id="75b61-119">Wenn der Tuner mehrere Empfangsmodi unterstützt, z. b. TV und FM Radio, wenden Sie [**iamtuner::p UT- \_ Modus**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) an, um den Modus auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="75b61-119">If the tuner supports multiple reception modes, such as television and FM radio, call [**IAMTuner::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) to select the mode.</span></span> <span data-ttu-id="75b61-120">Die [**iamtuner:: getavailablemodes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) -Methode gibt alle Modi zurück, die der Tuner unterstützt.</span><span class="sxs-lookup"><span data-stu-id="75b61-120">The [**IAMTuner::GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) method returns all of the modes that the tuner supports.</span></span> <span data-ttu-id="75b61-121">Mit dem folgenden Code wird beispielsweise überprüft, ob der TUNER FM Radio unterstützt. wenn dies der Fall ist, wechselt er in diesen Modus.</span><span class="sxs-lookup"><span data-stu-id="75b61-121">For example, the following code checks whether the tuner supports FM radio, and if so, switches to that mode.</span></span>


```C++
// Check whether the mode is supported.
long lModes = 0;
hr = m_pTuner->GetAvailableModes(&lModes);
if (SUCCEEDED(hr) && (lModes & AMTUNER_MODE_FM_RADIO))
{
    // Set the mode.
    hr = pTuner->put_Mode(AMTUNER_MODE_FM_RADIO);
}
```



<span data-ttu-id="75b61-122">Um das Land/die Region festzulegen, nennen Sie die [**iamtuner::p UT \_ CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) -Methode.</span><span class="sxs-lookup"><span data-stu-id="75b61-122">To set the country/region, call the [**IAMTuner::put\_CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) method.</span></span> <span data-ttu-id="75b61-123">Der Tuner verwendet diesen Wert, um die geeignete Häufigkeits Tabelle auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="75b61-123">The tuner uses this value to select the appropriate frequency table.</span></span> <span data-ttu-id="75b61-124">Weitere Informationen finden Sie unter [Land/Region-Zuweisungen](country-region-assignments.md) .</span><span class="sxs-lookup"><span data-stu-id="75b61-124">See [Country/Region Assignments](country-region-assignments.md) for more information.</span></span>

<span data-ttu-id="75b61-125">Um den Kanal festzulegen, wenden Sie die Methode [**iamtuner::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) an.</span><span class="sxs-lookup"><span data-stu-id="75b61-125">To set the channel, call the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method.</span></span> <span data-ttu-id="75b61-126">Das Argument für diese Methode ist keine Channelnummer, sondern ein Index in der aktuellen Häufigkeits Tabelle.</span><span class="sxs-lookup"><span data-stu-id="75b61-126">The argument to this method is actually not a channel number, but rather an index into the current frequency table.</span></span> <span data-ttu-id="75b61-127">Wie bereits beschrieben, entspricht die Indexnummer möglicherweise einer Kanalnummer.</span><span class="sxs-lookup"><span data-stu-id="75b61-127">As described previously, the index number may or may not correspond to a channel number.</span></span> <span data-ttu-id="75b61-128">Die [**iamtuner:: channelminmax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) -Methode gibt die minimalen und maximalen Indexwerte für die aktuelle Frequency-Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="75b61-128">The [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) method returns the minimum and maximum index values for the current frequency table.</span></span>

<span data-ttu-id="75b61-129">Überschreibungs Häufigkeits Einträge</span><span class="sxs-lookup"><span data-stu-id="75b61-129">Overriding Frequency Entries</span></span>

<span data-ttu-id="75b61-130">Möglicherweise sind einige Einträge in den Häufigkeits Tabellen falsch oder veraltet.</span><span class="sxs-lookup"><span data-stu-id="75b61-130">It is possible that some entries in the frequency tables might be incorrect or become obsolete.</span></span> <span data-ttu-id="75b61-131">Daher wird ein Mechanismus zum Überschreiben einzelner Einträge mithilfe von Registrierungs Schlüsseln bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="75b61-131">Therefore, a mechanism is provided for overriding individual entries using registry keys.</span></span>

<span data-ttu-id="75b61-132">Einzelheiten hierzu finden Sie im Thema [internationale analoge TV-](international-analog-tv-tuning.md)Optimierung.</span><span class="sxs-lookup"><span data-stu-id="75b61-132">The specifics are explained in the topic [International Analog TV Tuning](international-analog-tv-tuning.md).</span></span> <span data-ttu-id="75b61-133">Jeder Registrierungsschlüssel definiert einen "Optimierungs Bereich", der einen oder mehrere Unterschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="75b61-133">Each registry key defines a "tuning space" which contains one or more subkeys.</span></span> <span data-ttu-id="75b61-134">Jeder Unterschlüssel überschreibt einen Häufigkeits Eintrag.</span><span class="sxs-lookup"><span data-stu-id="75b61-134">Each subkey overrides one frequency entry.</span></span> <span data-ttu-id="75b61-135">Um den aktuellen Optimierungs Bereich festzulegen, verwenden Sie die [**iamtuner::p UT \_ tuningspace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) -Methode.</span><span class="sxs-lookup"><span data-stu-id="75b61-135">To set the current tuning space, use the [**IAMTuner::put\_TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) method.</span></span> <span data-ttu-id="75b61-136">Wenn Sie den Optimierungs Bereich aktivieren, werden die Häufigkeits Einträge in der Tabelle Current Frequency überschrieben.</span><span class="sxs-lookup"><span data-stu-id="75b61-136">Activating the tuning space overrides the frequency entries in the current frequency table.</span></span> <span data-ttu-id="75b61-137">Daher besteht die Anwendung darin, eine Entsprechung zwischen den Optimierungs Bereichen und Ländern bzw. Regionen beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="75b61-137">Therefore, it is up to the application to maintain a correspondence between tuning spaces and countries/regions.</span></span> <span data-ttu-id="75b61-138">Die beste Vorgehensweise besteht darin, den Land-/Regionsbezeichner als Namen für den Optimierungs Bereich zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="75b61-138">The best approach is simply to use the country/region identifier as the name of the tuning space.</span></span>

<span data-ttu-id="75b61-139">Optimieren der Häufigkeits Einträge</span><span class="sxs-lookup"><span data-stu-id="75b61-139">Fine Tuning the Frequency Entries</span></span>

<span data-ttu-id="75b61-140">Übertragungs Häufigkeiten können von der Broadcast Station mehrere kHz nach oben oder unten angepasst werden, um potenzielle Störungen durch benachbarte Kanäle zu verringern.</span><span class="sxs-lookup"><span data-stu-id="75b61-140">Broadcast frequencies may be adjusted up or down several kHz by the broadcast station to reduce potential interference with neighboring channels.</span></span> <span data-ttu-id="75b61-141">Aufgrund der nominalen Häufigkeit kann die Tuner-Karte die genaue Häufigkeit überprüfen.</span><span class="sxs-lookup"><span data-stu-id="75b61-141">Given the nominal frequency, the tuner card can scan for the exact frequency.</span></span> <span data-ttu-id="75b61-142">Der TV-Tuner-Filter verfügt über einen Mechanismus zum Speichern der angepassten Frequenzen in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="75b61-142">The TV Tuner filter has a mechanism for saving the adjusted frequencies in the registry.</span></span>

<span data-ttu-id="75b61-143">Für jeden Eintrag in der Frequency-Tabelle wird die Put \_ Channel-Methode aufgerufen, um diese Häufigkeit zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="75b61-143">For each entry in the frequency table, call the put\_Channel method to tune to that frequency.</span></span> <span data-ttu-id="75b61-144">Der Tuner scannt die präzisere Häufigkeit.</span><span class="sxs-lookup"><span data-stu-id="75b61-144">The tuner will scan for the most precise frequency.</span></span> <span data-ttu-id="75b61-145">Sie können überprüfen, ob der Tuner durch Aufrufen von [**iamtuner:: signalpresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent)eine horizontale Sperre erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="75b61-145">You can check whether the tuner achieved a horizontal lock by calling [**IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent).</span></span> <span data-ttu-id="75b61-146">Der TV-Tuner-Filter speichert das Ergebnis auch intern.</span><span class="sxs-lookup"><span data-stu-id="75b61-146">The TV Tuner filter also stores the result internally.</span></span>

<span data-ttu-id="75b61-147">Nachdem Sie alle Frequenzen überprüft haben, wenden Sie die [**iamtvtuner:: storeautotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) -Methode an, um die aktualisierten Werte in die Registrierung zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="75b61-147">After scanning all of the frequencies, call the [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) method to write the updated values into the registry.</span></span> <span data-ttu-id="75b61-148">Die aktualisierten Werte werden unter dem Registrierungs Eintrag für den aktuellen Optimierungs Bereich gespeichert.</span><span class="sxs-lookup"><span data-stu-id="75b61-148">The updated values are stored under the registry entry for the current tuning space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75b61-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="75b61-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75b61-150">Analog Fernsehen</span><span class="sxs-lookup"><span data-stu-id="75b61-150">Analog Television</span></span>](analog-television.md)
</dt> </dl>

 

 



