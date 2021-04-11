---
title: Audioprobennahme
description: Audioprobennahme
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- Windows Media-Format-SDK, audioresampling
- Windows Media-Format-SDK, neusampling von Audiodaten
- Advanced Systems Format (ASF), audioresampling
- ASF (Advanced Systems Format), audioresampling
- Advanced Systems Format (ASF), Resampling von Audiodaten
- ASF (Advanced Systems Format), Resampling von Audiodaten
- audioprobennahme
- Neuberechnung von Audioinformationen, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608272a7e531d7380991a705d391e6226a6758d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309987"
---
# <a name="audio-resampling"></a><span data-ttu-id="1d843-111">Audioprobennahme</span><span class="sxs-lookup"><span data-stu-id="1d843-111">Audio Resampling</span></span>

<span data-ttu-id="1d843-112">Jedes komprimierte Format eines Audiocodecs hat eine bestimmte Samplingrate und eine bestimmte Stichprobengröße.</span><span class="sxs-lookup"><span data-stu-id="1d843-112">Every compressed format of an audio codec has a specific sample rate and sample size.</span></span> <span data-ttu-id="1d843-113">Diese müssen nicht den Einstellungen des Eingabe Formats oder des Ausgabeformats entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1d843-113">These do not need to match the settings of the input format or output format.</span></span> <span data-ttu-id="1d843-114">Wenn ein Eingabeformat andere Einstellungen als das im Profil beschriebene komprimierte Format aufweist, wird das audioverfahren während des Codierungs Vorgangs vom Writer neu erstellt, um das komprimierte Format abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="1d843-114">If an input format has different settings than the compressed format described in the profile, the writer will resample the audio, during the encoding process, to match the compressed format.</span></span> <span data-ttu-id="1d843-115">Nur bestimmte Formate werden vom Writer als Eingabe akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="1d843-115">Only certain formats are accepted by the writer as input.</span></span> <span data-ttu-id="1d843-116">Wenn Sie die Eingabeformate für einen komprimierten Audiostream auflisten, können alle abgerufenen Formate neu erstellt werden, sodass Sie dem Format im Profil entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1d843-116">When you enumerate the input formats for a compressed audio stream, all of the formats retrieved can be resampled to match the format in the profile.</span></span>

<span data-ttu-id="1d843-117">Wenn Sie komprimierte Audiodaten lesen, wird der Inhalt vom Reader entsprechend dem Ausgabeformat neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="1d843-117">When reading compressed audio, the reader will resample the content to match the output format.</span></span> <span data-ttu-id="1d843-118">Sie müssen eines der Ausgabeformate verwenden, die vom Reader aufgelistet werden, damit Sie sicherstellen können, dass die Audiodaten in den Ausgabe Formateinstellungen erneut erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="1d843-118">You must use one of the output formats enumerated by the reader, so you are guaranteed that the audio can be resampled to the output format settings.</span></span>

<span data-ttu-id="1d843-119">Jede erneute Stichprobe wirkt sich potenziell auf die Audioqualität aus.</span><span class="sxs-lookup"><span data-stu-id="1d843-119">Each resampling potentially affects the quality of the audio.</span></span> <span data-ttu-id="1d843-120">Wenn möglich, sollten Sie Eingabe-und Ausgabeformate mit Einstellungen verwenden, die dem komprimierten Format entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1d843-120">When possible, you should use input and output formats with settings that match the compressed format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d843-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1d843-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d843-122">**Funktionen zum Schreiben von Dateien**</span><span class="sxs-lookup"><span data-stu-id="1d843-122">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="1d843-123">**Arbeiten mit Eingaben**</span><span class="sxs-lookup"><span data-stu-id="1d843-123">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="1d843-124">**Arbeiten mit Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="1d843-124">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




