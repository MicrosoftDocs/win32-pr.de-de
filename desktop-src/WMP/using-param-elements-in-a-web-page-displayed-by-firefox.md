---
title: Verwenden von param-Elementen in einer Webseite, die von Firefox angezeigt wird
description: Verwenden von param-Elementen in einer Webseite, die von Firefox angezeigt wird
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
keywords:
- Windows-Media Player, param-Elemente im Object-Element
- Windows Media Player-Objektmodell, param-Elemente im Object-Element
- Objektmodell, param-Elemente im Object-Element
- Windows Media Player Mobile, param-Elemente im Object-Element
- Windows Media Player ActiveX-Steuerelement, param-Elemente im Object-Element
- Windows Media Player Mobile ActiveX-Steuerelement, param-Elemente im Object-Element
- ActiveX-Steuerelement, param-Elemente im Object-Element
- Einbettungen, Webseiten
- Seiten Einbettung, param-Elemente im Object-Element
- Param-Elemente im Object-Element
- Windows Media Player, Firefox
- Windows Media Player-Objektmodell, Firefox
- Objektmodell, Firefox
- Windows Media Player Mobile, Firefox
- Windows Media Player ActiveX-Steuerelement, Firefox
- Windows Media Player Mobile ActiveX-Steuerelement, Firefox
- ActiveX-Steuerelement, Firefox
- Firefox, param-Elemente im Object-Element
- Einbettung von Webseiten, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b045d111ff3cd0de09f54a8cf7ac25028fa1dc6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "104311681"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="e60d5-122">Verwenden von param-Elementen in einer Webseite, die von Firefox angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="e60d5-122">Using PARAM Elements in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="e60d5-123">Sie können param-Elemente innerhalb eines Object-Elements verwenden, um den Anfangszustand des Player-Steuer Elements festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e60d5-123">You can use PARAM elements inside an OBJECT element to set the initial state of the Player control.</span></span> <span data-ttu-id="e60d5-124">Beispielsweise geben die param-Elemente im folgenden Beispiel an, dass das-Steuerelement automatisch Seattle. wmv abspielen soll.</span><span class="sxs-lookup"><span data-stu-id="e60d5-124">For example, the PARAM elements in the following example specify that the control should play seattle.wmv automatically.</span></span>


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



<span data-ttu-id="e60d5-125">Die meisten param-Elemente können von Internet Explorer und Firefox interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="e60d5-125">Most PARAM elements can be interpreted by Internet Explorer and by Firefox.</span></span> <span data-ttu-id="e60d5-126">Es gibt jedoch einige param-Elemente, die vom Firefox-Plug-in nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e60d5-126">However, there are a few PARAM elements that the Firefox plug-in does not support.</span></span> <span data-ttu-id="e60d5-127">Informationen darüber, welche param-Elemente vom Firefox-Plug-in unterstützt werden, finden Sie unter [param-Elemente in einem Object-Element](param-elements-in-an-object-element.md).</span><span class="sxs-lookup"><span data-stu-id="e60d5-127">For information about which PARAM elements are supported by the Firefox plug-in, see [PARAM Elements in an OBJECT Element](param-elements-in-an-object-element.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e60d5-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e60d5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e60d5-129">**Verwenden des Windows Media Player-Steuer Elements mit Firefox**</span><span class="sxs-lookup"><span data-stu-id="e60d5-129">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




