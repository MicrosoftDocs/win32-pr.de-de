---
title: VML gradientshapeok-Attribut
description: VML gradientshapeok-Attribut
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1b7c215fbe0b98c11f7e4d33301e81798bd37f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390921"
---
# <a name="vml-gradientshapeok-attribute"></a><span data-ttu-id="4ff34-103">VML gradientshapeok-Attribut</span><span class="sxs-lookup"><span data-stu-id="4ff34-103">VML GradientShapeOK Attribute</span></span>

<span data-ttu-id="4ff34-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="4ff34-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4ff34-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="4ff34-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4ff34-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="4ff34-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4ff34-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4ff34-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4ff34-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4ff34-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4ff34-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4ff34-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4ff34-110">Bestimmt, ob ein Farbverlaufs Pfad aus wiederholten konzentrischen Pfaden besteht.</span><span class="sxs-lookup"><span data-stu-id="4ff34-110">Determines whether a gradient path will be made up of repeated concentric paths.</span></span> <span data-ttu-id="4ff34-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4ff34-111">Read/write.</span></span> <span data-ttu-id="4ff34-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="4ff34-112">**VgTriState**.</span></span>

<span data-ttu-id="4ff34-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="4ff34-113">**Applies To**</span></span>

[<span data-ttu-id="4ff34-114">Pfad</span><span class="sxs-lookup"><span data-stu-id="4ff34-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="4ff34-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="4ff34-115">**Tag Syntax**</span></span>

<span data-ttu-id="4ff34-116"><v: *Element* gradientshapeok = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="4ff34-116"><v: *element* gradientshapeok=" *expression* "></span></span>

<span data-ttu-id="4ff34-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="4ff34-117">**Script Syntax**</span></span>

<span data-ttu-id="4ff34-118">*Element* . gradientshapeok = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="4ff34-118">*element* .gradientshapeok="*expression*"</span></span>

<span data-ttu-id="4ff34-119">*Ausdruck* = *Element*. gradientshapeok</span><span class="sxs-lookup"><span data-stu-id="4ff34-119">*expression*=*element*.gradientshapeok</span></span>

<span data-ttu-id="4ff34-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="4ff34-120">**Remarks**</span></span>

<span data-ttu-id="4ff34-121">**True** gibt an, dass der Pfad mit einer konzentrischen Farbverlaufsfüllung gefüllt wird, wobei der Pfad als wiederholte Form des Farbverlaufs verwendet wird. Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="4ff34-121">If **True**, the path will be filled with a concentric gradient fill using the path as the repeated shape of the gradient.The default is **False**.</span></span>

<span data-ttu-id="4ff34-122">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="4ff34-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="4ff34-123">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="4ff34-123">**Example**</span></span>

<span data-ttu-id="4ff34-124">Der Pfad wird mit einer konzentrischen Verlaufs Füllung aufgefüllt, die aus wiederholten Rechtecke besteht.</span><span class="sxs-lookup"><span data-stu-id="4ff34-124">The path will be filled with a concentric gradient fill made up of repeated rectangles.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 