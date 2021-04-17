---
title: Verwalten der Paketgröße
description: Verwalten der Paketgröße
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- Windows Media-Format-SDK, Verwalten von Paketgrößen
- Windows Media-Format-SDK, Paketgrößen
- Profile, Paketgrößen
- Profile, Verwalten von Paketgrößen
- Pakete, Größen
- Pakete, iwmpacketsize-Schnittstelle
- Iwmpacketsize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e5bb0720d54338a754838e3d44c4479e55af9d
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104390055"
---
# <a name="managing-packet-size"></a><span data-ttu-id="b8b03-110">Verwalten der Paketgröße</span><span class="sxs-lookup"><span data-stu-id="b8b03-110">Managing Packet Size</span></span>

<span data-ttu-id="b8b03-111">Der Writer ist darauf ausgelegt, die Größe von Paketen intern zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="b8b03-111">The writer is designed to manage the size of packets internally.</span></span> <span data-ttu-id="b8b03-112">Möglicherweise haben Sie jedoch spezielle Anforderungen an Ihre Anwendung, die eine manuelle Steuerung der Größe von Paketen in den von Ihnen geschriebenen ASF-Dateien erfordern.</span><span class="sxs-lookup"><span data-stu-id="b8b03-112">However, you may have specific requirements for your application that call for some manual control over the size of packets in the ASF files that you write.</span></span> <span data-ttu-id="b8b03-113">Das Windows Media-Format SDK bietet zwei Schnittstellen, [**iwmpacketsize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) und [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) , mit denen Sie die maximale und minimale Größe von Paketen steuern können.</span><span class="sxs-lookup"><span data-stu-id="b8b03-113">The Windows Media Format SDK provides two interfaces, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) and [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) that enable you to control the maximum and minimum size of packets.</span></span>

<span data-ttu-id="b8b03-114">Beide Schnittstellen für die Paketgröße werden im Profil Objekt verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="b8b03-114">Both packet size interfaces are exposed in the profile object.</span></span> <span data-ttu-id="b8b03-115">Sie sind auch für das Reader-Objekt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b8b03-115">They are also available to the reader object.</span></span> <span data-ttu-id="b8b03-116">Wie bei anderen Profil bezogenen Schnittstellen kann der Reader nur auf die Lesemethoden zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b8b03-116">As with other profile-related interfaces, the reader can access only the reading methods.</span></span>

<span data-ttu-id="b8b03-117">Die Größe von Paketen wirkt sich auf die Leistung aus.</span><span class="sxs-lookup"><span data-stu-id="b8b03-117">The size of packets has some effect on performance.</span></span> <span data-ttu-id="b8b03-118">Im Allgemeinen wird die Größe der Daten in einer Datei mit der geringeren Paketgröße fragmentiert.</span><span class="sxs-lookup"><span data-stu-id="b8b03-118">In general, the smaller the packet size, the more fragmented the data is within a file.</span></span> <span data-ttu-id="b8b03-119">Wenn eine Datei stärker fragmentiert ist, desto weniger effizient wird Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="b8b03-119">The more fragmented a file is, the less efficient it will be to reconstruct it.</span></span> <span data-ttu-id="b8b03-120">In einem Streamingszenario ist dies möglicherweise kein wichtiger Aspekt, da das Lesen einer Datei aus einer Internet Quelle im allgemeinen ineffizient ist.</span><span class="sxs-lookup"><span data-stu-id="b8b03-120">In a streaming scenario, this may not be an important consideration, as the process of reading a file from an Internet source is generally inefficient.</span></span> <span data-ttu-id="b8b03-121">Beim lokalen Umgang mit einer Datei ist dies jedoch möglicherweise ein Aspekt.</span><span class="sxs-lookup"><span data-stu-id="b8b03-121">When dealing with a file locally however, this might be a consideration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8b03-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b8b03-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8b03-123">**Iwmpacketsize-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b8b03-123">**IWMPacketSize Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[<span data-ttu-id="b8b03-124">**IWMPacketSize2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b8b03-124">**IWMPacketSize2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[<span data-ttu-id="b8b03-125">**Arbeiten mit Profilen**</span><span class="sxs-lookup"><span data-stu-id="b8b03-125">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




