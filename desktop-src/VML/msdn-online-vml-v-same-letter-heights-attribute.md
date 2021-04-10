---
title: VML-Attribut "V-gleich-Letter-Heights"
description: VML-Attribut "V-gleich-Letter-Heights"
ms.assetid: f06c0a50-1de1-47d8-8b94-01fe0599ed59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d155c3c72eb67718edd33ae601d22f8e5d074a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727761"
---
# <a name="vml-v-same-letter-heights-attribute"></a><span data-ttu-id="a520b-103">VML-Attribut "V-gleich-Letter-Heights"</span><span class="sxs-lookup"><span data-stu-id="a520b-103">VML V-Same-Letter-Heights Attribute</span></span>

<span data-ttu-id="a520b-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a520b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a520b-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="a520b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a520b-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="a520b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a520b-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a520b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a520b-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a520b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a520b-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a520b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a520b-110">Bestimmt, ob alle Buchstaben unabhängig vom ursprünglichen Fall dieselbe Höhe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a520b-110">Determines whether all letters will be the same height regardless of initial case.</span></span> <span data-ttu-id="a520b-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a520b-111">Read/write.</span></span> <span data-ttu-id="a520b-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="a520b-112">**VgTriState**.</span></span>

<span data-ttu-id="a520b-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="a520b-113">**Applies To**</span></span>

[<span data-ttu-id="a520b-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="a520b-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="a520b-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="a520b-115">**Tag Syntax**</span></span>

<span data-ttu-id="a520b-116"><v: *Element* Style = "v-same-Letter-Heights: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="a520b-116"><v: *element* style="v-same-letter-heights: *expression* "></span></span>

<span data-ttu-id="a520b-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="a520b-117">**Script Syntax**</span></span>

<span data-ttu-id="a520b-118">*Element* . Style. v-same-Letter-Höhen = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="a520b-118">*element* .style.v-same-letter-heights="*expression*"</span></span>

<span data-ttu-id="a520b-119">*Ausdruck* = *Element*. Style. v-Höhe-Letter-Höhen</span><span class="sxs-lookup"><span data-stu-id="a520b-119">*expression*=*element*.style.v-same-letter-heights</span></span>

<span data-ttu-id="a520b-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="a520b-120">**Remarks**</span></span>

<span data-ttu-id="a520b-121">**True** gibt an, dass die Kleinbuchstaben auf die Höhe der Großbuchstaben gestreckt werden.</span><span class="sxs-lookup"><span data-stu-id="a520b-121">If **True**, the lowercase letters are stretched to the height of the uppercase letters.</span></span> <span data-ttu-id="a520b-122">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="a520b-122">The default value is **False**.</span></span>

<span data-ttu-id="a520b-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="a520b-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="a520b-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="a520b-124">**Example**</span></span>

<span data-ttu-id="a520b-125">Alle Buchstaben haben unabhängig von der Groß-/Kleinschreibung dieselbe Höhe.</span><span class="sxs-lookup"><span data-stu-id="a520b-125">All letters will be the same height, regardless of case.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-same-letter-heights:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 