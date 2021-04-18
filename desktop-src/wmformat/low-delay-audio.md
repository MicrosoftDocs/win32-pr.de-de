---
title: Low-Delay Audiodaten
description: Low-Delay Audiodaten
ms.assetid: f93819eb-f38a-45a0-aa1b-4e677e33daf8
keywords:
- Windows Media-Format-SDK, Low-Delay-Audiodaten
- Windows Media-Format-SDK, Audiounterstützung
- Codecs, Low-Delay-Audiodaten
- Codecs, Audiounterstützung
- Low-Delay-Audiodaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8cedd3a6bb54942f5a517c7133e993cf5b11cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337814"
---
# <a name="low-delay-audio"></a><span data-ttu-id="00e05-108">Low-Delay Audiodaten</span><span class="sxs-lookup"><span data-stu-id="00e05-108">Low-Delay Audio</span></span>

<span data-ttu-id="00e05-109">Das Low-Delay-Audioformat ist ein Codierungs Modus, der komprimierte Audiodaten mit einer kleineren Puffer Fenster Einstellung als andere Modi erzeugt.</span><span class="sxs-lookup"><span data-stu-id="00e05-109">Low-delay audio is an encoding mode that produces compressed audio with a smaller buffer-window setting than other modes.</span></span> <span data-ttu-id="00e05-110">Dies ist nützlich für Datenströme, die während der Wiedergabe schnell gewechselt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="00e05-110">This is useful for streams that need to be switched quickly during playback.</span></span> <span data-ttu-id="00e05-111">Das typische Szenario für dieses Feature ist eine Streamingpräsentation, die die Möglichkeit bietet, Inhalte willkürlich zu wechseln, wie z. b. das Ändern des Kanals eines Fernsehsenders.</span><span class="sxs-lookup"><span data-stu-id="00e05-111">The typical scenario for this feature is a streamed presentation that includes the ability to arbitrarily switch content, like changing the channel of a television.</span></span>

<span data-ttu-id="00e05-112">Bei Verwendung eines Audioformats mit niedriger Verzögerung wird die Latenz beim Wechseln von Inhalten im Vergleich zu anderen Audioformaten drastisch reduziert.</span><span class="sxs-lookup"><span data-stu-id="00e05-112">When you use a low-delay audio format, the latency for switching content is drastically reduced compared to other audio formats.</span></span> <span data-ttu-id="00e05-113">Die Latenzzeit wird auch bei Live Übertragungen reduziert, wenn Sie Low-Delay-Formate verwenden.</span><span class="sxs-lookup"><span data-stu-id="00e05-113">Latency is also reduced for live broadcasts when you use low-delay formats.</span></span>

<span data-ttu-id="00e05-114">Diese Funktion wird von den Windows Media Audio 9,1-und Windows Media Audio 9,1 Professional-Codecs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00e05-114">This feature is supported by the Windows Media Audio 9.1 and Windows Media Audio 9.1 Professional codecs.</span></span> <span data-ttu-id="00e05-115">Low-Delay-Formate sind nur für die Konstante Bitrate-Codierung (sowohl ein-als auch zwei-Pass-) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="00e05-115">Low-delay formats are available only for constant bit rate encoding (both one-pass and two-pass).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00e05-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00e05-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00e05-117">**Codec-Features**</span><span class="sxs-lookup"><span data-stu-id="00e05-117">**Codec Features**</span></span>](codec-features.md)
</dt> </dl>

 

 




