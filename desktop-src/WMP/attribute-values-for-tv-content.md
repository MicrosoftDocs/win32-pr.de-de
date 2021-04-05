---
title: Attributwerte für TV-Inhalt
description: Attributwerte für TV-Inhalt
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
keywords:
- Windows Media Player, Attribute für Medienelemente
- Windows Media Player-Objektmodell, Attribute für Medienelemente
- Objektmodell, Attribute für Medienelemente
- Windows Media Player Mobile, Attribute für Medienelemente
- Windows Media Player ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player Mobile ActiveX-Steuerelement, Attribute für Medienelemente
- ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player-Bibliothek, Attribute für Medienelemente
- Bibliothek, Attribute für Medienelemente
- Attribute, TV-Inhalt
- Werte für TV-Inhalts Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb63e872edd80944772a320da5f2094e6d8f5757
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037599"
---
# <a name="attribute-values-for-tv-content"></a><span data-ttu-id="59036-114">Attributwerte für TV-Inhalt</span><span class="sxs-lookup"><span data-stu-id="59036-114">Attribute Values for TV Content</span></span>

<span data-ttu-id="59036-115">In diesem Thema wurde das **Player** -Objekt wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="59036-115">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="59036-116">Windows Media Player 10 oder höher kann TV-Inhalte in der Bibliothek organisieren.</span><span class="sxs-lookup"><span data-stu-id="59036-116">Windows Media Player 10 or later can organize TV content in the library.</span></span> <span data-ttu-id="59036-117">Windows Media Player behandelt TV-Inhalte als Unterkategorie von Videoinhalten.</span><span class="sxs-lookup"><span data-stu-id="59036-117">Windows Media Player treats TV content as a subcategory of video content.</span></span> <span data-ttu-id="59036-118">Um Videoinhalte in den TV-Knoten in der Bibliothek anzuzeigen, legen Sie die Attribute **WM/mediaclassprimaryid** und **WM/MediaClassSecondaryID** mithilfe der *Medien* auf die Werte in der folgenden Tabelle fest. die Methode " **stiteminfo** ":</span><span class="sxs-lookup"><span data-stu-id="59036-118">To make video content appear in the TV nodes in the library, set the **WM/MediaClassPrimaryID** and the **WM/MediaClassSecondaryID** attributes to the values in the following table by using the *media*.**setItemInfo** method:</span></span>



| <span data-ttu-id="59036-119">Attribut</span><span class="sxs-lookup"><span data-stu-id="59036-119">Attribute</span></span>                    | <span data-ttu-id="59036-120">Wert</span><span class="sxs-lookup"><span data-stu-id="59036-120">Value</span></span>                                |
|------------------------------|--------------------------------------|
| <span data-ttu-id="59036-121">**WM/mediaclassprimaryid**</span><span class="sxs-lookup"><span data-stu-id="59036-121">**WM/MediaClassPrimaryID**</span></span>   | <span data-ttu-id="59036-122">DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B</span><span class="sxs-lookup"><span data-stu-id="59036-122">DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B</span></span> |
| <span data-ttu-id="59036-123">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="59036-123">**WM/MediaClassSecondaryID**</span></span> | <span data-ttu-id="59036-124">BA7F258A-62F7-47A9-B21F-4651C42A000E</span><span class="sxs-lookup"><span data-stu-id="59036-124">BA7F258A-62F7-47A9-B21F-4651C42A000E</span></span> |



 

<span data-ttu-id="59036-125">Sie können diese Werte auch verwenden, um zu bestimmen, ob ein bestimmtes digitales Medien Element TV-Inhalte mithilfe der *Medien* enthält. **getiteminfo** oder *Medium*. **getItemInfoByType** -Methoden.</span><span class="sxs-lookup"><span data-stu-id="59036-125">You can also use these values to determine whether a particular digital media item contains TV content by using the *media*.**getItemInfo** or *media*.**getItemInfoByType** methods.</span></span>

<span data-ttu-id="59036-126">Denken Sie daran, die **GUID** -Werte als **Zeichen** folgen Werte zu verwenden, wenn Sie diese Werte angeben oder abrufen.</span><span class="sxs-lookup"><span data-stu-id="59036-126">Remember to use the **GUID** values as **string** values when specifying or retrieving these values.</span></span>

<span data-ttu-id="59036-127">Im folgenden c#-Beispielcode werden die Medien Klassenattribute so festgelegt, dass ein Medien Element als Fernseh Inhalt identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="59036-127">The following C# example code sets the media class attributes so that a media item will be identified as TV content.</span></span>


```C++
// Initialize the media object.
// This code assumes only 1 item named MyFile.
IWMPMedia3 media = (IWMPMedia3)Player.mediaCollection.getByName("MyFile").item(0);

// Set the primary media-class identifier.
media.setItemInfo("WM/MediaClassPrimaryID", "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B");

// Set the secondary media-class identifier.
media.setItemInfo("WM/MediaClassSecondaryID", "BA7F258A-62F7-47A9-B21F-4651C42A000E");

```



<span data-ttu-id="59036-128">Weitere Informationen zu den möglichen Werten für die Medien Klassenattribute finden Sie in den [Richtlinien zur Verwendung von Windows Media-Metadaten](/previous-versions/ms867702(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="59036-128">For more info about the possible values for the media class attributes, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="59036-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59036-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59036-130">**Medien Element Attribute**</span><span class="sxs-lookup"><span data-stu-id="59036-130">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="59036-131">**Bibliotheks Zugriff**</span><span class="sxs-lookup"><span data-stu-id="59036-131">**Library Access**</span></span>](library-access.md)
</dt> <dt>

[<span data-ttu-id="59036-132">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="59036-132">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 




