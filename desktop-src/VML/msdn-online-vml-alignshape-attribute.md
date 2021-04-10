---
title: VML-alignshape-Attribut
description: VML-alignshape-Attribut
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c32a4baba060dff4a7a45ccf5a374acf33620a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316299"
---
# <a name="vml-alignshape-attribute"></a><span data-ttu-id="5fe0c-103">VML-alignshape-Attribut</span><span class="sxs-lookup"><span data-stu-id="5fe0c-103">VML AlignShape Attribute</span></span>

<span data-ttu-id="5fe0c-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="5fe0c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5fe0c-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="5fe0c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5fe0c-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="5fe0c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5fe0c-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="5fe0c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5fe0c-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5fe0c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5fe0c-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5fe0c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5fe0c-110">Bestimmt, ob ein Bild an einer Form ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="5fe0c-110">Determines whether an image will align with a shape.</span></span> <span data-ttu-id="5fe0c-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5fe0c-111">Read/write.</span></span> <span data-ttu-id="5fe0c-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="5fe0c-112">**VgTriState**.</span></span>

<span data-ttu-id="5fe0c-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="5fe0c-113">**Applies To**</span></span>

[<span data-ttu-id="5fe0c-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="5fe0c-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="5fe0c-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="5fe0c-115">**Tag Syntax**</span></span>

<span data-ttu-id="5fe0c-116"><v: *Element* alignshape = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="5fe0c-116"><v: *element* alignshape=" *expression* "></span></span>

<span data-ttu-id="5fe0c-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="5fe0c-117">**Script Syntax**</span></span>

<span data-ttu-id="5fe0c-118">*Element* . alignshape = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="5fe0c-118">*element* .alignshape="*expression*"</span></span>

<span data-ttu-id="5fe0c-119">*Ausdruck* = *Element*. alignshape</span><span class="sxs-lookup"><span data-stu-id="5fe0c-119">*expression*=*element*.alignshape</span></span>

<span data-ttu-id="5fe0c-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="5fe0c-120">**Remarks**</span></span>

<span data-ttu-id="5fe0c-121">**True** gibt an, dass das zum Erstellen der Füllung verwendete Bild an der Form ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="5fe0c-121">If **True**, the image used to create the fill is aligned with the shape.</span></span> <span data-ttu-id="5fe0c-122">Wenn der Wert **false** ist, wird das Bild, das zum Erstellen der Füllung verwendet wird, an dem Fenster ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="5fe0c-122">If **False**, the image used to create the fill is aligned with the window.</span></span> <span data-ttu-id="5fe0c-123">Der Standardwert ist **true**.</span><span class="sxs-lookup"><span data-stu-id="5fe0c-123">Default is **True**.</span></span>

<span data-ttu-id="5fe0c-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="5fe0c-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="5fe0c-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="5fe0c-125">**Example**</span></span>

<span data-ttu-id="5fe0c-126">Das aus myimage.gif erstellte Kachel Füll Bild wird am Fenster ausgerichtet, nicht an der Form. Obwohl die Form gedreht wird, ist das Bild nicht.</span><span class="sxs-lookup"><span data-stu-id="5fe0c-126">The tiled fill image created from myimage.gif is aligned with the window, not the shape; even though the shape is rotated, the image is not.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 