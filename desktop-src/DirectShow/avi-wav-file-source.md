---
description: AVI/WAV-Datei Quelle
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: AVI/WAV-Datei Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef659d880ef570176f94ac91875291ea9d200cf5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344336"
---
# <a name="aviwav-file-source"></a><span data-ttu-id="7416d-103">AVI/WAV-Datei Quelle</span><span class="sxs-lookup"><span data-stu-id="7416d-103">AVI/WAV File Source</span></span>

<span data-ttu-id="7416d-104">(Veraltet.</span><span class="sxs-lookup"><span data-stu-id="7416d-104">(Deprecated.</span></span> <span data-ttu-id="7416d-105">Verwenden Sie für AVI-und WAV-Dateien die [Datei Quelle (Async)](file-source--async--filter.md) und den [avi-Splitter](avi-splitter-filter.md) -oder [Wave-Parser](wave-parser-filter.md).)</span><span class="sxs-lookup"><span data-stu-id="7416d-105">For AVI and WAV files, use the [File Source (Async)](file-source--async--filter.md) and the [AVI Splitter](avi-splitter-filter.md) or [WAVE Parser](wave-parser-filter.md).)</span></span>

<span data-ttu-id="7416d-106">Der Quell Filter der AVI/WAV-Datei liest AVI-und WAV-Quelldateien und generiert die entsprechenden Ausgabe Pins für den Dateityp.</span><span class="sxs-lookup"><span data-stu-id="7416d-106">The AVI/WAV File Source filter reads AVI and WAV source files and generates the appropriate output pins for the file type.</span></span>

<span data-ttu-id="7416d-107">Bei WAV-Dateien erstellt der Filter eine audioausgabepin, die einen Audiostream erzeugt, der mit einem audiorenderingfilter oder einem Beteiligten audiotransformier Filter verbunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="7416d-107">For WAV files, the filter creates an audio output pin, which produces an audio stream that can be connected to an audio rendering filter or intervening audio transform filter.</span></span>

<span data-ttu-id="7416d-108">Für AVI-Dateien erstellt der Filter eine Videoausgabe-PIN, die einen komprimierten AVI-Stream erzeugt, der für den AVI-Codec-Filter geeignet ist, sowie eine audioausgabepin, die einen Audiostream erzeugt, der für einen audiorenderingfilter oder einen dazwischen liegenden audiotransformier</span><span class="sxs-lookup"><span data-stu-id="7416d-108">For AVI files, the filter creates a video output pin, which produces a compressed AVI stream suitable for the AVI codec filter, and an audio output pin, which produces an audio stream suitable for an audio rendering filter or an intervening audio transform filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7416d-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7416d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7416d-110">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="7416d-110">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



