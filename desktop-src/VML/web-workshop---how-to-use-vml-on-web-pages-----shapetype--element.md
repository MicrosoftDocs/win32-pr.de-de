---
title: Verwenden des ShapeType-Elements
description: Verwenden des ShapeType-Elements
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- Webworkshop, ShapeType-Element
- Entwerfen von Webseiten, ShapeType-Element
- Vector Markup Language (VML), ShapeType-Element
- VML (Vector Markup Language), ShapeType-Element
- Vektorgrafiken, ShapeType-Element
- ShapeType-Element
- VML-Elemente, ShapeType
- VML-Formen, ShapeType-Element
- Vector Markup Language (VML), definieren häufig verwendeter Formen
- VML (Vector Markup Language), definieren häufig verwendeter Formen
- Vektorgrafiken, definieren häufig verwendeter Formen
- definieren häufig verwendeter Formen
- VML-Formen, häufig verwendete definieren
- Vector Markup Language (VML), Instanziieren von Kopien von Formen
- VML (Vector Markup Language), Instanziieren von Kopien von Formen
- Vektorgrafiken, Instanziieren von Kopien von Formen
- Instanziieren von Kopien von Formen
- VML-Formen, instanziieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa7ec47dde492231e8bcd54f68e4637454613b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474013"
---
# <a name="using-the-shapetype-element"></a><span data-ttu-id="d6df6-121">Verwenden des ShapeType-Elements</span><span class="sxs-lookup"><span data-stu-id="d6df6-121">Using the Shapetype Element</span></span>

<span data-ttu-id="d6df6-122">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="d6df6-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d6df6-123">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="d6df6-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d6df6-124">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="d6df6-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d6df6-125">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d6df6-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d6df6-126">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d6df6-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d6df6-127">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d6df6-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d6df6-128">In diesem Thema wird veranschaulicht, wie `<shapetype>` Sie das-Element verwenden, um Ihre eigenen häufig verwendeten Formen zu definieren und dann Formen aus dem ShapeType zu instanziieren oder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d6df6-128">In this topic, we will illustrate how to use the `<shapetype>` element to define your own frequently-used shapes and then instantiate, or create, shapes from the shapetype.</span></span>

<span data-ttu-id="d6df6-129">Wenn Sie viele Formen zeichnen möchten, die die gleichen oder ähnliche Eigenschaften aufweisen, wäre es mühsam, wenn Sie für jede Form wiederholt dieselben Eigenschafts Attribute eingeben müssten.</span><span class="sxs-lookup"><span data-stu-id="d6df6-129">If you wanted to draw many shapes that have the same or similar properties, it would be tedious if you had to repeatedly type the same property attributes for each shape.</span></span> <span data-ttu-id="d6df6-130">VML stellt das- `<shapetype>` Element bereit, sodass Sie einen Prototyp einer Form definieren können.</span><span class="sxs-lookup"><span data-stu-id="d6df6-130">VML provides the `<shapetype>` element so that you can define a prototype of a shape.</span></span> <span data-ttu-id="d6df6-131">Anschließend können Sie das- `<shape>` Element verwenden, um viele Kopien von Formen aus demselben ShapeType zu instanziieren.</span><span class="sxs-lookup"><span data-stu-id="d6df6-131">You can then use the `<shape>` element to instantiate many copies of shapes from the same shapetype.</span></span>

<span data-ttu-id="d6df6-132">Sie können die drei Schritte ausführen, um einen ShapeType zu definieren, und dann eine Form aus dem ShapeType instanziieren:</span><span class="sxs-lookup"><span data-stu-id="d6df6-132">You can follow the three steps to define a shapetype, and then instantiate a shape from the shapetype:</span></span>

1.  <span data-ttu-id="d6df6-133">`<shapetype>`Geben Sie ein-Element ein, und benennen Sie es durch Angeben des ID-Attributs.</span><span class="sxs-lookup"><span data-stu-id="d6df6-133">Type a `<shapetype>` element and give it a name by specifying the id attribute.</span></span>
2.  <span data-ttu-id="d6df6-134">Beschreiben Sie den ShapeType mithilfe der Eigenschafts Attribute oder untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="d6df6-134">Describe the shapetype by using its property attributes or sub-elements.</span></span>
3.  <span data-ttu-id="d6df6-135">Instanziieren Sie eine Form, indem `<shape>` Sie ein-Element eingeben und das Type-Attribut der Form auf das ID-Attribut des ShapeType-Elements verweisen.</span><span class="sxs-lookup"><span data-stu-id="d6df6-135">Instantiate a shape by typing a `<shape>` element, and refer the type attribute of the shape to the id attribute of the shapetype.</span></span>

