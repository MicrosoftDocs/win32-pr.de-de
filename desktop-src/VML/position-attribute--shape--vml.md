---
title: Position-Attribut (Form) (VML)
description: Position-Attribut (Form) (VML)
ms.assetid: 64ffe754-298b-4cf1-a236-6a4bdcd27123
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c14817ff6ac741b7fb41b1331f6d9ae32d069
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390966"
---
# <a name="position-attribute-shapevml"></a><span data-ttu-id="49851-103">Position-Attribut (Form) (VML)</span><span class="sxs-lookup"><span data-stu-id="49851-103">Position Attribute (Shape)(VML)</span></span>

<span data-ttu-id="49851-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="49851-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="49851-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="49851-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="49851-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="49851-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="49851-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="49851-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="49851-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="49851-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="49851-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="49851-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="49851-110">Definiert den Positionstyp, der zum Platzieren eines Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49851-110">Defines the type of positioning used to place an element.</span></span> <span data-ttu-id="49851-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="49851-111">Read/write.</span></span> <span data-ttu-id="49851-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="49851-112">**String**.</span></span>

<span data-ttu-id="49851-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="49851-113">**Applies To**</span></span>

[<span data-ttu-id="49851-114">Form</span><span class="sxs-lookup"><span data-stu-id="49851-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="49851-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="49851-115">**Tag Syntax**</span></span>

<span data-ttu-id="49851-116"><v: *Element* Style = "Position: *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="49851-116"><v: *element* style="position: *expression* "></span></span>

<span data-ttu-id="49851-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="49851-117">**Script Syntax**</span></span>

<span data-ttu-id="49851-118">*Element* . Style. Position = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="49851-118">*element* .style.position="*expression*"</span></span>

<span data-ttu-id="49851-119">*Ausdruck* = *Element*. Style. Position</span><span class="sxs-lookup"><span data-stu-id="49851-119">*expression*=*element*.style.position</span></span>

<span data-ttu-id="49851-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="49851-120">**Remarks**</span></span>

<span data-ttu-id="49851-121">Das **Positions** Attribut ähnelt dem standardmäßigen HTML- **Positions** Attribut, das mit Stylesheets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49851-121">The **Position** attribute is similar to the standard HTML **Position** attribute used with style sheets.</span></span>

<span data-ttu-id="49851-122">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="49851-122">Values include:</span></span>



| <span data-ttu-id="49851-123">Wert</span><span class="sxs-lookup"><span data-stu-id="49851-123">Value</span></span>    | <span data-ttu-id="49851-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49851-124">Description</span></span>                                                                                                                                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49851-125">static</span><span class="sxs-lookup"><span data-stu-id="49851-125">static</span></span>   | <span data-ttu-id="49851-126">Standard.</span><span class="sxs-lookup"><span data-stu-id="49851-126">Default.</span></span> <span data-ttu-id="49851-127">Das-Element wird gemäß dem normalen Fluss der Seite positioniert.</span><span class="sxs-lookup"><span data-stu-id="49851-127">The element is positioned according to the normal flow of the page.</span></span> <span data-ttu-id="49851-128">Die Attribute **Top** und **left** werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="49851-128">The **Top** and **Left** attributes are ignored.</span></span> <span data-ttu-id="49851-129">Wenn das Objekt Inline verankert ist, was nur in Microsoft Word geschieht, wird dieser Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="49851-129">If the object is anchored inline, which only happens in Microsoft Word, this value is used.</span></span> |
| <span data-ttu-id="49851-130">absolute</span><span class="sxs-lookup"><span data-stu-id="49851-130">absolute</span></span> | <span data-ttu-id="49851-131">Das-Element wird relativ zum übergeordneten Element positioniert, wobei die Attribute **Top** und **left** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49851-131">The element is positioned relative to the parent, using the **Top** and **Left** attributes.</span></span> <span data-ttu-id="49851-132">Dieser Wert wird von den Gleit Komma Objekten Microsoft Word und Microsoft Excel sowie von Microsoft PowerPoint-Folien verwendet.</span><span class="sxs-lookup"><span data-stu-id="49851-132">This value is used by Microsoft Word and Microsoft Excel floating objects, and Microsoft PowerPoint slides.</span></span>                  |
| <span data-ttu-id="49851-133">relative</span><span class="sxs-lookup"><span data-stu-id="49851-133">relative</span></span> | <span data-ttu-id="49851-134">Das-Element wird gemäß dem normalen Ablauf der Seite positioniert, aber die Attribute **Top** und **left** werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="49851-134">The element is positioned according to the normal flow of the page, but the **Top** and **Left** attributes are used.</span></span> <span data-ttu-id="49851-135">Die Überlappung der überlappenden Elemente wird durch das **Z-Index-** Attribut geregelt.</span><span class="sxs-lookup"><span data-stu-id="49851-135">The overlap of overlapping elements is governed by the **Z-Index** attribute.</span></span>                       |



 

<span data-ttu-id="49851-136">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="49851-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="49851-137">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="49851-137">**Example**</span></span>

<span data-ttu-id="49851-138">Die Position des Rechtecks wird mit dem *relativen* Stil angezeigt.</span><span class="sxs-lookup"><span data-stu-id="49851-138">The position of the rectangle is displayed using the *relative* style.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="49851-139">[Beispiel für das Positions Attribut](/previous-versions/bb264090(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="49851-139">[Position Attribute Example](/previous-versions/bb264090(v=vs.85)).</span></span> <span data-ttu-id="49851-140">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="49851-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 