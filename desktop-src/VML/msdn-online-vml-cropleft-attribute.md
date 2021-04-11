---
title: VML-Attribut "CropLeft"
description: VML-Attribut "CropLeft"
ms.assetid: 923482f2-e3eb-4508-81d4-f19db8fcf4eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff01af761e7177d866b46ed48e5d633506aa63fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209263"
---
# <a name="vml-cropleft-attribute"></a><span data-ttu-id="262cc-103">VML-Attribut "CropLeft"</span><span class="sxs-lookup"><span data-stu-id="262cc-103">VML CropLeft Attribute</span></span>

<span data-ttu-id="262cc-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="262cc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="262cc-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="262cc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="262cc-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="262cc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="262cc-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="262cc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="262cc-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="262cc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="262cc-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="262cc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="262cc-110">Definiert den Prozentsatz der Bild Entfernung von der linken Seite.</span><span class="sxs-lookup"><span data-stu-id="262cc-110">Defines the percentage of picture removal from the left side.</span></span> <span data-ttu-id="262cc-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="262cc-111">Read/write.</span></span> <span data-ttu-id="262cc-112">**Vgnumber**.</span><span class="sxs-lookup"><span data-stu-id="262cc-112">**VgNumber**.</span></span>

<span data-ttu-id="262cc-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="262cc-113">**Applies To**</span></span>

[<span data-ttu-id="262cc-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="262cc-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="262cc-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="262cc-115">**Tag Syntax**</span></span>

<span data-ttu-id="262cc-116"><v: *Element* CropLeft = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="262cc-116"><v: *element* cropleft=" *expression* "></span></span>

<span data-ttu-id="262cc-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="262cc-117">**Script Syntax**</span></span>

<span data-ttu-id="262cc-118">*Element* . CropLeft = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="262cc-118">*element* .cropleft="*expression*"</span></span>

<span data-ttu-id="262cc-119">*Ausdruck* = *Element*. CropLeft</span><span class="sxs-lookup"><span data-stu-id="262cc-119">*expression*=*element*.cropleft</span></span>

<span data-ttu-id="262cc-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="262cc-120">**Remarks**</span></span>

<span data-ttu-id="262cc-121">Der Wert für das Zuschneiden kann zwischen-1,0 und 1,0 liegen.</span><span class="sxs-lookup"><span data-stu-id="262cc-121">The amount of cropping can range from -1.0 to 1.0.</span></span> <span data-ttu-id="262cc-122">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="262cc-122">The default value is 0.</span></span> <span data-ttu-id="262cc-123">Beachten Sie, dass bei einem Wert von 1 überhaupt kein Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="262cc-123">Note that a value of 1 will display no picture at all.</span></span> <span data-ttu-id="262cc-124">Negative Werte führen dazu, dass das Bild von der Kante, die zugeschnitten wird, nach innen gedrückt wird (der leere Bereich zwischen dem Bild und dem Rand der Kante wird durch die Füllfarbe der Form aufgefüllt).</span><span class="sxs-lookup"><span data-stu-id="262cc-124">Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape).</span></span> <span data-ttu-id="262cc-125">Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild so gestreckt wird, dass es der Form entspricht.</span><span class="sxs-lookup"><span data-stu-id="262cc-125">Positive values less than 1 will result in the remaining picture being stretched to fit the shape.</span></span>

<span data-ttu-id="262cc-126">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="262cc-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="262cc-127">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="262cc-127">**Example**</span></span>

<span data-ttu-id="262cc-128">20% des Bilds werden auf der linken Seite entfernt, und das verbleibende Bild wird gestreckt, damit es an die Form angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="262cc-128">20% of the picture will be removed on the left side and the remaining picture will be stretched to fit the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropleft=".2" src="kids.jpg"/>
   </v:shape>
```



 

 