<span data-ttu-id="d6df6-136">Beispielsweise geben Sie die folgenden Zeilen ein, um einen ShapeType mit dem Namen "myShape" zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="d6df6-136">For example, you type the following lines to create a shapetype called "MyShape":</span></span>


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



<span data-ttu-id="d6df6-137">Anschließend ändern Sie den ShapeType, indem Sie einige Eigenschafts Attribute festlegen, z `fillcolor="red" strokecolor="blue"` . b..</span><span class="sxs-lookup"><span data-stu-id="d6df6-137">Then, you alter the shapetype by setting some property attributes, such as `fillcolor="red" strokecolor="blue"`.</span></span> <span data-ttu-id="d6df6-138">Oder Sie können unter Elemente innerhalb des ShapeType verwenden, z `<path>` . b., `<fill>` , `<stroke>` (wir werden diese unter Elemente in späteren Themen besprechen).</span><span class="sxs-lookup"><span data-stu-id="d6df6-138">Or, you can use sub-elements inside the shapetype, such as `<path>`, `<fill>`, `<stroke>` (we will talk about those sub-elements in later topics).</span></span>


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



<span data-ttu-id="d6df6-139">Dann Instanziieren Sie eine Form aus dem ShapeType "myShape", indem Sie angeben `type="#MyShape"` , wie in der folgenden VML-Darstellung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6df6-139">Then, you instantiate a shape from the shapetype "MyShape" by specifying `type="#MyShape"`, as shown in the following VML representation.</span></span> <span data-ttu-id="d6df6-140">Diese Form erbt alle Eigenschaften aus dem ShapeType "myShape" und wird in dem enthaltenden Feld mit einer Größe von 100 x 80 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6df6-140">This shape inherits all properties from the shapetype "MyShape", and is displayed within its containing box at a size of 100 by 80.</span></span>


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



<span data-ttu-id="d6df6-141">Sie können eine andere Form aus dem ShapeType "myShape" instanziieren, indem Sie `type="#MyShape"` einige Eigenschaften wie in der folgenden VML-Darstellung angeben und überschreiben, wie `fillcolor="maroon"` in der folgenden VML-Darstellung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6df6-141">You can instantiate another shape from the shapetype "MyShape" by specifying `type="#MyShape"` and overwrite some properties, such as `fillcolor="maroon"`, as shown in the following VML representation.</span></span> <span data-ttu-id="d6df6-142">Diese Form erbt alle Eigenschaften aus dem ShapeType "myShape" mit Ausnahme der FillColor-Eigenschaft und wird innerhalb des enthaltenden Felds mit einer Größe von 70 x 90 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6df6-142">This shape inherits all properties from the shapetype "MyShape" except the fillcolor property, and is displayed within its containing box at a size of 70 by 90.</span></span>


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



<span data-ttu-id="d6df6-143">Im folgenden finden Sie die komplette VML-Darstellung für das vorherige Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d6df6-143">Here is the complete VML representation for the preceding example:</span></span>

![Typ1 \-1.gif (477 bytes)](images/type1-1.gif)![Typ1 \-2.gif (471 bytes)](images/type1-2.gif)


```HTML
<body>
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue" coordsize="21600,21600"
path="m10860,2187c10451,1746,9529,1018,9015,730,7865,152,6685,,5415,,4175,
152,2995,575,1967,1305,1150,2187,575,3222,242,4220,,5410,242,6560,575,7597l10860,
21600,20995,7597c21480,6560,21600,5410,21480,4220,21115,3222,20420,2187,19632,
1305,18575,575,17425,152,16275,,15005,,13735,152,12705,730,12176,1018,11254,1746,
10860,2187xe">
</v:shapetype>
<v:shape type="#MyShape" style='width:100;height:80;'/>
<v:shape type="#MyShape" style='width:70;height:90;' fillcolor="maroon"/>
</body>
```





