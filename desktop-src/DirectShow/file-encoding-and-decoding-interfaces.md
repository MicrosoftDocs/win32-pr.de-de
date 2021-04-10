---
description: Datei Codierung und Decodierungs Schnittstellen
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Datei Codierung und Decodierungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73de2304f2b473a634127755ca900b99592ed63
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125594"
---
# <a name="file-encoding-and-decoding-interfaces"></a><span data-ttu-id="ea085-103">Datei Codierung und Decodierungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ea085-103">File Encoding and Decoding Interfaces</span></span>

<span data-ttu-id="ea085-104">Diese Schnittstellen unterstützen Datei Codierung und Decodierung.</span><span class="sxs-lookup"><span data-stu-id="ea085-104">These interfaces support file encoding and decoding.</span></span>



| <span data-ttu-id="ea085-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ea085-105">Interface</span></span>                                                    | <span data-ttu-id="ea085-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea085-106">Description</span></span>                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea085-107">**Iammediacontent**</span><span class="sxs-lookup"><span data-stu-id="ea085-107">**IAMMediaContent**</span></span>](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | <span data-ttu-id="ea085-108">Abrufen von Metadaten aus einem Stream, z. b. Autor und Titel.</span><span class="sxs-lookup"><span data-stu-id="ea085-108">Retrieve meta-data from a stream, such as the author and title.</span></span>                                              |
| [<span data-ttu-id="ea085-109">**Iamopenprogress**</span><span class="sxs-lookup"><span data-stu-id="ea085-109">**IAMOpenProgress**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | <span data-ttu-id="ea085-110">Legen Sie den Fortschritt eines Datei Öffnungs Vorgangs fest.</span><span class="sxs-lookup"><span data-stu-id="ea085-110">Determine the progress of a file-open operation.</span></span>                                                             |
| [<span data-ttu-id="ea085-111">**Iamanalysieren**</span><span class="sxs-lookup"><span data-stu-id="ea085-111">**IAMParse**</span></span>](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | <span data-ttu-id="ea085-112">Fragen Sie die Analysezeit für die aktuelle Position in einem MPEG-Stream ab, und legen Sie Sie fest.</span><span class="sxs-lookup"><span data-stu-id="ea085-112">Query and set the parse time for the current position in an MPEG stream.</span></span>                                     |
| [<span data-ttu-id="ea085-113">**Iamstreamselect**</span><span class="sxs-lookup"><span data-stu-id="ea085-113">**IAMStreamSelect**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | <span data-ttu-id="ea085-114">Steuern Sie, welche logischen Streams abgespielt werden, und rufen Sie Informationen zu diesen Datenströmen ab.</span><span class="sxs-lookup"><span data-stu-id="ea085-114">Control which logical streams are played, and retrieve information about them.</span></span>                               |
| [<span data-ttu-id="ea085-115">**Iamvfwcompressdialogfelder**</span><span class="sxs-lookup"><span data-stu-id="ea085-115">**IAMVfwCompressDialogs**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | <span data-ttu-id="ea085-116">Dialogfelder anzeigen, die von VFW-Codecs bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ea085-116">Display dialog boxes provided by VFW codecs.</span></span>                                                                 |
| [<span data-ttu-id="ea085-117">**IAMVideoCompression**</span><span class="sxs-lookup"><span data-stu-id="ea085-117">**IAMVideoCompression**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | <span data-ttu-id="ea085-118">Legen Sie Video Komprimierungs Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="ea085-118">Set video compression parameters.</span></span>                                                                            |
| [<span data-ttu-id="ea085-119">**Iconfigasfwriter**</span><span class="sxs-lookup"><span data-stu-id="ea085-119">**IConfigAsfWriter**</span></span>](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | <span data-ttu-id="ea085-120">Steuern der Art und Weise, wie der [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter Dateien des erweiterten Systems formatiert</span><span class="sxs-lookup"><span data-stu-id="ea085-120">Control how the [WM ASF Writer](wm-asf-writer-filter.md) filter writes Advanced Systems Format (ASF) files.</span></span> |
| [<span data-ttu-id="ea085-121">**Iconfigavimux**</span><span class="sxs-lookup"><span data-stu-id="ea085-121">**IConfigAviMux**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | <span data-ttu-id="ea085-122">Steuern Sie, wie der [AVI MUX](avi-mux-filter.md) -Filter AVI-Dateien schreibt.</span><span class="sxs-lookup"><span data-stu-id="ea085-122">Control how the [AVI Mux](avi-mux-filter.md) filter writes AVI files.</span></span>                                       |
| [<span data-ttu-id="ea085-123">**Iconfiginterleaving**</span><span class="sxs-lookup"><span data-stu-id="ea085-123">**IConfigInterleaving**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | <span data-ttu-id="ea085-124">Konfigurieren Sie die über Lapp Zeit, wenn der AVI MUX-Filter AVI-Dateien schreibt.</span><span class="sxs-lookup"><span data-stu-id="ea085-124">Configure interleaving when the AVI Mux filter writes AVI files.</span></span>                                             |
| [<span data-ttu-id="ea085-125">**Idvenc**</span><span class="sxs-lookup"><span data-stu-id="ea085-125">**IDVEnc**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | <span data-ttu-id="ea085-126">Legen Sie die Codierungs Auflösung für den [DV-Video Encoder](dv-video-encoder-filter.md) -Filter fest.</span><span class="sxs-lookup"><span data-stu-id="ea085-126">Set the encoding resolution on the [DV Video Encoder](dv-video-encoder-filter.md) filter.</span></span>                   |
| [<span data-ttu-id="ea085-127">**Idvsplitter**</span><span class="sxs-lookup"><span data-stu-id="ea085-127">**IDVSplitter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | <span data-ttu-id="ea085-128">Herabstufen der Framerate für einen Datenstrom im digitalen Video (DV)</span><span class="sxs-lookup"><span data-stu-id="ea085-128">Downgrade the frame rate on a digital video (DV) stream</span></span>                                                      |
| [<span data-ttu-id="ea085-129">**Iipdvdec**</span><span class="sxs-lookup"><span data-stu-id="ea085-129">**IIPDVDec**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | <span data-ttu-id="ea085-130">Legen Sie die Decodierungs Auflösung für den [DV-Video Decoder](dv-video-decoder-filter.md) Filter fest.</span><span class="sxs-lookup"><span data-stu-id="ea085-130">Set the decoding resolution on the [DV Video Decoder](dv-video-decoder-filter.md) filter.</span></span>                   |
| [<span data-ttu-id="ea085-131">**Ipersistmediapropertybag**</span><span class="sxs-lookup"><span data-stu-id="ea085-131">**IPersistMediaPropertyBag**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | <span data-ttu-id="ea085-132">Festlegen und Abrufen von Informations-und DISP-Blöcken in AVI-Streams.</span><span class="sxs-lookup"><span data-stu-id="ea085-132">Set and retrieve INFO and DISP chunks in AVI streams.</span></span>                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="ea085-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ea085-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea085-134">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ea085-134">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 



