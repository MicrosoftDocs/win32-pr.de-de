---
title: Position-Attribut (Fill) (VML)
description: Position-Attribut (Fill) (VML)
ms.assetid: 0d532d4c-0c96-4f41-b54f-55b6aade0c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01fff487f134d50b5a72623abf21c0b5710f9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102270"
---
# <a name="position-attribute-fillvml"></a><span data-ttu-id="4f93b-103">Position-Attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="4f93b-103">Position Attribute (Fill)(VML)</span></span>

<span data-ttu-id="4f93b-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="4f93b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4f93b-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="4f93b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4f93b-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="4f93b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4f93b-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4f93b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4f93b-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4f93b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4f93b-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4f93b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4f93b-110">Definiert die Position des Füllbilds.</span><span class="sxs-lookup"><span data-stu-id="4f93b-110">Defines the position of fill image.</span></span> <span data-ttu-id="4f93b-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4f93b-111">Read/write.</span></span> <span data-ttu-id="4f93b-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="4f93b-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="4f93b-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="4f93b-113">**Applies To**</span></span>

[<span data-ttu-id="4f93b-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="4f93b-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="4f93b-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="4f93b-115">**Tag Syntax**</span></span>

<span data-ttu-id="4f93b-116"><v: *Element* Position = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="4f93b-116"><v: *element* position=" *expression* "></span></span>

<span data-ttu-id="4f93b-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="4f93b-117">**Script Syntax**</span></span>

<span data-ttu-id="4f93b-118">*Element* . Position = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="4f93b-118">*element* .position="*expression*"</span></span>

<span data-ttu-id="4f93b-119">*Ausdruck* = *Element*. Position</span><span class="sxs-lookup"><span data-stu-id="4f93b-119">*expression*=*element*.position</span></span>

<span data-ttu-id="4f93b-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="4f93b-120">**Remarks**</span></span>

<span data-ttu-id="4f93b-121">Gibt einen Punkt in der Form an, um den Ursprung des Bilds zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="4f93b-121">Specifies a point in the shape to position the origin of the image.</span></span> <span data-ttu-id="4f93b-122">Der Standardwert ist die Mitte des Container Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="4f93b-122">Default is the center of the container rectangle.</span></span> <span data-ttu-id="4f93b-123">Der Vektor ist ein Bruchteil der Breite und Höhe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="4f93b-123">The vector is a fraction of the width and height of the image.</span></span>

<span data-ttu-id="4f93b-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="4f93b-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="4f93b-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="4f93b-125">**Example**</span></span>

<span data-ttu-id="4f93b-126">Das Bild der Füllung wird direkt auf einen Punkt 50% der Breite der Form verschoben.</span><span class="sxs-lookup"><span data-stu-id="4f93b-126">The image of the fill is shifted right to a point 50% of the width of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" position="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 