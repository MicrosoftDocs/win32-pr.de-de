---
title: Gruppieren von Formen
description: In diesem Artikel wird das Gruppieren von Formen in VML beschrieben, einem Feature, das seit Windows Internet Explorer 9 veraltet ist.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Web-Workshop, Gruppieren von Formen
- Entwerfen von Webseiten, Gruppieren von Formen
- Vector Markup Language (VML), Gruppieren von Formen
- VML (Vector Markup Language),Gruppieren von Formen
- Vektorgrafiken, Gruppieren von Formen
- VML-Formen, Gruppierung
- Gruppieren von Formen
- Vector Markup Language (VML),group-Element
- VML (Vector Markup Language),group-Element
- Vektorgrafik,Group-Element
- Gruppenelement
- VML-Elemente, Gruppe
- Vector Markup Language (VML), lokaler Koordinatenraum
- VML (Vector Markup Language),lokaler Koordinatenraum
- Vektorgrafiken, lokaler Koordinatenraum
- Lokaler Koordinatenraum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e0c3073f55d23c15734b5d5ddfa886e7291530
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407703"
---
# <a name="grouping-shapes"></a><span data-ttu-id="d7304-119">Gruppieren von Formen</span><span class="sxs-lookup"><span data-stu-id="d7304-119">Grouping Shapes</span></span>

<span data-ttu-id="d7304-120">In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="d7304-120">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d7304-121">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="d7304-121">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d7304-122">Seit Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="d7304-122">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d7304-123">Daher wird sie nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d7304-123">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d7304-124">Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="d7304-124">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d7304-125">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="d7304-125">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d7304-126">Wie Sie gelernt haben, können Sie mithilfe von VML ganz einfach einzelne Formen zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d7304-126">As you've learned, you can easily draw individual shapes by using VML.</span></span> <span data-ttu-id="d7304-127">In diesem Abschnitt werden die Vorteile des Gruppierens von Formen und das Gruppieren von Formen erläutert.</span><span class="sxs-lookup"><span data-stu-id="d7304-127">In this section, we will explain the benefits of grouping shapes together, and how to group shapes.</span></span>

<span data-ttu-id="d7304-128">Wenn Sie viele Formen hätten, die zusammen skaliert, verschoben oder gedreht werden mussten, wäre es mühsam, die Attribute für jede Form einzeln festlegen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="d7304-128">If you had many shapes that needed to be scaled, moved, or rotated together, you would find it tedious to set the attributes individually for each shape.</span></span> <span data-ttu-id="d7304-129">Außerdem würden Sie den Rand für Fehler erhöhen.</span><span class="sxs-lookup"><span data-stu-id="d7304-129">Plus you would raise your margin for errors.</span></span> <span data-ttu-id="d7304-130">Es wäre besser, wenn Sie die Formen gruppieren und dann die Attribute für die gesamte Gruppe festlegen könnten.</span><span class="sxs-lookup"><span data-stu-id="d7304-130">It would be better if you could group the shapes, and then set the attributes for the entire group.</span></span>

<span data-ttu-id="d7304-131">In VML können Sie das -Element verwenden, um viele Formen zu gruppieren, sodass `<group>` sie als eine Einheit transformiert werden können.</span><span class="sxs-lookup"><span data-stu-id="d7304-131">In VML, you can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span> <span data-ttu-id="d7304-132">Beispielsweise können Sie, wie in der folgenden VML-Darstellung gezeigt, problemlos zwei Formen gruppieren.</span><span class="sxs-lookup"><span data-stu-id="d7304-132">For example, as shown in the following VML representation, you can easily group two shapes together.</span></span>


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



<span data-ttu-id="d7304-133">Wenn Formen gruppiert werden, verwenden sie den [lokalen Koordinatenraum](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d7304-133">When shapes are grouped, they use the [local coordinate space](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) of the group.</span></span> <span data-ttu-id="d7304-134">Daher können Formen innerhalb einer Gruppe skaliert und zusammen verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="d7304-134">Therefore, shapes within a group can be scaled and moved together.</span></span> <span data-ttu-id="d7304-135">Weitere Beispiele finden Sie im Thema Verwenden des lokalen Koordinatenraums.</span><span class="sxs-lookup"><span data-stu-id="d7304-135">You will see more examples in the Use Local Coordinate Space topic.</span></span>

<span data-ttu-id="d7304-136">Innerhalb einer Gruppe können Sie über so viele Formen oder Gruppen verfügen, wie Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="d7304-136">Inside a group, you can have as many shapes or groups as you want.</span></span> <span data-ttu-id="d7304-137">Wenn sich eine Gruppe in einer anderen Gruppe befindet, wird sie als "geschachtelte Gruppe" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d7304-137">When a group is inside another group, it is called a "nested group".</span></span> <span data-ttu-id="d7304-138">Es gibt keine Einschränkung für die Schachtelungsebenen.</span><span class="sxs-lookup"><span data-stu-id="d7304-138">There is no limitation on the levels of nesting.</span></span>

<span data-ttu-id="d7304-139">Die folgenden Zeilen veranschaulichen beispielsweise eine geschachtelte Gruppe mit drei Ebene.</span><span class="sxs-lookup"><span data-stu-id="d7304-139">For example, the following lines demonstrate a 3-level nested group.</span></span> <span data-ttu-id="d7304-140">Shape3 und Shape4 befinden sich in GroupC.</span><span class="sxs-lookup"><span data-stu-id="d7304-140">Shape3 and Shape4 are in GroupC.</span></span> <span data-ttu-id="d7304-141">Shape2 und GroupC befinden sich in GroupB.</span><span class="sxs-lookup"><span data-stu-id="d7304-141">Shape2 and GroupC are in GroupB.</span></span> <span data-ttu-id="d7304-142">Shape1 und GroupB befinden sich in GroupA.</span><span class="sxs-lookup"><span data-stu-id="d7304-142">Shape1 and GroupB are in GroupA.</span></span>


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



<span data-ttu-id="d7304-143">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span><span class="sxs-lookup"><span data-stu-id="d7304-143">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span></span>

<span data-ttu-id="d7304-144">[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)</span><span class="sxs-lookup"><span data-stu-id="d7304-144">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="d7304-145">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d7304-145">Summary</span></span>

<span data-ttu-id="d7304-146">Sie können das `<group>` -Element verwenden, um viele Formen zu gruppieren, damit sie als eine Einheit transformiert werden können.</span><span class="sxs-lookup"><span data-stu-id="d7304-146">You can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span>

 

 