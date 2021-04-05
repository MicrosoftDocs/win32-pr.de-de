---
title: DVD
description: DVD
ms.assetid: b3634a28-b1d6-44a5-97e4-fcc1f655d652
keywords:
- Windows Media Player, Migrieren von DVDs
- Windows Media Player-Objektmodell, DVDs
- Objektmodell, DVDs
- Windows Media Player ActiveX-Steuerelement, DVDs
- ActiveX-Steuerelement, DVDs
- Windows Media Player Mobile ActiveX-Steuerelement, DVDs
- Windows Media Player Mobile, Migrieren von DVDs
- Migrations Handbuch, DVDs
- DVD-Migration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e0a19818ac01b5e3d6138f896f26fe674c5ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711627"
---
# <a name="dvd"></a><span data-ttu-id="fb3f5-112">DVD</span><span class="sxs-lookup"><span data-stu-id="fb3f5-112">DVD</span></span>

<span data-ttu-id="fb3f5-113">Das ActiveX-Steuerelement von Windows Media Player 6,4 enthält ein **DVD** -Objekt, das eine Vielzahl von Methoden und Eigenschaften verfügbar macht, und ein Ereignis, um speziell mit DVD-Inhalten umzugehen.</span><span class="sxs-lookup"><span data-stu-id="fb3f5-113">The Windows Media Player 6.4 ActiveX control contains a **DVD** object that exposes a variety of methods and properties, and one event, for dealing specifically with DVD content.</span></span> <span data-ttu-id="fb3f5-114">Um beispielsweise die Anzahl der verfügbaren DVD-Titel zu ermitteln, verwenden Sie **Player6**. **titlesavailable** -Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="fb3f5-114">For instance, to determine the number of DVD titles available, you use the **Player6**.**titlesAvailable** property:</span></span>


```C++
var numTitles = WMP64.DVD.TitlesAvailable;

```



<span data-ttu-id="fb3f5-115">Mit dem Objektmodell Windows Media Player 7 oder höher wird ein stärker integrierter Ansatz für DVD implementiert.</span><span class="sxs-lookup"><span data-stu-id="fb3f5-115">The Windows Media Player 7 or later object model implements a more integrated approach to DVD.</span></span> <span data-ttu-id="fb3f5-116">DVD-spezifische Eigenschaften, Methoden und Ereignisse werden nur bei Bedarf implementiert.</span><span class="sxs-lookup"><span data-stu-id="fb3f5-116">DVD-specific properties, methods, and events are implemented only where needed.</span></span> <span data-ttu-id="fb3f5-117">Andernfalls funktionieren vorhandene Objektmodell Funktionen wie erwartet mit DVD-Medien.</span><span class="sxs-lookup"><span data-stu-id="fb3f5-117">Otherwise, existing object model functionality works with DVD media as you might expect.</span></span> <span data-ttu-id="fb3f5-118">Wenn Sie z. b. die Anzahl der verfügbaren DVD-Titel ermitteln möchten, wenn Sie Windows Media Player 7 oder höher verwenden, rufen Sie ein **Wiedergabe** Listen Objekt aus dem **CDROM** -Objekt ab:</span><span class="sxs-lookup"><span data-stu-id="fb3f5-118">For example, to determine the number of DVD titles available when using Windows Media Player 7 or later, you retrieve a **Playlist** object from the **Cdrom** object:</span></span>


```C++
var dvdTitles = WMP9.cdromCollection.item(0).playlist;

```



<span data-ttu-id="fb3f5-119">Im vorangehenden Beispiel wird ein **Wiedergabe** Listen Objekt mit einem ersten Eintrag abgerufen, der das DVD-Medium auf dem ersten Laufwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="fb3f5-119">The preceding example retrieves a **Playlist** object with a first entry representing the DVD media in the first drive.</span></span> <span data-ttu-id="fb3f5-120">Zusätzliche Einträge stellen einzelne DVD-Titel dar.</span><span class="sxs-lookup"><span data-stu-id="fb3f5-120">Additional entries represent individual DVD titles.</span></span> <span data-ttu-id="fb3f5-121">Daher kann die Anzahl der verfügbaren Titel wie folgt berechnet werden:</span><span class="sxs-lookup"><span data-stu-id="fb3f5-121">Therefore, the number of titles available can be calculated as follows:</span></span>


```C++
var numTitles = dvdTitles.count - 1;

```



<span data-ttu-id="fb3f5-122">Im folgenden finden Sie die wichtigsten Unterschiede, die bei der Migration von Version 6,4 zu beachten sind:</span><span class="sxs-lookup"><span data-stu-id="fb3f5-122">Here are the main differences to keep in mind when migrating from version 6.4:</span></span>

-   <span data-ttu-id="fb3f5-123">Die DVD-Wiedergabe wird nur unterstützt, wenn Windows Media Player für Windows XP oder höher und das Betriebssystem Windows XP oder höher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb3f5-123">DVD playback is supported only when using Windows Media Player for Windows XP or later and the Windows XP operating system or later.</span></span>
-   <span data-ttu-id="fb3f5-124">DVD-ROM-Laufwerke werden genau wie CD-ROM-Laufwerke mit dem **cdromcollection** -Objekt aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fb3f5-124">DVD-ROM drives are enumerated exactly like CD-ROM drives using the **CdromCollection** object.</span></span>
-   <span data-ttu-id="fb3f5-125">Einzelne DVD-ROM-Laufwerke werden mithilfe des **CDROM** -Objekts verwaltet.</span><span class="sxs-lookup"><span data-stu-id="fb3f5-125">Individual DVD-ROM drives are managed using the **Cdrom** object.</span></span>
-   <span data-ttu-id="fb3f5-126">Das **DVD** -Objekt erweitert das Objektmodell mit Methoden und einer Eigenschaft, die speziell für die Arbeit mit DVD vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="fb3f5-126">The **DVD** object extends the object model with methods and one property specifically for working with DVD.</span></span>
-   <span data-ttu-id="fb3f5-127">Es gibt zwei neue Ereignisse: **openplaylistswitch** und **domainchange**, speziell für die Arbeit mit DVD.</span><span class="sxs-lookup"><span data-stu-id="fb3f5-127">There are two new events, **OpenPlaylistSwitch** and **DomainChange**, specifically for working with DVD.</span></span>
-   <span data-ttu-id="fb3f5-128">Der DVD-Inhalt wird mithilfe von **Wiedergabe** Listen Objekten und **Medien** Objekten organisiert.</span><span class="sxs-lookup"><span data-stu-id="fb3f5-128">DVD content is organized using **Playlist** objects and **Media** objects.</span></span>
-   <span data-ttu-id="fb3f5-129">DVD-Sprachen werden mithilfe der sprach Funktionalität verwaltet **, die im Steuerelement Objekt (** Windows Media Player 9 oder höher) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fb3f5-129">DVD languages are managed using the language functionality available from the **Controls** object (Windows Media Player 9 Series or later).</span></span>
-   <span data-ttu-id="fb3f5-130">Transport Steuerelemente und Positionsinformationen für DVD funktionieren identisch mit denen für andere digitale Medientypen.</span><span class="sxs-lookup"><span data-stu-id="fb3f5-130">Transport controls and position information for DVD work the same as for other digital media types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb3f5-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fb3f5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb3f5-132">**Handbuch für die Migration des Objektmodells**</span><span class="sxs-lookup"><span data-stu-id="fb3f5-132">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="fb3f5-133">**Verwenden des Windows Media Player-Steuer Elements mit Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="fb3f5-133">**Using the Windows Media Player Control with Visual Basic**</span></span>](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




