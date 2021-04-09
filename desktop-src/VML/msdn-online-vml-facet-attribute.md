---
title: VML-facetattribut
description: VML-facetattribut
ms.assetid: 6b874d79-a34e-45f7-bbbf-44d652410b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d4fec254ff3e6af35d82cd45146c201701555b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101843"
---
# <a name="vml-facet-attribute"></a><span data-ttu-id="b773d-103">VML-facetattribut</span><span class="sxs-lookup"><span data-stu-id="b773d-103">VML Facet Attribute</span></span>

<span data-ttu-id="b773d-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="b773d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b773d-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="b773d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b773d-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="b773d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b773d-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b773d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b773d-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b773d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b773d-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b773d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b773d-110">Definiert die Anzahl von Facetten, die zum Beschreiben von Kurven Oberflächen einer-Extrusion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b773d-110">Defines the number of facets used to describe curved surfaces of an extrusion.</span></span> <span data-ttu-id="b773d-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b773d-111">Read/write.</span></span> <span data-ttu-id="b773d-112">**Vgnumber**.</span><span class="sxs-lookup"><span data-stu-id="b773d-112">**VgNumber**.</span></span>

<span data-ttu-id="b773d-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="b773d-113">**Applies To**</span></span>

[<span data-ttu-id="b773d-114">Schläuche</span><span class="sxs-lookup"><span data-stu-id="b773d-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="b773d-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="b773d-115">**Tag Syntax**</span></span>

<span data-ttu-id="b773d-116"><o: *Element* Face= " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="b773d-116"><o: *element* facet=" *expression* "></span></span>

<span data-ttu-id="b773d-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="b773d-117">**Script Syntax**</span></span>

<span data-ttu-id="b773d-118">*Element* . Face= "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="b773d-118">*element* .facet="*expression*"</span></span>

<span data-ttu-id="b773d-119">*Ausdruck* = *Element*. Facette</span><span class="sxs-lookup"><span data-stu-id="b773d-119">*expression*=*element*.facet</span></span>

<span data-ttu-id="b773d-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="b773d-120">**Remarks**</span></span>

<span data-ttu-id="b773d-121">Definiert die Art und Weise, wie sich ein Renderingmodul der Extrusion anweist.</span><span class="sxs-lookup"><span data-stu-id="b773d-121">Defines the way that a rendering engine will approximate the extrusion.</span></span> <span data-ttu-id="b773d-122">Eine niedrigere Zahl gibt eine niedrigere renderingtoleranz für die Rendering-Engine an und führt zu mehr Facetten.</span><span class="sxs-lookup"><span data-stu-id="b773d-122">A lower number will indicate a lower rendering tolerance to the rendering engine and will yield more facets.</span></span> <span data-ttu-id="b773d-123">Eine höhere Anzahl von Zahlen führt zu einer größeren Darstellung der Extrusion.</span><span class="sxs-lookup"><span data-stu-id="b773d-123">Higher numbers will make the extrusion appear more faceted.</span></span> <span data-ttu-id="b773d-124">Der Standardwert ist 30.000.</span><span class="sxs-lookup"><span data-stu-id="b773d-124">The default value is 30,000.</span></span>

<span data-ttu-id="b773d-125">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="b773d-125">*Microsoft Office Extensions Attribute*</span></span>

 

 