<span data-ttu-id="d6df6-146">Wenn eine Form von einem ShapeType-Objekt instanziiert wird, erbt Sie alle Eigenschafts Attribute aus dem ShapeType.</span><span class="sxs-lookup"><span data-stu-id="d6df6-146">As you've learned, when a shape is instantiated from a shapetype, it inherits all of the property attributes from the shapetype.</span></span> <span data-ttu-id="d6df6-147">Sie können einige oder alle geerbten Attribute überschreiben, indem Sie Attribute innerhalb des `<shape>` Elements neu definieren.</span><span class="sxs-lookup"><span data-stu-id="d6df6-147">You can overwrite some or all of the inherited attributes by redefining attributes inside the `<shape>` element.</span></span> <span data-ttu-id="d6df6-148">Beachten Sie, dass die Vererbung nur eine Ebene ist.</span><span class="sxs-lookup"><span data-stu-id="d6df6-148">Be aware that the inheritance is only one level.</span></span> <span data-ttu-id="d6df6-149">Dies liegt daran, dass nur ein- `<shape>` Element auf ein-Element verweisen kann `<shapetype>` .</span><span class="sxs-lookup"><span data-stu-id="d6df6-149">This is because only a `<shape>` element can reference a `<shapetype>` element.</span></span> <span data-ttu-id="d6df6-150">Ein- `<shapetype>` Element kann nicht auf ein anderes `<shapetype>` Element verweisen.</span><span class="sxs-lookup"><span data-stu-id="d6df6-150">A `<shapetype>` element cannot reference another `<shapetype>` element.</span></span>

<span data-ttu-id="d6df6-151">Außerdem gehört ein ShapeType keiner Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="d6df6-151">Also, a shapetype doesn't belong to any group.</span></span> <span data-ttu-id="d6df6-152">Daher kann das- `<shapetype>` Element allein oder innerhalb eines-Elements angezeigt werden `<group>` .</span><span class="sxs-lookup"><span data-stu-id="d6df6-152">Therefore, the `<shapetype>` element can appear by itself or inside a `<group>` element.</span></span> <span data-ttu-id="d6df6-153">Sie können viele Formen innerhalb verschiedener Gruppen haben, die auf denselben ShapeType verweisen.</span><span class="sxs-lookup"><span data-stu-id="d6df6-153">You can have many shapes inside different groups that reference the same shapetype.</span></span> <span data-ttu-id="d6df6-154">Wenn ein ShapeType innerhalb einer Gruppe angezeigt wird, kann eine Form, die in einer anderen Gruppe lebt, weiterhin auf diesen ShapeType verweisen.</span><span class="sxs-lookup"><span data-stu-id="d6df6-154">If a shapetype appears inside a group, a shape living in another group can still reference this shapetype.</span></span>

<span data-ttu-id="d6df6-155">In der folgenden VML-Darstellung sind z. b. Rect1 und Rect2 in groupA und Rect3 in GroupB.</span><span class="sxs-lookup"><span data-stu-id="d6df6-155">For example, in the following VML representation, Rect1 and Rect2 are in GroupA, and Rect3 is in GroupB.</span></span> <span data-ttu-id="d6df6-156">Alle drei Rechtecke werden von myShape ShapeType instanziiert.</span><span class="sxs-lookup"><span data-stu-id="d6df6-156">All three rectangles are instantiated from MyShape shapetype.</span></span>


```HTML
<body>
...
<v:shapetype id="MyShape" fillcolor="blue" strokecolor="red"...>
</v:shapetype>

<v:group id="GroupA"...>
<v:shape id="Rect1" type="#MyShape" .../>
<v:shape id="Rect2" type="#MyShape" strokecolor="black".../>
</v:group>

<v:group id="GroupB"...>
<v:shape id="Rect3" type="#MyShape" fillcolor="green".../>
</v:group>
...
</body>
```



<span data-ttu-id="d6df6-157">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858387) .</span><span class="sxs-lookup"><span data-stu-id="d6df6-157">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858387) .</span></span>

 

 