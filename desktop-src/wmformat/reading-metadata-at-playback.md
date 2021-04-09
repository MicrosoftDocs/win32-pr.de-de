---
title: Lesen von Metadaten bei der Wiedergabe
description: Lesen von Metadaten bei der Wiedergabe
ms.assetid: 48d37a9e-5e22-4298-abc4-b69998906dcb
keywords:
- Windows Media-Format-SDK, Lesen von Metadaten
- SDK für den Windows Media-Format, asynchrone Leser
- SDK für den Windows Media-Format, synchrone Reader
- Advanced Systems Format (ASF), Lesen von Metadaten
- ASF (Advanced Systems Format), Lesen von Metadaten
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- asynchrone Leser, Lesen von Metadaten
- synchrone Leser, Lesen von Metadaten
- Metadaten, lesen bei der Wiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a2515dd62092d02a45b0261fe2b501e0833a31
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038672"
---
# <a name="reading-metadata-at-playback"></a><span data-ttu-id="ffa92-115">Lesen von Metadaten bei der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="ffa92-115">Reading Metadata at Playback</span></span>

<span data-ttu-id="ffa92-116">Sowohl das asynchrone Reader-Objekt als auch das synchrone Reader-Objekt können die Metadaten aus dem Header einer geladenen ASF-Datei lesen.</span><span class="sxs-lookup"><span data-stu-id="ffa92-116">Both the asynchronous reader object and the synchronous reader object can read the metadata from the header of a loaded ASF file.</span></span> <span data-ttu-id="ffa92-117">Beim Lesen von Dateien sind alle Metadatenattribute schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ffa92-117">When reading files, the metadata attributes are all read-only.</span></span> <span data-ttu-id="ffa92-118">Beide Reader-Objekte können für die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -und die [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) -Schnittstelle abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="ffa92-118">Both reader objects can be queried for the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) and [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) interfaces.</span></span>

<span data-ttu-id="ffa92-119">Weitere Informationen zum Zugreifen auf Metadaten finden Sie unter [Arbeiten mit Metadaten](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="ffa92-119">For more information about accessing metadata, see [Working with Metadata](working-with-metadata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffa92-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ffa92-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffa92-121">**Lesen von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="ffa92-121">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




