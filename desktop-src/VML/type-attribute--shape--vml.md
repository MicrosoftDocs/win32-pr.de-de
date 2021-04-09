---
title: Type-Attribut (Form) (VML)
description: Type-Attribut (Form) (VML)
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e53b275d6b6327b3d3783704dbd06156e643f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039148"
---
# <a name="type-attribute-shapevml"></a><span data-ttu-id="03eed-103">Type-Attribut (Form) (VML)</span><span class="sxs-lookup"><span data-stu-id="03eed-103">Type Attribute (Shape)(VML)</span></span>

<span data-ttu-id="03eed-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="03eed-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="03eed-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="03eed-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="03eed-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="03eed-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="03eed-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="03eed-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="03eed-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="03eed-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="03eed-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="03eed-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="03eed-110">Definiert einen Verweis auf die ID eines [ShapeType](msdn-online-vml-shapetype-element.md) -Elements.</span><span class="sxs-lookup"><span data-stu-id="03eed-110">Defines a reference to the ID of a [ShapeType](msdn-online-vml-shapetype-element.md) element.</span></span> <span data-ttu-id="03eed-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="03eed-111">Read/write.</span></span> <span data-ttu-id="03eed-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="03eed-112">**String**.</span></span>

<span data-ttu-id="03eed-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="03eed-113">**Applies To**</span></span>

[<span data-ttu-id="03eed-114">Form</span><span class="sxs-lookup"><span data-stu-id="03eed-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="03eed-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="03eed-115">**Tag Syntax**</span></span>

``` syntax
<v:
          element 
          type=" expression ">
```

<span data-ttu-id="03eed-116">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="03eed-116">**Script Syntax**</span></span>

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

<span data-ttu-id="03eed-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="03eed-117">**Remarks**</span></span>

<span data-ttu-id="03eed-118">Wenn das **Type** -Attribut auf die ID eines **ShapeType** -Elements verweist, werden die Füllungen, Pfade und Striche des **ShapeType** als Vorlagen verwendet, um die Form zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="03eed-118">If the **Type** attribute references the ID of a **ShapeType** element, the fills, paths, and strokes of the **ShapeType** are used as templates to create the shape.</span></span> <span data-ttu-id="03eed-119">Werte, die von **ShapeType** abgeleitet werden, können von einzelnen Form Werten überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="03eed-119">Values derived from **ShapeType** can be overridden by individual shape values.</span></span>

<span data-ttu-id="03eed-120">Bei Verwendung in Tags muss der Zeichen folgen Wert mit einem Nummern Zeichen ( \# ) beginnen.</span><span class="sxs-lookup"><span data-stu-id="03eed-120">If used in tags, the string value must begin with a number sign (\#) symbol.</span></span>

<span data-ttu-id="03eed-121">**VML-Standard Attribut**</span><span class="sxs-lookup"><span data-stu-id="03eed-121">**VML Standard Attribute**</span></span>

<span data-ttu-id="03eed-122">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="03eed-122">**Example**</span></span>

<span data-ttu-id="03eed-123">Eine **ShapeType** -Form wird mit dem "MyType" als ID erstellt.</span><span class="sxs-lookup"><span data-stu-id="03eed-123">A **ShapeType** shape is created with the "mytype" as an ID.</span></span>


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



<span data-ttu-id="03eed-124">Wenn Sie dann eine Form mithilfe der **ShapeType** -Werte erstellen, weist die Form die Attribute des **ShapeType**"MyType" auf. Das heißt, "shape01" hat eine rote Füllung mit einem blauen Strich.</span><span class="sxs-lookup"><span data-stu-id="03eed-124">Then if you create a shape using the **ShapeType** values, the shape will have the attributes of the "mytype" **ShapeType**; that is, "shape01" will have a red fill with a blue stroke.</span></span>


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



<span data-ttu-id="03eed-125">Sie können die geerbten Werte überschreiben, indem Sie z. b. die Farbe in grün ändern.</span><span class="sxs-lookup"><span data-stu-id="03eed-125">You can override the inherited values, for example, by changing the color to green.</span></span>


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



<span data-ttu-id="03eed-126">[Beispiel für Typattribut](/previous-versions/bb264099(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03eed-126">[Type Attribute Example](/previous-versions/bb264099(v=vs.85)).</span></span> <span data-ttu-id="03eed-127">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="03eed-127">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 