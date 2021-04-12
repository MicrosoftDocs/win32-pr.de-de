---
title: VML-Attribut "CropRight"
description: VML-Attribut "CropRight"
ms.assetid: 1e2bd8e8-3d56-435d-bfaf-fb07f6b6fba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21604fb341840847690e9e086386d46f7124908a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473213"
---
# <a name="vml-cropright-attribute"></a><span data-ttu-id="2adca-103">VML-Attribut "CropRight"</span><span class="sxs-lookup"><span data-stu-id="2adca-103">VML CropRight Attribute</span></span>

<span data-ttu-id="2adca-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="2adca-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2adca-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="2adca-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2adca-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="2adca-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2adca-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="2adca-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2adca-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2adca-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2adca-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2adca-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2adca-110">Definiert den Prozentsatz der Bild Entfernung von der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="2adca-110">Defines the percentage of picture removal from the right side.</span></span> <span data-ttu-id="2adca-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2adca-111">Read/write.</span></span> <span data-ttu-id="2adca-112">**Vgnumber**.</span><span class="sxs-lookup"><span data-stu-id="2adca-112">**VgNumber**.</span></span>

<span data-ttu-id="2adca-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="2adca-113">**Applies To**</span></span>

[<span data-ttu-id="2adca-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="2adca-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="2adca-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="2adca-115">**Tag Syntax**</span></span>

<span data-ttu-id="2adca-116"><v: *Element* CropRight = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="2adca-116"><v: *element* cropright=" *expression* "></span></span>

<span data-ttu-id="2adca-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="2adca-117">**Script Syntax**</span></span>

<span data-ttu-id="2adca-118">*Element* . CropRight = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="2adca-118">*element* .cropright="*expression*"</span></span>

<span data-ttu-id="2adca-119">*Ausdruck* = *Element*. CropRight</span><span class="sxs-lookup"><span data-stu-id="2adca-119">*expression*=*element*.cropright</span></span>

<span data-ttu-id="2adca-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="2adca-120">**Remarks**</span></span>

<span data-ttu-id="2adca-121">Der Wert für das Zuschneiden kann zwischen-1,0 und 1,0 liegen.</span><span class="sxs-lookup"><span data-stu-id="2adca-121">The amount of cropping can range from -1.0 to 1.0.</span></span> <span data-ttu-id="2adca-122">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="2adca-122">The default value is 0.</span></span> <span data-ttu-id="2adca-123">Beachten Sie, dass bei einem Wert von 1 überhaupt kein Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2adca-123">Note that a value of 1 will display no picture at all.</span></span> <span data-ttu-id="2adca-124">Negative Werte führen dazu, dass das Bild von der Kante, die zugeschnitten wird, nach innen gedrückt wird (der leere Bereich zwischen dem Bild und dem Rand der Kante wird durch die Füllfarbe der Form aufgefüllt).</span><span class="sxs-lookup"><span data-stu-id="2adca-124">Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape).</span></span> <span data-ttu-id="2adca-125">Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild so gestreckt wird, dass es der Form entspricht.</span><span class="sxs-lookup"><span data-stu-id="2adca-125">Positive values less than 1 will result in the remaining picture being stretched to fit the shape.</span></span>

<span data-ttu-id="2adca-126">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="2adca-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="2adca-127">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="2adca-127">**Example**</span></span>

<span data-ttu-id="2adca-128">Das Bild wird von der rechten Seite um 20% der Breite gedrückt.</span><span class="sxs-lookup"><span data-stu-id="2adca-128">The picture will be squeezed from the right side by 20% of the width.</span></span> <span data-ttu-id="2adca-129">Der leere Leerraum zwischen dem Bild und dem rechten Rand wird durch die Füllfarbe der Form aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="2adca-129">The empty space between the picture and the right edge will be filled by the fill color of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="blue"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropright="-.2" src="kids.jpg"/>
   </v:shape>
```





 

 