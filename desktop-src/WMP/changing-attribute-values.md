---
title: Ändern von Attributwerten
description: Ändern von Attributwerten
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
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
- Attribute, Ändern von Werten
- Ändern von Attributwerten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133e004e1140bdaac19b22be8bc1c77fe9327601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037113"
---
# <a name="changing-attribute-values"></a><span data-ttu-id="984b1-114">Ändern von Attributwerten</span><span class="sxs-lookup"><span data-stu-id="984b1-114">Changing Attribute Values</span></span>

<span data-ttu-id="984b1-115">Sie können den Wert eines Attributs ändern, wenn Ihre Webseite oder Anwendung Lese-/Schreibzugriff auf die Bibliothek hat und das Attribut gelesen und geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="984b1-115">You can change the value of an attribute if your webpage or application has read/write access to the library and the attribute can be both read and written.</span></span>

<span data-ttu-id="984b1-116">Sie können ein Attribut des aktuellen Medien Elements ändern.</span><span class="sxs-lookup"><span data-stu-id="984b1-116">You can change an attribute of the current media item.</span></span> <span data-ttu-id="984b1-117">Wenn Sie Attribute mehrerer Medienelemente ändern möchten, können Sie diese wiederum dem *Player* zuweisen. **currentMedia** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="984b1-117">To change attributes of multiple media items, you can assign each one in turn to the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="984b1-118">In diesem Thema wurde das **Player** -Objekt wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="984b1-118">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="984b1-119">Um ein Attribut zu ändern, nennen Sie den *Player*. *currentMedia*. die Methode " **stiteminfo** ", wie im folgenden c#-Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="984b1-119">To change an attribute, call the *Player*.*currentMedia*.**setItemInfo** method as shown in the following C# example.</span></span>


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



<span data-ttu-id="984b1-120">Es wird empfohlen, das *Medium* aufzurufen. **isleseronlyitem** -Methode, um zu bestimmen, ob Sie ein bestimmtes Attribut ändern können.</span><span class="sxs-lookup"><span data-stu-id="984b1-120">We recommend that you call the *Media*.**isReadOnlyItem** method to determine whether you can change a particular attribute.</span></span>

> [!Note]  
> <span data-ttu-id="984b1-121">Wenn Sie das-Steuerelement in Ihre Anwendung einbetten, werden Dateiattribute, die Sie ändern, erst dann in die digitale Mediendatei geschrieben, wenn der Benutzer Windows Media Player ausführt.</span><span class="sxs-lookup"><span data-stu-id="984b1-121">If you embed the control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span> <span data-ttu-id="984b1-122">Wenn Sie das-Steuerelement in einer Remote Anwendung verwenden, die in C++ geschrieben ist, werden die Dateiattribute, die Sie ändern, kurz nach dem vornehmen der Änderungen in die digitale Mediendatei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="984b1-122">If you use the control in a remoted application written in C++, file attributes that you change will be written to the digital media file shortly after you make the changes.</span></span> <span data-ttu-id="984b1-123">In beiden Fällen sind die Änderungen sofort über die Bibliothek verfügbar.</span><span class="sxs-lookup"><span data-stu-id="984b1-123">In either case, the changes are immediately available to you through the library.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="984b1-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="984b1-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="984b1-125">**Medien Element Attribute**</span><span class="sxs-lookup"><span data-stu-id="984b1-125">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="984b1-126">**Bibliotheks Zugriff**</span><span class="sxs-lookup"><span data-stu-id="984b1-126">**Library Access**</span></span>](library-access.md)
</dt> <dt>

[<span data-ttu-id="984b1-127">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="984b1-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="984b1-128">**Lesen von Attributwerten**</span><span class="sxs-lookup"><span data-stu-id="984b1-128">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> </dl>

 

 




