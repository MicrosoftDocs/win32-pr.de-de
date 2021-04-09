---
title: Konfigurieren von Bildschirm Aufzeichnungsdaten strömen
description: Konfigurieren von Bildschirm Aufzeichnungsdaten strömen
ms.assetid: 974e679f-0bf6-412b-9e80-43370de7605a
keywords:
- Streams, Konfigurieren von Bildschirm Erfassungsdaten strömen
- Codecs, Konfigurieren von Bildschirm Erfassungsdaten strömen
- Bildschirmaufnahme Datenströme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8200c4a6e733c2bb7f908b79cb73dbb2c3244dc4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948410"
---
# <a name="configuring-screen-capture-streams"></a><span data-ttu-id="56ec3-106">Konfigurieren von Bildschirm Aufzeichnungsdaten strömen</span><span class="sxs-lookup"><span data-stu-id="56ec3-106">Configuring Screen Capture Streams</span></span>

<span data-ttu-id="56ec3-107">Streams, die den Windows Media® Video 9-Bildschirm Codec verwenden, werden von Anwendungen auf die gleiche Weise konfiguriert wie normale Videostreams.</span><span class="sxs-lookup"><span data-stu-id="56ec3-107">Streams that use the Windows Media® Video 9 Screen codec are configured by applications in the same way as normal video streams.</span></span> <span data-ttu-id="56ec3-108">Wenn Sie jedoch die Komplexität des Videos auf 0 festlegen, ignoriert der Writer alle Video Qualitätswerte, die mit [**iwmvideomediadie:: setquality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality)festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="56ec3-108">However, if you set the video complexity level to 0, the writer will ignore any video quality value set with [**IWMVideoMediaProps::SetQuality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality).</span></span> <span data-ttu-id="56ec3-109">Weitere Informationen finden Sie unter [erzielen von guten Ergebnissen mit dem Windows Media Video 9-Bildschirm Codec](getting-good-results-with-the-windows-media-video-9-screen-codec.md).</span><span class="sxs-lookup"><span data-stu-id="56ec3-109">For more information, see [Getting Good Results with the Windows Media Video 9 Screen Codec](getting-good-results-with-the-windows-media-video-9-screen-codec.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56ec3-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56ec3-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56ec3-111">**Konfigurieren von Streams**</span><span class="sxs-lookup"><span data-stu-id="56ec3-111">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="56ec3-112">**Allgemeine Konfiguration für alle Streams**</span><span class="sxs-lookup"><span data-stu-id="56ec3-112">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="56ec3-113">**Konfigurieren von Videostreams**</span><span class="sxs-lookup"><span data-stu-id="56ec3-113">**Configuring Video Streams**</span></span>](configuring-video-streams.md)
</dt> </dl>

 

 




