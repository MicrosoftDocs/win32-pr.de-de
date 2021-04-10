---
title: VML-textboxrect-Attribut
description: VML-textboxrect-Attribut
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23e955c8dc929a442fe147d5401fd597534242e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039058"
---
# <a name="vml-textboxrect-attribute"></a><span data-ttu-id="344fe-103">VML-textboxrect-Attribut</span><span class="sxs-lookup"><span data-stu-id="344fe-103">VML TextBoxRect Attribute</span></span>

<span data-ttu-id="344fe-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="344fe-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="344fe-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="344fe-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="344fe-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="344fe-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="344fe-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="344fe-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="344fe-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="344fe-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="344fe-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="344fe-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="344fe-110">Definiert ein oder mehrere Textfelder innerhalb einer Form.</span><span class="sxs-lookup"><span data-stu-id="344fe-110">Defines one or more text boxes inside a shape.</span></span> <span data-ttu-id="344fe-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="344fe-111">Read/write.</span></span> <span data-ttu-id="344fe-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="344fe-112">**String**.</span></span>

<span data-ttu-id="344fe-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="344fe-113">**Applies To**</span></span>

[<span data-ttu-id="344fe-114">Pfad</span><span class="sxs-lookup"><span data-stu-id="344fe-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="344fe-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="344fe-115">**Tag Syntax**</span></span>

<span data-ttu-id="344fe-116"><v: *Element* textboxrect = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="344fe-116"><v: *element* textboxrect=" *expression* "></span></span>

<span data-ttu-id="344fe-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="344fe-117">**Script Syntax**</span></span>

<span data-ttu-id="344fe-118">*Element* . textboxrect = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="344fe-118">*element* .textboxrect="*expression*"</span></span>

<span data-ttu-id="344fe-119">*Ausdruck* = *Element*. textboxrect</span><span class="sxs-lookup"><span data-stu-id="344fe-119">*expression*=*element*.textboxrect</span></span>

<span data-ttu-id="344fe-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="344fe-120">**Remarks**</span></span>

<span data-ttu-id="344fe-121">Ein Textfeld wird durch mindestens einen Satz von Zahlen definiert, der (in der Reihenfolge) die linken, oberen, rechten und unteren Punkte des Rechtecks angibt.</span><span class="sxs-lookup"><span data-stu-id="344fe-121">A textbox is defined by one or more sets of numbers specifying (in order) the left, top, right, and bottom points of the rectangle.</span></span> <span data-ttu-id="344fe-122">Mehrere Sätze werden durch ein Semikolon getrennt.</span><span class="sxs-lookup"><span data-stu-id="344fe-122">Multiple sets are delimited by a semicolon.</span></span> <span data-ttu-id="344fe-123">Der Standardwert ist derselbe Dimensions Wert wie das enthaltende Rechteck.</span><span class="sxs-lookup"><span data-stu-id="344fe-123">The default value is the same dimension value as the containing rectangle.</span></span> <span data-ttu-id="344fe-124">Wenn mehr als ein Textfeld definiert ist, werden die durch Trennzeichen getrennten viertsets, die jedes Textfeld definieren, durch Semikolons getrennt.</span><span class="sxs-lookup"><span data-stu-id="344fe-124">If more than one textbox is defined, the comma-delimited quadruple sets that define each textbox are separated by semicolons.</span></span> <span data-ttu-id="344fe-125">Normalerweise treten Textfelder in Sätzen von 1, 2, 3 oder 6 Rechtecke in einer Form auf.</span><span class="sxs-lookup"><span data-stu-id="344fe-125">Normally textboxes come in sets of 1, 2, 3, or 6 rectangles on a shape.</span></span>

<span data-ttu-id="344fe-126">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="344fe-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="344fe-127">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="344fe-127">**Example**</span></span>

<span data-ttu-id="344fe-128">In der linken oberen Ecke der Form wird ein text95 Feld mit einer Einheit von 95 Einheiten definiert und 5 Einheiten platziert.</span><span class="sxs-lookup"><span data-stu-id="344fe-128">A textbox of 95 units by 95 units is defined and placed 5 units inside the top left corner of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "mypath" v="m 1,1 l 1,200, 200,200, 200,1 x e"
   textboxrect="5 5 100 100"/>
   </v:shape>
```



 

 