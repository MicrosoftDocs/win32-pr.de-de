---
title: VML-Attribut "V-Text-Spacing"
description: VML-Attribut "V-Text-Spacing"
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab31d1f0b0b1d41b7e99451c422028fe54498483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390667"
---
# <a name="vml-v-text-spacing-attribute"></a><span data-ttu-id="c15ad-103">VML-Attribut "V-Text-Spacing"</span><span class="sxs-lookup"><span data-stu-id="c15ad-103">VML V-Text-Spacing Attribute</span></span>

<span data-ttu-id="c15ad-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="c15ad-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c15ad-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="c15ad-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c15ad-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="c15ad-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c15ad-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c15ad-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c15ad-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c15ad-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c15ad-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c15ad-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c15ad-110">Definiert die Größe des Abstands für Text.</span><span class="sxs-lookup"><span data-stu-id="c15ad-110">Defines the amount of spacing for text.</span></span> <span data-ttu-id="c15ad-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c15ad-111">Read/write.</span></span> <span data-ttu-id="c15ad-112">**Vgnumber**.</span><span class="sxs-lookup"><span data-stu-id="c15ad-112">**VgNumber**.</span></span>

<span data-ttu-id="c15ad-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="c15ad-113">**Applies To**</span></span>

[<span data-ttu-id="c15ad-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="c15ad-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="c15ad-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="c15ad-115">**Tag Syntax**</span></span>

<span data-ttu-id="c15ad-116"><v: *Element* Style = "v-Text-Spacing: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="c15ad-116"><v: *element* style="v-text-spacing: *expression* "></span></span>

<span data-ttu-id="c15ad-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="c15ad-117">**Script Syntax**</span></span>

<span data-ttu-id="c15ad-118">*Element* . Style. v-Text-Spacing = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="c15ad-118">*element* .style.v-text-spacing="*expression*"</span></span>

<span data-ttu-id="c15ad-119">*Ausdruck* = *Element*. Style. v-Text-Abstand</span><span class="sxs-lookup"><span data-stu-id="c15ad-119">*expression*=*element*.style.v-text-spacing</span></span>

<span data-ttu-id="c15ad-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="c15ad-120">**Remarks**</span></span>

<span data-ttu-id="c15ad-121">Der Standardwert ist 100.</span><span class="sxs-lookup"><span data-stu-id="c15ad-121">The default value is 100.</span></span> <span data-ttu-id="c15ad-122">Weitere Informationen zum Text Abstand finden Sie im [V-Text-Spacing-Mode-](msdn-online-vml-v-text-spacing-mode-attribute.md) Attribut.</span><span class="sxs-lookup"><span data-stu-id="c15ad-122">See the [V-Text-Spacing-Mode](msdn-online-vml-v-text-spacing-mode-attribute.md) attribute for more information about text spacing.</span></span>

<span data-ttu-id="c15ad-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="c15ad-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="c15ad-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="c15ad-124">**Example**</span></span>

<span data-ttu-id="c15ad-125">Der Brief Abstand zwischen den einzelnen Buchstaben wird um 200 Einheiten gestrafft.</span><span class="sxs-lookup"><span data-stu-id="c15ad-125">The letterspacing between each letter is tightened by 200 units.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 