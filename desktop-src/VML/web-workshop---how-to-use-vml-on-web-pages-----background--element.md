---
title: Verwenden des Background-Elements
description: Verwenden des Background-Elements
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Webworkshop, Hintergrund Element
- Entwerfen von Webseiten, Background-Element
- Vector Markup Language (VML), Background-Element
- VML (Vector Markup Language), Background-Element
- Vektorgrafiken, Hintergrund Element
- Background-Element
- VML-Elemente, Hintergrund
- VML-Formen, Background-Element
- Vector Markup Language (VML), Anpassen von Hintergründen
- VML (Vector Markup Language), Anpassen von Hintergründen
- Vektorgrafiken, Anpassen von Hintergründen
- VML-Formen, Anpassen von Hintergründen
- Anpassen von Hintergründen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0108b91f199fbc3bff1c28ebdf016bfba11957
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858304"
---
# <a name="using-the-background-element"></a><span data-ttu-id="623e2-116">Verwenden des Background-Elements</span><span class="sxs-lookup"><span data-stu-id="623e2-116">Using the Background Element</span></span>

<span data-ttu-id="623e2-117">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="623e2-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="623e2-118">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="623e2-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="623e2-119">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="623e2-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="623e2-120">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="623e2-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="623e2-121">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="623e2-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="623e2-122">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="623e2-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="623e2-123">In diesem Thema wird veranschaulicht, wie Sie den Hintergrund einer Webseite anpassen können, indem Sie das `<background>` in VML bereitgestellte-Element verwenden.</span><span class="sxs-lookup"><span data-stu-id="623e2-123">In this topic, we will illustrate how you can customize the background of a Web page by using the `<background>` element provided in VML.</span></span>

<span data-ttu-id="623e2-124">Wie Sie aus dem Thema " [Verwendung `<fill>` ](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) " gelernt haben, können Sie das `<fill>` untergeordnete Element innerhalb des `<shape>` , `<shapetype>` oder eines beliebigen vordefinierten Shape-Elements platzieren, um zu beschreiben, wie die Form ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="623e2-124">As you've learned from the [Use `<fill>`](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) topic, you can place the `<fill>` sub-element inside the `<shape>`, `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span>

<span data-ttu-id="623e2-125">Entsprechend können Sie das untergeordnete `<fill>` -Element im- `<background>` Element platzieren, um zu beschreiben, wie der Hintergrund einer Webseite ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="623e2-125">Similarly, you can place the `<fill>` sub-element inside the `<background>` element to describe how to fill the background of a Web page.</span></span> <span data-ttu-id="623e2-126">Anschließend können Sie die Eigenschafts Attribute des `<fill>` unter Elements verwenden, um den Fülleffekt anzupassen, z. b. die Füllung des [Farbverlaufs](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), die [Musterfüllung](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)oder die [Bild Füllung](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).</span><span class="sxs-lookup"><span data-stu-id="623e2-126">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), [pattern fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), or [picture fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).</span></span>

<span data-ttu-id="623e2-127">Wenn Sie z. b. einen Hintergrund mit Farbverlauf zeichnen möchten, können Sie die folgenden Zeilen in den `<BODY>` Bereich der Webseite eingeben:</span><span class="sxs-lookup"><span data-stu-id="623e2-127">For example, to draw a gradient-filled background, you can type the following lines in the `<BODY>` region of your Web page:</span></span>


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





<span data-ttu-id="623e2-128">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858389) .</span><span class="sxs-lookup"><span data-stu-id="623e2-128">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858389) .</span></span>

 

 