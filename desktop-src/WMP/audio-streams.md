---
title: Audiodatenströme
description: Audiodatenströme
ms.assetid: 7bb39c48-5d0b-483d-83ee-946adfc9724f
keywords:
- Windows Media Player Online Stores, Audiostreams
- Online Stores, Audiostreams
- Typ 1 Online Stores, Audiostreams
- Windows Media Player Online Stores, Streams von Musik Servern
- Online Stores, Streams von Musik Servern
- Geben Sie 1 Online Stores, Streams von Musik Servern ein.
- Windows Media Player Online Stores, Music Server Streams
- Online Stores, Music Server Streams
- Typ 1 Online Stores, Music Server Streams
- Audiodatenströme
- Musik-Serverdaten Ströme
- Streams von Musik Servern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7164a703417e2efb8e32b2632890972957f7adf7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038581"
---
# <a name="audio-streams"></a><span data-ttu-id="6e126-115">Audiodatenströme</span><span class="sxs-lookup"><span data-stu-id="6e126-115">Audio Streams</span></span>

<span data-ttu-id="6e126-116">Online Stores können Musik als Stream von einem Musikserver bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6e126-116">Online stores can provide music as a stream from a music server.</span></span> <span data-ttu-id="6e126-117">Dies ist nützlich für das Bereitstellen von Beispielen, speziellen Aktions Artikeln oder das ermöglichen von Abonnement Benutzern, Musik zu nutzen, ohne den Inhalt herunterladen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="6e126-117">This is useful for providing samples, special promotional items, or to enable subscription users to enjoy music without having to download the content.</span></span> <span data-ttu-id="6e126-118">Es ist üblich, dass die URL des Streams nicht als Teil des musikkatalogs gespeichert wird, sondern stattdessen die URL vor der Wiedergabe basierend auf der ID des Titels aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="6e126-118">It is common not to store the URL of the stream as part of the music catalog, but instead to resolve the URL just before playback based upon the track ID.</span></span> <span data-ttu-id="6e126-119">Um dies zu ermöglichen, ruft Windows Media Player [iwmpcontentpartner:: getstreamingurl](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) auf und stellt den Streamingtyp (als [wmpstreamingtype](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) -Enumerationswert) und die ID für den Datenstrom bereit.</span><span class="sxs-lookup"><span data-stu-id="6e126-119">To enable this, Windows Media Player calls [IWMPContentPartner::GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) and provides the streaming type (as a [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) enumeration value) and the ID for the stream.</span></span> <span data-ttu-id="6e126-120">Das Plug-in gibt die URL für den Datenstrom über den *pbstrinurl* -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="6e126-120">The plug-in returns the URL for the stream through the *pbstrURL* parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e126-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e126-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e126-122">**Informationen zu Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="6e126-122">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




