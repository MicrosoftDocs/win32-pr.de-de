---
description: Überschreibungs Überschreitungen
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: Überschreibungs Überschreitungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57177e4990cb40be271fc551718964faf1696d2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520659"
---
# <a name="frequency-overrides"></a><span data-ttu-id="b93b3-103">Überschreibungs Überschreitungen</span><span class="sxs-lookup"><span data-stu-id="b93b3-103">Frequency Overrides</span></span>

<span data-ttu-id="b93b3-104">Es wurde ein erheblicher Aufwand aufgewendet, um sicherzustellen, dass die Übertragungs Häufigkeits-und Farbstandard Zuweisungen für jedes Land/jede Region korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="b93b3-104">A significant amount of effort was spent to ensure that the broadcast frequencies and color standard assignments are correct for each country/region.</span></span> <span data-ttu-id="b93b3-105">Es gibt auch Situationen, in denen die Häufigkeits Tabellen nicht ausreichen, Fehler enthalten oder veraltet sind.</span><span class="sxs-lookup"><span data-stu-id="b93b3-105">Even so, there will be situations when the frequency tables are not sufficient, contain errors, or become obsolete.</span></span> <span data-ttu-id="b93b3-106">Um dieses Problem zu beheben, werden die Häufigkeits Tabellen der TV-Tuner-Filter möglicherweise selektiv überschrieben, indem der folgende Registrierungsschlüssel verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="b93b3-106">To address this problem, the frequencies listed in the TV Tuner filter's frequency tables may be selectively overridden, by using the following registry key:</span></span>

<span data-ttu-id="b93b3-107">**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **TV System Services** \\ **tvautotune** \\ **TS0-1**</span><span class="sxs-lookup"><span data-stu-id="b93b3-107">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**TV System Services**\\**TVAutoTune**\\**TS0-1**</span></span>

> [!Note]  
> <span data-ttu-id="b93b3-108">Ab Windows 7 wird der folgende umgeleitete Registrierungsschlüssel für x86-Anwendungen verwendet, die in x64-Versionen von Windows ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="b93b3-108">Starting in Windows 7, the following redirected registry key is used for x86 applications running on x64 versions of Windows:</span></span>

 

<span data-ttu-id="b93b3-109">**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Wow6432Node** \\ **Microsoft** \\ **TV System Services** \\ **tvautotune** \\ **TS0-1**</span><span class="sxs-lookup"><span data-stu-id="b93b3-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Wow6432Node**\\**Microsoft**\\**TV System Services**\\**TVAutoTune**\\**TS0-1**</span></span>

<span data-ttu-id="b93b3-110">Häufigkeits Überschreibungen werden in Anwendungs definierte "optimierungsbereiche" gruppiert, die nach Zahl identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="b93b3-110">Frequency overrides are grouped into application-defined "tuning spaces," which are identified by number.</span></span> <span data-ttu-id="b93b3-111">Das folgende Beispiel zeigt eine Beispiel Überschreibung:</span><span class="sxs-lookup"><span data-stu-id="b93b3-111">The following example shows an example override:</span></span>

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

<span data-ttu-id="b93b3-112">In diesem Fall weist "TS0-1" auf den Optimierungs Bereich 0 für Kabel häufigerungen hin.</span><span class="sxs-lookup"><span data-stu-id="b93b3-112">In this case, "TS0-1" indicates Tuning Space 0 for cable frequencies.</span></span> <span data-ttu-id="b93b3-113">Die erste Zahl identifiziert den Optimierungs Bereich.</span><span class="sxs-lookup"><span data-stu-id="b93b3-113">The first number identifies the tuning space.</span></span> <span data-ttu-id="b93b3-114">Die zweite Zahl ist entweder 0 für Broadcast Häufigkeiten oder 1 für Kabel Häufigkeiten.</span><span class="sxs-lookup"><span data-stu-id="b93b3-114">The second number is either 0 for broadcast frequencies or 1 for cable frequencies.</span></span>

