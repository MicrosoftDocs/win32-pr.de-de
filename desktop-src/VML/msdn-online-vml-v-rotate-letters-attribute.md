---
title: VML-Attribut "V-Rotation-Letters"
description: VML-Attribut "V-Rotation-Letters"
ms.assetid: f9bd5c04-7479-4dc0-83d7-4a0bd5e2d41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9397fe8a819e9f4c8b517e1ac92e0094ad8e4458
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101710"
---
# <a name="vml-v-rotate-letters-attribute"></a><span data-ttu-id="413f6-103">VML-Attribut "V-Rotation-Letters"</span><span class="sxs-lookup"><span data-stu-id="413f6-103">VML V-Rotate-Letters Attribute</span></span>

<span data-ttu-id="413f6-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="413f6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="413f6-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="413f6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="413f6-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="413f6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="413f6-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="413f6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="413f6-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="413f6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="413f6-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="413f6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="413f6-110">Bestimmt, ob die Buchstaben des Texts gedreht werden.</span><span class="sxs-lookup"><span data-stu-id="413f6-110">Determines whether the letters of the text are rotated.</span></span> <span data-ttu-id="413f6-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="413f6-111">Read/write.</span></span> <span data-ttu-id="413f6-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="413f6-112">**VgTriState**.</span></span>

<span data-ttu-id="413f6-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="413f6-113">**Applies To**</span></span>

[<span data-ttu-id="413f6-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="413f6-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="413f6-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="413f6-115">**Tag Syntax**</span></span>

<span data-ttu-id="413f6-116"><v: *Element* Style = "v-Rotation-Letters: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="413f6-116"><v: *element* style="v-rotate-letters: *expression* "></span></span>

<span data-ttu-id="413f6-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="413f6-117">**Script Syntax**</span></span>

<span data-ttu-id="413f6-118">*Element* . Style. v-Rotation-Letters = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="413f6-118">*element* .style.v-rotate-letters="*expression*"</span></span>

<span data-ttu-id="413f6-119">*Ausdruck* = *Element*. Style. v-Rotation-Buchstaben</span><span class="sxs-lookup"><span data-stu-id="413f6-119">*expression*=*element*.style.v-rotate-letters</span></span>

<span data-ttu-id="413f6-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="413f6-120">**Remarks**</span></span>

<span data-ttu-id="413f6-121">**True** gibt an, dass die Buchstaben des Texts um 90 Grad gedreht werden.</span><span class="sxs-lookup"><span data-stu-id="413f6-121">If **True**, the letters of the text are rotated 90 degrees.</span></span> <span data-ttu-id="413f6-122">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="413f6-122">The default value is **False**.</span></span>

<span data-ttu-id="413f6-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="413f6-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="413f6-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="413f6-124">**Example**</span></span>

<span data-ttu-id="413f6-125">Die Buchstaben werden um 90 Grad gedreht.</span><span class="sxs-lookup"><span data-stu-id="413f6-125">The letters are rotated 90 degrees.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-rotate-letters:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 