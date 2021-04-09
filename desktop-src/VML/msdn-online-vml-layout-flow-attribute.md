---
title: VML-Layout-Flow Attribut
description: VML-Layout-Flow Attribut
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e437e31043afcf7fba4967076a861c9bca86477
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948903"
---
# <a name="vml-layout-flow-attribute"></a><span data-ttu-id="2c07e-103">VML-Layout-Flow Attribut</span><span class="sxs-lookup"><span data-stu-id="2c07e-103">VML Layout-Flow Attribute</span></span>

<span data-ttu-id="2c07e-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="2c07e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2c07e-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="2c07e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2c07e-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="2c07e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2c07e-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="2c07e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2c07e-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2c07e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2c07e-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2c07e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2c07e-110">Bestimmt den Fluss des Textlayouts in einem Textfeld.</span><span class="sxs-lookup"><span data-stu-id="2c07e-110">Determines the flow of the text layout in a textbox.</span></span> <span data-ttu-id="2c07e-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2c07e-111">Read/write.</span></span> <span data-ttu-id="2c07e-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="2c07e-112">**String**.</span></span>

<span data-ttu-id="2c07e-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="2c07e-113">**Applies To**</span></span>

[<span data-ttu-id="2c07e-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="2c07e-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="2c07e-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="2c07e-115">**Tag Syntax**</span></span>

<span data-ttu-id="2c07e-116"><v: *Element* Style = "Layout-Flow: *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="2c07e-116"><v: *element* style="layout-flow: *expression* "></span></span>

<span data-ttu-id="2c07e-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="2c07e-117">**Remarks**</span></span>

<span data-ttu-id="2c07e-118">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="2c07e-118">Values include:</span></span>



| <span data-ttu-id="2c07e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2c07e-119">Value</span></span>                  | <span data-ttu-id="2c07e-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c07e-120">Description</span></span>                                 |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2c07e-121">Horizontal</span><span class="sxs-lookup"><span data-stu-id="2c07e-121">horizontal</span></span>             | <span data-ttu-id="2c07e-122">Der Text wird horizontal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c07e-122">Text is displayed horizontally.</span></span> <span data-ttu-id="2c07e-123">Standard.</span><span class="sxs-lookup"><span data-stu-id="2c07e-123">Default.</span></span>    |
| <span data-ttu-id="2c07e-124">Rechtes</span><span class="sxs-lookup"><span data-stu-id="2c07e-124">vertical</span></span>               | <span data-ttu-id="2c07e-125">Der Text wird vertikal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c07e-125">Text is displayed vertically.</span></span>               |
| <span data-ttu-id="2c07e-126">vertikal-ideografisch</span><span class="sxs-lookup"><span data-stu-id="2c07e-126">vertical-ideographic</span></span>   | <span data-ttu-id="2c07e-127">Ideografischer Text wird vertikal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c07e-127">Ideographic text is displayed vertically.</span></span>   |
| <span data-ttu-id="2c07e-128">horizontal-ideografisch</span><span class="sxs-lookup"><span data-stu-id="2c07e-128">horizontal-ideographic</span></span> | <span data-ttu-id="2c07e-129">Ideografischer Text wird horizontal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c07e-129">Ideographic text is displayed horizontally.</span></span> |



 

<span data-ttu-id="2c07e-130">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="2c07e-130">*VML Standard Attribute*</span></span>

<span data-ttu-id="2c07e-131">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="2c07e-131">**Example**</span></span>

<span data-ttu-id="2c07e-132">Der Text Fluss im Textfeld wird vertikal weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="2c07e-132">The text flow in the textbox will flow vertically.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <textbox string="VML text" layout-flow="vertical"/>
   </v:shape>
```



 

 