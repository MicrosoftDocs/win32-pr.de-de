---
description: Informationen zur transcode-API
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: Informationen zur transcode-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d2d49a33a97bbb538888173db78705061583ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565505"
---
# <a name="about-the-transcode-api"></a><span data-ttu-id="fda3b-103">Informationen zur transcode-API</span><span class="sxs-lookup"><span data-stu-id="fda3b-103">About the Transcode API</span></span>

<span data-ttu-id="fda3b-104">Das folgende Diagramm zeigt, wie sich die transcodieren-API auf den Rest der Media Foundation Codierungs Pipeline bezieht.</span><span class="sxs-lookup"><span data-stu-id="fda3b-104">The following diagram shows how the transcode API relates to the rest of the Media Foundation encoding pipeline.</span></span>

![ein Diagramm, das die transcodieren-API anzeigt.](images/encoding08.png)

<span data-ttu-id="fda3b-106">Die Codierungs Pipeline enthält die folgenden Datenverarbeitungs Objekte:</span><span class="sxs-lookup"><span data-stu-id="fda3b-106">The encoding pipeline contains the following data-processing objects:</span></span>

-   <span data-ttu-id="fda3b-107">Medienquelle</span><span class="sxs-lookup"><span data-stu-id="fda3b-107">Media source</span></span>
-   <span data-ttu-id="fda3b-108">Decoder</span><span class="sxs-lookup"><span data-stu-id="fda3b-108">Decoder</span></span>
-   <span data-ttu-id="fda3b-109">Video Resizer oder audioresampler</span><span class="sxs-lookup"><span data-stu-id="fda3b-109">Video resizer or audio resampler</span></span>
-   <span data-ttu-id="fda3b-110">Encoder</span><span class="sxs-lookup"><span data-stu-id="fda3b-110">Encoder</span></span>
-   <span data-ttu-id="fda3b-111">Medien Senke</span><span class="sxs-lookup"><span data-stu-id="fda3b-111">Media sink</span></span>

<span data-ttu-id="fda3b-112">Die Video Resizer ist nur erforderlich, wenn die Größe des Ausgabevideos von der Quelle abweicht.</span><span class="sxs-lookup"><span data-stu-id="fda3b-112">The video resizer is needed only if the size of the output video differs from the source.</span></span> <span data-ttu-id="fda3b-113">Der audioresampler ist nur erforderlich, wenn die Audiodatei vor der Codierung erneut erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="fda3b-113">The audio resampler is needed only if the audio needs to be resampled before encoding.</span></span> <span data-ttu-id="fda3b-114">Das Decoder-/encoderpaar ist für die Transcodierung erforderlich, aber nicht für das remuxing.</span><span class="sxs-lookup"><span data-stu-id="fda3b-114">The decoder/encoder pair is required for transcoding, but not for remuxing.</span></span>

<span data-ttu-id="fda3b-115">Bei der Codierungs *Topologie* handelt es sich um den Satz von Pipeline Objekten (Quelle, Decoder, Resizer, Resampler, Encoder und Medien Senke) sowie die Verbindungspunkte zwischen Ihnen.</span><span class="sxs-lookup"><span data-stu-id="fda3b-115">The encoding *topology* is the set of pipeline objects (source, decoder, resizer, resampler, encoder, and media sink), plus the connection points between them.</span></span> <span data-ttu-id="fda3b-116">Weitere Informationen zu Topologien finden Sie unter [Topologien](topologies.md).</span><span class="sxs-lookup"><span data-stu-id="fda3b-116">For more information about topologies, see [Topologies](topologies.md).</span></span>

<span data-ttu-id="fda3b-117">Verschiedene Komponenten sind für das Erstellen der verschiedenen Pipeline Objekte verantwortlich:</span><span class="sxs-lookup"><span data-stu-id="fda3b-117">Different components are responsible for creating the various pipeline objects:</span></span>

-   <span data-ttu-id="fda3b-118">Die Anwendung verwendet in der Regel den [quellresolver](source-resolver.md) , um die Medienquelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fda3b-118">The application typically uses the [Source Resolver](source-resolver.md) to create the media source.</span></span>
-   <span data-ttu-id="fda3b-119">Die [Medien Sitzung](media-session.md) lädt und konfiguriert den Decoder, den Video Resizer und den audioresampler.</span><span class="sxs-lookup"><span data-stu-id="fda3b-119">The [Media Session](media-session.md) loads and configures the decoder, video resizer, and audio resampler.</span></span> <span data-ttu-id="fda3b-120">Intern wird hierfür das topologielader verwendet (siehe [**imftopoloader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).</span><span class="sxs-lookup"><span data-stu-id="fda3b-120">Internally, it uses the topology loader to do this (see [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).</span></span>
-   <span data-ttu-id="fda3b-121">Die transcodieren-API lädt und konfiguriert den Encoder und die Medien Senke.</span><span class="sxs-lookup"><span data-stu-id="fda3b-121">The transcode API loads and configures the encoder and the media sink.</span></span>

<span data-ttu-id="fda3b-122">Erweiterte Anwendungen können den Encoder und die Medien Senke direkt konfigurieren, anstatt die transcodieren-API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fda3b-122">Advanced applications can configure the encoder and the media sink directly, rather than using the transcode API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fda3b-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fda3b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fda3b-124">Transcode-API</span><span class="sxs-lookup"><span data-stu-id="fda3b-124">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="fda3b-125">Verwenden der transcode-API</span><span class="sxs-lookup"><span data-stu-id="fda3b-125">Using the Transcode API</span></span>](fast-transcode-objects.md)
</dt> </dl>

 

 



