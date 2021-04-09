---
title: Type-Attribut (Extrusion) (VML)
description: Type-Attribut (Extrusion) (VML)
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14bc91f9348603bc89189debb2255f8fff39e135
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858359"
---
# <a name="type-attribute-extrusionvml"></a><span data-ttu-id="9d9e6-103">Type-Attribut (Extrusion) (VML)</span><span class="sxs-lookup"><span data-stu-id="9d9e6-103">Type Attribute (Extrusion)(VML)</span></span>

<span data-ttu-id="9d9e6-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="9d9e6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9d9e6-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="9d9e6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9d9e6-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="9d9e6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9d9e6-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="9d9e6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9d9e6-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9d9e6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9d9e6-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9d9e6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9d9e6-110">Definiert die Art und Weise, in der die Form extrudiert wird.</span><span class="sxs-lookup"><span data-stu-id="9d9e6-110">Defines the way that the shape is extruded.</span></span> <span data-ttu-id="9d9e6-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9d9e6-111">Read/write.</span></span> <span data-ttu-id="9d9e6-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="9d9e6-112">**String**.</span></span>

<span data-ttu-id="9d9e6-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="9d9e6-113">**Applies To**</span></span>

[<span data-ttu-id="9d9e6-114">Schläuche</span><span class="sxs-lookup"><span data-stu-id="9d9e6-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="9d9e6-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="9d9e6-115">**Tag Syntax**</span></span>

<span data-ttu-id="9d9e6-116"><o: *Elementtyp* = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="9d9e6-116"><o: *element* type=" *expression* "></span></span>

<span data-ttu-id="9d9e6-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="9d9e6-117">**Script Syntax**</span></span>

<span data-ttu-id="9d9e6-118">*Element* . Type = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="9d9e6-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="9d9e6-119">*Ausdruck* = *Element*. Type</span><span class="sxs-lookup"><span data-stu-id="9d9e6-119">*expression*=*element*.type</span></span>

<span data-ttu-id="9d9e6-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="9d9e6-120">**Remarks**</span></span>

<span data-ttu-id="9d9e6-121">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="9d9e6-121">Values include:</span></span>



| <span data-ttu-id="9d9e6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="9d9e6-122">Value</span></span>       | <span data-ttu-id="9d9e6-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d9e6-123">Description</span></span>                                                                                                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d9e6-124">parallel</span><span class="sxs-lookup"><span data-stu-id="9d9e6-124">parallel</span></span>    | <span data-ttu-id="9d9e6-125">Die-Extrusion wird gerendert, sodass der Mittelpunkt der Projektion unendlich weit entfernt ist. Das heißt, die extrusionlinien werden nicht aufeinander abgestimmt (im Gegensatz zu perspektivischen Projektionen).</span><span class="sxs-lookup"><span data-stu-id="9d9e6-125">Extrusion is rendered so that the center of projection is infinitely far away; that is, the extrusion lines do not converge (unlike perspective projections).</span></span> <span data-ttu-id="9d9e6-126">Standard.</span><span class="sxs-lookup"><span data-stu-id="9d9e6-126">Default.</span></span> |
| <span data-ttu-id="9d9e6-127">Perspektive</span><span class="sxs-lookup"><span data-stu-id="9d9e6-127">perspective</span></span> | <span data-ttu-id="9d9e6-128">Die-Extrusion wird in einen Mittelpunkt der Projektion gerendert, der mit dem Verschwinden Punkt für undrehte-Objekte identisch ist.</span><span class="sxs-lookup"><span data-stu-id="9d9e6-128">Extrusion is rendered to a center of projection, which is the same as the vanishing point for unrotated objects.</span></span>                                                       |



 

<span data-ttu-id="9d9e6-129">**Microsoft Office Extensions-Attribut**</span><span class="sxs-lookup"><span data-stu-id="9d9e6-129">**Microsoft Office Extensions Attribute**</span></span>

 

 