---
title: Verwenden des Windows Media Player-Steuer Elements in einer Webseite
description: Verwenden des Windows Media Player-Steuer Elements in einer Webseite
ms.assetid: 70616985-86e2-48df-a9e1-89caa11b4bd1
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player ActiveX-Steuerelement, Webseiten
- Windows Media Player Mobile ActiveX-Steuerelement, Webseiten
- ActiveX-Steuerelement, Webseiten
- Einbettungen, Webseiten
- Einbettung von Webseiten, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9cb69b2afa519091d8d729445cb87f02b9461a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207057"
---
# <a name="using-the-windows-media-player-control-in-a-web-page"></a><span data-ttu-id="8ecd9-115">Verwenden des Windows Media Player-Steuer Elements in einer Webseite</span><span class="sxs-lookup"><span data-stu-id="8ecd9-115">Using the Windows Media Player Control in a Web Page</span></span>

<span data-ttu-id="8ecd9-116">Wenn Sie das Windows Media Player-Steuerelement in eine Webseite einbetten, können Sie die Art und Weise, wie der Benutzer mit dem Steuerelement interagiert</span><span class="sxs-lookup"><span data-stu-id="8ecd9-116">Embedding the Windows Media Player control in a webpage lets you completely customize the way the user interacts with the control.</span></span> <span data-ttu-id="8ecd9-117">Sie können die Schnittstelle verwenden, die vom Steuerelement bereitgestellt wird, oder Sie können Sie ausblenden und ihre eigene Benutzeroberfläche anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8ecd9-117">You can use the interface provided by the control, or you can hide it and display your own user interface.</span></span> <span data-ttu-id="8ecd9-118">An dem Punkt, an dem Sie das Steuerelement einbetten, können Sie mehrere Windows Media Player-Steuerelement Eigenschaften angeben, oder Sie können die Player-Eigenschaften festlegen und Player-Methoden im Skriptcode festlegen.</span><span class="sxs-lookup"><span data-stu-id="8ecd9-118">You can specify multiple Windows Media Player control properties at the point where you embed the control, or you can set Player properties and call Player methods in script code.</span></span>

<span data-ttu-id="8ecd9-119">In den folgenden Abschnitten werden die Grundlagen zum Einbetten des Steuer Elements auf einer Webseite beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8ecd9-119">The following sections describe the basics of embedding the control in a webpage.</span></span>



| <span data-ttu-id="8ecd9-120">`Section`</span><span class="sxs-lookup"><span data-stu-id="8ecd9-120">Section</span></span>                                                                                                        | <span data-ttu-id="8ecd9-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ecd9-121">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ecd9-122">Ausblenden des Windows Media Player-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="8ecd9-122">Hiding the Windows Media Player Control</span></span>](hiding-the-windows-media-player-control.md)                         | <span data-ttu-id="8ecd9-123">Beschreibt die Optionen zum Ausblenden des Windows Media Player-Steuer Elements, wenn Sie eine eigene Benutzeroberfläche bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="8ecd9-123">Describes the options for hiding the Windows Media Player control when you want to provide your own user interface.</span></span>               |
| [<span data-ttu-id="8ecd9-124">Param-Elemente in einem Object-Element</span><span class="sxs-lookup"><span data-stu-id="8ecd9-124">PARAM Elements in an OBJECT Element</span></span>](param-elements-in-an-object-element.md)                                 | <span data-ttu-id="8ecd9-125">Beschreibt, wie das Windows Media Player-Steuerelement beim Einbetten initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="8ecd9-125">Describes how to initialize the Windows Media Player control when you embed it.</span></span>                                                   |
| [<span data-ttu-id="8ecd9-126">Einfaches Beispiel für die Skripterstellung auf einer Webseite</span><span class="sxs-lookup"><span data-stu-id="8ecd9-126">Simple Example of Scripting in a Web Page</span></span>](simple-example-of-scripting-in-a-web-page.md)                     | <span data-ttu-id="8ecd9-127">Beschreibt ein einfaches, aber umfassendes Beispiel für ein eingebettetes Player-Steuerelement mit einer benutzerdefinierten Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="8ecd9-127">Describes a simple, but complete, example of an embedded Player control with a custom user interface.</span></span>                             |
| [<span data-ttu-id="8ecd9-128">Verwenden des Windows Media Player-Steuer Elements mit Firefox</span><span class="sxs-lookup"><span data-stu-id="8ecd9-128">Using the Windows Media Player Control with Firefox</span></span>](using-the-windows-media-player-control-with-firefox.md) | <span data-ttu-id="8ecd9-129">Hier wird beschrieben, wie Sie das Windows Media Player-Steuerelement in eine Webseite einbetten, sodass es von einem Firefox-Browser richtig angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8ecd9-129">Describes how to embed the Windows Media Player control in a webpage so that it will be displayed correctly by a Firefox browser.</span></span> |
| [<span data-ttu-id="8ecd9-130">Verwenden von Windows Media Player mit Netscape 7.1</span><span class="sxs-lookup"><span data-stu-id="8ecd9-130">Using Windows Media Player with Netscape 7.1</span></span>](using-windows-media-player-with-netscape-7-1.md)               | <span data-ttu-id="8ecd9-131">Beschreibt die Verwendung des Windows Media Player-Steuer Elements mit Netscape 7,1 und anderen Gecko-basierten Webbrowsern.</span><span class="sxs-lookup"><span data-stu-id="8ecd9-131">Describes how to use the Windows Media Player control with Netscape 7.1 and other Gecko-based Web browsers.</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="8ecd9-132">Das Windows Media Player 10 Mobile-Steuerelement enthält Funktionen, die auf einer Teilmenge der Funktionalität basieren, die in der Desktop Version des Windows Media Player-Steuer Elements bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8ecd9-132">The Windows Media Player 10 Mobile control contains functionality based on a subset of the functionality provided in the desktop version of the Windows Media Player control.</span></span> <span data-ttu-id="8ecd9-133">Daher kann Sie in eine Pocket Internet Explorer-Webseite auf die gleiche Weise eingebettet werden, wie das Desktop Steuerelement in eine Internet Explorer-Webseite eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="8ecd9-133">Therefore, it can be embedded in a Pocket Internet Explorer webpage the same way the desktop control is embedded in an Internet Explorer webpage.</span></span> <span data-ttu-id="8ecd9-134">Informationen dazu, ob eine bestimmte Methode, Eigenschaft oder ein Ereignis für das Windows Media Player 10 Mobile-Steuerelement unterstützt wird, finden Sie unter [Objektmodell Referenz für die Skript](object-model-reference-for-scripting.md)Erstellung.</span><span class="sxs-lookup"><span data-stu-id="8ecd9-134">To find out whether a particular method, property, or event is supported for the Windows Media Player 10 Mobile control, see [Object Model Reference for Scripting](object-model-reference-for-scripting.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8ecd9-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8ecd9-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ecd9-136">**Player-Steuerelement Handbuch**</span><span class="sxs-lookup"><span data-stu-id="8ecd9-136">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




