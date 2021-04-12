---
title: Verwenden der Bandbreiten Freigabe
description: Verwenden der Bandbreiten Freigabe
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- Windows Media-Format-SDK, Bandbreiten Freigabe
- Bandbreiten Freigabe, Informationen zu
- Profile, Bandbreiten Freigabe
- Streams, Bandbreiten Freigabe
- Bandbreiten Freigabe, iwmprofile-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298c690b484a8b4b5990aacd5d525867da8923c0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104390062"
---
# <a name="using-bandwidth-sharing"></a><span data-ttu-id="eeacc-108">Verwenden der Bandbreiten Freigabe</span><span class="sxs-lookup"><span data-stu-id="eeacc-108">Using Bandwidth Sharing</span></span>

<span data-ttu-id="eeacc-109">Mit Bandbreiten Freigabe Objekten können Sie angeben, dass bestimmte Datenströme, wenn kombiniert, nicht mehr Bandbreite als angegeben verwenden.</span><span class="sxs-lookup"><span data-stu-id="eeacc-109">You can use bandwidth sharing objects to specify that certain streams, when combined, will not use more bandwidth than specified.</span></span> <span data-ttu-id="eeacc-110">Die Informationen in einem Bandbreiten Freigabe Objekt werden weder vom Writer generiert noch überprüft.</span><span class="sxs-lookup"><span data-stu-id="eeacc-110">The information in a bandwidth sharing object is not generated or verified by the writer nor used by the reader for anything.</span></span>

<span data-ttu-id="eeacc-111">Wenn eine Datei mit Informationen zur Bandbreiten Freigabe im Profil geschrieben wird, werden die Daten im Header Abschnitt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="eeacc-111">When a file is written that has bandwidth sharing information in its profile, the data is stored in its header section.</span></span> <span data-ttu-id="eeacc-112">Sie können die [**iwmprofile**](iwmprofile.md) -Schnittstelle im Reader verwenden, um Informationen zur Bandbreiten Freigabe zu überprüfen, wenn die Datei wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eeacc-112">You can use the [**IWMProfile**](iwmprofile.md) interface in the reader to check for bandwidth sharing information when the file is played.</span></span>

<span data-ttu-id="eeacc-113">Jedes Bandbreiten Freigabe Objekt wird durch zwei Einstellungen definiert.</span><span class="sxs-lookup"><span data-stu-id="eeacc-113">Each bandwidth sharing object is defined by two settings.</span></span> <span data-ttu-id="eeacc-114">Die erste ist die Bandbreite, wie durch die Bandbreite und ein Puffer Fenster definiert.</span><span class="sxs-lookup"><span data-stu-id="eeacc-114">First is the bandwidth, as defined by a bandwidth and a buffer window.</span></span> <span data-ttu-id="eeacc-115">Die zweite Einstellung ist ein Typ der Bandbreiten Freigabe, der entweder exklusiv oder partiell sein kann.</span><span class="sxs-lookup"><span data-stu-id="eeacc-115">The second setting is a bandwidth sharing type, which can be either exclusive or partial.</span></span> <span data-ttu-id="eeacc-116">Exklusive Bandbreiten Freigabe bedeutet, dass die einzelnen Datenströme nacheinander wiedergegeben werden, während partiell bedeutet, dass die Streams gleichzeitig übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="eeacc-116">Exclusive bandwidth sharing means that the constituent streams are played back one at a time, while partial means the streams are delivered concurrently.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eeacc-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eeacc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeacc-118">**Iwmprofile-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="eeacc-118">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="eeacc-119">**IWMProfile3:: addbandwidthsharing**</span><span class="sxs-lookup"><span data-stu-id="eeacc-119">**IWMProfile3::AddBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="eeacc-120">**IWMProfile3:: kreatenewbandwidthsharing**</span><span class="sxs-lookup"><span data-stu-id="eeacc-120">**IWMProfile3::CreateNewBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="eeacc-121">**IWMProfile3:: getbandwidthsharing**</span><span class="sxs-lookup"><span data-stu-id="eeacc-121">**IWMProfile3::GetBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="eeacc-122">**IWMProfile3:: getbandwidthsharingcount**</span><span class="sxs-lookup"><span data-stu-id="eeacc-122">**IWMProfile3::GetBandwidthSharingCount**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount)
</dt> <dt>

[<span data-ttu-id="eeacc-123">**Arbeiten mit Profilen**</span><span class="sxs-lookup"><span data-stu-id="eeacc-123">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




