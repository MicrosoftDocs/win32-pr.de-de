---
title: Bandbreiten Freigabe
description: Bandbreiten Freigabe
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- Windows Media-Format-SDK, Bandbreiten Freigabe
- Advanced Systems Format (ASF), Bandbreiten Freigabe
- ASF (Advanced Systems Format), Bandbreiten Freigabe
- Windows Media-Format-SDK, Streams
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- Bandbreiten Freigabe, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2221d2fbc44654af7f12acf6e45fb85ca32b7d2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038576"
---
# <a name="bandwidth-sharing"></a><span data-ttu-id="c68ba-110">Bandbreiten Freigabe</span><span class="sxs-lookup"><span data-stu-id="c68ba-110">Bandwidth Sharing</span></span>

<span data-ttu-id="c68ba-111">Sie können Streams in einer Datei angeben, die, wenn Sie zusammengefasst werden, weniger Bandbreite als die Summe der angegebenen Bitraten kombiniert verwenden.</span><span class="sxs-lookup"><span data-stu-id="c68ba-111">You can specify streams in a file that, when taken together, use less bandwidth than the sum of their stated bit rates combined.</span></span> <span data-ttu-id="c68ba-112">Wenn Sie die Bandbreiten Freigabe im Profil angeben, verdeutlichen Sie, dass Anwendungen, die die verfügbare Bandbreite zum Streamen der Datei benötigt, nicht anders erscheinen.</span><span class="sxs-lookup"><span data-stu-id="c68ba-112">By specifying bandwidth sharing in the profile, you clarify to reading applications that the available bandwidth needed to stream the file is not what it might otherwise seem.</span></span>

<span data-ttu-id="c68ba-113">Keines der Objekte des SDK für das Windows Media-Format ändert das Verhalten in Reaktion auf Informationen zur Bandbreiten Freigabe, die ausschließlich bereitgestellt werden, damit Lese Anwendungen es berücksichtigen können, wenn Sie bestimmen, ob eine Datei mit eingeschränkter Bandbreiten Übermittlung wiedergegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="c68ba-113">None of the objects of the Windows Media Format SDK change their behavior in response to bandwidth sharing information, which is provided solely so that reading applications can take it into account when determining whether a file can be played with restricted bandwidth delivery.</span></span>

<span data-ttu-id="c68ba-114">Die Bandbreiten Freigabe wird mit einem Bandbreiten Freigabe Objekt konfiguriert und einem Profil hinzugefügt, bevor mit dem Schreiben einer Datei begonnen wird.</span><span class="sxs-lookup"><span data-stu-id="c68ba-114">Bandwidth sharing is configured with a bandwidth sharing object and is added to a profile before beginning to write a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c68ba-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c68ba-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c68ba-116">**Funktionen der ASF-Datei**</span><span class="sxs-lookup"><span data-stu-id="c68ba-116">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="c68ba-117">**Bandbreiten Freigabe Objekt**</span><span class="sxs-lookup"><span data-stu-id="c68ba-117">**Bandwidth Sharing Object**</span></span>](bandwidth-sharing-object.md)
</dt> <dt>

[<span data-ttu-id="c68ba-118">**Iwmbandwidthsharing-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c68ba-118">**IWMBandwidthSharing Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="c68ba-119">**IWMProfile3-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c68ba-119">**IWMProfile3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[<span data-ttu-id="c68ba-120">**Verwenden der Bandbreiten Freigabe**</span><span class="sxs-lookup"><span data-stu-id="c68ba-120">**Using Bandwidth Sharing**</span></span>](using-bandwidth-sharing.md)
</dt> </dl>

 

 




