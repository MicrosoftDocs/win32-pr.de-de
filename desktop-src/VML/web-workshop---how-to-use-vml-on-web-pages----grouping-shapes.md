---
title: Gruppieren von Formen
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Webworkshop, Gruppieren von Formen
- Entwerfen von Webseiten, Gruppieren von Formen
- Vector Markup Language (VML), Gruppieren von Formen
- VML (Vector Markup Language), Gruppieren von Formen
- Vektorgrafiken, Gruppierungs Formen
- VML-Formen, gruppieren
- Gruppieren von Formen
- Vector Markup Language (VML), Group-Element
- VML (Vector Markup Language), Group-Element
- Vektorgrafiken, Group-Element
- Gruppenelement
- VML-Elemente,-Gruppe
- Vector Markup Language (VML), lokaler Koordinaten Bereich
- VML (Vector Markup Language), lokaler Koordinaten Bereich
- Vektorgrafiken, lokaler Koordinatenraum
- lokaler Koordinaten Bereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59eed282094e2d24d2d27e338b93731eaaa1eec0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039508"
---
# <a name="grouping-shapes"></a><span data-ttu-id="bbe66-120">Gruppieren von Formen</span><span class="sxs-lookup"><span data-stu-id="bbe66-120">Grouping Shapes</span></span>

<span data-ttu-id="bbe66-121">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="bbe66-121">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bbe66-122">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="bbe66-122">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bbe66-123">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="bbe66-123">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bbe66-124">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="bbe66-124">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bbe66-125">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bbe66-125">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bbe66-126">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bbe66-126">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bbe66-127">Wie Sie gelernt haben, können Sie einfach einzelne Formen mithilfe von VML zeichnen.</span><span class="sxs-lookup"><span data-stu-id="bbe66-127">As you've learned, you can easily draw individual shapes by using VML.</span></span> <span data-ttu-id="bbe66-128">In diesem Abschnitt werden die Vorteile der Gruppierung von Formen und das Gruppieren von Formen erläutert.</span><span class="sxs-lookup"><span data-stu-id="bbe66-128">In this section, we will explain the benefits of grouping shapes together, and how to group shapes.</span></span>

<span data-ttu-id="bbe66-129">Wenn Sie über viele Formen verfügen, die skaliert, verschoben oder gedreht werden mussten, wäre es mühsam, die Attribute für jede Form einzeln festzulegen.</span><span class="sxs-lookup"><span data-stu-id="bbe66-129">If you had many shapes that needed to be scaled, moved, or rotated together, you would find it tedious to set the attributes individually for each shape.</span></span> <span data-ttu-id="bbe66-130">Außerdem würden Sie den Rand für Fehler erhöhen.</span><span class="sxs-lookup"><span data-stu-id="bbe66-130">Plus you would raise your margin for errors.</span></span> <span data-ttu-id="bbe66-131">Es wäre besser, wenn Sie die Formen gruppieren und dann die Attribute für die gesamte Gruppe festlegen.</span><span class="sxs-lookup"><span data-stu-id="bbe66-131">It would be better if you could group the shapes, and then set the attributes for the entire group.</span></span>

<span data-ttu-id="bbe66-132">In VML können Sie das- `<group>` Element verwenden, um viele Formen zu gruppieren, sodass Sie als eine Einheit transformiert werden können.</span><span class="sxs-lookup"><span data-stu-id="bbe66-132">In VML, you can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span> <span data-ttu-id="bbe66-133">Beispielsweise können Sie, wie in der folgenden VML-Darstellung gezeigt, zwei Formen problemlos gruppieren.</span><span class="sxs-lookup"><span data-stu-id="bbe66-133">For example, as shown in the following VML representation, you can easily group two shapes together.</span></span>


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



<span data-ttu-id="bbe66-134">Wenn Formen gruppiert sind, verwenden Sie den [lokalen Koordinaten Bereich](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="bbe66-134">When shapes are grouped, they use the [local coordinate space](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) of the group.</span></span> <span data-ttu-id="bbe66-135">Daher können Formen innerhalb einer Gruppe skaliert und gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="bbe66-135">Therefore, shapes within a group can be scaled and moved together.</span></span> <span data-ttu-id="bbe66-136">Weitere Beispiele finden Sie im Thema Verwenden von lokalem Koordinatenraum.</span><span class="sxs-lookup"><span data-stu-id="bbe66-136">You will see more examples in the Use Local Coordinate Space topic.</span></span>

<span data-ttu-id="bbe66-137">Innerhalb einer Gruppe können Sie beliebig viele Formen oder Gruppen haben.</span><span class="sxs-lookup"><span data-stu-id="bbe66-137">Inside a group, you can have as many shapes or groups as you want.</span></span> <span data-ttu-id="bbe66-138">Wenn sich eine Gruppe in einer anderen Gruppe befindet, wird Sie als "geschachtelte Gruppe" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbe66-138">When a group is inside another group, it is called a "nested group".</span></span> <span data-ttu-id="bbe66-139">Es gibt keine Einschränkung für die Schachtelungs Ebenen.</span><span class="sxs-lookup"><span data-stu-id="bbe66-139">There is no limitation on the levels of nesting.</span></span>

<span data-ttu-id="bbe66-140">In den folgenden Zeilen wird z. b. eine Gruppierungs Gruppe mit drei Ebenen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="bbe66-140">For example, the following lines demonstrate a 3-level nested group.</span></span> <span data-ttu-id="bbe66-141">Shape3 und Shape4 befinden sich in groupc.</span><span class="sxs-lookup"><span data-stu-id="bbe66-141">Shape3 and Shape4 are in GroupC.</span></span> <span data-ttu-id="bbe66-142">Shape2 und groupc sind in GroupB.</span><span class="sxs-lookup"><span data-stu-id="bbe66-142">Shape2 and GroupC are in GroupB.</span></span> <span data-ttu-id="bbe66-143">Shape1 und GroupB sind in groupA.</span><span class="sxs-lookup"><span data-stu-id="bbe66-143">Shape1 and GroupB are in GroupA.</span></span>


```HTML
<body>
   <v:group id="GroupA"...>
      <v:shape id="Shape1"...></v:shape>
      <v:group id="GroupB"...>
         <v:shape id="Shape2"...></v:shape>
         <v:group id="GroupC"...>
            <v:shape id="Shape3"...></v:shape>
            <v:shape id="Shape4"...></v:shape>
         </v:group>
      </v:group>
   </v:group>
</body>
```



<span data-ttu-id="bbe66-144">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span><span class="sxs-lookup"><span data-stu-id="bbe66-144">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span></span>

<span data-ttu-id="bbe66-145">[![zurück ](images/top.gif) zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="bbe66-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="bbe66-146">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="bbe66-146">Summary</span></span>

<span data-ttu-id="bbe66-147">Sie können das- `<group>` Element verwenden, um viele Formen zu gruppieren, sodass Sie als eine Einheit transformiert werden können.</span><span class="sxs-lookup"><span data-stu-id="bbe66-147">You can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span>

 

 