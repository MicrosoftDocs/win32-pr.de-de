---
title: VML-V-Text-Kern-Attribut
description: VML-V-Text-Kern-Attribut
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b20eab11cc24cd7580b68de8acf86468fb1d16a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948950"
---
# <a name="vml-v-text-kern-attribute"></a><span data-ttu-id="77363-103">VML-V-Text-Kern-Attribut</span><span class="sxs-lookup"><span data-stu-id="77363-103">VML V-Text-Kern Attribute</span></span>

<span data-ttu-id="77363-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="77363-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="77363-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="77363-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="77363-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="77363-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="77363-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="77363-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="77363-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="77363-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="77363-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="77363-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="77363-110">Bestimmt, ob die kernung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="77363-110">Determines whether kerning is turned on.</span></span> <span data-ttu-id="77363-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="77363-111">Read/write.</span></span> <span data-ttu-id="77363-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="77363-112">**VgTriState**.</span></span>

<span data-ttu-id="77363-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="77363-113">**Applies To**</span></span>

[<span data-ttu-id="77363-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="77363-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="77363-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="77363-115">**Tag Syntax**</span></span>

<span data-ttu-id="77363-116"><v: *Element* Style = "v-Text-Kern: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="77363-116"><v: *element* style="v-text-kern: *expression* "></span></span>

<span data-ttu-id="77363-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="77363-117">**Script Syntax**</span></span>

<span data-ttu-id="77363-118">*Element* . Style. v-Text-Kern = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="77363-118">*element* .style.v-text-kern="*expression*"</span></span>

<span data-ttu-id="77363-119">*Ausdruck* = *Element*. Style. v-Text-Kern</span><span class="sxs-lookup"><span data-stu-id="77363-119">*expression*=*element*.style.v-text-kern</span></span>

<span data-ttu-id="77363-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="77363-120">**Remarks**</span></span>

<span data-ttu-id="77363-121">**True** gibt an, dass die kernung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="77363-121">If **True**, the kerning is turned on.</span></span> <span data-ttu-id="77363-122">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="77363-122">The default is **False**.</span></span> <span data-ttu-id="77363-123">Die kernung ist das Entfernen von Leerzeichen zwischen bestimmten Brief Paaren, um ungleichmäßige letterforms auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="77363-123">Kerning is the removal of space between certain letter pairs to compensate for uneven letterforms.</span></span> <span data-ttu-id="77363-124">Wenn z. b. die kerif-Aktivierung aktiviert ist, wird zusätzlicher Speicherplatz zwischen dem Großbuchstaben "T" und dem Kleinbuchstaben "i" entfernt.</span><span class="sxs-lookup"><span data-stu-id="77363-124">For example, if kerning is turned on, extra space between a capital "T" and a lowercase "i" would be removed.</span></span>

<span data-ttu-id="77363-125">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="77363-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="77363-126">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="77363-126">**Example**</span></span>

<span data-ttu-id="77363-127">Die kernung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="77363-127">Kerning is turned on.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 