<span data-ttu-id="b93b3-115">Der Unterschlüssel mit dem Namen "12" überschreibt den Frequency-Wert für die Häufigkeit bei Index 12 in der aktuellen Häufigkeits Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b93b3-115">The subkey named "12" overrides the frequency value for the frequency at index 12 in the current frequency table.</span></span> <span data-ttu-id="b93b3-116">Der Wert des unter Schlüssels ist ein **DWORD** -Wert, der die Häufigkeit in Hertz (Hz) angibt.</span><span class="sxs-lookup"><span data-stu-id="b93b3-116">The value of the subkey is a **DWORD** that specifies the frequency in Hertz (Hz).</span></span> <span data-ttu-id="b93b3-117">In diesem Beispiel wird die Häufigkeit auf 67,25 MHz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b93b3-117">In this example, the frequency is set to 67.25 MHz.</span></span> <span data-ttu-id="b93b3-118">Außer Kraft setzungen können für alle Kanalnummern im Bereich zwischen 1 und 999 (einschließlich) definiert werden.</span><span class="sxs-lookup"><span data-stu-id="b93b3-118">Overrides can be defined for any channel numbers in the range of 1 to 999, inclusive.</span></span> <span data-ttu-id="b93b3-119">Wenn die Optimierungs Hardware eine bestimmte Häufigkeit nicht unterstützt, tritt bei der Tune-Anforderung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="b93b3-119">If the tuning hardware does not support a given frequency, the tune request will fail.</span></span>

<span data-ttu-id="b93b3-120">Dieser Mechanismus kann auch verwendet werden, um neue Kanalnummern außerhalb des vorhandenen Bereichs in der Häufigkeits Tabelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b93b3-120">This mechanism can also be used to create new channel numbers outside the existing range in the frequency table.</span></span> <span data-ttu-id="b93b3-121">Die [**iamtuner:: channelminmax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) -Methode gibt den erweiterten Kanalbereich zurück.</span><span class="sxs-lookup"><span data-stu-id="b93b3-121">The [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) method will return the extended channel range.</span></span> <span data-ttu-id="b93b3-122">Wenn der ursprüngliche Kanalbereich z. b. 1 bis 158 lautet und eine Kanal Überschreibung von "200" zur Registrierung hinzugefügt wird, gibt die **channelminmax** -Methode 200 als maximalen Kanal zurück.</span><span class="sxs-lookup"><span data-stu-id="b93b3-122">For example, if the original channel range was 1 to 158, and a channel override of "200" is added to the registry, the **ChannelMinMax** method will return 200 as the maximum channel.</span></span> <span data-ttu-id="b93b3-123">In diesem Fall werden den Kanalnummern im Bereich von 159 bis 199 keine Frequenzen zugewiesen, sodass alle Optimierungs Anforderungen in diesem Bereich automatisch fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="b93b3-123">In this case, channel numbers in the range of 159 to 199 will have no frequencies assigned to them, so any tuning requests in that range will automatically fail.</span></span>

<span data-ttu-id="b93b3-124">Die [**iamtuner::p UT \_ tuningspace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) -Methode ermöglicht der Anwendung die Auswahl der zu verwendenden außer Kraft setzungen und der fein Optimierungs Informationen.</span><span class="sxs-lookup"><span data-stu-id="b93b3-124">The [**IAMTuner::put\_TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) method allows the application to choose which set of overrides and fine-tuning information to use.</span></span> <span data-ttu-id="b93b3-125">Der Optimierungs Bereich ist beliebig.</span><span class="sxs-lookup"><span data-stu-id="b93b3-125">Tuning space numbers are arbitrary.</span></span> <span data-ttu-id="b93b3-126">Es liegt in der Verantwortung der Anwendung, die Beziehung zwischen dem Optimierungs Bereich und der Häufigkeits Tabelle aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="b93b3-126">It is the application's responsibility to maintain the relationship between the tuning space and the frequency table.</span></span> <span data-ttu-id="b93b3-127">Der einfachste Ansatz besteht darin, den Länder-/Regionscode als Optimierungs Raum Nummer zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b93b3-127">The most straightforward approach is to use the country/region code as the tuning space number.</span></span> <span data-ttu-id="b93b3-128">Jedes Mal, wenn die Anwendung zu einem neuen Land-/Regionscode wechselt, wechselt Sie auch in denselben Optimierungs Bereich (in dieser Reihenfolge).</span><span class="sxs-lookup"><span data-stu-id="b93b3-128">Then, every time the application switches to a new country/region code, it also switches to the same tuning space (in that order).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b93b3-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b93b3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b93b3-130">Internationale Analog-TV-Optimierung</span><span class="sxs-lookup"><span data-stu-id="b93b3-130">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



