---
title: Untertitel
description: Untertitel
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Windows Media Player, synchronisierter zugänglicher Medienaustausch (Sami)
- Windows Media Player-Objektmodell, synchronisierter zugänglicher Medienaustausch (Sami)
- Objektmodell, synchronisierter, zugänglicher Medienaustausch (Sami)
- Windows Media Player Mobile, synchronisierter verfügbarer Medienaustausch (Sami)
- Windows Media Player ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- Windows Media Player Mobile ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- ActiveX-Steuerelement, synchronisierter, zugänglicher Medienaustausch (Sami)
- Windows Media Player, Migrieren von Untertiteln
- Windows Media Player-Objektmodell, smigrieren von Untertiteln
- Objektmodell, Migrieren von Untertiteln
- Windows Media Player Mobile, Migrieren von Untertiteln
- Windows Media Player ActiveX-Steuerelement, Migrieren von Untertiteln
- Windows Media Player Mobile ActiveX-Steuerelement, Migrieren von Untertiteln
- ActiveX-Steuerelement, Migrieren von Untertiteln
- Synchronisierter, barrierefreier Medienaustausch (Sami), Migrieren von Untertiteln
- Sami (synchronisierter, barrierefreier Medienaustausch), Migrieren von Untertiteln
- Migrations Handbuch, synchronisierter zugänglicher Medienaustausch (Sami)
- Migrations Handbuch, Untertitel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc3dfdeff7a9893b617e99cd3f0b8fb5c62f4f
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101306"
---
# <a name="closed-captioning"></a><span data-ttu-id="d83fa-121">Untertitel</span><span class="sxs-lookup"><span data-stu-id="d83fa-121">Closed Captioning</span></span>

<span data-ttu-id="d83fa-122">Das ActiveX-Steuerelement von Windows Media Player 6,4 enthält einen integrierten Untertitel für die Untertitelanzeige, der bei sichtbar gemachten Untertiteln für den geschlossenen, zugänglichen Medienaustausch (Sami) aktiviert und den Text der geschlossenen Überschrift anzeigt.</span><span class="sxs-lookup"><span data-stu-id="d83fa-122">The Windows Media Player 6.4 ActiveX control includes an integrated closed caption display panel that, when made visible, enables Synchronized Accessible Media Interchange (SAMI) closed captions and displays the closed caption text.</span></span> <span data-ttu-id="d83fa-123">Das Steuerelement Windows Media Player 7 oder höher ermöglicht die Anzeige von Sami Closed Caption mithilfe eines HTML- **<DIV>** Elements.</span><span class="sxs-lookup"><span data-stu-id="d83fa-123">The Windows Media Player 7 or later control enables SAMI closed caption display by using an HTML **<DIV>** element.</span></span> <span data-ttu-id="d83fa-124">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d83fa-124">For example:</span></span>


```C++
<DIV  ID = "CCDiv"></DIV>

```



<span data-ttu-id="d83fa-125">Diese Technik bietet Ihnen vollständige Flexibilität, da Sie Ihre Webseite so entwerfen können, dass Untertitel auf angepasste Weise angezeigt werden. die Anzeige der geschlossenen Beschriftung ist nicht mehr erforderlich, um an einem bestimmten Speicherort neben der Windows Media Player-Benutzeroberfläche zu liegen.</span><span class="sxs-lookup"><span data-stu-id="d83fa-125">This technique provides you with complete flexibility, since you can design your webpage to display closed captions in a customized manner; the closed caption display is no longer required to be in a fixed location adjacent to the Windows Media Player user interface.</span></span>

<span data-ttu-id="d83fa-126">Nachdem Sie einen Bereich zum Anzeigen von Untertiteln erstellt haben, verwenden Sie *closedcaption*. **captioningid** -Eigenschaft, um den Speicherort anzugeben, an dem Windows Media Player den geschlossenen Beschriftungs Text rendert.</span><span class="sxs-lookup"><span data-stu-id="d83fa-126">Once you have created an area to display closed captions, use the *ClosedCaption*.**captioningID** property to specify the location where Windows Media Player renders the closed caption text.</span></span>


```C++
Player.closedCaption.captioningID = "CCDiv";

```



<span data-ttu-id="d83fa-127">Das Windows Media Player Software Development Kit (SDK) enthält ein funktionierendes Beispiel eines eingebetteten Players, der einen geschlossenen Beschriftungs Text anzeigt.</span><span class="sxs-lookup"><span data-stu-id="d83fa-127">The Windows Media Player Software Development Kit (SDK) contains a working sample of an embedded Player that displays closed caption text.</span></span> <span data-ttu-id="d83fa-128">Um die SDK-Beispiele zu erhalten, laden Sie das komplette Windows Media Player SDK von der Microsoft-Website herunter, und installieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="d83fa-128">To get the SDK samples, download and install the complete Windows Media Player SDK from the Microsoft Web Site.</span></span> <span data-ttu-id="d83fa-129">Weitere Informationen zu geschlossenen Beschriftungen und Sami finden Sie auf der [Microsoft-Website für Barrierefreiheit](https://www.microsoft.com/enable/).</span><span class="sxs-lookup"><span data-stu-id="d83fa-129">For more information about closed captions and SAMI, see the [Microsoft Accessibility website](https://www.microsoft.com/enable/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d83fa-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d83fa-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d83fa-131">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="d83fa-131">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="d83fa-132">**Closedcaption-Objekt**</span><span class="sxs-lookup"><span data-stu-id="d83fa-132">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="d83fa-133">**Handbuch für die Migration des Objektmodells**</span><span class="sxs-lookup"><span data-stu-id="d83fa-133">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




