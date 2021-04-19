---
title: VML-Sichtbarkeits Attribut
description: VML-Sichtbarkeits Attribut
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7325d09f60da13f0c7c44e73b347fa579870fcd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342353"
---
# <a name="vml-visibility-attribute"></a><span data-ttu-id="7f983-103">VML-Sichtbarkeits Attribut</span><span class="sxs-lookup"><span data-stu-id="7f983-103">VML Visibility Attribute</span></span>

<span data-ttu-id="7f983-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="7f983-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7f983-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="7f983-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7f983-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="7f983-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7f983-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7f983-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7f983-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7f983-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7f983-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7f983-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7f983-110">Bestimmt, ob eine Form angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7f983-110">Determines whether a shape is displayed.</span></span> <span data-ttu-id="7f983-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7f983-111">Read/write.</span></span> <span data-ttu-id="7f983-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="7f983-112">**String**.</span></span>

<span data-ttu-id="7f983-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="7f983-113">**Applies To**</span></span>

[<span data-ttu-id="7f983-114">Form</span><span class="sxs-lookup"><span data-stu-id="7f983-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="7f983-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="7f983-115">**Tag Syntax**</span></span>

<span data-ttu-id="7f983-116"><v: *Element* Style = "Visibility: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="7f983-116"><v: *element* style="visibility: *expression* "></span></span>

<span data-ttu-id="7f983-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="7f983-117">**Script Syntax**</span></span>

<span data-ttu-id="7f983-118">*Element* . Style. Visibility = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="7f983-118">*element* .style.visibility="*expression*"</span></span>

<span data-ttu-id="7f983-119">*Ausdruck* = *Element*. Style. Visibility</span><span class="sxs-lookup"><span data-stu-id="7f983-119">*expression*=*element*.style.visibility</span></span>

<span data-ttu-id="7f983-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="7f983-120">**Remarks**</span></span>

<span data-ttu-id="7f983-121">Das **Visibility** -Attribut ähnelt dem Standard-HTML- **Sichtbarkeits** Attribut für Stile.</span><span class="sxs-lookup"><span data-stu-id="7f983-121">The **Visibility** attribute is similar to the standard HTML **Visibility** attribute for styles.</span></span>

<span data-ttu-id="7f983-122">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="7f983-122">Values include:</span></span>



| <span data-ttu-id="7f983-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7f983-123">Value</span></span>    | <span data-ttu-id="7f983-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f983-124">Description</span></span>                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f983-125">visible</span><span class="sxs-lookup"><span data-stu-id="7f983-125">visible</span></span>  | <span data-ttu-id="7f983-126">Die Form ist sichtbar.</span><span class="sxs-lookup"><span data-stu-id="7f983-126">The shape is visible.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="7f983-127">hidden</span><span class="sxs-lookup"><span data-stu-id="7f983-127">hidden</span></span>   | <span data-ttu-id="7f983-128">Die Form ist nicht sichtbar, aber ist noch Teil des Flusses der Objekte im Browser.</span><span class="sxs-lookup"><span data-stu-id="7f983-128">The shape is not visible, but is still part of the flow of the objects in the browser.</span></span> <span data-ttu-id="7f983-129">Mausereignisse werden nicht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="7f983-129">Mouse events are not processed.</span></span>                                                                  |
| <span data-ttu-id="7f983-130">inherit</span><span class="sxs-lookup"><span data-stu-id="7f983-130">inherit</span></span>  | <span data-ttu-id="7f983-131">Standard.</span><span class="sxs-lookup"><span data-stu-id="7f983-131">Default.</span></span> <span data-ttu-id="7f983-132">Der Sichtbarkeits Zustand wird vom übergeordneten Element der Form geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f983-132">The visibility state is inherited from the parent of the shape.</span></span> <span data-ttu-id="7f983-133">Microsoft Office Anwendungen verwenden nur " **erben** " und " **Hidden**". alle anderen Werte werden als **Vererbung** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7f983-133">Microsoft Office applications only use **inherit** and **hidden**; any other values are mapped to **inherit**.</span></span> |
| <span data-ttu-id="7f983-134">Reduzieren</span><span class="sxs-lookup"><span data-stu-id="7f983-134">collapse</span></span> | <span data-ttu-id="7f983-135">Wird für grafische Bearbeitungsanwendungen verwendet, die Gruppen von Formen reduzieren können. beispielsweise outliners.</span><span class="sxs-lookup"><span data-stu-id="7f983-135">Used for graphical editing applications that can collapse groups of shapes; for example, outliners.</span></span>                                                                                     |



 

<span data-ttu-id="7f983-136">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="7f983-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="7f983-137">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="7f983-137">**Example**</span></span>

<span data-ttu-id="7f983-138">Der folgende Code erstellt eine Form, macht Sie jedoch ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="7f983-138">The following code creates a shape but makes it hidden.</span></span> <span data-ttu-id="7f983-139">Andere Objekte im Dokument fließen um diese, sodass ein Leerzeichen die gleiche Größe wie die Form hat.</span><span class="sxs-lookup"><span data-stu-id="7f983-139">Other objects in the document will flow around it, leaving a space the same size as the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



<span data-ttu-id="7f983-140">[Beispiel für das Sichtbarkeits Attribut](/previous-versions/bb264100(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7f983-140">[Visibility Attribute Example](/previous-versions/bb264100(v=vs.85)).</span></span> <span data-ttu-id="7f983-141">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="7f983-141">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 