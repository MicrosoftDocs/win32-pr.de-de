---
title: Color-Attribut (Strich) (VML)
description: Color-Attribut (Strich) (VML)
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa91522adcba5fa854d4749dc257f5489969270
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339902"
---
# <a name="color-attribute-strokevml"></a><span data-ttu-id="c7d28-103">Color-Attribut (Strich) (VML)</span><span class="sxs-lookup"><span data-stu-id="c7d28-103">Color Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="c7d28-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="c7d28-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c7d28-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="c7d28-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c7d28-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="c7d28-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c7d28-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c7d28-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c7d28-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c7d28-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c7d28-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c7d28-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c7d28-110">Definiert die Farbe eines Strichs.</span><span class="sxs-lookup"><span data-stu-id="c7d28-110">Defines the color of a stroke.</span></span> <span data-ttu-id="c7d28-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c7d28-111">Read/write.</span></span> <span data-ttu-id="c7d28-112">**Vgcolor**.</span><span class="sxs-lookup"><span data-stu-id="c7d28-112">**VgColor**.</span></span>

<span data-ttu-id="c7d28-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="c7d28-113">**Applies To**</span></span>

[<span data-ttu-id="c7d28-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="c7d28-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="c7d28-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="c7d28-115">**Tag Syntax**</span></span>

<span data-ttu-id="c7d28-116"><v: *Element* Color = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="c7d28-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="c7d28-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="c7d28-117">**Script Syntax**</span></span>

<span data-ttu-id="c7d28-118">*Element* . Color = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="c7d28-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="c7d28-119">*Ausdruck* = *Element*. Color</span><span class="sxs-lookup"><span data-stu-id="c7d28-119">*expression*=*element*.color</span></span>

<span data-ttu-id="c7d28-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="c7d28-120">**Remarks**</span></span>

<span data-ttu-id="c7d28-121">Überschreibt das **strokeColor** -Attribut einer Form.</span><span class="sxs-lookup"><span data-stu-id="c7d28-121">Overrides the **StrokeColor** attribute of a shape.</span></span> <span data-ttu-id="c7d28-122">Der Standardwert ist **schwarz**.</span><span class="sxs-lookup"><span data-stu-id="c7d28-122">The default value is **black**.</span></span>

<span data-ttu-id="c7d28-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="c7d28-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="c7d28-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="c7d28-124">**Example**</span></span>

<span data-ttu-id="c7d28-125">Die Form hat eine Strichfarbe, die **grün** ist, nicht **rot**.</span><span class="sxs-lookup"><span data-stu-id="c7d28-125">The shape has a stroke color of **green**, not **red**.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke color="green"/>
   </v:shape>
```



 

 