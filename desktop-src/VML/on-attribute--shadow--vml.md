---
title: On-Attribut (Schatten) (VML)
description: On-Attribut (Schatten) (VML)
ms.assetid: 234fe63e-8a4a-4067-9d05-a8990d1cee5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83df69d8c90c99839f55836941746717a205d07a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948949"
---
# <a name="on-attribute-shadowvml"></a><span data-ttu-id="e188d-103">On-Attribut (Schatten) (VML)</span><span class="sxs-lookup"><span data-stu-id="e188d-103">On Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="e188d-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="e188d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e188d-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="e188d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e188d-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="e188d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e188d-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e188d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e188d-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e188d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e188d-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e188d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e188d-110">Bestimmt, ob ein Schatten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e188d-110">Determines whether a shadow will be displayed.</span></span> <span data-ttu-id="e188d-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e188d-111">Read/write.</span></span> <span data-ttu-id="e188d-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="e188d-112">**VgTriState**.</span></span>

<span data-ttu-id="e188d-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="e188d-113">**Applies To**</span></span>

[<span data-ttu-id="e188d-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="e188d-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="e188d-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="e188d-115">**Tag Syntax**</span></span>

<span data-ttu-id="e188d-116"><v: *Element* on = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e188d-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="e188d-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="e188d-117">**Script Syntax**</span></span>

<span data-ttu-id="e188d-118">*Element* . on = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="e188d-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="e188d-119">*Ausdruck* = *Element*. on</span><span class="sxs-lookup"><span data-stu-id="e188d-119">*expression*=*element*.on</span></span>

<span data-ttu-id="e188d-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="e188d-120">**Remarks**</span></span>

<span data-ttu-id="e188d-121">**True** gibt an, dass der Schatten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e188d-121">If **True**, the shadow will be displayed.</span></span> <span data-ttu-id="e188d-122">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="e188d-122">The default value is **False**.</span></span>

<span data-ttu-id="e188d-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="e188d-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="e188d-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="e188d-124">**Example**</span></span>

<span data-ttu-id="e188d-125">Der Schatten wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e188d-125">The shadow will be displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True"/>
   </v:shape>
```





 

 