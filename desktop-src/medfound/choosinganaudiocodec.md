---
description: Auswählen eines Audiocodecs
ms.assetid: 37f3582c-c718-42ae-b887-d7d31ee853e9
title: Auswählen eines Audiocodecs (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b16dc0c6e65356f7d7e74b85b0671c2b41369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214340"
---
# <a name="choosing-an-audio-codec-microsoft-media-foundation"></a><span data-ttu-id="89285-103">Auswählen eines Audiocodecs (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="89285-103">Choosing an Audio Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="89285-104">Der [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md) bietet drei Kategorien von Audiocodierung, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="89285-104">The [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md) provides three categories of audio encoding as shown in the following table.</span></span>



| <span data-ttu-id="89285-105">Category</span><span class="sxs-lookup"><span data-stu-id="89285-105">Category</span></span>                         | <span data-ttu-id="89285-106">Zweck</span><span class="sxs-lookup"><span data-stu-id="89285-106">Purpose</span></span>                                                    |
|----------------------------------|------------------------------------------------------------|
| <span data-ttu-id="89285-107">Standard Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="89285-107">Windows Media Audio Standard</span></span>     | <span data-ttu-id="89285-108">Allgemeine Komprimierung von Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="89285-108">General-purpose compression of audio.</span></span>                      |
| <span data-ttu-id="89285-109">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="89285-109">Windows Media Audio Professional</span></span> | <span data-ttu-id="89285-110">Komprimieren von Multi-Channel-und High-Definition-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="89285-110">Compressing multi-channel and high-definition audio.</span></span>       |
| <span data-ttu-id="89285-111">Verlust von Windows Media Audio Verlust</span><span class="sxs-lookup"><span data-stu-id="89285-111">Windows Media Audio Lossless</span></span>     | <span data-ttu-id="89285-112">Komprimieren von Audiodaten, ohne dass die ursprünglichen Daten verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="89285-112">Compressing audio without losing any of the original data.</span></span> |



 

<span data-ttu-id="89285-113">Die Kategorie Standard bietet allgemeine Audiocodierung, die für eine Vielzahl von Wiedergabe Szenarios geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="89285-113">The Standard category provides general-purpose audio encoding suitable for a variety of playback scenarios.</span></span> <span data-ttu-id="89285-114">Beispielsweise kann die Audiogeschwindigkeit in eine niedrige Bitrate für das Streaming über ein Netzwerk mit eingeschränkter Bandbreite oder für das Rendern auf tragbaren Geräten komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="89285-114">For example, it can compress audio to a low bit rate for streaming over a network with limited bandwidth, or for rendering on portable devices.</span></span> <span data-ttu-id="89285-115">Am anderen Ende der Skala können komprimierte Audioinhalte für die Wiedergabe mit hoher Qualität erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="89285-115">On the other end of the scale, it can produce compressed audio content for high-quality playback.</span></span> <span data-ttu-id="89285-116">Der Schwerpunkt der Standard Codierungs Algorithmen liegt auf Musik, Sie sind jedoch auch für andere komplexe Audioinhalte geeignet.</span><span class="sxs-lookup"><span data-stu-id="89285-116">The emphasis of the Standard encoding algorithms is on music, but they are suitable for other complex audio content as well.</span></span> <span data-ttu-id="89285-117">Die Standard Kategorie sollte der Standardwert für Audioinhalte sein.</span><span class="sxs-lookup"><span data-stu-id="89285-117">The Standard category should be your default for audio content.</span></span> <span data-ttu-id="89285-118">Die Kategorien "Professional" und "Lossless" sollten verwendet werden, um bestimmte Anforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="89285-118">The Professional and Lossless categories should be used to meet specific needs.</span></span>

<span data-ttu-id="89285-119">Ein separater Encoder, der [**Windows Media Voice Encoder**](windowsmediaaudiovoiceencoder.md), bietet eine Komprimierung der Sprache.</span><span class="sxs-lookup"><span data-stu-id="89285-119">A separate encoder, the [**Windows Media Voice Encoder**](windowsmediaaudiovoiceencoder.md), provides compression of speech.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89285-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="89285-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89285-121">Arbeiten mit Audiodaten</span><span class="sxs-lookup"><span data-stu-id="89285-121">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



