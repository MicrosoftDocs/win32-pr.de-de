---
description: Verfügbar machen von Erfassung und Komprimierungs Formaten
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: Verfügbar machen von Erfassung und Komprimierungs Formaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02051d9e68b3ad919b96dca53b674305787b3186
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747640"
---
# <a name="exposing-capture-and-compression-formats"></a><span data-ttu-id="fd136-103">Verfügbar machen von Erfassung und Komprimierungs Formaten</span><span class="sxs-lookup"><span data-stu-id="fd136-103">Exposing Capture and Compression Formats</span></span>

<span data-ttu-id="fd136-104">In diesem Artikel wird beschrieben, wie Sie Erfassungs-und Komprimierungs Formate mit der [**iamstreamconfig:: getstreamcaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) -Methode zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fd136-104">This article describes how to return capture and compression formats by using the [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="fd136-105">Diese Methode kann mehr Informationen über akzeptierte Medientypen als die herkömmliche Methode zum Auflisten der Medientypen einer PIN erhalten. Daher sollte Sie normalerweise stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd136-105">This method can get more information about accepted media types than the traditional way of enumerating a pin's media types, so it should typically be used instead.</span></span> <span data-ttu-id="fd136-106">**Getstreamcaps** kann Informationen zu den Arten von Formaten zurückgeben, die für Audiodaten oder Videos zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="fd136-106">**GetStreamCaps** can return information about the kinds of formats allowed for audio or video.</span></span> <span data-ttu-id="fd136-107">Darüber hinaus enthält dieser Artikel einen Beispielcode, der veranschaulicht, wie die Eingabe-PIN eines Transformations Filters erneut verbunden wird, um sicherzustellen, dass Ihr Filter eine bestimmte Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="fd136-107">Additionally, this article provides some sample code that demonstrates how to reconnect the input pin of a transform filter to ensure your filter can produce a particular output.</span></span>

<span data-ttu-id="fd136-108">Die **getstreamcaps** -Methode gibt ein Array von Paaren von Medientyp-und Funktionsstrukturen zurück.</span><span class="sxs-lookup"><span data-stu-id="fd136-108">The **GetStreamCaps** method returns an array of pairs of media type and capabilities structures.</span></span> <span data-ttu-id="fd136-109">Beim Medientyp handelt es sich um eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, und die Funktionen werden entweder durch eine [**\_ audiodatenstream- \_ Konfigurations \_**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) Ober Struktur oder eine [**\_ Textstream- \_ config \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) -Struktur dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fd136-109">The media type is an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure and the capabilities are represented either by an [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structure or a [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure.</span></span> <span data-ttu-id="fd136-110">Der erste Abschnitt dieses Artikels enthält ein Video Beispiel, und das zweite Beispiel zeigt ein Audiobeispiel.</span><span class="sxs-lookup"><span data-stu-id="fd136-110">The first section in this article presents a video example and the second presents an audio example.</span></span>

<span data-ttu-id="fd136-111">Dieser Artikel enthält folgende Themen:</span><span class="sxs-lookup"><span data-stu-id="fd136-111">This article contains the following topics:</span></span>

-   [<span data-ttu-id="fd136-112">Video Funktionen</span><span class="sxs-lookup"><span data-stu-id="fd136-112">Video Capabilities</span></span>](video-capabilities.md)
-   [<span data-ttu-id="fd136-113">Audiofunktionen</span><span class="sxs-lookup"><span data-stu-id="fd136-113">Audio Capabilities</span></span>](audio-capabilities.md)
-   [<span data-ttu-id="fd136-114">Erneutes Verbinden Ihrer Eingabe, um bestimmte Ausgabetypen sicherzustellen</span><span class="sxs-lookup"><span data-stu-id="fd136-114">Reconnecting Your Input to Ensure Specific Output Types</span></span>](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a><span data-ttu-id="fd136-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd136-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd136-116">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="fd136-116">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



