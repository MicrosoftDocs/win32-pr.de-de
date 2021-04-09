---
title: VML-Attribut "V-Text-Reverse"
description: VML-Attribut "V-Text-Reverse"
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2625439d4b7a767a21de3578a7b15d3115a8f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039295"
---
# <a name="vml-v-text-reverse-attribute"></a><span data-ttu-id="2a154-103">VML-Attribut "V-Text-Reverse"</span><span class="sxs-lookup"><span data-stu-id="2a154-103">VML V-Text-Reverse Attribute</span></span>

<span data-ttu-id="2a154-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="2a154-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2a154-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="2a154-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2a154-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="2a154-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2a154-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="2a154-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2a154-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2a154-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2a154-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2a154-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2a154-110">Bestimmt, ob die layoutreihenfolge der Zeilen umgekehrt wird.</span><span class="sxs-lookup"><span data-stu-id="2a154-110">Determines whether the layout order of rows is reversed.</span></span> <span data-ttu-id="2a154-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2a154-111">Read/write.</span></span> <span data-ttu-id="2a154-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="2a154-112">**VgTriState**.</span></span>

<span data-ttu-id="2a154-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="2a154-113">**Applies To**</span></span>

[<span data-ttu-id="2a154-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="2a154-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="2a154-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="2a154-115">**Tag Syntax**</span></span>

<span data-ttu-id="2a154-116"><v: *Element* Style = "v-Text-Reverse: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="2a154-116"><v: *element* style="v-text-reverse: *expression* "></span></span>

<span data-ttu-id="2a154-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="2a154-117">**Script Syntax**</span></span>

<span data-ttu-id="2a154-118">*Element* . Style. v-Text-Reverse = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="2a154-118">*element* .style.v-text-reverse="*expression*"</span></span>

<span data-ttu-id="2a154-119">*Ausdruck* = *Element*. Style. v-Text-Reverse</span><span class="sxs-lookup"><span data-stu-id="2a154-119">*expression*=*element*.style.v-text-reverse</span></span>

<span data-ttu-id="2a154-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="2a154-120">**Remarks**</span></span>

<span data-ttu-id="2a154-121">**True** gibt an, dass die layoutreihenfolge der Zeilen umgekehrt wird.</span><span class="sxs-lookup"><span data-stu-id="2a154-121">If **True**, the layout order of rows is reversed.</span></span> <span data-ttu-id="2a154-122">Dieses Attribut wird für das vertikale Text Layout verwendet.</span><span class="sxs-lookup"><span data-stu-id="2a154-122">This attribute is used for vertical text layout.</span></span> <span data-ttu-id="2a154-123">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="2a154-123">The default value is **False**.</span></span>

<span data-ttu-id="2a154-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="2a154-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="2a154-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="2a154-125">**Example**</span></span>

<span data-ttu-id="2a154-126">Die layoutreihenfolge wird umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="2a154-126">The layout order is reversed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-reverse:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 