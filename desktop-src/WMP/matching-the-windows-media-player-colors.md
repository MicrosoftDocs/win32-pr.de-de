---
title: Übereinstimmung der Windows-Media Player Farben
description: Übereinstimmung der Windows-Media Player Farben
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Windows Media Player Online Stores, übereinstimmende Windows Media Player Farben
- Online Stores, übereinstimmende Windows-Media Player Farben
- Typ 1 Online Stores, übereinstimmende Windows-Media Player Farben
- Typ 2 Online Stores, übereinstimmende Windows-Media Player Farben
- Windows Media Player Online Stores, Windows Media Player Farbabgleich
- Online Stores, Windows Media Player Farbabgleich
- Typ 1 Online Stores, Windows Media Player Farbabgleich
- Typ 2 Online Stores, Windows Media Player Farbabgleich
- Windows Media Player Online Stores, Farbabgleich für Windows Media Player
- Online Stores, Farbabgleich für Windows-Media Player
- Typ 1 Online Stores, Farbabgleich für Windows-Media Player
- Typ 2 Online Stores, Farbabgleich für Windows Media Player
- Farbabgleich für Windows-Media Player
- übereinstimmende Windows-Media Player Farben
- Windows Media Player, übereinstimmende Farben
- Windows Media Player, Farbabgleich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340852"
---
# <a name="matching-the-windows-media-player-colors"></a><span data-ttu-id="2a31c-119">Übereinstimmung der Windows-Media Player Farben</span><span class="sxs-lookup"><span data-stu-id="2a31c-119">Matching the Windows Media Player Colors</span></span>

<span data-ttu-id="2a31c-120">Es ist einfach, die Online Store-Webseite mit dem Windows-Media Player Farbschema zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="2a31c-120">Making your online store webpage match the Windows Media Player color scheme is easy.</span></span> <span data-ttu-id="2a31c-121">Behandeln Sie einfach das **externe. oncolorchange** -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="2a31c-121">Simply handle the **External.OnColorChange** event.</span></span> <span data-ttu-id="2a31c-122">Wenn Sie eine Funktion zur Behandlung des Ereignisses angeben möchten, verwenden Sie Code wie den folgenden, wenn die Webseite geladen wird:</span><span class="sxs-lookup"><span data-stu-id="2a31c-122">To specify a function to handle the event, use code like the following when your webpage loads:</span></span>


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



<span data-ttu-id="2a31c-123">Jedes Mal, wenn der Benutzer das Farbschema von Windows Media Player ändert, ruft der Player die Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="2a31c-123">Each time the user changes the color scheme of Windows Media Player, the Player will call your function.</span></span> <span data-ttu-id="2a31c-124">Das folgende Beispiel zeigt eine einfache Funktion, mit der der Webseiten Hintergrund so festgelegt wird, dass er der **externen. appcolorlight** -Eigenschaft entspricht:</span><span class="sxs-lookup"><span data-stu-id="2a31c-124">The following example shows a simple function that sets the webpage background to match the **External.appColorLight** property:</span></span>


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



<span data-ttu-id="2a31c-125">Für ihre Verwendung stehen auch andere Farbeigenschaften zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2a31c-125">There are other color properties available for your use as well.</span></span> <span data-ttu-id="2a31c-126">Siehe [externes Objekt für den Typ 2 Online Stores](external-object-for-type-2-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="2a31c-126">See [External Object for Type 2 Online Stores](external-object-for-type-2-online-stores.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a31c-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2a31c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a31c-128">**Extern. appcolorlight**</span><span class="sxs-lookup"><span data-stu-id="2a31c-128">**External.appColorLight**</span></span>](external-appcolorlight.md)
</dt> <dt>

[<span data-ttu-id="2a31c-129">**Externes. oncolorchange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="2a31c-129">**External.OnColorChange Event**</span></span>](external-oncolorchange-event.md)
</dt> <dt>

[<span data-ttu-id="2a31c-130">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="2a31c-130">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




