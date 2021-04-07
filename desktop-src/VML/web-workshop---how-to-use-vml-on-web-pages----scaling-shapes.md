---
title: Skalieren von Formen
description: Skalieren von Formen
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- Webworkshop, Skalieren von Formen
- Entwerfen von Webseiten, Skalieren von Formen
- Vector Markup Language (VML), Skalieren von Formen
- VML (Vector Markup Language), Skalieren von Formen
- Vektorgrafiken, Skalierungs Formen
- VML-Formen, Skalierung
- Skalieren von Formen
- Vector Markup Language (VML), Größen Anpassungs Formen
- VML (Vector Markup Language), Größen Anpassungs Formen
- Vektorgrafiken, Größen Anpassungs Formen
- VML-Formen, Größenanpassung
- Größen Anpassungs Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e7c64fdc0eaa32df1f22b06734b366609ee319
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727937"
---
# <a name="scaling-shapes"></a><span data-ttu-id="8995f-115">Skalieren von Formen</span><span class="sxs-lookup"><span data-stu-id="8995f-115">Scaling Shapes</span></span>

<span data-ttu-id="8995f-116">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="8995f-116">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8995f-117">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="8995f-117">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8995f-118">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="8995f-118">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8995f-119">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8995f-119">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8995f-120">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8995f-120">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8995f-121">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8995f-121">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8995f-122">Sie haben gelernt, wie Formen mithilfe von VML auf einer Webseite gezeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="8995f-122">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="8995f-123">In diesem Thema wird veranschaulicht, wie Sie Formen auf eine beliebige Größe skalieren.</span><span class="sxs-lookup"><span data-stu-id="8995f-123">In this topic, we will illustrate how to scale shapes to any size you want.</span></span>

<span data-ttu-id="8995f-124">VML verwendet dieselbe Syntax, die im Abschnitt " [Details zum visuellen Renderingmodell](https://www.w3.org/TR/PR-CSS2/visudet.mdl) " der "CSS2"- [Spezifikation](https://www.w3.org/TR/PR-CSS2/) definiert ist, um die Größe des enthaltenden Felds anzugeben, damit der Inhalt einer Form im enthaltenden Feld gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="8995f-124">VML uses the same syntax defined in the [Visual Rendering Model Details](https://www.w3.org/TR/PR-CSS2/visudet.mdl) section of the [CSS2 specification](https://www.w3.org/TR/PR-CSS2/) to specify the size of the containing box so that the contents of a shape will be rendered (drawn) within the containing box.</span></span> <span data-ttu-id="8995f-125">Mit den Attributen **Width** und **height** können Sie die Größe des enthaltenden Felds definieren.</span><span class="sxs-lookup"><span data-stu-id="8995f-125">You can use the **width** and **height** style attributes to define the size of the containing box.</span></span>

<span data-ttu-id="8995f-126">Wenn Sie z. b. ein Oval zeichnen und **Style**= ' width: 75pt; height: 100pt ' angeben, wird das Oval innerhalb eines enthaltenden Felds mit einer Größe von 75 Punkten (Breite) um 100 Punkte (Höhe) gezeichnet, wie in der folgenden Abbildung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="8995f-126">For example, if you draw an oval and specify **style**='width:75pt;height:100pt', the oval will be drawn within a containing box at a size of 75 points (width) by 100 points (height), as shown in the following picture:</span></span>

![oval1.gif (660 bytes)](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





<span data-ttu-id="8995f-128">Wenn Sie die Größe in **Style**= "width: 120pt; height: 140pt" ändern, wird das Oval größer, da es im neuen enthaltenden Feld mit einer Größe von 120 Punkten (Breite) um 140 Punkte (Höhe) skaliert wird, wie in der folgenden Abbildung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="8995f-128">If you change the size to **style**='width:120pt;height:140pt', the oval becomes larger because it is scaled within the new containing box at a size of 120 points (width) by 140 points (height), as shown in the following picture:</span></span>

![oval2.gif (966 bytes)](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





<span data-ttu-id="8995f-130">Wenn Sie die Größe in **Style**= "width: 60pt; height: 40 PT" ändern, wird das Oval kleiner, da es im neuen enthaltenden Feld mit einer Größe von 60 Punkten (Breite) um 40 Punkte (Höhe) skaliert wird, wie in der folgenden Abbildung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="8995f-130">If you change the size to **style**='width:60pt;height:40pt', the oval becomes smaller because it is scaled within the new containing box at a size of 60 points (width) by 40 points (height), as shown in the following picture:</span></span>

![oval3.gif (394 bytes)](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 