---
title: VML V-Text-Spacing-Mode-Attribut
description: VML V-Text-Spacing-Mode-Attribut
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a288f89a1405412ba8c582a5c52c7bfe56809c38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474172"
---
# <a name="vml-v-text-spacing-mode-attribute"></a><span data-ttu-id="52518-103">VML V-Text-Spacing-Mode-Attribut</span><span class="sxs-lookup"><span data-stu-id="52518-103">VML V-Text-Spacing-Mode Attribute</span></span>

<span data-ttu-id="52518-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="52518-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="52518-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="52518-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="52518-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="52518-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="52518-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="52518-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="52518-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="52518-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="52518-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="52518-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="52518-110">Definiert den Modus für Brief Abstände.</span><span class="sxs-lookup"><span data-stu-id="52518-110">Defines the mode for letterspacing.</span></span> <span data-ttu-id="52518-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="52518-111">Read/write.</span></span> <span data-ttu-id="52518-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="52518-112">**String**.</span></span>

<span data-ttu-id="52518-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="52518-113">**Applies To**</span></span>

[<span data-ttu-id="52518-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="52518-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="52518-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="52518-115">**Tag Syntax**</span></span>

<span data-ttu-id="52518-116"><v: *Element* Style = "v-Text-Spacing-Mode: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="52518-116"><v: *element* style="v-text-spacing-mode: *expression* "></span></span>

<span data-ttu-id="52518-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="52518-117">**Script Syntax**</span></span>

<span data-ttu-id="52518-118">*Element* . Style. v-Text-Spacing-Mode = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="52518-118">*element* .style.v-text-spacing-mode="*expression*"</span></span>

<span data-ttu-id="52518-119">*Ausdruck* = *Element*. Style. v-Text-Abstände-Modus</span><span class="sxs-lookup"><span data-stu-id="52518-119">*expression*=*element*.style.v-text-spacing-mode</span></span>

<span data-ttu-id="52518-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="52518-120">**Remarks**</span></span>

<span data-ttu-id="52518-121">Zu den Werten zählen</span><span class="sxs-lookup"><span data-stu-id="52518-121">Values include</span></span>

-   <span data-ttu-id="52518-122">wird **verschärft** (Standard)</span><span class="sxs-lookup"><span data-stu-id="52518-122">**tightening** (default)</span></span>
-   <span data-ttu-id="52518-123">**Paletten**</span><span class="sxs-lookup"><span data-stu-id="52518-123">**tracking**</span></span>

<span data-ttu-id="52518-124">Mit diesem Attribut wird festgelegt, ob zwischen den einzelnen Buchstaben (das Ende) oder zwischen den einzelnen Buchstaben (Nachverfolgung) ein Leerzeichen entfernt wird</span><span class="sxs-lookup"><span data-stu-id="52518-124">This attribute determines whether space will be removed between each letter (tightening) or added between each letter (tracking).</span></span> <span data-ttu-id="52518-125">Die Menge der Änderungen im Buchstaben Abstand wird durch das [V-Text-Spacing-](msdn-online-vml-v-text-spacing-attribute.md) Attribut definiert.</span><span class="sxs-lookup"><span data-stu-id="52518-125">The amount of letterspacing change is defined by the [V-Text-Spacing](msdn-online-vml-v-text-spacing-attribute.md) attribute.</span></span>

<span data-ttu-id="52518-126">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="52518-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="52518-127">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="52518-127">**Example**</span></span>

<span data-ttu-id="52518-128">Der Brief Abstand zwischen den einzelnen Buchstaben wird um 200 Einheiten angehoben.</span><span class="sxs-lookup"><span data-stu-id="52518-128">The letterspacing between each letter is increased by 200 units.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 